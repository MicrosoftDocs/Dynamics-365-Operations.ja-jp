---
title: 返品原価価格と返品のロット ID
description: 顧客に製品を販売したときは、返品の原価を製品の原価と等しくする場合があります。 **返品のロット ID**を使用してこれを行うことができます。
author: ShylaThompson
manager: AnnBe
ms.date: 04/30/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReturnTableListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 33cd3d50fe342ba12a17419f4e759c243a60b3e0
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/15/2019
ms.locfileid: "1565537"
---
# <a name="return-cost-price-and-return-lot-id"></a><span data-ttu-id="a7045-104">返品原価価格と返品のロット ID</span><span class="sxs-lookup"><span data-stu-id="a7045-104">Return cost price and return lot ID</span></span>        

[!include [banner](../includes/banner.md)]



<span data-ttu-id="a7045-105">在庫に戻される製品の原価は、製品の現在の原価を使用して計算されます。</span><span class="sxs-lookup"><span data-stu-id="a7045-105">The cost of products that are returned to inventory is calculated by using the current cost of the products.</span></span> <span data-ttu-id="a7045-106">ただし、顧客に製品を販売したときは、返品の原価を製品の原価と等しくする場合があります。</span><span class="sxs-lookup"><span data-stu-id="a7045-106">However, you might want the cost of the returned products to equal the cost of the products at the time when you sold the products to the customer.</span></span> <span data-ttu-id="a7045-107">**販売注文**フォームの**明細行の詳細**クイック タブで、**返品のロット ID**フィールドを使用してこれを行うことができます。</span><span class="sxs-lookup"><span data-stu-id="a7045-107">You can do this by using the **Return lot ID** field on the **Line details** FastTab in the **Sales order** form.</span></span>

<span data-ttu-id="a7045-108">たとえば、次のシナリオを考えてみます。</span><span class="sxs-lookup"><span data-stu-id="a7045-108">For example, consider the following scenario.</span></span> <span data-ttu-id="a7045-109">顧客に請求書を送付します。</span><span class="sxs-lookup"><span data-stu-id="a7045-109">You invoice a customer.</span></span> <span data-ttu-id="a7045-110">その後、顧客に出荷された製品が返品されます。</span><span class="sxs-lookup"><span data-stu-id="a7045-110">Then, the customer returns the delivered products to you.</span></span> <span data-ttu-id="a7045-111">その製品を在庫に返します。</span><span class="sxs-lookup"><span data-stu-id="a7045-111">You return the products to stock.</span></span> <span data-ttu-id="a7045-112">この場合、その顧客の返品された製品を貸方に記入するとき、その製品の原価は製品の現在の原価を使用して計算されます。</span><span class="sxs-lookup"><span data-stu-id="a7045-112">In this case, when you credit the customer for the returned products, the cost of those products is calculated by using the current cost of the products.</span></span> <span data-ttu-id="a7045-113">ただし、**返品のロット ID**フィールドを使用する場合は、返品された製品の原価は、顧客に対する元の販売請求書の原価を使用して計算されます。</span><span class="sxs-lookup"><span data-stu-id="a7045-113">However, if you use the **Return lot ID** field, the cost of the returned products is calculated by using the cost on the invoice of the original sale to the customer.</span></span>

<span data-ttu-id="a7045-114">顧客からの返品の現在の原価以外の原価を使用するには、次の方法の 1 つを使用します。</span><span class="sxs-lookup"><span data-stu-id="a7045-114">To use a cost other than the current cost for returns from a customer, use one of the following methods.</span></span>

## <a name="method-1-manually-enter-the-return-cost-price"></a><span data-ttu-id="a7045-115">方法 1: 返品原価価格を手動で入力</span><span class="sxs-lookup"><span data-stu-id="a7045-115">Method 1: Manually enter the return cost price</span></span>

