---
title: Common Data Service の Core HR エンティティ
description: Core HR は、Common Data Service を使用して、拡張性シナリオおよび統合シナリオを有効にします。
author: andreabichsel
manager: AnnBe
ms.date: 11/04/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: IT Pro
ms.reviewer: anbichse
ms.search.scope: Talent
ms.search.region: Global
ms.search.industry: ''
ms.author: anbichse
ms.search.validFrom: 2018-08-11
ms.dyn365.ops.version: ''
ms.openlocfilehash: 6adbd3966fc3aedd0eab83cd8c4714860d6a0e7e
ms.sourcegitcommit: e895b3bbe309f4043d9aaa2a257f0c6e5698923b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/06/2019
ms.locfileid: "2899449"
---
# <a name="core-hr-entities-in-common-data-service"></a><span data-ttu-id="f0c36-103">Common Data Service の Core HR エンティティ</span><span class="sxs-lookup"><span data-stu-id="f0c36-103">Core HR entities in Common Data Service</span></span>

<span data-ttu-id="f0c36-104">Core HR は、Common Data Service を使用して、拡張性シナリオおよび統合シナリオを有効にします。</span><span class="sxs-lookup"><span data-stu-id="f0c36-104">Core HR uses Common Data Service to enable extensibility and integration scenarios.</span></span>

