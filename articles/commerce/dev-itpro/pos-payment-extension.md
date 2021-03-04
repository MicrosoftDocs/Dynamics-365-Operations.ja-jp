---
title: 販売時点管理 (POS) 支払拡張機能
description: 支払いの拡張性をサポートするために POS で拡張点を使用すると、ハードウェア ステーション API を使用する支払デバイスまたは支払コネクタに主要な支払いロジックを実装することができます。
author: mugunthanm
manager: AnnBe
ms.date: 09/01/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: rhaertle
ms.custom: 24411
ms.search.region: Global
ms.author: mumani
ms.search.validFrom: 2017-09-01
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 8eabce858f50369c791dbcf41ea538826bbf8f82
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/05/2020
ms.locfileid: "4681510"
---
# <a name="point-of-sale-pos-payment-extension"></a>販売時点管理 (POS) 支払拡張機能

[!include [banner](../../includes/banner.md)]

支払いの拡張性をサポートするために販売時点管理 (POS) の拡張点を使用すると、ハードウェア ステーション API を使用する支払デバイスまたは支払コネクタに主要な支払いロジックを実装することができます。 これを行うことがあるいくつかのシナリオは次のとおりです。
- 拡張機能のプロパティなどの追加情報をコネクター/デバイスに渡す必要がある場合。
- 支払フロー間に、カスタム メッセージを表示する必要があります。
- フローを完了して支払デバイス/コネクタの中間的な応答を送信するレジ担当者からの入力が必要です。 たとえば、顧客 ID の検証状態または音声認証を必要とする場合があります。 
- 顧客 PIN 入力待ちなどの、処理ダイアログ メッセージを表示する必要があります。 POS 支払い要求をオーバーライドしてこれらのシナリオを実装することができます。

POS 側から以下の要求ハンドラーをオーバーライドして、支払いフローをカスタマイズすることができます。

- PaymentTerminalAuthorizePaymentRequestHandler
- PaymentTerminalCapturePaymentRequestHandler
- PaymentTerminalExecuteTaskRequestHandler
- PaymentTerminalRefundPaymentRequestHandler
- PaymentTerminalVoidPaymentRequestHandler

POS ランタイムは、これらの要求ハンドラーに拡張機能があるかどうかを確認するために拡張子マニフェストをチェックします。 拡張機能がある場合は、ランタイムは拡張要求をロードし、オーバーライドされた要求を実行します。 拡張プロジェクトでは、これらの要求をオーバーライドし、カスタム支払プロバイダーを呼び出す独自の実装を追加して、プロバイダーによって返されるステータスに基づいて応答を更新します。 要求を上書きするときは、コア ロジックのみを上書きします。 すべてのカスタム ロジックの実行後、ハードウェア ステーション (支払デバイス/コネクタ) から受信した更新済の応答を POS に送信します。 すべての標準ワークフローは POS によって処理されるため、支払ラインの追加、無効、拒否、および応答に基づいたトランザクションの完結の方法を心配する必要はありません。

## <a name="paymentterminalauthorizepaymentrequesthandler"></a>PaymentTerminalAuthorizePaymentRequestHandler

**PaymentTerminalAuthorizePaymentRequestHandler**、承認要求は、カード支払要求を開始し許可する POS からのコア支払要求です。 承認ワークフローを変更する場合は、この要求をオーバーライドすることができます。 リクエストをオーバーライドにするには、POS の **PaymentTerminalAuthorizePaymentRequestHandler** を拡張する必要があります。

