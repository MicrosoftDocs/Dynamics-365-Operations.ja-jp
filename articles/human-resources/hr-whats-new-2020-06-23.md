---
title: Dynamics 365 Human Resources の新機能または変更された機能 (2020 年 6 月 25 日)
description: このトピックでは、2020 年 6 月 23 日に更新された、Microsoft Dynamics 365 Human Resources の新機能、または変更された機能について説明します。
author: andreabichsel
manager: tfehr
ms.date: 06/25/2020
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
ms.author: jaredha
ms.search.validFrom: 2020-06-25
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: ad80e53c0a24d602ac446d3e0765f397dd0fc2d9
ms.sourcegitcommit: f8bac7ca2803913fd236adbc3806259a17a110f4
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/06/2021
ms.locfileid: "5127500"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-june-23-2020"></a><span data-ttu-id="c404d-103">Dynamics 365 Human Resources の新機能または変更された機能 (2020 年 6 月 23 日)</span><span class="sxs-lookup"><span data-stu-id="c404d-103">What's new or changed in Dynamics 365 Human Resources (June 23, 2020)</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="c404d-104">このトピックでは、Dynamics 365 Human Resources の新機能または変更された機能について説明します。</span><span class="sxs-lookup"><span data-stu-id="c404d-104">This topic describes features that are either new or changed in Dynamics 365 Human Resources.</span></span> <span data-ttu-id="c404d-105">変更は、ビルド番号 8.1.3347 に適用されます。</span><span class="sxs-lookup"><span data-stu-id="c404d-105">Changes apply to build number 8.1.3347.</span></span> <span data-ttu-id="c404d-106">ヘッダーにあるかっこ内の数字は、参照用の LCS のサポート番号を参照していることがあります。</span><span class="sxs-lookup"><span data-stu-id="c404d-106">The numbers in parentheses in some headings refer to LCS support numbers for reference.</span></span>

## <a name="when-an-enrollment-is-expired-for-a-terminated-employee-the-leave-type-balance-and-amount-are-all-cleared-in-the-leave-enrollment-form-444867"></a><span data-ttu-id="c404d-107">加入契約は退職した従業員に対して期限切れになると、休暇タイプ、残高、および金額は、休暇登録フォーム にてすべてクリアされます (444867)</span><span class="sxs-lookup"><span data-stu-id="c404d-107">When an enrollment is expired for a terminated employee, the leave type, balance, and amount are all cleared in the Leave enrollment form (444867)</span></span>

<span data-ttu-id="c404d-108">**休暇タイプ**、**残高**、および **金額** は、この選択でクリアはされず、維持されるようになります。</span><span class="sxs-lookup"><span data-stu-id="c404d-108">Values in the **Leave type**, **Balance**, and **Amount** are now maintained instead of cleared upon making this selection.</span></span>

## <a name="incorrect-forecasted-balance-when-new-feature-leave-accrual-for-a-single-company-or-a-single-plan-is-enabled-456553"></a><span data-ttu-id="c404d-109">新しい機能 (1 つの会社または 1 つの計画に対する休暇見越) が有効な場合、予測残高は正しくありません (456553)</span><span class="sxs-lookup"><span data-stu-id="c404d-109">Incorrect forecasted balance when new feature (Leave accrual for a single company or a single plan) is enabled (456553)</span></span>

<span data-ttu-id="c404d-110">1 つの会社または 1 つの計画に対する休暇見越が有効な場合、予測残高は正しいです。</span><span class="sxs-lookup"><span data-stu-id="c404d-110">The correct forecasted balance now displays when the leave accrual for a single company or single plan has been enabled.</span></span>

## <a name="entities-with-relations-that-result-in-duplicate-navigation-properties-456486"></a><span data-ttu-id="c404d-111">ナビゲーション プロパティが重複する可能性のある関係を含むエンティティ (456486)</span><span class="sxs-lookup"><span data-stu-id="c404d-111">Entities with relations that result in duplicate navigation properties (456486)</span></span>

<span data-ttu-id="c404d-112">このリリースでは、複数のエンティティのナビゲーション プロパティ (関係) に関する問題が修正されます。</span><span class="sxs-lookup"><span data-stu-id="c404d-112">This release corrects an issue with the navigation properties (relation) of multiple entities.</span></span> <span data-ttu-id="c404d-113">重複する関係が検出されます。</span><span class="sxs-lookup"><span data-stu-id="c404d-113">Duplicate relations are detected.</span></span> <span data-ttu-id="c404d-114">これらのシナリオは、すべて修正されました。</span><span class="sxs-lookup"><span data-stu-id="c404d-114">These scenarios have all been corrected.</span></span>
 
