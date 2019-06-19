---
title: Dynamics 365 for Talent (2019 年 5 月 13 日) の新機能および変更された機能
description: このトピックでは、Microsoft Dynamics 365 for Talent の新機能または変更された機能について説明します。
author: Darinkramer
manager: AnnBe
ms.date: 05/13/2019
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
ms.search.validFrom: 2019-05-13
ms.dyn365.ops.version: Talent
ms.openlocfilehash: dac453ee83492655b6681b9784af4712bf39fc2a
ms.sourcegitcommit: 2bbc0eeca6826c529fb729b82d16f287c1ce05bb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/16/2019
ms.locfileid: "1591505"
---
# <a name="whats-new-or-changed-in-dynamics-365-for-talent-may-13-2019"></a><span data-ttu-id="b7dff-103">Dynamics 365 for Talent (2019 年 5 月 13 日) の新機能および変更された機能</span><span class="sxs-lookup"><span data-stu-id="b7dff-103">What's new or changed in Dynamics 365 for Talent (May 13, 2019)</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="b7dff-104">このトピックでは、Dynamics 365 for Talent の新機能または変更された機能について説明します。</span><span class="sxs-lookup"><span data-stu-id="b7dff-104">This topic describes features that are either new or changed in Dynamics 365 for Talent.</span></span>

## <a name="coming-soon-in-attract"></a><span data-ttu-id="b7dff-105">Attract で間もなく公開</span><span class="sxs-lookup"><span data-stu-id="b7dff-105">Coming soon in Attract</span></span>

### <a name="job-approvals-on-home-page"></a><span data-ttu-id="b7dff-106">ホーム ページのジョブ承認</span><span class="sxs-lookup"><span data-stu-id="b7dff-106">Job approvals on home page</span></span>

<span data-ttu-id="b7dff-107">承認は、ダッシュボードの**承認**セクションに表示されます。</span><span class="sxs-lookup"><span data-stu-id="b7dff-107">Approvals appear in an **Approvals** section on the dashboard.</span></span> <span data-ttu-id="b7dff-108">承認者は**自分に割り当て済み**で自分の承認を確認できます。ここではジョブ ID、職位、他の承認者、および割り当て日が表示されます。</span><span class="sxs-lookup"><span data-stu-id="b7dff-108">Approvers can review their approvals under **Assigned to you**, which displays the job ID, title, other approvers, and date assigned.</span></span> <span data-ttu-id="b7dff-109">承認のジョブを送信するユーザーは、**ユーザーにより要求済**で自分のジョブを確認できます。ここでは送信したジョブをまだ承認する必要がある承認者を表示します。</span><span class="sxs-lookup"><span data-stu-id="b7dff-109">Users who submit a job for approval can review their jobs under **Requested by you**, which displays the approvers who still need to approve the submitted job.</span></span>

## <a name="changes-in-onboard"></a><span data-ttu-id="b7dff-110">Onboard の変更</span><span class="sxs-lookup"><span data-stu-id="b7dff-110">Changes in Onboard</span></span>

<span data-ttu-id="b7dff-111">今回のリリースには、Dynamics 365 Talent: Onboard のマイナーなバグ修正が含まれています。</span><span class="sxs-lookup"><span data-stu-id="b7dff-111">This release includes minor bug fixes for Dynamics 365 Talent: Onboard.</span></span>

## <a name="changes-in-core-hr"></a><span data-ttu-id="b7dff-112">Core HR の変更</span><span class="sxs-lookup"><span data-stu-id="b7dff-112">Changes in Core HR</span></span>

<span data-ttu-id="b7dff-113">このセクションに記載された変更は、ビルド番号 8.1.2297 に適用されます。</span><span class="sxs-lookup"><span data-stu-id="b7dff-113">Changes described in this section apply to build number 8.1.2297.</span></span> <span data-ttu-id="b7dff-114">ヘッダーにあるかっこ内の数字は、Microsoft Dynamics Lifecycle Services (LCS) のサポート番号を参照していることがあります。</span><span class="sxs-lookup"><span data-stu-id="b7dff-114">The numbers in parentheses in some headings refer to support numbers in Microsoft Dynamics Lifecycle Services (LCS).</span></span>

### <a name="indicate-instance-type-when-provisioning-talent"></a><span data-ttu-id="b7dff-115">Talent のプロビジョニング時に、インスタンス タイプを示す</span><span class="sxs-lookup"><span data-stu-id="b7dff-115">Indicate instance type when provisioning Talent</span></span>

