---
title: Dynamics 365 Talent (2019 年 4 月 2 日) の新機能や変更された機能
description: このトピックでは、Microsoft Dynamics 365 Talent の新機能または変更された機能について説明します。
author: Darinkramer
manager: AnnBe
ms.date: 04/02/2019
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
ms.search.validFrom: 2019-04-02
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 68dc73b7316a3ceb7129c9ea46bc60669ed2be95
ms.sourcegitcommit: 871707a3fd236da693a3d51f401eb0cb9d4bae39
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/06/2019
ms.locfileid: "2896937"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-april-2-2019"></a><span data-ttu-id="885fd-103">Dynamics 365 Talent (2019 年 4 月 2 日) の新機能や変更された機能</span><span class="sxs-lookup"><span data-stu-id="885fd-103">What's new or changed in Dynamics 365 Talent (April 2, 2019)</span></span>

<span data-ttu-id="885fd-104">このトピックでは、Dynamics 365 Talent の新機能または変更された機能について説明します。</span><span class="sxs-lookup"><span data-stu-id="885fd-104">This topic describes features that are either new or changed in Dynamics 365 Talent.</span></span>

## <a name="changes-in-attract"></a><span data-ttu-id="885fd-105">Attract の変更</span><span class="sxs-lookup"><span data-stu-id="885fd-105">Changes in Attract</span></span>

### <a name="approval-emails-in-attract"></a><span data-ttu-id="885fd-106">Attract の電子メールの承認</span><span class="sxs-lookup"><span data-stu-id="885fd-106">Approval emails in Attract</span></span>
<span data-ttu-id="885fd-107">新しく承認された電子メールでは承認プロセスへの可視性が向上します。</span><span class="sxs-lookup"><span data-stu-id="885fd-107">New approval emails improve visibility into the approval process.</span></span> <span data-ttu-id="885fd-108">電子メールは、次のシナリオのいずれかが発生したときに、承認者に送信されます。</span><span class="sxs-lookup"><span data-stu-id="885fd-108">Emails are sent to approvers when one of the following scenarios occur:</span></span>

- <span data-ttu-id="885fd-109">要求元は、承認のためのジョブを送信します。</span><span class="sxs-lookup"><span data-stu-id="885fd-109">A requestor submits a job for approval.</span></span>
- <span data-ttu-id="885fd-110">ジョブが拒否または承認されます。</span><span class="sxs-lookup"><span data-stu-id="885fd-110">A job is either rejected or approved.</span></span>
- <span data-ttu-id="885fd-111">承認元が 24 時間内に承認の要求を行なっていません。</span><span class="sxs-lookup"><span data-stu-id="885fd-111">An approver hasn't acted on an approval request within 24 hours.</span></span>

<span data-ttu-id="885fd-112">新しいテンプレートを使用して承認電子メールのコンテンツをカスタマイズできます。</span><span class="sxs-lookup"><span data-stu-id="885fd-112">You can customize the content of approval emails with new templates.</span></span>

### <a name="application-and-profile-attachments"></a><span data-ttu-id="885fd-113">アプリケーションとプロファイルの添付ファイル</span><span class="sxs-lookup"><span data-stu-id="885fd-113">Application and profile attachments</span></span>
<span data-ttu-id="885fd-114">アプリケーションと人材プールプロファイルの**ドキュメント**タブの改良により、ドキュメント名とタイプの両方が表示されるようになりました。</span><span class="sxs-lookup"><span data-stu-id="885fd-114">Improvements to the **Documents** tab on applications and talent pool profiles now display both the document name and the type.</span></span>

## <a name="changes-in-onboard"></a><span data-ttu-id="885fd-115">Onboard の変更</span><span class="sxs-lookup"><span data-stu-id="885fd-115">Changes in Onboard</span></span>
<span data-ttu-id="885fd-116">今回のリリースには、Dynamics 365 Talent: Onboard のマイナーなバグ修正が含まれています。</span><span class="sxs-lookup"><span data-stu-id="885fd-116">This release includes minor bug fixes for Dynamics 365 Talent: Onboard.</span></span>

## <a name="coming-soon-attract-and-onboard"></a><span data-ttu-id="885fd-117">間もなく公開 (Attract および Onboard)</span><span class="sxs-lookup"><span data-stu-id="885fd-117">Coming soon (Attract and Onboard)</span></span>

