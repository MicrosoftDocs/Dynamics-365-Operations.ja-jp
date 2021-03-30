---
title: 販売コミッション ルールの設定
description: この手順は、販売コミッションの計算および追跡を設定して有効にする方法を示します。
author: omulvad
manager: tfehr
ms.date: 06/21/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CommissionCustomerGroup, CommissionItemGroup, CommissionSalesGroup, CommissionSalesMember, DirPartyLookup, CommissionCalc, InventPosting, CustTable, EcoResProductDetailsExtended, CommissionEmplSalesGroup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ab352e1174dbee65f676c5b9bae45f2947dbcd6f
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/15/2021
ms.locfileid: "5232257"
---
# <a name="set-up-sales-commission-rules"></a><span data-ttu-id="ad786-103">販売コミッション ルールの設定</span><span class="sxs-lookup"><span data-stu-id="ad786-103">Set up sales commission rules</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="ad786-104">この手順は、販売コミッションの計算および追跡を設定して有効にする方法を示します。</span><span class="sxs-lookup"><span data-stu-id="ad786-104">This procedure shows you how to set up and enable sales commission calculation and tracking.</span></span> <span data-ttu-id="ad786-105">この手順は、顧客と品目両方のコミッション グループの作成方法、次に各グループに選択した顧客と製品をリンクする方法を示します。</span><span class="sxs-lookup"><span data-stu-id="ad786-105">The procedure shows how to create both customer and item commission groups, and then how to link a selected customer and product to the respective groups.</span></span> <span data-ttu-id="ad786-106">これらのグループは次にコミッション計算の設定で使用されます。これらは、販売担当者にコミッションを与えるために、販売注文と合致する、顧客、品目、販売担当者の組み合わせである必要があります。</span><span class="sxs-lookup"><span data-stu-id="ad786-106">Those groups are then used in the commission calculation setup to create a customer, item, and sales representatives combination that must be matched by the sales order to entitle the sales people to a commission.</span></span> <span data-ttu-id="ad786-107">顧客および品目のコミッション グループの作成は、コミッションの計算が個々の顧客および/または品目に対してもできるため、オプションとなっています。</span><span class="sxs-lookup"><span data-stu-id="ad786-107">Creating customer and item commission groups are optional, as the calculation of commission can also be done for an individual customer and/or item.</span></span> <span data-ttu-id="ad786-108">この手順は、デモ データの会社 USMF で、または独自のデータで実行できます。</span><span class="sxs-lookup"><span data-stu-id="ad786-108">You can run this procedure in demo data company USMF or on your own data.</span></span>


## <a name="set-up-commission-groups-and-commission-rates"></a><span data-ttu-id="ad786-109">コミッション グループとコミッション レートの設定</span><span class="sxs-lookup"><span data-stu-id="ad786-109">Set up commission groups and commission rates</span></span>
1. <span data-ttu-id="ad786-110">**ナビゲーション ウィンドウ > モジュール > 販売とマーケティング > コミッション > コミッションの顧客グループ** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="ad786-110">Go to **Navigation pane > Modules > Sales and marketing > Commissions > Customer groups for commission**.</span></span>
2. <span data-ttu-id="ad786-111">**新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="ad786-111">Select **New**.</span></span>
3. <span data-ttu-id="ad786-112">**グループ** フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="ad786-112">In the **Group** field, type a value.</span></span>
4. <span data-ttu-id="ad786-113">**名前** フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="ad786-113">In the **Name** field, type a value.</span></span>
5. <span data-ttu-id="ad786-114">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="ad786-114">Select **Save**.</span></span>
6. <span data-ttu-id="ad786-115">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="ad786-115">Close the page.</span></span>
7. <span data-ttu-id="ad786-116">**ナビゲーション ウィンドウ > モジュール > 販売とマーケティング > コミッション > 品目グループ** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="ad786-116">Go to **Navigation pane > Modules > Sales and marketing > Commissions > Item groups**.</span></span>
8. <span data-ttu-id="ad786-117">**新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="ad786-117">Select **New**.</span></span>
9. <span data-ttu-id="ad786-118">**グループ** フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="ad786-118">In the **Group** field, type a value.</span></span>
10. <span data-ttu-id="ad786-119">**名前** フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="ad786-119">In the **Name** field, type a value.</span></span>
11. <span data-ttu-id="ad786-120">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="ad786-120">Select **Save**.</span></span>
12. <span data-ttu-id="ad786-121">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="ad786-121">Close the page.</span></span>
13. <span data-ttu-id="ad786-122">**販売とマーケティング > コミッション > 販売グループ** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="ad786-122">Go to **Sales and marketing > Commissions > Sales groups**.</span></span>
    - <span data-ttu-id="ad786-123">コミッション売上グループは、該当するセールス グループに関連する顧客が、特定の商品を購入した場合にコミッションを受け取る資格がある、販売担当者ロールの従業員を指定します。</span><span class="sxs-lookup"><span data-stu-id="ad786-123">A Commission sales group specifies the employees in sales representative roles who are eligible to receive a commission when a customer associated with the relevant sales group buys certain items.</span></span>  
    - <span data-ttu-id="ad786-124">USMF のデモ データの会社では、「米国販売担当者」と呼ばれる売上グループがあります。</span><span class="sxs-lookup"><span data-stu-id="ad786-124">In the USMF demo data company, there is a sales group called "Sales reps US."</span></span>  
