---
title: プロジェクトタスクを Project Service Automation から Finance and Operations に直接同期します
description: このトピックでは、Microsoft Dynamics 365 Project Service Automation から Dynamics 365 Finance にプロジェクト タスクを直接同期させるために使用されるテンプレートと基本的なタスクについて説明します。
author: KimANelson
manager: AnnBe
ms.date: 07/20/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.3.0
ms.openlocfilehash: ba475721b69e7c75dfd2197597b54050a3598d37
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/06/2019
ms.locfileid: "2770269"
---
# <a name="synchronize-project-tasks-directly-from-project-service-automation-to-finance-and-operations"></a><span data-ttu-id="a9327-103">プロジェクトタスクを Project Service Automation から Finance and Operations に直接同期します</span><span class="sxs-lookup"><span data-stu-id="a9327-103">Synchronize project tasks directly from Project Service Automation to Finance and Operations</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="a9327-104">このトピックでは、Dynamics 365 Project Service Automation から Dynamics 365 Finance にプロジェクト タスクを直接同期させるために使用されるテンプレートと基本的なタスクについて説明します。</span><span class="sxs-lookup"><span data-stu-id="a9327-104">This topic describes the template and underlying task that are used to synchronize project tasks directly from Dynamics 365 Project Service Automation to Dynamics 365 Finance.</span></span>

> [!NOTE]
> - <span data-ttu-id="a9327-105">プロジェクト タスクの統合、経費トランザクションのカテゴリ、時間見積、経費見積、および機能ロックは、バージョン 8.0 で利用できます。</span><span class="sxs-lookup"><span data-stu-id="a9327-105">Project task integration, expense transaction categories, hour estimates, expense estimates, and functionality locking are available in version 8.0.</span></span>
> - <span data-ttu-id="a9327-106">Enterprise edition 7.3.0 を使用している場合、KB 4132657 および KB 4132660 をインストールした後に、テンプレートを使用してプロジェクト タスクの統合、経費トランザクションのカテゴリ、時間見積、経費見積、実績、および機能ロックをコンフィギュレーションできます。</span><span class="sxs-lookup"><span data-stu-id="a9327-106">If you're using Enterprise edition 7.3.0, after you install KB 4132657 and KB 4132660, you will be able to use the templates to integrate project tasks, expense transaction categories, hour estimates, expense estimates, and actuals, and to configure functionality locking.</span></span> <span data-ttu-id="a9327-107">勘定配布をリセットする必要がある場合、KB 4131710 をインストールすることをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="a9327-107">If you must reset the accounting distributions, we recommended that you also install KB 4131710.</span></span>
> - <span data-ttu-id="a9327-108">実績の統合は、バージョン 8.0.1 以降で使用可能です。</span><span class="sxs-lookup"><span data-stu-id="a9327-108">Actuals integration is available in version 8.0.1 or later.</span></span>

## <a name="data-flow-for-project-service-automation-to-finance"></a><span data-ttu-id="a9327-109">Project Service Automation から Finance のデータ フロー</span><span class="sxs-lookup"><span data-stu-id="a9327-109">Data flow for Project Service Automation to Finance</span></span>

<span data-ttu-id="a9327-110">Project Service Automation の Finance への統合ソリューションは、データの統合機能を使用して Project Service Automation および Finance のインスタンス間でデータを同期させます。</span><span class="sxs-lookup"><span data-stu-id="a9327-110">The Project Service Automation to Finance integration solution uses the Data integration feature to synchronize data across instances of Project Service Automation and Finance.</span></span> <span data-ttu-id="a9327-111">データ統合機能で利用できる統合テンプレートを使用すると、Project Service Automation から Finance にプロジェクト タスクに関するデータ フローを有効にします。</span><span class="sxs-lookup"><span data-stu-id="a9327-111">The integration template that is available with the Data integration feature enables the flow of data about project tasks from Project Service Automation to Finance.</span></span>

<span data-ttu-id="a9327-112">次の図は、データが Project Service Automation と Finance との間で同期される方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="a9327-112">The following illustration shows how the data is synchronized between Project Service Automation and Finance.</span></span>

<span data-ttu-id="a9327-113">[![Project Service Automation のデータ フローを Finance と統合](./media/ProjectTasksFlow.png)](./media/ProjectTasksFlow.png)</span><span class="sxs-lookup"><span data-stu-id="a9327-113">[![Data flow for Project Service Automation integration with Finance](./media/ProjectTasksFlow.png)](./media/ProjectTasksFlow.png)</span></span>

## <a name="template-and-task"></a><span data-ttu-id="a9327-114">テンプレートおよびタスク</span><span class="sxs-lookup"><span data-stu-id="a9327-114">Template and task</span></span>

<span data-ttu-id="a9327-115">テンプレートにアクセスするには、Microsoft Power Apps の管理者センターで**プロジェクト**を選択、次に右上隅にある**新規プロジェクト**を選択しパブリック テンプレートを選択します。</span><span class="sxs-lookup"><span data-stu-id="a9327-115">To access the template, in the Microsoft Power Apps admin center, select **Projects**, and then, in the upper-right corner, select **New project** to select public templates.</span></span>

<span data-ttu-id="a9327-116">次のテンプレートおよび基本的なタスクは Project Service Automation から Finance プロジェクト タスクを同期させるために使用されます。</span><span class="sxs-lookup"><span data-stu-id="a9327-116">The following template and underlying task are used to synchronize project tasks from Project Service Automation to Finance:</span></span>

