---
title: "Finance and Operations 実装プロジェクトの配送準備"
description: "このトピックでは、Microsoft Dynamics Lifecycle Services (LCS) を使用して Finance and Operations のプロジェクト用に Microsoft Dynamics 365 を構成する方法について説明します。"
author: ClaudiaBetz-Haubold
manager: AnnBe
ms.date: 02/09/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: IT Pro
ms.reviewer: margoc
ms.search.scope: Operations
ms.search.region: Global
ms.author: chaubold
ms.search.validFrom: 2018-01-31
ms.dyn365.ops.version: July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 764d4c9049d94ebcd55c61654aa2f4133b35bae6
ms.openlocfilehash: 4bf2245355f5b14d89a7ac0ec94c24323633f801
ms.contentlocale: ja-jp
ms.lasthandoff: 08/09/2018

---

# <a name="onboard-a-finance-and-operations-implementation-project"></a><span data-ttu-id="2518c-103">Finance and Operations 実装プロジェクトの配送準備</span><span class="sxs-lookup"><span data-stu-id="2518c-103">Onboard a Finance and Operations implementation project</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="2518c-104">このトピックでは、Microsoft Dynamics Lifecycle Services (LCS) を使用して Finance and Operations のプロジェクト用に Microsoft Dynamics 365 を構成する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="2518c-104">This topic describes how to onboard a Microsoft Dynamics 365 for Finance and Operations project by using Microsoft Dynamics Lifecycle Services (LCS).</span></span>

## <a name="lcs-implementation-project-workspace"></a><span data-ttu-id="2518c-105">LCS 実装プロジェクト ワークスペース</span><span class="sxs-lookup"><span data-stu-id="2518c-105">LCS Implementation project workspace</span></span>