<span data-ttu-id="b7dff-116">Talent の新しいインスタンスのプロビジョニング時に、インスタンス タイプが**実稼働**か**サンドボックス**であるかを示すことができ、新しい機能を事前にテストできるようになります。</span><span class="sxs-lookup"><span data-stu-id="b7dff-116">When provisioning a new instance of Talent, you can indicate whether the instance type is **Production** or **Sandbox**, which allows for early testing of new features.</span></span> <span data-ttu-id="b7dff-117">既存の Talent のインスタンスすべては、**実稼働**インスタンス タイプに更新されます。</span><span class="sxs-lookup"><span data-stu-id="b7dff-117">All existing Talent instances will be updated to the **Production** instance type.</span></span> <span data-ttu-id="b7dff-118">既存のインスタンスのいずれかを**サンドボックス** インスタンス タイプに更新する場合は、変更要求を開始するよう [サポート](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/talent-support) に連絡してください。</span><span class="sxs-lookup"><span data-stu-id="b7dff-118">If you want one of your existing instances to be updated to the **Sandbox** instance type, please contact [Support](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/talent-support) to initiate the change request.</span></span>

### <a name="common-data-service-entity-support-for-custom-fields"></a><span data-ttu-id="b7dff-119">カスタム フィールドに対する Common Data Service エンティティのサポート</span><span class="sxs-lookup"><span data-stu-id="b7dff-119">Common Data Service entity support for custom fields</span></span>

<span data-ttu-id="b7dff-120">今週のリリースでは、次の Common Data Service エンティティでカスタム フィールドがサポートされるようになりました。雇用、給付金計算頻度、給付金の計算レート、作業カレンダーの休日、および ID タイプです。</span><span class="sxs-lookup"><span data-stu-id="b7dff-120">In this week's release, the following Common Data Service entities now support custom fields: Employment, Benefit calc frequency, Benefit calc rate, Work calendar holiday, and Identification type.</span></span>

### <a name="common-data-service-integration-page"></a><span data-ttu-id="b7dff-121">Common Data Service 統合ページ</span><span class="sxs-lookup"><span data-stu-id="b7dff-121">Common Data Service integration page</span></span>

<span data-ttu-id="b7dff-122">このリリースは、**システム管理 > リンク > 統合 > Common Data Service コンフィギュレーション**で新しいオプションを提供します。</span><span class="sxs-lookup"><span data-stu-id="b7dff-122">This release provides a new option in **System Administration > Links > Integrations > Common Data Service configuration**.</span></span> <span data-ttu-id="b7dff-123">**Common Data Service コンフィギュレーション** オプションを使用すると、管理者またはデータ管理者は、Common Data Service を使用してある程度の柔軟性と洞察を得ることができます。</span><span class="sxs-lookup"><span data-stu-id="b7dff-123">The **Common Data Service configuration** option allows an administrator or data management administrator some flexibility and insights with the Common Data Service.</span></span> <span data-ttu-id="b7dff-124">このオプションにより、Talent インスタンスとの Common Data Service 統合を有効または無効にでき、Talent インスタンスと Common Data Service 間の同期の詳細を表示できます。</span><span class="sxs-lookup"><span data-stu-id="b7dff-124">With this option, you can enable or disable Common Data Service integration with a Talent instance and view the sync details between the Talent instance and the Common Data Service.</span></span>

### <a name="import-performance-data-with-final-employee-rating-316710"></a><span data-ttu-id="b7dff-125">最終従業員評価 (316710) でパフォーマンス データをインポートします</span><span class="sxs-lookup"><span data-stu-id="b7dff-125">Import performance data with final employee rating (316710)</span></span>

<span data-ttu-id="b7dff-126">このリリースでは、過去の従業員評価データをインポートできます。</span><span class="sxs-lookup"><span data-stu-id="b7dff-126">In this release, you can import historical employee rating data.</span></span> <span data-ttu-id="b7dff-127">**FinalEmployeeRatingId** フィールドに書き込み許可が与えられます。</span><span class="sxs-lookup"><span data-stu-id="b7dff-127">The **FinalEmployeeRatingId** field now has write permission.</span></span>

### <a name="cant-create-worker-address-in-common-data-service-and-sync-it-with-talent-317555"></a><span data-ttu-id="b7dff-128">作業者の住所を Common Data Service で作成して、Talent と同期することはできません (317555)</span><span class="sxs-lookup"><span data-stu-id="b7dff-128">Can't create Worker address in Common Data Service and sync it with Talent (317555)</span></span>

