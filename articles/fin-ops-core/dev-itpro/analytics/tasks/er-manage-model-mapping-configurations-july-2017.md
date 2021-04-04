---
title: 個別の電子申告コンフィギュレーションで電子申告モデル マッピングを管理する
description: このトピックでは、個別の ER コンフィギュレーションで電子申告 (ER) モデル マッピングを管理する方法について説明します。
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
ms.openlocfilehash: fdd6804c33cc153974229c60b64c3bd76426241a
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/09/2021
ms.locfileid: "5569416"
---
# <a name="manage-er-model-mapping-in-separate-er-configurations"></a><span data-ttu-id="be256-103">個別の ER コンフィギュレーションにおける ER モデル マッピングの管理</span><span class="sxs-lookup"><span data-stu-id="be256-103">Manage ER model mapping in separate ER configurations</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="be256-104">次のステップでは、「システム管理者」または「電子レポート開発者」ロールに割り当てられたユーザーが、個別の ER コンフィギュレーションの電子申告 (ER) モデル マッピングを管理する方法を説明します。</span><span class="sxs-lookup"><span data-stu-id="be256-104">The following steps explain how a user assigned to the System administrator or Electronic reporting developer role can manage Electronic reporting (ER) model mappings in separate ER configurations.</span></span> <span data-ttu-id="be256-105">このタスク ガイドでは、サンプル会社 Litware, Inc. に必要となる ER 構成を作成します。このタスク ガイドを完了するには、まずタスク ガイド 「ER 構成プロバイダーの作成」 に記載のステップを完了する必要があります。</span><span class="sxs-lookup"><span data-stu-id="be256-105">In this task guide, you will create required ER configurations for the sample company, Litware, Inc. To complete this task guide, you must first complete the steps in the task guide, "ER Create a configuration provider" and mark it as active.</span></span> 

<span data-ttu-id="be256-106">ER コンフィギュレーションは会社間で共有されるので、選択した会社のデータ セットを使用してこのタスク ガイドを完了できます。</span><span class="sxs-lookup"><span data-stu-id="be256-106">Because ER configurations are shared among companies, you can complete this task guide using the company data set of your choice.</span></span> <span data-ttu-id="be256-107">このタスク ガイドの機能は、次の修正プログラムのうち 1 つをインストールした場合に使用可能です: Dynamics AX バージョン 7.0 の https://fix.lcs.dynamics.com/Issue/Resolved?kb=4012872 または Dynamics 365 for Operations バージョンの https://fix.lcs.dynamics.com/Issue/Resolved?kb=4012871。</span><span class="sxs-lookup"><span data-stu-id="be256-107">The functionality for this task guide is available if you have installed one of the following hotfixes: https://fix.lcs.dynamics.com/Issue/Resolved?kb=4012872 for the Dynamics AX 7.0 version or https://fix.lcs.dynamics.com/Issue/Resolved?kb=4012871 for the Dynamics 365 for Operations version.</span></span>

1. <span data-ttu-id="be256-108">[組織管理] > [ワークスペース] > [電子申告] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="be256-108">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
    * <span data-ttu-id="be256-109">サンプル会社 Litware, Inc. のコンフィギュレーション プロバイダーが使用可能であり、アクティブとしてマークされていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="be256-109">Verify that the configuration provider for the sample company Litware, Inc. is available and marked as active.</span></span> <span data-ttu-id="be256-110">この構成プロバイダーが表示されない場合は、まずタスク ガイド 「構成プロバイダを作成する」 の手順を完了し、アクティブとしてマークする必要があります。</span><span class="sxs-lookup"><span data-stu-id="be256-110">If you don't see this configuration provider, you must first complete the steps in the task guide, Create a configuration provider, and mark it as active.</span></span>   

