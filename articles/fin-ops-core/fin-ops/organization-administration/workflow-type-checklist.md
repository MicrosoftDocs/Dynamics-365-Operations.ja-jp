---
title: ワークフロー タイプ チェックリスト
description: このトピックでは、新しいワークフロー タイプを作成するために必要な手順について説明します。
author: RobinARH
manager: AnnBe
ms.date: 06/19/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: rhaertle
ms.custom: 202694
ms.assetid: 33349e0d-d8ac-4d20-8f9b-5f85d4e01004
ms.search.region: Global
ms.author: rhaertle
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: Platform update 1
ms.openlocfilehash: d2b95d17a80224adadac5f8e833a7023169ba087
ms.sourcegitcommit: b112925c389a460a98c3401cc2c67df7091b066f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/19/2020
ms.locfileid: "4798761"
---
# <a name="workflow-type-checklist"></a><span data-ttu-id="c9ce6-103">ワークフロー タイプ チェックリスト</span><span class="sxs-lookup"><span data-stu-id="c9ce6-103">Workflow type checklist</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c9ce6-104">このトピックでは、新しいワークフロー タイプを作成するために必要な手順について説明します。</span><span class="sxs-lookup"><span data-stu-id="c9ce6-104">This topic describes the steps that are required to create a new workflow type.</span></span> <span data-ttu-id="c9ce6-105">ワークフロー タイプは、 ワークフローの構成を作成するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="c9ce6-105">Workflow types are used to create configurations for a workflow.</span></span>

## <a name="workflow-type-checklist"></a><span data-ttu-id="c9ce6-106">ワークフロー タイプのチェックリスト</span><span class="sxs-lookup"><span data-stu-id="c9ce6-106">Workflow type checklist</span></span>

