---
title: 法人ごとの ER 形式のパラメーターの設定
description: このトピックでは、法人ごとに電子申告 (ER) 形式のパラメーターを設定する方法について説明します。
author: NickSelin
manager: AnnBe
ms.date: 10/29/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERSolutionTable, EROperationDesigner, ERLookupDesigner, ERComponentLookupStructureEditing
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2019-01-01
ms.dyn365.ops.version: Release 8.1.3
ms.openlocfilehash: b51a7ae8587a3cbb65efc4af574929efcbc8fbf8
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/05/2020
ms.locfileid: "4681475"
---
# <a name="set-up-the-parameters-of-an-er-format-per-legal-entity"></a><span data-ttu-id="06fb4-103">法人ごとの ER 形式のパラメーターの設定</span><span class="sxs-lookup"><span data-stu-id="06fb4-103">Set up the parameters of an ER format per legal entity</span></span>

[!include[banner](../includes/banner.md)]

## <a name="prerequisites"></a><span data-ttu-id="06fb4-104">必要条件</span><span class="sxs-lookup"><span data-stu-id="06fb4-104">Prerequisites</span></span>

<span data-ttu-id="06fb4-105">これらの手順を完了するには、まず [法人ごとに指定されるパラメーターを使用して ER 形式をコンフィギュレーションする](er-app-specific-parameters-configure-format.md) で、手順を完了する必要があります。</span><span class="sxs-lookup"><span data-stu-id="06fb4-105">To complete these steps, you must first complete the steps in the [Configure ER formats to use parameters that are specified per legal entity](er-app-specific-parameters-configure-format.md) topic.</span></span>

<span data-ttu-id="06fb4-106">このトピックの例を完了するには、次のいずれかのロールの Microsoft Dynamics 365 Finance (Finance) にアクセスできる必要があります。</span><span class="sxs-lookup"><span data-stu-id="06fb4-106">To complete the examples in this topic, you must have access to Microsoft Dynamics 365 Finance (Finance) for one of the following roles:</span></span>

- <span data-ttu-id="06fb4-107">電子申告開発者</span><span class="sxs-lookup"><span data-stu-id="06fb4-107">Electronic reporting developer</span></span>
- <span data-ttu-id="06fb4-108">電子申告機能コンサルタント</span><span class="sxs-lookup"><span data-stu-id="06fb4-108">Electronic reporting functional consultant</span></span>
- <span data-ttu-id="06fb4-109">システム管理者</span><span class="sxs-lookup"><span data-stu-id="06fb4-109">System administrator</span></span>

## <a name="import-er-configurations"></a><span data-ttu-id="06fb4-110">ER コンフィギュレーションをインポートする</span><span class="sxs-lookup"><span data-stu-id="06fb4-110">Import ER configurations</span></span>

1.  <span data-ttu-id="06fb4-111">環境にサインインします。</span><span class="sxs-lookup"><span data-stu-id="06fb4-111">Sign in to your environment.</span></span>
2.  <span data-ttu-id="06fb4-112">既定のダッシュボードで、**電子申告** を選択します。</span><span class="sxs-lookup"><span data-stu-id="06fb4-112">On the default dashboard, select **Electronic reporting**.</span></span>
3.  <span data-ttu-id="06fb4-113">**コンフィギュレーションをレポートする** を選択します。</span><span class="sxs-lookup"><span data-stu-id="06fb4-113">Select **Reporting configurations**.</span></span>
4.  <span data-ttu-id="06fb4-114">[法人ごとに指定されるパラメーターを使用して ER 形式をコンフィギュレーションする](er-app-specific-parameters-configure-format.md) トピックで手順を完了している間に、Regulatory Configuration Services (RCS) からエクスポートした構成を現在の Finance のインスタンスにインポートします。</span><span class="sxs-lookup"><span data-stu-id="06fb4-114">Import, into the current instance of Finance, the configurations that you exported from Regulatory Configuration Services (RCS) while you were completing the steps in the [Configure ER formats to use parameters that are specified per legal entity](er-app-specific-parameters-configure-format.md) topic.</span></span> <span data-ttu-id="06fb4-115">各電子申告 (ER) コンフィギュレーションに関して、データモデル、モデル マッピング、および形式の順にこれらの手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="06fb4-115">Follow these steps for each Electronic reporting (ER) configuration, in the following order: data model, model mapping, and formats.</span></span>

    1. <span data-ttu-id="06fb4-116">**交換 \> XML ファイルから読み込む** を選択します。</span><span class="sxs-lookup"><span data-stu-id="06fb4-116">Select **Exchange \> Load from XML file**.</span></span>
    2. <span data-ttu-id="06fb4-117">**参照** を選択して、必要な ER コンフィギュレーションファイルを XML 形式で選択します。</span><span class="sxs-lookup"><span data-stu-id="06fb4-117">Select **Browse** to select the file for the required ER configuration in XML format.</span></span>
    3. <span data-ttu-id="06fb4-118">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="06fb4-118">Select **OK**.</span></span>
    
    <span data-ttu-id="06fb4-119">次の図は、完了時に必要なコンフィギュレーションを示します。</span><span class="sxs-lookup"><span data-stu-id="06fb4-119">The following illustration shows the configurations that you must have when you've finished.</span></span>

    ![ER コンフィギュレーション ページ](./media/GER-AppSpecParms-ImportedConfigurations.PNG)

