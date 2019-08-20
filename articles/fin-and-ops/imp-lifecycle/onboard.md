---
title: Finance and Operations 実装プロジェクトの配送準備
description: このトピックでは、Microsoft Dynamics Lifecycle Services (LCS) を使用して Microsoft Dynamics 365 for Finance and Operations プロジェクトをオンボードする方法を説明します。
author: ClaudiaBetz-Haubold
manager: AnnBe
ms.date: 07/29/2019
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
ms.openlocfilehash: 36492b812ed7df813ef8ac8d0bea0679f6317c37
ms.sourcegitcommit: 16bfa0fd08feec1647829630401ce62ce2ffa1a4
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/02/2019
ms.locfileid: "1850765"
---
# <a name="onboard-a-finance-and-operations-implementation-project"></a><span data-ttu-id="f10b8-103">Finance and Operations 実装プロジェクトの配送準備</span><span class="sxs-lookup"><span data-stu-id="f10b8-103">Onboard a Finance and Operations implementation project</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f10b8-104">このトピックでは、Microsoft Dynamics Lifecycle Services (LCS) を使用して Microsoft Dynamics 365 for Finance and Operations プロジェクトをオンボードする方法を説明します。</span><span class="sxs-lookup"><span data-stu-id="f10b8-104">This topic describes how to onboard a Microsoft Dynamics 365 for Finance and Operations project by using Microsoft Dynamics Lifecycle Services (LCS).</span></span>

## <a name="microsoft-365-admin-center"></a><span data-ttu-id="f10b8-105">Microsoft 365 管理ビュー</span><span class="sxs-lookup"><span data-stu-id="f10b8-105">Microsoft 365 Admin Center</span></span>

<span data-ttu-id="f10b8-106">あなたの組織がFinance and Operationsのサブスクリプションを購入したら、次の手順を実行するテナントテナント管理者によって、あなたの組織のAzure Active Directory (Azure AD) テナントを有効にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="f10b8-106">After your organization has purchased a subscription to Finance and Operations, it must be activated on your organization's Azure Active Directory (Azure AD) tenant by your Tenant Administrator, who completes the following steps:</span></span>

