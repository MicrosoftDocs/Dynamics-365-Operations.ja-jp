---
title: "Dynamics 365 for Talent から Dynamics 365 for Finance and Operations への統合"
description: "このトピックでは、Talent と Finance and Operations の統合について説明します。"
author: jcart
manager: AnnBe
ms.date: 10/15/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
audience: IT Pro
ms.reviewer: josaw
ms.search.scope: 
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2018-10-8
ms.dyn365.ops.version: 
ms.translationtype: HT
ms.sourcegitcommit: 0450326dce0ba6be99aede4ebc871dc58c8039ab
ms.openlocfilehash: ab6f4393cfc83aa9ab39dd3759a590fa4b5301b4
ms.contentlocale: ja-jp
ms.lasthandoff: 11/01/2018

---

# <a name="integration-from-dynamics-365-for-talent-to-dynamics-365-for-finance-and-operations"></a><span data-ttu-id="3d953-103">Dynamics 365 for Talent から Dynamics 365 for Finance and Operations への統合</span><span class="sxs-lookup"><span data-stu-id="3d953-103">Integration from Dynamics 365 for Talent to Dynamics 365 for Finance and Operations</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="3d953-104">このトピックでは、Dynamics 365 for Talent と Dynamics 365 for Finance and Operations の統合のために使用できる機能について説明します。</span><span class="sxs-lookup"><span data-stu-id="3d953-104">This topic describes the functionality available for integration from Dynamics 365 for Talent and Dynamics 365 for Finance and Operations.</span></span> <span data-ttu-id="3d953-105">[データ インテグレーター](https://docs.microsoft.com/en-us/powerapps/administrator/data-integrator)と共に使用可能な Talent から Finance and Operations へのテンプレートにより、ジョブ、職位、および作業者のデータのフローが可能になります。</span><span class="sxs-lookup"><span data-stu-id="3d953-105">The Talent to Finance and Operations template that is available with the [Data Integrator](https://docs.microsoft.com/en-us/powerapps/administrator/data-integrator) enables the flow of data for jobs, positions, and workers.</span></span> <span data-ttu-id="3d953-106">Talent から Finance and Operations へのデータ フロー。</span><span class="sxs-lookup"><span data-stu-id="3d953-106">The data flows from Talent into Finance and Operations.</span></span> <span data-ttu-id="3d953-107">テンプレートでは、Finance and Operations から Talent にデータを戻す機能は提供されません。</span><span class="sxs-lookup"><span data-stu-id="3d953-107">The template does not provide the ability for data to flow back from Finance and Operations into Talent.</span></span> 

![Talent のから Finance and Operations への統合フロー](./media/TalentFinOpsFlow.png)

<span data-ttu-id="3d953-109">Talent から Finance and Operations へのソリューションは、次のタイプのデータ同期を提供します。</span><span class="sxs-lookup"><span data-stu-id="3d953-109">The Talent to Finance and Operations solution provides the following types of data synchronization.</span></span> 

- <span data-ttu-id="3d953-110">Talent のジョブを管理し、Talent から Finance and Operations に同期します。</span><span class="sxs-lookup"><span data-stu-id="3d953-110">Maintain jobs in Talent and sync them from Talent to Finance and Operations.</span></span>
- <span data-ttu-id="3d953-111">Talent の職位と職位の割り当てを管理し、Talent から Finance and Operations に同期します。</span><span class="sxs-lookup"><span data-stu-id="3d953-111">Maintain positions and position assignments in Talent and sync them from Talent to Finance and Operations.</span></span>
- <span data-ttu-id="3d953-112">Talent の雇用を管理し、Talent から Finance and Operations に同期します。</span><span class="sxs-lookup"><span data-stu-id="3d953-112">Maintain employments in Talent and sync them from Talent to Finance and Operations.</span></span>
- <span data-ttu-id="3d953-113">Talent の作業者と作業者住所を管理し、Talent から Finance and Operations に同期します。</span><span class="sxs-lookup"><span data-stu-id="3d953-113">Maintain workers and worker addresses in Talent and sync them from Talent to Finance and Operations.</span></span>

## <a name="system-requirements-for-talent"></a><span data-ttu-id="3d953-114">Talent のシステム要件</span><span class="sxs-lookup"><span data-stu-id="3d953-114">System requirements for Talent</span></span>
<span data-ttu-id="3d953-115">統合ソリューションには、次のバージョンの Talent および Finance and Operations アプリケーションが必要です。</span><span class="sxs-lookup"><span data-stu-id="3d953-115">The integration solution requires the following versions of the Talent and Finance and Operations apps.</span></span> 
- <span data-ttu-id="3d953-116">CDS for Apps の Dynamics 365 for Talent。</span><span class="sxs-lookup"><span data-stu-id="3d953-116">Dynamics 365 for Talent on CDS for Apps.</span></span>
- <span data-ttu-id="3d953-117">Dynamics 365 for Finance and Operations バージョン 7.2 以降。</span><span class="sxs-lookup"><span data-stu-id="3d953-117">Dynamics 365 for Finance and Operations version 7.2 and later.</span></span>

