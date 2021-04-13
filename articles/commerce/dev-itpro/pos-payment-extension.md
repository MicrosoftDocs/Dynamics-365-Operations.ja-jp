---
title: 販売時点管理 (POS) 支払拡張機能
description: このトピックでは、ハードウェア ステーション API を使用して、支払デバイスまたは支払コネクタに主要な支払いロジックを実装する方法について説明します。
author: mugunthanm
ms.date: 09/01/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: rhaertle
ms.custom: 24411
ms.search.region: Global
ms.author: mumani
ms.search.validFrom: 2017-09-01
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: b4322cdff4b5a416e76a11e88c89b8e65dc74184
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5792987"
---
# <a name="point-of-sale-pos-payment-extension"></a><span data-ttu-id="bdbaf-103">販売時点管理 (POS) 支払拡張機能</span><span class="sxs-lookup"><span data-stu-id="bdbaf-103">Point of sale (POS) payment extension</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="bdbaf-104">支払いの拡張性をサポートするために販売時点管理 (POS) の拡張点を使用すると、ハードウェア ステーション API を使用する支払デバイスまたは支払コネクタに主要な支払いロジックを実装することができます。</span><span class="sxs-lookup"><span data-stu-id="bdbaf-104">With the extension points in point of sale (POS) to support payment extensibility, you can implement the core payment logic in the payment device or payment connector using the Hardware station APIs.</span></span> <span data-ttu-id="bdbaf-105">これを行うことがあるいくつかのシナリオは次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="bdbaf-105">Some scenarios where you might want to do this are:</span></span>
- <span data-ttu-id="bdbaf-106">拡張機能のプロパティなどの追加情報をコネクター/デバイスに渡す必要がある場合。</span><span class="sxs-lookup"><span data-stu-id="bdbaf-106">You need to pass additional information such as extension properties to your connector/device.</span></span>
- <span data-ttu-id="bdbaf-107">支払フロー間に、カスタム メッセージを表示する必要があります。</span><span class="sxs-lookup"><span data-stu-id="bdbaf-107">You want to show custom messages in between the payment flow.</span></span>
- <span data-ttu-id="bdbaf-108">フローを完了して支払デバイス/コネクタの中間的な応答を送信するレジ担当者からの入力が必要です。</span><span class="sxs-lookup"><span data-stu-id="bdbaf-108">You need input from the cashier to complete the flow and send an intermediate response back to the payment device/connector.</span></span> <span data-ttu-id="bdbaf-109">たとえば、顧客 ID の検証状態または音声認証を必要とする場合があります。</span><span class="sxs-lookup"><span data-stu-id="bdbaf-109">For example, you might need the customer ID validation status or voice authorization.</span></span> 
- <span data-ttu-id="bdbaf-110">顧客 PIN 入力待ちなどの、処理ダイアログ メッセージを表示する必要があります。</span><span class="sxs-lookup"><span data-stu-id="bdbaf-110">You want to show processing dialog messages, such as waiting for the customer pin input.</span></span> <span data-ttu-id="bdbaf-111">POS 支払い要求をオーバーライドしてこれらのシナリオを実装することができます。</span><span class="sxs-lookup"><span data-stu-id="bdbaf-111">You can override POS payment requests to implement these scenarios.</span></span>

<span data-ttu-id="bdbaf-112">POS 側から以下の要求ハンドラーをオーバーライドして、支払いフローをカスタマイズすることができます。</span><span class="sxs-lookup"><span data-stu-id="bdbaf-112">You can override the following request handlers from the POS side to customize the payment flow:</span></span>

- <span data-ttu-id="bdbaf-113">PaymentTerminalAuthorizePaymentRequestHandler</span><span class="sxs-lookup"><span data-stu-id="bdbaf-113">PaymentTerminalAuthorizePaymentRequestHandler</span></span>
- <span data-ttu-id="bdbaf-114">PaymentTerminalCapturePaymentRequestHandler</span><span class="sxs-lookup"><span data-stu-id="bdbaf-114">PaymentTerminalCapturePaymentRequestHandler</span></span>
- <span data-ttu-id="bdbaf-115">PaymentTerminalExecuteTaskRequestHandler</span><span class="sxs-lookup"><span data-stu-id="bdbaf-115">PaymentTerminalExecuteTaskRequestHandler</span></span>
- <span data-ttu-id="bdbaf-116">PaymentTerminalRefundPaymentRequestHandler</span><span class="sxs-lookup"><span data-stu-id="bdbaf-116">PaymentTerminalRefundPaymentRequestHandler</span></span>
- <span data-ttu-id="bdbaf-117">PaymentTerminalVoidPaymentRequestHandler</span><span class="sxs-lookup"><span data-stu-id="bdbaf-117">PaymentTerminalVoidPaymentRequestHandler</span></span>