```typescript

import { PaymentTerminalAuthorizePaymentRequestHandler } from "PosApi/Extend/RequestHandlers/PeripheralsRequestHandlers";
import { PaymentTerminalAuthorizePaymentRequest, PaymentTerminalAuthorizePaymentResponse } from "PosApi/Consume/Peripherals";
import { ClientEntities, ProxyEntities } from "PosApi/Entities";
import { GetCurrentCartClientRequest, GetCurrentCartClientResponse } from "PosApi/Consume/Cart";
import { PaymentHandlerHelper } from "./PaymentHandlerHelper";
import { ObjectExtensions } from "PosApi/TypeExtensions";

/**
* Override request handler class for the payment terminal authorize payment request.
*/
export default class PaymentTerminalAuthorizePaymentRequestHandlerExt extends PaymentTerminalAuthorizePaymentRequestHandler {

    /**
    * Executes the request handler asynchronously.
    * @param {PaymentTerminalAuthorizePaymentRequest<PaymentTerminalAuthorizePaymentResponse>} request The request.
    * @return {Promise<ICancelableDataResult<PaymentTerminalAuthorizePaymentResponse>>} The cancelable promise containing
    * the response.
    */
    public executeAsync(request: PaymentTerminalAuthorizePaymentRequest<PaymentTerminalAuthorizePaymentResponse>):
        Promise<ClientEntities.ICancelableDataResult<PaymentTerminalAuthorizePaymentResponse>> {
        let cart: ProxyEntities.Cart = null;
        let cartRequest: GetCurrentCartClientRequest<GetCurrentCartClientResponse> = new GetCurrentCartClientRequest();

        // Get cart first and then build extension properties based on cart info.
        return this.context.runtime.executeAsync(cartRequest)
            .then((result: ClientEntities.ICancelableDataResult<GetCurrentCartClientResponse>): void => {
                if (!(result.canceled || ObjectExtensions.isNullOrUndefined(result.data))) {
                    cart = result.data.result;
                }
            }).then((): Promise<ClientEntities.ICancelableDataResult<PaymentTerminalAuthorizePaymentResponse>> => {
                let newRequest: PaymentTerminalAuthorizePaymentRequest<PaymentTerminalAuthorizePaymentResponse> =
                    new PaymentTerminalAuthorizePaymentRequest<PaymentTerminalAuthorizePaymentResponse>(
                        request.paymentConnectorId,
                        request.amount,
                        request.tenderInfo,
                        request.voiceAuthorization,
                        request.isManualEntry,
                        PaymentHandlerHelper.FillExtensionProperties(cart, request.extensionTransactionProperties));

                return this.defaultExecuteAsync(newRequest);
            });
    }
}
```

PaymentHandlerHelper.ts にこれらの変更を加える必要があります。

```typescript

import { ClientEntities, ProxyEntities } from "PosApi/Entities";
import { ObjectExtensions, StringExtensions } from "PosApi/TypeExtensions";

/**
 * Override request handler class for the payment terminal authorize payment request.
 */
export class PaymentHandlerHelper {
    // Get extra properties for payment terminal
    public static FillExtensionProperties(
        cart: ProxyEntities.Cart,
        extensionProperties: ClientEntities.IExtensionTransaction): ClientEntities.IExtensionTransaction {

        let extraProperties: ClientEntities.IExtensionTransaction = null;
        // Build extra extension properties.
        if (!ObjectExtensions.isNullOrUndefined(cart)) {
            extraProperties = {
                ExtensionProperties: [
                    <ProxyEntities.CommerceProperty>{
                        Key: "CartId",
                        Value: <ProxyEntities.CommercePropertyValue>{
                            StringValue: !ObjectExtensions.isNullOrUndefined(cart) ? cart.Id : ""
                        }
                    }, {
                        Key: "ChannelId",
                        Value: <ProxyEntities.CommercePropertyValue>{
                            StringValue: (ObjectExtensions.isNullOrUndefined(cart.ChannelId)) ? ""
                                : cart.ChannelId.toString()
                        }
                    }, {
                        Key: "TerminalId",
                        Value: <ProxyEntities.CommercePropertyValue>{
                            StringValue: cart.TerminalId
                        }
                    }, {
                        Key: "StaffId",
                        Value: <ProxyEntities.CommercePropertyValue>{ StringValue: cart.StaffId }
                    }, {
                        Key: "CustomerId",
                        Value: <ProxyEntities.CommercePropertyValue>{
                            StringValue: (StringExtensions.isNullOrWhitespace(cart.CustomerId)) ? ""
                                : cart.CustomerId
                        }
                    }, {
                        Key: "ShippingZipCode",
                        Value: <ProxyEntities.CommercePropertyValue>{
                            StringValue: !ObjectExtensions.isNullOrUndefined(cart.ShippingAddress) ?
                                (StringExtensions.isNullOrWhitespace(cart.ShippingAddress.ZipCode) ? "" :
                                    cart.ShippingAddress.ZipCode) : ""
                        }
                    }
                ]
            };
        };

        if (ObjectExtensions.isNullOrUndefined(extensionProperties)) {
            extensionProperties = extraProperties;
        } else {
            for (let i: number = 0; i < extraProperties.ExtensionProperties.length; i++) {
                extensionProperties.ExtensionProperties.push(extraProperties.ExtensionProperties[i]);
            }
        }

        return extensionProperties;
    }
}
```

