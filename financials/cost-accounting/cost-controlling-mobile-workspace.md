---
title: "コスト管理モバイル ワークスペース"
description: "このトピックでは、原価管理モバイル ワークスペースについての情報を提供します。 このワークスペースにより、コスト センターの管理者は時間や場所に関わらず、コスト センターのパフォーマンスに関する情報を表示できます。"
author: AndersGirke
manager: AnnBe
ms.date: 06/16/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations, UnifiedOperations
ms.custom: 267114
ms.assetid: 612f2988-b2b9-420d-9825-40b99dc0e204
ms.search.region: global
ms.author: aevengir
ms.dyn365.ops.intro: Version 1611
ms.search.validFrom: 2016-11-30
ms.translationtype: Human Translation
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 6019634c47bd97fb16ea8aaf029ea176f095b8b6
ms.contentlocale: ja-jp
ms.lasthandoff: 08/29/2017

---

# <a name="cost-controlling-mobile-workspace"></a><span data-ttu-id="4133f-104">コスト管理モバイル ワークスペース</span><span class="sxs-lookup"><span data-stu-id="4133f-104">Cost controlling mobile workspace</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="4133f-105">このトピックでは、**原価管理** モバイル ワークスペースについての情報を提供します。</span><span class="sxs-lookup"><span data-stu-id="4133f-105">This topic provides information about the **Cost controlling** mobile workspace.</span></span> <span data-ttu-id="4133f-106">このワークスペースにより、コスト センターの管理者は時間や場所に関わらず、コスト センターのパフォーマンスに関する情報を表示できます。</span><span class="sxs-lookup"><span data-stu-id="4133f-106">This workspace lets cost center managers view information about cost center performance anytime and anywhere.</span></span>

<span data-ttu-id="4133f-107">このモバイル ワークスペースは、Microsoft Dynamics 365 for Unified Operations モバイル アプリで使用するためのものです。</span><span class="sxs-lookup"><span data-stu-id="4133f-107">This mobile workspace is intended to be used with the Microsoft Dynamics 365 for Unified Operations mobile app.</span></span>

## <a name="overview"></a><span data-ttu-id="4133f-108">概要</span><span class="sxs-lookup"><span data-stu-id="4133f-108">Overview</span></span>
<span data-ttu-id="4133f-109">**原価管理** モバイル ワークスペースは、予算原価に対する実際原価を比較して、原価部門の現在のパフォーマンスのインスタント ビューを提供します。</span><span class="sxs-lookup"><span data-stu-id="4133f-109">The **Cost controlling** mobile workspace provides an instant view of the current performance of cost centers by comparing actual costs against the budgeted costs.</span></span> <span data-ttu-id="4133f-110">個々のコスト要素のステータスにドリル ダウンすることができます。</span><span class="sxs-lookup"><span data-stu-id="4133f-110">You can drill down to the status of individual cost elements.</span></span>

<span data-ttu-id="4133f-111">たとえば、従業員は国際会議への招待を受けますが、組織はすべての旅費を負担する必要があります。</span><span class="sxs-lookup"><span data-stu-id="4133f-111">For example, an employee receives an invitation to an international conference, but the organization must cover all the travel expenses.</span></span> <span data-ttu-id="4133f-112">その従業員は、会議に出席できるかどうか管理者に尋ねます。</span><span class="sxs-lookup"><span data-stu-id="4133f-112">The employee asks his manager whether he can attend the conference.</span></span> <span data-ttu-id="4133f-113">管理者は、すぐに携帯電話で **原価管理** モバイル ワークスペースを開き、会議に出席する予算があるかどうかを確認します。</span><span class="sxs-lookup"><span data-stu-id="4133f-113">The manager opens the **Cost controlling** mobile workspace on her mobile device to see whether she has budget for the employee to attend the conference.</span></span>

