---
title: "顧客注文の概要"
description: "このトピックでは、Retail Modern POS (MPOS) の顧客注文に関する情報を提供します。 顧客注文は、特別注文としても知られています。 このトピックには、関連パラメーターおよびトランザクション フローのディスカッションが含まれています。"
author: josaw1
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 260594
ms.assetid: 6fc835ef-d62e-4f23-9d49-50299be642ca
ms.search.region: global
ms.search.industry: Retail
ms.author: anpurush
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: ce6774ede836eb29e6ef2cd8d4baa9efb931020c
ms.contentlocale: ja-jp
ms.lasthandoff: 11/03/2017

---

# <a name="customer-orders-overview"></a><span data-ttu-id="e998c-105">顧客注文の概要</span><span class="sxs-lookup"><span data-stu-id="e998c-105">Customer orders overview</span></span>

[!include[banner](includes/banner.md)]


<span data-ttu-id="e998c-106">このトピックでは、Retail Modern POS (MPOS) の顧客注文に関する情報を提供します。</span><span class="sxs-lookup"><span data-stu-id="e998c-106">This topic provides information about customer orders in Retail Modern POS (MPOS).</span></span> <span data-ttu-id="e998c-107">顧客注文は、特別注文としても知られています。</span><span class="sxs-lookup"><span data-stu-id="e998c-107">Customer orders are also known as special orders.</span></span> <span data-ttu-id="e998c-108">このトピックには、関連パラメーターおよびトランザクション フローのディスカッションが含まれています。</span><span class="sxs-lookup"><span data-stu-id="e998c-108">The topic includes a discussion of related parameters and transaction flows.</span></span>

<span data-ttu-id="e998c-109">無指向性の小売チャンネルの世界では、多くの小売業者によって、さまざまな製品およびフルフィルメントの要件を満たすために、顧客注文または特別注文のオプションが用意されています。</span><span class="sxs-lookup"><span data-stu-id="e998c-109">In an omni-channel retail world, many retailers provide the option of customer orders, or special orders, to meet various product and fulfillment requirements.</span></span> <span data-ttu-id="e998c-110">以下に一般的なシナリオを挙げます。</span><span class="sxs-lookup"><span data-stu-id="e998c-110">Here are some typical scenarios:</span></span>

-   <span data-ttu-id="e998c-111">顧客が特定の日付に特定の住所まで製品の配送を希望しています。</span><span class="sxs-lookup"><span data-stu-id="e998c-111">A customer wants products to be delivered to a specific address on a specific date.</span></span>
-   <span data-ttu-id="e998c-112">顧客は、その製品を購入した店舗または場所とは異なる店舗または場所から製品の集荷を希望しています。</span><span class="sxs-lookup"><span data-stu-id="e998c-112">A customer wants to pick up products from a store or location that differs from the store or location where the customer purchased those products.</span></span>
-   <span data-ttu-id="e998c-113">顧客は、購入した製品を別の誰か受け取ってもらいたいと考えています。</span><span class="sxs-lookup"><span data-stu-id="e998c-113">A customer wants someone else to pick up products that the customer purchased.</span></span>

<span data-ttu-id="e998c-114">小売業者も、異なる時間や場所での商品の配送または受け取りが可能なため、顧客注文を使用して欠品による販売損失を最小限にします。</span><span class="sxs-lookup"><span data-stu-id="e998c-114">Retailers also use customer orders to minimize lost sales that stock outages might otherwise cause, because the merchandise can be delivered or picked up at a different time or place.</span></span>

## <a name="set-up-customer-orders"></a><span data-ttu-id="e998c-115">顧客注文の設定</span><span class="sxs-lookup"><span data-stu-id="e998c-115">Set up customer orders</span></span>
<span data-ttu-id="e998c-116">ここでは、顧客注文を履行する方法を定義するために**小売パラメーター** ページで設定できるパラメーターをいくつか説明します。</span><span class="sxs-lookup"><span data-stu-id="e998c-116">Here are some of the parameters that can be set on the **Retail parameters** page to define how customer orders are fulfilled:</span></span>

