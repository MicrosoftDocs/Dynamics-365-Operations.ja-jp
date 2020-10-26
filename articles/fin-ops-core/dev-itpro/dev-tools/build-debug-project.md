---
title: プロジェクトのビルドおよびデバッグ
description: このチュートリアルでは、フリート管理アプリケーションでコードを分析してデバッグするために Visual Studio でのツールの使用について確認します。 ブレークポイントを設定し、あるコードを変更し、その結果を構築する、単純な開発者のシナリオを検討します。
author: pvillads
manager: AnnBe
ms.date: 02/06/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.search.scope: Operations
ms.custom: 26731
ms.assetid: 5c2378fe-cb34-4a81-a940-57d4e13eb282
ms.search.region: Global
ms.author: pvillads
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 27e8bd1f4928a16b00127590de0169fbd9936ce0
ms.sourcegitcommit: 1edd3d4642f8fdc801b43b981b7c1a1c36ae0645
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/11/2020
ms.locfileid: "3796485"
---
# <a name="build-and-debug-projects"></a><span data-ttu-id="9a636-104">プロジェクトのビルドおよびデバッグ</span><span class="sxs-lookup"><span data-stu-id="9a636-104">Build and debug projects</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="9a636-105">このチュートリアルでは、フリート管理アプリケーションでコードを分析してデバッグするために Visual Studio でのツールの使用について確認します。</span><span class="sxs-lookup"><span data-stu-id="9a636-105">In this tutorial, you’ll learn about using the tools in Visual Studio to analyze and debug code in the Fleet Management application.</span></span> <span data-ttu-id="9a636-106">ブレークポイントを設定し、あるコードを変更し、その結果を構築する、単純な開発者のシナリオを検討します。</span><span class="sxs-lookup"><span data-stu-id="9a636-106">You’ll go through a simple developer scenario in which you will set breakpoints, modify some code, and build the result.</span></span> 

<a name="prerequisites"></a><span data-ttu-id="9a636-107">必要条件</span><span class="sxs-lookup"><span data-stu-id="9a636-107">Prerequisites</span></span>
-------------

<span data-ttu-id="9a636-108">コードおよび Visual Studio の以前の経験は、このチュートリアルを完全に活用するのに役立ちます。</span><span class="sxs-lookup"><span data-stu-id="9a636-108">Previous experience with code and Visual Studio is helpful to get the full benefit of this tutorial.</span></span> <span data-ttu-id="9a636-109">このチュートリアルでは、リモート デスクトップを使用して環境にアクセスし、インスタンスの管理者としてプロビジョニングする必要があります。</span><span class="sxs-lookup"><span data-stu-id="9a636-109">This tutorial requires you to access the environment using Remote Desktop and that you be provisioned as an administrator on the instance.</span></span>

## <a name="key-concepts"></a><span data-ttu-id="9a636-110">重要な概念</span><span class="sxs-lookup"><span data-stu-id="9a636-110">Key concepts</span></span>
-   <span data-ttu-id="9a636-111">Visual Studio のデバッガーは、プロジェクトのコードの分析とデバッグに使用されます。</span><span class="sxs-lookup"><span data-stu-id="9a636-111">The debugger in Visual Studio is used to analyze and debug code for your projects.</span></span>
-   <span data-ttu-id="9a636-112">Visual Studio デバッガーの標準機能は、実行中のアプリケーションを調べているときに使用することができます。</span><span class="sxs-lookup"><span data-stu-id="9a636-112">The standard features of the Visual Studio debugger are available to use when you're examining the running application.</span></span> <span data-ttu-id="9a636-113">これらの機能には、変数の値の変更、ブレークポイントの設定などが含まれます。</span><span class="sxs-lookup"><span data-stu-id="9a636-113">These features include modifying values of variables, setting breakpoints, and so on.</span></span>
-   <span data-ttu-id="9a636-114">IntelliSense および Visual Studio の他の機能は、効率的なコード編集および理解に不可欠です。</span><span class="sxs-lookup"><span data-stu-id="9a636-114">IntelliSense and other features of Visual Studio are vital to efficient code editing and comprehension.</span></span>
-   <span data-ttu-id="9a636-115">開発は反復的なプロセスです。</span><span class="sxs-lookup"><span data-stu-id="9a636-115">Development is an iterative process.</span></span> <span data-ttu-id="9a636-116">コードを変更すると、プロジェクトが作成され、変更をテストできます。</span><span class="sxs-lookup"><span data-stu-id="9a636-116">After making modifications to the code, the project will be built, and changes can be tested.</span></span>

## <a name="scenario"></a><span data-ttu-id="9a636-117">シナリオ</span><span class="sxs-lookup"><span data-stu-id="9a636-117">Scenario</span></span>
<span data-ttu-id="9a636-118">レンタル会社は、顧客が有効期限を過ぎているクレジット カードを使用して車を借りているときに、不幸な出来事に見舞われました。</span><span class="sxs-lookup"><span data-stu-id="9a636-118">The rental company has had unfortunate events when customers rent cars using credit cards that are past the expiration dates.</span></span> <span data-ttu-id="9a636-119">開発者は、この状況の阻止を支援するために、アプリケーションを修正する責任を負います。</span><span class="sxs-lookup"><span data-stu-id="9a636-119">You, the developer, are tasked with revising the application to help prevent this situation.</span></span> <span data-ttu-id="9a636-120">Visual Studio のデバッガーを使用して、問題を特定します。</span><span class="sxs-lookup"><span data-stu-id="9a636-120">You’ll identify the problem by using the debugger in Visual Studio.</span></span> <span data-ttu-id="9a636-121">問題識別された後は、修正を実装するためにいくつかのコードを編集します。</span><span class="sxs-lookup"><span data-stu-id="9a636-121">After the problem is identified, you’ll edit some code to implement a fix.</span></span> <span data-ttu-id="9a636-122">最後に、プロジェクトを構築し、修正プログラムが成功したことを検証します。</span><span class="sxs-lookup"><span data-stu-id="9a636-122">Finally, you’ll build the project and validate that the fix was successful.</span></span>

