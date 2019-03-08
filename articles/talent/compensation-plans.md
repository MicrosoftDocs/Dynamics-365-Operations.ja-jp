---
title: 報酬プラン
description: 報酬と給付金マネージャーは、報酬管理を使用して、組織の従業員の固定報酬プランおよび変動報酬プランを管理し、処理できます。
author: kherr75
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: HcmCompensationLevel, HRCCompGrid, HRMCompFixedAction, HRMCompFixedBudget, HRMCompFixedPlanTable
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Core, Operations, Talent
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.author: kherr
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Talent July 2017 update
ms.openlocfilehash: e80b3ebc9c374073ff5a2dfc8c2acf1d7f6c6287
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/29/2019
ms.locfileid: "305139"
---
# <a name="compensation-plans"></a><span data-ttu-id="d218f-103">報酬プラン</span><span class="sxs-lookup"><span data-stu-id="d218f-103">Compensation plans</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="d218f-104">報酬と給付金マネージャーは、報酬管理を使用して、組織の従業員の固定報酬プランおよび変動報酬プランを管理し、処理できます。</span><span class="sxs-lookup"><span data-stu-id="d218f-104">Compensation and Benefits Managers can use Compensation management to maintain and process fixed and variable compensation plans for the organization's employees.</span></span>

### <a name="introduction"></a><span data-ttu-id="d218f-105">はじめに</span><span class="sxs-lookup"><span data-stu-id="d218f-105">Introduction</span></span>

<span data-ttu-id="d218f-106">基準賃金と報奨を管理するには、報酬管理を使用します。</span><span class="sxs-lookup"><span data-stu-id="d218f-106">Compensation management is used to control the delivery of base pay and awards.</span></span> <span data-ttu-id="d218f-107">従業員の固定基準賃金および昇給は固定報酬プランで管理されます。</span><span class="sxs-lookup"><span data-stu-id="d218f-107">An employee's fixed base pay and merit increases are controlled through fixed compensation plans.</span></span> <span data-ttu-id="d218f-108">インセンティブ支払 (賞与の支払、業績報奨、ストック オプション、付与など) の支払および一時報奨は変動報酬プランで管理します。</span><span class="sxs-lookup"><span data-stu-id="d218f-108">The payment of incentive pay, such as bonus payments, performance awards, stock options, and grants, and also one-time awards, are controlled through variable compensation plans.</span></span> 

<span data-ttu-id="d218f-109">従業員は、両方のタイプの 1 つまたは複数のプランに登録することができます。</span><span class="sxs-lookup"><span data-stu-id="d218f-109">Employees can be enrolled in one or more plans of both types.</span></span> <span data-ttu-id="d218f-110">従業員は、報酬プランの登録対象となるには、次の要件を満たす必要があります。</span><span class="sxs-lookup"><span data-stu-id="d218f-110">An employee must meet the following requirements in order to be eligible for enrollment in a compensation plan:</span></span>
-   <span data-ttu-id="d218f-111">従業員は、有効な職位割り当てが必要です。</span><span class="sxs-lookup"><span data-stu-id="d218f-111">The employee must have an active position assignment.</span></span>
-   <span data-ttu-id="d218f-112">従業員は、報酬プランの適格性ルールで定義された基準を満たす必要があります。</span><span class="sxs-lookup"><span data-stu-id="d218f-112">The employee must meet the criteria that are defined by eligibility rules for a compensation plan.</span></span>