## <a name="set-up-parameters-for-the-demf-company"></a><span data-ttu-id="06fb4-121">DEMF 会社のパラメーターの設定</span><span class="sxs-lookup"><span data-stu-id="06fb4-121">Set up parameters for the DEMF company</span></span>

<span data-ttu-id="06fb4-122">ER フレームワークを使用して、ER 形式のアプリケーション固有のパラメーターを設定できます。</span><span class="sxs-lookup"><span data-stu-id="06fb4-122">You can use the ER framework to set up application-specific parameters for an ER format.</span></span>

1.  <span data-ttu-id="06fb4-123">**DEMF** 法人を選択します。</span><span class="sxs-lookup"><span data-stu-id="06fb4-123">Select the **DEMF** legal entity.</span></span>
2.  <span data-ttu-id="06fb4-124">コンフィギュレーション ツリーで、**LE データの参照方法を知るための形式** 形式を選択します。</span><span class="sxs-lookup"><span data-stu-id="06fb4-124">In the configurations tree, select the **Format to learn how to lookup LE data** format.</span></span>
3.  <span data-ttu-id="06fb4-125">アクション ウィンドウの、**コンフィギュレーション** タブの、**アプリケーション固有パラメーター** グループで、**設定** を選択します。</span><span class="sxs-lookup"><span data-stu-id="06fb4-125">On the Action Pane, on the **Configurations** tab, in the **Application specific parameters** group, select **Setup**.</span></span>

    ![ER アプリケーション固有パラメーター ページ](./media/GER-AppSpecParms-LookupForm.PNG)
    
    <span data-ttu-id="06fb4-127">**アプリケーション固有パラメーター** ページで、**LE データの参照方法を知るための形式** 形式の **セレクター** データソースに関するルールをコンフィギュレーションできます。</span><span class="sxs-lookup"><span data-stu-id="06fb4-127">On the **Application specific parameters** page, you can configure the rules for the **Selector** data source of the **Format to learn how to lookup LE data** format.</span></span>
    
    <span data-ttu-id="06fb4-128">基本の ER 形式に **ルックアップ** タイプのデータソースがいくつか含まれている場合は、データ ソースに対する一連のルールのコンフィギュレーションを開始する前に、**ルックアップ** クイック タブで目的のデータ ソースを選択する必要があります。</span><span class="sxs-lookup"><span data-stu-id="06fb4-128">If the base ER format will contain several data sources of the **Lookup** type, you must select the desired data source on the **Lookups** FastTab before you can start to configure the set of rules for the data source.</span></span>
    
    <span data-ttu-id="06fb4-129">データ ソースごとに、選択された ER 形式の各バージョンに対する個別のルールをコンフィギュレーションできます。</span><span class="sxs-lookup"><span data-stu-id="06fb4-129">For each data source, you can configure separate rules for each version of the selected ER format.</span></span>
    
    <span data-ttu-id="06fb4-130">基本の ER 形式の選択したバージョンで使用可能なすべてのルックアップ データ ソースのルール セット全体が、ER 形式のアプリケーション固有のパラメーターになります。</span><span class="sxs-lookup"><span data-stu-id="06fb4-130">The whole set of rules for all lookup data sources that are available in the selected version of the base ER format makes up the application-specific parameters for the ER format.</span></span>

4.  <span data-ttu-id="06fb4-131">ER 形式のバージョン **1.1.1** を選択します。</span><span class="sxs-lookup"><span data-stu-id="06fb4-131">Select version **1.1.1** of the ER format.</span></span>
5.  <span data-ttu-id="06fb4-132">**条件** クイック タブで、**追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="06fb4-132">On the **Conditions** FastTab, select **Add**.</span></span>
6.  <span data-ttu-id="06fb4-133">新しいレコードの **コード** フィールドで、ドロップダウン矢印を選択し、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="06fb4-133">In the **Code** field of the new record, select the drop-down arrow to open the lookup.</span></span>

    <span data-ttu-id="06fb4-134">ルックアップでは、選択する税コードの一覧が表示されます。</span><span class="sxs-lookup"><span data-stu-id="06fb4-134">The lookup presents the list of tax codes for selection.</span></span> <span data-ttu-id="06fb4-135">このリストは、基本の ER 形式でコンフィギュレーションされた **Model.Data.Tax** データ ソースにより返されます。</span><span class="sxs-lookup"><span data-stu-id="06fb4-135">This list is returned by the **Model.Data.Tax** data source that has been configured in the base ER format.</span></span> <span data-ttu-id="06fb4-136">このデータ ソースには **名前** フィールドが含まれているため、各税コードの名前がルックアップに表示されます。</span><span class="sxs-lookup"><span data-stu-id="06fb4-136">Because this data source contains the **Name** field, the name of each tax code appears in the lookup.</span></span>

    ![ER アプリケーション固有パラメーター ページ](./media/GER-AppSpecParms-LookupForm-CodeFldPicker.PNG)
    