## <a name="run-to-a-breakpoint"></a><span data-ttu-id="9a636-123">ブレークポイントまで実行</span><span class="sxs-lookup"><span data-stu-id="9a636-123">Run to a breakpoint</span></span>
1.  <span data-ttu-id="9a636-124">デスクトップで、Visual Studio ショートカットをダブルクリックして、開発環境を開きます。</span><span class="sxs-lookup"><span data-stu-id="9a636-124">On the desktop, double-click the Visual Studio shortcut to open the development environment.</span></span>
2.  <span data-ttu-id="9a636-125">FleetManagement ソリューションを開きます。</span><span class="sxs-lookup"><span data-stu-id="9a636-125">Open the FleetManagement solution.</span></span> <span data-ttu-id="9a636-126">**ファイル**メニューで、**開く**をポイントし、**プロジェクト/ソリューション**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="9a636-126">On the **File** menu, point to **Open**, and then click **Project/Solution**.</span></span>
3.  <span data-ttu-id="9a636-127">デスクトップを参照し、次に **FleetManagement** フォルダーを開きます。</span><span class="sxs-lookup"><span data-stu-id="9a636-127">Browse to the desktop, and then open the **FleetManagement** folder.</span></span> <span data-ttu-id="9a636-128">ソリューション ファイルがコンピュータにない場合は、作成手順が「[チュートリアル: AOT のフリート管理モデルからフリート管理ソリューションを作成する](https://community.dynamics.com/ax/b/newdynamicsax/archive/2016/05/19/tutorial-create-a-fleet-management-solution-file-out-of-the-fleet-management-models-in-the-aot)」に記載されています。</span><span class="sxs-lookup"><span data-stu-id="9a636-128">If the solution file is not on your computer, the steps to create it are listed in [Tutorial: Create a Fleet Management solution file out of the Fleet Management models in the AOT](https://community.dynamics.com/ax/b/newdynamicsax/archive/2016/05/19/tutorial-create-a-fleet-management-solution-file-out-of-the-fleet-management-models-in-the-aot).</span></span>
4.  <span data-ttu-id="9a636-129">**FleetManagement** という名前のファイルを選択します。</span><span class="sxs-lookup"><span data-stu-id="9a636-129">Select the file named **FleetManagement**.</span></span> <span data-ttu-id="9a636-130">表示されるファイル タイプは SLN ファイルです。</span><span class="sxs-lookup"><span data-stu-id="9a636-130">The file type listed is SLN File.</span></span>
5.  <span data-ttu-id="9a636-131">**開く** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="9a636-131">Click **Open**.</span></span> <span data-ttu-id="9a636-132">ソリューションの読み込みには時間がかかる場合があります。</span><span class="sxs-lookup"><span data-stu-id="9a636-132">Loading the solution may take some time.</span></span>
6.  <span data-ttu-id="9a636-133">**FleetManagement** プロジェクトをスタートアップ プロジェクトにします。</span><span class="sxs-lookup"><span data-stu-id="9a636-133">Make the **FleetManagement** project the startup project.</span></span> <span data-ttu-id="9a636-134">**ソリューション エクスプローラー** で、**フリート管理** プロジェクトを右クリックして、コンテキスト メニューで **スタートアップ プロジェクトとして設定** を選択します。</span><span class="sxs-lookup"><span data-stu-id="9a636-134">In **Solution Explorer**, right-click the **Fleet Management** project, and choose **Set as StartUp Project** in the context menu.</span></span>
7.  <span data-ttu-id="9a636-135">**ソリューション エクスプローラー** で、**フリート管理** プロジェクトをダブルクリックして内容を表示します。</span><span class="sxs-lookup"><span data-stu-id="9a636-135">In **Solution Explorer**, double-click the **Fleet Management** project to display its content.</span></span>
8.  <span data-ttu-id="9a636-136">**Code** フォルダーをダブルクリックしてから、フリート管理プロジェクトの **Classes** フォルダーをダブルクリックします。</span><span class="sxs-lookup"><span data-stu-id="9a636-136">Double-click the **Code** folder, and then double click the **Classes** folder of the Fleet Management project.</span></span> <span data-ttu-id="9a636-137">**FMRentailCheckoutProcessor** クラスを検索します。</span><span class="sxs-lookup"><span data-stu-id="9a636-137">Locate the **FMRentailCheckoutProcessor** class.</span></span> <span data-ttu-id="9a636-138">このクラスを右クリックしてから、**開く** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="9a636-138">Right-click this class, and then click **Open**.</span></span> <span data-ttu-id="9a636-139">または、ソリューション エクスプローラー ウィンドウの上部にあるソリューション エクスプローラーの検索バーを使用できます。</span><span class="sxs-lookup"><span data-stu-id="9a636-139">Alternatively, you can use the solution explorer search bar at the top of the solution explorer window.</span></span> <span data-ttu-id="9a636-140">検索バーに名前を入力すると、ソリューション エクスプローラーで選択された対応するコンポーネントが表示されます。</span><span class="sxs-lookup"><span data-stu-id="9a636-140">As you enter the name in the search bar, you'll see the corresponding artifacts selected in the solution explorer.</span></span> <span data-ttu-id="9a636-141">クラスで X++ コードを表示できるようになりました。</span><span class="sxs-lookup"><span data-stu-id="9a636-141">You can now see the X++ code for the class.</span></span> <span data-ttu-id="9a636-142">このクラスには **FinalizeRentalCheckout** という名前のメソッドがあります。</span><span class="sxs-lookup"><span data-stu-id="9a636-142">This class has a method named **FinalizeRentalCheckout**.</span></span>
9.  <span data-ttu-id="9a636-143">最初のコメントの次の行にあるこのメソッドにブレークポイントを配置します。</span><span class="sxs-lookup"><span data-stu-id="9a636-143">Place a breakpoint in this method on the line following the first comment.</span></span> <span data-ttu-id="9a636-144">これを行うには、デバッガで実行を一時停止するコード行の左側の余白をクリックします。</span><span class="sxs-lookup"><span data-stu-id="9a636-144">To do this, click in the margin to the left of the line of code where you want the debugger to pause execution.</span></span> <span data-ttu-id="9a636-145">また、コード行の任意の場所をクリックして、F9 を押すことができます。</span><span class="sxs-lookup"><span data-stu-id="9a636-145">You can also click anywhere in the line of code, and then press F9.</span></span> <span data-ttu-id="9a636-146">次の図はブレークポイントを示しています。ブレークポイントは余白に赤で塗りつぶされた円として表示されます。</span><span class="sxs-lookup"><span data-stu-id="9a636-146">The following illustration shows a breakpoint, which is displayed as a red-filled circle in the margin.</span></span> 

    <span data-ttu-id="9a636-147">[![RedCircleMargin\_BuildDebugProj](./media/redcirclemargin_builddebugproj.png)](./media/redcirclemargin_builddebugproj.png)</span><span class="sxs-lookup"><span data-stu-id="9a636-147">[![RedCircleMargin\_BuildDebugProj](./media/redcirclemargin_builddebugproj.png)](./media/redcirclemargin_builddebugproj.png)</span></span> 

    <span data-ttu-id="9a636-148">FinalizeRentalCheckout メソッドは、レンタル トランザクションが保存されるときに呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="9a636-148">The FinalizeRentalCheckout method is called when a rental transaction is saved.</span></span> <span data-ttu-id="9a636-149">このメソッドは、RentalTransactionAboutTobeFinalizedEvent という名前のデリゲートを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="9a636-149">This method calls the delegate named RentalTransactionAboutTobeFinalizedEvent.</span></span> <span data-ttu-id="9a636-150">このデリゲートで呼び出される、イベント ハンドラー メソッドを実装することができます。</span><span class="sxs-lookup"><span data-stu-id="9a636-150">You can implement an event handler method, which is called by this delegate.</span></span> <span data-ttu-id="9a636-151">デリゲートを呼び出すメソッドは、RentalConfirmation という名前のパラメーターを渡します。このパラメーターには、レンタルを許可するかブロックするかを示す値が含まれています。</span><span class="sxs-lookup"><span data-stu-id="9a636-151">The method that calls the delegate passes a parameter, named RentalConfirmation, which contains a value that indicates whether the rental should be allowed or blocked.</span></span> <span data-ttu-id="9a636-152">レンタルが許可されている場合、値に true が含まれ、ブロックされている場合は、値に false が含まれます。</span><span class="sxs-lookup"><span data-stu-id="9a636-152">If the rental is allowed, the value contains "true"; if it's blocked, the value contains "false".</span></span> <span data-ttu-id="9a636-153">イベント ハンドラーは、開発者がコード内で実装するために選択するテストに基づいてこの値を変更できます。</span><span class="sxs-lookup"><span data-stu-id="9a636-153">An event handler can change this value, based on any test the developer chooses to implement in code.</span></span> <span data-ttu-id="9a636-154">この場合、クレジット カードの有効期限をテストするコードを変更します。</span><span class="sxs-lookup"><span data-stu-id="9a636-154">In this case, we'll modify the code to test the expiration date of the credit card.</span></span>
10. <span data-ttu-id="9a636-155">F5 を押してアプリケーションをデバッグのために起動するか、**デバッグ** メニューで **デバッグ開始** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="9a636-155">Press F5 to start the application for debugging, or, on the **Debug** menu, click **Start Debugging**.</span></span> <span data-ttu-id="9a636-156">これらの方法のいずれかでアプリケーションを開始することが重要です。</span><span class="sxs-lookup"><span data-stu-id="9a636-156">It's important that you start the application in one of these ways.</span></span> <span data-ttu-id="9a636-157">しない場合は、Visual Studio デバッガーは起動されないため、設定されたブレークポイントのいずれかはヒットされません。</span><span class="sxs-lookup"><span data-stu-id="9a636-157">If you don't, the Visual Studio debugger won't start, so you won't hit any of the breakpoints you've set.</span></span> <span data-ttu-id="9a636-158">**注記**: デバッガーは、コードの位置をソースの位置に関連付ける必要があります。</span><span class="sxs-lookup"><span data-stu-id="9a636-158">**Note**: The debugger needs to relate code position to source positions.</span></span> <span data-ttu-id="9a636-159">アセンブリおよび net モジュールに沿って生成された PDB ファイルの消費を通じて実行されます。</span><span class="sxs-lookup"><span data-stu-id="9a636-159">It does this through consuming PDB files produced alongside the assemblies and net modules.</span></span> <span data-ttu-id="9a636-160">デバッガーは、グローバル ツール設定の設定に示すように、PDBファイルから記号を読み込みます。</span><span class="sxs-lookup"><span data-stu-id="9a636-160">The debugger will load symbols from the PDB files as described in the settings in the global tools settings.</span></span> <span data-ttu-id="9a636-161">読み込むシンボルを制御する設定を含むオプション ページを開くには、**ツール** メニューで **オプション** を選択します。</span><span class="sxs-lookup"><span data-stu-id="9a636-161">To open the options page containing the setting that controls which symbols load, go to the **Tools** menu and choose **Options**.</span></span> <span data-ttu-id="9a636-162">**Microsoft Dynamics 365 for Finance and Operations** グループで、**デバッグ** ページを選択します。</span><span class="sxs-lookup"><span data-stu-id="9a636-162">In the **Microsoft Dynamics 365 for Finance and Operations** group, select the **Debugging** page.</span></span> <span data-ttu-id="9a636-163">このオプションが選択されている場合、システムは、現在のソリューションのコンポーネントに関連する PDB ファイルのみから記号を読み込みます。</span><span class="sxs-lookup"><span data-stu-id="9a636-163">If this option is selected, the system will load symbols from only the PDB files related to the artifacts in the current solution.</span></span> <span data-ttu-id="9a636-164">これにより起動時間が大幅に短縮されるため、このラボでは必ずそれを選択してください。</span><span class="sxs-lookup"><span data-stu-id="9a636-164">This reduces the startup time significantly, so be sure it’s selected for this lab.</span></span> <span data-ttu-id="9a636-165">このオプションを選択すると、現在のソリューションの外部にあるエンティティからソース コードを確認することはできません。</span><span class="sxs-lookup"><span data-stu-id="9a636-165">Be aware that when this option is selected, it won’t be possible to see source code from entities outside of the current solution.</span></span> <span data-ttu-id="9a636-166">数分後、ブラウザーが起動し、プロジェクトで選択されたスタートアップ オブジェクトを表示します。</span><span class="sxs-lookup"><span data-stu-id="9a636-166">After a few moments, the browser will start and display the startup object that was selected in the project.</span></span>
11. <span data-ttu-id="9a636-167">**現在のレンタル** ページが開きます。</span><span class="sxs-lookup"><span data-stu-id="9a636-167">The **Current Rentals** page will open.</span></span>
    1.  <span data-ttu-id="9a636-168">アクション ウィンドウで、**編集** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="9a636-168">In the Action Pane, click **Edit**.</span></span>
    2.  <span data-ttu-id="9a636-169">ページが表示されたら、**表示/非表示** リストで **リストの表示** をクリックします (または **Ctrl+F8** を押します)。</span><span class="sxs-lookup"><span data-stu-id="9a636-169">When the page is displayed, click **Show list** in the **Show/Hide** list (or press **Ctrl+F8**).</span></span>

12. <span data-ttu-id="9a636-170">既存のレンタルに変更を加えます。</span><span class="sxs-lookup"><span data-stu-id="9a636-170">Make a change to any existing rental.</span></span> <span data-ttu-id="9a636-171">たとえば、**編集**をクリックして、レンタル期間が開始した時刻を変更します。</span><span class="sxs-lookup"><span data-stu-id="9a636-171">For example, click **Edit**, and change the time that the rental period started.</span></span>
13. <span data-ttu-id="9a636-172">レンタル レコードを強制的に検証するには、**保存**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="9a636-172">Click **Save** to force a validation of the rental record.</span></span> <span data-ttu-id="9a636-173">ブレークポイントを配置するメソッドが呼び出されます。</span><span class="sxs-lookup"><span data-stu-id="9a636-173">The method in which you placed a breakpoint is called.</span></span> <span data-ttu-id="9a636-174">実行は、ブレークポイントを含むコード行で一時停止します。</span><span class="sxs-lookup"><span data-stu-id="9a636-174">Execution pauses at the line of code that contains the breakpoint.</span></span> 

    <span data-ttu-id="9a636-175">[![ForceValidation\_BuildDebugProj](./media/forcevalidation_builddebugproj.png)](./media/forcevalidation_builddebugproj.png)</span><span class="sxs-lookup"><span data-stu-id="9a636-175">[![ForceValidation\_BuildDebugProj](./media/forcevalidation_builddebugproj.png)](./media/forcevalidation_builddebugproj.png)</span></span> 
    
    <span data-ttu-id="9a636-176">アプリケーションがブレークポイントで一時停止している間に、アプリケーションの状態を調べることができます。</span><span class="sxs-lookup"><span data-stu-id="9a636-176">While the application is paused at a breakpoint, you can examine the application state.</span></span> <span data-ttu-id="9a636-177">通常 Visual Studio で開発するアプリケーションと同じ方法を使用します。</span><span class="sxs-lookup"><span data-stu-id="9a636-177">Use the same techniques that you typically would for any application developed with Visual Studio.</span></span> <span data-ttu-id="9a636-178">たとえば、ツールヒントでその値を表示する変数またはパラメーターにカーソルを置きます。</span><span class="sxs-lookup"><span data-stu-id="9a636-178">For example, place the cursor over a variable or a parameter to see its value in a tooltip.</span></span> 
    
    <span data-ttu-id="9a636-179">[![Tooltip\_BuildDebugProj](./media/tooltip_builddebugproj.png)](./media/tooltip_builddebugproj.png)</span><span class="sxs-lookup"><span data-stu-id="9a636-179">[![Tooltip\_BuildDebugProj](./media/tooltip_builddebugproj.png)](./media/tooltip_builddebugproj.png)</span></span>

14. <span data-ttu-id="9a636-180">Visual Studio の他のデバッグ ツールも利用することができます。</span><span class="sxs-lookup"><span data-stu-id="9a636-180">The other debugging tools in Visual Studio are available as well.</span></span> <span data-ttu-id="9a636-181">たとえば、**ローカル**ウィンドウは、実行が停止した場所のすべてのローカル変数を表示します。</span><span class="sxs-lookup"><span data-stu-id="9a636-181">For example, the **Locals** window shows all of the local variables for the location where execution has stopped.</span></span> <span data-ttu-id="9a636-182">Visual Studio の下部にある **ローカル** タブをクリックし、**fmrentalrecord** 変数を展開します。</span><span class="sxs-lookup"><span data-stu-id="9a636-182">Click the **Locals** tab at the bottom of Visual Studio, and expand the **fmrentalrecord** variable.</span></span> <span data-ttu-id="9a636-183">レコード内のすべてのフィールドの値を示す、レコードの内部状態が表示されます。</span><span class="sxs-lookup"><span data-stu-id="9a636-183">You will see the internal state of the record, showing the values of all the fields in the record.</span></span> 

    <span data-ttu-id="9a636-184">[![InternalState\_BuildDebugProj](./media/internalstate_builddebugproj.png)](./media/internalstate_builddebugproj.png)</span><span class="sxs-lookup"><span data-stu-id="9a636-184">[![InternalState\_BuildDebugProj](./media/internalstate_builddebugproj.png)](./media/internalstate_builddebugproj.png)</span></span> 
    
    <span data-ttu-id="9a636-185">**fmrentalrecord** 変数の**車両**プロパティの値に注目してください。</span><span class="sxs-lookup"><span data-stu-id="9a636-185">Notice the value of the **Vehicle** property of the **fmrentalrecord** variable.</span></span> <span data-ttu-id="9a636-186">このプロパティは、**FMRental** テーブルの外部キー フィールドです。</span><span class="sxs-lookup"><span data-stu-id="9a636-186">This property is a foreign key field in the **FMRental** table.</span></span> <span data-ttu-id="9a636-187">デバッガーを使用すると、FMVehicle テーブルの関連するレコードを調べることができます。</span><span class="sxs-lookup"><span data-stu-id="9a636-187">The debugger allows us to peek into the related record in the FMVehicle table.</span></span> <span data-ttu-id="9a636-188">**AutoIdentification** フィールド グループに属する値を示します。</span><span class="sxs-lookup"><span data-stu-id="9a636-188">It shows values that belong to the **AutoIdentification** field group.</span></span>
15. <span data-ttu-id="9a636-189">**ブレークポイント** ウィンドウには、設定されているすべてのブレークポイントが一覧表示されます。</span><span class="sxs-lookup"><span data-stu-id="9a636-189">The **Breakpoints** window lists all of the breakpoints that have been set.</span></span> <span data-ttu-id="9a636-190">**ブレークポイント** タブをクリックし、コンテンツを表示します。</span><span class="sxs-lookup"><span data-stu-id="9a636-190">Click the **Breakpoints** tab to see its content.</span></span> 

    <span data-ttu-id="9a636-191">[![ブレークポイント\_BuildDebugProj](./media/breakpoint_builddebugproj.png)](./media/breakpoint_builddebugproj.png)</span><span class="sxs-lookup"><span data-stu-id="9a636-191">[![Breakpoint\_BuildDebugProj](./media/breakpoint_builddebugproj.png)](./media/breakpoint_builddebugproj.png)</span></span>

16. <span data-ttu-id="9a636-192">F10 キーを数回押してコードを 1 行ずつ実行し、デバッガー機能の完全な補完を使用します。</span><span class="sxs-lookup"><span data-stu-id="9a636-192">Press F10 a few times to step through the code, line-by-line, and use the full complement of debugger features.</span></span> <span data-ttu-id="9a636-193">**ローカル** ウィンドウが、実行される各ステートメントですぐに変数の値を更新することに注意します。</span><span class="sxs-lookup"><span data-stu-id="9a636-193">Notice that the **Locals** window updates the values of variables immediately with each statement that's executed.</span></span>
17. <span data-ttu-id="9a636-194">ツール バーで、**続行**をクリックするか、F5 を押します。</span><span class="sxs-lookup"><span data-stu-id="9a636-194">On the toolbar, click **Continue**, or press F5</span></span>
18. <span data-ttu-id="9a636-195">Internet Explorer を閉じ、**Fleet Management** アプリケーションを閉じます。</span><span class="sxs-lookup"><span data-stu-id="9a636-195">Close Internet Explorer to close the **Fleet Management** application.</span></span> <span data-ttu-id="9a636-196">Visual Studio はデバッグ モードを終了します。</span><span class="sxs-lookup"><span data-stu-id="9a636-196">Visual Studio will exit the debugging mode.</span></span> <span data-ttu-id="9a636-197">代替は**デバッグの停止**を**デバッグ**メニューから選択します。</span><span class="sxs-lookup"><span data-stu-id="9a636-197">An alternative is to choose **Stop Debugging** from the **Debug** menu.</span></span> <span data-ttu-id="9a636-198">これにより、Internet Explorer は開いたままになり、次のデバッグ セッションをより早く開始することができます。</span><span class="sxs-lookup"><span data-stu-id="9a636-198">This will leave Internet Explorer open, allowing the next debugging session to start faster.</span></span>

## <a name="add-the-validation-code"></a><span data-ttu-id="9a636-199">検証コードの追加</span><span class="sxs-lookup"><span data-stu-id="9a636-199">Add the validation code</span></span>
<span data-ttu-id="9a636-200">**FinalizeRentalCheckout** メソッドでは、開発者がコードを追加してレンタルの有効性を決定するために使用されるデリゲートを呼び出したことを確認します。</span><span class="sxs-lookup"><span data-stu-id="9a636-200">In the **FinalizeRentalCheckout** method, you saw that the developer added code to call the delegate that’s used to determine the validity of the rental.</span></span> <span data-ttu-id="9a636-201">期限切れのクレジット カードの問題を解決するには、クレジット カードが期限切れではないことを確認するために使用するイベント ハンドラーを追加します。</span><span class="sxs-lookup"><span data-stu-id="9a636-201">To solve the problem of expired credit cards, you’ll add an event handler, which you’ll use to verify that the credit card isn’t expired.</span></span> <span data-ttu-id="9a636-202">ラボを簡素化するために、ハンドラはデリゲートを含む同じファイルに追加されます。</span><span class="sxs-lookup"><span data-stu-id="9a636-202">To simplify the lab, the handler will be added in the same file that contains the delegate.</span></span> <span data-ttu-id="9a636-203">インスピレーションとして、次のコードを使用します。</span><span class="sxs-lookup"><span data-stu-id="9a636-203">Use the following code as inspiration.</span></span> <span data-ttu-id="9a636-204">コードをコピーして貼り付けるのではなく、手動で入力して IntelliSense 機能の動作を参照してください。</span><span class="sxs-lookup"><span data-stu-id="9a636-204">Rather than copying and pasting the code, type it in manually to see the IntelliSense features in action.</span></span> <span data-ttu-id="9a636-205">これらの機能により、Visual Studio ユーザーは高い生産性を期待することができます。</span><span class="sxs-lookup"><span data-stu-id="9a636-205">These features add to the high level of productivity that Visual Studio users expect.</span></span>

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

<span data-ttu-id="9a636-206">上記のコードはわかりやすいです。</span><span class="sxs-lookup"><span data-stu-id="9a636-206">The preceding code is straightforward.</span></span> <span data-ttu-id="9a636-207">このメソッドは、**SubscribesTo** 属性を使用して、関連するデリゲートのハンドラーとしてマークされています (図参照)</span><span class="sxs-lookup"><span data-stu-id="9a636-207">The method is marked as handler for the relevant delegate by using the **SubscribesTo** attribute, as shown.</span></span> <span data-ttu-id="9a636-208">コードでは、顧客レコードが取得されてから、クレジット カードの日付が今日の日付と比較されます。</span><span class="sxs-lookup"><span data-stu-id="9a636-208">In the code, the customer record is retrieved, and then the credit card date is compared to today's date.</span></span> <span data-ttu-id="9a636-209">クレジット カードの有効期限が過ぎている場合は、**RentalConfirmation** 構造でイベント ハンドラーの値を設定し、顧客が車両の貸し出しの対象ではないことを通知します。</span><span class="sxs-lookup"><span data-stu-id="9a636-209">If the expiration date of the credit card is in the past, the event handler sets a value in the **RentalConfirmation** structure to signal that the customer isn't eligible to rent a vehicle.</span></span> <span data-ttu-id="9a636-210">これは、任意の数のハンドラーがデリゲートにサブスクライブできるようにするためです。</span><span class="sxs-lookup"><span data-stu-id="9a636-210">The idea is that any number of handlers can subscribe to the delegate.</span></span> <span data-ttu-id="9a636-211">ハンドラーでレンタルを続行しないと決定した場合、**OkToRent** フラグを設定します。</span><span class="sxs-lookup"><span data-stu-id="9a636-211">If any handler determines that a rental should not proceed, it sets the **OkToRent** flag to false.</span></span> <span data-ttu-id="9a636-212">優れた実装では、**OkToRent** フラグがすでに false に設定されていると判断した場合、分析を行わないことがあります。</span><span class="sxs-lookup"><span data-stu-id="9a636-212">A superior implementation might refrain from doing any analysis if it determines that the **OkToRent** flag has already been set to false.</span></span>

1.  <span data-ttu-id="9a636-213">FMRentalCheckoutProcessor.xpp ファイルで作業していることを確認します。</span><span class="sxs-lookup"><span data-stu-id="9a636-213">Be sure that you're working in the FMRentalCheckoutProcessor.xpp file.</span></span> <span data-ttu-id="9a636-214">新しいイベント ハンドラー定義を FMRentalCheckoutProcessor クラスに追加することによって開始します。</span><span class="sxs-lookup"><span data-stu-id="9a636-214">Begin by adding the new event handler definition to the FMRentalCheckoutProcessor class.</span></span> <span data-ttu-id="9a636-215">クラス定義の終了を示す波括弧 (}) のすぐ上の空の明細行に次のコードを追加します。</span><span class="sxs-lookup"><span data-stu-id="9a636-215">Add the following code on an empty line just above the brace (}) that marks the end of the class definition.</span></span>

    ```xpp
    public static void RentalFinalizedEventHandler(FMRental rentalrecord, Struct rentalConfirmation)
    {

    }
    ```

2.  <span data-ttu-id="9a636-216">イベント ハンドラーの先頭に、属性を追加します。</span><span class="sxs-lookup"><span data-stu-id="9a636-216">Add the attributes to the beginning of the event handler.</span></span> <span data-ttu-id="9a636-217">これらの属性は、イベントハンドラーがどのデリゲートに加入しているかを示します。</span><span class="sxs-lookup"><span data-stu-id="9a636-217">These attributes indicate which delegate the event handler is subscribing to.</span></span>

    ```xpp
        [SubscribesTo(classstr(FMRentalCheckoutProcessor),
            delegatestr(FMRentalCheckoutProcessor, RentalTransactionAboutTobeFinalizedEvent))]
            public static void RentalFinalizedEventHandler(FMRental rentalrecord, Struct 
                                                                           RentalConfirmation)
        {

        }
    ```

3.  <span data-ttu-id="9a636-218">ここで、クレジット カードの有効期限の値を確認するコードを追加します。</span><span class="sxs-lookup"><span data-stu-id="9a636-218">Now, add the code that checks the credit card expiration value.</span></span> <span data-ttu-id="9a636-219">完了したメソッドは、次のコードのようになります。</span><span class="sxs-lookup"><span data-stu-id="9a636-219">The completed method should look similar to the following code.</span></span>

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

4.  <span data-ttu-id="9a636-220">ハンドラーとデリゲートが 1 行の空白行で区切られていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="9a636-220">Make sure the handler and the delegate are separated by exactly one blank line.</span></span>
5.  <span data-ttu-id="9a636-221">Visual Studio のツールバーで、**保存** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="9a636-221">On the toolbar in Visual Studio, click **Save**.</span></span>
6.  <span data-ttu-id="9a636-222">コードに問題がなければ、フリート管理プロジェクトのコードをビルドします。</span><span class="sxs-lookup"><span data-stu-id="9a636-222">After you're satisfied with the code, build the code for the Fleet Management project.</span></span> <span data-ttu-id="9a636-223">これを行うには、**ソリューション エクスプローラー** で、**FleetManagement** プロジェクト名を右クリックし、**Build** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="9a636-223">To do this, in **Solution Explorer**, right-click the **FleetManagement** project name, and then click **Build**.</span></span> <span data-ttu-id="9a636-224">コードが正しくない場合は、エラーまたは警告が表示される場合があります。</span><span class="sxs-lookup"><span data-stu-id="9a636-224">You may see errors or warnings if the code isn't correct.</span></span> <span data-ttu-id="9a636-225">その場合は、コードを修正し、再度ビルド警告やエラーが解決されるまでビルドを続行します。</span><span class="sxs-lookup"><span data-stu-id="9a636-225">If so, correct the code, and build again until all warnings and errors have been resolved.</span></span> <span data-ttu-id="9a636-226">これで、リビジョンが意図したとおりに動作することを確認する準備が整いました。</span><span class="sxs-lookup"><span data-stu-id="9a636-226">You're now ready to validate that the revision works as intended.</span></span>
7.  <span data-ttu-id="9a636-227">**デバッグ**メニューをクリックして、**すべてのブレークポイントを削除**します。</span><span class="sxs-lookup"><span data-stu-id="9a636-227">On the **Debug** menu, click **Delete All Breakpoints**.</span></span>
8.  <span data-ttu-id="9a636-228">次のステートメントを含む明細行にあるイベント ハンドラー メソッドに新しいブレークポイントを配置します。</span><span class="sxs-lookup"><span data-stu-id="9a636-228">Place a new breakpoint in the event-handler method at the line that contains the following statement:</span></span>

    ```xpp
    if (lastDayOfExpiryMonth < today())
    ```
    
9.  <span data-ttu-id="9a636-229">F5 キーを押してデバッグをアクティブにし、フリート管理サンプルを開始します。</span><span class="sxs-lookup"><span data-stu-id="9a636-229">Start the Fleet Management sample with debugging active by pressing F5.</span></span>
10. <span data-ttu-id="9a636-230">前のセクションのステップ 11 で説明されているように**現在のレンタル** ページを参照してください。</span><span class="sxs-lookup"><span data-stu-id="9a636-230">Browse to the **Current rentals** page, as described starting in step 11 of the previous section.</span></span> <span data-ttu-id="9a636-231">いずれかの予約を選択し、**編集** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="9a636-231">Select one of the reservations, and click **Edit**.</span></span>
11. <span data-ttu-id="9a636-232">**顧客**ドロップダウン リストで、一覧から Adrian Lannin を選択して**保存**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="9a636-232">In the **Customer** drop-down list, select Adrian Lannin from the list, and then click **Save**.</span></span> <span data-ttu-id="9a636-233">実行は、イベントハンドラー メソッドで設定したブレークポイントで一時停止します。</span><span class="sxs-lookup"><span data-stu-id="9a636-233">Execution pauses at the breakpoint that you set in the event-handler method.</span></span>
12. <span data-ttu-id="9a636-234">F10 キーを 3 回押して、コード ブロックを実行します。</span><span class="sxs-lookup"><span data-stu-id="9a636-234">Press F10 three times to step through the code block.</span></span> 

    <span data-ttu-id="9a636-235">[![StepCodeBlock\_BuildDebugProj](./media/stepcodeblock_builddebugproj.png)](./media/stepcodeblock_builddebugproj.png)</span><span class="sxs-lookup"><span data-stu-id="9a636-235">[![StepCodeBlock\_BuildDebugProj](./media/stepcodeblock_builddebugproj.png)](./media/stepcodeblock_builddebugproj.png)</span></span>
    
13. <span data-ttu-id="9a636-236">コール スタックのコード マップを表示するには、コード エディターを右クリックし、**コード マップにコール スタックを表示** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="9a636-236">To see the code map for the call stacks, right-click in the code editor, and then click **Show Call Stack on Code Map**.</span></span> <span data-ttu-id="9a636-237">呼び出し履歴にコメントを追加し、コードを進め、それに応じたコード マップの変更としてウォッチすることが必要な場合があります。</span><span class="sxs-lookup"><span data-stu-id="9a636-237">You may want to add a comment to the call stack, step through the code, and watch as the code map changes accordingly.</span></span>
14. <span data-ttu-id="9a636-238">F5 キーを押して続行します。</span><span class="sxs-lookup"><span data-stu-id="9a636-238">Press F5 to continue.</span></span> <span data-ttu-id="9a636-239">その顧客が許可されていないことが表示されます。</span><span class="sxs-lookup"><span data-stu-id="9a636-239">You'll see that the customer has been disallowed.</span></span>
15. <span data-ttu-id="9a636-240">同じレンタルで、顧客名を Phil Spencer に変更してから**更新**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="9a636-240">In the same rental, change the customer name to Phil Spencer, and then click **Update**.</span></span> <span data-ttu-id="9a636-241">今回は、トランザクションが可能です。</span><span class="sxs-lookup"><span data-stu-id="9a636-241">This time, the transaction is allowed.</span></span>
16. <span data-ttu-id="9a636-242">Internet Explorer を閉じます。</span><span class="sxs-lookup"><span data-stu-id="9a636-242">Close Internet Explorer.</span></span>
17. <span data-ttu-id="9a636-243">**RentalFinalizedEventHandler** メソッドで **SubscribesTo** をコメントにします。</span><span class="sxs-lookup"><span data-stu-id="9a636-243">Comment out the **SubscribesTo** attribute on the **RentalFinalizedEventHandler** method.</span></span> <span data-ttu-id="9a636-244">このステップでは、残りのチュートリアルで作業してもクレジット カード テストが実行されなくなります。</span><span class="sxs-lookup"><span data-stu-id="9a636-244">This step ensures that the credit card test will no longer run as you work on the remaining tutorials.</span></span>

## <a name="best-practices"></a><span data-ttu-id="9a636-245">ベスト プラクティス</span><span class="sxs-lookup"><span data-stu-id="9a636-245">Best practices</span></span>
<span data-ttu-id="9a636-246">このチュートリアルの前半では、プロジェクトにコードを追加し、変更を加えてソリューションをビルドする営業案件を得ました。</span><span class="sxs-lookup"><span data-stu-id="9a636-246">Earlier in this tutorial, you had the opportunity to add code to the project and build the solution with your changes.</span></span> <span data-ttu-id="9a636-247">ビルド プロセスが成功しなかったため、エラー ウィンドウを参照する必要があります。</span><span class="sxs-lookup"><span data-stu-id="9a636-247">The build process may not have been successful, requiring you to refer to the error window.</span></span> <span data-ttu-id="9a636-248">このウィンドウを使用しているとき、エラーを説明する明細行をクリックすると、エラー状態になります。</span><span class="sxs-lookup"><span data-stu-id="9a636-248">Using this window, you can get to the error by clicking on the line that describes the error.</span></span> <span data-ttu-id="9a636-249">コンパイル エラーを表していないいくつかの診断メッセージが通知される場合があります。</span><span class="sxs-lookup"><span data-stu-id="9a636-249">You may have noticed some diagnostic messages that don’t represent compilation errors.</span></span> <span data-ttu-id="9a636-250">これらは、**ベスト プラクティス** チェッカーからの診断です。</span><span class="sxs-lookup"><span data-stu-id="9a636-250">These are diagnostics from the **Best Practice** checker.</span></span> <span data-ttu-id="9a636-251">このツールは、開発者が既知のベスト プラクティスに違反したインスタンスをチェックして、違反が見つかったときに警告を表示します。</span><span class="sxs-lookup"><span data-stu-id="9a636-251">This tool will check for instances where the developer has violated a known best practice, and display a warning when one is found.</span></span> <span data-ttu-id="9a636-252">ベスト プラクティス ルールは、コードの構成要素とメタデータの両方に適用されます。</span><span class="sxs-lookup"><span data-stu-id="9a636-252">The Best Practice rules apply to both code constructs and metadata.</span></span> <span data-ttu-id="9a636-253">各ソフトウェアの開発組織は、実施するベスト プラクティスのセットを持つ可能性が高いです。</span><span class="sxs-lookup"><span data-stu-id="9a636-253">Each software development organization is likely to have its own set of best practices that they enforce.</span></span> <span data-ttu-id="9a636-254">既存のベスト プラクティス チェックの一部を無視する場合があります。</span><span class="sxs-lookup"><span data-stu-id="9a636-254">They may want to disregard some of the existing best practice checks.</span></span> <span data-ttu-id="9a636-255">これをサポートするために、報告されたベスト プラクティスの診断セットを個々の開発者が変更することができます。</span><span class="sxs-lookup"><span data-stu-id="9a636-255">To support this, the set of reported best practice diagnostics can be modified by the individual developer.</span></span> <span data-ttu-id="9a636-256">これを実証するには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="9a636-256">To demonstrate this, complete the following steps:</span></span>

1.  <span data-ttu-id="9a636-257">**表示**メニューで、**エラー リスト**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="9a636-257">On the **View** menu, click **Error List**.</span></span> <span data-ttu-id="9a636-258">いくつかのベスト プラクティス警告が表示されます。</span><span class="sxs-lookup"><span data-stu-id="9a636-258">You should see a small number of best practice warnings.</span></span>
2.  <span data-ttu-id="9a636-259">**Dynamics 365** メニューで、**オプション** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="9a636-259">On the **Dynamics 365** menu, click **Options**.</span></span> <span data-ttu-id="9a636-260">**Dynamics 365** グループで、**ベスト プラクティス** を選択します。</span><span class="sxs-lookup"><span data-stu-id="9a636-260">In the **Dynamics 365** group, choose **Best Practices**.</span></span>
3.  <span data-ttu-id="9a636-261">**モデル** ドロップダウン リストで、**フリート管理**モデルが選択されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="9a636-261">In the **Model** drop-down list, make sure that the **Fleet Management** model is selected.</span></span> <span data-ttu-id="9a636-262">ベスト プラクティス ルールは、特定のモデルに適用されます。</span><span class="sxs-lookup"><span data-stu-id="9a636-262">The best practice rules apply to a particular model.</span></span>
4.  <span data-ttu-id="9a636-263">ベスト プラクティス ルールのセットの一部に対する選択内容をマークします。</span><span class="sxs-lookup"><span data-stu-id="9a636-263">Mark the selections for some of the sets of Best Practice rules.</span></span> <span data-ttu-id="9a636-264">たとえば、**CodeStyleRules** のエントリを選択する場合、変数のベスト プラクティスのガイドラインが検査されます。</span><span class="sxs-lookup"><span data-stu-id="9a636-264">For example, if you select the entry for **CodeStyleRules**, best practice guidelines for variables will be examined.</span></span> <span data-ttu-id="9a636-265">選択を更新した後、**OK** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="9a636-265">After you've updated the selections, click **OK**.</span></span>
5.  <span data-ttu-id="9a636-266">プロジェクト名を右クリックして **リビルド** をクリックすることにより、フリート管理プロジェクトをリビルドします。</span><span class="sxs-lookup"><span data-stu-id="9a636-266">Rebuild the Fleet Management project by right-clicking the project name and then clicking **Rebuild**.</span></span> <span data-ttu-id="9a636-267">指定したベスト プラクティス ルールの違反が **エラー一覧** ウィンドウに表示されることがわかります。</span><span class="sxs-lookup"><span data-stu-id="9a636-267">You'll notice that the violations of the best practice rules that you specified appear in the **Error list** window.</span></span>

