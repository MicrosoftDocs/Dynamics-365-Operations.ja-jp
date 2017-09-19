--- 
title: "電子申告 (ER) のアプリケーション データ更新と共にドキュメントを生成するためのモデルとマッピングの変更"
description: "この手順のステップを完了するには、まず「ER アプリケーション データ更新と共にドキュメントを生成する (パート 2 - ドキュメントの生成)」の手順を完了する必要があります。"
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
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: aa173138eaf0178f2a942a88eafe80d4bac4d6a8
ms.contentlocale: ja-jp
ms.lasthandoff: 08/29/2017

---
# <a name="modify-model-and-mapping-to-generate-documents-with-application-data-update-for-electronic-reporting-er"></a><span data-ttu-id="b4864-103">電子申告 (ER) のアプリケーション データ更新と共にドキュメントを生成するためのモデルとマッピングの変更</span><span class="sxs-lookup"><span data-stu-id="b4864-103">Modify model and mapping to generate documents with application data update for electronic reporting (ER)</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="b4864-104">この手順のステップを完了するには、まず「ER アプリケーション データ更新と共にドキュメントを生成する (パート 2: ドキュメントの生成)」の手順を完了する必要があります。</span><span class="sxs-lookup"><span data-stu-id="b4864-104">To complete the steps in this procedure, you must first complete the procedure, “ER Generate documents with application data update (Part 2: Generate documents)”.</span></span> 

<span data-ttu-id="b4864-105">この手順のステップでは、電子ドキュメントを生成してアプリケーション データを更新するために電子申告 (ER) コンフィギュレーションを設計する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="b4864-105">The steps in this procedure explain how to design Electronic reporting (ER) configurations to generate an electronic document and update application data.</span></span> <span data-ttu-id="b4864-106">この手順では、ER コンフィギュレーションを変更し、その使用を開始して、電子ドキュメントを生成しアプリケーション データを更新します。</span><span class="sxs-lookup"><span data-stu-id="b4864-106">In this procedure, you will modify the ER configurations to start using them to generate electronic documents and update application data.</span></span> <span data-ttu-id="b4864-107">この手順は、「システム管理者」または「電子レポート開発者」ロールが割り当てられているユーザー用に作成されています。</span><span class="sxs-lookup"><span data-stu-id="b4864-107">This procedure is created for users with the assigned role of system administrator or electronic reporting developer.</span></span> <span data-ttu-id="b4864-108">これらのステップは、DEMF データ セットを使用して完了することができます。</span><span class="sxs-lookup"><span data-stu-id="b4864-108">These steps can be completed using the DEMF dataset.</span></span>


## <a name="modify-data-model"></a><span data-ttu-id="b4864-109">データ モデルの変更</span><span class="sxs-lookup"><span data-stu-id="b4864-109">Modify data model</span></span>
1. <span data-ttu-id="b4864-110">[組織管理] > [電子申告] > [コンフィギュレーション] に移動します。</span><span class="sxs-lookup"><span data-stu-id="b4864-110">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="b4864-111">ツリーで、「イントラスタット (モデル)」を選択します。</span><span class="sxs-lookup"><span data-stu-id="b4864-111">In the tree, select 'Intrastat (model)'.</span></span>
    * <span data-ttu-id="b4864-112">データ モデルを使用する方法を拡張します。</span><span class="sxs-lookup"><span data-stu-id="b4864-112">You will extend how you use the data model.</span></span> <span data-ttu-id="b4864-113">データ モデルは、イントラスタット レポートを生成するデータ ソースとして使用するだけでなく、イントラスタット レポート プロセスに関する詳細を収集するためにも使用します。</span><span class="sxs-lookup"><span data-stu-id="b4864-113">Besides using it as data source to generate the Intrastat report, the data model will be used to collect details about the Intrastat reporting process.</span></span> <span data-ttu-id="b4864-114">その詳細は、アプリケーション データの更新に使用されます。</span><span class="sxs-lookup"><span data-stu-id="b4864-114">The details will then be used to update application data.</span></span>   
