--- 
title: "電子申告 (ER) 用の形式コンフィギュレーションを作成する"
description: "次の手順では、システム管理者または電子申告開発者の役割のユーザーが、電子申告 (ER) にコンフィギュレーションの書式設定を作成する方法を説明します。"
author: NickSelin
manager: AnnBe
ms.date: 01/16/2017
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
ms.openlocfilehash: 04817d1f1851e43679995641e8b0ff99edaa83ad
ms.contentlocale: ja-jp
ms.lasthandoff: 08/29/2017

---
# <a name="create-a-format-configuration-for-electronic-reporting-er"></a><span data-ttu-id="fd18d-103">電子申告 (ER) 用の形式コンフィギュレーションを作成する</span><span class="sxs-lookup"><span data-stu-id="fd18d-103">Create a format configuration for electronic reporting (ER)</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="fd18d-104">次の手順では、システム管理者または電子申告開発者の役割のユーザーが、電子申告 (ER) にコンフィギュレーションの書式設定を作成する方法を説明します。</span><span class="sxs-lookup"><span data-stu-id="fd18d-104">The following steps explain how a user in the System Administrator or Electronic Reporting Developer role can create a format configuration for Electronic reporting (ER).</span></span> <span data-ttu-id="fd18d-105">このコンフィギュレーションの書式設定では、支払を処理するために使用される電子ドキュメントの書式を定義します。</span><span class="sxs-lookup"><span data-stu-id="fd18d-105">This format configuration will define the format of electronic documents that are used for processing payments.</span></span> <span data-ttu-id="fd18d-106">この例では、サンプル会社 Litware、Inc. の形式コンフィギュレーションを作成します。これらの手順を完了するには、先に「選択したデータソースへのモデルのマッピング」の手順の各ステップを完了する必要があります。</span><span class="sxs-lookup"><span data-stu-id="fd18d-106">In this example, you will create a format configuration for sample company, Litware, Inc. To complete these steps, you must first complete the steps in the “Map model to selected datasources” procedure.</span></span>


## <a name="create-a-new-format-configuration"></a><span data-ttu-id="fd18d-107">新しいコンフィギュレーションの書式設定の作成</span><span class="sxs-lookup"><span data-stu-id="fd18d-107">Create a new format configuration</span></span>
1. <span data-ttu-id="fd18d-108">[組織管理] > [ワークスペース] > [電子申告] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="fd18d-108">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="fd18d-109">[コンフィギュレーションをレポートする] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="fd18d-109">Click Reporting configurations.</span></span>
3. <span data-ttu-id="fd18d-110">ツリーで、「支払 (単純化モデル)」を選択します。</span><span class="sxs-lookup"><span data-stu-id="fd18d-110">In the tree, select 'Payments (simplified model)'.</span></span>
4. <span data-ttu-id="fd18d-111">[コンフィギュレーションの作成] をクリックすると、ドロップ ダイアログが開きます。</span><span class="sxs-lookup"><span data-stu-id="fd18d-111">Click Create configuration to open the drop dialog.</span></span>
5. <span data-ttu-id="fd18d-112">[新規] フィールドで、「PaymentModel データ モデルに基づいた書式」と入力します。</span><span class="sxs-lookup"><span data-stu-id="fd18d-112">In the New field, enter 'Format based on data model PaymentModel'.</span></span>
6. <span data-ttu-id="fd18d-113">[名前] フィールドに、「BACS (英国企業)」と入力します。</span><span class="sxs-lookup"><span data-stu-id="fd18d-113">In the Name field, type 'BACS (UK fictitious)'.</span></span>
    * <span data-ttu-id="fd18d-114">BACS (英国企業)</span><span class="sxs-lookup"><span data-stu-id="fd18d-114">BACS (UK fictitious)</span></span>  
