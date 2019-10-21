---
title: Commerce Data Exchange と小売チャネルのコミュニケーション
description: このトピックでは、Commerce Data Exchange とその要素の概要を示します。 ここでは、Microsoft Dynamics 365 Retail および小売チャネルとの間でのデータの転送において各コンポーネントが果たす役割について説明します。
author: athinesh99
manager: AnnBe
ms.date: 11/14/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations, Retail
ms.custom: 27021
ms.assetid: 179b1629-ac90-4cfb-b46a-5bda56c4f451
ms.search.region: global
ms.search.industry: Retail
ms.author: athinesh
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: f5b3c446df69613e14f3363d42e7b79553e2736d
ms.sourcegitcommit: f87de0f949b5d60993b19e0f61297f02d42b5bef
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2019
ms.locfileid: "2025733"
---
# <a name="commerce-data-exchange-and-retail-channel-communications"></a><span data-ttu-id="b9d62-104">Commerce Data Exchange と小売チャネルのコミュニケーション</span><span class="sxs-lookup"><span data-stu-id="b9d62-104">Commerce Data Exchange and retail channel communications</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b9d62-105">このトピックでは、Commerce Data Exchange とその要素の概要を示します。</span><span class="sxs-lookup"><span data-stu-id="b9d62-105">This topic provides an overview of Commerce Data Exchange and its components.</span></span> <span data-ttu-id="b9d62-106">ここでは、Microsoft Dynamics 365 Retail Headquarters と小売チャネルとの間でのデータの転送において各コンポーネントが果たす役割について説明します。</span><span class="sxs-lookup"><span data-stu-id="b9d62-106">It explains the part that each component plays in the transfer of data between Microsoft Dynamics 365 Retail headquarters and retail channels.</span></span>

<a name="overview"></a><span data-ttu-id="b9d62-107">概要</span><span class="sxs-lookup"><span data-stu-id="b9d62-107">Overview</span></span>
--------

<span data-ttu-id="b9d62-108">Commerce Data Exchange は、小売用バックオフィスと、オンライン ストア、実際の店舗などの小売チャネルの間でデータを転送するシステムです。</span><span class="sxs-lookup"><span data-stu-id="b9d62-108">Commerce Data Exchange is a system that transfers data between Retail headquarters and retail channels, such as online stores or brick-and-mortar stores.</span></span> <span data-ttu-id="b9d62-109">小売チャンネルのデータを格納するデータベースは、小売りデータベースとは別にあります。</span><span class="sxs-lookup"><span data-stu-id="b9d62-109">The database that stores data for a retail channel is separate from the Retail database.</span></span> <span data-ttu-id="b9d62-110">チャンネルのデータベースは、小売トランザクションに必要なデータのみ格納します。</span><span class="sxs-lookup"><span data-stu-id="b9d62-110">The channel database holds only the data that is required for retail transactions.</span></span> <span data-ttu-id="b9d62-111">マスター データが小売用バックオフィスでコンフィギュレーションされ、チャネルに配分されます。</span><span class="sxs-lookup"><span data-stu-id="b9d62-111">Master data is configured in Retail headquarters and distributed to channels.</span></span> <span data-ttu-id="b9d62-112">トランザクション データは販売時点管理 (POS) システムまたはオンライン店舗で作成され、小売用バックオフィスにアップロードされます。</span><span class="sxs-lookup"><span data-stu-id="b9d62-112">Transactional data is created in the point of sale (POS) system or the online store, and then uploaded to Retail headquarters.</span></span> <span data-ttu-id="b9d62-113">データ配送は非同期です。</span><span class="sxs-lookup"><span data-stu-id="b9d62-113">Data distribution is asynchronous.</span></span> <span data-ttu-id="b9d62-114">つまり、データを収集してソースでパッケージングするプロセスは、データを取得して適用するプロセスとは別に行われます。</span><span class="sxs-lookup"><span data-stu-id="b9d62-114">In other words, the process of gathering and packaging data at the source occurs separately from the process of receiving and applying data at the destination.</span></span> <span data-ttu-id="b9d62-115">価格および在庫検索などのシナリオの場合、データはリアルタイムに取得する必要があります。</span><span class="sxs-lookup"><span data-stu-id="b9d62-115">For some scenarios, such as price and inventory lookups, data must be retrieved in real time.</span></span> <span data-ttu-id="b9d62-116">これらのシナリオをサポートするために、Commerce Data Exchange には、小売用バックオフィスとチャネル間のリアルタイム通信を可能にするサービスが含まれます。</span><span class="sxs-lookup"><span data-stu-id="b9d62-116">To support these scenarios, Commerce Data Exchange also includes a service that enables real-time communication between Retail headquarters and a channel.</span></span> 

<span data-ttu-id="b9d62-117">[![更新済小売グラフィック](./media/updated-retail-graphic.png)](./media/updated-retail-graphic.png)</span><span class="sxs-lookup"><span data-stu-id="b9d62-117">[![updated-retail-graphic](./media/updated-retail-graphic.png)](./media/updated-retail-graphic.png)</span></span>  

