---
title: Dynamics 365 Talent (2019 年 10 月 8 日) の新機能および変更された機能
description: このトピックでは、Microsoft Dynamics 365 Talent の新機能または変更された機能について説明します。
author: Darinkramer
manager: AnnBe
ms.date: 10/08/2019
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
ms.search.validFrom: 2019-10-08
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 159320dcbdf257862378b347172ef71832e293dc
ms.sourcegitcommit: deb87e518a151d8bb084891851a39758938a96e4
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/15/2019
ms.locfileid: "2626065"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-october-8-2019"></a><span data-ttu-id="6200d-103">Dynamics 365 Talent (2019 年 10 月 8 日) の新機能および変更された機能</span><span class="sxs-lookup"><span data-stu-id="6200d-103">What's new or changed in Dynamics 365 Talent (October 8, 2019)</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="6200d-104">このトピックでは、Microsoft Dynamics 365 Talent の新機能または変更された機能について説明します。</span><span class="sxs-lookup"><span data-stu-id="6200d-104">This topic describes features that are either new or changed in Microsoft Dynamics 365 Talent.</span></span>

## <a name="changes-in-attract"></a><span data-ttu-id="6200d-105">Attract の変更</span><span class="sxs-lookup"><span data-stu-id="6200d-105">Changes in Attract</span></span>

<span data-ttu-id="6200d-106">今回のリリースには、Dynamics 365 Talent: Attract のマイナーなバグ修正が含まれています。</span><span class="sxs-lookup"><span data-stu-id="6200d-106">This release includes minor bug fixes for Dynamics 365 Talent: Attract.</span></span>

## <a name="changes-in-onboard"></a><span data-ttu-id="6200d-107">Onboard の変更</span><span class="sxs-lookup"><span data-stu-id="6200d-107">Changes in Onboard</span></span>

<span data-ttu-id="6200d-108">今回のリリースには、Dynamics 365 Talent: Onboard のマイナーなバグ修正が含まれています。</span><span class="sxs-lookup"><span data-stu-id="6200d-108">This release includes minor bug fixes for Dynamics 365 Talent: Onboard.</span></span>

## <a name="changes-in-core-hr"></a><span data-ttu-id="6200d-109">Core HR の変更</span><span class="sxs-lookup"><span data-stu-id="6200d-109">Changes in Core HR</span></span>

<span data-ttu-id="6200d-110">このセクションに記載された変更は、ビルド番号 8.1.2542 に適用されます。</span><span class="sxs-lookup"><span data-stu-id="6200d-110">The changes that are described in this section apply to build number 8.1.2542.</span></span> <span data-ttu-id="6200d-111">ヘッダーにあるかっこ内の数字は、Microsoft Dynamics Lifecycle Services (LCS) のサポート番号を参照していることがあります。</span><span class="sxs-lookup"><span data-stu-id="6200d-111">The numbers in parentheses in some headings refer to support numbers in Microsoft Dynamics Lifecycle Services (LCS).</span></span>

### <a name="removal-of-benefits-open-enrollment-from-public-preview"></a><span data-ttu-id="6200d-112">パブリック プレビューからの福利厚生の自由登録の削除</span><span class="sxs-lookup"><span data-stu-id="6200d-112">Removal of benefits open enrollment from public preview</span></span>

