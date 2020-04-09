---
title: 固定資産転記プロファイルの設定
description: このタスク ガイドでは、固定資産転記プロファイルを設定します。
author: saraschi2
manager: AnnBe
ms.date: 07/22/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetPosting
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 07961d8613b6b5e0e1c5dc6a91b554305dcb17f5
ms.sourcegitcommit: c69926b4285cb2ec2d9ce1ad72d1cb852024dd5e
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/18/2020
ms.locfileid: "3138164"
---
# <a name="set-up-fixed-asset-posting-profiles"></a><span data-ttu-id="7fdba-103">固定資産転記プロファイルの設定</span><span class="sxs-lookup"><span data-stu-id="7fdba-103">Set up fixed asset posting profiles</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="7fdba-104">このタスク ガイドでは、固定資産転記プロファイルを設定します。</span><span class="sxs-lookup"><span data-stu-id="7fdba-104">This task guide will set up Fixed asset posting profiles.</span></span>  <span data-ttu-id="7fdba-105">これは USMF の法人に対して経理担当ロールとデモ データを使用します。</span><span class="sxs-lookup"><span data-stu-id="7fdba-105">It uses the Accountant role and demo data for the USMF legal entity.</span></span>  <span data-ttu-id="7fdba-106">タスク ガイドにある例は、基本転記プロファイル用であるのに対して、転記プロファイルは、特定の勘定科目表と財務報告の要件に基づいて作成される必要があります。</span><span class="sxs-lookup"><span data-stu-id="7fdba-106">Examples given in the task guide are for a basic posting profile, though posting profiles must be created for your specific chart of accounts and financial reporting requirements.</span></span>

