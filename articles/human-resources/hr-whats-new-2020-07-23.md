---
title: Dynamics 365 Human Resources の新機能、または変更された機能 (2020 年 7 月 23 日)
description: このトピックでは、2020 年 7 月 23 日に更新された、Microsoft Dynamics 365 Human Resources の新機能、または変更された機能について説明します。
author: andreabichsel
ms.date: 07/23/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2020-07-23
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: e48b0694418710322957de811952e12da22b0509
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/18/2021
ms.locfileid: "6055392"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-july-23-2020"></a><span data-ttu-id="667b5-103">Dynamics 365 Human Resources の新機能、または変更された機能 (2020 年 7 月 23 日)</span><span class="sxs-lookup"><span data-stu-id="667b5-103">What's new or changed in Dynamics 365 Human Resources (July 23, 2020)</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="667b5-104">このトピックでは、Dynamics 365 Human Resources の新機能または変更された機能について説明します。</span><span class="sxs-lookup"><span data-stu-id="667b5-104">This topic describes features that are either new or changed in Dynamics 365 Human Resources.</span></span> <span data-ttu-id="667b5-105">変更は、ビルド番号 8.1.3416 に適用されます。</span><span class="sxs-lookup"><span data-stu-id="667b5-105">Changes apply to build number 8.1.3416.</span></span> <span data-ttu-id="667b5-106">ヘッダーにあるかっこ内の数字は、参照用の LCS のサポート番号を参照していることがあります。</span><span class="sxs-lookup"><span data-stu-id="667b5-106">The numbers in parentheses in some headings refer to LCS support numbers for reference.</span></span>

## <a name="deleting-financial-dimensions-on-a-position-doesnt-work-as-expected-445476"></a><span data-ttu-id="667b5-107">職位の財務分析コードの削除が想定された機能をしない (445476)</span><span class="sxs-lookup"><span data-stu-id="667b5-107">Deleting Financial Dimensions on a Position doesn't work as expected (445476)</span></span>

<span data-ttu-id="667b5-108">職位から分析コードを削除すると、Dataverse からも同じ職位が削除されてしまう。</span><span class="sxs-lookup"><span data-stu-id="667b5-108">Removing dimensions from a position now removes those same positions from Dataverse.</span></span>

## <a name="positions-not-in-hierarchy-show-inactive-positions-397257"></a><span data-ttu-id="667b5-109">階層にない職位が非アクティブな職位を表示する (397257)</span><span class="sxs-lookup"><span data-stu-id="667b5-109">Positions not in hierarchy show inactive positions (397257)</span></span>

<span data-ttu-id="667b5-110">非アクティブな (有効期間が切れている) 職位が、**階層内の職位** として職位階層に表示されなくなる。</span><span class="sxs-lookup"><span data-stu-id="667b5-110">Positions that are inactive (have an expired duration), no longer display in the position hierarchy as **Positions not in hierarchy**.</span></span> 

## <a name="validation-occurring-between-leaveenrollmententity-and-hcmworkerentity-on-data-management-framework-dmf-import-causes-slow-data-loads-442324"></a><span data-ttu-id="667b5-111">データ管理フレームワーク (DMF) インポートにおける LeaveEnrollmentEntity と HcmWorkerEntity との間で検証処理が発生し、データの読み込みが遅くなる (442324)</span><span class="sxs-lookup"><span data-stu-id="667b5-111">Validation occurring between LeaveEnrollmentEntity and HcmWorkerEntity on Data Management Framework (DMF) import causes slow data loads (442324)</span></span>

<span data-ttu-id="667b5-112">このリリースでの変更により、**LeaveEnrollmentEntity** のパフォーマンスが向上します。</span><span class="sxs-lookup"><span data-stu-id="667b5-112">Changes in this release increase the performance of **LeaveEnrollmentEntity**.</span></span>

## <a name="unable-to-personalize-in-organization-administration-447490"></a><span data-ttu-id="667b5-113">組織管理のカスタマイズができない (447490)</span><span class="sxs-lookup"><span data-stu-id="667b5-113">Unable to personalize in Organization administration (447490)</span></span>

<span data-ttu-id="667b5-114">今回の変更では、**組織の管理** でリンクをカスタマイズできるようになります。</span><span class="sxs-lookup"><span data-stu-id="667b5-114">With this change, you can now personalize the links in **Organization administration**.</span></span>