### <a name="data-security"></a><span data-ttu-id="4133f-114">データ セキュリティ</span><span class="sxs-lookup"><span data-stu-id="4133f-114">Data security</span></span>
<span data-ttu-id="4133f-115">**原価管理** モバイル ワークスペースのデータは、ユーザー資格情報で保護されます。</span><span class="sxs-lookup"><span data-stu-id="4133f-115">The data in the **Cost controlling** mobile workspace is secured through user credentials.</span></span> <span data-ttu-id="4133f-116">原価部門管理者は、自身の原価部門のデータだけを表示することができます。</span><span class="sxs-lookup"><span data-stu-id="4133f-116">Cost center managers are allowed to see data only for their own cost center.</span></span> <span data-ttu-id="4133f-117">アクセス レベルのセキュリティは、**原価会計** モジュール内で管理されます。</span><span class="sxs-lookup"><span data-stu-id="4133f-117">The access-level security is managed in the **Cost accounting** module.</span></span>

<span data-ttu-id="4133f-118">原価経理担当は、**原価会計** モジュールで **原価管理** モバイル ワークスペースのコンフィギュレーションを定義します。</span><span class="sxs-lookup"><span data-stu-id="4133f-118">Cost accountants define the configuration of the **Cost controlling** mobile workspace in the **Cost accounting** module.</span></span> <span data-ttu-id="4133f-119">ワークスペースをモバイル アプリに公開すると、このアプリで使用できるようになります。</span><span class="sxs-lookup"><span data-stu-id="4133f-119">After the workspace is published to the mobile app, it's available in the app.</span></span> <span data-ttu-id="4133f-120">これで組織内のすべての原価部門管理者が同じ形式でデータを表示できるようになります。</span><span class="sxs-lookup"><span data-stu-id="4133f-120">Therefore, all cost center managers in the organization can view data in the same format.</span></span>

### <a name="actions-views-and-links"></a><span data-ttu-id="4133f-121">操作、ビュー、リンク</span><span class="sxs-lookup"><span data-stu-id="4133f-121">Actions, views, and links</span></span>
<span data-ttu-id="4133f-122">**原価管理** モバイル ワークスペースでは、次のアクション、ビュー、およびリンクが提供されます。</span><span class="sxs-lookup"><span data-stu-id="4133f-122">The **Cost controlling** mobile workspace provides the following actions, views, and links:</span></span>

-   <span data-ttu-id="4133f-123">**アクション:**</span><span class="sxs-lookup"><span data-stu-id="4133f-123">**Actions:**</span></span>

    -   <span data-ttu-id="4133f-124">レイアウトを選択するには、**構成の選択** を使用します。</span><span class="sxs-lookup"><span data-stu-id="4133f-124">Use **Select configuration** to select a layout.</span></span>
    -   <span data-ttu-id="4133f-125">データをフィルター処理する原価部門を選択するには、**原価オブジェクトの選択** を使用します。</span><span class="sxs-lookup"><span data-stu-id="4133f-125">Use **Select cost object** to select the cost centers to filter data on.</span></span>
    
        > [!NOTE]
        > <span data-ttu-id="4133f-126">一覧に表示されるコスト センターは、**原価会計** モジュールで許可されるアクセスによって異なります。</span><span class="sxs-lookup"><span data-stu-id="4133f-126">The cost centers that appear in the list depend on the access that is granted in the **Cost accounting** module.</span></span>

