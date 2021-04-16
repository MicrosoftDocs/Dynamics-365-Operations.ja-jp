---
title: 在庫仕訳帳の承認ワークフロー
description: このトピックでは、さまざまな種類の現物在庫取引の在庫仕訳帳の承認ワークフローを設定方法と使用方法について説明します。 在庫仕訳帳のワークフローは、承認済の在庫仕訳帳のみをトランザクションに転記できるようにするのに役立ちます。
author: sherry-zheng
ms.date: 07/21/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventJournalTableWorkflowDropDialog
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2020-07-21
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: b53ecec4bb7593cb0a0cae72e4132c49d6ec6a68
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/01/2021
ms.locfileid: "5826014"
---
# <a name="inventory-journal-approval-workflows"></a><span data-ttu-id="e9461-104">在庫仕訳帳の承認ワークフロー</span><span class="sxs-lookup"><span data-stu-id="e9461-104">Inventory journal approval workflows</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e9461-105">このトピックでは、発行および領収書、在庫移動、部品表 (BOM)、および物理的な在庫の調整など、さまざまなタイプの現物在庫取引で使用する在庫仕訳帳のワークフローを設定して使用する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="e9461-105">This topic describes how to set up and use inventory journal approval workflows for various types of physical inventory transactions, such as issues and receipts, inventory movements, bills of materials (BOMs), and the reconciliation of physical inventory.</span></span> <span data-ttu-id="e9461-106">在庫仕訳帳のワークフローは、承認済の在庫仕訳帳のみをトランザクションに転記できるようにするのに役立ちます。</span><span class="sxs-lookup"><span data-stu-id="e9461-106">Inventory journal workflows help ensure that only approved inventory journals can be posted to transactions.</span></span>

> [!NOTE]
> <span data-ttu-id="e9461-107">在庫仕訳帳のワークフローは、在庫管理モジュールを使用して記録された取引にのみ適用されます。</span><span class="sxs-lookup"><span data-stu-id="e9461-107">Inventory journal approval workflows apply only to transactions recorded using the Inventory Management module.</span></span> <span data-ttu-id="e9461-108">倉庫管理モジュールからトリガーされた在庫仕訳帳では動作しません。</span><span class="sxs-lookup"><span data-stu-id="e9461-108">They don't work with inventory journals triggered from the Warehouse Management module.</span></span>

## <a name="turn-on-the-inventory-journal-approval-workflows-feature"></a><span data-ttu-id="e9461-109">在庫仕訳帳の承認ワークフロー機能をオンにする</span><span class="sxs-lookup"><span data-stu-id="e9461-109">Turn on the inventory journal approval workflows feature</span></span>

<span data-ttu-id="e9461-110">この機能を使用するには、システム上で有効にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="e9461-110">Before you can use this feature, it must be turned on in your system.</span></span> <span data-ttu-id="e9461-111">管理者は、[機能管理](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) 設定を使用して、機能の状態を確認し、有効にすることができます。</span><span class="sxs-lookup"><span data-stu-id="e9461-111">Admins can use the [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) settings to check the status of the feature and turn it on.</span></span> <span data-ttu-id="e9461-112">**機能管理** ワークスペースで、この機能は次のようにリストされています。</span><span class="sxs-lookup"><span data-stu-id="e9461-112">In the **Feature management** workspace, the feature is listed in the following way:</span></span>

- <span data-ttu-id="e9461-113">**モジュール:** *在庫と倉庫管理*</span><span class="sxs-lookup"><span data-stu-id="e9461-113">**Module:** *Inventory and warehouse management*</span></span>
- <span data-ttu-id="e9461-114">**機能名:** *在庫仕訳帳承認ワークフロー*</span><span class="sxs-lookup"><span data-stu-id="e9461-114">**Feature name:** *Inventory journal approve workflow*</span></span>

## <a name="create-your-inventory-journal-approval-workflows"></a><span data-ttu-id="e9461-115">在庫仕訳帳の承認ワークフローの作成</span><span class="sxs-lookup"><span data-stu-id="e9461-115">Create your inventory journal approval workflows</span></span>

