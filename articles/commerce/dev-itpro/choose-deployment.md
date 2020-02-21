---
title: 小売機能の配置オプション
description: このトピックでは、Dynamics 365 Commerce と Dynamics 365 Finance 間の機能の違いについて説明します。
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
ms.openlocfilehash: f77fc4857c743a35bf176f3b578e49b9b4831dab
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/01/2020
ms.locfileid: "3004597"
---
# <a name="deployment-options-for-retail-functionality"></a><span data-ttu-id="1ebac-103">小売機能の配置オプション</span><span class="sxs-lookup"><span data-stu-id="1ebac-103">Deployment options for retail functionality</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="1ebac-104">コマース機能は、次の製品で使用できます。</span><span class="sxs-lookup"><span data-stu-id="1ebac-104">Commerce functionality is available in the following products:</span></span>
 
- <span data-ttu-id="1ebac-105">Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="1ebac-105">Dynamics 365 Commerce</span></span>
- <span data-ttu-id="1ebac-106">Dynamics 365 Finance</span><span class="sxs-lookup"><span data-stu-id="1ebac-106">Dynamics 365 Finance</span></span>
 
<span data-ttu-id="1ebac-107">コマースには、ほとんどの小売業者が通常使用する主要な小売機能が含まれています。</span><span class="sxs-lookup"><span data-stu-id="1ebac-107">Commerce contains core retail functionality that is typically used by most retailers.</span></span> <span data-ttu-id="1ebac-108">この状況に応じた機能が、生産性を向上し、従業員の採用およびトレーニングのプロセスの簡素化に役立ちます。</span><span class="sxs-lookup"><span data-stu-id="1ebac-108">This tailored functionality improves productivity and helps to ease the on-boarding and training processes for your employees.</span></span> 

<span data-ttu-id="1ebac-109">コマースには、追加機能を有効にするオプションがあります。</span><span class="sxs-lookup"><span data-stu-id="1ebac-109">With Commerce, you also have the option to enable additional functionality.</span></span> <span data-ttu-id="1ebac-110">つまり、Finance 環境として機能的範囲が同じ環境を展開することができます。</span><span class="sxs-lookup"><span data-stu-id="1ebac-110">This means that you could deploy an environment that has the same functional footprint as a Finance environment.</span></span>
 
<span data-ttu-id="1ebac-111">次の表に、Commerce と Finance and Operations との主な違いを示します。</span><span class="sxs-lookup"><span data-stu-id="1ebac-111">The following table lists the key differences between Commerce and Finance and Operations.</span></span>

