---
title: Dynamics 365 Human Resources の新機能または変更された機能 (2020 年 7 月 8 日)
description: このトピックでは、2020 年 7 月 8 日に更新された、Microsoft Dynamics 365 Human Resources の新機能、または変更された機能について説明します。
author: andreabichsel
ms.date: 07/08/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: c0762c86842db32127ac1da97a92ec05d434707d
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5794424"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-july-8-2020"></a><span data-ttu-id="0894d-103">Dynamics 365 Human Resources の新機能または変更された機能 (2020 年 7 月 8 日)</span><span class="sxs-lookup"><span data-stu-id="0894d-103">What's new or changed in Dynamics 365 Human Resources (July 8, 2020)</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="0894d-104">このトピックでは、Dynamics 365 Human Resources の新機能または変更された機能について説明します。</span><span class="sxs-lookup"><span data-stu-id="0894d-104">This topic describes features that are either new or changed in Dynamics 365 Human Resources.</span></span> <span data-ttu-id="0894d-105">変更は、ビルド番号 8.1.3382 に適用されます。</span><span class="sxs-lookup"><span data-stu-id="0894d-105">Changes apply to build number 8.1.3382.</span></span> <span data-ttu-id="0894d-106">ヘッダーにあるかっこ内の数字は、参照用の LCS のサポート番号を参照していることがあります。</span><span class="sxs-lookup"><span data-stu-id="0894d-106">The numbers in parentheses in some headings refer to LCS support numbers for reference.</span></span>

## <a name="database-logging"></a><span data-ttu-id="0894d-107">データベースのログ</span><span class="sxs-lookup"><span data-stu-id="0894d-107">Database logging</span></span>

