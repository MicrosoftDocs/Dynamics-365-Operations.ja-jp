---
title: ワークフローの作成の概要
description: このトピックでは、ワークフローの作成方法を説明します。
author: sericks007
manager: AnnBe
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WorkflowSelectTemplateRnr, WorkflowTableListPageRnr
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 195583
ms.assetid: 836ddd01-cc34-45c3-a4b0-20647357dbc6
ms.search.region: Global
ms.author: donaldc
ms.search.validFrom: 2016-08-30
ms.dyn365.ops.version: Platform update 2
ms.openlocfilehash: a643be553f3fcdfbe53f2024982a596e498830a8
ms.sourcegitcommit: 57bc7e17682e2edb5e1766496b7a22f4621819dd
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/18/2019
ms.locfileid: "2811299"
---
# <a name="create-workflows-overview"></a><span data-ttu-id="428a4-103">ワークフローの作成の概要</span><span class="sxs-lookup"><span data-stu-id="428a4-103">Create workflows overview</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="428a4-104">このトピックでは、ワークフローの作成方法を説明します。</span><span class="sxs-lookup"><span data-stu-id="428a4-104">This topic explains how to create a workflow.</span></span>

## <a name="open-the-workflow-editor"></a><span data-ttu-id="428a4-105">ワークフロー エディターを開く</span><span class="sxs-lookup"><span data-stu-id="428a4-105">Open the workflow editor</span></span>

<span data-ttu-id="428a4-106">作成可能なワークフローのタイプは、使用しているモジュールによって決まります。</span><span class="sxs-lookup"><span data-stu-id="428a4-106">The module that you're working in determines the types of workflow that you can create.</span></span> <span data-ttu-id="428a4-107">次の手順に従って、作成するワークフローのタイプを選択し、ワークフロー エディターを開きます。</span><span class="sxs-lookup"><span data-stu-id="428a4-107">Follow these steps to select the type of workflow to create and open the workflow editor.</span></span>

1. <span data-ttu-id="428a4-108">新しいワークフローを作成するモジュールを開きます。</span><span class="sxs-lookup"><span data-stu-id="428a4-108">Open the module that you want to create a new workflow for.</span></span> <span data-ttu-id="428a4-109">たとえば、購買要求ワークフローを作成するには、**調達**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="428a4-109">For example, to create a workflow for purchase requisitions, click **Procurement and sourcing**.</span></span>
2. <span data-ttu-id="428a4-110">**設定** &gt; **\[モジュール名\] ワークフロー** の順にクリックします。</span><span class="sxs-lookup"><span data-stu-id="428a4-110">Click **Setup** &gt; **\[Module name\] workflows**.</span></span>
3. <span data-ttu-id="428a4-111">アクション ウィンドウのリスト ページで、**新規**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="428a4-111">On the list page that appears, on the Action Pane, click **New**.</span></span>
4. <span data-ttu-id="428a4-112">**ワークフローの作成**ページで、作成するワークフローのタイプを選択し、**ワークフローの作成**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="428a4-112">On the **Create workflow** page, select the type of workflow to create, and then click **Create workflow**.</span></span> <span data-ttu-id="428a4-113">ワークフロー エディターが表示されます。</span><span class="sxs-lookup"><span data-stu-id="428a4-113">The workflow editor appears.</span></span> <span data-ttu-id="428a4-114">ワークフローをデザインするには、次の手順を使用できます。</span><span class="sxs-lookup"><span data-stu-id="428a4-114">You can now use the following procedures to design the workflow.</span></span>

## <a name="drag-workflow-elements-onto-the-canvas"></a><span data-ttu-id="428a4-115">キャンバスへのワークフロー要素のドラッグ</span><span class="sxs-lookup"><span data-stu-id="428a4-115">Drag workflow elements onto the canvas</span></span>

