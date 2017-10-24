--- 
title: "電子申告 (ER) のアプリケーション データ更新と共にドキュメントを生成するための形式の変更"
description: "この手順のステップを完了するには、まず「ER アプリケーション データ更新と共にドキュメントを生成する (パート 3 - モデルとマッピングの変更)」の手順を完了する必要があります。"
author: NickSelin
manager: AnnBe
ms.date: 06/19/2017
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
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: 47a1fe9cbfc80adbd5d375221912a2fa9787af19
ms.contentlocale: ja-jp
ms.lasthandoff: 09/29/2017

---
# <a name="modify-format-to-generate-documents-with-application-data-update-for-electronic-reporting-er"></a><span data-ttu-id="8ea78-103">電子申告 (ER) のアプリケーション データ更新と共にドキュメントを生成するための形式の変更</span><span class="sxs-lookup"><span data-stu-id="8ea78-103">Modify format to generate documents with application data update for electronic reporting (ER)</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="8ea78-104">この手順のステップを完了するには、まず「ER アプリケーション データ更新と共にドキュメントを生成する (パート 3: モデルとマッピングの変更)」の手順を完了する必要があります。</span><span class="sxs-lookup"><span data-stu-id="8ea78-104">To complete the steps in this procedure, you must first complete the procedure, "ER Generate documents with application data update (Part 3: Modify model and mapping)".</span></span>

<span data-ttu-id="8ea78-105">この手順のステップでは、電子ドキュメントを生成してアプリケーション データを更新するために電子申告 (ER) コンフィギュレーションを設計する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="8ea78-105">The steps in this procedure explain how to design Electronic reporting (ER) configurations to generate an electronic document and update application data.</span></span> <span data-ttu-id="8ea78-106">この手順では、ER コンフィギュレーションを変更し、それを使用して電子ドキュメントを生成するだけでなく、アプリケーション データの更新も行います。</span><span class="sxs-lookup"><span data-stu-id="8ea78-106">In this procedure, you will modify the ER configurations to not just use them to generate electronic documents, but also to update application data.</span></span> <span data-ttu-id="8ea78-107">この手順は、「システム管理者」または「電子レポート開発者」ロールが割り当てられているユーザー用に作成されています。</span><span class="sxs-lookup"><span data-stu-id="8ea78-107">This procedure is created for users with the assigned role of system administrator or electronic reporting developer.</span></span> <span data-ttu-id="8ea78-108">これらのステップは、DEMF データ セットを使用して完了することができます。</span><span class="sxs-lookup"><span data-stu-id="8ea78-108">These steps can be completed using the DEMF dataset.</span></span>


## <a name="modify-format-to-collect-details-of-reporting"></a><span data-ttu-id="8ea78-109">レポートの詳細を収集するために形式を変更する</span><span class="sxs-lookup"><span data-stu-id="8ea78-109">Modify format to collect details of reporting</span></span>
1. <span data-ttu-id="8ea78-110">[組織管理] > [電子申告] > [コンフィギュレーション] に移動します。</span><span class="sxs-lookup"><span data-stu-id="8ea78-110">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="8ea78-111">ツリーで、「イントラスタット (モデル)」を展開します。</span><span class="sxs-lookup"><span data-stu-id="8ea78-111">In the tree, expand 'Intrastat (model)'.</span></span>
3. <span data-ttu-id="8ea78-112">ツリーで、「イントラスタット (モデル)\イントラスタット (形式)」を選択します。</span><span class="sxs-lookup"><span data-stu-id="8ea78-112">In the tree, select 'Intrastat (model)\Intrastat (format)'.</span></span>
4. <span data-ttu-id="8ea78-113">[デザイナー] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8ea78-113">Click Designer.</span></span>
5. <span data-ttu-id="8ea78-114">ツリーで、「ファイル」を展開します。</span><span class="sxs-lookup"><span data-stu-id="8ea78-114">In the tree, expand 'File'.</span></span>
6. <span data-ttu-id="8ea78-115">ツリーで、「ファイル\申告」を展開します。</span><span class="sxs-lookup"><span data-stu-id="8ea78-115">In the tree, expand 'File\Declaration'.</span></span>
7. <span data-ttu-id="8ea78-116">ツリーで、「ファイル\申告\データ」を選択します。</span><span class="sxs-lookup"><span data-stu-id="8ea78-116">In the tree, select 'File\Declaration\Data'.</span></span>
8. <span data-ttu-id="8ea78-117">[多様性] フィールドで、「1 つ、多数」を選択します。</span><span class="sxs-lookup"><span data-stu-id="8ea78-117">In the Multiplicity field, select 'One many'.</span></span>
    * <span data-ttu-id="8ea78-118">この形式要素をコンフィギュレーションして、イントラスタット レポート プロセスの詳細をアーカイブします。</span><span class="sxs-lookup"><span data-stu-id="8ea78-118">Configure this format element to archive details of the Intrastat reporting process.</span></span> <span data-ttu-id="8ea78-119">この項目は、アーカイブのヘッダー レコードを表します。</span><span class="sxs-lookup"><span data-stu-id="8ea78-119">This item represents the archive’s header record.</span></span>  
