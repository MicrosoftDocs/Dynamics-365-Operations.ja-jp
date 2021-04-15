---
title: Dataverse テーブル
description: Microsoft Dynamics 365 Human Resources は、Dataverse を使用して拡張性シナリオおよび統合シナリオを有効にします。
author: andreabichsel
ms.date: 01/25/2021
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: e316cda9b9c5361c0a2837e7ed6c050e76cc39b9
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5793612"
---
# <a name="dataverse-tables"></a><span data-ttu-id="008a1-103">Dataverse テーブル</span><span class="sxs-lookup"><span data-stu-id="008a1-103">Dataverse tables</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="008a1-104">Microsoft Dynamics 365 Human Resources は、Dataverse を使用して拡張性シナリオおよび統合シナリオを有効にします。</span><span class="sxs-lookup"><span data-stu-id="008a1-104">Microsoft Dynamics 365 Human Resources uses Dataverse to enable extensibility and integration scenarios.</span></span>

> [!NOTE]
> <span data-ttu-id="008a1-105">Human Resources エンティティは Dataverse テーブルに対応します。</span><span class="sxs-lookup"><span data-stu-id="008a1-105">Human Resources entities correspond to Dataverse tables.</span></span> <span data-ttu-id="008a1-106">Dataverse (旧 Common Data Service) および用語更新の詳細については、[Microsoft Dataverse とは何ですか?](https://docs.microsoft.com/powerapps/maker/data-platform/data-platform-intro)を参照してください</span><span class="sxs-lookup"><span data-stu-id="008a1-106">For more information about Dataverse (formerly Common Data Service) and terminology updates, see [What is Microsoft Dataverse?](https://docs.microsoft.com/powerapps/maker/data-platform/data-platform-intro)</span></span>

<span data-ttu-id="008a1-107">次の Dataverse テーブルは、Human Resources エンティティで利用できます。</span><span class="sxs-lookup"><span data-stu-id="008a1-107">The following Dataverse tables are available based on Human Resources entities.</span></span>

## <a name="benefit-tables"></a><span data-ttu-id="008a1-108">福利厚生テーブル</span><span class="sxs-lookup"><span data-stu-id="008a1-108">Benefit tables</span></span>

| <span data-ttu-id="008a1-109">氏名</span><span class="sxs-lookup"><span data-stu-id="008a1-109">Name</span></span> | <span data-ttu-id="008a1-110">テーブル</span><span class="sxs-lookup"><span data-stu-id="008a1-110">Table</span></span> |
| --- | --- |
| <span data-ttu-id="008a1-111">給付金計算頻度</span><span class="sxs-lookup"><span data-stu-id="008a1-111">Benefit Calculation Frequency</span></span> | <span data-ttu-id="008a1-112">cdm_benefitcalculationfrequency</span><span class="sxs-lookup"><span data-stu-id="008a1-112">cdm_benefitcalculationfrequency</span></span> |
| <span data-ttu-id="008a1-113">給付金計算頻度支払期間</span><span class="sxs-lookup"><span data-stu-id="008a1-113">Benefit Calculation Frequency Pay Period</span></span> | <span data-ttu-id="008a1-114">cdm_benefitcalculationfrequencypayperiod</span><span class="sxs-lookup"><span data-stu-id="008a1-114">cdm_benefitcalculationfrequencypayperiod</span></span> |
| <span data-ttu-id="008a1-115">給付金計算レート</span><span class="sxs-lookup"><span data-stu-id="008a1-115">Benefit Calculation Rate</span></span> | <span data-ttu-id="008a1-116">cdm_benefitcalculationrate</span><span class="sxs-lookup"><span data-stu-id="008a1-116">cdm_benefitcalculationrate</span></span> |
| <span data-ttu-id="008a1-117">給付金計算レートの詳細</span><span class="sxs-lookup"><span data-stu-id="008a1-117">Benefit Calculation Rate Detail</span></span> | <span data-ttu-id="008a1-118">cdm_benefitcalculationratedetail</span><span class="sxs-lookup"><span data-stu-id="008a1-118">cdm_benefitcalculationratedetail</span></span> |
| <span data-ttu-id="008a1-119">福利厚生オプション</span><span class="sxs-lookup"><span data-stu-id="008a1-119">Benefit Option</span></span> | <span data-ttu-id="008a1-120">cdm_benefitoption</span><span class="sxs-lookup"><span data-stu-id="008a1-120">cdm_benefitoption</span></span> |
| <span data-ttu-id="008a1-121">給付金計画</span><span class="sxs-lookup"><span data-stu-id="008a1-121">Benefit Plan</span></span> | <span data-ttu-id="008a1-122">cdm_benefitplan (カスタム フィールド サポートに対して有効化されていない)</span><span class="sxs-lookup"><span data-stu-id="008a1-122">cdm_benefitplan (Not enabled for custom field support)</span></span> |
| <span data-ttu-id="008a1-123">給付金タイプ</span><span class="sxs-lookup"><span data-stu-id="008a1-123">Benefit Type</span></span> | <span data-ttu-id="008a1-124">cdm_benefittype</span><span class="sxs-lookup"><span data-stu-id="008a1-124">cdm_benefittype</span></span> |

## <a name="business-process-tasks-tables"></a><span data-ttu-id="008a1-125">ビジネス プロセス タスク テーブル</span><span class="sxs-lookup"><span data-stu-id="008a1-125">Business process tasks tables</span></span>

| <span data-ttu-id="008a1-126">氏名</span><span class="sxs-lookup"><span data-stu-id="008a1-126">Name</span></span> | <span data-ttu-id="008a1-127">テーブル</span><span class="sxs-lookup"><span data-stu-id="008a1-127">Table</span></span> |
| --- | --- |
| <span data-ttu-id="008a1-128">業務プロセス カレンダー</span><span class="sxs-lookup"><span data-stu-id="008a1-128">Business Process Calendar</span></span> | <span data-ttu-id="008a1-129">cdm_businessprocesscalendar</span><span class="sxs-lookup"><span data-stu-id="008a1-129">cdm_businessprocesscalendar</span></span> |
| <span data-ttu-id="008a1-130">業務プロセス グループの割り当て</span><span class="sxs-lookup"><span data-stu-id="008a1-130">Business Process Group Assignment</span></span> | <span data-ttu-id="008a1-131">cdm_businessprocessgroupassignment</span><span class="sxs-lookup"><span data-stu-id="008a1-131">cdm_businessprocessgroupassignment</span></span> |
| <span data-ttu-id="008a1-132">業務プロセス ライブラリ タスク グループ</span><span class="sxs-lookup"><span data-stu-id="008a1-132">Business Process Library Task Group</span></span> | <span data-ttu-id="008a1-133">cdm_businessprocesslibrarytaskgroup</span><span class="sxs-lookup"><span data-stu-id="008a1-133">cdm_businessprocesslibrarytaskgroup</span></span> |
| <span data-ttu-id="008a1-134">業務プロセス ステージ</span><span class="sxs-lookup"><span data-stu-id="008a1-134">Business Process Stage</span></span> | <span data-ttu-id="008a1-135">cdm_businessprocessstage</span><span class="sxs-lookup"><span data-stu-id="008a1-135">cdm_businessprocessstage</span></span> |
| <span data-ttu-id="008a1-136">チェックリストのテンプレート ヘッダー</span><span class="sxs-lookup"><span data-stu-id="008a1-136">Checklist Template Header</span></span> | <span data-ttu-id="008a1-137">cdm_businessprocesstemplateheader</span><span class="sxs-lookup"><span data-stu-id="008a1-137">cdm_businessprocesstemplateheader</span></span> |
| <span data-ttu-id="008a1-138">チェックリストのテンプレート タスク</span><span class="sxs-lookup"><span data-stu-id="008a1-138">Checklist Template Task</span></span> | <span data-ttu-id="008a1-139">cdm_businessprocesstemplatetask</span><span class="sxs-lookup"><span data-stu-id="008a1-139">cdm_businessprocesstemplatetask</span></span> |

## <a name="compensation-tables"></a><span data-ttu-id="008a1-140">報酬テーブル</span><span class="sxs-lookup"><span data-stu-id="008a1-140">Compensation tables</span></span>

| <span data-ttu-id="008a1-141">氏名</span><span class="sxs-lookup"><span data-stu-id="008a1-141">Name</span></span> | <span data-ttu-id="008a1-142">テーブル</span><span class="sxs-lookup"><span data-stu-id="008a1-142">Table</span></span> |
| --- | --- |
| <span data-ttu-id="008a1-143">固定報酬プラン</span><span class="sxs-lookup"><span data-stu-id="008a1-143">Compensation Fixed Plan</span></span> | <span data-ttu-id="008a1-144">cdm_compensationfixedplan</span><span class="sxs-lookup"><span data-stu-id="008a1-144">cdm_compensationfixedplan</span></span> |
| <span data-ttu-id="008a1-145">報酬グリッド</span><span class="sxs-lookup"><span data-stu-id="008a1-145">Compensation Grid</span></span> | <span data-ttu-id="008a1-146">cdm_compensationgrid</span><span class="sxs-lookup"><span data-stu-id="008a1-146">cdm_compensationgrid</span></span> |
| <span data-ttu-id="008a1-147">報酬レベル</span><span class="sxs-lookup"><span data-stu-id="008a1-147">Compensation Level</span></span> | <span data-ttu-id="008a1-148">cdm_compensationlevel</span><span class="sxs-lookup"><span data-stu-id="008a1-148">cdm_compensationlevel</span></span> |
| <span data-ttu-id="008a1-149">報酬支払頻度</span><span class="sxs-lookup"><span data-stu-id="008a1-149">Compensation Pay Frequency</span></span> | <span data-ttu-id="008a1-150">cdm_compensationpayfrequency</span><span class="sxs-lookup"><span data-stu-id="008a1-150">cdm_compensationpayfrequency</span></span> |
| <span data-ttu-id="008a1-151">報酬基準点設定</span><span class="sxs-lookup"><span data-stu-id="008a1-151">Compensation Reference Point Setup</span></span> | <span data-ttu-id="008a1-152">cdm_compensationreferencepointsetup</span><span class="sxs-lookup"><span data-stu-id="008a1-152">cdm_compensationreferencepointsetup</span></span> |
| <span data-ttu-id="008a1-153">報酬基準点設定ライン</span><span class="sxs-lookup"><span data-stu-id="008a1-153">Compensation Reference Point Setup Line</span></span> | <span data-ttu-id="008a1-154">cdm_compensationreferencepointsetupline</span><span class="sxs-lookup"><span data-stu-id="008a1-154">cdm_compensationreferencepointsetupline</span></span> |
| <span data-ttu-id="008a1-155">報酬地域</span><span class="sxs-lookup"><span data-stu-id="008a1-155">Compensation Region</span></span> | <span data-ttu-id="008a1-156">cdm_compensationregion</span><span class="sxs-lookup"><span data-stu-id="008a1-156">cdm_compensationregion</span></span> |
| <span data-ttu-id="008a1-157">報酬構造</span><span class="sxs-lookup"><span data-stu-id="008a1-157">Compensation Structure</span></span> | <span data-ttu-id="008a1-158">cdm_compensationstructure</span><span class="sxs-lookup"><span data-stu-id="008a1-158">cdm_compensationstructure</span></span> |
| <span data-ttu-id="008a1-159">報酬変動プラン</span><span class="sxs-lookup"><span data-stu-id="008a1-159">Compensation Variable Plan</span></span> | <span data-ttu-id="008a1-160">cdm_compensationvariableplan</span><span class="sxs-lookup"><span data-stu-id="008a1-160">cdm_compensationvariableplan</span></span> |
| <span data-ttu-id="008a1-161">報酬変動プラン レベル</span><span class="sxs-lookup"><span data-stu-id="008a1-161">Compensation Variable Plan Level</span></span> | <span data-ttu-id="008a1-162">cdm_compensationvariableplanlevel</span><span class="sxs-lookup"><span data-stu-id="008a1-162">cdm_compensationvariableplanlevel</span></span> |
| <span data-ttu-id="008a1-163">報酬変動プラン タイプ</span><span class="sxs-lookup"><span data-stu-id="008a1-163">Compensation Variable Plan Type</span></span> | <span data-ttu-id="008a1-164">cdm_compensationvariableplantype</span><span class="sxs-lookup"><span data-stu-id="008a1-164">cdm_compensationvariableplantype</span></span> |
| <span data-ttu-id="008a1-165">固定報酬イベント</span><span class="sxs-lookup"><span data-stu-id="008a1-165">Fixed Compensation Event</span></span> | <span data-ttu-id="008a1-166">cdm_fixedcompensationevent</span><span class="sxs-lookup"><span data-stu-id="008a1-166">cdm_fixedcompensationevent</span></span> |
| <span data-ttu-id="008a1-167">給付ルール</span><span class="sxs-lookup"><span data-stu-id="008a1-167">Vesting Rule</span></span> | <span data-ttu-id="008a1-168">cdm_vestingrule</span><span class="sxs-lookup"><span data-stu-id="008a1-168">cdm_vestingrule</span></span> |
| <span data-ttu-id="008a1-169">作業者の固定報酬</span><span class="sxs-lookup"><span data-stu-id="008a1-169">Worker Fixed Compensation</span></span> | <span data-ttu-id="008a1-170">cdm_workerfixedcompensation</span><span class="sxs-lookup"><span data-stu-id="008a1-170">cdm_workerfixedcompensation</span></span> |

## <a name="organization-tables"></a><span data-ttu-id="008a1-171">組織テーブル</span><span class="sxs-lookup"><span data-stu-id="008a1-171">Organization tables</span></span>

| <span data-ttu-id="008a1-172">氏名</span><span class="sxs-lookup"><span data-stu-id="008a1-172">Name</span></span> | <span data-ttu-id="008a1-173">テーブル</span><span class="sxs-lookup"><span data-stu-id="008a1-173">Table</span></span> |
| --- | --- |
| <span data-ttu-id="008a1-174">部門</span><span class="sxs-lookup"><span data-stu-id="008a1-174">Department</span></span> | <span data-ttu-id="008a1-175">cdm_department</span><span class="sxs-lookup"><span data-stu-id="008a1-175">cdm_department</span></span> |
| <span data-ttu-id="008a1-176">雇用</span><span class="sxs-lookup"><span data-stu-id="008a1-176">Employment</span></span> | <span data-ttu-id="008a1-177">cdm_employment</span><span class="sxs-lookup"><span data-stu-id="008a1-177">cdm_employment</span></span> |
| <span data-ttu-id="008a1-178">法人</span><span class="sxs-lookup"><span data-stu-id="008a1-178">Company</span></span> | <span data-ttu-id="008a1-179">cdm_company</span><span class="sxs-lookup"><span data-stu-id="008a1-179">cdm_company</span></span> |
| <span data-ttu-id="008a1-180">ジョブ</span><span class="sxs-lookup"><span data-stu-id="008a1-180">Job</span></span> | <span data-ttu-id="008a1-181">cdm_job</span><span class="sxs-lookup"><span data-stu-id="008a1-181">cdm_job</span></span> |
| <span data-ttu-id="008a1-182">職務権限</span><span class="sxs-lookup"><span data-stu-id="008a1-182">Job Function</span></span> | <span data-ttu-id="008a1-183">cdm_jobfunction</span><span class="sxs-lookup"><span data-stu-id="008a1-183">cdm_jobfunction</span></span> |
| <span data-ttu-id="008a1-184">職位</span><span class="sxs-lookup"><span data-stu-id="008a1-184">Job Position</span></span> | <span data-ttu-id="008a1-185">cdm_jobposition</span><span class="sxs-lookup"><span data-stu-id="008a1-185">cdm_jobposition</span></span> |
| <span data-ttu-id="008a1-186">職位タイプ</span><span class="sxs-lookup"><span data-stu-id="008a1-186">Position Type</span></span> | <span data-ttu-id="008a1-187">cdm_positiontype</span><span class="sxs-lookup"><span data-stu-id="008a1-187">cdm_positiontype</span></span> |
| <span data-ttu-id="008a1-188">職位作業者割り当て</span><span class="sxs-lookup"><span data-stu-id="008a1-188">Position Worker Assignment</span></span> | <span data-ttu-id="008a1-189">cdm_positionworkerassignmentmap</span><span class="sxs-lookup"><span data-stu-id="008a1-189">cdm_positionworkerassignmentmap</span></span> |
| <span data-ttu-id="008a1-190">職位分析コード</span><span class="sxs-lookup"><span data-stu-id="008a1-190">Job Position Dimension</span></span> | <span data-ttu-id="008a1-191">cdm_jobpositiondimension</span><span class="sxs-lookup"><span data-stu-id="008a1-191">cdm_jobpositiondimension</span></span>|
| <span data-ttu-id="008a1-192">職務タイプ</span><span class="sxs-lookup"><span data-stu-id="008a1-192">Job Type</span></span> | <span data-ttu-id="008a1-193">cdm_jobtype</span><span class="sxs-lookup"><span data-stu-id="008a1-193">cdm_jobtype</span></span> |
| <span data-ttu-id="008a1-194">言語</span><span class="sxs-lookup"><span data-stu-id="008a1-194">Language</span></span> | <span data-ttu-id="008a1-195">cdm_language</span><span class="sxs-lookup"><span data-stu-id="008a1-195">cdm_language</span></span> |
| <span data-ttu-id="008a1-196">タイトル</span><span class="sxs-lookup"><span data-stu-id="008a1-196">Title</span></span> | <span data-ttu-id="008a1-197">cdm_title</span><span class="sxs-lookup"><span data-stu-id="008a1-197">cdm_title</span></span> |

> [!NOTE]
> <span data-ttu-id="008a1-198">**職位タイプ** に使用する財務分析コード 、**作業者の職位割り当て**、および **従業員** は、Dataverse にて一方向の統合機能が用意されています。</span><span class="sxs-lookup"><span data-stu-id="008a1-198">Financial dimensions for **Position Type**, **Position Worker Assignment**, and **Employment** provide one-direction integration to Dataverse.</span></span> <span data-ttu-id="008a1-199">財務分析コードの更新は、現在のところ、 Dataverse から Human Resources へは同期されません。</span><span class="sxs-lookup"><span data-stu-id="008a1-199">Financial dimensions updates currently can't synchronize from Dataverse to Human Resources.</span></span> 

## <a name="leave-and-absence-tables"></a><span data-ttu-id="008a1-200">休暇と欠勤テーブル</span><span class="sxs-lookup"><span data-stu-id="008a1-200">Leave and absence tables</span></span>

| <span data-ttu-id="008a1-201">氏名</span><span class="sxs-lookup"><span data-stu-id="008a1-201">Name</span></span> | <span data-ttu-id="008a1-202">テーブル</span><span class="sxs-lookup"><span data-stu-id="008a1-202">Table</span></span> |
| --- | --- |
| <span data-ttu-id="008a1-203">休暇バンク トランザクション</span><span class="sxs-lookup"><span data-stu-id="008a1-203">Leave Bank Transaction</span></span> | <span data-ttu-id="008a1-204">cdm_leavebanktransaction</span><span class="sxs-lookup"><span data-stu-id="008a1-204">cdm_leavebanktransaction</span></span> |
| <span data-ttu-id="008a1-205">休暇登録</span><span class="sxs-lookup"><span data-stu-id="008a1-205">Leave Enrollment</span></span> | <span data-ttu-id="008a1-206">cdm_leaveenrollment</span><span class="sxs-lookup"><span data-stu-id="008a1-206">cdm_leaveenrollment</span></span> |
| <span data-ttu-id="008a1-207">休暇計画</span><span class="sxs-lookup"><span data-stu-id="008a1-207">Leave Plan</span></span> | <span data-ttu-id="008a1-208">cdm_leaveplan</span><span class="sxs-lookup"><span data-stu-id="008a1-208">cdm_leaveplan</span></span> |
| <span data-ttu-id="008a1-209">休暇申請</span><span class="sxs-lookup"><span data-stu-id="008a1-209">Leave Request</span></span> | <span data-ttu-id="008a1-210">cdm_leaverequest</span><span class="sxs-lookup"><span data-stu-id="008a1-210">cdm_leaverequest</span></span> |
| <span data-ttu-id="008a1-211">休暇申請詳細情報</span><span class="sxs-lookup"><span data-stu-id="008a1-211">Leave Request Detail</span></span> | <span data-ttu-id="008a1-212">cdm_leaverequestdetail</span><span class="sxs-lookup"><span data-stu-id="008a1-212">cdm_leaverequestdetail</span></span> |
| <span data-ttu-id="008a1-213">休暇タイプ</span><span class="sxs-lookup"><span data-stu-id="008a1-213">Leave Type</span></span> | <span data-ttu-id="008a1-214">cdm_leavetype</span><span class="sxs-lookup"><span data-stu-id="008a1-214">cdm_leavetype</span></span> |
| <span data-ttu-id="008a1-215">休暇タイプの理由コード</span><span class="sxs-lookup"><span data-stu-id="008a1-215">Leave Type Reason Code</span></span> | <span data-ttu-id="008a1-216">cdm_leavetypereasoncode</span><span class="sxs-lookup"><span data-stu-id="008a1-216">cdm_leavetypereasoncode</span></span> |

## <a name="payroll-tables"></a><span data-ttu-id="008a1-217">給与テーブル</span><span class="sxs-lookup"><span data-stu-id="008a1-217">Payroll tables</span></span>

| <span data-ttu-id="008a1-218">氏名</span><span class="sxs-lookup"><span data-stu-id="008a1-218">Name</span></span> | <span data-ttu-id="008a1-219">テーブル</span><span class="sxs-lookup"><span data-stu-id="008a1-219">Table</span></span> |
| --- | --- |
| <span data-ttu-id="008a1-220">支払サイクル</span><span class="sxs-lookup"><span data-stu-id="008a1-220">Pay Cycle</span></span> | <span data-ttu-id="008a1-221">cdm_paycycle</span><span class="sxs-lookup"><span data-stu-id="008a1-221">cdm_paycycle</span></span> |
| <span data-ttu-id="008a1-222">支払期間</span><span class="sxs-lookup"><span data-stu-id="008a1-222">Pay Period</span></span> | <span data-ttu-id="008a1-223">cdm_payperiod</span><span class="sxs-lookup"><span data-stu-id="008a1-223">cdm_payperiod</span></span> |
| <span data-ttu-id="008a1-224">給与所得コード</span><span class="sxs-lookup"><span data-stu-id="008a1-224">Payroll Earning Code</span></span> | <span data-ttu-id="008a1-225">cdm_payrollearningcode</span><span class="sxs-lookup"><span data-stu-id="008a1-225">cdm_payrollearningcode</span></span> |
| <span data-ttu-id="008a1-226">銀行口座支出</span><span class="sxs-lookup"><span data-stu-id="008a1-226">Bank Account Disbursement</span></span> | <span data-ttu-id="008a1-227">cdm_bankaccountdisbursement</span><span class="sxs-lookup"><span data-stu-id="008a1-227">cdm_bankaccountdisbursement</span></span> |
| <span data-ttu-id="008a1-228">税地域</span><span class="sxs-lookup"><span data-stu-id="008a1-228">Tax Region</span></span> | <span data-ttu-id="008a1-229">cdm_taxregion</span><span class="sxs-lookup"><span data-stu-id="008a1-229">cdm_taxregion</span></span> |

## <a name="worker-tables"></a><span data-ttu-id="008a1-230">作業者テーブル</span><span class="sxs-lookup"><span data-stu-id="008a1-230">Worker tables</span></span>

| <span data-ttu-id="008a1-231">氏名</span><span class="sxs-lookup"><span data-stu-id="008a1-231">Name</span></span> | <span data-ttu-id="008a1-232">テーブル</span><span class="sxs-lookup"><span data-stu-id="008a1-232">Table</span></span> |
| --- | --- |
| <span data-ttu-id="008a1-233">作業者</span><span class="sxs-lookup"><span data-stu-id="008a1-233">Worker</span></span> | <span data-ttu-id="008a1-234">cdm_worker</span><span class="sxs-lookup"><span data-stu-id="008a1-234">cdm_worker</span></span> |
| <span data-ttu-id="008a1-235">作業者住所</span><span class="sxs-lookup"><span data-stu-id="008a1-235">Worker Address</span></span> | <span data-ttu-id="008a1-236">cdm_workeraddress</span><span class="sxs-lookup"><span data-stu-id="008a1-236">cdm_workeraddress</span></span> |
| <span data-ttu-id="008a1-237">作業者の個人詳細</span><span class="sxs-lookup"><span data-stu-id="008a1-237">Worker Personal Detail</span></span> | <span data-ttu-id="008a1-238">cdm_workerpersonaldetail</span><span class="sxs-lookup"><span data-stu-id="008a1-238">cdm_workerpersonaldetail</span></span> |
| <span data-ttu-id="008a1-239">ワーカーの個人識別番号</span><span class="sxs-lookup"><span data-stu-id="008a1-239">Worker Person Identification Number</span></span> | <span data-ttu-id="008a1-240">cdm_workerpersonidentificationnumber</span><span class="sxs-lookup"><span data-stu-id="008a1-240">cdm_workerpersonidentificationnumber</span></span> |
| <span data-ttu-id="008a1-241">作業者の ID タイプ</span><span class="sxs-lookup"><span data-stu-id="008a1-241">Worker Person Identification Type</span></span> | <span data-ttu-id="008a1-242">cdm_workerpersonidentificationtype</span><span class="sxs-lookup"><span data-stu-id="008a1-242">cdm_workerpersonidentificationtype</span></span> |
| <span data-ttu-id="008a1-243">作業カレンダー</span><span class="sxs-lookup"><span data-stu-id="008a1-243">Work Calendar</span></span> | <span data-ttu-id="008a1-244">cdm_workcalendar</span><span class="sxs-lookup"><span data-stu-id="008a1-244">cdm_workcalendar</span></span> |
| <span data-ttu-id="008a1-245">作業カレンダー日</span><span class="sxs-lookup"><span data-stu-id="008a1-245">Work Calendar Day</span></span> | <span data-ttu-id="008a1-246">cdm_workcalendarday</span><span class="sxs-lookup"><span data-stu-id="008a1-246">cdm_workcalendarday</span></span> |
| <span data-ttu-id="008a1-247">作業カレンダーの休日</span><span class="sxs-lookup"><span data-stu-id="008a1-247">Work Calendar Holiday</span></span> |<span data-ttu-id="008a1-248">cdm_workcalendarholiday</span><span class="sxs-lookup"><span data-stu-id="008a1-248">cdm_workcalendarholiday</span></span> |
| <span data-ttu-id="008a1-249">作業カレンダーの休日行</span><span class="sxs-lookup"><span data-stu-id="008a1-249">Work Calendar Holiday Line</span></span> | <span data-ttu-id="008a1-250">cdm_workcalendarholidayline</span><span class="sxs-lookup"><span data-stu-id="008a1-250">cdm_workcalendarholidayline</span></span> |
| <span data-ttu-id="008a1-251">作業カレンダー時間間隔</span><span class="sxs-lookup"><span data-stu-id="008a1-251">Work Calendar Time Interval</span></span> | <span data-ttu-id="008a1-252">cdm_workcalendartimeinterval (カスタム フィールド サポートに対しては有効化されていない)</span><span class="sxs-lookup"><span data-stu-id="008a1-252">cdm_workcalendartimeinterval (Not enabled for custom field support)</span></span> |
| <span data-ttu-id="008a1-253">作業者の銀行口座</span><span class="sxs-lookup"><span data-stu-id="008a1-253">Worker Bank Account</span></span> | <span data-ttu-id="008a1-254">cdm_workerbankaccount</span><span class="sxs-lookup"><span data-stu-id="008a1-254">cdm_workerbankaccount</span></span> |

## <a name="worker-setup-tables"></a><span data-ttu-id="008a1-255">作業者の設定テーブル</span><span class="sxs-lookup"><span data-stu-id="008a1-255">Worker setup tables</span></span>

| <span data-ttu-id="008a1-256">氏名</span><span class="sxs-lookup"><span data-stu-id="008a1-256">Name</span></span> | <span data-ttu-id="008a1-257">テーブル</span><span class="sxs-lookup"><span data-stu-id="008a1-257">Table</span></span> |
| --- | --- |
| <span data-ttu-id="008a1-258">退役軍人状態</span><span class="sxs-lookup"><span data-stu-id="008a1-258">Veteran Status</span></span> | <span data-ttu-id="008a1-259">cdm_veteranstatus</span><span class="sxs-lookup"><span data-stu-id="008a1-259">cdm_veteranstatus</span></span> |
| <span data-ttu-id="008a1-260">出身民族</span><span class="sxs-lookup"><span data-stu-id="008a1-260">Ethnic Origin</span></span> | <span data-ttu-id="008a1-261">cdm_ethnicorigin</span><span class="sxs-lookup"><span data-stu-id="008a1-261">cdm_ethnicorigin</span></span> |
| <span data-ttu-id="008a1-262">理由コード</span><span class="sxs-lookup"><span data-stu-id="008a1-262">Reason Code</span></span> | <span data-ttu-id="008a1-263">cdm_reasoncode</span><span class="sxs-lookup"><span data-stu-id="008a1-263">cdm_reasoncode</span></span> |
| <span data-ttu-id="008a1-264">個人 ID の発行機関</span><span class="sxs-lookup"><span data-stu-id="008a1-264">Person Identification Issuing Agency</span></span> | <span data-ttu-id="008a1-265">cdm_personidentificationissuingagency</span><span class="sxs-lookup"><span data-stu-id="008a1-265">cdm_personidentificationissuingagency</span></span> |

## <a name="competency-tables"></a><span data-ttu-id="008a1-266">能力テーブル</span><span class="sxs-lookup"><span data-stu-id="008a1-266">Competency tables</span></span>

| <span data-ttu-id="008a1-267">氏名</span><span class="sxs-lookup"><span data-stu-id="008a1-267">Name</span></span> | <span data-ttu-id="008a1-268">テーブル</span><span class="sxs-lookup"><span data-stu-id="008a1-268">Table</span></span> |
| --- | --- |
| <span data-ttu-id="008a1-269">スキルのタイプ</span><span class="sxs-lookup"><span data-stu-id="008a1-269">Skill Type</span></span> | <span data-ttu-id="008a1-270">cdm_skilltype</span><span class="sxs-lookup"><span data-stu-id="008a1-270">cdm_skilltype</span></span> |

## <a name="table-relationship-models"></a><span data-ttu-id="008a1-271">テーブル関係モデル</span><span class="sxs-lookup"><span data-stu-id="008a1-271">Table relationship models</span></span>

### <a name="worker"></a><span data-ttu-id="008a1-272">ワーカー</span><span class="sxs-lookup"><span data-stu-id="008a1-272">Worker</span></span>

![ワーカー](./media/HCMCommon-worker-entity-diagram.png)

### <a name="job-and-job-position"></a><span data-ttu-id="008a1-274">職務および職位</span><span class="sxs-lookup"><span data-stu-id="008a1-274">Job and Job Position</span></span>

![職務および職位](./media/HCMCommon-job-and-job-position-entity-diagram.png)

### <a name="benefits"></a><span data-ttu-id="008a1-276">福利厚生</span><span class="sxs-lookup"><span data-stu-id="008a1-276">Benefits</span></span>

![福利厚生](./media/HCMCommon-benefits-entity-diagram.png)

### <a name="compensation"></a><span data-ttu-id="008a1-278">報酬</span><span class="sxs-lookup"><span data-stu-id="008a1-278">Compensation</span></span>

![報酬](./media/HCMCommon-compensation-entity-diagram.png)

### <a name="leave"></a><span data-ttu-id="008a1-280">離脱</span><span class="sxs-lookup"><span data-stu-id="008a1-280">Leave</span></span>

![離脱](./media/HCMCommon-leave-entity-diagram.png)

### <a name="work-calendar"></a><span data-ttu-id="008a1-282">作業カレンダー</span><span class="sxs-lookup"><span data-stu-id="008a1-282">Work Calendar</span></span>

![作業カレンダー](./media/HCMCommon-work-calendar-entity-diagram.png)

## <a name="see-also"></a><span data-ttu-id="008a1-284">参照</span><span class="sxs-lookup"><span data-stu-id="008a1-284">See also</span></span>

[<span data-ttu-id="008a1-285">データ統合テクノロジの選択</span><span class="sxs-lookup"><span data-stu-id="008a1-285">Choose a data integration technology</span></span>](hr-admin-integration-choose-technology.md)<br>
[<span data-ttu-id="008a1-286">Dataverse 統合のコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="008a1-286">Configure Dataverse integration</span></span>](hr-admin-integration-common-data-service.md)<br>
[<span data-ttu-id="008a1-287">構成 Dataverse 仮想テーブル</span><span class="sxs-lookup"><span data-stu-id="008a1-287">Configure Dataverse virtual tables</span></span>](hr-admin-integration-common-data-service-virtual-entities.md)<br>
[<span data-ttu-id="008a1-288">Human Resources 仮想テーブルに関するよく寄せられる質問</span><span class="sxs-lookup"><span data-stu-id="008a1-288">Human Resources virtual tables FAQ</span></span>](hr-admin-virtual-entity-faq.md)<br>
[<span data-ttu-id="008a1-289">Microsoft Dataverse とは</span><span class="sxs-lookup"><span data-stu-id="008a1-289">What is Microsoft Dataverse?</span></span>](https://docs.microsoft.com/powerapps/maker/data-platform/data-platform-intro)<br>
[<span data-ttu-id="008a1-290">用語の更新</span><span class="sxs-lookup"><span data-stu-id="008a1-290">Terminology updates</span></span>](https://docs.microsoft.com/powerapps/maker/data-platform/data-platform-intro#terminology-updates)


[!INCLUDE[footer-include](../includes/footer-banner.md)]