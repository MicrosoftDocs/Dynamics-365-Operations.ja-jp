---
title: "経費管理の構成"
description: "この記事は、Microsoft Dynamics 365 for Finance and Operations、Enterprise エディションの経費管理をコンフィギュレーションする前に、計画プロセス中に決定する必要のある考慮事項について説明します。"
author: KimANelson
manager: AnnBe
ms.date: 08/29/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: GlobalCategory, ProjCategory, TrvLocations, TrvParameters, TrvPaymethod, TrvPerDiems
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 23001
ms.assetid: aa3fd14d-7e94-4603-985f-ca26d6f860ea
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 4fad62c5da11e88e07f4e9d4343c4ac1a487bdd8
ms.contentlocale: ja-jp
ms.lasthandoff: 11/03/2017

---

# <a name="configure-expense-management"></a><span data-ttu-id="0fa5d-103">経費管理の構成</span><span class="sxs-lookup"><span data-stu-id="0fa5d-103">Configure expense management</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="0fa5d-104">このトピックは、Microsoft Dynamics 365 for Finance and Operations、Enterprise エディションの経費管理をコンフィギュレーションする前に、計画プロセス中に決定する必要のある考慮事項について説明します。</span><span class="sxs-lookup"><span data-stu-id="0fa5d-104">This topic describes the considerations and the decisions that you must make during the planning process before you configure Expense management in Microsoft Dynamics 365 for Finance and Operations, Enterprise edition.</span></span> <span data-ttu-id="0fa5d-105">[経費管理] で、支払方法、出張費要求、経費精算書、ポリシーなどの情報を格納できます。</span><span class="sxs-lookup"><span data-stu-id="0fa5d-105">In Expense management, you can store information about payment methods, travel requisitions, expense reports, policies, and so on.</span></span>

<span data-ttu-id="0fa5d-106">経費管理に対するコンフィギュレーションを計画する場合の決定の多くが、組織の階層と財務構造に基づいているため、これらの領域の計画文書を参照する必要があります。</span><span class="sxs-lookup"><span data-stu-id="0fa5d-106">Because many of the decisions that you make when you plan your configuration for Expense management are based on your organization’s hierarchy and financial structure, you must refer to the planning documents for those areas.</span></span>

## <a name="intercompany-expenses"></a><span data-ttu-id="0fa5d-107">会社間経費</span><span class="sxs-lookup"><span data-stu-id="0fa5d-107">Intercompany expenses</span></span>

<span data-ttu-id="0fa5d-108">会社間経費を有効にすると、別の法人に代わって法人や従業員が経費を支払ったり、組織内の雇用法人から支払を回収したりできます。</span><span class="sxs-lookup"><span data-stu-id="0fa5d-108">When you enable intercompany expenses, you allow legal entities and employees to incur expenses on behalf of another legal entity, and collect payment from the legal entity of employment within your organization.</span></span> <span data-ttu-id="0fa5d-109">たとえば、法人 A に属する従業員が法人 B のプロジェクトを完了し、そのプロジェクトには出張関連経費が発生するとします。</span><span class="sxs-lookup"><span data-stu-id="0fa5d-109">For example, an employee in legal entity A completes a project for legal entity B, and the project incurs travel related expenses.</span></span> <span data-ttu-id="0fa5d-110">会社間経費が有効な場合、従業員は法人 B へ転記する経費の経費精算書をまとめ、その経費は法人 A により支払われる必要があります。組織に複数の法人がない場合、会社間経費を有効にする必要はありません。</span><span class="sxs-lookup"><span data-stu-id="0fa5d-110">If intercompany expenses are enabled, the employee can then file an expense report that will post the expense to legal entity B, and the expense must then be paid by legal entity A. If your organization doesn’t have multiple legal entities, you don’t have to enable intercompany expenses.</span></span>