1. <span data-ttu-id="7fdba-107">ナビゲーション ウィンドウで、**モジュール > 固定資産 > 設定 > 固定資産転記プロファイル**に移動します。</span><span class="sxs-lookup"><span data-stu-id="7fdba-107">In the Navigation pane, go to **Modules > Fixed assets > Setup > Fixed asset posting profiles**.</span></span>
2. <span data-ttu-id="7fdba-108">**新規** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="7fdba-108">Click **New**.</span></span>
3. <span data-ttu-id="7fdba-109">**転記プロファイル** フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="7fdba-109">In the **Posting profile** field, type a value.</span></span>
4. <span data-ttu-id="7fdba-110">**説明**フィールドで、値を入力します。</span><span class="sxs-lookup"><span data-stu-id="7fdba-110">In the **Description** field, type a value.</span></span> <span data-ttu-id="7fdba-111">固定資産を使用する場合、使用する各固定資産トランザクション タイプの転記プロファイルを作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="7fdba-111">You will need to create a posting profile for each fixed asset transaction type you will be using when working with fixed assets.</span></span> <span data-ttu-id="7fdba-112">このタスク ガイドは取得トランザクション タイプから開始します。</span><span class="sxs-lookup"><span data-stu-id="7fdba-112">This task guide will start with the Acquisition transaction type.</span></span>  
5. <span data-ttu-id="7fdba-113">ツール バーの**追加**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="7fdba-113">In the toolbar, click **Add**.</span></span>
6. <span data-ttu-id="7fdba-114">**帳簿**フィールドで値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="7fdba-114">In the **Book** field, enter or select a value.</span></span> <span data-ttu-id="7fdba-115">**グループ化**フィールドを使用すると、テーブル (各固定資産について 1 つの勘定を設定) またはグループ (各固定資産グループについて 1 つの勘定を設定) で転記プロファイルを定義することができます。</span><span class="sxs-lookup"><span data-stu-id="7fdba-115">The **Groupings** field allows you to define the posting profile down to the Table (one account set up for each fixed asset) or Group (one account set up for each fixed asset group).</span></span> <span data-ttu-id="7fdba-116">このタスク ガイドでは、指定した帳簿を使用してすべての固定資産に適用するために、この値を "すべて" に設定します。</span><span class="sxs-lookup"><span data-stu-id="7fdba-116">For this task guide, leave the value set to "All" to apply to all fixed assets with the specified Book.</span></span>  
7. <span data-ttu-id="7fdba-117">**主勘定**フィールドに、目的の値を指定します。</span><span class="sxs-lookup"><span data-stu-id="7fdba-117">In the **Main account** field, specify the desired values.</span></span> <span data-ttu-id="7fdba-118">取得の場合は、相手勘定を入力するか、または特定の取引の値を入力するために、空白のままにできます。</span><span class="sxs-lookup"><span data-stu-id="7fdba-118">For acquisitions, you can enter an offset account or leave it blank to be filled in for the specific transaction.</span></span>    
8. <span data-ttu-id="7fdba-119">**勘定科目**クイック タブの下のドロップダウン メニューで、「取得原価調整」を選択します。</span><span class="sxs-lookup"><span data-stu-id="7fdba-119">In the drop-down menu under the **Ledger accounts** fastTab, select 'Acquisition adjustment'.</span></span> <span data-ttu-id="7fdba-120">取得原価調整トランザクションにおいては、取得トランザクションに使用されているものと同じ勘定を使用します。</span><span class="sxs-lookup"><span data-stu-id="7fdba-120">For acquisition adjustment transactions, we will use the same accounts as used for Acquisition transactions.</span></span>  
9. <span data-ttu-id="7fdba-121">**追加**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="7fdba-121">Click **Add**.</span></span>
10. <span data-ttu-id="7fdba-122">**帳簿**フィールドで値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="7fdba-122">In the **Book** field, enter or select a value.</span></span>
11. <span data-ttu-id="7fdba-123">**主勘定**フィールドに、目的の値を指定します。</span><span class="sxs-lookup"><span data-stu-id="7fdba-123">In the **Main account** field, specify the desired values.</span></span> <span data-ttu-id="7fdba-124">取得原価調整の場合は、相手勘定を入力するか、または特定のトランザクションの値を入力するために、空白のままにできます。</span><span class="sxs-lookup"><span data-stu-id="7fdba-124">For acquisition adjustments, you can enter an offset account or leave it blank to be filled in for the specific transaction.</span></span>    
12. <span data-ttu-id="7fdba-125">**勘定科目**クイック タブの下のドロップダウン メニューで、「減価償却」を選択します。</span><span class="sxs-lookup"><span data-stu-id="7fdba-125">In the drop-down menu under the **Ledger accounts** fastTab, select 'Depreciation'.</span></span>
13. <span data-ttu-id="7fdba-126">**追加**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="7fdba-126">Click **Add**.</span></span>
14. <span data-ttu-id="7fdba-127">**帳簿**フィールドで値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="7fdba-127">In the **Book** field, enter or select a value.</span></span>
15. <span data-ttu-id="7fdba-128">**主勘定**フィールドに、目的の値を指定します。</span><span class="sxs-lookup"><span data-stu-id="7fdba-128">In the **Main account** field, specify the desired values.</span></span>
16. <span data-ttu-id="7fdba-129">**相殺勘定**フィールドで、任意の値を指定します。</span><span class="sxs-lookup"><span data-stu-id="7fdba-129">In the **Offset account** field, specify the desired values.</span></span>
17. <span data-ttu-id="7fdba-130">**勘定科目**クイック タブの下のドロップダウン メニューで、「減価償却調整」を選択します。</span><span class="sxs-lookup"><span data-stu-id="7fdba-130">In the drop-down menu under the **Ledger accounts** fastTab, select 'Depreciation adjustment'.</span></span> <span data-ttu-id="7fdba-131">減価償却調整トランザクションにおいては、減価償却トランザクションに使用されているものと同じ勘定を使用します。</span><span class="sxs-lookup"><span data-stu-id="7fdba-131">For depreciation adjustment transactions, we will use the same accounts as used for Depreciation transactions.</span></span>  
18. <span data-ttu-id="7fdba-132">**追加**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="7fdba-132">Click **Add**.</span></span>
19. <span data-ttu-id="7fdba-133">**帳簿**フィールドで値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="7fdba-133">In the **Book** field, enter or select a value.</span></span>
20. <span data-ttu-id="7fdba-134">**主勘定**フィールドに、目的の値を指定します。</span><span class="sxs-lookup"><span data-stu-id="7fdba-134">In the **Main account** field, specify the desired values.</span></span>
21. <span data-ttu-id="7fdba-135">**相殺勘定**フィールドで、任意の値を指定します。</span><span class="sxs-lookup"><span data-stu-id="7fdba-135">In the **Offset account** field, specify the desired values.</span></span>
22. <span data-ttu-id="7fdba-136">**勘定科目**クイック タブの下のドロップダウン メニューで、「処分 - 売却」を選択します。</span><span class="sxs-lookup"><span data-stu-id="7fdba-136">In the drop-down menu under the **Ledger accounts** fastTab, select 'Disposal - sale'.</span></span>
23. <span data-ttu-id="7fdba-137">**追加**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="7fdba-137">Click **Add**.</span></span>
24. <span data-ttu-id="7fdba-138">**帳簿**フィールドで値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="7fdba-138">In the **Book** field, enter or select a value.</span></span>
25. <span data-ttu-id="7fdba-139">**主勘定**フィールドに、目的の値を指定します。</span><span class="sxs-lookup"><span data-stu-id="7fdba-139">In the **Main account** field, specify the desired values.</span></span> <span data-ttu-id="7fdba-140">処理の場合は、相手勘定を入力するか、または特定のトランザクションの値を入力するために、空白のままにできます。</span><span class="sxs-lookup"><span data-stu-id="7fdba-140">For disposals, you can enter an offset account or leave it blank to be filled in for the specific transaction.</span></span>  
26. <span data-ttu-id="7fdba-141">**勘定科目**クイック タブの下のドロップダウン メニューで、「処分 - 仕損」を選択します。</span><span class="sxs-lookup"><span data-stu-id="7fdba-141">In the drop-down menu under the **Ledger accounts** fastTab, select 'Disposal - scrap'.</span></span> <span data-ttu-id="7fdba-142">「処分売却」および「処分仕損」に対して同じ勘定を使用します。</span><span class="sxs-lookup"><span data-stu-id="7fdba-142">Use the same accounts for 'Disposal sale' and 'Disposal scrap'.</span></span>  
27. <span data-ttu-id="7fdba-143">**追加**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="7fdba-143">Click **Add**.</span></span>
28. <span data-ttu-id="7fdba-144">**帳簿**フィールドで値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="7fdba-144">In the **Book** field, enter or select a value.</span></span>
29. <span data-ttu-id="7fdba-145">**主勘定**フィールドに、目的の値を指定します。</span><span class="sxs-lookup"><span data-stu-id="7fdba-145">In the **Main account** field, specify the desired values.</span></span> <span data-ttu-id="7fdba-146">処理の場合は、相手勘定を入力するか、または特定のトランザクションの値を入力するために、空白のままにできます。</span><span class="sxs-lookup"><span data-stu-id="7fdba-146">For disposals, you can enter an offset account or leave it blank to be filled in for the specific transaction.</span></span>  
30. <span data-ttu-id="7fdba-147">**処分**クイック タブを展開します。</span><span class="sxs-lookup"><span data-stu-id="7fdba-147">Expand the **Disposal** fastTab.</span></span> <span data-ttu-id="7fdba-148">売却と仕損両方の処分転記プロファイルを設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="7fdba-148">You must set up disposal posting profiles for both sale and scrap.</span></span>  <span data-ttu-id="7fdba-149">販売トランザクションの処分から開始します。</span><span class="sxs-lookup"><span data-stu-id="7fdba-149">We will start with disposal sale transactions.</span></span>  
31. <span data-ttu-id="7fdba-150">**追加**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="7fdba-150">Click **Add**.</span></span>
32. <span data-ttu-id="7fdba-151">**帳簿**フィールドで値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="7fdba-151">In the **Book** field, enter or select a value.</span></span>
33. <span data-ttu-id="7fdba-152">**転記金額**フィールドで「取得金額」を選択します。</span><span class="sxs-lookup"><span data-stu-id="7fdba-152">In the **Post value** field, select 'Acquisition value'.</span></span>
    * <span data-ttu-id="7fdba-153">取得金額は、すべての年の取得および取得原価調整の値を処理します。</span><span class="sxs-lookup"><span data-stu-id="7fdba-153">Acquisition value will address Acquisition and Acquisition adjustment values for all years.</span></span> <span data-ttu-id="7fdba-154">これらのトランザクション タイプの勘定を別途定義もできます。</span><span class="sxs-lookup"><span data-stu-id="7fdba-154">You can also define accounts for these transaction types separately.</span></span>  
    * <span data-ttu-id="7fdba-155">処分により発生する結果が差益または差損であるかによって異なる勘定を使用する処分プロセスを設定できます。</span><span class="sxs-lookup"><span data-stu-id="7fdba-155">You can set the disposal process to use different accounts depending upon if the disposal results in a gain or loss.</span></span> <span data-ttu-id="7fdba-156">処分のすべてのタイプに同じ勘定を使用するために、販売額のタイプを "すべて" に設定します。</span><span class="sxs-lookup"><span data-stu-id="7fdba-156">I will set the Sales value type to "All" to use the same accounts for all types of disposals.</span></span>  
