---
title: Project Service Automation の概要
description: このトピックでは、Dynamics 365 Project Service Automation から Dynamics 365 Finance への統合について説明します。
author: KimANelson
manager: AnnBe
ms.date: 07/25/2019
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
ms.openlocfilehash: 31d72591041f8d8cc327aa7c6578c15731ba13c5
ms.sourcegitcommit: 2460d0da812c45fce67a061386db52e0ae46b0f3
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/30/2019
ms.locfileid: "2250556"
---
# <a name="project-service-automation-overview"></a><span data-ttu-id="c1a84-103">Project Service Automation の概要</span><span class="sxs-lookup"><span data-stu-id="c1a84-103">Project Service Automation overview</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="c1a84-104">Project Service Automation から Finance の統合ソリューションは、データの統合機能を使用して、Common Data Service 経由で Dynamics 365 Finance のインスタンスおよび Dynamics 365 Project Service Automation 間でデータを同期します。</span><span class="sxs-lookup"><span data-stu-id="c1a84-104">The Project Service Automation to Finance integration solution uses the Data integration feature to synchronize data across instances of Dynamics 365 Finance and Dynamics 365 Project Service Automation via Common Data Service.</span></span> <span data-ttu-id="c1a84-105">データの統合機能で使用可能な統合テンプレートは、Project Service Automation から Finance へのプロジェクト、プロジェクト契約、プロジェクト契約ライン、プロジェクト契約明細行のマイルストーン、プロジェクト タスク、経費トランザクション カテゴリ、時間見積、および経費見積の流れを有効にします。</span><span class="sxs-lookup"><span data-stu-id="c1a84-105">The integration templates that are available with the Data integration feature enable the flow of projects, project contracts, project contract lines, project contract line milestones, project tasks, expense transaction categories, hour estimates, and expense estimates from Project Service Automation to Finance.</span></span>

> [!NOTE]
> - <span data-ttu-id="c1a84-106">バージョン 7.3.0 を使用している場合は、KB 4074835 をインストールする必要があります。</span><span class="sxs-lookup"><span data-stu-id="c1a84-106">If you're using version 7.3.0, you must install KB 4074835.</span></span> <span data-ttu-id="c1a84-107">その後、固定価格プロジェクトを統合することができます。</span><span class="sxs-lookup"><span data-stu-id="c1a84-107">You will then be able to integrate fixed price projects.</span></span>
> - <span data-ttu-id="c1a84-108">バージョン 7.3.0 を使用し、Project Service Automation から手数料トランザクションを挿入する場合は、プロジェクト請求書にそれらの手数料を含めるために KB 4345320 をインストールする必要があります。</span><span class="sxs-lookup"><span data-stu-id="c1a84-108">If you're using version 7.3.0, and you are bringing fee transactions over from Project Service Automation, you must install KB 4345320 in order to include those fees in the project invoice.</span></span>
> - <span data-ttu-id="c1a84-109">バージョン 8.0 を使用している場合は、プロジェクト タスクの統合、経費トランザクションのカテゴリ、時間見積、経費見積、および機能ロックを使用できるようになります。</span><span class="sxs-lookup"><span data-stu-id="c1a84-109">If you're using version 8.0, you will be able to use project task integration, expense transaction categories, hour estimates, expense estimates, and functionality locking.</span></span>
> - <span data-ttu-id="c1a84-110">バージョン 8.0.1 以降を使用している場合は、実績を同期できます。</span><span class="sxs-lookup"><span data-stu-id="c1a84-110">If you're using version 8.0.1 or later, you will be able to synchronize actuals.</span></span>

