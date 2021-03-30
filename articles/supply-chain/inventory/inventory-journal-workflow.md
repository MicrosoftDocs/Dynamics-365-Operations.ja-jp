---
title: 在庫仕訳帳の承認ワークフロー
description: このトピックでは、さまざまな種類の現物在庫取引の在庫仕訳帳の承認ワークフローを設定方法と使用方法について説明します。 在庫仕訳帳のワークフローは、承認済の在庫仕訳帳のみをトランザクションに転記できるようにするのに役立ちます。
author: sherry-zheng
manager: tfehr
ms.date: 07/21/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventJournalTableWorkflowDropDialog
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2020-07-21
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: 596182dfd7430e4d1e35ffebb795fbcf98d45e33
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/15/2021
ms.locfileid: "5247913"
---
# <a name="inventory-journal-approval-workflows"></a><span data-ttu-id="f46be-104">在庫仕訳帳の承認ワークフロー</span><span class="sxs-lookup"><span data-stu-id="f46be-104">Inventory journal approval workflows</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f46be-105">このトピックでは、発行および領収書、在庫移動、部品表 (BOM)、および物理的な在庫の調整など、さまざまなタイプの現物在庫取引で使用する在庫仕訳帳のワークフローを設定して使用する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="f46be-105">This topic describes how to set up and use inventory journal approval workflows for various types of physical inventory transactions, such as issues and receipts, inventory movements, bills of materials (BOMs), and the reconciliation of physical inventory.</span></span> <span data-ttu-id="f46be-106">在庫仕訳帳のワークフローは、承認済の在庫仕訳帳のみをトランザクションに転記できるようにするのに役立ちます。</span><span class="sxs-lookup"><span data-stu-id="f46be-106">Inventory journal workflows help ensure that only approved inventory journals can be posted to transactions.</span></span>

> [!NOTE]
> <span data-ttu-id="f46be-107">在庫仕訳帳のワークフローは、在庫管理モジュールを使用して記録された取引にのみ適用されます。</span><span class="sxs-lookup"><span data-stu-id="f46be-107">Inventory journal approval workflows apply only to transactions recorded using the Inventory Management module.</span></span> <span data-ttu-id="f46be-108">倉庫管理モジュールからトリガーされた在庫仕訳帳では動作しません。</span><span class="sxs-lookup"><span data-stu-id="f46be-108">They don't work with inventory journals triggered from the Warehouse Management module.</span></span>

## <a name="turn-on-the-inventory-journal-approval-workflows-feature"></a><span data-ttu-id="f46be-109">在庫仕訳帳の承認ワークフロー機能をオンにする</span><span class="sxs-lookup"><span data-stu-id="f46be-109">Turn on the inventory journal approval workflows feature</span></span>

<span data-ttu-id="f46be-110">この機能を使用するには、システム上で有効にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="f46be-110">Before you can use this feature, it must be turned on in your system.</span></span> <span data-ttu-id="f46be-111">管理者は、[機能管理](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) 設定を使用して、機能の状態を確認し、有効にすることができます。</span><span class="sxs-lookup"><span data-stu-id="f46be-111">Admins can use the [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) settings to check the status of the feature and turn it on.</span></span> <span data-ttu-id="f46be-112">**機能管理** ワークスペースで、この機能は次のようにリストされています。</span><span class="sxs-lookup"><span data-stu-id="f46be-112">In the **Feature management** workspace, the feature is listed in the following way:</span></span>

- <span data-ttu-id="f46be-113">**モジュール:** *在庫と倉庫管理*</span><span class="sxs-lookup"><span data-stu-id="f46be-113">**Module:** *Inventory and warehouse management*</span></span>
- <span data-ttu-id="f46be-114">**機能名:** *在庫仕訳帳承認ワークフロー*</span><span class="sxs-lookup"><span data-stu-id="f46be-114">**Feature name:** *Inventory journal approve workflow*</span></span>

## <a name="create-your-inventory-journal-approval-workflows"></a><span data-ttu-id="f46be-115">在庫仕訳帳の承認ワークフローの作成</span><span class="sxs-lookup"><span data-stu-id="f46be-115">Create your inventory journal approval workflows</span></span>

