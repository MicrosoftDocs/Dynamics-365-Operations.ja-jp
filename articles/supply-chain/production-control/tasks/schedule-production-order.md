---
title: 製造オーダーのスケジュール
description: この手順では、製造オーダーのスケジュール方法を示します。
author: johanhoffmann
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProdTableListPage, ProdSchedule, ProdRouteJob, WrkCtrCapResSum
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4ae2414fcc96b4a12aeb0c60252a27321aacc7df
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/18/2020
ms.locfileid: "3146632"
---
# <a name="schedule-a-production-order"></a><span data-ttu-id="5e083-103">製造オーダーのスケジュール</span><span class="sxs-lookup"><span data-stu-id="5e083-103">Schedule a production order</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="5e083-104">この手順では、製造オーダーのスケジュール方法を示します。</span><span class="sxs-lookup"><span data-stu-id="5e083-104">This procedure shows how to schedule a production order.</span></span> <span data-ttu-id="5e083-105">この手順の作成に使用するデモ データの会社は USMF です。</span><span class="sxs-lookup"><span data-stu-id="5e083-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="5e083-106">これは、製造オーダーのライフ サイクルを説明する 7 つの手順の 3 番目です。</span><span class="sxs-lookup"><span data-stu-id="5e083-106">This is the third procedure out of seven which explains the production order lifecycle.</span></span>


## <a name="schedule-a-production-order"></a><span data-ttu-id="5e083-107">製造オーダーのスケジュール</span><span class="sxs-lookup"><span data-stu-id="5e083-107">Schedule a production order</span></span>
1. <span data-ttu-id="5e083-108">[生産管理] > [製造オーダー] > [すべての製造オーダー] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="5e083-108">Go to Production control > Production orders > All production orders.</span></span>
    * <span data-ttu-id="5e083-109">[見積済] 状態の製造オーダーを選択します。</span><span class="sxs-lookup"><span data-stu-id="5e083-109">Select a production order that has the Estimated status.</span></span>  
2. <span data-ttu-id="5e083-110">[アクション ペイン] で、[スケジュール] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="5e083-110">On the Action Pane, click Schedule.</span></span>
3. <span data-ttu-id="5e083-111">[ジョブのスケジュール設定] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="5e083-111">Click Schedule jobs.</span></span>
    * <span data-ttu-id="5e083-112">スケジューリングのパラメーターはこのページで設定します。</span><span class="sxs-lookup"><span data-stu-id="5e083-112">The parameters for scheduling are set up on this page.</span></span> <span data-ttu-id="5e083-113">特定のユーザーまたはすべてのユーザー用のパラメータを設定できます。</span><span class="sxs-lookup"><span data-stu-id="5e083-113">You can set up the parameters for specific users or all users.</span></span>  
4. <span data-ttu-id="5e083-114">[スケジューリング指示] フィールドで、「今日からフォワード」 をクリックします。</span><span class="sxs-lookup"><span data-stu-id="5e083-114">In the Scheduling direction field, select 'Forward from today'.</span></span>
5. <span data-ttu-id="5e083-115">[スケジューリングの日付] フィールドに日付を入力します。</span><span class="sxs-lookup"><span data-stu-id="5e083-115">In the Scheduling date field, enter a date.</span></span>
6. <span data-ttu-id="5e083-116">[有限能力] チェック ボックスを選択またはクリアします。</span><span class="sxs-lookup"><span data-stu-id="5e083-116">Select or clear the Finite capacity check box.</span></span>
7. <span data-ttu-id="5e083-117">[有限原材料] チェック ボックスをオンまたはオフにします。</span><span class="sxs-lookup"><span data-stu-id="5e083-117">Select or clear the Finite material check box.</span></span>
8. <span data-ttu-id="5e083-118">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="5e083-118">Click OK.</span></span>

## <a name="view-the-scheduling-results"></a><span data-ttu-id="5e083-119">スケジューリング結果の表示</span><span class="sxs-lookup"><span data-stu-id="5e083-119">View the scheduling results</span></span>
1. <span data-ttu-id="5e083-120">アクション ウィンドウで、[製造オーダー] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="5e083-120">On the Action Pane, click Production order.</span></span>
2. <span data-ttu-id="5e083-121">[すべてのジョブ] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="5e083-121">Click All jobs.</span></span>
    * <span data-ttu-id="5e083-122">このページでは、生成したスケジュール済ジョブを表示します。</span><span class="sxs-lookup"><span data-stu-id="5e083-122">This page displays the scheduled jobs that you have just generated.</span></span>  
3. <span data-ttu-id="5e083-123">[スケジューリング] セクションを展開または折りたたみます。</span><span class="sxs-lookup"><span data-stu-id="5e083-123">Expand or collapse the Scheduling section.</span></span>
    * <span data-ttu-id="5e083-124">[スケジューリング クイック タブ] で、予定日時を表示できます。</span><span class="sxs-lookup"><span data-stu-id="5e083-124">On the Scheduling FastTab, you can view the scheduled date and time.</span></span>  
4. <span data-ttu-id="5e083-125">[照会] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="5e083-125">Click Inquiries.</span></span>
5. <span data-ttu-id="5e083-126">[最大能力負荷] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="5e083-126">Click Capacity load.</span></span>
    * <span data-ttu-id="5e083-127">[最大能力負荷] ページは、ジョブのスケジューリングで予約されている時間数、リソースで現在予約済の合計時間数、リソースのジョブのスケジューリングで使用できる残り時間数を表示します。</span><span class="sxs-lookup"><span data-stu-id="5e083-127">The Capacity load page displays the capacity that is reserved through job scheduling, the total number of hours that are currently reserved on the resource, and the number of hours that remain available for job scheduling on the resource.</span></span>  
6. <span data-ttu-id="5e083-128">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="5e083-128">Close the page.</span></span>
7. <span data-ttu-id="5e083-129">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="5e083-129">Close the page.</span></span>

