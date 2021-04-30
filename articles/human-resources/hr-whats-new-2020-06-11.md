---
title: Dynamics 365 Human Resources の新機能または変更された機能 (2020 年 6 月 11 日)
description: このトピックでは、2020 年 6 月 11 日に更新された、Microsoft Dynamics 365 Human Resources の新機能、または変更された機能について説明します。
author: andreabichsel
ms.date: 06/16/2020
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
ms.search.validFrom: 2020-06-11
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 8265c0b6218f69b95f2729140aa303edeaa31443
ms.sourcegitcommit: 951393b05bf409333cb3c7ad977bcaa804aa801b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/13/2021
ms.locfileid: "5891940"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-june-11-2020"></a><span data-ttu-id="d2747-103">Dynamics 365 Human Resources の新機能または変更された機能 (2020 年 6 月 11 日)</span><span class="sxs-lookup"><span data-stu-id="d2747-103">What's new or changed in Dynamics 365 Human Resources (June 11, 2020)</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="d2747-104">この記事では、Dynamics 365 Human Resources の新機能および変更された機能について説明します。</span><span class="sxs-lookup"><span data-stu-id="d2747-104">This article describes features that are either new or changed in Dynamics 365 Human Resources.</span></span> <span data-ttu-id="d2747-105">変更は、ビルド番号 8.1.3316 に適用されます。</span><span class="sxs-lookup"><span data-stu-id="d2747-105">Changes apply to build number 8.1.3316.</span></span> <span data-ttu-id="d2747-106">ヘッダーにあるかっこ内の数字は、参照用の LCS のサポート番号を参照していることがあります。</span><span class="sxs-lookup"><span data-stu-id="d2747-106">The numbers in parentheses in some headings refer to LCS support numbers for reference.</span></span>

## <a name="streamlined-employee-form-sometimes-causes-child-form-close-x-buttons-to-stop-working-442369"></a><span data-ttu-id="d2747-107">合理化された従業員フォームにより、子フォームの閉じる (X) ボタンが機能しなくなることがある (442369)</span><span class="sxs-lookup"><span data-stu-id="d2747-107">Streamlined employee form sometimes causes child form close (X) buttons to stop working (442369)</span></span>

<span data-ttu-id="d2747-108">新しい **作業者** フォームが有効になっていると、閉じる (**X**) ボタンが子フォームで機能しないことがありました。</span><span class="sxs-lookup"><span data-stu-id="d2747-108">When the new **Worker** form was enabled, the close (**X**) button occasionally didn't work on child forms.</span></span> <span data-ttu-id="d2747-109">この問題は断続的でした。</span><span class="sxs-lookup"><span data-stu-id="d2747-109">This problem was intermittent.</span></span> <span data-ttu-id="d2747-110">離れて戻ってきた後に、フォームを開じることができます。</span><span class="sxs-lookup"><span data-stu-id="d2747-110">You could close the form after leaving and coming back to it.</span></span> <span data-ttu-id="d2747-111">たとえば、左側のメニュー項目を選択し、**作業者** フォームに戻ってから閉じることができます。</span><span class="sxs-lookup"><span data-stu-id="d2747-111">For example, you could select a menu item on the left, and navigate back to the **Worker** form, and then close it.</span></span> <span data-ttu-id="d2747-112">今週のリリースでは、この問題が修正されています。</span><span class="sxs-lookup"><span data-stu-id="d2747-112">This week's release fixes this problem.</span></span> 

## <a name="the-worker-personal-contact-person-entity-doesnt-export-personal-contacts-with-a-parent-relationship-type"></a><span data-ttu-id="d2747-113">作業者の個人連絡担当者エンティティが、親の関係タイプを持つ個人連絡先をエクスポートしない</span><span class="sxs-lookup"><span data-stu-id="d2747-113">The Worker personal contact person entity doesn't export personal contacts with a parent relationship type</span></span>

<span data-ttu-id="d2747-114">このリリースでは、**作業者の個人連絡担当者** エンティティが、すべての関係タイプをエクスポートします。</span><span class="sxs-lookup"><span data-stu-id="d2747-114">With this release, the **Worker personal contact person** entity exports all relationship types.</span></span>

## <a name="the-hcmpositionworkerassignmentv2entity-should-be-part-of-the-ceridian-payroll-integration-package-by-default-448506"></a><span data-ttu-id="d2747-115">HcmPositionWorkerAssignmentV2Entity は、既定で Ceridian 給与統合パッケージの一部である必要があります (448506)</span><span class="sxs-lookup"><span data-stu-id="d2747-115">The HcmPositionWorkerAssignmentV2Entity should be part of the Ceridian payroll integration package by default (448506)</span></span>

