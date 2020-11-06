---
title: クラスター ピッキングの設定
description: このトピックでは、クラスター ピッキングを設定する方法およびクラスター ピッキングに品目の確認を適用する方法について説明します。
author: Mirzaab
manager: tfehr
ms.date: 05/26/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSClusterProfile, WHSRFAutoConfirm, WHSWorkCluster
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 269384
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 009345e608c26887fedbe4a9c268367080593da2
ms.sourcegitcommit: a36a4f9915ae3eb36bf8220111cf1486387713d9
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/16/2020
ms.locfileid: "4017578"
---
# <a name="set-up-cluster-picking"></a><span data-ttu-id="4f402-103">クラスター ピッキングの設定</span><span class="sxs-lookup"><span data-stu-id="4f402-103">Set up cluster picking</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="4f402-104">このトピックでは、作業者がモバイル デバイスを使用してピッキング作業をクラスターにグループ化して、複数のワーク オーダーに対して 1 つの場所から品目を同時にピッキングできるようにする方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="4f402-104">This topic describes how to enable workers to use their mobile devices to group picking work into clusters, so that they can pick items from a single location for multiple work orders at the same time.</span></span> <span data-ttu-id="4f402-105">これは *クラスター ピッキング* と呼ばれます。</span><span class="sxs-lookup"><span data-stu-id="4f402-105">This is called *cluster picking*.</span></span>

## <a name="about-cluster-picking"></a><span data-ttu-id="4f402-106">クラスター ピッキングについて</span><span class="sxs-lookup"><span data-stu-id="4f402-106">About cluster picking</span></span>

<span data-ttu-id="4f402-107">ワーク オーダーが倉庫にリリースされると、作業者はモバイル デバイスを使用してクラスターにオーダーを割り当てることができます。</span><span class="sxs-lookup"><span data-stu-id="4f402-107">After work orders are released to the warehouse, the worker can use a mobile device to assign the orders to a cluster.</span></span> <span data-ttu-id="4f402-108">クラスターは、作業者のピッキング作業を整理します。</span><span class="sxs-lookup"><span data-stu-id="4f402-108">The cluster will organize the picking work for the worker.</span></span> <span data-ttu-id="4f402-109">ワーク オーダーがクラスターに割り当てられると、作業者はクラスター ピッキングを使用して、そのオーダーのピッキング作業を実行する必要があります。</span><span class="sxs-lookup"><span data-stu-id="4f402-109">When a work order is assigned to a cluster, the worker must use cluster picking to perform the picking work for the order.</span></span> <span data-ttu-id="4f402-110">作業者は、他のピッキング方法を使用できません。</span><span class="sxs-lookup"><span data-stu-id="4f402-110">The worker cannot use other picking methods.</span></span> <span data-ttu-id="4f402-111">ワーク オーダーがクラスターに誤って割り当てられた場合、作業者はクラスターを破棄して、クラスターを再作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="4f402-111">If a work order is assigned to a cluster by mistake, the worker must break the cluster and then re-create it.</span></span>

<span data-ttu-id="4f402-112">必要に応じて、作業者は別の作業者にクラスターを渡すことができます。</span><span class="sxs-lookup"><span data-stu-id="4f402-112">If needed, a worker can pass a cluster to another worker.</span></span> <span data-ttu-id="4f402-113">これにより、クラスターの状態が [引渡済み] に変わります。</span><span class="sxs-lookup"><span data-stu-id="4f402-113">This changes the cluster status to Passed.</span></span> <span data-ttu-id="4f402-114">作業者がモバイル デバイスを使用してピッキングとプット アウェイ作業が完了したことを示したとき、出荷または積荷をクライアントで確認する必要があります。</span><span class="sxs-lookup"><span data-stu-id="4f402-114">When the worker uses a mobile device to indicate that the picking and put away work is completed, the shipment or load must be confirmed in the client.</span></span>

## <a name="enable-cluster-picking"></a><span data-ttu-id="4f402-115">クラスター ピッキングを有効化する</span><span class="sxs-lookup"><span data-stu-id="4f402-115">Enable cluster picking</span></span>

<span data-ttu-id="4f402-116">クラスター ピッキングを有効にするには、次の設定を行う必要があります。</span><span class="sxs-lookup"><span data-stu-id="4f402-116">To enable cluster picking, you must set up the following:</span></span>