<span data-ttu-id="f0c36-105">Common Data Service の詳細については、[Common Data Service とは何か](https://docs.microsoft.com/powerapps/maker/common-data-service/data-platform-intro)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="f0c36-105">For more information about Common Data Service, see [What is Common Data Service](https://docs.microsoft.com/powerapps/maker/common-data-service/data-platform-intro).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="f0c36-106">Common Data Service の以前のリリース (1.0) は、使用できなくなります。</span><span class="sxs-lookup"><span data-stu-id="f0c36-106">The previous release of the Common Data Service (1.0) is being discontinued.</span></span> <span data-ttu-id="f0c36-107">2019 年 4 月 15 日、Core HR および Common Data Service (1.0) 間の統合がオフになります。</span><span class="sxs-lookup"><span data-stu-id="f0c36-107">On April 15th, 2019 the integration between Core HR and the Common Data Service (1.0) will be turned off.</span></span> <span data-ttu-id="f0c36-108">アップグレードの詳細については、[Common Data Service へのアップグレード](https://docs.microsoft.com/common-data-service/upgradecds/introduction-upgrade-cds)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="f0c36-108">For more information about upgrading, see [Upgrade to Common Data Service](https://docs.microsoft.com/common-data-service/upgradecds/introduction-upgrade-cds).</span></span>

<span data-ttu-id="f0c36-109">次の Core HR エンティティは、Common Data Service で使用できます。</span><span class="sxs-lookup"><span data-stu-id="f0c36-109">The following Core HR entities are available in Common Data Service.</span></span>

## <a name="benefit-entities"></a><span data-ttu-id="f0c36-110">Benefit エンティティ</span><span class="sxs-lookup"><span data-stu-id="f0c36-110">Benefit entities</span></span>

| <span data-ttu-id="f0c36-111">氏名</span><span class="sxs-lookup"><span data-stu-id="f0c36-111">Name</span></span> | <span data-ttu-id="f0c36-112">エンティティ</span><span class="sxs-lookup"><span data-stu-id="f0c36-112">Entity</span></span> |
| --- | --- |
| <span data-ttu-id="f0c36-113">給付金計算頻度</span><span class="sxs-lookup"><span data-stu-id="f0c36-113">Benefit Calculation Frequency</span></span> | <span data-ttu-id="f0c36-114">cdm_benefitcalculationfrequency</span><span class="sxs-lookup"><span data-stu-id="f0c36-114">cdm_benefitcalculationfrequency</span></span> |
| <span data-ttu-id="f0c36-115">ベネフィット計算頻度支払期間</span><span class="sxs-lookup"><span data-stu-id="f0c36-115">Benefit Calculation Frequency Pay Period</span></span> | <span data-ttu-id="f0c36-116">cdm_benefitcalculationfrequencypayperiod</span><span class="sxs-lookup"><span data-stu-id="f0c36-116">cdm_benefitcalculationfrequencypayperiod</span></span> |
| <span data-ttu-id="f0c36-117">ベネフィット計算レート</span><span class="sxs-lookup"><span data-stu-id="f0c36-117">Benefit Calculation Rate</span></span> | <span data-ttu-id="f0c36-118">cdm_benefitcalculationrate</span><span class="sxs-lookup"><span data-stu-id="f0c36-118">cdm_benefitcalculationrate</span></span> |
| <span data-ttu-id="f0c36-119">ベネフィット計算レートの詳細</span><span class="sxs-lookup"><span data-stu-id="f0c36-119">Benefit Calculation Rate Detail</span></span> | <span data-ttu-id="f0c36-120">cdm_benefitcalculationratedetail</span><span class="sxs-lookup"><span data-stu-id="f0c36-120">cdm_benefitcalculationratedetail</span></span> |
| <span data-ttu-id="f0c36-121">ベネフィット オプション</span><span class="sxs-lookup"><span data-stu-id="f0c36-121">Benefit Option</span></span> | <span data-ttu-id="f0c36-122">cdm_benefitoption</span><span class="sxs-lookup"><span data-stu-id="f0c36-122">cdm_benefitoption</span></span> |
| <span data-ttu-id="f0c36-123">給付金計画</span><span class="sxs-lookup"><span data-stu-id="f0c36-123">Benefit Plan</span></span> | <span data-ttu-id="f0c36-124">cdm_benefitplan (ユーザー定義サポートは有効になっていません)</span><span class="sxs-lookup"><span data-stu-id="f0c36-124">cdm_benefitplan (Not enabled for custom field support)</span></span> |
| <span data-ttu-id="f0c36-125">給付金タイプ</span><span class="sxs-lookup"><span data-stu-id="f0c36-125">Benefit Type</span></span> | <span data-ttu-id="f0c36-126">cdm_benefittype</span><span class="sxs-lookup"><span data-stu-id="f0c36-126">cdm_benefittype</span></span> |

## <a name="business-process-tasks-entities"></a><span data-ttu-id="f0c36-127">ビジネス プロセス タスク エンティティ</span><span class="sxs-lookup"><span data-stu-id="f0c36-127">Business process tasks entities</span></span>

| <span data-ttu-id="f0c36-128">氏名</span><span class="sxs-lookup"><span data-stu-id="f0c36-128">Name</span></span> | <span data-ttu-id="f0c36-129">エンティティ</span><span class="sxs-lookup"><span data-stu-id="f0c36-129">Entity</span></span> |
| --- | --- |
| <span data-ttu-id="f0c36-130">業務プロセス カレンダー</span><span class="sxs-lookup"><span data-stu-id="f0c36-130">Business Process Calendar</span></span> | <span data-ttu-id="f0c36-131">cdm_businessprocesscalendar</span><span class="sxs-lookup"><span data-stu-id="f0c36-131">cdm_businessprocesscalendar</span></span> |
| <span data-ttu-id="f0c36-132">業務プロセス グループの割り当て</span><span class="sxs-lookup"><span data-stu-id="f0c36-132">Business Process Group Assignment</span></span> | <span data-ttu-id="f0c36-133">cdm_businessprocessgroupassignment</span><span class="sxs-lookup"><span data-stu-id="f0c36-133">cdm_businessprocessgroupassignment</span></span> |
| <span data-ttu-id="f0c36-134">業務プロセス ライブラリ タスク グループ</span><span class="sxs-lookup"><span data-stu-id="f0c36-134">Business Process Library Task Group</span></span> | <span data-ttu-id="f0c36-135">cdm_businessprocesslibrarytaskgroup</span><span class="sxs-lookup"><span data-stu-id="f0c36-135">cdm_businessprocesslibrarytaskgroup</span></span> |
| <span data-ttu-id="f0c36-136">業務プロセス ステージ</span><span class="sxs-lookup"><span data-stu-id="f0c36-136">Business Process Stage</span></span> | <span data-ttu-id="f0c36-137">cdm_businessprocessstage</span><span class="sxs-lookup"><span data-stu-id="f0c36-137">cdm_businessprocessstage</span></span> |
| <span data-ttu-id="f0c36-138">チェックリストのテンプレート ヘッダー</span><span class="sxs-lookup"><span data-stu-id="f0c36-138">Checklist Template Header</span></span> | <span data-ttu-id="f0c36-139">cdm_businessprocesstemplateheader</span><span class="sxs-lookup"><span data-stu-id="f0c36-139">cdm_businessprocesstemplateheader</span></span> |
| <span data-ttu-id="f0c36-140">チェックリストのテンプレート タスク</span><span class="sxs-lookup"><span data-stu-id="f0c36-140">Checklist Template Task</span></span> | <span data-ttu-id="f0c36-141">cdm_businessprocesstemplatetask</span><span class="sxs-lookup"><span data-stu-id="f0c36-141">cdm_businessprocesstemplatetask</span></span> |

## <a name="compensation-entities"></a><span data-ttu-id="f0c36-142">報酬エンティティ</span><span class="sxs-lookup"><span data-stu-id="f0c36-142">Compensation entities</span></span>

| <span data-ttu-id="f0c36-143">氏名</span><span class="sxs-lookup"><span data-stu-id="f0c36-143">Name</span></span> | <span data-ttu-id="f0c36-144">エンティティ</span><span class="sxs-lookup"><span data-stu-id="f0c36-144">Entity</span></span> |
| --- | --- |
| <span data-ttu-id="f0c36-145">報酬固定計画</span><span class="sxs-lookup"><span data-stu-id="f0c36-145">Compensation Fixed Plan</span></span> | <span data-ttu-id="f0c36-146">cdm_compensationfixedplan</span><span class="sxs-lookup"><span data-stu-id="f0c36-146">cdm_compensationfixedplan</span></span> |
| <span data-ttu-id="f0c36-147">報酬グリッド</span><span class="sxs-lookup"><span data-stu-id="f0c36-147">Compensation Grid</span></span> | <span data-ttu-id="f0c36-148">cdm_compensationgrid</span><span class="sxs-lookup"><span data-stu-id="f0c36-148">cdm_compensationgrid</span></span> |
| <span data-ttu-id="f0c36-149">報酬レベル</span><span class="sxs-lookup"><span data-stu-id="f0c36-149">Compensation Level</span></span> | <span data-ttu-id="f0c36-150">cdm_compensationlevel</span><span class="sxs-lookup"><span data-stu-id="f0c36-150">cdm_compensationlevel</span></span> |
| <span data-ttu-id="f0c36-151">報酬支払頻度</span><span class="sxs-lookup"><span data-stu-id="f0c36-151">Compensation Pay Frequency</span></span> | <span data-ttu-id="f0c36-152">cdm_compensationpayfrequency</span><span class="sxs-lookup"><span data-stu-id="f0c36-152">cdm_compensationpayfrequency</span></span> |
| <span data-ttu-id="f0c36-153">報酬基準点設定</span><span class="sxs-lookup"><span data-stu-id="f0c36-153">Compensation Reference Point Setup</span></span> | <span data-ttu-id="f0c36-154">cdm_compensationreferencepointsetup</span><span class="sxs-lookup"><span data-stu-id="f0c36-154">cdm_compensationreferencepointsetup</span></span> |
| <span data-ttu-id="f0c36-155">報酬基準点設定ライン</span><span class="sxs-lookup"><span data-stu-id="f0c36-155">Compensation Reference Point Setup Line</span></span> | <span data-ttu-id="f0c36-156">cdm_compensationreferencepointsetupline</span><span class="sxs-lookup"><span data-stu-id="f0c36-156">cdm_compensationreferencepointsetupline</span></span> |
| <span data-ttu-id="f0c36-157">報酬地域</span><span class="sxs-lookup"><span data-stu-id="f0c36-157">Compensation Region</span></span> | <span data-ttu-id="f0c36-158">cdm_compensationregion</span><span class="sxs-lookup"><span data-stu-id="f0c36-158">cdm_compensationregion</span></span> |
| <span data-ttu-id="f0c36-159">報酬構成</span><span class="sxs-lookup"><span data-stu-id="f0c36-159">Compensation Structure</span></span> | <span data-ttu-id="f0c36-160">cdm_compensationstructure</span><span class="sxs-lookup"><span data-stu-id="f0c36-160">cdm_compensationstructure</span></span> |
| <span data-ttu-id="f0c36-161">報酬変動プラン</span><span class="sxs-lookup"><span data-stu-id="f0c36-161">Compensation Variable Plan</span></span> | <span data-ttu-id="f0c36-162">cdm_compensationvariableplan</span><span class="sxs-lookup"><span data-stu-id="f0c36-162">cdm_compensationvariableplan</span></span> |
| <span data-ttu-id="f0c36-163">報酬変動プラン レベル</span><span class="sxs-lookup"><span data-stu-id="f0c36-163">Compensation Variable Plan Level</span></span> | <span data-ttu-id="f0c36-164">cdm_compensationvariableplanlevel</span><span class="sxs-lookup"><span data-stu-id="f0c36-164">cdm_compensationvariableplanlevel</span></span> |
| <span data-ttu-id="f0c36-165">報酬変動プラン タイプ</span><span class="sxs-lookup"><span data-stu-id="f0c36-165">Compensation Variable Plan Type</span></span> | <span data-ttu-id="f0c36-166">cdm_compensationvariableplantype</span><span class="sxs-lookup"><span data-stu-id="f0c36-166">cdm_compensationvariableplantype</span></span> |
| <span data-ttu-id="f0c36-167">固定報酬イベント</span><span class="sxs-lookup"><span data-stu-id="f0c36-167">Fixed Compensation Event</span></span> | <span data-ttu-id="f0c36-168">cdm_fixedcompensationevent</span><span class="sxs-lookup"><span data-stu-id="f0c36-168">cdm_fixedcompensationevent</span></span> |
| <span data-ttu-id="f0c36-169">給付ルール</span><span class="sxs-lookup"><span data-stu-id="f0c36-169">Vesting Rule</span></span> | <span data-ttu-id="f0c36-170">cdm_vestingrule</span><span class="sxs-lookup"><span data-stu-id="f0c36-170">cdm_vestingrule</span></span> |
| <span data-ttu-id="f0c36-171">ワーカー固定報酬</span><span class="sxs-lookup"><span data-stu-id="f0c36-171">Worker Fixed Compensation</span></span> | <span data-ttu-id="f0c36-172">cdm_workerfixedcompensation</span><span class="sxs-lookup"><span data-stu-id="f0c36-172">cdm_workerfixedcompensation</span></span> |

## <a name="organization-entities"></a><span data-ttu-id="f0c36-173">組織エンティティ</span><span class="sxs-lookup"><span data-stu-id="f0c36-173">Organization entities</span></span>

| <span data-ttu-id="f0c36-174">氏名</span><span class="sxs-lookup"><span data-stu-id="f0c36-174">Name</span></span> | <span data-ttu-id="f0c36-175">エンティティ</span><span class="sxs-lookup"><span data-stu-id="f0c36-175">Entity</span></span> |
| --- | --- |
| <span data-ttu-id="f0c36-176">部門</span><span class="sxs-lookup"><span data-stu-id="f0c36-176">Department</span></span> | <span data-ttu-id="f0c36-177">cdm_department</span><span class="sxs-lookup"><span data-stu-id="f0c36-177">cdm_department</span></span> |
| <span data-ttu-id="f0c36-178">雇用</span><span class="sxs-lookup"><span data-stu-id="f0c36-178">Employment</span></span> | <span data-ttu-id="f0c36-179">cdm_employment</span><span class="sxs-lookup"><span data-stu-id="f0c36-179">cdm_employment</span></span> |
| <span data-ttu-id="f0c36-180">法人</span><span class="sxs-lookup"><span data-stu-id="f0c36-180">Company</span></span> | <span data-ttu-id="f0c36-181">cdm_company</span><span class="sxs-lookup"><span data-stu-id="f0c36-181">cdm_company</span></span> |
| <span data-ttu-id="f0c36-182">ジョブ</span><span class="sxs-lookup"><span data-stu-id="f0c36-182">Job</span></span> | <span data-ttu-id="f0c36-183">cdm_job</span><span class="sxs-lookup"><span data-stu-id="f0c36-183">cdm_job</span></span> |
| <span data-ttu-id="f0c36-184">職務権限</span><span class="sxs-lookup"><span data-stu-id="f0c36-184">Job Function</span></span> | <span data-ttu-id="f0c36-185">cdm_jobfunction</span><span class="sxs-lookup"><span data-stu-id="f0c36-185">cdm_jobfunction</span></span> |
| <span data-ttu-id="f0c36-186">職位</span><span class="sxs-lookup"><span data-stu-id="f0c36-186">Job Position</span></span> | <span data-ttu-id="f0c36-187">cdm_jobposition</span><span class="sxs-lookup"><span data-stu-id="f0c36-187">cdm_jobposition</span></span> |
| <span data-ttu-id="f0c36-188">職位タイプ</span><span class="sxs-lookup"><span data-stu-id="f0c36-188">Position Type</span></span> | <span data-ttu-id="f0c36-189">cdm_positiontype</span><span class="sxs-lookup"><span data-stu-id="f0c36-189">cdm_positiontype</span></span> |
| <span data-ttu-id="f0c36-190">ワーカー割り当ての配置</span><span class="sxs-lookup"><span data-stu-id="f0c36-190">Position Worker Assignment</span></span> | <span data-ttu-id="f0c36-191">cdm_positionworkerassignmentmap</span><span class="sxs-lookup"><span data-stu-id="f0c36-191">cdm_positionworkerassignmentmap</span></span> |
| <span data-ttu-id="f0c36-192">職務タイプ</span><span class="sxs-lookup"><span data-stu-id="f0c36-192">Job Type</span></span> | <span data-ttu-id="f0c36-193">cdm_jobtype</span><span class="sxs-lookup"><span data-stu-id="f0c36-193">cdm_jobtype</span></span> |
| <span data-ttu-id="f0c36-194">言語</span><span class="sxs-lookup"><span data-stu-id="f0c36-194">Language</span></span> | <span data-ttu-id="f0c36-195">cdm_language</span><span class="sxs-lookup"><span data-stu-id="f0c36-195">cdm_language</span></span> |

## <a name="leave-and-absence-entities"></a><span data-ttu-id="f0c36-196">休暇エンティティ</span><span class="sxs-lookup"><span data-stu-id="f0c36-196">Leave and absence entities</span></span>

| <span data-ttu-id="f0c36-197">氏名</span><span class="sxs-lookup"><span data-stu-id="f0c36-197">Name</span></span> | <span data-ttu-id="f0c36-198">エンティティ</span><span class="sxs-lookup"><span data-stu-id="f0c36-198">Entity</span></span> |
| --- | --- |
| <span data-ttu-id="f0c36-199">空欄のトランザクションから移動</span><span class="sxs-lookup"><span data-stu-id="f0c36-199">Leave Bank Transaction</span></span> | <span data-ttu-id="f0c36-200">cdm_leavebanktransaction</span><span class="sxs-lookup"><span data-stu-id="f0c36-200">cdm_leavebanktransaction</span></span> |
| <span data-ttu-id="f0c36-201">加入契約から移動</span><span class="sxs-lookup"><span data-stu-id="f0c36-201">Leave Enrollment</span></span> | <span data-ttu-id="f0c36-202">cdm_leaveenrollment</span><span class="sxs-lookup"><span data-stu-id="f0c36-202">cdm_leaveenrollment</span></span> |
| <span data-ttu-id="f0c36-203">休暇計画</span><span class="sxs-lookup"><span data-stu-id="f0c36-203">Leave Plan</span></span> | <span data-ttu-id="f0c36-204">cdm_leaveplan</span><span class="sxs-lookup"><span data-stu-id="f0c36-204">cdm_leaveplan</span></span> |
| <span data-ttu-id="f0c36-205">休暇申請</span><span class="sxs-lookup"><span data-stu-id="f0c36-205">Leave Request</span></span> | <span data-ttu-id="f0c36-206">cdm_leaverequest</span><span class="sxs-lookup"><span data-stu-id="f0c36-206">cdm_leaverequest</span></span> |
| <span data-ttu-id="f0c36-207">要求の詳細から移動</span><span class="sxs-lookup"><span data-stu-id="f0c36-207">Leave Request Detail</span></span> | <span data-ttu-id="f0c36-208">cdm_leaverequestdetail</span><span class="sxs-lookup"><span data-stu-id="f0c36-208">cdm_leaverequestdetail</span></span> |
| <span data-ttu-id="f0c36-209">休暇タイプ</span><span class="sxs-lookup"><span data-stu-id="f0c36-209">Leave Type</span></span> | <span data-ttu-id="f0c36-210">cdm_leavetype</span><span class="sxs-lookup"><span data-stu-id="f0c36-210">cdm_leavetype</span></span> |
| <span data-ttu-id="f0c36-211">休暇タイプの理由コード</span><span class="sxs-lookup"><span data-stu-id="f0c36-211">Leave Type Reason Code</span></span> | <span data-ttu-id="f0c36-212">cdm_leavetypereasoncode</span><span class="sxs-lookup"><span data-stu-id="f0c36-212">cdm_leavetypereasoncode</span></span> |

## <a name="payroll-entities"></a><span data-ttu-id="f0c36-213">給与エンティティ</span><span class="sxs-lookup"><span data-stu-id="f0c36-213">Payroll entities</span></span>

| <span data-ttu-id="f0c36-214">氏名</span><span class="sxs-lookup"><span data-stu-id="f0c36-214">Name</span></span> | <span data-ttu-id="f0c36-215">エンティティ</span><span class="sxs-lookup"><span data-stu-id="f0c36-215">Entity</span></span> |
| --- | --- |
| <span data-ttu-id="f0c36-216">支払サイクル</span><span class="sxs-lookup"><span data-stu-id="f0c36-216">Pay Cycle</span></span> | <span data-ttu-id="f0c36-217">cdm_paycycle</span><span class="sxs-lookup"><span data-stu-id="f0c36-217">cdm_paycycle</span></span> |
| <span data-ttu-id="f0c36-218">支払期間</span><span class="sxs-lookup"><span data-stu-id="f0c36-218">Pay Period</span></span> | <span data-ttu-id="f0c36-219">cdm_payperiod</span><span class="sxs-lookup"><span data-stu-id="f0c36-219">cdm_payperiod</span></span> |
| <span data-ttu-id="f0c36-220">給与所得コード</span><span class="sxs-lookup"><span data-stu-id="f0c36-220">Payroll Earning Code</span></span> | <span data-ttu-id="f0c36-221">cdm_payrollearningcode</span><span class="sxs-lookup"><span data-stu-id="f0c36-221">cdm_payrollearningcode</span></span> |
| <span data-ttu-id="f0c36-222">銀行口座支出</span><span class="sxs-lookup"><span data-stu-id="f0c36-222">Bank Account Disbursement</span></span> | <span data-ttu-id="f0c36-223">cdm_bankaccountdisbursement</span><span class="sxs-lookup"><span data-stu-id="f0c36-223">cdm_bankaccountdisbursement</span></span> |
| <span data-ttu-id="f0c36-224">税地域</span><span class="sxs-lookup"><span data-stu-id="f0c36-224">Tax Region</span></span> | <span data-ttu-id="f0c36-225">cdm_taxregion</span><span class="sxs-lookup"><span data-stu-id="f0c36-225">cdm_taxregion</span></span> |

## <a name="worker-entities"></a><span data-ttu-id="f0c36-226">作業者エンティティ</span><span class="sxs-lookup"><span data-stu-id="f0c36-226">Worker entities</span></span>

| <span data-ttu-id="f0c36-227">氏名</span><span class="sxs-lookup"><span data-stu-id="f0c36-227">Name</span></span> | <span data-ttu-id="f0c36-228">エンティティ</span><span class="sxs-lookup"><span data-stu-id="f0c36-228">Entity</span></span> |
| --- | --- |
| <span data-ttu-id="f0c36-229">ワーカー</span><span class="sxs-lookup"><span data-stu-id="f0c36-229">Worker</span></span> | <span data-ttu-id="f0c36-230">cdm_worker</span><span class="sxs-lookup"><span data-stu-id="f0c36-230">cdm_worker</span></span> |
| <span data-ttu-id="f0c36-231">ワーカーの住所</span><span class="sxs-lookup"><span data-stu-id="f0c36-231">Worker Address</span></span> | <span data-ttu-id="f0c36-232">cdm_workeraddress</span><span class="sxs-lookup"><span data-stu-id="f0c36-232">cdm_workeraddress</span></span> |
| <span data-ttu-id="f0c36-233">ワーカーの個人情報詳細</span><span class="sxs-lookup"><span data-stu-id="f0c36-233">Worker Personal Detail</span></span> | <span data-ttu-id="f0c36-234">cdm_workerpersonaldetail</span><span class="sxs-lookup"><span data-stu-id="f0c36-234">cdm_workerpersonaldetail</span></span> |
| <span data-ttu-id="f0c36-235">ワーカーの個人識別番号</span><span class="sxs-lookup"><span data-stu-id="f0c36-235">Worker Person Identification Number</span></span> | <span data-ttu-id="f0c36-236">cdm_workerpersonidentificationnumber</span><span class="sxs-lookup"><span data-stu-id="f0c36-236">cdm_workerpersonidentificationnumber</span></span> |
| <span data-ttu-id="f0c36-237">作業者の ID タイプ</span><span class="sxs-lookup"><span data-stu-id="f0c36-237">Worker Person Identification Type</span></span> | <span data-ttu-id="f0c36-238">cdm_workerpersonidentificationtype</span><span class="sxs-lookup"><span data-stu-id="f0c36-238">cdm_workerpersonidentificationtype</span></span> |
| <span data-ttu-id="f0c36-239">作業カレンダー</span><span class="sxs-lookup"><span data-stu-id="f0c36-239">Work Calendar</span></span> | <span data-ttu-id="f0c36-240">cdm_workcalendar</span><span class="sxs-lookup"><span data-stu-id="f0c36-240">cdm_workcalendar</span></span> |
| <span data-ttu-id="f0c36-241">作業カレンダー日</span><span class="sxs-lookup"><span data-stu-id="f0c36-241">Work Calendar Day</span></span> | <span data-ttu-id="f0c36-242">cdm_workcalendarday</span><span class="sxs-lookup"><span data-stu-id="f0c36-242">cdm_workcalendarday</span></span> |
| <span data-ttu-id="f0c36-243">作業カレンダーの休日</span><span class="sxs-lookup"><span data-stu-id="f0c36-243">Work Calendar Holiday</span></span> |<span data-ttu-id="f0c36-244">cdm_workcalendarholiday</span><span class="sxs-lookup"><span data-stu-id="f0c36-244">cdm_workcalendarholiday</span></span> |
| <span data-ttu-id="f0c36-245">作業カレンダーの休日ライン</span><span class="sxs-lookup"><span data-stu-id="f0c36-245">Work Calendar Holiday Line</span></span> | <span data-ttu-id="f0c36-246">cdm_workcalendarholidayline</span><span class="sxs-lookup"><span data-stu-id="f0c36-246">cdm_workcalendarholidayline</span></span> |
| <span data-ttu-id="f0c36-247">作業カレンダーの時間間隔</span><span class="sxs-lookup"><span data-stu-id="f0c36-247">Work Calendar Time Interval</span></span> | <span data-ttu-id="f0c36-248">cdm_workcalendartimeinterval (個人定義フィールドサポートは有効になっていません)</span><span class="sxs-lookup"><span data-stu-id="f0c36-248">cdm_workcalendartimeinterval (Not enabled for custom field support)</span></span> |
| <span data-ttu-id="f0c36-249">ワーカーの銀行口座</span><span class="sxs-lookup"><span data-stu-id="f0c36-249">Worker Bank Account</span></span> | <span data-ttu-id="f0c36-250">cdm_workerbankaccount</span><span class="sxs-lookup"><span data-stu-id="f0c36-250">cdm_workerbankaccount</span></span> |

## <a name="worker-setup-entities"></a><span data-ttu-id="f0c36-251">ワーカーの設定エンティティ</span><span class="sxs-lookup"><span data-stu-id="f0c36-251">Worker setup entities</span></span>

| <span data-ttu-id="f0c36-252">氏名</span><span class="sxs-lookup"><span data-stu-id="f0c36-252">Name</span></span> | <span data-ttu-id="f0c36-253">エンティティ</span><span class="sxs-lookup"><span data-stu-id="f0c36-253">Entity</span></span> |
| --- | --- |
| <span data-ttu-id="f0c36-254">退役軍人状態</span><span class="sxs-lookup"><span data-stu-id="f0c36-254">Veteran Status</span></span> | <span data-ttu-id="f0c36-255">cdm_veteranstatus</span><span class="sxs-lookup"><span data-stu-id="f0c36-255">cdm_veteranstatus</span></span> |
| <span data-ttu-id="f0c36-256">出身民族</span><span class="sxs-lookup"><span data-stu-id="f0c36-256">Ethnic Origin</span></span> | <span data-ttu-id="f0c36-257">cdm_ethnicorigin</span><span class="sxs-lookup"><span data-stu-id="f0c36-257">cdm_ethnicorigin</span></span> |
| <span data-ttu-id="f0c36-258">理由コード</span><span class="sxs-lookup"><span data-stu-id="f0c36-258">Reason Code</span></span> | <span data-ttu-id="f0c36-259">cdm_reasoncode</span><span class="sxs-lookup"><span data-stu-id="f0c36-259">cdm_reasoncode</span></span> |
| <span data-ttu-id="f0c36-260">個人識別発行代理店</span><span class="sxs-lookup"><span data-stu-id="f0c36-260">Person Identification Issuing Agency</span></span> | <span data-ttu-id="f0c36-261">cdm_personidentificationissuingagency</span><span class="sxs-lookup"><span data-stu-id="f0c36-261">cdm_personidentificationissuingagency</span></span> |

## <a name="competency-entities"></a><span data-ttu-id="f0c36-262">コンピテンシー エンティティ</span><span class="sxs-lookup"><span data-stu-id="f0c36-262">Competency entities</span></span>

| <span data-ttu-id="f0c36-263">氏名</span><span class="sxs-lookup"><span data-stu-id="f0c36-263">Name</span></span> | <span data-ttu-id="f0c36-264">エンティティ</span><span class="sxs-lookup"><span data-stu-id="f0c36-264">Entity</span></span> |
| --- | --- |
| <span data-ttu-id="f0c36-265">スキルの種類</span><span class="sxs-lookup"><span data-stu-id="f0c36-265">Skill Type</span></span> | <span data-ttu-id="f0c36-266">cdm_skilltype</span><span class="sxs-lookup"><span data-stu-id="f0c36-266">cdm_skilltype</span></span> |

## <a name="entity-relationship-models"></a><span data-ttu-id="f0c36-267">エンティティ関係モデル</span><span class="sxs-lookup"><span data-stu-id="f0c36-267">Entity relationship models</span></span>

### <a name="worker"></a><span data-ttu-id="f0c36-268">ワーカー</span><span class="sxs-lookup"><span data-stu-id="f0c36-268">Worker</span></span>
![ワーカー](./media/HCMCommon-worker-entity-diagram.png)

### <a name="job-and-job-position"></a><span data-ttu-id="f0c36-270">職務および職位</span><span class="sxs-lookup"><span data-stu-id="f0c36-270">Job and Job Position</span></span>
![職務および職位](./media/HCMCommon-job-and-job-position-entity-diagram.png)

### <a name="benefits"></a><span data-ttu-id="f0c36-272">福利厚生</span><span class="sxs-lookup"><span data-stu-id="f0c36-272">Benefits</span></span>
![福利厚生](./media/HCMCommon-benefits-entity-diagram.png)

### <a name="compensation"></a><span data-ttu-id="f0c36-274">報酬</span><span class="sxs-lookup"><span data-stu-id="f0c36-274">Compensation</span></span>
![報酬](./media/HCMCommon-compensation-entity-diagram.png)

### <a name="leave"></a><span data-ttu-id="f0c36-276">休暇</span><span class="sxs-lookup"><span data-stu-id="f0c36-276">Leave</span></span>
![休暇](./media/HCMCommon-leave-entity-diagram.png)

### <a name="work-calendar"></a><span data-ttu-id="f0c36-278">作業カレンダー</span><span class="sxs-lookup"><span data-stu-id="f0c36-278">Work Calendar</span></span>
![作業カレンダー](./media/HCMCommon-work-calendar-entity-diagram.png)