要求ロジックを実装した後、POS が拡張を読み込むように、拡張情報で manifest.json を更新する必要があります。

```typescript
{
    "$schema": "../manifestSchema.json",
        "name": "Pos_Payment_Samples",
            "publisher": "Microsoft",
                "version": "7.2.0",
                    "minimumPosVersion": "7.2.0.0",
                        "components": {
        "extend": {
            "requestHandlers": [
                {
                    "modulePath": "Peripherals/Handlers/PaymentTerminalAuthorizePaymentRequestHandlerExt"
                }
            ]
        }
    }
}
```

拡張プロパティを渡す方法を含む、完全なコード サンプルは、RetailSDK\Code\POS\Extensions\PaymentSample フォルダーの Retail SDK アプリケーション更新プログラム 3 で利用できます。 上記のコード サンプルをチェックインした場合、支払いの完了や支払明細行の追加方法における主要なロジックではなく、呼び出し部分のみがオーバーライドされます。 POS ワークフローがこれを管理しきます。

## <a name="paymentterminalcapturepaymentrequesthandler"></a>PaymentTerminalCapturePaymentRequestHandler

**PaymentTerminalCapturePaymentRequestHandler**、支払要求は、カード支払要求を開始し取得する POS からの支払要求です。 キャプチャ ワークフローを変更する場合は、この要求をオーバーライドします。 リクエストをオーバーライドにするには、POS の **PaymentTerminalCapturePaymentRequestHandler** を拡張する必要があります。

```typescript
import { PaymentTerminalCapturePaymentRequestHandler } from "PosApi/Extend/RequestHandlers/PeripheralsRequestHandlers";
import { PaymentTerminalCapturePaymentRequest, PaymentTerminalCapturePaymentResponse } from "PosApi/Consume/Peripherals";
import { ClientEntities, ProxyEntities } from "PosApi/Entities";
import { GetCurrentCartClientRequest, GetCurrentCartClientResponse } from "PosApi/Consume/Cart";
import { PaymentHandlerHelper } from "./PaymentHandlerHelper";
import { ObjectExtensions } from "PosApi/TypeExtensions";

/**
 * Override request handler class for the payment terminal Capture payment request.
 */
export default class PaymentTerminalCapturePaymentRequestHandlerExt extends PaymentTerminalCapturePaymentRequestHandler {
    /**
     * Executes the request handler asynchronously.
     * @param {PaymentTerminalCapturePaymentRequest<PaymentTerminalCapturePaymentResponse>} request The request.
     * @return {Promise<ICancelableDataResult<PaymentTerminalCapturePaymentResponse>>} 
     * The cancelable promise containing the response.
     */
    public executeAsync(request: PaymentTerminalCapturePaymentRequest<PaymentTerminalCapturePaymentResponse>):
        Promise<ClientEntities.ICancelableDataResult<PaymentTerminalCapturePaymentResponse>> {
        let cart: ProxyEntities.Cart = null;
        let cartRequest: GetCurrentCartClientRequest<GetCurrentCartClientResponse> = new GetCurrentCartClientRequest();

        // Get cart first and then build extension properties based on cart info.
        return this.context.runtime.executeAsync(cartRequest)
            .then((result: ClientEntities.ICancelableDataResult<GetCurrentCartClientResponse>): void => {
                if (!(result.canceled || ObjectExtensions.isNullOrUndefined(result.data))) {
                    cart = result.data.result;
                }
            }).then((): Promise<ClientEntities.ICancelableDataResult<PaymentTerminalCapturePaymentResponse>> => {
                let newRequest: PaymentTerminalCapturePaymentRequest<PaymentTerminalCapturePaymentResponse> =
                    new PaymentTerminalCapturePaymentRequest<PaymentTerminalCapturePaymentResponse>(
                        request.amount,
                        request.paymentProperties,
                        PaymentHandlerHelper.FillExtensionProperties(cart, request.extensionTransactionProperties));

                return this.defaultExecuteAsync(newRequest);
            });
    }
}
```

