---
title: Modern POS (MPOS) の顧客注文
description: このトピックでは、Modern POS (MPOS) の顧客注文に関する情報を提供します。 顧客注文は、特別注文としても知られています。 このトピックには、関連パラメーターおよびトランザクション フローのディスカッションが含まれています。
author: josaw1
manager: AnnBe
ms.date: 08/17/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailFunctionalityProfile
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
ms.openlocfilehash: a6fdc7b8d7ad65c9e4bf1d3b932b62918dea6e77
ms.sourcegitcommit: 7061a93f9f2b54aec4bc4bf0cc92691e86d383a6
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/20/2020
ms.locfileid: "3710262"
---
# <a name="customer-orders-in-modern-pos-mpos"></a><span data-ttu-id="f60e3-105">Modern POS (MPOS) の顧客注文</span><span class="sxs-lookup"><span data-stu-id="f60e3-105">Customer orders in Modern POS (MPOS)</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="f60e3-106">このトピックでは、Modern POS (MPOS) の顧客注文に関する情報を提供します。</span><span class="sxs-lookup"><span data-stu-id="f60e3-106">This topic provides information about customer orders in Modern POS (MPOS).</span></span> <span data-ttu-id="f60e3-107">顧客注文は、特別注文としても知られています。</span><span class="sxs-lookup"><span data-stu-id="f60e3-107">Customer orders are also known as special orders.</span></span> <span data-ttu-id="f60e3-108">このトピックには、関連パラメーターおよびトランザクション フローのディスカッションが含まれています。</span><span class="sxs-lookup"><span data-stu-id="f60e3-108">The topic includes a discussion of related parameters and transaction flows.</span></span>

<span data-ttu-id="f60e3-109">無指向性のコマース チャネルの世界では、多くの小売業者によって、さまざまな製品およびフルフィルメントの要件を満たすために、顧客注文または特別注文のオプションが用意されています。</span><span class="sxs-lookup"><span data-stu-id="f60e3-109">In an omni-channel commerce world, many retailers provide the option of customer orders, or special orders, to meet various product and fulfillment requirements.</span></span> <span data-ttu-id="f60e3-110">以下に一般的なシナリオを挙げます。</span><span class="sxs-lookup"><span data-stu-id="f60e3-110">Here are some typical scenarios:</span></span>

- <span data-ttu-id="f60e3-111">顧客が特定の日付に特定の住所まで製品の配送を希望しています。</span><span class="sxs-lookup"><span data-stu-id="f60e3-111">A customer wants products to be delivered to a specific address on a specific date.</span></span>
- <span data-ttu-id="f60e3-112">顧客は、その製品を購入した店舗または場所とは異なる店舗または場所から製品の集荷を希望しています。</span><span class="sxs-lookup"><span data-stu-id="f60e3-112">A customer wants to pick up products from a store or location that differs from the store or location where the customer purchased those products.</span></span>
- <span data-ttu-id="f60e3-113">顧客は、購入した製品を別の誰か受け取ってもらいたいと考えています。</span><span class="sxs-lookup"><span data-stu-id="f60e3-113">A customer wants someone else to pick up products that the customer purchased.</span></span>

<span data-ttu-id="f60e3-114">小売業者も、異なる時間や場所での商品の配送または受け取りが可能なため、顧客注文を使用して欠品による販売損失を最小限にします。</span><span class="sxs-lookup"><span data-stu-id="f60e3-114">Retailers also use customer orders to minimize lost sales that stock outages might otherwise cause, because the merchandise can be delivered or picked up at a different time or place.</span></span>

## <a name="set-up-customer-orders"></a><span data-ttu-id="f60e3-115">顧客注文の設定</span><span class="sxs-lookup"><span data-stu-id="f60e3-115">Set up customer orders</span></span>

<span data-ttu-id="f60e3-116">ここでは、顧客注文を履行する方法を定義するために **Commerce パラメーター** ページで設定できるパラメーターをいくつか説明します。</span><span class="sxs-lookup"><span data-stu-id="f60e3-116">Here are some of the parameters that can be set on the **Commerce parameters** page to define how customer orders are fulfilled:</span></span>

