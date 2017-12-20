---
title: "モバイル アプリのホーム ページ"
description: "このトピックでは、Microsoft Dynamics 365 for Unified Operations モバイル アプリについて説明し、組織で実装するのに役立つリソースへのリンクを提供します。"
author: sericks007
manager: AnnBe
ms.date: 06/16/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.scope: Operations
ms.custom: 272853
ms.assetid: c99f818f-27b3-4e45-92b4-74272dad0e17
ms.search.region: Global
ms.author: sericks
ms.dyn365.ops.intro: Platform update 4
ms.search.validFrom: 2017-02-28
ms.translationtype: HT
ms.sourcegitcommit: 6e64337f19600b18320550d91c134949c33af7b0
ms.openlocfilehash: 233d91138b11905d971be90154da54e61bbe2919
ms.contentlocale: ja-jp
ms.lasthandoff: 12/01/2017

---

# <a name="mobile-app-home-page"></a><span data-ttu-id="e342d-103">モバイル アプリのホーム ページ</span><span class="sxs-lookup"><span data-stu-id="e342d-103">Mobile app home page</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="e342d-104">このトピックでは、Microsoft Dynamics 365 for Unified Operations モバイル アプリについて説明し、組織で実装するのに役立つリソースへのリンクを提供します。</span><span class="sxs-lookup"><span data-stu-id="e342d-104">This topic describes the Microsoft Dynamics 365 for Unified Operations mobile app and provides links to resources that can help you implement it in your organization.</span></span>

> [!NOTE]
> <span data-ttu-id="e342d-105">以前のモバイル アプリの名前は、*Microsoft Dynamics 365 for Finance and Operations* でした。</span><span class="sxs-lookup"><span data-stu-id="e342d-105">The mobile app was previously named *Microsoft Dynamics 365 for Finance and Operations*.</span></span>

<a name="overview"></a><span data-ttu-id="e342d-106">概要</span><span class="sxs-lookup"><span data-stu-id="e342d-106">Overview</span></span>
--------

<span data-ttu-id="e342d-107">モバイル アプリにより、組織が業務プロセスをモバイル デバイスで使用可能になります。</span><span class="sxs-lookup"><span data-stu-id="e342d-107">The mobile app enables your organization to make its business processes available on mobile devices.</span></span> <span data-ttu-id="e342d-108">IT 管理者が組織用のモバイル ワークスペースを有効にすると、ユーザーはアプリにログインしてすぐにモバイル デバイスから業務プロセスの実行を開始できます。</span><span class="sxs-lookup"><span data-stu-id="e342d-108">After your IT admin enables the mobile workspaces for your organization, users can sign in to the app and immediately begin to run business processes from their mobile devices.</span></span> <span data-ttu-id="e342d-109">モバイル アプリには、生産性を高めるのに役立つ次の機能が含まれています。</span><span class="sxs-lookup"><span data-stu-id="e342d-109">The mobile app includes the following features that can help increase productivity:</span></span>

- <span data-ttu-id="e342d-110">ネットワーク接続が断続的な場合やモバイル デバイスが完全にオフラインの場合でも、ユーザーは業務データを表示、編集、および処理できます。</span><span class="sxs-lookup"><span data-stu-id="e342d-110">Users can view, edit, and act on business data, even if they have intermittent network connectivity or their mobile devices are completely offline.</span></span> <span data-ttu-id="e342d-111">デバイスがネットワーク接続を再確立する際に、オフライン データ操作は Dynamics 365 for Finance and Operations、Enterprise Edition、または Microsoft Dynamics 365 for Finance and Operations と自動的に同期します。</span><span class="sxs-lookup"><span data-stu-id="e342d-111">When a device reestablishes a network connection, offline data operations are automatically synchronized with Dynamics 365 for Finance and Operations, Enterprise edition, or Microsoft Dynamics 365 for Finance and Operations.</span></span>
- <span data-ttu-id="e342d-112">IT 管理者または開発者は、組織に合わせたモバイル ワークスペースを構築し公開することができます。</span><span class="sxs-lookup"><span data-stu-id="e342d-112">IT admins or developers can build and publish mobile workspaces that have been tailored to their organization.</span></span> <span data-ttu-id="e342d-113">アプリは既存のコード資産を使用します。</span><span class="sxs-lookup"><span data-stu-id="e342d-113">The app uses your existing code assets.</span></span> <span data-ttu-id="e342d-114">したがって、検証手順、ビジネス ロジック、またセキュリティ コンフィギュレーションも再実装の必要はありません。</span><span class="sxs-lookup"><span data-stu-id="e342d-114">Therefore, you don't have to re-implement your validation procedures, business logic, or security configuration.</span></span>
- <span data-ttu-id="e342d-115">IT 管理者または開発者は、Web クライアントに含まれているポイント アンド クリック ワークスペース デザイナーを使用してモバイル ワークスペースを簡単に設計できます。</span><span class="sxs-lookup"><span data-stu-id="e342d-115">IT admins or developers can easily design mobile workspaces by using the point-and-click workspace designer that is included with the web client.</span></span>
- <span data-ttu-id="e342d-116">IT 管理者または開発者は、ビジネス ロジック拡張フレームワークを使用してワークスペースのオフライン機能を必要に応じて最適化できます。</span><span class="sxs-lookup"><span data-stu-id="e342d-116">IT admins or developers can optionally optimize the offline capabilities of workspaces by using the Business logic extensibility framework.</span></span> <span data-ttu-id="e342d-117">デバイスがオフラインの間もデータは引き続き処理されるため、デバイスが常時ネットワーク接続していなくても、モバイル シナリオは豊富で流動的なままです。</span><span class="sxs-lookup"><span data-stu-id="e342d-117">Because data continues to be processed while a device is offline, your mobile scenarios remain rich and fluid, even if devices don't have constant network connectivity.</span></span>

