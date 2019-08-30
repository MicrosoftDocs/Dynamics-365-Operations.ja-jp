---
title: Finance and Operations 実装プロジェクトの配送準備
description: このトピックでは、Microsoft Dynamics Lifecycle Services (LCS) を使用して Microsoft Dynamics 365 for Finance and Operations プロジェクトをオンボードする方法を説明します。
author: ClaudiaBetz-Haubold
manager: AnnBe
ms.date: 08/22/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: IT Pro
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: chaubold
ms.search.validFrom: 2018-01-31
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: 3a77daa442b9aea47926b90daf9bc72c8a7df234
ms.sourcegitcommit: 3f45db0bb1881ee287a41dcc283a304ba7aadab8
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/22/2019
ms.locfileid: "1918232"
---
# <a name="onboard-a-finance-and-operations-implementation-project"></a><span data-ttu-id="a4650-103">Finance and Operations 実装プロジェクトの配送準備</span><span class="sxs-lookup"><span data-stu-id="a4650-103">Onboard a Finance and Operations implementation project</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a4650-104">このトピックでは、Microsoft Dynamics Lifecycle Services (LCS) を使用して Microsoft Dynamics 365 for Finance and Operations プロジェクトをオンボードする方法を説明します。</span><span class="sxs-lookup"><span data-stu-id="a4650-104">This topic describes how to onboard a Microsoft Dynamics 365 for Finance and Operations project by using Microsoft Dynamics Lifecycle Services (LCS).</span></span>

## <a name="microsoft-365-admin-center"></a><span data-ttu-id="a4650-105">Microsoft 365 管理ビュー</span><span class="sxs-lookup"><span data-stu-id="a4650-105">Microsoft 365 Admin Center</span></span>

<span data-ttu-id="a4650-106">あなたの組織がFinance and Operationsのサブスクリプションを購入したら、次の手順を実行するテナントテナント管理者によって、あなたの組織のAzure Active Directory (Azure AD) テナントを有効にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="a4650-106">After your organization has purchased a subscription to Finance and Operations, it must be activated on your organization's Azure Active Directory (Azure AD) tenant by your Tenant Administrator, who completes the following steps:</span></span>

