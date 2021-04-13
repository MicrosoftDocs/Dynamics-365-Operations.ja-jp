---
title: 統合された作業者、職務、職位
description: このトピックでは、Microsoft Dynamics 365 アプリの統合された作業者データに関する情報を提供します。
author: RamaKrishnamoorthy
ms.date: 01/08/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.custom: 21311
ms.assetid: ''
ms.search.region: Global
ms.author: ramasri
ms.search.validFrom: 2020-01-08
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0d15b15643b7c9dcedcc6d0bc93d346b8127283e
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5748579"
---
# <a name="integrated-worker-job-and-position"></a><span data-ttu-id="a3997-103">作業者、職務、および職位の統合</span><span class="sxs-lookup"><span data-stu-id="a3997-103">Integrated worker, job, and position</span></span>

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]



<span data-ttu-id="a3997-104">1 つのアプリでのみマスターされている間は、作業者データは複数の Dynamics 365 アプリ間で同期できます。</span><span class="sxs-lookup"><span data-stu-id="a3997-104">While mastered in only one app, worker data can be synchronized across multiple Dynamics 365 apps.</span></span> <span data-ttu-id="a3997-105">たとえば、人事管理 (HR) データは Dynamics 365 Human Resources でマスターし、Dynamics 365 Commerce、Dynamics 365 Finance、および Dynamics 365 Supply Chain Management と同期することができます。</span><span class="sxs-lookup"><span data-stu-id="a3997-105">For example, human resources (HR) data can be mastered in Dynamics 365 Human Resources and synchronized with Dynamics 365 Commerce, Dynamics 365 Finance, and Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="a3997-106">データは、バックグラウンドでシームレスに統合されます。</span><span class="sxs-lookup"><span data-stu-id="a3997-106">The data is integrated seamlessly behind the scenes.</span></span> <span data-ttu-id="a3997-107">作業者に関するデータを統合する機能により、すべての Dynamics 365 アプリで同じデータを操作して、情報を包括的に把握することができます。</span><span class="sxs-lookup"><span data-stu-id="a3997-107">The ability to integrate data about workers ensures you're working with the same data across all Dynamics 365 apps, providing you a comprehensive view of your information.</span></span>

## <a name="human-resources"></a><span data-ttu-id="a3997-108">Human Resources</span><span class="sxs-lookup"><span data-stu-id="a3997-108">Human resources</span></span>

<span data-ttu-id="a3997-109">HR データの統合には、Dynamics 365 の Finance and Operations アプリとモデル駆動型アプリ間での HR データのマッピングが含まれます。</span><span class="sxs-lookup"><span data-stu-id="a3997-109">The integration of HR data involves just mapping the HR data between Finance and Operations apps and model-driven apps in Dynamics 365.</span></span>

## <a name="templates"></a><span data-ttu-id="a3997-110">テンプレート</span><span class="sxs-lookup"><span data-stu-id="a3997-110">Templates</span></span>

<span data-ttu-id="a3997-111">HR データには、従業員と契約社員、職位、職務に関する情報が含まれます。</span><span class="sxs-lookup"><span data-stu-id="a3997-111">HR data includes information about employees and contractors, positions, and jobs.</span></span> <span data-ttu-id="a3997-112">次の表に示すように、テーブル マップのコレクションは、データ操作中に連携して動作します。</span><span class="sxs-lookup"><span data-stu-id="a3997-112">A collection of table maps works together during data interaction, as shown in the following table.</span></span>

