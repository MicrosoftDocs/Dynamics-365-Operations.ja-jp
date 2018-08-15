---
title: "ワークスペースの Power BI を埋め込む"
description: "Finance and Operations は、アプリケーション ワークスペースにシームレスに統合される、強力な対話型レポートを備えるようになります。 Power BI でサポートされているグラフィックおよびビジュアルを使用することにより、ワークスペースは、ユーザーにとって非常に視覚的でありながらインタラクティブな体験を提供することができます。"
author: TJVass
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Developer, IT Pro
ms.reviewer: sericks
ms.search.scope: Operations
ms.custom: 270794
ms.assetid: f1d79557-2538-42b5-9ea3-4e86a61abfd4
ms.search.region: Global
ms.author: tjvass
ms.search.validFrom: 2017-02-28
ms.dyn365.ops.version: Platform update 4
ms.translationtype: HT
ms.sourcegitcommit: 821d8927211d7ac3e479848c7e7bef9f650d4340
ms.openlocfilehash: dcff36c4f59f0320ab545a60fe8cacc77a16103d
ms.contentlocale: ja-jp
ms.lasthandoff: 08/13/2018

---

# <a name="embedded-power-bi-in-workspaces"></a><span data-ttu-id="93297-104">ワークスペースの埋め込み Power BI</span><span class="sxs-lookup"><span data-stu-id="93297-104">Embedded Power BI in workspaces</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="93297-105">Finance and Operations は、アプリケーション ワークスペースにシームレスに統合される、強力な対話型レポートを備えるようになります。</span><span class="sxs-lookup"><span data-stu-id="93297-105">Finance and Operations now delivers rich, interactive reports seamlessly integrated into application workspaces.</span></span> <span data-ttu-id="93297-106">Power BI でサポートされているグラフィックおよびビジュアルを使用することにより、ワークスペースは、ユーザーにとって非常に視覚的でありながらインタラクティブな体験を提供することができます。</span><span class="sxs-lookup"><span data-stu-id="93297-106">By using graphics and visuals supported by Power BI, workspaces can provide a highly-visual, yet interactive experiences for users.</span></span>

## <a name="overview"></a><span data-ttu-id="93297-107">概要</span><span class="sxs-lookup"><span data-stu-id="93297-107">Overview</span></span>

<span data-ttu-id="93297-108">Finance and Operations 内のワークスペースはビジネス プロセスまたは事業単位の概要を提供します。</span><span class="sxs-lookup"><span data-stu-id="93297-108">Workspaces in Finance and Operations provide an overview of business processes or business units.</span></span> <span data-ttu-id="93297-109">豊富なワークスペースにより、詳細を表示してアクションを実行する前に、業務の状態の概要を取得することができます。</span><span class="sxs-lookup"><span data-stu-id="93297-109">With rich workspaces, users can get a bird's-eye view of the state of business before diving into details and taking action.</span></span> <span data-ttu-id="93297-110">ワークスペースには、レポートおよびページへのクイック リンクに加え、ビジュアル、カウント タイル、および KPI が含まれます。</span><span class="sxs-lookup"><span data-stu-id="93297-110">Workspaces contain visuals, count tiles, and KPIs as well as quick links to reports and pages.</span></span> <span data-ttu-id="93297-111">ワークスペース内では、すべてのコントロールが密接に統合され、生産性が高く魅力的な作業環境をユーザーに提供します。</span><span class="sxs-lookup"><span data-stu-id="93297-111">Within a workspace, all controls are tightly integrated to provide a highly-productive and engaging work environment to the user.</span></span> <span data-ttu-id="93297-112">Power BI Embedded は、ISV とアプリ開発者がアプリケーション内に Power BI データ エクスペリエンスを表示できるようにする Microsoft Azure サービスです。</span><span class="sxs-lookup"><span data-stu-id="93297-112">Power BI Embedded is a Microsoft Azure service that enables ISVs and app developers to surface Power BI data experiences within their applications.</span></span> <span data-ttu-id="93297-113">Power BI Embedded では、開発者は直接クエリを使用する常に最新のビューを提供することができます。</span><span class="sxs-lookup"><span data-stu-id="93297-113">With Power BI Embedded, developers can deliver always-up-to-date views with Direct Query.</span></span> <span data-ttu-id="93297-114">Power BI Embedded サービスと Finance and Operations の統合方法の詳細については、[[Power BI 埋め込み統合](power-bi-embedded-integration.md)] を参照してください。します。</span><span class="sxs-lookup"><span data-stu-id="93297-114">To learn more about how the Power BI Embedded service integrates with Finance and Operations, see [Power BI Embedded integration](power-bi-embedded-integration.md).</span></span>

