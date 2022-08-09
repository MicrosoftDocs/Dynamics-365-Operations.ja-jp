---
title: POS 要求ハンドラーのオーバーライド
description: この記事では、POS 要求ハンドラーを上書きする方法について説明します。
author: mugunthanm
ms.date: 07/13/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer
ms.reviewer: tfehr
ms.custom: 68673
ms.assetid: 72a63836-2908-45fa-b1a6-3b1c499a19a2
ms.search.region: Global
ms.author: mumani
ms.search.validFrom: 209/07/2018
ms.dyn365.ops.version: AX 7.3.5
ms.openlocfilehash: df00c7ec306754ba06b60458bfdfa2d966d96349
ms.sourcegitcommit: 28a726b3b0726ecac7620b5736f5457bc75a5f84
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/29/2022
ms.locfileid: "9070808"
---
# <a name="override-pos-request-handler"></a>POS 要求ハンドラーのオーバーライド

[!include [banner](../includes/banner.md)]

この記事では、POS 要求ハンドラーを上書きする方法について説明します。 POS ビジネス ロジックをオーバーライドするための拡張パターンを導入しました。 コア POS ビジネス フローにビジネス ロジックを変更/追加するシナリオがある場合、このパターンに従うことができます。

たとえば、シリアル品目を販売する場合、スキャン後、POS にはその品目のシリアル番号を入力するダイアログ ボックスが表示されます。 コードを使用してシリアル番号を入力することでシリアル番号プロセスを自動化する場合、このシリアル番号要求ハンドラーをオーバーライドしてカスタム ビジネス ロジックを使用できます。 POS のビジネス ロジックのほとんどは、要求ハンドラーで実装されます。ただし、関連する要求ハンドラーをオーバーライドして、ビジネス フローに従って応答を返すことができます。

> [!NOTE]
> すべての要求ハンドラー ロジックがカスタマイズ用に公開されるわけではありません。 ビジネス ロジックをカスタマイズする場合で、その要求ハンドラーがオーバーライド可能でない場合、サポート チケットを作成するか、LCS 機能拡張ツールでリクエストを登録します。

## <a name="pos-request-handler-logic-exposed-for-overriding"></a>オーバーライドするために公開される POS 要求ハンドラー ロジック

