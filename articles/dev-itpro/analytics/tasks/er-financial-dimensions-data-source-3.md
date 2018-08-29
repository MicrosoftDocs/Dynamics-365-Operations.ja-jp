--- 
title: "データ ソースとして財務分析コードを使用するためのレポートのデザイン"
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
ms.sourcegitcommit: e782d33f3748524491dace28008cd9148ae70529
ms.openlocfilehash: 055401104ae62c75694dff0b2ee64d12b2621686
ms.contentlocale: ja-jp
ms.lasthandoff: 08/09/2018

---
# <a name="design-reports-to-use-financial-dimensions-as-data-sources"></a><span data-ttu-id="0f1a4-103">データ ソースとして財務分析コードを使用するためのレポートのデザイン</span><span class="sxs-lookup"><span data-stu-id="0f1a4-103">Design reports to use financial dimensions as data sources</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="0f1a4-104">次の手順では、システム管理者に指定されたユーザーまたは電子レポート開発者のロールが、電子レポート・データソースとしての財務分析コードを使用するために 電子レポート（ER）モデルをどのように環境設定しているのか説明します。</span><span class="sxs-lookup"><span data-stu-id="0f1a4-104">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) model to use financial dimensions as a data source for ER reports.</span></span> <span data-ttu-id="0f1a4-105">これらの手順はどのタイプの企業でも実施できます。</span><span class="sxs-lookup"><span data-stu-id="0f1a4-105">These steps can be performed in any company.</span></span>