<span data-ttu-id="a7045-116">品目を返品注文に追加する場合、既定では、その品目は現在の原価価格で在庫に戻されます。</span><span class="sxs-lookup"><span data-stu-id="a7045-116">By default, when you add items to a return order, the items are returned to inventory at the current cost price.</span></span> <span data-ttu-id="a7045-117">別の返品原価価格を指定するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="a7045-117">To specify a different return cost price, follow these steps.</span></span>

1.  <span data-ttu-id="a7045-118">**販売とマーケティング** \> **共通** \> **返品注文** \> **すべての返品注文**の順にクリックします。</span><span class="sxs-lookup"><span data-stu-id="a7045-118">Click **Sales and marketing** \> **Common** \> **Return orders** \> **All return orders**.</span></span>

2.  <span data-ttu-id="a7045-119">**アクション ウィンドウ**の**新規**グループで、**返品注文**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a7045-119">On the **Action Pane**, in the **New** group, click **Return order**.</span></span>

3.  <span data-ttu-id="a7045-120">**返品注文の作成**フォームで、顧客勘定を選択し、**OK**をクリックしします。</span><span class="sxs-lookup"><span data-stu-id="a7045-120">In the **Create return order** form, select a customer account, and then click **OK**.</span></span>

4.  <span data-ttu-id="a7045-121">**返品注文 - RMA 番号: %1、%2** フォームで、品目を選択し、**数量**フィールドに負の数量を入力します。</span><span class="sxs-lookup"><span data-stu-id="a7045-121">In the **Return order - RMA number: %1, %2** form, select an item, and then enter a negative quantity in the **Quantity** field.</span></span>

5.  <span data-ttu-id="a7045-122">**明細行の詳細**クイック タブをクリックします。</span><span class="sxs-lookup"><span data-stu-id="a7045-122">Click the **Line details** FastTab.</span></span>

6.  <span data-ttu-id="a7045-123">**一般**タブで、**返品原価価格**フィールドの値を入力します。</span><span class="sxs-lookup"><span data-stu-id="a7045-123">On the **General** tab, enter a value in the **Return cost price** field.</span></span> <span data-ttu-id="a7045-124">この値は、商品が在庫に戻されたときに使用されます。</span><span class="sxs-lookup"><span data-stu-id="a7045-124">This value is used when the goods are returned to inventory.</span></span> <span data-ttu-id="a7045-125">値を入力しなかった場合、商品が在庫に戻されたとき、現在の原価価格が使用されます。</span><span class="sxs-lookup"><span data-stu-id="a7045-125">If you do not enter a value, the current cost price is used when the goods are returned to inventory.</span></span>

## <a name="method-2-automatically-generate-the-cost-price-based-on-the-customer-invoice-line"></a><span data-ttu-id="a7045-126">方法 2: 顧客請求明細行に基づいて、原価価格を自動的に生成</span><span class="sxs-lookup"><span data-stu-id="a7045-126">Method 2: Automatically generate the cost price based on the customer invoice line</span></span>

<span data-ttu-id="a7045-127">これは、返品明細行の作成に使用する推奨される方法です。</span><span class="sxs-lookup"><span data-stu-id="a7045-127">This is the preferred method to use to create return lines.</span></span> <span data-ttu-id="a7045-128">顧客に製品を販売した時点の製品の原価を使用するには、返品注文を作成し、返品する販売明細行を指定します。</span><span class="sxs-lookup"><span data-stu-id="a7045-128">To use the cost of the products at the time when you sold the products to the customer, create a return order and specify a sales line to return.</span></span>

1.  <span data-ttu-id="a7045-129">**販売とマーケティング** \> **共通** \> **返品注文** \> **すべての返品注文**の順にクリックします。</span><span class="sxs-lookup"><span data-stu-id="a7045-129">Click **Sales and marketing** \> **Common** \> **Return orders** \> **All return orders**.</span></span>