9. <span data-ttu-id="8ea78-120">ツリーで、「ファイル\申告\データ」を展開します。</span><span class="sxs-lookup"><span data-stu-id="8ea78-120">In the tree, expand 'File\Declaration\Data'.</span></span>
10. <span data-ttu-id="8ea78-121">ツリーで、「ファイル\申告\データ\品目」を選択します。</span><span class="sxs-lookup"><span data-stu-id="8ea78-121">In the tree, select 'File\Declaration\Data\Item'.</span></span>
11. <span data-ttu-id="8ea78-122">[多様性] フィールドで、「ゼロ、多数」を選択します。</span><span class="sxs-lookup"><span data-stu-id="8ea78-122">In the Multiplicity field, select 'Zero many'.</span></span>
    * <span data-ttu-id="8ea78-123">この形式要素をコンフィギュレーションして、イントラスタット レポート プロセスの詳細をアーカイブします。</span><span class="sxs-lookup"><span data-stu-id="8ea78-123">Configure this format element to archive details of the Intrastat reporting process.</span></span> <span data-ttu-id="8ea78-124">この項目は、アーカイブされた明細行のリストを表します。</span><span class="sxs-lookup"><span data-stu-id="8ea78-124">This item will represent the list of archived lines.</span></span>  
12. <span data-ttu-id="8ea78-125">ツリーで、「ファイル\申告\データ\品目」を展開します。</span><span class="sxs-lookup"><span data-stu-id="8ea78-125">In the tree, expand 'File\Declaration\Data\Item'.</span></span>
13. <span data-ttu-id="8ea78-126">ツリーで、「ファイル\申告\データ\品目\Dim1」を選択します。</span><span class="sxs-lookup"><span data-stu-id="8ea78-126">In the tree, select 'File\Declaration\Data\Item\Dim1'.</span></span>
14. <span data-ttu-id="8ea78-127">[除外] フィールドで [はい] を選択します。</span><span class="sxs-lookup"><span data-stu-id="8ea78-127">Select Yes in the Excluded field.</span></span>
    * <span data-ttu-id="8ea78-128">このデータはアーカイブしないので、この形式要素はイントラスタット レポートの詳細のデータ ソースから除外できます。</span><span class="sxs-lookup"><span data-stu-id="8ea78-128">You will not archive this data, so you can exclude this format element from the data source of Intrastat reporting details.</span></span>  
