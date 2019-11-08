---
title: ほぼリアルタイムの Common Data Service とのデータ統合
description: このトピックでは、Finance and Operations と Common Data Service 間の統合の概要を提供します。
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
ms.openlocfilehash: d70bce4e47c05a7974c1b974fdca17682e5370aa
ms.sourcegitcommit: 75db3b75d35d27034f9b56e7119c9d0cb7666830
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/03/2019
ms.locfileid: "2550860"
---
# <a name="near-real-time-data-integration-with-common-data-service"></a><span data-ttu-id="df65b-103">ほぼリアルタイムの Common Data Service とのデータ統合</span><span class="sxs-lookup"><span data-stu-id="df65b-103">Near-real-time data integration with Common Data Service</span></span>

[!include [banner](../includes/banner.md)]

[!include [preview](../includes/preview-banner.md)]

<span data-ttu-id="df65b-104">現在のデジタル世界では、ビジネス エコシステムが全体として Microsoft Dynamics 365 アプリケーションを使用しています。</span><span class="sxs-lookup"><span data-stu-id="df65b-104">In the current digital world, business ecosystems use Microsoft Dynamics 365 applications as a whole.</span></span> <span data-ttu-id="df65b-105">人材、顧客、運用、およびインターネット オブ シングス (IoT) デバイスからのデータが 1 つのソースに流れ込むため、デジタル フィードバック ループの営業案件があります。</span><span class="sxs-lookup"><span data-stu-id="df65b-105">Because data from people, customers, operations, and Internet of Things (IoT) devices flows into one source, there is an opportunity for digital feedback loops.</span></span> <span data-ttu-id="df65b-106">このエクスペリエンスを実現するには、Finance and Operations アプリとその他の Dynamics 365 アプリケーション間の統合が不可欠です。</span><span class="sxs-lookup"><span data-stu-id="df65b-106">To achieve this experience, integration between Finance and Operations apps and other Dynamics 365 applications is essential.</span></span> <span data-ttu-id="df65b-107">一部のアプリケーションは、Common Data Service の上に構築されています。</span><span class="sxs-lookup"><span data-stu-id="df65b-107">Some applications are built on top of Common Data Service.</span></span> <span data-ttu-id="df65b-108">Finance and Operations アプリのデータと Common Data Service 間の統合は、他のアプリケーションが Finance and Operations に一貫して流ちょうに通信できるようにします。</span><span class="sxs-lookup"><span data-stu-id="df65b-108">Integration between Finance and Operations apps data with Common Data Service lets other applications communicate coherently and fluently with Finance and Operations.</span></span>

<span data-ttu-id="df65b-109">Finance and Operations アプリと Common Data Service は、デュアル書き込みフレームワークを介して、Finance and Operations アプリとその他の Dynamics 365 アプリケーション間のほぼリアルタイムのデータ同期を提供します。</span><span class="sxs-lookup"><span data-stu-id="df65b-109">Finance and Operations apps and Common Data Service provide near-real-time data synchronization between Finance and Operations apps and other Dynamics 365 applications via a dual-write framework.</span></span> <span data-ttu-id="df65b-110">範囲は広く、アプリケーションの 28 の表面領域にまたがります。</span><span class="sxs-lookup"><span data-stu-id="df65b-110">The coverage is broad and spans 28 surface areas of the application.</span></span> <span data-ttu-id="df65b-111">目標は、アプリケーション間でビジネス プロセスを接続するシームレスなデータ フローを通じて、「One Dynamics 365」ユーザー エクスペリエンスを提供することです。</span><span class="sxs-lookup"><span data-stu-id="df65b-111">The goal is to provide a "One Dynamics 365" user experience through seamless data flows that connect business processes across applications.</span></span>

![アーキテクチャの概要図](media/dual-write-overview.jpg)

<span data-ttu-id="df65b-113">お客様には、以下のバリュー プロポジションを利用できます。</span><span class="sxs-lookup"><span data-stu-id="df65b-113">The following value propositions are available for customers:</span></span>

+ [<span data-ttu-id="df65b-114">Common Data Service の組織階層</span><span class="sxs-lookup"><span data-stu-id="df65b-114">Organization hierarchy in Common Data Service</span></span>](dual-write-organization.md)
+ [<span data-ttu-id="df65b-115">Common Data Service 企業理念</span><span class="sxs-lookup"><span data-stu-id="df65b-115">Company concept in Common Data Service</span></span>](dual-write-company.md)
+ [<span data-ttu-id="df65b-116">統合済み顧客マスター</span><span class="sxs-lookup"><span data-stu-id="df65b-116">Integrated customer master</span></span>](dual-write-customer.md)
+ [<span data-ttu-id="df65b-117">統合済み仕入先マスター</span><span class="sxs-lookup"><span data-stu-id="df65b-117">Integrated vendor master</span></span>](dual-write-vendor.md)
+ <span data-ttu-id="df65b-118">統合製品マスター</span><span class="sxs-lookup"><span data-stu-id="df65b-118">Unified product master</span></span>

## <a name="system-requirements"></a><span data-ttu-id="df65b-119">システム要件</span><span class="sxs-lookup"><span data-stu-id="df65b-119">System requirements</span></span>

