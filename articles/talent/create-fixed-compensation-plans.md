---
title: "固定報酬計画の作成"
description: "固定報酬は、従業員の通常の全体の給与や賃金を示します。 この記事は、固定報酬プランを作成し、従業員を登録する前に設定する必要があるコンポーネントを説明します。"
author: kherr75
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
ms.search.form: HRCCompGrid, HRCCompRefPointSetup, HRMCompEligibility, HRMCompEvent, HRMFixedCompPlanTable
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Core, Operations, Talent
ms.custom: 15991
ms.assetid: ef8cf992-176c-4c98-9dff-6510e1eb9f1c
ms.search.region: Global
ms.author: kherr
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Talent July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: ceea24519d641c676521771cee274feb64ca7783
ms.openlocfilehash: 0af9dd6c399032597b863f0fa15c58d3e094ba5b
ms.contentlocale: ja-jp
ms.lasthandoff: 01/31/2018

---

# <a name="create-fixed-compensation-plans"></a><span data-ttu-id="23896-104">固定報酬計画の作成</span><span class="sxs-lookup"><span data-stu-id="23896-104">Create fixed compensation plans</span></span>

[!include[banner](includes/banner.md)]


<span data-ttu-id="23896-105">固定報酬は、従業員の通常の全体の給与や賃金を示します。</span><span class="sxs-lookup"><span data-stu-id="23896-105">Fixed compensation refers to an employee's regular gross salary or wages.</span></span> <span data-ttu-id="23896-106">このトピックは、固定報酬プランを作成し、従業員を登録する前に設定する必要があるコンポーネントを説明します。</span><span class="sxs-lookup"><span data-stu-id="23896-106">This topic describes the components that must be set up before you can create a fixed compensation plan and enroll employees.</span></span>

<span data-ttu-id="23896-107">固定報酬金額は、パフォーマンス、地域、昇給予算などの係数に基づいて、従業員に対して計算できます。</span><span class="sxs-lookup"><span data-stu-id="23896-107">Fixed compensation amounts can be calculated for your employees, based on factors such as performance, region, and budget increases.</span></span> <span data-ttu-id="23896-108">Microsoft Talent では、ステップ、等級、およびバンド報酬のタイプがサポートされます。</span><span class="sxs-lookup"><span data-stu-id="23896-108">Microsoft Talent supports step, grade, and band compensation types.</span></span>

## <a name="fixed-compensation-components"></a><span data-ttu-id="23896-109">固定報酬コンポーネント</span><span class="sxs-lookup"><span data-stu-id="23896-109">Fixed compensation components</span></span>
### <a name="compensation-levels"></a><span data-ttu-id="23896-110">報酬レベル</span><span class="sxs-lookup"><span data-stu-id="23896-110">Compensation levels</span></span>

<span data-ttu-id="23896-111">さまざまなジョブに対する報酬を設定し、従業員がこれらのジョブを維持し、公正に支払われることを保証するために、**報酬レベル**を使用できます。</span><span class="sxs-lookup"><span data-stu-id="23896-111">You can use **compensation levels** to set compensation for various jobs, to help guarantee that the employees who hold those jobs are paid fairly.</span></span> <span data-ttu-id="23896-112">[報酬レベル] ページで、各ステップ、等級、およびバンド プランに必要な報酬レベルを設定できます。</span><span class="sxs-lookup"><span data-stu-id="23896-112">On the **Compensation levels** page, you can set up the compensation levels that are required for each step, grade, and band plan.</span></span> <span data-ttu-id="23896-113">[上へ] および [下へ] ボタンを使用して、各タイプに従ってレベルを設定します。</span><span class="sxs-lookup"><span data-stu-id="23896-113">Use the **Up** and **Down** buttons to put the levels in the correct order, according to their type.</span></span> <span data-ttu-id="23896-114">ジョブの報酬レベルを設定することにより、すべての従業員がその職務を維持し、同じレベルで支給されることを保証できます。</span><span class="sxs-lookup"><span data-stu-id="23896-114">By setting compensation levels on a job, you help guarantee that all employees who hold a position for that job are paid at the same level.</span></span>

