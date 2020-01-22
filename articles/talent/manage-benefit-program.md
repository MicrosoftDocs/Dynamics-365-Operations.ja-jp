---
title: 給付金プログラムの定義および管理
description: 人事管理は、給付金、控除、および組織が作業者に対して提供または処理する作業者の報酬プランを設定および管理するのに使用できる一連のツールを提供します。 この記事は、管理された給付金を設定する方法に関する情報を提供します。
author: andreabichsel
manager: AnnBe
ms.date: 07/16/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: HcmBenefitEligibilityDetail, HcmBenefitSelection, SysPolicyListPage, SysPolicySourceDocumentRuleType
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations, Talent
ms.custom: 15681
ms.assetid: 6aee97ac-29f7-4b3c-8aa1-c65810de3090
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Talent July 2017 update
ms.openlocfilehash: 49901445f39a2e1c9541e5482d1b4c96550003a6
ms.sourcegitcommit: 871707a3fd236da693a3d51f401eb0cb9d4bae39
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/06/2019
ms.locfileid: "2898599"
---
# <a name="define-and-manage-a-benefits-program"></a><span data-ttu-id="e3df7-104">給付金プログラムの定義および管理</span><span class="sxs-lookup"><span data-stu-id="e3df7-104">Define and manage a benefits program</span></span>

<span data-ttu-id="e3df7-105">人事管理は、給付金、控除、および組織が作業者に対して提供または処理する作業者の報酬プランを設定および管理するのに使用できる一連のツールを提供します。</span><span class="sxs-lookup"><span data-stu-id="e3df7-105">Human resources provides a set of tools that can be used to set up and maintain benefits, deductions, and workers' compensation plans that an organization offers or processes for its workers.</span></span> <span data-ttu-id="e3df7-106">このトピックは、給付金を管理および設定する方法に関する情報を提供します。</span><span class="sxs-lookup"><span data-stu-id="e3df7-106">This topic provides information about how to set up and manage benefits.</span></span>

<a name="benefit-setup"></a><span data-ttu-id="e3df7-107">Benefit の設定</span><span class="sxs-lookup"><span data-stu-id="e3df7-107">Benefit setup</span></span>
-------------

<span data-ttu-id="e3df7-108">作業者を給付金に登録する前に、各給付金の要素を作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="e3df7-108">Before workers can be enrolled in benefits, you must create the elements of each benefit.</span></span> <span data-ttu-id="e3df7-109">これらの要素は同様の給付金計画を組み合わせて、控除割合と計算の詳細などの既定の設定を定義します。</span><span class="sxs-lookup"><span data-stu-id="e3df7-109">These elements combine similar benefit plans and define default settings, such as deduction rates and accounting details.</span></span> <span data-ttu-id="e3df7-110">これらの設定の多くは、作業者が給付金に後で登録されたときに調整できます。</span><span class="sxs-lookup"><span data-stu-id="e3df7-110">Many of these settings can be adjusted when workers are later enrolled in the benefit.</span></span> <span data-ttu-id="e3df7-111">各給付金計画に対して、組織が複数の登録オプションを提供するか、作業者が計画への登録を免除できます。</span><span class="sxs-lookup"><span data-stu-id="e3df7-111">For each benefit plan, an organization can offer several enrollment options, or a worker can waive enrollment in the plan.</span></span> 

<span data-ttu-id="e3df7-112">[![給付金プロセス フロー](./media/benefit-process-flow1.png)](./media/benefit-process-flow1.png)</span><span class="sxs-lookup"><span data-stu-id="e3df7-112">[![Benefit process flow](./media/benefit-process-flow1.png)](./media/benefit-process-flow1.png)</span></span>

## <a name="benefit-elements"></a><span data-ttu-id="e3df7-113">給付金の要素</span><span class="sxs-lookup"><span data-stu-id="e3df7-113">Benefit elements</span></span>

<span data-ttu-id="e3df7-114">給付金の作成を開始し、作業者を登録する前に、給付金を構成する要素、つまり、タイプ、計画およびオプションを定義する必要があります。</span><span class="sxs-lookup"><span data-stu-id="e3df7-114">Before you begin to create benefits and enroll workers in them, you must define the elements that make up a benefit: the type, plan, and options.</span></span>

