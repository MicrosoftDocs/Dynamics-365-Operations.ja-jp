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
ms.openlocfilehash: 9102f53ab1b63d08b8bba7b0ae505416ec5a83fd
ms.sourcegitcommit: 70b1567d316f19c15a4b032b4897f15c8dcdca09
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/08/2021
ms.locfileid: "5556365"
---
# <a name="warehouse-orders-for-cloud-and-edge-scale-units"></a><span data-ttu-id="90c69-103">クラウドおよびエッジのスケール ユニットに対する倉庫オーダー</span><span class="sxs-lookup"><span data-stu-id="90c69-103">Warehouse orders for cloud and edge scale units</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

> [!WARNING]
> <span data-ttu-id="90c69-104">スケール ユニット ワークロードが使用されている場合、すべてのビジネス機能がパブリック プレビューで完全にサポートされているわけではありません。</span><span class="sxs-lookup"><span data-stu-id="90c69-104">Not all business functionality is fully supported in the public preview when scale unit workloads are used.</span></span> <span data-ttu-id="90c69-105">スケール ユニットを使用している場合、このトピックでサポート対象として明示的に説明したプロセスのみを使用してください。</span><span class="sxs-lookup"><span data-stu-id="90c69-105">If you're using scale units, be sure to use only those processes that this topic explicitly describes as supported.</span></span>

## <a name="what-are-warehouse-orders"></a><span data-ttu-id="90c69-106">倉庫オーダーとは何ですか?</span><span class="sxs-lookup"><span data-stu-id="90c69-106">What are warehouse orders?</span></span>

<span data-ttu-id="90c69-107">*倉庫オーダー* は、ハブやスケール ユニットの倉庫展開をサポートするために作成されたオーダーの一種です。</span><span class="sxs-lookup"><span data-stu-id="90c69-107">*Warehouse orders* are a type of order that was created to support hub and scale unit warehouse deployments.</span></span> <span data-ttu-id="90c69-108">これにより、スケール ユニットで倉庫ワークロードを実行しているときに、在庫を受け入れできます。</span><span class="sxs-lookup"><span data-stu-id="90c69-108">They let you receive inventory when you're running a warehouse workload on a scale unit.</span></span> <span data-ttu-id="90c69-109">現在は、発注書でのみ使用されています。</span><span class="sxs-lookup"><span data-stu-id="90c69-109">They are currently used only with purchase orders.</span></span>

<span data-ttu-id="90c69-110">倉庫オーダーは、入庫発注書の処理時に倉庫アプリを使用して現物手持在庫を登録する場合など、倉庫管理処理の一部として使用されます。</span><span class="sxs-lookup"><span data-stu-id="90c69-110">Warehouse orders are used as part of warehouse management processing, such as when the warehouse app is used to register physical on-hand inventory during processing of an inbound purchase order.</span></span> <span data-ttu-id="90c69-111">倉庫オーダーは、スケール ユニットの倉庫と倉庫管理プロセスの使用が可能な品目を指定する、発注書に使用できる *倉庫へのリリース* プロセスの一部として作成されます。</span><span class="sxs-lookup"><span data-stu-id="90c69-111">Warehouse orders are created as part of the *Release to warehouse* process that is available for purchase orders that specify a scale unit warehouse and items that are enabled to use warehouse management processes.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="90c69-112">倉庫オーダーは、[クラウドおよびエッジのスケール ユニットに対する倉庫管理ワークロード](cloud-edge-workload-warehousing.md) を使用する展開でのみ使用できます。</span><span class="sxs-lookup"><span data-stu-id="90c69-112">Warehouse orders are available only in deployments that use [warehouse management workloads for cloud and edge scale units](cloud-edge-workload-warehousing.md).</span></span>

## <a name="create-a-warehouse-order"></a><span data-ttu-id="90c69-113">倉庫オーダーの作成</span><span class="sxs-lookup"><span data-stu-id="90c69-113">Create a warehouse order</span></span>

