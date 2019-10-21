---
title: 小売機能の配置オプション
description: このトピックでは、Dynamics 365 Retail と Dynamics 365 Finance 間の小売機能の違いについて説明します。
author: ashishmsft
manager: AnnBe
ms.date: 10/17/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: IT Pro
ms.reviewer: rhaertle
ms.search.scope: Operations, Retail
ms.search.region: Global
ms.search.industry: retail
ms.author: asharchw
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: Retail July 2017 update
ms.openlocfilehash: 36a62b8664fe3d63d33252a09336cc5766dbd3aa
ms.sourcegitcommit: 2460d0da812c45fce67a061386db52e0ae46b0f3
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/30/2019
ms.locfileid: "2250356"
---
# <a name="deployment-options-for-retail-functionality"></a><span data-ttu-id="57167-103">小売機能の配置オプション</span><span class="sxs-lookup"><span data-stu-id="57167-103">Deployment options for retail functionality</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="57167-104">小売機能は、次の製品で使用できます。</span><span class="sxs-lookup"><span data-stu-id="57167-104">Retail functionality is available in the following products:</span></span>
 
- <span data-ttu-id="57167-105">Dynamics 365 Retail</span><span class="sxs-lookup"><span data-stu-id="57167-105">Dynamics 365 Retail</span></span>
- <span data-ttu-id="57167-106">Dynamics 365 Finance</span><span class="sxs-lookup"><span data-stu-id="57167-106">Dynamics 365 Finance</span></span>
 
<span data-ttu-id="57167-107">Dynamics 365 Retail には、ほとんどの小売業者が通常使用する主要な小売機能が含まれています。</span><span class="sxs-lookup"><span data-stu-id="57167-107">Dynamics 365 Retail contains core retail functionality that is typically used by most retailers.</span></span> <span data-ttu-id="57167-108">この状況に応じた機能が、生産性を向上し、従業員の採用およびトレーニングのプロセスの簡素化に役立ちます。</span><span class="sxs-lookup"><span data-stu-id="57167-108">This tailored functionality improves productivity and helps to ease the on-boarding and training processes for your employees.</span></span> 

<span data-ttu-id="57167-109">Dynamics 365 Retail には、追加機能を有効にするオプションがあります。</span><span class="sxs-lookup"><span data-stu-id="57167-109">With Dynamics 365 Retail, you also have the option to enable additional functionality.</span></span> <span data-ttu-id="57167-110">つまり、Dynamics 365 Finance 環境と機能的範囲が同じ Dynamics 365 Retail 環境を展開できます。</span><span class="sxs-lookup"><span data-stu-id="57167-110">This means that you could deploy a Dynamics 365 Retail environment that has the same functional footprint as a Dynamics 365 Finance environment.</span></span>
 
<span data-ttu-id="57167-111">次の表に、Retail と Finance and Operations の主な違いを示します。</span><span class="sxs-lookup"><span data-stu-id="57167-111">The following table lists the key differences between Retail and Finance and Operations.</span></span>

