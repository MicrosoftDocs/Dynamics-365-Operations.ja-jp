---
title: Dynamics 365 Talent (2019 年 4 月 16 日) の新機能および変更された機能
description: このトピックでは、Microsoft Dynamics 365 Talent の新機能または変更された機能について説明します。
author: Darinkramer
manager: AnnBe
ms.date: 04/16/2019
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
ms.search.validFrom: 2019-04-16
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 0781a479ebf37334d8eba18ea6d69d7cfb9db9ea
ms.sourcegitcommit: f87de0f949b5d60993b19e0f61297f02d42b5bef
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2019
ms.locfileid: "2024140"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-april-16-2019"></a><span data-ttu-id="f089b-103">Dynamics 365 Talent (2019 年 4 月 16 日) の新機能および変更された機能</span><span class="sxs-lookup"><span data-stu-id="f089b-103">What's new or changed in Dynamics 365 Talent (April 16, 2019)</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="f089b-104">このトピックでは、Dynamics 365 Talent の新機能または変更された機能について説明します。</span><span class="sxs-lookup"><span data-stu-id="f089b-104">This topic describes features that are either new or changed in Dynamics 365 Talent.</span></span>

## <a name="changes-in-attract"></a><span data-ttu-id="f089b-105">Attract の変更</span><span class="sxs-lookup"><span data-stu-id="f089b-105">Changes in Attract</span></span>

### <a name="process-auditing"></a><span data-ttu-id="f089b-106">プロセスの監査</span><span class="sxs-lookup"><span data-stu-id="f089b-106">Process auditing</span></span>

