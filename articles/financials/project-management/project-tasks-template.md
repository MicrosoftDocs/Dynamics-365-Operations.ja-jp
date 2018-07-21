---
title: "Project Service Automation からプロジェクト タスクを同期する"
description: "このトピックでは、Microsoft Dynamics 365 for Project Service Automation から Dynamics 365 for Finance and Operations へ直接プロジェクト タスクを同期させるために使用されるテンプレートと基本的なタスクについて説明します。"
author: KimANelson
manager: AnnBe
ms.date: 04/02/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.3.0
ms.translationtype: HT
ms.sourcegitcommit: 399b519ab0da4de405aeb06f3e7f4bf29a6c5cc3
ms.openlocfilehash: 89df0d99d780441ad08cd6bff3e1fd203694eb8e
ms.contentlocale: ja-jp
ms.lasthandoff: 05/30/2018

---

# <a name="synchronize-project-tasks-from-project-service-automation-directly-to-project-activities-in-finance-and-operations"></a><span data-ttu-id="a5bdc-103">Project Service Automation からプロジェクト タスクを直接プロジェクト活動の Finance and Operations に同期します。</span><span class="sxs-lookup"><span data-stu-id="a5bdc-103">Synchronize project tasks from Project Service Automation directly to project activities in Finance and Operations</span></span>

<span data-ttu-id="a5bdc-104">このトピックでは、Microsoft Dynamics 365 for Project Service Automation から Dynamics 365 for Finance and Operations へ直接プロジェクト タスクを同期させるために使用されるテンプレートと基本的なタスクについて説明します。</span><span class="sxs-lookup"><span data-stu-id="a5bdc-104">This topic describes the template and underlying task that is used to synchronize project tasks directly from Microsoft Dynamics 365 for Project Service Automation to Dynamics 365 for Finance and Operations.</span></span>

> [!NOTE]
> <span data-ttu-id="a5bdc-105">プロジェクト タスクの統合、経費トランザクションのカテゴリ、時間見積、経費見積、および機能ロックは、Dynamics 365 for Finance and Operations バージョン 8.0 で利用できます。</span><span class="sxs-lookup"><span data-stu-id="a5bdc-105">Project tasks integration, expense transaction categories, hour estimates, expense estimates, and functionality locking is available in Dynamics 365 for Finance and Operations version 8.0.</span></span>

## <a name="data-flow-for-project-service-automation-to-finance-and-operations"></a><span data-ttu-id="a5bdc-106">Project Service Automation から Finance and Operations のデータ フロー</span><span class="sxs-lookup"><span data-stu-id="a5bdc-106">Data flow for Project Service Automation to Finance and Operations</span></span>

<span data-ttu-id="a5bdc-107">Project Service Automation から Finance and Operations の統合ソリューションは、データの統合機能を使用して Project Service Automation および Finance and Operations のインスタンス間でデータを同期させます。</span><span class="sxs-lookup"><span data-stu-id="a5bdc-107">The Project Service Automation to Finance and Operations integration solution uses the Data integration feature to synchronize data across instances of Project Service Automation and Finance and Operations.</span></span> <span data-ttu-id="a5bdc-108">データ統合機能で利用できる統合テンプレートを使用すると、Project Service Automation から Finance and Operations にプロジェクト タスクに関するデータ フローを有効にします。</span><span class="sxs-lookup"><span data-stu-id="a5bdc-108">The integration template that is available with the Data integration feature enables the flow of data about project tasks from Project Service Automation to Finance and Operations.</span></span>

<span data-ttu-id="a5bdc-109">次の図は、データが Project Service Automation と Finance and Operations との間で同期される方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="a5bdc-109">The following illustration shows how the data is synchronized between Project Service Automation and Finance and Operations.</span></span>

<span data-ttu-id="a5bdc-110">[![Project Service Automation のデータ フローを Finance and Operations と統合](./media/ProjectTasksFlow.png)](./media/ProjectTasksFlow.png)</span><span class="sxs-lookup"><span data-stu-id="a5bdc-110">[![Data flow for Project Service Automation integration with Finance and Operations](./media/ProjectTasksFlow.png)](./media/ProjectTasksFlow.png)</span></span>

## <a name="template-and-task"></a><span data-ttu-id="a5bdc-111">テンプレートおよびタスク</span><span class="sxs-lookup"><span data-stu-id="a5bdc-111">Template and task</span></span>

<span data-ttu-id="a5bdc-112">テンプレートにアクセスするには、Microsoft PowerApps の管理者センターで**プロジェクト**を選択、次に右上隅にある**新規プロジェクト**を選択しパブリック テンプレートを選択します。</span><span class="sxs-lookup"><span data-stu-id="a5bdc-112">To access the template, in the Microsoft PowerApps Admin Center, select **Projects**, and then, in the upper-right corner, select **New project** to select public templates.</span></span>

<span data-ttu-id="a5bdc-113">次のテンプレートおよび基本的なタスクは Project Service Automation から Finance and Operations プロジェクト タスクを同期させるために使用されます。</span><span class="sxs-lookup"><span data-stu-id="a5bdc-113">The following template and underlying task is used to synchronize project tasks from Project Service Automation to Finance and Operations:</span></span>