7. <span data-ttu-id="fd18d-115">[説明] フィールドに、「BACS の仕入先支払形式 (英国企業) 」と入力します。</span><span class="sxs-lookup"><span data-stu-id="fd18d-115">In the Description field, type 'BACS vendor payment format (UK fictitious)'.</span></span>
    * <span data-ttu-id="fd18d-116">BACS の仕入先支払形式 (英国企業)</span><span class="sxs-lookup"><span data-stu-id="fd18d-116">BACS vendor payment format (UK fictitious)</span></span>  
    * <span data-ttu-id="fd18d-117">有効なコンフィギュレーション プロバイダーは自動的にここに入力されます。</span><span class="sxs-lookup"><span data-stu-id="fd18d-117">The active configuration provider is automatically entered here.</span></span> <span data-ttu-id="fd18d-118">このプロバイダーはこのコンフィギュレーションを管理できます。</span><span class="sxs-lookup"><span data-stu-id="fd18d-118">This provider will be able to maintain this configuration.</span></span> <span data-ttu-id="fd18d-119">他のプロバイダーはこのコンフィギュレーションを使用できますが、管理できません。</span><span class="sxs-lookup"><span data-stu-id="fd18d-119">Other providers can use this configuration, but will not be able to maintain it.</span></span>  
    * <span data-ttu-id="fd18d-120">電子ドキュメントの特定の形式を定義できます。</span><span class="sxs-lookup"><span data-stu-id="fd18d-120">A particular format of electronic document can be defined.</span></span> <span data-ttu-id="fd18d-121">実行時に形式を選択する場合は、このフィールドを空白のままにします。</span><span class="sxs-lookup"><span data-stu-id="fd18d-121">Leave this field blank if you want to select a format at run-time.</span></span>  
8. <span data-ttu-id="fd18d-122">[データモデル定義] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="fd18d-122">In the Data model definition field, enter or select a value.</span></span>
9. <span data-ttu-id="fd18d-123">[コンフィギュレーションの作成] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="fd18d-123">Click Create configuration.</span></span>
    * <span data-ttu-id="fd18d-124">新しいコンフィギュレーションが作成されました。</span><span class="sxs-lookup"><span data-stu-id="fd18d-124">A new configuration has been created.</span></span> <span data-ttu-id="fd18d-125">ドラフト バージョンは、電子ドキュメントを管理するためのデザイン形式の保存に使用できます。</span><span class="sxs-lookup"><span data-stu-id="fd18d-125">The draft version can be used to store the design format for managing electronic documents.</span></span>  

## <a name="design-format-of-electronic-document"></a><span data-ttu-id="fd18d-126">電子ドキュメントのデザイン形式</span><span class="sxs-lookup"><span data-stu-id="fd18d-126">Design format of electronic document</span></span>
1. <span data-ttu-id="fd18d-127">[デザイナー] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="fd18d-127">Click Designer.</span></span>
2. <span data-ttu-id="fd18d-128">[ルートの追加] をクリックして、ドロップ ダイアログを開きます。</span><span class="sxs-lookup"><span data-stu-id="fd18d-128">Click Add root to open the drop dialog.</span></span>
3. <span data-ttu-id="fd18d-129">ツリーで、[Common\File] を選択します。</span><span class="sxs-lookup"><span data-stu-id="fd18d-129">In the tree, select 'Common\File'.</span></span>
4. <span data-ttu-id="fd18d-130">[名前] フィールドに、「Xml」と入力します。</span><span class="sxs-lookup"><span data-stu-id="fd18d-130">In the Name field, type 'Xml'.</span></span>
    * <span data-ttu-id="fd18d-131">Xml</span><span class="sxs-lookup"><span data-stu-id="fd18d-131">Xml</span></span>  
5. <span data-ttu-id="fd18d-132">[エンコード] フィールドに、「UTF-8」と入力します。</span><span class="sxs-lookup"><span data-stu-id="fd18d-132">In the Encoding field, type 'UTF-8'.</span></span>
    * <span data-ttu-id="fd18d-133">UTF-8</span><span class="sxs-lookup"><span data-stu-id="fd18d-133">UTF-8</span></span>  
6. <span data-ttu-id="fd18d-134">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="fd18d-134">Click OK.</span></span>
7. <span data-ttu-id="fd18d-135">[追加] をクリックしてドロップ ダイアログを開きます。</span><span class="sxs-lookup"><span data-stu-id="fd18d-135">Click Add to open the drop dialog.</span></span>
8. <span data-ttu-id="fd18d-136">ツリーで、[XML\Element] を選択します。</span><span class="sxs-lookup"><span data-stu-id="fd18d-136">In the tree, select 'XML\Element'.</span></span>
9. <span data-ttu-id="fd18d-137">[名前] フィールドに、「メッセージ」と入力します。</span><span class="sxs-lookup"><span data-stu-id="fd18d-137">In the Name field, type 'Message'.</span></span>
    * <span data-ttu-id="fd18d-138">メッセージ</span><span class="sxs-lookup"><span data-stu-id="fd18d-138">Message</span></span>  
