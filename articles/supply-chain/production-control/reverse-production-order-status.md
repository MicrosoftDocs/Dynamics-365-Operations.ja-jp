---
title: "製造オーダーのステータスの取り消し"
description: "このトピックでは、製造オーダーのステータスを取り消す方法について説明します。"
author: johanhoffmann
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ProdParmStatusDecrease
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, Operations
ms.custom: 70131
ms.assetid: b1e0df43-b388-4326-8fb7-501f30c89776
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 4761e44b6bbc93ebf4a395948f42c2a73013ecb9
ms.contentlocale: ja-jp
ms.lasthandoff: 11/03/2017

---

# <a name="reverse-the-production-order-status"></a><span data-ttu-id="5b39a-103">製造オーダーのステータスの取り消し</span><span class="sxs-lookup"><span data-stu-id="5b39a-103">Reverse the production order status</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="5b39a-104">このトピックでは、製造オーダーのステータスを取り消す方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="5b39a-104">This topic describes how to reverse production order status.</span></span> 

<span data-ttu-id="5b39a-105">製造オーダーのステータスを戻すと、注文および工順に関連付けられているすべての工程が、生産ライフ サイクルの前のステップに戻されます。</span><span class="sxs-lookup"><span data-stu-id="5b39a-105">If you reverse the status of a production order, the order and all operations that are associated with the routes revert to a previous step in the production life cycle.</span></span> <span data-ttu-id="5b39a-106">たとえば、製造オーダーのステータスが**スケジュール済**で、ステータスを**作成済**に戻します。</span><span class="sxs-lookup"><span data-stu-id="5b39a-106">For example, a production order has a status of **Scheduled**, and you change the status back to **Created**.</span></span> <span data-ttu-id="5b39a-107">この場合、システムによって最初にステータスを**見積済**、つまり**スケジュール済**の直前のステータスに変更します。</span><span class="sxs-lookup"><span data-stu-id="5b39a-107">In this case, the system must first change the status to **Estimated**, which is the status that immediately precedes **Scheduled**.</span></span> <span data-ttu-id="5b39a-108">その後、ステータスを目的の**作成済**ステータスに変更できます。</span><span class="sxs-lookup"><span data-stu-id="5b39a-108">It can then change the status to the status that you want, **Created**.</span></span> <span data-ttu-id="5b39a-109">**注記:** 注文が**完了レポート**ステータスに到達していても、これを前のステータスに戻すことができます。</span><span class="sxs-lookup"><span data-stu-id="5b39a-109">**Note:** If your order has reached the **Report as finished** status, you can still reverse it to an earlier status.</span></span> <span data-ttu-id="5b39a-110">ただし、見積および工程のスケジューリングまたはジョブのスケジューリング、あるいはその両方のスケジューリングを実行して、再度注文の情報を更新する必要があります。</span><span class="sxs-lookup"><span data-stu-id="5b39a-110">However, you must re-run estimation and operations scheduling, job scheduling, or both types of scheduling, to update the information on the order.</span></span> <span data-ttu-id="5b39a-111">このステップは、残余品目消費および運営リソース消費の引当もリセットする必要があるため必須のステップです。</span><span class="sxs-lookup"><span data-stu-id="5b39a-111">This step is required, because any reservations of remaining item consumption and operations resource consumption must also be reset.</span></span> <span data-ttu-id="5b39a-112">この記事の残りの部分では、次のように、製造オーダーのステータスを戻す場合に実行される内容を説明します。</span><span class="sxs-lookup"><span data-stu-id="5b39a-112">The rest of this article explains what occurs when you reverse the status of a production order in the following ways:</span></span>

-   <span data-ttu-id="5b39a-113">**見積済**から**作成済**へ</span><span class="sxs-lookup"><span data-stu-id="5b39a-113">From **Estimated** to **Created**</span></span>
-   <span data-ttu-id="5b39a-114">**スケジュール済**から**見積済**へ</span><span class="sxs-lookup"><span data-stu-id="5b39a-114">From **Scheduled** to **Estimated**</span></span>
-   <span data-ttu-id="5b39a-115">**リリース済**から**スケジュール済**へ</span><span class="sxs-lookup"><span data-stu-id="5b39a-115">From **Released** to **Scheduled**</span></span>
-   <span data-ttu-id="5b39a-116">**開始済**から**リリース済**へ</span><span class="sxs-lookup"><span data-stu-id="5b39a-116">From **Started** to **Released**</span></span>

## <a name="from-estimated-to-created"></a><span data-ttu-id="5b39a-117">[見積済] から [作成済] へ</span><span class="sxs-lookup"><span data-stu-id="5b39a-117">From Estimated to Created</span></span>
<span data-ttu-id="5b39a-118">製造オーダーのステータスを**見積済**から**作成済**に戻す場合、部品表 (BOM) の品目に対して計算された品目消費は削除されます。</span><span class="sxs-lookup"><span data-stu-id="5b39a-118">When you reverse the status of a production order from **Estimated** to **Created**, the item consumption that was calculated for the items in the bill of materials (BOM) is removed.</span></span> <span data-ttu-id="5b39a-119">生産ラインの在庫トランザクションは削除され、生産の BOM 明細行の**残余のステータス**フィールドは**終了済**にリセットされます。</span><span class="sxs-lookup"><span data-stu-id="5b39a-119">Inventory transactions on the production line are deleted, and the **Remain status** field on the production order's BOM lines is reset to **Ended**.</span></span> <span data-ttu-id="5b39a-120">**派生購買**と**派生生産**オプションが選択されている場合、基になる発注書または製造オーダーが削除されます。</span><span class="sxs-lookup"><span data-stu-id="5b39a-120">When the **Derived purchases** and **Derived production** options are selected, any underlying purchase orders or production orders are deleted.</span></span> <span data-ttu-id="5b39a-121">製造オーダー原価を見積もる場合、または生産で使用するために品目を手動で引当されている場合、これらのトランザクションが削除されます。</span><span class="sxs-lookup"><span data-stu-id="5b39a-121">If you estimated the costs of the production order, or if you manually reserved items so that they could be used in production, those transactions are removed.</span></span>

