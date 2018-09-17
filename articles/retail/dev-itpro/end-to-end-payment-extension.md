---
title: "支払端末のエンド・ツー・エンド支払統合を作成する"
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
ms.sourcegitcommit: 965826f5fddc2f53f33157434929eb265979376e
ms.openlocfilehash: 49cce4a45177cec7652d89421d02026ce4f1924d
ms.contentlocale: ja-jp
ms.lasthandoff: 09/17/2018

---

# <a name="create-an-end-to-end-payment-integration-for-a-payment-terminal"></a><span data-ttu-id="8f60d-103">支払端末のエンド・ツー・エンド支払統合を作成する</span><span class="sxs-lookup"><span data-stu-id="8f60d-103">Create an end-to-end payment integration for a payment terminal</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="8f60d-104">このトピックでは、支払ゲートウェイと直接通信できる支払端末向けに Microsoft Dynamics 365 for Retail Modern POS とクラウド POS (POS) の支払統合を記述する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="8f60d-104">This topic describes how to write a payment integration for Microsoft Dynamics 365 for Retail Modern POS and Cloud POS (the POS) for a payment terminal that can directly communicate with the payment gateway.</span></span>

## <a name="key-terms"></a><span data-ttu-id="8f60d-105">重要な用語</span><span class="sxs-lookup"><span data-stu-id="8f60d-105">Key terms</span></span>

| <span data-ttu-id="8f60d-106">期間</span><span class="sxs-lookup"><span data-stu-id="8f60d-106">Term</span></span> | <span data-ttu-id="8f60d-107">説明</span><span class="sxs-lookup"><span data-stu-id="8f60d-107">Description</span></span> |
|---|---|
| <span data-ttu-id="8f60d-108">支払コネクタ</span><span class="sxs-lookup"><span data-stu-id="8f60d-108">Payment connector</span></span> | <span data-ttu-id="8f60d-109">POS に支払ターミナルを統合するために書き込まれた拡張ライブラリです。</span><span class="sxs-lookup"><span data-stu-id="8f60d-109">An extension library that is written to integrate the POS with a payment terminal.</span></span> |
| <span data-ttu-id="8f60d-110">支払プロセッサ</span><span class="sxs-lookup"><span data-stu-id="8f60d-110">Payment processor</span></span> | <span data-ttu-id="8f60d-111">支払コネクタで使用される商社プロパティを取得するために書き込まれる拡張ライブラリです。</span><span class="sxs-lookup"><span data-stu-id="8f60d-111">An extension library that is written to retrieve merchant properties that the payment connector uses.</span></span> |

## <a name="overview"></a><span data-ttu-id="8f60d-112">概要</span><span class="sxs-lookup"><span data-stu-id="8f60d-112">Overview</span></span>
<span data-ttu-id="8f60d-113">次の図は、POS を介した支払ターミナルの統合の概要を示しています。</span><span class="sxs-lookup"><span data-stu-id="8f60d-113">The following illustration shows a high-level overview of the payment terminal integration through the POS.</span></span> <span data-ttu-id="8f60d-114">この図では、ローカルのハードウェア ステーションを使用して支払端末と通信を使用することを前提にしていますが、同じパターンを共有のハードウェア ステーションにも適用できます。</span><span class="sxs-lookup"><span data-stu-id="8f60d-114">Although this illustration assumes that a local Hardware Station is used to communicate with the payment terminal, the same patterns apply to a shared Hardware Station.</span></span>

![支払コネクタ統合の概要](media/PAYMENTS/PAYMENT-TERMINAL/Overview.jpg)

<span data-ttu-id="8f60d-116">このトピックでは、支払端末のエンド・ツー・エンド支払統合を作成するために必要な以下の手順について説明します。</span><span class="sxs-lookup"><span data-stu-id="8f60d-116">This topic describes the following steps that are required to create an end-to-end payment integration for a payment terminal:</span></span>