<span data-ttu-id="0fa5d-111">**意思決定:** 会社間経費を有効にしますか。</span><span class="sxs-lookup"><span data-stu-id="0fa5d-111">**Decision:** Do you want to enable intercompany expenses?</span></span>

## <a name="financial-management"></a><span data-ttu-id="0fa5d-112">財務管理</span><span class="sxs-lookup"><span data-stu-id="0fa5d-112">Financial management</span></span>

<span data-ttu-id="0fa5d-113">経費管理は、組織の財務管理と密に統合されています。</span><span class="sxs-lookup"><span data-stu-id="0fa5d-113">Expense management is tightly integrated with the financial management of your organization.</span></span> <span data-ttu-id="0fa5d-114">経費管理の多くのコンフィギュレーションは、組織の財務に関する決定に基づいています。</span><span class="sxs-lookup"><span data-stu-id="0fa5d-114">Lots of your configuration for Expense management will be based on the decisions that you’ve made about your organization’s finances.</span></span> <span data-ttu-id="0fa5d-115">次のセクションでは、組織の財務上の決定および指導チームからのガイダンスに基づく、計画および決定が必要になるさまざまな領域について説明します。</span><span class="sxs-lookup"><span data-stu-id="0fa5d-115">The following sections describe the various areas that require planning and decisions, based on your organization’s financial decisions and guidance from your leadership team.</span></span>

### <a name="per-diems"></a><span data-ttu-id="0fa5d-116">日当</span><span class="sxs-lookup"><span data-stu-id="0fa5d-116">Per diems</span></span>

<span data-ttu-id="0fa5d-117">組織で提供する日当の従業員を定義する必要があります。</span><span class="sxs-lookup"><span data-stu-id="0fa5d-117">You must define the employee per diems that your organization provides.</span></span> <span data-ttu-id="0fa5d-118">日当は通常、食費、宿泊費、その他の臨時費などの経費を負担するために使用されるため、組織が提供する日当ルールを作成できます。</span><span class="sxs-lookup"><span data-stu-id="0fa5d-118">Because per diems are typically used to cover expenses such as meals, lodging, and other incidental expenses, you can create rules for the per diem allowances that your organization offers.</span></span> <span data-ttu-id="0fa5d-119">日当レートは、時期、出張先、または両方を基準にされます。</span><span class="sxs-lookup"><span data-stu-id="0fa5d-119">per diem rates can be based on the time of year, the travel location, or both.</span></span> <span data-ttu-id="0fa5d-120">日当ルールを定義する際に、作業者が無料の食事やサービスを受ける場合、日当レートから天引される割合を指定できます。</span><span class="sxs-lookup"><span data-stu-id="0fa5d-120">When you define a per diem rule, you can specify that a percentage of the per diem rate will be withheld if a worker receives complimentary meals or services.</span></span> <span data-ttu-id="0fa5d-121">作業員の出張に適用できる日当レートの最大時間数と最小時間数を設定するために日当レート層を定義することもできます。</span><span class="sxs-lookup"><span data-stu-id="0fa5d-121">You can also define per diem rate tiers to set the minimum and maximum number of hours that the per diem rate can be applied to a worker’s travel.</span></span>

<span data-ttu-id="0fa5d-122">**意思決定:**</span><span class="sxs-lookup"><span data-stu-id="0fa5d-122">**Decisions:**</span></span>