この一覧は、[Microsoft Dynamics 365 Finance - バージョン 7.3.5](https://fix.lcs.dynamics.com/Issue/Details?kb=4456209&bugId=235124&qc=9fef9e411bd4f715508205b6c65b16afdc4096cea0f15e1535c3d8e3f13716c1) に基づいています。

毎月の更新プログラムのたびに、拡張ポイントが追加されるため、完全な一覧については Retail SDK で Pos.api.d.ts ファイルをチェックしてください。

## <a name="cart-extension-handlers"></a>買い物カゴ拡張ハンドラー

| 要求名                           | 説明                                                                              |
|--------------------------------------------|----------------------------------------------------------------------------------------------|
| AddTenderLineToCartClientRequestHandler    | このハンドラーは、カートに支払/入金方法 (支払) 明細行を追加するときに実行されます。                          |
| GetKeyedInPriceClientRequestHandler        | このハンドラーは、販売時に、価格内にコンフィギュレーション キーを持つ品目を追加するときに実行されます。 |
| GetPickupDateClientRequestHandler          | 顧客注文時に集荷日を選択するときに実行されます。                                  |
| GetShippingDateClientRequestHandler        | 顧客注文時に出荷日を選択するときに実行されます。                                |
| ShowChangeDueClientRequestHandler          | トランザクションの終了時に期日の変更ダイアログ ボックスが表示されるときに実行されます。                             |
| GetReceiptEmailAddressClientRequestHandler | 受信者のメール アドレスを取得するときに実行されます。                                                 |
| DepositOverrideOperationRequestHandler     | 預金をオーバーライドするときに実行されます。                                                          |
| GetShippingChargeClientRequestHandler      | 顧客注文フロー中に開始された出荷費用ワークフローを取得するときに実行されます。                                                             |
| GetKeyedInPriceClientRequestHandler      | [製品価格] ダイアログ ボックスのキーが表示されたときに実行されます。                                                           |

## <a name="payment-extension-handler"></a>支払拡張機能ハンドラー

| 要求名                                 | 説明                                                                                                                                  |
|--------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| GetGiftCardByIdServiceRequestHandler             | このハンドラーは、ギフト カード ID を受け取ると実行されます。                                                                                           |
| GetPaymentCardTypeByBinRangeClientRequestHandler | このハンドラーは、Visa や Master Card などのカード タイプを POS が取得するときに実行されます。 これは、カード支払/入金の明細行の処理中の HQ コンフィギュレーションに基づきます。 |

## <a name="peripherals-request-handler"></a>周辺機器要求ハンドラー

| 要求名                                                  | 説明                                                                                                                                                     |
|---------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| CardPaymentAuthorizePaymentRequestHandler                     | カード支払が承認されたときに実行されます。                                                                                                                       |
| CardPaymentCapturePaymentRequestHandler                       | カード支払が取得されたときに実行されます。                                                                                                                         |
| CardPaymentExecuteTaskRequestHandler                          | カスタム タスクを実行するために使用します。 このハンドラーは、主に、サポートされていない支払コネクタを使用するカスタム機能の拡張機能用です。       |
| CardPaymentRefundPaymentRequestHandler                        | カード支払が払戻しされたときに実行されます。                                                                                                                         |
| CardPaymentVoidPaymentRequestHandler                          | カード支払が無効化されたときに実行されます。                                                                                                                           |
| CardPaymentBeginTransactionRequestHandler                     | カード支払が開始されたときに実行されます。                                                                                                                        |
| CardPaymentEndTransactionRequestHandler                       | カード支払が終了したときに実行されます。                                                                                                                            |
| CardPaymentEnquireGiftCardBalancePeripheralRequestHandler     | ギフト カードの残高照会が行われるときに実行されます。                                                                                                                |
| PaymentTerminalAuthorizePaymentActivityRequestHandler         | 支払ターミナル/デバイスを使用してカード支払が承認されたときに実行 されます。                                                                                         |
| PaymentTerminalAuthorizePaymentRequestHandler                 | 支払ターミナル/デバイスを使用してカード支払が承認されたときに実行 されます。                                                                                         |
| PaymentTerminalEnquireGiftCardBalancePeripheralRequestHandler | 支払ターミナル/デバイスを使用してギフト カードの残高照会が行われるときに実行 されます。                                                                                  |
| PaymentTerminalExecuteTaskRequestHandler                      | カスタム タスクを実行するために使用します。 このハンドラーは、主に、サポートされていない支払ターミナル/デバイスを使用するカスタム機能の拡張機能用です。 |
| PaymentTerminalRefundPaymentRequestHandler                    | 支払ターミナル/デバイスを使用してカード支払が払戻しされたときに実行されます。                                                                                           |
| PaymentTerminalUpdateLinesRequestHandler                      | POS が表示目的で明細行品目の詳細を支払デバイスに送信するときに実行されます。                                                                                 |
| PaymentTerminalVoidPaymentRequestHandler                      | 支払ターミナル/デバイスを使用してカード支払が無効化されたときに実行されます。                                                                                             |
| PaymentTerminalBeginTransactionRequestHandler                 | 支払ターミナル/デバイスを使用してカード支払が開始されたときに実行されます。                                                                                          |
| PaymentTerminalCancelOperationRequestHandler                  | 支払端末/デバイスを使用してカード支払がキャンセルされたときに実行されます。                                                                                          |
| PaymentTerminalEndTransactionRequestHandler                   | 支払ターミナル/デバイスを使用してカード支払が終了したときに実行されます。                                                                                              |
| CashDrawerOpenRequestHandler                                  | キャッシュ ドロワー オープン要求が POS によって開始されるときに実行されます。                                                                                                     |
| PaymentTerminalActivateGiftCardPeripheralRequestHandler       | POS により開始されたギフト カード要求をアクティブにしたときに実行されます。                                                                                                     |
| PaymentTerminalAddBalanceToGiftCardPeripheralRequestHandler   | POS により開始されたギフト カード要求に残高を追加したときに実行されます。|

## <a name="scan-request-handler"></a>スキャン要求ハンドラー

| 要求名                      | 説明                                                    |
|-----------------------------------|----------------------------------------------------------------|
| GetScanResultClientRequestHandler | スキャンするか、POS トランザクション画面テンキーで入力するときに実行されます。 |

## <a name="store-fulfillment-request-handler"></a>店舗フルフィルメント要求ハンドラー

| 要求名                         | 説明                                                          |
|--------------------------------------|----------------------------------------------------------------------|
| PrintPackingSlipClientRequestHandler | 店舗フルフィルメント ビューから梱包明細を印刷するときに実行されます。 |
| MarkAsPickedServiceRequestHandler    | 店舗フルフィルメント ビューからピッキングされた販売注文明細行をマークするときに実行されます。 |

## <a name="store-operations-request-handler"></a>店舗運営要求ハンドラー

| 要求名                                        | 説明                                                        |
|---------------------------------------------------- |--------------------------------------------------------------------|
| CreateTenderRemovalTransactionClientRequestHandler  | POS で支払/入金の削除操作を行うときに実行されます。              |
| CreateFloatEntryTransactionClientRequestHandler     | POS で釣銭入力操作を行うときに実行されます。                 |
| SelectZipCodeInfoClientRequestHandler               | POS で住所の追加/編集ビューで郵便番号を入力するときに実行されます。 |
| CreateStartingAmountTransactionClientRequestHandler | POS で開始金額申告を行うときに実行されます。 |
| LoyaltyCardPointsBalanceOperationRequestHandler     | POS でロイヤルティ カード残高操作を行うときに実行されます。 |
| GetReportParametersClientRequestHandler     | レポート パラメーターを使用するときに実行されます。 POS レポートに入力パラメーターが必要な場合は、このダイアログが実行されてパラメーターを取得します。 |
| GetPickingAndReceivingOrdersClientRequestHandler | 注文がピッキングおよび入荷処理に対してフェッチされると実行されます。 |
| GetStartingAmountClientRequestHandler | POS で開始金額申告を行うとき (ビューに移動する前) に実行されます。 |

## <a name="tender-counting-request-handler"></a>支払/入金計算要求ハンドラー

| 要求名                                           | 説明                                               |
|--------------------------------------------------------|-----------------------------------------------------------|
| CreateSafeDropTransactionClientRequestHandler          | POS で金庫保管操作を行うときに実行されます。          |
| GetTenderDetailsClientRequestHandler                   | POS で支払/入金申告の詳細を取得するときに実行されます。  |
| CreateBankDropTransactionClientRequestHandler          | POS で銀行入金操作を行うときに実行されます。          |
| CreateTenderDeclarationTransactionClientRequestHandler | POS で支払/入金申告操作を行うときに実行されます。 |
| GetCountedTenderDetailAmountClientRequestHandler | POS で入札件数の詳細を行うときに実行されます。 |
| CreateBankDropTransactionClientRequestHandler | POS で銀行入金操作を行うときに実行されます。 |

## <a name="sales-orders-request-handlers"></a>販売注文の要求ハンドラー

| 要求名                                           | 説明                                               |
|--------------------------------------------------------|-----------------------------------------------------------|
| GetGiftReceiptsClientRequestHandler | POS でギフト レシートを印刷するときに実行されます。          |
| SelectCustomerOrderTypeClientRequestHandler | 顧客注文または見積のどちらかを選択するオプションがあるダイアログ ボックスを取得するときに実行されます。          |
| GetCancellationChargeClientRequestHandler | 顧客注文ワークフロー中にキャンセル出荷費用を入力するダイアログ ボックスが表示されたときに実行されます。          |

## <a name="how-to-override-a-handler-in-pos"></a>POS でハンドラーをオーバーライドする方法

上記の POS 要求ハンドラー ロジックのいずれかをオーバーライドすると、次の手順を使用する必要があります。

1. 新しいクラスを作成し、対応するハンドラー クラスから拡張します。 たとえば、GetSerialNumberClientRequestHandler をオーバーライドする場合、クラスを GetSerialNumberClientRequestHandler から拡張します。

2. executeAsync メソッドを実装します。

3. 既定のハンドラーを呼び出すか、executeAsync メソッド内でカスタム ロジックを実行して、応答を返します。

## <a name="step-by-step-instructions"></a>ステップ バイ ステップの手順

次の例では、GetSerialNumberClientRequestHandler をオーバーライドして POS でシリアル番号の入力を自動化する方法を示します。 既定では、POS には、シリアル番号を要求するよう品目がコンフィギュレーションされている場合は、シリアル番号を入力するダイアログ ボックスが表示されます。 このダイアログ ボックスが表示されないようにし、コードを使用してシリアル番号を入力します。

1. 管理者モードで Visual Studio 2015 を開きます。

2. ModernPOS ソリューションを …\\RetailSDK\\POS から開きます。

3. POS.Extensions プロジェクトで、POSRequestHandlerExtension という名前の新しいフォルダーを作成します。

4. POSRequestHandlerExtension フォルダーに、Handlers という名前の新しいフォルダーを作成します。

5. Handlers フォルダーに、新しい .ts (typescript) ファイルを追加し、GetSerialNumberClientRequestHandlerExt.ts と名前を付けます。

6. 次の import ステートメントを追加して、GetSerialNumberClientRequestHandlerExt.ts ファイルに関連するエンティティおよびコンテキストをインポートします。

    ```typescript
    import { GetSerialNumberClientRequestHandler } from "PosApi/Extend/RequestHandlers/ProductsRequestHandlers";
    import { GetSerialNumberClientRequest, GetSerialNumberClientResponse } from "PosApi/Consume/Products";
    import { ClientEntities } from "PosApi/Entities";
    ```

7. GetSerialNumberClientRequestHandlerExt.ts ファイルで、GetSerialNumberClientRequestHandlerExtend という新しいクラスを作成し、GetSerialNumberClientRequestHandler から拡張します。

    ```typescript
    export default class GetSerialNumberClientRequestHandlerExt extends GetSerialNumberClientRequestHandler { }
    ```

8. GetSerialNumberClientRequestHandlerExt クラス内に executeAsync メソッドを実装します。 executeAsync メソッドでは、カスタム ロジックを書き込んで、応答を返すか、既定のハンドラーを呼び出すことができます。 POS は、シリアル品目を販売するとき、シリアル番号のロジックを実行する executeAsync を探しますが、オーバーライドされるため、POS は標準メソッドの代わりにこのオーバーライドされた executeAsync メソッドを実行します。

    **executeAsync メソッドをオーバーライドする方法のサンプル実装**

    ```typescript
    public executeAsync(request: GetSerialNumberClientRequest<GetSerialNumberClientResponse>):
    Promise<ClientEntities.ICancelableDataResult<GetSerialNumberClientResponse>> {

    // User could implement new business logic here to process the serial number.
    // The following example sets serial number "112233" for product 82001.

    if (request.product.ItemId === "82001") {
    let response: GetSerialNumberClientResponse = new GetSerialNumberClientResponse("112233");
    return Promise.resolve(<ClientEntities.ICancelableDataResult<GetSerialNumberClientResponse>>{

    canceled: false,
    data: response

    });

    }

    // If you don’t want to execute custom logic on some conditions, and you just want to call the standard logic, you can call the default request, as shown below.

    return this.defaultExecuteAsync(request);

    }
    ```

    完全なサンプル コード:

    ```typescript
    import { GetSerialNumberClientRequestHandler } from "PosApi/Extend/RequestHandlers/ProductsRequestHandlers";
    import { GetSerialNumberClientRequest, GetSerialNumberClientResponse } from "PosApi/Consume/Products";
    import { ClientEntities } from "PosApi/Entities";

    /**
    * Override request handler class for getting serial number request.
    */

    export default class GetSerialNumberClientRequestHandlerExt extends GetSerialNumberClientRequestHandler {

    /**
    * Executes the request handler asynchronously.
    * @param {GetSerialNumberClientRequest<GetSerialNumberClientResponse>} request The request containing the response.
    * @return {Promise<ICancelableDataResult<GetSerialNumberClientResponse>>} The cancelable promise containing the response.
    */

    public executeAsync(request: GetSerialNumberClientRequest<GetSerialNumberClientResponse>):
        Promise<ClientEntities.ICancelableDataResult<GetSerialNumberClientResponse>> {

    // User could implement new business logic here to process the serial number.
    // The following example sets serial number "112233" for product 82001.

    if (request.product.ItemId === "82001") {
    let response: GetSerialNumberClientResponse = new GetSerialNumberClientResponse("112233");
    return Promise.resolve(<ClientEntities.ICancelableDataResult<GetSerialNumberClientResponse>>{
    canceled: false,
    data: response
    });

    }
    return this.defaultExecuteAsync(request);
    }
    }
    ```

9. POSRequestHandlerExtension フォルダーの下に新しい json ファイルを作成します。 manifest.json という名前を付けます。

10. manifest.json ファイルに、次のコードをコピーして貼り付けます。 このコードをコピーする前に、既定で生成されたコードを削除してください。

    ```json
    {
        "$schema": "../manifestSchema.json",
        "name": "Pos_Extensibility_Samples",
        "publisher": "Microsoft",
        "version": "7.3.5.0",
        "minimumPosVersion": "7.3.5.0",
        "components": {
            "extend": {
                "requestHandlers": [
                    {
                        "modulePath": "Handlers/GetSerialNumberClientRequestHandlerExt"
                    }
                ]
            }
        }
    }
    ```

11. POS.Extensions プロジェクトにある extensions.json ファイルを開きます。 実行時の POS にこの拡張が含まれるように、POSRequestHandlerExtension サンプルで更新します。

    ```json
    {
        "extensionPackages": [
            {
                "baseUrl": "SampleExtensions2"
            },
            {
                "baseUrl": " SampleExtensions"
            },
            {
                "baseUrl": "POSRequestHandlerExtension"
            }
        ]
    }
    ```

    > [!NOTE]
    > extension.json ファイルには、常に 2 つの拡張フォルダー名が含まれている必要があるため、必ず SampleExtensions フォルダー名またはカスタム拡張フォルダー名を保持してください。 生産には、サンプル拡張を使用しないでください。 独自の拡張フォルダーを追加し、すべてのサンプルを削除する必要があります。

12. tsconfig.json ファイルを開いて、拡張パッケージ フォルダーを除外リストからコメント アウトします。 POS では、このファイルを使用して、コンパイル用に拡張機能を追加または除外します。 既定では、リストに除外されたすべての拡張リストが含まれています。 POS の拡張部分をコンパイルする場合は、拡張フォルダー名を追加し、以下のように拡張リストから拡張をコメント アウトする必要があります。

    ```json
    "exclude": [
        // "SampleExtensions",
        //"SampleExtensions2",
        //"POSRequestHandlerExtension"
    ],
    ```

13. プロジェクトをコンパイル、およびリビルドします。

## <a name="how-to-test-your-extension"></a>拡張機能をテストする方法

1. F5 キーを押し、POS を展開してカスタマイズをテストします。

2. POS が開始されたら、POS にサインインし、トランザクションへシリアル品目を追加します。

3. 拡張コードにブレークポイントを配置します。 シリアル品目を追加するとき、拡張コードをデバッグできるはずです。

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
