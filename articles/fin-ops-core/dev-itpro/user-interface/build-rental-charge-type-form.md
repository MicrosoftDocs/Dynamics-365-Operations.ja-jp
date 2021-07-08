---
title: レンタル料金のタイプ フォームの構築
description: このラボでは、簡易リストのフォームを作成します。 シンプル リスト フォームでは、参照データまたは 6 つ以下のフィールドが含まれるセカンダリ データを表示できます。
author: jasongre
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.custom: 13671
ms.assetid: 9b4f244c-f058-416c-b3c2-6f4ca29c8db8
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8cb4695a4a8b2a10d3d171256ffd2dd7e2a7e958
ms.sourcegitcommit: ff09736563d3cd2bc74c7664edd1767b218401cb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/04/2021
ms.locfileid: "6188107"
---
# <a name="build-the-rental-charge-type-form"></a><span data-ttu-id="35dcd-104">レンタル料金のタイプ フォームの構築</span><span class="sxs-lookup"><span data-stu-id="35dcd-104">Build the Rental Charge Type form</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="35dcd-105">このラボでは、簡易リストのフォームを作成します。</span><span class="sxs-lookup"><span data-stu-id="35dcd-105">In this lab you’ll create a Simple List form.</span></span> <span data-ttu-id="35dcd-106">シンプル リスト フォームでは、参照データまたは 6 つ以下のフィールドが含まれるセカンダリ データを表示できます。</span><span class="sxs-lookup"><span data-stu-id="35dcd-106">A Simple List form can show reference or secondary data that has six or fewer fields.</span></span> <span data-ttu-id="35dcd-107">たとえば、作成するフォームは、レンタル料金のタイプについて一覧表示して説明します。</span><span class="sxs-lookup"><span data-stu-id="35dcd-107">For example, the form that you create will list and describe the types of rental charges.</span></span> 

## <a name="prerequisites"></a><span data-ttu-id="35dcd-108">前提条件</span><span class="sxs-lookup"><span data-stu-id="35dcd-108">Prerequisites</span></span>