## <a name="add-a-new-er-model-configuration"></a><span data-ttu-id="be256-111">新しい ER モデル コンフィギュレーションの追加</span><span class="sxs-lookup"><span data-stu-id="be256-111">Add a new ER model configuration</span></span>
1. <span data-ttu-id="be256-112">[コンフィギュレーションをレポートする] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="be256-112">Click Reporting configurations.</span></span>
    * <span data-ttu-id="be256-113">新しいモデル コンフィギュレーションを追加します。</span><span class="sxs-lookup"><span data-stu-id="be256-113">Add a new model configuration.</span></span> <span data-ttu-id="be256-114">名前は、コンフィギュレーション ツリーで一意である必要があります。</span><span class="sxs-lookup"><span data-stu-id="be256-114">The name must be unique in the configurations tree.</span></span>  
2. <span data-ttu-id="be256-115">[コンフィギュレーションの作成] をクリックすると、ドロップ ダイアログが開きます。</span><span class="sxs-lookup"><span data-stu-id="be256-115">Click Create configuration to open the drop dialog.</span></span>
3. <span data-ttu-id="be256-116">[名前] フィールドに、「サンプル データ モデル」と入力します。</span><span class="sxs-lookup"><span data-stu-id="be256-116">In the Name field, type 'Sample data model'.</span></span>
    * <span data-ttu-id="be256-117">サンプルのデータ モデル</span><span class="sxs-lookup"><span data-stu-id="be256-117">Sample data model</span></span>  
4. <span data-ttu-id="be256-118">[コンフィギュレーションの作成] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="be256-118">Click Create configuration.</span></span>
5. <span data-ttu-id="be256-119">[デザイナー] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="be256-119">Click Designer.</span></span>
6. <span data-ttu-id="be256-120">[新規] をクリックすると、ドロップ ダイアログが開きます。</span><span class="sxs-lookup"><span data-stu-id="be256-120">Click New to open the drop dialog.</span></span>
7. <span data-ttu-id="be256-121">[名称] のフィールドに、「Root」を入力します。</span><span class="sxs-lookup"><span data-stu-id="be256-121">In the Name field, type 'Root'.</span></span>
    * <span data-ttu-id="be256-122">ルート</span><span class="sxs-lookup"><span data-stu-id="be256-122">Root</span></span>  