15. <span data-ttu-id="8ea78-129">ツリーで、「ファイル\申告\データ\品目\Dim1」を展開します。</span><span class="sxs-lookup"><span data-stu-id="8ea78-129">In the tree, expand 'File\Declaration\Data\Item\Dim1'.</span></span>
16. <span data-ttu-id="8ea78-130">ツリーで、「ファイル\申告\データ\品目\Dim1\プロパティ」を選択します。</span><span class="sxs-lookup"><span data-stu-id="8ea78-130">In the tree, select 'File\Declaration\Data\Item\Dim1\property'.</span></span>
17. <span data-ttu-id="8ea78-131">[除外] フィールドで [はい] を選択します。</span><span class="sxs-lookup"><span data-stu-id="8ea78-131">Select Yes in the Excluded field.</span></span>
18. <span data-ttu-id="8ea78-132">ツリーで、「ファイル\申告\データ\品目\Dim1\日付」を選択します。</span><span class="sxs-lookup"><span data-stu-id="8ea78-132">In the tree, select 'File\Declaration\Data\Item\Dim1\date'.</span></span>
19. <span data-ttu-id="8ea78-133">[除外] フィールドで [はい] を選択します。</span><span class="sxs-lookup"><span data-stu-id="8ea78-133">Select Yes in the Excluded field.</span></span>
20. <span data-ttu-id="8ea78-134">ツリーで、「ファイル\申告\データ\品目\Dim2」を選択します。</span><span class="sxs-lookup"><span data-stu-id="8ea78-134">In the tree, select 'File\Declaration\Data\Item\Dim2'.</span></span>
21. <span data-ttu-id="8ea78-135">[除外] フィールドで [はい] を選択します。</span><span class="sxs-lookup"><span data-stu-id="8ea78-135">Select Yes in the Excluded field.</span></span>
22. <span data-ttu-id="8ea78-136">ツリーで、「ファイル\申告\データ\品目\Dim2」を展開します。</span><span class="sxs-lookup"><span data-stu-id="8ea78-136">In the tree, expand 'File\Declaration\Data\Item\Dim2'.</span></span>
23. <span data-ttu-id="8ea78-137">ツリーで、「ファイル\申告\データ\品目\Dim2\プロパティ」を選択します。</span><span class="sxs-lookup"><span data-stu-id="8ea78-137">In the tree, select 'File\Declaration\Data\Item\Dim2\property'.</span></span>
24. <span data-ttu-id="8ea78-138">[除外] フィールドで [はい] を選択します。</span><span class="sxs-lookup"><span data-stu-id="8ea78-138">Select Yes in the Excluded field.</span></span>
25. <span data-ttu-id="8ea78-139">ツリーで、「ファイル\申告\データ\品目\Dim2\コード」を選択します。</span><span class="sxs-lookup"><span data-stu-id="8ea78-139">In the tree, select 'File\Declaration\Data\Item\Dim2\code'.</span></span>
26. <span data-ttu-id="8ea78-140">[除外] フィールドで [はい] を選択します。</span><span class="sxs-lookup"><span data-stu-id="8ea78-140">Select Yes in the Excluded field.</span></span>
27. <span data-ttu-id="8ea78-141">ツリーで、「ファイル\申告\データ\品目\Dim3」を選択します。</span><span class="sxs-lookup"><span data-stu-id="8ea78-141">In the tree, select 'File\Declaration\Data\Item\Dim3'.</span></span>
    * <span data-ttu-id="8ea78-142">複数の形式要素に同じ名前を付けることができます。</span><span class="sxs-lookup"><span data-stu-id="8ea78-142">Several format elements can have the same name.</span></span> <span data-ttu-id="8ea78-143">例: Dim。イントラスタット レポートの詳細をアーカイブするためにこの形式をデータ ソースとして使用するときには明示的に認識できないため、これらの形式要素に代替名を定義する必要があります。</span><span class="sxs-lookup"><span data-stu-id="8ea78-143">For example, Dim. You cannot explicitly recognize them when you use this format as a data source for archiving Intrastat reporting details, so you need to define the alternative names for these format elements.</span></span>   
28. <span data-ttu-id="8ea78-144">[名前] フィールドに、「$Amount」と入力します。</span><span class="sxs-lookup"><span data-stu-id="8ea78-144">In the Name field, type 'Amount'.</span></span>
    * <span data-ttu-id="8ea78-145">量</span><span class="sxs-lookup"><span data-stu-id="8ea78-145">Amount</span></span>  
29. <span data-ttu-id="8ea78-146">[多様性] フィールドで、「1 つのみ」を選択します。</span><span class="sxs-lookup"><span data-stu-id="8ea78-146">In the Multiplicity field, select 'Exactly one'.</span></span>
30. <span data-ttu-id="8ea78-147">ツリーで、「ファイル\申告\データ\品目\Dim4」を選択します。</span><span class="sxs-lookup"><span data-stu-id="8ea78-147">In the tree, select 'File\Declaration\Data\Item\Dim4'.</span></span>
31. <span data-ttu-id="8ea78-148">[名前] フィールドに、「Item」と入力します。</span><span class="sxs-lookup"><span data-stu-id="8ea78-148">In the Name field, type 'Item'.</span></span>
    * <span data-ttu-id="8ea78-149">項目</span><span class="sxs-lookup"><span data-stu-id="8ea78-149">Item</span></span>  
