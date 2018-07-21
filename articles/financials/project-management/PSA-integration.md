---
title: Project Service Automation
description: "このソリューションは、データ統合機能を使用して、Common Data Service (CDS) 経由で Microsoft Dynamics 365 for Finance and Operations のインスタンス、および Microsoft Dynamics 365 for Project Service Automation 間でデータを同期します。"
author: KimANelson
manager: AnnBe
ms.date: 11/27/2017
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
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: bd8feff598cf80ca675c7d2b5dda636799b19e29
ms.openlocfilehash: 0ad9e6ba7fe8dd915681da8e671ff210de887b1e
ms.contentlocale: ja-jp
ms.lasthandoff: 05/29/2018

---

# <a name="project-service-automation"></a><span data-ttu-id="53a21-103">Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="53a21-103">Project Service Automation</span></span>

<span data-ttu-id="53a21-104">Project Service Automation から Finance and Operations への統合のソリューションは、データ統合機能を使用して、Common Data Service (CDS) 経由で Microsoft Dynamics 365 for Finance and Operations のインスタンス、および Microsoft Dynamics 365 for Project Service Automation 間でデータを同期します。</span><span class="sxs-lookup"><span data-stu-id="53a21-104">The Project Service Automation to Finance and Operations integration solution uses the Data Integration feature to synchronize data across instances of Microsoft Dynamics 365 for Finance and Operations and Microsoft Dynamics 365 for Project Service Automation via the Common Data Service (CDS).</span></span> <span data-ttu-id="53a21-105">データの統合機能で使用可能な統合テンプレートは、Project Service Automation から Finance and Operations へのプロジェクト、プロジェクト契約、プロジェクト契約ライン、プロジェクト契約明細行のマイルストーン、プロジェクト タスク、経費トランザクション カテゴリ、時間見積、および経費見積の流れを有効にします。</span><span class="sxs-lookup"><span data-stu-id="53a21-105">The integration templates that are available with the Data Integration feature enable the flow of projects, project contracts, project contract lines, project contract line milestones, project tasks, expense transaction categories, hour estimates, and expense estimates from Project Service Automation to Finance and Operations.</span></span>

> [!NOTE] 
> <span data-ttu-id="53a21-106">Dynamics 365 for Finance and Operations、Enterprise edition 7.3.0 を使用している場合、KB 4074835 をインストールする必要があります。</span><span class="sxs-lookup"><span data-stu-id="53a21-106">If you are using Dynamics 365 for Finance and Operations, Enterprise edition 7.3.0, you must install KB 4074835.</span></span> <span data-ttu-id="53a21-107">これにより、固定価格プロジェクトを統合することができます。</span><span class="sxs-lookup"><span data-stu-id="53a21-107">This will allow you to integrate fixed price projects.</span></span>
>
> <span data-ttu-id="53a21-108">Dynamics 365 for Finance and Operations バージョン 8.0 を使用している場合は、プロジェクト タスクの統合、経費トランザクションのカテゴリ、時間見積、経費見積、および機能ロックを使用できるようになります。</span><span class="sxs-lookup"><span data-stu-id="53a21-108">If you are using Dynamics 365 for Finance and Operations version 8.0, you will be able to use project tasks integration, expense transaction categories, hour estimates, expense estimates, and functionality locking.</span></span>
>
> <span data-ttu-id="53a21-109">Dynamics 365 for Finance and Operations バージョン 8.0.1 を使用している場合は、実績を同期することができます。</span><span class="sxs-lookup"><span data-stu-id="53a21-109">If you are using Dynamics 365 for Finance and Operations version 8.0.1, you will be able to synchronize actuals.</span></span>
>
> <span data-ttu-id="53a21-110">Dynamics 365 for Finance and Operations、Enterprise edition 7.3.0 を使用している場合、KB 4132657 および KB 4132660 をインストールした後に、テンプレートを使用してプロジェクト タスクの統合、経費トランザクションのカテゴリ、時間見積、経費見積、実績、および機能ロックをコンフィギュレーションできます。</span><span class="sxs-lookup"><span data-stu-id="53a21-110">If you are using Dynamics 365 for Finance and Operations, Enterprise edition 7.3.0, after you install KB 4132657 and KB 4132660, you will be able to use the templates to integrate project tasks, expense transaction categories, hour estimates, expense estimates, and actuals, and to configure functionality locking.</span></span> <span data-ttu-id="53a21-111">勘定配布をリセットする必要がある場合、KB 4131710 をインストールすることをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="53a21-111">If you must reset the accounting distributions, we recommend that you also install KB 4131710.</span></span>

