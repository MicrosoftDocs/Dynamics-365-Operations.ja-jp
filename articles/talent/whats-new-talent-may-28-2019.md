---
title: Dynamics 365 Talent (2019 年 5 月 28 日) の新機能および変更された機能
description: このトピックでは、Microsoft Dynamics 365 Talent の新機能または変更された機能について説明します。
author: Darinkramer
manager: AnnBe
ms.date: 05/28/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2019-05-28
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 29e941ddab1b2746ccd74d6e335fec7742d1391e
ms.sourcegitcommit: e89bb3e5420a6ece84f4e80c11e360b4a042f59d
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/17/2020
ms.locfileid: "4529611"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-may-28-2019"></a><span data-ttu-id="2026b-103">Dynamics 365 Talent (2019 年 5 月 28 日) の新機能および変更された機能</span><span class="sxs-lookup"><span data-stu-id="2026b-103">What's new or changed in Dynamics 365 Talent (May 28, 2019)</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="2026b-104">このトピックでは、Dynamics 365 Talent の新機能または変更された機能について説明します。</span><span class="sxs-lookup"><span data-stu-id="2026b-104">This topic describes features that are either new or changed in Dynamics 365 Talent.</span></span>

## <a name="changes-in-attract"></a><span data-ttu-id="2026b-105">Attract の変更</span><span class="sxs-lookup"><span data-stu-id="2026b-105">Changes in Attract</span></span>
<span data-ttu-id="2026b-106">今回のリリースには、Dynamics 365 Talent: Attract のマイナーなバグ修正が含まれています。</span><span class="sxs-lookup"><span data-stu-id="2026b-106">This release includes minor bug fixes for Dynamics 365 Talent: Attract.</span></span>

## <a name="coming-soon-in-attract"></a><span data-ttu-id="2026b-107">Attract で間もなく公開</span><span class="sxs-lookup"><span data-stu-id="2026b-107">Coming soon in Attract</span></span>

### <a name="job-approvals-on-home-page"></a><span data-ttu-id="2026b-108">ホーム ページのジョブ承認</span><span class="sxs-lookup"><span data-stu-id="2026b-108">Job approvals on home page</span></span>

<span data-ttu-id="2026b-109">承認は、ダッシュボードの **承認** セクションに表示されます。</span><span class="sxs-lookup"><span data-stu-id="2026b-109">Approvals appear in an **Approvals** section on the dashboard.</span></span> <span data-ttu-id="2026b-110">承認者は **自分に割り当て済み** で自分の承認を確認できます。ここではジョブ ID、職位、他の承認者、および割り当て日が表示されます。</span><span class="sxs-lookup"><span data-stu-id="2026b-110">Approvers can review their approvals under **Assigned to you**, which displays the job ID, title, other approvers, and date assigned.</span></span> <span data-ttu-id="2026b-111">承認のジョブを送信するユーザーは、**ユーザーにより要求済** で自分のジョブを確認できます。ここでは送信したジョブをまだ承認する必要がある承認者を表示します。</span><span class="sxs-lookup"><span data-stu-id="2026b-111">Users who submit a job for approval can review their jobs under **Requested by you**, which displays the approvers who still need to approve the submitted job.</span></span>

## <a name="changes-in-onboard"></a><span data-ttu-id="2026b-112">Onboard の変更</span><span class="sxs-lookup"><span data-stu-id="2026b-112">Changes in Onboard</span></span>
<span data-ttu-id="2026b-113">今回のリリースには、Dynamics 365 Talent: Onboard のマイナーなバグ修正が含まれています。</span><span class="sxs-lookup"><span data-stu-id="2026b-113">This release includes minor bug fixes for Dynamics 365 Talent: Onboard.</span></span>

## <a name="changes-in-core-hr"></a><span data-ttu-id="2026b-114">Core HR の変更</span><span class="sxs-lookup"><span data-stu-id="2026b-114">Changes in Core HR</span></span>
<span data-ttu-id="2026b-115">このセクションに記載された変更は、ビルド番号 8.1.2319 に適用されます。</span><span class="sxs-lookup"><span data-stu-id="2026b-115">Changes described in this section apply to build number 8.1.2319.</span></span>

### <a name="common-data-service-entity-support-for-custom-fields"></a><span data-ttu-id="2026b-116">カスタム フィールドに対する Common Data Service エンティティのサポート</span><span class="sxs-lookup"><span data-stu-id="2026b-116">Common Data Service entity support for custom fields</span></span>

<span data-ttu-id="2026b-117">このリリースでは、次の Common Data Service エンティティでカスタム フィールドがサポートされるようになりました。給付金の計算レートの詳細、作業カレンダーの休日行、および雇用です。</span><span class="sxs-lookup"><span data-stu-id="2026b-117">In this release, the following Common Data Service entities now support custom fields: Benefit calc rate detail, Work calendar holiday line, and Employment.</span></span>

### <a name="copy-position-now-includes-payroll-details"></a><span data-ttu-id="2026b-118">職位のコピーに給与詳細が含まれるようにする</span><span class="sxs-lookup"><span data-stu-id="2026b-118">Copy position now includes payroll details</span></span>
<span data-ttu-id="2026b-119">**職位のコピー** を使用してすべてのオプションを選択すると、給与の詳細情報がコピー情報に含まれるようになります。</span><span class="sxs-lookup"><span data-stu-id="2026b-119">When you use **Copy position** and select all of the options, the payroll details information is now included in the copy information.</span></span> 

