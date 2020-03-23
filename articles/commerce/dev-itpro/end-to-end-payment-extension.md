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
ms.openlocfilehash: 359989e97bf902cf8cb835597ab971d2c3c76b02
ms.sourcegitcommit: 2464f371101ba616f472bab1631b0ecb863006ce
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/03/2020
ms.locfileid: "3095449"
---
# <a name="create-an-end-to-end-payment-integration-for-a-payment-terminal"></a><span data-ttu-id="fd721-103">支払端末のエンド・ツー・エンド支払統合を作成する</span><span class="sxs-lookup"><span data-stu-id="fd721-103">Create an end-to-end payment integration for a payment terminal</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="fd721-104">このトピックでは、支払ゲートウェイと直接通信できる支払端末向けに Microsoft Dynamics 365 Retail Modern POS とクラウド POS (POS) の支払統合を記述する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="fd721-104">This topic describes how to write a payment integration for Microsoft Dynamics 365 Retail Modern POS and Cloud POS (the POS) for a payment terminal that can directly communicate with the payment gateway.</span></span>

## <a name="key-terms"></a><span data-ttu-id="fd721-105">重要な用語</span><span class="sxs-lookup"><span data-stu-id="fd721-105">Key terms</span></span>

| <span data-ttu-id="fd721-106">期間</span><span class="sxs-lookup"><span data-stu-id="fd721-106">Term</span></span> | <span data-ttu-id="fd721-107">説明</span><span class="sxs-lookup"><span data-stu-id="fd721-107">Description</span></span> |
|---|---|
| <span data-ttu-id="fd721-108">支払コネクタ</span><span class="sxs-lookup"><span data-stu-id="fd721-108">Payment connector</span></span> | <span data-ttu-id="fd721-109">POS に支払ターミナルを統合するために書き込まれた拡張ライブラリです。</span><span class="sxs-lookup"><span data-stu-id="fd721-109">An extension library that is written to integrate the POS with a payment terminal.</span></span> |
| <span data-ttu-id="fd721-110">支払プロセッサ</span><span class="sxs-lookup"><span data-stu-id="fd721-110">Payment processor</span></span> | <span data-ttu-id="fd721-111">支払コネクタで使用される商社プロパティを取得するために書き込まれる拡張ライブラリです。</span><span class="sxs-lookup"><span data-stu-id="fd721-111">An extension library that is written to retrieve merchant properties that the payment connector uses.</span></span> |

## <a name="overview"></a><span data-ttu-id="fd721-112">概要</span><span class="sxs-lookup"><span data-stu-id="fd721-112">Overview</span></span>
<span data-ttu-id="fd721-113">次の図は、POS を介した支払ターミナルの統合の概要を示しています。</span><span class="sxs-lookup"><span data-stu-id="fd721-113">The following illustration shows a high-level overview of the payment terminal integration through the POS.</span></span> <span data-ttu-id="fd721-114">この図では、ローカルのハードウェア ステーションを使用して支払端末と通信を使用することを前提にしていますが、同じパターンを共有のハードウェア ステーションにも適用できます。</span><span class="sxs-lookup"><span data-stu-id="fd721-114">Although this illustration assumes that a local Hardware Station is used to communicate with the payment terminal, the same patterns apply to a shared Hardware Station.</span></span>

![支払コネクタ統合の概要](media/PAYMENTS/PAYMENT-TERMINAL/Overview.jpg)

<span data-ttu-id="fd721-116">このトピックでは、支払端末のエンド・ツー・エンド支払統合を作成するために必要な以下の手順について説明します。</span><span class="sxs-lookup"><span data-stu-id="fd721-116">This topic describes the following steps that are required to create an end-to-end payment integration for a payment terminal:</span></span>