<span data-ttu-id="90c69-114">倉庫オーダーを作成するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="90c69-114">To create a warehouse order, follow these steps.</span></span>

1. <span data-ttu-id="90c69-115">ハブで実行されている Microsoft Dynamics 365 Supply Chain Management のインスタンスにサインインします。</span><span class="sxs-lookup"><span data-stu-id="90c69-115">Sign in to the instance of Microsoft Dynamics 365 Supply Chain Management that is running on the hub.</span></span> <span data-ttu-id="90c69-116">(ハブにサインインしている間に、*倉庫へのリリース* プロセスを開始する必要があります。)</span><span class="sxs-lookup"><span data-stu-id="90c69-116">(You must initiate the *Release to warehouse* process while you're signed in on the hub.)</span></span>
1. <span data-ttu-id="90c69-117">**調達 \> 発注書 \> すべての発注書** に移動します。</span><span class="sxs-lookup"><span data-stu-id="90c69-117">Go to **Procurement and sourcing \> Purchase orders \> All purchase orders**.</span></span>
1. <span data-ttu-id="90c69-118">アクション ペインの、**倉庫** タブにある **アクション** グループで、**倉庫にリリース** を選択します。</span><span class="sxs-lookup"><span data-stu-id="90c69-118">On the Action Pane, on the **Warehouse** tab, in the **Actions** group, select **Release to warehouse**.</span></span>
1. <span data-ttu-id="90c69-119">関連する倉庫の注文明細行を表示するには、関連する発注書を開き、**発注書明細行** セクションで明細行を選択し、ツール バーで **倉庫 \> 倉庫注文明細行** を選択します。</span><span class="sxs-lookup"><span data-stu-id="90c69-119">To view the related warehouse order lines, open the relevant purchase order, select a line in the **Purchase order lines** section, and then, on the toolbar, select **Warehouse \> Warehouse order lines**.</span></span> <span data-ttu-id="90c69-120">すべての明細行を表示するには、**倉庫管理 \> 照会およびレポート \> 倉庫注文明細行** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="90c69-120">To view all the lines, go to **Warehouse management \> Inquiries and reports \> Warehouse order lines**.</span></span>

<span data-ttu-id="90c69-121">**倉庫管理 > 倉庫へのリリース > 発注書の自動リリース** の順に移動することで、バッチ ジョブから *倉庫へのリリース* プロセスをトリガーできます。</span><span class="sxs-lookup"><span data-stu-id="90c69-121">You can also trigger the *Release to warehouse* process from a batch job by going to **Warehouse management > Release to warehouse > Automatic release of purchase orders**.</span></span> <span data-ttu-id="90c69-122">バッチ ジョブの設定時に、クエリに基づいて特定の発注書明細行を選択できます。</span><span class="sxs-lookup"><span data-stu-id="90c69-122">When setting up the batch job, you can select specific purchase order lines based on a query.</span></span> <span data-ttu-id="90c69-123">一般的なシナリオとして、翌日に到着する予定のすべての確認済発注書明細行をリリースする反復バッチ ジョブを設定します。</span><span class="sxs-lookup"><span data-stu-id="90c69-123">A typical scenario would be to set up a recurrent batch job that releases all the confirmed purchase order lines expected to arrive the next day.</span></span>

## <a name="cancel-a-warehouse-order"></a><span data-ttu-id="90c69-124">倉庫オーダーのキャンセル</span><span class="sxs-lookup"><span data-stu-id="90c69-124">Cancel a warehouse order</span></span>

<span data-ttu-id="90c69-125">*倉庫へのリリース* プロセスの一環として、発注書の在庫トランザクションは倉庫オーダーにリンクされ、ハブによる更新からロックされます。</span><span class="sxs-lookup"><span data-stu-id="90c69-125">As part of the *Release to warehouse* process, purchase order inventory transactions are linked to warehouse orders and locked from being updated by the hub.</span></span> <span data-ttu-id="90c69-126">誤って倉庫にリリースした場合、または倉庫注文明細行の作成を取り消す他の理由がある場合は、倉庫注文明細行のキャンセルを要求できます。</span><span class="sxs-lookup"><span data-stu-id="90c69-126">If you released to the warehouse by mistake, or if you have some other reason to reverse the creation of warehouse order lines, you can request to cancel warehouse order lines.</span></span>

<span data-ttu-id="90c69-127">倉庫注文明細行をキャンセルするには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="90c69-127">To cancel warehouse order lines, follow these steps.</span></span>

1. <span data-ttu-id="90c69-128">ハブで実行されている Supply Chain Management のインスタンスにサインインします。</span><span class="sxs-lookup"><span data-stu-id="90c69-128">Sign in to the Supply Chain Management instance that is running on the hub.</span></span>
1. <span data-ttu-id="90c69-129">**倉庫管理 \> 照会およびレポート \> 倉庫注文明細行** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="90c69-129">Go to **Warehouse management \> Inquiries and reports \> Warehouse order lines**.</span></span>
1. <span data-ttu-id="90c69-130">関連する明細行を選択します。</span><span class="sxs-lookup"><span data-stu-id="90c69-130">Select the relevant line.</span></span>
1. <span data-ttu-id="90c69-131">アクション ペインで、**倉庫注文明細行のキャンセル** を選択します。</span><span class="sxs-lookup"><span data-stu-id="90c69-131">On the Action Pane, select **Cancel warehouse order lines**.</span></span>

> [!NOTE]
> <span data-ttu-id="90c69-132">すでにキャンセルを保留中の明細行、またはスケール ユニットでワークロードを実行している倉庫で現在処理されている明細行については、明細行のキャンセル要求は拒否されます。</span><span class="sxs-lookup"><span data-stu-id="90c69-132">The request to cancel lines will be denied for any lines that are already pending cancellation or that are actively being processed at a warehouse that is running its workload on a scale unit.</span></span>

## <a name="monitor-a-warehouse-order"></a><span data-ttu-id="90c69-133">倉庫オーダーの監視</span><span class="sxs-lookup"><span data-stu-id="90c69-133">Monitor a warehouse order</span></span>

<span data-ttu-id="90c69-134">**倉庫注文明細行** ビューで、**入庫残数量** 列の値を確認することで、入庫受入の進捗状況を監視できます。</span><span class="sxs-lookup"><span data-stu-id="90c69-134">In the **Warehouse order lines** view, you can monitor the progress of inbound receiving by reviewing the values in the **Quantity left to receive** column.</span></span> <span data-ttu-id="90c69-135">倉庫アプリを使用して行われた作業に関連する詳細を表示するには、次のいずれかの手順に従います。</span><span class="sxs-lookup"><span data-stu-id="90c69-135">To view details that are related to work that is done by using the warehouse app, follow one of these steps.</span></span>

- <span data-ttu-id="90c69-136">**倉庫管理 \> 照会およびレポート \> 倉庫注文明細行** に移動して、フィルターを使用し、探している明細行を検索します。</span><span class="sxs-lookup"><span data-stu-id="90c69-136">Go to **Warehouse management \> Inquiries and reports \> Warehouse order lines**, and use the filter to find the lines that you're looking for.</span></span>
- <span data-ttu-id="90c69-137">**調達 \> 発注書 \> すべての発注書** の順に移動し、関連する発注書を開きます。</span><span class="sxs-lookup"><span data-stu-id="90c69-137">Go to **Procurement and sourcing \> Purchase orders \> All purchase orders**, and open the relevant purchase order.</span></span> <span data-ttu-id="90c69-138">**発注書明細行** セクションで、1 つ以上の明細行を選択し、ツール バーで **倉庫 \> 入庫エントリ** を選択します。</span><span class="sxs-lookup"><span data-stu-id="90c69-138">In the **Purchase order lines** section, select one or more lines, and then, on the toolbar, select **Warehouse \> Warehouse receipt entries**.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]