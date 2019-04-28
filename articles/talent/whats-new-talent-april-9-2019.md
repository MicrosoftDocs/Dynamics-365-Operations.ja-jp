---
title: Dynamics 365 for Talent (2019 年 4 月 9 日) の新機能や変更された機能
description: このトピックでは、Microsoft Dynamics 365 for Talent の新機能または変更された機能について説明します。
author: Darinkramer
manager: AnnBe
ms.date: 04/09/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2019-04-09
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 25ef0d49c2600833aefa84d404e00c0c57cfbf52
ms.sourcegitcommit: 9796d022a8abf5c07abcdee6852ee34f06d2eb57
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/12/2019
ms.locfileid: "989963"
---
# <a name="whats-new-or-changed-in-dynamics-365-for-talent-april-9-2019"></a><span data-ttu-id="e5753-103">Dynamics 365 for Talent (2019 年 4 月 9 日) の新機能や変更された機能</span><span class="sxs-lookup"><span data-stu-id="e5753-103">What's new or changed in Dynamics 365 for Talent (April 9, 2019)</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="e5753-104">このトピックでは、Dynamics 365 for Talent の新機能または変更された機能について説明します。</span><span class="sxs-lookup"><span data-stu-id="e5753-104">This topic describes features that are either new or changed in Dynamics 365 for Talent.</span></span>

## <a name="changes-in-attract"></a><span data-ttu-id="e5753-105">Attract の変更</span><span class="sxs-lookup"><span data-stu-id="e5753-105">Changes in Attract</span></span>

### <a name="lifecycle-services-lcs-integration-with-report-a-problem"></a><span data-ttu-id="e5753-106">「問題の報告」と Lifecycle Services (LCS) の統合</span><span class="sxs-lookup"><span data-stu-id="e5753-106">Lifecycle Services (LCS) integration with 'report a problem'</span></span>
<span data-ttu-id="e5753-107">Attract と Onboard では、問題をレポートする機能を使用してエンドユーザーによって記録された問題は、顧客の LCS プロジェクトでサポートの問題を自動的に作成するようになりました。</span><span class="sxs-lookup"><span data-stu-id="e5753-107">In Attract and Onboard, issues logged by end users using the report a problem feature now automatically create support issues in the customer's LCS project.</span></span> <span data-ttu-id="e5753-108">その後、管理者は問題をトリアージし、必要に応じて Microsoft に送信することができます。</span><span class="sxs-lookup"><span data-stu-id="e5753-108">Admins can then triage the issues and submit them to Microsoft when needed.</span></span> <span data-ttu-id="e5753-109">これは、Core HR がエンド ユーザーのサポートの問題を処理する方法と一致しています。</span><span class="sxs-lookup"><span data-stu-id="e5753-109">This is consistent with how Core HR handles end user support issues.</span></span>

### <a name="relevance-search"></a><span data-ttu-id="e5753-110">関連情報の検索</span><span class="sxs-lookup"><span data-stu-id="e5753-110">Relevance search</span></span>
<span data-ttu-id="e5753-111">人材プールで、特定のスキル、名前、または学歴について候補データベース全体を検索できるようになりました。</span><span class="sxs-lookup"><span data-stu-id="e5753-111">In talent pools, you can now search your entire candidate database for particular skills, names, or educational background.</span></span> <span data-ttu-id="e5753-112">候補者プロファイルの検索したいセクションを指定する必要がなくなりました。</span><span class="sxs-lookup"><span data-stu-id="e5753-112">You no longer need to specify which section of a candidate's profile you want to search through.</span></span> <span data-ttu-id="e5753-113">Attract はプロファイル全体を検索し、すべての一致した項目を強調表示します。</span><span class="sxs-lookup"><span data-stu-id="e5753-113">Attract searches the entire profile and highlights all the matches found.</span></span> <span data-ttu-id="e5753-114">Attract はまた、候補者に利用可能なすべてのドキュメントを検索し、検索結果をインテリジェントにランク付けします。</span><span class="sxs-lookup"><span data-stu-id="e5753-114">Attract also searches all documents that are available for a candidate and intelligently ranks the search results.</span></span> <span data-ttu-id="e5753-115">さらに、検索結果をソース別、または銀メダリストかどうかでフィルター処理することもできます。</span><span class="sxs-lookup"><span data-stu-id="e5753-115">In addition, you can filter the results by source or by whether they are a silver medalist.</span></span> <span data-ttu-id="e5753-116">詳細については、[候補者プロファイルの検索および表示](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/attract-talent-pools#search-and-view-candidate-profiles) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="e5753-116">For more information, see [Search and view candidate profiles](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/attract-talent-pools#search-and-view-candidate-profiles).</span></span>

