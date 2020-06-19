---
title: Dynamics 365 Human Resources の新機能または変更された機能 (2020 年 5 月 28 日)
description: このトピックでは、Microsoft Dynamics 365 Human Resources の新機能または変更された機能について説明します。
author: Darinkramer
manager: AnnBe
ms.date: 05/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2020-05-28
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: c386025843edef83d229a42d3f2314678fadae20
ms.sourcegitcommit: beddfba095c23b3265f0004f5124c4e9dc6404cc
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/29/2020
ms.locfileid: "3411933"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-may-28-2020"></a><span data-ttu-id="a7243-103">Dynamics 365 Human Resources の新機能または変更された機能 (2020 年 5 月 28 日)</span><span class="sxs-lookup"><span data-stu-id="a7243-103">What's new or changed in Dynamics 365 Human Resources (May 28, 2020)</span></span>

<span data-ttu-id="a7243-104">このトピックでは、Dynamics 365 Human Resources の新機能または変更された機能について説明します。</span><span class="sxs-lookup"><span data-stu-id="a7243-104">This topic describes features that are either new or changed in Dynamics 365 Human Resources.</span></span> <span data-ttu-id="a7243-105">変更は、ビルド番号 8.1.3287 に適用されます。</span><span class="sxs-lookup"><span data-stu-id="a7243-105">Changes apply to build number 8.1.3287.</span></span> <span data-ttu-id="a7243-106">ヘッダーにあるかっこ内の数字は、参照用の LCS のサポート番号を参照していることがあります。</span><span class="sxs-lookup"><span data-stu-id="a7243-106">The numbers in parentheses in some headings refer to LCS support numbers for reference.</span></span>

## <a name="leaverequest-entity-doesnt-work-when-you-enable-multiple-types-per-leave-plan-447498"></a><span data-ttu-id="a7243-107">休暇プラン (447498) ごとに複数のタイプを有効にすると、LeaveRequest エンティティは機能しません</span><span class="sxs-lookup"><span data-stu-id="a7243-107">LeaveRequest entity doesn't work when you enable multiple types per leave plan (447498)</span></span>

<span data-ttu-id="a7243-108">この変更により、**LeaveEnrollmentV2Entity** で複数の休暇タイプを有効にしたときに発生するエラーを修正できるようになりました。</span><span class="sxs-lookup"><span data-stu-id="a7243-108">With this change, the **LeaveEnrollmentV2Entity** is now available to correct the error that occurs when you enable multiple leave types.</span></span>

## <a name="batch-contention-reduction-feature-preview-446619"></a><span data-ttu-id="a7243-109">バッチの競合軽減機能 (プレビュー) (446619)</span><span class="sxs-lookup"><span data-stu-id="a7243-109">Batch contention reduction feature (preview) (446619)</span></span>

<span data-ttu-id="a7243-110">この機能を有効にすると、タスクの選択とジョブの完了時のバッチ フレームワーク テーブルでブロックの減少が期待できます。</span><span class="sxs-lookup"><span data-stu-id="a7243-110">When you enable this feature, you can expect a reduction in blocking on batch framework tables while selecting tasks and finishing jobs.</span></span>

## <a name="updateconflict-while-saving-worker-prevents-editing-a-record-in-people-427915"></a><span data-ttu-id="a7243-111">UpdateConflict で作業者の保存中に、People でレコードの編集ができない (427915)</span><span class="sxs-lookup"><span data-stu-id="a7243-111">UpdateConflict while saving worker prevents editing a record in People (427915)</span></span>

<span data-ttu-id="a7243-112">この変更により、新しい作業者を追加したり、住所情報を更新したり、言語設定を変更したりするときのエラーが修正されます。</span><span class="sxs-lookup"><span data-stu-id="a7243-112">This change corrects an error when adding a new worker, updating address information, and changing language preference.</span></span> <span data-ttu-id="a7243-113">この固有のシナリオでは、レコードを更新できなかったことを示すエラーが表示されます。</span><span class="sxs-lookup"><span data-stu-id="a7243-113">In this unique scenario, an error displayed indicating the record couldn't be updated.</span></span> 

## <a name="unable-to-add-an-attachment-to-an-approved-leave-request-to-resubmit-425407"></a><span data-ttu-id="a7243-114">承認済の休暇申請に添付ファイルを追加して再提出できない (425407)</span><span class="sxs-lookup"><span data-stu-id="a7243-114">Unable to add an attachment to an approved leave request to resubmit (425407)</span></span>