<span data-ttu-id="d2747-116">この変更により、**HcmPositionWorkerAssignmentV2Entity** が Ceridian 給与統合パッケージに含まれるようになりました。</span><span class="sxs-lookup"><span data-stu-id="d2747-116">With this change, the **HcmPositionWorkerAssignmentV2Entity** is included in the Ceridian payroll integration package.</span></span>

## <a name="in-preview"></a><span data-ttu-id="d2747-117">プレビュー</span><span class="sxs-lookup"><span data-stu-id="d2747-117">In preview</span></span>

## <a name="database-logging"></a><span data-ttu-id="d2747-118">データベースのログ</span><span class="sxs-lookup"><span data-stu-id="d2747-118">Database logging</span></span>

<span data-ttu-id="d2747-119">データベース ログ機能を使用すると、監視するテーブルとフィールドを決定できます。</span><span class="sxs-lookup"><span data-stu-id="d2747-119">The database logging feature allows you to determine which tables and fields to monitor.</span></span> <span data-ttu-id="d2747-120">また、Change Tracking を起動するイベントを決定することもできます。</span><span class="sxs-lookup"><span data-stu-id="d2747-120">It also lets you determine the events that should trigger change tracking.</span></span> <span data-ttu-id="d2747-121">これらの変更を時間の経過と共に確認するには、データベースのログ機能を使用します。</span><span class="sxs-lookup"><span data-stu-id="d2747-121">You use database logging capabilities to see these changes over time.</span></span> <span data-ttu-id="d2747-122">詳細については、[データベース ログの構成と管理](hr-admin-database-logging.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="d2747-122">For more information, see [Configure and manage database logging](hr-admin-database-logging.md).</span></span>

## <a name="human-resources-application-in-teams"></a><span data-ttu-id="d2747-123">Teams の Human Resources アプリケーション</span><span class="sxs-lookup"><span data-stu-id="d2747-123">Human Resources application in Teams</span></span>

<span data-ttu-id="d2747-124">従業員は、Microsoft Teams 内で休暇の表示および申請ができます。</span><span class="sxs-lookup"><span data-stu-id="d2747-124">Employees can view and request time away from work within Microsoft Teams.</span></span> <span data-ttu-id="d2747-125">ボットと対話して、休暇申請を作成できます。</span><span class="sxs-lookup"><span data-stu-id="d2747-125">They can interact with a bot to create leave requests.</span></span> <span data-ttu-id="d2747-126">詳細については、[Teams の Human Resources アプリ](./hr-admin-teams-leave-app.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="d2747-126">For more information, see [Human Resources app in Teams](./hr-admin-teams-leave-app.md).</span></span> 

## <a name="data-management-framework-dmf-entities-for-benefits-management"></a><span data-ttu-id="d2747-127">福利厚生管理のためのデータ管理フレームワーク (DMF) エンティティ</span><span class="sxs-lookup"><span data-stu-id="d2747-127">Data management framework (DMF) entities for Benefits management</span></span>
 
<span data-ttu-id="d2747-128">福利厚生管理エンティティはリリースされてます。</span><span class="sxs-lookup"><span data-stu-id="d2747-128">Benefits management entities are releasing.</span></span> <span data-ttu-id="d2747-129">DMF エンティティを使用すると、データをインポートおよびエクスポートして、福利厚生管理を簡単に構成できます。</span><span class="sxs-lookup"><span data-stu-id="d2747-129">DMF entities allow you to import and export data to easily configure benefits management.</span></span> <span data-ttu-id="d2747-130">福利厚生管理テンプレートは、データの移動に使用できます。</span><span class="sxs-lookup"><span data-stu-id="d2747-130">A Benefits management template will be available to move data.</span></span> <span data-ttu-id="d2747-131">テンプレートは、データの依存関係を考慮してデータを順次エクスポートおよびインポートします。</span><span class="sxs-lookup"><span data-stu-id="d2747-131">The template exports and imports the data sequentially to respect data dependencies.</span></span>

## <a name="buy-and-sell-leave"></a><span data-ttu-id="d2747-132">休暇の売買</span><span class="sxs-lookup"><span data-stu-id="d2747-132">Buy and sell leave</span></span> 

<span data-ttu-id="d2747-133">一部の組織では、従業員が休暇を購入または売却できるという利点があります。</span><span class="sxs-lookup"><span data-stu-id="d2747-133">Some organizations provide a benefit that allows employees to buy or sell their leave.</span></span> <span data-ttu-id="d2747-134">このプロセスは、多くの場合、手動で管理します。</span><span class="sxs-lookup"><span data-stu-id="d2747-134">This process is often managed manually.</span></span> <span data-ttu-id="d2747-135">この機能により、人事部門のポリシーと申請の管理を自動化します。</span><span class="sxs-lookup"><span data-stu-id="d2747-135">This feature automates managing policies and requests for the HR department.</span></span> <span data-ttu-id="d2747-136">休暇管理プロセスを合理化し、ミスをなくすことができます。</span><span class="sxs-lookup"><span data-stu-id="d2747-136">It streamlines the leave management process and helps eliminate mistakes.</span></span> <span data-ttu-id="d2747-137">詳細については、以下を参照してください。</span><span class="sxs-lookup"><span data-stu-id="d2747-137">For more information, see:</span></span>

- [<span data-ttu-id="d2747-138">休暇の売買ポリシーの管理</span><span class="sxs-lookup"><span data-stu-id="d2747-138">Manage buy and sell leave policies</span></span>](hr-leave-and-absence-manage-buy-and-sell-leave-policies.md)
- [<span data-ttu-id="d2747-139">休暇の売買</span><span class="sxs-lookup"><span data-stu-id="d2747-139">Buy and sell leave</span></span>](hr-employee-self-service-buy-sell-leave.md)

## <a name="leave-accrual-for-a-single-company-or-single-plan"></a><span data-ttu-id="d2747-140">1 社または 1 プランの有給休暇</span><span class="sxs-lookup"><span data-stu-id="d2747-140">Leave accrual for a single company or single plan</span></span>

<span data-ttu-id="d2747-141">顧客は、1 社または 1 休暇および不就業プランの有給休暇を処理できます。</span><span class="sxs-lookup"><span data-stu-id="d2747-141">Customers can process accruals for a single company or a single leave and absence plan.</span></span> <span data-ttu-id="d2747-142">この機能により、異なる休暇年数または有給休暇ポリシーを持つ顧客のために有給休暇プロセスを明確にします。</span><span class="sxs-lookup"><span data-stu-id="d2747-142">This ability provides clarity into the accrual process for customers with different leave years or leave accrual policies.</span></span> <span data-ttu-id="d2747-143">詳細については、[会社別または休暇プラン別の有給休暇](hr-leave-and-absence-accrue.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="d2747-143">For more information, see [Accrue leave per company or per leave plan](hr-leave-and-absence-accrue.md).</span></span>

## <a name="add-attachments-to-time-off-requests"></a><span data-ttu-id="d2747-144">添付ファイルを休暇申請に追加</span><span class="sxs-lookup"><span data-stu-id="d2747-144">Add attachments to time off requests</span></span>

<span data-ttu-id="d2747-145">承認済み休暇申請に添付ファイルを追加する機能は、現在の COVID-19 環境では非常に重要です。</span><span class="sxs-lookup"><span data-stu-id="d2747-145">The ability to add attachments to approved leave requests is critical in the current COVID-19 environment.</span></span> <span data-ttu-id="d2747-146">従業員はこれらの添付ファイルを追加できます。</span><span class="sxs-lookup"><span data-stu-id="d2747-146">Employees can now add these attachments.</span></span> <span data-ttu-id="d2747-147">また、休暇申請がどのように更新されるかについても、より深く理解することができます。</span><span class="sxs-lookup"><span data-stu-id="d2747-147">They also have more insight into how updates are made to leave requests.</span></span> <span data-ttu-id="d2747-148">詳細については、[既存の申請に添付ファイルを追加](hr-employee-self-service-request-time-off.md#add-an-attachment-to-an-existing-request) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="d2747-148">For more information, see [Add an attachment to an existing request](hr-employee-self-service-request-time-off.md#add-an-attachment-to-an-existing-request).</span></span>

## <a name="add-reason-code-to-accrual-suspensions"></a><span data-ttu-id="d2747-149">休暇付与の一時停止に理由コードが追加されました</span><span class="sxs-lookup"><span data-stu-id="d2747-149">Add reason code to accrual suspensions</span></span> 

<span data-ttu-id="d2747-150">見越計上の中断に理由コードが追加されました。</span><span class="sxs-lookup"><span data-stu-id="d2747-150">Reason codes have been added to the accrual suspension.</span></span>

## <a name="carry-forward-rules"></a><span data-ttu-id="d2747-151">繰越ルール</span><span class="sxs-lookup"><span data-stu-id="d2747-151">Carry forward rules</span></span> 

<span data-ttu-id="d2747-152">繰越調整を転送する繰越残日数に対して、繰越休暇タイプを指定できます。</span><span class="sxs-lookup"><span data-stu-id="d2747-152">You can specify a carry forward leave type for carry forward balances where carry forward adjustments are transferred.</span></span> <span data-ttu-id="d2747-153">たとえば、従業員が 10 日間繰り越す場合、その 10 日間に別の休暇タイプを選択できます。</span><span class="sxs-lookup"><span data-stu-id="d2747-153">For example, if an employee carries forward 10 days, you can pick a different leave type for those 10 days.</span></span> <span data-ttu-id="d2747-154">詳細については、[休暇および欠勤タイプのコンフィギュレーション](hr-leave-and-absence-types.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="d2747-154">For more information, see [Configure leave and absence types](hr-leave-and-absence-types.md).</span></span>

## <a name="suspend-leave-accrual-for-specified-leave-types"></a><span data-ttu-id="d2747-155">指定した休暇タイプに対する休暇付与の一時停止</span><span class="sxs-lookup"><span data-stu-id="d2747-155">Suspend leave accrual for specified leave types</span></span>

<span data-ttu-id="d2747-156">無給休暇で休暇申請を入力した従業員に対して、休暇の発生を停止するルールを作成することができます。</span><span class="sxs-lookup"><span data-stu-id="d2747-156">You can create a rule to suspend leave accruals for employees with leave requests entered for unpaid leave.</span></span> <span data-ttu-id="d2747-157">無給休暇のタイプを指定できますが、必須ではあります。</span><span class="sxs-lookup"><span data-stu-id="d2747-157">Unpaid leave can be a type, but doesn't have to be.</span></span> <span data-ttu-id="d2747-158">他の休暇種類に基づいて、任意の休暇を停止することができます。</span><span class="sxs-lookup"><span data-stu-id="d2747-158">You can suspend any leave based on another leave type.</span></span>

## <a name="dmf-entity-available-for-accrual-suspensions"></a><span data-ttu-id="d2747-159">DMF エンティティで休暇付与の一時停止が可能</span><span class="sxs-lookup"><span data-stu-id="d2747-159">DMF entity available for accrual suspensions</span></span> 

<span data-ttu-id="d2747-160">DMF エンティティが見越し計上の停止に使用できるようになりました 。</span><span class="sxs-lookup"><span data-stu-id="d2747-160">A DMF entity is now available for accrual suspensions.</span></span>

## <a name="coming-soon"></a><span data-ttu-id="d2747-161">間もなく公開</span><span class="sxs-lookup"><span data-stu-id="d2747-161">Coming soon</span></span>

## <a name="new-platform-capabilities"></a><span data-ttu-id="d2747-162">新しいプラットフォーム機能</span><span class="sxs-lookup"><span data-stu-id="d2747-162">New platform capabilities</span></span> 

<span data-ttu-id="d2747-163">個人用設定を使用すると、フィールドを必須にすることができます。</span><span class="sxs-lookup"><span data-stu-id="d2747-163">You'll be able to make fields mandatory by using personalization.</span></span> <span data-ttu-id="d2747-164">この機能を使用するには、**保存されているビュー** を有効にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="d2747-164">This feature will require you to enable **Saved views**.</span></span>

## <a name="configure-the-name-of-employee-self-service"></a><span data-ttu-id="d2747-165">従業員セルフ サービス名のコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="d2747-165">Configure the name of Employee self-service</span></span>

<span data-ttu-id="d2747-166">人事管理パラメータで新しいオプションが使用可能になり、従業員セルフ サービス ワークスペースの名前をセルフ サービスに更新します。</span><span class="sxs-lookup"><span data-stu-id="d2747-166">A new option will be available in Human Resources parameters to update the name of the Employee self service workspace to Self service.</span></span> 

## <a name="see-also"></a><span data-ttu-id="d2747-167">参照</span><span class="sxs-lookup"><span data-stu-id="d2747-167">See also</span></span>

[<span data-ttu-id="d2747-168">Human Resources の新機能および変更された機能</span><span class="sxs-lookup"><span data-stu-id="d2747-168">What's new or changed in Human Resources</span></span>](hr-admin-whats-new.md)</br>
[<span data-ttu-id="d2747-169">Dynamics 365 Human Resources 2019 のリリース ウェーブ 2 の概要</span><span class="sxs-lookup"><span data-stu-id="d2747-169">Overview of Dynamics 365 Human Resources 2019 release wave 2</span></span>](/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[<span data-ttu-id="d2747-170">更新プロセス</span><span class="sxs-lookup"><span data-stu-id="d2747-170">Update process</span></span>](hr-admin-setup-update-process.md)</br>
[<span data-ttu-id="d2747-171">機能の管理</span><span class="sxs-lookup"><span data-stu-id="d2747-171">Manage features</span></span>](hr-admin-manage-features.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]