14. <span data-ttu-id="ad786-125">**アクション ウィンドウ** で、**一般** を選択します。</span><span class="sxs-lookup"><span data-stu-id="ad786-125">On the **Action Pane**, select **General**.</span></span>
15. <span data-ttu-id="ad786-126">**販売担当者** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="ad786-126">Click **Sales rep.**.</span></span> <span data-ttu-id="ad786-127">販売担当者 ページは、特定のコミッション グループに関連付けられる会社の販売担当者の一覧を表示します。</span><span class="sxs-lookup"><span data-stu-id="ad786-127">The Sales rep. page displays a list of the company's sales people who are associated with a specific commission group.</span></span> <span data-ttu-id="ad786-128">同じグループに複数の販売担当者を割り当て、パーセンテージ値として合計コミッション料金のそれぞれの比率を定義することができます。</span><span class="sxs-lookup"><span data-stu-id="ad786-128">You can assign multiple sales representatives to the same group and define their respective share of the total commission fee as a percentage value.</span></span> <span data-ttu-id="ad786-129">すべての従業員のコミッション分配の合計は 100 を超えることはできません。</span><span class="sxs-lookup"><span data-stu-id="ad786-129">The total commission share across all employees must not exceed 100.</span></span> 
16. <span data-ttu-id="ad786-130">一覧で、選択された行をマークします。</span><span class="sxs-lookup"><span data-stu-id="ad786-130">In the list, mark the selected row.</span></span>
17. <span data-ttu-id="ad786-131">**編集** を選択します。</span><span class="sxs-lookup"><span data-stu-id="ad786-131">Select **Edit**.</span></span>
18. <span data-ttu-id="ad786-132">**コミッション分配** を '50' に設定します。</span><span class="sxs-lookup"><span data-stu-id="ad786-132">Set **Commission share** to '50'.</span></span>
19. <span data-ttu-id="ad786-133">**新規** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="ad786-133">Click **New**.</span></span>
20. <span data-ttu-id="ad786-134">**名前** フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="ad786-134">In the **Name** field, click the drop-down button to open the lookup.</span></span>
21. <span data-ttu-id="ad786-135">**クイック フィルター** を使用して、レコードを見つけます。</span><span class="sxs-lookup"><span data-stu-id="ad786-135">Use the **Quick Filter** to find records.</span></span> <span data-ttu-id="ad786-136">たとえば、「Susan Burk」という値で [名前] フィールドをフィルターします。</span><span class="sxs-lookup"><span data-stu-id="ad786-136">For example, filter on the Name field with a value of 'Susan Burk'.</span></span>
22. <span data-ttu-id="ad786-137">**選択** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="ad786-137">Click **Select**.</span></span>
23. <span data-ttu-id="ad786-138">**コミッション分配** を '50' に設定します。</span><span class="sxs-lookup"><span data-stu-id="ad786-138">Set **Commission share** to '50'.</span></span>
24. <span data-ttu-id="ad786-139">**保存** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="ad786-139">Click **Save**.</span></span>
25. <span data-ttu-id="ad786-140">**販売とマーケティング > コミッション > コミッションの計算** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="ad786-140">Go to **Sales and marketing > Commissions > Commission calculation**.</span></span> <span data-ttu-id="ad786-141">**コミッションの計算** ページで、顧客および製品の事前設定された組み合わせが含まれる場合に、従業員が販売トランザクションに対して受け取るコミッション レートを定義します。</span><span class="sxs-lookup"><span data-stu-id="ad786-141">In the **Commission calculation** page, you define the commission rate that the employee is to receive for a sales transaction when it contains the pre-set combination of customer and product.</span></span> <span data-ttu-id="ad786-142">コミッション レートの設定の一部として、コミッションの計算基準、および割引を追加または除外するかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="ad786-142">As part of the commission rate setup, you must specify the commission calculation basis and whether it should include or exclude discounts.</span></span> <span data-ttu-id="ad786-143">コミッション レートがいつ有効なのかという、有効期間の入力もできます。</span><span class="sxs-lookup"><span data-stu-id="ad786-143">You can also enter a validity period for when the commission rate is active.</span></span>  
26. <span data-ttu-id="ad786-144">**新規** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="ad786-144">Click **New**.</span></span>
27. <span data-ttu-id="ad786-145">**品目コード** フィールドで「グループ」を選択します。</span><span class="sxs-lookup"><span data-stu-id="ad786-145">In the **Item code** field, select 'Group'.</span></span>
28. <span data-ttu-id="ad786-146">**品目関係** フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="ad786-146">In the **Item relation** field, click the drop-down button to open the lookup.</span></span>
29. <span data-ttu-id="ad786-147">一覧で、以前に作成したグループを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="ad786-147">In the list, find and select the group that you created earlier.</span></span>
30. <span data-ttu-id="ad786-148">**顧客コード** フィールドで、'グループ' を選択します。</span><span class="sxs-lookup"><span data-stu-id="ad786-148">In the **Customer code** field, select 'Group'.</span></span>
31. <span data-ttu-id="ad786-149">**顧客関係** フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="ad786-149">In the **Customer relation** field, click the drop-down button to open the lookup.</span></span>
32. <span data-ttu-id="ad786-150">一覧で、以前に設定したグループを選択します。</span><span class="sxs-lookup"><span data-stu-id="ad786-150">In the list, select the group that you set up earlier.</span></span>
33. <span data-ttu-id="ad786-151">**販売担当者関係** フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="ad786-151">In the **Sales rep. relation** field, click the drop-down button to open the lookup.</span></span>
34. <span data-ttu-id="ad786-152">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="ad786-152">In the list, find and select the desired record.</span></span>
    - <span data-ttu-id="ad786-153">「行割引前」オプションを有効にしたままにします。</span><span class="sxs-lookup"><span data-stu-id="ad786-153">Keep the "Before line discount" option.</span></span>  
    - <span data-ttu-id="ad786-154">コミッション値の計算の基礎になる、[収益] オプションを有効にしたままにします。</span><span class="sxs-lookup"><span data-stu-id="ad786-154">Keep the "Revenue" option as the basis for commission value calculation.</span></span>    
