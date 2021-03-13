---
title: ER 財務分析コードをデータ ソースとして使用する (第 3 部 - レポートのデザイン)
description: このトピックでは、財務分析コードを ER レポートのデータ ソースとして使用するために、電子申告 (ER) モデルを構成する方法について説明します。 (第 3 部)
author: NickSelin
manager: AnnBe
ms.date: 05/27/2020
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERSolutionTable, ERSolutionCreateDropDialog, EROperationDesigner, ERComponentTypeDropDialog
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b0d6da96850e04d5e975b3febbfae2737c8a86af
ms.sourcegitcommit: 5192cfaedfd861faea63d8954d7bcc500608a225
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/30/2021
ms.locfileid: "5092303"
---
# <a name="er-use-financial-dimensions-as-a-data-source-part-3---design-the-report"></a><span data-ttu-id="91066-104">ER 財務分析コードをデータ ソースとして使用する (第 3 部 - レポートのデザイン)</span><span class="sxs-lookup"><span data-stu-id="91066-104">ER Use financial dimensions as a data source (Part 3 - Design the report)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="91066-105">次の手順では、システム管理者に指定されたユーザーまたは電子レポート開発者のロールが、電子レポート・データソースとしての財務分析コードを使用するために 電子レポート（ER）モデルをどのように環境設定しているのか説明します。</span><span class="sxs-lookup"><span data-stu-id="91066-105">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) model to use financial dimensions as a data source for ER reports.</span></span> <span data-ttu-id="91066-106">これらの手順はどのタイプの企業でも実施できます。</span><span class="sxs-lookup"><span data-stu-id="91066-106">These steps can be performed in any company.</span></span>

<span data-ttu-id="91066-107">この手順を実施するには、まず 「ER 財務分析コードをデータ ソースとして使用する（パート2：モデル マッピング）」に記載の手順を実施する必要があります。</span><span class="sxs-lookup"><span data-stu-id="91066-107">To complete these steps, you must first complete the steps in the "ER Use financial dimensions as a data source (Part 2: Model mapping)" procedure.</span></span>


## <a name="design-a-report-to-present-financial-dimensions"></a><span data-ttu-id="91066-108">財務分析コードを示すレポートを作成する</span><span class="sxs-lookup"><span data-stu-id="91066-108">Design a report to present financial dimensions</span></span>
1. <span data-ttu-id="91066-109">[組織管理] > [電子申告] > [コンフィギュレーション] に移動します。</span><span class="sxs-lookup"><span data-stu-id="91066-109">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="91066-110">[ツリー] フィールドで、「財務分析コード・サンプル モデル」を選択します。</span><span class="sxs-lookup"><span data-stu-id="91066-110">In the tree, select 'Financial dimensions sample model'.</span></span>
3. <span data-ttu-id="91066-111">[コンフィギュレーションの作成] をクリックすると、ドロップ ダイアログが開きます。</span><span class="sxs-lookup"><span data-stu-id="91066-111">Click Create configuration to open the drop dialog.</span></span>
4. <span data-ttu-id="91066-112">[新規] フィールドで、「財務分析コード・サンプルモデルに基づくフォーマット」を入力します。</span><span class="sxs-lookup"><span data-stu-id="91066-112">In the New field, enter 'Format based on data model Financial dimensions sample model'.</span></span>
    * <span data-ttu-id="91066-113">新しいレポートのデータ ソースとして事前に作成されたモデルを使用します。</span><span class="sxs-lookup"><span data-stu-id="91066-113">Use the model that was created in advance as the data source for your new report.</span></span>  