- <span data-ttu-id="0fa5d-123">最初と最後の日の既定の日当ルール:</span><span class="sxs-lookup"><span data-stu-id="0fa5d-123">Default per diem rules for the first and last days:</span></span>

    - <span data-ttu-id="0fa5d-124">従業員が 1 日に要求し、日当を受け取る最小時間数はどのくらいですか。</span><span class="sxs-lookup"><span data-stu-id="0fa5d-124">What is the minimum number of hours that an employee can claim for a day and still receive a per diem?</span></span>
    - <span data-ttu-id="0fa5d-125">最初と最後の日の食事のために支給される金額に減額はありますか。</span><span class="sxs-lookup"><span data-stu-id="0fa5d-125">Is there a reduction in the amount that is offered for meals for the first day and last day?</span></span> <span data-ttu-id="0fa5d-126">減額がある場合、減額の割合はどのくらいですか。</span><span class="sxs-lookup"><span data-stu-id="0fa5d-126">If there is a reduction, what is the percentage of the reduction?</span></span>
    - <span data-ttu-id="0fa5d-127">最初と最後の日のホテルのために支給される金額に減額はありますか。</span><span class="sxs-lookup"><span data-stu-id="0fa5d-127">Is there a reduction in the amount that is offered for a hotel for the first day and last day?</span></span> <span data-ttu-id="0fa5d-128">減額がある場合、減額の割合はどのくらいですか。</span><span class="sxs-lookup"><span data-stu-id="0fa5d-128">If there is a reduction, what is the percentage of the reduction?</span></span>
    - <span data-ttu-id="0fa5d-129">最初と最後の日にかかるその他の経費に支給される金額に減額はありますか。</span><span class="sxs-lookup"><span data-stu-id="0fa5d-129">Is there a reduction in the amount that is offered for other expenses that are incurred on the first day and last day?</span></span> <span data-ttu-id="0fa5d-130">減額がある場合、減額の割合はどのくらいですか。</span><span class="sxs-lookup"><span data-stu-id="0fa5d-130">If there is a reduction, what is the percentage of the reduction?</span></span>

- <span data-ttu-id="0fa5d-131">既定の日当ルール:</span><span class="sxs-lookup"><span data-stu-id="0fa5d-131">Default per diem rules:</span></span>

    - <span data-ttu-id="0fa5d-132">食事が無料の場合などの食事に関する日当に割合での減額はありますか。</span><span class="sxs-lookup"><span data-stu-id="0fa5d-132">Is there a percentage reduction in the per diem allowance for each meal if, for example, the meal is complimentary?</span></span> <span data-ttu-id="0fa5d-133">減額がある場合、食事ごとの減額の割合はどのくらいですか。</span><span class="sxs-lookup"><span data-stu-id="0fa5d-133">If there is a reduction, what is the reduction percentage for each meal?</span></span>
    - <span data-ttu-id="0fa5d-134">1 日あたり、出張あたり、または 1 日あたりの食事数で計算される食費減額はありますか。</span><span class="sxs-lookup"><span data-stu-id="0fa5d-134">Is the meal reduction calculated per day, per trip, or by the number of meals per day?</span></span>
    - <span data-ttu-id="0fa5d-135">日当金額は通常どおりに丸められますか。または切り上げられますか。</span><span class="sxs-lookup"><span data-stu-id="0fa5d-135">Should per diem amounts be rounded in the regular manner or rounded up?</span></span>
    - <span data-ttu-id="0fa5d-136">日当は、24 時間制期間またはカレンダー日に基づいて計算しますか。</span><span class="sxs-lookup"><span data-stu-id="0fa5d-136">Are per diems calculated on a 24-hour period or on a calendar day?</span></span>

- <span data-ttu-id="0fa5d-137">場所に基づく日当ルール:</span><span class="sxs-lookup"><span data-stu-id="0fa5d-137">Per diem rules that are based on location:</span></span>

    - <span data-ttu-id="0fa5d-138">日当レートは場所に応じて異なりますか。</span><span class="sxs-lookup"><span data-stu-id="0fa5d-138">Do per diem rates vary according to location?</span></span> <span data-ttu-id="0fa5d-139">どのような場所が含まれますか。</span><span class="sxs-lookup"><span data-stu-id="0fa5d-139">What locations are included?</span></span>
    - <span data-ttu-id="0fa5d-140">日当レートが場所ごとの所在地に応じて変化する場合、次の経費タイプに対する割合率が用意されています。</span><span class="sxs-lookup"><span data-stu-id="0fa5d-140">If per diem rates vary according to location, for each location, what percentage amount is provided for the following types of expenses:</span></span>

        - <span data-ttu-id="0fa5d-141">食費</span><span class="sxs-lookup"><span data-stu-id="0fa5d-141">Meals</span></span>
        - <span data-ttu-id="0fa5d-142">ホテル</span><span class="sxs-lookup"><span data-stu-id="0fa5d-142">Hotel</span></span>
        - <span data-ttu-id="0fa5d-143">その他の経費</span><span class="sxs-lookup"><span data-stu-id="0fa5d-143">Other expenses</span></span>