## <a name="async-service"></a><span data-ttu-id="b9d62-118">非同期サービス</span><span class="sxs-lookup"><span data-stu-id="b9d62-118">Async Service</span></span>
<span data-ttu-id="b9d62-119">小売データベースの Microsoft SQL Server 変更追跡は、チャネルに送信する必要のあるデータの変更内容を特定するのに使用されます。</span><span class="sxs-lookup"><span data-stu-id="b9d62-119">Microsoft SQL Server change tracking on the Retail database is used to determine the data changes that must be sent to channels.</span></span> <span data-ttu-id="b9d62-120">配送スケジュールに基づいて、小売用バックオフィスはそのデータをパッケージングして中央の保存場所 (Azure blob storage) に保存します。</span><span class="sxs-lookup"><span data-stu-id="b9d62-120">Based on a distribution schedule, Retail headquarters packages that data and saves it to central storage (Azure blob storage).</span></span> <span data-ttu-id="b9d62-121">別のバッチ処理は、このデータ パッケージをチャネルのデータベースに挿入するために Commerce Data Exchange: Async Client ライブラリを使用します。</span><span class="sxs-lookup"><span data-stu-id="b9d62-121">A separate batch process uses the Commerce Data Exchange: Async Client library to insert this data package into the channel database.</span></span> 

<span data-ttu-id="b9d62-122">[![非同期サービス](./media/async-300x239.png)](./media/async.png)</span><span class="sxs-lookup"><span data-stu-id="b9d62-122">[![Async Service](./media/async-300x239.png)](./media/async.png)</span></span>

### <a name="retail-scheduler"></a><span data-ttu-id="b9d62-123">小売用スケジューラ</span><span class="sxs-lookup"><span data-stu-id="b9d62-123">Retail scheduler</span></span>

<span data-ttu-id="b9d62-124">スケジューラ ジョブとは、データを配送場所へ (から) 配送するためのメカニズムです。</span><span class="sxs-lookup"><span data-stu-id="b9d62-124">Scheduler jobs are the mechanism for distributing data to and from locations.</span></span> <span data-ttu-id="b9d62-125">ジョブは、配分するデータを含むテーブルおよびテーブル フィールドを指定するサブジョブで構成されます。</span><span class="sxs-lookup"><span data-stu-id="b9d62-125">Jobs are made up of subjobs, which specify the tables and table fields that contain the data to distribute.</span></span> <span data-ttu-id="b9d62-126">小売用バックオフィスには、ほとんどの組織のレプリケーションの要件を満たすサブジョブと定義済スケジューラ ジョブが含まれます。</span><span class="sxs-lookup"><span data-stu-id="b9d62-126">Retail headquarters includes predefined scheduler jobs and subjobs that meet the replication requirements of most organizations.</span></span> <span data-ttu-id="b9d62-127">次のタイプの定義済ジョブが作成されます。</span><span class="sxs-lookup"><span data-stu-id="b9d62-127">The following types of predefined jobs are created:</span></span>

-   <span data-ttu-id="b9d62-128">**ダウンロード ジョブ** - ダウンロード ジョブは、小売用バックオフィスからチャネル データベースに変更されたデータを送信します。</span><span class="sxs-lookup"><span data-stu-id="b9d62-128">**Download jobs** – Download jobs send data that has changed from Retail headquarters to channel databases.</span></span> <span data-ttu-id="b9d62-129">レコードへの変更は、SQL Server 変更履歴によって追跡されます。</span><span class="sxs-lookup"><span data-stu-id="b9d62-129">Modifications to records are tracked through SQL Server change tracking.</span></span>
-   <span data-ttu-id="b9d62-130">**アップロード ジョブ (P ジョブ)** – アップロード ジョブは、チャンネルから小売データベースへの販売トランザクションをプルします。</span><span class="sxs-lookup"><span data-stu-id="b9d62-130">**Upload jobs (P jobs)** – Upload jobs pull sales transactions from a channel into the Retail database.</span></span> <span data-ttu-id="b9d62-131">P ジョブは、データを漸増的にアップロードします。</span><span class="sxs-lookup"><span data-stu-id="b9d62-131">P jobs upload data incrementally.</span></span> <span data-ttu-id="b9d62-132">P ジョブが実行されると、Async Client ライブラリが場所から既に受け取ったレコードに対するレプリケーション カウンターをチェックします。</span><span class="sxs-lookup"><span data-stu-id="b9d62-132">When a P job runs, the Async Client library checks the replication counter for records that have already been received from a location.</span></span> <span data-ttu-id="b9d62-133">レコードは、レプリケーション カウンターが検出された最大値を超える場合のみアップロードされます。</span><span class="sxs-lookup"><span data-stu-id="b9d62-133">A record is uploaded only if its replication counter is more than the largest value that is found.</span></span> <span data-ttu-id="b9d62-134">P ジョブは以前にアップロードされたデータを更新しません。</span><span class="sxs-lookup"><span data-stu-id="b9d62-134">P jobs don't update data that was previously uploaded.</span></span>