### <a name="lifecycle-services-lcs-integration-with-report-a-problem"></a><span data-ttu-id="885fd-118">問題の報告と Lifecycle Services (LCS) の統合</span><span class="sxs-lookup"><span data-stu-id="885fd-118">Lifecycle Services (LCS) integration with report a problem</span></span>
<span data-ttu-id="885fd-119">Attract と Onboard では、問題をレポートする機能を使用してエンドユーザーによって記録された問題は、顧客の LCS プロジェクトでサポートの問題を自動的に作成するようになりました。</span><span class="sxs-lookup"><span data-stu-id="885fd-119">In Attract and Onboard, problems logged by end users through the report a problem feature now automatically create support issues in the customer's LCS project.</span></span> <span data-ttu-id="885fd-120">その後、管理者は問題をトリアージし、必要に応じて Microsoft に送信することができます。</span><span class="sxs-lookup"><span data-stu-id="885fd-120">Admins can then triage the issues and submit them to Microsoft when needed.</span></span> <span data-ttu-id="885fd-121">これは、Core HR がエンド ユーザーのサポートの問題を処理する方法と一致しています。</span><span class="sxs-lookup"><span data-stu-id="885fd-121">This is consistent with how Core HR handles end user support issues.</span></span>

## <a name="changes-in-core-hr"></a><span data-ttu-id="885fd-122">Core HR の変更</span><span class="sxs-lookup"><span data-stu-id="885fd-122">Changes in Core HR</span></span>
<span data-ttu-id="885fd-123">このセクションに記載された変更は、ビルド番号 8.1.2216 に適用されます。</span><span class="sxs-lookup"><span data-stu-id="885fd-123">Changes described in this section apply to build number 8.1.2216.</span></span>

### <a name="platform-update-25-for-finance-and-operations"></a><span data-ttu-id="885fd-124">Finance and Operations のプラットフォーム更新プログラム 25</span><span class="sxs-lookup"><span data-stu-id="885fd-124">Platform update 25 for Finance and Operations</span></span>
<span data-ttu-id="885fd-125">Finance and Operations のプラットフォーム更新プロフラム 25 の詳細については、[Dynamics 365 for Finance and Operations プラットフォーム更新プロフラム 25 (2019 年 4 月) のプレビュー機能](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/get-started/whats-new-platform-25) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="885fd-125">For more information about Platform update 25 for Finance and Operations, see [Preview features in Dynamics 365 for Finance and Operations platform update 25 (April 2019)](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/get-started/whats-new-platform-25).</span></span>

###  <a name="advanced-compensation-security-fixed-and-variable"></a><span data-ttu-id="885fd-126">高度な報酬セキュリティ (固定および変動)</span><span class="sxs-lookup"><span data-stu-id="885fd-126">Advanced compensation security (fixed and variable)</span></span>
<span data-ttu-id="885fd-127">多くの組織では、報酬および福利厚生の管理者は特定の報酬レコードにのみアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="885fd-127">In many organizations, compensation and benefits managers might only have access to certain compensation records.</span></span> <span data-ttu-id="885fd-128">これには、経営幹部または地域の従業員向けのレコードが含まれます。</span><span class="sxs-lookup"><span data-stu-id="885fd-128">These might include records for executives or regional employees.</span></span> <span data-ttu-id="885fd-129">この変更により、HR は組織内のさまざまな従業員グループの報酬プランを管理および維持できます。</span><span class="sxs-lookup"><span data-stu-id="885fd-129">This change allows HR to manage and maintain compensation plans for different employee groups in the organization.</span></span> <span data-ttu-id="885fd-130">セキュリティ ロールを固定および変動プランに割り当てることができます。</span><span class="sxs-lookup"><span data-stu-id="885fd-130">You can assign security roles to fixed and variable plans.</span></span> <span data-ttu-id="885fd-131">これらのセキュリティ ロールによって、給与または特別償却レコードなどのプランおよび関連する従業員データへのアクセスが決定されるため、それらのロールだけが従業員グループの報酬を処理できます。</span><span class="sxs-lookup"><span data-stu-id="885fd-131">These security roles determine access to plans and related employee data, such as salary or bonus records, so that only those roles can process compensation for the employee groups.</span></span>