35. <span data-ttu-id="ad786-155">[コミッション料率] フィールドに、数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="ad786-155">In the Commission percentage field, enter a number.</span></span>
36. <span data-ttu-id="ad786-156">**保存** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="ad786-156">Click **Save**.</span></span>

## <a name="setting-up-commission-posting"></a><span data-ttu-id="ad786-157">コミッション転記の設定</span><span class="sxs-lookup"><span data-stu-id="ad786-157">Setting up commission posting</span></span>
1. <span data-ttu-id="ad786-158">**ナビゲーション ウィンドウ > 販売とマーケティング > コミッション > コミッションの転記** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="ad786-158">Go to **Navigation pane  > Sales and marketing > Commissions > Commission posting**.</span></span> <span data-ttu-id="ad786-159">コミッション料金は従業員に支払うものであるため、**総勘定元帳** の適切な勘定に、適切な財務上の転記ができるように設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="ad786-159">Commission fees are payable to the employees and must therefore be set up to ensure correct financial posting to the appropriate accounts in the **General ledger**.</span></span> <span data-ttu-id="ad786-160">これは、**コミッションの転記** ページで行われます。</span><span class="sxs-lookup"><span data-stu-id="ad786-160">This is done in the **Commission posting** page.</span></span> <span data-ttu-id="ad786-161">現在の会社で使用できる設定を確認します。</span><span class="sxs-lookup"><span data-stu-id="ad786-161">Review the setup that is available for the current company.</span></span> <span data-ttu-id="ad786-162">通常、専用の経費勘定に対してコミッション金額が転記され、専用の支払勘定で相殺されます。</span><span class="sxs-lookup"><span data-stu-id="ad786-162">Typically, the commission amounts are posted to a dedicated expense account and are offset to a dedicated payable account.</span></span> <span data-ttu-id="ad786-163">コミッション転記ルールの設定がない場合、システムは適用できるコミッションがある販売注文の請求を完了しません。</span><span class="sxs-lookup"><span data-stu-id="ad786-163">If you don't have the commission posting rules set up, the system will fail to complete invoicing of a sales order which has eligible commissions.</span></span>  
2. <span data-ttu-id="ad786-164">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="ad786-164">Close the page.</span></span>

