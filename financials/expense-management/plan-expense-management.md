---
title: "経費管理の構成"
description: "この記事は、Microsoft Dynamics 365 for Finance and Operations、Enterprise エディションの経費管理をコンフィギュレーションする前に、計画プロセス中に決定する必要のある考慮事項について説明します。 [経費管理] 領域で、支払方法、出張費要求、経費精算書、ポリシー、およびその他の情報を格納できます。"
author: KimANelson
manager: AnnBe
ms.date: 06/08/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: GlobalCategory, ProjCategory, TrvLocations, TrvParameters, TrvPaymethod, TrvPerDiems
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 23001
ms.assetid: aa3fd14d-7e94-4603-985f-ca26d6f860ea
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 20d28e22e4e89d0d864a0cbeaadeb568e73e223e
ms.openlocfilehash: 83cfd2ef15ae3a02eba21bb31f3311e8f5e15b90
ms.contentlocale: ja-jp
ms.lasthandoff: 06/29/2017


---

# <a name="configure-expense-management"></a><span data-ttu-id="04512-104">経費管理の構成</span><span class="sxs-lookup"><span data-stu-id="04512-104">Configure expense management</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="04512-105">この記事は、Microsoft Dynamics 365 for Finance and Operations、Enterprise エディションの経費管理をコンフィギュレーションする前に、計画プロセス中に決定する必要のある考慮事項について説明します。</span><span class="sxs-lookup"><span data-stu-id="04512-105">This article describes the considerations and the decisions that you must make during the planning process before you configure Expense management in Microsoft Dynamics 365 for Finance and Operations, Enterprise edition.</span></span> <span data-ttu-id="04512-106">[経費管理] 領域で、支払方法、出張費要求、経費精算書、ポリシー、およびその他の情報を格納できます。</span><span class="sxs-lookup"><span data-stu-id="04512-106">In the Expense management area, you can store information about payment methods, travel requisitions, expense reports, and policies, among other things.</span></span> 

<span data-ttu-id="04512-107">経費管理に対するコンフィギュレーションを計画する場合の決定の多くが、組織の階層と財務構造に基づいているため、これらの領域の計画文書を参照する必要があります。</span><span class="sxs-lookup"><span data-stu-id="04512-107">Because many of the decisions that you make when you plan your configuration for Expense management are based on your organization’s hierarchy and financial structure, you must refer to the planning documents for those areas.</span></span>

## <a name="intercompany-expenses"></a><span data-ttu-id="04512-108">会社間経費</span><span class="sxs-lookup"><span data-stu-id="04512-108">Intercompany expenses</span></span>
<span data-ttu-id="04512-109">会社間経費を有効にすると、組織内の法人に代わって別の法人や従業員が経費を支払ったり、その法人から支払を回収したりできます。</span><span class="sxs-lookup"><span data-stu-id="04512-109">When you enable intercompany expenses, you allow legal entities and employees to incur expenses on behalf of, and collect payment from, another legal entity within your organization.</span></span> <span data-ttu-id="04512-110">たとえば、法人 A の従業員が、法人 B のプロジェクトを完了します。会社間経費が有効な場合、従業員は法人 B へのタイムシートをまとめ、法人 B が支払います。組織に複数の法人がない場合、会社間経費を有効にする必要はありません。</span><span class="sxs-lookup"><span data-stu-id="04512-110">For example, an employee in legal entity A completes a project for legal entity B. If intercompany expenses are enabled, the employee can then file a timesheet to, and be paid by, legal entity B. If your organization doesn’t have multiple legal entities, you won’t need to enable intercompany expenses.</span></span> <span data-ttu-id="04512-111">**意思決定:** 会社間経費を有効にしますか。</span><span class="sxs-lookup"><span data-stu-id="04512-111">**Decision:** Do you want to enable intercompany expenses?</span></span>

