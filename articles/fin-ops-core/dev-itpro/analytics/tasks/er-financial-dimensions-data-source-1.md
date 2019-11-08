---
title: ER 財務分析コードをデータ ソースとして使用する (第 1 部 - データ モデルのデザイン)
description: 次の手順では、システム管理者または電子レポート開発者が、電子レポート・データソースとしての財務分析コードを使用するために 電子レポート（ER）モデルをどのように環境設定しているのか説明します。
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERVendorPart, ERSolutionTable, ERSolutionCreateDropDialog, ERDataModelDesigner, ERDataModelContentsItemCreationDialog
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 92481749fa15d8a9c273edf6a79ee9fcfdc722e7
ms.sourcegitcommit: 75db3b75d35d27034f9b56e7119c9d0cb7666830
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/03/2019
ms.locfileid: "2550674"
---
# <a name="er-use-financial-dimensions-as-a-data-source-part-1---design-data-model"></a><span data-ttu-id="3d2a9-103">ER 財務分析コードをデータ ソースとして使用する (第 1 部 - データ モデルのデザイン)</span><span class="sxs-lookup"><span data-stu-id="3d2a9-103">ER Use financial dimensions as a data source (Part 1 - Design data model)</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="3d2a9-104">次の手順では、システム管理者または電子レポート開発者が、電子レポート・データソースとしての財務分析コードを使用するために 電子レポート（ER）モデルをどのように環境設定しているのか説明します。</span><span class="sxs-lookup"><span data-stu-id="3d2a9-104">The following steps explain how either a system administrator or electronic reporting developer can configure an Electronic reporting (ER) model to use financial dimensions as a data source for ER reports.</span></span> <span data-ttu-id="3d2a9-105">これらの手順はどのタイプの企業でも実施できます。</span><span class="sxs-lookup"><span data-stu-id="3d2a9-105">These steps can be performed in any company.</span></span>

<span data-ttu-id="3d2a9-106">これらの手順を完了するには、まず手順の「コンフィギュレーションプロバイダーを作成し、それを有効としてマークする」にある手順を完了する必要があります。</span><span class="sxs-lookup"><span data-stu-id="3d2a9-106">To complete these steps, you must first complete the steps in the procedure, “Create a configuration provider and mark it as active”.</span></span>


## <a name="create-a-new-data-model"></a><span data-ttu-id="3d2a9-107">新しいデータモデルを作成する</span><span class="sxs-lookup"><span data-stu-id="3d2a9-107">Create a new data model</span></span>
1. <span data-ttu-id="3d2a9-108">[組織管理] > [ワークスペース] > [電子申告] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="3d2a9-108">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
    * <span data-ttu-id="3d2a9-109">Litware, Inc. を確認します</span><span class="sxs-lookup"><span data-stu-id="3d2a9-109">Make sure that the “Litware, Inc.”</span></span> <span data-ttu-id="3d2a9-110">プロバイダーが使用可能であり、アクティブとしてマークされていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="3d2a9-110">provider is available and marked as active.</span></span>  