7.  <span data-ttu-id="06fb4-138">**VAT19** 税コードを選択します。</span><span class="sxs-lookup"><span data-stu-id="06fb4-138">Select the **VAT19** tax code.</span></span>
8.  <span data-ttu-id="06fb4-139">新しいレコードの **ルックアップの結果** フィールドで、ドロップダウン矢印を選択し、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="06fb4-139">In the **Lookup result** field of the new record, select the drop-down arrow to open the lookup.</span></span> <span data-ttu-id="06fb4-140">ルックアップにより、選択する TaxationLevel format 形式列挙の値の一覧が表示されます。</span><span class="sxs-lookup"><span data-stu-id="06fb4-140">The lookup presents the list of values for the TaxationLevel format enumeration for selection.</span></span>

    <span data-ttu-id="06fb4-141">サインインしているユーザーの優先言語としてドイツ語が選択されている場合、基本の ER 形式で翻訳されていれば、ルックアップの値のラベルはドイツ語になります。</span><span class="sxs-lookup"><span data-stu-id="06fb4-141">Note that, if German is selected as the preferred language of the user that you're signed in as, the labels of the values in the lookup will be in German, provided that they have been translated in the base ER format.</span></span> <span data-ttu-id="06fb4-142">さらに、ルックアップ データ ソースのラベルが翻訳されている場合、そのラベルは **ルックアップ** タブのユーザーの優先言語で表示されます。</span><span class="sxs-lookup"><span data-stu-id="06fb4-142">Additionally, if the label of a lookup data source has been translated, that label will appear in the user's preferred language on the **Lookups** tab.</span></span>

    ![ER アプリケーション固有パラメーター ページ](./media/GER-AppSpecParms-LookupForm-LookupFldPicker.PNG)

9.  <span data-ttu-id="06fb4-144">**通常の課税** 値を選択します。</span><span class="sxs-lookup"><span data-stu-id="06fb4-144">Select the **Regular taxation** value.</span></span>

    <span data-ttu-id="06fb4-145">このレコードを追加することにより、次のルールを定義します: **セレクター** ルックアップ データ ソースが要求され、**VAT19** 税コードが引数として渡されるたびに、**通常の課税** が要求された課税レベルとして返されます。</span><span class="sxs-lookup"><span data-stu-id="06fb4-145">By adding this record, you define the following rule: Whenever the **Selector** lookup data source is requested, and the **VAT19** tax code is passed as an argument, **Regular taxation** will be returned as the requested taxation level.</span></span>

10. <span data-ttu-id="06fb4-146">**追加** を選択し、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="06fb4-146">Select **Add**, and then follow these steps:</span></span>

    1. <span data-ttu-id="06fb4-147">**コード** フィールドで、**InVAT19** 税コードを選択します。</span><span class="sxs-lookup"><span data-stu-id="06fb4-147">In the **Code** field, select the **InVAT19** tax code.</span></span>
    2. <span data-ttu-id="06fb4-148">**ルックアップの結果** フィールドで、**通常の課税** 値を選択します。</span><span class="sxs-lookup"><span data-stu-id="06fb4-148">In the **Lookup result** field, select the **Regular taxation** value.</span></span>
    
11. <span data-ttu-id="06fb4-149">**追加** を再度選択し、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="06fb4-149">Select **Add** again, and then follow these steps:</span></span>

    1. <span data-ttu-id="06fb4-150">**コード** フィールドで、**VAT7** 税コードを選択します。</span><span class="sxs-lookup"><span data-stu-id="06fb4-150">In the **Code** field, select the **VAT7** tax code.</span></span>
    2. <span data-ttu-id="06fb4-151">**ルックアップの結果** フィールドで、**減額課税** 値を選択します。</span><span class="sxs-lookup"><span data-stu-id="06fb4-151">In the **Lookup result** field, select the **Reduced taxation** value.</span></span>
    
12. <span data-ttu-id="06fb4-152">**追加** を再度選択し、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="06fb4-152">Select **Add** again, and then follow these steps:</span></span>

    1. <span data-ttu-id="06fb4-153">**コード** フィールドで、**InVAT7** 税コードを選択します。</span><span class="sxs-lookup"><span data-stu-id="06fb4-153">In the **Code** field, select the **InVAT7** tax code.</span></span>
    2. <span data-ttu-id="06fb4-154">**ルックアップの結果** フィールドで、**減額課税** 値を選択します。</span><span class="sxs-lookup"><span data-stu-id="06fb4-154">In the **Lookup result** field, select the **Reduced taxation** value.</span></span>
    
13. <span data-ttu-id="06fb4-155">**追加** を再度選択し、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="06fb4-155">Select **Add** again, and then follow these steps:</span></span>

    1. <span data-ttu-id="06fb4-156">**コード** フィールドで、**THIRD** 税コードを選択します。</span><span class="sxs-lookup"><span data-stu-id="06fb4-156">In the **Code** field, select the **THIRD** tax code.</span></span>
    2. <span data-ttu-id="06fb4-157">**ルックアップの結果** フィールドで、**非課税** 値を選択します。</span><span class="sxs-lookup"><span data-stu-id="06fb4-157">In the **Lookup result** field, select the **No taxation** value.</span></span>
    
