---
title: ER 財務分析コードをデータ ソースとして使用する (第 1 部 - データ モデルのデザイン)
description: このトピックでは、財務分析コードを ER レポートのデータ ソースとして使用するために、電子申告 (ER) モデルを構成する方法について説明します。 (第 1 部)
author: NickSelin
manager: AnnBe
ms.date: 05/27/2020
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERVendorPart, ERSolutionTable, ERSolutionCreateDropDialog, ERDataModelDesigner, ERDataModelContentsItemCreationDialog
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 92d29d954debddd509eaba6b710f39b218da2c77
ms.sourcegitcommit: 5192cfaedfd861faea63d8954d7bcc500608a225
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/30/2021
ms.locfileid: "5092178"
---
# <a name="er-use-financial-dimensions-as-a-data-source-part-1---design-data-model"></a><span data-ttu-id="88509-104">ER 財務分析コードをデータ ソースとして使用する (第 1 部 - データ モデルのデザイン)</span><span class="sxs-lookup"><span data-stu-id="88509-104">ER Use financial dimensions as a data source (Part 1 - Design data model)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="88509-105">次の手順では、システム管理者または電子レポート開発者が、電子レポート・データソースとしての財務分析コードを使用するために 電子レポート（ER）モデルをどのように環境設定しているのか説明します。</span><span class="sxs-lookup"><span data-stu-id="88509-105">The following steps explain how either a system administrator or electronic reporting developer can configure an Electronic reporting (ER) model to use financial dimensions as a data source for ER reports.</span></span> <span data-ttu-id="88509-106">これらの手順はどのタイプの企業でも実施できます。</span><span class="sxs-lookup"><span data-stu-id="88509-106">These steps can be performed in any company.</span></span>

<span data-ttu-id="88509-107">これらの手順を完了するには、まず 「構成プロバイダーを作成し、有効としてマークする」 に記載の手順を完了する必要があります。</span><span class="sxs-lookup"><span data-stu-id="88509-107">To complete these steps, you must first complete the steps in the procedure, "Create a configuration provider and mark it as active".</span></span>


## <a name="create-a-new-data-model"></a><span data-ttu-id="88509-108">新しいデータモデルを作成する</span><span class="sxs-lookup"><span data-stu-id="88509-108">Create a new data model</span></span>
1. <span data-ttu-id="88509-109">[組織管理] > [ワークスペース] > [電子申告] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="88509-109">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
    * <span data-ttu-id="88509-110">「Litware, Inc.」 であることを確認してください。</span><span class="sxs-lookup"><span data-stu-id="88509-110">Make sure that the "Litware, Inc."</span></span> <span data-ttu-id="88509-111">プロバイダーが使用可能であり、アクティブとしてマークされていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="88509-111">provider is available and marked as active.</span></span>  
