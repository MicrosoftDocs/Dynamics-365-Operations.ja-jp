---
title: プロジェクトタスクを Project Service Automation から Finance and Operations に直接同期します
description: このトピックでは、Microsoft Dynamics 365 for Project Service Automation から Microsoft Dynamics 365 for Finance and Operations にプロジェクト タスクを直接同期させるために使用されるテンプレートと基本的なタスクについて説明します。
author: KimANelson
manager: AnnBe
ms.date: 07/20/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.3.0
ms.openlocfilehash: 53e4eab0d455af4ac1e17754f31d46458db742c3
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/29/2019
ms.locfileid: "355176"
---
# <a name="synchronize-project-tasks-directly-from-project-service-automation-to-finance-and-operations"></a><span data-ttu-id="aea56-103">プロジェクトタスクを Project Service Automation から Finance and Operations に直接同期します</span><span class="sxs-lookup"><span data-stu-id="aea56-103">Synchronize project tasks directly from Project Service Automation to Finance and Operations</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="aea56-104">このトピックでは、Microsoft Dynamics 365 for Project Service Automation から Microsoft Dynamics 365 for Finance and Operations にプロジェクト タスクを直接同期させるために使用されるテンプレートと基本的なタスクについて説明します。</span><span class="sxs-lookup"><span data-stu-id="aea56-104">This topic describes the template and underlying task that are used to synchronize project tasks directly from Microsoft Dynamics 365 for Project Service Automation to Microsoft Dynamics 365 for Finance and Operations.</span></span>

> [!NOTE]
> - <span data-ttu-id="aea56-105">プロジェクト タスクの統合、経費トランザクションのカテゴリ、時間見積、経費見積、および機能ロックは、Microsoft Dynamics 365 for Finance and Operations バージョン 8.0 で利用できます。</span><span class="sxs-lookup"><span data-stu-id="aea56-105">Project task integration, expense transaction categories, hour estimates, expense estimates, and functionality locking are available in Microsoft Dynamics 365 for Finance and Operations version 8.0.</span></span>
> - <span data-ttu-id="aea56-106">Microsoft Dynamics 365 for Finance and Operations、Enterprise edition 7.3.0 を使用している場合、KB 4132657 および KB 4132660 をインストールした後に、テンプレートを使用してプロジェクト タスクの統合、経費トランザクションのカテゴリ、時間見積、経費見積、実績、および機能ロックをコンフィギュレーションできます。</span><span class="sxs-lookup"><span data-stu-id="aea56-106">If you're using Microsoft Dynamics 365 for Finance and Operations, Enterprise edition 7.3.0, after you install KB 4132657 and KB 4132660, you will be able to use the templates to integrate project tasks, expense transaction categories, hour estimates, expense estimates, and actuals, and to configure functionality locking.</span></span> <span data-ttu-id="aea56-107">勘定配布をリセットする必要がある場合、KB 4131710 をインストールすることをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="aea56-107">If you must reset the accounting distributions, we recommended that you also install KB 4131710.</span></span>
> - <span data-ttu-id="aea56-108">実績の統合は、Microsoft Dynamics 365 for Finance and Operations バージョン 8.0.1 以降で使用可能です。</span><span class="sxs-lookup"><span data-stu-id="aea56-108">Actuals integration is available in Microsoft Dynamics 365 for Finance and Operations version 8.0.1 or later.</span></span>

## <a name="data-flow-for-project-service-automation-to-finance-and-operations"></a><span data-ttu-id="aea56-109">Project Service Automation から Finance and Operations のデータ フロー</span><span class="sxs-lookup"><span data-stu-id="aea56-109">Data flow for Project Service Automation to Finance and Operations</span></span>

<span data-ttu-id="aea56-110">Project Service Automation から Finance and Operations の統合ソリューションは、データの統合機能を使用して Project Service Automation および Finance and Operations のインスタンス間でデータを同期させます。</span><span class="sxs-lookup"><span data-stu-id="aea56-110">The Project Service Automation to Finance and Operations integration solution uses the Data integration feature to synchronize data across instances of Project Service Automation and Finance and Operations.</span></span> <span data-ttu-id="aea56-111">データ統合機能で利用できる統合テンプレートを使用すると、Project Service Automation から Finance and Operations にプロジェクト タスクに関するデータ フローを有効にします。</span><span class="sxs-lookup"><span data-stu-id="aea56-111">The integration template that is available with the Data integration feature enables the flow of data about project tasks from Project Service Automation to Finance and Operations.</span></span>

<span data-ttu-id="aea56-112">次の図は、データが Project Service Automation と Finance and Operations との間で同期される方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="aea56-112">The following illustration shows how the data is synchronized between Project Service Automation and Finance and Operations.</span></span>

<span data-ttu-id="aea56-113">[![Project Service Automation のデータ フローを Finance and Operations と統合](./media/ProjectTasksFlow.png)](./media/ProjectTasksFlow.png)</span><span class="sxs-lookup"><span data-stu-id="aea56-113">[![Data flow for Project Service Automation integration with Finance and Operations](./media/ProjectTasksFlow.png)](./media/ProjectTasksFlow.png)</span></span>

## <a name="template-and-task"></a><span data-ttu-id="aea56-114">テンプレートおよびタスク</span><span class="sxs-lookup"><span data-stu-id="aea56-114">Template and task</span></span>

<span data-ttu-id="aea56-115">テンプレートにアクセスするには、Microsoft PowerApps の管理者センターで**プロジェクト**を選択、次に右上隅にある**新規プロジェクト**を選択しパブリック テンプレートを選択します。</span><span class="sxs-lookup"><span data-stu-id="aea56-115">To access the template, in the Microsoft PowerApps admin center, select **Projects**, and then, in the upper-right corner, select **New project** to select public templates.</span></span>