- <span data-ttu-id="f60e3-117">**既定の預金率** – 注文を確定する前に、顧客が前金として支払う必要のある金額を指定します。</span><span class="sxs-lookup"><span data-stu-id="f60e3-117">**Default deposit percentage** – Specify the amount that the customer must pay as a deposit before an order can be confirmed.</span></span> <span data-ttu-id="f60e3-118">既定の前金の額は、注文金額の割合として計算されます。</span><span class="sxs-lookup"><span data-stu-id="f60e3-118">The default deposit amount is calculated as a percentage of the order value.</span></span> <span data-ttu-id="f60e3-119">権限によって、店舗スタッフは**前金の上書き**を使用して金額を上書きできる場合があります。</span><span class="sxs-lookup"><span data-stu-id="f60e3-119">Depending on privileges, a store associate might be able to override the amount by using **Deposit override**.</span></span>
- <span data-ttu-id="f60e3-120">**キャンセル料率** – 顧客注文がキャンセルされた際に料金が発生する場合、その料金の金額を指定します。</span><span class="sxs-lookup"><span data-stu-id="f60e3-120">**Cancellation charge percentage** – If a charge will be applied when a customer order is canceled, specify the amount of that charge.</span></span>
- <span data-ttu-id="f60e3-121">**キャンセル料コード** – 顧客注文がキャンセルされた際に料金が発生する場合、その料金は販売注文の請求額コードに反映されます。</span><span class="sxs-lookup"><span data-stu-id="f60e3-121">**Cancellation charge code** – If a charge will be applied when a customer order is canceled, that charge will be reflected under a charge code on the sales order.</span></span> <span data-ttu-id="f60e3-122">このパラメーターを使用して、キャンセル料コードを定義します。</span><span class="sxs-lookup"><span data-stu-id="f60e3-122">Use this parameter to define the cancellation charge code.</span></span>
- <span data-ttu-id="f60e3-123">**出荷費用コード** – 小売業者が顧客に出荷手数料を請求することができます。</span><span class="sxs-lookup"><span data-stu-id="f60e3-123">**Shipping charge code** – Retailers can charge an extra fee for shipping merchandise to a customer.</span></span> <span data-ttu-id="f60e3-124">その出荷費用は、販売注文の請求額コードに反映されます。</span><span class="sxs-lookup"><span data-stu-id="f60e3-124">The amount of that shipping charge will be reflected under a charge code on the sales order.</span></span> <span data-ttu-id="f60e3-125">このパラメーターを使用して、顧客注文の出荷費用に出荷費用コードをマップします。</span><span class="sxs-lookup"><span data-stu-id="f60e3-125">Use this parameter to map the shipping charge code to shipping charges on the customer order.</span></span>
- <span data-ttu-id="f60e3-126">**出荷費用の返金** – 顧客注文に関連付けられる出荷費用が払戻可能かどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="f60e3-126">**Refund shipping charges** – Specify whether shipping charges that are associated with a customer order are refundable.</span></span>
- <span data-ttu-id="f60e3-127">**承認なしで返金可能な最高額** – 出荷費用が払戻可能である場合、返品注文時の出荷費用払戻の最大金額を指定します。</span><span class="sxs-lookup"><span data-stu-id="f60e3-127">**Maximum amount without approval** – If shipping charges are refundable, specify the maximum amount of shipping charge refunds across return orders.</span></span> <span data-ttu-id="f60e3-128">この金額を超えた場合、払戻を進めるにはマネージャー オーバーライドが必要です。</span><span class="sxs-lookup"><span data-stu-id="f60e3-128">If this amount is exceeded, manager override is required in order to continue with the refund.</span></span> <span data-ttu-id="f60e3-129">次のシナリオに対応するには、出荷費用の払戻がもともと支払われた金額を超える場合があります。</span><span class="sxs-lookup"><span data-stu-id="f60e3-129">To accommodate the following scenarios, a refund of shipping charges can exceed the amount that was originally paid:</span></span>

    - <span data-ttu-id="f60e3-130">費用は、販売注文ヘッダーのレベルで適用され、製品ラインの数個が返品される場合、すべての顧客を対象とする方法で、製品と数量に許可されている出荷費用の最大払戻額を決定することはできません。</span><span class="sxs-lookup"><span data-stu-id="f60e3-130">Charges are applied at the level of the sales order header, and when some quantity of a product line is returned, the maximum refund of shipping charges that is allowed for the products and the quantity can't be determined in way that works for all customers.</span></span>
    - <span data-ttu-id="f60e3-131">出荷費用は、出荷のすべてのインスタンスに発生します。</span><span class="sxs-lookup"><span data-stu-id="f60e3-131">Shipping charges are incurred for every instance of shipping.</span></span> <span data-ttu-id="f60e3-132">顧客が製品の返品を複数回行い、小売業者のポリシーで小売業者が返品出荷費用を負担しないことを指定している場合、返品出荷費用は実際の出荷費用を超えます。</span><span class="sxs-lookup"><span data-stu-id="f60e3-132">If a customer returns products multiple times, and the retailer's policy specifies that the retailer will bear the cost of return shipping charges, the return shipping charges will be more than the actual shipping charges.</span></span>
    