14. <span data-ttu-id="06fb4-158">**追加** を再度選択し、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="06fb4-158">Select **Add** again, and then follow these steps:</span></span>

    1. <span data-ttu-id="06fb4-159">**コード** フィールドで、**InVAT0** 税コードを選択します。</span><span class="sxs-lookup"><span data-stu-id="06fb4-159">In the **Code** field, select the **InVAT0** tax code.</span></span>
    2. <span data-ttu-id="06fb4-160">**ルックアップの結果** フィールドで、**非課税** 値を選択します。</span><span class="sxs-lookup"><span data-stu-id="06fb4-160">In the **Lookup result** field, select the **No taxation** value.</span></span>
    
15. <span data-ttu-id="06fb4-161">**追加** を再度選択し、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="06fb4-161">Select **Add** again, and then follow these steps:</span></span>

    1. <span data-ttu-id="06fb4-162">**コード** フィールドで、**\*空白でない\*** オプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="06fb4-162">In the **Code** field, select the **\*Not blank\*** option.</span></span>
    2. <span data-ttu-id="06fb4-163">**ルックアップの結果** フィールドで、**その他** の値を選択します。</span><span class="sxs-lookup"><span data-stu-id="06fb4-163">In the **Lookup result** field, select the **Other** value.</span></span>
    
    <span data-ttu-id="06fb4-164">この最後のレコードを追加することにより、次のルールを定義します: 引数として渡された税コードが前述のルールのいずれも満たさない場合、ルックアップ データ ソースは、要求された課税レベルとして **その他** を返します。</span><span class="sxs-lookup"><span data-stu-id="06fb4-164">By adding this last record, you define the following rule: Whenever the tax code that is passed as an argument doesn't satisfy any of the previous rules, the lookup data source will return **Other** as the requested taxation level.</span></span>

    ![ER アプリケーション固有パラメーター ページ](./media/GER-AppSpecParms-LookupForm-RulesSet.PNG)
    
16. <span data-ttu-id="06fb4-166">**ステータス** フィールドで **完了** を選択します。</span><span class="sxs-lookup"><span data-stu-id="06fb4-166">In the **State** field, select **Completed**.</span></span>

    <span data-ttu-id="06fb4-167">**完了** または **共有** のいずれかのステータスがある ER 形式バージョンを実行する場合、この一連のルールは **完了** のステータスである必要があります。</span><span class="sxs-lookup"><span data-stu-id="06fb4-167">When you run an ER format version that has a status of either **Completed** or **Shared**, this set of rules must be in the **Completed** state.</span></span> <span data-ttu-id="06fb4-168">それ以外の場合、**セレクター** ルックアップ データ ソースの実行中に、形式がこの一連のルールからデータを読み込もうとすると、基本の ER 形式の実行が中断されます。</span><span class="sxs-lookup"><span data-stu-id="06fb4-168">Otherwise, execution of the base ER format will be interrupted when the format tries to load data from this set of rules while the **Selector** lookup data source is being run.</span></span>
    
    <span data-ttu-id="06fb4-169">**ドラフト** のステータスがある ER 形式バージョンを実行すると、基本の ER 形式は、そのステータスに関係なくこの一連のルールにアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="06fb4-169">When you run an ER format version that has a status of **Draft**, the base ER format can access this set of rules, regardless of its state.</span></span>
    
17. <span data-ttu-id="06fb4-170">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="06fb4-170">Select **Save**.</span></span>
18. <span data-ttu-id="06fb4-171">**アプリケーション固有パラメーター** ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="06fb4-171">Close the **Application specific parameters** page.</span></span>

## <a name="run-the-er-format-in-the-demf-company"></a><span data-ttu-id="06fb4-172">DEMF 会社で ER 形式を実行します。</span><span class="sxs-lookup"><span data-stu-id="06fb4-172">Run the ER format in the DEMF company</span></span>

1.  <span data-ttu-id="06fb4-173">コンフィギュレーション ツリーで、**LE データの参照方法を知るための形式** 形式を選択します。</span><span class="sxs-lookup"><span data-stu-id="06fb4-173">In the configurations tree, select the **Format to learn how to lookup LE data** format.</span></span>
2.  <span data-ttu-id="06fb4-174">アクション ウィンドウで、**実行** を選択します。</span><span class="sxs-lookup"><span data-stu-id="06fb4-174">On the Action Pane, select **Run**.</span></span>
3.  <span data-ttu-id="06fb4-175">表示されるダイアログ ボックスで、**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="06fb4-175">In the dialog box that appears, select **OK**.</span></span>
4.  <span data-ttu-id="06fb4-176">生成される明細書をダウンロードし、ローカルに保管します。</span><span class="sxs-lookup"><span data-stu-id="06fb4-176">Download the statement that is generated and store it locally.</span></span>

    <span data-ttu-id="06fb4-177">生成された明細書で、**InVAT7** 税コードの集計が **減額** レベルに、**VAT19** および **InVA19** 税コードの集計が **通常** レベルに設定されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="06fb4-177">In the generated statement, notice that the summary of the **InVAT7** tax code has been put on the **Reduced** level, and the summaries of the **VAT19** and **InVA19** tax codes have been put on the **Regular** level.</span></span> <span data-ttu-id="06fb4-178">この動作は、法人に依存する一連のルールのコンフィギュレーションによって決まります。</span><span class="sxs-lookup"><span data-stu-id="06fb4-178">This behavior is determined by the configuration in the legal entity–dependent set of rules.</span></span>
    