## <a name="cross-company-comments-on-performance-review-455536"></a><span data-ttu-id="c404d-115">パフォーマンス レビューに関する会社間のコメント (455536)</span><span class="sxs-lookup"><span data-stu-id="c404d-115">Cross-company comments on Performance review (455536)</span></span>

<span data-ttu-id="c404d-116">この修正を行うと、会社間コメントがパフォーマンス レビューに表示されるようになります。</span><span class="sxs-lookup"><span data-stu-id="c404d-116">Cross-company comments are now visible on performance reviews with this fix.</span></span> <span data-ttu-id="c404d-117">この変更により、同じパフォーマンス レビューのために複数の会社で入力された校閲者コメントの表示が修正されます。</span><span class="sxs-lookup"><span data-stu-id="c404d-117">This change corrects the view of reviewer comments that were entered in different companies for the same performance review.</span></span>
 
## <a name="inconsistency-in-showing-compensation-management-data-432562"></a><span data-ttu-id="c404d-118">報酬管理データの表示に不整合があります (432562)</span><span class="sxs-lookup"><span data-stu-id="c404d-118">Inconsistency in showing compensation management data (432562)</span></span>

<span data-ttu-id="c404d-119">報酬データの一貫した見解が、マネージャーのセルフ サービスで保持されるようになりました。</span><span class="sxs-lookup"><span data-stu-id="c404d-119">A consistent view of compensation data is now maintained in Manager self service.</span></span> <span data-ttu-id="c404d-120">報酬データは、作業者の **報酬の詳細** にどのように移動するかによって、一貫してマネージャーに表示されるようになっています。</span><span class="sxs-lookup"><span data-stu-id="c404d-120">Depending on how you navigate to a worker's **Compensation details**, compensation data now consistently displays to managers.</span></span>
 
## <a name="fixed-compensation-plans-effective-date-defaults-to-todays-date-411994"></a><span data-ttu-id="c404d-121">固定報酬プランの有効日の既定値は、今日の日付です (411994)</span><span class="sxs-lookup"><span data-stu-id="c404d-121">Fixed compensation plan's effective date defaults to today's date (411994)</span></span>

<span data-ttu-id="c404d-122">これで、報酬の開始日は、従業員に割り当てられている職位の開始日に基づいています。</span><span class="sxs-lookup"><span data-stu-id="c404d-122">The compensation start date is now based on the start date of the position being assigned to the employee.</span></span>

## <a name="leave-and-absence-form-enable-half-day-definition-is-disabled-when-form-opens-452607"></a><span data-ttu-id="c404d-123">半日の定義を有効にする休暇と欠勤のフォームが開くと、その定義は無効になります (452607)</span><span class="sxs-lookup"><span data-stu-id="c404d-123">Leave and absence form Enable half day definition is disabled when form opens (452607)</span></span>

<span data-ttu-id="c404d-124">この変更により、**半日の定義を有効にする** は、新しい休暇トランザクションが存在するまで有効になります。</span><span class="sxs-lookup"><span data-stu-id="c404d-124">With this change, the **Enable half day definition** will be enabled until new leave transactions exist.</span></span> 

## <a name="unable-to-publish-to-hcmdiscussionentity-via-excel-totalratingscore-field-error-453899"></a><span data-ttu-id="c404d-125">Excel 経由で HcmDiscussionEntity に発行することはできません; TotalRatingScore フィールド エラー (453899)</span><span class="sxs-lookup"><span data-stu-id="c404d-125">Unable to publish to HcmDiscussionEntity via Excel; TotalRatingScore field error (453899)</span></span>

<span data-ttu-id="c404d-126">これで、Excel ブック デザイナーの **HCMDiscussionEntity** を使用して、**TotalRatingScore** 項目を更新できます。</span><span class="sxs-lookup"><span data-stu-id="c404d-126">You can now update the **TotalRatingScore** field using **HCMDiscussionEntity** in the Excel workbook designer.</span></span>

## <a name="in-preview"></a><span data-ttu-id="c404d-127">プレビュー</span><span class="sxs-lookup"><span data-stu-id="c404d-127">In preview</span></span>

## <a name="database-logging"></a><span data-ttu-id="c404d-128">データベースのログ</span><span class="sxs-lookup"><span data-stu-id="c404d-128">Database logging</span></span>

