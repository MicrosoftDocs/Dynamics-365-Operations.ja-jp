---
title: 給付金管理の概要
description: Dynamics 365 Human Resources の給付金管理プレビュー機能の概要。 使いやすいオンライン エクスペリエンスで、従業員に拡張された給付金オプションを提供します。
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: BenefitWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 63db1b55bae9150dd87d9981136b96d72ffd0c59
ms.sourcegitcommit: 523049c363a999050c58d20695f1c7d151b3fd3e
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/06/2020
ms.locfileid: "3029466"
---
# <a name="benefits-management-overview"></a><span data-ttu-id="1f000-104">給付金管理の概要</span><span class="sxs-lookup"><span data-stu-id="1f000-104">Benefits management overview</span></span>

[!include [banner](includes/preview-feature.md)]

<span data-ttu-id="1f000-105">競争力を維持するには、最高の従業員を獲得し維持するために、充実したメリットを提供する必要があります。</span><span class="sxs-lookup"><span data-stu-id="1f000-105">To remain competitive, you must offer a rich set of benefits to attract and retain your best employees.</span></span> <span data-ttu-id="1f000-106">医療や歯科などの標準的な利点に加えて、採用支援、レクリエーション プログラム、および衣料手当などの拡張サービスを提供することもできます。</span><span class="sxs-lookup"><span data-stu-id="1f000-106">In addition to standard benefits like medical and dental coverage, you might also want to offer expanded services like adoption assistance, recreation programs, and clothing allowances.</span></span> <span data-ttu-id="1f000-107">Microsoft Dynamics 365 Human Resources の給付金管理プレビュー機能には、さまざまな給付金オプションをサポートする柔軟なソリューションが用意されています。</span><span class="sxs-lookup"><span data-stu-id="1f000-107">The Benefits management preview feature in Microsoft Dynamics 365 Human Resources provides you with a flexible solution that supports a wide variety of benefit options.</span></span> <span data-ttu-id="1f000-108">人事管理では、製品を紹介するための使いやすい従業員エクスペリエンスも含まれています。</span><span class="sxs-lookup"><span data-stu-id="1f000-108">Human Resources also includes an easy-to-use employee experience that showcases your offerings.</span></span>

- <span data-ttu-id="1f000-109">拡張された給付金プランを使用すると、独自の給付金プランを作成および管理し、複雑な給付金のレート テーブルとネストされた階層をサポートできます。</span><span class="sxs-lookup"><span data-stu-id="1f000-109">Enhanced benefits plans let you create and manage unique benefit plans and support complex benefit rate tables and nested tiers.</span></span> <span data-ttu-id="1f000-110">より簡単な従業員エクスペリエンスのために、給付金プログラム、バンドル、および自動登録ルールを容易に作成できます。</span><span class="sxs-lookup"><span data-stu-id="1f000-110">You can easily create benefit programs, bundles, and auto-enrollment rules for an easier employee experience.</span></span>

- <span data-ttu-id="1f000-111">レックス クレジット プログラムでは、退職やその他のライフ イベントをサポートします。</span><span class="sxs-lookup"><span data-stu-id="1f000-111">Flex credit programs let you prorate to support retirement and other life events.</span></span>

- <span data-ttu-id="1f000-112">広範な適格性ルールによって、適切な従業員が適切な利益を得ることができます。</span><span class="sxs-lookup"><span data-stu-id="1f000-112">Extensive eligibility rules ensure you make the right benefits available to the right employees.</span></span>

- <span data-ttu-id="1f000-113">オンライン給付金の登録は、従業員にとって簡単なエクスペリエンスです。</span><span class="sxs-lookup"><span data-stu-id="1f000-113">Online benefits enrollment provides an easy experience for your employees.</span></span>

- <span data-ttu-id="1f000-114">修飾ライフ イベントの処理は、従業員セルフ サービスと統合し、将来のライフ イベントもサポートします。</span><span class="sxs-lookup"><span data-stu-id="1f000-114">Qualified life event processing integrates with Employee self service, and also supports future life events.</span></span>

<span data-ttu-id="1f000-115">デモ データにアクセスする場合は、サンドボックス環境を再配置する必要があります。</span><span class="sxs-lookup"><span data-stu-id="1f000-115">If you would like to access the demo data, you'll need to redeploy your sandbox environment.</span></span>

<span data-ttu-id="1f000-116">直接のフィードバックまたはレポート問題については、D365BenefitsPreview@microsoft.com で提供可能です。</span><span class="sxs-lookup"><span data-stu-id="1f000-116">You can provide direct feedback or report issues to:  D365BenefitsPreview@microsoft.com.</span></span>

