---
title: "Retail Store スケール ユニット"
description: "このトピックでは、Retail Store Scale Unit と、どんなときにそれを使用するかについて説明します。"
author: athinesh99
manager: AnnBe
ms.date: 12/17/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: IT Pro
ms.reviewer: sericks
ms.search.scope: Operations, Retail
ms.custom: 219714
ms.assetid: 773fb32d-14c1-4dc8-8330-0332c6a037a2
ms.search.region: Global
ms.search.industry: Retail
ms.author: athinesh
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: eeccbe753cd4adf86665a3c6a372fdbfca371799
ms.openlocfilehash: fe22915375f31ce8273b744685057dac2aff621c
ms.contentlocale: ja-jp
ms.lasthandoff: 12/19/2018

---

# <a name="retail-store-scale-unit"></a><span data-ttu-id="ef1a4-103">Retail Store スケール ユニット</span><span class="sxs-lookup"><span data-stu-id="ef1a4-103">Retail Store Scale Unit</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ef1a4-104">このトピックでは、Retail Store Scale Unit と、どんなときにそれを使用するかについて説明します。</span><span class="sxs-lookup"><span data-stu-id="ef1a4-104">This topic describes the Retail Store Scale Unit and when to use it.</span></span>

<a name="overview"></a><span data-ttu-id="ef1a4-105">概要</span><span class="sxs-lookup"><span data-stu-id="ef1a4-105">Overview</span></span>
--------

<span data-ttu-id="ef1a4-106">Retail Store Scale Unit は、バック オフィスまたは本社 (HQ) への常時インターネット接続がない店舗で製品の販売をサポートする一連の機能です。</span><span class="sxs-lookup"><span data-stu-id="ef1a4-106">Retail Store Scale Unit is a set of features that supports selling products in a store that have inconsistent internet connectivity to a back office or headquarters (HQ).</span></span> <span data-ttu-id="ef1a4-107">Store Scale Unit は、店舗内の工程専用に設計されており、インターネット サービスが貧弱な場合でもターミナル間トランザクションおよびシフト操作が可能になります。</span><span class="sxs-lookup"><span data-stu-id="ef1a4-107">The Store Scale Unit is designed specifically for in-store operation, and enables cross-terminal transactions and shift operations despite poor internet service.</span></span> <span data-ttu-id="ef1a4-108">バック オフィスに自動的に接続することで、インターネット接続がある場合に、店舗はクレジット カード トランザクションを処理し、ギフト カードを発行し、HQ シームレスにデータを同期させることができます。</span><span class="sxs-lookup"><span data-stu-id="ef1a4-108">By automatically connecting to the back office, when you do have internet connectivity, your store can seamlessly process credit card transactions, issue gift cards, and sync data with HQ.</span></span> <span data-ttu-id="ef1a4-109">Store スケール ユニットは、標準 HQ 配置でダウンロードできます。</span><span class="sxs-lookup"><span data-stu-id="ef1a4-109">The Store Scale Unit is available for download in the standard HQ deployment.</span></span>

## <a name="is-the-retail-store-scale-unit-right-for-you"></a><span data-ttu-id="ef1a4-110">Retail Store Scale Unit は自分に適切ですか。</span><span class="sxs-lookup"><span data-stu-id="ef1a4-110">Is the Retail Store Scale Unit right for you?</span></span>
<span data-ttu-id="ef1a4-111">Store スケール ユニットのセットアップを開始する前に、このオプションが店舗に好適かどうかを多少の時間をとって判断してください。</span><span class="sxs-lookup"><span data-stu-id="ef1a4-111">Before you begin setting up Store Scale Unit, take a moment determine whether this option is the right fit for your store.</span></span> <span data-ttu-id="ef1a4-112">Store Scale Unit は、インターネット接続が低速または切断されやすい店舗を持っており、各店舗のオンプレミスに Store Scale Unit を展開する柔軟性を必要としている小売業者が選択できる展開です。</span><span class="sxs-lookup"><span data-stu-id="ef1a4-112">Store Scale Unit is a deployment choice intended for retailers with store locations that have slow or intermittent internet connectivity, who need the flexibility of the Store Scale Unit deployed on premises in each store.</span></span> <span data-ttu-id="ef1a4-113">安定したインターネット接続があり、クラウド環境の待ち時間が小さいシナリオでは、Store Scale Unit をセットアップせずに店舗をクラウドとしてのみ運用することを考慮することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="ef1a4-113">In scenarios where a stable internet connection is available and there is low latency to the cloud environment, then it is recommended to consider operating the store as Cloud only, without setting up a Store Scale Unit.</span></span> <span data-ttu-id="ef1a4-114">始める前に、次の点を考慮してください。</span><span class="sxs-lookup"><span data-stu-id="ef1a4-114">Consider the following before you begin:</span></span>