5.  <span data-ttu-id="06fb4-179">**税 \> 間接税 \> 売上税 \> 売上税コード** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="06fb4-179">Go to **Tax \> Indirect taxes \> Sales tax \> Sales tax codes**.</span></span>
6.  <span data-ttu-id="06fb4-180">**InVAT7** 税コードを選択します。</span><span class="sxs-lookup"><span data-stu-id="06fb4-180">Select the **InVAT7** tax code.</span></span>
7.  <span data-ttu-id="06fb4-181">アクション ウィンドウの、**売上税コード** タブの、**照会** グループで、**転記済売上税** を選択して、税コードごとに適用された税額と税率に関する情報を表示します。</span><span class="sxs-lookup"><span data-stu-id="06fb4-181">On the Action Pane, on the **Sales tax code** tab, in the **Inquiries** group, select **Posted sales tax** to view information about the tax value and applied tax rate per tax code.</span></span>

    ![転記済売上税ページ](./media/GER-AppSpecParms-Statement.PNG)

8.  <span data-ttu-id="06fb4-183">転記済売上税ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="06fb4-183">Close the Posted sales tax page.</span></span>

## <a name="set-up-parameters-for-the-usmf-company"></a><span data-ttu-id="06fb4-184">USMF 会社のパラメーターの設定</span><span class="sxs-lookup"><span data-stu-id="06fb4-184">Set up parameters for the USMF company</span></span>

1.  <span data-ttu-id="06fb4-185">**USMF** 法人を選択します。</span><span class="sxs-lookup"><span data-stu-id="06fb4-185">Select the **USMF** legal entity.</span></span>
2.  <span data-ttu-id="06fb4-186">**組織管理 \> 電子申告 \> コンフィギュレーション** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="06fb4-186">Go to **Organization administration \> Electronic reporting \> Configurations**.</span></span>
3.  <span data-ttu-id="06fb4-187">コンフィギュレーション ツリーで、**パラメーター化された呼び出しを知るためのモデル** 項目を展開し、**パラメーター化された呼び出しを知るための形式** を展開してから、**LE データの参照方法を知るための形式** 形式を選択します。</span><span class="sxs-lookup"><span data-stu-id="06fb4-187">In the configurations tree, expand the **Model to learn parameterized calls** item, expand the **Format to learn parameterized calls** item, and select the **Format to learn how to lookup LE data** format.</span></span>
4.  <span data-ttu-id="06fb4-188">アクション ウィンドウの、**コンフィギュレーション** タブの、**アプリケーション固有パラメーター** グループで、**設定** を選択します。</span><span class="sxs-lookup"><span data-stu-id="06fb4-188">On the Action Pane, on the **Configurations** tab, in the **Application specific parameters** group, select **Setup**.</span></span>
5.  <span data-ttu-id="06fb4-189">選択された ER 形式のバージョン **1.1.1** を選択します。</span><span class="sxs-lookup"><span data-stu-id="06fb4-189">Select version **1.1.1** of the selected ER format.</span></span>
6.  <span data-ttu-id="06fb4-190">**条件** クイック タブで、**追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="06fb4-190">On the **Conditions** FastTab, select **Add**.</span></span>
7.  <span data-ttu-id="06fb4-191">新しいレコードの **コード** フィールドで、ドロップダウン矢印を選択し、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="06fb4-191">In the **Code** field of the new record, select the drop-down arrow to open the lookup.</span></span>

    <span data-ttu-id="06fb4-192">このルックアップでは、選択する **USMF** 会社税の税コードの一覧が表示されるようになります。</span><span class="sxs-lookup"><span data-stu-id="06fb4-192">The lookup now presents the list of tax codes for the **USMF** company tax for selection.</span></span>

    ![ER アプリケーション固有パラメーター ページ](./media/GER-AppSpecParms-LookupForm-CodeFldPicker2.PNG)
    
8.  <span data-ttu-id="06fb4-194">**EXEMPT** 税コードを選択します。</span><span class="sxs-lookup"><span data-stu-id="06fb4-194">Select the **EXEMPT** tax code.</span></span>
9.  <span data-ttu-id="06fb4-195">新しいレコードの **ルックアップの結果** フィールドで、**非課税** 値を選択します。</span><span class="sxs-lookup"><span data-stu-id="06fb4-195">In the **Lookup resul** t field of the new record, select the **No taxation** value.</span></span>
10. <span data-ttu-id="06fb4-196">**追加** を再度選択します。</span><span class="sxs-lookup"><span data-stu-id="06fb4-196">Select **Add** again.</span></span>
11. <span data-ttu-id="06fb4-197">新しいレコードの **コード** フィールドで、**\*空白でない\*** オプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="06fb4-197">In the **Code** field of the new record, select the **\*Not blank\*** option.</span></span>
12. <span data-ttu-id="06fb4-198">新しいレコードの **ルックアップの結果** フィールドで、**通常の課税** 値を選択します。</span><span class="sxs-lookup"><span data-stu-id="06fb4-198">In the **Lookup result** field of the new record, select the **Regular taxation** value.</span></span>
13. <span data-ttu-id="06fb4-199">**ステータス** フィールドで **完了** を選択します。</span><span class="sxs-lookup"><span data-stu-id="06fb4-199">In the **State** field, select **Completed**.</span></span>
14. <span data-ttu-id="06fb4-200">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="06fb4-200">Select **Save**.</span></span>

    ![ER アプリケーション固有パラメーター ページ](./media/GER-AppSpecParms-LookupForm-RulesSet2.PNG)
    
