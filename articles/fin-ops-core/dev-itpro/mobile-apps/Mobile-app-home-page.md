---
title: モバイル アプリのホーム ページ
description: このトピックでは、Finance and Operations (Dynamics 365) モバイル アプリについて説明し、組織で実装するのに役立つリソースへのリンクを提供します。
author: ChrisGarty
ms.date: 01/22/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.custom: 272853
ms.assetid: c99f818f-27b3-4e45-92b4-74272dad0e17
ms.search.region: Global
ms.author: cgarty
ms.dyn365.ops.version: Platform update 4
ms.search.validFrom: 2017-02-28
ms.openlocfilehash: 9707a1f8a90a615dbc8f34f4bb1f05d34d8fe7f3
ms.sourcegitcommit: 34b478f175348d99df4f2f0c2f6c0c21b6b2660a
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/16/2021
ms.locfileid: "5908235"
---
# <a name="mobile-app-home-page"></a><span data-ttu-id="f083b-103">モバイル アプリのホーム ページ</span><span class="sxs-lookup"><span data-stu-id="f083b-103">Mobile app home page</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f083b-104">このトピックでは、**Finance and Operations (Dynamics 365)** モバイル アプリについて説明し、組織で実装するのに役立つリソースへのリンクを提供します。</span><span class="sxs-lookup"><span data-stu-id="f083b-104">This topic describes the **Finance and Operations (Dynamics 365)** mobile app and provides links to resources that can help you implement it in your organization.</span></span>

<a name="overview"></a><span data-ttu-id="f083b-105">概要</span><span class="sxs-lookup"><span data-stu-id="f083b-105">Overview</span></span>
--------

<span data-ttu-id="f083b-106">モバイル アプリにより、組織が業務プロセスをモバイル デバイスで使用可能になります。</span><span class="sxs-lookup"><span data-stu-id="f083b-106">The mobile app enables your organization to make its business processes available on mobile devices.</span></span> <span data-ttu-id="f083b-107">IT 管理者が組織用のモバイル ワークスペースを有効にすると、ユーザーはアプリにログインしてすぐにモバイル デバイスから業務プロセスの実行を開始できます。</span><span class="sxs-lookup"><span data-stu-id="f083b-107">After your IT admin enables the mobile workspaces for your organization, users can sign in to the app and immediately begin to run business processes from their mobile devices.</span></span> <span data-ttu-id="f083b-108">モバイル アプリには、生産性を高めるのに役立つ次の機能が含まれています。</span><span class="sxs-lookup"><span data-stu-id="f083b-108">The mobile app includes the following features that can help increase productivity:</span></span>

- <span data-ttu-id="f083b-109">ネットワーク接続が断続的な場合やモバイル デバイスが完全にオフラインの場合でも、ユーザーは業務データを表示、編集、および処理できます。</span><span class="sxs-lookup"><span data-stu-id="f083b-109">Users can view, edit, and act on business data, even if they have intermittent network connectivity or their mobile devices are completely offline.</span></span> <span data-ttu-id="f083b-110">デバイスがネットワーク接続を再確立する際に、オフライン データ操作は自動的に同期されます。</span><span class="sxs-lookup"><span data-stu-id="f083b-110">When a device reestablishes a network connection, offline data operations are automatically synchronized.</span></span>
- <span data-ttu-id="f083b-111">IT 管理者または開発者は、組織に合わせたモバイル ワークスペースを構築し公開することができます。</span><span class="sxs-lookup"><span data-stu-id="f083b-111">IT admins or developers can build and publish mobile workspaces that have been tailored to their organization.</span></span> <span data-ttu-id="f083b-112">アプリは既存のコード資産を使用します。</span><span class="sxs-lookup"><span data-stu-id="f083b-112">The app uses your existing code assets.</span></span> <span data-ttu-id="f083b-113">したがって、検証手順、ビジネス ロジック、またセキュリティ コンフィギュレーションも再実装の必要はありません。</span><span class="sxs-lookup"><span data-stu-id="f083b-113">Therefore, you don't have to re-implement your validation procedures, business logic, or security configuration.</span></span>
- <span data-ttu-id="f083b-114">IT 管理者または開発者は、Web クライアントに含まれているポイント アンド クリック ワークスペース デザイナーを使用してモバイル ワークスペースを簡単に設計できます。</span><span class="sxs-lookup"><span data-stu-id="f083b-114">IT admins or developers can easily design mobile workspaces by using the point-and-click workspace designer that is included with the web client.</span></span>
- <span data-ttu-id="f083b-115">IT 管理者または開発者は、ビジネス ロジック拡張フレームワークを使用してワークスペースのオフライン機能を必要に応じて最適化できます。</span><span class="sxs-lookup"><span data-stu-id="f083b-115">IT admins or developers can optionally optimize the offline capabilities of workspaces by using the Business logic extensibility framework.</span></span> <span data-ttu-id="f083b-116">デバイスがオフラインの間もデータは引き続き処理されるため、デバイスが常時ネットワーク接続していなくても、モバイル シナリオは豊富で流動的なままです。</span><span class="sxs-lookup"><span data-stu-id="f083b-116">Because data continues to be processed while a device is offline, your mobile scenarios remain rich and fluid, even if devices don't have constant network connectivity.</span></span>