<span data-ttu-id="428a4-116">ワークフロー エディターの**ワークフロー要素**領域には、ワークフローに追加できる要素があります。</span><span class="sxs-lookup"><span data-stu-id="428a4-116">The **Workflow elements** area of the workflow editor contains the elements that you can add to your workflow.</span></span> <span data-ttu-id="428a4-117">ワークフローに要素を追加するには、要素をキャンバスにドラッグします。</span><span class="sxs-lookup"><span data-stu-id="428a4-117">To add elements to the workflow, drag them onto the canvas.</span></span>

## <a name="connect-the-elements"></a><span data-ttu-id="428a4-118">要素の接続</span><span class="sxs-lookup"><span data-stu-id="428a4-118">Connect the elements</span></span>

<span data-ttu-id="428a4-119">あるワークフロー要素と別のワークフロー要素を接続するには、要素の上にポインターを移動して、接続ポイントが表示されるまで保持します。</span><span class="sxs-lookup"><span data-stu-id="428a4-119">To connect one workflow element to another, hold the pointer over an element until connection points appear.</span></span> <span data-ttu-id="428a4-120">接続ポイントをクリックし、別の要素にドラッグします。</span><span class="sxs-lookup"><span data-stu-id="428a4-120">Click a connection point, and drag it to another element.</span></span> <span data-ttu-id="428a4-121">すべての要素を接続してください。</span><span class="sxs-lookup"><span data-stu-id="428a4-121">Be sure to connect all the elements.</span></span>

## <a name="configure-the-properties-of-the-workflow"></a><span data-ttu-id="428a4-122">ワークフローのプロパティのコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="428a4-122">Configure the properties of the workflow</span></span>

<span data-ttu-id="428a4-123">次の手順に従って、ワークフローのプロパティをコンフィギュレーションします。</span><span class="sxs-lookup"><span data-stu-id="428a4-123">Follow these steps to configure the properties of the workflow.</span></span>

1. <span data-ttu-id="428a4-124">どのワークフロー要素も選択されていないようにするため、キャンバスをクリックします。</span><span class="sxs-lookup"><span data-stu-id="428a4-124">Click the canvas to make sure that no workflow element is selected.</span></span>
2. <span data-ttu-id="428a4-125">**プロパティ**をクリックして、ワークフローの**プロパティ**ページを開きます。</span><span class="sxs-lookup"><span data-stu-id="428a4-125">Click **Properties** to open the **Properties** page for the workflow.</span></span>
3. <span data-ttu-id="428a4-126">[ワークフロー プロパティのコンフィギュレーション](configure-workflow-properties.md) トピックで示されている次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="428a4-126">Follow the procedures in the [Configure workflow properties](configure-workflow-properties.md) topic.</span></span>

## <a name="configure-the-elements-of-the-workflow"></a><span data-ttu-id="428a4-127">ワークフローの要素のコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="428a4-127">Configure the elements of the workflow</span></span>

<span data-ttu-id="428a4-128">キャンバスにドラッグした各要素をコンフィギュレーションします。</span><span class="sxs-lookup"><span data-stu-id="428a4-128">Configure each element that you dragged onto the canvas.</span></span> <span data-ttu-id="428a4-129">各ワークフロー要素をコンフィギュレーションする方法については、次のトピックを参照してください。</span><span class="sxs-lookup"><span data-stu-id="428a4-129">For information about how to configure each workflow element, see the following topics:</span></span>

- [<span data-ttu-id="428a4-130">ワークフローでの手動タスクのコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="428a4-130">Configure manual tasks in a workflow</span></span>](configure-manual-task-workflow.md)
- [<span data-ttu-id="428a4-131">ワークフローでの自動化タスクのコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="428a4-131">Configure automated tasks in a workflow</span></span>](configure-automated-task-workflow.md)
- [<span data-ttu-id="428a4-132">ワークフローでの承認プロセスのコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="428a4-132">Configure approval processes in a workflow</span></span>](configure-approval-process-workflow.md)
- [<span data-ttu-id="428a4-133">ワークフローでの承認ステップのコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="428a4-133">Configure approval steps in a workflow</span></span>](configure-approval-step-workflow.md)
- [<span data-ttu-id="428a4-134">ワークフローでの手動決定のコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="428a4-134">Configure manual decisions in a workflow</span></span>](configure-manual-decision-workflow.md)
- [<span data-ttu-id="428a4-135">ワークフローでの条件付き意思決定のコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="428a4-135">Configure conditional decisions in a workflow</span></span>](configure-conditional-decision-workflow.md)
- [<span data-ttu-id="428a4-136">ワークフロー内の並列分岐のコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="428a4-136">Configure parallel branches in a workflow</span></span>](configure-parallel-activity-workflow.md)
- [<span data-ttu-id="428a4-137">並列分岐のコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="428a4-137">Configure a parallel branch</span></span>](configure-parallel-branch-workflow.md)
- [<span data-ttu-id="428a4-138">品目ワークフローのコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="428a4-138">Configure line-item workflows</span></span>](configure-line-item-workflow.md)