15. <span data-ttu-id="06fb4-202">**アプリケーション固有パラメーター** ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="06fb4-202">Close the **Application specific parameters** page.</span></span>

## <a name="run-the-er-format-in-the-usmf-company"></a><span data-ttu-id="06fb4-203">USMF 会社で ER 形式を実行します。</span><span class="sxs-lookup"><span data-stu-id="06fb4-203">Run the ER format in the USMF company</span></span>

1.  <span data-ttu-id="06fb4-204">コンフィギュレーション ツリーで、**LE データの参照方法を知るための形式** 形式を選択します。</span><span class="sxs-lookup"><span data-stu-id="06fb4-204">In the configurations tree, select the **Format to learn how to lookup LE data** format.</span></span>
2.  <span data-ttu-id="06fb4-205">アクション ウィンドウで、**実行** を選択します。</span><span class="sxs-lookup"><span data-stu-id="06fb4-205">On the Action Pane, select **Run**.</span></span>
3.  <span data-ttu-id="06fb4-206">表示されるダイアログ ボックスで、**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="06fb4-206">In the dialog box that appears, select **OK**.</span></span>
4.  <span data-ttu-id="06fb4-207">生成される明細書をダウンロードし、ローカルに保管します。</span><span class="sxs-lookup"><span data-stu-id="06fb4-207">Download the statement that is generated and store it locally.</span></span>

    <span data-ttu-id="06fb4-208">生成された明細書で、ER 形式に対する調整なしで、異なる法人に対して同じ ER 形式を再使用したことを確認します。</span><span class="sxs-lookup"><span data-stu-id="06fb4-208">In the generated statement, notice that you've now reused the same ER format for a different legal entity, but without making any adjustments to the ER format.</span></span>

## <a name="reuse-legal-entitydependent-parameters"></a><span data-ttu-id="06fb4-209">法人に依存するパラメーターの再利用</span><span class="sxs-lookup"><span data-stu-id="06fb4-209">Reuse legal entity–dependent parameters</span></span>

### <a name="export-parameters"></a><span data-ttu-id="06fb4-210">パラメーターのエクスポート</span><span class="sxs-lookup"><span data-stu-id="06fb4-210">Export parameters</span></span>

1.  <span data-ttu-id="06fb4-211">**組織管理  \> ワークスペース \> 電子申告** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="06fb4-211">Go to **Organization administration \> Workspaces \> Electronic reporting**.</span></span>
2.  <span data-ttu-id="06fb4-212">**コンフィギュレーションをレポートする** を選択します。</span><span class="sxs-lookup"><span data-stu-id="06fb4-212">Select **Reporting configurations**.</span></span>
3.  <span data-ttu-id="06fb4-213">コンフィギュレーション ツリーで、**LE データの参照方法を知るための形式** 形式を選択します。</span><span class="sxs-lookup"><span data-stu-id="06fb4-213">In the configurations tree, select the **Format to learn how to lookup LE data** format.</span></span>
4.  <span data-ttu-id="06fb4-214">アクション ウィンドウの、**コンフィギュレーション** タブの、**アプリケーション固有パラメーター** グループで、**設定** を選択します。</span><span class="sxs-lookup"><span data-stu-id="06fb4-214">On the Action Pane, on the **Configurations** tab, in the **Application specific parameters** group, select **Setup**.</span></span>
5.  <span data-ttu-id="06fb4-215">ER 形式のバージョン **1.1.1** を選択します。</span><span class="sxs-lookup"><span data-stu-id="06fb4-215">Select version **1.1.1** of the ER format.</span></span>
6.  <span data-ttu-id="06fb4-216">アクション ウィンドウで、**エクスポート** を選択します。</span><span class="sxs-lookup"><span data-stu-id="06fb4-216">On the Action Pane, select **Export**.</span></span>
7.  <span data-ttu-id="06fb4-217">生成されるファイルをダウンロードし、ローカルに保管します。</span><span class="sxs-lookup"><span data-stu-id="06fb4-217">Download the file that is generated and store it locally.</span></span>

    <span data-ttu-id="06fb4-218">コンフィギュレーションされる一連のアプリケーション固有のパラメーターが、XML ファイルとしてエクスポートされました。</span><span class="sxs-lookup"><span data-stu-id="06fb4-218">The configured set of application-specific parameters has now been exported as an XML file.</span></span>

### <a name="import-parameters"></a><span data-ttu-id="06fb4-219">パラメーターのインポート</span><span class="sxs-lookup"><span data-stu-id="06fb4-219">Import parameters</span></span>