### <a name="expense-management-journals-and-accounts"></a><span data-ttu-id="0fa5d-144">経費管理仕訳帳および勘定</span><span class="sxs-lookup"><span data-stu-id="0fa5d-144">Expense management journals and accounts</span></span>

<span data-ttu-id="0fa5d-145">経費管理には、複数の仕訳帳および勘定を使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="0fa5d-145">Expense management requires that you use multiple journals and accounts.</span></span> <span data-ttu-id="0fa5d-146">たとえば、同じ勘定を、現金前貸しとクレジット カードの争議に使用するかどうか決定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="0fa5d-146">You must decide, for example, whether the same account is used for cash advances and credit card disputes.</span></span>

<span data-ttu-id="0fa5d-147">**意思決定:**</span><span class="sxs-lookup"><span data-stu-id="0fa5d-147">**Decisions:**</span></span>

- <span data-ttu-id="0fa5d-148">どの仕訳元帳に承認済経費精算書を転記しますか。</span><span class="sxs-lookup"><span data-stu-id="0fa5d-148">Which ledger journal are approved expense reports posted to?</span></span>
- <span data-ttu-id="0fa5d-149">どの勘定を現金前貸しに使用しますか。</span><span class="sxs-lookup"><span data-stu-id="0fa5d-149">Which account is used for cash advances?</span></span>
- <span data-ttu-id="0fa5d-150">現金前貸しをすぐに転記しますか。</span><span class="sxs-lookup"><span data-stu-id="0fa5d-150">Should cash advances be posted immediately?</span></span>

### <a name="payment-methods"></a><span data-ttu-id="0fa5d-151">支払方法</span><span class="sxs-lookup"><span data-stu-id="0fa5d-151">Payment methods</span></span>

<span data-ttu-id="0fa5d-152">従業員が業務のために経費を支払うことを許可するときに、従業員が使用できる支払方法を定義する必要があります。</span><span class="sxs-lookup"><span data-stu-id="0fa5d-152">When you allow employees to incur expenses on behalf of your business, you must define the payment methods that employees are allowed to use.</span></span> <span data-ttu-id="0fa5d-153">たとえば、従業員による現金または会社のクレジット カードの使用を許可することができます。</span><span class="sxs-lookup"><span data-stu-id="0fa5d-153">For example, you might allow employees to use cash or a corporate credit card.</span></span> <span data-ttu-id="0fa5d-154">また、従業員が個人のクレジット カードを使用して、後で払い戻すようにすることもできます。</span><span class="sxs-lookup"><span data-stu-id="0fa5d-154">You might also allow employees to use personal credit cards, and then reimburse the employees.</span></span> <span data-ttu-id="0fa5d-155">許可する各支払方法に次の意思決定を行う必要があります。</span><span class="sxs-lookup"><span data-stu-id="0fa5d-155">You must make the following decisions for each payment method that you allow.</span></span>

<span data-ttu-id="0fa5d-156">**意思決定:**</span><span class="sxs-lookup"><span data-stu-id="0fa5d-156">**Decisions:**</span></span>