## <a name="from-scheduled-to-estimated"></a><span data-ttu-id="5b39a-122">[スケジュール済] から [見積済] へ</span><span class="sxs-lookup"><span data-stu-id="5b39a-122">From Scheduled to Estimated</span></span>
<span data-ttu-id="5b39a-123">ステータスを**スケジュール済**から**見積済**に戻す場合、スケジュールされた開始日と終了日および時刻が削除されます。</span><span class="sxs-lookup"><span data-stu-id="5b39a-123">When you reverse the status of a production order from **Scheduled** to **Estimated**, the scheduled start and end dates and times are removed.</span></span> <span data-ttu-id="5b39a-124">スケジュール中に作成された確保済能力は削除され、ジョブ スケジュール中に作成されたジョブも削除されます。</span><span class="sxs-lookup"><span data-stu-id="5b39a-124">Capacity reservations that were made during scheduling are removed, and jobs that were created during job scheduling are deleted.</span></span> <span data-ttu-id="5b39a-125">**製造オーダーの詳細**ページで記録される、工程スケジューリングとジョブ スケジューリングについてのすべての情報は、リセットされます。</span><span class="sxs-lookup"><span data-stu-id="5b39a-125">All information that is recorded about operation scheduling and job scheduling on the **Production order details** page is reset.</span></span>

## <a name="from-released-to-scheduled"></a><span data-ttu-id="5b39a-126">[リリース済] から [スケジュール済] へ</span><span class="sxs-lookup"><span data-stu-id="5b39a-126">From Released to Scheduled</span></span>
<span data-ttu-id="5b39a-127">製造オーダーのステータスを**リリース済**から**スケジュール済**に戻した場合、変化するのはステータスのフィールドの値のみです。</span><span class="sxs-lookup"><span data-stu-id="5b39a-127">When you reverse the status of a production order from **Released** to **Scheduled**, the only change that occurs is the value in the status field.</span></span>

## <a name="from-started-to-released"></a><span data-ttu-id="5b39a-128">[開始済] から [リリース済] へ</span><span class="sxs-lookup"><span data-stu-id="5b39a-128">From Started to Released</span></span>
<span data-ttu-id="5b39a-129">製造オーダーのステータスを **開始済**から**リリース済**に戻すと、完了したとして報告されたすべての品目の設定は戻されます。</span><span class="sxs-lookup"><span data-stu-id="5b39a-129">When you reverse the status of a production order from **Started** to **Released**, all items that were reported as finished are reverted.</span></span> <span data-ttu-id="5b39a-130">材料がピッキング済であるか、入庫および出荷の配送が生産に対して行われていた場合は、これらの設定は戻されます。</span><span class="sxs-lookup"><span data-stu-id="5b39a-130">If material has been picked, or if inbound and outbound deliveries have been made to production, those settings are reversed.</span></span> <span data-ttu-id="5b39a-131">製造オーダーの BOM 明細行の**残余のステータス**フィールドは、**終了済** から**材料消費量**に変更されます。</span><span class="sxs-lookup"><span data-stu-id="5b39a-131">The **Remain status** field on the production order’s BOM lines is changed from **Ended** to **Material consumption**.</span></span> <span data-ttu-id="5b39a-132">時間が登録済または数量が生産工順の工程で完了と報告される場合、これらの設定は取り消されます。</span><span class="sxs-lookup"><span data-stu-id="5b39a-132">If time has been registered, or if quantities have been reported as finished for the operations in the production route, those settings are reversed.</span></span> <span data-ttu-id="5b39a-133">生産工順における**残余のステータス**フィールドは、**終了済** から**工順消費**に変更されます。</span><span class="sxs-lookup"><span data-stu-id="5b39a-133">The **Remain status** field is changed from **Ended** to **Route consumption** in the production route.</span></span> <span data-ttu-id="5b39a-134">プロセス中またはプロセスの作業としてと転記されたすべての品目の設定は戻されます。</span><span class="sxs-lookup"><span data-stu-id="5b39a-134">The settings for all items that are posted as in process or work in process are reversed.</span></span> <span data-ttu-id="5b39a-135">**製造オーダーの詳細**ページで、開始または完了報告された数量を示すフィールドはリセットされます。</span><span class="sxs-lookup"><span data-stu-id="5b39a-135">On the **Production order details** page, fields that show a quantity that was started or reported as finished are reset.</span></span> <span data-ttu-id="5b39a-136">これらのトランザクションの日付も、リセットされます。</span><span class="sxs-lookup"><span data-stu-id="5b39a-136">The dates for those transactions are also reset.</span></span>




