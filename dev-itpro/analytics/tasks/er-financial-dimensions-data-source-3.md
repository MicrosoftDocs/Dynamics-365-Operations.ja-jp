--- 
title: "電子申告 (ER) 用のデータ ソースとして財務分析コードを使用するためのレポートを設計する"
description: "次の手順では、システム管理者に指定されたユーザーまたは電子レポート開発者のロールが、電子レポート・データソースとしての財務分析コードを使用するために 電子レポート（ER）モデルをどのように環境設定しているのか説明します。"
author: NickSelin
manager: AnnBe
ms.date: 10/18/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 02787c96077e8bae54d8073e8d0770613ea2b49a
ms.contentlocale: ja-jp
ms.lasthandoff: 08/29/2017

---
# <a name="design-a-report-to-use-financial-dimensions-as-a-data-source-for-electronic-reporting-er"></a><span data-ttu-id="a20a3-103">電子申告 (ER) 用のデータ ソースとして財務分析コードを使用するためのレポートを設計する</span><span class="sxs-lookup"><span data-stu-id="a20a3-103">Design a report to use financial dimensions as a data source for electronic reporting (ER)</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="a20a3-104">次の手順では、システム管理者に指定されたユーザーまたは電子レポート開発者のロールが、電子レポート・データソースとしての財務分析コードを使用するために 電子レポート（ER）モデルをどのように環境設定しているのか説明します。</span><span class="sxs-lookup"><span data-stu-id="a20a3-104">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) model to use financial dimensions as a data source for ER reports.</span></span> <span data-ttu-id="a20a3-105">これらの手順はどのタイプの企業でも実施できます。</span><span class="sxs-lookup"><span data-stu-id="a20a3-105">These steps can be performed in any company.</span></span>

