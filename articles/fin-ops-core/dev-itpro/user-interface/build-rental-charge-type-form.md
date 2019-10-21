---
title: レンタル料金のタイプ フォームの構築
description: このラボでは、簡易リストのフォームを作成します。 シンプル リスト フォームでは、参照データまたは 6 つ以下のフィールドが含まれるセカンダリ データを表示できます。 たとえば、作成するフォームは、レンタル料金のタイプについて一覧表示して説明します。
author: jasongre
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: sericks
ms.search.scope: Operations
ms.custom: 13671
ms.assetid: 9b4f244c-f058-416c-b3c2-6f4ca29c8db8
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 58a07639562acfc92326b281718d0f38131ebb7f
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/27/2019
ms.locfileid: "2183066"
---
# <a name="build-the-rental-charge-type-form"></a><span data-ttu-id="60f99-105">レンタル料金のタイプ フォームの構築</span><span class="sxs-lookup"><span data-stu-id="60f99-105">Build the Rental Charge Type form</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="60f99-106">このラボでは、簡易リストのフォームを作成します。</span><span class="sxs-lookup"><span data-stu-id="60f99-106">In this lab you’ll create a Simple List form.</span></span> <span data-ttu-id="60f99-107">シンプル リスト フォームでは、参照データまたは 6 つ以下のフィールドが含まれるセカンダリ データを表示できます。</span><span class="sxs-lookup"><span data-stu-id="60f99-107">A Simple List form can show reference or secondary data that has six or fewer fields.</span></span> <span data-ttu-id="60f99-108">たとえば、作成するフォームは、レンタル料金のタイプについて一覧表示して説明します。</span><span class="sxs-lookup"><span data-stu-id="60f99-108">For example, the form that you create will list and describe the types of rental charges.</span></span> 

<a name="prerequisites"></a><span data-ttu-id="60f99-109">前提条件</span><span class="sxs-lookup"><span data-stu-id="60f99-109">Prerequisites</span></span>
-------------

<span data-ttu-id="60f99-110">このチュートリアルでは、リモート デスクトップを使用して環境にアクセスし、インスタンスの管理者としてプロビジョニングされる必要があります。</span><span class="sxs-lookup"><span data-stu-id="60f99-110">For this tutorial, you’ll need to access the environment using Remote Desktop, and be provisioned as an administrator on the instance.</span></span> <span data-ttu-id="60f99-111">詳細については、「[アクセス インスタンス](../dev-tools/access-instances.md)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="60f99-111">For more information, see [Access Instances](../dev-tools/access-instances.md).</span></span>

## <a name="overview"></a><span data-ttu-id="60f99-112">概要</span><span class="sxs-lookup"><span data-stu-id="60f99-112">Overview</span></span>
<span data-ttu-id="60f99-113">フォームを作成するには、既存のフォーム **FmtChargeType** から開始します。</span><span class="sxs-lookup"><span data-stu-id="60f99-113">To create the form, you’ll start from the existing form, **FmtChargeType**.</span></span> <span data-ttu-id="60f99-114">このフォームは、簡易リストのパターンを使用します。</span><span class="sxs-lookup"><span data-stu-id="60f99-114">This form uses the Simple List pattern.</span></span> <span data-ttu-id="60f99-115">次の図は、**FmtChargeType** フォームと簡易リスト パターンからの必要なコントロールを示しています。</span><span class="sxs-lookup"><span data-stu-id="60f99-115">The following illustration shows the **FmtChargeType** form with the required controls from the Simple List pattern.</span></span> 

<span data-ttu-id="60f99-116">[![rentalcharge1](./media/rentalcharge1.png)](./media/rentalcharge1.png)</span><span class="sxs-lookup"><span data-stu-id="60f99-116">[![rentalcharge1](./media/rentalcharge1.png)](./media/rentalcharge1.png)</span></span> 

<span data-ttu-id="60f99-117">フォーム パターンに従うことによって、この簡易リストのフォームは、他の簡易リストのフォームと同じ構造とレイアウトを持つようになります。</span><span class="sxs-lookup"><span data-stu-id="60f99-117">Adhering to the form pattern ensures that this Simple List form has the same structure and layout as other Simple List forms.</span></span>