## <a name="elements-of-the-mobile-app"></a><span data-ttu-id="e342d-118">モバイル アプリの要素</span><span class="sxs-lookup"><span data-stu-id="e342d-118">Elements of the mobile app</span></span>
<span data-ttu-id="e342d-119">モバイル アプリのナビゲーションは、ダッシュボード、ワークスペース、ページ、およびアクションという 4 つの基本概念で構成されています。</span><span class="sxs-lookup"><span data-stu-id="e342d-119">Navigation in the mobile app consists of four basic concepts: the dashboard, workspaces, pages, and actions.</span></span> 

<span data-ttu-id="e342d-120">[![モバイル アプリのナビゲーション概念](./media/mobilephoneapp1-1024x536.png)](./media/mobilephoneapp1.png)</span><span class="sxs-lookup"><span data-stu-id="e342d-120">[![Navigation concepts in the mobile app](./media/mobilephoneapp1-1024x536.png)](./media/mobilephoneapp1.png)</span></span>

1. <span data-ttu-id="e342d-121">アプリを起動すると、**ダッシュボード** に移動します。</span><span class="sxs-lookup"><span data-stu-id="e342d-121">When you start the app, you go to the **dashboard**.</span></span>
2. <span data-ttu-id="e342d-122">ダッシュボードでは、公開された **ワークスペース** の一覧が表示されます。</span><span class="sxs-lookup"><span data-stu-id="e342d-122">On the dashboard, you can see a list of **workspaces** that have been published.</span></span>
3. <span data-ttu-id="e342d-123">各ワークスペースでは、そのワークスペースで使用可能な **ページ** の一覧が表示されます。</span><span class="sxs-lookup"><span data-stu-id="e342d-123">In each workspace, you can see a list of **pages** that are available for that workspace.</span></span>
4. <span data-ttu-id="e342d-124">ページ上では、いくつかの操作を行うことができます。</span><span class="sxs-lookup"><span data-stu-id="e342d-124">After you're on a page, you can perform several actions.</span></span> <span data-ttu-id="e342d-125">次にいくつか例を挙げます。</span><span class="sxs-lookup"><span data-stu-id="e342d-125">Here are some examples:</span></span>

    - <span data-ttu-id="e342d-126">詳細データの表示。</span><span class="sxs-lookup"><span data-stu-id="e342d-126">View detailed data.</span></span>
    - <span data-ttu-id="e342d-127">エンティティの詳細または明細行などの関連データの他のページに移動します。</span><span class="sxs-lookup"><span data-stu-id="e342d-127">Navigate to other pages for related data, such as entity details or lines.</span></span>
    - <span data-ttu-id="e342d-128">そのページに有効な **アクション** の一覧を参照してください。</span><span class="sxs-lookup"><span data-stu-id="e342d-128">See a list of **actions** that are available for that page.</span></span> <span data-ttu-id="e342d-129">アクションで、データ作成もしくは既存データの編集ができます。</span><span class="sxs-lookup"><span data-stu-id="e342d-129">Actions let you create or edit existing data.</span></span>