## <a name="financial-management"></a><span data-ttu-id="04512-112">財務管理</span><span class="sxs-lookup"><span data-stu-id="04512-112">Financial management</span></span>
<span data-ttu-id="04512-113">経費管理は、組織の財務管理と密に統合されています。</span><span class="sxs-lookup"><span data-stu-id="04512-113">Expense management is tightly integrated with the financial management of your organization.</span></span> <span data-ttu-id="04512-114">経費管理の多くのコンフィギュレーションは、組織の財務に関する決定に基づいています。</span><span class="sxs-lookup"><span data-stu-id="04512-114">A lot of your configuration for Expense management will be based on the decisions that you’ve made about your organization’s finances.</span></span> <span data-ttu-id="04512-115">次のセクションでは、組織の財務上の決定および指導チームからのガイダンスに基づいた計画および決定が必要になるさまざまな領域について説明します。</span><span class="sxs-lookup"><span data-stu-id="04512-115">The following sections describe the different areas that require planning and decisions based on your organization’s financial decisions and guidance from your leadership team.</span></span>

### <a name="per-diems"></a><span data-ttu-id="04512-116">日当</span><span class="sxs-lookup"><span data-stu-id="04512-116">Per diems</span></span>

<span data-ttu-id="04512-117">組織で提供する日当の従業員を定義する必要があります。</span><span class="sxs-lookup"><span data-stu-id="04512-117">You must define the employee per diems that your organization provides.</span></span> <span data-ttu-id="04512-118">日当は通常、食費、宿泊費、その他の臨時費などの経費を負担するために使用されるため、組織が提供する日当ルールを作成できます。</span><span class="sxs-lookup"><span data-stu-id="04512-118">Because per diems are typically used to cover expenses such as meals, lodging, and other incidental expenses, you can create rules for the per diem allowances that your organization offers.</span></span> <span data-ttu-id="04512-119">日当レートは、時期、出張先、または両方を基準にされます。</span><span class="sxs-lookup"><span data-stu-id="04512-119">Per diem rates can be based on the time of year, the travel location, or both.</span></span> <span data-ttu-id="04512-120">日当ルールを定義する際に、作業者が無料の食事やサービスを受ける場合、日当レートから天引される割合を指定できます。</span><span class="sxs-lookup"><span data-stu-id="04512-120">When you define a per diem rule, you can specify that a percentage of the per diem rate will be withheld if a worker receives complimentary meals or services.</span></span> <span data-ttu-id="04512-121">作業員の出張に適用できる日当レートの最大時間数と最小時間数を設定するために日当レート層を定義することもできます。</span><span class="sxs-lookup"><span data-stu-id="04512-121">You can also define per diem rate tiers to set the minimum and maximum number of hours that the per diem rate can be applied to a worker’s travel.</span></span> <span data-ttu-id="04512-122">**意思決定:**</span><span class="sxs-lookup"><span data-stu-id="04512-122">**Decisions:**</span></span>

-   <span data-ttu-id="04512-123">最初と最後の日の既定の日当ルール:</span><span class="sxs-lookup"><span data-stu-id="04512-123">Default per diem rules for the first and last days:</span></span>
    -   <span data-ttu-id="04512-124">従業員が 1 日に要求し、日当を受け取る最小時間数はどのくらいですか。</span><span class="sxs-lookup"><span data-stu-id="04512-124">What is the minimum number of hours that an employee can claim for a day and still receive a per diem?</span></span>
    -   <span data-ttu-id="04512-125">最初と最後の日の食事のために支給される金額に減額はありますか。</span><span class="sxs-lookup"><span data-stu-id="04512-125">Is there a reduction in the amount that is offered for meals for the first and last day?</span></span> <span data-ttu-id="04512-126">ある場合、減少の割合はどのくらいですか。</span><span class="sxs-lookup"><span data-stu-id="04512-126">If so, what is the percentage of the reduction?</span></span>
    -   <span data-ttu-id="04512-127">最初と最後の日のホテルのために支給される金額に減額はありますか。</span><span class="sxs-lookup"><span data-stu-id="04512-127">Is there a reduction in the amount that is offered for a hotel for the first and last day?</span></span> <span data-ttu-id="04512-128">ある場合、減少の割合はどのくらいですか。</span><span class="sxs-lookup"><span data-stu-id="04512-128">If so, what is the percentage of the reduction?</span></span>
    -   <span data-ttu-id="04512-129">最初と最後の日にかかるその他の経費に支給される金額に減額はありますか。</span><span class="sxs-lookup"><span data-stu-id="04512-129">Is there a reduction in the amount that is offered for other expenses incurred on the first and last day?</span></span> <span data-ttu-id="04512-130">ある場合、減少の割合はどのくらいですか。</span><span class="sxs-lookup"><span data-stu-id="04512-130">If so, what is the percentage of the reduction?</span></span>