## <a name="resolve-any-errors-or-warnings"></a><span data-ttu-id="428a4-139">エラーまたは警告の解決</span><span class="sxs-lookup"><span data-stu-id="428a4-139">Resolve any errors or warnings</span></span>

<span data-ttu-id="428a4-140">ワークフロー エディターの下部にある**エラーおよび警告**ウィンドウには、ワークフローに対して生成されたメッセージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="428a4-140">The **Errors and warnings** pane at the bottom of the workflow editor shows messages that have been generated for the workflow.</span></span> <span data-ttu-id="428a4-141">エラーまたは警告が発生した要素を特定するには、エラーまたは警告メッセージをダブルクリックします。</span><span class="sxs-lookup"><span data-stu-id="428a4-141">To find the element where an error or warning occurred, double-click the error or warning message.</span></span> <span data-ttu-id="428a4-142">ワークフローを有効にする前に、エラーと警告をすべて解決する必要があります。</span><span class="sxs-lookup"><span data-stu-id="428a4-142">You must resolve all errors and warnings before you can make the workflow active.</span></span>

## <a name="save-and-activate-the-workflow"></a><span data-ttu-id="428a4-143">ワークフローの保存と有効化</span><span class="sxs-lookup"><span data-stu-id="428a4-143">Save and activate the workflow</span></span>

<span data-ttu-id="428a4-144">ワークフローを保存して有効化する準備が整ったら、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="428a4-144">When you're ready to save and activate the workflow, follow these steps.</span></span>

1. <span data-ttu-id="428a4-145">**保存して終了**をクリックして、ワークフロー エディターを閉じ、**ワークフローの保存**ページを開きます。</span><span class="sxs-lookup"><span data-stu-id="428a4-145">Click **Save and close** to close the workflow editor and open the **Save workflow** page.</span></span>
2. <span data-ttu-id="428a4-146">ワークフローに加えた変更に関するコメントを入力し、**OK** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="428a4-146">Enter comments about the changes that you've made to the workflow, and then click **OK**.</span></span>
3. <span data-ttu-id="428a4-147">エラーと警告がすべて解決されると、**ワークフローの有効化**ページが表示されます。</span><span class="sxs-lookup"><span data-stu-id="428a4-147">If all errors and warnings have been resolved, the **Activate workflow** page appears.</span></span> <span data-ttu-id="428a4-148">次のいずれかのオプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="428a4-148">Select one of the following options:</span></span>

    - <span data-ttu-id="428a4-149">ワークフローのこのバージョンを有効にするには、**新しいバージョンの有効化**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="428a4-149">To activate this version of the workflow, click **Activate the new version**.</span></span> <span data-ttu-id="428a4-150">ワークフローが有効な場合は、ユーザーが、処理するドキュメントをワークフローに送信できます。</span><span class="sxs-lookup"><span data-stu-id="428a4-150">When a workflow is active, users can submit documents to it for processing.</span></span>
    - <span data-ttu-id="428a4-151">このバージョンを有効にしない場合は、**新しいバージョンを有効にしない**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="428a4-151">If you don't want to activate this version, click **Do not activate the new version**.</span></span> <span data-ttu-id="428a4-152">ワークフローは後で有効にすることができます。</span><span class="sxs-lookup"><span data-stu-id="428a4-152">You can activate the workflow later.</span></span>
