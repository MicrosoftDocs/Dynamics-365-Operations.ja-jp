---
title: "Power BI Embedded を使用したワークスペースへの分析の追加"
description: "このトピックでは、ワークスペースの分析タブで Power BI レポートを組み込む方法を説明します。"
author: tjvass
manager: AnnBe
ms.date: 06/21/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application user, IT Pro
ms.reviewer: robinr
ms.search.scope: Operations
ms.search.region: Global
ms.author: tjvass
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 029511634e56aec7fdd91bad9441cd12951fbd8d
ms.openlocfilehash: bf2c6c9be05f2b1f941d99c90a681cb9951de875
ms.contentlocale: ja-jp
ms.lasthandoff: 01/17/2018

---

# <a name="add-analytics-to-workspaces-by-using-power-bi-embedded"></a><span data-ttu-id="93e3d-103">Power BI Embedded を使用したワークスペースへの分析の追加</span><span class="sxs-lookup"><span data-stu-id="93e3d-103">Add analytics to workspaces by using Power BI Embedded</span></span>

[!include[banner](../includes/banner.md)]

> [!NOTE]
> <span data-ttu-id="93e3d-104">この機能は、Dynamics 365 for Finance and Operations (バージョン 7.2 以降) でサポートされています。</span><span class="sxs-lookup"><span data-stu-id="93e3d-104">This feature is supported in Dynamics 365 for Finance and Operations (version 7.2 and later).</span></span>

# <a name="introduction"></a><span data-ttu-id="93e3d-105">はじめに</span><span class="sxs-lookup"><span data-stu-id="93e3d-105">Introduction</span></span>
<span data-ttu-id="93e3d-106">このトピックでは、ワークスペースの [分析] タブで Microsoft Power BI レポートを組み込む方法を説明します。</span><span class="sxs-lookup"><span data-stu-id="93e3d-106">This topic shows how to embed a Microsoft Power BI report on the **Analytics** tab of a workspace.</span></span> <span data-ttu-id="93e3d-107">ここで示した例では、フリート管理アプリケーションの **予約管理** ワークスペースを拡張して、分析ワークスペースを [分析] タブに埋め込みます。</span><span class="sxs-lookup"><span data-stu-id="93e3d-107">For the example that is given here, we will extend the **Reservation management** workspace in the Fleet Management application to embed an analytical workspace on an **Analytics** tab.</span></span>

# <a name="prerequisites"></a><span data-ttu-id="93e3d-108">前提条件</span><span class="sxs-lookup"><span data-stu-id="93e3d-108">Prerequisites</span></span>
+ <span data-ttu-id="93e3d-109">プラットフォーム更新プログラム 8 以降を実行する開発環境へのアクセス。</span><span class="sxs-lookup"><span data-stu-id="93e3d-109">Access to a developer environment that runs Platform update 8 or later.</span></span>
+ <span data-ttu-id="93e3d-110">Microsoft Power BI Desktop を使用して作成され、Entity ストア データベースから取得されたデータ モデルを持つ分析レポート (.pbix ファイル)。</span><span class="sxs-lookup"><span data-stu-id="93e3d-110">An analytical report (.pbix file) that was created by using Microsoft Power BI Desktop, and that has a data model that is sourced from the Entity store database.</span></span>

# <a name="overview"></a><span data-ttu-id="93e3d-111">概要</span><span class="sxs-lookup"><span data-stu-id="93e3d-111">Overview</span></span>
<span data-ttu-id="93e3d-112">既存のアプリケーション ワークスペースを拡張する場合でも、自分の新しいワークスペースを導入する場合でも、埋め込み分析ビューを使用して、ビジネス データの洞察的でインタラクティブなビューを提供できます。</span><span class="sxs-lookup"><span data-stu-id="93e3d-112">Whether you extend an existing application workspace or introduce a new workspace of your own, you can use embedded analytical views to deliver insightful and interactive views of your business data.</span></span> <span data-ttu-id="93e3d-113">分析ワークスペース タブを追加するプロセスには、4 つのステップがあります。</span><span class="sxs-lookup"><span data-stu-id="93e3d-113">The process for adding an analytical workspace tab has four steps.</span></span>

