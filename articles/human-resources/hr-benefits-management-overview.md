---
title: 福利厚生の管理の概要
description: Dynamics 365 Human Resources の福利厚生の管理機能の概要。 使いやすいオンライン エクスペリエンスで、従業員に拡張された給付金オプションを提供します。
author: andreabichsel
ms.date: 04/21/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 1b6ace2ce83c668e83ec1b433f8062148a6dfaf4
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/18/2021
ms.locfileid: "6059067"
---
# <a name="benefits-management-overview"></a><span data-ttu-id="929ff-104">給付金管理の概要</span><span class="sxs-lookup"><span data-stu-id="929ff-104">Benefits management overview</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="929ff-105">競争力を維持するには、最高の従業員を獲得し維持するために、充実したメリットを提供する必要があります。</span><span class="sxs-lookup"><span data-stu-id="929ff-105">To remain competitive, you must offer a rich set of benefits to attract and retain your best employees.</span></span> <span data-ttu-id="929ff-106">医療や歯科などの標準的な利点に加えて、採用支援、レクリエーション プログラム、および衣料手当などの拡張サービスを提供することもできます。</span><span class="sxs-lookup"><span data-stu-id="929ff-106">In addition to standard benefits like medical and dental coverage, you might also want to offer expanded services like adoption assistance, recreation programs, and clothing allowances.</span></span> <span data-ttu-id="929ff-107">Microsoft Dynamics 365 Human Resources の福利厚生の管理には、さまざまな福利厚生オプションをサポートする柔軟なソリューションが用意されています。</span><span class="sxs-lookup"><span data-stu-id="929ff-107">Benefits management in Microsoft Dynamics 365 Human Resources provides you with a flexible solution that supports a wide variety of benefit options.</span></span> <span data-ttu-id="929ff-108">人事管理では、製品を紹介するための使いやすい従業員エクスペリエンスも含まれています。</span><span class="sxs-lookup"><span data-stu-id="929ff-108">Human Resources also includes an easy-to-use employee experience that showcases your offerings.</span></span>

- <span data-ttu-id="929ff-109">拡張された給付金プランを使用すると、独自の給付金プランを作成および管理し、複雑な給付金のレート テーブルとネストされた階層をサポートできます。</span><span class="sxs-lookup"><span data-stu-id="929ff-109">Enhanced benefits plans let you create and manage unique benefit plans and support complex benefit rate tables and nested tiers.</span></span> <span data-ttu-id="929ff-110">より簡単な従業員エクスペリエンスのために、給付金プログラム、バンドル、および自動登録ルールを容易に作成できます。</span><span class="sxs-lookup"><span data-stu-id="929ff-110">You can easily create benefit programs, bundles, and auto-enrollment rules for an easier employee experience.</span></span>

- <span data-ttu-id="929ff-111">レックス クレジット プログラムでは、退職やその他のライフ イベントをサポートします。</span><span class="sxs-lookup"><span data-stu-id="929ff-111">Flex credit programs let you prorate to support retirement and other life events.</span></span>

- <span data-ttu-id="929ff-112">広範な適格性ルールによって、適切な従業員が適切な利益を得ることができます。</span><span class="sxs-lookup"><span data-stu-id="929ff-112">Extensive eligibility rules ensure you make the right benefits available to the right employees.</span></span>

- <span data-ttu-id="929ff-113">オンライン給付金の登録は、従業員にとって簡単なエクスペリエンスです。</span><span class="sxs-lookup"><span data-stu-id="929ff-113">Online benefits enrollment provides an easy experience for your employees.</span></span>

- <span data-ttu-id="929ff-114">認定されたライフ イベント処理は将来のライフ イベントをサポートします。</span><span class="sxs-lookup"><span data-stu-id="929ff-114">Qualified life event processing supports future life events.</span></span>

<span data-ttu-id="929ff-115">デモ データにアクセスする場合は、サンドボックス環境を再配置する必要があります。</span><span class="sxs-lookup"><span data-stu-id="929ff-115">If you would like to access the demo data, you'll need to redeploy your sandbox environment.</span></span>