- <span data-ttu-id="0fa5d-157">どの支払方法を許可しますか。</span><span class="sxs-lookup"><span data-stu-id="0fa5d-157">What payment methods are allowed?</span></span>
- <span data-ttu-id="0fa5d-158">誰が支払方法の経費を所持しますか。</span><span class="sxs-lookup"><span data-stu-id="0fa5d-158">Who owns the payment method expenses?</span></span>
- <span data-ttu-id="0fa5d-159">相手勘定タイプはありますか。</span><span class="sxs-lookup"><span data-stu-id="0fa5d-159">Is there an offset account type?</span></span> <span data-ttu-id="0fa5d-160">相手勘定タイプがある場合、それは何ですか。</span><span class="sxs-lookup"><span data-stu-id="0fa5d-160">If there is an offset account type, what is it?</span></span>
- <span data-ttu-id="0fa5d-161">相手勘定がある場合、勘定は何ですか。</span><span class="sxs-lookup"><span data-stu-id="0fa5d-161">If there is an offset account, what is the account?</span></span>
- <span data-ttu-id="0fa5d-162">支払方法がクレジット カードである場合、その支払方法をインポートされたトランザクションでのみ使用しますか。</span><span class="sxs-lookup"><span data-stu-id="0fa5d-162">If the payment method is a credit card, should the payment method be used only with imported transactions?</span></span>

### <a name="expense-categories-and-shared-categories"></a><span data-ttu-id="0fa5d-163">経費カテゴリおよび共有カテゴリ</span><span class="sxs-lookup"><span data-stu-id="0fa5d-163">Expense categories and shared categories</span></span>

<span data-ttu-id="0fa5d-164">従業員が経費精算書を作成する際、記録する各費用は経費カテゴリと関連付けている必要があります。</span><span class="sxs-lookup"><span data-stu-id="0fa5d-164">When employees create an expense report, each expense that they record must be associated with an expense category.</span></span> <span data-ttu-id="0fa5d-165">経費カテゴリは、組織の法人間で共有できる共有カテゴリから取得されます。</span><span class="sxs-lookup"><span data-stu-id="0fa5d-165">Expense categories are derived from shared categories that can be shared across the legal entities in your organization.</span></span> <span data-ttu-id="0fa5d-166">これらのカテゴリは、組織の定義方法に応じて、プロジェクト管理および会計で共有することもできます。</span><span class="sxs-lookup"><span data-stu-id="0fa5d-166">These categories can also be shared in Project management and accounting, depending on the way that your organization is defined.</span></span> <span data-ttu-id="0fa5d-167">組織の定義および実装チームからのガイダンスに基づいて、[経費管理] に使用するカテゴリは [経費管理] のみで使用するか、または [プロジェクト管理と会計] および [経費管理] との間で共有する必要があるかを決定します。</span><span class="sxs-lookup"><span data-stu-id="0fa5d-167">Based on the definition of your organization and guidance from the implementation team, determine whether the categories that are used in Expense management will be used only in Expense management, or whether they should be shared between Project management and accounting and Expense management.</span></span> <span data-ttu-id="0fa5d-168">これらのカテゴリは、プロジェクトと経費、またはプロジェクトと運用の間で共有できますが、経費と運用の間では共有できないことに注意してください。</span><span class="sxs-lookup"><span data-stu-id="0fa5d-168">Note that these categories can be shared between Project and Expense or Project and Production, but not between Expense and Production.</span></span> <span data-ttu-id="0fa5d-169">各経費カテゴリに対して次の意思決定を行う必要があります。</span><span class="sxs-lookup"><span data-stu-id="0fa5d-169">You must make the following decisions for each expense category.</span></span>

<span data-ttu-id="0fa5d-170">**意思決定:**</span><span class="sxs-lookup"><span data-stu-id="0fa5d-170">**Decisions:**</span></span>

