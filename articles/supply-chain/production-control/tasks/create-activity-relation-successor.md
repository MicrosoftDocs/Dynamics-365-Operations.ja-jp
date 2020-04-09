---
title: 活動リレーションの作成 - 後続処理
description: リーン生産フローの活動フローは活動関係を通して文書化されています。
author: cvocph
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LeanProductionFlow, PlanActivity, PlanActivityRelationNew, PlanActivityLookup, DefaultDashboard
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: conradv
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: dfd9d515b9417ce0142b7bf5db3485902968e4de
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/18/2020
ms.locfileid: "3149300"
---
# <a name="create-activity-relation---successor"></a><span data-ttu-id="682d6-103">活動リレーションの作成 - 後続処理</span><span class="sxs-lookup"><span data-stu-id="682d6-103">Create activity relation - Successor</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="682d6-104">リーン生産フローの活動フローは活動関係を通して文書化されています。</span><span class="sxs-lookup"><span data-stu-id="682d6-104">The flow of activities in a lean production flow is documented through activity relations.</span></span> <span data-ttu-id="682d6-105">このレコードは、活動関係を作成する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="682d6-105">This recording shows how to create an activity relation.</span></span>

<span data-ttu-id="682d6-106">前提条件:</span><span class="sxs-lookup"><span data-stu-id="682d6-106">Prerequisites:</span></span>

- <span data-ttu-id="682d6-107">ドラフト モードの生産フローとバージョン。</span><span class="sxs-lookup"><span data-stu-id="682d6-107">A production flow and version in draft mode.</span></span> 

- <span data-ttu-id="682d6-108">生産フローで交互に実行される 2 つの活動が作成されましたが、関連付けられていません。</span><span class="sxs-lookup"><span data-stu-id="682d6-108">Two activities that follow each other in the production flow are created but not related.</span></span>


## <a name="find-the-production-flow-version"></a><span data-ttu-id="682d6-109">生産フロー バージョンの検索</span><span class="sxs-lookup"><span data-stu-id="682d6-109">Find the production flow version</span></span> 
1. <span data-ttu-id="682d6-110">[生産管理] > [設定] > [リーン生産フロー] > [生産フロー] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="682d6-110">Go to Production control > Setup > Lean production flow > Production flows.</span></span>
2. <span data-ttu-id="682d6-111">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="682d6-111">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="682d6-112">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="682d6-112">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="682d6-113">一覧で、選択された行をマークします。</span><span class="sxs-lookup"><span data-stu-id="682d6-113">In the list, mark the selected row.</span></span>
5. <span data-ttu-id="682d6-114">一覧で、ドラフト バージョンを選択します。</span><span class="sxs-lookup"><span data-stu-id="682d6-114">In the list, select a draft version.</span></span>
    * <span data-ttu-id="682d6-115">活動関係は、生産フローのドラフトか、有効なバージョンの両方に追加できます。</span><span class="sxs-lookup"><span data-stu-id="682d6-115">Activity relations can be added to both draft or active versions of a production flow.</span></span>  

## <a name="open-the-activity-overview"></a><span data-ttu-id="682d6-116">活動の概要を開く</span><span class="sxs-lookup"><span data-stu-id="682d6-116">Open the activity overview</span></span>
1. <span data-ttu-id="682d6-117">[活動] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="682d6-117">Click Activities.</span></span>
    * <span data-ttu-id="682d6-118">このフォームは、作業している生産フローのバージョンに割り当てられている生産フローのすべての活動を示すことに注意してください。</span><span class="sxs-lookup"><span data-stu-id="682d6-118">Note that the form shows all activities of the production flow that are allocated to the Version of the production flows that you are working in.</span></span>  

## <a name="add-a-successor"></a><span data-ttu-id="682d6-119">後続処理の追加</span><span class="sxs-lookup"><span data-stu-id="682d6-119">Add a Successor</span></span>
1. <span data-ttu-id="682d6-120">[後続処理の追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="682d6-120">Click Add successor.</span></span>
2. <span data-ttu-id="682d6-121">[活動] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="682d6-121">In the Activity field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="682d6-122">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="682d6-122">In the list, find and select the desired record.</span></span>
4. <span data-ttu-id="682d6-123">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="682d6-123">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="682d6-124">[制約] チェック ボックスをオンにします。</span><span class="sxs-lookup"><span data-stu-id="682d6-124">Select the Constraint check box.</span></span>
6. <span data-ttu-id="682d6-125">[制約値] フィールドで、値を入力します。</span><span class="sxs-lookup"><span data-stu-id="682d6-125">In the Constraint value field, enter a number.</span></span>
    * <span data-ttu-id="682d6-126">制約時間とは、先行処理の終了予定時刻 (期日の日時) と後続処理の開始予定時刻の間にスケジュールされる時間です。</span><span class="sxs-lookup"><span data-stu-id="682d6-126">The constraint time is the time to be scheduled between the scheduled end of the predecessor (due date and time) and the scheduled start of the successor.</span></span>  
7. <span data-ttu-id="682d6-127">[単位] フィールドで、値を入力します。</span><span class="sxs-lookup"><span data-stu-id="682d6-127">In the Units field, type a value.</span></span>
8. <span data-ttu-id="682d6-128">[サイクル時間の比率] フィールドで、数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="682d6-128">In the Cycle time ratio field, enter a number.</span></span>
    * <span data-ttu-id="682d6-129">両方の活動が同じタクトで実行される場合、サイクル時間率は 1 にしてください。</span><span class="sxs-lookup"><span data-stu-id="682d6-129">If both activities run at the same takt, the cycle time ratio should be 1.</span></span> <span data-ttu-id="682d6-130">先行処理が後続処理の 2 倍のスピードで実行される場合、サイクル時間率は 2 にしてください。</span><span class="sxs-lookup"><span data-stu-id="682d6-130">If the predecessor runs at the double speed of the successor, the ratio should be 2.</span></span>   <span data-ttu-id="682d6-131">サイクル時間率は生産フロー活動の個々のサイクル時間の計算に使用されます。</span><span class="sxs-lookup"><span data-stu-id="682d6-131">The cycle time ratios are used to calculate the individual cycle times of the production flow activities.</span></span>  
9. <span data-ttu-id="682d6-132">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="682d6-132">Click OK.</span></span>
10. <span data-ttu-id="682d6-133">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="682d6-133">Close the page.</span></span>
11. <span data-ttu-id="682d6-134">[グリッド パネル] タブをクリックします。</span><span class="sxs-lookup"><span data-stu-id="682d6-134">Click the GridPanel tab.</span></span>
12. <span data-ttu-id="682d6-135">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="682d6-135">Close the page.</span></span>
13. <span data-ttu-id="682d6-136">ページを更新します。</span><span class="sxs-lookup"><span data-stu-id="682d6-136">Refresh the page.</span></span>