-   <span data-ttu-id="04512-131">既定の日当ルール:</span><span class="sxs-lookup"><span data-stu-id="04512-131">Default per diem rules:</span></span>
    -   <span data-ttu-id="04512-132">食事が無料の場合などの食事に関する日当に割合での減額はありますか。</span><span class="sxs-lookup"><span data-stu-id="04512-132">Is there a percentage reduction in the per diem allowance for each meal if, for example, the meal is complimentary?</span></span> <span data-ttu-id="04512-133">ある場合、食事ごとの減額の割合はどのくらいですか。</span><span class="sxs-lookup"><span data-stu-id="04512-133">If so, what is the reduction percentage for each meal?</span></span>
    -   <span data-ttu-id="04512-134">1 日あたり、出張あたり、または 1 日あたりの食事数で計算される食費減額はありますか。</span><span class="sxs-lookup"><span data-stu-id="04512-134">Is the meal reduction calculated per day, per trip, or by the number of meals per day?</span></span>
    -   <span data-ttu-id="04512-135">日当金額は、丸め処理、または切り上げ処理を行いますか。</span><span class="sxs-lookup"><span data-stu-id="04512-135">Should per diem amounts be rounded normally or rounded up?</span></span>
    -   <span data-ttu-id="04512-136">日当は、24 時間制期間またはカレンダー日に基づいて計算しますか。</span><span class="sxs-lookup"><span data-stu-id="04512-136">Are per diems calculated on a 24-hour period or on a calendar day?</span></span>
-   <span data-ttu-id="04512-137">場所に基づく日当ルール:</span><span class="sxs-lookup"><span data-stu-id="04512-137">Per diem rules based on location:</span></span>
    -   <span data-ttu-id="04512-138">日当レートは、場所および場所が含まれるものに基づいて異なりますか。</span><span class="sxs-lookup"><span data-stu-id="04512-138">Do per diem rates vary based on location and what locations are included?</span></span>
    -   <span data-ttu-id="04512-139">日当レートが場所に基づいて異なる場合、それぞれの場所での支給の割合はどのくらいですか。</span><span class="sxs-lookup"><span data-stu-id="04512-139">If per diem rate do vary based on location, for each location, what percentage amount is provided for:</span></span>
        -   <span data-ttu-id="04512-140">食事</span><span class="sxs-lookup"><span data-stu-id="04512-140">meals</span></span>
        -   <span data-ttu-id="04512-141">ホテル</span><span class="sxs-lookup"><span data-stu-id="04512-141">hotel</span></span>
        -   <span data-ttu-id="04512-142">その他の経費</span><span class="sxs-lookup"><span data-stu-id="04512-142">other expenses</span></span>

### <a name="expense-management-journals-and-accounts"></a><span data-ttu-id="04512-143">経費管理仕訳帳および勘定</span><span class="sxs-lookup"><span data-stu-id="04512-143">Expense management journals and accounts</span></span>

<span data-ttu-id="04512-144">経費管理には、複数の仕訳帳および勘定を使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="04512-144">Expense management requires that you use multiple journals and accounts.</span></span> <span data-ttu-id="04512-145">たとえば、同じ勘定を、現金前貸しとクレジット カードの争議に使用するかどうか決定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="04512-145">You must decide, for example, whether the same account is used for cash advances and credit card disputes.</span></span> <span data-ttu-id="04512-146">**意思決定:**</span><span class="sxs-lookup"><span data-stu-id="04512-146">**Decisions:**</span></span>

