---
title: ワークフロー タイプの作成
description: このトピックでは、ワークフロー タイプを作成する方法について説明します。
author: RobinARH
manager: AnnBe
ms.date: 06/19/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: 202694
ms.assetid: 33349e0d-d8ac-4d20-8f9b-5f85d4e01004
ms.search.region: Global
ms.author: RobinARH
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: Platform update 1
ms.openlocfilehash: 4ff63339c09b7b0bac2982a26f905b82b0ac4e16
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/27/2019
ms.locfileid: "2191711"
---
# <a name="create-a-workflow-type"></a><span data-ttu-id="142ce-103">ワークフロー タイプの作成</span><span class="sxs-lookup"><span data-stu-id="142ce-103">Create a workflow type</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="142ce-104">ドキュメント のワークフロー サポートを追加するには、ワークフロー タイプを作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="142ce-104">To add workflow support for a document, you must create a workflow type.</span></span> <span data-ttu-id="142ce-105">ワークフロー タイプを作成すると、ドキュメントのワークフロー コンフィギュレーションを作成するために使用できます。</span><span class="sxs-lookup"><span data-stu-id="142ce-105">After you create a workflow type, it can be used to create workflow configurations for the document.</span></span> <span data-ttu-id="142ce-106">このトピックでは、ワークフロー タイプを作成する手順へのリンクを提供します。</span><span class="sxs-lookup"><span data-stu-id="142ce-106">This topic provides links to the procedures for creating a workflow type.</span></span>

<span data-ttu-id="142ce-107">ワークフロータイプを作成して、次の要素を定義します:</span><span class="sxs-lookup"><span data-stu-id="142ce-107">You create workflow types to define the following elements:</span></span>

- <span data-ttu-id="142ce-108">ワークフローを割り当てるワークフロー ドキュメント</span><span class="sxs-lookup"><span data-stu-id="142ce-108">The workflow document to assign the workflow to</span></span>
- <span data-ttu-id="142ce-109">ワークフロー タイプが使用可能なモジュールを定義するカテゴリ</span><span class="sxs-lookup"><span data-stu-id="142ce-109">A category that defines the module that the workflow type is available in</span></span>
- <span data-ttu-id="142ce-110">ワークフローでサポートされているタスク、自動化タスク、および承認</span><span class="sxs-lookup"><span data-stu-id="142ce-110">Tasks, automated tasks, and approvals that are supported for the workflow</span></span>
- <span data-ttu-id="142ce-111">ワークフローの開始、完了、コンフィギュレーションデータの変更、およびキャンセルされたイベント ハンドラー</span><span class="sxs-lookup"><span data-stu-id="142ce-111">The workflow started, completed, configuration data change, and canceled event handlers</span></span>
- <span data-ttu-id="142ce-112">**SubmitToWorkflowMenuItem** メニュー項目</span><span class="sxs-lookup"><span data-stu-id="142ce-112">A **SubmitToWorkflowMenuItem** menu item</span></span>

## <a name="in-this-section"></a><span data-ttu-id="142ce-113">このセクションでは</span><span class="sxs-lookup"><span data-stu-id="142ce-113">In this section</span></span>

- [<span data-ttu-id="142ce-114">ワークフロー タイプ チェックリスト</span><span class="sxs-lookup"><span data-stu-id="142ce-114">Workflow type checklist</span></span>](workflow-type-checklist.md)
- [<span data-ttu-id="142ce-115">ワークフロー カテゴリの作成</span><span class="sxs-lookup"><span data-stu-id="142ce-115">Create a workflow category</span></span>](workflow-type-category.md)
- [<span data-ttu-id="142ce-116">ワークフロー タイプのクエリの作成</span><span class="sxs-lookup"><span data-stu-id="142ce-116">Create a query for a workflow type</span></span>](workflow-type-query.md)
- [<span data-ttu-id="142ce-117">新しいワークフロー タイプの作成</span><span class="sxs-lookup"><span data-stu-id="142ce-117">Create a new workflow type</span></span>](workflow-type-create-new.md)
- [<span data-ttu-id="142ce-118">ワークフロー ドキュメント クラスの作成</span><span class="sxs-lookup"><span data-stu-id="142ce-118">Create a workflow document class</span></span>](workflow-type-document-create.md)
- [<span data-ttu-id="142ce-119">SubmitToWorkflow クラスの作成</span><span class="sxs-lookup"><span data-stu-id="142ce-119">Create a SubmitToWorkflow class</span></span>](workflow-type-submit-to-workflow.md)
- [<span data-ttu-id="142ce-120">ワークフロー ドキュメント クラスとワークフロー タイプの関連付け</span><span class="sxs-lookup"><span data-stu-id="142ce-120">Associate a workflow document class with a workflow type</span></span>](workflow-type-associate-document.md)
