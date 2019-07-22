---
title: Dynamics 365 for Talent の新機能または変更された機能 (2019 年 6 月 11 日)
description: このトピックでは、Microsoft Dynamics 365 for Talent の新機能または変更された機能について説明します。
author: Darinkramer
manager: AnnBe
ms.date: 06/11/2019
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
ms.search.validFrom: 2019-06-11
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 42b9541b152d2a6daa1dbf95ecf30a2f51eb36f3
ms.sourcegitcommit: 31a918d357a7182f3870713a9c4455bd5c44cd58
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/18/2019
ms.locfileid: "1634483"
---
# <a name="whats-new-or-changed-in-dynamics-365-for-talent-june-11-2019"></a><span data-ttu-id="bdfe7-103">Dynamics 365 for Talent の新機能または変更された機能 (2019 年 6 月 11 日)</span><span class="sxs-lookup"><span data-stu-id="bdfe7-103">What's new or changed in Dynamics 365 for Talent (June 11, 2019)</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="bdfe7-104">このトピックでは、Microsoft Dynamics 365 for Talent の新機能または変更された機能について説明します。</span><span class="sxs-lookup"><span data-stu-id="bdfe7-104">This topic describes features that are either new or changed in Microsoft Dynamics 365 for Talent.</span></span>

## <a name="changes-in-attract"></a><span data-ttu-id="bdfe7-105">Attract の変更</span><span class="sxs-lookup"><span data-stu-id="bdfe7-105">Changes in Attract</span></span>

### <a name="search-engine-optimization-for-job-posts"></a><span data-ttu-id="bdfe7-106">人材募集のための検索エンジンの最適化</span><span class="sxs-lookup"><span data-stu-id="bdfe7-106">Search engine optimization for job posts</span></span>

<span data-ttu-id="bdfe7-107">Dynamics 365 for Talent: Attract 管理センターで**検索エンジン最適化**が有効にされた後、Attract は Google インデックス作成アプリケーション プログラミング インターフェイス (API) に、新しいジョブの有効化およびポスト時、または既存のジョブが更新された時に Web ページのクローリングを行うよう通知します。</span><span class="sxs-lookup"><span data-stu-id="bdfe7-107">After you turn on **Search Engine Optimization** in the Dynamics 365 for Talent: Attract Admin center, Attract informs the Google Indexing application programming interface (API) to crawl the webpage whenever you activate and post a new job or update an existing job.</span></span> <span data-ttu-id="bdfe7-108">このようにして、ジョブは Google および他の検索エンジンの検索結果に表示されます。</span><span class="sxs-lookup"><span data-stu-id="bdfe7-108">In this way, the job will appear in the search results for Google and other search engines.</span></span>

<span data-ttu-id="bdfe7-109">同様に、ジョブをアンポストした場合、Attract はインデックス作成 API に通知し、アンポストされたジョブは検索結果に表示されなくなります。</span><span class="sxs-lookup"><span data-stu-id="bdfe7-109">Likewise, whenever you unpost a job, Attract informs the Indexing API, so that the unposted job will stop appearing in search results.</span></span>

> [!NOTE]
> <span data-ttu-id="bdfe7-110">Web クローラーには、Web ページのクローリングまたは検索結果の更新のために定義されたタイムフレームはありません。</span><span class="sxs-lookup"><span data-stu-id="bdfe7-110">Web crawlers don't have a defined timeframe for crawling webpages or updating search results.</span></span>

## <a name="coming-soon-in-attract"></a><span data-ttu-id="bdfe7-111">Attract で間もなく公開</span><span class="sxs-lookup"><span data-stu-id="bdfe7-111">Coming soon in Attract</span></span>

### <a name="job-approvals-appear-on-the-home-page"></a><span data-ttu-id="bdfe7-112">ホーム ページ上のジョブ承認の表示</span><span class="sxs-lookup"><span data-stu-id="bdfe7-112">Job approvals appear on the home page</span></span>

<span data-ttu-id="bdfe7-113">承認は、ダッシュボードの**承認**セクションに表示されます。</span><span class="sxs-lookup"><span data-stu-id="bdfe7-113">Approvals appear in an **Approvals** section on the dashboard.</span></span> <span data-ttu-id="bdfe7-114">承認者は**自分に割り当て済み**で自分の承認を確認できます。ここではジョブ ID、職位、他の承認者、およびジョブが割り当てられた日付が表示されます。</span><span class="sxs-lookup"><span data-stu-id="bdfe7-114">Approvers can review their approvals under **Assigned to you**, which shows the job ID, the job title, other approvers, and the date when the job was assigned.</span></span> <span data-ttu-id="bdfe7-115">承認のジョブを送信するユーザーは、**ユーザーにより要求済**で自分のジョブを確認できます。ここでは送信したジョブを承認する必要がある承認者を表示します。</span><span class="sxs-lookup"><span data-stu-id="bdfe7-115">Users who submit a job for approval can review their jobs under **Requested by you**, which shows the approvers who must still approve the submitted job.</span></span>

