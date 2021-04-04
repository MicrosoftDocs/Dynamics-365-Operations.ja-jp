---
title: アプリケーション データを含むドキュメントを生成するためのモデルおよびマッピングの変更
description: このトピックでは、電子ドキュメントを生成し、アプリケーション データを更新するためのレポート コンフィギュレーションを設計する方法について説明します。 (パート 2 - ドキュメントの生成)。
author: NickSelin
manager: AnnBe
ms.date: 06/19/2017
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 64bcf885fe2f5fca6b91589171b5e539eff2c3e5
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/09/2021
ms.locfileid: "5567095"
---
# <a name="modify-models-and-mappings-to-generate-documents-that-have-application-data"></a><span data-ttu-id="1d189-104">アプリケーション データを含むドキュメントを生成するためのモデルおよびマッピングの変更</span><span class="sxs-lookup"><span data-stu-id="1d189-104">Modify models and mappings to generate documents that have application data</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="1d189-105">この手順のステップを完了するには、まず 「ER アプリケーション データ更新と共にドキュメントを生成する (パート 2：ドキュメントの生成)」 に記載の手順を完了する必要があります。</span><span class="sxs-lookup"><span data-stu-id="1d189-105">To complete the steps in this procedure, you must first complete the procedure, "ER Generate documents with application data update (Part 2: Generate documents)".</span></span> 

<span data-ttu-id="1d189-106">この手順のステップでは、電子ドキュメントを生成してアプリケーション データを更新するために電子申告 (ER) コンフィギュレーションを設計する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="1d189-106">The steps in this procedure explain how to design Electronic reporting (ER) configurations to generate an electronic document and update application data.</span></span> <span data-ttu-id="1d189-107">この手順では、ER コンフィギュレーションを変更し、その使用を開始して、電子ドキュメントを生成しアプリケーション データを更新します。</span><span class="sxs-lookup"><span data-stu-id="1d189-107">In this procedure, you will modify the ER configurations to start using them to generate electronic documents and update application data.</span></span> <span data-ttu-id="1d189-108">この手順は、「システム管理者」または「電子レポート開発者」ロールが割り当てられているユーザー用に作成されています。</span><span class="sxs-lookup"><span data-stu-id="1d189-108">This procedure is created for users with the assigned role of system administrator or electronic reporting developer.</span></span> <span data-ttu-id="1d189-109">これらのステップは、DEMF データ セットを使用して完了することができます。</span><span class="sxs-lookup"><span data-stu-id="1d189-109">These steps can be completed using the DEMF dataset.</span></span>


## <a name="modify-data-model"></a><span data-ttu-id="1d189-110">データ モデルの変更</span><span class="sxs-lookup"><span data-stu-id="1d189-110">Modify data model</span></span>
1. <span data-ttu-id="1d189-111">[組織管理] > [電子申告] > [コンフィギュレーション] に移動します。</span><span class="sxs-lookup"><span data-stu-id="1d189-111">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="1d189-112">ツリーで、「イントラスタット (モデル)」を選択します。</span><span class="sxs-lookup"><span data-stu-id="1d189-112">In the tree, select 'Intrastat (model)'.</span></span>
    * <span data-ttu-id="1d189-113">データ モデルを使用する方法を拡張します。</span><span class="sxs-lookup"><span data-stu-id="1d189-113">You will extend how you use the data model.</span></span> <span data-ttu-id="1d189-114">データ モデルは、イントラスタット レポートを生成するデータ ソースとして使用するだけでなく、イントラスタット レポート プロセスに関する詳細を収集するためにも使用します。</span><span class="sxs-lookup"><span data-stu-id="1d189-114">Besides using it as data source to generate the Intrastat report, the data model will be used to collect details about the Intrastat reporting process.</span></span> <span data-ttu-id="1d189-115">その詳細は、アプリケーション データの更新に使用されます。</span><span class="sxs-lookup"><span data-stu-id="1d189-115">The details will then be used to update application data.</span></span>   