## <a name="key-concepts"></a><span data-ttu-id="60f99-118">重要な概念</span><span class="sxs-lookup"><span data-stu-id="60f99-118">Key concepts</span></span>
-   <span data-ttu-id="60f99-119">パターンを使用して簡易リストのフォームを作成します。</span><span class="sxs-lookup"><span data-stu-id="60f99-119">Create a Simple List form using a pattern.</span></span>
-   <span data-ttu-id="60f99-120">テーブルをフォームにバインドします。</span><span class="sxs-lookup"><span data-stu-id="60f99-120">Bind a table to the form.</span></span>
-   <span data-ttu-id="60f99-121">フォームにコントロールを追加します。</span><span class="sxs-lookup"><span data-stu-id="60f99-121">Add controls to the form.</span></span>
-   <span data-ttu-id="60f99-122">Visual Studio とブラウザーを使用してフォームを表示します。</span><span class="sxs-lookup"><span data-stu-id="60f99-122">View the form using Visual Studio and a browser.</span></span>

## <a name="setup"></a><span data-ttu-id="60f99-123">セットアップ</span><span class="sxs-lookup"><span data-stu-id="60f99-123">Setup</span></span>
### <a name="import-the-tutorial-project-and-transactional-data"></a><span data-ttu-id="60f99-124">チュートリアル プロジェクトおよびトランザクション データのインポート</span><span class="sxs-lookup"><span data-stu-id="60f99-124">Import the tutorial project and transactional data</span></span>

<span data-ttu-id="60f99-125">Visual Studio を使用してチュートリアル プロジェクトをインポートします。</span><span class="sxs-lookup"><span data-stu-id="60f99-125">Use Visual Studio to import the tutorial project.</span></span> <span data-ttu-id="60f99-126">チュートリアル プロジェクトには、このチュートリアルを完了するために使用する成果物が含まれています。</span><span class="sxs-lookup"><span data-stu-id="60f99-126">The tutorial project includes the artifacts that you’ll use to complete this tutorial.</span></span> <span data-ttu-id="60f99-127">Visual Studio を使用して FMTutorial プロジェクトを開き、チュートリアル用のデータを読み込みます。</span><span class="sxs-lookup"><span data-stu-id="60f99-127">Use Visual Studio to open the FMTutorial project and load the data for the tutorial.</span></span> <span data-ttu-id="60f99-128">フリート管理チュートリアルのデータを読み込むために、FMTDataHelper クラスを使用します。</span><span class="sxs-lookup"><span data-stu-id="60f99-128">You’ll use the FMTDataHelper class to load data for the Fleet Management tutorial.</span></span> <span data-ttu-id="60f99-129">これが作業する最初のチュートリアルである場合は、[アクセス Microsoft インスタンス](../dev-tools/access-instances.md)を確認し、ローカル VM で作業している場合に、管理者ユーザーを提供するかどうかを確認します。</span><span class="sxs-lookup"><span data-stu-id="60f99-129">If this is the first tutorial you’re working on, review [Access Microsoft Instances](../dev-tools/access-instances.md) and make sure you provision your administrator user if you’re working on a local VM.</span></span>