| <span data-ttu-id="1ebac-112">能力</span><span class="sxs-lookup"><span data-stu-id="1ebac-112">Capability</span></span>   |  <span data-ttu-id="1ebac-113">Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="1ebac-113">Dynamics 365 Commerce</span></span>   |  <span data-ttu-id="1ebac-114">Dynamics 365 Finance</span><span class="sxs-lookup"><span data-stu-id="1ebac-114">Dynamics 365 Finance</span></span> |
|--------------|----------------------------|-------------------------------------------|
|<span data-ttu-id="1ebac-115">アプリケーション モデルの更新をシームレスに受け取ります。</span><span class="sxs-lookup"><span data-stu-id="1ebac-115">Receive app model updates seamlessly.</span></span> <span data-ttu-id="1ebac-116">(アプリケーション モデルの更新は、カスタマイズしてコンパイルしたりマージしたりする必要はありません。)</span><span class="sxs-lookup"><span data-stu-id="1ebac-116">(App model updates do not need to be compiled or merged with your customizations.)</span></span> | <span data-ttu-id="1ebac-117">はい</span><span class="sxs-lookup"><span data-stu-id="1ebac-117">Yes</span></span> | <span data-ttu-id="1ebac-118">いいえ</span><span class="sxs-lookup"><span data-stu-id="1ebac-118">No</span></span>|
|<span data-ttu-id="1ebac-119">チャンネル コンポーネントの更新プログラムをシームレスに受け取ります。</span><span class="sxs-lookup"><span data-stu-id="1ebac-119">Receive channel component updates seamlessly.</span></span> <span data-ttu-id="1ebac-120">(チャネル コンポーネントの更新は、カスタマイズしてマージする必要はありません。)</span><span class="sxs-lookup"><span data-stu-id="1ebac-120">(Channel components updates do not need to be merged with your customizations.)</span></span> | <span data-ttu-id="1ebac-121">はい</span><span class="sxs-lookup"><span data-stu-id="1ebac-121">Yes</span></span> | <span data-ttu-id="1ebac-122">はい</span><span class="sxs-lookup"><span data-stu-id="1ebac-122">Yes</span></span> |
|<span data-ttu-id="1ebac-123">コマース機能のみを提供するスコープのあるソリューションを展開します。</span><span class="sxs-lookup"><span data-stu-id="1ebac-123">Deploy a solution that is scoped to provide commerce functionality only.</span></span> | <span data-ttu-id="1ebac-124">はい</span><span class="sxs-lookup"><span data-stu-id="1ebac-124">Yes</span></span>  | <span data-ttu-id="1ebac-125">はい\*</span><span class="sxs-lookup"><span data-stu-id="1ebac-125">Yes\*</span></span><br><br><span data-ttu-id="1ebac-126">\* 配置後にコンフィギュレーションできます。</span><span class="sxs-lookup"><span data-stu-id="1ebac-126">\* Can be configured after deployment.</span></span>  |
|<span data-ttu-id="1ebac-127">インテリジェントで最新の企業ビジネス アプリケーションによって、財務および操作を最適化して成長を促進し、リアルタイムのデータに基づく判断を行います。</span><span class="sxs-lookup"><span data-stu-id="1ebac-127">Optimize your financials and operations to drive growth and make real-time, data-driven decisions with an intelligent, modern enterprise business application.</span></span>| <span data-ttu-id="1ebac-128">いいえ\*</span><span class="sxs-lookup"><span data-stu-id="1ebac-128">No\*</span></span><br><br><span data-ttu-id="1ebac-129">\* Finance and Operations Plan または Dynamics 365 Plan で追加機能を有効にすることができます。</span><span class="sxs-lookup"><span data-stu-id="1ebac-129">\* You can enable additional functionality with a Finance and Operations Plan or Dynamics 365 Plan.</span></span> | <span data-ttu-id="1ebac-130">はい</span><span class="sxs-lookup"><span data-stu-id="1ebac-130">Yes</span></span> |

<span data-ttu-id="1ebac-131">ライセンスの詳細については、[ライセンス ガイド](https://go.microsoft.com/fwlink/?LinkId=866544&clcid=0x409) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="1ebac-131">For more information about licensing, see the [Licensing Guide](https://go.microsoft.com/fwlink/?LinkId=866544&clcid=0x409).</span></span>

<span data-ttu-id="1ebac-132">テナントとしての必要なライセンスを取得した後、Lifecycle Services (LCS) を最初にアクセスするとき、実装プロジェクト タイプを選択するように要求されます。実装プロジェクト タイプでは、**Dynamics 365 Commerce** または **Dynamics 365 Finance** を選択する必要があります。</span><span class="sxs-lookup"><span data-stu-id="1ebac-132">When you first visit Lifecycle Services (LCS) after acquiring the necessary licenses for your tenant, you will be prompted to choose an implementation project type, which is where you must select **Dynamics 365 Commerce** or **Dynamics 365 Finance**.</span></span> <span data-ttu-id="1ebac-133">上記の考慮事項を使用すると、適切な製品を選択して展開することができます。</span><span class="sxs-lookup"><span data-stu-id="1ebac-133">You can use the above considerations to choose the right product to deploy.</span></span>
 
<span data-ttu-id="1ebac-134">上の表に示すように、Dynamics 365 Commerce を展開する場合 (また必要なライセンスがある場合)、必要に応じて、展開時にソリューションを構成することができます。</span><span class="sxs-lookup"><span data-stu-id="1ebac-134">As indicated in the table above, if you choose to deploy Dynamics 365 Commerce--and you have the necessary licenses--you will have the option, at deployment time, to configure the solution:</span></span> 

- <span data-ttu-id="1ebac-135">ソリューションの対象範囲をコマース機能のみにする場合は、**コマースのみ**を選択します。</span><span class="sxs-lookup"><span data-stu-id="1ebac-135">If you want the solution scoped to commerce functionality only, select **Commerce only**.</span></span> 
- <span data-ttu-id="1ebac-136">追加機能を有効にする場合は、**コマース + 工程**を選択します。</span><span class="sxs-lookup"><span data-stu-id="1ebac-136">If you want to enable additional functionality, select **Commerce + Operations**.</span></span>
 
![配置設定](media/Deployment-settings.png)
