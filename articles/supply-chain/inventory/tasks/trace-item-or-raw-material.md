---
title: 品目または原材料の追跡
description: この手順は、品目の追跡を使用して、品目または原材料が使用された場所または使用されている場所を識別する方法を示します。
author: pjacobse
manager: AnnBe
ms.date: 08/12/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventTrackingDimTracing, InventTrackingDimTracingCriteria, InventTrackingItemIdLookup, InventBatchIdLookup, CustTable, SalesLine
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: pjacobse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: fe0fd9a7c27efb71f15cca9d3a0341b550bf9698
ms.sourcegitcommit: cbcf344b3b552acca56c3e27606eac7f2f124afe
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/22/2019
ms.locfileid: "1916678"
---
# <a name="trace-an-item-or-raw-material"></a><span data-ttu-id="6f2e0-103">品目または原材料の追跡</span><span class="sxs-lookup"><span data-stu-id="6f2e0-103">Trace an item or raw material</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="6f2e0-104">この手順は、品目の追跡を使用して、品目または原材料が使用された場所または使用されている場所を識別する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="6f2e0-104">This procedure demonstrates how to use item tracing to identify where items or raw materials have been used or are being used.</span></span> <span data-ttu-id="6f2e0-105">この手順を使用すると、品目を識別し、ソースまで過去方向に追跡してから、完成品の生産と販売まで将来方向に追跡できます。</span><span class="sxs-lookup"><span data-stu-id="6f2e0-105">With this procedure, you can identify an item, trace it back to the source, and then trace forward through the production and sale of the finished product.</span></span> <span data-ttu-id="6f2e0-106">このプロセスは、影響を受ける顧客、販売注文などの調査に使用できます。</span><span class="sxs-lookup"><span data-stu-id="6f2e0-106">The process can be used to investigate the customers impacted, the sales orders affected, and more.</span></span> <span data-ttu-id="6f2e0-107">この手順では、デモ データの会社 USP2 を使用します。</span><span class="sxs-lookup"><span data-stu-id="6f2e0-107">This procedure uses demo data company USP2.</span></span>


## <a name="trace-an-item-backwards-using-a-known-batch-number"></a><span data-ttu-id="6f2e0-108">既知のバッチ番号を使用して品目を過去方向に追跡</span><span class="sxs-lookup"><span data-stu-id="6f2e0-108">Trace an item backwards using a known batch number</span></span>
1. <span data-ttu-id="6f2e0-109">**ナビゲーション ウィンドウ**で、**モジュール > 在庫管理 > 照会およびレポート > 追跡用分析コード > 品目の追跡**に移動します。</span><span class="sxs-lookup"><span data-stu-id="6f2e0-109">In the **Navigation pane**, go to **Modules > Inventory management > Inquiries and reports > Tracking dimensions > Item tracing**.</span></span>
2. <span data-ttu-id="6f2e0-110">**品目番号**フィールドで、'P9100' を選択します。</span><span class="sxs-lookup"><span data-stu-id="6f2e0-110">In the **Item number** field, select 'P9100'.</span></span>
3. <span data-ttu-id="6f2e0-111">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="6f2e0-111">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="6f2e0-112">**前方向または後方向**のフィールドで「後方向」を選択します。</span><span class="sxs-lookup"><span data-stu-id="6f2e0-112">In the **Forward or backward** field, select 'Backward'.</span></span>
5. <span data-ttu-id="6f2e0-113">**バッチ番号**フィールドで、'as-12-344-01' を選択します。</span><span class="sxs-lookup"><span data-stu-id="6f2e0-113">In the **Batch number** field, select 'as-12-344-01'.</span></span>
6. <span data-ttu-id="6f2e0-114">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="6f2e0-114">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="6f2e0-115">**OK**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="6f2e0-115">Click **OK**.</span></span>

## <a name="identify-an-item-trace-it-forward-and-make-an-analysis"></a><span data-ttu-id="6f2e0-116">品目を識別し、将来方向に追跡し、分析を行う</span><span class="sxs-lookup"><span data-stu-id="6f2e0-116">Identify an item, trace it forward, and make an analysis</span></span>