<span data-ttu-id="df65b-120">同期、双方向、ほぼリアル タイムのデータ フローには、次のバージョンが必要です。</span><span class="sxs-lookup"><span data-stu-id="df65b-120">Synchronous, bidirectional, near-real-time data flows require the following versions:</span></span>

+ <span data-ttu-id="df65b-121">Microsoft Dynamics 365 for Finance and Operationsバージョン 10.0.4 (2019 年 7 月) プラットフォーム更新プログラム 28 以降</span><span class="sxs-lookup"><span data-stu-id="df65b-121">Microsoft Dynamics 365 for Finance and Operations version 10.0.4 (July 2019) with Platform update 28, or later</span></span>
+ <span data-ttu-id="df65b-122">Microsoft Dynamics 365 for Customer Engagement、プラットフォーム バージョン 9.1 (4.2) 以降</span><span class="sxs-lookup"><span data-stu-id="df65b-122">Microsoft Dynamics 365 for Customer Engagement, Platform version 9.1 (4.2) or later</span></span>

## <a name="setup-instructions"></a><span data-ttu-id="df65b-123">設定指示</span><span class="sxs-lookup"><span data-stu-id="df65b-123">Setup instructions</span></span>

<span data-ttu-id="df65b-124">Finance and Operations アプリと Common Data Service 間の統合を設定するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="df65b-124">Follow these steps to set up integration between Finance and Operations apps and Common Data Service.</span></span>
    
1. <span data-ttu-id="df65b-125">デュアル書き込みシステムの設定については、デュアル書き込みプレビューの発表の[ステップ バイ ステップ ガイド](https://aka.ms/dualwrite-docs) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="df65b-125">For the setup of the dual-write system, see the [step-by-step guide](https://aka.ms/dualwrite-docs) on Announcing Dual Write Preview.</span></span>
2. <span data-ttu-id="df65b-126">[Finance and Operations、Common Data Service、および Customer Engagement 統合](https://www.yammer.com/dynamicsaxfeedbackprograms/#/threads/inGroup?type=in_group&feedId=66052096)Yammer グループから、ソリューションをダウンロードしてインストールします。</span><span class="sxs-lookup"><span data-stu-id="df65b-126">Download and install the solution from the [Finance and Operations, Common Data Service, and Customer Engagement Integration](https://www.yammer.com/dynamicsaxfeedbackprograms/#/threads/inGroup?type=in_group&feedId=66052096) Yammer group.</span></span> <span data-ttu-id="df65b-127">パッケージには、次の 5 つのソリューションが含まれています。</span><span class="sxs-lookup"><span data-stu-id="df65b-127">The package contains five solutions:</span></span>

    + <span data-ttu-id="df65b-128">Dynamics365Company</span><span class="sxs-lookup"><span data-stu-id="df65b-128">Dynamics365Company</span></span>
    + <span data-ttu-id="df65b-129">CurrencyExchangeRates</span><span class="sxs-lookup"><span data-stu-id="df65b-129">CurrencyExchangeRates</span></span>
    + <span data-ttu-id="df65b-130">Dynamics365FinanceAndOperationsCommon</span><span class="sxs-lookup"><span data-stu-id="df65b-130">Dynamics365FinanceAndOperationsCommon</span></span>
    + <span data-ttu-id="df65b-131">Dynamics365FinanceCommon</span><span class="sxs-lookup"><span data-stu-id="df65b-131">Dynamics365FinanceCommon</span></span>
    + <span data-ttu-id="df65b-132">Dynamics365SupplyChainCommon</span><span class="sxs-lookup"><span data-stu-id="df65b-132">Dynamics365SupplyChainCommon</span></span>

3. <span data-ttu-id="df65b-133">[初期参照データを同期](dual-write-initial.md) の実行順序に従います。</span><span class="sxs-lookup"><span data-stu-id="df65b-133">Follow the execution order for [synchronizing initial reference data](dual-write-initial.md).</span></span>
4. <span data-ttu-id="df65b-134">デュアル書き込み同期の問題が発生した場合は、[データ統合のトラブルシューティング ガイド](dual-write-troubleshooting.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="df65b-134">If you encounter dual-write synchronization issues, see the [Troubleshooting guide for data integration](dual-write-troubleshooting.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="df65b-135">デュアル書き込みと[見込み客を現金化](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/accounts-template-mapping-direct) を並べて実行できません。</span><span class="sxs-lookup"><span data-stu-id="df65b-135">You can’t run dual-write and [Prospect to cash](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/accounts-template-mapping-direct) side-by-side.</span></span> <span data-ttu-id="df65b-136">見込み客を現金化するソリューションを実行している場合は、アンインストールする必要があります。</span><span class="sxs-lookup"><span data-stu-id="df65b-136">If you're running the Prospect to cash solution, you must uninstall it.</span></span> <span data-ttu-id="df65b-137">また、見込み客の現金化ソルーションの一部である顧客および仕入先のデュアル書き込みテンプレートを無効にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="df65b-137">You must also disable the customer and vendor dual-write templates that are part of the Prospect to cash solution.</span></span>