## <a name="disable-option-to-pay-later"></a><span data-ttu-id="f60e3-133">後で支払うオプションを無効にする</span><span class="sxs-lookup"><span data-stu-id="f60e3-133">Disable option to pay later</span></span>

<span data-ttu-id="f60e3-134">Commerce バージョン 10.0.12 およびそれ以降では、業者は、POS で顧客の注文が作成されたときに後で支払うオプションを削除することができます。</span><span class="sxs-lookup"><span data-stu-id="f60e3-134">In Commerce version 10.0.12 and later, merchants can remove the option to pay later when a customer order is created at the POS.</span></span> <span data-ttu-id="f60e3-135">このオプションを無効にするには、後で支払うことが許可されていないチャネルの **機能プロファイル** を開き、**編集** を選択します。</span><span class="sxs-lookup"><span data-stu-id="f60e3-135">To disable the option, open the **Functionality profile** for the channel that paying later is not allowed in, and then select **Edit**.</span></span> <span data-ttu-id="f60e3-136">**全般** タブで、**フィルフィルメントの支払必須** のドロップダウンを選択します。</span><span class="sxs-lookup"><span data-stu-id="f60e3-136">On the **General** tab, select the dropdown for **Require payment for fulfillment**.</span></span> <span data-ttu-id="f60e3-137">後で支払うことを POS で許可しない場合、**要カード** を選択し、**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="f60e3-137">If paying later should not be allowed at the POS, select **Card required** and select **Save**.</span></span> <span data-ttu-id="f60e3-138">**1070** 配送スケジュールを実行して、この変更をチャネルに同期させます。</span><span class="sxs-lookup"><span data-stu-id="f60e3-138">Run the **1070** distribution schedule to synchronize this change to the channel.</span></span> 

## <a name="transaction-flow-for-customer-orders"></a><span data-ttu-id="f60e3-139">顧客注文のトランザクション フロー</span><span class="sxs-lookup"><span data-stu-id="f60e3-139">Transaction flow for customer orders</span></span>

### <a name="create-a-customer-order-in-modern-pos"></a><span data-ttu-id="f60e3-140">Modern POS で顧客注文を作成する</span><span class="sxs-lookup"><span data-stu-id="f60e3-140">Create a customer order in Modern POS</span></span>