8. <span data-ttu-id="be256-123">[追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="be256-123">Click Add.</span></span>
9. <span data-ttu-id="be256-124">[新規] をクリックすると、ドロップ ダイアログが開きます。</span><span class="sxs-lookup"><span data-stu-id="be256-124">Click New to open the drop dialog.</span></span>
10. <span data-ttu-id="be256-125">[名前] フィールドに、「Company」と入力します。</span><span class="sxs-lookup"><span data-stu-id="be256-125">In the Name field, type 'Company'.</span></span>
    * <span data-ttu-id="be256-126">法人</span><span class="sxs-lookup"><span data-stu-id="be256-126">Company</span></span>  
11. <span data-ttu-id="be256-127">[追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="be256-127">Click Add.</span></span>
12. <span data-ttu-id="be256-128">[説明] フィールドに、「実行時にユーザーがログインした法人または会社の説明」というテキストを入力します。</span><span class="sxs-lookup"><span data-stu-id="be256-128">In the Description field, enter the text, Description of the legal entity or company in which a user logged at run-time.</span></span> 
    * <span data-ttu-id="be256-129">実行時にユーザーがログインした法人または会社の説明。</span><span class="sxs-lookup"><span data-stu-id="be256-129">Description of the legal entity or company in which a user logged at run-time.</span></span>  
13. <span data-ttu-id="be256-130">[ルート参照] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="be256-130">Click Root reference.</span></span>
14. <span data-ttu-id="be256-131">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="be256-131">Click OK.</span></span>
15. <span data-ttu-id="be256-132">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="be256-132">Click Save.</span></span>
16. <span data-ttu-id="be256-133">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="be256-133">Close the page.</span></span>
17. <span data-ttu-id="be256-134">[状態の変更] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="be256-134">Click Change status.</span></span>
18. <span data-ttu-id="be256-135">[完了] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="be256-135">Click Complete.</span></span>
19. <span data-ttu-id="be256-136">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="be256-136">Click OK.</span></span>

## <a name="add-a-new-er-model-mapping-configuration"></a><span data-ttu-id="be256-137">新しい ER モデル マッピング コンフィギュレーションを追加する</span><span class="sxs-lookup"><span data-stu-id="be256-137">Add a new ER model-mapping configuration</span></span>
1. <span data-ttu-id="be256-138">[コンフィギュレーションの作成] をクリックすると、ドロップ ダイアログが開きます。</span><span class="sxs-lookup"><span data-stu-id="be256-138">Click Create configuration to open the drop dialog.</span></span>
2. <span data-ttu-id="be256-139">[新規] フィールドで、「データ モデル サンプルのデータ モデルに基づいたモデル マッピング」と入力します。</span><span class="sxs-lookup"><span data-stu-id="be256-139">In the New field, enter 'Model Mapping based on data model Sample data model'.</span></span>
3. <span data-ttu-id="be256-140">[名前] フィールドで、「サンプルのマッピング」と入力します。</span><span class="sxs-lookup"><span data-stu-id="be256-140">In the Name field, type 'Sample mapping'.</span></span>
    * <span data-ttu-id="be256-141">サンプルのマッピング</span><span class="sxs-lookup"><span data-stu-id="be256-141">Sample mapping</span></span>  
4. <span data-ttu-id="be256-142">[コンフィギュレーションの作成] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="be256-142">Click Create configuration.</span></span>
5. <span data-ttu-id="be256-143">[前提条件] セクションを展開します。</span><span class="sxs-lookup"><span data-stu-id="be256-143">Expand the Prerequisites section.</span></span>
    * <span data-ttu-id="be256-144">実装の前提条件グループが自動的に追加されました。</span><span class="sxs-lookup"><span data-stu-id="be256-144">The Implementations prerequisites group has been added automatically.</span></span> <span data-ttu-id="be256-145">このグループには、親データ モデル コンフィギュレーションを参照し「実装」としてマークされている、前提条件コンポーネントが含まれています。</span><span class="sxs-lookup"><span data-stu-id="be256-145">The group contains the prerequisite component that refers to the parent data model configuration and is marked as Implementation.</span></span> <span data-ttu-id="be256-146">つまり、この サンプル マッピング モデル マッピング コンフィギュレーションが、「サンプル データ モデル」データ モデルの実装と見なされます。</span><span class="sxs-lookup"><span data-stu-id="be256-146">This means that this Sample-mapping model-mapping configuration is considered the implementation of the data model, Sample data model.</span></span> <span data-ttu-id="be256-147">したがって、「サンプル データ モデル」モデル コンフィギュレーションがダウンロードされるときに、このコンポーネントは強制的に ER に 「ER リポジトリからのサンプル マッピング」モデル マッピング コンフィギュレーションをダウンロードさせます。</span><span class="sxs-lookup"><span data-stu-id="be256-147">Therefore, this component will force ER to download the model-mapping configuration, Sample mapping from an ER repository when the model configuration, Sample data model, is downloaded.</span></span>   
6. <span data-ttu-id="be256-148">[デザイナー] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="be256-148">Click Designer.</span></span>
    * <span data-ttu-id="be256-149">作成されたモデル マッピング コンフィギュレーションには、作成されたコンフィギュレーションと同じ名前の新しい空白のマッピングが含まれています。</span><span class="sxs-lookup"><span data-stu-id="be256-149">The created model-mapping configuration contains a new blank mapping with the same name as the created configuration.</span></span> <span data-ttu-id="be256-150">選択した親モデル コンフィギュレーションにモデル マッピングが含まれている場合、それは新しいモデル マッピング コンフィギュレーションにコピーされます。</span><span class="sxs-lookup"><span data-stu-id="be256-150">When a selected parent model configuration contains model mappings, they will be copied to a new model-mapping configuration.</span></span>   
7. <span data-ttu-id="be256-151">[デザイナー] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="be256-151">Click Designer.</span></span>
8. <span data-ttu-id="be256-152">ツリーで、'Dynamics 365 for Operations\Table を選択します。</span><span class="sxs-lookup"><span data-stu-id="be256-152">In the tree, select 'Dynamics 365 for Operations\Table'.</span></span>
9. <span data-ttu-id="be256-153">[ルートの追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="be256-153">Click Add root.</span></span>
10. <span data-ttu-id="be256-154">[名前] フィールドに、「Company」と入力します。</span><span class="sxs-lookup"><span data-stu-id="be256-154">In the Name field, type 'Company'.</span></span>
    * <span data-ttu-id="be256-155">法人</span><span class="sxs-lookup"><span data-stu-id="be256-155">Company</span></span>  
11. <span data-ttu-id="be256-156">[テーブル] フィールドに「CompanyInfo」と入力します。</span><span class="sxs-lookup"><span data-stu-id="be256-156">In the Table field, type 'CompanyInfo'.</span></span>
    * <span data-ttu-id="be256-157">CompanyInfo</span><span class="sxs-lookup"><span data-stu-id="be256-157">CompanyInfo</span></span>  
12. <span data-ttu-id="be256-158">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="be256-158">Click OK.</span></span>
13. <span data-ttu-id="be256-159">ツリーで、「会社」を展開します。</span><span class="sxs-lookup"><span data-stu-id="be256-159">In the tree, expand 'Company'.</span></span>
14. <span data-ttu-id="be256-160">ツリーで、「会社\find()」を展開します。</span><span class="sxs-lookup"><span data-stu-id="be256-160">In the tree, expand 'Company\find()'.</span></span>
15. <span data-ttu-id="be256-161">ツリーで、「会社\find()\名前」を選択します。</span><span class="sxs-lookup"><span data-stu-id="be256-161">In the tree, select 'Company\find()\Name'.</span></span>
16. <span data-ttu-id="be256-162">[バインド] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="be256-162">Click Bind.</span></span>
17. <span data-ttu-id="be256-163">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="be256-163">Click Save.</span></span>
18. <span data-ttu-id="be256-164">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="be256-164">Close the page.</span></span>
19. <span data-ttu-id="be256-165">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="be256-165">Close the page.</span></span>
20. <span data-ttu-id="be256-166">アクション ウィンドウで、[設定] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="be256-166">On the Action Pane, click Configurations.</span></span>
21. <span data-ttu-id="be256-167">[ユーザー パラメーター] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="be256-167">Click User parameters.</span></span>
22. <span data-ttu-id="be256-168">[設定の実行] フィールドで、[はい] を選択します。</span><span class="sxs-lookup"><span data-stu-id="be256-168">Select Yes in the Run settings field.</span></span>
23. <span data-ttu-id="be256-169">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="be256-169">Click OK.</span></span>
24. <span data-ttu-id="be256-170">[編集] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="be256-170">Click Edit.</span></span>
25. <span data-ttu-id="be256-171">[ドラフトの実行] フィールドで、[はい] を選択します。</span><span class="sxs-lookup"><span data-stu-id="be256-171">Select Yes in the Run Draft field.</span></span>

## <a name="add-a-new-er-format-configuration"></a><span data-ttu-id="be256-172">新しい ER 形式コンフィギュレーションを追加する</span><span class="sxs-lookup"><span data-stu-id="be256-172">Add a new ER format configuration</span></span>
1. <span data-ttu-id="be256-173">ツリーで、「サンプルのデータ モデル」を選択します。</span><span class="sxs-lookup"><span data-stu-id="be256-173">In the tree, select 'Sample data model'.</span></span>
2. <span data-ttu-id="be256-174">[コンフィギュレーションの作成] をクリックすると、ドロップ ダイアログが開きます。</span><span class="sxs-lookup"><span data-stu-id="be256-174">Click Create configuration to open the drop dialog.</span></span>
3. <span data-ttu-id="be256-175">[新規] フィールドで、「データ モデル サンプルのデータ モデルに基づいた形式」と入力します。</span><span class="sxs-lookup"><span data-stu-id="be256-175">In the New field, enter 'Format based on data model Sample data model'.</span></span>
4. <span data-ttu-id="be256-176">[名前] フィールドで、「サンプルの形式」と入力します。</span><span class="sxs-lookup"><span data-stu-id="be256-176">In the Name field, type 'Sample format'.</span></span>
    * <span data-ttu-id="be256-177">サンプルの形式</span><span class="sxs-lookup"><span data-stu-id="be256-177">Sample format</span></span>  
5. <span data-ttu-id="be256-178">[コンフィギュレーションの作成] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="be256-178">Click Create configuration.</span></span>
6. <span data-ttu-id="be256-179">[デザイナー] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="be256-179">Click Designer.</span></span>
7. <span data-ttu-id="be256-180">[ルートの追加] をクリックして、ドロップ ダイアログを開きます。</span><span class="sxs-lookup"><span data-stu-id="be256-180">Click Add root to open the drop dialog.</span></span>
8. <span data-ttu-id="be256-181">ツリーで、[Text\String] を選択します。</span><span class="sxs-lookup"><span data-stu-id="be256-181">In the tree, select 'Text\String'.</span></span>
9. <span data-ttu-id="be256-182">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="be256-182">Click OK.</span></span>
10. <span data-ttu-id="be256-183">[マッピング] タブをクリックします。</span><span class="sxs-lookup"><span data-stu-id="be256-183">Click the Mapping tab.</span></span>
11. <span data-ttu-id="be256-184">ツリーで、「model」を展開します。</span><span class="sxs-lookup"><span data-stu-id="be256-184">In the tree, expand 'model'.</span></span>
12. <span data-ttu-id="be256-185">ツリーで、「モデル\会社」を選択します。</span><span class="sxs-lookup"><span data-stu-id="be256-185">In the tree, select 'model\Company'.</span></span>
13. <span data-ttu-id="be256-186">[バインド] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="be256-186">Click Bind.</span></span>
14. <span data-ttu-id="be256-187">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="be256-187">Click Save.</span></span>
15. <span data-ttu-id="be256-188">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="be256-188">Close the page.</span></span>
    * <span data-ttu-id="be256-189">テスト目的で、作成された形式のドラフト バージョンを実行します。</span><span class="sxs-lookup"><span data-stu-id="be256-189">Run the draft version of the created format for testing purposes.</span></span>  
16. <span data-ttu-id="be256-190">[実行] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="be256-190">Click Run.</span></span>
    * <span data-ttu-id="be256-191">[バージョン] クイック タブで、[実行] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="be256-191">On the Versions FastTab, click Run.</span></span>  
17. <span data-ttu-id="be256-192">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="be256-192">Click OK.</span></span>
    * <span data-ttu-id="be256-193">この形式コンフィギュレーションを実行中のユーザーがログインしている会社の名前を含む出力を確認します。</span><span class="sxs-lookup"><span data-stu-id="be256-193">Review the output that contains the name of the company in which the user who is running this format configuration is logged into.</span></span> <span data-ttu-id="be256-194">必要なモデル マッピングを含む使用可能なコンフィギュレーションが 1 つしかないので、作成されたモデル マッピング コンフィギュレーションがこの形式コンフィギュレーションによって使用されます。</span><span class="sxs-lookup"><span data-stu-id="be256-194">The created model-mapping configuration is used by this format configuration because there is only one configuration available that contains required model mappings.</span></span>   

## <a name="add-alternative-er-model-mapping-configuration"></a><span data-ttu-id="be256-195">代替 ER モデル マッピング コンフィギュレーションを追加する</span><span class="sxs-lookup"><span data-stu-id="be256-195">Add alternative ER model-mapping configuration</span></span>
1. <span data-ttu-id="be256-196">ツリーで、「サンプルのデータ モデル」を選択します。</span><span class="sxs-lookup"><span data-stu-id="be256-196">In the tree, select 'Sample data model'.</span></span>
2. <span data-ttu-id="be256-197">[コンフィギュレーションの作成] をクリックすると、ドロップ ダイアログが開きます。</span><span class="sxs-lookup"><span data-stu-id="be256-197">Click Create configuration to open the drop dialog.</span></span>
3. <span data-ttu-id="be256-198">[新規] フィールドで、「データ モデル サンプルのデータ モデルに基づいたモデル マッピング」と入力します。</span><span class="sxs-lookup"><span data-stu-id="be256-198">In the New field, enter 'Model Mapping based on data model Sample data model'.</span></span>
4. <span data-ttu-id="be256-199">[名前] フィールドに、「サンプルのマッピング (代替)」と入力します。</span><span class="sxs-lookup"><span data-stu-id="be256-199">In the Name field, type 'Sample mapping (alternative)'.</span></span>
    * <span data-ttu-id="be256-200">サンプルのマッピング (代替)</span><span class="sxs-lookup"><span data-stu-id="be256-200">Sample mapping (alternative)</span></span>  
5. <span data-ttu-id="be256-201">[コンフィギュレーションの作成] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="be256-201">Click Create configuration.</span></span>
6. <span data-ttu-id="be256-202">[デザイナー] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="be256-202">Click Designer.</span></span>
7. <span data-ttu-id="be256-203">[デザイナー] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="be256-203">Click Designer.</span></span>
8. <span data-ttu-id="be256-204">ツリーで、'Dynamics 365 for Operations\Table を選択します。</span><span class="sxs-lookup"><span data-stu-id="be256-204">In the tree, select 'Dynamics 365 for Operations\Table'.</span></span>
9. <span data-ttu-id="be256-205">[ルートの追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="be256-205">Click Add root.</span></span>
10. <span data-ttu-id="be256-206">[名前] フィールドに、「Company」と入力します。</span><span class="sxs-lookup"><span data-stu-id="be256-206">In the Name field, type 'Company'.</span></span>
    * <span data-ttu-id="be256-207">法人</span><span class="sxs-lookup"><span data-stu-id="be256-207">Company</span></span>  
11. <span data-ttu-id="be256-208">[テーブル] フィールドに「CompanyInfo」と入力します。</span><span class="sxs-lookup"><span data-stu-id="be256-208">In the Table field, type 'CompanyInfo'.</span></span>
    * <span data-ttu-id="be256-209">CompanyInfo</span><span class="sxs-lookup"><span data-stu-id="be256-209">CompanyInfo</span></span>  
12. <span data-ttu-id="be256-210">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="be256-210">Click OK.</span></span>
13. <span data-ttu-id="be256-211">[編集] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="be256-211">Click Edit.</span></span>
14. <span data-ttu-id="be256-212">ツリーで、[String\CONCATENATE] を選択します。</span><span class="sxs-lookup"><span data-stu-id="be256-212">In the tree, select 'String\CONCATENATE'.</span></span>
15. <span data-ttu-id="be256-213">[機能の追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="be256-213">Click Add function.</span></span>
16. <span data-ttu-id="be256-214">ツリーで、「会社」を展開します。</span><span class="sxs-lookup"><span data-stu-id="be256-214">In the tree, expand 'Company'.</span></span>
17. <span data-ttu-id="be256-215">ツリーで、「会社\find()」を展開します。</span><span class="sxs-lookup"><span data-stu-id="be256-215">In the tree, expand 'Company\find()'.</span></span>
18. <span data-ttu-id="be256-216">ツリーで、「会社\find()\名前」を選択します。</span><span class="sxs-lookup"><span data-stu-id="be256-216">In the tree, select 'Company\find()\Name'.</span></span>
19. <span data-ttu-id="be256-217">[データ ソースの追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="be256-217">Click Add data source.</span></span>
20. <span data-ttu-id="be256-218">[フォーミュラ] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="be256-218">In the Formula field, type a value.</span></span>
    * <span data-ttu-id="be256-219">CONCATENATE(Company.'find()'.Name, ";",</span><span class="sxs-lookup"><span data-stu-id="be256-219">CONCATENATE(Company.'find()'.Name, ";",</span></span>  
21. <span data-ttu-id="be256-220">ツリーで、「会社\find()\会社 (DataArea)」を選択します。</span><span class="sxs-lookup"><span data-stu-id="be256-220">In the tree, select 'Company\find()\Company(DataArea)'.</span></span>
22. <span data-ttu-id="be256-221">[データ ソースの追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="be256-221">Click Add data source.</span></span>
23. <span data-ttu-id="be256-222">[フォーミュラ] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="be256-222">In the Formula field, type a value.</span></span>
    * <span data-ttu-id="be256-223">CONCATENATE(Company.'find()'.Name, ";", Company.'find()'.DataArea)</span><span class="sxs-lookup"><span data-stu-id="be256-223">CONCATENATE(Company.'find()'.Name, ";", Company.'find()'.DataArea)</span></span>  
24. <span data-ttu-id="be256-224">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="be256-224">Click Save.</span></span>
25. <span data-ttu-id="be256-225">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="be256-225">Close the page.</span></span>
26. <span data-ttu-id="be256-226">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="be256-226">Click Save.</span></span>
27. <span data-ttu-id="be256-227">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="be256-227">Close the page.</span></span>
28. <span data-ttu-id="be256-228">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="be256-228">Close the page.</span></span>
29. <span data-ttu-id="be256-229">[ドラフトの実行] フィールドで、[はい] を選択します。</span><span class="sxs-lookup"><span data-stu-id="be256-229">Select Yes in the Run Draft field.</span></span>

## <a name="use-an-existing-er-model-mapping-configuration"></a><span data-ttu-id="be256-230">既存の ER モデル マッピング コンフィギュレーションを使用する</span><span class="sxs-lookup"><span data-stu-id="be256-230">Use an existing ER model-mapping configuration</span></span>
1. <span data-ttu-id="be256-231">ツリーで、「サンプルのデータ モデル\サンプルの形式」を選択します。</span><span class="sxs-lookup"><span data-stu-id="be256-231">In the tree, select 'Sample data model\Sample format'.</span></span>
2. <span data-ttu-id="be256-232">[実行] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="be256-232">Click Run.</span></span>
    * <span data-ttu-id="be256-233">実行中の ER 形式のデータソースとして選択された未定義データ モデルには、複数のモデル マッピング コンフィギュレーションがあるため、選択されたドラフト版の ER 形式コンフィギュレーションは実行できません。</span><span class="sxs-lookup"><span data-stu-id="be256-233">The selected draft version of the ER format configuration can't be executed because there is more than one model-mapping configuration available for the undefined data model that has been selected as the data source of the running ER format.</span></span>   
    * <span data-ttu-id="be256-234">次に、ER 形式を実行するためのデータ ソースとしてモデル マッピングを使用する代替モデル マッピング コンフィギュレーションを定義します。</span><span class="sxs-lookup"><span data-stu-id="be256-234">Next, you will define the alternative model-mapping configuration as the one from which model mappings will be used as data sources for running ER format.</span></span>   
3. <span data-ttu-id="be256-235">ツリーで、「サンプルのデータ モデル\サンプルのマッピング (代替)」を選択します。</span><span class="sxs-lookup"><span data-stu-id="be256-235">In the tree, select 'Sample data model\Sample mapping (alternative)'.</span></span>
4. <span data-ttu-id="be256-236">[モデル マッピング] フィールドの既定値で [はい] を選択します。</span><span class="sxs-lookup"><span data-stu-id="be256-236">Select Yes in the Default for model-mapping field.</span></span>
5. <span data-ttu-id="be256-237">ツリーで、「サンプルのデータ モデル\サンプルの形式」を選択します。</span><span class="sxs-lookup"><span data-stu-id="be256-237">In the tree, select 'Sample data model\Sample format'.</span></span>
6. <span data-ttu-id="be256-238">[実行] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="be256-238">Click Run.</span></span>
7. <span data-ttu-id="be256-239">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="be256-239">Click OK.</span></span>
    * <span data-ttu-id="be256-240">既定のモデル マッピング コンフィギュレーションが、電子ドキュメントを生成するためにこの形式コンフィギュレーションによって使用されます (作成した出力に会社コードが含まれます)。</span><span class="sxs-lookup"><span data-stu-id="be256-240">The default model-mapping configuration is used by this format configuration for generating the electronic document (the created output contains the company code).</span></span>  



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]