>[!NOTE]
><span data-ttu-id="929ff-116">これで、給付金管理フォームをカスタマイズできます。</span><span class="sxs-lookup"><span data-stu-id="929ff-116">You can now customize Benefits management forms.</span></span> <span data-ttu-id="929ff-117">補償レートに関連するカスタム フィールドを、給付金計画の **補償オプション** フォームに追加できます。</span><span class="sxs-lookup"><span data-stu-id="929ff-117">You can now add custom fields related to coverage rates to the **Coverage option** form for benefit plans.</span></span> <span data-ttu-id="929ff-118">カスタム フィールドの操作についての詳細については、[カスタム フィールド](hr-developer-custom-fields.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="929ff-118">For more information about working with custom fields, see [Custom fields](hr-developer-custom-fields.md).</span></span>
><span data-ttu-id="929ff-119">![給付金管理カスタム フィールド](media/hr-benefits-management-custom-fields.png)</span><span class="sxs-lookup"><span data-stu-id="929ff-119">![Benefits management custom fields](media/hr-benefits-management-custom-fields.png)</span></span>

## <a name="enable-benefits-management"></a><span data-ttu-id="929ff-120">給付金管理を有効にする</span><span class="sxs-lookup"><span data-stu-id="929ff-120">Enable Benefits management</span></span>

<span data-ttu-id="929ff-121">このトピックでは、Human Resources の機能を有効にする方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="929ff-121">This topic describes how to turn on features in Human Resources.</span></span> <span data-ttu-id="929ff-122">また、福利厚生の管理を有効にすると、福利厚生の管理が置換されるか無効になる Human Resources の既存機能も示されます。</span><span class="sxs-lookup"><span data-stu-id="929ff-122">It also tells which existing features in Human Resources that Benefits management replaces or are disabled once you turn on Benefits management.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="929ff-123">**実稼働** 環境で福利厚生の管理を有効にした後、無効にすることはできません。</span><span class="sxs-lookup"><span data-stu-id="929ff-123">After you enable Benefits management in a **Production** environment, you can't disable it.</span></span> <span data-ttu-id="929ff-124">**実稼働** 環境で有効にする前に、**サンドボックス** 環境で福利厚生の管理を有効にしてテストすることをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="929ff-124">We recommend enabling and testing Benefits management in a **Sandbox** environment before enabling it in a **Production** environment.</span></span> <span data-ttu-id="929ff-125">従来の福利厚生機能と新しい福利厚生の管理機能には大きな違いがあり、追加の設定が必要であり、実稼働前にテストする必要があります。</span><span class="sxs-lookup"><span data-stu-id="929ff-125">There are significant differences between the legacy Benefit functionality and new Benefits management functionality that require additional setup and should be tested prior to being placed into production.</span></span>

- [<span data-ttu-id="929ff-126">機能の管理</span><span class="sxs-lookup"><span data-stu-id="929ff-126">Manage features</span></span>](hr-admin-manage-features.md)

## <a name="configure-employee-information"></a><span data-ttu-id="929ff-127">従業員情報のコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="929ff-127">Configure employee information</span></span>

<span data-ttu-id="929ff-128">従業員を福利厚生に登録する前に、必要な情報を提供する必要があります。</span><span class="sxs-lookup"><span data-stu-id="929ff-128">Before you can enroll employees in benefits, you must provide required information.</span></span> <span data-ttu-id="929ff-129">従業員を開始日に **固定報酬プラン** に登録し、**従業員** フォームの **従業員の詳細** で **給付金支払頻度** を選択する必要があります。</span><span class="sxs-lookup"><span data-stu-id="929ff-129">You must enroll an employee in a **Fixed compensation plan** on their start date, and you must select a **Benefit pay frequency** in **Employment details** on the **Worker** form.</span></span>

<span data-ttu-id="929ff-130">コミッションなどの補足報酬を受け取る従業員がいる場合は、従業員レコードから **福利厚生の年間給与** 額を追加できます。</span><span class="sxs-lookup"><span data-stu-id="929ff-130">If you have an employee who receives supplemental compensation like commissions, you can add a **Benefits annual salary** amount from the employee record.</span></span> <span data-ttu-id="929ff-131">Human Resources では、補償範囲額を決定する際に、固定報酬の年間金額ではなく、**福利厚生の年間給与** 額を使用します。</span><span class="sxs-lookup"><span data-stu-id="929ff-131">Human Resources will use the **Benefits annual salary** amount when determining coverage amounts, instead of the fixed compensation annual amount.</span></span> <span data-ttu-id="929ff-132">**福利厚生の年間給与** は、従業員の開始日または受給期間の開始日のいずれか遅い方の日付で有効である必要があります。</span><span class="sxs-lookup"><span data-stu-id="929ff-132">The **Benefits annual salary** must be valid as of the employee’s start date or the beginning of the benefit period, whichever is latest.</span></span> <span data-ttu-id="929ff-133">従業員に対して固定報酬と福利厚生の年間給与額の両方が記録されている場合、福利厚生の年間給与が補償範囲額の決定に使用されます。</span><span class="sxs-lookup"><span data-stu-id="929ff-133">If both a fixed compensation and benefits annual salary amount is recorded for an employee, the benefits annual salary will be used in determining coverage amounts.</span></span>

<span data-ttu-id="929ff-134">性別または年齢に基づくレートを使用する給付金プランを作成する場合、従業員が福利厚生コストを計算するには、生年月日と性別を入力する必要があります。</span><span class="sxs-lookup"><span data-stu-id="929ff-134">When you create a benefit plan that uses rates that are based on gender or age, you must enter a birth date and gender for the employee to calculate the benefit cost.</span></span>

## <a name="configure-benefits-management"></a><span data-ttu-id="929ff-135">福利厚生の管理のコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="929ff-135">Configure Benefits management</span></span>

<span data-ttu-id="929ff-136">従業員の給付金計画を作成する前に、その計画のオプションを構成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="929ff-136">Before you can create benefit plans for your employees, you need to configure options for the plans.</span></span>

- [<span data-ttu-id="929ff-137">給付金管理パラメーターを設定</span><span class="sxs-lookup"><span data-stu-id="929ff-137">Set Benefits management parameters</span></span>](hr-benefits-setup-parameters.md)
- [<span data-ttu-id="929ff-138">適格性ルールとオプションを構成</span><span class="sxs-lookup"><span data-stu-id="929ff-138">Configure eligibility rules and options</span></span>](hr-benefits-setup-eligibility-rules.md)
- [<span data-ttu-id="929ff-139">個人の連絡先の適格性オプションのコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="929ff-139">Configure personal contact eligibility options</span></span>](hr-benefits-setup-contact-eligibility-options.md)
- [<span data-ttu-id="929ff-140">補充オプションの作成</span><span class="sxs-lookup"><span data-stu-id="929ff-140">Create coverage options</span></span>](hr-benefits-setup-coverage-options.md)
- [<span data-ttu-id="929ff-141">支払頻度の設定</span><span class="sxs-lookup"><span data-stu-id="929ff-141">Set up payment frequencies</span></span>](hr-benefits-setup-payment-frequencies.md)
- [<span data-ttu-id="929ff-142">ライフ イベント タイプのコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="929ff-142">Configure life event types</span></span>](hr-benefits-setup-life-event-types.md)
- [<span data-ttu-id="929ff-143">計画タイプの作成</span><span class="sxs-lookup"><span data-stu-id="929ff-143">Create plan types</span></span>](hr-benefits-setup-plan-types.md)
- [<span data-ttu-id="929ff-144">理由コードの設定</span><span class="sxs-lookup"><span data-stu-id="929ff-144">Set up reason codes</span></span>](hr-benefits-setup-reason-codes.md)
- [<span data-ttu-id="929ff-145">層コードの設定</span><span class="sxs-lookup"><span data-stu-id="929ff-145">Set up tier codes</span></span>](hr-benefits-setup-tier-codes.md)
- [<span data-ttu-id="929ff-146">レートのコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="929ff-146">Configure rates</span></span>](hr-benefits-setup-rates.md)
- [<span data-ttu-id="929ff-147">控除のコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="929ff-147">Configure deductions</span></span>](hr-benefits-setup-deductions.md)
- [<span data-ttu-id="929ff-148">待機日数のコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="929ff-148">Configure waiting days</span></span>](hr-benefits-setup-waiting-days.md)
- [<span data-ttu-id="929ff-149">待機期間のコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="929ff-149">Configure waiting periods</span></span>](hr-benefits-setup-waiting-periods.md)
- [<span data-ttu-id="929ff-150">丸めルールの設定</span><span class="sxs-lookup"><span data-stu-id="929ff-150">Set up rounding rules</span></span>](hr-benefits-setup-rounding-rules.md)
- [<span data-ttu-id="929ff-151">雇用カテゴリの作成</span><span class="sxs-lookup"><span data-stu-id="929ff-151">Create employment categories</span></span>](hr-benefits-setup-employment-categories.md)
- [<span data-ttu-id="929ff-152">雇用タイプを設定</span><span class="sxs-lookup"><span data-stu-id="929ff-152">Set up employment types</span></span>](hr-benefits-setup-employment-types.md)
- [<span data-ttu-id="929ff-153">従業員のセルフ サービスを構成</span><span class="sxs-lookup"><span data-stu-id="929ff-153">Configure employee self service</span></span>](hr-benefits-setup-employee-self-service.md)

## <a name="create-benefit-plans"></a><span data-ttu-id="929ff-154">給付金プランの作成</span><span class="sxs-lookup"><span data-stu-id="929ff-154">Create benefit plans</span></span>

<span data-ttu-id="929ff-155">これらの記事では、バンドルおよびフレックス クレジット プログラムなどの給付金プランの作成方法を示します。</span><span class="sxs-lookup"><span data-stu-id="929ff-155">These articles show how to create benefit plans, including bundles and flex credit programs.</span></span>

- [<span data-ttu-id="929ff-156">福利厚生計画の設定</span><span class="sxs-lookup"><span data-stu-id="929ff-156">Set up benefit plans</span></span>](hr-benefits-plans-setup.md)
- [<span data-ttu-id="929ff-157">フレックス クレジット プログラムの設定</span><span class="sxs-lookup"><span data-stu-id="929ff-157">Set up flex credit programs</span></span>](hr-benefits-plans-flex-credit-programs.md)

## <a name="process-benefit-plans"></a><span data-ttu-id="929ff-158">福利厚生計画の処理</span><span class="sxs-lookup"><span data-stu-id="929ff-158">Process benefit plans</span></span>

<span data-ttu-id="929ff-159">変更を有効にするには、いくつかの変更を処理する必要があります。</span><span class="sxs-lookup"><span data-stu-id="929ff-159">You need to process some of your changes to make them active.</span></span>

- [<span data-ttu-id="929ff-160">登録の適格性を処理</span><span class="sxs-lookup"><span data-stu-id="929ff-160">Process enrollment eligibility</span></span>](hr-benefits-process-enrollment-eligibility.md)
- [<span data-ttu-id="929ff-161">ライフ イベントの処理</span><span class="sxs-lookup"><span data-stu-id="929ff-161">Process life events</span></span>](hr-benefits-process-life-events.md)
- [<span data-ttu-id="929ff-162">ライフ イベントの変更の処理</span><span class="sxs-lookup"><span data-stu-id="929ff-162">Process life event changes</span></span>](hr-benefits-process-life-event-changes.md)
- [<span data-ttu-id="929ff-163">ライフ イベントの適格性の処理</span><span class="sxs-lookup"><span data-stu-id="929ff-163">Process life event eligibility</span></span>](hr-benefits-process-life-event-eligibility.md)
- [<span data-ttu-id="929ff-164">レート変更の処理</span><span class="sxs-lookup"><span data-stu-id="929ff-164">Process rate changes</span></span>](hr-benefits-process-rate-changes.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]