-   <span data-ttu-id="04512-147">どの仕訳元帳に承認済経費精算書を転記しますか。</span><span class="sxs-lookup"><span data-stu-id="04512-147">Which ledger journal are approved expense reports posted to?</span></span>
-   <span data-ttu-id="04512-148">どの勘定を現金前貸しに使用しますか。</span><span class="sxs-lookup"><span data-stu-id="04512-148">Which account is used for cash advances?</span></span>
-   <span data-ttu-id="04512-149">現金前貸しをすぐに転記しますか。</span><span class="sxs-lookup"><span data-stu-id="04512-149">Should cash advances be posted immediately?</span></span>

### <a name="payment-methods"></a><span data-ttu-id="04512-150">支払方法</span><span class="sxs-lookup"><span data-stu-id="04512-150">Payment methods</span></span>

<span data-ttu-id="04512-151">従業員が業務のために経費を支払うことを許可するときに、従業員が使用できる支払方法を定義する必要があります。</span><span class="sxs-lookup"><span data-stu-id="04512-151">When you allow employees to incur expenses on behalf of your business, you must define the payment methods that employees are allowed to use.</span></span> <span data-ttu-id="04512-152">たとえば、従業員による現金または会社のクレジット カードの使用を許可することができます。</span><span class="sxs-lookup"><span data-stu-id="04512-152">For example, you might allow employees to use cash or a corporate credit card.</span></span> <span data-ttu-id="04512-153">また、従業員が個人のクレジット カードを使用して、後で払い戻すようにすることもできます。</span><span class="sxs-lookup"><span data-stu-id="04512-153">You might also allow employees to use personal credit cards, and then reimburse the employees.</span></span> <span data-ttu-id="04512-154">許可する各支払方法に次の意思決定を行う必要があります。</span><span class="sxs-lookup"><span data-stu-id="04512-154">You must make the following decisions for each payment method that you allow.</span></span> <span data-ttu-id="04512-155">**意思決定:**</span><span class="sxs-lookup"><span data-stu-id="04512-155">**Decisions:**</span></span>

-   <span data-ttu-id="04512-156">どの支払方法を許可しますか。</span><span class="sxs-lookup"><span data-stu-id="04512-156">What payment methods are allowed?</span></span>
-   <span data-ttu-id="04512-157">誰が支払方法の経費を所持しますか。</span><span class="sxs-lookup"><span data-stu-id="04512-157">Who owns the payment method expenses?</span></span>
-   <span data-ttu-id="04512-158">相手勘定タイプはありますか。</span><span class="sxs-lookup"><span data-stu-id="04512-158">Is there an offset account type?</span></span> <span data-ttu-id="04512-159">ある場合、何ですか。</span><span class="sxs-lookup"><span data-stu-id="04512-159">If so, what is it?</span></span>
-   <span data-ttu-id="04512-160">相手勘定がある場合、勘定は何ですか。</span><span class="sxs-lookup"><span data-stu-id="04512-160">If there is an offset account, what is the account?</span></span>
-   <span data-ttu-id="04512-161">支払方法がクレジット カードである場合、その支払方法をインポートされたトランザクションでのみ使用しますか。</span><span class="sxs-lookup"><span data-stu-id="04512-161">If the payment method is a credit card, should the payment method be used only with imported transactions?</span></span>

### <a name="expense-categories-and-shared-categories"></a><span data-ttu-id="04512-162">経費カテゴリおよび共有カテゴリ</span><span class="sxs-lookup"><span data-stu-id="04512-162">Expense categories and shared categories</span></span>