1.  <span data-ttu-id="60f99-130">フリート管理のサンプルを <https://github.com/Microsoft/FMLab> からダウンロードし、**C:\\** に保存してから解凍します。</span><span class="sxs-lookup"><span data-stu-id="60f99-130">Download the Fleet Management sample from <https://github.com/Microsoft/FMLab>, save it to **C:\\**, and unzip it.</span></span>
2.  <span data-ttu-id="60f99-131">デスクトップで、Visual Studio ショートカットをダブルクリックして、開発環境を開きます。</span><span class="sxs-lookup"><span data-stu-id="60f99-131">On the desktop, double-click the Visual Studio shortcut to open the development environment.</span></span>
3.  <span data-ttu-id="60f99-132">**Finance and Operations** メニューで、**プロジェクトのインポート**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="60f99-132">On the **Finance and Operations** menu, click **Import Project**.</span></span>
4.  <span data-ttu-id="60f99-133">**プロジェクトのインポート** ウィンドウで、**ファイル名**テキスト ボックスの隣にある、省略記号ボタンをクリックします。</span><span class="sxs-lookup"><span data-stu-id="60f99-133">In the **Import Project** window, next to the **Filename** text box, click the ellipsis button.</span></span>
5.  <span data-ttu-id="60f99-134">**インポートするファイルの選択**ウィンドウで、C:\FMLab を参照して FMTutorialDataModel.axpp をクリックしてから**開く**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="60f99-134">In the **Select the file to import** window, browse to C:\FMLab, click FMTutorialDataModel.axpp, and then click **Open**.</span></span>
6.  <span data-ttu-id="60f99-135">**プロジェクト ファイルの場所**テキスト ボックスに、C:\FMLab と入力します。</span><span class="sxs-lookup"><span data-stu-id="60f99-135">In the **Project file location** text box, enter C:\FMLab.</span></span>
7.  <span data-ttu-id="60f99-136">**要素の上書き** オプションをオンにし、**現在のソリューション** ラジオ オプションをオンにします。</span><span class="sxs-lookup"><span data-stu-id="60f99-136">Select the **Overwrite Elements** option, and the **Current solution** radio button.</span></span> <span data-ttu-id="60f99-137">次の図は、完了した **インポート プロジェクト** ダイアログ ボックスを示しています。</span><span class="sxs-lookup"><span data-stu-id="60f99-137">The following illustration shows the completed **Import Project** dialog box.</span></span> 

    <span data-ttu-id="60f99-138">[![rentalcharge2](./media/rentalcharge2.png)](./media/rentalcharge2.png)</span><span class="sxs-lookup"><span data-stu-id="60f99-138">[![rentalcharge2](./media/rentalcharge2.png)](./media/rentalcharge2.png)</span></span>

8.  <span data-ttu-id="60f99-139">**OK** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="60f99-139">Click **OK**.</span></span>
9.  <span data-ttu-id="60f99-140">デザイナー**ソリューション エクスプローラー**で、**クラス**を展開して、**FMTutorial** プロジェクトで **FMTDataHelper** を右クリックしてから、**スタートアップ オブジェクトとして設定**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="60f99-140">In **Solution Explorer**, expand **Classes, and** under the **FMTutorial** project, right-click **FMTDataHelper**, and then click **Set as Startup Object**.</span></span>
10. <span data-ttu-id="60f99-141">**ビルド**メニューで、**ソリューションの再構築**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="60f99-141">On the **Build** menu, click **Rebuild Solution**.</span></span> <span data-ttu-id="60f99-142">タイムスタンプに関係なく、プロジェクトのすべてのファイルを確実に作成するには、リビルドを使用します。</span><span class="sxs-lookup"><span data-stu-id="60f99-142">Use the rebuild to make sure that all of the files in the project are built regardless of timestamps.</span></span> <span data-ttu-id="60f99-143">**出力** ウィンドウでビルドの進行状況を表示できます。</span><span class="sxs-lookup"><span data-stu-id="60f99-143">You can view the build progress in the **Output** window.</span></span>
11. <span data-ttu-id="60f99-144">ビルドが完了すると、**Ctrl + F5** を押してプロジェクトを実行します。</span><span class="sxs-lookup"><span data-stu-id="60f99-144">After the build completes, press **Ctrl+F5** to run the project.</span></span> <span data-ttu-id="60f99-145">ブラウザーが開き、データをインポートするクラスが実行されます。</span><span class="sxs-lookup"><span data-stu-id="60f99-145">The browser will open and run the class that imports the data.</span></span>

## <a name="open-the-fmtutorial-project"></a><span data-ttu-id="60f99-146">FMTutorial プロジェクトを開く</span><span class="sxs-lookup"><span data-stu-id="60f99-146">Open the FMTutorial project</span></span>
<span data-ttu-id="60f99-147">Visual Studio を使用して FMTutorial プロジェクトを開きます。</span><span class="sxs-lookup"><span data-stu-id="60f99-147">Use Visual Studio to open the FMTutorial project.</span></span> <span data-ttu-id="60f99-148">Visual Studio を開き、FMTutorial プロジェクトが既に読み込まれている場合は、次のセクションに続行することができます。</span><span class="sxs-lookup"><span data-stu-id="60f99-148">If you have Visual Studio open and have already loaded the FMTutorial project, you can continue to the next section.</span></span>

