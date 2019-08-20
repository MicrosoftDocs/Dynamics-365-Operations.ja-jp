---
title: ナビゲーションの構築
description: このチュートリアルでは、ワークスペースとナビゲーション ウィンドウにナビゲーション要素を追加します。
author: aneesmsft
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: sericks
ms.search.scope: Operations
ms.custom: 26031
ms.assetid: ad8ba47b-becb-4d13-a5af-8aca46075e82
ms.search.region: Global
ms.author: aneesa
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9cdefb4302ae9af1674e1e5c1de14e11120f349b
ms.sourcegitcommit: 16bfa0fd08feec1647829630401ce62ce2ffa1a4
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/02/2019
ms.locfileid: "1851239"
---
# <a name="build-navigation"></a><span data-ttu-id="71815-103">ナビゲーションの構築</span><span class="sxs-lookup"><span data-stu-id="71815-103">Build navigation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="71815-104">このチュートリアルでは、ワークスペースとナビゲーション ウィンドウにナビゲーション要素を追加します。</span><span class="sxs-lookup"><span data-stu-id="71815-104">In this tutorial, you will add navigational elements to a workspace and the navigation pane.</span></span>

<a name="prerequisites"></a><span data-ttu-id="71815-105">前提条件</span><span class="sxs-lookup"><span data-stu-id="71815-105">Prerequisites</span></span>
-------------