<span data-ttu-id="f46be-116">この機能を設定するには、制御対象とする在庫の仕訳タイプごとにワークフローを作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="f46be-116">To set up this feature, you must create a workflow for each of the inventory journal types you want to control.</span></span> <span data-ttu-id="f46be-117">在庫仕訳帳のタイプごとに異なる承認階層とワークフローのステップを持つことができるため、在庫仕訳帳のタイプごとに個別のワークフローを構成することができます。</span><span class="sxs-lookup"><span data-stu-id="f46be-117">Because different inventory journal types can have different approval hierarchies and workflow steps, you can configure individual workflows for each inventory journal type.</span></span>

<span data-ttu-id="f46be-118">ワークフローはバージョン管理に対応しており、それぞれにワークフロー IDとアクティブなバージョンが存在します。</span><span class="sxs-lookup"><span data-stu-id="f46be-118">Workflows support version control, and each has a workflow ID and an active version.</span></span> <span data-ttu-id="f46be-119">新たなワークフローのそれぞれのバージョンは、作成時にすぐにアクティブにするか、非アクティブのままにするかを選択できます。</span><span class="sxs-lookup"><span data-stu-id="f46be-119">You can choose to activate each new workflow version immediately upon creation or keep it inactive.</span></span> <span data-ttu-id="f46be-120">同じ仕訳帳のタイプに対して異なるワークフローが必要な場合は、当該の仕訳帳タイプに対して複数のワークフローを作成し、それぞれのワークフローをそのタイプで使用する別の仕訳帳名に割り当てます。</span><span class="sxs-lookup"><span data-stu-id="f46be-120">If you need different workflows for the same journal type, then create multiple workflows for that journal type, and then assign each of these to a different journal name that uses that type.</span></span>

<span data-ttu-id="f46be-121">在庫仕訳帳の承認ワークフローの作成方法 :</span><span class="sxs-lookup"><span data-stu-id="f46be-121">To create your inventory journal approval workflows:</span></span>

1. <span data-ttu-id="f46be-122">**在庫管理 \> 設定\> 在庫管理ワークフロー** に移動します。</span><span class="sxs-lookup"><span data-stu-id="f46be-122">Go to **Inventory Management \> Setup\> Inventory management workflows**.</span></span>
1. <span data-ttu-id="f46be-123">アクション ウィンドウで、**新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="f46be-123">Select **New** on the Action Pane.</span></span>
1. <span data-ttu-id="f46be-124">ワークフローを設定する在庫仕訳帳のタイプを選択します :</span><span class="sxs-lookup"><span data-stu-id="f46be-124">Choose the inventory journal type for which you want to set up a workflow:</span></span>
    - <span data-ttu-id="f46be-125">**在庫タグ集計仕訳帳**</span><span class="sxs-lookup"><span data-stu-id="f46be-125">**Inventory tag counting journal**</span></span>
    - <span data-ttu-id="f46be-126">**在庫所有権変更仕訳**</span><span class="sxs-lookup"><span data-stu-id="f46be-126">**Inventory ownership change journal**</span></span>
    - <span data-ttu-id="f46be-127">**在庫移動仕訳帳**</span><span class="sxs-lookup"><span data-stu-id="f46be-127">**Inventory movement journal**</span></span>
    - <span data-ttu-id="f46be-128">**在庫移動仕訳帳**</span><span class="sxs-lookup"><span data-stu-id="f46be-128">**Inventory transfer journal**</span></span>
    - <span data-ttu-id="f46be-129">**在庫集計仕訳帳**</span><span class="sxs-lookup"><span data-stu-id="f46be-129">**Inventory counting journal**</span></span>
    - <span data-ttu-id="f46be-130">**在庫 BOM 仕訳帳**</span><span class="sxs-lookup"><span data-stu-id="f46be-130">**Inventory BOM journal**</span></span>
    - <span data-ttu-id="f46be-131">**在庫調整仕訳帳**</span><span class="sxs-lookup"><span data-stu-id="f46be-131">**Inventory adjustment journal**</span></span>

    <span data-ttu-id="f46be-132">![作成ワークフロー ダイアログ ボックス](media/journal-workflow-create-workflow.png "作成ワークフロー ダイアログ ボックス")</span><span class="sxs-lookup"><span data-stu-id="f46be-132">![The Create workflow dialog box](media/journal-workflow-create-workflow.png "The Create workflow dialog box")</span></span>