## <a name="benefits-management-known-issues"></a><span data-ttu-id="1f000-117">給付金管理に関する既知の問題</span><span class="sxs-lookup"><span data-stu-id="1f000-117">Benefits management known issues</span></span>

### <a name="eligibility-processing"></a><span data-ttu-id="1f000-118">適格性処理中</span><span class="sxs-lookup"><span data-stu-id="1f000-118">Eligibility processing</span></span>

<span data-ttu-id="1f000-119">1-5X 給与、給与の % および均一額の補償金額を使用する給付金の適格性を実行する場合、**給付金の詳細**日付を**従業員履歴**の**従業員の雇用開始日**に設定します。</span><span class="sxs-lookup"><span data-stu-id="1f000-119">When running eligibility for benefits that use a 1-5X Salary, % of Salary, and Flat Amount coverage amount, you must set the **Benefit details** date to the **Employee start date** in **Employment history**.</span></span> <span data-ttu-id="1f000-120">また、**就業時間**、**支払頻度**および**年間給付金の給与額**を含む必要があります。</span><span class="sxs-lookup"><span data-stu-id="1f000-120">You must also include **Hours worked**, **Payment frequency**, and **Annual benefits salary amount**.</span></span> <span data-ttu-id="1f000-121">作業者に固定報酬がある場合、**勤務時間**および**支払頻度**を入力します。</span><span class="sxs-lookup"><span data-stu-id="1f000-121">If the worker has fixed compensation, enter **Hours worked** and **Payment frequency**.</span></span> <span data-ttu-id="1f000-122">年収額が計算されます。</span><span class="sxs-lookup"><span data-stu-id="1f000-122">The annual salary amount will calculate.</span></span> <span data-ttu-id="1f000-123">従業員に給与がかかる場合は、**作業時間**を入力する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="1f000-123">If the employee is salaried, you don't need to enter **Hours worked**.</span></span> <span data-ttu-id="1f000-124">新しい従業員を作成する場合は、先に固定報酬を入力することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="1f000-124">We recommend that when creating new workers, enter fixed compensation first.</span></span> <span data-ttu-id="1f000-125">給付金の詳細記録を更新するには、**従業員 > 作業員の履歴 > 従業員の詳細**に移動します。</span><span class="sxs-lookup"><span data-stu-id="1f000-125">To update the benefit details record, navigate to **Worker > Worker history > Employment details**.</span></span> <span data-ttu-id="1f000-126">日付を作業者の雇用開始日に調整します。</span><span class="sxs-lookup"><span data-stu-id="1f000-126">Adjust the date to the worker's start date.</span></span>

### <a name="employee-self-service"></a><span data-ttu-id="1f000-127">従業員セルフ サービス</span><span class="sxs-lookup"><span data-stu-id="1f000-127">Employee self-service</span></span>

<span data-ttu-id="1f000-128">生命保険の補償金額を更新する場合、従業員の金額は計算されません。</span><span class="sxs-lookup"><span data-stu-id="1f000-128">Employee amount doesn't calculate when updating the coverage amount for life insurance.</span></span> <span data-ttu-id="1f000-129">たとえば、従業員に生命保険プランが提供されている場合は、1,000 ドルの補償につき 0.36 ドルの費用で、最大 50,000 ドルの補償を選択できます。</span><span class="sxs-lookup"><span data-stu-id="1f000-129">For example, when an employee is offered a life insurance plan, they can select up to $50,000 in coverage at a cost of $.36 per $1,000 of coverage.</span></span>  <span data-ttu-id="1f000-130">従業員が補充金額を更新すると、従業員に関連付けられている原価はゼロのままになります。</span><span class="sxs-lookup"><span data-stu-id="1f000-130">When the employee updates the coverage amount, the employee’s associated cost remains at zero.</span></span>

<span data-ttu-id="1f000-131">その計画タイプの単一選択のみを許可する給付金計画の場合、ユーザーは計画を選択した後に、計画を放棄しようとするとエラーを受け取ります。</span><span class="sxs-lookup"><span data-stu-id="1f000-131">For a benefit plan that only allows a single selection of that plan type, the user receives an error if they attempt to waive a plan after selecting a plan.</span></span> <span data-ttu-id="1f000-132">たとえば、ユーザーが医療プランを選択してカートに配置したとします。</span><span class="sxs-lookup"><span data-stu-id="1f000-132">For example, a user selects a medical plan and places it in their cart.</span></span> <span data-ttu-id="1f000-133">その後、ユーザー は別の医療プランの**放棄**を選択します。</span><span class="sxs-lookup"><span data-stu-id="1f000-133">The user then selects **Waive** for another medical plan.</span></span> <span data-ttu-id="1f000-134">ユーザーにはエラーが表示されます。</span><span class="sxs-lookup"><span data-stu-id="1f000-134">The user will receive an error.</span></span>