- <span data-ttu-id="4f402-117">**クラスター プロファイル** – クラスター ID、使用するポジションの数、クラスターを破棄する時期、ピッキング作業の順序付けと検証方法を自動的に生成するかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="4f402-117">**Cluster profiles** – Specify whether to automatically generate cluster   IDs, the number of positions to use, when to break clusters, and how to   sequence and verify the picking work.</span></span>

- <span data-ttu-id="4f402-118">**作業テンプレート** – クラスター ピッキングのピッキング作業を作成する方法を定義します。</span><span class="sxs-lookup"><span data-stu-id="4f402-118">**Work templates** – Define how to create the picking work for cluster   picking.</span></span>

- <span data-ttu-id="4f402-119">**ロケーション指示** – 品目のピッキングのロケーションとプット アウェイ ロケーションを指定します。</span><span class="sxs-lookup"><span data-stu-id="4f402-119">**Location directives** – Specify where to pick items from, and where to put   them.</span></span>

- <span data-ttu-id="4f402-120">**モバイル デバイスのメニュー品目** – クラスター ピッキングによって指示される既存の作業を使用するモバイル デバイス メニュー項目をコンフィギュレーションします。</span><span class="sxs-lookup"><span data-stu-id="4f402-120">**Mobile device menu items** – Configure a mobile device menu item to use existing work that is directed by cluster picking.</span></span> <span data-ttu-id="4f402-121">次に、モバイル デバイスに表示されるように、モバイル デバイスのメニューにメニュー項目を追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="4f402-121">You must then add the menu item to a mobile device menu so that it is displayed on mobile devices.</span></span>

- <span data-ttu-id="4f402-122">**倉庫管理パラメーター** – クラスターの ID を生成するには、使用する番号の順序を指定します。</span><span class="sxs-lookup"><span data-stu-id="4f402-122">**Warehouse management parameters** – Specify the number sequence to use if   you want to generate identifiers for clusters.</span></span>

## <a name="set-up-a-cluster-profile"></a><span data-ttu-id="4f402-123">クラスター プロファイルの設定</span><span class="sxs-lookup"><span data-stu-id="4f402-123">Set up a cluster profile</span></span>

<span data-ttu-id="4f402-124">クラスター プロファイルを設定するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="4f402-124">To set up a cluster profile, follow these steps:</span></span>

1. <span data-ttu-id="4f402-125">**倉庫管理** \> **設定** \> **モバイル デバイス** \> **クラスター プロファイル** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="4f402-125">Click **Warehouse management** \> **Setup** \> **Mobile device** \>  **Cluster profiles**.</span></span>

1. <span data-ttu-id="4f402-126">**新規** をクリックして、新しいプロファイルを作成します。</span><span class="sxs-lookup"><span data-stu-id="4f402-126">Click **New** to create a new profile.</span></span>

1. <span data-ttu-id="4f402-127">**クラスターを作成** をクリックし、 **クラスターの並べ替え** の下で、 **新規** をクリックして、クラスターの並べ替え基準を設定します。</span><span class="sxs-lookup"><span data-stu-id="4f402-127">Click **Create cluster** and, under **Cluster sorting** , click **New** to set up the sorting criteria for the cluster.</span></span> <span data-ttu-id="4f402-128">並べ替え基準は、作業者がピッキング作業を実行する順序を制御します。</span><span class="sxs-lookup"><span data-stu-id="4f402-128">The sorting criteria control the order in which the worker will perform the picking work.</span></span> <span data-ttu-id="4f402-129">必要な数だけ基準を追加できます。</span><span class="sxs-lookup"><span data-stu-id="4f402-129">You can add as many criteria as needed.</span></span>

1. <span data-ttu-id="4f402-130">**シーケンス番号** フィールドで、番号を入力してソート基準が処理される順序を定義します。</span><span class="sxs-lookup"><span data-stu-id="4f402-130">In the **Sequence number** field, enter a number to define the order in  which the sorting criteria are processed.</span></span>

1. <span data-ttu-id="4f402-131">**フィールド名** フィールドで、並べ替えを決定するフィールドを選択します。</span><span class="sxs-lookup"><span data-stu-id="4f402-131">In the **Field name** field, select the field that will determine the sorting.</span></span> <span data-ttu-id="4f402-132">たとえば、 **WMSLocationId** フィールドを選択した場合、作業は場所別に並べ替えられます。</span><span class="sxs-lookup"><span data-stu-id="4f402-132">For example, if you select the **WMSLocationId** field, the work will be sorted by location.</span></span>

1. <span data-ttu-id="4f402-133">**並べ替え** フィールドで、次のいずれかのオプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="4f402-133">In the **Sorting** field, select one of the following options.</span></span>