<span data-ttu-id="a7243-115">この変更により、承認済の休暇申請への添付ファイルが可能になりました。</span><span class="sxs-lookup"><span data-stu-id="a7243-115">This change now allows attachments to approved leave requests.</span></span>

## <a name="user-can-enter-compensation-for-an-employee-in-a-different-legal-entity-form-409529"></a><span data-ttu-id="a7243-116">ユーザーは別の法人のフォームで従業員の報酬を入力できる (409529)</span><span class="sxs-lookup"><span data-stu-id="a7243-116">User can enter compensation for an employee in a different legal entity form (409529)</span></span>

<span data-ttu-id="a7243-117">この変更により、誤った法人の報酬レコードが誤って入力されないように報酬オプションが無効になります。</span><span class="sxs-lookup"><span data-stu-id="a7243-117">This change disables compensation options to prevent inadvertent entry of compensation records for the wrong legal entity.</span></span>

## <a name="error-when-you-transfer-an-employee-and-the-worker-position-assignment-date-is-before-the-position-duration-429402"></a><span data-ttu-id="a7243-118">従業員を異動する際に、作業者の職位の割り当て日が職位の期間よりも前である場合のエラー (429402)</span><span class="sxs-lookup"><span data-stu-id="a7243-118">Error when you transfer an employee and the Worker position assignment date is before the position duration (429402)</span></span>

<span data-ttu-id="a7243-119">このシナリオで従業員を異動する際のエラー メッセージは、この問題を修正するために必要な変更をより的確に説明するために更新されています。</span><span class="sxs-lookup"><span data-stu-id="a7243-119">Error messages when transferring an employee in this scenario have been updated to better describe the changes needed to correct the problem.</span></span>

## <a name="attachments-capabilities-in-employee-self-service-benefits-enrollment"></a><span data-ttu-id="a7243-120">従業員セルフサービス福利厚生の添付ファイル機能</span><span class="sxs-lookup"><span data-stu-id="a7243-120">Attachments capabilities in Employee self service benefits enrollment</span></span>
 
<span data-ttu-id="a7243-121">これで、従業員が登録している各プランの福利厚生登録プロセス中に、添付ファイルを追加できます。</span><span class="sxs-lookup"><span data-stu-id="a7243-121">Now you can add attachments during the benefits enrollment process for each plan that the employee's enrolling in.</span></span> <span data-ttu-id="a7243-122">**作業者登録福利厚生** フォーム内で添付ファイルを表示できます。</span><span class="sxs-lookup"><span data-stu-id="a7243-122">You can then view the attachments within the **Worker enrolled benefit** form.</span></span>

## <a name="in-preview"></a><span data-ttu-id="a7243-123">プレビュー</span><span class="sxs-lookup"><span data-stu-id="a7243-123">In preview</span></span>

## <a name="human-resources-application-in-teams"></a><span data-ttu-id="a7243-124">Teams の Human Resources アプリケーション</span><span class="sxs-lookup"><span data-stu-id="a7243-124">Human Resources application in Teams</span></span>