- <span data-ttu-id="a9327-117">**データ統合でのテンプレートの名前:** プロジェクト タスク (Project Service Automation から Finance and Operations)</span><span class="sxs-lookup"><span data-stu-id="a9327-117">**Name of the template in Data integration:** Project tasks (PSA to Fin and Ops)</span></span>
- <span data-ttu-id="a9327-118">**データ統合プロジェクトのタスク名:** プロジェクト タスク</span><span class="sxs-lookup"><span data-stu-id="a9327-118">**Name of the task in the project:** Project tasks</span></span>

<span data-ttu-id="a9327-119">プロジェクト タスクの同期を行う前に、プロジェクト契約とプロジェクトを同期する必要があります。</span><span class="sxs-lookup"><span data-stu-id="a9327-119">Before synchronization of project tasks can occur, you must synchronize project contracts and projects.</span></span>

## <a name="entity-set"></a><span data-ttu-id="a9327-120">エンティティ セット</span><span class="sxs-lookup"><span data-stu-id="a9327-120">Entity set</span></span>

| <span data-ttu-id="a9327-121">Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="a9327-121">Project Service Automation</span></span> | <span data-ttu-id="a9327-122">財務</span><span class="sxs-lookup"><span data-stu-id="a9327-122">Finance</span></span>                             |
|----------------------------|-------------------------------------|
| <span data-ttu-id="a9327-123">プロジェクト タスク</span><span class="sxs-lookup"><span data-stu-id="a9327-123">Project Tasks</span></span>              | <span data-ttu-id="a9327-124">プロジェクトタスクの統合エンティティ</span><span class="sxs-lookup"><span data-stu-id="a9327-124">Integration entity for project task</span></span> |

## <a name="entity-flow"></a><span data-ttu-id="a9327-125">エンティティのフロー</span><span class="sxs-lookup"><span data-stu-id="a9327-125">Entity flow</span></span>

<span data-ttu-id="a9327-126">プロジェクト タスクは Project Service Automation で管理され、プロジェクト活動として Finance に同期されます。</span><span class="sxs-lookup"><span data-stu-id="a9327-126">Project tasks are managed in Project Service Automation, and they are synchronized to Finance as project activities.</span></span>

## <a name="prerequisites-and-mapping-setup"></a><span data-ttu-id="a9327-127">前提条件およびマッピングの設定</span><span class="sxs-lookup"><span data-stu-id="a9327-127">Prerequisites and mapping setup</span></span>

<span data-ttu-id="a9327-128">プロジェクト タスクの同期を行う前に、プロジェクト契約とプロジェクトを同期する必要があります。</span><span class="sxs-lookup"><span data-stu-id="a9327-128">Before synchronization of project tasks can occur, you must synchronize project contracts and projects.</span></span>

## <a name="power-query"></a><span data-ttu-id="a9327-129">Power Query</span><span class="sxs-lookup"><span data-stu-id="a9327-129">Power Query</span></span>

<span data-ttu-id="a9327-130">この条件が満たされた場合、フィルター処理する Microsoft Power Query for Excel を使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="a9327-130">You must use Microsoft Power Query for Excel to filter data if this condition is met:</span></span>

- <span data-ttu-id="a9327-131">プロジェクト タスク内のリソース特定のレコードがあります。</span><span class="sxs-lookup"><span data-stu-id="a9327-131">You have resource-specific records in a project task.</span></span>

<span data-ttu-id="a9327-132">Power Query を使用する必要がある場合は、このガイドラインに従います。</span><span class="sxs-lookup"><span data-stu-id="a9327-132">If you must use Power Query, follow this guideline:</span></span>

- <span data-ttu-id="a9327-133">プロジェクト タスク (Project Service Automation から Finance and Operations) テンプレートには、**IsLineTask** から **False** のフィルターを設定することでプロジェクト タスクからのリソース特定レコードを除外する既定のフィルターがあります。</span><span class="sxs-lookup"><span data-stu-id="a9327-133">The Project tasks (PSA to Fin and Ops) template has a default filter that excludes resource-specific records from a project task by setting the filter on **IsLineTask** to **False**.</span></span> <span data-ttu-id="a9327-134">独自のテンプレートを作成する場合は、このフィルターを追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="a9327-134">If you create your own template, you must add this filter.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="a9327-135">データ統合のテンプレートのマッピング</span><span class="sxs-lookup"><span data-stu-id="a9327-135">Template mapping in Data integration</span></span>

<span data-ttu-id="a9327-136">次の図は、データ インテグレーターのタスク マッピングの例を示します。</span><span class="sxs-lookup"><span data-stu-id="a9327-136">The following illustration shows an example of the template task mappings in Data integration.</span></span> <span data-ttu-id="a9327-137">マッピングは、Project Service Automation から Finance に同期するフィールド情報を表示します。</span><span class="sxs-lookup"><span data-stu-id="a9327-137">The mapping shows the field information that will be synchronized from Project Service Automation to Finance.</span></span>

<span data-ttu-id="a9327-138">[![テンプレートのマッピング](./media/ProjectTasksMapping.png)](./media/ProjectTasksMapping.png)</span><span class="sxs-lookup"><span data-stu-id="a9327-138">[![Template mapping](./media/ProjectTasksMapping.png)](./media/ProjectTasksMapping.png)</span></span>