<span data-ttu-id="04512-163">従業員が経費精算書を作成する際、記録する各費用は経費カテゴリと関連付けている必要があります。</span><span class="sxs-lookup"><span data-stu-id="04512-163">When employees create an expense report, each expense that they record must be associated with an expense category.</span></span> <span data-ttu-id="04512-164">経費カテゴリは、組織内の法人間で共有できる共有カテゴリから取得されます。</span><span class="sxs-lookup"><span data-stu-id="04512-164">Expense categories are derived from Shared categories that can be shared across the legal entities within your organization.</span></span> <span data-ttu-id="04512-165">これらのカテゴリは、組織の定義方法に応じて、プロジェクト管理および会計で共有することもできます。</span><span class="sxs-lookup"><span data-stu-id="04512-165">These categories can also be shared in Project management and accounting, depending on how your organization is defined.</span></span> <span data-ttu-id="04512-166">組織の定義および実装チームからのガイダンスに基づいて、経費管理に使用するカテゴリを経費のみで使用するか、プロジェクトと経費との間で共有する必要があるかを決定します。</span><span class="sxs-lookup"><span data-stu-id="04512-166">Based on the definition of your organization and guidance from the implementation team, determine whether the categories used in expense management are to be used in only expense or if they should be shared between Project and Expense.</span></span> <span data-ttu-id="04512-167">これらのカテゴリは、プロジェクトと経費、またはプロジェクトと運用の間で共有できますが、経費と運用の間では共有できないことに注意してください。</span><span class="sxs-lookup"><span data-stu-id="04512-167">Note that these categories can be shared between Project and Expense or Project and Production, but not between Expense and Production.</span></span> <span data-ttu-id="04512-168">各経費カテゴリに対して次の意思決定を行う必要があります。</span><span class="sxs-lookup"><span data-stu-id="04512-168">You must make the following decisions for each expense category.</span></span> <span data-ttu-id="04512-169">**意思決定:**</span><span class="sxs-lookup"><span data-stu-id="04512-169">**Decisions:**</span></span>

-   <span data-ttu-id="04512-170">経費カテゴリは何ですか。</span><span class="sxs-lookup"><span data-stu-id="04512-170">What is the expense category?</span></span> <span data-ttu-id="04512-171">たとえば、航空運賃、宿泊費、またはマイレージ。</span><span class="sxs-lookup"><span data-stu-id="04512-171">For example, flights, hotel, or mileage.</span></span>
-   <span data-ttu-id="04512-172">この経費カテゴリは、プロジェクト管理および会計でも使用できますか。</span><span class="sxs-lookup"><span data-stu-id="04512-172">Can this expense category also be used in Project management and accounting?</span></span>
-   <span data-ttu-id="04512-173">経費タイプは何ですか。</span><span class="sxs-lookup"><span data-stu-id="04512-173">What is the expense type?</span></span>
-   <span data-ttu-id="04512-174">経費カテゴリの既定の支払方法は何ですか。</span><span class="sxs-lookup"><span data-stu-id="04512-174">What is the default payment method for the expense category?</span></span>
-   <span data-ttu-id="04512-175">このカテゴリの経費を明細化する必要はありますか。</span><span class="sxs-lookup"><span data-stu-id="04512-175">Are expenses in this category required to be itemized?</span></span>
-   <span data-ttu-id="04512-176">経費カテゴリに対するメインの既定の勘定は何ですか。</span><span class="sxs-lookup"><span data-stu-id="04512-176">What is the main default account for the expense category?</span></span>
-   <span data-ttu-id="04512-177">経費カテゴリに対する既定の品目売上税グループは何ですか。</span><span class="sxs-lookup"><span data-stu-id="04512-177">What is the default item sales tax group for the expense category?</span></span>
-   <span data-ttu-id="04512-178">この経費カテゴリに対して許可されている追加の支払方法はありますか。</span><span class="sxs-lookup"><span data-stu-id="04512-178">Are additional payment methods allowed for the expense category?</span></span> <span data-ttu-id="04512-179">ある場合、それは何ですか。</span><span class="sxs-lookup"><span data-stu-id="04512-179">If so, what are they?</span></span>
-   <span data-ttu-id="04512-180">この経費カテゴリ内に下位カテゴリはありますか。</span><span class="sxs-lookup"><span data-stu-id="04512-180">Are there subcategories within this expense category?</span></span> <span data-ttu-id="04512-181">ある場合:</span><span class="sxs-lookup"><span data-stu-id="04512-181">If so:</span></span>
    -   <span data-ttu-id="04512-182">過誤納税の還付から除外される下位カテゴリはありますか。</span><span class="sxs-lookup"><span data-stu-id="04512-182">Are any of the subcategories excluded from tax recovery?</span></span>
    -   <span data-ttu-id="04512-183">下位カテゴリの品目売上税グループは何ですか。</span><span class="sxs-lookup"><span data-stu-id="04512-183">What is the item sales tax group of the subcategories?</span></span>

    <span data-ttu-id="04512-184">この経費カテゴリがプロジェクト管理および会計でも使用されている場合、残りの質問にご回答ください。</span><span class="sxs-lookup"><span data-stu-id="04512-184">If this expense category is also used in Project management and accounting, answer the remaining questions.</span></span> <span data-ttu-id="04512-185">それ以外の場合、このセクションは終了です。</span><span class="sxs-lookup"><span data-stu-id="04512-185">Otherwise, you are finished with this section.</span></span>