1. <span data-ttu-id="f60e3-141">トランザクションに顧客を追加します。</span><span class="sxs-lookup"><span data-stu-id="f60e3-141">Add a customer to the transaction.</span></span>
2. <span data-ttu-id="f60e3-142">製品をカートに追加します。</span><span class="sxs-lookup"><span data-stu-id="f60e3-142">Add products to the cart.</span></span>
3. <span data-ttu-id="f60e3-143">**顧客注文の作成**をクリックして、注文タイプを選択します。</span><span class="sxs-lookup"><span data-stu-id="f60e3-143">Click **Create customer order**, and then select the order type.</span></span> <span data-ttu-id="f60e3-144">注文タイプは、**顧客注文**または**見積**のいずれかを指定できます。</span><span class="sxs-lookup"><span data-stu-id="f60e3-144">The order type can be either **Customer order** or **Quote**.</span></span>
4. <span data-ttu-id="f60e3-145">**選択された出荷**または**すべて出荷**をクリックし、顧客 ID の住所に製品を出荷して、要求出荷日、出荷費用を指定します。</span><span class="sxs-lookup"><span data-stu-id="f60e3-145">Click **Ship selected** or **Ship all** to ship the products to an address on the customer account, specify the requested shipping date, and specify shipping charges.</span></span>
5. <span data-ttu-id="f60e3-146">**選択された集荷**または**すべて集荷**をクリックして、特定の日付に現在の店舗または異なる店舗から集荷される製品を選択します。</span><span class="sxs-lookup"><span data-stu-id="f60e3-146">Click **Pick up selected** or **Pick-up all** to select products that will be picked up from the current store or a different store on a specific date.</span></span>
6. <span data-ttu-id="f60e3-147">前金が必要な場合は、前金金額を回収します。</span><span class="sxs-lookup"><span data-stu-id="f60e3-147">Collect the deposit amount, if a deposit is required.</span></span>

### <a name="edit-an-existing-customer-order"></a><span data-ttu-id="f60e3-148">既存の顧客注文の編集</span><span class="sxs-lookup"><span data-stu-id="f60e3-148">Edit an existing customer order</span></span>

1. <span data-ttu-id="f60e3-149">ホーム ページで**注文の検索**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="f60e3-149">On the home page, click **Find an order**.</span></span>
2. <span data-ttu-id="f60e3-150">編集する注文を検索して選択します。</span><span class="sxs-lookup"><span data-stu-id="f60e3-150">Find and select the order to edit.</span></span> <span data-ttu-id="f60e3-151">ページの下部にある**編集**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="f60e3-151">At the bottom of the page, click the **Edit**.</span></span>

### <a name="pick-up-an-order"></a><span data-ttu-id="f60e3-152">注文の集荷</span><span class="sxs-lookup"><span data-stu-id="f60e3-152">Pick up an order</span></span>

1. <span data-ttu-id="f60e3-153">ホーム ページで**注文の検索**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="f60e3-153">On the home page, click **Find an order**.</span></span>
2. <span data-ttu-id="f60e3-154">集荷する注文を選択します。</span><span class="sxs-lookup"><span data-stu-id="f60e3-154">Select the order to pick up.</span></span> <span data-ttu-id="f60e3-155">ページの下部にある**ピッキングと梱包**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="f60e3-155">At the bottom of the page, click **Picking and packing**.</span></span>
3. <span data-ttu-id="f60e3-156">**集荷**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="f60e3-156">Click **Pick up**.</span></span>

### <a name="cancel-an-order"></a><span data-ttu-id="f60e3-157">注文のキャンセル</span><span class="sxs-lookup"><span data-stu-id="f60e3-157">Cancel an order</span></span>

1. <span data-ttu-id="f60e3-158">ホーム ページで**注文の検索**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="f60e3-158">On the home page, click **Find an order**.</span></span>
2. <span data-ttu-id="f60e3-159">キャンセルする注文を選択します。</span><span class="sxs-lookup"><span data-stu-id="f60e3-159">Select the order to cancel.</span></span> <span data-ttu-id="f60e3-160">ページの下部にある**キャンセル**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="f60e3-160">At the bottom of the page, click **Cancel**.</span></span>

### <a name="create-a-return-order"></a><span data-ttu-id="f60e3-161">返品注文の作成</span><span class="sxs-lookup"><span data-stu-id="f60e3-161">Create a return order</span></span>

