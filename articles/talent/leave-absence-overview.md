---
title: "休暇管理の概要"
description: "このトピックでは、休暇管理モジュールの概要を示します。 このモジュールは、休暇管理プロセスを定義するための柔軟なフレームワークを提供します。 従業員が休暇を蓄積するもしくは交付される方法を決定するために、休暇計画を作成できます。"
author: ryansandness
manager: AnnBe
ms.date: 08/01/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-talent
ms.technology: 
ms.search.form: 
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Operations, Core
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.author: ryansand
ms.search.validFrom: 2017-07-01
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: d9b080ff46a0fbc73ed4f8fa3f03d71e9d758cc2
ms.openlocfilehash: 331e3eae38d3abc9fa545e84d18de91b81352af9
ms.contentlocale: ja-jp
ms.lasthandoff: 01/17/2018

---
# <a name="leave-and-absence-management-overview"></a><span data-ttu-id="81b62-105">休暇管理の概要</span><span class="sxs-lookup"><span data-stu-id="81b62-105">Leave and absence management overview</span></span>

<span data-ttu-id="81b62-106">[**休暇管理**] モジュールは、休暇管理プロセスを定義するための柔軟なフレームワークを提供します。</span><span class="sxs-lookup"><span data-stu-id="81b62-106">The **Leave and absence management** module offers a flexible framework for defining the absence management process.</span></span> <span data-ttu-id="81b62-107">従業員が休暇を蓄積するもしくは交付される方法を決定するために、休暇計画を作成できます。</span><span class="sxs-lookup"><span data-stu-id="81b62-107">Leave and absence plans can be created to determine how employees accrue or are granted time off.</span></span> <span data-ttu-id="81b62-108">従業員が計画に登録されると、管理者による承認を求めて休暇申請を送信できます。</span><span class="sxs-lookup"><span data-stu-id="81b62-108">After employees are enrolled in a plan, they can submit time-off requests for approval by managers.</span></span> <span data-ttu-id="81b62-109">休暇追跡により、ファーストレベル マネージャーと人事管理 (HR) マネージャーの両方が、休暇を取っている従業員および各従業員の残っている休暇時間を確認することができます。</span><span class="sxs-lookup"><span data-stu-id="81b62-109">Leave tracking lets both first-level managers and Human Resources (HR) managers see who is taking time off and how much time off each employee still has.</span></span>  

<span data-ttu-id="81b62-110">休暇管理は、次の機能を提供します。</span><span class="sxs-lookup"><span data-stu-id="81b62-110">Leave and absence management provides the following features:</span></span> 

- <span data-ttu-id="81b62-111">**休暇タイプを定義します。**</span><span class="sxs-lookup"><span data-stu-id="81b62-111">**Define leave and absence types.**</span></span>

    <span data-ttu-id="81b62-112">休暇タイプは、従業員がレポートできるさまざまなタイプの休暇を定義します。</span><span class="sxs-lookup"><span data-stu-id="81b62-112">Leave types define the various types of absences that employees can report.</span></span> <span data-ttu-id="81b62-113">これらのタイプはユーザー定義であるため、組織に合わせることができます。</span><span class="sxs-lookup"><span data-stu-id="81b62-113">Because these types are user-defined, they can be tailored to your organization.</span></span> <span data-ttu-id="81b62-114">代表的な休暇タイプには、有給休暇 (PTO)、休暇、短期障害、陪審義務 (この休暇タイプは米国に固有)、および忌引きが含まれます。</span><span class="sxs-lookup"><span data-stu-id="81b62-114">Some typical leave types include paid time off (PTO), leave, short-term disability, jury duty (this leave type is specific to the United States), and bereavement.</span></span> 