3. <span data-ttu-id="b4864-115">[デザイナー] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b4864-115">Click Designer.</span></span>
4. <span data-ttu-id="b4864-116">[新規] をクリックすると、ドロップ ダイアログが開きます。</span><span class="sxs-lookup"><span data-stu-id="b4864-116">Click New to open the drop dialog.</span></span>
5. <span data-ttu-id="b4864-117">[新しいノード] フィールドに、「モデル ルート」を入力します。</span><span class="sxs-lookup"><span data-stu-id="b4864-117">In the New node as a field, enter 'Model root'.</span></span>
6. <span data-ttu-id="b4864-118">[名前] フィールドに、「アプリケーション データの更新用」と入力します。</span><span class="sxs-lookup"><span data-stu-id="b4864-118">In the Name field, type 'For application data update'.</span></span>
    * <span data-ttu-id="b4864-119">アプリケーション データの更新用</span><span class="sxs-lookup"><span data-stu-id="b4864-119">For application data update</span></span>  
7. <span data-ttu-id="b4864-120">[追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b4864-120">Click Add.</span></span>
8. <span data-ttu-id="b4864-121">ツリーで、「アプリケーション データの更新用」を選択します。</span><span class="sxs-lookup"><span data-stu-id="b4864-121">In the tree, select 'For application data update'.</span></span>
    * <span data-ttu-id="b4864-122">この新しいルート項目は、イントラスタット レポート (データ ソースとして使用) からアプリケーション テーブル (更新先) にデータを移動するためのデータ フローを指定するために追加されます。</span><span class="sxs-lookup"><span data-stu-id="b4864-122">This new root item is added to specify the data flow for moving data from the Intrastat report (used as a data source) to the application tables (the update destination).</span></span> <span data-ttu-id="b4864-123">送信文書に投稿されるデータを取得したり、アプリケーション データを更新するために使用される文書からデータを取得するには、異なるルート項目を使用する必要があることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="b4864-123">Note that different root items must be used for getting data that is posted to the outgoing document and for getting data from the document that is used to update application data.</span></span>   
9. <span data-ttu-id="b4864-124">[新規] をクリックすると、ドロップ ダイアログが開きます。</span><span class="sxs-lookup"><span data-stu-id="b4864-124">Click New to open the drop dialog.</span></span>
10. <span data-ttu-id="b4864-125">[名前] フィールドに、「アーカイブ ヘッダー」と入力します。</span><span class="sxs-lookup"><span data-stu-id="b4864-125">In the Name field, type 'Archive header'.</span></span>
    * <span data-ttu-id="b4864-126">アーカイブ ヘッダー</span><span class="sxs-lookup"><span data-stu-id="b4864-126">Archive header</span></span>  
11. <span data-ttu-id="b4864-127">[品目タイプ] フィールドで、「レコード リスト」を選択します。</span><span class="sxs-lookup"><span data-stu-id="b4864-127">In the Item type field, select 'Record list'.</span></span>
12. <span data-ttu-id="b4864-128">[追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b4864-128">Click Add.</span></span>
    * <span data-ttu-id="b4864-129">生成されるそれぞれのイントラスタット レポートにレコードを作成するので、そのための新しい品目を作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="b4864-129">Because you will create a record for each Intrastat report that is generated, you must create a new item for that.</span></span>  
13. <span data-ttu-id="b4864-130">[新規] をクリックすると、ドロップ ダイアログが開きます。</span><span class="sxs-lookup"><span data-stu-id="b4864-130">Click New to open the drop dialog.</span></span>
14. <span data-ttu-id="b4864-131">[名称] フィールドで、「ファイル名」を入力します。</span><span class="sxs-lookup"><span data-stu-id="b4864-131">In the Name field, type 'File name'.</span></span>
    * <span data-ttu-id="b4864-132">ファイル名</span><span class="sxs-lookup"><span data-stu-id="b4864-132">File name</span></span>  
15. <span data-ttu-id="b4864-133">[品目タイプ] フィールドで、「String」を選択します。</span><span class="sxs-lookup"><span data-stu-id="b4864-133">In the Item type field, select 'String'.</span></span>
16. <span data-ttu-id="b4864-134">[追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b4864-134">Click Add.</span></span>
17. <span data-ttu-id="b4864-135">[新規] をクリックすると、ドロップ ダイアログが開きます。</span><span class="sxs-lookup"><span data-stu-id="b4864-135">Click New to open the drop dialog.</span></span>
18. <span data-ttu-id="b4864-136">[名前] フィールドに、「行数」と入力します。</span><span class="sxs-lookup"><span data-stu-id="b4864-136">In the Name field, type 'Number of lines'.</span></span>
    * <span data-ttu-id="b4864-137">ライン数</span><span class="sxs-lookup"><span data-stu-id="b4864-137">Number of lines</span></span>  
19. <span data-ttu-id="b4864-138">[項目タイプ] フィールドで、「整数」を選択します。</span><span class="sxs-lookup"><span data-stu-id="b4864-138">In the Item type field, select 'Integer'.</span></span>
20. <span data-ttu-id="b4864-139">[追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b4864-139">Click Add.</span></span>
    * <span data-ttu-id="b4864-140">現在のレポート プロセス中にレポートされたイントラスタット トランザクションの数を表すために、この品目を追加します。</span><span class="sxs-lookup"><span data-stu-id="b4864-140">Add this item to represent the number of Intrastat transactions that are reported during the current reporting process.</span></span>  
21. <span data-ttu-id="b4864-141">[新規] をクリックすると、ドロップ ダイアログが開きます。</span><span class="sxs-lookup"><span data-stu-id="b4864-141">Click New to open the drop dialog.</span></span>
22. <span data-ttu-id="b4864-142">[名前] フィールドに、「アーカイブ明細行」と入力します。</span><span class="sxs-lookup"><span data-stu-id="b4864-142">In the Name field, type 'Archive lines'.</span></span>
    * <span data-ttu-id="b4864-143">アーカイブ明細行</span><span class="sxs-lookup"><span data-stu-id="b4864-143">Archive lines</span></span>  
23. <span data-ttu-id="b4864-144">[品目タイプ] フィールドで、「レコード リスト」を選択します。</span><span class="sxs-lookup"><span data-stu-id="b4864-144">In the Item type field, select 'Record list'.</span></span>
24. <span data-ttu-id="b4864-145">[追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b4864-145">Click Add.</span></span>
    * <span data-ttu-id="b4864-146">現在のレポート プロセス中にレポートされたイントラスタット トランザクションのリストを表すために、この品目を追加します。</span><span class="sxs-lookup"><span data-stu-id="b4864-146">Add this item to represent the list of Intrastat transactions that are reported during the current reporting process.</span></span>  
25. <span data-ttu-id="b4864-147">[新規] をクリックすると、ドロップ ダイアログが開きます。</span><span class="sxs-lookup"><span data-stu-id="b4864-147">Click New to open the drop dialog.</span></span>
26. <span data-ttu-id="b4864-148">[名前] フィールドに、「$Amount」と入力します。</span><span class="sxs-lookup"><span data-stu-id="b4864-148">In the Name field, type 'Amount'.</span></span>
    * <span data-ttu-id="b4864-149">量</span><span class="sxs-lookup"><span data-stu-id="b4864-149">Amount</span></span>  
27. <span data-ttu-id="b4864-150">[品目タイプ] フィールドで、「実数」を選択します。</span><span class="sxs-lookup"><span data-stu-id="b4864-150">In the Item type field, select 'Real'.</span></span>
28. <span data-ttu-id="b4864-151">[追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b4864-151">Click Add.</span></span>
29. <span data-ttu-id="b4864-152">[新規] をクリックすると、ドロップ ダイアログが開きます。</span><span class="sxs-lookup"><span data-stu-id="b4864-152">Click New to open the drop dialog.</span></span>
30. <span data-ttu-id="b4864-153">[名前] フィールドに、「商品 rec id」と入力します。</span><span class="sxs-lookup"><span data-stu-id="b4864-153">In the Name field, type 'Commodity rec id'.</span></span>
    * <span data-ttu-id="b4864-154">商品 rec id</span><span class="sxs-lookup"><span data-stu-id="b4864-154">Commodity rec id</span></span>  
31. <span data-ttu-id="b4864-155">[項目タイプ] フィールドで、「Int64」を選択します。</span><span class="sxs-lookup"><span data-stu-id="b4864-155">In the Item type field, select 'Int64'.</span></span>
32. <span data-ttu-id="b4864-156">[追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b4864-156">Click Add.</span></span>
33. <span data-ttu-id="b4864-157">[新規] をクリックすると、ドロップ ダイアログが開きます。</span><span class="sxs-lookup"><span data-stu-id="b4864-157">Click New to open the drop dialog.</span></span>
34. <span data-ttu-id="b4864-158">[名前] フィールドに、「品目番号」と入力します。</span><span class="sxs-lookup"><span data-stu-id="b4864-158">In the Name field, type 'Item number'.</span></span>
    * <span data-ttu-id="b4864-159">品目番号</span><span class="sxs-lookup"><span data-stu-id="b4864-159">Item number</span></span>  
35. <span data-ttu-id="b4864-160">[品目タイプ] フィールドで、「String」を選択します。</span><span class="sxs-lookup"><span data-stu-id="b4864-160">In the Item type field, select 'String'.</span></span>
36. <span data-ttu-id="b4864-161">[追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b4864-161">Click Add.</span></span>
37. <span data-ttu-id="b4864-162">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b4864-162">Click Save.</span></span>
38. <span data-ttu-id="b4864-163">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="b4864-163">Close the page.</span></span>

## <a name="modify-model-mapping"></a><span data-ttu-id="b4864-164">モデル マッピングの変更</span><span class="sxs-lookup"><span data-stu-id="b4864-164">Modify model mapping</span></span>
1. <span data-ttu-id="b4864-165">ツリーで、「イントラスタット (モデル)」を展開します。</span><span class="sxs-lookup"><span data-stu-id="b4864-165">In the tree, expand 'Intrastat (model)'.</span></span>
2. <span data-ttu-id="b4864-166">ツリーで、「イントラスタット (モデル)\イントラスタット (マッピング)」を選択します。</span><span class="sxs-lookup"><span data-stu-id="b4864-166">In the tree, select 'Intrastat (model)\Intrastat (mapping)'.</span></span>
    * <span data-ttu-id="b4864-167">既存のモデルマッピングを変更して、アプリケーションデータの更新への使用を開始し、イントラスタット レポートの詳細をアーカイブします。</span><span class="sxs-lookup"><span data-stu-id="b4864-167">Modify the existing model mapping to start using it for  the application data update and to archive Intrastat reporting details.</span></span>  
3. <span data-ttu-id="b4864-168">[デザイナー] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b4864-168">Click Designer.</span></span>
4. <span data-ttu-id="b4864-169">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b4864-169">Click New.</span></span>
5. <span data-ttu-id="b4864-170">[名前] フィールドに、「アーカイブの更新」と入力します。</span><span class="sxs-lookup"><span data-stu-id="b4864-170">In the Name field, type 'Update archive'.</span></span>
    * <span data-ttu-id="b4864-171">アーカイブの更新</span><span class="sxs-lookup"><span data-stu-id="b4864-171">Update archive</span></span>  
6. <span data-ttu-id="b4864-172">[方向] フィールドで、「宛先」を選択します。</span><span class="sxs-lookup"><span data-stu-id="b4864-172">In the Direction field, select 'To destination'.</span></span>
7. <span data-ttu-id="b4864-173">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b4864-173">Click Save.</span></span>
    * <span data-ttu-id="b4864-174">この新しいマッピングは、データ モデルからアプリケーション テーブル (更新先) にデータ (イントラスタット レポートの詳細) を移動するためのデータ フローを指定します。</span><span class="sxs-lookup"><span data-stu-id="b4864-174">This new mapping specifies the data flow for moving data (Intrastat reporting details) from the data model to the application tables (the update destination).</span></span> <span data-ttu-id="b4864-175">レポート プロセスのためにアプリケーションからデータを取得し、アプリケーション データ更新のためにデータ モデルのデータを使用するには、異なるモデルのルート項目を使用する必要があることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="b4864-175">Note that different model’s root items must be used to get data from the application for the reporting process and then use the data from data model for the application data update.</span></span>   
8. <span data-ttu-id="b4864-176">[デザイナー] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b4864-176">Click Designer.</span></span>
9. <span data-ttu-id="b4864-177">ツリーで、「データ モデル\データ モデル」を選択します。</span><span class="sxs-lookup"><span data-stu-id="b4864-177">In the tree, select 'Data model\Data model'.</span></span>
    * <span data-ttu-id="b4864-178">必要なデータ ソースを追加します。</span><span class="sxs-lookup"><span data-stu-id="b4864-178">Add the required data source.</span></span> <span data-ttu-id="b4864-179">これは、アーカイブする必要のあるレポートされたイントラスタット トランザクションの詳細を含むデータ モデルです。</span><span class="sxs-lookup"><span data-stu-id="b4864-179">This is the data model that contains details of the reported Intrastat transactions that must be archived.</span></span>  
10. <span data-ttu-id="b4864-180">[ルートの追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b4864-180">Click Add root.</span></span>
11. <span data-ttu-id="b4864-181">[名前] フィールドに、「モデル」と入力します。</span><span class="sxs-lookup"><span data-stu-id="b4864-181">In the Name field, type 'model'.</span></span>
    * <span data-ttu-id="b4864-182">モデル</span><span class="sxs-lookup"><span data-stu-id="b4864-182">model</span></span>  
12. <span data-ttu-id="b4864-183">[定義] フィールドで、「アプリケーション データの更新用」という値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="b4864-183">In the Definition field, enter or select the value ‘For application data update’.</span></span>
    * <span data-ttu-id="b4864-184">アプリケーション データの更新用</span><span class="sxs-lookup"><span data-stu-id="b4864-184">For application data update</span></span>  
13. <span data-ttu-id="b4864-185">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b4864-185">Click OK.</span></span>
14. <span data-ttu-id="b4864-186">ツリーで、「model」を展開します。</span><span class="sxs-lookup"><span data-stu-id="b4864-186">In the tree, expand 'model'.</span></span>
15. <span data-ttu-id="b4864-187">ツリーで、[Functions\Calculated field] を選択します。</span><span class="sxs-lookup"><span data-stu-id="b4864-187">In the tree, select 'Functions\Calculated field'.</span></span>
16. <span data-ttu-id="b4864-188">ツリーで、「モデル\アーカイブ ヘッダー」を選択します。</span><span class="sxs-lookup"><span data-stu-id="b4864-188">In the tree, select 'model\Archive header'.</span></span>
17. <span data-ttu-id="b4864-189">[追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b4864-189">Click Add.</span></span>
    * <span data-ttu-id="b4864-190">アーカイブ用にレポート済イントラスタット トランザクションを列挙するため、適切なデータ ソースを追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="b4864-190">Because you want to enumerate reported Intrastat transactions for archiving, the appropriate data source must be added.</span></span>  
18. <span data-ttu-id="b4864-191">[名前] フィールドに、「列挙された明細行」と入力します。</span><span class="sxs-lookup"><span data-stu-id="b4864-191">In the Name field, type 'Enumerated lines'.</span></span>
    * <span data-ttu-id="b4864-192">列挙された明細行</span><span class="sxs-lookup"><span data-stu-id="b4864-192">Enumerated lines</span></span>  
19. <span data-ttu-id="b4864-193">[式の編集] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b4864-193">Click Edit formula.</span></span>
20. <span data-ttu-id="b4864-194">ツリーで、「リスト\ENUMERATE」を選択します。</span><span class="sxs-lookup"><span data-stu-id="b4864-194">In the tree, select 'List\ENUMERATE'.</span></span>
21. <span data-ttu-id="b4864-195">[機能の追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b4864-195">Click Add function.</span></span>
22. <span data-ttu-id="b4864-196">ツリーで、「model」を展開します。</span><span class="sxs-lookup"><span data-stu-id="b4864-196">In the tree, expand 'model'.</span></span>
23. <span data-ttu-id="b4864-197">ツリーで、「モデル\アーカイブ ヘッダー」を展開します。</span><span class="sxs-lookup"><span data-stu-id="b4864-197">In the tree, expand 'model\Archive header'.</span></span>
24. <span data-ttu-id="b4864-198">ツリーで、「モデル\アーカイブ ヘッダー\アーカイブ明細行」を選択します。</span><span class="sxs-lookup"><span data-stu-id="b4864-198">In the tree, select 'model\Archive header\Archive lines'.</span></span>
25. <span data-ttu-id="b4864-199">[データ ソースの追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b4864-199">Click Add data source.</span></span>
26. <span data-ttu-id="b4864-200">[フォーミュラ] フィールドに、「ENUMERATE(model.'Archive header'.'Archive lines')」と入力します。</span><span class="sxs-lookup"><span data-stu-id="b4864-200">In the Formula field, enter 'ENUMERATE(model.'Archive header'.'Archive lines')'.</span></span>
    * <span data-ttu-id="b4864-201">ENUMERATE(model.'Archive header'.'Archive lines')</span><span class="sxs-lookup"><span data-stu-id="b4864-201">ENUMERATE(model.'Archive header'.'Archive lines')</span></span>  
27. <span data-ttu-id="b4864-202">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b4864-202">Click Save.</span></span>
28. <span data-ttu-id="b4864-203">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="b4864-203">Close the page.</span></span>
29. <span data-ttu-id="b4864-204">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b4864-204">Click OK.</span></span>
30. <span data-ttu-id="b4864-205">[宛先の追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b4864-205">Click Add destination.</span></span>
    * <span data-ttu-id="b4864-206">レポート済のイントラスタット トランザクションの詳細をアーカイブするために更新を必要とする必要な出力先として、アプリケーション テーブルを追加します。</span><span class="sxs-lookup"><span data-stu-id="b4864-206">Add application tables as required destinations that require updates to archive details of reported Intrastat transactions.</span></span>  
31. <span data-ttu-id="b4864-207">[名前] フィールドに、「アーカイブ」と入力します。</span><span class="sxs-lookup"><span data-stu-id="b4864-207">In the Name field, type 'Archive'.</span></span>
    * <span data-ttu-id="b4864-208">アーカイブ</span><span class="sxs-lookup"><span data-stu-id="b4864-208">Archive</span></span>  
32. <span data-ttu-id="b4864-209">[テーブル名] フィールドで、「IntrastatArchiveGeneral」と入力します。</span><span class="sxs-lookup"><span data-stu-id="b4864-209">In the Table name field, type 'IntrastatArchiveGeneral'.</span></span>
    * <span data-ttu-id="b4864-210">IntrastatArchiveGeneral</span><span class="sxs-lookup"><span data-stu-id="b4864-210">IntrastatArchiveGeneral</span></span>  
    * <span data-ttu-id="b4864-211">各イントラスタット レポート プロセスの詳細アーカイブ中にレコードを追加できるように、レコード アクションを「挿入」にしておきます。</span><span class="sxs-lookup"><span data-stu-id="b4864-211">Keep the record action ‘Insert’ so you can add records during the detail archiving of each Intrastat reporting process.</span></span>  
33. <span data-ttu-id="b4864-212">[レコード情報ログ] フィールドで [はい] を選択します。</span><span class="sxs-lookup"><span data-stu-id="b4864-212">Select Yes in the Record infolog field.</span></span>
    * <span data-ttu-id="b4864-213">[はい] を選択して、アプリケーション データ更新の問題に関する情報を取得します。</span><span class="sxs-lookup"><span data-stu-id="b4864-213">Select Yes to get information about issues with the application data update.</span></span>  
34. <span data-ttu-id="b4864-214">[レコード アクションの検証のスキップ] フィールドで [はい] を選択します。</span><span class="sxs-lookup"><span data-stu-id="b4864-214">Select Yes in the Skip record action validation field.</span></span>
    * <span data-ttu-id="b4864-215">[はい] を選択して、空の [イントラスタット アーカイブ ID] フィールドについての検証エラーを非表示にします。</span><span class="sxs-lookup"><span data-stu-id="b4864-215">Select Yes to suppress validation errors about the empty ‘Intrastat archive ID’ field.</span></span> <span data-ttu-id="b4864-216">これは、[対外貿易パラメーター] フォームのこのテーブルにコンフィギュレーションされている順序番号設定に基づいて、レコードの追加後に行われます。</span><span class="sxs-lookup"><span data-stu-id="b4864-216">This will be done after records are added, based on the sequence number settings that are configured for this table in the Foreign trade parameters form.</span></span>  
35. <span data-ttu-id="b4864-217">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b4864-217">Click OK.</span></span>
    * <span data-ttu-id="b4864-218">追加されたデータ ソースの要素 (選択されたルート項目に基づいてフィルタ処理されたモデル) を、追加された出力先の要素とバインドします。</span><span class="sxs-lookup"><span data-stu-id="b4864-218">Bind elements of the added data source (the filtered model based on the selected root item) with elements from the added destination.</span></span>  
36. <span data-ttu-id="b4864-219">ツリーで、「アーカイブ」を展開します。</span><span class="sxs-lookup"><span data-stu-id="b4864-219">In the tree, expand 'Archive'.</span></span>
37. <span data-ttu-id="b4864-220">ツリーで、「アーカイブ\<リレーション」を展開します。</span><span class="sxs-lookup"><span data-stu-id="b4864-220">In the tree, expand 'Archive\<Relations'.</span></span>
38. <span data-ttu-id="b4864-221">ツリーで、「アーカイブ\<リレーション\IntrastatArchiveDetail」を展開します。</span><span class="sxs-lookup"><span data-stu-id="b4864-221">In the tree, expand 'Archive\<Relations\IntrastatArchiveDetail'.</span></span>
39. <span data-ttu-id="b4864-222">ツリーで、「アーカイブ\<リレーション\IntrastatArchiveDetail\Amount(AmountMST)」を選択します。</span><span class="sxs-lookup"><span data-stu-id="b4864-222">In the tree, select 'Archive\<Relations\IntrastatArchiveDetail\Amount(AmountMST)'.</span></span>
40. <span data-ttu-id="b4864-223">ツリーで、「モデル\アーカイブ ヘッダー\列挙された明細行」を展開します。</span><span class="sxs-lookup"><span data-stu-id="b4864-223">In the tree, expand 'model\Archive header\Enumerated lines'.</span></span>
41. <span data-ttu-id="b4864-224">ツリーで、「モデル\アーカイブ ヘッダー\列挙された明細行\値」を展開します。</span><span class="sxs-lookup"><span data-stu-id="b4864-224">In the tree, expand 'model\Archive header\Enumerated lines\Value'.</span></span>
42. <span data-ttu-id="b4864-225">ツリーで、「モデル\アーカイブ ヘッダー\列挙された明細行\値\金額」を選択します。</span><span class="sxs-lookup"><span data-stu-id="b4864-225">In the tree, select 'model\Archive header\Enumerated lines\Value\Amount'.</span></span>
43. <span data-ttu-id="b4864-226">[バインド] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b4864-226">Click Bind.</span></span>
44. <span data-ttu-id="b4864-227">ツリーで、「アーカイブ\<リレーション\IntrastatArchiveDetail\商品 (IntrastatCommodity)」を選択します。</span><span class="sxs-lookup"><span data-stu-id="b4864-227">In the tree, select 'Archive\<Relations\IntrastatArchiveDetail\Commodity(IntrastatCommodity)'.</span></span>
45. <span data-ttu-id="b4864-228">ツリーで、「モデル\アーカイブ ヘッダー\列挙された明細行\値\商品 rec id」を選択します。</span><span class="sxs-lookup"><span data-stu-id="b4864-228">In the tree, select 'model\Archive header\Enumerated lines\Value\Commodity rec id'.</span></span>
46. <span data-ttu-id="b4864-229">[バインド] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b4864-229">Click Bind.</span></span>
47. <span data-ttu-id="b4864-230">ツリーで、「アーカイブ\<リレーション\IntrastatArchiveDetail\品目番号 (ItemId)」を選択します。</span><span class="sxs-lookup"><span data-stu-id="b4864-230">In the tree, select 'Archive\<Relations\IntrastatArchiveDetail\Item number(ItemId)'.</span></span>
48. <span data-ttu-id="b4864-231">ツリーで、「モデル\アーカイブ ヘッダー\列挙された明細行\値\品目番号」を選択します。</span><span class="sxs-lookup"><span data-stu-id="b4864-231">In the tree, select 'model\Archive header\Enumerated lines\Value\Item number'.</span></span>
49. <span data-ttu-id="b4864-232">[バインド] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b4864-232">Click Bind.</span></span>
50. <span data-ttu-id="b4864-233">ツリーで、「アーカイブ\<リレーション\IntrastatArchiveDetail\行番号 (LineNumber)」を選択します。</span><span class="sxs-lookup"><span data-stu-id="b4864-233">In the tree, select 'Archive\<Relations\IntrastatArchiveDetail\Line number(LineNumber)'.</span></span>
51. <span data-ttu-id="b4864-234">ツリーで、「モデル\アーカイブ ヘッダー\列挙された明細行\番号」を選択します。</span><span class="sxs-lookup"><span data-stu-id="b4864-234">In the tree, select 'model\Archive header\Enumerated lines\Number'.</span></span>
52. <span data-ttu-id="b4864-235">[バインド] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b4864-235">Click Bind.</span></span>
53. <span data-ttu-id="b4864-236">ツリーで、「アーカイブ\<リレーション\IntrastatArchiveDetail」を選択します。</span><span class="sxs-lookup"><span data-stu-id="b4864-236">In the tree, select 'Archive\<Relations\IntrastatArchiveDetail'.</span></span>
54. <span data-ttu-id="b4864-237">ツリーで、「モデル\アーカイブ ヘッダー\列挙された明細行」を選択します。</span><span class="sxs-lookup"><span data-stu-id="b4864-237">In the tree, select 'model\Archive header\Enumerated lines'.</span></span>
55. <span data-ttu-id="b4864-238">[バインド] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b4864-238">Click Bind.</span></span>
56. <span data-ttu-id="b4864-239">ツリーで、「アーカイブ\ファイル名 (FileName)」を選択します。</span><span class="sxs-lookup"><span data-stu-id="b4864-239">In the tree, select 'Archive\File name(FileName)'.</span></span>
57. <span data-ttu-id="b4864-240">ツリーで、「モデル\アーカイブ ヘッダー\ファイル名」を選択します。</span><span class="sxs-lookup"><span data-stu-id="b4864-240">In the tree, select 'model\Archive header\File name'.</span></span>
58. <span data-ttu-id="b4864-241">[バインド] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b4864-241">Click Bind.</span></span>
59. <span data-ttu-id="b4864-242">ツリーで、「アーカイブ\行数 (NumberOfLines)」を選択します。</span><span class="sxs-lookup"><span data-stu-id="b4864-242">In the tree, select 'Archive\Number of lines(NumberOfLines)'.</span></span>
60. <span data-ttu-id="b4864-243">ツリーで、「モデル\アーカイブ ヘッダー\行数」を選択します。</span><span class="sxs-lookup"><span data-stu-id="b4864-243">In the tree, select 'model\Archive header\Number of lines'.</span></span>
61. <span data-ttu-id="b4864-244">[バインド] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b4864-244">Click Bind.</span></span>
62. <span data-ttu-id="b4864-245">ツリーで、「アーカイブ」を選択します。</span><span class="sxs-lookup"><span data-stu-id="b4864-245">In the tree, select 'Archive'.</span></span>
63. <span data-ttu-id="b4864-246">ツリーで、「モデル\アーカイブ ヘッダー」を選択します。</span><span class="sxs-lookup"><span data-stu-id="b4864-246">In the tree, select 'model\Archive header'.</span></span>
64. <span data-ttu-id="b4864-247">[バインド] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b4864-247">Click Bind.</span></span>
65. <span data-ttu-id="b4864-248">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b4864-248">Click Save.</span></span>
66. <span data-ttu-id="b4864-249">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="b4864-249">Close the page.</span></span>
67. <span data-ttu-id="b4864-250">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="b4864-250">Close the page.</span></span>

