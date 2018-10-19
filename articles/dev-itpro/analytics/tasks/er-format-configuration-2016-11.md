--- 
title: "ER 書式設定のコンフィギュレーションの作成 (2016 年 11 月)"
description: "次の手順では、システム管理者または電子申告開発者の役割のユーザーが、電子申告 (ER) にコンフィギュレーションの書式設定を作成する方法を説明します。"
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ERWorkspace, ERSolutionTable, ERSolutionCreateDropDialog, EROperationDesigner, ERComponentTypeDropDialog
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: 803ed4a1018d344f1b40fa1f2338fc066e784c3c
ms.contentlocale: ja-jp
ms.lasthandoff: 10/16/2018

---
# <a name="er-create-a-format-configuration-november-2016"></a><span data-ttu-id="64178-103">ER 書式設定のコンフィギュレーションの作成 (2016 年 11 月)</span><span class="sxs-lookup"><span data-stu-id="64178-103">ER Create a format configuration (November 2016)</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="64178-104">次の手順では、システム管理者または電子申告開発者の役割のユーザーが、電子申告 (ER) にコンフィギュレーションの書式設定を作成する方法を説明します。</span><span class="sxs-lookup"><span data-stu-id="64178-104">The following steps explain how a user in the System Administrator or Electronic Reporting Developer role can create a format configuration for Electronic reporting (ER).</span></span> <span data-ttu-id="64178-105">このコンフィギュレーションの書式設定では、支払を処理するために使用される電子ドキュメントの書式を定義します。</span><span class="sxs-lookup"><span data-stu-id="64178-105">This format configuration will define the format of electronic documents that are used for processing payments.</span></span> <span data-ttu-id="64178-106">この例では、サンプル会社 Litware、Inc. の形式コンフィギュレーションを作成します。これらの手順を完了するには、先に「選択したデータソースへのモデルのマッピング」の手順の各ステップを完了する必要があります。</span><span class="sxs-lookup"><span data-stu-id="64178-106">In this example, you will create a format configuration for sample company, Litware, Inc. To complete these steps, you must first complete the steps in the “Map model to selected datasources” procedure.</span></span>


## <a name="create-a-new-format-configuration"></a><span data-ttu-id="64178-107">新しいコンフィギュレーションの書式設定の作成</span><span class="sxs-lookup"><span data-stu-id="64178-107">Create a new format configuration</span></span>
1. <span data-ttu-id="64178-108">[組織管理] > [ワークスペース] > [電子申告] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="64178-108">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="64178-109">[コンフィギュレーションをレポートする] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="64178-109">Click Reporting configurations.</span></span>
3. <span data-ttu-id="64178-110">ツリーで、「支払 (単純化モデル)」を選択します。</span><span class="sxs-lookup"><span data-stu-id="64178-110">In the tree, select 'Payments (simplified model)'.</span></span>
4. <span data-ttu-id="64178-111">[コンフィギュレーションの作成] をクリックすると、ドロップ ダイアログが開きます。</span><span class="sxs-lookup"><span data-stu-id="64178-111">Click Create configuration to open the drop dialog.</span></span>
5. <span data-ttu-id="64178-112">[新規] フィールドで、「PaymentModel データ モデルに基づいた書式」と入力します。</span><span class="sxs-lookup"><span data-stu-id="64178-112">In the New field, enter 'Format based on data model PaymentModel'.</span></span>
6. <span data-ttu-id="64178-113">[名前] フィールドに、「BACS (英国企業)」と入力します。</span><span class="sxs-lookup"><span data-stu-id="64178-113">In the Name field, type 'BACS (UK fictitious)'.</span></span>
    * <span data-ttu-id="64178-114">BACS (英国企業)</span><span class="sxs-lookup"><span data-stu-id="64178-114">BACS (UK fictitious)</span></span>  
