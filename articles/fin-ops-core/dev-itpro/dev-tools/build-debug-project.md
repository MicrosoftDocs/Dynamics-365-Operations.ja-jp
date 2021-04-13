---
title: プロジェクトのビルドおよびデバッグ
description: このチュートリアルでは、フリート管理アプリを使用して、ブレークポイントの設定方法、コードの変更方法、および結果の構築方法を示します。
author: pvillads
ms.date: 02/06/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.custom: 26731
ms.assetid: 5c2378fe-cb34-4a81-a940-57d4e13eb282
ms.search.region: Global
ms.author: pvillads
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 69dd2d360f8cb34817ef6c4dddff4d726fdd9199
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5750366"
---
# <a name="build-and-debug-projects"></a><span data-ttu-id="ef790-103">プロジェクトのビルドおよびデバッグ</span><span class="sxs-lookup"><span data-stu-id="ef790-103">Build and debug projects</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ef790-104">このチュートリアルでは、フリート管理アプリケーションでコードを分析してデバッグするために Visual Studio でのツールの使用について確認します。</span><span class="sxs-lookup"><span data-stu-id="ef790-104">In this tutorial, you’ll learn about using the tools in Visual Studio to analyze and debug code in the Fleet Management application.</span></span> <span data-ttu-id="ef790-105">ブレークポイントを設定し、あるコードを変更し、その結果を構築する、単純な開発者のシナリオを検討します。</span><span class="sxs-lookup"><span data-stu-id="ef790-105">You’ll go through a simple developer scenario in which you will set breakpoints, modify some code, and build the result.</span></span> 

## <a name="prerequisites"></a><span data-ttu-id="ef790-106">必要条件</span><span class="sxs-lookup"><span data-stu-id="ef790-106">Prerequisites</span></span>

<span data-ttu-id="ef790-107">コードおよび Visual Studio の以前の経験は、このチュートリアルを完全に活用するのに役立ちます。</span><span class="sxs-lookup"><span data-stu-id="ef790-107">Previous experience with code and Visual Studio is helpful to get the full benefit of this tutorial.</span></span> <span data-ttu-id="ef790-108">このチュートリアルでは、リモート デスクトップを使用して環境にアクセスし、インスタンスの管理者としてプロビジョニングする必要があります。</span><span class="sxs-lookup"><span data-stu-id="ef790-108">This tutorial requires you to access the environment using Remote Desktop and that you be provisioned as an administrator on the instance.</span></span>

## <a name="key-concepts"></a><span data-ttu-id="ef790-109">重要な概念</span><span class="sxs-lookup"><span data-stu-id="ef790-109">Key concepts</span></span>

-   <span data-ttu-id="ef790-110">Visual Studio のデバッガーは、プロジェクトのコードの分析とデバッグに使用されます。</span><span class="sxs-lookup"><span data-stu-id="ef790-110">The debugger in Visual Studio is used to analyze and debug code for your projects.</span></span>
-   <span data-ttu-id="ef790-111">Visual Studio デバッガーの標準機能は、実行中のアプリケーションを調べているときに使用することができます。</span><span class="sxs-lookup"><span data-stu-id="ef790-111">The standard features of the Visual Studio debugger are available to use when you're examining the running application.</span></span> <span data-ttu-id="ef790-112">これらの機能には、変数の値の変更、ブレークポイントの設定などが含まれます。</span><span class="sxs-lookup"><span data-stu-id="ef790-112">These features include modifying values of variables, setting breakpoints, and so on.</span></span>
-   <span data-ttu-id="ef790-113">IntelliSense および Visual Studio の他の機能は、効率的なコード編集および理解に不可欠です。</span><span class="sxs-lookup"><span data-stu-id="ef790-113">IntelliSense and other features of Visual Studio are vital to efficient code editing and comprehension.</span></span>
-   <span data-ttu-id="ef790-114">開発は反復的なプロセスです。</span><span class="sxs-lookup"><span data-stu-id="ef790-114">Development is an iterative process.</span></span> <span data-ttu-id="ef790-115">コードを変更すると、プロジェクトが作成され、変更をテストできます。</span><span class="sxs-lookup"><span data-stu-id="ef790-115">After making modifications to the code, the project will be built, and changes can be tested.</span></span>

## <a name="scenario"></a><span data-ttu-id="ef790-116">シナリオ</span><span class="sxs-lookup"><span data-stu-id="ef790-116">Scenario</span></span>

<span data-ttu-id="ef790-117">レンタル会社は、顧客が有効期限を過ぎているクレジット カードを使用して車を借りているときに、不幸な出来事に見舞われました。</span><span class="sxs-lookup"><span data-stu-id="ef790-117">The rental company has had unfortunate events when customers rent cars using credit cards that are past the expiration dates.</span></span> <span data-ttu-id="ef790-118">開発者は、この状況の阻止を支援するために、アプリケーションを修正する責任を負います。</span><span class="sxs-lookup"><span data-stu-id="ef790-118">You, the developer, are tasked with revising the application to help prevent this situation.</span></span> <span data-ttu-id="ef790-119">Visual Studio のデバッガーを使用して、問題を特定します。</span><span class="sxs-lookup"><span data-stu-id="ef790-119">You’ll identify the problem by using the debugger in Visual Studio.</span></span> <span data-ttu-id="ef790-120">問題識別された後は、修正を実装するためにいくつかのコードを編集します。</span><span class="sxs-lookup"><span data-stu-id="ef790-120">After the problem is identified, you’ll edit some code to implement a fix.</span></span> <span data-ttu-id="ef790-121">最後に、プロジェクトを構築し、修正プログラムが成功したことを検証します。</span><span class="sxs-lookup"><span data-stu-id="ef790-121">Finally, you’ll build the project and validate that the fix was successful.</span></span>

## <a name="run-to-a-breakpoint"></a><span data-ttu-id="ef790-122">ブレークポイントまで実行</span><span class="sxs-lookup"><span data-stu-id="ef790-122">Run to a breakpoint</span></span>