要求ロジックを実装した後、POS が拡張を読み込むように、拡張情報で manifest.json を更新する必要があります。 上書きする要求はすべてマニフェストで指定されます。 標準要求のいずれかを上書きしなかった場合は、マニフェストに何も指定する必要はありません。 マニフェストの例では、2 つの上書きされた要求が示されています。

```typescript
{
    "$schema": "../manifestSchema.json",
        "name": "Pos_Payment_Samples",
            "publisher": "Microsoft",
                "version": "7.2.0",
                    "minimumPosVersion": "7.2.0.0",
                        "components": {
        "extend": {
            "requestHandlers": [
                {
                    "modulePath": "Peripherals/Handlers/PaymentTerminalAuthorizePaymentRequestHandlerExt"
                },
                {
                    "modulePath": "Peripherals/Handlers/PaymentTerminalCapturePaymentRequestHandlerExt"
                }
            ]
        }
    }
}
```

拡張プロパティを渡す方法に関する完全なコード サンプルは、RetailSDK\Code\POS\Extensions\PaymentSample フォルダーの Retail SDK アプリケーション更新プログラムで利用できます。

## <a name="paymentterminalexecutetaskrequesthandler"></a>PaymentTerminalExecuteTaskRequestHandler

**PaymentTerminalExecuteTaskRequestHandler**、POS からの任意のカスタム支払デバイス/コネクタ操作を開始するために POS から使用される実行要求です。 POS から支払デバイスの正常性チェックを行うため、バッチ処理を行うため、または支払デバイスへ営業終了要求のためには、これを使用する場合があります。 標準の承認、キャプチャ、無効化、および払戻以外のカスタム オプションを実行する場合、この要求をオーバーライドすることができます。 リクエストをオーバーライドにするには、POS の **PaymentTerminalExecuteTaskRequestHandler** を拡張する必要があります。

