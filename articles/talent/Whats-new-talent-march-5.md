---
title: Dynamics 365 Talent の新機能および変更された機能 (2019 年 3 月 5 日)
description: このトピックでは、Microsoft Dynamics 365 Talent の新機能または変更された機能について説明します。
author: Darinkramer
manager: AnnBe
ms.date: 03/05/2019
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
ms.search.validFrom: 2019-03-05
ms.dyn365.ops.version: Talent
ms.openlocfilehash: c7ee8f4cf14197d6bd4549741058fc5fe95ae55d
ms.sourcegitcommit: f87de0f949b5d60993b19e0f61297f02d42b5bef
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2019
ms.locfileid: "2026673"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-march-5-2019"></a><span data-ttu-id="03ef5-103">Dynamics 365 Talent の新機能および変更された機能 (2019 年 3 月 5 日)</span><span class="sxs-lookup"><span data-stu-id="03ef5-103">What's new or changed in Dynamics 365 Talent (March 5, 2019)</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="03ef5-104">このトピックでは、 Talent の新機能または変更された機能について説明します。</span><span class="sxs-lookup"><span data-stu-id="03ef5-104">This topic describes features that are either new or changed in Talent.</span></span>

## <a name="changes-in-attract"></a><span data-ttu-id="03ef5-105">Attract の変更</span><span class="sxs-lookup"><span data-stu-id="03ef5-105">Changes in Attract</span></span>

### <a name="extending-option-sets-in-attract"></a><span data-ttu-id="03ef5-106">Attract のオプション セットの拡張</span><span class="sxs-lookup"><span data-stu-id="03ef5-106">Extending option sets in Attract</span></span>

<span data-ttu-id="03ef5-107">Attract には、Common Data Service 内のオプション セットである複数のフィールドがあります。</span><span class="sxs-lookup"><span data-stu-id="03ef5-107">In Attract, there are multiple fields that are option sets within the Common Data Service.</span></span> <span data-ttu-id="03ef5-108">**不採用**理由フィールド、**雇用タイプ**フィールド、および**勤続タイプ**フィールドをはじめとするオプション セットを拡張するための新しい機能が導入されました。</span><span class="sxs-lookup"><span data-stu-id="03ef5-108">New capabilities have been introduced to extend the option sets, beginning with the **Rejection** reason field, **Employment type** field, and **Seniority type** field.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="03ef5-109">LinkedIn 機能へのジョブ求人転記には、**ジョブの詳細**ページの**雇用タイプ**および**勤続タイプ**フィールドの使用が求められます。</span><span class="sxs-lookup"><span data-stu-id="03ef5-109">The job posting to LinkedIn functionality requires the use of the **Employment type** and **Seniority type** fields on the **Job details** page.</span></span> <span data-ttu-id="03ef5-110">これらのフィールドの既定値は LinkedIn でサポートされ、ジョブが転記されるときに表示されます。</span><span class="sxs-lookup"><span data-stu-id="03ef5-110">The default values in these fields are supported by LinkedIn and are displayed when the job is posted.</span></span> <span data-ttu-id="03ef5-111">LinkedIn にジョブ求人を転記していて、これらのフィールドの既存のオプション セット値を変更した場合、ジョブ求人は転記されますが、LinkedIn はカスタム**雇用タイプ**および**勤続タイプ**の値を表示しません。</span><span class="sxs-lookup"><span data-stu-id="03ef5-111">If you are posting jobs to LinkedIn and you modify the existing option set values for these fields, the job will still post, but LinkedIn will not display the custom **Employment type** and **Seniority type** values.</span></span>

## <a name="changes-in-onboarding"></a><span data-ttu-id="03ef5-112">オンボードの変更</span><span class="sxs-lookup"><span data-stu-id="03ef5-112">Changes in Onboarding</span></span>

