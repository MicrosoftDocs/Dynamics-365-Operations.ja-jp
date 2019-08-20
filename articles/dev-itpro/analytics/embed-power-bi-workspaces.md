---
title: ワークスペースで Power BI を埋め込みます。
description: Finance and Operations は、アプリケーション ワークスペースにシームレスに統合される、強力な対話型レポートを備えるようになります。 Power BI でサポートされているグラフィックおよびビジュアルを使用することにより、ワークスペースは、ユーザーにとって非常に視覚的でありながらインタラクティブな体験を提供することができます。
author: TJVass
manager: AnnBe
ms.date: 07/23/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Operations
ms.custom: 270794
ms.assetid: f1d79557-2538-42b5-9ea3-4e86a61abfd4
ms.search.region: Global
ms.author: tjvass
ms.search.validFrom: 2017-02-28
ms.dyn365.ops.version: Platform update 4
ms.openlocfilehash: fb3d7cd37575cfa82affbde123d47e5ae52c0aaf
ms.sourcegitcommit: 16bfa0fd08feec1647829630401ce62ce2ffa1a4
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/02/2019
ms.locfileid: "1849803"
---
# <a name="embedded-power-bi-in-workspaces"></a><span data-ttu-id="f8aa9-104">ワークスペースで埋め込まれた Power BI</span><span class="sxs-lookup"><span data-stu-id="f8aa9-104">Embedded Power BI in workspaces</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f8aa9-105">Finance and Operations は、アプリケーション ワークスペースにシームレスに統合される、強力な対話型レポートを備えるようになります。</span><span class="sxs-lookup"><span data-stu-id="f8aa9-105">Finance and Operations now delivers rich, interactive reports seamlessly integrated into application workspaces.</span></span> <span data-ttu-id="f8aa9-106">Power BI でサポートされているグラフィックおよびビジュアルを使用することにより、ワークスペースは、ユーザーにとって非常に視覚的でありながらインタラクティブな体験を提供することができます。</span><span class="sxs-lookup"><span data-stu-id="f8aa9-106">By using graphics and visuals supported by Power BI, workspaces can provide a highly-visual, yet interactive experiences for users.</span></span>

## <a name="overview"></a><span data-ttu-id="f8aa9-107">概要</span><span class="sxs-lookup"><span data-stu-id="f8aa9-107">Overview</span></span>

<span data-ttu-id="f8aa9-108">Finance and Operations 内のワークスペースはビジネス プロセスまたは事業単位の概要を提供します。</span><span class="sxs-lookup"><span data-stu-id="f8aa9-108">Workspaces in Finance and Operations provide an overview of business processes or business units.</span></span> <span data-ttu-id="f8aa9-109">豊富なワークスペースにより、詳細を表示してアクションを実行する前に、業務の状態の概要を取得することができます。</span><span class="sxs-lookup"><span data-stu-id="f8aa9-109">With rich workspaces, users can get a bird's-eye view of the state of business before diving into details and taking action.</span></span> <span data-ttu-id="f8aa9-110">ワークスペースには、レポートおよびページへのクイック リンクに加え、ビジュアル、カウント タイル、および KPI が含まれます。</span><span class="sxs-lookup"><span data-stu-id="f8aa9-110">Workspaces contain visuals, count tiles, and KPIs as well as quick links to reports and pages.</span></span> <span data-ttu-id="f8aa9-111">ワークスペース内では、すべてのコントロールが密接に統合され、生産性が高く魅力的な作業環境をユーザーに提供します。</span><span class="sxs-lookup"><span data-stu-id="f8aa9-111">Within a workspace, all controls are tightly integrated to provide a highly-productive and engaging work environment to the user.</span></span> <span data-ttu-id="f8aa9-112">Power BI Embedded は Microsoft Azure サービスで、ISV およびアプリの開発者がアプリケーション内で Power BI データ エクスペリエンスを表すことを可能にします。</span><span class="sxs-lookup"><span data-stu-id="f8aa9-112">Power BI Embedded is a Microsoft Azure service that enables ISVs and app developers to surface Power BI data experiences within their applications.</span></span> <span data-ttu-id="f8aa9-113">Power BI Embedded では、開発者は直接クエリで常に最新のビューを提供することができます。</span><span class="sxs-lookup"><span data-stu-id="f8aa9-113">With Power BI Embedded, developers can deliver always-up-to-date views with Direct Query.</span></span> <span data-ttu-id="f8aa9-114">Power BI Embedded サービスと Finance and Operations の統合方法の詳細については、[Power BI Embedded 統合](power-bi-embedded-integration.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="f8aa9-114">To learn more about how the Power BI Embedded service integrates with Finance and Operations, see [Power BI Embedded integration](power-bi-embedded-integration.md).</span></span>