1. <span data-ttu-id="93e3d-114">Dynamics 365 リソースとして .pbix ファイルを追加します。</span><span class="sxs-lookup"><span data-stu-id="93e3d-114">Add a .pbix file as a Dynamics 365 resource.</span></span>
2. <span data-ttu-id="93e3d-115">分析ワークスペース タブを定義します。</span><span class="sxs-lookup"><span data-stu-id="93e3d-115">Define an analytical workspace tab.</span></span>
3. <span data-ttu-id="93e3d-116">ワークスペース タブに .pbix リソースを埋め込みます。</span><span class="sxs-lookup"><span data-stu-id="93e3d-116">Embed the .pbix resource on the workspace tab.</span></span>
4. <span data-ttu-id="93e3d-117">オプション: 表示をカスタマイズする拡張機能を追加します。</span><span class="sxs-lookup"><span data-stu-id="93e3d-117">Optional: Add extensions to customize the view.</span></span>

> [!NOTE]
> <span data-ttu-id="93e3d-118">分析レポートを作成する方法の詳細については、[Power BI デスクトップの使い方](https://powerbi.microsoft.com/en-us/documentation/powerbi-desktop-getting-started/)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="93e3d-118">For more information about how to create analytical reports, see [Getting started with Power BI Desktop](https://powerbi.microsoft.com/en-us/documentation/powerbi-desktop-getting-started/).</span></span> <span data-ttu-id="93e3d-119">このページは、魅力的な分析レポート作成ソリューションの作成に役立つ素晴らしいソースです。</span><span class="sxs-lookup"><span data-stu-id="93e3d-119">This page is a great source for insights that can help you create compelling analytical reporting solutions.</span></span>

# <a name="add-a-pbix-file-as-a-resource"></a><span data-ttu-id="93e3d-120">リソースとして .pbix ファイルを追加します。</span><span class="sxs-lookup"><span data-stu-id="93e3d-120">Add a .pbix file as a resource</span></span>
<span data-ttu-id="93e3d-121">開始する前に、ワークスペースに埋め込む Power BI レポートを作成または取得する必要があります。</span><span class="sxs-lookup"><span data-stu-id="93e3d-121">Before you begin, you must create or obtain the Power BI report that you will embed in the workspace.</span></span> <span data-ttu-id="93e3d-122">分析レポートを作成する方法の詳細については、[Power BI デスクトップの使い方](https://powerbi.microsoft.com/en-us/documentation/powerbi-desktop-getting-started/)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="93e3d-122">For more information about how to create analytical reports, see [Getting started with Power BI Desktop](https://powerbi.microsoft.com/en-us/documentation/powerbi-desktop-getting-started/).</span></span>
 
<span data-ttu-id="93e3d-123">.pbix ファイルを Visual Studio プロジェクト コンポーネントとして追加するには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="93e3d-123">Follow these steps to add a .pbix file as a Visual Studio project artifact.</span></span>

1. <span data-ttu-id="93e3d-124">該当するモデルで新しいプロジェクトを作成します。</span><span class="sxs-lookup"><span data-stu-id="93e3d-124">Create a new project in the appropriate model.</span></span>
2. <span data-ttu-id="93e3d-125">ソリューション エクスプローラーで、プロジェクトを選択し、右クリックした後に、[追加] > [新しい品目] の順に選択します。</span><span class="sxs-lookup"><span data-stu-id="93e3d-125">In Solution Explorer, select the project, right-click, and then select **Add** > **New Item**.</span></span>
3. <span data-ttu-id="93e3d-126">[新しい項目の追加] ダイアログ ボックスの [工程コンポーネント] で [リソース] テンプレートを選択します。</span><span class="sxs-lookup"><span data-stu-id="93e3d-126">In the **Add New Item** dialog box, under **Operations Artifacts**, select the **Resource** template.</span></span>
4. <span data-ttu-id="93e3d-127">X++ メタデータのレポートを参照するために使用する名前を入力し、[追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="93e3d-127">Enter a name that will be used to reference the report in X++ metadata, and then click **Add**.</span></span>

    ![[新しい項目の追加] ダイアログ ボックスの追加](media/analytical-workspace-add.png)

5. <span data-ttu-id="93e3d-129">分析のレポートの定義を含む .pbix ファイルを見つけて、[未処理] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="93e3d-129">Find the .pbix file that contains the definition of the analytical report, and then click **Open**.</span></span>

    ![[リソース ファイル] ダイアログ ボックスをオンにします。](media/analytical-workspace-select-resource.png)
  
<span data-ttu-id="93e3d-131">Dynamics 365 リソースとして .pbix ファイルを追加したため、ワークスペースにレポートを埋め込み、メニュー項目を使用して直接リンクを追加できるようになりました。</span><span class="sxs-lookup"><span data-stu-id="93e3d-131">Now that you've added the .pbix file as a Dynamics 365 resource, you can embed the reports in workspaces and add direct links by using menu items.</span></span>

# <a name="add-a-tab-control-to-an-application-workspace"></a><span data-ttu-id="93e3d-132">アプリケーション ワークスペースへのタブ コントロールの追加</span><span class="sxs-lookup"><span data-stu-id="93e3d-132">Add a tab control to an application workspace</span></span>
<span data-ttu-id="93e3d-133">この例では、**FMClerkWorkspace** フォームの定義に [分析] タブを追加することで、フリート管理モデルの **引当管理** ワークスペースを拡張します。</span><span class="sxs-lookup"><span data-stu-id="93e3d-133">In this example, we will extend the **Reservation management** workspace in the Fleet Management model by adding the **Analytics** tab to the definition of the **FMClerkWorkspace** form.</span></span>
 
<span data-ttu-id="93e3d-134">次の図は、**FMClerkWorkspace** フォームが Microsoft Visual Studio のデザイナーにどのように表示されるかを示しています。</span><span class="sxs-lookup"><span data-stu-id="93e3d-134">The following illustration shows what the **FMClerkWorkspace** form looks like in the designer in Microsoft Visual Studio.</span></span>

![変更する前の FMClerkWorkspace フォーム](media/analytical-workspace-definition-before.png)

<span data-ttu-id="93e3d-136">次の手順に従って、**引当管理**ワークスペースの定義を拡張します。</span><span class="sxs-lookup"><span data-stu-id="93e3d-136">Follow these steps to extend the form definition for the **Reservation management** workspace.</span></span>

1. <span data-ttu-id="93e3d-137">デザイン定義を拡張するフォーム デザイナーを開きます。</span><span class="sxs-lookup"><span data-stu-id="93e3d-137">Open the form designer to extend the design definition.</span></span>
2. <span data-ttu-id="93e3d-138">設計の定義では、[デザイン | パターン: 操作ワークスペース] というラベルが付いた最上位の要素を選択します。</span><span class="sxs-lookup"><span data-stu-id="93e3d-138">In the design definition, select the top element that is labeled **Design | Pattern: Workspace Operational**.</span></span>
3. <span data-ttu-id="93e3d-139">[新規] > [タブ] の順に右クリックし、選択し、**FormTabControl1** という名前の新しいコントロールを追加します。</span><span class="sxs-lookup"><span data-stu-id="93e3d-139">Right-click, and then select **New** > **Tab** to add a new control that is named **FormTabControl1**.</span></span>
4. <span data-ttu-id="93e3d-140">フォーム デザイナーで **FormTabControl1** を選択します。</span><span class="sxs-lookup"><span data-stu-id="93e3d-140">In the form designer, select **FormTabControl1**.</span></span>
5. <span data-ttu-id="93e3d-141">、[新しいタブ ページ] を右クリックし、選択し、新しいタブ ページを追加します。</span><span class="sxs-lookup"><span data-stu-id="93e3d-141">Right-click, and then select **New Tab Page** to add a new tab page.</span></span>
6. <span data-ttu-id="93e3d-142">**ワークスペース**など、タブ ページをわかりやすい名前に変更します。</span><span class="sxs-lookup"><span data-stu-id="93e3d-142">Rename the tab page to something meaningful, such as **Workspace**.</span></span>
7. <span data-ttu-id="93e3d-143">フォーム デザイナーで **FormTabControl1** を選択します。</span><span class="sxs-lookup"><span data-stu-id="93e3d-143">In the form designer, select **FormTabControl1**.</span></span>
8. <span data-ttu-id="93e3d-144">[新しいタブ ページ] を右クリックし、選択します。</span><span class="sxs-lookup"><span data-stu-id="93e3d-144">Right-click, and then select **New Tab Page**.</span></span>
9. <span data-ttu-id="93e3d-145">**分析**など、タブ ページをわかりやすい名前に変更します。</span><span class="sxs-lookup"><span data-stu-id="93e3d-145">Rename the tab page to something meaningful, such as **Analytics**.</span></span>
10. <span data-ttu-id="93e3d-146">フォーム デザイナーで、[分析 (タブ ページ)] を選択します。</span><span class="sxs-lookup"><span data-stu-id="93e3d-146">In the form designer, select **Analytics (Tab Page)**.</span></span>
11. <span data-ttu-id="93e3d-147">[キャプション] プロパティを**分析**に設定します。</span><span class="sxs-lookup"><span data-stu-id="93e3d-147">Set the **Caption** property to **Analytics**.</span></span>
12. <span data-ttu-id="93e3d-148">コントロールを右クリックし、[新規] > [グループ] の順に選択し、新しいフォーム グループ コントロールを追加します。</span><span class="sxs-lookup"><span data-stu-id="93e3d-148">Right-click the control, and then select **New** > **Group** to add a new form group control.</span></span>
13. <span data-ttu-id="93e3d-149">**powerBIReportGroup** など、フォーム グループをわかりやすい名前に変更します。</span><span class="sxs-lookup"><span data-stu-id="93e3d-149">Rename the form group to something meaningful, such as **powerBIReportGroup**.</span></span>
14. <span data-ttu-id="93e3d-150">フォーム デザイナーで、[PanoramaBody (タブ)] を選択し、コントロールを**ワークスペース**タブの上にドラッグします。</span><span class="sxs-lookup"><span data-stu-id="93e3d-150">In the form designer, select **PanoramaBody (Tab)**, and then drag the control onto the **Workspace** tab.</span></span>
15. <span data-ttu-id="93e3d-151">設計の定義では、[デザイン | パターン: 操作ワークスペース] というラベルが付いた最上位の要素を選択します。</span><span class="sxs-lookup"><span data-stu-id="93e3d-151">In the design definition, select the top element that is labeled **Design | Pattern: Workspace Operational**.</span></span>
16. <span data-ttu-id="93e3d-152">[パターンの削除] を右クリックし、選択します。</span><span class="sxs-lookup"><span data-stu-id="93e3d-152">Right-click, and then select **Remove pattern**.</span></span>
17. <span data-ttu-id="93e3d-153">[パターンの追加] > [ワークスペース タブ] の順にもう一度右クリックし、選択します。</span><span class="sxs-lookup"><span data-stu-id="93e3d-153">Right-click again, and then select **Add pattern** > **Workspace Tabbed**.</span></span>
18. <span data-ttu-id="93e3d-154">変更を確認するビルドを実行します。</span><span class="sxs-lookup"><span data-stu-id="93e3d-154">Perform a build to verify your changes.</span></span>
 
<span data-ttu-id="93e3d-155">次の図は、これらの変更が適用された後に設計がどのように表示されるかを示します。</span><span class="sxs-lookup"><span data-stu-id="93e3d-155">The following illustration shows what the design looks like after these changes are applied.</span></span>

![変更後の FMClerkWorkspace](media/analytical-workspace-definition-after.png)

<span data-ttu-id="93e3d-157">ワークスペース レポートの埋め込みに使用するフォーム コントロールを追加したため、親コントロールのサイズがレイアウトに対応できるように、それを定義する必要があります。</span><span class="sxs-lookup"><span data-stu-id="93e3d-157">Now that you've added the form controls that will be used to embed the workspace report, you must define the size of the parent control so that it accommodates the layout.</span></span> <span data-ttu-id="93e3d-158">既定では、[フィルタ ウィンドウ] ページと [タブ] ページの両方がレポートに表示されます。</span><span class="sxs-lookup"><span data-stu-id="93e3d-158">By default, both the **Filters Pane** page and the **Tab** page will be visible on the report.</span></span> <span data-ttu-id="93e3d-159">ただし、これらのコントロールの表示/非表示を、レポートの対象となる消費者の必要に応じて変更することができます。</span><span class="sxs-lookup"><span data-stu-id="93e3d-159">However, you can change the visibility of these controls as appropriate for the target consumer of the report.</span></span>
 
> [!NOTE]
> <span data-ttu-id="93e3d-160">埋め込みのワークスペースについては、ページの一貫性を保つため、拡張機能を使用して、[フィルタ ウィンドウ] および [タブ] ページを非表示にすることをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="93e3d-160">For embedded workspaces, we recommend that you use extensions to hide both the **Filters Pane** and **Tab** pages, for consistency.</span></span>
 
<span data-ttu-id="93e3d-161">これでアプリケーション フォームの定義を拡張するためのタスクが完了しました。</span><span class="sxs-lookup"><span data-stu-id="93e3d-161">You've now completed the task of extending the application form definition.</span></span> <span data-ttu-id="93e3d-162">カスタマイズを行うために拡張機能を使用する方法に関する詳細については、[カスタマイズ: オーバーレイおよび拡張機能](../extensibility/customization-overlayering-extensions.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="93e3d-162">For more information about how to use extensions to do customizations, see  [Customization: Overlayering and extensions](../extensibility/customization-overlayering-extensions.md).</span></span>

# <a name="add-x-business-logic-to-embed-a-viewer-control"></a><span data-ttu-id="93e3d-163">ビューアー コントロールを埋め込むための X++ ビジネス ロジックの追加</span><span class="sxs-lookup"><span data-stu-id="93e3d-163">Add X++ business logic to embed a viewer control</span></span>
<span data-ttu-id="93e3d-164">これらの手順に従い、**引当管理** ワークスペースに埋め込まれているレポート ビューアー コントロールを初期化するビジネス ロジックを追加します。</span><span class="sxs-lookup"><span data-stu-id="93e3d-164">Follow these steps to add business logic that initializes the report viewer control that is embedded in the **Reservation management** workspace.</span></span>

1. <span data-ttu-id="93e3d-165">[FMClerkWorkspace] フォーム デザイナーを開き、デザイン定義を拡張します。</span><span class="sxs-lookup"><span data-stu-id="93e3d-165">Open the **FMClerkWorkspace** form designer to extend the design definition.</span></span>
2. <span data-ttu-id="93e3d-166">F7 キーを押し、コードの定義の背後にあるコードにアクセスします。</span><span class="sxs-lookup"><span data-stu-id="93e3d-166">Press F7 to access the code behind the code definition.</span></span>
3. <span data-ttu-id="93e3d-167">次の X++ コードを追加します。</span><span class="sxs-lookup"><span data-stu-id="93e3d-167">Add the following X++ code.</span></span>

    ```
    [Form] 
    public class FMClerkWorkspace extends FormRun
    {
        private boolean initReportControl = true;     
        protected void initAnalyticalReport()
        {
            if (!initReportControl)
            {
                return;
            }
            // Note: secure entry point into the Workspace's Analytics report
            if (Global::hasMenuItemAccess(menuItemDisplayStr(FMClerkWorkspace), MenuItemType::Display))
            {
                FMPBIWorkspaceController controller = new FMPBIWorkspaceController();
                PBIReportHelper::initializeReportControl('FMPBIWorkspaces', powerBIReportGroup);
            }
            initReportControl = false;
    }
        /// <summary>
        /// Initializes the form.
        /// </summary>
        public void init()
        {
            super();
            this.initAnalyticalReport();
        }
    }
    ```

4. <span data-ttu-id="93e3d-168">変更を確認するビルドを実行します。</span><span class="sxs-lookup"><span data-stu-id="93e3d-168">Perform a build to verify your changes.</span></span>

<span data-ttu-id="93e3d-169">これで、埋め込みレポート ビューアー コントロールを初期化するビジネス ロジックを追加するタスクを完了しました。</span><span class="sxs-lookup"><span data-stu-id="93e3d-169">You've now completed the task of adding business logic to initialize the embedded report viewer control.</span></span> <span data-ttu-id="93e3d-170">次の図は、これらの変更が適用された後にワークスペースがどのように表示されるかを示します。</span><span class="sxs-lookup"><span data-stu-id="93e3d-170">The following illustration shows what the workspace looks like after these changes are applied.</span></span>

![ワークスペースに埋め込まれているレポート](media/analytical-workspace-final.png)

> [!NOTE]
> <span data-ttu-id="93e3d-172">既存の操作ビューは、ページのタイトルの下のワークスペース タブを使用してアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="93e3d-172">You can access the existing operational view by using the workspace tabs below the page title.</span></span>

# <a name="reference"></a><span data-ttu-id="93e3d-173">参照</span><span class="sxs-lookup"><span data-stu-id="93e3d-173">Reference</span></span>

## <a name="pbireporthelperinitializereportcontrol-method"></a><span data-ttu-id="93e3d-174">PBIReportHelper.initializeReportControl 方法</span><span class="sxs-lookup"><span data-stu-id="93e3d-174">PBIReportHelper.initializeReportControl method</span></span>
<span data-ttu-id="93e3d-175">このセクションでは、フォーム グループ コントロールで Power BI レポート (.pbix リソース) の埋め込みに使用されるヘルパー クラスに関する情報を提供します。</span><span class="sxs-lookup"><span data-stu-id="93e3d-175">This section provides information about the helper class that is used to embed a Power BI report (.pbix resource) in a form group control.</span></span>

### <a name="syntax"></a><span data-ttu-id="93e3d-176">構文</span><span class="sxs-lookup"><span data-stu-id="93e3d-176">Syntax</span></span>
```
public static void initializeReportControl(
     str                 _resourceName,
     FormGroupControl    _formGroupControl,
     str                 _defaultPageName = '',
     boolean             _showFilterPane = false,
     boolean             _showNavPane = false,
     List                _defaultFilters = new List(Types::Class))
```

### <a name="parameters"></a><span data-ttu-id="93e3d-177">パラメーター</span><span class="sxs-lookup"><span data-stu-id="93e3d-177">Parameters</span></span>

| <span data-ttu-id="93e3d-178">氏名</span><span class="sxs-lookup"><span data-stu-id="93e3d-178">Name</span></span> | <span data-ttu-id="93e3d-179">説明</span><span class="sxs-lookup"><span data-stu-id="93e3d-179">Description</span></span> |
|---|---|
| <span data-ttu-id="93e3d-180">resourceName</span><span class="sxs-lookup"><span data-stu-id="93e3d-180">resourceName</span></span> | <span data-ttu-id="93e3d-181">.pbix リソースの名前。</span><span class="sxs-lookup"><span data-stu-id="93e3d-181">The name of the .pbix resource.</span></span> |
| <span data-ttu-id="93e3d-182">formGroupControl</span><span class="sxs-lookup"><span data-stu-id="93e3d-182">formGroupControl</span></span> | <span data-ttu-id="93e3d-183">Power BI レポートのコントロール適用先のフォーム グループ コントロール。</span><span class="sxs-lookup"><span data-stu-id="93e3d-183">The form group control to apply the Power BI report control to.</span></span> |
| <span data-ttu-id="93e3d-184">defaultPageName</span><span class="sxs-lookup"><span data-stu-id="93e3d-184">defaultPageName</span></span> | <span data-ttu-id="93e3d-185">既定のページの名前</span><span class="sxs-lookup"><span data-stu-id="93e3d-185">The default page name.</span></span> |
| <span data-ttu-id="93e3d-186">showFilterPane</span><span class="sxs-lookup"><span data-stu-id="93e3d-186">showFilterPane</span></span> | <span data-ttu-id="93e3d-187">フィルタ ウィンドウを表示 (**true**) または非表示 (**false**) するかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="93e3d-187">A Boolean value that indicates whether the filter pane should be shown (**true**) or hidden (**false**).</span></span> |
| <span data-ttu-id="93e3d-188">showNavPane</span><span class="sxs-lookup"><span data-stu-id="93e3d-188">showNavPane</span></span> | <span data-ttu-id="93e3d-189">ナビゲーション ウィンドウを表示 (**true**) または非表示 (**false**) するかを示すブール値。</span><span class="sxs-lookup"><span data-stu-id="93e3d-189">A Boolean value that indicates whether the navigation pane should be shown (**true**) or hidden (**false**).</span></span> |
| <span data-ttu-id="93e3d-190">defaultFilters</span><span class="sxs-lookup"><span data-stu-id="93e3d-190">defaultFilters</span></span> | <span data-ttu-id="93e3d-191">Power BI レポートの既定のフィルター。</span><span class="sxs-lookup"><span data-stu-id="93e3d-191">The default filters for the Power BI report.</span></span> |

