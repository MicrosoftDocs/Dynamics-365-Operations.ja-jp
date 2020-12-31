---
title: 顧客フォームの構築
description: このラボでは、マスター詳細フォームを作成し、適切なフォームのパターンおよびサブパターンを適用します。 マスター詳細フォームには、多数のフィールドが含まれるプライマリ データが表示されます。 たとえば、作成するフォームは、顧客情報を表示します。
author: jasongre
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.custom: 20401
ms.assetid: 78199ae8-0631-4cf4-b206-b952f09b92a9
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 40d32a6de03b792d4e95d9c22a6046126d79c02d
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/05/2020
ms.locfileid: "4682465"
---
# <a name="build-the-customer-form"></a><span data-ttu-id="628ae-105">顧客フォームの構築</span><span class="sxs-lookup"><span data-stu-id="628ae-105">Build the Customer form</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="628ae-106">このラボでは、マスター詳細フォームを作成し、適切なフォームのパターンおよびサブパターンを適用します。</span><span class="sxs-lookup"><span data-stu-id="628ae-106">In this lab you’ll create a Master Details form and apply the appropriate form pattern and subpatterns.</span></span> <span data-ttu-id="628ae-107">マスター詳細フォームには、多数のフィールドが含まれるプライマリ データが表示されます。</span><span class="sxs-lookup"><span data-stu-id="628ae-107">A Master Details form shows primary data that has many fields.</span></span> <span data-ttu-id="628ae-108">たとえば、作成するフォームは、顧客情報を表示します。</span><span class="sxs-lookup"><span data-stu-id="628ae-108">For example, the form that you create will show customer information.</span></span>

<a name="prerequisites"></a><span data-ttu-id="628ae-109">前提条件</span><span class="sxs-lookup"><span data-stu-id="628ae-109">Prerequisites</span></span>
-------------

