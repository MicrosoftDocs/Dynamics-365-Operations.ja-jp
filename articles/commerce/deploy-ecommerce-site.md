---
title: 新しい eコマース テナントのデプロイ
description: このトピックでは、Microsoft Dynamics Lifecycle Services (LCS) を使用して新しい Dynamics 365 Commerce e コマース サイトをデプロイする方法について説明します。
author: psimolin
manager: annbe
ms.date: 07/02/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 157dc8225e5bbf9338a1b5a79a2880e8a8c4bf10
ms.sourcegitcommit: 4bf5ae2f2f144a28e431ed574c7e8438dc5935de
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/13/2020
ms.locfileid: "4517285"
---
# <a name="deploy-a-new-e-commerce-tenant"></a><span data-ttu-id="19be2-103">新しい eコマース テナントのデプロイ</span><span class="sxs-lookup"><span data-stu-id="19be2-103">Deploy a new e-commerce tenant</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="19be2-104">このトピックでは、Microsoft Dynamics Lifecycle Services (LCS) を使用して新しい Dynamics 365 Commerce e コマース サイトをデプロイする方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="19be2-104">This topic describes how to deploy a new Dynamics 365 Commerce e-commerce site by using Microsoft Dynamics Lifecycle Services (LCS).</span></span>

## <a name="overview"></a><span data-ttu-id="19be2-105">概要</span><span class="sxs-lookup"><span data-stu-id="19be2-105">Overview</span></span>

<span data-ttu-id="19be2-106">Microsoft Dynamics Lifecycle Services (LCS) は、パートナーや顧客がプロジェクト環境を管理したり、Microsoft Dynamics 製品や機能に関する最新情報を表示したり、サポート インシデントを作成、追跡、参照したりするために使用できる、クラウドベースのコラボレーション ワークスペースです。</span><span class="sxs-lookup"><span data-stu-id="19be2-106">Microsoft Dynamics Lifecycle Services (LCS) is a cloud-based collaborative workspace that partners and customers can use to manage their projects and environments, view the latest information about Microsoft Dynamics products and features, and create, track, and browse support incidents.</span></span> <span data-ttu-id="19be2-107">e コマースの管理機能は LCS に統合されています。</span><span class="sxs-lookup"><span data-stu-id="19be2-107">E-commerce management features are integrated into LCS.</span></span>