2.  <span data-ttu-id="a7045-130">**アクション ウィンドウ**の**新規**グループで、**返品注文**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a7045-130">On the **Action Pane**, in the **New** group, click **Return order**.</span></span>

3.  <span data-ttu-id="a7045-131">**返品注文の作成**フォームで、顧客勘定を選択し、**OK**をクリックしします。</span><span class="sxs-lookup"><span data-stu-id="a7045-131">In the **Create return order** form, select a customer account, and then click **OK**.</span></span>

4.  <span data-ttu-id="a7045-132">**アクション ウィンドウ**の**返品注文 - RMA 番号: %1、%2** フォームで、**販売注文の検索**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a7045-132">In the **Return order - RMA number: %1, %2** form, on the **Action Pane**, click **Find sales order**.</span></span>

5.  <span data-ttu-id="a7045-133">**販売注文の検索**フォームで、返品する請求明細行を選択し、**OK**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a7045-133">In the **Find sales order** form, select the invoice line to return, and then click **OK**.</span></span>
    
    <span data-ttu-id="a7045-134">**一般**タブの**明細行の詳細**クイック タブで、**返品のロット ID**フィールドは、元の販売明細行の値を表示します。</span><span class="sxs-lookup"><span data-stu-id="a7045-134">On the **Line details** FastTab, on the **General** tab, the **Return lot ID** field displays the value from the original sales line.</span></span> <span data-ttu-id="a7045-135">また、**返品原価価格**フィールドには、元の販売注文明細行から原価価値が表示されます。</span><span class="sxs-lookup"><span data-stu-id="a7045-135">Additionally, the **Return cost price** field displays the cost value from the original sales line.</span></span>

## <a name="cost-calculation-example"></a><span data-ttu-id="a7045-136">原価計算の例</span><span class="sxs-lookup"><span data-stu-id="a7045-136">Cost calculation example</span></span>

<span data-ttu-id="a7045-137">返品注文明細行の**返品のロット ID**フィールドを使用して返品原価価格を指定するとき、返品注文明細行の原価が使用されます。</span><span class="sxs-lookup"><span data-stu-id="a7045-137">When you use the **Return lot ID** field on a return order line to specify the return cost price, the cost on the return order line is used.</span></span> <span data-ttu-id="a7045-138">在庫決算または再計算機能を実行する場合、原価が元の販売注文明細行に対して調整されます。</span><span class="sxs-lookup"><span data-stu-id="a7045-138">If you run the inventory close or recalculation functionality, the cost is adjusted on the original sales line.</span></span> <span data-ttu-id="a7045-139">返品注文明細行の原価は、区分ごとに同じ原価を反映するように自動的に調整されます。</span><span class="sxs-lookup"><span data-stu-id="a7045-139">The cost on the return order line is automatically adjusted to reflect the same cost per piece.</span></span>

1.  <span data-ttu-id="a7045-140">テストという製品を作成し、リリースします。</span><span class="sxs-lookup"><span data-stu-id="a7045-140">Create and release a product that is named Test.</span></span> <span data-ttu-id="a7045-141">**リリース済製品の詳細**フォームで、次の情報を指定します。</span><span class="sxs-lookup"><span data-stu-id="a7045-141">In the **Released product details** form, specify the following information:</span></span>
    
    1.  <span data-ttu-id="a7045-142">**品目グループ**フィールドの**原価の管理**クイック タブで、**パーツ**グループを選択します。</span><span class="sxs-lookup"><span data-stu-id="a7045-142">On the **Manage costs** FastTab, in the **Item group** field, select the **Parts** group.</span></span>
    
    2.  <span data-ttu-id="a7045-143">**一般**クイックタブの、**品目モデル グループ**フィールドで、**DEF**を選択します。</span><span class="sxs-lookup"><span data-stu-id="a7045-143">On the **General** FastTab, in the **Item model group** field, select **DEF**.</span></span>
    
    3.  <span data-ttu-id="a7045-144">**購買**クイック タブの、**価格**フィールドに、品目の原価価格として 10.00 を入力します。</span><span class="sxs-lookup"><span data-stu-id="a7045-144">On the **Purchase** FastTab, in the **Price** field, type 10.00 as the cost price of the item.</span></span>
    
    4.  <span data-ttu-id="a7045-145">**アクション ペイン**で、**分析コード グループ**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a7045-145">On the **Action Pane**, click **Dimension groups**.</span></span> <span data-ttu-id="a7045-146">**保管分析コード グループ**フィールドで、**サイトと倉庫のみ**を選択します。</span><span class="sxs-lookup"><span data-stu-id="a7045-146">In the **Storage dimension group** field, select **Site and Warehouse only**.</span></span> <span data-ttu-id="a7045-147">**追跡用分析コード グループ**フィールドで、**有効な追跡用分析コードなし**を選択します。</span><span class="sxs-lookup"><span data-stu-id="a7045-147">In the **Tracking dimension group** field, select **No active tracking dimensions**.</span></span>