1. <span data-ttu-id="c9ce6-107">既存のカテゴリが適切ではない場合は、ワークフロー タイプに使用する新しいワークフロー カテゴリを作成します。</span><span class="sxs-lookup"><span data-stu-id="c9ce6-107">If an existing category isn't appropriate, create a new workflow category to use for the workflow type.</span></span> <span data-ttu-id="c9ce6-108">詳細については、 [新しいワークフロー カテゴリの作成](workflow-type-category.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="c9ce6-108">For more information, see [Create a workflow category](workflow-type-category.md).</span></span>
2. <span data-ttu-id="c9ce6-109">新しいワークフロー タイプが作成されるドキュメントにアクセスするクエリを作成します。</span><span class="sxs-lookup"><span data-stu-id="c9ce6-109">Create a query that accesses the document that the new workflow type is being created for.</span></span> <span data-ttu-id="c9ce6-110">詳細については、 [ワークフロー タイプのクエリの作成](workflow-type-query.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="c9ce6-110">For more information, see [Create a query for a workflow type](workflow-type-query.md).</span></span>
3. <span data-ttu-id="c9ce6-111">アプリケーション エクスプローラーでワークフロー タイプを作成します。</span><span class="sxs-lookup"><span data-stu-id="c9ce6-111">Create a workflow type in Application Explorer.</span></span> <span data-ttu-id="c9ce6-112">通常、 **ワークフロー** ウィザードを使用してこの手順を完了します。</span><span class="sxs-lookup"><span data-stu-id="c9ce6-112">Typically, you complete this step by using the **Workflow** wizard.</span></span> <span data-ttu-id="c9ce6-113">詳細については、 [新しいワークフロー タイプの作成](workflow-type-create-new.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="c9ce6-113">For more information, see [Create a new workflow type](workflow-type-create-new.md).</span></span>

<span data-ttu-id="c9ce6-114">ワークフロー タイプを作成するために、 **ワークフロー** ウィザードを使用することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="c9ce6-114">We recommend that you use the **Workflow** wizard to create a workflow type.</span></span> <span data-ttu-id="c9ce6-115">ウィザードでは次のタスクを実行します。</span><span class="sxs-lookup"><span data-stu-id="c9ce6-115">The wizard performs the following tasks.</span></span> <span data-ttu-id="c9ce6-116">場合によっては、ワークフロー タイプに対してさらにコードを追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="c9ce6-116">In some cases, you must add more code for your workflow type.</span></span> <span data-ttu-id="c9ce6-117">ウィザードによって実行されるアクションの詳細、およびワークフロー タイプを完了するために実行する必要がある追加手順を確認できるように、リンクが提供されています。</span><span class="sxs-lookup"><span data-stu-id="c9ce6-117">Links are provided so that you can see the details of the actions that the wizard performs and the additional steps that you must perform to complete your workflow type.</span></span>

1. <span data-ttu-id="c9ce6-118">ワークフロー ドキュメント クラスを作成し、ワークフローに使用するクエリをクラスにバインドします。</span><span class="sxs-lookup"><span data-stu-id="c9ce6-118">Create a workflow document class, and then bind the query that is used for the workflow to the class.</span></span> <span data-ttu-id="c9ce6-119">詳細については、 [新しいワークフロー ドキュメント クラスの作成](workflow-type-document-create.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="c9ce6-119">For more information, see [Create a workflow document class](workflow-type-document-create.md).</span></span>
2. <span data-ttu-id="c9ce6-120">ワークフロー ドキュメント クラスをワークフロー タイプにバインドします。</span><span class="sxs-lookup"><span data-stu-id="c9ce6-120">Bind the workflow document class to the workflow type.</span></span> <span data-ttu-id="c9ce6-121">詳細については、 [ワークフロー ドキュメント クラスとワークフロー タイプの関連付け](workflow-type-associate-document.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="c9ce6-121">For more information, see [Associate a workflow document class with a workflow type](workflow-type-associate-document.md).</span></span>
3. <span data-ttu-id="c9ce6-122">開始、完了、コンフィギュレーションの変更、およびキャンセルされたイベントのワークフロー イベント ハンドラーを作成し、イベント ハンドラーをワークフロー タイプにバインドします。</span><span class="sxs-lookup"><span data-stu-id="c9ce6-122">Create workflow event handlers for started, completed, configuration change, and canceled events, and then bind event handlers to the workflow type.</span></span> <span data-ttu-id="c9ce6-123">詳細については、 [新しいワークフロー イベント ハンドラーの作成](https://docs.microsoft.com/dynamicsax-2012/developer/how-to-create-a-workflow-event-handler) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="c9ce6-123">For more information, see [Create a workflow event handler](https://docs.microsoft.com/dynamicsax-2012/developer/how-to-create-a-workflow-event-handler).</span></span>
4. <span data-ttu-id="c9ce6-124">**SubmitToWorkflowMenuItem** のクラスを作成します。</span><span class="sxs-lookup"><span data-stu-id="c9ce6-124">Create a class for **SubmitToWorkflowMenuItem**.</span></span> <span data-ttu-id="c9ce6-125">必要に応じて、 **CancelMenuItem** のクラスを作成します。</span><span class="sxs-lookup"><span data-stu-id="c9ce6-125">Optionally create a class for **CancelMenuItem**.</span></span> <span data-ttu-id="c9ce6-126">次のステップで作成するアクション メニュー項目にクラスをバインドします。</span><span class="sxs-lookup"><span data-stu-id="c9ce6-126">Bind the classes to the action menu items that you will create in the next step.</span></span> <span data-ttu-id="c9ce6-127">詳細については、[クラスおよびメソッド](../../dev-itpro/dev-ref/xpp-classes-methods.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="c9ce6-127">For more information, see [Classes and methods](../../dev-itpro/dev-ref/xpp-classes-methods.md).</span></span>
5. <span data-ttu-id="c9ce6-128">**SubmitToWorkflowMenuItem** ワークフロー プロパティのアクション メニュー項目を作成します。</span><span class="sxs-lookup"><span data-stu-id="c9ce6-128">Create an action menu item for the **SubmitToWorkflowMenuItem** workflow property.</span></span> <span data-ttu-id="c9ce6-129">必要に応じて、 **CancelMenuItem** プロパティのアクション メニュー項目を作成します。</span><span class="sxs-lookup"><span data-stu-id="c9ce6-129">Optionally create an action menu item for the **CancelMenuItem** property.</span></span> <span data-ttu-id="c9ce6-130">アクションをワークフロー タイプにバインドします。</span><span class="sxs-lookup"><span data-stu-id="c9ce6-130">Bind the actions to the workflow type.</span></span> <span data-ttu-id="c9ce6-131">詳細については、 [新しいワークフロー タイプの作成](workflow-type-create-new.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="c9ce6-131">For more information, see [Create a new workflow type](workflow-type-create-new.md).</span></span>

## <a name="next-steps"></a><span data-ttu-id="c9ce6-132">次のステップ</span><span class="sxs-lookup"><span data-stu-id="c9ce6-132">Next steps</span></span>

<span data-ttu-id="c9ce6-133">ワークフロー タイプを作成した後、タスク、自動化されたタスク、および承認を追加できます。</span><span class="sxs-lookup"><span data-stu-id="c9ce6-133">After you create a workflow type, you can add tasks, automated tasks, and approvals.</span></span>

## <a name="see-also"></a><span data-ttu-id="c9ce6-134">参照</span><span class="sxs-lookup"><span data-stu-id="c9ce6-134">See also</span></span>

[<span data-ttu-id="c9ce6-135">ワークフロー プロパティのコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="c9ce6-135">Configure workflow properties</span></span>](configure-workflow-properties.md)

[<span data-ttu-id="c9ce6-136">ワークフローでの手動タスクのコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="c9ce6-136">Configure manual tasks in a workflow</span></span>](configure-manual-task-workflow.md)

[<span data-ttu-id="c9ce6-137">ワークフローでの自動化タスクのコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="c9ce6-137">Configure automated tasks in a workflow</span></span>](configure-automated-task-workflow.md)

[<span data-ttu-id="c9ce6-138">ワークフローでの承認プロセスのコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="c9ce6-138">Configure approval processes in a workflow</span></span>](configure-approval-process-workflow.md)