- <span data-ttu-id="81b62-115">**業務に合うよう階層化した休暇計画を定義します。**</span><span class="sxs-lookup"><span data-stu-id="81b62-115">**Define leave and absence plans that are tiered to fit your business.**</span></span>

    <span data-ttu-id="81b62-116">年ごと、月ごと、または半月ごと、といった特定の頻度で累積が発生するように休暇計画を定義することができます。</span><span class="sxs-lookup"><span data-stu-id="81b62-116">Leave and absence plans can be defined so that accrual occurs at specific frequencies, such as annually, monthly, or semimonthly.</span></span> <span data-ttu-id="81b62-117">計画は、特定の日付で 1 つの累積が発生する交付として定義することもできます。</span><span class="sxs-lookup"><span data-stu-id="81b62-117">Plans can also be defined as a grant, where a single accrual occurs on a specific date.</span></span> 

    <span data-ttu-id="81b62-118">多くの場合、休暇計画は、組織に所属してきた時間量に基づいて従業員のいくつかのグループが追加の給付を受ける階層を含んでいます。</span><span class="sxs-lookup"><span data-stu-id="81b62-118">Leave plans often contain tiers, where some groups of employees receive additional benefits, based on the amount of time that they have been with the organization.</span></span> <span data-ttu-id="81b62-119">これらのユーザー定義の階層は、定義されている日付基準に基づき、追加の給付時間への自動登録を有効にします。</span><span class="sxs-lookup"><span data-stu-id="81b62-119">These user-defined tiers enable automatic enrollment in additional benefit hours, based on the date criteria that are defined.</span></span> <span data-ttu-id="81b62-120">従業員が蓄積した以上の給付時間を使用することを防ぐために、最大繰越量または最低残高を適用する休暇計画を構成することもできます。</span><span class="sxs-lookup"><span data-stu-id="81b62-120">Leave plans can also be configured to enforce a maximum carry-over amount or a minimum balance, to prevent employees from using more benefit hours than they have accrued.</span></span> 

    <span data-ttu-id="81b62-121">代表的な休暇計画には、新しい従業員には 80 時間の PTO の給付を交付するが 60 か月のサービス後には 120 時間の給付を交付する、段階的な計画が含まれます。</span><span class="sxs-lookup"><span data-stu-id="81b62-121">Typical leave plans include tiered plans that grant a benefit of 80 hours of PTO to new employees but a benefit of 120 hours after 60 months of service.</span></span> <span data-ttu-id="81b62-122">追加の計画で、流動的な休日、または経営幹部専用の給付時間といった職位に基づく給付を交付する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="81b62-122">Additional plans might grant floating holidays or position-based benefits, such as executive-only benefit hours.</span></span>

- <span data-ttu-id="81b62-123">**個別に、または職務基準に基づく一括割り当てにより、休暇計画に従業員を登録します。**</span><span class="sxs-lookup"><span data-stu-id="81b62-123">**Enroll employees in leave and absence plans individually or through mass assignment that is based on job criteria.**</span></span>

    <span data-ttu-id="81b62-124">複数の職務関連のフィルターを使用して、従業員のグループを休暇計画に割り当てることができます。</span><span class="sxs-lookup"><span data-stu-id="81b62-124">Several job-related filters can be used to assign a group of employees to a leave plan.</span></span> <span data-ttu-id="81b62-125">HR マネージャーは、従業員を表示してその従業員が登録されている休暇計画を確認することができます。</span><span class="sxs-lookup"><span data-stu-id="81b62-125">HR managers can view an employee to see what leave and absence plans the employee is enrolled in.</span></span> <span data-ttu-id="81b62-126">または、HR マネージャーはすべての計画および関連する従業員の登録を表示できます。</span><span class="sxs-lookup"><span data-stu-id="81b62-126">Alternatively, HR managers can view all plans and the related employee enrollments.</span></span>