2.  <span data-ttu-id="a7045-148">1 個 6.00 のテスト品目の 10 個の発注書を作成し、発注書の請求書を転記します。</span><span class="sxs-lookup"><span data-stu-id="a7045-148">Create a purchase order for 10 pieces of the Test item at 6.00 per piece, and then post an invoice for the purchase order.</span></span>
    
    <span data-ttu-id="a7045-149">1 個 8.00 のテスト品目 10 個のもう 1 つの発注書を作成し、発注書の請求書を転記します。</span><span class="sxs-lookup"><span data-stu-id="a7045-149">Create a second purchase order for 10 pieces of the Test item at 8.00 per piece, and then post an invoice for the purchase order.</span></span>

3.  <span data-ttu-id="a7045-150">テスト品目 5 個を販売する販売注文の請求書を転記します。</span><span class="sxs-lookup"><span data-stu-id="a7045-150">Post an invoice for a sales order to sell five pieces of the Test item.</span></span>
    
    <span data-ttu-id="a7045-151">この場合、販売注文明細行が 35.00 (5 個 \* 7.00 平均原価/1 個) で原価計算されます。</span><span class="sxs-lookup"><span data-stu-id="a7045-151">In this case, the sales order line is costed at 35.00 (5 pieces \* 7.00 average cost per piece).</span></span>

4.  <span data-ttu-id="a7045-152">顧客に対する返品注文を作成します</span><span class="sxs-lookup"><span data-stu-id="a7045-152">Create a return order for the customer.</span></span> <span data-ttu-id="a7045-153">**販売注文の検索**フォームで、請求明細行を選択し、**OK**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a7045-153">In the **Find sales order** form, select the invoice line, and then click **OK**.</span></span>

5.  <span data-ttu-id="a7045-154">**返品注文 - RMA 番号: %1、%2** フォームで、テスト項目を返すため生成された返品注文を確認します。</span><span class="sxs-lookup"><span data-stu-id="a7045-154">In the **Return order - RMA number: %1, %2** form, verify that a return order is generated to return the Test item.</span></span> <span data-ttu-id="a7045-155">返品注文の数量が -5.00 に設定されます。</span><span class="sxs-lookup"><span data-stu-id="a7045-155">The quantity of the return order is set to -5.00.</span></span>
    
    <span data-ttu-id="a7045-156">**返品のロット ID**フィールドには、ロット IDが表示されます。</span><span class="sxs-lookup"><span data-stu-id="a7045-156">The **Return lot ID** field displays a lot ID.</span></span> <span data-ttu-id="a7045-157">このロット ID は、顧客に販売された品目の元の販売注文から取得されます。</span><span class="sxs-lookup"><span data-stu-id="a7045-157">This lot ID is taken from the original sales order of the item that was sold to the customer.</span></span> <span data-ttu-id="a7045-158">**返品原価価格**フィールドには、元の販売注文明細行から原価価格が表示されます。</span><span class="sxs-lookup"><span data-stu-id="a7045-158">The **Return cost price** field displays the cost price from the original sales line.</span></span>