-   <span data-ttu-id="e998c-117">**既定の預金率** – 注文を確定する前に、顧客が前金として支払う必要のある金額を指定します。</span><span class="sxs-lookup"><span data-stu-id="e998c-117">**Default deposit percentage** – Specify the amount that the customer must pay as a deposit before an order can be confirmed.</span></span> <span data-ttu-id="e998c-118">既定の前金の額は、注文金額の割合として計算されます。</span><span class="sxs-lookup"><span data-stu-id="e998c-118">The default deposit amount is calculated as a percentage of the order value.</span></span> <span data-ttu-id="e998c-119">権限によって、店舗スタッフは [**前金の上書き**] を使用して金額を上書きできる場合があります。</span><span class="sxs-lookup"><span data-stu-id="e998c-119">Depending on privileges, a store associate might be able to override the amount by using **Deposit override**.</span></span>
-   <span data-ttu-id="e998c-120">**キャンセル料率** – 顧客注文がキャンセルされた際に料金が発生する場合、その料金の金額を指定します。</span><span class="sxs-lookup"><span data-stu-id="e998c-120">**Cancellation charge percentage** – If a charge will be applied when a customer order is canceled, specify the amount of that charge.</span></span>
-   <span data-ttu-id="e998c-121">**キャンセル料コード** – 顧客注文がキャンセルされた際に料金が発生する場合、その料金は販売注文の請求額コードに反映されます。</span><span class="sxs-lookup"><span data-stu-id="e998c-121">**Cancellation charge code** – If a charge will be applied when a customer order is canceled, that charge will be reflected under a charge code on the sales order.</span></span> <span data-ttu-id="e998c-122">このパラメーターを使用して、キャンセル料コードを定義します。</span><span class="sxs-lookup"><span data-stu-id="e998c-122">Use this parameter to define the cancellation charge code.</span></span>
-   <span data-ttu-id="e998c-123">**出荷費用コード** – 小売業者が顧客に出荷手数料を請求することができます。</span><span class="sxs-lookup"><span data-stu-id="e998c-123">**Shipping charge code** – Retailers can charge an extra fee for shipping merchandise to a customer.</span></span> <span data-ttu-id="e998c-124">その出荷費用は、販売注文の請求額コードに反映されます。</span><span class="sxs-lookup"><span data-stu-id="e998c-124">The amount of that shipping charge will be reflected under a charge code on the sales order.</span></span> <span data-ttu-id="e998c-125">このパラメーターを使用して、顧客注文の出荷費用に出荷費用コードをマップします。</span><span class="sxs-lookup"><span data-stu-id="e998c-125">Use this parameter to map the shipping charge code to shipping charges on the customer order.</span></span>
-   <span data-ttu-id="e998c-126">**出荷費用の返金** – 顧客注文に関連付けられる出荷費用が払戻可能かどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="e998c-126">**Refund shipping charges** – Specify whether shipping charges that are associated with a customer order are refundable.</span></span>
-   <span data-ttu-id="e998c-127">**承認なしで返金可能な最高額** – 出荷費用が払戻可能である場合、返品注文時の出荷費用払戻の最大金額を指定します。</span><span class="sxs-lookup"><span data-stu-id="e998c-127">**Maximum amount without approval** – If shipping charges are refundable, specify the maximum amount of shipping charge refunds across return orders.</span></span> <span data-ttu-id="e998c-128">この金額を超えた場合、払戻を進めるにはマネージャー オーバーライドが必要です。</span><span class="sxs-lookup"><span data-stu-id="e998c-128">If this amount is exceeded, manager override is required in order to continue with the refund.</span></span> <span data-ttu-id="e998c-129">次のシナリオに対応するには、出荷費用の払戻がもともと支払われた金額を超える場合があります。</span><span class="sxs-lookup"><span data-stu-id="e998c-129">To accommodate the following scenarios, a refund of shipping charges can exceed the amount that was originally paid:</span></span>
    -   <span data-ttu-id="e998c-130">費用は、販売注文ヘッダーのレベルで適用され、製品ラインの数個が返品される場合、すべての小売顧客を対象とする方法で、製品と数量に許可されている出荷費用の最大払戻額を決定することはできません。</span><span class="sxs-lookup"><span data-stu-id="e998c-130">Charges are applied at the level of the sales order header, and when some quantity of a product line is returned, the maximum refund of shipping charges that is allowed for the products and the quantity can't be determined in way that works for all retail customers.</span></span>
    -   <span data-ttu-id="e998c-131">出荷費用は、出荷のすべてのインスタンスに発生します。</span><span class="sxs-lookup"><span data-stu-id="e998c-131">Shipping charges are incurred for every instance of shipping.</span></span> <span data-ttu-id="e998c-132">顧客が製品の返品を複数回行い、小売業者のポリシーで小売業者が返品出荷費用を負担しないことを指定している場合、返品出荷費用は実際の出荷費用を超えます。</span><span class="sxs-lookup"><span data-stu-id="e998c-132">If a customer returns products multiple times, and the retailer’s policy specifies that the retailer will bear the cost of return shipping charges, the return shipping charges will be more than the actual shipping charges.</span></span>