-   <span data-ttu-id="04512-186">次のものにどの原価勘定を使用しますか。</span><span class="sxs-lookup"><span data-stu-id="04512-186">Which cost accounts will be used for the following?</span></span>
    -   <span data-ttu-id="04512-187">コスト</span><span class="sxs-lookup"><span data-stu-id="04512-187">Cost</span></span>
    -   <span data-ttu-id="04512-188">給与配賦</span><span class="sxs-lookup"><span data-stu-id="04512-188">Payroll allocation</span></span>
    -   <span data-ttu-id="04512-189">仕掛品 - 原価価値</span><span class="sxs-lookup"><span data-stu-id="04512-189">WIP-cost value</span></span>
    -   <span data-ttu-id="04512-190">原価 - 品目</span><span class="sxs-lookup"><span data-stu-id="04512-190">Cost-item</span></span>
    -   <span data-ttu-id="04512-191">仕掛品 - 原価価値 - 品目</span><span class="sxs-lookup"><span data-stu-id="04512-191">WIP-cost value-item</span></span>
    -   <span data-ttu-id="04512-192">未収損益</span><span class="sxs-lookup"><span data-stu-id="04512-192">Accrued loss</span></span>
    -   <span data-ttu-id="04512-193">仕掛品 - 未収損失</span><span class="sxs-lookup"><span data-stu-id="04512-193">WIP-accrued loss</span></span>
-   <span data-ttu-id="04512-194">次のものにどの収益勘定を使用しますか。</span><span class="sxs-lookup"><span data-stu-id="04512-194">Which revenue accounts will be used for the following?</span></span>
    -   <span data-ttu-id="04512-195">請求済み収益</span><span class="sxs-lookup"><span data-stu-id="04512-195">Invoiced revenue</span></span>
    -   <span data-ttu-id="04512-196">未収収益 - 販売額</span><span class="sxs-lookup"><span data-stu-id="04512-196">Accrued revenue-sales value</span></span>
    -   <span data-ttu-id="04512-197">仕掛品 - 販売額</span><span class="sxs-lookup"><span data-stu-id="04512-197">WIP-sales value</span></span>
    -   <span data-ttu-id="04512-198">未収収益 - 生産</span><span class="sxs-lookup"><span data-stu-id="04512-198">Accrued revenue-production</span></span>
    -   <span data-ttu-id="04512-199">仕掛品 - 生産</span><span class="sxs-lookup"><span data-stu-id="04512-199">WIP-production</span></span>
    -   <span data-ttu-id="04512-200">未収収益 - 利益</span><span class="sxs-lookup"><span data-stu-id="04512-200">Accrued revenue-profit</span></span>
    -   <span data-ttu-id="04512-201">仕掛品 - 利益</span><span class="sxs-lookup"><span data-stu-id="04512-201">WIP-profit</span></span>
    -   <span data-ttu-id="04512-202">未収収益 - 定期売買</span><span class="sxs-lookup"><span data-stu-id="04512-202">Accrued revenue-subscription</span></span>
    -   <span data-ttu-id="04512-203">仕掛品 - 定期売買</span><span class="sxs-lookup"><span data-stu-id="04512-203">WIP-subscription</span></span>

 

### <a name="taxes"></a><span data-ttu-id="04512-204">税</span><span class="sxs-lookup"><span data-stu-id="04512-204">Taxes</span></span>