## <a name="changes-in-onboard"></a><span data-ttu-id="bdfe7-116">Onboard の変更</span><span class="sxs-lookup"><span data-stu-id="bdfe7-116">Changes in Onboard</span></span>

<span data-ttu-id="bdfe7-117">今回のリリースには、Dynamics 365 for Talent: Onboard のマイナーなバグ修正が含まれています。</span><span class="sxs-lookup"><span data-stu-id="bdfe7-117">This release includes minor bug fixes for Dynamics 365 for Talent: Onboard.</span></span>

## <a name="changes-in-core-hr"></a><span data-ttu-id="bdfe7-118">Core HR の変更</span><span class="sxs-lookup"><span data-stu-id="bdfe7-118">Changes in Core HR</span></span>

<span data-ttu-id="bdfe7-119">このセクションに記載された変更は、ビルド番号 8.1.2337 に適用されます。</span><span class="sxs-lookup"><span data-stu-id="bdfe7-119">The changes that are described in this section apply to build number 8.1.2337.</span></span>

### <a name="platform-update-27"></a><span data-ttu-id="bdfe7-120">プラットフォーム update 27</span><span class="sxs-lookup"><span data-stu-id="bdfe7-120">Platform update 27</span></span>

<span data-ttu-id="bdfe7-121">プラットフォーム更新プログラム 27 に関する詳細については [Dynamics 365 for Finance and Operations プラットフォーム更新プログラム 27 (2019 年 6 月) のプレビュー機能](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/get-started/whats-new-platform-update-27) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="bdfe7-121">For more details about Platform update 27, see [Preview features in Dynamics 365 for Finance and Operations platform update 27 (June 2019)](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/get-started/whats-new-platform-update-27).</span></span>

### <a name="feature-management-workspace-in-talent"></a><span data-ttu-id="bdfe7-122">Talent における機能管理ワークスペース</span><span class="sxs-lookup"><span data-stu-id="bdfe7-122">Feature management workspace in Talent</span></span>

<span data-ttu-id="bdfe7-123">**システム管理**の**機能管理**ワークスペースにより、各リリースで提供されている機能の表示、有効化、無効化、およびスケジュールを行うことができます。</span><span class="sxs-lookup"><span data-stu-id="bdfe7-123">The **Feature management** workspace in **System administration** lets you view, enable, disable, and schedule features that have been delivered in each release.</span></span> <span data-ttu-id="bdfe7-124">既定では、新機能が無効になっています。</span><span class="sxs-lookup"><span data-stu-id="bdfe7-124">By default, new features are turned off.</span></span> <span data-ttu-id="bdfe7-125">**機能管理**ワークスペースを使用して、ドキュメントを有効にし、表示することができます。</span><span class="sxs-lookup"><span data-stu-id="bdfe7-125">You can use the **Feature management** workspace to turn them on and view the documentation for them.</span></span>

### <a name="common-data-service-entity-support-for-custom-fields"></a><span data-ttu-id="bdfe7-126">カスタム フィールドに対する Common Data Service エンティティのサポート</span><span class="sxs-lookup"><span data-stu-id="bdfe7-126">Common Data Service entity support for custom fields</span></span>

<span data-ttu-id="bdfe7-127">発行機関エンティティは、カスタム フィールドをサポートするようになりました。</span><span class="sxs-lookup"><span data-stu-id="bdfe7-127">The Issuing agency entity now supports custom fields.</span></span>

### <a name="new-common-data-service-entities"></a><span data-ttu-id="bdfe7-128">新しい Common Data Service エンティティ</span><span class="sxs-lookup"><span data-stu-id="bdfe7-128">New Common Data Service entities</span></span>

<span data-ttu-id="bdfe7-129">タスク グループ エンティティが追加されました。</span><span class="sxs-lookup"><span data-stu-id="bdfe7-129">The Task group entity has been added.</span></span>

## <a name="in-preview"></a><span data-ttu-id="bdfe7-130">プレビュー</span><span class="sxs-lookup"><span data-stu-id="bdfe7-130">In preview</span></span>

### <a name="preview-features-will-be-enabled-only-in-sandbox-environments"></a><span data-ttu-id="bdfe7-131">プレビュー機能はサンドボックス環境でのみ有効になります</span><span class="sxs-lookup"><span data-stu-id="bdfe7-131">Preview features will be enabled only in sandbox environments</span></span>

<span data-ttu-id="bdfe7-132">変更を公開する方法の詳細については、[Talent のプロビジョニング](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/provisioning-talent) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="bdfe7-132">For more information about how changes are published, see [Provision Talent](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/provisioning-talent).</span></span>