### <a name="reference-points"></a><span data-ttu-id="23896-115">基準点</span><span class="sxs-lookup"><span data-stu-id="23896-115">Reference points</span></span>

<span data-ttu-id="23896-116">[基準点] は、各レベルの報酬範囲を定義するグリッドの列です。</span><span class="sxs-lookup"><span data-stu-id="23896-116">**Reference points** are the columns in the grid that define the compensation ranges for each level.</span></span> <span data-ttu-id="23896-117">[報酬レベル] は、グリッドの行です。</span><span class="sxs-lookup"><span data-stu-id="23896-117">The compensation level is the row in the grid.</span></span> <span data-ttu-id="23896-118">等級タイプのプランの標準的な基準点は、最小、平均、および最大です。</span><span class="sxs-lookup"><span data-stu-id="23896-118">Typical reference points for a plan of the grade type are a minimum, a midpoint, and a maximum.</span></span> <span data-ttu-id="23896-119">[基準点設定] ページで基準点を作成します。</span><span class="sxs-lookup"><span data-stu-id="23896-119">You create reference points on the **Reference point setups** page.</span></span>

### <a name="compensation-grids"></a><span data-ttu-id="23896-120">報酬グリッド</span><span class="sxs-lookup"><span data-stu-id="23896-120">Compensation grids</span></span>

<span data-ttu-id="23896-121">レベルと基準点を設定したら、それらを組み合わせて**報酬グリッド**を作成できます。</span><span class="sxs-lookup"><span data-stu-id="23896-121">After you set up the levels and reference points, they can be combined to create a **compensation grid**.</span></span> <span data-ttu-id="23896-122">[報酬グリッド] ページで、グリッドに関する情報を定義します。</span><span class="sxs-lookup"><span data-stu-id="23896-122">On the **Compensation grids** page, define information about the grid.</span></span> <span data-ttu-id="23896-123">たとえば、使用されるグリッドのデザイン、使用するプランのタイプ、グリッドに必要な基準点と列を指定します。</span><span class="sxs-lookup"><span data-stu-id="23896-123">For example, specify what the grid designed to be used for, what type of plan it will be used with, and which reference points or columns are required in the grid.</span></span> <span data-ttu-id="23896-124">その情報を入力したら、[報酬構造] をクリックして、グリッドにレベルと金額を追加します。</span><span class="sxs-lookup"><span data-stu-id="23896-124">After you've finished entering that information, click **Compensation structure** to add levels and amounts to your grid.</span></span> 

<span data-ttu-id="23896-125">**ヒント:** 報酬構造の [一括変更] 機能を使用して、最初の金額を設定し、次にレベルまたは基準点の割合または金額を増加します。</span><span class="sxs-lookup"><span data-stu-id="23896-125">**Tip:** Use the **Mass changes** function on the compensation structure to set initial amounts, and then increment by percentages or amounts across your levels or reference points.</span></span>

### <a name="pay-frequencies"></a><span data-ttu-id="23896-126">支払頻度</span><span class="sxs-lookup"><span data-stu-id="23896-126">Pay frequencies</span></span>

<span data-ttu-id="23896-127">[支払頻度] は、従業員の賃金または給与の指定方法 (たとえば、1 時間あたり $10 対して 1 年間あたり $50,000) を定義し、時間単位、週単位、月単位 (12 カ月)、および年間レートの間の換算を定義するために使用します。</span><span class="sxs-lookup"><span data-stu-id="23896-127">**Pay frequencies** are used to define how an employee's wage or salary is being specified (for example $10 per hour versus $50,000 per year), and the conversion between the hourly, weekly, monthly (12 months), and annual rates.</span></span> <span data-ttu-id="23896-128">たとえば、時給の従業員に対して 38 時間の作業週を使用する会社は、時間レートが 1、週レートが 38、月レートが 164.6666666667、年レートが 1,976 の支払頻度を設定します。</span><span class="sxs-lookup"><span data-stu-id="23896-128">For example, a company that uses a 38-hour work week for its hourly employees sets up a pay frequency that has an hourly rate of 1, a weekly rate of 38, a monthly rate of 164.6666666667, and an annual rate of 1,976.</span></span> <span data-ttu-id="23896-129">これらの換算は、従業員の固定報酬レコードに表示されるさまざまな支払レートの計算に使用されます。</span><span class="sxs-lookup"><span data-stu-id="23896-129">These conversions are used to calculate the various pay rates that appear on an employee's fixed compensation record.</span></span>