<span data-ttu-id="e9461-116">この機能を設定するには、制御対象とする在庫の仕訳タイプごとにワークフローを作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="e9461-116">To set up this feature, you must create a workflow for each of the inventory journal types you want to control.</span></span> <span data-ttu-id="e9461-117">在庫仕訳帳のタイプごとに異なる承認階層とワークフローのステップを持つことができるため、在庫仕訳帳のタイプごとに個別のワークフローを構成することができます。</span><span class="sxs-lookup"><span data-stu-id="e9461-117">Because different inventory journal types can have different approval hierarchies and workflow steps, you can configure individual workflows for each inventory journal type.</span></span>

<span data-ttu-id="e9461-118">ワークフローはバージョン管理に対応しており、それぞれにワークフロー IDとアクティブなバージョンが存在します。</span><span class="sxs-lookup"><span data-stu-id="e9461-118">Workflows support version control, and each has a workflow ID and an active version.</span></span> <span data-ttu-id="e9461-119">新たなワークフローのそれぞれのバージョンは、作成時にすぐにアクティブにするか、非アクティブのままにするかを選択できます。</span><span class="sxs-lookup"><span data-stu-id="e9461-119">You can choose to activate each new workflow version immediately upon creation or keep it inactive.</span></span> <span data-ttu-id="e9461-120">同じ仕訳帳のタイプに対して異なるワークフローが必要な場合は、当該の仕訳帳タイプに対して複数のワークフローを作成し、それぞれのワークフローをそのタイプで使用する別の仕訳帳名に割り当てます。</span><span class="sxs-lookup"><span data-stu-id="e9461-120">If you need different workflows for the same journal type, then create multiple workflows for that journal type, and then assign each of these to a different journal name that uses that type.</span></span>

<span data-ttu-id="e9461-121">在庫仕訳帳の承認ワークフローの作成方法 :</span><span class="sxs-lookup"><span data-stu-id="e9461-121">To create your inventory journal approval workflows:</span></span>

1. <span data-ttu-id="e9461-122">**在庫管理 \> 設定\> 在庫管理ワークフロー** に移動します。</span><span class="sxs-lookup"><span data-stu-id="e9461-122">Go to **Inventory Management \> Setup\> Inventory management workflows**.</span></span>
1. <span data-ttu-id="e9461-123">アクション ウィンドウで、**新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="e9461-123">Select **New** on the Action Pane.</span></span>
1. <span data-ttu-id="e9461-124">ワークフローを設定する在庫仕訳帳のタイプを選択します :</span><span class="sxs-lookup"><span data-stu-id="e9461-124">Choose the inventory journal type for which you want to set up a workflow:</span></span>
    - <span data-ttu-id="e9461-125">**在庫タグ集計仕訳帳**</span><span class="sxs-lookup"><span data-stu-id="e9461-125">**Inventory tag counting journal**</span></span>
    - <span data-ttu-id="e9461-126">**在庫所有権変更仕訳**</span><span class="sxs-lookup"><span data-stu-id="e9461-126">**Inventory ownership change journal**</span></span>
    - <span data-ttu-id="e9461-127">**在庫移動仕訳帳**</span><span class="sxs-lookup"><span data-stu-id="e9461-127">**Inventory movement journal**</span></span>
    - <span data-ttu-id="e9461-128">**在庫移動仕訳帳**</span><span class="sxs-lookup"><span data-stu-id="e9461-128">**Inventory transfer journal**</span></span>
    - <span data-ttu-id="e9461-129">**在庫集計仕訳帳**</span><span class="sxs-lookup"><span data-stu-id="e9461-129">**Inventory counting journal**</span></span>
    - <span data-ttu-id="e9461-130">**在庫 BOM 仕訳帳**</span><span class="sxs-lookup"><span data-stu-id="e9461-130">**Inventory BOM journal**</span></span>
    - <span data-ttu-id="e9461-131">**在庫調整仕訳帳**</span><span class="sxs-lookup"><span data-stu-id="e9461-131">**Inventory adjustment journal**</span></span>

    <span data-ttu-id="e9461-132">![作成ワークフロー ダイアログ ボックス](media/journal-workflow-create-workflow.png "作成ワークフロー ダイアログ ボックス")</span><span class="sxs-lookup"><span data-stu-id="e9461-132">![The Create workflow dialog box](media/journal-workflow-create-workflow.png "The Create workflow dialog box")</span></span>