1. <span data-ttu-id="a4650-107">Inprivate/Incognito ブラウズセッションを開いて、[Microsoft 365 管理センター](https://admin.microsoft.com/)に移動します。</span><span class="sxs-lookup"><span data-stu-id="a4650-107">Open an Inprivate/Incognito browser session and go to the [Microsoft 365 Admin Center](https://admin.microsoft.com/).</span></span>
2. <span data-ttu-id="a4650-108">テナント管理者の資格情報を使用してログインします。</span><span class="sxs-lookup"><span data-stu-id="a4650-108">Sign in with the Tenant Administrator credentials.</span></span>
3. <span data-ttu-id="a4650-109">**請求 > サブスクリプション** に移動して、有効な **Dynamics 365 Unified Operations** サブスクリプションがある事を確認してください。</span><span class="sxs-lookup"><span data-stu-id="a4650-109">Go to **Billing > Subscriptions** and confirm that there is an active **Dynamics 365 Unified Operations** subscription.</span></span> 
   > [!NOTE]
   > <span data-ttu-id="a4650-110">サブスクリプションが表示されない場合は、ライセンスパートナーに問い合わせて、サブスクリプショントランザクションの状態と、サブスクリプションのテナントを確認してください。</span><span class="sxs-lookup"><span data-stu-id="a4650-110">If you do not see a subscription, consult with your Licensing Partner to confirm the status of the subscription transaction as well as the tenant for the subscription.</span></span> <span data-ttu-id="a4650-111">既定では、すべてのMicrosoftオンラインサービスが同じAzure ADテナント上で実行されている必要があります。</span><span class="sxs-lookup"><span data-stu-id="a4650-111">By default, all Microsoft Online Services should be running on the same Azure AD tenant.</span></span>
4. <span data-ttu-id="a4650-112">有効な**Dynamics 365 Unified Operations**サブスクリプションが表示されている場合は、LCSにログインして実装のプロジェクト作成フローをトリガーすることにより、次のステップに進むことができます。</span><span class="sxs-lookup"><span data-stu-id="a4650-112">If there is an active **Dynamics 365 Unified Operations** subscription displayed, you can proceed to the next step by signing in to LCS to trigger the Implementation Project creation flow.</span></span>
5. <span data-ttu-id="a4650-113">別のプライベートブラウザータブを開き、[Lifecycle Services](https://lcs.dynamics.com)に移動します。</span><span class="sxs-lookup"><span data-stu-id="a4650-113">Open another private browser tab and go to [Lifecycle Services](https://lcs.dynamics.com).</span></span> <span data-ttu-id="a4650-114">現在のテナント管理者の資格情報を使用してアクセスするには、**ログイン** を選択します。</span><span class="sxs-lookup"><span data-stu-id="a4650-114">Select **Login** to access LCS with your current Tenant Admin credentials.</span></span>
6. <span data-ttu-id="a4650-115">実装プロジェクトのプロビジョニングを完了するために、他の表示されたメッセージを承認して確認します。</span><span class="sxs-lookup"><span data-stu-id="a4650-115">Accept and confirm any other prompts displayed to complete the Implementation Project provisioning.</span></span>
7. <span data-ttu-id="a4650-116">テナント管理者には、プロビジョニングされた実装プロジェクトのプロジェクト所有者セキュリティ ロールが割り当てられます。</span><span class="sxs-lookup"><span data-stu-id="a4650-116">The Tenant Administrator is assigned the Project Owner security role in the provisioned Implementation Project.</span></span>  
   > [!NOTE]
   > <span data-ttu-id="a4650-117">テナント管理者が Finance and Operations の実装に参加していない場合は、最低 1 人の追加プロジェクト所有者を実装プロジェクトに割り当てる必要があります。</span><span class="sxs-lookup"><span data-stu-id="a4650-117">If the Tenant Administrator will not be a participant in the Finance and Operations implementation, at least one additional Project Owner must be assigned to the implementation project.</span></span>

   <span data-ttu-id="a4650-118">ユーザーに割り当てることができるセキュリティ ロールなど、LCS ユーザー管理の概要については、[プロジェクト セキュリティの構成](../../dev-itpro/lifecycle-services/configure-lcs-security.md#configuring-project-security)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="a4650-118">For an overview of LCS user management, including the security roles that can be assigned to users, see [Configuring project security](../../dev-itpro/lifecycle-services/configure-lcs-security.md#configuring-project-security).</span></span>

## <a name="lcs-implementation-project-workspace"></a><span data-ttu-id="a4650-119">LCS 実装プロジェクト ワークスペース</span><span class="sxs-lookup"><span data-stu-id="a4650-119">LCS implementation project workspace</span></span>

<span data-ttu-id="a4650-120">テナント管理者が Finance and Operations サブスクリプションの有効化を完了し、適切なプロジェクト所有者を追加した後、チーム メンバーは **実装プロジェクト** ワークスペースにアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="a4650-120">After the Tenant Administrator has completed the Finance and Operations subscription activation and added additional project owners as appropriate, those team members can access the **Implementation project** workspace.</span></span>

<span data-ttu-id="a4650-121">LCS で完了する最初の手順は、**プロジェクトのオンボード**です。</span><span class="sxs-lookup"><span data-stu-id="a4650-121">The first step to be completed in LCS is **Project onboarding**.</span></span> <span data-ttu-id="a4650-122">この手順は、Microsoft が管理するすべての環境を展開する前に、**2019 年 8 月 22 日 (PST) またはそれ以降**に作成されたすべての LCS 実装プロジェクトに必要です。</span><span class="sxs-lookup"><span data-stu-id="a4650-122">This step is required for all LCS implementation projects that are created **on or after August 22, 2019, PST**, prior to deploying any of the Microsoft-managed environments.</span></span> <span data-ttu-id="a4650-123">**プロジェクトのオンボード**機能には、アクション センターの通知または LCS 実装プロジェクト メニューを使用してアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="a4650-123">You can access the **Project onboarding** feature using the action center notification or the LCS Implementation project menu.</span></span> <span data-ttu-id="a4650-124">LCS の**プロジェクト オンボード**にアクセスするには、プロジェクト所有者セキュリティ ロールに割り当てられている必要があります。</span><span class="sxs-lookup"><span data-stu-id="a4650-124">You must be assigned to the Project owner security role to access **Project onboarding** in LCS.</span></span>

<span data-ttu-id="a4650-125">LCS を開始するには、「[Lifecycle Services for Finance and Operations の顧客](../../dev-itpro/lifecycle-services/lcs-works-lcs.md)」を参照します。</span><span class="sxs-lookup"><span data-stu-id="a4650-125">To get started with LCS, see [Lifecycle Services for Finance and Operations customers](../../dev-itpro/lifecycle-services/lcs-works-lcs.md).</span></span> 

## <a name="fasttrack-onboarding-services"></a><span data-ttu-id="a4650-126">FastTrack オンボード サービス</span><span class="sxs-lookup"><span data-stu-id="a4650-126">FastTrack onboarding services</span></span>

<span data-ttu-id="a4650-127">LCS  **実装プロジェクト** ワークスペースがプロビジョニングされたら、Microsoft FastTrack チームはオンボードの進捗状況を監視します。</span><span class="sxs-lookup"><span data-stu-id="a4650-127">After the LCS **Implementation project** workspace is provisioned, the Microsoft FastTrack team will monitor your onboarding progress.</span></span> <span data-ttu-id="a4650-128">FastTrack プログラムおよび提供サービスの詳細については、[Dynamics 365 の Microsoft FastTrack](../get-started/fasttrack-dynamics-365-overview.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="a4650-128">For more information about the FastTrack program and the services provided, see [Microsoft FastTrack for Dynamics 365](../get-started/fasttrack-dynamics-365-overview.md).</span></span>

<span data-ttu-id="a4650-129">すべてのLCS **実装プロジェクト** は、プロジェクトのオンボードを正常に完了した後に、そのサービスを歓迎する FastTrack チームからの電子メールを受け取ります。</span><span class="sxs-lookup"><span data-stu-id="a4650-129">All LCS **Implementation projects** will receive an email from the FastTrack team welcoming them to the service after they successfully complete the project onboarding.</span></span> <span data-ttu-id="a4650-130">LCS **実装プロジェクト**を作成してから数週間以内にプロジェクトのオンボードを完了しなかった場合、プロジェクト チームにアラームが送信されます。</span><span class="sxs-lookup"><span data-stu-id="a4650-130">If project onboarding is not completed within a few weeks after creating an LCS **Implementation project** creation, a reminder will be sent to the project team.</span></span>

<span data-ttu-id="a4650-131">特定のプロジェクトについては、FastTrack はプロジェクト チームに電子メールを送り、オンボード ミーティング (60 分の会議通話) を提供します。</span><span class="sxs-lookup"><span data-stu-id="a4650-131">For qualifying projects, FastTrack will email the project team offering an onboarding meeting, which is a 60-minute conference call.</span></span> <span data-ttu-id="a4650-132">特定のプロジェクトに関する詳細については、[FastTrack for Finance and Operations の適格性](../get-started/fasttrack-dynamics-365-overview.md#eligibility-for-fasttrack-for-finance-and-operations)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="a4650-132">For more information about qualifying projects, see [Eligibility for FastTrack for Finance and Operations](../get-started/fasttrack-dynamics-365-overview.md#eligibility-for-fasttrack-for-finance-and-operations).</span></span> <span data-ttu-id="a4650-133">オンボード ミーティングはオプションです。</span><span class="sxs-lookup"><span data-stu-id="a4650-133">The onboarding meeting is optional.</span></span> <span data-ttu-id="a4650-134">この通話中に、FastTrack チームは FastTrack プログラムを紹介し、テナントの検証、環境計画、アプリケーション ライフサイクル管理、および運用準備に関する重要なトピックについて説明します。</span><span class="sxs-lookup"><span data-stu-id="a4650-134">During this call, the FastTrack team will introduce the FastTrack program and discuss important topics such as tenant validation, environment planning, application lifecycle management, and go-live readiness.</span></span> <span data-ttu-id="a4650-135">必要に応じて、通話中に**プロジェクトのオンボード**を完了するようチームを支援します。</span><span class="sxs-lookup"><span data-stu-id="a4650-135">If necessary, during the call we will assist the team in completing the **Project onboarding**.</span></span> <span data-ttu-id="a4650-136">プロジェクト マネージャーとデリバリー リーダーのほか、顧客およびパートナーのソリューション設計者がオンボード ミーティングに参加することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="a4650-136">It is suggested that Project managers and Delivery leads as well as Solution Architects from customer and partner participate in the onboarding meeting.</span></span> 
> [!NOTE]
> <span data-ttu-id="a4650-137">FastTrack チームからのオンボードに関連するすべての電子メールは Dynamics 365 Onboarding (<ond365@microsoft.com>) から発信されるので、スパムのブロック/フィルターがこの住所からの電子メールを許可していることを確認してください。</span><span class="sxs-lookup"><span data-stu-id="a4650-137">All onboarding-related emails from the FastTrack team will originate from Dynamics 365 Onboarding (<ond365@microsoft.com>), so please ensure that any spam blocker/filter allows email from this address.</span></span>


## <a name="key-data-to-keep-current-in-lcs"></a><span data-ttu-id="a4650-138">LCS で最新状態にするキー データ</span><span class="sxs-lookup"><span data-stu-id="a4650-138">Key data to keep current in LCS</span></span>

<span data-ttu-id="a4650-139">LCS 実装プロジェクトに主要なプロジェクト メンバー (プロジェクト マネージャーなど) を追加することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="a4650-139">We recommend that you add key project members (such as project managers) to the LCS implementation project.</span></span> <span data-ttu-id="a4650-140">各人の勤務先電子メールを必ず含めるようにしてください。</span><span class="sxs-lookup"><span data-stu-id="a4650-140">Be sure to include each person's work email address.</span></span> <span data-ttu-id="a4650-141">この方法で、お客様と協力して、プロジェクトのメンバーが弊社からの重要な連絡を見逃さないよう保証できます。</span><span class="sxs-lookup"><span data-stu-id="a4650-141">In this way, you help us work best with you and help ensure that project members don't miss important communication from us.</span></span>

<span data-ttu-id="a4650-142">LCSプロジェクトのマイルストーン日付は、必ず最新の状態に保つようにしてください。</span><span class="sxs-lookup"><span data-stu-id="a4650-142">Be sure to keep the milestone dates in your LCS project current.</span></span> <span data-ttu-id="a4650-143">このように、さまざまなプロジェクトステージでお客様と連絡をとれます。</span><span class="sxs-lookup"><span data-stu-id="a4650-143">In this way, you help us connect with you at different project stages.</span></span> <span data-ttu-id="a4650-144">お客様が Go-live 日 により近づいたとき、マイクロソフトは、実稼働環境を配置する前に、プロジェクトの Go-live 評価のためにお客様と連絡を取ります。</span><span class="sxs-lookup"><span data-stu-id="a4650-144">When you're closer to your go-live date, we will contact you for a project Go-live assessment before we deploy your production environment.</span></span>

<span data-ttu-id="a4650-145">マイルストーンの日付は、LCS 実装方法に格納されます。</span><span class="sxs-lookup"><span data-stu-id="a4650-145">Milestone dates are stored in the LCS implementation methodology.</span></span> <span data-ttu-id="a4650-146">詳細については、「顧客向け LCS」トピックの [方法](../../dev-itpro/lifecycle-services/lcs-works-lcs.md#methodologies) セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="a4650-146">For more information, see the [Methodologies](../../dev-itpro/lifecycle-services/lcs-works-lcs.md#methodologies) section of the "LCS for Customers" topic.</span></span>