<span data-ttu-id="bdbaf-118">POS ランタイムは、これらの要求ハンドラーに拡張機能があるかどうかを確認するために拡張子マニフェストをチェックします。</span><span class="sxs-lookup"><span data-stu-id="bdbaf-118">The POS runtime checks the extension manifest to see if there are any extensions for these request handlers.</span></span> <span data-ttu-id="bdbaf-119">拡張機能がある場合は、ランタイムは拡張要求をロードし、オーバーライドされた要求を実行します。</span><span class="sxs-lookup"><span data-stu-id="bdbaf-119">If there are extensions, then the runtime loads the extended requests and executes the overridden requests.</span></span> <span data-ttu-id="bdbaf-120">拡張プロジェクトでは、これらの要求をオーバーライドし、カスタム支払プロバイダーを呼び出す独自の実装を追加して、プロバイダーによって返されるステータスに基づいて応答を更新します。</span><span class="sxs-lookup"><span data-stu-id="bdbaf-120">In the extension project, you can override these requests, add your own implementation to call the custom payment providers, and then update the response based on the status that is returned by your providers.</span></span> <span data-ttu-id="bdbaf-121">要求を上書きするときは、コア ロジックのみを上書きします。</span><span class="sxs-lookup"><span data-stu-id="bdbaf-121">When you override a request, you are overriding only the core logic.</span></span> <span data-ttu-id="bdbaf-122">すべてのカスタム ロジックの実行後、ハードウェア ステーション (支払デバイス/コネクタ) から受信した更新済の応答を POS に送信します。</span><span class="sxs-lookup"><span data-stu-id="bdbaf-122">After all your custom logic has run, you send the updated response that you received from Hardware station (payment device/connector) to POS.</span></span> <span data-ttu-id="bdbaf-123">すべての標準ワークフローは POS によって処理されるため、支払ラインの追加、無効、拒否、および応答に基づいたトランザクションの完結の方法を心配する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="bdbaf-123">All the standard workflow is handled by the POS, so that you do not need to worry about how to add, void, or decline the payment line and conclude the transaction based on the response.</span></span>

## <a name="paymentterminalauthorizepaymentrequesthandler"></a><span data-ttu-id="bdbaf-124">PaymentTerminalAuthorizePaymentRequestHandler</span><span class="sxs-lookup"><span data-stu-id="bdbaf-124">PaymentTerminalAuthorizePaymentRequestHandler</span></span>

<span data-ttu-id="bdbaf-125">**PaymentTerminalAuthorizePaymentRequestHandler**、承認要求は、カード支払要求を開始し許可する POS からのコア支払要求です。</span><span class="sxs-lookup"><span data-stu-id="bdbaf-125">**PaymentTerminalAuthorizePaymentRequestHandler**, the authorization request, is the core payment request from POS that initiates and authorizes a card payment request.</span></span> <span data-ttu-id="bdbaf-126">承認ワークフローを変更する場合は、この要求をオーバーライドすることができます。</span><span class="sxs-lookup"><span data-stu-id="bdbaf-126">You can override this request if you want to change the authorize workflow.</span></span> <span data-ttu-id="bdbaf-127">リクエストをオーバーライドにするには、POS の **PaymentTerminalAuthorizePaymentRequestHandler** を拡張する必要があります。</span><span class="sxs-lookup"><span data-stu-id="bdbaf-127">To override the request, you need to extend the **PaymentTerminalAuthorizePaymentRequestHandler** in POS.</span></span>

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

<span data-ttu-id="bdbaf-128">PaymentHandlerHelper.ts にこれらの変更を加える必要があります。</span><span class="sxs-lookup"><span data-stu-id="bdbaf-128">You need to make these changes in PaymentHandlerHelper.ts.</span></span>

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

<span data-ttu-id="bdbaf-129">要求ロジックを実装した後、POS が拡張を読み込むように、拡張情報で manifest.json を更新する必要があります。</span><span class="sxs-lookup"><span data-stu-id="bdbaf-129">After implementing the request logic, you need to update manifest.json with the extension information so that POS loads the extension.</span></span>

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

<span data-ttu-id="bdbaf-130">拡張プロパティを渡す方法を含む、完全なコード サンプルは、RetailSDK\Code\POS\Extensions\PaymentSample フォルダーの Retail SDK アプリケーション更新プログラム 3 で利用できます。</span><span class="sxs-lookup"><span data-stu-id="bdbaf-130">The full code sample, including how to pass extension properties, is available in Retail SDK app update 3 in the RetailSDK\Code\POS\Extensions\PaymentSample folder.</span></span> <span data-ttu-id="bdbaf-131">上記のコード サンプルをチェックインした場合、支払いの完了や支払明細行の追加方法における主要なロジックではなく、呼び出し部分のみがオーバーライドされます。</span><span class="sxs-lookup"><span data-stu-id="bdbaf-131">If you check in the above code sample, only the calling portion has been overridden, and not the core logic on how to complete the payment or add payment line.</span></span> <span data-ttu-id="bdbaf-132">POS ワークフローがこれを管理しきます。</span><span class="sxs-lookup"><span data-stu-id="bdbaf-132">The POS workflow manages that.</span></span>