32. <span data-ttu-id="8ea78-150">[多様性] フィールドで、「1 つのみ」を選択します。</span><span class="sxs-lookup"><span data-stu-id="8ea78-150">In the Multiplicity field, select 'Exactly one'.</span></span>
    * <span data-ttu-id="8ea78-151">デザイン形式要素に加えて、以下のイントラスタット レポートの詳細をアーカイブする必要があります。レポートされる各商品品目の一意のレコード ID、および生成されるファイルの名前です。</span><span class="sxs-lookup"><span data-stu-id="8ea78-151">In addition to the design format elements, the following Intrastat reporting details must be archived: unique record identification of each reported commodity item and name of the generated file.</span></span> <span data-ttu-id="8ea78-152">このデータはイントラスタット レポートに入力されないため、これらの詳細要素に関連する形式をデータ ソース項目として追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="8ea78-152">Because this data will not be populated in the Intrastat report, you need to add the format that is related to these detail elements as data source items.</span></span>  
33. <span data-ttu-id="8ea78-153">ツリーで、「ファイル\申告\データ」を選択します。</span><span class="sxs-lookup"><span data-stu-id="8ea78-153">In the tree, select 'File\Declaration\Data'.</span></span>
34. <span data-ttu-id="8ea78-154">[追加] をクリックしてドロップ ダイアログを開きます。</span><span class="sxs-lookup"><span data-stu-id="8ea78-154">Click Add to open the drop dialog.</span></span>
35. <span data-ttu-id="8ea78-155">ツリーで、「データ ソース\品目」を選択します。</span><span class="sxs-lookup"><span data-stu-id="8ea78-155">In the tree, select 'Data source\Item'.</span></span>
36. <span data-ttu-id="8ea78-156">[名称] フィールドで、「ファイル名」を入力します。</span><span class="sxs-lookup"><span data-stu-id="8ea78-156">In the Name field, type 'File name'.</span></span>
    * <span data-ttu-id="8ea78-157">ファイル名</span><span class="sxs-lookup"><span data-stu-id="8ea78-157">File name</span></span>  
