---
title: Commerce データ所在地
description: このトピックでは Commerce Scale Unit (クラウド) を配置するときのデータ所在地に関する考慮事項を説明します。
author: AamirAllaq
manager: AnnBe
ms.date: 10/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: aamiral
ms.search.validFrom: 2018-4-30
ms.dyn365.ops.version: 8
ms.openlocfilehash: 8f54caeec9c71c4a1d1c7fa28f88da73c4bbc924
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/05/2020
ms.locfileid: "4683969"
---
# <a name="commerce-data-residency"></a><span data-ttu-id="4f6d5-103">Commerce データ所在地</span><span class="sxs-lookup"><span data-stu-id="4f6d5-103">Commerce data residency</span></span>

[!include[banner](../includes/banner.md)]


## <a name="choose-a-region"></a><span data-ttu-id="4f6d5-104">地域を選択</span><span class="sxs-lookup"><span data-stu-id="4f6d5-104">Choose a region</span></span>

<span data-ttu-id="4f6d5-105">Commerce Scale Unit (クラウド) を初期化するときは、ホストするデータ センターの場所を選択する必要があります。</span><span class="sxs-lookup"><span data-stu-id="4f6d5-105">When you initialize a Commerce Scale Unit (cloud), you need to select a data center location to host.</span></span> <span data-ttu-id="4f6d5-106">ネットワークの待機時間を最小限に抑えてパフォーマンスを向上するには、RCSU を使用してサービスを提供する予定のチャネルに最も近いデータ センターの場所を選択する必要があります。</span><span class="sxs-lookup"><span data-stu-id="4f6d5-106">To minimize network latency and improve performance, you should choose a datacenter location that is in proximity to the channels that you plan to serve using the RCSU.</span></span> <span data-ttu-id="4f6d5-107">各データ センターのおおよその場所を参照するには [Azure のリージョン](https://azure.microsoft.com/global-infrastructure/regions/) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="4f6d5-107">To reference approximate locations of each datacenter, see [Azure regions](https://azure.microsoft.com/global-infrastructure/regions/).</span></span> <span data-ttu-id="4f6d5-108">[Azure 速度の参照](https://azurespeedtest.azurewebsites.net/) などの Web ベースのユーティリティを参照して、各店舗の場所から Azure データ センターへの待機時間を測定することもできます。</span><span class="sxs-lookup"><span data-stu-id="4f6d5-108">You can also reference a web-based utility, such as [Azure speed reference](https://azurespeedtest.azurewebsites.net/), and measure latency to Azure datacenters from each store location.</span></span> <span data-ttu-id="4f6d5-109">これは RCSU を初期化するときデータ センターを正しく選択することに役立ちます。</span><span class="sxs-lookup"><span data-stu-id="4f6d5-109">This can help you to make the right choice of datacenter when you initialize the RCSU.</span></span>

## <a name="data-between-regions"></a><span data-ttu-id="4f6d5-110">地域間のデータ</span><span class="sxs-lookup"><span data-stu-id="4f6d5-110">Data between regions</span></span>

<span data-ttu-id="4f6d5-111">本社とは異なる場所のデータ センターで RCSU を初期化すると、データはこれらのデータ センター間を定期的に同期して移動します。</span><span class="sxs-lookup"><span data-stu-id="4f6d5-111">If you initialize RCSU in a data center that is different than where your head office is located, the data will travel between these data centers with periodic synchronization.</span></span> <span data-ttu-id="4f6d5-112">システムは特定の種類のデータを転送するようにコンフィギュレーション済みです。</span><span class="sxs-lookup"><span data-stu-id="4f6d5-112">The system is pre-configured to transfer specific types of data.</span></span> <span data-ttu-id="4f6d5-113">このコンフィギュレーションを変更して異なるデータを同期できます。</span><span class="sxs-lookup"><span data-stu-id="4f6d5-113">You can modify this configuration to synchronize different data.</span></span>

<span data-ttu-id="4f6d5-114">データ同期コンフィギュレーションを表示するには、**Retail とコマース** \> **バックオフィスの設定** \> **コマース スケジューラ** \> **スケジューラ ジョブ** に移動してデータ同期ジョブとサブジョブを表示します。</span><span class="sxs-lookup"><span data-stu-id="4f6d5-114">To view the data synchronization configuration, go to **Retail and Commerce** \> **Headquarters setup** \> **Commerce scheduler** \> **Scheduler jobs** to view the data synchronization jobs and sub-jobs.</span></span> <span data-ttu-id="4f6d5-115">同期中のフィールドを表示するには、サブジョブをクリックします。</span><span class="sxs-lookup"><span data-stu-id="4f6d5-115">To view the fields being synchronized, click through a sub-job.</span></span> 

## <a name="synchronize-specific-segments-of-records"></a><span data-ttu-id="4f6d5-116">レコードの特定の区分を同期する</span><span class="sxs-lookup"><span data-stu-id="4f6d5-116">Synchronize specific segments of records</span></span>

<span data-ttu-id="4f6d5-117">Commerce Data Exchange (CDX) を構成して、レコードの特定の区分のみを特定の RCSU に同期することができます。</span><span class="sxs-lookup"><span data-stu-id="4f6d5-117">You can configure Commerce Data Exchange (CDX) so that only specific segments of records are synchronized to specific RCSUs.</span></span> 

### <a name="prerequisites"></a><span data-ttu-id="4f6d5-118">必要条件</span><span class="sxs-lookup"><span data-stu-id="4f6d5-118">Prerequisites</span></span>

<span data-ttu-id="4f6d5-119">同期するレコード区分を構成する前に、チャネル データベース グループを構成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="4f6d5-119">Before you configure the record segments that will be synchronized, you need to configure Channel database groups.</span></span> <span data-ttu-id="4f6d5-120">これらのデータベース グループは、セグメント化されたデータを同期する各 CSU に対して構成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="4f6d5-120">These database groups must be configured for each CSU where you want to synchronize segmented data.</span></span> <span data-ttu-id="4f6d5-121">同じチャネル データベース グループ内のすべての CSU は、その CSU 内のすべてのチャネルにサービスを提供するのに必要なデータを受け取ります。</span><span class="sxs-lookup"><span data-stu-id="4f6d5-121">All CSUs in the same Channel database group receive the data that is needed to serve all the channels in that CSU.</span></span> <span data-ttu-id="4f6d5-122">セグメント化されたデータを同期させる予定の各 CSU チャネル データベースに対して、別々のデータベース グループを作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="4f6d5-122">You will need to create a separate database group for each CSU channel database where you plan to synchronize segmented data.</span></span> <span data-ttu-id="4f6d5-123">それには、次の手順を実行します:</span><span class="sxs-lookup"><span data-stu-id="4f6d5-123">To do this, perform the following steps:</span></span>

1. <span data-ttu-id="4f6d5-124">**Retail と Commerce** \> **Headquarters の設定** \> **Commerce スケジューラ** \> **チャネル データベース グループ** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="4f6d5-124">Go to **Retail and Commerce** \> **Headquarters setup** \> **Commerce scheduler** \> **Channel database group**.</span></span>
2. <span data-ttu-id="4f6d5-125">セグメント化されたデータを同期させる各 CSU に対して新しいデータベース グループを作成します。</span><span class="sxs-lookup"><span data-stu-id="4f6d5-125">Create a new database group for each CSU where you want to synchronize segmented data.</span></span>
3. <span data-ttu-id="4f6d5-126">**Retail と Commerce** \> **Retail と Commerce IT** \> **配送スケジュール** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="4f6d5-126">Go to **Retail and Commerce** \> **Retail and Commerce IT** \> **Distribution schedule**.</span></span>
4. <span data-ttu-id="4f6d5-127">新しく作成されたチャンネル データベース グループを各スケジューラ ジョブに追加します。</span><span class="sxs-lookup"><span data-stu-id="4f6d5-127">Add the newly created Channel database group to each scheduler job.</span></span>
5. <span data-ttu-id="4f6d5-128">**Retail とコマース** \> **バックオフィスの設定** \> **コマース スケジューラ** \> **チャネル データベース** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="4f6d5-128">Go to **Retail and Commerce** \> **Headquarters setup** \> **Commerce scheduler** \> **Channel database**.</span></span>
6. <span data-ttu-id="4f6d5-129">対応する Commerce Scale Unit (クラウド) のチャネル データベースを選択します。</span><span class="sxs-lookup"><span data-stu-id="4f6d5-129">Select the Channel database for the corresponding Commerce Scale Unit (cloud).</span></span>
7. <span data-ttu-id="4f6d5-130">**編集** を選択し、ステップ 2 で作成したチャネル データベース グループを選択します。</span><span class="sxs-lookup"><span data-stu-id="4f6d5-130">Select **Edit** and choose the channel database group that you created in step 2.</span></span>
8. <span data-ttu-id="4f6d5-131">**保存** を選択します。</span><span class="sxs-lookup"><span data-stu-id="4f6d5-131">Select **Save**.</span></span> 
9. <span data-ttu-id="4f6d5-132">選択したチャンネル データベースに対して **すべてのジョブの完全データ同期** を選択します。</span><span class="sxs-lookup"><span data-stu-id="4f6d5-132">Select **Full data sync for all jobs** for the selected channel database.</span></span>

### <a name="available-controls-for-synchronizing-segments-of-data-to-different-rcsus"></a><span data-ttu-id="4f6d5-133">データの区分を異なる RCSU に同期させるための利用可能なコントロール</span><span class="sxs-lookup"><span data-stu-id="4f6d5-133">Available controls for synchronizing segments of data to different RCSUs</span></span>

<span data-ttu-id="4f6d5-134">チャンネル コンフィギュレーション データは、特定の RCSU によって提供されるチャンネルに対してのみ同期されます。</span><span class="sxs-lookup"><span data-stu-id="4f6d5-134">Channel configuration data will only be synchronized for channels that are served by specific RCSUs.</span></span> <span data-ttu-id="4f6d5-135">たとえば、西ヨーロッパのチャネルで配信されるように構成されたチャネルのチャネル コンフィギュレーション データのみがその RCSU に同期されます。</span><span class="sxs-lookup"><span data-stu-id="4f6d5-135">For example, only the channel configuration data for channels that are configured to be served by the West Europe channel will be synchronized to that RCSU.</span></span> 

<span data-ttu-id="4f6d5-136">品揃えを使用して、商品および価格設定に関連するデータを特定のチャネルでセグメント化できます。</span><span class="sxs-lookup"><span data-stu-id="4f6d5-136">Using assortments, product and pricing related data can be segmented by specific channels.</span></span> <span data-ttu-id="4f6d5-137">たとえば、北米の店舗が婦人靴のみを販売し、西ヨーロッパの店舗がスポーツ用品のみを販売する場合は、品揃えを使用してこのデータをセグメント化できます。</span><span class="sxs-lookup"><span data-stu-id="4f6d5-137">For example, if your stores in North America only sell women's shoes and your stores in West Europe only sell sporting goods, you can use Assortments to segment this data.</span></span> <span data-ttu-id="4f6d5-138">データが RCSU に同期されている場合、婦人靴のデータは北米の RCSU にのみ同期され、スポーツ用品のデータは西ヨーロッパの RCSU にのみ同期されます。</span><span class="sxs-lookup"><span data-stu-id="4f6d5-138">When data is synchronized to RCSU, women's shoes data will only be synchronized to the North America RCSU and sporting goods data will only be synchronized to the West Europe RCSU.</span></span>

<span data-ttu-id="4f6d5-139">顧客レコードと従業員レコードはグローバル アドレス帳を使用して構成し、それは特定のチャネルに対して構成できます。</span><span class="sxs-lookup"><span data-stu-id="4f6d5-139">Customer and employee records are configured using the Global Address Book, which can be configured for specific channels.</span></span> <span data-ttu-id="4f6d5-140">たとえば、西ヨーロッパの RCSU と北米の RCSU で提供されるチャネル用に、顧客と従業員用に別々のアドレス帳を構成できます。</span><span class="sxs-lookup"><span data-stu-id="4f6d5-140">For example, you can configure separate address books for customers and employees for channels served by the West Europe RCSU and those for North America RCSU.</span></span>