5. <span data-ttu-id="91066-114">[名称] フィールドで、「Ledger journal report」を入力します。</span><span class="sxs-lookup"><span data-stu-id="91066-114">In the Name field, type 'Ledger journal report'.</span></span>
6. <span data-ttu-id="91066-115">[データモデル定義] フィールドで、「エントリ」を選択します。</span><span class="sxs-lookup"><span data-stu-id="91066-115">In the Data model definition field, select Entry.</span></span>
7. <span data-ttu-id="91066-116">[コンフィギュレーションの作成] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="91066-116">Click Create configuration.</span></span>
8. <span data-ttu-id="91066-117">[デザイナー] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="91066-117">Click Designer.</span></span>
9. <span data-ttu-id="91066-118">[ルートの追加] をクリックして、ドロップ ダイアログを開きます。</span><span class="sxs-lookup"><span data-stu-id="91066-118">Click Add root to open the drop dialog.</span></span>
10. <span data-ttu-id="91066-119">ツリーで、[XML\Element] を選択します。</span><span class="sxs-lookup"><span data-stu-id="91066-119">In the tree, select 'XML\Element'.</span></span>
11. <span data-ttu-id="91066-120">[名称] のフィールドに、「Root」を入力します。</span><span class="sxs-lookup"><span data-stu-id="91066-120">In the Name field, type 'Root'.</span></span>
12. <span data-ttu-id="91066-121">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="91066-121">Click OK.</span></span>
13. <span data-ttu-id="91066-122">[追加] をクリックしてドロップ ダイアログを開きます。</span><span class="sxs-lookup"><span data-stu-id="91066-122">Click Add to open the drop dialog.</span></span>
14. <span data-ttu-id="91066-123">ツリーで、[XML\Attribute] を選択します。</span><span class="sxs-lookup"><span data-stu-id="91066-123">In the tree, select 'XML\Attribute'.</span></span>
15. <span data-ttu-id="91066-124">[名前] フィールドに、「Company」と入力します。</span><span class="sxs-lookup"><span data-stu-id="91066-124">In the Name field, type 'Company'.</span></span>
16. <span data-ttu-id="91066-125">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="91066-125">Click OK.</span></span>
17. <span data-ttu-id="91066-126">[追加] をクリックしてドロップ ダイアログを開きます。</span><span class="sxs-lookup"><span data-stu-id="91066-126">Click Add to open the drop dialog.</span></span>
18. <span data-ttu-id="91066-127">ツリーで、[XML\Element] を選択します。</span><span class="sxs-lookup"><span data-stu-id="91066-127">In the tree, select 'XML\Element'.</span></span>
19. <span data-ttu-id="91066-128">[名称] フィールドに、「仕訳」と入力します。</span><span class="sxs-lookup"><span data-stu-id="91066-128">In the Name field, type 'Journal'.</span></span>
20. <span data-ttu-id="91066-129">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="91066-129">Click OK.</span></span>
21. <span data-ttu-id="91066-130">ツリーで、「Root: XML Element\Journal: XML Element」を選択します。</span><span class="sxs-lookup"><span data-stu-id="91066-130">In the tree, select 'Root: XML Element\Journal: XML Element'.</span></span>
22. <span data-ttu-id="91066-131">[追加] をクリックしてドロップ ダイアログを開きます。</span><span class="sxs-lookup"><span data-stu-id="91066-131">Click Add to open the drop dialog.</span></span>
23. <span data-ttu-id="91066-132">ツリーで、[XML\Attribute] を選択します。</span><span class="sxs-lookup"><span data-stu-id="91066-132">In the tree, select 'XML\Attribute'.</span></span>
24. <span data-ttu-id="91066-133">[名称] フィールドに、「バッチ」と入力します。</span><span class="sxs-lookup"><span data-stu-id="91066-133">In the Name field, type 'Batch'.</span></span>
25. <span data-ttu-id="91066-134">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="91066-134">Click OK.</span></span>
26. <span data-ttu-id="91066-135">[追加] をクリックしてドロップ ダイアログを開きます。</span><span class="sxs-lookup"><span data-stu-id="91066-135">Click Add to open the drop dialog.</span></span>
27. <span data-ttu-id="91066-136">ツリーで、[XML\Element] を選択します。</span><span class="sxs-lookup"><span data-stu-id="91066-136">In the tree, select 'XML\Element'.</span></span>
28. <span data-ttu-id="91066-137">[名称] フィールドで、「トランザクション」と入力します。</span><span class="sxs-lookup"><span data-stu-id="91066-137">In the Name field, type 'Transaction'.</span></span>
29. <span data-ttu-id="91066-138">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="91066-138">Click OK.</span></span>
30. <span data-ttu-id="91066-139">ツリーで、「Root: XML Element\Journal: XML Element\Transaction: XML Element」を選択します。</span><span class="sxs-lookup"><span data-stu-id="91066-139">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element'.</span></span>
31. <span data-ttu-id="91066-140">[追加] をクリックしてドロップ ダイアログを開きます。</span><span class="sxs-lookup"><span data-stu-id="91066-140">Click Add to open the drop dialog.</span></span>
32. <span data-ttu-id="91066-141">ツリーで、[XML\Attribute] を選択します。</span><span class="sxs-lookup"><span data-stu-id="91066-141">In the tree, select 'XML\Attribute'.</span></span>
33. <span data-ttu-id="91066-142">[名称] フィールドで、「伝票」と入力します。</span><span class="sxs-lookup"><span data-stu-id="91066-142">In the Name field, type 'Voucher'.</span></span>
34. <span data-ttu-id="91066-143">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="91066-143">Click OK.</span></span>
35. <span data-ttu-id="91066-144">[属性を加える] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="91066-144">Click Add Attribute.</span></span>
36. <span data-ttu-id="91066-145">[名称] フィールドで、「日付」と入力します。</span><span class="sxs-lookup"><span data-stu-id="91066-145">In the Name field, type 'Date'.</span></span>
37. <span data-ttu-id="91066-146">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="91066-146">Click OK.</span></span>
38. <span data-ttu-id="91066-147">[属性を加える] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="91066-147">Click Add Attribute.</span></span>
39. <span data-ttu-id="91066-148">[名前] フィールドで、「通貨」と入力します。</span><span class="sxs-lookup"><span data-stu-id="91066-148">In the Name field, type 'Currency'.</span></span>
40. <span data-ttu-id="91066-149">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="91066-149">Click OK.</span></span>
41. <span data-ttu-id="91066-150">[属性を加える] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="91066-150">Click Add Attribute.</span></span>
42. <span data-ttu-id="91066-151">[名称] フィールドに、「Dt」と入力します。</span><span class="sxs-lookup"><span data-stu-id="91066-151">In the Name field, type 'Dt'.</span></span>
43. <span data-ttu-id="91066-152">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="91066-152">Click OK.</span></span>
44. <span data-ttu-id="91066-153">[属性を加える] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="91066-153">Click Add Attribute.</span></span>
45. <span data-ttu-id="91066-154">[名称] フィールドに、「Ct」と入力します。</span><span class="sxs-lookup"><span data-stu-id="91066-154">In the Name field, type 'Ct'.</span></span>
46. <span data-ttu-id="91066-155">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="91066-155">Click OK.</span></span>
47. <span data-ttu-id="91066-156">[追加] をクリックしてドロップ ダイアログを開きます。</span><span class="sxs-lookup"><span data-stu-id="91066-156">Click Add to open the drop dialog.</span></span>
48. <span data-ttu-id="91066-157">ツリーで、[XML\Element] を選択します。</span><span class="sxs-lookup"><span data-stu-id="91066-157">In the tree, select 'XML\Element'.</span></span>
49. <span data-ttu-id="91066-158">[名称] フィールドに、「分析コード」を入力します。</span><span class="sxs-lookup"><span data-stu-id="91066-158">In the Name field, type 'Dimensions'.</span></span>
50. <span data-ttu-id="91066-159">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="91066-159">Click OK.</span></span>
51. <span data-ttu-id="91066-160">ツリーで、「Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element'」を選択します。</span><span class="sxs-lookup"><span data-stu-id="91066-160">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element'.</span></span>
52. <span data-ttu-id="91066-161">[追加] をクリックしてドロップ ダイアログを開きます。</span><span class="sxs-lookup"><span data-stu-id="91066-161">Click Add to open the drop dialog.</span></span>
53. <span data-ttu-id="91066-162">ツリーで、[XML\Attribute] を選択します。</span><span class="sxs-lookup"><span data-stu-id="91066-162">In the tree, select 'XML\Attribute'.</span></span>
54. <span data-ttu-id="91066-163">[名称] フィールドに、「コード」と入力します。</span><span class="sxs-lookup"><span data-stu-id="91066-163">In the Name field, type 'Code'.</span></span>
55. <span data-ttu-id="91066-164">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="91066-164">Click OK.</span></span>
56. <span data-ttu-id="91066-165">[属性を加える] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="91066-165">Click Add Attribute.</span></span>
57. <span data-ttu-id="91066-166">[名称] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="91066-166">In the Name field, type 'Value'.</span></span>
58. <span data-ttu-id="91066-167">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="91066-167">Click OK.</span></span>
59. <span data-ttu-id="91066-168">[属性を加える] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="91066-168">Click Add Attribute.</span></span>
60. <span data-ttu-id="91066-169">[名称] フィールドに説明を入力します。</span><span class="sxs-lookup"><span data-stu-id="91066-169">In the Name field, type 'Desc'.</span></span>
61. <span data-ttu-id="91066-170">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="91066-170">Click OK.</span></span>
<span data-ttu-id="91066-171">![ER Operations デザイナーのページ](../media/er-financial-dimensions-guides-format1.png)</span><span class="sxs-lookup"><span data-stu-id="91066-171">![ER Operations designer page](../media/er-financial-dimensions-guides-format1.png)</span></span>