<span data-ttu-id="628ae-110">このチュートリアルでは、リモート デスクトップを使用して環境にアクセスし、インスタンスの管理者としてプロビジョニングされる必要があります。</span><span class="sxs-lookup"><span data-stu-id="628ae-110">For this tutorial, you will need to access the environment using Remote Desktop, and be provisioned as an administrator on the instance.</span></span> <span data-ttu-id="628ae-111">詳細については、「[アクセス インスタンス](../dev-tools/access-instances.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="628ae-111">For more information, see [Access Instances](../dev-tools/access-instances.md).</span></span>

## <a name="overview"></a><span data-ttu-id="628ae-112">概要</span><span class="sxs-lookup"><span data-stu-id="628ae-112">Overview</span></span>
<span data-ttu-id="628ae-113">フォームを作成するには、既存のフォーム **FmtCustomer** から開始します。</span><span class="sxs-lookup"><span data-stu-id="628ae-113">To create the form, you’ll start from the existing form, **FmtCustomer**.</span></span> <span data-ttu-id="628ae-114">フォームは、古いマスター詳細テンプレートをテーブルします。</span><span class="sxs-lookup"><span data-stu-id="628ae-114">The form represents the old Master Details template.</span></span> <span data-ttu-id="628ae-115">チュートリアルの一環として、このフォーム タイプに一貫した構造を実行するマスターの詳細パターンを適用します。</span><span class="sxs-lookup"><span data-stu-id="628ae-115">As a part of the tutorial, you’ll apply the Master Details pattern, which will enforce a consistent structure for this form type.</span></span> <span data-ttu-id="628ae-116">次の図は、**FmtCustomer** 開始コンポーネントを示しています。</span><span class="sxs-lookup"><span data-stu-id="628ae-116">The following illustration shows the **FmtCustomer** starting artifact.</span></span> 

<span data-ttu-id="628ae-117">[![FmtCustomer 開始コンポーネントのスクリーン ショット](./media/custform1.png)](./media/custform1.png)</span><span class="sxs-lookup"><span data-stu-id="628ae-117">[![Screen shot of FmtCustomer starting artifact](./media/custform1.png)](./media/custform1.png)</span></span>

## <a name="key-concepts"></a><span data-ttu-id="628ae-118">重要な概念</span><span class="sxs-lookup"><span data-stu-id="628ae-118">Key concepts</span></span>
-   <span data-ttu-id="628ae-119">マスター詳細フォームを作成します。</span><span class="sxs-lookup"><span data-stu-id="628ae-119">Create a Master Details form.</span></span>
-   <span data-ttu-id="628ae-120">フォームにフォーム パターンを適用します。</span><span class="sxs-lookup"><span data-stu-id="628ae-120">Apply a form pattern to a form.</span></span>
-   <span data-ttu-id="628ae-121">Visual Studio のパターン アドインを使用して、フォーム/モデル パターンのカバレッジに関する情報を取得します。</span><span class="sxs-lookup"><span data-stu-id="628ae-121">Use the Visual Studio pattern add-ins to get information about form/model pattern coverage.</span></span>
-   <span data-ttu-id="628ae-122">フォーム コントロールにサブパターンを適用します。</span><span class="sxs-lookup"><span data-stu-id="628ae-122">Apply subpatterns to form controls.</span></span>
-   <span data-ttu-id="628ae-123">Visual Studio とブラウザーを使用してフォームを表示します。</span><span class="sxs-lookup"><span data-stu-id="628ae-123">View the form using Visual Studio and a browser.</span></span>
-   <span data-ttu-id="628ae-124">モデル内で残っているパターンの作業の量を決定します。</span><span class="sxs-lookup"><span data-stu-id="628ae-124">Determine the amount of remaining patterns work in a model.</span></span>

## <a name="setup"></a><span data-ttu-id="628ae-125">セットアップ</span><span class="sxs-lookup"><span data-stu-id="628ae-125">Setup</span></span>
### <a name="import-the-tutorial-project-and-transactional-data"></a><span data-ttu-id="628ae-126">チュートリアル プロジェクトおよびトランザクション データのインポート</span><span class="sxs-lookup"><span data-stu-id="628ae-126">Import the tutorial project and transactional data</span></span>

<span data-ttu-id="628ae-127">Visual Studio を使用してチュートリアル プロジェクトをインポートします。</span><span class="sxs-lookup"><span data-stu-id="628ae-127">Use Visual Studio to import the tutorial project.</span></span> <span data-ttu-id="628ae-128">チュートリアル プロジェクトには、このチュートリアルを完了するために使用する成果物が含まれています。</span><span class="sxs-lookup"><span data-stu-id="628ae-128">The tutorial project includes the artifacts you will use to complete this tutorial.</span></span> <span data-ttu-id="628ae-129">Visual Studio を使用して FMTutorial プロジェクトを開き、チュートリアル用のデータを読み込みます。</span><span class="sxs-lookup"><span data-stu-id="628ae-129">Use Visual Studio to open the FMTutorial project and load the data for the tutorial.</span></span> <span data-ttu-id="628ae-130">フリート管理チュートリアルのデータを読み込むために、FMTDataHelper クラスを使用します。</span><span class="sxs-lookup"><span data-stu-id="628ae-130">You will use the FMTDataHelper class to load data for the Fleet Management tutorial.</span></span> <span data-ttu-id="628ae-131">これが作業する最初のチュートリアルである場合は、[アクセス インスタンス](../dev-tools/access-instances.md)を確認し、ローカル VM で作業している場合に、管理者ユーザーを提供するかどうかを確認します。</span><span class="sxs-lookup"><span data-stu-id="628ae-131">If this is the first tutorial you are working on, review [Access Instances](../dev-tools/access-instances.md) and make sure you provision your administrator user if you’re working on a local VM.</span></span>

1.  <span data-ttu-id="628ae-132">フリート管理のサンプルを <https://github.com/Microsoft/FMLab> からダウンロードし、**C:\\** に保存してから解凍します。</span><span class="sxs-lookup"><span data-stu-id="628ae-132">Download the Fleet Management sample from <https://github.com/Microsoft/FMLab>, save it to **C:\\**, and unzip it.</span></span>
2.  <span data-ttu-id="628ae-133">デスクトップで、Visual Studio ショートカットをダブルクリックして、開発環境を開きます。</span><span class="sxs-lookup"><span data-stu-id="628ae-133">On the desktop, double-click the Visual Studio shortcut to open the development environment.</span></span>
3.  <span data-ttu-id="628ae-134">**Finance and Operations** メニューで、**プロジェクトのインポート** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="628ae-134">On the **Finance and Operations** menu, click **Import Project**.</span></span>
4.  <span data-ttu-id="628ae-135">**プロジェクトのインポート** ウィンドウで、**ファイル名** テキスト ボックスの隣にある、省略記号ボタンをクリックします。</span><span class="sxs-lookup"><span data-stu-id="628ae-135">In the **Import Project** window, next to the **Filename** text box, click the ellipsis button.</span></span>
5.  <span data-ttu-id="628ae-136">**インポートするファイルの選択** ウィンドウで、**C:\FMLab** を参照して FMTutorialDataModel.axpp をクリックしてから **開く** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="628ae-136">In the **Select the file to import** window, browse to **C:\FMLab**, click FMTutorialDataModel.axpp, and then click **Open**.</span></span>
6.  <span data-ttu-id="628ae-137">**プロジェクト ファイルの場所** テキスト ボックスに、**C:\FMLab** と入力します。</span><span class="sxs-lookup"><span data-stu-id="628ae-137">In the **Project file location** text box, enter **C:\FMLab**.</span></span>
7.  <span data-ttu-id="628ae-138">**要素の上書き** オプションをオンにし、**現在のソリューション** ラジオ オプションをオンにします。</span><span class="sxs-lookup"><span data-stu-id="628ae-138">Select the **Overwrite Elements** option and the **Current solution** radio button.</span></span> <span data-ttu-id="628ae-139">次の図は、完了した **インポート プロジェクト** ダイアログ ボックスを示しています。</span><span class="sxs-lookup"><span data-stu-id="628ae-139">The following illustration shows the completed **Import Project** dialog box.</span></span> 

    ![完了したプロジェクトのインポート ダイアログ ボックス](./media/custform2.png)

8.  <span data-ttu-id="628ae-141">**OK** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="628ae-141">Click **OK**.</span></span>
9.  <span data-ttu-id="628ae-142">**ソリューション エクスプローラー** で、**クラス** を展開して、**FMTutorial** プロジェクトで **FMTDataHelper** を右クリックしてから、**スタートアップ オブジェクトとして設定** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="628ae-142">In **Solution Explorer**, expand **Classes**, and under the **FMTutorial** project, right-click **FMTDataHelper**, and then click **Set as Startup Object**.</span></span>
10. <span data-ttu-id="628ae-143">**ビルド** メニューで、**ソリューションの再構築** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="628ae-143">On the **Build** menu, click **Rebuild Solution**.</span></span> <span data-ttu-id="628ae-144">タイムスタンプに関係なく、プロジェクトのすべてのファイルを確実に作成するには、リビルドを使用します。</span><span class="sxs-lookup"><span data-stu-id="628ae-144">You use the rebuild to make sure all files in the project are built regardless of timestamps.</span></span> <span data-ttu-id="628ae-145">出力ウィンドウでビルドの進行状況を表示できます。</span><span class="sxs-lookup"><span data-stu-id="628ae-145">You can view the build progress in the Output window.</span></span>
11. <span data-ttu-id="628ae-146">ビルドが完了すると、**Ctrl + F5** を押してプロジェクトを実行します。</span><span class="sxs-lookup"><span data-stu-id="628ae-146">After the build completes, press **Ctrl+F5** to run the project.</span></span> <span data-ttu-id="628ae-147">ブラウザーが開き、データをインポートするクラスが実行されます。</span><span class="sxs-lookup"><span data-stu-id="628ae-147">The browser will open and run the class that imports the data.</span></span>

## <a name="open-the-fmtutorial-project"></a><span data-ttu-id="628ae-148">FMTutorial プロジェクトを開く</span><span class="sxs-lookup"><span data-stu-id="628ae-148">Open the FMTutorial project</span></span>
<span data-ttu-id="628ae-149">Visual Studio を使用して FMTutorial プロジェクトを開きます。</span><span class="sxs-lookup"><span data-stu-id="628ae-149">Use Visual Studio to open the FMTutorial project.</span></span> <span data-ttu-id="628ae-150">Visual Studio を開き、FMTutorial プロジェクトが既に読み込まれている場合は、次のセクションに続行することができます。</span><span class="sxs-lookup"><span data-stu-id="628ae-150">If you have Visual Studio open and have already loaded the FMTutorial project, you can continue to the next section.</span></span>

1.  <span data-ttu-id="628ae-151">開発環境がまだ開いていない場合は、デスクトップで開発環境への Visual Studio ショートカットをダブルクリックして開発環境を開きます。</span><span class="sxs-lookup"><span data-stu-id="628ae-151">If the development environment is not already open, on the Desktop, double-click the Visual Studio shortcut to open the development environment.</span></span>
2.  <span data-ttu-id="628ae-152">**ファイル** メニューで、**開く** &gt; **プロジェクト/ソリューション** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="628ae-152">On the **File** menu, click **Open** &gt; **Project/Solution**.</span></span>
3.  <span data-ttu-id="628ae-153">**プロジェクトを開く** ダイアログ ボックスで、C:\FmLab\FMTutorial を参照し、**FMTutorial** ソリューションを選択してから **開く** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="628ae-153">In the **Open Project** dialog box, browse to C:\FmLab\FMTutorial, select the **FMTutorial** solution, and then click **Open**.</span></span>
4.  <span data-ttu-id="628ae-154">FMTutorial プロジェクトが **ソリューション エクスプローラー** に表示されます。</span><span class="sxs-lookup"><span data-stu-id="628ae-154">The FMTutorial project appears in **Solution Explorer**.</span></span>

## <a name="use-a-template-to-create-the-form"></a><span data-ttu-id="628ae-155">テンプレートを使用してフォームを作成</span><span class="sxs-lookup"><span data-stu-id="628ae-155">Use a template to create the form</span></span>
<span data-ttu-id="628ae-156">Visual Studio を使用して **FmtCustomer** フォームを作成します。</span><span class="sxs-lookup"><span data-stu-id="628ae-156">Use Visual Studio to create the **FmtCustomer** form.</span></span> <span data-ttu-id="628ae-157">テンプレートを使用して、新しいマスターの詳細フォームを作成します。</span><span class="sxs-lookup"><span data-stu-id="628ae-157">You’ll use a template to create a new master details form.</span></span> <span data-ttu-id="628ae-158">このチュートリアルのデータ ソースは、スターター形式によって提供されています。</span><span class="sxs-lookup"><span data-stu-id="628ae-158">The data source for this tutorial is provided by the starter form.</span></span> <span data-ttu-id="628ae-159">ただし、グリッドと詳細ビューにフィールドを追加し、マスター詳細フォーム パターンを適用します。</span><span class="sxs-lookup"><span data-stu-id="628ae-159">However, you’ll add fields to the grid and details view and apply the Master Details form pattern.</span></span>

1.  <span data-ttu-id="628ae-160">**ソリューション エクスプローラー** で、**FMTutorial** プロジェクトを右クリックして **追加** をポイントしてから **既存の項目** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="628ae-160">In **Solution Explorer**, right-click the **FMTutorial** project, point to **Add**, and then click **Existing Item**.</span></span>
2.  <span data-ttu-id="628ae-161">**既存の品目を追加** ウィンドウで、C:\FmLab を参照し、**AxForm\_FmtCustomer** を選択してから **追加** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="628ae-161">In the **Add Existing Item** window, browse to C:\FmLab, select **AxForm\_FmtCustomer**, and then click **Add**.</span></span> <span data-ttu-id="628ae-162">ソリューション エクスプローラーの **FMTutorial** プロジェクトの下に **FmtCustomer** フォームが表示されます。</span><span class="sxs-lookup"><span data-stu-id="628ae-162">The **FmtCustomer** form appears at the bottom of the **FMTutorial** project in Solution Explorer.</span></span>
3.  <span data-ttu-id="628ae-163">ソリューション エクスプローラーで、**FmtCustomer** をダブルクリックします。</span><span class="sxs-lookup"><span data-stu-id="628ae-163">In Solution Explorer, double-click **FmtCustomer**.</span></span> <span data-ttu-id="628ae-164">フォーム デザイナーで、フォームを開きます。</span><span class="sxs-lookup"><span data-stu-id="628ae-164">The form opens in the form designer.</span></span>
4.  <span data-ttu-id="628ae-165">フォーム デザイナーで、**デザイン** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="628ae-165">In the Form designer, click **Design**.</span></span> <span data-ttu-id="628ae-166">**プロパティ** ウィンドウで、次の値を指定します。</span><span class="sxs-lookup"><span data-stu-id="628ae-166">In the **Properties** window, specify the following values.</span></span>

    | <span data-ttu-id="628ae-167">**プロパティ**</span><span class="sxs-lookup"><span data-stu-id="628ae-167">**Property**</span></span> | <span data-ttu-id="628ae-168">**値**</span><span class="sxs-lookup"><span data-stu-id="628ae-168">**Value**</span></span>   |
    |--------------|-------------|
    | <span data-ttu-id="628ae-169">データ ソース</span><span class="sxs-lookup"><span data-stu-id="628ae-169">Data Source</span></span>  | <span data-ttu-id="628ae-170">FmtCustomer</span><span class="sxs-lookup"><span data-stu-id="628ae-170">FmtCustomer</span></span> |
    | <span data-ttu-id="628ae-171">キャプション</span><span class="sxs-lookup"><span data-stu-id="628ae-171">Caption</span></span>      | <span data-ttu-id="628ae-172">顧客</span><span class="sxs-lookup"><span data-stu-id="628ae-172">Customers</span></span>   |

5.  <span data-ttu-id="628ae-173">フォーム デザイナーで、**デザイン** &gt; **GridDetailsTab** &gt; **TabPageGrid** &gt; **MainGrid** とクリックしてから **MainGrid** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="628ae-173">In the Form designer, click **Design** &gt; **GridDetailsTab** &gt; **TabPageGrid** &gt; **MainGrid**, and then click **MainGrid**.</span></span>
6.  <span data-ttu-id="628ae-174">**プロパティ** ウィンドウで、**データ ソース** をクリックしてから **FmtCustomer** を選択して **FmtCustomer** テーブルをグリッドにバインドします。</span><span class="sxs-lookup"><span data-stu-id="628ae-174">In the **Properties** window, click **Data Source**, and then select **FmtCustomer** to bind the **FmtCustomer** table to the grid.</span></span> <span data-ttu-id="628ae-175">データ ソースからのフィールドを使用して、グリッドに列を追加できるようになりました。</span><span class="sxs-lookup"><span data-stu-id="628ae-175">You can now use the fields from the data source to add columns to the grid.</span></span>
7.  <span data-ttu-id="628ae-176">**データ ソース** &gt; **FmtCustomer** &gt; **フィールド** とクリックし、グリッドにフィールドを追加します。</span><span class="sxs-lookup"><span data-stu-id="628ae-176">Click **Data sources** &gt; **FmtCustomer** &gt; **Fields** to add fields to the grid.</span></span>
    1.  <span data-ttu-id="628ae-177">**名** をクリックし、**Ctrl** キーを押しながら、表示された順序で次の追加フィールドを選択します。</span><span class="sxs-lookup"><span data-stu-id="628ae-177">Click **FirstName**, press and hold the **Ctrl** key, and then select the following additional fields in the order shown:</span></span>
        - <span data-ttu-id="628ae-178">姓</span><span class="sxs-lookup"><span data-stu-id="628ae-178">LastName</span></span>
        - <span data-ttu-id="628ae-179">CellPhone</span><span class="sxs-lookup"><span data-stu-id="628ae-179">CellPhone</span></span>
        - <span data-ttu-id="628ae-180">DriverLicense</span><span class="sxs-lookup"><span data-stu-id="628ae-180">DriverLicense</span></span>
        - <span data-ttu-id="628ae-181">電子メール</span><span class="sxs-lookup"><span data-stu-id="628ae-181">Email</span></span>

    2.  <span data-ttu-id="628ae-182">協調表示されたフィールドを **Design** &gt; **GridDetailsTab**&gt; **TabPageGrid** &gt; **MainGrid** にドラッグします。</span><span class="sxs-lookup"><span data-stu-id="628ae-182">Drag the highlighted fields to **Design** &gt; **GridDetailsTab**&gt; **TabPageGrid** &gt; **MainGrid**.</span></span> <span data-ttu-id="628ae-183">次の図は、グリッド ノードを展開してフィールドを追加した後のグリッドを示しています。</span><span class="sxs-lookup"><span data-stu-id="628ae-183">The following illustration shows the grid after expanding the grid node and adding the fields.</span></span> 

        ![ノードを展開しフィールドを追加した後の、グリッドを表示するスクリーン ショット](./media/custform3.png)     

8.  <span data-ttu-id="628ae-185">**保存** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="628ae-185">Click **Save**.</span></span>
9.  <span data-ttu-id="628ae-186">**デザイン** &gt; **GridDetailsTab** &gt; **TabPageDetails** &gt; **TitleGroup** の順にクリックし、レコード ヘッダーを詳細ビューに追加します。</span><span class="sxs-lookup"><span data-stu-id="628ae-186">Click **Design** &gt; **GridDetailsTab** &gt; **TabPageDetails** &gt; **TitleGroup** to add the record header to the details view.</span></span>
10. <span data-ttu-id="628ae-187">**HeaderTitle** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="628ae-187">Click **HeaderTitle**.</span></span> <span data-ttu-id="628ae-188">**プロパティ** ウィンドウで、次の値を指定します。</span><span class="sxs-lookup"><span data-stu-id="628ae-188">In the **Properties** window, specify the following values.</span></span>

    | <span data-ttu-id="628ae-189">**プロパティ**</span><span class="sxs-lookup"><span data-stu-id="628ae-189">**Property**</span></span> | <span data-ttu-id="628ae-190">**値**</span><span class="sxs-lookup"><span data-stu-id="628ae-190">**Value**</span></span>   |
    |--------------|-------------|
    | <span data-ttu-id="628ae-191">データ ソース</span><span class="sxs-lookup"><span data-stu-id="628ae-191">Data Source</span></span>  | <span data-ttu-id="628ae-192">FmtCustomer</span><span class="sxs-lookup"><span data-stu-id="628ae-192">FmtCustomer</span></span> |
    | <span data-ttu-id="628ae-193">データ メソッド</span><span class="sxs-lookup"><span data-stu-id="628ae-193">Data Method</span></span>  | <span data-ttu-id="628ae-194">titleFields</span><span class="sxs-lookup"><span data-stu-id="628ae-194">titleFields</span></span> |

11. <span data-ttu-id="628ae-195">詳細ビューにコンテンツを追加するには、**デザイン** &gt; **GridDetailsTab** &gt; **TabPageDetails** &gt; **DetailsBodyTab** &gt; **一般** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="628ae-195">Click **Design** &gt; **GridDetailsTab** &gt; **TabPageDetails** &gt; **DetailsBodyTab** &gt; **General** to add content to the details view.</span></span>
    1.  <span data-ttu-id="628ae-196">**FmtCustomer** &gt; **データ ソース** &gt; **FmtCustomer** &gt; **フィールド** とクリックし、Ctrl キーを押したまま、次のフィールドを選択します。</span><span class="sxs-lookup"><span data-stu-id="628ae-196">Click **FmtCustomer** &gt; **Data sources** &gt; **FmtCustomer** &gt; **Fields**, press and hold the Ctrl key, and then select the following fields:</span></span>
        -   <span data-ttu-id="628ae-197">名</span><span class="sxs-lookup"><span data-stu-id="628ae-197">FirstName</span></span>
        -   <span data-ttu-id="628ae-198">姓</span><span class="sxs-lookup"><span data-stu-id="628ae-198">LastName</span></span>
        -   <span data-ttu-id="628ae-199">CellPhone</span><span class="sxs-lookup"><span data-stu-id="628ae-199">CellPhone</span></span>
        -   <span data-ttu-id="628ae-200">DriverLicense</span><span class="sxs-lookup"><span data-stu-id="628ae-200">DriverLicense</span></span>
        -   <span data-ttu-id="628ae-201">電子メール</span><span class="sxs-lookup"><span data-stu-id="628ae-201">Email</span></span>

    2.  <span data-ttu-id="628ae-202">協調表示されたフィールドを **一般** にドラッグし、**保存** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="628ae-202">Drag the highlighted fields onto **General**, and then click **Save**.</span></span>

## <a name="view-the-form"></a><span data-ttu-id="628ae-203">フォームの表示</span><span class="sxs-lookup"><span data-stu-id="628ae-203">View the form</span></span>
<span data-ttu-id="628ae-204">正しく読み込まれることを確認するためにフォームを実行します。</span><span class="sxs-lookup"><span data-stu-id="628ae-204">Run the form to verify that it loads correctly.</span></span>

1.  <span data-ttu-id="628ae-205">**ソリューション エクスプローラー** で、**FmtCustomer** を右クリックしてから、**スタートアップ オブジェクトとして設定** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="628ae-205">In **Solution Explorer**, right-click **FmtCustomer**, and then click **Set as Startup Object**.</span></span>
2.  <span data-ttu-id="628ae-206">**Ctrl+F5** キーを押します。</span><span class="sxs-lookup"><span data-stu-id="628ae-206">Press **Ctrl+F5**.</span></span> <span data-ttu-id="628ae-207">グリッド ビューは、次の図のように表示する必要があります。</span><span class="sxs-lookup"><span data-stu-id="628ae-207">The grid view should render like the following illustration.</span></span> 

    <span data-ttu-id="628ae-208">[![グリッド ビューの図](./media/custform4-1024x567.png)](./media/custform4.png)</span><span class="sxs-lookup"><span data-stu-id="628ae-208">[![Illustration of grid view](./media/custform4-1024x567.png)](./media/custform4.png)</span></span>

3.  <span data-ttu-id="628ae-209">アプリケーション バーで、**Microsoft Office を開く** &gt; **Excel にエクスポート &gt; 顧客** をクリックして、グリッド ビューの情報を Microsoft Excel スプレッドシートに送信します。</span><span class="sxs-lookup"><span data-stu-id="628ae-209">On the application bar, click **Open in Microsoft Office** &gt; **Export to Excel &gt; Customers** to send the information in the grid view to a Microsoft Excel spreadsheet.</span></span> <span data-ttu-id="628ae-210">(ページを終了するかどうかを確認するダイアログが表示されたら、「このページを終了」をクリックします。) 求められたら、**開く** をクリックして Excel でデータを表示します。</span><span class="sxs-lookup"><span data-stu-id="628ae-210">(If a dialog appears asking if you’re sure you want to leave the page, click “Leave this page”.) When asked, click **Open** to view the data in Excel.</span></span>
4.  <span data-ttu-id="628ae-211">Excel を閉じます。</span><span class="sxs-lookup"><span data-stu-id="628ae-211">Close Excel.</span></span>
5.  <span data-ttu-id="628ae-212">**Tony** をクリックしてそのレコードの詳細ビューに移動します。</span><span class="sxs-lookup"><span data-stu-id="628ae-212">Click **Tony** to navigate to the details view for that record.</span></span> 
6.  <span data-ttu-id="628ae-213">**閉じる** またはブラウザーの 戻る ボタンをクリックすると、グリッド ビューに戻ります。</span><span class="sxs-lookup"><span data-stu-id="628ae-213">Click **Close**  (or the browser Back button) to go back to the grid view.</span></span>

## <a name="apply-a-pattern-to-the-form"></a><span data-ttu-id="628ae-214">フォームにパターンを適用します</span><span class="sxs-lookup"><span data-stu-id="628ae-214">Apply a pattern to the form</span></span>
<span data-ttu-id="628ae-215">Visual Studio を使用して **顧客** フォームに Master Details のフォーム パターンを適用します。</span><span class="sxs-lookup"><span data-stu-id="628ae-215">Use Visual Studio to apply the Master Details form pattern to the **Customer** form.</span></span> <span data-ttu-id="628ae-216">フォーム パターンを適用すると、フォームに期待される構造が確実に適用されます。</span><span class="sxs-lookup"><span data-stu-id="628ae-216">Applying a form pattern ensures your form has the expected structure.</span></span> <span data-ttu-id="628ae-217">また、パターンの一部であるノードでプロパティの値を自動的に設定することでデザイン体験を簡素化します。</span><span class="sxs-lookup"><span data-stu-id="628ae-217">It also simplifies the design experience by automatically setting the values of properties in the nodes that are part of the pattern.</span></span>

1.  <span data-ttu-id="628ae-218">**デザイン** を右クリックして **パターンの適用** をポイントし、**詳細マスター** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="628ae-218">Right-click **Design**, point to **Apply pattern,** and then click **Details Master**.</span></span>

    <span data-ttu-id="628ae-219">[![詳細マスター フォーム パターンの適用](./media/custform6.png)](./media/custform6.png)</span><span class="sxs-lookup"><span data-stu-id="628ae-219">[![Apply Details Master form pattern](./media/custform6.png)](./media/custform6.png)</span></span>

    <span data-ttu-id="628ae-220">[![ナビゲーション リスト グループが表示されないスクリーン ショット](./media/custform7.png)](./media/custform7.png)</span><span class="sxs-lookup"><span data-stu-id="628ae-220">[![Screen shot showing missing Navigation List group](./media/custform7.png)](./media/custform7.png)</span></span>

2.  <span data-ttu-id="628ae-221">欠落しているナビゲーション リスト グループを追加します。</span><span class="sxs-lookup"><span data-stu-id="628ae-221">Add the missing Navigation List group.</span></span> <span data-ttu-id="628ae-222">パターン情報パネルが赤色でハイライトされると、このコントロールがないことを示します。</span><span class="sxs-lookup"><span data-stu-id="628ae-222">The red highlighting in the Patterns Information Panel indicates that this control is missing.</span></span>
    1.  <span data-ttu-id="628ae-223">**デザイン** を右クリックして **新規** をクリックし、**グループ** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="628ae-223">Right-click **Design**, point to **New**, and then click **Group**.</span></span>
    2.  <span data-ttu-id="628ae-224">**プロパティ** ウィンドウの **名前** プロパティに、**SidePanel** と入力します。</span><span class="sxs-lookup"><span data-stu-id="628ae-224">In the **Properties** window, in the **Name** property, enter **SidePanel**.</span></span>
    3.  <span data-ttu-id="628ae-225">**SidePanel** をクリックし、**Alt + ↑** を押してこのグループを **GridDetailsTab (タブ)** の上の移動します。</span><span class="sxs-lookup"><span data-stu-id="628ae-225">Click **SidePanel**, and press **Alt+Up** to move this group above the **GridDetailsTab (Tab)**.</span></span>

3.  <span data-ttu-id="628ae-226">**デザイン** を再度クリックします。</span><span class="sxs-lookup"><span data-stu-id="628ae-226">Click **Design** again.</span></span> <span data-ttu-id="628ae-227">**ナビゲーション リスト** と **パネル タブ** の周りの黄色のハイライトは、パターンが正常に適用される前にこれらの各ノードの下で解決する必要のある問題があることを示します。</span><span class="sxs-lookup"><span data-stu-id="628ae-227">The yellow highlighting around the **Navigation List** and the **Panel Tab** indicate that there are problems that need to be resolved under each of these nodes before the pattern can be successfully applied.</span></span>

    <span data-ttu-id="628ae-228">[![デザインを再度クリックする](./media/custform8.png)](./media/custform8.png)</span><span class="sxs-lookup"><span data-stu-id="628ae-228">[![Click Design again](./media/custform8.png)](./media/custform8.png)</span></span>

    <span data-ttu-id="628ae-229">[![黄色の強調表示を含むノードを示すスクリーン ショット](./media/custform9.png)](./media/custform9.png)</span><span class="sxs-lookup"><span data-stu-id="628ae-229">[![Screen shot showing nodes with yellow highlighting](./media/custform9.png)](./media/custform9.png)</span></span>

4.  <span data-ttu-id="628ae-230">パターン情報パネルで **SidePanel** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="628ae-230">In the Patterns Information Panel, click **SidePanel**.</span></span>

    <span data-ttu-id="628ae-231">[![情報パネルで選択した SidePanel](./media/custform10.png)](./media/custform10.png)</span><span class="sxs-lookup"><span data-stu-id="628ae-231">[![SidePanel selected in Information Panel](./media/custform10.png)](./media/custform10.png)</span></span>

    <span data-ttu-id="628ae-232">[![欠落しているコントロールを示す SidePanel](./media/custform11.png)](./media/custform11.png)</span><span class="sxs-lookup"><span data-stu-id="628ae-232">[![SidePanel showing missing controls](./media/custform11.png)](./media/custform11.png)</span></span>

5.  <span data-ttu-id="628ae-233">欠落しているコントロールを追加します。</span><span class="sxs-lookup"><span data-stu-id="628ae-233">Add the missing controls.</span></span>
    1.  <span data-ttu-id="628ae-234">**SidePanel** を右クリックして **新規** をクリックし、**QuickFilter** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="628ae-234">Right-click **SidePanel**, point to **New**, and then click **QuickFilter**.</span></span>
    2.  <span data-ttu-id="628ae-235">**プロパティ** ウィンドウで、次の値を指定します。</span><span class="sxs-lookup"><span data-stu-id="628ae-235">In the **Properties** window, specify the following values.</span></span>

        | <span data-ttu-id="628ae-236">**プロパティ**</span><span class="sxs-lookup"><span data-stu-id="628ae-236">**Property**</span></span> | <span data-ttu-id="628ae-237">**値**</span><span class="sxs-lookup"><span data-stu-id="628ae-237">**Value**</span></span>      |
        |--------------|----------------|
        | <span data-ttu-id="628ae-238">氏名</span><span class="sxs-lookup"><span data-stu-id="628ae-238">Name</span></span>           | <span data-ttu-id="628ae-239">SidePanelQuickFilter</span><span class="sxs-lookup"><span data-stu-id="628ae-239">SidePanelQuickFilter</span></span>                            |
        | <span data-ttu-id="628ae-240">ターゲット コントロール</span><span class="sxs-lookup"><span data-stu-id="628ae-240">Target Control</span></span> | <span data-ttu-id="628ae-241">MainGrid *この QuickFilter には、フォーム上の主要なグリッドと同じフィルター処理に使用できる列が必要です*</span><span class="sxs-lookup"><span data-stu-id="628ae-241">MainGrid *This QuickFilter should have the same columns available for filtering as the main grid on the form*</span></span> |

    3.  <span data-ttu-id="628ae-242">**SidePanel** を右クリックして **新規** をクリックし、**グリッド** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="628ae-242">Right-click **SidePanel**, point to **New**, and then click **Grid.**</span></span>

        | <span data-ttu-id="628ae-243">**プロパティ**</span><span class="sxs-lookup"><span data-stu-id="628ae-243">**Property**</span></span> | <span data-ttu-id="628ae-244">**値**</span><span class="sxs-lookup"><span data-stu-id="628ae-244">**Value**</span></span>      |
        |--------------|----------------|
        | <span data-ttu-id="628ae-245">氏名</span><span class="sxs-lookup"><span data-stu-id="628ae-245">Name</span></span>         | <span data-ttu-id="628ae-246">NavigationList</span><span class="sxs-lookup"><span data-stu-id="628ae-246">NavigationList</span></span> |
        | <span data-ttu-id="628ae-247">データソース</span><span class="sxs-lookup"><span data-stu-id="628ae-247">Datasource</span></span>   | <span data-ttu-id="628ae-248">FmtCustomer</span><span class="sxs-lookup"><span data-stu-id="628ae-248">FmtCustomer</span></span>    |

6.  <span data-ttu-id="628ae-249">ナビゲーション リストに識別するフィールドを追加します。</span><span class="sxs-lookup"><span data-stu-id="628ae-249">Add identifying fields to the Navigation list.</span></span> <span data-ttu-id="628ae-250">**NavigationList** を右クリックして **新規** をポイントし、**文字列** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="628ae-250">Right-click **NavigationList**, point to **New**, and then click **String**.</span></span>
    1.  <span data-ttu-id="628ae-251">**プロパティ** ウィンドウで、次の値を指定します。</span><span class="sxs-lookup"><span data-stu-id="628ae-251">In the **Properties** window, specify the following values.</span></span>

        | <span data-ttu-id="628ae-252">**プロパティ**</span><span class="sxs-lookup"><span data-stu-id="628ae-252">**Property**</span></span> | <span data-ttu-id="628ae-253">**値**</span><span class="sxs-lookup"><span data-stu-id="628ae-253">**Value**</span></span>             |
        |--------------|-----------------------|
        | <span data-ttu-id="628ae-254">DataSource</span><span class="sxs-lookup"><span data-stu-id="628ae-254">DataSource</span></span>   | <span data-ttu-id="628ae-255">FmtCustomer</span><span class="sxs-lookup"><span data-stu-id="628ae-255">FmtCustomer</span></span>           |
        | <span data-ttu-id="628ae-256">DataMethod</span><span class="sxs-lookup"><span data-stu-id="628ae-256">DataMethod</span></span>   | <span data-ttu-id="628ae-257">fullName</span><span class="sxs-lookup"><span data-stu-id="628ae-257">fullName</span></span>              |
        | <span data-ttu-id="628ae-258">氏名</span><span class="sxs-lookup"><span data-stu-id="628ae-258">Name</span></span>         | <span data-ttu-id="628ae-259">FmtCustomer\_FullName</span><span class="sxs-lookup"><span data-stu-id="628ae-259">FmtCustomer\_FullName</span></span> |

    2.  <span data-ttu-id="628ae-260">電話番号を簡易リストに追加するには、**データ ソース**&gt;**FmtCustomer**&gt;**フィールド** を展開します。</span><span class="sxs-lookup"><span data-stu-id="628ae-260">Expand **Data Sources** &gt; **FmtCustomer** &gt; **Fields** to add phone numbers to the Simple list.</span></span>
    3.  <span data-ttu-id="628ae-261">**CellPhone** フィールドを **Design &gt; SidePanel &gt; NavigationList** の下のグリッドにドラッグします。</span><span class="sxs-lookup"><span data-stu-id="628ae-261">Drag the **CellPhone** field onto the grid under **Design &gt; SidePanel &gt; NavigationList**.</span></span>

7.  <span data-ttu-id="628ae-262">**SidePanel** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="628ae-262">Click **SidePanel**.</span></span> <span data-ttu-id="628ae-263">**パターン情報パネル** は、このサブツリーのコントロールがパターンに完全に準拠していることを示しています。</span><span class="sxs-lookup"><span data-stu-id="628ae-263">Notice the **Patterns Information Panel** is now indicating that the controls in this subtree are in full compliance with the pattern.</span></span>

    ![パターン情報パネル](./media/custform12.png)

    ![パターン情報パネル](./media/custform13.png)

8.  <span data-ttu-id="628ae-266">**デザイン** &gt; **GridDetailsTab** とクリックします。</span><span class="sxs-lookup"><span data-stu-id="628ae-266">Click **Design** &gt; **GridDetailsTab**.</span></span> <span data-ttu-id="628ae-267">サブノードの周りの黄色のハイライトは、フォーム パターンが正常に適用される前に両方のノードの下で解決する必要のある問題があることを示します。</span><span class="sxs-lookup"><span data-stu-id="628ae-267">The yellow highlighting around the subnodes indicates that there are problems that need to be resolved under both nodes before the form pattern can be successfully applied.</span></span>

    <span data-ttu-id="628ae-268">[![GridDetailsTab](./media/custform14.png)](./media/custform14.png)</span><span class="sxs-lookup"><span data-stu-id="628ae-268">[![GridDetailsTab](./media/custform14.png)](./media/custform14.png)</span></span>

    <span data-ttu-id="628ae-269">[![サブノードの周囲の黄色い強調表示](./media/custform15.png)](./media/custform15.png)</span><span class="sxs-lookup"><span data-stu-id="628ae-269">[![Yellow highlighting around subnodes](./media/custform15.png)](./media/custform15.png)</span></span>

9.  <span data-ttu-id="628ae-270">パターンは **グリッド パネル** が **詳細パネル** の後に配置されることを期待します。</span><span class="sxs-lookup"><span data-stu-id="628ae-270">Notice that the pattern expects the **Grid Panel** to be after the **Details Panel.**</span></span> <span data-ttu-id="628ae-271">**TabPageGrid** をクリックし、**Alt + ↓** キーを押してそのタブを **詳細パネル** の下に移動します。</span><span class="sxs-lookup"><span data-stu-id="628ae-271">Click **TabPageGrid** and press **Alt+Down** to move that tab below the **Details Panel**.</span></span>
10. <span data-ttu-id="628ae-272">**GridDetailsTab** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="628ae-272">Click **GridDetailsTab**.</span></span> <span data-ttu-id="628ae-273">**TabPageDetails** タブ ページはパターンに準拠するようになりました。</span><span class="sxs-lookup"><span data-stu-id="628ae-273">The **TabPageDetails** tab page now adheres to the pattern.</span></span> <span data-ttu-id="628ae-274">ただし、**TabPageGrid** タブ ページには更なる注意が必要です。</span><span class="sxs-lookup"><span data-stu-id="628ae-274">However, the **TabPageGrid** tab page needs additional attention.</span></span>

    <span data-ttu-id="628ae-275">[![GridDetailsTab](./media/custform16.png)](./media/custform16.png)</span><span class="sxs-lookup"><span data-stu-id="628ae-275">[![GridDetailsTab](./media/custform16.png)](./media/custform16.png)</span></span>

    <span data-ttu-id="628ae-276">[![TabPageGrid タブ ページには更なる注意が必要](./media/custform17.png)](./media/custform17.png)</span><span class="sxs-lookup"><span data-stu-id="628ae-276">[![TabPageGrid tab page needs additonal attention](./media/custform17.png)](./media/custform17.png)</span></span>

11. <span data-ttu-id="628ae-277">**TabPageGrid** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="628ae-277">Click **TabPageGrid**.</span></span> <span data-ttu-id="628ae-278">デザイナーでフォーカスがすぐに **TabPageGrid** がオンになり、**パターン情報パネル** が更新されています。</span><span class="sxs-lookup"><span data-stu-id="628ae-278">Focus in the designer is now on **TabPageGrid**, and the **Patterns Information Panel** has been updated.</span></span>

    <span data-ttu-id="628ae-279">[![TabPageGrid のフォーカス](./media/custform18.png)](./media/custform18.png)</span><span class="sxs-lookup"><span data-stu-id="628ae-279">[![Focus on TabPageGrid](./media/custform18.png)](./media/custform18.png)</span></span>

    <span data-ttu-id="628ae-280">[![パターン情報パネル](./media/custform19.png)](./media/custform19.png)</span><span class="sxs-lookup"><span data-stu-id="628ae-280">[![Patterns Information Panel](./media/custform19.png)](./media/custform19.png)</span></span>

12. <span data-ttu-id="628ae-281">**パターン情報パネル** には、**TabPageGrid** コンテナーの上部で欠落しているグループ コントロールが表示されるようになりました。</span><span class="sxs-lookup"><span data-stu-id="628ae-281">The **Patterns Information Panel** now indicates a missing Group control at the top of the **TabPageGrid** container.</span></span>
    1.  <span data-ttu-id="628ae-282">**TabPageGrid** を右クリックして **新規** をポイントし、**グループ** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="628ae-282">Right-click **TabPageGrid**, point to **New**, and then click **Group**.</span></span>
    2.  <span data-ttu-id="628ae-283">**Alt+上方向** キーを 2 回押して、そのグループをグループの最初のコントロールとして配置します。</span><span class="sxs-lookup"><span data-stu-id="628ae-283">Press **Alt+Up** two times to position the group as the first control in the group.</span></span>
    3.  <span data-ttu-id="628ae-284">**プロパティ** ウィンドウの **名前** プロパティに、**GridCustomFilterGroup** と入力します。</span><span class="sxs-lookup"><span data-stu-id="628ae-284">In the **Properties** window, in the **Name** property, enter **GridCustomFilterGroup**.</span></span> <span data-ttu-id="628ae-285">[![GridCustomFilterGroup の入力](./media/custform20.png)](./media/custform20.png)</span><span class="sxs-lookup"><span data-stu-id="628ae-285">[![Enter GridCustomFilterGroup](./media/custform20.png)](./media/custform20.png)</span></span>

13. <span data-ttu-id="628ae-286">パターンが、**GridCustomFilterGroup** に適用されるサブパターンをお探しています。</span><span class="sxs-lookup"><span data-stu-id="628ae-286">The pattern is looking for a subpattern to be applied to **GridCustomFilterGroup**.</span></span> <span data-ttu-id="628ae-287">**GridCustomFilterGroup** を右クリックして **パターンの適用** をポイントし、**カスタムおよびクイック フィルター** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="628ae-287">Right-click **GridCustomFilterGroup,** point to **Apply pattern**, and then click **Custom and Quick Filters**.</span></span>

    <span data-ttu-id="628ae-288">[![カスタムおよびクイック フィルターをクリックする](./media/custform21.png)](./media/custform21.png)</span><span class="sxs-lookup"><span data-stu-id="628ae-288">[![Click Custom and Quick Filters](./media/custform21.png)](./media/custform21.png)</span></span>

    <span data-ttu-id="628ae-289">[![カスタムおよびクイック フィルター](./media/custform22.png)](./media/custform22.png)</span><span class="sxs-lookup"><span data-stu-id="628ae-289">[![Custom and Quick Filters](./media/custform22.png)](./media/custform22.png)</span></span>

14. <span data-ttu-id="628ae-290">**カスタムおよびクイック フィルター** サブパターンには、QuickFilter コントロールが必須です。</span><span class="sxs-lookup"><span data-stu-id="628ae-290">The **Custom and Quick Filters** subpattern requires a QuickFilter control.</span></span>
    1.  <span data-ttu-id="628ae-291">**GridCustomFilterGroup** を右クリックして **新規** をクリックし、**QuickFilter** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="628ae-291">Right-click **GridCustomFilterGroup**, point to **New**, and then click **QuickFilter**.</span></span>
    2.  <span data-ttu-id="628ae-292">**プロパティ** ウィンドウで、次の値を指定します。</span><span class="sxs-lookup"><span data-stu-id="628ae-292">In the **Properties** window, specify the following values.</span></span>

        | <span data-ttu-id="628ae-293">**プロパティ**</span><span class="sxs-lookup"><span data-stu-id="628ae-293">**Property**</span></span>   | <span data-ttu-id="628ae-294">**値**</span><span class="sxs-lookup"><span data-stu-id="628ae-294">**Value**</span></span>           |
        |----------------|---------------------|
        | <span data-ttu-id="628ae-295">氏名</span><span class="sxs-lookup"><span data-stu-id="628ae-295">Name</span></span>           | <span data-ttu-id="628ae-296">MainGridQuickFilter</span><span class="sxs-lookup"><span data-stu-id="628ae-296">MainGridQuickFilter</span></span> |
        | <span data-ttu-id="628ae-297">ターゲット コントロール</span><span class="sxs-lookup"><span data-stu-id="628ae-297">Target Control</span></span> | <span data-ttu-id="628ae-298">MainGrid</span><span class="sxs-lookup"><span data-stu-id="628ae-298">MainGrid</span></span>            |

15. <span data-ttu-id="628ae-299">コントロール ツリーを参照して設計し、各コントロールで **パターン情報パネル** に問題が表示されなくなった方法に注意てください。</span><span class="sxs-lookup"><span data-stu-id="628ae-299">Browse up the control tree to design and notice how the **Patterns Information Panel** now shows no issues under each of the controls.</span></span>
16. <span data-ttu-id="628ae-300">**Ctrl+S** キーを押してフォームを保存します。</span><span class="sxs-lookup"><span data-stu-id="628ae-300">Press **Ctrl+S** to save the form.</span></span>

## <a name="view-the-details-form"></a><span data-ttu-id="628ae-301">詳細フォームの表示</span><span class="sxs-lookup"><span data-stu-id="628ae-301">View the details form</span></span>
<span data-ttu-id="628ae-302">詳細ビューとグリッド ビューに表示するフォームを実行します。</span><span class="sxs-lookup"><span data-stu-id="628ae-302">Run the form to see the Details view and the Grid view.</span></span>

1.  <span data-ttu-id="628ae-303">**Ctrl+F5** キーを押してプロジェクトを実行します。</span><span class="sxs-lookup"><span data-stu-id="628ae-303">Press **Ctrl+F5** to run the project.</span></span> <span data-ttu-id="628ae-304">次の図は、グリッド ビューの表示方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="628ae-304">The following illustration shows how the grid view appears.</span></span>

    <span data-ttu-id="628ae-305">[![グリッド ビューの図](./media/custform23-1024x599.png)](./media/custform23.png)</span><span class="sxs-lookup"><span data-stu-id="628ae-305">[![Illustration of grid view](./media/custform23-1024x599.png)](./media/custform23.png)</span></span>

2.  <span data-ttu-id="628ae-306">**Phil** をクリックしてそのレコードの詳細ビューに移動します。</span><span class="sxs-lookup"><span data-stu-id="628ae-306">Click **Phil** to go to the details view for that record.</span></span> 

3.  <span data-ttu-id="628ae-307">ナビゲーション リストを開くには、フォームの左側にある **リストを表示** ボタンをクリックします。</span><span class="sxs-lookup"><span data-stu-id="628ae-307">Click the **Show list** button on the left side of the form to open the navigation list.</span></span> 

    <span data-ttu-id="628ae-308">[![ナビゲーション リストを表示するために開かれたフォーム](./media/custform25-1024x597.png)](./media/custform25.png)</span><span class="sxs-lookup"><span data-stu-id="628ae-308">[![Form opened to show navigation list](./media/custform25-1024x597.png)](./media/custform25.png)</span></span>

4.  <span data-ttu-id="628ae-309">グリッド表示に戻るには、**閉じる** (またはブラウザーの [戻る] ボタン) をクリックします。</span><span class="sxs-lookup"><span data-stu-id="628ae-309">To go back to the grid view, click **Close** (or the browser Back button).</span></span>
5.  <span data-ttu-id="628ae-310">Visual Studio に戻ります。</span><span class="sxs-lookup"><span data-stu-id="628ae-310">Return to Visual Studio.</span></span>

## <a name="add-subpatterns"></a><span data-ttu-id="628ae-311">サブパターンの追加</span><span class="sxs-lookup"><span data-stu-id="628ae-311">Add subpatterns</span></span>
1.  <span data-ttu-id="628ae-312">Visual Studio の、フォーム デザイナーで、**FmtCustomer** を右クリックして **アドイン** をポイントしてから、**フォーム統計情報** を選択します。</span><span class="sxs-lookup"><span data-stu-id="628ae-312">In Visual Studio, in the Form designer, right-click **FmtCustomer**, point to **Addins**, and then select **Form statistics**.</span></span> 

    <span data-ttu-id="628ae-313">[![フォーム デザイナーで選択されたフォームの統計情報](./media/custform26.png)](./media/custform26.png)</span><span class="sxs-lookup"><span data-stu-id="628ae-313">[![Form statistics selected in Form designer](./media/custform26.png)](./media/custform26.png)</span></span> 

    <span data-ttu-id="628ae-314">**フォーム統計** アドインは、フォームの状態に関するいくつかの役に立つデータ ポイントを提供します。</span><span class="sxs-lookup"><span data-stu-id="628ae-314">The **Form Statistics** add-in provides several useful data points about the state of the form.</span></span> <span data-ttu-id="628ae-315">これには、次のものが含まれます。</span><span class="sxs-lookup"><span data-stu-id="628ae-315">This includes:</span></span>
    -   <span data-ttu-id="628ae-316">**パターン = 未指定のカウント** – フォーム パターンまたはサブパターンが適用されていないノードの数。</span><span class="sxs-lookup"><span data-stu-id="628ae-316">**Pattern=Unspecified count** – The number of nodes for which no form pattern or subpattern has been applied.</span></span>
    -   <span data-ttu-id="628ae-317">**パターン = カスタム カウント** – カスタム パターンが適用されたノードの数。構造が既存のパターンに適合しなかったことを意味します。</span><span class="sxs-lookup"><span data-stu-id="628ae-317">**Pattern=Custom count** – The number of nodes for which a custom pattern was applied, meaning the structure did not fit with any existing pattern.</span></span>
    -   <span data-ttu-id="628ae-318">**パターン カバレッジ** – フォーム上のコントロールのうち、フォーム パターンまたはサブパターンの対象となるものの割合。</span><span class="sxs-lookup"><span data-stu-id="628ae-318">**Pattern coverage** – The percentage of controls on the form that are covered by the form pattern or a subpattern.</span></span> <span data-ttu-id="628ae-319">100% の値は、完全に対象となるフォームを示します。</span><span class="sxs-lookup"><span data-stu-id="628ae-319">A value of 100% indicates a fully covered form.</span></span> 

        <span data-ttu-id="628ae-320">[![フォームに関するデータを示すダイアログ ボックス](./media/custform27.png)](./media/custform27.png)</span><span class="sxs-lookup"><span data-stu-id="628ae-320">[![Dialog box showing data about the form](./media/custform27.png)](./media/custform27.png)</span></span>

2.  <span data-ttu-id="628ae-321">このフォームのパターン カバレッジを完成させるには、Pattern = Unspecified カウントをゼロにする必要があります。</span><span class="sxs-lookup"><span data-stu-id="628ae-321">To complete pattern coverage for this form, the Pattern=Unspecified count should be zero.</span></span> <span data-ttu-id="628ae-322">Visual Studio のフォーム検索を使用して、フォーム内の「指定されていない」すべてのインスタンスを検索します。</span><span class="sxs-lookup"><span data-stu-id="628ae-322">Use the Visual Studio form search to find all instances of “unspecified “in the form.</span></span> 

    <span data-ttu-id="628ae-323">[![検索からの Visual Studio の例](./media/custform28.png)](./media/custform28.png)</span><span class="sxs-lookup"><span data-stu-id="628ae-323">[![Example of Visual Studio from search](./media/custform28.png)](./media/custform28.png)</span></span>

3.  <span data-ttu-id="628ae-324">**一般** タブ ページには入力コントロールのみが含まれており、このクイックタブにはカスタム レイアウトが不要なため、応答レイアウトを保証するためにフィールドおよびフィールド グループのパターンを適用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="628ae-324">Because the **General** tab page contains only input controls and no custom layout is required for this FastTab, the Fields and Field Groups pattern should be applied to guarantee a responsive layout.</span></span> <span data-ttu-id="628ae-325">**全般** を右クリックして **パターンの適用** をポイントし、**フィールドおよびフィールド グループ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="628ae-325">Right-click **General**, point to **Apply pattern**, and then select **Fields and Field Groups**.</span></span>
4.  <span data-ttu-id="628ae-326">画面の右端で、**検索のクリア** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="628ae-326">On the far right of the screen, click **Clear search**.</span></span> 

    <span data-ttu-id="628ae-327">[![画面の右端にある検索のクリア オプションを示すスクリーン ショット](./media/custform29.png)](./media/custform29.png)</span><span class="sxs-lookup"><span data-stu-id="628ae-327">[![Screen shot showing Clear search option on the far right of screen](./media/custform29.png)](./media/custform29.png)</span></span>

5.  <span data-ttu-id="628ae-328">**Ctrl+S** キーを押してフォームを保存します。</span><span class="sxs-lookup"><span data-stu-id="628ae-328">Press **Ctrl+S** to save the form.</span></span>
6.  <span data-ttu-id="628ae-329">手順 1 を繰り返して **フォーム統計** アドインを再度実行し、フォームがパターンによって完全にカバーされていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="628ae-329">Repeat step 1 to run the **Form Statistics** add-in a second time to verify the form is fully covered by patterns.</span></span> 

    <span data-ttu-id="628ae-330">[![100% パターン カバレッジを示すダイアログ ボックス](./media/custform30.png)](./media/custform30.png)</span><span class="sxs-lookup"><span data-stu-id="628ae-330">[![Dialog box showing 100% pattern coverage](./media/custform30.png)](./media/custform30.png)</span></span>

7.  <span data-ttu-id="628ae-331">**Ctrl+F5** キーを押してプロジェクトを実行し、更新されたフォームを表示します。</span><span class="sxs-lookup"><span data-stu-id="628ae-331">Press **Ctrl+F5** to run the project and see the updated form.</span></span>
8.  <span data-ttu-id="628ae-332">**里美 (サンプル)** をクリックし、詳細ビューに移動します。</span><span class="sxs-lookup"><span data-stu-id="628ae-332">Click **Adrian** to go to the details view.</span></span> <span data-ttu-id="628ae-333">次の図は、フィールドおよびフィールド グループのサブパターンを適用し、フィールドが反応しやすいようにレイアウトした後に詳細ビューがどのように表示されるかを示しています。</span><span class="sxs-lookup"><span data-stu-id="628ae-333">The following illustration shows how the details view now appears after applying the Fields and Field Groups subpattern so that the fields lay out responsively.</span></span> <span data-ttu-id="628ae-334">ブラウザーの幅を変更することで、ブラウザーの幅を十分に埋めるためにフィールド レイアウトがどのように調整されるのかが分かります。</span><span class="sxs-lookup"><span data-stu-id="628ae-334">By changing the browser width, you’ll see how the field layout adjusts to better fill the width of the browser.</span></span> 

    <span data-ttu-id="628ae-335">[![フィールドおよびフィールド グループのサブパターンを適用した後の詳細ビュー](./media/custform31-1024x674.png)](./media/custform31.png)</span><span class="sxs-lookup"><span data-stu-id="628ae-335">[![Details view after applying Fields and Field Groups subpattern](./media/custform31-1024x674.png)](./media/custform31.png)</span></span>

9.  <span data-ttu-id="628ae-336">Visual Studio に戻る</span><span class="sxs-lookup"><span data-stu-id="628ae-336">Return to Visual Studio</span></span>

## <a name="determine-the-amount-of-remaining-patterns-work-in-a-model"></a><span data-ttu-id="628ae-337">モデル内で残っているパターンの作業の量を決定する</span><span class="sxs-lookup"><span data-stu-id="628ae-337">Determine the amount of remaining patterns work in a model</span></span>
1.  <span data-ttu-id="628ae-338">**Finance and Operations** をクリックし、**アドイン** をポイントし、**フォーム パターン レポートを実行** を選択します。</span><span class="sxs-lookup"><span data-stu-id="628ae-338">Click **Finance and Operations**, point to **Addins**, and then select **Run form patterns report**.</span></span> 

    <span data-ttu-id="628ae-339">フォームのパターン レポートが生成されたときに表示される通知ダイアログです。</span><span class="sxs-lookup"><span data-stu-id="628ae-339">A notification dialog will be shown when the form patterns report has been generated.</span></span> 

    <span data-ttu-id="628ae-340">[![レポートが生成されたことを示すダイアログ ボックス](./media/custform33.png)](./media/custform33.png)</span><span class="sxs-lookup"><span data-stu-id="628ae-340">[![Dialog box that says the report has been generated](./media/custform33.png)](./media/custform33.png)</span></span>

2.  <span data-ttu-id="628ae-341">PatternsReport ファイルを Excel で開きます。</span><span class="sxs-lookup"><span data-stu-id="628ae-341">Open the PatternsReport file in Excel.</span></span>
3.  <span data-ttu-id="628ae-342">フリート管理チュートリアル モデルへのレポートをフィルター処理します。</span><span class="sxs-lookup"><span data-stu-id="628ae-342">Filter the report to the Fleet Management Tutorial model.</span></span>
    1.  <span data-ttu-id="628ae-343">**データ** &gt; **フィルター** の順にクリックします。</span><span class="sxs-lookup"><span data-stu-id="628ae-343">Click **Data** &gt; **Filter**.</span></span>
    2.  <span data-ttu-id="628ae-344">FleetMgmntTutorial への **モデル** 列をフィルター処理します。</span><span class="sxs-lookup"><span data-stu-id="628ae-344">Filter the **Model** column to FleetMgmntTutorial.</span></span> 

        <span data-ttu-id="628ae-345">[![フィルター処理されたレポートのスクリーン ショット](./media/custform34-1024x422.png)](./media/custform34.png)</span><span class="sxs-lookup"><span data-stu-id="628ae-345">[![Screen shot of filtered report](./media/custform34-1024x422.png)](./media/custform34.png)</span></span>


<span data-ttu-id="628ae-346">レポートには、現在適用されている最上位のフォーム パターンと、パターンでカバーされているフォーム上のコントロールの割合など、このモデルのフォームに関するパターン関連の情報が表示されます。</span><span class="sxs-lookup"><span data-stu-id="628ae-346">The report shows pattern-related information regarding the forms in this model including the top-level form pattern currently applied, and the percentage of controls on the form covered by patterns.</span></span> <span data-ttu-id="628ae-347">これは、1 つまたは複数のモデルの残りのパターンの作業を追跡するために使用できます。</span><span class="sxs-lookup"><span data-stu-id="628ae-347">This can be used to track the remaining patterns work in one or more models.</span></span>  