-   <span data-ttu-id="ef1a4-115">Store Scale Unit またはクラウド専用システムとしての店舗を設定する営業案件は 1 件だけです。</span><span class="sxs-lookup"><span data-stu-id="ef1a4-115">You only have one opportunity to set up a store as a Store Scale Unit or a Cloud-only system.</span></span> <span data-ttu-id="ef1a4-116">Store スケール ユニット有効の店舗からクラウド専用の店舗への移動は、既定ではサポートされず、手動での構成が必要になります。</span><span class="sxs-lookup"><span data-stu-id="ef1a4-116">Moving from a Store Scale Unit-enabled store to a Cloud-Only store is not supported by default, and will require manual configuration.</span></span>
-   <span data-ttu-id="ef1a4-117">Store Scale Unit では、店舗内の MPOS および Cloud POS の両方がサポートされます。</span><span class="sxs-lookup"><span data-stu-id="ef1a4-117">Store Scale Unit will support both MPOS and Cloud POS within the store.</span></span>
-   <span data-ttu-id="ef1a4-118">Store Scale Unit は、1 台のコンピューター上の 1 ボックス配置トポロジでセットアップするか (推奨)、異なるコンピューター上の複数ボックス トポロジでセットアップできます。</span><span class="sxs-lookup"><span data-stu-id="ef1a4-118">Store Scale Unit can be set up in a one-box deployment topology on a single computer (recommended) or in a multi-box topology on different computers.</span></span>
-   <span data-ttu-id="ef1a4-119">ボックス環境の店舗スケール単位オプションを選択した場合、設定の多くは事前に設定されます。</span><span class="sxs-lookup"><span data-stu-id="ef1a4-119">If you choose the one-box Store Scale Unit option, most of the settings are pre-configured.</span></span> <span data-ttu-id="ef1a4-120">マルチボックス トポロジに関しては、手動でコンポーネント間の接続をコンフィギュレーションする必要があります。</span><span class="sxs-lookup"><span data-stu-id="ef1a4-120">For a multi-box topology, you will have to manually configure connections between components.</span></span>
-   <span data-ttu-id="ef1a4-121">Store スケール ユニットで、ユーザーはトランザクションの中断/取り消しおよびシフト操作と同様に、複数の POS デバイスでクロス ターミナル シナリオを実行できます。</span><span class="sxs-lookup"><span data-stu-id="ef1a4-121">In Store Scale Unit, users can perform cross-terminal scenarios across multiple POS devices, like suspend/recall transactions and shift operations.</span></span>
-   <span data-ttu-id="ef1a4-122">Store Scale Unit では、本社または支払プロバイダーへのインターネット接続がない限り、ユーザーはギフト カードの発行、製品の検索、クレジット カード トランザクションの実行などのリアルタイム操作を実行することはできません。</span><span class="sxs-lookup"><span data-stu-id="ef1a4-122">In Store Scale Unit, users cannot perform any real-time operations such as issuing gift cards, looking up products, or performing credit card transactions, unless there is internet connectivity to HQ or a payment provider.</span></span> <span data-ttu-id="ef1a4-123">取引の大部分でリアルタイムのトランザクションが関係する場合、Store Scale Unit が、HQ または支払プロバイダーへの接続を有効にするには、インターネットに常に接続されている必要があります。</span><span class="sxs-lookup"><span data-stu-id="ef1a4-123">If most of your transactions involve real time transactions, then your Store Scale Unit will always need internet connectivity to enable the connection to HQ or payment provider.</span></span>
-   <span data-ttu-id="ef1a4-124">店舗スケール ユニットでは、POS からチャネル データベースへの直接データベース接続はサポートされていません。</span><span class="sxs-lookup"><span data-stu-id="ef1a4-124">Direct database connectivity from POS to the channel database is not supported in the Store Scale Unit.</span></span> <span data-ttu-id="ef1a4-125">Store スケール ユニットの POS デバイスは、常に操作の実行に Retail Server を使用します。</span><span class="sxs-lookup"><span data-stu-id="ef1a4-125">The POS devices in the Store Scale Unit will always use the Retail Server for performing operations.</span></span>

> [!NOTE]
> <span data-ttu-id="ef1a4-126">Retail Store Scale Unit はオフラインでは置き換えられないことに注意してください。</span><span class="sxs-lookup"><span data-stu-id="ef1a4-126">It is critical to note that a Retail Store Scale Unit does not replace offline.</span></span> <span data-ttu-id="ef1a4-127">現時点では、オフライン データベースを持つ Retail Modern POS でのみオフライン機能を使用できます。</span><span class="sxs-lookup"><span data-stu-id="ef1a4-127">Currently, Retail Modern POS with an offline database is the only true way to have offline capabilities.</span></span> 

## <a name="get-started-with-store-scale-unit"></a><span data-ttu-id="ef1a4-128">Store Scale Unit の使用を開始する</span><span class="sxs-lookup"><span data-stu-id="ef1a4-128">Get started with Store Scale Unit</span></span>

<span data-ttu-id="ef1a4-129">開始するには、店舗規模単位の構成に関する [[Retail Store Scale Unit の設定およびインストール](retail-store-scale-unit-configuration-installation.md)] トピックを確認してください。</span><span class="sxs-lookup"><span data-stu-id="ef1a4-129">To get started, review the following topic on configuring the Store Scale Unit, [Retail Store Scale Unit configuration and installation](retail-store-scale-unit-configuration-installation.md).</span></span>

<a name="additional-resources"></a><span data-ttu-id="ef1a4-130">その他のリソース</span><span class="sxs-lookup"><span data-stu-id="ef1a4-130">Additional resources</span></span>
--------

[<span data-ttu-id="ef1a4-131">セルフ サービスによる Retail Store スケール ユニットのダウンロードおよびコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="ef1a4-131">Retail Store Scale Unit download and configuration through self-service</span></span>](retail-store-scale-unit-configuration-installation.md)