<span data-ttu-id="2518c-106">Finance and Operations を購入してサブスクリプションを有効化した後、**実装プロジェクト** ワークスペースでテナント管理者が初めてサインインすると、LCS にプロビジョニングされます。</span><span class="sxs-lookup"><span data-stu-id="2518c-106">After you've purchased and activated a subscription to Finance and Operations, an **Implementation project** workspace is provisioned in LCS when the tenant administrator signs in for the first time.</span></span> <span data-ttu-id="2518c-107">LCS を使い始めるにあたってヘルプが必要な場合は、「[Lifecycle Services for Finance and Operations の顧客](../../dev-itpro/lifecycle-services/lcs-works-lcs.md)」を参照します。</span><span class="sxs-lookup"><span data-stu-id="2518c-107">If you're a customer and require help to get started with LCS, see [Lifecycle Services for Finance and Operations customers](../../dev-itpro/lifecycle-services/lcs-works-lcs.md).</span></span> <span data-ttu-id="2518c-108">LCS の包括的な概要については、[Lifecycle Services の概要](../../dev-itpro/lifecycle-services/lcs-works-lcs.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="2518c-108">For a comprehensive overview of LCS, see [Overview of Lifecycle Services](../../dev-itpro/lifecycle-services/lcs-works-lcs.md).</span></span>

## <a name="fasttrack-onboarding-services"></a><span data-ttu-id="2518c-109">FastTrack オンボード サービス</span><span class="sxs-lookup"><span data-stu-id="2518c-109">FastTrack onboarding services</span></span>

<span data-ttu-id="2518c-110">LCS **実装プロジェクト** ワークスペースがプロビジョニングされた後、Microsoft FastTrack チームはプロジェクト チームに連絡してオンボーディング サービスについて説明します。</span><span class="sxs-lookup"><span data-stu-id="2518c-110">After your LCS **Implementation project** workspace is provisioned, the Microsoft FastTrack team will contact your project team to discuss onboarding services.</span></span> <span data-ttu-id="2518c-111">FastTrack プログラムおよびその提供するサービスの詳細については、[Dynamics 365 の Microsoft FastTrack](../get-started/fasttrack-dynamics-365-overview.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="2518c-111">For more information about the FastTrack program and the services that it offers, see [Microsoft FastTrack for Dynamics 365](../get-started/fasttrack-dynamics-365-overview.md).</span></span>

<span data-ttu-id="2518c-112">FastTrack チームは、LCS プロジェクトですべてのパートナーおよび顧客ユーザーに連絡し、Skype 経由で 60分のオンボード コールをスケジュールします。</span><span class="sxs-lookup"><span data-stu-id="2518c-112">The FastTrack team will contact all the partner and customer users in your LCS project to schedule a 60-minute onboarding call via Skype.</span></span> <span data-ttu-id="2518c-113">呼び出し中に、チームが FastTrack プログラムを導入し、LCS プロジェクトおよび関連するタスクの初期構成に役立ちます。</span><span class="sxs-lookup"><span data-stu-id="2518c-113">During this call, the team will introduce the FastTrack program and help you with the initial configuration of the LCS project and related tasks:</span></span>

- <span data-ttu-id="2518c-114">Tenant 検証</span><span class="sxs-lookup"><span data-stu-id="2518c-114">Tenant validation</span></span> 
- <span data-ttu-id="2518c-115">LCS の概要</span><span class="sxs-lookup"><span data-stu-id="2518c-115">Introduction to LCS</span></span>
- <span data-ttu-id="2518c-116">LCS プロジェクト ユーザーの設定</span><span class="sxs-lookup"><span data-stu-id="2518c-116">Setup of LCS project users</span></span>
- <span data-ttu-id="2518c-117">Microsoft Visual Studio Team Services の設定</span><span class="sxs-lookup"><span data-stu-id="2518c-117">Setup of Microsoft Visual Studio Team Services</span></span>
- <span data-ttu-id="2518c-118">サブスクリプション見積もりツール/使用状況プロファイラー</span><span class="sxs-lookup"><span data-stu-id="2518c-118">Subscription estimator/Usage profiler</span></span>
- <span data-ttu-id="2518c-119">環境計画</span><span class="sxs-lookup"><span data-stu-id="2518c-119">Environment planning</span></span>
- <span data-ttu-id="2518c-120">環境配置</span><span class="sxs-lookup"><span data-stu-id="2518c-120">Environment deployment</span></span>
- <span data-ttu-id="2518c-121">サービスの概要、サポート、サービスの正常性</span><span class="sxs-lookup"><span data-stu-id="2518c-121">Introduction to servicing, support, and service health</span></span>
- <span data-ttu-id="2518c-122">プランの準備</span><span class="sxs-lookup"><span data-stu-id="2518c-122">Readiness planning</span></span>

<span data-ttu-id="2518c-123">次に示すプロジェクト ロールのユーザーはミーティングに参加することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="2518c-123">We recommend that the people in the following project roles participate in the meeting.</span></span> <span data-ttu-id="2518c-124">その他のロール内のユーザーはオプションです。</span><span class="sxs-lookup"><span data-stu-id="2518c-124">People in other roles are optional.</span></span>

<span data-ttu-id="2518c-125">**顧客**</span><span class="sxs-lookup"><span data-stu-id="2518c-125">**Customer**</span></span>

- <span data-ttu-id="2518c-126">プロジェクト所有者</span><span class="sxs-lookup"><span data-stu-id="2518c-126">Project owner</span></span>
- <span data-ttu-id="2518c-127">Microsoft ビジネス センターの管理者、ライセンスが Microsoft とのボリューム サービス契約を通じて調達された場合</span><span class="sxs-lookup"><span data-stu-id="2518c-127">Microsoft Business Center administrator, if the license was procured through a Volume Service agreement with Microsoft</span></span>

<span data-ttu-id="2518c-128">**パートナー**</span><span class="sxs-lookup"><span data-stu-id="2518c-128">**Partner**</span></span>

- <span data-ttu-id="2518c-129">デリバリー リード/ソリューション アーキテクト</span><span class="sxs-lookup"><span data-stu-id="2518c-129">Delivery lead/solution architect</span></span>
- <span data-ttu-id="2518c-130">プロジェクト マネージャー</span><span class="sxs-lookup"><span data-stu-id="2518c-130">Project manager</span></span>

## <a name="key-data-to-keep-current-in-lcs"></a><span data-ttu-id="2518c-131">LCS で最新状態にするキー データ</span><span class="sxs-lookup"><span data-stu-id="2518c-131">Key data to keep current in LCS</span></span>

<span data-ttu-id="2518c-132">LCS プロジェクトに主要なプロジェクト メンバー (プロジェクト マネージャーなど) を追加することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="2518c-132">We recommend that you add key project members (such as project managers) to the LCS project.</span></span> <span data-ttu-id="2518c-133">各人の勤務先電子メールを必ず含めるようにしてください。</span><span class="sxs-lookup"><span data-stu-id="2518c-133">Be sure to include each person's work email address.</span></span> <span data-ttu-id="2518c-134">この方法で、お客様と協力して、プロジェクトのメンバーが弊社からの重要な連絡を見逃さないよう保証できます。</span><span class="sxs-lookup"><span data-stu-id="2518c-134">In this way, you help us work best with you and help guarantee that project members don't miss important communication from us.</span></span>

<span data-ttu-id="2518c-135">LCS プロジェクト内のマイルストーンの日付を最新の状態にして、さまざまなプロジェクト ステージであなたとつながれるようにします。</span><span class="sxs-lookup"><span data-stu-id="2518c-135">Keep the milestone dates in your LCS project current to help us connect with you at different project stages.</span></span> <span data-ttu-id="2518c-136">お客様が Go-live 日 により近づいたとき、マイクロソフトは、実稼働環境を配置する前に、プロジェクトの Go-live 評価のためにお客様と連絡を取ります。</span><span class="sxs-lookup"><span data-stu-id="2518c-136">When you're closer to your go-live date, we will contact you for a project Go-live assessment before we deploy your production environment.</span></span>

<span data-ttu-id="2518c-137">マイルストーンの日付は、LCS 実装方法に格納されます。</span><span class="sxs-lookup"><span data-stu-id="2518c-137">Milestone dates are stored in the LCS implementation methodology.</span></span> <span data-ttu-id="2518c-138">詳細については、「顧客向け LCS」トピックの [方法](../../dev-itpro/lifecycle-services/lcs-works-lcs.md#methodologies) セクションを参照してください。</span><span class="sxs-lookup"><span data-stu-id="2518c-138">For more information, see the [Methodologies](../../dev-itpro/lifecycle-services/lcs-works-lcs.md#methodologies) section of the "LCS for Customers" topic.</span></span>

<span data-ttu-id="2518c-139">オンボーディング呼び出しはオプションのサービスです。</span><span class="sxs-lookup"><span data-stu-id="2518c-139">The onboarding call is an optional service.</span></span> <span data-ttu-id="2518c-140">Finance and Operations の実装を理解しているパートナーは、FastTrack チームのサポートがなくても顧客と共にタスクを処理できます。</span><span class="sxs-lookup"><span data-stu-id="2518c-140">Partners who are experienced with Finance and Operations implementations can work through the tasks with their customers without the help of the FastTrack team.</span></span> <span data-ttu-id="2518c-141">そのような場合、プロジェクト ユーザーおよびマイルストーン日付を最新にしておくことが特に重要です。</span><span class="sxs-lookup"><span data-stu-id="2518c-141">In these cases, it's especially important that you keep the project users and milestone dates current.</span></span>

