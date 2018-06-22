---
title: "エンド ツー エンドの支払拡張機能を作成する"
description: "このトピックでは、支払端末のエンド・ツー・エンド支払統合を作成する方法について説明します。"
author: 
manager: AnnBe
ms.date: 02/21/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Developer
ms.reviewer: josaw
ms.search.scope: Operations, Retail
ms.custom: 
ms.search.region: Global
ms.search.industry: Retail
ms.author: rassadi
ms.search.validFrom: 2018-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 879eb9f2a63a8514791f74965005ed3e22bc0de7
ms.openlocfilehash: d681032b28c6df23a0591b2610e72edefcc40034
ms.contentlocale: ja-jp
ms.lasthandoff: 04/20/2018

---

# <a name="payment-integration-with-a-payment-terminal"></a><span data-ttu-id="84378-103">支払ターミナルとの支払の統合</span><span class="sxs-lookup"><span data-stu-id="84378-103">Payment integration with a payment terminal</span></span>
<span data-ttu-id="84378-104">このトピックでは、支払ゲートウェイと直接通信できる支払端末向けに Microsoft Dynamics 365 for Retail Modern POS とクラウド POS (POS) の支払統合を記述する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="84378-104">This topic describes how to write a payment integration for Microsoft Dynamics 365 for Retail Modern POS and Cloud POS (the POS) for a payment terminal that can directly communicate with the payment gateway.</span></span>

## <a name="key-terms"></a><span data-ttu-id="84378-105">重要な用語</span><span class="sxs-lookup"><span data-stu-id="84378-105">Key terms</span></span>

| <span data-ttu-id="84378-106">期間</span><span class="sxs-lookup"><span data-stu-id="84378-106">Term</span></span> | <span data-ttu-id="84378-107">説明</span><span class="sxs-lookup"><span data-stu-id="84378-107">Description</span></span> |
|---|---|
| <span data-ttu-id="84378-108">支払コネクタ</span><span class="sxs-lookup"><span data-stu-id="84378-108">Payment connector</span></span> | <span data-ttu-id="84378-109">POS に支払ターミナルを統合するために書き込まれた拡張ライブラリです。</span><span class="sxs-lookup"><span data-stu-id="84378-109">An extension library that is written to integrate the POS with a payment terminal.</span></span> |
| <span data-ttu-id="84378-110">支払プロセッサ</span><span class="sxs-lookup"><span data-stu-id="84378-110">Payment processor</span></span> | <span data-ttu-id="84378-111">支払コネクタで使用される商社プロパティを取得するために書き込まれる拡張ライブラリです。</span><span class="sxs-lookup"><span data-stu-id="84378-111">An extension library that is written to retrieve merchant properties that the payment connector uses.</span></span> |

## <a name="overview"></a><span data-ttu-id="84378-112">概要</span><span class="sxs-lookup"><span data-stu-id="84378-112">Overview</span></span>
<span data-ttu-id="84378-113">次の図は、POS を介した支払ターミナルの統合の概要を示しています。</span><span class="sxs-lookup"><span data-stu-id="84378-113">The following illustration shows a high-level overview of the payment terminal integration through the POS.</span></span> <span data-ttu-id="84378-114">この図では、ローカルのハードウェア ステーションを使用して支払端末と通信を使用することを前提にしていますが、同じパターンを共有のハードウェア ステーションにも適用できます。</span><span class="sxs-lookup"><span data-stu-id="84378-114">Although this illustration assumes that a local Hardware Station is used to communicate with the payment terminal, the same patterns apply to a shared Hardware Station.</span></span>

![支払コネクタ統合の概要](media/PAYMENTS/PAYMENT-TERMINAL/Overview.jpg)

<span data-ttu-id="84378-116">このトピックでは、支払端末のエンド・ツー・エンド支払統合を作成するために必要な以下の手順について説明します。</span><span class="sxs-lookup"><span data-stu-id="84378-116">This topic describes the following steps that are required to create an end-to-end payment integration for a payment terminal:</span></span>