<span data-ttu-id="6f2e0-117">ツリーのトップ ノードは、選択された品目とバッチの手持数量を表します。</span><span class="sxs-lookup"><span data-stu-id="6f2e0-117">The top node of the tree represents the on hand quantity of the selected item and batch.</span></span> <span data-ttu-id="6f2e0-118">後方向追跡を実行する必要がある品目を検索するには、ツリーのノードを展開する必要があります。</span><span class="sxs-lookup"><span data-stu-id="6f2e0-118">You need to expand the nodes of the tree to find the item that the forward trace should be executed on.</span></span>   
1. <span data-ttu-id="6f2e0-119">ツリーで、[以下に説明されたノード、次に最後のノードを選択する] を展開します。</span><span class="sxs-lookup"><span data-stu-id="6f2e0-119">In the tree, expand 'the nodes described below, and then select the last node'.</span></span>
    
    <span data-ttu-id="6f2e0-120">「P9100 / 1 / 10 / as-12-344-01 ● 2 keg ● 7.00 gal  \P9100 ● Picked ● Sales order 000072 ● 12/22/2015  ● -1 keg ● -4.00 gal ● Site=1, Warehouse=10, Batch number=as-12-344-01  \P9100 ● Production B-000050 ● 12/9/2015● 7 keg ● 27.00 gal ● Site=1,Warehouse=10,Batch number=as-12-344-01 ● Co-products: P9101」 を展開し、次にそのノードを選択します。</span><span class="sxs-lookup"><span data-stu-id="6f2e0-120">Expand: 'P9100 / 1 / 10 / as-12-344-01 ● 2 keg ● 7.00 gal  \P9100 ● Picked ● Sales order 000072 ● 12/22/2015  ● -1 keg ● -4.00 gal ● Site=1, Warehouse=10, Batch number=as-12-344-01  \P9100 ● Production B-000050 ● 12/9/2015● 7 keg ● 27.00 gal ● Site=1,Warehouse=10,Batch number=as-12-344-01 ● Co-products: P9101' and then select that node.</span></span>     
2. <span data-ttu-id="6f2e0-121">ツリーで、[以下に説明されたノード、次にそのノードを選択する] を展開します。</span><span class="sxs-lookup"><span data-stu-id="6f2e0-121">In the tree, expand 'the node described below and then select that node'.</span></span>
    
    <span data-ttu-id="6f2e0-122">先ほど選択したノードから開始します。「M9103 ● 生産ライン B-000050 ● 12/9/2015  ● -160.00 lb ● Size=70, Color=OK, Site=1, Warehouse=10, Batch number=App01」を展開し、次にそのノードを選択します。</span><span class="sxs-lookup"><span data-stu-id="6f2e0-122">Starting from the node that you’ve just selected,  expand 'M9103 ● Production line B-000050 ● 12/9/2015  ● -160.00 lb ● Size=70, Color=OK, Site=1, Warehouse=10, Batch number=App01' and then select that node.</span></span>  
3. <span data-ttu-id="6f2e0-123">**ノードから追跡**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="6f2e0-123">Click **Trace from node**.</span></span>
4. <span data-ttu-id="6f2e0-124">**次**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="6f2e0-124">Click **Forward**.</span></span>
5. <span data-ttu-id="6f2e0-125">**アクション ウィンドウ**で、**追跡**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="6f2e0-125">On the **Action Pane**, click **Tracing**.</span></span>
    
    <span data-ttu-id="6f2e0-126">追跡する品目により影響を受ける顧客に関する情報、および出荷済み品目と未出荷品目に関連する販売品目に関する情報を提供する複数の追跡オプションがあります。</span><span class="sxs-lookup"><span data-stu-id="6f2e0-126">There are several tracing options which provide information about the customers impacted by the item that you’re tracing, and the sales orders related to the item which have and haven’t been shipped.</span></span>   
6. <span data-ttu-id="6f2e0-127">**顧客**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="6f2e0-127">Click **Customers**.</span></span>
7. <span data-ttu-id="6f2e0-128">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="6f2e0-128">Close the page.</span></span>
8. <span data-ttu-id="6f2e0-129">**アクション ウィンドウ**で、**追跡**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="6f2e0-129">On the **Action Pane**, click **Tracing**.</span></span>
9. <span data-ttu-id="6f2e0-130">**未出荷の販売注文**をクリックします。</span><span class="sxs-lookup"><span data-stu-id="6f2e0-130">Click **Shipped sales orders**.</span></span>
10. <span data-ttu-id="6f2e0-131">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="6f2e0-131">Close the page.</span></span>