- <span data-ttu-id="81b62-127">**休暇計画を中断します。**</span><span class="sxs-lookup"><span data-stu-id="81b62-127">**Suspend leave and absence plans.**</span></span>

    <span data-ttu-id="81b62-128">休暇計画を無効にし追加の累積を阻むために、休暇計画を中断することができます。</span><span class="sxs-lookup"><span data-stu-id="81b62-128">Leave and absence plans can be suspended to make them inactive and prevent additional accruals.</span></span> <span data-ttu-id="81b62-129">雇用が終了した場合、その従業員に対して累積が中断されます。</span><span class="sxs-lookup"><span data-stu-id="81b62-129">Accruals are suspended for employees if their employment ends.</span></span>  

- <span data-ttu-id="81b62-130">**資格および交付を調整します。**</span><span class="sxs-lookup"><span data-stu-id="81b62-130">**Adjust entitlements and grants.**</span></span>

    <span data-ttu-id="81b62-131">作業者固有の日付を使用して従業員の既定の計画を上書きすることによって、その従業員を上の計画階層に登録できます。</span><span class="sxs-lookup"><span data-stu-id="81b62-131">An employee can be enrolled in a higher plan tier by using a worker-specific date to override the employee's default plan offering.</span></span> <span data-ttu-id="81b62-132">従業員は、計画登録時に自分の休暇残高への手動調整を受け取ることができます。または HR がいつでも手動調整を行うことができます。</span><span class="sxs-lookup"><span data-stu-id="81b62-132">Employees can receive a manual adjustment to their leave and absence balance at the time of plan enrollment, or HR can make a manual adjustment at any time.</span></span> 

- <span data-ttu-id="81b62-133">**休暇申請にワークフローを適用します。**</span><span class="sxs-lookup"><span data-stu-id="81b62-133">**Apply a workflow to time-off requests.**</span></span>

     <span data-ttu-id="81b62-134">組織の要件を満たすために、ワークフローをカスタマイズし休暇申請に適用することができます。</span><span class="sxs-lookup"><span data-stu-id="81b62-134">A workflow can be customized and applied to time-off requests to meet the organization’s requirements.</span></span>  

- <span data-ttu-id="81b62-135">**従業員の休暇残高を追跡します。**</span><span class="sxs-lookup"><span data-stu-id="81b62-135">**Track employee absence balances.**</span></span>

    <span data-ttu-id="81b62-136">従業員、マネージャー、および HR は休暇残高を表示できます。</span><span class="sxs-lookup"><span data-stu-id="81b62-136">Employees, their manager, and HR can view leave and absence balances.</span></span> <span data-ttu-id="81b62-137">HR は対話型レポートを使用して、タイプ別の計画登録および休暇残高を追跡します。</span><span class="sxs-lookup"><span data-stu-id="81b62-137">HR can use interactive reports to track plan enrollments and time-off balances by type.</span></span> 

- <span data-ttu-id="81b62-138">**休暇申請を送信します。**</span><span class="sxs-lookup"><span data-stu-id="81b62-138">**Submit time-off requests.**</span></span>

    <span data-ttu-id="81b62-139">従業員は、使用可能な時間に対して休暇申請を送信できます。</span><span class="sxs-lookup"><span data-stu-id="81b62-139">Employees can submit time-off requests against their available hours.</span></span> <span data-ttu-id="81b62-140">申請は、単純な 1 日申請、または複数の休暇タイプを含む複数日申請が可能です。</span><span class="sxs-lookup"><span data-stu-id="81b62-140">Requests can be simple single-day requests or multiple-day requests that include multiple leave and absence types.</span></span> <span data-ttu-id="81b62-141">ワークフローが有効でない場合は、申請は自動的に承認されます。</span><span class="sxs-lookup"><span data-stu-id="81b62-141">If a workflow isn't enabled, the requests are automatically approved.</span></span> <span data-ttu-id="81b62-142">ワークフローが有効になっている場合、承認が自動になっている可能性もあれば、ワークフローのコンフィギュレーションによってはサインオフを要求する可能性もあります。</span><span class="sxs-lookup"><span data-stu-id="81b62-142">If a workflow is enabled, the approval can be automatic, or it can require sign-off, depending on the workflow configuration.</span></span>

