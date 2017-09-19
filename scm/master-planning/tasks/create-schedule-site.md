--- 
title: "サイトのスケジュールの作成"
description: "この手順は、サイトでまだ開始されていない製造オーダーをスケジュールする方法を示します。"
author: YuyuScheller
manager: AnnBe
ms.date: 06/10/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.author: yuyus
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 775428bf84a752c03c492e764fa9ed576ab64fb8
ms.contentlocale: ja-jp
ms.lasthandoff: 08/29/2017

---
# <a name="create-a-schedule-for-a-site"></a><span data-ttu-id="c58cd-103">サイトのスケジュールの作成</span><span class="sxs-lookup"><span data-stu-id="c58cd-103">Create a schedule for a site</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="c58cd-104">この手順は、サイトでまだ開始されていない製造オーダーをスケジュールする方法を示します。</span><span class="sxs-lookup"><span data-stu-id="c58cd-104">This procedure shows how to schedule production orders that are not yet started for a site.</span></span>  <span data-ttu-id="c58cd-105">この手順を完了するのにデモ データの会社 USMF が使用されています。</span><span class="sxs-lookup"><span data-stu-id="c58cd-105">The demo data company USMF is used to complete this procedure.</span></span>


## <a name="identify-production-orders-that-are-not-started"></a><span data-ttu-id="c58cd-106">開始されていない製造オーダーを識別します</span><span class="sxs-lookup"><span data-stu-id="c58cd-106">Identify production orders that are not started</span></span>
1. <span data-ttu-id="c58cd-107">[生産管理] > [製造オーダー] > [すべての製造オーダー] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="c58cd-107">Go to Production control > Production orders > All production orders.</span></span>
2. <span data-ttu-id="c58cd-108">クイック フィルターを使用して、レコードを見つけます。</span><span class="sxs-lookup"><span data-stu-id="c58cd-108">Use the Quick Filter to find records.</span></span> <span data-ttu-id="c58cd-109">たとえば、「1」という値で [サイト] フィールドをフィルター処理します。</span><span class="sxs-lookup"><span data-stu-id="c58cd-109">For example, filter on the Site field with a value of '1'.</span></span>
    * <span data-ttu-id="c58cd-110">1 では USMF 内のサイトを表します。</span><span class="sxs-lookup"><span data-stu-id="c58cd-110">1 represents a site in USMF.</span></span> <span data-ttu-id="c58cd-111">USMF を使用していない場合は、自分の会社からサイトを選択します。</span><span class="sxs-lookup"><span data-stu-id="c58cd-111">If you are not using USMF, select a site from your own company.</span></span>  
3. <span data-ttu-id="c58cd-112">[ステータス列フィルター] を開きます。</span><span class="sxs-lookup"><span data-stu-id="c58cd-112">Open the Status column filter.</span></span>
4. <span data-ttu-id="c58cd-113">[次の値と完全に一致する] フィルター演算子を使用して、[ステータス] フィールドに値 [スケジュール済] でフィルターを適用します。</span><span class="sxs-lookup"><span data-stu-id="c58cd-113">Apply a filter on the "Status" field, with a value of "Scheduled", using the "is exactly" filter operator.</span></span>

## <a name="create-a-schedule"></a><span data-ttu-id="c58cd-114">スケジュールの作成</span><span class="sxs-lookup"><span data-stu-id="c58cd-114">Create a schedule</span></span>
1. <span data-ttu-id="c58cd-115">一覧で、すべての行のマークを設定または解除します。</span><span class="sxs-lookup"><span data-stu-id="c58cd-115">In the list, mark or unmark all rows.</span></span>
2. <span data-ttu-id="c58cd-116">[アクション ペイン] で、[スケジュール] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="c58cd-116">On the Action Pane, click Schedule.</span></span>
3. <span data-ttu-id="c58cd-117">[ジョブのスケジュール] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="c58cd-117">Click Schedule jobs.</span></span>
4. <span data-ttu-id="c58cd-118">[スケジューリング指示] フィールドで、[出荷日からバックワード] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="c58cd-118">In the Scheduling direction field, select 'Backward from delivery date'.</span></span>
5. <span data-ttu-id="c58cd-119">[有限能力] フィールドで [いいえ] を選択します。</span><span class="sxs-lookup"><span data-stu-id="c58cd-119">Select No in the Finite capacity field.</span></span>
6. <span data-ttu-id="c58cd-120">[有限原材料] フィールドで [いいえ] を選択します。</span><span class="sxs-lookup"><span data-stu-id="c58cd-120">Select No in the Finite material field.</span></span>
7. <span data-ttu-id="c58cd-121">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="c58cd-121">Click OK.</span></span>
    * <span data-ttu-id="c58cd-122">しばらく時間がかかる場合があります</span><span class="sxs-lookup"><span data-stu-id="c58cd-122">This may take a while.</span></span>  

## <a name="view-the-result-of-scheduled-production-orders"></a><span data-ttu-id="c58cd-123">スケジュールされた製造オーダーの結果を表示します</span><span class="sxs-lookup"><span data-stu-id="c58cd-123">View the result of scheduled production orders</span></span>
1. <span data-ttu-id="c58cd-124">一覧で、選択された行をマークします。</span><span class="sxs-lookup"><span data-stu-id="c58cd-124">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="c58cd-125">どの行でもマークできます。</span><span class="sxs-lookup"><span data-stu-id="c58cd-125">You can mark any row.</span></span>  
2. <span data-ttu-id="c58cd-126">アクション ウィンドウで、[製造オーダー] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="c58cd-126">On the Action Pane, click Production order.</span></span>
3. <span data-ttu-id="c58cd-127">[すべてのジョブ] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="c58cd-127">Click All jobs.</span></span>
    * <span data-ttu-id="c58cd-128">このページで、ジョブのリストを表示できます。</span><span class="sxs-lookup"><span data-stu-id="c58cd-128">On this page, you can see the list of jobs.</span></span> <span data-ttu-id="c58cd-129">[スケジューリング] タブで、ジョブの開始日と終了日を表示できます。</span><span class="sxs-lookup"><span data-stu-id="c58cd-129">On the Scheduling tab, you can see the Start date and End date for a job.</span></span>  
4. <span data-ttu-id="c58cd-130">[材料] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="c58cd-130">Click Materials.</span></span>
    * <span data-ttu-id="c58cd-131">このページで、製造オーダー工程用の材料消費見積、および現在利用可能な在庫を確認できます。</span><span class="sxs-lookup"><span data-stu-id="c58cd-131">On this page, you can see the estimated material consumption for the operations on the production order and the current available inventory.</span></span>  