- <span data-ttu-id="0fa5d-171">経費カテゴリは何ですか。</span><span class="sxs-lookup"><span data-stu-id="0fa5d-171">What is the expense category?</span></span> <span data-ttu-id="0fa5d-172">この例には、フライト、ホテル、またはマイレージのカテゴリが含まれます。</span><span class="sxs-lookup"><span data-stu-id="0fa5d-172">Examples include categories for flights, hotel, or mileage.</span></span>
- <span data-ttu-id="0fa5d-173">経費カテゴリは、プロジェクト管理および会計でも使用できますか。</span><span class="sxs-lookup"><span data-stu-id="0fa5d-173">Can the expense category also be used in Project management and accounting?</span></span>
- <span data-ttu-id="0fa5d-174">経費タイプは何ですか。</span><span class="sxs-lookup"><span data-stu-id="0fa5d-174">What is the expense type?</span></span>
- <span data-ttu-id="0fa5d-175">経費カテゴリの既定の支払方法は何ですか。</span><span class="sxs-lookup"><span data-stu-id="0fa5d-175">What is the default payment method for the expense category?</span></span>
- <span data-ttu-id="0fa5d-176">経費カテゴリの経費を明細化する必要はありますか。</span><span class="sxs-lookup"><span data-stu-id="0fa5d-176">Do expenses in the expense category have to be itemized?</span></span>
- <span data-ttu-id="0fa5d-177">経費カテゴリに対するメインの既定の勘定は何ですか。</span><span class="sxs-lookup"><span data-stu-id="0fa5d-177">What is the main default account for the expense category?</span></span>
- <span data-ttu-id="0fa5d-178">経費カテゴリに対する既定の品目売上税グループは何ですか。</span><span class="sxs-lookup"><span data-stu-id="0fa5d-178">What is the default item sales tax group for the expense category?</span></span>
- <span data-ttu-id="0fa5d-179">この経費カテゴリに対して許可されている追加の支払方法はありますか。</span><span class="sxs-lookup"><span data-stu-id="0fa5d-179">Are additional payment methods allowed for the expense category?</span></span> <span data-ttu-id="0fa5d-180">追加の支払方法が許可されている場合、どんな方法がありますか。</span><span class="sxs-lookup"><span data-stu-id="0fa5d-180">If additional payment methods are allowed, what are they?</span></span>
- <span data-ttu-id="0fa5d-181">この経費カテゴリ内に下位カテゴリはありますか。</span><span class="sxs-lookup"><span data-stu-id="0fa5d-181">Are there subcategories in this expense category?</span></span> <span data-ttu-id="0fa5d-182">下位カテゴリがある場合、次の決定をする必要があります。</span><span class="sxs-lookup"><span data-stu-id="0fa5d-182">If there are subcategories, you must also make the following decisions:</span></span>

    - <span data-ttu-id="0fa5d-183">過誤納税の還付から除外される下位カテゴリはありますか。</span><span class="sxs-lookup"><span data-stu-id="0fa5d-183">Are any of the subcategories excluded from tax recovery?</span></span>
    - <span data-ttu-id="0fa5d-184">下位カテゴリの品目売上税グループは何ですか。</span><span class="sxs-lookup"><span data-stu-id="0fa5d-184">What is the item sales tax group of the subcategories?</span></span>

<span data-ttu-id="0fa5d-185">経費カテゴリがプロジェクト管理および会計でも使用されている場合、残りの質問にご回答ください。</span><span class="sxs-lookup"><span data-stu-id="0fa5d-185">If the expense category is also used in Project management and accounting, answer the remaining questions.</span></span> <span data-ttu-id="0fa5d-186">それ以外の場合は、次のセクションに移動します。</span><span class="sxs-lookup"><span data-stu-id="0fa5d-186">Otherwise, move on to the next section.</span></span>