1.  <span data-ttu-id="60f99-149">開発環境がまだ開いていない場合は、デスクトップで開発環境への Visual Studio ショートカットをダブルクリックして、開発環境を開きます。</span><span class="sxs-lookup"><span data-stu-id="60f99-149">If the development environment isn’t already open, on the desktop, double-click the Visual Studio shortcut to open the development environment.</span></span>
2.  <span data-ttu-id="60f99-150">**ファイル**メニューで、**開く** &gt; **プロジェクト/ソリューション**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="60f99-150">On the **File** menu, click **Open** &gt; **Project/Solution**.</span></span>
3.  <span data-ttu-id="60f99-151">**プロジェクトを開く**ダイアログ ボックスで、C:\FmLab\FMTutorial を参照し、**FMTutorial** ソリューションを選択してから**開く**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="60f99-151">In the **Open Project** dialog box, browse to C:\FmLab\FMTutorial, select the **FMTutorial** solution, and then click **Open**</span></span>
4.  <span data-ttu-id="60f99-152">FMTutorial プロジェクトが**ソリューション エクスプローラー**に表示されます。</span><span class="sxs-lookup"><span data-stu-id="60f99-152">The FMTutorial project appears in **Solution Explorer**.</span></span>

## <a name="use-a-template-to-create-the-form"></a><span data-ttu-id="60f99-153">テンプレートを使用してフォームを作成</span><span class="sxs-lookup"><span data-stu-id="60f99-153">Use a template to create the form</span></span>
<span data-ttu-id="60f99-154">Visual Studio を使用して **FmtChargeType** フォームを作成します。</span><span class="sxs-lookup"><span data-stu-id="60f99-154">Use Visual Studio to create the **FmtChargeType** form.</span></span> <span data-ttu-id="60f99-155">簡易リスト フォームを構築ためのテンプレートを使用します。</span><span class="sxs-lookup"><span data-stu-id="60f99-155">You’ll use a template for building the Simple List form.</span></span> <span data-ttu-id="60f99-156">また、フォームにデータ ソースを追加し、データ グリッドにフィールドを追加します。</span><span class="sxs-lookup"><span data-stu-id="60f99-156">You’ll also add a data source to the form and add fields to the data grid.</span></span>