<span data-ttu-id="71815-106">このチュートリアルでは、リモート デスクトップを使用して環境にアクセスし、インスタンスの管理者としてプロビジョニングされる必要があります。</span><span class="sxs-lookup"><span data-stu-id="71815-106">For this tutorial, you need to access the environment using Remote Desktop, and be provisioned as an administrator on the instance.</span></span> <span data-ttu-id="71815-107">詳細については、「[アクセス インスタンス](../dev-tools/access-instances.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="71815-107">For more information, see [Access Instances](../dev-tools/access-instances.md).</span></span>

## <a name="key-concepts"></a><span data-ttu-id="71815-108">重要な概念</span><span class="sxs-lookup"><span data-stu-id="71815-108">Key concepts</span></span>
-   <span data-ttu-id="71815-109">*ワークスペース*は、特定のサブジェクト領域固有の概要ページです。</span><span class="sxs-lookup"><span data-stu-id="71815-109">A *workspace* is an overview page that is specific to a particular subject area.</span></span> <span data-ttu-id="71815-110">ワークスペースはすべてのユーザーに共通です。</span><span class="sxs-lookup"><span data-stu-id="71815-110">Workspaces are common to all users.</span></span> <span data-ttu-id="71815-111">このチュートリアルでは、既存のワークスペースにコンテンツを追加します。</span><span class="sxs-lookup"><span data-stu-id="71815-111">In this tutorial, you will add content into an existing workspace.</span></span>
-   <span data-ttu-id="71815-112">*ダッシュボード*は、ユーザーごとの既定のホーム ページです。</span><span class="sxs-lookup"><span data-stu-id="71815-112">The *dashboard* is the default home page for each user.</span></span>
-   <span data-ttu-id="71815-113">*タイル*はワークスペースまたはダッシュボードに表示できるセキュリティ保護可能なオブジェクトです。</span><span class="sxs-lookup"><span data-stu-id="71815-113">*Tiles* are securable objects that can be shown on a workspace or the dashboard.</span></span> <span data-ttu-id="71815-114">これらは、メニュー項目を使用して保護できます。</span><span class="sxs-lookup"><span data-stu-id="71815-114">They can be secured by using menu items.</span></span>

## <a name="setup"></a><span data-ttu-id="71815-115">段取り</span><span class="sxs-lookup"><span data-stu-id="71815-115">Setup</span></span>
<span data-ttu-id="71815-116">これが作業する最初のチュートリアルである場合は、[アクセス インスタンス](../dev-tools/access-instances.md)を確認し、ローカル VM で作業している場合に、管理者ユーザーを提供するかどうかを確認します。</span><span class="sxs-lookup"><span data-stu-id="71815-116">If this is the first tutorial that you are working on, review [Access Instances](../dev-tools/access-instances.md) and make sure that you provision your administrator user if you are working on a local VM.</span></span>

### <a name="import-the-tutorial-project"></a><span data-ttu-id="71815-117">チュートリアル プロジェクトのインポート</span><span class="sxs-lookup"><span data-stu-id="71815-117">Import the tutorial project</span></span>

<span data-ttu-id="71815-118">フリート管理チュートリアル プロジェクトを既にインポートした場合は、次のセクションに進みます。</span><span class="sxs-lookup"><span data-stu-id="71815-118">If you have already imported the Fleet management tutorial project, skip to the next section.</span></span>

1.  <span data-ttu-id="71815-119">フリート管理のサンプルを <https://github.com/Microsoft/FMLab> からダウンロードし、**C:\\** に保存してから解凍します。</span><span class="sxs-lookup"><span data-stu-id="71815-119">Download the Fleet Management sample from <https://github.com/Microsoft/FMLab>, save it to **C:\\**, and unzip it.</span></span>
2.  <span data-ttu-id="71815-120">Visual Studio の、**Finance and Operations** メニューで、**プロジェクトのインポート** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="71815-120">In Visual Studio, on the **Finance and Operations** menu, click **Import Project**.</span></span>
3.  <span data-ttu-id="71815-121">**プロジェクトのインポート** ウィンドウで、**ファイル名**テキスト ボックスの隣にある、省略記号ボタンをクリックします。</span><span class="sxs-lookup"><span data-stu-id="71815-121">In the **Import Project** window, next to the **Filename** text box, click the ellipsis button.</span></span>
4.  <span data-ttu-id="71815-122">**インポートするファイルの選択**ウィンドウで、**C:\FMLab** を参照して **FMTutorialDataModel.axpp** をクリックしてから**開く**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="71815-122">In the **Select the file to import** window, browse to **C:\FMLab**, click **FMTutorialDataModel.axpp,** and then click **Open**.</span></span>
5.  <span data-ttu-id="71815-123">プロジェクト ファイルの場所テキスト ボックスに、**C:\FMLab** と入力します。</span><span class="sxs-lookup"><span data-stu-id="71815-123">In the Project file location text box, enter **C:\FMLab.**</span></span>
6.  <span data-ttu-id="71815-124">**要素の上書き** オプションをオンにし、**OK** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="71815-124">Select the **Overwrite Elements** option, and then click **OK**.</span></span>

### <a name="import-transactional-data"></a><span data-ttu-id="71815-125">トランザクション データのインポート</span><span class="sxs-lookup"><span data-stu-id="71815-125">Import transactional data</span></span>

1.  <span data-ttu-id="71815-126">Visual Studio で、**FMTutorial** プロジェクトを開きます。</span><span class="sxs-lookup"><span data-stu-id="71815-126">In Visual Studio, open the **FMTutorial** project.</span></span> <span data-ttu-id="71815-127">**ファイル**メニューで、**開く**をポイントし、**プロジェクト/ソリューション**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="71815-127">On the **File** menu, point to **Open**, and then click **Project/Solution**.</span></span>
2.  <span data-ttu-id="71815-128">**プロジェクトを開く**ダイアログ ボックスで、C:\FMLab\FMTutorial を参照してから FMTutorial をクリックします。</span><span class="sxs-lookup"><span data-stu-id="71815-128">In the **Open Project** dialog box, browse to C:\FMLab\FMTutorial, and then click FMTutorial.</span></span> <span data-ttu-id="71815-129">**開く** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="71815-129">Click **Open**.</span></span> <span data-ttu-id="71815-130">**FMTutorial** プロジェクトが**ソリューション エクスプローラー**に表示されます。</span><span class="sxs-lookup"><span data-stu-id="71815-130">The **FMTutorial** project appears in **Solution Explorer**.</span></span>
3.  <span data-ttu-id="71815-131">フリート管理チュートリアルのデータを読み込むには、FMTDataHelper クラスを使用します。</span><span class="sxs-lookup"><span data-stu-id="71815-131">Use the FMTDataHelper class to load data for the Fleet Management tutorial.</span></span> <span data-ttu-id="71815-132">**ソリューション エクスプローラー**の FMTutorial プロジェクトで、**クラス**を展開して、**FMTDataHelper** を右クリックしてから、**スタートアップ オブジェクトとして設定**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="71815-132">In **Solution Explorer**, in the FMTutorial project, expand **Classes**, right-click **FMTDataHelper**, and then click **Set as Startup Object**.</span></span>
4.  <span data-ttu-id="71815-133">**ビルド**メニューから、**ソリューションの再構築**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="71815-133">From the **BUILD** menu, click **Rebuild Solution**.</span></span> <span data-ttu-id="71815-134">インポートされたアーティファクトのタイムスタンプを更新するには、リビルドを使用します。</span><span class="sxs-lookup"><span data-stu-id="71815-134">You use the rebuild to update the timestamps of the imported artifacts.</span></span> <span data-ttu-id="71815-135">**出力** ウィンドウでビルドの進行状況を表示できます。</span><span class="sxs-lookup"><span data-stu-id="71815-135">You can view the build progress in the **Output** window.</span></span>
5.  <span data-ttu-id="71815-136">**Ctrl+F5** キーを押してプロジェクトを実行し、データを読み込みます。</span><span class="sxs-lookup"><span data-stu-id="71815-136">Press **Ctrl+F5** to run the project and load the data.</span></span>

## <a name="add-a-tile-to-the-tutorial-workspace"></a><span data-ttu-id="71815-137">チュートリアル ワークスペースへのタイルの追加</span><span class="sxs-lookup"><span data-stu-id="71815-137">Add a tile to the tutorial workspace</span></span>
<span data-ttu-id="71815-138">最初に、FMTClerkWorkspace のフォームに新しいタイルを追加します。</span><span class="sxs-lookup"><span data-stu-id="71815-138">First, we will add a new tile to the form FMTClerkWorkspace.</span></span>

1.  <span data-ttu-id="71815-139">**ソリューション エクスプローラー**で、**フォーム**を展開してから、**FMTClerkWorkspace** をダブルクリックします。</span><span class="sxs-lookup"><span data-stu-id="71815-139">In **Solution Explorer**, expand **Forms** and then double-click **FMTClerkWorkspace**.</span></span>
2.  <span data-ttu-id="71815-140">デザイナーで、**PanoramaBody** を展開します。</span><span class="sxs-lookup"><span data-stu-id="71815-140">In the designer, expand **PanoramaBody**.</span></span>
3.  <span data-ttu-id="71815-141">**TileContainer** を右クリックし、**新規** &gt; **ボタンを並べて表示** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="71815-141">Right-click **TileContainer**, and then click **New** &gt; **Tile Button.**</span></span>
4.  <span data-ttu-id="71815-142">新しいタイル ボタンの次のプロパティを指定します。</span><span class="sxs-lookup"><span data-stu-id="71815-142">Specify the following properties for the new tile button.</span></span>

    | <span data-ttu-id="71815-143">**プロパティ**</span><span class="sxs-lookup"><span data-stu-id="71815-143">**Property**</span></span> | <span data-ttu-id="71815-144">**値**</span><span class="sxs-lookup"><span data-stu-id="71815-144">**Value**</span></span>           |
    |--------------|---------------------|
    | <span data-ttu-id="71815-145">テキスト</span><span class="sxs-lookup"><span data-stu-id="71815-145">Text</span></span>         | <span data-ttu-id="71815-146">タイルをテスト</span><span class="sxs-lookup"><span data-stu-id="71815-146">Test tile</span></span>           |
    | <span data-ttu-id="71815-147">タイル</span><span class="sxs-lookup"><span data-stu-id="71815-147">Tile</span></span>         | <span data-ttu-id="71815-148">FMTAllCustomersTile</span><span class="sxs-lookup"><span data-stu-id="71815-148">FMTAllCustomersTile</span></span> |

    <span data-ttu-id="71815-149">これにより、既存の**すべての顧客**タイルの複製が作成されます。</span><span class="sxs-lookup"><span data-stu-id="71815-149">This will create a duplicate of the existing **All customers** tile.</span></span>
5.  <span data-ttu-id="71815-150">**ソリューション エクスプローラー**で、**フォーム** &gt; **FMTClerkWorkspace** とクリックし、右クリックしてから**スタートアップ オブジェクトとして設定**を選択します。</span><span class="sxs-lookup"><span data-stu-id="71815-150">In **Solution Explorer**, click **Forms** &gt; **FMTClerkWorkspace**, right-click, and then select **Set as Start-up Object**.</span></span> <span data-ttu-id="71815-151">スタートアップ オブジェクトを設定することは、手順 7 で Ctrl + F5 キーを押すと Visual Studio が起動するために必要です。</span><span class="sxs-lookup"><span data-stu-id="71815-151">Setting a start-up object is necessary to allow Visual Studio to launch when you press Ctrl+F5 in step 7.</span></span> <span data-ttu-id="71815-152">起動オブジェクトとしてこのフォームを設定すると、Ctrl + F5 キーを押した後に、進行中のフリート管理係ワークスペースが表示されます。</span><span class="sxs-lookup"><span data-stu-id="71815-152">Setting this form as the start-up object will cause the work-in-progress Fleet management clerk workspace to appear after you press Ctrl+F5.</span></span> <span data-ttu-id="71815-153">後で再度このフォームを詳細にプレビュー表示します。</span><span class="sxs-lookup"><span data-stu-id="71815-153">We will preview this form again later in detail.</span></span>
6.  <span data-ttu-id="71815-154">**FMTutorial** を右クリックし、**再ビルド** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="71815-154">Right-click **FMTutorial**, and then click **Rebuild**.</span></span>
7.  <span data-ttu-id="71815-155">**Ctrl+F5** キーを押してプロジェクトを実行します。</span><span class="sxs-lookup"><span data-stu-id="71815-155">Press **Ctrl+F5** to run the project.</span></span>

<span data-ttu-id="71815-156">プロジェクトをビルドして実行すると、フリート管理係ワークスペースが起動します。</span><span class="sxs-lookup"><span data-stu-id="71815-156">After you build and run the project, the Fleet management clerk workspace will launch.</span></span> <span data-ttu-id="71815-157">作成した **テスト タイル** という名前の新しいタイルは、タイルのセットの最後にある、ワークスペースの最初のセクションに含まれます。</span><span class="sxs-lookup"><span data-stu-id="71815-157">The new tile named, **Test tile**, that you created will be included in the first section of the workspace, at the end of the set of tiles.</span></span> 

<span data-ttu-id="71815-158">[![Nav1](./media/nav1.png)](./media/nav1.png)</span><span class="sxs-lookup"><span data-stu-id="71815-158">[![Nav1](./media/nav1.png)](./media/nav1.png)</span></span> 

> [!NOTE]
> <span data-ttu-id="71815-159">タイルがクリックされたとき、どこにも移動しません。</span><span class="sxs-lookup"><span data-stu-id="71815-159">The tile will not navigate anywhere when clicked.</span></span> <span data-ttu-id="71815-160">これを有効にするには、**ソリューション エクスプローラー** の**タイル**の下にあるメニュー項目名を FMTAllCustomersTile に定義します。</span><span class="sxs-lookup"><span data-stu-id="71815-160">To enable this, you can define a Menu Item Name on FMTAllCustomersTile, under **Tiles** in **Solution Explorer**.</span></span>

## <a name="add-a-new-workspace-to-the-navigation-pane"></a><span data-ttu-id="71815-161">ナビゲーション ウィンドウへの新しいワークスペースの追加</span><span class="sxs-lookup"><span data-stu-id="71815-161">Add a new workspace to the navigation pane</span></span>
<span data-ttu-id="71815-162">次に、FMTClerkWorkspace フォームをナビゲーション ウィンドウに追加します。</span><span class="sxs-lookup"><span data-stu-id="71815-162">Next, we will add the FMTClerkWorkspace form to the navigation pane.</span></span> <span data-ttu-id="71815-163">これを次の 2 つの場所で実行します。</span><span class="sxs-lookup"><span data-stu-id="71815-163">We will do this in two locations:</span></span>

-   <span data-ttu-id="71815-164">**すべてのワークスペース** リスト。</span><span class="sxs-lookup"><span data-stu-id="71815-164">The **All workspaces** list.</span></span>
-   <span data-ttu-id="71815-165">ワークスペースを示すメニュー構造を含む領域のリストにある新しい項目。</span><span class="sxs-lookup"><span data-stu-id="71815-165">A new item in the area list containing a menu structure that shows the workspace.</span></span>

### <a name="create-a-menu-item-that-points-to-the-fmtclerkworkspace-workspace"></a><span data-ttu-id="71815-166">FMTClerkWorkspace ワークスペースを指すメニュー項目を作成します</span><span class="sxs-lookup"><span data-stu-id="71815-166">Create a menu item that points to the FMTClerkWorkspace workspace</span></span>

1.  <span data-ttu-id="71815-167">**FMTutorial** を右クリックして **追加** をポイントしてから **新しい項目** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="71815-167">Right-click **FMTutorial**, point to **Add**, and then click **New Item**.</span></span>
2.  <span data-ttu-id="71815-168">**AX アーティファクト** &gt; **ユーザー インターフェイス** &gt; **表示メニュー項目** の順にクリックします。</span><span class="sxs-lookup"><span data-stu-id="71815-168">Click **AX Artifacts** &gt; **User Interface** &gt; **Display Menu Item**.</span></span> <span data-ttu-id="71815-169">**名前**プロパティで、**FMTClerkWorkspace** と入力します。</span><span class="sxs-lookup"><span data-stu-id="71815-169">In the **Name** property, enter **FMTClerkWorkspace**.</span></span>
3.  <span data-ttu-id="71815-170">**追加** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="71815-170">Click **Add**.</span></span>
4.  <span data-ttu-id="71815-171">新しいメニュー項目の次のプロパティを指定します。</span><span class="sxs-lookup"><span data-stu-id="71815-171">Specify the following properties for the new menu item.</span></span>

    | <span data-ttu-id="71815-172">**プロパティ**</span><span class="sxs-lookup"><span data-stu-id="71815-172">**Property**</span></span> | <span data-ttu-id="71815-173">**値**</span><span class="sxs-lookup"><span data-stu-id="71815-173">**Value**</span></span>                       |
    |--------------|---------------------------------|
    | <span data-ttu-id="71815-174">ラベル</span><span class="sxs-lookup"><span data-stu-id="71815-174">Label</span></span>        | <span data-ttu-id="71815-175">予約管理チュートリアル</span><span class="sxs-lookup"><span data-stu-id="71815-175">Reservation management tutorial</span></span> |
    | <span data-ttu-id="71815-176">オブジェクト</span><span class="sxs-lookup"><span data-stu-id="71815-176">Object</span></span>       | <span data-ttu-id="71815-177">FMTClerkWorkspace</span><span class="sxs-lookup"><span data-stu-id="71815-177">FMTClerkWorkspace</span></span>               |

### <a name="create-a-tile-that-points-to-the-fmtclerkworkspace-workspace-menu-item"></a><span data-ttu-id="71815-178">FMTClerkWorkspace ワークスペース メニュー項目をポイントするタイルを作成する</span><span class="sxs-lookup"><span data-stu-id="71815-178">Create a tile that points to the FMTClerkWorkspace workspace menu item</span></span>

1.  <span data-ttu-id="71815-179">**FMTutorial** を右クリックして **追加** をポイントしてから **新しい項目** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="71815-179">Right-click **FMTutorial**, point to **Add**, and then click **New Item**.</span></span>
2.  <span data-ttu-id="71815-180">**AX アーティファクト** &gt; **ユーザー インターフェイス** &gt; **タイル** の順にクリックします。</span><span class="sxs-lookup"><span data-stu-id="71815-180">Click **AX Artifacts** &gt; **User Interface** &gt; **Tile**.</span></span> <span data-ttu-id="71815-181">**名前**プロパティで、**FMTClerkWorkspace** と入力します。</span><span class="sxs-lookup"><span data-stu-id="71815-181">In the **Name** property, enter **FMTClerkWorkspace**.</span></span>
3.  <span data-ttu-id="71815-182">**追加** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="71815-182">Click **Add**.</span></span>
4.  <span data-ttu-id="71815-183">新しいタイルの次のプロパティを指定します。</span><span class="sxs-lookup"><span data-stu-id="71815-183">Specify the following properties for the new tile.</span></span>

    | <span data-ttu-id="71815-184">**プロパティ**</span><span class="sxs-lookup"><span data-stu-id="71815-184">**Property**</span></span> | <span data-ttu-id="71815-185">**値**</span><span class="sxs-lookup"><span data-stu-id="71815-185">**Value**</span></span>         |
    |--------------|-------------------|
    | <span data-ttu-id="71815-186">MenuItemName</span><span class="sxs-lookup"><span data-stu-id="71815-186">MenuItemName</span></span> | <span data-ttu-id="71815-187">FMTClerkWorkspace</span><span class="sxs-lookup"><span data-stu-id="71815-187">FMTClerkWorkspace</span></span> |

### <a name="add-a-menu-extension-for-the-navigation-pane"></a><span data-ttu-id="71815-188">ナビゲーション ウィンドウのメニューの拡張機能を追加します。</span><span class="sxs-lookup"><span data-stu-id="71815-188">Add a menu extension for the navigation pane</span></span>

1.  <span data-ttu-id="71815-189">**アプリケーション エクスプローラー**で、**ユーザー インターフェイス** &gt; **メニュー**とクリックし、**NavPaneMenu** を右クリックしてから**拡張機能を作成**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="71815-189">In **Application Explorer**, click **User Interface** &gt; **Menus**, right-click **NavPaneMenu**, and then click **Create extension**.</span></span>
2.  <span data-ttu-id="71815-190">**ソリューション エクスプローラー**で、**NavPaneMenu.Extension** をダブルクリックします。</span><span class="sxs-lookup"><span data-stu-id="71815-190">In **Solution Explorer**, double-click **NavPaneMenu.Extension**.</span></span>
3.  <span data-ttu-id="71815-191">デザイナーで、**NavPaneMenu.Extension** を右クリックし、**新規**をポイントしてから**サブメニュー**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="71815-191">In the designer, right-click **NavPaneMenu.Extension**, point to **New**, and then click **Submenu**.</span></span>
4.  <span data-ttu-id="71815-192">新しいサブメニューを選択します。</span><span class="sxs-lookup"><span data-stu-id="71815-192">Select the new submenu.</span></span> <span data-ttu-id="71815-193">**名前**プロパティで、**NavPaneMenuFleetTutorial** と入力します。</span><span class="sxs-lookup"><span data-stu-id="71815-193">In the **Name** property, enter **NavPaneMenuFleetTutorial**.</span></span>
5.  <span data-ttu-id="71815-194">**ソリューション エクスプローラー**または**アプリケーション エクスプローラー**で、**FMTClerkWorkspace** タイルを探し、新しく作成されたサブメニューにドラッグします。</span><span class="sxs-lookup"><span data-stu-id="71815-194">In **Solution Explorer** or **Application Explorer**, locate the **FMTClerkWorkspace** tile, and drag it onto the newly created submenu.</span></span> <span data-ttu-id="71815-195">**保存** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="71815-195">Click **Save**.</span></span>
6.  <span data-ttu-id="71815-196">**FMTutorial** を右クリックし、**再ビルド** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="71815-196">Right-click **FMTutorial**, and then click **Rebuild**.</span></span>
7.  <span data-ttu-id="71815-197">**Ctrl+F5** キーを押してプロジェクトを実行します。</span><span class="sxs-lookup"><span data-stu-id="71815-197">Press **Ctrl+F5** to run the project.</span></span> <span data-ttu-id="71815-198">プロジェクトをビルドして実行すると、ナビゲーション ウィンドウに新しいワークスペースへのリンクが含まれます。</span><span class="sxs-lookup"><span data-stu-id="71815-198">After you build and run the project, the navigation pane will contain a link to the new workspace.</span></span> <span data-ttu-id="71815-199">アプリケーション ウィンドウの右上にある、ナビゲーション ウィンドウのボタン (3 つの明細行) をクリックして、ナビゲーション ウィンドウを開きます。</span><span class="sxs-lookup"><span data-stu-id="71815-199">Open the navigation pane by clicking the navigation pane button (three lines) at the top right of the application window.</span></span> 

    <span data-ttu-id="71815-200">[![Nav2](./media/nav2.png)](./media/nav2.png)</span><span class="sxs-lookup"><span data-stu-id="71815-200">[![Nav2](./media/nav2.png)](./media/nav2.png)</span></span>

8.  <span data-ttu-id="71815-201">ナビゲーション ウィンドウを開いたら、**すべてのワークスペース** を選択し、それを開いた後、一覧を下方向にスクロールします。</span><span class="sxs-lookup"><span data-stu-id="71815-201">When you open the navigation pane, select **All workspaces**, and scroll down in the list after it opens.</span></span> <span data-ttu-id="71815-202">以下の新しい予約管理チュートリアル ワークスペースが一覧に表示されます。</span><span class="sxs-lookup"><span data-stu-id="71815-202">You should see the following new Reservation management tutorial workspace in the list.</span></span> 

    <span data-ttu-id="71815-203">[![Nav3](./media/nav3.png)](./media/nav3.png)</span><span class="sxs-lookup"><span data-stu-id="71815-203">[![Nav3](./media/nav3.png)](./media/nav3.png)</span></span>

### <a name="add-the-form-to-the-main-menu-structure"></a><span data-ttu-id="71815-204">メイン メニュー構造へのフォームの追加</span><span class="sxs-lookup"><span data-stu-id="71815-204">Add the form to the main menu structure</span></span>

<span data-ttu-id="71815-205">ここで、チュートリアル ワークスペースを示すタイルを含む新しいメイン メニュー セクションを追加します。</span><span class="sxs-lookup"><span data-stu-id="71815-205">Now you’ll add a new main menu section that contains a tile that points to the tutorial workspace.</span></span> <span data-ttu-id="71815-206">次に、このセクションの同じフォームにリンクを追加します。</span><span class="sxs-lookup"><span data-stu-id="71815-206">You will then add a link to the same form in this section.</span></span> <span data-ttu-id="71815-207">これは、非ワークスペースのフォーム リンクの外観を示します。</span><span class="sxs-lookup"><span data-stu-id="71815-207">This will demonstrate the appearance of a non-workspace form link.</span></span>

1.  <span data-ttu-id="71815-208">Visual Studio の、**ソリューション エクスプローラー** で、**FMTutorial** を右クリックして、**追加** をポイントしてから、**新しい項目** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="71815-208">In Visual Studio, in **Solution Explorer**, right-click **FMTutorial**, point to **Add**, and then click **New Item**.</span></span>
2.  <span data-ttu-id="71815-209">**AX アーティファクト** &gt; **ユーザー インターフェイス** &gt; **メニュー** の順にクリックします。</span><span class="sxs-lookup"><span data-stu-id="71815-209">Click **AX Artifacts** &gt; **User Interface** &gt; **Menu**.</span></span> <span data-ttu-id="71815-210">**名前**プロパティで、**FleetManagementTutorial** と入力します。</span><span class="sxs-lookup"><span data-stu-id="71815-210">In the **Name** property, enter **FleetManagementTutorial**.</span></span>
3.  <span data-ttu-id="71815-211">**追加** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="71815-211">Click **Add**.</span></span>
4.  <span data-ttu-id="71815-212">**ソリューション エクスプローラー**で、新しいメニュー **FleetManagementTutorial** をまだ開いていない場合はダブルクリックします。</span><span class="sxs-lookup"><span data-stu-id="71815-212">In **Solution Explorer**, double-click the new menu **FleetManagementTutorial** if it isn’t already open.</span></span>
5.  <span data-ttu-id="71815-213">プロパティ リストで、**ラベル** プロパティを**フリート管理のチュートリアル**に設定します。</span><span class="sxs-lookup"><span data-stu-id="71815-213">In the properties list, set the **Label** property to **Fleet management tutorial**.</span></span>
6.  <span data-ttu-id="71815-214">デザイナーで、**FleetManagementTutorial** を右クリックして、**新規** &gt; **サブメニュー**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="71815-214">In the designer, right-click **FleetManagementTutorial**, and click **New** &gt; **Submenu**.</span></span>
7.  <span data-ttu-id="71815-215">新しいサブメニューの次のプロパティを指定します。</span><span class="sxs-lookup"><span data-stu-id="71815-215">Specify the following properties for the new submenu.</span></span>

    | <span data-ttu-id="71815-216">**プロパティ**</span><span class="sxs-lookup"><span data-stu-id="71815-216">**Property**</span></span> | <span data-ttu-id="71815-217">**値**</span><span class="sxs-lookup"><span data-stu-id="71815-217">**Value**</span></span>  |
    |--------------|------------|
    | <span data-ttu-id="71815-218">氏名</span><span class="sxs-lookup"><span data-stu-id="71815-218">Name</span></span>         | <span data-ttu-id="71815-219">ワークスペース</span><span class="sxs-lookup"><span data-stu-id="71815-219">Workspaces</span></span> |
    | <span data-ttu-id="71815-220">ラベル</span><span class="sxs-lookup"><span data-stu-id="71815-220">Label</span></span>        | <span data-ttu-id="71815-221">ワークスペース</span><span class="sxs-lookup"><span data-stu-id="71815-221">Workspaces</span></span> |

8.  <span data-ttu-id="71815-222">**ソリューション エクスプローラー**または**アプリケーション エクスプローラー**で、**FMTClerkWorkspace** 表示メニュー項目を探し、新しい**ワークスペース** サブメニューにドラッグします。</span><span class="sxs-lookup"><span data-stu-id="71815-222">In **Solution Explorer** or **Application Explorer**, locate the **FMTClerkWorkspace** display menu item and drag it onto the new **Workspaces** submenu.</span></span>
9.  <span data-ttu-id="71815-223">デザイナーで、**FleetManagementTutorial** を右クリックしてから、**新規** &gt; **サブメニュー**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="71815-223">In the designer, right-click **FleetManagementTutorial**, and then click **New** &gt; **Submenu**.</span></span>
10. <span data-ttu-id="71815-224">新しいサブメニューの次のプロパティを指定します。</span><span class="sxs-lookup"><span data-stu-id="71815-224">Specify the following properties for the new submenu.</span></span>

    | <span data-ttu-id="71815-225">**プロパティ**</span><span class="sxs-lookup"><span data-stu-id="71815-225">**Property**</span></span> | <span data-ttu-id="71815-226">**値**</span><span class="sxs-lookup"><span data-stu-id="71815-226">**Value**</span></span> |
    |--------------|-----------|
    | <span data-ttu-id="71815-227">氏名</span><span class="sxs-lookup"><span data-stu-id="71815-227">Name</span></span>         | <span data-ttu-id="71815-228">共通</span><span class="sxs-lookup"><span data-stu-id="71815-228">Common</span></span>    |
    | <span data-ttu-id="71815-229">ラベル</span><span class="sxs-lookup"><span data-stu-id="71815-229">Label</span></span>        | <span data-ttu-id="71815-230">共通</span><span class="sxs-lookup"><span data-stu-id="71815-230">Common</span></span>    |

11. <span data-ttu-id="71815-231">**ソリューション エクスプローラー**または**アプリケーション エクスプローラー**で、**FMTClerkWorkspace** 表示メニュー項目を探し、新しい**共通**サブメニューにドラッグします。</span><span class="sxs-lookup"><span data-stu-id="71815-231">In **Solution Explorer** or **Application Explorer**, locate the **FMTClerkWorkspace** display menu item and drag it onto the new **Common** submenu.</span></span>
12. <span data-ttu-id="71815-232">**アプリケーション エクスプローラー**で、**ユーザー インターフェイス** &gt; **メニュー** &gt; **MainMenu** とクリックします。</span><span class="sxs-lookup"><span data-stu-id="71815-232">In **Application Explorer**, click **User Interface** &gt; **Menus** &gt; **MainMenu**.</span></span> <span data-ttu-id="71815-233">**MainMenu** を右クリックし、**拡張子の作成** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="71815-233">Right-click **MainMenu**, and then click **Create extension**.</span></span>
13. <span data-ttu-id="71815-234">**ソリューション エクスプローラー**で新しい拡張機能を探して開きます。</span><span class="sxs-lookup"><span data-stu-id="71815-234">In **Solution Explorer**, locate and open the new extension.</span></span> <span data-ttu-id="71815-235">**MainMenu.Extension** を選択し、ダブルクリックして開きます。</span><span class="sxs-lookup"><span data-stu-id="71815-235">Select and double-click **MainMenu.Extension** to open it.</span></span>
14. <span data-ttu-id="71815-236">デザイナーで、**MainMenu.Extension** を右クリックし、**新規**をポイントしてから**メニュー参照**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="71815-236">In the designer, right click **MainMenu.Extension**, point to **New**, and then click **Menu reference**.</span></span>
15. <span data-ttu-id="71815-237">新しいメニュー参照の次のプロパティを指定します。</span><span class="sxs-lookup"><span data-stu-id="71815-237">Specify the following properties for the new menu reference.</span></span>

    | <span data-ttu-id="71815-238">**プロパティ**</span><span class="sxs-lookup"><span data-stu-id="71815-238">**Property**</span></span> | <span data-ttu-id="71815-239">**値**</span><span class="sxs-lookup"><span data-stu-id="71815-239">**Value**</span></span>               |
    |--------------|-------------------------|
    | <span data-ttu-id="71815-240">氏名</span><span class="sxs-lookup"><span data-stu-id="71815-240">Name</span></span>         | <span data-ttu-id="71815-241">FleetManagementTutorial</span><span class="sxs-lookup"><span data-stu-id="71815-241">FleetManagementTutorial</span></span> |
    | <span data-ttu-id="71815-242">メニュー名</span><span class="sxs-lookup"><span data-stu-id="71815-242">Menu Name</span></span>    | <span data-ttu-id="71815-243">FleetManagementTutorial</span><span class="sxs-lookup"><span data-stu-id="71815-243">FleetManagementTutorial</span></span> |

16. <span data-ttu-id="71815-244">**保存** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="71815-244">Click **Save**.</span></span>
17. <span data-ttu-id="71815-245">**FMTutorial** を右クリックし、**ビルド** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="71815-245">Right-click **FMTutorial**, and then click **Build**.</span></span>
18. <span data-ttu-id="71815-246">**Ctrl+F5** キーを押してプロジェクトを実行します。</span><span class="sxs-lookup"><span data-stu-id="71815-246">Press **Ctrl+F5** to run the project.</span></span>
19. <span data-ttu-id="71815-247">変更したメイン メニューのセクションに移動します。</span><span class="sxs-lookup"><span data-stu-id="71815-247">Go to the main menu section you just modified.</span></span> <span data-ttu-id="71815-248">ナビゲーション ウィンドウを開いて、新しいトップレベルの**フリート管理のチュートリアル**メニューが表示されるまでスクロールします。</span><span class="sxs-lookup"><span data-stu-id="71815-248">Open the navigation pane and scroll down until you see the new top-level **Fleet management tutorial** menu.</span></span> <span data-ttu-id="71815-249">**Ctrl+F5** を押して、ブラウザー キャッシュをクリアすることが必要な場合があります。</span><span class="sxs-lookup"><span data-stu-id="71815-249">You may need to clear your browser cache by pressing **Ctrl+F5**.</span></span> 

    <span data-ttu-id="71815-250">[![Nav4](./media/nav4.png)](./media/nav4.png)</span><span class="sxs-lookup"><span data-stu-id="71815-250">[![Nav4](./media/nav4.png)](./media/nav4.png)</span></span>

20. <span data-ttu-id="71815-251">そのサブメニューを展開するには、**フリート管理のチュートリアル** &gt; **ワークスペース**とクリックします。</span><span class="sxs-lookup"><span data-stu-id="71815-251">Click **Fleet management tutorial** &gt; **Workspaces** to expand that submenu.</span></span> <span data-ttu-id="71815-252">ナビゲーション ウィンドウは、次のようになります。</span><span class="sxs-lookup"><span data-stu-id="71815-252">Your navigation pane should look like the following.</span></span> 

    <span data-ttu-id="71815-253">[![Nav5](./media/nav5.png)](./media/nav5.png)</span><span class="sxs-lookup"><span data-stu-id="71815-253">[![Nav5](./media/nav5.png)](./media/nav5.png)</span></span> 

    <span data-ttu-id="71815-254">**一般的な** サブメニューをクリックすると、モデル化されているメニュー項目が表示されます。</span><span class="sxs-lookup"><span data-stu-id="71815-254">If you click on the **Common** submenu, you will see the menu item that you modeled there.</span></span> <span data-ttu-id="71815-255">これらのリンクのいずれかをクリックして、参照を正しく設定したか確認することができます。</span><span class="sxs-lookup"><span data-stu-id="71815-255">You can click either of these links to check that you have set up the references correctly.</span></span> <span data-ttu-id="71815-256">参照を正しく設定した場合は、作成中のチュートリアル ワークスペースをクリックすると、開きます。</span><span class="sxs-lookup"><span data-stu-id="71815-256">If you have set up the references correctly, the tutorial workspace you’re working on should open when clicked on.</span></span>