<span data-ttu-id="04512-205">経費に関係する税の場合、経費精算書に含まれるものや有効なものを判断する必要があります。</span><span class="sxs-lookup"><span data-stu-id="04512-205">For expense-related taxes, you must determine what is included or enabled on expense reports.</span></span> <span data-ttu-id="04512-206">**意思決定:**</span><span class="sxs-lookup"><span data-stu-id="04512-206">**Decisions:**</span></span>

-   <span data-ttu-id="04512-207">売上税が経費金額に含まれていますか。</span><span class="sxs-lookup"><span data-stu-id="04512-207">Is sales tax included in the expense amounts?</span></span>
-   <span data-ttu-id="04512-208">過誤納税の還付は、経費で有効にしますか。</span><span class="sxs-lookup"><span data-stu-id="04512-208">Should tax recovery be enabled on expenses?</span></span>

<span data-ttu-id="04512-209">一般会計の計画時に、米国の売上税を適用し、[**売上税課税ルールの適用**] フィールドで [はい] に切り替えて税ルールを使用する場合、経費で過誤納税の還付を有効にできないことに注意してください。</span><span class="sxs-lookup"><span data-stu-id="04512-209">Note that if, during your planning of the general ledger, you have decided to apply U.S. sales tax and use tax rules, which is done by toggling the **Apply sales tax taxations rules** field to Yes, you can’t enable tax recovery on expenses.</span></span>

## <a name="policies"></a><span data-ttu-id="04512-210">ポリシー</span><span class="sxs-lookup"><span data-stu-id="04512-210">Policies</span></span>
<span data-ttu-id="04512-211">従業員が変わって経費を負担したときに、組織が時間とお金を節約できるように、経費精算書のポリシーを作成できます。</span><span class="sxs-lookup"><span data-stu-id="04512-211">You can create expense report policies so that your organization can save time and money when employees incur expenses on its behalf.</span></span> <span data-ttu-id="04512-212">ポリシーでは、従業員が予算の範囲内で、必要なすべての情報を入力し、必要な場合のみ金銭を支出することを確認します。</span><span class="sxs-lookup"><span data-stu-id="04512-212">Policies ensure that employees stay within budget, provide all required information, and spend money only as necessary.</span></span> <span data-ttu-id="04512-213">作成した各経費精算書のポリシーおよび各経費精算書の承認ポリシーに対して次の意思決定を行う必要があります。</span><span class="sxs-lookup"><span data-stu-id="04512-213">You must make the following decisions for each expense report policy and each expense report approval policy that you create.</span></span> <span data-ttu-id="04512-214">**意思決定:**</span><span class="sxs-lookup"><span data-stu-id="04512-214">**Decisions:**</span></span>

-   <span data-ttu-id="04512-215">ポリシーの名前は何ですか。</span><span class="sxs-lookup"><span data-stu-id="04512-215">What is the name of the policy?</span></span>
-   <span data-ttu-id="04512-216">経費ポリシーの目的は何ですか。</span><span class="sxs-lookup"><span data-stu-id="04512-216">What is the expense policy for?</span></span>
-   <span data-ttu-id="04512-217">以前に、会社間経費を有効にすると決定した場合、どの会社にこのポリシーを適用しますか。</span><span class="sxs-lookup"><span data-stu-id="04512-217">If you previously decided to enable intercompany expenses, to which companies in your organization will this policy apply?</span></span>
-   <span data-ttu-id="04512-218">ポリシーはいつ有効にしますか。</span><span class="sxs-lookup"><span data-stu-id="04512-218">When does the policy become effective?</span></span>
-   <span data-ttu-id="04512-219">ポリシーの有効期限はいつにしますか。</span><span class="sxs-lookup"><span data-stu-id="04512-219">When does the policy expire?</span></span>
-   <span data-ttu-id="04512-220">ポリシー ルールは何ですか。</span><span class="sxs-lookup"><span data-stu-id="04512-220">What is the policy rule?</span></span>
-   <span data-ttu-id="04512-221">ポリシー ルールの結果は何ですか。</span><span class="sxs-lookup"><span data-stu-id="04512-221">What is the outcome of the policy rule?</span></span>





