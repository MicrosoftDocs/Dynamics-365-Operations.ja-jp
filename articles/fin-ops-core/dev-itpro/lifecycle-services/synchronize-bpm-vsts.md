---
title: BPM ライブラリと Azure DevOps の同期
description: このトピックでは、LCS の BPM ライブラリを Azure DevOps と同期させる方法について説明します。
author: amarshall
ms.date: 05/13/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: sericks
ms.custom: 13301
ms.assetid: ''
ms.search.region: Global
ms.author: tsmarsha
ms.search.validFrom: ''
ms.dyn365.ops.version: 2012
ms.openlocfilehash: e86b88d74c28fa78f2f194c61d77e49946795db6
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5748423"
---
# <a name="synchronize-bpm-libraries-with-azure-devops"></a><span data-ttu-id="791ab-103">BPM ライブラリと Azure DevOps の同期</span><span class="sxs-lookup"><span data-stu-id="791ab-103">Synchronize BPM libraries with Azure DevOps</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="791ab-104">プロジェクトの実装のステージを開始するには、Microsoft Azure DevOps で、ビジネス プロセス モデラー (BPM) とお客様のプロジェクトを同期します。</span><span class="sxs-lookup"><span data-stu-id="791ab-104">You start the implementation stage of a project by synchronizing a Business process modeler (BPM) library with your project in Microsoft Azure DevOps.</span></span> <span data-ttu-id="791ab-105">この方法で、プロセスを確認し、要件を業務プロセスと関連付けることができます。</span><span class="sxs-lookup"><span data-stu-id="791ab-105">In this way, you can review processes and associate requirements with business processes.</span></span> <span data-ttu-id="791ab-106">BPM ライブラリを Azure DevOps プロジェクトと同期させることにより、Azure DevOps での実装プロジェクトの進捗状況を追跡したり、さまざまな作業項目を要件や業務プロセスに関連付けることができます。</span><span class="sxs-lookup"><span data-stu-id="791ab-106">By synchronizing a BPM library with a Azure DevOps project, you can also track the progress of your implementation project in Azure DevOps, and can associate various work items with requirements and business processes.</span></span> <span data-ttu-id="791ab-107">これらの作業項目には、バグ、タスク、バックログ項目、テスト、ドキュメントが含まれます。</span><span class="sxs-lookup"><span data-stu-id="791ab-107">These work items include bugs, tasks, backlog items, tests, and documents.</span></span>

<span data-ttu-id="791ab-108">現在、BPM Azure DevOps 同期では、カスタム作業項目または業務プロセスとの同期をサポートしていません。</span><span class="sxs-lookup"><span data-stu-id="791ab-108">Currently, BPM-Azure DevOps synchronization doesn't support custom work item types or synchronizing business processes with custom work item types.</span></span> <span data-ttu-id="791ab-109">これらのいずれかを試みると、警告が表示されます。</span><span class="sxs-lookup"><span data-stu-id="791ab-109">If you try either of these, you will receive a warning.</span></span> <span data-ttu-id="791ab-110">警告を無視して、カスタム テンプレートとの Azure DevOps 同期を試みる場合は、テンプレートの次の内容を確認することで同期の問題を回避できます。</span><span class="sxs-lookup"><span data-stu-id="791ab-110">If you choose to ignore the warning and attempt a Azure DevOps sync with a custom template, you can avoid synchronization issues by verifying the following for the template:</span></span>
- <span data-ttu-id="791ab-111">作業品目タイプの状態を削除しないでください。</span><span class="sxs-lookup"><span data-stu-id="791ab-111">Does not delete any work item type</span></span>
- <span data-ttu-id="791ab-112">作業品目タイプの状態を削除しないでください。</span><span class="sxs-lookup"><span data-stu-id="791ab-112">Does not delete any state of a work item type</span></span>
- <span data-ttu-id="791ab-113">必須フィールドを作業項目の種類に追加しない</span><span class="sxs-lookup"><span data-stu-id="791ab-113">Does not add any required fields to a work item type</span></span>

