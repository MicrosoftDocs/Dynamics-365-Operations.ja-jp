---
title: ワークフロー タイプの作成
description: このトピックでは、ワークフロー タイプを作成する方法について説明します。
author: RobinARH
ms.date: 06/19/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: rhaertle
ms.custom: 202694
ms.assetid: 33349e0d-d8ac-4d20-8f9b-5f85d4e01004
ms.search.region: Global
ms.author: rhaertle
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: Platform update 1
ms.openlocfilehash: 4dcda1abcd199130f8aeb578aad3b65bf82d0d65
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5747129"
---
# <a name="create-a-workflow-type"></a><span data-ttu-id="15992-103">ワークフロー タイプの作成</span><span class="sxs-lookup"><span data-stu-id="15992-103">Create a workflow type</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="15992-104">ドキュメント のワークフロー サポートを追加するには、ワークフロー タイプを作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="15992-104">To add workflow support for a document, you must create a workflow type.</span></span> <span data-ttu-id="15992-105">ワークフロー タイプを作成すると、ドキュメントのワークフロー コンフィギュレーションを作成するために使用できます。</span><span class="sxs-lookup"><span data-stu-id="15992-105">After you create a workflow type, it can be used to create workflow configurations for the document.</span></span> <span data-ttu-id="15992-106">このトピックでは、ワークフロー タイプを作成する手順へのリンクを提供します。</span><span class="sxs-lookup"><span data-stu-id="15992-106">This topic provides links to the procedures for creating a workflow type.</span></span>

<span data-ttu-id="15992-107">ワークフロータイプを作成して、次の要素を定義します:</span><span class="sxs-lookup"><span data-stu-id="15992-107">You create workflow types to define the following elements:</span></span>

- <span data-ttu-id="15992-108">ワークフローを割り当てるワークフロー ドキュメント</span><span class="sxs-lookup"><span data-stu-id="15992-108">The workflow document to assign the workflow to</span></span>
- <span data-ttu-id="15992-109">ワークフロー タイプが使用可能なモジュールを定義するカテゴリ</span><span class="sxs-lookup"><span data-stu-id="15992-109">A category that defines the module that the workflow type is available in</span></span>
- <span data-ttu-id="15992-110">ワークフローでサポートされているタスク、自動化タスク、および承認</span><span class="sxs-lookup"><span data-stu-id="15992-110">Tasks, automated tasks, and approvals that are supported for the workflow</span></span>
- <span data-ttu-id="15992-111">ワークフローの開始、完了、コンフィギュレーションデータの変更、およびキャンセルされたイベント ハンドラー</span><span class="sxs-lookup"><span data-stu-id="15992-111">The workflow started, completed, configuration data change, and canceled event handlers</span></span>
- <span data-ttu-id="15992-112">**SubmitToWorkflowMenuItem** メニュー項目</span><span class="sxs-lookup"><span data-stu-id="15992-112">A **SubmitToWorkflowMenuItem** menu item</span></span>

## <a name="in-this-section"></a><span data-ttu-id="15992-113">このセクションでは</span><span class="sxs-lookup"><span data-stu-id="15992-113">In this section</span></span>

- [<span data-ttu-id="15992-114">ワークフロー タイプ チェックリスト</span><span class="sxs-lookup"><span data-stu-id="15992-114">Workflow type checklist</span></span>](workflow-type-checklist.md)
- [<span data-ttu-id="15992-115">ワークフロー カテゴリの作成</span><span class="sxs-lookup"><span data-stu-id="15992-115">Create a workflow category</span></span>](workflow-type-category.md)
- [<span data-ttu-id="15992-116">ワークフロー タイプのクエリの作成</span><span class="sxs-lookup"><span data-stu-id="15992-116">Create a query for a workflow type</span></span>](workflow-type-query.md)
- [<span data-ttu-id="15992-117">新しいワークフロー タイプの作成</span><span class="sxs-lookup"><span data-stu-id="15992-117">Create a new workflow type</span></span>](workflow-type-create-new.md)
- [<span data-ttu-id="15992-118">ワークフロー ドキュメント クラスの作成</span><span class="sxs-lookup"><span data-stu-id="15992-118">Create a workflow document class</span></span>](workflow-type-document-create.md)
- [<span data-ttu-id="15992-119">SubmitToWorkflow クラスの作成</span><span class="sxs-lookup"><span data-stu-id="15992-119">Create a SubmitToWorkflow class</span></span>](workflow-type-submit-to-workflow.md)
- [<span data-ttu-id="15992-120">ワークフロー ドキュメント クラスとワークフロー タイプの関連付け</span><span class="sxs-lookup"><span data-stu-id="15992-120">Associate a workflow document class with a workflow type</span></span>](workflow-type-associate-document.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]