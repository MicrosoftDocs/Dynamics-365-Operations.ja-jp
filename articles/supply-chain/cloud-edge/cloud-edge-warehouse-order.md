---
title: クラウドおよびエッジのスケール ユニットに対する倉庫オーダー
description: このトピックでは、倉庫のスケール ユニット ワークロードの一部として使用される倉庫オーダー機能について説明します。
author: perlynne
manager: tfeyr
ms.date: 01/14/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSWarehouseOrderLine, WHSWarehouseReceiptEntry, PurchTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: SCM
ms.author: perlynne
ms.search.validFrom: 2021-01-14
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: c04127b9fe621d962be2d7fe06358b3bd1b78916
ms.sourcegitcommit: 289e9183d908825f4c8dcf85d9affd4119238d0c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/02/2021
ms.locfileid: "5105716"
---
# <a name="warehouse-orders-for-cloud-and-edge-scale-units"></a><span data-ttu-id="41ec3-103">クラウドおよびエッジのスケール ユニットに対する倉庫オーダー</span><span class="sxs-lookup"><span data-stu-id="41ec3-103">Warehouse orders for cloud and edge scale units</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

> [!WARNING]
> <span data-ttu-id="41ec3-104">スケール ユニット ワークロードが使用されている場合、すべてのビジネス機能がパブリック プレビューで完全にサポートされているわけではありません。</span><span class="sxs-lookup"><span data-stu-id="41ec3-104">Not all business functionality is fully supported in the public preview when scale unit workloads are used.</span></span> <span data-ttu-id="41ec3-105">スケール ユニットを使用している場合、このトピックでサポート対象として明示的に説明したプロセスのみを使用してください。</span><span class="sxs-lookup"><span data-stu-id="41ec3-105">If you're using scale units, be sure to use only those processes that this topic explicitly describes as supported.</span></span>

## <a name="what-are-warehouse-orders"></a><span data-ttu-id="41ec3-106">倉庫オーダーとは何ですか?</span><span class="sxs-lookup"><span data-stu-id="41ec3-106">What are warehouse orders?</span></span>

<span data-ttu-id="41ec3-107">*倉庫オーダー* は、ハブやスケール ユニットの倉庫展開をサポートするために作成されたオーダーの一種です。</span><span class="sxs-lookup"><span data-stu-id="41ec3-107">*Warehouse orders* are a type of order that was created to support hub and scale unit warehouse deployments.</span></span> <span data-ttu-id="41ec3-108">これにより、スケール ユニットで倉庫ワークロードを実行しているときに、在庫を受け入れできます。</span><span class="sxs-lookup"><span data-stu-id="41ec3-108">They let you receive inventory when you're running a warehouse workload on a scale unit.</span></span> <span data-ttu-id="41ec3-109">現在は、発注書でのみ使用されています。</span><span class="sxs-lookup"><span data-stu-id="41ec3-109">They are currently used only with purchase orders.</span></span>

<span data-ttu-id="41ec3-110">倉庫オーダーは、入庫発注書の処理時に倉庫アプリを使用して現物手持在庫を登録する場合など、倉庫管理処理の一部として使用されます。</span><span class="sxs-lookup"><span data-stu-id="41ec3-110">Warehouse orders are used as part of warehouse management processing, such as when the warehouse app is used to register physical on-hand inventory during processing of an inbound purchase order.</span></span> <span data-ttu-id="41ec3-111">倉庫オーダーは、スケール ユニットの倉庫と倉庫管理プロセスの使用が可能な品目を指定する、発注書に使用できる *倉庫へのリリース* プロセスの一部として作成されます。</span><span class="sxs-lookup"><span data-stu-id="41ec3-111">Warehouse orders are created as part of the *Release to warehouse* process that is available for purchase orders that specify a scale unit warehouse and items that are enabled to use warehouse management processes.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="41ec3-112">倉庫オーダーは、[クラウドおよびエッジのスケール ユニットに対する倉庫管理ワークロード](cloud-edge-workload-warehousing.md) を使用する展開でのみ使用できます。</span><span class="sxs-lookup"><span data-stu-id="41ec3-112">Warehouse orders are available only in deployments that use [warehouse management workloads for cloud and edge scale units](cloud-edge-workload-warehousing.md).</span></span>

## <a name="create-a-warehouse-order"></a><span data-ttu-id="41ec3-113">倉庫オーダーの作成</span><span class="sxs-lookup"><span data-stu-id="41ec3-113">Create a warehouse order</span></span>

<span data-ttu-id="41ec3-114">倉庫オーダーを作成するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="41ec3-114">To create a warehouse order, follow these steps.</span></span>