7. <span data-ttu-id="64178-115">[説明] フィールドに、「BACS の仕入先支払形式 (英国企業) 」と入力します。</span><span class="sxs-lookup"><span data-stu-id="64178-115">In the Description field, type 'BACS vendor payment format (UK fictitious)'.</span></span>
    * <span data-ttu-id="64178-116">BACS の仕入先支払形式 (英国企業)</span><span class="sxs-lookup"><span data-stu-id="64178-116">BACS vendor payment format (UK fictitious)</span></span>  
    * <span data-ttu-id="64178-117">有効なコンフィギュレーション プロバイダーは自動的にここに入力されます。</span><span class="sxs-lookup"><span data-stu-id="64178-117">The active configuration provider is automatically entered here.</span></span> <span data-ttu-id="64178-118">このプロバイダーはこのコンフィギュレーションを管理できます。</span><span class="sxs-lookup"><span data-stu-id="64178-118">This provider will be able to maintain this configuration.</span></span> <span data-ttu-id="64178-119">他のプロバイダーはこのコンフィギュレーションを使用できますが、管理できません。</span><span class="sxs-lookup"><span data-stu-id="64178-119">Other providers can use this configuration, but will not be able to maintain it.</span></span>  
    * <span data-ttu-id="64178-120">電子ドキュメントの特定の形式を定義できます。</span><span class="sxs-lookup"><span data-stu-id="64178-120">A particular format of electronic document can be defined.</span></span> <span data-ttu-id="64178-121">実行時に形式を選択する場合は、このフィールドを空白のままにします。</span><span class="sxs-lookup"><span data-stu-id="64178-121">Leave this field blank if you want to select a format at run-time.</span></span>  
8. <span data-ttu-id="64178-122">[データモデル定義] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="64178-122">In the Data model definition field, enter or select a value.</span></span>
9. <span data-ttu-id="64178-123">[コンフィギュレーションの作成] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="64178-123">Click Create configuration.</span></span>
    * <span data-ttu-id="64178-124">新しいコンフィギュレーションが作成されました。</span><span class="sxs-lookup"><span data-stu-id="64178-124">A new configuration has been created.</span></span> <span data-ttu-id="64178-125">ドラフト バージョンは、電子ドキュメントを管理するためのデザイン形式の保存に使用できます。</span><span class="sxs-lookup"><span data-stu-id="64178-125">The draft version can be used to store the design format for managing electronic documents.</span></span>  

## <a name="design-format-of-electronic-document"></a><span data-ttu-id="64178-126">電子ドキュメントのデザイン形式</span><span class="sxs-lookup"><span data-stu-id="64178-126">Design format of electronic document</span></span>
1. <span data-ttu-id="64178-127">[デザイナー] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="64178-127">Click Designer.</span></span>
2. <span data-ttu-id="64178-128">[ルートの追加] をクリックして、ドロップ ダイアログを開きます。</span><span class="sxs-lookup"><span data-stu-id="64178-128">Click Add root to open the drop dialog.</span></span>
3. <span data-ttu-id="64178-129">ツリーで、[Common\File] を選択します。</span><span class="sxs-lookup"><span data-stu-id="64178-129">In the tree, select 'Common\File'.</span></span>
4. <span data-ttu-id="64178-130">[名前] フィールドに、「Xml」と入力します。</span><span class="sxs-lookup"><span data-stu-id="64178-130">In the Name field, type 'Xml'.</span></span>
    * <span data-ttu-id="64178-131">Xml</span><span class="sxs-lookup"><span data-stu-id="64178-131">Xml</span></span>  
5. <span data-ttu-id="64178-132">[エンコード] フィールドに、「UTF-8」と入力します。</span><span class="sxs-lookup"><span data-stu-id="64178-132">In the Encoding field, type 'UTF-8'.</span></span>
    * <span data-ttu-id="64178-133">UTF-8</span><span class="sxs-lookup"><span data-stu-id="64178-133">UTF-8</span></span>  
