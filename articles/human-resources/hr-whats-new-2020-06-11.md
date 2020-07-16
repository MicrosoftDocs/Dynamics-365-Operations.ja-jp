---
title: Dynamics 365 Human Resources の新機能または変更された機能 (2020 年 6 月 11 日)
description: このトピックでは、Microsoft Dynamics 365 Human Resources の新機能または変更された機能について説明します。
author: Darinkramer
manager: AnnBe
ms.date: 6/16/2020
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
ms.search.validFrom: 2020-06-11
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 39f18dc92fb01f9a0437f4166c0f08f8d6b1b81b
ms.sourcegitcommit: 218e22014a964b8b52fc0152e355b07b0b84ae2c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/16/2020
ms.locfileid: "3456623"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-june-11-2020"></a><span data-ttu-id="9b2be-103">Dynamics 365 Human Resources の新機能または変更された機能 (2020 年 6 月 11 日)</span><span class="sxs-lookup"><span data-stu-id="9b2be-103">What's new or changed in Dynamics 365 Human Resources (June 11, 2020)</span></span>

<span data-ttu-id="9b2be-104">この記事では、Dynamics 365 Human Resources の新機能および変更された機能について説明します。</span><span class="sxs-lookup"><span data-stu-id="9b2be-104">This article describes features that are either new or changed in Dynamics 365 Human Resources.</span></span> <span data-ttu-id="9b2be-105">変更は、ビルド番号 8.1.3316 に適用されます。</span><span class="sxs-lookup"><span data-stu-id="9b2be-105">Changes apply to build number 8.1.3316.</span></span> <span data-ttu-id="9b2be-106">ヘッダーにあるかっこ内の数字は、参照用の LCS のサポート番号を参照していることがあります。</span><span class="sxs-lookup"><span data-stu-id="9b2be-106">The numbers in parentheses in some headings refer to LCS support numbers for reference.</span></span>

## <a name="streamlined-employee-form-sometimes-causes-child-form-close-x-buttons-to-stop-working-442369"></a><span data-ttu-id="9b2be-107">合理化された従業員フォームにより、子フォームの閉じる (X) ボタンが機能しなくなることがある (442369)</span><span class="sxs-lookup"><span data-stu-id="9b2be-107">Streamlined employee form sometimes causes child form close (X) buttons to stop working (442369)</span></span>

<span data-ttu-id="9b2be-108">新しい **作業者** フォームが有効になっていると、閉じる (**X**) ボタンが子フォームで機能しないことがありました。</span><span class="sxs-lookup"><span data-stu-id="9b2be-108">When the new **Worker** form was enabled, the close (**X**) button occasionally didn't work on child forms.</span></span> <span data-ttu-id="9b2be-109">この問題は断続的でした。</span><span class="sxs-lookup"><span data-stu-id="9b2be-109">This problem was intermittent.</span></span> <span data-ttu-id="9b2be-110">離れて戻ってきた後に、フォームを開じることができます。</span><span class="sxs-lookup"><span data-stu-id="9b2be-110">You could close the form after leaving and coming back to it.</span></span> <span data-ttu-id="9b2be-111">たとえば、左側のメニュー項目を選択し、**作業者** フォームに戻ってから閉じることができます。</span><span class="sxs-lookup"><span data-stu-id="9b2be-111">For example, you could select a menu item on the left, and navigate back to the **Worker** form, and then close it.</span></span> <span data-ttu-id="9b2be-112">今週のリリースでは、この問題が修正されています。</span><span class="sxs-lookup"><span data-stu-id="9b2be-112">This week's release fixes this problem.</span></span> 

## <a name="the-worker-personal-contact-person-entity-doesnt-export-personal-contacts-with-a-parent-relationship-type"></a><span data-ttu-id="9b2be-113">作業者の個人連絡担当者エンティティが、親の関係タイプを持つ個人連絡先をエクスポートしない</span><span class="sxs-lookup"><span data-stu-id="9b2be-113">The Worker personal contact person entity doesn't export personal contacts with a parent relationship type</span></span>

<span data-ttu-id="9b2be-114">このリリースでは、**作業者の個人連絡担当者** エンティティが、すべての関係タイプをエクスポートします。</span><span class="sxs-lookup"><span data-stu-id="9b2be-114">With this release, the **Worker personal contact person** entity exports all relationship types.</span></span>

