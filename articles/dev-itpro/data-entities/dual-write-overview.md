---
title: Finance and Operations と Common Data Service 間のほぼリアル タイム データの統合
description: このトピックでは、Microsoft Dynamics 365 for Finance and Operations と Common Data Service 間の統合概要を提供します。
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 07/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: aa614c8e6a79a3f7a4f8f2f99f1f1bd1a67ac921
ms.sourcegitcommit: efcc0dee8bde5f8f93f6291e7f059ad426843e57
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/31/2019
ms.locfileid: "1797231"
---
# <a name="near-real-time-data-integration-between-finance-and-operations-and-common-data-service"></a><span data-ttu-id="89a8a-103">Finance and Operations と Common Data Service 間のほぼリアル タイム データの統合</span><span class="sxs-lookup"><span data-stu-id="89a8a-103">Near-real-time data integration between Finance and Operations and Common Data Service</span></span>

[!include [banner](../includes/banner.md)]

[!include [preview](../includes/preview-banner.md)]

<span data-ttu-id="89a8a-104">現在のデジタル世界では、ビジネス エコシステムが全体として Microsoft Dynamics 365 スイートを使用しています。</span><span class="sxs-lookup"><span data-stu-id="89a8a-104">In the current digital world, business ecosystems use the Microsoft Dynamics 365 suite as a whole.</span></span> <span data-ttu-id="89a8a-105">人材、顧客、運用、およびインターネット オブ シングス (IoT) デバイスからのデータが 1 つのソースに流れ込むため、デジタル フィードバック ループの営業案件があります。</span><span class="sxs-lookup"><span data-stu-id="89a8a-105">Because data from people, customers, operations, and Internet of Things (IoT) devices flows into one source, there is an opportunity for digital feedback loops.</span></span> <span data-ttu-id="89a8a-106">このエクスペリエンスを実現するには、Dynamics 365 for Finance and Operations と Dynamics 365 for Customer Engagement のアプリケーション間の統合が不可欠です。</span><span class="sxs-lookup"><span data-stu-id="89a8a-106">To achieve this experience, integration between Dynamics 365 for Finance and Operations and Dynamics 365 for Customer Engagement applications is essential.</span></span> <span data-ttu-id="89a8a-107">Customer Engagement アプリケーションは、Common Data Service の上に構築されています。</span><span class="sxs-lookup"><span data-stu-id="89a8a-107">Customer Engagement applications are built on top of Common Data Service.</span></span> <span data-ttu-id="89a8a-108">Finance and Operations データと Common Data Service 間の統合は、Customer Engagement アプリケーションが Finance and Operations に明確で流ちょうに通信できるようにします。</span><span class="sxs-lookup"><span data-stu-id="89a8a-108">Integration between Finance and Operations data with Common Data Service lets Customer Engagement applications communicate coherently and fluently with Finance and Operations.</span></span>

<span data-ttu-id="89a8a-109">Finance and Operations と Common Data Service は、デュアル書き込みフレームワークを介して、Finance and Operations と Customer Engagement 間のほぼリアルタイムのデータ同期を提供します。</span><span class="sxs-lookup"><span data-stu-id="89a8a-109">Finance and Operations and Common Data Service provide near-real-time data synchronization between Finance and Operations and Customer Engagement applications via a dual-write framework.</span></span> <span data-ttu-id="89a8a-110">補充は広く、Finance and Operations の 28 の表面領域にまたがります。</span><span class="sxs-lookup"><span data-stu-id="89a8a-110">The coverage is broad and spans 28 surface areas of Finance and Operations.</span></span> <span data-ttu-id="89a8a-111">目標は、アプリケーション間でビジネス プロセスを接続するシームレスなデータ フローを通じて、「One Dynamics 365」ユーザー エクスペリエンスを提供することです。</span><span class="sxs-lookup"><span data-stu-id="89a8a-111">The goal is to provide a "One Dynamics 365" user experience through seamless data flows that connect business processes across applications.</span></span>

![アーキテクチャの概要図](media/dual-write-overview.jpg)

<span data-ttu-id="89a8a-113">お客様には、以下のバリュー プロポジションを利用できます。</span><span class="sxs-lookup"><span data-stu-id="89a8a-113">The following value propositions are available for customers:</span></span>

+ [<span data-ttu-id="89a8a-114">Common Data Service の組織階層</span><span class="sxs-lookup"><span data-stu-id="89a8a-114">Organization hierarchy in Common Data Service</span></span>](dual-write-organization.md)
+ [<span data-ttu-id="89a8a-115">Common Data Service 企業理念</span><span class="sxs-lookup"><span data-stu-id="89a8a-115">Company concept in Common Data Service</span></span>](dual-write-company.md)
+ [<span data-ttu-id="89a8a-116">統合済み顧客マスター</span><span class="sxs-lookup"><span data-stu-id="89a8a-116">Integrated customer master</span></span>](dual-write-customer.md)
+ [<span data-ttu-id="89a8a-117">統合済み仕入先マスター</span><span class="sxs-lookup"><span data-stu-id="89a8a-117">Integrated vendor master</span></span>](dual-write-vendor.md)
+ <span data-ttu-id="89a8a-118">統合製品マスター</span><span class="sxs-lookup"><span data-stu-id="89a8a-118">Unified product master</span></span>

