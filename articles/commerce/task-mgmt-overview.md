---
title: タスク管理の概要
description: このトピックでは、Microsoft Dynamics 365 Commerce におけるマネージャーおよび作業者のタスク管理の概要を示します。
author: gvrmohanreddy
manager: annbe
ms.date: 02/10/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.search.industry: ''
ms.author: gmohanv
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Release 10.0.9
ms.openlocfilehash: 3891d846f51b5335809876a6557dfb5a031272c8
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/13/2020
ms.locfileid: "4413817"
---
# <a name="task-management-overview"></a><span data-ttu-id="1155b-103">タスク管理の概要</span><span class="sxs-lookup"><span data-stu-id="1155b-103">Task management overview</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="1155b-104">このトピックでは、Microsoft Dynamics 365 Commerce におけるマネージャーおよび作業者のタスク管理の概要を示します。</span><span class="sxs-lookup"><span data-stu-id="1155b-104">This topic provides an overview of task management for managers and workers in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="1155b-105">概要</span><span class="sxs-lookup"><span data-stu-id="1155b-105">Overview</span></span>

<span data-ttu-id="1155b-106">小売環境において、タスクが適切なタイミングで適切な担当者によって実行されるようにすることは常に困難です。</span><span class="sxs-lookup"><span data-stu-id="1155b-106">In a retail environment, it's always difficult to make sure that tasks are performed by the right person at the right time.</span></span> <span data-ttu-id="1155b-107">タスクが期限厳守で正しく完了されるように、小売業者には、次回のタスクについて作業者に通知し、関連するビジネス コンテキストを提供できる必要があります。</span><span class="sxs-lookup"><span data-stu-id="1155b-107">Retailers must be able to notify workers about upcoming tasks and provide related business context, so that the tasks can be completed correctly and on time.</span></span>

<span data-ttu-id="1155b-108">タスク管理は、Dynamics 365 Commerce においてマネージャーおよび作業者がタスク リストの作成、割り当て基準の管理、タスクの状態の追跡、および Commerce バック オフィスと販売時点管理 (POS) アプリケーション間でのこれらの操作の統合を行えるようにする、生産性向上機能です。</span><span class="sxs-lookup"><span data-stu-id="1155b-108">Task management is a productivity feature in Dynamics 365 Commerce that lets managers and workers create task lists, manage assignment criteria, track task status, and integrate these operations between Commerce back office and point of sale (POS) applications.</span></span>

<span data-ttu-id="1155b-109">本社のペルソナは、タスク管理を使用して小売店舗に対してタスク リストを作成し、店舗または作業者ごとに状態を追跡できます。</span><span class="sxs-lookup"><span data-stu-id="1155b-109">Headquarters personas can use task management to create task lists for retail stores, and to track status by store or worker.</span></span> <span data-ttu-id="1155b-110">反復タスク (たとえば、「木曜日夜の決算チェックリスト」など) を作成することもできます。</span><span class="sxs-lookup"><span data-stu-id="1155b-110">They can also create recurrent tasks (for example, "Thursday night closing checklist").</span></span>

<span data-ttu-id="1155b-111">店舗の管理者はタスク管理を使用して、個々の作業者へのタスクの割り当て、次回のタスクまたは期日が経過したタスクに関する通知の送信、タスク状態の更新、および POS アプリケーションでの単一目的のタスクの作成を行うことができます。</span><span class="sxs-lookup"><span data-stu-id="1155b-111">Store managers can use task management to assign tasks to individual workers, send notifications about upcoming tasks or tasks that are past due, update task status, and create single-purpose tasks in the POS application.</span></span> <span data-ttu-id="1155b-112">作業者は、通知およびタスク詳細の表示、および POS でのタスク状態の更新を行うことができます。</span><span class="sxs-lookup"><span data-stu-id="1155b-112">Workers can then see notifications, view task details, and update task status at the POS.</span></span>

<span data-ttu-id="1155b-113">次の図は、Commerce におけるタスク管理の概念アーキテクチャを示しています。</span><span class="sxs-lookup"><span data-stu-id="1155b-113">The following illustration shows the conceptual architecture of task management in Commerce.</span></span>

![タスク管理の概念アーキテクチャ](media/Tasks-management-conceptual-architecture.png)

## <a name="additional-resources"></a><span data-ttu-id="1155b-115">追加リソース</span><span class="sxs-lookup"><span data-stu-id="1155b-115">Additional resources</span></span>

[<span data-ttu-id="1155b-116">タスク管理のコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="1155b-116">Configure task management</span></span>](task-mgmt-configure.md)

[<span data-ttu-id="1155b-117">タスク リストの作成およびタスクの追加</span><span class="sxs-lookup"><span data-stu-id="1155b-117">Create task lists and add tasks</span></span>](task-mgmt-create-lists.md)

[<span data-ttu-id="1155b-118">店舗または従業員へのタスク リストの割り当て</span><span class="sxs-lookup"><span data-stu-id="1155b-118">Assign task lists to stores or employees</span></span>](task-mgmt-assign-lists.md)

[<span data-ttu-id="1155b-119">POS におけるタスクの管理</span><span class="sxs-lookup"><span data-stu-id="1155b-119">Task management in POS</span></span>](task-mgmt-POS.md)