1. <span data-ttu-id="41ec3-115">ハブで実行されている Microsoft Dynamics 365 Supply Chain Management のインスタンスにサインインします。</span><span class="sxs-lookup"><span data-stu-id="41ec3-115">Sign in to the instance of Microsoft Dynamics 365 Supply Chain Management that is running on the hub.</span></span> <span data-ttu-id="41ec3-116">(ハブにサインインしている間に、*倉庫へのリリース* プロセスを開始する必要があります。)</span><span class="sxs-lookup"><span data-stu-id="41ec3-116">(You must initiate the *Release to warehouse* process while you're signed in on the hub.)</span></span>
1. <span data-ttu-id="41ec3-117">**調達 \> 発注書 \> すべての発注書** に移動します。</span><span class="sxs-lookup"><span data-stu-id="41ec3-117">Go to **Procurement and sourcing \> Purchase orders \> All purchase orders**.</span></span>
1. <span data-ttu-id="41ec3-118">アクション ペインの、**倉庫** タブにある **アクション** グループで、**倉庫にリリース** を選択します。</span><span class="sxs-lookup"><span data-stu-id="41ec3-118">On the Action Pane, on the **Warehouse** tab, in the **Actions** group, select **Release to warehouse**.</span></span>
1. <span data-ttu-id="41ec3-119">関連する倉庫の注文明細行を表示するには、関連する発注書を開き、**発注書明細行** セクションで明細行を選択し、ツール バーで **倉庫 \> 倉庫注文明細行** を選択します。</span><span class="sxs-lookup"><span data-stu-id="41ec3-119">To view the related warehouse order lines, open the relevant purchase order, select a line in the **Purchase order lines** section, and then, on the toolbar, select **Warehouse \> Warehouse order lines**.</span></span> <span data-ttu-id="41ec3-120">すべての明細行を表示するには、**倉庫管理 \> 照会およびレポート \> 倉庫注文明細行** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="41ec3-120">To view all the lines, go to **Warehouse management \> Inquiries and reports \> Warehouse order lines**.</span></span>

## <a name="cancel-a-warehouse-order"></a><span data-ttu-id="41ec3-121">倉庫オーダーのキャンセル</span><span class="sxs-lookup"><span data-stu-id="41ec3-121">Cancel a warehouse order</span></span>

<span data-ttu-id="41ec3-122">*倉庫へのリリース* プロセスの一環として、発注書の在庫トランザクションは倉庫オーダーにリンクされ、ハブによる更新からロックされます。</span><span class="sxs-lookup"><span data-stu-id="41ec3-122">As part of the *Release to warehouse* process, purchase order inventory transactions are linked to warehouse orders and locked from being updated by the hub.</span></span> <span data-ttu-id="41ec3-123">誤って倉庫にリリースした場合、または倉庫注文明細行の作成を取り消す他の理由がある場合は、倉庫注文明細行のキャンセルを要求できます。</span><span class="sxs-lookup"><span data-stu-id="41ec3-123">If you released to the warehouse by mistake, or if you have some other reason to reverse the creation of warehouse order lines, you can request to cancel warehouse order lines.</span></span>

<span data-ttu-id="41ec3-124">倉庫注文明細行をキャンセルするには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="41ec3-124">To cancel warehouse order lines, follow these steps.</span></span>

1. <span data-ttu-id="41ec3-125">ハブで実行されている Supply Chain Management のインスタンスにサインインします。</span><span class="sxs-lookup"><span data-stu-id="41ec3-125">Sign in to the Supply Chain Management instance that is running on the hub.</span></span>
1. <span data-ttu-id="41ec3-126">**倉庫管理 \> 照会およびレポート \> 倉庫注文明細行** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="41ec3-126">Go to **Warehouse management \> Inquiries and reports \> Warehouse order lines**.</span></span>
1. <span data-ttu-id="41ec3-127">関連する明細行を選択します。</span><span class="sxs-lookup"><span data-stu-id="41ec3-127">Select the relevant line.</span></span>
1. <span data-ttu-id="41ec3-128">アクション ペインで、**倉庫注文明細行のキャンセル** を選択します。</span><span class="sxs-lookup"><span data-stu-id="41ec3-128">On the Action Pane, select **Cancel warehouse order lines**.</span></span>

> [!NOTE]
> <span data-ttu-id="41ec3-129">すでにキャンセルを保留中の明細行、またはスケール ユニットでワークロードを実行している倉庫で現在処理されている明細行については、明細行のキャンセル要求は拒否されます。</span><span class="sxs-lookup"><span data-stu-id="41ec3-129">The request to cancel lines will be denied for any lines that are already pending cancellation or that are actively being processed at a warehouse that is running its workload on a scale unit.</span></span>

## <a name="monitor-a-warehouse-order"></a><span data-ttu-id="41ec3-130">倉庫オーダーの監視</span><span class="sxs-lookup"><span data-stu-id="41ec3-130">Monitor a warehouse order</span></span>

<span data-ttu-id="41ec3-131">**倉庫注文明細行** ビューで、**入庫残数量** 列の値を確認することで、入庫受入の進捗状況を監視できます。</span><span class="sxs-lookup"><span data-stu-id="41ec3-131">In the **Warehouse order lines** view, you can monitor the progress of inbound receiving by reviewing the values in the **Quantity left to receive** column.</span></span> <span data-ttu-id="41ec3-132">倉庫アプリを使用して行われた作業に関連する詳細を表示するには、次のいずれかの手順に従います。</span><span class="sxs-lookup"><span data-stu-id="41ec3-132">To view details that are related to work that is done by using the warehouse app, follow one of these steps.</span></span>

- <span data-ttu-id="41ec3-133">**倉庫管理 \> 照会およびレポート \> 倉庫注文明細行** に移動して、フィルターを使用し、探している明細行を検索します。</span><span class="sxs-lookup"><span data-stu-id="41ec3-133">Go to **Warehouse management \> Inquiries and reports \> Warehouse order lines**, and use the filter to find the lines that you're looking for.</span></span>
- <span data-ttu-id="41ec3-134">**調達 \> 発注書 \> すべての発注書** の順に移動し、関連する発注書を開きます。</span><span class="sxs-lookup"><span data-stu-id="41ec3-134">Go to **Procurement and sourcing \> Purchase orders \> All purchase orders**, and open the relevant purchase order.</span></span> <span data-ttu-id="41ec3-135">**発注書明細行** セクションで、1 つ以上の明細行を選択し、ツール バーで **倉庫 \> 入庫エントリ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="41ec3-135">In the **Purchase order lines** section, select one or more lines, and then, on the toolbar, select **Warehouse \> Warehouse receipt entries**.</span></span>