6.  <span data-ttu-id="a7045-159">返品品目の受入を登録します。</span><span class="sxs-lookup"><span data-stu-id="a7045-159">Register the receipt of the returned items.</span></span>

7.  <span data-ttu-id="a7045-160">返品品目の梱包明細を転記します。</span><span class="sxs-lookup"><span data-stu-id="a7045-160">Post a packing slip for the returned items.</span></span>

8.  <span data-ttu-id="a7045-161">返品注文の請求書を転記します。</span><span class="sxs-lookup"><span data-stu-id="a7045-161">Post an invoice for the return order.</span></span> <span data-ttu-id="a7045-162">**すべての販売注文**リスト ページで、**返品注文**が注文タイプである販売注文を選択します。</span><span class="sxs-lookup"><span data-stu-id="a7045-162">On the **All sales orders** list page, select a sales order for which **Returned order** is the order type.</span></span>

9.  <span data-ttu-id="a7045-163">**在庫トランザクション**フォームを開きます。</span><span class="sxs-lookup"><span data-stu-id="a7045-163">Open the **Inventory transactions** form.</span></span> <span data-ttu-id="a7045-164">返品の原価は、**返品原価価格**フィールドの値を使用して 1 個 7.00 であり、**原価金額**フィールドで合計 35.00 であることを確認します。</span><span class="sxs-lookup"><span data-stu-id="a7045-164">Verify that the return is costed at 7.00 per piece by using the value in the **Return cost price** field, for a total of 35.00 in the **Cost amount** field.</span></span> <span data-ttu-id="a7045-165">**返品注文 - RMA 番号: %1、%2** フォームから**在庫トランザクション**フォームを開くことができます。</span><span class="sxs-lookup"><span data-stu-id="a7045-165">You can open the **Inventory transactions** form from the **Return order - RMA number: %1, %2** form.</span></span> <span data-ttu-id="a7045-166">**明細行**グリッドで、**在庫** \> **トランザクション**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a7045-166">In the **Lines** grid, click **Inventory** \> **Transactions**.</span></span>

10. <span data-ttu-id="a7045-167">在庫および倉庫管理で、**決算と調整**フォームを使用して、**3. 決算**手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="a7045-167">In Inventory and warehouse management, use the **Closing and adjustment** form to run the **3. Close** procedure.</span></span>
    
    <span data-ttu-id="a7045-168">このアクションでは、-35.00 (5 個 \* 7.00) と原価計算された元の販売明細行の原価が、-30.00 (5 個 \* 6.00) に調整されます。</span><span class="sxs-lookup"><span data-stu-id="a7045-168">This action adjusts the cost on the original sales line that was costed at -35.00 (5 pieces \* 7.00) to -30.00 (5 pieces \* 6.00).</span></span> <span data-ttu-id="a7045-169">これは、在庫モデル グループが先入れ先出し (FIFO) を使用し、1 個 6.00 は最初の発注書の FIFO 原価であるからです。</span><span class="sxs-lookup"><span data-stu-id="a7045-169">This is because the inventory model group uses First in, First out (FIFO), and 6.00 per piece is the FIFO cost from the first purchase order.</span></span> <span data-ttu-id="a7045-170">また、このアクションでは、元の販売注文明細行の 1 個あたりの原価に合わせて、返品販売明細行の原価が調整されます。</span><span class="sxs-lookup"><span data-stu-id="a7045-170">Additionally, the action adjusts the cost on the return sales line to match the cost per piece on the original sales line.</span></span> <span data-ttu-id="a7045-171">したがって、返品明細行の原価は 35.00 から 30.00 に調整されます。</span><span class="sxs-lookup"><span data-stu-id="a7045-171">Therefore, the cost of the return line is adjusted from 35.00 to 30.00.</span></span>