## <a name="power-bi-in-workspaces"></a><span data-ttu-id="f8aa9-115">ワークスペースでの Power BI</span><span class="sxs-lookup"><span data-stu-id="f8aa9-115">Power BI in workspaces</span></span>
<span data-ttu-id="f8aa9-116">Finance and Operations は、アプリケーション ワークスペースにシームレスに統合する対話型レポートを備えるようになります。</span><span class="sxs-lookup"><span data-stu-id="f8aa9-116">Finance and Operations now delivers interactive reports that seamlessly integrate into application workspaces.</span></span> <span data-ttu-id="f8aa9-117">Power BI でサポートされている強力なインフォグラフィックやビジュアル (サード パーティが提供する多数のコントロールを含む) を使用することで、ワークスペースは非常に視覚的でありながらインタラクティブな体験をユーザーに提供することができます。</span><span class="sxs-lookup"><span data-stu-id="f8aa9-117">By using rich infographics and visuals supported by Power BI (including the large number of controls provided by third parties), workspaces can provide a highly-visual, yet interactive experience for users.</span></span> <span data-ttu-id="f8aa9-118">概要ページでインフォグラフィックを使用すると、ユーザーはビジネスの状態を素早く一目見ることができます。</span><span class="sxs-lookup"><span data-stu-id="f8aa9-118">Using infographics in the overview page, users can get a quick glance of the state of the business.</span></span> <span data-ttu-id="f8aa9-119">ページ上のビジュアルを単純にクリックまたはタッチすることで、データを操作できます。</span><span class="sxs-lookup"><span data-stu-id="f8aa9-119">They can interact with data by simply clicking or touching visuals on the page.</span></span> <span data-ttu-id="f8aa9-120">ワークスペース内だけで、原因と影響を分析したり、簡単な what-if 操作を実行したりできます。</span><span class="sxs-lookup"><span data-stu-id="f8aa9-120">They can see the cause and effect, perform simple what-if operations without leaving the workspace.</span></span> <span data-ttu-id="f8aa9-121">魅力的かつ対話型のビジュアルにより、ユーザーはデータの調査に没頭し、隠れたトレンドを発見することができます。</span><span class="sxs-lookup"><span data-stu-id="f8aa9-121">Thanks to stunning yet interactive visuals, your users will have fun exploring data and discovering hidden trends.</span></span>

<span data-ttu-id="f8aa9-122">次のスクリーン ショットは、ワークスペース内の Power BI を示しています。</span><span class="sxs-lookup"><span data-stu-id="f8aa9-122">The following screenshot shows Power BI in a workspace.</span></span>

![ワークスペースでの Power BI](./media/Power-BI-in-D365-Workspace.png)

## <a name="power-bi-vs-operational-workspaces"></a><span data-ttu-id="f8aa9-124">Power BI 対 運用ワークスペース</span><span class="sxs-lookup"><span data-stu-id="f8aa9-124">Power BI vs operational workspaces</span></span>
<span data-ttu-id="f8aa9-125">Power BI ワークスペースは、ほぼリアルタイムの情報に基づく分析インサイトによって運用ビューを補完します。</span><span class="sxs-lookup"><span data-stu-id="f8aa9-125">Power BI workspaces complement operational views with analytical insights based on near real-time information.</span></span> <span data-ttu-id="f8aa9-126">次は、Power BI ワークスペースと運用ワークスペースを視覚的に比較したものです。</span><span class="sxs-lookup"><span data-stu-id="f8aa9-126">The following offers a visual comparison of a Power BI workspace and an operational workspace.</span></span>

<span data-ttu-id="f8aa9-127">次のスクリーン ショットは、操作可能なワークスペースを示しています。</span><span class="sxs-lookup"><span data-stu-id="f8aa9-127">The following screenshot shows an operational workspace.</span></span>

![運用ワークスペース](./media/D365-Operational-Workspace.png)

## <a name="edit-embedded-reports-in-analytical-workspaces"></a><span data-ttu-id="f8aa9-129">分析ワークスペースで埋め込みレポートを編集する</span><span class="sxs-lookup"><span data-stu-id="f8aa9-129">Edit embedded reports in analytical workspaces</span></span>

> [!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RE3nnj4]

<span data-ttu-id="f8aa9-130">[分析ワークスペースで埋め込みレポートを編集する方法](https://youtu.be/_8WlwmSggcQ) のビデオ (上記) は YouTube で利用可能な [Finance and Operations プレイリスト](https://www.youtube.com/playlist?list=PLcakwueIHoT_SYfIaPGoOhloFoCXiUSyW) に含まれています。</span><span class="sxs-lookup"><span data-stu-id="f8aa9-130">The [How to edit an embedded report in an analytical workspace](https://youtu.be/_8WlwmSggcQ) video (shown above) is included in the [Finance and Operations playlist](https://www.youtube.com/playlist?list=PLcakwueIHoT_SYfIaPGoOhloFoCXiUSyW) available on YouTube.</span></span>


## <a name="whats-next"></a><span data-ttu-id="f8aa9-131">次の新機能</span><span class="sxs-lookup"><span data-stu-id="f8aa9-131">What's next?</span></span>
<span data-ttu-id="f8aa9-132">今後、Power BI Embedded サービスがバンドルされた新しいクラウド配置が登場します。</span><span class="sxs-lookup"><span data-stu-id="f8aa9-132">Going forward, new cloud deployments will come bundled with the Power BI Embedded service.</span></span> <span data-ttu-id="f8aa9-133">開発者 ALM プロセスを説明している追加のドキュメントは、使用可能な Power BI Embedded サービス統合オプションを利用して新しいソリューションを作成するパートナーと ISV を支援するために利用可能になります。</span><span class="sxs-lookup"><span data-stu-id="f8aa9-133">Additional documentation describing the Developer ALM process will be made available to help partners and ISVs create new solutions that take advantage of the Power BI Embedded service integration options that are available.</span></span>