<span data-ttu-id="aea56-116">次のテンプレートおよび基本的なタスクは Project Service Automation から Finance and Operations プロジェクト タスクを同期させるために使用されます。</span><span class="sxs-lookup"><span data-stu-id="aea56-116">The following template and underlying task are used to synchronize project tasks from Project Service Automation to Finance and Operations:</span></span>

- <span data-ttu-id="aea56-117">**データ統合でのテンプレートの名前:** プロジェクト タスク (Project Service Automation から Finance and Operations)</span><span class="sxs-lookup"><span data-stu-id="aea56-117">**Name of the template in Data integration:** Project tasks (PSA to Fin and Ops)</span></span>
- <span data-ttu-id="aea56-118">**データ統合プロジェクトのタスク名:** プロジェクト タスク</span><span class="sxs-lookup"><span data-stu-id="aea56-118">**Name of the task in the project:** Project tasks</span></span>

<span data-ttu-id="aea56-119">プロジェクト タスクの同期を行う前に、プロジェクト契約とプロジェクトを同期する必要があります。</span><span class="sxs-lookup"><span data-stu-id="aea56-119">Before synchronization of project tasks can occur, you must synchronize project contracts and projects.</span></span>

## <a name="entity-set"></a><span data-ttu-id="aea56-120">エンティティ セット</span><span class="sxs-lookup"><span data-stu-id="aea56-120">Entity set</span></span>

| <span data-ttu-id="aea56-121">Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="aea56-121">Project Service Automation</span></span> | <span data-ttu-id="aea56-122">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="aea56-122">Finance and Operations</span></span>              |
|----------------------------|-------------------------------------|
| <span data-ttu-id="aea56-123">プロジェクト タスク</span><span class="sxs-lookup"><span data-stu-id="aea56-123">Project Tasks</span></span>              | <span data-ttu-id="aea56-124">プロジェクトタスクの統合エンティティ</span><span class="sxs-lookup"><span data-stu-id="aea56-124">Integration entity for project task</span></span> |

## <a name="entity-flow"></a><span data-ttu-id="aea56-125">エンティティのフロー</span><span class="sxs-lookup"><span data-stu-id="aea56-125">Entity flow</span></span>

<span data-ttu-id="aea56-126">プロジェクト タスクは Project Service Automation で管理され、プロジェクト活動として Finance and Operations に同期されます。</span><span class="sxs-lookup"><span data-stu-id="aea56-126">Project tasks are managed in Project Service Automation, and they are synchronized to Finance and Operations as project activities.</span></span>

## <a name="prerequisites-and-mapping-setup"></a><span data-ttu-id="aea56-127">前提条件およびマッピングの設定</span><span class="sxs-lookup"><span data-stu-id="aea56-127">Prerequisites and mapping setup</span></span>

<span data-ttu-id="aea56-128">プロジェクト タスクの同期を行う前に、プロジェクト契約とプロジェクトを同期する必要があります。</span><span class="sxs-lookup"><span data-stu-id="aea56-128">Before synchronization of project tasks can occur, you must synchronize project contracts and projects.</span></span>

## <a name="power-query"></a><span data-ttu-id="aea56-129">Power Query</span><span class="sxs-lookup"><span data-stu-id="aea56-129">Power Query</span></span>

<span data-ttu-id="aea56-130">この条件が満たされた場合、フィルター処理する Microsoft Power Query for Excel を使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="aea56-130">You must use Microsoft Power Query for Excel to filter data if this condition is met:</span></span>

- <span data-ttu-id="aea56-131">プロジェクト タスク内のリソース特定のレコードがあります。</span><span class="sxs-lookup"><span data-stu-id="aea56-131">You have resource-specific records in a project task.</span></span>

<span data-ttu-id="aea56-132">Power Query を使用する必要がある場合は、このガイドラインに従います。</span><span class="sxs-lookup"><span data-stu-id="aea56-132">If you must use Power Query, follow this guideline:</span></span>

- <span data-ttu-id="aea56-133">プロジェクト タスク (Project Service Automation から Finance and Operations) テンプレートには、**IsLineTask** から **False** のフィルターを設定することでプロジェクト タスクからのリソース特定レコードを除外する既定のフィルターがあります。</span><span class="sxs-lookup"><span data-stu-id="aea56-133">The Project tasks (PSA to Fin and Ops) template has a default filter that excludes resource-specific records from a project task by setting the filter on **IsLineTask** to **False**.</span></span> <span data-ttu-id="aea56-134">独自のテンプレートを作成する場合は、このフィルターを追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="aea56-134">If you create your own template, you must add this filter.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="aea56-135">データ統合のテンプレートのマッピング</span><span class="sxs-lookup"><span data-stu-id="aea56-135">Template mapping in Data integration</span></span>

<span data-ttu-id="aea56-136">次の図は、データ インテグレーターのタスク マッピングの例を示します。</span><span class="sxs-lookup"><span data-stu-id="aea56-136">The following illustration shows an example of the template task mappings in Data integration.</span></span> <span data-ttu-id="aea56-137">マッピングは、Project Service Automation から Finance and Operations に同期するフィールド情報を表示します。</span><span class="sxs-lookup"><span data-stu-id="aea56-137">The mapping shows the field information that will be synchronized from Project Service Automation to Finance and Operations.</span></span>

<span data-ttu-id="aea56-138">[![テンプレートのマッピング](./media/ProjectTasksMapping.png)](./media/ProjectTasksMapping.png)</span><span class="sxs-lookup"><span data-stu-id="aea56-138">[![Template mapping](./media/ProjectTasksMapping.png)](./media/ProjectTasksMapping.png)</span></span>
