---
title: Dynamics 365 Commerce 評価環境の概要
description: このトピックでは、Microsoft Dynamics 365 Commerce の環境環境の概要を説明します。
author: v-chgri
manager: annbe
ms.date: 07/16/2020
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
ms.openlocfilehash: 25c0574e8d4502bcb846fba0ddf913d81eded87b
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/13/2020
ms.locfileid: "4413647"
---
# <a name="dynamics-365-commerce-evaluation-environment-overview"></a><span data-ttu-id="3d83b-103">Dynamics 365 Commerce 評価環境の概要</span><span class="sxs-lookup"><span data-stu-id="3d83b-103">Dynamics 365 Commerce evaluation environment overview</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="3d83b-104">このトピックでは、Microsoft Dynamics 365 Commerce の環境環境の概要を説明します。</span><span class="sxs-lookup"><span data-stu-id="3d83b-104">This topic gives an overview of the Microsoft Dynamics 365 Commerce evaluation environment.</span></span>

> [!NOTE]
> <span data-ttu-id="3d83b-105">コマースの評価環境は一般的には提供されておらず、パートナーや顧客からのリクエストに応じて付与されます。</span><span class="sxs-lookup"><span data-stu-id="3d83b-105">Commerce evaluation environments aren't generally available, and are granted to partners and customers on a per-request basis.</span></span> <span data-ttu-id="3d83b-106">ライセンスの詳細については、Microsoft パートナーにお問い合わせください。</span><span class="sxs-lookup"><span data-stu-id="3d83b-106">For more information, reach out to your Microsoft partner contact.</span></span>

## <a name="overview"></a><span data-ttu-id="3d83b-107">概要</span><span class="sxs-lookup"><span data-stu-id="3d83b-107">Overview</span></span>

<span data-ttu-id="3d83b-108">コマースの評価環境は、パートナーや見込み顧客にコマース製品を試用できる、 Dynamics 365 Commerce のオプションのエンドツーエンド環境です。</span><span class="sxs-lookup"><span data-stu-id="3d83b-108">The Commerce evaluation environment is an optional end-to-end environment of Dynamics 365 Commerce that lets partners and potential customers try out the Commerce product.</span></span>

<span data-ttu-id="3d83b-109">評価環境は、プロビジョニング後に必要となる手順を減らす目的でに、部分的に事前に構成されています。</span><span class="sxs-lookup"><span data-stu-id="3d83b-109">Evaluation environments are partially preconfigured to reduce the required post-provisioning steps.</span></span>

<span data-ttu-id="3d83b-110">機能や機能に影響を与えない軽微な制限事項とは別に、コマースの評価環境は完全なコマースの経験を提供し、顧客や実装パートナーが製品の評価、フィードバックの提供、フィット アンド ギャップ分析に使用することができます。</span><span class="sxs-lookup"><span data-stu-id="3d83b-110">Aside from some minor limitations that don't affect features or functionality, the Commerce evaluation environment provides the complete Commerce experience, and can be used by customers and implementation partners to evaluate the product, provide feedback, and do fit/gap analysis.</span></span>

## <a name="limitations-of-the-commerce-evaluation-environment"></a><span data-ttu-id="3d83b-111">コマースの評価環境の制限事項</span><span class="sxs-lookup"><span data-stu-id="3d83b-111">Limitations of the Commerce evaluation environment</span></span>

<span data-ttu-id="3d83b-112">コマースの評価環境では、コマースの機能の完全なセットが提供されますが、いくつかの制限事項があります。</span><span class="sxs-lookup"><span data-stu-id="3d83b-112">Although the Commerce evaluation environment provides the full set of Commerce features and functionality, there are some minor limitations:</span></span>

- <span data-ttu-id="3d83b-113">コマースの評価環境自体には地理的な制限はありませんが、Retail Cloud Scale Unit (RCSU) や eコマース アプリケーションなどの環境の構成要素は、米国内のみでプロビジョニングできます。</span><span class="sxs-lookup"><span data-stu-id="3d83b-113">Although the Commerce evaluation environment itself has no geographical limitations, components of the environment, such as the Retail Cloud Scale Unit (RCSU) and e-Commerce applications, should be provisioned only in the United States.</span></span>
- <span data-ttu-id="3d83b-114">コマースの評価環境の使用には、eコマースのプロビジョニング日から 30 日間という期限の設定があります。</span><span class="sxs-lookup"><span data-stu-id="3d83b-114">Use of the Commerce evaluation environment is limited to 30 days from the date when e-Commerce is provisioned.</span></span>
- <span data-ttu-id="3d83b-115">コマースの評価環境は、環境のすべてのコンポーネントが単一のクラウド ホスト仮想マシン (VM) 上にデプロイされているデモ トポロジを使用する環境でのみ、正常にデプロイや初期化が可能です。</span><span class="sxs-lookup"><span data-stu-id="3d83b-115">The Commerce evaluation environment can be successfully deployed and initialized only in an environment that uses the demo topology, where all components of an environment are deployed on a single cloud-hosted virtual machine (VM).</span></span> <span data-ttu-id="3d83b-116">このトポロジの主な制限は、環境が対応できる同時使用ユーザー数です。</span><span class="sxs-lookup"><span data-stu-id="3d83b-116">The main limitation of this topology is the number of concurrent users that the environment can support.</span></span>

## <a name="get-started"></a><span data-ttu-id="3d83b-117">はじめに</span><span class="sxs-lookup"><span data-stu-id="3d83b-117">Get started</span></span>

<span data-ttu-id="3d83b-118">コマースの評価環境をプロビジョニングする方法については、[コマースのプレビュー環境をプロビジョニングする](provisioning-guide.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="3d83b-118">To provision the Commerce evaluation environment, see [Provision a Commerce evaluation environment](provisioning-guide.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="3d83b-119">追加リソース</span><span class="sxs-lookup"><span data-stu-id="3d83b-119">Additional resources</span></span>

[<span data-ttu-id="3d83b-120">Dynamics 365 Commerce 評価環境をプロビジョニングする</span><span class="sxs-lookup"><span data-stu-id="3d83b-120">Provision a Dynamics 365 Commerce evaluation environment</span></span>](provisioning-guide.md)

[<span data-ttu-id="3d83b-121">Dynamics 365 Commerce の評価環境を構成する</span><span class="sxs-lookup"><span data-stu-id="3d83b-121">Configure a Dynamics 365 Commerce evaluation environment</span></span>](cpe-post-provisioning.md)

[<span data-ttu-id="3d83b-122">Dynamics 365 Commerce 評価環境で BOPIS を構成する</span><span class="sxs-lookup"><span data-stu-id="3d83b-122">Configure BOPIS in a Dynamics 365 Commerce evaluation environment</span></span>](cpe-bopis.md)

[<span data-ttu-id="3d83b-123">Dynamics 365 Commerce 評価環境のオプション機能を構成する</span><span class="sxs-lookup"><span data-stu-id="3d83b-123">Configure optional features for a Dynamics 365 Commerce evaluation environment</span></span>](cpe-optional-features.md)

[<span data-ttu-id="3d83b-124">Dynamics 365 Commerce 評価環境に関するよく寄せられる質問</span><span class="sxs-lookup"><span data-stu-id="3d83b-124">Dynamics 365 Commerce evaluation environment FAQ</span></span>](cpe-faq.md)