<span data-ttu-id="53a21-112">Project Service Automation を Finance and Operations と統合する前に、Project Service Automation の統合パラメーターをコンフィギュレーションする必要があります。</span><span class="sxs-lookup"><span data-stu-id="53a21-112">Before you can integrate Project Service Automation with Finance and Operations, you must configure the Project Service Automation integration parameters.</span></span> <span data-ttu-id="53a21-113">詳細については、Project Service Automation の統合パラメーターを参照してください。</span><span class="sxs-lookup"><span data-stu-id="53a21-113">For more information, see Project Service Automation integration parameters.</span></span>

<span data-ttu-id="53a21-114">統合ソリューションにより、次のシナリオで直接同期できます。</span><span class="sxs-lookup"><span data-stu-id="53a21-114">This integration solution enables direct synchronization in the following scenarios:</span></span>

- <span data-ttu-id="53a21-115">Project Service Automation でプロジェクト契約を管理し、Project Service Automation から Finance and Operations に直接同期させます。</span><span class="sxs-lookup"><span data-stu-id="53a21-115">Maintain project contracts in Project Service Automation, and synchronize them directly from Project Service Automation to Finance and Operations.</span></span>
- <span data-ttu-id="53a21-116">Project Service Automation でプロジェクトを作成し、Project Service Automation から Finance and Operations に直接同期させます。</span><span class="sxs-lookup"><span data-stu-id="53a21-116">Create projects in Project Service Automation, and synchronize them directly from Project Service Automation to Finance and Operations.</span></span>
- <span data-ttu-id="53a21-117">Project Service Automation でプロジェクト契約明細行を管理し、Project Service Automation から Finance and Operations に直接同期させます。</span><span class="sxs-lookup"><span data-stu-id="53a21-117">Maintain project contract lines in Project Service Automation, and synchronize them directly from Project Service Automation to Finance and Operations.</span></span>
- <span data-ttu-id="53a21-118">Project Service Automation でプロジェクト契約明細行のマイルストーンを管理し、Project Service Automation から Finance and Operations に直接同期させます。</span><span class="sxs-lookup"><span data-stu-id="53a21-118">Maintain project contract line milestones in Project Service Automation, and synchronize them directly from Project Service Automation to Finance and Operations.</span></span>
- <span data-ttu-id="53a21-119">Project Service Automation でプロジェクト タスクを管理し、Project Service Automation から Finance and Operations に直接同期させます。</span><span class="sxs-lookup"><span data-stu-id="53a21-119">Maintain project tasks in Project Service Automation, and synchronize them directly from Project Service Automation to Finance and Operations.</span></span>
- <span data-ttu-id="53a21-120">Finance and Operations で経費トランザクション カテゴリを管理し、Finance and Operations から Project Service Automation に直接同期させます。</span><span class="sxs-lookup"><span data-stu-id="53a21-120">Maintain expense transaction categories in Finance and Operations, and synchronize them directly from Finance and Operations to Project Service Automation.</span></span>
- <span data-ttu-id="53a21-121">Project Service Automation でプロジェクト時間見積を作成し、Project Service Automation から Finance and Operations に直接同期させます。</span><span class="sxs-lookup"><span data-stu-id="53a21-121">Create project hour estimates in Project Service Automation, and synchronize them directly from Project Service Automation to Finance and Operations.</span></span>
- <span data-ttu-id="53a21-122">Project Service Automation でプロジェクト経費見積を作成し、Project Service Automation から Finance and Operations に直接同期させます。</span><span class="sxs-lookup"><span data-stu-id="53a21-122">Create project expense estimates in Project Service Automation, and synchronize them directly from Project Service Automation to Finance and Operations.</span></span>