## <a name="implementation-process"></a><span data-ttu-id="e342d-130">実装プロセス</span><span class="sxs-lookup"><span data-stu-id="e342d-130">Implementation process</span></span>
<span data-ttu-id="e342d-131">次の図では、Microsoft に提供されるモバイル ワークスペースとカスタム モバイル ワークスペースの両方を実装するためのプロセスを表示します。</span><span class="sxs-lookup"><span data-stu-id="e342d-131">The following illustration shows the process for implementing both mobile workspaces that are provided by Microsoft and custom mobile workspaces.</span></span> 

![モバイル アプリの実装プロセス](./media/Mobile-implementation-process-5.png)

<span data-ttu-id="e342d-133">次の表には、Microsoft によって提供されるモバイル ワークスペースとカスタム モバイル ワークスペースの両方を実装する際に役立つリソースへのリンクが含まれています。</span><span class="sxs-lookup"><span data-stu-id="e342d-133">The following table includes links to resources that can help you implement both mobile workspaces that are provided by Microsoft and custom mobile workspaces.</span></span> <span data-ttu-id="e342d-134">最初の列の番号は、前述の図の番号付きの手順に対応します。</span><span class="sxs-lookup"><span data-stu-id="e342d-134">The numbers in the first column correspond to the numbered steps in the previous illustration.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="e342d-135">ステップ</span><span class="sxs-lookup"><span data-stu-id="e342d-135">Step</span></span></th>
<th><span data-ttu-id="e342d-136">役割</span><span class="sxs-lookup"><span data-stu-id="e342d-136">Role</span></span></th>
<th><span data-ttu-id="e342d-137">アクション</span><span class="sxs-lookup"><span data-stu-id="e342d-137">Action</span></span></th>
<th><span data-ttu-id="e342d-138">アクションを完了するのに役立つリソース</span><span class="sxs-lookup"><span data-stu-id="e342d-138">Resources to help you complete the action</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="e342d-139">1</span><span class="sxs-lookup"><span data-stu-id="e342d-139">1</span></span></td>
<td><span data-ttu-id="e342d-140">システム管理者</span><span class="sxs-lookup"><span data-stu-id="e342d-140">System administrator</span></span></td>
<td><span data-ttu-id="e342d-141">組織内の Finance and Operations を実装します。</span><span class="sxs-lookup"><span data-stu-id="e342d-141">Implement Finance and Operations in your organization.</span></span></td>
<td><ul><li><span data-ttu-id="e342d-142">まだ Microsoft Dynamics 365 のバージョンを配置していない場合は、<a href="../deployment/deploy-demo-environment.md">デモ環境を配置</a> を参照してください。</span><span class="sxs-lookup"><span data-stu-id="e342d-142">If you haven't yet deployed a version of Microsoft Dynamics 365, see <a href="../deployment/deploy-demo-environment.md">Deploy a demo environment</a>.</span></span></li><li><span data-ttu-id="e342d-143">使用可能なモバイル ワークスペースの一覧は、<a href="mobile-workspaces-released.md">最近リリースされたモバイル ワークスペース</a> を参照してください。</span><span class="sxs-lookup"><span data-stu-id="e342d-143">To see a list of mobile workspaces that can be used, see <a href="mobile-workspaces-released.md">Mobile workspaces recently released</a>.</span></span></li></ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e342d-144">2</span><span class="sxs-lookup"><span data-stu-id="e342d-144">2</span></span></td>
<td><span data-ttu-id="e342d-145">システム管理者</span><span class="sxs-lookup"><span data-stu-id="e342d-145">System administrator</span></span></td>
<td><span data-ttu-id="e342d-146"><strong>Microsoft Dynamics 365 for Finance and Operations バージョン 1611 を使用している場合 :</strong> Microsoft が提供するモバイル ワークスペースを有効にする KB をダウンロードしインストールします。</span><span class="sxs-lookup"><span data-stu-id="e342d-146"><strong>If you're using Microsoft Dynamics 365 for Finance and Operations version 1611:</strong> Download and install KBs that enable the mobile workspaces that are provided by Microsoft.</span></span></td>
<td><span data-ttu-id="e342d-147">詳細については、次のトピックを参照してください。</span><span class="sxs-lookup"><span data-stu-id="e342d-147">See the following topics for more information:</span></span>
<ul>

