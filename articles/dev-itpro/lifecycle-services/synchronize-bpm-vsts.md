---
title: "BPM ライブラリと Visual Studio Team Services の同期"
description: "このトピックでは、LCS の BPM ライブラリを Visual Studio Team Services (VSTS) と同期させる方法について説明します。"
author: kfend
manager: AnnBe
ms.date: 11/13/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: AX 2012, Operations
ms.custom: 13301
ms.assetid: 
ms.search.region: Global
ms.author: ntecklu
ms.search.validFrom: 
ms.dyn365.ops.version: 2012
ms.translationtype: HT
ms.sourcegitcommit: e782d33f3748524491dace28008cd9148ae70529
ms.openlocfilehash: b952a5c1b56e8f0a8534323d0e20b00401147615
ms.contentlocale: ja-jp
ms.lasthandoff: 08/09/2018

---

# <a name="synchronize-bpm-libraries-with-visual-studio-team-services"></a><span data-ttu-id="afd89-103">BPM ライブラリと Visual Studio Team Services の同期</span><span class="sxs-lookup"><span data-stu-id="afd89-103">Synchronize BPM libraries with Visual Studio Team Services</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="afd89-104">プロジェクトの実装のステージを開始するには、Microsoft Visual Studio Team Services (VSTS) で、ビジネス プロセス モデラー (BPM) とお客様のプロジェクトを同期します。</span><span class="sxs-lookup"><span data-stu-id="afd89-104">You start the implementation stage of a project by synchronizing a Business process modeler (BPM) library with your project in Microsoft Visual Studio Team Services (VSTS).</span></span> <span data-ttu-id="afd89-105">この方法で、プロセスを確認し、要件を業務プロセスと関連付けることができます。</span><span class="sxs-lookup"><span data-stu-id="afd89-105">In this way, you can review processes and associate requirements with business processes.</span></span> <span data-ttu-id="afd89-106">BPM ライブラリを VSTS プロジェクトと同期させることにより、VSTS での実装プロジェクトの進捗状況を追跡したり、さまざまな作業項目を要件や業務プロセスに関連付けることができます。</span><span class="sxs-lookup"><span data-stu-id="afd89-106">By synchronizing a BPM library with a VSTS project, you can also track the progress of your implementation project in VSTS, and can associate various work items with requirements and business processes.</span></span> <span data-ttu-id="afd89-107">これらの作業項目には、バグ、タスク、バックログ項目、テスト、ドキュメントが含まれます。</span><span class="sxs-lookup"><span data-stu-id="afd89-107">These work items include bugs, tasks, backlog items, tests, and documents.</span></span>

<span data-ttu-id="afd89-108">現在、BPM VSTS 同期では、カスタム作業項目または業務プロセスとの同期をサポートしていません。</span><span class="sxs-lookup"><span data-stu-id="afd89-108">Currently, BPM-VSTS synchronization doesn't support custom work item types or synchronizing business processes with custom work item types.</span></span> <span data-ttu-id="afd89-109">これらのいずれかを試みると、警告が表示されます。</span><span class="sxs-lookup"><span data-stu-id="afd89-109">If you try either of these, you will receive a warning.</span></span> <span data-ttu-id="afd89-110">警告を無視して、カスタム テンプレートとの VSTS 同期を試みる場合は、テンプレートの次の内容を確認することで同期の問題を回避できます。</span><span class="sxs-lookup"><span data-stu-id="afd89-110">If you choose to ignore the warning and attempt a VSTS sync with a custom template, you can avoid synchronization issues by verifying the following for the template:</span></span>
- <span data-ttu-id="afd89-111">作業品目タイプの状態を削除しないでください。</span><span class="sxs-lookup"><span data-stu-id="afd89-111">Does not delete any work item type</span></span>
- <span data-ttu-id="afd89-112">作業品目タイプの状態を削除しないでください。</span><span class="sxs-lookup"><span data-stu-id="afd89-112">Does not delete any state of a work item type</span></span>
- <span data-ttu-id="afd89-113">必須フィールドを作業項目の種類に追加しない</span><span class="sxs-lookup"><span data-stu-id="afd89-113">Does not add any required fields to a work item type</span></span>