6. <span data-ttu-id="64178-134">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="64178-134">Click OK.</span></span>
7. <span data-ttu-id="64178-135">[追加] をクリックしてドロップ ダイアログを開きます。</span><span class="sxs-lookup"><span data-stu-id="64178-135">Click Add to open the drop dialog.</span></span>
8. <span data-ttu-id="64178-136">ツリーで、[XML\Element] を選択します。</span><span class="sxs-lookup"><span data-stu-id="64178-136">In the tree, select 'XML\Element'.</span></span>
9. <span data-ttu-id="64178-137">[名前] フィールドに、「メッセージ」と入力します。</span><span class="sxs-lookup"><span data-stu-id="64178-137">In the Name field, type 'Message'.</span></span>
    * <span data-ttu-id="64178-138">メッセージ</span><span class="sxs-lookup"><span data-stu-id="64178-138">Message</span></span>  
10. <span data-ttu-id="64178-139">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="64178-139">Click OK.</span></span>
11. <span data-ttu-id="64178-140">ツリーで、「Xml\Message」を選択します。</span><span class="sxs-lookup"><span data-stu-id="64178-140">In the tree, select 'Xml\Message'.</span></span>
12. <span data-ttu-id="64178-141">[エレメントの追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="64178-141">Click Add Element.</span></span>
13. <span data-ttu-id="64178-142">[名前] フィールドに、「ProcessingDate」と入力します。</span><span class="sxs-lookup"><span data-stu-id="64178-142">In the Name field, type 'ProcessingDate'.</span></span>
    * <span data-ttu-id="64178-143">ProcessingDate</span><span class="sxs-lookup"><span data-stu-id="64178-143">ProcessingDate</span></span>  
14. <span data-ttu-id="64178-144">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="64178-144">Click OK.</span></span>
15. <span data-ttu-id="64178-145">[エレメントの追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="64178-145">Click Add Element.</span></span>
16. <span data-ttu-id="64178-146">[名前] フィールドに、「MessageId」と入力します。</span><span class="sxs-lookup"><span data-stu-id="64178-146">In the Name field, type 'MessageId'.</span></span>
    * <span data-ttu-id="64178-147">MessageId</span><span class="sxs-lookup"><span data-stu-id="64178-147">MessageId</span></span>  
17. <span data-ttu-id="64178-148">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="64178-148">Click OK.</span></span>
18. <span data-ttu-id="64178-149">[エレメントの追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="64178-149">Click Add Element.</span></span>
19. <span data-ttu-id="64178-150">[名前] フィールドに、「支払」と入力します。</span><span class="sxs-lookup"><span data-stu-id="64178-150">In the Name field, type 'Payments'.</span></span>
    * <span data-ttu-id="64178-151">支払利息</span><span class="sxs-lookup"><span data-stu-id="64178-151">Payments</span></span>  
20. <span data-ttu-id="64178-152">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="64178-152">Click OK.</span></span>
21. <span data-ttu-id="64178-153">ツリーで、「Xml\Message\Payments」を選択します。</span><span class="sxs-lookup"><span data-stu-id="64178-153">In the tree, select 'Xml\Message\Payments'.</span></span>
22. <span data-ttu-id="64178-154">[エレメントの追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="64178-154">Click Add Element.</span></span>
23. <span data-ttu-id="64178-155">[名前] フィールドに、「Item」と入力します。</span><span class="sxs-lookup"><span data-stu-id="64178-155">In the Name field, type 'Item'.</span></span>
    * <span data-ttu-id="64178-156">項目</span><span class="sxs-lookup"><span data-stu-id="64178-156">Item</span></span>  
24. <span data-ttu-id="64178-157">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="64178-157">Click OK.</span></span>
25. <span data-ttu-id="64178-158">ツリーで、「Xml\Message\Payments\Item」を選択します。</span><span class="sxs-lookup"><span data-stu-id="64178-158">In the tree, select 'Xml\Message\Payments\Item'.</span></span>
26. <span data-ttu-id="64178-159">[追加] をクリックしてドロップ ダイアログを開きます。</span><span class="sxs-lookup"><span data-stu-id="64178-159">Click Add to open the drop dialog.</span></span>
27. <span data-ttu-id="64178-160">ツリーで、[XML\Attribute] を選択します。</span><span class="sxs-lookup"><span data-stu-id="64178-160">In the tree, select 'XML\Attribute'.</span></span>
28. <span data-ttu-id="64178-161">[名前] フィールドに、「Id」と入力します。</span><span class="sxs-lookup"><span data-stu-id="64178-161">In the Name field, type 'Id'.</span></span>
    * <span data-ttu-id="64178-162">ID</span><span class="sxs-lookup"><span data-stu-id="64178-162">Id</span></span>  
29. <span data-ttu-id="64178-163">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="64178-163">Click OK.</span></span>
30. <span data-ttu-id="64178-164">[追加] をクリックしてドロップ ダイアログを開きます。</span><span class="sxs-lookup"><span data-stu-id="64178-164">Click Add to open the drop dialog.</span></span>
31. <span data-ttu-id="64178-165">ツリーで、[XML\Element] を選択します。</span><span class="sxs-lookup"><span data-stu-id="64178-165">In the tree, select 'XML\Element'.</span></span>
32. <span data-ttu-id="64178-166">[名前] フィールドに、「Vendor」と入力します。</span><span class="sxs-lookup"><span data-stu-id="64178-166">In the Name field, type 'Vendor'.</span></span>
    * <span data-ttu-id="64178-167">ベンダー</span><span class="sxs-lookup"><span data-stu-id="64178-167">Vendor</span></span>  
33. <span data-ttu-id="64178-168">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="64178-168">Click OK.</span></span>
34. <span data-ttu-id="64178-169">ツリーで、「Xml\Message\Payments\Item\Vendor」を選択します。</span><span class="sxs-lookup"><span data-stu-id="64178-169">In the tree, select 'Xml\Message\Payments\Item\Vendor'.</span></span>
35. <span data-ttu-id="64178-170">[エレメントの追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="64178-170">Click Add Element.</span></span>
36. <span data-ttu-id="64178-171">[名前] フィールドに、「名前」と入力します。</span><span class="sxs-lookup"><span data-stu-id="64178-171">In the Name field, type 'Name'.</span></span>
    * <span data-ttu-id="64178-172">氏名</span><span class="sxs-lookup"><span data-stu-id="64178-172">Name</span></span>  
37. <span data-ttu-id="64178-173">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="64178-173">Click OK.</span></span>
38. <span data-ttu-id="64178-174">[エレメントの追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="64178-174">Click Add Element.</span></span>
39. <span data-ttu-id="64178-175">[名前] フィールドに、「Bank」と入力します。</span><span class="sxs-lookup"><span data-stu-id="64178-175">In the Name field, type 'Bank'.</span></span>
    * <span data-ttu-id="64178-176">銀行</span><span class="sxs-lookup"><span data-stu-id="64178-176">Bank</span></span>  
40. <span data-ttu-id="64178-177">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="64178-177">Click OK.</span></span>
41. <span data-ttu-id="64178-178">ツリーで、「Xml\Message\Payments\Item\Vendor\Bank」を選択します。</span><span class="sxs-lookup"><span data-stu-id="64178-178">In the tree, select 'Xml\Message\Payments\Item\Vendor\Bank'.</span></span>
42. <span data-ttu-id="64178-179">[エレメントの追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="64178-179">Click Add Element.</span></span>
43. <span data-ttu-id="64178-180">[名前] フィールドに、「RoutingNumber」と入力します。</span><span class="sxs-lookup"><span data-stu-id="64178-180">In the Name field, type 'RoutingNumber'.</span></span>
    * <span data-ttu-id="64178-181">RoutingNumber</span><span class="sxs-lookup"><span data-stu-id="64178-181">RoutingNumber</span></span>  
44. <span data-ttu-id="64178-182">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="64178-182">Click OK.</span></span>
45. <span data-ttu-id="64178-183">[エレメントの追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="64178-183">Click Add Element.</span></span>
46. <span data-ttu-id="64178-184">[名前] フィールドに、「AccountNumber」と入力します。</span><span class="sxs-lookup"><span data-stu-id="64178-184">In the Name field, type 'AccountNumber'.</span></span>
    * <span data-ttu-id="64178-185">AccountNumber</span><span class="sxs-lookup"><span data-stu-id="64178-185">AccountNumber</span></span>  
47. <span data-ttu-id="64178-186">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="64178-186">Click OK.</span></span>
48. <span data-ttu-id="64178-187">ツリーで、「Xml\Message\Payments\Item\Vendor」を選択します。</span><span class="sxs-lookup"><span data-stu-id="64178-187">In the tree, select 'Xml\Message\Payments\Item\Vendor'.</span></span>
49. <span data-ttu-id="64178-188">[コピー] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="64178-188">Click Copy.</span></span>
50. <span data-ttu-id="64178-189">ツリーで、「Xml\Message\Payments\Item」を選択します。</span><span class="sxs-lookup"><span data-stu-id="64178-189">In the tree, select 'Xml\Message\Payments\Item'.</span></span>
51. <span data-ttu-id="64178-190">[ペースト] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="64178-190">Click Paste.</span></span>
52. <span data-ttu-id="64178-191">[名前] フィールドに、「Payer」と入力します。</span><span class="sxs-lookup"><span data-stu-id="64178-191">In the Name field, type 'Payer'.</span></span>
    * <span data-ttu-id="64178-192">指定します</span><span class="sxs-lookup"><span data-stu-id="64178-192">Payer</span></span>  
53. <span data-ttu-id="64178-193">ツリーで、「Xml\Message\Payments\Item」を選択します。</span><span class="sxs-lookup"><span data-stu-id="64178-193">In the tree, select 'Xml\Message\Payments\Item'.</span></span>
54. <span data-ttu-id="64178-194">[エレメントの追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="64178-194">Click Add Element.</span></span>
55. <span data-ttu-id="64178-195">[名前] フィールドで、「通貨」と入力します。</span><span class="sxs-lookup"><span data-stu-id="64178-195">In the Name field, type 'Currency'.</span></span>
    * <span data-ttu-id="64178-196">通貨</span><span class="sxs-lookup"><span data-stu-id="64178-196">Currency</span></span>  
56. <span data-ttu-id="64178-197">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="64178-197">Click OK.</span></span>
57. <span data-ttu-id="64178-198">[エレメントの追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="64178-198">Click Add Element.</span></span>
58. <span data-ttu-id="64178-199">[名前] フィールドに、「説明」と入力します。</span><span class="sxs-lookup"><span data-stu-id="64178-199">In the Name field, type 'Description'.</span></span>
    * <span data-ttu-id="64178-200">説明</span><span class="sxs-lookup"><span data-stu-id="64178-200">Description</span></span>  
59. <span data-ttu-id="64178-201">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="64178-201">Click OK.</span></span>
60. <span data-ttu-id="64178-202">[エレメントの追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="64178-202">Click Add Element.</span></span>
61. <span data-ttu-id="64178-203">[名前] フィールドに、「TransDate」と入力します。</span><span class="sxs-lookup"><span data-stu-id="64178-203">In the Name field, type 'TransDate'.</span></span>
    * <span data-ttu-id="64178-204">TransDate</span><span class="sxs-lookup"><span data-stu-id="64178-204">TransDate</span></span>  
62. <span data-ttu-id="64178-205">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="64178-205">Click OK.</span></span>
63. <span data-ttu-id="64178-206">[エレメントの追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="64178-206">Click Add Element.</span></span>
64. <span data-ttu-id="64178-207">[名前] フィールドに、「$Amount」と入力します。</span><span class="sxs-lookup"><span data-stu-id="64178-207">In the Name field, type 'Amount'.</span></span>
    * <span data-ttu-id="64178-208">量</span><span class="sxs-lookup"><span data-stu-id="64178-208">Amount</span></span>  
65. <span data-ttu-id="64178-209">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="64178-209">Click OK.</span></span>

## <a name="prepare-format-components-for-mapping-to-data-model-elements"></a><span data-ttu-id="64178-210">データ モデルの要素にマッピングする形式のコンポーネントを準備します。</span><span class="sxs-lookup"><span data-stu-id="64178-210">Prepare format components for mapping to data model elements</span></span>
1. <span data-ttu-id="64178-211">ツリーで、「Xml\Message\ProcessingDate」を選択します。</span><span class="sxs-lookup"><span data-stu-id="64178-211">In the tree, select 'Xml\Message\ProcessingDate'.</span></span>
2. <span data-ttu-id="64178-212">[追加] をクリックしてドロップ ダイアログを開きます。</span><span class="sxs-lookup"><span data-stu-id="64178-212">Click Add to open the drop dialog.</span></span>
3. <span data-ttu-id="64178-213">ツリーで、「Text\DateTime」を選択します。</span><span class="sxs-lookup"><span data-stu-id="64178-213">In the tree, select 'Text\DateTime'.</span></span>
4. <span data-ttu-id="64178-214">[形式] フィールドで、「yyyy-MM-dd」と入力します。</span><span class="sxs-lookup"><span data-stu-id="64178-214">In the Format field, type 'yyyy-MM-dd'.</span></span>
    * <span data-ttu-id="64178-215">yyyy-MM-dd</span><span class="sxs-lookup"><span data-stu-id="64178-215">yyyy-MM-dd</span></span>  
5. <span data-ttu-id="64178-216">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="64178-216">Click OK.</span></span>
6. <span data-ttu-id="64178-217">ツリーで、「Xml\Message\Payments\Item\TransDate」を選択します。</span><span class="sxs-lookup"><span data-stu-id="64178-217">In the tree, select 'Xml\Message\Payments\Item\TransDate'.</span></span>
7. <span data-ttu-id="64178-218">[日時を追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="64178-218">Click Add DateTime.</span></span>
8. <span data-ttu-id="64178-219">[形式] フィールドで、「yyyy-MM-dd」と入力します。</span><span class="sxs-lookup"><span data-stu-id="64178-219">In the Format field, type 'yyyy-MM-dd'.</span></span>
    * <span data-ttu-id="64178-220">yyyy-MM-dd</span><span class="sxs-lookup"><span data-stu-id="64178-220">yyyy-MM-dd</span></span>  
9. <span data-ttu-id="64178-221">[DateTime 型] フィールドで、「日付」を選択します。</span><span class="sxs-lookup"><span data-stu-id="64178-221">In the DateTime type field, select 'Date'.</span></span>
10. <span data-ttu-id="64178-222">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="64178-222">Click OK.</span></span>
11. <span data-ttu-id="64178-223">ツリーで、「Xml\Message\MessageId」を選択します。</span><span class="sxs-lookup"><span data-stu-id="64178-223">In the tree, select 'Xml\Message\MessageId'.</span></span>
12. <span data-ttu-id="64178-224">[追加] をクリックしてドロップ ダイアログを開きます。</span><span class="sxs-lookup"><span data-stu-id="64178-224">Click Add to open the drop dialog.</span></span>
13. <span data-ttu-id="64178-225">ツリーで、[Text\String] を選択します。</span><span class="sxs-lookup"><span data-stu-id="64178-225">In the tree, select 'Text\String'.</span></span>
14. <span data-ttu-id="64178-226">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="64178-226">Click OK.</span></span>
15. <span data-ttu-id="64178-227">ツリーで、「Xml\Message\Payments\Item\Vendor\Name」を選択します。</span><span class="sxs-lookup"><span data-stu-id="64178-227">In the tree, select 'Xml\Message\Payments\Item\Vendor\Name'.</span></span>
16. <span data-ttu-id="64178-228">[ストリングの追加」をクリックします。</span><span class="sxs-lookup"><span data-stu-id="64178-228">Click Add String.</span></span>
17. <span data-ttu-id="64178-229">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="64178-229">Click OK.</span></span>
18. <span data-ttu-id="64178-230">ツリーで、「Xml\Message\Payments\Item\Vendor\Bank\RoutingNumber」を選択します。</span><span class="sxs-lookup"><span data-stu-id="64178-230">In the tree, select 'Xml\Message\Payments\Item\Vendor\Bank\RoutingNumber'.</span></span>
19. <span data-ttu-id="64178-231">[ストリングの追加」をクリックします。</span><span class="sxs-lookup"><span data-stu-id="64178-231">Click Add String.</span></span>
20. <span data-ttu-id="64178-232">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="64178-232">Click OK.</span></span>
21. <span data-ttu-id="64178-233">ツリーで、「Xml\Message\Payments\Item\Vendor\Bank\AccountNumber」を選択します。</span><span class="sxs-lookup"><span data-stu-id="64178-233">In the tree, select 'Xml\Message\Payments\Item\Vendor\Bank\AccountNumber'.</span></span>
22. <span data-ttu-id="64178-234">[ストリングの追加」をクリックします。</span><span class="sxs-lookup"><span data-stu-id="64178-234">Click Add String.</span></span>
23. <span data-ttu-id="64178-235">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="64178-235">Click OK.</span></span>
24. <span data-ttu-id="64178-236">ツリーで、「Xml\Message\Payments\Item\Payer\Name」を選択します。</span><span class="sxs-lookup"><span data-stu-id="64178-236">In the tree, select 'Xml\Message\Payments\Item\Payer\Name'.</span></span>
25. <span data-ttu-id="64178-237">[ストリングの追加」をクリックします。</span><span class="sxs-lookup"><span data-stu-id="64178-237">Click Add String.</span></span>
26. <span data-ttu-id="64178-238">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="64178-238">Click OK.</span></span>
27. <span data-ttu-id="64178-239">ツリーで、「Xml\Message\Payments\Item\Payer\Bank\RoutingNumber」を選択します。</span><span class="sxs-lookup"><span data-stu-id="64178-239">In the tree, select 'Xml\Message\Payments\Item\Payer\Bank\RoutingNumber'.</span></span>
28. <span data-ttu-id="64178-240">[ストリングの追加」をクリックします。</span><span class="sxs-lookup"><span data-stu-id="64178-240">Click Add String.</span></span>
29. <span data-ttu-id="64178-241">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="64178-241">Click OK.</span></span>
30. <span data-ttu-id="64178-242">ツリーで、「Xml\Message\Payments\Item\Payer\Bank\AccountNumber」を選択します。</span><span class="sxs-lookup"><span data-stu-id="64178-242">In the tree, select 'Xml\Message\Payments\Item\Payer\Bank\AccountNumber'.</span></span>
31. <span data-ttu-id="64178-243">[ストリングの追加」をクリックします。</span><span class="sxs-lookup"><span data-stu-id="64178-243">Click Add String.</span></span>
32. <span data-ttu-id="64178-244">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="64178-244">Click OK.</span></span>
33. <span data-ttu-id="64178-245">ツリーで、「Xml\Message\Payments\Item\Currency」を選択します。</span><span class="sxs-lookup"><span data-stu-id="64178-245">In the tree, select 'Xml\Message\Payments\Item\Currency'.</span></span>
34. <span data-ttu-id="64178-246">[ストリングの追加」をクリックします。</span><span class="sxs-lookup"><span data-stu-id="64178-246">Click Add String.</span></span>
35. <span data-ttu-id="64178-247">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="64178-247">Click OK.</span></span>
36. <span data-ttu-id="64178-248">ツリーで、「Xml\Message\Payments\Item\Description」を選択します。</span><span class="sxs-lookup"><span data-stu-id="64178-248">In the tree, select 'Xml\Message\Payments\Item\Description'.</span></span>
37. <span data-ttu-id="64178-249">[ストリングの追加」をクリックします。</span><span class="sxs-lookup"><span data-stu-id="64178-249">Click Add String.</span></span>
38. <span data-ttu-id="64178-250">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="64178-250">Click OK.</span></span>
39. <span data-ttu-id="64178-251">ツリーで、「Xml\Message\Payments\Item\Amount」を選択します。</span><span class="sxs-lookup"><span data-stu-id="64178-251">In the tree, select 'Xml\Message\Payments\Item\Amount'.</span></span>
40. <span data-ttu-id="64178-252">[ストリングの追加」をクリックします。</span><span class="sxs-lookup"><span data-stu-id="64178-252">Click Add String.</span></span>
41. <span data-ttu-id="64178-253">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="64178-253">Click OK.</span></span>
42. <span data-ttu-id="64178-254">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="64178-254">Click Save.</span></span>
43. <span data-ttu-id="64178-255">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="64178-255">Close the page.</span></span>