<span data-ttu-id="19be2-108">LCS の詳細については、[Lifecycle Services ユーザー ガイド](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="19be2-108">To learn more about LCS, see the [Lifecycle Services User Guide](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide).</span></span>
    
## <a name="get-started"></a><span data-ttu-id="19be2-109">開始する</span><span class="sxs-lookup"><span data-stu-id="19be2-109">Get started</span></span>

<span data-ttu-id="19be2-110">e コマースを初期化する前に、プロジェクト、環境、Retail Cloud Scale Unit (RCSU) を初期化する必要があります。</span><span class="sxs-lookup"><span data-stu-id="19be2-110">Before you can initialize e-commerce, you must initialize a project, an environment, and a Retail Cloud Scale Unit (RCSU).</span></span> <span data-ttu-id="19be2-111">LCS で初期化を行うには、プロジェクト所有者ロールまたは環境マネージャ ロールのいずれかのアクセス許可が必要です。</span><span class="sxs-lookup"><span data-stu-id="19be2-111">To do the initialization in LCS, you must have permissions for either the Project Owner or Environment manager role.</span></span> <span data-ttu-id="19be2-112">実稼働環境とサンドボックス環境のトポロジがサポートされています。</span><span class="sxs-lookup"><span data-stu-id="19be2-112">The production and sandbox environment topologies are supported.</span></span>

<span data-ttu-id="19be2-113">環境に関する詳細については、[環境計画](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/imp-lifecycle/environment-planning)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="19be2-113">For more information about environments, see [Environment planning](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/imp-lifecycle/environment-planning).</span></span> <span data-ttu-id="19be2-114">RCSU の詳細については、[Retail Cloud Scale Unit の初期化](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/deployment/initialize-retail-channels)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="19be2-114">For more information about RCSU, see [Initialize Retail Cloud Scale Unit](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/deployment/initialize-retail-channels).</span></span>

## <a name="initialize-e-commerce"></a><span data-ttu-id="19be2-115">e コマースの初期化</span><span class="sxs-lookup"><span data-stu-id="19be2-115">Initialize e-commerce</span></span>

<span data-ttu-id="19be2-116">この手順を使用して、既存環境で e コマース機能を初期化します。</span><span class="sxs-lookup"><span data-stu-id="19be2-116">Use this procedure to initialize the e-commerce feature in an existing environment.</span></span>

<span data-ttu-id="19be2-117">開始する前に、次の必要な情報があることを確認してください。</span><span class="sxs-lookup"><span data-stu-id="19be2-117">Before you begin, make sure that you have the following required information:</span></span>

- <span data-ttu-id="19be2-118">使用される RCSU。</span><span class="sxs-lookup"><span data-stu-id="19be2-118">The RCSU that will be used.</span></span>
- <span data-ttu-id="19be2-119">e コマース システムで使用される Microsoft Azure Active Directory セキュリティ グループ。</span><span class="sxs-lookup"><span data-stu-id="19be2-119">The Microsoft Azure Active Directory security group that will be used for e-commerce system admins.</span></span>
- <span data-ttu-id="19be2-120">評価およびレビュー モデレーターで使用される Microsoft Azure Active Directory セキュリティ グループ。</span><span class="sxs-lookup"><span data-stu-id="19be2-120">The Microsoft Azure Active Directory security group that will be used for ratings and reviews moderators.</span></span>
- <span data-ttu-id="19be2-121">環境に関連付けられるドメイン。</span><span class="sxs-lookup"><span data-stu-id="19be2-121">The domains that will be associated with the environment.</span></span>

<span data-ttu-id="19be2-122">さらに、次のオプション情報を収集できます。</span><span class="sxs-lookup"><span data-stu-id="19be2-122">In addition, you can collect the following optional information:</span></span>

- <span data-ttu-id="19be2-123">Azure AD 企業と顧客間 (B2C) 情報:</span><span class="sxs-lookup"><span data-stu-id="19be2-123">Azure AD business-to-consumer (B2C) information:</span></span>

    - <span data-ttu-id="19be2-124">テナント名。</span><span class="sxs-lookup"><span data-stu-id="19be2-124">Tenant Name.</span></span>
    - <span data-ttu-id="19be2-125">クライアント ID。</span><span class="sxs-lookup"><span data-stu-id="19be2-125">Client ID.</span></span>
    - <span data-ttu-id="19be2-126">ログイン カスタム ドメイン。</span><span class="sxs-lookup"><span data-stu-id="19be2-126">Login Custom Domain.</span></span>
    - <span data-ttu-id="19be2-127">返信 URL。</span><span class="sxs-lookup"><span data-stu-id="19be2-127">Reply URL.</span></span>
    - <span data-ttu-id="19be2-128">ポリシー ID のサインアップ サインイン。</span><span class="sxs-lookup"><span data-stu-id="19be2-128">SignUp SignIn Policy ID.</span></span>
    - <span data-ttu-id="19be2-129">リセット パスワード ポリシー ID。</span><span class="sxs-lookup"><span data-stu-id="19be2-129">Reset password Policy ID.</span></span>
    - <span data-ttu-id="19be2-130">プロファイル ポリシー 編集 ID。</span><span class="sxs-lookup"><span data-stu-id="19be2-130">Edit Profile Policy ID.</span></span>

> [!NOTE]
> <span data-ttu-id="19be2-131">この情報は、サービス要求を介して後から追加できます。</span><span class="sxs-lookup"><span data-stu-id="19be2-131">This information can be added later, through a service request.</span></span>

<span data-ttu-id="19be2-132">必要な情報を収集したら、次の手順に従って e コマースを初期化します。</span><span class="sxs-lookup"><span data-stu-id="19be2-132">After you've collected the required information, follow these steps to initialize e-commerce.</span></span>

1. <span data-ttu-id="19be2-133">[LCS](https://lcs.dynamics.com) にサインインします。</span><span class="sxs-lookup"><span data-stu-id="19be2-133">Sign in to [LCS](https://lcs.dynamics.com).</span></span>
1. <span data-ttu-id="19be2-134">e コマースを初期化する環境を含むプロジェクトを開きます。</span><span class="sxs-lookup"><span data-stu-id="19be2-134">Open the project that contains the environment where you want to initialize e-commerce.</span></span>
1. <span data-ttu-id="19be2-135">**環境** セクションで、環境を選択します。</span><span class="sxs-lookup"><span data-stu-id="19be2-135">In the **Environments** section, select the environment.</span></span>
1. <span data-ttu-id="19be2-136">**環境機能** で、**小売管理** のリンクを選択します。</span><span class="sxs-lookup"><span data-stu-id="19be2-136">Under **Environment features**, select the **Retail manage** link.</span></span>
1. <span data-ttu-id="19be2-137">**E コマース** タブで、**設定** を選択します。</span><span class="sxs-lookup"><span data-stu-id="19be2-137">On the **e-Commerce** tab, select **Setup**.</span></span> <span data-ttu-id="19be2-138">ダイアログ ボックスが表示されるので、プロビジョニングに必要な情報を入力します。</span><span class="sxs-lookup"><span data-stu-id="19be2-138">A dialog box appears, where you must enter the information that is required for provisioning.</span></span>
1. <span data-ttu-id="19be2-139">必要な情報を入力し、次のページに進みます。</span><span class="sxs-lookup"><span data-stu-id="19be2-139">Fill in the required information, and then go to the next page.</span></span>
1. <span data-ttu-id="19be2-140">次のページで必要な情報を入力し、フォームを送信します。</span><span class="sxs-lookup"><span data-stu-id="19be2-140">On the next page, fill in the required information, and then submit the form.</span></span> <span data-ttu-id="19be2-141">**E コマース** タブに戻り、初期化が開始されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="19be2-141">You're returned to the **e-Commerce** tab, where you should see that initialization has been started.</span></span>
1. <span data-ttu-id="19be2-142">初期化の状態を表示するには、**更新** もしくは後で **E コマース** タブに戻ります。</span><span class="sxs-lookup"><span data-stu-id="19be2-142">To view the initialization status, either **Refresh** or return to the **e-Commerce** tab later.</span></span>
    
<span data-ttu-id="19be2-143">e コマースが LCS から初期化されると、システムは e コマースに必要な複数のコンポーネントをプロビジョニングし、それらを環境に関連付けます。</span><span class="sxs-lookup"><span data-stu-id="19be2-143">When e-commerce is initialized from LCS, the system provisions several components that are required for e-commerce and associates them with the environment.</span></span> <span data-ttu-id="19be2-144">プロビジョニングが完了すると、**小売管理** ページの **E コマース** タブが更新されて、プロビジョニングが反映されます。</span><span class="sxs-lookup"><span data-stu-id="19be2-144">After provisioning is complete, the **e-Commerce** tab on the **Retail management** page is updated to reflect the provisioning.</span></span> <span data-ttu-id="19be2-145">このページには、最新のカスタマイズ配置と、進行中の他の配置状態が表示されます。</span><span class="sxs-lookup"><span data-stu-id="19be2-145">The page shows the latest customization deployments and the status of any other ongoing deployments.</span></span> <span data-ttu-id="19be2-146">また、e コマース サイトと作成されるサイトの e コマース サイト ビルダーへのリンクも含まれています。</span><span class="sxs-lookup"><span data-stu-id="19be2-146">It also includes links to the e-commerce site and the Commerce site builder where sites are authored.</span></span>

## <a name="access-commerce-site-builder"></a><span data-ttu-id="19be2-147">Commerce のサイト ビルダーへのアクセス</span><span class="sxs-lookup"><span data-stu-id="19be2-147">Access Commerce site builder</span></span>

<span data-ttu-id="19be2-148">Commerce サイト ビルダーにアクセスするには、LCS の **小売管理** ページの **e コマース** タブに移動し、**e コマース サイトの管理ツール** リンクを選択します。</span><span class="sxs-lookup"><span data-stu-id="19be2-148">To access Commerce site builder, go to the **e-Commerce** tab on the **Retail management** page in LCS and select the **e-Commerce site management tool** link.</span></span> <span data-ttu-id="19be2-149">サイト ビルダー ランディング ページには、テナント レベルのビューが表示されます。</span><span class="sxs-lookup"><span data-stu-id="19be2-149">The site builder landing page displays a tenant-level view.</span></span> <span data-ttu-id="19be2-150">このページから次の操作を実行できます。</span><span class="sxs-lookup"><span data-stu-id="19be2-150">From this page, you can:</span></span>

- <span data-ttu-id="19be2-151">テナント レベルの設定を変更します。</span><span class="sxs-lookup"><span data-stu-id="19be2-151">Modify tenant-level settings.</span></span>
- <span data-ttu-id="19be2-152">作成したサイトで、表示するためのアクセス許可を持っているサイトに移動します。</span><span class="sxs-lookup"><span data-stu-id="19be2-152">Navigate to any site you have created, and have permission to view.</span></span> 
- <span data-ttu-id="19be2-153">管理および報告などのレビュー機能にアクセスします。</span><span class="sxs-lookup"><span data-stu-id="19be2-153">Access Reviews features such as moderation and reporting.</span></span>
- <span data-ttu-id="19be2-154">新しいサイトを作成します。</span><span class="sxs-lookup"><span data-stu-id="19be2-154">Create a new site.</span></span> <span data-ttu-id="19be2-155">新しいサイトを作成する方法の詳細については、[新しい e コマース サイトの作成](create-ecommerce-site.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="19be2-155">For more information about how to create a new site, see [Create an e-commerce site](create-ecommerce-site.md) .</span></span> 

## <a name="additional-resources"></a><span data-ttu-id="19be2-156">追加リソース</span><span class="sxs-lookup"><span data-stu-id="19be2-156">Additional resources</span></span>

[<span data-ttu-id="19be2-157">ドメイン名のコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="19be2-157">Configure your domain name</span></span>](configure-your-domain-name.md)

[<span data-ttu-id="19be2-158">eコマース サイトの作成</span><span class="sxs-lookup"><span data-stu-id="19be2-158">Create an e-commerce site</span></span>](create-ecommerce-site.md)

[<span data-ttu-id="19be2-159">オンライン チャンネルと Dynamics 365 Commerce サイトの関連付け</span><span class="sxs-lookup"><span data-stu-id="19be2-159">Associate a Dynamics 365 Commerce site with an online channel</span></span>](associate-site-online-store.md)

[<span data-ttu-id="19be2-160">robots.txt ファイルの管理</span><span class="sxs-lookup"><span data-stu-id="19be2-160">Manage robots.txt files</span></span>](manage-robots-txt-files.md)

[<span data-ttu-id="19be2-161">URL リダイレクトの一括アップロード</span><span class="sxs-lookup"><span data-stu-id="19be2-161">Upload URL redirects in bulk</span></span>](upload-bulk-redirects.md)

[<span data-ttu-id="19be2-162">B2C テナントを Commerce に 設定</span><span class="sxs-lookup"><span data-stu-id="19be2-162">Set up a B2C tenant in Commerce</span></span>](set-up-B2C-tenant.md)

[<span data-ttu-id="19be2-163">ユーザー ログイン用のカスタム ページの設定</span><span class="sxs-lookup"><span data-stu-id="19be2-163">Set up custom pages for user logins</span></span>](custom-pages-user-logins.md)

[<span data-ttu-id="19be2-164">Commerce 環境での複数の B2C テナントのコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="19be2-164">Configure multiple B2C tenants in a Commerce environment</span></span>](configure-multi-B2C-tenants.md)

[<span data-ttu-id="19be2-165">コンテンツ配信ネットワーク (CDN) のサポートの追加</span><span class="sxs-lookup"><span data-stu-id="19be2-165">Add support for a content delivery network (CDN)</span></span>](add-cdn-support.md)

[<span data-ttu-id="19be2-166">場所に基づく店舗検出の有効化</span><span class="sxs-lookup"><span data-stu-id="19be2-166">Enable location-based store detection</span></span>](enable-store-detection.md)