## <a name="template-and-tasks"></a><span data-ttu-id="3d953-118">テンプレートおよびタスク</span><span class="sxs-lookup"><span data-stu-id="3d953-118">Template and tasks</span></span>

<span data-ttu-id="3d953-119">テンプレートにアクセスするには、次の操作を行います。</span><span class="sxs-lookup"><span data-stu-id="3d953-119">To access the template, do the following.</span></span>
1. <span data-ttu-id="3d953-120">[PowerApps 管理センター](https://admin.powerapps.com/)を開きます。</span><span class="sxs-lookup"><span data-stu-id="3d953-120">Open [PowerApps Admin Center](https://admin.powerapps.com/).</span></span> 
1. <span data-ttu-id="3d953-121">**プロジェクト**を選択した後、右上隅にある **新しいプロジェクト** を選択してパブリック テンプレートを選択します。</span><span class="sxs-lookup"><span data-stu-id="3d953-121">Select **Projects**, and then, in the upper-right corner, select **New project** to select public templates.</span></span> <span data-ttu-id="3d953-122">新しいプロジェクトは、Finance and Operations に統合する法人ごとに作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="3d953-122">A new project will need to be created for each legal entity that you want to integrate into in Finance and Operations.</span></span>

<span data-ttu-id="3d953-123">Talent から Finance and Operations にレコードを同期するには、次のテンプレートを使用します。</span><span class="sxs-lookup"><span data-stu-id="3d953-123">The following template is used to synchronize records from Talent to Finance and Operations.</span></span>

- <span data-ttu-id="3d953-124">**データ統合でのテンプレートの名前:** Core HR (Talent CDS から Fin and Ops)</span><span class="sxs-lookup"><span data-stu-id="3d953-124">**Name of the template in Data integration:** Core HR (Talent CDS to Fin and Ops)</span></span>

  > [!NOTE]
  > <span data-ttu-id="3d953-125">タスクの名前には、各アプリケーションで使用されるエンティティが含まれています。</span><span class="sxs-lookup"><span data-stu-id="3d953-125">The name of the task contains the entities used in each application.</span></span> <span data-ttu-id="3d953-126">ソース (Talent) は左にあり、ターゲット (Finance and Operations) は右にあります。</span><span class="sxs-lookup"><span data-stu-id="3d953-126">The source (Talent) is on the left and the destination (Finance and Operations) is on the right.</span></span>

<span data-ttu-id="3d953-127">Talent から Finance and Operations にレコードを同期するには、次の基になるタスクを使用します。</span><span class="sxs-lookup"><span data-stu-id="3d953-127">The following underlying tasks are used to synchronize records from Talent to Finance and Operations.</span></span>
- <span data-ttu-id="3d953-128">職務権限から報酬職務権限。</span><span class="sxs-lookup"><span data-stu-id="3d953-128">Job Functions to Compensation Job Function.</span></span>
- <span data-ttu-id="3d953-129">部門から作業単位</span><span class="sxs-lookup"><span data-stu-id="3d953-129">Departments to Operating Unit</span></span>
- <span data-ttu-id="3d953-130">部門から作業単位</span><span class="sxs-lookup"><span data-stu-id="3d953-130">Departments to Operating Unit</span></span>
- <span data-ttu-id="3d953-131">ジョブ タイプから報酬ジョブ タイプ</span><span class="sxs-lookup"><span data-stu-id="3d953-131">Job Types to Compensation Job Type</span></span>
- <span data-ttu-id="3d953-132">ジョブからジョブ</span><span class="sxs-lookup"><span data-stu-id="3d953-132">Jobs to Jobs</span></span>
- <span data-ttu-id="3d953-133">ジョブからジョブ詳細</span><span class="sxs-lookup"><span data-stu-id="3d953-133">Jobs to Job Detail</span></span>
- <span data-ttu-id="3d953-134">職位タイプから職位タイプ</span><span class="sxs-lookup"><span data-stu-id="3d953-134">Position Types to Position Type</span></span>
- <span data-ttu-id="3d953-135">ジョブ職位から職位</span><span class="sxs-lookup"><span data-stu-id="3d953-135">Job Positions to Positions</span></span>
- <span data-ttu-id="3d953-136">ジョブ職位から職位親ジョブ割り当て</span><span class="sxs-lookup"><span data-stu-id="3d953-136">Job Positions to Positions Parent Job Assignment</span></span>
- <span data-ttu-id="3d953-137">作業者から作業者</span><span class="sxs-lookup"><span data-stu-id="3d953-137">Workers to Worker</span></span>
- <span data-ttu-id="3d953-138">雇用から雇用</span><span class="sxs-lookup"><span data-stu-id="3d953-138">Employments to Employment</span></span>
- <span data-ttu-id="3d953-139">雇用から雇用詳細</span><span class="sxs-lookup"><span data-stu-id="3d953-139">Employments to Employment Detail</span></span>
- <span data-ttu-id="3d953-140">職位作業者割り当てから職位作業者割り当て</span><span class="sxs-lookup"><span data-stu-id="3d953-140">Position Worker Assignment to Position Worker Assignments</span></span>
- <span data-ttu-id="3d953-141">作業者住所から作業者の住所 V2</span><span class="sxs-lookup"><span data-stu-id="3d953-141">Worker Addresses to Worker Postal Address V2</span></span>

## <a name="integration-considerations"></a><span data-ttu-id="3d953-142">統合に関する考慮事項</span><span class="sxs-lookup"><span data-stu-id="3d953-142">Integration considerations</span></span>
<span data-ttu-id="3d953-143">Talent から Finance and Operations にデータを統合する場合は、統合が ID に基づいてレコードを一致させようとします。</span><span class="sxs-lookup"><span data-stu-id="3d953-143">When integrating data from Talent to Finance and Operations, the integration will attempt to match records based on the ID.</span></span> <span data-ttu-id="3d953-144">一致が発生した場合、Finance and Operations のデータは、Talent の値で上書きされます。</span><span class="sxs-lookup"><span data-stu-id="3d953-144">If the match occurs, the data in Finance and Operations will be overwritten with the values in Talent.</span></span> <span data-ttu-id="3d953-145">ただし、論理的にさまざまなレコードが存在し、Talent または Finance and Operations のいずれかでそれぞれの番号順序に基づいて同一の ID が生成された場合に、問題が発生する場合があります。</span><span class="sxs-lookup"><span data-stu-id="3d953-145">However, an issue may occur if logically these are different records and the same ID was generated in either Talent or Finance and Operations based on the respective number sequence.</span></span>

<span data-ttu-id="3d953-146">これが発生する領域は、従業員番号を使用して一致が作成される作業者と、職位です。</span><span class="sxs-lookup"><span data-stu-id="3d953-146">The areas where this can occur are Worker, which uses Personnel number to make the match, and Positions.</span></span> <span data-ttu-id="3d953-147">ジョブは、番号順序を使用しません。その結果、同一のジョブ ID が Talent と Finance and Operations の両方で存在する場合は、Talent 情報により Finance and Operations 情報が上書きされます。</span><span class="sxs-lookup"><span data-stu-id="3d953-147">Jobs do not use number sequences, as a result, if the same job ID is present in both Talent and Finance and Operations, the Talent information will overwrite the Finance and Operations information.</span></span> 

<span data-ttu-id="3d953-148">重複する ID の問題を防ぐには、[番号順序](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/organization-administration/number-sequence-overview?toc=/dynamics365/unified-operations/talent/toc.json)に接頭語を追加するか、その他のシステムの範囲を超えている番号順序の開始番号を設定します。</span><span class="sxs-lookup"><span data-stu-id="3d953-148">To prevent issues with duplicate IDs, you can either add a prefix on the [number sequence](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/organization-administration/number-sequence-overview?toc=/dynamics365/unified-operations/talent/toc.json), or set a beginning number on the number sequence that is beyond the range of the other system.</span></span> 

<span data-ttu-id="3d953-149">番号順序に含まれていない作業者住所に使用される場所 ID。</span><span class="sxs-lookup"><span data-stu-id="3d953-149">The location ID used for worker address isn't part of a number sequence.</span></span> <span data-ttu-id="3d953-150">Talent から Finance and Operations に作業者住所を統合するとき、Finance and Operations に作業者の住所が既に存在する場合は、重複する住所レコードが作成される場合があります。</span><span class="sxs-lookup"><span data-stu-id="3d953-150">When integrating a worker address from Talent to Finance and Operations, if the worker address already exists in Finance and Operations, a duplicate address record may be created.</span></span> 

<span data-ttu-id="3d953-151">次の図は、データ インテグレーターのテンプレート マッピングの例を示しています。</span><span class="sxs-lookup"><span data-stu-id="3d953-151">The following illustration shows an example of a template mapping in Data Integrator.</span></span> 

![テンプレートのマッピング](./media/IntegrationMapping.png)