<li><span data-ttu-id="e342d-148"><a href="../../financials/cost-accounting/cost-controlling-mobile-workspace.md">コスト管理モバイル ワークスペース</a></span><span class="sxs-lookup"><span data-stu-id="e342d-148"><a href="../../financials/cost-accounting/cost-controlling-mobile-workspace.md">Cost controlling mobile workspaces</a></span></span></li>
<li><span data-ttu-id="e342d-149"><a href="../../supply-chain/inventory/inventory-on-hand-mobile-workspace.md">手持在庫モバイル ワークスペース</a></span><span class="sxs-lookup"><span data-stu-id="e342d-149"><a href="../../supply-chain/inventory/inventory-on-hand-mobile-workspace.md">Inventory on-hand mobile workspace</a></span></span></li>
<li><span data-ttu-id="e342d-150"><a href="../../supply-chain/sales-marketing/sales-orders-mobile-workspace.md">販売注文モバイル ワークスペース</a></span><span class="sxs-lookup"><span data-stu-id="e342d-150"><a href="../../supply-chain/sales-marketing/sales-orders-mobile-workspace.md">Sales orders mobile workspaces</a></span></span></li>
<li><span data-ttu-id="e342d-151"><a href="../../supply-chain/procurement/vendor-collaboration-mobile-workspace.md">仕入先コラボレーションのモバイル ワークスペース</a></span><span class="sxs-lookup"><span data-stu-id="e342d-151"><a href="../../supply-chain/procurement/vendor-collaboration-mobile-workspace.md">Vendor collaboration mobile workspace</a></span></span></li>
<li><span data-ttu-id="e342d-152"><a href="../../financials/project-management/project-time-entry-mobile-workspace.md">プロジェクト時間入力モバイル ワークスペース</a></span><span class="sxs-lookup"><span data-stu-id="e342d-152"><a href="../../financials/project-management/project-time-entry-mobile-workspace.md">Project time entry mobile workspace</a></span></span></li>
<li><span data-ttu-id="e342d-153"><a href="../../financials/expense-management/expense-management-mobile-workspace.md">経費管理モバイル ワークスペース</a></span><span class="sxs-lookup"><span data-stu-id="e342d-153"><a href="../../financials/expense-management/expense-management-mobile-workspace.md">Expense management mobile workspace</a></span></span></li>

