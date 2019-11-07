---
title: Analysis Services キューブから集計モデルへの移行
description: ことトピックでは、どのように、メモリ内、リアルタイム集計モデルが解析に使われ、なぜ Server Analysis Services (SSAS) キューブの使用から移行したのかを説明します。
author: MilindaV2
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 24511
ms.assetid: 877db646-da4b-48b5-83ab-61ae59d91921
ms.search.region: Global
ms.author: milindav
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 06c30a2b89745c1a41e5896c9234c98910ebd36a
ms.sourcegitcommit: d37fb09101c30858bcb975931b3d8f947d72017b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/10/2019
ms.locfileid: "2570544"
---
# <a name="transition-from-analysis-services-cubes-to-aggregate-models"></a><span data-ttu-id="2ad71-103">Analysis Services キューブから集計モデルへの移行</span><span class="sxs-lookup"><span data-stu-id="2ad71-103">Transition from Analysis Services cubes to aggregate models</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="2ad71-104">ことトピックでは、どのように、メモリ内、リアルタイム集計モデルが解析に使われ、なぜ Server Analysis Services (SSAS) キューブの使用から移行したのかを説明します。</span><span class="sxs-lookup"><span data-stu-id="2ad71-104">This topic explains how in-memory, real-time aggregate models are used for analytics, and why we transitioned from using Server Analysis Services (SSAS) cubes.</span></span>

<span data-ttu-id="2ad71-105">世界は、リアルタイムの積極的な分析に移行しています。</span><span class="sxs-lookup"><span data-stu-id="2ad71-105">The world is moving to real-time, proactive analytics.</span></span> <span data-ttu-id="2ad71-106">履歴データのレポートとトレンドは、最新の視覚化およびプロアクティブ ガイダンスにより置き換えられます。</span><span class="sxs-lookup"><span data-stu-id="2ad71-106">Reporting and trending on historical data is being replaced by up-to-the-second visualizations and proactive guidance.</span></span> <span data-ttu-id="2ad71-107">メモリ内でのリアルタイムな集計モデルにより、分析に以前使用された分析視点が置換されます。</span><span class="sxs-lookup"><span data-stu-id="2ad71-107">In-memory, real-time aggregate models now replace the perspectives that were previously used for analytics.</span></span>

## <a name="a-historical-look-at-perspectives-and-cubes"></a><span data-ttu-id="2ad71-108">分析視点とキューブの履歴</span><span class="sxs-lookup"><span data-stu-id="2ad71-108">A historical look at perspectives and cubes</span></span>
<span data-ttu-id="2ad71-109">Finance and Operations のユーザー エクスペリエンスで重要な役割を果たす埋め込みインサイトを想定しています。</span><span class="sxs-lookup"><span data-stu-id="2ad71-109">We envision embedded insights playing a key role in the Finance and Operations user experience.</span></span> <span data-ttu-id="2ad71-110">このビジョンにより、製品内に分析機能を構築するための投資が行われました。</span><span class="sxs-lookup"><span data-stu-id="2ad71-110">This vision has driven us to invest in building analytic capabilities within the product.</span></span> <span data-ttu-id="2ad71-111">Dynamics AX 4.0 では、*分析視点*の概念を導入しました。</span><span class="sxs-lookup"><span data-stu-id="2ad71-111">In Dynamics AX 4.0, we introduced the concept of *perspectives*.</span></span> <span data-ttu-id="2ad71-112">目的は、特にレポートのためにモデル化された、ERP スキーマのより簡単なビューを提示することでした。</span><span class="sxs-lookup"><span data-stu-id="2ad71-112">The objective was to present a simpler view of the ERP schema, specifically modeled for reporting.</span></span> <span data-ttu-id="2ad71-113">このより単純なビューは、分析視点と呼ばれていました。</span><span class="sxs-lookup"><span data-stu-id="2ad71-113">This simpler view was referred to as perspectives.</span></span> <span data-ttu-id="2ad71-114">Dynamics AX 4.0 では、システムが、SQL Server レポート ビルダーでアドホック レポートを作成できるレポート モデル (SMDL モデル) を生成していました。</span><span class="sxs-lookup"><span data-stu-id="2ad71-114">In Dynamics AX 4.0, the system generated reporting models (SMDL models) that enabled you to create ad-hoc reports with SQL Server Report Builder.</span></span> <span data-ttu-id="2ad71-115">Dynamics AX 2009 では、分析視点でメタデータ定義を使用して、SQL Server Analysis Services (SSAS) プロジェクトを生成する機能を追加しました。</span><span class="sxs-lookup"><span data-stu-id="2ad71-115">In Dynamics AX 2009, we added the capability to generate SQL Server Analysis Services (SSAS) projects using metadata definitions in perspectives.</span></span> <span data-ttu-id="2ad71-116">これらのプロジェクトは、SSAS サーバーに展開するとキューブになります。</span><span class="sxs-lookup"><span data-stu-id="2ad71-116">These projects become cubes when deployed to an SSAS server.</span></span> <span data-ttu-id="2ad71-117">Dynamics AX 2012 では、分析視点でのモデリングと、SSAS プロジェクトのライフ サイクルを管理するためのツール サポートが向上しました。</span><span class="sxs-lookup"><span data-stu-id="2ad71-117">In Dynamics AX 2012, we improved modeling in perspectives and improved tooling support for managing the lifecycle of SSAS projects.</span></span> <span data-ttu-id="2ad71-118">データを参照し、Dynamics AX 2012 のキューブでレポートを作成するには、Excel のほか Power View も使用することができました。</span><span class="sxs-lookup"><span data-stu-id="2ad71-118">You could use Excel, as well as Power View, to explore data and create reports with cubes in Dynamics AX 2012.</span></span> <span data-ttu-id="2ad71-119">SMDL テクノロジも使用されなくなりました。</span><span class="sxs-lookup"><span data-stu-id="2ad71-119">The SMDL technology was also deprecated.</span></span> <span data-ttu-id="2ad71-120">Dynamics AX 2012 では、SMDL モデルを生成しなくなりました。</span><span class="sxs-lookup"><span data-stu-id="2ad71-120">In Dynamics AX 2012, we stopped generating SMDL models.</span></span>