-   <span data-ttu-id="4133f-127">**ビュー:** 選択されたアクションと **原価会計** モジュールの設定に基づいて、カードに関する以下の情報を表示することができます。</span><span class="sxs-lookup"><span data-stu-id="4133f-127">**Views:** Based on the actions that are selected and the configuration in the **Cost accounting** module, you can view the following information on the cards:</span></span>

    -   <span data-ttu-id="4133f-128">実績対予算 (現在の期間)</span><span class="sxs-lookup"><span data-stu-id="4133f-128">Actual vs budget (current period)</span></span>
    -   <span data-ttu-id="4133f-129">実績対修正予算 (現在の期間)</span><span class="sxs-lookup"><span data-stu-id="4133f-129">Actual vs revised budget (current period)</span></span>
    -   <span data-ttu-id="4133f-130">実際対予算 (前の期間)</span><span class="sxs-lookup"><span data-stu-id="4133f-130">Actual vs budget (previous period)</span></span>
    -   <span data-ttu-id="4133f-131">実際対修正予算 (前の期間)</span><span class="sxs-lookup"><span data-stu-id="4133f-131">Actual vs revised budget (previous period)</span></span>
    -   <span data-ttu-id="4133f-132">実際対予算 (年度累計)</span><span class="sxs-lookup"><span data-stu-id="4133f-132">Actual vs budget (year to date)</span></span>
    -   <span data-ttu-id="4133f-133">実際対修正予算 (年度累計)</span><span class="sxs-lookup"><span data-stu-id="4133f-133">Actual vs revised budget (year to date)</span></span>

    <span data-ttu-id="4133f-134">すべてのカードに表示される金額は、実績、予算、差異、差異の割合 (％) です。</span><span class="sxs-lookup"><span data-stu-id="4133f-134">The following amounts are shown on every card: Actual, Budget, Variance, and Variance %.</span></span>

-   <span data-ttu-id="4133f-135">**リンク:**</span><span class="sxs-lookup"><span data-stu-id="4133f-135">**Links:**</span></span>

    -   <span data-ttu-id="4133f-136">現在の期間の詳細</span><span class="sxs-lookup"><span data-stu-id="4133f-136">Details for current period</span></span>
    -   <span data-ttu-id="4133f-137">前の期間の詳細</span><span class="sxs-lookup"><span data-stu-id="4133f-137">Details for previous period</span></span>
    -   <span data-ttu-id="4133f-138">年度累計の詳細</span><span class="sxs-lookup"><span data-stu-id="4133f-138">Details for year to date</span></span>

    <span data-ttu-id="4133f-139">リンクを選択すると、カードが原価要素ごとに表示されます。</span><span class="sxs-lookup"><span data-stu-id="4133f-139">When you select a link, a card is shown for each cost element.</span></span> <span data-ttu-id="4133f-140">すべてのカードに表示される金額は、実績、予算、予算差異、予算差異 %、修正予算、修正予算差異、修正予算差異 % です。</span><span class="sxs-lookup"><span data-stu-id="4133f-140">The following amounts are shown on every card: Actual, Budget, Budget variance, Budget variance %, Revised budget, Revised budget variance, and Revised budget variance %.</span></span>
    
    <span data-ttu-id="4133f-141">[![原価要素のカード](./media/Cost-controlling.png)](./media/Cost-controlling.png)</span><span class="sxs-lookup"><span data-stu-id="4133f-141">[![Card for a cost element](./media/Cost-controlling.png)](./media/Cost-controlling.png)</span></span>

## <a name="prerequisites"></a><span data-ttu-id="4133f-142">前提条件</span><span class="sxs-lookup"><span data-stu-id="4133f-142">Prerequisites</span></span>
<span data-ttu-id="4133f-143">組織に配置されている Microsoft Dynamics 365 のバージョンに基づいて、前提条件は異なります。</span><span class="sxs-lookup"><span data-stu-id="4133f-143">The prerequisites differ, based on the version of Microsoft Dynamics 365 that has been deployed for your organization.</span></span>

### <a name="prerequisites-if-you-use-microsoft-dynamics-365-for-finance-and-operations-enterprise-edition-july-2017-update"></a><span data-ttu-id="4133f-144">Microsoft Dynamics 365 for Finance and Operations、Enterprise Edition 2017 年 7 月の更新プログラムを使用している場合の前提条件</span><span class="sxs-lookup"><span data-stu-id="4133f-144">Prerequisites if you use Microsoft Dynamics 365 for Finance and Operations, Enterprise edition July 2017 update</span></span>
<span data-ttu-id="4133f-145">Microsoft Dynamics 365 for Finance and Operations、Enterprise Edition 2017 年 ７ 月の更新プログラムを組織に配置している場合、システム管理者は **原価管理** モバイル ワークスペースを公開する必要があります。</span><span class="sxs-lookup"><span data-stu-id="4133f-145">If Microsoft Dynamics 365 for Finance and Operations, Enterprise edition July 2017 update has been deployed for your organization, the system administrator must publish the **Cost controlling** mobile workspace.</span></span> <span data-ttu-id="4133f-146">手順については、「[モバイル ワークスペースの公開](/dynamics365/unified-operations/dev-itpro/mobile-apps/publish-mobile-workspace)」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="4133f-146">For instructions, see [Publish a mobile workspace](/dynamics365/unified-operations/dev-itpro/mobile-apps/publish-mobile-workspace).</span></span>

