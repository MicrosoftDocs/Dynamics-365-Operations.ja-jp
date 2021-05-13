---
title: 新しい eコマース テナントのデプロイ
description: このトピックでは、Microsoft Dynamics Lifecycle Services (LCS) を使用して新しい Dynamics 365 Commerce e コマース サイトをデプロイする方法について説明します。
author: psimolin
ms.date: 07/02/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 6b228babfd32a4191eeed2a6d924a8b99f1a5311
ms.sourcegitcommit: 9eadc7ca08e2db3fd208f5fc835551abe9d06dc8
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/22/2021
ms.locfileid: "5936709"
---
# <a name="deploy-a-new-e-commerce-tenant"></a><span data-ttu-id="9c35b-103">新しい eコマース テナントのデプロイ</span><span class="sxs-lookup"><span data-stu-id="9c35b-103">Deploy a new e-commerce tenant</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="9c35b-104">このトピックでは、Microsoft Dynamics Lifecycle Services (LCS) を使用して新しい Dynamics 365 Commerce e コマース サイトをデプロイする方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="9c35b-104">This topic describes how to deploy a new Dynamics 365 Commerce e-commerce site by using Microsoft Dynamics Lifecycle Services (LCS).</span></span>

<span data-ttu-id="9c35b-105">Microsoft Dynamics Lifecycle Services (LCS) は、パートナーや顧客がプロジェクト環境を管理したり、Microsoft Dynamics 製品や機能に関する最新情報を表示したり、サポート インシデントを作成、追跡、参照したりするために使用できる、クラウドベースのコラボレーション ワークスペースです。</span><span class="sxs-lookup"><span data-stu-id="9c35b-105">Microsoft Dynamics Lifecycle Services (LCS) is a cloud-based collaborative workspace that partners and customers can use to manage their projects and environments, view the latest information about Microsoft Dynamics products and features, and create, track, and browse support incidents.</span></span> <span data-ttu-id="9c35b-106">e コマースの管理機能は LCS に統合されています。</span><span class="sxs-lookup"><span data-stu-id="9c35b-106">E-commerce management features are integrated into LCS.</span></span>