## <a name="fixed-compensation-plans"></a><span data-ttu-id="23896-130">固定報酬プラン</span><span class="sxs-lookup"><span data-stu-id="23896-130">Fixed compensation plans</span></span>
<span data-ttu-id="23896-131">コンフィギュレーションしたすべてのコンポーネントを組み合わせた固定報酬プランを作成できます。</span><span class="sxs-lookup"><span data-stu-id="23896-131">You can design the fixed compensation plan to combine all the components that you've configured.</span></span> <span data-ttu-id="23896-132">固定報酬プランを作成するには、[固定報酬プラン] ページを開きます。</span><span class="sxs-lookup"><span data-stu-id="23896-132">To create a fixed compensation plan, open the **Fixed compensation plans** page.</span></span> <span data-ttu-id="23896-133">ここでは、プランに名前と説明を指定し、プランのタイプ (ステップ、等級、またはバンド) を選択し、従業員の支払レート (時給額、年収額など) に使用する支払頻度を選択し、報酬の処理方法を制御するオプションを設定できます。</span><span class="sxs-lookup"><span data-stu-id="23896-133">Here, you can give your plan a name and description, select what type of plan it is (step, grade, or band), select the pay frequency that you'll use for the employee's pay rate (amount per hour, amount per year, and so on), and set some options that control how compensation is processed.</span></span> 

<span data-ttu-id="23896-134">[許容範囲外] 設定では、報酬金額が必ず最小金額と最大金額の間にあるようにするための制限方法を指定できます。</span><span class="sxs-lookup"><span data-stu-id="23896-134">The **Out of range tolerance** setting lets you specify how strict you want to be about making sure that compensation amounts are between the minimum and maximum amounts.</span></span> <span data-ttu-id="23896-135">[ハード] 許容範囲では、指定したレベルのために定義した範囲内に報酬がある必要があります。</span><span class="sxs-lookup"><span data-stu-id="23896-135">A **Hard** tolerance requires that compensation be within the range that is defined for a given level.</span></span> <span data-ttu-id="23896-136">[ソフト] 許容範囲では、報酬額がその範囲に含まれない場合、警告が表示されますが、続行できます。</span><span class="sxs-lookup"><span data-stu-id="23896-136">A **Soft** tolerance alerts you when the compensation amount is outside the range but allows you to continue.</span></span> <span data-ttu-id="23896-137">許容範囲を [なし] に設定すると、警告またはエラー メッセージを受け取ることなしに、任意の従業員の報酬金額を入力できます。</span><span class="sxs-lookup"><span data-stu-id="23896-137">If you set the tolerance to **None**, you can enter any compensation amount for an employee without receiving warning or error messages.</span></span> 

<span data-ttu-id="23896-138">[採用ルール] 設定では、採用された日付に関係なく、すべての従業員が同じ昇給を受け取るかどうか (**採用ルール** = **なし**)、またはサイクル中の雇用期間に基づき、従業員がその割合の報酬を受け取るかどうか (**採用ルール** = **割合**) を指定します。</span><span class="sxs-lookup"><span data-stu-id="23896-138">The **Hire rule** setting lets you specify whether all employees should receive the same increase, regardless of the date that they were hired (**Hire rule** = **None**), or whether employees should receive a percentage of the award, based on how long they were employed during the cycle (**Hire rule** = **Percent**).</span></span> 