<span data-ttu-id="a5bdc-114">-**データ統合のテンプレートの名前:** プロジェクト タスク (Project Service Automation から Finance and Operations) - **プロジェクトのタスクの名前:** プロジェクト タスク</span><span class="sxs-lookup"><span data-stu-id="a5bdc-114">-**Name of the template in Data integration:** Project tasks (PSA to Fin and Ops) -**Name of the task in the project:** Project tasks</span></span>

<span data-ttu-id="a5bdc-115">プロジェクト タスクの同期を行う前に、プロジェクト契約とプロジェクトを同期する必要があります。</span><span class="sxs-lookup"><span data-stu-id="a5bdc-115">Before synchronization of project tasks can occur, you must synchronize project contracts and projects.</span></span>

## <a name="entity-set"></a><span data-ttu-id="a5bdc-116">エンティティ セット</span><span class="sxs-lookup"><span data-stu-id="a5bdc-116">Entity set</span></span>

|<span data-ttu-id="a5bdc-117">Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="a5bdc-117">Project Service Automation</span></span>               | <span data-ttu-id="a5bdc-118">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="a5bdc-118">Finance and Operations</span></span>                |
|-----------------------------------------|---------------------------------------|
| <span data-ttu-id="a5bdc-119">プロジェクト タスク</span><span class="sxs-lookup"><span data-stu-id="a5bdc-119">Project Tasks</span></span>                           | <span data-ttu-id="a5bdc-120">統合エンティティのプロジェクト タスク。</span><span class="sxs-lookup"><span data-stu-id="a5bdc-120">Integration entity for project task.</span></span>   |

## <a name="entity-flow"></a><span data-ttu-id="a5bdc-121">エンティティのフロー</span><span class="sxs-lookup"><span data-stu-id="a5bdc-121">Entity flow</span></span>

<span data-ttu-id="a5bdc-122">プロジェクト タスクは Project Service Automation で管理され、プロジェクト活動として Finance and Operations に同期されます。</span><span class="sxs-lookup"><span data-stu-id="a5bdc-122">Project tasks are managed in Project Service Automation, and they are synchronized to Finance and Operations as project activities.</span></span>

## <a name="prerequisites-and-mapping-setup"></a><span data-ttu-id="a5bdc-123">前提条件およびマッピングの設定</span><span class="sxs-lookup"><span data-stu-id="a5bdc-123">Prerequisites and mapping setup</span></span>

<span data-ttu-id="a5bdc-124">プロジェクト タスクの同期を行う前に、プロジェクト契約とプロジェクトを同期する必要があります。</span><span class="sxs-lookup"><span data-stu-id="a5bdc-124">Before synchronization of project tasks can occur, you must synchronize project contracts and projects.</span></span>

## <a name="power-query"></a><span data-ttu-id="a5bdc-125">Power Query</span><span class="sxs-lookup"><span data-stu-id="a5bdc-125">Power Query</span></span>

<span data-ttu-id="a5bdc-126">これらの条件が満たされた場合、フィルター処理する Microsoft Power Query を使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="a5bdc-126">You must use Microsoft Power Query to filter data if these conditions are met:</span></span>

- <span data-ttu-id="a5bdc-127">プロジェクト タスク内のリソース特定のレコードがあります。</span><span class="sxs-lookup"><span data-stu-id="a5bdc-127">You have resource specific records within a project task.</span></span>

<span data-ttu-id="a5bdc-128">Power Query を使用する必要がある場合は、これらのガイドラインに従います。</span><span class="sxs-lookup"><span data-stu-id="a5bdc-128">If you must use Power Query, follow these guidelines:</span></span>

- <span data-ttu-id="a5bdc-129">プロジェクト タスク (Project Service Automation から Finance and Operations) テンプレートは、既定のフィルターに **IsLineTask** から **False** のフィルターを設定することでプロジェクト タスク内のリソース特定レコードを除外できます。</span><span class="sxs-lookup"><span data-stu-id="a5bdc-129">The Project tasks (PSA to Fin and Ops) template has a default filter to exclude resource specific records from within a project task by setting the filter on the **IsLineTask** to **False**.</span></span> <span data-ttu-id="a5bdc-130">独自のテンプレートを作成する場合は、このフィルターを追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="a5bdc-130">If you create your own template, you must add this filter.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="a5bdc-131">データ統合のテンプレートのマッピング</span><span class="sxs-lookup"><span data-stu-id="a5bdc-131">Template mapping in Data integration</span></span>

<span data-ttu-id="a5bdc-132">次の図は、データ インテグレーターのタスク マッピングの例を示します。</span><span class="sxs-lookup"><span data-stu-id="a5bdc-132">The following illustration shows an example of the template task mappings in Data integration.</span></span> <span data-ttu-id="a5bdc-133">マッピングは、Project Service Automation から Finance and Operations に同期するフィールド情報を表示します。</span><span class="sxs-lookup"><span data-stu-id="a5bdc-133">The mapping shows the field information that will be synchronized from Project Service Automation to Finance and Operations.</span></span>

<span data-ttu-id="a5bdc-134">[![テンプレートのマッピング](./media/ProjectTasksMapping.png)](./media/ProjectTasksMapping.png)</span><span class="sxs-lookup"><span data-stu-id="a5bdc-134">[![Template mapping](./media/ProjectTasksMapping.png)](./media/ProjectTasksMapping.png)</span></span>


