---
title: "ワークスペースの構築"
description: "このチュートリアルでは、新しいタイルを作成し、ワークスペースの概要にそれを含め、ワークスペースの新しいリストを構築して、ワークスペースにリストのデータ キャッシュを作成します。"
author: jasongre
manager: AnnBe
ms.date: 08/25/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Developer
ms.reviewer: robinr
ms.search.scope: Operations
ms.custom: 10794
ms.assetid: fe596786-c229-47b5-af0a-6022569ebee8
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 786474f093d8a394c2a975b129132f9a4a243a74
ms.contentlocale: ja-jp
ms.lasthandoff: 05/08/2018

---

# <a name="build-a-workspace"></a><span data-ttu-id="978fa-103">ワークスペースの構築</span><span class="sxs-lookup"><span data-stu-id="978fa-103">Build a workspace</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="978fa-104">このチュートリアルでは、新しいタイルを作成し、ワークスペースの概要にそれを含め、ワークスペースの新しいリストを構築して、ワークスペースにリストのデータ キャッシュを作成します。</span><span class="sxs-lookup"><span data-stu-id="978fa-104">In this tutorial, you will create a new tile and include it in the summary section of a workspace, build a new list for a workspace, and create a data cache for the list in the workspace.</span></span>

<a name="prerequisites"></a><span data-ttu-id="978fa-105">前提条件</span><span class="sxs-lookup"><span data-stu-id="978fa-105">Prerequisites</span></span>
-------------