1. <span data-ttu-id="f60e3-162">ホーム ページで**注文の検索**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="f60e3-162">On the home page, click **Find an order**.</span></span>
2. <span data-ttu-id="f60e3-163">返品する注文、注文の請求書を選択してから、返品する商品の製品ラインを選択します。</span><span class="sxs-lookup"><span data-stu-id="f60e3-163">Select the order to return, select the invoice for the order, and then select the product line for the merchandise to return.</span></span>
3. <span data-ttu-id="f60e3-164">ページの下部にある**返品注文**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="f60e3-164">At the bottom of the page, click the **Return order**.</span></span>

## <a name="asynchronous-transaction-flow-for-customer-orders"></a><span data-ttu-id="f60e3-165">顧客注文の非同期トランザクション フロー</span><span class="sxs-lookup"><span data-stu-id="f60e3-165">Asynchronous transaction flow for customer orders</span></span>

<span data-ttu-id="f60e3-166">顧客注文は、同期モードまたは非同期モードで販売時点管理 (POS) クライアントから作成できます。</span><span class="sxs-lookup"><span data-stu-id="f60e3-166">Customer orders can be created from the point of sale (POS) client in either synchronous mode or asynchronous mode.</span></span>

### <a name="enable-customer-orders-to-be-created-in-asynchronous-mode"></a><span data-ttu-id="f60e3-167">非同期モードで作成する顧客注文の有効化</span><span class="sxs-lookup"><span data-stu-id="f60e3-167">Enable customer orders to be created in asynchronous mode</span></span>

1. <span data-ttu-id="f60e3-168">**Retail と Commerce** &gt; **チャネル設定** &gt; **POS 設定** &gt; **POS プロファイル** &gt; **機能プロファイル**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="f60e3-168">Click **Retail and Commerce** &gt; **Channel setup** &gt; **POS setup** &gt; **POS profile** &gt; **Functionality profiles**.</span></span>
2. <span data-ttu-id="f60e3-169">**一般**クイック タブで、**非同期モードで顧客注文を作成**オプションを**はい**に設定します。</span><span class="sxs-lookup"><span data-stu-id="f60e3-169">On the **General** FastTab, set the **Create customer order in async mode** option to **Yes**.</span></span>

<span data-ttu-id="f60e3-170">**非同期モードで顧客注文を作成**オプションを**はい**に設定すると、顧客注文は Retail Transaction Service (RTS) が使用できる場合でも常に非同期モードで作成されます。</span><span class="sxs-lookup"><span data-stu-id="f60e3-170">When the **Create customer order in async mode** option is set to **Yes**, customer orders are always created in asynchronous mode, even if Retail Transaction Service (RTS) is available.</span></span> <span data-ttu-id="f60e3-171">このオプションを**いいえ**に設定した場合、顧客注文は RTS を使用して常に同期モードで作成されます。</span><span class="sxs-lookup"><span data-stu-id="f60e3-171">If you set this option to **No**, customer orders are always created in synchronous mode by using RTS.</span></span> <span data-ttu-id="f60e3-172">顧客注文が非同期モードで作成されると、プル (P) ジョブによって Commerce に引っ張られ、挿入されます。</span><span class="sxs-lookup"><span data-stu-id="f60e3-172">When customer orders are created in asynchronous mode, they are pulled and inserted into Commerce by Pull (P) jobs.</span></span> <span data-ttu-id="f60e3-173">**注文の同期**が手動またはバッチ処理で実行される場合、対応する販売注文が作成されます。</span><span class="sxs-lookup"><span data-stu-id="f60e3-173">The corresponding sales orders are created when **Synchronize orders** is run either manually or through a batch process.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="f60e3-174">その他のリソース</span><span class="sxs-lookup"><span data-stu-id="f60e3-174">Additional resources</span></span>

[<span data-ttu-id="f60e3-175">ハイブリッド顧客注文</span><span class="sxs-lookup"><span data-stu-id="f60e3-175">Hybrid customer orders</span></span>](hybrid-customer-orders.md)