<span data-ttu-id="c404d-129">データベース ログを使用すると、監視するテーブルとフィールドを決定できます。</span><span class="sxs-lookup"><span data-stu-id="c404d-129">Database logging allows you to determine which tables and fields to monitor.</span></span> <span data-ttu-id="c404d-130">また、Change Tracking を起動するイベントを決定することもできます。</span><span class="sxs-lookup"><span data-stu-id="c404d-130">It also lets you determine the events that should trigger change tracking.</span></span> <span data-ttu-id="c404d-131">これらの変更を時間の経過と共に確認するには、データベースのログ機能を使用します。</span><span class="sxs-lookup"><span data-stu-id="c404d-131">You use database logging capabilities to see these changes over time.</span></span> <span data-ttu-id="c404d-132">詳細については、[データベース ログの構成と管理](hr-admin-database-logging.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="c404d-132">For more information, see [Configure and manage database logging](hr-admin-database-logging.md).</span></span>

## <a name="mandatory-fields"></a><span data-ttu-id="c404d-133">必須項目</span><span class="sxs-lookup"><span data-stu-id="c404d-133">Mandatory fields</span></span> 

<span data-ttu-id="c404d-134">人事管理のパーソナル化機能を使用することにより、項目を必須にすることができます。</span><span class="sxs-lookup"><span data-stu-id="c404d-134">You can now make fields mandatory by using Human Resources personalization capabilities.</span></span> <span data-ttu-id="c404d-135">この機能には **保存されたビュー** が必要です。</span><span class="sxs-lookup"><span data-stu-id="c404d-135">This feature requires **Saved views**.</span></span>

## <a name="human-resources-application-in-teams"></a><span data-ttu-id="c404d-136">Teams の Human Resources アプリケーション</span><span class="sxs-lookup"><span data-stu-id="c404d-136">Human Resources application in Teams</span></span>

<span data-ttu-id="c404d-137">従業員は、Microsoft Teams 内で休暇の表示および申請ができます。</span><span class="sxs-lookup"><span data-stu-id="c404d-137">Employees can view and request time away from work within Microsoft Teams.</span></span> <span data-ttu-id="c404d-138">ボットと対話して、休暇申請を作成できます。</span><span class="sxs-lookup"><span data-stu-id="c404d-138">They can interact with a bot to create leave requests.</span></span> <span data-ttu-id="c404d-139">詳細については、[Teams の Human Resources アプリ](https://go.microsoft.com/fwlink/?linkid=2127841) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="c404d-139">For more information, see [Human Resources app in Teams](https://go.microsoft.com/fwlink/?linkid=2127841).</span></span> 

## <a name="data-management-framework-dmf-entities-for-benefits-management"></a><span data-ttu-id="c404d-140">福利厚生管理のためのデータ管理フレームワーク (DMF) エンティティ</span><span class="sxs-lookup"><span data-stu-id="c404d-140">Data management framework (DMF) entities for Benefits management</span></span>
 
<span data-ttu-id="c404d-141">福利厚生管理エンティティはリリースされてます。</span><span class="sxs-lookup"><span data-stu-id="c404d-141">Benefits management entities are releasing.</span></span> <span data-ttu-id="c404d-142">DMF エンティティを使用すると、データをインポートおよびエクスポートして、福利厚生管理を簡単に構成できます。</span><span class="sxs-lookup"><span data-stu-id="c404d-142">DMF entities allow you to import and export data to easily configure benefits management.</span></span> <span data-ttu-id="c404d-143">福利厚生管理テンプレートは、データの移動に使用できます。</span><span class="sxs-lookup"><span data-stu-id="c404d-143">A Benefits management template will be available to move data.</span></span> <span data-ttu-id="c404d-144">テンプレートは、データの依存関係を考慮してデータを順次エクスポートおよびインポートします。</span><span class="sxs-lookup"><span data-stu-id="c404d-144">The template exports and imports the data sequentially to respect data dependencies.</span></span>

## <a name="buy-and-sell-leave"></a><span data-ttu-id="c404d-145">休暇の売買</span><span class="sxs-lookup"><span data-stu-id="c404d-145">Buy and sell leave</span></span> 

<span data-ttu-id="c404d-146">一部の組織では、従業員が休暇を購入または売却できるという利点があります。</span><span class="sxs-lookup"><span data-stu-id="c404d-146">Some organizations provide a benefit that allows employees to buy or sell their leave.</span></span> <span data-ttu-id="c404d-147">このプロセスは、多くの場合、手動で管理します。</span><span class="sxs-lookup"><span data-stu-id="c404d-147">This process is often managed manually.</span></span> <span data-ttu-id="c404d-148">この機能により、人事部門のポリシーと申請の管理を自動化します。</span><span class="sxs-lookup"><span data-stu-id="c404d-148">This feature automates managing policies and requests for the HR department.</span></span> <span data-ttu-id="c404d-149">休暇管理プロセスを合理化し、ミスをなくすことができます。</span><span class="sxs-lookup"><span data-stu-id="c404d-149">It streamlines the leave management process and helps eliminate mistakes.</span></span> <span data-ttu-id="c404d-150">詳細については、以下を参照してください。</span><span class="sxs-lookup"><span data-stu-id="c404d-150">For more information, see:</span></span>

- [<span data-ttu-id="c404d-151">休暇の売買ポリシーの管理</span><span class="sxs-lookup"><span data-stu-id="c404d-151">Manage buy and sell leave policies</span></span>](hr-leave-and-absence-manage-buy-and-sell-leave-policies.md)
- [<span data-ttu-id="c404d-152">休暇の売買</span><span class="sxs-lookup"><span data-stu-id="c404d-152">Buy and sell leave</span></span>](hr-employee-self-service-buy-sell-leave.md)

## <a name="leave-accrual-for-a-single-company-or-single-plan"></a><span data-ttu-id="c404d-153">1 社または 1 プランの有給休暇</span><span class="sxs-lookup"><span data-stu-id="c404d-153">Leave accrual for a single company or single plan</span></span>

<span data-ttu-id="c404d-154">顧客は、1 社または 1 休暇および不就業プランの有給休暇を処理できます。</span><span class="sxs-lookup"><span data-stu-id="c404d-154">Customers can process accruals for a single company or a single leave and absence plan.</span></span> <span data-ttu-id="c404d-155">この機能により、異なる休暇年数または有給休暇ポリシーを持つ顧客のために有給休暇プロセスを明確にします。</span><span class="sxs-lookup"><span data-stu-id="c404d-155">This ability provides clarity into the accrual process for customers with different leave years or leave accrual policies.</span></span> <span data-ttu-id="c404d-156">詳細については、[会社別または休暇プラン別の有給休暇](hr-leave-and-absence-accrue.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="c404d-156">For more information, see [Accrue leave per company or per leave plan](hr-leave-and-absence-accrue.md).</span></span>

## <a name="add-attachments-to-time-off-requests"></a><span data-ttu-id="c404d-157">添付ファイルを休暇申請に追加</span><span class="sxs-lookup"><span data-stu-id="c404d-157">Add attachments to time off requests</span></span>

<span data-ttu-id="c404d-158">承認済み休暇申請に添付ファイルを追加する機能は、現在の COVID-19 環境では非常に重要です。</span><span class="sxs-lookup"><span data-stu-id="c404d-158">The ability to add attachments to approved leave requests is critical in the current COVID-19 environment.</span></span> <span data-ttu-id="c404d-159">従業員はこれらの添付ファイルを追加できます。</span><span class="sxs-lookup"><span data-stu-id="c404d-159">Employees can now add these attachments.</span></span> <span data-ttu-id="c404d-160">また、休暇申請がどのように更新されるかについても、より深く理解することができます。</span><span class="sxs-lookup"><span data-stu-id="c404d-160">They also have more insight into how updates are made to leave requests.</span></span> <span data-ttu-id="c404d-161">詳細については、[既存の申請に添付ファイルを追加](hr-employee-self-service-request-time-off.md#add-an-attachment-to-an-existing-request) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="c404d-161">For more information, see [Add an attachment to an existing request](hr-employee-self-service-request-time-off.md#add-an-attachment-to-an-existing-request).</span></span>

## <a name="add-reason-code-to-accrual-suspensions"></a><span data-ttu-id="c404d-162">休暇付与の一時停止に理由コードが追加されました</span><span class="sxs-lookup"><span data-stu-id="c404d-162">Add reason code to accrual suspensions</span></span> 

<span data-ttu-id="c404d-163">見越計上の中断に理由コードが追加されました。</span><span class="sxs-lookup"><span data-stu-id="c404d-163">Reason codes have been added to the accrual suspension.</span></span>

## <a name="carry-forward-rules"></a><span data-ttu-id="c404d-164">繰越ルール</span><span class="sxs-lookup"><span data-stu-id="c404d-164">Carry forward rules</span></span> 

<span data-ttu-id="c404d-165">繰越調整を転送する繰越残日数に対して、繰越休暇タイプを指定できます。</span><span class="sxs-lookup"><span data-stu-id="c404d-165">You can specify a carry forward leave type for carry forward balances where carry forward adjustments are transferred.</span></span> <span data-ttu-id="c404d-166">たとえば、従業員が 10 日間繰り越す場合、その 10 日間に別の休暇タイプを選択できます。</span><span class="sxs-lookup"><span data-stu-id="c404d-166">For example, if an employee carries forward 10 days, you can pick a different leave type for those 10 days.</span></span> <span data-ttu-id="c404d-167">詳細については、[休暇および欠勤タイプのコンフィギュレーション](hr-leave-and-absence-types.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="c404d-167">For more information, see [Configure leave and absence types](hr-leave-and-absence-types.md).</span></span>

## <a name="suspend-leave-accrual-for-specified-leave-types"></a><span data-ttu-id="c404d-168">指定した休暇タイプに対する休暇付与の一時停止</span><span class="sxs-lookup"><span data-stu-id="c404d-168">Suspend leave accrual for specified leave types</span></span>

<span data-ttu-id="c404d-169">無給休暇で休暇申請を入力した従業員に対して、休暇の発生を停止するルールを作成することができます。</span><span class="sxs-lookup"><span data-stu-id="c404d-169">You can create a rule to suspend leave accruals for employees with leave requests entered for unpaid leave.</span></span> <span data-ttu-id="c404d-170">無給休暇のタイプを指定できますが、必須ではあります。</span><span class="sxs-lookup"><span data-stu-id="c404d-170">Unpaid leave can be a type, but doesn't have to be.</span></span> <span data-ttu-id="c404d-171">他の休暇種類に基づいて、任意の休暇を停止することができます。</span><span class="sxs-lookup"><span data-stu-id="c404d-171">You can suspend any leave based on another leave type.</span></span>

## <a name="dmf-entity-available-for-accrual-suspensions"></a><span data-ttu-id="c404d-172">DMF エンティティで休暇付与の一時停止が可能</span><span class="sxs-lookup"><span data-stu-id="c404d-172">DMF entity available for accrual suspensions</span></span> 

<span data-ttu-id="c404d-173">DMF エンティティが見越し計上の停止に使用できるようになりました 。</span><span class="sxs-lookup"><span data-stu-id="c404d-173">A DMF entity is now available for accrual suspensions.</span></span>

## <a name="coming-soon"></a><span data-ttu-id="c404d-174">間もなく公開</span><span class="sxs-lookup"><span data-stu-id="c404d-174">Coming soon</span></span>

## <a name="configure-the-name-of-employee-self-service"></a><span data-ttu-id="c404d-175">従業員セルフ サービス名のコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="c404d-175">Configure the name of Employee self-service</span></span>

<span data-ttu-id="c404d-176">**人事管理パラメータ** で新しいオプションが使用可能になり、従業員セルフ サービス ワークスペースの名前をセルフ サービスに更新します。</span><span class="sxs-lookup"><span data-stu-id="c404d-176">A new option will be available in **Human Resources parameters** to update the name of the Employee self service workspace to Self service.</span></span>

## <a name="checklist-entities-included-in-dataverse"></a><span data-ttu-id="c404d-177">Dataverse に含まれるチェックリスト エンティティ</span><span class="sxs-lookup"><span data-stu-id="c404d-177">Checklist entities included in Dataverse</span></span>

<span data-ttu-id="c404d-178">オンボード、オフボード、転送、および業務プロセスのチェックリスト エンティティは、Dataverse 内ですぐに使用可能になります。</span><span class="sxs-lookup"><span data-stu-id="c404d-178">Checklist entities for Onboarding, Offboarding, Transfers, and Business processes will be available soon within Dataverse.</span></span>

## <a name="see-also"></a><span data-ttu-id="c404d-179">参照</span><span class="sxs-lookup"><span data-stu-id="c404d-179">See also</span></span>

[<span data-ttu-id="c404d-180">Human Resources の新機能および変更された機能</span><span class="sxs-lookup"><span data-stu-id="c404d-180">What's new or changed in Human Resources</span></span>](hr-admin-whats-new.md)</br>
[<span data-ttu-id="c404d-181">Dynamics 365 Human Resources 2019 のリリース ウェーブ 2 の概要</span><span class="sxs-lookup"><span data-stu-id="c404d-181">Overview of Dynamics 365 Human Resources 2019 release wave 2</span></span>](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[<span data-ttu-id="c404d-182">更新プロセス</span><span class="sxs-lookup"><span data-stu-id="c404d-182">Update process</span></span>](hr-admin-setup-update-process.md)</br>
[<span data-ttu-id="c404d-183">機能の管理</span><span class="sxs-lookup"><span data-stu-id="c404d-183">Manage features</span></span>](hr-admin-manage-features.md)