## <a name="elements-of-the-mobile-app"></a><span data-ttu-id="f083b-117">モバイル アプリの要素</span><span class="sxs-lookup"><span data-stu-id="f083b-117">Elements of the mobile app</span></span>
<span data-ttu-id="f083b-118">モバイル アプリのナビゲーションは、ダッシュボード、ワークスペース、ページ、およびアクションという 4 つの基本概念で構成されています。</span><span class="sxs-lookup"><span data-stu-id="f083b-118">Navigation in the mobile app consists of four basic concepts: the dashboard, workspaces, pages, and actions.</span></span> 

<span data-ttu-id="f083b-119">[![モバイル アプリのナビゲーション概念](./media/mobilephoneapp1-1024x536.png)](./media/mobilephoneapp1.png)</span><span class="sxs-lookup"><span data-stu-id="f083b-119">[![Navigation concepts in the mobile app](./media/mobilephoneapp1-1024x536.png)](./media/mobilephoneapp1.png)</span></span>

1. <span data-ttu-id="f083b-120">アプリを起動すると、**ダッシュボード** に移動します。</span><span class="sxs-lookup"><span data-stu-id="f083b-120">When you start the app, you go to the **dashboard**.</span></span>
2. <span data-ttu-id="f083b-121">ダッシュボードでは、公開された **ワークスペース** の一覧が表示されます。</span><span class="sxs-lookup"><span data-stu-id="f083b-121">On the dashboard, you can see a list of **workspaces** that have been published.</span></span>
3. <span data-ttu-id="f083b-122">各ワークスペースでは、そのワークスペースで使用可能な **ページ** の一覧が表示されます。</span><span class="sxs-lookup"><span data-stu-id="f083b-122">In each workspace, you can see a list of **pages** that are available for that workspace.</span></span>
4. <span data-ttu-id="f083b-123">ページ上では、いくつかの操作を行うことができます。</span><span class="sxs-lookup"><span data-stu-id="f083b-123">After you're on a page, you can perform several actions.</span></span> <span data-ttu-id="f083b-124">次にいくつか例を挙げます。</span><span class="sxs-lookup"><span data-stu-id="f083b-124">Here are some examples:</span></span>

    - <span data-ttu-id="f083b-125">詳細データの表示。</span><span class="sxs-lookup"><span data-stu-id="f083b-125">View detailed data.</span></span>
    - <span data-ttu-id="f083b-126">エンティティの詳細または明細行などの関連データの他のページに移動します。</span><span class="sxs-lookup"><span data-stu-id="f083b-126">Navigate to other pages for related data, such as entity details or lines.</span></span>
    - <span data-ttu-id="f083b-127">そのページに有効な **アクション** の一覧を参照してください。</span><span class="sxs-lookup"><span data-stu-id="f083b-127">See a list of **actions** that are available for that page.</span></span> <span data-ttu-id="f083b-128">アクションで、データ作成もしくは既存データの編集ができます。</span><span class="sxs-lookup"><span data-stu-id="f083b-128">Actions let you create or edit existing data.</span></span>

## <a name="implementation-process"></a><span data-ttu-id="f083b-129">実装プロセス</span><span class="sxs-lookup"><span data-stu-id="f083b-129">Implementation process</span></span>
<span data-ttu-id="f083b-130">次の図では、Microsoft に提供されるモバイル ワークスペースとカスタム モバイル ワークスペースの両方を実装するためのプロセスを表示します。</span><span class="sxs-lookup"><span data-stu-id="f083b-130">The following illustration shows the process for implementing both mobile workspaces that are provided by Microsoft and custom mobile workspaces.</span></span> 

<span data-ttu-id="f083b-131">[![モバイル アプリの実装プロセス](./media/Mobile-implementation-process-5.png)](./media/Mobile-implementation-process-5.png)</span><span class="sxs-lookup"><span data-stu-id="f083b-131">[![Mobile apps implementation process](./media/Mobile-implementation-process-5.png)](./media/Mobile-implementation-process-5.png)</span></span>