<span data-ttu-id="c1a84-111">Project Service Automation Finance を統合する前に、Project Service Automation の統合パラメーターをコンフィギュレーションする必要があります。</span><span class="sxs-lookup"><span data-stu-id="c1a84-111">Before you can integrate Project Service Automation Finance, you must configure the Project Service Automation integration parameters.</span></span> <span data-ttu-id="c1a84-112">詳細については、[Project Service Automation 統合パラメーター](PSA-parameters.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="c1a84-112">For more information, see [Project Service Automation integration parameters](PSA-parameters.md).</span></span>

<span data-ttu-id="c1a84-113">統合ソリューションにより、次のシナリオで直接同期できます。</span><span class="sxs-lookup"><span data-stu-id="c1a84-113">This integration solution enables direct synchronization in the following scenarios:</span></span>

- <span data-ttu-id="c1a84-114">Project Service Automation でプロジェクト契約を管理し、Project Service Automation から Finance に直接同期させます。</span><span class="sxs-lookup"><span data-stu-id="c1a84-114">Maintain project contracts in Project Service Automation, and synchronize them directly from Project Service Automation to Finance.</span></span>
- <span data-ttu-id="c1a84-115">Project Service Automation でプロジェクトを作成し、Project Service Automation から Finance に直接同期させます。</span><span class="sxs-lookup"><span data-stu-id="c1a84-115">Create projects in Project Service Automation, and synchronize them directly from Project Service Automation to Finance.</span></span>
- <span data-ttu-id="c1a84-116">Project Service Automation でプロジェクト契約明細行を管理し、Project Service Automation から Finance に直接同期させます。</span><span class="sxs-lookup"><span data-stu-id="c1a84-116">Maintain project contract lines in Project Service Automation, and synchronize them directly from Project Service Automation to Finance.</span></span>
- <span data-ttu-id="c1a84-117">Project Service Automation でプロジェクト契約明細行のマイルストーンを管理し、Project Service Automation から Finance に直接同期させます。</span><span class="sxs-lookup"><span data-stu-id="c1a84-117">Maintain project contract line milestones in Project Service Automation, and synchronize them directly from Project Service Automation to Finance.</span></span>
- <span data-ttu-id="c1a84-118">Project Service Automation でプロジェクト タスクを管理し、Project Service Automation から Finance に直接同期させます。</span><span class="sxs-lookup"><span data-stu-id="c1a84-118">Maintain project tasks in Project Service Automation, and synchronize them directly from Project Service Automation to Finance.</span></span>
- <span data-ttu-id="c1a84-119">Finance で経費トランザクション カテゴリを管理し、Finance から Project Service Automation に直接同期させます。</span><span class="sxs-lookup"><span data-stu-id="c1a84-119">Maintain expense transaction categories in Finance, and synchronize them directly from Finance to Project Service Automation.</span></span>
- <span data-ttu-id="c1a84-120">Project Service Automation でプロジェクト時間見積を作成し、Project Service Automation から Finance に直接同期させます。</span><span class="sxs-lookup"><span data-stu-id="c1a84-120">Create project hour estimates in Project Service Automation, and synchronize them directly from Project Service Automation to Finance.</span></span>
- <span data-ttu-id="c1a84-121">Project Service Automation でプロジェクト経費の見積を作成し、Project Service Automation から Finance に直接同期させます。</span><span class="sxs-lookup"><span data-stu-id="c1a84-121">Create project expense estimates in Project Service Automation, and synchronize them directly from Project Service Automation to Finance.</span></span>
- <span data-ttu-id="c1a84-122">Project Service Automation でプロジェクト時間、経費、および手数料の実績を作成し、Finance に転記できるように、Project Service Automation 統合仕訳帳でプロジェクト トランザクションを作成します。</span><span class="sxs-lookup"><span data-stu-id="c1a84-122">Create project time, expense, and fee actuals in Project Service Automation, and create project transactions in the Project Service Automation integration journal so that they can be posted in Finance.</span></span>

## <a name="data-synchronization"></a><span data-ttu-id="c1a84-123">データ同期</span><span class="sxs-lookup"><span data-stu-id="c1a84-123">Data synchronization</span></span>

<span data-ttu-id="c1a84-124">次の図は、データが Project Service Automation と Finance との間で統合の一部として同期される方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="c1a84-124">The following illustration shows how data is synchronized as part of the integration between Project Service Automation and Finance.</span></span>

> [!NOTE]
> <span data-ttu-id="c1a84-125">現在利用可能なテンプレートはありません。</span><span class="sxs-lookup"><span data-stu-id="c1a84-125">Not all templates are currently available.</span></span> <span data-ttu-id="c1a84-126">完了するとテンプレートがリリースされます。</span><span class="sxs-lookup"><span data-stu-id="c1a84-126">Templates will be released as they are completed.</span></span>

<span data-ttu-id="c1a84-127">[![Project Service Automation とFinance の統合](./media/PSA-integration.png)](./media/PSA-integration.png)</span><span class="sxs-lookup"><span data-stu-id="c1a84-127">[![Project Service Automation integration with Finance](./media/PSA-integration.png)](./media/PSA-integration.png)</span></span>

## <a name="system-requirements-for-finance"></a><span data-ttu-id="c1a84-128">Finance のシステム要件</span><span class="sxs-lookup"><span data-stu-id="c1a84-128">System requirements for Finance</span></span>

<span data-ttu-id="c1a84-129">Finance 統合ソリューションに対して Project Service Automation を使用するには、Enterprise edition 7.3 およびプラットフォーム更新プログラム 12 またはそれ以降のバージョンをインストールする必要があります。</span><span class="sxs-lookup"><span data-stu-id="c1a84-129">To use the Project Service Automation to Finance integration solution, you must install Enterprise edition 7.3 with Platform update 12 or later.</span></span>

## <a name="system-requirements-for-project-service-automation"></a><span data-ttu-id="c1a84-130">Project Service Automation のシステム要件</span><span class="sxs-lookup"><span data-stu-id="c1a84-130">System requirements for Project Service Automation</span></span>

<span data-ttu-id="c1a84-131">Finance 統合ソリューションに対して Project Service Automation を使用するには、次のコンポーネントをインストールする必要があります。</span><span class="sxs-lookup"><span data-stu-id="c1a84-131">To use the Project Service Automation to Finance integration solution, you must install the following components:</span></span>

- <span data-ttu-id="c1a84-132">Dynamics 365 Project Service Automation バージョン 9.0.0.0 以降</span><span class="sxs-lookup"><span data-stu-id="c1a84-132">Dynamics 365 Project Service Automation version 9.0.0.0 or later</span></span>
- <span data-ttu-id="c1a84-133">Dynamics 365 Sales バージョン 1.14.0.0 (v14) またはそれ以降の見込顧客を現金化するソリューション</span><span class="sxs-lookup"><span data-stu-id="c1a84-133">Prospect to cash solution for Dynamics 365 Sales, version 1.14.0.0 (v14) or later</span></span>
- <span data-ttu-id="c1a84-134">Dynamics 365 Project Service Automation バージョン 1.0.0.0 以降の Finance ソリューションに対する Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="c1a84-134">Project Service Automation to Finance solution for Dynamics 365 Project Service Automation version 1.0.0.0 or later</span></span>

## <a name="install-the-project-service-automation-to-finance-integration-solution-in-your-project-service-automation-instance"></a><span data-ttu-id="c1a84-135">Project Service Automation インスタンス に Finance 統合ソリューションに対する Project Service Automation をインストールします</span><span class="sxs-lookup"><span data-stu-id="c1a84-135">Install the Project Service Automation to Finance integration solution in your Project Service Automation instance</span></span>

<span data-ttu-id="c1a84-136">[Microsoft ダウンロード センター](https://www.microsoft.com/download/details.aspx?id=57016) から Finance ソリューションに対する Project Service Automation をダウンロードし、ソリューションに含まれている手順に従ってください。</span><span class="sxs-lookup"><span data-stu-id="c1a84-136">Download the Project Service Automation to Finance integration solution from [Microsoft Download Center](https://www.microsoft.com/download/details.aspx?id=57016), and follow the instructions that are included with the solution.</span></span>