2. <span data-ttu-id="3d2a9-111">[コンフィギュレーションをレポートする] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="3d2a9-111">Click Reporting configurations.</span></span>
3. <span data-ttu-id="3d2a9-112">[コンフィギュレーションの作成] をクリックすると、ドロップ ダイアログが開きます。</span><span class="sxs-lookup"><span data-stu-id="3d2a9-112">Click Create configuration to open the drop dialog.</span></span>
4. <span data-ttu-id="3d2a9-113">[名称] フィールドに、「財務分析コード・サンプル モデル」と入力します。</span><span class="sxs-lookup"><span data-stu-id="3d2a9-113">In the Name field, type 'Financial dimensions sample model'.</span></span>
5. <span data-ttu-id="3d2a9-114">[コンフィギュレーションの作成] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="3d2a9-114">Click Create configuration.</span></span>
6. <span data-ttu-id="3d2a9-115">[デザイナー] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="3d2a9-115">Click Designer.</span></span>
7. <span data-ttu-id="3d2a9-116">[新規] をクリックすると、ドロップ ダイアログが開きます。</span><span class="sxs-lookup"><span data-stu-id="3d2a9-116">Click New to open the drop dialog.</span></span>
8. <span data-ttu-id="3d2a9-117">[名称] フィールドに、「エントリ」と入力します。</span><span class="sxs-lookup"><span data-stu-id="3d2a9-117">In the Name field, type 'Entry'.</span></span>
9. <span data-ttu-id="3d2a9-118">[追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="3d2a9-118">Click Add.</span></span>
10. <span data-ttu-id="3d2a9-119">[新規] をクリックすると、ドロップ ダイアログが開きます。</span><span class="sxs-lookup"><span data-stu-id="3d2a9-119">Click New to open the drop dialog.</span></span>
11. <span data-ttu-id="3d2a9-120">[名前] フィールドに、「Company」と入力します。</span><span class="sxs-lookup"><span data-stu-id="3d2a9-120">In the Name field, type 'Company'.</span></span>
12. <span data-ttu-id="3d2a9-121">[追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="3d2a9-121">Click Add.</span></span>
    * <span data-ttu-id="3d2a9-122">新規記録リストにモデルを追加します。</span><span class="sxs-lookup"><span data-stu-id="3d2a9-122">We will add to our model a new record list.</span></span> <span data-ttu-id="3d2a9-123">このリストは、選択した財務分析コードの設定を示します（このモデルをデータソースとして使用するERレポート向け）。</span><span class="sxs-lookup"><span data-stu-id="3d2a9-123">This list will expose (for any ER reports using this model as data source) the settings of selected financial dimensions.</span></span> <span data-ttu-id="3d2a9-124">各財務分析コードは、分析コード設定に基づくフィールドを有する記録としてこのリストに表示されます。</span><span class="sxs-lookup"><span data-stu-id="3d2a9-124">Each financial dimension will be presented in this list as a record with appropriate fields representing dimension’s setting.</span></span>  
13. <span data-ttu-id="3d2a9-125">[新規] をクリックすると、ドロップ ダイアログが開きます。</span><span class="sxs-lookup"><span data-stu-id="3d2a9-125">Click New to open the drop dialog.</span></span>
14. <span data-ttu-id="3d2a9-126">[名称] フィールドで、「分析コード設定」と入力します。</span><span class="sxs-lookup"><span data-stu-id="3d2a9-126">In the Name field, type 'Dimensions setting'.</span></span>
15. <span data-ttu-id="3d2a9-127">[品目タイプ] フィールドで、「レコード リスト」を選択します。</span><span class="sxs-lookup"><span data-stu-id="3d2a9-127">In the Item type field, select 'Record list'.</span></span>
16. <span data-ttu-id="3d2a9-128">[追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="3d2a9-128">Click Add.</span></span>
17. <span data-ttu-id="3d2a9-129">[新規] をクリックすると、ドロップ ダイアログが開きます。</span><span class="sxs-lookup"><span data-stu-id="3d2a9-129">Click New to open the drop dialog.</span></span>
18. <span data-ttu-id="3d2a9-130">[名称] フィールドに、「コード」と入力します。</span><span class="sxs-lookup"><span data-stu-id="3d2a9-130">In the Name field, type 'Code'.</span></span>
19. <span data-ttu-id="3d2a9-131">[品目タイプ] フィールドで、「String」を選択します。</span><span class="sxs-lookup"><span data-stu-id="3d2a9-131">In the Item type field, select 'String'.</span></span>
20. <span data-ttu-id="3d2a9-132">[追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="3d2a9-132">Click Add.</span></span>
21. <span data-ttu-id="3d2a9-133">[新規] をクリックすると、ドロップ ダイアログが開きます。</span><span class="sxs-lookup"><span data-stu-id="3d2a9-133">Click New to open the drop dialog.</span></span>
22. <span data-ttu-id="3d2a9-134">[名前] フィールドに、「名前」と入力します。</span><span class="sxs-lookup"><span data-stu-id="3d2a9-134">In the Name field, type 'Name'.</span></span>
23. <span data-ttu-id="3d2a9-135">[追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="3d2a9-135">Click Add.</span></span>
24. <span data-ttu-id="3d2a9-136">ツリーで、「エントリ」を選択します。</span><span class="sxs-lookup"><span data-stu-id="3d2a9-136">In the tree, select 'Entry'.</span></span>
25. <span data-ttu-id="3d2a9-137">[新規] をクリックすると、ドロップ ダイアログが開きます。</span><span class="sxs-lookup"><span data-stu-id="3d2a9-137">Click New to open the drop dialog.</span></span>
26. <span data-ttu-id="3d2a9-138">[名称] フィールドに、「仕訳」と入力します。</span><span class="sxs-lookup"><span data-stu-id="3d2a9-138">In the Name field, type 'Journal'.</span></span>
27. <span data-ttu-id="3d2a9-139">[品目タイプ] フィールドで、「レコード リスト」を選択します。</span><span class="sxs-lookup"><span data-stu-id="3d2a9-139">In the Item type field, select 'Record list'.</span></span>
28. <span data-ttu-id="3d2a9-140">[追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="3d2a9-140">Click Add.</span></span>
29. <span data-ttu-id="3d2a9-141">[新規] をクリックすると、ドロップ ダイアログが開きます。</span><span class="sxs-lookup"><span data-stu-id="3d2a9-141">Click New to open the drop dialog.</span></span>
30. <span data-ttu-id="3d2a9-142">[名称] フィールドに、「バッチ」と入力します。</span><span class="sxs-lookup"><span data-stu-id="3d2a9-142">In the Name field, type 'Batch'.</span></span>
31. <span data-ttu-id="3d2a9-143">[品目タイプ] フィールドで、「String」を選択します。</span><span class="sxs-lookup"><span data-stu-id="3d2a9-143">In the Item type field, select 'String'.</span></span>
32. <span data-ttu-id="3d2a9-144">[追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="3d2a9-144">Click Add.</span></span>
33. <span data-ttu-id="3d2a9-145">[新規] をクリックすると、ドロップ ダイアログが開きます。</span><span class="sxs-lookup"><span data-stu-id="3d2a9-145">Click New to open the drop dialog.</span></span>
34. <span data-ttu-id="3d2a9-146">[名称] フィールドで、「トランザクション」と入力します。</span><span class="sxs-lookup"><span data-stu-id="3d2a9-146">In the Name field, type 'Transaction'.</span></span>
35. <span data-ttu-id="3d2a9-147">[品目タイプ] フィールドで、「レコード リスト」を選択します。</span><span class="sxs-lookup"><span data-stu-id="3d2a9-147">In the Item type field, select 'Record list'.</span></span>
36. <span data-ttu-id="3d2a9-148">[追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="3d2a9-148">Click Add.</span></span>
37. <span data-ttu-id="3d2a9-149">[新規] をクリックすると、ドロップ ダイアログが開きます。</span><span class="sxs-lookup"><span data-stu-id="3d2a9-149">Click New to open the drop dialog.</span></span>
38. <span data-ttu-id="3d2a9-150">[名称] フィールドで、「日付」と入力します。</span><span class="sxs-lookup"><span data-stu-id="3d2a9-150">In the Name field, type 'Date'.</span></span>
39. <span data-ttu-id="3d2a9-151">[品目タイプ] フィールドで、「日付」を選択します。</span><span class="sxs-lookup"><span data-stu-id="3d2a9-151">In the Item type field, select 'Date'.</span></span>
40. <span data-ttu-id="3d2a9-152">[追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="3d2a9-152">Click Add.</span></span>
41. <span data-ttu-id="3d2a9-153">[新規] をクリックすると、ドロップ ダイアログが開きます。</span><span class="sxs-lookup"><span data-stu-id="3d2a9-153">Click New to open the drop dialog.</span></span>
42. <span data-ttu-id="3d2a9-154">[名称] フィールドで、「借方」と入力します。</span><span class="sxs-lookup"><span data-stu-id="3d2a9-154">In the Name field, type 'Debit'.</span></span>
43. <span data-ttu-id="3d2a9-155">[品目タイプ] フィールドで、「実数」を選択します。</span><span class="sxs-lookup"><span data-stu-id="3d2a9-155">In the Item type field, select 'Real'.</span></span>
44. <span data-ttu-id="3d2a9-156">[追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="3d2a9-156">Click Add.</span></span>
45. <span data-ttu-id="3d2a9-157">[新規] をクリックすると、ドロップ ダイアログが開きます。</span><span class="sxs-lookup"><span data-stu-id="3d2a9-157">Click New to open the drop dialog.</span></span>
46. <span data-ttu-id="3d2a9-158">[名称] フィールドで、「貸方」と入力します。</span><span class="sxs-lookup"><span data-stu-id="3d2a9-158">In the Name field, type 'Credit'.</span></span>
47. <span data-ttu-id="3d2a9-159">[追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="3d2a9-159">Click Add.</span></span>
48. <span data-ttu-id="3d2a9-160">[新規] をクリックすると、ドロップ ダイアログが開きます。</span><span class="sxs-lookup"><span data-stu-id="3d2a9-160">Click New to open the drop dialog.</span></span>
49. <span data-ttu-id="3d2a9-161">[名前] フィールドで、「通貨」と入力します。</span><span class="sxs-lookup"><span data-stu-id="3d2a9-161">In the Name field, type 'Currency'.</span></span>
50. <span data-ttu-id="3d2a9-162">[品目タイプ] フィールドで、「String」を選択します。</span><span class="sxs-lookup"><span data-stu-id="3d2a9-162">In the Item type field, select 'String'.</span></span>
51. <span data-ttu-id="3d2a9-163">[追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="3d2a9-163">Click Add.</span></span>
52. <span data-ttu-id="3d2a9-164">[新規] をクリックすると、ドロップ ダイアログが開きます。</span><span class="sxs-lookup"><span data-stu-id="3d2a9-164">Click New to open the drop dialog.</span></span>
53. <span data-ttu-id="3d2a9-165">[名称] フィールドで、「伝票」と入力します。</span><span class="sxs-lookup"><span data-stu-id="3d2a9-165">In the Name field, type 'Voucher'.</span></span>
54. <span data-ttu-id="3d2a9-166">[追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="3d2a9-166">Click Add.</span></span>
55. <span data-ttu-id="3d2a9-167">[新規] をクリックすると、ドロップ ダイアログが開きます。</span><span class="sxs-lookup"><span data-stu-id="3d2a9-167">Click New to open the drop dialog.</span></span>
56. <span data-ttu-id="3d2a9-168">[名称] フィールドで、「分析コードデータ」と入力します。</span><span class="sxs-lookup"><span data-stu-id="3d2a9-168">In the Name field, type 'Dimensions data'.</span></span>
57. <span data-ttu-id="3d2a9-169">[品目タイプ] フィールドで、「レコード リスト」を選択します。</span><span class="sxs-lookup"><span data-stu-id="3d2a9-169">In the Item type field, select 'Record list'.</span></span>
58. <span data-ttu-id="3d2a9-170">[追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="3d2a9-170">Click Add.</span></span>
    * <span data-ttu-id="3d2a9-171">新規記録リストにモデルを追加しました。</span><span class="sxs-lookup"><span data-stu-id="3d2a9-171">We added to our model a new record list.</span></span> <span data-ttu-id="3d2a9-172">このリストは、選択した財務分析コードの値を示します（このモデルをデータソースとして使用するERレポート向け）。</span><span class="sxs-lookup"><span data-stu-id="3d2a9-172">This list will expose (for any ER reports using this model as data source) the values of selected financial dimensions.</span></span> <span data-ttu-id="3d2a9-173">各財務分析コードは、分析コードの値に基づくフィールドを有する記録としてこのリストに表示されます。</span><span class="sxs-lookup"><span data-stu-id="3d2a9-173">Each financial dimension will be presented in this list as a record with appropriate fields representing dimension’s values.</span></span> <span data-ttu-id="3d2a9-174">分析コードの名称は、目的選択用のフィールドとしてこの記録にも表示されます。</span><span class="sxs-lookup"><span data-stu-id="3d2a9-174">Dimension name will be also presented in this record as a field to be used, if needed, for selection purposes.</span></span>  
59. <span data-ttu-id="3d2a9-175">[新規] をクリックすると、ドロップ ダイアログが開きます。</span><span class="sxs-lookup"><span data-stu-id="3d2a9-175">Click New to open the drop dialog.</span></span>
60. <span data-ttu-id="3d2a9-176">[名称] フィールドに、「コード」と入力します。</span><span class="sxs-lookup"><span data-stu-id="3d2a9-176">In the Name field, type 'Code'.</span></span>
61. <span data-ttu-id="3d2a9-177">[品目タイプ] フィールドで、「String」を選択します。</span><span class="sxs-lookup"><span data-stu-id="3d2a9-177">In the Item type field, select 'String'.</span></span>
62. <span data-ttu-id="3d2a9-178">[追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="3d2a9-178">Click Add.</span></span>
63. <span data-ttu-id="3d2a9-179">[新規] をクリックすると、ドロップ ダイアログが開きます。</span><span class="sxs-lookup"><span data-stu-id="3d2a9-179">Click New to open the drop dialog.</span></span>
64. <span data-ttu-id="3d2a9-180">[名前] フィールドに、「説明」と入力します。</span><span class="sxs-lookup"><span data-stu-id="3d2a9-180">In the Name field, type 'Description'.</span></span>
65. <span data-ttu-id="3d2a9-181">[追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="3d2a9-181">Click Add.</span></span>
66. <span data-ttu-id="3d2a9-182">[新規] をクリックすると、ドロップ ダイアログが開きます。</span><span class="sxs-lookup"><span data-stu-id="3d2a9-182">Click New to open the drop dialog.</span></span>
67. <span data-ttu-id="3d2a9-183">[名前] フィールドに、「名前」と入力します。</span><span class="sxs-lookup"><span data-stu-id="3d2a9-183">In the Name field, type 'Name'.</span></span>
68. <span data-ttu-id="3d2a9-184">[追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="3d2a9-184">Click Add.</span></span>
69. <span data-ttu-id="3d2a9-185">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="3d2a9-185">Click Save.</span></span>
70. <span data-ttu-id="3d2a9-186">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="3d2a9-186">Close the page.</span></span>