-   <span data-ttu-id="e3df7-115">**タイプ** – 医療または駐車料金など、固有の給付金計画の集合。</span><span class="sxs-lookup"><span data-stu-id="e3df7-115">**Type** – A collection of plans for a specific benefit, such as medical or parking.</span></span>
-   <span data-ttu-id="e3df7-116">**計画** – 業者との契約による固有の給付金。</span><span class="sxs-lookup"><span data-stu-id="e3df7-116">**Plan** – A specific benefit that is contracted from a provider.</span></span>
-   <span data-ttu-id="e3df7-117">**オプション** – 従業員のみまたは従業員と配偶者/パートナーなどの補償範囲レベル。</span><span class="sxs-lookup"><span data-stu-id="e3df7-117">**Option** – The coverage level, such as employee only, or employee and spouse/partner.</span></span>

<span data-ttu-id="e3df7-118">視力または歯科などの各給付金のタイプごとに、組織は作業者に複数の計画を提供できます。</span><span class="sxs-lookup"><span data-stu-id="e3df7-118">For each type of benefit, such as vision or dental, an organization can offer one or more plans to its workers.</span></span> <span data-ttu-id="e3df7-119">各計画ごとに、組織はさまざまなオプションを提供できます。</span><span class="sxs-lookup"><span data-stu-id="e3df7-119">For each plan, the organization can offer different options.</span></span> <span data-ttu-id="e3df7-120">たとえば、作業者は年間の給与から、1 回 2 回または 3 回追加の定期生命保険の補充を購入できます。</span><span class="sxs-lookup"><span data-stu-id="e3df7-120">For example, workers can buy additional term life insurance coverage at one, two, or three times their yearly salary.</span></span> <span data-ttu-id="e3df7-121">計画とオプションの各組み合わせが、作業者が登録する給付金になります。</span><span class="sxs-lookup"><span data-stu-id="e3df7-121">Each combination of a plan and options becomes a benefit that workers can enroll in.</span></span> 

<span data-ttu-id="e3df7-122">[![給付金の図](./media/benefit-pic.png)](./media/benefit-pic.png)</span><span class="sxs-lookup"><span data-stu-id="e3df7-122">[![benefit pic](./media/benefit-pic.png)](./media/benefit-pic.png)</span></span>

## <a name="eligibility"></a><span data-ttu-id="e3df7-123">適格性</span><span class="sxs-lookup"><span data-stu-id="e3df7-123">Eligibility</span></span>
<span data-ttu-id="e3df7-124">さまざまな要因により、雇用主が提供する給付金のさまざまなタイプに対する作業者の適格性が決定します。</span><span class="sxs-lookup"><span data-stu-id="e3df7-124">Many factors determine worker eligibility for the various types of benefits that an employer offers.</span></span> <span data-ttu-id="e3df7-125">Dynamics 365 Talent を使用して給付金を作成すると、その給付金が適用される適格性のタイプを設定できます。</span><span class="sxs-lookup"><span data-stu-id="e3df7-125">When you create a benefit in Dynamics 365 Talent, you can set the type of eligibility that applies to that benefit.</span></span> 

<span data-ttu-id="e3df7-126">すべての作業者が給付金を使用できるようにすることができます。</span><span class="sxs-lookup"><span data-stu-id="e3df7-126">You can make a benefit available to all workers.</span></span> <span data-ttu-id="e3df7-127">たとえば、一部の会社では、駐車許可証を付加給付としてすべての従業員に提供します。</span><span class="sxs-lookup"><span data-stu-id="e3df7-127">For example, some companies offer parking passes to all employees as a fringe benefit.</span></span> <span data-ttu-id="e3df7-128">この給付金を作成する場合、**すべての作業者が適格** である適格性として設定します。</span><span class="sxs-lookup"><span data-stu-id="e3df7-128">When you create this benefit, you set the eligibility to **All workers are eligible**.</span></span> 

<span data-ttu-id="e3df7-129">債権差し押さえ、および税徴収の処理などの他の給付金については、適格性は適用されません。</span><span class="sxs-lookup"><span data-stu-id="e3df7-129">For other benefits, such as garnishments and tax levies, eligibility doesn't apply.</span></span> <span data-ttu-id="e3df7-130">これらのタイプの給付金を作成する場合、**適格性処理のバイパス**として適格性を設定します。</span><span class="sxs-lookup"><span data-stu-id="e3df7-130">Whey you create these types of benefits, you set the eligibility to **Bypass eligibility process**.</span></span> 