- <span data-ttu-id="0fa5d-187">次の経費にどの原価勘定を使用しますか。</span><span class="sxs-lookup"><span data-stu-id="0fa5d-187">Which cost accounts will be used for the following expenses?</span></span>

    - <span data-ttu-id="0fa5d-188">コスト</span><span class="sxs-lookup"><span data-stu-id="0fa5d-188">Cost</span></span>
    - <span data-ttu-id="0fa5d-189">給与配賦</span><span class="sxs-lookup"><span data-stu-id="0fa5d-189">Payroll allocation</span></span>
    - <span data-ttu-id="0fa5d-190">仕掛品 - 原価価値</span><span class="sxs-lookup"><span data-stu-id="0fa5d-190">WIP-cost value</span></span>
    - <span data-ttu-id="0fa5d-191">原価 - 品目</span><span class="sxs-lookup"><span data-stu-id="0fa5d-191">Cost-item</span></span>
    - <span data-ttu-id="0fa5d-192">仕掛品 - 原価価値 - 品目</span><span class="sxs-lookup"><span data-stu-id="0fa5d-192">WIP-cost value-item</span></span>
    - <span data-ttu-id="0fa5d-193">未収損益</span><span class="sxs-lookup"><span data-stu-id="0fa5d-193">Accrued loss</span></span>
    - <span data-ttu-id="0fa5d-194">仕掛品 - 未収損失</span><span class="sxs-lookup"><span data-stu-id="0fa5d-194">WIP-accrued loss</span></span>

- <span data-ttu-id="0fa5d-195">次のものにどの収益勘定を使用しますか。</span><span class="sxs-lookup"><span data-stu-id="0fa5d-195">Which revenue accounts will be used for the following?</span></span>

    - <span data-ttu-id="0fa5d-196">請求済み収益</span><span class="sxs-lookup"><span data-stu-id="0fa5d-196">Invoiced revenue</span></span>
    - <span data-ttu-id="0fa5d-197">未収収益 - 販売額</span><span class="sxs-lookup"><span data-stu-id="0fa5d-197">Accrued revenue-sales value</span></span>
    - <span data-ttu-id="0fa5d-198">仕掛品 - 販売額</span><span class="sxs-lookup"><span data-stu-id="0fa5d-198">WIP-sales value</span></span>
    - <span data-ttu-id="0fa5d-199">未収収益 - 生産</span><span class="sxs-lookup"><span data-stu-id="0fa5d-199">Accrued revenue-production</span></span>
    - <span data-ttu-id="0fa5d-200">仕掛品 - 生産</span><span class="sxs-lookup"><span data-stu-id="0fa5d-200">WIP-production</span></span>
    - <span data-ttu-id="0fa5d-201">未収収益 - 利益</span><span class="sxs-lookup"><span data-stu-id="0fa5d-201">Accrued revenue-profit</span></span>
    - <span data-ttu-id="0fa5d-202">仕掛品 - 利益</span><span class="sxs-lookup"><span data-stu-id="0fa5d-202">WIP-profit</span></span>
    - <span data-ttu-id="0fa5d-203">未収収益 - 定期売買</span><span class="sxs-lookup"><span data-stu-id="0fa5d-203">Accrued revenue-subscription</span></span>
    - <span data-ttu-id="0fa5d-204">仕掛品 - 定期売買</span><span class="sxs-lookup"><span data-stu-id="0fa5d-204">WIP-subscription</span></span>

### <a name="taxes"></a><span data-ttu-id="0fa5d-205">税</span><span class="sxs-lookup"><span data-stu-id="0fa5d-205">Taxes</span></span>

<span data-ttu-id="0fa5d-206">経費に関係する税の場合、経費精算書に含まれるものや有効なものを判断する必要があります。</span><span class="sxs-lookup"><span data-stu-id="0fa5d-206">For expense-related taxes, you must determine what is included or enabled on expense reports.</span></span>

<span data-ttu-id="0fa5d-207">**意思決定:**</span><span class="sxs-lookup"><span data-stu-id="0fa5d-207">**Decisions:**</span></span>