1.  <span data-ttu-id="06fb4-220">ER 形式のバージョン **1.1.2** を選択します。</span><span class="sxs-lookup"><span data-stu-id="06fb4-220">Select version **1.1.2** of the ER format.</span></span>
2.  <span data-ttu-id="06fb4-221">アクション ウィンドウで、**インポート** を選択します。</span><span class="sxs-lookup"><span data-stu-id="06fb4-221">On the Action Pane, select **Import**.</span></span>
3.  <span data-ttu-id="06fb4-222">**はい** を選択して、この形式バージョンに対する既存のアプリケーション固有のパラメーターを上書きすることを確認します。</span><span class="sxs-lookup"><span data-stu-id="06fb4-222">Select **Yes** to confirm that you want to override the existing application-specific parameters for this format version.</span></span>
4.  <span data-ttu-id="06fb4-223">**参照** を選択して、バージョン **1.1.1** のエクスポートされたアプリケーション固有のパラメーターを含むファイルを検索します。</span><span class="sxs-lookup"><span data-stu-id="06fb4-223">Select **Browse** to find the file that contains the exported application-specific parameters for version **1.1.1**.</span></span>
5.  <span data-ttu-id="06fb4-224">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="06fb4-224">Select **OK**.</span></span>

    <span data-ttu-id="06fb4-225">ER 形式のバージョン **1.1.2** には、バージョン **1.1.1** に対して最初に設定したものと同じアプリケーション固有のパラメーターがあります。</span><span class="sxs-lookup"><span data-stu-id="06fb4-225">Version **1.1.2** of the ER format now has the same application-specific parameters that you originally configured for version **1.1.1**.</span></span>
    
    <span data-ttu-id="06fb4-226">ER 形式のアプリケーション固有のパラメーターは、法人に依存することに注意してください。</span><span class="sxs-lookup"><span data-stu-id="06fb4-226">Note that the application-specific parameters of an ER format are legal entity–dependent.</span></span> <span data-ttu-id="06fb4-227">1 つの法人に対してコンフィギュレーションされたアプリケーション固有のパラメーターを別の法人で再利用するには、最初の法人にサインイン中にそれらをエクスポートし、他の法人にサインインした後にそれらをインポートする必要があります。</span><span class="sxs-lookup"><span data-stu-id="06fb4-227">To reuse the application-specific parameters that were configured for one legal entity in a different legal entity, you must export them while you're signed in to the first legal entity and then import them after you sign in to the other legal entity.</span></span>

    <span data-ttu-id="06fb4-228">この方法を使用して、最初に Finance の 1 つのインスタンスでコンフィギュレーションされた ER 形式に関連するアプリケーション固有のパラメーターを Finance の別のインスタンスに転送することもできます。</span><span class="sxs-lookup"><span data-stu-id="06fb4-228">You can also use this approach to transfer an ER format related application-specific parameters that were originally configured in one instance of Finance to another instance of Finance.</span></span>

    <span data-ttu-id="06fb4-229">ER 形式の 1 つのバージョンに対してアプリケーション固有のパラメーターをコンフィギュレーションし、同じ形式の新しいバージョンを現在の Finance インスタンスにインポートする場合、既存のアプリケーション固有のパラメーターはインポートされたバージョンには適用されないことに注意してください。</span><span class="sxs-lookup"><span data-stu-id="06fb4-229">Be aware that if you configure application-specific parameters for one version of an ER format and import a higher version of the same format into the current Finance instance, the existing application-specific parameters won't be applied for the imported version.</span></span>
    
    <span data-ttu-id="06fb4-230">また、インポートのファイルを選択すると、そのファイル内のアプリケーション固有のパラメーターの構造が、インポート用に選択されたER 形式の **ルックアップ** タイプの対応するデータ ソースの構造と比較されることにも注意してください。</span><span class="sxs-lookup"><span data-stu-id="06fb4-230">Also be aware that, when you select a file for import, the structure of the application-specific parameters in that file is compared with the structure of the corresponding data source of the **Lookup** type in the ER format that is selected for import.</span></span> <span data-ttu-id="06fb4-231">インポートは、各アプリケーション固有パラメーターの構造が、インポート用に選択された ER 形式の対応するデータ ソースの構造と一致する場合に実行されます。</span><span class="sxs-lookup"><span data-stu-id="06fb4-231">The import is done when the structure of each application-specific parameter matches the structure of the corresponding data source in the ER format that is selected for import.</span></span> <span data-ttu-id="06fb4-232">構造が一致しない場合は、インポートを実行できないことを示す警告メッセージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="06fb4-232">If the structures don't match, you receive a warning message that states that the import can't be done.</span></span> <span data-ttu-id="06fb4-233">インポートを強制的に実行すると、選択した ER 形式に対する既存のアプリケーション固有のパラメーターがクリーンアップされ、最初から設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="06fb4-233">If you force the import to be done, the existing application-specific parameters for the selected ER format will be cleaned up, and you must set them up from the beginning.</span></span>

## <a name="relationship-between-application-specific-parameters-and-an-er-format"></a><span data-ttu-id="06fb4-234">アプリケーション固有のパラメーターと ER 形式間の関係</span><span class="sxs-lookup"><span data-stu-id="06fb4-234">Relationship between application-specific parameters and an ER format</span></span>

