---
title: 統合された作業者、職務、職位
description: このトピックでは、Microsoft Dynamics 365 アプリの統合された作業者データに関する情報を提供します。
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 01/08/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.search.scope: Operations
ms.custom: 21311
ms.assetid: ''
ms.search.region: Global
ms.author: ramasri
ms.search.validFrom: 2020-01-08
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 549e3f72b936e8f4274587a92306fc4f97b617b1
ms.sourcegitcommit: 68f1485de7d64a6c9eba1088af63bd07992d972d
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/27/2020
ms.locfileid: "3173028"
---
# <a name="integrated-worker-job-and-position"></a><span data-ttu-id="3ff34-103">統合された作業者、職務、職位</span><span class="sxs-lookup"><span data-stu-id="3ff34-103">Integrated worker, job, and position</span></span>

[!include [banner](../../includes/banner.md)]



<span data-ttu-id="3ff34-104">作業者データは、複数の Microsoft Dynamics 365 アプリでマスターできます。</span><span class="sxs-lookup"><span data-stu-id="3ff34-104">Worker data can be mastered in more than one Microsoft Dynamics 365 app.</span></span> <span data-ttu-id="3ff34-105">たとえば、人事管理 (HR) データは、Dynamics 365 Human Resources、Dynamics 365 Commerce、Dynamics 365 Supply Chain Management で管理できます。</span><span class="sxs-lookup"><span data-stu-id="3ff34-105">For example, Human resources (HR) data can be managed in Dynamics 365 Human Resources, Dynamics 365 Commerce, and Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="3ff34-106">データの出所に関係なく、バックグラウンドで統合されます。</span><span class="sxs-lookup"><span data-stu-id="3ff34-106">Regardless of where the data originates, it's integrated behind the scenes.</span></span> <span data-ttu-id="3ff34-107">作業者に関するデータを統合する機能により、あらゆる Dynamics 365 アプリで作業者データを柔軟にマスターできます。</span><span class="sxs-lookup"><span data-stu-id="3ff34-107">The ability to integrate data about workers gives you the flexibility to master worker data in any Dynamics 365 app.</span></span> <span data-ttu-id="3ff34-108">また、Dynamics 365 アプリの情報を包括的に把握することもできます。</span><span class="sxs-lookup"><span data-stu-id="3ff34-108">It also provides a comprehensive view of the information in Dynamics 365 apps.</span></span>

## <a name="human-resources"></a><span data-ttu-id="3ff34-109">人事管理</span><span class="sxs-lookup"><span data-stu-id="3ff34-109">Human resources</span></span>

<span data-ttu-id="3ff34-110">HR データの統合には、Dynamics 365 の Finance and Operations アプリとモデル駆動型アプリ間での HR データのマッピングが含まれます。</span><span class="sxs-lookup"><span data-stu-id="3ff34-110">The integration of HR data involves just mapping the HR data between Finance and Operations apps and model-driven apps in Dynamics 365.</span></span>

## <a name="templates"></a><span data-ttu-id="3ff34-111">テンプレート</span><span class="sxs-lookup"><span data-stu-id="3ff34-111">Templates</span></span>

<span data-ttu-id="3ff34-112">HR データには、従業員と契約社員、職位、職務に関する情報が含まれます。</span><span class="sxs-lookup"><span data-stu-id="3ff34-112">HR data includes information about employees and contractors, positions, and jobs.</span></span> <span data-ttu-id="3ff34-113">次の表に示すように、エンティティ マップのコレクションは、データ操作中に連携して動作します。</span><span class="sxs-lookup"><span data-stu-id="3ff34-113">A collection of entity maps works together during data interaction, as shown in the following table.</span></span>