## <a name="paymentterminalcapturepaymentrequesthandler"></a><span data-ttu-id="bdbaf-133">PaymentTerminalCapturePaymentRequestHandler</span><span class="sxs-lookup"><span data-stu-id="bdbaf-133">PaymentTerminalCapturePaymentRequestHandler</span></span>

<span data-ttu-id="bdbaf-134">**PaymentTerminalCapturePaymentRequestHandler**、支払要求は、カード支払要求を開始し取得する POS からの支払要求です。</span><span class="sxs-lookup"><span data-stu-id="bdbaf-134">**PaymentTerminalCapturePaymentRequestHandler**, the payment request, is a payment request from POS that initiates and captures the card payment request.</span></span> <span data-ttu-id="bdbaf-135">キャプチャ ワークフローを変更する場合は、この要求をオーバーライドします。</span><span class="sxs-lookup"><span data-stu-id="bdbaf-135">Override this request if you want to change the capture workflow.</span></span> <span data-ttu-id="bdbaf-136">リクエストをオーバーライドにするには、POS の **PaymentTerminalCapturePaymentRequestHandler** を拡張する必要があります。</span><span class="sxs-lookup"><span data-stu-id="bdbaf-136">To override the request, you need to extend the **PaymentTerminalCapturePaymentRequestHandler** in POS.</span></span>

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

<span data-ttu-id="bdbaf-137">要求ロジックを実装した後、POS が拡張を読み込むように、拡張情報で manifest.json を更新する必要があります。</span><span class="sxs-lookup"><span data-stu-id="bdbaf-137">After implementing the request logic, you need to update the manifest.json with the extension information so that POS loads the extension.</span></span> <span data-ttu-id="bdbaf-138">上書きする要求はすべてマニフェストで指定されます。</span><span class="sxs-lookup"><span data-stu-id="bdbaf-138">Any requests that you override are specified in the manifest.</span></span> <span data-ttu-id="bdbaf-139">標準要求のいずれかを上書きしなかった場合は、マニフェストに何も指定する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="bdbaf-139">If you didn’t override any of the standard requests, then you do not need to specify anything in the manifest.</span></span> <span data-ttu-id="bdbaf-140">マニフェストの例では、2 つの上書きされた要求が示されています。</span><span class="sxs-lookup"><span data-stu-id="bdbaf-140">The example of the manifest shows two overriden requests.</span></span>

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

<span data-ttu-id="bdbaf-141">拡張プロパティを渡す方法に関する完全なコード サンプルは、RetailSDK\Code\POS\Extensions\PaymentSample フォルダーの Retail SDK アプリケーション更新プログラムで利用できます。</span><span class="sxs-lookup"><span data-stu-id="bdbaf-141">The full code sample, with how to pass extension properties, is available in Retail SDK app update in the RetailSDK\Code\POS\Extensions\PaymentSample folder.</span></span>

## <a name="paymentterminalexecutetaskrequesthandler"></a><span data-ttu-id="bdbaf-142">PaymentTerminalExecuteTaskRequestHandler</span><span class="sxs-lookup"><span data-stu-id="bdbaf-142">PaymentTerminalExecuteTaskRequestHandler</span></span>

<span data-ttu-id="bdbaf-143">**PaymentTerminalExecuteTaskRequestHandler**、POS からの任意のカスタム支払デバイス/コネクタ操作を開始するために POS から使用される実行要求です。</span><span class="sxs-lookup"><span data-stu-id="bdbaf-143">**PaymentTerminalExecuteTaskRequestHandler**, the execution request, is used from POS to initiate any custom payment device/connector operation from POS.</span></span> <span data-ttu-id="bdbaf-144">POS から支払デバイスの正常性チェックを行うため、バッチ処理を行うため、または支払デバイスへ営業終了要求のためには、これを使用する場合があります。</span><span class="sxs-lookup"><span data-stu-id="bdbaf-144">You might use this to do a health check of the payment device from POS, to do batch processing, or for an end-of-day request to the payment device.</span></span> <span data-ttu-id="bdbaf-145">標準の承認、キャプチャ、無効化、および払戻以外のカスタム オプションを実行する場合、この要求をオーバーライドすることができます。</span><span class="sxs-lookup"><span data-stu-id="bdbaf-145">You can override this request if you want to do a custom operation other than the standard authorize, capture, void, and refund.</span></span> <span data-ttu-id="bdbaf-146">リクエストをオーバーライドにするには、POS の **PaymentTerminalExecuteTaskRequestHandler** を拡張する必要があります。</span><span class="sxs-lookup"><span data-stu-id="bdbaf-146">To override the request, you need to extend the **PaymentTerminalExecuteTaskRequestHandler** in POS.</span></span>

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