## <a name="system-requirements"></a><span data-ttu-id="89a8a-119">システム要件</span><span class="sxs-lookup"><span data-stu-id="89a8a-119">System requirements</span></span>

<span data-ttu-id="89a8a-120">同期、双方向、ほぼリアル タイムのデータ フローには、次のバージョンが必要です。</span><span class="sxs-lookup"><span data-stu-id="89a8a-120">Synchronous, bidirectional, near-real-time data flows require the following versions:</span></span>

+ <span data-ttu-id="89a8a-121">Microsoft Dynamics 365 for Finance and Operationsバージョン 10.0.4 (2019 年 7 月) プラットフォーム更新プログラム 28 以降</span><span class="sxs-lookup"><span data-stu-id="89a8a-121">Microsoft Dynamics 365 for Finance and Operations version 10.0.4 (July 2019) with Platform update 28, or later</span></span>
+ <span data-ttu-id="89a8a-122">Microsoft Dynamics 365 for Customer Engagement、プラットフォーム バージョン 9.1 (4.2) 以降</span><span class="sxs-lookup"><span data-stu-id="89a8a-122">Microsoft Dynamics 365 for Customer Engagement, Platform version 9.1 (4.2) or later</span></span>

## <a name="setup-instructions"></a><span data-ttu-id="89a8a-123">設定指示</span><span class="sxs-lookup"><span data-stu-id="89a8a-123">Setup instructions</span></span>

<span data-ttu-id="89a8a-124">Finance and Operations と Common Data Service 間の統合を設定するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="89a8a-124">Follow these steps to set up integration between Finance and Operations and Common Data Service.</span></span>
    
1. <span data-ttu-id="89a8a-125">デュアル書き込みシステムの設定については、デュアル書き込みプレビューの発表の[ステップ バイ ステップ ガイド](https://aka.ms/dualwrite-docs) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="89a8a-125">For the setup of the dual-write system, see the [step-by-step guide](https://aka.ms/dualwrite-docs) on Announcing Dual Write Preview.</span></span>
2. <span data-ttu-id="89a8a-126">[Finance and Operations、Common Data Service、および Customer Engagement 統合](https://www.yammer.com/dynamicsaxfeedbackprograms/#/threads/inGroup?type=in_group&feedId=66052096)Yammer グループから、ソリューションをダウンロードしてインストールします。</span><span class="sxs-lookup"><span data-stu-id="89a8a-126">Download and install the solution from the [Finance and Operations, Common Data Service, and Customer Engagement Integration](https://www.yammer.com/dynamicsaxfeedbackprograms/#/threads/inGroup?type=in_group&feedId=66052096) Yammer group.</span></span> <span data-ttu-id="89a8a-127">パッケージには、次の 5 つのソリューションが含まれています。</span><span class="sxs-lookup"><span data-stu-id="89a8a-127">The package contains five solutions:</span></span>

    + <span data-ttu-id="89a8a-128">Dynamics365Company</span><span class="sxs-lookup"><span data-stu-id="89a8a-128">Dynamics365Company</span></span>
    + <span data-ttu-id="89a8a-129">CurrencyExchangeRates</span><span class="sxs-lookup"><span data-stu-id="89a8a-129">CurrencyExchangeRates</span></span>
    + <span data-ttu-id="89a8a-130">Dynamics365FinanceAndOperationsCommon</span><span class="sxs-lookup"><span data-stu-id="89a8a-130">Dynamics365FinanceAndOperationsCommon</span></span>
    + <span data-ttu-id="89a8a-131">Dynamics365FinanceCommon</span><span class="sxs-lookup"><span data-stu-id="89a8a-131">Dynamics365FinanceCommon</span></span>
    + <span data-ttu-id="89a8a-132">Dynamics365SupplyChainCommon</span><span class="sxs-lookup"><span data-stu-id="89a8a-132">Dynamics365SupplyChainCommon</span></span>

3. <span data-ttu-id="89a8a-133">[初期参照データを同期](dual-write-initial.md) の実行順序に従います。</span><span class="sxs-lookup"><span data-stu-id="89a8a-133">Follow the execution order for [synchronizing initial reference data](dual-write-initial.md).</span></span>
4. <span data-ttu-id="89a8a-134">デュアル書き込み同期の問題が発生した場合は、[データ統合のトラブルシューティング ガイド](dual-write-troubleshooting.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="89a8a-134">If you encounter dual-write synchronization issues, see the [Troubleshooting guide for data integration](dual-write-troubleshooting.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="89a8a-135">デュアル書き込みと[見込み客を現金化](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/accounts-template-mapping-direct) を並べて実行できません。</span><span class="sxs-lookup"><span data-stu-id="89a8a-135">You can’t run dual-write and [Prospect to cash](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/accounts-template-mapping-direct) side-by-side.</span></span> <span data-ttu-id="89a8a-136">見込み客を現金化するソリューションを実行している場合は、アンインストールする必要があります。</span><span class="sxs-lookup"><span data-stu-id="89a8a-136">If you're running the Prospect to cash solution, you must uninstall it.</span></span> <span data-ttu-id="89a8a-137">また、見込み客の現金化ソルーションの一部である顧客および仕入先のデュアル書き込みテンプレートを無効にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="89a8a-137">You must also disable the customer and vendor dual-write templates that are part of the Prospect to cash solution.</span></span>