| <span data-ttu-id="3ff34-114">Finance and Operations アプリ</span><span class="sxs-lookup"><span data-stu-id="3ff34-114">Finance and Operations apps</span></span> | <span data-ttu-id="3ff34-115">Dynamics 365 モデル駆動型アプリ</span><span class="sxs-lookup"><span data-stu-id="3ff34-115">Model-driven apps in Dynamics 365</span></span> | <span data-ttu-id="3ff34-116">説明</span><span class="sxs-lookup"><span data-stu-id="3ff34-116">Description</span></span> |
|-----------------------------|----------------------------------|-------------|
| <span data-ttu-id="3ff34-117">報酬ジョブ機能</span><span class="sxs-lookup"><span data-stu-id="3ff34-117">Compensation job function</span></span> | <span data-ttu-id="3ff34-118">cdm\_jobfunctions</span><span class="sxs-lookup"><span data-stu-id="3ff34-118">cdm\_jobfunctions</span></span> | |
| <span data-ttu-id="3ff34-119">報酬ジョブ タイプ</span><span class="sxs-lookup"><span data-stu-id="3ff34-119">Compensation job type</span></span> | <span data-ttu-id="3ff34-120">cdm\_jobtypes</span><span class="sxs-lookup"><span data-stu-id="3ff34-120">cdm\_jobtypes</span></span> | |
| <span data-ttu-id="3ff34-121">雇用</span><span class="sxs-lookup"><span data-stu-id="3ff34-121">Employment</span></span> | <span data-ttu-id="3ff34-122">cdm\_employments</span><span class="sxs-lookup"><span data-stu-id="3ff34-122">cdm\_employments</span></span> | |
| <span data-ttu-id="3ff34-123">雇用の詳細</span><span class="sxs-lookup"><span data-stu-id="3ff34-123">Employment detail</span></span> | <span data-ttu-id="3ff34-124">cdm\_employments</span><span class="sxs-lookup"><span data-stu-id="3ff34-124">cdm\_employments</span></span> | |
| <span data-ttu-id="3ff34-125">職務</span><span class="sxs-lookup"><span data-stu-id="3ff34-125">Jobs</span></span> | <span data-ttu-id="3ff34-126">cdm\_jobs</span><span class="sxs-lookup"><span data-stu-id="3ff34-126">cdm\_jobs</span></span> | |
| <span data-ttu-id="3ff34-127">ジョブの詳細</span><span class="sxs-lookup"><span data-stu-id="3ff34-127">Job detail</span></span> | <span data-ttu-id="3ff34-128">cdm\_jobs</span><span class="sxs-lookup"><span data-stu-id="3ff34-128">cdm\_jobs</span></span> | |
| <span data-ttu-id="3ff34-129">職位の詳細</span><span class="sxs-lookup"><span data-stu-id="3ff34-129">Position details</span></span> | <span data-ttu-id="3ff34-130">cdm\_jobpositions</span><span class="sxs-lookup"><span data-stu-id="3ff34-130">cdm\_jobpositions</span></span> | |
| <span data-ttu-id="3ff34-131">職位の期間</span><span class="sxs-lookup"><span data-stu-id="3ff34-131">Position durations</span></span> | <span data-ttu-id="3ff34-132">cdm\_jobpositions</span><span class="sxs-lookup"><span data-stu-id="3ff34-132">cdm\_jobpositions</span></span> | |
| <span data-ttu-id="3ff34-133">職位階層</span><span class="sxs-lookup"><span data-stu-id="3ff34-133">Position hierarchies</span></span> | <span data-ttu-id="3ff34-134">cdm\_jobpositions</span><span class="sxs-lookup"><span data-stu-id="3ff34-134">cdm\_jobpositions</span></span> | |
| <span data-ttu-id="3ff34-135">職位タイプ</span><span class="sxs-lookup"><span data-stu-id="3ff34-135">Position type</span></span> | <span data-ttu-id="3ff34-136">cdm\_positiontypes</span><span class="sxs-lookup"><span data-stu-id="3ff34-136">cdm\_positiontypes</span></span> | |
| <span data-ttu-id="3ff34-137">職位作業者割り当て</span><span class="sxs-lookup"><span data-stu-id="3ff34-137">Position worker assignments</span></span> | <span data-ttu-id="3ff34-138">cdm\_positionworkerassignmentmaps</span><span class="sxs-lookup"><span data-stu-id="3ff34-138">cdm\_positionworkerassignmentmaps</span></span> | |
| <span data-ttu-id="3ff34-139">ワーカー</span><span class="sxs-lookup"><span data-stu-id="3ff34-139">Worker</span></span> | <span data-ttu-id="3ff34-140">cdm\_workers</span><span class="sxs-lookup"><span data-stu-id="3ff34-140">cdm\_workers</span></span> | <span data-ttu-id="3ff34-141">Dynamics 365 Finance と Supply Chain Management では、作業者は従業員または契約社員のいずれかに分類されます。</span><span class="sxs-lookup"><span data-stu-id="3ff34-141">In Dynamics 365 Finance and Supply Chain Management data, workers are classified as either employees or contractors.</span></span> <span data-ttu-id="3ff34-142">Common Data Service では、作業者をボランティアとして分類することもできます。</span><span class="sxs-lookup"><span data-stu-id="3ff34-142">Common Data Service can also classify workers as volunteers.</span></span> <span data-ttu-id="3ff34-143">データが Finance と Supply Chain Management に変換されると、ボランティアは契約社員になります。</span><span class="sxs-lookup"><span data-stu-id="3ff34-143">Volunteers will become contractors when the data is transformed back into Finance and Supply Chain Management.</span></span> |

[!include [symbols](../../includes/dual-write-symbols.md)]

[!include [job function](includes/JobFunction-cdm-jobfunctions.md)]

[!include [job type](includes/JobType-cdm-jobtypes.md)]

[!include [employment](includes/Employment-cdm-employments.md)]

[!include [employment detail](includes/EmploymentDetail-cdm-employments.md)]

[!include [job](includes/Job-cdm-jobs.md)]

[!include [job detail](includes/JobDetail-cdm-jobs.md)]

[!include [position detail](includes/PositionDetail-cdm-jobpositions.md)]

[!include [position duration](includes/PositionDuration-cdm-jobpositions.md)]

[!include [position hierarchy](includes/PositionHierarchy-cdm-jobpositions.md)]

[!include [position type](includes/PositionType-cdm-positiontypes.md)]

[!include [position worker assignment](includes/PositionWorkerAssignment-cdm-positionworkerassignmentmaps.md)]

[!include [worker](includes/Worker-cdm-workers.md)]
