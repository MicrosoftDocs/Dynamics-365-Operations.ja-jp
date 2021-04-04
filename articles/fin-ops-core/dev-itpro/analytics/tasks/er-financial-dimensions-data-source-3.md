---
title: ER 財務分析コードをデータ ソースとして使用する (第 3 部 - レポートのデザイン)
description: このトピックでは、財務分析コードを ER レポートのデータ ソースとして使用するために、電子申告 (ER) モデルを構成する方法について説明します。 (第 3 部)
author: NickSelin
manager: AnnBe
ms.date: 05/27/2020
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ERSolutionTable, ERSolutionCreateDropDialog, EROperationDesigner, ERComponentTypeDropDialog
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a9594a12c28109d80c6ee07a9ee38f4923963dca
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/09/2021
ms.locfileid: "5565241"
---
# <a name="er-use-financial-dimensions-as-a-data-source-part-3---design-the-report"></a><span data-ttu-id="8a60f-104">ER 財務分析コードをデータ ソースとして使用する (第 3 部 - レポートのデザイン)</span><span class="sxs-lookup"><span data-stu-id="8a60f-104">ER Use financial dimensions as a data source (Part 3 - Design the report)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="8a60f-105">次の手順では、システム管理者に指定されたユーザーまたは電子レポート開発者のロールが、電子レポート・データソースとしての財務分析コードを使用するために 電子レポート（ER）モデルをどのように環境設定しているのか説明します。</span><span class="sxs-lookup"><span data-stu-id="8a60f-105">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) model to use financial dimensions as a data source for ER reports.</span></span> <span data-ttu-id="8a60f-106">これらの手順はどのタイプの企業でも実施できます。</span><span class="sxs-lookup"><span data-stu-id="8a60f-106">These steps can be performed in any company.</span></span>

<span data-ttu-id="8a60f-107">この手順を実施するには、まず 「ER 財務分析コードをデータ ソースとして使用する（パート2：モデル マッピング）」に記載の手順を実施する必要があります。</span><span class="sxs-lookup"><span data-stu-id="8a60f-107">To complete these steps, you must first complete the steps in the "ER Use financial dimensions as a data source (Part 2: Model mapping)" procedure.</span></span>


## <a name="design-a-report-to-present-financial-dimensions"></a><span data-ttu-id="8a60f-108">財務分析コードを示すレポートを作成する</span><span class="sxs-lookup"><span data-stu-id="8a60f-108">Design a report to present financial dimensions</span></span>
1. <span data-ttu-id="8a60f-109">[組織管理] > [電子申告] > [コンフィギュレーション] に移動します。</span><span class="sxs-lookup"><span data-stu-id="8a60f-109">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="8a60f-110">[ツリー] フィールドで、「財務分析コード・サンプル モデル」を選択します。</span><span class="sxs-lookup"><span data-stu-id="8a60f-110">In the tree, select 'Financial dimensions sample model'.</span></span>
3. <span data-ttu-id="8a60f-111">[コンフィギュレーションの作成] をクリックすると、ドロップ ダイアログが開きます。</span><span class="sxs-lookup"><span data-stu-id="8a60f-111">Click Create configuration to open the drop dialog.</span></span>
4. <span data-ttu-id="8a60f-112">[新規] フィールドで、「財務分析コード・サンプルモデルに基づくフォーマット」を入力します。</span><span class="sxs-lookup"><span data-stu-id="8a60f-112">In the New field, enter 'Format based on data model Financial dimensions sample model'.</span></span>
    * <span data-ttu-id="8a60f-113">新しいレポートのデータ ソースとして事前に作成されたモデルを使用します。</span><span class="sxs-lookup"><span data-stu-id="8a60f-113">Use the model that was created in advance as the data source for your new report.</span></span>  