<span data-ttu-id="a20a3-106">これらの手順を実施するには、まず「データ ソース (パート2：モデルマッピング）手順としてのER使用・財務分析コード」にある手順を実施する必要があります。</span><span class="sxs-lookup"><span data-stu-id="a20a3-106">To complete these steps, you must first complete the steps in the “ER Use financial dimensions as a data source (Part 2: Model mapping)” procedure.</span></span>


## <a name="design-a-report-to-present-financial-dimensions"></a><span data-ttu-id="a20a3-107">財務分析コードを示すレポートを作成する</span><span class="sxs-lookup"><span data-stu-id="a20a3-107">Design a report to present financial dimensions</span></span>
1. <span data-ttu-id="a20a3-108">[組織管理] > [電子申告] > [コンフィギュレーション] に移動します。</span><span class="sxs-lookup"><span data-stu-id="a20a3-108">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="a20a3-109">[ツリー] フィールドで、「財務分析コード・サンプル モデル」を選択します。</span><span class="sxs-lookup"><span data-stu-id="a20a3-109">In the tree, select 'Financial dimensions sample model'.</span></span>
3. <span data-ttu-id="a20a3-110">[コンフィギュレーションの作成] をクリックすると、ドロップ ダイアログが開きます。</span><span class="sxs-lookup"><span data-stu-id="a20a3-110">Click Create configuration to open the drop dialog.</span></span>
4. <span data-ttu-id="a20a3-111">[新規] フィールドで、「財務分析コード・サンプルモデルに基づくフォーマット」を入力します。</span><span class="sxs-lookup"><span data-stu-id="a20a3-111">In the New field, enter 'Format based on data model Financial dimensions sample model'.</span></span>
    * <span data-ttu-id="a20a3-112">新しいレポートのデータ ソースとして事前に作成されたモデルを使用します。</span><span class="sxs-lookup"><span data-stu-id="a20a3-112">Use the model that was created in advance as the data source for your new report.</span></span>  
5. <span data-ttu-id="a20a3-113">[名称] フィールドで、「Ledger journal report」を入力します。</span><span class="sxs-lookup"><span data-stu-id="a20a3-113">In the Name field, type 'Ledger journal report'.</span></span>
6. <span data-ttu-id="a20a3-114">[データモデル定義] フィールドで、「エントリ」を選択します。</span><span class="sxs-lookup"><span data-stu-id="a20a3-114">In the Data model definition field, select Entry.</span></span>
7. <span data-ttu-id="a20a3-115">[コンフィギュレーションの作成] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a20a3-115">Click Create configuration.</span></span>
8. <span data-ttu-id="a20a3-116">[デザイナー] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a20a3-116">Click Designer.</span></span>
9. <span data-ttu-id="a20a3-117">[ルートの追加] をクリックして、ドロップ ダイアログを開きます。</span><span class="sxs-lookup"><span data-stu-id="a20a3-117">Click Add root to open the drop dialog.</span></span>
10. <span data-ttu-id="a20a3-118">ツリーで、[XML\Element] を選択します。</span><span class="sxs-lookup"><span data-stu-id="a20a3-118">In the tree, select 'XML\Element'.</span></span>
11. <span data-ttu-id="a20a3-119">[名称] のフィールドに、「Root」を入力します。</span><span class="sxs-lookup"><span data-stu-id="a20a3-119">In the Name field, type 'Root'.</span></span>
12. <span data-ttu-id="a20a3-120">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a20a3-120">Click OK.</span></span>
13. <span data-ttu-id="a20a3-121">[追加] をクリックしてドロップ ダイアログを開きます。</span><span class="sxs-lookup"><span data-stu-id="a20a3-121">Click Add to open the drop dialog.</span></span>
14. <span data-ttu-id="a20a3-122">ツリーで、[XML\Attribute] を選択します。</span><span class="sxs-lookup"><span data-stu-id="a20a3-122">In the tree, select 'XML\Attribute'.</span></span>
15. <span data-ttu-id="a20a3-123">[名前] フィールドに、「Company」と入力します。</span><span class="sxs-lookup"><span data-stu-id="a20a3-123">In the Name field, type 'Company'.</span></span>
16. <span data-ttu-id="a20a3-124">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a20a3-124">Click OK.</span></span>
17. <span data-ttu-id="a20a3-125">[追加] をクリックしてドロップ ダイアログを開きます。</span><span class="sxs-lookup"><span data-stu-id="a20a3-125">Click Add to open the drop dialog.</span></span>
18. <span data-ttu-id="a20a3-126">ツリーで、[XML\Element] を選択します。</span><span class="sxs-lookup"><span data-stu-id="a20a3-126">In the tree, select 'XML\Element'.</span></span>
19. <span data-ttu-id="a20a3-127">[名称] フィールドに、「仕訳」と入力します。</span><span class="sxs-lookup"><span data-stu-id="a20a3-127">In the Name field, type 'Journal'.</span></span>
20. <span data-ttu-id="a20a3-128">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a20a3-128">Click OK.</span></span>
21. <span data-ttu-id="a20a3-129">ツリーで、「Root: XML Element\Journal: XML Element」を選択します。</span><span class="sxs-lookup"><span data-stu-id="a20a3-129">In the tree, select 'Root: XML Element\Journal: XML Element'.</span></span>
22. <span data-ttu-id="a20a3-130">[追加] をクリックしてドロップ ダイアログを開きます。</span><span class="sxs-lookup"><span data-stu-id="a20a3-130">Click Add to open the drop dialog.</span></span>
23. <span data-ttu-id="a20a3-131">ツリーで、[XML\Attribute] を選択します。</span><span class="sxs-lookup"><span data-stu-id="a20a3-131">In the tree, select 'XML\Attribute'.</span></span>
24. <span data-ttu-id="a20a3-132">[名称] フィールドに、「バッチ」と入力します。</span><span class="sxs-lookup"><span data-stu-id="a20a3-132">In the Name field, type 'Batch'.</span></span>
25. <span data-ttu-id="a20a3-133">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a20a3-133">Click OK.</span></span>
26. <span data-ttu-id="a20a3-134">[追加] をクリックしてドロップ ダイアログを開きます。</span><span class="sxs-lookup"><span data-stu-id="a20a3-134">Click Add to open the drop dialog.</span></span>
27. <span data-ttu-id="a20a3-135">ツリーで、[XML\Element] を選択します。</span><span class="sxs-lookup"><span data-stu-id="a20a3-135">In the tree, select 'XML\Element'.</span></span>
28. <span data-ttu-id="a20a3-136">[名称] フィールドで、「トランザクション」と入力します。</span><span class="sxs-lookup"><span data-stu-id="a20a3-136">In the Name field, type 'Transaction'.</span></span>
29. <span data-ttu-id="a20a3-137">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a20a3-137">Click OK.</span></span>
30. <span data-ttu-id="a20a3-138">ツリーで、「Root: XML Element\Journal: XML Element\Transaction: XML Element」を選択します。</span><span class="sxs-lookup"><span data-stu-id="a20a3-138">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element'.</span></span>
31. <span data-ttu-id="a20a3-139">[追加] をクリックしてドロップ ダイアログを開きます。</span><span class="sxs-lookup"><span data-stu-id="a20a3-139">Click Add to open the drop dialog.</span></span>
32. <span data-ttu-id="a20a3-140">ツリーで、[XML\Attribute] を選択します。</span><span class="sxs-lookup"><span data-stu-id="a20a3-140">In the tree, select 'XML\Attribute'.</span></span>
33. <span data-ttu-id="a20a3-141">[名称] フィールドで、「伝票」と入力します。</span><span class="sxs-lookup"><span data-stu-id="a20a3-141">In the Name field, type 'Voucher'.</span></span>
34. <span data-ttu-id="a20a3-142">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a20a3-142">Click OK.</span></span>
35. <span data-ttu-id="a20a3-143">[属性を加える] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a20a3-143">Click Add Attribute.</span></span>
36. <span data-ttu-id="a20a3-144">[名称] フィールドで、「日付」と入力します。</span><span class="sxs-lookup"><span data-stu-id="a20a3-144">In the Name field, type 'Date'.</span></span>
37. <span data-ttu-id="a20a3-145">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a20a3-145">Click OK.</span></span>
38. <span data-ttu-id="a20a3-146">[属性を加える] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a20a3-146">Click Add Attribute.</span></span>
39. <span data-ttu-id="a20a3-147">[名前] フィールドで、「通貨」と入力します。</span><span class="sxs-lookup"><span data-stu-id="a20a3-147">In the Name field, type 'Currency'.</span></span>
40. <span data-ttu-id="a20a3-148">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a20a3-148">Click OK.</span></span>
41. <span data-ttu-id="a20a3-149">[属性を加える] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a20a3-149">Click Add Attribute.</span></span>
42. <span data-ttu-id="a20a3-150">[名称] フィールドに、「Dt」と入力します。</span><span class="sxs-lookup"><span data-stu-id="a20a3-150">In the Name field, type 'Dt'.</span></span>
43. <span data-ttu-id="a20a3-151">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a20a3-151">Click OK.</span></span>
44. <span data-ttu-id="a20a3-152">[属性を加える] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a20a3-152">Click Add Attribute.</span></span>
45. <span data-ttu-id="a20a3-153">[名称] フィールドに、「Ct」と入力します。</span><span class="sxs-lookup"><span data-stu-id="a20a3-153">In the Name field, type 'Ct'.</span></span>
46. <span data-ttu-id="a20a3-154">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a20a3-154">Click OK.</span></span>
47. <span data-ttu-id="a20a3-155">[追加] をクリックしてドロップ ダイアログを開きます。</span><span class="sxs-lookup"><span data-stu-id="a20a3-155">Click Add to open the drop dialog.</span></span>
48. <span data-ttu-id="a20a3-156">ツリーで、[XML\Element] を選択します。</span><span class="sxs-lookup"><span data-stu-id="a20a3-156">In the tree, select 'XML\Element'.</span></span>
49. <span data-ttu-id="a20a3-157">[名称] フィールドに、「分析コード」を入力します。</span><span class="sxs-lookup"><span data-stu-id="a20a3-157">In the Name field, type 'Dimensions'.</span></span>
50. <span data-ttu-id="a20a3-158">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a20a3-158">Click OK.</span></span>
51. <span data-ttu-id="a20a3-159">ツリーで、「Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element'」を選択します。</span><span class="sxs-lookup"><span data-stu-id="a20a3-159">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element'.</span></span>
52. <span data-ttu-id="a20a3-160">[追加] をクリックしてドロップ ダイアログを開きます。</span><span class="sxs-lookup"><span data-stu-id="a20a3-160">Click Add to open the drop dialog.</span></span>
53. <span data-ttu-id="a20a3-161">ツリーで、[XML\Attribute] を選択します。</span><span class="sxs-lookup"><span data-stu-id="a20a3-161">In the tree, select 'XML\Attribute'.</span></span>
54. <span data-ttu-id="a20a3-162">[名称] フィールドに、「コード」と入力します。</span><span class="sxs-lookup"><span data-stu-id="a20a3-162">In the Name field, type 'Code'.</span></span>
55. <span data-ttu-id="a20a3-163">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a20a3-163">Click OK.</span></span>
56. <span data-ttu-id="a20a3-164">[属性を加える] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a20a3-164">Click Add Attribute.</span></span>
57. <span data-ttu-id="a20a3-165">[名称] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="a20a3-165">In the Name field, type 'Value'.</span></span>
58. <span data-ttu-id="a20a3-166">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a20a3-166">Click OK.</span></span>
59. <span data-ttu-id="a20a3-167">[属性を加える] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a20a3-167">Click Add Attribute.</span></span>
60. <span data-ttu-id="a20a3-168">[名称] フィールドに説明を入力します。</span><span class="sxs-lookup"><span data-stu-id="a20a3-168">In the Name field, type 'Desc'.</span></span>
61. <span data-ttu-id="a20a3-169">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a20a3-169">Click OK.</span></span>

## <a name="map-report-elements-to-data-sources"></a><span data-ttu-id="a20a3-170">レポートエレメントをデータソースにマッピングする</span><span class="sxs-lookup"><span data-stu-id="a20a3-170">Map report elements to data sources</span></span>
1. <span data-ttu-id="a20a3-171">[マッピング] タブをクリックします。</span><span class="sxs-lookup"><span data-stu-id="a20a3-171">Click the Mapping tab.</span></span>
2. <span data-ttu-id="a20a3-172">ツリーで、「model: Data model Financial dimensions sample model」を展開します。</span><span class="sxs-lookup"><span data-stu-id="a20a3-172">In the tree, expand 'model: Data model Financial dimensions sample model'.</span></span>
3. <span data-ttu-id="a20a3-173">ツリーで、「model: Data model Financial dimensions sample model\Journal: Record list」を展開します。</span><span class="sxs-lookup"><span data-stu-id="a20a3-173">In the tree, expand 'model: Data model Financial dimensions sample model\Journal: Record list'.</span></span>
4. <span data-ttu-id="a20a3-174">ツリーで、「model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list」を展開します。</span><span class="sxs-lookup"><span data-stu-id="a20a3-174">In the tree, expand 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list'.</span></span>
5. <span data-ttu-id="a20a3-175">ツリーで、「model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list」を展開します。</span><span class="sxs-lookup"><span data-stu-id="a20a3-175">In the tree, expand 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list'.</span></span>
6. <span data-ttu-id="a20a3-176">ツリーで、「Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element\Desc: XML Attribute」を選択します。</span><span class="sxs-lookup"><span data-stu-id="a20a3-176">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element\Desc: XML Attribute'.</span></span>
7. <span data-ttu-id="a20a3-177">ツリーで、「model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list\Description: String」を展開します。</span><span class="sxs-lookup"><span data-stu-id="a20a3-177">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list\Description: String'.</span></span>
8. <span data-ttu-id="a20a3-178">[バインド] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a20a3-178">Click Bind.</span></span>
9. <span data-ttu-id="a20a3-179">ツリーで、「Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element\Value: XML Attribute」を選択します。</span><span class="sxs-lookup"><span data-stu-id="a20a3-179">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element\Value: XML Attribute'.</span></span>
10. <span data-ttu-id="a20a3-180">ツリーで、「model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record listt\Code: String」を選択します。</span><span class="sxs-lookup"><span data-stu-id="a20a3-180">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list\Code: String'.</span></span>
11. <span data-ttu-id="a20a3-181">[バインド] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a20a3-181">Click Bind.</span></span>
12. <span data-ttu-id="a20a3-182">ツリーで、「Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element\Code: XML Attribute」を選択します。</span><span class="sxs-lookup"><span data-stu-id="a20a3-182">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element\Code: XML Attribute'.</span></span>
13. <span data-ttu-id="a20a3-183">ツリーで、「model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list\Name: String」を選択します。</span><span class="sxs-lookup"><span data-stu-id="a20a3-183">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list\Name: String'.</span></span>
14. <span data-ttu-id="a20a3-184">[バインド] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a20a3-184">Click Bind.</span></span>
15. <span data-ttu-id="a20a3-185">ツリーで、「model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list」を展開します。</span><span class="sxs-lookup"><span data-stu-id="a20a3-185">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list'.</span></span>
16. <span data-ttu-id="a20a3-186">ツリーで、「Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element'」を選択します。</span><span class="sxs-lookup"><span data-stu-id="a20a3-186">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element'.</span></span>
17. <span data-ttu-id="a20a3-187">[バインド] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a20a3-187">Click Bind.</span></span>
18. <span data-ttu-id="a20a3-188">ツリーで、「Root: XML Element\Journal: XML Element\Transaction: XML Element\Ct: XML Attribute'」を選択します。</span><span class="sxs-lookup"><span data-stu-id="a20a3-188">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Ct: XML Attribute'.</span></span>
19. <span data-ttu-id="a20a3-189">ツリーで、「model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Credit: Real」を選択します。</span><span class="sxs-lookup"><span data-stu-id="a20a3-189">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Credit: Real'.</span></span>
20. <span data-ttu-id="a20a3-190">[バインド] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a20a3-190">Click Bind.</span></span>
21. <span data-ttu-id="a20a3-191">ツリーで、「Root: XML Element\Journal: XML Element\Transaction: XML Element\Dt: XML Attribute'」を選択します。</span><span class="sxs-lookup"><span data-stu-id="a20a3-191">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dt: XML Attribute'.</span></span>
22. <span data-ttu-id="a20a3-192">ツリーで、「model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Debit: Real」を選択します。</span><span class="sxs-lookup"><span data-stu-id="a20a3-192">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Debit: Real'.</span></span>
23. <span data-ttu-id="a20a3-193">[バインド] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a20a3-193">Click Bind.</span></span>
24. <span data-ttu-id="a20a3-194">ツリーで、「Root: XML Element\Journal: XML Element\Transaction: XML Element\Currency: XML Attribute'」を選択します。</span><span class="sxs-lookup"><span data-stu-id="a20a3-194">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Currency: XML Attribute'.</span></span>
25. <span data-ttu-id="a20a3-195">ツリーで、「model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Currency: String」を選択します。</span><span class="sxs-lookup"><span data-stu-id="a20a3-195">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Currency: String'.</span></span>
26. <span data-ttu-id="a20a3-196">[バインド] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a20a3-196">Click Bind.</span></span>
27. <span data-ttu-id="a20a3-197">ツリーで、「Root: XML Element\Journal: XML Element\Transaction: XML Element\Date: XML Attribute'」を選択します。</span><span class="sxs-lookup"><span data-stu-id="a20a3-197">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Date: XML Attribute'.</span></span>
28. <span data-ttu-id="a20a3-198">ツリーで、「model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Date: Date」を選択します。</span><span class="sxs-lookup"><span data-stu-id="a20a3-198">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Date: Date'.</span></span>
29. <span data-ttu-id="a20a3-199">[バインド] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a20a3-199">Click Bind.</span></span>
30. <span data-ttu-id="a20a3-200">ツリーで、「Root: XML Element\Journal: XML Element\Transaction: XML Element\Voucher: XML Attribute'」を選択します。</span><span class="sxs-lookup"><span data-stu-id="a20a3-200">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Voucher: XML Attribute'.</span></span>
31. <span data-ttu-id="a20a3-201">ツリーで、「model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Currency: String」を選択します。</span><span class="sxs-lookup"><span data-stu-id="a20a3-201">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Voucher: String'.</span></span>
32. <span data-ttu-id="a20a3-202">[バインド] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a20a3-202">Click Bind.</span></span>
33. <span data-ttu-id="a20a3-203">ツリーで、「Root: XML Element\Journal: XML Element\Transaction: XML Element」を選択します。</span><span class="sxs-lookup"><span data-stu-id="a20a3-203">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element'.</span></span>
34. <span data-ttu-id="a20a3-204">ツリーで、「model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list」を選択します。</span><span class="sxs-lookup"><span data-stu-id="a20a3-204">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list'.</span></span>
35. <span data-ttu-id="a20a3-205">[バインド] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a20a3-205">Click Bind.</span></span>
36. <span data-ttu-id="a20a3-206">ツリーで、「Root: XML Element\Journal: XML Element\Batch: XML Attribute」を選択します。</span><span class="sxs-lookup"><span data-stu-id="a20a3-206">In the tree, select 'Root: XML Element\Journal: XML Element\Batch: XML Attribute'.</span></span>
37. <span data-ttu-id="a20a3-207">ツリーで、「model: Data model Financial dimensions sample model\Journal: Record list\Batch: String」を選択します。</span><span class="sxs-lookup"><span data-stu-id="a20a3-207">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Batch: String'.</span></span>
38. <span data-ttu-id="a20a3-208">[バインド] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a20a3-208">Click Bind.</span></span>
39. <span data-ttu-id="a20a3-209">ツリーで、「Root: XML Element\Journal: XML Element」を選択します。</span><span class="sxs-lookup"><span data-stu-id="a20a3-209">In the tree, select 'Root: XML Element\Journal: XML Element'.</span></span>
40. <span data-ttu-id="a20a3-210">ツリーで、「model: Data model Financial dimensions sample model\Journal: Record list」を選択します。</span><span class="sxs-lookup"><span data-stu-id="a20a3-210">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list'.</span></span>
41. <span data-ttu-id="a20a3-211">[バインド] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a20a3-211">Click Bind.</span></span>
42. <span data-ttu-id="a20a3-212">ツリーで、「Root: XML Element\Company: XML Attribute」を選択します。</span><span class="sxs-lookup"><span data-stu-id="a20a3-212">In the tree, select 'Root: XML Element\Company: XML Attribute'.</span></span>
43. <span data-ttu-id="a20a3-213">ツリーで、「model: Data model Financial dimensions sample model\Company: String」を選択します。</span><span class="sxs-lookup"><span data-stu-id="a20a3-213">In the tree, select 'model: Data model Financial dimensions sample model\Company: String'.</span></span>
44. <span data-ttu-id="a20a3-214">[バインド] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a20a3-214">Click Bind.</span></span>
45. <span data-ttu-id="a20a3-215">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="a20a3-215">Click Save.</span></span>
46. <span data-ttu-id="a20a3-216">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="a20a3-216">Close the page.</span></span>