<span data-ttu-id="f089b-107">求人、職務申請、およびジョブ アプリケーションに加えられた変更を追跡できるようになりました。</span><span class="sxs-lookup"><span data-stu-id="f089b-107">You can now track the changes made to candidates, job openings, and job applications.</span></span> <span data-ttu-id="f089b-108">詳細については、[採用データの変更の追跡](process-auditing.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="f089b-108">For more information, see [Track changes in recruiting data](process-auditing.md).</span></span>

## <a name="changes-in-onboard"></a><span data-ttu-id="f089b-109">Onboard の変更</span><span class="sxs-lookup"><span data-stu-id="f089b-109">Changes in Onboard</span></span>

<span data-ttu-id="f089b-110">今回のリリースには、Dynamics 365 Talent: Onboard のマイナーなバグ修正が含まれています。</span><span class="sxs-lookup"><span data-stu-id="f089b-110">This release includes minor bug fixes for Dynamics 365 Talent: Onboard.</span></span>

## <a name="changes-in-core-hr"></a><span data-ttu-id="f089b-111">Core HR の変更</span><span class="sxs-lookup"><span data-stu-id="f089b-111">Changes in Core HR</span></span>

<span data-ttu-id="f089b-112">このセクションに記載された変更は、ビルド番号 8.1.2239 に適用されます。</span><span class="sxs-lookup"><span data-stu-id="f089b-112">Changes described in this section apply to build number 8.1.2239.</span></span> <span data-ttu-id="f089b-113">かっこ内の数字は、Lifecycle Services (LCS) のサポート番号を参照しています。</span><span class="sxs-lookup"><span data-stu-id="f089b-113">Numbers in parentheses refer to support numbers in Lifecycle Services (LCS).</span></span>

### <a name="compensation-region-compensation-level-benefit-option-and-skill-type-entities-in-common-data-service-updated-to-include-customer-field-support"></a><span data-ttu-id="f089b-114">Common Data Service の報酬地域、報酬レベル、福利厚生オプションおよびスキル タイプのエンティティは、顧客フィールドのサポートを含むように更新されました。</span><span class="sxs-lookup"><span data-stu-id="f089b-114">Compensation region, Compensation level, Benefit option and Skill type entities in Common Data Service updated to include customer field support</span></span>

<span data-ttu-id="f089b-115">このリリースでは、これらの Common Data Service のエンティティが、Talent: Core HR によって追加されたカスタム フィールドを含める機能を持つように更新されました。</span><span class="sxs-lookup"><span data-stu-id="f089b-115">With this release, these Common Data Service entities have been updated to include the ability to include custom field added through Talent: Core HR.</span></span>

### <a name="new-common-data-service-entity-support-for-compensation-vesting-rules-compensation-variable-plan-variable-compensation"></a><span data-ttu-id="f089b-116">新しい Common Data Service エンティティは、報酬給付ルール、変動報酬プラン、変動報酬に対してサポートされます。</span><span class="sxs-lookup"><span data-stu-id="f089b-116">New Common Data Service entity support for: Compensation vesting rules, Compensation variable plan, Variable compensation</span></span>

<span data-ttu-id="f089b-117">このリリースでは、報酬給付ルール、変動報酬プラン、および変動報酬エンティティが Common Data Service に追加されました。</span><span class="sxs-lookup"><span data-stu-id="f089b-117">With this release, Compensation vesting rules, Compensation variable plan, and Variable compensation entities have been added to Common Data Service.</span></span> <span data-ttu-id="f089b-118">これらのエンティティは、Talent: Core HR によって追加されたカスタム フィールドもサポートします。</span><span class="sxs-lookup"><span data-stu-id="f089b-118">These entities also support custom fields added through Talent: Core HR.</span></span>

### <a name="powerbi-refresh-issues-314342"></a><span data-ttu-id="f089b-119">PowerBI の更新に関する問題 (314342)</span><span class="sxs-lookup"><span data-stu-id="f089b-119">PowerBI refresh issues (314342)</span></span>

<span data-ttu-id="f089b-120">この変更により、PowerBI レポートが正常に更新されるよう問題が修正されます。</span><span class="sxs-lookup"><span data-stu-id="f089b-120">This change corrects an issue with PowerBI reports refreshing correctly.</span></span>

### <a name="unable-to-click-directly-through-on-transition-tasks-in-employee-self-service-303309"></a><span data-ttu-id="f089b-121">従業員セルフサービスの移行タスクにおいて直接クリックできない (303309)</span><span class="sxs-lookup"><span data-stu-id="f089b-121">Unable to click directly through on transition tasks in employee self-service (303309)</span></span>

<span data-ttu-id="f089b-122">この変更により、従業員ロールを持つユーザーは、Talent のタスク リストから移行タスクを選択および更新できるようになります。</span><span class="sxs-lookup"><span data-stu-id="f089b-122">This change enables users with the employee role to select and update transition tasks from the Talent to-do list.</span></span>

### <a name="performance-feedback-email-message-updated-309615"></a><span data-ttu-id="f089b-123">パフォーマンス フィードバックのメール メッセージが更新されました (309615)</span><span class="sxs-lookup"><span data-stu-id="f089b-123">Performance feedback email message updated (309615)</span></span>

<span data-ttu-id="f089b-124">この変更により、フィードバックが正常に送信された時に確認メッセージが表示されるようになりました。</span><span class="sxs-lookup"><span data-stu-id="f089b-124">With this change, a confirmation message displays when feedback is successfully submitted.</span></span>

### <a name="missing-tables-in-word-template-308048"></a><span data-ttu-id="f089b-125">Word テンプレート内の見つからないテーブル (308048)</span><span class="sxs-lookup"><span data-stu-id="f089b-125">Missing tables in Word template (308048)</span></span>

<span data-ttu-id="f089b-126">この変更により、従業員およびスキル情報を含む Word テンプレートを作成する時、選択された従業員のスキルのみが Word ドキュメントに表示されます。</span><span class="sxs-lookup"><span data-stu-id="f089b-126">With this change, when creating a Word template with employee and skill information, only the skills for the selected employee appear in the Word document.</span></span>

### <a name="when-applying-an-offboarding-checklist-an-error-is-displayed-299877"></a><span data-ttu-id="f089b-127">除籍チェックリストの適用時にエラーが表示されます。</span><span class="sxs-lookup"><span data-stu-id="f089b-127">When applying an offboarding checklist an error is displayed.</span></span> <span data-ttu-id="f089b-128">(299877)</span><span class="sxs-lookup"><span data-stu-id="f089b-128">(299877)</span></span>

<span data-ttu-id="f089b-129">この変更により、作業者フォームから除籍チェックリストを直接適用した場合の問題が修正されます。</span><span class="sxs-lookup"><span data-stu-id="f089b-129">This change corrects an issue when applying an offboarding checklist directly from the worker form.</span></span>

## <a name="in-preview"></a><span data-ttu-id="f089b-130">プレビュー</span><span class="sxs-lookup"><span data-stu-id="f089b-130">In preview</span></span>

### <a name="allow-reason-codes-to-be-specified-on-leave-types"></a><span data-ttu-id="f089b-131">理由コードを休暇タイプに指定できるようにする</span><span class="sxs-lookup"><span data-stu-id="f089b-131">Allow reason codes to be specified on leave types</span></span>

<span data-ttu-id="f089b-132">組織は、休暇申請に関する追加情報が必要な場合があります。</span><span class="sxs-lookup"><span data-stu-id="f089b-132">Organizations might need additional information about time-off requests.</span></span> <span data-ttu-id="f089b-133">休暇タイプに理由コードを指定し、従業員が休暇申請で理由コードを選択できるようになりました。</span><span class="sxs-lookup"><span data-stu-id="f089b-133">You can now specify reason codes for leave types and enable employees to select a reason code on their time-off requests.</span></span>

### <a name="require-reason-codes-for-certain-leave-types-on-time-off-requests"></a><span data-ttu-id="f089b-134">休暇申請で特定の休暇タイプに理由コードが必要</span><span class="sxs-lookup"><span data-stu-id="f089b-134">Require reason codes for certain leave types on time-off requests</span></span>

<span data-ttu-id="f089b-135">従業員が休暇を送信するときに、組織は特定の休暇タイプに理由コードを要求することがあります。</span><span class="sxs-lookup"><span data-stu-id="f089b-135">Organizations might require reason codes for specific leave types when employees submit time off.</span></span> <span data-ttu-id="f089b-136">これは、会社の方針または規制要件が原因である可能性があります。</span><span class="sxs-lookup"><span data-stu-id="f089b-136">This might be due to company policy or regulatory requirements.</span></span> <span data-ttu-id="f089b-137">どの休暇タイプに理由コードが必要かを指定できるようになりました。また、従業員に休暇申請で休暇タイプに理由コードを指定するように要求できます。</span><span class="sxs-lookup"><span data-stu-id="f089b-137">You can now specify which leave types require a reason code, and you can require employees to provide a reason code for the leave type on their time-off requests.</span></span>

### <a name="provide-leave-and-absence-transaction-list-for-hr"></a><span data-ttu-id="f089b-138">HR の休暇および欠勤トランザクション リストを提供します。</span><span class="sxs-lookup"><span data-stu-id="f089b-138">Provide leave and absence transaction list for HR</span></span>

<span data-ttu-id="f089b-139">従業員の休暇を追跡し、どのように計算するかを理解することにより、HR が従業員の質問に答えるのに役立つだけでなく、従業員に正確な休暇の付与ができるようになります。</span><span class="sxs-lookup"><span data-stu-id="f089b-139">Tracking employee time off and understanding how time off is calculated not only helps HR answer employee questions, but also ensures accurate time-off awards for employees.</span></span> <span data-ttu-id="f089b-140">HR は、残高の背後にある理由を確認するための、トランザクション (交付、見越、調整、および要求) の表示が新しくなりました。</span><span class="sxs-lookup"><span data-stu-id="f089b-140">HR now has a new view into the transactions (grants, accruals, adjustments, and requests) to see the reasons behind balances.</span></span>

## <a name="coming-soon"></a><span data-ttu-id="f089b-141">間もなく公開</span><span class="sxs-lookup"><span data-stu-id="f089b-141">Coming soon</span></span>

### <a name="improvements-to-the-user-interface-for-duplicate-employee-check"></a><span data-ttu-id="f089b-142">重複する従業員チェックのためのユーザー インターフェイスの改良</span><span class="sxs-lookup"><span data-stu-id="f089b-142">Improvements to the user interface for duplicate employee check</span></span>

<span data-ttu-id="f089b-143">この変更により、名前のフィールドを入力すると重複が検出され、見つかった重複の数がステータスに表示されるようになります。</span><span class="sxs-lookup"><span data-stu-id="f089b-143">With this change, duplicates are detected as you enter name fields, and a status displays the number of duplicates found.</span></span> <span data-ttu-id="f089b-144">提供されたリンクを選択して新しいページを開き、検出された一致を使用するかどうかを評価できます。</span><span class="sxs-lookup"><span data-stu-id="f089b-144">You can select the provided link to open a new page to evaluate whether to use the detected match.</span></span> <span data-ttu-id="f089b-145">データ入力の中断を回避するために、重複フォームは自動的に開きません。</span><span class="sxs-lookup"><span data-stu-id="f089b-145">To avoid interrupting data entry, the duplicates form doesn't automatically open.</span></span>

### <a name="email-support-for-alerts"></a><span data-ttu-id="f089b-146">アラートの電子メールサポート</span><span class="sxs-lookup"><span data-stu-id="f089b-146">Email support for alerts</span></span>

<span data-ttu-id="f089b-147">Finance and Operations のプラットフォーム更新プログラム 25 では、あるイベントによってトリガーされた時、自動的に連絡先に電子メール通知を送信する警告ルールを作成できます。</span><span class="sxs-lookup"><span data-stu-id="f089b-147">With Platform update 25 for Finance and Operations, users can create alert rules that automatically send email notifications to contacts when triggered by an event.</span></span>