<span data-ttu-id="9c35b-107">LCS の詳細については、[Lifecycle Services ユーザー ガイド](/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="9c35b-107">To learn more about LCS, see the [Lifecycle Services User Guide](/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide).</span></span>
    
## <a name="get-started"></a><span data-ttu-id="9c35b-108">開始する</span><span class="sxs-lookup"><span data-stu-id="9c35b-108">Get started</span></span>

<span data-ttu-id="9c35b-109">e コマースを初期化する前に、プロジェクト、環境、Retail Cloud Scale Unit (RCSU) を初期化する必要があります。</span><span class="sxs-lookup"><span data-stu-id="9c35b-109">Before you can initialize e-commerce, you must initialize a project, an environment, and a Retail Cloud Scale Unit (RCSU).</span></span> <span data-ttu-id="9c35b-110">LCS で初期化を行うには、プロジェクト所有者ロールまたは環境マネージャ ロールのいずれかのアクセス許可が必要です。</span><span class="sxs-lookup"><span data-stu-id="9c35b-110">To do the initialization in LCS, you must have permissions for either the Project Owner or Environment manager role.</span></span> <span data-ttu-id="9c35b-111">実稼働環境とサンドボックス環境のトポロジがサポートされています。</span><span class="sxs-lookup"><span data-stu-id="9c35b-111">The production and sandbox environment topologies are supported.</span></span>

<span data-ttu-id="9c35b-112">環境に関する詳細については、[環境計画](/dynamics365/unified-operations/fin-and-ops/imp-lifecycle/environment-planning)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="9c35b-112">For more information about environments, see [Environment planning](/dynamics365/unified-operations/fin-and-ops/imp-lifecycle/environment-planning).</span></span> <span data-ttu-id="9c35b-113">RCSU の詳細については、[Retail Cloud Scale Unit の初期化](/dynamics365/unified-operations/dev-itpro/deployment/initialize-retail-channels)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="9c35b-113">For more information about RCSU, see [Initialize Retail Cloud Scale Unit](/dynamics365/unified-operations/dev-itpro/deployment/initialize-retail-channels).</span></span>

## <a name="initialize-e-commerce"></a><span data-ttu-id="9c35b-114">e コマースの初期化</span><span class="sxs-lookup"><span data-stu-id="9c35b-114">Initialize e-commerce</span></span>

<span data-ttu-id="9c35b-115">この手順を使用して、既存環境で e コマース機能を初期化します。</span><span class="sxs-lookup"><span data-stu-id="9c35b-115">Use this procedure to initialize the e-commerce feature in an existing environment.</span></span>

<span data-ttu-id="9c35b-116">開始する前に、次の必要な情報があることを確認してください。</span><span class="sxs-lookup"><span data-stu-id="9c35b-116">Before you begin, make sure that you have the following required information:</span></span>

- <span data-ttu-id="9c35b-117">使用される RCSU。</span><span class="sxs-lookup"><span data-stu-id="9c35b-117">The RCSU that will be used.</span></span>
- <span data-ttu-id="9c35b-118">e コマース システムで使用される Microsoft Azure Active Directory セキュリティ グループ。</span><span class="sxs-lookup"><span data-stu-id="9c35b-118">The Microsoft Azure Active Directory security group that will be used for e-commerce system admins.</span></span>
- <span data-ttu-id="9c35b-119">評価およびレビュー モデレーターで使用される Microsoft Azure Active Directory セキュリティ グループ。</span><span class="sxs-lookup"><span data-stu-id="9c35b-119">The Microsoft Azure Active Directory security group that will be used for ratings and reviews moderators.</span></span>
- <span data-ttu-id="9c35b-120">環境に関連付けられるドメイン。</span><span class="sxs-lookup"><span data-stu-id="9c35b-120">The domains that will be associated with the environment.</span></span>

<span data-ttu-id="9c35b-121">さらに、次のオプション情報を収集できます。</span><span class="sxs-lookup"><span data-stu-id="9c35b-121">In addition, you can collect the following optional information:</span></span>

- <span data-ttu-id="9c35b-122">Azure AD 企業と顧客間 (B2C) 情報:</span><span class="sxs-lookup"><span data-stu-id="9c35b-122">Azure AD business-to-consumer (B2C) information:</span></span>

    - <span data-ttu-id="9c35b-123">テナント名。</span><span class="sxs-lookup"><span data-stu-id="9c35b-123">Tenant Name.</span></span>
    - <span data-ttu-id="9c35b-124">クライアント ID。</span><span class="sxs-lookup"><span data-stu-id="9c35b-124">Client ID.</span></span>
    - <span data-ttu-id="9c35b-125">ログイン カスタム ドメイン。</span><span class="sxs-lookup"><span data-stu-id="9c35b-125">Login Custom Domain.</span></span>
    - <span data-ttu-id="9c35b-126">返信 URL。</span><span class="sxs-lookup"><span data-stu-id="9c35b-126">Reply URL.</span></span>
    - <span data-ttu-id="9c35b-127">ポリシー ID のサインアップ サインイン。</span><span class="sxs-lookup"><span data-stu-id="9c35b-127">SignUp SignIn Policy ID.</span></span>
    - <span data-ttu-id="9c35b-128">リセット パスワード ポリシー ID。</span><span class="sxs-lookup"><span data-stu-id="9c35b-128">Reset password Policy ID.</span></span>
    - <span data-ttu-id="9c35b-129">プロファイル ポリシー 編集 ID。</span><span class="sxs-lookup"><span data-stu-id="9c35b-129">Edit Profile Policy ID.</span></span>

> [!NOTE]
> <span data-ttu-id="9c35b-130">この情報は、サービス要求を介して後から追加できます。</span><span class="sxs-lookup"><span data-stu-id="9c35b-130">This information can be added later, through a service request.</span></span>

<span data-ttu-id="9c35b-131">必要な情報を収集したら、次の手順に従って e コマースを初期化します。</span><span class="sxs-lookup"><span data-stu-id="9c35b-131">After you've collected the required information, follow these steps to initialize e-commerce.</span></span>

1. <span data-ttu-id="9c35b-132">[LCS](https://lcs.dynamics.com) にサインインします。</span><span class="sxs-lookup"><span data-stu-id="9c35b-132">Sign in to [LCS](https://lcs.dynamics.com).</span></span>
1. <span data-ttu-id="9c35b-133">e コマースを初期化する環境を含むプロジェクトを開きます。</span><span class="sxs-lookup"><span data-stu-id="9c35b-133">Open the project that contains the environment where you want to initialize e-commerce.</span></span>
1. <span data-ttu-id="9c35b-134">**環境** セクションで、環境を選択します。</span><span class="sxs-lookup"><span data-stu-id="9c35b-134">In the **Environments** section, select the environment.</span></span>
1. <span data-ttu-id="9c35b-135">**環境機能** で、**小売管理** のリンクを選択します。</span><span class="sxs-lookup"><span data-stu-id="9c35b-135">Under **Environment features**, select the **Retail manage** link.</span></span>
1. <span data-ttu-id="9c35b-136">**E コマース** タブで、**設定** を選択します。</span><span class="sxs-lookup"><span data-stu-id="9c35b-136">On the **e-Commerce** tab, select **Setup**.</span></span> <span data-ttu-id="9c35b-137">ダイアログ ボックスが表示されるので、プロビジョニングに必要な情報を入力します。</span><span class="sxs-lookup"><span data-stu-id="9c35b-137">A dialog box appears, where you must enter the information that is required for provisioning.</span></span>
1. <span data-ttu-id="9c35b-138">必要な情報を入力し、次のページに進みます。</span><span class="sxs-lookup"><span data-stu-id="9c35b-138">Fill in the required information, and then go to the next page.</span></span>
1. <span data-ttu-id="9c35b-139">次のページで必要な情報を入力し、フォームを送信します。</span><span class="sxs-lookup"><span data-stu-id="9c35b-139">On the next page, fill in the required information, and then submit the form.</span></span> <span data-ttu-id="9c35b-140">**E コマース** タブに戻り、初期化が開始されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="9c35b-140">You're returned to the **e-Commerce** tab, where you should see that initialization has been started.</span></span>
1. <span data-ttu-id="9c35b-141">初期化の状態を表示するには、**更新** もしくは後で **E コマース** タブに戻ります。</span><span class="sxs-lookup"><span data-stu-id="9c35b-141">To view the initialization status, either **Refresh** or return to the **e-Commerce** tab later.</span></span>
    
<span data-ttu-id="9c35b-142">e コマースが LCS から初期化されると、システムは e コマースに必要な複数のコンポーネントをプロビジョニングし、それらを環境に関連付けます。</span><span class="sxs-lookup"><span data-stu-id="9c35b-142">When e-commerce is initialized from LCS, the system provisions several components that are required for e-commerce and associates them with the environment.</span></span> <span data-ttu-id="9c35b-143">プロビジョニングが完了すると、**小売管理** ページの **E コマース** タブが更新されて、プロビジョニングが反映されます。</span><span class="sxs-lookup"><span data-stu-id="9c35b-143">After provisioning is complete, the **e-Commerce** tab on the **Retail management** page is updated to reflect the provisioning.</span></span> <span data-ttu-id="9c35b-144">このページには、最新のカスタマイズ配置と、進行中の他の配置状態が表示されます。</span><span class="sxs-lookup"><span data-stu-id="9c35b-144">The page shows the latest customization deployments and the status of any other ongoing deployments.</span></span> <span data-ttu-id="9c35b-145">また、e コマース サイトと作成されるサイトの e コマース サイト ビルダーへのリンクも含まれています。</span><span class="sxs-lookup"><span data-stu-id="9c35b-145">It also includes links to the e-commerce site and the Commerce site builder where sites are authored.</span></span>

## <a name="access-commerce-site-builder"></a><span data-ttu-id="9c35b-146">Commerce のサイト ビルダーへのアクセス</span><span class="sxs-lookup"><span data-stu-id="9c35b-146">Access Commerce site builder</span></span>

<span data-ttu-id="9c35b-147">Commerce サイト ビルダーにアクセスするには、LCS の **小売管理** ページの **e コマース** タブに移動し、**e コマース サイトの管理ツール** リンクを選択します。</span><span class="sxs-lookup"><span data-stu-id="9c35b-147">To access Commerce site builder, go to the **e-Commerce** tab on the **Retail management** page in LCS and select the **e-Commerce site management tool** link.</span></span> <span data-ttu-id="9c35b-148">サイト ビルダー ランディング ページには、テナント レベルのビューが表示されます。</span><span class="sxs-lookup"><span data-stu-id="9c35b-148">The site builder landing page displays a tenant-level view.</span></span> <span data-ttu-id="9c35b-149">このページから次の操作を実行できます。</span><span class="sxs-lookup"><span data-stu-id="9c35b-149">From this page, you can:</span></span>

- <span data-ttu-id="9c35b-150">テナント レベルの設定を変更します。</span><span class="sxs-lookup"><span data-stu-id="9c35b-150">Modify tenant-level settings.</span></span>
- <span data-ttu-id="9c35b-151">作成したサイトで、表示するためのアクセス許可を持っているサイトに移動します。</span><span class="sxs-lookup"><span data-stu-id="9c35b-151">Navigate to any site you have created, and have permission to view.</span></span> 
- <span data-ttu-id="9c35b-152">管理および報告などのレビュー機能にアクセスします。</span><span class="sxs-lookup"><span data-stu-id="9c35b-152">Access Reviews features such as moderation and reporting.</span></span>
- <span data-ttu-id="9c35b-153">新しいサイトを作成します。</span><span class="sxs-lookup"><span data-stu-id="9c35b-153">Create a new site.</span></span> <span data-ttu-id="9c35b-154">新しいサイトを作成する方法の詳細については、[新しい e コマース サイトの作成](create-ecommerce-site.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="9c35b-154">For more information about how to create a new site, see [Create an e-commerce site](create-ecommerce-site.md) .</span></span> 

## <a name="additional-resources"></a><span data-ttu-id="9c35b-155">追加リソース</span><span class="sxs-lookup"><span data-stu-id="9c35b-155">Additional resources</span></span>

[<span data-ttu-id="9c35b-156">ドメイン名のコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="9c35b-156">Configure your domain name</span></span>](configure-your-domain-name.md)

[<span data-ttu-id="9c35b-157">eコマース サイトの作成</span><span class="sxs-lookup"><span data-stu-id="9c35b-157">Create an e-commerce site</span></span>](create-ecommerce-site.md)

[<span data-ttu-id="9c35b-158">オンライン チャンネルと Dynamics 365 Commerce サイトの関連付け</span><span class="sxs-lookup"><span data-stu-id="9c35b-158">Associate a Dynamics 365 Commerce site with an online channel</span></span>](associate-site-online-store.md)

[<span data-ttu-id="9c35b-159">robots.txt ファイルの管理</span><span class="sxs-lookup"><span data-stu-id="9c35b-159">Manage robots.txt files</span></span>](manage-robots-txt-files.md)

[<span data-ttu-id="9c35b-160">URL リダイレクトの一括アップロード</span><span class="sxs-lookup"><span data-stu-id="9c35b-160">Upload URL redirects in bulk</span></span>](upload-bulk-redirects.md)

[<span data-ttu-id="9c35b-161">B2C テナントを Commerce に 設定</span><span class="sxs-lookup"><span data-stu-id="9c35b-161">Set up a B2C tenant in Commerce</span></span>](set-up-B2C-tenant.md)

[<span data-ttu-id="9c35b-162">ユーザー ログイン用のカスタム ページの設定</span><span class="sxs-lookup"><span data-stu-id="9c35b-162">Set up custom pages for user logins</span></span>](custom-pages-user-logins.md)

[<span data-ttu-id="9c35b-163">Commerce 環境での複数の B2C テナントのコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="9c35b-163">Configure multiple B2C tenants in a Commerce environment</span></span>](configure-multi-B2C-tenants.md)

[<span data-ttu-id="9c35b-164">コンテンツ配信ネットワーク (CDN) のサポートの追加</span><span class="sxs-lookup"><span data-stu-id="9c35b-164">Add support for a content delivery network (CDN)</span></span>](add-cdn-support.md)

[<span data-ttu-id="9c35b-165">場所に基づく店舗検出の有効化</span><span class="sxs-lookup"><span data-stu-id="9c35b-165">Enable location-based store detection</span></span>](enable-store-detection.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]