- <span data-ttu-id="0fa5d-208">売上税が経費金額に含まれていますか。</span><span class="sxs-lookup"><span data-stu-id="0fa5d-208">Is sales tax included in the expense amounts?</span></span>
- <span data-ttu-id="0fa5d-209">過誤納税の還付は、経費で有効にしますか。</span><span class="sxs-lookup"><span data-stu-id="0fa5d-209">Should tax recovery be enabled on expenses?</span></span>

    > [!NOTE]
    > <span data-ttu-id="0fa5d-210">一般会計を計画していた場合、米国消費税の適用と税規則の使用を決定すると、経費で過誤納税の還付を有効にできません。</span><span class="sxs-lookup"><span data-stu-id="0fa5d-210">When you were planning the general ledger, if you decided to apply U.S. sales tax and use tax rules, you can’t enable tax recovery on expenses.</span></span> <span data-ttu-id="0fa5d-211">(米国消費税の適用および税規則を使用するには、[**売上税課税ルールの適用**] オプションを [**はい**] に設定します。)</span><span class="sxs-lookup"><span data-stu-id="0fa5d-211">(To apply U.S. sales tax and use tax rules, set the **Apply sales tax taxations rules** option to **Yes**.)</span></span>

## <a name="policies"></a><span data-ttu-id="0fa5d-212">ポリシー</span><span class="sxs-lookup"><span data-stu-id="0fa5d-212">Policies</span></span>

<span data-ttu-id="0fa5d-213">経費精算書のポリシーを作成により、従業員が変わって経費を負担した際、組織が時間とお金を節約するのに役立ちます。</span><span class="sxs-lookup"><span data-stu-id="0fa5d-213">By creating expense report policies, you can help your organization save time and money when employees incur expenses on its behalf.</span></span> <span data-ttu-id="0fa5d-214">ポリシーでは、従業員が予算の範囲内で、必要なすべての情報を入力し、必要に応じてのみ金銭を支出することを確認する助けになります。</span><span class="sxs-lookup"><span data-stu-id="0fa5d-214">Policies help guarantee that employees stay in budget, provide all required information, and spend money only as they require it.</span></span> <span data-ttu-id="0fa5d-215">作成した各経費精算書のポリシーおよび各経費精算書の承認ポリシーに対して次の意思決定を行う必要があります。</span><span class="sxs-lookup"><span data-stu-id="0fa5d-215">You must make the following decisions for each expense report policy and each expense report approval policy that you create.</span></span>

<span data-ttu-id="0fa5d-216">**意思決定:**</span><span class="sxs-lookup"><span data-stu-id="0fa5d-216">**Decisions:**</span></span>

- <span data-ttu-id="0fa5d-217">ポリシーの名前は何ですか。</span><span class="sxs-lookup"><span data-stu-id="0fa5d-217">What is the name of the policy?</span></span>
- <span data-ttu-id="0fa5d-218">経費ポリシーの目的は何ですか。</span><span class="sxs-lookup"><span data-stu-id="0fa5d-218">What is the expense policy for?</span></span>
- <span data-ttu-id="0fa5d-219">以前に、会社間経費を有効にすると決定した場合、どの会社にこのポリシーを適用しますか。</span><span class="sxs-lookup"><span data-stu-id="0fa5d-219">If you previously decided to enable intercompany expenses, which companies in your organization will this policy apply to?</span></span>
- <span data-ttu-id="0fa5d-220">ポリシーはいつ有効にしますか。</span><span class="sxs-lookup"><span data-stu-id="0fa5d-220">When does the policy become effective?</span></span>
- <span data-ttu-id="0fa5d-221">ポリシーの有効期限はいつにしますか。</span><span class="sxs-lookup"><span data-stu-id="0fa5d-221">When does the policy expire?</span></span>
- <span data-ttu-id="0fa5d-222">ポリシー ルールは何ですか。</span><span class="sxs-lookup"><span data-stu-id="0fa5d-222">What is the policy rule?</span></span>
- <span data-ttu-id="0fa5d-223">ポリシー ルールの結果は何ですか。</span><span class="sxs-lookup"><span data-stu-id="0fa5d-223">What is the outcome of the policy rule?</span></span>