37. <span data-ttu-id="8ea78-158">[データ タイプ] フィールドで、「文字列」を選択します。</span><span class="sxs-lookup"><span data-stu-id="8ea78-158">In the Data type field, select 'String'.</span></span>
38. <span data-ttu-id="8ea78-159">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8ea78-159">Click OK.</span></span>
39. <span data-ttu-id="8ea78-160">ツリーで、「ファイル\申告\データ\品目」を選択します。</span><span class="sxs-lookup"><span data-stu-id="8ea78-160">In the tree, select 'File\Declaration\Data\Item'.</span></span>
40. <span data-ttu-id="8ea78-161">[品目の追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8ea78-161">Click Add Item.</span></span>
41. <span data-ttu-id="8ea78-162">[名前] フィールドに、「商品 rec id」と入力します。</span><span class="sxs-lookup"><span data-stu-id="8ea78-162">In the Name field, type 'Commodity rec id'.</span></span>
    * <span data-ttu-id="8ea78-163">商品 rec id</span><span class="sxs-lookup"><span data-stu-id="8ea78-163">Commodity rec id</span></span>  
42. <span data-ttu-id="8ea78-164">[データ タイプ] フィールドで、「Int64」を選択します。</span><span class="sxs-lookup"><span data-stu-id="8ea78-164">In the Data type field, select 'Int64'.</span></span>
43. <span data-ttu-id="8ea78-165">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8ea78-165">Click OK.</span></span>
44. <span data-ttu-id="8ea78-166">[マッピング] タブをクリックします。</span><span class="sxs-lookup"><span data-stu-id="8ea78-166">Click the Mapping tab.</span></span>
45. <span data-ttu-id="8ea78-167">ツリーで、「ファイル\申告\データ\ファイル名」を選択します。</span><span class="sxs-lookup"><span data-stu-id="8ea78-167">In the tree, select 'File\Declaration\Data\File name'.</span></span>
46. <span data-ttu-id="8ea78-168">[バインド] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8ea78-168">Click Bind.</span></span>
47. <span data-ttu-id="8ea78-169">ツリーで、「model」を展開します。</span><span class="sxs-lookup"><span data-stu-id="8ea78-169">In the tree, expand 'model'.</span></span>
48. <span data-ttu-id="8ea78-170">ツリーで、「モデル\トランザクション」を展開します。</span><span class="sxs-lookup"><span data-stu-id="8ea78-170">In the tree, expand 'model\Transactions'.</span></span>
49. <span data-ttu-id="8ea78-171">ツリーで、「ファイル\申告\データ\Item = model.Transactions\商品 rec id」を選択します。</span><span class="sxs-lookup"><span data-stu-id="8ea78-171">In the tree, select 'File\Declaration\Data\Item =  model.Transactions\Commodity rec id'.</span></span>
50. <span data-ttu-id="8ea78-172">ツリーで、「モデル\トランザクション\商品 rec id」を選択します。</span><span class="sxs-lookup"><span data-stu-id="8ea78-172">In the tree, select 'model\Transactions\Commodity rec id'.</span></span>
51. <span data-ttu-id="8ea78-173">[バインド] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8ea78-173">Click Bind.</span></span>
52. <span data-ttu-id="8ea78-174">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8ea78-174">Click Save.</span></span>

## <a name="modify-format-to-memorize-details-of-reporting"></a><span data-ttu-id="8ea78-175">レポートの詳細を記憶するために形式を変更する</span><span class="sxs-lookup"><span data-stu-id="8ea78-175">Modify format to memorize details of reporting</span></span>
1. <span data-ttu-id="8ea78-176">[形式をモデルにマップ] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8ea78-176">Click Map format to model.</span></span>
2. <span data-ttu-id="8ea78-177">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8ea78-177">Click New.</span></span>
3. <span data-ttu-id="8ea78-178">[定義] フィールドで、「アプリケーション データの更新用」ルート項目を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="8ea78-178">In the Definition field, enter or select the ‘For application data update’ root item.</span></span>
    * <span data-ttu-id="8ea78-179">アプリケーション データの更新用</span><span class="sxs-lookup"><span data-stu-id="8ea78-179">For application data update</span></span>  
4. <span data-ttu-id="8ea78-180">[名前] フィールドで、「データを更新するためのマッピング」と入力します。</span><span class="sxs-lookup"><span data-stu-id="8ea78-180">In the Name field, type 'Mapping to update data'.</span></span>
    * <span data-ttu-id="8ea78-181">データを更新するためのマッピング</span><span class="sxs-lookup"><span data-stu-id="8ea78-181">Mapping to update data</span></span>  
5. <span data-ttu-id="8ea78-182">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8ea78-182">Click Save.</span></span>
    * <span data-ttu-id="8ea78-183">このマッピングは、データ モデル内でイントラスタット レポートの詳細をどのように収集するかを定義します。その構造は、選択したルート項目「アプリケーション データの更新用」によって指定されます。</span><span class="sxs-lookup"><span data-stu-id="8ea78-183">This mapping defines how the details of the Intrastat report are collected in the data model, the structure of which is specified by the selected root item ‘For application data update’.</span></span> <span data-ttu-id="8ea78-184">これらの詳細、同じルート項目「アプリケーション データ更新用」のモデル マッピング、および方向「宛先」は、アプリケーション データの更新に使用されます。</span><span class="sxs-lookup"><span data-stu-id="8ea78-184">These details, the model mapping with same root item ‘For application data update’, and the direction ‘To destination’ will be used for the application data update.</span></span> <span data-ttu-id="8ea78-185">アプリケーション データの更新は、送信するイントラスタット レポートの生成後すぐに開始します。</span><span class="sxs-lookup"><span data-stu-id="8ea78-185">The application data update starts immediately after the outgoing Intrastat report is generated.</span></span> <span data-ttu-id="8ea78-186">アプリケーション データの更新は実行時にスキップできますが、データ モデルは空でなければならないことに注意してください (空のレコード リストを含みます)。</span><span class="sxs-lookup"><span data-stu-id="8ea78-186">Note that the application data update can be skipped at run-time, but the data model must be empty (containing empty record list).</span></span>   
6. <span data-ttu-id="8ea78-187">[デザイナー] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8ea78-187">Click Designer.</span></span>
    * <span data-ttu-id="8ea78-188">送信するイントラスタット レポート形式が、このモデル マッピングのデータ ソースとしてデフォルトで追加されていることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="8ea78-188">Note that the outgoing Intrastat report format is added by default as a data source for this model mapping.</span></span>  
    * <span data-ttu-id="8ea78-189">選択したモデルのルート項目に基づいてフィルタ処理されたデータ モデルの要素に、設計されたレポートの要素 (データ ソースとして提示) をバインドします。</span><span class="sxs-lookup"><span data-stu-id="8ea78-189">Bind elements of the designed report (presented as data source) to elements of the data model, which is filtered based on the selected model’s root item.</span></span>  
7. <span data-ttu-id="8ea78-190">ツリーで、「アーカイブ ヘッダー」を展開します。</span><span class="sxs-lookup"><span data-stu-id="8ea78-190">In the tree, expand 'Archive header'.</span></span>
8. <span data-ttu-id="8ea78-191">ツリーで、「アーカイブ ヘッダー\アーカイブ明細行」を展開します。</span><span class="sxs-lookup"><span data-stu-id="8ea78-191">In the tree, expand 'Archive header\Archive lines'.</span></span>
9. <span data-ttu-id="8ea78-192">ツリーで、「形式」を展開します。</span><span class="sxs-lookup"><span data-stu-id="8ea78-192">In the tree, expand 'format'.</span></span>
10. <span data-ttu-id="8ea78-193">ツリーで、「形式\Declaration: XML Element(Declaration)」を展開します。</span><span class="sxs-lookup"><span data-stu-id="8ea78-193">In the tree, expand 'format\Declaration: XML Element(Declaration)'.</span></span>
11. <span data-ttu-id="8ea78-194">ツリーで、「形式\Declaration: XML Element(Declaration)\Data: XML Element 1..* (Data)」を展開します。</span><span class="sxs-lookup"><span data-stu-id="8ea78-194">In the tree, expand 'format\Declaration: XML Element(Declaration)\Data: XML Element 1..* (Data)'.</span></span>
12. <span data-ttu-id="8ea78-195">ツリーで、「形式\Declaration: XML Element(Declaration)\Data: XML Element 1..* (Data)\Item: XML Element 0..* (Item)」を展開します。</span><span class="sxs-lookup"><span data-stu-id="8ea78-195">In the tree, expand 'format\Declaration: XML Element(Declaration)\Data: XML Element 1..* (Data)\Item: XML Element 0..* (Item)'.</span></span>
13. <span data-ttu-id="8ea78-196">ツリーで、「形式\Declaration: XML Element(Declaration)\Data: XML Element 1..* (Data)\Item: XML Element 0..* (Item)\Dim3: XML Element 1..1 (Amount)」を展開します。</span><span class="sxs-lookup"><span data-stu-id="8ea78-196">In the tree, expand 'format\Declaration: XML Element(Declaration)\Data: XML Element 1..* (Data)\Item: XML Element 0..* (Item)\Dim3: XML Element 1..1 (Amount)'.</span></span>
14. <span data-ttu-id="8ea78-197">ツリーで、「形式\Declaration: XML Element(Declaration)\Data: XML Element 1..* (Data)\Item: XML Element 0..* (Item)\Dim4: XML Element 1..1 (Item)」を展開します。</span><span class="sxs-lookup"><span data-stu-id="8ea78-197">In the tree, expand 'format\Declaration: XML Element(Declaration)\Data: XML Element 1..* (Data)\Item: XML Element 0..* (Item)\Dim4: XML Element 1..1 (Item)'.</span></span>
15. <span data-ttu-id="8ea78-198">ツリーで、「アーカイブ ヘッダー\行数」を選択します。</span><span class="sxs-lookup"><span data-stu-id="8ea78-198">In the tree, select 'Archive header\Number of lines'.</span></span>
16. <span data-ttu-id="8ea78-199">[編集] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8ea78-199">Click Edit.</span></span>
17. <span data-ttu-id="8ea78-200">ツリーで、「リスト\COUNT」を選択します。</span><span class="sxs-lookup"><span data-stu-id="8ea78-200">In the tree, select 'List\COUNT'.</span></span>
18. <span data-ttu-id="8ea78-201">[機能の追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8ea78-201">Click Add function.</span></span>
19. <span data-ttu-id="8ea78-202">ツリーで、「形式」を展開します。</span><span class="sxs-lookup"><span data-stu-id="8ea78-202">In the tree, expand 'format'.</span></span>
20. <span data-ttu-id="8ea78-203">ツリーで、「形式\Declaration: XML Element(Declaration)」を展開します。</span><span class="sxs-lookup"><span data-stu-id="8ea78-203">In the tree, expand 'format\Declaration: XML Element(Declaration)'.</span></span>
21. <span data-ttu-id="8ea78-204">ツリーで、「形式\Declaration: XML Element(Declaration)\Data: XML Element 1..* (Data)」を展開します。</span><span class="sxs-lookup"><span data-stu-id="8ea78-204">In the tree, expand 'format\Declaration: XML Element(Declaration)\Data: XML Element 1..* (Data)'.</span></span>
22. <span data-ttu-id="8ea78-205">ツリーで、「形式\Declaration: XML Element(Declaration)\Data: XML Element 1..* (Data)\Item: XML Element 0..* (Item)」を選択します。</span><span class="sxs-lookup"><span data-stu-id="8ea78-205">In the tree, select 'format\Declaration: XML Element(Declaration)\Data: XML Element 1..* (Data)\Item: XML Element 0..* (Item)'.</span></span>
23. <span data-ttu-id="8ea78-206">[データ ソースの追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8ea78-206">Click Add data source.</span></span>
24. <span data-ttu-id="8ea78-207">[フォーミュラ] フィールドに、「COUNT(format.Declaration.Data.Item)」と入力します。</span><span class="sxs-lookup"><span data-stu-id="8ea78-207">In the Formula field, enter 'COUNT(format.Declaration.Data.Item)'.</span></span>
    * <span data-ttu-id="8ea78-208">COUNT(format.Declaration.Data.Item)</span><span class="sxs-lookup"><span data-stu-id="8ea78-208">COUNT(format.Declaration.Data.Item)</span></span>  
25. <span data-ttu-id="8ea78-209">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8ea78-209">Click Save.</span></span>
26. <span data-ttu-id="8ea78-210">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="8ea78-210">Close the page.</span></span>
27. <span data-ttu-id="8ea78-211">ツリーで、「アーカイブ ヘッダー\ファイル名」を選択します。</span><span class="sxs-lookup"><span data-stu-id="8ea78-211">In the tree, select 'Archive header\File name'.</span></span>
28. <span data-ttu-id="8ea78-212">ツリーで、「形式\Declaration: XML Element(Declaration)\Data: XML Element 1..* (Data)\File name: Item String(File name)」を選択します。</span><span class="sxs-lookup"><span data-stu-id="8ea78-212">In the tree, select 'format\Declaration: XML Element(Declaration)\Data: XML Element 1..* (Data)\File name: Item String(File name)'.</span></span>
29. <span data-ttu-id="8ea78-213">[バインド] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8ea78-213">Click Bind.</span></span>
30. <span data-ttu-id="8ea78-214">ツリーで、「形式\Declaration: XML Element(Declaration)\Data: XML Element 1..* (Data)\Item: XML Element 0..* (Item)\Dim4: XML Element 1..1 (Item)\number: String(number)」を選択します。</span><span class="sxs-lookup"><span data-stu-id="8ea78-214">In the tree, select 'format\Declaration: XML Element(Declaration)\Data: XML Element 1..* (Data)\Item: XML Element 0..* (Item)\Dim4: XML Element 1..1 (Item)\number: String(number)'.</span></span>
31. <span data-ttu-id="8ea78-215">ツリーで、「アーカイブ ヘッダー\アーカイブ明細行\品目番号」を選択します。</span><span class="sxs-lookup"><span data-stu-id="8ea78-215">In the tree, select 'Archive header\Archive lines\Item number'.</span></span>
32. <span data-ttu-id="8ea78-216">[バインド] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8ea78-216">Click Bind.</span></span>
33. <span data-ttu-id="8ea78-217">ツリーで、「形式\Declaration: XML Element(Declaration)\Data: XML Element 1..* (Data)\Item: XML Element 0..* (Item)\Dim3: XML Element 1..1 (Amount)\value: Numeric Real(value)」を選択します。</span><span class="sxs-lookup"><span data-stu-id="8ea78-217">In the tree, select 'format\Declaration: XML Element(Declaration)\Data: XML Element 1..* (Data)\Item: XML Element 0..* (Item)\Dim3: XML Element 1..1 (Amount)\value: Numeric Real(value)'.</span></span>
34. <span data-ttu-id="8ea78-218">ツリーで、「アーカイブ ヘッダー\アーカイブ明細行\金額」を選択します。</span><span class="sxs-lookup"><span data-stu-id="8ea78-218">In the tree, select 'Archive header\Archive lines\Amount'.</span></span>
35. <span data-ttu-id="8ea78-219">[バインド] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8ea78-219">Click Bind.</span></span>
36. <span data-ttu-id="8ea78-220">ツリーで、「形式\Declaration: XML Element(Declaration)\Data: XML Element 1..* (Data)\Item: XML Element 0..* (Item)\Commodity rec id: Item Int64(Commodity rec id)」を選択します。</span><span class="sxs-lookup"><span data-stu-id="8ea78-220">In the tree, select 'format\Declaration: XML Element(Declaration)\Data: XML Element 1..* (Data)\Item: XML Element 0..* (Item)\Commodity rec id: Item Int64(Commodity rec id)'.</span></span>
37. <span data-ttu-id="8ea78-221">ツリーで、「アーカイブ ヘッダー\アーカイブ明細行\商品 rec id」を選択します。</span><span class="sxs-lookup"><span data-stu-id="8ea78-221">In the tree, select 'Archive header\Archive lines\Commodity rec id'.</span></span>
38. <span data-ttu-id="8ea78-222">[バインド] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8ea78-222">Click Bind.</span></span>
39. <span data-ttu-id="8ea78-223">ツリーで、「アーカイブ ヘッダー\アーカイブ明細行」を選択します。</span><span class="sxs-lookup"><span data-stu-id="8ea78-223">In the tree, select 'Archive header\Archive lines'.</span></span>
40. <span data-ttu-id="8ea78-224">ツリーで、「形式\Declaration: XML Element(Declaration)\Data: XML Element 1..* (Data)\Item: XML Element 0..* (Item)」を選択します。</span><span class="sxs-lookup"><span data-stu-id="8ea78-224">In the tree, select 'format\Declaration: XML Element(Declaration)\Data: XML Element 1..* (Data)\Item: XML Element 0..* (Item)'.</span></span>
41. <span data-ttu-id="8ea78-225">[バインド] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8ea78-225">Click Bind.</span></span>
42. <span data-ttu-id="8ea78-226">ツリーで、「アーカイブ ヘッダー」を選択します。</span><span class="sxs-lookup"><span data-stu-id="8ea78-226">In the tree, select 'Archive header'.</span></span>
43. <span data-ttu-id="8ea78-227">ツリーで、「形式\Declaration: XML Element(Declaration)\Data: XML Element 1..* (Data)」を選択します。</span><span class="sxs-lookup"><span data-stu-id="8ea78-227">In the tree, select 'format\Declaration: XML Element(Declaration)\Data: XML Element 1..* (Data)'.</span></span>
44. <span data-ttu-id="8ea78-228">[バインド] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8ea78-228">Click Bind.</span></span>
45. <span data-ttu-id="8ea78-229">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="8ea78-229">Click Save.</span></span>
46. <span data-ttu-id="8ea78-230">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="8ea78-230">Close the page.</span></span>
47. <span data-ttu-id="8ea78-231">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="8ea78-231">Close the page.</span></span>
48. <span data-ttu-id="8ea78-232">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="8ea78-232">Close the page.</span></span>