1.  <span data-ttu-id="60f99-157">**ソリューション エクスプローラー**で、**FMTutorial** プロジェクトを右クリックして**追加**をポイントしてから**既存の項目**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="60f99-157">In **Solution Explorer**, right-click the **FMTutorial** project, point to **Add**, and then click **Existing Item**.</span></span>
2.  <span data-ttu-id="60f99-158">**既存の品目を追加**ウィンドウで、C:\FmLab を参照し、**AxForm\_FmtChargeType** をクリックしてから**追加**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="60f99-158">In the **Add Existing Item** window, browse to C:\FmLab, click **AxForm\_FmtChargeType**, and then click **Add**.</span></span> <span data-ttu-id="60f99-159">**ソリューション エクスプローラー**の **FMTutorial** プロジェクトの下に **FmtChargeType** フォームが表示されます。</span><span class="sxs-lookup"><span data-stu-id="60f99-159">The **FmtChargeType** form appears at the bottom of the **FMTutorial** project in **Solution Explorer**.</span></span>
3.  <span data-ttu-id="60f99-160">**ソリューション エクスプローラー**で、**FmtChargeType** をダブルクリックします。</span><span class="sxs-lookup"><span data-stu-id="60f99-160">In **Solution Explorer**, double-click **FmtChargeType**.</span></span> <span data-ttu-id="60f99-161">フォーム デザイナーで、フォームを開きます。</span><span class="sxs-lookup"><span data-stu-id="60f99-161">The form opens in the Form designer.</span></span>
4.  <span data-ttu-id="60f99-162">フォームのデータ ソースとして **FmtChargeType** テーブルを追加します。</span><span class="sxs-lookup"><span data-stu-id="60f99-162">Add the **FmtChargeType** table as the data source for the form.</span></span> <span data-ttu-id="60f99-163">**データ ソース** を右クリックし、**新しいデータ ソース** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="60f99-163">Right-click **Data Sources,** and then click **New Data Source**.</span></span> <span data-ttu-id="60f99-164">データ ソース ノードが追加されます。</span><span class="sxs-lookup"><span data-stu-id="60f99-164">A data source node is added.</span></span>
5.  <span data-ttu-id="60f99-165">前の手順でデータ ソース ノードをクリックします。</span><span class="sxs-lookup"><span data-stu-id="60f99-165">Click the data source node from the previous step.</span></span> <span data-ttu-id="60f99-166">**プロパティ** ウィンドウで、次のプロパティに指定された値を設定します。</span><span class="sxs-lookup"><span data-stu-id="60f99-166">In the **Properties** window, populate the following properties with the specified values.</span></span>

    | <span data-ttu-id="60f99-167">**プロパティ**</span><span class="sxs-lookup"><span data-stu-id="60f99-167">**Property**</span></span> | <span data-ttu-id="60f99-168">**値**</span><span class="sxs-lookup"><span data-stu-id="60f99-168">**Value**</span></span>|
    |--------------|------|
    | <span data-ttu-id="60f99-169">テーブル</span><span class="sxs-lookup"><span data-stu-id="60f99-169">Table</span></span>        | <span data-ttu-id="60f99-170">FMTChargeType</span><span class="sxs-lookup"><span data-stu-id="60f99-170">FMTChargeType</span></span>|
    | <span data-ttu-id="60f99-171">氏名</span><span class="sxs-lookup"><span data-stu-id="60f99-171">Name</span></span>         | <span data-ttu-id="60f99-172">FMTChargeType *まず Table プロパティの値を指定してください。このプロパティは、同じ値を使用するよう自動的に更新されます。*</span><span class="sxs-lookup"><span data-stu-id="60f99-172">FMTChargeType *Be sure to specify the value for the Table property first. This property will automatically update to use that same value.*</span></span> |

    <span data-ttu-id="60f99-173">次の図は、**FMTChargeType** テーブルを追加した後の **データソース**を示しています。</span><span class="sxs-lookup"><span data-stu-id="60f99-173">The following illustration shows **Data Sources** after you add the **FMTChargeType** table.</span></span> 

    <span data-ttu-id="60f99-174">[![rentalcharge3](./media/rentalcharge3.png)](./media/rentalcharge3.png)</span><span class="sxs-lookup"><span data-stu-id="60f99-174">[![rentalcharge3](./media/rentalcharge3.png)](./media/rentalcharge3.png)</span></span>

6.  <span data-ttu-id="60f99-175">フォーム デザイナーで、**デザイン**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="60f99-175">In the Form designer, click **Design**.</span></span> <span data-ttu-id="60f99-176">**プロパティ** ウィンドウで、次のプロパティに指定された値を設定します。</span><span class="sxs-lookup"><span data-stu-id="60f99-176">In the **Properties** window, populate the following properties with the specified values.</span></span>

    | <span data-ttu-id="60f99-177">**プロパティ**</span><span class="sxs-lookup"><span data-stu-id="60f99-177">**Property**</span></span> | <span data-ttu-id="60f99-178">**値**</span><span class="sxs-lookup"><span data-stu-id="60f99-178">**Value**</span></span>                                                                    |
    |--------------|------------------------------------------------------------------------------|
    | <span data-ttu-id="60f99-179">キャプション</span><span class="sxs-lookup"><span data-stu-id="60f99-179">Caption</span></span>      | <span data-ttu-id="60f99-180">レンタル料金のタイプ *これは、フォームの上部に表示されるラベルです。*</span><span class="sxs-lookup"><span data-stu-id="60f99-180">Rental charge types *This is the label that appears at the top of the form.*</span></span> |
    | <span data-ttu-id="60f99-181">データ ソース</span><span class="sxs-lookup"><span data-stu-id="60f99-181">Data Source</span></span>  | <span data-ttu-id="60f99-182">FMTChargeType *フォームのデータ ソースを指定するには、このプロパティを使用します。*</span><span class="sxs-lookup"><span data-stu-id="60f99-182">FMTChargeType *Use this property to specify the data source for the form.*</span></span>   |

