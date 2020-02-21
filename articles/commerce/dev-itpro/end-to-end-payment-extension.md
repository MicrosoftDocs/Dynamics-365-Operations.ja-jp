---
title: 支払端末のエンド・ツー・エンド支払統合を作成する
description: このトピックでは、支払端末のエンド・ツー・エンド支払統合を作成する方法について説明します。
author: Reza-Assadi
manager: AnnBe
ms.date: 02/21/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.search.scope: Operations, Retail
ms.custom: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: rassadi
ms.search.validFrom: 2018-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 321660aa78b23b5a74f39a5af42f49ad300e6113
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/01/2020
ms.locfileid: "3004578"
---
# <a name="create-an-end-to-end-payment-integration-for-a-payment-terminal"></a>支払端末のエンド・ツー・エンド支払統合を作成する

[!include [banner](../../includes/banner.md)]

このトピックでは、支払ゲートウェイと直接通信できる支払端末向けに Microsoft Dynamics 365 Retail Modern POS とクラウド POS (POS) の支払統合を記述する方法について説明します。

## <a name="key-terms"></a>重要な用語

| 期間 | 説明 |
|---|---|
| 支払コネクタ | POS に支払ターミナルを統合するために書き込まれた拡張ライブラリです。 |
| 支払プロセッサ | 支払コネクタで使用される商社プロパティを取得するために書き込まれる拡張ライブラリです。 |

## <a name="overview"></a>概要
次の図は、POS を介した支払ターミナルの統合の概要を示しています。 この図では、ローカルのハードウェア ステーションを使用して支払端末と通信を使用することを前提にしていますが、同じパターンを共有のハードウェア ステーションにも適用できます。

![支払コネクタ統合の概要](media/PAYMENTS/PAYMENT-TERMINAL/Overview.jpg)

このトピックでは、支払端末のエンド・ツー・エンド支払統合を作成するために必要な以下の手順について説明します。