## <a name="data-synchronization"></a><span data-ttu-id="53a21-123">データ同期</span><span class="sxs-lookup"><span data-stu-id="53a21-123">Data synchronization</span></span>
<span data-ttu-id="53a21-124">次の図は、データが Project Service Automation と Finance and Operations との間で統合の一部として同期される方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="53a21-124">The following illustration shows how data is synchronized as part of the integration between Project Service Automation and Finance and Operations.</span></span>

> [!NOTE]
> <span data-ttu-id="53a21-125">現在利用可能なテンプレートはありません。</span><span class="sxs-lookup"><span data-stu-id="53a21-125">Not all templates are currently available.</span></span> <span data-ttu-id="53a21-126">完了するとテンプレートがリリースされます。</span><span class="sxs-lookup"><span data-stu-id="53a21-126">Templates will be released as they are completed.</span></span>

<span data-ttu-id="53a21-127">[![Project Service Automation を Finance and Operations と統合](./media/PSA-integration.png)](./media/PSA-integration.png)</span><span class="sxs-lookup"><span data-stu-id="53a21-127">[![Project Service Automation integration with Finance and Operations](./media/PSA-integration.png)](./media/PSA-integration.png)</span></span>

## <a name="system-requirements-for-finance-and-operations"></a><span data-ttu-id="53a21-128">Finance and Operations のシステム要件</span><span class="sxs-lookup"><span data-stu-id="53a21-128">System requirements for Finance and Operations</span></span>

<span data-ttu-id="53a21-129">Finance and Operations 統合ソリューションに対して Project Service Automation を使用するには、Microsoft Dynamics 365 for Finance and Operations、Enterprise edition 7.3 およびプラットフォーム更新プログラム 12 またはそれ以降のバージョンをインストールする必要があります。</span><span class="sxs-lookup"><span data-stu-id="53a21-129">To use the Project Service Automation to Finance and Operations integration solution, you must install Microsoft Dynamics 365 for Finance and Operations, Enterprise edition 7.3 with platform update 12 or later.</span></span>

## <a name="system-requirements-for-project-service-automation"></a><span data-ttu-id="53a21-130">Project Service Automation のシステム要件</span><span class="sxs-lookup"><span data-stu-id="53a21-130">System requirements for Project Service Automation</span></span>

<span data-ttu-id="53a21-131">Finance and Operations 統合ソリューションに対して Project Service Automation を使用するには、次のコンポーネントをインストールする必要があります。</span><span class="sxs-lookup"><span data-stu-id="53a21-131">To use the Project Service Automation to Finance and Operations integration solution, you must install the following components:</span></span>

- <span data-ttu-id="53a21-132">Microsoft Dynamics 365 for Project Service Automation バージョン 9.0.0.0 以降。</span><span class="sxs-lookup"><span data-stu-id="53a21-132">Microsoft Dynamics 365 for Project Service Automation version 9.0.0.0 or later.</span></span>
- <span data-ttu-id="53a21-133">Dynamics 365 for Sales バージョン 1.14.0.0 (v14) またはそれ以降の見込顧客を現金化するソリューション。</span><span class="sxs-lookup"><span data-stu-id="53a21-133">Prospect to cash solution for Dynamics 365 for Sales, version 1.14.0.0 (v14) or later.</span></span>
- <span data-ttu-id="53a21-134">Dynamics 365 for Project Service Automation バージョン 1.0.0.0 以降の Operations ソリューションに対する Project Service Automation。</span><span class="sxs-lookup"><span data-stu-id="53a21-134">Project Service Automation to Operations solution for Dynamics 365 for Project Service Automation version 1.0.0.0 or later.</span></span>

## <a name="install-the-project-service-automation-to-finance-and-operations-integration-solution-in-your-project-service-automation-instance"></a><span data-ttu-id="53a21-135">Project Service Automation インスタンス に Finance and Operations 統合ソリューションに対する Project Service Automation をインストールします</span><span class="sxs-lookup"><span data-stu-id="53a21-135">Install the Project Service Automation to Finance and Operations integration solution in your Project Service Automation instance</span></span>