| <span data-ttu-id="57167-112">能力</span><span class="sxs-lookup"><span data-stu-id="57167-112">Capability</span></span>   |  <span data-ttu-id="57167-113">Dynamics 365 Retail</span><span class="sxs-lookup"><span data-stu-id="57167-113">Dynamics 365 Retail</span></span>   |  <span data-ttu-id="57167-114">Dynamics 365 Finance</span><span class="sxs-lookup"><span data-stu-id="57167-114">Dynamics 365 Finance</span></span> |
|--------------|----------------------------|-------------------------------------------|
|<span data-ttu-id="57167-115">アプリケーション モデルの更新をシームレスに受け取ります。</span><span class="sxs-lookup"><span data-stu-id="57167-115">Receive app model updates seamlessly.</span></span> <span data-ttu-id="57167-116">(アプリケーション モデルの更新は、カスタマイズしてコンパイルしたりマージしたりする必要はありません。)</span><span class="sxs-lookup"><span data-stu-id="57167-116">(App model updates do not need to be compiled or merged with your customizations.)</span></span> | <span data-ttu-id="57167-117">有</span><span class="sxs-lookup"><span data-stu-id="57167-117">Yes</span></span> | <span data-ttu-id="57167-118">無</span><span class="sxs-lookup"><span data-stu-id="57167-118">No</span></span>|
|<span data-ttu-id="57167-119">小売チャンネル コンポーネントの更新プログラムをシームレスに受け取ります。</span><span class="sxs-lookup"><span data-stu-id="57167-119">Receive retail channel component updates seamlessly.</span></span> <span data-ttu-id="57167-120">(小売チャネル コンポーネントの更新は、カスタマイズしてマージする必要はありません。)</span><span class="sxs-lookup"><span data-stu-id="57167-120">(Retail channel components updates do not need to be merged with your customizations.)</span></span> | <span data-ttu-id="57167-121">有</span><span class="sxs-lookup"><span data-stu-id="57167-121">Yes</span></span> | <span data-ttu-id="57167-122">有</span><span class="sxs-lookup"><span data-stu-id="57167-122">Yes</span></span> |
|<span data-ttu-id="57167-123">小売機能のみを提供するスコープのあるソリューションを展開します。</span><span class="sxs-lookup"><span data-stu-id="57167-123">Deploy a solution that is scoped to provide retail functionality only.</span></span> | <span data-ttu-id="57167-124">有</span><span class="sxs-lookup"><span data-stu-id="57167-124">Yes</span></span>  | <span data-ttu-id="57167-125">はい\*</span><span class="sxs-lookup"><span data-stu-id="57167-125">Yes\*</span></span><br><br><span data-ttu-id="57167-126">\* 配置後にコンフィギュレーションできます。</span><span class="sxs-lookup"><span data-stu-id="57167-126">\* Can be configured after deployment.</span></span>  |
|<span data-ttu-id="57167-127">インテリジェントで最新の企業ビジネス アプリケーションによって、財務および操作を最適化して成長を促進し、リアルタイムのデータに基づく判断を行います。</span><span class="sxs-lookup"><span data-stu-id="57167-127">Optimize your financials and operations to drive growth and make real-time, data-driven decisions with an intelligent, modern enterprise business application.</span></span>| <span data-ttu-id="57167-128">いいえ\*</span><span class="sxs-lookup"><span data-stu-id="57167-128">No\*</span></span><br><br><span data-ttu-id="57167-129">\* Finance and Operations Plan または Dynamics 365 Plan で追加機能を有効にすることができます。</span><span class="sxs-lookup"><span data-stu-id="57167-129">\* You can enable additional functionality with a Finance and Operations Plan or Dynamics 365 Plan.</span></span> | <span data-ttu-id="57167-130">はい</span><span class="sxs-lookup"><span data-stu-id="57167-130">Yes</span></span> |

<span data-ttu-id="57167-131">ライセンスの詳細については、[ライセンス ガイド](https://go.microsoft.com/fwlink/?LinkId=866544&clcid=0x409) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="57167-131">For more information about licensing, see the [Licensing Guide](https://go.microsoft.com/fwlink/?LinkId=866544&clcid=0x409).</span></span>

<span data-ttu-id="57167-132">テナントとしての必要なライセンスを取得した後、Lifecycle Services (LCS) を最初にアクセスするとき、実装プロジェクト タイプを選択するように要求されます。実装プロジェクト タイプでは、**Dynamics 365 Retail** または **Dynamics 365 Finance** を選択する必要があります。</span><span class="sxs-lookup"><span data-stu-id="57167-132">When you first visit Lifecycle Services (LCS) after acquiring the necessary licenses for your tenant, you will be prompted to choose an implementation project type, which is where you must select **Dynamics 365 Retail** or \*\*Dynamics 365 Finance \*\*.</span></span> <span data-ttu-id="57167-133">上記の考慮事項を使用すると、適切な製品を選択して展開することができます。</span><span class="sxs-lookup"><span data-stu-id="57167-133">You can use the above considerations to choose the right product to deploy.</span></span>
 
<span data-ttu-id="57167-134">上の表に示すように、Dynamics 365 Retail を展開する場合 (また必要なライセンスがある場合)、必要に応じて、展開時にソリューションを構成することができます。</span><span class="sxs-lookup"><span data-stu-id="57167-134">As indicated in the table above, if you choose to deploy Dynamics 365 Retail--and you have the necessary licenses--you will have the option, at deployment time, to configure the solution:</span></span> 

- <span data-ttu-id="57167-135">ソリューションの対象範囲を小売機能のみにする場合は、**小売のみ**を選択します。</span><span class="sxs-lookup"><span data-stu-id="57167-135">If you want the solution scoped to retail functionality only, select **Retail only**.</span></span> 
- <span data-ttu-id="57167-136">追加機能を有効にする場合は、**小売 + 工程**を選択します。</span><span class="sxs-lookup"><span data-stu-id="57167-136">If you want to enable additional functionality, select **Retail + Operations**.</span></span>
 
![配置設定](media/Deployment-settings.png)