<span data-ttu-id="791ab-114">Azure DevOps の詳細については、[www.visualstudio.com/team-services](https://www.visualstudio.com/team-services) をご覧ください。</span><span class="sxs-lookup"><span data-stu-id="791ab-114">To learn more about Azure DevOps, go to [www.visualstudio.com/team-services](https://www.visualstudio.com/team-services).</span></span>

## <a name="lcs-project-settings-set-up-azure-devops"></a><span data-ttu-id="791ab-115">LCS プロジェクト設定: Azure DevOps の設定</span><span class="sxs-lookup"><span data-stu-id="791ab-115">LCS project settings: Set up Azure DevOps</span></span>

<span data-ttu-id="791ab-116">既に Microsoft Dynamics Lifecycle Services (LCS) から Azure DevOps を設定している場合、このセクションの手順を省略できます。</span><span class="sxs-lookup"><span data-stu-id="791ab-116">If you've already set up Azure DevOps from Microsoft Dynamics Lifecycle Services (LCS), you can skip the procedures in this section.</span></span>

### <a name="create-a-personal-access-token"></a><span data-ttu-id="791ab-117">個人用アクセス トークンを作成する</span><span class="sxs-lookup"><span data-stu-id="791ab-117">Create a personal access token</span></span>

<span data-ttu-id="791ab-118">Azure DevOps プロジェクトに接続するために、LCS は個人用アクセス トークンを使用して認証されます。</span><span class="sxs-lookup"><span data-stu-id="791ab-118">To connect to a Azure DevOps project, LCS is authenticated by using a personal access token.</span></span> <span data-ttu-id="791ab-119">Azure DevOps で個人用アクセス トークンを作成するには、これらの手順に従います。</span><span class="sxs-lookup"><span data-stu-id="791ab-119">Follow these steps to create a personal access token in Azure DevOps.</span></span>

1. <span data-ttu-id="791ab-120"><https://www.visualstudio.com> に移動し、サインイン、および Azure DevOps プロジェクトを検索します。</span><span class="sxs-lookup"><span data-stu-id="791ab-120">Go to <https://www.visualstudio.com>, sign in, and find your Azure DevOps project.</span></span>
2. <span data-ttu-id="791ab-121">右上隅で、自分の名前にポインターを置き、表示されるメニューで **セキュリティ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="791ab-121">In the upper-right corner, hold the pointer over your name, and then, on the menu that appears, select **Security**.</span></span>
3. <span data-ttu-id="791ab-122">**追加** を選択し、新しい個人用アクセス トークンを作成します。</span><span class="sxs-lookup"><span data-stu-id="791ab-122">Select **Add** to create a new personal access token.</span></span>
4. <span data-ttu-id="791ab-123">トークン名を入力し、トークンの持続時間を指定します。</span><span class="sxs-lookup"><span data-stu-id="791ab-123">Enter a name for the token, and then specify how long the token should last.</span></span>
5. <span data-ttu-id="791ab-124">**トークンの作成** を選択します。</span><span class="sxs-lookup"><span data-stu-id="791ab-124">Select **Create Token**.</span></span>
6. <span data-ttu-id="791ab-125">トークンをクリップボードにコピーします。</span><span class="sxs-lookup"><span data-stu-id="791ab-125">Copy the token to your clipboard.</span></span>

    > [!NOTE]
    > <span data-ttu-id="791ab-126">このステップを完了してこのページから移動すると、トークンの詳細を再度検索することはできません。</span><span class="sxs-lookup"><span data-stu-id="791ab-126">You won't be able to find the token details again after you complete this step and move away from the page.</span></span> <span data-ttu-id="791ab-127">したがって、ページから移動する前にトークンをコピーしたことを確認してください。</span><span class="sxs-lookup"><span data-stu-id="791ab-127">Therefore, make sure that you've copied the token before you move away from the page.</span></span>

### <a name="configure-your-lcs-project-to-connect-to-azure-devops"></a><span data-ttu-id="791ab-128">LCS プロジェクトをコンフィギュレーションして Azure DevOps に接続する</span><span class="sxs-lookup"><span data-stu-id="791ab-128">Configure your LCS project to connect to Azure DevOps</span></span>

1. <span data-ttu-id="791ab-129">LCS プロジェクトで、**プロジェクト設定** タイルを選択します。</span><span class="sxs-lookup"><span data-stu-id="791ab-129">In your LCS project, select the **Project settings** tile.</span></span>
2. <span data-ttu-id="791ab-130">**Azure DevOps** を選択し、**Azure DevOps の設定** を選択します。</span><span class="sxs-lookup"><span data-stu-id="791ab-130">Select **Azure DevOps**, and then select **Setup Azure DevOps**.</span></span> <span data-ttu-id="791ab-131">この構成は多くの LCS ツールで必要です。</span><span class="sxs-lookup"><span data-stu-id="791ab-131">This configuration is required by many LCS tools.</span></span> <span data-ttu-id="791ab-132">既に LCS を構成して Azure DevOps プロジェクトに接続している場合、この手順を省略するか、**変更** を選択して既存のコンフィギュレーションを変更できます。</span><span class="sxs-lookup"><span data-stu-id="791ab-132">If you've already configured LCS to connect to your Azure DevOps project, you can either skip this procedure or select **Change** to change the existing configuration.</span></span>
3. <span data-ttu-id="791ab-133">Azure DevOps アカウントのルート URL および以前に作成した個人用アクセス トークンを入力し、**続行** を選択します。</span><span class="sxs-lookup"><span data-stu-id="791ab-133">Enter the root URL for your Azure DevOps account, and the personal access token that you created earlier, and then select **Continue**.</span></span>
4. <span data-ttu-id="791ab-134">Azure DevOps プロジェクトを選択します。</span><span class="sxs-lookup"><span data-stu-id="791ab-134">Select your Azure DevOps project.</span></span>
5. <span data-ttu-id="791ab-135">LCS/BPM 項目と関連付けられている Azure DevOps 作業項目の種類の間のマッピングを指定します。</span><span class="sxs-lookup"><span data-stu-id="791ab-135">Specify the mapping between LCS/BPM items and the associated Azure DevOps work item types.</span></span>

    ![作業項目タイプ マッピング](./media/newbpm_BlogPost24.png)

6. <span data-ttu-id="791ab-137">**続行** を選択して変更内容を確認し、**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="791ab-137">Select **Continue**, review your changes, and then select **Save**.</span></span>

## <a name="synchronize-a-bpm-library-with-a-azure-devops-project"></a><span data-ttu-id="791ab-138">Azure DevOps プロジェクトと BPM ライブラリの同期</span><span class="sxs-lookup"><span data-stu-id="791ab-138">Synchronize a BPM library with a Azure DevOps project</span></span>

<span data-ttu-id="791ab-139">LCS プロジェクトおよび Azure DevOps プロジェクト間の接続を設定した後は、Azure DevOps プロジェクトに BPM ライブラリを同期することができます。</span><span class="sxs-lookup"><span data-stu-id="791ab-139">After you've set up the connection between the LCS project and a Azure DevOps project, you can synchronize a BPM library with the Azure DevOps project.</span></span> <span data-ttu-id="791ab-140">BPM ライブラリを Azure DevOps プロジェクトと同期させると、BPM ライブラリ内の各業務プロセスの明細行に対して Azure DevOps 作業項目が作成されます。</span><span class="sxs-lookup"><span data-stu-id="791ab-140">When you synchronize a BPM library with a Azure DevOps project, a Azure DevOps work item is created for each business process line in the BPM library.</span></span> <span data-ttu-id="791ab-141">さらに、BPM の業務プロセスの階層は、Azure DevOps の作業項目の階層に反映されます。</span><span class="sxs-lookup"><span data-stu-id="791ab-141">In addition, the hierarchy of business processes in BPM is reflected in the hierarchy of work items in Azure DevOps.</span></span> <span data-ttu-id="791ab-142">Azure DevOps で作成される作業項目のタイプは、LCS プロジェクトの設定によって異なります。</span><span class="sxs-lookup"><span data-stu-id="791ab-142">The type of work items that are created in Azure DevOps depends on the settings of your LCS project.</span></span>

<span data-ttu-id="791ab-143">この同期は一方向の同期です。</span><span class="sxs-lookup"><span data-stu-id="791ab-143">This synchronization is a one-way synchronization.</span></span> <span data-ttu-id="791ab-144">LCS の変更は Azure DevOps に反映されますが、Azure DevOps の変更は LCS に反映されません。</span><span class="sxs-lookup"><span data-stu-id="791ab-144">Changes in LCS are reflected in Azure DevOps, but changes in Azure DevOps aren't reflected in LCS.</span></span>

<span data-ttu-id="791ab-145">次の情報が同期されます。</span><span class="sxs-lookup"><span data-stu-id="791ab-145">The following information is synchronized:</span></span>

- <span data-ttu-id="791ab-146">業務プロセスの名前</span><span class="sxs-lookup"><span data-stu-id="791ab-146">Business process names</span></span>
- <span data-ttu-id="791ab-147">業務プロセスの説明</span><span class="sxs-lookup"><span data-stu-id="791ab-147">Business process descriptions</span></span>
- <span data-ttu-id="791ab-148">キーワード (タグとして)</span><span class="sxs-lookup"><span data-stu-id="791ab-148">Keywords (as tags)</span></span>
- <span data-ttu-id="791ab-149">国または地域 (タグとして)</span><span class="sxs-lookup"><span data-stu-id="791ab-149">Countries or regions (as tags)</span></span>
- <span data-ttu-id="791ab-150">業界 (タグとして)</span><span class="sxs-lookup"><span data-stu-id="791ab-150">Industries (as tags)</span></span>

<span data-ttu-id="791ab-151">BPM ライブラリを Azure DevOps プロジェクトと同期させるには、**業務プロセス ライブラリ** ページで、同期するライブラリのタイルの省略記号ボタン (...) を選択し、**Azure DevOps 同期** を選択します。</span><span class="sxs-lookup"><span data-stu-id="791ab-151">To synchronize a BPM library with a Azure DevOps project, on the **Business process libraries** page, on the tile for the library that you want to synchronize, select the ellipsis button (…), and then select **Azure DevOps sync**.</span></span>

![ライブラリのタイルから Azure DevOps 同期を開始](./media/newbpm_BlogPost25.png)

<span data-ttu-id="791ab-153">また、BPM ライブラリ内のツールバーから Azure DevOps 同期を開始することができます。</span><span class="sxs-lookup"><span data-stu-id="791ab-153">You can also start Azure DevOps synchronization from the toolbar in a BPM library.</span></span> <span data-ttu-id="791ab-154">省略記号ボタン (...) を選択し、**Azure DevOps の同期** を選択します。</span><span class="sxs-lookup"><span data-stu-id="791ab-154">Select the ellipsis button (…), and then select **Azure DevOps sync**.</span></span>

![ライブラリのツール バーから Azure DevOps 同期を開始](./media/newbpm_BlogPost26.png)

> [!NOTE]
> <span data-ttu-id="791ab-156">BPM ローカライズはサポートされません。</span><span class="sxs-lookup"><span data-stu-id="791ab-156">BPM localization is not supported.</span></span> <span data-ttu-id="791ab-157">EN-US 以外の言語で新しい BPM クライアントを編集すると、変更が加えられた言語で BPM を表示したときのみ変更が表示されます。</span><span class="sxs-lookup"><span data-stu-id="791ab-157">If you edit in the new BPM client in any language other than EN-US, your changes will only display when you view the BPM in the language in which the changes were made.</span></span> <span data-ttu-id="791ab-158">EN-US で行われた変更を表示するには、変更が表示される前に、Visual Studio Team Server と同期する必要があります。</span><span class="sxs-lookup"><span data-stu-id="791ab-158">To view any changes made in EN-US, you must synchronize with Visual Studio Team Server before the changes will display.</span></span>

## <a name="turn-off-synchronization-of-bpm-with-azure-devops"></a><span data-ttu-id="791ab-159">BPM と Azure DevOps の同期の停止</span><span class="sxs-lookup"><span data-stu-id="791ab-159">Turn off synchronization of BPM with Azure DevOps</span></span>

<span data-ttu-id="791ab-160">同期をオフにするには、**業務プロセス ライブラリ** ページで同期を停止するライブラリを選択し、省略記号ボタン (...) を選択してから **Azure DevOps 同期** を選択解除します。</span><span class="sxs-lookup"><span data-stu-id="791ab-160">To turn off synchronization, on the **Business process libraries** page, select the library that you want to stop synchronizing, select the ellipsis button (…), and then unselect **Azure DevOps sync**.</span></span>

## <a name="review-processes-and-add-requirements"></a><span data-ttu-id="791ab-161">プロセスを確認し、要件を追加</span><span class="sxs-lookup"><span data-stu-id="791ab-161">Review processes and add requirements</span></span>

<span data-ttu-id="791ab-162">要件を収集しているプロジェクトのフェーズ中に、BPM ライブラリを使用して、ビジネス プロセスおよびタスクをレビューし、要件を特定することができます。</span><span class="sxs-lookup"><span data-stu-id="791ab-162">During the project phase where you're gathering requirements, you can use the BPM library to review business processes and tasks, and to identify requirements.</span></span> <span data-ttu-id="791ab-163">BPM で、業務プロセスを確認済みとマークして、確認プロセスを追跡することができます。</span><span class="sxs-lookup"><span data-stu-id="791ab-163">In BPM, you can mark business processes as reviewed to track the review process.</span></span>

<span data-ttu-id="791ab-164">プロセスまたはその子プロセスの 1 つをレビューとしてマークするには、BPMでプロセスを選択し、右ウィンドウの **概要** タブで **レビューとしてマーク** を選択します。</span><span class="sxs-lookup"><span data-stu-id="791ab-164">To mark a process or one of its child processes as reviewed, select the process in BPM, and then, in the right pane, on the **Overview** tab, select **Mark as reviewed**.</span></span>

<span data-ttu-id="791ab-165">業務プロセスを確認済みとしてマークすると、**確認済** 列が更新されます。</span><span class="sxs-lookup"><span data-stu-id="791ab-165">When a business process is marked as reviewed, the **Reviewed** column is updated.</span></span> <span data-ttu-id="791ab-166">この列には、次の情報が表示されます。</span><span class="sxs-lookup"><span data-stu-id="791ab-166">This column shows the following information:</span></span>

- <span data-ttu-id="791ab-167">分数では、直接の子プロセスの確認された数を示します。</span><span class="sxs-lookup"><span data-stu-id="791ab-167">A fraction indicates how many direct child processes have been reviewed.</span></span>
- <span data-ttu-id="791ab-168">記号は、プロセスとその子プロセスがどれだけ完全にレビューされたかを示します。</span><span class="sxs-lookup"><span data-stu-id="791ab-168">A symbol indicates how completely the process and its child processes have been reviewed:</span></span>

   - <span data-ttu-id="791ab-169">**緑のチェック マーク** – プロセスとそのすべての子プロセスは完全に確認済です。</span><span class="sxs-lookup"><span data-stu-id="791ab-169">**Green check mark** – The process and all its child processes have been fully reviewed.</span></span>
   - <span data-ttu-id="791ab-170">**黄色の円** – プロセスおよびその子プロセスは部分的に確認されています。</span><span class="sxs-lookup"><span data-stu-id="791ab-170">**Yellow circle** – The process and its child processes have been partially reviewed.</span></span>
   - <span data-ttu-id="791ab-171">**赤いダッシュ** – プロセスとその子プロセスは確認されていません。</span><span class="sxs-lookup"><span data-stu-id="791ab-171">**Red dash** – The process and its child processes haven't been reviewed.</span></span>

![レビュー列の例](./media/newbpm_BlogPost28.png)

<span data-ttu-id="791ab-173">Azure DevOps に接続されている業務プロセスを確認するとき、Azure DevOps プロジェクトに要求を直接追加することができます。</span><span class="sxs-lookup"><span data-stu-id="791ab-173">While you're reviewing a business process that is connected to Azure DevOps, you can add a requirement directly to your Azure DevOps project.</span></span>

1. <span data-ttu-id="791ab-174">ビジネス プロセスを選択します。</span><span class="sxs-lookup"><span data-stu-id="791ab-174">Select a business process.</span></span>
2. <span data-ttu-id="791ab-175">右ウィンドウの **要件** タブで、**要件を追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="791ab-175">In the right pane, on the **Requirements** tab, select **Add requirement**.</span></span>
3. <span data-ttu-id="791ab-176">名前、説明、およびタイプを入力し、次に **作成** を選択します。</span><span class="sxs-lookup"><span data-stu-id="791ab-176">Enter a name, description, and type, and then select **Create**.</span></span>

    <span data-ttu-id="791ab-177">Azure DevOps では、現在の業務プロセスに関連付けられている要求作業項目が作成されます。</span><span class="sxs-lookup"><span data-stu-id="791ab-177">In Azure DevOps, a requirement work item is created that is associated with the current business process.</span></span>

<span data-ttu-id="791ab-178">現在の業務プロセスに関連付けられている Azure DevOps 作業項目に移動するには、**要件** タブで適切なリンクを選択します。</span><span class="sxs-lookup"><span data-stu-id="791ab-178">To go to the Azure DevOps work items that are associated with the current business process, on the **Requirements** tab, select the appropriate links.</span></span>

## <a name="common-syncing-errors"></a><span data-ttu-id="791ab-179">一般的な同期エラー</span><span class="sxs-lookup"><span data-stu-id="791ab-179">Common syncing errors</span></span>

<span data-ttu-id="791ab-180">BPM から Azure DevOps への同期が失敗した場合、失敗したプロセス名、作業項目の種類、およびエラー メッセージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="791ab-180">If the BPM to Azure DevOps synchronization fails, you will see the failed process name, work item type, and an error message.</span></span> 

![BPM 同期エラー](./media/BPMsyncError.jpg)

<span data-ttu-id="791ab-182">ここでいくつか一般的な原因と、エラーを解決するために推奨するアクションを示します。</span><span class="sxs-lookup"><span data-stu-id="791ab-182">Here are some common causes and suggested actions to resolve the error.</span></span>

| <span data-ttu-id="791ab-183">**考えられる原因**</span><span class="sxs-lookup"><span data-stu-id="791ab-183">**Possible cause**</span></span> | <span data-ttu-id="791ab-184">**エラー メッセージ**</span><span class="sxs-lookup"><span data-stu-id="791ab-184">**Error message**</span></span> | <span data-ttu-id="791ab-185">**推奨される解決策**</span><span class="sxs-lookup"><span data-stu-id="791ab-185">**Suggested solution**</span></span> | 
|---------|--------|--------|
| <span data-ttu-id="791ab-186">必須フィールドが追加されました</span><span class="sxs-lookup"><span data-stu-id="791ab-186">Required field added</span></span> | <span data-ttu-id="791ab-187">作業項目の作成に失敗しました。</span><span class="sxs-lookup"><span data-stu-id="791ab-187">Failed to create work item.</span></span> <span data-ttu-id="791ab-188">必須フィールドがこの作業項目の種類に追加されましたが、サポートされていません。</span><span class="sxs-lookup"><span data-stu-id="791ab-188">A required field has been added to this work item type, which is not supported.</span></span> <span data-ttu-id="791ab-189">この要件を削除するか、プロセス テンプレートで既定値を提供して、操作をブロック解除します。</span><span class="sxs-lookup"><span data-stu-id="791ab-189">Remove this requirement or provide a default value in the process template to unblock the operation.</span></span> | <span data-ttu-id="791ab-190">必須フィールドを削除するか、既定値を提供します。</span><span class="sxs-lookup"><span data-stu-id="791ab-190">Remove the required field or provide a default value.</span></span> | 
| <span data-ttu-id="791ab-191">作業項目の種類が無効です</span><span class="sxs-lookup"><span data-stu-id="791ab-191">Work item type disabled</span></span> | <span data-ttu-id="791ab-192">作業項目の作成に失敗しました。</span><span class="sxs-lookup"><span data-stu-id="791ab-192">Failed to create work item.</span></span> <span data-ttu-id="791ab-193">作業項目の種類がプロセス テンプレートで無効になっています。</span><span class="sxs-lookup"><span data-stu-id="791ab-193">The work item type has been disabled in the process template.</span></span> <span data-ttu-id="791ab-194">作業項目の種類を有効にして、操作をブロック解除します。</span><span class="sxs-lookup"><span data-stu-id="791ab-194">Enable the work item type to unblock the operation.</span></span> | <span data-ttu-id="791ab-195">作業項目の種類をプロセス テンプレートで有効にします。</span><span class="sxs-lookup"><span data-stu-id="791ab-195">Enable the work item type in the process template</span></span> |  
| <span data-ttu-id="791ab-196">更新する作業項目が見つかりませんでした</span><span class="sxs-lookup"><span data-stu-id="791ab-196">Couldn't find work item to update</span></span> | <span data-ttu-id="791ab-197">作業項目の更新に失敗しました。</span><span class="sxs-lookup"><span data-stu-id="791ab-197">Failed to update work item.</span></span> <span data-ttu-id="791ab-198">作業項目が存在しないか、読み取るためのアクセス許可がありません。</span><span class="sxs-lookup"><span data-stu-id="791ab-198">The work item does not exist, or you do not have permissions to read it.</span></span> <span data-ttu-id="791ab-199">プロジェクト設定で PAT コンフィギュレーションを確認するか、作業項目が DevOps プロジェクトから直接削除されている場合は作業項目を復元します。</span><span class="sxs-lookup"><span data-stu-id="791ab-199">Check the PAT configuration in the project settings or restore the work item if it has been deleted directly from the DevOps project.</span></span> | <span data-ttu-id="791ab-200">削除された場合はごみ箱から作業項目を復元するか、新しい個人用アクセス トークン (PAT) を作成して完全なアクセス許可があることを確認します。</span><span class="sxs-lookup"><span data-stu-id="791ab-200">Restore the work item from the recycle bin if it was deleted, or create a new Personal Access Token (PAT) and make sure that it has full permissions.</span></span> |  
| <span data-ttu-id="791ab-201">個人用アクセス トークンの期限が切れています</span><span class="sxs-lookup"><span data-stu-id="791ab-201">Personal Access Token is expired</span></span> | <span data-ttu-id="791ab-202">Visual Studio Team Services との同期に失敗しました。</span><span class="sxs-lookup"><span data-stu-id="791ab-202">Failed to sync with Visual Studio Team Services.</span></span> <span data-ttu-id="791ab-203">要求応答は次のとおりです: 無許可。</span><span class="sxs-lookup"><span data-stu-id="791ab-203">The request response is: Unauthorized.</span></span> <span data-ttu-id="791ab-204">PAT が正しく設定されていてまだ有効なことを確認し、エラーが引き続き発生する場合は再試行してサポートに連絡してください。</span><span class="sxs-lookup"><span data-stu-id="791ab-204">Please check that the PAT is setup correctly and still valid, try again and contact support if the error persists.</span></span> | <span data-ttu-id="791ab-205">Azure DevOps から新しい個人用アクセス トークン (PAT) を作成し、LCS プロジェクト設定で PAT 値を更新します。</span><span class="sxs-lookup"><span data-stu-id="791ab-205">Create a new Personal Access Token (PAT) from Azure DevOps and update the PAT value in your LCS Project settings.</span></span> | 
| <span data-ttu-id="791ab-206">一般的なエラー</span><span class="sxs-lookup"><span data-stu-id="791ab-206">Generic error</span></span> | <span data-ttu-id="791ab-207">Visual Studio Team Services との同期に失敗しました。</span><span class="sxs-lookup"><span data-stu-id="791ab-207">Failed to sync with Visual Studio Team Services.</span></span> <span data-ttu-id="791ab-208">要求応答は次のとおりです: {0}。</span><span class="sxs-lookup"><span data-stu-id="791ab-208">The request response is: {0}.</span></span> <span data-ttu-id="791ab-209">PAT が正しく設定されていてまだ有効なことを確認し、エラーが引き続き発生する場合は再試行してサポートに連絡してください。</span><span class="sxs-lookup"><span data-stu-id="791ab-209">Please check that the PAT is setup correctly and still valid, try again and contact support if the error persists.</span></span> | <span data-ttu-id="791ab-210">同期エラーの原因となった要求応答で、顧客サポートに問い合わせてください。</span><span class="sxs-lookup"><span data-stu-id="791ab-210">Contact customer support with the request response that caused the syncing error.</span></span> | 


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]