2. <span data-ttu-id="88509-112">[コンフィギュレーションをレポートする] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="88509-112">Click Reporting configurations.</span></span>
3. <span data-ttu-id="88509-113">[コンフィギュレーションの作成] をクリックすると、ドロップ ダイアログが開きます。</span><span class="sxs-lookup"><span data-stu-id="88509-113">Click Create configuration to open the drop dialog.</span></span>
4. <span data-ttu-id="88509-114">[名称] フィールドに、「財務分析コード・サンプル モデル」と入力します。</span><span class="sxs-lookup"><span data-stu-id="88509-114">In the Name field, type 'Financial dimensions sample model'.</span></span>
5. <span data-ttu-id="88509-115">[コンフィギュレーションの作成] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="88509-115">Click Create configuration.</span></span>
6. <span data-ttu-id="88509-116">[デザイナー] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="88509-116">Click Designer.</span></span>
7. <span data-ttu-id="88509-117">[新規] をクリックすると、ドロップ ダイアログが開きます。</span><span class="sxs-lookup"><span data-stu-id="88509-117">Click New to open the drop dialog.</span></span>
8. <span data-ttu-id="88509-118">[名称] フィールドに、「エントリ」と入力します。</span><span class="sxs-lookup"><span data-stu-id="88509-118">In the Name field, type 'Entry'.</span></span>
9. <span data-ttu-id="88509-119">[追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="88509-119">Click Add.</span></span>
10. <span data-ttu-id="88509-120">[新規] をクリックすると、ドロップ ダイアログが開きます。</span><span class="sxs-lookup"><span data-stu-id="88509-120">Click New to open the drop dialog.</span></span>
11. <span data-ttu-id="88509-121">[名前] フィールドに、「Company」と入力します。</span><span class="sxs-lookup"><span data-stu-id="88509-121">In the Name field, type 'Company'.</span></span>
12. <span data-ttu-id="88509-122">[追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="88509-122">Click Add.</span></span>
    * <span data-ttu-id="88509-123">新規記録リストにモデルを追加します。</span><span class="sxs-lookup"><span data-stu-id="88509-123">We will add to our model a new record list.</span></span> <span data-ttu-id="88509-124">このリストは、選択した財務分析コードの設定を示します（このモデルをデータソースとして使用するERレポート向け）。</span><span class="sxs-lookup"><span data-stu-id="88509-124">This list will expose (for any ER reports using this model as data source) the settings of selected financial dimensions.</span></span> <span data-ttu-id="88509-125">それぞれの財務分析コードは、分析コード設定を表す適切なフィールドを持つレコードとして、このリストに表示されます。</span><span class="sxs-lookup"><span data-stu-id="88509-125">Each financial dimension will be presented in this list as a record with appropriate fields representing dimension's setting.</span></span>  
13. <span data-ttu-id="88509-126">[新規] をクリックすると、ドロップ ダイアログが開きます。</span><span class="sxs-lookup"><span data-stu-id="88509-126">Click New to open the drop dialog.</span></span>
14. <span data-ttu-id="88509-127">[名称] フィールドで、「分析コード設定」と入力します。</span><span class="sxs-lookup"><span data-stu-id="88509-127">In the Name field, type 'Dimensions setting'.</span></span>
15. <span data-ttu-id="88509-128">[品目タイプ] フィールドで、「レコード リスト」を選択します。</span><span class="sxs-lookup"><span data-stu-id="88509-128">In the Item type field, select 'Record list'.</span></span>
16. <span data-ttu-id="88509-129">[追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="88509-129">Click Add.</span></span>
17. <span data-ttu-id="88509-130">[新規] をクリックすると、ドロップ ダイアログが開きます。</span><span class="sxs-lookup"><span data-stu-id="88509-130">Click New to open the drop dialog.</span></span>
18. <span data-ttu-id="88509-131">[名称] フィールドに、「コード」と入力します。</span><span class="sxs-lookup"><span data-stu-id="88509-131">In the Name field, type 'Code'.</span></span>
19. <span data-ttu-id="88509-132">[品目タイプ] フィールドで、「String」を選択します。</span><span class="sxs-lookup"><span data-stu-id="88509-132">In the Item type field, select 'String'.</span></span>
20. <span data-ttu-id="88509-133">[追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="88509-133">Click Add.</span></span>
21. <span data-ttu-id="88509-134">[新規] をクリックすると、ドロップ ダイアログが開きます。</span><span class="sxs-lookup"><span data-stu-id="88509-134">Click New to open the drop dialog.</span></span>
22. <span data-ttu-id="88509-135">[名前] フィールドに、「名前」と入力します。</span><span class="sxs-lookup"><span data-stu-id="88509-135">In the Name field, type 'Name'.</span></span>
23. <span data-ttu-id="88509-136">[追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="88509-136">Click Add.</span></span>
24. <span data-ttu-id="88509-137">ツリーで、「エントリ」を選択します。</span><span class="sxs-lookup"><span data-stu-id="88509-137">In the tree, select 'Entry'.</span></span>
25. <span data-ttu-id="88509-138">[新規] をクリックすると、ドロップ ダイアログが開きます。</span><span class="sxs-lookup"><span data-stu-id="88509-138">Click New to open the drop dialog.</span></span>
26. <span data-ttu-id="88509-139">[名称] フィールドに、「仕訳」と入力します。</span><span class="sxs-lookup"><span data-stu-id="88509-139">In the Name field, type 'Journal'.</span></span>
27. <span data-ttu-id="88509-140">[品目タイプ] フィールドで、「レコード リスト」を選択します。</span><span class="sxs-lookup"><span data-stu-id="88509-140">In the Item type field, select 'Record list'.</span></span>
28. <span data-ttu-id="88509-141">[追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="88509-141">Click Add.</span></span>
29. <span data-ttu-id="88509-142">[新規] をクリックすると、ドロップ ダイアログが開きます。</span><span class="sxs-lookup"><span data-stu-id="88509-142">Click New to open the drop dialog.</span></span>
30. <span data-ttu-id="88509-143">[名称] フィールドに、「バッチ」と入力します。</span><span class="sxs-lookup"><span data-stu-id="88509-143">In the Name field, type 'Batch'.</span></span>
31. <span data-ttu-id="88509-144">[品目タイプ] フィールドで、「String」を選択します。</span><span class="sxs-lookup"><span data-stu-id="88509-144">In the Item type field, select 'String'.</span></span>
32. <span data-ttu-id="88509-145">[追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="88509-145">Click Add.</span></span>
33. <span data-ttu-id="88509-146">[新規] をクリックすると、ドロップ ダイアログが開きます。</span><span class="sxs-lookup"><span data-stu-id="88509-146">Click New to open the drop dialog.</span></span>
34. <span data-ttu-id="88509-147">[名称] フィールドで、「トランザクション」と入力します。</span><span class="sxs-lookup"><span data-stu-id="88509-147">In the Name field, type 'Transaction'.</span></span>
35. <span data-ttu-id="88509-148">[品目タイプ] フィールドで、「レコード リスト」を選択します。</span><span class="sxs-lookup"><span data-stu-id="88509-148">In the Item type field, select 'Record list'.</span></span>
36. <span data-ttu-id="88509-149">[追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="88509-149">Click Add.</span></span>
37. <span data-ttu-id="88509-150">[新規] をクリックすると、ドロップ ダイアログが開きます。</span><span class="sxs-lookup"><span data-stu-id="88509-150">Click New to open the drop dialog.</span></span>
38. <span data-ttu-id="88509-151">[名称] フィールドで、「日付」と入力します。</span><span class="sxs-lookup"><span data-stu-id="88509-151">In the Name field, type 'Date'.</span></span>
39. <span data-ttu-id="88509-152">[品目タイプ] フィールドで、「日付」を選択します。</span><span class="sxs-lookup"><span data-stu-id="88509-152">In the Item type field, select 'Date'.</span></span>
40. <span data-ttu-id="88509-153">[追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="88509-153">Click Add.</span></span>
41. <span data-ttu-id="88509-154">[新規] をクリックすると、ドロップ ダイアログが開きます。</span><span class="sxs-lookup"><span data-stu-id="88509-154">Click New to open the drop dialog.</span></span>
42. <span data-ttu-id="88509-155">[名称] フィールドで、「借方」と入力します。</span><span class="sxs-lookup"><span data-stu-id="88509-155">In the Name field, type 'Debit'.</span></span>
43. <span data-ttu-id="88509-156">[品目タイプ] フィールドで、「実数」を選択します。</span><span class="sxs-lookup"><span data-stu-id="88509-156">In the Item type field, select 'Real'.</span></span>
44. <span data-ttu-id="88509-157">[追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="88509-157">Click Add.</span></span>
45. <span data-ttu-id="88509-158">[新規] をクリックすると、ドロップ ダイアログが開きます。</span><span class="sxs-lookup"><span data-stu-id="88509-158">Click New to open the drop dialog.</span></span>
46. <span data-ttu-id="88509-159">[名称] フィールドで、「貸方」と入力します。</span><span class="sxs-lookup"><span data-stu-id="88509-159">In the Name field, type 'Credit'.</span></span>
47. <span data-ttu-id="88509-160">[追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="88509-160">Click Add.</span></span>
48. <span data-ttu-id="88509-161">[新規] をクリックすると、ドロップ ダイアログが開きます。</span><span class="sxs-lookup"><span data-stu-id="88509-161">Click New to open the drop dialog.</span></span>
49. <span data-ttu-id="88509-162">[名前] フィールドで、「通貨」と入力します。</span><span class="sxs-lookup"><span data-stu-id="88509-162">In the Name field, type 'Currency'.</span></span>
50. <span data-ttu-id="88509-163">[品目タイプ] フィールドで、「String」を選択します。</span><span class="sxs-lookup"><span data-stu-id="88509-163">In the Item type field, select 'String'.</span></span>
51. <span data-ttu-id="88509-164">[追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="88509-164">Click Add.</span></span>
52. <span data-ttu-id="88509-165">[新規] をクリックすると、ドロップ ダイアログが開きます。</span><span class="sxs-lookup"><span data-stu-id="88509-165">Click New to open the drop dialog.</span></span>
53. <span data-ttu-id="88509-166">[名称] フィールドで、「伝票」と入力します。</span><span class="sxs-lookup"><span data-stu-id="88509-166">In the Name field, type 'Voucher'.</span></span>
54. <span data-ttu-id="88509-167">[追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="88509-167">Click Add.</span></span>
55. <span data-ttu-id="88509-168">[新規] をクリックすると、ドロップ ダイアログが開きます。</span><span class="sxs-lookup"><span data-stu-id="88509-168">Click New to open the drop dialog.</span></span>
56. <span data-ttu-id="88509-169">[名称] フィールドで、「分析コードデータ」と入力します。</span><span class="sxs-lookup"><span data-stu-id="88509-169">In the Name field, type 'Dimensions data'.</span></span>
57. <span data-ttu-id="88509-170">[品目タイプ] フィールドで、「レコード リスト」を選択します。</span><span class="sxs-lookup"><span data-stu-id="88509-170">In the Item type field, select 'Record list'.</span></span>
58. <span data-ttu-id="88509-171">[追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="88509-171">Click Add.</span></span>
    * <span data-ttu-id="88509-172">新規記録リストにモデルを追加しました。</span><span class="sxs-lookup"><span data-stu-id="88509-172">We added to our model a new record list.</span></span> <span data-ttu-id="88509-173">このリストは、選択した財務分析コードの値を示します（このモデルをデータソースとして使用するERレポート向け）。</span><span class="sxs-lookup"><span data-stu-id="88509-173">This list will expose (for any ER reports using this model as data source) the values of selected financial dimensions.</span></span> <span data-ttu-id="88509-174">それぞれの財務分析コードは、分析コードの値を表す適切なフィールドを持つレコードとして、このリストに表示されます。</span><span class="sxs-lookup"><span data-stu-id="88509-174">Each financial dimension will be presented in this list as a record with appropriate fields representing dimension's values.</span></span> <span data-ttu-id="88509-175">分析コードの名称は、目的選択用のフィールドとしてこの記録にも表示されます。</span><span class="sxs-lookup"><span data-stu-id="88509-175">Dimension name will be also presented in this record as a field to be used, if needed, for selection purposes.</span></span>  
59. <span data-ttu-id="88509-176">[新規] をクリックすると、ドロップ ダイアログが開きます。</span><span class="sxs-lookup"><span data-stu-id="88509-176">Click New to open the drop dialog.</span></span>
60. <span data-ttu-id="88509-177">[名称] フィールドに、「コード」と入力します。</span><span class="sxs-lookup"><span data-stu-id="88509-177">In the Name field, type 'Code'.</span></span>
61. <span data-ttu-id="88509-178">[品目タイプ] フィールドで、「String」を選択します。</span><span class="sxs-lookup"><span data-stu-id="88509-178">In the Item type field, select 'String'.</span></span>
62. <span data-ttu-id="88509-179">[追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="88509-179">Click Add.</span></span>
63. <span data-ttu-id="88509-180">[新規] をクリックすると、ドロップ ダイアログが開きます。</span><span class="sxs-lookup"><span data-stu-id="88509-180">Click New to open the drop dialog.</span></span>
64. <span data-ttu-id="88509-181">[名前] フィールドに、「説明」と入力します。</span><span class="sxs-lookup"><span data-stu-id="88509-181">In the Name field, type 'Description'.</span></span>
65. <span data-ttu-id="88509-182">[追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="88509-182">Click Add.</span></span>
66. <span data-ttu-id="88509-183">[新規] をクリックすると、ドロップ ダイアログが開きます。</span><span class="sxs-lookup"><span data-stu-id="88509-183">Click New to open the drop dialog.</span></span>
67. <span data-ttu-id="88509-184">[名前] フィールドに、「名前」と入力します。</span><span class="sxs-lookup"><span data-stu-id="88509-184">In the Name field, type 'Name'.</span></span>
68. <span data-ttu-id="88509-185">[追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="88509-185">Click Add.</span></span>
69. <span data-ttu-id="88509-186">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="88509-186">Click Save.</span></span>
70. <span data-ttu-id="88509-187">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="88509-187">Close the page.</span></span>

![ER データ モデル デザイナーのページ](../media/er-financial-dimensions-guides-data-model.png)