3. <span data-ttu-id="1d189-116">[デザイナー] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="1d189-116">Click Designer.</span></span>
4. <span data-ttu-id="1d189-117">[新規] をクリックすると、ドロップ ダイアログが開きます。</span><span class="sxs-lookup"><span data-stu-id="1d189-117">Click New to open the drop dialog.</span></span>
5. <span data-ttu-id="1d189-118">[新しいノード] フィールドに、「モデル ルート」を入力します。</span><span class="sxs-lookup"><span data-stu-id="1d189-118">In the New node as a field, enter 'Model root'.</span></span>
6. <span data-ttu-id="1d189-119">[名前] フィールドに、「アプリケーション データの更新用」と入力します。</span><span class="sxs-lookup"><span data-stu-id="1d189-119">In the Name field, type 'For application data update'.</span></span>
    * <span data-ttu-id="1d189-120">アプリケーション データの更新用</span><span class="sxs-lookup"><span data-stu-id="1d189-120">For application data update</span></span>  
7. <span data-ttu-id="1d189-121">[追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="1d189-121">Click Add.</span></span>
8. <span data-ttu-id="1d189-122">ツリーで、「アプリケーション データの更新用」を選択します。</span><span class="sxs-lookup"><span data-stu-id="1d189-122">In the tree, select 'For application data update'.</span></span>
    * <span data-ttu-id="1d189-123">この新しいルート項目は、イントラスタット レポート (データ ソースとして使用) からアプリケーション テーブル (更新先) にデータを移動するためのデータ フローを指定するために追加されます。</span><span class="sxs-lookup"><span data-stu-id="1d189-123">This new root item is added to specify the data flow for moving data from the Intrastat report (used as a data source) to the application tables (the update destination).</span></span> <span data-ttu-id="1d189-124">送信文書に投稿されるデータを取得したり、アプリケーション データを更新するために使用される文書からデータを取得するには、異なるルート項目を使用する必要があることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="1d189-124">Note that different root items must be used for getting data that is posted to the outgoing document and for getting data from the document that is used to update application data.</span></span>   
9. <span data-ttu-id="1d189-125">[新規] をクリックすると、ドロップ ダイアログが開きます。</span><span class="sxs-lookup"><span data-stu-id="1d189-125">Click New to open the drop dialog.</span></span>
10. <span data-ttu-id="1d189-126">[名前] フィールドに、「アーカイブ ヘッダー」と入力します。</span><span class="sxs-lookup"><span data-stu-id="1d189-126">In the Name field, type 'Archive header'.</span></span>
    * <span data-ttu-id="1d189-127">アーカイブ ヘッダー</span><span class="sxs-lookup"><span data-stu-id="1d189-127">Archive header</span></span>  
11. <span data-ttu-id="1d189-128">[品目タイプ] フィールドで、「レコード リスト」を選択します。</span><span class="sxs-lookup"><span data-stu-id="1d189-128">In the Item type field, select 'Record list'.</span></span>
12. <span data-ttu-id="1d189-129">[追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="1d189-129">Click Add.</span></span>
    * <span data-ttu-id="1d189-130">生成されるそれぞれのイントラスタット レポートにレコードを作成するので、そのための新しい品目を作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="1d189-130">Because you will create a record for each Intrastat report that is generated, you must create a new item for that.</span></span>  
13. <span data-ttu-id="1d189-131">[新規] をクリックすると、ドロップ ダイアログが開きます。</span><span class="sxs-lookup"><span data-stu-id="1d189-131">Click New to open the drop dialog.</span></span>
14. <span data-ttu-id="1d189-132">[名称] フィールドで、「ファイル名」を入力します。</span><span class="sxs-lookup"><span data-stu-id="1d189-132">In the Name field, type 'File name'.</span></span>
    * <span data-ttu-id="1d189-133">ファイル名</span><span class="sxs-lookup"><span data-stu-id="1d189-133">File name</span></span>  
15. <span data-ttu-id="1d189-134">[品目タイプ] フィールドで、「String」を選択します。</span><span class="sxs-lookup"><span data-stu-id="1d189-134">In the Item type field, select 'String'.</span></span>
16. <span data-ttu-id="1d189-135">[追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="1d189-135">Click Add.</span></span>
17. <span data-ttu-id="1d189-136">[新規] をクリックすると、ドロップ ダイアログが開きます。</span><span class="sxs-lookup"><span data-stu-id="1d189-136">Click New to open the drop dialog.</span></span>
18. <span data-ttu-id="1d189-137">[名前] フィールドに、「行数」と入力します。</span><span class="sxs-lookup"><span data-stu-id="1d189-137">In the Name field, type 'Number of lines'.</span></span>
    * <span data-ttu-id="1d189-138">ライン数</span><span class="sxs-lookup"><span data-stu-id="1d189-138">Number of lines</span></span>  
19. <span data-ttu-id="1d189-139">[項目タイプ] フィールドで、「整数」を選択します。</span><span class="sxs-lookup"><span data-stu-id="1d189-139">In the Item type field, select 'Integer'.</span></span>
20. <span data-ttu-id="1d189-140">[追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="1d189-140">Click Add.</span></span>
    * <span data-ttu-id="1d189-141">現在のレポート プロセス中にレポートされたイントラスタット トランザクションの数を表すために、この品目を追加します。</span><span class="sxs-lookup"><span data-stu-id="1d189-141">Add this item to represent the number of Intrastat transactions that are reported during the current reporting process.</span></span>  
21. <span data-ttu-id="1d189-142">[新規] をクリックすると、ドロップ ダイアログが開きます。</span><span class="sxs-lookup"><span data-stu-id="1d189-142">Click New to open the drop dialog.</span></span>
22. <span data-ttu-id="1d189-143">[名前] フィールドに、「アーカイブ明細行」と入力します。</span><span class="sxs-lookup"><span data-stu-id="1d189-143">In the Name field, type 'Archive lines'.</span></span>
    * <span data-ttu-id="1d189-144">アーカイブ明細行</span><span class="sxs-lookup"><span data-stu-id="1d189-144">Archive lines</span></span>  
23. <span data-ttu-id="1d189-145">[品目タイプ] フィールドで、「レコード リスト」を選択します。</span><span class="sxs-lookup"><span data-stu-id="1d189-145">In the Item type field, select 'Record list'.</span></span>
24. <span data-ttu-id="1d189-146">[追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="1d189-146">Click Add.</span></span>
    * <span data-ttu-id="1d189-147">現在のレポート プロセス中にレポートされたイントラスタット トランザクションのリストを表すために、この品目を追加します。</span><span class="sxs-lookup"><span data-stu-id="1d189-147">Add this item to represent the list of Intrastat transactions that are reported during the current reporting process.</span></span>  
25. <span data-ttu-id="1d189-148">[新規] をクリックすると、ドロップ ダイアログが開きます。</span><span class="sxs-lookup"><span data-stu-id="1d189-148">Click New to open the drop dialog.</span></span>
26. <span data-ttu-id="1d189-149">[名前] フィールドに、「$Amount」と入力します。</span><span class="sxs-lookup"><span data-stu-id="1d189-149">In the Name field, type 'Amount'.</span></span>
    * <span data-ttu-id="1d189-150">量</span><span class="sxs-lookup"><span data-stu-id="1d189-150">Amount</span></span>  
27. <span data-ttu-id="1d189-151">[品目タイプ] フィールドで、「実数」を選択します。</span><span class="sxs-lookup"><span data-stu-id="1d189-151">In the Item type field, select 'Real'.</span></span>
28. <span data-ttu-id="1d189-152">[追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="1d189-152">Click Add.</span></span>
29. <span data-ttu-id="1d189-153">[新規] をクリックすると、ドロップ ダイアログが開きます。</span><span class="sxs-lookup"><span data-stu-id="1d189-153">Click New to open the drop dialog.</span></span>
30. <span data-ttu-id="1d189-154">[名前] フィールドに、「商品 rec id」と入力します。</span><span class="sxs-lookup"><span data-stu-id="1d189-154">In the Name field, type 'Commodity rec id'.</span></span>
    * <span data-ttu-id="1d189-155">商品 rec id</span><span class="sxs-lookup"><span data-stu-id="1d189-155">Commodity rec id</span></span>  
31. <span data-ttu-id="1d189-156">[項目タイプ] フィールドで、「Int64」を選択します。</span><span class="sxs-lookup"><span data-stu-id="1d189-156">In the Item type field, select 'Int64'.</span></span>
32. <span data-ttu-id="1d189-157">[追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="1d189-157">Click Add.</span></span>
33. <span data-ttu-id="1d189-158">[新規] をクリックすると、ドロップ ダイアログが開きます。</span><span class="sxs-lookup"><span data-stu-id="1d189-158">Click New to open the drop dialog.</span></span>
34. <span data-ttu-id="1d189-159">[名前] フィールドに、「品目番号」と入力します。</span><span class="sxs-lookup"><span data-stu-id="1d189-159">In the Name field, type 'Item number'.</span></span>
    * <span data-ttu-id="1d189-160">品目番号</span><span class="sxs-lookup"><span data-stu-id="1d189-160">Item number</span></span>  
35. <span data-ttu-id="1d189-161">[品目タイプ] フィールドで、「String」を選択します。</span><span class="sxs-lookup"><span data-stu-id="1d189-161">In the Item type field, select 'String'.</span></span>
36. <span data-ttu-id="1d189-162">[追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="1d189-162">Click Add.</span></span>
37. <span data-ttu-id="1d189-163">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="1d189-163">Click Save.</span></span>
38. <span data-ttu-id="1d189-164">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="1d189-164">Close the page.</span></span>

## <a name="modify-model-mapping"></a><span data-ttu-id="1d189-165">モデル マッピングの変更</span><span class="sxs-lookup"><span data-stu-id="1d189-165">Modify model mapping</span></span>
1. <span data-ttu-id="1d189-166">ツリーで、「イントラスタット (モデル)」を展開します。</span><span class="sxs-lookup"><span data-stu-id="1d189-166">In the tree, expand 'Intrastat (model)'.</span></span>
2. <span data-ttu-id="1d189-167">ツリーで、「イントラスタット (モデル)\イントラスタット (マッピング)」を選択します。</span><span class="sxs-lookup"><span data-stu-id="1d189-167">In the tree, select 'Intrastat (model)\Intrastat (mapping)'.</span></span>
    * <span data-ttu-id="1d189-168">既存のモデルマッピングを変更して、アプリケーションデータの更新への使用を開始し、イントラスタット レポートの詳細をアーカイブします。</span><span class="sxs-lookup"><span data-stu-id="1d189-168">Modify the existing model mapping to start using it for  the application data update and to archive Intrastat reporting details.</span></span>  
3. <span data-ttu-id="1d189-169">[デザイナー] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="1d189-169">Click Designer.</span></span>
4. <span data-ttu-id="1d189-170">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="1d189-170">Click New.</span></span>
5. <span data-ttu-id="1d189-171">[名前] フィールドに、「アーカイブの更新」と入力します。</span><span class="sxs-lookup"><span data-stu-id="1d189-171">In the Name field, type 'Update archive'.</span></span>
    * <span data-ttu-id="1d189-172">アーカイブの更新</span><span class="sxs-lookup"><span data-stu-id="1d189-172">Update archive</span></span>  
6. <span data-ttu-id="1d189-173">[方向] フィールドで、「宛先」を選択します。</span><span class="sxs-lookup"><span data-stu-id="1d189-173">In the Direction field, select 'To destination'.</span></span>
7. <span data-ttu-id="1d189-174">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="1d189-174">Click Save.</span></span>
    * <span data-ttu-id="1d189-175">この新しいマッピングは、データ モデルからアプリケーション テーブル (更新先) にデータ (イントラスタット レポートの詳細) を移動するためのデータ フローを指定します。</span><span class="sxs-lookup"><span data-stu-id="1d189-175">This new mapping specifies the data flow for moving data (Intrastat reporting details) from the data model to the application tables (the update destination).</span></span> <span data-ttu-id="1d189-176">レポート プロセスで使用するアプリケーションからデータを取得し、アプリケーション データ更新のためにデータ モデルのデータを使用するには、異なるモデルのルート項目を使用する必要があることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="1d189-176">Note that different model's root items must be used to get data from the application for the reporting process and then use the data from data model for the application data update.</span></span>   
8. <span data-ttu-id="1d189-177">[デザイナー] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="1d189-177">Click Designer.</span></span>
9. <span data-ttu-id="1d189-178">ツリーで、「データ モデル\データ モデル」を選択します。</span><span class="sxs-lookup"><span data-stu-id="1d189-178">In the tree, select 'Data model\Data model'.</span></span>
    * <span data-ttu-id="1d189-179">必要なデータ ソースを追加します。</span><span class="sxs-lookup"><span data-stu-id="1d189-179">Add the required data source.</span></span> <span data-ttu-id="1d189-180">これは、アーカイブする必要のあるレポートされたイントラスタット トランザクションの詳細を含むデータ モデルです。</span><span class="sxs-lookup"><span data-stu-id="1d189-180">This is the data model that contains details of the reported Intrastat transactions that must be archived.</span></span>  
10. <span data-ttu-id="1d189-181">[ルートの追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="1d189-181">Click Add root.</span></span>
11. <span data-ttu-id="1d189-182">[名前] フィールドに、「モデル」と入力します。</span><span class="sxs-lookup"><span data-stu-id="1d189-182">In the Name field, type 'model'.</span></span>
    * <span data-ttu-id="1d189-183">モデル</span><span class="sxs-lookup"><span data-stu-id="1d189-183">model</span></span>  
12. <span data-ttu-id="1d189-184">[定義] フィールドで、「アプリケーション データの更新」 という値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="1d189-184">In the Definition field, enter or select the value 'For application data update'.</span></span>
    * <span data-ttu-id="1d189-185">アプリケーション データの更新用</span><span class="sxs-lookup"><span data-stu-id="1d189-185">For application data update</span></span>  
13. <span data-ttu-id="1d189-186">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="1d189-186">Click OK.</span></span>
14. <span data-ttu-id="1d189-187">ツリーで、[model] を展開します。</span><span class="sxs-lookup"><span data-stu-id="1d189-187">In the tree, expand 'model'.</span></span>
15. <span data-ttu-id="1d189-188">ツリーで、[Functions\Calculated field] を選択します。</span><span class="sxs-lookup"><span data-stu-id="1d189-188">In the tree, select 'Functions\Calculated field'.</span></span>
16. <span data-ttu-id="1d189-189">ツリーで、「モデル\アーカイブ ヘッダー」を選択します。</span><span class="sxs-lookup"><span data-stu-id="1d189-189">In the tree, select 'model\Archive header'.</span></span>
17. <span data-ttu-id="1d189-190">[追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="1d189-190">Click Add.</span></span>
    * <span data-ttu-id="1d189-191">アーカイブ用にレポート済イントラスタット トランザクションを列挙するため、適切なデータ ソースを追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="1d189-191">Because you want to enumerate reported Intrastat transactions for archiving, the appropriate data source must be added.</span></span>  
18. <span data-ttu-id="1d189-192">[名前] フィールドに、「列挙された明細行」と入力します。</span><span class="sxs-lookup"><span data-stu-id="1d189-192">In the Name field, type 'Enumerated lines'.</span></span>
    * <span data-ttu-id="1d189-193">列挙された明細行</span><span class="sxs-lookup"><span data-stu-id="1d189-193">Enumerated lines</span></span>  
19. <span data-ttu-id="1d189-194">[式の編集] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="1d189-194">Click Edit formula.</span></span>
20. <span data-ttu-id="1d189-195">ツリーで、「リスト\ENUMERATE」を選択します。</span><span class="sxs-lookup"><span data-stu-id="1d189-195">In the tree, select 'List\ENUMERATE'.</span></span>
21. <span data-ttu-id="1d189-196">[機能の追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="1d189-196">Click Add function.</span></span>
22. <span data-ttu-id="1d189-197">ツリーで、「model」を展開します。</span><span class="sxs-lookup"><span data-stu-id="1d189-197">In the tree, expand 'model'.</span></span>
23. <span data-ttu-id="1d189-198">ツリーで、「モデル\アーカイブ ヘッダー」を展開します。</span><span class="sxs-lookup"><span data-stu-id="1d189-198">In the tree, expand 'model\Archive header'.</span></span>
24. <span data-ttu-id="1d189-199">ツリーで、「モデル\アーカイブ ヘッダー\アーカイブ明細行」を選択します。</span><span class="sxs-lookup"><span data-stu-id="1d189-199">In the tree, select 'model\Archive header\Archive lines'.</span></span>
25. <span data-ttu-id="1d189-200">[データ ソースの追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="1d189-200">Click Add data source.</span></span>
26. <span data-ttu-id="1d189-201">[フォーミュラ] フィールドに、「ENUMERATE(model.'Archive header'.'Archive lines')」と入力します。</span><span class="sxs-lookup"><span data-stu-id="1d189-201">In the Formula field, enter 'ENUMERATE(model.'Archive header'.'Archive lines')'.</span></span>
    * <span data-ttu-id="1d189-202">ENUMERATE(model.'Archive header'.'Archive lines')</span><span class="sxs-lookup"><span data-stu-id="1d189-202">ENUMERATE(model.'Archive header'.'Archive lines')</span></span>  
27. <span data-ttu-id="1d189-203">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="1d189-203">Click Save.</span></span>
28. <span data-ttu-id="1d189-204">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="1d189-204">Close the page.</span></span>
29. <span data-ttu-id="1d189-205">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="1d189-205">Click OK.</span></span>
30. <span data-ttu-id="1d189-206">[宛先の追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="1d189-206">Click Add destination.</span></span>
    * <span data-ttu-id="1d189-207">レポート済のイントラスタット トランザクションの詳細をアーカイブするために更新を必要とする必要な出力先として、アプリケーション テーブルを追加します。</span><span class="sxs-lookup"><span data-stu-id="1d189-207">Add application tables as required destinations that require updates to archive details of reported Intrastat transactions.</span></span>  
31. <span data-ttu-id="1d189-208">[名前] フィールドに、「アーカイブ」と入力します。</span><span class="sxs-lookup"><span data-stu-id="1d189-208">In the Name field, type 'Archive'.</span></span>
    * <span data-ttu-id="1d189-209">アーカイブ</span><span class="sxs-lookup"><span data-stu-id="1d189-209">Archive</span></span>  
32. <span data-ttu-id="1d189-210">[テーブル名] フィールドで、「IntrastatArchiveGeneral」と入力します。</span><span class="sxs-lookup"><span data-stu-id="1d189-210">In the Table name field, type 'IntrastatArchiveGeneral'.</span></span>
    * <span data-ttu-id="1d189-211">IntrastatArchiveGeneral</span><span class="sxs-lookup"><span data-stu-id="1d189-211">IntrastatArchiveGeneral</span></span>  
    * <span data-ttu-id="1d189-212">レコードアクション 「挿入」 を保持することで、イントラスタット レポートプロセスの詳細アーカイブ中にレコードを追加することができます。</span><span class="sxs-lookup"><span data-stu-id="1d189-212">Keep the record action 'Insert' so you can add records during the detail archiving of each Intrastat reporting process.</span></span>  
33. <span data-ttu-id="1d189-213">[レコード情報ログ] フィールドで [はい] を選択します。</span><span class="sxs-lookup"><span data-stu-id="1d189-213">Select Yes in the Record infolog field.</span></span>
    * <span data-ttu-id="1d189-214">[はい] を選択して、アプリケーション データ更新の問題に関する情報を取得します。</span><span class="sxs-lookup"><span data-stu-id="1d189-214">Select Yes to get information about issues with the application data update.</span></span>  
34. <span data-ttu-id="1d189-215">[レコード アクションの検証のスキップ] フィールドで [はい] を選択します。</span><span class="sxs-lookup"><span data-stu-id="1d189-215">Select Yes in the Skip record action validation field.</span></span>
    * <span data-ttu-id="1d189-216">[はい] を選択すると、空の [イントラスタット アーカイブ ID] フィールドに関する検証エラーを抑制することができます。</span><span class="sxs-lookup"><span data-stu-id="1d189-216">Select Yes to suppress validation errors about the empty 'Intrastat archive ID' field.</span></span> <span data-ttu-id="1d189-217">これは、[対外貿易パラメーター] フォームのこのテーブルにコンフィギュレーションされている順序番号設定に基づいて、レコードの追加後に行われます。</span><span class="sxs-lookup"><span data-stu-id="1d189-217">This will be done after records are added, based on the sequence number settings that are configured for this table in the Foreign trade parameters form.</span></span>  
35. <span data-ttu-id="1d189-218">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="1d189-218">Click OK.</span></span>
    * <span data-ttu-id="1d189-219">追加されたデータ ソースの要素 (選択されたルート項目に基づいてフィルタ処理されたモデル) を、追加された出力先の要素とバインドします。</span><span class="sxs-lookup"><span data-stu-id="1d189-219">Bind elements of the added data source (the filtered model based on the selected root item) with elements from the added destination.</span></span>  
36. <span data-ttu-id="1d189-220">ツリーで、「アーカイブ」を展開します。</span><span class="sxs-lookup"><span data-stu-id="1d189-220">In the tree, expand 'Archive'.</span></span>
37. <span data-ttu-id="1d189-221">ツリーで、「アーカイブ\<リレーション」を展開します。</span><span class="sxs-lookup"><span data-stu-id="1d189-221">In the tree, expand 'Archive\<Relations'.</span></span>
38. <span data-ttu-id="1d189-222">ツリーで、「アーカイブ\<リレーション\IntrastatArchiveDetail」を展開します。</span><span class="sxs-lookup"><span data-stu-id="1d189-222">In the tree, expand 'Archive\<Relations\IntrastatArchiveDetail'.</span></span>
39. <span data-ttu-id="1d189-223">ツリーで、「アーカイブ\<リレーション\IntrastatArchiveDetail\Amount(AmountMST)」を選択します。</span><span class="sxs-lookup"><span data-stu-id="1d189-223">In the tree, select 'Archive\<Relations\IntrastatArchiveDetail\Amount(AmountMST)'.</span></span>
40. <span data-ttu-id="1d189-224">ツリーで、「モデル\アーカイブ ヘッダー\列挙された明細行」を展開します。</span><span class="sxs-lookup"><span data-stu-id="1d189-224">In the tree, expand 'model\Archive header\Enumerated lines'.</span></span>
41. <span data-ttu-id="1d189-225">ツリーで、「モデル\アーカイブ ヘッダー\列挙された明細行\値」を展開します。</span><span class="sxs-lookup"><span data-stu-id="1d189-225">In the tree, expand 'model\Archive header\Enumerated lines\Value'.</span></span>
42. <span data-ttu-id="1d189-226">ツリーで、「モデル\アーカイブ ヘッダー\列挙された明細行\値\金額」を選択します。</span><span class="sxs-lookup"><span data-stu-id="1d189-226">In the tree, select 'model\Archive header\Enumerated lines\Value\Amount'.</span></span>
43. <span data-ttu-id="1d189-227">[バインド] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="1d189-227">Click Bind.</span></span>
44. <span data-ttu-id="1d189-228">ツリーで、「アーカイブ\<リレーション\IntrastatArchiveDetail\商品 (IntrastatCommodity)」を選択します。</span><span class="sxs-lookup"><span data-stu-id="1d189-228">In the tree, select 'Archive\<Relations\IntrastatArchiveDetail\Commodity(IntrastatCommodity)'.</span></span>
45. <span data-ttu-id="1d189-229">ツリーで、「モデル\アーカイブ ヘッダー\列挙された明細行\値\商品 rec id」を選択します。</span><span class="sxs-lookup"><span data-stu-id="1d189-229">In the tree, select 'model\Archive header\Enumerated lines\Value\Commodity rec id'.</span></span>
46. <span data-ttu-id="1d189-230">[バインド] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="1d189-230">Click Bind.</span></span>
47. <span data-ttu-id="1d189-231">ツリーで、「アーカイブ\<リレーション\IntrastatArchiveDetail\品目番号 (ItemId)」を選択します。</span><span class="sxs-lookup"><span data-stu-id="1d189-231">In the tree, select 'Archive\<Relations\IntrastatArchiveDetail\Item number(ItemId)'.</span></span>
48. <span data-ttu-id="1d189-232">ツリーで、「モデル\アーカイブ ヘッダー\列挙された明細行\値\品目番号」を選択します。</span><span class="sxs-lookup"><span data-stu-id="1d189-232">In the tree, select 'model\Archive header\Enumerated lines\Value\Item number'.</span></span>
49. <span data-ttu-id="1d189-233">[バインド] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="1d189-233">Click Bind.</span></span>
50. <span data-ttu-id="1d189-234">ツリーで、「アーカイブ\<リレーション\IntrastatArchiveDetail\行番号 (LineNumber)」を選択します。</span><span class="sxs-lookup"><span data-stu-id="1d189-234">In the tree, select 'Archive\<Relations\IntrastatArchiveDetail\Line number(LineNumber)'.</span></span>
51. <span data-ttu-id="1d189-235">ツリーで、「モデル\アーカイブ ヘッダー\列挙された明細行\番号」を選択します。</span><span class="sxs-lookup"><span data-stu-id="1d189-235">In the tree, select 'model\Archive header\Enumerated lines\Number'.</span></span>
52. <span data-ttu-id="1d189-236">[バインド] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="1d189-236">Click Bind.</span></span>
53. <span data-ttu-id="1d189-237">ツリーで、「アーカイブ\<リレーション\IntrastatArchiveDetail」を選択します。</span><span class="sxs-lookup"><span data-stu-id="1d189-237">In the tree, select 'Archive\<Relations\IntrastatArchiveDetail'.</span></span>
54. <span data-ttu-id="1d189-238">ツリーで、「モデル\アーカイブ ヘッダー\列挙された明細行」を選択します。</span><span class="sxs-lookup"><span data-stu-id="1d189-238">In the tree, select 'model\Archive header\Enumerated lines'.</span></span>
55. <span data-ttu-id="1d189-239">[バインド] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="1d189-239">Click Bind.</span></span>
56. <span data-ttu-id="1d189-240">ツリーで、「アーカイブ\ファイル名 (FileName)」を選択します。</span><span class="sxs-lookup"><span data-stu-id="1d189-240">In the tree, select 'Archive\File name(FileName)'.</span></span>
57. <span data-ttu-id="1d189-241">ツリーで、「モデル\アーカイブ ヘッダー\ファイル名」を選択します。</span><span class="sxs-lookup"><span data-stu-id="1d189-241">In the tree, select 'model\Archive header\File name'.</span></span>
58. <span data-ttu-id="1d189-242">[バインド] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="1d189-242">Click Bind.</span></span>
59. <span data-ttu-id="1d189-243">ツリーで、「アーカイブ\行数 (NumberOfLines)」を選択します。</span><span class="sxs-lookup"><span data-stu-id="1d189-243">In the tree, select 'Archive\Number of lines(NumberOfLines)'.</span></span>
60. <span data-ttu-id="1d189-244">ツリーで、「モデル\アーカイブ ヘッダー\行数」を選択します。</span><span class="sxs-lookup"><span data-stu-id="1d189-244">In the tree, select 'model\Archive header\Number of lines'.</span></span>
61. <span data-ttu-id="1d189-245">[バインド] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="1d189-245">Click Bind.</span></span>
62. <span data-ttu-id="1d189-246">ツリーで、「アーカイブ」を選択します。</span><span class="sxs-lookup"><span data-stu-id="1d189-246">In the tree, select 'Archive'.</span></span>
63. <span data-ttu-id="1d189-247">ツリーで、「モデル\アーカイブ ヘッダー」を選択します。</span><span class="sxs-lookup"><span data-stu-id="1d189-247">In the tree, select 'model\Archive header'.</span></span>
64. <span data-ttu-id="1d189-248">[バインド] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="1d189-248">Click Bind.</span></span>
65. <span data-ttu-id="1d189-249">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="1d189-249">Click Save.</span></span>
66. <span data-ttu-id="1d189-250">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="1d189-250">Close the page.</span></span>
67. <span data-ttu-id="1d189-251">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="1d189-251">Close the page.</span></span>



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]