<span data-ttu-id="e3df7-131">最後に、福利厚生の適格性はルールに基づいています。</span><span class="sxs-lookup"><span data-stu-id="e3df7-131">Finally, benefit eligibility can be rule-based.</span></span> <span data-ttu-id="e3df7-132">たとえばある会社が、従業員に生命保険の給付金の 2 つのタイプを提供するとします。</span><span class="sxs-lookup"><span data-stu-id="e3df7-132">For example, a company offers two types of life insurance benefit to employees.</span></span> <span data-ttu-id="e3df7-133">経営幹部の従業員は、1 つの生命保険プランの適格性がありますが、他のすべてのフルタイム従業員は他の生命保険プランの適格性があります。</span><span class="sxs-lookup"><span data-stu-id="e3df7-133">Executive employees are eligible for one life insurance plan, whereas all other full-time employees are eligible for the other life insurance plan.</span></span> <span data-ttu-id="e3df7-134">Talent では、すべての経営幹部の従業員を検索する適格性ルール、また他のすべてのフルタイム従業員を検索する適格性ルールを作成でき、次に適切な給付金にそれらのルールを適用します。</span><span class="sxs-lookup"><span data-stu-id="e3df7-134">In Talent, you can create a benefit eligibility rule to find all executive employees and another rule to find all other full-time employees, and then apply those rules to the appropriate benefit.</span></span>

## <a name="enrollment"></a><span data-ttu-id="e3df7-135">登録</span><span class="sxs-lookup"><span data-stu-id="e3df7-135">Enrollment</span></span>
<span data-ttu-id="e3df7-136">組織が提供する給付金を作成し、適格性を決定した後に、作業者を給付金に登録します。</span><span class="sxs-lookup"><span data-stu-id="e3df7-136">After you've created the benefits that your organization offers and determined eligibility, you can enroll your workers in benefits.</span></span> <span data-ttu-id="e3df7-137">給付金に 1 人の作業者を登録する、または単一のプロセス中に 1 つまたは複数の給付金に多数の作業者を登録できます。</span><span class="sxs-lookup"><span data-stu-id="e3df7-137">You can enroll a single worker in benefits, or you can enroll many workers in one or more benefits during a single process.</span></span> 

<span data-ttu-id="e3df7-138">場合によっては、組織は特定の給付金の提供を停止します。</span><span class="sxs-lookup"><span data-stu-id="e3df7-138">Sometimes, an organization stops offering certain benefits.</span></span> <span data-ttu-id="e3df7-139">この場合、給付金および登録されている作業者を更新する必要があります。</span><span class="sxs-lookup"><span data-stu-id="e3df7-139">In this case, you must update the benefit and the workers who are enrolled in.</span></span> <span data-ttu-id="e3df7-140">給付金有効期限一括設定により、給付金の有効期限とその給付金に登録している作業者の登録の有効期限両方を一括で変更することができます。</span><span class="sxs-lookup"><span data-stu-id="e3df7-140">Mass benefit expiration lets you change the expiration date of both a benefit and the worker enrollments for that benefit at the same time.</span></span> <span data-ttu-id="e3df7-141">給付金に登録されている複数の作業者を選択し、それらの補償の終了日を変更することもできます。</span><span class="sxs-lookup"><span data-stu-id="e3df7-141">You can also select multiple workers who are enrolled in a benefit and change the ending date of their coverage.</span></span> 

<span data-ttu-id="e3df7-142">同様に、給付金の一括延長により、当初計画していた期間より長く給付金を提供すると決定した場合に、給付金およびその給付金に登録されている作業者両方の有効期限を同時に延長できます。</span><span class="sxs-lookup"><span data-stu-id="e3df7-142">Similarly, mass benefit extension lets you extend the expiration date of both a benefit and the worker enrollments for that benefit if you decide to offer a benefit longer than you originally planned.</span></span>

<a name="additional-resources"></a><span data-ttu-id="e3df7-143">その他のリソース</span><span class="sxs-lookup"><span data-stu-id="e3df7-143">Additional resources</span></span>
--------

[<span data-ttu-id="e3df7-144">給付金の適格性ポリシー</span><span class="sxs-lookup"><span data-stu-id="e3df7-144">Benefit eligibility policies</span></span>](benefit-eligibility-policies.md)