<span data-ttu-id="f083b-132">次の表には、Microsoft によって提供されるモバイル ワークスペースとカスタム モバイル ワークスペースの両方を実装する際に役立つリソースへのリンクが含まれています。</span><span class="sxs-lookup"><span data-stu-id="f083b-132">The following table includes links to resources that can help you implement both mobile workspaces that are provided by Microsoft and custom mobile workspaces.</span></span> <span data-ttu-id="f083b-133">最初の列の番号は、前述の図の番号付きの手順に対応します。</span><span class="sxs-lookup"><span data-stu-id="f083b-133">The numbers in the first column correspond to the numbered steps in the previous illustration.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="f083b-134">ステップ</span><span class="sxs-lookup"><span data-stu-id="f083b-134">Step</span></span></th>
<th><span data-ttu-id="f083b-135">役割</span><span class="sxs-lookup"><span data-stu-id="f083b-135">Role</span></span></th>
<th><span data-ttu-id="f083b-136">アクション</span><span class="sxs-lookup"><span data-stu-id="f083b-136">Action</span></span></th>
<th><span data-ttu-id="f083b-137">アクションを完了するのに役立つリソース</span><span class="sxs-lookup"><span data-stu-id="f083b-137">Resources to help you complete the action</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="f083b-138">1</span><span class="sxs-lookup"><span data-stu-id="f083b-138">1</span></span></td>
<td><span data-ttu-id="f083b-139">システム管理者</span><span class="sxs-lookup"><span data-stu-id="f083b-139">System administrator</span></span></td>
<td><span data-ttu-id="f083b-140">組織で Finance and Operations アプリを実装します。</span><span class="sxs-lookup"><span data-stu-id="f083b-140">Implement the Finance and Operations app in your organization.</span></span></td>
<td><ul><li><span data-ttu-id="f083b-141">まだ Microsoft Dynamics 365 のバージョンを配置していない場合は、<a href="../deployment/deploy-demo-environment.md">デモ環境の配置</a> を参照してください。</span><span class="sxs-lookup"><span data-stu-id="f083b-141">If you haven&#39;t yet deployed a version of Microsoft Dynamics 365, see <a href="../deployment/deploy-demo-environment.md">Deploy a demo environment</a>.</span></span></li><li><span data-ttu-id="f083b-142">使用可能なモバイル ワークスペースの一覧は、<a href="mobile-workspaces-released.md">最近リリースされたモバイル ワークスペース</a> を参照してください。</span><span class="sxs-lookup"><span data-stu-id="f083b-142">To see a list of mobile workspaces that can be used, see <a href="mobile-workspaces-released.md">Mobile workspaces recently released</a>.</span></span></li></ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f083b-143">2</span><span class="sxs-lookup"><span data-stu-id="f083b-143">2</span></span></td>
<td><span data-ttu-id="f083b-144">システム管理者</span><span class="sxs-lookup"><span data-stu-id="f083b-144">System administrator</span></span></td>
<td><span data-ttu-id="f083b-145"><strong>Microsoft Dynamics 365 for Operations バージョン 1611 を使用している場合は:</strong>Microsoft が提供するモバイル ワークスペースを有効にする KB をダウンロードしインストールします。</span><span class="sxs-lookup"><span data-stu-id="f083b-145"><strong>If you&#39;re using Microsoft Dynamics 365 for Operations version 1611:</strong> Download and install KBs that enable the mobile workspaces that are provided by Microsoft.</span></span></td>
<td><span data-ttu-id="f083b-146">詳細については、次のトピックを参照してください。</span><span class="sxs-lookup"><span data-stu-id="f083b-146">See the following topics for more information:</span></span>
<ul>

