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
ms.openlocfilehash: 6879a45dd1fcc1ba718747aaaf0d7936c2eac49f
ms.sourcegitcommit: 3cad15f8ecc257d3a45c1bc1fada7c094ff4bcec
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/26/2020
ms.locfileid: "3087349"
---
# <a name="common-data-service-entities"></a><span data-ttu-id="47080-103">Common Data Service エンティティ</span><span class="sxs-lookup"><span data-stu-id="47080-103">Common Data Service entities</span></span>

<span data-ttu-id="47080-104">Microsoft Dynamics 365 Human Resources は、Common Data Service を使用して拡張性シナリオおよび統合シナリオを有効にします。</span><span class="sxs-lookup"><span data-stu-id="47080-104">Microsoft Dynamics 365 Human Resources uses Common Data Service to enable extensibility and integration scenarios.</span></span>

<span data-ttu-id="47080-105">Common Data Service の詳細については、[Common Data Service とは何か](https://docs.microsoft.com/powerapps/maker/common-data-service/data-platform-intro)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="47080-105">For more information about Common Data Service, see [What is Common Data Service](https://docs.microsoft.com/powerapps/maker/common-data-service/data-platform-intro).</span></span>

<span data-ttu-id="47080-106">次の人事管理エンティティは、Common Data Service で使用できます。</span><span class="sxs-lookup"><span data-stu-id="47080-106">The following Human Resources entities are available in Common Data Service.</span></span>

## <a name="benefit-entities"></a><span data-ttu-id="47080-107">Benefit エンティティ</span><span class="sxs-lookup"><span data-stu-id="47080-107">Benefit entities</span></span>

| <span data-ttu-id="47080-108">氏名</span><span class="sxs-lookup"><span data-stu-id="47080-108">Name</span></span> | <span data-ttu-id="47080-109">エンティティ</span><span class="sxs-lookup"><span data-stu-id="47080-109">Entity</span></span> |
| --- | --- |
| <span data-ttu-id="47080-110">給付金計算頻度</span><span class="sxs-lookup"><span data-stu-id="47080-110">Benefit Calculation Frequency</span></span> | <span data-ttu-id="47080-111">cdm_benefitcalculationfrequency</span><span class="sxs-lookup"><span data-stu-id="47080-111">cdm_benefitcalculationfrequency</span></span> |
| <span data-ttu-id="47080-112">給付金計算頻度支払期間</span><span class="sxs-lookup"><span data-stu-id="47080-112">Benefit Calculation Frequency Pay Period</span></span> | <span data-ttu-id="47080-113">cdm_benefitcalculationfrequencypayperiod</span><span class="sxs-lookup"><span data-stu-id="47080-113">cdm_benefitcalculationfrequencypayperiod</span></span> |
| <span data-ttu-id="47080-114">給付金計算レート</span><span class="sxs-lookup"><span data-stu-id="47080-114">Benefit Calculation Rate</span></span> | <span data-ttu-id="47080-115">cdm_benefitcalculationrate</span><span class="sxs-lookup"><span data-stu-id="47080-115">cdm_benefitcalculationrate</span></span> |
| <span data-ttu-id="47080-116">給付金計算レートの詳細</span><span class="sxs-lookup"><span data-stu-id="47080-116">Benefit Calculation Rate Detail</span></span> | <span data-ttu-id="47080-117">cdm_benefitcalculationratedetail</span><span class="sxs-lookup"><span data-stu-id="47080-117">cdm_benefitcalculationratedetail</span></span> |
| <span data-ttu-id="47080-118">福利厚生オプション</span><span class="sxs-lookup"><span data-stu-id="47080-118">Benefit Option</span></span> | <span data-ttu-id="47080-119">cdm_benefitoption</span><span class="sxs-lookup"><span data-stu-id="47080-119">cdm_benefitoption</span></span> |
| <span data-ttu-id="47080-120">給付金計画</span><span class="sxs-lookup"><span data-stu-id="47080-120">Benefit Plan</span></span> | <span data-ttu-id="47080-121">cdm_benefitplan (ユーザー定義サポートは有効になっていません)</span><span class="sxs-lookup"><span data-stu-id="47080-121">cdm_benefitplan (Not enabled for custom field support)</span></span> |
| <span data-ttu-id="47080-122">給付金タイプ</span><span class="sxs-lookup"><span data-stu-id="47080-122">Benefit Type</span></span> | <span data-ttu-id="47080-123">cdm_benefittype</span><span class="sxs-lookup"><span data-stu-id="47080-123">cdm_benefittype</span></span> |

## <a name="business-process-tasks-entities"></a><span data-ttu-id="47080-124">ビジネス プロセス タスク エンティティ</span><span class="sxs-lookup"><span data-stu-id="47080-124">Business process tasks entities</span></span>

| <span data-ttu-id="47080-125">氏名</span><span class="sxs-lookup"><span data-stu-id="47080-125">Name</span></span> | <span data-ttu-id="47080-126">エンティティ</span><span class="sxs-lookup"><span data-stu-id="47080-126">Entity</span></span> |
| --- | --- |
| <span data-ttu-id="47080-127">業務プロセス カレンダー</span><span class="sxs-lookup"><span data-stu-id="47080-127">Business Process Calendar</span></span> | <span data-ttu-id="47080-128">cdm_businessprocesscalendar</span><span class="sxs-lookup"><span data-stu-id="47080-128">cdm_businessprocesscalendar</span></span> |
| <span data-ttu-id="47080-129">業務プロセス グループの割り当て</span><span class="sxs-lookup"><span data-stu-id="47080-129">Business Process Group Assignment</span></span> | <span data-ttu-id="47080-130">cdm_businessprocessgroupassignment</span><span class="sxs-lookup"><span data-stu-id="47080-130">cdm_businessprocessgroupassignment</span></span> |
| <span data-ttu-id="47080-131">業務プロセス ライブラリ タスク グループ</span><span class="sxs-lookup"><span data-stu-id="47080-131">Business Process Library Task Group</span></span> | <span data-ttu-id="47080-132">cdm_businessprocesslibrarytaskgroup</span><span class="sxs-lookup"><span data-stu-id="47080-132">cdm_businessprocesslibrarytaskgroup</span></span> |
| <span data-ttu-id="47080-133">業務プロセス ステージ</span><span class="sxs-lookup"><span data-stu-id="47080-133">Business Process Stage</span></span> | <span data-ttu-id="47080-134">cdm_businessprocessstage</span><span class="sxs-lookup"><span data-stu-id="47080-134">cdm_businessprocessstage</span></span> |
| <span data-ttu-id="47080-135">チェックリストのテンプレート ヘッダー</span><span class="sxs-lookup"><span data-stu-id="47080-135">Checklist Template Header</span></span> | <span data-ttu-id="47080-136">cdm_businessprocesstemplateheader</span><span class="sxs-lookup"><span data-stu-id="47080-136">cdm_businessprocesstemplateheader</span></span> |
| <span data-ttu-id="47080-137">チェックリストのテンプレート タスク</span><span class="sxs-lookup"><span data-stu-id="47080-137">Checklist Template Task</span></span> | <span data-ttu-id="47080-138">cdm_businessprocesstemplatetask</span><span class="sxs-lookup"><span data-stu-id="47080-138">cdm_businessprocesstemplatetask</span></span> |

## <a name="compensation-entities"></a><span data-ttu-id="47080-139">報酬エンティティ</span><span class="sxs-lookup"><span data-stu-id="47080-139">Compensation entities</span></span>

| <span data-ttu-id="47080-140">氏名</span><span class="sxs-lookup"><span data-stu-id="47080-140">Name</span></span> | <span data-ttu-id="47080-141">エンティティ</span><span class="sxs-lookup"><span data-stu-id="47080-141">Entity</span></span> |
| --- | --- |
| <span data-ttu-id="47080-142">報酬固定計画</span><span class="sxs-lookup"><span data-stu-id="47080-142">Compensation Fixed Plan</span></span> | <span data-ttu-id="47080-143">cdm_compensationfixedplan</span><span class="sxs-lookup"><span data-stu-id="47080-143">cdm_compensationfixedplan</span></span> |
| <span data-ttu-id="47080-144">報酬グリッド</span><span class="sxs-lookup"><span data-stu-id="47080-144">Compensation Grid</span></span> | <span data-ttu-id="47080-145">cdm_compensationgrid</span><span class="sxs-lookup"><span data-stu-id="47080-145">cdm_compensationgrid</span></span> |
| <span data-ttu-id="47080-146">報酬レベル</span><span class="sxs-lookup"><span data-stu-id="47080-146">Compensation Level</span></span> | <span data-ttu-id="47080-147">cdm_compensationlevel</span><span class="sxs-lookup"><span data-stu-id="47080-147">cdm_compensationlevel</span></span> |
| <span data-ttu-id="47080-148">報酬支払頻度</span><span class="sxs-lookup"><span data-stu-id="47080-148">Compensation Pay Frequency</span></span> | <span data-ttu-id="47080-149">cdm_compensationpayfrequency</span><span class="sxs-lookup"><span data-stu-id="47080-149">cdm_compensationpayfrequency</span></span> |
| <span data-ttu-id="47080-150">報酬基準点設定</span><span class="sxs-lookup"><span data-stu-id="47080-150">Compensation Reference Point Setup</span></span> | <span data-ttu-id="47080-151">cdm_compensationreferencepointsetup</span><span class="sxs-lookup"><span data-stu-id="47080-151">cdm_compensationreferencepointsetup</span></span> |
| <span data-ttu-id="47080-152">報酬基準点設定ライン</span><span class="sxs-lookup"><span data-stu-id="47080-152">Compensation Reference Point Setup Line</span></span> | <span data-ttu-id="47080-153">cdm_compensationreferencepointsetupline</span><span class="sxs-lookup"><span data-stu-id="47080-153">cdm_compensationreferencepointsetupline</span></span> |
| <span data-ttu-id="47080-154">報酬地域</span><span class="sxs-lookup"><span data-stu-id="47080-154">Compensation Region</span></span> | <span data-ttu-id="47080-155">cdm_compensationregion</span><span class="sxs-lookup"><span data-stu-id="47080-155">cdm_compensationregion</span></span> |
| <span data-ttu-id="47080-156">報酬構造</span><span class="sxs-lookup"><span data-stu-id="47080-156">Compensation Structure</span></span> | <span data-ttu-id="47080-157">cdm_compensationstructure</span><span class="sxs-lookup"><span data-stu-id="47080-157">cdm_compensationstructure</span></span> |
| <span data-ttu-id="47080-158">報酬変動プラン</span><span class="sxs-lookup"><span data-stu-id="47080-158">Compensation Variable Plan</span></span> | <span data-ttu-id="47080-159">cdm_compensationvariableplan</span><span class="sxs-lookup"><span data-stu-id="47080-159">cdm_compensationvariableplan</span></span> |
| <span data-ttu-id="47080-160">報酬変動プラン レベル</span><span class="sxs-lookup"><span data-stu-id="47080-160">Compensation Variable Plan Level</span></span> | <span data-ttu-id="47080-161">cdm_compensationvariableplanlevel</span><span class="sxs-lookup"><span data-stu-id="47080-161">cdm_compensationvariableplanlevel</span></span> |
| <span data-ttu-id="47080-162">報酬変動プラン タイプ</span><span class="sxs-lookup"><span data-stu-id="47080-162">Compensation Variable Plan Type</span></span> | <span data-ttu-id="47080-163">cdm_compensationvariableplantype</span><span class="sxs-lookup"><span data-stu-id="47080-163">cdm_compensationvariableplantype</span></span> |
| <span data-ttu-id="47080-164">固定報酬イベント</span><span class="sxs-lookup"><span data-stu-id="47080-164">Fixed Compensation Event</span></span> | <span data-ttu-id="47080-165">cdm_fixedcompensationevent</span><span class="sxs-lookup"><span data-stu-id="47080-165">cdm_fixedcompensationevent</span></span> |
| <span data-ttu-id="47080-166">給付ルール</span><span class="sxs-lookup"><span data-stu-id="47080-166">Vesting Rule</span></span> | <span data-ttu-id="47080-167">cdm_vestingrule</span><span class="sxs-lookup"><span data-stu-id="47080-167">cdm_vestingrule</span></span> |
| <span data-ttu-id="47080-168">ワーカー固定報酬</span><span class="sxs-lookup"><span data-stu-id="47080-168">Worker Fixed Compensation</span></span> | <span data-ttu-id="47080-169">cdm_workerfixedcompensation</span><span class="sxs-lookup"><span data-stu-id="47080-169">cdm_workerfixedcompensation</span></span> |

## <a name="organization-entities"></a><span data-ttu-id="47080-170">組織エンティティ</span><span class="sxs-lookup"><span data-stu-id="47080-170">Organization entities</span></span>

| <span data-ttu-id="47080-171">氏名</span><span class="sxs-lookup"><span data-stu-id="47080-171">Name</span></span> | <span data-ttu-id="47080-172">エンティティ</span><span class="sxs-lookup"><span data-stu-id="47080-172">Entity</span></span> |
| --- | --- |
| <span data-ttu-id="47080-173">部門</span><span class="sxs-lookup"><span data-stu-id="47080-173">Department</span></span> | <span data-ttu-id="47080-174">cdm_department</span><span class="sxs-lookup"><span data-stu-id="47080-174">cdm_department</span></span> |
| <span data-ttu-id="47080-175">雇用</span><span class="sxs-lookup"><span data-stu-id="47080-175">Employment</span></span> | <span data-ttu-id="47080-176">cdm_employment</span><span class="sxs-lookup"><span data-stu-id="47080-176">cdm_employment</span></span> |
| <span data-ttu-id="47080-177">法人</span><span class="sxs-lookup"><span data-stu-id="47080-177">Company</span></span> | <span data-ttu-id="47080-178">cdm_company</span><span class="sxs-lookup"><span data-stu-id="47080-178">cdm_company</span></span> |
| <span data-ttu-id="47080-179">ジョブ</span><span class="sxs-lookup"><span data-stu-id="47080-179">Job</span></span> | <span data-ttu-id="47080-180">cdm_job</span><span class="sxs-lookup"><span data-stu-id="47080-180">cdm_job</span></span> |
| <span data-ttu-id="47080-181">職務権限</span><span class="sxs-lookup"><span data-stu-id="47080-181">Job Function</span></span> | <span data-ttu-id="47080-182">cdm_jobfunction</span><span class="sxs-lookup"><span data-stu-id="47080-182">cdm_jobfunction</span></span> |
| <span data-ttu-id="47080-183">職位</span><span class="sxs-lookup"><span data-stu-id="47080-183">Job Position</span></span> | <span data-ttu-id="47080-184">cdm_jobposition</span><span class="sxs-lookup"><span data-stu-id="47080-184">cdm_jobposition</span></span> |
| <span data-ttu-id="47080-185">職位タイプ</span><span class="sxs-lookup"><span data-stu-id="47080-185">Position Type</span></span> | <span data-ttu-id="47080-186">cdm_positiontype</span><span class="sxs-lookup"><span data-stu-id="47080-186">cdm_positiontype</span></span> |
| <span data-ttu-id="47080-187">ワーカー割り当ての配置</span><span class="sxs-lookup"><span data-stu-id="47080-187">Position Worker Assignment</span></span> | <span data-ttu-id="47080-188">cdm_positionworkerassignmentmap</span><span class="sxs-lookup"><span data-stu-id="47080-188">cdm_positionworkerassignmentmap</span></span> |
| <span data-ttu-id="47080-189">職務タイプ</span><span class="sxs-lookup"><span data-stu-id="47080-189">Job Type</span></span> | <span data-ttu-id="47080-190">cdm_jobtype</span><span class="sxs-lookup"><span data-stu-id="47080-190">cdm_jobtype</span></span> |
| <span data-ttu-id="47080-191">言語</span><span class="sxs-lookup"><span data-stu-id="47080-191">Language</span></span> | <span data-ttu-id="47080-192">cdm_language</span><span class="sxs-lookup"><span data-stu-id="47080-192">cdm_language</span></span> |

## <a name="leave-and-absence-entities"></a><span data-ttu-id="47080-193">休暇エンティティ</span><span class="sxs-lookup"><span data-stu-id="47080-193">Leave and absence entities</span></span>

| <span data-ttu-id="47080-194">氏名</span><span class="sxs-lookup"><span data-stu-id="47080-194">Name</span></span> | <span data-ttu-id="47080-195">エンティティ</span><span class="sxs-lookup"><span data-stu-id="47080-195">Entity</span></span> |
| --- | --- |
| <span data-ttu-id="47080-196">空欄のトランザクションから移動</span><span class="sxs-lookup"><span data-stu-id="47080-196">Leave Bank Transaction</span></span> | <span data-ttu-id="47080-197">cdm_leavebanktransaction</span><span class="sxs-lookup"><span data-stu-id="47080-197">cdm_leavebanktransaction</span></span> |
| <span data-ttu-id="47080-198">加入契約から移動</span><span class="sxs-lookup"><span data-stu-id="47080-198">Leave Enrollment</span></span> | <span data-ttu-id="47080-199">cdm_leaveenrollment</span><span class="sxs-lookup"><span data-stu-id="47080-199">cdm_leaveenrollment</span></span> |
| <span data-ttu-id="47080-200">休暇計画</span><span class="sxs-lookup"><span data-stu-id="47080-200">Leave Plan</span></span> | <span data-ttu-id="47080-201">cdm_leaveplan</span><span class="sxs-lookup"><span data-stu-id="47080-201">cdm_leaveplan</span></span> |
| <span data-ttu-id="47080-202">休暇申請</span><span class="sxs-lookup"><span data-stu-id="47080-202">Leave Request</span></span> | <span data-ttu-id="47080-203">cdm_leaverequest</span><span class="sxs-lookup"><span data-stu-id="47080-203">cdm_leaverequest</span></span> |
| <span data-ttu-id="47080-204">休暇申請詳細情報</span><span class="sxs-lookup"><span data-stu-id="47080-204">Leave Request Detail</span></span> | <span data-ttu-id="47080-205">cdm_leaverequestdetail</span><span class="sxs-lookup"><span data-stu-id="47080-205">cdm_leaverequestdetail</span></span> |
| <span data-ttu-id="47080-206">休暇タイプ</span><span class="sxs-lookup"><span data-stu-id="47080-206">Leave Type</span></span> | <span data-ttu-id="47080-207">cdm_leavetype</span><span class="sxs-lookup"><span data-stu-id="47080-207">cdm_leavetype</span></span> |
| <span data-ttu-id="47080-208">休暇タイプの理由コード</span><span class="sxs-lookup"><span data-stu-id="47080-208">Leave Type Reason Code</span></span> | <span data-ttu-id="47080-209">cdm_leavetypereasoncode</span><span class="sxs-lookup"><span data-stu-id="47080-209">cdm_leavetypereasoncode</span></span> |

## <a name="payroll-entities"></a><span data-ttu-id="47080-210">給与エンティティ</span><span class="sxs-lookup"><span data-stu-id="47080-210">Payroll entities</span></span>

| <span data-ttu-id="47080-211">氏名</span><span class="sxs-lookup"><span data-stu-id="47080-211">Name</span></span> | <span data-ttu-id="47080-212">エンティティ</span><span class="sxs-lookup"><span data-stu-id="47080-212">Entity</span></span> |
| --- | --- |
| <span data-ttu-id="47080-213">支払サイクル</span><span class="sxs-lookup"><span data-stu-id="47080-213">Pay Cycle</span></span> | <span data-ttu-id="47080-214">cdm_paycycle</span><span class="sxs-lookup"><span data-stu-id="47080-214">cdm_paycycle</span></span> |
| <span data-ttu-id="47080-215">支払期間</span><span class="sxs-lookup"><span data-stu-id="47080-215">Pay Period</span></span> | <span data-ttu-id="47080-216">cdm_payperiod</span><span class="sxs-lookup"><span data-stu-id="47080-216">cdm_payperiod</span></span> |
| <span data-ttu-id="47080-217">給与所得コード</span><span class="sxs-lookup"><span data-stu-id="47080-217">Payroll Earning Code</span></span> | <span data-ttu-id="47080-218">cdm_payrollearningcode</span><span class="sxs-lookup"><span data-stu-id="47080-218">cdm_payrollearningcode</span></span> |
| <span data-ttu-id="47080-219">銀行口座支出</span><span class="sxs-lookup"><span data-stu-id="47080-219">Bank Account Disbursement</span></span> | <span data-ttu-id="47080-220">cdm_bankaccountdisbursement</span><span class="sxs-lookup"><span data-stu-id="47080-220">cdm_bankaccountdisbursement</span></span> |
| <span data-ttu-id="47080-221">税地域</span><span class="sxs-lookup"><span data-stu-id="47080-221">Tax Region</span></span> | <span data-ttu-id="47080-222">cdm_taxregion</span><span class="sxs-lookup"><span data-stu-id="47080-222">cdm_taxregion</span></span> |

## <a name="worker-entities"></a><span data-ttu-id="47080-223">作業者エンティティ</span><span class="sxs-lookup"><span data-stu-id="47080-223">Worker entities</span></span>

| <span data-ttu-id="47080-224">氏名</span><span class="sxs-lookup"><span data-stu-id="47080-224">Name</span></span> | <span data-ttu-id="47080-225">エンティティ</span><span class="sxs-lookup"><span data-stu-id="47080-225">Entity</span></span> |
| --- | --- |
| <span data-ttu-id="47080-226">ワーカー</span><span class="sxs-lookup"><span data-stu-id="47080-226">Worker</span></span> | <span data-ttu-id="47080-227">cdm_worker</span><span class="sxs-lookup"><span data-stu-id="47080-227">cdm_worker</span></span> |
| <span data-ttu-id="47080-228">ワーカーの住所</span><span class="sxs-lookup"><span data-stu-id="47080-228">Worker Address</span></span> | <span data-ttu-id="47080-229">cdm_workeraddress</span><span class="sxs-lookup"><span data-stu-id="47080-229">cdm_workeraddress</span></span> |
| <span data-ttu-id="47080-230">ワーカーの個人情報詳細</span><span class="sxs-lookup"><span data-stu-id="47080-230">Worker Personal Detail</span></span> | <span data-ttu-id="47080-231">cdm_workerpersonaldetail</span><span class="sxs-lookup"><span data-stu-id="47080-231">cdm_workerpersonaldetail</span></span> |
| <span data-ttu-id="47080-232">ワーカーの個人識別番号</span><span class="sxs-lookup"><span data-stu-id="47080-232">Worker Person Identification Number</span></span> | <span data-ttu-id="47080-233">cdm_workerpersonidentificationnumber</span><span class="sxs-lookup"><span data-stu-id="47080-233">cdm_workerpersonidentificationnumber</span></span> |
| <span data-ttu-id="47080-234">作業者の ID タイプ</span><span class="sxs-lookup"><span data-stu-id="47080-234">Worker Person Identification Type</span></span> | <span data-ttu-id="47080-235">cdm_workerpersonidentificationtype</span><span class="sxs-lookup"><span data-stu-id="47080-235">cdm_workerpersonidentificationtype</span></span> |
| <span data-ttu-id="47080-236">作業カレンダー</span><span class="sxs-lookup"><span data-stu-id="47080-236">Work Calendar</span></span> | <span data-ttu-id="47080-237">cdm_workcalendar</span><span class="sxs-lookup"><span data-stu-id="47080-237">cdm_workcalendar</span></span> |
| <span data-ttu-id="47080-238">作業カレンダー日</span><span class="sxs-lookup"><span data-stu-id="47080-238">Work Calendar Day</span></span> | <span data-ttu-id="47080-239">cdm_workcalendarday</span><span class="sxs-lookup"><span data-stu-id="47080-239">cdm_workcalendarday</span></span> |
| <span data-ttu-id="47080-240">作業カレンダーの休日</span><span class="sxs-lookup"><span data-stu-id="47080-240">Work Calendar Holiday</span></span> |<span data-ttu-id="47080-241">cdm_workcalendarholiday</span><span class="sxs-lookup"><span data-stu-id="47080-241">cdm_workcalendarholiday</span></span> |
| <span data-ttu-id="47080-242">作業カレンダーの休日行</span><span class="sxs-lookup"><span data-stu-id="47080-242">Work Calendar Holiday Line</span></span> | <span data-ttu-id="47080-243">cdm_workcalendarholidayline</span><span class="sxs-lookup"><span data-stu-id="47080-243">cdm_workcalendarholidayline</span></span> |
| <span data-ttu-id="47080-244">作業カレンダー時間間隔</span><span class="sxs-lookup"><span data-stu-id="47080-244">Work Calendar Time Interval</span></span> | <span data-ttu-id="47080-245">cdm_workcalendartimeinterval (個人定義フィールドサポートは有効になっていません)</span><span class="sxs-lookup"><span data-stu-id="47080-245">cdm_workcalendartimeinterval (Not enabled for custom field support)</span></span> |
| <span data-ttu-id="47080-246">ワーカーの銀行口座</span><span class="sxs-lookup"><span data-stu-id="47080-246">Worker Bank Account</span></span> | <span data-ttu-id="47080-247">cdm_workerbankaccount</span><span class="sxs-lookup"><span data-stu-id="47080-247">cdm_workerbankaccount</span></span> |

## <a name="worker-setup-entities"></a><span data-ttu-id="47080-248">ワーカーの設定エンティティ</span><span class="sxs-lookup"><span data-stu-id="47080-248">Worker setup entities</span></span>

| <span data-ttu-id="47080-249">氏名</span><span class="sxs-lookup"><span data-stu-id="47080-249">Name</span></span> | <span data-ttu-id="47080-250">エンティティ</span><span class="sxs-lookup"><span data-stu-id="47080-250">Entity</span></span> |
| --- | --- |
| <span data-ttu-id="47080-251">退役軍人状態</span><span class="sxs-lookup"><span data-stu-id="47080-251">Veteran Status</span></span> | <span data-ttu-id="47080-252">cdm_veteranstatus</span><span class="sxs-lookup"><span data-stu-id="47080-252">cdm_veteranstatus</span></span> |
| <span data-ttu-id="47080-253">出身民族</span><span class="sxs-lookup"><span data-stu-id="47080-253">Ethnic Origin</span></span> | <span data-ttu-id="47080-254">cdm_ethnicorigin</span><span class="sxs-lookup"><span data-stu-id="47080-254">cdm_ethnicorigin</span></span> |
| <span data-ttu-id="47080-255">理由コード</span><span class="sxs-lookup"><span data-stu-id="47080-255">Reason Code</span></span> | <span data-ttu-id="47080-256">cdm_reasoncode</span><span class="sxs-lookup"><span data-stu-id="47080-256">cdm_reasoncode</span></span> |
| <span data-ttu-id="47080-257">個人識別発行代理店</span><span class="sxs-lookup"><span data-stu-id="47080-257">Person Identification Issuing Agency</span></span> | <span data-ttu-id="47080-258">cdm_personidentificationissuingagency</span><span class="sxs-lookup"><span data-stu-id="47080-258">cdm_personidentificationissuingagency</span></span> |

## <a name="competency-entities"></a><span data-ttu-id="47080-259">コンピテンシー エンティティ</span><span class="sxs-lookup"><span data-stu-id="47080-259">Competency entities</span></span>

| <span data-ttu-id="47080-260">氏名</span><span class="sxs-lookup"><span data-stu-id="47080-260">Name</span></span> | <span data-ttu-id="47080-261">エンティティ</span><span class="sxs-lookup"><span data-stu-id="47080-261">Entity</span></span> |
| --- | --- |
| <span data-ttu-id="47080-262">スキルの種類</span><span class="sxs-lookup"><span data-stu-id="47080-262">Skill Type</span></span> | <span data-ttu-id="47080-263">cdm_skilltype</span><span class="sxs-lookup"><span data-stu-id="47080-263">cdm_skilltype</span></span> |

## <a name="entity-relationship-models"></a><span data-ttu-id="47080-264">エンティティ関係モデル</span><span class="sxs-lookup"><span data-stu-id="47080-264">Entity relationship models</span></span>

### <a name="worker"></a><span data-ttu-id="47080-265">ワーカー</span><span class="sxs-lookup"><span data-stu-id="47080-265">Worker</span></span>

![ワーカー](./media/HCMCommon-worker-entity-diagram.png)

### <a name="job-and-job-position"></a><span data-ttu-id="47080-267">職務および職位</span><span class="sxs-lookup"><span data-stu-id="47080-267">Job and Job Position</span></span>

![職務および職位](./media/HCMCommon-job-and-job-position-entity-diagram.png)

### <a name="benefits"></a><span data-ttu-id="47080-269">福利厚生</span><span class="sxs-lookup"><span data-stu-id="47080-269">Benefits</span></span>

![福利厚生](./media/HCMCommon-benefits-entity-diagram.png)

### <a name="compensation"></a><span data-ttu-id="47080-271">報酬</span><span class="sxs-lookup"><span data-stu-id="47080-271">Compensation</span></span>

![報酬](./media/HCMCommon-compensation-entity-diagram.png)

### <a name="leave"></a><span data-ttu-id="47080-273">離脱</span><span class="sxs-lookup"><span data-stu-id="47080-273">Leave</span></span>

![離脱](./media/HCMCommon-leave-entity-diagram.png)

### <a name="work-calendar"></a><span data-ttu-id="47080-275">作業カレンダー</span><span class="sxs-lookup"><span data-stu-id="47080-275">Work Calendar</span></span>

![作業カレンダー](./media/HCMCommon-work-calendar-entity-diagram.png)

## <a name="see-also"></a><span data-ttu-id="47080-277">参照</span><span class="sxs-lookup"><span data-stu-id="47080-277">See also</span></span>

[<span data-ttu-id="47080-278">データ統合テクノロジの選択</span><span class="sxs-lookup"><span data-stu-id="47080-278">Choose a data integration technology</span></span>](hr-admin-integration-choose-technology.md)</br>
[<span data-ttu-id="47080-279">Common Data Service 統合のコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="47080-279">Configure Common Data Service integration</span></span>](hr-admin-integration-common-data-service.md)