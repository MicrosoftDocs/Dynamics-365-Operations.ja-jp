---
title: Dynamics 365 for Talent のモジュラー アプリのプロビジョニング
description: このトピックでは、Microsoft Dynamics 365 for Talent に含まれる Core Human Resources (HR) 機能を提供するために購入できるスタンドアロンのモジュラー アプリケーションをプロビジョニングする方法について説明します。 この機能は、Attract および Onboard などの追加エクスペリエンスを提供します。
author: rschloma
manager: AnnBe
ms.date: 08/03/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: IT Pro
ms.reviewer: rschloma
ms.search.scope: Core, Talent
ms.custom: 17271
ms.assetid: ba1ad49d-8232-400e-b11f-525423506a3f
ms.search.region: Global
ms.author: rschloma
ms.search.validFrom: 2018-03-20
ms.dyn365.ops.version: Talent March 2018 update
ms.openlocfilehash: 949695df931c2c01f1cc656478b39cde2c6d8879
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/29/2019
ms.locfileid: "368489"
---
# <a name="provisioning-for-the-dynamics-365-for-talent-modular-apps"></a><span data-ttu-id="09406-104">Dynamics 365 for Talent のモジュラー アプリのプロビジョニング</span><span class="sxs-lookup"><span data-stu-id="09406-104">Provisioning for the Dynamics 365 for Talent modular apps</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="09406-105">Microsoft Dynamics 365 for Talent には、Core Human Resources (HR) 機能および Attract や Onboard などの追加エクスペリエンスを提供する機能が含まれます。</span><span class="sxs-lookup"><span data-stu-id="09406-105">Microsoft Dynamics 365 for Talent includes core human resources (HR) capabilities and functionality that provide additional experiences, such as Attract and Onboard.</span></span> <span data-ttu-id="09406-106">この機能は、Web ダイレクトを通じたスタンドアロン モジュール アプリケーションとして購入することもできます。</span><span class="sxs-lookup"><span data-stu-id="09406-106">This functionality can also be purchased as standalone modular applications through web-direct.</span></span> <span data-ttu-id="09406-107">Microsoft Dynamics 365 for Talent: Attract および Microsoft Dynamics 365 for Talent: Onboard SKU などがその例です。</span><span class="sxs-lookup"><span data-stu-id="09406-107">Examples include Microsoft Dynamics 365 for Talent: Attract and Microsoft Dynamics 365 for Talent: Onboard SKUs.</span></span> <span data-ttu-id="09406-108">完全な Talent を購入するか、モジュラー アプリケーションを購入するのかによって、エクスペリエンスは多少異なります。</span><span class="sxs-lookup"><span data-stu-id="09406-108">Depending on whether you purchase full Talent or the modular applications, the experience differs somewhat.</span></span>

<span data-ttu-id="09406-109">モジュラー アプリケーションは、サービスの試用を開始したり、Web ダイレクトを通じて購入すると自動的にプロビジョニングされます。</span><span class="sxs-lookup"><span data-stu-id="09406-109">Modular applications are automatically provisioned when you initiate a trial of the services or purchase them through web-direct.</span></span> <span data-ttu-id="09406-110">顧客は Attract および Onboard の試用版を個別にサインアップできます。</span><span class="sxs-lookup"><span data-stu-id="09406-110">Customers can sign up for trials of Attract and Onboard separately.</span></span>

<span data-ttu-id="09406-111">Microsoft Dynamics Lifecycle Services (LCS) は Talent をプロビジョニングするために使用されますが、モジュラー アプリケーションのプロビジョニングには使用されません。</span><span class="sxs-lookup"><span data-stu-id="09406-111">Although Microsoft Dynamics Lifecycle Services (LCS) is used to provision Talent, it isn't used to provision the modular applications.</span></span>

<span data-ttu-id="09406-112">顧客は、モジュラー アプリケーションをプロビジョニングする必要な正確な場所を選択しません。</span><span class="sxs-lookup"><span data-stu-id="09406-112">Customers don't select the exact location where the modular applications should be provisioned.</span></span> <span data-ttu-id="09406-113">代わりに、次の要因により、モジュラー アプリケーションがプロビジョニングされる場所が決定します。</span><span class="sxs-lookup"><span data-stu-id="09406-113">Instead, the following factors determine where the modular applications are provisioned:</span></span>

+ <span data-ttu-id="09406-114">組織の既存の Microsoft PowerApps 環境の場所</span><span class="sxs-lookup"><span data-stu-id="09406-114">The location of the organization's existing Microsoft PowerApps environments</span></span>
+ <span data-ttu-id="09406-115">PowerApps 環境が存在しない場合は、組織の既存のテナントの場所は</span><span class="sxs-lookup"><span data-stu-id="09406-115">If no PowerApps environments exist, the location of the organization's existing tenant</span></span>
+ <span data-ttu-id="09406-116">Talent が現在サポートするデータ センター</span><span class="sxs-lookup"><span data-stu-id="09406-116">The data centers that Talent currently supports</span></span>

<span data-ttu-id="09406-117">サポートされている国または地域でのみ、モジュラー アプリケーションがプロビジョニングされます。</span><span class="sxs-lookup"><span data-stu-id="09406-117">Modular applications will be provisioned only in supported countries or regions.</span></span> <span data-ttu-id="09406-118">次の図は、使用されるロジックを示しています。</span><span class="sxs-lookup"><span data-stu-id="09406-118">The following illustration shows the logic that is used.</span></span> <span data-ttu-id="09406-119">(サポートされている国と地域は Microsoft Trust Center for Talent データ透過性で定義されています。)</span><span class="sxs-lookup"><span data-stu-id="09406-119">(The supported countries and regions are defined in the Microsoft Trust Center for Talent data transparency.)</span></span>

<span data-ttu-id="09406-120">[![国/地域に基づくモジュラー アプリケーションのプロビジョニング プロセス](./media/modular-apps-diagram-mod-app-tech.png)](./media/modular-apps-diagram-mod-app-tech.png)</span><span class="sxs-lookup"><span data-stu-id="09406-120">[![Provisioning process for modular applications, based on country/region](./media/modular-apps-diagram-mod-app-tech.png)](./media/modular-apps-diagram-mod-app-tech.png)</span></span>

<span data-ttu-id="09406-121">Talent とは異なり、モジュラー アプリケーションでは各ユーザーがアクセス可能な環境のリストは維持されません。</span><span class="sxs-lookup"><span data-stu-id="09406-121">Unlike Talent, the modular applications don't maintain a list of the environments that each user can access.</span></span> <span data-ttu-id="09406-122">ユーザーは、使用した最後の環境に自動的にサインインされます。</span><span class="sxs-lookup"><span data-stu-id="09406-122">Users are automatically signed in to the last environment that they used.</span></span> <span data-ttu-id="09406-123">**設定**ボタン (ギヤ記号) を使用して、さまざまな環境を選択できます。</span><span class="sxs-lookup"><span data-stu-id="09406-123">They can then select different environments by using the **Settings** button (the gear symbol).</span></span>