## <a name="compensation-setup"></a><span data-ttu-id="d218f-113">報酬の設定</span><span class="sxs-lookup"><span data-stu-id="d218f-113">Compensation setup</span></span>
<span data-ttu-id="d218f-114">次の表に、会社の報酬プランの設定で不可欠な報酬プロセスのコンポーネント一覧を示します。</span><span class="sxs-lookup"><span data-stu-id="d218f-114">The following table lists components of the compensation process that can be integral in setting up your company's compensation plans.</span></span>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="d218f-115">コンポーネント</span><span class="sxs-lookup"><span data-stu-id="d218f-115">Component</span></span></th>
<th><span data-ttu-id="d218f-116">詳細</span><span class="sxs-lookup"><span data-stu-id="d218f-116">More information…</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="d218f-117">固定報酬アクション</span><span class="sxs-lookup"><span data-stu-id="d218f-117">Fixed compensation actions</span></span></td>
<td><span data-ttu-id="d218f-118">固定報酬アクションには 2 つの目的があります。</span><span class="sxs-lookup"><span data-stu-id="d218f-118">Fixed compensation actions accomplish two purposes:</span></span>
<ul>
<li><span data-ttu-id="d218f-119">アクションで、従業員の報酬が変更されたときに記録する必要のある情報の種類を指定できます。</span><span class="sxs-lookup"><span data-stu-id="d218f-119">Actions can specify the kind of information that must be recorded when an employee’s compensation changes.</span></span> <span data-ttu-id="d218f-120">たとえば、昇給や降給などの変更と理由を記録するよう要求できます。</span><span class="sxs-lookup"><span data-stu-id="d218f-120">For example, you can require that the reason a change, such as a promotion or a demotion be recorded.</span></span></li>
<li><span data-ttu-id="d218f-121">アクションによって、固定報酬プランが処理されるときの計算を適用することを確認できます。</span><span class="sxs-lookup"><span data-stu-id="d218f-121">Actions can ensure that a calculation is applied when fixed compensation plans are processed.</span></span>  <span data-ttu-id="d218f-122">たとえば、株主資本タイプのアクションでは、従業員のレベルの最小基準点と従業員への支払を比較し、従業員が最低限以上の給料を受け取っていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="d218f-122">For example, actions of type Equity will compare the employees pay to the minimum reference point for the level on the employee&#39;s and ensure the employee is getting paid at least the minimum.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d218f-123">レベル</span><span class="sxs-lookup"><span data-stu-id="d218f-123">Levels</span></span></td>
<td><span data-ttu-id="d218f-124">レベルは、ジョブと、ジョブ参照に関連付けられた職位に関連付けられます。</span><span class="sxs-lookup"><span data-stu-id="d218f-124">Levels are associated with jobs and any positions that are related to a job reference.</span></span> <span data-ttu-id="d218f-125">3 種類の報酬プラン (等級、バンド、ステップ) について、それぞれ異なるレベルを作成できます。</span><span class="sxs-lookup"><span data-stu-id="d218f-125">You can create discrete levels for the three types of compensation plans: Grade, Band, and Step.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d218f-126">給与レンジ到達割合マトリックス</span><span class="sxs-lookup"><span data-stu-id="d218f-126">Range utilization matrix</span></span></td>
<td><span data-ttu-id="d218f-127">給与レンジ到達割合マトリックスでは、従業員を標準職務給に移行させることができます。</span><span class="sxs-lookup"><span data-stu-id="d218f-127">A range utilization matrix helps you transition employees to the control point for their jobs.</span></span> <span data-ttu-id="d218f-128">給与レンジ到達割合を使用して、各従業員の業績や会社全体の業績に関係のない、社内の支払レートの株式資本を管理することもできます。</span><span class="sxs-lookup"><span data-stu-id="d218f-128">You can also use range utilization to control pay rate equity in the company without regard to an individual employee&#39;s performance or the overall performance of the company.</span></span> <span data-ttu-id="d218f-129">たとえば、給与レンジの低い従業員は、給与レンジの高い従業員よりも高い昇給率が割り当てられます。</span><span class="sxs-lookup"><span data-stu-id="d218f-129">For example, employees who are paid lower in their range get higher percentage increases than employees who are paid higher in the range.</span></span> <span data-ttu-id="d218f-130">これにより、体系的に資本の差額を相殺できます。</span><span class="sxs-lookup"><span data-stu-id="d218f-130">In this manner, you can systematically offset equity differences.</span></span> <span data-ttu-id="d218f-131">給与レンジ到達割合は、"固定支払レート - 範囲の最低額 / 範囲の最高額 - 範囲の最低額" として計算されます。</span><span class="sxs-lookup"><span data-stu-id="d218f-131">The range utilization is calculated as follows: (Fixed Pay Rate - Range Minimum) ÷ (Range Maximum - Range Minimum).</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d218f-132">基準点設定</span><span class="sxs-lookup"><span data-stu-id="d218f-132">Reference point setups</span></span></td>
<td><span data-ttu-id="d218f-133">基準点設定には、マトリックスの範囲を構成する基準点のセットが含まれます。</span><span class="sxs-lookup"><span data-stu-id="d218f-133">A reference point setup includes a set of reference points that represent ranges in a matrix.</span></span> <span data-ttu-id="d218f-134">それぞれの範囲は、支払レートに関連付けることができます。</span><span class="sxs-lookup"><span data-stu-id="d218f-134">Each range can be associated with a pay rate.</span></span> <span data-ttu-id="d218f-135">たとえば、等級プランには、よく平均、最小および最大の基準点があります。</span><span class="sxs-lookup"><span data-stu-id="d218f-135">For example, grade plans will often have reference points of Minimum, Midpoint, and Maximum.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d218f-136">報酬マトリックス</span><span class="sxs-lookup"><span data-stu-id="d218f-136">Compensation matrix</span></span></td>
<td><span data-ttu-id="d218f-137">報酬マトリックスは、報酬構造の作成に使用する基準点およびレベルのセットです。</span><span class="sxs-lookup"><span data-stu-id="d218f-137">A compensation matrix is the set of reference points and levels that you use to create a compensation structure.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d218f-138">報酬構造</span><span class="sxs-lookup"><span data-stu-id="d218f-138">Compensation structure</span></span></td>
<td><span data-ttu-id="d218f-139">報酬構造は、各レベルの基準点に関連付けられている支払レートを持つ報酬マトリックスです。</span><span class="sxs-lookup"><span data-stu-id="d218f-139">A compensation structure is a compensation matrix that has pay rates associated with the reference points for each level.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d218f-140">適格性ルール</span><span class="sxs-lookup"><span data-stu-id="d218f-140">Eligibility rules</span></span></td>
<td><span data-ttu-id="d218f-141">適格性ルールは、特定のジョブ、ジョブ機能、ジョブ タイプ、部門、労働組合、または特定の報酬プランの対象になる報酬場所で従業員を識別するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="d218f-141">Eligibility rules are used to identify employees in specific jobs, job functions, job types, departments, labor unions, or compensation regions that are covered by specific compensation plans.</span></span> <span data-ttu-id="d218f-142">プランに従業員を登録するために、変動報酬プランと固定報酬プランの両方に対して適格性ルールを作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="d218f-142">You must create eligibility rules for both variable and fixed compensation plans in order to enroll employees in the plan.</span></span> <span data-ttu-id="d218f-143">報酬プランの適格性ルールを指定したら、そのプランの対象になるジョブに適用するレベルを定義できます。</span><span class="sxs-lookup"><span data-stu-id="d218f-143">After eligibility rules are specified for a compensation plan, you can define the levels that should apply to the jobs that are covered by the plan.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d218f-144">支払頻度</span><span class="sxs-lookup"><span data-stu-id="d218f-144">Pay frequencies</span></span></td>
<td><span data-ttu-id="d218f-145">支払頻度は、報酬に指定される期間の定義に使用されます。</span><span class="sxs-lookup"><span data-stu-id="d218f-145">Pay frequencies are used to define the time period for which the compensation is specified.</span></span>  <span data-ttu-id="d218f-146">たとえば、支払頻度は、報酬額が年間給与または時給レートで指定されているかを把握することに役立ちます。</span><span class="sxs-lookup"><span data-stu-id="d218f-146">For example, the pay frequency helps you understand if the compensation amount is specified as an annual salary versus an hourly pay rate.</span></span> <span data-ttu-id="d218f-147">支払頻度は、換算率の設定にも使用され、支払頻度を月、週、隔週、および時間から年に変換できます。</span><span class="sxs-lookup"><span data-stu-id="d218f-147">Pay frequencies are also used to set up conversion factors to convert compensation amounts from monthly, weekly, biweekly and hourly pay frequencies to an annual pay frequency.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d218f-148">報酬地域</span><span class="sxs-lookup"><span data-stu-id="d218f-148">Compensation regions</span></span></td>
<td><span data-ttu-id="d218f-149">報酬場所は、作業場所に基づいて従業員の報酬を指定するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="d218f-149">Compensation regions are used to specify employee compensation based on the location of the workplace.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d218f-150">標準職務給</span><span class="sxs-lookup"><span data-stu-id="d218f-150">Control point</span></span></td>
<td><span data-ttu-id="d218f-151">標準職務給は、ある報酬レベルにおける、すべての従業員に対して最適だと考える支払レートを定義します。</span><span class="sxs-lookup"><span data-stu-id="d218f-151">The control point defines what you consider to be the ideal pay rate for all employees at a compensation level.</span></span> <span data-ttu-id="d218f-152">通常、段階的なプラン構造の場合、範囲の中間点が標準職務給になります。</span><span class="sxs-lookup"><span data-stu-id="d218f-152">For grade plan structures, control points are typically the midpoint of the ranges.</span></span> <span data-ttu-id="d218f-153">バンド構造では、標準職務給はほとんど使用されません。</span><span class="sxs-lookup"><span data-stu-id="d218f-153">Band structures rarely use control points.</span></span> <span data-ttu-id="d218f-154">[固定報酬プラン] フォームで、固定報酬プランの標準職務給を指定できます。</span><span class="sxs-lookup"><span data-stu-id="d218f-154">You can specify the control point for a fixed compensation plan in the Fixed compensation plans form.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d218f-155">ジョブ機能</span><span class="sxs-lookup"><span data-stu-id="d218f-155">Job functions</span></span></td>
<td><span data-ttu-id="d218f-156">職務権限は、特定の職務に対する報酬プランの分類やフィルタ処理に使用されます。</span><span class="sxs-lookup"><span data-stu-id="d218f-156">Job functions are used to classify and filter compensation plans to specific jobs.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d218f-157">ジョブ タイプ</span><span class="sxs-lookup"><span data-stu-id="d218f-157">Job types</span></span></td>
<td><span data-ttu-id="d218f-158">ジョブ タイプは、特定の職務に対する報酬プランの分類やフィルタ処理に使用されます。</span><span class="sxs-lookup"><span data-stu-id="d218f-158">Job types are used to classify and filter compensation plans to specific jobs.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d218f-159">変動報酬タイプ</span><span class="sxs-lookup"><span data-stu-id="d218f-159">Variable compensation types</span></span></td>
<td><span data-ttu-id="d218f-160">株式付与や賞金ボーナスなどの変動報酬タイプは、変動報酬プランで設定されます。</span><span class="sxs-lookup"><span data-stu-id="d218f-160">Variable compensation types, such as stock awards or cash award bonuses, are set up in variable compensation plans.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d218f-161">報酬グリッド</span><span class="sxs-lookup"><span data-stu-id="d218f-161">Compensation grids</span></span></td>
<td><span data-ttu-id="d218f-162">報酬グリッドには、報酬構造が含まれます。</span><span class="sxs-lookup"><span data-stu-id="d218f-162">Compensation grids contain the compensation structure.</span></span>  <span data-ttu-id="d218f-163">報酬グリッドは、1 つ以上の報酬プランで使用できます。</span><span class="sxs-lookup"><span data-stu-id="d218f-163">Compensation grids can be used by one or more compensation plans.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d218f-164">業績計画</span><span class="sxs-lookup"><span data-stu-id="d218f-164">Performance plans</span></span></td>
<td><span data-ttu-id="d218f-165">業績計画を使用して業績を配賦マトリックスに関連付けると、業績計画を能力給戦略で使用できるようになります。</span><span class="sxs-lookup"><span data-stu-id="d218f-165">Performance plans are used to associate performance with an allocation matrix, so that you can use the plan in a pay-for-performance strategy.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d218f-166">業績評価</span><span class="sxs-lookup"><span data-stu-id="d218f-166">Performance ratings</span></span></td>
<td><span data-ttu-id="d218f-167">業績評価は、業績計画で昇給や業績報奨の金額を決定するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="d218f-167">Performance ratings are used in performance plans to determine the amount of a merit award or performance award.</span></span></td>
</tr>
</tbody>
</table>