- <span data-ttu-id="fd721-117">**[支払コネクタの記述](#write-a-payment-connector):** 支払コネクタは POS と支払ターミナルの間の主要な統合ポイントです。</span><span class="sxs-lookup"><span data-stu-id="fd721-117">**[Write a payment connector](#write-a-payment-connector):** The payment connector is the main integration point between the POS and the payment terminal.</span></span> <span data-ttu-id="fd721-118">このステップのセクションでは、支払要求 (たとえば、承認、払い戻し、無効化要求) を支払端末に中継できる、新しい支払コネクタを実装し、設定する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="fd721-118">The section for this step describes how to implement and configure a new payment connector that can relay payment requests (for example, authorize, refund, and void requests) to the payment terminal.</span></span> 
- <span data-ttu-id="fd721-119">**[支払プロセッサの記述](#write-a-payment-processor):** 支払プロセッサは、支払の統合の一部として使用される商社プロパティを定義するために使用します。</span><span class="sxs-lookup"><span data-stu-id="fd721-119">**[Write a payment processor](#write-a-payment-processor):** The payment processor is used to define the merchant properties that are used as part of the payment integration.</span></span> <span data-ttu-id="fd721-120">このステップのセクションでは、新しい支払プロセッサを実装する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="fd721-120">The section for this step describes how to implement a new payment processor.</span></span> <span data-ttu-id="fd721-121">これには、実装する必要があるインターフェイスおよび従う必要があるパターンに関する情報が含まれています。</span><span class="sxs-lookup"><span data-stu-id="fd721-121">It includes information about the interfaces that you should implement and patterns that you should follow.</span></span>

## <a name="write-a-payment-connector"></a><span data-ttu-id="fd721-122">支払コネクタの記述</span><span class="sxs-lookup"><span data-stu-id="fd721-122">Write a payment connector</span></span>
<span data-ttu-id="fd721-123">次のこのセクションでは、新しい支払コネクタを記述する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="fd721-123">This section describes how to write a new payment connector.</span></span>

### <a name="understanding-the-payment-flows"></a><span data-ttu-id="fd721-124">支払フローを理解する</span><span class="sxs-lookup"><span data-stu-id="fd721-124">Understanding the payment flows</span></span>
<span data-ttu-id="fd721-125">次の図は、POS、ハードウェア ステーション、および支払コネクタ全体にわたるいくつかの支払フロー (トランザクションの開始、カート ラインの更新、承認、キャプチャ、および終了トランザクション) の概要を示しています。</span><span class="sxs-lookup"><span data-stu-id="fd721-125">The following illustration shows a high-level overview of several payment flows (Begin Transaction, Update Cart Lines, Authorize, Capture, and End Transaction) across the POS, Hardware Station, and payment connector.</span></span>

![支払フローの概要](media/PAYMENTS/PAYMENT-TERMINAL/PaymentFlow.jpg)

### <a name="implement-a-payment-connector"></a><span data-ttu-id="fd721-127">支払コネクタの実装</span><span class="sxs-lookup"><span data-stu-id="fd721-127">Implement a payment connector</span></span>
<span data-ttu-id="fd721-128">次のこのセクションでは、新しい支払コネクタを実装する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="fd721-128">This section below describes how to implement a new payment connector.</span></span> <span data-ttu-id="fd721-129">ここに示す例は、Retailソフトウェアの開発キット (SDK) の **SampleExtensions\HardwareStation\Extension.PaymentSample** フォルダーにある **PaymentDeviceSample** クラスにあります。</span><span class="sxs-lookup"><span data-stu-id="fd721-129">The examples that are shown here can be found in the **PaymentDeviceSample** class that is located under the **SampleExtensions\HardwareStation\Extension.PaymentSample** folder in the Retail software development kit (SDK).</span></span>

#### <a name="implement-the-inamedrequesthandler-interface"></a><span data-ttu-id="fd721-130">INamedRequestHandler インターフェイスの実装</span><span class="sxs-lookup"><span data-stu-id="fd721-130">Implement the INamedRequestHandler interface</span></span>
<span data-ttu-id="fd721-131">すべての POS 支払関連フローは、ハードウェア ステーションで要求/応答パターンを通じて処理されます。</span><span class="sxs-lookup"><span data-stu-id="fd721-131">All POS payment-related flows are handled through request/response patterns in the Hardware Station.</span></span> <span data-ttu-id="fd721-132">新しい支払コネクタを作成するプロセスの第一歩は、**Microsoft.Dynamics.Commerce.Runtime.Framework** ライブラリで定義されている **INamedRequestHandler** インターフェイスを実装するクラスを作成することです。</span><span class="sxs-lookup"><span data-stu-id="fd721-132">The first step in the process of writing a new payment connector is to create a class that implements the **INamedRequestHandler** interface that is defined in the **Microsoft.Dynamics.Commerce.Runtime.Framework** library.</span></span>

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

<span data-ttu-id="fd721-133">**HandlerName** 文字列は、クライアントを通して特定の POS で使用される支払コネクタを構成するために使用されます (このトピックの後半の情報を参照してください)。</span><span class="sxs-lookup"><span data-stu-id="fd721-133">The **HandlerName** string is used to configure the payment connector that is used on a given POS register through the client (see the information later in this topic).</span></span>

#### <a name="implement-supported-payment-requests"></a><span data-ttu-id="fd721-134">サポートされている支払要求の実装</span><span class="sxs-lookup"><span data-stu-id="fd721-134">Implement supported payment requests</span></span>
<span data-ttu-id="fd721-135">支払関連フローを処理するには、支払コネクタが処理できる、サポートされている要求タイプを定義する必要があります。</span><span class="sxs-lookup"><span data-stu-id="fd721-135">To process payment-related flows, the payment connector must define the supported request types that it can handle.</span></span> <span data-ttu-id="fd721-136">また、**実行**メソッドは、コネクタが指定されたメソッドをサポートする各要求をルーティングするために実装する必要があります。</span><span class="sxs-lookup"><span data-stu-id="fd721-136">Additionally, the **Execute** method must be implemented to route each request that the connector supports to a given method.</span></span> <span data-ttu-id="fd721-137">次の例は、サポートされている要求のタイプの完全な一覧と、特定の要求 (すなわち、承認要求) の例を示しています。</span><span class="sxs-lookup"><span data-stu-id="fd721-137">The following example shows the complete list of supported request types and an example of a specific request (that is, an authorize request).</span></span>

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
                        typeof(LockPaymentTerminalDeviceRequest),
                        typeof(OpenPaymentTerminalDeviceRequest),
                        typeof(ClosePaymentTerminalDeviceRequest),
                        typeof(BeginTransactionPaymentTerminalDeviceRequest),
                        typeof(EndTransactionPaymentTerminalDeviceRequest),
                        typeof(UpdateLineItemsPaymentTerminalDeviceRequest),
                        typeof(AuthorizePaymentTerminalDeviceRequest),
                        typeof(CapturePaymentTerminalDeviceRequest),
                        typeof(VoidPaymentTerminalDeviceRequest),
                        typeof(RefundPaymentTerminalDeviceRequest),
                        typeof(FetchTokenPaymentTerminalDeviceRequest),
                        typeof(ExecuteTaskPaymentTerminalDeviceRequest),
                        typeof(ActivateGiftCardPaymentTerminalRequest),
                        typeof(AddBalanceToGiftCardPaymentTerminalRequest),
                        typeof(GetGiftCardBalancePaymentTerminalRequest),
                        typeof(GetPrivateTenderPaymentTerminalDeviceRequest),
                        typeof(CancelOperationPaymentTerminalDeviceRequest),
                        typeof(GetTransactionReferencePaymentTerminalDeviceRequest),
                        typeof(GetTransactionByTransactionReferencePaymentTerminalDeviceRequest),
                        typeof(CashoutGiftCardPaymentTerminalRequest)
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

#### <a name="full-list-of-supported-request-types"></a><span data-ttu-id="fd721-138">サポートされる要求タイプの完全な一覧</span><span class="sxs-lookup"><span data-stu-id="fd721-138">Full list of supported request types</span></span>
<span data-ttu-id="fd721-139">次のテーブルは、支払コネクタが実装できるサポートされているすべての要求のタイプを示しています。</span><span class="sxs-lookup"><span data-stu-id="fd721-139">The following table describes all supported requests types that a payment connector can implement.</span></span>

| <span data-ttu-id="fd721-140">クラスのリクエスト</span><span class="sxs-lookup"><span data-stu-id="fd721-140">Request class</span></span> | <span data-ttu-id="fd721-141">支払フローの説明</span><span class="sxs-lookup"><span data-stu-id="fd721-141">Payment flow description</span></span> |
|---|---|
| <span data-ttu-id="fd721-142">OpenPaymentTerminalDeviceRequest</span><span class="sxs-lookup"><span data-stu-id="fd721-142">OpenPaymentTerminalDeviceRequest</span></span> | <span data-ttu-id="fd721-143">この要求は、販売取引が開始される前に呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="fd721-143">This request is called before a sales transaction is initiated.</span></span> <span data-ttu-id="fd721-144">支払ターミナルへの接続を確立するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="fd721-144">It is used to establish a connection to the payment terminal.</span></span> |
| <span data-ttu-id="fd721-145">BeginTransactionPaymentTerminalDeviceRequest</span><span class="sxs-lookup"><span data-stu-id="fd721-145">BeginTransactionPaymentTerminalDeviceRequest</span></span> | <span data-ttu-id="fd721-146">この要求は、新しい販売取引が開始されたときに呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="fd721-146">This request is called when a new sales transaction is initiated.</span></span> <span data-ttu-id="fd721-147">支払ターミナルで初期化を処理するために使用されます (たとえば、トランザクション画面の初期化)。</span><span class="sxs-lookup"><span data-stu-id="fd721-147">It is used to handle any initialization on the payment terminal (for example, by initializing the transaction screen).</span></span> |
| <span data-ttu-id="fd721-148">LockPaymentTerminalDeviceRequest</span><span class="sxs-lookup"><span data-stu-id="fd721-148">LockPaymentTerminalDeviceRequest</span></span> | <span data-ttu-id="fd721-149">この要求は支払ターミナルがトランザクションに対してロックされている場合、呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="fd721-149">This request is called when a payment terminal is locked for a transaction.</span></span> |
| <span data-ttu-id="fd721-150">UpdateLineItemsPaymentTerminalDeviceRequest</span><span class="sxs-lookup"><span data-stu-id="fd721-150">UpdateLineItemsPaymentTerminalDeviceRequest</span></span> | <span data-ttu-id="fd721-151">この要求は、カート内の明細行品目が更新されたときに呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="fd721-151">This request is called when line items in the cart are updated.</span></span> |
| <span data-ttu-id="fd721-152">AuthorizePaymentTerminalDeviceRequest</span><span class="sxs-lookup"><span data-stu-id="fd721-152">AuthorizePaymentTerminalDeviceRequest</span></span> | <span data-ttu-id="fd721-153">この要求は、POS 支払ビューで支払が開始されたときに呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="fd721-153">This request is called when a payment is initiated in the POS payment view.</span></span> |
| <span data-ttu-id="fd721-154">CancelOperationPaymentTerminalDeviceRequest</span><span class="sxs-lookup"><span data-stu-id="fd721-154">CancelOperationPaymentTerminalDeviceRequest</span></span> | <span data-ttu-id="fd721-155">この要求は、支払いが開始された後、支払い端末で支払いが完了する前に、支払いビュー ダイアログ ボックスで **キャンセル** ボタンを選択すると呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="fd721-155">This request is called when a user selects the **Cancel** button in the payment view dialog box after the payment is initiated but before the payment is completed on the payment terminal.</span></span> |
| <span data-ttu-id="fd721-156">CapturePaymentTerminalDeviceRequest</span><span class="sxs-lookup"><span data-stu-id="fd721-156">CapturePaymentTerminalDeviceRequest</span></span> | <span data-ttu-id="fd721-157">この要求は、カート内の全額が支払われた時点で、販売取引が終了する前に、各支払い行に対して呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="fd721-157">This request is called for each payment line when the whole amount in the cart is paid but before the sales transaction is concluded.</span></span> |
| <span data-ttu-id="fd721-158">VoidPaymentTerminalDeviceRequest</span><span class="sxs-lookup"><span data-stu-id="fd721-158">VoidPaymentTerminalDeviceRequest</span></span> | <span data-ttu-id="fd721-159">この要求は、カート内の支払い行が無効になったときに呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="fd721-159">This request is called when a payment line is voided in the cart.</span></span> |
| <span data-ttu-id="fd721-160">RefundPaymentTerminalDeviceRequest</span><span class="sxs-lookup"><span data-stu-id="fd721-160">RefundPaymentTerminalDeviceRequest</span></span> | <span data-ttu-id="fd721-161">この要求は、払い戻しが行われたときに呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="fd721-161">This request is called when a refund is issued.</span></span> |
| <span data-ttu-id="fd721-162">FetchTokenPaymentTerminalDeviceRequest</span><span class="sxs-lookup"><span data-stu-id="fd721-162">FetchTokenPaymentTerminalDeviceRequest</span></span> | <span data-ttu-id="fd721-163">この要求は、顧客注文の繰延支払いをサポートするために支払トークンをフェッチするために呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="fd721-163">This request is called to fetch a payment token to support deferred payments for customer orders.</span></span> |
| <span data-ttu-id="fd721-164">EndTransactionPaymentTerminalDeviceRequest</span><span class="sxs-lookup"><span data-stu-id="fd721-164">EndTransactionPaymentTerminalDeviceRequest</span></span> | <span data-ttu-id="fd721-165">この要求は、販売取引が終了し、すべての支払いが取り込まれたときに呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="fd721-165">This request is called when the sales transaction is concluded and all payments have been captured.</span></span> |
| <span data-ttu-id="fd721-166">ClosePaymentTerminalDeviceRequest</span><span class="sxs-lookup"><span data-stu-id="fd721-166">ClosePaymentTerminalDeviceRequest</span></span> | <span data-ttu-id="fd721-167">この要求は、販売取引の終了後に呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="fd721-167">This request is called after the sales transaction is concluded.</span></span> <span data-ttu-id="fd721-168">支払ターミナルへの接続を閉じるために使用されます。</span><span class="sxs-lookup"><span data-stu-id="fd721-168">It is used to close the connection to the payment terminal.</span></span> |
| <span data-ttu-id="fd721-169">ActivateGiftCardPaymentTerminalRequest</span><span class="sxs-lookup"><span data-stu-id="fd721-169">ActivateGiftCardPaymentTerminalRequest</span></span> | <span data-ttu-id="fd721-170">この要求は、外部ギフト カードが POS を介して有効化されているときに呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="fd721-170">This request is called when an external gift card is being activated through the POS.</span></span> |
| <span data-ttu-id="fd721-171">AddBalanceToGiftCardPaymentTerminalRequest</span><span class="sxs-lookup"><span data-stu-id="fd721-171">AddBalanceToGiftCardPaymentTerminalRequest</span></span> | <span data-ttu-id="fd721-172">この要求は、外部ギフト カードに残高が追加されるときに呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="fd721-172">This request is called when a balance is being added to an external gift card.</span></span> |
| <span data-ttu-id="fd721-173">GetGiftCardBalancePaymentTerminalRequest</span><span class="sxs-lookup"><span data-stu-id="fd721-173">GetGiftCardBalancePaymentTerminalRequest</span></span> | <span data-ttu-id="fd721-174">この要求は、ギフト カードの残高が取得されるときに呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="fd721-174">This request is called when the balance on the gift card is being retrieved.</span></span> |
| <span data-ttu-id="fd721-175">GetPrivateTenderPaymentTerminalDeviceRequest</span><span class="sxs-lookup"><span data-stu-id="fd721-175">GetPrivateTenderPaymentTerminalDeviceRequest</span></span> | <span data-ttu-id="fd721-176">この要求は、ギフト カード番号がギフト カード フローの支払い端末から取得されたときに呼び出されます (ギフト カードの発行、ギフト カードによる支払い、ギフト カードへの追加など)。</span><span class="sxs-lookup"><span data-stu-id="fd721-176">This request is called when gift card numbers are retrieved from the payment terminal for gift card flows (for example, Issue gift card, Pay by gift card, or Add to gift card).</span></span> |
| <span data-ttu-id="fd721-177">ExecuteTaskPaymentTerminalDeviceRequest</span><span class="sxs-lookup"><span data-stu-id="fd721-177">ExecuteTaskPaymentTerminalDeviceRequest</span></span> | <span data-ttu-id="fd721-178">この拡張要求は、カスタマイズを介して POS から呼び出すことができます。</span><span class="sxs-lookup"><span data-stu-id="fd721-178">This extension request can be invoked from the POS through customizations.</span></span> <span data-ttu-id="fd721-179">支払に関連する追加のフローを有効にするために使用されます。</span><span class="sxs-lookup"><span data-stu-id="fd721-179">It is used to enable additional payment-related flows.</span></span> |
| <span data-ttu-id="fd721-180">GetTransactionReferencePaymentTerminalDeviceRequest</span><span class="sxs-lookup"><span data-stu-id="fd721-180">GetTransactionReferencePaymentTerminalDeviceRequest</span></span> | <span data-ttu-id="fd721-181">この要求は、相関する ID をチェックするために呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="fd721-181">This request is called to check the correlation ID.</span></span> <span data-ttu-id="fd721-182">重複した支払を回避するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="fd721-182">It is used for duplicate payment protection.</span></span> |
| <span data-ttu-id="fd721-183">GetTransactionByTransactionReferencePaymentTerminalDeviceRequest</span><span class="sxs-lookup"><span data-stu-id="fd721-183">GetTransactionByTransactionReferencePaymentTerminalDeviceRequest</span></span> | <span data-ttu-id="fd721-184">この要求は、相関する ID を使用して前の取引を取得するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="fd721-184">This request is used to obtain the previous transaction by correlation ID.</span></span> |
| <span data-ttu-id="fd721-185">CashoutGiftCardPaymentTerminalRequest</span><span class="sxs-lookup"><span data-stu-id="fd721-185">CashoutGiftCardPaymentTerminalRequest</span></span> | <span data-ttu-id="fd721-186">この要求は、POS からキャッシュ アウト ギフト カード処理が実行されたときに呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="fd721-186">This request is called when a the cash out gift card operation is executed from the POS.</span></span> |



##### <a name="openpaymentterminaldevicerequest"></a><span data-ttu-id="fd721-187">OpenPaymentTerminalDeviceRequest</span><span class="sxs-lookup"><span data-stu-id="fd721-187">OpenPaymentTerminalDeviceRequest</span></span>
###### <a name="signature"></a><span data-ttu-id="fd721-188">署名</span><span class="sxs-lookup"><span data-stu-id="fd721-188">Signature</span></span>
``` csharp
public OpenPaymentTerminalDeviceRequest(string token, string deviceName, SettingsInfo terminalSettings, PeripheralConfiguration deviceConfig, ExtensionTransaction extensionTransactionProperties);
```

###### <a name="variables"></a><span data-ttu-id="fd721-189">変数</span><span class="sxs-lookup"><span data-stu-id="fd721-189">Variables</span></span>

| <span data-ttu-id="fd721-190">変動</span><span class="sxs-lookup"><span data-stu-id="fd721-190">Variable</span></span> | <span data-ttu-id="fd721-191">説明</span><span class="sxs-lookup"><span data-stu-id="fd721-191">Description</span></span> |
|---|---|
| <span data-ttu-id="fd721-192">token</span><span class="sxs-lookup"><span data-stu-id="fd721-192">token</span></span> | <span data-ttu-id="fd721-193">支払い端末が最初のトランザクションのためにロックされたときに生成される一意のトークン値。</span><span class="sxs-lookup"><span data-stu-id="fd721-193">The unique token value that is generated when the payment terminal is initially locked for the transaction.</span></span> |
| <span data-ttu-id="fd721-194">deviceName</span><span class="sxs-lookup"><span data-stu-id="fd721-194">deviceName</span></span> | <span data-ttu-id="fd721-195">クライアントの **POS ハードウェア プロファイル** ページで定義されている、デバイスの名前。</span><span class="sxs-lookup"><span data-stu-id="fd721-195">The name of the device, as defined on the **POS hardware profile** page in the client.</span></span> |
| <span data-ttu-id="fd721-196">terminalSettings</span><span class="sxs-lookup"><span data-stu-id="fd721-196">terminalSettings</span></span> | <span data-ttu-id="fd721-197">クライアントで定義された支払端末固有の構成プロパティのセット。署名キャプチャの最小額やデビット キャッシュバック限度などです。</span><span class="sxs-lookup"><span data-stu-id="fd721-197">The set of payment terminal–specific configuration properties that are defined in the client, such as the minimum amount for signature capture and the debit cash-back limit.</span></span> |
| <span data-ttu-id="fd721-198">deviceConfig</span><span class="sxs-lookup"><span data-stu-id="fd721-198">deviceConfig</span></span> | <span data-ttu-id="fd721-199">ネットワーク端末の場合の IP アドレスやポートなど、名前/値のペアの形式の支払端末固有の設定プロパティのセット。</span><span class="sxs-lookup"><span data-stu-id="fd721-199">The set of payment terminal–specific configuration properties in the form of name/value pairs, such as the IP address and port in the case of network devices.</span></span> |
| <span data-ttu-id="fd721-200">extensionTransactionProperties</span><span class="sxs-lookup"><span data-stu-id="fd721-200">extensionTransactionProperties</span></span> | <span data-ttu-id="fd721-201">名前/値のペアの形式の拡張構成プロパティのセット。</span><span class="sxs-lookup"><span data-stu-id="fd721-201">The set of extension configuration properties in the form of name/value pairs.</span></span> |

##### <a name="begintransactionpaymentterminaldevicerequest"></a><span data-ttu-id="fd721-202">BeginTransactionPaymentTerminalDeviceRequest</span><span class="sxs-lookup"><span data-stu-id="fd721-202">BeginTransactionPaymentTerminalDeviceRequest</span></span>
###### <a name="signature"></a><span data-ttu-id="fd721-203">署名</span><span class="sxs-lookup"><span data-stu-id="fd721-203">Signature</span></span>
``` csharp
public BeginTransactionPaymentTerminalDeviceRequest(string token, string paymentConnectorName, string merchantInformation, string invoiceNumber, bool isTestMode, ExtensionTransaction extensionTransactionProperties)
```

###### <a name="variables"></a><span data-ttu-id="fd721-204">変数</span><span class="sxs-lookup"><span data-stu-id="fd721-204">Variables</span></span>

| <span data-ttu-id="fd721-205">変動</span><span class="sxs-lookup"><span data-stu-id="fd721-205">Variable</span></span> | <span data-ttu-id="fd721-206">説明</span><span class="sxs-lookup"><span data-stu-id="fd721-206">Description</span></span> |
|---|---|
| <span data-ttu-id="fd721-207">token</span><span class="sxs-lookup"><span data-stu-id="fd721-207">token</span></span> | <span data-ttu-id="fd721-208">支払い端末が最初のトランザクションのためにロックされたときに生成される一意のトークン値。</span><span class="sxs-lookup"><span data-stu-id="fd721-208">The unique token value that is generated when the payment terminal is initially locked for the transaction.</span></span> |
| <span data-ttu-id="fd721-209">paymentConnectorName</span><span class="sxs-lookup"><span data-stu-id="fd721-209">paymentConnectorName</span></span> | <span data-ttu-id="fd721-210">支払フローの一部として使用される支払コネクタの名前。</span><span class="sxs-lookup"><span data-stu-id="fd721-210">The name of the payment connector that is used as part of the payment flow.</span></span> <span data-ttu-id="fd721-211">この変数は、**IPaymentProcessor** インターフェイスを使用する支払フローと統合する予定がある場合に使用されます。</span><span class="sxs-lookup"><span data-stu-id="fd721-211">This variable is used if you plan to integrate with payment flows that use the **IPaymentProcessor** interface.</span></span> |
| <span data-ttu-id="fd721-212">merchantInformation</span><span class="sxs-lookup"><span data-stu-id="fd721-212">merchantInformation</span></span> | <span data-ttu-id="fd721-213">クライアントの **POS ハードウェア プロファイル** ページで定義されている商社情報。</span><span class="sxs-lookup"><span data-stu-id="fd721-213">The merchant information that is defined on the **POS hardware profile** page in the client.</span></span> |
| <span data-ttu-id="fd721-214">invoiceNumber</span><span class="sxs-lookup"><span data-stu-id="fd721-214">invoiceNumber</span></span> | <span data-ttu-id="fd721-215">POS が販売トランザクションを追跡するために生成する一意の請求書番号。</span><span class="sxs-lookup"><span data-stu-id="fd721-215">The unique invoice number that the POS generates to track the sales transaction.</span></span> |
| <span data-ttu-id="fd721-216">isTestMode</span><span class="sxs-lookup"><span data-stu-id="fd721-216">isTestMode</span></span> | <span data-ttu-id="fd721-217">支払コネクタがテスト モードで使用されているかどうかを示す値。</span><span class="sxs-lookup"><span data-stu-id="fd721-217">A value that indicates whether the payment connector is being used in testing mode.</span></span> |
| <span data-ttu-id="fd721-218">extensionTransactionProperties</span><span class="sxs-lookup"><span data-stu-id="fd721-218">extensionTransactionProperties</span></span> | <span data-ttu-id="fd721-219">名前/値のペアの形式の拡張構成プロパティのセット。</span><span class="sxs-lookup"><span data-stu-id="fd721-219">The set of extension configuration properties in the form of name/value pairs.</span></span> |

##### <a name="lockpaymentterminaldevicerequest"></a><span data-ttu-id="fd721-220">LockPaymentTerminalDeviceRequest</span><span class="sxs-lookup"><span data-stu-id="fd721-220">LockPaymentTerminalDeviceRequest</span></span>
###### <a name="signature"></a><span data-ttu-id="fd721-221">署名</span><span class="sxs-lookup"><span data-stu-id="fd721-221">Signature</span></span>
``` csharp
public LockPaymentTerminalDeviceRequest(string clientDeviceNumber, string deviceType, string deviceName, bool isExclusive, bool isOverride)
```

###### <a name="variables"></a><span data-ttu-id="fd721-222">変数</span><span class="sxs-lookup"><span data-stu-id="fd721-222">Variables</span></span>

| <span data-ttu-id="fd721-223">変動</span><span class="sxs-lookup"><span data-stu-id="fd721-223">Variable</span></span> | <span data-ttu-id="fd721-224">説明</span><span class="sxs-lookup"><span data-stu-id="fd721-224">Description</span></span> |
|---|---|
| <span data-ttu-id="fd721-225">clientDeviceNumber</span><span class="sxs-lookup"><span data-stu-id="fd721-225">clientDeviceNumber</span></span> | <span data-ttu-id="fd721-226">ロックに使用される固有の POS デバイス番号</span><span class="sxs-lookup"><span data-stu-id="fd721-226">The unique POS device number that is acquiring the lock.</span></span> |
| <span data-ttu-id="fd721-227">deviceType</span><span class="sxs-lookup"><span data-stu-id="fd721-227">deviceType</span></span> | <span data-ttu-id="fd721-228">POS ハードウェア プロファイル (「Windows」など) で構成されるようにロックを取得したデバイス タイプ。</span><span class="sxs-lookup"><span data-stu-id="fd721-228">The device type that the lock is acquired for as configured in the POS hardware profile (such as "Windows").</span></span> |
| <span data-ttu-id="fd721-229">deviceName</span><span class="sxs-lookup"><span data-stu-id="fd721-229">deviceName</span></span> | <span data-ttu-id="fd721-230">POS ハードウェア プロファイル (「MOCKPAYMENTTERMINAL」など) で構成されるようにロックを取得したデバイス タイプ。</span><span class="sxs-lookup"><span data-stu-id="fd721-230">The device type that the lock is acquired for as configured in the POS hardware profile (such as "MOCKPAYMENTTERMINAL").</span></span> |
| <span data-ttu-id="fd721-231">isExclusive</span><span class="sxs-lookup"><span data-stu-id="fd721-231">isExclusive</span></span> | <span data-ttu-id="fd721-232">取得したロックが占有されているかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="fd721-232">Determines whether the lock that is acquired is exclusive.</span></span> | 
| <span data-ttu-id="fd721-233">isOverride</span><span class="sxs-lookup"><span data-stu-id="fd721-233">isOverride</span></span> | <span data-ttu-id="fd721-234">この要求が、既存のロックを上書きするかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="fd721-234">Determines whether this request will override any existing lock.</span></span> |

##### <a name="updatelineitemspaymentterminaldevicerequest"></a><span data-ttu-id="fd721-235">UpdateLineItemsPaymentTerminalDeviceRequest</span><span class="sxs-lookup"><span data-stu-id="fd721-235">UpdateLineItemsPaymentTerminalDeviceRequest</span></span>
###### <a name="signature"></a><span data-ttu-id="fd721-236">署名</span><span class="sxs-lookup"><span data-stu-id="fd721-236">Signature</span></span>
``` csharp
public UpdateLineItemsPaymentTerminalDeviceRequest(string token, string totalAmount, string taxAmount, string discountAmount, string subTotalAmount, IEnumerable<ItemInfo> items, ExtensionTransaction extensionTransactionProperties = null)
```

###### <a name="variables"></a><span data-ttu-id="fd721-237">変数</span><span class="sxs-lookup"><span data-stu-id="fd721-237">Variables</span></span>

| <span data-ttu-id="fd721-238">変動</span><span class="sxs-lookup"><span data-stu-id="fd721-238">Variable</span></span> | <span data-ttu-id="fd721-239">説明</span><span class="sxs-lookup"><span data-stu-id="fd721-239">Description</span></span> |
|---|---|
| <span data-ttu-id="fd721-240">token</span><span class="sxs-lookup"><span data-stu-id="fd721-240">token</span></span> | <span data-ttu-id="fd721-241">支払い端末が最初のトランザクションのためにロックされたときに生成される一意のトークン値。</span><span class="sxs-lookup"><span data-stu-id="fd721-241">The unique token value that is generated when the payment terminal is initially locked for the transaction.</span></span> |
| <span data-ttu-id="fd721-242">totalAmount</span><span class="sxs-lookup"><span data-stu-id="fd721-242">totalAmount</span></span> | <span data-ttu-id="fd721-243">現在の販売トランザクションでの合計金額。</span><span class="sxs-lookup"><span data-stu-id="fd721-243">The total amount on the current sales transaction.</span></span> |
| <span data-ttu-id="fd721-244">taxAmount</span><span class="sxs-lookup"><span data-stu-id="fd721-244">taxAmount</span></span> | <span data-ttu-id="fd721-245">現在の販売トランザクションでの税金額。</span><span class="sxs-lookup"><span data-stu-id="fd721-245">The tax amount on the current sales transaction.</span></span> |
| <span data-ttu-id="fd721-246">discountAmount</span><span class="sxs-lookup"><span data-stu-id="fd721-246">discountAmount</span></span> | <span data-ttu-id="fd721-247">現在の販売トランザクションでの割引金額。</span><span class="sxs-lookup"><span data-stu-id="fd721-247">The discount amount on the current sales transaction.</span></span> |
| <span data-ttu-id="fd721-248">subTotalAmount</span><span class="sxs-lookup"><span data-stu-id="fd721-248">subTotalAmount</span></span> | <span data-ttu-id="fd721-249">現在の販売トランザクションでの小計金額。</span><span class="sxs-lookup"><span data-stu-id="fd721-249">The subtotal amount on the current sales transaction.</span></span> |
| <span data-ttu-id="fd721-250">項目</span><span class="sxs-lookup"><span data-stu-id="fd721-250">items</span></span> | <span data-ttu-id="fd721-251">表示する明細行品目のリスト。</span><span class="sxs-lookup"><span data-stu-id="fd721-251">The list of line items to show.</span></span> |
| <span data-ttu-id="fd721-252">extensionTransactionProperties</span><span class="sxs-lookup"><span data-stu-id="fd721-252">extensionTransactionProperties</span></span> | <span data-ttu-id="fd721-253">名前/値のペアの形式の拡張構成プロパティのセット。</span><span class="sxs-lookup"><span data-stu-id="fd721-253">The set of extension configuration properties in the form of name/value pairs.</span></span> |

##### <a name="authorizepaymentterminaldevicerequest"></a><span data-ttu-id="fd721-254">AuthorizePaymentTerminalDeviceRequest</span><span class="sxs-lookup"><span data-stu-id="fd721-254">AuthorizePaymentTerminalDeviceRequest</span></span>
###### <a name="signature"></a><span data-ttu-id="fd721-255">署名</span><span class="sxs-lookup"><span data-stu-id="fd721-255">Signature</span></span>
``` csharp
public AuthorizePaymentTerminalDeviceRequest(string token, string paymentConnectorName, decimal amount, string currency, TenderInfo tenderInfo, string voiceAuthorization, bool isManualEntry, ExtensionTransaction extensionTransactionProperties)
```

###### <a name="variables"></a><span data-ttu-id="fd721-256">変数</span><span class="sxs-lookup"><span data-stu-id="fd721-256">Variables</span></span>

| <span data-ttu-id="fd721-257">変動</span><span class="sxs-lookup"><span data-stu-id="fd721-257">Variable</span></span> | <span data-ttu-id="fd721-258">説明</span><span class="sxs-lookup"><span data-stu-id="fd721-258">Description</span></span> |
|---|---|
| <span data-ttu-id="fd721-259">token</span><span class="sxs-lookup"><span data-stu-id="fd721-259">token</span></span> | <span data-ttu-id="fd721-260">支払い端末が最初のトランザクションのためにロックされたときに生成される一意のトークン値。</span><span class="sxs-lookup"><span data-stu-id="fd721-260">The unique token value that is generated when the payment terminal is initially locked for the transaction.</span></span> |
| <span data-ttu-id="fd721-261">paymentConnectorName</span><span class="sxs-lookup"><span data-stu-id="fd721-261">paymentConnectorName</span></span> | <span data-ttu-id="fd721-262">支払フローの一部として使用される支払コネクタの名前。</span><span class="sxs-lookup"><span data-stu-id="fd721-262">The name of the payment connector that is used as part of the payment flow.</span></span> <span data-ttu-id="fd721-263">この変数は、**IPaymentProcessor** インターフェイスを使用する支払フローとの統合がある場合に使用されます。</span><span class="sxs-lookup"><span data-stu-id="fd721-263">This variable is used if there is an integration with payment flows that use the **IPaymentProcessor** interface.</span></span> |
| <span data-ttu-id="fd721-264">金額</span><span class="sxs-lookup"><span data-stu-id="fd721-264">amount</span></span> | <span data-ttu-id="fd721-265">承認する金額。</span><span class="sxs-lookup"><span data-stu-id="fd721-265">The amount to authorize.</span></span> |
| <span data-ttu-id="fd721-266">通貨</span><span class="sxs-lookup"><span data-stu-id="fd721-266">currency</span></span> | <span data-ttu-id="fd721-267">承認する金額の通貨。</span><span class="sxs-lookup"><span data-stu-id="fd721-267">The currency for the amount to authorize.</span></span> |
| <span data-ttu-id="fd721-268">tenderInfo</span><span class="sxs-lookup"><span data-stu-id="fd721-268">tenderInfo</span></span> | <span data-ttu-id="fd721-269">外部ソースから取得された POS から送信されるカード情報 (外部ソースがある場合)。</span><span class="sxs-lookup"><span data-stu-id="fd721-269">The card information that is sent from the POS that is retrieved from an external source (if an external source is present).</span></span> |
| <span data-ttu-id="fd721-270">voiceAuthorization</span><span class="sxs-lookup"><span data-stu-id="fd721-270">voiceAuthorization</span></span> | <span data-ttu-id="fd721-271">音声認証が必要な場合は、POS から送信される音声承認コード。</span><span class="sxs-lookup"><span data-stu-id="fd721-271">The voice approval code that is sent from the POS if voice authorization is required.</span></span> |
| <span data-ttu-id="fd721-272">isManualEntry</span><span class="sxs-lookup"><span data-stu-id="fd721-272">isManualEntry</span></span> | <span data-ttu-id="fd721-273">カード番号を手動で入力されたかどうかを定義する値。</span><span class="sxs-lookup"><span data-stu-id="fd721-273">A value that defines whether the card number was entered manually.</span></span> |
| <span data-ttu-id="fd721-274">extensionTransactionProperties</span><span class="sxs-lookup"><span data-stu-id="fd721-274">extensionTransactionProperties</span></span> | <span data-ttu-id="fd721-275">名前/値のペアの形式の拡張構成プロパティのセット。</span><span class="sxs-lookup"><span data-stu-id="fd721-275">The set of extension configuration properties in the form of name/value pairs.</span></span> |

###### <a name="response"></a><span data-ttu-id="fd721-276">応答</span><span class="sxs-lookup"><span data-stu-id="fd721-276">Response</span></span>
<span data-ttu-id="fd721-277">**AuthorizePaymentCardPaymentResponse** 応答オブジェクトは、**AuthorizePaymentTerminalDeviceRequest** 要求が処理されたときに返される必要があります。</span><span class="sxs-lookup"><span data-stu-id="fd721-277">The **AuthorizePaymentCardPaymentResponse** response object must be returned when the **AuthorizePaymentTerminalDeviceRequest** request is handled.</span></span> <span data-ttu-id="fd721-278">応答には、次の必須プロパティを持つ **PaymentInfo** オブジェクトのインスタンスが含まれている必要があります。</span><span class="sxs-lookup"><span data-stu-id="fd721-278">The response must contain an instance of the **PaymentInfo** object that has the following required properties.</span></span>

| <span data-ttu-id="fd721-279">プロパティ</span><span class="sxs-lookup"><span data-stu-id="fd721-279">Property</span></span> | <span data-ttu-id="fd721-280">説明</span><span class="sxs-lookup"><span data-stu-id="fd721-280">Description</span></span> |
|---|---|
| <span data-ttu-id="fd721-281">ApprovedAmount</span><span class="sxs-lookup"><span data-stu-id="fd721-281">ApprovedAmount</span></span> | <span data-ttu-id="fd721-282">トランザクションに対して承認された金額。</span><span class="sxs-lookup"><span data-stu-id="fd721-282">The amount that was approved for the transaction.</span></span> |
| <span data-ttu-id="fd721-283">CardNumberMasked</span><span class="sxs-lookup"><span data-stu-id="fd721-283">CardNumberMasked</span></span> | <span data-ttu-id="fd721-284">マスクされたクレジット カード番号。</span><span class="sxs-lookup"><span data-stu-id="fd721-284">The masked credit card number.</span></span> <span data-ttu-id="fd721-285">この値には、少なくとも POS 内の在庫置場範囲の参照をサポートするため、クレジット カードの最初の桁が含まれている必要があります。</span><span class="sxs-lookup"><span data-stu-id="fd721-285">The value must contain at least the first digit of the credit card to support bin range lookup in the POS.</span></span> <span data-ttu-id="fd721-286">(ほとんどのデバイスは、最初の 6 桁と最後の 4 桁を返します。)</span><span class="sxs-lookup"><span data-stu-id="fd721-286">(Most devices return the first six digits and the last four digits.)</span></span> |
| <span data-ttu-id="fd721-287">CardType</span><span class="sxs-lookup"><span data-stu-id="fd721-287">CardType</span></span> | <span data-ttu-id="fd721-288">**Microsoft.Dynamics.Commerce.HardwareStation.CardPayment.CardType** エンティティを使用して支払い (**クレジット** または **デビット** など) に使われたカードのタイプ。</span><span class="sxs-lookup"><span data-stu-id="fd721-288">The type of card that was used for the payment (for example, **Credit** or **Debit**) by using the **Microsoft.Dynamics.Commerce.HardwareStation.CardPayment.CardType** entity.</span></span> |
| <span data-ttu-id="fd721-289">CashbackAmount</span><span class="sxs-lookup"><span data-stu-id="fd721-289">CashbackAmount</span></span> | <span data-ttu-id="fd721-290">借方トランザクションの場合、キャッシュ バック金額は支払のターミナルで定義されました。</span><span class="sxs-lookup"><span data-stu-id="fd721-290">For debit transactions, the cash-back amount that was defined on the payment terminal.</span></span> |
| <span data-ttu-id="fd721-291">エラー</span><span class="sxs-lookup"><span data-stu-id="fd721-291">Errors</span></span> | <span data-ttu-id="fd721-292">承認呼び出し中に発生したエラーのリスト。</span><span class="sxs-lookup"><span data-stu-id="fd721-292">The list of errors that occurred during the authorize call.</span></span> |
| <span data-ttu-id="fd721-293">IsApproved</span><span class="sxs-lookup"><span data-stu-id="fd721-293">IsApproved</span></span> | <span data-ttu-id="fd721-294">支払が承認されたかどうかを示すフラグ。</span><span class="sxs-lookup"><span data-stu-id="fd721-294">A flag that indicates whether the payment was approved.</span></span> |
| <span data-ttu-id="fd721-295">PaymentSdkData</span><span class="sxs-lookup"><span data-stu-id="fd721-295">PaymentSdkData</span></span> | <span data-ttu-id="fd721-296">承認/返金と、キャプチャ/呼び出しの無効化またはクロスチャネルの支払操作の間の状態をサポートするために使用される応答データ。</span><span class="sxs-lookup"><span data-stu-id="fd721-296">The response data that is used to support state between the authorize/refund and capture/void calls or cross-channel payment operations.</span></span> |

<span data-ttu-id="fd721-297">**PaymentSdkData** プロパティには、次のデータを含める必要があります。</span><span class="sxs-lookup"><span data-stu-id="fd721-297">The **PaymentSdkData** property must contain the following data.</span></span>

| <span data-ttu-id="fd721-298">名前空間</span><span class="sxs-lookup"><span data-stu-id="fd721-298">Namespace</span></span> | <span data-ttu-id="fd721-299">氏名</span><span class="sxs-lookup"><span data-stu-id="fd721-299">Name</span></span> | <span data-ttu-id="fd721-300">説明</span><span class="sxs-lookup"><span data-stu-id="fd721-300">Description</span></span> | <span data-ttu-id="fd721-301">サンプル値</span><span class="sxs-lookup"><span data-stu-id="fd721-301">Sample value</span></span> |
|---|---|---|---|
| <span data-ttu-id="fd721-302">コネクタ</span><span class="sxs-lookup"><span data-stu-id="fd721-302">Connector</span></span> | <span data-ttu-id="fd721-303">ConnectorName</span><span class="sxs-lookup"><span data-stu-id="fd721-303">ConnectorName</span></span> | <span data-ttu-id="fd721-304">このトピックの後半にある「支払プロセッサの記述」セクションで説明している、トランザクションに使用される **IPaymentProcessor**インターフェイスの名前です。</span><span class="sxs-lookup"><span data-stu-id="fd721-304">The name of the **IPaymentProcessor** interface that is used for the transactions, as described in the "Write a payment processor" section later in this topic.</span></span> |
| <span data-ttu-id="fd721-305">AuthorizationResponse</span><span class="sxs-lookup"><span data-stu-id="fd721-305">AuthorizationResponse</span></span> | <span data-ttu-id="fd721-306">プロパティ</span><span class="sxs-lookup"><span data-stu-id="fd721-306">Properties</span></span> | <span data-ttu-id="fd721-307">承認応答のリスト。</span><span class="sxs-lookup"><span data-stu-id="fd721-307">The list of authorization responses.</span></span> | <span data-ttu-id="fd721-308">次の表を参照してください。</span><span class="sxs-lookup"><span data-stu-id="fd721-308">See the next table.</span></span> |

<span data-ttu-id="fd721-309">**PaymentSdkData** プロパティの **プロパティ** フィールドには、次のフィールドを含める必要があります。</span><span class="sxs-lookup"><span data-stu-id="fd721-309">The **Properties** field of the **PaymentSdkData** property must contain the following fields.</span></span>

| <span data-ttu-id="fd721-310">名前空間</span><span class="sxs-lookup"><span data-stu-id="fd721-310">Namespace</span></span> | <span data-ttu-id="fd721-311">氏名</span><span class="sxs-lookup"><span data-stu-id="fd721-311">Name</span></span> | <span data-ttu-id="fd721-312">説明</span><span class="sxs-lookup"><span data-stu-id="fd721-312">Description</span></span> | <span data-ttu-id="fd721-313">サンプル値</span><span class="sxs-lookup"><span data-stu-id="fd721-313">Sample value</span></span> |
|---|---|---|---|
| <span data-ttu-id="fd721-314">AuthorizationResponse</span><span class="sxs-lookup"><span data-stu-id="fd721-314">AuthorizationResponse</span></span> | <span data-ttu-id="fd721-315">ApprovedAmount</span><span class="sxs-lookup"><span data-stu-id="fd721-315">ApprovedAmount</span></span> | <span data-ttu-id="fd721-316">トランザクションに対して承認された金額。</span><span class="sxs-lookup"><span data-stu-id="fd721-316">The amount that was approved for the transaction.</span></span> | <span data-ttu-id="fd721-317">28.08 m</span><span class="sxs-lookup"><span data-stu-id="fd721-317">28.08m</span></span> |
| <span data-ttu-id="fd721-318">AuthorizationResponse</span><span class="sxs-lookup"><span data-stu-id="fd721-318">AuthorizationResponse</span></span> | <span data-ttu-id="fd721-319">AvailableBalance</span><span class="sxs-lookup"><span data-stu-id="fd721-319">AvailableBalance</span></span> | <span data-ttu-id="fd721-320">カードの使用可能な残高。</span><span class="sxs-lookup"><span data-stu-id="fd721-320">The available balance on the card.</span></span> | <span data-ttu-id="fd721-321">100.00m</span><span class="sxs-lookup"><span data-stu-id="fd721-321">100.00m</span></span> |
| <span data-ttu-id="fd721-322">AuthorizationResponse</span><span class="sxs-lookup"><span data-stu-id="fd721-322">AuthorizationResponse</span></span> | <span data-ttu-id="fd721-323">ApprovalCode</span><span class="sxs-lookup"><span data-stu-id="fd721-323">ApprovalCode</span></span> | <span data-ttu-id="fd721-324">トランザクションの承認コード。</span><span class="sxs-lookup"><span data-stu-id="fd721-324">The approval code for the transaction.</span></span> | <span data-ttu-id="fd721-325">Z123456</span><span class="sxs-lookup"><span data-stu-id="fd721-325">Z123456</span></span> |
| <span data-ttu-id="fd721-326">AuthorizationResponse</span><span class="sxs-lookup"><span data-stu-id="fd721-326">AuthorizationResponse</span></span> | <span data-ttu-id="fd721-327">ProviderTransactionId</span><span class="sxs-lookup"><span data-stu-id="fd721-327">ProviderTransactionId</span></span> | <span data-ttu-id="fd721-328">支払いプロバイダーのトランザクション識別子。</span><span class="sxs-lookup"><span data-stu-id="fd721-328">The transaction identifier of the payment provider.</span></span> | <span data-ttu-id="fd721-329">123456789</span><span class="sxs-lookup"><span data-stu-id="fd721-329">123456789</span></span> |
| <span data-ttu-id="fd721-330">AuthorizationResponse</span><span class="sxs-lookup"><span data-stu-id="fd721-330">AuthorizationResponse</span></span> | <span data-ttu-id="fd721-331">AuthorizationResult</span><span class="sxs-lookup"><span data-stu-id="fd721-331">AuthorizationResult</span></span> | <span data-ttu-id="fd721-332">権限呼び出しの結果。</span><span class="sxs-lookup"><span data-stu-id="fd721-332">The result of the authorization call.</span></span> | <span data-ttu-id="fd721-333">AuthorizationResult.Success.ToString()</span><span class="sxs-lookup"><span data-stu-id="fd721-333">AuthorizationResult.Success.ToString()</span></span> |
| <span data-ttu-id="fd721-334">AuthorizationResponse</span><span class="sxs-lookup"><span data-stu-id="fd721-334">AuthorizationResponse</span></span> | <span data-ttu-id="fd721-335">ExternalReceipt</span><span class="sxs-lookup"><span data-stu-id="fd721-335">ExternalReceipt</span></span> | <span data-ttu-id="fd721-336">支払プロバイダーからの外部レシート データ。</span><span class="sxs-lookup"><span data-stu-id="fd721-336">The external receipt data from the payment provider.</span></span> | <span data-ttu-id="fd721-337">\<ReceiptData\>...\</ReceiptData\></span><span class="sxs-lookup"><span data-stu-id="fd721-337">\<ReceiptData\>...\</ReceiptData\></span></span> |
| <span data-ttu-id="fd721-338">AuthorizationResponse</span><span class="sxs-lookup"><span data-stu-id="fd721-338">AuthorizationResponse</span></span> | <span data-ttu-id="fd721-339">TerminalId</span><span class="sxs-lookup"><span data-stu-id="fd721-339">TerminalId</span></span> | <span data-ttu-id="fd721-340">支払を処理した端末の一意の識別子。</span><span class="sxs-lookup"><span data-stu-id="fd721-340">The unique identifier of the terminal that handled the payment.</span></span> | <span data-ttu-id="fd721-341">000001</span><span class="sxs-lookup"><span data-stu-id="fd721-341">000001</span></span> |

<span data-ttu-id="fd721-342">次の例は、**PaymentSdkData** オブジェクトを作成する方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="fd721-342">The following example shows how to construct the **PaymentSdkData** object.</span></span>

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

<span data-ttu-id="fd721-343">支払端末がレシートを返す場合、先ほど説明した **ExternalReceipt** オブジェクトで次のデータを設定し、POS を介して印刷することができます。</span><span class="sxs-lookup"><span data-stu-id="fd721-343">If the payment terminal returns a receipt, you can print it through the POS by setting the following data on the **ExternalReceipt** object that was described earlier.</span></span>

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

###### <a name="other-considerations"></a><span data-ttu-id="fd721-344">その他の考慮事項</span><span class="sxs-lookup"><span data-stu-id="fd721-344">Other considerations</span></span>
<span data-ttu-id="fd721-345">支払端末が 1 つの呼び出しでの要求を承認し、キャプチャし (つまり*迅速なキャプチャ*が発生する場合)、出納係が取引を無効にすることを希望する場合、支払い端末では即時回収の取消がサポートされている必要があります。</span><span class="sxs-lookup"><span data-stu-id="fd721-345">If the payment terminal handles the authorize and capture requests in a single call (that is, if *immediate capture* occurs), and the cashier wants to void the transaction, the payment terminal must support reversal of an immediate capture.</span></span> <span data-ttu-id="fd721-346">迅速なキャプチャが無効なとき、無効化要求が失敗した場合、レジ担当者は、ローカルで支払を無効にするかどうかを求められます。</span><span class="sxs-lookup"><span data-stu-id="fd721-346">When an immediate capture is voided, if the void request fails, the cashier will be asked whether he or she wants to locally void the payment.</span></span> <span data-ttu-id="fd721-347">レジ担当者が**はい**と選択した場合、入札は POS でのみ無効になります。</span><span class="sxs-lookup"><span data-stu-id="fd721-347">If the cashier selects **Yes**, the tender is voided only in the POS.</span></span> <span data-ttu-id="fd721-348">支払を無効にするために支払ターミナルに対して行われる呼び出しはありません。</span><span class="sxs-lookup"><span data-stu-id="fd721-348">No call is made to the payment terminal to void the payment.</span></span> <span data-ttu-id="fd721-349">基本的には、この動作により、支払ターミナルの支払を無効にできなくなった場合レジ担当者は POS をブロック解除することができます。</span><span class="sxs-lookup"><span data-stu-id="fd721-349">Basically, this behavior lets the cashier unblock the POS if it can no longer void the payment on the payment terminal.</span></span> <span data-ttu-id="fd721-350">ただし、銀行が取り消すまでの 3 ~ 5日間はロックが続くため、この動作には問題が生じますが、迅速なキャプチャのための支払いが行われます。</span><span class="sxs-lookup"><span data-stu-id="fd721-350">However, this behavior can cause issues, because a lock lasts for three to five days, until the bank reverses it, but the payment is made for immediate capture.</span></span> <span data-ttu-id="fd721-351">したがって、重複した支払いが発生する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="fd721-351">Therefore, duplicate payments can occur.</span></span>

##### <a name="canceloperationpaymentterminaldevicerequest"></a><span data-ttu-id="fd721-352">CancelOperationPaymentTerminalDeviceRequest</span><span class="sxs-lookup"><span data-stu-id="fd721-352">CancelOperationPaymentTerminalDeviceRequest</span></span>
###### <a name="signature"></a><span data-ttu-id="fd721-353">署名</span><span class="sxs-lookup"><span data-stu-id="fd721-353">Signature</span></span>
``` csharp
public CancelOperationPaymentTerminalDeviceRequest(string token)
```

###### <a name="variables"></a><span data-ttu-id="fd721-354">変数</span><span class="sxs-lookup"><span data-stu-id="fd721-354">Variables</span></span>

| <span data-ttu-id="fd721-355">変動</span><span class="sxs-lookup"><span data-stu-id="fd721-355">Variable</span></span> | <span data-ttu-id="fd721-356">説明</span><span class="sxs-lookup"><span data-stu-id="fd721-356">Description</span></span> |
|---|---|
| <span data-ttu-id="fd721-357">token</span><span class="sxs-lookup"><span data-stu-id="fd721-357">token</span></span> | <span data-ttu-id="fd721-358">支払い端末が最初のトランザクションのためにロックされたときに生成される一意のトークン値。</span><span class="sxs-lookup"><span data-stu-id="fd721-358">The unique token value that is generated when the payment terminal is initially locked for the transaction.</span></span> |

##### <a name="capturepaymentterminaldevicerequest"></a><span data-ttu-id="fd721-359">CapturePaymentTerminalDeviceRequest</span><span class="sxs-lookup"><span data-stu-id="fd721-359">CapturePaymentTerminalDeviceRequest</span></span>
###### <a name="signature"></a><span data-ttu-id="fd721-360">署名</span><span class="sxs-lookup"><span data-stu-id="fd721-360">Signature</span></span>
``` csharp
public CapturePaymentTerminalDeviceRequest(string token, decimal amount, string currency, string paymentPropertiesXml, ExtensionTransaction extensionTransactionProperties)
```

###### <a name="variables"></a><span data-ttu-id="fd721-361">変数</span><span class="sxs-lookup"><span data-stu-id="fd721-361">Variables</span></span>

| <span data-ttu-id="fd721-362">変動</span><span class="sxs-lookup"><span data-stu-id="fd721-362">Variable</span></span> | <span data-ttu-id="fd721-363">説明</span><span class="sxs-lookup"><span data-stu-id="fd721-363">Description</span></span> |
|---|---|
| <span data-ttu-id="fd721-364">token</span><span class="sxs-lookup"><span data-stu-id="fd721-364">token</span></span> | <span data-ttu-id="fd721-365">支払い端末が最初のトランザクションのためにロックされたときに生成される一意のトークン値。</span><span class="sxs-lookup"><span data-stu-id="fd721-365">The unique token value that is generated when the payment terminal is initially locked for the transaction.</span></span> |
| <span data-ttu-id="fd721-366">金額</span><span class="sxs-lookup"><span data-stu-id="fd721-366">amount</span></span> | <span data-ttu-id="fd721-367">取得する金額。</span><span class="sxs-lookup"><span data-stu-id="fd721-367">The amount to capture.</span></span> |
| <span data-ttu-id="fd721-368">通貨</span><span class="sxs-lookup"><span data-stu-id="fd721-368">currency</span></span> | <span data-ttu-id="fd721-369">取得する金額の通貨。</span><span class="sxs-lookup"><span data-stu-id="fd721-369">The currency for the amount to capture.</span></span> |
| <span data-ttu-id="fd721-370">paymentPropertiesXml</span><span class="sxs-lookup"><span data-stu-id="fd721-370">paymentPropertiesXml</span></span> | <span data-ttu-id="fd721-371">**AuthorizePaymentTerminalDeviceRequest** 要求または **RefundPaymentTerminalDeviceRequest** 要求によって返され、要求間のステートフル プロパティをサポートするために使用される **PaymentSdkData** オブジェクトのコンテンツ。</span><span class="sxs-lookup"><span data-stu-id="fd721-371">The content of the **PaymentSdkData** object that is returned by the **AuthorizePaymentTerminalDeviceRequest** or **RefundPaymentTerminalDeviceRequest** request, and that is used to support stateful properties between the requests.</span></span> |
| <span data-ttu-id="fd721-372">extensionTransactionProperties</span><span class="sxs-lookup"><span data-stu-id="fd721-372">extensionTransactionProperties</span></span> | <span data-ttu-id="fd721-373">名前/値のペアの形式の拡張構成プロパティのセット。</span><span class="sxs-lookup"><span data-stu-id="fd721-373">The set of extension configuration properties in the form of name/value pairs.</span></span> |

###### <a name="other-considerations"></a><span data-ttu-id="fd721-374">その他の考慮事項</span><span class="sxs-lookup"><span data-stu-id="fd721-374">Other considerations</span></span>
<span data-ttu-id="fd721-375">支払端末が 1 つの呼び出しでの要求を承認およびキャプチャする場合、**CapturePaymentTerminalDeviceRequest** 要求はノーオーペレーションである必要があり、すぐに返す必要があります。</span><span class="sxs-lookup"><span data-stu-id="fd721-375">If the payment terminal handles the authorize and capture requests in a single call, the **CapturePaymentTerminalDeviceRequest** request should be a no-op and should immediately return.</span></span>

<span data-ttu-id="fd721-376">支払端末が、キャプチャ呼び出しを処理する許可要求からの状態を必要とする場合、プロパティは、先に説明した **AuthorizePaymentTerminalDeviceResponse** 要求の **PaymentSdkData** オブジェクトに格納され、 **CapturePaymentTerminalDeviceRequest** 要求の **paymentPropertiesXml** 変数を渡します。</span><span class="sxs-lookup"><span data-stu-id="fd721-376">If the payment terminal requires state from the authorize requests to handle the capture call, the properties should be stored in the **PaymentSdkData** object of the **AuthorizePaymentTerminalDeviceResponse** request that is described earlier, and passed through the **paymentPropertiesXml** variable of the **CapturePaymentTerminalDeviceRequest** request.</span></span>

##### <a name="voidpaymentterminaldevicerequest"></a><span data-ttu-id="fd721-377">VoidPaymentTerminalDeviceRequest</span><span class="sxs-lookup"><span data-stu-id="fd721-377">VoidPaymentTerminalDeviceRequest</span></span>
###### <a name="signature"></a><span data-ttu-id="fd721-378">署名</span><span class="sxs-lookup"><span data-stu-id="fd721-378">Signature</span></span>
``` csharp
public VoidPaymentTerminalDeviceRequest(string token, string paymentConnectorName, decimal amount, string currency, TenderInfo tenderInfo, string paymentPropertiesXml, ExtensionTransaction extensionTransactionProperties)
```

###### <a name="variables"></a><span data-ttu-id="fd721-379">変数</span><span class="sxs-lookup"><span data-stu-id="fd721-379">Variables</span></span>

| <span data-ttu-id="fd721-380">変動</span><span class="sxs-lookup"><span data-stu-id="fd721-380">Variable</span></span> | <span data-ttu-id="fd721-381">説明</span><span class="sxs-lookup"><span data-stu-id="fd721-381">Description</span></span> |
|---|---|
| <span data-ttu-id="fd721-382">token</span><span class="sxs-lookup"><span data-stu-id="fd721-382">token</span></span> | <span data-ttu-id="fd721-383">支払い端末が最初のトランザクションのためにロックされたときに生成される一意のトークン値。</span><span class="sxs-lookup"><span data-stu-id="fd721-383">The unique token value that is generated when the payment terminal is initially locked for the transaction.</span></span> |
| <span data-ttu-id="fd721-384">paymentConnectorName</span><span class="sxs-lookup"><span data-stu-id="fd721-384">paymentConnectorName</span></span> | <span data-ttu-id="fd721-385">支払フローの一部として使用される支払コネクタの名前。</span><span class="sxs-lookup"><span data-stu-id="fd721-385">The name of the payment connector that is used as part of the payment flow.</span></span> <span data-ttu-id="fd721-386">この変数は、**IPaymentProcessor** インターフェイスを使用する支払フローとの統合がある場合に使用されます。</span><span class="sxs-lookup"><span data-stu-id="fd721-386">This variable is used if there is an integration with payment flows that use the **IPaymentProcessor** interface.</span></span> |
| <span data-ttu-id="fd721-387">金額</span><span class="sxs-lookup"><span data-stu-id="fd721-387">amount</span></span> | <span data-ttu-id="fd721-388">支払いが無効になる金額。</span><span class="sxs-lookup"><span data-stu-id="fd721-388">The amount for the payment to void.</span></span> |
| <span data-ttu-id="fd721-389">通貨</span><span class="sxs-lookup"><span data-stu-id="fd721-389">currency</span></span> | <span data-ttu-id="fd721-390">支払いが無効になる通貨。</span><span class="sxs-lookup"><span data-stu-id="fd721-390">The currency for the payment to void.</span></span> |
| <span data-ttu-id="fd721-391">tenderInfo</span><span class="sxs-lookup"><span data-stu-id="fd721-391">tenderInfo</span></span> | <span data-ttu-id="fd721-392">外部ソースから取得された POS から送信されるカード情報 (外部ソースがある場合)。</span><span class="sxs-lookup"><span data-stu-id="fd721-392">The card information that is sent from the POS that is retrieved from an external source (if an external source is present).</span></span> |
| <span data-ttu-id="fd721-393">paymentPropertiesXml</span><span class="sxs-lookup"><span data-stu-id="fd721-393">paymentPropertiesXml</span></span> | <span data-ttu-id="fd721-394">**AuthorizePaymentTerminalDeviceRequest** 要求または **RefundPaymentTerminalDeviceRequest** 要求によって返され、要求間のステートフル プロパティをサポートするために使用される **PaymentSdkData** オブジェクトのコンテンツ。</span><span class="sxs-lookup"><span data-stu-id="fd721-394">The content of the **PaymentSdkData** object that is returned by the **AuthorizePaymentTerminalDeviceRequest** or **RefundPaymentTerminalDeviceRequest** request, and that is used to support stateful properties between the requests.</span></span> |
| <span data-ttu-id="fd721-395">extensionTransactionProperties</span><span class="sxs-lookup"><span data-stu-id="fd721-395">extensionTransactionProperties</span></span> | <span data-ttu-id="fd721-396">名前/値のペアの形式の拡張構成プロパティのセット。</span><span class="sxs-lookup"><span data-stu-id="fd721-396">The set of extension configuration properties in the form of name/value pairs.</span></span> |

##### <a name="refundpaymentterminaldevicerequest"></a><span data-ttu-id="fd721-397">RefundPaymentTerminalDeviceRequest</span><span class="sxs-lookup"><span data-stu-id="fd721-397">RefundPaymentTerminalDeviceRequest</span></span>
###### <a name="signature"></a><span data-ttu-id="fd721-398">署名</span><span class="sxs-lookup"><span data-stu-id="fd721-398">Signature</span></span>
``` csharp
public RefundPaymentTerminalDeviceRequest(string token, string paymentConnectorName, TenderInfo tenderInfo, decimal amount, string currency, bool isManualEntry, ExtensionTransaction extensionTransactionProperties)
```

###### <a name="variables"></a><span data-ttu-id="fd721-399">変数</span><span class="sxs-lookup"><span data-stu-id="fd721-399">Variables</span></span>

| <span data-ttu-id="fd721-400">変動</span><span class="sxs-lookup"><span data-stu-id="fd721-400">Variable</span></span> | <span data-ttu-id="fd721-401">説明</span><span class="sxs-lookup"><span data-stu-id="fd721-401">Description</span></span> |
|---|---|
| <span data-ttu-id="fd721-402">token</span><span class="sxs-lookup"><span data-stu-id="fd721-402">token</span></span> | <span data-ttu-id="fd721-403">支払い端末が最初のトランザクションのためにロックされたときに生成される一意のトークン値。</span><span class="sxs-lookup"><span data-stu-id="fd721-403">The unique token value that is generated when the payment terminal is initially locked for the transaction.</span></span> |
| <span data-ttu-id="fd721-404">paymentConnectorName</span><span class="sxs-lookup"><span data-stu-id="fd721-404">paymentConnectorName</span></span> | <span data-ttu-id="fd721-405">支払フローの一部として使用される支払コネクタの名前。</span><span class="sxs-lookup"><span data-stu-id="fd721-405">The name of the payment connector that is used as part of the payment flow.</span></span> <span data-ttu-id="fd721-406">この変数は、**IPaymentProcessor** インターフェイスを使用する支払フローとの統合がある場合に使用されます。</span><span class="sxs-lookup"><span data-stu-id="fd721-406">This variable is used if there is an integration with payment flows that use the **IPaymentProcessor** interface.</span></span> |
| <span data-ttu-id="fd721-407">tenderInfo</span><span class="sxs-lookup"><span data-stu-id="fd721-407">tenderInfo</span></span> | <span data-ttu-id="fd721-408">外部ソースから取得された POS から送信されるカード情報 (外部ソースがある場合)。</span><span class="sxs-lookup"><span data-stu-id="fd721-408">The card information that is sent from the POS that is retrieved from an external source (if an external source is present).</span></span> |
| <span data-ttu-id="fd721-409">金額</span><span class="sxs-lookup"><span data-stu-id="fd721-409">amount</span></span> | <span data-ttu-id="fd721-410">払い戻す金額。</span><span class="sxs-lookup"><span data-stu-id="fd721-410">The amount to refund.</span></span> |
| <span data-ttu-id="fd721-411">通貨</span><span class="sxs-lookup"><span data-stu-id="fd721-411">currency</span></span> | <span data-ttu-id="fd721-412">払い戻す金額の通貨。</span><span class="sxs-lookup"><span data-stu-id="fd721-412">The currency for the amount to refund.</span></span> |
| <span data-ttu-id="fd721-413">isManualEntry</span><span class="sxs-lookup"><span data-stu-id="fd721-413">isManualEntry</span></span> | <span data-ttu-id="fd721-414">カード番号を手動で入力されたかどうかを定義する値。</span><span class="sxs-lookup"><span data-stu-id="fd721-414">A value that defines whether the card number was entered manually.</span></span> |
| <span data-ttu-id="fd721-415">extensionTransactionProperties</span><span class="sxs-lookup"><span data-stu-id="fd721-415">extensionTransactionProperties</span></span> | <span data-ttu-id="fd721-416">名前/値のペアの形式の拡張構成プロパティのセット。</span><span class="sxs-lookup"><span data-stu-id="fd721-416">The set of extension configuration properties in the form of name/value pairs.</span></span> |

##### <a name="fetchtokenpaymentterminaldevicerequest"></a><span data-ttu-id="fd721-417">FetchTokenPaymentTerminalDeviceRequest</span><span class="sxs-lookup"><span data-stu-id="fd721-417">FetchTokenPaymentTerminalDeviceRequest</span></span>
###### <a name="signature"></a><span data-ttu-id="fd721-418">署名</span><span class="sxs-lookup"><span data-stu-id="fd721-418">Signature</span></span>
``` csharp
public FetchTokenPaymentTerminalDeviceRequest(string token, bool isManualEntry, ExtensionTransaction extensionTransactionProperties)
```

###### <a name="variables"></a><span data-ttu-id="fd721-419">変数</span><span class="sxs-lookup"><span data-stu-id="fd721-419">Variables</span></span>

| <span data-ttu-id="fd721-420">変動</span><span class="sxs-lookup"><span data-stu-id="fd721-420">Variable</span></span> | <span data-ttu-id="fd721-421">説明</span><span class="sxs-lookup"><span data-stu-id="fd721-421">Description</span></span> |
|---|---|
| <span data-ttu-id="fd721-422">token</span><span class="sxs-lookup"><span data-stu-id="fd721-422">token</span></span> | <span data-ttu-id="fd721-423">支払い端末が最初のトランザクションのためにロックされたときに生成される一意のトークン値。</span><span class="sxs-lookup"><span data-stu-id="fd721-423">The unique token value that is generated when the payment terminal is initially locked for the transaction.</span></span> |
| <span data-ttu-id="fd721-424">isManualEntry</span><span class="sxs-lookup"><span data-stu-id="fd721-424">isManualEntry</span></span> | <span data-ttu-id="fd721-425">カード番号を手動で入力されたかどうかを定義する値。</span><span class="sxs-lookup"><span data-stu-id="fd721-425">A value that defines whether the card number was entered manually.</span></span> |
| <span data-ttu-id="fd721-426">extensionTransactionProperties</span><span class="sxs-lookup"><span data-stu-id="fd721-426">extensionTransactionProperties</span></span> | <span data-ttu-id="fd721-427">名前/値のペアの形式の拡張構成プロパティのセット。</span><span class="sxs-lookup"><span data-stu-id="fd721-427">The set of extension configuration properties in the form of name/value pairs.</span></span> |

##### <a name="endtransactionpaymentterminaldevicerequest"></a><span data-ttu-id="fd721-428">EndTransactionPaymentTerminalDeviceRequest</span><span class="sxs-lookup"><span data-stu-id="fd721-428">EndTransactionPaymentTerminalDeviceRequest</span></span>
##### <a name="signature"></a><span data-ttu-id="fd721-429">署名</span><span class="sxs-lookup"><span data-stu-id="fd721-429">Signature</span></span>
``` csharp
public EndTransactionPaymentTerminalDeviceRequest(string token, ExtensionTransaction extensionTransactionProperties)
```

###### <a name="variables"></a><span data-ttu-id="fd721-430">変数</span><span class="sxs-lookup"><span data-stu-id="fd721-430">Variables</span></span>

| <span data-ttu-id="fd721-431">変動</span><span class="sxs-lookup"><span data-stu-id="fd721-431">Variable</span></span> | <span data-ttu-id="fd721-432">説明</span><span class="sxs-lookup"><span data-stu-id="fd721-432">Description</span></span> |
|---|---|
| <span data-ttu-id="fd721-433">token</span><span class="sxs-lookup"><span data-stu-id="fd721-433">token</span></span> | <span data-ttu-id="fd721-434">支払い端末が最初のトランザクションのためにロックされたときに生成される一意のトークン値。</span><span class="sxs-lookup"><span data-stu-id="fd721-434">The unique token value that is generated when the payment terminal is initially locked for the transaction.</span></span> |
| <span data-ttu-id="fd721-435">extensionTransactionProperties</span><span class="sxs-lookup"><span data-stu-id="fd721-435">extensionTransactionProperties</span></span> | <span data-ttu-id="fd721-436">名前/値のペアの形式の拡張構成プロパティのセット。</span><span class="sxs-lookup"><span data-stu-id="fd721-436">The set of extension configuration properties in the form of name/value pairs.</span></span> |

##### <a name="closepaymentterminaldevicerequest"></a><span data-ttu-id="fd721-437">ClosePaymentTerminalDeviceRequest</span><span class="sxs-lookup"><span data-stu-id="fd721-437">ClosePaymentTerminalDeviceRequest</span></span>
###### <a name="signature"></a><span data-ttu-id="fd721-438">署名</span><span class="sxs-lookup"><span data-stu-id="fd721-438">Signature</span></span>
``` csharp
public ClosePaymentTerminalDeviceRequest(string token, ExtensionTransaction extensionTransactionProperties)
```

###### <a name="variables"></a><span data-ttu-id="fd721-439">変数</span><span class="sxs-lookup"><span data-stu-id="fd721-439">Variables</span></span>

| <span data-ttu-id="fd721-440">変動</span><span class="sxs-lookup"><span data-stu-id="fd721-440">Variable</span></span> | <span data-ttu-id="fd721-441">説明</span><span class="sxs-lookup"><span data-stu-id="fd721-441">Description</span></span> |
|---|---|
| <span data-ttu-id="fd721-442">token</span><span class="sxs-lookup"><span data-stu-id="fd721-442">token</span></span> | <span data-ttu-id="fd721-443">支払い端末が最初のトランザクションのためにロックされたときに生成される一意のトークン値。</span><span class="sxs-lookup"><span data-stu-id="fd721-443">The unique token value that is generated when the payment terminal is initially locked for the transaction.</span></span> |
| <span data-ttu-id="fd721-444">extensionTransactionProperties</span><span class="sxs-lookup"><span data-stu-id="fd721-444">extensionTransactionProperties</span></span> | <span data-ttu-id="fd721-445">名前/値のペアの形式の拡張構成プロパティのセット。</span><span class="sxs-lookup"><span data-stu-id="fd721-445">The set of extension configuration properties in the form of name/value pairs.</span></span> |

##### <a name="activategiftcardpaymentterminalrequest"></a><span data-ttu-id="fd721-446">ActivateGiftCardPaymentTerminalRequest</span><span class="sxs-lookup"><span data-stu-id="fd721-446">ActivateGiftCardPaymentTerminalRequest</span></span>
###### <a name="signature"></a><span data-ttu-id="fd721-447">署名</span><span class="sxs-lookup"><span data-stu-id="fd721-447">Signature</span></span>
``` csharp
public ActivateGiftCardPaymentTerminalRequest(string token, string paymentConnectorName, decimal amount, string currencyCode, TenderInfo tenderInfo, ExtensionTransaction extensionTransactionProperties)
```

###### <a name="variables"></a><span data-ttu-id="fd721-448">変数</span><span class="sxs-lookup"><span data-stu-id="fd721-448">Variables</span></span>

| <span data-ttu-id="fd721-449">変動</span><span class="sxs-lookup"><span data-stu-id="fd721-449">Variable</span></span> | <span data-ttu-id="fd721-450">説明</span><span class="sxs-lookup"><span data-stu-id="fd721-450">Description</span></span> |
|---|---|
| <span data-ttu-id="fd721-451">token</span><span class="sxs-lookup"><span data-stu-id="fd721-451">token</span></span> | <span data-ttu-id="fd721-452">支払い端末が最初のトランザクションのためにロックされたときに生成される一意のトークン値。</span><span class="sxs-lookup"><span data-stu-id="fd721-452">The unique token value that is generated when the payment terminal is initially locked for the transaction.</span></span> |
| <span data-ttu-id="fd721-453">paymentConnectorName</span><span class="sxs-lookup"><span data-stu-id="fd721-453">paymentConnectorName</span></span> | <span data-ttu-id="fd721-454">支払フローの一部として使用される支払コネクタの名前。</span><span class="sxs-lookup"><span data-stu-id="fd721-454">The name of the payment connector that is used as part of the payment flow.</span></span> <span data-ttu-id="fd721-455">この変数は、**IPaymentProcessor** インターフェイスを使用する支払フローとの統合がある場合に使用されます。</span><span class="sxs-lookup"><span data-stu-id="fd721-455">This variable is used if there is an integration with payment flows that use the **IPaymentProcessor** interface.</span></span> |
| <span data-ttu-id="fd721-456">金額</span><span class="sxs-lookup"><span data-stu-id="fd721-456">amount</span></span> | <span data-ttu-id="fd721-457">有効化中にギフト カードに追加する初期金額。</span><span class="sxs-lookup"><span data-stu-id="fd721-457">The initial amount to add to the gift card during activation.</span></span> |
| <span data-ttu-id="fd721-458">通貨</span><span class="sxs-lookup"><span data-stu-id="fd721-458">currency</span></span> | <span data-ttu-id="fd721-459">有効化中にギフト カードに追加する初期金額の通貨。</span><span class="sxs-lookup"><span data-stu-id="fd721-459">The currency for the initial amount to add to the gift card during activation.</span></span> |
| <span data-ttu-id="fd721-460">tenderInfo</span><span class="sxs-lookup"><span data-stu-id="fd721-460">tenderInfo</span></span> | <span data-ttu-id="fd721-461">外部ソースから取得された POS から送信されるカード情報 (外部ソースがある場合)。</span><span class="sxs-lookup"><span data-stu-id="fd721-461">The card information that is sent from the POS that is retrieved from an external source (if an external source is present).</span></span> |
| <span data-ttu-id="fd721-462">extensionTransactionProperties</span><span class="sxs-lookup"><span data-stu-id="fd721-462">extensionTransactionProperties</span></span> | <span data-ttu-id="fd721-463">名前/値のペアの形式の拡張構成プロパティのセット。</span><span class="sxs-lookup"><span data-stu-id="fd721-463">The set of extension configuration properties in the form of name/value pairs.</span></span> |

##### <a name="addbalancetogiftcardpaymentterminalrequest"></a><span data-ttu-id="fd721-464">AddBalanceToGiftCardPaymentTerminalRequest</span><span class="sxs-lookup"><span data-stu-id="fd721-464">AddBalanceToGiftCardPaymentTerminalRequest</span></span>
###### <a name="signature"></a><span data-ttu-id="fd721-465">署名</span><span class="sxs-lookup"><span data-stu-id="fd721-465">Signature</span></span>
``` csharp
public AddBalanceToGiftCardPaymentTerminalRequest(string token, string paymentConnectorName, decimal amount, string currencyCode, TenderInfo tenderInfo, ExtensionTransaction extensionTransactionProperties)
```

###### <a name="variables"></a><span data-ttu-id="fd721-466">変数</span><span class="sxs-lookup"><span data-stu-id="fd721-466">Variables</span></span>

| <span data-ttu-id="fd721-467">変動</span><span class="sxs-lookup"><span data-stu-id="fd721-467">Variable</span></span> | <span data-ttu-id="fd721-468">説明</span><span class="sxs-lookup"><span data-stu-id="fd721-468">Description</span></span> |
|---|---|
| <span data-ttu-id="fd721-469">token</span><span class="sxs-lookup"><span data-stu-id="fd721-469">token</span></span> | <span data-ttu-id="fd721-470">支払い端末が最初のトランザクションのためにロックされたときに生成される一意のトークン値。</span><span class="sxs-lookup"><span data-stu-id="fd721-470">The unique token value that is generated when the payment terminal is initially locked for the transaction.</span></span> |
| <span data-ttu-id="fd721-471">paymentConnectorName</span><span class="sxs-lookup"><span data-stu-id="fd721-471">paymentConnectorName</span></span> | <span data-ttu-id="fd721-472">支払フローの一部として使用される支払コネクタの名前。</span><span class="sxs-lookup"><span data-stu-id="fd721-472">The name of the payment connector that is used as part of the payment flow.</span></span> <span data-ttu-id="fd721-473">この変数は、**IPaymentProcessor** インターフェイスを使用する支払フローとの統合がある場合に使用されます。</span><span class="sxs-lookup"><span data-stu-id="fd721-473">This variable is used if there is an integration with payment flows that use the **IPaymentProcessor** interface.</span></span> |
| <span data-ttu-id="fd721-474">金額</span><span class="sxs-lookup"><span data-stu-id="fd721-474">amount</span></span> | <span data-ttu-id="fd721-475">ギフト カードに追加される金額。</span><span class="sxs-lookup"><span data-stu-id="fd721-475">The amount to add to the gift card.</span></span> |
| <span data-ttu-id="fd721-476">通貨</span><span class="sxs-lookup"><span data-stu-id="fd721-476">currency</span></span> | <span data-ttu-id="fd721-477">ギフト カード残高に追加する金額の通貨。</span><span class="sxs-lookup"><span data-stu-id="fd721-477">The currency for the amount to add to the gift card balance.</span></span> |
| <span data-ttu-id="fd721-478">tenderInfo</span><span class="sxs-lookup"><span data-stu-id="fd721-478">tenderInfo</span></span> | <span data-ttu-id="fd721-479">外部ソースから取得された POS から送信されるカード情報 (外部ソースがある場合)。</span><span class="sxs-lookup"><span data-stu-id="fd721-479">The card information that is sent from the POS that is retrieved from an external source (if an external source present).</span></span> |
| <span data-ttu-id="fd721-480">extensionTransactionProperties</span><span class="sxs-lookup"><span data-stu-id="fd721-480">extensionTransactionProperties</span></span> | <span data-ttu-id="fd721-481">名前/値のペアの形式の拡張構成プロパティのセット。</span><span class="sxs-lookup"><span data-stu-id="fd721-481">The set of extension configuration properties in the form of name/value pairs.</span></span> |

##### <a name="getgiftcardbalancepaymentterminalrequest"></a><span data-ttu-id="fd721-482">GetGiftCardBalancePaymentTerminalRequest</span><span class="sxs-lookup"><span data-stu-id="fd721-482">GetGiftCardBalancePaymentTerminalRequest</span></span>
###### <a name="signature"></a><span data-ttu-id="fd721-483">署名</span><span class="sxs-lookup"><span data-stu-id="fd721-483">Signature</span></span>
``` csharp
public GetGiftCardBalancePaymentTerminalRequest(string token, string paymentConnectorName, string currencyCode, TenderInfo tenderInfo, ExtensionTransaction extensionTransactionProperties)
```

###### <a name="variables"></a><span data-ttu-id="fd721-484">変数</span><span class="sxs-lookup"><span data-stu-id="fd721-484">Variables</span></span>

| <span data-ttu-id="fd721-485">変動</span><span class="sxs-lookup"><span data-stu-id="fd721-485">Variable</span></span> | <span data-ttu-id="fd721-486">説明</span><span class="sxs-lookup"><span data-stu-id="fd721-486">Description</span></span> |
|---|---|
| <span data-ttu-id="fd721-487">token</span><span class="sxs-lookup"><span data-stu-id="fd721-487">token</span></span> | <span data-ttu-id="fd721-488">支払い端末が最初のトランザクションのためにロックされたときに生成される一意のトークン値。</span><span class="sxs-lookup"><span data-stu-id="fd721-488">The unique token value that is generated when the payment terminal is initially locked for the transaction.</span></span> |
| <span data-ttu-id="fd721-489">paymentConnectorName</span><span class="sxs-lookup"><span data-stu-id="fd721-489">paymentConnectorName</span></span> | <span data-ttu-id="fd721-490">支払フローの一部として使用される支払コネクタの名前。</span><span class="sxs-lookup"><span data-stu-id="fd721-490">The name of the payment connector that is used as part of the payment flow.</span></span> <span data-ttu-id="fd721-491">この変数は、**IPaymentProcessor** インターフェイスを使用する支払フローとの統合がある場合に使用されます。</span><span class="sxs-lookup"><span data-stu-id="fd721-491">This variable is used if there is an integration with payment flows that use the **IPaymentProcessor** interface.</span></span> |
| <span data-ttu-id="fd721-492">通貨</span><span class="sxs-lookup"><span data-stu-id="fd721-492">currency</span></span> | <span data-ttu-id="fd721-493">ギフト カード残高を取得するための通貨。</span><span class="sxs-lookup"><span data-stu-id="fd721-493">The currency to retrieve the gift card balance in.</span></span> |
| <span data-ttu-id="fd721-494">tenderInfo</span><span class="sxs-lookup"><span data-stu-id="fd721-494">tenderInfo</span></span> | <span data-ttu-id="fd721-495">外部ソースから取得された POS から送信されるカード情報 (外部ソースがある場合)。</span><span class="sxs-lookup"><span data-stu-id="fd721-495">The card information that is sent from the POS that is retrieved from an external source (if an external source present).</span></span> |
| <span data-ttu-id="fd721-496">extensionTransactionProperties</span><span class="sxs-lookup"><span data-stu-id="fd721-496">extensionTransactionProperties</span></span> | <span data-ttu-id="fd721-497">名前/値のペアの形式の拡張構成プロパティのセット。</span><span class="sxs-lookup"><span data-stu-id="fd721-497">The set of extension configuration properties in the form of name/value pairs.</span></span> |

##### <a name="getprivatetenderpaymentterminaldevicerequest"></a><span data-ttu-id="fd721-498">GetPrivateTenderPaymentTerminalDeviceRequest</span><span class="sxs-lookup"><span data-stu-id="fd721-498">GetPrivateTenderPaymentTerminalDeviceRequest</span></span>
###### <a name="signature"></a><span data-ttu-id="fd721-499">署名</span><span class="sxs-lookup"><span data-stu-id="fd721-499">Signature</span></span>
``` csharp
public GetPrivateTenderPaymentTerminalDeviceRequest(string token, decimal amount, bool declined, bool isSwipe, ExtensionTransaction extensionTransactionProperties)
```

###### <a name="variables"></a><span data-ttu-id="fd721-500">変数</span><span class="sxs-lookup"><span data-stu-id="fd721-500">Variables</span></span>

| <span data-ttu-id="fd721-501">変動</span><span class="sxs-lookup"><span data-stu-id="fd721-501">Variable</span></span> | <span data-ttu-id="fd721-502">説明</span><span class="sxs-lookup"><span data-stu-id="fd721-502">Description</span></span> |
|---|---|
| <span data-ttu-id="fd721-503">token</span><span class="sxs-lookup"><span data-stu-id="fd721-503">token</span></span> | <span data-ttu-id="fd721-504">支払い端末が最初のトランザクションのためにロックされたときに生成される一意のトークン値。</span><span class="sxs-lookup"><span data-stu-id="fd721-504">The unique token value that is generated when the payment terminal is initially locked for the transaction.</span></span> |
| <span data-ttu-id="fd721-505">金額</span><span class="sxs-lookup"><span data-stu-id="fd721-505">amount</span></span> | <span data-ttu-id="fd721-506">POS に設定された金額。</span><span class="sxs-lookup"><span data-stu-id="fd721-506">The amount that is set on the POS.</span></span> <span data-ttu-id="fd721-507">(通常、この変数は、カード番号を取得したときに支払ターミナルの金額を表示するために使用されます。)</span><span class="sxs-lookup"><span data-stu-id="fd721-507">(Typically, this variable is used to show the amount on the payment terminal when the card number is retrieved.)</span></span> |
| <span data-ttu-id="fd721-508">declined</span><span class="sxs-lookup"><span data-stu-id="fd721-508">declined</span></span> | <span data-ttu-id="fd721-509">この値は廃止されています。</span><span class="sxs-lookup"><span data-stu-id="fd721-509">This variable is obsolete.</span></span> |
| <span data-ttu-id="fd721-510">isSwipe</span><span class="sxs-lookup"><span data-stu-id="fd721-510">isSwipe</span></span> | <span data-ttu-id="fd721-511">支払ターミナルで読み取りまたは手動入力によってカード番号を取得する必要があるかどうかを決定する値。</span><span class="sxs-lookup"><span data-stu-id="fd721-511">A value that determines whether the card number should be retrieved through a swipe or manual entry on the payment terminal.</span></span> |
| <span data-ttu-id="fd721-512">extensionTransactionProperties</span><span class="sxs-lookup"><span data-stu-id="fd721-512">extensionTransactionProperties</span></span> | <span data-ttu-id="fd721-513">名前/値のペアの形式の拡張構成プロパティのセット。</span><span class="sxs-lookup"><span data-stu-id="fd721-513">The set of extension configuration properties in the form of name/value pairs.</span></span> |

##### <a name="executetaskpaymentterminaldevicerequest"></a><span data-ttu-id="fd721-514">ExecuteTaskPaymentTerminalDeviceRequest</span><span class="sxs-lookup"><span data-stu-id="fd721-514">ExecuteTaskPaymentTerminalDeviceRequest</span></span>
###### <a name="signature"></a><span data-ttu-id="fd721-515">署名</span><span class="sxs-lookup"><span data-stu-id="fd721-515">Signature</span></span>
``` csharp
public ExecuteTaskPaymentTerminalDeviceRequest(string token, string task, ExtensionTransaction extensionTransactionProperties)
```

###### <a name="variables"></a><span data-ttu-id="fd721-516">変数</span><span class="sxs-lookup"><span data-stu-id="fd721-516">Variables</span></span>

| <span data-ttu-id="fd721-517">変動</span><span class="sxs-lookup"><span data-stu-id="fd721-517">Variable</span></span> | <span data-ttu-id="fd721-518">説明</span><span class="sxs-lookup"><span data-stu-id="fd721-518">Description</span></span> |
|---|---|
| <span data-ttu-id="fd721-519">token</span><span class="sxs-lookup"><span data-stu-id="fd721-519">token</span></span> | <span data-ttu-id="fd721-520">支払い端末が最初のトランザクションのためにロックされたときに生成される一意のトークン値。</span><span class="sxs-lookup"><span data-stu-id="fd721-520">The unique token value that is generated when the payment terminal is initially locked for the transaction.</span></span> |
| <span data-ttu-id="fd721-521">タスク</span><span class="sxs-lookup"><span data-stu-id="fd721-521">task</span></span> | <span data-ttu-id="fd721-522">実行されているタスクの一意の識別子。</span><span class="sxs-lookup"><span data-stu-id="fd721-522">The unique identifier for the task that is being run.</span></span> |
| <span data-ttu-id="fd721-523">extensionTransactionProperties</span><span class="sxs-lookup"><span data-stu-id="fd721-523">extensionTransactionProperties</span></span> | <span data-ttu-id="fd721-524">名前/値のペアの形式の拡張構成プロパティのセット。</span><span class="sxs-lookup"><span data-stu-id="fd721-524">The set of extension configuration properties in the form of name/value pairs.</span></span> |

##### <a name="gettransactionreferencepaymentterminaldevicerequest"></a><span data-ttu-id="fd721-525">GetTransactionReferencePaymentTerminalDeviceRequest</span><span class="sxs-lookup"><span data-stu-id="fd721-525">GetTransactionReferencePaymentTerminalDeviceRequest</span></span>
###### <a name="signature"></a><span data-ttu-id="fd721-526">署名</span><span class="sxs-lookup"><span data-stu-id="fd721-526">Signature</span></span>
``` csharp
 public GetTransactionReferencePaymentTerminalDeviceRequest(string lockToken, string posTerminalId, string eftTerminalId)
```

###### <a name="variables"></a><span data-ttu-id="fd721-527">変数</span><span class="sxs-lookup"><span data-stu-id="fd721-527">Variables</span></span>

| <span data-ttu-id="fd721-528">変数</span><span class="sxs-lookup"><span data-stu-id="fd721-528">Variable</span></span> | <span data-ttu-id="fd721-529">説明</span><span class="sxs-lookup"><span data-stu-id="fd721-529">Description</span></span> |
|---|---|
| <span data-ttu-id="fd721-530">locktoken</span><span class="sxs-lookup"><span data-stu-id="fd721-530">locktoken</span></span> | <span data-ttu-id="fd721-531">支払端末が取引で最初にロックされたときに生成された一意のロック トークンを取得します。</span><span class="sxs-lookup"><span data-stu-id="fd721-531">Gets the unique lock token that was generated when the payment terminal was initially locked for the transaction.</span></span> |
| <span data-ttu-id="fd721-532">posTerminalId</span><span class="sxs-lookup"><span data-stu-id="fd721-532">posTerminalId</span></span> | <span data-ttu-id="fd721-533">ロック トークンに関連付けられた POS 端末の ID を取得します。</span><span class="sxs-lookup"><span data-stu-id="fd721-533">Gets the POS terminal ID associated with the lock token.</span></span> |
| <span data-ttu-id="fd721-534">extensionTransactionProperties</span><span class="sxs-lookup"><span data-stu-id="fd721-534">extensionTransactionProperties</span></span> | <span data-ttu-id="fd721-535">取引とロック トークンに関連付けられた EFT 端末の ID を取得します。</span><span class="sxs-lookup"><span data-stu-id="fd721-535">Gets the EFT terminal ID associated witht the transaction and lock token.</span></span> |

##### <a name="gettransactionbytransactionreferencepaymentterminaldevicerequest"></a><span data-ttu-id="fd721-536">GetTransactionByTransactionReferencePaymentTerminalDeviceRequest</span><span class="sxs-lookup"><span data-stu-id="fd721-536">GetTransactionByTransactionReferencePaymentTerminalDeviceRequest</span></span>
###### <a name="signature"></a><span data-ttu-id="fd721-537">署名</span><span class="sxs-lookup"><span data-stu-id="fd721-537">Signature</span></span>
``` csharp
 public GetTransactionByTransactionReferencePaymentTerminalDeviceRequest(string lockToken, Retail.PaymentSDK.Portable.PaymentTransactionReferenceData transactionReferenceData)
```

###### <a name="variables"></a><span data-ttu-id="fd721-538">変数</span><span class="sxs-lookup"><span data-stu-id="fd721-538">Variables</span></span>

| <span data-ttu-id="fd721-539">変数</span><span class="sxs-lookup"><span data-stu-id="fd721-539">Variable</span></span> | <span data-ttu-id="fd721-540">説明</span><span class="sxs-lookup"><span data-stu-id="fd721-540">Description</span></span> |
|---|---|
| <span data-ttu-id="fd721-541">locktoken</span><span class="sxs-lookup"><span data-stu-id="fd721-541">locktoken</span></span> | <span data-ttu-id="fd721-542">支払端末が取引で最初にロックされたときに生成された一意のロック トークンを取得します。</span><span class="sxs-lookup"><span data-stu-id="fd721-542">Gets the unique lock token that was generated when the payment terminal was initially locked for the transaction.</span></span> |
| <span data-ttu-id="fd721-543">Retail.PaymentSDK.Portable.PaymentTransactionReferenceData TransactionReferenceData</span><span class="sxs-lookup"><span data-stu-id="fd721-543">Retail.PaymentSDK.Portable.PaymentTransactionReferenceData TransactionReferenceData</span></span> | <span data-ttu-id="fd721-544">相関する ID が同期していない場合に、支払取引の参照データを取得します。</span><span class="sxs-lookup"><span data-stu-id="fd721-544">Gets reference data for the for payment transactions in case the correlation ID is out of sync.</span></span> |


##### <a name="cashoutgiftcardpaymentterminalrequest"></a><span data-ttu-id="fd721-545">CashoutGiftCardPaymentTerminalRequest</span><span class="sxs-lookup"><span data-stu-id="fd721-545">CashoutGiftCardPaymentTerminalRequest</span></span>
###### <a name="signature"></a><span data-ttu-id="fd721-546">署名</span><span class="sxs-lookup"><span data-stu-id="fd721-546">Signature</span></span>
``` csharp
 public CashoutGiftCardPaymentTerminalRequest(
            string paymentConnectorName,
            decimal amount,
            string currencyCode,
            TenderInfo tenderInfo,
            ExtensionTransaction extensionTransactionProperties)
```

###### <a name="variables"></a><span data-ttu-id="fd721-547">変数</span><span class="sxs-lookup"><span data-stu-id="fd721-547">Variables</span></span>

| <span data-ttu-id="fd721-548">変数</span><span class="sxs-lookup"><span data-stu-id="fd721-548">Variable</span></span> | <span data-ttu-id="fd721-549">説明</span><span class="sxs-lookup"><span data-stu-id="fd721-549">Description</span></span> |
|---|---|
| <span data-ttu-id="fd721-550">paymentConnectorName</span><span class="sxs-lookup"><span data-stu-id="fd721-550">paymentConnectorName</span></span> | <span data-ttu-id="fd721-551">支払フローの一部として使用される支払コネクタの名前。</span><span class="sxs-lookup"><span data-stu-id="fd721-551">The name of the payment connector that is used as part of the payment flow.</span></span> <span data-ttu-id="fd721-552">この変数は、IPaymentProcessor インターフェイスを使用する支払フローとの統合がある場合に使用されます。</span><span class="sxs-lookup"><span data-stu-id="fd721-552">This variable is used if there is an integration with payment flows that use the IPaymentProcessor interface.</span></span> |
| <span data-ttu-id="fd721-553">金額</span><span class="sxs-lookup"><span data-stu-id="fd721-553">amount</span></span> | <span data-ttu-id="fd721-554">ギフト カードのキャッシュ アウト要求額。</span><span class="sxs-lookup"><span data-stu-id="fd721-554">The amount gift card cash out request.</span></span> |
| <span data-ttu-id="fd721-555">currencyCode</span><span class="sxs-lookup"><span data-stu-id="fd721-555">currencyCode</span></span> | <span data-ttu-id="fd721-556">ギフト カードのキャッシュ アウト要求に使用する通貨。</span><span class="sxs-lookup"><span data-stu-id="fd721-556">The currency for the gift card cash out request.</span></span> |
| <span data-ttu-id="fd721-557">tenderinfo</span><span class="sxs-lookup"><span data-stu-id="fd721-557">tenderinfo</span></span> | <span data-ttu-id="fd721-558">外部ソースから取得された POS から送信されるカード情報 (外部ソースがある場合)。</span><span class="sxs-lookup"><span data-stu-id="fd721-558">The card information that is sent from the POS that is retrieved from an external source (if an external source is present).</span></span> |
| <span data-ttu-id="fd721-559">extensionTransactionProperties</span><span class="sxs-lookup"><span data-stu-id="fd721-559">extensionTransactionProperties</span></span> | <span data-ttu-id="fd721-560">名前/値のペアの形式の拡張構成プロパティのセット。</span><span class="sxs-lookup"><span data-stu-id="fd721-560">The set of extension configuration properties in the form of name/value pairs.</span></span> |


#### <a name="state-in-the-payment-connector"></a><span data-ttu-id="fd721-561">支払コネクタの状態</span><span class="sxs-lookup"><span data-stu-id="fd721-561">State in the payment connector</span></span>
<span data-ttu-id="fd721-562">支払いコネクターは、POS 内のインプロセス ハードウェア ステーションを通じてホストされているとき、dllhost.exe プロセスの一部としてホストすることができます。</span><span class="sxs-lookup"><span data-stu-id="fd721-562">The payment connector can be hosted as part of the dllhost.exe process when it's hosted through the in-process Hardware Station inside the POS.</span></span> <span data-ttu-id="fd721-563">または、 Microsoft Internet Information Services (IIS) に基づくハードウェア ステーションでホストされている場合、w3wp.exe プロセスとして支払コネクタをホストすることができます。</span><span class="sxs-lookup"><span data-stu-id="fd721-563">Alternatively, the payment connector can be hosted as a w3wp.exe process when it's hosted in the Hardware Station that is based on Microsoft Internet Information Services (IIS).</span></span> <span data-ttu-id="fd721-564">状況によっては、支払フローの間または最中に両方のプロセスを終了したり、応答を停止したりできます。</span><span class="sxs-lookup"><span data-stu-id="fd721-564">In some circumstances, both processes can be terminated or stop responding between or during payment flows.</span></span> <span data-ttu-id="fd721-565">したがって、支払コネクタには状態依存性がなく、以前に説明した支払フロー関連の要求のいずれかの時点で終了すると回復することができるようにすることをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="fd721-565">Therefore, we recommend that payment connectors not have state dependencies, and that they be able to recover if they are terminated at any point during the payment flow–related requests that are described earlier.</span></span>

### <a name="configure-the-payment-connector-in-the-hardware-station-config"></a><span data-ttu-id="fd721-566">ハードウェア ステーションのコンフィギュレーションで支払コネクタをコンフィギュレーションする</span><span class="sxs-lookup"><span data-stu-id="fd721-566">Configure the payment connector in the Hardware Station config</span></span>
<span data-ttu-id="fd721-567">ハードウェア ステーションが支払コネクタを読み込むようにするために、対応するアセンブリ参照を **HardwareStation.Extension.config** ファイルに設定する必要があります。このファイルは Retail SDK の **Assets** フォルダーにあります。</span><span class="sxs-lookup"><span data-stu-id="fd721-567">To help guarantee that the Hardware Station loads the payment connector, you must set the corresponding assembly reference in the **HardwareStation.Extension.config** file that is located in the **Assets** folder in the Retail SDK.</span></span>

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

### <a name="configure-the-payment-connector-on-the-pos-hardware-profile-page-in-the-client"></a><span data-ttu-id="fd721-568">クライアントの POS ハードウェア プロファイル ページで支払コネクタをコンフィギュレーションする</span><span class="sxs-lookup"><span data-stu-id="fd721-568">Configure the payment connector on the POS hardware profile page in the client</span></span>
<span data-ttu-id="fd721-569">POS にロードする正しい支払コネクタを決定するには、次の図に示すように、クライアントの **POS ハードウェア プロファイル** ページの **PIN パッド** クイック タブで、**デバイス名**フィールドの **PaymentTerminalDevice** プロパティの値を設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="fd721-569">To determine the correct payment connector that should be loaded on the POS, you must set the value of the **PaymentTerminalDevice** property in the **Device name** field on the **PIN pad** FastTab of the **POS hardware profile** page in the client, as shown in the following illustration.</span></span>

![クライアントの POS ハードウェア プロファイル ページで支払コネクタをコンフィギュレーションする](media/PAYMENTS/PAYMENT-TERMINAL/SamplePaymentDeviceConfigurInAx.jpg)

## <a name="write-a-payment-processor"></a><span data-ttu-id="fd721-571">支払プロセッサの記述</span><span class="sxs-lookup"><span data-stu-id="fd721-571">Write a payment processor</span></span>
<span data-ttu-id="fd721-572">通常は、支払ゲートウェイへの直接接続が確立された場合にのみ、支払プロセスが使用されます。</span><span class="sxs-lookup"><span data-stu-id="fd721-572">Payment processes are usually used only if a direct connection to a payment gateway is established.</span></span> <span data-ttu-id="fd721-573">このシナリオは、カードが存在しない販売取引またはより複雑なカードが存在するシナリオで最も頻繁に発生します。</span><span class="sxs-lookup"><span data-stu-id="fd721-573">This scenario most often occurs in card-not-present sales transactions or more complex card-present scenarios.</span></span> <span data-ttu-id="fd721-574">また、支払プロセッサは、クライアントの **POS ハードウェア プロファイル** ページを使用してコンフィギュレーションされている商社プロパティを処理するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="fd721-574">Additionally, the payment processor is used to process the merchant properties that are configured through the **POS hardware profile** page in the client.</span></span>

> [!NOTE]
> <span data-ttu-id="fd721-575">支払プロセッサは、支払要求がすべて支払ターミナルを使用して直接処理され、商社プロパティを POS を使用して設定する必要がない場合でも、現在のところは必要です。</span><span class="sxs-lookup"><span data-stu-id="fd721-575">The payment processor is currently required, even if all payment requests are handled directly through the payment terminal and no merchant properties must be set through the POS.</span></span>

### <a name="understanding-the-merchant-properties-flows"></a><span data-ttu-id="fd721-576">商社プロパティ フローを理解する</span><span class="sxs-lookup"><span data-stu-id="fd721-576">Understanding the merchant properties flows</span></span>
<span data-ttu-id="fd721-577">次のセクションでは、クライアントの **POS ハードウェア プロファイル** ページでの商社プロパティの設定方法と、POS での支払フロー中に支払コネクタにこれらのプロパティを渡す方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="fd721-577">The following sections describe how the merchant properties are set on the **POS hardware profile** page in the client, and how they are passed to the payment connector during payment flows on the POS.</span></span>

#### <a name="set-merchant-properties-on-the-pos-hardware-profile-page-in-the-client"></a><span data-ttu-id="fd721-578">クライアントの POS ハードウェア プロファイル ページで商社プロパティを設定</span><span class="sxs-lookup"><span data-stu-id="fd721-578">Set merchant properties on the POS hardware profile page in the client</span></span>
<span data-ttu-id="fd721-579">次の図は、クライアントの **POS ハードウェア プロファイル** ページで商社プロパティを設定する方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="fd721-579">The following illustration shows how the merchant properties are set through the **POS hardware profile** page in the client.</span></span> <span data-ttu-id="fd721-580">マーチャントプロパティを設定するには、**IPaymentProcessor** ライブラリで定義されている **Microsoft.Dynamics.Retail.PaymentSDK** インターフェイスを実装する必要があります。</span><span class="sxs-lookup"><span data-stu-id="fd721-580">To enable the merchant properties to be set, the **IPaymentProcessor** interface that is defined in the **Microsoft.Dynamics.Retail.PaymentSDK** library must be implemented.</span></span> <span data-ttu-id="fd721-581">**GetMerchantAccountPropertyMetadata** と **ValidateMerchantAccount** の 2 つのインターフェイス メソッドが必要です。</span><span class="sxs-lookup"><span data-stu-id="fd721-581">Two interface methods are required: **GetMerchantAccountPropertyMetadata** and **ValidateMerchantAccount**.</span></span>

![クライアントの POS ハードウェア プロファイル ページで商社プロパティを設定する](media/PAYMENTS/PAYMENT-TERMINAL/MerchantPropertiesAXFlow.jpg)

#### <a name="set-merchant-properties-on-payment-connector-during-pos-sales-transaction"></a><span data-ttu-id="fd721-583">POS 販売トランザクションの間に支払コネクタで商社プロパティを設定</span><span class="sxs-lookup"><span data-stu-id="fd721-583">Set merchant properties on payment connector during POS sales transaction</span></span>
<span data-ttu-id="fd721-584">次の図は、**BeginTransactionPaymentTerminalDeviceRequest** 要求の間に Commerce Scale Unit を介してデータベースから商社プロパティを取得して支払コネクタに渡す仕組みを示しています。</span><span class="sxs-lookup"><span data-stu-id="fd721-584">The following illustration shows how the merchant properties are retrieved from the database through the Commerce Scale Unit and passed to the payment connector during the **BeginTransactionPaymentTerminalDeviceRequest** request.</span></span>

![POS 支払フロー時に支払コネクタに商社プロパティを設定](media/PAYMENTS/PAYMENT-TERMINAL/MerchantPropertiesPOSFlow.jpg)

### <a name="implement-the-ipaymentprocessor-interface"></a><span data-ttu-id="fd721-586">IPaymentProcessor インターフェイスの実装</span><span class="sxs-lookup"><span data-stu-id="fd721-586">Implement the IPaymentProcessor interface</span></span>
<span data-ttu-id="fd721-587">支払フローに関連するマーチャント プロパティを処理するには、**Microsoft.Dynamics.Retail.PaymentSDK** ライブラリで定義されている **IPaymentProcessor** インターフェイスを実装する必要があります。</span><span class="sxs-lookup"><span data-stu-id="fd721-587">To handle merchant properties that are related to payment flows, the **IPaymentProcessor** interface that is defined in the **Microsoft.Dynamics.Retail.PaymentSDK** library must be implemented.</span></span> <span data-ttu-id="fd721-588">次の例は、2 つの必須インターフェイス メソッド、**GetMerchantAccountPropertyMetadata** と **ValidateMerchantAccount** を実装する方法を示しています。.</span><span class="sxs-lookup"><span data-stu-id="fd721-588">The following example shows how to implement the two required interface methods, **GetMerchantAccountPropertyMetadata** and **ValidateMerchantAccount**.</span></span> <span data-ttu-id="fd721-589">他のインターフェイス メソッドは、空白にできます (たとえば、**FeatureNotSupportedException** を返すことができます)。</span><span class="sxs-lookup"><span data-stu-id="fd721-589">Other interface methods can be left blank (for example, they can return **FeatureNotSupportedException**).</span></span>

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

#### <a name="required-merchant-property-fields"></a><span data-ttu-id="fd721-590">必須商社プロパティ フィールド</span><span class="sxs-lookup"><span data-stu-id="fd721-590">Required merchant property fields</span></span>
<span data-ttu-id="fd721-591">次のテーブルに、**GetMerchantAccountPropertyMetadata** メソッドの一部として設定する必要のある商社プロパティのフィールドを示します。</span><span class="sxs-lookup"><span data-stu-id="fd721-591">The following table shows the required merchant property fields that must be set as part of the **GetMerchantAccountPropertyMetadata** method.</span></span>

| <span data-ttu-id="fd721-592">名前空間</span><span class="sxs-lookup"><span data-stu-id="fd721-592">Namespace</span></span> | <span data-ttu-id="fd721-593">氏名</span><span class="sxs-lookup"><span data-stu-id="fd721-593">Name</span></span> | <span data-ttu-id="fd721-594">サンプル値\*</span><span class="sxs-lookup"><span data-stu-id="fd721-594">Sample value\*</span></span> |
|---|---|---|
| <span data-ttu-id="fd721-595">MerchantAccount</span><span class="sxs-lookup"><span data-stu-id="fd721-595">MerchantAccount</span></span> | <span data-ttu-id="fd721-596">PortableAssemblyName</span><span class="sxs-lookup"><span data-stu-id="fd721-596">PortableAssemblyName</span></span> | <span data-ttu-id="fd721-597">Contoso.Microsoft.PaymentsSample</span><span class="sxs-lookup"><span data-stu-id="fd721-597">Contoso.Microsoft.PaymentsSample</span></span> |
| <span data-ttu-id="fd721-598">MerchantAccount</span><span class="sxs-lookup"><span data-stu-id="fd721-598">MerchantAccount</span></span> | <span data-ttu-id="fd721-599">ServiceAccountId</span><span class="sxs-lookup"><span data-stu-id="fd721-599">ServiceAccountId</span></span> | <span data-ttu-id="fd721-600">f35989c8-e571-4de1-862a-996c82a2e6b6</span><span class="sxs-lookup"><span data-stu-id="fd721-600">f35989c8-e571-4de1-862a-996c82a2e6b6</span></span> |
| <span data-ttu-id="fd721-601">MerchantAccount</span><span class="sxs-lookup"><span data-stu-id="fd721-601">MerchantAccount</span></span> | <span data-ttu-id="fd721-602">SupportedCurrencies</span><span class="sxs-lookup"><span data-stu-id="fd721-602">SupportedCurrencies</span></span> | <span data-ttu-id="fd721-603">AUD、BRL、CAD、CHF、CNY、CZK、DKK、EUR、GBP、HKD、HUF、INR、JPY、KPW、KRW、MXN、NOK、NZD、PLN、SEK、SGD、TWD、USD、ZAR</span><span class="sxs-lookup"><span data-stu-id="fd721-603">AUD;BRL;CAD;CHF;CNY;CZK;DKK;EUR;GBP;HKD;HUF;INR;JPY;KPW;KRW;MXN;NOK;NZD;PLN;SEK;SGD;TWD;USD;ZAR</span></span> |
| <span data-ttu-id="fd721-604">MerchantAccount</span><span class="sxs-lookup"><span data-stu-id="fd721-604">MerchantAccount</span></span> | <span data-ttu-id="fd721-605">SupportedTenderTypes</span><span class="sxs-lookup"><span data-stu-id="fd721-605">SupportedTenderTypes</span></span> | <span data-ttu-id="fd721-606">Visa;MasterCard;Amex;Discover;Debit</span><span class="sxs-lookup"><span data-stu-id="fd721-606">Visa;MasterCard;Amex;Discover;Debit</span></span> |

<span data-ttu-id="fd721-607">\* この列のサンプル値を、独自の支払プロセッサの固有値に置き換える **必要があります** 。</span><span class="sxs-lookup"><span data-stu-id="fd721-607">\* You **must** replace the sample values in this column with unique values for your own payment processor.</span></span>
