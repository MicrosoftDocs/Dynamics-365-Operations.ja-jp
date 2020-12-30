---
title: Dynamics 365 Talent (2019 年 10 月 29 日) の新機能および変更された機能
description: このトピックでは、Microsoft Dynamics 365 Talent の新機能または変更された機能について説明します。
author: Darinkramer
manager: AnnBe
ms.date: 10/29/2019
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
ms.search.validFrom: 2019-10-29
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 09d53c82b4244f20d0d7f301691b01263258a32f
ms.sourcegitcommit: e89bb3e5420a6ece84f4e80c11e360b4a042f59d
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/17/2020
ms.locfileid: "4529687"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-october-29-2019"></a><span data-ttu-id="e19de-103">Dynamics 365 Talent (2019 年 10 月 29 日) の新機能および変更された機能</span><span class="sxs-lookup"><span data-stu-id="e19de-103">What's new or changed in Dynamics 365 Talent (October 29, 2019)</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="e19de-104">このトピックでは、Dynamics 365 Talent の新機能または変更された機能について説明します。</span><span class="sxs-lookup"><span data-stu-id="e19de-104">This topic describes features that are either new or changed in Dynamics 365 Talent.</span></span>

## <a name="changes-in-attract"></a><span data-ttu-id="e19de-105">Attract の変更</span><span class="sxs-lookup"><span data-stu-id="e19de-105">Changes in Attract</span></span>

<span data-ttu-id="e19de-106">今回のリリースには、Dynamics 365 Talent: Attract のマイナーなバグ修正が含まれています。</span><span class="sxs-lookup"><span data-stu-id="e19de-106">This release includes minor bug fixes for Dynamics 365 Talent: Attract.</span></span>

## <a name="changes-in-onboard"></a><span data-ttu-id="e19de-107">Onboard の変更</span><span class="sxs-lookup"><span data-stu-id="e19de-107">Changes in Onboard</span></span>

<span data-ttu-id="e19de-108">今回のリリースには、Dynamics 365 Talent: Onboard のマイナーなバグ修正が含まれています。</span><span class="sxs-lookup"><span data-stu-id="e19de-108">This release includes minor bug fixes for Dynamics 365 Talent: Onboard.</span></span>

## <a name="changes-in-core-hr"></a><span data-ttu-id="e19de-109">Core HR の変更</span><span class="sxs-lookup"><span data-stu-id="e19de-109">Changes in Core HR</span></span>

<span data-ttu-id="e19de-110">このセクションに記載された変更は、ビルド番号 8.1.2586 に適用されます。</span><span class="sxs-lookup"><span data-stu-id="e19de-110">Changes described in this section apply to build number 8.1.2586.</span></span> <span data-ttu-id="e19de-111">ヘッダーにあるかっこ内の数字は、Microsoft Dynamics Lifecycle Services (LCS) のサポート番号を参照していることがあります。</span><span class="sxs-lookup"><span data-stu-id="e19de-111">The numbers in parentheses in some headings refer to support numbers in Microsoft Dynamics Lifecycle Services (LCS).</span></span>

### <a name="delete-parties-with-no-roles-should-be-on-by-default-371233"></a><span data-ttu-id="e19de-112">ロールのない関係者は既定で削除すべき (371233)</span><span class="sxs-lookup"><span data-stu-id="e19de-112">Delete parties with no roles should be on by default (371233)</span></span>

<span data-ttu-id="e19de-113">Talent で新しい環境をプロビジョニングする場合、**ロールが存在しない関係者を削除** が既定でオンになります。</span><span class="sxs-lookup"><span data-stu-id="e19de-113">When you provision a new environment in Talent, **Delete parties if no roles exist** is turned on by default.</span></span> <span data-ttu-id="e19de-114">この設定がオンになっている場合を除き、作業者を削除しても、作業者に関連付けられている関係者は削除されません。</span><span class="sxs-lookup"><span data-stu-id="e19de-114">When you delete a worker, the party associated with the worker is not removed unless this setting is on.</span></span> <span data-ttu-id="e19de-115">この変更により、作業者のインポート、変更、または再インポートを行う必要がある場合に、グローバル アドレス帳の重複レコードが制限されます。</span><span class="sxs-lookup"><span data-stu-id="e19de-115">This change limits duplicate records in the global address book when you need to import, change, or reimport workers.</span></span>

### <a name="draft-and-cancelled-leave-requests-should-be-allowed-to-be-deleted-in-common-data-service-376999"></a><span data-ttu-id="e19de-116">下書きおよびキャンセルされた休暇要求は、Common Data Service で削除が許可されるべき (376999)</span><span class="sxs-lookup"><span data-stu-id="e19de-116">Draft and cancelled leave requests should be allowed to be deleted in Common Data Service (376999)</span></span>

<span data-ttu-id="e19de-117">この変更により、Common Data Service でステータスが **下書き** または **キャンセル済** になっている休暇依頼を削除できます。</span><span class="sxs-lookup"><span data-stu-id="e19de-117">With this change, you can now delete leave requests with a status of **Draft** or **Cancelled** in Common Data Service.</span></span>