### <a name="upgrade-to-common-data-service"></a><span data-ttu-id="885fd-132">Common Data Service へのアップグレード</span><span class="sxs-lookup"><span data-stu-id="885fd-132">Upgrade to Common Data Service</span></span>
<span data-ttu-id="885fd-133">Common Data Service へのアップグレードの期限に近づいています。</span><span class="sxs-lookup"><span data-stu-id="885fd-133">Deadlines to upgrade to Common Data Service are rapidly approaching.</span></span> <span data-ttu-id="885fd-134">データベースをアップグレードする必要があるかどうかを決定するために、Microsoft Power Apps 管理者センターにサインインします。</span><span class="sxs-lookup"><span data-stu-id="885fd-134">Sign in to the Microsoft Power Apps Admin center to determine if your database needs to be upgraded.</span></span> <span data-ttu-id="885fd-135">期限およびアップグレードに必要な手順の詳細については、[Common Data Service へのアップグレード](https://docs.microsoft.com/common-data-service/upgradecds/introduction-upgrade-cds) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="885fd-135">For more information about deadlines and necessary steps to upgrade, see [Upgrade to Common Data Service](https://docs.microsoft.com/common-data-service/upgradecds/introduction-upgrade-cds).</span></span>

## <a name="in-preview"></a><span data-ttu-id="885fd-136">プレビュー</span><span class="sxs-lookup"><span data-stu-id="885fd-136">In preview</span></span>

### <a name="allow-reason-codes-to-be-specified-on-leave-types"></a><span data-ttu-id="885fd-137">理由コードを休暇タイプに指定できるようにする</span><span class="sxs-lookup"><span data-stu-id="885fd-137">Allow reason codes to be specified on leave types</span></span>
<span data-ttu-id="885fd-138">組織は、休暇申請に関する追加情報が必要な場合があります。</span><span class="sxs-lookup"><span data-stu-id="885fd-138">Organizations might need additional information about time-off requests.</span></span> <span data-ttu-id="885fd-139">休暇タイプに理由コードを指定し、従業員が休暇申請で理由コードを選択できるようになりました。</span><span class="sxs-lookup"><span data-stu-id="885fd-139">You can now specify reason codes for leave types and enable employees to select a reason code on their time-off requests.</span></span>

### <a name="require-reason-codes-for-certain-leave-types-on-time-off-requests"></a><span data-ttu-id="885fd-140">休暇申請で特定の休暇タイプに理由コードが必要</span><span class="sxs-lookup"><span data-stu-id="885fd-140">Require reason codes for certain leave types on time-off requests</span></span>
<span data-ttu-id="885fd-141">従業員が休暇を送信するときに、組織は特定の休暇タイプに理由コードを要求することがあります。</span><span class="sxs-lookup"><span data-stu-id="885fd-141">Organizations might require reason codes for specific leave types when employees submit time-off.</span></span> <span data-ttu-id="885fd-142">これは、会社の方針または規制要件が原因である可能性があります。</span><span class="sxs-lookup"><span data-stu-id="885fd-142">This might be due to company policy or regulatory requirements.</span></span> <span data-ttu-id="885fd-143">どの休暇タイプに理由コードが必要かを指定できるようになりました。また、従業員に休暇申請で休暇タイプに理由コードを指定するように要求できます。</span><span class="sxs-lookup"><span data-stu-id="885fd-143">You can now specify which leave types require a reason code, and you can require employees to provide a reason code for the leave type on their time-off requests.</span></span>

## <a name="coming-soon"></a><span data-ttu-id="885fd-144">間もなく公開</span><span class="sxs-lookup"><span data-stu-id="885fd-144">Coming soon</span></span>

### <a name="improvements-to-the-user-interface-for-duplicate-employee-check"></a><span data-ttu-id="885fd-145">重複する従業員チェックのためのユーザー インターフェイスの改良</span><span class="sxs-lookup"><span data-stu-id="885fd-145">Improvements to the user interface for duplicate employee check</span></span>
<span data-ttu-id="885fd-146">この変更により、名前のフィールドを入力すると重複が検出され、見つかった重複の数がステータスに表示されるようになります。</span><span class="sxs-lookup"><span data-stu-id="885fd-146">With this change, duplicates are detected as you enter name fields, and a status displays the number of duplicates found.</span></span> <span data-ttu-id="885fd-147">提供されたリンクを選択して新しいページを開き、検出された一致を使用するかどうかを評価できます。</span><span class="sxs-lookup"><span data-stu-id="885fd-147">You can select the provided link to open a new page to evaluate whether to use the detected match.</span></span> <span data-ttu-id="885fd-148">データ入力の中断を回避するために、重複フォームは自動的に開きません。</span><span class="sxs-lookup"><span data-stu-id="885fd-148">To avoid interrupting data entry, the duplicates form doesn't automatically open.</span></span>

###  <a name="email-support-for-alerts"></a><span data-ttu-id="885fd-149">アラートの電子メールサポート</span><span class="sxs-lookup"><span data-stu-id="885fd-149">Email support for alerts</span></span>
<span data-ttu-id="885fd-150">Finance and Operations のプラットフォーム更新プログラム 25 では、あるイベントによってトリガーされた時、自動的に連絡先に電子メール通知を送信する警告ルールを作成できます。</span><span class="sxs-lookup"><span data-stu-id="885fd-150">With Platform update 25 for Finance and Operations, users can create alert rules that automatically send email notifications to contacts when triggered by an event.</span></span> 
