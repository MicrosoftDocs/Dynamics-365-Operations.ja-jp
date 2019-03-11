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
ms.reviewer: robinr
ms.search.scope: Operations
ms.custom: 20401
ms.assetid: 78199ae8-0631-4cf4-b206-b952f09b92a9
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a0b71da3ba67604138cdef3ab2dc3abcf96a7647
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/29/2019
ms.locfileid: "368813"
---
# <a name="build-the-customer-form"></a><span data-ttu-id="bfac7-105">顧客フォームの構築</span><span class="sxs-lookup"><span data-stu-id="bfac7-105">Build the Customer form</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="bfac7-106">このラボでは、マスター詳細フォームを作成し、適切なフォームのパターンおよびサブパターンを適用します。</span><span class="sxs-lookup"><span data-stu-id="bfac7-106">In this lab you’ll create a Master Details form and apply the appropriate form pattern and subpatterns.</span></span> <span data-ttu-id="bfac7-107">マスター詳細フォームには、多数のフィールドが含まれるプライマリ データが表示されます。</span><span class="sxs-lookup"><span data-stu-id="bfac7-107">A Master Details form shows primary data that has many fields.</span></span> <span data-ttu-id="bfac7-108">たとえば、作成するフォームは、顧客情報を表示します。</span><span class="sxs-lookup"><span data-stu-id="bfac7-108">For example, the form that you create will show customer information.</span></span>

<a name="prerequisites"></a><span data-ttu-id="bfac7-109">前提条件</span><span class="sxs-lookup"><span data-stu-id="bfac7-109">Prerequisites</span></span>
-------------