7.  <span data-ttu-id="60f99-183">フォーム デザイナーで、**デザイン** &gt; **グリッド**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="60f99-183">In the Form designer, click **Design** &gt; **Grid**.</span></span>
8.  <span data-ttu-id="60f99-184">FMTChargeType データ ソースを簡易リスト フォームで表示されているグリッドにバインドします。</span><span class="sxs-lookup"><span data-stu-id="60f99-184">Bind the FMTChargeType data source to the grid that appears in the simple list form.</span></span> <span data-ttu-id="60f99-185">**プロパティ** ウィンドウの**データ ソース**に、**FMTChargeType** を入力します。</span><span class="sxs-lookup"><span data-stu-id="60f99-185">In the **Properties** window, in **Data Source**, enter **FMTChargeType**.</span></span>
9.  <span data-ttu-id="60f99-186">グリッドにフィールドを追加する前に、データ ソースを指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="60f99-186">You have to specify the data source before you add fields to the grid.</span></span> <span data-ttu-id="60f99-187">次に、データ ソースからのフィールドを使用して、グリッドに列を追加することができます。</span><span class="sxs-lookup"><span data-stu-id="60f99-187">You can then use the fields from the data source to add columns to the grid.</span></span> <span data-ttu-id="60f99-188">グリッドにデータ ソースから 2 つのフォームを追加します。</span><span class="sxs-lookup"><span data-stu-id="60f99-188">Add two fields from the data source to the grid.</span></span> <span data-ttu-id="60f99-189">追加するフィールドは、簡易リスト フォームの列として表示されます。</span><span class="sxs-lookup"><span data-stu-id="60f99-189">The fields you add will appear as columns on the Simple List form.</span></span> <span data-ttu-id="60f99-190">左側のウィンドウで、FMTChargeType データ ソース**フィールド**ノードを展開します。</span><span class="sxs-lookup"><span data-stu-id="60f99-190">Expand the FMTChargeType data source **Fields** node in the left pane.</span></span> <span data-ttu-id="60f99-191">**Ctrl** を押し、次のフィールドをクリックします。</span><span class="sxs-lookup"><span data-stu-id="60f99-191">Press **Ctrl** and then click the following fields:</span></span>
    -   <span data-ttu-id="60f99-192">ChargeType</span><span class="sxs-lookup"><span data-stu-id="60f99-192">ChargeType</span></span>
    -   <span data-ttu-id="60f99-193">説明</span><span class="sxs-lookup"><span data-stu-id="60f99-193">Description</span></span>

10. <span data-ttu-id="60f99-194">選択したフィールドを右ウィンドウの**デザイン** &gt; **グリッド**にドラッグします。</span><span class="sxs-lookup"><span data-stu-id="60f99-194">Drag the selected fields to **Design** &gt; **Grid** in the right pane.</span></span> <span data-ttu-id="60f99-195">次の図は、グリッド ノードが展開され、2 つのフィールドが追加された後のグリッドを示しています。</span><span class="sxs-lookup"><span data-stu-id="60f99-195">The following illustration shows the grid after the grid node is expanded and the two fields are added.</span></span> 

    <span data-ttu-id="60f99-196">[![rentalcharge4](./media/rentalcharge4.png)](./media/rentalcharge4.png)</span><span class="sxs-lookup"><span data-stu-id="60f99-196">[![rentalcharge4](./media/rentalcharge4.png)](./media/rentalcharge4.png)</span></span>

11. <span data-ttu-id="60f99-197">フォーム デザイナーで、**デザイン &gt; CustomFilterGroup &gt; QuickFilter** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="60f99-197">In the Form designer, click **Design &gt; CustomFilterGroup &gt; QuickFilter**.</span></span>
12. <span data-ttu-id="60f99-198">**プロパティ** ウィンドウで、**TargetControl** をクリックしてから**グリッド**を選択して **QuickFilter** コントロールをフォームのグリッドにバインドします。</span><span class="sxs-lookup"><span data-stu-id="60f99-198">In the **Properties** window, click **TargetControl**, and then select **Grid** to bind the **QuickFilter** control to the grid on the form.</span></span>
13. <span data-ttu-id="60f99-199">**ファイル** &gt; **保存** **FmtChargeType** とクリックします。</span><span class="sxs-lookup"><span data-stu-id="60f99-199">Click **File** &gt; **Save** **FmtChargeType**.</span></span>