## <a name="enable-benefits-management"></a><span data-ttu-id="1f000-135">給付金管理を有効にする</span><span class="sxs-lookup"><span data-stu-id="1f000-135">Enable Benefits management</span></span>

<span data-ttu-id="1f000-136">給付金管理はプレビュー機能であり、**サンドボックス**環境でのみ使用できます。</span><span class="sxs-lookup"><span data-stu-id="1f000-136">Benefits management is a preview feature, and is only available in **Sandbox** environments.</span></span> <span data-ttu-id="1f000-137">これらの記事では、人事管理でプレビュー機能を有効にする方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="1f000-137">These articles describe how to turn on preview features in Human Resources.</span></span> <span data-ttu-id="1f000-138">また、人事管理のプレビュー機能のうち、一度給付金管理をオンにして、給付金管理に置き換わるか無効になるかを示します。</span><span class="sxs-lookup"><span data-stu-id="1f000-138">They also tell which existing features in Human Resources that Benefits management replaces or are disabled once you turn on Benefits management.</span></span>

- [<span data-ttu-id="1f000-139">機能の管理</span><span class="sxs-lookup"><span data-stu-id="1f000-139">Manage features</span></span>](hr-admin-manage-features.md)
- [<span data-ttu-id="1f000-140">プレビュー機能: 給付金管理</span><span class="sxs-lookup"><span data-stu-id="1f000-140">Preview feature: Benefits management</span></span>](hr-admin-manage-features.md?preview-feature-benefits-management)

## <a name="configure-benefits-management"></a><span data-ttu-id="1f000-141">給付金管理の構成</span><span class="sxs-lookup"><span data-stu-id="1f000-141">Configure Benefits management</span></span>

<span data-ttu-id="1f000-142">従業員の給付金計画を作成する前に、その計画のオプションを構成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="1f000-142">Before you can create benefit plans for your employees, you need to configure options for the plans.</span></span>

- [<span data-ttu-id="1f000-143">給付金管理パラメーターを設定</span><span class="sxs-lookup"><span data-stu-id="1f000-143">Set Benefits management parameters</span></span>](hr-benefits-setup-parameters.md)
- [<span data-ttu-id="1f000-144">適格性ルールとオプションを構成</span><span class="sxs-lookup"><span data-stu-id="1f000-144">Configure eligibility rules and options</span></span>](hr-benefits-setup-eligibility-rules.md)
- [<span data-ttu-id="1f000-145">個人の連絡先適格性オプションを構成</span><span class="sxs-lookup"><span data-stu-id="1f000-145">Configure personal contact eligibility options</span></span>](hr-benefits-setup-contact-eligibility-options.md)
- [<span data-ttu-id="1f000-146">補償オプションを作成</span><span class="sxs-lookup"><span data-stu-id="1f000-146">Create coverage options</span></span>](hr-benefits-setup-coverage-options.md)
- [<span data-ttu-id="1f000-147">支払頻度の設定</span><span class="sxs-lookup"><span data-stu-id="1f000-147">Set up payment frequencies</span></span>](hr-benefits-setup-payment-frequencies.md)
- [<span data-ttu-id="1f000-148">将来のライフ イベントの構成</span><span class="sxs-lookup"><span data-stu-id="1f000-148">Configure life event types</span></span>](hr-benefits-setup-life-event-types.md)
- [<span data-ttu-id="1f000-149">プラン タイプの作成</span><span class="sxs-lookup"><span data-stu-id="1f000-149">Create plan types</span></span>](hr-benefits-setup-plan-types.md)
- [<span data-ttu-id="1f000-150">理由コードの設定</span><span class="sxs-lookup"><span data-stu-id="1f000-150">Set up reason codes</span></span>](hr-benefits-setup-reason-codes.md)
- [<span data-ttu-id="1f000-151">階層コードの設定</span><span class="sxs-lookup"><span data-stu-id="1f000-151">Set up tier codes</span></span>](hr-benefits-setup-tier-codes.md)
- [<span data-ttu-id="1f000-152">レートの構成</span><span class="sxs-lookup"><span data-stu-id="1f000-152">Configure rates</span></span>](hr-benefits-setup-rates.md)
- [<span data-ttu-id="1f000-153">控除の構成</span><span class="sxs-lookup"><span data-stu-id="1f000-153">Configure deductions</span></span>](hr-benefits-setup-deductions.md)
- [<span data-ttu-id="1f000-154">待機日数の構成</span><span class="sxs-lookup"><span data-stu-id="1f000-154">Configure waiting days</span></span>](hr-benefits-setup-waiting-days.md)
- [<span data-ttu-id="1f000-155">待機期間の構成</span><span class="sxs-lookup"><span data-stu-id="1f000-155">Configure waiting periods</span></span>](hr-benefits-setup-waiting-periods.md)
- [<span data-ttu-id="1f000-156">丸めルールの設定</span><span class="sxs-lookup"><span data-stu-id="1f000-156">Set up rounding rules</span></span>](hr-benefits-setup-rounding-rules.md)
- [<span data-ttu-id="1f000-157">従業員カテゴリの作成</span><span class="sxs-lookup"><span data-stu-id="1f000-157">Create employment categories</span></span>](hr-benefits-setup-employment-categories.md)
- [<span data-ttu-id="1f000-158">雇用タイプを設定</span><span class="sxs-lookup"><span data-stu-id="1f000-158">Set up employment types</span></span>](hr-benefits-setup-employment-types.md)
- [<span data-ttu-id="1f000-159">従業員のセルフ サービスを構成</span><span class="sxs-lookup"><span data-stu-id="1f000-159">Configure employee self service</span></span>](hr-benefits-setup-employee-self-service.md)