<span data-ttu-id="afd89-114">VSTS の詳細については、[[www.visualstudio.com/team-services](http://www.visualstudio.com/team-services)] をご覧ください。</span><span class="sxs-lookup"><span data-stu-id="afd89-114">To learn more about VSTS, go to [www.visualstudio.com/team-services](http://www.visualstudio.com/team-services).</span></span>

## <a name="lcs-project-settings-set-up-vsts"></a><span data-ttu-id="afd89-115">LCS プロジェクト設定: VSTS の設定</span><span class="sxs-lookup"><span data-stu-id="afd89-115">LCS project settings: Set up VSTS</span></span>

<span data-ttu-id="afd89-116">既に Microsoft Dynamics Lifecycle Services (LCS) から VSTS を設定している場合、このセクションの手順を省略できます。</span><span class="sxs-lookup"><span data-stu-id="afd89-116">If you've already set up VSTS from Microsoft Dynamics Lifecycle Services (LCS), you can skip the procedures in this section.</span></span>

### <a name="create-a-personal-access-token"></a><span data-ttu-id="afd89-117">個人用アクセス トークンを作成する</span><span class="sxs-lookup"><span data-stu-id="afd89-117">Create a personal access token</span></span>

<span data-ttu-id="afd89-118">VSTS プロジェクトに接続するために、LCS は個人用アクセス トークンを使用して認証されます。</span><span class="sxs-lookup"><span data-stu-id="afd89-118">To connect to a VSTS project, LCS is authenticated by using a personal access token.</span></span> <span data-ttu-id="afd89-119">VSTS で個人用アクセス トークンを作成するには、これらの手順に従います。</span><span class="sxs-lookup"><span data-stu-id="afd89-119">Follow these steps to create a personal access token in VSTS.</span></span>

1. <span data-ttu-id="afd89-120"><https://www.visualstudio.com> に移動し、サインイン、および VSTS プロジェクトを検索します。</span><span class="sxs-lookup"><span data-stu-id="afd89-120">Go to <https://www.visualstudio.com>, sign in, and find your VSTS project.</span></span>
2. <span data-ttu-id="afd89-121">右上隅で、自分の名前にポインターを置き、表示されるメニューで**セキュリティ**を選択します。</span><span class="sxs-lookup"><span data-stu-id="afd89-121">In the upper-right corner, hold the pointer over your name, and then, on the menu that appears, select **Security**.</span></span>
3. <span data-ttu-id="afd89-122">**追加** を選択し、新しい個人用アクセス トークンを作成します。</span><span class="sxs-lookup"><span data-stu-id="afd89-122">Select **Add** to create a new personal access token.</span></span>
4. <span data-ttu-id="afd89-123">トークン名を入力し、トークンの持続時間を指定します。</span><span class="sxs-lookup"><span data-stu-id="afd89-123">Enter a name for the token, and then specify how long the token should last.</span></span>
5. <span data-ttu-id="afd89-124">**トークンの作成** を選択します。</span><span class="sxs-lookup"><span data-stu-id="afd89-124">Select **Create Token**.</span></span>
6. <span data-ttu-id="afd89-125">トークンをクリップボードにコピーします。</span><span class="sxs-lookup"><span data-stu-id="afd89-125">Copy the token to your clipboard.</span></span>

    > [!NOTE]
    > <span data-ttu-id="afd89-126">このステップを完了してこのページから移動すると、トークンの詳細を再度検索することはできません。</span><span class="sxs-lookup"><span data-stu-id="afd89-126">You won't be able to find the token details again after you complete this step and move away from the page.</span></span> <span data-ttu-id="afd89-127">したがって、ページから移動する前にトークンをコピーしたことを確認してください。</span><span class="sxs-lookup"><span data-stu-id="afd89-127">Therefore, make sure that you've copied the token before you move away from the page.</span></span>

### <a name="configure-your-lcs-project-to-connect-to-vsts"></a><span data-ttu-id="afd89-128">LCS プロジェクト コンフィギュレーションして VSTS に接続する</span><span class="sxs-lookup"><span data-stu-id="afd89-128">Configure your LCS project to connect to VSTS</span></span>

1. <span data-ttu-id="afd89-129">LCS プロジェクトで、**プロジェクト設定**タイルを選択します。</span><span class="sxs-lookup"><span data-stu-id="afd89-129">In your LCS project, select the **Project settings** tile.</span></span>
2. <span data-ttu-id="afd89-130">**Visual Studio Team Services** を選択し、**Visual Studio Team Services の設定** を選択します。</span><span class="sxs-lookup"><span data-stu-id="afd89-130">Select **Visual Studio Team Services**, and then select **Setup Visual Studio Team Services**.</span></span> <span data-ttu-id="afd89-131">この構成は多くの LCS ツールで必要です。</span><span class="sxs-lookup"><span data-stu-id="afd89-131">This configuration is required by many LCS tools.</span></span> <span data-ttu-id="afd89-132">既に LCS を構成して VSTS プロジェクトに接続している場合、この手順を省略するか、**変更**を選択して既存のコンフィギュレーションを変更できます。</span><span class="sxs-lookup"><span data-stu-id="afd89-132">If you've already configured LCS to connect to your VSTS project, you can either skip this procedure or select **Change** to change the existing configuration.</span></span>
3. <span data-ttu-id="afd89-133">VSTS アカウントのルート URL および以前に作成した個人用アクセス トークンを入力し、**続行**を選択します。</span><span class="sxs-lookup"><span data-stu-id="afd89-133">Enter the root URL for your VSTS account, and the personal access token that you created earlier, and then select **Continue**.</span></span>
4. <span data-ttu-id="afd89-134">VSTS プロジェクトを選択します。</span><span class="sxs-lookup"><span data-stu-id="afd89-134">Select your VSTS project.</span></span>
5. <span data-ttu-id="afd89-135">LCS/BPM 項目と関連付けられている VSTS 作業項目の種類の間のマッピングを指定します。</span><span class="sxs-lookup"><span data-stu-id="afd89-135">Specify the mapping between LCS/BPM items and the associated VSTS work item types.</span></span>

    ![作業項目タイプ マッピング](./media/newbpm_BlogPost24.png)

6. <span data-ttu-id="afd89-137">**続行** を選択して変更内容を確認し、**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="afd89-137">Select **Continue**, review your changes, and then select **Save**.</span></span>

## <a name="synchronize-a-bpm-library-with-a-vsts-project"></a><span data-ttu-id="afd89-138">VSTS プロジェクトと BPM ライブラリを同期</span><span class="sxs-lookup"><span data-stu-id="afd89-138">Synchronize a BPM library with a VSTS project</span></span>

<span data-ttu-id="afd89-139">LCS プロジェクトおよび VSTS プロジェクト間の接続を設定した後は、VSTS プロジェクトにBPM ライブラリを同期することができます。</span><span class="sxs-lookup"><span data-stu-id="afd89-139">After you've set up the connection between the LCS project and a VSTS project, you can synchronize a BPM library with the VSTS project.</span></span> <span data-ttu-id="afd89-140">BPM ライブラリを VSTS プロジェクトと同期させると、BPM ライブラリ内の各業務プロセスの明細行に対して VSTS 作業項目が作成されます。</span><span class="sxs-lookup"><span data-stu-id="afd89-140">When you synchronize a BPM library with a VSTS project, a VSTS work item is created for each business process line in the BPM library.</span></span> <span data-ttu-id="afd89-141">さらに、BPM の業務プロセスの階層は、VSTS の作業項目の階層に反映されます。</span><span class="sxs-lookup"><span data-stu-id="afd89-141">In addition, the hierarchy of business processes in BPM is reflected in the hierarchy of work items in VSTS.</span></span> <span data-ttu-id="afd89-142">VSTS で作成される作業項目のタイプは、LCS プロジェクトの設定によって異なります。</span><span class="sxs-lookup"><span data-stu-id="afd89-142">The type of work items that are created in VSTS depends on the settings of your LCS project.</span></span>

<span data-ttu-id="afd89-143">この同期は一方向の同期です。</span><span class="sxs-lookup"><span data-stu-id="afd89-143">This synchronization is a one-way synchronization.</span></span> <span data-ttu-id="afd89-144">LCS の変更は VSTS に反映されますが、VSTS の変更は LCS に反映されません。</span><span class="sxs-lookup"><span data-stu-id="afd89-144">Changes in LCS are reflected in VSTS, but changes in VSTS aren't reflected in LCS.</span></span>

<span data-ttu-id="afd89-145">次の情報が同期されます。</span><span class="sxs-lookup"><span data-stu-id="afd89-145">The following information is synchronized:</span></span>

- <span data-ttu-id="afd89-146">業務プロセスの名前</span><span class="sxs-lookup"><span data-stu-id="afd89-146">Business process names</span></span>
- <span data-ttu-id="afd89-147">業務プロセスの説明</span><span class="sxs-lookup"><span data-stu-id="afd89-147">Business process descriptions</span></span>
- <span data-ttu-id="afd89-148">キーワード (タグとして)</span><span class="sxs-lookup"><span data-stu-id="afd89-148">Keywords (as tags)</span></span>
- <span data-ttu-id="afd89-149">国または地域 (タグとして)</span><span class="sxs-lookup"><span data-stu-id="afd89-149">Countries or regions (as tags)</span></span>
- <span data-ttu-id="afd89-150">業界 (タグとして)</span><span class="sxs-lookup"><span data-stu-id="afd89-150">Industries (as tags)</span></span>

<span data-ttu-id="afd89-151">BPM ライブラリを VSTS プロジェクトと同期させるには、**業務プロセス ライブラリ**ページで、同期するライブラリのタイルの省略記号ボタン (...) を選択し、**VSTS同期**を選択します。</span><span class="sxs-lookup"><span data-stu-id="afd89-151">To synchronize a BPM library with a VSTS project, on the **Business process libraries** page, on the tile for the library that you want to synchronize, select the ellipsis button (…), and then select **VSTS sync**.</span></span>

![ライブラリのタイルから VSTS 同期を開始](./media/newbpm_BlogPost25.png)

<span data-ttu-id="afd89-153">また、BPM ライブラリ内のツールバーから VSTS 同期を開始することができます。</span><span class="sxs-lookup"><span data-stu-id="afd89-153">You can also start VSTS synchronization from the toolbar in a BPM library.</span></span> <span data-ttu-id="afd89-154">省略記号ボタン (...) を選択し、**VSTS の同期** を選択します。</span><span class="sxs-lookup"><span data-stu-id="afd89-154">Select the ellipsis button (…), and then select **VSTS sync**.</span></span>

![ライブラリのツール バーから VSTS 同期を開始](./media/newbpm_BlogPost26.png)

>[!NOTE]
> <span data-ttu-id="afd89-156">BPM ローカライズはサポートされません。</span><span class="sxs-lookup"><span data-stu-id="afd89-156">BPM localization is not supported.</span></span> <span data-ttu-id="afd89-157">EN-US 以外の言語で新しい BPM クライアントを編集すると、変更が加えられた言語で BPM を表示したときのみ変更が表示されます。</span><span class="sxs-lookup"><span data-stu-id="afd89-157">If you edit in the new BPM client in any language other than EN-US, your changes will only display when you view the BPM in the language in which the changes were made.</span></span> <span data-ttu-id="afd89-158">EN-US で行われた変更を表示するには、変更が表示される前に、Visual Studio Team Server と同期する必要があります。</span><span class="sxs-lookup"><span data-stu-id="afd89-158">To view any changes made in EN-US, you must synchronize with Visual Studio Team Server before the changes will display.</span></span>

## <a name="turn-off-synchronization-of-bpm-with-vsts"></a><span data-ttu-id="afd89-159">VSTS と BPM の同期をオフにする</span><span class="sxs-lookup"><span data-stu-id="afd89-159">Turn off synchronization of BPM with VSTS</span></span>

<span data-ttu-id="afd89-160">同期をオフにするには、**業務プロセス ライブラリ** ページで同期を停止するライブラリを選択し、省略記号ボタン (...) を選択してから **VSTS 同期** を選択解除します。</span><span class="sxs-lookup"><span data-stu-id="afd89-160">To turn off synchronization, on the **Business process libraries** page, select the library that you want to stop synchronizing, select the ellipsis button (…), and then unselect **VSTS sync**.</span></span>

## <a name="review-processes-and-add-requirements"></a><span data-ttu-id="afd89-161">プロセスを確認し、要件を追加</span><span class="sxs-lookup"><span data-stu-id="afd89-161">Review processes and add requirements</span></span>

<span data-ttu-id="afd89-162">要件を収集しているプロジェクトのフェーズ中に、BPM ライブラリを使用して、ビジネス プロセスおよびタスクをレビューし、要件を特定することができます。</span><span class="sxs-lookup"><span data-stu-id="afd89-162">During the project phase where you're gathering requirements, you can use the BPM library to review business processes and tasks, and to identify requirements.</span></span> <span data-ttu-id="afd89-163">BPM で、業務プロセスを確認済みとマークして、確認プロセスを追跡することができます。</span><span class="sxs-lookup"><span data-stu-id="afd89-163">In BPM, you can mark business processes as reviewed to track the review process.</span></span>

<span data-ttu-id="afd89-164">プロセスまたはその子プロセスの 1 つをレビューとしてマークするには、BPMでプロセスを選択し、右ウィンドウの **概要** タブで **レビューとしてマーク** を選択します。</span><span class="sxs-lookup"><span data-stu-id="afd89-164">To mark a process or one of its child processes as reviewed, select the process in BPM, and then, in the right pane, on the **Overview** tab, select **Mark as reviewed**.</span></span>

<span data-ttu-id="afd89-165">業務プロセスを確認済みとしてマークすると、**確認済** 列が更新されます。</span><span class="sxs-lookup"><span data-stu-id="afd89-165">When a business process is marked as reviewed, the **Reviewed** column is updated.</span></span> <span data-ttu-id="afd89-166">この列には、次の情報が表示されます。</span><span class="sxs-lookup"><span data-stu-id="afd89-166">This column shows the following information:</span></span>

- <span data-ttu-id="afd89-167">分数では、直接の子プロセスの確認された数を示します。</span><span class="sxs-lookup"><span data-stu-id="afd89-167">A fraction indicates how many direct child processes have been reviewed.</span></span>
- <span data-ttu-id="afd89-168">記号は、プロセスとその子プロセスがどれだけ完全にレビューされたかを示します。</span><span class="sxs-lookup"><span data-stu-id="afd89-168">A symbol indicates how completely the process and its child processes have been reviewed:</span></span>

   - <span data-ttu-id="afd89-169">**緑のチェック マーク** – プロセスとそのすべての子プロセスは完全に確認済です。</span><span class="sxs-lookup"><span data-stu-id="afd89-169">**Green check mark** – The process and all its child processes have been fully reviewed.</span></span>
   - <span data-ttu-id="afd89-170">**黄色の円** – プロセスおよびその子プロセスは部分的に確認されています。</span><span class="sxs-lookup"><span data-stu-id="afd89-170">**Yellow circle** – The process and its child processes have been partially reviewed.</span></span>
   - <span data-ttu-id="afd89-171">**赤いダッシュ** – プロセスとその子プロセスは確認されていません。</span><span class="sxs-lookup"><span data-stu-id="afd89-171">**Red dash** – The process and its child processes haven't been reviewed.</span></span>

![レビュー列の例](./media/newbpm_BlogPost28.png)

<span data-ttu-id="afd89-173">BPM ライブラリが VSTS プロジェクトと同期され、プロセスを BPM でレビュー済みとマークすると、そのステータスは VSTS の **Active** に変更されます。</span><span class="sxs-lookup"><span data-stu-id="afd89-173">If a BPM library is synchronized with a VSTS project, and you mark a process as reviewed in BPM, its status is changed to **Active** in VSTS.</span></span>

<span data-ttu-id="afd89-174">VSTS に接続されている業務プロセスを確認するとき、VSTS プロジェクトに要求を直接追加することができます。</span><span class="sxs-lookup"><span data-stu-id="afd89-174">While you're reviewing a business process that is connected to VSTS, you can add a requirement directly to your VSTS project.</span></span>

1. <span data-ttu-id="afd89-175">ビジネス プロセスを選択します。</span><span class="sxs-lookup"><span data-stu-id="afd89-175">Select a business process.</span></span>
2. <span data-ttu-id="afd89-176">右ウィンドウの**要件**タブで、**要件を追加**を選択します。</span><span class="sxs-lookup"><span data-stu-id="afd89-176">In the right pane, on the **Requirements** tab, select **Add requirement**.</span></span>
3. <span data-ttu-id="afd89-177">名前、説明、およびタイプを入力し、次に**作成**を選択します。</span><span class="sxs-lookup"><span data-stu-id="afd89-177">Enter a name, description, and type, and then select **Create**.</span></span>

    ![要件を作成しています](./media/newbpm_BlogPost29.png)

    <span data-ttu-id="afd89-179">VSTS では、現在の業務プロセスに関連付けられている要求作業項目が作成されます。</span><span class="sxs-lookup"><span data-stu-id="afd89-179">In VSTS, a requirement work item is created that is associated with the current business process.</span></span>

<span data-ttu-id="afd89-180">現在の業務プロセスに関連付けられている VSTS 作業項目に移動するには、**要件** タブで適切なリンクを選択します。</span><span class="sxs-lookup"><span data-stu-id="afd89-180">To go to the VSTS work items that are associated with the current business process, on the **Requirements** tab, select the appropriate links.</span></span>