## <a name="in-preview-in-core-hr"></a><span data-ttu-id="2026b-120">Core HR のプレビュー</span><span class="sxs-lookup"><span data-stu-id="2026b-120">In preview in Core HR</span></span>

### <a name="restrict-the-leave-types-in-time-off-requests"></a><span data-ttu-id="2026b-121">休暇申請で休暇タイプを制限する</span><span class="sxs-lookup"><span data-stu-id="2026b-121">Restrict the leave types in time off requests</span></span>

<span data-ttu-id="2026b-122">組織はさまざまな種類の休暇を従業員に提供できます。</span><span class="sxs-lookup"><span data-stu-id="2026b-122">Organizations can offer many different types of leave to employees.</span></span> <span data-ttu-id="2026b-123">いくつかの休暇タイプは、従業員が休暇を送信するのに適していない可能性があり、その代わりに人事管理 (HR) によって管理されます。</span><span class="sxs-lookup"><span data-stu-id="2026b-123">Some of these leave types might not be appropriate for employees to submit time off for and are managed by Human Resources (HR) instead.</span></span> <span data-ttu-id="2026b-124">このリリースでは、従業員が休暇申請を送信できる休暇タイプをコンフィギュレーションできます。</span><span class="sxs-lookup"><span data-stu-id="2026b-124">With this release, you can configure which leave types employees can submit time-off requests for.</span></span> 

### <a name="new-page-to-validate-position-hierarchy-data"></a><span data-ttu-id="2026b-125">職位階層データを検証する新しいページ</span><span class="sxs-lookup"><span data-stu-id="2026b-125">New page to validate position hierarchy data</span></span>

<span data-ttu-id="2026b-126">HR および管理者は、誤ってインポートされた循環参照に対して、管理階層を検証できます。</span><span class="sxs-lookup"><span data-stu-id="2026b-126">HR and administrators can validate the managerial hierarchy for any circular references that might have been inadvertently imported.</span></span> <span data-ttu-id="2026b-127">この新しいページは、**組織管理 > リンク > 職位 > 職位階層の検証** からアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="2026b-127">You can access this new page from **Organizational administration > Links > Positions > Position hierarchy validation**.</span></span>

### <a name="specify-reason-codes-on-leave-types"></a><span data-ttu-id="2026b-128">休暇タイプの理由コードの指定</span><span class="sxs-lookup"><span data-stu-id="2026b-128">Specify reason codes on leave types</span></span>

<span data-ttu-id="2026b-129">組織は、休暇申請に関する追加情報を要求する場合があります。</span><span class="sxs-lookup"><span data-stu-id="2026b-129">Organizations might require additional information about time-off requests.</span></span> <span data-ttu-id="2026b-130">休暇タイプに理由コードを指定し、従業員は休暇申請で理由コードを選択できるようになりました。</span><span class="sxs-lookup"><span data-stu-id="2026b-130">You can now specify reason codes for leave types and let employees select a reason code on their time-off requests.</span></span>

### <a name="require-reason-codes-for-specific-leave-types-on-time-off-requests"></a><span data-ttu-id="2026b-131">休暇申請で固有の休暇タイプについては理由コードが必要</span><span class="sxs-lookup"><span data-stu-id="2026b-131">Require reason codes for specific leave types on time-off requests</span></span>

<span data-ttu-id="2026b-132">従業員が休暇申請を送信するときに、組織は特定の休暇タイプに理由コードを要求することがあります。</span><span class="sxs-lookup"><span data-stu-id="2026b-132">Organizations might require reason codes for specific leave types when employees submit time-off requests.</span></span> <span data-ttu-id="2026b-133">この要件は、会社のポリシーや規制要件が原因であることがあります。</span><span class="sxs-lookup"><span data-stu-id="2026b-133">This requirement might exist because of company policy or regulatory requirements.</span></span> <span data-ttu-id="2026b-134">どの休暇タイプに理由コードが必要かを指定できます。また、従業員に休暇申請で休暇タイプに理由コードを指定するように要求できます。</span><span class="sxs-lookup"><span data-stu-id="2026b-134">You can specify which leave types require a reason code, and you can require that employees provide a reason code for the leave type on their time-off requests.</span></span>

### <a name="provide-a-leave-and-absence-transaction-list-for-hr"></a><span data-ttu-id="2026b-135">HR の休暇および欠勤トランザクション リストを提供します</span><span class="sxs-lookup"><span data-stu-id="2026b-135">Provide a leave and absence transaction list for HR</span></span>

<span data-ttu-id="2026b-136">従業員の休暇を追跡し、どのように計算するかを理解する機能は、HR が従業員の質問に答えるのに役立つだけでなく、従業員に正確な休暇を付与することにも役立ちます。</span><span class="sxs-lookup"><span data-stu-id="2026b-136">The ability to track employee time off and understand how time off is calculated not only helps HR answer employee questions, but also helps ensure accurate time-off awards for employees.</span></span> <span data-ttu-id="2026b-137">HR において、トランザクション (交付、見越、調整、および要求) の表示が新しくなり、HR スタッフは休暇残高の背後にある理由を確認することができるようになりました。</span><span class="sxs-lookup"><span data-stu-id="2026b-137">HR now has a new view into the transactions (grants, accruals, adjustments, and requests), so that HR staff can view the reasons behind time-off balances.</span></span>
