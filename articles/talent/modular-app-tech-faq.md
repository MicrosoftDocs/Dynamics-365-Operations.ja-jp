---
title: Dynamics 365 Talent - Onboard アプリのプロビジョニング
description: このトピックでは、スタンドアロン Dynamics 365 Talent - Onboard アプリをプロビジョニングする方法について説明します。
author: andreabichsel
manager: AnnBe
ms.date: 04/16/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: IT Pro
ms.reviewer: anbichse
ms.search.scope: Core, Talent
ms.custom: 17271
ms.assetid: ba1ad49d-8232-400e-b11f-525423506a3f
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2018-03-20
ms.dyn365.ops.version: Talent March 2018 update
ms.openlocfilehash: 7d541a315b4e25e4cece990792fa48f02f980d30
ms.sourcegitcommit: 75db3b75d35d27034f9b56e7119c9d0cb7666830
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/03/2019
ms.locfileid: "2550356"
---
#  <a name="provisioning-for-the-dynamics-365-talent---onboard-app"></a><span data-ttu-id="dfe7a-103">Dynamics 365 Talent - Onboard アプリのプロビジョニング</span><span class="sxs-lookup"><span data-stu-id="dfe7a-103">Provisioning for the Dynamics 365 Talent - Onboard app</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="dfe7a-104">Microsoft Dynamics 365 Talent の完全版には、中核人事 (Core HR) 機能に加えて Attract と Onboard が含まれており、社内の 採用と オンボードのプロセス を認識することができます。</span><span class="sxs-lookup"><span data-stu-id="dfe7a-104">The full version of Microsoft Dynamics 365 Talent includes core human resources (HR) capabilities plus Attract and Onboard, which provide recruiting and onboarding experiences for your organization.</span></span> <span data-ttu-id="dfe7a-105">また、オンボード アプリのスタンドアロンバージョンを購入することもできます。</span><span class="sxs-lookup"><span data-stu-id="dfe7a-105">You can also purchase a standalone version of the Onboard app.</span></span> <span data-ttu-id="dfe7a-106">Talent の完全版とスタンドアロンのオンボードアプリのどちらを購入したかによって、プロビジョニング内容が若干異なります。</span><span class="sxs-lookup"><span data-stu-id="dfe7a-106">Depending on whether you purchase the full version of Talent or the standalone Onboard app, the provisioning experience is slightly different.</span></span>

<span data-ttu-id="dfe7a-107">オンボードアプリは、試用版を起動するか、またはオンラインで購入したときに自動的に準備されます。</span><span class="sxs-lookup"><span data-stu-id="dfe7a-107">The Onboard app is automatically provisioned when you start a trial or purchase it online.</span></span> <span data-ttu-id="dfe7a-108">完全版の Talent を使用するにはプロビジョニングのために Microsoft Dynamics Lifecycle Services (LCS) が必要となりますが、スタンドアロンの Onboard アプリには LCS は必要ありません。</span><span class="sxs-lookup"><span data-stu-id="dfe7a-108">The full version of Talent requires Microsoft Dynamics Lifecycle Services (LCS) for provisioning, but the standalone Onboard app doesn't require LCS.</span></span>

<span data-ttu-id="dfe7a-109">スタンドアロンの Onboard アプリでは、プロビジョニングの対象を選択をすることはありません。</span><span class="sxs-lookup"><span data-stu-id="dfe7a-109">With the standalone Onboard app, you don't select the exact location where it should be provisioned.</span></span> <span data-ttu-id="dfe7a-110">そのかわりに、以下の要素によって Onboard がプロビジョニングされる場所が決まります。</span><span class="sxs-lookup"><span data-stu-id="dfe7a-110">Instead, the following factors determine where Onboard is provisioned:</span></span>

- <span data-ttu-id="dfe7a-111">Microsoft PowerApps 環境が存在する場合は同環境の場所を参照します</span><span class="sxs-lookup"><span data-stu-id="dfe7a-111">The location of your organization's existing Microsoft PowerApps environments, if any.</span></span>
- <span data-ttu-id="dfe7a-112">PowerApps 環境が存在しない場合は、組織の既存のテナントの場所を参照します</span><span class="sxs-lookup"><span data-stu-id="dfe7a-112">If no PowerApps environments exist, the location of the organization's existing tenant.</span></span>
- <span data-ttu-id="dfe7a-113">Talent が現在対応しているデータ センター</span><span class="sxs-lookup"><span data-stu-id="dfe7a-113">The data centers that Talent currently supports.</span></span>

<span data-ttu-id="dfe7a-114">Onboard アプリは、対応する国または地域でのみで提供しています。</span><span class="sxs-lookup"><span data-stu-id="dfe7a-114">The Onboard app is provisioned only in supported countries or regions.</span></span> <span data-ttu-id="dfe7a-115">サポートされている国と地域は Microsoft Trust Center for Talent データ透過性で定義されています。</span><span class="sxs-lookup"><span data-stu-id="dfe7a-115">The supported countries and regions are defined in the Microsoft Trust Center for Talent data transparency.</span></span> <span data-ttu-id="dfe7a-116">サポートされている国と地域の一覧は、『[Microsoft Dynamics 365 の国際可用性ガイド](https://docs.microsoft.com/dynamics365/get-started/availability)』を参照してください。</span><span class="sxs-lookup"><span data-stu-id="dfe7a-116">For a list of supported countries and regions, see [International availability of Microsoft Dynamics 365](https://docs.microsoft.com/dynamics365/get-started/availability).</span></span>

<span data-ttu-id="dfe7a-117">以下の図では、スタンドアロンの Onboard アプリを提供するにあたって使用されているロジックを示しています。</span><span class="sxs-lookup"><span data-stu-id="dfe7a-117">The following illustration shows the logic used for provisioning the standalone Onboard app.</span></span>

<span data-ttu-id="dfe7a-118">[![国/地域にもとづいた、スタンドアロン Onboardアプリの プロビジョニングプロセス](./media/modular-apps-diagram-mod-app-tech.png)](./media/modular-apps-diagram-mod-app-tech.png)</span><span class="sxs-lookup"><span data-stu-id="dfe7a-118">[![Provisioning process for the standalone Onboard app, based on country/region](./media/modular-apps-diagram-mod-app-tech.png)](./media/modular-apps-diagram-mod-app-tech.png)</span></span>

<span data-ttu-id="dfe7a-119">完全版の Talent とは異なり、スタンドアロンの Onboard アプリ では、各ユーザーがアクセス可能となる環境の一覧を管理していません。</span><span class="sxs-lookup"><span data-stu-id="dfe7a-119">Unlike the full version of Talent, the standalone Onboard app doesn't maintain a list of the environments that each user can access.</span></span> <span data-ttu-id="dfe7a-120">ユーザーは、最後に使用した環境に自動的にサインインします。</span><span class="sxs-lookup"><span data-stu-id="dfe7a-120">Users are automatically signed in to the last environment they used.</span></span> <span data-ttu-id="dfe7a-121">**設定**ボタン (ギヤ記号) を使用して、さまざまな環境を選択できます。</span><span class="sxs-lookup"><span data-stu-id="dfe7a-121">They can then select different environments by using the **Settings** button (the gear symbol).</span></span>