<span data-ttu-id="bfac7-110">このチュートリアルでは、リモート デスクトップを使用して環境にアクセスし、インスタンスの管理者としてプロビジョニングされる必要があります。</span><span class="sxs-lookup"><span data-stu-id="bfac7-110">For this tutorial, you will need to access the environment using Remote Desktop, and be provisioned as an administrator on the instance.</span></span> <span data-ttu-id="bfac7-111">詳細については、「[アクセス インスタンス](../dev-tools/access-instances.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="bfac7-111">For more information, see [Access Instances](../dev-tools/access-instances.md).</span></span>

## <a name="overview"></a><span data-ttu-id="bfac7-112">概要</span><span class="sxs-lookup"><span data-stu-id="bfac7-112">Overview</span></span>
<span data-ttu-id="bfac7-113">フォームを作成するには、既存のフォーム **FmtCustomer** から開始します。</span><span class="sxs-lookup"><span data-stu-id="bfac7-113">To create the form, you’ll start from the existing form, **FmtCustomer**.</span></span> <span data-ttu-id="bfac7-114">フォームは、古いマスター詳細テンプレートをテーブルします。</span><span class="sxs-lookup"><span data-stu-id="bfac7-114">The form represents the old Master Details template.</span></span> <span data-ttu-id="bfac7-115">チュートリアルの一環として、このフォーム タイプに一貫した構造を実行するマスターの詳細パターンを適用します。</span><span class="sxs-lookup"><span data-stu-id="bfac7-115">As a part of the tutorial, you’ll apply the Master Details pattern, which will enforce a consistent structure for this form type.</span></span> <span data-ttu-id="bfac7-116">次の図は、**FmtCustomer** 開始コンポーネントを示しています。</span><span class="sxs-lookup"><span data-stu-id="bfac7-116">The following illustration shows the **FmtCustomer** starting artifact.</span></span> 

<span data-ttu-id="bfac7-117">[![CustForm1](./media/custform1.png)](./media/custform1.png)</span><span class="sxs-lookup"><span data-stu-id="bfac7-117">[![CustForm1](./media/custform1.png)](./media/custform1.png)</span></span>

## <a name="key-concepts"></a><span data-ttu-id="bfac7-118">重要な概念</span><span class="sxs-lookup"><span data-stu-id="bfac7-118">Key concepts</span></span>
-   <span data-ttu-id="bfac7-119">マスター詳細フォームを作成します。</span><span class="sxs-lookup"><span data-stu-id="bfac7-119">Create a Master Details form.</span></span>
-   <span data-ttu-id="bfac7-120">フォームにフォーム パターンを適用します。</span><span class="sxs-lookup"><span data-stu-id="bfac7-120">Apply a form pattern to a form.</span></span>
-   <span data-ttu-id="bfac7-121">Visual Studio のパターン アドインを使用して、フォーム/モデル パターンのカバレッジに関する情報を取得します。</span><span class="sxs-lookup"><span data-stu-id="bfac7-121">Use the Visual Studio pattern add-ins to get information about form/model pattern coverage.</span></span>
-   <span data-ttu-id="bfac7-122">フォーム コントロールにサブパターンを適用します。</span><span class="sxs-lookup"><span data-stu-id="bfac7-122">Apply subpatterns to form controls.</span></span>
-   <span data-ttu-id="bfac7-123">Visual Studio とブラウザーを使用してフォームを表示します。</span><span class="sxs-lookup"><span data-stu-id="bfac7-123">View the form using Visual Studio and a browser.</span></span>
-   <span data-ttu-id="bfac7-124">モデル内で残っているパターンの作業の量を決定します。</span><span class="sxs-lookup"><span data-stu-id="bfac7-124">Determine the amount of remaining patterns work in a model.</span></span>

## <a name="setup"></a><span data-ttu-id="bfac7-125">セットアップ</span><span class="sxs-lookup"><span data-stu-id="bfac7-125">Setup</span></span>
### <a name="import-the-tutorial-project-and-transactional-data"></a><span data-ttu-id="bfac7-126">チュートリアル プロジェクトおよびトランザクション データのインポート</span><span class="sxs-lookup"><span data-stu-id="bfac7-126">Import the tutorial project and transactional data</span></span>

<span data-ttu-id="bfac7-127">Visual Studio を使用してチュートリアル プロジェクトをインポートします。</span><span class="sxs-lookup"><span data-stu-id="bfac7-127">Use Visual Studio to import the tutorial project.</span></span> <span data-ttu-id="bfac7-128">チュートリアル プロジェクトには、このチュートリアルを完了するために使用する成果物が含まれています。</span><span class="sxs-lookup"><span data-stu-id="bfac7-128">The tutorial project includes the artifacts you will use to complete this tutorial.</span></span> <span data-ttu-id="bfac7-129">Visual Studio を使用して FMTutorial プロジェクトを開き、チュートリアル用のデータを読み込みます。</span><span class="sxs-lookup"><span data-stu-id="bfac7-129">Use Visual Studio to open the FMTutorial project and load the data for the tutorial.</span></span> <span data-ttu-id="bfac7-130">フリート管理チュートリアルのデータを読み込むために、FMTDataHelper クラスを使用します。</span><span class="sxs-lookup"><span data-stu-id="bfac7-130">You will use the FMTDataHelper class to load data for the Fleet Management tutorial.</span></span> <span data-ttu-id="bfac7-131">これが作業する最初のチュートリアルである場合は、[アクセス インスタンス](../dev-tools/access-instances.md)を確認し、ローカル VM で作業している場合に、管理者ユーザーを提供するかどうかを確認します。</span><span class="sxs-lookup"><span data-stu-id="bfac7-131">If this is the first tutorial you are working on, review [Access Instances](../dev-tools/access-instances.md) and make sure you provision your administrator user if you’re working on a local VM.</span></span>

1.  <span data-ttu-id="bfac7-132">フリート管理のサンプルを <https://github.com/Microsoft/FMLab> からダウンロードし、**C:\\** に保存してから解凍します。</span><span class="sxs-lookup"><span data-stu-id="bfac7-132">Download the Fleet Management sample from <https://github.com/Microsoft/FMLab>, save it to **C:\\**, and unzip it.</span></span>
2.  <span data-ttu-id="bfac7-133">デスクトップで、Visual Studio ショートカットをダブルクリックして、開発環境を開きます。</span><span class="sxs-lookup"><span data-stu-id="bfac7-133">On the desktop, double-click the Visual Studio shortcut to open the development environment.</span></span>
3.  <span data-ttu-id="bfac7-134">**Finance and Operations** メニューで、**プロジェクトのインポート**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="bfac7-134">On the **Finance and Operations** menu, click **Import Project**.</span></span>
4.  <span data-ttu-id="bfac7-135">**プロジェクトのインポート** ウィンドウで、**ファイル名**テキスト ボックスの隣にある、省略記号ボタンをクリックします。</span><span class="sxs-lookup"><span data-stu-id="bfac7-135">In the **Import Project** window, next to the **Filename** text box, click the ellipsis button.</span></span>
5.  <span data-ttu-id="bfac7-136">**インポートするファイルの選択**ウィンドウで、**C:\FMLab** を参照して FMTutorialDataModel.axpp をクリックしてから**開く**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="bfac7-136">In the **Select the file to import** window, browse to **C:\FMLab**, click FMTutorialDataModel.axpp, and then click **Open**.</span></span>
6.  <span data-ttu-id="bfac7-137">**プロジェクト ファイルの場所**テキスト ボックスに、**C:\FMLab** と入力します。</span><span class="sxs-lookup"><span data-stu-id="bfac7-137">In the **Project file location** text box, enter **C:\FMLab**.</span></span>
7.  <span data-ttu-id="bfac7-138">**要素の上書き** オプションをオンにし、**現在のソリューション** ラジオ オプションをオンにします。</span><span class="sxs-lookup"><span data-stu-id="bfac7-138">Select the **Overwrite Elements** option and the **Current solution** radio button.</span></span> <span data-ttu-id="bfac7-139">次の図は、完了した **インポート プロジェクト** ダイアログ ボックスを示しています。</span><span class="sxs-lookup"><span data-stu-id="bfac7-139">The following illustration shows the completed **Import Project** dialog box.</span></span> 

    ![CustForm2](./media/custform2.png)

8.  <span data-ttu-id="bfac7-141">**OK** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="bfac7-141">Click **OK**.</span></span>
9.  <span data-ttu-id="bfac7-142">**ソリューション エクスプローラー**で、**クラス**を展開して、**FMTutorial** プロジェクトで **FMTDataHelper** を右クリックしてから、**スタートアップ オブジェクトとして設定**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="bfac7-142">In **Solution Explorer**, expand **Classes**, and under the **FMTutorial** project, right-click **FMTDataHelper**, and then click **Set as Startup Object**.</span></span>
10. <span data-ttu-id="bfac7-143">**ビルド**メニューで、**ソリューションの再構築**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="bfac7-143">On the **Build** menu, click **Rebuild Solution**.</span></span> <span data-ttu-id="bfac7-144">タイムスタンプに関係なく、プロジェクトのすべてのファイルを確実に作成するには、リビルドを使用します。</span><span class="sxs-lookup"><span data-stu-id="bfac7-144">You use the rebuild to make sure all files in the project are built regardless of timestamps.</span></span> <span data-ttu-id="bfac7-145">出力ウィンドウでビルドの進行状況を表示できます。</span><span class="sxs-lookup"><span data-stu-id="bfac7-145">You can view the build progress in the Output window.</span></span>
11. <span data-ttu-id="bfac7-146">ビルドが完了すると、**Ctrl + F5** を押してプロジェクトを実行します。</span><span class="sxs-lookup"><span data-stu-id="bfac7-146">After the build completes, press **Ctrl+F5** to run the project.</span></span> <span data-ttu-id="bfac7-147">ブラウザーが開き、データをインポートするクラスが実行されます。</span><span class="sxs-lookup"><span data-stu-id="bfac7-147">The browser will open and run the class that imports the data.</span></span>

## <a name="open-the-fmtutorial-project"></a><span data-ttu-id="bfac7-148">FMTutorial プロジェクトを開く</span><span class="sxs-lookup"><span data-stu-id="bfac7-148">Open the FMTutorial project</span></span>
<span data-ttu-id="bfac7-149">Visual Studio を使用して FMTutorial プロジェクトを開きます。</span><span class="sxs-lookup"><span data-stu-id="bfac7-149">Use Visual Studio to open the FMTutorial project.</span></span> <span data-ttu-id="bfac7-150">Visual Studio を開き、FMTutorial プロジェクトが既に読み込まれている場合は、次のセクションに続行することができます。</span><span class="sxs-lookup"><span data-stu-id="bfac7-150">If you have Visual Studio open and have already loaded the FMTutorial project, you can continue to the next section.</span></span>

1.  <span data-ttu-id="bfac7-151">開発環境がまだ開いていない場合は、デスクトップで開発環境への Visual Studio ショートカットをダブルクリックして開発環境を開きます。</span><span class="sxs-lookup"><span data-stu-id="bfac7-151">If the development environment is not already open, on the Desktop, double-click the Visual Studio shortcut to open the development environment.</span></span>
2.  <span data-ttu-id="bfac7-152">**ファイル**メニューで、**開く** &gt; **プロジェクト/ソリューション**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="bfac7-152">On the **File** menu, click **Open** &gt; **Project/Solution**.</span></span>
3.  <span data-ttu-id="bfac7-153">**プロジェクトを開く**ダイアログ ボックスで、C:\FmLab\FMTutorial を参照し、**FMTutorial** ソリューションを選択してから**開く**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="bfac7-153">In the **Open Project** dialog box, browse to C:\FmLab\FMTutorial, select the **FMTutorial** solution, and then click **Open**.</span></span>
4.  <span data-ttu-id="bfac7-154">FMTutorial プロジェクトが**ソリューション エクスプローラー**に表示されます。</span><span class="sxs-lookup"><span data-stu-id="bfac7-154">The FMTutorial project appears in **Solution Explorer**.</span></span>

## <a name="use-a-template-to-create-the-form"></a><span data-ttu-id="bfac7-155">テンプレートを使用してフォームを作成</span><span class="sxs-lookup"><span data-stu-id="bfac7-155">Use a template to create the form</span></span>
<span data-ttu-id="bfac7-156">Visual Studio を使用して **FmtCustomer** フォームを作成します。</span><span class="sxs-lookup"><span data-stu-id="bfac7-156">Use Visual Studio to create the **FmtCustomer** form.</span></span> <span data-ttu-id="bfac7-157">テンプレートを使用して、新しいマスターの詳細フォームを作成します。</span><span class="sxs-lookup"><span data-stu-id="bfac7-157">You’ll use a template to create a new master details form.</span></span> <span data-ttu-id="bfac7-158">このチュートリアルのデータ ソースは、スターター形式によって提供されています。</span><span class="sxs-lookup"><span data-stu-id="bfac7-158">The data source for this tutorial is provided by the starter form.</span></span> <span data-ttu-id="bfac7-159">ただし、グリッドと詳細ビューにフィールドを追加し、マスター詳細フォーム パターンを適用します。</span><span class="sxs-lookup"><span data-stu-id="bfac7-159">However, you’ll add fields to the grid and details view and apply the Master Details form pattern.</span></span>

1.  <span data-ttu-id="bfac7-160">**ソリューション エクスプローラー**で、**FMTutorial** プロジェクトを右クリックして**追加**をポイントしてから**既存の項目**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="bfac7-160">In **Solution Explorer**, right-click the **FMTutorial** project, point to **Add**, and then click **Existing Item**.</span></span>
2.  <span data-ttu-id="bfac7-161">**既存の品目を追加**ウィンドウで、C:\FmLab を参照し、**AxForm\_FmtCustomer** を選択してから**追加**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="bfac7-161">In the **Add Existing Item** window, browse to C:\FmLab, select **AxForm\_FmtCustomer**, and then click **Add**.</span></span> <span data-ttu-id="bfac7-162">ソリューション エクスプローラーの **FMTutorial** プロジェクトの下に **FmtCustomer** フォームが表示されます。</span><span class="sxs-lookup"><span data-stu-id="bfac7-162">The **FmtCustomer** form appears at the bottom of the **FMTutorial** project in Solution Explorer.</span></span>
3.  <span data-ttu-id="bfac7-163">ソリューション エクスプローラーで、**FmtCustomer** をダブルクリックします。</span><span class="sxs-lookup"><span data-stu-id="bfac7-163">In Solution Explorer, double-click **FmtCustomer**.</span></span> <span data-ttu-id="bfac7-164">フォーム デザイナーで、フォームを開きます。</span><span class="sxs-lookup"><span data-stu-id="bfac7-164">The form opens in the form designer.</span></span>
4.  <span data-ttu-id="bfac7-165">フォーム デザイナーで、**デザイン**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="bfac7-165">In the Form designer, click **Design**.</span></span> <span data-ttu-id="bfac7-166">**プロパティ** ウィンドウで、次の値を指定します。</span><span class="sxs-lookup"><span data-stu-id="bfac7-166">In the **Properties** window, specify the following values.</span></span>

    | <span data-ttu-id="bfac7-167">**プロパティ**</span><span class="sxs-lookup"><span data-stu-id="bfac7-167">**Property**</span></span> | <span data-ttu-id="bfac7-168">**値**</span><span class="sxs-lookup"><span data-stu-id="bfac7-168">**Value**</span></span>   |
    |--------------|-------------|
    | <span data-ttu-id="bfac7-169">データ ソース</span><span class="sxs-lookup"><span data-stu-id="bfac7-169">Data Source</span></span>  | <span data-ttu-id="bfac7-170">FmtCustomer</span><span class="sxs-lookup"><span data-stu-id="bfac7-170">FmtCustomer</span></span> |
    | <span data-ttu-id="bfac7-171">キャプション</span><span class="sxs-lookup"><span data-stu-id="bfac7-171">Caption</span></span>      | <span data-ttu-id="bfac7-172">顧客</span><span class="sxs-lookup"><span data-stu-id="bfac7-172">Customers</span></span>   |

5.  <span data-ttu-id="bfac7-173">フォーム デザイナーで、**デザイン** &gt; **GridDetailsTab** &gt; **TabPageGrid** &gt; **MainGrid** とクリックしてから **MainGrid** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="bfac7-173">In the Form designer, click **Design** &gt; **GridDetailsTab** &gt; **TabPageGrid** &gt; **MainGrid**, and then click **MainGrid**.</span></span>
6.  <span data-ttu-id="bfac7-174">**プロパティ** ウィンドウで、**データ ソース**をクリックしてから **FmtCustomer** を選択して **FmtCustomer** テーブルをグリッドにバインドします。</span><span class="sxs-lookup"><span data-stu-id="bfac7-174">In the **Properties** window, click **Data Source**, and then select **FmtCustomer** to bind the **FmtCustomer** table to the grid.</span></span> <span data-ttu-id="bfac7-175">データ ソースからのフィールドを使用して、グリッドに列を追加できるようになりました。</span><span class="sxs-lookup"><span data-stu-id="bfac7-175">You can now use the fields from the data source to add columns to the grid.</span></span>
7.  <span data-ttu-id="bfac7-176">**データ ソース** &gt; **FmtCustomer** &gt; **フィールド**とクリックし、グリッドにフィールドを追加します。</span><span class="sxs-lookup"><span data-stu-id="bfac7-176">Click **Data sources** &gt; **FmtCustomer** &gt; **Fields** to add fields to the grid.</span></span>
    1.  <span data-ttu-id="bfac7-177">**名**をクリックし、**Ctrl**キーを押しながら、表示された順序で次の追加フィールドを選択します。</span><span class="sxs-lookup"><span data-stu-id="bfac7-177">Click **FirstName**, press and hold the **Ctrl** key, and then select the following additional fields in the order shown:</span></span>
        - <span data-ttu-id="bfac7-178">姓</span><span class="sxs-lookup"><span data-stu-id="bfac7-178">LastName</span></span>
        - <span data-ttu-id="bfac7-179">CellPhone</span><span class="sxs-lookup"><span data-stu-id="bfac7-179">CellPhone</span></span>
        - <span data-ttu-id="bfac7-180">DriverLicense</span><span class="sxs-lookup"><span data-stu-id="bfac7-180">DriverLicense</span></span>
        - <span data-ttu-id="bfac7-181">電子メール</span><span class="sxs-lookup"><span data-stu-id="bfac7-181">Email</span></span>

    2.  <span data-ttu-id="bfac7-182">協調表示されたフィールドを **Design** &gt; **GridDetailsTab**&gt; **TabPageGrid** &gt; **MainGrid** にドラッグします。</span><span class="sxs-lookup"><span data-stu-id="bfac7-182">Drag the highlighted fields to **Design** &gt; **GridDetailsTab**&gt; **TabPageGrid** &gt; **MainGrid**.</span></span> <span data-ttu-id="bfac7-183">次の図は、グリッド ノードを展開してフィールドを追加した後のグリッドを示しています。</span><span class="sxs-lookup"><span data-stu-id="bfac7-183">The following illustration shows the grid after expanding the grid node and adding the fields.</span></span> 

        ![CustForm3](./media/custform3.png)     

8.  <span data-ttu-id="bfac7-185">**保存** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="bfac7-185">Click **Save**.</span></span>
9.  <span data-ttu-id="bfac7-186">**デザイン** &gt; **GridDetailsTab** &gt; **TabPageDetails** &gt; **TitleGroup** の順にクリックし、レコード ヘッダーを詳細ビューに追加します。</span><span class="sxs-lookup"><span data-stu-id="bfac7-186">Click **Design** &gt; **GridDetailsTab** &gt; **TabPageDetails** &gt; **TitleGroup** to add the record header to the details view.</span></span>
10. <span data-ttu-id="bfac7-187">**HeaderTitle** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="bfac7-187">Click **HeaderTitle**.</span></span> <span data-ttu-id="bfac7-188">**プロパティ** ウィンドウで、次の値を指定します。</span><span class="sxs-lookup"><span data-stu-id="bfac7-188">In the **Properties** window, specify the following values.</span></span>

    | <span data-ttu-id="bfac7-189">**プロパティ**</span><span class="sxs-lookup"><span data-stu-id="bfac7-189">**Property**</span></span> | <span data-ttu-id="bfac7-190">**値**</span><span class="sxs-lookup"><span data-stu-id="bfac7-190">**Value**</span></span>   |
    |--------------|-------------|
    | <span data-ttu-id="bfac7-191">データ ソース</span><span class="sxs-lookup"><span data-stu-id="bfac7-191">Data Source</span></span>  | <span data-ttu-id="bfac7-192">FmtCustomer</span><span class="sxs-lookup"><span data-stu-id="bfac7-192">FmtCustomer</span></span> |
    | <span data-ttu-id="bfac7-193">データ メソッド</span><span class="sxs-lookup"><span data-stu-id="bfac7-193">Data Method</span></span>  | <span data-ttu-id="bfac7-194">titleFields</span><span class="sxs-lookup"><span data-stu-id="bfac7-194">titleFields</span></span> |

11. <span data-ttu-id="bfac7-195">詳細ビューにコンテンツを追加するには、**デザイン** &gt; **GridDetailsTab** &gt; **TabPageDetails** &gt; **DetailsBodyTab** &gt; **一般**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="bfac7-195">Click **Design** &gt; **GridDetailsTab** &gt; **TabPageDetails** &gt; **DetailsBodyTab** &gt; **General** to add content to the details view.</span></span>
    1.  <span data-ttu-id="bfac7-196">**FmtCustomer** &gt; **データ ソース** &gt; **FmtCustomer** &gt; **フィールド**とクリックし、Ctrl キーを押したまま、次のフィールドを選択します。</span><span class="sxs-lookup"><span data-stu-id="bfac7-196">Click **FmtCustomer** &gt; **Data sources** &gt; **FmtCustomer** &gt; **Fields**, press and hold the Ctrl key, and then select the following fields:</span></span>
        -   <span data-ttu-id="bfac7-197">名</span><span class="sxs-lookup"><span data-stu-id="bfac7-197">FirstName</span></span>
        -   <span data-ttu-id="bfac7-198">姓</span><span class="sxs-lookup"><span data-stu-id="bfac7-198">LastName</span></span>
        -   <span data-ttu-id="bfac7-199">CellPhone</span><span class="sxs-lookup"><span data-stu-id="bfac7-199">CellPhone</span></span>
        -   <span data-ttu-id="bfac7-200">DriverLicense</span><span class="sxs-lookup"><span data-stu-id="bfac7-200">DriverLicense</span></span>
        -   <span data-ttu-id="bfac7-201">電子メール</span><span class="sxs-lookup"><span data-stu-id="bfac7-201">Email</span></span>

    2.  <span data-ttu-id="bfac7-202">協調表示されたフィールドを**一般**にドラッグし、**保存**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="bfac7-202">Drag the highlighted fields onto **General**, and then click **Save**.</span></span>

## <a name="view-the-form"></a><span data-ttu-id="bfac7-203">フォームの表示</span><span class="sxs-lookup"><span data-stu-id="bfac7-203">View the form</span></span>
<span data-ttu-id="bfac7-204">正しく読み込まれることを確認するためにフォームを実行します。</span><span class="sxs-lookup"><span data-stu-id="bfac7-204">Run the form to verify that it loads correctly.</span></span>

1.  <span data-ttu-id="bfac7-205">**ソリューション エクスプローラー**で、**FmtCustomer** を右クリックしてから、**スタートアップ オブジェクトとして設定**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="bfac7-205">In **Solution Explorer**, right-click **FmtCustomer**, and then click **Set as Startup Object**.</span></span>
2.  <span data-ttu-id="bfac7-206">**Ctrl+F5** キーを押します。</span><span class="sxs-lookup"><span data-stu-id="bfac7-206">Press **Ctrl+F5**.</span></span> <span data-ttu-id="bfac7-207">グリッド ビューは、次の図のように表示する必要があります。</span><span class="sxs-lookup"><span data-stu-id="bfac7-207">The grid view should render like the following illustration.</span></span> 

    <span data-ttu-id="bfac7-208">[![CustForm4](./media/custform4-1024x567.png)](./media/custform4.png)</span><span class="sxs-lookup"><span data-stu-id="bfac7-208">[![CustForm4](./media/custform4-1024x567.png)](./media/custform4.png)</span></span>

3.  <span data-ttu-id="bfac7-209">アプリケーション バーで、**Microsoft Office を開く** &gt; **Excel にエクスポート &gt; 顧客** をクリックして、グリッド ビューの情報を Microsoft Excel スプレッドシートに送信します。</span><span class="sxs-lookup"><span data-stu-id="bfac7-209">On the application bar, click **Open in Microsoft Office** &gt; **Export to Excel &gt; Customers** to send the information in the grid view to a Microsoft Excel spreadsheet.</span></span> <span data-ttu-id="bfac7-210">(ページを終了するかどうかを確認するダイアログが表示されたら、「このページを終了」をクリックします。) 求められたら、**開く**をクリックして Excel でデータを表示します。</span><span class="sxs-lookup"><span data-stu-id="bfac7-210">(If a dialog appears asking if you’re sure you want to leave the page, click “Leave this page”.) When asked, click **Open** to view the data in Excel.</span></span>
4.  <span data-ttu-id="bfac7-211">Excel を閉じます。</span><span class="sxs-lookup"><span data-stu-id="bfac7-211">Close Excel.</span></span>
5.  <span data-ttu-id="bfac7-212">**Tony** をクリックしてそのレコードの詳細ビューに移動します。</span><span class="sxs-lookup"><span data-stu-id="bfac7-212">Click **Tony** to navigate to the details view for that record.</span></span> 

    <span data-ttu-id="bfac7-213">[![CustForm5](./media/custform5-1024x567.png)](./media/custform5.png)</span><span class="sxs-lookup"><span data-stu-id="bfac7-213">[![CustForm5](./media/custform5-1024x567.png)](./media/custform5.png)</span></span>

6.  <span data-ttu-id="bfac7-214">**閉じる**またはブラウザーの 戻る ボタンをクリックすると、グリッド ビューに戻ります。</span><span class="sxs-lookup"><span data-stu-id="bfac7-214">Click **Close**  (or the browser Back button) to go back to the grid view.</span></span>

## <a name="apply-a-pattern-to-the-form"></a><span data-ttu-id="bfac7-215">フォームにパターンを適用します</span><span class="sxs-lookup"><span data-stu-id="bfac7-215">Apply a pattern to the form</span></span>
<span data-ttu-id="bfac7-216">Visual Studio を使用して **顧客** フォームに Master Details のフォーム パターンを適用します。</span><span class="sxs-lookup"><span data-stu-id="bfac7-216">Use Visual Studio to apply the Master Details form pattern to the **Customer** form.</span></span> <span data-ttu-id="bfac7-217">フォーム パターンを適用すると、フォームに期待される構造が確実に適用されます。</span><span class="sxs-lookup"><span data-stu-id="bfac7-217">Applying a form pattern ensures your form has the expected structure.</span></span> <span data-ttu-id="bfac7-218">また、パターンの一部であるノードでプロパティの値を自動的に設定することでデザイン体験を簡素化します。</span><span class="sxs-lookup"><span data-stu-id="bfac7-218">It also simplifies the design experience by automatically setting the values of properties in the nodes that are part of the pattern.</span></span>

1.  <span data-ttu-id="bfac7-219">**デザイン** を右クリックして **パターンの適用** をポイントし、**詳細マスター** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="bfac7-219">Right-click **Design**, point to **Apply pattern,** and then click **Details Master**.</span></span>

    <span data-ttu-id="bfac7-220">[![CustForm6](./media/custform6.png)](./media/custform6.png)</span><span class="sxs-lookup"><span data-stu-id="bfac7-220">[![CustForm6](./media/custform6.png)](./media/custform6.png)</span></span>

    <span data-ttu-id="bfac7-221">[![CustForm7](./media/custform7.png)](./media/custform7.png)</span><span class="sxs-lookup"><span data-stu-id="bfac7-221">[![CustForm7](./media/custform7.png)](./media/custform7.png)</span></span>

2.  <span data-ttu-id="bfac7-222">欠落しているナビゲーション リスト グループを追加します。</span><span class="sxs-lookup"><span data-stu-id="bfac7-222">Add the missing Navigation List group.</span></span> <span data-ttu-id="bfac7-223">パターン情報パネルが赤色でハイライトされると、このコントロールがないことを示します。</span><span class="sxs-lookup"><span data-stu-id="bfac7-223">The red highlighting in the Patterns Information Panel indicates that this control is missing.</span></span>
    1.  <span data-ttu-id="bfac7-224">**デザイン** を右クリックして **新規** をクリックし、**グループ** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="bfac7-224">Right-click **Design**, point to **New**, and then click **Group**.</span></span>
    2.  <span data-ttu-id="bfac7-225">**プロパティ** ウィンドウの**名前**プロパティに、**SidePanel** と入力します。</span><span class="sxs-lookup"><span data-stu-id="bfac7-225">In the **Properties** window, in the **Name** property, enter **SidePanel**.</span></span>
    3.  <span data-ttu-id="bfac7-226">**SidePanel** をクリックし、**Alt + ↑**を押してこのグループを **GridDetailsTab (タブ)** の上の移動します。</span><span class="sxs-lookup"><span data-stu-id="bfac7-226">Click **SidePanel**, and press **Alt+Up** to move this group above the **GridDetailsTab (Tab)**.</span></span>

3.  <span data-ttu-id="bfac7-227">**デザイン**を再度クリックします。</span><span class="sxs-lookup"><span data-stu-id="bfac7-227">Click **Design** again.</span></span> <span data-ttu-id="bfac7-228">**ナビゲーション リスト**と**パネル タブ**の周りの黄色のハイライトは、パターンが正常に適用される前にこれらの各ノードの下で解決する必要のある問題があることを示します。</span><span class="sxs-lookup"><span data-stu-id="bfac7-228">The yellow highlighting around the **Navigation List** and the **Panel Tab** indicate that there are problems that need to be resolved under each of these nodes before the pattern can be successfully applied.</span></span>

    <span data-ttu-id="bfac7-229">[![CustForm8](./media/custform8.png)](./media/custform8.png)</span><span class="sxs-lookup"><span data-stu-id="bfac7-229">[![CustForm8](./media/custform8.png)](./media/custform8.png)</span></span>

    <span data-ttu-id="bfac7-230">[![CustForm9](./media/custform9.png)](./media/custform9.png)</span><span class="sxs-lookup"><span data-stu-id="bfac7-230">[![CustForm9](./media/custform9.png)](./media/custform9.png)</span></span>

4.  <span data-ttu-id="bfac7-231">パターン情報パネルで **SidePanel** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="bfac7-231">In the Patterns Information Panel, click **SidePanel**.</span></span>

    <span data-ttu-id="bfac7-232">[![CustForm10](./media/custform10.png)](./media/custform10.png)</span><span class="sxs-lookup"><span data-stu-id="bfac7-232">[![CustForm10](./media/custform10.png)](./media/custform10.png)</span></span>

    <span data-ttu-id="bfac7-233">[![CustForm11](./media/custform11.png)](./media/custform11.png)</span><span class="sxs-lookup"><span data-stu-id="bfac7-233">[![CustForm11](./media/custform11.png)](./media/custform11.png)</span></span>

5.  <span data-ttu-id="bfac7-234">欠落しているコントロールを追加します。</span><span class="sxs-lookup"><span data-stu-id="bfac7-234">Add the missing controls.</span></span>
    1.  <span data-ttu-id="bfac7-235">**SidePanel** を右クリックして **新規** をクリックし、**QuickFilter** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="bfac7-235">Right-click **SidePanel**, point to **New**, and then click **QuickFilter**.</span></span>
    2.  <span data-ttu-id="bfac7-236">**プロパティ** ウィンドウで、次の値を指定します。</span><span class="sxs-lookup"><span data-stu-id="bfac7-236">In the **Properties** window, specify the following values.</span></span>

        | <span data-ttu-id="bfac7-237">**プロパティ**</span><span class="sxs-lookup"><span data-stu-id="bfac7-237">**Property**</span></span> | <span data-ttu-id="bfac7-238">**値**</span><span class="sxs-lookup"><span data-stu-id="bfac7-238">**Value**</span></span>      |
        |--------------|----------------|
        | <span data-ttu-id="bfac7-239">氏名</span><span class="sxs-lookup"><span data-stu-id="bfac7-239">Name</span></span>           | <span data-ttu-id="bfac7-240">SidePanelQuickFilter</span><span class="sxs-lookup"><span data-stu-id="bfac7-240">SidePanelQuickFilter</span></span>                            |
        | <span data-ttu-id="bfac7-241">ターゲット コントロール</span><span class="sxs-lookup"><span data-stu-id="bfac7-241">Target Control</span></span> | <span data-ttu-id="bfac7-242">MainGrid *この QuickFilter には、フォーム上の主要なグリッドと同じフィルター処理に使用できる列が必要です*</span><span class="sxs-lookup"><span data-stu-id="bfac7-242">MainGrid *This QuickFilter should have the same columns available for filtering as the main grid on the form*</span></span> |

    3.  <span data-ttu-id="bfac7-243">**SidePanel** を右クリックして **新規** をクリックし、**グリッド** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="bfac7-243">Right-click **SidePanel**, point to **New**, and then click **Grid.**</span></span>

        | <span data-ttu-id="bfac7-244">**プロパティ**</span><span class="sxs-lookup"><span data-stu-id="bfac7-244">**Property**</span></span> | <span data-ttu-id="bfac7-245">**値**</span><span class="sxs-lookup"><span data-stu-id="bfac7-245">**Value**</span></span>      |
        |--------------|----------------|
        | <span data-ttu-id="bfac7-246">氏名</span><span class="sxs-lookup"><span data-stu-id="bfac7-246">Name</span></span>         | <span data-ttu-id="bfac7-247">NavigationList</span><span class="sxs-lookup"><span data-stu-id="bfac7-247">NavigationList</span></span> |
        | <span data-ttu-id="bfac7-248">データソース</span><span class="sxs-lookup"><span data-stu-id="bfac7-248">Datasource</span></span>   | <span data-ttu-id="bfac7-249">FmtCustomer</span><span class="sxs-lookup"><span data-stu-id="bfac7-249">FmtCustomer</span></span>    |

6.  <span data-ttu-id="bfac7-250">ナビゲーション リストに識別するフィールドを追加します。</span><span class="sxs-lookup"><span data-stu-id="bfac7-250">Add identifying fields to the Navigation list.</span></span> <span data-ttu-id="bfac7-251">**NavigationList** を右クリックして **新規** をポイントし、**文字列** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="bfac7-251">Right-click **NavigationList**, point to **New**, and then click **String**.</span></span>
    1.  <span data-ttu-id="bfac7-252">**プロパティ** ウィンドウで、次の値を指定します。</span><span class="sxs-lookup"><span data-stu-id="bfac7-252">In the **Properties** window, specify the following values.</span></span>

        | <span data-ttu-id="bfac7-253">**プロパティ**</span><span class="sxs-lookup"><span data-stu-id="bfac7-253">**Property**</span></span> | <span data-ttu-id="bfac7-254">**値**</span><span class="sxs-lookup"><span data-stu-id="bfac7-254">**Value**</span></span>             |
        |--------------|-----------------------|
        | <span data-ttu-id="bfac7-255">DataSource</span><span class="sxs-lookup"><span data-stu-id="bfac7-255">DataSource</span></span>   | <span data-ttu-id="bfac7-256">FmtCustomer</span><span class="sxs-lookup"><span data-stu-id="bfac7-256">FmtCustomer</span></span>           |
        | <span data-ttu-id="bfac7-257">DataMethod</span><span class="sxs-lookup"><span data-stu-id="bfac7-257">DataMethod</span></span>   | <span data-ttu-id="bfac7-258">fullName</span><span class="sxs-lookup"><span data-stu-id="bfac7-258">fullName</span></span>              |
        | <span data-ttu-id="bfac7-259">氏名</span><span class="sxs-lookup"><span data-stu-id="bfac7-259">Name</span></span>         | <span data-ttu-id="bfac7-260">FmtCustomer\_FullName</span><span class="sxs-lookup"><span data-stu-id="bfac7-260">FmtCustomer\_FullName</span></span> |

    2.  <span data-ttu-id="bfac7-261">電話番号を簡易リストに追加するには、**データ ソース**&gt;**FmtCustomer**&gt;**フィールド**を展開します。</span><span class="sxs-lookup"><span data-stu-id="bfac7-261">Expand **Data Sources** &gt; **FmtCustomer** &gt; **Fields** to add phone numbers to the Simple list.</span></span>
    3.  <span data-ttu-id="bfac7-262">**CellPhone** フィールドを **Design &gt; SidePanel &gt; NavigationList** の下のグリッドにドラッグします。</span><span class="sxs-lookup"><span data-stu-id="bfac7-262">Drag the **CellPhone** field onto the grid under **Design &gt; SidePanel &gt; NavigationList**.</span></span>

7.  <span data-ttu-id="bfac7-263">**SidePanel** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="bfac7-263">Click **SidePanel**.</span></span> <span data-ttu-id="bfac7-264">**パターン情報パネル**は、このサブツリーのコントロールがパターンに完全に準拠していることを示しています。</span><span class="sxs-lookup"><span data-stu-id="bfac7-264">Notice the **Patterns Information Panel** is now indicating that the controls in this subtree are in full compliance with the pattern.</span></span>

    ![CustForm12](./media/custform12.png)

    ![CustForm13](./media/custform13.png)

8.  <span data-ttu-id="bfac7-267">**デザイン** &gt; **GridDetailsTab** とクリックします。</span><span class="sxs-lookup"><span data-stu-id="bfac7-267">Click **Design** &gt; **GridDetailsTab**.</span></span> <span data-ttu-id="bfac7-268">サブノードの周りの黄色のハイライトは、フォーム パターンが正常に適用される前に両方のノードの下で解決する必要のある問題があることを示します。</span><span class="sxs-lookup"><span data-stu-id="bfac7-268">The yellow highlighting around the subnodes indicates that there are problems that need to be resolved under both nodes before the form pattern can be successfully applied.</span></span>

    <span data-ttu-id="bfac7-269">[![CustForm14](./media/custform14.png)](./media/custform14.png)</span><span class="sxs-lookup"><span data-stu-id="bfac7-269">[![CustForm14](./media/custform14.png)](./media/custform14.png)</span></span>

    <span data-ttu-id="bfac7-270">[![CustForm15](./media/custform15.png)](./media/custform15.png)</span><span class="sxs-lookup"><span data-stu-id="bfac7-270">[![CustForm15](./media/custform15.png)](./media/custform15.png)</span></span>

9.  <span data-ttu-id="bfac7-271">パターンは**グリッド パネル**が**詳細パネル**の後に配置されることを期待します。</span><span class="sxs-lookup"><span data-stu-id="bfac7-271">Notice that the pattern expects the **Grid Panel** to be after the **Details Panel.**</span></span> <span data-ttu-id="bfac7-272">**TabPageGrid** をクリックし、**Alt + ↓**キーを押してそのタブを**詳細パネル**の下に移動します。</span><span class="sxs-lookup"><span data-stu-id="bfac7-272">Click **TabPageGrid** and press **Alt+Down** to move that tab below the **Details Panel**.</span></span>
10. <span data-ttu-id="bfac7-273">**GridDetailsTab** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="bfac7-273">Click **GridDetailsTab**.</span></span> <span data-ttu-id="bfac7-274">**TabPageDetails** タブ ページはパターンに準拠するようになりました。</span><span class="sxs-lookup"><span data-stu-id="bfac7-274">The **TabPageDetails** tab page now adheres to the pattern.</span></span> <span data-ttu-id="bfac7-275">ただし、**TabPageGrid** タブ ページには更なる注意が必要です。</span><span class="sxs-lookup"><span data-stu-id="bfac7-275">However, the **TabPageGrid** tab page needs additional attention.</span></span>

    <span data-ttu-id="bfac7-276">[![CustForm16](./media/custform16.png)](./media/custform16.png)</span><span class="sxs-lookup"><span data-stu-id="bfac7-276">[![CustForm16](./media/custform16.png)](./media/custform16.png)</span></span>

    <span data-ttu-id="bfac7-277">[![CustForm17](./media/custform17.png)](./media/custform17.png)</span><span class="sxs-lookup"><span data-stu-id="bfac7-277">[![CustForm17](./media/custform17.png)](./media/custform17.png)</span></span>

11. <span data-ttu-id="bfac7-278">**TabPageGrid** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="bfac7-278">Click **TabPageGrid**.</span></span> <span data-ttu-id="bfac7-279">デザイナーでフォーカスがすぐに **TabPageGrid** がオンになり、**パターン情報パネル**が更新されています。</span><span class="sxs-lookup"><span data-stu-id="bfac7-279">Focus in the designer is now on **TabPageGrid**, and the **Patterns Information Panel** has been updated.</span></span>

    <span data-ttu-id="bfac7-280">[![CustForm18](./media/custform18.png)](./media/custform18.png)</span><span class="sxs-lookup"><span data-stu-id="bfac7-280">[![CustForm18](./media/custform18.png)](./media/custform18.png)</span></span>

    <span data-ttu-id="bfac7-281">[![CustForm19](./media/custform19.png)](./media/custform19.png)</span><span class="sxs-lookup"><span data-stu-id="bfac7-281">[![CustForm19](./media/custform19.png)](./media/custform19.png)</span></span>

12. <span data-ttu-id="bfac7-282">**パターン情報パネル** には、**TabPageGrid** コンテナーの上部で欠落しているグループ コントロールが表示されるようになりました。</span><span class="sxs-lookup"><span data-stu-id="bfac7-282">The **Patterns Information Panel** now indicates a missing Group control at the top of the **TabPageGrid** container.</span></span>
    1.  <span data-ttu-id="bfac7-283">**TabPageGrid** を右クリックして **新規** をポイントし、**グループ** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="bfac7-283">Right-click **TabPageGrid**, point to **New**, and then click **Group**.</span></span>
    2.  <span data-ttu-id="bfac7-284">**Alt+上方向**キーを 2 回押して、そのグループをグループの最初のコントロールとして配置します。</span><span class="sxs-lookup"><span data-stu-id="bfac7-284">Press **Alt+Up** two times to position the group as the first control in the group.</span></span>
    3.  <span data-ttu-id="bfac7-285">**プロパティ** ウィンドウの**名前**プロパティに、**GridCustomFilterGroup** と入力します。</span><span class="sxs-lookup"><span data-stu-id="bfac7-285">In the **Properties** window, in the **Name** property, enter **GridCustomFilterGroup**.</span></span> <span data-ttu-id="bfac7-286">[![CustForm20](./media/custform20.png)](./media/custform20.png)</span><span class="sxs-lookup"><span data-stu-id="bfac7-286">[![CustForm20](./media/custform20.png)](./media/custform20.png)</span></span>

13. <span data-ttu-id="bfac7-287">パターンが、**GridCustomFilterGroup** に適用されるサブパターンをお探しています。</span><span class="sxs-lookup"><span data-stu-id="bfac7-287">The pattern is looking for a subpattern to be applied to **GridCustomFilterGroup**.</span></span> <span data-ttu-id="bfac7-288">**GridCustomFilterGroup** を右クリックして **パターンの適用** をポイントし、**カスタムおよびクイック フィルター** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="bfac7-288">Right-click **GridCustomFilterGroup,** point to **Apply pattern**, and then click **Custom and Quick Filters**.</span></span>

    <span data-ttu-id="bfac7-289">[![CustForm21](./media/custform21.png)](./media/custform21.png)</span><span class="sxs-lookup"><span data-stu-id="bfac7-289">[![CustForm21](./media/custform21.png)](./media/custform21.png)</span></span>

    <span data-ttu-id="bfac7-290">[![CustForm22](./media/custform22.png)](./media/custform22.png)</span><span class="sxs-lookup"><span data-stu-id="bfac7-290">[![CustForm22](./media/custform22.png)](./media/custform22.png)</span></span>

14. <span data-ttu-id="bfac7-291">**カスタムおよびクイック フィルター** サブパターンには、QuickFilter コントロールが必須です。</span><span class="sxs-lookup"><span data-stu-id="bfac7-291">The **Custom and Quick Filters** subpattern requires a QuickFilter control.</span></span>
    1.  <span data-ttu-id="bfac7-292">**GridCustomFilterGroup** を右クリックして **新規** をクリックし、**QuickFilter** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="bfac7-292">Right-click **GridCustomFilterGroup**, point to **New**, and then click **QuickFilter**.</span></span>
    2.  <span data-ttu-id="bfac7-293">**プロパティ** ウィンドウで、次の値を指定します。</span><span class="sxs-lookup"><span data-stu-id="bfac7-293">In the **Properties** window, specify the following values.</span></span>

        | <span data-ttu-id="bfac7-294">**プロパティ**</span><span class="sxs-lookup"><span data-stu-id="bfac7-294">**Property**</span></span>   | <span data-ttu-id="bfac7-295">**値**</span><span class="sxs-lookup"><span data-stu-id="bfac7-295">**Value**</span></span>           |
        |----------------|---------------------|
        | <span data-ttu-id="bfac7-296">氏名</span><span class="sxs-lookup"><span data-stu-id="bfac7-296">Name</span></span>           | <span data-ttu-id="bfac7-297">MainGridQuickFilter</span><span class="sxs-lookup"><span data-stu-id="bfac7-297">MainGridQuickFilter</span></span> |
        | <span data-ttu-id="bfac7-298">ターゲット コントロール</span><span class="sxs-lookup"><span data-stu-id="bfac7-298">Target Control</span></span> | <span data-ttu-id="bfac7-299">MainGrid</span><span class="sxs-lookup"><span data-stu-id="bfac7-299">MainGrid</span></span>            |

15. <span data-ttu-id="bfac7-300">コントロール ツリーを参照して設計し、各コントロールで**パターン情報パネル**に問題が表示されなくなった方法に注意てください。</span><span class="sxs-lookup"><span data-stu-id="bfac7-300">Browse up the control tree to design and notice how the **Patterns Information Panel** now shows no issues under each of the controls.</span></span>
16. <span data-ttu-id="bfac7-301">**Ctrl+S** キーを押してフォームを保存します。</span><span class="sxs-lookup"><span data-stu-id="bfac7-301">Press **Ctrl+S** to save the form.</span></span>

## <a name="view-the-details-form"></a><span data-ttu-id="bfac7-302">詳細フォームの表示</span><span class="sxs-lookup"><span data-stu-id="bfac7-302">View the details form</span></span>
<span data-ttu-id="bfac7-303">詳細ビューとグリッド ビューに表示するフォームを実行します。</span><span class="sxs-lookup"><span data-stu-id="bfac7-303">Run the form to see the Details view and the Grid view.</span></span>

1.  <span data-ttu-id="bfac7-304">**Ctrl+F5** キーを押してプロジェクトを実行します。</span><span class="sxs-lookup"><span data-stu-id="bfac7-304">Press **Ctrl+F5** to run the project.</span></span> <span data-ttu-id="bfac7-305">次の図は、グリッド ビューの表示方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="bfac7-305">The following illustration shows how the grid view appears.</span></span>

    <span data-ttu-id="bfac7-306">[![CustForm23](./media/custform23-1024x599.png)](./media/custform23.png)</span><span class="sxs-lookup"><span data-stu-id="bfac7-306">[![CustForm23](./media/custform23-1024x599.png)](./media/custform23.png)</span></span>

2.  <span data-ttu-id="bfac7-307">**Phil** をクリックしてそのレコードの詳細ビューに移動します。</span><span class="sxs-lookup"><span data-stu-id="bfac7-307">Click **Phil** to go to the details view for that record.</span></span> 

    <span data-ttu-id="bfac7-308">[![CustForm24](./media/custform24-1024x599.png)](./media/custform24.png)</span><span class="sxs-lookup"><span data-stu-id="bfac7-308">[![CustForm24](./media/custform24-1024x599.png)](./media/custform24.png)</span></span>

3.  <span data-ttu-id="bfac7-309">ナビゲーション リストを開くには、フォームの左側にある**リストを表示**ボタンをクリックします。</span><span class="sxs-lookup"><span data-stu-id="bfac7-309">Click the **Show list** button on the left side of the form to open the navigation list.</span></span> 

    <span data-ttu-id="bfac7-310">[![CustForm25](./media/custform25-1024x597.png)](./media/custform25.png)</span><span class="sxs-lookup"><span data-stu-id="bfac7-310">[![CustForm25](./media/custform25-1024x597.png)](./media/custform25.png)</span></span>

4.  <span data-ttu-id="bfac7-311">グリッド表示に戻るには、**閉じる** (またはブラウザーの [戻る] ボタン) をクリックします。</span><span class="sxs-lookup"><span data-stu-id="bfac7-311">To go back to the grid view, click **Close** (or the browser Back button).</span></span>
5.  <span data-ttu-id="bfac7-312">Visual Studio に戻ります。</span><span class="sxs-lookup"><span data-stu-id="bfac7-312">Return to Visual Studio.</span></span>

## <a name="add-subpatterns"></a><span data-ttu-id="bfac7-313">サブパターンの追加</span><span class="sxs-lookup"><span data-stu-id="bfac7-313">Add subpatterns</span></span>
1.  <span data-ttu-id="bfac7-314">Visual Studio の、フォーム デザイナーで、**FmtCustomer** を右クリックして **アドイン** をポイントしてから、**フォーム統計情報** を選択します。</span><span class="sxs-lookup"><span data-stu-id="bfac7-314">In Visual Studio, in the Form designer, right-click **FmtCustomer**, point to **Addins**, and then select **Form statistics**.</span></span> 

    <span data-ttu-id="bfac7-315">[![CustForm26](./media/custform26.png)](./media/custform26.png)</span><span class="sxs-lookup"><span data-stu-id="bfac7-315">[![CustForm26](./media/custform26.png)](./media/custform26.png)</span></span> 

    <span data-ttu-id="bfac7-316">**フォーム統計** アドインは、フォームの状態に関するいくつかの役に立つデータ ポイントを提供します。</span><span class="sxs-lookup"><span data-stu-id="bfac7-316">The **Form Statistics** add-in provides several useful data points about the state of the form.</span></span> <span data-ttu-id="bfac7-317">これには、次のものが含まれます。</span><span class="sxs-lookup"><span data-stu-id="bfac7-317">This includes:</span></span>
    -   <span data-ttu-id="bfac7-318">**パターン = 未指定のカウント** – フォーム パターンまたはサブパターンが適用されていないノードの数。</span><span class="sxs-lookup"><span data-stu-id="bfac7-318">**Pattern=Unspecified count** – The number of nodes for which no form pattern or subpattern has been applied.</span></span>
    -   <span data-ttu-id="bfac7-319">**パターン = カスタム カウント** – カスタム パターンが適用されたノードの数。構造が既存のパターンに適合しなかったことを意味します。</span><span class="sxs-lookup"><span data-stu-id="bfac7-319">**Pattern=Custom count** – The number of nodes for which a custom pattern was applied, meaning the structure did not fit with any existing pattern.</span></span>
    -   <span data-ttu-id="bfac7-320">**パターン カバレッジ** – フォーム上のコントロールのうち、フォーム パターンまたはサブパターンの対象となるものの割合。</span><span class="sxs-lookup"><span data-stu-id="bfac7-320">**Pattern coverage** – The percentage of controls on the form that are covered by the form pattern or a subpattern.</span></span> <span data-ttu-id="bfac7-321">100% の値は、完全に対象となるフォームを示します。</span><span class="sxs-lookup"><span data-stu-id="bfac7-321">A value of 100% indicates a fully-covered form.</span></span> 

        <span data-ttu-id="bfac7-322">[![CustForm27](./media/custform27.png)](./media/custform27.png)</span><span class="sxs-lookup"><span data-stu-id="bfac7-322">[![CustForm27](./media/custform27.png)](./media/custform27.png)</span></span>

2.  <span data-ttu-id="bfac7-323">このフォームのパターン カバレッジを完成させるには、Pattern = Unspecified カウントをゼロにする必要があります。</span><span class="sxs-lookup"><span data-stu-id="bfac7-323">To complete pattern coverage for this form, the Pattern=Unspecified count should be zero.</span></span> <span data-ttu-id="bfac7-324">Visual Studio のフォーム検索を使用して、フォーム内の「指定されていない」すべてのインスタンスを検索します。</span><span class="sxs-lookup"><span data-stu-id="bfac7-324">Use the Visual Studio form search to find all instances of “unspecified “in the form.</span></span> 

    <span data-ttu-id="bfac7-325">[![CustForm28](./media/custform28.png)](./media/custform28.png)</span><span class="sxs-lookup"><span data-stu-id="bfac7-325">[![CustForm28](./media/custform28.png)](./media/custform28.png)</span></span>

3.  <span data-ttu-id="bfac7-326">**一般**タブ ページには入力コントロールのみが含まれており、このクイックタブにはカスタム レイアウトが不要なため、応答レイアウトを保証するためにフィールドおよびフィールド グループのパターンを適用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="bfac7-326">Because the **General** tab page contains only input controls and no custom layout is required for this FastTab, the Fields and Field Groups pattern should be applied to guarantee a responsive layout.</span></span> <span data-ttu-id="bfac7-327">**全般** を右クリックして **パターンの適用** をポイントし、**フィールドおよびフィールド グループ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="bfac7-327">Right-click **General**, point to **Apply pattern**, and then select **Fields and Field Groups**.</span></span>
4.  <span data-ttu-id="bfac7-328">画面の右端で、**検索のクリア**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="bfac7-328">On the far right of the screen, click **Clear search**.</span></span> 

    <span data-ttu-id="bfac7-329">[![CustForm29](./media/custform29.png)](./media/custform29.png)</span><span class="sxs-lookup"><span data-stu-id="bfac7-329">[![CustForm29](./media/custform29.png)](./media/custform29.png)</span></span>

5.  <span data-ttu-id="bfac7-330">**Ctrl+S** キーを押してフォームを保存します。</span><span class="sxs-lookup"><span data-stu-id="bfac7-330">Press **Ctrl+S** to save the form.</span></span>
6.  <span data-ttu-id="bfac7-331">手順 1 を繰り返して **フォーム統計** アドインを再度実行し、フォームがパターンによって完全にカバーされていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="bfac7-331">Repeat step 1 to run the **Form Statistics** add-in a second time to verify the form is fully-covered by patterns.</span></span> 

    <span data-ttu-id="bfac7-332">[![CustForm30](./media/custform30.png)](./media/custform30.png)</span><span class="sxs-lookup"><span data-stu-id="bfac7-332">[![CustForm30](./media/custform30.png)](./media/custform30.png)</span></span>

7.  <span data-ttu-id="bfac7-333">**Ctrl+F5** キーを押してプロジェクトを実行し、更新されたフォームを表示します。</span><span class="sxs-lookup"><span data-stu-id="bfac7-333">Press **Ctrl+F5** to run the project and see the updated form.</span></span>
8.  <span data-ttu-id="bfac7-334">**里美 (サンプル)** をクリックし、詳細ビューに移動します。</span><span class="sxs-lookup"><span data-stu-id="bfac7-334">Click **Adrian** to go to the details view.</span></span> <span data-ttu-id="bfac7-335">次の図は、フィールドおよびフィールド グループのサブパターンを適用し、フィールドが反応しやすいようにレイアウトした後に詳細ビューがどのように表示されるかを示しています。</span><span class="sxs-lookup"><span data-stu-id="bfac7-335">The following illustration shows how the details view now appears after applying the Fields and Field Groups subpattern so that the fields lay out responsively.</span></span> <span data-ttu-id="bfac7-336">ブラウザーの幅を変更することで、ブラウザーの幅を十分に埋めるためにフィールド レイアウトがどのように調整されるのかが分かります。</span><span class="sxs-lookup"><span data-stu-id="bfac7-336">By changing the browser width, you’ll see how the field layout adjusts to better fill the width of the browser.</span></span> 

    <span data-ttu-id="bfac7-337">[![CustForm31](./media/custform31-1024x674.png)](./media/custform31.png)</span><span class="sxs-lookup"><span data-stu-id="bfac7-337">[![CustForm31](./media/custform31-1024x674.png)](./media/custform31.png)</span></span>

9.  <span data-ttu-id="bfac7-338">Visual Studio に戻る</span><span class="sxs-lookup"><span data-stu-id="bfac7-338">Return to Visual Studio</span></span>

## <a name="determine-the-amount-of-remaining-patterns-work-in-a-model"></a><span data-ttu-id="bfac7-339">モデル内で残っているパターンの作業の量を決定する</span><span class="sxs-lookup"><span data-stu-id="bfac7-339">Determine the amount of remaining patterns work in a model</span></span>
1.  <span data-ttu-id="bfac7-340">**Finance and Operations** をクリックし、**アドイン**をポイントし、**フォーム パターン レポートを実行**を選択します。</span><span class="sxs-lookup"><span data-stu-id="bfac7-340">Click **Finance and Operations**, point to **Addins**, and then select **Run form patterns report**.</span></span> 

    <span data-ttu-id="bfac7-341">[![CustForm32](./media/custform32-1024x469.png)](./media/custform32.png)</span><span class="sxs-lookup"><span data-stu-id="bfac7-341">[![CustForm32](./media/custform32-1024x469.png)](./media/custform32.png)</span></span> 

    <span data-ttu-id="bfac7-342">フォームのパターン レポートが生成されたときに表示される通知ダイアログです。</span><span class="sxs-lookup"><span data-stu-id="bfac7-342">A notification dialog will be shown when the form patterns report has been generated.</span></span> 

    <span data-ttu-id="bfac7-343">[![CustForm33](./media/custform33.png)](./media/custform33.png)</span><span class="sxs-lookup"><span data-stu-id="bfac7-343">[![CustForm33](./media/custform33.png)](./media/custform33.png)</span></span>

2.  <span data-ttu-id="bfac7-344">PatternsReport ファイルを Excel で開きます。</span><span class="sxs-lookup"><span data-stu-id="bfac7-344">Open the PatternsReport file in Excel.</span></span>
3.  <span data-ttu-id="bfac7-345">フリート管理チュートリアル モデルへのレポートをフィルター処理します。</span><span class="sxs-lookup"><span data-stu-id="bfac7-345">Filter the report to the Fleet Management Tutorial model.</span></span>
    1.  <span data-ttu-id="bfac7-346">**データ** &gt; **フィルター**の順にクリックします。</span><span class="sxs-lookup"><span data-stu-id="bfac7-346">Click **Data** &gt; **Filter**.</span></span>
    2.  <span data-ttu-id="bfac7-347">FleetMgmntTutorial への**モデル**列をフィルター処理します。</span><span class="sxs-lookup"><span data-stu-id="bfac7-347">Filter the **Model** column to FleetMgmntTutorial.</span></span> 

        <span data-ttu-id="bfac7-348">[![CustForm34](./media/custform34-1024x422.png)](./media/custform34.png)</span><span class="sxs-lookup"><span data-stu-id="bfac7-348">[![CustForm34](./media/custform34-1024x422.png)](./media/custform34.png)</span></span>


<span data-ttu-id="bfac7-349">レポートには、現在適用されている最上位のフォーム パターンと、パターンでカバーされているフォーム上のコントロールの割合など、このモデルのフォームに関するパターン関連の情報が表示されます。</span><span class="sxs-lookup"><span data-stu-id="bfac7-349">The report shows pattern-related information regarding the forms in this model including the top-level form pattern currently applied, and the percentage of controls on the form covered by patterns.</span></span> <span data-ttu-id="bfac7-350">これは、1 つまたは複数のモデルの残りのパターンの作業を追跡するために使用できます。</span><span class="sxs-lookup"><span data-stu-id="bfac7-350">This can be used to track the remaining patterns work in one or more models.</span></span>  