<li><span data-ttu-id="f083b-147"><a href="../../../finance/cost-accounting/cost-controlling-mobile-workspace.md">コスト管理モバイル ワークスペース</a></span><span class="sxs-lookup"><span data-stu-id="f083b-147"><a href="../../../finance/cost-accounting/cost-controlling-mobile-workspace.md">Cost controlling mobile workspaces</a></span></span></li>
<li><span data-ttu-id="f083b-148"><a href="../../../supply-chain/inventory/inventory-on-hand-mobile-workspace.md">手持在庫モバイル ワークスペース</a></span><span class="sxs-lookup"><span data-stu-id="f083b-148"><a href="../../../supply-chain/inventory/inventory-on-hand-mobile-workspace.md">Inventory on-hand mobile workspace</a></span></span></li>
<li><span data-ttu-id="f083b-149"><a href="../../../supply-chain/sales-marketing/sales-orders-mobile-workspace.md">販売注文モバイル ワークスペース</a></span><span class="sxs-lookup"><span data-stu-id="f083b-149"><a href="../../../supply-chain/sales-marketing/sales-orders-mobile-workspace.md">Sales orders mobile workspaces</a></span></span></li>
<li><span data-ttu-id="f083b-150"><a href="../../../supply-chain/procurement/vendor-collaboration-mobile-workspace.md">仕入先コラボレーションのモバイル ワークスペース</a></span><span class="sxs-lookup"><span data-stu-id="f083b-150"><a href="../../../supply-chain/procurement/vendor-collaboration-mobile-workspace.md">Vendor collaboration mobile workspace</a></span></span></li>
<li><span data-ttu-id="f083b-151"><a href="/dynamics365/project-operations/prod-pma/project-time-entry-mobile-workspace">プロジェクト時間入力モバイル ワークスペース</a></span><span class="sxs-lookup"><span data-stu-id="f083b-151"><a href="/dynamics365/project-operations/prod-pma/project-time-entry-mobile-workspace">Project time entry mobile workspace</a></span></span></li>
<li><span data-ttu-id="f083b-152"><a href="/dynamics365/project-operations/prod-exp/expense-management-mobile-workspace">経費管理モバイル ワークスペース</a></span><span class="sxs-lookup"><span data-stu-id="f083b-152"><a href="/dynamics365/project-operations/prod-exp/expense-management-mobile-workspace">Expense management mobile workspace</a></span></span></li>