## <a name="view-the-form"></a><span data-ttu-id="60f99-200">フォームの表示</span><span class="sxs-lookup"><span data-stu-id="60f99-200">View the form</span></span>
<span data-ttu-id="60f99-201">Visual Studio を使用して、**FmtChargeType** フォームをビルドして実行します。</span><span class="sxs-lookup"><span data-stu-id="60f99-201">Use Visual Studio to build and run the **FmtChargeType** form.</span></span>

1.  <span data-ttu-id="60f99-202">**ソリューション エクスプローラー**で、**FmtChargeType** フォームを右クリックしてから、**スタートアップ オブジェクトとして設定**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="60f99-202">In **Solution Explorer**, right-click the **FmtChargeType** form, and then click **Set as Startup Object**.</span></span>
2.  <span data-ttu-id="60f99-203">Ctrl+F5 キーを押して、フォームをビルドおよび実行します。</span><span class="sxs-lookup"><span data-stu-id="60f99-203">Press Ctrl+F5 to build and run the form.</span></span>
3.  <span data-ttu-id="60f99-204">Internet Explorer でフォームが開きます。</span><span class="sxs-lookup"><span data-stu-id="60f99-204">The form opens in Internet Explorer.</span></span>
4.  <span data-ttu-id="60f99-205">レンタル料金タイプを追加するには、フォームの上部にあるアクション ペインで **新規** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="60f99-205">To add a rental charge type, click **New** in the Action Pane at the top of the form.</span></span> <span data-ttu-id="60f99-206">次の情報を追加します。</span><span class="sxs-lookup"><span data-stu-id="60f99-206">Add the following information.</span></span>

    | <span data-ttu-id="60f99-207">**レンタル料金のタイプ**</span><span class="sxs-lookup"><span data-stu-id="60f99-207">**Rental Charge Type**</span></span> | <span data-ttu-id="60f99-208">**説明**</span><span class="sxs-lookup"><span data-stu-id="60f99-208">**Description**</span></span> |
    |------------------------|-----------------|
    | <span data-ttu-id="60f99-209">クリーニング</span><span class="sxs-lookup"><span data-stu-id="60f99-209">cleaning</span></span>               | <span data-ttu-id="60f99-210">クリーニング代</span><span class="sxs-lookup"><span data-stu-id="60f99-210">Cleaning fee</span></span>    |

5.  <span data-ttu-id="60f99-211">アクション ウィンドウで、**保存**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="60f99-211">In the Action Pane, click **Save**.</span></span>
6.  <span data-ttu-id="60f99-212">ブラウザーを更新して、一覧に新しいレコードを表示します。</span><span class="sxs-lookup"><span data-stu-id="60f99-212">Refresh the browser to see the new record in the list.</span></span> <span data-ttu-id="60f99-213">次の図は、フォームの外観を示しています。</span><span class="sxs-lookup"><span data-stu-id="60f99-213">The following illustration shows how the form should look.</span></span>

    <span data-ttu-id="60f99-214">[![rentalcharge5](./media/rentalcharge5.png)](./media/rentalcharge5.png)</span><span class="sxs-lookup"><span data-stu-id="60f99-214">[![rentalcharge5](./media/rentalcharge5.png)](./media/rentalcharge5.png)</span></span>

7.  <span data-ttu-id="60f99-215">表示モードでフォームを開きます。</span><span class="sxs-lookup"><span data-stu-id="60f99-215">The form opens in view mode.</span></span> <span data-ttu-id="60f99-216">アクション ウィンドウの**編集**をクリックして、フォームを編集モードに切り替えます。</span><span class="sxs-lookup"><span data-stu-id="60f99-216">Click **Edit** in the Action Pane to switch the form into edit mode.</span></span> <span data-ttu-id="60f99-217">表示モードに戻るには、**オプション** をクリックしてから **読み取りモード** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="60f99-217">To return to view mode, click **Options** and then **Read mode**.</span></span>