5. <span data-ttu-id="8a60f-114">[名称] フィールドで、「Ledger journal report」を入力します。</span><span class="sxs-lookup"><span data-stu-id="8a60f-114">In the Name field, type 'Ledger journal report'.</span></span>
6. <span data-ttu-id="8a60f-115">[データモデル定義] フィールドで、「エントリ」を選択します。</span><span class="sxs-lookup"><span data-stu-id="8a60f-115">In the Data model definition field, select Entry.</span></span>
7. <span data-ttu-id="8a60f-116">[コンフィギュレーションの作成] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8a60f-116">Click Create configuration.</span></span>
8. <span data-ttu-id="8a60f-117">[デザイナー] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8a60f-117">Click Designer.</span></span>
9. <span data-ttu-id="8a60f-118">[ルートの追加] をクリックして、ドロップ ダイアログを開きます。</span><span class="sxs-lookup"><span data-stu-id="8a60f-118">Click Add root to open the drop dialog.</span></span>
10. <span data-ttu-id="8a60f-119">ツリーで、[XML\Element] を選択します。</span><span class="sxs-lookup"><span data-stu-id="8a60f-119">In the tree, select 'XML\Element'.</span></span>
11. <span data-ttu-id="8a60f-120">[名称] のフィールドに、「Root」を入力します。</span><span class="sxs-lookup"><span data-stu-id="8a60f-120">In the Name field, type 'Root'.</span></span>
12. <span data-ttu-id="8a60f-121">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8a60f-121">Click OK.</span></span>
13. <span data-ttu-id="8a60f-122">[追加] をクリックしてドロップ ダイアログを開きます。</span><span class="sxs-lookup"><span data-stu-id="8a60f-122">Click Add to open the drop dialog.</span></span>
14. <span data-ttu-id="8a60f-123">ツリーで、[XML\Attribute] を選択します。</span><span class="sxs-lookup"><span data-stu-id="8a60f-123">In the tree, select 'XML\Attribute'.</span></span>
15. <span data-ttu-id="8a60f-124">[名前] フィールドに、「Company」と入力します。</span><span class="sxs-lookup"><span data-stu-id="8a60f-124">In the Name field, type 'Company'.</span></span>
16. <span data-ttu-id="8a60f-125">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8a60f-125">Click OK.</span></span>
17. <span data-ttu-id="8a60f-126">[追加] をクリックしてドロップ ダイアログを開きます。</span><span class="sxs-lookup"><span data-stu-id="8a60f-126">Click Add to open the drop dialog.</span></span>
18. <span data-ttu-id="8a60f-127">ツリーで、[XML\Element] を選択します。</span><span class="sxs-lookup"><span data-stu-id="8a60f-127">In the tree, select 'XML\Element'.</span></span>
19. <span data-ttu-id="8a60f-128">[名称] フィールドに、「仕訳」と入力します。</span><span class="sxs-lookup"><span data-stu-id="8a60f-128">In the Name field, type 'Journal'.</span></span>
20. <span data-ttu-id="8a60f-129">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8a60f-129">Click OK.</span></span>
21. <span data-ttu-id="8a60f-130">ツリーで、「Root: XML Element\Journal: XML Element」を選択します。</span><span class="sxs-lookup"><span data-stu-id="8a60f-130">In the tree, select 'Root: XML Element\Journal: XML Element'.</span></span>
22. <span data-ttu-id="8a60f-131">[追加] をクリックしてドロップ ダイアログを開きます。</span><span class="sxs-lookup"><span data-stu-id="8a60f-131">Click Add to open the drop dialog.</span></span>
23. <span data-ttu-id="8a60f-132">ツリーで、[XML\Attribute] を選択します。</span><span class="sxs-lookup"><span data-stu-id="8a60f-132">In the tree, select 'XML\Attribute'.</span></span>
24. <span data-ttu-id="8a60f-133">[名称] フィールドに、「バッチ」と入力します。</span><span class="sxs-lookup"><span data-stu-id="8a60f-133">In the Name field, type 'Batch'.</span></span>
25. <span data-ttu-id="8a60f-134">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8a60f-134">Click OK.</span></span>
26. <span data-ttu-id="8a60f-135">[追加] をクリックしてドロップ ダイアログを開きます。</span><span class="sxs-lookup"><span data-stu-id="8a60f-135">Click Add to open the drop dialog.</span></span>
27. <span data-ttu-id="8a60f-136">ツリーで、[XML\Element] を選択します。</span><span class="sxs-lookup"><span data-stu-id="8a60f-136">In the tree, select 'XML\Element'.</span></span>
28. <span data-ttu-id="8a60f-137">[名称] フィールドで、「トランザクション」と入力します。</span><span class="sxs-lookup"><span data-stu-id="8a60f-137">In the Name field, type 'Transaction'.</span></span>
29. <span data-ttu-id="8a60f-138">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8a60f-138">Click OK.</span></span>
30. <span data-ttu-id="8a60f-139">ツリーで、「Root: XML Element\Journal: XML Element\Transaction: XML Element」を選択します。</span><span class="sxs-lookup"><span data-stu-id="8a60f-139">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element'.</span></span>
31. <span data-ttu-id="8a60f-140">[追加] をクリックしてドロップ ダイアログを開きます。</span><span class="sxs-lookup"><span data-stu-id="8a60f-140">Click Add to open the drop dialog.</span></span>
32. <span data-ttu-id="8a60f-141">ツリーで、[XML\Attribute] を選択します。</span><span class="sxs-lookup"><span data-stu-id="8a60f-141">In the tree, select 'XML\Attribute'.</span></span>
33. <span data-ttu-id="8a60f-142">[名称] フィールドで、「伝票」と入力します。</span><span class="sxs-lookup"><span data-stu-id="8a60f-142">In the Name field, type 'Voucher'.</span></span>
34. <span data-ttu-id="8a60f-143">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8a60f-143">Click OK.</span></span>
35. <span data-ttu-id="8a60f-144">[属性を加える] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8a60f-144">Click Add Attribute.</span></span>
36. <span data-ttu-id="8a60f-145">[名称] フィールドで、「日付」と入力します。</span><span class="sxs-lookup"><span data-stu-id="8a60f-145">In the Name field, type 'Date'.</span></span>
37. <span data-ttu-id="8a60f-146">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8a60f-146">Click OK.</span></span>
38. <span data-ttu-id="8a60f-147">[属性を加える] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8a60f-147">Click Add Attribute.</span></span>
39. <span data-ttu-id="8a60f-148">[名前] フィールドで、「通貨」と入力します。</span><span class="sxs-lookup"><span data-stu-id="8a60f-148">In the Name field, type 'Currency'.</span></span>
40. <span data-ttu-id="8a60f-149">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8a60f-149">Click OK.</span></span>
41. <span data-ttu-id="8a60f-150">[属性を加える] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8a60f-150">Click Add Attribute.</span></span>
42. <span data-ttu-id="8a60f-151">[名称] フィールドに、「Dt」と入力します。</span><span class="sxs-lookup"><span data-stu-id="8a60f-151">In the Name field, type 'Dt'.</span></span>
43. <span data-ttu-id="8a60f-152">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8a60f-152">Click OK.</span></span>
44. <span data-ttu-id="8a60f-153">[属性を加える] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8a60f-153">Click Add Attribute.</span></span>
45. <span data-ttu-id="8a60f-154">[名称] フィールドに、「Ct」と入力します。</span><span class="sxs-lookup"><span data-stu-id="8a60f-154">In the Name field, type 'Ct'.</span></span>
46. <span data-ttu-id="8a60f-155">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8a60f-155">Click OK.</span></span>
47. <span data-ttu-id="8a60f-156">[追加] をクリックしてドロップ ダイアログを開きます。</span><span class="sxs-lookup"><span data-stu-id="8a60f-156">Click Add to open the drop dialog.</span></span>
48. <span data-ttu-id="8a60f-157">ツリーで、[XML\Element] を選択します。</span><span class="sxs-lookup"><span data-stu-id="8a60f-157">In the tree, select 'XML\Element'.</span></span>
49. <span data-ttu-id="8a60f-158">[名称] フィールドに、「分析コード」を入力します。</span><span class="sxs-lookup"><span data-stu-id="8a60f-158">In the Name field, type 'Dimensions'.</span></span>
50. <span data-ttu-id="8a60f-159">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8a60f-159">Click OK.</span></span>
51. <span data-ttu-id="8a60f-160">ツリーで、「Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element'」を選択します。</span><span class="sxs-lookup"><span data-stu-id="8a60f-160">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element'.</span></span>
52. <span data-ttu-id="8a60f-161">[追加] をクリックしてドロップ ダイアログを開きます。</span><span class="sxs-lookup"><span data-stu-id="8a60f-161">Click Add to open the drop dialog.</span></span>
53. <span data-ttu-id="8a60f-162">ツリーで、[XML\Attribute] を選択します。</span><span class="sxs-lookup"><span data-stu-id="8a60f-162">In the tree, select 'XML\Attribute'.</span></span>
54. <span data-ttu-id="8a60f-163">[名称] フィールドに、「コード」と入力します。</span><span class="sxs-lookup"><span data-stu-id="8a60f-163">In the Name field, type 'Code'.</span></span>
55. <span data-ttu-id="8a60f-164">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8a60f-164">Click OK.</span></span>
56. <span data-ttu-id="8a60f-165">[属性を加える] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8a60f-165">Click Add Attribute.</span></span>
57. <span data-ttu-id="8a60f-166">[名称] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="8a60f-166">In the Name field, type 'Value'.</span></span>
58. <span data-ttu-id="8a60f-167">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8a60f-167">Click OK.</span></span>
59. <span data-ttu-id="8a60f-168">[属性を加える] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8a60f-168">Click Add Attribute.</span></span>
60. <span data-ttu-id="8a60f-169">[名称] フィールドに説明を入力します。</span><span class="sxs-lookup"><span data-stu-id="8a60f-169">In the Name field, type 'Desc'.</span></span>
61. <span data-ttu-id="8a60f-170">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8a60f-170">Click OK.</span></span>
<span data-ttu-id="8a60f-171">![ER Operations デザイナーのページ](../media/er-financial-dimensions-guides-format1.png)</span><span class="sxs-lookup"><span data-stu-id="8a60f-171">![ER Operations designer page](../media/er-financial-dimensions-guides-format1.png)</span></span>