<span data-ttu-id="b7dff-129">この変更により、Common Data Service で作成された住所データと Talent との同期が可能になります。</span><span class="sxs-lookup"><span data-stu-id="b7dff-129">This change allows address data created in Common Data Service to sync with Talent.</span></span>

## <a name="in-preview"></a><span data-ttu-id="b7dff-130">プレビュー</span><span class="sxs-lookup"><span data-stu-id="b7dff-130">In preview</span></span>

### <a name="new-page-to-validate-position-hierarchy-data"></a><span data-ttu-id="b7dff-131">職位階層データを検証する新しいページ</span><span class="sxs-lookup"><span data-stu-id="b7dff-131">New page to validate position hierarchy data</span></span>

<span data-ttu-id="b7dff-132">人事管理 (HR) および管理者は、誤ってインポートされた循環参照に対して、管理階層を検証できます。</span><span class="sxs-lookup"><span data-stu-id="b7dff-132">Human resources (HR) and administrators can validate the managerial hierarchy for any circular references that might have been inadvertently imported.</span></span> <span data-ttu-id="b7dff-133">この新しいページは、**組織管理 > リンク > 職位 > 職位階層の検証**からアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="b7dff-133">You can access this new page from **Organizational administration > Links > Positions > Position hierarchy validation**.</span></span>

### <a name="specify-reason-codes-on-leave-types"></a><span data-ttu-id="b7dff-134">休暇タイプの理由コードの指定</span><span class="sxs-lookup"><span data-stu-id="b7dff-134">Specify reason codes on leave types</span></span>

<span data-ttu-id="b7dff-135">組織は、休暇申請に関する追加情報を要求する場合があります。</span><span class="sxs-lookup"><span data-stu-id="b7dff-135">Organizations might require additional information about time-off requests.</span></span> <span data-ttu-id="b7dff-136">休暇タイプに理由コードを指定し、従業員は休暇申請で理由コードを選択できるようになりました。</span><span class="sxs-lookup"><span data-stu-id="b7dff-136">You can now specify reason codes for leave types and let employees select a reason code on their time-off requests.</span></span>

### <a name="require-reason-codes-for-specific-leave-types-on-time-off-requests"></a><span data-ttu-id="b7dff-137">休暇申請で固有の休暇タイプについては理由コードが必要</span><span class="sxs-lookup"><span data-stu-id="b7dff-137">Require reason codes for specific leave types on time-off requests</span></span>

<span data-ttu-id="b7dff-138">従業員が休暇申請を送信するときに、組織は特定の休暇タイプに理由コードを要求することがあります。</span><span class="sxs-lookup"><span data-stu-id="b7dff-138">Organizations might require reason codes for specific leave types when employees submit time-off requests.</span></span> <span data-ttu-id="b7dff-139">この要件は、会社のポリシーや規制要件が原因であることがあります。</span><span class="sxs-lookup"><span data-stu-id="b7dff-139">This requirement might exist because of company policy or regulatory requirements.</span></span> <span data-ttu-id="b7dff-140">どの休暇タイプに理由コードが必要かを指定できます。また、従業員に休暇申請で休暇タイプに理由コードを指定するように要求できます。</span><span class="sxs-lookup"><span data-stu-id="b7dff-140">You can specify which leave types require a reason code, and you can require that employees provide a reason code for the leave type on their time-off requests.</span></span>

### <a name="provide-a-leave-and-absence-transaction-list-for-hr"></a><span data-ttu-id="b7dff-141">HR の休暇および欠勤トランザクション リストを提供します</span><span class="sxs-lookup"><span data-stu-id="b7dff-141">Provide a leave and absence transaction list for HR</span></span>

<span data-ttu-id="b7dff-142">従業員の休暇を追跡し、どのように計算するかを理解する機能は、HR が従業員の質問に答えるのに役立つだけでなく、従業員に正確な休暇を付与することにも役立ちます。</span><span class="sxs-lookup"><span data-stu-id="b7dff-142">The ability to track employee time off and understand how time off is calculated not only helps HR answer employee questions, but also helps ensure accurate time-off awards for employees.</span></span> <span data-ttu-id="b7dff-143">HR において、トランザクション (交付、見越、調整、および要求) の表示が新しくなり、HR スタッフは休暇残高の背後にある理由を確認することができるようになりました。</span><span class="sxs-lookup"><span data-stu-id="b7dff-143">HR now has a new view into the transactions (grants, accruals, adjustments, and requests), so that HR staff can view the reasons behind time-off balances.</span></span>