## <a name="create-benefit-plans"></a><span data-ttu-id="1f000-160">給付金プランの作成</span><span class="sxs-lookup"><span data-stu-id="1f000-160">Create benefit plans</span></span>

<span data-ttu-id="1f000-161">これらの記事では、バンドルおよびフレックス クレジット プログラムなどの給付金プランの作成方法を示します。</span><span class="sxs-lookup"><span data-stu-id="1f000-161">These articles show how to create benefit plans, including bundles and flex credit programs.</span></span>

- [<span data-ttu-id="1f000-162">給付金プランの設定</span><span class="sxs-lookup"><span data-stu-id="1f000-162">Set up benefit plans</span></span>](hr-benefits-plans-setup.md)
- [<span data-ttu-id="1f000-163">作業者の給付金プランの作成</span><span class="sxs-lookup"><span data-stu-id="1f000-163">Create worker benefit plans</span></span>](hr-benefits-plans-worker.md)
- [<span data-ttu-id="1f000-164">フレックス クレジット プログラムの設定</span><span class="sxs-lookup"><span data-stu-id="1f000-164">Set up flex credit programs</span></span>](hr-benefits-plans-flex-credit-programs.md)
- [<span data-ttu-id="1f000-165">将来のライフ イベントの構成</span><span class="sxs-lookup"><span data-stu-id="1f000-165">Configure future life events</span></span>](hr-benefits-plans-future-life-events.md)

## <a name="process-benefit-plans"></a><span data-ttu-id="1f000-166">給付金プランの処理</span><span class="sxs-lookup"><span data-stu-id="1f000-166">Process benefit plans</span></span>

<span data-ttu-id="1f000-167">変更を有効にするには、いくつかの変更を処理する必要があります。</span><span class="sxs-lookup"><span data-stu-id="1f000-167">You need to process some of your changes to make them active.</span></span>

- [<span data-ttu-id="1f000-168">登録の適格性を処理</span><span class="sxs-lookup"><span data-stu-id="1f000-168">Process enrollment eligibility</span></span>](hr-benefits-process-enrollment-eligibility.md)
- [<span data-ttu-id="1f000-169">ライフ イベントの処理</span><span class="sxs-lookup"><span data-stu-id="1f000-169">Process life events</span></span>](hr-benefits-process-life-events.md)
- [<span data-ttu-id="1f000-170">ライフ イベントの変更の処理</span><span class="sxs-lookup"><span data-stu-id="1f000-170">Process life event changes</span></span>](hr-benefits-process-life-event-changes.md)
- [<span data-ttu-id="1f000-171">ライフ イベントの適格性の処理</span><span class="sxs-lookup"><span data-stu-id="1f000-171">Process life event eligibility</span></span>](hr-benefits-process-life-event-eligibility.md)
- [<span data-ttu-id="1f000-172">レート変更の処理</span><span class="sxs-lookup"><span data-stu-id="1f000-172">Process rate changes</span></span>](hr-benefits-process-rate-changes.md)