## <a name="transaction-flow-for-customer-orders"></a><span data-ttu-id="e998c-133">顧客注文のトランザクション フロー</span><span class="sxs-lookup"><span data-stu-id="e998c-133">Transaction flow for customer orders</span></span>
### <a name="create-a-customer-order-in-retail-modern-pos"></a><span data-ttu-id="e998c-134">Retail Modern POS での顧客注文の作成</span><span class="sxs-lookup"><span data-stu-id="e998c-134">Create a customer order in Retail Modern POS</span></span>

1.  <span data-ttu-id="e998c-135">トランザクションに顧客を追加します。</span><span class="sxs-lookup"><span data-stu-id="e998c-135">Add a customer to the transaction.</span></span>
2.  <span data-ttu-id="e998c-136">製品をカートに追加します。</span><span class="sxs-lookup"><span data-stu-id="e998c-136">Add products to the cart.</span></span>
3.  <span data-ttu-id="e998c-137">[**顧客注文の作成**] をクリックして、注文タイプを選択します。</span><span class="sxs-lookup"><span data-stu-id="e998c-137">Click **Create customer order**, and then select the order type.</span></span> <span data-ttu-id="e998c-138">注文タイプは、[**顧客注文**] または [**見積**] のいずれかを指定できます。</span><span class="sxs-lookup"><span data-stu-id="e998c-138">The order type can be either **Customer order** or **Quote**.</span></span>
4.  <span data-ttu-id="e998c-139">[**選択された出荷**] または [**すべて出荷**] をクリックし、顧客 ID の住所に製品を出荷して、要求出荷日、出荷費用を指定します。</span><span class="sxs-lookup"><span data-stu-id="e998c-139">Click **Ship selected** or **Ship all** to ship the products to an address on the customer account, specify the requested shipping date, and specify shipping charges.</span></span>
5.  <span data-ttu-id="e998c-140">[**選択された集荷**] または [**すべて集荷**] をクリックして、特定の日付に現在の店舗または異なる店舗から集荷される製品を選択します。</span><span class="sxs-lookup"><span data-stu-id="e998c-140">Click **Pick up selected** or **Pick-up all** to select products that will be picked up from the current store or a different store on a specific date.</span></span>
6.  <span data-ttu-id="e998c-141">前金が必要な場合は、前金金額を回収します。</span><span class="sxs-lookup"><span data-stu-id="e998c-141">Collect the deposit amount, if a deposit is required.</span></span>

### <a name="edit-an-existing-customer-order"></a><span data-ttu-id="e998c-142">既存の顧客注文の編集</span><span class="sxs-lookup"><span data-stu-id="e998c-142">Edit an existing customer order</span></span>

