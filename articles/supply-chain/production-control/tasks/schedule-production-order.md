---
title: "製造オーダーのスケジュール"
description: "この手順では、製造オーダーのスケジュール方法を示します。"
author: johanhoffmann
manager: AnnBe
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 007eae16a2a3c3fd138899f7b8a9ed768cc6600d
ms.contentlocale: ja-jp
ms.lasthandoff: 04/13/2018

---
# <a name="schedule-a-production-order"></a><span data-ttu-id="0d7a6-103">製造オーダーのスケジュール</span><span class="sxs-lookup"><span data-stu-id="0d7a6-103">Schedule a production order</span></span>

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="0d7a6-104">この手順では、製造オーダーのスケジュール方法を示します。</span><span class="sxs-lookup"><span data-stu-id="0d7a6-104">This procedure shows how to schedule a production order.</span></span> <span data-ttu-id="0d7a6-105">この手順の作成に使用するデモ データの会社は USMF です。</span><span class="sxs-lookup"><span data-stu-id="0d7a6-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="0d7a6-106">これは、製造オーダーのライフ サイクルを説明する 7 つの手順の 3 番目です。</span><span class="sxs-lookup"><span data-stu-id="0d7a6-106">This is the third procedure out of seven which explains the production order lifecycle.</span></span>


## <a name="schedule-a-production-order"></a><span data-ttu-id="0d7a6-107">製造オーダーのスケジュール</span><span class="sxs-lookup"><span data-stu-id="0d7a6-107">Schedule a production order</span></span>
1. <span data-ttu-id="0d7a6-108">[生産管理] > [製造オーダー] > [すべての製造オーダー] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="0d7a6-108">Go to Production control > Production orders > All production orders.</span></span>
    * <span data-ttu-id="0d7a6-109">[見積済] 状態の製造オーダーを選択します。</span><span class="sxs-lookup"><span data-stu-id="0d7a6-109">Select a production order that has the Estimated status.</span></span>  
2. <span data-ttu-id="0d7a6-110">[アクション ペイン] で、[スケジュール] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="0d7a6-110">On the Action Pane, click Schedule.</span></span>
3. <span data-ttu-id="0d7a6-111">[ジョブのスケジュール設定] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="0d7a6-111">Click Schedule jobs.</span></span>
    * <span data-ttu-id="0d7a6-112">スケジューリングのパラメーターはこのページで設定します。</span><span class="sxs-lookup"><span data-stu-id="0d7a6-112">The parameters for scheduling are set up on this page.</span></span> <span data-ttu-id="0d7a6-113">特定のユーザーまたはすべてのユーザー用のパラメータを設定できます。</span><span class="sxs-lookup"><span data-stu-id="0d7a6-113">You can set up the parameters for specific users or all users.</span></span>  
4. <span data-ttu-id="0d7a6-114">[スケジューリング指示] フィールドで、「今日からフォワード」 をクリックします。</span><span class="sxs-lookup"><span data-stu-id="0d7a6-114">In the Scheduling direction field, select 'Forward from today'.</span></span>
5. <span data-ttu-id="0d7a6-115">[スケジューリングの日付] フィールドに日付を入力します。</span><span class="sxs-lookup"><span data-stu-id="0d7a6-115">In the Scheduling date field, enter a date.</span></span>
6. <span data-ttu-id="0d7a6-116">[有限能力] チェック ボックスを選択またはクリアします。</span><span class="sxs-lookup"><span data-stu-id="0d7a6-116">Select or clear the Finite capacity check box.</span></span>
7. <span data-ttu-id="0d7a6-117">[有限原材料] チェック ボックスをオンまたはオフにします。</span><span class="sxs-lookup"><span data-stu-id="0d7a6-117">Select or clear the Finite material check box.</span></span>
8. <span data-ttu-id="0d7a6-118">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="0d7a6-118">Click OK.</span></span>

## <a name="view-the-scheduling-results"></a><span data-ttu-id="0d7a6-119">スケジューリング結果の表示</span><span class="sxs-lookup"><span data-stu-id="0d7a6-119">View the scheduling results</span></span>
1. <span data-ttu-id="0d7a6-120">アクション ウィンドウで、[製造オーダー] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="0d7a6-120">On the Action Pane, click Production order.</span></span>
2. <span data-ttu-id="0d7a6-121">[すべてのジョブ] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="0d7a6-121">Click All jobs.</span></span>
    * <span data-ttu-id="0d7a6-122">このページでは、生成したスケジュール済ジョブを表示します。</span><span class="sxs-lookup"><span data-stu-id="0d7a6-122">This page displays the scheduled jobs that you have just generated.</span></span>  
3. <span data-ttu-id="0d7a6-123">[スケジューリング] セクションを展開または折りたたみます。</span><span class="sxs-lookup"><span data-stu-id="0d7a6-123">Expand or collapse the Scheduling section.</span></span>
    * <span data-ttu-id="0d7a6-124">[スケジューリング クイック タブ] で、予定日時を表示できます。</span><span class="sxs-lookup"><span data-stu-id="0d7a6-124">On the Scheduling FastTab, you can view the scheduled date and time.</span></span>  
4. <span data-ttu-id="0d7a6-125">[照会] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="0d7a6-125">Click Inquiries.</span></span>
5. <span data-ttu-id="0d7a6-126">[最大能力負荷] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="0d7a6-126">Click Capacity load.</span></span>
    * <span data-ttu-id="0d7a6-127">[最大能力負荷] ページは、ジョブのスケジューリングで予約されている時間数、リソースで現在予約済の合計時間数、リソースのジョブのスケジューリングで使用できる残り時間数を表示します。</span><span class="sxs-lookup"><span data-stu-id="0d7a6-127">The Capacity load page displays the capacity that is reserved through job scheduling, the total number of hours that are currently reserved on the resource, and the number of hours that remain available for job scheduling on the resource.</span></span>  
6. <span data-ttu-id="0d7a6-128">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="0d7a6-128">Close the page.</span></span>
7. <span data-ttu-id="0d7a6-129">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="0d7a6-129">Close the page.</span></span>