1. <span data-ttu-id="f10b8-107">Inprivate/Incognito ブラウズセッションを開いて、[Microsoft 365 管理センター](https://admin.microsoft.com/)に移動します。</span><span class="sxs-lookup"><span data-stu-id="f10b8-107">Open an Inprivate/Incognito browser session and go to the [Microsoft 365 Admin Center](https://admin.microsoft.com/).</span></span>
2. <span data-ttu-id="f10b8-108">テナント管理者の資格情報を使用してログインします。</span><span class="sxs-lookup"><span data-stu-id="f10b8-108">Sign in with the Tenant Administrator credentials.</span></span>
3. <span data-ttu-id="f10b8-109">**請求 > サブスクリプション** に移動して、有効な **Dynamics 365 Unified Operations** サブスクリプションがある事を確認してください。</span><span class="sxs-lookup"><span data-stu-id="f10b8-109">Go to **Billing > Subscriptions** and confirm that there is an active **Dynamics 365 Unified Operations** subscription.</span></span> 
   > [!NOTE]
   > <span data-ttu-id="f10b8-110">サブスクリプションが表示されない場合は、ライセンスパートナーに問い合わせて、サブスクリプショントランザクションの状態と、サブスクリプションのテナントを確認してください。</span><span class="sxs-lookup"><span data-stu-id="f10b8-110">If you do not see a subscription, consult with your Licensing Partner to confirm the status of the subscription transaction as well as the tenant for the subscription.</span></span> <span data-ttu-id="f10b8-111">既定では、すべてのMicrosoftオンラインサービスが同じAzure ADテナント上で実行されている必要があります。</span><span class="sxs-lookup"><span data-stu-id="f10b8-111">By default, all Microsoft Online Services should be running on the same Azure AD tenant.</span></span>
4. <span data-ttu-id="f10b8-112">有効な**Dynamics 365 Unified Operations**サブスクリプションが表示されている場合は、LCSにログインして実装のプロジェクト作成フローをトリガーすることにより、次のステップに進むことができます。</span><span class="sxs-lookup"><span data-stu-id="f10b8-112">If there is an active **Dynamics 365 Unified Operations** subscription displayed, you can proceed to the next step by signing in to LCS to trigger the Implementation Project creation flow.</span></span>
5. <span data-ttu-id="f10b8-113">別のプライベートブラウザータブを開き、[Lifecycle Services](https://lcs.dynamics.com)に移動します。</span><span class="sxs-lookup"><span data-stu-id="f10b8-113">Open another private browser tab and go to [Lifecycle Services](https://lcs.dynamics.com).</span></span> <span data-ttu-id="f10b8-114">現在のテナント管理者の資格情報を使用してアクセスするには、**ログイン** を選択します。</span><span class="sxs-lookup"><span data-stu-id="f10b8-114">Select **Login** to access LCS with your current Tenant Admin credentials.</span></span>
6. <span data-ttu-id="f10b8-115">実装プロジェクトのプロビジョニングを完了するために、他の表示されたメッセージを承認して確認します。</span><span class="sxs-lookup"><span data-stu-id="f10b8-115">Accept and confirm any other prompts displayed to complete the Implementation Project provisioning.</span></span>
7. <span data-ttu-id="f10b8-116">テナント管理者には、プロビジョニングされた実装プロジェクトにプロジェクト所有者が割り当てられます。</span><span class="sxs-lookup"><span data-stu-id="f10b8-116">The Tenant Administrator is assigned the Project Owner to the provisioned Implementation Project.</span></span> <span data-ttu-id="f10b8-117">最後の手順として、テナント管理者は、Dynamics 365 for Finance and Operations 実装に参加するその他の組織やパートナーチームメンバーを追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="f10b8-117">As a final step, the Tenant Administrator must add additional organization and/or partner team members who will be participating in the Dynamics 365 for Finance and Operations implementation.</span></span> <span data-ttu-id="f10b8-118">これは、LCS 実装プロジェクトメニューから選択された LCS プロジェクトユーザー管理で実行されます。</span><span class="sxs-lookup"><span data-stu-id="f10b8-118">This is performed in LCS Project User Management, selected from the LCS Implementation Project menu.</span></span>

   ![LCS プロジェクト ユーザー管理](./media/LCSProjectUsersMenu.PNG)
   > [!NOTE]
   > <span data-ttu-id="f10b8-120">テナント管理者が Finance and Operations の実装に参加していない場合は、追加のプロジェクト所有者を実装プロジェクトに割り当てる必要があります。</span><span class="sxs-lookup"><span data-stu-id="f10b8-120">If the Tenant Administrator will not be a participant in the Finance and Operations implementation, an additional Project Owner must be assigned to the implementation project.</span></span>

   <span data-ttu-id="f10b8-121">ユーザーに割り当てることができるセキュリティロールの概要については、[プロジェクトセキュリティの構成](../../dev-itpro/lifecycle-services/configure-lcs-security.md#configuring-project-security)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="f10b8-121">For an overview of the security roles that can be assigned to users, see [Configuring project security](../../dev-itpro/lifecycle-services/configure-lcs-security.md#configuring-project-security).</span></span>

## <a name="lcs-implementation-project-workspace"></a><span data-ttu-id="f10b8-122">LCS 実装プロジェクト ワークスペース</span><span class="sxs-lookup"><span data-stu-id="f10b8-122">LCS implementation project workspace</span></span>

<span data-ttu-id="f10b8-123">テナント管理者が Finance and Operations サブスクリプションの有効化を完了し、適切なユーザーを追加した後、チームメンバーは**実装プロジェクト**にアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="f10b8-123">After the Tenant Administrator has completed the Finance and Operations subscription activation and added the appropriate users, team members can access the **Implementation project** workspace.</span></span> 

<span data-ttu-id="f10b8-124">LCS を開始するには、「[Lifecycle Services for Finance and Operations の顧客](../../dev-itpro/lifecycle-services/lcs-works-lcs.md)」を参照します。</span><span class="sxs-lookup"><span data-stu-id="f10b8-124">To get started with LCS, see [Lifecycle Services for Finance and Operations customers](../../dev-itpro/lifecycle-services/lcs-works-lcs.md).</span></span> 

## <a name="fasttrack-onboarding-services"></a><span data-ttu-id="f10b8-125">FastTrack オンボード サービス</span><span class="sxs-lookup"><span data-stu-id="f10b8-125">FastTrack onboarding services</span></span>

<span data-ttu-id="f10b8-126">LCS **実装プロジェクト** ワークスペースがプロビジョニングされた後、Microsoft FastTrack チームはプロジェクト チームに電子メールしてオンボーディング サービスについて議論するための呼出を要求します。</span><span class="sxs-lookup"><span data-stu-id="f10b8-126">After the LCS **Implementation project** workspace is provisioned, the Microsoft FastTrack team will email the project team to request a call to discuss onboarding services.</span></span> <span data-ttu-id="f10b8-127">(この電子メールはond365@microsoft.comから発信されるので、スパムのブロック/フィルタがこのアドレスからの電子メールを許可していることを確認してください。) FastTrackプログラムと提供されるサービスの詳細については[Microsoft FastTrack for Dynamics 365](../get-started/fasttrack-dynamics-365-overview.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="f10b8-127">(Note that this email will originate from ond365@microsoft.com, so please ensure that any spam blocker/filter allows email from this address.) For more information about the FastTrack program and the services provided, see [Microsoft FastTrack for Dynamics 365](../get-started/fasttrack-dynamics-365-overview.md).</span></span>

<span data-ttu-id="f10b8-128">FastTrack Onboarding ミーティングは60分の会議通話です。</span><span class="sxs-lookup"><span data-stu-id="f10b8-128">The FastTrack Onboarding meeting is a 60-minute conference call.</span></span> <span data-ttu-id="f10b8-129">呼び出し中に、チームは FastTrack プログラムへ実装チームを紹介し、LCS プロジェクトおよび関連するタスクの初期構成の支援をおこないます。</span><span class="sxs-lookup"><span data-stu-id="f10b8-129">During this call, the team will introduce the implementation team to the FastTrack program as well as assist with the initial configuration of the LCS project and related tasks:</span></span>

- <span data-ttu-id="f10b8-130">Tenant 検証</span><span class="sxs-lookup"><span data-stu-id="f10b8-130">Tenant validation</span></span>
- <span data-ttu-id="f10b8-131">LCS の概要</span><span class="sxs-lookup"><span data-stu-id="f10b8-131">Introduction to LCS</span></span>
- <span data-ttu-id="f10b8-132">LCS プロジェクト ユーザーの設定</span><span class="sxs-lookup"><span data-stu-id="f10b8-132">Setup of LCS project users</span></span>
- <span data-ttu-id="f10b8-133">Microsoft Azure DevOps の設定</span><span class="sxs-lookup"><span data-stu-id="f10b8-133">Setup of Microsoft Azure DevOps</span></span>
- <span data-ttu-id="f10b8-134">サブスクリプション見積もりツール/使用状況プロファイラー</span><span class="sxs-lookup"><span data-stu-id="f10b8-134">Subscription estimator/Usage profiler</span></span>
- <span data-ttu-id="f10b8-135">環境計画</span><span class="sxs-lookup"><span data-stu-id="f10b8-135">Environment planning</span></span>
- <span data-ttu-id="f10b8-136">環境配置</span><span class="sxs-lookup"><span data-stu-id="f10b8-136">Environment deployment</span></span>
- <span data-ttu-id="f10b8-137">サービスの概要、サポート、サービスの正常性</span><span class="sxs-lookup"><span data-stu-id="f10b8-137">Introduction to servicing, support, and service health</span></span>
- <span data-ttu-id="f10b8-138">プランの準備</span><span class="sxs-lookup"><span data-stu-id="f10b8-138">Readiness planning</span></span>

<span data-ttu-id="f10b8-139">次に示すプロジェクト ロールの参加者ーはこのオンボード ミーティングに参加することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="f10b8-139">It is suggested that the following project roles participate in the onboarding meeting.</span></span> <span data-ttu-id="f10b8-140">その他のロールはオプションです。</span><span class="sxs-lookup"><span data-stu-id="f10b8-140">Other roles are optional.</span></span>

<span data-ttu-id="f10b8-141">**顧客**</span><span class="sxs-lookup"><span data-stu-id="f10b8-141">**Customer**</span></span>

- <span data-ttu-id="f10b8-142">プロジェクト所有者</span><span class="sxs-lookup"><span data-stu-id="f10b8-142">Project owner</span></span>
- <span data-ttu-id="f10b8-143">Microsoft ビジネス センターの管理者、ライセンスが Microsoft とのボリューム サービス契約を通じて調達された場合</span><span class="sxs-lookup"><span data-stu-id="f10b8-143">Microsoft Business Center administrator, if the license was procured through a Volume Service agreement with Microsoft</span></span>

<span data-ttu-id="f10b8-144">**パートナー**</span><span class="sxs-lookup"><span data-stu-id="f10b8-144">**Partner**</span></span>

- <span data-ttu-id="f10b8-145">デリバリー リード/ソリューション アーキテクト</span><span class="sxs-lookup"><span data-stu-id="f10b8-145">Delivery lead/solution architect</span></span>
- <span data-ttu-id="f10b8-146">プロジェクト マネージャー</span><span class="sxs-lookup"><span data-stu-id="f10b8-146">Project manager</span></span>

## <a name="key-data-to-keep-current-in-lcs"></a><span data-ttu-id="f10b8-147">LCS で最新状態にするキー データ</span><span class="sxs-lookup"><span data-stu-id="f10b8-147">Key data to keep current in LCS</span></span>

<span data-ttu-id="f10b8-148">LCS 実装プロジェクトに主要なプロジェクト メンバー (プロジェクト マネージャーなど) を追加することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="f10b8-148">We recommend that you add key project members (such as project managers) to the LCS implementation project.</span></span> <span data-ttu-id="f10b8-149">各人の勤務先電子メールを必ず含めるようにしてください。</span><span class="sxs-lookup"><span data-stu-id="f10b8-149">Be sure to include each person's work email address.</span></span> <span data-ttu-id="f10b8-150">この方法で、お客様と協力して、プロジェクトのメンバーが弊社からの重要な連絡を見逃さないよう保証できます。</span><span class="sxs-lookup"><span data-stu-id="f10b8-150">In this way, you help us work best with you and help ensure that project members don't miss important communication from us.</span></span>

<span data-ttu-id="f10b8-151">LCSプロジェクトのマイルストーン日付は、必ず最新の状態に保つようにしてください。</span><span class="sxs-lookup"><span data-stu-id="f10b8-151">Be sure to keep the milestone dates in your LCS project current.</span></span> <span data-ttu-id="f10b8-152">このように、さまざまなプロジェクトステージでお客様と連絡をとれます。</span><span class="sxs-lookup"><span data-stu-id="f10b8-152">In this way, you help us connect with you at different project stages.</span></span> <span data-ttu-id="f10b8-153">お客様が Go-live 日 により近づいたとき、マイクロソフトは、実稼働環境を配置する前に、プロジェクトの Go-live 評価のためにお客様と連絡を取ります。</span><span class="sxs-lookup"><span data-stu-id="f10b8-153">When you're closer to your go-live date, we will contact you for a project Go-live assessment before we deploy your production environment.</span></span>

<span data-ttu-id="f10b8-154">マイルストーンの日付は、LCS 実装方法に格納されます。</span><span class="sxs-lookup"><span data-stu-id="f10b8-154">Milestone dates are stored in the LCS implementation methodology.</span></span> <span data-ttu-id="f10b8-155">詳細については、「顧客向け LCS」トピックの [方法](../../dev-itpro/lifecycle-services/lcs-works-lcs.md#methodologies) セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="f10b8-155">For more information, see the [Methodologies](../../dev-itpro/lifecycle-services/lcs-works-lcs.md#methodologies) section of the "LCS for Customers" topic.</span></span>

<span data-ttu-id="f10b8-156">オンボーディング呼び出しはオプションのサービスです。</span><span class="sxs-lookup"><span data-stu-id="f10b8-156">The onboarding call is an optional service.</span></span> <span data-ttu-id="f10b8-157">Finance and Operations の実装を理解しているパートナーは、FastTrack チームのサポートがなくても顧客と共にタスクを処理できます。</span><span class="sxs-lookup"><span data-stu-id="f10b8-157">Partners who are experienced with Finance and Operations implementations can work through the tasks with their customers without the help of the FastTrack team.</span></span> <span data-ttu-id="f10b8-158">そのような場合、プロジェクト ユーザーおよびマイルストーン日付を最新にしておくことが特に重要です。</span><span class="sxs-lookup"><span data-stu-id="f10b8-158">In these cases, it's especially important that you keep the project users and milestone dates current.</span></span>