<span data-ttu-id="0894d-108">データベース ログを使用すると、監視するテーブルとフィールドを決定できます。</span><span class="sxs-lookup"><span data-stu-id="0894d-108">Database logging allows you to determine which tables and fields to monitor.</span></span> <span data-ttu-id="0894d-109">また、Change Tracking を起動するイベントを決定することもできます。</span><span class="sxs-lookup"><span data-stu-id="0894d-109">It also lets you determine the events that should trigger change tracking.</span></span> <span data-ttu-id="0894d-110">これらの変更を時間の経過と共に確認するには、データベースのログ機能を使用します。</span><span class="sxs-lookup"><span data-stu-id="0894d-110">You use database logging capabilities to see these changes over time.</span></span> <span data-ttu-id="0894d-111">詳細については、[データベース ログの構成と管理](hr-admin-database-logging.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="0894d-111">For more information, see [Configure and manage database logging](hr-admin-database-logging.md).</span></span>

## <a name="configure-the-name-of-employee-self-service"></a><span data-ttu-id="0894d-112">従業員セルフ サービス名のコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="0894d-112">Configure the name of Employee self service</span></span>

<span data-ttu-id="0894d-113">**人事管理パラメータ** で、**従業員セルフ サービス** ワークスペースの名前を **セルフ サービス** に変更できるようになりました。</span><span class="sxs-lookup"><span data-stu-id="0894d-113">In **Human Resources parameters**, you can now change the name of the **Employee self service** workspace to **Self service**.</span></span> <span data-ttu-id="0894d-114">詳細については、[従業員セルフ サービス ワークスペース名の変更](hr-employee-self-service-workspace-name.md) を参照してください</span><span class="sxs-lookup"><span data-stu-id="0894d-114">For more information, see [Change Employee self service workspace name](hr-employee-self-service-workspace-name.md)</span></span>

## <a name="benefits-management-open-enrollment-access-outside-of-period"></a><span data-ttu-id="0894d-115">期間外の福利厚生管理のオープン登録アクセス</span><span class="sxs-lookup"><span data-stu-id="0894d-115">Benefits management open enrollment access outside of period</span></span>

<span data-ttu-id="0894d-116">このリリースでは、従業員が登録期間外またはライフ イベントなしで福利厚生のオープン登録にアクセスできるバグを修正します。</span><span class="sxs-lookup"><span data-stu-id="0894d-116">This release fixes a bug where employees could access benefits open enrollment outside of the enrollment period or without a life event.</span></span> <span data-ttu-id="0894d-117">そのため、従業員セルフ サービスでオープン登録をデモする必要がある場合は、オープン登録日を今日 (またはそれ以前) に調整して、アクセスできるようにする必要があります。</span><span class="sxs-lookup"><span data-stu-id="0894d-117">As a result, if you need to demo open enrollment in Employee self service, you must adjust the open enrollment dates to today (or earlier) to make it accessible.</span></span> <span data-ttu-id="0894d-118">この設定は、**福利厚生管理 > ルールとオプション期間** で変更できます。</span><span class="sxs-lookup"><span data-stu-id="0894d-118">You can change this setting under **Benefits management > Rules and options periods**.</span></span>

## <a name="email-employee-enrollment-confirmation"></a><span data-ttu-id="0894d-119">従業員の登録確認メール</span><span class="sxs-lookup"><span data-stu-id="0894d-119">Email employee enrollment confirmation</span></span>

<span data-ttu-id="0894d-120">福利厚生の選択が完了した後、従業員に電子メールを送信できるようになりました。</span><span class="sxs-lookup"><span data-stu-id="0894d-120">You can now send emails to employees after they complete their benefits selection.</span></span> <span data-ttu-id="0894d-121">既定のメッセージを送信するか、組織の電子メール テンプレートを使用することができます。</span><span class="sxs-lookup"><span data-stu-id="0894d-121">You can either send a default message or use an organization email template.</span></span> <span data-ttu-id="0894d-122">これらの設定は、**人事管理パラメータ > 福利厚生の管理** にあります。</span><span class="sxs-lookup"><span data-stu-id="0894d-122">These settings are under **Human resource parameters > Benefits management**.</span></span>

## <a name="canceled-leave-still-appears-in-upcoming-time-off-on-people-workspace-441358"></a><span data-ttu-id="0894d-123">人員ワークスペースの今後の休暇にキャンセルされた休暇が引き続き表示される (441358)</span><span class="sxs-lookup"><span data-stu-id="0894d-123">Canceled leave still appears in upcoming time off on People workspace (441358)</span></span>

<span data-ttu-id="0894d-124">キャンセルされた休暇は、**人員** ワークスペースの休暇カードに今後の休暇として表示されなくなりました。</span><span class="sxs-lookup"><span data-stu-id="0894d-124">Canceled leave no longer displays as upcoming time off on the leave cards in the **People** workspace.</span></span>

## <a name="unable-to-use-the-department-entity-property-in-the-positionv2-entity-456486"></a><span data-ttu-id="0894d-125">PositionV2 エンティティで部門エンティティのプロパティを使用できない (456486)</span><span class="sxs-lookup"><span data-stu-id="0894d-125">Unable to use the department entity property in the PositionV2 entity (456486)</span></span>

<span data-ttu-id="0894d-126">重複リレーションを作成せずに部署を追加できるようになりました。</span><span class="sxs-lookup"><span data-stu-id="0894d-126">You can now add a department without creating a duplicate relation.</span></span>

## <a name="payrollworkerenrolledbenefitdetailentity-should-only-use-calculated-field-for-retirement-plans-459779"></a><span data-ttu-id="0894d-127">PayrollWorkerEnrolledBenefitDetailEntity は、退職プランの計算フィールドのみを使用する必要がある (459779)</span><span class="sxs-lookup"><span data-stu-id="0894d-127">PayrollWorkerEnrolledBenefitDetailEntity should only use calculated field for retirement plans (459779)</span></span>

<span data-ttu-id="0894d-128">**PayrollWorkerEnrolledBenefitDetailEntity** エンティティをエクスポートする場合、エクスポートは、レート テーブルに基づく計算フィールドを使用するか、バッキング テーブルで **ContributionAmountCur** フィールドを使用するかを決定します。</span><span class="sxs-lookup"><span data-stu-id="0894d-128">When exporting the **PayrollWorkerEnrolledBenefitDetailEntity** entity, the export determines whether it should use a calculated field based on a rate table or use the **ContributionAmountCur** field on the backing table.</span></span> <span data-ttu-id="0894d-129">データ エンティティがロジックは、アプリケーションが通常使用しない状況で、レート テーブルを使用します。</span><span class="sxs-lookup"><span data-stu-id="0894d-129">The logic used by the data entity uses the rate table in situations where the application normally doesn't.</span></span> <span data-ttu-id="0894d-130">このロジックでは、計算レート テーブルがなく、製品では顧客が指定できないため、エンティティ エクスポートでは、この列の値がゼロになります。</span><span class="sxs-lookup"><span data-stu-id="0894d-130">This logic causes the entity exports to return a zero value for this column, because there's no calculation rate table and the product doesn't allow the customer to specify one.</span></span>
 
## <a name="confusing-translations-in-czech-language-in-personnel-management-and-employee-self-service-400276"></a><span data-ttu-id="0894d-131">人事管理および従業員セルフ サービスにおけるチェコ語での翻訳の混乱 (400276)</span><span class="sxs-lookup"><span data-stu-id="0894d-131">Confusing translations in Czech language in Personnel management and Employee self service (400276)</span></span>

<span data-ttu-id="0894d-132">このリリースでは、**会社のディレクトリ**、**次の登録済コース**、**職務**、および **職位** の翻訳が修正されます。</span><span class="sxs-lookup"><span data-stu-id="0894d-132">This release corrects the translations for **Company directory**, **Next registered course**, **Job**, and **Position**.</span></span>
 
## <a name="the-workcalendaremployment-table-doesnt-have-the-created-and-modified-system-fields-enabled-460171"></a><span data-ttu-id="0894d-133">WorkCalendarEmployment テーブルでは、作成および変更されたシステム フィールドが有効になっていない (460171)</span><span class="sxs-lookup"><span data-stu-id="0894d-133">The WorkCalendarEmployment table doesn't have the created and modified system fields enabled (460171)</span></span>

<span data-ttu-id="0894d-134">作成および変更されたシステム フィールドが、Human Resources の **WorkCalendarEmployment** テーブルで有効になりました。</span><span class="sxs-lookup"><span data-stu-id="0894d-134">Created and modified system fields are now enabled on the **WorkCalendarEmployment** table in Human Resources.</span></span>
 
## <a name="null-reference-exception-for-hire-and-add-details-for-future-employee-455475"></a><span data-ttu-id="0894d-135">将来の従業員の採用および詳細の追加に関する null 参照例外 (455475)</span><span class="sxs-lookup"><span data-stu-id="0894d-135">Null reference exception for Hire and add details for future employee (455475)</span></span>

<span data-ttu-id="0894d-136">このリリースでは、**採用および詳細の追加** オプションを使用して従業員を採用すると、合理化された従業員エントリのエラー (null 参照) が修正されます。</span><span class="sxs-lookup"><span data-stu-id="0894d-136">This release corrects an error (null reference) in streamlined employee entry when you hire an employee using the option to **Hire and add details**.</span></span>

## <a name="changes-made-in-the-dataverse-worker-entity-dont-reflect-in-human-resources-455652"></a><span data-ttu-id="0894d-137">Dataverse 作業者エンティティに加えられた変更が、Human Resources に反映されない (455652)</span><span class="sxs-lookup"><span data-stu-id="0894d-137">Changes made in the Dataverse Worker entity don't reflect in Human Resources (455652)</span></span>

<span data-ttu-id="0894d-138">Dataverse の **作業者** エンティティの次のフィールドに加えられた変更は、Human Resources に表示されます:</span><span class="sxs-lookup"><span data-stu-id="0894d-138">Changes made to the following fields in the **Worker** entity in Dataverse will now show up in Human Resources:</span></span>

- <span data-ttu-id="0894d-139">**自宅での作業**</span><span class="sxs-lookup"><span data-stu-id="0894d-139">**Works from home**</span></span>
- <span data-ttu-id="0894d-140">**勤続日数**</span><span class="sxs-lookup"><span data-stu-id="0894d-140">**Seniority date**</span></span>
- <span data-ttu-id="0894d-141">**記念日**</span><span class="sxs-lookup"><span data-stu-id="0894d-141">**Anniversary date**</span></span>
- <span data-ttu-id="0894d-142">**元の採用日付**</span><span class="sxs-lookup"><span data-stu-id="0894d-142">**Original hire date**</span></span>

## <a name="correct-compensation-level-doesnt-default-based-on-the-job-assigned-to-the-position-394136"></a><span data-ttu-id="0894d-143">職位に割り当てられた職務に基づいて正しい報酬レベルがデフォルト設定されない (394136)</span><span class="sxs-lookup"><span data-stu-id="0894d-143">Correct compensation level doesn't default based on the job assigned to the position (394136)</span></span>

<span data-ttu-id="0894d-144">この変更により、正しい報酬レベルが **職位の詳細** の **有効日** レコードと **報酬プラン割り当て** の **開始日** に基づいてデフォルト設定されます。</span><span class="sxs-lookup"><span data-stu-id="0894d-144">With this change, the correct compensation level defaults based on the **Date effective** records for the **Position details** and the **Start date** of the **Compensation plan assignment**.</span></span>

## <a name="in-preview"></a><span data-ttu-id="0894d-145">プレビュー</span><span class="sxs-lookup"><span data-stu-id="0894d-145">In preview</span></span>

## <a name="mandatory-fields"></a><span data-ttu-id="0894d-146">必須項目</span><span class="sxs-lookup"><span data-stu-id="0894d-146">Mandatory fields</span></span> 

<span data-ttu-id="0894d-147">人事管理のパーソナル化機能を使用することにより、項目を必須にすることができます。</span><span class="sxs-lookup"><span data-stu-id="0894d-147">You can now make fields mandatory by using Human Resources personalization capabilities.</span></span> <span data-ttu-id="0894d-148">この機能には **保存されたビュー** が必要です。</span><span class="sxs-lookup"><span data-stu-id="0894d-148">This feature requires **Saved views**.</span></span>

## <a name="human-resources-application-in-teams"></a><span data-ttu-id="0894d-149">Teams の Human Resources アプリケーション</span><span class="sxs-lookup"><span data-stu-id="0894d-149">Human Resources application in Teams</span></span>

<span data-ttu-id="0894d-150">従業員は、Microsoft Teams 内で休暇の表示および申請ができます。</span><span class="sxs-lookup"><span data-stu-id="0894d-150">Employees can view and request time away from work within Microsoft Teams.</span></span> <span data-ttu-id="0894d-151">ボットと対話して、休暇申請を作成できます。</span><span class="sxs-lookup"><span data-stu-id="0894d-151">They can interact with a bot to create leave requests.</span></span> <span data-ttu-id="0894d-152">詳細については、[Teams の Human Resources アプリ](https://go.microsoft.com/fwlink/?linkid=2127841) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="0894d-152">For more information, see [Human Resources app in Teams](https://go.microsoft.com/fwlink/?linkid=2127841).</span></span> 

## <a name="data-management-framework-dmf-entities-for-benefits-management"></a><span data-ttu-id="0894d-153">福利厚生管理のためのデータ管理フレームワーク (DMF) エンティティ</span><span class="sxs-lookup"><span data-stu-id="0894d-153">Data management framework (DMF) entities for Benefits management</span></span>
 
<span data-ttu-id="0894d-154">福利厚生管理エンティティはリリースされてます。</span><span class="sxs-lookup"><span data-stu-id="0894d-154">Benefits management entities are releasing.</span></span> <span data-ttu-id="0894d-155">DMF エンティティを使用すると、データをインポートおよびエクスポートして、福利厚生管理を簡単に構成できます。</span><span class="sxs-lookup"><span data-stu-id="0894d-155">DMF entities allow you to import and export data to easily configure benefits management.</span></span> <span data-ttu-id="0894d-156">福利厚生管理テンプレートは、データの移動に使用できます。</span><span class="sxs-lookup"><span data-stu-id="0894d-156">A Benefits management template will be available to move data.</span></span> <span data-ttu-id="0894d-157">テンプレートは、データの依存関係を考慮してデータを順次エクスポートおよびインポートします。</span><span class="sxs-lookup"><span data-stu-id="0894d-157">The template exports and imports the data sequentially to respect data dependencies.</span></span>

## <a name="buy-and-sell-leave"></a><span data-ttu-id="0894d-158">休暇の売買</span><span class="sxs-lookup"><span data-stu-id="0894d-158">Buy and sell leave</span></span> 

<span data-ttu-id="0894d-159">一部の組織では、従業員が休暇を購入または売却できるという利点があります。</span><span class="sxs-lookup"><span data-stu-id="0894d-159">Some organizations provide a benefit that allows employees to buy or sell their leave.</span></span> <span data-ttu-id="0894d-160">このプロセスは、多くの場合、手動で管理します。</span><span class="sxs-lookup"><span data-stu-id="0894d-160">This process is often managed manually.</span></span> <span data-ttu-id="0894d-161">この機能により、人事部門のポリシーと申請の管理を自動化します。</span><span class="sxs-lookup"><span data-stu-id="0894d-161">This feature automates managing policies and requests for the HR department.</span></span> <span data-ttu-id="0894d-162">休暇管理プロセスを合理化し、ミスをなくすことができます。</span><span class="sxs-lookup"><span data-stu-id="0894d-162">It streamlines the leave management process and helps eliminate mistakes.</span></span> <span data-ttu-id="0894d-163">詳細については、以下を参照してください。</span><span class="sxs-lookup"><span data-stu-id="0894d-163">For more information, see:</span></span>

- [<span data-ttu-id="0894d-164">休暇の売買ポリシーの管理</span><span class="sxs-lookup"><span data-stu-id="0894d-164">Manage buy and sell leave policies</span></span>](hr-leave-and-absence-manage-buy-and-sell-leave-policies.md)
- [<span data-ttu-id="0894d-165">休暇の売買</span><span class="sxs-lookup"><span data-stu-id="0894d-165">Buy and sell leave</span></span>](hr-employee-self-service-buy-sell-leave.md)

## <a name="leave-accrual-for-a-single-company-or-single-plan"></a><span data-ttu-id="0894d-166">1 社または 1 プランの有給休暇</span><span class="sxs-lookup"><span data-stu-id="0894d-166">Leave accrual for a single company or single plan</span></span>

<span data-ttu-id="0894d-167">顧客は、1 社または 1 休暇および不就業プランの有給休暇を処理できます。</span><span class="sxs-lookup"><span data-stu-id="0894d-167">Customers can process accruals for a single company or a single leave and absence plan.</span></span> <span data-ttu-id="0894d-168">この機能により、異なる休暇年数または有給休暇ポリシーを持つ顧客のために有給休暇プロセスを明確にします。</span><span class="sxs-lookup"><span data-stu-id="0894d-168">This ability provides clarity for the accrual process for customers with different leave years or leave accrual policies.</span></span> <span data-ttu-id="0894d-169">詳細については、[会社別または休暇プラン別の有給休暇](hr-leave-and-absence-accrue.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="0894d-169">For more information, see [Accrue leave per company or per leave plan](hr-leave-and-absence-accrue.md).</span></span>

## <a name="add-attachments-to-time-off-requests"></a><span data-ttu-id="0894d-170">添付ファイルを休暇申請に追加</span><span class="sxs-lookup"><span data-stu-id="0894d-170">Add attachments to time-off requests</span></span>

<span data-ttu-id="0894d-171">承認済み休暇申請に添付ファイルを追加する機能は、現在の COVID-19 環境では非常に重要です。</span><span class="sxs-lookup"><span data-stu-id="0894d-171">The ability to add attachments to approved leave requests is critical in the current COVID-19 environment.</span></span> <span data-ttu-id="0894d-172">従業員はこれらの添付ファイルを追加できます。</span><span class="sxs-lookup"><span data-stu-id="0894d-172">Employees can now add these attachments.</span></span> <span data-ttu-id="0894d-173">また、休暇申請がどのように更新されるかについても、より深く理解することができます。</span><span class="sxs-lookup"><span data-stu-id="0894d-173">They also have more insight into how updates are made to leave requests.</span></span> <span data-ttu-id="0894d-174">詳細については、[既存の申請に添付ファイルを追加](hr-employee-self-service-request-time-off.md#add-an-attachment-to-an-existing-request) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="0894d-174">For more information, see [Add an attachment to an existing request](hr-employee-self-service-request-time-off.md#add-an-attachment-to-an-existing-request).</span></span>

## <a name="add-reason-code-to-accrual-suspensions"></a><span data-ttu-id="0894d-175">休暇付与の一時停止に理由コードが追加されました</span><span class="sxs-lookup"><span data-stu-id="0894d-175">Add reason code to accrual suspensions</span></span> 

<span data-ttu-id="0894d-176">見越計上の中断に理由コードが追加されました。</span><span class="sxs-lookup"><span data-stu-id="0894d-176">Reason codes have been added to the accrual suspension.</span></span>

## <a name="carry-forward-rules"></a><span data-ttu-id="0894d-177">繰越ルール</span><span class="sxs-lookup"><span data-stu-id="0894d-177">Carry forward rules</span></span> 

<span data-ttu-id="0894d-178">繰越調整を転送する繰越残日数に対して、繰越休暇タイプを指定できます。</span><span class="sxs-lookup"><span data-stu-id="0894d-178">You can specify a carry forward leave type for carry forward balances where carry forward adjustments are transferred.</span></span> <span data-ttu-id="0894d-179">たとえば、従業員が 10 日間繰り越す場合、その 10 日間に別の休暇タイプを選択できます。</span><span class="sxs-lookup"><span data-stu-id="0894d-179">For example, if an employee carries forward 10 days, you can pick a different leave type for those 10 days.</span></span> <span data-ttu-id="0894d-180">詳細については、[休暇および欠勤タイプのコンフィギュレーション](hr-leave-and-absence-types.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="0894d-180">For more information, see [Configure leave and absence types](hr-leave-and-absence-types.md).</span></span>

## <a name="suspend-leave-accrual-for-specified-leave-types"></a><span data-ttu-id="0894d-181">指定した休暇タイプに対する休暇付与の一時停止</span><span class="sxs-lookup"><span data-stu-id="0894d-181">Suspend leave accrual for specified leave types</span></span>

<span data-ttu-id="0894d-182">無給休暇で休暇申請を入力した従業員に対して、休暇の発生を停止するルールを作成することができます。</span><span class="sxs-lookup"><span data-stu-id="0894d-182">You can create a rule to suspend leave accruals for employees with leave requests entered for unpaid leave.</span></span> <span data-ttu-id="0894d-183">無給休暇のタイプを指定できますが、必須ではあります。</span><span class="sxs-lookup"><span data-stu-id="0894d-183">Unpaid leave can be a type, but doesn't have to be.</span></span> <span data-ttu-id="0894d-184">他の休暇種類に基づいて、任意の休暇を停止することができます。</span><span class="sxs-lookup"><span data-stu-id="0894d-184">You can suspend any leave based on another leave type.</span></span>

## <a name="dmf-entity-available-for-accrual-suspensions"></a><span data-ttu-id="0894d-185">DMF エンティティで休暇付与の一時停止が可能</span><span class="sxs-lookup"><span data-stu-id="0894d-185">DMF entity available for accrual suspensions</span></span> 

<span data-ttu-id="0894d-186">DMF エンティティが見越し計上の停止に使用できるようになりました 。</span><span class="sxs-lookup"><span data-stu-id="0894d-186">A DMF entity is now available for accrual suspensions.</span></span>

## <a name="coming-soon"></a><span data-ttu-id="0894d-187">間もなく公開</span><span class="sxs-lookup"><span data-stu-id="0894d-187">Coming soon</span></span>

## <a name="checklist-entities-included-in-dataverse"></a><span data-ttu-id="0894d-188">Dataverse に含まれるチェックリスト エンティティ</span><span class="sxs-lookup"><span data-stu-id="0894d-188">Checklist entities included in Dataverse</span></span>

<span data-ttu-id="0894d-189">オンボード、オフボード、転送、および業務プロセスのチェックリスト エンティティは、Dataverse ですぐに使用可能になります。</span><span class="sxs-lookup"><span data-stu-id="0894d-189">Checklist entities for Onboarding, Offboarding, Transfers, and Business processes will be available soon in Dataverse.</span></span>

## <a name="see-also"></a><span data-ttu-id="0894d-190">参照</span><span class="sxs-lookup"><span data-stu-id="0894d-190">See also</span></span>

[<span data-ttu-id="0894d-191">Human Resources の新機能および変更された機能</span><span class="sxs-lookup"><span data-stu-id="0894d-191">What's new or changed in Human Resources</span></span>](hr-admin-whats-new.md)</br>
[<span data-ttu-id="0894d-192">Dynamics 365 Human Resources 2019 のリリース ウェーブ 2 の概要</span><span class="sxs-lookup"><span data-stu-id="0894d-192">Overview of Dynamics 365 Human Resources 2019 release wave 2</span></span>](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[<span data-ttu-id="0894d-193">更新プロセス</span><span class="sxs-lookup"><span data-stu-id="0894d-193">Update process</span></span>](hr-admin-setup-update-process.md)</br>
[<span data-ttu-id="0894d-194">機能の管理</span><span class="sxs-lookup"><span data-stu-id="0894d-194">Manage features</span></span>](hr-admin-manage-features.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]