### <a name="prospect-recommendations"></a><span data-ttu-id="e5753-117">候補者の推奨事項</span><span class="sxs-lookup"><span data-stu-id="e5753-117">Prospect recommendations</span></span>
<span data-ttu-id="e5753-118">Attract は、組織の候補者データベースからインテリジェントな候補者の推奨事項を作成することで、有効にするとすぐ職務の調達に弾みをつけるのに役立ちます。</span><span class="sxs-lookup"><span data-stu-id="e5753-118">Attract can help kickstart sourcing for a job as soon as you activate it by making intelligent candidate recommendations from your organization's candidate database.</span></span> <span data-ttu-id="e5753-119">推奨事項には、関連する候補者を検索する際に特定されたスキルと教育情報が含まれます。</span><span class="sxs-lookup"><span data-stu-id="e5753-119">The recommendations include the skills and education information identified while searching for relevant prospects.</span></span> <span data-ttu-id="e5753-120">職務の採用プロセスで有効にした場合、これらの推奨事項は職務の下の**候補者**タブに表示されます。</span><span class="sxs-lookup"><span data-stu-id="e5753-120">These recommendations appear on the **Prospects** tab under a job, if you enable it during the job's hiring process.</span></span> <span data-ttu-id="e5753-121">詳細については、[候補者の推奨事項](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/intelligent-recommendations#prospect-recommendations)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="e5753-121">For more information, see [Prospect recommendations](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/intelligent-recommendations#prospect-recommendations).</span></span>

### <a name="interviewer-availability-statuses"></a><span data-ttu-id="e5753-122">面接者の使用可能状態</span><span class="sxs-lookup"><span data-stu-id="e5753-122">Interviewer availability statuses</span></span>
<span data-ttu-id="e5753-123">面接スケジューラは面接者が効率よく働くために時間をスケジュールするのに役立つ、**外出中、他の場所からの作業**ステータスを表示するようになります。</span><span class="sxs-lookup"><span data-stu-id="e5753-123">Interview schedulers will soon be able to view **Out of office, working elsewhere** statuses for interviewers, to help schedule times that might work better for interviewers.</span></span>

### <a name="candidate-interview-experience-save-calendar-invites"></a><span data-ttu-id="e5753-124">候補者の面接経験: カレンダーの招待を保存</span><span class="sxs-lookup"><span data-stu-id="e5753-124">Candidate interview experience: Save calendar invites</span></span>
<span data-ttu-id="e5753-125">候補者は、候補者に送信された面接の概要の電子メールに添付されている .ics ファイルを使用して、自分の個人カレンダーに面接イベントをダウンロードして保存できるようになりました。</span><span class="sxs-lookup"><span data-stu-id="e5753-125">Candidates can now download and save their interview events to their personal calendars using an .ics file attached to the interview summary email sent to the candidate.</span></span>

## <a name="changes-in-onboard"></a><span data-ttu-id="e5753-126">Onboard の変更</span><span class="sxs-lookup"><span data-stu-id="e5753-126">Changes in Onboard</span></span>

### <a name="lifecycle-services-lcs-integration-with-report-a-problem"></a><span data-ttu-id="e5753-127">問題の報告と Lifecycle Services (LCS) の統合</span><span class="sxs-lookup"><span data-stu-id="e5753-127">Lifecycle Services (LCS) integration with report a problem</span></span>
<span data-ttu-id="e5753-128">Attract と Onboard では、問題をレポートする機能を使用してエンドユーザーによって記録された問題は、顧客の LCS プロジェクトでサポートの問題を自動的に作成するようになりました。</span><span class="sxs-lookup"><span data-stu-id="e5753-128">In Attract and Onboard, issues logged by end users using the report a problem feature now automatically create support issues in the customer's LCS project.</span></span> <span data-ttu-id="e5753-129">その後、管理者は問題をトリアージし、必要に応じて Microsoft に送信することができます。</span><span class="sxs-lookup"><span data-stu-id="e5753-129">Admins can then triage the issues and submit them to Microsoft when needed.</span></span> <span data-ttu-id="e5753-130">これは、Core HR がエンド ユーザーのサポートの問題を処理する方法と一致しています。</span><span class="sxs-lookup"><span data-stu-id="e5753-130">This is consistent with how Core HR handles end user support issues.</span></span>

## <a name="changes-in-core-hr"></a><span data-ttu-id="e5753-131">Core HR の変更</span><span class="sxs-lookup"><span data-stu-id="e5753-131">Changes in Core HR</span></span>
<span data-ttu-id="e5753-132">このセクションに記載された変更は、ビルド番号 8.1.2225 に適用されます。</span><span class="sxs-lookup"><span data-stu-id="e5753-132">Changes described in this section apply to build number 8.1.2225.</span></span>

### <a name="percent-of-basis-variable-plans-load-incorrect-amount"></a><span data-ttu-id="e5753-133">基準の割合変動プランが誤った金額を読み込む</span><span class="sxs-lookup"><span data-stu-id="e5753-133">Percent of basis variable plans load incorrect amount</span></span>
<span data-ttu-id="e5753-134">今週のリリースでは、基準プランの割合を使用して変動報酬報酬を読み込む際の問題が修正されました。</span><span class="sxs-lookup"><span data-stu-id="e5753-134">This week’s release corrects an issue when loading variable compensation awards using percent of basis plans.</span></span>
 
### <a name="date-picker-on-last-day-worked-doesnt-work-correctly"></a><span data-ttu-id="e5753-135">最終勤務日の日付の選択が正しく動作しません</span><span class="sxs-lookup"><span data-stu-id="e5753-135">Date picker on Last day worked doesn’t work correctly</span></span>
<span data-ttu-id="e5753-136">この変更により、次の問題を修正 : ユーザーが**雇用の終了日**を編集し、カレンダーの管理を使用して日付を選択すると、選択に日付が追加されます。</span><span class="sxs-lookup"><span data-stu-id="e5753-136">This change corrects the issue: When users edit the **Employment end date** and select the date using the calendar control, a day is added to the selection.</span></span>

###  <a name="limit-personnel-action-types-by-the-action-taken"></a><span data-ttu-id="e5753-137">行なわれるアクションによる個人のアクション タイプを制限する</span><span class="sxs-lookup"><span data-stu-id="e5753-137">Limit personnel action types by the action taken</span></span>
<span data-ttu-id="e5753-138">この変更により、特定のアクションを実行するときに表示されるアクション タイプが制限されます。</span><span class="sxs-lookup"><span data-stu-id="e5753-138">This change limits the action types that appear when taking specific actions.</span></span> <span data-ttu-id="e5753-139">たとえば、新しい職位が要求されると、選択するアクションの一覧に新しい職位アクションのみが表示されます。</span><span class="sxs-lookup"><span data-stu-id="e5753-139">For example, when a new position is requested, only the new position actions appear in the list of actions to select.</span></span> <span data-ttu-id="e5753-140">以前は、新規アクションと編集アクションの両方が表示されていました。</span><span class="sxs-lookup"><span data-stu-id="e5753-140">Previously, both new and edit actions appeared.</span></span> 

### <a name="transferring-an-employee-with-compensation-in-a-second-legal-entity"></a><span data-ttu-id="e5753-141">第 2 の法人の従業員の報酬を転送</span><span class="sxs-lookup"><span data-stu-id="e5753-141">Transferring an employee with compensation in a second legal entity</span></span>
<span data-ttu-id="e5753-142">今回のリリースでは、転送が会社間転送である場合、第 2 の法人で補償が終了するようになりました。</span><span class="sxs-lookup"><span data-stu-id="e5753-142">This release allows compensation to be ended in a second legal entity if the transfer is for a cross-company transfer.</span></span>

### <a name="unable-to-select-compensation-for-a-future-employment-during-a-transfer"></a><span data-ttu-id="e5753-143">転送中に雇用の予定の報酬を選択できません</span><span class="sxs-lookup"><span data-stu-id="e5753-143">Unable to select compensation for a future employment during a transfer</span></span>
<span data-ttu-id="e5753-144">従業員を新しい法人に転送するとき、転送プロセス中に新しい法人の報酬を設定できるようになりました。</span><span class="sxs-lookup"><span data-stu-id="e5753-144">When transferring an employee to a new legal entity, you can now set compensation for the new legal entity during the transfer process.</span></span>

### <a name="user-isnt-able-to-assign-compensation-during-position-assignment"></a><span data-ttu-id="e5753-145">ユーザーは職位の割り当て中に報酬を割り当てることができません</span><span class="sxs-lookup"><span data-stu-id="e5753-145">User isn't able to assign compensation during position assignment</span></span>
<span data-ttu-id="e5753-146">新しい職務割り当てを追加すると、固定報酬レコードを設定できるようになりました。</span><span class="sxs-lookup"><span data-stu-id="e5753-146">Adding a new position assignment now allows setting up fixed compensation records.</span></span> 

## <a name="in-preview"></a><span data-ttu-id="e5753-147">プレビュー</span><span class="sxs-lookup"><span data-stu-id="e5753-147">In preview</span></span>

### <a name="allow-reason-codes-to-be-specified-on-leave-types"></a><span data-ttu-id="e5753-148">理由コードを休暇タイプに指定できるようにする</span><span class="sxs-lookup"><span data-stu-id="e5753-148">Allow reason codes to be specified on leave types</span></span>
<span data-ttu-id="e5753-149">組織は、休暇申請に関する追加情報が必要な場合があります。</span><span class="sxs-lookup"><span data-stu-id="e5753-149">Organizations might need additional information about time-off requests.</span></span> <span data-ttu-id="e5753-150">休暇タイプに理由コードを指定し、従業員が休暇申請で理由コードを選択できるようになりました。</span><span class="sxs-lookup"><span data-stu-id="e5753-150">You can now specify reason codes for leave types and enable employees to select a reason code on their time-off requests.</span></span>

### <a name="require-reason-codes-for-certain-leave-types-on-time-off-requests"></a><span data-ttu-id="e5753-151">休暇申請で特定の休暇タイプに理由コードが必要</span><span class="sxs-lookup"><span data-stu-id="e5753-151">Require reason codes for certain leave types on time-off requests</span></span>
<span data-ttu-id="e5753-152">従業員が休暇を送信するときに、組織は特定の休暇タイプに理由コードを要求することがあります。</span><span class="sxs-lookup"><span data-stu-id="e5753-152">Organizations might require reason codes for specific leave types when employees submit time off.</span></span> <span data-ttu-id="e5753-153">これは、会社の方針または規制要件が原因である可能性があります。</span><span class="sxs-lookup"><span data-stu-id="e5753-153">This might be due to company policy or regulatory requirements.</span></span> <span data-ttu-id="e5753-154">どの休暇タイプに理由コードが必要かを指定できるようになりました。また、従業員に休暇申請で休暇タイプに理由コードを指定するように要求できます。</span><span class="sxs-lookup"><span data-stu-id="e5753-154">You can now specify which leave types require a reason code, and you can require employees to provide a reason code for the leave type on their time-off requests.</span></span>

### <a name="provide-leave-and-absence-transaction-list-for-hr"></a><span data-ttu-id="e5753-155">HR の休暇および欠勤トランザクション リストを提供します。</span><span class="sxs-lookup"><span data-stu-id="e5753-155">Provide leave and absence transaction list for HR</span></span>
<span data-ttu-id="e5753-156">従業員の休暇を追跡し、どのように計算するかを理解することにより、HR が従業員の質問に答えるのに役立つだけでなく、従業員に正確な休暇の付与ができるようになります。</span><span class="sxs-lookup"><span data-stu-id="e5753-156">Tracking employee time off and understanding how time off is calculated not only helps HR answer employee questions, but also ensures accurate time off awards for employees.</span></span> <span data-ttu-id="e5753-157">HR は、残高の背後にある理由を確認するための、トランザクション (交付、見越、調整、および要求) の表示が新しくなりました。</span><span class="sxs-lookup"><span data-stu-id="e5753-157">HR now has a new view into the transactions (grants, accruals, adjustments, and requests) to see the reasons behind balances.</span></span> 

## <a name="coming-soon"></a><span data-ttu-id="e5753-158">間もなく公開</span><span class="sxs-lookup"><span data-stu-id="e5753-158">Coming soon</span></span>

### <a name="improvements-to-the-user-interface-for-duplicate-employee-check"></a><span data-ttu-id="e5753-159">重複する従業員チェックのためのユーザー インターフェイスの改良</span><span class="sxs-lookup"><span data-stu-id="e5753-159">Improvements to the user interface for duplicate employee check</span></span>
<span data-ttu-id="e5753-160">この変更により、名前のフィールドを入力すると重複が検出され、見つかった重複の数がステータスに表示されるようになります。</span><span class="sxs-lookup"><span data-stu-id="e5753-160">With this change, duplicates are detected as you enter name fields, and a status displays the number of duplicates found.</span></span> <span data-ttu-id="e5753-161">提供されたリンクを選択して新しいページを開き、検出された一致を使用するかどうかを評価できます。</span><span class="sxs-lookup"><span data-stu-id="e5753-161">You can select the provided link to open a new page to evaluate whether to use the detected match.</span></span> <span data-ttu-id="e5753-162">データ入力の中断を回避するために、重複フォームは自動的に開きません。</span><span class="sxs-lookup"><span data-stu-id="e5753-162">To avoid interrupting data entry, the duplicates form doesn't automatically open.</span></span>

###  <a name="email-support-for-alerts"></a><span data-ttu-id="e5753-163">アラートの電子メールサポート</span><span class="sxs-lookup"><span data-stu-id="e5753-163">Email support for alerts</span></span>
<span data-ttu-id="e5753-164">プラットフォーム更新プログラム 25 を使用すると、あるイベントによってトリガーされたときに、自動的に連絡先に電子メール通知を送信する警告ルールを作成できます。</span><span class="sxs-lookup"><span data-stu-id="e5753-164">With Platform update 25, users can create alert rules that automatically send email notifications to contacts when triggered by an event.</span></span> 