## <a name="assign-a-commission-group-to-a-customer-and-a-product"></a><span data-ttu-id="ad786-165">顧客および製品のコミッション グループの割当</span><span class="sxs-lookup"><span data-stu-id="ad786-165">Assign a commission group to a customer and a product</span></span>
1. <span data-ttu-id="ad786-166">**ナビゲーション ウィンドウ > モジュール > 販売とマーケティング > 顧客 > すべての顧客** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="ad786-166">Go to **Navigation pane > Modules > Sales and marketing > Customers > All customers**.</span></span>
2. <span data-ttu-id="ad786-167">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="ad786-167">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="ad786-168">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="ad786-168">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="ad786-169">**編集** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="ad786-169">Click **Edit**.</span></span>
5. <span data-ttu-id="ad786-170">**販売注文の既定値** セクションを展開します。</span><span class="sxs-lookup"><span data-stu-id="ad786-170">Expand the **Sales order defaults** section.</span></span>
6. <span data-ttu-id="ad786-171">**コミッション グループ** フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="ad786-171">In the **Commission group** field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="ad786-172">一覧で、以前に作成したグループを選択します。</span><span class="sxs-lookup"><span data-stu-id="ad786-172">In the list, select the group that you created earlier.</span></span>
8. <span data-ttu-id="ad786-173">**売上グループ** フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="ad786-173">In the **Sales group** field, click the drop-down button to open the lookup.</span></span>
9. <span data-ttu-id="ad786-174">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="ad786-174">In the list, find and select the desired record.</span></span>
10. <span data-ttu-id="ad786-175">**保存** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="ad786-175">Click **Save**.</span></span>
11. <span data-ttu-id="ad786-176">**ナビゲーション ウィンドウ > モジュール > 製品情報管理 > 製品 > リリース済製品** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="ad786-176">Go to **Navigation pane > Modules > Product information management > Products > Released products**.</span></span>
12. <span data-ttu-id="ad786-177">**フィルター** を使用して、レコードを見つけます。</span><span class="sxs-lookup"><span data-stu-id="ad786-177">Use the **Filter** to find records.</span></span> <span data-ttu-id="ad786-178">たとえば、「T0020」という値で [品目番号] フィールドをフィルターします。</span><span class="sxs-lookup"><span data-stu-id="ad786-178">For example, filter on the Item number field with a value of 'T0020 '.</span></span>
13. <span data-ttu-id="ad786-179">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="ad786-179">In the list, click the link in the selected row.</span></span>
14. <span data-ttu-id="ad786-180">**編集** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="ad786-180">Click **Edit**.</span></span>
15. <span data-ttu-id="ad786-181">**販売** セクションを展開します。</span><span class="sxs-lookup"><span data-stu-id="ad786-181">Expand the **Sell** section.</span></span>
16. <span data-ttu-id="ad786-182">**コミッション グループ** フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="ad786-182">In the **Commission group** field, click the drop-down button to open the lookup.</span></span>
17. <span data-ttu-id="ad786-183">一覧で、以前に作成したコミッショングループを選択します。</span><span class="sxs-lookup"><span data-stu-id="ad786-183">In the list, select the commission group that you created earlier.</span></span>
18. <span data-ttu-id="ad786-184">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="ad786-184">Select **Save**.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]