### <a name="prerequisites-if-you-use-microsoft-dynamics-365-for-operations-version-1611-with-platform-update-3-or-later"></a><span data-ttu-id="4133f-147">Microsoft Dynamics 365 for Operations バージョン 1611 およびプラットフォーム更新プログラム 3 以降を使用している場合の前提条件</span><span class="sxs-lookup"><span data-stu-id="4133f-147">Prerequisites if you use Microsoft Dynamics 365 for Operations version 1611 with platform update 3 or later</span></span>
<span data-ttu-id="4133f-148">Microsoft Dynamics 365 for Operations バージョン 1611 およびプラットフォーム 更新プログラム 3 以降を組織に配置している場合、システム管理者は次の前提条件を満たす必要があります。</span><span class="sxs-lookup"><span data-stu-id="4133f-148">If Microsoft Dynamics 365 for Operations version 1611 with platform update 3 or later has been deployed for your organization, the system administrator must complete the following prerequisites.</span></span>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="4133f-149">前提条件</span><span class="sxs-lookup"><span data-stu-id="4133f-149">Prerequisite</span></span></th>
<th><span data-ttu-id="4133f-150">役割</span><span class="sxs-lookup"><span data-stu-id="4133f-150">Role</span></span></th>
<th><span data-ttu-id="4133f-151">説明</span><span class="sxs-lookup"><span data-stu-id="4133f-151">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="4133f-152">KB 4013633 を実装します。</span><span class="sxs-lookup"><span data-stu-id="4133f-152">Implement KB 4013633.</span></span></td>
<td><span data-ttu-id="4133f-153">システム管理者</span><span class="sxs-lookup"><span data-stu-id="4133f-153">System administrator</span></span></td>

<td><span data-ttu-id="4133f-154">KB 4013633 は、<strong>原価管理</strong> モバイル ワークスペースを含む X++ の更新またはメタデータ修正プログラムです。</span><span class="sxs-lookup"><span data-stu-id="4133f-154">KB 4013633 is an X++ update or metadata hotfix that contains the <strong>Cost controlling</strong> mobile workspace.</span></span> <span data-ttu-id="4133f-155">KB 4013633 を実装するには、システム管理者は次の手順に従う必要があります。</span><span class="sxs-lookup"><span data-stu-id="4133f-155">To implement KB 4013633, your system administrator must follow these steps.</span></span>
<ol>
<li><span data-ttu-id="4133f-156"><a href="/dynamics365/unified-operations/dev-itpro/migration-upgrade/download-hotfix-lcs">Microsoft Dynamics Lifecycle Services (LCS) からメタデータ修正プログラムをダウンロードします</a>。</span><span class="sxs-lookup"><span data-stu-id="4133f-156"><a href="/dynamics365/unified-operations/dev-itpro/migration-upgrade/download-hotfix-lcs">Download the metadata hotfix from Microsoft Dynamics Lifecycle Services (LCS)</a>.</span></span></li>
<li><span data-ttu-id="4133f-157"><a href="/dynamics365/unified-operations/dev-itpro/migration-upgrade/install-metadata-hotfix-package">メタデータ修正プログラムをインストールします。</a></span><span class="sxs-lookup"><span data-stu-id="4133f-157"><a href="/dynamics365/unified-operations/dev-itpro/migration-upgrade/install-metadata-hotfix-package">Install the metadata hotfix</a>.</span></span></li>
<li><span data-ttu-id="4133f-158"><strong>SCMMobile</strong> モデルを含む<a href="/dynamics365/unified-operations/dev-itpro/deployment/create-apply-deployable-package">配置可能パッケージを作成し</a>、配置可能パッケージを LCS にアップロードします。</span><span class="sxs-lookup"><span data-stu-id="4133f-158"><a href="/dynamics365/unified-operations/dev-itpro/deployment/create-apply-deployable-package">Create a deployable package</a> that contains the <strong>SCMMobile</strong> model, and then upload the deployable package to LCS.</span></span></li>
<li><span data-ttu-id="4133f-159"><a href="/dynamics365/unified-operations/dev-itpro/deployment/apply-deployable-package-system">配置可能パッケージを適用します</a>。</span><span class="sxs-lookup"><span data-stu-id="4133f-159"><a href="/dynamics365/unified-operations/dev-itpro/deployment/apply-deployable-package-system">Apply the deployable package</a>.</span></span></li>