## <a name="the-hcmpositionworkerassignmentv2entity-should-be-part-of-the-ceridian-payroll-integration-package-by-default-448506"></a><span data-ttu-id="9b2be-115">HcmPositionWorkerAssignmentV2Entity は、既定で Ceridian 給与統合パッケージの一部である必要があります (448506)</span><span class="sxs-lookup"><span data-stu-id="9b2be-115">The HcmPositionWorkerAssignmentV2Entity should be part of the Ceridian payroll integration package by default (448506)</span></span>

<span data-ttu-id="9b2be-116">この変更により、**HcmPositionWorkerAssignmentV2Entity** が Ceridian 給与統合パッケージに含まれるようになりました。</span><span class="sxs-lookup"><span data-stu-id="9b2be-116">With this change, the **HcmPositionWorkerAssignmentV2Entity** is included in the Ceridian payroll integration package.</span></span>

## <a name="in-preview"></a><span data-ttu-id="9b2be-117">プレビュー</span><span class="sxs-lookup"><span data-stu-id="9b2be-117">In preview</span></span>

## <a name="database-logging"></a><span data-ttu-id="9b2be-118">データベースのログ</span><span class="sxs-lookup"><span data-stu-id="9b2be-118">Database logging</span></span>

<span data-ttu-id="9b2be-119">データベース ログ機能を使用すると、監視するテーブルとフィールドを決定できます。</span><span class="sxs-lookup"><span data-stu-id="9b2be-119">The database logging feature allows you to determine which tables and fields to monitor.</span></span> <span data-ttu-id="9b2be-120">また、Change Tracking を起動するイベントを決定することもできます。</span><span class="sxs-lookup"><span data-stu-id="9b2be-120">It also lets you determine the events that should trigger change tracking.</span></span> <span data-ttu-id="9b2be-121">これらの変更を時間の経過と共に確認するには、データベースのログ機能を使用します。</span><span class="sxs-lookup"><span data-stu-id="9b2be-121">You use database logging capabilities to see these changes over time.</span></span> <span data-ttu-id="9b2be-122">詳細については、[データベース ログの構成と管理](hr-admin-database-logging.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="9b2be-122">For more information, see [Configure and manage database logging](hr-admin-database-logging.md).</span></span>

## <a name="human-resources-application-in-teams"></a><span data-ttu-id="9b2be-123">Teams の Human Resources アプリケーション</span><span class="sxs-lookup"><span data-stu-id="9b2be-123">Human Resources application in Teams</span></span>

<span data-ttu-id="9b2be-124">従業員は、Microsoft Teams 内で休暇の表示および申請ができます。</span><span class="sxs-lookup"><span data-stu-id="9b2be-124">Employees can view and request time away from work within Microsoft Teams.</span></span> <span data-ttu-id="9b2be-125">ボットと対話して、休暇申請を作成できます。</span><span class="sxs-lookup"><span data-stu-id="9b2be-125">They can interact with a bot to create leave requests.</span></span> <span data-ttu-id="9b2be-126">詳細については、[Teams の Human Resources アプリ](https://go.microsoft.com/fwlink/?linkid=2127841) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="9b2be-126">For more information, see [Human Resources app in Teams](https://go.microsoft.com/fwlink/?linkid=2127841).</span></span> 

## <a name="data-management-framework-dmf-entities-for-benefits-management"></a><span data-ttu-id="9b2be-127">福利厚生管理のためのデータ管理フレームワーク (DMF) エンティティ</span><span class="sxs-lookup"><span data-stu-id="9b2be-127">Data management framework (DMF) entities for Benefits management</span></span>
 
<span data-ttu-id="9b2be-128">福利厚生管理エンティティはリリースされてます。</span><span class="sxs-lookup"><span data-stu-id="9b2be-128">Benefits management entities are releasing.</span></span> <span data-ttu-id="9b2be-129">DMF エンティティを使用すると、データをインポートおよびエクスポートして、福利厚生管理を簡単に構成できます。</span><span class="sxs-lookup"><span data-stu-id="9b2be-129">DMF entities allow you to import and export data to easily configure benefits management.</span></span> <span data-ttu-id="9b2be-130">福利厚生管理テンプレートは、データの移動に使用できます。</span><span class="sxs-lookup"><span data-stu-id="9b2be-130">A Benefits management template will be available to move data.</span></span> <span data-ttu-id="9b2be-131">テンプレートは、データの依存関係を考慮してデータを順次エクスポートおよびインポートします。</span><span class="sxs-lookup"><span data-stu-id="9b2be-131">The template exports and imports the data sequentially to respect data dependencies.</span></span>

## <a name="buy-and-sell-leave"></a><span data-ttu-id="9b2be-132">休暇の売買</span><span class="sxs-lookup"><span data-stu-id="9b2be-132">Buy and sell leave</span></span> 

<span data-ttu-id="9b2be-133">一部の組織では、従業員が休暇を購入または売却できるという利点があります。</span><span class="sxs-lookup"><span data-stu-id="9b2be-133">Some organizations provide a benefit that allows employees to buy or sell their leave.</span></span> <span data-ttu-id="9b2be-134">このプロセスは、多くの場合、手動で管理します。</span><span class="sxs-lookup"><span data-stu-id="9b2be-134">This process is often managed manually.</span></span> <span data-ttu-id="9b2be-135">この機能により、人事部門のポリシーと申請の管理を自動化します。</span><span class="sxs-lookup"><span data-stu-id="9b2be-135">This feature automates managing policies and requests for the HR department.</span></span> <span data-ttu-id="9b2be-136">休暇管理プロセスを合理化し、ミスをなくすことができます。</span><span class="sxs-lookup"><span data-stu-id="9b2be-136">It streamlines the leave management process and helps eliminate mistakes.</span></span> <span data-ttu-id="9b2be-137">詳細については、以下を参照してください。</span><span class="sxs-lookup"><span data-stu-id="9b2be-137">For more information, see:</span></span>

- [<span data-ttu-id="9b2be-138">休暇の売買ポリシーの管理</span><span class="sxs-lookup"><span data-stu-id="9b2be-138">Manage buy and sell leave policies</span></span>](hr-leave-and-absence-manage-buy-and-sell-leave-policies.md)
- [<span data-ttu-id="9b2be-139">休暇の売買</span><span class="sxs-lookup"><span data-stu-id="9b2be-139">Buy and sell leave</span></span>](hr-employee-self-service-buy-sell-leave.md)

## <a name="leave-accrual-for-a-single-company-or-single-plan"></a><span data-ttu-id="9b2be-140">1 社または 1 プランの有給休暇</span><span class="sxs-lookup"><span data-stu-id="9b2be-140">Leave accrual for a single company or single plan</span></span>

<span data-ttu-id="9b2be-141">顧客は、1 社または 1 休暇および不就業プランの有給休暇を処理できます。</span><span class="sxs-lookup"><span data-stu-id="9b2be-141">Customers can process accruals for a single company or a single leave and absence plan.</span></span> <span data-ttu-id="9b2be-142">この機能により、異なる休暇年数または有給休暇ポリシーを持つ顧客のために有給休暇プロセスを明確にします。</span><span class="sxs-lookup"><span data-stu-id="9b2be-142">This ability provides clarity into the accrual process for customers with different leave years or leave accrual policies.</span></span> <span data-ttu-id="9b2be-143">詳細については、[会社別または休暇プラン別の有給休暇](hr-leave-and-absence-accrue.md#accrue-leave-per-company-or-per-leave-plan) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="9b2be-143">For more information, see [Accrue leave per company or per leave plan](hr-leave-and-absence-accrue.md#accrue-leave-per-company-or-per-leave-plan).</span></span>

## <a name="add-attachments-to-time-off-requests"></a><span data-ttu-id="9b2be-144">添付ファイルを休暇申請に追加</span><span class="sxs-lookup"><span data-stu-id="9b2be-144">Add attachments to time off requests</span></span>

<span data-ttu-id="9b2be-145">承認済み休暇申請に添付ファイルを追加する機能は、現在の COVID-19 環境では非常に重要です。</span><span class="sxs-lookup"><span data-stu-id="9b2be-145">The ability to add attachments to approved leave requests is critical in the current COVID-19 environment.</span></span> <span data-ttu-id="9b2be-146">従業員はこれらの添付ファイルを追加できます。</span><span class="sxs-lookup"><span data-stu-id="9b2be-146">Employees can now add these attachments.</span></span> <span data-ttu-id="9b2be-147">また、休暇申請がどのように更新されるかについても、より深く理解することができます。</span><span class="sxs-lookup"><span data-stu-id="9b2be-147">They also have more insight into how updates are made to leave requests.</span></span> <span data-ttu-id="9b2be-148">詳細については、[既存の申請に添付ファイルを追加](hr-employee-self-service-request-time-off.md#add-an-attachment-to-an-existing-request) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="9b2be-148">For more information, see [Add an attachment to an existing request](hr-employee-self-service-request-time-off.md#add-an-attachment-to-an-existing-request).</span></span>

## <a name="add-reason-code-to-accrual-suspensions"></a><span data-ttu-id="9b2be-149">休暇付与の一時停止に理由コードが追加されました</span><span class="sxs-lookup"><span data-stu-id="9b2be-149">Add reason code to accrual suspensions</span></span> 

<span data-ttu-id="9b2be-150">見越計上の中断に理由コードが追加されました。</span><span class="sxs-lookup"><span data-stu-id="9b2be-150">Reason codes have been added to the accrual suspension.</span></span>

## <a name="carry-forward-rules"></a><span data-ttu-id="9b2be-151">繰越ルール</span><span class="sxs-lookup"><span data-stu-id="9b2be-151">Carry forward rules</span></span> 

<span data-ttu-id="9b2be-152">繰越調整を転送する繰越残日数に対して、繰越休暇タイプを指定できます。</span><span class="sxs-lookup"><span data-stu-id="9b2be-152">You can specify a carry forward leave type for carry forward balances where carry forward adjustments are transferred.</span></span> <span data-ttu-id="9b2be-153">たとえば、従業員が 10 日間繰り越す場合、その 10 日間に別の休暇タイプを選択できます。</span><span class="sxs-lookup"><span data-stu-id="9b2be-153">For example, if an employee carries forward 10 days, you can pick a different leave type for those 10 days.</span></span> <span data-ttu-id="9b2be-154">詳細については、[休暇および欠勤タイプのコンフィギュレーション](hr-leave-and-absence-types.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="9b2be-154">For more information, see [Configure leave and absence types](hr-leave-and-absence-types.md).</span></span>

## <a name="suspend-leave-accrual-for-specified-leave-types"></a><span data-ttu-id="9b2be-155">指定した休暇タイプに対する休暇付与の一時停止</span><span class="sxs-lookup"><span data-stu-id="9b2be-155">Suspend leave accrual for specified leave types</span></span>

<span data-ttu-id="9b2be-156">無給休暇で休暇申請を入力した従業員に対して、休暇の発生を停止するルールを作成することができます。</span><span class="sxs-lookup"><span data-stu-id="9b2be-156">You can create a rule to suspend leave accruals for employees with leave requests entered for unpaid leave.</span></span> <span data-ttu-id="9b2be-157">無給休暇のタイプを指定できますが、必須ではあります。</span><span class="sxs-lookup"><span data-stu-id="9b2be-157">Unpaid leave can be a type, but doesn't have to be.</span></span> <span data-ttu-id="9b2be-158">他の休暇種類に基づいて、任意の休暇を停止することができます。</span><span class="sxs-lookup"><span data-stu-id="9b2be-158">You can suspend any leave based on another leave type.</span></span>

## <a name="dmf-entity-available-for-accrual-suspensions"></a><span data-ttu-id="9b2be-159">DMF エンティティで休暇付与の一時停止が可能</span><span class="sxs-lookup"><span data-stu-id="9b2be-159">DMF entity available for accrual suspensions</span></span> 

<span data-ttu-id="9b2be-160">DMF エンティティが見越し計上の停止に使用できるようになりました 。</span><span class="sxs-lookup"><span data-stu-id="9b2be-160">A DMF entity is now available for accrual suspensions.</span></span>

## <a name="coming-soon"></a><span data-ttu-id="9b2be-161">間もなく公開</span><span class="sxs-lookup"><span data-stu-id="9b2be-161">Coming soon</span></span>

## <a name="new-platform-capabilities"></a><span data-ttu-id="9b2be-162">新しいプラットフォーム機能</span><span class="sxs-lookup"><span data-stu-id="9b2be-162">New platform capabilities</span></span> 

<span data-ttu-id="9b2be-163">個人用設定を使用すると、フィールドを必須にすることができます。</span><span class="sxs-lookup"><span data-stu-id="9b2be-163">You'll be able to make fields mandatory by using personalization.</span></span> <span data-ttu-id="9b2be-164">この機能を使用するには、**保存されているビュー** を有効にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="9b2be-164">This feature will require you to enable **Saved views**.</span></span>

## <a name="configure-the-name-of-employee-self-service"></a><span data-ttu-id="9b2be-165">従業員セルフ サービス名のコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="9b2be-165">Configure the name of Employee self-service</span></span>

<span data-ttu-id="9b2be-166">人事管理パラメータで新しいオプションが使用可能になり、従業員セルフ サービス ワークスペースの名前をセルフ サービスに更新します。</span><span class="sxs-lookup"><span data-stu-id="9b2be-166">A new option will be available in Human Resources parameters to update the name of the Employee self service workspace to Self service.</span></span> 