</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e342d-154">3</span><span class="sxs-lookup"><span data-stu-id="e342d-154">3</span></span></td>
<td><span data-ttu-id="e342d-155">システム管理者</span><span class="sxs-lookup"><span data-stu-id="e342d-155">System administrator</span></span></td>
<td><span data-ttu-id="e342d-156">Microsoft が提供するモバイル ワークスペースを公開します。</span><span class="sxs-lookup"><span data-stu-id="e342d-156">Publish the mobile workspaces that are provided by Microsoft.</span></span></td>
<td><span data-ttu-id="e342d-157"><a href="publish-mobile-workspace.md">モバイル ワークスペースの公開</a>
</span><span class="sxs-lookup"><span data-stu-id="e342d-157"><a href="publish-mobile-workspace.md">Publish a mobile workspace</a>
</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e342d-158">4</span><span class="sxs-lookup"><span data-stu-id="e342d-158">4</span></span></td>
<td><span data-ttu-id="e342d-159">開発者もしくは独立系ソフトウェア ベンダー (ISV)</span><span class="sxs-lookup"><span data-stu-id="e342d-159">Developer or independent software vendor (ISV)</span></span></td>
<td><span data-ttu-id="e342d-160">モバイル プラットフォームを使用して、カスタム モバイル ワークスペースを作成します。</span><span class="sxs-lookup"><span data-stu-id="e342d-160">Use the mobile platform to create custom mobile workspaces.</span></span></td>
<td><span data-ttu-id="e342d-161"><a href="platform/mobile-platform-home-page.md">モバイル プラットフォーム</a></span><span class="sxs-lookup"><span data-stu-id="e342d-161"><a href="platform/mobile-platform-home-page.md">Mobile platform</a></span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e342d-162">5</span><span class="sxs-lookup"><span data-stu-id="e342d-162">5</span></span></td>
<td><span data-ttu-id="e342d-163">ISV</span><span class="sxs-lookup"><span data-stu-id="e342d-163">ISV</span></span></td>
<td><span data-ttu-id="e342d-164">カスタム モバイル ワークスペースを含む配置可能パッケージを作成し、Microsoft Dynamics Lifecycle Services (LCS) にそのパッケージをアップロードします。</span><span class="sxs-lookup"><span data-stu-id="e342d-164">Create a deployable package that contains custom mobile workspaces, and upload the package to Microsoft Dynamics Lifecycle Services (LCS).</span></span></td>
<td><span data-ttu-id="e342d-165"><a href="../deployment/create-apply-deployable-package.md">配置可能パッケージを作成</a></span><span class="sxs-lookup"><span data-stu-id="e342d-165"><a href="../deployment/create-apply-deployable-package.md">Create a deployable package</a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e342d-166">6</span><span class="sxs-lookup"><span data-stu-id="e342d-166">6</span></span></td>
<td><span data-ttu-id="e342d-167">システム管理者</span><span class="sxs-lookup"><span data-stu-id="e342d-167">System administrator</span></span></td>
<td><span data-ttu-id="e342d-168">独立系ソフトウェア ベンダー (ISV) が提供するカスタム ワークスペースの含まれた配置可能パッケージを適用します。</span><span class="sxs-lookup"><span data-stu-id="e342d-168">Apply the deployable package that contains the custom workspaces that are provided by the independent software vendor (ISV).</span></span></td>
<td><span data-ttu-id="e342d-169"><a href="../deployment/apply-deployable-package-system.md">配置可能パッケージの適用</a></span><span class="sxs-lookup"><span data-stu-id="e342d-169"><a href="../deployment/apply-deployable-package-system.md">Apply a deployable package</a></span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e342d-170">7</span><span class="sxs-lookup"><span data-stu-id="e342d-170">7</span></span></td>
<td><span data-ttu-id="e342d-171">システム管理者</span><span class="sxs-lookup"><span data-stu-id="e342d-171">System administrator</span></span></td>
<td><span data-ttu-id="e342d-172">ISV が提供するカスタム モバイル ワークスペースを公開します。</span><span class="sxs-lookup"><span data-stu-id="e342d-172">Publish the custom mobile workspaces that are provided by the ISV.</span></span></td>
<td><span data-ttu-id="e342d-173"><a href="publish-mobile-workspace.md">モバイル ワークスペースの公開</a></span><span class="sxs-lookup"><span data-stu-id="e342d-173"><a href="publish-mobile-workspace.md">Publish a mobile workspace</a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e342d-174">8</span><span class="sxs-lookup"><span data-stu-id="e342d-174">8</span></span></td>
<td><span data-ttu-id="e342d-175">ユーザー</span><span class="sxs-lookup"><span data-stu-id="e342d-175">User</span></span></td>
<td><span data-ttu-id="e342d-176">モバイル アプリのダウンロードとインストール。</span><span class="sxs-lookup"><span data-stu-id="e342d-176">Download and install the mobile app.</span></span></td>
<td><ul>
<li><span data-ttu-id="e342d-177"><a href="https://go.microsoft.com/fwlink/?linkid=850662">Android フォン用</a></span><span class="sxs-lookup"><span data-stu-id="e342d-177"><a href="https://go.microsoft.com/fwlink/?linkid=850662">For Android phones</a></span></span></li>
<li><span data-ttu-id="e342d-178"><a href="https://go.microsoft.com/fwlink/?linkid=850663">iPhone 用</a></span><span class="sxs-lookup"><span data-stu-id="e342d-178"><a href="https://go.microsoft.com/fwlink/?linkid=850663">For iPhones</a></span></span></li></ul>
</td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e342d-179">9</span><span class="sxs-lookup"><span data-stu-id="e342d-179">9</span></span></td>
<td><span data-ttu-id="e342d-180">ユーザー</span><span class="sxs-lookup"><span data-stu-id="e342d-180">User</span></span></td>
<td><span data-ttu-id="e342d-181">ログインして、モバイル アプリを使用します。</span><span class="sxs-lookup"><span data-stu-id="e342d-181">Sign in, and use the mobile app.</span></span> <span data-ttu-id="e342d-182">アプリには、システム管理者によって公開されたモバイル ワークスペースが含まれています。</span><span class="sxs-lookup"><span data-stu-id="e342d-182">The app includes the mobile workspaces that have been published by the system administrator.</span></span></td>
<td><span data-ttu-id="e342d-183">Microsoft が提供したモバイル ワークスペースの一覧は、<a href="mobile-workspaces-released.md">最近リリースされたモバイル ワークスペース</a> を参照してください。</span><span class="sxs-lookup"><span data-stu-id="e342d-183">To see a list of mobile workspaces that are provided by Microsoft, see <a href="mobile-workspaces-released.md">Mobile workspaces recently released</a>.</span></span>
</td>
</tr>
</tbody>
</table>