<span data-ttu-id="b9d62-135">配送スケジュールは、手動または小売用バックオフィスでスケジューリングされたバッチ ジョブによるデータ転送の実行に使用されます。</span><span class="sxs-lookup"><span data-stu-id="b9d62-135">The distribution schedule is used to run the data transfer, either manually or by scheduling a batch job in Retail headquarters.</span></span> <span data-ttu-id="b9d62-136">配送スケジュールには、1 つ以上のチャンネル データ グループと 1 つ以上のスケジューラ ジョブを含めることができます。</span><span class="sxs-lookup"><span data-stu-id="b9d62-136">A distribution schedule can contain one or more channel data groups, and one or more scheduler jobs.</span></span> <span data-ttu-id="b9d62-137">スケジューラー・ジョブが円滑に実行されていることを確認するには、インスタンス用に構成された「既定の」データベース名を変更せず、2 番目のデータベースを作成しないでください。</span><span class="sxs-lookup"><span data-stu-id="b9d62-137">To ensure that the scheduler jobs are running smoothly, do not rename the "Default" database configured for the instance, and do not create a second database.</span></span> <span data-ttu-id="b9d62-138">Retail Store Scale Unit ではないすべてのデータベースは Microsoft により管理され、1 つの既定のデータベースのみが必要です。</span><span class="sxs-lookup"><span data-stu-id="b9d62-138">All non-Retail Store Scale Unit databases are managed by Microsoft, and only one default database is expected.</span></span> 

## <a name="realtime-service"></a><span data-ttu-id="b9d62-139">リアルタイム サービス</span><span class="sxs-lookup"><span data-stu-id="b9d62-139">Realtime Service</span></span>
<span data-ttu-id="b9d62-140">Commerce Data Exchange: Real-time Service は、小売用バックオフィスと小売チャネル間のリアルタイム通信を提供する統合サービスです。</span><span class="sxs-lookup"><span data-stu-id="b9d62-140">Commerce Data Exchange: Real-time Service is an integrated service that provides real-time communication between Retail headquarters and retail channels.</span></span> <span data-ttu-id="b9d62-141">リアル タイム サービスにより、個々の POS コンピューターとオンライン ストアが小売用バックオフィスから特定のデータをリアルタイムで取得できるようになります。</span><span class="sxs-lookup"><span data-stu-id="b9d62-141">Real-time Service enables individual POS computers and online stores to retrieve specific data from Retail headquarters in real time.</span></span> <span data-ttu-id="b9d62-142">ほとんどのキー操作はローカルのチャンネル データベースで実行できますが、次のシナリオは小売用バックオフィスに格納されているデータへの直接アクセスが必要です。</span><span class="sxs-lookup"><span data-stu-id="b9d62-142">Although most key operations can be performed in the local channel database, the following scenarios require direct access to the data that is stored in Retail headquarters:</span></span>

-   <span data-ttu-id="b9d62-143">ギフトカードの発行および引換え</span><span class="sxs-lookup"><span data-stu-id="b9d62-143">Issuing and redeeming gift cards</span></span>
-   <span data-ttu-id="b9d62-144">ロイヤルティ ポイントを引き換え</span><span class="sxs-lookup"><span data-stu-id="b9d62-144">Redeeming loyalty points</span></span>
-   <span data-ttu-id="b9d62-145">クレジット メモの発行および引換え</span><span class="sxs-lookup"><span data-stu-id="b9d62-145">Issuing and redeeming credit memos</span></span>
-   <span data-ttu-id="b9d62-146">顧客レコードを作成または更新します</span><span class="sxs-lookup"><span data-stu-id="b9d62-146">Creating and updating customer records</span></span>
-   <span data-ttu-id="b9d62-147">販売注文を作成、更新、完了しています</span><span class="sxs-lookup"><span data-stu-id="b9d62-147">Creating, updating, and completing sales orders</span></span>
-   <span data-ttu-id="b9d62-148">発注書または移動オーダーに対する在庫を入荷</span><span class="sxs-lookup"><span data-stu-id="b9d62-148">Receiving inventory against a purchase order or transfer order</span></span>
-   <span data-ttu-id="b9d62-149">棚卸資産会計の実行</span><span class="sxs-lookup"><span data-stu-id="b9d62-149">Performing inventory counts</span></span>
-   <span data-ttu-id="b9d62-150">店舗間から販売トランザクションを取得し、返品トランザクションを完了します</span><span class="sxs-lookup"><span data-stu-id="b9d62-150">Retrieving sales transactions across stores and completing return transactions</span></span>

<span data-ttu-id="b9d62-151">[![Real-time Service](./media/rts.png)](./media/rts.png)</span><span class="sxs-lookup"><span data-stu-id="b9d62-151">[![Real-time Service](./media/rts.png)](./media/rts.png)</span></span> 

<span data-ttu-id="b9d62-152">定義済の Real-time Service プロファイルが作成されます。</span><span class="sxs-lookup"><span data-stu-id="b9d62-152">A predefined Real-time Service profile is created.</span></span>