<span data-ttu-id="6200d-113">Microsoft では、[Core HR ドライブのオペレーショナル エクセレンスにおける戦略的投資](https://cloudblogs.microsoft.com/dynamics365/bdm/2019/10/02/strategic-investments-in-core-hr-drive-operational-excellence/)ブログ投稿におけるお知らせと共に、2019 年 10 月 18 日のパブリック プレビューから自由登録機能を削除しています。</span><span class="sxs-lookup"><span data-stu-id="6200d-113">In conjunction with our announcement in the [Strategic investments in core HR drive operational excellence](https://cloudblogs.microsoft.com/dynamics365/bdm/2019/10/02/strategic-investments-in-core-hr-drive-operational-excellence/) blog post, Microsoft is removing the benefits open enrollment feature from public preview on October 18, 2019.</span></span> <span data-ttu-id="6200d-114">代わりに、新しい機能が将来リリースされます。</span><span class="sxs-lookup"><span data-stu-id="6200d-114">Instead, new functionality will be released in the future.</span></span> <span data-ttu-id="6200d-115">現在パブリック プレビューにある福利厚生の自由登録機能は、運用上の用途ではサポートされません。</span><span class="sxs-lookup"><span data-stu-id="6200d-115">Production use of the benefits open enrollment feature that is currently in public preview won't be supported.</span></span> 

### <a name="common-data-service-integration-is-now-turned-off-by-default-on-new-provisions-343675"></a><span data-ttu-id="6200d-116">Common Data Service 統合は、新しいプロビジョニングで既定でオフになりました (343675)</span><span class="sxs-lookup"><span data-stu-id="6200d-116">Common Data Service integration is now turned off by default on new provisions (343675)</span></span>
 
<span data-ttu-id="6200d-117">新しい環境が準備されると Common Data Service 統合はオフになります。</span><span class="sxs-lookup"><span data-stu-id="6200d-117">When new environments are provisioned, Common Data Service integration is now turned off.</span></span> <span data-ttu-id="6200d-118">詳細については、[Common Data Service 統合のコンフィギュレーション](hr-common-data-service-integration.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6200d-118">For more information, see [Configure Common Data Service integration](hr-common-data-service-integration.md).</span></span>

### <a name="streamlined-employee-entry-and-navigation"></a><span data-ttu-id="6200d-119">合理化された従業員の入力とナビゲーション</span><span class="sxs-lookup"><span data-stu-id="6200d-119">Streamlined employee entry and navigation</span></span>

<span data-ttu-id="6200d-120">従業員の入力とナビゲーションの機能をすべての環境で使用できるようになりました。</span><span class="sxs-lookup"><span data-stu-id="6200d-120">Functionality for employee entry and navigation is now available in all environments.</span></span> <span data-ttu-id="6200d-121">この機能を有効にするには、**システム管理 \> リンク \> 設定 \> システム パラメーター \> プレビュー機能**に移動し、**拡張された作業者フォームとナビゲーション**を選択します。</span><span class="sxs-lookup"><span data-stu-id="6200d-121">To turn on this feature, go to **System administration \> Links \> Setup \> System parameters \> Preview features**, and select **Enhanced worker form and navigation**.</span></span> <span data-ttu-id="6200d-122">この機能は、すべてのユーザーに対して有効になります。</span><span class="sxs-lookup"><span data-stu-id="6200d-122">The feature is then turned for all users.</span></span> <span data-ttu-id="6200d-123">このオプションはいつでもオフにすることができます。</span><span class="sxs-lookup"><span data-stu-id="6200d-123">You can turn this option off at any time.</span></span>

<span data-ttu-id="6200d-124">詳細については、Dynamics 365: 2019 リリース ウェーブ 2 プラン[合理化された従業員のデータ入力](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-talent/streamlined-employee-data-entry)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6200d-124">For more information, see [Streamlined employee data entry](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-talent/streamlined-employee-data-entry) in the Dynamics 365: 2019 release wave 2 plan.</span></span>

### <a name="issue-attract-and-onboard-create-inactive-workers-in-core-hr-380517"></a><span data-ttu-id="6200d-125">問題: Attract および Onboard により、無効な作業者が Core HR に作成される (380517)</span><span class="sxs-lookup"><span data-stu-id="6200d-125">Issue: Attract and Onboard create inactive workers in Core HR (380517)</span></span>

<span data-ttu-id="6200d-126">今週のリリースでは、Attract および Onboard により無効な作業者が Core HR に作成されるという問題が修正されます。</span><span class="sxs-lookup"><span data-stu-id="6200d-126">This week's release corrects an issue where Attract and Onboard create inactive workers in Core HR.</span></span>

### <a name="issue-the-workflow-fails-when-the-manager-is-signed-in-to-another-company-while-terminating-an-employee-346852"></a><span data-ttu-id="6200d-127">問題: 従業員の退職に際してマネージャーが別の会社にサインインすると、ワークフローが失敗する (346852)</span><span class="sxs-lookup"><span data-stu-id="6200d-127">Issue: The workflow fails when the manager is signed in to another company while terminating an employee (346852)</span></span>

<span data-ttu-id="6200d-128">マネージャーがサインインしている法人に基づいてワークフローが失敗することはなくなりました。</span><span class="sxs-lookup"><span data-stu-id="6200d-128">The workflow no longer fails based on the legal entity that the manager is signed in to.</span></span>

### <a name="issue-missing-information-on-hcmonboardingworkerchecklisttaskentity-349591"></a><span data-ttu-id="6200d-129">問題: HcmOnboardingWorkerChecklistTaskEntity に関する情報が不足している (349591)</span><span class="sxs-lookup"><span data-stu-id="6200d-129">Issue: Missing information on HcmOnboardingWorkerChecklistTaskEntity (349591)</span></span>

<span data-ttu-id="6200d-130">このリリースには、**HcmOnboardingWorkerChecklistTaskEntity** に関する追加情報が含まれています。</span><span class="sxs-lookup"><span data-stu-id="6200d-130">This release includes additional information on **HcmOnboardingWorkerChecklistTaskEntity**.</span></span> <span data-ttu-id="6200d-131">次にいくつか例を挙げます。</span><span class="sxs-lookup"><span data-stu-id="6200d-131">Here are some examples:</span></span>

- <span data-ttu-id="6200d-132">**グループ名** 割り当てられたタイプが**グループ**の場合</span><span class="sxs-lookup"><span data-stu-id="6200d-132">**Group name** when the assigned type is **group**</span></span>
- <span data-ttu-id="6200d-133">**従業員名** 割り当てられたタイプが**従業員**の場合</span><span class="sxs-lookup"><span data-stu-id="6200d-133">**Employee name** when the assigned type is **employee**</span></span>
- <span data-ttu-id="6200d-134">**マネージャー名** 割り当てられたタイプが**マネージャー**の場合</span><span class="sxs-lookup"><span data-stu-id="6200d-134">**Manager name** when the assigned type is **manager**</span></span>

### <a name="issue-entities-arent-listed-in-alphabetical-order-in-common-data-service-administration-377414"></a><span data-ttu-id="6200d-135">問題: Common Data Service 管理においてエンティティがアルファベット順にリストされていない (377414)</span><span class="sxs-lookup"><span data-stu-id="6200d-135">Issue: Entities aren't listed in alphabetical order in Common Data Service Administration (377414)</span></span>

<span data-ttu-id="6200d-136">エンティティは、**CDS 管理**ページにアルファベット順にリストされるようになりました。</span><span class="sxs-lookup"><span data-stu-id="6200d-136">Entities are now listed in alphabetical order on the **CDS Administration** page.</span></span>

### <a name="issue-changing-the-employment-type-with-a-future-date-doesnt-allow-a-position-assignment-339958"></a><span data-ttu-id="6200d-137">問題: 未来の日付で雇用タイプを変更しても、職位割り当てが許可されない (339958)</span><span class="sxs-lookup"><span data-stu-id="6200d-137">Issue: Changing the employment type with a future date doesn't allow a position assignment (339958)</span></span>

<span data-ttu-id="6200d-138">この変更により、作業者タイプが変更された場合 (たとえば、従業員から契約社員へ) に職位割り当てが可能になります。</span><span class="sxs-lookup"><span data-stu-id="6200d-138">This change allows for position assignments when worker types are changed (for example, from employee to contractor).</span></span>

### <a name="issue-updating-the-common-data-service-leave-bank-transaction-entity-creates-a-new-record-in-talent-352938"></a><span data-ttu-id="6200d-139">問題: Common Data Service 休暇バンク トランザクション エンティティを更新すると、Talent に新しいレコードが作成される (352938)</span><span class="sxs-lookup"><span data-stu-id="6200d-139">Issue: Updating the Common Data Service Leave bank transaction entity creates a new record in Talent (352938)</span></span>

<span data-ttu-id="6200d-140">休暇バンク トランザクションの Common Data Service が更新されると、休暇トランザクションが更新されるようになりました。</span><span class="sxs-lookup"><span data-stu-id="6200d-140">The leave transaction is now updated when an update is made to Common Data Service for leave bank transactions.</span></span>

### <a name="issue-the-title-of-attachments-for-feedback-items-shows-the-feedback-description-343765"></a><span data-ttu-id="6200d-141">問題: フィードバック項目の添付ファイルのタイトルに、フィードバックの説明が表示される (343765)</span><span class="sxs-lookup"><span data-stu-id="6200d-141">Issue: The title of attachments for feedback items shows the feedback description (343765)</span></span>

<span data-ttu-id="6200d-142">フィードバックの説明は、添付ファイルのタイトルに表示されなくなります。</span><span class="sxs-lookup"><span data-stu-id="6200d-142">The feedback description no longer appears in the attachment title.</span></span>

### <a name="issue-compensation-workflow-comments-field-shows-incorrect-content-339297"></a><span data-ttu-id="6200d-143">問題: 報酬ワークフローのコメント フィールドに正しくない内容が表示される (339297)</span><span class="sxs-lookup"><span data-stu-id="6200d-143">Issue: Compensation workflow Comments field shows incorrect content (339297)</span></span>

<span data-ttu-id="6200d-144">この変更により、**%HcmActionState.HcmWorkerActionComment.Comments%** フィールドの内容が表示されます。</span><span class="sxs-lookup"><span data-stu-id="6200d-144">This change shows the content of the **%HcmActionState.HcmWorkerActionComment.Comments%** field.</span></span>

### <a name="issue-workcalendarentity-and-workcalendardayentity-arent-exposed-through-odata-376329"></a><span data-ttu-id="6200d-145">問題: WorkCalendarEntity と WorkCalendarDayEntity が OData を通して公開されていない (376329)</span><span class="sxs-lookup"><span data-stu-id="6200d-145">Issue: WorkCalendarEntity and WorkCalendarDayEntity aren't exposed through OData (376329)</span></span>

<span data-ttu-id="6200d-146">このリリースでは、**WorkCalendarEntity** および **WorkCalendarDayEntity** がオープン データ プロトコル (OData) を通して使用できるようになりました。</span><span class="sxs-lookup"><span data-stu-id="6200d-146">In this release, **WorkCalendarEntity** and **WorkCalendarDayEntity** are now available through Open Data Protocol (OData).</span></span>

### <a name="issue-hcmworkerentity-is-slow-when-odata-is-used-375221"></a><span data-ttu-id="6200d-147">問題: OData が使用されると HCMWorkerEntity の速度が低下する (375221)</span><span class="sxs-lookup"><span data-stu-id="6200d-147">Issue: HCMWorkerEntity is slow when OData is used (375221)</span></span>

<span data-ttu-id="6200d-148">変更により、Microsoft Excel ブック デザイナーが使用される場合、**HCMWorkerEntity** のパフォーマンスは向上します。</span><span class="sxs-lookup"><span data-stu-id="6200d-148">Changes improve the performance of **HCMWorkerEntity** when the Microsoft Excel workbook designer is used.</span></span>

### <a name="issue-manager-performance-journal-entry-shows-an-error-after-deleting-a-performance-journal-and-creating-a-new-one-336061"></a><span data-ttu-id="6200d-149">問題: 業績仕訳帳を削除して新しい仕訳帳を作成した後に、マネージャー業績仕訳帳入力でエラーが表示される (336061)</span><span class="sxs-lookup"><span data-stu-id="6200d-149">Issue: Manager performance journal entry shows an error after deleting a performance journal and creating a new one (336061)</span></span>

<span data-ttu-id="6200d-150">このリリースでは、1 つの業績仕訳帳が削除され、その後すぐに新しい仕訳帳が作成された場合に発生する問題が修正されています。</span><span class="sxs-lookup"><span data-stu-id="6200d-150">This release corrects an issue that occurs after one performance journal is deleted and a new one is created immediately afterward.</span></span> <span data-ttu-id="6200d-151">この修正により、マネージャーのセルフサービスの動作が変更されます。</span><span class="sxs-lookup"><span data-stu-id="6200d-151">This correction changes the behavior in manager self-service.</span></span>

## <a name="coming-soon"></a><span data-ttu-id="6200d-152">間もなく公開</span><span class="sxs-lookup"><span data-stu-id="6200d-152">Coming soon</span></span>

### <a name="print-performance-reviews"></a><span data-ttu-id="6200d-153">業績の確認の印刷</span><span class="sxs-lookup"><span data-stu-id="6200d-153">Print performance reviews</span></span>

<span data-ttu-id="6200d-154">詳細については、Dynamics 365: 2019 リリース ウェーブ 2 プランにある[業績の確認の印刷](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-talent/print-performance-reviews)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="6200d-154">See [Print performance reviews](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-talent/print-performance-reviews) in the Dynamics 365: 2019 release wave 2 plan.</span></span>