## <a name="how-perspectives-are-used-now"></a><span data-ttu-id="2ad71-121">現在分析視点がどのように使用されているか</span><span class="sxs-lookup"><span data-stu-id="2ad71-121">How perspectives are used now</span></span>
<span data-ttu-id="2ad71-122">開発者として、システムとの「契約」は視点でした。</span><span class="sxs-lookup"><span data-stu-id="2ad71-122">As a developer, your “contract” with the system was a perspective.</span></span> <span data-ttu-id="2ad71-123">システムは、最終目標を達成するのに役立つ「もの」を生み出しました。</span><span class="sxs-lookup"><span data-stu-id="2ad71-123">The system generated “stuff” to help you achieve your end goal.</span></span> <span data-ttu-id="2ad71-124">Dynamics AX 2012 では、生成された "もの" は SSAS プロジェクトでした。</span><span class="sxs-lookup"><span data-stu-id="2ad71-124">In Dynamics AX 2012, the "stuff” that was generated was SSAS projects.</span></span> <span data-ttu-id="2ad71-125">したがって、あなた (開発者) とシステム (BI フレームワーク) の間の契約は次のとおりでした。</span><span class="sxs-lookup"><span data-stu-id="2ad71-125">So the contract between you (the  developer) and the system (the BI framework), was as follows:</span></span>

-   <span data-ttu-id="2ad71-126">分析視点をモデル化しました。</span><span class="sxs-lookup"><span data-stu-id="2ad71-126">You modeled perspectives.</span></span>
-   <span data-ttu-id="2ad71-127">システムは、ビジュアルとレポートを作成するために必要な「もの」を生成しました。</span><span class="sxs-lookup"><span data-stu-id="2ad71-127">The system generated the "stuff" needed to enable you to build visuals and reports.</span></span>

<span data-ttu-id="2ad71-128">分析視点は、Visual Studio のアドインを使ってモデル化されるようになりました。</span><span class="sxs-lookup"><span data-stu-id="2ad71-128">Perspectives are now modeled using add-ins for Visual Studio.</span></span> <span data-ttu-id="2ad71-129">(Visual Studio は開発環境になっています。) 分析視点は*集計の測定*および*集計分析コード*から構成されます。</span><span class="sxs-lookup"><span data-stu-id="2ad71-129">(Visual Studio is now the development environment.) Perspectives are comprised of *aggregate measurements* and *aggregate dimensions*.</span></span> <span data-ttu-id="2ad71-130">開発者は、集計の測定と集計分析コードを使用して業務質問に答えるための簡単なスキーマをモデル化することができます。</span><span class="sxs-lookup"><span data-stu-id="2ad71-130">As a developer, you have the ability to model simpler schemas for answering business questions using aggregate measurements and aggregate dimensions.</span></span> <span data-ttu-id="2ad71-131">集計測定は Finance and Operations フォームにデータ ソースとして直接バインドできるデータ エンティティ (*集計データ エンティティ*と呼ばれる) を定義することができます。</span><span class="sxs-lookup"><span data-stu-id="2ad71-131">Aggregate measurements can be used to define data entities (called *aggregate data entities*) which can be directly bound to Finance and Operations forms as a data source.</span></span> <span data-ttu-id="2ad71-132">集計データ エンティティは に使用することもできます</span><span class="sxs-lookup"><span data-stu-id="2ad71-132">Aggregate data entities can also be used to</span></span>

-   <span data-ttu-id="2ad71-133">PowerBI にデータを公開します。</span><span class="sxs-lookup"><span data-stu-id="2ad71-133">Expose data to PowerBI.</span></span>
-   <span data-ttu-id="2ad71-134">AXQuery オブジェクトを使用してプログラムでデータにアクセス。</span><span class="sxs-lookup"><span data-stu-id="2ad71-134">Access data programmatically using the AXQuery object.</span></span>

<span data-ttu-id="2ad71-135">[![how-perspectives-are-used](./../media/how-perspectives-are-used.png)](./../media/how-perspectives-are-used.png)</span><span class="sxs-lookup"><span data-stu-id="2ad71-135">[![how-perspectives-are-used](./../media/how-perspectives-are-used.png)](./../media/how-perspectives-are-used.png)</span></span>  