34. <span data-ttu-id="7fdba-157">**主勘定**フィールドに、目的の値を指定します。</span><span class="sxs-lookup"><span data-stu-id="7fdba-157">In the **Main account** field, specify the desired values.</span></span>
35. <span data-ttu-id="7fdba-158">**相殺勘定**フィールドで、任意の値を指定します。</span><span class="sxs-lookup"><span data-stu-id="7fdba-158">In the **Offset account** field, specify the desired values.</span></span>
36. <span data-ttu-id="7fdba-159">**追加**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="7fdba-159">Click **Add**.</span></span>
37. <span data-ttu-id="7fdba-160">**帳簿**フィールドで値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="7fdba-160">In the **Book** field, enter or select a value.</span></span>
38. <span data-ttu-id="7fdba-161">**転記金額**フィールドで、「減価償却 (前年度まで)」を選択します。</span><span class="sxs-lookup"><span data-stu-id="7fdba-161">In the **Post value** field, select 'Depreciation (prior years)'.</span></span>  
38. <span data-ttu-id="7fdba-162">**主勘定**フィールドに、目的の値を指定します。</span><span class="sxs-lookup"><span data-stu-id="7fdba-162">In the **Main account** field, specify the desired values.</span></span>
39. <span data-ttu-id="7fdba-163">**相殺勘定**フィールドで、任意の値を指定します。</span><span class="sxs-lookup"><span data-stu-id="7fdba-163">In the **Offset account** field, specify the desired values.</span></span>
40. <span data-ttu-id="7fdba-164">**追加**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="7fdba-164">Click **Add**.</span></span>
41. <span data-ttu-id="7fdba-165">**帳簿**フィールドで値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="7fdba-165">In the **Book** field, enter or select a value.</span></span>
42. <span data-ttu-id="7fdba-166">**転記金額**フィールドで、「減価償却 (今年度)」を選択します。</span><span class="sxs-lookup"><span data-stu-id="7fdba-166">In the **Post value** field, select 'Depreciation (this year)'.</span></span>
43. <span data-ttu-id="7fdba-167">**主勘定**フィールドに、目的の値を指定します。</span><span class="sxs-lookup"><span data-stu-id="7fdba-167">In the **Main account** field, specify the desired values.</span></span>
44. <span data-ttu-id="7fdba-168">**相殺勘定**フィールドで、任意の値を指定します。</span><span class="sxs-lookup"><span data-stu-id="7fdba-168">In the **Offset account** field, specify the desired values.</span></span>
45. <span data-ttu-id="7fdba-169">**追加**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="7fdba-169">Click **Add**.</span></span>
46. <span data-ttu-id="7fdba-170">**帳簿**フィールドで値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="7fdba-170">In the **Book** field, enter or select a value.</span></span>
47. <span data-ttu-id="7fdba-171">**転記金額**フィールドで、「減価償却調整 (前年度まで)」を選択します。</span><span class="sxs-lookup"><span data-stu-id="7fdba-171">In the **Post value** field, select 'Depreciation adjustments (prior years)'.</span></span>
48. <span data-ttu-id="7fdba-172">**主勘定**フィールドに、目的の値を指定します。</span><span class="sxs-lookup"><span data-stu-id="7fdba-172">In the **Main account** field, specify the desired values.</span></span>
49. <span data-ttu-id="7fdba-173">**相殺勘定**フィールドで、任意の値を指定します。</span><span class="sxs-lookup"><span data-stu-id="7fdba-173">In the **Offset account** field, specify the desired values.</span></span>
50. <span data-ttu-id="7fdba-174">**追加**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="7fdba-174">Click **Add**.</span></span>
51. <span data-ttu-id="7fdba-175">**帳簿**フィールドで値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="7fdba-175">In the **Book** field, enter or select a value.</span></span>
52. <span data-ttu-id="7fdba-176">**転記金額**フィールドで、「減価償却調整 (今年度)」を選択します。</span><span class="sxs-lookup"><span data-stu-id="7fdba-176">In the **Post value** field, select 'Depreciation adjustments (this year)'.</span></span>
53. <span data-ttu-id="7fdba-177">**主勘定**フィールドに、目的の値を指定します。</span><span class="sxs-lookup"><span data-stu-id="7fdba-177">In the **Main account** field, specify the desired values.</span></span>
54. <span data-ttu-id="7fdba-178">**相殺勘定**フィールドで、任意の値を指定します。</span><span class="sxs-lookup"><span data-stu-id="7fdba-178">In the **Offset account** field, specify the desired values.</span></span>
55. <span data-ttu-id="7fdba-179">**追加**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="7fdba-179">Click **Add**.</span></span>
56. <span data-ttu-id="7fdba-180">**帳簿**フィールドで値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="7fdba-180">In the **Book** field, enter or select a value.</span></span>
57. <span data-ttu-id="7fdba-181">**転記金額**フィールドで「正味帳簿価格」を選択します。</span><span class="sxs-lookup"><span data-stu-id="7fdba-181">In the **Post value** field, select 'Net book value'.</span></span>
58. <span data-ttu-id="7fdba-182">**主勘定**フィールドに、目的の値を指定します。</span><span class="sxs-lookup"><span data-stu-id="7fdba-182">In the **Main account** field, specify the desired values.</span></span>
59. <span data-ttu-id="7fdba-183">**相殺勘定**フィールドで、任意の値を指定します。</span><span class="sxs-lookup"><span data-stu-id="7fdba-183">In the **Offset account** field, specify the desired values.</span></span>
60. <span data-ttu-id="7fdba-184">**売却または仕損**フィールドで「仕損」を選択します。</span><span class="sxs-lookup"><span data-stu-id="7fdba-184">In the **Sale or scrap** field, select 'Scrap'.</span></span>
61. <span data-ttu-id="7fdba-185">**追加**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="7fdba-185">Click **Add**.</span></span>
62. <span data-ttu-id="7fdba-186">**帳簿**フィールドで値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="7fdba-186">In the **Book** field, enter or select a value.</span></span>
63. <span data-ttu-id="7fdba-187">**転記金額**フィールドで「取得金額」を選択します。</span><span class="sxs-lookup"><span data-stu-id="7fdba-187">In the **Post value** field, select 'Acquisition value'.</span></span>
64. <span data-ttu-id="7fdba-188">**主勘定**フィールドに、目的の値を指定します。</span><span class="sxs-lookup"><span data-stu-id="7fdba-188">In the **Main account** field, specify the desired values.</span></span>
65. <span data-ttu-id="7fdba-189">**相殺勘定**フィールドで、任意の値を指定します。</span><span class="sxs-lookup"><span data-stu-id="7fdba-189">In the **Offset account** field, specify the desired values.</span></span>
66. <span data-ttu-id="7fdba-190">**追加**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="7fdba-190">Click **Add**.</span></span>
67. <span data-ttu-id="7fdba-191">**帳簿**フィールドで値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="7fdba-191">In the **Book** field, enter or select a value.</span></span>
67. <span data-ttu-id="7fdba-192">**転記金額**フィールドで、「減価償却 (前年度まで)」を選択します。</span><span class="sxs-lookup"><span data-stu-id="7fdba-192">In **Post value** field, select 'Depreciation (prior years)'.</span></span>  
68. <span data-ttu-id="7fdba-193">**主勘定**フィールドに、目的の値を指定します。</span><span class="sxs-lookup"><span data-stu-id="7fdba-193">In the **Main account** field, specify the desired values.</span></span>
69. <span data-ttu-id="7fdba-194">**相殺勘定**フィールドで、任意の値を指定します。</span><span class="sxs-lookup"><span data-stu-id="7fdba-194">In the **Offset account** field, specify the desired values.</span></span>
70. <span data-ttu-id="7fdba-195">**追加**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="7fdba-195">Click **Add**.</span></span>
71. <span data-ttu-id="7fdba-196">**帳簿**フィールドで値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="7fdba-196">In the **Book** field, enter or select a value.</span></span>
72. <span data-ttu-id="7fdba-197">**転記金額**フィールドで、「減価償却 (今年度)」を選択します。</span><span class="sxs-lookup"><span data-stu-id="7fdba-197">In the **Post value** field, select 'Depreciation (this year)'.</span></span>
73. <span data-ttu-id="7fdba-198">**主勘定**フィールドに、目的の値を指定します。</span><span class="sxs-lookup"><span data-stu-id="7fdba-198">In the **Main account** field, specify the desired values.</span></span>
74. <span data-ttu-id="7fdba-199">**相殺勘定**フィールドで、任意の値を指定します。</span><span class="sxs-lookup"><span data-stu-id="7fdba-199">In the **Offset account** field, specify the desired values.</span></span>
75. <span data-ttu-id="7fdba-200">**追加**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="7fdba-200">Click **Add**.</span></span>
76. <span data-ttu-id="7fdba-201">**帳簿**フィールドで値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="7fdba-201">In the **Book** field, enter or select a value.</span></span>
77. <span data-ttu-id="7fdba-202">**転記金額**フィールドで、「減価償却調整 (前年度まで)」を選択します。</span><span class="sxs-lookup"><span data-stu-id="7fdba-202">In the **Post value** field, select 'Depreciation adjustments (prior years)'.</span></span>
78. <span data-ttu-id="7fdba-203">**主勘定**フィールドに、目的の値を指定します。</span><span class="sxs-lookup"><span data-stu-id="7fdba-203">In the **Main account** field, specify the desired values.</span></span>
79. <span data-ttu-id="7fdba-204">**相殺勘定**フィールドで、任意の値を指定します。</span><span class="sxs-lookup"><span data-stu-id="7fdba-204">In the **Offset account** field, specify the desired values.</span></span>
80. <span data-ttu-id="7fdba-205">**追加**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="7fdba-205">Click **Add**.</span></span>
81. <span data-ttu-id="7fdba-206">**帳簿**フィールドで値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="7fdba-206">In the **Book** field, enter or select a value.</span></span>
82. <span data-ttu-id="7fdba-207">**転記金額**フィールドで、「減価償却調整 (今年度)」を選択します。</span><span class="sxs-lookup"><span data-stu-id="7fdba-207">In the **Post value** field, select 'Depreciation adjustments (this year)'.</span></span>
83. <span data-ttu-id="7fdba-208">**主勘定**フィールドに、目的の値を指定します。</span><span class="sxs-lookup"><span data-stu-id="7fdba-208">In the **Main account** field, specify the desired values.</span></span>
84. <span data-ttu-id="7fdba-209">**相殺勘定**フィールドで、任意の値を指定します。</span><span class="sxs-lookup"><span data-stu-id="7fdba-209">In the **Offset account** field, specify the desired values.</span></span>
85. <span data-ttu-id="7fdba-210">**追加**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="7fdba-210">Click **Add**.</span></span>
86. <span data-ttu-id="7fdba-211">**帳簿**フィールドで値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="7fdba-211">In the **Book** field, enter or select a value.</span></span>
87. <span data-ttu-id="7fdba-212">**転記金額**フィールドで「正味帳簿価格」を選択します。</span><span class="sxs-lookup"><span data-stu-id="7fdba-212">In the **Post value** field, select 'Net book value'.</span></span>
88. <span data-ttu-id="7fdba-213">**主勘定**フィールドに、目的の値を指定します。</span><span class="sxs-lookup"><span data-stu-id="7fdba-213">In the **Main account** field, specify the desired values.</span></span>
89. <span data-ttu-id="7fdba-214">**相殺勘定**フィールドで、任意の値を指定します。</span><span class="sxs-lookup"><span data-stu-id="7fdba-214">In the **Offset account** field, specify the desired values.</span></span>