<span data-ttu-id="06fb4-235">ER 形式とアプリケーション固有のパラメーター間の関係は、ER 形式のインスタンスに依存しない固有の ID コードによって確立されます。</span><span class="sxs-lookup"><span data-stu-id="06fb4-235">The relationship between an ER format and its application-specific parameters is established by the ER format's instance-independent unique identification code.</span></span> <span data-ttu-id="06fb4-236">したがって、ER 形式を Finance から削除する場合、ER 形式に対してコンフィギュレーションされるアプリケーション固有のパラメーターは Finance の現在のインスタンスに保持されます。</span><span class="sxs-lookup"><span data-stu-id="06fb4-236">Therefore, when you remove an ER format from Finance, the application-specific parameters that are configured for the ER format are kept in the current instance of Finance.</span></span> <span data-ttu-id="06fb4-237">基本の ER 形式が Finance のこのインスタンスに再インポートされると、いつでもアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="06fb4-237">They can be accessed whenever the base ER format is reimported into this instance of Finance.</span></span>

## <a name="access-application-specific-parameters-by-using-the-er-framework"></a><span data-ttu-id="06fb4-238">ER フレームワークを使用してアプリケーション固有のパラメーターにアクセスする</span><span class="sxs-lookup"><span data-stu-id="06fb4-238">Access application-specific parameters by using the ER framework</span></span>

<span data-ttu-id="06fb4-239">前の例では、ER フレームワークを使用して ER 形式のアプリケーション固有のパラメーターにアクセスできました。</span><span class="sxs-lookup"><span data-stu-id="06fb4-239">In the preceding example, you have accessed application-specific parameters of an ER format by using the ER framework.</span></span> <span data-ttu-id="06fb4-240">この方法では、特定の ER 形式のアプリケーション固有のパラメーターへのアクセスを制限することはできません。</span><span class="sxs-lookup"><span data-stu-id="06fb4-240">This approach doesn't let you restrict access to the application-specific parameters of a specific ER format.</span></span> <span data-ttu-id="06fb4-241">制限を適用する必要がある場合は、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="06fb4-241">If you must apply such restrictions, follow these steps.</span></span> 

1.  <span data-ttu-id="06fb4-242">既存の **ERSolutionAppSpecificParametersDesigner** メニュー項目を再利用するか、または独自の **ERSolutionAppSpecificParametersDesigner** メニュー項目を実装します。</span><span class="sxs-lookup"><span data-stu-id="06fb4-242">Either reuse an existing **ERSolutionAppSpecificParametersDesigner** menu item, or implement your own **ERSolutionAppSpecificParametersDesigner** menu item.</span></span>

    ![Visual Studio ページ](./media/GER-AppSpecParms-LookupForm-Access1.PNG)
    
2.  <span data-ttu-id="06fb4-244">次の手順のいずれかを実行します。</span><span class="sxs-lookup"><span data-stu-id="06fb4-244">Follow one of these steps:</span></span>

    1.  <span data-ttu-id="06fb4-245">新しいメニュー項目ボタンを作成し、**データ ソース** プロパティを **ERSolutionTable** に設定することにより **ERSolutionTable** テーブルから対応するレコードにリンクします。</span><span class="sxs-lookup"><span data-stu-id="06fb4-245">Create a new menu item button, and link it to the corresponding record from the **ERSolutionTable** table by setting its **Data Source** property to **ERSolutionTable**.</span></span>
    
        ![Visual Studio ページ](./media/GER-AppSpecParms-LookupForm-Access2.PNG)
        
    2.  <span data-ttu-id="06fb4-247">簡易ボタンを作成し、次の例に示すように **クリック済** メソッドを上書きします。</span><span class="sxs-lookup"><span data-stu-id="06fb4-247">Create a simple button, and override the **Clicked** method as shown in the following example.</span></span>
    
        <span data-ttu-id="06fb4-248">この方法を使用すると、一意のソリューション ID (**GUID** 値で定義された) を指定して、特定の ER 形式とそれから派生した子孫コピーのみのアプリケーション固有のパラメーターへのアクセスを許可できます。</span><span class="sxs-lookup"><span data-stu-id="06fb4-248">By using this approach, you can specify a unique solution ID (defined via the **GUID** value) to allow access to the application-specific parameters of only a specific ER format and descendant copies that have been derived from it.</span></span>
        
        ```xpp
        public void clicked()
            {
                super();

                ERSolutionTable solutionTableRecord = ERSolutionTable::findByGUID(str2Guid('ADACCB2F-EFD1-4C90-877D-7E1E5D1AEE92'));

                Args args = new Args();
                args.record(solutionTableRecord);
                args.caller(this);

                new MenuFunction(menuItemDisplayStr(ERSolutionAppSpecificParametersDesigner), MenuItemType::Display)
                    .run(args);
            }
        ```

## <a name="additional-resources"></a><span data-ttu-id="06fb4-249">追加リソース</span><span class="sxs-lookup"><span data-stu-id="06fb4-249">Additional resources</span></span>

[<span data-ttu-id="06fb4-250">電子申告のフォーミュラ デザイナー</span><span class="sxs-lookup"><span data-stu-id="06fb4-250">Formula designer in Electronic reporting</span></span>](general-electronic-reporting-formula-designer.md)

[<span data-ttu-id="06fb4-251">法人ごとに指定されたパラメーターを使用するよう ER 形式を構成する</span><span class="sxs-lookup"><span data-stu-id="06fb4-251">Configure ER formats to use parameters that are specified per legal entity</span></span>](er-app-specific-parameters-configure-format.md)
