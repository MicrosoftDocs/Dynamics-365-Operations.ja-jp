---
title: 新しい ER ソリューションを設計してカスタム レポートを印刷する
description: このトピックでは、電子レポート (ER) を設計してカスタム レポートを印刷する方法について説明します。
author: NickSelin
ms.date: 08/10/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, ERParameters, ERDataModelDesigner, ERModelMappingTable, ERModelMappingDesigner, EROperationDesigner, ERVendorTable
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: 220314
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0f5a3ac7cae58d17409ea081ec30f61cecf29ce9
ms.sourcegitcommit: 15aacd0e109b05c7281407b5bba4e6cd99116c28
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/10/2021
ms.locfileid: "6224037"
---
# <a name="design-a-new-er-solution-to-print-a-custom-report"></a><span data-ttu-id="00999-103">新しい ER ソリューションを設計してカスタム レポートを印刷する</span><span class="sxs-lookup"><span data-stu-id="00999-103">Design a new ER solution to print a custom report</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="00999-104">以下の手順では、システム管理者、電子レポートの開発者、電子レポート機能のコンサルタントのロールが付与されているユーザーが、ER のフレーム ワークを構成し、求められる ER ソリューションを構成して、特定のビジネス ドメインのデータにアクセスし、 Microsoft Office 形式でカスタムレポートを生成する方法を説明します。</span><span class="sxs-lookup"><span data-stu-id="00999-104">The following steps explain how a user in the System Administrator, Electronic Reporting Developer, or Electronic Reporting Functional Consultant role can configure parameters of the ER framework, design the required ER configurations of a new ER solution to access the data of a particular business domain, and generate a custom report in Microsoft Office format.</span></span> <span data-ttu-id="00999-105">これらの設定を **USMF** 社を使用して説明します。</span><span class="sxs-lookup"><span data-stu-id="00999-105">These steps can be completed in the **USMF** company.</span></span>