<span data-ttu-id="23896-139">**給与レンジ到達割合マトリックス**は、従業員がその範囲の平均に達するために必要な時間を減らす場合、または従業員がその範囲の最高額の基準点に達するために必要な時間を増やす場合に役立ちます。</span><span class="sxs-lookup"><span data-stu-id="23896-139">A **range utilization matrix** is useful if you want either to reduce the time that is required for employees to reach the midpoint of their range, or to increase the time that is required for employees to reach to the maximum reference point in the range.</span></span> <span data-ttu-id="23896-140">たとえば、範囲の 25% の下限にいる従業員には目標達成報酬の 110% を与えたいが、範囲の 25% の上限にいる従業員には、すぐに最高額に達するのを防ぐために、目標達成報酬の 80% のみを与えたい場合があります。</span><span class="sxs-lookup"><span data-stu-id="23896-140">For example, you want to give employees who are in the bottom 25 percent of their range 110 percent of their target award, but you want to give employees who are in the top 25 percent of their range only 80 percent of their target award, to prevent them from reaching the maximum as quickly.</span></span> 

<span data-ttu-id="23896-141">固定報酬プランの基礎となるデータを定義した後、プランの報酬構造を設定できます。</span><span class="sxs-lookup"><span data-stu-id="23896-141">After you define the basics of the fixed compensation plan, you can set up the compensation structure for the plan.</span></span> <span data-ttu-id="23896-142">[報酬の設定] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="23896-142">Click **Set up compensation**.</span></span> <span data-ttu-id="23896-143">次の 3 つのオプションを選択するダイアログのスライダーが開きます。</span><span class="sxs-lookup"><span data-stu-id="23896-143">A dialog slider opens that gives you three options:</span></span>

-   <span data-ttu-id="23896-144">基準点設定を選択し、グリッドに名前を付けることによって、新しい報酬グリッドを作成します。</span><span class="sxs-lookup"><span data-stu-id="23896-144">Create a new compensation grid by selecting a reference point setup and giving the grid a name.</span></span>
-   <span data-ttu-id="23896-145">開始点として使用できる既存のグリッドのコピーを作成することによって、新しい報酬グリッドを作成します。</span><span class="sxs-lookup"><span data-stu-id="23896-145">Create a new compensation grid by making a copy of an existing grid that you can use as a starting point.</span></span>
-   <span data-ttu-id="23896-146">既に定義済みの既存の報酬グリッドを使用します。</span><span class="sxs-lookup"><span data-stu-id="23896-146">Use an existing compensation grid that has already been defined.</span></span> <span data-ttu-id="23896-147">同じグリッドを使用するすべての報酬プランは、グリッドが変更されると更新が表示されます。</span><span class="sxs-lookup"><span data-stu-id="23896-147">All compensation plans that use the same grid receive updates if that grid is changed.</span></span>

<span data-ttu-id="23896-148">オプションの選択後、[報酬構造] ページが開き、新しい報酬グリッドまたは既存の報酬グリッドに変更を加えることができます。</span><span class="sxs-lookup"><span data-stu-id="23896-148">After you select an option, the **Compensation structure** page opens, and you can make changes to the new compensation grid or the existing compensation grid.</span></span>

## <a name="fixed-compensation-enrollment"></a><span data-ttu-id="23896-149">固定報酬登録</span><span class="sxs-lookup"><span data-stu-id="23896-149">Fixed compensation enrollment</span></span>
### <a name="determine-who-is-eligible-for-the-plan"></a><span data-ttu-id="23896-150">プランに適用できる人の決定</span><span class="sxs-lookup"><span data-stu-id="23896-150">Determine who is eligible for the plan</span></span>

<span data-ttu-id="23896-151">固定報酬プランに従業員を登録するための最初の手順は、プランに定義された報酬に適用できる人を決めることです。</span><span class="sxs-lookup"><span data-stu-id="23896-151">The first step in enrolling employees in a fixed compensation plan is to determine who is eligible for the compensation that is defined in the plan.</span></span> <span data-ttu-id="23896-152">適格性を決定するまで、各従業員にプランを割り当てることはできません。</span><span class="sxs-lookup"><span data-stu-id="23896-152">Until you determine eligibility, you won't be able to assign the plan to any employees.</span></span> <span data-ttu-id="23896-153">適格性を設定するには、[適格性ルール] ページを開きます。</span><span class="sxs-lookup"><span data-stu-id="23896-153">To set up eligibility, open the **Eligibility rules** page.</span></span> <span data-ttu-id="23896-154">ここで、報酬プランに新しい適格性ルールを作成し、従業員がプランに適用するために満たす必要がある基準を定義します。</span><span class="sxs-lookup"><span data-stu-id="23896-154">Here, you create a new eligibility rule for your compensation plan and define the criteria that an employee must meet to be eligible for a plan.</span></span> <span data-ttu-id="23896-155">部門、労働組合、報酬地域 (場所)、職務、職務権限、ジョブ タイプ、および報酬レベルに基づき、適格性を制限できます。</span><span class="sxs-lookup"><span data-stu-id="23896-155">You can limit eligibility based on department, labor union, compensation region (location), job, job function, job type, or compensation level.</span></span> <span data-ttu-id="23896-156">適格性ルールで設定されたすべての条件を満たす場合にのみ、従業員を報酬プランに登録できます。</span><span class="sxs-lookup"><span data-stu-id="23896-156">Employees can be enrolled in a compensation plan only if they meet all conditions that are set on the eligibility rule.</span></span> 