</ol></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4133f-160"><strong>原価管理</strong> モバイル ワークスペースを公開します。</span><span class="sxs-lookup"><span data-stu-id="4133f-160">Publish the <strong>Cost controlling</strong> mobile workspace.</span></span></td>
<td><span data-ttu-id="4133f-161">システム管理者</span><span class="sxs-lookup"><span data-stu-id="4133f-161">System administrator</span></span></td>
<td><span data-ttu-id="4133f-162">「<a href="/dynamics365/unified-operations/dev-itpro/mobile-apps/publish-mobile-workspace">モバイル ワークスペースの公開</a>」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="4133f-162">See <a href="/dynamics365/unified-operations/dev-itpro/mobile-apps/publish-mobile-workspace">Publish a mobile workspace</a>.</span></span></td>
</tr>
</tbody>
</table>


## <a name="download-and-install-the-mobile-app"></a><span data-ttu-id="4133f-163">モバイル アプリのダウンロードとインストール</span><span class="sxs-lookup"><span data-stu-id="4133f-163">Download and install the mobile app</span></span>
<span data-ttu-id="4133f-164">Dynamics 365 for Unified Operations モバイル アプリをダウンロードしてインストールします。</span><span class="sxs-lookup"><span data-stu-id="4133f-164">Download and install the Dynamics 365 for Unified Operations mobile app:</span></span>