<span data-ttu-id="bdfe7-133">Talent の新しいインスタンスをプロビジョニングする時に、インスタンス タイプを実稼働またはサンドボックスのどちらかに指定することができます。</span><span class="sxs-lookup"><span data-stu-id="bdfe7-133">When you provision a new instance of Talent, you can indicate whether the instance type is Production or Sandbox.</span></span> <span data-ttu-id="bdfe7-134">サンドボックス インスタンス タイプにより、新機能を事前にテストできるようになります。</span><span class="sxs-lookup"><span data-stu-id="bdfe7-134">The Sandbox instance type allows for early testing of new features.</span></span> <span data-ttu-id="bdfe7-135">既存の Talent のインスタンスすべては、**実稼働**インスタンス タイプに更新されます。</span><span class="sxs-lookup"><span data-stu-id="bdfe7-135">All existing Talent instances will be updated to the **Production** instance type.</span></span> <span data-ttu-id="bdfe7-136">既存のインスタンスのいずれかを**サンドボックス** インスタンス タイプに更新する場合は、変更要求を開始するよう [サポート](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/talent-support) に連絡してください。</span><span class="sxs-lookup"><span data-stu-id="bdfe7-136">If you want one of your existing instances to be updated to the **Sandbox** instance type, contact [Support](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/talent-support) to initiate the change request.</span></span>

### <a name="restrict-the-leave-types-in-time-off-requests"></a><span data-ttu-id="bdfe7-137">休暇申請で休暇タイプを制限する</span><span class="sxs-lookup"><span data-stu-id="bdfe7-137">Restrict the leave types in time-off requests</span></span>

<span data-ttu-id="bdfe7-138">組織はさまざまなタイプの休暇を従業員に提供できます。</span><span class="sxs-lookup"><span data-stu-id="bdfe7-138">Organizations can offer many types of leave to employees.</span></span> <span data-ttu-id="bdfe7-139">ただし、一部の休暇タイプについては、従業員が休暇申請を送信することが適切でない場合もあります。</span><span class="sxs-lookup"><span data-stu-id="bdfe7-139">However, it might not be appropriate for employees to submit time-off requests for some leave types.</span></span> <span data-ttu-id="bdfe7-140">それらの休暇タイプは、Human resources (HR) によって代わりに管理されることがあります。</span><span class="sxs-lookup"><span data-stu-id="bdfe7-140">Those leave types might be managed by Human resources (HR) instead.</span></span> <span data-ttu-id="bdfe7-141">このリリースでは、従業員が休暇申請を送信できる休暇タイプをコンフィギュレーションできます。</span><span class="sxs-lookup"><span data-stu-id="bdfe7-141">In this release, you can configure which leave types employees can submit time-off requests for.</span></span> 

## <a name="coming-soon-in-core-hr"></a><span data-ttu-id="bdfe7-142">Core HR で間もなく公開</span><span class="sxs-lookup"><span data-stu-id="bdfe7-142">Coming soon in Core HR</span></span>

### <a name="view-extended-information-about-report-performance-in-manager-self-service"></a><span data-ttu-id="bdfe7-143">マネージャー セルフサービスのレポートのパフォーマンスに関する追加情報の確認</span><span class="sxs-lookup"><span data-stu-id="bdfe7-143">View extended information about report performance in manager self-service</span></span>

<span data-ttu-id="bdfe7-144">新しいオプションにより、マネージャーは自分の直接レポートと拡張レポートの両方の業績を確認できるようになります。</span><span class="sxs-lookup"><span data-stu-id="bdfe7-144">A new option will let managers view the performance of both their direct reports and their extended reports.</span></span> <span data-ttu-id="bdfe7-145">現在、ライン マネージャーは業績目標の割り当てと更新、また新しい確認の発行をすることができます。</span><span class="sxs-lookup"><span data-stu-id="bdfe7-145">Currently, line managers can assign and update performance goals and issue new reviews.</span></span> <span data-ttu-id="bdfe7-146">また、直属のマネージャーと従業員は業績仕訳の管理および更新を行うことにより、業績確認プロセスがスムーズに行われることを保証できます。</span><span class="sxs-lookup"><span data-stu-id="bdfe7-146">In addition, direct managers and their employees can maintain and update performance journals to help guarantee that the performance review process goes smoothly.</span></span> <span data-ttu-id="bdfe7-147">この変更が実装されると、マネージャーは直接レポートに加えて、拡張レポートの業績関連情報の確認および管理ができるようになります。</span><span class="sxs-lookup"><span data-stu-id="bdfe7-147">When this change is implemented, managers will be able to view and maintain performance-related information for their extended reports in addition to their direct reports.</span></span>

### <a name="print-performance-reviews"></a><span data-ttu-id="bdfe7-148">業績の確認の印刷</span><span class="sxs-lookup"><span data-stu-id="bdfe7-148">Print performance reviews</span></span>

<span data-ttu-id="bdfe7-149">従業員、マネージャー、および HR は、従業員の業績の確認を印刷できるようになります。</span><span class="sxs-lookup"><span data-stu-id="bdfe7-149">Employees, managers, and HR will be able to print an employee's performance review.</span></span>