- [<span data-ttu-id="00999-106">ER フレームワークの構成</span><span class="sxs-lookup"><span data-stu-id="00999-106">Configure the ER framework</span></span>](#ConfigureFramework)

    - [<span data-ttu-id="00999-107">ER パラメーターの構成</span><span class="sxs-lookup"><span data-stu-id="00999-107">Configure ER parameters</span></span>](#ConfigureParameters)
    - [<span data-ttu-id="00999-108">ER 構成 プロバイダーをアクティブにする</span><span class="sxs-lookup"><span data-stu-id="00999-108">Activate an ER configuration provider</span></span>](#ActivateProvider)

        - [<span data-ttu-id="00999-109">ER 構成 プロバイダーの一覧を確認</span><span class="sxs-lookup"><span data-stu-id="00999-109">Review the list of ER configuration providers</span></span>](#ReviewProvidersList)
        - [<span data-ttu-id="00999-110">新しい ER 構成 プロバイダーを追加</span><span class="sxs-lookup"><span data-stu-id="00999-110">Add a new ER configuration provider</span></span>](#AddProvider)
        - [<span data-ttu-id="00999-111">ER 構成 プロバイダーをアクティブにする</span><span class="sxs-lookup"><span data-stu-id="00999-111">Activate an ER configuration provider</span></span>](#ActivateAddedProvider)

- [<span data-ttu-id="00999-112">ドメイン固有のデータ モデルを設計する</span><span class="sxs-lookup"><span data-stu-id="00999-112">Design a domain-specific data model</span></span>](#DesignModel)

    - [<span data-ttu-id="00999-113">新たなデータ モデルのインポート</span><span class="sxs-lookup"><span data-stu-id="00999-113">Import a new data model configuration</span></span>](#ImportDataModel)
    - [<span data-ttu-id="00999-114">新しいデータ モデル 構成の作成</span><span class="sxs-lookup"><span data-stu-id="00999-114">Create a new data model configuration</span></span>](#DesignDataModel)

        - [<span data-ttu-id="00999-115">データ モデルに名前をつける</span><span class="sxs-lookup"><span data-stu-id="00999-115">Name the data model</span></span>](#NameDataModel)
        - [<span data-ttu-id="00999-116">データ モデル フィールドを追加する</span><span class="sxs-lookup"><span data-stu-id="00999-116">Add data model fields</span></span>](#FieldsEntry)
        - [<span data-ttu-id="00999-117">データ モデルの設計を完了する</span><span class="sxs-lookup"><span data-stu-id="00999-117">Complete the design of the data model</span></span>](#CompleteDataModel)

- [<span data-ttu-id="00999-118">構成データ モデルで使用するデータ モデルを設計する</span><span class="sxs-lookup"><span data-stu-id="00999-118">Design a model mapping for the configured data model</span></span>](#DesignMapping)

    - [<span data-ttu-id="00999-119">新しいモデル マッピングの構成をインポートする</span><span class="sxs-lookup"><span data-stu-id="00999-119">Import a new model mapping configuration</span></span>](#ImportModelMapping)
    - [<span data-ttu-id="00999-120">新しいモデル マッピングの構成を作成する</span><span class="sxs-lookup"><span data-stu-id="00999-120">Create a new model mapping configuration</span></span>](#CreateModelMapping)

        - [<span data-ttu-id="00999-121">新しいモデル マッピングのコンポーネントを設計する</span><span class="sxs-lookup"><span data-stu-id="00999-121">Design a new model mapping component</span></span>](#DesignMappingComponent)
        - [<span data-ttu-id="00999-122">データ ソースを追加してアプリケーション テーブルにアクセスする</span><span class="sxs-lookup"><span data-stu-id="00999-122">Add data sources to access application tables</span></span>](#AddMmDataSource1)
        - [<span data-ttu-id="00999-123">データ ソースを追加してアプリケーション リストにアクセスする</span><span class="sxs-lookup"><span data-stu-id="00999-123">Add data sources to access application enumerations</span></span>](#AddMmDataSource2)
        - [<span data-ttu-id="00999-124">ER ラベルを追加して指定した言語でレポートを生成する</span><span class="sxs-lookup"><span data-stu-id="00999-124">Add ER labels to generate a report in a specified language</span></span>](#AddMmLabels)
        - [<span data-ttu-id="00999-125">データ ソースを追加して、比較した列挙値の結果をテキスト値に変換する</span><span class="sxs-lookup"><span data-stu-id="00999-125">Add a data source to transform the results of comparing enumeration values to a text value</span></span>](#AddMmDataSource3)
        - [<span data-ttu-id="00999-126">データ ソースをデータ モデル フィールドにバインドする</span><span class="sxs-lookup"><span data-stu-id="00999-126">Bind data sources to data model fields</span></span>](#AddMmBindings1)
        - [<span data-ttu-id="00999-127">データ モデルのマッピングを完了する</span><span class="sxs-lookup"><span data-stu-id="00999-127">Complete the design of the model mapping</span></span>](#CompleteModelMapping)

- [<span data-ttu-id="00999-128">カスタム レポートで使用するテンプレートを設計する</span><span class="sxs-lookup"><span data-stu-id="00999-128">Design a template for a custom report</span></span>](#DesignReportTemplate)
- [<span data-ttu-id="00999-129">形式のデザイン</span><span class="sxs-lookup"><span data-stu-id="00999-129">Design a format</span></span>](#DesignFormat)

    - [<span data-ttu-id="00999-130">設計済みフォーマットの構成をインポートする</span><span class="sxs-lookup"><span data-stu-id="00999-130">Import a designed format configuration</span></span>](#FormatImport)
    - [<span data-ttu-id="00999-131">新しい構成の書式設定の作成</span><span class="sxs-lookup"><span data-stu-id="00999-131">Create a new format configuration</span></span>](#FormatCreate)

        - [<span data-ttu-id="00999-132">レポートのテンプレートをインポートする</span><span class="sxs-lookup"><span data-stu-id="00999-132">Import a report template</span></span>](#ImportReportTemplate)
        - [<span data-ttu-id="00999-133">フォーマットを構成する</span><span class="sxs-lookup"><span data-stu-id="00999-133">Configure a format</span></span>](#ConfigureFormat)
        - [<span data-ttu-id="00999-134">レポートのタイトルに使用するデータのバインドを定義する</span><span class="sxs-lookup"><span data-stu-id="00999-134">Define the data binding for a report title</span></span>](#DefineFormatBindings)
        - [<span data-ttu-id="00999-135">モデル データ ソースをレビューする</span><span class="sxs-lookup"><span data-stu-id="00999-135">Review the model data source</span></span>](#ReviewModelDataSource)
        - [<span data-ttu-id="00999-136">フォーマットの要素をデータ ソース フィールドにバインドする</span><span class="sxs-lookup"><span data-stu-id="00999-136">Bind format elements to data source fields</span></span>](#BindFormatElements)

    - [<span data-ttu-id="00999-137">ER から設計済みのフォーマットを実行する</span><span class="sxs-lookup"><span data-stu-id="00999-137">Run a designed format from ER</span></span>](#RunFormatFromER)

- [<span data-ttu-id="00999-138">設計済みのフォーマットを調整する</span><span class="sxs-lookup"><span data-stu-id="00999-138">Tune a designed format</span></span>](#TuneFormat)

    - [<span data-ttu-id="00999-139">フォーマットを修正して生成されたドキュメントの名前を変更する</span><span class="sxs-lookup"><span data-stu-id="00999-139">Modify a format to change the name of a generated document</span></span>](#ModifyToChangeName)
    - [<span data-ttu-id="00999-140">フォーマットを修正して質問の表示順を変更する</span><span class="sxs-lookup"><span data-stu-id="00999-140">Modify a format to change the order of questions</span></span>](#ModifyToOrder)
    - [<span data-ttu-id="00999-141">ER から修正済みのフォーマットを実行する</span><span class="sxs-lookup"><span data-stu-id="00999-141">Run a modified format from ER</span></span>](#RunFormatFromER2)
    - [<span data-ttu-id="00999-142">フォーマットの設計を完了する</span><span class="sxs-lookup"><span data-stu-id="00999-142">Complete the format design</span></span>](#CompleteFormat)

- [<span data-ttu-id="00999-143">アプリケーション アーティファクトを開発して、設計済みのレポートを呼び出す</span><span class="sxs-lookup"><span data-stu-id="00999-143">Develop application artefacts to call the designed report</span></span>](#DevelopCustomCode)

    - [<span data-ttu-id="00999-144">ソース コードの修正</span><span class="sxs-lookup"><span data-stu-id="00999-144">Modify source code</span></span>](#ModifySourceCode)

        - [<span data-ttu-id="00999-145">データ コントラクトのクラスを追加する</span><span class="sxs-lookup"><span data-stu-id="00999-145">Add a data contract class</span></span>](#DataContractClass)
        - [<span data-ttu-id="00999-146">UI Builder のクラスを追加する</span><span class="sxs-lookup"><span data-stu-id="00999-146">Add a UI builder class</span></span>](#UIBuilderClass)
        - [<span data-ttu-id="00999-147">データ プロバイダーのクラスを追加する</span><span class="sxs-lookup"><span data-stu-id="00999-147">Add a data provider class</span></span>](#DataProviderClass)
        - [<span data-ttu-id="00999-148">ラベル ファイルを追加する</span><span class="sxs-lookup"><span data-stu-id="00999-148">Add a labels file</span></span>](#LabelsFile)
        - [<span data-ttu-id="00999-149">レポート サービス クラスを追加する</span><span class="sxs-lookup"><span data-stu-id="00999-149">Add a report service class</span></span>](#ServiceClass)
        - [<span data-ttu-id="00999-150">レポートのコントローラ クラスを追加する</span><span class="sxs-lookup"><span data-stu-id="00999-150">Add a report controller class</span></span>](#ControllerClass)
        - [<span data-ttu-id="00999-151">メニュー項目を追加する</span><span class="sxs-lookup"><span data-stu-id="00999-151">Add a menu item</span></span>](#MenuItem)
        - [<span data-ttu-id="00999-152">メニュー項目をメニューに追加する</span><span class="sxs-lookup"><span data-stu-id="00999-152">Add a menu item to a menu</span></span>](#Menu)
        - [<span data-ttu-id="00999-153">Visual Studio プロジェクトをビルドする</span><span class="sxs-lookup"><span data-stu-id="00999-153">Build a Visual Studio project</span></span>](#BuildVSProject)

    - [<span data-ttu-id="00999-154">アプリケーションからフォーマットを実行する</span><span class="sxs-lookup"><span data-stu-id="00999-154">Run a format from the application</span></span>](#RunFormatFromApp)

- [<span data-ttu-id="00999-155">設計済みの ER ソリューションを調整する</span><span class="sxs-lookup"><span data-stu-id="00999-155">Tune a designed ER solution</span></span>](#TuneSolution)

    - [<span data-ttu-id="00999-156">モデルのマッピングを修正する</span><span class="sxs-lookup"><span data-stu-id="00999-156">Modify a model mapping</span></span>](#ModifyModelMapping)

        - [<span data-ttu-id="00999-157">データ ソースを追加してデータ コントラクト オブジェクトにアクセスする</span><span class="sxs-lookup"><span data-stu-id="00999-157">Add data sources to access a data contract object</span></span>](#AddDataSource1)
        - [<span data-ttu-id="00999-158">データ ソースを追加して ER フォーマット マッピング レコードにアクセスする</span><span class="sxs-lookup"><span data-stu-id="00999-158">Add a data source to access ER format mapping records</span></span>](#AddDataSource2)
        - [<span data-ttu-id="00999-159">データ ソースを追加して実行中の ER フォーマットのフォーマット マッピング レコードにアクセスする</span><span class="sxs-lookup"><span data-stu-id="00999-159">Add a data source to access a format mapping record of a running ER format</span></span>](#AddDataSource3)
        - [<span data-ttu-id="00999-160">データ モデル内の実行中の ER フォーマットの名前を入力する</span><span class="sxs-lookup"><span data-stu-id="00999-160">Enter the name of the running ER format in the data model</span></span>](#AddBinding)
        - [<span data-ttu-id="00999-161">データ モデルのマッピングを完了する</span><span class="sxs-lookup"><span data-stu-id="00999-161">Complete the design of the model mapping</span></span>](#CompleteModelMapping2)

    - [<span data-ttu-id="00999-162">フォーマットを変更する</span><span class="sxs-lookup"><span data-stu-id="00999-162">Modify a format</span></span>](#ModifyFormat)

        - [<span data-ttu-id="00999-163">新たなフォーマット要素を追加する</span><span class="sxs-lookup"><span data-stu-id="00999-163">Add a new format element</span></span>](#AddFormatElement)
        - [<span data-ttu-id="00999-164">追加されたフォーマット要素をバインドする</span><span class="sxs-lookup"><span data-stu-id="00999-164">Bind the added format element</span></span>](#BindAddedFormatElement)
        - [<span data-ttu-id="00999-165">フォーマットの設計を完了する</span><span class="sxs-lookup"><span data-stu-id="00999-165">Complete the format design</span></span>](#CompleteFormat2)

    - [<span data-ttu-id="00999-166">アプリケーションからフォーマットを実行する</span><span class="sxs-lookup"><span data-stu-id="00999-166">Run a format from the application</span></span>](#RunFormatFromApp2)
    - [<span data-ttu-id="00999-167">ER からフォーマットを実行する</span><span class="sxs-lookup"><span data-stu-id="00999-167">Run a format from ER</span></span>](#RunFormatFromER3)
    - [<span data-ttu-id="00999-168">オン スクリーン プレビューに使用するフォーマットの出力先を構成する</span><span class="sxs-lookup"><span data-stu-id="00999-168">Configure a format destination for on-screen preview</span></span>](#ConfigureDestination)
    - [<span data-ttu-id="00999-169">アプリケーションからフォーマットを実行して、PDF ドキュメントでプレビューする</span><span class="sxs-lookup"><span data-stu-id="00999-169">Run a format from the application to preview it as a PDF document</span></span>](#RunFormatFromApp3)

- [<span data-ttu-id="00999-170">追加リソース</span><span class="sxs-lookup"><span data-stu-id="00999-170">Additional resources</span></span>](#References)

<span data-ttu-id="00999-171">この例では、[アンケート](../../../human-resources/hr-learning-questionnaires.md)モジュールで使用する新しい ER ソリューションを作成します。</span><span class="sxs-lookup"><span data-stu-id="00999-171">In this example, you will create a new ER solution for the [Questionnaire](../../../human-resources/hr-learning-questionnaires.md) module.</span></span> <span data-ttu-id="00999-172">この新しい ER ソリューションを使用すると、Microsoft Excel ワークシートをテンプレートに使用してレポートを設計することができます。</span><span class="sxs-lookup"><span data-stu-id="00999-172">This new ER solution lets you design a report by using a Microsoft Excel worksheet as a template.</span></span> <span data-ttu-id="00999-173">**アンケート** レポートは、既存の SQL Server Reporting Services (SSRS) レポートに加えて、Excel 形式や PDF 形式で生成できます。</span><span class="sxs-lookup"><span data-stu-id="00999-173">You can then generate the **Questionnaire** report in Excel or PDF format, in addition to generating the existing SQL Server Reporting Services (SSRS) report.</span></span> <span data-ttu-id="00999-174">必要に応じて、この新規レポートを後で修正することも可能です。</span><span class="sxs-lookup"><span data-stu-id="00999-174">You can also modify the new report later, upon request.</span></span> <span data-ttu-id="00999-175">コーディングは必要ありません。</span><span class="sxs-lookup"><span data-stu-id="00999-175">No coding is required.</span></span>

1. <span data-ttu-id="00999-176">既存のレポートを実行するには、**アンケート** \> **設計** \> **アンケート レポート** に移動してください。</span><span class="sxs-lookup"><span data-stu-id="00999-176">To run the existing report, go to **Questionnaire** \> **Design** \> **Questionnaires report**.</span></span>

    ![アンケート モジュールでアンケート レポートのメニュー項目を選択し、既存の SSRS レポートを実行する](./media/er-quick-start1-application-menu-origin.png)

2. <span data-ttu-id="00999-178">**アンケート レポート** のダイアログ ボックスで、選択基準を指定します。</span><span class="sxs-lookup"><span data-stu-id="00999-178">In the **Questionnaires report** dialog box, specify selection criteria.</span></span> <span data-ttu-id="00999-179">フィルターを適用するとレポートに、アンケート **SBCCrsExam** のみを表示させることができます。</span><span class="sxs-lookup"><span data-stu-id="00999-179">Apply a filter so that the report includes only the **SBCCrsExam** questionnaire.</span></span>

    ![アンケート レポートのダイアログ ボックスで、選択基準を指定する](./media/er-quick-start1-ssrs-report-dialog.png)

<span data-ttu-id="00999-181">以下の図では、 アンケート **SBCCrsExam** で使用する SSRS レポートが生成されたバージョンを示しています。</span><span class="sxs-lookup"><span data-stu-id="00999-181">The following illustration shows the generated version of the SSRS report for the **SBCCrsExam** questionnaire.</span></span>

![生成済みの SSRS レポート](./media/er-quick-start1-ssrs-report.png)

## <a name="configure-the-er-framework"></a><a name="ConfigureFramework"></a> <span data-ttu-id="00999-183">ER フレームワークを構成</span><span class="sxs-lookup"><span data-stu-id="00999-183">Configure the ER framework</span></span>

<span data-ttu-id="00999-184">電子レポートの開発者ロールが付与されたユーザーは、ER フレームワークを使用して 新たな ER ソリューションを設計する前に、最小限の ER パラメータを構成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="00999-184">As a user in the Electronic Reporting Developer role, you must configure the minimal set of ER parameters before you can start to use the ER framework to design your new ER solution.</span></span>

### <a name="configure-er-parameters"></a><a name="ConfigureParameters"></a><span data-ttu-id="00999-185">ER パラメーターの構成</span><span class="sxs-lookup"><span data-stu-id="00999-185">Configure ER parameters</span></span>

1. <span data-ttu-id="00999-186">**組織管理** \> **ワークスペース** \> **電子申告** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="00999-186">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="00999-187">**電子申告** ワークスペースで、**電子申告パラメーター** を選択します。</span><span class="sxs-lookup"><span data-stu-id="00999-187">In the **Electronic reporting** workspace, select **Electronic reporting parameters**.</span></span>
3. <span data-ttu-id="00999-188">**電子申告パラメーター** ページの、**一般** タブで、**デザイン モードの有効化** オプションを **はい** に設定します。</span><span class="sxs-lookup"><span data-stu-id="00999-188">On the **Electronic reporting parameters** page, on the **General** tab, set the **Enable design mode** option to **Yes**.</span></span>
4. <span data-ttu-id="00999-189">**添付** タブで、次のパラメーターを設定します:</span><span class="sxs-lookup"><span data-stu-id="00999-189">On the **Attachments** tab, set the following parameters:</span></span>

    - <span data-ttu-id="00999-190">**USMF** 社で使用する **構成** フィールドを、**ファイル** に設定します。</span><span class="sxs-lookup"><span data-stu-id="00999-190">Set the **Configurations** field to **File** for the **USMF** company.</span></span>
    - <span data-ttu-id="00999-191">**ジョブ アーカイブ**、**テンポラリー**、 **ベースライン**、**その他** の各フィールドを **ファイル** に設定します。</span><span class="sxs-lookup"><span data-stu-id="00999-191">Set **Job archive**, **Temporary**, **Baseline**, and **Others** fields to **File**.</span></span>

<span data-ttu-id="00999-192">ER パラメーターについては、[ER フレームワークの構成](electronic-reporting-er-configure-parameters.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="00999-192">For more information about ER parameters, see [Configure the ER framework](electronic-reporting-er-configure-parameters.md).</span></span>

### <a name="activate-an-er-configuration-provider"></a><a name="ActivateProvider"></a> <span data-ttu-id="00999-193">ER 構成 プロバイダーをアクティブにする</span><span class="sxs-lookup"><span data-stu-id="00999-193">Activate an ER configuration provider</span></span>

<span data-ttu-id="00999-194">各ER の構成は、構成プロバイダーに所有権があるものとして表示されます。</span><span class="sxs-lookup"><span data-stu-id="00999-194">Every ER configuration is marked as owned by an ER configuration provider.</span></span> <span data-ttu-id="00999-195">そのため、ER 構成を追加、または編集する前に、**電子レポート** ワークスペースで ER 構成プロバイダーを有効化する必要があります。</span><span class="sxs-lookup"><span data-stu-id="00999-195">Therefore, you must activate an ER configuration provider in the **Electronic reporting** workspace before you start to add or edit any ER configurations.</span></span>

> [!NOTE]
> <span data-ttu-id="00999-196">ER 構成の所有者のみが編集できます。</span><span class="sxs-lookup"><span data-stu-id="00999-196">Only the owner of an ER configuration can edit it.</span></span> <span data-ttu-id="00999-197">したがって、ER 構成を編集する前に、適切な ER 構成 プロバイダーは **電子申告** ワークスペースで有効化する必要があります。</span><span class="sxs-lookup"><span data-stu-id="00999-197">Therefore, before an ER configuration can be edited, the appropriate ER configuration provider must be activated in the **Electronic reporting** workspace.</span></span>

#### <a name="review-the-list-of-er-configuration-providers"></a><a name="ReviewProvidersList"></a> <span data-ttu-id="00999-198">ER 構成 プロバイダーの一覧をレビュー</span><span class="sxs-lookup"><span data-stu-id="00999-198">Review the list of ER configuration providers</span></span>

1. <span data-ttu-id="00999-199">**組織管理** \> **ワークスペース** \> **電子申告** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="00999-199">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="00999-200">**電子レポート** ワークスペースの、**関連するリンク** セクションで、**構成プロバイダー** を選択します。</span><span class="sxs-lookup"><span data-stu-id="00999-200">In the **Electronic reporting** workspace, in the **Related links** section, select **Configuration providers**.</span></span>
3. <span data-ttu-id="00999-201">**構成プロバイダー** ページで、各構成プロバイダー レコードは一意の名称と URL を持っています。</span><span class="sxs-lookup"><span data-stu-id="00999-201">On the **Configuration providers** page, each configuration provider record has a unique name and URL.</span></span> <span data-ttu-id="00999-202">このページの内容をレビューします。</span><span class="sxs-lookup"><span data-stu-id="00999-202">Review the contents of this page.</span></span> <span data-ttu-id="00999-203">**Litware, Inc.** (`https://www.litware.com`) のレコードが既に存在する場合は、次の手順をスキップし、[新しい ER 構成 プロバイダーを追加](#ActivateProvider) します。</span><span class="sxs-lookup"><span data-stu-id="00999-203">If a record for **Litware, Inc.** (`https://www.litware.com`) already exists, skip the next procedure, [Add a new ER configuration provider](#ActivateProvider).</span></span>

#### <a name="add-a-new-er-configuration-provider"></a><a name="AddProvider"></a> <span data-ttu-id="00999-204">新しい ER 構成 プロバイダーを追加</span><span class="sxs-lookup"><span data-stu-id="00999-204">Add a new ER configuration provider</span></span>

1. <span data-ttu-id="00999-205">**構成 プロバイダー** ページで、**新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="00999-205">On the **Configuration providers** page, select **New**.</span></span>
2. <span data-ttu-id="00999-206">**名前** フィールドに、**Litware, Inc.** と入力</span><span class="sxs-lookup"><span data-stu-id="00999-206">In the **Name** field, enter **Litware, Inc.**</span></span>
3. <span data-ttu-id="00999-207">**インターネット アドレス** フィールドで、`https://www.litware.com` を入力します。</span><span class="sxs-lookup"><span data-stu-id="00999-207">In the **Internet address** field, enter `https://www.litware.com`.</span></span>
4. <span data-ttu-id="00999-208">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="00999-208">Select **Save**.</span></span>

#### <a name="activate-an-er-configuration-provider"></a><a name="ActivateAddedProvider"></a> <span data-ttu-id="00999-209">ER 構成 プロバイダーをアクティブにする</span><span class="sxs-lookup"><span data-stu-id="00999-209">Activate an ER configuration provider</span></span>

1. <span data-ttu-id="00999-210">**組織管理** \> **ワークスペース** \> **電子申告** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="00999-210">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="00999-211">**電子レポート** ワークスペースの、構成プロバイダーに **Litware, Inc.** を選択します。</span><span class="sxs-lookup"><span data-stu-id="00999-211">In the **Electronic reporting** workspace, select the **Litware, Inc.** configuration provider.</span></span>
3. <span data-ttu-id="00999-212">**有効に設定** を選択します。</span><span class="sxs-lookup"><span data-stu-id="00999-212">Select **Set active**.</span></span>

<span data-ttu-id="00999-213">ER 構成 プロバイダーについては、[構成 プロバイダーを作成し有効としてマークする](tasks/er-configuration-provider-mark-it-active-2016-11.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="00999-213">For more information about ER configuration providers, see [Create configuration providers and mark them as active](tasks/er-configuration-provider-mark-it-active-2016-11.md).</span></span>

## <a name="design-a-domain-specific-data-model"></a><a name="DesignModel"></a><span data-ttu-id="00999-214">ドメイン固有のデータ モデルを設計する</span><span class="sxs-lookup"><span data-stu-id="00999-214">Design a domain-specific data model</span></span>

<span data-ttu-id="00999-215">**アンケート** ビジネス ドメインで使用する [データ モデル](general-electronic-reporting.md#data-model-and-model-mapping-components) コンポーネントを含む、新たな ER 構成を作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="00999-215">You must create a new ER configuration that contains a [data model](general-electronic-reporting.md#data-model-and-model-mapping-components) component for the **Questionnaire** business domain.</span></span> <span data-ttu-id="00999-216">このデータ モデルは後で、ER フォーマットを設計して **アンケート** レポートを作成する際に、データ ソースとして使用されます。</span><span class="sxs-lookup"><span data-stu-id="00999-216">This data model will later be used as a data source when you design an ER format to generate the **Questionnaire** report.</span></span>

<span data-ttu-id="00999-217">[新しいデータ モデル構成をインポートする](#ImportDataModel) セクションに記載されている手順を完了すると、提供された XML ファイルから必要なデータ モデルをインポートすることができます。</span><span class="sxs-lookup"><span data-stu-id="00999-217">By completing the steps in the [Import a new data model configuration](#ImportDataModel) section, you can import the required data model from the provided XML file.</span></span> <span data-ttu-id="00999-218">あるいは、[新しいデータ モデルの構成を作成する](#DesignDataModel) セクションに記載されている手順を完了すると、ゼロからこのデータ モデルを設計することができます。</span><span class="sxs-lookup"><span data-stu-id="00999-218">Alternatively, you can complete the steps in the [Create a new data model configuration](#DesignDataModel) section to design this data model from scratch.</span></span>

### <a name="import-a-new-data-model-configuration"></a><a name="ImportDataModel"></a><span data-ttu-id="00999-219">新しいデータ モデルのインポート</span><span class="sxs-lookup"><span data-stu-id="00999-219">Import a new data model configuration</span></span>

1. <span data-ttu-id="00999-220">[Questionnaires model.version.1.xml](https://go.microsoft.com/fwlink/?linkid=851448) ファイルをダウンロードし、ご利用のコンピューターに保存してください。</span><span class="sxs-lookup"><span data-stu-id="00999-220">Download the [Questionnaires model.version.1.xml](https://go.microsoft.com/fwlink/?linkid=851448) file, and save it to your local computer.</span></span>
2. <span data-ttu-id="00999-221">**組織管理** \> **ワークスペース** \> **電子申告** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="00999-221">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
3. <span data-ttu-id="00999-222">**電子レポート** ワークスペースで、**レポートの構成** を選択します。</span><span class="sxs-lookup"><span data-stu-id="00999-222">In the **Electronic reporting** workspace, select **Reporting configurations**.</span></span>
4. <span data-ttu-id="00999-223">操作ウィンドウで、**交換** \> **XML ファイルからロード** を選択します。</span><span class="sxs-lookup"><span data-stu-id="00999-223">On the Action Pane, select **Exchange** \> **Load from XML file**.</span></span>
5. <span data-ttu-id="00999-224">**参照** を選択し、**Questionnaires model.version.1.xml** ファイルを検索して、選択します。</span><span class="sxs-lookup"><span data-stu-id="00999-224">Select **Browse**, and then find and select the **Questionnaires model.version.1.xml** file.</span></span>
6. <span data-ttu-id="00999-225">**OK** を選択し、構成をインポートします。</span><span class="sxs-lookup"><span data-stu-id="00999-225">Select **OK** to import the configuration.</span></span>

<span data-ttu-id="00999-226">続けるには、次の手順をスキップしてください : [新しいデータ モデルの構成を作成する](#DesignDataModel)。</span><span class="sxs-lookup"><span data-stu-id="00999-226">To continue, skip the next procedure, [Create a new data model configuration](#DesignDataModel).</span></span>

### <a name="create-a-new-data-model-configuration"></a><a name="DesignDataModel"></a><span data-ttu-id="00999-227">新しいデータ モデル 構成の作成</span><span class="sxs-lookup"><span data-stu-id="00999-227">Create a new data model configuration</span></span>

1. <span data-ttu-id="00999-228">**組織管理** \> **ワークスペース** \> **電子申告** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="00999-228">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="00999-229">**電子レポート** ワークスペースで、**レポートの構成** を選択します。</span><span class="sxs-lookup"><span data-stu-id="00999-229">In the **Electronic reporting** workspace, select **Reporting configurations**.</span></span>
3. <span data-ttu-id="00999-230">**構成の作成** を選択します。</span><span class="sxs-lookup"><span data-stu-id="00999-230">Select **Create configuration**.</span></span>
4. <span data-ttu-id="00999-231">ドロップダウン ダイアログ ボックスの、**名前** フィールドで、**アンケート モデル** を入力してください。</span><span class="sxs-lookup"><span data-stu-id="00999-231">In the drop-down dialog box, in the **Name** field, enter **Questionnaire model**.</span></span>
5. <span data-ttu-id="00999-232">**構成を作成する** を選択して、構成を作成します。</span><span class="sxs-lookup"><span data-stu-id="00999-232">Select **Create configuration** to create the configuration.</span></span>

#### <a name="name-the-data-model"></a><a name="NameDataModel"></a><span data-ttu-id="00999-233">データ モデルに名前をつける</span><span class="sxs-lookup"><span data-stu-id="00999-233">Name the data model</span></span>

1. <span data-ttu-id="00999-234">**構成** ページの、構成ツリーで、**アンケート モデル** を選択します。</span><span class="sxs-lookup"><span data-stu-id="00999-234">On the **Configurations** page, in the configuration tree, select **Questionnaire model**.</span></span>
2. <span data-ttu-id="00999-235">**デザイナー** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="00999-235">Select **Designer**.</span></span>
3. <span data-ttu-id="00999-236">**データ モデル デザイナー** ページの、**全般** クイックタブ内の、 **名前** フィールドに <a name="DataModeName"></a>**アンケート** と入力します。</span><span class="sxs-lookup"><span data-stu-id="00999-236">On the **Data model designer** page, on the **General** FastTab, in the **Name** field, enter <a name="DataModeName"></a>**Questionnaires**.</span></span>

#### <a name="add-new-data-model-fields"></a><a name="FieldsEntry"></a><span data-ttu-id="00999-237">新しいデータ モデル フィールドを追加する</span><span class="sxs-lookup"><span data-stu-id="00999-237">Add new data model fields</span></span>

1. <span data-ttu-id="00999-238">**データ モデル デザイナー** ページで、**新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="00999-238">On the **Data model designer** page, select **New**.</span></span>
2. <span data-ttu-id="00999-239">データ モデル ノードを追加するドロップダウン ダイアログ ボックスで、以下の手順を実行してください :</span><span class="sxs-lookup"><span data-stu-id="00999-239">In the drop-down dialog box for adding a data model node, follow these steps:</span></span>

    1. <span data-ttu-id="00999-240">新しいノードの種類に、**モデル ルート** を選択します。</span><span class="sxs-lookup"><span data-stu-id="00999-240">Select **Model root** as the type of the new node.</span></span>
    2. <span data-ttu-id="00999-241">**名前** フィールドに、<a name="RootDefinitionName"></a>**ルート** と入力します。</span><span class="sxs-lookup"><span data-stu-id="00999-241">In the **Name** field, enter <a name="RootDefinitionName"></a>**Root**.</span></span>
    3. <span data-ttu-id="00999-242">**追加** を選択して新しいノードを追加します。</span><span class="sxs-lookup"><span data-stu-id="00999-242">Select **Add** to add the new node.</span></span>

    <span data-ttu-id="00999-243">このルートの記述子は、**アンケート** レポートにデータを提供する目的で使用されます。</span><span class="sxs-lookup"><span data-stu-id="00999-243">This root descriptor will be used to provide data for the **Questionnaire** report.</span></span> <span data-ttu-id="00999-244">1つのデータモデルには複数の記述子を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="00999-244">A single data model can have multiple descriptors.</span></span> <span data-ttu-id="00999-245">それぞれの記述子は、1つの ER フォーマットに対して指定することができ、レポートの生成に必要なデータを識別することができます。</span><span class="sxs-lookup"><span data-stu-id="00999-245">Each descriptor can be specified for a single ER format, to identify data that is required to generate the report.</span></span>

3. <span data-ttu-id="00999-246">再度 **新規** を選択し、データ モデル ノードを追加するドロップダウン ダイアログ ボックスで、次の手順を実行します :</span><span class="sxs-lookup"><span data-stu-id="00999-246">Select **New** again, and then, in the drop-down dialog box for adding a data model node, follow these steps:</span></span>

    1. <span data-ttu-id="00999-247">新規ノードのタイプに、**アクティブなノードの子ノード** を選択します。</span><span class="sxs-lookup"><span data-stu-id="00999-247">Select **Child of an active node** as the type of the new node.</span></span>
    2. <span data-ttu-id="00999-248">**名前** フィールドに、**CompanyName** と入力します。</span><span class="sxs-lookup"><span data-stu-id="00999-248">In the **Name** field, enter **CompanyName**.</span></span>
    3. <span data-ttu-id="00999-249">**品目タイプ** フィールドで、**文字列** を選択します。</span><span class="sxs-lookup"><span data-stu-id="00999-249">In the **Item type** field, select **String**.</span></span>
    4. <span data-ttu-id="00999-250">**追加** を選択して、新しいフィールドを追加します。</span><span class="sxs-lookup"><span data-stu-id="00999-250">Select **Add** to add the new field.</span></span>

    <span data-ttu-id="00999-251">このフィールドは、このデータ モデルをデータ ソースとして使用する ER レポートに現在の会社名を渡すために必要となります。</span><span class="sxs-lookup"><span data-stu-id="00999-251">This field is required to pass the name of the current company to an ER report that consumes this data model as a data source.</span></span>

4. <span data-ttu-id="00999-252">再度 **新規** を選択し、データ モデル ノードを追加するドロップダウン ダイアログ ボックスで、次の手順を実行します :</span><span class="sxs-lookup"><span data-stu-id="00999-252">Select **New** again, and then, in the drop-down dialog box for adding a data model node, follow these steps:</span></span>

    1. <span data-ttu-id="00999-253">新規ノードのタイプに、**アクティブなノードの子ノード** を選択します。</span><span class="sxs-lookup"><span data-stu-id="00999-253">Select **Child of an active node** as the type of the new node.</span></span>
    2. <span data-ttu-id="00999-254">**名前** フィールドに、**アンケート** と入力します。</span><span class="sxs-lookup"><span data-stu-id="00999-254">In the **Name** field, enter **Questionnaire**.</span></span>
    3. <span data-ttu-id="00999-255">**品目タイプ** フィールドで、**レコード リスト** を選択します。</span><span class="sxs-lookup"><span data-stu-id="00999-255">In the **Item type** field, select **Record list**.</span></span>
    4. <span data-ttu-id="00999-256">**追加** を選択して、新しいフィールドを追加します。</span><span class="sxs-lookup"><span data-stu-id="00999-256">Select **Add** to add the new field.</span></span>

    <span data-ttu-id="00999-257">このフィールドは、このデータ モデルをデータソースとして使用する ER レポートにアンケートのリストを渡すために使用されます。</span><span class="sxs-lookup"><span data-stu-id="00999-257">This field will be used to pass the list of questionnaires to an ER report that consumes this data model as a data source.</span></span>

5. <span data-ttu-id="00999-258">**アンケート** ノードを選択します。</span><span class="sxs-lookup"><span data-stu-id="00999-258">Select the **Questionnaire** node.</span></span>
6. <span data-ttu-id="00999-259">以下のデータ モデル構造が完成するまで、編集可能なデータ モデルの必須フィールドを同じ方法で追加していきます。</span><span class="sxs-lookup"><span data-stu-id="00999-259">Continue to add the required fields of the editable data model in the same manner until you complete the following data model structure.</span></span>

    | <span data-ttu-id="00999-260">フィールド パス</span><span class="sxs-lookup"><span data-stu-id="00999-260">Field path</span></span>                                                    | <span data-ttu-id="00999-261">データ型</span><span class="sxs-lookup"><span data-stu-id="00999-261">Data type</span></span>   | <span data-ttu-id="00999-262">フィールドの指定/戻り値</span><span class="sxs-lookup"><span data-stu-id="00999-262">Field designation/returned value</span></span> |
    |---------------------------------------------------------------|-------------|----------------------------------|
    | <span data-ttu-id="00999-263">ルート</span><span class="sxs-lookup"><span data-stu-id="00999-263">Root</span></span>                                                          |             | <span data-ttu-id="00999-264">アンケート データを依頼する際に基準となるポイントです。</span><span class="sxs-lookup"><span data-stu-id="00999-264">The reference point to request questionnaire data.</span></span> |
    | <span data-ttu-id="00999-265">Root\\CompanyName</span><span class="sxs-lookup"><span data-stu-id="00999-265">Root\\CompanyName</span></span>                                             | <span data-ttu-id="00999-266">文字列</span><span class="sxs-lookup"><span data-stu-id="00999-266">String</span></span>      | <span data-ttu-id="00999-267">現在の会社の名前です。</span><span class="sxs-lookup"><span data-stu-id="00999-267">The name of the current company.</span></span> |
    | <span data-ttu-id="00999-268">Root\\ExecutionContext</span><span class="sxs-lookup"><span data-stu-id="00999-268">Root\\ExecutionContext</span></span>                                        | <span data-ttu-id="00999-269">レコード</span><span class="sxs-lookup"><span data-stu-id="00999-269">Record</span></span>      | <span data-ttu-id="00999-270">フォーマット実行の詳細です。</span><span class="sxs-lookup"><span data-stu-id="00999-270">Format execution details.</span></span> |
    | <span data-ttu-id="00999-271">Root\\ExecutionContext\\FormatName</span><span class="sxs-lookup"><span data-stu-id="00999-271">Root\\ExecutionContext\\FormatName</span></span>                            | <span data-ttu-id="00999-272">文字列</span><span class="sxs-lookup"><span data-stu-id="00999-272">String</span></span>      | <span data-ttu-id="00999-273">実行中の ER フォーマットの名前です。</span><span class="sxs-lookup"><span data-stu-id="00999-273">The name of the ER format that is being run.</span></span> |
    | <span data-ttu-id="00999-274">Root\\Questionnaire</span><span class="sxs-lookup"><span data-stu-id="00999-274">Root\\Questionnaire</span></span>                                           | <span data-ttu-id="00999-275">レコード リスト</span><span class="sxs-lookup"><span data-stu-id="00999-275">Record list</span></span> | <span data-ttu-id="00999-276">アンケートの一覧です</span><span class="sxs-lookup"><span data-stu-id="00999-276">The list of questionnaires</span></span> |
    | <span data-ttu-id="00999-277">Root\\Questionnaire\\Active</span><span class="sxs-lookup"><span data-stu-id="00999-277">Root\\Questionnaire\\Active</span></span>                                   | <span data-ttu-id="00999-278">文字列</span><span class="sxs-lookup"><span data-stu-id="00999-278">String</span></span>      | <span data-ttu-id="00999-279">現在のアンケートの状態です。</span><span class="sxs-lookup"><span data-stu-id="00999-279">The status of the current questionnaire.</span></span> |
    | <span data-ttu-id="00999-280">Root\\Questionnaire\\Code</span><span class="sxs-lookup"><span data-stu-id="00999-280">Root\\Questionnaire\\Code</span></span>                                     | <span data-ttu-id="00999-281">文字列</span><span class="sxs-lookup"><span data-stu-id="00999-281">String</span></span>      | <span data-ttu-id="00999-282">現在のアンケートのコードです。</span><span class="sxs-lookup"><span data-stu-id="00999-282">The code of the current questionnaire.</span></span> |
    | <span data-ttu-id="00999-283">Root\\Questionnaire\\Description</span><span class="sxs-lookup"><span data-stu-id="00999-283">Root\\Questionnaire\\Description</span></span>                              | <span data-ttu-id="00999-284">文字列</span><span class="sxs-lookup"><span data-stu-id="00999-284">String</span></span>      | <span data-ttu-id="00999-285">現在のアンケートの説明です。</span><span class="sxs-lookup"><span data-stu-id="00999-285">The description of the current questionnaire.</span></span> |
    | <span data-ttu-id="00999-286">Root\\Questionnaire\\QuestionnaireType</span><span class="sxs-lookup"><span data-stu-id="00999-286">Root\\Questionnaire\\QuestionnaireType</span></span>                        | <span data-ttu-id="00999-287">文字列</span><span class="sxs-lookup"><span data-stu-id="00999-287">String</span></span>      | <span data-ttu-id="00999-288">現在のアンケートのタイプです。</span><span class="sxs-lookup"><span data-stu-id="00999-288">The type of the current questionnaire.</span></span> |
    | <span data-ttu-id="00999-289">Root\\Questionnaire\\QuestionOrder</span><span class="sxs-lookup"><span data-stu-id="00999-289">Root\\Questionnaire\\QuestionOrder</span></span>                            | <span data-ttu-id="00999-290">文字列</span><span class="sxs-lookup"><span data-stu-id="00999-290">String</span></span>      | <span data-ttu-id="00999-291">現在のアンケートの番号順です。</span><span class="sxs-lookup"><span data-stu-id="00999-291">The numerical order of the current questionnaire.</span></span> |
    | <span data-ttu-id="00999-292">Root\\Questionnaire\\ResultsGroup</span><span class="sxs-lookup"><span data-stu-id="00999-292">Root\\Questionnaire\\ResultsGroup</span></span>                             | <span data-ttu-id="00999-293">レコード</span><span class="sxs-lookup"><span data-stu-id="00999-293">Record</span></span>      | <span data-ttu-id="00999-294">現在のアンケートの結果パラメーターです。</span><span class="sxs-lookup"><span data-stu-id="00999-294">The result parameters of the current questionnaire.</span></span> |
    | <span data-ttu-id="00999-295">Root\\Questionnaire\\ResultsGroup\\Code</span><span class="sxs-lookup"><span data-stu-id="00999-295">Root\\Questionnaire\\ResultsGroup\\Code</span></span>                       | <span data-ttu-id="00999-296">文字列</span><span class="sxs-lookup"><span data-stu-id="00999-296">String</span></span>      | <span data-ttu-id="00999-297">現在の結果グループの ID コードです。</span><span class="sxs-lookup"><span data-stu-id="00999-297">The identification code of the current result group.</span></span> |
    | <span data-ttu-id="00999-298">Root\\Questionnaire\\ResultsGroup\\Description</span><span class="sxs-lookup"><span data-stu-id="00999-298">Root\\Questionnaire\\ResultsGroup\\Description</span></span>                | <span data-ttu-id="00999-299">文字列</span><span class="sxs-lookup"><span data-stu-id="00999-299">String</span></span>      | <span data-ttu-id="00999-300">現在の結果グループの説明です。</span><span class="sxs-lookup"><span data-stu-id="00999-300">The description of the current result group.</span></span> |
    | <span data-ttu-id="00999-301">Root\\Questionnaire\\ResultsGroup\\MaxNumberOfPoints</span><span class="sxs-lookup"><span data-stu-id="00999-301">Root\\Questionnaire\\ResultsGroup\\MaxNumberOfPoints</span></span>          | <span data-ttu-id="00999-302">実績</span><span class="sxs-lookup"><span data-stu-id="00999-302">Real</span></span>        | <span data-ttu-id="00999-303">獲得できる最大ポイント数です。</span><span class="sxs-lookup"><span data-stu-id="00999-303">The maximum number of points that could be earned.</span></span> |
    | <span data-ttu-id="00999-304">Root\\Questionnaire\\Question</span><span class="sxs-lookup"><span data-stu-id="00999-304">Root\\Questionnaire\\Question</span></span>                                 | <span data-ttu-id="00999-305">レコード リスト</span><span class="sxs-lookup"><span data-stu-id="00999-305">Record list</span></span> | <span data-ttu-id="00999-306">現在のアンケートの質問の一覧です。</span><span class="sxs-lookup"><span data-stu-id="00999-306">The list of questions for the current questionnaire.</span></span> |
    | <span data-ttu-id="00999-307">Root\\Questionnaire\\Question\\CollectionSequenceNumber</span><span class="sxs-lookup"><span data-stu-id="00999-307">Root\\Questionnaire\\Question\\CollectionSequenceNumber</span></span>       | <span data-ttu-id="00999-308">整数</span><span class="sxs-lookup"><span data-stu-id="00999-308">Integer</span></span>     | <span data-ttu-id="00999-309">現在の応答コレクションのシーケンス番号です。</span><span class="sxs-lookup"><span data-stu-id="00999-309">The sequence number of the current answer collection.</span></span> |
    | <span data-ttu-id="00999-310">Root\\Questionnaire\\Question\\Id</span><span class="sxs-lookup"><span data-stu-id="00999-310">Root\\Questionnaire\\Question\\Id</span></span>                             | <span data-ttu-id="00999-311">文字列</span><span class="sxs-lookup"><span data-stu-id="00999-311">String</span></span>      | <span data-ttu-id="00999-312">現在の質問の ID コードです。</span><span class="sxs-lookup"><span data-stu-id="00999-312">The identification code of the current question.</span></span> |
    | <span data-ttu-id="00999-313">Root\\Questionnaire\\Question\\MustBeCompleted</span><span class="sxs-lookup"><span data-stu-id="00999-313">Root\\Questionnaire\\Question\\MustBeCompleted</span></span>                | <span data-ttu-id="00999-314">文字列</span><span class="sxs-lookup"><span data-stu-id="00999-314">String</span></span>      | <span data-ttu-id="00999-315">現在の質問が必須であるかどうかを示すフラグです。</span><span class="sxs-lookup"><span data-stu-id="00999-315">A flag that indicates whether the current question must be answered.</span></span> |
    | <span data-ttu-id="00999-316">Root\\Questionnaire\\Question\\PrimaryQuestion</span><span class="sxs-lookup"><span data-stu-id="00999-316">Root\\Questionnaire\\Question\\PrimaryQuestion</span></span>                | <span data-ttu-id="00999-317">文字列</span><span class="sxs-lookup"><span data-stu-id="00999-317">String</span></span>      | <span data-ttu-id="00999-318">現在の質問が主要なものであるかどうかを示すフラグです。</span><span class="sxs-lookup"><span data-stu-id="00999-318">A flag that indicates whether the current question is primary.</span></span> |
    | <span data-ttu-id="00999-319">Root\\Questionnaire\\Question\\SequenceNumber</span><span class="sxs-lookup"><span data-stu-id="00999-319">Root\\Questionnaire\\Question\\SequenceNumber</span></span>                 | <span data-ttu-id="00999-320">整数</span><span class="sxs-lookup"><span data-stu-id="00999-320">Integer</span></span>     | <span data-ttu-id="00999-321">現在の質問のシーケンス番号です。</span><span class="sxs-lookup"><span data-stu-id="00999-321">The sequence number of the current question.</span></span> |
    | <span data-ttu-id="00999-322">Root\\Questionnaire\\Question\\Text</span><span class="sxs-lookup"><span data-stu-id="00999-322">Root\\Questionnaire\\Question\\Text</span></span>                           | <span data-ttu-id="00999-323">文字列</span><span class="sxs-lookup"><span data-stu-id="00999-323">String</span></span>      | <span data-ttu-id="00999-324">現在の質問のテキストです。</span><span class="sxs-lookup"><span data-stu-id="00999-324">The text of the current question.</span></span> |
    | <span data-ttu-id="00999-325">Root\\Questionnaire\\Question\\Answer</span><span class="sxs-lookup"><span data-stu-id="00999-325">Root\\Questionnaire\\Question\\Answer</span></span>                         | <span data-ttu-id="00999-326">レコード リスト</span><span class="sxs-lookup"><span data-stu-id="00999-326">Record list</span></span> | <span data-ttu-id="00999-327">現在の質問の回答の一覧です。</span><span class="sxs-lookup"><span data-stu-id="00999-327">The list of answers for the current question.</span></span> |
    | <span data-ttu-id="00999-328">Root\\Questionnaire\\Question\\Answer\\CorrectAnswer</span><span class="sxs-lookup"><span data-stu-id="00999-328">Root\\Questionnaire\\Question\\Answer\\CorrectAnswer</span></span>          | <span data-ttu-id="00999-329">文字列</span><span class="sxs-lookup"><span data-stu-id="00999-329">String</span></span>      | <span data-ttu-id="00999-330">現在の回答が正しいものであるかどうかを示すフラグです。</span><span class="sxs-lookup"><span data-stu-id="00999-330">A flag that indicates whether the current answer is correct.</span></span> |
    | <span data-ttu-id="00999-331">Root\\Questionnaire\\Question\\Answer\\Points</span><span class="sxs-lookup"><span data-stu-id="00999-331">Root\\Questionnaire\\Question\\Answer\\Points</span></span>                 | <span data-ttu-id="00999-332">実績</span><span class="sxs-lookup"><span data-stu-id="00999-332">Real</span></span>        | <span data-ttu-id="00999-333">現在の回答が選択されたときに確定するポイントです。</span><span class="sxs-lookup"><span data-stu-id="00999-333">The points that are earned when the current answer is selected.</span></span> |
    | <span data-ttu-id="00999-334">Root\\Questionnaire\\Question\\Answer\\SequenceNumber</span><span class="sxs-lookup"><span data-stu-id="00999-334">Root\\Questionnaire\\Question\\Answer\\SequenceNumber</span></span>         | <span data-ttu-id="00999-335">整数</span><span class="sxs-lookup"><span data-stu-id="00999-335">Integer</span></span>     | <span data-ttu-id="00999-336">現在の回答のシーケンス番号です。</span><span class="sxs-lookup"><span data-stu-id="00999-336">The sequence number of the current answer.</span></span> |
    | <span data-ttu-id="00999-337">Root\\Questionnaire\\Question\\Answer\\Text</span><span class="sxs-lookup"><span data-stu-id="00999-337">Root\\Questionnaire\\Question\\Answer\\Text</span></span>                   | <span data-ttu-id="00999-338">文字列</span><span class="sxs-lookup"><span data-stu-id="00999-338">String</span></span>      | <span data-ttu-id="00999-339">現在の回答のテキストです。</span><span class="sxs-lookup"><span data-stu-id="00999-339">The text of the current answer.</span></span> |

    <span data-ttu-id="00999-340">以下の図は、**データ モデル デザイナー** ページ上の完成した編集可能なデータ モデルを示して います。</span><span class="sxs-lookup"><span data-stu-id="00999-340">The following illustration shows the completed editable data model on the **Data model designer** page.</span></span>

    ![ER データ モデル デザイナーで構成されたデータ モデル](./media/er-quick-start1-model2.png)

7. <span data-ttu-id="00999-342">変更を保存します。</span><span class="sxs-lookup"><span data-stu-id="00999-342">Save your changes.</span></span>
8. <span data-ttu-id="00999-343">**データ モデル デザイナー** ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="00999-343">Close the **Data model designer** page.</span></span>

#### <a name="complete-the-design-of-the-data-model"></a><a name="CompleteDataModel"></a><span data-ttu-id="00999-344">データモデルのデザインを完成させる</span><span class="sxs-lookup"><span data-stu-id="00999-344">Complete the design of the data model</span></span>

1. <span data-ttu-id="00999-345">**組織管理** \> **電子申告** \> **構成** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="00999-345">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="00999-346">**構成** ページの、構成ツリーで、**アンケート モデル** を選択します。</span><span class="sxs-lookup"><span data-stu-id="00999-346">On the **Configurations** page, in the configuration tree, select **Questionnaire model**.</span></span>
3. <span data-ttu-id="00999-347">**バージョン** クイック タブで、状態が **下書き** となっている構成のバージョンを選択します。</span><span class="sxs-lookup"><span data-stu-id="00999-347">On the **Versions** FastTab, select the configuration version that has a status of **Draft**.</span></span>
4. <span data-ttu-id="00999-348">**ステータスの変更** \> **完了** を選択します。</span><span class="sxs-lookup"><span data-stu-id="00999-348">Select **Change status** \> **Complete**.</span></span>

<span data-ttu-id="00999-349">この構成のバージョン 1 の状態 **下書き** から **完了** に変更されます。</span><span class="sxs-lookup"><span data-stu-id="00999-349">The status of version 1 of this configuration is changed from **Draft** to **Completed**.</span></span> <span data-ttu-id="00999-350">バージョン 1 を変更することはできなくなります。</span><span class="sxs-lookup"><span data-stu-id="00999-350">Version 1 can no longer be changed.</span></span> <span data-ttu-id="00999-351">このバージョンには、構成済みのデータ モデルが含まれており、その他の ER の構成の基礎として使用できます。</span><span class="sxs-lookup"><span data-stu-id="00999-351">This version contains the configured data model and can be used as the basis for other ER configurations.</span></span> <span data-ttu-id="00999-352">この構成のバージョン2が作成され、状態が **下書き** になります。</span><span class="sxs-lookup"><span data-stu-id="00999-352">Version 2 of this configuration is created and has a status of **Draft**.</span></span> <span data-ttu-id="00999-353">このバージョンを編集して、**アンケート** データ モデルを調整することができます。</span><span class="sxs-lookup"><span data-stu-id="00999-353">You can edit this version to adjust the **Questionnaire** data model.</span></span>

![[構成] ページの編集可能な ER 構成のバージョン](./media/er-quick-start1-model-configuration.png)

<span data-ttu-id="00999-355">ER の構成に関する詳細情報については、 [電子レポート (ER) の概要](general-electronic-reporting.md#component-versioning) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="00999-355">For more information about versioning for ER configurations, see [Electronic reporting (ER) overview](general-electronic-reporting.md#component-versioning).</span></span>

> [!NOTE]
> <span data-ttu-id="00999-356">設定されたデータモデルは、**アンケート** の業務ドメインの概要を表わすものであり、Microsoft Dynamics 365 Finance に固有のアーティファクトとの関係はありません。</span><span class="sxs-lookup"><span data-stu-id="00999-356">The configured data model is your abstract representation of the **Questionnaire** business domain and contains no relations to artefacts that are specific to Microsoft Dynamics 365 Finance.</span></span>

## <a name="design-a-model-mapping-for-the-configured-data-model"></a><a name="DesignMapping"></a><span data-ttu-id="00999-357">構成済みのデータモデルで使用するモデル マッピングをデザインする</span><span class="sxs-lookup"><span data-stu-id="00999-357">Design a model mapping for the configured data model</span></span>

<span data-ttu-id="00999-358">電子レポート開発者のロールを付与されたユーザーは、**アンケート** データ モデルの[モデル マッピング](general-electronic-reporting.md#data-model-and-model-mapping-components)コンポーネントを含む、新たな ER 構成を作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="00999-358">As a user in the Electronic Reporting Developer role, you must create a new ER configuration that contains a [model mapping](general-electronic-reporting.md#data-model-and-model-mapping-components) component for the **Questionnaire** data model.</span></span> <span data-ttu-id="00999-359">このコンポーネントは、財務に特化して構成されたデータモデルを実装しています。</span><span class="sxs-lookup"><span data-stu-id="00999-359">Because this component implements the configured data model for Finance, it's Finance-specific.</span></span> <span data-ttu-id="00999-360">構成済みのデータモデルの実行時にアプリケーション データの入力に使用する必要があるアプリケーション オブジェクトを指定するには、モデルマッピング コンポーネントを構成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="00999-360">You must configure the model mapping component to specify the application objects that must be used to fill in the configured data model with application data at runtime.</span></span> <span data-ttu-id="00999-361">このタスクを完了するには、財務における **アンケート** 事業ドメインのデータ構造の実装についての詳細を把握しておく必要があります。</span><span class="sxs-lookup"><span data-stu-id="00999-361">To complete this task, you must be aware of the implementation details of the data structure of the **Questionnaire** business domain in Finance.</span></span>

<span data-ttu-id="00999-362">続いて[新しいモデル マッピング構成をインポートする](#ImportModelMapping) セクションに記載されている手順を完了すると、提供された XML ファイルから必要なデータ モデルをインポートすることができます。</span><span class="sxs-lookup"><span data-stu-id="00999-362">By completing the steps in the [Import a new model mapping configuration](#ImportModelMapping) section that follows, you can import the required model mapping configuration from the provided XML file.</span></span> <span data-ttu-id="00999-363">あるいは、[新しいモデル マッピング構成を作成する](#CreateModelMapping) セクションに記載されている手順を完了すると、ゼロからこのモデル マッピングを設計することができます。</span><span class="sxs-lookup"><span data-stu-id="00999-363">Alternatively, you can complete the steps in the [Create a new model mapping configuration](#CreateModelMapping) section to design this model mapping from scratch.</span></span>

### <a name="import-a-new-model-mapping-configuration"></a><a name="ImportModelMapping"></a><span data-ttu-id="00999-364">新しいモデル マッピング構成をインポートする</span><span class="sxs-lookup"><span data-stu-id="00999-364">Import a new model mapping configuration</span></span>

1. <span data-ttu-id="00999-365">[アンケート mapping.version.1.1.xml](https://go.microsoft.com/fwlink/?linkid=851448) ファイルをダウンロードし、ご利用のコンピューターに保存してください。</span><span class="sxs-lookup"><span data-stu-id="00999-365">Download the [Questionnaires mapping.version.1.1.xml](https://go.microsoft.com/fwlink/?linkid=851448) file, and save it to your local computer.</span></span>
2. <span data-ttu-id="00999-366">**組織管理** \> **ワークスペース** \> **電子申告** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="00999-366">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
3. <span data-ttu-id="00999-367">**電子レポート** ワークスペースで、**レポートの構成** を選択します。</span><span class="sxs-lookup"><span data-stu-id="00999-367">In the **Electronic reporting** workspace, select **Reporting configurations**.</span></span>
4. <span data-ttu-id="00999-368">操作ウィンドウで、**交換** \> **XML ファイルからロード** を選択します。</span><span class="sxs-lookup"><span data-stu-id="00999-368">On the Action Pane, select **Exchange** \> **Load from XML file**.</span></span>
5. <span data-ttu-id="00999-369">**参照** を選択し、**アンケート mapping.version.1.1.xml** ファイルを検索して、選択します。</span><span class="sxs-lookup"><span data-stu-id="00999-369">Select **Browse**, and then find and select the **Questionnaires mapping.version.1.1.xml** file.</span></span>
6. <span data-ttu-id="00999-370">**OK** を選択し、構成をインポートします。</span><span class="sxs-lookup"><span data-stu-id="00999-370">Select **OK** to import the configuration.</span></span>

<span data-ttu-id="00999-371">続けるには、次の手順をスキップしてください : [新しいモデル マッピング構成を作成する](#CreateModelMapping)。</span><span class="sxs-lookup"><span data-stu-id="00999-371">To continue, skip the next procedure, [Create a new model mapping configuration](#CreateModelMapping).</span></span>

### <a name="create-a-new-model-mapping-configuration"></a><a name="CreateModelMapping"></a><span data-ttu-id="00999-372">新しいモデル マッピング構成を作成する</span><span class="sxs-lookup"><span data-stu-id="00999-372">Create a new model mapping configuration</span></span>

1. <span data-ttu-id="00999-373">**組織管理** \> **電子申告** \> **構成** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="00999-373">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="00999-374">**構成** ページの、構成ツリーで、**アンケート モデル** を選択します。</span><span class="sxs-lookup"><span data-stu-id="00999-374">On the **Configurations** page, in the configuration tree, select **Questionnaire model**.</span></span>
3. <span data-ttu-id="00999-375">**構成の作成** を選択します。</span><span class="sxs-lookup"><span data-stu-id="00999-375">Select **Create configuration**.</span></span>
4. <span data-ttu-id="00999-376">ドロップダウン ダイアログ ボックスで、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="00999-376">In the drop-down dialog box, follow these steps:</span></span>

    1. <span data-ttu-id="00999-377">**新規** フィールドで、**データ モデル アンケートに基づいたモデル マッピング** を選択します。</span><span class="sxs-lookup"><span data-stu-id="00999-377">In the **New** field, select **Model Mapping based on data model Questionnaires**.</span></span>
    2. <span data-ttu-id="00999-378">**名前** フィールドに、**アンケート マッピング** と入力します。</span><span class="sxs-lookup"><span data-stu-id="00999-378">In the **Name** field, enter **Questionnaire mapping**.</span></span>
    3. <span data-ttu-id="00999-379">**データ モデル定義** フィールドで、**ルート** の定義を選択します。</span><span class="sxs-lookup"><span data-stu-id="00999-379">In the **Data model definition** field, select the **Root** definition.</span></span>
    4. <span data-ttu-id="00999-380">**構成を作成する** を選択して、構成を作成します。</span><span class="sxs-lookup"><span data-stu-id="00999-380">Select **Create configuration** to create the configuration.</span></span>

#### <a name="design-a-new-model-mapping-component"></a><a name="DesignMappingComponent"></a><span data-ttu-id="00999-381">新しいモデル マッピング コンポーネントを設計する</span><span class="sxs-lookup"><span data-stu-id="00999-381">Design a new model mapping component</span></span>

1. <span data-ttu-id="00999-382">**構成** ページの、構成ツリーで、**アンケート マッピング** を選択します。</span><span class="sxs-lookup"><span data-stu-id="00999-382">On the **Configurations** page, in the configuration tree, select **Questionnaire mapping**.</span></span>
2. <span data-ttu-id="00999-383">**デザイナー** を選択して、マッピングの一覧を開きます。</span><span class="sxs-lookup"><span data-stu-id="00999-383">Select **Designer** to open the list of mappings.</span></span>
3. <span data-ttu-id="00999-384">**ルート** 定義に対して自動的に追加された **アンケート マッピング** マッピングを選択します</span><span class="sxs-lookup"><span data-stu-id="00999-384">Select the **Questionnaires mapping** mapping that was automatically added for the **Root** definition</span></span>
4. <span data-ttu-id="00999-385">**デザイナー** を選択して、選択したマッピングの構成を開始します。</span><span class="sxs-lookup"><span data-stu-id="00999-385">Select **Designer** to start to configure the selected mapping.</span></span>

<span data-ttu-id="00999-386">**ルート定義** に新しいマッピングが自動的に追加されます。</span><span class="sxs-lookup"><span data-stu-id="00999-386">A new mapping is automatically added for the **Root** definition.</span></span> <span data-ttu-id="00999-387">このマッピングは、**モデル** の方向に対応しています。</span><span class="sxs-lookup"><span data-stu-id="00999-387">This mapping has the **To model** direction.</span></span> <span data-ttu-id="00999-388">そのため、このマッピングを使用してデータ モデルに必要なデータを入力することができます。</span><span class="sxs-lookup"><span data-stu-id="00999-388">Therefore, this mapping can be used to fill in a data model with required data.</span></span>

#### <a name="add-data-sources-to-access-application-tables"></a><a name="AddMmDataSource1"></a><span data-ttu-id="00999-389">データ ソースを追加してアプリケーション テーブルにアクセスする</span><span class="sxs-lookup"><span data-stu-id="00999-389">Add data sources to access application tables</span></span>

<span data-ttu-id="00999-390">アンケートの詳細を含むアプリケーション テーブルにアクセスするには、データソースを構成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="00999-390">You must configure data sources to access the application tables that contain questionnaire details.</span></span>

1. <span data-ttu-id="00999-391">**モデル マッピング デザイナー** ページの、**データ ソース タイプ** ペインで、**Dynamics 365 for Operations\\テーブル レコード** を選択します。</span><span class="sxs-lookup"><span data-stu-id="00999-391">On the **Model mapping designer** page, in the **Data source types** pane, select **Dynamics 365 for Operations\\Table records**.</span></span>
2. <span data-ttu-id="00999-392">KMCollection テーブルへのアクセスに使用する新しいデータ ソースを追加します。ここでは、すべてのレコードが単一のアンケートを表します :</span><span class="sxs-lookup"><span data-stu-id="00999-392">Add a new data source that will be used to access the KMCollection table, where every record represents a single questionnaire:</span></span>

    1. <span data-ttu-id="00999-393">**データ ソース** ペインで、**ルートの追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="00999-393">In the **Data sources** pane, select **Add root**.</span></span>
    2. <span data-ttu-id="00999-394">ダイアログ ボックスの **名前** フィールドに **アンケート** と入力します。</span><span class="sxs-lookup"><span data-stu-id="00999-394">In dialog box, in the **Name** field, enter **Questionnaire**.</span></span>
    3. <span data-ttu-id="00999-395">**テーブル** フィールドに、**KMCollection** と入力します。</span><span class="sxs-lookup"><span data-stu-id="00999-395">In the **Table** field, enter **KMCollection**.</span></span>
    4. <span data-ttu-id="00999-396">**問い合わせをする** オプションを **はい** に設定します。</span><span class="sxs-lookup"><span data-stu-id="00999-396">Set the **Ask for query** option to **Yes**.</span></span> <span data-ttu-id="00999-397">これにより、実行時に [システムクエリ] ダイアログボックスで、このテーブルに[フィルタ処理](../../fin-ops/get-started/advanced-filtering-query-options.md)オプションを指定できるようになります。</span><span class="sxs-lookup"><span data-stu-id="00999-397">You will then be able to specify [filtering](../../fin-ops/get-started/advanced-filtering-query-options.md) options for this table in the system query dialog box at runtime.</span></span>
    5. <span data-ttu-id="00999-398">**OK** を選択して新しいデータ ソースを追加します。</span><span class="sxs-lookup"><span data-stu-id="00999-398">Select **OK** to add the new data source.</span></span>

3. <span data-ttu-id="00999-399">**データ ソース タイプ** ペインで、**Dynamics 365 for Operations\\テーブル レコード** を選択します。</span><span class="sxs-lookup"><span data-stu-id="00999-399">In the **Data source types** pane, select **Dynamics 365 for Operations\\Table records**.</span></span>
4. <span data-ttu-id="00999-400">KMQuestion テーブルへのアクセスに使用する新しいデータ ソースを追加します。ここでは、すべてのレコードが単一の質問を表します :</span><span class="sxs-lookup"><span data-stu-id="00999-400">Add a new data source that will be used to access the KMQuestion table, where every record represents a single question in a questionnaire:</span></span>

    1. <span data-ttu-id="00999-401">**データ ソース** ペインで、**ルートの追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="00999-401">In the **Data sources** pane, select **Add root**.</span></span>
    2. <span data-ttu-id="00999-402">ダイアログ ボックスで、**名前** フィールドに **質問** と入力します。</span><span class="sxs-lookup"><span data-stu-id="00999-402">In the dialog box, in the **Name** field, enter **Question**.</span></span>
    3. <span data-ttu-id="00999-403">**テーブル** フィールドに、**KMQuestion** と入力します。</span><span class="sxs-lookup"><span data-stu-id="00999-403">In the **Table** field, enter **KMQuestion**.</span></span>
    4. <span data-ttu-id="00999-404">**OK** を選択して新しいデータ ソースを追加します。</span><span class="sxs-lookup"><span data-stu-id="00999-404">Select **OK** to add the new data source.</span></span>

5. <span data-ttu-id="00999-405">**データ ソース タイプ** ペインで、**Dynamics 365 for Operations\\テーブル レコード** を選択します。</span><span class="sxs-lookup"><span data-stu-id="00999-405">In the **Data source types** pane, select **Dynamics 365 for Operations\\Table records**.</span></span>
6. <span data-ttu-id="00999-406">KMAnswer テーブルへのアクセスに使用する新しいデータ ソースを追加します。ここでは、すべてのレコードが回答の質問を表します :</span><span class="sxs-lookup"><span data-stu-id="00999-406">Add a new data source try that will be used to access the KMAnswer table, where every record represents a single answer to a question in a questionnaire:</span></span>

    1. <span data-ttu-id="00999-407">**データ ソース** ペインで、**ルートの追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="00999-407">In the **Data sources** pane, select **Add root**.</span></span>
    2. <span data-ttu-id="00999-408">**名前** フィールドに、**回答** と入力します。</span><span class="sxs-lookup"><span data-stu-id="00999-408">In the **Name** field, enter **Answer**.</span></span>
    3. <span data-ttu-id="00999-409">**テーブル** フィールドに、**KMAnswer** と入力します。</span><span class="sxs-lookup"><span data-stu-id="00999-409">In the **Table** field, enter **KMAnswer**.</span></span>
    4. <span data-ttu-id="00999-410">**OK** を選択して新しいデータ ソースを追加します。</span><span class="sxs-lookup"><span data-stu-id="00999-410">Select **OK** to add the new data source.</span></span>

7. <span data-ttu-id="00999-411">**データ ソース タイプ** ペインで、 **Functions\\計算フィールド** を選択します。</span><span class="sxs-lookup"><span data-stu-id="00999-411">In the **Data source types** pane, select **Functions\\Calculated field**.</span></span>
8. <span data-ttu-id="00999-412">親となる KMCollection テーブルのすべてのレコードから KMQuestionResultGroup テーブルのレコードへのアクセスに使用する新しい計算フィールドを追加します。</span><span class="sxs-lookup"><span data-stu-id="00999-412">Add a new calculated field that will be used to access a record of the KMQuestionResultGroup table from every record of the parent KMCollection table:</span></span>

    1. <span data-ttu-id="00999-413">**データ ソース** ペインで、**アンケート** を選択します。</span><span class="sxs-lookup"><span data-stu-id="00999-413">In the **Data sources** pane, select **Questionnaire**.</span></span>
    2. <span data-ttu-id="00999-414">**追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="00999-414">Select **Add**.</span></span>
    3. <span data-ttu-id="00999-415">ダイアログ ボックスで、**名前** フィールドに **\$ResultGroup** と入力します。</span><span class="sxs-lookup"><span data-stu-id="00999-415">In the dialog box, in the **Name** field, enter **\$ResultGroup**.</span></span>
    4. <span data-ttu-id="00999-416">**式の編集** を選択します。</span><span class="sxs-lookup"><span data-stu-id="00999-416">Select **Edit formula**.</span></span>
    5. <span data-ttu-id="00999-417">[ER 式エディター](general-electronic-reporting-formula-designer.md)で、 **式** フィールドに **FIRSTORNULL(\@.'\<Relations'.KMQuestionResultGroup)**  と入力し、KMCollection テーブルと KMQuestionResultGroup テーブル間の一対多の関係の[パス](er-formula-language.md#paths)を使用します。</span><span class="sxs-lookup"><span data-stu-id="00999-417">In the [ER formula editor](general-electronic-reporting-formula-designer.md), in the **Formula** field, enter **FIRSTORNULL(\@.'\<Relations'.KMQuestionResultGroup)** to use the [path](er-formula-language.md#paths) of the one-to-many relation between the KMCollection and KMQuestionResultGroup tables.</span></span>
    6. <span data-ttu-id="00999-418">**保存** を選択し、式エディターを閉じます。</span><span class="sxs-lookup"><span data-stu-id="00999-418">Select **Save**, and close the formula editor.</span></span>
    7. <span data-ttu-id="00999-419">**OK** を選択して新しい計算フィールドを追加します。</span><span class="sxs-lookup"><span data-stu-id="00999-419">Select **OK** to add the new calculated field.</span></span>

9. <span data-ttu-id="00999-420">**データ ソース タイプ** ペインで、 **Functions\\計算フィールド** を選択します。</span><span class="sxs-lookup"><span data-stu-id="00999-420">In the **Data source types** pane, select **Functions\\Calculated field**.</span></span>
10. <span data-ttu-id="00999-421">親となる KMCollectionQuestion テーブルのすべてのレコードから KMQuestion テーブルの質問レコードへのアクセスに使用する新しい計算フィールドを追加します。</span><span class="sxs-lookup"><span data-stu-id="00999-421">Add a new calculated field that will be used to access question records of the KMQuestion table from every record of the parent KMCollectionQuestion table:</span></span>

    1. <span data-ttu-id="00999-422">**データ ソース** ペインで、**アンケート** を選択します。</span><span class="sxs-lookup"><span data-stu-id="00999-422">In the **Data sources** pane, select **Questionnaire**.</span></span>
    2. <span data-ttu-id="00999-423">KMCollection テーブルの1対多の関係を含む **\<関係性** ノードを展開します。</span><span class="sxs-lookup"><span data-stu-id="00999-423">Expand the **\<Relations** node that contains one-to-many relations of the KMCollection table.</span></span>
    3. <span data-ttu-id="00999-424">関連する **KMCollectionQuestion** テーブルを選択し、**追加** をクリックし ます。</span><span class="sxs-lookup"><span data-stu-id="00999-424">Select the related **KMCollectionQuestion** table, and then select **Add**.</span></span>
    4. <span data-ttu-id="00999-425">ダイアログ ボックスで、 **名前**  フィールドに **\$Question** と入力します。</span><span class="sxs-lookup"><span data-stu-id="00999-425">In the dialog box, in the **Name** field, enter **\$Question**.</span></span>
    5. <span data-ttu-id="00999-426">**式の編集** を選択します。</span><span class="sxs-lookup"><span data-stu-id="00999-426">Select **Edit formula**.</span></span>
    6. <span data-ttu-id="00999-427">式エディターの **式** フィールドで、**FIRSTORNULL (FILTER(Question, Question.kmQuestionId = \@.kmQuestionId))** と入力し、KMQuestion テーブルから適切な質問レコードを返します。</span><span class="sxs-lookup"><span data-stu-id="00999-427">In the formula editor, in the **Formula** field, enter **FIRSTORNULL (FILTER(Question, Question.kmQuestionId = \@.kmQuestionId))** to return the appropriate question records from the KMQuestion table.</span></span>
    7. <span data-ttu-id="00999-428">**保存** を選択し、式エディターを閉じます。</span><span class="sxs-lookup"><span data-stu-id="00999-428">Select **Save**, and close the formula editor.</span></span>
    8. <span data-ttu-id="00999-429">**OK** を選択して新しい計算フィールドを追加します。</span><span class="sxs-lookup"><span data-stu-id="00999-429">Select **OK** to add the new calculated field.</span></span>

11. <span data-ttu-id="00999-430">**データ ソース タイプ** ペインで、 **Functions\\計算フィールド** を選択します。</span><span class="sxs-lookup"><span data-stu-id="00999-430">In the **Data source types** pane, select **Functions\\Calculated field**.</span></span>
12. <span data-ttu-id="00999-431">親となる KMQuestion テーブルのすべてのレコードから KMAnswer テーブルの回答レコードへのアクセスに使用する新しい計算フィールドを追加します。</span><span class="sxs-lookup"><span data-stu-id="00999-431">Add a new calculated field that will be used to access answer records of the KMAnswer table from every record of the parent KMQuestion table:</span></span>

    1. <span data-ttu-id="00999-432">**データソース** ペインで、**Questionnaire.\<Relations.KMCollectionQuestion.\$Question** を選択し、続いて **追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="00999-432">In the **Data sources** pane, select **Questionnaire.\<Relations.KMCollectionQuestion.\$Question**, and then select **Add**.</span></span>
    2. <span data-ttu-id="00999-433">ダイアログ ボックスで、**名前** フィールドに **\$Answer** と入力します。</span><span class="sxs-lookup"><span data-stu-id="00999-433">In the dialog box, in the **Name** field, enter **\$Answer**.</span></span>
    3. <span data-ttu-id="00999-434">**式の編集** を選択します。</span><span class="sxs-lookup"><span data-stu-id="00999-434">Select **Edit formula**.</span></span>
    4. <span data-ttu-id="00999-435">式エディターの **式** フィールドで、**FILTER (Answer, Answer.kmAnswerCollectionId = \@.kmAnswerCollectionId)** と入力し、KMAnswer テーブルから適切な回答レコードを返します。</span><span class="sxs-lookup"><span data-stu-id="00999-435">In the formula editor, in the **Formula** field, enter **FILTER (Answer, Answer.kmAnswerCollectionId = \@.kmAnswerCollectionId)** to return the appropriate answer records from the KMAnswer table.</span></span>
    5. <span data-ttu-id="00999-436">**保存** を選択し、式エディターを閉じます。</span><span class="sxs-lookup"><span data-stu-id="00999-436">Select **Save**, and close the formula editor.</span></span>
    6. <span data-ttu-id="00999-437">**OK** を選択して新しい計算フィールドを追加します。</span><span class="sxs-lookup"><span data-stu-id="00999-437">Select **OK** to add the new calculated field.</span></span>

13. <span data-ttu-id="00999-438">**データ ソース タイプ** ペインで、**Dynamics 365 for Operations\\テーブル** を選択します。</span><span class="sxs-lookup"><span data-stu-id="00999-438">In the **Data source types** pane, select **Dynamics 365 for Operations\\Table**.</span></span>
14. <span data-ttu-id="00999-439">会社情報テーブルのメソッドへのアクセスに使用する新しいデータ ソースを追加します。</span><span class="sxs-lookup"><span data-stu-id="00999-439">Add a new data source that will be used to access methods of the CompanyInfo table.</span></span> <span data-ttu-id="00999-440">このテーブルの **find()** メソッドは、このマッピングが呼び出された現在の財務インスタンスの会社を表すレコードを返すことに注意してください。</span><span class="sxs-lookup"><span data-stu-id="00999-440">Note that the **find()** method of this table returns a record that represents a company of the current Finance instance that this mapping is called in the context of.</span></span>

    1. <span data-ttu-id="00999-441">**データ ソース** ペインで、**ルートの追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="00999-441">In the **Data sources** pane, select **Add root**.</span></span>
    2. <span data-ttu-id="00999-442">ダイアログ ボックスの **名前** フィールドに **CompanyInfo** と入力します。</span><span class="sxs-lookup"><span data-stu-id="00999-442">In the dialog box, in the **Name** field, enter **CompanyInfo**.</span></span>
    3. <span data-ttu-id="00999-443">**テーブル** フィールドに、**CompanyInfo** と入力します。</span><span class="sxs-lookup"><span data-stu-id="00999-443">In the **Table** field, enter **CompanyInfo**.</span></span>
    4. <span data-ttu-id="00999-444">**OK** を選択して新しいデータ ソースを追加します。</span><span class="sxs-lookup"><span data-stu-id="00999-444">Select **OK** to add the new data source.</span></span>

#### <a name="add-data-sources-to-access-application-enumerations"></a><a name="AddMmDataSource2"></a><span data-ttu-id="00999-445">データ ソースを追加してアプリケーション リストにアクセスする</span><span class="sxs-lookup"><span data-stu-id="00999-445">Add data sources to access application enumerations</span></span>

<span data-ttu-id="00999-446">アプリケーション リストへのアクセスに使用するデータ ソースを構成し、その値をアプリケーション テーブルの **列挙** 型のフィールドの値と比較する必要があります。</span><span class="sxs-lookup"><span data-stu-id="00999-446">You must configure data sources to access application enumerations and compare their values with values of fields of the **Enumeration** type in the application tables.</span></span> <span data-ttu-id="00999-447">データ モデルの適切なフィールドにデータを入力するには、比較の結果を使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="00999-447">You must use the result of the comparison to fill in appropriate fields of the data model.</span></span>

1. <span data-ttu-id="00999-448">**モデル マッピング デザイナー** ページの、**データ ソース タイプ** ペインで、**Dynamics 365 for Operations\\列挙型** を選択します。</span><span class="sxs-lookup"><span data-stu-id="00999-448">On the **Model mapping designer** page, in the **Data source types** pane, select **Dynamics 365 for Operations\\Enumeration**.</span></span>
2. <span data-ttu-id="00999-449">**EnumAppNoYes** リストの値へのアクセスに使用する新しいデータ ソースを追加します :</span><span class="sxs-lookup"><span data-stu-id="00999-449">Add a new data source that will be used to access values of the **EnumAppNoYes** enumeration:</span></span>

    1. <span data-ttu-id="00999-450">**データ ソース** ペインで、**ルートの追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="00999-450">In the **Data sources** pane, select **Add root**.</span></span>
    2. <span data-ttu-id="00999-451">ダイアログ ボックスの **名前** フィールドに **EnumAppNoYes** と入力します。</span><span class="sxs-lookup"><span data-stu-id="00999-451">In the dialog box, in the **Name** field, enter **EnumAppNoYes**.</span></span>
    3. <span data-ttu-id="00999-452">**リスト** フィールドに、**NoYes** と入力します。</span><span class="sxs-lookup"><span data-stu-id="00999-452">In the **Enumeration** field, enter **NoYes**.</span></span>
    4. <span data-ttu-id="00999-453">**OK** を選択して新しいデータ ソースを追加します。</span><span class="sxs-lookup"><span data-stu-id="00999-453">Select **OK** to add the new data source.</span></span>

3. <span data-ttu-id="00999-454">**データ ソース タイプ** ペインで、**Dynamics 365 for Operations\\\列挙型** を選択します。</span><span class="sxs-lookup"><span data-stu-id="00999-454">In the **Data source types** pane, select **Dynamics 365 for Operations\\Enumeration**.</span></span>
4. <span data-ttu-id="00999-455">**KMCollectionQuestionMode** リストの値へのアクセスに使用する新しいデータ ソースを追加します :</span><span class="sxs-lookup"><span data-stu-id="00999-455">Add a new data source that will be used to access the values of the **KMCollectionQuestionMode** enumeration:</span></span>

    1. <span data-ttu-id="00999-456">**データ ソース** ペインで、**ルートの追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="00999-456">In the **Data sources** pane, select **Add root**.</span></span>
    2. <span data-ttu-id="00999-457">ドロップダウン ダイアログボックスの **名前** フィールドに **EnumAppQuestionOrder** と入力します。</span><span class="sxs-lookup"><span data-stu-id="00999-457">In the dialog box, in the **Name** field, enter **EnumAppQuestionOrder**.</span></span>
    3. <span data-ttu-id="00999-458">**リスト** フィールドに、**KMCollectionQuestionMode** と入力します。</span><span class="sxs-lookup"><span data-stu-id="00999-458">In the **Enumeration** field, enter **KMCollectionQuestionMode**.</span></span>
    4. <span data-ttu-id="00999-459">**OK** を選択して新しいデータ ソースを追加します。</span><span class="sxs-lookup"><span data-stu-id="00999-459">Select **OK** to add the new data source.</span></span>

#### <a name="add-er-labels-to-generate-a-report-in-a-specified-language"></a><a name="AddMmLabels"></a><span data-ttu-id="00999-460">ER ラベルを追加して指定した言語でレポートを生成する</span><span class="sxs-lookup"><span data-stu-id="00999-460">Add ER labels to generate a report in a specified language</span></span>

<span data-ttu-id="00999-461">ER ラベルを追加して、モデル マッピングを呼び出すコンテキストで定義された言語に依存する値を返すよう、データ ソースの一部を構成することができます。</span><span class="sxs-lookup"><span data-stu-id="00999-461">You can add ER labels to configure some of your data sources to return values that depend on the language that is defined in the context of the model mapping's call.</span></span>

1. <span data-ttu-id="00999-462">**モデル マッピング デザイナー**  ページの、 **データ ソース** ペインで、**回答** を選択し、続いて **編集** を選択します。</span><span class="sxs-lookup"><span data-stu-id="00999-462">On the **Model mapping designer** page, in the **Data sources** pane, select **Answer**, and then select **Edit**.</span></span>
2. <span data-ttu-id="00999-463">**ラベル** フィールドをアクティブ化します。</span><span class="sxs-lookup"><span data-stu-id="00999-463">Activate the **Label** field.</span></span>
3. <span data-ttu-id="00999-464">**翻訳** を選択します。</span><span class="sxs-lookup"><span data-stu-id="00999-464">Select **Translate**.</span></span>
4. <span data-ttu-id="00999-465">**テキストの翻訳** ダイアログ ボックスで、次の手順に従ってください :</span><span class="sxs-lookup"><span data-stu-id="00999-465">In the **Text translation** dialog box, follow these steps:</span></span>

    1. <span data-ttu-id="00999-466">**ラベル ID** フィールドで、**PositiveAnswer** と入力します。</span><span class="sxs-lookup"><span data-stu-id="00999-466">In the **Label Id** field, enter **PositiveAnswer**.</span></span>
    2. <span data-ttu-id="00999-467">**既定の言語のテキスト** フィールドに **はい** と入力します。</span><span class="sxs-lookup"><span data-stu-id="00999-467">In the **Text in default language** field, enter **Yes**.</span></span>
    3. <span data-ttu-id="00999-468">**翻訳** を選択します。</span><span class="sxs-lookup"><span data-stu-id="00999-468">Select **Translate**.</span></span>
    4. <span data-ttu-id="00999-469">**ラベル ID** フィールドで、**NegativeAnswer** と入力します。</span><span class="sxs-lookup"><span data-stu-id="00999-469">In the **Label Id** field, enter **NegativeAnswer**.</span></span>
    5. <span data-ttu-id="00999-470">**既定の言語のテキスト** フィールドに **いいえ** と入力します。</span><span class="sxs-lookup"><span data-stu-id="00999-470">In the **Text in default language** field, enter **No**.</span></span>
    6. <span data-ttu-id="00999-471">**翻訳** を選択します。</span><span class="sxs-lookup"><span data-stu-id="00999-471">Select **Translate**.</span></span>

5. <span data-ttu-id="00999-472">**テキストの翻訳** ダイアログ ボックスを閉じます。</span><span class="sxs-lookup"><span data-stu-id="00999-472">Close the **Text translation** dialog box.</span></span>
6. <span data-ttu-id="00999-473">**キャンセル** を選択します。</span><span class="sxs-lookup"><span data-stu-id="00999-473">Select **Cancel**.</span></span>

![編集可能なモデル マッピングへの ER ラベルの追加](./media/er-quick-start1-adding-labels.png)

<span data-ttu-id="00999-475">既定の言語に対してのみ ER ラベルを入力しました。</span><span class="sxs-lookup"><span data-stu-id="00999-475">You've entered ER labels only for the default language.</span></span> <span data-ttu-id="00999-476">ER ラベルを他の言語に翻訳する方法については、[多言語のレポートを設計する](er-design-multilingual-reports.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="00999-476">For information about how ER labels can be translated into other languages, see [Design multilingual reports](er-design-multilingual-reports.md).</span></span>

#### <a name="add-a-data-source-to-transform-the-results-of-comparing-enumeration-values-to-a-text-value"></a><a name="AddMmDataSource3"></a><span data-ttu-id="00999-477">データ ソースを追加してリストの比較結果値をテキスト値に変換する</span><span class="sxs-lookup"><span data-stu-id="00999-477">Add a data source to transform the results of comparing enumeration values to a text value</span></span>

<span data-ttu-id="00999-478">列挙値とテキスト値の比較結果は、差分ソースに対して何度か変換する必要があるため、このロジックを単一のデータソースとして構成することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="00999-478">Because you must transform the results of the comparison between enumeration values and text values several times for difference sources, it's a good idea to configure this logic as a single data source.</span></span> <span data-ttu-id="00999-479">ただし、このデータソースを再利用できるようにするには、パラメーター化されたデータソースとして設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="00999-479">However, to make this data source reusable, you must then configure it as the parametrized data source.</span></span> <span data-ttu-id="00999-480">詳細情報については、[計算フィールド タイプのER データ ソースのパラメーター化された呼び出しに対応する](er-calculated-field-type.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="00999-480">For more information, see [Support parameterized calls of ER data sources of the Calculated field type](er-calculated-field-type.md).</span></span>

1. <span data-ttu-id="00999-481">**モデル マッピング デザイナー**  ページの、**データ ソース タイプ**  ペインで、**全般\\空のコンテナー** を選択します。</span><span class="sxs-lookup"><span data-stu-id="00999-481">On the **Model mapping designer** page, in the **Data source types** pane, select **General\\Empty container**.</span></span>
2. <span data-ttu-id="00999-482">新しいコンテナー データ ソースを追加します :</span><span class="sxs-lookup"><span data-stu-id="00999-482">Add a new container data source:</span></span>

    1. <span data-ttu-id="00999-483">**データ ソース** ペインで、**ルートの追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="00999-483">In the **Data sources** pane, select **Add root**.</span></span>
    2. <span data-ttu-id="00999-484">ダイアログ ボックスで、**名前** フィールドに **ヘルパー** と入力します。</span><span class="sxs-lookup"><span data-stu-id="00999-484">In the dialog box, in the **Name** field, enter **Helper**.</span></span>
    3. <span data-ttu-id="00999-485">**OK** を選択し、新しいコンテナー データ ソースを追加します。</span><span class="sxs-lookup"><span data-stu-id="00999-485">Select **OK** to add the new container data source.</span></span>

3. <span data-ttu-id="00999-486">**データ ソース タイプ** ペインで、 **Functions\\計算フィールド** を選択します。</span><span class="sxs-lookup"><span data-stu-id="00999-486">In the **Data source types** pane, select **Functions\\Calculated field**.</span></span>
4. <span data-ttu-id="00999-487">新しいデータ ソースを追加します :</span><span class="sxs-lookup"><span data-stu-id="00999-487">Add a new data source:</span></span>

    1. <span data-ttu-id="00999-488">**データ ソース** ペインで、**ヘルパー** を選択します。</span><span class="sxs-lookup"><span data-stu-id="00999-488">In the **Data sources** pane, select **Helper**.</span></span>
    2. <span data-ttu-id="00999-489">**追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="00999-489">Select **Add**.</span></span>
    3. <span data-ttu-id="00999-490">ドロップダウン ダイアログボックスの **名前** フィールドに **NoYesEnumToString** と入力します。</span><span class="sxs-lookup"><span data-stu-id="00999-490">In the dialog box, in the **Name** field, enter **NoYesEnumToString**.</span></span>
    4. <span data-ttu-id="00999-491">**式の編集** を選択します。</span><span class="sxs-lookup"><span data-stu-id="00999-491">Select **Edit formula**.</span></span>
    5. <span data-ttu-id="00999-492">式エディターで、**パラメーター** を選択します。</span><span class="sxs-lookup"><span data-stu-id="00999-492">In the formula editor, select **Parameters**.</span></span>
    6. <span data-ttu-id="00999-493">次の手順に従い、構成された式のパラメータを指定します :</span><span class="sxs-lookup"><span data-stu-id="00999-493">Follow these steps to specify parameters for the configured expression:</span></span>

        1. <span data-ttu-id="00999-494">**新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="00999-494">Select **New**.</span></span>
        2. <span data-ttu-id="00999-495">ダイアログ ボックスで、**名前** フィールドに **引数** と入力します。</span><span class="sxs-lookup"><span data-stu-id="00999-495">In the dialog box, in the **Name** field, enter **Argument**.</span></span>
        3. <span data-ttu-id="00999-496">**タイプ** フィールドで、データー型に **ブール** を選択します。</span><span class="sxs-lookup"><span data-stu-id="00999-496">In the **Type** field, select the **Boolean** data type.</span></span>
        4. <span data-ttu-id="00999-497">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="00999-497">Select **OK**.</span></span>

    7. <span data-ttu-id="00999-498">**式** フィールドで、**IF (Argument = true, \@"GER\_LABEL:PositiveAnswer", \@"GER\_LABEL:NegativeAnswer")** と入力し、適切な ER ラベルのテキストを返すよう設定します。ER ラベルは実行コンテキストの言語と指定されたパラメータの値によって異なります。</span><span class="sxs-lookup"><span data-stu-id="00999-498">In the **Formula** field, enter **IF (Argument = true, \@"GER\_LABEL:PositiveAnswer", \@"GER\_LABEL:NegativeAnswer")** to return the text of the appropriate ER label, depending on the language of the execution context and value of the specified parameter.</span></span>
    8. <span data-ttu-id="00999-499">**保存** を選択し、式エディターを閉じます。</span><span class="sxs-lookup"><span data-stu-id="00999-499">Select **Save**, and close the formula editor.</span></span>
    9. <span data-ttu-id="00999-500">**OK** を選択して新しいデータ ソースを追加します。</span><span class="sxs-lookup"><span data-stu-id="00999-500">Select **OK** to add the new data source.</span></span>

![ER モデル マッピング デザイナーで構成されたモデル マッピング](./media/er-quick-start1-added-data-sources.png)

#### <a name="bind-data-sources-to-data-model-fields"></a><a name="AddMmBindings1"></a><span data-ttu-id="00999-502">データ ソースをデータ モデル フィールドにバインドする</span><span class="sxs-lookup"><span data-stu-id="00999-502">Bind data sources to data model fields</span></span>

<span data-ttu-id="00999-503">構成されたデータ ソースをデータ モデルのフィールドにバインドして、実行時にアプリケーション データに対するデータ モデルの入力方法を指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="00999-503">You must bind the configured data sources to the fields of the data model to specify how the data model will by filled in with application data at runtime.</span></span>

1. <span data-ttu-id="00999-504">**モデル マッピング デザイナー** ページの、**データ モデル** ペインで、**CompanyName** を選択します。</span><span class="sxs-lookup"><span data-stu-id="00999-504">On the **Model mapping designer** page, in the **Data model** pane, select **CompanyName**.</span></span>
2. <span data-ttu-id="00999-505">**データ ソース** ペインで、**CompanyInfo** を展開し、続いて以下の手順を実行します :</span><span class="sxs-lookup"><span data-stu-id="00999-505">In the **Data sources** pane, expand **CompanyInfo**, and then follow these steps:</span></span>

    1. <span data-ttu-id="00999-506">CompanyInfo テーブルの **find()** メソッドを表わす、**CompanyInfo.find()** ノードを展開します。</span><span class="sxs-lookup"><span data-stu-id="00999-506">Expand the **CompanyInfo.find()** node that represents the **find()** method of the CompanyInfo table.</span></span>
    2. <span data-ttu-id="00999-507">**CompanyInfo.find().Name** を選択します。</span><span class="sxs-lookup"><span data-stu-id="00999-507">Select **CompanyInfo.find().Name**.</span></span>
    3. <span data-ttu-id="00999-508">**バインド** を選択し、構成されたモデル マッピングが実行時のコンテキストで呼び出される会社名を入力します。</span><span class="sxs-lookup"><span data-stu-id="00999-508">Select **Bind** to fill in the name of the company that the configured model mapping is called in the context of at runtime.</span></span>

3. <span data-ttu-id="00999-509">**データ モデル** ペインで、**アンケート** を選択します。</span><span class="sxs-lookup"><span data-stu-id="00999-509">In the **Data model** pane, select **Questionnaire**.</span></span>
4. <span data-ttu-id="00999-510">**データ ソース** ペインで、**Questionnaire** を選択し、続いて **Bind** を選択してアンケートのレコードを入力します。</span><span class="sxs-lookup"><span data-stu-id="00999-510">In the **Data sources** pane, select **Questionnaire**, and then select **Bind** to fill in questionnaire records.</span></span>
5. <span data-ttu-id="00999-511">**データ モデル** ペインで、**アンケート** を展開し、続いて以下の手順を実行します :</span><span class="sxs-lookup"><span data-stu-id="00999-511">In the **Data model** pane, expand **Questionnaire**, and then follow these steps:</span></span>

    1. <span data-ttu-id="00999-512">**データ モデル** ペインで、**アクティブ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="00999-512">In the **Data model** pane, select **Active**.</span></span>
    2. <span data-ttu-id="00999-513">**データ モデル** ペインで、**編集** を選択します。</span><span class="sxs-lookup"><span data-stu-id="00999-513">In the **Data model** pane, select **Edit**.</span></span>
    3. <span data-ttu-id="00999-514">**式** フィールドに **Helper.NoYesEnumToString (\@.Active = EnumAppNoYes.Yes)** と入力し、リストされた値間の比較を行ったテキスト依存、言語依存の結果を入力します。</span><span class="sxs-lookup"><span data-stu-id="00999-514">In the **Formula** field, enter **Helper.NoYesEnumToString (\@.Active = EnumAppNoYes.Yes)** to fill the text-dependent and language-dependent result of the comparison between enumeration values.</span></span>

6. <span data-ttu-id="00999-515">以下の結果が得られるまで、同じ方法でデータ ソースをデータ モデル フィールドにバインドしていきます。</span><span class="sxs-lookup"><span data-stu-id="00999-515">Continue to bind data sources to data model fields in the same manner until you achieve the following result.</span></span>

    | <span data-ttu-id="00999-516">フィールド パス</span><span class="sxs-lookup"><span data-stu-id="00999-516">Field path</span></span>                                              | <span data-ttu-id="00999-517">データ型</span><span class="sxs-lookup"><span data-stu-id="00999-517">Data type</span></span>   | <span data-ttu-id="00999-518">アクション</span><span class="sxs-lookup"><span data-stu-id="00999-518">Action</span></span> | <span data-ttu-id="00999-519">バインド式</span><span class="sxs-lookup"><span data-stu-id="00999-519">Binding expression</span></span> |
    |---------------------------------------------------------|-------------|--------|--------------------|
    | <span data-ttu-id="00999-520">CompanyName</span><span class="sxs-lookup"><span data-stu-id="00999-520">CompanyName</span></span>                                             | <span data-ttu-id="00999-521">文字列</span><span class="sxs-lookup"><span data-stu-id="00999-521">String</span></span>      | <span data-ttu-id="00999-522">バインド</span><span class="sxs-lookup"><span data-stu-id="00999-522">Bind</span></span>   | <span data-ttu-id="00999-523">CompanyInfo.'find()'.Name</span><span class="sxs-lookup"><span data-stu-id="00999-523">CompanyInfo.'find()'.Name</span></span> |
    | <span data-ttu-id="00999-524">アンケート</span><span class="sxs-lookup"><span data-stu-id="00999-524">Questionnaire</span></span>                                           | <span data-ttu-id="00999-525">レコード リスト</span><span class="sxs-lookup"><span data-stu-id="00999-525">Record list</span></span> | <span data-ttu-id="00999-526">バインド</span><span class="sxs-lookup"><span data-stu-id="00999-526">Bind</span></span>   | <span data-ttu-id="00999-527">アンケート</span><span class="sxs-lookup"><span data-stu-id="00999-527">Questionnaire</span></span> |
    | <span data-ttu-id="00999-528">Questionnaire\\Active</span><span class="sxs-lookup"><span data-stu-id="00999-528">Questionnaire\\Active</span></span>                                   | <span data-ttu-id="00999-529">文字列</span><span class="sxs-lookup"><span data-stu-id="00999-529">String</span></span>      | <span data-ttu-id="00999-530">編集</span><span class="sxs-lookup"><span data-stu-id="00999-530">Edit</span></span>   | <span data-ttu-id="00999-531">Helper.NoYesEnumToString(\@.active = EnumAppNoYes.Yes)</span><span class="sxs-lookup"><span data-stu-id="00999-531">Helper.NoYesEnumToString(\@.active = EnumAppNoYes.Yes)</span></span> |
    | <span data-ttu-id="00999-532">Questionnaire\\Code</span><span class="sxs-lookup"><span data-stu-id="00999-532">Questionnaire\\Code</span></span>                                     | <span data-ttu-id="00999-533">文字列</span><span class="sxs-lookup"><span data-stu-id="00999-533">String</span></span>      | <span data-ttu-id="00999-534">バインド</span><span class="sxs-lookup"><span data-stu-id="00999-534">Bind</span></span>   | <span data-ttu-id="00999-535">\@.kmCollectionId</span><span class="sxs-lookup"><span data-stu-id="00999-535">\@.kmCollectionId</span></span> |
    | <span data-ttu-id="00999-536">Questionnaire\\Description</span><span class="sxs-lookup"><span data-stu-id="00999-536">Questionnaire\\Description</span></span>                              | <span data-ttu-id="00999-537">文字列</span><span class="sxs-lookup"><span data-stu-id="00999-537">String</span></span>      | <span data-ttu-id="00999-538">バインド</span><span class="sxs-lookup"><span data-stu-id="00999-538">Bind</span></span>   | <span data-ttu-id="00999-539">\@.Description</span><span class="sxs-lookup"><span data-stu-id="00999-539">\@.Description</span></span> |
    | <span data-ttu-id="00999-540">Questionnaire\\QuestionnaireType</span><span class="sxs-lookup"><span data-stu-id="00999-540">Questionnaire\\QuestionnaireType</span></span>                        | <span data-ttu-id="00999-541">文字列</span><span class="sxs-lookup"><span data-stu-id="00999-541">String</span></span>      | <span data-ttu-id="00999-542">バインド</span><span class="sxs-lookup"><span data-stu-id="00999-542">Bind</span></span>   | <span data-ttu-id="00999-543">\@.'&gt;Relations'.kmCollectionTypeId.Description</span><span class="sxs-lookup"><span data-stu-id="00999-543">\@.'&gt;Relations'.kmCollectionTypeId.Description</span></span> |
    | <span data-ttu-id="00999-544">Questionnaire\\QuestionOrder</span><span class="sxs-lookup"><span data-stu-id="00999-544">Questionnaire\\QuestionOrder</span></span>                            | <span data-ttu-id="00999-545">文字列</span><span class="sxs-lookup"><span data-stu-id="00999-545">String</span></span>      | <span data-ttu-id="00999-546">編集</span><span class="sxs-lookup"><span data-stu-id="00999-546">Edit</span></span>   | <span data-ttu-id="00999-547">CASE (\@.questionMode,</span><span class="sxs-lookup"><span data-stu-id="00999-547">CASE (\@.questionMode,</span></span><br><span data-ttu-id="00999-548">EnumAppQuestionOrder.Conditional, "Conditional",</span><span class="sxs-lookup"><span data-stu-id="00999-548">EnumAppQuestionOrder.Conditional, "Conditional",</span></span><br><span data-ttu-id="00999-549">EnumAppQuestionOrder.Random, "Random (percentage in questionnaire)",</span><span class="sxs-lookup"><span data-stu-id="00999-549">EnumAppQuestionOrder.Random, "Random (percentage in questionnaire)",</span></span><br><span data-ttu-id="00999-550">EnumAppQuestionOrder.RandomGroup, "Random (percentage in result groups)",</span><span class="sxs-lookup"><span data-stu-id="00999-550">EnumAppQuestionOrder.RandomGroup, "Random (percentage in result groups)",</span></span><br><span data-ttu-id="00999-551">EnumAppQuestionOrder.Sequence, "Sequential",</span><span class="sxs-lookup"><span data-stu-id="00999-551">EnumAppQuestionOrder.Sequence, "Sequential",</span></span><br><span data-ttu-id="00999-552">"")</span><span class="sxs-lookup"><span data-stu-id="00999-552">"")</span></span> |
    | <span data-ttu-id="00999-553">Questionnaire\\ResultsGroup</span><span class="sxs-lookup"><span data-stu-id="00999-553">Questionnaire\\ResultsGroup</span></span>                             | <span data-ttu-id="00999-554">レコード</span><span class="sxs-lookup"><span data-stu-id="00999-554">Record</span></span>      |        | |
    | <span data-ttu-id="00999-555">Questionnaire\\ResultsGroup\\Code</span><span class="sxs-lookup"><span data-stu-id="00999-555">Questionnaire\\ResultsGroup\\Code</span></span>                       | <span data-ttu-id="00999-556">文字列</span><span class="sxs-lookup"><span data-stu-id="00999-556">String</span></span>      | <span data-ttu-id="00999-557">バインド</span><span class="sxs-lookup"><span data-stu-id="00999-557">Bind</span></span>   | <span data-ttu-id="00999-558">\@.'\$ResultGroup'.kmQuestionResultGroupId</span><span class="sxs-lookup"><span data-stu-id="00999-558">\@.'\$ResultGroup'.kmQuestionResultGroupId</span></span> |
    | <span data-ttu-id="00999-559">Questionnaire\\ResultsGroup\\Description</span><span class="sxs-lookup"><span data-stu-id="00999-559">Questionnaire\\ResultsGroup\\Description</span></span>                | <span data-ttu-id="00999-560">文字列</span><span class="sxs-lookup"><span data-stu-id="00999-560">String</span></span>      | <span data-ttu-id="00999-561">バインド</span><span class="sxs-lookup"><span data-stu-id="00999-561">Bind</span></span>   | <span data-ttu-id="00999-562">\@.'\$ResultGroup'.description</span><span class="sxs-lookup"><span data-stu-id="00999-562">\@.'\$ResultGroup'.description</span></span> |
    | <span data-ttu-id="00999-563">Questionnaire\\ResultsGroup\\MaxNumberOfPoints</span><span class="sxs-lookup"><span data-stu-id="00999-563">Questionnaire\\ResultsGroup\\MaxNumberOfPoints</span></span>          | <span data-ttu-id="00999-564">実績</span><span class="sxs-lookup"><span data-stu-id="00999-564">Real</span></span>        | <span data-ttu-id="00999-565">バインド</span><span class="sxs-lookup"><span data-stu-id="00999-565">Bind</span></span>   | <span data-ttu-id="00999-566">\@.'\$ResultGroup'.maxPoint</span><span class="sxs-lookup"><span data-stu-id="00999-566">\@.'\$ResultGroup'.maxPoint</span></span> |
    | <span data-ttu-id="00999-567">Questionnaire\\Question</span><span class="sxs-lookup"><span data-stu-id="00999-567">Questionnaire\\Question</span></span>                                 | <span data-ttu-id="00999-568">レコード リスト</span><span class="sxs-lookup"><span data-stu-id="00999-568">Record list</span></span> | <span data-ttu-id="00999-569">バインド</span><span class="sxs-lookup"><span data-stu-id="00999-569">Bind</span></span>   | <span data-ttu-id="00999-570">\@.'&lt;Relations'.KMCollectionQuestion</span><span class="sxs-lookup"><span data-stu-id="00999-570">\@.'&lt;Relations'.KMCollectionQuestion</span></span> |
    | <span data-ttu-id="00999-571">Questionnaire\\Question\\CollectionSequenceNumber</span><span class="sxs-lookup"><span data-stu-id="00999-571">Questionnaire\\Question\\CollectionSequenceNumber</span></span>       | <span data-ttu-id="00999-572">整数</span><span class="sxs-lookup"><span data-stu-id="00999-572">Integer</span></span>     | <span data-ttu-id="00999-573">バインド</span><span class="sxs-lookup"><span data-stu-id="00999-573">Bind</span></span>   | <span data-ttu-id="00999-574">\@.answerCollectionSequenceNumber</span><span class="sxs-lookup"><span data-stu-id="00999-574">\@.answerCollectionSequenceNumber</span></span> |
    | <span data-ttu-id="00999-575">Questionnaire\\Question\\Id</span><span class="sxs-lookup"><span data-stu-id="00999-575">Questionnaire\\Question\\Id</span></span>                             | <span data-ttu-id="00999-576">文字列</span><span class="sxs-lookup"><span data-stu-id="00999-576">String</span></span>      | <span data-ttu-id="00999-577">バインド</span><span class="sxs-lookup"><span data-stu-id="00999-577">Bind</span></span>   | <span data-ttu-id="00999-578">\@.kmQuestionId</span><span class="sxs-lookup"><span data-stu-id="00999-578">\@.kmQuestionId</span></span> |
    | <span data-ttu-id="00999-579">Questionnaire\\Question\\MustBeCompleted</span><span class="sxs-lookup"><span data-stu-id="00999-579">Questionnaire\\Question\\MustBeCompleted</span></span>                | <span data-ttu-id="00999-580">文字列</span><span class="sxs-lookup"><span data-stu-id="00999-580">String</span></span>      | <span data-ttu-id="00999-581">編集</span><span class="sxs-lookup"><span data-stu-id="00999-581">Edit</span></span>   | <span data-ttu-id="00999-582">Helper.NoYesEnumToString(\@.mandatory = EnumAppNoYes.Yes)</span><span class="sxs-lookup"><span data-stu-id="00999-582">Helper.NoYesEnumToString(\@.mandatory = EnumAppNoYes.Yes)</span></span> |
    | <span data-ttu-id="00999-583">Questionnaire\\Question\\PrimaryQuestion</span><span class="sxs-lookup"><span data-stu-id="00999-583">Questionnaire\\Question\\PrimaryQuestion</span></span>                | <span data-ttu-id="00999-584">文字列</span><span class="sxs-lookup"><span data-stu-id="00999-584">String</span></span>      | <span data-ttu-id="00999-585">バインド</span><span class="sxs-lookup"><span data-stu-id="00999-585">Bind</span></span>   | <span data-ttu-id="00999-586">\@.parentQuestionId</span><span class="sxs-lookup"><span data-stu-id="00999-586">\@.parentQuestionId</span></span> |
    | <span data-ttu-id="00999-587">Questionnaire\\Question\\SequenceNumber</span><span class="sxs-lookup"><span data-stu-id="00999-587">Questionnaire\\Question\\SequenceNumber</span></span>                 | <span data-ttu-id="00999-588">整数</span><span class="sxs-lookup"><span data-stu-id="00999-588">Integer</span></span>     | <span data-ttu-id="00999-589">バインド</span><span class="sxs-lookup"><span data-stu-id="00999-589">Bind</span></span>   | <span data-ttu-id="00999-590">\@.SequenceNumber</span><span class="sxs-lookup"><span data-stu-id="00999-590">\@.SequenceNumber</span></span> |
    | <span data-ttu-id="00999-591">Questionnaire\\Question\\Text</span><span class="sxs-lookup"><span data-stu-id="00999-591">Questionnaire\\Question\\Text</span></span>                           | <span data-ttu-id="00999-592">文字列</span><span class="sxs-lookup"><span data-stu-id="00999-592">String</span></span>      | <span data-ttu-id="00999-593">バインド</span><span class="sxs-lookup"><span data-stu-id="00999-593">Bind</span></span>   | <span data-ttu-id="00999-594">\@.'\$Question'.text</span><span class="sxs-lookup"><span data-stu-id="00999-594">\@.'\$Question'.text</span></span> |
    | <span data-ttu-id="00999-595">Questionnaire\\Question\\Answer</span><span class="sxs-lookup"><span data-stu-id="00999-595">Questionnaire\\Question\\Answer</span></span>                         | <span data-ttu-id="00999-596">レコード リスト</span><span class="sxs-lookup"><span data-stu-id="00999-596">Record list</span></span> | <span data-ttu-id="00999-597">バインド</span><span class="sxs-lookup"><span data-stu-id="00999-597">Bind</span></span>   | <span data-ttu-id="00999-598">\@.'\$Question'.'\$Answer'</span><span class="sxs-lookup"><span data-stu-id="00999-598">\@.'\$Question'.'\$Answer'</span></span> |
    | <span data-ttu-id="00999-599">Questionnaire\\Question\\Answer\\CorrectAnswer</span><span class="sxs-lookup"><span data-stu-id="00999-599">Questionnaire\\Question\\Answer\\CorrectAnswer</span></span>          | <span data-ttu-id="00999-600">文字列</span><span class="sxs-lookup"><span data-stu-id="00999-600">String</span></span>      | <span data-ttu-id="00999-601">編集</span><span class="sxs-lookup"><span data-stu-id="00999-601">Edit</span></span>   | <span data-ttu-id="00999-602">Helper.NoYesEnumToString(\@.correctAnswer = EnumAppNoYes.Yes)</span><span class="sxs-lookup"><span data-stu-id="00999-602">Helper.NoYesEnumToString(\@.correctAnswer = EnumAppNoYes.Yes)</span></span> |
    | <span data-ttu-id="00999-603">Questionnaire\\Question\\Answer\\Points</span><span class="sxs-lookup"><span data-stu-id="00999-603">Questionnaire\\Question\\Answer\\Points</span></span>                 | <span data-ttu-id="00999-604">実績</span><span class="sxs-lookup"><span data-stu-id="00999-604">Real</span></span>        | <span data-ttu-id="00999-605">バインド</span><span class="sxs-lookup"><span data-stu-id="00999-605">Bind</span></span>   | <span data-ttu-id="00999-606">\@.point</span><span class="sxs-lookup"><span data-stu-id="00999-606">\@.point</span></span> |
    | <span data-ttu-id="00999-607">Questionnaire\\Question\\Answer\\SequenceNumber</span><span class="sxs-lookup"><span data-stu-id="00999-607">Questionnaire\\Question\\Answer\\SequenceNumber</span></span>         | <span data-ttu-id="00999-608">整数</span><span class="sxs-lookup"><span data-stu-id="00999-608">Integer</span></span>     | <span data-ttu-id="00999-609">バインド</span><span class="sxs-lookup"><span data-stu-id="00999-609">Bind</span></span>   | <span data-ttu-id="00999-610">\@.sequenceNumber</span><span class="sxs-lookup"><span data-stu-id="00999-610">\@.sequenceNumber</span></span> |
    | <span data-ttu-id="00999-611">Questionnaire\\Question\\Answer\\Text</span><span class="sxs-lookup"><span data-stu-id="00999-611">Questionnaire\\Question\\Answer\\Text</span></span>                   | <span data-ttu-id="00999-612">文字列</span><span class="sxs-lookup"><span data-stu-id="00999-612">String</span></span>      | <span data-ttu-id="00999-613">バインド</span><span class="sxs-lookup"><span data-stu-id="00999-613">Bind</span></span>   | <span data-ttu-id="00999-614">\@.text</span><span class="sxs-lookup"><span data-stu-id="00999-614">\@.text</span></span> |

    <span data-ttu-id="00999-615">以下の画面は、**モデル マッピング デザイナー** のページ上で構成されたモデル マッピングの最終的な状態を示して います。</span><span class="sxs-lookup"><span data-stu-id="00999-615">The following illustration shows the final state of the configured model mapping on the **Model mapping designer** page.</span></span>

    ![ER モデル マッピング デザイナーで構成が完了したモデル マッピング](./media/er-quick-start1-mapping2.png)

7. <span data-ttu-id="00999-617">変更を保存します。</span><span class="sxs-lookup"><span data-stu-id="00999-617">Save your changes.</span></span>
8. <span data-ttu-id="00999-618">**モデル マッピング デザイナー** ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="00999-618">Close the **Model mapping designer** page.</span></span>

#### <a name="complete-the-design-of-the-model-mapping"></a><a name="CompleteModelMapping"></a><span data-ttu-id="00999-619">モデル マッピングを完了する</span><span class="sxs-lookup"><span data-stu-id="00999-619">Complete the design of the model mapping</span></span>

1. <span data-ttu-id="00999-620">**組織管理** \> **電子申告** \> **構成** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="00999-620">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="00999-621">**構成** ページの、構成ツリーで、**アンケート マッピング** を選択します。</span><span class="sxs-lookup"><span data-stu-id="00999-621">On the **Configurations** page, in the configuration tree, select **Questionnaire mapping**.</span></span>
3. <span data-ttu-id="00999-622">**バージョン** クイック タブで、状態が **下書き** となっている構成のバージョンを選択します。</span><span class="sxs-lookup"><span data-stu-id="00999-622">On the **Versions** FastTab, select the configuration version that has a status of **Draft**.</span></span>
4. <span data-ttu-id="00999-623">**ステータスの変更** \> **完了** を選択します。</span><span class="sxs-lookup"><span data-stu-id="00999-623">Select **Change status** \> **Complete**.</span></span>

<span data-ttu-id="00999-624">この構成のバージョン 1.1 の状態 **下書き** から **完了** に変更されます。</span><span class="sxs-lookup"><span data-stu-id="00999-624">The status of version 1.1 of this configuration is changed from **Draft** to **Completed**.</span></span> <span data-ttu-id="00999-625">バージョン 1.1 を変更することはできなくなります。</span><span class="sxs-lookup"><span data-stu-id="00999-625">Version 1.1 can no longer be changed.</span></span> <span data-ttu-id="00999-626">このバージョンには、構成済みのモデル マッピングが含まれており、その他の ER の構成の基礎として使用できます。</span><span class="sxs-lookup"><span data-stu-id="00999-626">This version contains the configured model mapping and can be used as the basis for other ER configurations.</span></span> <span data-ttu-id="00999-627">この構成のバージョン 1.2 が作成され、状態が **下書き** になります。</span><span class="sxs-lookup"><span data-stu-id="00999-627">Version 1.2 of this configuration is created and has a status of **Draft**.</span></span> <span data-ttu-id="00999-628">このバージョンを編集して、**アンケート マッピング** の構成を調整することができます。</span><span class="sxs-lookup"><span data-stu-id="00999-628">You can edit this version to adjust the **Questionnaire mapping** configuration.</span></span>

![[構成] ページの編集可能な ER 構成のバージョン](./media/er-quick-start1-mapping-configuration.png)

> [!NOTE]
> <span data-ttu-id="00999-630">ご利用の財務に固有となる実装となり、**アンケート** 業務ドメインを表わす抽象データ モデルです。</span><span class="sxs-lookup"><span data-stu-id="00999-630">The configured model mapping is your Finance-specific implementation of the abstract data model that represents the **Questionnaire** business domain.</span></span>

## <a name="design-a-template-for-a-custom-report"></a><a name="DesignReportTemplate"></a><span data-ttu-id="00999-631">カスタム レポートで使用するテンプレートを設計する</span><span class="sxs-lookup"><span data-stu-id="00999-631">Design a template for a custom report</span></span>

<span data-ttu-id="00999-632">ER フレームワークは、定義済みのテンプレートを使用して、Microsoft Office 形式 (Excel ワークブック、または Word ドキュメント) でレポートを生成します。</span><span class="sxs-lookup"><span data-stu-id="00999-632">The ER framework uses predefined templates to generate reports in Microsoft Office formats (Excel workbooks or Word documents).</span></span> <span data-ttu-id="00999-633">必要なレポートが生成されている間、構成されたデータフローに従って、テンプレートに必要なデータが入力されます。</span><span class="sxs-lookup"><span data-stu-id="00999-633">While the required report is being generated, a template is filled in with required data according to the configured dataflow.</span></span> <span data-ttu-id="00999-634">ます、まずカスタム レポートデ使用するテンプレートを設計する必要があります。</span><span class="sxs-lookup"><span data-stu-id="00999-634">Therefore, you must first design a template for your custom report.</span></span> <span data-ttu-id="00999-635">このテンプレートは、カスタム レポートのレイアウトを表す構造を持つ Excel ワークブック形式で設計されている必要があります。</span><span class="sxs-lookup"><span data-stu-id="00999-635">This template must be designed as an Excel workbook, the structure of which represents the layout of a custom report.</span></span> <span data-ttu-id="00999-636">必要なデータを入力するすべての Excel 項目には名前を付ける必要があります。</span><span class="sxs-lookup"><span data-stu-id="00999-636">You must name every Excel item that you plan to fill in with required data.</span></span>

1. <span data-ttu-id="00999-637">[Questionnaires report template.xslx](https://go.microsoft.com/fwlink/?linkid=851448) ファイルをダウンロードし、ご利用のコンピューターに保存してください。</span><span class="sxs-lookup"><span data-stu-id="00999-637">Download the [Questionnaires report template.xslx](https://go.microsoft.com/fwlink/?linkid=851448) file, and save it to your local computer.</span></span>
2. <span data-ttu-id="00999-638">ファイルを Excel で開き、ブックの構造を確認します。</span><span class="sxs-lookup"><span data-stu-id="00999-638">Open the file in Excel, and review the structure of the workbook.</span></span>

<span data-ttu-id="00999-639">以下の図に示すように、ダウンロードしたテンプレートは、特定のアンケートの質問とその適切な回答を印刷する意図で設計されています。</span><span class="sxs-lookup"><span data-stu-id="00999-639">As the following illustration shows, the downloaded template has been designed to print specified questionnaires that present a questionnaire's questions together with appropriate answers.</span></span>

![指定されたアンケートを印刷する Excel テンプレート](./media/er-quick-start1-template-layout.png)

<span data-ttu-id="00999-641">このテンプレートに Excel 名が追加され、アンケートの詳細が入力されます。</span><span class="sxs-lookup"><span data-stu-id="00999-641">Excel names have been added to this template to fill in the questionnaire details.</span></span> <span data-ttu-id="00999-642">名前マネージャを使用すると、Excel の名前を確認できます。</span><span class="sxs-lookup"><span data-stu-id="00999-642">You can use Name Manager to review the Excel names.</span></span>

![名前マネージャを使用して入力だれた Excel テンプレートの名前を確認する](./media/er-quick-start1-template-names.png)

<span data-ttu-id="00999-644">レポート ラベルは、英語では固定テキストとして追加されています。</span><span class="sxs-lookup"><span data-stu-id="00999-644">Report labels have been added as fixed text in the English language.</span></span> <span data-ttu-id="00999-645">構成されたモデル マッピングの言語依存の式を使用した場合と同様に、ER フォーマット[ラベル](#AddMmLabels)を使用して、ラベルに入力する新しい Excel 名をレポート ラベルに置き換えることができます。</span><span class="sxs-lookup"><span data-stu-id="00999-645">You can replace the report labels with new Excel names that fill in the labels with language-dependent text by using the ER format [labels](#AddMmLabels), as you did for language-dependent expressions in the configured model mapping.</span></span> <span data-ttu-id="00999-646">この場合、ER ラベルを編集可能な形式で追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="00999-646">In this case, ER labels must be added in the editable ER format.</span></span>

<span data-ttu-id="00999-647">以下の画像のように、カスタム レポートのヘッダーを指定して、Excel が呼び出しできるようになっています。</span><span class="sxs-lookup"><span data-stu-id="00999-647">As the following illustration shows, the custom report header has been specified to enable Excel to do paging.</span></span>

![Excel テンプレートのカスタム レポート ヘッダー](./media/er-quick-start1-template-header.png)

## <a name="design-a-format"></a><a name="DesignFormat"></a><span data-ttu-id="00999-649">形式のデザイン</span><span class="sxs-lookup"><span data-stu-id="00999-649">Design a format</span></span>

<span data-ttu-id="00999-650">電子レポート機能コンサルタントのロールが付与されているユーザーは、[フォーマット](general-electronic-reporting.md#FormatComponentOutbound) コンポーネントを含む新しい ER 構成を作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="00999-650">As a user in the Electronic Reporting Functional Consultant role, you must create a new ER configuration that contains a [format](general-electronic-reporting.md#FormatComponentOutbound) component.</span></span> <span data-ttu-id="00999-651">実行時にレポートのテンプレートに必要となるデータをどのように入力するかを指定するには、フォーマットのコンポーネントを構成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="00999-651">You must configure the format component to specify how a report template will be filled in with required data at runtime.</span></span>

<span data-ttu-id="00999-652">[設計されたフォーマットの構成をインポートする](#FormatImport) セクションに記載されている手順を完了すると、提供された XML ファイルから必要なフォーマットをインポートすることができます。</span><span class="sxs-lookup"><span data-stu-id="00999-652">By completing the steps in the [Import a designed format configuration](#FormatImport) section, you can import the required format from the provided XML file.</span></span> <span data-ttu-id="00999-653">あるいは、[新しいフォーマットの構成を作成する](#FormatCreate) セクションに記載されている手順を完了すると、ゼロからこのフォーマットを設計することができます。</span><span class="sxs-lookup"><span data-stu-id="00999-653">Alternatively, you can complete the steps in the [Create a new format configuration](#FormatCreate) section to design this format from scratch.</span></span>

### <a name="import-a-designed-format-configuration"></a><a name="FormatImport"></a><span data-ttu-id="00999-654">設計済みフォーマットの構成をインポートする</span><span class="sxs-lookup"><span data-stu-id="00999-654">Import a designed format configuration</span></span>

1. <span data-ttu-id="00999-655">[アンケート format.version.1.1.xml](https://go.microsoft.com/fwlink/?linkid=851448) ファイルをダウンロードし、ご利用のコンピューターに保存してください。</span><span class="sxs-lookup"><span data-stu-id="00999-655">Download the [Questionnaires format.version.1.1.xml](https://go.microsoft.com/fwlink/?linkid=851448) file, and save it to your local computer.</span></span>
2. <span data-ttu-id="00999-656">**組織管理** \> **ワークスペース** \> **電子申告** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="00999-656">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
3. <span data-ttu-id="00999-657">**電子レポート** ワークスペースで、**レポートの構成** を選択します。</span><span class="sxs-lookup"><span data-stu-id="00999-657">In the **Electronic reporting** workspace, select **Reporting configurations**.</span></span>
4. <span data-ttu-id="00999-658">アクション ペインで、**変換** \> **XML ファイルから読み込む** を選択します。</span><span class="sxs-lookup"><span data-stu-id="00999-658">On the Action pane, Select **Exchange** \> **Load from XML file**.</span></span>
5. <span data-ttu-id="00999-659">**参照** を選択し、**アンケート format.version.1.1.xml** ファイルを検索して、選択します。</span><span class="sxs-lookup"><span data-stu-id="00999-659">Select **Browse**, and then find and select the **Questionnaires format.version.1.1.xml** file.</span></span>
6. <span data-ttu-id="00999-660">**OK** を選択し、構成をインポートします。</span><span class="sxs-lookup"><span data-stu-id="00999-660">Select **OK** to import the configuration.</span></span>

<span data-ttu-id="00999-661">続けるには、次の手順をスキップしてください : [新しいフォーマットの構成を作成する](#FormatCreate)。</span><span class="sxs-lookup"><span data-stu-id="00999-661">To continue, skip the next procedure, [Create a new format configuration](#FormatCreate).</span></span>

### <a name="create-a-new-format-configuration"></a><a name="FormatCreate"></a><span data-ttu-id="00999-662">新しい構成の書式設定の作成</span><span class="sxs-lookup"><span data-stu-id="00999-662">Create a new format configuration</span></span>
 
1. <span data-ttu-id="00999-663">**組織管理** \> **電子申告** \> **構成** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="00999-663">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="00999-664">**構成** ページの、構成ツリーで、**アンケート モデル** を選択します。</span><span class="sxs-lookup"><span data-stu-id="00999-664">On the **Configurations** page, in the configuration tree, select **Questionnaire model**.</span></span>
3. <span data-ttu-id="00999-665">**構成の作成** を選択します。</span><span class="sxs-lookup"><span data-stu-id="00999-665">Select **Create configuration**.</span></span>
4. <span data-ttu-id="00999-666">ドロップダウン ダイアログ ボックスで、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="00999-666">In the drop-down dialog box, follow these steps:</span></span>

    1. <span data-ttu-id="00999-667">**新規** フィールドで、**データ モデル アンケートに基づいたフォーマット** を選択します。</span><span class="sxs-lookup"><span data-stu-id="00999-667">In the **New** field, select **Format based on data model Questionnaires**.</span></span>
    2. <span data-ttu-id="00999-668">**名前** フィールドに、**アンケート レポート** と入力します。</span><span class="sxs-lookup"><span data-stu-id="00999-668">In the **Name** field, enter **Questionnaire report**.</span></span>
    3. <span data-ttu-id="00999-669">**データ モデルのバージョン** フィールドで、**1** を選択します。</span><span class="sxs-lookup"><span data-stu-id="00999-669">In the **Data model version** field, select **1**.</span></span>

        > [!NOTE]
        > - <span data-ttu-id="00999-670">基本データモデルの特定のバージョンを選択すると、対応するバージョンのデータ モデルの構造が、作成されたフォーマットの **モデル** のデータ ソース構造として表示されます。</span><span class="sxs-lookup"><span data-stu-id="00999-670">If you select a specific version of the base data model, the structure of the corresponding version of the data model will be presented to you as the structure of the **Model** data source in the format that is created.</span></span>
        > - <span data-ttu-id="00999-671">このフィールドは必須ではありません。</span><span class="sxs-lookup"><span data-stu-id="00999-671">You can leave this field blank.</span></span> <span data-ttu-id="00999-672">この場合、**下書き** 版のデータ モデルの構造は、作成されたフォーマットの **モデル** のデータソースの構造として表示されます。</span><span class="sxs-lookup"><span data-stu-id="00999-672">In that case, the structure of the **Draft** version of the data model will be presented to you as the structure of the **Model** data source in the format that is created.</span></span> <span data-ttu-id="00999-673">その後、モデルを調整を行って、フォーマットにおける調整結果をすぐに確認することができます。</span><span class="sxs-lookup"><span data-stu-id="00999-673">You can then adjust your model and immediately see those adjustments in your format.</span></span> <span data-ttu-id="00999-674">この方法では、データモデル、モデルマッピング、フォーマットを同時に構成する場合に、ER ソリューション設計の効率を向上させることが期待できます。</span><span class="sxs-lookup"><span data-stu-id="00999-674">This approach might improve the efficiency of ER solution design when you configure your data model, model mapping, and format simultaneously.</span></span>
        > - <span data-ttu-id="00999-675">基本データ モデルの特定のバージョンを選択した場合、フォーマットの編集を開始したときに、後で **下書き** 版を使用するように切り替えることができます。</span><span class="sxs-lookup"><span data-stu-id="00999-675">If you select a specific version of the base data model, you can switch to using the **Draft** version later, when you start to edit a format.</span></span>

    4. <span data-ttu-id="00999-676">**データ モデル定義** フィールドで、**ルート** の定義を選択します。</span><span class="sxs-lookup"><span data-stu-id="00999-676">In the **Data model definition** field, select the **Root** definition.</span></span>

5. <span data-ttu-id="00999-677">**構成を作成する** を選択して、構成を作成します。</span><span class="sxs-lookup"><span data-stu-id="00999-677">Select **Create configuration** to create the configuration.</span></span>

#### <a name="import-a-report-template"></a><a name="ImportReportTemplate"></a><span data-ttu-id="00999-678">レポートのテンプレートをインポートする</span><span class="sxs-lookup"><span data-stu-id="00999-678">Import a report template</span></span>

1. <span data-ttu-id="00999-679">**構成** ページの、構成ツリーで、**アンケート レポート** を選択します。</span><span class="sxs-lookup"><span data-stu-id="00999-679">On the **Configurations** page, in the configuration tree, select **Questionnaire report**.</span></span>
2. <span data-ttu-id="00999-680">**デザイナー** を選択して、カスタム フォーマットの構成を始めます。</span><span class="sxs-lookup"><span data-stu-id="00999-680">Select **Designer** to start to configure a custom format.</span></span>
3. <span data-ttu-id="00999-681">**フォーマット デザイナー** ページの、アクション ペインで、**インポート** \> **Excel からインポートする** を選択します。</span><span class="sxs-lookup"><span data-stu-id="00999-681">On the **Format designer** page, on the Action Pane, select **Import** \> **Import from Excel**.</span></span>
4. <span data-ttu-id="00999-682">ダイアログ ボックスで、次の手順に従ってください :</span><span class="sxs-lookup"><span data-stu-id="00999-682">In the dialog box, follow these steps:</span></span>

    1. <span data-ttu-id="00999-683">**テンプレートの選択** を選択します。</span><span class="sxs-lookup"><span data-stu-id="00999-683">Select **Add template**.</span></span>
    2. <span data-ttu-id="00999-684">ローカルに保存した **アンケート レポート template.xslx** ファイルを検索して選択し、**開く** を選択します。</span><span class="sxs-lookup"><span data-stu-id="00999-684">Find and select the locally saved **Questionnaires report template.xslx** file, and then select **Open**.</span></span>
    3. <span data-ttu-id="00999-685">テンプレートをインポートするには、**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="00999-685">Select **OK** to import the template.</span></span>

    ![レポートのテンプレートをインポートする](./media/er-quick-start1-template-import.png)

<span data-ttu-id="00999-687">**Excel \\ファイル** フォーマットの要素は、自動的にルート要素として編集可能なフォーマットに追加されます。</span><span class="sxs-lookup"><span data-stu-id="00999-687">The **Excel\\File** format element is automatically added to the editable format as a root element.</span></span> <span data-ttu-id="00999-688">さらに、**Excel \\範囲** フォーマットの要素、または **Excel \\セル** フォーマット要素のいずれかが、インポートされたテンプレートの認識された Excel 名ごとに自動的に追加されます。</span><span class="sxs-lookup"><span data-stu-id="00999-688">Additionally, either the **Excel\\Range** format element or the **Excel\\Cell** format element is automatically added for every recognized Excel name of the imported template.</span></span> <span data-ttu-id="00999-689">**Excel\\ヘッダー** フォーマットで、**文字列** 要素がネストされているものは、インポートしたテンプレートのヘッダーの設定を反映して自動的に追加されます。</span><span class="sxs-lookup"><span data-stu-id="00999-689">The **Excel\\Header** format that has the nested **String** element is automatically added to reflect the header settings of the imported template.</span></span>

![ER 工程デザイナーに自動追加された要素を含むフォーマットの構成](./media/er-quick-start1-template-import2.png)

#### <a name="configure-a-format"></a><a name="ConfigureFormat"></a><span data-ttu-id="00999-691">フォーマットを構成する</span><span class="sxs-lookup"><span data-stu-id="00999-691">Configure a format</span></span>

1. <span data-ttu-id="00999-692">フォーマット ツリーの **フォーマット デザイナー** ページで、**Excel** のルート要素を選択します。</span><span class="sxs-lookup"><span data-stu-id="00999-692">On the **Format designer** page, in the format tree, select the **Excel** root element.</span></span>
2. <span data-ttu-id="00999-693">ページ右側の **フォーマット** タブの **名前** フィールドに、 <a name="AddFormatRootElement"></a>**レポート** と入力します。</span><span class="sxs-lookup"><span data-stu-id="00999-693">On the **Format** tab on the right side of the page, in the **Name** field, enter <a name="AddFormatRootElement"></a>**Report**.</span></span>
3. <span data-ttu-id="00999-694">**優先する言語** フィールドで、**ユーザー設定** を選択して、ユーザーの優先する言語でレポートを実行します。</span><span class="sxs-lookup"><span data-stu-id="00999-694">In the **Language preference** field, select **User preference** to run the report in the user's preferred language.</span></span>
4. <span data-ttu-id="00999-695">**優先する文化** フィールドで、**ユーザー設定** を選択して、ユーザーの優先する文化でレポートを実行します。</span><span class="sxs-lookup"><span data-stu-id="00999-695">In the **Culture preference** field, select **User preference** to run the report in the user's preferred culture.</span></span>

    <span data-ttu-id="00999-696">ER プロセスで使用する言語と文化のコンテキストを指定する方法については、[多言語のレポートを設計する](er-design-multilingual-reports.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="00999-696">For information about how to specify the language and culture contexts for an ER process, see [Design multilingual reports](er-design-multilingual-reports.md).</span></span>

    ![ER 操作デザイナーで設計されたレポートの言語と文化の設定を構成する](./media/er-quick-start1-template-format-structure1.png)

5. <span data-ttu-id="00999-698">フォーマット ツリーで、ルート ノードを展開し、続いて **ResultsGroup** を選択します。</span><span class="sxs-lookup"><span data-stu-id="00999-698">In the format tree, expand the root node, and then select **ResultsGroup**.</span></span>
6. <span data-ttu-id="00999-699">**フォーマット** タブの **レプリケーションの方向** フィールドで、**レプリケーションなし** を選択してください。この場合は、1つのアンケートに複数の結果グループが存在することを想定していないためです。</span><span class="sxs-lookup"><span data-stu-id="00999-699">On the **Format** tab, in the **Replication direction** field, select **No replication**, because you don't expect to have multiple result groups for a single questionnaire.</span></span>

    ![ER 操作デザイナーで範囲フォーマット要素のレプリケーション方向を定義する](./media/er-quick-start1-template-format-structure2.png)

7. <span data-ttu-id="00999-701">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="00999-701">Select **Save**.</span></span>

#### <a name="define-the-data-binding-for-a-report-title"></a><a name="DefineFormatBindings"></a><span data-ttu-id="00999-702">レポートのタイトルに使用するデータのバインドを定義する</span><span class="sxs-lookup"><span data-stu-id="00999-702">Define the data binding for a report title</span></span>

<span data-ttu-id="00999-703">生成されたレポートのタイトルの入力に使用するフォーマット要素のデータ バインディングを指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="00999-703">You must specify a data binding for a format element that is used to fill in the title of a generated report.</span></span>

1. <span data-ttu-id="00999-704">**フォーマット デザイナー** ページの、右側の **マッピング** タブ形式で、**レポート\\ReportTitle** 要素を選択します。</span><span class="sxs-lookup"><span data-stu-id="00999-704">On the **Format designer** page, on the **Mapping** tab on the right, select the **Report\\ReportTitle** element.</span></span>
2. <span data-ttu-id="00999-705">**式の編集** を選択します。</span><span class="sxs-lookup"><span data-stu-id="00999-705">Select **Edit formula**.</span></span>
3. <span data-ttu-id="00999-706">式エディターで、**翻訳** を選択します。</span><span class="sxs-lookup"><span data-stu-id="00999-706">In the formula editor, select **Translate**.</span></span>
4. <span data-ttu-id="00999-707">**テキストの翻訳** ダイアログ ボックスで、次の手順に従ってください :</span><span class="sxs-lookup"><span data-stu-id="00999-707">In the **Text translation** dialog box, follow these steps:</span></span>

    1. <span data-ttu-id="00999-708">**ラベル ID** フィールドで、**ReportTitle** と入力します。</span><span class="sxs-lookup"><span data-stu-id="00999-708">In the **Label ID** field, enter **ReportTitle**.</span></span>
    2. <span data-ttu-id="00999-709">**既定の言語のテキスト** フィールドに **アンケート レポート** と入力します。</span><span class="sxs-lookup"><span data-stu-id="00999-709">In the **Text in default language** field, enter **Questionnaires report**.</span></span>
    3. <span data-ttu-id="00999-710">**翻訳** を選択してから、**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="00999-710">Select **Translate**, and then select **Save**.</span></span>
    4. <span data-ttu-id="00999-711">**翻訳** を選択して、**テキストの翻訳** ダイアログ ボックスを閉じます。</span><span class="sxs-lookup"><span data-stu-id="00999-711">Select **Translate** to close the **Text translation** dialog box.</span></span>

5. <span data-ttu-id="00999-712">式エディターを閉じます。</span><span class="sxs-lookup"><span data-stu-id="00999-712">Close the formula editor.</span></span>

    ![バインドを構成して生成されたレポートのタイトルを入力する](./media/er-quick-start1-add-report-title-label.png)

<span data-ttu-id="00999-714">この手法を使用して、現在のテンプレートの他のすべてのラベルを言語依存にすることができます。</span><span class="sxs-lookup"><span data-stu-id="00999-714">You can use this technique to make all other labels of the current template language-dependent.</span></span> <span data-ttu-id="00999-715">1つの ER 構成の追加ラベルを対応しているすべての言語に翻訳する方法については、[多言語のレポートを設計する](er-design-multilingual-reports.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="00999-715">For information about how the added labels of a single ER configuration can be translated into all supported languages, see [Design multilingual reports](er-design-multilingual-reports.md).</span></span>

#### <a name="review-model-data-source"></a><a name="ReviewModelDataSource"></a><span data-ttu-id="00999-716">モデル データ ソースをレビューする</span><span class="sxs-lookup"><span data-stu-id="00999-716">Review model data source</span></span>

1. <span data-ttu-id="00999-717">**フォーマット デザイナー** ページの **マッピング** タブで、<a name="ModelDSName"></a>この ER フォーマットの基本データ モデルを表す **モデル** データ ソースを選択します。</span><span class="sxs-lookup"><span data-stu-id="00999-717">On the **Format designer** page, on the **Mapping** tab, select the <a name="ModelDSName"></a>**model** data source that represents the base data model of this ER format.</span></span>
2. <span data-ttu-id="00999-718">**編集** を選択します。</span><span class="sxs-lookup"><span data-stu-id="00999-718">Select **Edit**.</span></span>
3. <span data-ttu-id="00999-719">**データ ソース プロパティ** ダイアログ ボックスの情報をを確認します。</span><span class="sxs-lookup"><span data-stu-id="00999-719">Review the information in the **Data source properties** dialog box.</span></span> <span data-ttu-id="00999-720">このデータソースは、**アンケート** モデルの ER 構成に存在する **アンケート** データ モデル コンポーネントのバージョン 1 を表しています。</span><span class="sxs-lookup"><span data-stu-id="00999-720">This data source represents version 1 of the **Questionnaires** data model component that resides in the **Questionnaires model** ER configuration.</span></span>

![ER 操作デザイナー モデルデータ ソースのプロパティ](./media/er-quick-start1-model-data-source.png)

#### <a name="bind-format-elements-to-data-source-fields"></a><a name="BindFormatElements"></a><span data-ttu-id="00999-722">フォーマットの要素をデータ ソース フィールドにバインドする</span><span class="sxs-lookup"><span data-stu-id="00999-722">Bind format elements to data source fields</span></span>

<span data-ttu-id="00999-723">実行時のテンプレートへの入力方法を指定するには、適切な Excel 名に関連付けられたすべてのフォーマット要素を、このフォーマットのデータソースの 1 つのフィールドにバインドする必要があります。</span><span class="sxs-lookup"><span data-stu-id="00999-723">To specify how a template is filled in at runtime, you must bind every format element that is associated with an appropriate Excel name to a single field of this format's data source.</span></span>

1. <span data-ttu-id="00999-724">フォーマット ツリーの **フォーマット デザイナー**  ページで、**レポート\\CompanyName** フォーマット要素を選択します。</span><span class="sxs-lookup"><span data-stu-id="00999-724">On the **Format designer** page, in the format tree, select the **Report\\CompanyName** format element.</span></span>
2. <span data-ttu-id="00999-725">**マッピング** タブで、**文字列** 型のデータ ソース フィールド **model.CompanyName** を選択します。</span><span class="sxs-lookup"><span data-stu-id="00999-725">On the **Mapping** tab, select the **model.CompanyName** data source field of the **String** type.</span></span>
3. <span data-ttu-id="00999-726">**バインド** を選択して、テンプレートに会社名を入力します。</span><span class="sxs-lookup"><span data-stu-id="00999-726">Select **Bind** to enter a company name in a template.</span></span>
4. <span data-ttu-id="00999-727">フォーマット ツリーで、**レポート\\アンケート** 要素を選択し ます。</span><span class="sxs-lookup"><span data-stu-id="00999-727">In the format tree, select the **Report\\Questionnaire** element.</span></span>
5. <span data-ttu-id="00999-728">**マッピング** タブで、**レコード リスト** 型のデータ ソース フィールド **model.Questionnaire** を選択します。</span><span class="sxs-lookup"><span data-stu-id="00999-728">On the **Mapping** tab, select the **model.Questionnaire** data source field of the **Record list** type.</span></span>
6. <span data-ttu-id="00999-729">**バインド** を選択します。</span><span class="sxs-lookup"><span data-stu-id="00999-729">Select **Bind**.</span></span>
7. <span data-ttu-id="00999-730">**詳細の表示** を選択して、フォーマット要素の詳細を表示します。</span><span class="sxs-lookup"><span data-stu-id="00999-730">Select **Show details** to see more details for format elements.</span></span>

    <span data-ttu-id="00999-731">**アンケート** 範囲フォーマット要素は、垂直方向に複製されるように構成されています。</span><span class="sxs-lookup"><span data-stu-id="00999-731">The **Questionnaire** range format element is configured as vertically replicated.</span></span> <span data-ttu-id="00999-732">**レコード リスト** 型のデータソースにバインドすると、Excel テンプレートの適切な **アンケート** の範囲が、バインドされたデータソースのすべてのレコードに対して繰り返されます。</span><span class="sxs-lookup"><span data-stu-id="00999-732">When it's bound to a data source of the **Record list** type, the appropriate **Questionnaire** range of the Excel template is repeated for every record of the bound data source.</span></span>
 
    ![ER 操作デザイナーの適切なレコード リストのデータ ソースにアンケート範囲のフォーマット要素をバインドする](./media/er-quick-start1-bindings1.png)

    <span data-ttu-id="00999-734">Excel テンプレートの **アンケート** 範囲は 5 から 14 行目までの間の定義されているため、これらの行は提出されたアンケートごとに繰り返されます。</span><span class="sxs-lookup"><span data-stu-id="00999-734">Because the **Questionnaire** range of the Excel template is defined between rows 5 through 14, these rows are repeated for every reported questionnaire.</span></span>

    ![レコード リストのデータ ソースの各レコードに対して、生成されたレポートで繰り返される Excel テンプレートの行](./media/er-quick-start1-template-questionnaire-range.png)

8. <span data-ttu-id="00999-736">以下の表に示すように、残りのフォーマット要素にも同様のバインディングを設定してください。</span><span class="sxs-lookup"><span data-stu-id="00999-736">Configure similar bindings for the remaining format elements, as described in the following table.</span></span>

    > [!NOTE]
    > <span data-ttu-id="00999-737">この表では、「データソースパス」欄の情報は、 ER 機能 [相対パス](relative-path-data-bindings-er-models-format.md)がオンになっていることを前提としています。</span><span class="sxs-lookup"><span data-stu-id="00999-737">In this table, the information in the "Data source path" column assumes that the [relative path](relative-path-data-bindings-er-models-format.md) ER feature is turned on.</span></span>

    | <span data-ttu-id="00999-738">フォーマット要素のパス</span><span class="sxs-lookup"><span data-stu-id="00999-738">Format element path</span></span>                                      | <span data-ttu-id="00999-739">データ ソースのパス</span><span class="sxs-lookup"><span data-stu-id="00999-739">Data source path</span></span> |
    |----------------------------------------------------------|------------------|
    | <span data-ttu-id="00999-740">Excel\\ReportTitle</span><span class="sxs-lookup"><span data-stu-id="00999-740">Excel\\ReportTitle</span></span>                                       | <span data-ttu-id="00999-741">**\@"GER\_LABEL:ReportTitle"**</span><span class="sxs-lookup"><span data-stu-id="00999-741">**\@"GER\_LABEL:ReportTitle"**</span></span> |
    | <span data-ttu-id="00999-742">Excel\\CompanyName</span><span class="sxs-lookup"><span data-stu-id="00999-742">Excel\\CompanyName</span></span>                                       | <span data-ttu-id="00999-743">**model.CompanyName**</span><span class="sxs-lookup"><span data-stu-id="00999-743">**model.CompanyName**</span></span> |
    | <span data-ttu-id="00999-744">Excel\\Questionnaire</span><span class="sxs-lookup"><span data-stu-id="00999-744">Excel\\Questionnaire</span></span>                                     | <span data-ttu-id="00999-745">**model.Questionnaire**</span><span class="sxs-lookup"><span data-stu-id="00999-745">**model.Questionnaire**</span></span> |
    | <span data-ttu-id="00999-746">Excel\\Questionnaire\\Active</span><span class="sxs-lookup"><span data-stu-id="00999-746">Excel\\Questionnaire\\Active</span></span>                             | <span data-ttu-id="00999-747">**\@.Active**、**\@** が **model.Questionnaire** の場合</span><span class="sxs-lookup"><span data-stu-id="00999-747">**\@.Active**, where **\@** is **model.Questionnaire**</span></span> |
    | <span data-ttu-id="00999-748">Excel\\Questionnaire\\Code</span><span class="sxs-lookup"><span data-stu-id="00999-748">Excel\\Questionnaire\\Code</span></span>                               | <span data-ttu-id="00999-749">**\@.Code**</span><span class="sxs-lookup"><span data-stu-id="00999-749">**\@.Code**</span></span> |
    | <span data-ttu-id="00999-750">Excel\\Questionnaire\\Description</span><span class="sxs-lookup"><span data-stu-id="00999-750">Excel\\Questionnaire\\Description</span></span>                        | <span data-ttu-id="00999-751">**\@.Description**</span><span class="sxs-lookup"><span data-stu-id="00999-751">**\@.Description**</span></span> |
    | <span data-ttu-id="00999-752">Excel\\Questionnaire\\QuestionnaireType</span><span class="sxs-lookup"><span data-stu-id="00999-752">Excel\\Questionnaire\\QuestionnaireType</span></span>                  | <span data-ttu-id="00999-753">**\@.QuestionnaireType**</span><span class="sxs-lookup"><span data-stu-id="00999-753">**\@.QuestionnaireType**</span></span> |
    | <span data-ttu-id="00999-754">Excel\\Questionnaire\\QuestionOrder</span><span class="sxs-lookup"><span data-stu-id="00999-754">Excel\\Questionnaire\\QuestionOrder</span></span>                      | <span data-ttu-id="00999-755">**\@.QuestionOrder**</span><span class="sxs-lookup"><span data-stu-id="00999-755">**\@.QuestionOrder**</span></span> |
    | <span data-ttu-id="00999-756">Excel\\Questionnaire\\ResultsGroup\\Code\_</span><span class="sxs-lookup"><span data-stu-id="00999-756">Excel\\Questionnaire\\ResultsGroup\\Code\_</span></span>               | <span data-ttu-id="00999-757">**\@.ResultsGroup.Code**</span><span class="sxs-lookup"><span data-stu-id="00999-757">**\@.ResultsGroup.Code**</span></span> |
    | <span data-ttu-id="00999-758">Excel\\Questionnaire\\ResultsGroup\\Description\_</span><span class="sxs-lookup"><span data-stu-id="00999-758">Excel\\Questionnaire\\ResultsGroup\\Description\_</span></span>        | <span data-ttu-id="00999-759">**\@.ResultsGroup.Description**</span><span class="sxs-lookup"><span data-stu-id="00999-759">**\@.ResultsGroup.Description**</span></span> |
    | <span data-ttu-id="00999-760">Excel\\Questionnaire\\ResultsGroup\\MaxNumberOfPoints</span><span class="sxs-lookup"><span data-stu-id="00999-760">Excel\\Questionnaire\\ResultsGroup\\MaxNumberOfPoints</span></span>    | <span data-ttu-id="00999-761">**\@.ResultsGroup.MaxNumberOfPoint**</span><span class="sxs-lookup"><span data-stu-id="00999-761">**\@.ResultsGroup.MaxNumberOfPoint**</span></span> |
    | <span data-ttu-id="00999-762">Excel\\Questionnaire\\Question</span><span class="sxs-lookup"><span data-stu-id="00999-762">Excel\\Questionnaire\\Question</span></span>                           | <span data-ttu-id="00999-763">**\@.Question**</span><span class="sxs-lookup"><span data-stu-id="00999-763">**\@.Question**</span></span> |
    | <span data-ttu-id="00999-764">Excel\\Questionnaire\\Question\\CollectionSequenceNumber</span><span class="sxs-lookup"><span data-stu-id="00999-764">Excel\\Questionnaire\\Question\\CollectionSequenceNumber</span></span> | <span data-ttu-id="00999-765">**\@.CollectionSequenceNumber**、 **\@** が **model.Questionnaire.Question** の場合</span><span class="sxs-lookup"><span data-stu-id="00999-765">**\@.CollectionSequenceNumber**, where **\@** is **model.Questionnaire.Question**</span></span> |
    | <span data-ttu-id="00999-766">Excel\\Questionnaire\\Question\\Id</span><span class="sxs-lookup"><span data-stu-id="00999-766">Excel\\Questionnaire\\Question\\Id</span></span>                       | <span data-ttu-id="00999-767">**\@.Id**</span><span class="sxs-lookup"><span data-stu-id="00999-767">**\@.Id**</span></span> |
    | <span data-ttu-id="00999-768">Excel\\Questionnaire\\Question\\MustBeCompleted</span><span class="sxs-lookup"><span data-stu-id="00999-768">Excel\\Questionnaire\\Question\\MustBeCompleted</span></span>          | <span data-ttu-id="00999-769">**\@.MustBeCompleted**</span><span class="sxs-lookup"><span data-stu-id="00999-769">**\@.MustBeCompleted**</span></span> |
    | <span data-ttu-id="00999-770">Excel\\Questionnaire\\Question\\PrimaryQuestion</span><span class="sxs-lookup"><span data-stu-id="00999-770">Excel\\Questionnaire\\Question\\PrimaryQuestion</span></span>          | <span data-ttu-id="00999-771">**\@.PrimaryQuestion**</span><span class="sxs-lookup"><span data-stu-id="00999-771">**\@.PrimaryQuestion**</span></span> |
    | <span data-ttu-id="00999-772">Excel\\Questionnaire\\Question\\SequenceNumber</span><span class="sxs-lookup"><span data-stu-id="00999-772">Excel\\Questionnaire\\Question\\SequenceNumber</span></span>           | <span data-ttu-id="00999-773">**\@.SequenceNumber**</span><span class="sxs-lookup"><span data-stu-id="00999-773">**\@.SequenceNumber**</span></span> |
    | <span data-ttu-id="00999-774">Excel\\Questionnaire\\Question\\Text</span><span class="sxs-lookup"><span data-stu-id="00999-774">Excel\\Questionnaire\\Question\\Text</span></span>                     | <span data-ttu-id="00999-775">**\@.Text**</span><span class="sxs-lookup"><span data-stu-id="00999-775">**\@.Text**</span></span> |
    | <span data-ttu-id="00999-776">Excel\\Questionnaire\\Question\\Answer</span><span class="sxs-lookup"><span data-stu-id="00999-776">Excel\\Questionnaire\\Question\\Answer</span></span>                   | <span data-ttu-id="00999-777">**\@.Answer**</span><span class="sxs-lookup"><span data-stu-id="00999-777">**\@.Answer**</span></span> |
    | <span data-ttu-id="00999-778">Excel\\Questionnaire\\Question\\Answer\\CorrectAnswer</span><span class="sxs-lookup"><span data-stu-id="00999-778">Excel\\Questionnaire\\Question\\Answer\\CorrectAnswer</span></span>    | <span data-ttu-id="00999-779">**\@.CorrectAnswer** **\@** が **model.Questionnaire.Answer** の場合</span><span class="sxs-lookup"><span data-stu-id="00999-779">**\@.CorrectAnswer**, where **\@** is **model.Questionnaire.Answer**</span></span> |
    | <span data-ttu-id="00999-780">Excel\\Questionnaire\\Question\\Answer\\Points</span><span class="sxs-lookup"><span data-stu-id="00999-780">Excel\\Questionnaire\\Question\\Answer\\Points</span></span>           | <span data-ttu-id="00999-781">**\@.Points**</span><span class="sxs-lookup"><span data-stu-id="00999-781">**\@.Points**</span></span> |
    | <span data-ttu-id="00999-782">Excel\\Questionnaire\\Question\\Answer\\Text</span><span class="sxs-lookup"><span data-stu-id="00999-782">Excel\\Questionnaire\\Question\\Answer\\Text</span></span>             | <span data-ttu-id="00999-783">**\@.Text**</span><span class="sxs-lookup"><span data-stu-id="00999-783">**\@.Text**</span></span> |

9. <span data-ttu-id="00999-784">完了したら、**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="00999-784">When you've finished, select **Save**.</span></span>

<span data-ttu-id="00999-785">以下の画面は、**フォーマット デザイナー** ページ上で構成されたデータ バインディングの最終的な状態を示して います。</span><span class="sxs-lookup"><span data-stu-id="00999-785">The following illustration shows the final state of the configured data bindings on the **Format designer** page.</span></span>

![ER 操作デザイナーで構成されたデータ バインディング](./media/er-quick-start1-bindings2.png)

> [!IMPORTANT]
> <span data-ttu-id="00999-787">指定されたデータソースとバインディングの全体のコレクションは、構成されたフォーマットのフォーマット マッピング コンポーネントを表します。</span><span class="sxs-lookup"><span data-stu-id="00999-787">The whole collection of specified data sources and bindings represents a format mapping component of the configured format.</span></span> <span data-ttu-id="00999-788">このフォーマット マッピングは、レポート生成に向けて構成されたフォーマットを実行する際に呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="00999-788">This format mapping is called when you run the configured format for report generation.</span></span>

### <a name="run-a-designed-format-from-er"></a><a name="RunFormatFromER"></a><span data-ttu-id="00999-789">ER から設計済みのフォーマットを実行する</span><span class="sxs-lookup"><span data-stu-id="00999-789">Run a designed format from ER</span></span>

<span data-ttu-id="00999-790">**構成** ページから、テスト用にデザインされた形式を実行できます。</span><span class="sxs-lookup"><span data-stu-id="00999-790">You can now run a designed format for testing purposes from the **Configurations** page.</span></span>

1. <span data-ttu-id="00999-791">**組織管理** \> **電子申告** \> **構成** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="00999-791">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="00999-792">**構成** ページの構成ツリーで、**アンケート モデル** を展開し、**アンケート レポート** を選択します。</span><span class="sxs-lookup"><span data-stu-id="00999-792">On the **Configuration** page, in the configuration tree, expand **Questionnaire model**, and then select **Questionnaire report**.</span></span>
3. <span data-ttu-id="00999-793">**下書き** 状態のフォーマット バージョンの **デザイナー** を選択します。</span><span class="sxs-lookup"><span data-stu-id="00999-793">Select **Designer** for the format version that has a status of **Draft**.</span></span>
4. <span data-ttu-id="00999-794">**フォーマット デザイナー** ページで、**実行** を選択します。</span><span class="sxs-lookup"><span data-stu-id="00999-794">On the **Format designer** page, select **Run**.</span></span>
5. <span data-ttu-id="00999-795">**ER パラメーター** ダイアログ ボックスの **含めるレコード** クイックタブに、**sbccrsexam** アンケートのみが含まれるようにフィルター処理オプションを構成します。</span><span class="sxs-lookup"><span data-stu-id="00999-795">In the **ER parameters** dialog box, on the **Records to include** FastTab, configure the filtering option so that only the **SBCCrsExam** questionnaire is included.</span></span>
6. <span data-ttu-id="00999-796">**OK** を選択してオプションを確認します。</span><span class="sxs-lookup"><span data-stu-id="00999-796">Select **OK** to confirm the filtering option.</span></span>
7. <span data-ttu-id="00999-797">**OK** を選択してレポートを実行します。</span><span class="sxs-lookup"><span data-stu-id="00999-797">Select **OK** to run the report.</span></span>
8. <span data-ttu-id="00999-798">生成されたレポートを確認します。</span><span class="sxs-lookup"><span data-stu-id="00999-798">Review the generated report.</span></span>

<span data-ttu-id="00999-799">[既定](electronic-reporting-destinations.md#default-behavior)では、生成されたレポートは、ダウンロード可能な Excel ファイル形式で配信されます。</span><span class="sxs-lookup"><span data-stu-id="00999-799">By [default](electronic-reporting-destinations.md#default-behavior), a generated report is delivered as an Excel file that you can download.</span></span> <span data-ttu-id="00999-800">次の図は、生成されたレポートの2つのページを Excel 形式で示しています。</span><span class="sxs-lookup"><span data-stu-id="00999-800">The following illustrations show two pages of the generated report in Excel format.</span></span>

![Excel フォーマットで生成されたレポートの例 (ページ1)](./media/er-quick-start1-report1a.png)

![Excel フォーマットで生成されたレポートの例 (ページ2)](./media/er-quick-start1-report1b.png)

## <a name="tune-a-designed-format"></a><a name="TuneFormat"></a><span data-ttu-id="00999-803">設計済みのフォーマットを調整する</span><span class="sxs-lookup"><span data-stu-id="00999-803">Tune a designed format</span></span>

### <a name="modify-a-format-to-change-the-name-of-a-generated-document"></a><a name="ModifyToChangeName"></a><span data-ttu-id="00999-804">フォーマットを修正して生成されたドキュメントの名前を変更する</span><span class="sxs-lookup"><span data-stu-id="00999-804">Modify a format to change the name of a generated document</span></span>

<span data-ttu-id="00999-805">既定では、生成されたドキュメントには現在のユーザーのエイリアスを使用して名前が付けられます。</span><span class="sxs-lookup"><span data-stu-id="00999-805">By default, a generated document is named by using the alias of the current user.</span></span> <span data-ttu-id="00999-806">フォーマットを変更することで、この動作を変更して、生成されたドキュメントにカスタム ロジックに基づいて名前を付けることができます。</span><span class="sxs-lookup"><span data-stu-id="00999-806">By modifying the format, you can change this behavior so that a generated document is named based on your custom logic.</span></span> <span data-ttu-id="00999-807">たとえば、生成されたドキュメントの名前は、現在のセッションの日時とレポートのタイトルに基づいて付けることができます。</span><span class="sxs-lookup"><span data-stu-id="00999-807">For example, the name of a generated document can be based on the current session date and time, and on the report's title.</span></span>

1. <span data-ttu-id="00999-808">**フォーマット デザイナー** ページで、ルート項目 **レポート** を選択します。</span><span class="sxs-lookup"><span data-stu-id="00999-808">On the **Format designer** page, select the **Report** root item.</span></span>
2. <span data-ttu-id="00999-809">**マッピング** タブで、**ファイル名の編集** を選択します。</span><span class="sxs-lookup"><span data-stu-id="00999-809">On the **Mapping** tab, select **Edit file name**.</span></span>
3. <span data-ttu-id="00999-810">**式** フィールドに、**CONCATENATE (\@"GER\_LABEL:ReportTitle", " - ", DATETIMEFORMAT(SESSIONNOW(), "yyyy-MM-dd hh-mm-ss"))** と入力します。</span><span class="sxs-lookup"><span data-stu-id="00999-810">In the **Formula** field, enter **CONCATENATE (\@"GER\_LABEL:ReportTitle", " - ", DATETIMEFORMAT(SESSIONNOW(), "yyyy-MM-dd hh-mm-ss"))**.</span></span>
4. <span data-ttu-id="00999-811">**保存** を選択し、式エディターを閉じます。</span><span class="sxs-lookup"><span data-stu-id="00999-811">Select **Save**, and close the formula editor.</span></span>
5. <span data-ttu-id="00999-812">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="00999-812">Select **Save**.</span></span>

### <a name="modify-a-format-to-change-the-order-of-questions"></a><a name="ModifyToOrder"></a><span data-ttu-id="00999-813">フォーマットを修正して質問の表示順を変更する</span><span class="sxs-lookup"><span data-stu-id="00999-813">Modify a format to change the order of questions</span></span>

<span data-ttu-id="00999-814">生成されたレポートでは、質問は正しく順序付けられていません。</span><span class="sxs-lookup"><span data-stu-id="00999-814">The questions aren't correctly ordered in a generated report.</span></span> <span data-ttu-id="00999-815">フォーマットを変更することで順番を変更することができます。</span><span class="sxs-lookup"><span data-stu-id="00999-815">You can change the order by modifying the format.</span></span>

1. <span data-ttu-id="00999-816">**フォーマット デザイナー** ページで、ルート項目 **レポート** を選択します。</span><span class="sxs-lookup"><span data-stu-id="00999-816">On the **Format designer** page, select the **Report** root item.</span></span>
2. <span data-ttu-id="00999-817">**マッピング** タブのフォーマット ツリーで、**レポート\\アンケート\\質問** を展開します。</span><span class="sxs-lookup"><span data-stu-id="00999-817">On the **Mapping** tab, in the format tree, expand **Report\\Questionnaire\\Question**.</span></span>

    ![ER 作業工程デザイナーにおける範囲タイプの質問フォーマット要素](./media/er-quick-start1-bindings3.png)

3. <span data-ttu-id="00999-819">**マッピング** タブで、**model.Questionnaire** を選択します。</span><span class="sxs-lookup"><span data-stu-id="00999-819">On the **Mapping** tab, select **model.Questionnaire**.</span></span>
4. <span data-ttu-id="00999-820">**追加**\>**関数\\計算フィールド** を選択し、**Name** フィールドに **OrderedQuestions** と入力します。</span><span class="sxs-lookup"><span data-stu-id="00999-820">Select **Add** \> **Functions\\Calculated field**, and then, in the **Name** field, enter **OrderedQuestions**.</span></span>
5. <span data-ttu-id="00999-821">**式の編集** を選択します。</span><span class="sxs-lookup"><span data-stu-id="00999-821">Select **Edit formula**.</span></span>
6. <span data-ttu-id="00999-822">式の編集エディターの **式** フィールドに **ORDERBY (model.Questionnaire.Question, model.Questionnaire.Question.SequenceNumber)** を入力し、現在のアンケートの質問のリストをシーケンス オーダー番号順に並び替えます。</span><span class="sxs-lookup"><span data-stu-id="00999-822">In the formula editor, in the **Formula** field, enter **ORDERBY (model.Questionnaire.Question, model.Questionnaire.Question.SequenceNumber)** to order the list of questions of the current questionnaire by the sequence order number.</span></span>
7. <span data-ttu-id="00999-823">**保存** を選択し、式エディターを閉じます。</span><span class="sxs-lookup"><span data-stu-id="00999-823">Select **Save**, and close the formula editor.</span></span>
8. <span data-ttu-id="00999-824">**OK** をクリックして、新しい計算フィールドの入力を完了します。</span><span class="sxs-lookup"><span data-stu-id="00999-824">Select **OK** to complete the entry of a new calculated field.</span></span>
9. <span data-ttu-id="00999-825">**マッピング** タブで、**model.Questionnaire.OrderedQuestions** を選択します。</span><span class="sxs-lookup"><span data-stu-id="00999-825">On the **Mapping** tab, select **model.Questionnaire.OrderedQuestions**.</span></span>
10. <span data-ttu-id="00999-826">フォーマットのツリーで、**Excel\\アンケート\\質問** を選択します。</span><span class="sxs-lookup"><span data-stu-id="00999-826">In the format tree, select **Excel\\Questionnaire\\Question**.</span></span>
11. <span data-ttu-id="00999-827">**Bind** を選択し、 入れ子になった要素のすべてのバインディングで、現在の **model.Questionnaire.Questions** パスが新しい **model.Questionnaire.OrderedQuestions** パスに置き換えられていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="00999-827">Select **Bind**, and then confirm that the current **model.Questionnaire.Questions** path is replaced by the new **model.Questionnaire.OrderedQuestions** path in all bindings of nested elements.</span></span>
12. <span data-ttu-id="00999-828">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="00999-828">Select **Save**.</span></span>

![ER 操作デザイナーで、構成された OrderedQuestions データソースに アンケート フォーマット要素をバインドする](./media/er-quick-start1-bindings4.png)

### <a name="run-a-modified-format-from-er"></a><a name="RunFormatFromER2"></a><span data-ttu-id="00999-830">ER から修正済みのフォーマットを実行する</span><span class="sxs-lookup"><span data-stu-id="00999-830">Run a modified format from ER</span></span>

<span data-ttu-id="00999-831">ER フレームワークから、テスト用に変更されたフィーマットを実行できます。</span><span class="sxs-lookup"><span data-stu-id="00999-831">You can now run a modified format for testing purposes from the ER framework.</span></span>

1. <span data-ttu-id="00999-832">**フォーマット デザイナー** ページで、**実行** を選択します。</span><span class="sxs-lookup"><span data-stu-id="00999-832">On the **Format designer** page, select **Run**.</span></span>
2. <span data-ttu-id="00999-833">**ER パラメーター** ダイアログ ボックスの **含めるレコード** クイックタブに、**sbccrsexam** アンケートのみが含まれるようにフィルター処理オプションを構成します。</span><span class="sxs-lookup"><span data-stu-id="00999-833">In the **ER parameters** dialog box, on the **Records to include** FastTab, configure the filtering option so that only the **SBCCrsExam** questionnaire is included.</span></span>
3. <span data-ttu-id="00999-834">**OK** を選択してオプションを確認します。</span><span class="sxs-lookup"><span data-stu-id="00999-834">Select **OK** to confirm the filtering option.</span></span>
4. <span data-ttu-id="00999-835">**OK** を選択してレポートを実行します。</span><span class="sxs-lookup"><span data-stu-id="00999-835">Select **OK** to run the report.</span></span>
5. <span data-ttu-id="00999-836">生成されたレポートを確認します。</span><span class="sxs-lookup"><span data-stu-id="00999-836">Review the generated report.</span></span>

<span data-ttu-id="00999-837">次の図は、質問が正しい順番に並べられた Excel 形式の生成レポートを示しています。</span><span class="sxs-lookup"><span data-stu-id="00999-837">The following illustration shows a generated report in Excel format where the questions are correctly ordered.</span></span>

![質問を正しく並べ替えた Excel 形式のレポートを生成する](./media/er-quick-start1-report2.png)

### <a name="complete-the-format-design"></a><a name="CompleteFormat"></a><span data-ttu-id="00999-839">フォーマットの設計を完了する</span><span class="sxs-lookup"><span data-stu-id="00999-839">Complete the format design</span></span>

1. <span data-ttu-id="00999-840">**組織管理** \> **電子申告** \> **構成** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="00999-840">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="00999-841">**構成** ページの構成ツリーで、**アンケート モデル** を展開し、**アンケート レポート** を選択します。</span><span class="sxs-lookup"><span data-stu-id="00999-841">On the **Configurations** page, in the configuration tree, expand **Questionnaire model**, and then select **Questionnaire report**.</span></span>
3. <span data-ttu-id="00999-842">**バージョン** クイック タブで、状態が **下書き** となっている構成のバージョンを選択します。</span><span class="sxs-lookup"><span data-stu-id="00999-842">On the **Versions** FastTab, select the configuration version that has a status of **Draft**.</span></span>
4. <span data-ttu-id="00999-843">**ステータスの変更** \> **完了** を選択します。</span><span class="sxs-lookup"><span data-stu-id="00999-843">Select **Change status** \> **Complete**.</span></span>

<span data-ttu-id="00999-844">この構成のバージョン 1.1 の状態 **下書き** から **完了** に変更されます。</span><span class="sxs-lookup"><span data-stu-id="00999-844">The status of version 1.1 of this configuration is changed from **Draft** to **Completed**.</span></span> <span data-ttu-id="00999-845">バージョン 1.1 を変更することはできなくなります。</span><span class="sxs-lookup"><span data-stu-id="00999-845">Version 1.1 can no longer be changed.</span></span> <span data-ttu-id="00999-846">このバージョンには、構成済のフォーマットが含まれており、カスタム レポートの印刷に使用できます。</span><span class="sxs-lookup"><span data-stu-id="00999-846">This version contains the configured format and can be used to print your custom report.</span></span> <span data-ttu-id="00999-847">この構成のバージョン 1.2 が作成され、状態が **下書き** になります。</span><span class="sxs-lookup"><span data-stu-id="00999-847">Version 1.2 of this configuration is created and has a status of **Draft**.</span></span> <span data-ttu-id="00999-848">このバージョンを編集して、**アンケート** レポートのフォーマットを調整することができます。</span><span class="sxs-lookup"><span data-stu-id="00999-848">You can edit this version to adjust the format of your **Questionnaire** report.</span></span>

![[構成] ページの編集可能な ER 構成のバージョン](./media/er-quick-start1-format-configuration.png)

> [!NOTE]
> <span data-ttu-id="00999-850">構成されたフォーマットは、**アンケート** レポートのデザインであり、財務固有のアーティファクトとの関係はありません。</span><span class="sxs-lookup"><span data-stu-id="00999-850">The configured format is your design of the **Questionnaire** report and contains no relations to the Finance-specific artefacts.</span></span>

## <a name="develop-application-artefacts-to-call-the-designed-report"></a><a name="DevelopCustomCode"></a><span data-ttu-id="00999-851">アプリケーション アーティファクトを開発して、設計済みのレポートを呼び出す</span><span class="sxs-lookup"><span data-stu-id="00999-851">Develop application artefacts to call the designed report</span></span>

<span data-ttu-id="00999-852">システム管理者ロールが付与されたユーザーは、設定された ER フォーマットをアプリケーション ユーザー インターフェース (UI) から呼び出してカスタム レポートを生成できるように、新しいロジックを開発する必要があります。</span><span class="sxs-lookup"><span data-stu-id="00999-852">As a user in the System Administrator role, you must develop new logic so that the configured ER format can be called from the application user interface (UI) to generate your custom report.</span></span> <span data-ttu-id="00999-853">現在 ER には、この種のロジックを構成する機能はありません。</span><span class="sxs-lookup"><span data-stu-id="00999-853">Currently, ER doesn't offer any capability for configuring this type of logic.</span></span> <span data-ttu-id="00999-854">そのため、多少の技術的な作業が必要となります。</span><span class="sxs-lookup"><span data-stu-id="00999-854">Therefore, some engineering work is required.</span></span> 

<span data-ttu-id="00999-855">新しいロジックを開発するには、継続的なビルドに対応したトポロジをデプロイする必要があります。</span><span class="sxs-lookup"><span data-stu-id="00999-855">To develop the new logic, you must deploy a topology that supports continuous build.</span></span> <span data-ttu-id="00999-856">詳細については、[継続的ビルドとテストの自動化をサポートするトポロジの配置](../perf-test/continuous-build-test-automation.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="00999-856">For more information, see [Deploy topologies that support continuous build and test automation](../perf-test/continuous-build-test-automation.md).</span></span> <span data-ttu-id="00999-857">また、このトポロジの開発環境にもアクセスできる必要があります。</span><span class="sxs-lookup"><span data-stu-id="00999-857">You must also have access to the development environment for this topology.</span></span> <span data-ttu-id="00999-858">利用可能な ER の API については、[ER フレームワークの API](er-apis-app73.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="00999-858">For more information about the available ER API, see [ER framework API](er-apis-app73.md).</span></span>

### <a name="modify-source-code"></a><a name="ModifySourceCode"></a><span data-ttu-id="00999-859">ソース コードの修正</span><span class="sxs-lookup"><span data-stu-id="00999-859">Modify source code</span></span>

#### <a name="add-a-data-contract-class"></a><a name="DataContractClass"></a><span data-ttu-id="00999-860">データ コントラクトのクラスを追加する</span><span class="sxs-lookup"><span data-stu-id="00999-860">Add a data contract class</span></span>

<span data-ttu-id="00999-861">新しい **QuestionnairesErReportContract** クラスを Visual Studio プロジェクトに追加し、構成された ER フォーマットの実行に使用するデータ コントラクトを指定するコードを記述します。</span><span class="sxs-lookup"><span data-stu-id="00999-861">Add the new **QuestionnairesErReportContract** class to your Microsoft Visual Studio project, and write code that specifies the data contract that should be used to run the configured ER format.</span></span>

```xpp
/// <summary>
///     This class is the data contract class for the <c>QuestionnairesErReportDP</c> class.
/// </summary>
/// <remarks>
///    This is the data contract class for the Questionnaires ER report.
/// </remarks>
[
    DataContractAttribute,
    SysOperationContractProcessingAttribute(classStr(QuestionnairesErReportUIBuilder))
    ]
    public class QuestionnairesErReportContract extends ERFormatMappingRunBaseContract implements SysOperationValidatable
{
    ERFormatMappingId formatMapping;

    /// <summary>
    ///    Validates the report parameters.
    /// </summary>
    /// <returns>
    ///    true if no errors; otherwise, false.
    /// </returns>
    public boolean validate()
    {
        boolean ret = true;
        if (!formatMapping)
        {
            ret = checkFailed(strFmt("@SYS26332", new SysDictType(extendedTypeNum(ERFormatMappingId)).label()));
        }
        return ret;
    }
    [
        DataMemberAttribute('FormatMapping'),
        SysOperationLabelAttribute(literalstr("@ElectronicReporting:FormatMapping")),
        SysOperationHelpTextAttribute(literalstr("@ElectronicReporting:FormatMapping"))
    ]
    public ERFormatMappingId parmFormatMapping(ERFormatMappingId _formatMapping = formatMapping)
    {
        formatMapping = _formatMapping;
        return formatMapping;
    }
}
```

#### <a name="add-a-ui-builder-class"></a><a name="UIBuilderClass"></a><span data-ttu-id="00999-862">UI Builder のクラスを追加する</span><span class="sxs-lookup"><span data-stu-id="00999-862">Add a UI builder class</span></span>

<span data-ttu-id="00999-863">新しい **QuestionnairesErReportUIBuilder** クラスを Visual Studio プロジェクトに追加し、実行の必要がある ER フォーマットのフォーマット マッピング ID の検索に使用するランタイム ダイアログ ボックスを生成するコードを作成します。</span><span class="sxs-lookup"><span data-stu-id="00999-863">Add the new **QuestionnairesErReportUIBuilder** class to your Visual Studio project, and write code to generate a runtime dialog box that will be used to look up the format mapping ID of the ER format that must be run.</span></span> <span data-ttu-id="00999-864">入力されたコードは、**[ルート](#RootDefinitionName)** 定義を使用して、**[アンケート](#DataModeName)** データ モデルを参照する **データ モデル** タイプのデータ ソースを含む ER フォーマットのみを検索します。</span><span class="sxs-lookup"><span data-stu-id="00999-864">The provided code looks up only ER formats that contain a data source of the **Data model** type that refers to the **[Questionnaires](#DataModeName)** data model by using the **[Root](#RootDefinitionName)** definition.</span></span>

> [!NOTE]
> <span data-ttu-id="00999-865">また、ER 統合ポイントを使用して ER フォーマットをフィルター処理することもできます。</span><span class="sxs-lookup"><span data-stu-id="00999-865">Alternatively, you can use ER integration points to filter ER formats.</span></span> <span data-ttu-id="00999-866">詳細については、[フォーマット マッピングの検索を表示する API](er-apis-app10-0-11.md#api-to-show-a-format-mapping-lookup)を参照してください 。</span><span class="sxs-lookup"><span data-stu-id="00999-866">For more information, see [API to show a format mapping lookup](er-apis-app10-0-11.md#api-to-show-a-format-mapping-lookup).</span></span>

```xpp
/// <summary>
/// The UIBuilder class for Questionnaires ER report
/// </summary>
class QuestionnairesErReportUIBuilder extends SysOperationAutomaticUIBuilder
{
    public const str ERQuestionnairesModel = 'Questionnaires';
    public const str ERQuestionnairesDataContainer = 'Root';

    /// <summary>
    /// Action after build of the dialog UI.
    /// </summary>
    public void postBuild()
    {
        DialogField formatMapping;
        super();
        formatMapping = this.bindInfo().getDialogField(this.dataContractObject(),
            methodStr(QuestionnairesErReportContract, parmFormatMapping));
        formatMapping.registerOverrideMethod(
            methodStr(FormReferenceControl, lookupReference),
            methodStr(QuestionnairesErReportUIBuilder, formatMappingLookup),
            this);
    }

    /// <summary>
    /// Performs the lookup form for format mapping.
    /// </summary>
    /// <param name="_referenceGroupControl">
    /// The control to perform lookup form.
    /// </param>
    public void formatMappingLookup(FormReferenceControl _referenceGroupControl)
    {
        ERObjectsFactory::createFormatMappingTableLookupForControlAndModel(
            _referenceGroupControl,
            ERQuestionnairesModel,
            ERQuestionnairesDataContainer).performFormLookup();
    }
}
```

#### <a name="add-a-data-provider-class"></a><a name="DataProviderClass"></a><span data-ttu-id="00999-867">データ プロバイダーのクラスを追加する</span><span class="sxs-lookup"><span data-stu-id="00999-867">Add a data provider class</span></span>

<span data-ttu-id="00999-868">新しい **QuestionnairesErReportDP** クラスを Visual Studio プロジェクトに追加し、構成された ER フォーマットの実行に使用するデータ プロバイダーを導入するコードを記述します。</span><span class="sxs-lookup"><span data-stu-id="00999-868">Add the new **QuestionnairesErReportDP** class to your Visual Studio project, and write code that introduces the data provider that should used to run the configured ER format.</span></span> <span data-ttu-id="00999-869">作成されたコードには、このデータ プロバイダーのデータ コントラクトのみが含まれます。</span><span class="sxs-lookup"><span data-stu-id="00999-869">The provided code includes only the data contract for this data provider.</span></span>

```xpp
/// <summary>
/// Data provider class for Questionnaires ER report.
/// </summary>
public class QuestionnairesErReportDP
{
    QuestionnairesErReportContract contract;
    public static QuestionnairesErReportDP construct()
    {
        QuestionnairesErReportDP  dataProvider;
        dataProvider = new QuestionnairesErReportDP();
        return dataProvider;
    }
}
```

#### <a name="add-a-labels-file"></a><a name="LabelsFile"></a><span data-ttu-id="00999-870">ラベル ファイルを追加する</span><span class="sxs-lookup"><span data-stu-id="00999-870">Add a labels file</span></span>

<span data-ttu-id="00999-871">Visual Studio プロジェクトに新しい **QuestionnairesErReportLabels\_en-US** ラベルを追加し、新たな UI リソースで使用する次のラベルを指定します :</span><span class="sxs-lookup"><span data-stu-id="00999-871">Add the new **QuestionnairesErReportLabels\_en-US** labels file to your Visual Studio project, and specify the following labels for new UI resources:</span></span>

- <span data-ttu-id="00999-872">**\@QuestionnairesReport** ラベル : 米国英語 (en-US) で記述された **アンケート レポート (ER で実行)** のテキストを含む、新たなメニュー項目に使用される</span><span class="sxs-lookup"><span data-stu-id="00999-872">The **\@QuestionnairesReport** label for a new menu item that contains the following text in US English (en-US): **Questionnaires report (powered by ER)**</span></span>
- <span data-ttu-id="00999-873">**\@QuestionnairesReportBatchJobDescription** ラベル : 選択された ER フォーマットがバッチジョブを実行するようにスケジュールされている場合に、バッチ ジョブのタイトルに使用される</span><span class="sxs-lookup"><span data-stu-id="00999-873">The **\@QuestionnairesReportBatchJobDescription** label for a batch job title if a selected ER format is scheduled for execution as a batch job</span></span>

#### <a name="add-a-report-service-class"></a><a name="ServiceClass"></a><span data-ttu-id="00999-874">レポート サービス クラスを追加する</span><span class="sxs-lookup"><span data-stu-id="00999-874">Add a report service class</span></span>

<span data-ttu-id="00999-875">Visual Studio プロジェクトに新しい **QuestionnairesErReportService** クラスを追加します。続いて ER フォーマットを呼び出し、それをフォーマット マッピング IDで識別し、データ コントラクトをパラメーターとして提供するコードを記述します。</span><span class="sxs-lookup"><span data-stu-id="00999-875">Add the new **QuestionnairesErReportService** class to your Visual Studio project, and write code that calls an ER format, identifies it by a format mapping ID, and provides a data contract as a parameter.</span></span>

```xpp
using Microsoft.Dynamics365.LocalizationFramework;
/// <summary>
/// The electronic reporting service class for Questionnaires ER report
/// </summary>
class QuestionnairesErReportService extends SysOperationServiceBase
{
    public const str ERModelDataSourceName = 'model';
    public const str DefaultExportedFileName = 'Questionnaires report';
    public const str ParametersDataSourceName = 'RunTimeParameters';

    /// <summary>
    /// Generates report by using Electronic reporting framework
    /// </summary>
    /// <param name = "_contract">The Questionnaires report contract</param>
    public void generateReportByGER(QuestionnairesErReportContract _contract)
    {
        ERFormatMappingId formatMappingId;
        QuestionnairesErReportDP  dataProvider;
        dataProvider = QuestionnairesErReportDP::construct();
        formatMappingId = _contract.parmFormatMapping();
        if (formatMappingId)
        {
            try
            {
                ERIModelDefinitionParamsAction parameters = new ERModelDefinitionParamsUIActionComposite()
                    .add(new ERModelDefinitionObjectParameterAction(ERModelDataSourceName, ParametersDataSourceName, _contract, true));

                // Call ER to generate the report.
                ERIFormatMappingRun formatMappingRun = ERObjectsFactory::createFormatMappingRunByFormatMappingId(formatMappingId, DefaultExportedFileName);
                if (formatMappingRun.parmShowPromptDialog(true))
                {
                    formatMappingRun.withParameter(parameters);
                    formatMappingRun.withFileDestination(_contract.getFileDestination());
                    formatMappingRun.run();
                }
            }
            catch
            {
                // An error occurred while exporting data.
                error("@SYP4861341");
            }
        }
        else
        {
            // There is no data available.
            info("@SYS300117");
        }
    }
}
```

<span data-ttu-id="00999-876">アプリケーションデータを実行する ER フォーマットを使用する必要がある場合は、フォーマット マッピングで **データ モデル** タイプのデータ ソースを構成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="00999-876">When you must use an ER format that runs application data, you must configure a data source of the **Data model** type in the format mapping.</span></span> <span data-ttu-id="00999-877">このデータソースは、単一のルート定義を使用して、指定されたデータ モデルの特定の部分を参照します。</span><span class="sxs-lookup"><span data-stu-id="00999-877">This data source refers to a specific part of the specified data model by using a single root definition.</span></span> <span data-ttu-id="00999-878">ER フォーマットを実行するとと、このデータソースを呼び出して、指定されたモデルとルート定義に対して構成されている適切な ER モデル マッピングにアクセスします。</span><span class="sxs-lookup"><span data-stu-id="00999-878">When the ER format is run, it calls this data source to access the appropriate ER model mapping that is configured for a given model and root definition.</span></span>

<span data-ttu-id="00999-879">ソースコードで作成し、データ コントラクトの一部として保存されているすべての情報は、このタイプの ER モデル マッピングを使用して、実行中の ER フォーマットに渡すことができます。</span><span class="sxs-lookup"><span data-stu-id="00999-879">All the information that you might prepare in the source code and store as part of the data contract can be passed to the running ER format by using an ER model mapping of this type.</span></span> <span data-ttu-id="00999-880">ER モデル マッピングでは、**[QuestionnairesErReportContract](#DataContractClass)** クラスを参照する **オブジェクト** 型のデータ ソースを設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="00999-880">In the ER model mapping, you must configure a data source of the **Object** type that refers to the **[QuestionnairesErReportContract](#DataContractClass)** class.</span></span> <span data-ttu-id="00999-881">モデル マッピングを識別するには、このモデル マッピングを呼び出すデータ ソースを指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="00999-881">To identify a model mapping, you must specify a data source that calls this model mapping.</span></span> <span data-ttu-id="00999-882">作成されたコードでは、**[モデル](#ModelDSName)** の値を持つ **ERModelDataSourceName** 定数で指定されたこのデータソースが指定されます。</span><span class="sxs-lookup"><span data-stu-id="00999-882">In the provided code, this data source specified by the **ERModelDataSourceName** constant that has the **[model](#ModelDSName)** value.</span></span> <span data-ttu-id="00999-883">モデル マッピングに対して、どのデータ ソースがデータ コントラクトの公開に使用されているかを特定するには、データ ソース名を指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="00999-883">To identify which data source is used to expose the data contract in the model mapping, you must specify a data source name.</span></span> <span data-ttu-id="00999-884">作成されたコードでは、この名前は <a name="DataContractDSName"></a>**RunTimeParameters** の値を持つ **ParametersDataSourceName** 定数で指定されます。</span><span class="sxs-lookup"><span data-stu-id="00999-884">In the provided code, this name is specified by the **ParametersDataSourceName** constant that has <a name="DataContractDSName"></a>**RunTimeParameters** value.</span></span>

> [!NOTE]
> <span data-ttu-id="00999-885">新しい環境では、ER モデル マッピング デザイナーでこのタイプのクラスが利用できるよう、ER メタデータの更新が必要となる場合があります。</span><span class="sxs-lookup"><span data-stu-id="00999-885">In a new environment, you might have to refresh the ER metadata so that this type of class is available in the ER model mapping designer.</span></span> <span data-ttu-id="00999-886">詳細については、[電子レポート (ER) フレームワークの構成](electronic-reporting-er-configure-parameters.md#frequently-asked-questions) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="00999-886">For more information, see [Configure the ER framework](electronic-reporting-er-configure-parameters.md#frequently-asked-questions).</span></span>

#### <a name="add-a-report-controller-class"></a><a name="ControllerClass"></a><span data-ttu-id="00999-887">レポートのコントローラ クラスを追加する</span><span class="sxs-lookup"><span data-stu-id="00999-887">Add a report controller class</span></span>

<span data-ttu-id="00999-888">Visual Studio プロジェクトに、新しい **QuestionnairesErReportController** クラスを追加し、提供された **QuestionnairesErReportUIBuilder** クラスのロジックに基づいて構築されたダイアログ ボックスで、同期モードまたはバッチモードのいずれかでERフォーマットを実行するコードを記述します。</span><span class="sxs-lookup"><span data-stu-id="00999-888">Add the new **QuestionnairesErReportController** class to your Visual Studio project, and write code that runs an ER format in either synchronous mode or batch mode, as you prefer, in the dialog box that is built based on the logic of the provided **QuestionnairesErReportUIBuilder** class.</span></span>

```xpp
/// <summary>
/// The controller for Questionnaires ER report
/// </summary>
class QuestionnairesErReportController extends ERFormatMappingRunBaseController
{
    /// <summary>
    /// The main entrance of the controller
    /// </summary>
    /// <param name = "args">The arguments</param>
    public static void main(Args args)
    {
        QuestionnairesErReportController operation;
        operation = new QuestionnairesErReportController(
            classStr(QuestionnairesErReportService),
            methodStr(QuestionnairesErReportService, generateReportByGER),
            SysOperationExecutionMode::Synchronous);
        operation.startOperation();
    }

    /// <summary>
    /// Gets caption of the dialog.
    /// </summary>
    /// <returns>Caption of the dialog</returns>
    public ClassDescription defaultCaption()
    {
        ClassDescription batchDescription;
        batchDescription = "Questionnaires report (powered by ER)";
        return batchDescription;
    }
}
```

#### <a name="add-a-menu-item"></a><a name="MenuItem"></a><span data-ttu-id="00999-889">メニュー項目を追加する</span><span class="sxs-lookup"><span data-stu-id="00999-889">Add a menu item</span></span>

<span data-ttu-id="00999-890">Visual Studio プロジェクトに新しい **QuestionnairesErReport** メニュー項目を追加します。</span><span class="sxs-lookup"><span data-stu-id="00999-890">Add the new **QuestionnairesErReport** menu item to your Visual Studio project.</span></span> <span data-ttu-id="00999-891">**オブジェクト** プロパティでは、このメニュー項目は **QuestionnairesErReportController** クラスを参照し、ER フォーマットを選択して実行するユーザーアクセス許可を指定するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="00999-891">In the **Object** property, this menu item refers to the **QuestionnairesErReportController** class, and it's used to specify a user permission to select and run an ER format.</span></span> <span data-ttu-id="00999-892">**ラベル** プロパティでは、このメニュー項目は前述の手順で作成した **\@QuestionnairesReport** ラベルを参照し、アプリケーションの UI に正しいテキストが表示されるようになります。</span><span class="sxs-lookup"><span data-stu-id="00999-892">In the **Label** property, this menu item refers to the **\@QuestionnairesReport** label that you created earlier, so that correct text is presented in the application UI.</span></span>

#### <a name="add-a-menu-item-to-a-menu"></a><a name="Menu"></a><span data-ttu-id="00999-893">メニュー項目をメニューに追加する</span><span class="sxs-lookup"><span data-stu-id="00999-893">Add a menu item to a menu</span></span>

<span data-ttu-id="00999-894">既存の **KM** メニューを Visual Studio プロジェクトに追加します。</span><span class="sxs-lookup"><span data-stu-id="00999-894">Add the existing **KM** menu to your Visual Studio project.</span></span> <span data-ttu-id="00999-895">このメニューには、**出力** タイプに新しい **QuestionnairesErReport** 項目を追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="00999-895">You must add a new **QuestionnairesErReport** item of the **Output** type to this menu.</span></span> <span data-ttu-id="00999-896">この項目は、前のセクションで説明したメニュー項目 **QuestionnairesErReport** を参照する必要があります。</span><span class="sxs-lookup"><span data-stu-id="00999-896">This item must refer to the **QuestionnairesErReport** menu item that is described in the previous section.</span></span>

#### <a name="build-a-visual-studio-project"></a><a name="BuildVSProject"></a><span data-ttu-id="00999-897">Visual Studio プロジェクトをビルドする</span><span class="sxs-lookup"><span data-stu-id="00999-897">Build a Visual Studio project</span></span>

<span data-ttu-id="00999-898">プロジェクトをビルドして、新しいメニュー項目をユーザーが使用できるようにします。</span><span class="sxs-lookup"><span data-stu-id="00999-898">Build your project to make a new menu item available to users.</span></span>

### <a name="run-a-format-from-the-application"></a><a name="RunFormatFromApp"></a><span data-ttu-id="00999-899">アプリケーションからフォーマットを実行する</span><span class="sxs-lookup"><span data-stu-id="00999-899">Run a format from the application</span></span>

1. <span data-ttu-id="00999-900">**アンケート** \> **デザイン** \> **アンケート レポート (ER による実行)** に移動します。</span><span class="sxs-lookup"><span data-stu-id="00999-900">Go to **Questionnaire** \> **Design** \> **Questionnaires report (powered by ER)**.</span></span>

    ![アンケート モジュールのアンケート レポート (ER による実行) メニュー項目を選択して、構成された ER フォーマットが実行する](./media/er-quick-start1-application-menu-modified.png)

2. <span data-ttu-id="00999-902">ダイアログボックスの **フォーマットのマッピング** フィールドで、**アンケート レポート** を選択します。</span><span class="sxs-lookup"><span data-stu-id="00999-902">In the dialog box, in the **Format mapping** field, select **Questionnaires report**.</span></span>
3. <span data-ttu-id="00999-903">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="00999-903">Select **OK**.</span></span>
4. <span data-ttu-id="00999-904">**電子レポート** ダイアログ ボックスの **含めるレコード** クイックタブに、**SBCCrsExam** アンケートのみが含まれるようにフィルター処理オプションを構成します。</span><span class="sxs-lookup"><span data-stu-id="00999-904">In the **Electronic report parameters** dialog box, on the **Records to include** FastTab, configure the filtering option so that only the **SBCCrsExam** questionnaire is included.</span></span>
5. <span data-ttu-id="00999-905">**OK** を選択してオプションを確認します。</span><span class="sxs-lookup"><span data-stu-id="00999-905">Select **OK** to confirm the filtering option.</span></span>
6. <span data-ttu-id="00999-906">**OK** を選択してレポートを実行します。</span><span class="sxs-lookup"><span data-stu-id="00999-906">Select **OK** to run the report.</span></span>

    ![電子レポートのダイアログ ボックスで、選択基準を指定する](./media/er-quick-start1-report-run-dialog-page.png)

7. <span data-ttu-id="00999-908">生成されたレポートを確認します。</span><span class="sxs-lookup"><span data-stu-id="00999-908">Review the generated report.</span></span>

## <a name="tune-a-designed-er-solution"></a><a name="TuneSolution"></a><span data-ttu-id="00999-909">設計済みの ER ソリューションを調整する</span><span class="sxs-lookup"><span data-stu-id="00999-909">Tune a designed ER solution</span></span>

<span data-ttu-id="00999-910">構成された ER ソリューションを変更して、実行中の ER フォーマットの詳細にアクセスするために開発したデータ プロバイダ クラスを使用し、生成されたレポートにこの ER フォーマットの名前を入力することができます。</span><span class="sxs-lookup"><span data-stu-id="00999-910">You can modify the configured ER solution so that it uses the data provider class that you developed to access details of the running ER format, and so that it enters the name of this ER format in a generated report.</span></span>

### <a name="modify-a-model-mapping"></a><a name="ModifyModelMapping"></a><span data-ttu-id="00999-911">モデルのマッピングを修正する</span><span class="sxs-lookup"><span data-stu-id="00999-911">Modify a model mapping</span></span>

#### <a name="add-data-sources-to-access-a-data-contract-object"></a><a name="AddDataSource1"></a><span data-ttu-id="00999-912">データ ソースを追加してデータ コントラクト オブジェクトにアクセスする</span><span class="sxs-lookup"><span data-stu-id="00999-912">Add data sources to access a data contract object</span></span>

1. <span data-ttu-id="00999-913">**組織管理** \> **電子申告** \> **構成** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="00999-913">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="00999-914">**構成** ページの構成ツリーで、**アンケート モデル** を展開し、**アンケート マッピング** を選択します。</span><span class="sxs-lookup"><span data-stu-id="00999-914">On the **Configurations** page, in the configuration tree, expand **Questionnaire model**, and then select **Questionnaire mapping**.</span></span>
3. <span data-ttu-id="00999-915">**デザイナー** を選択すると、**データソース マッピングに使用するモデル** ページが開きます。</span><span class="sxs-lookup"><span data-stu-id="00999-915">Select **Designer** to open the **Model to datasource mapping** page.</span></span>
4. <span data-ttu-id="00999-916">**デザーナー** を選択して、モデル マッピング デザイナーで選択したデザイナーを開きます。</span><span class="sxs-lookup"><span data-stu-id="00999-916">Select **Designer** to open the selected mapping in the model mapping designer.</span></span>
5. <span data-ttu-id="00999-917">**モデル マッピング デザイナー** ページの **データ ソース タイプ** ペインで、**Dynamics 365 for Operations\\オブジェクト** を選択します。</span><span class="sxs-lookup"><span data-stu-id="00999-917">On the **Model mapping designer** page, in the **Data source types** pane, select **Dynamics 365 for Operations\\Object**.</span></span>
6. <span data-ttu-id="00999-918">**データ ソース** ペインで、**ルートの追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="00999-918">In the **Data sources** pane, select **Add root**.</span></span>
7. <span data-ttu-id="00999-919">ダイアログ ボックスの **名前** フィールドに、**QuestionnairesErReportService** クラスのソースコードで定義されている **[RunTimeParameters](#DataContractDSName)** を入力します。</span><span class="sxs-lookup"><span data-stu-id="00999-919">In the dialog box, in the **Name** field, enter **[RunTimeParameters](#DataContractDSName)**, as defined in the source code of the **QuestionnairesErReportService** class.</span></span>
8. <span data-ttu-id="00999-920">**クラス** フィールドで、前述の手順で記述した **[QuestionnairesErReportContract](#DataContractClass)** を入力します。</span><span class="sxs-lookup"><span data-stu-id="00999-920">In the **Class** field, enter **[QuestionnairesErReportContract](#DataContractClass)**, which was coded earlier.</span></span>
9. <span data-ttu-id="00999-921">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="00999-921">Select **OK**.</span></span>
10. <span data-ttu-id="00999-922">**RunTimeParameters** を展開します。</span><span class="sxs-lookup"><span data-stu-id="00999-922">Expand **RunTimeParameters**.</span></span>

<span data-ttu-id="00999-923">追加されたデータソースは、実行中の ER フォーマット マッピングのレコード ID に関する情報を提供します。</span><span class="sxs-lookup"><span data-stu-id="00999-923">The added data source provides information about the record ID of the running ER format mapping.</span></span>

![ER モデル マッピング デザイナーにデータソースを追加する](./media/er-quick-start1-mapping3.png)

#### <a name="add-a-data-source-to-access-er-format-mapping-records"></a><a name="AddDataSource2"></a><span data-ttu-id="00999-925">データ ソースを追加して ER フォーマット マッピング レコードにアクセスする</span><span class="sxs-lookup"><span data-stu-id="00999-925">Add a data source to access ER format mapping records</span></span>

<span data-ttu-id="00999-926">ER フォーマットのマッピング レコードへのアクセスに使用するデータソースを追加して、選択したモデル マッピングの編集を続行します。</span><span class="sxs-lookup"><span data-stu-id="00999-926">Continue to edit the selected model mapping by adding a data source to access ER format mapping records.</span></span>

1. <span data-ttu-id="00999-927">**モデル マッピング デザイナー** ページの、**データ ソース タイプ** ペインで、**Dynamics 365 for Operations\\テーブル レコード** を選択します。</span><span class="sxs-lookup"><span data-stu-id="00999-927">On the **Model mapping designer** page, in the **Data source types** pane, select **Dynamics 365 for Operations\\Table records**.</span></span>
2. <span data-ttu-id="00999-928">**データ ソース** ペインで、**ルートの追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="00999-928">In the **Data sources** pane, select **Add root**.</span></span>
3. <span data-ttu-id="00999-929">ダイアログ ボックスで、**名前** フィールドに **ER1** と入力します。</span><span class="sxs-lookup"><span data-stu-id="00999-929">In the dialog box, in the **Name** field, enter **ER1**.</span></span>
4. <span data-ttu-id="00999-930">**テーブル** フィールドに、**ERFormatMappingTable** と入力します。</span><span class="sxs-lookup"><span data-stu-id="00999-930">In the **Table** field, enter **ERFormatMappingTable**.</span></span>
5. <span data-ttu-id="00999-931">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="00999-931">Select **OK**.</span></span>

#### <a name="add-a-data-source-to-access-a-format-mapping-record-of-a-running-er-format"></a><a name="AddDataSource3"></a><span data-ttu-id="00999-932">データ ソースを追加して実行中の ER フォーマットのフォーマット マッピング レコードにアクセスする</span><span class="sxs-lookup"><span data-stu-id="00999-932">Add a data source to access a format mapping record of a running ER format</span></span>

<span data-ttu-id="00999-933">実行中の ER フォーマットのフォーマット マッピング レコードへのアクセスに使用するデータソースを追加して、選択したモデルマッピングの編集を続行します。</span><span class="sxs-lookup"><span data-stu-id="00999-933">Continue to edit the selected model mapping by adding a data source to access the format mapping record of the running ER format.</span></span>

1. <span data-ttu-id="00999-934">**モデル マッピング デザイナー** ページの **データ ソース タイプ** ウィンドウで、**関数\\計算フィールド** を選択します。</span><span class="sxs-lookup"><span data-stu-id="00999-934">On the **Model mapping designer** page, in the **Data source types** pane, select **Functions\\Calculated field**.</span></span>
2. <span data-ttu-id="00999-935">**データ ソース** ペインで、**ルートの追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="00999-935">In the **Data sources** pane, select **Add root**.</span></span>
3. <span data-ttu-id="00999-936">ダイアログ ボックスで、**名前** フィールドに **ER2** と入力します。</span><span class="sxs-lookup"><span data-stu-id="00999-936">In the dialog box, in the **Name** field, enter **ER2**.</span></span>
4. <span data-ttu-id="00999-937">**式の編集** を選択します。</span><span class="sxs-lookup"><span data-stu-id="00999-937">Select **Edit formula**.</span></span>
5. <span data-ttu-id="00999-938">式エディターで、**式** フィールドに、**FIRSTORNULL (FILTER(ER1, ER1.RecId = RunTimeParameters.parmFormatMapping))** と入力します。</span><span class="sxs-lookup"><span data-stu-id="00999-938">In the formula editor, in the **Formula** field, enter **FIRSTORNULL (FILTER(ER1, ER1.RecId = RunTimeParameters.parmFormatMapping))**.</span></span>
6. <span data-ttu-id="00999-939">**保存** を選択し、式エディターを閉じます。</span><span class="sxs-lookup"><span data-stu-id="00999-939">Select **Save**, and close the formula editor.</span></span>
7. <span data-ttu-id="00999-940">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="00999-940">Select **OK**.</span></span>

#### <a name="enter-the-name-of-the-running-er-format-in-the-data-model"></a><a name="AddBinding"></a><span data-ttu-id="00999-941">データ モデル内で実行中の ER フォーマットの名前を入力する</span><span class="sxs-lookup"><span data-stu-id="00999-941">Enter the name of the running ER format in the data model</span></span>

<span data-ttu-id="00999-942">選択したモデルマッピングの編集を続けて、実行中の ER フォーマットの名前がデータモデルに入力されるようにします。</span><span class="sxs-lookup"><span data-stu-id="00999-942">Continue to edit the selected model mapping so that the name of the running ER format is entered in the data model.</span></span>

1. <span data-ttu-id="00999-943">**モデル マッピング デザイナー** ページの、 **データ モデル** ペインで、**ExecutionContext** を展開し、続いて **ExecutionContext\\FormatName** 編集を選択します。</span><span class="sxs-lookup"><span data-stu-id="00999-943">On the **Model mapping designer** page, in the **Data model** pane, expand **ExecutionContext**, and then select **ExecutionContext\\FormatName**.</span></span>
2. <span data-ttu-id="00999-944">**データモデル** ペインで、**編集** を選択してデータ モデル フィールドのデータ バインドを構成します。</span><span class="sxs-lookup"><span data-stu-id="00999-944">In the **Data model** pane, select **Edit** to configure a data binding for the selected data model's field.</span></span>
3. <span data-ttu-id="00999-945">式エディターで、**式** フィールドに **FIRSTORNULL (ER2.'\>Relations'.Format).Name** と入力します。</span><span class="sxs-lookup"><span data-stu-id="00999-945">In the formula editor, in the **Formula** field, enter **FIRSTORNULL (ER2.'\>Relations'.Format).Name**.</span></span>
4. <span data-ttu-id="00999-946">**保存** を選択し、式エディターを閉じます。</span><span class="sxs-lookup"><span data-stu-id="00999-946">Select **Save**, and close the formula editor.</span></span>

<span data-ttu-id="00999-947">**FormatName** フィールドを使用したため、構成されたモデル マッピングでは、実行中にこのモデル マッピングの呼び出しを行う ER フォーマットの名前を公開するようになります。</span><span class="sxs-lookup"><span data-stu-id="00999-947">Because you used the **FormatName** field, the configured model mapping now exposes the name of an ER format that calls this model mapping during execution.</span></span>

![ER モデル マッピング デザイナーで追加されたデータソースのメソッドにデータ モデル フィールドをバインドする](./media/er-quick-start1-mapping4.png)

#### <a name="complete-the-design-of-the-model-mapping"></a><a name="CompleteModelMapping2"></a><span data-ttu-id="00999-949">モデル マッピングを完了する</span><span class="sxs-lookup"><span data-stu-id="00999-949">Complete the design of the model mapping</span></span>

1. <span data-ttu-id="00999-950">**データ モデル デザイナー** ページで、**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="00999-950">On the **Model mapping designer** page, select **Save**.</span></span>
2. <span data-ttu-id="00999-951">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="00999-951">Close the page.</span></span>
3. <span data-ttu-id="00999-952">モデル マッピング ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="00999-952">Close the model mappings page.</span></span>
4. <span data-ttu-id="00999-953">**構成** ページの構成ツリーで、**アンケート マッピング** の構成が選択されていることを確認してください。</span><span class="sxs-lookup"><span data-stu-id="00999-953">On the **Configurations** page, in the configuration tree, make sure that the **Questionnaire mapping** configuration is still selected.</span></span> <span data-ttu-id="00999-954">続いて、**バージョン** クイック タブで、状態が **下書き** となっている構成のバージョンを選択します。</span><span class="sxs-lookup"><span data-stu-id="00999-954">Then, on the **Versions** FastTab, select the configuration version that has a status of **Draft**.</span></span>
5. <span data-ttu-id="00999-955">**ステータスの変更** \> **完了** を選択します。</span><span class="sxs-lookup"><span data-stu-id="00999-955">Select **Change status** \> **Complete**.</span></span>

<span data-ttu-id="00999-956">この構成のバージョン 1.2 の状態 **下書き** から **完了** に変更されます。</span><span class="sxs-lookup"><span data-stu-id="00999-956">The status of version 1.2 of this configuration is changed from **Draft** to **Completed**.</span></span> <span data-ttu-id="00999-957">バージョン 1.2 を変更することはできなくなります。</span><span class="sxs-lookup"><span data-stu-id="00999-957">Version 1.2 can no longer be changed.</span></span> <span data-ttu-id="00999-958">このバージョンには、構成済みのモデル マッピングが含まれており、その他の ER の構成の基礎として使用できます。</span><span class="sxs-lookup"><span data-stu-id="00999-958">This version contains the configured model mapping and can be used as the basis for other ER configurations.</span></span> <span data-ttu-id="00999-959">この構成のバージョン 1.3 が作成され、状態が **下書き** になります。</span><span class="sxs-lookup"><span data-stu-id="00999-959">Version 1.3 of this configuration is created and has a status of **Draft**.</span></span> <span data-ttu-id="00999-960">このバージョンを編集して、**アンケート** モデル マッピングを調整することができます。</span><span class="sxs-lookup"><span data-stu-id="00999-960">You can edit this version to adjust the **Questionnaire** model mapping.</span></span>

### <a name="modify-a-format"></a><a name="ModifyFormat"></a><span data-ttu-id="00999-961">フォーマットを変更する</span><span class="sxs-lookup"><span data-stu-id="00999-961">Modify a format</span></span>

<span data-ttu-id="00999-962">構成された ER フォーマットを変更することがで、ER フォーマットの実行時に生成されるレポートのフッターに名前が表示させることができます。</span><span class="sxs-lookup"><span data-stu-id="00999-962">You can modify the configured ER format so that its name is shown in the footer of a report that is generated when the ER format is run.</span></span>

#### <a name="add-a-new-format-element"></a><a name="AddFormatElement"></a><span data-ttu-id="00999-963">新たなフォーマット要素を追加する</span><span class="sxs-lookup"><span data-stu-id="00999-963">Add a new format element</span></span>

1. <span data-ttu-id="00999-964">**組織管理** \> **電子申告** \> **構成** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="00999-964">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="00999-965">**構成** ページの構成ツリーで、**アンケート モデル** を展開し、**アンケート レポート** を選択します。</span><span class="sxs-lookup"><span data-stu-id="00999-965">On the **Configurations** page, in the configuration tree, expand **Questionnaire model**, and then select **Questionnaire report**.</span></span>
3. <span data-ttu-id="00999-966">**デザイナー** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="00999-966">Select **Designer**.</span></span>
4. <span data-ttu-id="00999-967">**フォーマット デザイナー** ページで、ルート項目 **レポート** を選択します。</span><span class="sxs-lookup"><span data-stu-id="00999-967">On the **Format designer** page, select the **Report** root item.</span></span>
5. <span data-ttu-id="00999-968">**追加** を選択して、 選択されたルート項目の **レポート** に新しいネストされたフォーマット要素を追加します。</span><span class="sxs-lookup"><span data-stu-id="00999-968">Select **Add** to add a new nested format element for the selected **Report** root item.</span></span>
6. <span data-ttu-id="00999-969">**Excel\\フッター** を選択します。</span><span class="sxs-lookup"><span data-stu-id="00999-969">Select **Excel\\Footer**.</span></span>
7. <span data-ttu-id="00999-970">**名前** フィールドに、**フッター** と入力します。</span><span class="sxs-lookup"><span data-stu-id="00999-970">In the **Name** field, enter **Footer**.</span></span>
8. <span data-ttu-id="00999-971">**レポート\フッター** を選択し、続いて **追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="00999-971">Select **Report\Footer**, and then select **Add**.</span></span>
9. <span data-ttu-id="00999-972">**テキスト\\文字列** を選択します。</span><span class="sxs-lookup"><span data-stu-id="00999-972">Select **Text\\String**.</span></span>

#### <a name="bind-the-added-format-element"></a><a name="BindAddedFormatElement"></a><span data-ttu-id="00999-973">追加されたフォーマット要素をバインドする</span><span class="sxs-lookup"><span data-stu-id="00999-973">Bind the added format element</span></span>

1. <span data-ttu-id="00999-974">**フォーマット デザーナー** ページ上の **マッピング** タブでのフォーマット ツリーで、**フッター\\文字列** 要素に対して **式の編集** を選択します。</span><span class="sxs-lookup"><span data-stu-id="00999-974">On the **Format designer** page, on the **Mapping** tab, in the format tree, for the active **Footer\\String** element, select **Edit formula**.</span></span>
2. <span data-ttu-id="00999-975">式エディターの **式** フィールドで、**CONCATENATE ("\&C\&10", FORMAT("Generated by'\%1' ER solution", model.ExecutionContext.FormatName))** と入力します。</span><span class="sxs-lookup"><span data-stu-id="00999-975">In the formula editor, in the **Formula** field, enter **CONCATENATE ("\&C\&10", FORMAT("Generated by'\%1' ER solution", model.ExecutionContext.FormatName))**.</span></span>
3. <span data-ttu-id="00999-976">**保存** を選択し、式エディターを閉じます。</span><span class="sxs-lookup"><span data-stu-id="00999-976">Select **Save**, and close the formula editor.</span></span>
4. <span data-ttu-id="00999-977">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="00999-977">Select **Save**.</span></span>

<span data-ttu-id="00999-978">構成されたフォーマットが、**フッター\\文字列** 要素を使用して、生成されたレポートのフッターにその名前を入力するよう変更されます。</span><span class="sxs-lookup"><span data-stu-id="00999-978">The configured format has now been modified so that its name will be entered in the footer of a generated report by using the **Footer\\String** element.</span></span>

![ER 操作デザイナーで設定したフォーマットにフッター フォーマットの要素を追加する](./media/er-quick-start1-template-format-structure3.png)

#### <a name="complete-the-format-design"></a><a name="CompleteFormat2"></a><span data-ttu-id="00999-980">フォーマットの設計を完了する</span><span class="sxs-lookup"><span data-stu-id="00999-980">Complete the format design</span></span>

1. <span data-ttu-id="00999-981">**形式デザイナー** ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="00999-981">Close the **Format designer** page.</span></span>
2. <span data-ttu-id="00999-982">**構成** ページの構成ツリーで、**アンケート レポート** の構成が選択されていることを確認してください。</span><span class="sxs-lookup"><span data-stu-id="00999-982">On the **Configurations** page, in the configuration tree, make sure that the **Questionnaire report** configuration is still selected.</span></span> <span data-ttu-id="00999-983">続いて、**バージョン** クイック タブで、状態が **下書き** となっている構成のバージョンを選択します。</span><span class="sxs-lookup"><span data-stu-id="00999-983">Then, on the **Versions** FastTab, select the configuration version that has a status of **Draft**.</span></span>
3. <span data-ttu-id="00999-984">**ステータスの変更** \> **完了** を選択します。</span><span class="sxs-lookup"><span data-stu-id="00999-984">Select **Change status** \> **Complete**.</span></span>

<span data-ttu-id="00999-985">この構成のバージョン 1.2 の状態 **下書き** から **完了** に変更されます。</span><span class="sxs-lookup"><span data-stu-id="00999-985">The status of version 1.2 of this configuration is changed from **Draft** to **Completed**.</span></span> <span data-ttu-id="00999-986">バージョン 1.2 を変更することはできなくなります。</span><span class="sxs-lookup"><span data-stu-id="00999-986">Version 1.2 can no longer be changed.</span></span> <span data-ttu-id="00999-987">このバージョンには、構成済みのフォーマットが含まれており、その他の ER の構成の基礎として使用することができます。</span><span class="sxs-lookup"><span data-stu-id="00999-987">This version contains the configured format and can be used as the basis for other ER configurations.</span></span> <span data-ttu-id="00999-988">この構成のバージョン 1.3 が作成され、状態が **下書き** になります。</span><span class="sxs-lookup"><span data-stu-id="00999-988">Version 1.3 of this configuration is created and has a status of **Draft**.</span></span> <span data-ttu-id="00999-989">このバージョンを編集して、**アンケート** レポートを調整することができます。</span><span class="sxs-lookup"><span data-stu-id="00999-989">You can edit this version to adjust the **Questionnaire** report.</span></span>

### <a name="run-a-format-from-the-application"></a><a name="RunFormatFromApp2"></a><span data-ttu-id="00999-990">アプリケーションからフォーマットを実行する</span><span class="sxs-lookup"><span data-stu-id="00999-990">Run a format from the application</span></span>

1. <span data-ttu-id="00999-991">**アンケート** \> **デザイン** \> **アンケート レポート (ER による実行)** に移動します。</span><span class="sxs-lookup"><span data-stu-id="00999-991">Go to **Questionnaire** \> **Design** \> **Questionnaires report (powered by ER)**.</span></span>
2. <span data-ttu-id="00999-992">ダイアログボックスの **フォーマットのマッピング** フィールドで、**アンケート レポート** を選択します。</span><span class="sxs-lookup"><span data-stu-id="00999-992">In the dialog box, in the **Format mapping** field, select **Questionnaires report**.</span></span>
3. <span data-ttu-id="00999-993">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="00999-993">Select **OK**.</span></span>
4. <span data-ttu-id="00999-994">**ER パラメーター** ダイアログ ボックスの **含めるレコード** クイックタブに、**sbccrsexam** アンケートのみが含まれるようにフィルター処理オプションを構成します。</span><span class="sxs-lookup"><span data-stu-id="00999-994">In the **ER parameters** dialog box, on the **Records to include** FastTab, configure the filtering option so that only the **SBCCrsExam** questionnaire is included.</span></span>
5. <span data-ttu-id="00999-995">**OK** を選択してオプションを確認します。</span><span class="sxs-lookup"><span data-stu-id="00999-995">Select **OK** to confirm the filtering option.</span></span>
6. <span data-ttu-id="00999-996">**OK** を選択してレポートを実行します。</span><span class="sxs-lookup"><span data-stu-id="00999-996">Select **OK** to run the report.</span></span>
7. <span data-ttu-id="00999-997">Excel フォーマットで生成されたレポートを確認してください。</span><span class="sxs-lookup"><span data-stu-id="00999-997">Review the generated report in Excel format.</span></span>

<span data-ttu-id="00999-998">生成されたレポートのフッターには、生成に使用した ER フォーマットの名前が含まれることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="00999-998">Notice that the footer of the generated report contains the name of the ER format that was used to generate it.</span></span>

![Excel フォーマットで生成されたレポート](./media/er-quick-start1-report4.png)

### <a name="run-a-format-from-er"></a><a name="RunFormatFromER3"></a><span data-ttu-id="00999-1000">ER からフォーマットを実行する</span><span class="sxs-lookup"><span data-stu-id="00999-1000">Run a format from ER</span></span>

1. <span data-ttu-id="00999-1001">**組織管理** \> **電子申告** \> **構成** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="00999-1001">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="00999-1002">**構成** ページの構成ツリーで、**アンケート モデル** を展開し、**アンケート レポート** を選択します。</span><span class="sxs-lookup"><span data-stu-id="00999-1002">On the **Configurations** page, in the configuration tree, expand **Questionnaire model**, and then select **Questionnaire report**.</span></span>
3. <span data-ttu-id="00999-1003">アクション ウィンドウで、**実行** を選択します。</span><span class="sxs-lookup"><span data-stu-id="00999-1003">On the Action Pane, select **Run**.</span></span>
4. <span data-ttu-id="00999-1004">**電子レポート** ダイアログ ボックスの **含めるレコード** クイックタブに、**SBCCrsExam** アンケートのみが含まれるようにフィルター処理オプションを構成します。</span><span class="sxs-lookup"><span data-stu-id="00999-1004">In the **Electronic report parameters** dialog box, on the **Records to include** FastTab, configure the filtering option so that only the **SBCCrsExam** questionnaire is included.</span></span>
5. <span data-ttu-id="00999-1005">**OK** を選択してオプションを確認します。</span><span class="sxs-lookup"><span data-stu-id="00999-1005">Select **OK** to confirm the filtering option.</span></span>
6. <span data-ttu-id="00999-1006">**OK** を選択してレポートを実行します。</span><span class="sxs-lookup"><span data-stu-id="00999-1006">Select **OK** to run the report.</span></span>
7. <span data-ttu-id="00999-1007">Excel フォーマットで生成されたレポートを確認してください。</span><span class="sxs-lookup"><span data-stu-id="00999-1007">Review the generated report in Excel format.</span></span>

<span data-ttu-id="00999-1008">生成されるレポートのフッターには、生成時に使用された ER 形式の名前が含まれないことに注意してください。これは ER から実行されたER フォーマットが呼び出したデータ コントラクト オブジェクトが、実行中のモデル マッピングに渡されないためです。</span><span class="sxs-lookup"><span data-stu-id="00999-1008">Notice that the footer of the generated report doesn't contain the name of ER format that was used to generate it, because the data contract object wasn't passed to the running model mapping when it was called by the ER format that was run from ER.</span></span>

### <a name="configure-a-format-destination-for-on-screen-preview"></a><a name="ConfigureDestination"></a><span data-ttu-id="00999-1009">オン スクリーン プレビューに使用するフォーマットの出力先を構成する</span><span class="sxs-lookup"><span data-stu-id="00999-1009">Configure a format destination for on-screen preview</span></span>

1. <span data-ttu-id="00999-1010">**組織管理** \> **電子レポート** \> **電子レポートの送信先** に移動します。</span><span class="sxs-lookup"><span data-stu-id="00999-1010">Go to **Organization administration** \> **Electronic reporting** \> **Electronic reporting destination**.</span></span>
2. <span data-ttu-id="00999-1011">**電子レポートの送信先** ページで、構成済の ER フォーマット **アンケート レポート** の送信先レコードを追加します。</span><span class="sxs-lookup"><span data-stu-id="00999-1011">On the **Electronic reporting destination** page, add a destination record for the configured **Questionnaire report** ER format.</span></span>
3. <span data-ttu-id="00999-1012">**ファイルの送信先** クイックタブで、構成済み ER フォーマット **アンケート レポート** のルート要素として [追加された](#AddFormatRootElement)**レポート** フォーマット コンポーネントの [送信先](er-destination-type-screen.md)**画面** を設定します。</span><span class="sxs-lookup"><span data-stu-id="00999-1012">On the **File destination** FastTab, set up the **Screen** [destination](er-destination-type-screen.md) for the **Report** format component that has been [added](#AddFormatRootElement) as the root element of the configured **Questionnaire report** ER format.</span></span>
4. <span data-ttu-id="00999-1013">**PDF 変換設定** ファストタブで、送信先の構成を行い、レポートの印刷の向きを **横方向** に設定した[PDF フォーマット](electronic-reporting-destinations.md#OutputConversionToPDF)へと変換します。</span><span class="sxs-lookup"><span data-stu-id="00999-1013">On the **PDF conversion settings** FastTab, configure the destination to convert a report to [PDF format](electronic-reporting-destinations.md#OutputConversionToPDF) that uses the **Landscape** page orientation.</span></span>

![電子レポートのカスタム画面送信先を設定して ER フォーマットの送信先を構成する](./media/er-quick-start1-destination.png)

### <a name="run-a-format-from-the-application-to-preview-it-as-a-pdf-document"></a><a name="RunFormatFromApp3"></a><span data-ttu-id="00999-1015">アプリケーションからフォーマットを実行して、PDF ドキュメントでプレビューする</span><span class="sxs-lookup"><span data-stu-id="00999-1015">Run a format from the application to preview it as a PDF document</span></span>

1. <span data-ttu-id="00999-1016">**アンケート** \> **デザイン** \> **アンケート レポート (ER による実行)** に移動します。</span><span class="sxs-lookup"><span data-stu-id="00999-1016">Go to **Questionnaire** \> **Design** \> **Questionnaires report (powered by ER)**.</span></span>
2. <span data-ttu-id="00999-1017">ダイアログボックスの **フォーマットのマッピング** フィールドで、**アンケート レポート** を選択します。</span><span class="sxs-lookup"><span data-stu-id="00999-1017">In the dialog box, in the **Format mapping** field, select **Questionnaires report**.</span></span>
3. <span data-ttu-id="00999-1018">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="00999-1018">Select **OK**.</span></span>
4. <span data-ttu-id="00999-1019">**電子レポート** ダイアログ ボックスの **含めるレコード** クイックタブに、**SBCCrsExam** アンケートのみが含まれるようにフィルター処理オプションを構成します。</span><span class="sxs-lookup"><span data-stu-id="00999-1019">In the **Electronic report parameters** dialog box, on the **Records to include** FastTab, configure the filtering option so that only the **SBCCrsExam** questionnaire is included.</span></span>
5. <span data-ttu-id="00999-1020">**OK** を選択してオプションを確認します。</span><span class="sxs-lookup"><span data-stu-id="00999-1020">Select **OK** to confirm the filtering option.</span></span>

    <span data-ttu-id="00999-1021">**宛先** クイック タブで、**出力** フィールドが  **画面** に設定されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="00999-1021">On the **Destinations** FastTab, notice that the **Output** field is set to **Screen**.</span></span> <span data-ttu-id="00999-1022">構成済の送信先を変更する場合は、**変更** を選択し ます。</span><span class="sxs-lookup"><span data-stu-id="00999-1022">If you want to change the configured destination, select **Change**.</span></span>

    ![ER レポートのランタイム ダイアログ ボックスで構成された送信先を変更する](./media/er-quick-start1-run-settings.png)

6. <span data-ttu-id="00999-1024">**OK** を選択してレポートを実行します。</span><span class="sxs-lookup"><span data-stu-id="00999-1024">Select **OK** to run the report.</span></span>
7. <span data-ttu-id="00999-1025">PDF フォーマットで生成されたレポートを確認してください。</span><span class="sxs-lookup"><span data-stu-id="00999-1025">Review the generated report in PDF format.</span></span>

    ![PDF フォーマットで生成されたレポートの画面上でのレビュー](./media/er-quick-start1-preview-PDF.png)

## <a name="additional-resources"></a><a name="References"></a><span data-ttu-id="00999-1027">追加リソース</span><span class="sxs-lookup"><span data-stu-id="00999-1027">Additional resources</span></span>

- [<span data-ttu-id="00999-1028">電子申告の概要</span><span class="sxs-lookup"><span data-stu-id="00999-1028">Electronic Reporting overview</span></span>](general-electronic-reporting.md)
- [<span data-ttu-id="00999-1029">電子報告のフォーミュラ言語</span><span class="sxs-lookup"><span data-stu-id="00999-1029">Electronic reporting formula language</span></span>](er-formula-language.md)
- [<span data-ttu-id="00999-1030">多言語レポートのデザイン</span><span class="sxs-lookup"><span data-stu-id="00999-1030">Design multilingual reports</span></span>](er-design-multilingual-reports.md)
- [<span data-ttu-id="00999-1031">電子申告フレームワーク API</span><span class="sxs-lookup"><span data-stu-id="00999-1031">ER framework API</span></span>](er-apis-app73.md)
- [<span data-ttu-id="00999-1032">CASE 関数</span><span class="sxs-lookup"><span data-stu-id="00999-1032">CASE function</span></span>](er-functions-logical-case.md)
- [<span data-ttu-id="00999-1033">CONCATENATE 関数</span><span class="sxs-lookup"><span data-stu-id="00999-1033">CONCATENATE function</span></span>](er-functions-text-concatenate.md)
- [<span data-ttu-id="00999-1034">DATETIMEFORMAT 関数</span><span class="sxs-lookup"><span data-stu-id="00999-1034">DATETIMEFORMAT function</span></span>](er-functions-datetime-datetimeformat.md)
- [<span data-ttu-id="00999-1035">FILTER 関数</span><span class="sxs-lookup"><span data-stu-id="00999-1035">FILTER function</span></span>](er-functions-list-filter.md)
- [<span data-ttu-id="00999-1036">FIRSTORNULL 関数</span><span class="sxs-lookup"><span data-stu-id="00999-1036">FIRSTORNULL function</span></span>](er-functions-list-firstornull.md)
- [<span data-ttu-id="00999-1037">FORMAT 関数</span><span class="sxs-lookup"><span data-stu-id="00999-1037">FORMAT function</span></span>](er-functions-text-format.md)
- [<span data-ttu-id="00999-1038">IF 関数</span><span class="sxs-lookup"><span data-stu-id="00999-1038">IF function</span></span>](er-functions-logical-if.md)
- [<span data-ttu-id="00999-1039">ORDERBY 関数</span><span class="sxs-lookup"><span data-stu-id="00999-1039">ORDERBY function</span></span>](er-functions-list-orderby.md)
- [<span data-ttu-id="00999-1040">SESSIONNOW 関数</span><span class="sxs-lookup"><span data-stu-id="00999-1040">SESSIONNOW function</span></span>](er-functions-datetime-sessionnow.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
