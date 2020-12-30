---
title: Common Data Service エンティティ
description: Microsoft Dynamics 365 Human Resources は、Common Data Service を使用して拡張性シナリオおよび統合シナリオを有効にします。
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 988fa0b6d39a49b973626a8a0abe83c546f42297
ms.sourcegitcommit: e89bb3e5420a6ece84f4e80c11e360b4a042f59d
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/17/2020
ms.locfileid: "4530009"
---
# <a name="common-data-service-entities"></a><span data-ttu-id="4268d-103">Common Data Service エンティティ</span><span class="sxs-lookup"><span data-stu-id="4268d-103">Common Data Service entities</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="4268d-104">Microsoft Dynamics 365 Human Resources は、Common Data Service を使用して拡張性シナリオおよび統合シナリオを有効にします。</span><span class="sxs-lookup"><span data-stu-id="4268d-104">Microsoft Dynamics 365 Human Resources uses Common Data Service to enable extensibility and integration scenarios.</span></span>

<span data-ttu-id="4268d-105">Common Data Service の詳細については、[Common Data Service とは何か](https://docs.microsoft.com/powerapps/maker/common-data-service/data-platform-intro)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="4268d-105">For more information about Common Data Service, see [What is Common Data Service](https://docs.microsoft.com/powerapps/maker/common-data-service/data-platform-intro).</span></span>

<span data-ttu-id="4268d-106">次の人事管理エンティティは、Common Data Service で使用できます。</span><span class="sxs-lookup"><span data-stu-id="4268d-106">The following Human Resources entities are available in Common Data Service.</span></span>

## <a name="benefit-entities"></a><span data-ttu-id="4268d-107">Benefit エンティティ</span><span class="sxs-lookup"><span data-stu-id="4268d-107">Benefit entities</span></span>

| <span data-ttu-id="4268d-108">氏名</span><span class="sxs-lookup"><span data-stu-id="4268d-108">Name</span></span> | <span data-ttu-id="4268d-109">エンティティ</span><span class="sxs-lookup"><span data-stu-id="4268d-109">Entity</span></span> |
| --- | --- |
| <span data-ttu-id="4268d-110">給付金計算頻度</span><span class="sxs-lookup"><span data-stu-id="4268d-110">Benefit Calculation Frequency</span></span> | <span data-ttu-id="4268d-111">cdm_benefitcalculationfrequency</span><span class="sxs-lookup"><span data-stu-id="4268d-111">cdm_benefitcalculationfrequency</span></span> |
| <span data-ttu-id="4268d-112">給付金計算頻度支払期間</span><span class="sxs-lookup"><span data-stu-id="4268d-112">Benefit Calculation Frequency Pay Period</span></span> | <span data-ttu-id="4268d-113">cdm_benefitcalculationfrequencypayperiod</span><span class="sxs-lookup"><span data-stu-id="4268d-113">cdm_benefitcalculationfrequencypayperiod</span></span> |
| <span data-ttu-id="4268d-114">給付金計算レート</span><span class="sxs-lookup"><span data-stu-id="4268d-114">Benefit Calculation Rate</span></span> | <span data-ttu-id="4268d-115">cdm_benefitcalculationrate</span><span class="sxs-lookup"><span data-stu-id="4268d-115">cdm_benefitcalculationrate</span></span> |
| <span data-ttu-id="4268d-116">給付金計算レートの詳細</span><span class="sxs-lookup"><span data-stu-id="4268d-116">Benefit Calculation Rate Detail</span></span> | <span data-ttu-id="4268d-117">cdm_benefitcalculationratedetail</span><span class="sxs-lookup"><span data-stu-id="4268d-117">cdm_benefitcalculationratedetail</span></span> |
| <span data-ttu-id="4268d-118">福利厚生オプション</span><span class="sxs-lookup"><span data-stu-id="4268d-118">Benefit Option</span></span> | <span data-ttu-id="4268d-119">cdm_benefitoption</span><span class="sxs-lookup"><span data-stu-id="4268d-119">cdm_benefitoption</span></span> |
| <span data-ttu-id="4268d-120">給付金計画</span><span class="sxs-lookup"><span data-stu-id="4268d-120">Benefit Plan</span></span> | <span data-ttu-id="4268d-121">cdm_benefitplan (ユーザー定義サポートは有効になっていません)</span><span class="sxs-lookup"><span data-stu-id="4268d-121">cdm_benefitplan (Not enabled for custom field support)</span></span> |
| <span data-ttu-id="4268d-122">給付金タイプ</span><span class="sxs-lookup"><span data-stu-id="4268d-122">Benefit Type</span></span> | <span data-ttu-id="4268d-123">cdm_benefittype</span><span class="sxs-lookup"><span data-stu-id="4268d-123">cdm_benefittype</span></span> |

## <a name="business-process-tasks-entities"></a><span data-ttu-id="4268d-124">ビジネス プロセス タスク エンティティ</span><span class="sxs-lookup"><span data-stu-id="4268d-124">Business process tasks entities</span></span>

| <span data-ttu-id="4268d-125">氏名</span><span class="sxs-lookup"><span data-stu-id="4268d-125">Name</span></span> | <span data-ttu-id="4268d-126">エンティティ</span><span class="sxs-lookup"><span data-stu-id="4268d-126">Entity</span></span> |
| --- | --- |
| <span data-ttu-id="4268d-127">業務プロセス カレンダー</span><span class="sxs-lookup"><span data-stu-id="4268d-127">Business Process Calendar</span></span> | <span data-ttu-id="4268d-128">cdm_businessprocesscalendar</span><span class="sxs-lookup"><span data-stu-id="4268d-128">cdm_businessprocesscalendar</span></span> |
| <span data-ttu-id="4268d-129">業務プロセス グループの割り当て</span><span class="sxs-lookup"><span data-stu-id="4268d-129">Business Process Group Assignment</span></span> | <span data-ttu-id="4268d-130">cdm_businessprocessgroupassignment</span><span class="sxs-lookup"><span data-stu-id="4268d-130">cdm_businessprocessgroupassignment</span></span> |
| <span data-ttu-id="4268d-131">業務プロセス ライブラリ タスク グループ</span><span class="sxs-lookup"><span data-stu-id="4268d-131">Business Process Library Task Group</span></span> | <span data-ttu-id="4268d-132">cdm_businessprocesslibrarytaskgroup</span><span class="sxs-lookup"><span data-stu-id="4268d-132">cdm_businessprocesslibrarytaskgroup</span></span> |
| <span data-ttu-id="4268d-133">業務プロセス ステージ</span><span class="sxs-lookup"><span data-stu-id="4268d-133">Business Process Stage</span></span> | <span data-ttu-id="4268d-134">cdm_businessprocessstage</span><span class="sxs-lookup"><span data-stu-id="4268d-134">cdm_businessprocessstage</span></span> |
| <span data-ttu-id="4268d-135">チェックリストのテンプレート ヘッダー</span><span class="sxs-lookup"><span data-stu-id="4268d-135">Checklist Template Header</span></span> | <span data-ttu-id="4268d-136">cdm_businessprocesstemplateheader</span><span class="sxs-lookup"><span data-stu-id="4268d-136">cdm_businessprocesstemplateheader</span></span> |
| <span data-ttu-id="4268d-137">チェックリストのテンプレート タスク</span><span class="sxs-lookup"><span data-stu-id="4268d-137">Checklist Template Task</span></span> | <span data-ttu-id="4268d-138">cdm_businessprocesstemplatetask</span><span class="sxs-lookup"><span data-stu-id="4268d-138">cdm_businessprocesstemplatetask</span></span> |

## <a name="compensation-entities"></a><span data-ttu-id="4268d-139">報酬エンティティ</span><span class="sxs-lookup"><span data-stu-id="4268d-139">Compensation entities</span></span>

| <span data-ttu-id="4268d-140">氏名</span><span class="sxs-lookup"><span data-stu-id="4268d-140">Name</span></span> | <span data-ttu-id="4268d-141">エンティティ</span><span class="sxs-lookup"><span data-stu-id="4268d-141">Entity</span></span> |
| --- | --- |
| <span data-ttu-id="4268d-142">報酬固定計画</span><span class="sxs-lookup"><span data-stu-id="4268d-142">Compensation Fixed Plan</span></span> | <span data-ttu-id="4268d-143">cdm_compensationfixedplan</span><span class="sxs-lookup"><span data-stu-id="4268d-143">cdm_compensationfixedplan</span></span> |
| <span data-ttu-id="4268d-144">報酬グリッド</span><span class="sxs-lookup"><span data-stu-id="4268d-144">Compensation Grid</span></span> | <span data-ttu-id="4268d-145">cdm_compensationgrid</span><span class="sxs-lookup"><span data-stu-id="4268d-145">cdm_compensationgrid</span></span> |
| <span data-ttu-id="4268d-146">報酬レベル</span><span class="sxs-lookup"><span data-stu-id="4268d-146">Compensation Level</span></span> | <span data-ttu-id="4268d-147">cdm_compensationlevel</span><span class="sxs-lookup"><span data-stu-id="4268d-147">cdm_compensationlevel</span></span> |
| <span data-ttu-id="4268d-148">報酬支払頻度</span><span class="sxs-lookup"><span data-stu-id="4268d-148">Compensation Pay Frequency</span></span> | <span data-ttu-id="4268d-149">cdm_compensationpayfrequency</span><span class="sxs-lookup"><span data-stu-id="4268d-149">cdm_compensationpayfrequency</span></span> |
| <span data-ttu-id="4268d-150">報酬基準点設定</span><span class="sxs-lookup"><span data-stu-id="4268d-150">Compensation Reference Point Setup</span></span> | <span data-ttu-id="4268d-151">cdm_compensationreferencepointsetup</span><span class="sxs-lookup"><span data-stu-id="4268d-151">cdm_compensationreferencepointsetup</span></span> |
| <span data-ttu-id="4268d-152">報酬基準点設定ライン</span><span class="sxs-lookup"><span data-stu-id="4268d-152">Compensation Reference Point Setup Line</span></span> | <span data-ttu-id="4268d-153">cdm_compensationreferencepointsetupline</span><span class="sxs-lookup"><span data-stu-id="4268d-153">cdm_compensationreferencepointsetupline</span></span> |
| <span data-ttu-id="4268d-154">報酬地域</span><span class="sxs-lookup"><span data-stu-id="4268d-154">Compensation Region</span></span> | <span data-ttu-id="4268d-155">cdm_compensationregion</span><span class="sxs-lookup"><span data-stu-id="4268d-155">cdm_compensationregion</span></span> |
| <span data-ttu-id="4268d-156">報酬構造</span><span class="sxs-lookup"><span data-stu-id="4268d-156">Compensation Structure</span></span> | <span data-ttu-id="4268d-157">cdm_compensationstructure</span><span class="sxs-lookup"><span data-stu-id="4268d-157">cdm_compensationstructure</span></span> |
| <span data-ttu-id="4268d-158">報酬変動プラン</span><span class="sxs-lookup"><span data-stu-id="4268d-158">Compensation Variable Plan</span></span> | <span data-ttu-id="4268d-159">cdm_compensationvariableplan</span><span class="sxs-lookup"><span data-stu-id="4268d-159">cdm_compensationvariableplan</span></span> |
| <span data-ttu-id="4268d-160">報酬変動プラン レベル</span><span class="sxs-lookup"><span data-stu-id="4268d-160">Compensation Variable Plan Level</span></span> | <span data-ttu-id="4268d-161">cdm_compensationvariableplanlevel</span><span class="sxs-lookup"><span data-stu-id="4268d-161">cdm_compensationvariableplanlevel</span></span> |
| <span data-ttu-id="4268d-162">報酬変動プラン タイプ</span><span class="sxs-lookup"><span data-stu-id="4268d-162">Compensation Variable Plan Type</span></span> | <span data-ttu-id="4268d-163">cdm_compensationvariableplantype</span><span class="sxs-lookup"><span data-stu-id="4268d-163">cdm_compensationvariableplantype</span></span> |
| <span data-ttu-id="4268d-164">固定報酬イベント</span><span class="sxs-lookup"><span data-stu-id="4268d-164">Fixed Compensation Event</span></span> | <span data-ttu-id="4268d-165">cdm_fixedcompensationevent</span><span class="sxs-lookup"><span data-stu-id="4268d-165">cdm_fixedcompensationevent</span></span> |
| <span data-ttu-id="4268d-166">給付ルール</span><span class="sxs-lookup"><span data-stu-id="4268d-166">Vesting Rule</span></span> | <span data-ttu-id="4268d-167">cdm_vestingrule</span><span class="sxs-lookup"><span data-stu-id="4268d-167">cdm_vestingrule</span></span> |
| <span data-ttu-id="4268d-168">ワーカー固定報酬</span><span class="sxs-lookup"><span data-stu-id="4268d-168">Worker Fixed Compensation</span></span> | <span data-ttu-id="4268d-169">cdm_workerfixedcompensation</span><span class="sxs-lookup"><span data-stu-id="4268d-169">cdm_workerfixedcompensation</span></span> |

## <a name="organization-entities"></a><span data-ttu-id="4268d-170">組織エンティティ</span><span class="sxs-lookup"><span data-stu-id="4268d-170">Organization entities</span></span>

| <span data-ttu-id="4268d-171">氏名</span><span class="sxs-lookup"><span data-stu-id="4268d-171">Name</span></span> | <span data-ttu-id="4268d-172">エンティティ</span><span class="sxs-lookup"><span data-stu-id="4268d-172">Entity</span></span> |
| --- | --- |
| <span data-ttu-id="4268d-173">部門</span><span class="sxs-lookup"><span data-stu-id="4268d-173">Department</span></span> | <span data-ttu-id="4268d-174">cdm_department</span><span class="sxs-lookup"><span data-stu-id="4268d-174">cdm_department</span></span> |
| <span data-ttu-id="4268d-175">雇用</span><span class="sxs-lookup"><span data-stu-id="4268d-175">Employment</span></span> | <span data-ttu-id="4268d-176">cdm_employment</span><span class="sxs-lookup"><span data-stu-id="4268d-176">cdm_employment</span></span> |
| <span data-ttu-id="4268d-177">法人</span><span class="sxs-lookup"><span data-stu-id="4268d-177">Company</span></span> | <span data-ttu-id="4268d-178">cdm_company</span><span class="sxs-lookup"><span data-stu-id="4268d-178">cdm_company</span></span> |
| <span data-ttu-id="4268d-179">ジョブ</span><span class="sxs-lookup"><span data-stu-id="4268d-179">Job</span></span> | <span data-ttu-id="4268d-180">cdm_job</span><span class="sxs-lookup"><span data-stu-id="4268d-180">cdm_job</span></span> |
| <span data-ttu-id="4268d-181">職務権限</span><span class="sxs-lookup"><span data-stu-id="4268d-181">Job Function</span></span> | <span data-ttu-id="4268d-182">cdm_jobfunction</span><span class="sxs-lookup"><span data-stu-id="4268d-182">cdm_jobfunction</span></span> |
| <span data-ttu-id="4268d-183">職位</span><span class="sxs-lookup"><span data-stu-id="4268d-183">Job Position</span></span> | <span data-ttu-id="4268d-184">cdm_jobposition</span><span class="sxs-lookup"><span data-stu-id="4268d-184">cdm_jobposition</span></span> |
| <span data-ttu-id="4268d-185">職位タイプ</span><span class="sxs-lookup"><span data-stu-id="4268d-185">Position Type</span></span> | <span data-ttu-id="4268d-186">cdm_positiontype</span><span class="sxs-lookup"><span data-stu-id="4268d-186">cdm_positiontype</span></span> |
| <span data-ttu-id="4268d-187">職位作業者割り当て</span><span class="sxs-lookup"><span data-stu-id="4268d-187">Position Worker Assignment</span></span> | <span data-ttu-id="4268d-188">cdm_positionworkerassignmentmap</span><span class="sxs-lookup"><span data-stu-id="4268d-188">cdm_positionworkerassignmentmap</span></span> |
| <span data-ttu-id="4268d-189">職位分析コード</span><span class="sxs-lookup"><span data-stu-id="4268d-189">Job Position Dimension</span></span> | <span data-ttu-id="4268d-190">cdm_jobpositiondimension</span><span class="sxs-lookup"><span data-stu-id="4268d-190">cdm_jobpositiondimension</span></span>|
| <span data-ttu-id="4268d-191">職務タイプ</span><span class="sxs-lookup"><span data-stu-id="4268d-191">Job Type</span></span> | <span data-ttu-id="4268d-192">cdm_jobtype</span><span class="sxs-lookup"><span data-stu-id="4268d-192">cdm_jobtype</span></span> |
| <span data-ttu-id="4268d-193">言語</span><span class="sxs-lookup"><span data-stu-id="4268d-193">Language</span></span> | <span data-ttu-id="4268d-194">cdm_language</span><span class="sxs-lookup"><span data-stu-id="4268d-194">cdm_language</span></span> |
| <span data-ttu-id="4268d-195">タイトル</span><span class="sxs-lookup"><span data-stu-id="4268d-195">Title</span></span> | <span data-ttu-id="4268d-196">cdm_title</span><span class="sxs-lookup"><span data-stu-id="4268d-196">cdm_title</span></span> |

> [!NOTE]
> <span data-ttu-id="4268d-197">**職位タイプ** に使用する財務分析コード 、**作業者の職位割り当て**、および **従業員** は、Common Data Service にて一方向の統合機能が用意されています。</span><span class="sxs-lookup"><span data-stu-id="4268d-197">Financial dimensions for **Position Type**, **Position Worker Assignment**, and **Employment** provide one-direction integration to Common Data Service.</span></span> <span data-ttu-id="4268d-198">財務分析コードの更新は、現在のところ、 Common Data Service から Human Resources へは同期されません。</span><span class="sxs-lookup"><span data-stu-id="4268d-198">Financial dimensions updates currently can't synchronize from Common Data Service to Human Resources.</span></span> 

## <a name="leave-and-absence-entities"></a><span data-ttu-id="4268d-199">休暇エンティティ</span><span class="sxs-lookup"><span data-stu-id="4268d-199">Leave and absence entities</span></span>

| <span data-ttu-id="4268d-200">氏名</span><span class="sxs-lookup"><span data-stu-id="4268d-200">Name</span></span> | <span data-ttu-id="4268d-201">エンティティ</span><span class="sxs-lookup"><span data-stu-id="4268d-201">Entity</span></span> |
| --- | --- |
| <span data-ttu-id="4268d-202">休暇バンク トランザクション</span><span class="sxs-lookup"><span data-stu-id="4268d-202">Leave Bank Transaction</span></span> | <span data-ttu-id="4268d-203">cdm_leavebanktransaction</span><span class="sxs-lookup"><span data-stu-id="4268d-203">cdm_leavebanktransaction</span></span> |
| <span data-ttu-id="4268d-204">加入契約から移動</span><span class="sxs-lookup"><span data-stu-id="4268d-204">Leave Enrollment</span></span> | <span data-ttu-id="4268d-205">cdm_leaveenrollment</span><span class="sxs-lookup"><span data-stu-id="4268d-205">cdm_leaveenrollment</span></span> |
| <span data-ttu-id="4268d-206">休暇計画</span><span class="sxs-lookup"><span data-stu-id="4268d-206">Leave Plan</span></span> | <span data-ttu-id="4268d-207">cdm_leaveplan</span><span class="sxs-lookup"><span data-stu-id="4268d-207">cdm_leaveplan</span></span> |
| <span data-ttu-id="4268d-208">休暇申請</span><span class="sxs-lookup"><span data-stu-id="4268d-208">Leave Request</span></span> | <span data-ttu-id="4268d-209">cdm_leaverequest</span><span class="sxs-lookup"><span data-stu-id="4268d-209">cdm_leaverequest</span></span> |
| <span data-ttu-id="4268d-210">休暇申請詳細情報</span><span class="sxs-lookup"><span data-stu-id="4268d-210">Leave Request Detail</span></span> | <span data-ttu-id="4268d-211">cdm_leaverequestdetail</span><span class="sxs-lookup"><span data-stu-id="4268d-211">cdm_leaverequestdetail</span></span> |
| <span data-ttu-id="4268d-212">休暇タイプ</span><span class="sxs-lookup"><span data-stu-id="4268d-212">Leave Type</span></span> | <span data-ttu-id="4268d-213">cdm_leavetype</span><span class="sxs-lookup"><span data-stu-id="4268d-213">cdm_leavetype</span></span> |
| <span data-ttu-id="4268d-214">休暇タイプの理由コード</span><span class="sxs-lookup"><span data-stu-id="4268d-214">Leave Type Reason Code</span></span> | <span data-ttu-id="4268d-215">cdm_leavetypereasoncode</span><span class="sxs-lookup"><span data-stu-id="4268d-215">cdm_leavetypereasoncode</span></span> |

## <a name="payroll-entities"></a><span data-ttu-id="4268d-216">給与エンティティ</span><span class="sxs-lookup"><span data-stu-id="4268d-216">Payroll entities</span></span>

| <span data-ttu-id="4268d-217">氏名</span><span class="sxs-lookup"><span data-stu-id="4268d-217">Name</span></span> | <span data-ttu-id="4268d-218">エンティティ</span><span class="sxs-lookup"><span data-stu-id="4268d-218">Entity</span></span> |
| --- | --- |
| <span data-ttu-id="4268d-219">支払サイクル</span><span class="sxs-lookup"><span data-stu-id="4268d-219">Pay Cycle</span></span> | <span data-ttu-id="4268d-220">cdm_paycycle</span><span class="sxs-lookup"><span data-stu-id="4268d-220">cdm_paycycle</span></span> |
| <span data-ttu-id="4268d-221">支払期間</span><span class="sxs-lookup"><span data-stu-id="4268d-221">Pay Period</span></span> | <span data-ttu-id="4268d-222">cdm_payperiod</span><span class="sxs-lookup"><span data-stu-id="4268d-222">cdm_payperiod</span></span> |
| <span data-ttu-id="4268d-223">給与所得コード</span><span class="sxs-lookup"><span data-stu-id="4268d-223">Payroll Earning Code</span></span> | <span data-ttu-id="4268d-224">cdm_payrollearningcode</span><span class="sxs-lookup"><span data-stu-id="4268d-224">cdm_payrollearningcode</span></span> |
| <span data-ttu-id="4268d-225">銀行口座支出</span><span class="sxs-lookup"><span data-stu-id="4268d-225">Bank Account Disbursement</span></span> | <span data-ttu-id="4268d-226">cdm_bankaccountdisbursement</span><span class="sxs-lookup"><span data-stu-id="4268d-226">cdm_bankaccountdisbursement</span></span> |
| <span data-ttu-id="4268d-227">税地域</span><span class="sxs-lookup"><span data-stu-id="4268d-227">Tax Region</span></span> | <span data-ttu-id="4268d-228">cdm_taxregion</span><span class="sxs-lookup"><span data-stu-id="4268d-228">cdm_taxregion</span></span> |

## <a name="worker-entities"></a><span data-ttu-id="4268d-229">作業者エンティティ</span><span class="sxs-lookup"><span data-stu-id="4268d-229">Worker entities</span></span>

| <span data-ttu-id="4268d-230">氏名</span><span class="sxs-lookup"><span data-stu-id="4268d-230">Name</span></span> | <span data-ttu-id="4268d-231">エンティティ</span><span class="sxs-lookup"><span data-stu-id="4268d-231">Entity</span></span> |
| --- | --- |
| <span data-ttu-id="4268d-232">ワーカー</span><span class="sxs-lookup"><span data-stu-id="4268d-232">Worker</span></span> | <span data-ttu-id="4268d-233">cdm_worker</span><span class="sxs-lookup"><span data-stu-id="4268d-233">cdm_worker</span></span> |
| <span data-ttu-id="4268d-234">ワーカーの住所</span><span class="sxs-lookup"><span data-stu-id="4268d-234">Worker Address</span></span> | <span data-ttu-id="4268d-235">cdm_workeraddress</span><span class="sxs-lookup"><span data-stu-id="4268d-235">cdm_workeraddress</span></span> |
| <span data-ttu-id="4268d-236">ワーカーの個人情報詳細</span><span class="sxs-lookup"><span data-stu-id="4268d-236">Worker Personal Detail</span></span> | <span data-ttu-id="4268d-237">cdm_workerpersonaldetail</span><span class="sxs-lookup"><span data-stu-id="4268d-237">cdm_workerpersonaldetail</span></span> |
| <span data-ttu-id="4268d-238">ワーカーの個人識別番号</span><span class="sxs-lookup"><span data-stu-id="4268d-238">Worker Person Identification Number</span></span> | <span data-ttu-id="4268d-239">cdm_workerpersonidentificationnumber</span><span class="sxs-lookup"><span data-stu-id="4268d-239">cdm_workerpersonidentificationnumber</span></span> |
| <span data-ttu-id="4268d-240">作業者の ID タイプ</span><span class="sxs-lookup"><span data-stu-id="4268d-240">Worker Person Identification Type</span></span> | <span data-ttu-id="4268d-241">cdm_workerpersonidentificationtype</span><span class="sxs-lookup"><span data-stu-id="4268d-241">cdm_workerpersonidentificationtype</span></span> |
| <span data-ttu-id="4268d-242">作業カレンダー</span><span class="sxs-lookup"><span data-stu-id="4268d-242">Work Calendar</span></span> | <span data-ttu-id="4268d-243">cdm_workcalendar</span><span class="sxs-lookup"><span data-stu-id="4268d-243">cdm_workcalendar</span></span> |
| <span data-ttu-id="4268d-244">作業カレンダー日</span><span class="sxs-lookup"><span data-stu-id="4268d-244">Work Calendar Day</span></span> | <span data-ttu-id="4268d-245">cdm_workcalendarday</span><span class="sxs-lookup"><span data-stu-id="4268d-245">cdm_workcalendarday</span></span> |
| <span data-ttu-id="4268d-246">作業カレンダーの休日</span><span class="sxs-lookup"><span data-stu-id="4268d-246">Work Calendar Holiday</span></span> |<span data-ttu-id="4268d-247">cdm_workcalendarholiday</span><span class="sxs-lookup"><span data-stu-id="4268d-247">cdm_workcalendarholiday</span></span> |
| <span data-ttu-id="4268d-248">作業カレンダーの休日行</span><span class="sxs-lookup"><span data-stu-id="4268d-248">Work Calendar Holiday Line</span></span> | <span data-ttu-id="4268d-249">cdm_workcalendarholidayline</span><span class="sxs-lookup"><span data-stu-id="4268d-249">cdm_workcalendarholidayline</span></span> |
| <span data-ttu-id="4268d-250">作業カレンダー時間間隔</span><span class="sxs-lookup"><span data-stu-id="4268d-250">Work Calendar Time Interval</span></span> | <span data-ttu-id="4268d-251">cdm_workcalendartimeinterval (個人定義フィールドサポートは有効になっていません)</span><span class="sxs-lookup"><span data-stu-id="4268d-251">cdm_workcalendartimeinterval (Not enabled for custom field support)</span></span> |
| <span data-ttu-id="4268d-252">ワーカーの銀行口座</span><span class="sxs-lookup"><span data-stu-id="4268d-252">Worker Bank Account</span></span> | <span data-ttu-id="4268d-253">cdm_workerbankaccount</span><span class="sxs-lookup"><span data-stu-id="4268d-253">cdm_workerbankaccount</span></span> |

## <a name="worker-setup-entities"></a><span data-ttu-id="4268d-254">ワーカーの設定エンティティ</span><span class="sxs-lookup"><span data-stu-id="4268d-254">Worker setup entities</span></span>

| <span data-ttu-id="4268d-255">氏名</span><span class="sxs-lookup"><span data-stu-id="4268d-255">Name</span></span> | <span data-ttu-id="4268d-256">エンティティ</span><span class="sxs-lookup"><span data-stu-id="4268d-256">Entity</span></span> |
| --- | --- |
| <span data-ttu-id="4268d-257">退役軍人状態</span><span class="sxs-lookup"><span data-stu-id="4268d-257">Veteran Status</span></span> | <span data-ttu-id="4268d-258">cdm_veteranstatus</span><span class="sxs-lookup"><span data-stu-id="4268d-258">cdm_veteranstatus</span></span> |
| <span data-ttu-id="4268d-259">出身民族</span><span class="sxs-lookup"><span data-stu-id="4268d-259">Ethnic Origin</span></span> | <span data-ttu-id="4268d-260">cdm_ethnicorigin</span><span class="sxs-lookup"><span data-stu-id="4268d-260">cdm_ethnicorigin</span></span> |
| <span data-ttu-id="4268d-261">理由コード</span><span class="sxs-lookup"><span data-stu-id="4268d-261">Reason Code</span></span> | <span data-ttu-id="4268d-262">cdm_reasoncode</span><span class="sxs-lookup"><span data-stu-id="4268d-262">cdm_reasoncode</span></span> |
| <span data-ttu-id="4268d-263">個人識別発行代理店</span><span class="sxs-lookup"><span data-stu-id="4268d-263">Person Identification Issuing Agency</span></span> | <span data-ttu-id="4268d-264">cdm_personidentificationissuingagency</span><span class="sxs-lookup"><span data-stu-id="4268d-264">cdm_personidentificationissuingagency</span></span> |

## <a name="competency-entities"></a><span data-ttu-id="4268d-265">コンピテンシー エンティティ</span><span class="sxs-lookup"><span data-stu-id="4268d-265">Competency entities</span></span>

| <span data-ttu-id="4268d-266">氏名</span><span class="sxs-lookup"><span data-stu-id="4268d-266">Name</span></span> | <span data-ttu-id="4268d-267">エンティティ</span><span class="sxs-lookup"><span data-stu-id="4268d-267">Entity</span></span> |
| --- | --- |
| <span data-ttu-id="4268d-268">スキルの種類</span><span class="sxs-lookup"><span data-stu-id="4268d-268">Skill Type</span></span> | <span data-ttu-id="4268d-269">cdm_skilltype</span><span class="sxs-lookup"><span data-stu-id="4268d-269">cdm_skilltype</span></span> |

## <a name="entity-relationship-models"></a><span data-ttu-id="4268d-270">エンティティ関係モデル</span><span class="sxs-lookup"><span data-stu-id="4268d-270">Entity relationship models</span></span>

### <a name="worker"></a><span data-ttu-id="4268d-271">ワーカー</span><span class="sxs-lookup"><span data-stu-id="4268d-271">Worker</span></span>

![ワーカー](./media/HCMCommon-worker-entity-diagram.png)

### <a name="job-and-job-position"></a><span data-ttu-id="4268d-273">職務および職位</span><span class="sxs-lookup"><span data-stu-id="4268d-273">Job and Job Position</span></span>

![職務および職位](./media/HCMCommon-job-and-job-position-entity-diagram.png)

### <a name="benefits"></a><span data-ttu-id="4268d-275">福利厚生</span><span class="sxs-lookup"><span data-stu-id="4268d-275">Benefits</span></span>

![福利厚生](./media/HCMCommon-benefits-entity-diagram.png)

### <a name="compensation"></a><span data-ttu-id="4268d-277">報酬</span><span class="sxs-lookup"><span data-stu-id="4268d-277">Compensation</span></span>

![報酬](./media/HCMCommon-compensation-entity-diagram.png)

### <a name="leave"></a><span data-ttu-id="4268d-279">離脱</span><span class="sxs-lookup"><span data-stu-id="4268d-279">Leave</span></span>

![離脱](./media/HCMCommon-leave-entity-diagram.png)

### <a name="work-calendar"></a><span data-ttu-id="4268d-281">作業カレンダー</span><span class="sxs-lookup"><span data-stu-id="4268d-281">Work Calendar</span></span>

![作業カレンダー](./media/HCMCommon-work-calendar-entity-diagram.png)

## <a name="see-also"></a><span data-ttu-id="4268d-283">参照</span><span class="sxs-lookup"><span data-stu-id="4268d-283">See also</span></span>

[<span data-ttu-id="4268d-284">データ統合テクノロジの選択</span><span class="sxs-lookup"><span data-stu-id="4268d-284">Choose a data integration technology</span></span>](hr-admin-integration-choose-technology.md)</br>
[<span data-ttu-id="4268d-285">Common Data Service 統合のコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="4268d-285">Configure Common Data Service integration</span></span>](hr-admin-integration-common-data-service.md)