## <a name="power-bi-in-workspaces"></a><span data-ttu-id="93297-115">ワークスペースにおける Power BI</span><span class="sxs-lookup"><span data-stu-id="93297-115">Power BI in workspaces</span></span>
<span data-ttu-id="93297-116">Finance and Operations は、アプリケーション ワークスペースにシームレスに統合する対話型レポートを備えるようになります。</span><span class="sxs-lookup"><span data-stu-id="93297-116">Finance and Operations now delivers interactive reports that seamlessly integrate into application workspaces.</span></span> <span data-ttu-id="93297-117">Power BI でサポートされている強力なインフォグラフィックやビジュアル (サード パーティが提供する多数のコントロールを含む) を使用することで、ワークスペースは非常に視覚的でありながらインタラクティブな体験をユーザーに提供することができます。</span><span class="sxs-lookup"><span data-stu-id="93297-117">By using rich infographics and visuals supported by Power BI (including the large number of controls provided by third parties), workspaces can provide a highly-visual, yet interactive experience for users.</span></span> <span data-ttu-id="93297-118">概要ページでインフォグラフィックを使用すると、ユーザーはビジネスの状態を素早く一目見ることができます。</span><span class="sxs-lookup"><span data-stu-id="93297-118">Using infographics in the overview page, users can get a quick glance of the state of the business.</span></span> <span data-ttu-id="93297-119">ページ上のビジュアルを単純にクリックまたはタッチすることで、データを操作できます。</span><span class="sxs-lookup"><span data-stu-id="93297-119">They can interact with data by simply clicking or touching visuals on the page.</span></span> <span data-ttu-id="93297-120">ワークスペース内だけで、原因と影響を分析したり、簡単な what-if 操作を実行したりできます。</span><span class="sxs-lookup"><span data-stu-id="93297-120">They can see the cause and effect, perform simple what-if operations without leaving the workspace.</span></span> <span data-ttu-id="93297-121">魅力的かつ対話型のビジュアルにより、ユーザーはデータの調査に没頭し、隠れたトレンドを発見することができます。</span><span class="sxs-lookup"><span data-stu-id="93297-121">Thanks to stunning yet interactive visuals, your users will have fun exploring data and discovering hidden trends.</span></span>

<span data-ttu-id="93297-122">次のスクリーン ショットは、ワークスペース内の Power BI を示しています。</span><span class="sxs-lookup"><span data-stu-id="93297-122">The following screenshot shows Power BI in a workspace.</span></span>

![ワークスペースにおける Power BI](./media/Power-BI-in-D365-Workspace.png)

### <a name="power-bi-vs-operational-workspaces"></a><span data-ttu-id="93297-124">Power BI と運用ワークスペース</span><span class="sxs-lookup"><span data-stu-id="93297-124">Power BI vs operational workspaces</span></span>
<span data-ttu-id="93297-125">Power BI ワークスペースは、ほぼリアルタイムの情報に基づく分析インサイトによって運用ビューを補完します。</span><span class="sxs-lookup"><span data-stu-id="93297-125">Power BI workspaces complement operational views with analytical insights based on near real-time information.</span></span> <span data-ttu-id="93297-126">次は、Power BI ワークスペースと操作可能なワークスペースを視覚的に比較したものです。</span><span class="sxs-lookup"><span data-stu-id="93297-126">The following offers a visual comparison of a Power BI workspace and an operational workspace.</span></span>

<span data-ttu-id="93297-127">次のスクリーン ショットは、操作可能なワークスペースを示しています。</span><span class="sxs-lookup"><span data-stu-id="93297-127">The following screenshot shows an operational workspace.</span></span>

![運用ワークスペース](./media/D365-Operational-Workspace.png)

## <a name="whats-next"></a><span data-ttu-id="93297-129">次の新機能</span><span class="sxs-lookup"><span data-stu-id="93297-129">What's next?</span></span>
<span data-ttu-id="93297-130">今後、新しいクラウド配置が Power BI 埋め込みサービスでバンドルされます。</span><span class="sxs-lookup"><span data-stu-id="93297-130">Going forward, new cloud deployments will come bundled with the Power BI Embedded service.</span></span> <span data-ttu-id="93297-131">開発者 ALM プロセスを説明している追加のドキュメントは、使用可能な Power BI Embedded サービス統合オプションを利用する新しいソリューションを作成するパートナーと ISV を支援するために利用可能になります。</span><span class="sxs-lookup"><span data-stu-id="93297-131">Additional documentation describing the Developer ALM process will be made available to help partners and ISVs create new solutions that take advantage of the Power BI Embedded service integration options that are available.</span></span>