- <span data-ttu-id="8f60d-117">**[支払コネクタの記述](#Write-a-payment-connector):** 支払コネクタは POS と支払ターミナルの間の主要な統合ポイントです。</span><span class="sxs-lookup"><span data-stu-id="8f60d-117">**[Write a payment connector](#Write-a-payment-connector):** The payment connector is the main integration point between the POS and the payment terminal.</span></span> <span data-ttu-id="8f60d-118">このステップのセクションでは、支払要求 (たとえば、承認、払い戻し、無効化要求) を支払端末に中継できる、新しい支払コネクタを実装し、設定する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="8f60d-118">The section for this step describes how to implement and configure a new payment connector that can relay payment requests (for example, authorize, refund, and void requests) to the payment terminal.</span></span> 
- <span data-ttu-id="8f60d-119">**[支払プロセッサの記述](#Write-a-payment-processor):** 支払プロセッサは、支払の統合の一部として使用される商社プロパティを定義するために使用します。</span><span class="sxs-lookup"><span data-stu-id="8f60d-119">**[Write a payment processor](#Write-a-payment-processor):** The payment processor is used to define the merchant properties that are used as part of the payment integration.</span></span> <span data-ttu-id="8f60d-120">このステップのセクションでは、新しい支払プロセッサを実装する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="8f60d-120">The section for this step describes how to implement a new payment processor.</span></span> <span data-ttu-id="8f60d-121">これには、実装する必要があるインターフェイスおよび従う必要があるパターンに関する情報が含まれています。</span><span class="sxs-lookup"><span data-stu-id="8f60d-121">It includes information about the interfaces that you should implement and patterns that you should follow.</span></span>

## <a name="write-a-payment-connector"></a><span data-ttu-id="8f60d-122">支払コネクタの記述</span><span class="sxs-lookup"><span data-stu-id="8f60d-122">Write a payment connector</span></span>
<span data-ttu-id="8f60d-123">次のこのセクションでは、新しい支払コネクタを記述する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="8f60d-123">This section describes how to write a new payment connector.</span></span>

### <a name="understanding-the-payment-flows"></a><span data-ttu-id="8f60d-124">支払フローを理解する</span><span class="sxs-lookup"><span data-stu-id="8f60d-124">Understanding the payment flows</span></span>
<span data-ttu-id="8f60d-125">次の図は、POS、ハードウェア ステーション、および支払コネクタ全体にわたるいくつかの支払フロー (トランザクションの開始、カート ラインの更新、承認、キャプチャ、および終了トランザクション) の概要を示しています。</span><span class="sxs-lookup"><span data-stu-id="8f60d-125">The following illustration shows a high-level overview of several payment flows (Begin Transaction, Update Cart Lines, Authorize, Capture, and End Transaction) across the POS, Hardware Station, and payment connector.</span></span>

![支払フローの概要](media/PAYMENTS/PAYMENT-TERMINAL/PaymentFlow.jpg)

### <a name="implement-a-payment-connector"></a><span data-ttu-id="8f60d-127">支払コネクタの実装</span><span class="sxs-lookup"><span data-stu-id="8f60d-127">Implement a payment connector</span></span>
<span data-ttu-id="8f60d-128">次のこのセクションでは、新しい支払コネクタを実装する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="8f60d-128">This section below describes how to implement a new payment connector.</span></span> <span data-ttu-id="8f60d-129">ここに示す例は、Retailソフトウェアの開発キット (SDK) の **SampleExtensions\HardwareStation\Extension.PaymentSample** フォルダーにある **PaymentDeviceSample** クラスにあります。</span><span class="sxs-lookup"><span data-stu-id="8f60d-129">The examples that are shown here can be found in the **PaymentDeviceSample** class that is located under the **SampleExtensions\HardwareStation\Extension.PaymentSample** folder in the Retail software development kit (SDK).</span></span>

#### <a name="implement-the-inamedrequesthandler-interface"></a><span data-ttu-id="8f60d-130">INamedRequestHandler インターフェイスの実装</span><span class="sxs-lookup"><span data-stu-id="8f60d-130">Implement the INamedRequestHandler interface</span></span>
<span data-ttu-id="8f60d-131">すべての POS 支払関連フローは、ハードウェア ステーションで要求/応答パターンを通じて処理されます。</span><span class="sxs-lookup"><span data-stu-id="8f60d-131">All POS payment-related flows are handled through request/response patterns in the Hardware Station.</span></span> <span data-ttu-id="8f60d-132">新しい支払コネクタを作成するプロセスの第一歩は、**Microsoft.Dynamics.Commerce.Runtime.Framework** ライブラリで定義されている **INamedRequestHandler** インターフェイスを実装するクラスを作成することです。</span><span class="sxs-lookup"><span data-stu-id="8f60d-132">The first step in the process of writing a new payment connector is to create a class that implements the **INamedRequestHandler** interface that is defined in the **Microsoft.Dynamics.Commerce.Runtime.Framework** library.</span></span>

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

<span data-ttu-id="8f60d-133">**HandlerName** 文字列は、Microsoft Dynamics 365 for Finance and Operations クライアントを通じて特定の POS で使用される支払コネクタを構成するために使用されます (このトピックの後半の情報を参照してください)。</span><span class="sxs-lookup"><span data-stu-id="8f60d-133">The **HandlerName** string is used to configure the payment connector that is used on a given POS register through the Microsoft Dynamics 365 for Finance and Operations client (see the information later in this topic).</span></span>

#### <a name="implement-supported-payment-requests"></a><span data-ttu-id="8f60d-134">サポートされている支払要求の実装</span><span class="sxs-lookup"><span data-stu-id="8f60d-134">Implement supported payment requests</span></span>
<span data-ttu-id="8f60d-135">支払関連フローを処理するには、支払コネクタが処理できる、サポートされている要求タイプを定義する必要があります。</span><span class="sxs-lookup"><span data-stu-id="8f60d-135">To process payment-related flows, the payment connector must define the supported request types that it can handle.</span></span> <span data-ttu-id="8f60d-136">また、**実行**メソッドは、コネクタが指定されたメソッドをサポートする各要求をルーティングするために実装する必要があります。</span><span class="sxs-lookup"><span data-stu-id="8f60d-136">Additionally, the **Execute** method must be implemented to route each request that the connector supports to a given method.</span></span> <span data-ttu-id="8f60d-137">次の例は、サポートされている要求のタイプの完全な一覧と、特定の要求 (すなわち、承認要求) の例を示しています。</span><span class="sxs-lookup"><span data-stu-id="8f60d-137">The following example shows the complete list of supported request types and an example of a specific request (that is, an authorize request).</span></span>

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

#### <a name="full-list-of-supported-request-types"></a><span data-ttu-id="8f60d-138">サポートされる要求タイプの完全な一覧</span><span class="sxs-lookup"><span data-stu-id="8f60d-138">Full list of supported request types</span></span>
<span data-ttu-id="8f60d-139">次のテーブルは、支払コネクタが実装できるサポートされているすべての要求のタイプを示しています。</span><span class="sxs-lookup"><span data-stu-id="8f60d-139">The following table describes all supported requests types that a payment connector can implement.</span></span>

| <span data-ttu-id="8f60d-140">クラスのリクエスト</span><span class="sxs-lookup"><span data-stu-id="8f60d-140">Request class</span></span> | <span data-ttu-id="8f60d-141">支払フローの説明</span><span class="sxs-lookup"><span data-stu-id="8f60d-141">Payment flow description</span></span> |
|---|---|
| <span data-ttu-id="8f60d-142">OpenPaymentTerminalDeviceRequest</span><span class="sxs-lookup"><span data-stu-id="8f60d-142">OpenPaymentTerminalDeviceRequest</span></span> | <span data-ttu-id="8f60d-143">この要求は、販売取引が開始される前に呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="8f60d-143">This request is called before a sales transaction is initiated.</span></span> <span data-ttu-id="8f60d-144">支払ターミナルへの接続を確立するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="8f60d-144">It is used to establish a connection to the payment terminal.</span></span> |
| <span data-ttu-id="8f60d-145">BeginTransactionPaymentTerminalDeviceRequest</span><span class="sxs-lookup"><span data-stu-id="8f60d-145">BeginTransactionPaymentTerminalDeviceRequest</span></span> | <span data-ttu-id="8f60d-146">この要求は、新しい販売取引が開始されたときに呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="8f60d-146">This request is called when a new sales transaction is initiated.</span></span> <span data-ttu-id="8f60d-147">支払ターミナルで初期化を処理するために使用されます (たとえば、トランザクション画面の初期化)。</span><span class="sxs-lookup"><span data-stu-id="8f60d-147">It is used to handle any initialization on the payment terminal (for example, by initializing the transaction screen).</span></span> |
| <span data-ttu-id="8f60d-148">LockPaymentTerminalDeviceRequest</span><span class="sxs-lookup"><span data-stu-id="8f60d-148">LockPaymentTerminalDeviceRequest</span></span> | <span data-ttu-id="8f60d-149">この要求は支払ターミナルがトランザクションに対してロックされている場合、呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="8f60d-149">This request is called when a payment terminal is locked for a transaction.</span></span> |
| <span data-ttu-id="8f60d-150">UpdateLineItemsPaymentTerminalDeviceRequest</span><span class="sxs-lookup"><span data-stu-id="8f60d-150">UpdateLineItemsPaymentTerminalDeviceRequest</span></span> | <span data-ttu-id="8f60d-151">この要求は、カート内の明細行品目が更新されたときに呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="8f60d-151">This request is called when line items in the cart are updated.</span></span> |
| <span data-ttu-id="8f60d-152">AuthorizePaymentTerminalDeviceRequest</span><span class="sxs-lookup"><span data-stu-id="8f60d-152">AuthorizePaymentTerminalDeviceRequest</span></span> | <span data-ttu-id="8f60d-153">この要求は、POS 支払ビューで支払が開始されたときに呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="8f60d-153">This request is called when a payment is initiated in the POS payment view.</span></span> |
| <span data-ttu-id="8f60d-154">CancelOperationPaymentTerminalDeviceRequest</span><span class="sxs-lookup"><span data-stu-id="8f60d-154">CancelOperationPaymentTerminalDeviceRequest</span></span> | <span data-ttu-id="8f60d-155">この要求は、支払いが開始された後、支払い端末で支払いが完了する前に、支払いビュー ダイアログ ボックスで **キャンセル** ボタンを選択すると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="8f60d-155">This request is called when a user selects the **Cancel** button in the payment view dialog box after the payment is initiated but before the payment is completed on the payment terminal.</span></span> |
| <span data-ttu-id="8f60d-156">CapturePaymentTerminalDeviceRequest</span><span class="sxs-lookup"><span data-stu-id="8f60d-156">CapturePaymentTerminalDeviceRequest</span></span> | <span data-ttu-id="8f60d-157">この要求は、カート内の全額が支払われた時点で、販売取引が終了する前に、各支払い行に対して呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="8f60d-157">This request is called for each payment line when the whole amount in the cart is paid but before the sales transaction is concluded.</span></span> |
| <span data-ttu-id="8f60d-158">VoidPaymentTerminalDeviceRequest</span><span class="sxs-lookup"><span data-stu-id="8f60d-158">VoidPaymentTerminalDeviceRequest</span></span> | <span data-ttu-id="8f60d-159">この要求は、カート内の支払い行が無効になったときに呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="8f60d-159">This request is called when a payment line is voided in the cart.</span></span> |
| <span data-ttu-id="8f60d-160">RefundPaymentTerminalDeviceRequest</span><span class="sxs-lookup"><span data-stu-id="8f60d-160">RefundPaymentTerminalDeviceRequest</span></span> | <span data-ttu-id="8f60d-161">この要求は、払い戻しが行われたときに呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="8f60d-161">This request is called when a refund is issued.</span></span> |
| <span data-ttu-id="8f60d-162">FetchTokenPaymentTerminalDeviceRequest</span><span class="sxs-lookup"><span data-stu-id="8f60d-162">FetchTokenPaymentTerminalDeviceRequest</span></span> | <span data-ttu-id="8f60d-163">この要求は、顧客注文の繰延支払いをサポートするために支払トークンをフェッチするために呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="8f60d-163">This request is called to fetch a payment token to support deferred payments for customer orders.</span></span> |
| <span data-ttu-id="8f60d-164">EndTransactionPaymentTerminalDeviceRequest</span><span class="sxs-lookup"><span data-stu-id="8f60d-164">EndTransactionPaymentTerminalDeviceRequest</span></span> | <span data-ttu-id="8f60d-165">この要求は、販売取引が終了し、すべての支払いが取り込まれたときに呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="8f60d-165">This request is called when the sales transaction is concluded and all payments have been captured.</span></span> |
| <span data-ttu-id="8f60d-166">ClosePaymentTerminalDeviceRequest</span><span class="sxs-lookup"><span data-stu-id="8f60d-166">ClosePaymentTerminalDeviceRequest</span></span> | <span data-ttu-id="8f60d-167">この要求は、販売取引の終了後に呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="8f60d-167">This request is called after the sales transaction is concluded.</span></span> <span data-ttu-id="8f60d-168">支払ターミナルへの接続を閉じるために使用されます。</span><span class="sxs-lookup"><span data-stu-id="8f60d-168">It is used to close the connection to the payment terminal.</span></span> |
| <span data-ttu-id="8f60d-169">ActivateGiftCardPaymentTerminalRequest</span><span class="sxs-lookup"><span data-stu-id="8f60d-169">ActivateGiftCardPaymentTerminalRequest</span></span> | <span data-ttu-id="8f60d-170">この要求は、外部ギフト カードが POS を介して有効化されているときに呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="8f60d-170">This request is called when an external gift card is being activated through the POS.</span></span> |
| <span data-ttu-id="8f60d-171">AddBalanceToGiftCardPaymentTerminalRequest</span><span class="sxs-lookup"><span data-stu-id="8f60d-171">AddBalanceToGiftCardPaymentTerminalRequest</span></span> | <span data-ttu-id="8f60d-172">この要求は、外部ギフト カードに残高が追加されるときに呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="8f60d-172">This request is called when a balance is being added to an external gift card.</span></span> |
| <span data-ttu-id="8f60d-173">GetGiftCardBalancePaymentTerminalRequest</span><span class="sxs-lookup"><span data-stu-id="8f60d-173">GetGiftCardBalancePaymentTerminalRequest</span></span> | <span data-ttu-id="8f60d-174">この要求は、ギフト カードの残高が取得されるときに呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="8f60d-174">This request is called when the balance on the gift card is being retrieved.</span></span> |
| <span data-ttu-id="8f60d-175">GetPrivateTenderPaymentTerminalDeviceRequest</span><span class="sxs-lookup"><span data-stu-id="8f60d-175">GetPrivateTenderPaymentTerminalDeviceRequest</span></span> | <span data-ttu-id="8f60d-176">この要求は、ギフト カード番号がギフト カード フローの支払い端末から取得されたときに呼び出されます (ギフト カードの発行、ギフト カードによる支払い、ギフト カードへの追加など)。</span><span class="sxs-lookup"><span data-stu-id="8f60d-176">This request is called when gift card numbers are retrieved from the payment terminal for gift card flows (for example, Issue gift card, Pay by gift card, or Add to gift card).</span></span> |
| <span data-ttu-id="8f60d-177">ExecuteTaskPaymentTerminalDeviceRequest</span><span class="sxs-lookup"><span data-stu-id="8f60d-177">ExecuteTaskPaymentTerminalDeviceRequest</span></span> | <span data-ttu-id="8f60d-178">この拡張要求は、カスタマイズを介して POS から呼び出すことができます。</span><span class="sxs-lookup"><span data-stu-id="8f60d-178">This extension request can be invoked from the POS through customizations.</span></span> <span data-ttu-id="8f60d-179">支払に関連する追加のフローを有効にするために使用されます。</span><span class="sxs-lookup"><span data-stu-id="8f60d-179">It is used to enable additional payment-related flows.</span></span> |

##### <a name="openpaymentterminaldevicerequest"></a><span data-ttu-id="8f60d-180">OpenPaymentTerminalDeviceRequest</span><span class="sxs-lookup"><span data-stu-id="8f60d-180">OpenPaymentTerminalDeviceRequest</span></span>
###### <a name="signature"></a><span data-ttu-id="8f60d-181">署名</span><span class="sxs-lookup"><span data-stu-id="8f60d-181">Signature</span></span>
``` csharp
public OpenPaymentTerminalDeviceRequest(string token, string deviceName, SettingsInfo terminalSettings, PeripheralConfiguration deviceConfig, ExtensionTransaction extensionTransactionProperties);
```

###### <a name="variables"></a><span data-ttu-id="8f60d-182">変数</span><span class="sxs-lookup"><span data-stu-id="8f60d-182">Variables</span></span>

| <span data-ttu-id="8f60d-183">変動</span><span class="sxs-lookup"><span data-stu-id="8f60d-183">Variable</span></span> | <span data-ttu-id="8f60d-184">説明</span><span class="sxs-lookup"><span data-stu-id="8f60d-184">Description</span></span> |
|---|---|
| <span data-ttu-id="8f60d-185">token</span><span class="sxs-lookup"><span data-stu-id="8f60d-185">token</span></span> | <span data-ttu-id="8f60d-186">支払い端末が最初のトランザクションのためにロックされたときに生成される一意のトークン値。</span><span class="sxs-lookup"><span data-stu-id="8f60d-186">The unique token value that is generated when the payment terminal is initially locked for the transaction.</span></span> |
| <span data-ttu-id="8f60d-187">deviceName</span><span class="sxs-lookup"><span data-stu-id="8f60d-187">deviceName</span></span> | <span data-ttu-id="8f60d-188">Finance and Operations クライアントの **POS hardware profile** ページで定義されている、デバイスの名前。</span><span class="sxs-lookup"><span data-stu-id="8f60d-188">The name of the device, as defined on the **POS hardware profile** page in the Finance and Operations client.</span></span> |
| <span data-ttu-id="8f60d-189">terminalSettings</span><span class="sxs-lookup"><span data-stu-id="8f60d-189">terminalSettings</span></span> | <span data-ttu-id="8f60d-190">Finance and Operations クライアントで定義された支払端末固有の構成プロパティのセット。シグネチャ取り込みの最小額やデビット キャッシュバック限度などです。</span><span class="sxs-lookup"><span data-stu-id="8f60d-190">The set of payment terminal–specific configuration properties that are defined in the Finance and Operations client, such as the minimum amount for signature capture and the debit cash-back limit.</span></span> |
| <span data-ttu-id="8f60d-191">deviceConfig</span><span class="sxs-lookup"><span data-stu-id="8f60d-191">deviceConfig</span></span> | <span data-ttu-id="8f60d-192">ネットワーク端末の場合の IP アドレスやポートなど、名前/値のペアの形式の支払端末固有の設定プロパティのセット。</span><span class="sxs-lookup"><span data-stu-id="8f60d-192">The set of payment terminal–specific configuration properties in the form of name/value pairs, such as the IP address and port in the case of network devices.</span></span> |
| <span data-ttu-id="8f60d-193">extensionTransactionProperties</span><span class="sxs-lookup"><span data-stu-id="8f60d-193">extensionTransactionProperties</span></span> | <span data-ttu-id="8f60d-194">名前/値のペアの形式の拡張構成プロパティのセット。</span><span class="sxs-lookup"><span data-stu-id="8f60d-194">The set of extension configuration properties in the form of name/value pairs.</span></span> |

##### <a name="begintransactionpaymentterminaldevicerequest"></a><span data-ttu-id="8f60d-195">BeginTransactionPaymentTerminalDeviceRequest</span><span class="sxs-lookup"><span data-stu-id="8f60d-195">BeginTransactionPaymentTerminalDeviceRequest</span></span>
###### <a name="signature"></a><span data-ttu-id="8f60d-196">署名</span><span class="sxs-lookup"><span data-stu-id="8f60d-196">Signature</span></span>
``` csharp
public BeginTransactionPaymentTerminalDeviceRequest(string token, string paymentConnectorName, string merchantInformation, string invoiceNumber, bool isTestMode, ExtensionTransaction extensionTransactionProperties)
```

###### <a name="variables"></a><span data-ttu-id="8f60d-197">変数</span><span class="sxs-lookup"><span data-stu-id="8f60d-197">Variables</span></span>

| <span data-ttu-id="8f60d-198">変動</span><span class="sxs-lookup"><span data-stu-id="8f60d-198">Variable</span></span> | <span data-ttu-id="8f60d-199">説明</span><span class="sxs-lookup"><span data-stu-id="8f60d-199">Description</span></span> |
|---|---|
| <span data-ttu-id="8f60d-200">token</span><span class="sxs-lookup"><span data-stu-id="8f60d-200">token</span></span> | <span data-ttu-id="8f60d-201">支払い端末が最初のトランザクションのためにロックされたときに生成される一意のトークン値。</span><span class="sxs-lookup"><span data-stu-id="8f60d-201">The unique token value that is generated when the payment terminal is initially locked for the transaction.</span></span> |
| <span data-ttu-id="8f60d-202">paymentConnectorName</span><span class="sxs-lookup"><span data-stu-id="8f60d-202">paymentConnectorName</span></span> | <span data-ttu-id="8f60d-203">支払フローの一部として使用される支払コネクタの名前。</span><span class="sxs-lookup"><span data-stu-id="8f60d-203">The name of the payment connector that is used as part of the payment flow.</span></span> <span data-ttu-id="8f60d-204">この変数は、**IPaymentProcessor** インターフェイスを使用する支払フローと統合する予定がある場合に使用されます。</span><span class="sxs-lookup"><span data-stu-id="8f60d-204">This variable is used if you plan to integrate with payment flows that use the **IPaymentProcessor** interface.</span></span> |
| <span data-ttu-id="8f60d-205">merchantInformation</span><span class="sxs-lookup"><span data-stu-id="8f60d-205">merchantInformation</span></span> | <span data-ttu-id="8f60d-206">Finance and Operations クライアントの **POS hardware profile** ページで定義されている商社情報。</span><span class="sxs-lookup"><span data-stu-id="8f60d-206">The merchant information that is defined on the **POS hardware profile** page in the Finance and Operations client.</span></span> |
| <span data-ttu-id="8f60d-207">invoiceNumber</span><span class="sxs-lookup"><span data-stu-id="8f60d-207">invoiceNumber</span></span> | <span data-ttu-id="8f60d-208">POS が販売トランザクションを追跡するために生成する一意の請求書番号。</span><span class="sxs-lookup"><span data-stu-id="8f60d-208">The unique invoice number that the POS generates to track the sales transaction.</span></span> |
| <span data-ttu-id="8f60d-209">isTestMode</span><span class="sxs-lookup"><span data-stu-id="8f60d-209">isTestMode</span></span> | <span data-ttu-id="8f60d-210">支払コネクタがテスト モードで使用されているかどうかを示す値。</span><span class="sxs-lookup"><span data-stu-id="8f60d-210">A value that indicates whether the payment connector is being used in testing mode.</span></span> |
| <span data-ttu-id="8f60d-211">extensionTransactionProperties</span><span class="sxs-lookup"><span data-stu-id="8f60d-211">extensionTransactionProperties</span></span> | <span data-ttu-id="8f60d-212">名前/値のペアの形式の拡張構成プロパティのセット。</span><span class="sxs-lookup"><span data-stu-id="8f60d-212">The set of extension configuration properties in the form of name/value pairs.</span></span> |

##### <a name="lockpaymentterminaldevicerequest"></a><span data-ttu-id="8f60d-213">LockPaymentTerminalDeviceRequest</span><span class="sxs-lookup"><span data-stu-id="8f60d-213">LockPaymentTerminalDeviceRequest</span></span>
###### <a name="signature"></a><span data-ttu-id="8f60d-214">署名</span><span class="sxs-lookup"><span data-stu-id="8f60d-214">Signature</span></span>
``` csharp
public LockPaymentTerminalDeviceRequest(string clientDeviceNumber, string deviceType, string deviceName, bool isExclusive, bool isOverride)
```

###### <a name="variables"></a><span data-ttu-id="8f60d-215">変数</span><span class="sxs-lookup"><span data-stu-id="8f60d-215">Variables</span></span>

| <span data-ttu-id="8f60d-216">変動</span><span class="sxs-lookup"><span data-stu-id="8f60d-216">Variable</span></span> | <span data-ttu-id="8f60d-217">説明</span><span class="sxs-lookup"><span data-stu-id="8f60d-217">Description</span></span> |
|---|---|
| <span data-ttu-id="8f60d-218">clientDeviceNumber</span><span class="sxs-lookup"><span data-stu-id="8f60d-218">clientDeviceNumber</span></span> | <span data-ttu-id="8f60d-219">ロックに使用される固有の POS デバイス番号</span><span class="sxs-lookup"><span data-stu-id="8f60d-219">The unique POS device number that is acquiring the lock.</span></span> |
| <span data-ttu-id="8f60d-220">deviceType</span><span class="sxs-lookup"><span data-stu-id="8f60d-220">deviceType</span></span> | <span data-ttu-id="8f60d-221">POS ハードウェア プロファイル (「Windows」など) で構成されるようにロックを取得したデバイス タイプ。</span><span class="sxs-lookup"><span data-stu-id="8f60d-221">The device type that the lock is acquired for as configured in the POS hardware profile (such as "Windows").</span></span> |
| <span data-ttu-id="8f60d-222">deviceName</span><span class="sxs-lookup"><span data-stu-id="8f60d-222">deviceName</span></span> | <span data-ttu-id="8f60d-223">POS ハードウェア プロファイル (「MOCKPAYMENTTERMINAL」など) で構成されるようにロックを取得したデバイス タイプ。</span><span class="sxs-lookup"><span data-stu-id="8f60d-223">The device type that the lock is acquired for as configured in the POS hardware profile (such as "MOCKPAYMENTTERMINAL").</span></span> |
| <span data-ttu-id="8f60d-224">isExclusive</span><span class="sxs-lookup"><span data-stu-id="8f60d-224">isExclusive</span></span> | <span data-ttu-id="8f60d-225">取得したロックが占有されているかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="8f60d-225">Determines whether the lock that is acquired is exclusive.</span></span> | 
| <span data-ttu-id="8f60d-226">isOverride</span><span class="sxs-lookup"><span data-stu-id="8f60d-226">isOverride</span></span> | <span data-ttu-id="8f60d-227">この要求が、既存のロックを上書きするかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="8f60d-227">Determines whether this request will override any existing lock.</span></span> |

##### <a name="updatelineitemspaymentterminaldevicerequest"></a><span data-ttu-id="8f60d-228">UpdateLineItemsPaymentTerminalDeviceRequest</span><span class="sxs-lookup"><span data-stu-id="8f60d-228">UpdateLineItemsPaymentTerminalDeviceRequest</span></span>
###### <a name="signature"></a><span data-ttu-id="8f60d-229">署名</span><span class="sxs-lookup"><span data-stu-id="8f60d-229">Signature</span></span>
``` csharp
public UpdateLineItemsPaymentTerminalDeviceRequest(string token, string totalAmount, string taxAmount, string discountAmount, string subTotalAmount, IEnumerable<ItemInfo> items, ExtensionTransaction extensionTransactionProperties = null)
```

###### <a name="variables"></a><span data-ttu-id="8f60d-230">変数</span><span class="sxs-lookup"><span data-stu-id="8f60d-230">Variables</span></span>

| <span data-ttu-id="8f60d-231">変動</span><span class="sxs-lookup"><span data-stu-id="8f60d-231">Variable</span></span> | <span data-ttu-id="8f60d-232">説明</span><span class="sxs-lookup"><span data-stu-id="8f60d-232">Description</span></span> |
|---|---|
| <span data-ttu-id="8f60d-233">token</span><span class="sxs-lookup"><span data-stu-id="8f60d-233">token</span></span> | <span data-ttu-id="8f60d-234">支払い端末が最初のトランザクションのためにロックされたときに生成される一意のトークン値。</span><span class="sxs-lookup"><span data-stu-id="8f60d-234">The unique token value that is generated when the payment terminal is initially locked for the transaction.</span></span> |
| <span data-ttu-id="8f60d-235">totalAmount</span><span class="sxs-lookup"><span data-stu-id="8f60d-235">totalAmount</span></span> | <span data-ttu-id="8f60d-236">現在の販売トランザクションでの合計金額。</span><span class="sxs-lookup"><span data-stu-id="8f60d-236">The total amount on the current sales transaction.</span></span> |
| <span data-ttu-id="8f60d-237">taxAmount</span><span class="sxs-lookup"><span data-stu-id="8f60d-237">taxAmount</span></span> | <span data-ttu-id="8f60d-238">現在の販売トランザクションでの税金額。</span><span class="sxs-lookup"><span data-stu-id="8f60d-238">The tax amount on the current sales transaction.</span></span> |
| <span data-ttu-id="8f60d-239">discountAmount</span><span class="sxs-lookup"><span data-stu-id="8f60d-239">discountAmount</span></span> | <span data-ttu-id="8f60d-240">現在の販売トランザクションでの割引金額。</span><span class="sxs-lookup"><span data-stu-id="8f60d-240">The discount amount on the current sales transaction.</span></span> |
| <span data-ttu-id="8f60d-241">subTotalAmount</span><span class="sxs-lookup"><span data-stu-id="8f60d-241">subTotalAmount</span></span> | <span data-ttu-id="8f60d-242">現在の販売トランザクションでの小計金額。</span><span class="sxs-lookup"><span data-stu-id="8f60d-242">The subtotal amount on the current sales transaction.</span></span> |
| <span data-ttu-id="8f60d-243">項目</span><span class="sxs-lookup"><span data-stu-id="8f60d-243">items</span></span> | <span data-ttu-id="8f60d-244">表示する明細行品目のリスト。</span><span class="sxs-lookup"><span data-stu-id="8f60d-244">The list of line items to show.</span></span> |
| <span data-ttu-id="8f60d-245">extensionTransactionProperties</span><span class="sxs-lookup"><span data-stu-id="8f60d-245">extensionTransactionProperties</span></span> | <span data-ttu-id="8f60d-246">名前/値のペアの形式の拡張構成プロパティのセット。</span><span class="sxs-lookup"><span data-stu-id="8f60d-246">The set of extension configuration properties in the form of name/value pairs.</span></span> |

##### <a name="authorizepaymentterminaldevicerequest"></a><span data-ttu-id="8f60d-247">AuthorizePaymentTerminalDeviceRequest</span><span class="sxs-lookup"><span data-stu-id="8f60d-247">AuthorizePaymentTerminalDeviceRequest</span></span>
###### <a name="signature"></a><span data-ttu-id="8f60d-248">署名</span><span class="sxs-lookup"><span data-stu-id="8f60d-248">Signature</span></span>
``` csharp
public AuthorizePaymentTerminalDeviceRequest(string token, string paymentConnectorName, decimal amount, string currency, TenderInfo tenderInfo, string voiceAuthorization, bool isManualEntry, ExtensionTransaction extensionTransactionProperties)
```

###### <a name="variables"></a><span data-ttu-id="8f60d-249">変数</span><span class="sxs-lookup"><span data-stu-id="8f60d-249">Variables</span></span>

| <span data-ttu-id="8f60d-250">変動</span><span class="sxs-lookup"><span data-stu-id="8f60d-250">Variable</span></span> | <span data-ttu-id="8f60d-251">説明</span><span class="sxs-lookup"><span data-stu-id="8f60d-251">Description</span></span> |
|---|---|
| <span data-ttu-id="8f60d-252">token</span><span class="sxs-lookup"><span data-stu-id="8f60d-252">token</span></span> | <span data-ttu-id="8f60d-253">支払い端末が最初のトランザクションのためにロックされたときに生成される一意のトークン値。</span><span class="sxs-lookup"><span data-stu-id="8f60d-253">The unique token value that is generated when the payment terminal is initially locked for the transaction.</span></span> |
| <span data-ttu-id="8f60d-254">paymentConnectorName</span><span class="sxs-lookup"><span data-stu-id="8f60d-254">paymentConnectorName</span></span> | <span data-ttu-id="8f60d-255">支払フローの一部として使用される支払コネクタの名前。</span><span class="sxs-lookup"><span data-stu-id="8f60d-255">The name of the payment connector that is used as part of the payment flow.</span></span> <span data-ttu-id="8f60d-256">この変数は、**IPaymentProcessor** インターフェイスを使用する支払フローとの統合がある場合に使用されます。</span><span class="sxs-lookup"><span data-stu-id="8f60d-256">This variable is used if there is an integration with payment flows that use the **IPaymentProcessor** interface.</span></span> |
| <span data-ttu-id="8f60d-257">金額</span><span class="sxs-lookup"><span data-stu-id="8f60d-257">amount</span></span> | <span data-ttu-id="8f60d-258">承認する金額。</span><span class="sxs-lookup"><span data-stu-id="8f60d-258">The amount to authorize.</span></span> |
| <span data-ttu-id="8f60d-259">通貨</span><span class="sxs-lookup"><span data-stu-id="8f60d-259">currency</span></span> | <span data-ttu-id="8f60d-260">承認する金額の通貨。</span><span class="sxs-lookup"><span data-stu-id="8f60d-260">The currency for the amount to authorize.</span></span> |
| <span data-ttu-id="8f60d-261">tenderInfo</span><span class="sxs-lookup"><span data-stu-id="8f60d-261">tenderInfo</span></span> | <span data-ttu-id="8f60d-262">外部ソースから取得された POS から送信されるカード情報 (外部ソースがある場合)。</span><span class="sxs-lookup"><span data-stu-id="8f60d-262">The card information that is sent from the POS that is retrieved from an external source (if an external source is present).</span></span> |
| <span data-ttu-id="8f60d-263">voiceAuthorization</span><span class="sxs-lookup"><span data-stu-id="8f60d-263">voiceAuthorization</span></span> | <span data-ttu-id="8f60d-264">音声認証が必要な場合は、POS から送信される音声承認コード。</span><span class="sxs-lookup"><span data-stu-id="8f60d-264">The voice approval code that is sent from the POS if voice authorization is required.</span></span> |
| <span data-ttu-id="8f60d-265">isManualEntry</span><span class="sxs-lookup"><span data-stu-id="8f60d-265">isManualEntry</span></span> | <span data-ttu-id="8f60d-266">カード番号を手動で入力されたかどうかを定義する値。</span><span class="sxs-lookup"><span data-stu-id="8f60d-266">A value that defines whether the card number was entered manually.</span></span> |
| <span data-ttu-id="8f60d-267">extensionTransactionProperties</span><span class="sxs-lookup"><span data-stu-id="8f60d-267">extensionTransactionProperties</span></span> | <span data-ttu-id="8f60d-268">名前/値のペアの形式の拡張構成プロパティのセット。</span><span class="sxs-lookup"><span data-stu-id="8f60d-268">The set of extension configuration properties in the form of name/value pairs.</span></span> |

###### <a name="response"></a><span data-ttu-id="8f60d-269">応答</span><span class="sxs-lookup"><span data-stu-id="8f60d-269">Response</span></span>
<span data-ttu-id="8f60d-270">**AuthorizePaymentCardPaymentResponse** 応答オブジェクトは、**AuthorizePaymentTerminalDeviceRequest** 要求が処理されたときに返される必要があります。</span><span class="sxs-lookup"><span data-stu-id="8f60d-270">The **AuthorizePaymentCardPaymentResponse** response object must be returned when the **AuthorizePaymentTerminalDeviceRequest** request is handled.</span></span> <span data-ttu-id="8f60d-271">応答には、次の必須プロパティを持つ **PaymentInfo** オブジェクトのインスタンスが含まれている必要があります。</span><span class="sxs-lookup"><span data-stu-id="8f60d-271">The response must contain an instance of the **PaymentInfo** object that has the following required properties.</span></span>

| <span data-ttu-id="8f60d-272">プロパティ</span><span class="sxs-lookup"><span data-stu-id="8f60d-272">Property</span></span> | <span data-ttu-id="8f60d-273">説明</span><span class="sxs-lookup"><span data-stu-id="8f60d-273">Description</span></span> |
|---|---|
| <span data-ttu-id="8f60d-274">ApprovedAmount</span><span class="sxs-lookup"><span data-stu-id="8f60d-274">ApprovedAmount</span></span> | <span data-ttu-id="8f60d-275">トランザクションに対して承認された金額。</span><span class="sxs-lookup"><span data-stu-id="8f60d-275">The amount that was approved for the transaction.</span></span> |
| <span data-ttu-id="8f60d-276">CardNumberMasked</span><span class="sxs-lookup"><span data-stu-id="8f60d-276">CardNumberMasked</span></span> | <span data-ttu-id="8f60d-277">マスクされたクレジット カード番号。</span><span class="sxs-lookup"><span data-stu-id="8f60d-277">The masked credit card number.</span></span> <span data-ttu-id="8f60d-278">この値には、少なくとも POS 内の在庫置場範囲の参照をサポートするため、クレジット カードの最初の桁が含まれている必要があります。</span><span class="sxs-lookup"><span data-stu-id="8f60d-278">The value must contain at least the first digit of the credit card to support bin range lookup in the POS.</span></span> <span data-ttu-id="8f60d-279">(ほとんどのデバイスは、最初の 6 桁と最後の 4 桁を返します。)</span><span class="sxs-lookup"><span data-stu-id="8f60d-279">(Most devices return the first six digits and the last four digits.)</span></span> |
| <span data-ttu-id="8f60d-280">CardType</span><span class="sxs-lookup"><span data-stu-id="8f60d-280">CardType</span></span> | <span data-ttu-id="8f60d-281">**Microsoft.Dynamics.Commerce.HardwareStation.CardPayment.CardType** エンティティを使用して支払い (**クレジット** または **デビット** など) に使われたカードのタイプ。</span><span class="sxs-lookup"><span data-stu-id="8f60d-281">The type of card that was used for the payment (for example, **Credit** or **Debit**) by using the **Microsoft.Dynamics.Commerce.HardwareStation.CardPayment.CardType** entity.</span></span> |
| <span data-ttu-id="8f60d-282">CashbackAmount</span><span class="sxs-lookup"><span data-stu-id="8f60d-282">CashbackAmount</span></span> | <span data-ttu-id="8f60d-283">借方トランザクションの場合、キャッシュ バック金額は支払のターミナルで定義されました。</span><span class="sxs-lookup"><span data-stu-id="8f60d-283">For debit transactions, the cash-back amount that was defined on the payment terminal.</span></span> |
| <span data-ttu-id="8f60d-284">エラー</span><span class="sxs-lookup"><span data-stu-id="8f60d-284">Errors</span></span> | <span data-ttu-id="8f60d-285">承認呼び出し中に発生したエラーのリスト。</span><span class="sxs-lookup"><span data-stu-id="8f60d-285">The list of errors that occurred during the authorize call.</span></span> |
| <span data-ttu-id="8f60d-286">IsApproved</span><span class="sxs-lookup"><span data-stu-id="8f60d-286">IsApproved</span></span> | <span data-ttu-id="8f60d-287">支払が承認されたかどうかを示すフラグ。</span><span class="sxs-lookup"><span data-stu-id="8f60d-287">A flag that indicates whether the payment was approved.</span></span> |
| <span data-ttu-id="8f60d-288">PaymentSdkData</span><span class="sxs-lookup"><span data-stu-id="8f60d-288">PaymentSdkData</span></span> | <span data-ttu-id="8f60d-289">承認/返金と、キャプチャ/呼び出しの無効化またはクロスチャネルの支払操作の間の状態をサポートするために使用される応答データ。</span><span class="sxs-lookup"><span data-stu-id="8f60d-289">The response data that is used to support state between the authorize/refund and capture/void calls or cross-channel payment operations.</span></span> |

<span data-ttu-id="8f60d-290">**PaymentSdkData** プロパティには、次のデータを含める必要があります。</span><span class="sxs-lookup"><span data-stu-id="8f60d-290">The **PaymentSdkData** property must contain the following data.</span></span>

| <span data-ttu-id="8f60d-291">名前空間</span><span class="sxs-lookup"><span data-stu-id="8f60d-291">Namespace</span></span> | <span data-ttu-id="8f60d-292">氏名</span><span class="sxs-lookup"><span data-stu-id="8f60d-292">Name</span></span> | <span data-ttu-id="8f60d-293">説明</span><span class="sxs-lookup"><span data-stu-id="8f60d-293">Description</span></span> | <span data-ttu-id="8f60d-294">サンプル値</span><span class="sxs-lookup"><span data-stu-id="8f60d-294">Sample value</span></span> |
|---|---|---|---|
| <span data-ttu-id="8f60d-295">コネクタ</span><span class="sxs-lookup"><span data-stu-id="8f60d-295">Connector</span></span> | <span data-ttu-id="8f60d-296">ConnectorName</span><span class="sxs-lookup"><span data-stu-id="8f60d-296">ConnectorName</span></span> | <span data-ttu-id="8f60d-297">このトピックの後半にある「支払プロセッサの記述」セクションで説明している、トランザクションに使用される **IPaymentProcessor**インターフェイスの名前です。</span><span class="sxs-lookup"><span data-stu-id="8f60d-297">The name of the **IPaymentProcessor** interface that is used for the transactions, as described in the "Write a payment processor" section later in this topic.</span></span> |
| <span data-ttu-id="8f60d-298">AuthorizationResponse</span><span class="sxs-lookup"><span data-stu-id="8f60d-298">AuthorizationResponse</span></span> | <span data-ttu-id="8f60d-299">プロパティ</span><span class="sxs-lookup"><span data-stu-id="8f60d-299">Properties</span></span> | <span data-ttu-id="8f60d-300">承認応答のリスト。</span><span class="sxs-lookup"><span data-stu-id="8f60d-300">The list of authorization responses.</span></span> | <span data-ttu-id="8f60d-301">次の表を参照してください。</span><span class="sxs-lookup"><span data-stu-id="8f60d-301">See the next table.</span></span> |

<span data-ttu-id="8f60d-302">**PaymentSdkData** プロパティの **プロパティ** フィールドには、次のフィールドを含める必要があります。</span><span class="sxs-lookup"><span data-stu-id="8f60d-302">The **Properties** field of the **PaymentSdkData** property must contain the following fields.</span></span>

| <span data-ttu-id="8f60d-303">名前空間</span><span class="sxs-lookup"><span data-stu-id="8f60d-303">Namespace</span></span> | <span data-ttu-id="8f60d-304">氏名</span><span class="sxs-lookup"><span data-stu-id="8f60d-304">Name</span></span> | <span data-ttu-id="8f60d-305">説明</span><span class="sxs-lookup"><span data-stu-id="8f60d-305">Description</span></span> | <span data-ttu-id="8f60d-306">サンプル値</span><span class="sxs-lookup"><span data-stu-id="8f60d-306">Sample value</span></span> |
|---|---|---|---|
| <span data-ttu-id="8f60d-307">AuthorizationResponse</span><span class="sxs-lookup"><span data-stu-id="8f60d-307">AuthorizationResponse</span></span> | <span data-ttu-id="8f60d-308">ApprovedAmount</span><span class="sxs-lookup"><span data-stu-id="8f60d-308">ApprovedAmount</span></span> | <span data-ttu-id="8f60d-309">トランザクションに対して承認された金額。</span><span class="sxs-lookup"><span data-stu-id="8f60d-309">The amount that was approved for the transaction.</span></span> | <span data-ttu-id="8f60d-310">28.08 m</span><span class="sxs-lookup"><span data-stu-id="8f60d-310">28.08m</span></span> |
| <span data-ttu-id="8f60d-311">AuthorizationResponse</span><span class="sxs-lookup"><span data-stu-id="8f60d-311">AuthorizationResponse</span></span> | <span data-ttu-id="8f60d-312">AvailableBalance</span><span class="sxs-lookup"><span data-stu-id="8f60d-312">AvailableBalance</span></span> | <span data-ttu-id="8f60d-313">カードの使用可能な残高。</span><span class="sxs-lookup"><span data-stu-id="8f60d-313">The available balance on the card.</span></span> | <span data-ttu-id="8f60d-314">100.00m</span><span class="sxs-lookup"><span data-stu-id="8f60d-314">100.00m</span></span> |
| <span data-ttu-id="8f60d-315">AuthorizationResponse</span><span class="sxs-lookup"><span data-stu-id="8f60d-315">AuthorizationResponse</span></span> | <span data-ttu-id="8f60d-316">ApprovalCode</span><span class="sxs-lookup"><span data-stu-id="8f60d-316">ApprovalCode</span></span> | <span data-ttu-id="8f60d-317">トランザクションの承認コード。</span><span class="sxs-lookup"><span data-stu-id="8f60d-317">The approval code for the transaction.</span></span> | <span data-ttu-id="8f60d-318">Z123456</span><span class="sxs-lookup"><span data-stu-id="8f60d-318">Z123456</span></span> |
| <span data-ttu-id="8f60d-319">AuthorizationResponse</span><span class="sxs-lookup"><span data-stu-id="8f60d-319">AuthorizationResponse</span></span> | <span data-ttu-id="8f60d-320">ProviderTransactionId</span><span class="sxs-lookup"><span data-stu-id="8f60d-320">ProviderTransactionId</span></span> | <span data-ttu-id="8f60d-321">支払いプロバイダーのトランザクション識別子。</span><span class="sxs-lookup"><span data-stu-id="8f60d-321">The transaction identifier of the payment provider.</span></span> | <span data-ttu-id="8f60d-322">123456789</span><span class="sxs-lookup"><span data-stu-id="8f60d-322">123456789</span></span> |
| <span data-ttu-id="8f60d-323">AuthorizationResponse</span><span class="sxs-lookup"><span data-stu-id="8f60d-323">AuthorizationResponse</span></span> | <span data-ttu-id="8f60d-324">AuthorizationResult</span><span class="sxs-lookup"><span data-stu-id="8f60d-324">AuthorizationResult</span></span> | <span data-ttu-id="8f60d-325">権限呼び出しの結果。</span><span class="sxs-lookup"><span data-stu-id="8f60d-325">The result of the authorization call.</span></span> | <span data-ttu-id="8f60d-326">AuthorizationResult.Success.ToString()</span><span class="sxs-lookup"><span data-stu-id="8f60d-326">AuthorizationResult.Success.ToString()</span></span> |
| <span data-ttu-id="8f60d-327">AuthorizationResponse</span><span class="sxs-lookup"><span data-stu-id="8f60d-327">AuthorizationResponse</span></span> | <span data-ttu-id="8f60d-328">ExternalReceipt</span><span class="sxs-lookup"><span data-stu-id="8f60d-328">ExternalReceipt</span></span> | <span data-ttu-id="8f60d-329">支払プロバイダーからの外部レシート データ。</span><span class="sxs-lookup"><span data-stu-id="8f60d-329">The external receipt data from the payment provider.</span></span> | <span data-ttu-id="8f60d-330">\<ReceiptData\>...\</ReceiptData\></span><span class="sxs-lookup"><span data-stu-id="8f60d-330">\<ReceiptData\>...\</ReceiptData\></span></span> |
| <span data-ttu-id="8f60d-331">AuthorizationResponse</span><span class="sxs-lookup"><span data-stu-id="8f60d-331">AuthorizationResponse</span></span> | <span data-ttu-id="8f60d-332">TerminalId</span><span class="sxs-lookup"><span data-stu-id="8f60d-332">TerminalId</span></span> | <span data-ttu-id="8f60d-333">支払を処理した端末の一意の識別子。</span><span class="sxs-lookup"><span data-stu-id="8f60d-333">The unique identifier of the terminal that handled the payment.</span></span> | <span data-ttu-id="8f60d-334">000001</span><span class="sxs-lookup"><span data-stu-id="8f60d-334">000001</span></span> |

<span data-ttu-id="8f60d-335">次の例は、**PaymentSdkData** オブジェクトを作成する方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="8f60d-335">The following example shows how to construct the **PaymentSdkData** object.</span></span>

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

<span data-ttu-id="8f60d-336">支払端末がレシートを返す場合、先ほど説明した **ExternalReceipt** オブジェクトで次のデータを設定し、POS を介して印刷することができます。</span><span class="sxs-lookup"><span data-stu-id="8f60d-336">If the payment terminal returns a receipt, you can print it through the POS by setting the following data on the **ExternalReceipt** object that was described earlier.</span></span>

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

###### <a name="other-considerations"></a><span data-ttu-id="8f60d-337">その他の考慮事項</span><span class="sxs-lookup"><span data-stu-id="8f60d-337">Other considerations</span></span>
<span data-ttu-id="8f60d-338">支払端末が 1 つの呼び出しでの要求を承認し、キャプチャし (つまり*迅速なキャプチャ*が発生する場合)、出納係が取引を無効にすることを希望する場合、支払い端末では即時回収の取消がサポートされている必要があります。</span><span class="sxs-lookup"><span data-stu-id="8f60d-338">If the payment terminal handles the authorize and capture requests in a single call (that is, if *immediate capture* occurs), and the cashier wants to void the transaction, the payment terminal must support reversal of an immediate capture.</span></span> <span data-ttu-id="8f60d-339">迅速なキャプチャが無効なとき、無効化要求が失敗した場合、レジ担当者は、ローカルで支払を無効にするかどうかを求められます。</span><span class="sxs-lookup"><span data-stu-id="8f60d-339">When an immediate capture is voided, if the void request fails, the cashier will be asked whether he or she wants to locally void the payment.</span></span> <span data-ttu-id="8f60d-340">レジ担当者が**はい**と選択した場合、入札は POS でのみ無効になります。</span><span class="sxs-lookup"><span data-stu-id="8f60d-340">If the cashier selects **Yes**, the tender is voided only in the POS.</span></span> <span data-ttu-id="8f60d-341">支払を無効にするために支払ターミナルに対して行われる呼び出しはありません。</span><span class="sxs-lookup"><span data-stu-id="8f60d-341">No call is made to the payment terminal to void the payment.</span></span> <span data-ttu-id="8f60d-342">基本的には、この動作により、支払ターミナルの支払を無効にできなくなった場合レジ担当者は POS をブロック解除することができます。</span><span class="sxs-lookup"><span data-stu-id="8f60d-342">Basically, this behavior lets the cashier unblock the POS if it can no longer void the payment on the payment terminal.</span></span> <span data-ttu-id="8f60d-343">ただし、銀行が取り消すまでの 3 ~ 5日間はロックが続くため、この動作には問題が生じますが、迅速なキャプチャのための支払いが行われます。</span><span class="sxs-lookup"><span data-stu-id="8f60d-343">However, this behavior can cause issues, because a lock lasts for three to five days, until the bank reverses it, but the payment is made for immediate capture.</span></span> <span data-ttu-id="8f60d-344">したがって、重複した支払いが発生する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="8f60d-344">Therefore, duplicate payments can occur.</span></span>

##### <a name="canceloperationpaymentterminaldevicerequest"></a><span data-ttu-id="8f60d-345">CancelOperationPaymentTerminalDeviceRequest</span><span class="sxs-lookup"><span data-stu-id="8f60d-345">CancelOperationPaymentTerminalDeviceRequest</span></span>
###### <a name="signature"></a><span data-ttu-id="8f60d-346">署名</span><span class="sxs-lookup"><span data-stu-id="8f60d-346">Signature</span></span>
``` csharp
public CancelOperationPaymentTerminalDeviceRequest(string token)
```

###### <a name="variables"></a><span data-ttu-id="8f60d-347">変数</span><span class="sxs-lookup"><span data-stu-id="8f60d-347">Variables</span></span>

| <span data-ttu-id="8f60d-348">変動</span><span class="sxs-lookup"><span data-stu-id="8f60d-348">Variable</span></span> | <span data-ttu-id="8f60d-349">説明</span><span class="sxs-lookup"><span data-stu-id="8f60d-349">Description</span></span> |
|---|---|
| <span data-ttu-id="8f60d-350">token</span><span class="sxs-lookup"><span data-stu-id="8f60d-350">token</span></span> | <span data-ttu-id="8f60d-351">支払い端末が最初のトランザクションのためにロックされたときに生成される一意のトークン値。</span><span class="sxs-lookup"><span data-stu-id="8f60d-351">The unique token value that is generated when the payment terminal is initially locked for the transaction.</span></span> |

##### <a name="capturepaymentterminaldevicerequest"></a><span data-ttu-id="8f60d-352">CapturePaymentTerminalDeviceRequest</span><span class="sxs-lookup"><span data-stu-id="8f60d-352">CapturePaymentTerminalDeviceRequest</span></span>
###### <a name="signature"></a><span data-ttu-id="8f60d-353">署名</span><span class="sxs-lookup"><span data-stu-id="8f60d-353">Signature</span></span>
``` csharp
public CapturePaymentTerminalDeviceRequest(string token, decimal amount, string currency, string paymentPropertiesXml, ExtensionTransaction extensionTransactionProperties)
```

###### <a name="variables"></a><span data-ttu-id="8f60d-354">変数</span><span class="sxs-lookup"><span data-stu-id="8f60d-354">Variables</span></span>

| <span data-ttu-id="8f60d-355">変動</span><span class="sxs-lookup"><span data-stu-id="8f60d-355">Variable</span></span> | <span data-ttu-id="8f60d-356">説明</span><span class="sxs-lookup"><span data-stu-id="8f60d-356">Description</span></span> |
|---|---|
| <span data-ttu-id="8f60d-357">token</span><span class="sxs-lookup"><span data-stu-id="8f60d-357">token</span></span> | <span data-ttu-id="8f60d-358">支払い端末が最初のトランザクションのためにロックされたときに生成される一意のトークン値。</span><span class="sxs-lookup"><span data-stu-id="8f60d-358">The unique token value that is generated when the payment terminal is initially locked for the transaction.</span></span> |
| <span data-ttu-id="8f60d-359">金額</span><span class="sxs-lookup"><span data-stu-id="8f60d-359">amount</span></span> | <span data-ttu-id="8f60d-360">取得する金額。</span><span class="sxs-lookup"><span data-stu-id="8f60d-360">The amount to capture.</span></span> |
| <span data-ttu-id="8f60d-361">通貨</span><span class="sxs-lookup"><span data-stu-id="8f60d-361">currency</span></span> | <span data-ttu-id="8f60d-362">取得する金額の通貨。</span><span class="sxs-lookup"><span data-stu-id="8f60d-362">The currency for the amount to capture.</span></span> |
| <span data-ttu-id="8f60d-363">paymentPropertiesXml</span><span class="sxs-lookup"><span data-stu-id="8f60d-363">paymentPropertiesXml</span></span> | <span data-ttu-id="8f60d-364">**AuthorizePaymentTerminalDeviceRequest** 要求または **RefundPaymentTerminalDeviceRequest** 要求によって返され、要求間のステートフル プロパティをサポートするために使用される **PaymentSdkData** オブジェクトのコンテンツ。</span><span class="sxs-lookup"><span data-stu-id="8f60d-364">The content of the **PaymentSdkData** object that is returned by the **AuthorizePaymentTerminalDeviceRequest** or **RefundPaymentTerminalDeviceRequest** request, and that is used to support stateful properties between the requests.</span></span> |
| <span data-ttu-id="8f60d-365">extensionTransactionProperties</span><span class="sxs-lookup"><span data-stu-id="8f60d-365">extensionTransactionProperties</span></span> | <span data-ttu-id="8f60d-366">名前/値のペアの形式の拡張構成プロパティのセット。</span><span class="sxs-lookup"><span data-stu-id="8f60d-366">The set of extension configuration properties in the form of name/value pairs.</span></span> |

###### <a name="other-considerations"></a><span data-ttu-id="8f60d-367">その他の考慮事項</span><span class="sxs-lookup"><span data-stu-id="8f60d-367">Other considerations</span></span>
<span data-ttu-id="8f60d-368">支払端末が 1 つの呼び出しでの要求を承認およびキャプチャする場合、**CapturePaymentTerminalDeviceRequest** 要求はノーオーペレーションである必要があり、すぐに返す必要があります。</span><span class="sxs-lookup"><span data-stu-id="8f60d-368">If the payment terminal handles the authorize and capture requests in a single call, the **CapturePaymentTerminalDeviceRequest** request should be a no-op and should immediately return.</span></span>

<span data-ttu-id="8f60d-369">支払端末が、キャプチャ呼び出しを処理する許可要求からの状態を必要とする場合、プロパティは、先に説明した **AuthorizePaymentTerminalDeviceResponse** 要求の **PaymentSdkData** オブジェクトに格納され、 **CapturePaymentTerminalDeviceRequest** 要求の **paymentPropertiesXml** 変数を渡します。</span><span class="sxs-lookup"><span data-stu-id="8f60d-369">If the payment terminal requires state from the authorize requests to handle the capture call, the properties should be stored in the **PaymentSdkData** object of the **AuthorizePaymentTerminalDeviceResponse** request that is described earlier, and passed through the **paymentPropertiesXml** variable of the **CapturePaymentTerminalDeviceRequest** request.</span></span>

##### <a name="voidpaymentterminaldevicerequest"></a><span data-ttu-id="8f60d-370">VoidPaymentTerminalDeviceRequest</span><span class="sxs-lookup"><span data-stu-id="8f60d-370">VoidPaymentTerminalDeviceRequest</span></span>
###### <a name="signature"></a><span data-ttu-id="8f60d-371">署名</span><span class="sxs-lookup"><span data-stu-id="8f60d-371">Signature</span></span>
``` csharp
public VoidPaymentTerminalDeviceRequest(string token, string paymentConnectorName, decimal amount, string currency, TenderInfo tenderInfo, string paymentPropertiesXml, ExtensionTransaction extensionTransactionProperties)
```

###### <a name="variables"></a><span data-ttu-id="8f60d-372">変数</span><span class="sxs-lookup"><span data-stu-id="8f60d-372">Variables</span></span>

| <span data-ttu-id="8f60d-373">変動</span><span class="sxs-lookup"><span data-stu-id="8f60d-373">Variable</span></span> | <span data-ttu-id="8f60d-374">説明</span><span class="sxs-lookup"><span data-stu-id="8f60d-374">Description</span></span> |
|---|---|
| <span data-ttu-id="8f60d-375">token</span><span class="sxs-lookup"><span data-stu-id="8f60d-375">token</span></span> | <span data-ttu-id="8f60d-376">支払い端末が最初のトランザクションのためにロックされたときに生成される一意のトークン値。</span><span class="sxs-lookup"><span data-stu-id="8f60d-376">The unique token value that is generated when the payment terminal is initially locked for the transaction.</span></span> |
| <span data-ttu-id="8f60d-377">paymentConnectorName</span><span class="sxs-lookup"><span data-stu-id="8f60d-377">paymentConnectorName</span></span> | <span data-ttu-id="8f60d-378">支払フローの一部として使用される支払コネクタの名前。</span><span class="sxs-lookup"><span data-stu-id="8f60d-378">The name of the payment connector that is used as part of the payment flow.</span></span> <span data-ttu-id="8f60d-379">この変数は、**IPaymentProcessor** インターフェイスを使用する支払フローとの統合がある場合に使用されます。</span><span class="sxs-lookup"><span data-stu-id="8f60d-379">This variable is used if there is an integration with payment flows that use the **IPaymentProcessor** interface.</span></span> |
| <span data-ttu-id="8f60d-380">金額</span><span class="sxs-lookup"><span data-stu-id="8f60d-380">amount</span></span> | <span data-ttu-id="8f60d-381">支払いが無効になる金額。</span><span class="sxs-lookup"><span data-stu-id="8f60d-381">The amount for the payment to void.</span></span> |
| <span data-ttu-id="8f60d-382">通貨</span><span class="sxs-lookup"><span data-stu-id="8f60d-382">currency</span></span> | <span data-ttu-id="8f60d-383">支払いが無効になる通貨。</span><span class="sxs-lookup"><span data-stu-id="8f60d-383">The currency for the payment to void.</span></span> |
| <span data-ttu-id="8f60d-384">tenderInfo</span><span class="sxs-lookup"><span data-stu-id="8f60d-384">tenderInfo</span></span> | <span data-ttu-id="8f60d-385">外部ソースから取得された POS から送信されるカード情報 (外部ソースがある場合)。</span><span class="sxs-lookup"><span data-stu-id="8f60d-385">The card information that is sent from the POS that is retrieved from an external source (if an external source is present).</span></span> |
| <span data-ttu-id="8f60d-386">paymentPropertiesXml</span><span class="sxs-lookup"><span data-stu-id="8f60d-386">paymentPropertiesXml</span></span> | <span data-ttu-id="8f60d-387">**AuthorizePaymentTerminalDeviceRequest** 要求または **RefundPaymentTerminalDeviceRequest** 要求によって返され、要求間のステートフル プロパティをサポートするために使用される **PaymentSdkData** オブジェクトのコンテンツ。</span><span class="sxs-lookup"><span data-stu-id="8f60d-387">The content of the **PaymentSdkData** object that is returned by the **AuthorizePaymentTerminalDeviceRequest** or **RefundPaymentTerminalDeviceRequest** request, and that is used to support stateful properties between the requests.</span></span> |
| <span data-ttu-id="8f60d-388">extensionTransactionProperties</span><span class="sxs-lookup"><span data-stu-id="8f60d-388">extensionTransactionProperties</span></span> | <span data-ttu-id="8f60d-389">名前/値のペアの形式の拡張構成プロパティのセット。</span><span class="sxs-lookup"><span data-stu-id="8f60d-389">The set of extension configuration properties in the form of name/value pairs.</span></span> |

##### <a name="refundpaymentterminaldevicerequest"></a><span data-ttu-id="8f60d-390">RefundPaymentTerminalDeviceRequest</span><span class="sxs-lookup"><span data-stu-id="8f60d-390">RefundPaymentTerminalDeviceRequest</span></span>
###### <a name="signature"></a><span data-ttu-id="8f60d-391">署名</span><span class="sxs-lookup"><span data-stu-id="8f60d-391">Signature</span></span>
``` csharp
public RefundPaymentTerminalDeviceRequest(string token, string paymentConnectorName, TenderInfo tenderInfo, decimal amount, string currency, bool isManualEntry, ExtensionTransaction extensionTransactionProperties)
```

###### <a name="variables"></a><span data-ttu-id="8f60d-392">変数</span><span class="sxs-lookup"><span data-stu-id="8f60d-392">Variables</span></span>

| <span data-ttu-id="8f60d-393">変動</span><span class="sxs-lookup"><span data-stu-id="8f60d-393">Variable</span></span> | <span data-ttu-id="8f60d-394">説明</span><span class="sxs-lookup"><span data-stu-id="8f60d-394">Description</span></span> |
|---|---|
| <span data-ttu-id="8f60d-395">token</span><span class="sxs-lookup"><span data-stu-id="8f60d-395">token</span></span> | <span data-ttu-id="8f60d-396">支払い端末が最初のトランザクションのためにロックされたときに生成される一意のトークン値。</span><span class="sxs-lookup"><span data-stu-id="8f60d-396">The unique token value that is generated when the payment terminal is initially locked for the transaction.</span></span> |
| <span data-ttu-id="8f60d-397">paymentConnectorName</span><span class="sxs-lookup"><span data-stu-id="8f60d-397">paymentConnectorName</span></span> | <span data-ttu-id="8f60d-398">支払フローの一部として使用される支払コネクタの名前。</span><span class="sxs-lookup"><span data-stu-id="8f60d-398">The name of the payment connector that is used as part of the payment flow.</span></span> <span data-ttu-id="8f60d-399">この変数は、**IPaymentProcessor** インターフェイスを使用する支払フローとの統合がある場合に使用されます。</span><span class="sxs-lookup"><span data-stu-id="8f60d-399">This variable is used if there is an integration with payment flows that use the **IPaymentProcessor** interface.</span></span> |
| <span data-ttu-id="8f60d-400">tenderInfo</span><span class="sxs-lookup"><span data-stu-id="8f60d-400">tenderInfo</span></span> | <span data-ttu-id="8f60d-401">外部ソースから取得された POS から送信されるカード情報 (外部ソースがある場合)。</span><span class="sxs-lookup"><span data-stu-id="8f60d-401">The card information that is sent from the POS that is retrieved from an external source (if an external source is present).</span></span> |
| <span data-ttu-id="8f60d-402">金額</span><span class="sxs-lookup"><span data-stu-id="8f60d-402">amount</span></span> | <span data-ttu-id="8f60d-403">払い戻す金額。</span><span class="sxs-lookup"><span data-stu-id="8f60d-403">The amount to refund.</span></span> |
| <span data-ttu-id="8f60d-404">通貨</span><span class="sxs-lookup"><span data-stu-id="8f60d-404">currency</span></span> | <span data-ttu-id="8f60d-405">払い戻す金額の通貨。</span><span class="sxs-lookup"><span data-stu-id="8f60d-405">The currency for the amount to refund.</span></span> |
| <span data-ttu-id="8f60d-406">isManualEntry</span><span class="sxs-lookup"><span data-stu-id="8f60d-406">isManualEntry</span></span> | <span data-ttu-id="8f60d-407">カード番号を手動で入力されたかどうかを定義する値。</span><span class="sxs-lookup"><span data-stu-id="8f60d-407">A value that defines whether the card number was entered manually.</span></span> |
| <span data-ttu-id="8f60d-408">extensionTransactionProperties</span><span class="sxs-lookup"><span data-stu-id="8f60d-408">extensionTransactionProperties</span></span> | <span data-ttu-id="8f60d-409">名前/値のペアの形式の拡張構成プロパティのセット。</span><span class="sxs-lookup"><span data-stu-id="8f60d-409">The set of extension configuration properties in the form of name/value pairs.</span></span> |

##### <a name="fetchtokenpaymentterminaldevicerequest"></a><span data-ttu-id="8f60d-410">FetchTokenPaymentTerminalDeviceRequest</span><span class="sxs-lookup"><span data-stu-id="8f60d-410">FetchTokenPaymentTerminalDeviceRequest</span></span>
###### <a name="signature"></a><span data-ttu-id="8f60d-411">署名</span><span class="sxs-lookup"><span data-stu-id="8f60d-411">Signature</span></span>
``` csharp
public FetchTokenPaymentTerminalDeviceRequest(string token, bool isManualEntry, ExtensionTransaction extensionTransactionProperties)
```

###### <a name="variables"></a><span data-ttu-id="8f60d-412">変数</span><span class="sxs-lookup"><span data-stu-id="8f60d-412">Variables</span></span>

| <span data-ttu-id="8f60d-413">変動</span><span class="sxs-lookup"><span data-stu-id="8f60d-413">Variable</span></span> | <span data-ttu-id="8f60d-414">説明</span><span class="sxs-lookup"><span data-stu-id="8f60d-414">Description</span></span> |
|---|---|
| <span data-ttu-id="8f60d-415">token</span><span class="sxs-lookup"><span data-stu-id="8f60d-415">token</span></span> | <span data-ttu-id="8f60d-416">支払い端末が最初のトランザクションのためにロックされたときに生成される一意のトークン値。</span><span class="sxs-lookup"><span data-stu-id="8f60d-416">The unique token value that is generated when the payment terminal is initially locked for the transaction.</span></span> |
| <span data-ttu-id="8f60d-417">isManualEntry</span><span class="sxs-lookup"><span data-stu-id="8f60d-417">isManualEntry</span></span> | <span data-ttu-id="8f60d-418">カード番号を手動で入力されたかどうかを定義する値。</span><span class="sxs-lookup"><span data-stu-id="8f60d-418">A value that defines whether the card number was entered manually.</span></span> |
| <span data-ttu-id="8f60d-419">extensionTransactionProperties</span><span class="sxs-lookup"><span data-stu-id="8f60d-419">extensionTransactionProperties</span></span> | <span data-ttu-id="8f60d-420">名前/値のペアの形式の拡張構成プロパティのセット。</span><span class="sxs-lookup"><span data-stu-id="8f60d-420">The set of extension configuration properties in the form of name/value pairs.</span></span> |

##### <a name="endtransactionpaymentterminaldevicerequest"></a><span data-ttu-id="8f60d-421">EndTransactionPaymentTerminalDeviceRequest</span><span class="sxs-lookup"><span data-stu-id="8f60d-421">EndTransactionPaymentTerminalDeviceRequest</span></span>
##### <a name="signature"></a><span data-ttu-id="8f60d-422">署名</span><span class="sxs-lookup"><span data-stu-id="8f60d-422">Signature</span></span>
``` csharp
public EndTransactionPaymentTerminalDeviceRequest(string token, ExtensionTransaction extensionTransactionProperties)
```

###### <a name="variables"></a><span data-ttu-id="8f60d-423">変数</span><span class="sxs-lookup"><span data-stu-id="8f60d-423">Variables</span></span>

| <span data-ttu-id="8f60d-424">変動</span><span class="sxs-lookup"><span data-stu-id="8f60d-424">Variable</span></span> | <span data-ttu-id="8f60d-425">説明</span><span class="sxs-lookup"><span data-stu-id="8f60d-425">Description</span></span> |
|---|---|
| <span data-ttu-id="8f60d-426">token</span><span class="sxs-lookup"><span data-stu-id="8f60d-426">token</span></span> | <span data-ttu-id="8f60d-427">支払い端末が最初のトランザクションのためにロックされたときに生成される一意のトークン値。</span><span class="sxs-lookup"><span data-stu-id="8f60d-427">The unique token value that is generated when the payment terminal is initially locked for the transaction.</span></span> |
| <span data-ttu-id="8f60d-428">extensionTransactionProperties</span><span class="sxs-lookup"><span data-stu-id="8f60d-428">extensionTransactionProperties</span></span> | <span data-ttu-id="8f60d-429">名前/値のペアの形式の拡張構成プロパティのセット。</span><span class="sxs-lookup"><span data-stu-id="8f60d-429">The set of extension configuration properties in the form of name/value pairs.</span></span> |

##### <a name="closepaymentterminaldevicerequest"></a><span data-ttu-id="8f60d-430">ClosePaymentTerminalDeviceRequest</span><span class="sxs-lookup"><span data-stu-id="8f60d-430">ClosePaymentTerminalDeviceRequest</span></span>
###### <a name="signature"></a><span data-ttu-id="8f60d-431">署名</span><span class="sxs-lookup"><span data-stu-id="8f60d-431">Signature</span></span>
``` csharp
public ClosePaymentTerminalDeviceRequest(string token, ExtensionTransaction extensionTransactionProperties)
```

###### <a name="variables"></a><span data-ttu-id="8f60d-432">変数</span><span class="sxs-lookup"><span data-stu-id="8f60d-432">Variables</span></span>

| <span data-ttu-id="8f60d-433">変動</span><span class="sxs-lookup"><span data-stu-id="8f60d-433">Variable</span></span> | <span data-ttu-id="8f60d-434">説明</span><span class="sxs-lookup"><span data-stu-id="8f60d-434">Description</span></span> |
|---|---|
| <span data-ttu-id="8f60d-435">token</span><span class="sxs-lookup"><span data-stu-id="8f60d-435">token</span></span> | <span data-ttu-id="8f60d-436">支払い端末が最初のトランザクションのためにロックされたときに生成される一意のトークン値。</span><span class="sxs-lookup"><span data-stu-id="8f60d-436">The unique token value that is generated when the payment terminal is initially locked for the transaction.</span></span> |
| <span data-ttu-id="8f60d-437">extensionTransactionProperties</span><span class="sxs-lookup"><span data-stu-id="8f60d-437">extensionTransactionProperties</span></span> | <span data-ttu-id="8f60d-438">名前/値のペアの形式の拡張構成プロパティのセット。</span><span class="sxs-lookup"><span data-stu-id="8f60d-438">The set of extension configuration properties in the form of name/value pairs.</span></span> |

##### <a name="activategiftcardpaymentterminalrequest"></a><span data-ttu-id="8f60d-439">ActivateGiftCardPaymentTerminalRequest</span><span class="sxs-lookup"><span data-stu-id="8f60d-439">ActivateGiftCardPaymentTerminalRequest</span></span>
###### <a name="signature"></a><span data-ttu-id="8f60d-440">署名</span><span class="sxs-lookup"><span data-stu-id="8f60d-440">Signature</span></span>
``` csharp
public ActivateGiftCardPaymentTerminalRequest(string token, string paymentConnectorName, decimal amount, string currencyCode, TenderInfo tenderInfo, ExtensionTransaction extensionTransactionProperties)
```

###### <a name="variables"></a><span data-ttu-id="8f60d-441">変数</span><span class="sxs-lookup"><span data-stu-id="8f60d-441">Variables</span></span>

| <span data-ttu-id="8f60d-442">変動</span><span class="sxs-lookup"><span data-stu-id="8f60d-442">Variable</span></span> | <span data-ttu-id="8f60d-443">説明</span><span class="sxs-lookup"><span data-stu-id="8f60d-443">Description</span></span> |
|---|---|
| <span data-ttu-id="8f60d-444">token</span><span class="sxs-lookup"><span data-stu-id="8f60d-444">token</span></span> | <span data-ttu-id="8f60d-445">支払い端末が最初のトランザクションのためにロックされたときに生成される一意のトークン値。</span><span class="sxs-lookup"><span data-stu-id="8f60d-445">The unique token value that is generated when the payment terminal is initially locked for the transaction.</span></span> |
| <span data-ttu-id="8f60d-446">paymentConnectorName</span><span class="sxs-lookup"><span data-stu-id="8f60d-446">paymentConnectorName</span></span> | <span data-ttu-id="8f60d-447">支払フローの一部として使用される支払コネクタの名前。</span><span class="sxs-lookup"><span data-stu-id="8f60d-447">The name of the payment connector that is used as part of the payment flow.</span></span> <span data-ttu-id="8f60d-448">この変数は、**IPaymentProcessor** インターフェイスを使用する支払フローとの統合がある場合に使用されます。</span><span class="sxs-lookup"><span data-stu-id="8f60d-448">This variable is used if there is an integration with payment flows that use the **IPaymentProcessor** interface.</span></span> |
| <span data-ttu-id="8f60d-449">金額</span><span class="sxs-lookup"><span data-stu-id="8f60d-449">amount</span></span> | <span data-ttu-id="8f60d-450">有効化中にギフト カードに追加する初期金額。</span><span class="sxs-lookup"><span data-stu-id="8f60d-450">The initial amount to add to the gift card during activation.</span></span> |
| <span data-ttu-id="8f60d-451">通貨</span><span class="sxs-lookup"><span data-stu-id="8f60d-451">currency</span></span> | <span data-ttu-id="8f60d-452">有効化中にギフト カードに追加する初期金額の通貨。</span><span class="sxs-lookup"><span data-stu-id="8f60d-452">The currency for the initial amount to add to the gift card during activation.</span></span> |
| <span data-ttu-id="8f60d-453">tenderInfo</span><span class="sxs-lookup"><span data-stu-id="8f60d-453">tenderInfo</span></span> | <span data-ttu-id="8f60d-454">外部ソースから取得された POS から送信されるカード情報 (外部ソースがある場合)。</span><span class="sxs-lookup"><span data-stu-id="8f60d-454">The card information that is sent from the POS that is retrieved from an external source (if an external source is present).</span></span> |
| <span data-ttu-id="8f60d-455">extensionTransactionProperties</span><span class="sxs-lookup"><span data-stu-id="8f60d-455">extensionTransactionProperties</span></span> | <span data-ttu-id="8f60d-456">名前/値のペアの形式の拡張構成プロパティのセット。</span><span class="sxs-lookup"><span data-stu-id="8f60d-456">The set of extension configuration properties in the form of name/value pairs.</span></span> |

##### <a name="addbalancetogiftcardpaymentterminalrequest"></a><span data-ttu-id="8f60d-457">AddBalanceToGiftCardPaymentTerminalRequest</span><span class="sxs-lookup"><span data-stu-id="8f60d-457">AddBalanceToGiftCardPaymentTerminalRequest</span></span>
###### <a name="signature"></a><span data-ttu-id="8f60d-458">署名</span><span class="sxs-lookup"><span data-stu-id="8f60d-458">Signature</span></span>
``` csharp
public AddBalanceToGiftCardPaymentTerminalRequest(string token, string paymentConnectorName, decimal amount, string currencyCode, TenderInfo tenderInfo, ExtensionTransaction extensionTransactionProperties)
```

###### <a name="variables"></a><span data-ttu-id="8f60d-459">変数</span><span class="sxs-lookup"><span data-stu-id="8f60d-459">Variables</span></span>

| <span data-ttu-id="8f60d-460">変動</span><span class="sxs-lookup"><span data-stu-id="8f60d-460">Variable</span></span> | <span data-ttu-id="8f60d-461">説明</span><span class="sxs-lookup"><span data-stu-id="8f60d-461">Description</span></span> |
|---|---|
| <span data-ttu-id="8f60d-462">token</span><span class="sxs-lookup"><span data-stu-id="8f60d-462">token</span></span> | <span data-ttu-id="8f60d-463">支払い端末が最初のトランザクションのためにロックされたときに生成される一意のトークン値。</span><span class="sxs-lookup"><span data-stu-id="8f60d-463">The unique token value that is generated when the payment terminal is initially locked for the transaction.</span></span> |
| <span data-ttu-id="8f60d-464">paymentConnectorName</span><span class="sxs-lookup"><span data-stu-id="8f60d-464">paymentConnectorName</span></span> | <span data-ttu-id="8f60d-465">支払フローの一部として使用される支払コネクタの名前。</span><span class="sxs-lookup"><span data-stu-id="8f60d-465">The name of the payment connector that is used as part of the payment flow.</span></span> <span data-ttu-id="8f60d-466">この変数は、**IPaymentProcessor** インターフェイスを使用する支払フローとの統合がある場合に使用されます。</span><span class="sxs-lookup"><span data-stu-id="8f60d-466">This variable is used if there is an integration with payment flows that use the **IPaymentProcessor** interface.</span></span> |
| <span data-ttu-id="8f60d-467">金額</span><span class="sxs-lookup"><span data-stu-id="8f60d-467">amount</span></span> | <span data-ttu-id="8f60d-468">ギフト カードに追加される金額。</span><span class="sxs-lookup"><span data-stu-id="8f60d-468">The amount to add to the gift card.</span></span> |
| <span data-ttu-id="8f60d-469">通貨</span><span class="sxs-lookup"><span data-stu-id="8f60d-469">currency</span></span> | <span data-ttu-id="8f60d-470">ギフト カード残高に追加する金額の通貨。</span><span class="sxs-lookup"><span data-stu-id="8f60d-470">The currency for the amount to add to the gift card balance.</span></span> |
| <span data-ttu-id="8f60d-471">tenderInfo</span><span class="sxs-lookup"><span data-stu-id="8f60d-471">tenderInfo</span></span> | <span data-ttu-id="8f60d-472">外部ソースから取得された POS から送信されるカード情報 (外部ソースがある場合)。</span><span class="sxs-lookup"><span data-stu-id="8f60d-472">The card information that is sent from the POS that is retrieved from an external source (if an external source present).</span></span> |
| <span data-ttu-id="8f60d-473">extensionTransactionProperties</span><span class="sxs-lookup"><span data-stu-id="8f60d-473">extensionTransactionProperties</span></span> | <span data-ttu-id="8f60d-474">名前/値のペアの形式の拡張構成プロパティのセット。</span><span class="sxs-lookup"><span data-stu-id="8f60d-474">The set of extension configuration properties in the form of name/value pairs.</span></span> |

##### <a name="getgiftcardbalancepaymentterminalrequest"></a><span data-ttu-id="8f60d-475">GetGiftCardBalancePaymentTerminalRequest</span><span class="sxs-lookup"><span data-stu-id="8f60d-475">GetGiftCardBalancePaymentTerminalRequest</span></span>
###### <a name="signature"></a><span data-ttu-id="8f60d-476">署名</span><span class="sxs-lookup"><span data-stu-id="8f60d-476">Signature</span></span>
``` csharp
public GetGiftCardBalancePaymentTerminalRequest(string token, string paymentConnectorName, string currencyCode, TenderInfo tenderInfo, ExtensionTransaction extensionTransactionProperties)
```

###### <a name="variables"></a><span data-ttu-id="8f60d-477">変数</span><span class="sxs-lookup"><span data-stu-id="8f60d-477">Variables</span></span>

| <span data-ttu-id="8f60d-478">変動</span><span class="sxs-lookup"><span data-stu-id="8f60d-478">Variable</span></span> | <span data-ttu-id="8f60d-479">説明</span><span class="sxs-lookup"><span data-stu-id="8f60d-479">Description</span></span> |
|---|---|
| <span data-ttu-id="8f60d-480">token</span><span class="sxs-lookup"><span data-stu-id="8f60d-480">token</span></span> | <span data-ttu-id="8f60d-481">支払い端末が最初のトランザクションのためにロックされたときに生成される一意のトークン値。</span><span class="sxs-lookup"><span data-stu-id="8f60d-481">The unique token value that is generated when the payment terminal is initially locked for the transaction.</span></span> |
| <span data-ttu-id="8f60d-482">paymentConnectorName</span><span class="sxs-lookup"><span data-stu-id="8f60d-482">paymentConnectorName</span></span> | <span data-ttu-id="8f60d-483">支払フローの一部として使用される支払コネクタの名前。</span><span class="sxs-lookup"><span data-stu-id="8f60d-483">The name of the payment connector that is used as part of the payment flow.</span></span> <span data-ttu-id="8f60d-484">この変数は、**IPaymentProcessor** インターフェイスを使用する支払フローとの統合がある場合に使用されます。</span><span class="sxs-lookup"><span data-stu-id="8f60d-484">This variable is used if there is an integration with payment flows that use the **IPaymentProcessor** interface.</span></span> |
| <span data-ttu-id="8f60d-485">通貨</span><span class="sxs-lookup"><span data-stu-id="8f60d-485">currency</span></span> | <span data-ttu-id="8f60d-486">ギフト カード残高を取得するための通貨。</span><span class="sxs-lookup"><span data-stu-id="8f60d-486">The currency to retrieve the gift card balance in.</span></span> |
| <span data-ttu-id="8f60d-487">tenderInfo</span><span class="sxs-lookup"><span data-stu-id="8f60d-487">tenderInfo</span></span> | <span data-ttu-id="8f60d-488">外部ソースから取得された POS から送信されるカード情報 (外部ソースがある場合)。</span><span class="sxs-lookup"><span data-stu-id="8f60d-488">The card information that is sent from the POS that is retrieved from an external source (if an external source present).</span></span> |
| <span data-ttu-id="8f60d-489">extensionTransactionProperties</span><span class="sxs-lookup"><span data-stu-id="8f60d-489">extensionTransactionProperties</span></span> | <span data-ttu-id="8f60d-490">名前/値のペアの形式の拡張構成プロパティのセット。</span><span class="sxs-lookup"><span data-stu-id="8f60d-490">The set of extension configuration properties in the form of name/value pairs.</span></span> |

##### <a name="getprivatetenderpaymentterminaldevicerequest"></a><span data-ttu-id="8f60d-491">GetPrivateTenderPaymentTerminalDeviceRequest</span><span class="sxs-lookup"><span data-stu-id="8f60d-491">GetPrivateTenderPaymentTerminalDeviceRequest</span></span>
###### <a name="signature"></a><span data-ttu-id="8f60d-492">署名</span><span class="sxs-lookup"><span data-stu-id="8f60d-492">Signature</span></span>
``` csharp
public GetPrivateTenderPaymentTerminalDeviceRequest(string token, decimal amount, bool declined, bool isSwipe, ExtensionTransaction extensionTransactionProperties)
```

###### <a name="variables"></a><span data-ttu-id="8f60d-493">変数</span><span class="sxs-lookup"><span data-stu-id="8f60d-493">Variables</span></span>

| <span data-ttu-id="8f60d-494">変動</span><span class="sxs-lookup"><span data-stu-id="8f60d-494">Variable</span></span> | <span data-ttu-id="8f60d-495">説明</span><span class="sxs-lookup"><span data-stu-id="8f60d-495">Description</span></span> |
|---|---|
| <span data-ttu-id="8f60d-496">token</span><span class="sxs-lookup"><span data-stu-id="8f60d-496">token</span></span> | <span data-ttu-id="8f60d-497">支払い端末が最初のトランザクションのためにロックされたときに生成される一意のトークン値。</span><span class="sxs-lookup"><span data-stu-id="8f60d-497">The unique token value that is generated when the payment terminal is initially locked for the transaction.</span></span> |
| <span data-ttu-id="8f60d-498">金額</span><span class="sxs-lookup"><span data-stu-id="8f60d-498">amount</span></span> | <span data-ttu-id="8f60d-499">POS に設定された金額。</span><span class="sxs-lookup"><span data-stu-id="8f60d-499">The amount that is set on the POS.</span></span> <span data-ttu-id="8f60d-500">(通常、この変数は、カード番号を取得したときに支払ターミナルの金額を表示するために使用されます。)</span><span class="sxs-lookup"><span data-stu-id="8f60d-500">(Typically, this variable is used to show the amount on the payment terminal when the card number is retrieved.)</span></span> |
| <span data-ttu-id="8f60d-501">declined</span><span class="sxs-lookup"><span data-stu-id="8f60d-501">declined</span></span> | <span data-ttu-id="8f60d-502">この値は廃止されています。</span><span class="sxs-lookup"><span data-stu-id="8f60d-502">This variable is obsolete.</span></span> |
| <span data-ttu-id="8f60d-503">isSwipe</span><span class="sxs-lookup"><span data-stu-id="8f60d-503">isSwipe</span></span> | <span data-ttu-id="8f60d-504">支払ターミナルで読み取りまたは手動入力によってカード番号を取得する必要があるかどうかを決定する値。</span><span class="sxs-lookup"><span data-stu-id="8f60d-504">A value that determines whether the card number should be retrieved through a swipe or manual entry on the payment terminal.</span></span> |
| <span data-ttu-id="8f60d-505">extensionTransactionProperties</span><span class="sxs-lookup"><span data-stu-id="8f60d-505">extensionTransactionProperties</span></span> | <span data-ttu-id="8f60d-506">名前/値のペアの形式の拡張構成プロパティのセット。</span><span class="sxs-lookup"><span data-stu-id="8f60d-506">The set of extension configuration properties in the form of name/value pairs.</span></span> |

##### <a name="executetaskpaymentterminaldevicerequest"></a><span data-ttu-id="8f60d-507">ExecuteTaskPaymentTerminalDeviceRequest</span><span class="sxs-lookup"><span data-stu-id="8f60d-507">ExecuteTaskPaymentTerminalDeviceRequest</span></span>
###### <a name="signature"></a><span data-ttu-id="8f60d-508">署名</span><span class="sxs-lookup"><span data-stu-id="8f60d-508">Signature</span></span>
``` csharp
public ExecuteTaskPaymentTerminalDeviceRequest(string token, string task, ExtensionTransaction extensionTransactionProperties)
```

###### <a name="variables"></a><span data-ttu-id="8f60d-509">変数</span><span class="sxs-lookup"><span data-stu-id="8f60d-509">Variables</span></span>

| <span data-ttu-id="8f60d-510">変動</span><span class="sxs-lookup"><span data-stu-id="8f60d-510">Variable</span></span> | <span data-ttu-id="8f60d-511">説明</span><span class="sxs-lookup"><span data-stu-id="8f60d-511">Description</span></span> |
|---|---|
| <span data-ttu-id="8f60d-512">token</span><span class="sxs-lookup"><span data-stu-id="8f60d-512">token</span></span> | <span data-ttu-id="8f60d-513">支払い端末が最初のトランザクションのためにロックされたときに生成される一意のトークン値。</span><span class="sxs-lookup"><span data-stu-id="8f60d-513">The unique token value that is generated when the payment terminal is initially locked for the transaction.</span></span> |
| <span data-ttu-id="8f60d-514">タスク</span><span class="sxs-lookup"><span data-stu-id="8f60d-514">task</span></span> | <span data-ttu-id="8f60d-515">実行されているタスクの一意の識別子。</span><span class="sxs-lookup"><span data-stu-id="8f60d-515">The unique identifier for the task that is being run.</span></span> |
| <span data-ttu-id="8f60d-516">extensionTransactionProperties</span><span class="sxs-lookup"><span data-stu-id="8f60d-516">extensionTransactionProperties</span></span> | <span data-ttu-id="8f60d-517">名前/値のペアの形式の拡張構成プロパティのセット。</span><span class="sxs-lookup"><span data-stu-id="8f60d-517">The set of extension configuration properties in the form of name/value pairs.</span></span> |

#### <a name="state-in-the-payment-connector"></a><span data-ttu-id="8f60d-518">支払コネクタの状態</span><span class="sxs-lookup"><span data-stu-id="8f60d-518">State in the payment connector</span></span>
<span data-ttu-id="8f60d-519">支払いコネクターは、POS 内のインプロセス ハードウェア ステーションを通じてホストされているとき、dllhost.exe プロセスの一部としてホストすることができます。</span><span class="sxs-lookup"><span data-stu-id="8f60d-519">The payment connector can be hosted as part of the dllhost.exe process when it's hosted through the in-process Hardware Station inside the POS.</span></span> <span data-ttu-id="8f60d-520">または、 Microsoft Internet Information Services (IIS) に基づくハードウェア ステーションでホストされている場合、w3wp.exe プロセスとして支払コネクタをホストすることができます。</span><span class="sxs-lookup"><span data-stu-id="8f60d-520">Alternatively, the payment connector can be hosted as a w3wp.exe process when it's hosted in the Hardware Station that is based on Microsoft Internet Information Services (IIS).</span></span> <span data-ttu-id="8f60d-521">状況によっては、支払フローの間または最中に両方のプロセスを終了したり、応答を停止したりできます。</span><span class="sxs-lookup"><span data-stu-id="8f60d-521">In some circumstances, both processes can be terminated or stop responding between or during payment flows.</span></span> <span data-ttu-id="8f60d-522">したがって、支払コネクタには状態依存性がなく、以前に説明した支払フロー関連の要求のいずれかの時点で終了すると回復することができるようにすることをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="8f60d-522">Therefore, we recommend that payment connectors not have state dependencies, and that they be able to recover if they are terminated at any point during the payment flow–related requests that are described earlier.</span></span>

### <a name="configure-the-payment-connector-in-the-hardware-station-config"></a><span data-ttu-id="8f60d-523">ハードウェア ステーションのコンフィギュレーションで支払コネクタをコンフィギュレーションする</span><span class="sxs-lookup"><span data-stu-id="8f60d-523">Configure the payment connector in the Hardware Station config</span></span>
<span data-ttu-id="8f60d-524">ハードウェア ステーションが支払コネクタを読み込むようにするために、対応するアセンブリ参照を **HardwareStation.Extension.config** ファイルに設定する必要があります。このファイルは Retail SDK の **Assets** フォルダーにあります。</span><span class="sxs-lookup"><span data-stu-id="8f60d-524">To help guarantee that the Hardware Station loads the payment connector, you must set the corresponding assembly reference in the **HardwareStation.Extension.config** file that is located in the **Assets** folder in the Retail SDK.</span></span>

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

### <a name="configure-the-payment-connector-on-the-pos-hardware-profile-page-in-the-finance-and-operations-client"></a><span data-ttu-id="8f60d-525">Finance and Operations クライアントの POS ハードウェア プロファイル ページで支払コネクタをコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="8f60d-525">Configure the payment connector on the POS hardware profile page in the Finance and Operations client</span></span>
<span data-ttu-id="8f60d-526">POS にロードする正しい支払コネクタを決定するには、次の図に示すように、Finance and Operations クライアントの **POSハードウェア プロファイル** ページの **PINパッド** FastTab で、**デバイス名** フィールドの **PaymentTerminalDevice** プロパティの値を設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="8f60d-526">To determine the correct payment connector that should be loaded on the POS, you must set the value of the **PaymentTerminalDevice** property in the **Device name** field on the **PIN pad** FastTab of the **POS hardware profile** page in the Finance and Operations client, as shown in the following illustration.</span></span>

![Finance and Operations クライアントの POS ハードウェア プロファイル ページで支払コネクタをコンフィギュレーション](media/PAYMENTS/PAYMENT-TERMINAL/SamplePaymentDeviceConfigurInAx.jpg)

## <a name="write-a-payment-processor"></a><span data-ttu-id="8f60d-528">支払プロセッサの記述</span><span class="sxs-lookup"><span data-stu-id="8f60d-528">Write a payment processor</span></span>
<span data-ttu-id="8f60d-529">通常は、支払ゲートウェイへの直接接続が確立された場合にのみ、支払プロセスが使用されます。</span><span class="sxs-lookup"><span data-stu-id="8f60d-529">Payment processes are usually used only if a direct connection to a payment gateway is established.</span></span> <span data-ttu-id="8f60d-530">このシナリオは、カードが存在しない販売取引またはより複雑なカードが存在するシナリオで最も頻繁に発生します。</span><span class="sxs-lookup"><span data-stu-id="8f60d-530">This scenario most often occurs in card-not-present sales transactions or more complex card-present scenarios.</span></span> <span data-ttu-id="8f60d-531">また、支払プロセッサは、Finance and Operations クライアントの **POS ハードウェア プロファイル** ページを使用してコンフィギュレーションされている商社プロパティを処理するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="8f60d-531">Additionally, the payment processor is used to process the merchant properties that are configured through the **POS hardware profile** page in the Finance and Operations client.</span></span>

> [!NOTE]
> <span data-ttu-id="8f60d-532">支払プロセッサは、支払要求がすべて支払ターミナルを使用して直接処理され、商社プロパティを POS を使用して設定する必要がない場合でも、現在のところは必要です。</span><span class="sxs-lookup"><span data-stu-id="8f60d-532">The payment processor is currently required, even if all payment requests are handled directly through the payment terminal and no merchant properties must be set through the POS.</span></span>

### <a name="understanding-the-merchant-properties-flows"></a><span data-ttu-id="8f60d-533">商社プロパティ フローを理解する</span><span class="sxs-lookup"><span data-stu-id="8f60d-533">Understanding the merchant properties flows</span></span>
<span data-ttu-id="8f60d-534">次のセクションでは、Finance and Operations クライアントの **POS ハードウェア プロファイル** ページでの商社プロパティの設定方法と、POS での支払フロー中に支払コネクタにこれらのプロパティを渡す方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="8f60d-534">The following sections describe how the merchant properties are set on the **POS hardware profile** page in the Finance and Operations client, and how they are passed to the payment connector during payment flows on the POS.</span></span>

#### <a name="set-merchant-properties-on-the-pos-hardware-profile-page-in-the-finance-and-operations-client"></a><span data-ttu-id="8f60d-535">Finance and Operations クライアントの POS ハードウェア プロファイル ページで商社プロパティを設定</span><span class="sxs-lookup"><span data-stu-id="8f60d-535">Set merchant properties on the POS hardware profile page in the Finance and Operations client</span></span>
<span data-ttu-id="8f60d-536">次の図は、Finance and Operations クライアントの **POS ハードウェア プロファイル** ページで商社プロパティを設定する方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="8f60d-536">The following illustration shows how the merchant properties are set through the **POS hardware profile** page in the Finance and Operations client.</span></span> <span data-ttu-id="8f60d-537">マーチャントプロパティを設定するには、**IPaymentProcessor** ライブラリで定義されている **Microsoft.Dynamics.Retail.PaymentSDK** インターフェイスを実装する必要があります。</span><span class="sxs-lookup"><span data-stu-id="8f60d-537">To enable the merchant properties to be set, the **IPaymentProcessor** interface that is defined in the **Microsoft.Dynamics.Retail.PaymentSDK** library must be implemented.</span></span> <span data-ttu-id="8f60d-538">**GetMerchantAccountPropertyMetadata** と **ValidateMerchantAccount** の 2 つのインターフェイス メソッドが必要です。</span><span class="sxs-lookup"><span data-stu-id="8f60d-538">Two interface methods are required: **GetMerchantAccountPropertyMetadata** and **ValidateMerchantAccount**.</span></span>

![Finance and Operations クライアントの POS ハードウェア プロファイル ページで商社プロパティを設定](media/PAYMENTS/PAYMENT-TERMINAL/MerchantPropertiesAXFlow.jpg)

#### <a name="set-merchant-properties-on-payment-connector-during-pos-sales-transaction"></a><span data-ttu-id="8f60d-540">POS 販売トランザクションの間に支払コネクタで商社プロパティを設定</span><span class="sxs-lookup"><span data-stu-id="8f60d-540">Set merchant properties on payment connector during POS sales transaction</span></span>
<span data-ttu-id="8f60d-541">次の図は、**BeginTransactionPaymentTerminalDeviceRequest** 要求の間に Retail サーバーを介して Finance and Operations データベースから商社プロパティを取得して支払コネクタに渡す仕組みを示しています。</span><span class="sxs-lookup"><span data-stu-id="8f60d-541">The following illustration shows how the merchant properties are retrieved from the Finance and Operations database through the Retail Server and passed to the payment connector during the **BeginTransactionPaymentTerminalDeviceRequest** request.</span></span>

![POS 支払フロー時に支払コネクタに商社プロパティを設定](media/PAYMENTS/PAYMENT-TERMINAL/MerchantPropertiesPOSFlow.jpg)

### <a name="implement-the-ipaymentprocessor-interface"></a><span data-ttu-id="8f60d-543">IPaymentProcessor インターフェイスの実装</span><span class="sxs-lookup"><span data-stu-id="8f60d-543">Implement the IPaymentProcessor interface</span></span>
<span data-ttu-id="8f60d-544">支払フローに関連するマーチャント プロパティを処理するには、**Microsoft.Dynamics.Retail.PaymentSDK** ライブラリで定義されている **IPaymentProcessor** インターフェイスを実装する必要があります。</span><span class="sxs-lookup"><span data-stu-id="8f60d-544">To handle merchant properties that are related to payment flows, the **IPaymentProcessor** interface that is defined in the **Microsoft.Dynamics.Retail.PaymentSDK** library must be implemented.</span></span> <span data-ttu-id="8f60d-545">次の例は、2 つの必須インターフェイス メソッド、**GetMerchantAccountPropertyMetadata** と **ValidateMerchantAccount** を実装する方法を示しています。.</span><span class="sxs-lookup"><span data-stu-id="8f60d-545">The following example shows how to implement the two required interface methods, **GetMerchantAccountPropertyMetadata** and **ValidateMerchantAccount**.</span></span> <span data-ttu-id="8f60d-546">他のインターフェイス メソッドは、空白にできます (たとえば、**FeatureNotSupportedException** を返すことができます)。</span><span class="sxs-lookup"><span data-stu-id="8f60d-546">Other interface methods can be left blank (for example, they can return **FeatureNotSupportedException**).</span></span>

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

#### <a name="required-merchant-property-fields"></a><span data-ttu-id="8f60d-547">必須商社プロパティ フィールド</span><span class="sxs-lookup"><span data-stu-id="8f60d-547">Required merchant property fields</span></span>
<span data-ttu-id="8f60d-548">次のテーブルに、**GetMerchantAccountPropertyMetadata** メソッドの一部として設定する必要のある商社プロパティのフィールドを示します。</span><span class="sxs-lookup"><span data-stu-id="8f60d-548">The following table shows the required merchant property fields that must be set as part of the **GetMerchantAccountPropertyMetadata** method.</span></span>

| <span data-ttu-id="8f60d-549">名前空間</span><span class="sxs-lookup"><span data-stu-id="8f60d-549">Namespace</span></span> | <span data-ttu-id="8f60d-550">氏名</span><span class="sxs-lookup"><span data-stu-id="8f60d-550">Name</span></span> | <span data-ttu-id="8f60d-551">サンプル値\*</span><span class="sxs-lookup"><span data-stu-id="8f60d-551">Sample value\*</span></span> |
|---|---|---|
| <span data-ttu-id="8f60d-552">MerchantAccount</span><span class="sxs-lookup"><span data-stu-id="8f60d-552">MerchantAccount</span></span> | <span data-ttu-id="8f60d-553">PortableAssemblyName</span><span class="sxs-lookup"><span data-stu-id="8f60d-553">PortableAssemblyName</span></span> | <span data-ttu-id="8f60d-554">Contoso.Microsoft.PaymentsSample</span><span class="sxs-lookup"><span data-stu-id="8f60d-554">Contoso.Microsoft.PaymentsSample</span></span> |
| <span data-ttu-id="8f60d-555">MerchantAccount</span><span class="sxs-lookup"><span data-stu-id="8f60d-555">MerchantAccount</span></span> | <span data-ttu-id="8f60d-556">ServiceAccountId</span><span class="sxs-lookup"><span data-stu-id="8f60d-556">ServiceAccountId</span></span> | <span data-ttu-id="8f60d-557">f35989c8-e571-4de1-862a-996c82a2e6b6</span><span class="sxs-lookup"><span data-stu-id="8f60d-557">f35989c8-e571-4de1-862a-996c82a2e6b6</span></span> |
| <span data-ttu-id="8f60d-558">MerchantAccount</span><span class="sxs-lookup"><span data-stu-id="8f60d-558">MerchantAccount</span></span> | <span data-ttu-id="8f60d-559">SupportedCurrencies</span><span class="sxs-lookup"><span data-stu-id="8f60d-559">SupportedCurrencies</span></span> | <span data-ttu-id="8f60d-560">AUD、BRL、CAD、CHF、CNY、CZK、DKK、EUR、GBP、HKD、HUF、INR、JPY、KPW、KRW、MXN、NOK、NZD、PLN、SEK、SGD、TWD、USD、ZAR</span><span class="sxs-lookup"><span data-stu-id="8f60d-560">AUD;BRL;CAD;CHF;CNY;CZK;DKK;EUR;GBP;HKD;HUF;INR;JPY;KPW;KRW;MXN;NOK;NZD;PLN;SEK;SGD;TWD;USD;ZAR</span></span> |
| <span data-ttu-id="8f60d-561">MerchantAccount</span><span class="sxs-lookup"><span data-stu-id="8f60d-561">MerchantAccount</span></span> | <span data-ttu-id="8f60d-562">SupportedTenderTypes</span><span class="sxs-lookup"><span data-stu-id="8f60d-562">SupportedTenderTypes</span></span> | <span data-ttu-id="8f60d-563">Visa;MasterCard;Amex;Discover;Debit</span><span class="sxs-lookup"><span data-stu-id="8f60d-563">Visa;MasterCard;Amex;Discover;Debit</span></span> |

<span data-ttu-id="8f60d-564">\* この列のサンプル値を、独自の支払プロセッサの固有値に置き換える **必要があります** 。</span><span class="sxs-lookup"><span data-stu-id="8f60d-564">\* You **must** replace the sample values in this column with unique values for your own payment processor.</span></span>