| <span data-ttu-id="a3997-113">Finance and Operations アプリ</span><span class="sxs-lookup"><span data-stu-id="a3997-113">Finance and Operations apps</span></span> | <span data-ttu-id="a3997-114">Dynamics 365 モデル駆動型アプリ</span><span class="sxs-lookup"><span data-stu-id="a3997-114">Model-driven apps in Dynamics 365</span></span> | <span data-ttu-id="a3997-115">説明</span><span class="sxs-lookup"><span data-stu-id="a3997-115">Description</span></span> |
|-----------------------------|----------------------------------|-------------|
| <span data-ttu-id="a3997-116">報酬ジョブ機能</span><span class="sxs-lookup"><span data-stu-id="a3997-116">Compensation job function</span></span> | <span data-ttu-id="a3997-117">cdm\_jobfunctions</span><span class="sxs-lookup"><span data-stu-id="a3997-117">cdm\_jobfunctions</span></span> | |
| <span data-ttu-id="a3997-118">報酬ジョブ タイプ</span><span class="sxs-lookup"><span data-stu-id="a3997-118">Compensation job type</span></span> | <span data-ttu-id="a3997-119">cdm\_jobtypes</span><span class="sxs-lookup"><span data-stu-id="a3997-119">cdm\_jobtypes</span></span> | |
| <span data-ttu-id="a3997-120">雇用</span><span class="sxs-lookup"><span data-stu-id="a3997-120">Employment</span></span> | <span data-ttu-id="a3997-121">cdm\_employments</span><span class="sxs-lookup"><span data-stu-id="a3997-121">cdm\_employments</span></span> | |
| <span data-ttu-id="a3997-122">雇用の詳細</span><span class="sxs-lookup"><span data-stu-id="a3997-122">Employment detail</span></span> | <span data-ttu-id="a3997-123">cdm\_employments</span><span class="sxs-lookup"><span data-stu-id="a3997-123">cdm\_employments</span></span> | |
| <span data-ttu-id="a3997-124">職務</span><span class="sxs-lookup"><span data-stu-id="a3997-124">Jobs</span></span> | <span data-ttu-id="a3997-125">cdm\_jobs</span><span class="sxs-lookup"><span data-stu-id="a3997-125">cdm\_jobs</span></span> | |
| <span data-ttu-id="a3997-126">ジョブの詳細</span><span class="sxs-lookup"><span data-stu-id="a3997-126">Job detail</span></span> | <span data-ttu-id="a3997-127">cdm\_jobs</span><span class="sxs-lookup"><span data-stu-id="a3997-127">cdm\_jobs</span></span> | |
| <span data-ttu-id="a3997-128">職位の詳細</span><span class="sxs-lookup"><span data-stu-id="a3997-128">Position details</span></span> | <span data-ttu-id="a3997-129">cdm\_jobpositions</span><span class="sxs-lookup"><span data-stu-id="a3997-129">cdm\_jobpositions</span></span> | |
| <span data-ttu-id="a3997-130">職位の期間</span><span class="sxs-lookup"><span data-stu-id="a3997-130">Position durations</span></span> | <span data-ttu-id="a3997-131">cdm\_jobpositions</span><span class="sxs-lookup"><span data-stu-id="a3997-131">cdm\_jobpositions</span></span> | |
| <span data-ttu-id="a3997-132">職位階層</span><span class="sxs-lookup"><span data-stu-id="a3997-132">Position hierarchies</span></span> | <span data-ttu-id="a3997-133">cdm\_jobpositions</span><span class="sxs-lookup"><span data-stu-id="a3997-133">cdm\_jobpositions</span></span> | |
| <span data-ttu-id="a3997-134">職位タイプ</span><span class="sxs-lookup"><span data-stu-id="a3997-134">Position type</span></span> | <span data-ttu-id="a3997-135">cdm\_positiontypes</span><span class="sxs-lookup"><span data-stu-id="a3997-135">cdm\_positiontypes</span></span> | |
| <span data-ttu-id="a3997-136">職位作業者割り当て</span><span class="sxs-lookup"><span data-stu-id="a3997-136">Position worker assignments</span></span> | <span data-ttu-id="a3997-137">cdm\_positionworkerassignmentmaps</span><span class="sxs-lookup"><span data-stu-id="a3997-137">cdm\_positionworkerassignmentmaps</span></span> | |
| <span data-ttu-id="a3997-138">ワーカー</span><span class="sxs-lookup"><span data-stu-id="a3997-138">Worker</span></span> | <span data-ttu-id="a3997-139">cdm\_workers</span><span class="sxs-lookup"><span data-stu-id="a3997-139">cdm\_workers</span></span> | <span data-ttu-id="a3997-140">Dynamics 365 Finance と Supply Chain Management では、作業者は従業員または契約社員のいずれかに分類されます。</span><span class="sxs-lookup"><span data-stu-id="a3997-140">In Dynamics 365 Finance and Supply Chain Management data, workers are classified as either employees or contractors.</span></span> <span data-ttu-id="a3997-141">Dataverse では、作業者をボランティアとして分類することもできます。</span><span class="sxs-lookup"><span data-stu-id="a3997-141">Dataverse can also classify workers as volunteers.</span></span> <span data-ttu-id="a3997-142">データが Finance と Supply Chain Management に変換されると、ボランティアは契約社員になります。</span><span class="sxs-lookup"><span data-stu-id="a3997-142">Volunteers will become contractors when the data is transformed back into Finance and Supply Chain Management.</span></span> |

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


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