-   [<span data-ttu-id="4133f-165">Android フォン用</span><span class="sxs-lookup"><span data-stu-id="4133f-165">For Android phones</span></span>](https://go.microsoft.com/fwlink/?linkid=850662)
-   [<span data-ttu-id="4133f-166">iPhone 用</span><span class="sxs-lookup"><span data-stu-id="4133f-166">For iPhones</span></span>](https://go.microsoft.com/fwlink/?linkid=850663)

## <a name="sign-in-to-the-mobile-app"></a><span data-ttu-id="4133f-167">モバイル アプリにログインします。</span><span class="sxs-lookup"><span data-stu-id="4133f-167">Sign in to the mobile app</span></span>

1.  <span data-ttu-id="4133f-168">モバイル デバイスでアプリを起動します。</span><span class="sxs-lookup"><span data-stu-id="4133f-168">Start the app on your mobile device.</span></span>
2.  <span data-ttu-id="4133f-169">Dynamics 365 の URL を入力します。</span><span class="sxs-lookup"><span data-stu-id="4133f-169">Enter your Dynamics 365 URL.</span></span>
3.  <span data-ttu-id="4133f-170">初めてサインインすると、ユーザー名とパスワードを要求されます。</span><span class="sxs-lookup"><span data-stu-id="4133f-170">The first time that you sign in, you're prompted for your user name and password.</span></span> <span data-ttu-id="4133f-171">資格情報を入力します。</span><span class="sxs-lookup"><span data-stu-id="4133f-171">Enter your credentials.</span></span>
4.  <span data-ttu-id="4133f-172">サインインすると、使用可能な会社のワークスペースが表示されます。</span><span class="sxs-lookup"><span data-stu-id="4133f-172">After you sign in, the available workspaces for your company are shown.</span></span> <span data-ttu-id="4133f-173">なお、システム管理者が後で新しいワークスペースを公開すると、モバイル ワークスペースのリストを更新する必要があります。</span><span class="sxs-lookup"><span data-stu-id="4133f-173">Note that if your system administrator publishes a new workspace later, you will have to refresh the list of mobile workspaces.</span></span>

<span data-ttu-id="4133f-174">[![プルして更新](./media/pull-to-refresh-list-of-workspaces-183x300.png)](./media/pull-to-refresh-list-of-workspaces.png)</span><span class="sxs-lookup"><span data-stu-id="4133f-174">[![Pull to refresh](./media/pull-to-refresh-list-of-workspaces-183x300.png)](./media/pull-to-refresh-list-of-workspaces.png)</span></span>

## <a name="view-the-performance-of-your-cost-center-by-using-the-cost-controlling-mobile-workspace"></a><span data-ttu-id="4133f-175">原価管理モバイル ワークスペースを使用して、原価部門のパフォーマンスを表示します。</span><span class="sxs-lookup"><span data-stu-id="4133f-175">View the performance of your cost center by using the Cost controlling mobile workspace</span></span>

1.  <span data-ttu-id="4133f-176">モバイル デバイスで、[**原価管理**] ワークスペースを選択します。</span><span class="sxs-lookup"><span data-stu-id="4133f-176">On your mobile device, select the **Cost controlling** workspace.</span></span>
2.  <span data-ttu-id="4133f-177">[**原価オブジェクト管理**] を選択します。</span><span class="sxs-lookup"><span data-stu-id="4133f-177">Select **Cost object controlling**.</span></span>
3.  <span data-ttu-id="4133f-178">**操作** を選択します。</span><span class="sxs-lookup"><span data-stu-id="4133f-178">Select **Actions**.</span></span>
4.  <span data-ttu-id="4133f-179">**コンフィギュレーションの選択** を選択して、原価管理レイアウトを選択します。</span><span class="sxs-lookup"><span data-stu-id="4133f-179">Select **Select configuration** to select a cost controlling layout.</span></span>
5.  <span data-ttu-id="4133f-180">**完了** を選択します。</span><span class="sxs-lookup"><span data-stu-id="4133f-180">Select **Done**.</span></span>
6.  <span data-ttu-id="4133f-181">**操作** を選択します。</span><span class="sxs-lookup"><span data-stu-id="4133f-181">Select **Actions**.</span></span>
7.  <span data-ttu-id="4133f-182">[**原価オブジェクトの選択**] を選択して、アクセスが許可された原価部門を選択します。</span><span class="sxs-lookup"><span data-stu-id="4133f-182">Select **Select cost object** to select the cost centers that you've been granted access to.</span></span>
8.  <span data-ttu-id="4133f-183">**完了** を選択します。</span><span class="sxs-lookup"><span data-stu-id="4133f-183">Select **Done**.</span></span>
9.  <span data-ttu-id="4133f-184">原価部門の全体パフォーマンスを表示します。</span><span class="sxs-lookup"><span data-stu-id="4133f-184">View the overall performance of your cost center.</span></span>
10. <span data-ttu-id="4133f-185">**現在の期間の詳細を** リンクを選択します。</span><span class="sxs-lookup"><span data-stu-id="4133f-185">Select the **Details for current period** link.</span></span>
11. <span data-ttu-id="4133f-186">個々の原価要素のパフォーマンスを表示します。</span><span class="sxs-lookup"><span data-stu-id="4133f-186">View the performance of individual cost elements.</span></span>
12. <span data-ttu-id="4133f-187">特定の原価要素も検索できます。</span><span class="sxs-lookup"><span data-stu-id="4133f-187">You can also search for specific cost elements.</span></span>