<span data-ttu-id="978fa-106">このチュートリアルでは、リモート デスクトップを使用して Microsoft Dynamics AX 環境にアクセスし、Dynamics AX インスタンスの管理者としてプロビジョニングされる必要があります。</span><span class="sxs-lookup"><span data-stu-id="978fa-106">For this tutorial, you must access the Microsoft Dynamics AX environment by using Remote Desktop, and you must be provisioned as an administrator on the Dynamics AX instance.</span></span> <span data-ttu-id="978fa-107">詳細については、[Microsoft Dynamics AX インスタンスへのアクセス](../dev-tools/access-instances.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="978fa-107">For more information, see [Access Microsoft Dynamics AX Instances](../dev-tools/access-instances.md).</span></span>

## <a name="key-concepts"></a><span data-ttu-id="978fa-108">重要な概念</span><span class="sxs-lookup"><span data-stu-id="978fa-108">Key concepts</span></span>
-   <span data-ttu-id="978fa-109">ワークスペースに関連付けられているフォーム パターンについて学んで使用します。</span><span class="sxs-lookup"><span data-stu-id="978fa-109">Learn about and use form patterns that are related to workspaces.</span></span>
-   <span data-ttu-id="978fa-110">新しいタイルを作成し、それをワークスペースの**集計**セクションに含めます。</span><span class="sxs-lookup"><span data-stu-id="978fa-110">Create a new tile, and include it in the **Summary** section of a workspace.</span></span>
-   <span data-ttu-id="978fa-111">ワークスペースの新しいリストをビルドします。</span><span class="sxs-lookup"><span data-stu-id="978fa-111">Build a new list for a workspace.</span></span>
-   <span data-ttu-id="978fa-112">リストのデータ キャッシュをワークスペースに作成します。</span><span class="sxs-lookup"><span data-stu-id="978fa-112">Create a data cache for the list in the workspace.</span></span>

## <a name="setup"></a><span data-ttu-id="978fa-113">段取り</span><span class="sxs-lookup"><span data-stu-id="978fa-113">Setup</span></span>
### <a name="import-the-tutorial-project-and-transactional-data"></a><span data-ttu-id="978fa-114">チュートリアル プロジェクトおよびトランザクション データのインポート</span><span class="sxs-lookup"><span data-stu-id="978fa-114">Import the tutorial project and transactional data</span></span>

<span data-ttu-id="978fa-115">Microsoft Visual Studio を使用して、チュートリアル プロジェクトをインポートします。</span><span class="sxs-lookup"><span data-stu-id="978fa-115">Use Microsoft Visual Studio to import the tutorial project.</span></span> <span data-ttu-id="978fa-116">チュートリアル プロジェクトには、このチュートリアルを完了するために使用する成果物が含まれています。</span><span class="sxs-lookup"><span data-stu-id="978fa-116">The tutorial project includes the artifacts that you will use to complete this tutorial.</span></span> <span data-ttu-id="978fa-117">Visual Studio を使用して FMTutorial プロジェクトを開き、チュートリアル用のデータを読み込みます。</span><span class="sxs-lookup"><span data-stu-id="978fa-117">Use Visual Studio to open the FMTutorial project and load the data for the tutorial.</span></span> <span data-ttu-id="978fa-118">フリート管理チュートリアルのデータを読み込むために、**FMTDataHelper** クラスを使用します。</span><span class="sxs-lookup"><span data-stu-id="978fa-118">You will use the **FMTDataHelper** class to load data for the Fleet Management tutorial.</span></span> <span data-ttu-id="978fa-119">これが作業する最初のチュートリアルである場合は、[アクセス Microsoft Dynamics AX インスタンス](../dev-tools/access-instances.md)を確認し、ローカル 仮想マシン (VM) で作業している場合に、管理者ユーザーを提供するかどうかを確認します。</span><span class="sxs-lookup"><span data-stu-id="978fa-119">If this is the first tutorial that you’re working on, review [Access Microsoft Dynamics AX Instances](../dev-tools/access-instances.md), and make sure that you provision your administrator user if you’re working on a local virtual machine (VM).</span></span>

1.  <span data-ttu-id="978fa-120">Microsoft Dynamics Lifecycle Services (LCS) 方法から **FMTutorialDataModel.axpp** ファイルをダウンロードし、VM の **Downloads** フォルダーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="978fa-120">Download the **FMTutorialDataModel.axpp** file from the Microsoft Dynamics Lifecycle Services (LCS) methodology, and copy it to the **Downloads** folder of the VM.</span></span>
2.  <span data-ttu-id="978fa-121">デスクトップで、Visual Studio ショートカットをダブルクリックして、開発環境を開きます。</span><span class="sxs-lookup"><span data-stu-id="978fa-121">On the desktop, double-click the Visual Studio shortcut to open the development environment.</span></span>
3.  <span data-ttu-id="978fa-122">**Dynamics AX** メニューで、**プロジェクトのインポート**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="978fa-122">On the **Dynamics AX** menu, click **Import Project**.</span></span>
4.  <span data-ttu-id="978fa-123">**プロジェクトのインポート** ダイアログ ボックスで、**ファイル名**フィールドの隣にある、省略記号 (**...**) ボタンをクリックします。</span><span class="sxs-lookup"><span data-stu-id="978fa-123">In the **Import Project** dialog box, next to the **File name** field, click the ellipsis (**...**) button.</span></span>
5.  <span data-ttu-id="978fa-124">**インポートするファイルの選択**ダイアログ ボックスで、**ダウンロード** フォルダーを参照して **FMTutorialDataModel.axpp** をクリックしてから**開く**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="978fa-124">In the **Select the file to import** dialog box, browse to the **Downloads** folder, click **FMTutorialDataModel.axpp**, and then click **Open**.</span></span>
6.  <span data-ttu-id="978fa-125">**要素の上書き** チェック ボックスをオンにし、**現在のソリューション** オプションをオンにします。</span><span class="sxs-lookup"><span data-stu-id="978fa-125">Select the **Overwrite Elements** check box and the **Current solution** option.</span></span> <span data-ttu-id="978fa-126">次の図は、完了した **インポート プロジェクト** ダイアログ ボックスを示しています。</span><span class="sxs-lookup"><span data-stu-id="978fa-126">The following illustration shows the completed **Import Project** dialog box.</span></span> 

    <span data-ttu-id="978fa-127">[![プロジェクトのインポート](./media/importproject1.png)](./media/importproject1.png)</span><span class="sxs-lookup"><span data-stu-id="978fa-127">[![Import project](./media/importproject1.png)](./media/importproject1.png)</span></span>

7.  <span data-ttu-id="978fa-128">**OK** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="978fa-128">Click **OK**.</span></span>
8.  <span data-ttu-id="978fa-129">ソリューション エクスプローラーで**クラス**を展開して、**FMTutorial** プロジェクトで **FMTDataHelper** を右クリックしてから、**スタートアップ オブジェクトとして設定**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="978fa-129">In Solution Explorer, expand **Classes**, and then, under the **FMTutorial** project, right-click **FMTDataHelper**, and then click **Set as Startup Object**.</span></span>
9.  <span data-ttu-id="978fa-130">**ビルド**メニューで、**ソリューションの再構築**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="978fa-130">On the **Build** menu, click **Rebuild Solution**.</span></span> <span data-ttu-id="978fa-131">タイムスタンプに関係なく、プロジェクトのすべてのファイルを確実に作成するには、リビルドを使用します。</span><span class="sxs-lookup"><span data-stu-id="978fa-131">Use the rebuild to make sure that all the files in the project are built, regardless of timestamps.</span></span> <span data-ttu-id="978fa-132">**出力** ウィンドウでビルドの進行状況を表示できます。</span><span class="sxs-lookup"><span data-stu-id="978fa-132">You can view the build progress in the **Output** window.</span></span>
10. <span data-ttu-id="978fa-133">ビルドが完了した後、**Ctrl + F5** を押してプロジェクトを実行します。</span><span class="sxs-lookup"><span data-stu-id="978fa-133">After the build is completed, press **Ctrl+F5** to run the project.</span></span> <span data-ttu-id="978fa-134">ブラウザーが開き、データをインポートするクラスが実行されます。</span><span class="sxs-lookup"><span data-stu-id="978fa-134">The browser opens and runs the class that imports the data.</span></span>

### <a name="open-the-fmtutorial-project"></a><span data-ttu-id="978fa-135">FMTutorial プロジェクトを開く</span><span class="sxs-lookup"><span data-stu-id="978fa-135">Open the FMTutorial project</span></span>

<span data-ttu-id="978fa-136">Visual Studio を使用して、FMTutorial プロジェクトを開きます。</span><span class="sxs-lookup"><span data-stu-id="978fa-136">Use Visual Studio to open the FMTutorial project.</span></span> <span data-ttu-id="978fa-137">Visual Studio を開き、FMTutorial プロジェクトが既に読み込まれている場合は、次のセクションに続行することができます。</span><span class="sxs-lookup"><span data-stu-id="978fa-137">If you have Visual Studio open and have already loaded the FMTutorial project, you can continue to the next section.</span></span>

1.  <span data-ttu-id="978fa-138">デスクトップ環境がまだ開かれていない場合は、Visual Studio ショートカットをデスクトップ上でダブルクリックして、開発環境を開きます。</span><span class="sxs-lookup"><span data-stu-id="978fa-138">If the development environment isn’t already open, on the desktop, double-click the Visual Studio shortcut to open it.</span></span>
2.  <span data-ttu-id="978fa-139">**ファイル**メニューで、**開く** &gt; **プロジェクト/ソリューション**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="978fa-139">On the **File** menu, click **Open** &gt; **Project/Solution**.</span></span>
3.  <span data-ttu-id="978fa-140">**プロジェクトを開く**ダイアログ ボックスで、**ドキュメント** &gt; **Visual Studio 15.0** &gt; **プロジェクト**を参照し、**FMTutorial** ソリューションを選択してから**開く**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="978fa-140">In the **Open Project** dialog box, browse to **Documents** &gt; **Visual Studio 15.0** &gt; **Projects**, select the **FMTutorial** solution, and then click **Open**.</span></span>
4.  <span data-ttu-id="978fa-141">FMTutorial プロジェクトがソリューション エクスプローラーに表示されます。</span><span class="sxs-lookup"><span data-stu-id="978fa-141">The FMTutorial project appears in Solution Explorer.</span></span>

## <a name="exercise-1-understand-the-operational-workspace-pattern"></a><span data-ttu-id="978fa-142">手順 1: 運用ワークスペースのパターンを理解</span><span class="sxs-lookup"><span data-stu-id="978fa-142">Exercise 1: Understand the Operational Workspace pattern</span></span>
<span data-ttu-id="978fa-143">**FmtClerkWorkspace** フォームを調整する前に、フォームの現在の状態を確認して既に存在するコンテンツと、その内容が運用ワークスペース パターンにどのように適合するかを理解してください。</span><span class="sxs-lookup"><span data-stu-id="978fa-143">Before you start to make adjustments to **FmtClerkWorkspace** form, you will look at the current state of the form to better understand what content is already there and how that contents fits the Operational Workspace pattern.</span></span>

1.  <span data-ttu-id="978fa-144">ソリューション エクスプローラーで、**FmtClerkWorkspace** フォームをダブルクリックしてデザイナーで開きます。</span><span class="sxs-lookup"><span data-stu-id="978fa-144">In Solution Explorer, double-click the **FmtClerkWorkspace** form to open it in the designer.</span></span>
2.  <span data-ttu-id="978fa-145">**デザイン** ノードをクリックします。</span><span class="sxs-lookup"><span data-stu-id="978fa-145">Click the **Design** node.</span></span>
3.  <span data-ttu-id="978fa-146">**パターン** タブをクリックします。運用ワークスペースにはオプションのアクション ウィンドウとオプションのフィルター グループがあります (これらのノードの左に 0..1 の表記で示されています)。</span><span class="sxs-lookup"><span data-stu-id="978fa-146">Click the **Pattern** tab. Operational workspaces have an optional Action Pane and optional filter group (as indicated by the 0..1 notation to the left of those nodes).</span></span> <span data-ttu-id="978fa-147">ただし、このパターンによってパノラマ スタイル タブが必要になります。</span><span class="sxs-lookup"><span data-stu-id="978fa-147">However, the panorama-style tab is required by this pattern.</span></span> <span data-ttu-id="978fa-148">**パターン** タブでは、PanoramaBody コントロールがパターンで必要なタブと一致していることを示しますが、このパターンのレベルでオプションの項目に対応するコントロールはないことに注意してください。</span><span class="sxs-lookup"><span data-stu-id="978fa-148">Note that the **Patterns** tab shows that the PanoramaBody control matches the required Tab in the pattern, but there are no corresponding controls for the optional items at this level of the pattern.</span></span> 

    <span data-ttu-id="978fa-149">[![稼働中のワークスペース パターン](./media/workspacepattern1.png)](./media/workspacepattern1.png)</span><span class="sxs-lookup"><span data-stu-id="978fa-149">[![Operational workspace pattern](./media/workspacepattern1.png)](./media/workspacepattern1.png)</span></span>

4.  <span data-ttu-id="978fa-150">**PanoramaBody** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="978fa-150">Click **PanoramaBody**.</span></span> 

    <span data-ttu-id="978fa-151">[![稼働中のワークスペース パターン](./media/workspacepattern2.png)](./media/workspacepattern2.png)</span><span class="sxs-lookup"><span data-stu-id="978fa-151">[![Operational workspace pattern](./media/workspacepattern2.png)](./media/workspacepattern2.png)</span></span>


<span data-ttu-id="978fa-152">すべてのワークスペースに必要な 3 つのセクションがあることに注意します。</span><span class="sxs-lookup"><span data-stu-id="978fa-152">Notice that all workspaces have three required sections:</span></span>

-   <span data-ttu-id="978fa-153">**集計セクション** – このセクションは、カードまたはグラフに対応するタイルまたはフォーム パーツを含むことを意図しています。</span><span class="sxs-lookup"><span data-stu-id="978fa-153">**Summary section** – This section is intended to contain tiles or form parts, which correspond to a card or chart.</span></span>
-   <span data-ttu-id="978fa-154">**タブ付きリスト** – このセクションでは、ユーザーの作業に関連するデータの 1 つまたは複数のリストで構成されています。</span><span class="sxs-lookup"><span data-stu-id="978fa-154">**Tabbed list** – This section consists of one or more lists of data that is relevant to the user’s work.</span></span> <span data-ttu-id="978fa-155">一度に 1 つだけ一覧が表示され、各一覧はローカル フィルターとアクションを含めることもできます。</span><span class="sxs-lookup"><span data-stu-id="978fa-155">Only one list is shown at a time, and each list can optionally include local filters and actions.</span></span> <span data-ttu-id="978fa-156">個別のリストは、フォーム パーツ コントロール内でモデル化されます。</span><span class="sxs-lookup"><span data-stu-id="978fa-156">Individual lists are modeled inside form part controls.</span></span>
-   <span data-ttu-id="978fa-157">**関連リンク** – このセクションは、この活動またはペルソナの、重要なリンクまたは一般的に使用されるリンクで構成されています。</span><span class="sxs-lookup"><span data-stu-id="978fa-157">**Related links** – This section consists of important or commonly used links for this activity or persona.</span></span>

<span data-ttu-id="978fa-158">運用ワークスペースは、最大 2 つのグラフ (セクション グラフのタブ ページ) を含むパノラマ セクションと Power BI セクションを必要に応じて含めることができます。</span><span class="sxs-lookup"><span data-stu-id="978fa-158">Operational workspaces can optionally include a panorama section that contains up to two charts (the Section Charts tab page) and a Power BI section.</span></span>

### <a name="view-the-workspace"></a><span data-ttu-id="978fa-159">ワークスペースの表示</span><span class="sxs-lookup"><span data-stu-id="978fa-159">View the workspace</span></span>

1.  <span data-ttu-id="978fa-160">ソリューション エクスプローラーで、**FmtClerkWorkspace** フォームを右クリックしてから、**スタートアップ オブジェクトとして設定**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="978fa-160">In Solution Explorer, right-click the **FmtClerkWorkspace** form, and then click **Set as Startup Object**.</span></span>
2.  <span data-ttu-id="978fa-161">**Ctrl+F5** キーを押して、フォームをビルドおよび実行します。</span><span class="sxs-lookup"><span data-stu-id="978fa-161">Press **Ctrl+F5** to build and run the form.</span></span> <span data-ttu-id="978fa-162">Internet Explorerで、フォームを開きます。</span><span class="sxs-lookup"><span data-stu-id="978fa-162">The form opens in Internet Explorer.</span></span> 

    <span data-ttu-id="978fa-163">[![フォームを開く](./media/fmtworkspaceinitial-1024x650.png)](./media/fmtworkspaceinitial.png)</span><span class="sxs-lookup"><span data-stu-id="978fa-163">[![Open form](./media/fmtworkspaceinitial-1024x650.png)](./media/fmtworkspaceinitial.png)</span></span>


## <a name="exercise-2-create-a-new-tile-for-the-workspace"></a><span data-ttu-id="978fa-164">手順 2: ワークスペースの新しいタイルを作成</span><span class="sxs-lookup"><span data-stu-id="978fa-164">Exercise 2: Create a new tile for the workspace</span></span>
<span data-ttu-id="978fa-165">ワークスペースのコンテンツ構造がわかったので、ワークスペースにコンテンツを追加する方法を見てみます。</span><span class="sxs-lookup"><span data-stu-id="978fa-165">Now that you understand the content structure of a workspace, you will see how to add content to a workspace.</span></span> <span data-ttu-id="978fa-166">たとえば、このワークスペースに対する 1 つの重要な情報は、現在進行中であるレンタル数である可能性があります。</span><span class="sxs-lookup"><span data-stu-id="978fa-166">For example, one important piece of information for this workspace might be the number of rentals that are currently in progress.</span></span> <span data-ttu-id="978fa-167">このセクションでは、**FmtClerkWorkspace** フォームの**概要**セクションに新しいタイルを追加してこの情報を表示するために必要なメタデータを追加します。</span><span class="sxs-lookup"><span data-stu-id="978fa-167">In this section, you will add the required metadata to add a new tile to the **Summary** section of the **FmtClerkWorkspace** form to show this information.</span></span> <span data-ttu-id="978fa-168">このタイルを正しく機能させるには、クエリ、メニュー項目、タイル、タイル ボタンの 4 つのメタデータ アーティファクトを追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="978fa-168">To make this tile work correctly, you will have to add four metadata artifacts: a query, a menu item, a tile, and a tile button.</span></span>

### <a name="add-a-query-that-retrieves-current-rentals"></a><span data-ttu-id="978fa-169">現在のレンタルを取得するクエリの追加</span><span class="sxs-lookup"><span data-stu-id="978fa-169">Add a query that retrieves current rentals</span></span>

<span data-ttu-id="978fa-170">すべてのタイルは、正しい情報を取得するバッキング クエリが必要です。</span><span class="sxs-lookup"><span data-stu-id="978fa-170">All tiles require a backing query to retrieve the correct information.</span></span>

1.  <span data-ttu-id="978fa-171">ソリューション エクスプローラーの **FMTutorial** プロジェクトで、**クエリ** フォルダーを右クリックし、**追加**をポイントしてから**新しい項目**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="978fa-171">In Solution Explorer, in the **FMTutorial** project, right-click the **Queries** folder, point to **Add**, and then click **New item**.</span></span>
2.  <span data-ttu-id="978fa-172">**Dynamics AX アーティファクト** &gt; **データ モデル** &gt; **クエリ**とクリックします。</span><span class="sxs-lookup"><span data-stu-id="978fa-172">Click **Dynamics AX Artifacts** &gt; **Data Model** &gt; **Query**.</span></span> <span data-ttu-id="978fa-173">**名前**プロパティについては、**FMTRental\_Current** を入力します。</span><span class="sxs-lookup"><span data-stu-id="978fa-173">For the **Name** property, enter **FMTRental\_Current**.</span></span>
3.  <span data-ttu-id="978fa-174">**追加** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="978fa-174">Click **Add**.</span></span>
4.  <span data-ttu-id="978fa-175">新しい **FMTRental\_Current** クエリーがデザイナーで開かれていない場合、ソリューション エクスプローラーでダブルクリックします。</span><span class="sxs-lookup"><span data-stu-id="978fa-175">If the new **FMTRental\_Current** query isn’t already open in the designer, double-click it in Solution Explorer.</span></span>
5.  <span data-ttu-id="978fa-176">デザイナーで、**データ ソース**を右クリックしてから**新しいデータ ソース**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="978fa-176">In the designer, right-click **Data Sources**, and then click **New Data Source**.</span></span>
6.  <span data-ttu-id="978fa-177">**プロパティ** ウィンドウで、次のプロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="978fa-177">In the **Properties** window, set the following properties.</span></span>

    | <span data-ttu-id="978fa-178">プロパティ</span><span class="sxs-lookup"><span data-stu-id="978fa-178">Property</span></span>        | <span data-ttu-id="978fa-179">先頭値</span><span class="sxs-lookup"><span data-stu-id="978fa-179">Value</span></span>     |
    |-----------------|-----------|
    | <span data-ttu-id="978fa-180">テーブル</span><span class="sxs-lookup"><span data-stu-id="978fa-180">Table</span></span>           | <span data-ttu-id="978fa-181">FMTRental</span><span class="sxs-lookup"><span data-stu-id="978fa-181">FMTRental</span></span> |
    | <span data-ttu-id="978fa-182">Dynamics フィールド</span><span class="sxs-lookup"><span data-stu-id="978fa-182">Dynamics Fields</span></span> | <span data-ttu-id="978fa-183">有</span><span class="sxs-lookup"><span data-stu-id="978fa-183">Yes</span></span>       |

7.  <span data-ttu-id="978fa-184">**範囲** を右クリックし、**新しい範囲** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="978fa-184">Right-click **Ranges**, and then click **New Range**.</span></span>
8.  <span data-ttu-id="978fa-185">**プロパティ** ウィンドウで、次のプロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="978fa-185">In the **Properties** window, set the following properties.</span></span>

    | <span data-ttu-id="978fa-186">プロパティ</span><span class="sxs-lookup"><span data-stu-id="978fa-186">Property</span></span> | <span data-ttu-id="978fa-187">先頭値</span><span class="sxs-lookup"><span data-stu-id="978fa-187">Value</span></span>      |
    |----------|------------|
    | <span data-ttu-id="978fa-188">フィールド</span><span class="sxs-lookup"><span data-stu-id="978fa-188">Field</span></span>    | <span data-ttu-id="978fa-189">行政単位 (区画)</span><span class="sxs-lookup"><span data-stu-id="978fa-189">State</span></span>      |
    | <span data-ttu-id="978fa-190">先頭値</span><span class="sxs-lookup"><span data-stu-id="978fa-190">Value</span></span>    | <span data-ttu-id="978fa-191">InProgress</span><span class="sxs-lookup"><span data-stu-id="978fa-191">InProgress</span></span> |

9.  <span data-ttu-id="978fa-192">**並べ替え** を右クリックし、**新しいフィールド** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="978fa-192">Right-click **Order By**, and then click **New Field**.</span></span>
10. <span data-ttu-id="978fa-193">**プロパティ** ウィンドウで、次のプロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="978fa-193">In the **Properties** window, set the following properties.</span></span>

    | <span data-ttu-id="978fa-194">プロパティ</span><span class="sxs-lookup"><span data-stu-id="978fa-194">Property</span></span>    | <span data-ttu-id="978fa-195">先頭値</span><span class="sxs-lookup"><span data-stu-id="978fa-195">Value</span></span>      |
    |-------------|------------|
    | <span data-ttu-id="978fa-196">方向</span><span class="sxs-lookup"><span data-stu-id="978fa-196">Direction</span></span>   | <span data-ttu-id="978fa-197">降順</span><span class="sxs-lookup"><span data-stu-id="978fa-197">Descending</span></span> |
    | <span data-ttu-id="978fa-198">データ ソース</span><span class="sxs-lookup"><span data-stu-id="978fa-198">Data Source</span></span> | <span data-ttu-id="978fa-199">FMTRental</span><span class="sxs-lookup"><span data-stu-id="978fa-199">FMTRental</span></span>  |
    | <span data-ttu-id="978fa-200">フィールド</span><span class="sxs-lookup"><span data-stu-id="978fa-200">Field</span></span>       | <span data-ttu-id="978fa-201">StartDate</span><span class="sxs-lookup"><span data-stu-id="978fa-201">StartDate</span></span>  |

11. <span data-ttu-id="978fa-202">**Ctrl+S** キーを押して保存します。</span><span class="sxs-lookup"><span data-stu-id="978fa-202">Press **Ctrl+S** to save.</span></span>

### <a name="add-the-corresponding-menu-item"></a><span data-ttu-id="978fa-203">対応するメニュー項目の追加</span><span class="sxs-lookup"><span data-stu-id="978fa-203">Add the corresponding menu item</span></span>

1. <span data-ttu-id="978fa-204">ソリューション エクスプローラーの **FMTutorial** プロジェクトで、**メニュー項目**フォルダーを右クリックし、**追加**をポイントしてから**新しい項目**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="978fa-204">In Solution Explorer, in the **FMTutorial** project, right-click the **Menu items** folder, point to **Add**, and then click **New item**.</span></span>
2. <span data-ttu-id="978fa-205">**Dynamics AX アーティファクト** &gt; **ユーザー インターフェイス** &gt; **表示メニュー項目**とクリックします。</span><span class="sxs-lookup"><span data-stu-id="978fa-205">Click **Dynamics AX Artifacts** &gt; **User Interface** &gt; **Display menu item**.</span></span> <span data-ttu-id="978fa-206">**Name** プロパティを **FMTRental\_Current** に置き換えます。</span><span class="sxs-lookup"><span data-stu-id="978fa-206">Set the **Name** property to **FMTRental\_Current**.</span></span>
3. <span data-ttu-id="978fa-207">**追加** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="978fa-207">Click **Add**.</span></span>
4. <span data-ttu-id="978fa-208">新しい **FMTRental\_Current** メニュー項目がデザイナーで開かれていない場合、ソリューション エクスプローラーでダブルクリックします。</span><span class="sxs-lookup"><span data-stu-id="978fa-208">If the new **FMTRental\_Current** menu item isn’t already open in the designer, double-click it in Solution Explorer.</span></span>
5. <span data-ttu-id="978fa-209">**プロパティ** ウィンドウで、次のプロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="978fa-209">In the **Properties** window, set the following properties.</span></span>


   | <span data-ttu-id="978fa-210">プロパティ</span><span class="sxs-lookup"><span data-stu-id="978fa-210">Property</span></span> |                                    <span data-ttu-id="978fa-211">先頭値</span><span class="sxs-lookup"><span data-stu-id="978fa-211">Value</span></span>                                    |
   |----------|-----------------------------------------------------------------------------|
   |  <span data-ttu-id="978fa-212">ラベル</span><span class="sxs-lookup"><span data-stu-id="978fa-212">Label</span></span>   | <span data-ttu-id="978fa-213">@FMT197<strong>注記:</strong> この値が「現在のレンタル」に対応します。</span><span class="sxs-lookup"><span data-stu-id="978fa-213">@FMT197 <strong>Note:</strong> This value corresponds to “Current rentals”.</span></span> |
   |  <span data-ttu-id="978fa-214">オブジェクト</span><span class="sxs-lookup"><span data-stu-id="978fa-214">Object</span></span>  |                                  <span data-ttu-id="978fa-215">FMTRental</span><span class="sxs-lookup"><span data-stu-id="978fa-215">FMTRental</span></span>                                  |
   |  <span data-ttu-id="978fa-216">クエリ</span><span class="sxs-lookup"><span data-stu-id="978fa-216">Query</span></span>   |                             <span data-ttu-id="978fa-217">FMTRental\_Current</span><span class="sxs-lookup"><span data-stu-id="978fa-217">FMTRental\_Current</span></span>                              |


6. <span data-ttu-id="978fa-218">**Ctrl+S** キーを押して保存します。</span><span class="sxs-lookup"><span data-stu-id="978fa-218">Press **Ctrl+S** to save.</span></span>

### <a name="add-a-tile"></a><span data-ttu-id="978fa-219">タイルの追加</span><span class="sxs-lookup"><span data-stu-id="978fa-219">Add a tile</span></span>

1.  <span data-ttu-id="978fa-220">ソリューション エクスプローラーの **FMTutorial** プロジェクトで、**タイル** フォルダーを右クリックし、**追加**をポイントしてから**新しい項目**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="978fa-220">In Solution Explorer, in the **FMTutorial** project, right-click the **Tiles** folder, point to **Add**, and then click **New item**.</span></span>
2.  <span data-ttu-id="978fa-221">**Dynamics AX アーティファクト** &gt; **ユーザー インターフェイス** &gt; **タイル**とクリックします。</span><span class="sxs-lookup"><span data-stu-id="978fa-221">Click **Dynamics AX Artifacts** &gt; **User Interface** &gt; **Tile**.</span></span> <span data-ttu-id="978fa-222">**Name** プロパティを **FMTCurrentRentalsTile** に置き換えます。</span><span class="sxs-lookup"><span data-stu-id="978fa-222">Set the **Name** property to **FMTCurrentRentalsTile**.</span></span>
3.  <span data-ttu-id="978fa-223">**追加** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="978fa-223">Click **Add**.</span></span>
4.  <span data-ttu-id="978fa-224">新しい **FMTRental\_Current** タイルがデザイナーで開かれていない場合、ソリューション エクスプローラーでダブルクリックします。</span><span class="sxs-lookup"><span data-stu-id="978fa-224">If the new **FMTRental\_Current** tile isn’t already open in the designer, double-click it in Solution Explorer.</span></span>
5.  <span data-ttu-id="978fa-225">**プロパティ** ウィンドウで、次のプロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="978fa-225">In the **Properties** window, set the following properties.</span></span>

    | <span data-ttu-id="978fa-226">プロパティ</span><span class="sxs-lookup"><span data-stu-id="978fa-226">Property</span></span>       | <span data-ttu-id="978fa-227">先頭値</span><span class="sxs-lookup"><span data-stu-id="978fa-227">Value</span></span>              |
    |----------------|--------------------|
    | <span data-ttu-id="978fa-228">サイズ</span><span class="sxs-lookup"><span data-stu-id="978fa-228">Size</span></span>           | <span data-ttu-id="978fa-229">ShortWide</span><span class="sxs-lookup"><span data-stu-id="978fa-229">ShortWide</span></span>          |
    | <span data-ttu-id="978fa-230">メニュー項目名</span><span class="sxs-lookup"><span data-stu-id="978fa-230">Menu Item Name</span></span> | <span data-ttu-id="978fa-231">FMTRental\_Current</span><span class="sxs-lookup"><span data-stu-id="978fa-231">FMTRental\_Current</span></span> |
    | <span data-ttu-id="978fa-232">種類</span><span class="sxs-lookup"><span data-stu-id="978fa-232">Type</span></span>           | <span data-ttu-id="978fa-233">COUNT</span><span class="sxs-lookup"><span data-stu-id="978fa-233">Count</span></span>              |

6.  <span data-ttu-id="978fa-234">**Ctrl+S** キーを押して保存します。</span><span class="sxs-lookup"><span data-stu-id="978fa-234">Press **Ctrl+S** to save.</span></span>

<span data-ttu-id="978fa-235">タイルには、タイルのカウントが自動的に更新される頻度を制御するリフレッシュ頻度プロパティもあります。</span><span class="sxs-lookup"><span data-stu-id="978fa-235">Tiles also have a refresh frequency property that controls how often the counts on the tiles are automatically updated.</span></span> <span data-ttu-id="978fa-236">このプロパティに設定されている値は、ボリューム データに対するクエリの実行速度とともに、更新されたカウントの要求に基づいている必要があります。</span><span class="sxs-lookup"><span data-stu-id="978fa-236">The value that is set for this property should be based on the demand for updated counts, together with query execution speed against volume data.</span></span> <span data-ttu-id="978fa-237">このプロパティを設定する方法の指針については、[ワークスペースのタイルおよびリストのキャッシュ](tile-list-caching-workspaces.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="978fa-237">For guidance about how to set this property, see [Tile and List Caching for Workspaces](tile-list-caching-workspaces.md).</span></span> <span data-ttu-id="978fa-238">このラボでは、10 分の既定値で十分です。</span><span class="sxs-lookup"><span data-stu-id="978fa-238">For this lab, the default value of 10 minutes will be enough.</span></span>

### <a name="add-a-tile-button-to-the-workspace-form"></a><span data-ttu-id="978fa-239">ワークスペースのフォームへのタイル ボタンの追加</span><span class="sxs-lookup"><span data-stu-id="978fa-239">Add a tile button to the workspace form</span></span>

1.  <span data-ttu-id="978fa-240">ソリューション エクスプローラーで、**FmtClerkWorkspace** フォームをダブルクリックしてデザイナーで開きます。</span><span class="sxs-lookup"><span data-stu-id="978fa-240">In Solution Explorer, double-click the **FmtClerkWorkspace** form to open it in the designer.</span></span>
2.  <span data-ttu-id="978fa-241">**デザイン** &gt; **PanoramaBody** &gt; **TileContainer** を右クリックして **新規** をポイントし、**ボタンを並べて表示** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="978fa-241">Right-click **Design** &gt; **PanoramaBody** &gt; **TileContainer**, point to **New**, and then click **Tile Button**.</span></span>
3.  <span data-ttu-id="978fa-242">**Alt+上方向キー**を 4 回押して、タイル ボタンを TileContainer の上部に移動します。</span><span class="sxs-lookup"><span data-stu-id="978fa-242">Press **Alt+Up arrow** four times to move the tile button to the top of TileContainer.</span></span>
4.  <span data-ttu-id="978fa-243">**プロパティ** ウィンドウで、次のプロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="978fa-243">In the **Properties** window, set the following properties.</span></span>

    | <span data-ttu-id="978fa-244">プロパティ</span><span class="sxs-lookup"><span data-stu-id="978fa-244">Property</span></span> | <span data-ttu-id="978fa-245">先頭値</span><span class="sxs-lookup"><span data-stu-id="978fa-245">Value</span></span>                 |
    |----------|-----------------------|
    | <span data-ttu-id="978fa-246">氏名</span><span class="sxs-lookup"><span data-stu-id="978fa-246">Name</span></span>     | <span data-ttu-id="978fa-247">FMTCurrentRentalsTile</span><span class="sxs-lookup"><span data-stu-id="978fa-247">FMTCurrentRentalsTile</span></span> |
    | <span data-ttu-id="978fa-248">タイル</span><span class="sxs-lookup"><span data-stu-id="978fa-248">Tile</span></span>     | <span data-ttu-id="978fa-249">FMTCurrentRentalsTile</span><span class="sxs-lookup"><span data-stu-id="978fa-249">FMTCurrentRentalsTile</span></span> |

5.  <span data-ttu-id="978fa-250">**Ctrl+S** キーを押して保存します。</span><span class="sxs-lookup"><span data-stu-id="978fa-250">Press **Ctrl+S** to save.</span></span>

### <a name="view-the-new-tile-on-the-workspace"></a><span data-ttu-id="978fa-251">ワークスペース上の新規タイルの表示</span><span class="sxs-lookup"><span data-stu-id="978fa-251">View the new tile on the workspace</span></span>

<span data-ttu-id="978fa-252">Visual Studio を使用し、更新した **FmtClerkWorkspace** フォームをビルドして実行します。</span><span class="sxs-lookup"><span data-stu-id="978fa-252">Use Visual Studio to build and run the updated **FmtClerkWorkspace** form.</span></span>

1.  <span data-ttu-id="978fa-253">ソリューション エクスプローラーで、**FmtClerkWorkspace** フォームを右クリックしてから、**スタートアップ オブジェクトとして設定**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="978fa-253">In Solution Explorer, right-click the **FmtClerkWorkspace** form, and then click **Set as Startup Object**.</span></span>
2.  <span data-ttu-id="978fa-254">**Ctrl+F5** キーを押して、フォームをビルドおよび実行します。</span><span class="sxs-lookup"><span data-stu-id="978fa-254">Press **Ctrl+F5** to build and run the form.</span></span> <span data-ttu-id="978fa-255">Internet Explorerで、フォームを開きます。</span><span class="sxs-lookup"><span data-stu-id="978fa-255">The form opens in Internet Explorer.</span></span> 

    <span data-ttu-id="978fa-256">[![レンタル タイル](./media/currentrentalstile.png)](./media/currentrentalstile.png)</span><span class="sxs-lookup"><span data-stu-id="978fa-256">[![Rentals tile](./media/currentrentalstile.png)](./media/currentrentalstile.png)</span></span>

3.  <span data-ttu-id="978fa-257">**現在のレンタル** タイルをクリックします。</span><span class="sxs-lookup"><span data-stu-id="978fa-257">Click the **Current rentals** tile.</span></span> <span data-ttu-id="978fa-258">**レンタル** ページに移動し、それは 3 つの現在のレンタルにフィルター処理する必要があります。</span><span class="sxs-lookup"><span data-stu-id="978fa-258">You go to the **Rentals** page, which should be filtered to the three current rentals.</span></span>
4.  <span data-ttu-id="978fa-259">**戻る**ボタン、または**閉じる**ボタンをクリックし、ワークスペースに戻ります。</span><span class="sxs-lookup"><span data-stu-id="978fa-259">Click the **Back** button or the **Close** button to return to the workspace.</span></span>
5.  <span data-ttu-id="978fa-260">**現在のレンタル** タイルの右上隅にある小さな **i** ボタンをクリックします。</span><span class="sxs-lookup"><span data-stu-id="978fa-260">Click on the small **i** button in the upper-right corner of the **Current rentals** tile.</span></span> <span data-ttu-id="978fa-261">並べて表示されたデータに関する情報が、どの程度新しいかが確認できます。</span><span class="sxs-lookup"><span data-stu-id="978fa-261">You see information about how current the data in the tile is.</span></span> <span data-ttu-id="978fa-262">また、更新されたデータを表示するためのタイルを手動で更新するために使用できるリンクが指定されます。</span><span class="sxs-lookup"><span data-stu-id="978fa-262">Additionally, a link is provided that you can use to manually refresh the tile to view updated data.</span></span>

### <a name="view-tile-data-cache-values-at-run-time"></a><span data-ttu-id="978fa-263">実行時のタイル データ キャッシュ値の表示</span><span class="sxs-lookup"><span data-stu-id="978fa-263">View tile data cache values at run time</span></span>

<span data-ttu-id="978fa-264">システム管理者は、実行時に**タイル データ キャッシュ コンフィギュレーション** ページを使用して、タイル キャッシュ パラメーターを変更できます。</span><span class="sxs-lookup"><span data-stu-id="978fa-264">A system administrator can modify tile cache parameters at run time by using the **Tile data cache configuration** page.</span></span>

1. <span data-ttu-id="978fa-265">ナビゲーション バーのナビゲーション検索フィールドをクリックします。</span><span class="sxs-lookup"><span data-stu-id="978fa-265">Click in the navigation search field on the navigation bar.</span></span>
2. <span data-ttu-id="978fa-266">**タイル データ** を入力し、検索結果の **タイル データ キャッシュ構成** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="978fa-266">Type **Tile data**, and then click **Tile data cache configuration** in the search results.</span></span> 

   <span data-ttu-id="978fa-267">[![タイル キャッシュ 検索](./media/tilecachesearch.png)](./media/tilecachesearch.png)</span><span class="sxs-lookup"><span data-stu-id="978fa-267">[![Tile cache search](./media/tilecachesearch.png)](./media/tilecachesearch.png)</span></span>

3. <span data-ttu-id="978fa-268">**FMTCurrentRentalsTile** レコードを検索します。</span><span class="sxs-lookup"><span data-stu-id="978fa-268">Find the **FMTCurrentRentalsTile** record.</span></span> 

   <span data-ttu-id="978fa-269">[![タイル キャッシュ パラメーター](./media/tilecacheparams-1024x328.png)](./media/tilecacheparams.png)</span><span class="sxs-lookup"><span data-stu-id="978fa-269">[![Tile cache parameters](./media/tilecacheparams-1024x328.png)](./media/tilecacheparams.png)</span></span>


<span data-ttu-id="978fa-270">このページから、システム管理者はタイル キャッシュにいくつかのランタイム変更を実行できます。</span><span class="sxs-lookup"><span data-stu-id="978fa-270">From this page, the system administrator can perform several run-time modifications to a tile cache.</span></span> <span data-ttu-id="978fa-271">たとえば、システム管理者は、データ キャッシュの有効化/無効化、更新頻度の変更、およびカウント タイルを手動で更新する機能の有効化/無効化をすることができます。</span><span class="sxs-lookup"><span data-stu-id="978fa-271">For example, the system administrator can enable/disable the data cache, modify the refresh frequency, and enable/disable the ability to manually refresh the count tile.</span></span> <span data-ttu-id="978fa-272">タイル キャッシュは、タイルのあるフォームが最初に開かれたときに登録されることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="978fa-272">Note that tile caches are registered when a form that has a tile is first opened.</span></span> <span data-ttu-id="978fa-273">したがって、ご使用の環境に表示されているタイルのリストが、上の図のリストと異なる場合があります。</span><span class="sxs-lookup"><span data-stu-id="978fa-273">Therefore, the list of tiles that is shown in your environment might differ from the list in the preceding illustration.</span></span>

## <a name="exercise-3-create-a-new-tabbed-list-in-the-workspace"></a><span data-ttu-id="978fa-274">手順 3: ワークスペースに新しいタブ リストを作成</span><span class="sxs-lookup"><span data-stu-id="978fa-274">Exercise 3: Create a new tabbed list in the workspace</span></span>
<span data-ttu-id="978fa-275">次に、ワークスペースに追加のリストを含める方法を確認します。</span><span class="sxs-lookup"><span data-stu-id="978fa-275">Next, you will next see how to include an additional list in the workspace.</span></span> <span data-ttu-id="978fa-276">このセクションでは、Dynamics AX でフォームを作成する際の経験を紹介し、フォーム パターンも公開します。</span><span class="sxs-lookup"><span data-stu-id="978fa-276">This section will give you some experience with building forms in Dynamics AX and will also expose you to form patterns.</span></span> <span data-ttu-id="978fa-277">利用可能な車両を選択することによって新しいレンタルを開始できるように、利用可能な車両の一覧を追加します。</span><span class="sxs-lookup"><span data-stu-id="978fa-277">You will add a list of available vehicles, so that you will be able to initiate a new rental by selecting an available vehicle.</span></span> <span data-ttu-id="978fa-278">このセクションでは、新しいワークスペースに新しいリストを追加するだけで、レンタルを開始するアクションは追加しません。</span><span class="sxs-lookup"><span data-stu-id="978fa-278">In this section, you will just add the new list to the new workspace but won't add the action to initiate the rental.</span></span> <span data-ttu-id="978fa-279">このリストを追加するには、次のタスクを完了する必要があります。</span><span class="sxs-lookup"><span data-stu-id="978fa-279">To add this list, you will have to complete the following tasks:</span></span>

1.  <span data-ttu-id="978fa-280">ワークスペースに新しいタブ ページを追加します。</span><span class="sxs-lookup"><span data-stu-id="978fa-280">Add a new tab page to the workspace.</span></span>
2.  <span data-ttu-id="978fa-281">リストの内容を持つ新しいフォームを追加します。</span><span class="sxs-lookup"><span data-stu-id="978fa-281">Add a new form that has the list content.</span></span>
3.  <span data-ttu-id="978fa-282">新しいフォームを示す新しいメニュー項目を追加します。</span><span class="sxs-lookup"><span data-stu-id="978fa-282">Add a new menu item that points to the new form.</span></span>
4.  <span data-ttu-id="978fa-283">車両を使用可能な車両に限定する新しいクエリを追加します。</span><span class="sxs-lookup"><span data-stu-id="978fa-283">Add a new query to limit the vehicles to available vehicles.</span></span>

### <a name="add-space-in-the-workspace-for-a-new-list"></a><span data-ttu-id="978fa-284">新しいリストのワークスペースへのスペースの追加</span><span class="sxs-lookup"><span data-stu-id="978fa-284">Add space in the workspace for a new list</span></span>

1. <span data-ttu-id="978fa-285">ソリューション エクスプローラーで、**FmtClerkWorkspace** フォームをダブルクリックしてデザイナーで開きます。</span><span class="sxs-lookup"><span data-stu-id="978fa-285">In Solution Explorer, double-click the **FmtClerkWorkspace** form to open it in the designer.</span></span>
2. <span data-ttu-id="978fa-286">**デザイン** &gt; **PanoramaBody** &gt; **TabbedListSection** &gt; **TabbedLists** を右クリックし、**新しいタブ ページ** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="978fa-286">Right-click **Design** &gt; **PanoramaBody** &gt; **TabbedListSection** &gt; **TabbedLists**, and then click **New Tab Page**.</span></span>
3. <span data-ttu-id="978fa-287">**プロパティ** ウィンドウで、次のプロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="978fa-287">In the **Properties** window, set the following properties.</span></span>


   | <span data-ttu-id="978fa-288">プロパティ</span><span class="sxs-lookup"><span data-stu-id="978fa-288">Property</span></span> |                                     <span data-ttu-id="978fa-289">先頭値</span><span class="sxs-lookup"><span data-stu-id="978fa-289">Value</span></span>                                      |
   |----------|--------------------------------------------------------------------------------|
   |   <span data-ttu-id="978fa-290">氏名</span><span class="sxs-lookup"><span data-stu-id="978fa-290">Name</span></span>   |                           <span data-ttu-id="978fa-291">AvailableVehiclesContainer</span><span class="sxs-lookup"><span data-stu-id="978fa-291">AvailableVehiclesContainer</span></span>                           |
   | <span data-ttu-id="978fa-292">キャプション</span><span class="sxs-lookup"><span data-stu-id="978fa-292">Caption</span></span>  | <span data-ttu-id="978fa-293">@FMT199 <strong>注記:</strong> この値は「使用可能な車両」に対応します。</span><span class="sxs-lookup"><span data-stu-id="978fa-293">@FMT199 <strong>Note:</strong> This value corresponds to “Available vehicles”.</span></span> |


4. <span data-ttu-id="978fa-294">**AvailableVehiclesContainer** を右クリックし、**新規** をポイントして、**パーツから** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="978fa-294">Right-click **AvailableVehiclesContainer**, point to **New**, and then click **Form Part**.</span></span> <span data-ttu-id="978fa-295">**注記:** **フォーム パート**はオペレーション ワークスペース パターンにより、ここで唯一許可されるコントロール タイプです。</span><span class="sxs-lookup"><span data-stu-id="978fa-295">**Note:** **Form Part **is the only control type that the Operational Workspace pattern allows here.</span></span> <span data-ttu-id="978fa-296">このコントロールは、このセクションのコンテンツを保持するためにビルドするフォームにリンクするために使用されます。</span><span class="sxs-lookup"><span data-stu-id="978fa-296">This control will be used to link to the form that you will build to hold the content for this section.</span></span> 

   <span data-ttu-id="978fa-297">[![セクションを追加](./media/addsection1.png)](./media/addsection1.png)</span><span class="sxs-lookup"><span data-stu-id="978fa-297">[![Add section](./media/addsection1.png)](./media/addsection1.png)</span></span>

5. <span data-ttu-id="978fa-298">**プロパティ** ウィンドウで、**名前**プロパティを **AvailableVehiclesPart** に設定します。</span><span class="sxs-lookup"><span data-stu-id="978fa-298">In the **Properties** window, set the **Name** property to **AvailableVehiclesPart**.</span></span>
6. <span data-ttu-id="978fa-299">**Ctrl+S** キーを押して保存します。</span><span class="sxs-lookup"><span data-stu-id="978fa-299">Press **Ctrl+S** to save.</span></span>

### <a name="add-a-new-form-that-has-the-new-workspace-content"></a><span data-ttu-id="978fa-300">新しいワークスペースの内容を持つ新しいフォームを追加します。</span><span class="sxs-lookup"><span data-stu-id="978fa-300">Add a new form that has the new workspace content</span></span>

1.  <span data-ttu-id="978fa-301">ソリューション エクスプローラーの **FMTutorial** プロジェクトで、**フォーム** フォルダーを右クリックし、**追加**をポイントしてから**新しい項目**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="978fa-301">In Solution Explorer, in the **FMTutorial** project, right-click the **Forms** folder, point to **Add**, and then click **New item**.</span></span>
2.  <span data-ttu-id="978fa-302">**Dynamics AX アーティファクト** &gt; **ユーザー インターフェイス** &gt; **フォーム**とクリックします。</span><span class="sxs-lookup"><span data-stu-id="978fa-302">Click **Dynamics AX Artifacts** &gt; **User Interface** &gt; **Form**.</span></span> <span data-ttu-id="978fa-303">**Name** プロパティを **FMTAvailableVehicles** に置き換えます。</span><span class="sxs-lookup"><span data-stu-id="978fa-303">Set the **Name** property to **FMTAvailableVehicles**.</span></span>
3.  <span data-ttu-id="978fa-304">**追加** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="978fa-304">Click **Add**.</span></span>
4.  <span data-ttu-id="978fa-305">新しい **FMTAvailableVehicles** フォームがデザイナーで開かれていない場合、ソリューション エクスプローラーでダブルクリックします。</span><span class="sxs-lookup"><span data-stu-id="978fa-305">If the new **FMTAvailableVehicles** form isn’t already open in the designer, double-click it in Solution Explorer.</span></span>
5.  <span data-ttu-id="978fa-306">フォームのデータ ソースとして **FmtVehicle** テーブルを追加します。</span><span class="sxs-lookup"><span data-stu-id="978fa-306">Add the **FmtVehicle** table as a data source for the form.</span></span>
    1.  <span data-ttu-id="978fa-307">**データ ソース** を右クリックし、**新しいデータ ソース** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="978fa-307">Right-click **Data Sources**, and then click **New Data Source**.</span></span>
    2.  <span data-ttu-id="978fa-308">新しいデータ ソース ノードをクリックします。</span><span class="sxs-lookup"><span data-stu-id="978fa-308">Click the new data source node.</span></span> <span data-ttu-id="978fa-309">**プロパティ** ウィンドウで、次のプロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="978fa-309">In the **Properties** window, set the following properties.</span></span>

        | <span data-ttu-id="978fa-310">プロパティ</span><span class="sxs-lookup"><span data-stu-id="978fa-310">Property</span></span> | <span data-ttu-id="978fa-311">先頭値</span><span class="sxs-lookup"><span data-stu-id="978fa-311">Value</span></span>                                                                                                                                                      |
        |----------|------------------------------------------------------------------------------------------------------------------------------------------------------------|
        | <span data-ttu-id="978fa-312">テーブル</span><span class="sxs-lookup"><span data-stu-id="978fa-312">Table</span></span>    | <span data-ttu-id="978fa-313">FMTVehicle</span><span class="sxs-lookup"><span data-stu-id="978fa-313">FMTVehicle</span></span>                                                                                                                                                 |
        | <span data-ttu-id="978fa-314">氏名</span><span class="sxs-lookup"><span data-stu-id="978fa-314">Name</span></span>     | <span data-ttu-id="978fa-315">FMTVehicle **注記:** 最初に **Table** プロパティの値を指定してください。</span><span class="sxs-lookup"><span data-stu-id="978fa-315">FMTVehicle **Note:** Be sure to specify the value for the **Table** property first.</span></span> <span data-ttu-id="978fa-316">このプロパティは、同じ値を使用するように自動的に更新されます。</span><span class="sxs-lookup"><span data-stu-id="978fa-316">This property is automatically updated so that it uses the same value.</span></span> |

6.  <span data-ttu-id="978fa-317">フォームの 2 番目のデータ ソースとして **FmtVehicleModel** テーブルを追加します。</span><span class="sxs-lookup"><span data-stu-id="978fa-317">Add the **FmtVehicleModel** table as a second data source for the form.</span></span>
    1.  <span data-ttu-id="978fa-318">**データ ソース** を右クリックし、**新しいデータ ソース** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="978fa-318">Right-click **Data Sources**, and then click **New Data Source**.</span></span>
    2.  <span data-ttu-id="978fa-319">新しいデータ ソース ノードをクリックします。</span><span class="sxs-lookup"><span data-stu-id="978fa-319">Click the new data source node.</span></span> <span data-ttu-id="978fa-320">**プロパティ** ウィンドウで、次のプロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="978fa-320">In the **Properties** window, set the following properties.</span></span>

        | <span data-ttu-id="978fa-321">プロパティ</span><span class="sxs-lookup"><span data-stu-id="978fa-321">Property</span></span>    | <span data-ttu-id="978fa-322">先頭値</span><span class="sxs-lookup"><span data-stu-id="978fa-322">Value</span></span>                                                                                                                                                           |
        |-------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
        | <span data-ttu-id="978fa-323">テーブル</span><span class="sxs-lookup"><span data-stu-id="978fa-323">Table</span></span>       | <span data-ttu-id="978fa-324">FMTVehicleModel</span><span class="sxs-lookup"><span data-stu-id="978fa-324">FMTVehicleModel</span></span>                                                                                                                                                 |
        | <span data-ttu-id="978fa-325">氏名</span><span class="sxs-lookup"><span data-stu-id="978fa-325">Name</span></span>        | <span data-ttu-id="978fa-326">FMTVehicleModel **注記:** 最初に **Table** プロパティの値を指定してください。</span><span class="sxs-lookup"><span data-stu-id="978fa-326">FMTVehicleModel **Note:** Be sure to specify the value for the **Table** property first.</span></span> <span data-ttu-id="978fa-327">このプロパティは、同じ値を使用するように自動的に更新されます。</span><span class="sxs-lookup"><span data-stu-id="978fa-327">This property is automatically updated so that it uses the same value.</span></span> |
        | <span data-ttu-id="978fa-328">ソースの結合</span><span class="sxs-lookup"><span data-stu-id="978fa-328">Join Source</span></span> | <span data-ttu-id="978fa-329">FMTVehicle</span><span class="sxs-lookup"><span data-stu-id="978fa-329">FMTVehicle</span></span>                                                                                                                                                      |
        | <span data-ttu-id="978fa-330">リンク タイプ</span><span class="sxs-lookup"><span data-stu-id="978fa-330">Link Type</span></span>   | <span data-ttu-id="978fa-331">内部結合</span><span class="sxs-lookup"><span data-stu-id="978fa-331">Inner Join</span></span>                                                                                                                                                      |

7.  <span data-ttu-id="978fa-332">**パターン: &lt;選択&gt;** の表記が**フォーム デザイン**の横にあることを確認します。</span><span class="sxs-lookup"><span data-stu-id="978fa-332">Notice the **Pattern: &lt;select&gt;** notation next to **Form Design**.</span></span> <span data-ttu-id="978fa-333">これは、このノードに必要なパターンを示します。</span><span class="sxs-lookup"><span data-stu-id="978fa-333">This indicates the required pattern for this node.</span></span> <span data-ttu-id="978fa-334">**デザイン** を右クリックして **パターンの適用** をポイントし、**フォーム パターン セクション リスト** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="978fa-334">Right-click **Design**, point to **Apply pattern**, and then click **Form Part Section List**.</span></span> <span data-ttu-id="978fa-335">このフォーム パターンは通常、ワークスペースのリストで使用されます。</span><span class="sxs-lookup"><span data-stu-id="978fa-335">This form pattern is typically used by workspace lists.</span></span>
8.  <span data-ttu-id="978fa-336">このパターンの予想されるコンテンツを表示するには、**パターン** タブをクリックします。</span><span class="sxs-lookup"><span data-stu-id="978fa-336">Click the **Pattern** tab to see the expected content for this pattern.</span></span> <span data-ttu-id="978fa-337">この情報は、フォームのコンテンツを作成する際に役立ちます。</span><span class="sxs-lookup"><span data-stu-id="978fa-337">This information will help guide you as you create content for the form.</span></span> <span data-ttu-id="978fa-338">**注記:** 今後は、選択したフォーム パターンに基づいて自動的にフォーム構造を作成するメカニズムを提供する予定です。</span><span class="sxs-lookup"><span data-stu-id="978fa-338">**Note:** In the future, we plan to provide a mechanism for automatically creating a form structure, based on a selected form pattern.</span></span> 

    <span data-ttu-id="978fa-339">[![セクション リスト](./media/formpartsectionlist.png)](./media/formpartsectionlist.png)</span><span class="sxs-lookup"><span data-stu-id="978fa-339">[![Section list](./media/formpartsectionlist.png)](./media/formpartsectionlist.png)</span></span> 

    <span data-ttu-id="978fa-340">特に、このパターンは次の要素を検索します。</span><span class="sxs-lookup"><span data-stu-id="978fa-340">In particular, this pattern looks for the following elements:</span></span>
    -   <span data-ttu-id="978fa-341">ワークスペース リストに必要なすべてのフィルターおよびアクションを含むオプションのヘッダー グループです。</span><span class="sxs-lookup"><span data-stu-id="978fa-341">An optional header group that contains any filters and actions that are required for this workspace list.</span></span>
    -   <span data-ttu-id="978fa-342">必要なグリッド。</span><span class="sxs-lookup"><span data-stu-id="978fa-342">A required grid.</span></span> <span data-ttu-id="978fa-343">前の図の赤い枠線が示すように、パターン エンジンは現在この要素を見つけることができません。</span><span class="sxs-lookup"><span data-stu-id="978fa-343">As the red border in the preceding illustration indicates, the patterns engine can't currently find this element.</span></span>
    -   <span data-ttu-id="978fa-344">オプションの既定アクションは、グリッド内の個々のレコードのバッキング フォームへのナビゲーションを提供できます。</span><span class="sxs-lookup"><span data-stu-id="978fa-344">An optional default action, which can provide navigation to a backing form for an individual record in the grid.</span></span>
    -   <span data-ttu-id="978fa-345">オプション ボタンで、このセクションの品目の完全なリストを表示するバッキング フォームへユーザーを移動させます。</span><span class="sxs-lookup"><span data-stu-id="978fa-345">An optional button that takes the user to a backing form that shows the full list of items in this section.</span></span>

9.  <span data-ttu-id="978fa-346">**デザイン** を右クリックして **新規** をクリックし、**グリッド** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="978fa-346">Right-click **Design**, point to **New**, and then click **Grid**.</span></span>
10. <span data-ttu-id="978fa-347">**プロパティ** ウィンドウで、次のプロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="978fa-347">In the **Properties** window, set the following properties.</span></span> <span data-ttu-id="978fa-348">**注記:** 構築中のグリッドには複数のカードが含まれ、カード 2 枚の幅になります。</span><span class="sxs-lookup"><span data-stu-id="978fa-348">**Note:** The grid that we are building will contain cards and will be two cards wide.</span></span>

    | <span data-ttu-id="978fa-349">プロパティ</span><span class="sxs-lookup"><span data-stu-id="978fa-349">Property</span></span>             | <span data-ttu-id="978fa-350">先頭値</span><span class="sxs-lookup"><span data-stu-id="978fa-350">Value</span></span>       |
    |----------------------|-------------|
    | <span data-ttu-id="978fa-351">ExtendedStyle</span><span class="sxs-lookup"><span data-stu-id="978fa-351">ExtendedStyle</span></span>        | <span data-ttu-id="978fa-352">cardList</span><span class="sxs-lookup"><span data-stu-id="978fa-352">cardList</span></span>    |
    | <span data-ttu-id="978fa-353">複数選択</span><span class="sxs-lookup"><span data-stu-id="978fa-353">Multi Select</span></span>         | <span data-ttu-id="978fa-354">無</span><span class="sxs-lookup"><span data-stu-id="978fa-354">No</span></span>          |
    | <span data-ttu-id="978fa-355">スタイル</span><span class="sxs-lookup"><span data-stu-id="978fa-355">Style</span></span>                | <span data-ttu-id="978fa-356">リスト</span><span class="sxs-lookup"><span data-stu-id="978fa-356">List</span></span>        |
    | <span data-ttu-id="978fa-357">データ ソース</span><span class="sxs-lookup"><span data-stu-id="978fa-357">Data Source</span></span>          | <span data-ttu-id="978fa-358">FMTVehicle</span><span class="sxs-lookup"><span data-stu-id="978fa-358">FMTVehicle</span></span>  |
    | <span data-ttu-id="978fa-359">氏名</span><span class="sxs-lookup"><span data-stu-id="978fa-359">Name</span></span>                 | <span data-ttu-id="978fa-360">VehicleList</span><span class="sxs-lookup"><span data-stu-id="978fa-360">VehicleList</span></span> |
    | <span data-ttu-id="978fa-361">表示されている列のモード</span><span class="sxs-lookup"><span data-stu-id="978fa-361">Visible Columns Mode</span></span> | <span data-ttu-id="978fa-362">開始日固定</span><span class="sxs-lookup"><span data-stu-id="978fa-362">Fixed</span></span>       |
    | <span data-ttu-id="978fa-363">表示されている列</span><span class="sxs-lookup"><span data-stu-id="978fa-363">Visible Columns</span></span>      | <span data-ttu-id="978fa-364">2</span><span class="sxs-lookup"><span data-stu-id="978fa-364">2</span></span>           |

11. <span data-ttu-id="978fa-365">**VehicleList** グリッドを右クリックして **新規** をクリックし、**Group** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="978fa-365">Right-click the **VehicleList** grid, point to **New**, and then click **Group**.</span></span>
12. <span data-ttu-id="978fa-366">**プロパティ** ウィンドウで、**名前**プロパティを **VehicleCard** に設定します。</span><span class="sxs-lookup"><span data-stu-id="978fa-366">In the **Properties** window, set the **Name** property to **VehicleCard**.</span></span>
13. <span data-ttu-id="978fa-367">**VehicleCard** グループを右クリックして **パターンの適用** をポイントし、**ビジネス カード – 3 つのフィールド** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="978fa-367">Right-click the **VehicleCard** group, point to **Apply pattern**, and then click **Business Card – Three Fields**.</span></span>
14. <span data-ttu-id="978fa-368">**VehicleCard** グループを右クリックして **新規** をクリックし、**Image** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="978fa-368">Right-click the **VehicleCard** group, point to **New**, and then click **Image**.</span></span>
15. <span data-ttu-id="978fa-369">**プロパティ** ウィンドウで、次のプロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="978fa-369">In the **Properties** window, set the following properties.</span></span>

    | <span data-ttu-id="978fa-370">プロパティ</span><span class="sxs-lookup"><span data-stu-id="978fa-370">Property</span></span>    | <span data-ttu-id="978fa-371">先頭値</span><span class="sxs-lookup"><span data-stu-id="978fa-371">Value</span></span>           |
    |-------------|-----------------|
    | <span data-ttu-id="978fa-372">データ ソース</span><span class="sxs-lookup"><span data-stu-id="978fa-372">Data Source</span></span> | <span data-ttu-id="978fa-373">FMTVehicleModel</span><span class="sxs-lookup"><span data-stu-id="978fa-373">FMTVehicleModel</span></span> |
    | <span data-ttu-id="978fa-374">データ メソッド</span><span class="sxs-lookup"><span data-stu-id="978fa-374">Data Method</span></span> | <span data-ttu-id="978fa-375">vehicleImage</span><span class="sxs-lookup"><span data-stu-id="978fa-375">vehicleImage</span></span>    |

16. <span data-ttu-id="978fa-376">**データ ソース** &gt; **FMTVehicle** &gt; **フィールド**を展開します。</span><span class="sxs-lookup"><span data-stu-id="978fa-376">Expand **Data Sources** &gt; **FMTVehicle** &gt; **Fields**.</span></span>
17. <span data-ttu-id="978fa-377">**VehicleId** および **DisplayRelationType** フィールドを **VehicleCard** グループにドラッグします。</span><span class="sxs-lookup"><span data-stu-id="978fa-377">Drag the **VehicleId** and **DisplayRelationType** fields into the **VehicleCard** group.</span></span>
18. <span data-ttu-id="978fa-378">**デザイン** を右クリックして **新規** をクリックし、**グループ** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="978fa-378">Right-click **Design**, point to **New**, and then click **Group**.</span></span> <span data-ttu-id="978fa-379">新しいグループの **Name** プロパティを **HeaderGroup** に更新します。</span><span class="sxs-lookup"><span data-stu-id="978fa-379">Update the new group's **Name** property to **HeaderGroup**.</span></span>
19. <span data-ttu-id="978fa-380">新しい HeaderGroup 要素にはサブパターンが必要です。これは、これらのセクションのフィルターとアクションの配置に 2 つのバリアントがあるためです。</span><span class="sxs-lookup"><span data-stu-id="978fa-380">The new HeaderGroup element requires a subpattern, because there are two variants for the arrangement of filters and actions in these sections.</span></span> <span data-ttu-id="978fa-381">**HeaderGroup** を右クリックして **パターンの適用** をポイントし、**フィルターとツール バー - インライン** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="978fa-381">Right-click **HeaderGroup**, point to **Apply pattern**, and then click **Filters and Toolbar – Inline**.</span></span>
20. <span data-ttu-id="978fa-382">**HeaderGroup** を右クリックして **新規** をクリックし、**グループ** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="978fa-382">Right-click **HeaderGroup**, point to **New**, and then click **Group**.</span></span> <span data-ttu-id="978fa-383">新しいグループの **Name** プロパティを **FilterGroup** に更新します。</span><span class="sxs-lookup"><span data-stu-id="978fa-383">Update the new group’s **Name** property to **FilterGroup**.</span></span>
21. <span data-ttu-id="978fa-384">**FilterGroup** を右クリックして **新規** をクリックし、**QuickFilter** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="978fa-384">Right-click **FilterGroup**, point to **New**, and then click **QuickFilter**.</span></span>
22. <span data-ttu-id="978fa-385">**プロパティ** ウィンドウで、次のプロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="978fa-385">In the **Properties** window, set the following properties.</span></span>

    | <span data-ttu-id="978fa-386">プロパティ</span><span class="sxs-lookup"><span data-stu-id="978fa-386">Property</span></span>       | <span data-ttu-id="978fa-387">先頭値</span><span class="sxs-lookup"><span data-stu-id="978fa-387">Value</span></span>              |
    |----------------|--------------------|
    | <span data-ttu-id="978fa-388">氏名</span><span class="sxs-lookup"><span data-stu-id="978fa-388">Name</span></span>           | <span data-ttu-id="978fa-389">VehicleQuickFilter</span><span class="sxs-lookup"><span data-stu-id="978fa-389">VehicleQuickFilter</span></span> |
    | <span data-ttu-id="978fa-390">ターゲット コントロール</span><span class="sxs-lookup"><span data-stu-id="978fa-390">Target Control</span></span> | <span data-ttu-id="978fa-391">VehicleGrid</span><span class="sxs-lookup"><span data-stu-id="978fa-391">VehicleGrid</span></span>        |

23. <span data-ttu-id="978fa-392">**Ctrl+S** キーを押して保存します。</span><span class="sxs-lookup"><span data-stu-id="978fa-392">Press **Ctrl+S** to save.</span></span>

### <a name="add-a-new-query-that-limits-the-data-to-available-vehicles"></a><span data-ttu-id="978fa-393">データを使用可能な車両に限定する新しいクエリの追加</span><span class="sxs-lookup"><span data-stu-id="978fa-393">Add a new query that limits the data to available vehicles</span></span>

1.  <span data-ttu-id="978fa-394">ソリューション エクスプローラーの **FMTutorial** プロジェクトで、**クエリ** フォルダーを右クリックし、**追加**をポイントしてから**新しい項目**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="978fa-394">In Solution Explorer, in the **FMTutorial** project, right-click the **Queries** folder, point to **Add**, and then click **New item**.</span></span>
2.  <span data-ttu-id="978fa-395">**Dynamics AX アーティファクト** &gt; **データ モデル** &gt; **クエリ**とクリックします。</span><span class="sxs-lookup"><span data-stu-id="978fa-395">Click **Dynamics AX Artifacts** &gt; **Data Model** &gt; **Query**.</span></span> <span data-ttu-id="978fa-396">**Name** プロパティを **FMTAvailableVehicles** に置き換えます。</span><span class="sxs-lookup"><span data-stu-id="978fa-396">Set the **Name** property to **FMTAvailableVehicles**.</span></span>
3.  <span data-ttu-id="978fa-397">**追加** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="978fa-397">Click **Add**.</span></span>
4.  <span data-ttu-id="978fa-398">新しい **FMTAvailableVehicles** クエリがデザイナーで開かれていない場合、ソリューション エクスプローラーでダブルクリックします。</span><span class="sxs-lookup"><span data-stu-id="978fa-398">If the new **FMTAvailableVehicles** query isn’t already open in the designer, double-click it in Solution Explorer.</span></span>
5.  <span data-ttu-id="978fa-399">デザイナーで、**データ ソース**を右クリックしてから**新しいデータ ソース**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="978fa-399">In the designer, right-click **Data Sources**, and then click **New Data Source**.</span></span>
6.  <span data-ttu-id="978fa-400">**プロパティ** ウィンドウで、次のプロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="978fa-400">In the **Properties** window, set the following properties.</span></span>

    | <span data-ttu-id="978fa-401">プロパティ</span><span class="sxs-lookup"><span data-stu-id="978fa-401">Property</span></span>        | <span data-ttu-id="978fa-402">先頭値</span><span class="sxs-lookup"><span data-stu-id="978fa-402">Value</span></span>       |
    |-----------------|-------------|
    | <span data-ttu-id="978fa-403">テーブル</span><span class="sxs-lookup"><span data-stu-id="978fa-403">Table</span></span>           | <span data-ttu-id="978fa-404">FMTVehicles</span><span class="sxs-lookup"><span data-stu-id="978fa-404">FMTVehicles</span></span> |
    | <span data-ttu-id="978fa-405">Dynamics フィールド</span><span class="sxs-lookup"><span data-stu-id="978fa-405">Dynamics Fields</span></span> | <span data-ttu-id="978fa-406">有</span><span class="sxs-lookup"><span data-stu-id="978fa-406">Yes</span></span>         |

7.  <span data-ttu-id="978fa-407">**範囲** を右クリックし、**新しい範囲** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="978fa-407">Right-click **Ranges**, and then click **New Range**.</span></span>
8.  <span data-ttu-id="978fa-408">**プロパティ** ウィンドウで、次のプロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="978fa-408">In the **Properties** window, set the following properties.</span></span>

    | <span data-ttu-id="978fa-409">プロパティ</span><span class="sxs-lookup"><span data-stu-id="978fa-409">Property</span></span> | <span data-ttu-id="978fa-410">先頭値</span><span class="sxs-lookup"><span data-stu-id="978fa-410">Value</span></span>     |
    |----------|-----------|
    | <span data-ttu-id="978fa-411">フィールド</span><span class="sxs-lookup"><span data-stu-id="978fa-411">Field</span></span>    | <span data-ttu-id="978fa-412">ステータス</span><span class="sxs-lookup"><span data-stu-id="978fa-412">Status</span></span>    |
    | <span data-ttu-id="978fa-413">先頭値</span><span class="sxs-lookup"><span data-stu-id="978fa-413">Value</span></span>    | <span data-ttu-id="978fa-414">取得可能</span><span class="sxs-lookup"><span data-stu-id="978fa-414">Available</span></span> |

9.  <span data-ttu-id="978fa-415">**Ctrl+S** キーを押して保存します。</span><span class="sxs-lookup"><span data-stu-id="978fa-415">Press **Ctrl+S** to save.</span></span>

### <a name="add-a-new-menu-item-that-references-the-new-form"></a><span data-ttu-id="978fa-416">新しいフォームを参照する新しいメニュー項目の追加</span><span class="sxs-lookup"><span data-stu-id="978fa-416">Add a new menu item that references the new form</span></span>

1.  <span data-ttu-id="978fa-417">ソリューション エクスプローラーの **FMTutorial** プロジェクトで、**メニュー項目**フォルダーを右クリックし、**追加**をポイントしてから**新しい項目**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="978fa-417">In Solution Explorer, in the **FMTutorial** project, right-click the **Menu items** folder, point to **Add**, and then click **New item**.</span></span>
2.  <span data-ttu-id="978fa-418">**Dynamics AX アーティファクト** &gt; **ユーザー インターフェイス** &gt; **表示メニュー項目**とクリックします。</span><span class="sxs-lookup"><span data-stu-id="978fa-418">Click **Dynamics AX Artifacts** &gt; **User Interface** &gt; **Display menu item**.</span></span> <span data-ttu-id="978fa-419">**Name** プロパティを **FMTAvailableVehicles** に置き換えます。</span><span class="sxs-lookup"><span data-stu-id="978fa-419">Set the **Name** property to **FMTAvailableVehicles**.</span></span>
3.  <span data-ttu-id="978fa-420">**追加** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="978fa-420">Click **Add**.</span></span>
4.  <span data-ttu-id="978fa-421">新しい **FMTAvailableVehicles** メニュー項目がデザイナーで開かれていない場合、ソリューション エクスプローラーでダブルクリックします。</span><span class="sxs-lookup"><span data-stu-id="978fa-421">If the new **FMTAvailableVehicles** menu item isn’t already open in the designer, double-click it in Solution Explorer.</span></span>
5.  <span data-ttu-id="978fa-422">**プロパティ** ウィンドウで、次のプロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="978fa-422">In the **Properties** window, set the following properties.</span></span>

    | <span data-ttu-id="978fa-423">プロパティ</span><span class="sxs-lookup"><span data-stu-id="978fa-423">Property</span></span>       | <span data-ttu-id="978fa-424">先頭値</span><span class="sxs-lookup"><span data-stu-id="978fa-424">Value</span></span>                |
    |----------------|----------------------|
    | <span data-ttu-id="978fa-425">メニュー項目名</span><span class="sxs-lookup"><span data-stu-id="978fa-425">Menu item name</span></span> | <span data-ttu-id="978fa-426">FMTAvailableVehicles</span><span class="sxs-lookup"><span data-stu-id="978fa-426">FMTAvailableVehicles</span></span> |
    | <span data-ttu-id="978fa-427">クエリ</span><span class="sxs-lookup"><span data-stu-id="978fa-427">Query</span></span>          | <span data-ttu-id="978fa-428">FMTAvailableVehicles</span><span class="sxs-lookup"><span data-stu-id="978fa-428">FMTAvailableVehicles</span></span> |

6.  <span data-ttu-id="978fa-429">**Ctrl+S** キーを押して保存します。</span><span class="sxs-lookup"><span data-stu-id="978fa-429">Press **Ctrl+S** to save.</span></span>

### <a name="link-the-new-list-to-the-workspace"></a><span data-ttu-id="978fa-430">新しいリストのワークスペースへのリンク</span><span class="sxs-lookup"><span data-stu-id="978fa-430">Link the new list to the workspace</span></span>

1.  <span data-ttu-id="978fa-431">ソリューション エクスプローラーで、**FmtClerkWorkspace** フォームをダブルクリックしてデザイナーで開きます。</span><span class="sxs-lookup"><span data-stu-id="978fa-431">In Solution Explorer, double-click the **FmtClerkWorkspace** form to open it in the designer.</span></span>
2.  <span data-ttu-id="978fa-432">**デザイン** &gt; **PanoramaBody** &gt; **TabbedListSection** &gt; **TabbedLists** &gt; **AvailableVehiclesContainer** &gt; **AvailableVehiclesPart** の順にクリックします。</span><span class="sxs-lookup"><span data-stu-id="978fa-432">Click **Design** &gt; **PanoramaBody** &gt; **TabbedListSection** &gt; **TabbedLists** &gt; **AvailableVehiclesContainer** &gt; **AvailableVehiclesPart**.</span></span>
3.  <span data-ttu-id="978fa-433">**プロパティ** ウィンドウで、**メニュー項目名**プロパティを **FmtAvailableVehicles** に設定します。</span><span class="sxs-lookup"><span data-stu-id="978fa-433">In the **Properties** window, set the **Menu item name** property to **FmtAvailableVehicles**.</span></span>

### <a name="view-the-updated-form"></a><span data-ttu-id="978fa-434">更新されたフォームの表示</span><span class="sxs-lookup"><span data-stu-id="978fa-434">View the updated form</span></span>

<span data-ttu-id="978fa-435">Visual Studio を使用し、更新した **FmtClerkWorkspace** フォームをビルドして実行します。</span><span class="sxs-lookup"><span data-stu-id="978fa-435">Use Visual Studio to build and run the updated **FmtClerkWorkspace** form.</span></span>

1.  <span data-ttu-id="978fa-436">ソリューション エクスプローラーで、**FmtClerkWorkspace** フォームを右クリックしてから、**スタートアップ オブジェクトとして設定**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="978fa-436">In Solution Explorer, right-click the **FmtClerkWorkspace** form, and then click **Set as Startup Object**.</span></span>
2.  <span data-ttu-id="978fa-437">**Ctrl+F5** キーを押して、フォームをビルドおよび実行します。</span><span class="sxs-lookup"><span data-stu-id="978fa-437">Press **Ctrl+F5** to build and run the form.</span></span> <span data-ttu-id="978fa-438">Internet Explorerで、フォームを開きます。</span><span class="sxs-lookup"><span data-stu-id="978fa-438">The form opens in Internet Explorer.</span></span> 

    <span data-ttu-id="978fa-439">[![使用可能なリスト](./media/availablelist.png)](./media/availablelist.png)</span><span class="sxs-lookup"><span data-stu-id="978fa-439">[![Available list](./media/availablelist.png)](./media/availablelist.png)</span></span>

3.  <span data-ttu-id="978fa-440">**使用可能な車両**タブをクリックし、新しいリストを表示します。</span><span class="sxs-lookup"><span data-stu-id="978fa-440">Click the **Available vehicles** tab to see the new list.</span></span>
4.  <span data-ttu-id="978fa-441">QuickFilter をクリックして **Lit** と入力し、**Enter** を押して利用可能な Litware モデルの車両に絞り込みます。</span><span class="sxs-lookup"><span data-stu-id="978fa-441">Click in the QuickFilter, type **Lit**, and then press **Enter** to filter down to Litware model vehicles that are available.</span></span>

## <a name="exercise-4-create-a-backing-data-cache-for-a-list-extra-credit"></a><span data-ttu-id="978fa-442">手順 4: リストのバック データ キャッシュを作成 (追加クレジット)</span><span class="sxs-lookup"><span data-stu-id="978fa-442">Exercise 4: Create a backing data cache for a list (Extra credit)</span></span>
<span data-ttu-id="978fa-443">価値が高いクエリのリスト、同じワークスペースから複数のユーザーが使用し作業する場合があるリストについては、パフォーマンスを向上させるためにリストのキャッシュを考慮してください。</span><span class="sxs-lookup"><span data-stu-id="978fa-443">For lists that have expensive queries, or lists where multiple users might use and work from the same workspace, consider caching the list to improve performance.</span></span> <span data-ttu-id="978fa-444">このセクションでは、一覧のデータ キャッシュを作成するために必要なコンポーネントを追加します。</span><span class="sxs-lookup"><span data-stu-id="978fa-444">In this section, you will add the necessary artifacts to create a data cache for a list.</span></span> <span data-ttu-id="978fa-445">これらのコンポーネントには、フィールドをキャッシュにマップするクエリ、キャッシュを保持するテーブル、クエリとテーブルの間のマッピングを提供するクラスが含まれます。</span><span class="sxs-lookup"><span data-stu-id="978fa-445">These artifacts include a query that maps fields to the cache, a table that holds the cache, and a class that provides the mapping between the query and the table.</span></span> <span data-ttu-id="978fa-446">次に、ワークスペース内のいずれかのタブ付きリストにこのキャッシュを取り込みます。</span><span class="sxs-lookup"><span data-stu-id="978fa-446">You will then uptake this cache on one of the tabbed lists in the workspace.</span></span>

### <a name="add-a-query-that-maps-fields-to-the-data-cache"></a><span data-ttu-id="978fa-447">フィールドをデータ キャッシュにマップするクエリの追加</span><span class="sxs-lookup"><span data-stu-id="978fa-447">Add a query that maps fields to the data cache</span></span>

<span data-ttu-id="978fa-448">最初のステップでは、キャッシュ テーブルを作成するために使用されるクエリをビルドします。</span><span class="sxs-lookup"><span data-stu-id="978fa-448">The first step is to build a query that will be used to populate the cache table.</span></span> <span data-ttu-id="978fa-449">このクエリには、キャッシュ データを取得するすべてのテーブルが含まれている必要があります。また、結果をキャッシュするレコード/列に限定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="978fa-449">This query should include all the tables that you want to get your cache data from, and it should limit the results to those records/columns that you want cached.</span></span>

1.  <span data-ttu-id="978fa-450">ソリューション エクスプローラーの **FMTutorial** プロジェクトで、**クエリ** フォルダーを右クリックし、**追加**をポイントしてから**新しい項目**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="978fa-450">In Solution Explorer, in the **FMTutorial** project, right-click the **Queries** folder, point to **Add**, and then click **New item**.</span></span>
2.  <span data-ttu-id="978fa-451">**Dynamics AX アーティファクト** &gt; **データ モデル** &gt; **クエリ**とクリックします。</span><span class="sxs-lookup"><span data-stu-id="978fa-451">Click **Dynamics AX Artifacts** &gt; **Data Model** &gt; **Query**.</span></span> <span data-ttu-id="978fa-452">**Name** プロパティを **FMTPickupAndReturnQuery** に置き換えます。</span><span class="sxs-lookup"><span data-stu-id="978fa-452">Set the **Name** property to **FMTPickupAndReturnQuery**.</span></span>
3.  <span data-ttu-id="978fa-453">**追加** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="978fa-453">Click **Add**.</span></span>
4.  <span data-ttu-id="978fa-454">新しい **FMTPickupAndReturnQuery** クエリがデザイナーで開かれていない場合、ソリューション エクスプローラーでダブルクリックします。</span><span class="sxs-lookup"><span data-stu-id="978fa-454">If the new **FMTPickupAndReturnQuery** query isn’t already open in the designer, double-click it in Solution Explorer.</span></span>
5.  <span data-ttu-id="978fa-455">デザイナーで、**データ ソース**を右クリックしてから**新しいデータ ソース**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="978fa-455">In the designer, right-click **Data Sources**, and then click **New Data Source**.</span></span>
6.  <span data-ttu-id="978fa-456">**プロパティ** ウィンドウで、次のプロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="978fa-456">In the **Properties** window, set the following properties.</span></span>

    | <span data-ttu-id="978fa-457">プロパティ</span><span class="sxs-lookup"><span data-stu-id="978fa-457">Property</span></span>        | <span data-ttu-id="978fa-458">先頭値</span><span class="sxs-lookup"><span data-stu-id="978fa-458">Value</span></span>     |
    |-----------------|-----------|
    | <span data-ttu-id="978fa-459">テーブル</span><span class="sxs-lookup"><span data-stu-id="978fa-459">Table</span></span>           | <span data-ttu-id="978fa-460">FMTRental</span><span class="sxs-lookup"><span data-stu-id="978fa-460">FMTRental</span></span> |
    | <span data-ttu-id="978fa-461">Dynamics フィールド</span><span class="sxs-lookup"><span data-stu-id="978fa-461">Dynamics Fields</span></span> | <span data-ttu-id="978fa-462">無</span><span class="sxs-lookup"><span data-stu-id="978fa-462">No</span></span>        |

7.  <span data-ttu-id="978fa-463">FMTRental データ ソースに、次の 5 つのフィールドを追加します。</span><span class="sxs-lookup"><span data-stu-id="978fa-463">Add the following five fields to the FMTRental data source.</span></span> <span data-ttu-id="978fa-464">各フィールドについては、**フィールド**を右クリックし、**新規**を指し、次に**フィールド**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="978fa-464">For each field, right-click **Fields**, point to **New**, and then click **Field**.</span></span> <span data-ttu-id="978fa-465">**プロパティ** ウィンドウで、必要に応じて**フィールド** プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="978fa-465">In the **Properties** window, set the **Field** property as appropriate.</span></span>
    -   <span data-ttu-id="978fa-466">StartDate</span><span class="sxs-lookup"><span data-stu-id="978fa-466">StartDate</span></span>
    -   <span data-ttu-id="978fa-467">EndDate</span><span class="sxs-lookup"><span data-stu-id="978fa-467">EndDate</span></span>
    -   <span data-ttu-id="978fa-468">車両</span><span class="sxs-lookup"><span data-stu-id="978fa-468">Vehicle</span></span>
    -   <span data-ttu-id="978fa-469">行政単位 (区画)</span><span class="sxs-lookup"><span data-stu-id="978fa-469">State</span></span>
    -   <span data-ttu-id="978fa-470">RentalId</span><span class="sxs-lookup"><span data-stu-id="978fa-470">RentalId</span></span>

8.  <span data-ttu-id="978fa-471">**範囲** を右クリックし、**新しい範囲** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="978fa-471">Right-click **Ranges**, and then click **New Range**.</span></span>
9.  <span data-ttu-id="978fa-472">**プロパティ** ウィンドウで、次のプロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="978fa-472">In the **Properties** window, set the following properties.</span></span>

    | <span data-ttu-id="978fa-473">プロパティ</span><span class="sxs-lookup"><span data-stu-id="978fa-473">Property</span></span> | <span data-ttu-id="978fa-474">先頭値</span><span class="sxs-lookup"><span data-stu-id="978fa-474">Value</span></span>                                                                                  |
    |----------|----------------------------------------------------------------------------------------|
    | <span data-ttu-id="978fa-475">フィールド</span><span class="sxs-lookup"><span data-stu-id="978fa-475">Field</span></span>    | <span data-ttu-id="978fa-476">行政単位 (区画)</span><span class="sxs-lookup"><span data-stu-id="978fa-476">State</span></span>                                                                                  |
    | <span data-ttu-id="978fa-477">先頭値</span><span class="sxs-lookup"><span data-stu-id="978fa-477">Value</span></span>    | <span data-ttu-id="978fa-478">1..2 **注記:** この値は受取準備完了または処理中のレンタルをキャッシュします。</span><span class="sxs-lookup"><span data-stu-id="978fa-478">1..2 **Note:** This value will cache rentals that are Ready for Pickup or In Progress.</span></span> |

10. <span data-ttu-id="978fa-479">**FMTRental** で **データ ソース** を右クリックし、**新しいデータ ソース** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="978fa-479">Under **FMTRental**, right-click **Data Sources**, and then click **New Data Source**.</span></span>
11. <span data-ttu-id="978fa-480">**プロパティ** ウィンドウで、次のプロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="978fa-480">In the **Properties** window, set the following properties.</span></span>

    | <span data-ttu-id="978fa-481">プロパティ</span><span class="sxs-lookup"><span data-stu-id="978fa-481">Property</span></span>        | <span data-ttu-id="978fa-482">先頭値</span><span class="sxs-lookup"><span data-stu-id="978fa-482">Value</span></span>       |
    |-----------------|-------------|
    | <span data-ttu-id="978fa-483">テーブル</span><span class="sxs-lookup"><span data-stu-id="978fa-483">Table</span></span>           | <span data-ttu-id="978fa-484">FMTCustomer</span><span class="sxs-lookup"><span data-stu-id="978fa-484">FMTCustomer</span></span> |
    | <span data-ttu-id="978fa-485">Dynamics フィールド</span><span class="sxs-lookup"><span data-stu-id="978fa-485">Dynamics Fields</span></span> | <span data-ttu-id="978fa-486">無</span><span class="sxs-lookup"><span data-stu-id="978fa-486">No</span></span>          |

12. <span data-ttu-id="978fa-487">FMTCustomer データ ソースに、次の 3 つのフィールドを追加します。</span><span class="sxs-lookup"><span data-stu-id="978fa-487">Add the following three fields to the FMTCustomer data source.</span></span> <span data-ttu-id="978fa-488">各フィールドについては、**フィールド**を右クリックし、**新規**を指し、次に**フィールド**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="978fa-488">For each field, right-click **Fields**, point to **New**, and then click **Field**.</span></span> <span data-ttu-id="978fa-489">**プロパティ** ウィンドウで、必要に応じて**フィールド** プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="978fa-489">In the **Properties** window, set the **Field** property as appropriate.</span></span>
    -   <span data-ttu-id="978fa-490">名</span><span class="sxs-lookup"><span data-stu-id="978fa-490">FirstName</span></span>
    -   <span data-ttu-id="978fa-491">姓</span><span class="sxs-lookup"><span data-stu-id="978fa-491">LastName</span></span>
    -   <span data-ttu-id="978fa-492">画像</span><span class="sxs-lookup"><span data-stu-id="978fa-492">Image</span></span>

13. <span data-ttu-id="978fa-493">**関係** を右クリックし、 **新しい関係** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="978fa-493">Right-click **Relations**, and then click **New Relation**.</span></span>
14. <span data-ttu-id="978fa-494">**プロパティ** ウィンドウで、次のプロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="978fa-494">In the **Properties** window, set the following properties.</span></span>

    | <span data-ttu-id="978fa-495">プロパティ</span><span class="sxs-lookup"><span data-stu-id="978fa-495">Property</span></span>         | <span data-ttu-id="978fa-496">先頭値</span><span class="sxs-lookup"><span data-stu-id="978fa-496">Value</span></span>     |
    |------------------|-----------|
    | <span data-ttu-id="978fa-497">データ ソースの結合</span><span class="sxs-lookup"><span data-stu-id="978fa-497">Join Data Source</span></span> | <span data-ttu-id="978fa-498">FMTRental</span><span class="sxs-lookup"><span data-stu-id="978fa-498">FMTRental</span></span> |
    | <span data-ttu-id="978fa-499">フィールド</span><span class="sxs-lookup"><span data-stu-id="978fa-499">Field</span></span>            | <span data-ttu-id="978fa-500">顧客</span><span class="sxs-lookup"><span data-stu-id="978fa-500">Customer</span></span>  |
    | <span data-ttu-id="978fa-501">関連フィールド</span><span class="sxs-lookup"><span data-stu-id="978fa-501">Related Field</span></span>    | <span data-ttu-id="978fa-502">RecID</span><span class="sxs-lookup"><span data-stu-id="978fa-502">RecID</span></span>     |

    <span data-ttu-id="978fa-503">作成したクエリは、次の図と一致する必要があります。</span><span class="sxs-lookup"><span data-stu-id="978fa-503">The query that you've constructed should match the following illustration.</span></span> 

    ![キャッシュ クエリ](./media/cachequery.png)

15. <span data-ttu-id="978fa-505">**Ctrl+S** キーを押して保存します。</span><span class="sxs-lookup"><span data-stu-id="978fa-505">Press **Ctrl+S** to save.</span></span>

### <a name="add-a-cache-table"></a><span data-ttu-id="978fa-506">キャッシュ テーブルの追加</span><span class="sxs-lookup"><span data-stu-id="978fa-506">Add a cache table</span></span>

<span data-ttu-id="978fa-507">2 番目のステップでは、キャッシュ クエリから返されるフィールドを持つテーブルを定義します。</span><span class="sxs-lookup"><span data-stu-id="978fa-507">The second step is to define a table that has the fields that are returned from the cache query.</span></span> <span data-ttu-id="978fa-508">キャッシュ行をベース フレームワーク キャッシュ テーブルにマップするために使用される **SysDataCacheContextId** フィールドを追加することも必要です。</span><span class="sxs-lookup"><span data-stu-id="978fa-508">You must also add a **SysDataCacheContextId** field that will be used to map the cache row to the base framework cache tables.</span></span> <span data-ttu-id="978fa-509">また、このテーブルと他のテーブルとの間に必要な関係を定義する必要もあり、関係するキャッシュされたフィールドを必要とするデータ メソッドも必要です。</span><span class="sxs-lookup"><span data-stu-id="978fa-509">Additionally, you should also define any required relations between this table and other tables, and also any data methods that you require that involve the cached fields.</span></span>

1.  <span data-ttu-id="978fa-510">ソリューション エクスプローラーの **FMTutorial** プロジェクトで、**テーブル** フォルダーを右クリックし、**追加**をポイントしてから**新しい項目**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="978fa-510">In Solution Explorer, in the **FMTutorial** project, right-click the **Tables** folder, point to **Add**, and then click **New item**.</span></span>
2.  <span data-ttu-id="978fa-511">**Dynamics AX アーティファクト** &gt; **データ モデル** &gt; **テーブル**とクリックします。</span><span class="sxs-lookup"><span data-stu-id="978fa-511">Click **Dynamics AX Artifacts** &gt; **Data Model** &gt; **Table**.</span></span> <span data-ttu-id="978fa-512">**Name** プロパティを **FMTPickupAndReturnTableCache** に置き換えます。</span><span class="sxs-lookup"><span data-stu-id="978fa-512">Set the **Name** property to **FMTPickupAndReturnTableCache**.</span></span>
3.  <span data-ttu-id="978fa-513">**追加** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="978fa-513">Click **Add**.</span></span>
4.  <span data-ttu-id="978fa-514">新しい **FMTPickupAndReturnTableCache** テーブルがデザイナーで開かれていない場合、ソリューション エクスプローラーでダブルクリックします。</span><span class="sxs-lookup"><span data-stu-id="978fa-514">If the new **FMTPickupAndReturnTableCache** table isn’t already open in the designer, double-click it in Solution Explorer.</span></span>
5.  <span data-ttu-id="978fa-515">デザイナーで、**フィールド**を右クリックしてから、次のフィールドを追加します。</span><span class="sxs-lookup"><span data-stu-id="978fa-515">In the designer, right-click **Fields**, and then add the following fields.</span></span> <span data-ttu-id="978fa-516">各フィールドについては、次の表は、データ型および拡張データ型 (EDT) または列挙型を表示します。</span><span class="sxs-lookup"><span data-stu-id="978fa-516">For each field, the following table shows the data type and the extended data type (EDT) or enum type.</span></span>

    | <span data-ttu-id="978fa-517">フィールド タイプ</span><span class="sxs-lookup"><span data-stu-id="978fa-517">Field type</span></span>    | <span data-ttu-id="978fa-518">フィールド名</span><span class="sxs-lookup"><span data-stu-id="978fa-518">Field name</span></span>            | <span data-ttu-id="978fa-519">EDT/ 列挙型タイプ</span><span class="sxs-lookup"><span data-stu-id="978fa-519">EDT/enum type</span></span>               |
    |---------------|-----------------------|-----------------------------|
    | <span data-ttu-id="978fa-520">文字列</span><span class="sxs-lookup"><span data-stu-id="978fa-520">String</span></span>        | <span data-ttu-id="978fa-521">名</span><span class="sxs-lookup"><span data-stu-id="978fa-521">First Name</span></span>            | <span data-ttu-id="978fa-522">FirstName (EDT)</span><span class="sxs-lookup"><span data-stu-id="978fa-522">FirstName (EDT)</span></span>             |
    | <span data-ttu-id="978fa-523">文字列</span><span class="sxs-lookup"><span data-stu-id="978fa-523">String</span></span>        | <span data-ttu-id="978fa-524">姓</span><span class="sxs-lookup"><span data-stu-id="978fa-524">Last Name</span></span>             | <span data-ttu-id="978fa-525">LastName (EDT)</span><span class="sxs-lookup"><span data-stu-id="978fa-525">LastName (EDT)</span></span>              |
    | <span data-ttu-id="978fa-526">コンテナー</span><span class="sxs-lookup"><span data-stu-id="978fa-526">Container</span></span>     | <span data-ttu-id="978fa-527">画像</span><span class="sxs-lookup"><span data-stu-id="978fa-527">Image</span></span>                 | <span data-ttu-id="978fa-528">ビットマップ (EDT)</span><span class="sxs-lookup"><span data-stu-id="978fa-528">Bitmap (EDT)</span></span>                |
    | <span data-ttu-id="978fa-529">Int64</span><span class="sxs-lookup"><span data-stu-id="978fa-529">Int64</span></span>         | <span data-ttu-id="978fa-530">車両</span><span class="sxs-lookup"><span data-stu-id="978fa-530">Vehicle</span></span>               | <span data-ttu-id="978fa-531">FMTVehicleRecID (EDT)</span><span class="sxs-lookup"><span data-stu-id="978fa-531">FMTVehicleRecID (EDT)</span></span>       |
    | <span data-ttu-id="978fa-532">UTC 日時</span><span class="sxs-lookup"><span data-stu-id="978fa-532">Utc Date Time</span></span> | <span data-ttu-id="978fa-533">StartDate</span><span class="sxs-lookup"><span data-stu-id="978fa-533">StartDate</span></span>             | <span data-ttu-id="978fa-534">StartDateTime (EDT)</span><span class="sxs-lookup"><span data-stu-id="978fa-534">StartDateTime (EDT)</span></span>         |
    | <span data-ttu-id="978fa-535">UTC 日時</span><span class="sxs-lookup"><span data-stu-id="978fa-535">Utc Date Time</span></span> | <span data-ttu-id="978fa-536">EndDate</span><span class="sxs-lookup"><span data-stu-id="978fa-536">EndDate</span></span>               | <span data-ttu-id="978fa-537">EndDateTime (EDT)</span><span class="sxs-lookup"><span data-stu-id="978fa-537">EndDateTime (EDT)</span></span>           |
    | <span data-ttu-id="978fa-538">Int64</span><span class="sxs-lookup"><span data-stu-id="978fa-538">Int64</span></span>         | <span data-ttu-id="978fa-539">SysDataCacheContextId</span><span class="sxs-lookup"><span data-stu-id="978fa-539">SysDataCacheContextId</span></span> | <span data-ttu-id="978fa-540">SysDataCacheContextId (EDT)</span><span class="sxs-lookup"><span data-stu-id="978fa-540">SysDataCacheContextId (EDT)</span></span> |
    | <span data-ttu-id="978fa-541">列挙</span><span class="sxs-lookup"><span data-stu-id="978fa-541">Enum</span></span>          | <span data-ttu-id="978fa-542">行政単位 (区画)</span><span class="sxs-lookup"><span data-stu-id="978fa-542">State</span></span>                 | <span data-ttu-id="978fa-543">FMTReservationState (Enum)</span><span class="sxs-lookup"><span data-stu-id="978fa-543">FMTReservationState (Enum)</span></span>  |
    | <span data-ttu-id="978fa-544">文字列</span><span class="sxs-lookup"><span data-stu-id="978fa-544">String</span></span>        | <span data-ttu-id="978fa-545">RentalId</span><span class="sxs-lookup"><span data-stu-id="978fa-545">RentalId</span></span>              | <span data-ttu-id="978fa-546">FMTRentalId (EDT)</span><span class="sxs-lookup"><span data-stu-id="978fa-546">FMTRentalId (EDT)</span></span>           |

6.  <span data-ttu-id="978fa-547">デザイナーで、**リレーション**を右クリックし、**新規**をポイントしてから**リレーション**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="978fa-547">In the designer, right-click **Relations**, point to **New**, and then click **Relation**.</span></span>
7.  <span data-ttu-id="978fa-548">**プロパティ** ウィンドウで、次のプロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="978fa-548">In the **Properties** window, set the following properties.</span></span>

    | <span data-ttu-id="978fa-549">プロパティ</span><span class="sxs-lookup"><span data-stu-id="978fa-549">Property</span></span>      | <span data-ttu-id="978fa-550">先頭値</span><span class="sxs-lookup"><span data-stu-id="978fa-550">Value</span></span>     |
    |---------------|-----------|
    | <span data-ttu-id="978fa-551">氏名</span><span class="sxs-lookup"><span data-stu-id="978fa-551">Name</span></span>          | <span data-ttu-id="978fa-552">FMTRental</span><span class="sxs-lookup"><span data-stu-id="978fa-552">FMTRental</span></span> |
    | <span data-ttu-id="978fa-553">関連テーブル</span><span class="sxs-lookup"><span data-stu-id="978fa-553">Related Table</span></span> | <span data-ttu-id="978fa-554">FMTRental</span><span class="sxs-lookup"><span data-stu-id="978fa-554">FMTRental</span></span> |

8.  <span data-ttu-id="978fa-555">**FMTRental** 関係を右クリックし、**新規** をポイントして **標準** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="978fa-555">Right-click the **FMTRental** relation, point to **New**, and then click **Normal**.</span></span>
9.  <span data-ttu-id="978fa-556">**プロパティ** ウィンドウで、次のプロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="978fa-556">In the **Properties** window, set the following properties.</span></span>

    | <span data-ttu-id="978fa-557">プロパティ</span><span class="sxs-lookup"><span data-stu-id="978fa-557">Property</span></span>      | <span data-ttu-id="978fa-558">先頭値</span><span class="sxs-lookup"><span data-stu-id="978fa-558">Value</span></span>    |
    |---------------|----------|
    | <span data-ttu-id="978fa-559">フィールド</span><span class="sxs-lookup"><span data-stu-id="978fa-559">Field</span></span>         | <span data-ttu-id="978fa-560">RentalId</span><span class="sxs-lookup"><span data-stu-id="978fa-560">RentalId</span></span> |
    | <span data-ttu-id="978fa-561">関連フィールド</span><span class="sxs-lookup"><span data-stu-id="978fa-561">Related Field</span></span> | <span data-ttu-id="978fa-562">RentalId</span><span class="sxs-lookup"><span data-stu-id="978fa-562">RentalId</span></span> |

10. <span data-ttu-id="978fa-563">デザイナーで、**マッピング**を右クリックしてから**新規**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="978fa-563">In the designer, right-click **Mappings**, and then click **New**.</span></span>
11. <span data-ttu-id="978fa-564">**プロパティ** ウィンドウで、**マップ** プロパティを **SysDataSetCacheTableMap** に設定します。</span><span class="sxs-lookup"><span data-stu-id="978fa-564">In the **Properties** window, set the **Map** property to **SysDataSetCacheTableMap**.</span></span>
12. <span data-ttu-id="978fa-565">**ID** をクリックします。 **プロパティ** ウィンドウで、**フィールドのマップ** プロパティを **RecId** に設定します。</span><span class="sxs-lookup"><span data-stu-id="978fa-565">Click **Id**. In the **Properties** window, set the **Map Field To** property to **RecId**.</span></span>
13. <span data-ttu-id="978fa-566">**SysDataCacheContextId** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="978fa-566">Click **SysDataCacheContextId**.</span></span> <span data-ttu-id="978fa-567">**プロパティ** ウィンドウで、**フィールドのマップ** プロパティを **SysDataCacheContextId** に設定します。</span><span class="sxs-lookup"><span data-stu-id="978fa-567">In the **Properties** window, set the **Map Field To** property to **SysDataCacheContextId**.</span></span> <span data-ttu-id="978fa-568">**注記:** フィールドが一覧に表示されない場合は、**Ctrl+S** キーを押してテーブルを保存しなければならない場合があります。</span><span class="sxs-lookup"><span data-stu-id="978fa-568">**Note:** If the field doesn't appear in the list, you might have to save the table first, by pressing **Ctrl+S**.</span></span>
14. <span data-ttu-id="978fa-569">**F7** キーを押して、テーブルのコードを表示します。</span><span class="sxs-lookup"><span data-stu-id="978fa-569">Press **F7** to view the table’s code.</span></span> <span data-ttu-id="978fa-570">または、**FMTReturnAndPickupTableCache** を右クリックし、その後**コードの表示**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="978fa-570">Alternatively, right-click **FMTReturnAndPickupTableCache**, and then click **View Code**.</span></span>
15. <span data-ttu-id="978fa-571">テーブルに、次の表示メソッドを追加します。</span><span class="sxs-lookup"><span data-stu-id="978fa-571">Add the following display methods to the table.</span></span> <span data-ttu-id="978fa-572">フォームは後でこれらのメソッドを使用します。</span><span class="sxs-lookup"><span data-stu-id="978fa-572">The form will use these methods later.</span></span>

        public display FMTName fullName()
        {
            return this.FirstName + ' ' + this.LastName;
        }
        public display container customerImage()
        {
            ImageReference imgRef;
            container imgContainer = this.Image;
            if(imgContainer == connull())
            {
                imgRef = ImageReference::constructForSymbol("Person");
                imgContainer = imgRef.pack();
            }
            return imgContainer;
        }
        public display str rentalVehicle()
        {
            FMTVehicle vehicle;
            str value;
            if(this.Vehicle == 0)
            {
                value = "No vehicle assigned";
            }
            else
            {
                select vehicle where vehicle.RecId == this.Vehicle;
                value = vehicle.Description;
            }
            return value;
        }

16. <span data-ttu-id="978fa-573">**Ctrl+S** キーを押して保存します。</span><span class="sxs-lookup"><span data-stu-id="978fa-573">Press **Ctrl+S** to save.</span></span>

### <a name="adding-a-cache-class-that-links-the-query-and-table"></a><span data-ttu-id="978fa-574">クエリとテーブルをリンクするキャッシュ クラスの追加</span><span class="sxs-lookup"><span data-stu-id="978fa-574">Adding a cache class that links the query and table</span></span>

<span data-ttu-id="978fa-575">3 番目のステップは、キャッシュ クエリとキャッシュ テーブルの間のリレーションシップを定義するクラスを作成することです。</span><span class="sxs-lookup"><span data-stu-id="978fa-575">The third step is to create a class that defines the relationship between the cache query and the catch table.</span></span>

1.  <span data-ttu-id="978fa-576">ソリューション エクスプローラーの **FMTutorial** プロジェクトで、**クラス** フォルダーを右クリックし、**追加**をポイントしてから**新しい項目**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="978fa-576">In Solution Explorer, in the **FMTutorial** project, right-click the **Classes** folder, point to **Add**, and then click **New item**.</span></span>
2.  <span data-ttu-id="978fa-577">**Dynamics AX アーティファクト** &gt; **コード** &gt; **クラス**とクリックします。</span><span class="sxs-lookup"><span data-stu-id="978fa-577">Click **Dynamics AX Artifacts** &gt; **Code** &gt; **Class**.</span></span> <span data-ttu-id="978fa-578">**Name** プロパティを **FMTPickupAndReturnClass** に置き換えます。</span><span class="sxs-lookup"><span data-stu-id="978fa-578">Set the **Name** property to **FMTPickupAndReturnClass**.</span></span>
3.  <span data-ttu-id="978fa-579">**追加** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="978fa-579">Click **Add**.</span></span>
4.  <span data-ttu-id="978fa-580">新しい **FMTPickupAndReturnClass** クラスがデザイナーで開かれていない場合、ソリューション エクスプローラーでダブルクリックします。</span><span class="sxs-lookup"><span data-stu-id="978fa-580">If the new **FMTPickupAndReturnClass** class isn’t already open in the designer, double-click it in Solution Explorer.</span></span>
5.  <span data-ttu-id="978fa-581">クラスに次のコードを追加します。</span><span class="sxs-lookup"><span data-stu-id="978fa-581">Add the following code to the class.</span></span>

        [SysDataSetExtension(classStr(FMTPickupAndReturnClass)), // The name of this class
        SysDataSetCacheTableExtension(tableStr(FMTPickupAndReturnTableCache))] // The name of the cache table
        class FMTPickupAndReturnClass extends SysDataSetQuery implements SysIDataSet
        {
            public SysDataCacheRefreshFrequency parmRefreshFrequency()
            {
                return 600; // Cache refresh frequency, in seconds.
            }
            public SysQueryableIdentifier parmQueryableIdentifier()
            {
                return queryStr(FMTPickupAndReturnQuery); // The name of the query.
            }
            public SysDataCacheTypeId parmCacheTypeId()
            {
                return tableNum(FMTPickupAndReturnTableCache); // The name of the table.
            }
            public static FMTPickupAndReturnClass construct()
            {
                return new FMTPickupAndReturnClass();
            }
        }

6.  <span data-ttu-id="978fa-582">**Ctrl+S** キーを押して保存します。</span><span class="sxs-lookup"><span data-stu-id="978fa-582">Press **Ctrl+S** to save.</span></span>

### <a name="uptake-the-data-cache-on-a-list-in-the-workspace-and-table"></a><span data-ttu-id="978fa-583">ワークスペースとテーブルの一覧にあるデータ キャッシュを読み込む</span><span class="sxs-lookup"><span data-stu-id="978fa-583">Uptake the data cache on a list in the workspace and table</span></span>

<span data-ttu-id="978fa-584">データ キャッシュを設定した後、フォーム内でキャッシュの使用を開始することができます。</span><span class="sxs-lookup"><span data-stu-id="978fa-584">After you've set up the data cache, you can start to use the cache in your forms.</span></span> <span data-ttu-id="978fa-585">このセクションでは、データ キャッシュを使用するようワークスペース リストのいずれかを更新します。</span><span class="sxs-lookup"><span data-stu-id="978fa-585">In this section, you will update one of the workspace lists so that it uses the data cache.</span></span>

1.  <span data-ttu-id="978fa-586">ソリューション エクスプローラーで、**FMTReturningTodayPart** フォームをダブルクリックしてデザイナーで開きます。</span><span class="sxs-lookup"><span data-stu-id="978fa-586">In Solution Explorer, double-click the **FMTReturningTodayPart** form to open it in the designer.</span></span>
2.  <span data-ttu-id="978fa-587">**データ ソース**ノードを展開します。</span><span class="sxs-lookup"><span data-stu-id="978fa-587">Expand the **Data Sources** node.</span></span>
3.  <span data-ttu-id="978fa-588">**FMTCustomer** データソースを削除します。</span><span class="sxs-lookup"><span data-stu-id="978fa-588">Delete the **FMTCustomer** data source.</span></span>
4.  <span data-ttu-id="978fa-589">**FMTRental** データ ソースをクリックします。</span><span class="sxs-lookup"><span data-stu-id="978fa-589">Click the **FMTRental** data source.</span></span> <span data-ttu-id="978fa-590">**プロパティ** ウィンドウで、**テーブル** プロパティを **FMTPickupAndReturnTableCache** に設定します。</span><span class="sxs-lookup"><span data-stu-id="978fa-590">In the **Properties** window, set the **Table** property to **FMTPickupAndReturnTableCache**.</span></span>
5.  <span data-ttu-id="978fa-591">**デザイン** &gt; **ReturningTodayGrid** とクリックします。</span><span class="sxs-lookup"><span data-stu-id="978fa-591">Click **Design** &gt; **ReturningTodayGrid**.</span></span> <span data-ttu-id="978fa-592">**プロパティ** ウィンドウで、**データ ソース** プロパティを **FMTPickupAndReturnTableCache** に設定します。</span><span class="sxs-lookup"><span data-stu-id="978fa-592">In the **Properties** window, set the **Data Source** property to **FMTPickupAndReturnTableCache**.</span></span>
6.  <span data-ttu-id="978fa-593">**ReturningTodayGrid** 内で、**CustomerImage** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="978fa-593">Inside **ReturningTodayGrid**, click **CustomerImage**.</span></span> <span data-ttu-id="978fa-594">**データ ソース**プロパティを **FMTPickupAndReturnTableCache** に、**データ メソッド**プロパティを **customerImage** に更新します。</span><span class="sxs-lookup"><span data-stu-id="978fa-594">Update the **Data Source** property to **FMTPickupAndReturnTableCache** and the **Data Method** property to **customerImage**.</span></span>
7.  <span data-ttu-id="978fa-595">**ReturningTodayGrid** 内で、**FirstNameCopy1** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="978fa-595">Inside **ReturningTodayGrid**, click **FirstNameCopy1**.</span></span> <span data-ttu-id="978fa-596">**データ ソース**プロパティを **FMTPickupAndReturnTableCache** に、**データ メソッド**プロパティを **fullName** に更新します。</span><span class="sxs-lookup"><span data-stu-id="978fa-596">Update the **Data Source** property to **FMTPickupAndReturnTableCache** and the **Data Method** property to **fullName**.</span></span>
8.  <span data-ttu-id="978fa-597">**F7** キーを押して、フォームのコードを表示します。</span><span class="sxs-lookup"><span data-stu-id="978fa-597">Press **F7** to view code for the form.</span></span>
9.  <span data-ttu-id="978fa-598">次のコードに示すように、データ キャッシュに対処できることができるようフォームをインストルメント化します。</span><span class="sxs-lookup"><span data-stu-id="978fa-598">Instrument the form so that it can react to data caching, as shown in the following code.</span></span>

        [Form]
        public class FMTReturningTodayPart extends FormRun implements SysIDataSetConsumerForm
        {
            public void registerDatasourceOnQueryingEvent()
            {
                FMTPickupAndReturnTableCache_DS.OnQueryExecuting += 
                    eventhandler(this.parmDataSetFormQueryEventHandler().prepareDataSet);
            }
        }

10. <span data-ttu-id="978fa-599">**Ctrl+S** キーを押して保存します。</span><span class="sxs-lookup"><span data-stu-id="978fa-599">Press **Ctrl+S** to save.</span></span>

### <a name="update-the-action-above-the-list-so-that-it-works-with-the-cache-table"></a><span data-ttu-id="978fa-600">キャッシュ テーブルで動作するようにリストにあるアクションを更新する</span><span class="sxs-lookup"><span data-stu-id="978fa-600">Update the action above the list so that it works with the cache table</span></span>

<span data-ttu-id="978fa-601">ワークスペースから実行されるアクションは、ベース テーブルからのレコードが必要とするかもしれません。</span><span class="sxs-lookup"><span data-stu-id="978fa-601">Actions that are performed from the workspace might expect records from the base tables.</span></span> <span data-ttu-id="978fa-602">したがって、これらのアクションを更新してキャッシュ テーブルと連携させる必要があります。</span><span class="sxs-lookup"><span data-stu-id="978fa-602">Therefore, these actions might have to be updated so that they work with the cache table.</span></span> <span data-ttu-id="978fa-603">この例では、**FmtCompleteRecord** は **FMTRental** レコードをコンテキストとして期待しています。</span><span class="sxs-lookup"><span data-stu-id="978fa-603">In this example, the **FmtCompleteRecord** form currently expects a **FMTRental** record as context.</span></span> <span data-ttu-id="978fa-604">したがって、このフォームを更新して、ベース レンタル レコードまたはキャッシュ テーブル レコードのいずれかで正しく動作するようにする必要があります。</span><span class="sxs-lookup"><span data-stu-id="978fa-604">Therefore, this form must be updated so that it works correctly with either a base rental record or a cache table record as context.</span></span>

1.  <span data-ttu-id="978fa-605">ソリューション エクスプローラーで、**FmtCompleteRental** フォームをダブルクリックしてデザイナーで開きます。</span><span class="sxs-lookup"><span data-stu-id="978fa-605">In Solution Explorer, double-click the **FmtCompleteRental** form to open it in the designer.</span></span>
2.  <span data-ttu-id="978fa-606">**F7** キーを押して、フォームのコードを表示します。</span><span class="sxs-lookup"><span data-stu-id="978fa-606">Press **F7** to view the form’s code.</span></span>

        public void init()
        {
            //If this form was opened with a Rental as context
            if(element.args() != null && element.args().record() != null && element.args().record().TableId == tablenum(FMTRental))
            {
                //Get the Rental context
                rentalDS = FormDataUtil::getFormDataSource(element.args().record());
                rental = element.args().record();
                if(rental != null)
                {
                    select firstonly forupdate vehicle where vehicle.RecId == rental.Vehicle;
                }
            }
            super();
        }

3.  <span data-ttu-id="978fa-607">**init()** メソッドを次のコードと一致するように更新します。</span><span class="sxs-lookup"><span data-stu-id="978fa-607">Update the **init()** method so that it matches the following code.</span></span>

        public void init()
        {
            //If this form was opened with a record context
            if(element.args() != null && element.args().record() != null))
            {
                //Get that context
                rentalDS = FormDataUtil::getFormDataSource(element.args().record());
                if(element.args().record().TableId == tableNum(FMTPickupAndReturnTableCache))
                {
                    FMTPickupAndReturnTableCache cacheRecord = element.args().record();
                    select firstonly forupdate rental where rental.RentalId == cacheRecord.RentalId;
                }
                else if(element.args().record().TableId == tableNum(FMTRental))
                {
                    rental = element.args().record();
                }
                if(rental != null)
                {
                    select firstonly forupdate vehicle where vehicle.RecId == rental.Vehicle;
                }
            }
            super();
        }

4.  <span data-ttu-id="978fa-608">**Ctrl+S** キーを押して保存します。</span><span class="sxs-lookup"><span data-stu-id="978fa-608">Press **Ctrl+S** to save.</span></span>

### <a name="update-the-returning-today-query-so-that-it-works-with-the-cache-table"></a><span data-ttu-id="978fa-609">キャッシュ テーブルで動作するように Returning today クエリ を更新する</span><span class="sxs-lookup"><span data-stu-id="978fa-609">Update the Returning today query so that it works with the cache table</span></span>

1.  <span data-ttu-id="978fa-610">ソリューション エクスプローラーで、**FmtRental\_ReturningToday** クエリをダブルクリックしてデザイナーで開きます。</span><span class="sxs-lookup"><span data-stu-id="978fa-610">In Solution Explorer, double-click the **FmtRental\_ReturningToday** query to open it in the designer.</span></span>
2.  <span data-ttu-id="978fa-611">**データ ソース**ノードを展開し、**FMTRental** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="978fa-611">Expand the **Data Sources** node, and then click **FMTRental**.</span></span>
3.  <span data-ttu-id="978fa-612">**プロパティ** ウィンドウで、**テーブル** プロパティを **FMTPickupAndReturnTableCache** に更新します。</span><span class="sxs-lookup"><span data-stu-id="978fa-612">In the **Properties** window, update the **Table** property to **FMTPickupAndReturnTableCache**.</span></span> <span data-ttu-id="978fa-613">**注記:** **名前**プロパティは、自動的に同じ値に更新されます。</span><span class="sxs-lookup"><span data-stu-id="978fa-613">**Note:** The **Name** property should be updated automatically to the same value.</span></span>
4.  <span data-ttu-id="978fa-614">**Ctrl+S** キーを押して保存します。</span><span class="sxs-lookup"><span data-stu-id="978fa-614">Press **Ctrl+S** to save.</span></span>

### <a name="view-the-updated-form"></a><span data-ttu-id="978fa-615">更新されたフォームの表示</span><span class="sxs-lookup"><span data-stu-id="978fa-615">View the updated form</span></span>

<span data-ttu-id="978fa-616">Visual Studio を使用し、更新した **FmtClerkWorkspace** フォームをビルドして実行します。</span><span class="sxs-lookup"><span data-stu-id="978fa-616">Use Visual Studio to build and run the updated **FmtClerkWorkspace** form.</span></span>

1.  <span data-ttu-id="978fa-617">ソリューション エクスプローラーで、**FmtClerkWorkspace** フォームを右クリックしてから、**スタートアップ オブジェクトとして設定**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="978fa-617">In Solution Explorer, right-click the **FmtClerkWorkspace** form, and then click **Set as Startup Object**.</span></span>
2.  <span data-ttu-id="978fa-618">**Ctrl+F5** キーを押して、フォームをビルドおよび実行します。</span><span class="sxs-lookup"><span data-stu-id="978fa-618">Press **Ctrl+F5** to build and run the form.</span></span> <span data-ttu-id="978fa-619">Internet Explorerで、フォームを開きます。</span><span class="sxs-lookup"><span data-stu-id="978fa-619">The form opens in Internet Explorer.</span></span>
3.  <span data-ttu-id="978fa-620">**今日を返す**垂直タブをクリックします。</span><span class="sxs-lookup"><span data-stu-id="978fa-620">Click the **Returning today** vertical tab.</span></span>
4.  <span data-ttu-id="978fa-621">リストの 2 番目のレコードに対する**完全レンタル**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="978fa-621">Click **Complete rental** for the second record in the list.</span></span>
5.  <span data-ttu-id="978fa-622">**終了マイレージ** を **200** に設定し、**OK** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="978fa-622">Set **End Mileage** to **200**, and then click **OK**.</span></span> <span data-ttu-id="978fa-623">返却されたレンタルがまだ一覧に表示されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="978fa-623">Notice that the rental that you just returned still appears in the list.</span></span>

### <a name="make-sure-that-your-workspace-is-responsive"></a><span data-ttu-id="978fa-624">ワークスペースが応答可能であることを確認します。</span><span class="sxs-lookup"><span data-stu-id="978fa-624">Make sure that your workspace is responsive</span></span>

<span data-ttu-id="978fa-625">一覧からレコードを削除する (例えばユーザーがレンタルを完了させる) アクションをユーザーが行った後は、ご自分の一覧を最新に保つようにしてください。</span><span class="sxs-lookup"><span data-stu-id="978fa-625">You must make sure that your lists remain up to date after a user performs an action that should remove a record from the list (for example, the user completes a rental).</span></span> <span data-ttu-id="978fa-626">このセクションでは、ワークスペースが適切に反応することを保証するために、そのアクションをインストルメント化します。</span><span class="sxs-lookup"><span data-stu-id="978fa-626">In this section, we will instrument that action to help guarantee that the workspace reacts appropriately.</span></span>

1.  <span data-ttu-id="978fa-627">ソリューション エクスプローラーで、**FmtCompleteRental** フォームをダブルクリックしてデザイナーで開きます。</span><span class="sxs-lookup"><span data-stu-id="978fa-627">In Solution Explorer, double-click the **FmtCompleteRental** form to open it in the designer.</span></span>
2.  <span data-ttu-id="978fa-628">**F7** キーを押して、フォームのコードを表示します。</span><span class="sxs-lookup"><span data-stu-id="978fa-628">Press **F7** to view the code for the form.</span></span>
3.  <span data-ttu-id="978fa-629">**OKButton** の **clicked()** コードを検索します。</span><span class="sxs-lookup"><span data-stu-id="978fa-629">Locate the **clicked()** code for **OKButton**.</span></span> <span data-ttu-id="978fa-630">呼び出しフォームでのデータ ソースの調査呼び出しは、このメソッドの最後の方です。</span><span class="sxs-lookup"><span data-stu-id="978fa-630">Near the end of this method is a research call on the calling form’s data source.</span></span> <span data-ttu-id="978fa-631">そのコード行の直前に、次の **if** ステートメントを追加してキャッシュ テーブルから処理済のレンタルを削除します。</span><span class="sxs-lookup"><span data-stu-id="978fa-631">Just before that line of code, add the following **if** statement to delete the processed rental from the cache table.</span></span>

        . . .
        if(rentalDS.table() == tableNum(FMTPickupAndReturnTableCache))
        {
            //Delete updated record from backing cache
            FMTPickupAndReturnTableCache cacheRecord = element.args().record();
            cacheRecord.delete();
        }
        rentalDS.research(true);
        }

