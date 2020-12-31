---
title: 実装プロジェクトの研修
description: このトピックでは、Microsoft Dynamics Lifecycle Services (LCS) を使用してプロジェクトをオンボードする方法を説明します。
author: ClaudiaBetz-Haubold
manager: AnnBe
ms.date: 05/21/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: chaubold
ms.search.validFrom: 2018-01-31
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: 8ef65a5a51ad1752083835604f86978fbb095ed9
ms.sourcegitcommit: f5e31c34640add6d40308ac1365cc0ee60e60e24
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/08/2020
ms.locfileid: "4694405"
---
# <a name="onboard-an-implementation-project"></a><span data-ttu-id="a555c-103">実装プロジェクトの研修</span><span class="sxs-lookup"><span data-stu-id="a555c-103">Onboard an implementation project</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a555c-104">このトピックでは、Microsoft Dynamics Lifecycle Services (LCS) を使用して Finance and Operations プロジェクトをオンボードする方法を説明します。</span><span class="sxs-lookup"><span data-stu-id="a555c-104">This topic describes how to onboard a Finance and Operations project by using Microsoft Dynamics Lifecycle Services (LCS).</span></span>

## <a name="microsoft-365-admin-center"></a><span data-ttu-id="a555c-105">Microsoft 365 管理ビュー</span><span class="sxs-lookup"><span data-stu-id="a555c-105">Microsoft 365 Admin Center</span></span>

<span data-ttu-id="a555c-106">組織が Finance and Operations のサブスクリプションを購入したら、テナント管理者は、組織の Azure Active Directory (Azure AD) テナントを有効にし、次の手順を完了する必要があります。</span><span class="sxs-lookup"><span data-stu-id="a555c-106">After your organization has purchased a subscription to Finance and Operations, it must be activated on your organization's Azure Active Directory (Azure AD) tenant by your Tenant Administrator, who completes the following steps:</span></span>