<span data-ttu-id="35dcd-109">このチュートリアルでは、リモート デスクトップを使用して環境にアクセスし、インスタンスの管理者としてプロビジョニングされる必要があります。</span><span class="sxs-lookup"><span data-stu-id="35dcd-109">For this tutorial, you’ll need to access the environment using Remote Desktop, and be provisioned as an administrator on the instance.</span></span> <span data-ttu-id="35dcd-110">詳細については、「[アクセス インスタンス](../dev-tools/access-instances.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="35dcd-110">For more information, see [Access Instances](../dev-tools/access-instances.md).</span></span>

## <a name="overview"></a><span data-ttu-id="35dcd-111">概要</span><span class="sxs-lookup"><span data-stu-id="35dcd-111">Overview</span></span>
<span data-ttu-id="35dcd-112">フォームを作成するには、既存のフォーム **FmtChargeType** から開始します。</span><span class="sxs-lookup"><span data-stu-id="35dcd-112">To create the form, you’ll start from the existing form, **FmtChargeType**.</span></span> <span data-ttu-id="35dcd-113">このフォームは、簡易リストのパターンを使用します。</span><span class="sxs-lookup"><span data-stu-id="35dcd-113">This form uses the Simple List pattern.</span></span> <span data-ttu-id="35dcd-114">次の図は、**FmtChargeType** フォームと簡易リスト パターンからの必要なコントロールを示しています。</span><span class="sxs-lookup"><span data-stu-id="35dcd-114">The following illustration shows the **FmtChargeType** form with the required controls from the Simple List pattern.</span></span> 

<span data-ttu-id="35dcd-115">[![FmtChargeType フォームのスクリーン ショット](./media/rentalcharge1.png)](./media/rentalcharge1.png)</span><span class="sxs-lookup"><span data-stu-id="35dcd-115">[![Screen shot of FmtChargeType form](./media/rentalcharge1.png)](./media/rentalcharge1.png)</span></span> 

<span data-ttu-id="35dcd-116">フォーム パターンに従うことによって、この簡易リストのフォームは、他の簡易リストのフォームと同じ構造とレイアウトを持つようになります。</span><span class="sxs-lookup"><span data-stu-id="35dcd-116">Adhering to the form pattern ensures that this Simple List form has the same structure and layout as other Simple List forms.</span></span>

## <a name="key-concepts"></a><span data-ttu-id="35dcd-117">重要な概念</span><span class="sxs-lookup"><span data-stu-id="35dcd-117">Key concepts</span></span>
-   <span data-ttu-id="35dcd-118">パターンを使用して簡易リストのフォームを作成します。</span><span class="sxs-lookup"><span data-stu-id="35dcd-118">Create a Simple List form using a pattern.</span></span>
-   <span data-ttu-id="35dcd-119">テーブルをフォームにバインドします。</span><span class="sxs-lookup"><span data-stu-id="35dcd-119">Bind a table to the form.</span></span>
-   <span data-ttu-id="35dcd-120">フォームにコントロールを追加します。</span><span class="sxs-lookup"><span data-stu-id="35dcd-120">Add controls to the form.</span></span>
-   <span data-ttu-id="35dcd-121">Visual Studio とブラウザーを使用してフォームを表示します。</span><span class="sxs-lookup"><span data-stu-id="35dcd-121">View the form using Visual Studio and a browser.</span></span>

## <a name="setup"></a><span data-ttu-id="35dcd-122">セットアップ</span><span class="sxs-lookup"><span data-stu-id="35dcd-122">Setup</span></span>
### <a name="import-the-tutorial-project-and-transactional-data"></a><span data-ttu-id="35dcd-123">チュートリアル プロジェクトおよびトランザクション データのインポート</span><span class="sxs-lookup"><span data-stu-id="35dcd-123">Import the tutorial project and transactional data</span></span>

<span data-ttu-id="35dcd-124">Visual Studio を使用してチュートリアル プロジェクトをインポートします。</span><span class="sxs-lookup"><span data-stu-id="35dcd-124">Use Visual Studio to import the tutorial project.</span></span> <span data-ttu-id="35dcd-125">チュートリアル プロジェクトには、このチュートリアルを完了するために使用する成果物が含まれています。</span><span class="sxs-lookup"><span data-stu-id="35dcd-125">The tutorial project includes the artifacts that you’ll use to complete this tutorial.</span></span> <span data-ttu-id="35dcd-126">Visual Studio を使用して FMTutorial プロジェクトを開き、チュートリアル用のデータを読み込みます。</span><span class="sxs-lookup"><span data-stu-id="35dcd-126">Use Visual Studio to open the FMTutorial project and load the data for the tutorial.</span></span> <span data-ttu-id="35dcd-127">フリート管理チュートリアルのデータを読み込むために、FMTDataHelper クラスを使用します。</span><span class="sxs-lookup"><span data-stu-id="35dcd-127">You’ll use the FMTDataHelper class to load data for the Fleet Management tutorial.</span></span> <span data-ttu-id="35dcd-128">これが作業する最初のチュートリアルである場合は、[アクセス Microsoft インスタンス](../dev-tools/access-instances.md)を確認し、ローカル VM で作業している場合に、管理者ユーザーを提供するかどうかを確認します。</span><span class="sxs-lookup"><span data-stu-id="35dcd-128">If this is the first tutorial you’re working on, review [Access Microsoft Instances](../dev-tools/access-instances.md) and make sure you provision your administrator user if you’re working on a local VM.</span></span>

1.  <span data-ttu-id="35dcd-129">フリート管理のサンプルを <https://github.com/Microsoft/FMLab> からダウンロードし、**C:\\** に保存してから解凍します。</span><span class="sxs-lookup"><span data-stu-id="35dcd-129">Download the Fleet Management sample from <https://github.com/Microsoft/FMLab>, save it to **C:\\**, and unzip it.</span></span>
2.  <span data-ttu-id="35dcd-130">デスクトップで、Visual Studio ショートカットをダブルクリックして、開発環境を開きます。</span><span class="sxs-lookup"><span data-stu-id="35dcd-130">On the desktop, double-click the Visual Studio shortcut to open the development environment.</span></span>
3.  <span data-ttu-id="35dcd-131">**Finance and Operations** メニューで、**プロジェクトのインポート** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="35dcd-131">On the **Finance and Operations** menu, click **Import Project**.</span></span>
4.  <span data-ttu-id="35dcd-132">**プロジェクトのインポート** ウィンドウで、**ファイル名** テキスト ボックスの隣にある、省略記号ボタンをクリックします。</span><span class="sxs-lookup"><span data-stu-id="35dcd-132">In the **Import Project** window, next to the **Filename** text box, click the ellipsis button.</span></span>
5.  <span data-ttu-id="35dcd-133">**インポートするファイルの選択** ウィンドウで、C:\FMLab を参照して FMTutorialDataModel.axpp をクリックしてから **開く** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="35dcd-133">In the **Select the file to import** window, browse to C:\FMLab, click FMTutorialDataModel.axpp, and then click **Open**.</span></span>
6.  <span data-ttu-id="35dcd-134">**プロジェクト ファイルの場所** テキスト ボックスに、C:\FMLab と入力します。</span><span class="sxs-lookup"><span data-stu-id="35dcd-134">In the **Project file location** text box, enter C:\FMLab.</span></span>
7.  <span data-ttu-id="35dcd-135">**要素の上書き** オプションをオンにし、**現在のソリューション** ラジオ オプションをオンにします。</span><span class="sxs-lookup"><span data-stu-id="35dcd-135">Select the **Overwrite Elements** option, and the **Current solution** radio button.</span></span> <span data-ttu-id="35dcd-136">次の図は、完了した **インポート プロジェクト** ダイアログ ボックスを示しています。</span><span class="sxs-lookup"><span data-stu-id="35dcd-136">The following illustration shows the completed **Import Project** dialog box.</span></span> 

    <span data-ttu-id="35dcd-137">[![完了したプロジェクトのインポート ダイアログ ボックスのスクリーン ショット](./media/rentalcharge2.png)](./media/rentalcharge2.png)</span><span class="sxs-lookup"><span data-stu-id="35dcd-137">[![Screen shot of completed Import Project dialog box](./media/rentalcharge2.png)](./media/rentalcharge2.png)</span></span>

8.  <span data-ttu-id="35dcd-138">**OK** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="35dcd-138">Click **OK**.</span></span>
9.  <span data-ttu-id="35dcd-139">デザイナー **ソリューション エクスプローラー** で、**クラス** を展開して、**FMTutorial** プロジェクトで **FMTDataHelper** を右クリックしてから、**スタートアップ オブジェクトとして設定** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="35dcd-139">In **Solution Explorer**, expand **Classes, and** under the **FMTutorial** project, right-click **FMTDataHelper**, and then click **Set as Startup Object**.</span></span>
10. <span data-ttu-id="35dcd-140">**ビルド** メニューで、**ソリューションの再構築** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="35dcd-140">On the **Build** menu, click **Rebuild Solution**.</span></span> <span data-ttu-id="35dcd-141">タイムスタンプに関係なく、プロジェクトのすべてのファイルを確実に作成するには、リビルドを使用します。</span><span class="sxs-lookup"><span data-stu-id="35dcd-141">Use the rebuild to make sure that all of the files in the project are built regardless of timestamps.</span></span> <span data-ttu-id="35dcd-142">**出力** ウィンドウでビルドの進行状況を表示できます。</span><span class="sxs-lookup"><span data-stu-id="35dcd-142">You can view the build progress in the **Output** window.</span></span>
11. <span data-ttu-id="35dcd-143">ビルドが完了すると、**Ctrl + F5** を押してプロジェクトを実行します。</span><span class="sxs-lookup"><span data-stu-id="35dcd-143">After the build completes, press **Ctrl+F5** to run the project.</span></span> <span data-ttu-id="35dcd-144">ブラウザーが開き、データをインポートするクラスが実行されます。</span><span class="sxs-lookup"><span data-stu-id="35dcd-144">The browser will open and run the class that imports the data.</span></span>

## <a name="open-the-fmtutorial-project"></a><span data-ttu-id="35dcd-145">FMTutorial プロジェクトを開く</span><span class="sxs-lookup"><span data-stu-id="35dcd-145">Open the FMTutorial project</span></span>
<span data-ttu-id="35dcd-146">Visual Studio を使用して FMTutorial プロジェクトを開きます。</span><span class="sxs-lookup"><span data-stu-id="35dcd-146">Use Visual Studio to open the FMTutorial project.</span></span> <span data-ttu-id="35dcd-147">Visual Studio を開き、FMTutorial プロジェクトが既に読み込まれている場合は、次のセクションに続行することができます。</span><span class="sxs-lookup"><span data-stu-id="35dcd-147">If you have Visual Studio open and have already loaded the FMTutorial project, you can continue to the next section.</span></span>

1.  <span data-ttu-id="35dcd-148">開発環境がまだ開いていない場合は、デスクトップで開発環境への Visual Studio ショートカットをダブルクリックして、開発環境を開きます。</span><span class="sxs-lookup"><span data-stu-id="35dcd-148">If the development environment isn’t already open, on the desktop, double-click the Visual Studio shortcut to open the development environment.</span></span>
2.  <span data-ttu-id="35dcd-149">**ファイル** メニューで、**開く** &gt; **プロジェクト/ソリューション** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="35dcd-149">On the **File** menu, click **Open** &gt; **Project/Solution**.</span></span>
3.  <span data-ttu-id="35dcd-150">**プロジェクトを開く** ダイアログ ボックスで、C:\FmLab\FMTutorial を参照し、**FMTutorial** ソリューションを選択してから **開く** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="35dcd-150">In the **Open Project** dialog box, browse to C:\FmLab\FMTutorial, select the **FMTutorial** solution, and then click **Open**</span></span>
4.  <span data-ttu-id="35dcd-151">FMTutorial プロジェクトが **ソリューション エクスプローラー** に表示されます。</span><span class="sxs-lookup"><span data-stu-id="35dcd-151">The FMTutorial project appears in **Solution Explorer**.</span></span>

## <a name="use-a-template-to-create-the-form"></a><span data-ttu-id="35dcd-152">テンプレートを使用してフォームを作成</span><span class="sxs-lookup"><span data-stu-id="35dcd-152">Use a template to create the form</span></span>
<span data-ttu-id="35dcd-153">Visual Studio を使用して **FmtChargeType** フォームを作成します。</span><span class="sxs-lookup"><span data-stu-id="35dcd-153">Use Visual Studio to create the **FmtChargeType** form.</span></span> <span data-ttu-id="35dcd-154">簡易リスト フォームを構築ためのテンプレートを使用します。</span><span class="sxs-lookup"><span data-stu-id="35dcd-154">You’ll use a template for building the Simple List form.</span></span> <span data-ttu-id="35dcd-155">また、フォームにデータ ソースを追加し、データ グリッドにフィールドを追加します。</span><span class="sxs-lookup"><span data-stu-id="35dcd-155">You’ll also add a data source to the form and add fields to the data grid.</span></span>

1.  <span data-ttu-id="35dcd-156">**ソリューション エクスプローラー** で、**FMTutorial** プロジェクトを右クリックして **追加** をポイントしてから **既存の項目** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="35dcd-156">In **Solution Explorer**, right-click the **FMTutorial** project, point to **Add**, and then click **Existing Item**.</span></span>
2.  <span data-ttu-id="35dcd-157">**既存の品目を追加** ウィンドウで、C:\FmLab を参照し、**AxForm\_FmtChargeType** をクリックしてから **追加** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="35dcd-157">In the **Add Existing Item** window, browse to C:\FmLab, click **AxForm\_FmtChargeType**, and then click **Add**.</span></span> <span data-ttu-id="35dcd-158">**ソリューション エクスプローラー** の **FMTutorial** プロジェクトの下に **FmtChargeType** フォームが表示されます。</span><span class="sxs-lookup"><span data-stu-id="35dcd-158">The **FmtChargeType** form appears at the bottom of the **FMTutorial** project in **Solution Explorer**.</span></span>
3.  <span data-ttu-id="35dcd-159">**ソリューション エクスプローラー** で、**FmtChargeType** をダブルクリックします。</span><span class="sxs-lookup"><span data-stu-id="35dcd-159">In **Solution Explorer**, double-click **FmtChargeType**.</span></span> <span data-ttu-id="35dcd-160">フォーム デザイナーで、フォームを開きます。</span><span class="sxs-lookup"><span data-stu-id="35dcd-160">The form opens in the Form designer.</span></span>
4.  <span data-ttu-id="35dcd-161">フォームのデータ ソースとして **FmtChargeType** テーブルを追加します。</span><span class="sxs-lookup"><span data-stu-id="35dcd-161">Add the **FmtChargeType** table as the data source for the form.</span></span> <span data-ttu-id="35dcd-162">**データ ソース** を右クリックし、**新しいデータ ソース** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="35dcd-162">Right-click **Data Sources,** and then click **New Data Source**.</span></span> <span data-ttu-id="35dcd-163">データ ソース ノードが追加されます。</span><span class="sxs-lookup"><span data-stu-id="35dcd-163">A data source node is added.</span></span>
5.  <span data-ttu-id="35dcd-164">前の手順でデータ ソース ノードをクリックします。</span><span class="sxs-lookup"><span data-stu-id="35dcd-164">Click the data source node from the previous step.</span></span> <span data-ttu-id="35dcd-165">**プロパティ** ウィンドウで、次のプロパティに指定された値を設定します。</span><span class="sxs-lookup"><span data-stu-id="35dcd-165">In the **Properties** window, populate the following properties with the specified values.</span></span>

    | <span data-ttu-id="35dcd-166">**プロパティ**</span><span class="sxs-lookup"><span data-stu-id="35dcd-166">**Property**</span></span> | <span data-ttu-id="35dcd-167">**値**</span><span class="sxs-lookup"><span data-stu-id="35dcd-167">**Value**</span></span>|
    |--------------|------|
    | <span data-ttu-id="35dcd-168">テーブル</span><span class="sxs-lookup"><span data-stu-id="35dcd-168">Table</span></span>        | <span data-ttu-id="35dcd-169">FMTChargeType</span><span class="sxs-lookup"><span data-stu-id="35dcd-169">FMTChargeType</span></span>|
    | <span data-ttu-id="35dcd-170">氏名</span><span class="sxs-lookup"><span data-stu-id="35dcd-170">Name</span></span>         | <span data-ttu-id="35dcd-171">FMTChargeType *まず Table プロパティの値を指定してください。このプロパティは、同じ値を使用するよう自動的に更新されます。*</span><span class="sxs-lookup"><span data-stu-id="35dcd-171">FMTChargeType *Be sure to specify the value for the Table property first. This property will automatically update to use that same value.*</span></span> |

    <span data-ttu-id="35dcd-172">次の図は、**FMTChargeType** テーブルを追加した後の **データソース** を示しています。</span><span class="sxs-lookup"><span data-stu-id="35dcd-172">The following illustration shows **Data Sources** after you add the **FMTChargeType** table.</span></span> 

    <span data-ttu-id="35dcd-173">[![FMTChargeType テーブルを追加した後のデータ ソースのスクリーン ショット](./media/rentalcharge3.png)](./media/rentalcharge3.png)</span><span class="sxs-lookup"><span data-stu-id="35dcd-173">[![Screen shot of Data Sources after you add FMTChargeType table](./media/rentalcharge3.png)](./media/rentalcharge3.png)</span></span>

6.  <span data-ttu-id="35dcd-174">フォーム デザイナーで、**デザイン** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="35dcd-174">In the Form designer, click **Design**.</span></span> <span data-ttu-id="35dcd-175">**プロパティ** ウィンドウで、次のプロパティに指定された値を設定します。</span><span class="sxs-lookup"><span data-stu-id="35dcd-175">In the **Properties** window, populate the following properties with the specified values.</span></span>

    | <span data-ttu-id="35dcd-176">**プロパティ**</span><span class="sxs-lookup"><span data-stu-id="35dcd-176">**Property**</span></span> | <span data-ttu-id="35dcd-177">**値**</span><span class="sxs-lookup"><span data-stu-id="35dcd-177">**Value**</span></span>                                                                    |
    |--------------|------------------------------------------------------------------------------|
    | <span data-ttu-id="35dcd-178">キャプション</span><span class="sxs-lookup"><span data-stu-id="35dcd-178">Caption</span></span>      | <span data-ttu-id="35dcd-179">レンタル料金のタイプ *これは、フォームの上部に表示されるラベルです。*</span><span class="sxs-lookup"><span data-stu-id="35dcd-179">Rental charge types *This is the label that appears at the top of the form.*</span></span> |
    | <span data-ttu-id="35dcd-180">データ ソース</span><span class="sxs-lookup"><span data-stu-id="35dcd-180">Data Source</span></span>  | <span data-ttu-id="35dcd-181">FMTChargeType *フォームのデータ ソースを指定するには、このプロパティを使用します。*</span><span class="sxs-lookup"><span data-stu-id="35dcd-181">FMTChargeType *Use this property to specify the data source for the form.*</span></span>   |

7.  <span data-ttu-id="35dcd-182">フォーム デザイナーで、**デザイン** &gt; **グリッド** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="35dcd-182">In the Form designer, click **Design** &gt; **Grid**.</span></span>
8.  <span data-ttu-id="35dcd-183">FMTChargeType データ ソースを簡易リスト フォームで表示されているグリッドにバインドします。</span><span class="sxs-lookup"><span data-stu-id="35dcd-183">Bind the FMTChargeType data source to the grid that appears in the simple list form.</span></span> <span data-ttu-id="35dcd-184">**プロパティ** ウィンドウの **データ ソース** に、**FMTChargeType** を入力します。</span><span class="sxs-lookup"><span data-stu-id="35dcd-184">In the **Properties** window, in **Data Source**, enter **FMTChargeType**.</span></span>
9.  <span data-ttu-id="35dcd-185">グリッドにフィールドを追加する前に、データ ソースを指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="35dcd-185">You have to specify the data source before you add fields to the grid.</span></span> <span data-ttu-id="35dcd-186">次に、データ ソースからのフィールドを使用して、グリッドに列を追加することができます。</span><span class="sxs-lookup"><span data-stu-id="35dcd-186">You can then use the fields from the data source to add columns to the grid.</span></span> <span data-ttu-id="35dcd-187">グリッドにデータ ソースから 2 つのフォームを追加します。</span><span class="sxs-lookup"><span data-stu-id="35dcd-187">Add two fields from the data source to the grid.</span></span> <span data-ttu-id="35dcd-188">追加するフィールドは、簡易リスト フォームの列として表示されます。</span><span class="sxs-lookup"><span data-stu-id="35dcd-188">The fields you add will appear as columns on the Simple List form.</span></span> <span data-ttu-id="35dcd-189">左側のウィンドウで、FMTChargeType データ ソース **フィールド** ノードを展開します。</span><span class="sxs-lookup"><span data-stu-id="35dcd-189">Expand the FMTChargeType data source **Fields** node in the left pane.</span></span> <span data-ttu-id="35dcd-190">**Ctrl** を押し、次のフィールドをクリックします。</span><span class="sxs-lookup"><span data-stu-id="35dcd-190">Press **Ctrl** and then click the following fields:</span></span>
    -   <span data-ttu-id="35dcd-191">ChargeType</span><span class="sxs-lookup"><span data-stu-id="35dcd-191">ChargeType</span></span>
    -   <span data-ttu-id="35dcd-192">説明</span><span class="sxs-lookup"><span data-stu-id="35dcd-192">Description</span></span>

10. <span data-ttu-id="35dcd-193">選択したフィールドを右ウィンドウの **デザイン** &gt; **グリッド** にドラッグします。</span><span class="sxs-lookup"><span data-stu-id="35dcd-193">Drag the selected fields to **Design** &gt; **Grid** in the right pane.</span></span> <span data-ttu-id="35dcd-194">次の図は、グリッド ノードが展開され、2 つのフィールドが追加された後のグリッドを示しています。</span><span class="sxs-lookup"><span data-stu-id="35dcd-194">The following illustration shows the grid after the grid node is expanded and the two fields are added.</span></span> 

    <span data-ttu-id="35dcd-195">[![グリッド ノードが展開された後のグリッドを示すスクリーン ショット](./media/rentalcharge4.png)](./media/rentalcharge4.png)</span><span class="sxs-lookup"><span data-stu-id="35dcd-195">[![Screen shot showing grid after the grid node is expanded](./media/rentalcharge4.png)](./media/rentalcharge4.png)</span></span>

11. <span data-ttu-id="35dcd-196">フォーム デザイナーで、**デザイン &gt; CustomFilterGroup &gt; QuickFilter** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="35dcd-196">In the Form designer, click **Design &gt; CustomFilterGroup &gt; QuickFilter**.</span></span>
12. <span data-ttu-id="35dcd-197">**プロパティ** ウィンドウで、**TargetControl** をクリックしてから **グリッド** を選択して **QuickFilter** コントロールをフォームのグリッドにバインドします。</span><span class="sxs-lookup"><span data-stu-id="35dcd-197">In the **Properties** window, click **TargetControl**, and then select **Grid** to bind the **QuickFilter** control to the grid on the form.</span></span>
13. <span data-ttu-id="35dcd-198">**ファイル** &gt; **保存** **FmtChargeType** とクリックします。</span><span class="sxs-lookup"><span data-stu-id="35dcd-198">Click **File** &gt; **Save** **FmtChargeType**.</span></span>

## <a name="view-the-form"></a><span data-ttu-id="35dcd-199">フォームの表示</span><span class="sxs-lookup"><span data-stu-id="35dcd-199">View the form</span></span>
<span data-ttu-id="35dcd-200">Visual Studio を使用して、**FmtChargeType** フォームをビルドして実行します。</span><span class="sxs-lookup"><span data-stu-id="35dcd-200">Use Visual Studio to build and run the **FmtChargeType** form.</span></span>

1.  <span data-ttu-id="35dcd-201">**ソリューション エクスプローラー** で、**FmtChargeType** フォームを右クリックしてから、**スタートアップ オブジェクトとして設定** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="35dcd-201">In **Solution Explorer**, right-click the **FmtChargeType** form, and then click **Set as Startup Object**.</span></span>
2.  <span data-ttu-id="35dcd-202">Ctrl+F5 キーを押して、フォームをビルドおよび実行します。</span><span class="sxs-lookup"><span data-stu-id="35dcd-202">Press Ctrl+F5 to build and run the form.</span></span>
3.  <span data-ttu-id="35dcd-203">Internet Explorer でフォームが開きます。</span><span class="sxs-lookup"><span data-stu-id="35dcd-203">The form opens in Internet Explorer.</span></span>
4.  <span data-ttu-id="35dcd-204">レンタル料金タイプを追加するには、フォームの上部にあるアクション ペインで **新規** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="35dcd-204">To add a rental charge type, click **New** in the Action Pane at the top of the form.</span></span> <span data-ttu-id="35dcd-205">次の情報を追加します。</span><span class="sxs-lookup"><span data-stu-id="35dcd-205">Add the following information.</span></span>

    | <span data-ttu-id="35dcd-206">**レンタル料金のタイプ**</span><span class="sxs-lookup"><span data-stu-id="35dcd-206">**Rental Charge Type**</span></span> | <span data-ttu-id="35dcd-207">**説明**</span><span class="sxs-lookup"><span data-stu-id="35dcd-207">**Description**</span></span> |
    |------------------------|-----------------|
    | <span data-ttu-id="35dcd-208">クリーニング</span><span class="sxs-lookup"><span data-stu-id="35dcd-208">cleaning</span></span>               | <span data-ttu-id="35dcd-209">クリーニング代</span><span class="sxs-lookup"><span data-stu-id="35dcd-209">Cleaning fee</span></span>    |

5.  <span data-ttu-id="35dcd-210">アクション ウィンドウで、**保存** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="35dcd-210">In the Action Pane, click **Save**.</span></span>
6.  <span data-ttu-id="35dcd-211">ブラウザーを更新して、一覧に新しいレコードを表示します。</span><span class="sxs-lookup"><span data-stu-id="35dcd-211">Refresh the browser to see the new record in the list.</span></span> <span data-ttu-id="35dcd-212">次の図は、フォームの外観を示しています。</span><span class="sxs-lookup"><span data-stu-id="35dcd-212">The following illustration shows how the form should look.</span></span>

    <span data-ttu-id="35dcd-213">[![フォームの外観のスクリーン ショット](./media/rentalcharge5.png)](./media/rentalcharge5.png)</span><span class="sxs-lookup"><span data-stu-id="35dcd-213">[![Screen shot of how the form should look](./media/rentalcharge5.png)](./media/rentalcharge5.png)</span></span>

7.  <span data-ttu-id="35dcd-214">表示モードでフォームを開きます。</span><span class="sxs-lookup"><span data-stu-id="35dcd-214">The form opens in view mode.</span></span> <span data-ttu-id="35dcd-215">アクション ウィンドウの **編集** をクリックして、フォームを編集モードに切り替えます。</span><span class="sxs-lookup"><span data-stu-id="35dcd-215">Click **Edit** in the Action Pane to switch the form into edit mode.</span></span> <span data-ttu-id="35dcd-216">表示モードに戻るには、**オプション** をクリックしてから **読み取りモード** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="35dcd-216">To return to view mode, click **Options** and then **Read mode**.</span></span>






[!INCLUDE[footer-include](../../../includes/footer-banner.md)]