<span data-ttu-id="23896-157">**注記:** 適格性ルールは、固定報酬プランと変動報酬プランの両方の適格性の決定に使用できます。</span><span class="sxs-lookup"><span data-stu-id="23896-157">**Note:** Eligibility rules are used to determine eligibility for both fixed and variable compensation plans.</span></span> 

<span data-ttu-id="23896-158">従業員適格性ルールは、職務、職位、および従業員レコードの特定のフィールドの値を考慮し、
従業員が報酬プランに適用できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="23896-158">The eligibility rule considers the value of specific fields in the Job, Position, and Employee records to determine whether an employee is eligible for a compensation plan.</span></span>

-   <span data-ttu-id="23896-159">[ジョブ] ページでは、適格性ルールは、次のフィールドを考慮します。</span><span class="sxs-lookup"><span data-stu-id="23896-159">On the **Job** page, the eligibility rule considers the following fields:</span></span>
    -   <span data-ttu-id="23896-160">[ジョブ] フィールド</span><span class="sxs-lookup"><span data-stu-id="23896-160">The **Job** field</span></span>
    -   <span data-ttu-id="23896-161">[ジョブ分類] タブの [機能] フィールドと[ジョブ タイプ] フィールド</span><span class="sxs-lookup"><span data-stu-id="23896-161">On the **Job classification** tab, the **Function** and **Job type** fields</span></span>
    -   <span data-ttu-id="23896-162">[報酬] タブの [レベル] フィールド</span><span class="sxs-lookup"><span data-stu-id="23896-162">On the **Compensation** tab, the **Level** field</span></span>
-   <span data-ttu-id="23896-163">[職位] ページでは、適格性ルールは、[部門] フィールドと[報酬地域] フィールドを考慮します。</span><span class="sxs-lookup"><span data-stu-id="23896-163">On the **Positions** page, the eligibility rule considers the **Department** and **Compensation region** fields.</span></span>

<span data-ttu-id="23896-164">また、適格性ルールは、従業員に関連付けられている労働組合を考慮します ([従業員] ページの [作業員] タブで、[個人情報] &gt; [労働組合] をクリックします)。</span><span class="sxs-lookup"><span data-stu-id="23896-164">The eligibility rule also considers labor unions that are associated with the employee (on the **Employees** page, on the **Worker** tab, click **Personal information** &gt; **Labor unions**).</span></span>

### <a name="define-fixed-compensation-actions"></a><span data-ttu-id="23896-165">固定報酬アクションの定義</span><span class="sxs-lookup"><span data-stu-id="23896-165">Define fixed compensation actions</span></span>

<span data-ttu-id="23896-166">従業員の固定報酬を設定または変更する場合は、[固定報酬アクション] を使用します。</span><span class="sxs-lookup"><span data-stu-id="23896-166">**Fixed compensation actions** are used when you set or apply changes to an employee's fixed compensation.</span></span> <span data-ttu-id="23896-167">固定報酬アクションでは、報酬と給付金マネージャーが実行できるアクション タイプに内容を示す名前を指定することができます。</span><span class="sxs-lookup"><span data-stu-id="23896-167">Fixed compensation actions let you provide descriptive names for the types of actions that a Compensation and benefits manager can perform.</span></span> <span data-ttu-id="23896-168">さまざまなアクション タイプには、特別な論理が設定されているため、指定した時間に使用できます。</span><span class="sxs-lookup"><span data-stu-id="23896-168">Different action types have special logic behind them, so that they can be used at specific times.</span></span> 