## <a name="map-report-elements-to-data-sources"></a><span data-ttu-id="91066-172">レポートエレメントをデータソースにマッピングする</span><span class="sxs-lookup"><span data-stu-id="91066-172">Map report elements to data sources</span></span>
1. <span data-ttu-id="91066-173">[マッピング] タブをクリックします。</span><span class="sxs-lookup"><span data-stu-id="91066-173">Click the Mapping tab.</span></span>
2. <span data-ttu-id="91066-174">ツリーで、「model: Data model Financial dimensions sample model」を展開します。</span><span class="sxs-lookup"><span data-stu-id="91066-174">In the tree, expand 'model: Data model Financial dimensions sample model'.</span></span>
3. <span data-ttu-id="91066-175">ツリーで、「model: Data model Financial dimensions sample model\Journal: Record list」を展開します。</span><span class="sxs-lookup"><span data-stu-id="91066-175">In the tree, expand 'model: Data model Financial dimensions sample model\Journal: Record list'.</span></span>
4. <span data-ttu-id="91066-176">ツリーで、「model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list」を展開します。</span><span class="sxs-lookup"><span data-stu-id="91066-176">In the tree, expand 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list'.</span></span>
5. <span data-ttu-id="91066-177">ツリーで、「model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list」を展開します。</span><span class="sxs-lookup"><span data-stu-id="91066-177">In the tree, expand 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list'.</span></span>
6. <span data-ttu-id="91066-178">ツリーで、「Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element\Desc: XML Attribute」を選択します。</span><span class="sxs-lookup"><span data-stu-id="91066-178">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element\Desc: XML Attribute'.</span></span>
7. <span data-ttu-id="91066-179">ツリーで、「model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list\Description: String」を展開します。</span><span class="sxs-lookup"><span data-stu-id="91066-179">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list\Description: String'.</span></span>
8. <span data-ttu-id="91066-180">[バインド] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="91066-180">Click Bind.</span></span>
9. <span data-ttu-id="91066-181">ツリーで、「Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element\Value: XML Attribute」を選択します。</span><span class="sxs-lookup"><span data-stu-id="91066-181">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element\Value: XML Attribute'.</span></span>
10. <span data-ttu-id="91066-182">ツリーで、「model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record listt\Code: String」を選択します。</span><span class="sxs-lookup"><span data-stu-id="91066-182">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list\Code: String'.</span></span>
11. <span data-ttu-id="91066-183">[バインド] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="91066-183">Click Bind.</span></span>
12. <span data-ttu-id="91066-184">ツリーで、「Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element\Code: XML Attribute」を選択します。</span><span class="sxs-lookup"><span data-stu-id="91066-184">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element\Code: XML Attribute'.</span></span>
13. <span data-ttu-id="91066-185">ツリーで、「model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list\Name: String」を選択します。</span><span class="sxs-lookup"><span data-stu-id="91066-185">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list\Name: String'.</span></span>
14. <span data-ttu-id="91066-186">[バインド] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="91066-186">Click Bind.</span></span>
15. <span data-ttu-id="91066-187">ツリーで、「model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list」を展開します。</span><span class="sxs-lookup"><span data-stu-id="91066-187">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list'.</span></span>
16. <span data-ttu-id="91066-188">ツリーで、「Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element'」を選択します。</span><span class="sxs-lookup"><span data-stu-id="91066-188">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element'.</span></span>
17. <span data-ttu-id="91066-189">[バインド] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="91066-189">Click Bind.</span></span>
18. <span data-ttu-id="91066-190">ツリーで、「Root: XML Element\Journal: XML Element\Transaction: XML Element\Ct: XML Attribute'」を選択します。</span><span class="sxs-lookup"><span data-stu-id="91066-190">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Ct: XML Attribute'.</span></span>
19. <span data-ttu-id="91066-191">ツリーで、「model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Credit: Real」を選択します。</span><span class="sxs-lookup"><span data-stu-id="91066-191">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Credit: Real'.</span></span>
20. <span data-ttu-id="91066-192">[バインド] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="91066-192">Click Bind.</span></span>
21. <span data-ttu-id="91066-193">ツリーで、「Root: XML Element\Journal: XML Element\Transaction: XML Element\Dt: XML Attribute'」を選択します。</span><span class="sxs-lookup"><span data-stu-id="91066-193">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dt: XML Attribute'.</span></span>
22. <span data-ttu-id="91066-194">ツリーで、「model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Debit: Real」を選択します。</span><span class="sxs-lookup"><span data-stu-id="91066-194">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Debit: Real'.</span></span>
23. <span data-ttu-id="91066-195">[バインド] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="91066-195">Click Bind.</span></span>
24. <span data-ttu-id="91066-196">ツリーで、「Root: XML Element\Journal: XML Element\Transaction: XML Element\Currency: XML Attribute'」を選択します。</span><span class="sxs-lookup"><span data-stu-id="91066-196">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Currency: XML Attribute'.</span></span>
25. <span data-ttu-id="91066-197">ツリーで、「model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Currency: String」を選択します。</span><span class="sxs-lookup"><span data-stu-id="91066-197">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Currency: String'.</span></span>
26. <span data-ttu-id="91066-198">[バインド] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="91066-198">Click Bind.</span></span>
27. <span data-ttu-id="91066-199">ツリーで、「Root: XML Element\Journal: XML Element\Transaction: XML Element\Date: XML Attribute'」を選択します。</span><span class="sxs-lookup"><span data-stu-id="91066-199">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Date: XML Attribute'.</span></span>
28. <span data-ttu-id="91066-200">ツリーで、「model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Date: Date」を選択します。</span><span class="sxs-lookup"><span data-stu-id="91066-200">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Date: Date'.</span></span>
29. <span data-ttu-id="91066-201">[バインド] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="91066-201">Click Bind.</span></span>
30. <span data-ttu-id="91066-202">ツリーで、「Root: XML Element\Journal: XML Element\Transaction: XML Element\Voucher: XML Attribute'」を選択します。</span><span class="sxs-lookup"><span data-stu-id="91066-202">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Voucher: XML Attribute'.</span></span>
31. <span data-ttu-id="91066-203">ツリーで、「model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Currency: String」を選択します。</span><span class="sxs-lookup"><span data-stu-id="91066-203">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Voucher: String'.</span></span>
32. <span data-ttu-id="91066-204">[バインド] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="91066-204">Click Bind.</span></span>
33. <span data-ttu-id="91066-205">ツリーで、「Root: XML Element\Journal: XML Element\Transaction: XML Element」を選択します。</span><span class="sxs-lookup"><span data-stu-id="91066-205">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element'.</span></span>
34. <span data-ttu-id="91066-206">ツリーで、「model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list」を選択します。</span><span class="sxs-lookup"><span data-stu-id="91066-206">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list'.</span></span>
35. <span data-ttu-id="91066-207">[バインド] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="91066-207">Click Bind.</span></span>
36. <span data-ttu-id="91066-208">ツリーで、「Root: XML Element\Journal: XML Element\Batch: XML Attribute」を選択します。</span><span class="sxs-lookup"><span data-stu-id="91066-208">In the tree, select 'Root: XML Element\Journal: XML Element\Batch: XML Attribute'.</span></span>
37. <span data-ttu-id="91066-209">ツリーで、「model: Data model Financial dimensions sample model\Journal: Record list\Batch: String」を選択します。</span><span class="sxs-lookup"><span data-stu-id="91066-209">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Batch: String'.</span></span>
38. <span data-ttu-id="91066-210">[バインド] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="91066-210">Click Bind.</span></span>
39. <span data-ttu-id="91066-211">ツリーで、「Root: XML Element\Journal: XML Element」を選択します。</span><span class="sxs-lookup"><span data-stu-id="91066-211">In the tree, select 'Root: XML Element\Journal: XML Element'.</span></span>
40. <span data-ttu-id="91066-212">ツリーで、「model: Data model Financial dimensions sample model\Journal: Record list」を選択します。</span><span class="sxs-lookup"><span data-stu-id="91066-212">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list'.</span></span>
41. <span data-ttu-id="91066-213">[バインド] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="91066-213">Click Bind.</span></span>
42. <span data-ttu-id="91066-214">ツリーで、「Root: XML Element\Company: XML Attribute」を選択します。</span><span class="sxs-lookup"><span data-stu-id="91066-214">In the tree, select 'Root: XML Element\Company: XML Attribute'.</span></span>
43. <span data-ttu-id="91066-215">ツリーで、「model: Data model Financial dimensions sample model\Company: String」を選択します。</span><span class="sxs-lookup"><span data-stu-id="91066-215">In the tree, select 'model: Data model Financial dimensions sample model\Company: String'.</span></span>
44. <span data-ttu-id="91066-216">[バインド] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="91066-216">Click Bind.</span></span>
45. <span data-ttu-id="91066-217">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="91066-217">Click Save.</span></span>
46. <span data-ttu-id="91066-218">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="91066-218">Close the page.</span></span>
<span data-ttu-id="91066-219">![ER Operations デザイナーのページ](../media/er-financial-dimensions-guides-format2.png)</span><span class="sxs-lookup"><span data-stu-id="91066-219">![ER Operations designer page](../media/er-financial-dimensions-guides-format2.png)</span></span>