## <a name="in-preview"></a><span data-ttu-id="667b5-115">プレビュー</span><span class="sxs-lookup"><span data-stu-id="667b5-115">In preview</span></span>

## <a name="mandatory-fields"></a><span data-ttu-id="667b5-116">必須項目</span><span class="sxs-lookup"><span data-stu-id="667b5-116">Mandatory fields</span></span> 

<span data-ttu-id="667b5-117">人事管理のパーソナル化機能を使用することにより、項目を必須にすることができます。</span><span class="sxs-lookup"><span data-stu-id="667b5-117">You can now make fields mandatory by using Human Resources personalization capabilities.</span></span> <span data-ttu-id="667b5-118">この機能には **保存されたビュー** が必要です。</span><span class="sxs-lookup"><span data-stu-id="667b5-118">This feature requires **Saved views**.</span></span>

## <a name="human-resources-application-in-teams"></a><span data-ttu-id="667b5-119">Teams の Human Resources アプリケーション</span><span class="sxs-lookup"><span data-stu-id="667b5-119">Human Resources application in Teams</span></span>

<span data-ttu-id="667b5-120">従業員は、Microsoft Teams 内で休暇の表示および申請ができます。</span><span class="sxs-lookup"><span data-stu-id="667b5-120">Employees can view and request time away from work within Microsoft Teams.</span></span> <span data-ttu-id="667b5-121">ボットと対話して、休暇申請を作成できます。</span><span class="sxs-lookup"><span data-stu-id="667b5-121">They can interact with a bot to create leave requests.</span></span> <span data-ttu-id="667b5-122">詳細については、[Teams の Human Resources アプリ](./hr-admin-teams-leave-app.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="667b5-122">For more information, see [Human Resources app in Teams](./hr-admin-teams-leave-app.md).</span></span> 

## <a name="data-management-framework-dmf-entities-for-benefits-management"></a><span data-ttu-id="667b5-123">福利厚生管理のためのデータ管理フレームワーク (DMF) エンティティ</span><span class="sxs-lookup"><span data-stu-id="667b5-123">Data management framework (DMF) entities for Benefits management</span></span>
 
<span data-ttu-id="667b5-124">福利厚生管理エンティティはリリースされてます。</span><span class="sxs-lookup"><span data-stu-id="667b5-124">Benefits management entities are releasing.</span></span> <span data-ttu-id="667b5-125">DMF エンティティを使用すると、データをインポートおよびエクスポートして、福利厚生管理を簡単に構成できます。</span><span class="sxs-lookup"><span data-stu-id="667b5-125">DMF entities allow you to import and export data to easily configure benefits management.</span></span> <span data-ttu-id="667b5-126">福利厚生管理テンプレートは、データの移動に使用できます。</span><span class="sxs-lookup"><span data-stu-id="667b5-126">A Benefits management template will be available to move data.</span></span> <span data-ttu-id="667b5-127">テンプレートは、データの依存関係を考慮してデータを順次エクスポートおよびインポートします。</span><span class="sxs-lookup"><span data-stu-id="667b5-127">The template exports and imports the data sequentially to respect data dependencies.</span></span>

## <a name="buy-and-sell-leave"></a><span data-ttu-id="667b5-128">休暇の売買</span><span class="sxs-lookup"><span data-stu-id="667b5-128">Buy and sell leave</span></span> 

<span data-ttu-id="667b5-129">一部の組織では、従業員が休暇を購入または売却できるという利点があります。</span><span class="sxs-lookup"><span data-stu-id="667b5-129">Some organizations provide a benefit that allows employees to buy or sell their leave.</span></span> <span data-ttu-id="667b5-130">このプロセスは、多くの場合、手動で管理します。</span><span class="sxs-lookup"><span data-stu-id="667b5-130">This process is often managed manually.</span></span> <span data-ttu-id="667b5-131">この機能により、人事部門のポリシーと申請の管理を自動化します。</span><span class="sxs-lookup"><span data-stu-id="667b5-131">This feature automates managing policies and requests for the HR department.</span></span> <span data-ttu-id="667b5-132">休暇管理プロセスを合理化し、ミスをなくすことができます。</span><span class="sxs-lookup"><span data-stu-id="667b5-132">It streamlines the leave management process and helps eliminate mistakes.</span></span> <span data-ttu-id="667b5-133">詳細については、以下を参照してください。</span><span class="sxs-lookup"><span data-stu-id="667b5-133">For more information, see:</span></span>

- [<span data-ttu-id="667b5-134">休暇の売買ポリシーの管理</span><span class="sxs-lookup"><span data-stu-id="667b5-134">Manage buy and sell leave policies</span></span>](hr-leave-and-absence-manage-buy-and-sell-leave-policies.md)
- [<span data-ttu-id="667b5-135">休暇の売買</span><span class="sxs-lookup"><span data-stu-id="667b5-135">Buy and sell leave</span></span>](hr-employee-self-service-buy-sell-leave.md)

## <a name="leave-accrual-for-a-single-company-or-single-plan"></a><span data-ttu-id="667b5-136">1 社または 1 プランの有給休暇</span><span class="sxs-lookup"><span data-stu-id="667b5-136">Leave accrual for a single company or single plan</span></span>

<span data-ttu-id="667b5-137">顧客は、1 社または 1 休暇および不就業プランの有給休暇を処理できます。</span><span class="sxs-lookup"><span data-stu-id="667b5-137">Customers can process accruals for a single company or a single leave and absence plan.</span></span> <span data-ttu-id="667b5-138">この機能を使用することで、異なる休暇年数や有給休暇ポリシーを持つ顧客に向けた有給休暇のプロセスを明確化します。</span><span class="sxs-lookup"><span data-stu-id="667b5-138">This ability provides clarity for the accrual process for customers with different leave years or leaves accrual policies.</span></span> <span data-ttu-id="667b5-139">詳細については、[会社別または休暇プラン別の有給休暇](hr-leave-and-absence-accrue.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="667b5-139">For more information, see [Accrue leave per company or per leave plan](hr-leave-and-absence-accrue.md).</span></span>

## <a name="add-attachments-to-time-off-requests"></a><span data-ttu-id="667b5-140">添付ファイルを休暇申請に追加</span><span class="sxs-lookup"><span data-stu-id="667b5-140">Add attachments to time-off requests</span></span>

<span data-ttu-id="667b5-141">承認済み休暇申請に添付ファイルを追加する機能は、現在の COVID-19 環境では非常に重要です。</span><span class="sxs-lookup"><span data-stu-id="667b5-141">The ability to add attachments to approved leave requests is critical in the current COVID-19 environment.</span></span> <span data-ttu-id="667b5-142">従業員はこれらの添付ファイルを追加できます。</span><span class="sxs-lookup"><span data-stu-id="667b5-142">Employees can now add these attachments.</span></span> <span data-ttu-id="667b5-143">また、休暇申請がどのように更新されるかについても、より深く理解することができます。</span><span class="sxs-lookup"><span data-stu-id="667b5-143">They also have more insight into how updates are made to leave requests.</span></span> <span data-ttu-id="667b5-144">詳細については、[既存の申請に添付ファイルを追加](hr-employee-self-service-request-time-off.md#add-an-attachment-to-an-existing-request) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="667b5-144">For more information, see [Add an attachment to an existing request](hr-employee-self-service-request-time-off.md#add-an-attachment-to-an-existing-request).</span></span>

## <a name="add-reason-code-to-accrual-suspensions"></a><span data-ttu-id="667b5-145">休暇付与の一時停止に理由コードが追加されました</span><span class="sxs-lookup"><span data-stu-id="667b5-145">Add reason code to accrual suspensions</span></span> 

<span data-ttu-id="667b5-146">見越計上の中断に理由コードが追加されました。</span><span class="sxs-lookup"><span data-stu-id="667b5-146">Reason codes have been added to the accrual suspension.</span></span>

## <a name="carry-forward-rules"></a><span data-ttu-id="667b5-147">繰越ルール</span><span class="sxs-lookup"><span data-stu-id="667b5-147">Carry forward rules</span></span> 

<span data-ttu-id="667b5-148">繰越調整を転送する繰越残日数に対して、繰越休暇タイプを指定できます。</span><span class="sxs-lookup"><span data-stu-id="667b5-148">You can specify a carry forward leave type for carry forward balances where carry forward adjustments are transferred.</span></span> <span data-ttu-id="667b5-149">たとえば、従業員が 10 日間繰り越す場合、その 10 日間に別の休暇タイプを選択できます。</span><span class="sxs-lookup"><span data-stu-id="667b5-149">For example, if an employee carries forward 10 days, you can pick a different leave type for those 10 days.</span></span> <span data-ttu-id="667b5-150">詳細については、[休暇および欠勤タイプのコンフィギュレーション](hr-leave-and-absence-types.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="667b5-150">For more information, see [Configure leave and absence types](hr-leave-and-absence-types.md).</span></span>

## <a name="suspend-leave-accrual-for-specified-leave-types"></a><span data-ttu-id="667b5-151">指定した休暇タイプに対する休暇付与の一時停止</span><span class="sxs-lookup"><span data-stu-id="667b5-151">Suspend leave accrual for specified leave types</span></span>

<span data-ttu-id="667b5-152">無給休暇で休暇申請を入力した従業員に対して、休暇の発生を停止するルールを作成することができます。</span><span class="sxs-lookup"><span data-stu-id="667b5-152">You can create a rule to suspend leave accruals for employees with leave requests entered for unpaid leave.</span></span> <span data-ttu-id="667b5-153">無給休暇のタイプを指定できますが、必須ではあります。</span><span class="sxs-lookup"><span data-stu-id="667b5-153">Unpaid leave can be a type, but doesn't have to be.</span></span> <span data-ttu-id="667b5-154">他の休暇種類に基づいて、任意の休暇を停止することができます。</span><span class="sxs-lookup"><span data-stu-id="667b5-154">You can suspend any leave based on another leave type.</span></span>

## <a name="dmf-entity-available-for-accrual-suspensions"></a><span data-ttu-id="667b5-155">DMF エンティティで休暇付与の一時停止が可能</span><span class="sxs-lookup"><span data-stu-id="667b5-155">DMF entity available for accrual suspensions</span></span> 

<span data-ttu-id="667b5-156">DMF エンティティが見越し計上の停止に使用できるようになりました 。</span><span class="sxs-lookup"><span data-stu-id="667b5-156">A DMF entity is now available for accrual suspensions.</span></span>

## <a name="coming-soon"></a><span data-ttu-id="667b5-157">間もなく公開</span><span class="sxs-lookup"><span data-stu-id="667b5-157">Coming soon</span></span>

## <a name="checklist-entities-included-in-dataverse"></a><span data-ttu-id="667b5-158">Dataverse に含まれるチェックリスト エンティティ</span><span class="sxs-lookup"><span data-stu-id="667b5-158">Checklist entities included in Dataverse</span></span>

<span data-ttu-id="667b5-159">オンボード、オフボード、転送、および業務プロセスのチェックリスト エンティティは、Dataverse ですぐに使用可能になります。</span><span class="sxs-lookup"><span data-stu-id="667b5-159">Checklist entities for Onboarding, Offboarding, Transfers, and Business processes will be available soon in Dataverse.</span></span>

## <a name="platform-changes"></a><span data-ttu-id="667b5-160">プラットフォームの変更</span><span class="sxs-lookup"><span data-stu-id="667b5-160">Platform changes</span></span>

<span data-ttu-id="667b5-161">プラットフォーム 更新プログラム 10.0.12 (36)</span><span class="sxs-lookup"><span data-stu-id="667b5-161">Platform update 10.0.12 (36)</span></span>

## <a name="see-also"></a><span data-ttu-id="667b5-162">参照</span><span class="sxs-lookup"><span data-stu-id="667b5-162">See also</span></span>

[<span data-ttu-id="667b5-163">Human Resources の新機能および変更された機能</span><span class="sxs-lookup"><span data-stu-id="667b5-163">What's new or changed in Human Resources</span></span>](hr-admin-whats-new.md)</br>
[<span data-ttu-id="667b5-164">Dynamics 365 Human Resources 2019 のリリース ウェーブ 2 の概要</span><span class="sxs-lookup"><span data-stu-id="667b5-164">Overview of Dynamics 365 Human Resources 2019 release wave 2</span></span>](/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[<span data-ttu-id="667b5-165">更新プロセス</span><span class="sxs-lookup"><span data-stu-id="667b5-165">Update process</span></span>](hr-admin-setup-update-process.md)</br>
[<span data-ttu-id="667b5-166">機能の管理</span><span class="sxs-lookup"><span data-stu-id="667b5-166">Manage features</span></span>](hr-admin-manage-features.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]