1.  <span data-ttu-id="e998c-143">ホーム ページで [**注文の検索**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e998c-143">On the home page, click **Find an order**.</span></span>
2.  <span data-ttu-id="e998c-144">編集する注文を検索して選択します。</span><span class="sxs-lookup"><span data-stu-id="e998c-144">Find and select the order to edit.</span></span> <span data-ttu-id="e998c-145">ページの下部にある [**編集**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e998c-145">At the bottom of the page, click the **Edit**.</span></span>

### <a name="pick-up-an-order"></a><span data-ttu-id="e998c-146">注文の集荷</span><span class="sxs-lookup"><span data-stu-id="e998c-146">Pick up an order</span></span>

1.  <span data-ttu-id="e998c-147">ホーム ページで [**注文の検索**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e998c-147">On the home page, click **Find an order**.</span></span>
2.  <span data-ttu-id="e998c-148">集荷する注文を選択します。</span><span class="sxs-lookup"><span data-stu-id="e998c-148">Select the order to pick up.</span></span> <span data-ttu-id="e998c-149">ページの下部にある [**ピッキングと梱包**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e998c-149">At the bottom of the page, click **Picking and packing**.</span></span>
3.  <span data-ttu-id="e998c-150">[**集荷**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e998c-150">Click **Pick up**.</span></span>

### <a name="cancel-an-order"></a><span data-ttu-id="e998c-151">注文のキャンセル</span><span class="sxs-lookup"><span data-stu-id="e998c-151">Cancel an order</span></span>

1.  <span data-ttu-id="e998c-152">ホーム ページで [**注文の検索**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e998c-152">On the home page, click **Find an order**.</span></span>
2.  <span data-ttu-id="e998c-153">キャンセルする注文を選択します。</span><span class="sxs-lookup"><span data-stu-id="e998c-153">Select the order to cancel.</span></span> <span data-ttu-id="e998c-154">ページの下部にある [**キャンセル**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e998c-154">At the bottom of the page, click **Cancel**.</span></span>

#### <a name="create-a-return-order"></a><span data-ttu-id="e998c-155">返品注文の作成</span><span class="sxs-lookup"><span data-stu-id="e998c-155">Create a return order</span></span>

1.  <span data-ttu-id="e998c-156">ホーム ページで [**注文の検索**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e998c-156">On the home page, click **Find an order**.</span></span>
2.  <span data-ttu-id="e998c-157">返品する注文、注文の請求書を選択してから、返品する商品の製品ラインを選択します。</span><span class="sxs-lookup"><span data-stu-id="e998c-157">Select the order to return, select the invoice for the order, and then select the product line for the merchandise to return.</span></span>
3.  <span data-ttu-id="e998c-158">ページの下部にある [**返品注文**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e998c-158">At the bottom of the page, click the **Return order**.</span></span>

## <a name="asynchronous-transaction-flow-for-customer-orders"></a><span data-ttu-id="e998c-159">顧客注文の非同期トランザクション フロー</span><span class="sxs-lookup"><span data-stu-id="e998c-159">Asynchronous transaction flow for customer orders</span></span>
<span data-ttu-id="e998c-160">顧客注文は、同期モードまたは非同期モードで販売時点管理 (POS) クライアントから作成できます。</span><span class="sxs-lookup"><span data-stu-id="e998c-160">Customer orders can be created from the point of sale (POS) client in either synchronous mode or asynchronous mode.</span></span>

### <a name="enable-customer-orders-to-be-created-in-asynchronous-mode"></a><span data-ttu-id="e998c-161">非同期モードで作成する顧客注文の有効化</span><span class="sxs-lookup"><span data-stu-id="e998c-161">Enable customer orders to be created in asynchronous mode</span></span>

1.  <span data-ttu-id="e998c-162">[**小売り**] &gt; [**チャンネル設定**] &gt; [**POS 設定**] &gt; [**POS プロファイル**] &gt; [**機能プロファイル**] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="e998c-162">Click **Retail** &gt; **Channel setup** &gt; **POS setup** &gt; **POS profile** &gt; **Functionality profiles**.</span></span>
2.  <span data-ttu-id="e998c-163">[**一般**] クイック タブで、[**非同期モードで顧客注文を作成**] オプションを [**はい**] に設定します。</span><span class="sxs-lookup"><span data-stu-id="e998c-163">On the **General** FastTab, set the **Create customer order in async mode** option to **Yes**.</span></span>

<span data-ttu-id="e998c-164">[**非同期モードで顧客注文を作成**] オプションを [**はい**] に設定すると、顧客注文は Retail Transaction Service (RTS) が使用できる場合でも常に非同期モードで作成されます。</span><span class="sxs-lookup"><span data-stu-id="e998c-164">When the **Create customer order in async mode** option is set to **Yes**, customer orders are always created in asynchronous mode, even if Retail Transaction Service (RTS) is available.</span></span> <span data-ttu-id="e998c-165">このオプションを [**いいえ**] に設定した場合、顧客注文は RTS を使用して常に同期モードで作成されます。</span><span class="sxs-lookup"><span data-stu-id="e998c-165">If you set this option to **No**, customer orders are always created in synchronous mode by using RTS.</span></span> <span data-ttu-id="e998c-166">顧客注文が非同期モードで作成されると、プル (P) ジョブによって Retail に引っ張られ、挿入されます。</span><span class="sxs-lookup"><span data-stu-id="e998c-166">When customer orders are created in asynchronous mode, they are pulled and inserted into Retail by Pull (P) jobs.</span></span> <span data-ttu-id="e998c-167">[**注文の同期**] が手動またはバッチ処理で実行される場合、対応する販売注文は Retail で作成されます。</span><span class="sxs-lookup"><span data-stu-id="e998c-167">The corresponding sales orders are created in Retail when **Synchronize orders** is run either manually or through a batch process.</span></span>

<a name="see-also"></a><span data-ttu-id="e998c-168">参照</span><span class="sxs-lookup"><span data-stu-id="e998c-168">See also</span></span>
--------

[<span data-ttu-id="e998c-169">ハイブリッド顧客注文</span><span class="sxs-lookup"><span data-stu-id="e998c-169">Hybrid customer orders</span></span>](hybrid-customer-orders.md)