1.  <span data-ttu-id="ef790-123">デスクトップで、Visual Studio ショートカットをダブルクリックして、開発環境を開きます。</span><span class="sxs-lookup"><span data-stu-id="ef790-123">On the desktop, double-click the Visual Studio shortcut to open the development environment.</span></span>
2.  <span data-ttu-id="ef790-124">FleetManagement ソリューションを開きます。</span><span class="sxs-lookup"><span data-stu-id="ef790-124">Open the FleetManagement solution.</span></span> <span data-ttu-id="ef790-125">**ファイル** メニューで、**開く** をポイントし、**プロジェクト/ソリューション** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="ef790-125">On the **File** menu, point to **Open**, and then click **Project/Solution**.</span></span>
3.  <span data-ttu-id="ef790-126">デスクトップを参照し、次に **FleetManagement** フォルダーを開きます。</span><span class="sxs-lookup"><span data-stu-id="ef790-126">Browse to the desktop, and then open the **FleetManagement** folder.</span></span> <span data-ttu-id="ef790-127">ソリューション ファイルがコンピュータにない場合は、作成手順が「[チュートリアル: AOT のフリート管理モデルからフリート管理ソリューションを作成する](https://community.dynamics.com/ax/b/newdynamicsax/archive/2016/05/19/tutorial-create-a-fleet-management-solution-file-out-of-the-fleet-management-models-in-the-aot)」に記載されています。</span><span class="sxs-lookup"><span data-stu-id="ef790-127">If the solution file is not on your computer, the steps to create it are listed in [Tutorial: Create a Fleet Management solution file out of the Fleet Management models in the AOT](https://community.dynamics.com/ax/b/newdynamicsax/archive/2016/05/19/tutorial-create-a-fleet-management-solution-file-out-of-the-fleet-management-models-in-the-aot).</span></span>
4.  <span data-ttu-id="ef790-128">**FleetManagement** という名前のファイルを選択します。</span><span class="sxs-lookup"><span data-stu-id="ef790-128">Select the file named **FleetManagement**.</span></span> <span data-ttu-id="ef790-129">表示されるファイル タイプは SLN ファイルです。</span><span class="sxs-lookup"><span data-stu-id="ef790-129">The file type listed is SLN File.</span></span>
5.  <span data-ttu-id="ef790-130">**開く** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="ef790-130">Click **Open**.</span></span> <span data-ttu-id="ef790-131">ソリューションの読み込みには時間がかかる場合があります。</span><span class="sxs-lookup"><span data-stu-id="ef790-131">Loading the solution may take some time.</span></span>
6.  <span data-ttu-id="ef790-132">**FleetManagement** プロジェクトをスタートアップ プロジェクトにします。</span><span class="sxs-lookup"><span data-stu-id="ef790-132">Make the **FleetManagement** project the startup project.</span></span> <span data-ttu-id="ef790-133">**ソリューション エクスプローラー** で、**フリート管理** プロジェクトを右クリックして、コンテキスト メニューで **スタートアップ プロジェクトとして設定** を選択します。</span><span class="sxs-lookup"><span data-stu-id="ef790-133">In **Solution Explorer**, right-click the **Fleet Management** project, and choose **Set as StartUp Project** in the context menu.</span></span>
7.  <span data-ttu-id="ef790-134">**ソリューション エクスプローラー** で、**フリート管理** プロジェクトをダブルクリックして内容を表示します。</span><span class="sxs-lookup"><span data-stu-id="ef790-134">In **Solution Explorer**, double-click the **Fleet Management** project to display its content.</span></span>
8.  <span data-ttu-id="ef790-135">**Code** フォルダーをダブルクリックしてから、フリート管理プロジェクトの **Classes** フォルダーをダブルクリックします。</span><span class="sxs-lookup"><span data-stu-id="ef790-135">Double-click the **Code** folder, and then double click the **Classes** folder of the Fleet Management project.</span></span> <span data-ttu-id="ef790-136">**FMRentailCheckoutProcessor** クラスを検索します。</span><span class="sxs-lookup"><span data-stu-id="ef790-136">Locate the **FMRentailCheckoutProcessor** class.</span></span> <span data-ttu-id="ef790-137">このクラスを右クリックしてから、**開く** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="ef790-137">Right-click this class, and then click **Open**.</span></span> <span data-ttu-id="ef790-138">または、ソリューション エクスプローラー ウィンドウの上部にあるソリューション エクスプローラーの検索バーを使用できます。</span><span class="sxs-lookup"><span data-stu-id="ef790-138">Alternatively, you can use the solution explorer search bar at the top of the solution explorer window.</span></span> <span data-ttu-id="ef790-139">検索バーに名前を入力すると、ソリューション エクスプローラーで選択された対応するコンポーネントが表示されます。</span><span class="sxs-lookup"><span data-stu-id="ef790-139">As you enter the name in the search bar, you'll see the corresponding artifacts selected in the solution explorer.</span></span> <span data-ttu-id="ef790-140">クラスで X++ コードを表示できるようになりました。</span><span class="sxs-lookup"><span data-stu-id="ef790-140">You can now see the X++ code for the class.</span></span> <span data-ttu-id="ef790-141">このクラスには **FinalizeRentalCheckout** という名前のメソッドがあります。</span><span class="sxs-lookup"><span data-stu-id="ef790-141">This class has a method named **FinalizeRentalCheckout**.</span></span>
9.  <span data-ttu-id="ef790-142">最初のコメントの次の行にあるこのメソッドにブレークポイントを配置します。</span><span class="sxs-lookup"><span data-stu-id="ef790-142">Place a breakpoint in this method on the line following the first comment.</span></span> <span data-ttu-id="ef790-143">これを行うには、デバッガで実行を一時停止するコード行の左側の余白をクリックします。</span><span class="sxs-lookup"><span data-stu-id="ef790-143">To do this, click in the margin to the left of the line of code where you want the debugger to pause execution.</span></span> <span data-ttu-id="ef790-144">また、コード行の任意の場所をクリックして、F9 を押すことができます。</span><span class="sxs-lookup"><span data-stu-id="ef790-144">You can also click anywhere in the line of code, and then press F9.</span></span> <span data-ttu-id="ef790-145">次の図はブレークポイントを示しています。ブレークポイントは余白に赤で塗りつぶされた円として表示されます。</span><span class="sxs-lookup"><span data-stu-id="ef790-145">The following illustration shows a breakpoint, which is displayed as a red-filled circle in the margin.</span></span> 

    <span data-ttu-id="ef790-146">[![FMRentalCheckoutProcessorのブレークポイント](./media/redcirclemargin_builddebugproj.png)](./media/redcirclemargin_builddebugproj.png)</span><span class="sxs-lookup"><span data-stu-id="ef790-146">[![Breakpoint in FMRentalCheckoutProcessor](./media/redcirclemargin_builddebugproj.png)](./media/redcirclemargin_builddebugproj.png)</span></span> 

    <span data-ttu-id="ef790-147">FinalizeRentalCheckout メソッドは、レンタル トランザクションが保存されるときに呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="ef790-147">The FinalizeRentalCheckout method is called when a rental transaction is saved.</span></span> <span data-ttu-id="ef790-148">このメソッドは、RentalTransactionAboutTobeFinalizedEvent という名前のデリゲートを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="ef790-148">This method calls the delegate named RentalTransactionAboutTobeFinalizedEvent.</span></span> <span data-ttu-id="ef790-149">このデリゲートで呼び出される、イベント ハンドラー メソッドを実装することができます。</span><span class="sxs-lookup"><span data-stu-id="ef790-149">You can implement an event handler method, which is called by this delegate.</span></span> <span data-ttu-id="ef790-150">デリゲートを呼び出すメソッドは、RentalConfirmation という名前のパラメーターを渡します。このパラメーターには、レンタルを許可するかブロックするかを示す値が含まれています。</span><span class="sxs-lookup"><span data-stu-id="ef790-150">The method that calls the delegate passes a parameter, named RentalConfirmation, which contains a value that indicates whether the rental should be allowed or blocked.</span></span> <span data-ttu-id="ef790-151">レンタルが許可されている場合、値に true が含まれ、ブロックされている場合は、値に false が含まれます。</span><span class="sxs-lookup"><span data-stu-id="ef790-151">If the rental is allowed, the value contains "true"; if it's blocked, the value contains "false".</span></span> <span data-ttu-id="ef790-152">イベント ハンドラーは、開発者がコード内で実装するために選択するテストに基づいてこの値を変更できます。</span><span class="sxs-lookup"><span data-stu-id="ef790-152">An event handler can change this value, based on any test the developer chooses to implement in code.</span></span> <span data-ttu-id="ef790-153">この場合、クレジット カードの有効期限をテストするコードを変更します。</span><span class="sxs-lookup"><span data-stu-id="ef790-153">In this case, we'll modify the code to test the expiration date of the credit card.</span></span>
10. <span data-ttu-id="ef790-154">F5 を押してアプリケーションをデバッグのために起動するか、**デバッグ** メニューで **デバッグ開始** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="ef790-154">Press F5 to start the application for debugging, or, on the **Debug** menu, click **Start Debugging**.</span></span> <span data-ttu-id="ef790-155">これらの方法のいずれかでアプリケーションを開始することが重要です。</span><span class="sxs-lookup"><span data-stu-id="ef790-155">It's important that you start the application in one of these ways.</span></span> <span data-ttu-id="ef790-156">しない場合は、Visual Studio デバッガーは起動されないため、設定されたブレークポイントのいずれかはヒットされません。</span><span class="sxs-lookup"><span data-stu-id="ef790-156">If you don't, the Visual Studio debugger won't start, so you won't hit any of the breakpoints you've set.</span></span> <span data-ttu-id="ef790-157">**注記**: デバッガーは、コードの位置をソースの位置に関連付ける必要があります。</span><span class="sxs-lookup"><span data-stu-id="ef790-157">**Note**: The debugger needs to relate code position to source positions.</span></span> <span data-ttu-id="ef790-158">アセンブリおよび net モジュールに沿って生成された PDB ファイルの消費を通じて実行されます。</span><span class="sxs-lookup"><span data-stu-id="ef790-158">It does this through consuming PDB files produced alongside the assemblies and net modules.</span></span> <span data-ttu-id="ef790-159">デバッガーは、グローバル ツール設定の設定に示すように、PDBファイルから記号を読み込みます。</span><span class="sxs-lookup"><span data-stu-id="ef790-159">The debugger will load symbols from the PDB files as described in the settings in the global tools settings.</span></span> <span data-ttu-id="ef790-160">読み込むシンボルを制御する設定を含むオプション ページを開くには、**ツール** メニューで **オプション** を選択します。</span><span class="sxs-lookup"><span data-stu-id="ef790-160">To open the options page containing the setting that controls which symbols load, go to the **Tools** menu and choose **Options**.</span></span> <span data-ttu-id="ef790-161">**Microsoft Dynamics 365 for Finance and Operations** グループで、**デバッグ** ページを選択します。</span><span class="sxs-lookup"><span data-stu-id="ef790-161">In the **Microsoft Dynamics 365 for Finance and Operations** group, select the **Debugging** page.</span></span> <span data-ttu-id="ef790-162">このオプションが選択されている場合、システムは、現在のソリューションのコンポーネントに関連する PDB ファイルのみから記号を読み込みます。</span><span class="sxs-lookup"><span data-stu-id="ef790-162">If this option is selected, the system will load symbols from only the PDB files related to the artifacts in the current solution.</span></span> <span data-ttu-id="ef790-163">これにより起動時間が大幅に短縮されるため、このラボでは必ずそれを選択してください。</span><span class="sxs-lookup"><span data-stu-id="ef790-163">This reduces the startup time significantly, so be sure it’s selected for this lab.</span></span> <span data-ttu-id="ef790-164">このオプションを選択すると、現在のソリューションの外部にあるエンティティからソース コードを確認することはできません。</span><span class="sxs-lookup"><span data-stu-id="ef790-164">Be aware that when this option is selected, it won’t be possible to see source code from entities outside of the current solution.</span></span> <span data-ttu-id="ef790-165">数分後、ブラウザーが起動し、プロジェクトで選択されたスタートアップ オブジェクトを表示します。</span><span class="sxs-lookup"><span data-stu-id="ef790-165">After a few moments, the browser will start and display the startup object that was selected in the project.</span></span>
11. <span data-ttu-id="ef790-166">**現在のレンタル** ページが開きます。</span><span class="sxs-lookup"><span data-stu-id="ef790-166">The **Current Rentals** page will open.</span></span>
    1.  <span data-ttu-id="ef790-167">アクション ウィンドウで、**編集** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="ef790-167">In the Action Pane, click **Edit**.</span></span>
    2.  <span data-ttu-id="ef790-168">ページが表示されたら、**表示/非表示** リストで **リストの表示** をクリックします (または **Ctrl+F8** を押します)。</span><span class="sxs-lookup"><span data-stu-id="ef790-168">When the page is displayed, click **Show list** in the **Show/Hide** list (or press **Ctrl+F8**).</span></span>

12. <span data-ttu-id="ef790-169">既存のレンタルに変更を加えます。</span><span class="sxs-lookup"><span data-stu-id="ef790-169">Make a change to any existing rental.</span></span> <span data-ttu-id="ef790-170">たとえば、**編集** をクリックして、レンタル期間が開始した時刻を変更します。</span><span class="sxs-lookup"><span data-stu-id="ef790-170">For example, click **Edit**, and change the time that the rental period started.</span></span>
13. <span data-ttu-id="ef790-171">レンタル レコードを強制的に検証するには、**保存** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="ef790-171">Click **Save** to force a validation of the rental record.</span></span> <span data-ttu-id="ef790-172">ブレークポイントを配置するメソッドが呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="ef790-172">The method in which you placed a breakpoint is called.</span></span> <span data-ttu-id="ef790-173">実行は、ブレークポイントを含むコード行で一時停止します。</span><span class="sxs-lookup"><span data-stu-id="ef790-173">Execution pauses at the line of code that contains the breakpoint.</span></span> 

    <span data-ttu-id="ef790-174">[![ブレークポイントでの実行の一時停止](./media/forcevalidation_builddebugproj.png)](./media/forcevalidation_builddebugproj.png)</span><span class="sxs-lookup"><span data-stu-id="ef790-174">[![Execution paused at breakpoint](./media/forcevalidation_builddebugproj.png)](./media/forcevalidation_builddebugproj.png)</span></span> 
    
    <span data-ttu-id="ef790-175">アプリケーションがブレークポイントで一時停止している間に、アプリケーションの状態を調べることができます。</span><span class="sxs-lookup"><span data-stu-id="ef790-175">While the application is paused at a breakpoint, you can examine the application state.</span></span> <span data-ttu-id="ef790-176">通常 Visual Studio で開発するアプリケーションと同じ方法を使用します。</span><span class="sxs-lookup"><span data-stu-id="ef790-176">Use the same techniques that you typically would for any application developed with Visual Studio.</span></span> <span data-ttu-id="ef790-177">たとえば、ツールヒントでその値を表示する変数またはパラメーターにカーソルを置きます。</span><span class="sxs-lookup"><span data-stu-id="ef790-177">For example, place the cursor over a variable or a parameter to see its value in a tooltip.</span></span> 
    
    <span data-ttu-id="ef790-178">[![一時停止中のブレークポイントのヒント](./media/tooltip_builddebugproj.png)](./media/tooltip_builddebugproj.png)</span><span class="sxs-lookup"><span data-stu-id="ef790-178">[![Tooltip for breakpoint while paused](./media/tooltip_builddebugproj.png)](./media/tooltip_builddebugproj.png)</span></span>

14. <span data-ttu-id="ef790-179">Visual Studio の他のデバッグ ツールも利用することができます。</span><span class="sxs-lookup"><span data-stu-id="ef790-179">The other debugging tools in Visual Studio are available as well.</span></span> <span data-ttu-id="ef790-180">たとえば、**ローカル** ウィンドウは、実行が停止した場所のすべてのローカル変数を表示します。</span><span class="sxs-lookup"><span data-stu-id="ef790-180">For example, the **Locals** window shows all of the local variables for the location where execution has stopped.</span></span> <span data-ttu-id="ef790-181">Visual Studio の下部にある **ローカル** タブをクリックし、**fmrentalrecord** 変数を展開します。</span><span class="sxs-lookup"><span data-stu-id="ef790-181">Click the **Locals** tab at the bottom of Visual Studio, and expand the **fmrentalrecord** variable.</span></span> <span data-ttu-id="ef790-182">レコード内のすべてのフィールドの値を示す、レコードの内部状態が表示されます。</span><span class="sxs-lookup"><span data-stu-id="ef790-182">You will see the internal state of the record, showing the values of all the fields in the record.</span></span> 

    <span data-ttu-id="ef790-183">[![ローカル ウィンドウ](./media/internalstate_builddebugproj.png)](./media/internalstate_builddebugproj.png)</span><span class="sxs-lookup"><span data-stu-id="ef790-183">[![Locals window](./media/internalstate_builddebugproj.png)](./media/internalstate_builddebugproj.png)</span></span> 
    
    <span data-ttu-id="ef790-184">**fmrentalrecord** 変数の **車両** プロパティの値に注目してください。</span><span class="sxs-lookup"><span data-stu-id="ef790-184">Notice the value of the **Vehicle** property of the **fmrentalrecord** variable.</span></span> <span data-ttu-id="ef790-185">このプロパティは、**FMRental** テーブルの外部キー フィールドです。</span><span class="sxs-lookup"><span data-stu-id="ef790-185">This property is a foreign key field in the **FMRental** table.</span></span> <span data-ttu-id="ef790-186">デバッガーを使用すると、FMVehicle テーブルの関連するレコードを調べることができます。</span><span class="sxs-lookup"><span data-stu-id="ef790-186">The debugger allows us to peek into the related record in the FMVehicle table.</span></span> <span data-ttu-id="ef790-187">**AutoIdentification** フィールド グループに属する値を示します。</span><span class="sxs-lookup"><span data-stu-id="ef790-187">It shows values that belong to the **AutoIdentification** field group.</span></span>
15. <span data-ttu-id="ef790-188">**ブレークポイント** ウィンドウには、設定されているすべてのブレークポイントが一覧表示されます。</span><span class="sxs-lookup"><span data-stu-id="ef790-188">The **Breakpoints** window lists all of the breakpoints that have been set.</span></span> <span data-ttu-id="ef790-189">**ブレークポイント** タブをクリックし、コンテンツを表示します。</span><span class="sxs-lookup"><span data-stu-id="ef790-189">Click the **Breakpoints** tab to see its content.</span></span> 

    <span data-ttu-id="ef790-190">[![ブレークポイント ウィンドウ](./media/breakpoint_builddebugproj.png)](./media/breakpoint_builddebugproj.png)</span><span class="sxs-lookup"><span data-stu-id="ef790-190">[![Breakpoints window](./media/breakpoint_builddebugproj.png)](./media/breakpoint_builddebugproj.png)</span></span>

16. <span data-ttu-id="ef790-191">F10 キーを数回押してコードを 1 行ずつ実行し、デバッガー機能の完全な補完を使用します。</span><span class="sxs-lookup"><span data-stu-id="ef790-191">Press F10 a few times to step through the code, line-by-line, and use the full complement of debugger features.</span></span> <span data-ttu-id="ef790-192">**ローカル** ウィンドウが、実行される各ステートメントですぐに変数の値を更新することに注意します。</span><span class="sxs-lookup"><span data-stu-id="ef790-192">Notice that the **Locals** window updates the values of variables immediately with each statement that's executed.</span></span>
17. <span data-ttu-id="ef790-193">ツール バーで、**続行** をクリックするか、F5 を押します。</span><span class="sxs-lookup"><span data-stu-id="ef790-193">On the toolbar, click **Continue**, or press F5</span></span>
18. <span data-ttu-id="ef790-194">Internet Explorer を閉じ、**Fleet Management** アプリケーションを閉じます。</span><span class="sxs-lookup"><span data-stu-id="ef790-194">Close Internet Explorer to close the **Fleet Management** application.</span></span> <span data-ttu-id="ef790-195">Visual Studio はデバッグ モードを終了します。</span><span class="sxs-lookup"><span data-stu-id="ef790-195">Visual Studio will exit the debugging mode.</span></span> <span data-ttu-id="ef790-196">代替は **デバッグの停止** を **デバッグ** メニューから選択します。</span><span class="sxs-lookup"><span data-stu-id="ef790-196">An alternative is to choose **Stop Debugging** from the **Debug** menu.</span></span> <span data-ttu-id="ef790-197">これにより、Internet Explorer は開いたままになり、次のデバッグ セッションをより早く開始することができます。</span><span class="sxs-lookup"><span data-stu-id="ef790-197">This will leave Internet Explorer open, allowing the next debugging session to start faster.</span></span>

## <a name="add-the-validation-code"></a><span data-ttu-id="ef790-198">検証コードの追加</span><span class="sxs-lookup"><span data-stu-id="ef790-198">Add the validation code</span></span>

<span data-ttu-id="ef790-199">**FinalizeRentalCheckout** メソッドでは、開発者がコードを追加してレンタルの有効性を決定するために使用されるデリゲートを呼び出したことを確認します。</span><span class="sxs-lookup"><span data-stu-id="ef790-199">In the **FinalizeRentalCheckout** method, you saw that the developer added code to call the delegate that’s used to determine the validity of the rental.</span></span> <span data-ttu-id="ef790-200">期限切れのクレジット カードの問題を解決するには、クレジット カードが期限切れではないことを確認するために使用するイベント ハンドラーを追加します。</span><span class="sxs-lookup"><span data-stu-id="ef790-200">To solve the problem of expired credit cards, you’ll add an event handler, which you’ll use to verify that the credit card isn’t expired.</span></span> <span data-ttu-id="ef790-201">ラボを簡素化するために、ハンドラはデリゲートを含む同じファイルに追加されます。</span><span class="sxs-lookup"><span data-stu-id="ef790-201">To simplify the lab, the handler will be added in the same file that contains the delegate.</span></span> <span data-ttu-id="ef790-202">インスピレーションとして、次のコードを使用します。</span><span class="sxs-lookup"><span data-stu-id="ef790-202">Use the following code as inspiration.</span></span> <span data-ttu-id="ef790-203">コードをコピーして貼り付けるのではなく、手動で入力して IntelliSense 機能の動作を参照してください。</span><span class="sxs-lookup"><span data-stu-id="ef790-203">Rather than copying and pasting the code, type it in manually to see the IntelliSense features in action.</span></span> <span data-ttu-id="ef790-204">これらの機能により、Visual Studio ユーザーは高い生産性を期待することができます。</span><span class="sxs-lookup"><span data-stu-id="ef790-204">These features add to the high level of productivity that Visual Studio users expect.</span></span>

```xpp
[SubscribesTo(classstr(FMRentalCheckoutProcessor), 
    delegatestr(FMRentalCheckoutProcessor, RentalTransactionAboutTobeFinalizedEvent))]
public static void RentalFinalizedEventHandler(FMRental rentalrecord, Struct rentalConfirmation)
{
    FMPaymentInformation paymentInfo;
    date ccExpiryDate, lastDayOfExpiryMonth;
    str s;

    select firstonly * from paymentInfo where paymentinfo.RecId == rentalRecord.PaymentInformationId;

    if (paymentInfo)
    {
        // Check if the payment info is valid
        // For now, we will check if the credit card is expired
        // Credit cards expire on the last day of the month indicated
        ccExpiryDate = mkdate(1, str2int(paymentInfo.ExpirationMonth), paymentInfo.ExpirationYear);
        lastDayOfExpiryMonth = endmth(ccExpiryDate);

        if (lastDayOfExpiryMonth < today())
        {
            rentalConfirmation.value('OktoRent', false);
            s = "Credit card validation failed for rental ";
        }
        else
        {
            s = "Credit card validation succeeded for rental ";
        }

        info (s + rentalrecord.RentalId);
    }
    else
    {
        rentalConfirmation.value('OktoRent', false);
        info ("No Credit card available for " + rentalrecord.RentalId);
    }
}
```

<span data-ttu-id="ef790-205">上記のコードはわかりやすいです。</span><span class="sxs-lookup"><span data-stu-id="ef790-205">The preceding code is straightforward.</span></span> <span data-ttu-id="ef790-206">このメソッドは、**SubscribesTo** 属性を使用して、関連するデリゲートのハンドラーとしてマークされています (図参照)</span><span class="sxs-lookup"><span data-stu-id="ef790-206">The method is marked as handler for the relevant delegate by using the **SubscribesTo** attribute, as shown.</span></span> <span data-ttu-id="ef790-207">コードでは、顧客レコードが取得されてから、クレジット カードの日付が今日の日付と比較されます。</span><span class="sxs-lookup"><span data-stu-id="ef790-207">In the code, the customer record is retrieved, and then the credit card date is compared to today's date.</span></span> <span data-ttu-id="ef790-208">クレジット カードの有効期限が過ぎている場合は、**RentalConfirmation** 構造でイベント ハンドラーの値を設定し、顧客が車両の貸し出しの対象ではないことを通知します。</span><span class="sxs-lookup"><span data-stu-id="ef790-208">If the expiration date of the credit card is in the past, the event handler sets a value in the **RentalConfirmation** structure to signal that the customer isn't eligible to rent a vehicle.</span></span> <span data-ttu-id="ef790-209">これは、任意の数のハンドラーがデリゲートにサブスクライブできるようにするためです。</span><span class="sxs-lookup"><span data-stu-id="ef790-209">The idea is that any number of handlers can subscribe to the delegate.</span></span> <span data-ttu-id="ef790-210">ハンドラーでレンタルを続行しないと決定した場合、**OkToRent** フラグを設定します。</span><span class="sxs-lookup"><span data-stu-id="ef790-210">If any handler determines that a rental should not proceed, it sets the **OkToRent** flag to false.</span></span> <span data-ttu-id="ef790-211">優れた実装では、**OkToRent** フラグがすでに false に設定されていると判断した場合、分析を行わないことがあります。</span><span class="sxs-lookup"><span data-stu-id="ef790-211">A superior implementation might refrain from doing any analysis if it determines that the **OkToRent** flag has already been set to false.</span></span>

1.  <span data-ttu-id="ef790-212">FMRentalCheckoutProcessor.xpp ファイルで作業していることを確認します。</span><span class="sxs-lookup"><span data-stu-id="ef790-212">Be sure that you're working in the FMRentalCheckoutProcessor.xpp file.</span></span> <span data-ttu-id="ef790-213">新しいイベント ハンドラー定義を FMRentalCheckoutProcessor クラスに追加することによって開始します。</span><span class="sxs-lookup"><span data-stu-id="ef790-213">Begin by adding the new event handler definition to the FMRentalCheckoutProcessor class.</span></span> <span data-ttu-id="ef790-214">クラス定義の終了を示す波括弧 (}) のすぐ上の空の明細行に次のコードを追加します。</span><span class="sxs-lookup"><span data-stu-id="ef790-214">Add the following code on an empty line just above the brace (}) that marks the end of the class definition.</span></span>

    ```xpp
    public static void RentalFinalizedEventHandler(FMRental rentalrecord, Struct rentalConfirmation)
    {

    }
    ```

2.  <span data-ttu-id="ef790-215">イベント ハンドラーの先頭に、属性を追加します。</span><span class="sxs-lookup"><span data-stu-id="ef790-215">Add the attributes to the beginning of the event handler.</span></span> <span data-ttu-id="ef790-216">これらの属性は、イベントハンドラーがどのデリゲートに加入しているかを示します。</span><span class="sxs-lookup"><span data-stu-id="ef790-216">These attributes indicate which delegate the event handler is subscribing to.</span></span>

    ```xpp
        [SubscribesTo(classstr(FMRentalCheckoutProcessor),
            delegatestr(FMRentalCheckoutProcessor, RentalTransactionAboutTobeFinalizedEvent))]
            public static void RentalFinalizedEventHandler(FMRental rentalrecord, Struct 
                                                                           RentalConfirmation)
        {

        }
    ```

3.  <span data-ttu-id="ef790-217">ここで、クレジット カードの有効期限の値を確認するコードを追加します。</span><span class="sxs-lookup"><span data-stu-id="ef790-217">Now, add the code that checks the credit card expiration value.</span></span> <span data-ttu-id="ef790-218">完了したメソッドは、次のコードのようになります。</span><span class="sxs-lookup"><span data-stu-id="ef790-218">The completed method should look similar to the following code.</span></span>

    ```xpp
    [SubscribesTo(classstr(FMRentalCheckoutProcessor), 
        delegatestr(FMRentalCheckoutProcessor, RentalTransactionAboutTobeFinalizedEvent))]
    public static void RentalFinalizedEventHandler(FMRental rentalrecord, Struct rentalConfirmation)
    {
        FMPaymentInformation paymentInfo;
        date ccExpiryDate, lastDayOfExpiryMonth;
        str s;

        select firstonly * from PaymentInfo where paymentinfo.RecId == rentalRecord.PaymentInformationId;

        if (paymentInfo)
        {
            // Check if the payment info is valid
            // For now we will check if the credit card is expired
            // Credit cards expire on the last day of the month indicated
            ccExpiryDate = mkdate(1, str2int(paymentInfo.ExpirationMonth), paymentInfo.ExpirationYear);
            lastDayOfExpiryMonth = endmth(ccExpiryDate);

            if (lastDayOfExpiryMonth < today())
            {
                rentalConfirmation.value('OktoRent', false);
                s = "Credit card validation failed for rental ";
            }
            else
            {
                s = "Credit card validation succeeded for rental ";
            }

            info (s + rentalrecord.RentalId);
        }
        else
        {
            rentalConfirmation.value('OktoRent', false);
            info ("No Credit card available for " + rentalrecord.RentalId);
        }
    }
    ```

4.  <span data-ttu-id="ef790-219">ハンドラーとデリゲートが 1 行の空白行で区切られていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="ef790-219">Make sure the handler and the delegate are separated by exactly one blank line.</span></span>
5.  <span data-ttu-id="ef790-220">Visual Studio のツールバーで、**保存** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="ef790-220">On the toolbar in Visual Studio, click **Save**.</span></span>
6.  <span data-ttu-id="ef790-221">コードに問題がなければ、フリート管理プロジェクトのコードをビルドします。</span><span class="sxs-lookup"><span data-stu-id="ef790-221">After you're satisfied with the code, build the code for the Fleet Management project.</span></span> <span data-ttu-id="ef790-222">これを行うには、**ソリューション エクスプローラー** で、**FleetManagement** プロジェクト名を右クリックし、**Build** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="ef790-222">To do this, in **Solution Explorer**, right-click the **FleetManagement** project name, and then click **Build**.</span></span> <span data-ttu-id="ef790-223">コードが正しくない場合は、エラーまたは警告が表示される場合があります。</span><span class="sxs-lookup"><span data-stu-id="ef790-223">You may see errors or warnings if the code isn't correct.</span></span> <span data-ttu-id="ef790-224">その場合は、コードを修正し、再度ビルド警告やエラーが解決されるまでビルドを続行します。</span><span class="sxs-lookup"><span data-stu-id="ef790-224">If so, correct the code, and build again until all warnings and errors have been resolved.</span></span> <span data-ttu-id="ef790-225">これで、リビジョンが意図したとおりに動作することを確認する準備が整いました。</span><span class="sxs-lookup"><span data-stu-id="ef790-225">You're now ready to validate that the revision works as intended.</span></span>
7.  <span data-ttu-id="ef790-226">**デバッグ** メニューをクリックして、**すべてのブレークポイントを削除** します。</span><span class="sxs-lookup"><span data-stu-id="ef790-226">On the **Debug** menu, click **Delete All Breakpoints**.</span></span>
8.  <span data-ttu-id="ef790-227">次のステートメントを含む明細行にあるイベント ハンドラー メソッドに新しいブレークポイントを配置します。</span><span class="sxs-lookup"><span data-stu-id="ef790-227">Place a new breakpoint in the event-handler method at the line that contains the following statement:</span></span>

    ```xpp
    if (lastDayOfExpiryMonth < today())
    ```
    
9.  <span data-ttu-id="ef790-228">F5 キーを押してデバッグをアクティブにし、フリート管理サンプルを開始します。</span><span class="sxs-lookup"><span data-stu-id="ef790-228">Start the Fleet Management sample with debugging active by pressing F5.</span></span>
10. <span data-ttu-id="ef790-229">前のセクションのステップ 11 で説明されているように **現在のレンタル** ページを参照してください。</span><span class="sxs-lookup"><span data-stu-id="ef790-229">Browse to the **Current rentals** page, as described starting in step 11 of the previous section.</span></span> <span data-ttu-id="ef790-230">いずれかの予約を選択し、**編集** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="ef790-230">Select one of the reservations, and click **Edit**.</span></span>
11. <span data-ttu-id="ef790-231">**顧客** ドロップダウン リストで、一覧から Adrian Lannin を選択して **保存** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="ef790-231">In the **Customer** drop-down list, select Adrian Lannin from the list, and then click **Save**.</span></span> <span data-ttu-id="ef790-232">実行は、イベントハンドラー メソッドで設定したブレークポイントで一時停止します。</span><span class="sxs-lookup"><span data-stu-id="ef790-232">Execution pauses at the breakpoint that you set in the event-handler method.</span></span>
12. <span data-ttu-id="ef790-233">F10 キーを 3 回押して、コード ブロックを実行します。</span><span class="sxs-lookup"><span data-stu-id="ef790-233">Press F10 three times to step through the code block.</span></span> 

    <span data-ttu-id="ef790-234">[![コードを進める](./media/stepcodeblock_builddebugproj.png)](./media/stepcodeblock_builddebugproj.png)</span><span class="sxs-lookup"><span data-stu-id="ef790-234">[![Stepping through code](./media/stepcodeblock_builddebugproj.png)](./media/stepcodeblock_builddebugproj.png)</span></span>
    
13. <span data-ttu-id="ef790-235">コール スタックのコード マップを表示するには、コード エディターを右クリックし、**コード マップにコール スタックを表示** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="ef790-235">To see the code map for the call stacks, right-click in the code editor, and then click **Show Call Stack on Code Map**.</span></span> <span data-ttu-id="ef790-236">呼び出し履歴にコメントを追加し、コードを進め、それに応じたコード マップの変更としてウォッチすることが必要な場合があります。</span><span class="sxs-lookup"><span data-stu-id="ef790-236">You may want to add a comment to the call stack, step through the code, and watch as the code map changes accordingly.</span></span>
14. <span data-ttu-id="ef790-237">F5 キーを押して続行します。</span><span class="sxs-lookup"><span data-stu-id="ef790-237">Press F5 to continue.</span></span> <span data-ttu-id="ef790-238">その顧客が許可されていないことが表示されます。</span><span class="sxs-lookup"><span data-stu-id="ef790-238">You'll see that the customer has been disallowed.</span></span>
15. <span data-ttu-id="ef790-239">同じレンタルで、顧客名を Phil Spencer に変更してから **更新** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="ef790-239">In the same rental, change the customer name to Phil Spencer, and then click **Update**.</span></span> <span data-ttu-id="ef790-240">今回は、トランザクションが可能です。</span><span class="sxs-lookup"><span data-stu-id="ef790-240">This time, the transaction is allowed.</span></span>
16. <span data-ttu-id="ef790-241">Internet Explorer を閉じます。</span><span class="sxs-lookup"><span data-stu-id="ef790-241">Close Internet Explorer.</span></span>
17. <span data-ttu-id="ef790-242">**RentalFinalizedEventHandler** メソッドで **SubscribesTo** をコメントにします。</span><span class="sxs-lookup"><span data-stu-id="ef790-242">Comment out the **SubscribesTo** attribute on the **RentalFinalizedEventHandler** method.</span></span> <span data-ttu-id="ef790-243">このステップでは、残りのチュートリアルで作業してもクレジット カード テストが実行されなくなります。</span><span class="sxs-lookup"><span data-stu-id="ef790-243">This step ensures that the credit card test will no longer run as you work on the remaining tutorials.</span></span>

## <a name="best-practices"></a><span data-ttu-id="ef790-244">ベスト プラクティス</span><span class="sxs-lookup"><span data-stu-id="ef790-244">Best practices</span></span>

<span data-ttu-id="ef790-245">このチュートリアルの前半では、プロジェクトにコードを追加し、変更を加えてソリューションをビルドする営業案件を得ました。</span><span class="sxs-lookup"><span data-stu-id="ef790-245">Earlier in this tutorial, you had the opportunity to add code to the project and build the solution with your changes.</span></span> <span data-ttu-id="ef790-246">ビルド プロセスが成功しなかったため、エラー ウィンドウを参照する必要があります。</span><span class="sxs-lookup"><span data-stu-id="ef790-246">The build process may not have been successful, requiring you to refer to the error window.</span></span> <span data-ttu-id="ef790-247">このウィンドウを使用しているとき、エラーを説明する明細行をクリックすると、エラー状態になります。</span><span class="sxs-lookup"><span data-stu-id="ef790-247">Using this window, you can get to the error by clicking on the line that describes the error.</span></span> <span data-ttu-id="ef790-248">コンパイル エラーを表していないいくつかの診断メッセージが通知される場合があります。</span><span class="sxs-lookup"><span data-stu-id="ef790-248">You may have noticed some diagnostic messages that don’t represent compilation errors.</span></span> <span data-ttu-id="ef790-249">これらは、**ベスト プラクティス** チェッカーからの診断です。</span><span class="sxs-lookup"><span data-stu-id="ef790-249">These are diagnostics from the **Best Practice** checker.</span></span> <span data-ttu-id="ef790-250">このツールは、開発者が既知のベスト プラクティスに違反したインスタンスをチェックして、違反が見つかったときに警告を表示します。</span><span class="sxs-lookup"><span data-stu-id="ef790-250">This tool will check for instances where the developer has violated a known best practice, and display a warning when one is found.</span></span> <span data-ttu-id="ef790-251">ベスト プラクティス ルールは、コードの構成要素とメタデータの両方に適用されます。</span><span class="sxs-lookup"><span data-stu-id="ef790-251">The Best Practice rules apply to both code constructs and metadata.</span></span> <span data-ttu-id="ef790-252">各ソフトウェアの開発組織は、実施するベスト プラクティスのセットを持つ可能性が高いです。</span><span class="sxs-lookup"><span data-stu-id="ef790-252">Each software development organization is likely to have its own set of best practices that they enforce.</span></span> <span data-ttu-id="ef790-253">既存のベスト プラクティス チェックの一部を無視する場合があります。</span><span class="sxs-lookup"><span data-stu-id="ef790-253">They may want to disregard some of the existing best practice checks.</span></span> <span data-ttu-id="ef790-254">これをサポートするために、報告されたベスト プラクティスの診断セットを個々の開発者が変更することができます。</span><span class="sxs-lookup"><span data-stu-id="ef790-254">To support this, the set of reported best practice diagnostics can be modified by the individual developer.</span></span> <span data-ttu-id="ef790-255">これを実証するには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="ef790-255">To demonstrate this, complete the following steps:</span></span>

1.  <span data-ttu-id="ef790-256">**表示** メニューで、**エラー リスト** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="ef790-256">On the **View** menu, click **Error List**.</span></span> <span data-ttu-id="ef790-257">いくつかのベスト プラクティス警告が表示されます。</span><span class="sxs-lookup"><span data-stu-id="ef790-257">You should see a small number of best practice warnings.</span></span>
2.  <span data-ttu-id="ef790-258">**Dynamics 365** メニューで、**オプション** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="ef790-258">On the **Dynamics 365** menu, click **Options**.</span></span> <span data-ttu-id="ef790-259">**Dynamics 365** グループで、**ベスト プラクティス** を選択します。</span><span class="sxs-lookup"><span data-stu-id="ef790-259">In the **Dynamics 365** group, choose **Best Practices**.</span></span>
3.  <span data-ttu-id="ef790-260">**モデル** ドロップダウン リストで、**フリート管理** モデルが選択されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="ef790-260">In the **Model** drop-down list, make sure that the **Fleet Management** model is selected.</span></span> <span data-ttu-id="ef790-261">ベスト プラクティス ルールは、特定のモデルに適用されます。</span><span class="sxs-lookup"><span data-stu-id="ef790-261">The best practice rules apply to a particular model.</span></span>
4.  <span data-ttu-id="ef790-262">ベスト プラクティス ルールのセットの一部に対する選択内容をマークします。</span><span class="sxs-lookup"><span data-stu-id="ef790-262">Mark the selections for some of the sets of Best Practice rules.</span></span> <span data-ttu-id="ef790-263">たとえば、**CodeStyleRules** のエントリを選択する場合、変数のベスト プラクティスのガイドラインが検査されます。</span><span class="sxs-lookup"><span data-stu-id="ef790-263">For example, if you select the entry for **CodeStyleRules**, best practice guidelines for variables will be examined.</span></span> <span data-ttu-id="ef790-264">選択を更新した後、**OK** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="ef790-264">After you've updated the selections, click **OK**.</span></span>
5.  <span data-ttu-id="ef790-265">プロジェクト名を右クリックして **リビルド** をクリックすることにより、フリート管理プロジェクトをリビルドします。</span><span class="sxs-lookup"><span data-stu-id="ef790-265">Rebuild the Fleet Management project by right-clicking the project name and then clicking **Rebuild**.</span></span> <span data-ttu-id="ef790-266">指定したベスト プラクティス ルールの違反が **エラー一覧** ウィンドウに表示されることがわかります。</span><span class="sxs-lookup"><span data-stu-id="ef790-266">You'll notice that the violations of the best practice rules that you specified appear in the **Error list** window.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]