- **[支払コネクタの記述](#write-a-payment-connector):** 支払コネクタは POS と支払ターミナルの間の主要な統合ポイントです。 このステップのセクションでは、支払要求 (たとえば、承認、払い戻し、無効化要求) を支払端末に中継できる、新しい支払コネクタを実装し、設定する方法について説明します。 
- **[支払プロセッサの記述](#write-a-payment-processor):** 支払プロセッサは、支払の統合の一部として使用される商社プロパティを定義するために使用します。 このステップのセクションでは、新しい支払プロセッサを実装する方法について説明します。 これには、実装する必要があるインターフェイスおよび従う必要があるパターンに関する情報が含まれています。

## <a name="write-a-payment-connector"></a>支払コネクタの記述
次のこのセクションでは、新しい支払コネクタを記述する方法について説明します。

### <a name="understanding-the-payment-flows"></a>支払フローを理解する
次の図は、POS、ハードウェア ステーション、および支払コネクタ全体にわたるいくつかの支払フロー (トランザクションの開始、カート ラインの更新、承認、キャプチャ、および終了トランザクション) の概要を示しています。

![支払フローの概要](media/PAYMENTS/PAYMENT-TERMINAL/PaymentFlow.jpg)

### <a name="implement-a-payment-connector"></a>支払コネクタの実装
次のこのセクションでは、新しい支払コネクタを実装する方法について説明します。 ここに示す例は、Retailソフトウェアの開発キット (SDK) の **SampleExtensions\HardwareStation\Extension.PaymentSample** フォルダーにある **PaymentDeviceSample** クラスにあります。

#### <a name="implement-the-inamedrequesthandler-interface"></a>INamedRequestHandler インターフェイスの実装
すべての POS 支払関連フローは、ハードウェア ステーションで要求/応答パターンを通じて処理されます。 新しい支払コネクタを作成するプロセスの第一歩は、**Microsoft.Dynamics.Commerce.Runtime.Framework** ライブラリで定義されている **INamedRequestHandler** インターフェイスを実装するクラスを作成することです。

``` csharp
namespace Contoso.Commerce.HardwareStation.PaymentSample 
{ 
    public class PaymentDeviceSample : INamedRequestHandler
    {
        private const string PaymentTerminalDevice = "MOCKPAYMENTTERMINAL";

        /// <summary>
        /// Gets the specify the name of the request handler.
        /// </summary>
        public string HandlerName
        {
              get
            {
                return PaymentDeviceSample.PaymentTerminalDevice;
            }
        }
    }
}
```

**HandlerName** 文字列は、クライアントを通して特定の POS で使用される支払コネクタを構成するために使用されます (このトピックの後半の情報を参照してください)。

#### <a name="implement-supported-payment-requests"></a>サポートされている支払要求の実装
支払関連フローを処理するには、支払コネクタが処理できる、サポートされている要求タイプを定義する必要があります。 また、**実行**メソッドは、コネクタが指定されたメソッドをサポートする各要求をルーティングするために実装する必要があります。 次の例は、サポートされている要求のタイプの完全な一覧と、特定の要求 (すなわち、承認要求) の例を示しています。

``` csharp
namespace Contoso.Commerce.HardwareStation.PaymentSample 
{ 
    /// <summary>
    /// <c>Simulator</c> manager payment device class.
    /// </summary>
    public class PaymentDeviceSample : INamedRequestHandler
    {
        /// <summary>
        /// Gets the collection of supported request types by this handler.
        /// </summary>
        public IEnumerable<Type> SupportedRequestTypes
        {
            get
            {
                return new[]
                {
                    typeof(OpenPaymentTerminalDeviceRequest),
                    typeof(BeginTransactionPaymentTerminalDeviceRequest),
                    typeof(LockPaymentTerminalDeviceRequest),
                    typeof(UpdateLineItemsPaymentTerminalDeviceRequest),
                    typeof(CancelOperationPaymentTerminalDeviceRequest),
                    typeof(AuthorizePaymentTerminalDeviceRequest),
                    typeof(CapturePaymentTerminalDeviceRequest),
                    typeof(VoidPaymentTerminalDeviceRequest),
                    typeof(RefundPaymentTerminalDeviceRequest),
                    typeof(FetchTokenPaymentTerminalDeviceRequest),
                    typeof(EndTransactionPaymentTerminalDeviceRequest),
                    typeof(ClosePaymentTerminalDeviceRequest),
                    typeof(ActivateGiftCardPaymentTerminalRequest),
                    typeof(AddBalanceToGiftCardPaymentTerminalRequest),
                    typeof(GetGiftCardBalancePaymentTerminalRequest),
                    typeof(GetPrivateTenderPaymentTerminalDeviceRequest)
                };
            }
        }

        /// <summary>
        /// Executes the payment device simulator operation based on the incoming request type.
        /// </summary>
        /// <param name="request">The payment terminal device simulator request message.</param>
        /// <returns>Returns the payment terminal device simulator response.</returns>
        public Response Execute(Microsoft.Dynamics.Commerce.Runtime.Messages.Request request)
        {
            ThrowIf.Null(request, "request");

            Type requestType = request.GetType();

            if (requestType == typeof(AuthorizePaymentTerminalDeviceRequest))
            {
                return this.AuthorizePayment((AuthorizePaymentTerminalDeviceRequest)request);
            }
            else if (...)
            {
                ...
            }

            return new NullResponse();
        }

        /// <summary>
        /// Authorize payment.
        /// </summary>
        /// <param name="request">The authorize payment request.</param>
        /// <returns>The authorize payment response.</returns>
        public AuthorizePaymentTerminalDeviceResponse AuthorizePayment(AuthorizePaymentTerminalDeviceRequest request)
        {
            ThrowIf.Null(request, "request");

            PaymentInfo paymentInfo = Utilities.WaitAsyncTask(() => this.AuthorizePaymentAsync(request.Amount, request.Currency, request.VoiceAuthorization, request.IsManualEntry, request.ExtensionTransactionProperties));

            return new AuthorizePaymentTerminalDeviceResponse(paymentInfo);
        }
    }
}
```

#### <a name="full-list-of-supported-request-types"></a>サポートされる要求タイプの完全な一覧
次のテーブルは、支払コネクタが実装できるサポートされているすべての要求のタイプを示しています。

| クラスのリクエスト | 支払フローの説明 |
|---|---|
| OpenPaymentTerminalDeviceRequest | この要求は、販売取引が開始される前に呼び出されます。 支払ターミナルへの接続を確立するために使用されます。 |
| BeginTransactionPaymentTerminalDeviceRequest | この要求は、新しい販売取引が開始されたときに呼び出されます。 支払ターミナルで初期化を処理するために使用されます (たとえば、トランザクション画面の初期化)。 |
| LockPaymentTerminalDeviceRequest | この要求は支払ターミナルがトランザクションに対してロックされている場合、呼び出されます。 |
| UpdateLineItemsPaymentTerminalDeviceRequest | この要求は、カート内の明細行品目が更新されたときに呼び出されます。 |
| AuthorizePaymentTerminalDeviceRequest | この要求は、POS 支払ビューで支払が開始されたときに呼び出されます。 |
| CancelOperationPaymentTerminalDeviceRequest | この要求は、支払いが開始された後、支払い端末で支払いが完了する前に、支払いビュー ダイアログ ボックスで **キャンセル** ボタンを選択すると呼び出されます。 |
| CapturePaymentTerminalDeviceRequest | この要求は、カート内の全額が支払われた時点で、販売取引が終了する前に、各支払い行に対して呼び出されます。 |
| VoidPaymentTerminalDeviceRequest | この要求は、カート内の支払い行が無効になったときに呼び出されます。 |
| RefundPaymentTerminalDeviceRequest | この要求は、払い戻しが行われたときに呼び出されます。 |
| FetchTokenPaymentTerminalDeviceRequest | この要求は、顧客注文の繰延支払いをサポートするために支払トークンをフェッチするために呼び出されます。 |
| EndTransactionPaymentTerminalDeviceRequest | この要求は、販売取引が終了し、すべての支払いが取り込まれたときに呼び出されます。 |
| ClosePaymentTerminalDeviceRequest | この要求は、販売取引の終了後に呼び出されます。 支払ターミナルへの接続を閉じるために使用されます。 |
| ActivateGiftCardPaymentTerminalRequest | この要求は、外部ギフト カードが POS を介して有効化されているときに呼び出されます。 |
| AddBalanceToGiftCardPaymentTerminalRequest | この要求は、外部ギフト カードに残高が追加されるときに呼び出されます。 |
| GetGiftCardBalancePaymentTerminalRequest | この要求は、ギフト カードの残高が取得されるときに呼び出されます。 |
| GetPrivateTenderPaymentTerminalDeviceRequest | この要求は、ギフト カード番号がギフト カード フローの支払い端末から取得されたときに呼び出されます (ギフト カードの発行、ギフト カードによる支払い、ギフト カードへの追加など)。 |
| ExecuteTaskPaymentTerminalDeviceRequest | この拡張要求は、カスタマイズを介して POS から呼び出すことができます。 支払に関連する追加のフローを有効にするために使用されます。 |

##### <a name="openpaymentterminaldevicerequest"></a>OpenPaymentTerminalDeviceRequest
###### <a name="signature"></a>署名
``` csharp
public OpenPaymentTerminalDeviceRequest(string token, string deviceName, SettingsInfo terminalSettings, PeripheralConfiguration deviceConfig, ExtensionTransaction extensionTransactionProperties);
```

###### <a name="variables"></a>変数

| 変動 | 説明 |
|---|---|
| token | 支払い端末が最初のトランザクションのためにロックされたときに生成される一意のトークン値。 |
| deviceName | クライアントの **POS ハードウェア プロファイル** ページで定義されている、デバイスの名前。 |
| terminalSettings | クライアントで定義された支払端末固有の構成プロパティのセット。署名キャプチャの最小額やデビット キャッシュバック限度などです。 |
| deviceConfig | ネットワーク端末の場合の IP アドレスやポートなど、名前/値のペアの形式の支払端末固有の設定プロパティのセット。 |
| extensionTransactionProperties | 名前/値のペアの形式の拡張構成プロパティのセット。 |

##### <a name="begintransactionpaymentterminaldevicerequest"></a>BeginTransactionPaymentTerminalDeviceRequest
###### <a name="signature"></a>署名
``` csharp
public BeginTransactionPaymentTerminalDeviceRequest(string token, string paymentConnectorName, string merchantInformation, string invoiceNumber, bool isTestMode, ExtensionTransaction extensionTransactionProperties)
```

###### <a name="variables"></a>変数

| 変動 | 説明 |
|---|---|
| token | 支払い端末が最初のトランザクションのためにロックされたときに生成される一意のトークン値。 |
| paymentConnectorName | 支払フローの一部として使用される支払コネクタの名前。 この変数は、**IPaymentProcessor** インターフェイスを使用する支払フローと統合する予定がある場合に使用されます。 |
| merchantInformation | クライアントの **POS ハードウェア プロファイル** ページで定義されている商社情報。 |
| invoiceNumber | POS が販売トランザクションを追跡するために生成する一意の請求書番号。 |
| isTestMode | 支払コネクタがテスト モードで使用されているかどうかを示す値。 |
| extensionTransactionProperties | 名前/値のペアの形式の拡張構成プロパティのセット。 |

##### <a name="lockpaymentterminaldevicerequest"></a>LockPaymentTerminalDeviceRequest
###### <a name="signature"></a>署名
``` csharp
public LockPaymentTerminalDeviceRequest(string clientDeviceNumber, string deviceType, string deviceName, bool isExclusive, bool isOverride)
```

###### <a name="variables"></a>変数

| 変動 | 説明 |
|---|---|
| clientDeviceNumber | ロックに使用される固有の POS デバイス番号 |
| deviceType | POS ハードウェア プロファイル (「Windows」など) で構成されるようにロックを取得したデバイス タイプ。 |
| deviceName | POS ハードウェア プロファイル (「MOCKPAYMENTTERMINAL」など) で構成されるようにロックを取得したデバイス タイプ。 |
| isExclusive | 取得したロックが占有されているかどうかを決定します。 | 
| isOverride | この要求が、既存のロックを上書きするかどうかを決定します。 |

##### <a name="updatelineitemspaymentterminaldevicerequest"></a>UpdateLineItemsPaymentTerminalDeviceRequest
###### <a name="signature"></a>署名
``` csharp
public UpdateLineItemsPaymentTerminalDeviceRequest(string token, string totalAmount, string taxAmount, string discountAmount, string subTotalAmount, IEnumerable<ItemInfo> items, ExtensionTransaction extensionTransactionProperties = null)
```

###### <a name="variables"></a>変数

| 変動 | 説明 |
|---|---|
| token | 支払い端末が最初のトランザクションのためにロックされたときに生成される一意のトークン値。 |
| totalAmount | 現在の販売トランザクションでの合計金額。 |
| taxAmount | 現在の販売トランザクションでの税金額。 |
| discountAmount | 現在の販売トランザクションでの割引金額。 |
| subTotalAmount | 現在の販売トランザクションでの小計金額。 |
| 項目 | 表示する明細行品目のリスト。 |
| extensionTransactionProperties | 名前/値のペアの形式の拡張構成プロパティのセット。 |

##### <a name="authorizepaymentterminaldevicerequest"></a>AuthorizePaymentTerminalDeviceRequest
###### <a name="signature"></a>署名
``` csharp
public AuthorizePaymentTerminalDeviceRequest(string token, string paymentConnectorName, decimal amount, string currency, TenderInfo tenderInfo, string voiceAuthorization, bool isManualEntry, ExtensionTransaction extensionTransactionProperties)
```

###### <a name="variables"></a>変数

| 変動 | 説明 |
|---|---|
| token | 支払い端末が最初のトランザクションのためにロックされたときに生成される一意のトークン値。 |
| paymentConnectorName | 支払フローの一部として使用される支払コネクタの名前。 この変数は、**IPaymentProcessor** インターフェイスを使用する支払フローとの統合がある場合に使用されます。 |
| 金額 | 承認する金額。 |
| 通貨 | 承認する金額の通貨。 |
| tenderInfo | 外部ソースから取得された POS から送信されるカード情報 (外部ソースがある場合)。 |
| voiceAuthorization | 音声認証が必要な場合は、POS から送信される音声承認コード。 |
| isManualEntry | カード番号を手動で入力されたかどうかを定義する値。 |
| extensionTransactionProperties | 名前/値のペアの形式の拡張構成プロパティのセット。 |

###### <a name="response"></a>応答
**AuthorizePaymentCardPaymentResponse** 応答オブジェクトは、**AuthorizePaymentTerminalDeviceRequest** 要求が処理されたときに返される必要があります。 応答には、次の必須プロパティを持つ **PaymentInfo** オブジェクトのインスタンスが含まれている必要があります。

| プロパティ | 説明 |
|---|---|
| ApprovedAmount | トランザクションに対して承認された金額。 |
| CardNumberMasked | マスクされたクレジット カード番号。 この値には、少なくとも POS 内の在庫置場範囲の参照をサポートするため、クレジット カードの最初の桁が含まれている必要があります。 (ほとんどのデバイスは、最初の 6 桁と最後の 4 桁を返します。) |
| CardType | **Microsoft.Dynamics.Commerce.HardwareStation.CardPayment.CardType** エンティティを使用して支払い (**クレジット** または **デビット** など) に使われたカードのタイプ。 |
| CashbackAmount | 借方トランザクションの場合、キャッシュ バック金額は支払のターミナルで定義されました。 |
| エラー | 承認呼び出し中に発生したエラーのリスト。 |
| IsApproved | 支払が承認されたかどうかを示すフラグ。 |
| PaymentSdkData | 承認/返金と、キャプチャ/呼び出しの無効化またはクロスチャネルの支払操作の間の状態をサポートするために使用される応答データ。 |

**PaymentSdkData** プロパティには、次のデータを含める必要があります。

| 名前空間 | 氏名 | 説明 | サンプル値 |
|---|---|---|---|
| コネクタ | ConnectorName | このトピックの後半にある「支払プロセッサの記述」セクションで説明している、トランザクションに使用される **IPaymentProcessor**インターフェイスの名前です。 |
| AuthorizationResponse | プロパティ | 承認応答のリスト。 | 次の表を参照してください。 |

**PaymentSdkData** プロパティの **プロパティ** フィールドには、次のフィールドを含める必要があります。

| 名前空間 | 氏名 | 説明 | サンプル値 |
|---|---|---|---|
| AuthorizationResponse | ApprovedAmount | トランザクションに対して承認された金額。 | 28.08 m |
| AuthorizationResponse | AvailableBalance | カードの使用可能な残高。 | 100.00m |
| AuthorizationResponse | ApprovalCode | トランザクションの承認コード。 | Z123456 |
| AuthorizationResponse | ProviderTransactionId | 支払いプロバイダーのトランザクション識別子。 | 123456789 |
| AuthorizationResponse | AuthorizationResult | 権限呼び出しの結果。 | AuthorizationResult.Success.ToString() |
| AuthorizationResponse | ExternalReceipt | 支払プロバイダーからの外部レシート データ。 | \<ReceiptData\>...\</ReceiptData\> |
| AuthorizationResponse | TerminalId | 支払を処理した端末の一意の識別子。 | 000001 |

次の例は、**PaymentSdkData** オブジェクトを作成する方法を示しています。

``` csharp
List<PaymentProperty> paymentSdkProperties = new List<PaymentProperty>();
paymentSdkProperties.Add(new PaymentProperty(GenericNamespace.Connector, ConnectorProperties.ConnectorName, "TestConnector"));

List<PaymentProperty> paymentSdkAuthorizationProperties = new List<PaymentProperty>();
paymentSdkAuthorizationProperties.Add(new PaymentProperty(GenericNamespace.AuthorizationResponse, AuthorizationResponseProperties.ApprovedAmount, 28.08m));
paymentSdkAuthorizationProperties.Add(new PaymentProperty(GenericNamespace.AuthorizationResponse, AuthorizationResponseProperties.AvailableBalance, 100.00m));
paymentSdkAuthorizationProperties.Add(new PaymentProperty(GenericNamespace.AuthorizationResponse, AuthorizationResponseProperties.ApprovalCode, "Z123456"));
paymentSdkAuthorizationProperties.Add(new PaymentProperty(GenericNamespace.AuthorizationResponse, AuthorizationResponseProperties.ProviderTransactionId, "123456789"));
paymentSdkAuthorizationProperties.Add(new PaymentProperty(GenericNamespace.AuthorizationResponse, AuthorizationResponseProperties.AuthorizationResult, AuthorizationResult.Success.ToString()));
paymentSdkAuthorizationProperties.Add(new PaymentProperty(GenericNamespace.AuthorizationResponse, TransactionDataProperties.TerminalId, "000001"));

paymentSdkProperties.Add(new PaymentProperty(GenericNamespace.AuthorizationResponse, AuthorizationResponseProperties.Properties, paymentSdkAuthorizationProperties.ToArray()));

string paymentSdkData = PaymentProperty.ConvertPropertyArrayToXML(paymentSdkProperties.ToArray());
```

支払端末がレシートを返す場合、先ほど説明した **ExternalReceipt** オブジェクトで次のデータを設定し、POS を介して印刷することができます。

```xml
<ReceiptData>
    <Receipt Type='Customer'>
        <Line>Line 1 of receipt.</Line>
        <Line>Line 2 of receipt.</Line>
    </Receipt>
    <Receipt Type='Merchant'>
        <Line>Line 1 of receipt.</Line>
        <Line>Line 2 of receipt.</Line>
    </Receipt>
</ReceiptData>
```

###### <a name="other-considerations"></a>その他の考慮事項
支払端末が 1 つの呼び出しでの要求を承認し、キャプチャし (つまり*迅速なキャプチャ*が発生する場合)、出納係が取引を無効にすることを希望する場合、支払い端末では即時回収の取消がサポートされている必要があります。 迅速なキャプチャが無効なとき、無効化要求が失敗した場合、レジ担当者は、ローカルで支払を無効にするかどうかを求められます。 レジ担当者が**はい**と選択した場合、入札は POS でのみ無効になります。 支払を無効にするために支払ターミナルに対して行われる呼び出しはありません。 基本的には、この動作により、支払ターミナルの支払を無効にできなくなった場合レジ担当者は POS をブロック解除することができます。 ただし、銀行が取り消すまでの 3 ~ 5日間はロックが続くため、この動作には問題が生じますが、迅速なキャプチャのための支払いが行われます。 したがって、重複した支払いが発生する可能性があります。

##### <a name="canceloperationpaymentterminaldevicerequest"></a>CancelOperationPaymentTerminalDeviceRequest
###### <a name="signature"></a>署名
``` csharp
public CancelOperationPaymentTerminalDeviceRequest(string token)
```

###### <a name="variables"></a>変数

| 変動 | 説明 |
|---|---|
| token | 支払い端末が最初のトランザクションのためにロックされたときに生成される一意のトークン値。 |

##### <a name="capturepaymentterminaldevicerequest"></a>CapturePaymentTerminalDeviceRequest
###### <a name="signature"></a>署名
``` csharp
public CapturePaymentTerminalDeviceRequest(string token, decimal amount, string currency, string paymentPropertiesXml, ExtensionTransaction extensionTransactionProperties)
```

###### <a name="variables"></a>変数

| 変動 | 説明 |
|---|---|
| token | 支払い端末が最初のトランザクションのためにロックされたときに生成される一意のトークン値。 |
| 金額 | 取得する金額。 |
| 通貨 | 取得する金額の通貨。 |
| paymentPropertiesXml | **AuthorizePaymentTerminalDeviceRequest** 要求または **RefundPaymentTerminalDeviceRequest** 要求によって返され、要求間のステートフル プロパティをサポートするために使用される **PaymentSdkData** オブジェクトのコンテンツ。 |
| extensionTransactionProperties | 名前/値のペアの形式の拡張構成プロパティのセット。 |

###### <a name="other-considerations"></a>その他の考慮事項
支払端末が 1 つの呼び出しでの要求を承認およびキャプチャする場合、**CapturePaymentTerminalDeviceRequest** 要求はノーオーペレーションである必要があり、すぐに返す必要があります。

支払端末が、キャプチャ呼び出しを処理する許可要求からの状態を必要とする場合、プロパティは、先に説明した **AuthorizePaymentTerminalDeviceResponse** 要求の **PaymentSdkData** オブジェクトに格納され、 **CapturePaymentTerminalDeviceRequest** 要求の **paymentPropertiesXml** 変数を渡します。

##### <a name="voidpaymentterminaldevicerequest"></a>VoidPaymentTerminalDeviceRequest
###### <a name="signature"></a>署名
``` csharp
public VoidPaymentTerminalDeviceRequest(string token, string paymentConnectorName, decimal amount, string currency, TenderInfo tenderInfo, string paymentPropertiesXml, ExtensionTransaction extensionTransactionProperties)
```

###### <a name="variables"></a>変数

| 変動 | 説明 |
|---|---|
| token | 支払い端末が最初のトランザクションのためにロックされたときに生成される一意のトークン値。 |
| paymentConnectorName | 支払フローの一部として使用される支払コネクタの名前。 この変数は、**IPaymentProcessor** インターフェイスを使用する支払フローとの統合がある場合に使用されます。 |
| 金額 | 支払いが無効になる金額。 |
| 通貨 | 支払いが無効になる通貨。 |
| tenderInfo | 外部ソースから取得された POS から送信されるカード情報 (外部ソースがある場合)。 |
| paymentPropertiesXml | **AuthorizePaymentTerminalDeviceRequest** 要求または **RefundPaymentTerminalDeviceRequest** 要求によって返され、要求間のステートフル プロパティをサポートするために使用される **PaymentSdkData** オブジェクトのコンテンツ。 |
| extensionTransactionProperties | 名前/値のペアの形式の拡張構成プロパティのセット。 |

##### <a name="refundpaymentterminaldevicerequest"></a>RefundPaymentTerminalDeviceRequest
###### <a name="signature"></a>署名
``` csharp
public RefundPaymentTerminalDeviceRequest(string token, string paymentConnectorName, TenderInfo tenderInfo, decimal amount, string currency, bool isManualEntry, ExtensionTransaction extensionTransactionProperties)
```

###### <a name="variables"></a>変数

| 変動 | 説明 |
|---|---|
| token | 支払い端末が最初のトランザクションのためにロックされたときに生成される一意のトークン値。 |
| paymentConnectorName | 支払フローの一部として使用される支払コネクタの名前。 この変数は、**IPaymentProcessor** インターフェイスを使用する支払フローとの統合がある場合に使用されます。 |
| tenderInfo | 外部ソースから取得された POS から送信されるカード情報 (外部ソースがある場合)。 |
| 金額 | 払い戻す金額。 |
| 通貨 | 払い戻す金額の通貨。 |
| isManualEntry | カード番号を手動で入力されたかどうかを定義する値。 |
| extensionTransactionProperties | 名前/値のペアの形式の拡張構成プロパティのセット。 |

##### <a name="fetchtokenpaymentterminaldevicerequest"></a>FetchTokenPaymentTerminalDeviceRequest
###### <a name="signature"></a>署名
``` csharp
public FetchTokenPaymentTerminalDeviceRequest(string token, bool isManualEntry, ExtensionTransaction extensionTransactionProperties)
```

###### <a name="variables"></a>変数

| 変動 | 説明 |
|---|---|
| token | 支払い端末が最初のトランザクションのためにロックされたときに生成される一意のトークン値。 |
| isManualEntry | カード番号を手動で入力されたかどうかを定義する値。 |
| extensionTransactionProperties | 名前/値のペアの形式の拡張構成プロパティのセット。 |

##### <a name="endtransactionpaymentterminaldevicerequest"></a>EndTransactionPaymentTerminalDeviceRequest
##### <a name="signature"></a>署名
``` csharp
public EndTransactionPaymentTerminalDeviceRequest(string token, ExtensionTransaction extensionTransactionProperties)
```

###### <a name="variables"></a>変数

| 変動 | 説明 |
|---|---|
| token | 支払い端末が最初のトランザクションのためにロックされたときに生成される一意のトークン値。 |
| extensionTransactionProperties | 名前/値のペアの形式の拡張構成プロパティのセット。 |

##### <a name="closepaymentterminaldevicerequest"></a>ClosePaymentTerminalDeviceRequest
###### <a name="signature"></a>署名
``` csharp
public ClosePaymentTerminalDeviceRequest(string token, ExtensionTransaction extensionTransactionProperties)
```

###### <a name="variables"></a>変数

| 変動 | 説明 |
|---|---|
| token | 支払い端末が最初のトランザクションのためにロックされたときに生成される一意のトークン値。 |
| extensionTransactionProperties | 名前/値のペアの形式の拡張構成プロパティのセット。 |

##### <a name="activategiftcardpaymentterminalrequest"></a>ActivateGiftCardPaymentTerminalRequest
###### <a name="signature"></a>署名
``` csharp
public ActivateGiftCardPaymentTerminalRequest(string token, string paymentConnectorName, decimal amount, string currencyCode, TenderInfo tenderInfo, ExtensionTransaction extensionTransactionProperties)
```

###### <a name="variables"></a>変数

| 変動 | 説明 |
|---|---|
| token | 支払い端末が最初のトランザクションのためにロックされたときに生成される一意のトークン値。 |
| paymentConnectorName | 支払フローの一部として使用される支払コネクタの名前。 この変数は、**IPaymentProcessor** インターフェイスを使用する支払フローとの統合がある場合に使用されます。 |
| 金額 | 有効化中にギフト カードに追加する初期金額。 |
| 通貨 | 有効化中にギフト カードに追加する初期金額の通貨。 |
| tenderInfo | 外部ソースから取得された POS から送信されるカード情報 (外部ソースがある場合)。 |
| extensionTransactionProperties | 名前/値のペアの形式の拡張構成プロパティのセット。 |

##### <a name="addbalancetogiftcardpaymentterminalrequest"></a>AddBalanceToGiftCardPaymentTerminalRequest
###### <a name="signature"></a>署名
``` csharp
public AddBalanceToGiftCardPaymentTerminalRequest(string token, string paymentConnectorName, decimal amount, string currencyCode, TenderInfo tenderInfo, ExtensionTransaction extensionTransactionProperties)
```

###### <a name="variables"></a>変数

| 変動 | 説明 |
|---|---|
| token | 支払い端末が最初のトランザクションのためにロックされたときに生成される一意のトークン値。 |
| paymentConnectorName | 支払フローの一部として使用される支払コネクタの名前。 この変数は、**IPaymentProcessor** インターフェイスを使用する支払フローとの統合がある場合に使用されます。 |
| 金額 | ギフト カードに追加される金額。 |
| 通貨 | ギフト カード残高に追加する金額の通貨。 |
| tenderInfo | 外部ソースから取得された POS から送信されるカード情報 (外部ソースがある場合)。 |
| extensionTransactionProperties | 名前/値のペアの形式の拡張構成プロパティのセット。 |

##### <a name="getgiftcardbalancepaymentterminalrequest"></a>GetGiftCardBalancePaymentTerminalRequest
###### <a name="signature"></a>署名
``` csharp
public GetGiftCardBalancePaymentTerminalRequest(string token, string paymentConnectorName, string currencyCode, TenderInfo tenderInfo, ExtensionTransaction extensionTransactionProperties)
```

###### <a name="variables"></a>変数

| 変動 | 説明 |
|---|---|
| token | 支払い端末が最初のトランザクションのためにロックされたときに生成される一意のトークン値。 |
| paymentConnectorName | 支払フローの一部として使用される支払コネクタの名前。 この変数は、**IPaymentProcessor** インターフェイスを使用する支払フローとの統合がある場合に使用されます。 |
| 通貨 | ギフト カード残高を取得するための通貨。 |
| tenderInfo | 外部ソースから取得された POS から送信されるカード情報 (外部ソースがある場合)。 |
| extensionTransactionProperties | 名前/値のペアの形式の拡張構成プロパティのセット。 |

##### <a name="getprivatetenderpaymentterminaldevicerequest"></a>GetPrivateTenderPaymentTerminalDeviceRequest
###### <a name="signature"></a>署名
``` csharp
public GetPrivateTenderPaymentTerminalDeviceRequest(string token, decimal amount, bool declined, bool isSwipe, ExtensionTransaction extensionTransactionProperties)
```

###### <a name="variables"></a>変数

| 変動 | 説明 |
|---|---|
| token | 支払い端末が最初のトランザクションのためにロックされたときに生成される一意のトークン値。 |
| 金額 | POS に設定された金額。 (通常、この変数は、カード番号を取得したときに支払ターミナルの金額を表示するために使用されます。) |
| declined | この値は廃止されています。 |
| isSwipe | 支払ターミナルで読み取りまたは手動入力によってカード番号を取得する必要があるかどうかを決定する値。 |
| extensionTransactionProperties | 名前/値のペアの形式の拡張構成プロパティのセット。 |

##### <a name="executetaskpaymentterminaldevicerequest"></a>ExecuteTaskPaymentTerminalDeviceRequest
###### <a name="signature"></a>署名
``` csharp
public ExecuteTaskPaymentTerminalDeviceRequest(string token, string task, ExtensionTransaction extensionTransactionProperties)
```

###### <a name="variables"></a>変数

| 変動 | 説明 |
|---|---|
| token | 支払い端末が最初のトランザクションのためにロックされたときに生成される一意のトークン値。 |
| タスク | 実行されているタスクの一意の識別子。 |
| extensionTransactionProperties | 名前/値のペアの形式の拡張構成プロパティのセット。 |

#### <a name="state-in-the-payment-connector"></a>支払コネクタの状態
支払いコネクターは、POS 内のインプロセス ハードウェア ステーションを通じてホストされているとき、dllhost.exe プロセスの一部としてホストすることができます。 または、 Microsoft Internet Information Services (IIS) に基づくハードウェア ステーションでホストされている場合、w3wp.exe プロセスとして支払コネクタをホストすることができます。 状況によっては、支払フローの間または最中に両方のプロセスを終了したり、応答を停止したりできます。 したがって、支払コネクタには状態依存性がなく、以前に説明した支払フロー関連の要求のいずれかの時点で終了すると回復することができるようにすることをお勧めします。

### <a name="configure-the-payment-connector-in-the-hardware-station-config"></a>ハードウェア ステーションのコンフィギュレーションで支払コネクタをコンフィギュレーションする
ハードウェア ステーションが支払コネクタを読み込むようにするために、対応するアセンブリ参照を **HardwareStation.Extension.config** ファイルに設定する必要があります。このファイルは Retail SDK の **Assets** フォルダーにあります。

``` xml
<?xml version="1.0" encoding="utf-8"?>
<hardwareStationExtension>
    <composition>
        <!-- 
        Register your own assemblies or types here. The following example registers NewPeripheralDevice 
        (and all its request handlers). Any other services are not being overridden:

        <add source="type" 
            value="Contoso.Commerce.HardwareStation.NewPeripheralDevice, Contoso.Commerce.HardwareStation.NewPeripheralDevice" />
        <add source="assembly" 
            value="Contoso.Commerce.HardwareStation.NewPeripheralDevice” />
        -->
        <add source="assembly" value="Contoso.Commerce.HardwareStation.PaymentSample" />
    </composition>
</hardwareStationExtension>
```

### <a name="configure-the-payment-connector-on-the-pos-hardware-profile-page-in-the-client"></a>クライアントの POS ハードウェア プロファイル ページで支払コネクタをコンフィギュレーションする
POS にロードする正しい支払コネクタを決定するには、次の図に示すように、クライアントの **POS ハードウェア プロファイル** ページの **PIN パッド** クイック タブで、**デバイス名**フィールドの **PaymentTerminalDevice** プロパティの値を設定する必要があります。

![クライアントの POS ハードウェア プロファイル ページで支払コネクタをコンフィギュレーションする](media/PAYMENTS/PAYMENT-TERMINAL/SamplePaymentDeviceConfigurInAx.jpg)

## <a name="write-a-payment-processor"></a>支払プロセッサの記述
通常は、支払ゲートウェイへの直接接続が確立された場合にのみ、支払プロセスが使用されます。 このシナリオは、カードが存在しない販売取引またはより複雑なカードが存在するシナリオで最も頻繁に発生します。 また、支払プロセッサは、クライアントの **POS ハードウェア プロファイル** ページを使用してコンフィギュレーションされている商社プロパティを処理するために使用されます。

> [!NOTE]
> 支払プロセッサは、支払要求がすべて支払ターミナルを使用して直接処理され、商社プロパティを POS を使用して設定する必要がない場合でも、現在のところは必要です。

### <a name="understanding-the-merchant-properties-flows"></a>商社プロパティ フローを理解する
次のセクションでは、クライアントの **POS ハードウェア プロファイル** ページでの商社プロパティの設定方法と、POS での支払フロー中に支払コネクタにこれらのプロパティを渡す方法について説明します。

#### <a name="set-merchant-properties-on-the-pos-hardware-profile-page-in-the-client"></a>クライアントの POS ハードウェア プロファイル ページで商社プロパティを設定
次の図は、クライアントの **POS ハードウェア プロファイル** ページで商社プロパティを設定する方法を示しています。 マーチャントプロパティを設定するには、**IPaymentProcessor** ライブラリで定義されている **Microsoft.Dynamics.Retail.PaymentSDK** インターフェイスを実装する必要があります。 **GetMerchantAccountPropertyMetadata** と **ValidateMerchantAccount** の 2 つのインターフェイス メソッドが必要です。

![クライアントの POS ハードウェア プロファイル ページで商社プロパティを設定する](media/PAYMENTS/PAYMENT-TERMINAL/MerchantPropertiesAXFlow.jpg)

#### <a name="set-merchant-properties-on-payment-connector-during-pos-sales-transaction"></a>POS 販売トランザクションの間に支払コネクタで商社プロパティを設定
次の図は、**BeginTransactionPaymentTerminalDeviceRequest** 要求の間に Commerce Scale Unit を介してデータベースから商社プロパティを取得して支払コネクタに渡す仕組みを示しています。

![POS 支払フロー時に支払コネクタに商社プロパティを設定](media/PAYMENTS/PAYMENT-TERMINAL/MerchantPropertiesPOSFlow.jpg)

### <a name="implement-the-ipaymentprocessor-interface"></a>IPaymentProcessor インターフェイスの実装
支払フローに関連するマーチャント プロパティを処理するには、**Microsoft.Dynamics.Retail.PaymentSDK** ライブラリで定義されている **IPaymentProcessor** インターフェイスを実装する必要があります。 次の例は、2 つの必須インターフェイス メソッド、**GetMerchantAccountPropertyMetadata** と **ValidateMerchantAccount** を実装する方法を示しています。. 他のインターフェイス メソッドは、空白にできます (たとえば、**FeatureNotSupportedException** を返すことができます)。

``` csharp
/// <summary>
/// SampleConnector class (Portable Class Library version).
/// </summary>
public class SampleConnector : IPaymentProcessor
{
    /// <summary>
    /// GetMerchantAccountPropertyMetadata returns the merchant account properties need by the payment provider.
    /// </summary>
    /// <param name="request">Request object.</param>
    /// <returns>
    /// Response object.
    /// </returns>
    public Response GetMerchantAccountPropertyMetadata(Request request)
    {
        string methodName = "GetMerchantAccountPropertyMetadata";

        // Check null request
        List<PaymentError> errors = new List<PaymentError>();
        if (request == null)
        {
            errors.Add(new PaymentError(ErrorCode.InvalidRequest, "Request is null."));
            return PaymentUtilities.CreateAndLogResponseForReturn(methodName, this.Name, Platform, locale: null, properties: null, errors: errors);
        }

        // Prepare response
        List<PaymentProperty> properties = new List<PaymentProperty>();
        PaymentProperty property;
        property = new PaymentProperty(
            GenericNamespace.MerchantAccount,
            MerchantAccountProperties.AssemblyName,
            this.GetAssemblyName());
        property.SetMetadata("Assembly Name:", "The assembly name of the test provider", false, true, 0);
        properties.Add(property);

        Response response = new Response();
        response.Locale = request.Locale;
        response.Properties = properties.ToArray();
        if (errors.Count > 0)
        {
            response.Errors = errors.ToArray();
        }

        PaymentUtilities.LogResponseBeforeReturn(methodName, this.Name, Platform, response);
        return response;
    }

    /// <summary>
    /// ValidateMerchantAccount the passed merchant account properties with the payment provider.
    /// </summary>
    /// <param name="request">Request object to validate.</param>
    /// <returns>
    /// Response object.
    /// </returns>
    public Response ValidateMerchantAccount(Request request)
    {
        string methodName = "ValidateMerchantAccount";

        // Convert request
        ValidateMerchantAccountRequest validateRequest = null;
        try
        {
            validateRequest = ValidateMerchantAccountRequest.ConvertFrom(request);
        }
        catch (SampleException ex)
        {
            return PaymentUtilities.CreateAndLogResponseForReturn(methodName, this.Name, Platform, locale: request == null ? null : request.Locale, properties: null, errors: ex.Errors);
        }

        // Validate merchant account
        List<PaymentError> errors = new List<PaymentError>();
        ValidateMerchantProperties(validateRequest, errors);
        if (errors.Count > 0)
        {
            return PaymentUtilities.CreateAndLogResponseForReturn(methodName, this.Name, Platform, validateRequest.Locale, errors);
        }

        // Create response
        var validateResponse = new ValidateMerchantAccountResponse(validateRequest.Locale, validateRequest.ServiceAccountId, this.Name);

        // Convert response and return
        Response response = ValidateMerchantAccountResponse.ConvertTo(validateResponse);
        PaymentUtilities.LogResponseBeforeReturn(methodName, this.Name, Platform, response);
        return response;
    }
}
```

#### <a name="required-merchant-property-fields"></a>必須商社プロパティ フィールド
次のテーブルに、**GetMerchantAccountPropertyMetadata** メソッドの一部として設定する必要のある商社プロパティのフィールドを示します。

| 名前空間 | 氏名 | サンプル値\* |
|---|---|---|
| MerchantAccount | PortableAssemblyName | Contoso.Microsoft.PaymentsSample |
| MerchantAccount | ServiceAccountId | f35989c8-e571-4de1-862a-996c82a2e6b6 |
| MerchantAccount | SupportedCurrencies | AUD、BRL、CAD、CHF、CNY、CZK、DKK、EUR、GBP、HKD、HUF、INR、JPY、KPW、KRW、MXN、NOK、NZD、PLN、SEK、SGD、TWD、USD、ZAR |
| MerchantAccount | SupportedTenderTypes | Visa;MasterCard;Amex;Discover;Debit |

\* この列のサンプル値を、独自の支払プロセッサの固有値に置き換える **必要があります** 。