<span data-ttu-id="a7243-125">従業員は、Microsoft Teams 内で休暇の表示および申請ができます。</span><span class="sxs-lookup"><span data-stu-id="a7243-125">Employees can view and request time away from work within Microsoft Teams.</span></span> <span data-ttu-id="a7243-126">ボットと対話して、休暇申請を作成できます。</span><span class="sxs-lookup"><span data-stu-id="a7243-126">They can interact with a bot to create leave requests.</span></span> <span data-ttu-id="a7243-127">詳細については、[Teams の Human Resources アプリ](https://go.microsoft.com/fwlink/?linkid=2127841) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="a7243-127">For more information, see [Human Resources app in Teams](https://go.microsoft.com/fwlink/?linkid=2127841).</span></span> 

## <a name="leave-suspension"></a><span data-ttu-id="a7243-128">休暇の停止</span><span class="sxs-lookup"><span data-stu-id="a7243-128">Leave suspension</span></span>

<span data-ttu-id="a7243-129">従業員に対し Human Resources で休暇および欠勤を中断できます。</span><span class="sxs-lookup"><span data-stu-id="a7243-129">You can suspend leave and absence in Human Resources for an employee.</span></span> <span data-ttu-id="a7243-130">休暇を中断すると、選択した休暇タイプの休暇の発生が停止します。</span><span class="sxs-lookup"><span data-stu-id="a7243-130">Suspending leave stops the leave accruals for selected leave types.</span></span> <span data-ttu-id="a7243-131">一時停止が見越計上プロセス後に発生した場合、休暇の一時停止により、従業員の休暇残日数が比例配分調整されます。</span><span class="sxs-lookup"><span data-stu-id="a7243-131">If the suspension occurs after an accrual has been processed, suspending leave creates a prorated adjustment to the employee's leave balance.</span></span> <span data-ttu-id="a7243-132">詳細については、[休暇の中断](hr-leave-and-absence-suspend-leave.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="a7243-132">For more information, see [Suspend leave](hr-leave-and-absence-suspend-leave.md).</span></span>

## <a name="update-user-experience-to-indicate-that-accrual-is-suspended-429550"></a><span data-ttu-id="a7243-133">ユーザー エクスペリエンスを更新し、見越計上の中断が表示されるようになりました (429550)</span><span class="sxs-lookup"><span data-stu-id="a7243-133">Update user experience to indicate that accrual is suspended (429550)</span></span>

<span data-ttu-id="a7243-134">ユーザー エクスペリエンスは、計画に対して見越計上が中断されたことを示します。</span><span class="sxs-lookup"><span data-stu-id="a7243-134">The user experience now indicates that the accrual has been suspended for a plan.</span></span>

## <a name="coming-soon"></a><span data-ttu-id="a7243-135">間もなく公開</span><span class="sxs-lookup"><span data-stu-id="a7243-135">Coming soon</span></span>

## <a name="database-logging-in-preview-in-june"></a><span data-ttu-id="a7243-136">データベース ログ (6 月のプレビュー)</span><span class="sxs-lookup"><span data-stu-id="a7243-136">Database logging (in preview in June)</span></span>

<span data-ttu-id="a7243-137">データベース ログ機能を使用すると、監視するテーブルとフィールドを決定できます。</span><span class="sxs-lookup"><span data-stu-id="a7243-137">The database logging feature allows you to determine which table and fields should be monitored.</span></span> <span data-ttu-id="a7243-138">また、変更追跡を起動するイベントを決定することもできます。</span><span class="sxs-lookup"><span data-stu-id="a7243-138">It also lets you determine the events that should trigger change tracking.</span></span> <span data-ttu-id="a7243-139">時間の経過に伴う変更を確認するために、照会機能を使用できます。</span><span class="sxs-lookup"><span data-stu-id="a7243-139">Inquiry capabilities are available to see these changes over time.</span></span>

## <a name="buy-and-sell-leave-in-preview-june-1"></a><span data-ttu-id="a7243-140">休暇の売買 (6 月 1 日のプレビュー)</span><span class="sxs-lookup"><span data-stu-id="a7243-140">Buy and sell leave (in preview June 1)</span></span>

<span data-ttu-id="a7243-141">一部の組織では、従業員が休暇を購入または売却できるという利点があります。</span><span class="sxs-lookup"><span data-stu-id="a7243-141">Some organizations provide a benefit that allows employees to buy or sell their leave.</span></span> <span data-ttu-id="a7243-142">このプロセスは、多くの場合、手動で管理します。</span><span class="sxs-lookup"><span data-stu-id="a7243-142">This process is often managed manually.</span></span> <span data-ttu-id="a7243-143">この機能により、人事部門のポリシーと申請をより自動化された方法で管理できるようになり、休暇管理プロセスを合理化しながらミスを排除するのに役立ちます。</span><span class="sxs-lookup"><span data-stu-id="a7243-143">This feature provides a more automated way to manage policies and requests for the HR department, and it helps eliminate mistakes while streamlining the leave management process.</span></span>

## <a name="data-management-framework-dmf-entities-for-benefits-management"></a><span data-ttu-id="a7243-144">福利厚生管理のためのデータ管理フレームワーク (DMF) エンティティ</span><span class="sxs-lookup"><span data-stu-id="a7243-144">Data management framework (DMF) entities for Benefits management</span></span>
 
<span data-ttu-id="a7243-145">福利厚生管理エンティティはリリースされてます。</span><span class="sxs-lookup"><span data-stu-id="a7243-145">Benefits management entities are releasing.</span></span> <span data-ttu-id="a7243-146">DMF エンティティを使用すると、データをインポートおよびエクスポートして、福利厚生管理を簡単にコンフィギュレーションできます。</span><span class="sxs-lookup"><span data-stu-id="a7243-146">DMF entities allow importing and exporting data to easily configure benefits management.</span></span> <span data-ttu-id="a7243-147">福利厚生管理テンプレートは、データの移動にも使用できます。</span><span class="sxs-lookup"><span data-stu-id="a7243-147">A Benefits management template will also be available to move data.</span></span> <span data-ttu-id="a7243-148">テンプレートは、データの依存関係を考慮してデータを順次エクスポートおよびインポートします。</span><span class="sxs-lookup"><span data-stu-id="a7243-148">The template exports and imports the data in a sequential manner to respect data dependencies.</span></span>

## <a name="add-reason-code-to-accrual-suspensions-june-1"></a><span data-ttu-id="a7243-149">休暇付与の一時停止に理由コードが追加されました (6 月 1 日)</span><span class="sxs-lookup"><span data-stu-id="a7243-149">Add reason code to accrual suspensions (June 1)</span></span>

<span data-ttu-id="a7243-150">見越計上の中断に理由コードが追加されました。</span><span class="sxs-lookup"><span data-stu-id="a7243-150">Reason codes have been added to the accrual suspension.</span></span>

## <a name="carry-forward-rules-june-1"></a><span data-ttu-id="a7243-151">繰越ルール (6 月 1 日)</span><span class="sxs-lookup"><span data-stu-id="a7243-151">Carry forward rules (June 1)</span></span>

<span data-ttu-id="a7243-152">繰越調整を転送する繰越残日数に対して、繰越休暇タイプを指定できます。</span><span class="sxs-lookup"><span data-stu-id="a7243-152">You can specify a carry forward leave type for carry forward balances where carry forward adjustments are transferred.</span></span> <span data-ttu-id="a7243-153">たとえば、従業員が 10 日間繰り越す場合、その 10 日間に別の休暇タイプを選択できます。</span><span class="sxs-lookup"><span data-stu-id="a7243-153">For example, if an employee carries forward 10 days, you can pick a different leave type for those 10 days.</span></span> <span data-ttu-id="a7243-154">詳細については、[休暇および欠勤タイプのコンフィギュレーション](hr-leave-and-absence-types.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="a7243-154">For more information, see [Configure leave and absence types](hr-leave-and-absence-types.md).</span></span>

## <a name="suspend-leave-accrual-for-specified-leave-types-june-1"></a><span data-ttu-id="a7243-155">指定した休暇タイプに対する休暇付与の一時停止 (6 月 1 日)</span><span class="sxs-lookup"><span data-stu-id="a7243-155">Suspend leave accrual for specified leave types (June 1)</span></span>

<span data-ttu-id="a7243-156">今回のリリースでは、人事部は無給休暇の休暇申請を入力した従業員に対して、休暇の発生を停止するルールを作成することができます。</span><span class="sxs-lookup"><span data-stu-id="a7243-156">In this release, HR can create a rule to suspend leave accruals for employees with leave requests entered for unpaid leave.</span></span> <span data-ttu-id="a7243-157">無給休暇のタイプを指定できますが、必須ではあります。</span><span class="sxs-lookup"><span data-stu-id="a7243-157">Unpaid leave can be a type, but doesn't have to be.</span></span> <span data-ttu-id="a7243-158">他の休暇種類に基づいて、任意の休暇を停止することができます。</span><span class="sxs-lookup"><span data-stu-id="a7243-158">You can suspend any leave based on another leave type.</span></span>

## <a name="dmf-entity-available-for-accrual-suspensions-june-1"></a><span data-ttu-id="a7243-159">DMF エンティティで休暇付与の一時停止が可能 (6 月 1 日)</span><span class="sxs-lookup"><span data-stu-id="a7243-159">DMF entity available for accrual suspensions (June 1)</span></span>

<span data-ttu-id="a7243-160">DMF エンティティが見越し計上の停止に使用できるようになりました 。</span><span class="sxs-lookup"><span data-stu-id="a7243-160">A DMF entity is now available for accrual suspensions.</span></span>