<span data-ttu-id="23896-169">たとえば、固定報酬が従業員に設定されている場合、[雇用/再雇用] タイプのアクションのみ使用できます。</span><span class="sxs-lookup"><span data-stu-id="23896-169">For example, when the fixed compensation is set up for an employee, only actions that have a type of **Hire/Rehire** can be used.</span></span> <span data-ttu-id="23896-170">この場合、[雇用/再雇用] タイプの異なる 3 つのタイプを作成したいときには、それらのタイプに「採用」、「再雇用」、「異動」と名前を付けます。</span><span class="sxs-lookup"><span data-stu-id="23896-170">In this case, you might want to create three different actions of the **Hire/Rehire** type, and name them **Hire**, **Rehire**, and **Transfer**.</span></span> <span data-ttu-id="23896-171">固定報酬が従業員に支給された理由、または変更された理由をより詳しく示す説明を設定できます。</span><span class="sxs-lookup"><span data-stu-id="23896-171">You then have a more descriptive explanation of why the fixed compensation was given to an employee or changed.</span></span>

### <a name="enroll-the-employee"></a><span data-ttu-id="23896-172">従業員の登録</span><span class="sxs-lookup"><span data-stu-id="23896-172">Enroll the employee</span></span>

<span data-ttu-id="23896-173">固定報酬プランに、従業員を割り当てることができます。</span><span class="sxs-lookup"><span data-stu-id="23896-173">You can now assign an employee to a fixed compensation plan.</span></span> <span data-ttu-id="23896-174">[従業員] ページを開き、報酬プランに登録する従業員を選択します。</span><span class="sxs-lookup"><span data-stu-id="23896-174">Open the **Employees** page, and select the employee to enroll in the compensation plan.</span></span> <span data-ttu-id="23896-175">アクション ウィンドウで、[報酬] &gt; [固定プラン] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="23896-175">On the Action Pane, click **Compensation** &gt; **Fixed plan**.</span></span> <span data-ttu-id="23896-176">これで、その従業員の新しい固定報酬アクションを作成できます。</span><span class="sxs-lookup"><span data-stu-id="23896-176">You can now create a new fixed compensation action for that employee.</span></span> 

<span data-ttu-id="23896-177">**注記:** [報酬プラン] フィールドには、従業員が各プランに対して設定した適格性ルールに適用できるプランだけが表示されます。</span><span class="sxs-lookup"><span data-stu-id="23896-177">**Note:** The compensation plan field shows only the plans that an employee is eligible for under the eligibility rules that were set up for each plan.</span></span> <span data-ttu-id="23896-178">プランに適格性ルールが設定されていない場合は、プランに適用できる従業員はいません。</span><span class="sxs-lookup"><span data-stu-id="23896-178">If no eligibility rule is set up for a plan, no employees will be eligible for that plan.</span></span> 

<span data-ttu-id="23896-179">システムは、等級タイプまたはバンドのタイプの報酬プランに対して指定された報酬金額が、従業員の職務に指定された報酬レベルの最小および最大の基準点の範囲内であることを確認します。</span><span class="sxs-lookup"><span data-stu-id="23896-179">The system verifies that the compensation amount that is specified for a compensation plan of the grade or band type is within the minimum and maximum reference points for the given compensation level on the employee's job.</span></span> <span data-ttu-id="23896-180">報酬金額が許可範囲外の場合は、固定報酬プランで設定されている許容範囲レベルに応じて、警告メッセージまたはエラー メッセージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="23896-180">If the compensation amount is outside the allowed range, a warning or error message is displayed, depending on the tolerance level that is set on the fixed compensation plan.</span></span>

<a name="see-also"></a><span data-ttu-id="23896-181">参照</span><span class="sxs-lookup"><span data-stu-id="23896-181">See also</span></span>
--------

[<span data-ttu-id="23896-182">報酬プラン</span><span class="sxs-lookup"><span data-stu-id="23896-182">Compensation plans</span></span>](compensation-plans.md)