| <span data-ttu-id="4f402-134">**オプション**</span><span class="sxs-lookup"><span data-stu-id="4f402-134">**Option**</span></span>     | <span data-ttu-id="4f402-135">**説明**</span><span class="sxs-lookup"><span data-stu-id="4f402-135">**Description**</span></span>                                                                                                                                                                                                                    |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4f402-136">**昇順**</span><span class="sxs-lookup"><span data-stu-id="4f402-136">**Ascending**</span></span>  | <span data-ttu-id="4f402-137">ピッキング作業は、並べ替え基準に基づいて、昇順で順序付けられます。</span><span class="sxs-lookup"><span data-stu-id="4f402-137">Picking work is sequenced in ascending order based on the sorting criteria.</span></span> <span data-ttu-id="4f402-138">たとえば、並べ替え基準として **WMSLocationId** フィールドを使用し、その場所 ID が 1、2、3、および 4 の場合、最初に場所 4 からピッキングします。</span><span class="sxs-lookup"><span data-stu-id="4f402-138">For example, if you use the **WMSLocationId** field as sorting criteria, and your location IDs are 1, 2, 3, and 4, you will pick from location 4 first.</span></span> |
| <span data-ttu-id="4f402-139">**降順**</span><span class="sxs-lookup"><span data-stu-id="4f402-139">**Descending**</span></span> | <span data-ttu-id="4f402-140">ピッキング作業は、並べ替え基準に基づいて、降順で順序付けられます。</span><span class="sxs-lookup"><span data-stu-id="4f402-140">Picking work is sequenced in descending order based on the sorting criteria.</span></span> <span data-ttu-id="4f402-141">たとえば、並べ替え基準として **WMSLocationId** フィールドを使用し、その場所 ID が 1、2、3、および 4 の場合、最初に場所 1 からピッキングします。</span><span class="sxs-lookup"><span data-stu-id="4f402-141">For example, if you use the **WMSLocationId** field as sorting criteria, and your location IDs are 1, 2, 3, and 4, you will pick from location 1 first.</span></span> |

## <a name="item-confirmation"></a><span data-ttu-id="4f402-142">品目確認</span><span class="sxs-lookup"><span data-stu-id="4f402-142">Item confirmation</span></span>

<span data-ttu-id="4f402-143">クラスタ ピッキングが適用される場合、クラスタに追加される品目を確認するための品目確認書は重要です。</span><span class="sxs-lookup"><span data-stu-id="4f402-143">When cluster picking is applied, item confirmation is crucial to verify the items that are added to clusters.</span></span> <span data-ttu-id="4f402-144">クラスタ ピッキング プロセス中にクラスタ ピッキングの品目を確認することができます。</span><span class="sxs-lookup"><span data-stu-id="4f402-144">You can verify items in cluster picking during the cluster picking process.</span></span> <span data-ttu-id="4f402-145">設定は、製品バー コード設定に基づいています。</span><span class="sxs-lookup"><span data-stu-id="4f402-145">The setup is based on the product bar code setup.</span></span>

### <a name="set-up-item-verification-with-cluster-picking"></a><span data-ttu-id="4f402-146">クラスタ ピッキングの品目の検証の設定</span><span class="sxs-lookup"><span data-stu-id="4f402-146">Set up item verification with cluster picking</span></span>

1. <span data-ttu-id="4f402-147">モバイル デバイスのメニュー項目で、作業確認の設定フォームを開きます、 **倉庫管理** \> **倉庫管理** \> **設定** \>  **モバイル デバイス** \> **モバイル デバイスのメニュー項目** に移動します。</span><span class="sxs-lookup"><span data-stu-id="4f402-147">On a mobile device menu item, open the setup form for work confirmation:  **Warehouse management** \> **Warehouse management** \> **Setup** \>  **Mobile device** \> **Mobile device menu items**.</span></span>

1. <span data-ttu-id="4f402-148">モバイル デバイス メニュー品目から、 **作業確認の設定** を開きます。</span><span class="sxs-lookup"><span data-stu-id="4f402-148">From the mobile device menu item, open **Work confirmation setup**.</span></span> <span data-ttu-id="4f402-149">**製品確認** オプションでは、スャンしたときにモバイル デバイスから各在庫を確認できます。</span><span class="sxs-lookup"><span data-stu-id="4f402-149">The **Product confirmation** option allows you to verify each piece of inventory from the mobile device when scanned.</span></span>
