---
title: Project Service Automation
description: このトピックでは、Finance and Operations 統合ソリューションに対する Project Service Automation に関する情報を提供します。 この統合ソリューションは、データ統合機能を使用して、Common Data Service 経由で Microsoft Dynamics 365 for Finance and Operations のインスタンス、および Microsoft Dynamics 365 for Project Service Automation 間でデータを同期します。
author: KimANelson
manager: AnnBe
ms.date: 06/29/2018
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
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4b1d2ae69899a2937d47f6547ee4ba72b2d1ece4
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/15/2019
ms.locfileid: "1557309"
---
# <a name="project-service-automation"></a><span data-ttu-id="f4bc8-104">Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="f4bc8-104">Project Service Automation</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="f4bc8-105">Project Service Automation から Finance and Operations の統合ソリューションは、データの統合機能を使用して、Common Data Service 経由で Microsoft Dynamics 365 for Finance and Operations のインスタンスおよび Microsoft Dynamics 365 for Project Service Automation 間でデータを同期します。</span><span class="sxs-lookup"><span data-stu-id="f4bc8-105">The Project Service Automation to Finance and Operations integration solution uses the Data integration feature to synchronize data across instances of Microsoft Dynamics 365 for Finance and Operations and Microsoft Dynamics 365 for Project Service Automation via Common Data Service.</span></span> <span data-ttu-id="f4bc8-106">データの統合機能で使用可能な統合テンプレートは、Project Service Automation から Finance and Operations へのプロジェクト、プロジェクト契約、プロジェクト契約ライン、プロジェクト契約明細行のマイルストーン、プロジェクト タスク、経費トランザクション カテゴリ、時間見積、および経費見積の流れを有効にします。</span><span class="sxs-lookup"><span data-stu-id="f4bc8-106">The integration templates that are available with the Data integration feature enable the flow of projects, project contracts, project contract lines, project contract line milestones, project tasks, expense transaction categories, hour estimates, and expense estimates from Project Service Automation to Finance and Operations.</span></span>

> [!NOTE]
> - <span data-ttu-id="f4bc8-107">Microsoft Dynamics 365 for Finance and Operations、Enterprise edition 7.3.0 を使用している場合、KB 4132657 および KB 4132660 をインストールした後に、テンプレートを使用してプロジェクト タスクの統合、経費トランザクションのカテゴリ、時間見積、経費見積、実績、および機能ロックをコンフィギュレーションできます。</span><span class="sxs-lookup"><span data-stu-id="f4bc8-107">If you're using Microsoft Dynamics 365 for Finance and Operations, Enterprise edition 7.3.0, after you install KB 4132657 and KB 4132660, you will be able to use the templates to integrate project tasks, expense transaction categories, hour estimates, expense estimates, and actuals, and to configure functionality locking.</span></span> <span data-ttu-id="f4bc8-108">勘定配布をリセットする必要がある場合、KB 4131710 をインストールすることをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="f4bc8-108">If you must reset the accounting distributions, we recommend that you also install KB 4131710.</span></span>
> - <span data-ttu-id="f4bc8-109">Finance and Operations 7.3.0 を使用している場合は、KB 4074835 をインストールする必要があります。</span><span class="sxs-lookup"><span data-stu-id="f4bc8-109">If you're using Finance and Operations 7.3.0, you must install KB 4074835.</span></span> <span data-ttu-id="f4bc8-110">その後、固定価格プロジェクトを統合することができます。</span><span class="sxs-lookup"><span data-stu-id="f4bc8-110">You will then be able to integrate fixed price projects.</span></span>
> - <span data-ttu-id="f4bc8-111">Finance and Operations 7.3.0 を使用し、Project Service Automation から手数料トランザクションを挿入する場合は、プロジェクト請求書にそれらの手数料を含めるために KB 4345320 をインストールする必要があります。</span><span class="sxs-lookup"><span data-stu-id="f4bc8-111">If you're using Finance and Operations 7.3.0, and you are bringing fee transactions over from Project Service Automation, you must install KB 4345320 in order to include those fees in the project invoice.</span></span>
> - <span data-ttu-id="f4bc8-112">Microsoft Dynamics 365 for Finance and Operations バージョン 8.0 を使用している場合は、プロジェクト タスクの統合、経費トランザクションのカテゴリ、時間見積、経費見積、および機能ロックを使用できるようになります。</span><span class="sxs-lookup"><span data-stu-id="f4bc8-112">If you're using Microsoft Dynamics 365 for Finance and Operations version 8.0, you will be able to use project task integration, expense transaction categories, hour estimates, expense estimates, and functionality locking.</span></span>
> - <span data-ttu-id="f4bc8-113">Microsoft Dynamics 365 for Finance and Operations バージョン 8.0.1 以降を使用している場合は、実績を同期できます。</span><span class="sxs-lookup"><span data-stu-id="f4bc8-113">If you're using Microsoft Dynamics 365 for Finance and Operations version 8.0.1, or later, you will be able to synchronize actuals.</span></span>