```typescript
import { PaymentTerminalExecuteTaskRequestHandler } from "PosApi/Extend/RequestHandlers/PeripheralsRequestHandlers";
import { PaymentTerminalExecuteTaskRequest, PaymentTerminalExecuteTaskResponse } from "PosApi/Consume/Peripherals";
import { ClientEntities, ProxyEntities } from "PosApi/Entities";
import { GetCurrentCartClientRequest, GetCurrentCartClientResponse } from "PosApi/Consume/Cart";
import { PaymentHandlerHelper } from "./PaymentHandlerHelper";
import { ObjectExtensions } from "PosApi/TypeExtensions";

/**
 * Override request handler class for the payment terminal ExecuteTask request.
 */
export default class PaymentTerminalExecuteTaskRequestHandlerExt extends PaymentTerminalExecuteTaskRequestHandler {
    /**
     * Executes the request handler asynchronously.
     * @param {PaymentTerminaExecuteTaskRequest<PaymentTerminalExecuteTaskResponse>} request The request.
     * @return {Promise<ICancelableDataResult<PaymentTerminalExecuteTaskResponse>>} 
     * The cancelable promise containing the response.
     */
    public executeAsync(request: PaymentTerminalExecuteTaskRequest<PaymentTerminalExecuteTaskResponse>):
        Promise<ClientEntities.ICancelableDataResult<PaymentTerminalExecuteTaskResponse>> {
        let cart: ProxyEntities.Cart = null;
        let cartRequest: GetCurrentCartClientRequest<GetCurrentCartClientResponse> = new GetCurrentCartClientRequest();

        // Get cart first and then build extension properties based on cart info.
        return this.context.runtime.executeAsync(cartRequest)
            .then((result: ClientEntities.ICancelableDataResult<GetCurrentCartClientResponse>): void => {
                if (!(result.canceled || ObjectExtensions.isNullOrUndefined(result.data))) {
                    cart = result.data.result;
                }
            }).then((): Promise<ClientEntities.ICancelableDataResult<PaymentTerminalExecuteTaskResponse>> => {
                let newRequest: PaymentTerminalExecuteTaskRequest<PaymentTerminalExecuteTaskResponse> =
                    new PaymentTerminalExecuteTaskRequest<PaymentTerminalExecuteTaskResponse>(
                        request.task,
                        PaymentHandlerHelper.FillExtensionProperties(cart, request.extensionTransactionProperties));

                return this.defaultExecuteAsync(newRequest);
            });
    }
}
```

要求ロジックを実装した後、POS が拡張を読み込むように、拡張情報で manifest.json を更新する必要があります。 

```typescript
{
    "$schema": "../manifestSchema.json",
        "name": "Pos_Payment_Samples",
            "publisher": "Microsoft",
                "version": "7.2.0",
                    "minimumPosVersion": "7.2.0.0",
                        "components": {
        "extend": {
            "requestHandlers": [
                {
                    "modulePath": "Peripherals/Handlers/PaymentTerminalAuthorizePaymentRequestHandlerExt"
                },
                {
                    "modulePath": "Peripherals/Handlers/PaymentTerminalCapturePaymentRequestHandlerExt"
                },
                {
                    "modulePath": "Peripherals/Handlers/PaymentTerminalExecuteTaskRequestHandlerExt"
                }
            ]
        }
    }
}
```

拡張プロパティを渡す方法に関する完全なコード サンプルは、RetailSDK\Code\POS\Extensions\PaymentSample フォルダーの Retail SDK アプリケーション更新プログラム 3 で利用できます。


## <a name="paymentterminalrefundpaymentrequesthandler"></a>PaymentTerminalRefundPaymentRequestHandler

**PaymentTerminalRefundPaymentRequestHandler**、カード要求の払戻または返金を開始する POS からの払戻要求です。 払戻ワークフローを変更する場合は、この要求をオーバーライドします。 リクエストをオーバーライドにするには、POS の **PaymentTerminalRefundPaymentRequestHandler** を拡張する必要があります。

## <a name="paymentterminalvoidpaymentrequesthandler"></a>PaymentTerminalVoidPaymentRequestHandler

**PaymentTerminalVoidPaymentRequestHandler**、無効化要求、無効化カード支払要求を開始する POS からの支払要求です。 無効なワークフローを変更する場合は、この要求をオーバーライドします。 リクエストをオーバーライドにするには、POS の **PaymentTerminalVoidPaymentRequestHandler** を拡張する必要があります。

無効および払い戻し要求コード パターンを拡張することは、承認および取得要求と同じです。 拡張プロパティを渡す方法とともに、無効および払い戻し支払要求の完全なコードサンプルは、RetailSDK\Code\POS\Extensions\PaymentSample フォルダーの Retail SDK アプリケーション 3 で利用できます。


[!INCLUDE[footer-include](../../includes/footer-banner.md)]