</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f083b-153">3</span><span class="sxs-lookup"><span data-stu-id="f083b-153">3</span></span></td>
<td><span data-ttu-id="f083b-154">システム管理者</span><span class="sxs-lookup"><span data-stu-id="f083b-154">System administrator</span></span></td>
<td><span data-ttu-id="f083b-155">Microsoft が提供するモバイル ワークスペースを公開します。</span><span class="sxs-lookup"><span data-stu-id="f083b-155">Publish the mobile workspaces that are provided by Microsoft.</span></span></td>
<td><span data-ttu-id="f083b-156"><a href="publish-mobile-workspace.md">モバイル ワークスペースの公開</a>
</span><span class="sxs-lookup"><span data-stu-id="f083b-156"><a href="publish-mobile-workspace.md">Publish a mobile workspace</a>
</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f083b-157">4</span><span class="sxs-lookup"><span data-stu-id="f083b-157">4</span></span></td>
<td><span data-ttu-id="f083b-158">開発者もしくは独立系ソフトウェア ベンダー (ISV)</span><span class="sxs-lookup"><span data-stu-id="f083b-158">Developer or independent software vendor (ISV)</span></span></td>
<td><span data-ttu-id="f083b-159">モバイル プラットフォームを使用して、カスタム モバイル ワークスペースを作成します。</span><span class="sxs-lookup"><span data-stu-id="f083b-159">Use the mobile platform to create custom mobile workspaces.</span></span></td>
<td><span data-ttu-id="f083b-160"><a href="platform/mobile-platform-home-page.md">モバイル プラットフォーム</a></span><span class="sxs-lookup"><span data-stu-id="f083b-160"><a href="platform/mobile-platform-home-page.md">Mobile platform</a></span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f083b-161">5</span><span class="sxs-lookup"><span data-stu-id="f083b-161">5</span></span></td>
<td><span data-ttu-id="f083b-162">ISV</span><span class="sxs-lookup"><span data-stu-id="f083b-162">ISV</span></span></td>
<td><span data-ttu-id="f083b-163">カスタム モバイル ワークスペースを含む配置可能パッケージを作成し、Microsoft Dynamics Lifecycle Services (LCS) にそのパッケージをアップロードします。</span><span class="sxs-lookup"><span data-stu-id="f083b-163">Create a deployable package that contains custom mobile workspaces, and upload the package to Microsoft Dynamics Lifecycle Services (LCS).</span></span></td>
<td><span data-ttu-id="f083b-164"><a href="../deployment/create-apply-deployable-package.md">配置可能パッケージの作成</a></span><span class="sxs-lookup"><span data-stu-id="f083b-164"><a href="../deployment/create-apply-deployable-package.md">Create a deployable package</a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f083b-165">6</span><span class="sxs-lookup"><span data-stu-id="f083b-165">6</span></span></td>
<td><span data-ttu-id="f083b-166">システム管理者</span><span class="sxs-lookup"><span data-stu-id="f083b-166">System administrator</span></span></td>
<td><span data-ttu-id="f083b-167">独立系ソフトウェア ベンダー (ISV) が提供するカスタム ワークスペースの含まれた配置可能パッケージを適用します。</span><span class="sxs-lookup"><span data-stu-id="f083b-167">Apply the deployable package that contains the custom workspaces that are provided by the independent software vendor (ISV).</span></span></td>
<td><span data-ttu-id="f083b-168"><a href="../deployment/apply-deployable-package-system.md">配置可能パッケージの適用</a></span><span class="sxs-lookup"><span data-stu-id="f083b-168"><a href="../deployment/apply-deployable-package-system.md">Apply a deployable package</a></span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f083b-169">7</span><span class="sxs-lookup"><span data-stu-id="f083b-169">7</span></span></td>
<td><span data-ttu-id="f083b-170">システム管理者</span><span class="sxs-lookup"><span data-stu-id="f083b-170">System administrator</span></span></td>
<td><span data-ttu-id="f083b-171">ISV が提供するカスタム モバイル ワークスペースを公開します。</span><span class="sxs-lookup"><span data-stu-id="f083b-171">Publish the custom mobile workspaces that are provided by the ISV.</span></span></td>
<td><span data-ttu-id="f083b-172"><a href="publish-mobile-workspace.md">モバイル ワークスペースの公開</a></span><span class="sxs-lookup"><span data-stu-id="f083b-172"><a href="publish-mobile-workspace.md">Publish a mobile workspace</a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f083b-173">8</span><span class="sxs-lookup"><span data-stu-id="f083b-173">8</span></span></td>
<td><span data-ttu-id="f083b-174">ユーザー</span><span class="sxs-lookup"><span data-stu-id="f083b-174">User</span></span></td>
<td><span data-ttu-id="f083b-175">モバイル アプリのダウンロードとインストール。</span><span class="sxs-lookup"><span data-stu-id="f083b-175">Download and install the mobile app.</span></span></td>
<td><span data-ttu-id="f083b-176">
<a href="https://go.microsoft.com/fwlink/?linkid=850662">Android 用 Finance and Operations アプリ</a></span><span class="sxs-lookup"><span data-stu-id="f083b-176">
<a href="https://go.microsoft.com/fwlink/?linkid=850662">Finance and Operations app for Android</a></span></span><BR/><span data-ttu-id="f083b-177">
<a href="https://go.microsoft.com/fwlink/?linkid=850663">iOS 用 Finance and Operations アプリ</a></span><span class="sxs-lookup"><span data-stu-id="f083b-177">
<a href="https://go.microsoft.com/fwlink/?linkid=850663">Finance and Operations app for iOS</a></span></span><BR/>
<span data-ttu-id="f083b-178">(サポートされていない Windows Phone)</span><span class="sxs-lookup"><span data-stu-id="f083b-178">(Windows Phone unsupported)</span></span>
</td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f083b-179">9</span><span class="sxs-lookup"><span data-stu-id="f083b-179">9</span></span></td>
<td><span data-ttu-id="f083b-180">ユーザー</span><span class="sxs-lookup"><span data-stu-id="f083b-180">User</span></span></td>
<td><span data-ttu-id="f083b-181">ログインして、モバイル アプリを使用します。</span><span class="sxs-lookup"><span data-stu-id="f083b-181">Sign in, and use the mobile app.</span></span> <span data-ttu-id="f083b-182">アプリには、システム管理者によって公開されたモバイル ワークスペースが含まれています。</span><span class="sxs-lookup"><span data-stu-id="f083b-182">The app includes the mobile workspaces that have been published by the system administrator.</span></span></td>
<td><span data-ttu-id="f083b-183">Microsoft が提供したモバイル ワークスペースの一覧は、<a href="mobile-workspaces-released.md">最近リリースされたモバイル ワークスペース</a> を参照してください。</span><span class="sxs-lookup"><span data-stu-id="f083b-183">To see a list of mobile workspaces that are provided by Microsoft, see <a href="mobile-workspaces-released.md">Mobile workspaces recently released</a>.</span></span>
</td>
</tr>
</tbody>
</table>

## <a name="troubleshooting"></a><span data-ttu-id="f083b-184">トラブルシューティング</span><span class="sxs-lookup"><span data-stu-id="f083b-184">Troubleshooting</span></span>
[<span data-ttu-id="f083b-185">モバイル プラットフォームのリソース</span><span class="sxs-lookup"><span data-stu-id="f083b-185">Mobile platform resources</span></span>](platform/mobile-platform-home-page.md#troubleshooting-the-app)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]