<span data-ttu-id="0f1a4-106">これらの手順を実施するには、まず「データ ソース (パート2：モデルマッピング）手順としてのER使用・財務分析コード」にある手順を実施する必要があります。</span><span class="sxs-lookup"><span data-stu-id="0f1a4-106">To complete these steps, you must first complete the steps in the “ER Use financial dimensions as a data source (Part 2: Model mapping)” procedure.</span></span>


## <a name="design-a-report-to-present-financial-dimensions"></a><span data-ttu-id="0f1a4-107">財務分析コードを示すレポートを作成する</span><span class="sxs-lookup"><span data-stu-id="0f1a4-107">Design a report to present financial dimensions</span></span>
1. <span data-ttu-id="0f1a4-108">[組織管理] > [電子申告] > [コンフィギュレーション] に移動します。</span><span class="sxs-lookup"><span data-stu-id="0f1a4-108">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="0f1a4-109">[ツリー] フィールドで、「財務分析コード・サンプル モデル」を選択します。</span><span class="sxs-lookup"><span data-stu-id="0f1a4-109">In the tree, select 'Financial dimensions sample model'.</span></span>
3. <span data-ttu-id="0f1a4-110">[コンフィギュレーションの作成] をクリックすると、ドロップ ダイアログが開きます。</span><span class="sxs-lookup"><span data-stu-id="0f1a4-110">Click Create configuration to open the drop dialog.</span></span>
4. <span data-ttu-id="0f1a4-111">[新規] フィールドで、「財務分析コード・サンプルモデルに基づくフォーマット」を入力します。</span><span class="sxs-lookup"><span data-stu-id="0f1a4-111">In the New field, enter 'Format based on data model Financial dimensions sample model'.</span></span>
    * <span data-ttu-id="0f1a4-112">新しいレポートのデータ ソースとして事前に作成されたモデルを使用します。</span><span class="sxs-lookup"><span data-stu-id="0f1a4-112">Use the model that was created in advance as the data source for your new report.</span></span>  
5. <span data-ttu-id="0f1a4-113">[名称] フィールドで、「Ledger journal report」を入力します。</span><span class="sxs-lookup"><span data-stu-id="0f1a4-113">In the Name field, type 'Ledger journal report'.</span></span>
6. <span data-ttu-id="0f1a4-114">[データモデル定義] フィールドで、「エントリ」を選択します。</span><span class="sxs-lookup"><span data-stu-id="0f1a4-114">In the Data model definition field, select Entry.</span></span>
7. <span data-ttu-id="0f1a4-115">[コンフィギュレーションの作成] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="0f1a4-115">Click Create configuration.</span></span>
8. <span data-ttu-id="0f1a4-116">[デザイナー] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="0f1a4-116">Click Designer.</span></span>
9. <span data-ttu-id="0f1a4-117">[ルートの追加] をクリックして、ドロップ ダイアログを開きます。</span><span class="sxs-lookup"><span data-stu-id="0f1a4-117">Click Add root to open the drop dialog.</span></span>
10. <span data-ttu-id="0f1a4-118">ツリーで、[XML\Element] を選択します。</span><span class="sxs-lookup"><span data-stu-id="0f1a4-118">In the tree, select 'XML\Element'.</span></span>
11. <span data-ttu-id="0f1a4-119">[名称] のフィールドに、「Root」を入力します。</span><span class="sxs-lookup"><span data-stu-id="0f1a4-119">In the Name field, type 'Root'.</span></span>
12. <span data-ttu-id="0f1a4-120">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="0f1a4-120">Click OK.</span></span>
13. <span data-ttu-id="0f1a4-121">[追加] をクリックしてドロップ ダイアログを開きます。</span><span class="sxs-lookup"><span data-stu-id="0f1a4-121">Click Add to open the drop dialog.</span></span>
14. <span data-ttu-id="0f1a4-122">ツリーで、[XML\Attribute] を選択します。</span><span class="sxs-lookup"><span data-stu-id="0f1a4-122">In the tree, select 'XML\Attribute'.</span></span>
15. <span data-ttu-id="0f1a4-123">[名前] フィールドに、「Company」と入力します。</span><span class="sxs-lookup"><span data-stu-id="0f1a4-123">In the Name field, type 'Company'.</span></span>
16. <span data-ttu-id="0f1a4-124">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="0f1a4-124">Click OK.</span></span>
17. <span data-ttu-id="0f1a4-125">[追加] をクリックしてドロップ ダイアログを開きます。</span><span class="sxs-lookup"><span data-stu-id="0f1a4-125">Click Add to open the drop dialog.</span></span>
18. <span data-ttu-id="0f1a4-126">ツリーで、[XML\Element] を選択します。</span><span class="sxs-lookup"><span data-stu-id="0f1a4-126">In the tree, select 'XML\Element'.</span></span>
19. <span data-ttu-id="0f1a4-127">[名称] フィールドに、「仕訳」と入力します。</span><span class="sxs-lookup"><span data-stu-id="0f1a4-127">In the Name field, type 'Journal'.</span></span>
20. <span data-ttu-id="0f1a4-128">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="0f1a4-128">Click OK.</span></span>
21. <span data-ttu-id="0f1a4-129">ツリーで、「Root: XML Element\Journal: XML Element」を選択します。</span><span class="sxs-lookup"><span data-stu-id="0f1a4-129">In the tree, select 'Root: XML Element\Journal: XML Element'.</span></span>
22. <span data-ttu-id="0f1a4-130">[追加] をクリックしてドロップ ダイアログを開きます。</span><span class="sxs-lookup"><span data-stu-id="0f1a4-130">Click Add to open the drop dialog.</span></span>
23. <span data-ttu-id="0f1a4-131">ツリーで、[XML\Attribute] を選択します。</span><span class="sxs-lookup"><span data-stu-id="0f1a4-131">In the tree, select 'XML\Attribute'.</span></span>
24. <span data-ttu-id="0f1a4-132">[名称] フィールドに、「バッチ」と入力します。</span><span class="sxs-lookup"><span data-stu-id="0f1a4-132">In the Name field, type 'Batch'.</span></span>
25. <span data-ttu-id="0f1a4-133">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="0f1a4-133">Click OK.</span></span>
26. <span data-ttu-id="0f1a4-134">[追加] をクリックしてドロップ ダイアログを開きます。</span><span class="sxs-lookup"><span data-stu-id="0f1a4-134">Click Add to open the drop dialog.</span></span>
27. <span data-ttu-id="0f1a4-135">ツリーで、[XML\Element] を選択します。</span><span class="sxs-lookup"><span data-stu-id="0f1a4-135">In the tree, select 'XML\Element'.</span></span>
28. <span data-ttu-id="0f1a4-136">[名称] フィールドで、「トランザクション」と入力します。</span><span class="sxs-lookup"><span data-stu-id="0f1a4-136">In the Name field, type 'Transaction'.</span></span>
29. <span data-ttu-id="0f1a4-137">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="0f1a4-137">Click OK.</span></span>
30. <span data-ttu-id="0f1a4-138">ツリーで、「Root: XML Element\Journal: XML Element\Transaction: XML Element」を選択します。</span><span class="sxs-lookup"><span data-stu-id="0f1a4-138">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element'.</span></span>
31. <span data-ttu-id="0f1a4-139">[追加] をクリックしてドロップ ダイアログを開きます。</span><span class="sxs-lookup"><span data-stu-id="0f1a4-139">Click Add to open the drop dialog.</span></span>
32. <span data-ttu-id="0f1a4-140">ツリーで、[XML\Attribute] を選択します。</span><span class="sxs-lookup"><span data-stu-id="0f1a4-140">In the tree, select 'XML\Attribute'.</span></span>
33. <span data-ttu-id="0f1a4-141">[名称] フィールドで、「伝票」と入力します。</span><span class="sxs-lookup"><span data-stu-id="0f1a4-141">In the Name field, type 'Voucher'.</span></span>
34. <span data-ttu-id="0f1a4-142">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="0f1a4-142">Click OK.</span></span>
35. <span data-ttu-id="0f1a4-143">[属性を加える] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="0f1a4-143">Click Add Attribute.</span></span>
36. <span data-ttu-id="0f1a4-144">[名称] フィールドで、「日付」と入力します。</span><span class="sxs-lookup"><span data-stu-id="0f1a4-144">In the Name field, type 'Date'.</span></span>
37. <span data-ttu-id="0f1a4-145">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="0f1a4-145">Click OK.</span></span>
38. <span data-ttu-id="0f1a4-146">[属性を加える] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="0f1a4-146">Click Add Attribute.</span></span>
39. <span data-ttu-id="0f1a4-147">[名前] フィールドで、「通貨」と入力します。</span><span class="sxs-lookup"><span data-stu-id="0f1a4-147">In the Name field, type 'Currency'.</span></span>
40. <span data-ttu-id="0f1a4-148">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="0f1a4-148">Click OK.</span></span>
41. <span data-ttu-id="0f1a4-149">[属性を加える] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="0f1a4-149">Click Add Attribute.</span></span>
42. <span data-ttu-id="0f1a4-150">[名称] フィールドに、「Dt」と入力します。</span><span class="sxs-lookup"><span data-stu-id="0f1a4-150">In the Name field, type 'Dt'.</span></span>
43. <span data-ttu-id="0f1a4-151">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="0f1a4-151">Click OK.</span></span>
44. <span data-ttu-id="0f1a4-152">[属性を加える] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="0f1a4-152">Click Add Attribute.</span></span>
45. <span data-ttu-id="0f1a4-153">[名称] フィールドに、「Ct」と入力します。</span><span class="sxs-lookup"><span data-stu-id="0f1a4-153">In the Name field, type 'Ct'.</span></span>
46. <span data-ttu-id="0f1a4-154">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="0f1a4-154">Click OK.</span></span>
47. <span data-ttu-id="0f1a4-155">[追加] をクリックしてドロップ ダイアログを開きます。</span><span class="sxs-lookup"><span data-stu-id="0f1a4-155">Click Add to open the drop dialog.</span></span>
48. <span data-ttu-id="0f1a4-156">ツリーで、[XML\Element] を選択します。</span><span class="sxs-lookup"><span data-stu-id="0f1a4-156">In the tree, select 'XML\Element'.</span></span>
49. <span data-ttu-id="0f1a4-157">[名称] フィールドに、「分析コード」を入力します。</span><span class="sxs-lookup"><span data-stu-id="0f1a4-157">In the Name field, type 'Dimensions'.</span></span>
50. <span data-ttu-id="0f1a4-158">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="0f1a4-158">Click OK.</span></span>
51. <span data-ttu-id="0f1a4-159">ツリーで、「Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element'」を選択します。</span><span class="sxs-lookup"><span data-stu-id="0f1a4-159">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element'.</span></span>
52. <span data-ttu-id="0f1a4-160">[追加] をクリックしてドロップ ダイアログを開きます。</span><span class="sxs-lookup"><span data-stu-id="0f1a4-160">Click Add to open the drop dialog.</span></span>
53. <span data-ttu-id="0f1a4-161">ツリーで、[XML\Attribute] を選択します。</span><span class="sxs-lookup"><span data-stu-id="0f1a4-161">In the tree, select 'XML\Attribute'.</span></span>
54. <span data-ttu-id="0f1a4-162">[名称] フィールドに、「コード」と入力します。</span><span class="sxs-lookup"><span data-stu-id="0f1a4-162">In the Name field, type 'Code'.</span></span>
55. <span data-ttu-id="0f1a4-163">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="0f1a4-163">Click OK.</span></span>
56. <span data-ttu-id="0f1a4-164">[属性を加える] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="0f1a4-164">Click Add Attribute.</span></span>
57. <span data-ttu-id="0f1a4-165">[名称] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="0f1a4-165">In the Name field, type 'Value'.</span></span>
58. <span data-ttu-id="0f1a4-166">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="0f1a4-166">Click OK.</span></span>
59. <span data-ttu-id="0f1a4-167">[属性を加える] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="0f1a4-167">Click Add Attribute.</span></span>
60. <span data-ttu-id="0f1a4-168">[名称] フィールドに説明を入力します。</span><span class="sxs-lookup"><span data-stu-id="0f1a4-168">In the Name field, type 'Desc'.</span></span>
61. <span data-ttu-id="0f1a4-169">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="0f1a4-169">Click OK.</span></span>

## <a name="map-report-elements-to-data-sources"></a><span data-ttu-id="0f1a4-170">レポートエレメントをデータソースにマッピングする</span><span class="sxs-lookup"><span data-stu-id="0f1a4-170">Map report elements to data sources</span></span>
1. <span data-ttu-id="0f1a4-171">[マッピング] タブをクリックします。</span><span class="sxs-lookup"><span data-stu-id="0f1a4-171">Click the Mapping tab.</span></span>
2. <span data-ttu-id="0f1a4-172">ツリーで、「model: Data model Financial dimensions sample model」を展開します。</span><span class="sxs-lookup"><span data-stu-id="0f1a4-172">In the tree, expand 'model: Data model Financial dimensions sample model'.</span></span>
3. <span data-ttu-id="0f1a4-173">ツリーで、「model: Data model Financial dimensions sample model\Journal: Record list」を展開します。</span><span class="sxs-lookup"><span data-stu-id="0f1a4-173">In the tree, expand 'model: Data model Financial dimensions sample model\Journal: Record list'.</span></span>
4. <span data-ttu-id="0f1a4-174">ツリーで、「model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list」を展開します。</span><span class="sxs-lookup"><span data-stu-id="0f1a4-174">In the tree, expand 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list'.</span></span>
5. <span data-ttu-id="0f1a4-175">ツリーで、「model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list」を展開します。</span><span class="sxs-lookup"><span data-stu-id="0f1a4-175">In the tree, expand 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list'.</span></span>
6. <span data-ttu-id="0f1a4-176">ツリーで、「Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element\Desc: XML Attribute」を選択します。</span><span class="sxs-lookup"><span data-stu-id="0f1a4-176">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element\Desc: XML Attribute'.</span></span>
7. <span data-ttu-id="0f1a4-177">ツリーで、「model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list\Description: String」を展開します。</span><span class="sxs-lookup"><span data-stu-id="0f1a4-177">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list\Description: String'.</span></span>
8. <span data-ttu-id="0f1a4-178">[バインド] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="0f1a4-178">Click Bind.</span></span>
9. <span data-ttu-id="0f1a4-179">ツリーで、「Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element\Value: XML Attribute」を選択します。</span><span class="sxs-lookup"><span data-stu-id="0f1a4-179">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element\Value: XML Attribute'.</span></span>
10. <span data-ttu-id="0f1a4-180">ツリーで、「model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record listt\Code: String」を選択します。</span><span class="sxs-lookup"><span data-stu-id="0f1a4-180">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list\Code: String'.</span></span>
11. <span data-ttu-id="0f1a4-181">[バインド] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="0f1a4-181">Click Bind.</span></span>
12. <span data-ttu-id="0f1a4-182">ツリーで、「Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element\Code: XML Attribute」を選択します。</span><span class="sxs-lookup"><span data-stu-id="0f1a4-182">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element\Code: XML Attribute'.</span></span>
13. <span data-ttu-id="0f1a4-183">ツリーで、「model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list\Name: String」を選択します。</span><span class="sxs-lookup"><span data-stu-id="0f1a4-183">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list\Name: String'.</span></span>
14. <span data-ttu-id="0f1a4-184">[バインド] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="0f1a4-184">Click Bind.</span></span>
15. <span data-ttu-id="0f1a4-185">ツリーで、「model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list」を展開します。</span><span class="sxs-lookup"><span data-stu-id="0f1a4-185">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Dimensions data: Record list'.</span></span>
16. <span data-ttu-id="0f1a4-186">ツリーで、「Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element'」を選択します。</span><span class="sxs-lookup"><span data-stu-id="0f1a4-186">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dimensions: XML Element'.</span></span>
17. <span data-ttu-id="0f1a4-187">[バインド] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="0f1a4-187">Click Bind.</span></span>
18. <span data-ttu-id="0f1a4-188">ツリーで、「Root: XML Element\Journal: XML Element\Transaction: XML Element\Ct: XML Attribute'」を選択します。</span><span class="sxs-lookup"><span data-stu-id="0f1a4-188">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Ct: XML Attribute'.</span></span>
19. <span data-ttu-id="0f1a4-189">ツリーで、「model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Credit: Real」を選択します。</span><span class="sxs-lookup"><span data-stu-id="0f1a4-189">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Credit: Real'.</span></span>
20. <span data-ttu-id="0f1a4-190">[バインド] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="0f1a4-190">Click Bind.</span></span>
21. <span data-ttu-id="0f1a4-191">ツリーで、「Root: XML Element\Journal: XML Element\Transaction: XML Element\Dt: XML Attribute'」を選択します。</span><span class="sxs-lookup"><span data-stu-id="0f1a4-191">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Dt: XML Attribute'.</span></span>
22. <span data-ttu-id="0f1a4-192">ツリーで、「model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Debit: Real」を選択します。</span><span class="sxs-lookup"><span data-stu-id="0f1a4-192">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Debit: Real'.</span></span>
23. <span data-ttu-id="0f1a4-193">[バインド] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="0f1a4-193">Click Bind.</span></span>
24. <span data-ttu-id="0f1a4-194">ツリーで、「Root: XML Element\Journal: XML Element\Transaction: XML Element\Currency: XML Attribute'」を選択します。</span><span class="sxs-lookup"><span data-stu-id="0f1a4-194">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Currency: XML Attribute'.</span></span>
25. <span data-ttu-id="0f1a4-195">ツリーで、「model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Currency: String」を選択します。</span><span class="sxs-lookup"><span data-stu-id="0f1a4-195">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Currency: String'.</span></span>
26. <span data-ttu-id="0f1a4-196">[バインド] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="0f1a4-196">Click Bind.</span></span>
27. <span data-ttu-id="0f1a4-197">ツリーで、「Root: XML Element\Journal: XML Element\Transaction: XML Element\Date: XML Attribute'」を選択します。</span><span class="sxs-lookup"><span data-stu-id="0f1a4-197">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Date: XML Attribute'.</span></span>
28. <span data-ttu-id="0f1a4-198">ツリーで、「model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Date: Date」を選択します。</span><span class="sxs-lookup"><span data-stu-id="0f1a4-198">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Date: Date'.</span></span>
29. <span data-ttu-id="0f1a4-199">[バインド] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="0f1a4-199">Click Bind.</span></span>
30. <span data-ttu-id="0f1a4-200">ツリーで、「Root: XML Element\Journal: XML Element\Transaction: XML Element\Voucher: XML Attribute'」を選択します。</span><span class="sxs-lookup"><span data-stu-id="0f1a4-200">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element\Voucher: XML Attribute'.</span></span>
31. <span data-ttu-id="0f1a4-201">ツリーで、「model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Currency: String」を選択します。</span><span class="sxs-lookup"><span data-stu-id="0f1a4-201">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list\Voucher: String'.</span></span>
32. <span data-ttu-id="0f1a4-202">[バインド] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="0f1a4-202">Click Bind.</span></span>
33. <span data-ttu-id="0f1a4-203">ツリーで、「Root: XML Element\Journal: XML Element\Transaction: XML Element」を選択します。</span><span class="sxs-lookup"><span data-stu-id="0f1a4-203">In the tree, select 'Root: XML Element\Journal: XML Element\Transaction: XML Element'.</span></span>
34. <span data-ttu-id="0f1a4-204">ツリーで、「model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list」を選択します。</span><span class="sxs-lookup"><span data-stu-id="0f1a4-204">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Transaction: Record list'.</span></span>
35. <span data-ttu-id="0f1a4-205">[バインド] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="0f1a4-205">Click Bind.</span></span>
36. <span data-ttu-id="0f1a4-206">ツリーで、「Root: XML Element\Journal: XML Element\Batch: XML Attribute」を選択します。</span><span class="sxs-lookup"><span data-stu-id="0f1a4-206">In the tree, select 'Root: XML Element\Journal: XML Element\Batch: XML Attribute'.</span></span>
37. <span data-ttu-id="0f1a4-207">ツリーで、「model: Data model Financial dimensions sample model\Journal: Record list\Batch: String」を選択します。</span><span class="sxs-lookup"><span data-stu-id="0f1a4-207">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list\Batch: String'.</span></span>
38. <span data-ttu-id="0f1a4-208">[バインド] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="0f1a4-208">Click Bind.</span></span>
39. <span data-ttu-id="0f1a4-209">ツリーで、「Root: XML Element\Journal: XML Element」を選択します。</span><span class="sxs-lookup"><span data-stu-id="0f1a4-209">In the tree, select 'Root: XML Element\Journal: XML Element'.</span></span>
40. <span data-ttu-id="0f1a4-210">ツリーで、「model: Data model Financial dimensions sample model\Journal: Record list」を選択します。</span><span class="sxs-lookup"><span data-stu-id="0f1a4-210">In the tree, select 'model: Data model Financial dimensions sample model\Journal: Record list'.</span></span>
41. <span data-ttu-id="0f1a4-211">[バインド] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="0f1a4-211">Click Bind.</span></span>
42. <span data-ttu-id="0f1a4-212">ツリーで、「Root: XML Element\Company: XML Attribute」を選択します。</span><span class="sxs-lookup"><span data-stu-id="0f1a4-212">In the tree, select 'Root: XML Element\Company: XML Attribute'.</span></span>
43. <span data-ttu-id="0f1a4-213">ツリーで、「model: Data model Financial dimensions sample model\Company: String」を選択します。</span><span class="sxs-lookup"><span data-stu-id="0f1a4-213">In the tree, select 'model: Data model Financial dimensions sample model\Company: String'.</span></span>
44. <span data-ttu-id="0f1a4-214">[バインド] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="0f1a4-214">Click Bind.</span></span>
45. <span data-ttu-id="0f1a4-215">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="0f1a4-215">Click Save.</span></span>
46. <span data-ttu-id="0f1a4-216">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="0f1a4-216">Close the page.</span></span>