10. <span data-ttu-id="fd18d-139">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="fd18d-139">Click OK.</span></span>
11. <span data-ttu-id="fd18d-140">ツリーで、「Xml\Message」を選択します。</span><span class="sxs-lookup"><span data-stu-id="fd18d-140">In the tree, select 'Xml\Message'.</span></span>
12. <span data-ttu-id="fd18d-141">[エレメントの追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="fd18d-141">Click Add Element.</span></span>
13. <span data-ttu-id="fd18d-142">[名前] フィールドに、「ProcessingDate」と入力します。</span><span class="sxs-lookup"><span data-stu-id="fd18d-142">In the Name field, type 'ProcessingDate'.</span></span>
    * <span data-ttu-id="fd18d-143">ProcessingDate</span><span class="sxs-lookup"><span data-stu-id="fd18d-143">ProcessingDate</span></span>  
14. <span data-ttu-id="fd18d-144">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="fd18d-144">Click OK.</span></span>
15. <span data-ttu-id="fd18d-145">[エレメントの追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="fd18d-145">Click Add Element.</span></span>
16. <span data-ttu-id="fd18d-146">[名前] フィールドに、「MessageId」と入力します。</span><span class="sxs-lookup"><span data-stu-id="fd18d-146">In the Name field, type 'MessageId'.</span></span>
    * <span data-ttu-id="fd18d-147">MessageId</span><span class="sxs-lookup"><span data-stu-id="fd18d-147">MessageId</span></span>  
17. <span data-ttu-id="fd18d-148">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="fd18d-148">Click OK.</span></span>
18. <span data-ttu-id="fd18d-149">[エレメントの追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="fd18d-149">Click Add Element.</span></span>
19. <span data-ttu-id="fd18d-150">[名前] フィールドに、「支払」と入力します。</span><span class="sxs-lookup"><span data-stu-id="fd18d-150">In the Name field, type 'Payments'.</span></span>
    * <span data-ttu-id="fd18d-151">支払利息</span><span class="sxs-lookup"><span data-stu-id="fd18d-151">Payments</span></span>  
20. <span data-ttu-id="fd18d-152">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="fd18d-152">Click OK.</span></span>
21. <span data-ttu-id="fd18d-153">ツリーで、「Xml\Message\Payments」を選択します。</span><span class="sxs-lookup"><span data-stu-id="fd18d-153">In the tree, select 'Xml\Message\Payments'.</span></span>
22. <span data-ttu-id="fd18d-154">[エレメントの追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="fd18d-154">Click Add Element.</span></span>
23. <span data-ttu-id="fd18d-155">[名前] フィールドに、「Item」と入力します。</span><span class="sxs-lookup"><span data-stu-id="fd18d-155">In the Name field, type 'Item'.</span></span>
    * <span data-ttu-id="fd18d-156">項目</span><span class="sxs-lookup"><span data-stu-id="fd18d-156">Item</span></span>  
24. <span data-ttu-id="fd18d-157">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="fd18d-157">Click OK.</span></span>
25. <span data-ttu-id="fd18d-158">ツリーで、「Xml\Message\Payments\Item」を選択します。</span><span class="sxs-lookup"><span data-stu-id="fd18d-158">In the tree, select 'Xml\Message\Payments\Item'.</span></span>
26. <span data-ttu-id="fd18d-159">[追加] をクリックしてドロップ ダイアログを開きます。</span><span class="sxs-lookup"><span data-stu-id="fd18d-159">Click Add to open the drop dialog.</span></span>
27. <span data-ttu-id="fd18d-160">ツリーで、[XML\Attribute] を選択します。</span><span class="sxs-lookup"><span data-stu-id="fd18d-160">In the tree, select 'XML\Attribute'.</span></span>
28. <span data-ttu-id="fd18d-161">[名前] フィールドに、「Id」と入力します。</span><span class="sxs-lookup"><span data-stu-id="fd18d-161">In the Name field, type 'Id'.</span></span>
    * <span data-ttu-id="fd18d-162">ID</span><span class="sxs-lookup"><span data-stu-id="fd18d-162">Id</span></span>  
29. <span data-ttu-id="fd18d-163">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="fd18d-163">Click OK.</span></span>
30. <span data-ttu-id="fd18d-164">[追加] をクリックしてドロップ ダイアログを開きます。</span><span class="sxs-lookup"><span data-stu-id="fd18d-164">Click Add to open the drop dialog.</span></span>
31. <span data-ttu-id="fd18d-165">ツリーで、[XML\Element] を選択します。</span><span class="sxs-lookup"><span data-stu-id="fd18d-165">In the tree, select 'XML\Element'.</span></span>
32. <span data-ttu-id="fd18d-166">[名前] フィールドに、「Vendor」と入力します。</span><span class="sxs-lookup"><span data-stu-id="fd18d-166">In the Name field, type 'Vendor'.</span></span>
    * <span data-ttu-id="fd18d-167">ベンダー</span><span class="sxs-lookup"><span data-stu-id="fd18d-167">Vendor</span></span>  
33. <span data-ttu-id="fd18d-168">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="fd18d-168">Click OK.</span></span>
34. <span data-ttu-id="fd18d-169">ツリーで、「Xml\Message\Payments\Item\Vendor」を選択します。</span><span class="sxs-lookup"><span data-stu-id="fd18d-169">In the tree, select 'Xml\Message\Payments\Item\Vendor'.</span></span>
35. <span data-ttu-id="fd18d-170">[エレメントの追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="fd18d-170">Click Add Element.</span></span>
36. <span data-ttu-id="fd18d-171">[名前] フィールドに、「名前」と入力します。</span><span class="sxs-lookup"><span data-stu-id="fd18d-171">In the Name field, type 'Name'.</span></span>
    * <span data-ttu-id="fd18d-172">氏名</span><span class="sxs-lookup"><span data-stu-id="fd18d-172">Name</span></span>  
37. <span data-ttu-id="fd18d-173">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="fd18d-173">Click OK.</span></span>
38. <span data-ttu-id="fd18d-174">[エレメントの追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="fd18d-174">Click Add Element.</span></span>
39. <span data-ttu-id="fd18d-175">[名前] フィールドに、「Bank」と入力します。</span><span class="sxs-lookup"><span data-stu-id="fd18d-175">In the Name field, type 'Bank'.</span></span>
    * <span data-ttu-id="fd18d-176">銀行</span><span class="sxs-lookup"><span data-stu-id="fd18d-176">Bank</span></span>  
40. <span data-ttu-id="fd18d-177">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="fd18d-177">Click OK.</span></span>
41. <span data-ttu-id="fd18d-178">ツリーで、「Xml\Message\Payments\Item\Vendor\Bank」を選択します。</span><span class="sxs-lookup"><span data-stu-id="fd18d-178">In the tree, select 'Xml\Message\Payments\Item\Vendor\Bank'.</span></span>
42. <span data-ttu-id="fd18d-179">[エレメントの追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="fd18d-179">Click Add Element.</span></span>
43. <span data-ttu-id="fd18d-180">[名前] フィールドに、「RoutingNumber」と入力します。</span><span class="sxs-lookup"><span data-stu-id="fd18d-180">In the Name field, type 'RoutingNumber'.</span></span>
    * <span data-ttu-id="fd18d-181">RoutingNumber</span><span class="sxs-lookup"><span data-stu-id="fd18d-181">RoutingNumber</span></span>  
44. <span data-ttu-id="fd18d-182">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="fd18d-182">Click OK.</span></span>
45. <span data-ttu-id="fd18d-183">[エレメントの追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="fd18d-183">Click Add Element.</span></span>
46. <span data-ttu-id="fd18d-184">[名前] フィールドに、「AccountNumber」と入力します。</span><span class="sxs-lookup"><span data-stu-id="fd18d-184">In the Name field, type 'AccountNumber'.</span></span>
    * <span data-ttu-id="fd18d-185">AccountNumber</span><span class="sxs-lookup"><span data-stu-id="fd18d-185">AccountNumber</span></span>  
47. <span data-ttu-id="fd18d-186">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="fd18d-186">Click OK.</span></span>
48. <span data-ttu-id="fd18d-187">ツリーで、「Xml\Message\Payments\Item\Vendor」を選択します。</span><span class="sxs-lookup"><span data-stu-id="fd18d-187">In the tree, select 'Xml\Message\Payments\Item\Vendor'.</span></span>
49. <span data-ttu-id="fd18d-188">[コピー] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="fd18d-188">Click Copy.</span></span>
50. <span data-ttu-id="fd18d-189">ツリーで、「Xml\Message\Payments\Item」を選択します。</span><span class="sxs-lookup"><span data-stu-id="fd18d-189">In the tree, select 'Xml\Message\Payments\Item'.</span></span>
51. <span data-ttu-id="fd18d-190">[ペースト] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="fd18d-190">Click Paste.</span></span>
52. <span data-ttu-id="fd18d-191">[名前] フィールドに、「Payer」と入力します。</span><span class="sxs-lookup"><span data-stu-id="fd18d-191">In the Name field, type 'Payer'.</span></span>
    * <span data-ttu-id="fd18d-192">指定します</span><span class="sxs-lookup"><span data-stu-id="fd18d-192">Payer</span></span>  
53. <span data-ttu-id="fd18d-193">ツリーで、「Xml\Message\Payments\Item」を選択します。</span><span class="sxs-lookup"><span data-stu-id="fd18d-193">In the tree, select 'Xml\Message\Payments\Item'.</span></span>
54. <span data-ttu-id="fd18d-194">[エレメントの追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="fd18d-194">Click Add Element.</span></span>
55. <span data-ttu-id="fd18d-195">[名前] フィールドで、「通貨」と入力します。</span><span class="sxs-lookup"><span data-stu-id="fd18d-195">In the Name field, type 'Currency'.</span></span>
    * <span data-ttu-id="fd18d-196">通貨</span><span class="sxs-lookup"><span data-stu-id="fd18d-196">Currency</span></span>  
56. <span data-ttu-id="fd18d-197">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="fd18d-197">Click OK.</span></span>
57. <span data-ttu-id="fd18d-198">[エレメントの追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="fd18d-198">Click Add Element.</span></span>
58. <span data-ttu-id="fd18d-199">[名前] フィールドに、「説明」と入力します。</span><span class="sxs-lookup"><span data-stu-id="fd18d-199">In the Name field, type 'Description'.</span></span>
    * <span data-ttu-id="fd18d-200">説明</span><span class="sxs-lookup"><span data-stu-id="fd18d-200">Description</span></span>  
59. <span data-ttu-id="fd18d-201">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="fd18d-201">Click OK.</span></span>
60. <span data-ttu-id="fd18d-202">[エレメントの追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="fd18d-202">Click Add Element.</span></span>
61. <span data-ttu-id="fd18d-203">[名前] フィールドに、「TransDate」と入力します。</span><span class="sxs-lookup"><span data-stu-id="fd18d-203">In the Name field, type 'TransDate'.</span></span>
    * <span data-ttu-id="fd18d-204">TransDate</span><span class="sxs-lookup"><span data-stu-id="fd18d-204">TransDate</span></span>  
62. <span data-ttu-id="fd18d-205">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="fd18d-205">Click OK.</span></span>
63. <span data-ttu-id="fd18d-206">[エレメントの追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="fd18d-206">Click Add Element.</span></span>
64. <span data-ttu-id="fd18d-207">[名前] フィールドに、「$Amount」と入力します。</span><span class="sxs-lookup"><span data-stu-id="fd18d-207">In the Name field, type 'Amount'.</span></span>
    * <span data-ttu-id="fd18d-208">量</span><span class="sxs-lookup"><span data-stu-id="fd18d-208">Amount</span></span>  
65. <span data-ttu-id="fd18d-209">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="fd18d-209">Click OK.</span></span>

## <a name="prepare-format-components-for-mapping-to-data-model-elements"></a><span data-ttu-id="fd18d-210">データ モデルの要素にマッピングする形式のコンポーネントを準備します。</span><span class="sxs-lookup"><span data-stu-id="fd18d-210">Prepare format components for mapping to data model elements</span></span>
1. <span data-ttu-id="fd18d-211">ツリーで、「Xml\Message\ProcessingDate」を選択します。</span><span class="sxs-lookup"><span data-stu-id="fd18d-211">In the tree, select 'Xml\Message\ProcessingDate'.</span></span>
2. <span data-ttu-id="fd18d-212">[追加] をクリックしてドロップ ダイアログを開きます。</span><span class="sxs-lookup"><span data-stu-id="fd18d-212">Click Add to open the drop dialog.</span></span>
3. <span data-ttu-id="fd18d-213">ツリーで、「Text\DateTime」を選択します。</span><span class="sxs-lookup"><span data-stu-id="fd18d-213">In the tree, select 'Text\DateTime'.</span></span>
4. <span data-ttu-id="fd18d-214">[形式] フィールドで、「yyyy-MM-dd」と入力します。</span><span class="sxs-lookup"><span data-stu-id="fd18d-214">In the Format field, type 'yyyy-MM-dd'.</span></span>
    * <span data-ttu-id="fd18d-215">yyyy-MM-dd</span><span class="sxs-lookup"><span data-stu-id="fd18d-215">yyyy-MM-dd</span></span>  
5. <span data-ttu-id="fd18d-216">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="fd18d-216">Click OK.</span></span>
6. <span data-ttu-id="fd18d-217">ツリーで、「Xml\Message\Payments\Item\TransDate」を選択します。</span><span class="sxs-lookup"><span data-stu-id="fd18d-217">In the tree, select 'Xml\Message\Payments\Item\TransDate'.</span></span>
7. <span data-ttu-id="fd18d-218">[日時を追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="fd18d-218">Click Add DateTime.</span></span>
8. <span data-ttu-id="fd18d-219">[形式] フィールドで、「yyyy-MM-dd」と入力します。</span><span class="sxs-lookup"><span data-stu-id="fd18d-219">In the Format field, type 'yyyy-MM-dd'.</span></span>
    * <span data-ttu-id="fd18d-220">yyyy-MM-dd</span><span class="sxs-lookup"><span data-stu-id="fd18d-220">yyyy-MM-dd</span></span>  
9. <span data-ttu-id="fd18d-221">[DateTime 型] フィールドで、「日付」を選択します。</span><span class="sxs-lookup"><span data-stu-id="fd18d-221">In the DateTime type field, select 'Date'.</span></span>
10. <span data-ttu-id="fd18d-222">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="fd18d-222">Click OK.</span></span>
11. <span data-ttu-id="fd18d-223">ツリーで、「Xml\Message\MessageId」を選択します。</span><span class="sxs-lookup"><span data-stu-id="fd18d-223">In the tree, select 'Xml\Message\MessageId'.</span></span>
12. <span data-ttu-id="fd18d-224">[追加] をクリックしてドロップ ダイアログを開きます。</span><span class="sxs-lookup"><span data-stu-id="fd18d-224">Click Add to open the drop dialog.</span></span>
13. <span data-ttu-id="fd18d-225">ツリーで、[Text\String] を選択します。</span><span class="sxs-lookup"><span data-stu-id="fd18d-225">In the tree, select 'Text\String'.</span></span>
14. <span data-ttu-id="fd18d-226">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="fd18d-226">Click OK.</span></span>
15. <span data-ttu-id="fd18d-227">ツリーで、「Xml\Message\Payments\Item\Vendor\Name」を選択します。</span><span class="sxs-lookup"><span data-stu-id="fd18d-227">In the tree, select 'Xml\Message\Payments\Item\Vendor\Name'.</span></span>
16. <span data-ttu-id="fd18d-228">[ストリングの追加」をクリックします。</span><span class="sxs-lookup"><span data-stu-id="fd18d-228">Click Add String.</span></span>
17. <span data-ttu-id="fd18d-229">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="fd18d-229">Click OK.</span></span>
18. <span data-ttu-id="fd18d-230">ツリーで、「Xml\Message\Payments\Item\Vendor\Bank\RoutingNumber」を選択します。</span><span class="sxs-lookup"><span data-stu-id="fd18d-230">In the tree, select 'Xml\Message\Payments\Item\Vendor\Bank\RoutingNumber'.</span></span>
19. <span data-ttu-id="fd18d-231">[ストリングの追加」をクリックします。</span><span class="sxs-lookup"><span data-stu-id="fd18d-231">Click Add String.</span></span>
20. <span data-ttu-id="fd18d-232">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="fd18d-232">Click OK.</span></span>
21. <span data-ttu-id="fd18d-233">ツリーで、「Xml\Message\Payments\Item\Vendor\Bank\AccountNumber」を選択します。</span><span class="sxs-lookup"><span data-stu-id="fd18d-233">In the tree, select 'Xml\Message\Payments\Item\Vendor\Bank\AccountNumber'.</span></span>
22. <span data-ttu-id="fd18d-234">[ストリングの追加」をクリックします。</span><span class="sxs-lookup"><span data-stu-id="fd18d-234">Click Add String.</span></span>
23. <span data-ttu-id="fd18d-235">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="fd18d-235">Click OK.</span></span>
24. <span data-ttu-id="fd18d-236">ツリーで、「Xml\Message\Payments\Item\Payer\Name」を選択します。</span><span class="sxs-lookup"><span data-stu-id="fd18d-236">In the tree, select 'Xml\Message\Payments\Item\Payer\Name'.</span></span>
25. <span data-ttu-id="fd18d-237">[ストリングの追加」をクリックします。</span><span class="sxs-lookup"><span data-stu-id="fd18d-237">Click Add String.</span></span>
26. <span data-ttu-id="fd18d-238">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="fd18d-238">Click OK.</span></span>
27. <span data-ttu-id="fd18d-239">ツリーで、「Xml\Message\Payments\Item\Payer\Bank\RoutingNumber」を選択します。</span><span class="sxs-lookup"><span data-stu-id="fd18d-239">In the tree, select 'Xml\Message\Payments\Item\Payer\Bank\RoutingNumber'.</span></span>
28. <span data-ttu-id="fd18d-240">[ストリングの追加」をクリックします。</span><span class="sxs-lookup"><span data-stu-id="fd18d-240">Click Add String.</span></span>
29. <span data-ttu-id="fd18d-241">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="fd18d-241">Click OK.</span></span>
30. <span data-ttu-id="fd18d-242">ツリーで、「Xml\Message\Payments\Item\Payer\Bank\AccountNumber」を選択します。</span><span class="sxs-lookup"><span data-stu-id="fd18d-242">In the tree, select 'Xml\Message\Payments\Item\Payer\Bank\AccountNumber'.</span></span>
31. <span data-ttu-id="fd18d-243">[ストリングの追加」をクリックします。</span><span class="sxs-lookup"><span data-stu-id="fd18d-243">Click Add String.</span></span>
32. <span data-ttu-id="fd18d-244">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="fd18d-244">Click OK.</span></span>
33. <span data-ttu-id="fd18d-245">ツリーで、「Xml\Message\Payments\Item\Currency」を選択します。</span><span class="sxs-lookup"><span data-stu-id="fd18d-245">In the tree, select 'Xml\Message\Payments\Item\Currency'.</span></span>
34. <span data-ttu-id="fd18d-246">[ストリングの追加」をクリックします。</span><span class="sxs-lookup"><span data-stu-id="fd18d-246">Click Add String.</span></span>
35. <span data-ttu-id="fd18d-247">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="fd18d-247">Click OK.</span></span>
36. <span data-ttu-id="fd18d-248">ツリーで、「Xml\Message\Payments\Item\Description」を選択します。</span><span class="sxs-lookup"><span data-stu-id="fd18d-248">In the tree, select 'Xml\Message\Payments\Item\Description'.</span></span>
37. <span data-ttu-id="fd18d-249">[ストリングの追加」をクリックします。</span><span class="sxs-lookup"><span data-stu-id="fd18d-249">Click Add String.</span></span>
38. <span data-ttu-id="fd18d-250">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="fd18d-250">Click OK.</span></span>
39. <span data-ttu-id="fd18d-251">ツリーで、「Xml\Message\Payments\Item\Amount」を選択します。</span><span class="sxs-lookup"><span data-stu-id="fd18d-251">In the tree, select 'Xml\Message\Payments\Item\Amount'.</span></span>
40. <span data-ttu-id="fd18d-252">[ストリングの追加」をクリックします。</span><span class="sxs-lookup"><span data-stu-id="fd18d-252">Click Add String.</span></span>
41. <span data-ttu-id="fd18d-253">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="fd18d-253">Click OK.</span></span>
42. <span data-ttu-id="fd18d-254">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="fd18d-254">Click Save.</span></span>
43. <span data-ttu-id="fd18d-255">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="fd18d-255">Close the page.</span></span>