<span data-ttu-id="bdbaf-147">要求ロジックを実装した後、POS が拡張を読み込むように、拡張情報で manifest.json を更新する必要があります。</span><span class="sxs-lookup"><span data-stu-id="bdbaf-147">After implementing the request logic, you need to update the manifest.json with the extension information so that POS loads the extension.</span></span> 

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

<span data-ttu-id="bdbaf-148">拡張プロパティを渡す方法に関する完全なコード サンプルは、RetailSDK\Code\POS\Extensions\PaymentSample フォルダーの Retail SDK アプリケーション更新プログラム 3 で利用できます。</span><span class="sxs-lookup"><span data-stu-id="bdbaf-148">The full code sample, with how to pass extension properties, is available in Retail SDK app update 3 in the RetailSDK\Code\POS\Extensions\PaymentSample folder</span></span>


## <a name="paymentterminalrefundpaymentrequesthandler"></a><span data-ttu-id="bdbaf-149">PaymentTerminalRefundPaymentRequestHandler</span><span class="sxs-lookup"><span data-stu-id="bdbaf-149">PaymentTerminalRefundPaymentRequestHandler</span></span>

<span data-ttu-id="bdbaf-150">**PaymentTerminalRefundPaymentRequestHandler**、カード要求の払戻または返金を開始する POS からの払戻要求です。</span><span class="sxs-lookup"><span data-stu-id="bdbaf-150">**PaymentTerminalRefundPaymentRequestHandler**, the refund request, is a payment request from POS that initiates a refund or return of the card payment.</span></span> <span data-ttu-id="bdbaf-151">払戻ワークフローを変更する場合は、この要求をオーバーライドします。</span><span class="sxs-lookup"><span data-stu-id="bdbaf-151">You override this request if you want to change the refund workflow.</span></span> <span data-ttu-id="bdbaf-152">リクエストをオーバーライドにするには、POS の **PaymentTerminalRefundPaymentRequestHandler** を拡張する必要があります。</span><span class="sxs-lookup"><span data-stu-id="bdbaf-152">To override the request, you need to extend the **PaymentTerminalRefundPaymentRequestHandler** in POS.</span></span>

## <a name="paymentterminalvoidpaymentrequesthandler"></a><span data-ttu-id="bdbaf-153">PaymentTerminalVoidPaymentRequestHandler</span><span class="sxs-lookup"><span data-stu-id="bdbaf-153">PaymentTerminalVoidPaymentRequestHandler</span></span>

<span data-ttu-id="bdbaf-154">**PaymentTerminalVoidPaymentRequestHandler**、無効化要求、無効化カード支払要求を開始する POS からの支払要求です。</span><span class="sxs-lookup"><span data-stu-id="bdbaf-154">**PaymentTerminalVoidPaymentRequestHandler**, the void request, is a payment request from POS that initiates the void card payment request.</span></span> <span data-ttu-id="bdbaf-155">無効なワークフローを変更する場合は、この要求をオーバーライドします。</span><span class="sxs-lookup"><span data-stu-id="bdbaf-155">You override this request if you want to change the void workflow.</span></span> <span data-ttu-id="bdbaf-156">リクエストをオーバーライドにするには、POS の **PaymentTerminalVoidPaymentRequestHandler** を拡張する必要があります。</span><span class="sxs-lookup"><span data-stu-id="bdbaf-156">To override the request, you need to extend the **PaymentTerminalVoidPaymentRequestHandler** in POS.</span></span>

<span data-ttu-id="bdbaf-157">無効および払い戻し要求コード パターンを拡張することは、承認および取得要求と同じです。</span><span class="sxs-lookup"><span data-stu-id="bdbaf-157">Extending the void and refund request code pattern is same as the authorize and capture request.</span></span> <span data-ttu-id="bdbaf-158">拡張プロパティを渡す方法とともに、無効および払い戻し支払要求の完全なコードサンプルは、RetailSDK\Code\POS\Extensions\PaymentSample フォルダーの Retail SDK アプリケーション 3 で利用できます。</span><span class="sxs-lookup"><span data-stu-id="bdbaf-158">The full code sample for the void and refund payment request, with how to pass extension properties, is available in Retail SDK app update 3 in the RetailSDK\Code\POS\Extensions\PaymentSample folder.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]