1. <span data-ttu-id="f46be-133">ワークフロー エディタ アプリがマシン上で起動します。</span><span class="sxs-lookup"><span data-stu-id="f46be-133">The workflow editor app launches on your machine.</span></span> <span data-ttu-id="f46be-134">(このアクションの承認が要求される場合があります。)必要に応じてワークフローの設計に利用してください。</span><span class="sxs-lookup"><span data-stu-id="f46be-134">(You may be asked to approve this action.) Use it to design your workflow as needed.</span></span> <span data-ttu-id="f46be-135">ワークフロー エディターの使用方法については、[ワークフロー システムの概要](../../fin-ops-core/fin-ops/organization-administration/overview-workflow-system.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="f46be-135">For details about how to use the workflow editor, see [Workflow system overview](../../fin-ops-core/fin-ops/organization-administration/overview-workflow-system.md).</span></span>
1. <span data-ttu-id="f46be-136">ワークフロー エディター アプリを保存して閉じた後、このワーク フローのバージョンをアクティブにするか、非アクティブのままにしておくかを選択する必要があります。</span><span class="sxs-lookup"><span data-stu-id="f46be-136">After saving and closing the workflow editor app, you must choose whether to activate this workflow version or keep it as inactivate.</span></span>

> [!NOTE]
> <span data-ttu-id="f46be-137">ワークフローではバージョン管理を提供しており、作成したバージョンの一覧を表示し、どのバージョンがアクティブであるかを選択できます。</span><span class="sxs-lookup"><span data-stu-id="f46be-137">Workflows provide version control, which means that you can view a list of versions you have created and choose which one is active.</span></span> <span data-ttu-id="f46be-138">利用可能なバージョンのリストを表示し、どのバージョンを有効化するかを選択するには、**在庫管理ワークフロー** ページに一覧表示されているワークフローを選択します。</span><span class="sxs-lookup"><span data-stu-id="f46be-138">To view the list of available versions and choose which to activate, select a workflow listed on the **Inventory management workflows** page.</span></span> <span data-ttu-id="f46be-139">[アクション] ペインで、**ワークフロー** タブを開き、**バージョン** を選択します。</span><span class="sxs-lookup"><span data-stu-id="f46be-139">On the Action Pane, open the **Workflow** tab, and select **Versions**.</span></span> <span data-ttu-id="f46be-140">各ワークフロー ID に対しては、一度に 1 つのバージョンのみをアクティブにすることができます。</span><span class="sxs-lookup"><span data-stu-id="f46be-140">Only one version can be active at a time for each workflow ID.</span></span>

## <a name="assign-approval-workflows-to-inventory-journal-names"></a><span data-ttu-id="f46be-141">在庫仕訳帳に承認ワークフローを割り当てる</span><span class="sxs-lookup"><span data-stu-id="f46be-141">Assign approval workflows to inventory journal names</span></span>

<span data-ttu-id="f46be-142">次に、各在庫仕訳帳の名称に在庫仕訳帳のワークフローを割り当てます。</span><span class="sxs-lookup"><span data-stu-id="f46be-142">The next step is to assign a inventory journal workflow to each inventory journal name.</span></span> <span data-ttu-id="f46be-143">在庫仕訳帳の種類ごとに、複数の在庫仕訳帳名を設定することができます。</span><span class="sxs-lookup"><span data-stu-id="f46be-143">For each inventory journal type, you can set up multiple inventory journal names.</span></span>

<span data-ttu-id="f46be-144">在庫仕訳帳のワークフローと在庫仕訳帳名を関連付ける方法 :</span><span class="sxs-lookup"><span data-stu-id="f46be-144">To associate an inventory journal workflow with an inventory journal name:</span></span>

1. <span data-ttu-id="f46be-145">**在庫管理 \> 設定 \> 在庫仕訳帳名 \> 在庫** に移動します。</span><span class="sxs-lookup"><span data-stu-id="f46be-145">Go to **Inventory management \> Setup \> Journal names \> Inventory**.</span></span>
1. <span data-ttu-id="f46be-146">リスト列から仕訳帳名を選択すると、設定ページが表示されます。</span><span class="sxs-lookup"><span data-stu-id="f46be-146">Select a journal name from the list column to open its settings page.</span></span>
1. <span data-ttu-id="f46be-147">**全般** クイック タブ で、**承認ワークフロー** を **はい** に設定します。</span><span class="sxs-lookup"><span data-stu-id="f46be-147">On the **General** FastTab, set **Approval workflow** to **Yes**.</span></span> <span data-ttu-id="f46be-148">アクションの承認を求めるメッセージが表示されたら、**はい** を選択します。</span><span class="sxs-lookup"><span data-stu-id="f46be-148">If you are prompted to approve the action, select **Yes**.</span></span>

    <span data-ttu-id="f46be-149">![仕訳帳名にワークフローを割り当てる](media/journal-workflow-journal-name.png "仕訳帳名にワークフローを割り当てる")</span><span class="sxs-lookup"><span data-stu-id="f46be-149">![Assign a workflow to a journal name](media/journal-workflow-journal-name.png "Assign a workflow to a journal name")</span></span>

1. <span data-ttu-id="f46be-150">**ワークフロー** のドロップダウン リストを開き、承認ワークフローを選択します。</span><span class="sxs-lookup"><span data-stu-id="f46be-150">Open the **Workflow** drop-down list and select the appropriate workflow.</span></span> <span data-ttu-id="f46be-151">このリストには、ワークフロー エディター アプリを使用して作成したそれぞれのアクティブなワークフローが表示されます。</span><span class="sxs-lookup"><span data-stu-id="f46be-151">The list shows each active workflow that you have created using the workflow editor app.</span></span>

## <a name="create-an-inventory-journal-and-send-it-for-approval"></a><span data-ttu-id="f46be-152">在庫仕訳帳を作成して送信し、承認を得る</span><span class="sxs-lookup"><span data-stu-id="f46be-152">Create an inventory journal and send it for approval</span></span>

<span data-ttu-id="f46be-153">在庫仕訳帳名と一致する在庫仕訳帳の承認ワークフローを関連付けた後、その名前を使用して新しい在庫仕訳帳を作成し、ワークフローを使用してこれらの仕訳帳を送信し、承認を得ることができます。</span><span class="sxs-lookup"><span data-stu-id="f46be-153">After you associate an inventory journal name with its matching inventory journal approval workflow, you'll be able to create new inventory journals that use that name and then send these journals for approval using that workflow.</span></span> <span data-ttu-id="f46be-154">ワークフローで設定した承認者が承認すまでは、在庫仕訳帳を投稿することはできません。</span><span class="sxs-lookup"><span data-stu-id="f46be-154">You won't be able post the inventory journal until it has been approved by the approvers configured in the workflow.</span></span>

1. <span data-ttu-id="f46be-155">ナビゲーション ウィンドウで、**在庫管理 \> 仕訳帳の入力 \> 項目** を展開し、在庫仕訳帳のタイプを選択します。</span><span class="sxs-lookup"><span data-stu-id="f46be-155">On the navigation pane, expand **Inventory management \> Journal entries \> Items** and then select an inventory journal type.</span></span>
1. <span data-ttu-id="f46be-156">**新規** を選択して、選択したタイプの新しい仕訳帳を作成します。</span><span class="sxs-lookup"><span data-stu-id="f46be-156">Select **New** to create a new journal of your selected type.</span></span>
1. <span data-ttu-id="f46be-157">**在庫仕訳帳の作成** ダイアログ ボックスが開きます。</span><span class="sxs-lookup"><span data-stu-id="f46be-157">The **Create inventory journal** dialog box opens.</span></span> <span data-ttu-id="f46be-158">必要に応じてフォームに入力し、**OK** を選択して仕訳帳を保存します。</span><span class="sxs-lookup"><span data-stu-id="f46be-158">Fill out the form as needed and then select **OK** to save the journal.</span></span>
1. <span data-ttu-id="f46be-159">必要に応じて仕訳帳を完成させます。</span><span class="sxs-lookup"><span data-stu-id="f46be-159">Complete the journal as required.</span></span>
1. <span data-ttu-id="f46be-160">承認ワークフローに関連付けられた在庫仕訳帳を作成、または開くと、アクション ペインで **ワークフロー** ボタンがアクティブになります。</span><span class="sxs-lookup"><span data-stu-id="f46be-160">When you create or open an inventory journal with an approval workflow associated with it, the **Workflow** button will be active in the Action Pane.</span></span> <span data-ttu-id="f46be-161">承認のために仕訳帳を送信する準備ができたら、**ワークフロー** ボタンを選択してドロップダウン ダイアログ ボックスを開き、**送信** を選択します。</span><span class="sxs-lookup"><span data-stu-id="f46be-161">When you are ready to submit the journal for approval, select the **Workflow** button to open a drop-down dialog box and then select **Submit**.</span></span> <span data-ttu-id="f46be-162">承認要求が関連する承認者に送信されます。この承認者にはワークフローで設定された通知方法を使用して通知がされます。</span><span class="sxs-lookup"><span data-stu-id="f46be-162">The approval request will then route to the relevant approver, who will be alerted using the notification method configured for the workflow.</span></span>

    <span data-ttu-id="f46be-163">![承認のために仕訳帳を送信する](media/journal-workflow-inventory-journal.png "承認のために仕訳帳を送信する")</span><span class="sxs-lookup"><span data-stu-id="f46be-163">![Submit a journal for approval](media/journal-workflow-inventory-journal.png "Submit a journal for approval")</span></span>

<span data-ttu-id="f46be-164">承認要求を取り消すには、該当する仕訳帳を開き、**ワークフロー** ボタンを選択し、**取り消し** を選択します。</span><span class="sxs-lookup"><span data-stu-id="f46be-164">To recall an approval request, open the relevant journal, select the **Workflow** button and then select **Recall**.</span></span> <span data-ttu-id="f46be-165">これにより、ワークフローがリセットされます。</span><span class="sxs-lookup"><span data-stu-id="f46be-165">This will reset the workflow.</span></span>

<span data-ttu-id="f46be-166">仕訳帳が承認されると、投稿できるようになります。</span><span class="sxs-lookup"><span data-stu-id="f46be-166">When your journal has been approved, you'll be able to post it.</span></span> <span data-ttu-id="f46be-167">仕訳帳を投稿するには、アクション ペインから **投稿** を選択します。</span><span class="sxs-lookup"><span data-stu-id="f46be-167">To post the journal, select **Post** from the Action Pane.</span></span> <span data-ttu-id="f46be-168">**投稿** ボタンがアクティブになっていない場合は、仕訳帳がまだ承認されていないことを意味します。</span><span class="sxs-lookup"><span data-stu-id="f46be-168">If the **Post** button isn't active the journal hasn't been approved yet.</span></span>

## <a name="respond-to-an-inventory-journal-approval-request"></a><span data-ttu-id="f46be-169">在庫仕訳帳の承認要求に応答する</span><span class="sxs-lookup"><span data-stu-id="f46be-169">Respond to an inventory journal approval request</span></span>

<span data-ttu-id="f46be-170">あなたが承認者の場合は、承認が必要になるたびにメッセージを受け取ることになります (関連するワークフローで設定されています)。</span><span class="sxs-lookup"><span data-stu-id="f46be-170">If you are an approver, you should receive a message each time your approval is needed (as configured in the relevant workflow).</span></span> <span data-ttu-id="f46be-171">その後、仕訳帳の承認要求を承認または拒否するには、以下の操作を行います :</span><span class="sxs-lookup"><span data-stu-id="f46be-171">Then you can approve or reject a journal approval request by doing the following:</span></span>

1. <span data-ttu-id="f46be-172">ナビゲーション ウィンドウで、**在庫管理 \> 仕訳帳の入力 \> 項目** を展開し、在庫仕訳帳のタイプを選択します。</span><span class="sxs-lookup"><span data-stu-id="f46be-172">On the navigation pane, expand **Inventory management \> Journal entries \> Items** and then select an inventory journal type.</span></span>
1. <span data-ttu-id="f46be-173">関連する仕訳帳を開き、確認します。</span><span class="sxs-lookup"><span data-stu-id="f46be-173">Open the relevant journal and review it.</span></span>
1. <span data-ttu-id="f46be-174">アクションペインの **ワークフロー** ボタンを選択すると、ドロップダウン ダイアログ ボックスが開きます。</span><span class="sxs-lookup"><span data-stu-id="f46be-174">Select the **Workflow** button on the Action Pane to open a drop-down dialog box.</span></span> <span data-ttu-id="f46be-175">次のいずれかを選択してください。</span><span class="sxs-lookup"><span data-stu-id="f46be-175">Select one of the following:</span></span>
    - <span data-ttu-id="f46be-176">**承認** - 申請を承認します。</span><span class="sxs-lookup"><span data-stu-id="f46be-176">**Approve** - To approve the request.</span></span>
    - <span data-ttu-id="f46be-177">**拒否**  - 申請を否認します。</span><span class="sxs-lookup"><span data-stu-id="f46be-177">**Reject** - To reject the reject the request.</span></span>
    - <span data-ttu-id="f46be-178">**その他 \> 要求の変更** - 依頼元にメッセージを送信して、特定の内容を変更してから再提出するように依頼します。</span><span class="sxs-lookup"><span data-stu-id="f46be-178">**More \> Request change** - To send a message to the requester asking them to change something specific and then resubmit.</span></span>
    - <span data-ttu-id="f46be-179">**その他 \> 代理** - 承認を他のユーザーに委任します。</span><span class="sxs-lookup"><span data-stu-id="f46be-179">**More \> Delegate** - To delegate the approval to another user.</span></span>
    - <span data-ttu-id="f46be-180">**その他 \> 取り消し** - 承認要求を取り消します (ワークフローがリセットされます)。</span><span class="sxs-lookup"><span data-stu-id="f46be-180">**More \> Recall** - To recall the approval request (resets the workflow).</span></span>
    - <span data-ttu-id="f46be-181">**その他 \> ワークフロー履歴** - これまでの承認ワークフローの履歴を参照します。</span><span class="sxs-lookup"><span data-stu-id="f46be-181">**More \> Workflow history** - To view the history of this approval workflow so far.</span></span>

## <a name="review-the-approval-history"></a><span data-ttu-id="f46be-182">承認の履歴を確認する</span><span class="sxs-lookup"><span data-stu-id="f46be-182">Review the approval history</span></span>

<span data-ttu-id="f46be-183">他のタイプのワークフローと同様に、**ワークフローの履歴** ページを使用して、任意の仕訳帳の承認ワークフローの履歴を表示することができます。</span><span class="sxs-lookup"><span data-stu-id="f46be-183">As with other types of workflows, you can use the **Workflow history** page to view the approval workflow history for any journal.</span></span>

<span data-ttu-id="f46be-184">仕訳帳のワークフロー履歴を確認します。</span><span class="sxs-lookup"><span data-stu-id="f46be-184">To review the workflow history for a journal:</span></span>

1. <span data-ttu-id="f46be-185">ナビゲーション ウィンドウで、**在庫管理 \> 仕訳帳の入力 \> 項目** を展開し、在庫仕訳帳のタイプを選択します。</span><span class="sxs-lookup"><span data-stu-id="f46be-185">On the navigation pane, expand **Inventory management \> Journal entries \> Items** and then select an inventory journal type.</span></span>
1. <span data-ttu-id="f46be-186">関連する仕訳を開きます。</span><span class="sxs-lookup"><span data-stu-id="f46be-186">Open the relevant journal.</span></span>
1. <span data-ttu-id="f46be-187">アクションペインの **ワークフロー** ボタンを選択すると、ドロップダウン ダイアログ ボックスが開きます。</span><span class="sxs-lookup"><span data-stu-id="f46be-187">Select the **Workflow** button on the Action Pane to open a drop-down dialog box.</span></span> <span data-ttu-id="f46be-188">**ワークフロー履歴** を選択します。</span><span class="sxs-lookup"><span data-stu-id="f46be-188">Select **Workflow history**.</span></span> <span data-ttu-id="f46be-189">詳細については、[ワークフロー履歴を確認する](../../fin-ops-core/fin-ops/organization-administration/tasks/view-workflow-history.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="f46be-189">For more information, see [View workflow history](../../fin-ops-core/fin-ops/organization-administration/tasks/view-workflow-history.md).</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]