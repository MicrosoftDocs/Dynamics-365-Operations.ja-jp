---
title: 支払コネクタの重複支払保護の有効化
description: このトピックでは、指定された支払コネクタで重複支払保護を有効にする方法について説明します。
author: Reza-Assadi
manager: AnnBe
ms.date: 12/28/2018
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
ms.openlocfilehash: f8fd423ae9609801c19ad0d14548a50652b44365
ms.sourcegitcommit: 299e20b59ebefa584ed46a13da3f1a7ff709e43c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/05/2019
ms.locfileid: "1863311"
---
#  <a name="enable-duplicate-payment-protection-for-payment-connector"></a>支払コネクタの重複支払保護の有効化

[!include [banner](../../includes/banner.md)]

このトピックでは、支払ターミナルとの統合を管理する支払コネクタの重複支払保護機能を有効にする方法について説明します。 *支払コネクタ*は支払ターミナルをPOSに統合するために書き込まれた拡張ライブラリです。

## <a name="overview"></a>概要

- [必読](#required-reading) - 支払コネクタに重複支払保護機能の実装を開始する前に必ず読むべきトピックの一覧。 
- [前提条件](#prerequisites) - 支払コネクタの実装に重複支払保護を有効にする前提条件の一覧。
- [重複支払保護フローを理解する](#understanding-duplicate-payment-protection-flows) - 重複支払保護が POS で呼び出される時のさまざまなフローについて説明します。
- [重複支払要求の実装](#implement-duplicate-payment-requests) - 重複支払保護機能をサポートするために実装する必要があるさまざまな支払に関連する要求について説明します。

## <a name="required-reading"></a>読む必要があります
指定された支払コネクタで重複支払保護を有効にする前に次のトピックを必ず読むようにしてください。

- [支払端末のエンド・ツー・エンド支払統合を作成する](end-to-end-payment-extension.md) - 重複支払保護機能は、このトピックで説明されている支払端末の支払統合に基づいています。
- [支払の保護の複製](duplicate-payment-protection.md) - このトピックでは重複支払保護機能の鍵となる機能要素について説明します。

## <a name="prerequisites"></a>必要条件
支払コネクタの実装で重複支払保護を有効にする前に、次の前提条件が満たされる必要があります。

### <a name="support-for-unique-transaction-scope-in-payment-terminal-or-payment-gatewayprocessor"></a>支払端末または支払ゲートウェイ/プロセッサに固有のトランザクション スコープのサポート
重複支払保護のサポートを有効にするために、対応する支払端末または支払ゲートウェイ/プロセッサは固有のトランザクション スコープのサポートを提供する必要があります。 通常、このサポートは支払端末で生成される固有の支払参照識別子を通して、または支払が処理される前に支払ゲートウェイ/プロセッサにより処理されています。 一意の識別子のサポートなしでは、コネクタは先に開始された取引を、正常に行われた支払の承認と一意に対応付けることができず、これが重複支払保護が失敗する元となります。

## <a name="understanding-duplicate-payment-protection-flows"></a>重複支払保護フローを理解します。
Dynamics 365 for RetailPOSが拡張され、支払コネクタに**承認**を出す直前など、POS 全体の様々なシナリオで新しい要求である `GetTransactionReferencePaymentTerminalDeviceRequest` および `GetTransactionByTransactionReferencePaymentTerminalDeviceRequest` を呼び出すようになりました。 これらの新しい要求の目的は、新しい支払要求を実行する前に、支払コネクタを通して正常に処理された支払を検出し、復元するものです。 次の図は、支払要求は支払コネクタを通して正常に処理されたものの、応答を受信する前にPOS がクラッシュしたというシンプルなシナリオを示しています。 その後、POS は重複支払保護機能により、前の処理済の支払を復元することができます。 

![重複支払保護フロー](media/PAYMENTS/DUPLICATE-PAYMENT-PROTECTION/DuplicatePaymentProtectionFlow.jpg)


### <a name="supported-pos-flows"></a>サポートされている POS フロー
次のリストは、`GetTransactionByTransactionReferencePaymentTerminalDeviceRequest` が既存の支払を回収するために呼び出される時のすべての POS フローを示しています。 これらは、支払取引の処理中にPOS がクラッシュ、または支払端末または支払ゲートウェイへの接続を喪失したときに最も一般的に実行されるフローです。

- レジ担当者がカード支払を使用して金額に対して支払を呼び出します。
- レジ担当者が現金支払を使用して金額に対して支払を呼び出します
- レジ担当者が、カートの明細行を無効化しようとしています。
- レジ担当者が取引を無効化しようとしています
- レジ担当者が取引を停止しようとしています

## <a name="implement-duplicate-payment-requests"></a>重複支払要求の実装
次のサンプルは、`INamedRequestHandler` での要求を例示します- これは、重複支払保護機能を確実に有効化するために必要な支払コネクタ実装です。

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
                    // New request types specific to the duplicate payment protection feature.
                    typeof(GetTransactionReferencePaymentTerminalDeviceRequest),
                    typeof(GetTransactionByTransactionReferencePaymentTerminalDeviceRequest),
                    
                    // Extended with new functionality.
                    typeof(AuthorizePaymentTerminalDeviceRequest)
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
            ThrowIf.Null(request, nameof(request));

            Type requestType = request.GetType();

            if (requestType == typeof(GetTransactionReferencePaymentTerminalDeviceRequest))
            {
                return this.GetTransactionReference((GetTransactionReferencePaymentTerminalDeviceRequest)request);
            }
            else if (requestType == typeof(GetTransactionByTransactionReferencePaymentTerminalDeviceRequest))
            {
                return this.GetTransactionByTransactionReference((GetTransactionByTransactionReferencePaymentTerminalDeviceRequest)request);
            }
            else if (requestType == typeof(AuthorizePaymentTerminalDeviceRequest))
            {
                return this.AuthorizePayment((AuthorizePaymentTerminalDeviceRequest)request);
            }
            ...

            return new NullResponse();
        }
    }
}
```

### <a name="gettransactionreferencepaymentterminaldevicerequest--gettransactionreferencepaymentterminaldeviceresponse"></a>GetTransactionReferencePaymentTerminalDeviceRequest / GetTransactionReferencePaymentTerminalDeviceResponse

#### <a name="description"></a>説明
`GetTransactionReferencePaymentTerminalDeviceRequest` は、支払取引の開始時に Dynamics 365 for Retail POS に呼び出され、支払のスコープを設定します。 この要求のスコープは、支払明細行が正常にカートに追加されるか、もしくはカードが使用できず、支払コネクタから戻らないことを表示するエラーが出ると終了します。 対応する `GetTransactionReferencePaymentTerminalDeviceResponse` 応答には、支払取引を検索するために支払コネクタによって生成される対応する一意の識別子が含まれます。 ID はアプリケーションの再起動後も維持される必要があり、通常、支払ゲートウェイによって ID が生成されるべきなので、支払コネクタの実装は生成された ID をキャッシュしてはいけないことに注意してください。

#### <a name="request-signature"></a>署名の要求
``` csharp
public GetTransactionReferencePaymentTerminalDeviceRequest(string lockToken, string posTerminalId, string eftTerminalId);
```

#### <a name="request-variables"></a>変数の要求
| 変数 | 説明 |
|---|---|
| lockToken | 支払端末が最初の取引のためにロックされたときに生成される一意のトークン値。 |
| posTerminalId | POS レジスターの固有の名前 |
| eftTerminalId | EFT POS 端末番号は、POS レジスターまたは共有ハードウェア ステーションを構成します。 |

#### <a name="response-signature"></a>署名への応答
``` csharp
public GetTransactionReferencePaymentTerminalDeviceResponse(string id);
```

#### <a name="response-variables"></a>変数への応答
| 変数 | 説明 |
|---|---|
| id | 支払取引のスコープに使用する一意の識別子。 |

### <a name="paymenttransactionreferencedata"></a>PaymentTransactionReferenceData 
`GetTransactionReferencePaymentTerminalDeviceRequest` が実行された後、Dynamics 365 for Retail POS は `PaymentTransactionReferenceData` クラスの新しいインスタンスを生成し、重複支払保護スコープを維持するために POS に必要なコンテキスト データを実行します。 この変数は POS で格納および管理され、キーの支払操作時に既存の取引を確認するために使用します。 

#### <a name="properties"></a>プロパティ
| 変数 | 説明 |
|---|---|
| コマンド | 支払には、呼び出されたコマンドが関連付けられます。 可能性がある値は、`Sale`、`Refund`、`Activate`、もしくは `Load` です。 |
| IdFromConnector | `GetTransactionReferencePaymentTerminalDeviceRequest` 要求を通して生成された一意の識別子。 |
| InitiatedDate | 元の支払に関連する取引が開始された日付と時刻。 |
| UniqueTransactionId | (支払そのものには特定されていない) カート取引の一意の識別子。 |
| 金額 | 処理されている支払取引の金額。 |

### <a name="authorizepaymentterminaldevicerequest"></a>AuthorizePaymentTerminalDeviceRequest

#### <a name="description"></a>説明
`AuthorizePaymentTerminalDeviceRequest` パラメーターは、新しい要求である `PaymentTransactionReferenceData` をサポートする新しいコンストラクターを提供するよう拡張されています。 このパラメーターの目的は、コンテキスト参照データを管理し、また支払コネクタによって生成され、重複支払を識別し、後でのクエリのために POS により使用される一意の識別子と支払端末または支払ゲートウェイ/プロセッサへの承認要求にスタンプすることです。 

### <a name="gettransactionbytransactionreferencepaymentterminaldevicerequest--gettransactionbytransactionreferencepaymentterminaldeviceresponse"></a>GetTransactionByTransactionReferencePaymentTerminalDeviceRequest / GetTransactionByTransactionReferencePaymentTerminalDeviceResponse
既存の支払取引が支払端末または支払ゲートウェイ/プロセッサですでに呼び出され、かつ処理されたかどうかをし区別するため、特定の支払いに関連した操作の直前に、Dynamics 365 for Retail POS は `GetTransactionByTransactionReferencePaymentTerminalDeviceRequest` を呼び出します。 既存のトランザクションが支払コネクタにより復旧すると、新しい取引をトリガーするためコネクタに返され、短い回路の続く呼び出しがあります。

#### <a name="request-signature"></a>署名の要求
``` csharp
public GetTransactionByTransactionReferencePaymentTerminalDeviceRequest(string lockToken, PaymentTransactionReferenceData transactionReferenceData);
```

#### <a name="request-variables"></a>変数の要求
| 変数 | 説明 |
|---|---|
| lockToken | 支払端末が最初の取引のためにロックされたときに生成される一意のトークン値。 |
| transactionReferenceData | プロパティ バッグは、支払取引を一意に識別するために使用されるさまざまなプロパティを含みます。 詳細については、このトピック [PaymentTransactionReferenceData](#paymenttransactionreferencedata) セクションを参照してください。 |

#### <a name="response-signature"></a>署名への応答
``` csharp
public GetTransactionByTransactionReferencePaymentTerminalDeviceResponse(PaymentInfo paymentInfo);
```

#### <a name="response-variables"></a>変数への応答
| 変数 | 説明 |
|---|---|
| paymentInfo | 復元された支払取引。 これは、**承認**または**返金**のような、ほかの支払要求などで返される支払応答と同じです。 |