## <a name="process-events"></a><span data-ttu-id="d218f-168">プロセス イベント</span><span class="sxs-lookup"><span data-stu-id="d218f-168">Process events</span></span>
<span data-ttu-id="d218f-169">プロセス イベントでは、1 つ以上の固定報酬プランまたは変動報酬プランに登録されるすべての従業員の、特定の期間の報酬情報を計算します。</span><span class="sxs-lookup"><span data-stu-id="d218f-169">A process event calculates compensation information for a specific period for all employees who are enrolled in one or more fixed or variable compensation plans.</span></span> <span data-ttu-id="d218f-170">計算した報酬結果をテストしたり更新したり場合に、プロセス イベントを繰り返し実行できます。</span><span class="sxs-lookup"><span data-stu-id="d218f-170">You can run a process event repeatedly to test or update calculated compensation results.</span></span>

<a name="compensation-events"></a><span data-ttu-id="d218f-171">報酬イベント</span><span class="sxs-lookup"><span data-stu-id="d218f-171">Compensation events</span></span>
-------------------

<span data-ttu-id="d218f-172">プロセス イベントを実行するたびに、報酬イベントが作成されます。</span><span class="sxs-lookup"><span data-stu-id="d218f-172">Each time a process event is run, a compensation event is created.</span></span>  <span data-ttu-id="d218f-173">報酬イベントには、そのプロセス イベントに含まれる各従業員の報酬プロセスの結果が含まれます。</span><span class="sxs-lookup"><span data-stu-id="d218f-173">Compensation events contain the results of the compensation process for each employee included in that process event.</span></span>  <span data-ttu-id="d218f-174">計算が正しい場合、プロセス イベントによって影響を受ける従業員の報酬レコードを更新するために、報酬イベントを読み込むことができます。</span><span class="sxs-lookup"><span data-stu-id="d218f-174">When the calculations are correct, you can load the compensation event to update the compensation records for the employees who are affected by the process event.</span></span>

## <a name="recommendations"></a><span data-ttu-id="d218f-175">推奨事項</span><span class="sxs-lookup"><span data-stu-id="d218f-175">Recommendations</span></span>
<span data-ttu-id="d218f-176">プロセス イベントを実行した後、プロセス イベントの計算された規定に基づいて従業員の昇給または報奨の金額の調整を認定できます。</span><span class="sxs-lookup"><span data-stu-id="d218f-176">After you run a process event, you can recommend adjustments to an employee’s merit increase or award amount, based on the calculated guidelines of the process event.</span></span> <span data-ttu-id="d218f-177">従業員の認定を行うには、報酬プランの設定時またはプロセス イベントの設定時に認定を有効にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="d218f-177">To make recommendations for employees, you must enable recommendations when you set up compensation plans or when you set up the process event.</span></span>