### <a name="private-preview-for-onboard-teams"></a><span data-ttu-id="03ef5-113">Onboard チームのプライベート プレビュー</span><span class="sxs-lookup"><span data-stu-id="03ef5-113">Private preview for Onboard teams</span></span>
<span data-ttu-id="03ef5-114">組織全体でテンプレートを簡単に共有して共同作業できるようになりました。</span><span class="sxs-lookup"><span data-stu-id="03ef5-114">You can now easily share and collaborate on templates across your entire organization.</span></span> <span data-ttu-id="03ef5-115">詳細については、[Onboard チームを使用して、組織全体のベスト プラクティスを共有する](https://docs.microsoft.com/business-applications-release-notes/April19/dynamics365-talent/onboard/share-best-practices-teams) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="03ef5-115">For more information, see [Share best practices across your organization using Onboard Teams](https://docs.microsoft.com/business-applications-release-notes/April19/dynamics365-talent/onboard/share-best-practices-teams).</span></span>

### <a name="private-preview-for-assignee-placeholders"></a><span data-ttu-id="03ef5-116">割り当て先のプレース ホルダーのプライベート プレビュー</span><span class="sxs-lookup"><span data-stu-id="03ef5-116">Private preview for assignee placeholders</span></span>
<span data-ttu-id="03ef5-117">活動を個人の代わりにロールに割り当てることにより、テンプレートを強化できます。</span><span class="sxs-lookup"><span data-stu-id="03ef5-117">You can enrich your templates by assigning activities to roles instead of individuals.</span></span> <span data-ttu-id="03ef5-118">ロールは、ガイドの作成時に個人に割り当てられます。</span><span class="sxs-lookup"><span data-stu-id="03ef5-118">Roles are then assigned to individuals at the time of guide creation.</span></span> <span data-ttu-id="03ef5-119">詳細については、[活動をロールに割り当てることによってガイド管理を合理化する](https://docs.microsoft.com/business-applications-release-notes/April19/dynamics365-talent/onboard/assign-activities-roles) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="03ef5-119">For more information, see [Streamline guide administration by assigning activities to roles](https://docs.microsoft.com/business-applications-release-notes/April19/dynamics365-talent/onboard/assign-activities-roles).</span></span>

## <a name="changes-in-core-hr"></a><span data-ttu-id="03ef5-120">Core HR の変更</span><span class="sxs-lookup"><span data-stu-id="03ef5-120">Changes in Core HR</span></span>
<span data-ttu-id="03ef5-121">**ビルド 8.1.2178**</span><span class="sxs-lookup"><span data-stu-id="03ef5-121">**Build 8.1.2178**</span></span>

### <a name="configure-workflow-to-auto-approve-or-follow-workflow-when-an-hr-or-line-manager-submits-or-updates-time-off-requests"></a><span data-ttu-id="03ef5-122">HR または明細行のマネージャーが休暇申請を送信または更新するときに、ワークフローを自動承認またはワークフローに従うようにコンフィギュレーションします。</span><span class="sxs-lookup"><span data-stu-id="03ef5-122">Configure workflow to auto-approve or follow workflow when an HR or line manager submits or updates time off requests</span></span>
<span data-ttu-id="03ef5-123">従業員のマネージャーまたは HR によって提出された場合に休暇要求が自動的に承認されるように、新しいワークフローの条件が追加されました。</span><span class="sxs-lookup"><span data-stu-id="03ef5-123">New workflow conditions have been added to allow for leave requests to be automatically approved if submitted by an employee’s manager or by HR.</span></span> <span data-ttu-id="03ef5-124">ワークフローでのこの自動承認を達成するための 1 つの方法は、ワークフローの承認で自動アクションを有効にすることです。</span><span class="sxs-lookup"><span data-stu-id="03ef5-124">One way to achieve this auto-approval on a workflow is to enable an automatic action on the workflow approval.</span></span>

<span data-ttu-id="03ef5-125">追加された条件には以下が含まれます:</span><span class="sxs-lookup"><span data-stu-id="03ef5-125">The conditions that have been added include:</span></span>

- <span data-ttu-id="03ef5-126">送信者 - 要求をワークフローに送信したユーザーのシステムのユーザー ID を評価するために使用します。</span><span class="sxs-lookup"><span data-stu-id="03ef5-126">Submitted by - Used to evaluate the system user ID of the user who submitted the request to workflow.</span></span>
- <span data-ttu-id="03ef5-127">次のユーザーの代理で送信 - 休暇要求が要求に関連付けられている作業者の代理として送信されたかどうかを評価するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="03ef5-127">Submitted on behalf of - Used to evaluate if the leave request was submitted on behalf of the worker associated to the request.</span></span>
- <span data-ttu-id="03ef5-128">人事管理が送信 - 要求をワークフローに送信したシステム ユーザーが人事管理ロールに属しているかどうかを評価するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="03ef5-128">Submitted by human resources - Used to evaluate if the system user who submitted the request to workflow is in a Human Resources role.</span></span>
- <span data-ttu-id="03ef5-129">マネージャーが送信 - ワークフローに休暇要求を送信したユーザーが要求に関連付けられている作業者の明細行の階層マネージャーかどうかを評価するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="03ef5-129">Submitted by manager - Used to evaluate if the user who submitted the leave request to workflow is a line hierarchy manager of the worker associated to the request.</span></span>

### <a name="enable-employee-fixed-compensation-for-future-position-assignments"></a><span data-ttu-id="03ef5-130">従業員の固定報酬を将来の職位の割り当てのために有効化する</span><span class="sxs-lookup"><span data-stu-id="03ef5-130">Enable employee fixed compensation for future position assignments</span></span>
<span data-ttu-id="03ef5-131">従業員が将来の開始日で組織に参加するのは一般的です。</span><span class="sxs-lookup"><span data-stu-id="03ef5-131">It is typical for employees to join an organization with a future start date.</span></span> <span data-ttu-id="03ef5-132">この変更により、将来の職位の割り当てを持つ従業員に対する固定報酬の定義が有効化されます。</span><span class="sxs-lookup"><span data-stu-id="03ef5-132">This change enables defining fixed compensation for employees with future position assignments.</span></span>

### <a name="position-payroll-fields-are-blank-when-editing-the-position"></a><span data-ttu-id="03ef5-133">職位の編集時に職位給与フィールドが空白になる</span><span class="sxs-lookup"><span data-stu-id="03ef5-133">Position Payroll fields are blank when editing the position</span></span>
<span data-ttu-id="03ef5-134">この変更により、既存の職位の変更を要求するときに、給与フィールドは既定で現在の値になります。</span><span class="sxs-lookup"><span data-stu-id="03ef5-134">With this change, when requesting changes to existing positions, the payroll fields will now default to the current values.</span></span>

### <a name="other-miscellaneous-bug-fixes"></a><span data-ttu-id="03ef5-135">その他の雑費のバグ修正</span><span class="sxs-lookup"><span data-stu-id="03ef5-135">Other miscellaneous bug fixes</span></span>
<span data-ttu-id="03ef5-136">このリリースには、他のマイナーなバグ修正が含まれています。</span><span class="sxs-lookup"><span data-stu-id="03ef5-136">Other minor bug fixes are included with this release.</span></span>

### <a name="upgrade-to-common-data-service"></a><span data-ttu-id="03ef5-137">Common Data Service へのアップグレード</span><span class="sxs-lookup"><span data-stu-id="03ef5-137">Upgrade to Common Data Service</span></span>
<span data-ttu-id="03ef5-138">Common Data Service へのアップグレードの期限が近づいています。</span><span class="sxs-lookup"><span data-stu-id="03ef5-138">Deadlines to upgrade to Common Data Service are quickly approaching.</span></span> <span data-ttu-id="03ef5-139">データベースをアップグレードする必要があるかどうかを決定するために、PowerApps 管理者センターにサインインします。</span><span class="sxs-lookup"><span data-stu-id="03ef5-139">Sign in to the PowerApps Admin center to determine if your database needs to be upgraded.</span></span> <span data-ttu-id="03ef5-140">期限およびアップグレードに必要な手順の詳細については、[Common Data Service へのアップグレード](https://docs.microsoft.com/common-data-service/upgradecds/introduction-upgrade-cds) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="03ef5-140">For more information about deadlines and necessary steps to upgrade, see [Upgrade to Common Data Service](https://docs.microsoft.com/common-data-service/upgradecds/introduction-upgrade-cds).</span></span>

## <a name="coming-soon"></a><span data-ttu-id="03ef5-141">間もなく公開</span><span class="sxs-lookup"><span data-stu-id="03ef5-141">Coming soon</span></span>

###  <a name="advanced-compensation-security-fixed-and-variable"></a><span data-ttu-id="03ef5-142">高度な報酬セキュリティ (固定および変動)</span><span class="sxs-lookup"><span data-stu-id="03ef5-142">Advanced compensation security (fixed and variable)</span></span>
<span data-ttu-id="03ef5-143">多くの組織で、報酬および福利厚生のマネージャーは、経営幹部または地域の従業員のレコードなど、特定の報酬レコードにのみアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="03ef5-143">In many organizations, compensation and benefits managers can only access certain compensation records, such as records for executives or regional-based employees.</span></span> <span data-ttu-id="03ef5-144">この変更により、組織内のさまざまな従業員数の報酬プランを管理および維持できます。</span><span class="sxs-lookup"><span data-stu-id="03ef5-144">With this change, you can manage and maintain the compensation plans for different employee populations in the organization.</span></span> <span data-ttu-id="03ef5-145">固定および変動プランにはセキュリティ ロールを割り当てることができます。これは、プランへのアクセス権とプランに関連する従業員データ (給与または特別償却レコードなど) を決定します。</span><span class="sxs-lookup"><span data-stu-id="03ef5-145">Fixed and variable plans can be assigned security roles, which will determine the access to the plans and the employee data related to the plans, such as salary or bonus records.</span></span> <span data-ttu-id="03ef5-146">与えられたアクセス権を持つロールのみが、それらの従業員の報酬を処理できます。</span><span class="sxs-lookup"><span data-stu-id="03ef5-146">Only the roles with the given access will be able to process compensation for those employees.</span></span>

###  <a name="platform-update-24-for-finance-and-operations"></a><span data-ttu-id="03ef5-147">Finance and Operations のプラットフォーム更新プログラム 24</span><span class="sxs-lookup"><span data-stu-id="03ef5-147">Platform update 24 for Finance and Operations</span></span>
<span data-ttu-id="03ef5-148">Finance and Operations のプラットフォーム更新プログラム 24 の詳細については、[Finance and Operations プラットフォーム更新プログラム 24 (2019 年 3 月) の新機能と変更された機能](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/get-started/whats-new-platform-update-24) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="03ef5-148">For additional details about Platform update 24 for Finance and Operations, see [What's new or changed in Finance and Operations platform update 24 (March 2019)](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/get-started/whats-new-platform-update-24).</span></span>