<span data-ttu-id="f4bc8-114">Project Service Automation を Finance and Operations と統合する前に、Project Service Automation の統合パラメーターをコンフィギュレーションする必要があります。</span><span class="sxs-lookup"><span data-stu-id="f4bc8-114">Before you can integrate Project Service Automation with Finance and Operations, you must configure the Project Service Automation integration parameters.</span></span> <span data-ttu-id="f4bc8-115">詳細については、[Project Service Automation 統合パラメーター](PSA-parameters.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="f4bc8-115">For more information, see [Project Service Automation integration parameters](PSA-parameters.md).</span></span>

<span data-ttu-id="f4bc8-116">統合ソリューションにより、次のシナリオで直接同期できます。</span><span class="sxs-lookup"><span data-stu-id="f4bc8-116">This integration solution enables direct synchronization in the following scenarios:</span></span>

- <span data-ttu-id="f4bc8-117">Project Service Automation でプロジェクト契約を管理し、Project Service Automation から Finance and Operations に直接同期させます。</span><span class="sxs-lookup"><span data-stu-id="f4bc8-117">Maintain project contracts in Project Service Automation, and synchronize them directly from Project Service Automation to Finance and Operations.</span></span>
- <span data-ttu-id="f4bc8-118">Project Service Automation でプロジェクトを作成し、Project Service Automation から Finance and Operations に直接同期させます。</span><span class="sxs-lookup"><span data-stu-id="f4bc8-118">Create projects in Project Service Automation, and synchronize them directly from Project Service Automation to Finance and Operations.</span></span>
- <span data-ttu-id="f4bc8-119">Project Service Automation でプロジェクト契約明細行を管理し、Project Service Automation から Finance and Operations に直接同期させます。</span><span class="sxs-lookup"><span data-stu-id="f4bc8-119">Maintain project contract lines in Project Service Automation, and synchronize them directly from Project Service Automation to Finance and Operations.</span></span>
- <span data-ttu-id="f4bc8-120">Project Service Automation でプロジェクト契約明細行のマイルストーンを管理し、Project Service Automation から Finance and Operations に直接同期させます。</span><span class="sxs-lookup"><span data-stu-id="f4bc8-120">Maintain project contract line milestones in Project Service Automation, and synchronize them directly from Project Service Automation to Finance and Operations.</span></span>
- <span data-ttu-id="f4bc8-121">Project Service Automation でプロジェクト タスクを管理し、Project Service Automation から Finance and Operations に直接同期させます。</span><span class="sxs-lookup"><span data-stu-id="f4bc8-121">Maintain project tasks in Project Service Automation, and synchronize them directly from Project Service Automation to Finance and Operations.</span></span>
- <span data-ttu-id="f4bc8-122">Finance and Operations で経費トランザクション カテゴリを管理し、Finance and Operations から Project Service Automation に直接同期させます。</span><span class="sxs-lookup"><span data-stu-id="f4bc8-122">Maintain expense transaction categories in Finance and Operations, and synchronize them directly from Finance and Operations to Project Service Automation.</span></span>
- <span data-ttu-id="f4bc8-123">Project Service Automation でプロジェクト時間見積を作成し、Project Service Automation から Finance and Operations に直接同期させます。</span><span class="sxs-lookup"><span data-stu-id="f4bc8-123">Create project hour estimates in Project Service Automation, and synchronize them directly from Project Service Automation to Finance and Operations.</span></span>
- <span data-ttu-id="f4bc8-124">Project Service Automation でプロジェクト経費見積を作成し、Project Service Automation から Finance and Operations に直接同期させます。</span><span class="sxs-lookup"><span data-stu-id="f4bc8-124">Create project expense estimates in Project Service Automation, and synchronize them directly from Project Service Automation to Finance and Operations.</span></span>
- <span data-ttu-id="f4bc8-125">Project Service Automation でプロジェクト時間、経費、および手数料の実績を作成し、Finance and Operations に転記できるように、Project Service Automation 統合仕訳帳でプロジェクト トランザクションを作成します。</span><span class="sxs-lookup"><span data-stu-id="f4bc8-125">Create project time, expense, and fee actuals in Project Service Automation, and create project transactions in the Project Service Automation integration journal so that they can be posted in Finance and Operations.</span></span>

## <a name="data-synchronization"></a><span data-ttu-id="f4bc8-126">データ同期</span><span class="sxs-lookup"><span data-stu-id="f4bc8-126">Data synchronization</span></span>

<span data-ttu-id="f4bc8-127">次の図は、データが Project Service Automation と Finance and Operations との間で統合の一部として同期される方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="f4bc8-127">The following illustration shows how data is synchronized as part of the integration between Project Service Automation and Finance and Operations.</span></span>

> [!NOTE]
> <span data-ttu-id="f4bc8-128">現在利用可能なテンプレートはありません。</span><span class="sxs-lookup"><span data-stu-id="f4bc8-128">Not all templates are currently available.</span></span> <span data-ttu-id="f4bc8-129">完了するとテンプレートがリリースされます。</span><span class="sxs-lookup"><span data-stu-id="f4bc8-129">Templates will be released as they are completed.</span></span>

<span data-ttu-id="f4bc8-130">[![Project Service Automation を Finance and Operations と統合](./media/PSA-integration.png)](./media/PSA-integration.png)</span><span class="sxs-lookup"><span data-stu-id="f4bc8-130">[![Project Service Automation integration with Finance and Operations](./media/PSA-integration.png)](./media/PSA-integration.png)</span></span>

## <a name="system-requirements-for-finance-and-operations"></a><span data-ttu-id="f4bc8-131">Finance and Operations のシステム要件</span><span class="sxs-lookup"><span data-stu-id="f4bc8-131">System requirements for Finance and Operations</span></span>

<span data-ttu-id="f4bc8-132">Finance and Operations 統合ソリューションに対して Project Service Automation を使用するには、Microsoft Dynamics 365 for Finance and Operations、Enterprise edition 7.3 およびプラットフォーム更新プログラム 12 またはそれ以降のバージョンをインストールする必要があります。</span><span class="sxs-lookup"><span data-stu-id="f4bc8-132">To use the Project Service Automation to Finance and Operations integration solution, you must install Microsoft Dynamics 365 for Finance and Operations, Enterprise edition 7.3 with platform update 12 or later.</span></span>

## <a name="system-requirements-for-project-service-automation"></a><span data-ttu-id="f4bc8-133">Project Service Automation のシステム要件</span><span class="sxs-lookup"><span data-stu-id="f4bc8-133">System requirements for Project Service Automation</span></span>

<span data-ttu-id="f4bc8-134">Finance and Operations 統合ソリューションに対して Project Service Automation を使用するには、次のコンポーネントをインストールする必要があります。</span><span class="sxs-lookup"><span data-stu-id="f4bc8-134">To use the Project Service Automation to Finance and Operations integration solution, you must install the following components:</span></span>

- <span data-ttu-id="f4bc8-135">Microsoft Dynamics 365 for Project Service Automation バージョン 9.0.0.0 以降</span><span class="sxs-lookup"><span data-stu-id="f4bc8-135">Microsoft Dynamics 365 for Project Service Automation version 9.0.0.0 or later</span></span>
- <span data-ttu-id="f4bc8-136">Microsoft Dynamics 365 for Sales バージョン 1.14.0.0 (v14) またはそれ以降の見込顧客を現金化するソリューション。</span><span class="sxs-lookup"><span data-stu-id="f4bc8-136">Prospect to cash solution for Microsoft Dynamics 365 for Sales, version 1.14.0.0 (v14) or later</span></span>
- <span data-ttu-id="f4bc8-137">Microsoft Dynamics 365 for Project Service Automation バージョン 1.0.0.0 以降の Finance and Operations ソリューションに対する Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="f4bc8-137">Project Service Automation to Finance and Operations solution for Microsoft Dynamics 365 for Project Service Automation version 1.0.0.0 or later</span></span>

## <a name="install-the-project-service-automation-to-finance-and-operations-integration-solution-in-your-project-service-automation-instance"></a><span data-ttu-id="f4bc8-138">Project Service Automation インスタンス に Finance and Operations 統合ソリューションに対する Project Service Automation をインストールします</span><span class="sxs-lookup"><span data-stu-id="f4bc8-138">Install the Project Service Automation to Finance and Operations integration solution in your Project Service Automation instance</span></span>

<span data-ttu-id="f4bc8-139">[Microsoft ダウンロード センター](https://www.microsoft.com/en-us/download/details.aspx?id=57016) から Finance and Operations ソリューションに対する Project Service Automation をダウンロードし、ソリューションに含まれている手順に従ってください。</span><span class="sxs-lookup"><span data-stu-id="f4bc8-139">Download the Project Service Automation to Finance and Operations integration solution from [Microsoft Download Center](https://www.microsoft.com/en-us/download/details.aspx?id=57016), and follow the instructions that are included with the solution.</span></span>