### <a name="additional-list-values-in-custom-fields-arent-reflected-in-common-data-service-after-clicking-apply-on-the-custom-fields-form-379599"></a><span data-ttu-id="e19de-118">カスタム フィールド フォームで適用をクリックしても、カスタム フィールドの追加リスト値が Common Data Service に反映されない (379599)</span><span class="sxs-lookup"><span data-stu-id="e19de-118">Additional list values in custom fields aren't reflected in Common Data Service after clicking Apply on the Custom fields form (379599)</span></span>

<span data-ttu-id="e19de-119">すでに Common Data Service と同期している既存のカスタム フィールドに新しいリスト値を追加すると、**カスタム フィールド** フォームで変更を適用した後に、Common Data Serivce で使用できるようになります。</span><span class="sxs-lookup"><span data-stu-id="e19de-119">When you add new list values to an existing custom field that has already synchronized with Common Data Service, they're now available in Common Data Serivce after you apply your changes in the **Custom fields** form.</span></span>

### <a name="apply-onboarding-checklists-across-legal-entities-when-more-than-one-employment-exists-371270"></a><span data-ttu-id="e19de-120">1 つ以上の雇用がある場合、会社間でオンボーディング チェックリストを適用 (371270)</span><span class="sxs-lookup"><span data-stu-id="e19de-120">Apply onboarding checklists across legal entities when more than one employment exists (371270)</span></span>

<span data-ttu-id="e19de-121">今週のリリースにより、**作業者フォーム > チェックリスト** で、1 つ以上の雇用のある従業員にチェックリストを適用することができます。</span><span class="sxs-lookup"><span data-stu-id="e19de-121">In this week's release, you can apply checklists to employees with more than one employment in **Worker form > Checklists**.</span></span>

### <a name="benefits-open-enrollment-preview-feature-has-been-removed"></a><span data-ttu-id="e19de-122">福利厚生の自由登録プレビュー機能は削除されました</span><span class="sxs-lookup"><span data-stu-id="e19de-122">Benefits open enrollment preview feature has been removed</span></span>

<span data-ttu-id="e19de-123">Microsoft では、[Core HR ドライブのオペレーショナル エクセレンスにおける戦略的投資](https://cloudblogs.microsoft.com/dynamics365/bdm/2019/10/02/strategic-investments-in-core-hr-drive-operational-excellence)ブログ投稿におけるお知らせと共に、パブリック プレビューから福利厚生の自由登録機能を削除しました。</span><span class="sxs-lookup"><span data-stu-id="e19de-123">In conjunction with our announcement in the [Strategic investments in core HR drive operational excellence](https://cloudblogs.microsoft.com/dynamics365/bdm/2019/10/02/strategic-investments-in-core-hr-drive-operational-excellence) blog post, Microsoft has removed the benefits open enrollment feature from public preview.</span></span> <span data-ttu-id="e19de-124">新しい機能が将来リリースされます。</span><span class="sxs-lookup"><span data-stu-id="e19de-124">New functionality will be released in the future.</span></span> <span data-ttu-id="e19de-125">福利厚生の自由登録機能は、運用上の用途としてはまだサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="e19de-125">Production use of the benefits open enrollment feature isn't be supported.</span></span>

## <a name="coming-soon"></a><span data-ttu-id="e19de-126">間もなく公開</span><span class="sxs-lookup"><span data-stu-id="e19de-126">Coming soon</span></span>

### <a name="print-performance-reviews"></a><span data-ttu-id="e19de-127">業績の確認の印刷</span><span class="sxs-lookup"><span data-stu-id="e19de-127">Print performance reviews</span></span>

<span data-ttu-id="e19de-128">詳細については、Dynamics 365: 2019 リリース ウェーブ 2 プランにある[業績の確認の印刷](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-talent/print-performance-reviews)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="e19de-128">See [Print performance reviews](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-talent/print-performance-reviews) in the Dynamics 365: 2019 release wave 2 plan.</span></span>

### <a name="feature-management-workspace"></a><span data-ttu-id="e19de-129">機能管理ワークスペース</span><span class="sxs-lookup"><span data-stu-id="e19de-129">Feature management workspace</span></span>

<span data-ttu-id="e19de-130">機能は、すべてのリリースで追加および更新されます</span><span class="sxs-lookup"><span data-stu-id="e19de-130">Features are added and updated in every release.</span></span> <span data-ttu-id="e19de-131">機能管理エクスペリエンスは、各リリースで提供されている機能のリストを表示できるワークスペースを提供します。</span><span class="sxs-lookup"><span data-stu-id="e19de-131">The feature management experience provides a workspace where you can view a list of features that have been delivered in each release.</span></span> <span data-ttu-id="e19de-132">既定では、新機能が無効になっています。</span><span class="sxs-lookup"><span data-stu-id="e19de-132">By default, new features are turned off.</span></span> <span data-ttu-id="e19de-133">ワークスペースを使用してそれらを有効にし、それらのドキュメントを参照できます。</span><span class="sxs-lookup"><span data-stu-id="e19de-133">You can use the workspace to turn them on and view the documentation for them.</span></span>

<span data-ttu-id="e19de-134">機能管理に伴う変更の詳細については、[機能管理の概要](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="e19de-134">To learn more about the changes coming with feature management, see [Feature management overview](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview).</span></span>
