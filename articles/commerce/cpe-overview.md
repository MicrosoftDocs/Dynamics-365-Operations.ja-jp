---
title: Dynamics 365 Commerce プレビュー環境の概要
description: このトピックでは、Microsoft Dynamics 365 Commerce プレビュー環境の概要を示します。
author: v-chgri
manager: annbe
ms.date: 12/10/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Operations, Retail, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: v-chgri
ms.search.validFrom: 2019-12-10
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 1ff96aeb5963df9ddee56783a089dad129bbb71c
ms.sourcegitcommit: 4ed1d8ad8a0206a4172dbb41cc43f7d95073059c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/04/2020
ms.locfileid: "3024686"
---
# <a name="dynamics-365-commerce-preview-environment-overview"></a><span data-ttu-id="b2ca5-103">Dynamics 365 Commerce プレビュー環境の概要</span><span class="sxs-lookup"><span data-stu-id="b2ca5-103">Dynamics 365 Commerce preview environment overview</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="b2ca5-104">このトピックでは、Microsoft Dynamics 365 Commerce プレビュー環境の概要を示します。</span><span class="sxs-lookup"><span data-stu-id="b2ca5-104">This topic gives an overview of the Microsoft Dynamics 365 Commerce preview environment.</span></span>

## <a name="overview"></a><span data-ttu-id="b2ca5-105">概要</span><span class="sxs-lookup"><span data-stu-id="b2ca5-105">Overview</span></span>

<span data-ttu-id="b2ca5-106">Commerce プレビュー環境は Dynamics 365 Commerce のオプションのエンドツーエンドのプレビュー環境であり、潜在顧客が一般公開前に Commerce 製品を試すことができます。</span><span class="sxs-lookup"><span data-stu-id="b2ca5-106">The Commerce preview environment is an optional end-to-end preview environment of Dynamics 365 Commerce that lets potential customers try out the Commerce product before its general release to the public.</span></span>

<span data-ttu-id="b2ca5-107">機能に影響しないいくつかの制限事項とは別に、Commerce プレビュー環境は完全なコマース経験を提供し、顧客および実装パートナーが製品の評価、フィードバックの提供、およびフィット/ギャップ分析を行うために使用できます。</span><span class="sxs-lookup"><span data-stu-id="b2ca5-107">Aside from some minor limitations that don't affect features or functionality, the Commerce preview environment provides the complete Commerce experience, and can be used by customers and implementation partners to evaluate the product, provide feedback, and do fit/gap analysis.</span></span>

## <a name="limitations-of-the-commerce-preview-environment"></a><span data-ttu-id="b2ca5-108">Commerce プレビュー環境の制限事項</span><span class="sxs-lookup"><span data-stu-id="b2ca5-108">Limitations of the Commerce preview environment</span></span>

<span data-ttu-id="b2ca5-109">Commerce プレビュー環境では Commerce 機能の完全なセットが提供されますが、いくつかの制限事項があります。</span><span class="sxs-lookup"><span data-stu-id="b2ca5-109">Although the Commerce preview environment provides the full set of Commerce features and functionality, there are some minor limitations:</span></span>

- <span data-ttu-id="b2ca5-110">Commerce プレビュー環境自体には地理的な制限事項はありませんが、Retail Cloud Scale Unit (RCSU) および E コマース アプリケーションなどの環境のコンポーネントは米国でのみプロビジョニングできます。</span><span class="sxs-lookup"><span data-stu-id="b2ca5-110">Although the Commerce preview environment itself has no geographical limitations, components of the environment, such as the Retail Cloud Scale Unit (RCSU) and e-Commerce applications, can be provisioned only in the United States.</span></span>
- <span data-ttu-id="b2ca5-111">Commerce プレビュー環境の使用には、E コマースのプロビジョニング日から 30 日間という期限設定があります。</span><span class="sxs-lookup"><span data-stu-id="b2ca5-111">Use of the Commerce preview environment is limited to 30 days from the date when e-Commerce is provisioned.</span></span>
- <span data-ttu-id="b2ca5-112">Commerce プレビュー環境は、デモ トポロジを使用する環境でのみ正常に展開および初期化でき、環境のすべてのコンポーネントが単一の仮想マシン (VM) に展開されます。</span><span class="sxs-lookup"><span data-stu-id="b2ca5-112">The Commerce preview environment can be successfully deployed and initialized only in an environment that uses the demo topology, where all components of an environment are deployed in a single virtual machine (VM).</span></span> <span data-ttu-id="b2ca5-113">この OneBox VMトポロジの主な制限事項は、プレビュー環境がサポートできる同時ユーザー数です。</span><span class="sxs-lookup"><span data-stu-id="b2ca5-113">The main limitation of this OneBox VM topology is the number of concurrent users that the preview environment can support.</span></span>
- <span data-ttu-id="b2ca5-114">Commerce プレビュー環境は、Commerce 製品の一般提供 (GA) 前に評価できます。</span><span class="sxs-lookup"><span data-stu-id="b2ca5-114">The Commerce preview environment can be evaluated only until the general availability (GA) of the Commerce product.</span></span> <span data-ttu-id="b2ca5-115">新しいデモ環境は GA 後に使用できます。</span><span class="sxs-lookup"><span data-stu-id="b2ca5-115">New demo environments will be available after GA.</span></span>

## <a name="get-started"></a><span data-ttu-id="b2ca5-116">はじめに</span><span class="sxs-lookup"><span data-stu-id="b2ca5-116">Get started</span></span>

<span data-ttu-id="b2ca5-117">Commerce プレビュー環境をプロビジョニングする方法については、[Commerce プレビュー環境のプロビジョニング](provisioning-guide.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="b2ca5-117">To provision the Commerce preview environment, see [Provision a Commerce preview environment](provisioning-guide.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="b2ca5-118">追加リソース</span><span class="sxs-lookup"><span data-stu-id="b2ca5-118">Additional resources</span></span>

[<span data-ttu-id="b2ca5-119">Dynamics 365 Commerce プレビュー環境のプロビジョニング</span><span class="sxs-lookup"><span data-stu-id="b2ca5-119">Provision a Dynamics 365 Commerce preview environment</span></span>](provisioning-guide.md)

[<span data-ttu-id="b2ca5-120">Dynamics 365 Commerce レビュー環境のコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="b2ca5-120">Configure a Dynamics 365 Commerce preview environment</span></span>](cpe-post-provisioning.md)

[<span data-ttu-id="b2ca5-121">Dynamics 365 Commerce プレビュー環境のオプション機能のコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="b2ca5-121">Configure optional features for a Dynamics 365 Commerce preview environment</span></span>](cpe-optional-features.md)

[<span data-ttu-id="b2ca5-122">Dynamics 365 Commerce プレビュー環境に関するよく寄せられる質問</span><span class="sxs-lookup"><span data-stu-id="b2ca5-122">Dynamics 365 Commerce preview environment FAQ</span></span>](cpe-faq.md)