1. <span data-ttu-id="e9461-133">ワークフロー エディタ アプリがマシン上で起動します。</span><span class="sxs-lookup"><span data-stu-id="e9461-133">The workflow editor app launches on your machine.</span></span> <span data-ttu-id="e9461-134">(このアクションの承認が要求される場合があります。)必要に応じてワークフローの設計に利用してください。</span><span class="sxs-lookup"><span data-stu-id="e9461-134">(You may be asked to approve this action.) Use it to design your workflow as needed.</span></span> <span data-ttu-id="e9461-135">ワークフロー エディターの使用方法については、[ワークフロー システムの概要](../../fin-ops-core/fin-ops/organization-administration/overview-workflow-system.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="e9461-135">For details about how to use the workflow editor, see [Workflow system overview](../../fin-ops-core/fin-ops/organization-administration/overview-workflow-system.md).</span></span>
1. <span data-ttu-id="e9461-136">ワークフロー エディター アプリを保存して閉じた後、このワーク フローのバージョンをアクティブにするか、非アクティブのままにしておくかを選択する必要があります。</span><span class="sxs-lookup"><span data-stu-id="e9461-136">After saving and closing the workflow editor app, you must choose whether to activate this workflow version or keep it as inactivate.</span></span>

> [!NOTE]
> <span data-ttu-id="e9461-137">ワークフローではバージョン管理を提供しており、作成したバージョンの一覧を表示し、どのバージョンがアクティブであるかを選択できます。</span><span class="sxs-lookup"><span data-stu-id="e9461-137">Workflows provide version control, which means that you can view a list of versions you have created and choose which one is active.</span></span> <span data-ttu-id="e9461-138">利用可能なバージョンのリストを表示し、どのバージョンを有効化するかを選択するには、**在庫管理ワークフロー** ページに一覧表示されているワークフローを選択します。</span><span class="sxs-lookup"><span data-stu-id="e9461-138">To view the list of available versions and choose which to activate, select a workflow listed on the **Inventory management workflows** page.</span></span> <span data-ttu-id="e9461-139">[アクション] ペインで、**ワークフロー** タブを開き、**バージョン** を選択します。</span><span class="sxs-lookup"><span data-stu-id="e9461-139">On the Action Pane, open the **Workflow** tab, and select **Versions**.</span></span> <span data-ttu-id="e9461-140">各ワークフロー ID に対しては、一度に 1 つのバージョンのみをアクティブにすることができます。</span><span class="sxs-lookup"><span data-stu-id="e9461-140">Only one version can be active at a time for each workflow ID.</span></span>

## <a name="assign-approval-workflows-to-inventory-journal-names"></a><span data-ttu-id="e9461-141">在庫仕訳帳に承認ワークフローを割り当てる</span><span class="sxs-lookup"><span data-stu-id="e9461-141">Assign approval workflows to inventory journal names</span></span>

<span data-ttu-id="e9461-142">次に、各在庫仕訳帳の名称に在庫仕訳帳のワークフローを割り当てます。</span><span class="sxs-lookup"><span data-stu-id="e9461-142">The next step is to assign a inventory journal workflow to each inventory journal name.</span></span> <span data-ttu-id="e9461-143">在庫仕訳帳の種類ごとに、複数の在庫仕訳帳名を設定することができます。</span><span class="sxs-lookup"><span data-stu-id="e9461-143">For each inventory journal type, you can set up multiple inventory journal names.</span></span>

<span data-ttu-id="e9461-144">在庫仕訳帳のワークフローと在庫仕訳帳名を関連付ける方法 :</span><span class="sxs-lookup"><span data-stu-id="e9461-144">To associate an inventory journal workflow with an inventory journal name:</span></span>

1. <span data-ttu-id="e9461-145">**在庫管理 \> 設定 \> 在庫仕訳帳名 \> 在庫** に移動します。</span><span class="sxs-lookup"><span data-stu-id="e9461-145">Go to **Inventory management \> Setup \> Journal names \> Inventory**.</span></span>
1. <span data-ttu-id="e9461-146">リスト列から仕訳帳名を選択すると、設定ページが表示されます。</span><span class="sxs-lookup"><span data-stu-id="e9461-146">Select a journal name from the list column to open its settings page.</span></span>
1. <span data-ttu-id="e9461-147">**全般** クイック タブ で、**承認ワークフロー** を **はい** に設定します。</span><span class="sxs-lookup"><span data-stu-id="e9461-147">On the **General** FastTab, set **Approval workflow** to **Yes**.</span></span> <span data-ttu-id="e9461-148">アクションの承認を求めるメッセージが表示されたら、**はい** を選択します。</span><span class="sxs-lookup"><span data-stu-id="e9461-148">If you are prompted to approve the action, select **Yes**.</span></span>

    <span data-ttu-id="e9461-149">![仕訳帳名にワークフローを割り当てる](media/journal-workflow-journal-name.png "仕訳帳名にワークフローを割り当てる")</span><span class="sxs-lookup"><span data-stu-id="e9461-149">![Assign a workflow to a journal name](media/journal-workflow-journal-name.png "Assign a workflow to a journal name")</span></span>

1. <span data-ttu-id="e9461-150">**ワークフロー** のドロップダウン リストを開き、承認ワークフローを選択します。</span><span class="sxs-lookup"><span data-stu-id="e9461-150">Open the **Workflow** drop-down list and select the appropriate workflow.</span></span> <span data-ttu-id="e9461-151">このリストには、ワークフロー エディター アプリを使用して作成したそれぞれのアクティブなワークフローが表示されます。</span><span class="sxs-lookup"><span data-stu-id="e9461-151">The list shows each active workflow that you have created using the workflow editor app.</span></span>

## <a name="create-an-inventory-journal-and-send-it-for-approval"></a><span data-ttu-id="e9461-152">在庫仕訳帳を作成して送信し、承認を得る</span><span class="sxs-lookup"><span data-stu-id="e9461-152">Create an inventory journal and send it for approval</span></span>

<span data-ttu-id="e9461-153">在庫仕訳帳名と一致する在庫仕訳帳の承認ワークフローを関連付けた後、その名前を使用して新しい在庫仕訳帳を作成し、ワークフローを使用してこれらの仕訳帳を送信し、承認を得ることができます。</span><span class="sxs-lookup"><span data-stu-id="e9461-153">After you associate an inventory journal name with its matching inventory journal approval workflow, you'll be able to create new inventory journals that use that name and then send these journals for approval using that workflow.</span></span> <span data-ttu-id="e9461-154">ワークフローで設定した承認者が承認すまでは、在庫仕訳帳を投稿することはできません。</span><span class="sxs-lookup"><span data-stu-id="e9461-154">You won't be able post the inventory journal until it has been approved by the approvers configured in the workflow.</span></span>

1. <span data-ttu-id="e9461-155">ナビゲーション ウィンドウで、**在庫管理 \> 仕訳帳の入力 \> 項目** を展開し、在庫仕訳帳のタイプを選択します。</span><span class="sxs-lookup"><span data-stu-id="e9461-155">On the navigation pane, expand **Inventory management \> Journal entries \> Items** and then select an inventory journal type.</span></span>
1. <span data-ttu-id="e9461-156">**新規** を選択して、選択したタイプの新しい仕訳帳を作成します。</span><span class="sxs-lookup"><span data-stu-id="e9461-156">Select **New** to create a new journal of your selected type.</span></span>
1. <span data-ttu-id="e9461-157">**在庫仕訳帳の作成** ダイアログ ボックスが開きます。</span><span class="sxs-lookup"><span data-stu-id="e9461-157">The **Create inventory journal** dialog box opens.</span></span> <span data-ttu-id="e9461-158">必要に応じてフォームに入力し、**OK** を選択して仕訳帳を保存します。</span><span class="sxs-lookup"><span data-stu-id="e9461-158">Fill out the form as needed and then select **OK** to save the journal.</span></span>
1. <span data-ttu-id="e9461-159">必要に応じて仕訳帳を完成させます。</span><span class="sxs-lookup"><span data-stu-id="e9461-159">Complete the journal as required.</span></span>
1. <span data-ttu-id="e9461-160">承認ワークフローに関連付けられた在庫仕訳帳を作成、または開くと、アクション ペインで **ワークフロー** ボタンがアクティブになります。</span><span class="sxs-lookup"><span data-stu-id="e9461-160">When you create or open an inventory journal with an approval workflow associated with it, the **Workflow** button will be active in the Action Pane.</span></span> <span data-ttu-id="e9461-161">承認のために仕訳帳を送信する準備ができたら、**ワークフロー** ボタンを選択してドロップダウン ダイアログ ボックスを開き、**送信** を選択します。</span><span class="sxs-lookup"><span data-stu-id="e9461-161">When you are ready to submit the journal for approval, select the **Workflow** button to open a drop-down dialog box and then select **Submit**.</span></span> <span data-ttu-id="e9461-162">承認要求が関連する承認者に送信されます。この承認者にはワークフローで設定された通知方法を使用して通知がされます。</span><span class="sxs-lookup"><span data-stu-id="e9461-162">The approval request will then route to the relevant approver, who will be alerted using the notification method configured for the workflow.</span></span>

    <span data-ttu-id="e9461-163">![承認のために仕訳帳を送信する](media/journal-workflow-inventory-journal.png "承認のために仕訳帳を送信する")</span><span class="sxs-lookup"><span data-stu-id="e9461-163">![Submit a journal for approval](media/journal-workflow-inventory-journal.png "Submit a journal for approval")</span></span>

<span data-ttu-id="e9461-164">承認要求を取り消すには、該当する仕訳帳を開き、**ワークフロー** ボタンを選択し、**取り消し** を選択します。</span><span class="sxs-lookup"><span data-stu-id="e9461-164">To recall an approval request, open the relevant journal, select the **Workflow** button and then select **Recall**.</span></span> <span data-ttu-id="e9461-165">これにより、ワークフローがリセットされます。</span><span class="sxs-lookup"><span data-stu-id="e9461-165">This will reset the workflow.</span></span>

<span data-ttu-id="e9461-166">仕訳帳が承認されると、投稿できるようになります。</span><span class="sxs-lookup"><span data-stu-id="e9461-166">When your journal has been approved, you'll be able to post it.</span></span> <span data-ttu-id="e9461-167">仕訳帳を投稿するには、アクション ペインから **投稿** を選択します。</span><span class="sxs-lookup"><span data-stu-id="e9461-167">To post the journal, select **Post** from the Action Pane.</span></span> <span data-ttu-id="e9461-168">**投稿** ボタンがアクティブになっていない場合は、仕訳帳がまだ承認されていないことを意味します。</span><span class="sxs-lookup"><span data-stu-id="e9461-168">If the **Post** button isn't active the journal hasn't been approved yet.</span></span>

## <a name="respond-to-an-inventory-journal-approval-request"></a><span data-ttu-id="e9461-169">在庫仕訳帳の承認要求に応答する</span><span class="sxs-lookup"><span data-stu-id="e9461-169">Respond to an inventory journal approval request</span></span>

<span data-ttu-id="e9461-170">あなたが承認者の場合は、承認が必要になるたびにメッセージを受け取ることになります (関連するワークフローで設定されています)。</span><span class="sxs-lookup"><span data-stu-id="e9461-170">If you are an approver, you should receive a message each time your approval is needed (as configured in the relevant workflow).</span></span> <span data-ttu-id="e9461-171">その後、仕訳帳の承認要求を承認または拒否するには、以下の操作を行います :</span><span class="sxs-lookup"><span data-stu-id="e9461-171">Then you can approve or reject a journal approval request by doing the following:</span></span>

1. <span data-ttu-id="e9461-172">ナビゲーション ウィンドウで、**在庫管理 \> 仕訳帳の入力 \> 項目** を展開し、在庫仕訳帳のタイプを選択します。</span><span class="sxs-lookup"><span data-stu-id="e9461-172">On the navigation pane, expand **Inventory management \> Journal entries \> Items** and then select an inventory journal type.</span></span>
1. <span data-ttu-id="e9461-173">関連する仕訳帳を開き、確認します。</span><span class="sxs-lookup"><span data-stu-id="e9461-173">Open the relevant journal and review it.</span></span>
1. <span data-ttu-id="e9461-174">アクションペインの **ワークフロー** ボタンを選択すると、ドロップダウン ダイアログ ボックスが開きます。</span><span class="sxs-lookup"><span data-stu-id="e9461-174">Select the **Workflow** button on the Action Pane to open a drop-down dialog box.</span></span> <span data-ttu-id="e9461-175">次のいずれかを選択してください。</span><span class="sxs-lookup"><span data-stu-id="e9461-175">Select one of the following:</span></span>
    - <span data-ttu-id="e9461-176">**承認** - 申請を承認します。</span><span class="sxs-lookup"><span data-stu-id="e9461-176">**Approve** - To approve the request.</span></span>
    - <span data-ttu-id="e9461-177">**拒否**  - 申請を否認します。</span><span class="sxs-lookup"><span data-stu-id="e9461-177">**Reject** - To reject the reject the request.</span></span>
    - <span data-ttu-id="e9461-178">**その他 \> 要求の変更** - 依頼元にメッセージを送信して、特定の内容を変更してから再提出するように依頼します。</span><span class="sxs-lookup"><span data-stu-id="e9461-178">**More \> Request change** - To send a message to the requester asking them to change something specific and then resubmit.</span></span>
    - <span data-ttu-id="e9461-179">**その他 \> 代理** - 承認を他のユーザーに委任します。</span><span class="sxs-lookup"><span data-stu-id="e9461-179">**More \> Delegate** - To delegate the approval to another user.</span></span>
    - <span data-ttu-id="e9461-180">**その他 \> 取り消し** - 承認要求を取り消します (ワークフローがリセットされます)。</span><span class="sxs-lookup"><span data-stu-id="e9461-180">**More \> Recall** - To recall the approval request (resets the workflow).</span></span>
    - <span data-ttu-id="e9461-181">**その他 \> ワークフロー履歴** - これまでの承認ワークフローの履歴を参照します。</span><span class="sxs-lookup"><span data-stu-id="e9461-181">**More \> Workflow history** - To view the history of this approval workflow so far.</span></span>

## <a name="review-the-approval-history"></a><span data-ttu-id="e9461-182">承認の履歴を確認する</span><span class="sxs-lookup"><span data-stu-id="e9461-182">Review the approval history</span></span>

<span data-ttu-id="e9461-183">他のタイプのワークフローと同様に、**ワークフローの履歴** ページを使用して、任意の仕訳帳の承認ワークフローの履歴を表示することができます。</span><span class="sxs-lookup"><span data-stu-id="e9461-183">As with other types of workflows, you can use the **Workflow history** page to view the approval workflow history for any journal.</span></span>

<span data-ttu-id="e9461-184">仕訳帳のワークフロー履歴を確認します。</span><span class="sxs-lookup"><span data-stu-id="e9461-184">To review the workflow history for a journal:</span></span>

1. <span data-ttu-id="e9461-185">ナビゲーション ウィンドウで、**在庫管理 \> 仕訳帳の入力 \> 項目** を展開し、在庫仕訳帳のタイプを選択します。</span><span class="sxs-lookup"><span data-stu-id="e9461-185">On the navigation pane, expand **Inventory management \> Journal entries \> Items** and then select an inventory journal type.</span></span>
1. <span data-ttu-id="e9461-186">関連する仕訳を開きます。</span><span class="sxs-lookup"><span data-stu-id="e9461-186">Open the relevant journal.</span></span>
1. <span data-ttu-id="e9461-187">アクションペインの **ワークフロー** ボタンを選択すると、ドロップダウン ダイアログ ボックスが開きます。</span><span class="sxs-lookup"><span data-stu-id="e9461-187">Select the **Workflow** button on the Action Pane to open a drop-down dialog box.</span></span> <span data-ttu-id="e9461-188">**ワークフロー履歴** を選択します。</span><span class="sxs-lookup"><span data-stu-id="e9461-188">Select **Workflow history**.</span></span> <span data-ttu-id="e9461-189">詳細については、[ワークフロー履歴を確認する](../../fin-ops-core/fin-ops/organization-administration/tasks/view-workflow-history.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="e9461-189">For more information, see [View workflow history](../../fin-ops-core/fin-ops/organization-administration/tasks/view-workflow-history.md).</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]