- <span data-ttu-id="84378-117">**[支払コネクタの記述](#Write-a-payment-connector):** 支払コネクタは POS と支払ターミナルの間の主要な統合ポイントです。</span><span class="sxs-lookup"><span data-stu-id="84378-117">**[Write a payment connector](#Write-a-payment-connector):** The payment connector is the main integration point between the POS and the payment terminal.</span></span> <span data-ttu-id="84378-118">このステップのセクションでは、支払要求 (たとえば、承認、払い戻し、無効化要求) を支払端末に中継できる、新しい支払コネクタを実装し、設定する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="84378-118">The section for this step describes how to implement and configure a new payment connector that can relay payment requests (for example, authorize, refund, and void requests) to the payment terminal.</span></span> 
- <span data-ttu-id="84378-119">**[支払プロセッサの記述](#Write-a-payment-processor):** 支払プロセッサは、支払の統合の一部として使用される商社プロパティを定義するために使用します。</span><span class="sxs-lookup"><span data-stu-id="84378-119">**[Write a payment processor](#Write-a-payment-processor):** The payment processor is used to define the merchant properties that are used as part of the payment integration.</span></span> <span data-ttu-id="84378-120">このステップのセクションでは、新しい支払プロセッサを実装する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="84378-120">The section for this step describes how to implement a new payment processor.</span></span> <span data-ttu-id="84378-121">これには、実装する必要があるインターフェイスおよび従う必要があるパターンに関する情報が含まれています。</span><span class="sxs-lookup"><span data-stu-id="84378-121">It includes information about the interfaces that you should implement and patterns that you should follow.</span></span>

## <a name="write-a-payment-connector"></a><span data-ttu-id="84378-122">支払コネクタの記述</span><span class="sxs-lookup"><span data-stu-id="84378-122">Write a payment connector</span></span>
<span data-ttu-id="84378-123">次のこのセクションでは、新しい支払コネクタを記述する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="84378-123">This section describes how to write a new payment connector.</span></span>

### <a name="understanding-the-payment-flows"></a><span data-ttu-id="84378-124">支払フローを理解する</span><span class="sxs-lookup"><span data-stu-id="84378-124">Understanding the payment flows</span></span>
<span data-ttu-id="84378-125">次の図は、POS、ハードウェア ステーション、および支払コネクタ全体にわたるいくつかの支払フロー (トランザクションの開始、カート ラインの更新、承認、キャプチャ、および終了トランザクション) の概要を示しています。</span><span class="sxs-lookup"><span data-stu-id="84378-125">The following illustration shows a high-level overview of several payment flows (Begin Transaction, Update Cart Lines, Authorize, Capture, and End Transaction) across the POS, Hardware Station, and payment connector.</span></span>

![支払フローの概要](media/PAYMENTS/PAYMENT-TERMINAL/PaymentFlow.jpg)

### <a name="implement-a-payment-connector"></a><span data-ttu-id="84378-127">支払コネクタの実装</span><span class="sxs-lookup"><span data-stu-id="84378-127">Implement a payment connector</span></span>
<span data-ttu-id="84378-128">次のこのセクションでは、新しい支払コネクタを実装する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="84378-128">This section below describes how to implement a new payment connector.</span></span> <span data-ttu-id="84378-129">ここに示す例は、Retailソフトウェアの開発キット (SDK) の **SampleExtensions\HardwareStation\Extension.PaymentSample** フォルダーにある **PaymentDeviceSample** クラスにあります。</span><span class="sxs-lookup"><span data-stu-id="84378-129">The examples that are shown here can be found in the **PaymentDeviceSample** class that is located under the **SampleExtensions\HardwareStation\Extension.PaymentSample** folder in the Retail software development kit (SDK).</span></span>

#### <a name="implement-the-inamedrequesthandler-interface"></a><span data-ttu-id="84378-130">INamedRequestHandler インターフェイスの実装</span><span class="sxs-lookup"><span data-stu-id="84378-130">Implement the INamedRequestHandler interface</span></span>
<span data-ttu-id="84378-131">すべての POS 支払関連フローは、ハードウェア ステーションで要求/応答パターンを通じて処理されます。</span><span class="sxs-lookup"><span data-stu-id="84378-131">All POS payment-related flows are handled through request/response patterns in the Hardware Station.</span></span> <span data-ttu-id="84378-132">新しい支払コネクタを作成するプロセスの第一歩は、**Microsoft.Dynamics.Commerce.Runtime.Framework** ライブラリで定義されている **INamedRequestHandler** インターフェイスを実装するクラスを作成することです。</span><span class="sxs-lookup"><span data-stu-id="84378-132">The first step in the process of writing a new payment connector is to create a class that implements the **INamedRequestHandler** interface that is defined in the **Microsoft.Dynamics.Commerce.Runtime.Framework** library.</span></span>

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

<span data-ttu-id="84378-133">**HandlerName** 文字列は、Microsoft Dynamics 365 for Finance and Operations クライアントを通じて特定の POS で使用される支払コネクタを構成するために使用されます (このトピックの後半の情報を参照してください)。</span><span class="sxs-lookup"><span data-stu-id="84378-133">The **HandlerName** string is used to configure the payment connector that is used on a given POS register through the Microsoft Dynamics 365 for Finance and Operations client (see the information later in this topic).</span></span>

#### <a name="implement-supported-payment-requests"></a><span data-ttu-id="84378-134">サポートされている支払要求の実装</span><span class="sxs-lookup"><span data-stu-id="84378-134">Implement supported payment requests</span></span>
<span data-ttu-id="84378-135">支払関連フローを処理するには、支払コネクタが処理できる、サポートされている要求タイプを定義する必要があります。</span><span class="sxs-lookup"><span data-stu-id="84378-135">To process payment-related flows, the payment connector must define the supported request types that it can handle.</span></span> <span data-ttu-id="84378-136">また、**実行**メソッドは、コネクタが指定されたメソッドをサポートする各要求をルーティングするために実装する必要があります。</span><span class="sxs-lookup"><span data-stu-id="84378-136">Additionally, the **Execute** method must be implemented to route each request that the connector supports to a given method.</span></span> <span data-ttu-id="84378-137">次の例は、サポートされている要求のタイプの完全な一覧と、特定の要求 (すなわち、承認要求) の例を示しています。</span><span class="sxs-lookup"><span data-stu-id="84378-137">The following example shows the complete list of supported request types and an example of a specific request (that is, an authorize request).</span></span>

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

#### <a name="full-list-of-supported-request-types"></a><span data-ttu-id="84378-138">サポートされる要求タイプの完全な一覧</span><span class="sxs-lookup"><span data-stu-id="84378-138">Full list of supported request types</span></span>
<span data-ttu-id="84378-139">次のテーブルは、支払コネクタが実装できるサポートされているすべての要求のタイプを示しています。</span><span class="sxs-lookup"><span data-stu-id="84378-139">The following table describes all supported requests types that a payment connector can implement.</span></span>

| <span data-ttu-id="84378-140">クラスのリクエスト</span><span class="sxs-lookup"><span data-stu-id="84378-140">Request class</span></span> | <span data-ttu-id="84378-141">支払フローの説明</span><span class="sxs-lookup"><span data-stu-id="84378-141">Payment flow description</span></span> |
|---|---|
| <span data-ttu-id="84378-142">OpenPaymentTerminalDeviceRequest</span><span class="sxs-lookup"><span data-stu-id="84378-142">OpenPaymentTerminalDeviceRequest</span></span> | <span data-ttu-id="84378-143">この要求は、販売取引が開始される前に呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="84378-143">This request is called before a sales transaction is initiated.</span></span> <span data-ttu-id="84378-144">支払ターミナルへの接続を確立するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="84378-144">It is used to establish a connection to the payment terminal.</span></span> |
| <span data-ttu-id="84378-145">BeginTransactionPaymentTerminalDeviceRequest</span><span class="sxs-lookup"><span data-stu-id="84378-145">BeginTransactionPaymentTerminalDeviceRequest</span></span> | <span data-ttu-id="84378-146">この要求は、新しい販売取引が開始されたときに呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="84378-146">This request is called when a new sales transaction is initiated.</span></span> <span data-ttu-id="84378-147">支払ターミナルで初期化を処理するために使用されます (たとえば、トランザクション画面の初期化)。</span><span class="sxs-lookup"><span data-stu-id="84378-147">It is used to handle any initialization on the payment terminal (for example, by initializing the transaction screen).</span></span> |
| <span data-ttu-id="84378-148">UpdateLineItemsPaymentTerminalDeviceRequest</span><span class="sxs-lookup"><span data-stu-id="84378-148">UpdateLineItemsPaymentTerminalDeviceRequest</span></span> | <span data-ttu-id="84378-149">この要求は、カート内の明細行品目が更新されたときに呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="84378-149">This request is called when line items in the cart are updated.</span></span> |
| <span data-ttu-id="84378-150">AuthorizePaymentTerminalDeviceRequest</span><span class="sxs-lookup"><span data-stu-id="84378-150">AuthorizePaymentTerminalDeviceRequest</span></span> | <span data-ttu-id="84378-151">この要求は、POS 支払ビューで支払が開始されたときに呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="84378-151">This request is called when a payment is initiated in the POS payment view.</span></span> |
| <span data-ttu-id="84378-152">CancelOperationPaymentTerminalDeviceRequest</span><span class="sxs-lookup"><span data-stu-id="84378-152">CancelOperationPaymentTerminalDeviceRequest</span></span> | <span data-ttu-id="84378-153">この要求は、支払いが開始された後、支払い端末で支払いが完了する前に、支払いビュー ダイアログ ボックスで **キャンセル** ボタンを選択すると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="84378-153">This request is called when a user selects the **Cancel** button in the payment view dialog box after the payment is initiated but before the payment is completed on the payment terminal.</span></span> |
| <span data-ttu-id="84378-154">CapturePaymentTerminalDeviceRequest</span><span class="sxs-lookup"><span data-stu-id="84378-154">CapturePaymentTerminalDeviceRequest</span></span> | <span data-ttu-id="84378-155">この要求は、カート内の全額が支払われた時点で、販売取引が終了する前に、各支払い行に対して呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="84378-155">This request is called for each payment line when the whole amount in the cart is paid but before the sales transaction is concluded.</span></span> |
| <span data-ttu-id="84378-156">VoidPaymentTerminalDeviceRequest</span><span class="sxs-lookup"><span data-stu-id="84378-156">VoidPaymentTerminalDeviceRequest</span></span> | <span data-ttu-id="84378-157">この要求は、カート内の支払い行が無効になったときに呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="84378-157">This request is called when a payment line is voided in the cart.</span></span> |
| <span data-ttu-id="84378-158">RefundPaymentTerminalDeviceRequest</span><span class="sxs-lookup"><span data-stu-id="84378-158">RefundPaymentTerminalDeviceRequest</span></span> | <span data-ttu-id="84378-159">この要求は、払い戻しが行われたときに呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="84378-159">This request is called when a refund is issued.</span></span> |
| <span data-ttu-id="84378-160">FetchTokenPaymentTerminalDeviceRequest</span><span class="sxs-lookup"><span data-stu-id="84378-160">FetchTokenPaymentTerminalDeviceRequest</span></span> | <span data-ttu-id="84378-161">この要求は、顧客注文の繰延支払いをサポートするために支払トークンをフェッチするために呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="84378-161">This request is called to fetch a payment token to support deferred payments for customer orders.</span></span> |
| <span data-ttu-id="84378-162">EndTransactionPaymentTerminalDeviceRequest</span><span class="sxs-lookup"><span data-stu-id="84378-162">EndTransactionPaymentTerminalDeviceRequest</span></span> | <span data-ttu-id="84378-163">この要求は、販売取引が終了し、すべての支払いが取り込まれたときに呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="84378-163">This request is called when the sales transaction is concluded and all payments have been captured.</span></span> |
| <span data-ttu-id="84378-164">ClosePaymentTerminalDeviceRequest</span><span class="sxs-lookup"><span data-stu-id="84378-164">ClosePaymentTerminalDeviceRequest</span></span> | <span data-ttu-id="84378-165">この要求は、販売取引の終了後に呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="84378-165">This request is called after the sales transaction is concluded.</span></span> <span data-ttu-id="84378-166">支払ターミナルへの接続を閉じるために使用されます。</span><span class="sxs-lookup"><span data-stu-id="84378-166">It is used to close the connection to the payment terminal.</span></span> |
| <span data-ttu-id="84378-167">ActivateGiftCardPaymentTerminalRequest</span><span class="sxs-lookup"><span data-stu-id="84378-167">ActivateGiftCardPaymentTerminalRequest</span></span> | <span data-ttu-id="84378-168">この要求は、外部ギフト カードが POS を介して有効化されているときに呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="84378-168">This request is called when an external gift card is being activated through the POS.</span></span> |
| <span data-ttu-id="84378-169">AddBalanceToGiftCardPaymentTerminalRequest</span><span class="sxs-lookup"><span data-stu-id="84378-169">AddBalanceToGiftCardPaymentTerminalRequest</span></span> | <span data-ttu-id="84378-170">この要求は、外部ギフト カードに残高が追加されるときに呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="84378-170">This request is called when a balance is being added to an external gift card.</span></span> |
| <span data-ttu-id="84378-171">GetGiftCardBalancePaymentTerminalRequest</span><span class="sxs-lookup"><span data-stu-id="84378-171">GetGiftCardBalancePaymentTerminalRequest</span></span> | <span data-ttu-id="84378-172">この要求は、ギフト カードの残高が取得されるときに呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="84378-172">This request is called when the balance on the gift card is being retrieved.</span></span> |
| <span data-ttu-id="84378-173">GetPrivateTenderPaymentTerminalDeviceRequest</span><span class="sxs-lookup"><span data-stu-id="84378-173">GetPrivateTenderPaymentTerminalDeviceRequest</span></span> | <span data-ttu-id="84378-174">この要求は、ギフト カード番号がギフト カード フローの支払い端末から取得されたときに呼び出されます (ギフト カードの発行、ギフト カードによる支払い、ギフト カードへの追加など)。</span><span class="sxs-lookup"><span data-stu-id="84378-174">This request is called when gift card numbers are retrieved from the payment terminal for gift card flows (for example, Issue gift card, Pay by gift card, or Add to gift card).</span></span> |
| <span data-ttu-id="84378-175">ExecuteTaskPaymentTerminalDeviceRequest</span><span class="sxs-lookup"><span data-stu-id="84378-175">ExecuteTaskPaymentTerminalDeviceRequest</span></span> | <span data-ttu-id="84378-176">この拡張要求は、カスタマイズを介して POS から呼び出すことができます。</span><span class="sxs-lookup"><span data-stu-id="84378-176">This extension request can be invoked from the POS through customizations.</span></span> <span data-ttu-id="84378-177">支払に関連する追加のフローを有効にするために使用されます。</span><span class="sxs-lookup"><span data-stu-id="84378-177">It is used to enable additional payment-related flows.</span></span> |

##### <a name="openpaymentterminaldevicerequest"></a><span data-ttu-id="84378-178">OpenPaymentTerminalDeviceRequest</span><span class="sxs-lookup"><span data-stu-id="84378-178">OpenPaymentTerminalDeviceRequest</span></span>
###### <a name="signature"></a><span data-ttu-id="84378-179">署名</span><span class="sxs-lookup"><span data-stu-id="84378-179">Signature</span></span>
``` csharp
public OpenPaymentTerminalDeviceRequest(string token, string deviceName, SettingsInfo terminalSettings, PeripheralConfiguration deviceConfig, ExtensionTransaction extensionTransactionProperties);
```

###### <a name="variables"></a><span data-ttu-id="84378-180">変数</span><span class="sxs-lookup"><span data-stu-id="84378-180">Variables</span></span>

| <span data-ttu-id="84378-181">変動</span><span class="sxs-lookup"><span data-stu-id="84378-181">Variable</span></span> | <span data-ttu-id="84378-182">説明</span><span class="sxs-lookup"><span data-stu-id="84378-182">Description</span></span> |
|---|---|
| <span data-ttu-id="84378-183">token</span><span class="sxs-lookup"><span data-stu-id="84378-183">token</span></span> | <span data-ttu-id="84378-184">支払い端末が最初のトランザクションのためにロックされたときに生成される一意のトークン値。</span><span class="sxs-lookup"><span data-stu-id="84378-184">The unique token value that is generated when the payment terminal is initially locked for the transaction.</span></span> |
| <span data-ttu-id="84378-185">deviceName</span><span class="sxs-lookup"><span data-stu-id="84378-185">deviceName</span></span> | <span data-ttu-id="84378-186">Finance and Operations クライアントの **POS hardware profile** ページで定義されている、デバイスの名前。</span><span class="sxs-lookup"><span data-stu-id="84378-186">The name of the device, as defined on the **POS hardware profile** page in the Finance and Operations client.</span></span> |
| <span data-ttu-id="84378-187">terminalSettings</span><span class="sxs-lookup"><span data-stu-id="84378-187">terminalSettings</span></span> | <span data-ttu-id="84378-188">Finance and Operations クライアントで定義された支払端末固有の構成プロパティのセット。シグネチャ取り込みの最小額やデビット キャッシュバック限度などです。</span><span class="sxs-lookup"><span data-stu-id="84378-188">The set of payment terminal–specific configuration properties that are defined in the Finance and Operations client, such as the minimum amount for signature capture and the debit cash-back limit.</span></span> |
| <span data-ttu-id="84378-189">deviceConfig</span><span class="sxs-lookup"><span data-stu-id="84378-189">deviceConfig</span></span> | <span data-ttu-id="84378-190">ネットワーク端末の場合の IP アドレスやポートなど、名前/値のペアの形式の支払端末固有の設定プロパティのセット。</span><span class="sxs-lookup"><span data-stu-id="84378-190">The set of payment terminal–specific configuration properties in the form of name/value pairs, such as the IP address and port in the case of network devices.</span></span> |
| <span data-ttu-id="84378-191">extensionTransactionProperties</span><span class="sxs-lookup"><span data-stu-id="84378-191">extensionTransactionProperties</span></span> | <span data-ttu-id="84378-192">名前/値のペアの形式の拡張構成プロパティのセット。</span><span class="sxs-lookup"><span data-stu-id="84378-192">The set of extension configuration properties in the form of name/value pairs.</span></span> |

##### <a name="begintransactionpaymentterminaldevicerequest"></a><span data-ttu-id="84378-193">BeginTransactionPaymentTerminalDeviceRequest</span><span class="sxs-lookup"><span data-stu-id="84378-193">BeginTransactionPaymentTerminalDeviceRequest</span></span>
###### <a name="signature"></a><span data-ttu-id="84378-194">署名</span><span class="sxs-lookup"><span data-stu-id="84378-194">Signature</span></span>
``` csharp
public BeginTransactionPaymentTerminalDeviceRequest(string token, string paymentConnectorName, string merchantInformation, string invoiceNumber, bool isTestMode, ExtensionTransaction extensionTransactionProperties)
```

###### <a name="variables"></a><span data-ttu-id="84378-195">変数</span><span class="sxs-lookup"><span data-stu-id="84378-195">Variables</span></span>

| <span data-ttu-id="84378-196">変動</span><span class="sxs-lookup"><span data-stu-id="84378-196">Variable</span></span> | <span data-ttu-id="84378-197">説明</span><span class="sxs-lookup"><span data-stu-id="84378-197">Description</span></span> |
|---|---|
| <span data-ttu-id="84378-198">token</span><span class="sxs-lookup"><span data-stu-id="84378-198">token</span></span> | <span data-ttu-id="84378-199">支払い端末が最初のトランザクションのためにロックされたときに生成される一意のトークン値。</span><span class="sxs-lookup"><span data-stu-id="84378-199">The unique token value that is generated when the payment terminal is initially locked for the transaction.</span></span> |
| <span data-ttu-id="84378-200">paymentConnectorName</span><span class="sxs-lookup"><span data-stu-id="84378-200">paymentConnectorName</span></span> | <span data-ttu-id="84378-201">支払フローの一部として使用される支払コネクタの名前。</span><span class="sxs-lookup"><span data-stu-id="84378-201">The name of the payment connector that is used as part of the payment flow.</span></span> <span data-ttu-id="84378-202">この変数は、**IPaymentProcessor** インターフェイスを使用する支払フローと統合する予定がある場合に使用されます。</span><span class="sxs-lookup"><span data-stu-id="84378-202">This variable is used if you plan to integrate with payment flows that use the **IPaymentProcessor** interface.</span></span> |
| <span data-ttu-id="84378-203">merchantInformation</span><span class="sxs-lookup"><span data-stu-id="84378-203">merchantInformation</span></span> | <span data-ttu-id="84378-204">Finance and Operations クライアントの **POS hardware profile** ページで定義されている商社情報。</span><span class="sxs-lookup"><span data-stu-id="84378-204">The merchant information that is defined on the **POS hardware profile** page in the Finance and Operations client.</span></span> |
| <span data-ttu-id="84378-205">invoiceNumber</span><span class="sxs-lookup"><span data-stu-id="84378-205">invoiceNumber</span></span> | <span data-ttu-id="84378-206">POS が販売トランザクションを追跡するために生成する一意の請求書番号。</span><span class="sxs-lookup"><span data-stu-id="84378-206">The unique invoice number that the POS generates to track the sales transaction.</span></span> |
| <span data-ttu-id="84378-207">isTestMode</span><span class="sxs-lookup"><span data-stu-id="84378-207">isTestMode</span></span> | <span data-ttu-id="84378-208">支払コネクタがテスト モードで使用されているかどうかを示す値。</span><span class="sxs-lookup"><span data-stu-id="84378-208">A value that indicates whether the payment connector is being used in testing mode.</span></span> |
| <span data-ttu-id="84378-209">extensionTransactionProperties</span><span class="sxs-lookup"><span data-stu-id="84378-209">extensionTransactionProperties</span></span> | <span data-ttu-id="84378-210">名前/値のペアの形式の拡張構成プロパティのセット。</span><span class="sxs-lookup"><span data-stu-id="84378-210">The set of extension configuration properties in the form of name/value pairs.</span></span> |

##### <a name="updatelineitemspaymentterminaldevicerequest"></a><span data-ttu-id="84378-211">UpdateLineItemsPaymentTerminalDeviceRequest</span><span class="sxs-lookup"><span data-stu-id="84378-211">UpdateLineItemsPaymentTerminalDeviceRequest</span></span>
###### <a name="signature"></a><span data-ttu-id="84378-212">署名</span><span class="sxs-lookup"><span data-stu-id="84378-212">Signature</span></span>
``` csharp
public UpdateLineItemsPaymentTerminalDeviceRequest(string token, string totalAmount, string taxAmount, string discountAmount, string subTotalAmount, IEnumerable<ItemInfo> items, ExtensionTransaction extensionTransactionProperties = null)
```

###### <a name="variables"></a><span data-ttu-id="84378-213">変数</span><span class="sxs-lookup"><span data-stu-id="84378-213">Variables</span></span>

| <span data-ttu-id="84378-214">変動</span><span class="sxs-lookup"><span data-stu-id="84378-214">Variable</span></span> | <span data-ttu-id="84378-215">説明</span><span class="sxs-lookup"><span data-stu-id="84378-215">Description</span></span> |
|---|---|
| <span data-ttu-id="84378-216">token</span><span class="sxs-lookup"><span data-stu-id="84378-216">token</span></span> | <span data-ttu-id="84378-217">支払い端末が最初のトランザクションのためにロックされたときに生成される一意のトークン値。</span><span class="sxs-lookup"><span data-stu-id="84378-217">The unique token value that is generated when the payment terminal is initially locked for the transaction.</span></span> |
| <span data-ttu-id="84378-218">totalAmount</span><span class="sxs-lookup"><span data-stu-id="84378-218">totalAmount</span></span> | <span data-ttu-id="84378-219">現在の販売トランザクションでの合計金額。</span><span class="sxs-lookup"><span data-stu-id="84378-219">The total amount on the current sales transaction.</span></span> |
| <span data-ttu-id="84378-220">taxAmount</span><span class="sxs-lookup"><span data-stu-id="84378-220">taxAmount</span></span> | <span data-ttu-id="84378-221">現在の販売トランザクションでの税金額。</span><span class="sxs-lookup"><span data-stu-id="84378-221">The tax amount on the current sales transaction.</span></span> |
| <span data-ttu-id="84378-222">discountAmount</span><span class="sxs-lookup"><span data-stu-id="84378-222">discountAmount</span></span> | <span data-ttu-id="84378-223">現在の販売トランザクションでの割引金額。</span><span class="sxs-lookup"><span data-stu-id="84378-223">The discount amount on the current sales transaction.</span></span> |
| <span data-ttu-id="84378-224">subTotalAmount</span><span class="sxs-lookup"><span data-stu-id="84378-224">subTotalAmount</span></span> | <span data-ttu-id="84378-225">現在の販売トランザクションでの小計金額。</span><span class="sxs-lookup"><span data-stu-id="84378-225">The subtotal amount on the current sales transaction.</span></span> |
| <span data-ttu-id="84378-226">項目</span><span class="sxs-lookup"><span data-stu-id="84378-226">items</span></span> | <span data-ttu-id="84378-227">表示する明細行品目のリスト。</span><span class="sxs-lookup"><span data-stu-id="84378-227">The list of line items to show.</span></span> |
| <span data-ttu-id="84378-228">extensionTransactionProperties</span><span class="sxs-lookup"><span data-stu-id="84378-228">extensionTransactionProperties</span></span> | <span data-ttu-id="84378-229">名前/値のペアの形式の拡張構成プロパティのセット。</span><span class="sxs-lookup"><span data-stu-id="84378-229">The set of extension configuration properties in the form of name/value pairs.</span></span> |

##### <a name="authorizepaymentterminaldevicerequest"></a><span data-ttu-id="84378-230">AuthorizePaymentTerminalDeviceRequest</span><span class="sxs-lookup"><span data-stu-id="84378-230">AuthorizePaymentTerminalDeviceRequest</span></span>
###### <a name="signature"></a><span data-ttu-id="84378-231">署名</span><span class="sxs-lookup"><span data-stu-id="84378-231">Signature</span></span>
``` csharp
public AuthorizePaymentTerminalDeviceRequest(string token, string paymentConnectorName, decimal amount, string currency, TenderInfo tenderInfo, string voiceAuthorization, bool isManualEntry, ExtensionTransaction extensionTransactionProperties)
```

###### <a name="variables"></a><span data-ttu-id="84378-232">変数</span><span class="sxs-lookup"><span data-stu-id="84378-232">Variables</span></span>

| <span data-ttu-id="84378-233">変動</span><span class="sxs-lookup"><span data-stu-id="84378-233">Variable</span></span> | <span data-ttu-id="84378-234">説明</span><span class="sxs-lookup"><span data-stu-id="84378-234">Description</span></span> |
|---|---|
| <span data-ttu-id="84378-235">token</span><span class="sxs-lookup"><span data-stu-id="84378-235">token</span></span> | <span data-ttu-id="84378-236">支払い端末が最初のトランザクションのためにロックされたときに生成される一意のトークン値。</span><span class="sxs-lookup"><span data-stu-id="84378-236">The unique token value that is generated when the payment terminal is initially locked for the transaction.</span></span> |
| <span data-ttu-id="84378-237">paymentConnectorName</span><span class="sxs-lookup"><span data-stu-id="84378-237">paymentConnectorName</span></span> | <span data-ttu-id="84378-238">支払フローの一部として使用される支払コネクタの名前。</span><span class="sxs-lookup"><span data-stu-id="84378-238">The name of the payment connector that is used as part of the payment flow.</span></span> <span data-ttu-id="84378-239">この変数は、**IPaymentProcessor** インターフェイスを使用する支払フローとの統合がある場合に使用されます。</span><span class="sxs-lookup"><span data-stu-id="84378-239">This variable is used if there is an integration with payment flows that use the **IPaymentProcessor** interface.</span></span> |
| <span data-ttu-id="84378-240">金額</span><span class="sxs-lookup"><span data-stu-id="84378-240">amount</span></span> | <span data-ttu-id="84378-241">承認する金額。</span><span class="sxs-lookup"><span data-stu-id="84378-241">The amount to authorize.</span></span> |
| <span data-ttu-id="84378-242">通貨</span><span class="sxs-lookup"><span data-stu-id="84378-242">currency</span></span> | <span data-ttu-id="84378-243">承認する金額の通貨。</span><span class="sxs-lookup"><span data-stu-id="84378-243">The currency for the amount to authorize.</span></span> |
| <span data-ttu-id="84378-244">tenderInfo</span><span class="sxs-lookup"><span data-stu-id="84378-244">tenderInfo</span></span> | <span data-ttu-id="84378-245">外部ソースから取得された POS から送信されるカード情報 (外部ソースがある場合)。</span><span class="sxs-lookup"><span data-stu-id="84378-245">The card information that is sent from the POS that is retrieved from an external source (if an external source is present).</span></span> |
| <span data-ttu-id="84378-246">voiceAuthorization</span><span class="sxs-lookup"><span data-stu-id="84378-246">voiceAuthorization</span></span> | <span data-ttu-id="84378-247">音声認証が必要な場合は、POS から送信される音声承認コード。</span><span class="sxs-lookup"><span data-stu-id="84378-247">The voice approval code that is sent from the POS if voice authorization is required.</span></span> |
| <span data-ttu-id="84378-248">isManualEntry</span><span class="sxs-lookup"><span data-stu-id="84378-248">isManualEntry</span></span> | <span data-ttu-id="84378-249">カード番号を手動で入力されたかどうかを定義する値。</span><span class="sxs-lookup"><span data-stu-id="84378-249">A value that defines whether the card number was entered manually.</span></span> |
| <span data-ttu-id="84378-250">extensionTransactionProperties</span><span class="sxs-lookup"><span data-stu-id="84378-250">extensionTransactionProperties</span></span> | <span data-ttu-id="84378-251">名前/値のペアの形式の拡張構成プロパティのセット。</span><span class="sxs-lookup"><span data-stu-id="84378-251">The set of extension configuration properties in the form of name/value pairs.</span></span> |

###### <a name="response"></a><span data-ttu-id="84378-252">応答</span><span class="sxs-lookup"><span data-stu-id="84378-252">Response</span></span>
<span data-ttu-id="84378-253">**AuthorizePaymentCardPaymentResponse** 応答オブジェクトは、**AuthorizePaymentTerminalDeviceRequest** 要求が処理されたときに返される必要があります。</span><span class="sxs-lookup"><span data-stu-id="84378-253">The **AuthorizePaymentCardPaymentResponse** response object must be returned when the **AuthorizePaymentTerminalDeviceRequest** request is handled.</span></span> <span data-ttu-id="84378-254">応答には、次の必須プロパティを持つ **PaymentInfo** オブジェクトのインスタンスが含まれている必要があります。</span><span class="sxs-lookup"><span data-stu-id="84378-254">The response must contain an instance of the **PaymentInfo** object that has the following required properties.</span></span>

| <span data-ttu-id="84378-255">プロパティ</span><span class="sxs-lookup"><span data-stu-id="84378-255">Property</span></span> | <span data-ttu-id="84378-256">説明</span><span class="sxs-lookup"><span data-stu-id="84378-256">Description</span></span> |
|---|---|
| <span data-ttu-id="84378-257">ApprovedAmount</span><span class="sxs-lookup"><span data-stu-id="84378-257">ApprovedAmount</span></span> | <span data-ttu-id="84378-258">トランザクションに対して承認された金額。</span><span class="sxs-lookup"><span data-stu-id="84378-258">The amount that was approved for the transaction.</span></span> |
| <span data-ttu-id="84378-259">CardNumberMasked</span><span class="sxs-lookup"><span data-stu-id="84378-259">CardNumberMasked</span></span> | <span data-ttu-id="84378-260">マスクされたクレジット カード番号。</span><span class="sxs-lookup"><span data-stu-id="84378-260">The masked credit card number.</span></span> <span data-ttu-id="84378-261">この値には、少なくとも POS 内の在庫置場範囲の参照をサポートするため、クレジット カードの最初の桁が含まれている必要があります。</span><span class="sxs-lookup"><span data-stu-id="84378-261">The value must contain at least the first digit of the credit card to support bin range lookup in the POS.</span></span> <span data-ttu-id="84378-262">(ほとんどのデバイスは、最初の 6 桁と最後の 4 桁を返します。)</span><span class="sxs-lookup"><span data-stu-id="84378-262">(Most devices return the first six digits and the last four digits.)</span></span> |
| <span data-ttu-id="84378-263">CardType</span><span class="sxs-lookup"><span data-stu-id="84378-263">CardType</span></span> | <span data-ttu-id="84378-264">**Microsoft.Dynamics.Commerce.HardwareStation.CardPayment.CardType** エンティティを使用して支払い (**クレジット** または **デビット** など) に使われたカードのタイプ。</span><span class="sxs-lookup"><span data-stu-id="84378-264">The type of card that was used for the payment (for example, **Credit** or **Debit**) by using the **Microsoft.Dynamics.Commerce.HardwareStation.CardPayment.CardType** entity.</span></span> |
| <span data-ttu-id="84378-265">CashbackAmount</span><span class="sxs-lookup"><span data-stu-id="84378-265">CashbackAmount</span></span> | <span data-ttu-id="84378-266">借方トランザクションの場合、キャッシュ バック金額は支払のターミナルで定義されました。</span><span class="sxs-lookup"><span data-stu-id="84378-266">For debit transactions, the cash-back amount that was defined on the payment terminal.</span></span> |
| <span data-ttu-id="84378-267">エラー</span><span class="sxs-lookup"><span data-stu-id="84378-267">Errors</span></span> | <span data-ttu-id="84378-268">承認呼び出し中に発生したエラーのリスト。</span><span class="sxs-lookup"><span data-stu-id="84378-268">The list of errors that occurred during the authorize call.</span></span> |
| <span data-ttu-id="84378-269">IsApproved</span><span class="sxs-lookup"><span data-stu-id="84378-269">IsApproved</span></span> | <span data-ttu-id="84378-270">支払が承認されたかどうかを示すフラグ。</span><span class="sxs-lookup"><span data-stu-id="84378-270">A flag that indicates whether the payment was approved.</span></span> |
| <span data-ttu-id="84378-271">PaymentSdkData</span><span class="sxs-lookup"><span data-stu-id="84378-271">PaymentSdkData</span></span> | <span data-ttu-id="84378-272">承認/返金と、キャプチャ/呼び出しの無効化またはクロスチャネルの支払操作の間の状態をサポートするために使用される応答データ。</span><span class="sxs-lookup"><span data-stu-id="84378-272">The response data that is used to support state between the authorize/refund and capture/void calls or cross-channel payment operations.</span></span> |

<span data-ttu-id="84378-273">**PaymentSdkData** プロパティには、次のデータを含める必要があります。</span><span class="sxs-lookup"><span data-stu-id="84378-273">The **PaymentSdkData** property must contain the following data.</span></span>

| <span data-ttu-id="84378-274">名前空間</span><span class="sxs-lookup"><span data-stu-id="84378-274">Namespace</span></span> | <span data-ttu-id="84378-275">氏名</span><span class="sxs-lookup"><span data-stu-id="84378-275">Name</span></span> | <span data-ttu-id="84378-276">説明</span><span class="sxs-lookup"><span data-stu-id="84378-276">Description</span></span> | <span data-ttu-id="84378-277">サンプル値</span><span class="sxs-lookup"><span data-stu-id="84378-277">Sample value</span></span> |
|---|---|---|---|
| <span data-ttu-id="84378-278">コネクタ</span><span class="sxs-lookup"><span data-stu-id="84378-278">Connector</span></span> | <span data-ttu-id="84378-279">ConnectorName</span><span class="sxs-lookup"><span data-stu-id="84378-279">ConnectorName</span></span> | <span data-ttu-id="84378-280">このトピックの後半にある「支払プロセッサの記述」セクションで説明している、トランザクションに使用される **IPaymentProcessor**インターフェイスの名前です。</span><span class="sxs-lookup"><span data-stu-id="84378-280">The name of the **IPaymentProcessor** interface that is used for the transactions, as described in the "Write a payment processor" section later in this topic.</span></span> |
| <span data-ttu-id="84378-281">AuthorizationResponse</span><span class="sxs-lookup"><span data-stu-id="84378-281">AuthorizationResponse</span></span> | <span data-ttu-id="84378-282">プロパティ</span><span class="sxs-lookup"><span data-stu-id="84378-282">Properties</span></span> | <span data-ttu-id="84378-283">承認応答のリスト。</span><span class="sxs-lookup"><span data-stu-id="84378-283">The list of authorization responses.</span></span> | <span data-ttu-id="84378-284">次の表を参照してください。</span><span class="sxs-lookup"><span data-stu-id="84378-284">See the next table.</span></span> |

<span data-ttu-id="84378-285">**PaymentSdkData** プロパティの **プロパティ** フィールドには、次のフィールドを含める必要があります。</span><span class="sxs-lookup"><span data-stu-id="84378-285">The **Properties** field of the **PaymentSdkData** property must contain the following fields.</span></span>

| <span data-ttu-id="84378-286">名前空間</span><span class="sxs-lookup"><span data-stu-id="84378-286">Namespace</span></span> | <span data-ttu-id="84378-287">氏名</span><span class="sxs-lookup"><span data-stu-id="84378-287">Name</span></span> | <span data-ttu-id="84378-288">説明</span><span class="sxs-lookup"><span data-stu-id="84378-288">Description</span></span> | <span data-ttu-id="84378-289">サンプル値</span><span class="sxs-lookup"><span data-stu-id="84378-289">Sample value</span></span> |
|---|---|---|---|
| <span data-ttu-id="84378-290">AuthorizationResponse</span><span class="sxs-lookup"><span data-stu-id="84378-290">AuthorizationResponse</span></span> | <span data-ttu-id="84378-291">ApprovedAmount</span><span class="sxs-lookup"><span data-stu-id="84378-291">ApprovedAmount</span></span> | <span data-ttu-id="84378-292">トランザクションに対して承認された金額。</span><span class="sxs-lookup"><span data-stu-id="84378-292">The amount that was approved for the transaction.</span></span> | <span data-ttu-id="84378-293">28.08 m</span><span class="sxs-lookup"><span data-stu-id="84378-293">28.08m</span></span> |
| <span data-ttu-id="84378-294">AuthorizationResponse</span><span class="sxs-lookup"><span data-stu-id="84378-294">AuthorizationResponse</span></span> | <span data-ttu-id="84378-295">AvailableBalance</span><span class="sxs-lookup"><span data-stu-id="84378-295">AvailableBalance</span></span> | <span data-ttu-id="84378-296">カードの使用可能な残高。</span><span class="sxs-lookup"><span data-stu-id="84378-296">The available balance on the card.</span></span> | <span data-ttu-id="84378-297">100.00m</span><span class="sxs-lookup"><span data-stu-id="84378-297">100.00m</span></span> |
| <span data-ttu-id="84378-298">AuthorizationResponse</span><span class="sxs-lookup"><span data-stu-id="84378-298">AuthorizationResponse</span></span> | <span data-ttu-id="84378-299">ApprovalCode</span><span class="sxs-lookup"><span data-stu-id="84378-299">ApprovalCode</span></span> | <span data-ttu-id="84378-300">トランザクションの承認コード。</span><span class="sxs-lookup"><span data-stu-id="84378-300">The approval code for the transaction.</span></span> | <span data-ttu-id="84378-301">Z123456</span><span class="sxs-lookup"><span data-stu-id="84378-301">Z123456</span></span> |
| <span data-ttu-id="84378-302">AuthorizationResponse</span><span class="sxs-lookup"><span data-stu-id="84378-302">AuthorizationResponse</span></span> | <span data-ttu-id="84378-303">ProviderTransactionId</span><span class="sxs-lookup"><span data-stu-id="84378-303">ProviderTransactionId</span></span> | <span data-ttu-id="84378-304">支払いプロバイダーのトランザクション識別子。</span><span class="sxs-lookup"><span data-stu-id="84378-304">The transaction identifier of the payment provider.</span></span> | <span data-ttu-id="84378-305">123456789</span><span class="sxs-lookup"><span data-stu-id="84378-305">123456789</span></span> |
| <span data-ttu-id="84378-306">AuthorizationResponse</span><span class="sxs-lookup"><span data-stu-id="84378-306">AuthorizationResponse</span></span> | <span data-ttu-id="84378-307">AuthorizationResult</span><span class="sxs-lookup"><span data-stu-id="84378-307">AuthorizationResult</span></span> | <span data-ttu-id="84378-308">権限呼び出しの結果。</span><span class="sxs-lookup"><span data-stu-id="84378-308">The result of the authorization call.</span></span> | <span data-ttu-id="84378-309">AuthorizationResult.Success.ToString()</span><span class="sxs-lookup"><span data-stu-id="84378-309">AuthorizationResult.Success.ToString()</span></span> |
| <span data-ttu-id="84378-310">AuthorizationResponse</span><span class="sxs-lookup"><span data-stu-id="84378-310">AuthorizationResponse</span></span> | <span data-ttu-id="84378-311">ExternalReceipt</span><span class="sxs-lookup"><span data-stu-id="84378-311">ExternalReceipt</span></span> | <span data-ttu-id="84378-312">支払プロバイダーからの外部レシート データ。</span><span class="sxs-lookup"><span data-stu-id="84378-312">The external receipt data from the payment provider.</span></span> | <span data-ttu-id="84378-313">\<ReceiptData\>...\</ReceiptData\></span><span class="sxs-lookup"><span data-stu-id="84378-313">\<ReceiptData\>...\</ReceiptData\></span></span> |
| <span data-ttu-id="84378-314">AuthorizationResponse</span><span class="sxs-lookup"><span data-stu-id="84378-314">AuthorizationResponse</span></span> | <span data-ttu-id="84378-315">TerminalId</span><span class="sxs-lookup"><span data-stu-id="84378-315">TerminalId</span></span> | <span data-ttu-id="84378-316">支払を処理した端末の一意の識別子。</span><span class="sxs-lookup"><span data-stu-id="84378-316">The unique identifier of the terminal that handled the payment.</span></span> | <span data-ttu-id="84378-317">000001</span><span class="sxs-lookup"><span data-stu-id="84378-317">000001</span></span> |

<span data-ttu-id="84378-318">次の例は、**PaymentSdkData** オブジェクトを作成する方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="84378-318">The following example shows how to construct the **PaymentSdkData** object.</span></span>

``` csharp
List<PaymentProperty> paymentSdkProperties = new List<PaymentProperty>();
paymentSdkProperties.Add(new PaymentProperty(GenericNamespace.Connector, ConnectorProperties.ConnectorName, "TestConnector");

List<PaymentProperty> paymentSdkAuthorizationProperties = new List<PaymentProperty>();
paymentSdkAuthorizationProperties.Add(new PaymentProperty(GenericNamespace.AuthorizationResponse, AuthorizationResponseProperties.ApprovedAmount, 28.08m);
paymentSdkAuthorizationProperties.Add(new PaymentProperty(GenericNamespace.AuthorizationResponse, AuthorizationResponseProperties.AvailableBalane, 100.00);
paymentSdkAuthorizationProperties.Add(new PaymentProperty(GenericNamespace.AuthorizationResponse, AuthorizationResponseProperties.ApprovalCode, "Z123456");
paymentSdkAuthorizationProperties.Add(new PaymentProperty(GenericNamespace.AuthorizationResponse, AuthorizationResponseProperties.ProviderTrasactionId, "123456789");
paymentSdkAuthorizationProperties.Add(new PaymentProperty(GenericNamespace.AuthorizationResponse, AuthorizationResponseProperties.AuthorizationResult, AuthorizationResult.Success.ToString());
paymentSdkAuthorizationProperties.Add(new PaymentProperty(GenericNamespace.AuthorizationResponse, TransactionDataProperties.TerminalId, "000001");

paymentSdkProperties.Add(new PaymentProperty(GenericNamespace.AuthorizationResponse, AuthorizationResponseProperties.Properties, paymentSdkAuthorizationProperties.ToArray()));

string paymentSdkData = PaymentProperty.ConvertPropertyArrayToXML(paymentSdkProperties.ToArray());
```

<span data-ttu-id="84378-319">支払端末がレシートを返す場合、先ほど説明した **ExternalReceipt** オブジェクトで次のデータを設定し、POS を介して印刷することができます。</span><span class="sxs-lookup"><span data-stu-id="84378-319">If the payment terminal returns a receipt, you can print it through the POS by setting the following data on the **ExternalReceipt** object that was described earlier.</span></span>

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

###### <a name="other-considerations"></a><span data-ttu-id="84378-320">その他の考慮事項</span><span class="sxs-lookup"><span data-stu-id="84378-320">Other considerations</span></span>
<span data-ttu-id="84378-321">支払端末が 1 つの呼び出しでの要求を承認し、キャプチャし (つまり*迅速なキャプチャ*が発生する場合)、出納係が取引を無効にすることを希望する場合、支払い端末では即時回収の取消がサポートされている必要があります。</span><span class="sxs-lookup"><span data-stu-id="84378-321">If the payment terminal handles the authorize and capture requests in a single call (that is, if *immediate capture* occurs), and the cashier wants to void the transaction, the payment terminal must support reversal of an immediate capture.</span></span> <span data-ttu-id="84378-322">迅速なキャプチャが無効なとき、無効化要求が失敗した場合、レジ担当者は、ローカルで支払を無効にするかどうかを求められます。</span><span class="sxs-lookup"><span data-stu-id="84378-322">When an immediate capture is voided, if the void request fails, the cashier will be asked whether he or she wants to locally void the payment.</span></span> <span data-ttu-id="84378-323">レジ担当者が**はい**と選択した場合、入札は POS でのみ無効になります。</span><span class="sxs-lookup"><span data-stu-id="84378-323">If the cashier selects **Yes**, the tender is voided only in the POS.</span></span> <span data-ttu-id="84378-324">支払を無効にするために支払ターミナルに対して行われる呼び出しはありません。</span><span class="sxs-lookup"><span data-stu-id="84378-324">No call is made to the payment terminal to void the payment.</span></span> <span data-ttu-id="84378-325">基本的には、この動作により、支払ターミナルの支払を無効にできなくなった場合レジ担当者は POS をブロック解除することができます。</span><span class="sxs-lookup"><span data-stu-id="84378-325">Basically, this behavior lets the cashier unblock the POS if it can no longer void the payment on the payment terminal.</span></span> <span data-ttu-id="84378-326">ただし、銀行が取り消すまでの 3 ~ 5日間はロックが続くため、この動作には問題が生じますが、迅速なキャプチャのための支払いが行われます。</span><span class="sxs-lookup"><span data-stu-id="84378-326">However, this behavior can cause issues, because a lock lasts for three to five days, until the bank reverses it, but the payment is made for immediate capture.</span></span> <span data-ttu-id="84378-327">したがって、重複した支払いが発生する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="84378-327">Therefore, duplicate payments can occur.</span></span>

##### <a name="canceloperationpaymentterminaldevicerequest"></a><span data-ttu-id="84378-328">CancelOperationPaymentTerminalDeviceRequest</span><span class="sxs-lookup"><span data-stu-id="84378-328">CancelOperationPaymentTerminalDeviceRequest</span></span>
###### <a name="signature"></a><span data-ttu-id="84378-329">署名</span><span class="sxs-lookup"><span data-stu-id="84378-329">Signature</span></span>
``` csharp
public CancelOperationPaymentTerminalDeviceRequest(string token)
```

###### <a name="variables"></a><span data-ttu-id="84378-330">変数</span><span class="sxs-lookup"><span data-stu-id="84378-330">Variables</span></span>

| <span data-ttu-id="84378-331">変動</span><span class="sxs-lookup"><span data-stu-id="84378-331">Variable</span></span> | <span data-ttu-id="84378-332">説明</span><span class="sxs-lookup"><span data-stu-id="84378-332">Description</span></span> |
|---|---|
| <span data-ttu-id="84378-333">token</span><span class="sxs-lookup"><span data-stu-id="84378-333">token</span></span> | <span data-ttu-id="84378-334">支払い端末が最初のトランザクションのためにロックされたときに生成される一意のトークン値。</span><span class="sxs-lookup"><span data-stu-id="84378-334">The unique token value that is generated when the payment terminal is initially locked for the transaction.</span></span> |

##### <a name="capturepaymentterminaldevicerequest"></a><span data-ttu-id="84378-335">CapturePaymentTerminalDeviceRequest</span><span class="sxs-lookup"><span data-stu-id="84378-335">CapturePaymentTerminalDeviceRequest</span></span>
###### <a name="signature"></a><span data-ttu-id="84378-336">署名</span><span class="sxs-lookup"><span data-stu-id="84378-336">Signature</span></span>
``` csharp
public CapturePaymentTerminalDeviceRequest(string token, decimal amount, string currency, string paymentPropertiesXml, ExtensionTransaction extensionTransactionProperties)
```

###### <a name="variables"></a><span data-ttu-id="84378-337">変数</span><span class="sxs-lookup"><span data-stu-id="84378-337">Variables</span></span>

| <span data-ttu-id="84378-338">変動</span><span class="sxs-lookup"><span data-stu-id="84378-338">Variable</span></span> | <span data-ttu-id="84378-339">説明</span><span class="sxs-lookup"><span data-stu-id="84378-339">Description</span></span> |
|---|---|
| <span data-ttu-id="84378-340">token</span><span class="sxs-lookup"><span data-stu-id="84378-340">token</span></span> | <span data-ttu-id="84378-341">支払い端末が最初のトランザクションのためにロックされたときに生成される一意のトークン値。</span><span class="sxs-lookup"><span data-stu-id="84378-341">The unique token value that is generated when the payment terminal is initially locked for the transaction.</span></span> |
| <span data-ttu-id="84378-342">金額</span><span class="sxs-lookup"><span data-stu-id="84378-342">amount</span></span> | <span data-ttu-id="84378-343">取得する金額。</span><span class="sxs-lookup"><span data-stu-id="84378-343">The amount to capture.</span></span> |
| <span data-ttu-id="84378-344">通貨</span><span class="sxs-lookup"><span data-stu-id="84378-344">currency</span></span> | <span data-ttu-id="84378-345">取得する金額の通貨。</span><span class="sxs-lookup"><span data-stu-id="84378-345">The currency for the amount to capture.</span></span> |
| <span data-ttu-id="84378-346">paymentPropertiesXml</span><span class="sxs-lookup"><span data-stu-id="84378-346">paymentPropertiesXml</span></span> | <span data-ttu-id="84378-347">**AuthorizePaymentTerminalDeviceRequest** 要求または **RefundPaymentTerminalDeviceRequest** 要求によって返され、要求間のステートフル プロパティをサポートするために使用される **PaymentSdkData** オブジェクトのコンテンツ。</span><span class="sxs-lookup"><span data-stu-id="84378-347">The content of the **PaymentSdkData** object that is returned by the **AuthorizePaymentTerminalDeviceRequest** or **RefundPaymentTerminalDeviceRequest** request, and that is used to support stateful properties between the requests.</span></span> |
| <span data-ttu-id="84378-348">extensionTransactionProperties</span><span class="sxs-lookup"><span data-stu-id="84378-348">extensionTransactionProperties</span></span> | <span data-ttu-id="84378-349">名前/値のペアの形式の拡張構成プロパティのセット。</span><span class="sxs-lookup"><span data-stu-id="84378-349">The set of extension configuration properties in the form of name/value pairs.</span></span> |

###### <a name="other-considerations"></a><span data-ttu-id="84378-350">その他の考慮事項</span><span class="sxs-lookup"><span data-stu-id="84378-350">Other considerations</span></span>
<span data-ttu-id="84378-351">支払端末が 1 つの呼び出しでの要求を承認およびキャプチャする場合、**CapturePaymentTerminalDeviceRequest** 要求はノーオーペレーションである必要があり、すぐに返す必要があります。</span><span class="sxs-lookup"><span data-stu-id="84378-351">If the payment terminal handles the authorize and capture requests in a single call, the **CapturePaymentTerminalDeviceRequest** request should be a no-op and should immediately return.</span></span>

<span data-ttu-id="84378-352">支払端末が、キャプチャ呼び出しを処理する許可要求からの状態を必要とする場合、プロパティは、先に説明した **AuthorizePaymentTerminalDeviceResponse** 要求の **PaymentSdkData** オブジェクトに格納され、 **CapturePaymentTerminalDeviceRequest** 要求の **paymentPropertiesXml** 変数を渡します。</span><span class="sxs-lookup"><span data-stu-id="84378-352">If the payment terminal requires state from the authorize requests to handle the capture call, the properties should be stored in the **PaymentSdkData** object of the **AuthorizePaymentTerminalDeviceResponse** request that is described earlier, and passed through the **paymentPropertiesXml** variable of the **CapturePaymentTerminalDeviceRequest** request.</span></span>

##### <a name="voidpaymentterminaldevicerequest"></a><span data-ttu-id="84378-353">VoidPaymentTerminalDeviceRequest</span><span class="sxs-lookup"><span data-stu-id="84378-353">VoidPaymentTerminalDeviceRequest</span></span>
###### <a name="signature"></a><span data-ttu-id="84378-354">署名</span><span class="sxs-lookup"><span data-stu-id="84378-354">Signature</span></span>
``` csharp
public VoidPaymentTerminalDeviceRequest(string token, string paymentConnectorName, decimal amount, string currency, TenderInfo tenderInfo, string paymentPropertiesXml, ExtensionTransaction extensionTransactionProperties)
```

###### <a name="variables"></a><span data-ttu-id="84378-355">変数</span><span class="sxs-lookup"><span data-stu-id="84378-355">Variables</span></span>

| <span data-ttu-id="84378-356">変動</span><span class="sxs-lookup"><span data-stu-id="84378-356">Variable</span></span> | <span data-ttu-id="84378-357">説明</span><span class="sxs-lookup"><span data-stu-id="84378-357">Description</span></span> |
|---|---|
| <span data-ttu-id="84378-358">token</span><span class="sxs-lookup"><span data-stu-id="84378-358">token</span></span> | <span data-ttu-id="84378-359">支払い端末が最初のトランザクションのためにロックされたときに生成される一意のトークン値。</span><span class="sxs-lookup"><span data-stu-id="84378-359">The unique token value that is generated when the payment terminal is initially locked for the transaction.</span></span> |
| <span data-ttu-id="84378-360">paymentConnectorName</span><span class="sxs-lookup"><span data-stu-id="84378-360">paymentConnectorName</span></span> | <span data-ttu-id="84378-361">支払フローの一部として使用される支払コネクタの名前。</span><span class="sxs-lookup"><span data-stu-id="84378-361">The name of the payment connector that is used as part of the payment flow.</span></span> <span data-ttu-id="84378-362">この変数は、**IPaymentProcessor** インターフェイスを使用する支払フローとの統合がある場合に使用されます。</span><span class="sxs-lookup"><span data-stu-id="84378-362">This variable is used if there is an integration with payment flows that use the **IPaymentProcessor** interface.</span></span> |
| <span data-ttu-id="84378-363">金額</span><span class="sxs-lookup"><span data-stu-id="84378-363">amount</span></span> | <span data-ttu-id="84378-364">支払いが無効になる金額。</span><span class="sxs-lookup"><span data-stu-id="84378-364">The amount for the payment to void.</span></span> |
| <span data-ttu-id="84378-365">通貨</span><span class="sxs-lookup"><span data-stu-id="84378-365">currency</span></span> | <span data-ttu-id="84378-366">支払いが無効になる通貨。</span><span class="sxs-lookup"><span data-stu-id="84378-366">The currency for the payment to void.</span></span> |
| <span data-ttu-id="84378-367">tenderInfo</span><span class="sxs-lookup"><span data-stu-id="84378-367">tenderInfo</span></span> | <span data-ttu-id="84378-368">外部ソースから取得された POS から送信されるカード情報 (外部ソースがある場合)。</span><span class="sxs-lookup"><span data-stu-id="84378-368">The card information that is sent from the POS that is retrieved from an external source (if an external source is present).</span></span> |
| <span data-ttu-id="84378-369">paymentPropertiesXml</span><span class="sxs-lookup"><span data-stu-id="84378-369">paymentPropertiesXml</span></span> | <span data-ttu-id="84378-370">**AuthorizePaymentTerminalDeviceRequest** 要求または **RefundPaymentTerminalDeviceRequest** 要求によって返され、要求間のステートフル プロパティをサポートするために使用される **PaymentSdkData** オブジェクトのコンテンツ。</span><span class="sxs-lookup"><span data-stu-id="84378-370">The content of the **PaymentSdkData** object that is returned by the **AuthorizePaymentTerminalDeviceRequest** or **RefundPaymentTerminalDeviceRequest** request, and that is used to support stateful properties between the requests.</span></span> |
| <span data-ttu-id="84378-371">extensionTransactionProperties</span><span class="sxs-lookup"><span data-stu-id="84378-371">extensionTransactionProperties</span></span> | <span data-ttu-id="84378-372">名前/値のペアの形式の拡張構成プロパティのセット。</span><span class="sxs-lookup"><span data-stu-id="84378-372">The set of extension configuration properties in the form of name/value pairs.</span></span> |

##### <a name="refundpaymentterminaldevicerequest"></a><span data-ttu-id="84378-373">RefundPaymentTerminalDeviceRequest</span><span class="sxs-lookup"><span data-stu-id="84378-373">RefundPaymentTerminalDeviceRequest</span></span>
###### <a name="signature"></a><span data-ttu-id="84378-374">署名</span><span class="sxs-lookup"><span data-stu-id="84378-374">Signature</span></span>
``` csharp
public RefundPaymentTerminalDeviceRequest(string token, string paymentConnectorName, TenderInfo tenderInfo, decimal amount, string currency, bool isManualEntry, ExtensionTransaction extensionTransactionProperties)
```

###### <a name="variables"></a><span data-ttu-id="84378-375">変数</span><span class="sxs-lookup"><span data-stu-id="84378-375">Variables</span></span>

| <span data-ttu-id="84378-376">変動</span><span class="sxs-lookup"><span data-stu-id="84378-376">Variable</span></span> | <span data-ttu-id="84378-377">説明</span><span class="sxs-lookup"><span data-stu-id="84378-377">Description</span></span> |
|---|---|
| <span data-ttu-id="84378-378">token</span><span class="sxs-lookup"><span data-stu-id="84378-378">token</span></span> | <span data-ttu-id="84378-379">支払い端末が最初のトランザクションのためにロックされたときに生成される一意のトークン値。</span><span class="sxs-lookup"><span data-stu-id="84378-379">The unique token value that is generated when the payment terminal is initially locked for the transaction.</span></span> |
| <span data-ttu-id="84378-380">paymentConnectorName</span><span class="sxs-lookup"><span data-stu-id="84378-380">paymentConnectorName</span></span> | <span data-ttu-id="84378-381">支払フローの一部として使用される支払コネクタの名前。</span><span class="sxs-lookup"><span data-stu-id="84378-381">The name of the payment connector that is used as part of the payment flow.</span></span> <span data-ttu-id="84378-382">この変数は、**IPaymentProcessor** インターフェイスを使用する支払フローとの統合がある場合に使用されます。</span><span class="sxs-lookup"><span data-stu-id="84378-382">This variable is used if there is an integration with payment flows that use the **IPaymentProcessor** interface.</span></span> |
| <span data-ttu-id="84378-383">tenderInfo</span><span class="sxs-lookup"><span data-stu-id="84378-383">tenderInfo</span></span> | <span data-ttu-id="84378-384">外部ソースから取得された POS から送信されるカード情報 (外部ソースがある場合)。</span><span class="sxs-lookup"><span data-stu-id="84378-384">The card information that is sent from the POS that is retrieved from an external source (if an external source is present).</span></span> |
| <span data-ttu-id="84378-385">金額</span><span class="sxs-lookup"><span data-stu-id="84378-385">amount</span></span> | <span data-ttu-id="84378-386">払い戻す金額。</span><span class="sxs-lookup"><span data-stu-id="84378-386">The amount to refund.</span></span> |
| <span data-ttu-id="84378-387">通貨</span><span class="sxs-lookup"><span data-stu-id="84378-387">currency</span></span> | <span data-ttu-id="84378-388">払い戻す金額の通貨。</span><span class="sxs-lookup"><span data-stu-id="84378-388">The currency for the amount to refund.</span></span> |
| <span data-ttu-id="84378-389">isManualEntry</span><span class="sxs-lookup"><span data-stu-id="84378-389">isManualEntry</span></span> | <span data-ttu-id="84378-390">カード番号を手動で入力されたかどうかを定義する値。</span><span class="sxs-lookup"><span data-stu-id="84378-390">A value that defines whether the card number was entered manually.</span></span> |
| <span data-ttu-id="84378-391">extensionTransactionProperties</span><span class="sxs-lookup"><span data-stu-id="84378-391">extensionTransactionProperties</span></span> | <span data-ttu-id="84378-392">名前/値のペアの形式の拡張構成プロパティのセット。</span><span class="sxs-lookup"><span data-stu-id="84378-392">The set of extension configuration properties in the form of name/value pairs.</span></span> |

##### <a name="fetchtokenpaymentterminaldevicerequest"></a><span data-ttu-id="84378-393">FetchTokenPaymentTerminalDeviceRequest</span><span class="sxs-lookup"><span data-stu-id="84378-393">FetchTokenPaymentTerminalDeviceRequest</span></span>
###### <a name="signature"></a><span data-ttu-id="84378-394">署名</span><span class="sxs-lookup"><span data-stu-id="84378-394">Signature</span></span>
``` csharp
public FetchTokenPaymentTerminalDeviceRequest(string token, bool isManualEntry, ExtensionTransaction extensionTransactionProperties)
```

###### <a name="variables"></a><span data-ttu-id="84378-395">変数</span><span class="sxs-lookup"><span data-stu-id="84378-395">Variables</span></span>

| <span data-ttu-id="84378-396">変動</span><span class="sxs-lookup"><span data-stu-id="84378-396">Variable</span></span> | <span data-ttu-id="84378-397">説明</span><span class="sxs-lookup"><span data-stu-id="84378-397">Description</span></span> |
|---|---|
| <span data-ttu-id="84378-398">token</span><span class="sxs-lookup"><span data-stu-id="84378-398">token</span></span> | <span data-ttu-id="84378-399">支払い端末が最初のトランザクションのためにロックされたときに生成される一意のトークン値。</span><span class="sxs-lookup"><span data-stu-id="84378-399">The unique token value that is generated when the payment terminal is initially locked for the transaction.</span></span> |
| <span data-ttu-id="84378-400">isManualEntry</span><span class="sxs-lookup"><span data-stu-id="84378-400">isManualEntry</span></span> | <span data-ttu-id="84378-401">カード番号を手動で入力されたかどうかを定義する値。</span><span class="sxs-lookup"><span data-stu-id="84378-401">A value that defines whether the card number was entered manually.</span></span> |
| <span data-ttu-id="84378-402">extensionTransactionProperties</span><span class="sxs-lookup"><span data-stu-id="84378-402">extensionTransactionProperties</span></span> | <span data-ttu-id="84378-403">名前/値のペアの形式の拡張構成プロパティのセット。</span><span class="sxs-lookup"><span data-stu-id="84378-403">The set of extension configuration properties in the form of name/value pairs.</span></span> |

##### <a name="endtransactionpaymentterminaldevicerequest"></a><span data-ttu-id="84378-404">EndTransactionPaymentTerminalDeviceRequest</span><span class="sxs-lookup"><span data-stu-id="84378-404">EndTransactionPaymentTerminalDeviceRequest</span></span>
##### <a name="signature"></a><span data-ttu-id="84378-405">署名</span><span class="sxs-lookup"><span data-stu-id="84378-405">Signature</span></span>
``` csharp
public EndTransactionPaymentTerminalDeviceRequest(string token, ExtensionTransaction extensionTransactionProperties)
```

###### <a name="variables"></a><span data-ttu-id="84378-406">変数</span><span class="sxs-lookup"><span data-stu-id="84378-406">Variables</span></span>

| <span data-ttu-id="84378-407">変動</span><span class="sxs-lookup"><span data-stu-id="84378-407">Variable</span></span> | <span data-ttu-id="84378-408">説明</span><span class="sxs-lookup"><span data-stu-id="84378-408">Description</span></span> |
|---|---|
| <span data-ttu-id="84378-409">token</span><span class="sxs-lookup"><span data-stu-id="84378-409">token</span></span> | <span data-ttu-id="84378-410">支払い端末が最初のトランザクションのためにロックされたときに生成される一意のトークン値。</span><span class="sxs-lookup"><span data-stu-id="84378-410">The unique token value that is generated when the payment terminal is initially locked for the transaction.</span></span> |
| <span data-ttu-id="84378-411">extensionTransactionProperties</span><span class="sxs-lookup"><span data-stu-id="84378-411">extensionTransactionProperties</span></span> | <span data-ttu-id="84378-412">名前/値のペアの形式の拡張構成プロパティのセット。</span><span class="sxs-lookup"><span data-stu-id="84378-412">The set of extension configuration properties in the form of name/value pairs.</span></span> |

##### <a name="closepaymentterminaldevicerequest"></a><span data-ttu-id="84378-413">ClosePaymentTerminalDeviceRequest</span><span class="sxs-lookup"><span data-stu-id="84378-413">ClosePaymentTerminalDeviceRequest</span></span>
###### <a name="signature"></a><span data-ttu-id="84378-414">署名</span><span class="sxs-lookup"><span data-stu-id="84378-414">Signature</span></span>
``` csharp
public ClosePaymentTerminalDeviceRequest(string token, ExtensionTransaction extensionTransactionProperties)
```

###### <a name="variables"></a><span data-ttu-id="84378-415">変数</span><span class="sxs-lookup"><span data-stu-id="84378-415">Variables</span></span>

| <span data-ttu-id="84378-416">変動</span><span class="sxs-lookup"><span data-stu-id="84378-416">Variable</span></span> | <span data-ttu-id="84378-417">説明</span><span class="sxs-lookup"><span data-stu-id="84378-417">Description</span></span> |
|---|---|
| <span data-ttu-id="84378-418">token</span><span class="sxs-lookup"><span data-stu-id="84378-418">token</span></span> | <span data-ttu-id="84378-419">支払い端末が最初のトランザクションのためにロックされたときに生成される一意のトークン値。</span><span class="sxs-lookup"><span data-stu-id="84378-419">The unique token value that is generated when the payment terminal is initially locked for the transaction.</span></span> |
| <span data-ttu-id="84378-420">extensionTransactionProperties</span><span class="sxs-lookup"><span data-stu-id="84378-420">extensionTransactionProperties</span></span> | <span data-ttu-id="84378-421">名前/値のペアの形式の拡張構成プロパティのセット。</span><span class="sxs-lookup"><span data-stu-id="84378-421">The set of extension configuration properties in the form of name/value pairs.</span></span> |

##### <a name="activategiftcardpaymentterminalrequest"></a><span data-ttu-id="84378-422">ActivateGiftCardPaymentTerminalRequest</span><span class="sxs-lookup"><span data-stu-id="84378-422">ActivateGiftCardPaymentTerminalRequest</span></span>
###### <a name="signature"></a><span data-ttu-id="84378-423">署名</span><span class="sxs-lookup"><span data-stu-id="84378-423">Signature</span></span>
``` csharp
public ActivateGiftCardPaymentTerminalRequest(string token, string paymentConnectorName, decimal amount, string currencyCode, TenderInfo tenderInfo, ExtensionTransaction extensionTransactionProperties)
```

###### <a name="variables"></a><span data-ttu-id="84378-424">変数</span><span class="sxs-lookup"><span data-stu-id="84378-424">Variables</span></span>

| <span data-ttu-id="84378-425">変動</span><span class="sxs-lookup"><span data-stu-id="84378-425">Variable</span></span> | <span data-ttu-id="84378-426">説明</span><span class="sxs-lookup"><span data-stu-id="84378-426">Description</span></span> |
|---|---|
| <span data-ttu-id="84378-427">token</span><span class="sxs-lookup"><span data-stu-id="84378-427">token</span></span> | <span data-ttu-id="84378-428">支払い端末が最初のトランザクションのためにロックされたときに生成される一意のトークン値。</span><span class="sxs-lookup"><span data-stu-id="84378-428">The unique token value that is generated when the payment terminal is initially locked for the transaction.</span></span> |
| <span data-ttu-id="84378-429">paymentConnectorName</span><span class="sxs-lookup"><span data-stu-id="84378-429">paymentConnectorName</span></span> | <span data-ttu-id="84378-430">支払フローの一部として使用される支払コネクタの名前。</span><span class="sxs-lookup"><span data-stu-id="84378-430">The name of the payment connector that is used as part of the payment flow.</span></span> <span data-ttu-id="84378-431">この変数は、**IPaymentProcessor** インターフェイスを使用する支払フローとの統合がある場合に使用されます。</span><span class="sxs-lookup"><span data-stu-id="84378-431">This variable is used if there is an integration with payment flows that use the **IPaymentProcessor** interface.</span></span> |
| <span data-ttu-id="84378-432">金額</span><span class="sxs-lookup"><span data-stu-id="84378-432">amount</span></span> | <span data-ttu-id="84378-433">有効化中にギフト カードに追加する初期金額。</span><span class="sxs-lookup"><span data-stu-id="84378-433">The initial amount to add to the gift card during activation.</span></span> |
| <span data-ttu-id="84378-434">通貨</span><span class="sxs-lookup"><span data-stu-id="84378-434">currency</span></span> | <span data-ttu-id="84378-435">有効化中にギフト カードに追加する初期金額の通貨。</span><span class="sxs-lookup"><span data-stu-id="84378-435">The currency for the initial amount to add to the gift card during activation.</span></span> |
| <span data-ttu-id="84378-436">tenderInfo</span><span class="sxs-lookup"><span data-stu-id="84378-436">tenderInfo</span></span> | <span data-ttu-id="84378-437">外部ソースから取得された POS から送信されるカード情報 (外部ソースがある場合)。</span><span class="sxs-lookup"><span data-stu-id="84378-437">The card information that is sent from the POS that is retrieved from an external source (if an external source is present).</span></span> |
| <span data-ttu-id="84378-438">extensionTransactionProperties</span><span class="sxs-lookup"><span data-stu-id="84378-438">extensionTransactionProperties</span></span> | <span data-ttu-id="84378-439">名前/値のペアの形式の拡張構成プロパティのセット。</span><span class="sxs-lookup"><span data-stu-id="84378-439">The set of extension configuration properties in the form of name/value pairs.</span></span> |

##### <a name="addbalancetogiftcardpaymentterminalrequest"></a><span data-ttu-id="84378-440">AddBalanceToGiftCardPaymentTerminalRequest</span><span class="sxs-lookup"><span data-stu-id="84378-440">AddBalanceToGiftCardPaymentTerminalRequest</span></span>
###### <a name="signature"></a><span data-ttu-id="84378-441">署名</span><span class="sxs-lookup"><span data-stu-id="84378-441">Signature</span></span>
``` csharp
public AddBalanceToGiftCardPaymentTerminalRequest(string token, string paymentConnectorName, decimal amount, string currencyCode, TenderInfo tenderInfo, ExtensionTransaction extensionTransactionProperties)
```

###### <a name="variables"></a><span data-ttu-id="84378-442">変数</span><span class="sxs-lookup"><span data-stu-id="84378-442">Variables</span></span>

| <span data-ttu-id="84378-443">変動</span><span class="sxs-lookup"><span data-stu-id="84378-443">Variable</span></span> | <span data-ttu-id="84378-444">説明</span><span class="sxs-lookup"><span data-stu-id="84378-444">Description</span></span> |
|---|---|
| <span data-ttu-id="84378-445">token</span><span class="sxs-lookup"><span data-stu-id="84378-445">token</span></span> | <span data-ttu-id="84378-446">支払い端末が最初のトランザクションのためにロックされたときに生成される一意のトークン値。</span><span class="sxs-lookup"><span data-stu-id="84378-446">The unique token value that is generated when the payment terminal is initially locked for the transaction.</span></span> |
| <span data-ttu-id="84378-447">paymentConnectorName</span><span class="sxs-lookup"><span data-stu-id="84378-447">paymentConnectorName</span></span> | <span data-ttu-id="84378-448">支払フローの一部として使用される支払コネクタの名前。</span><span class="sxs-lookup"><span data-stu-id="84378-448">The name of the payment connector that is used as part of the payment flow.</span></span> <span data-ttu-id="84378-449">この変数は、**IPaymentProcessor** インターフェイスを使用する支払フローとの統合がある場合に使用されます。</span><span class="sxs-lookup"><span data-stu-id="84378-449">This variable is used if there is an integration with payment flows that use the **IPaymentProcessor** interface.</span></span> |
| <span data-ttu-id="84378-450">金額</span><span class="sxs-lookup"><span data-stu-id="84378-450">amount</span></span> | <span data-ttu-id="84378-451">ギフト カードに追加される金額。</span><span class="sxs-lookup"><span data-stu-id="84378-451">The amount to add to the gift card.</span></span> |
| <span data-ttu-id="84378-452">通貨</span><span class="sxs-lookup"><span data-stu-id="84378-452">currency</span></span> | <span data-ttu-id="84378-453">ギフト カード残高に追加する金額の通貨。</span><span class="sxs-lookup"><span data-stu-id="84378-453">The currency for the amount to add to the gift card balance.</span></span> |
| <span data-ttu-id="84378-454">tenderInfo</span><span class="sxs-lookup"><span data-stu-id="84378-454">tenderInfo</span></span> | <span data-ttu-id="84378-455">外部ソースから取得された POS から送信されるカード情報 (外部ソースがある場合)。</span><span class="sxs-lookup"><span data-stu-id="84378-455">The card information that is sent from the POS that is retrieved from an external source (if an external source present).</span></span> |
| <span data-ttu-id="84378-456">extensionTransactionProperties</span><span class="sxs-lookup"><span data-stu-id="84378-456">extensionTransactionProperties</span></span> | <span data-ttu-id="84378-457">名前/値のペアの形式の拡張構成プロパティのセット。</span><span class="sxs-lookup"><span data-stu-id="84378-457">The set of extension configuration properties in the form of name/value pairs.</span></span> |

##### <a name="getgiftcardbalancepaymentterminalrequest"></a><span data-ttu-id="84378-458">GetGiftCardBalancePaymentTerminalRequest</span><span class="sxs-lookup"><span data-stu-id="84378-458">GetGiftCardBalancePaymentTerminalRequest</span></span>
###### <a name="signature"></a><span data-ttu-id="84378-459">署名</span><span class="sxs-lookup"><span data-stu-id="84378-459">Signature</span></span>
``` csharp
public GetGiftCardBalancePaymentTerminalRequest(string token, string paymentConnectorName, string currencyCode, TenderInfo tenderInfo, ExtensionTransaction extensionTransactionProperties)
```

###### <a name="variables"></a><span data-ttu-id="84378-460">変数</span><span class="sxs-lookup"><span data-stu-id="84378-460">Variables</span></span>

| <span data-ttu-id="84378-461">変動</span><span class="sxs-lookup"><span data-stu-id="84378-461">Variable</span></span> | <span data-ttu-id="84378-462">説明</span><span class="sxs-lookup"><span data-stu-id="84378-462">Description</span></span> |
|---|---|
| <span data-ttu-id="84378-463">token</span><span class="sxs-lookup"><span data-stu-id="84378-463">token</span></span> | <span data-ttu-id="84378-464">支払い端末が最初のトランザクションのためにロックされたときに生成される一意のトークン値。</span><span class="sxs-lookup"><span data-stu-id="84378-464">The unique token value that is generated when the payment terminal is initially locked for the transaction.</span></span> |
| <span data-ttu-id="84378-465">paymentConnectorName</span><span class="sxs-lookup"><span data-stu-id="84378-465">paymentConnectorName</span></span> | <span data-ttu-id="84378-466">支払フローの一部として使用される支払コネクタの名前。</span><span class="sxs-lookup"><span data-stu-id="84378-466">The name of the payment connector that is used as part of the payment flow.</span></span> <span data-ttu-id="84378-467">この変数は、**IPaymentProcessor** インターフェイスを使用する支払フローとの統合がある場合に使用されます。</span><span class="sxs-lookup"><span data-stu-id="84378-467">This variable is used if there is an integration with payment flows that use the **IPaymentProcessor** interface.</span></span> |
| <span data-ttu-id="84378-468">通貨</span><span class="sxs-lookup"><span data-stu-id="84378-468">currency</span></span> | <span data-ttu-id="84378-469">ギフト カード残高を取得するための通貨。</span><span class="sxs-lookup"><span data-stu-id="84378-469">The currency to retrieve the gift card balance in.</span></span> |
| <span data-ttu-id="84378-470">tenderInfo</span><span class="sxs-lookup"><span data-stu-id="84378-470">tenderInfo</span></span> | <span data-ttu-id="84378-471">外部ソースから取得された POS から送信されるカード情報 (外部ソースがある場合)。</span><span class="sxs-lookup"><span data-stu-id="84378-471">The card information that is sent from the POS that is retrieved from an external source (if an external source present).</span></span> |
| <span data-ttu-id="84378-472">extensionTransactionProperties</span><span class="sxs-lookup"><span data-stu-id="84378-472">extensionTransactionProperties</span></span> | <span data-ttu-id="84378-473">名前/値のペアの形式の拡張構成プロパティのセット。</span><span class="sxs-lookup"><span data-stu-id="84378-473">The set of extension configuration properties in the form of name/value pairs.</span></span> |

##### <a name="getprivatetenderpaymentterminaldevicerequest"></a><span data-ttu-id="84378-474">GetPrivateTenderPaymentTerminalDeviceRequest</span><span class="sxs-lookup"><span data-stu-id="84378-474">GetPrivateTenderPaymentTerminalDeviceRequest</span></span>
###### <a name="signature"></a><span data-ttu-id="84378-475">署名</span><span class="sxs-lookup"><span data-stu-id="84378-475">Signature</span></span>
``` csharp
public GetPrivateTenderPaymentTerminalDeviceRequest(string token, decimal amount, bool declined, bool isSwipe, ExtensionTransaction extensionTransactionProperties)
```

###### <a name="variables"></a><span data-ttu-id="84378-476">変数</span><span class="sxs-lookup"><span data-stu-id="84378-476">Variables</span></span>

| <span data-ttu-id="84378-477">変動</span><span class="sxs-lookup"><span data-stu-id="84378-477">Variable</span></span> | <span data-ttu-id="84378-478">説明</span><span class="sxs-lookup"><span data-stu-id="84378-478">Description</span></span> |
|---|---|
| <span data-ttu-id="84378-479">token</span><span class="sxs-lookup"><span data-stu-id="84378-479">token</span></span> | <span data-ttu-id="84378-480">支払い端末が最初のトランザクションのためにロックされたときに生成される一意のトークン値。</span><span class="sxs-lookup"><span data-stu-id="84378-480">The unique token value that is generated when the payment terminal is initially locked for the transaction.</span></span> |
| <span data-ttu-id="84378-481">金額</span><span class="sxs-lookup"><span data-stu-id="84378-481">amount</span></span> | <span data-ttu-id="84378-482">POS に設定された金額。</span><span class="sxs-lookup"><span data-stu-id="84378-482">The amount that is set on the POS.</span></span> <span data-ttu-id="84378-483">(通常、この変数は、カード番号を取得したときに支払ターミナルの金額を表示するために使用されます。)</span><span class="sxs-lookup"><span data-stu-id="84378-483">(Typically, this variable is used to show the amount on the payment terminal when the card number is retrieved.)</span></span> |
| <span data-ttu-id="84378-484">declined</span><span class="sxs-lookup"><span data-stu-id="84378-484">declined</span></span> | <span data-ttu-id="84378-485">この値は廃止されています。</span><span class="sxs-lookup"><span data-stu-id="84378-485">This variable is obsolete.</span></span> |
| <span data-ttu-id="84378-486">isSwipe</span><span class="sxs-lookup"><span data-stu-id="84378-486">isSwipe</span></span> | <span data-ttu-id="84378-487">支払ターミナルで読み取りまたは手動入力によってカード番号を取得する必要があるかどうかを決定する値。</span><span class="sxs-lookup"><span data-stu-id="84378-487">A value that determines whether the card number should be retrieved through a swipe or manual entry on the payment terminal.</span></span> |
| <span data-ttu-id="84378-488">extensionTransactionProperties</span><span class="sxs-lookup"><span data-stu-id="84378-488">extensionTransactionProperties</span></span> | <span data-ttu-id="84378-489">名前/値のペアの形式の拡張構成プロパティのセット。</span><span class="sxs-lookup"><span data-stu-id="84378-489">The set of extension configuration properties in the form of name/value pairs.</span></span> |

##### <a name="executetaskpaymentterminaldevicerequest"></a><span data-ttu-id="84378-490">ExecuteTaskPaymentTerminalDeviceRequest</span><span class="sxs-lookup"><span data-stu-id="84378-490">ExecuteTaskPaymentTerminalDeviceRequest</span></span>
###### <a name="signature"></a><span data-ttu-id="84378-491">署名</span><span class="sxs-lookup"><span data-stu-id="84378-491">Signature</span></span>
``` csharp
public ExecuteTaskPaymentTerminalDeviceRequest(string token, string task, ExtensionTransaction extensionTransactionProperties)
```

###### <a name="variables"></a><span data-ttu-id="84378-492">変数</span><span class="sxs-lookup"><span data-stu-id="84378-492">Variables</span></span>

| <span data-ttu-id="84378-493">変動</span><span class="sxs-lookup"><span data-stu-id="84378-493">Variable</span></span> | <span data-ttu-id="84378-494">説明</span><span class="sxs-lookup"><span data-stu-id="84378-494">Description</span></span> |
|---|---|
| <span data-ttu-id="84378-495">token</span><span class="sxs-lookup"><span data-stu-id="84378-495">token</span></span> | <span data-ttu-id="84378-496">支払い端末が最初のトランザクションのためにロックされたときに生成される一意のトークン値。</span><span class="sxs-lookup"><span data-stu-id="84378-496">The unique token value that is generated when the payment terminal is initially locked for the transaction.</span></span> |
| <span data-ttu-id="84378-497">タスク</span><span class="sxs-lookup"><span data-stu-id="84378-497">task</span></span> | <span data-ttu-id="84378-498">実行されているタスクの一意の識別子。</span><span class="sxs-lookup"><span data-stu-id="84378-498">The unique identifier for the task that is being run.</span></span> |
| <span data-ttu-id="84378-499">extensionTransactionProperties</span><span class="sxs-lookup"><span data-stu-id="84378-499">extensionTransactionProperties</span></span> | <span data-ttu-id="84378-500">名前/値のペアの形式の拡張構成プロパティのセット。</span><span class="sxs-lookup"><span data-stu-id="84378-500">The set of extension configuration properties in the form of name/value pairs.</span></span> |

#### <a name="state-in-the-payment-connector"></a><span data-ttu-id="84378-501">支払コネクタの状態</span><span class="sxs-lookup"><span data-stu-id="84378-501">State in the payment connector</span></span>
<span data-ttu-id="84378-502">支払いコネクターは、POS 内のインプロセス ハードウェア ステーションを通じてホストされているとき、dllhost.exe プロセスの一部としてホストすることができます。</span><span class="sxs-lookup"><span data-stu-id="84378-502">The payment connector can be hosted as part of the dllhost.exe process when it's hosted through the in-process Hardware Station inside the POS.</span></span> <span data-ttu-id="84378-503">または、 Microsoft Internet Information Services (IIS) に基づくハードウェア ステーションでホストされている場合、w3wp.exe プロセスとして支払コネクタをホストすることができます。</span><span class="sxs-lookup"><span data-stu-id="84378-503">Alternatively, the payment connector can be hosted as a w3wp.exe process when it's hosted in the Hardware Station that is based on Microsoft Internet Information Services (IIS).</span></span> <span data-ttu-id="84378-504">状況によっては、支払フローの間または最中に両方のプロセスを終了したり、応答を停止したりできます。</span><span class="sxs-lookup"><span data-stu-id="84378-504">In some circumstances, both processes can be terminated or stop responding between or during payment flows.</span></span> <span data-ttu-id="84378-505">したがって、支払コネクタには状態依存性がなく、以前に説明した支払フロー関連の要求のいずれかの時点で終了すると回復することができるようにすることをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="84378-505">Therefore, we recommend that payment connectors not have state dependencies, and that they be able to recover if they are terminated at any point during the payment flow–related requests that are described earlier.</span></span>

### <a name="configure-the-payment-connector-in-the-hardware-station-config"></a><span data-ttu-id="84378-506">ハードウェア ステーションのコンフィギュレーションで支払コネクタをコンフィギュレーションする</span><span class="sxs-lookup"><span data-stu-id="84378-506">Configure the payment connector in the Hardware Station config</span></span>
<span data-ttu-id="84378-507">ハードウェア ステーションが支払コネクタを読み込むようにするために、対応するアセンブリ参照を **HardwareStation.Extension.config** ファイルに設定する必要があります。このファイルは Retail SDK の **Assets** フォルダーにあります。</span><span class="sxs-lookup"><span data-stu-id="84378-507">To help guarantee that the Hardware Station loads the payment connector, you must set the corresponding assembly reference in the **HardwareStation.Extension.config** file that is located in the **Assets** folder in the Retail SDK.</span></span>

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

### <a name="configure-the-payment-connector-on-the-pos-hardware-profile-page-in-the-finance-and-operations-client"></a><span data-ttu-id="84378-508">Finance and Operations クライアントの POS ハードウェア プロファイル ページで支払コネクタをコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="84378-508">Configure the payment connector on the POS hardware profile page in the Finance and Operations client</span></span>
<span data-ttu-id="84378-509">POS にロードする正しい支払コネクタを決定するには、次の図に示すように、Finance and Operations クライアントの **POSハードウェア プロファイル** ページの **PINパッド** FastTab で、**デバイス名** フィールドの **PaymentTerminalDevice** プロパティの値を設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="84378-509">To determine the correct payment connector that should be loaded on the POS, you must set the value of the **PaymentTerminalDevice** property in the **Device name** field on the **PIN pad** FastTab of the **POS hardware profile** page in the Finance and Operations client, as shown in the following illustration.</span></span>

![Finance and Operations クライアントの POS ハードウェア プロファイル ページで支払コネクタをコンフィギュレーション](media/PAYMENTS/PAYMENT-TERMINAL/SamplePaymentDeviceConfigurInAx.jpg)

## <a name="write-a-payment-processor"></a><span data-ttu-id="84378-511">支払プロセッサの記述</span><span class="sxs-lookup"><span data-stu-id="84378-511">Write a payment processor</span></span>
<span data-ttu-id="84378-512">通常は、支払ゲートウェイへの直接接続が確立された場合にのみ、支払プロセスが使用されます。</span><span class="sxs-lookup"><span data-stu-id="84378-512">Payment processes are usually used only if a direct connection to a payment gateway is established.</span></span> <span data-ttu-id="84378-513">このシナリオは、カードが存在しない販売取引またはより複雑なカードが存在するシナリオで最も頻繁に発生します。</span><span class="sxs-lookup"><span data-stu-id="84378-513">This scenario most often occurs in card-not-present sales transactions or more complex card-present scenarios.</span></span> <span data-ttu-id="84378-514">また、支払プロセッサは、Finance and Operations クライアントの **POS ハードウェア プロファイル** ページを使用してコンフィギュレーションされている商社プロパティを処理するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="84378-514">Additionally, the payment processor is used to process the merchant properties that are configured through the **POS hardware profile** page in the Finance and Operations client.</span></span>

> [!NOTE]
> <span data-ttu-id="84378-515">支払プロセッサは、支払要求がすべて支払ターミナルを使用して直接処理され、商社プロパティを POS を使用して設定する必要がない場合でも、現在のところは必要です。</span><span class="sxs-lookup"><span data-stu-id="84378-515">The payment processor is currently required, even if all payment requests are handled directly through the payment terminal and no merchant properties must be set through the POS.</span></span>

### <a name="understanding-the-merchant-properties-flows"></a><span data-ttu-id="84378-516">商社プロパティ フローを理解する</span><span class="sxs-lookup"><span data-stu-id="84378-516">Understanding the merchant properties flows</span></span>
<span data-ttu-id="84378-517">次のセクションでは、Finance and Operations クライアントの **POS ハードウェア プロファイル** ページでの商社プロパティの設定方法と、POS での支払フロー中に支払コネクタにこれらのプロパティを渡す方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="84378-517">The following sections describe how the merchant properties are set on the **POS hardware profile** page in the Finance and Operations client, and how they are passed to the payment connector during payment flows on the POS.</span></span>

#### <a name="set-merchant-properties-on-the-pos-hardware-profile-page-in-the-finance-and-operations-client"></a><span data-ttu-id="84378-518">Finance and Operations クライアントの POS ハードウェア プロファイル ページで商社プロパティを設定</span><span class="sxs-lookup"><span data-stu-id="84378-518">Set merchant properties on the POS hardware profile page in the Finance and Operations client</span></span>
<span data-ttu-id="84378-519">次の図は、Finance and Operations クライアントの **POS ハードウェア プロファイル** ページで商社プロパティを設定する方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="84378-519">The following illustration shows how the merchant properties are set through the **POS hardware profile** page in the Finance and Operations client.</span></span> <span data-ttu-id="84378-520">マーチャントプロパティを設定するには、**IPaymentProcessor** ライブラリで定義されている **Microsoft.Dynamics.Retail.PaymentSDK** インターフェイスを実装する必要があります。</span><span class="sxs-lookup"><span data-stu-id="84378-520">To enable the merchant properties to be set, the **IPaymentProcessor** interface that is defined in the **Microsoft.Dynamics.Retail.PaymentSDK** library must be implemented.</span></span> <span data-ttu-id="84378-521">**GetMerchantAccountPropertyMetadata** と **ValidateMerchantAccount** の 2 つのインターフェイス メソッドが必要です。</span><span class="sxs-lookup"><span data-stu-id="84378-521">Two interface methods are required: **GetMerchantAccountPropertyMetadata** and **ValidateMerchantAccount**.</span></span>

![Finance and Operations クライアントの POS ハードウェア プロファイル ページで商社プロパティを設定](media/PAYMENTS/PAYMENT-TERMINAL/MerchantPropertiesAXFlow.jpg)

#### <a name="set-merchant-properties-on-payment-connector-during-pos-sales-transaction"></a><span data-ttu-id="84378-523">POS 販売トランザクションの間に支払コネクタで商社プロパティを設定</span><span class="sxs-lookup"><span data-stu-id="84378-523">Set merchant properties on payment connector during POS sales transaction</span></span>
<span data-ttu-id="84378-524">次の図は、**BeginTransactionPaymentTerminalDeviceRequest** 要求の間に Retail サーバーを介して Finance and Operations データベースから商社プロパティを取得して支払コネクタに渡す仕組みを示しています。</span><span class="sxs-lookup"><span data-stu-id="84378-524">The following illustration shows how the merchant properties are retrieved from the Finance and Operations database through the Retail Server and passed to the payment connector during the **BeginTransactionPaymentTerminalDeviceRequest** request.</span></span>

![POS 支払フロー時に支払コネクタに商社プロパティを設定](media/PAYMENTS/PAYMENT-TERMINAL/MerchantPropertiesPOSFlow.jpg)

### <a name="implement-the-ipaymentprocessor-interface"></a><span data-ttu-id="84378-526">IPaymentProcessor インターフェイスの実装</span><span class="sxs-lookup"><span data-stu-id="84378-526">Implement the IPaymentProcessor interface</span></span>
<span data-ttu-id="84378-527">支払フローに関連するマーチャント プロパティを処理するには、**Microsoft.Dynamics.Retail.PaymentSDK** ライブラリで定義されている **IPaymentProcessor** インターフェイスを実装する必要があります。</span><span class="sxs-lookup"><span data-stu-id="84378-527">To handle merchant properties that are related to payment flows, the **IPaymentProcessor** interface that is defined in the **Microsoft.Dynamics.Retail.PaymentSDK** library must be implemented.</span></span> <span data-ttu-id="84378-528">次の例は、2 つの必須インターフェイス メソッド、**GetMerchantAccountPropertyMetadata** と **ValidateMerchantAccount** を実装する方法を示しています。.</span><span class="sxs-lookup"><span data-stu-id="84378-528">The following example shows how to implement the two required interface methods, **GetMerchantAccountPropertyMetadata** and **ValidateMerchantAccount**.</span></span> <span data-ttu-id="84378-529">他のインターフェイス メソッドは、空白にできます (たとえば、**FeatureNotSupportedException** を返すことができます)。</span><span class="sxs-lookup"><span data-stu-id="84378-529">Other interface methods can be left blank (for example, they can return **FeatureNotSupportedException**).</span></span>

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

#### <a name="required-merchant-property-fields"></a><span data-ttu-id="84378-530">必須商社プロパティ フィールド</span><span class="sxs-lookup"><span data-stu-id="84378-530">Required merchant property fields</span></span>
<span data-ttu-id="84378-531">次のテーブルに、**GetMerchantAccountPropertyMetadata** メソッドの一部として設定する必要のある商社プロパティのフィールドを示します。</span><span class="sxs-lookup"><span data-stu-id="84378-531">The following table shows the required merchant property fields that must be set as part of the **GetMerchantAccountPropertyMetadata** method.</span></span>

| <span data-ttu-id="84378-532">名前空間</span><span class="sxs-lookup"><span data-stu-id="84378-532">Namespace</span></span> | <span data-ttu-id="84378-533">氏名</span><span class="sxs-lookup"><span data-stu-id="84378-533">Name</span></span> | <span data-ttu-id="84378-534">サンプル値\*</span><span class="sxs-lookup"><span data-stu-id="84378-534">Sample value\*</span></span> |
|---|---|---|
| <span data-ttu-id="84378-535">MerchantAccount</span><span class="sxs-lookup"><span data-stu-id="84378-535">MerchantAccount</span></span> | <span data-ttu-id="84378-536">PortableAssemblyName</span><span class="sxs-lookup"><span data-stu-id="84378-536">PortableAssemblyName</span></span> | <span data-ttu-id="84378-537">Contoso.Microsoft.PaymentsSample</span><span class="sxs-lookup"><span data-stu-id="84378-537">Contoso.Microsoft.PaymentsSample</span></span> |
| <span data-ttu-id="84378-538">MerchantAccount</span><span class="sxs-lookup"><span data-stu-id="84378-538">MerchantAccount</span></span> | <span data-ttu-id="84378-539">ServiceAccountId</span><span class="sxs-lookup"><span data-stu-id="84378-539">ServiceAccountId</span></span> | <span data-ttu-id="84378-540">f35989c8-e571-4de1-862a-996c82a2e6b6</span><span class="sxs-lookup"><span data-stu-id="84378-540">f35989c8-e571-4de1-862a-996c82a2e6b6</span></span> |
| <span data-ttu-id="84378-541">MerchantAccount</span><span class="sxs-lookup"><span data-stu-id="84378-541">MerchantAccount</span></span> | <span data-ttu-id="84378-542">SupportedCurrencies</span><span class="sxs-lookup"><span data-stu-id="84378-542">SupportedCurrencies</span></span> | <span data-ttu-id="84378-543">AUD、BRL、CAD、CHF、CNY、CZK、DKK、EUR、GBP、HKD、HUF、INR、JPY、KPW、KRW、MXN、NOK、NZD、PLN、SEK、SGD、TWD、USD、ZAR</span><span class="sxs-lookup"><span data-stu-id="84378-543">AUD;BRL;CAD;CHF;CNY;CZK;DKK;EUR;GBP;HKD;HUF;INR;JPY;KPW;KRW;MXN;NOK;NZD;PLN;SEK;SGD;TWD;USD;ZAR</span></span> |
| <span data-ttu-id="84378-544">MerchantAccount</span><span class="sxs-lookup"><span data-stu-id="84378-544">MerchantAccount</span></span> | <span data-ttu-id="84378-545">SupportedTenderTypes</span><span class="sxs-lookup"><span data-stu-id="84378-545">SupportedTenderTypes</span></span> | <span data-ttu-id="84378-546">Visa;MasterCard;Amex;Discover;Debit</span><span class="sxs-lookup"><span data-stu-id="84378-546">Visa;MasterCard;Amex;Discover;Debit</span></span> |

<span data-ttu-id="84378-547">\* この列のサンプル値を、独自の支払プロセッサの固有値に置き換える **必要があります** 。</span><span class="sxs-lookup"><span data-stu-id="84378-547">\* You **must** replace the sample values in this column with unique values for your own payment processor.</span></span>

