---
title: "Microsoft Dynamics 365 for Talent のモジュラー アプリのプロビジョニング"
description: "Dynamics 365 for Talent には Core HR 機能および Attract や Onboard などの追加エクスペリエンスを提供する機能が含まれます。 このような機能は、スタンドアロン モジュール アプリケーションとして購入することもできます。"
author: rschloma
manager: AnnBe
ms.date: 03/20/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: IT Pro
ms.reviewer: rschloma
ms.search.scope: Core, Talent
ms.custom: 17271
ms.assetid: ba1ad49d-8232-400e-b11f-525423506a3f
ms.search.region: Global
ms.author: rschloma
ms.search.validFrom: 2018-03-20
ms.dyn365.ops.version: Talent March 2018 update
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 6e9a39b23b37dec85b5f93b4da4f6f08ea973a9a
ms.contentlocale: ja-jp
ms.lasthandoff: 05/08/2018

---
# <a name="provision-microsoft-dynamics-365-for-talent-modular-apps"></a><span data-ttu-id="1a811-104">Microsoft Dynamics 365 for Talent のモジュラー アプリのプロビジョニング</span><span class="sxs-lookup"><span data-stu-id="1a811-104">Provision Microsoft Dynamics 365 for Talent Modular Apps</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="1a811-105">Dynamics 365 for Talent には、Core Human Resources 機能および Attract や Onboard などの追加エクスペリエンスを提供する機能が含まれます。</span><span class="sxs-lookup"><span data-stu-id="1a811-105">Dynamics 365 for Talent includes core human resources capabilities and functionality that provide additional experiences such as Attract and Onboard.</span></span> <span data-ttu-id="1a811-106">このような機能は、Web ダイレクトを通じたスタンドアロン モジュール アプリケーションとして購入することもできます (Dynamics 365 for Talent: Attract または Dynamics 365 for Talent: Onboard SKU など)。</span><span class="sxs-lookup"><span data-stu-id="1a811-106">Such functionality may also be available for purchase as a standalone modular application through web-direct (for example, Dynamics 365 for Talent: Attract or Dynamics 365 for Talent: Onboard SKUs).</span></span> <span data-ttu-id="1a811-107">完全な Talent をモジュラー アプリケーションと比べて購入すると、操作上の違いがいくつかあります。</span><span class="sxs-lookup"><span data-stu-id="1a811-107">There are some experience differences when purchasing full Talent versus the modular applications.</span></span>  

<span data-ttu-id="1a811-108">モジュラー アプリケーションは、試用版の開始時または Web ダイレクトを通じたサービスの購入時に自動的に準備されます。</span><span class="sxs-lookup"><span data-stu-id="1a811-108">Modular applications will automatically provision upon initiation of a trial or purchase of the services through web-direct.</span></span> <span data-ttu-id="1a811-109">Dynamics 365 for Talent のプロビジョニングに使用される Lifecycle Services (LCS) は、モジュラー アプリケーションとは使用されません。</span><span class="sxs-lookup"><span data-stu-id="1a811-109">Lifecycle Services (LCS), which is used to provision Dynamics 365 for Talent, is not used with the modular applications.</span></span> <span data-ttu-id="1a811-110">顧客は Attract または Onboard の評価版に個別にサインアップができます。</span><span class="sxs-lookup"><span data-stu-id="1a811-110">Customers can sign up for a trial for Attract or Onboard independently.</span></span>

<span data-ttu-id="1a811-111">顧客は、モジュラー アプリケーションのプロビジョニングを具体的に選択するのではなく、モジュラー アプリケーションのプロビジョニングを決定します。</span><span class="sxs-lookup"><span data-stu-id="1a811-111">Customers do not select specifically where their modular applications will provision, rather provisioning of modular applications is determined by:</span></span> 

 > + <span data-ttu-id="1a811-112">組織の既存の PowerApps 環境の場所</span><span class="sxs-lookup"><span data-stu-id="1a811-112">location of the organization’s existing PowerApps environments;</span></span>
 > + <span data-ttu-id="1a811-113">PowerApps 環境が存在しない場合は、組織の既存のテナントの場所</span><span class="sxs-lookup"><span data-stu-id="1a811-113">location of the organization’s existing tenant if no PowerApps environments exist; and</span></span>
 > + <span data-ttu-id="1a811-114">現在 Dynamics 365 for Talent でサポートされているデータ センター</span><span class="sxs-lookup"><span data-stu-id="1a811-114">the data centers currently supported by Dynamics 365 for Talent</span></span> 

<span data-ttu-id="1a811-115">モジュラー アプリケーションは、以下のロジックに従って (Microsoft Trust Center for Talent データ透過性で定義されたとおり) サポートされている地域でのみ準備されます。</span><span class="sxs-lookup"><span data-stu-id="1a811-115">Modular applications will provision only in supported geographies (as defined in the Microsoft Trust Center for Talent data transparency), according to the logic below:</span></span> 

<span data-ttu-id="1a811-116">[![モジュラー アプリケーションの地域](./media/modular-apps-diagram-mod-app-tech.png)](./media/modular-apps-diagram-mod-app-tech.png)</span><span class="sxs-lookup"><span data-stu-id="1a811-116">[![Geographies for modular applications](./media/modular-apps-diagram-mod-app-tech.png)](./media/modular-apps-diagram-mod-app-tech.png)</span></span>

<span data-ttu-id="1a811-117">Dynamics 365 for Talent とは異なり、モジュラー アプリケーションでは各ユーザーがアクセス可能な環境のリストは維持されません。</span><span class="sxs-lookup"><span data-stu-id="1a811-117">Unlike Dynamics 365 for Talent, the modular applications do not maintain a list of environments accessible by each user.</span></span> <span data-ttu-id="1a811-118">モジュール アプリケーション サービスを使用すると、ユーザーは最後に使用した環境に自動的にログインし、装置メニューから代替環境を選択できます。</span><span class="sxs-lookup"><span data-stu-id="1a811-118">When using the modular applications service users, will automatically log into the last environment used, and can select alternate environments through the gear menu.</span></span> 