4.  <span data-ttu-id="978fa-632">**Ctrl+S** キーを押して保存します。</span><span class="sxs-lookup"><span data-stu-id="978fa-632">Press **Ctrl+S** to save.</span></span>

### <a name="view-the-updated-form"></a><span data-ttu-id="978fa-633">更新されたフォームの表示</span><span class="sxs-lookup"><span data-stu-id="978fa-633">View the updated form</span></span>

<span data-ttu-id="978fa-634">Visual Studio を使用し、更新した **FmtClerkWorkspace** フォームをビルドして実行します。</span><span class="sxs-lookup"><span data-stu-id="978fa-634">Use Visual Studio to build and run the updated **FmtClerkWorkspace** form.</span></span>

1.  <span data-ttu-id="978fa-635">ソリューション エクスプローラーで、**FmtClerkWorkspace** フォームを右クリックしてから、**スタートアップ オブジェクトとして設定**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="978fa-635">In Solution Explorer, right-click the **FmtClerkWorkspace** form, and then click **Set as Startup Object**.</span></span>
2.  <span data-ttu-id="978fa-636">**Ctrl+F5** キーを押して、フォームをビルドおよび実行します。</span><span class="sxs-lookup"><span data-stu-id="978fa-636">Press **Ctrl+F5** to build and run the form.</span></span> <span data-ttu-id="978fa-637">Internet Explorerで、フォームを開きます。</span><span class="sxs-lookup"><span data-stu-id="978fa-637">The form opens in Internet Explorer.</span></span>
3.  <span data-ttu-id="978fa-638">**今日を返す**垂直タブをクリックします。</span><span class="sxs-lookup"><span data-stu-id="978fa-638">Click the **Returning today** vertical tab.</span></span>
4.  <span data-ttu-id="978fa-639">リストの 2 番目のレコードに対する**完全レンタル**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="978fa-639">Click **Complete rental** for the second record in the list.</span></span>
5.  <span data-ttu-id="978fa-640">**終了マイレージ** を **100** に設定し、**OK** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="978fa-640">Set **End Mileage** to **100**, and then click **OK**.</span></span> <span data-ttu-id="978fa-641">返却されたレンタルが一覧に表示されなくなったことを確認します。</span><span class="sxs-lookup"><span data-stu-id="978fa-641">Notice that the rental that you just returned no longer appears in the list.</span></span>

## <a name="related-tutorials"></a><span data-ttu-id="978fa-642">関連するチュートリアル</span><span class="sxs-lookup"><span data-stu-id="978fa-642">Related tutorials</span></span>
-   <span data-ttu-id="978fa-643">[顧客フォームの作成](build-customer-form.md) – フォーム パターンを公開する場合は、このチュートリアルを参照してください。</span><span class="sxs-lookup"><span data-stu-id="978fa-643">[Building the Customer form](build-customer-form.md) – See this tutorial if you want more exposure to form patterns.</span></span> <span data-ttu-id="978fa-644">このチュートリアルでは、詳細マスター パターンをフォームに適用するプロセスについて説明します。</span><span class="sxs-lookup"><span data-stu-id="978fa-644">This tutorial will walk through the process of applying the Details Master pattern to a form.</span></span>
-   <span data-ttu-id="978fa-645">[ナビゲーションの構築](build-navigation.md) – Dynamics AX のメニュー構造にワークスペースを追加する方法については、このチュートリアルを参照してください。</span><span class="sxs-lookup"><span data-stu-id="978fa-645">[Building navigation](build-navigation.md) – See this tutorial if you want instructions for adding your workspace to the Dynamics AX menu structure.</span></span>