## <a name="map-report-elements-to-data-sources"></a><span data-ttu-id="8a60f-172">レポートエレメントをデータソースにマッピングする</span><span class="sxs-lookup"><span data-stu-id="8a60f-172">Map report elements to data sources</span></span>
1. <span data-ttu-id="8a60f-173">[マッピング] タブをクリックします。</span><span class="sxs-lookup"><span data-stu-id="8a60f-173">Click the Mapping tab.</span></span>
2. <span data-ttu-id="8a60f-174">ツリーで、「model: Data model Financial dimensions sample model」を展開します。</span><span class="sxs-lookup"><span data-stu-id="8a60f-174">In the tree, expand 'model: Data model Financial dimensions sample model'.</span></span>
3. <span data-ttu-id="8a60f-175">ツリーで、「model: Data model Financial dimensions sample model\Journal: Record list」を展開します。</span><span class="sxs-lookup"><span data-stu-id="8a60f-175">In the tree, expand 'model: Data model Financial dimensions sample model\Journal: Record list'.</span></span>
4. <span data-ttu-id="8a60f-176">ツリーで、「model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list」を展開します。</span><span class="sxs-lookup"><span data-stu-id="8a60f-176">In the tree, expand 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list'.</span></span>
5. <span data-ttu-id="8a60f-177">ツリーで、「model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list」を展開します。</span><span class="sxs-lookup"><span data-stu-id="8a60f-177">In the tree, expand 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list'.</span></span>
6. <span data-ttu-id="8a60f-178">ツリーで、「Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element\Desc: XML Attribute」を選択します。</span><span class="sxs-lookup"><span data-stu-id="8a60f-178">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element\Desc: XML Attribute'.</span></span>
7. <span data-ttu-id="8a60f-179">ツリーで、「model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list\Description: String」を展開します。</span><span class="sxs-lookup"><span data-stu-id="8a60f-179">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list\Description: String'.</span></span>
8. <span data-ttu-id="8a60f-180">[バインド] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8a60f-180">Click Bind.</span></span>
9. <span data-ttu-id="8a60f-181">ツリーで、「Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element\Value: XML Attribute」を選択します。</span><span class="sxs-lookup"><span data-stu-id="8a60f-181">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element\Value: XML Attribute'.</span></span>
10. <span data-ttu-id="8a60f-182">ツリーで、「model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record listt\Code: String」を選択します。</span><span class="sxs-lookup"><span data-stu-id="8a60f-182">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list\Code: String'.</span></span>
11. <span data-ttu-id="8a60f-183">[バインド] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8a60f-183">Click Bind.</span></span>
12. <span data-ttu-id="8a60f-184">ツリーで、「Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element\Code: XML Attribute」を選択します。</span><span class="sxs-lookup"><span data-stu-id="8a60f-184">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element\Code: XML Attribute'.</span></span>
13. <span data-ttu-id="8a60f-185">ツリーで、「model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list\Name: String」を選択します。</span><span class="sxs-lookup"><span data-stu-id="8a60f-185">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list\Name: String'.</span></span>
14. <span data-ttu-id="8a60f-186">[バインド] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8a60f-186">Click Bind.</span></span>
15. <span data-ttu-id="8a60f-187">ツリーで、「model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list」を展開します。</span><span class="sxs-lookup"><span data-stu-id="8a60f-187">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list'.</span></span>
16. <span data-ttu-id="8a60f-188">ツリーで、「Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element'」を選択します。</span><span class="sxs-lookup"><span data-stu-id="8a60f-188">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element'.</span></span>
17. <span data-ttu-id="8a60f-189">[バインド] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8a60f-189">Click Bind.</span></span>
18. <span data-ttu-id="8a60f-190">ツリーで、「Root: XML Element\Journal: XML Element\Transaction: XML Element\Ct: XML Attribute'」を選択します。</span><span class="sxs-lookup"><span data-stu-id="8a60f-190">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Ct: XML Attribute'.</span></span>
19. <span data-ttu-id="8a60f-191">ツリーで、「model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Credit: Real」を選択します。</span><span class="sxs-lookup"><span data-stu-id="8a60f-191">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Credit: Real'.</span></span>
20. <span data-ttu-id="8a60f-192">[バインド] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8a60f-192">Click Bind.</span></span>
21. <span data-ttu-id="8a60f-193">ツリーで、「Root: XML Element\Journal: XML Element\Transaction: XML Element\Dt: XML Attribute'」を選択します。</span><span class="sxs-lookup"><span data-stu-id="8a60f-193">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dt: XML Attribute'.</span></span>
22. <span data-ttu-id="8a60f-194">ツリーで、「model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Debit: Real」を選択します。</span><span class="sxs-lookup"><span data-stu-id="8a60f-194">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Debit: Real'.</span></span>
23. <span data-ttu-id="8a60f-195">[バインド] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8a60f-195">Click Bind.</span></span>
24. <span data-ttu-id="8a60f-196">ツリーで、「Root: XML Element\Journal: XML Element\Transaction: XML Element\Currency: XML Attribute'」を選択します。</span><span class="sxs-lookup"><span data-stu-id="8a60f-196">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Currency: XML Attribute'.</span></span>
25. <span data-ttu-id="8a60f-197">ツリーで、「model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Currency: String」を選択します。</span><span class="sxs-lookup"><span data-stu-id="8a60f-197">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Currency: String'.</span></span>
26. <span data-ttu-id="8a60f-198">[バインド] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8a60f-198">Click Bind.</span></span>
27. <span data-ttu-id="8a60f-199">ツリーで、「Root: XML Element\Journal: XML Element\Transaction: XML Element\Date: XML Attribute'」を選択します。</span><span class="sxs-lookup"><span data-stu-id="8a60f-199">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Date: XML Attribute'.</span></span>
28. <span data-ttu-id="8a60f-200">ツリーで、「model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Date: Date」を選択します。</span><span class="sxs-lookup"><span data-stu-id="8a60f-200">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Date: Date'.</span></span>
29. <span data-ttu-id="8a60f-201">[バインド] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8a60f-201">Click Bind.</span></span>
30. <span data-ttu-id="8a60f-202">ツリーで、「Root: XML Element\Journal: XML Element\Transaction: XML Element\Voucher: XML Attribute'」を選択します。</span><span class="sxs-lookup"><span data-stu-id="8a60f-202">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Voucher: XML Attribute'.</span></span>
31. <span data-ttu-id="8a60f-203">ツリーで、「model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Currency: String」を選択します。</span><span class="sxs-lookup"><span data-stu-id="8a60f-203">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Voucher: String'.</span></span>
32. <span data-ttu-id="8a60f-204">[バインド] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8a60f-204">Click Bind.</span></span>
33. <span data-ttu-id="8a60f-205">ツリーで、「Root: XML Element\Journal: XML Element\Transaction: XML Element」を選択します。</span><span class="sxs-lookup"><span data-stu-id="8a60f-205">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element'.</span></span>
34. <span data-ttu-id="8a60f-206">ツリーで、「model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list」を選択します。</span><span class="sxs-lookup"><span data-stu-id="8a60f-206">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list'.</span></span>
35. <span data-ttu-id="8a60f-207">[バインド] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8a60f-207">Click Bind.</span></span>
36. <span data-ttu-id="8a60f-208">ツリーで、「Root: XML Element\Journal: XML Element\Batch: XML Attribute」を選択します。</span><span class="sxs-lookup"><span data-stu-id="8a60f-208">In the tree, select 'Root: XML Element\Journal: XML Element\Batch: XML Attribute'.</span></span>
37. <span data-ttu-id="8a60f-209">ツリーで、「model: Data model Financial dimensions sample model\Journal: Record list\Batch: String」を選択します。</span><span class="sxs-lookup"><span data-stu-id="8a60f-209">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Batch: String'.</span></span>
38. <span data-ttu-id="8a60f-210">[バインド] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8a60f-210">Click Bind.</span></span>
39. <span data-ttu-id="8a60f-211">ツリーで、「Root: XML Element\Journal: XML Element」を選択します。</span><span class="sxs-lookup"><span data-stu-id="8a60f-211">In the tree, select 'Root: XML Element\Journal: XML Element'.</span></span>
40. <span data-ttu-id="8a60f-212">ツリーで、「model: Data model Financial dimensions sample model\Journal: Record list」を選択します。</span><span class="sxs-lookup"><span data-stu-id="8a60f-212">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list'.</span></span>
41. <span data-ttu-id="8a60f-213">[バインド] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8a60f-213">Click Bind.</span></span>
42. <span data-ttu-id="8a60f-214">ツリーで、「Root: XML Element\Company: XML Attribute」を選択します。</span><span class="sxs-lookup"><span data-stu-id="8a60f-214">In the tree, select 'Root: XML Element\Company: XML Attribute'.</span></span>
43. <span data-ttu-id="8a60f-215">ツリーで、「model: Data model Financial dimensions sample model\Company: String」を選択します。</span><span class="sxs-lookup"><span data-stu-id="8a60f-215">In the tree, select 'model: Data model Financial dimensions sample model\Company: String'.</span></span>
44. <span data-ttu-id="8a60f-216">[バインド] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8a60f-216">Click Bind.</span></span>
45. <span data-ttu-id="8a60f-217">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8a60f-217">Click Save.</span></span>
46. <span data-ttu-id="8a60f-218">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="8a60f-218">Close the page.</span></span>
<span data-ttu-id="8a60f-219">![ER Operations デザイナーのページ](../media/er-financial-dimensions-guides-format2.png)</span><span class="sxs-lookup"><span data-stu-id="8a60f-219">![ER Operations designer page](../media/er-financial-dimensions-guides-format2.png)</span></span>



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]