1. <span data-ttu-id="a555c-107">InPrivate/Incognito ブラウズ セッションを開いて、[Microsoft 365 管理センター](https://admin.microsoft.com/) に移動します。</span><span class="sxs-lookup"><span data-stu-id="a555c-107">Open an InPrivate/Incognito browser session and go to the [Microsoft 365 Admin Center](https://admin.microsoft.com/).</span></span>
2. <span data-ttu-id="a555c-108">テナント管理者の資格情報を使用してログインします。</span><span class="sxs-lookup"><span data-stu-id="a555c-108">Sign in with the Tenant Administrator credentials.</span></span>
3. <span data-ttu-id="a555c-109">**請求 > 製品 & サービス** に移動して、配置するアプリケーションに対して有効なサブスクリプションがあることを確認します。</span><span class="sxs-lookup"><span data-stu-id="a555c-109">Go to **Billing > Products & services** and confirm that there is an active subscription for the application that you want to deploy.</span></span> 
   > [!NOTE]
   > <span data-ttu-id="a555c-110">有効なサブスクリプションが表示されない場合は、ライセンス パートナーに問い合わせて、サブスクリプション トランザクションの状態と、サブスクリプションのテナントを確認してください。</span><span class="sxs-lookup"><span data-stu-id="a555c-110">If you do not see an active subscription, consult with your Licensing Partner to confirm the status of the subscription transaction as well as the tenant for the subscription.</span></span> <span data-ttu-id="a555c-111">既定では、すべてのMicrosoftオンラインサービスが同じAzure ADテナント上で実行されている必要があります。</span><span class="sxs-lookup"><span data-stu-id="a555c-111">By default, all Microsoft Online Services should be running on the same Azure AD tenant.</span></span>
4. <span data-ttu-id="a555c-112">問題のサブスクリプションが有効と表示されている場合は、LCS にサインインして実装のプロジェクト作成フローをトリガーすることにより、次のステップに進むことができます。</span><span class="sxs-lookup"><span data-stu-id="a555c-112">If the subscription in question is shown as active, proceed to the next step by signing in to LCS to trigger the Implementation Project creation flow.</span></span>
5. <span data-ttu-id="a555c-113">別のプライベートブラウザータブを開き、[Lifecycle Services](https://lcs.dynamics.com)に移動します。</span><span class="sxs-lookup"><span data-stu-id="a555c-113">Open another private browser tab and go to [Lifecycle Services](https://lcs.dynamics.com).</span></span> <span data-ttu-id="a555c-114">現在のテナント管理者の資格情報を使用してアクセスするには、**ログイン** を選択します。</span><span class="sxs-lookup"><span data-stu-id="a555c-114">Select **Login** to access LCS with your current Tenant Admin credentials.</span></span>
6. <span data-ttu-id="a555c-115">実装プロジェクトのプロビジョニングを完了するために、他の表示されたメッセージを承認して確認します。</span><span class="sxs-lookup"><span data-stu-id="a555c-115">Accept and confirm any other prompts displayed to complete the Implementation Project provisioning.</span></span>
7. <span data-ttu-id="a555c-116">テナント管理者には、プロビジョニングされた実装プロジェクトのプロジェクト所有者セキュリティ ロールが割り当てられます。</span><span class="sxs-lookup"><span data-stu-id="a555c-116">The Tenant Administrator is assigned the Project Owner security role in the provisioned Implementation Project.</span></span>  
   > [!NOTE]
   > <span data-ttu-id="a555c-117">テナント管理者が実装に参加していない場合は、少なくとも 1 人の追加のプロジェクト所有者を実装プロジェクトに割り当てる必要があります。</span><span class="sxs-lookup"><span data-stu-id="a555c-117">If the Tenant Administrator will not be a participant in the implementation, at least one additional Project Owner must be assigned to the implementation project.</span></span>

   <span data-ttu-id="a555c-118">ユーザーに割り当てることができるセキュリティ ロールを含む、LCS ユーザー管理の概要については、 [Lifecycle Services (LCS) のセキュリティのコンフィギュレーション](../../dev-itpro/lifecycle-services/configure-lcs-security.md#configuring-project-security) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="a555c-118">For an overview of LCS user management, including the security roles that can be assigned to users, see [Configure Lifecycle Services (LCS) security](../../dev-itpro/lifecycle-services/configure-lcs-security.md#configuring-project-security).</span></span>

## <a name="lcs-implementation-project-workspace"></a><span data-ttu-id="a555c-119">LCS 実装プロジェクト ワークスペース</span><span class="sxs-lookup"><span data-stu-id="a555c-119">LCS implementation project workspace</span></span>

<span data-ttu-id="a555c-120">テナント管理者が Finance and Operations サブスクリプションの有効化を完了し、適切なプロジェクト所有者を追加した後、チーム メンバーは **実装プロジェクト** ワークスペースにアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="a555c-120">After the Tenant Administrator has completed the Finance and Operations subscription activation and added additional project owners as appropriate, those team members can access the **Implementation project** workspace.</span></span>

<span data-ttu-id="a555c-121">LCS で完了する最初の手順は、**プロジェクトのオンボード** です。</span><span class="sxs-lookup"><span data-stu-id="a555c-121">The first step to be completed in LCS is **Project onboarding**.</span></span> <span data-ttu-id="a555c-122">この手順は、Microsoft が管理するすべての環境を展開する前に、**2019 年 8 月 22 日 (PST) またはそれ以降** に作成されたすべての LCS 実装プロジェクトに必要です。</span><span class="sxs-lookup"><span data-stu-id="a555c-122">This step is required for all LCS implementation projects that are created **on or after August 22, 2019, PST**, prior to deploying any of the Microsoft-managed environments.</span></span> <span data-ttu-id="a555c-123">**プロジェクトのオンボード** 機能には、アクション センターの通知または LCS 実装プロジェクト メニューを使用してアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="a555c-123">You can access the **Project onboarding** feature using the action center notification or the LCS Implementation project menu.</span></span> <span data-ttu-id="a555c-124">LCS の **プロジェクト オンボード** にアクセスするには、プロジェクト所有者セキュリティ ロールに割り当てられている必要があります。</span><span class="sxs-lookup"><span data-stu-id="a555c-124">You must be assigned to the Project owner security role to access **Project onboarding** in LCS.</span></span>

<span data-ttu-id="a555c-125">LCS を開始するには、[Finance and Operations アプリ顧客用の Lifecycle Services (LCS)](../../dev-itpro/lifecycle-services/lcs-works-lcs.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="a555c-125">To get started with LCS, see [Lifecycle Services (LCS) for Finance and Operations apps customers](../../dev-itpro/lifecycle-services/lcs-works-lcs.md).</span></span> 

## <a name="fasttrack-onboarding-services"></a><span data-ttu-id="a555c-126">FastTrack オンボード サービス</span><span class="sxs-lookup"><span data-stu-id="a555c-126">FastTrack onboarding services</span></span>

<span data-ttu-id="a555c-127">LCS **実装プロジェクト** ワークスペースがプロビジョニングされたら、Microsoft FastTrack チームはオンボードの進捗状況を監視します。</span><span class="sxs-lookup"><span data-stu-id="a555c-127">After the LCS **Implementation project** workspace is provisioned, the Microsoft FastTrack team will monitor your onboarding progress.</span></span> <span data-ttu-id="a555c-128">LCS **実装プロジェクト** を作成してから数週間以内にプロジェクトのオンボードを完了しなかった場合、プロジェクト チームにアラームが送信されます。</span><span class="sxs-lookup"><span data-stu-id="a555c-128">If project onboarding is not completed within a few weeks after creating an LCS **Implementation project**, a reminder will be sent to the project team.</span></span> 

<span data-ttu-id="a555c-129">FastTrack プログラムおよび提供されるサービスの詳細については、 [Microsoft FastTrack](../get-started/fasttrack-dynamics-365-overview.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="a555c-129">For more information about the FastTrack program and the services provided, see [Microsoft FastTrack](../get-started/fasttrack-dynamics-365-overview.md).</span></span>

<span data-ttu-id="a555c-130">LCS プロジェクト オンボードの詳細については、[LCS プロジェクト オンボードの](../../dev-itpro/lifecycle-services/project-onboarding.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="a555c-130">For more information about LCS project onboarding, see [LCS project onboarding](../../dev-itpro/lifecycle-services/project-onboarding.md).</span></span>


> [!NOTE]
> <span data-ttu-id="a555c-131">FastTrack チームからのオンボードに関連するすべての電子メールは Dynamics 365 Onboarding (<ond365@microsoft.com>) から発信されるので、スパムのブロック/フィルターがこの住所からの電子メールを許可していることを確認してください。</span><span class="sxs-lookup"><span data-stu-id="a555c-131">All onboarding-related emails from the FastTrack team will originate from Dynamics 365 Onboarding (<ond365@microsoft.com>), so please ensure that any spam blocker/filter allows email from this address.</span></span>


## <a name="key-data-to-keep-current-in-lcs"></a><span data-ttu-id="a555c-132">LCS で最新状態にするキー データ</span><span class="sxs-lookup"><span data-stu-id="a555c-132">Key data to keep current in LCS</span></span>

<span data-ttu-id="a555c-133">LCS 実装プロジェクトに顧客やパートナー チームから主要なプロジェクト メンバー (プロジェクト マネージャーなど) を追加することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="a555c-133">We recommend that you add key project members (such as project managers) from the customer and partner teams to the LCS implementation project.</span></span> <span data-ttu-id="a555c-134">各人の勤務先電子メールを必ず含めるようにしてください。</span><span class="sxs-lookup"><span data-stu-id="a555c-134">Be sure to include each person's work email address.</span></span> <span data-ttu-id="a555c-135">この方法で、お客様と協力して、プロジェクトのメンバーが弊社からの重要な連絡を見逃さないよう保証できます。</span><span class="sxs-lookup"><span data-stu-id="a555c-135">In this way, you help us work best with you and help ensure that project members don't miss important communication from us.</span></span>

<span data-ttu-id="a555c-136">LCSプロジェクトのマイルストーン日付は、必ず最新の状態に保つようにしてください。</span><span class="sxs-lookup"><span data-stu-id="a555c-136">Be sure to keep the milestone dates in your LCS project current.</span></span> <span data-ttu-id="a555c-137">このように、さまざまなプロジェクトステージでお客様と連絡をとれます。</span><span class="sxs-lookup"><span data-stu-id="a555c-137">In this way, you help us connect with you at different project stages.</span></span> <span data-ttu-id="a555c-138">お客様が Go-live 日 により近づいたとき、マイクロソフトは、実稼働環境を配置する前に、プロジェクトの Go-live 評価のためにお客様と連絡を取ります。</span><span class="sxs-lookup"><span data-stu-id="a555c-138">When you're closer to your go-live date, we will contact you for a project Go-live assessment before we deploy your production environment.</span></span>

<span data-ttu-id="a555c-139">マイルストーンの日付は、LCS 実装方法に格納されます。</span><span class="sxs-lookup"><span data-stu-id="a555c-139">Milestone dates are stored in the LCS implementation methodology.</span></span> <span data-ttu-id="a555c-140">詳細については、「顧客向け LCS」トピックの [方法](../../dev-itpro/lifecycle-services/lcs-works-lcs.md#methodologies) セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="a555c-140">For more information, see the [Methodologies](../../dev-itpro/lifecycle-services/lcs-works-lcs.md#methodologies) section of the "LCS for Customers" topic.</span></span>
