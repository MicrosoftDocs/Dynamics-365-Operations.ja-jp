---
title: モバイル ジョブ デバイスでの進捗のレポート
description: この手順では、ジョブ デバイスの登録フォームで生産ジョブの進行を開始してレポートする方法を示します。
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: JmgRegistrationTouch, JmgRegistrationTouchUserConfiguration, JmgRegistrationTouchStart, JmgRegistrationTouchReportFeedback, JmgRegistrationTouchAssignedJobs, JmgRegistrationTouchBreak, JmgRegistrationTouchLeave, JmgRegistrationTouchIndirectActivity, JmgDialogForm
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 70cdd5aff68581af29984e88a16339de921c8ff0
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/18/2020
ms.locfileid: "3146655"
---
# <a name="report-progress-on-a-mobile-job-device"></a><span data-ttu-id="4d6d2-103">モバイル ジョブ デバイスでの進捗のレポート</span><span class="sxs-lookup"><span data-stu-id="4d6d2-103">Report progress on a mobile job device</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="4d6d2-104">この手順では、ジョブ デバイスの登録フォームで生産ジョブの進行を開始してレポートする方法を示します。</span><span class="sxs-lookup"><span data-stu-id="4d6d2-104">This procedure shows you how to start and report progress on a production job in the job device registration form.</span></span>



<span data-ttu-id="4d6d2-105">この手順を実行するには、「システム管理者」または「機械オペレーター」ロールがユーザー アカウントと関連付けられている必要があります。</span><span class="sxs-lookup"><span data-stu-id="4d6d2-105">To be able to run this procedure you must have the System administator or Machine Operator role associated with the user account.</span></span>

1. <span data-ttu-id="4d6d2-106">[生産管理] > [製造実行] > [ジョブ カード デバイス] に移動します。</span><span class="sxs-lookup"><span data-stu-id="4d6d2-106">Go to Production control > Manufacturing execution > Job card device.</span></span>
2. <span data-ttu-id="4d6d2-107">WorkerTextField のフィールドで、作業者のバッジを入力します。</span><span class="sxs-lookup"><span data-stu-id="4d6d2-107">In the WorkerTextField field, enter the badge of a worker.</span></span> <span data-ttu-id="4d6d2-108">USMF のデモ データに、クリスティーナ Portra の「 123 」を入力します。</span><span class="sxs-lookup"><span data-stu-id="4d6d2-108">In the USMF demo data type '123' for Christina Portra..</span></span>
3. <span data-ttu-id="4d6d2-109">[ログイン] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="4d6d2-109">Click Log in.</span></span>
4. <span data-ttu-id="4d6d2-110">[フィルター] ボタンをクリックしてください。</span><span class="sxs-lookup"><span data-stu-id="4d6d2-110">Click the Filter button.</span></span>
5. <span data-ttu-id="4d6d2-111">[コンフィギュレーション フィルターの適用] チェック ボックスをオンまたはオフにします。</span><span class="sxs-lookup"><span data-stu-id="4d6d2-111">Check or uncheck the Apply configuration filter check box.</span></span> <span data-ttu-id="4d6d2-112">フィルターを設定すると、USMF の生産単位フィルタ 110 を使用できます。</span><span class="sxs-lookup"><span data-stu-id="4d6d2-112">If you set a filter you can use production unit 110 in USMF.</span></span>
6. <span data-ttu-id="4d6d2-113">[生産単位] フィールドで、作業者が作業できる生産ジョブのリソース グループを選択します。</span><span class="sxs-lookup"><span data-stu-id="4d6d2-113">In the Production unit field, select the ressource group for which production jobs the worker can work on.</span></span>
7. <span data-ttu-id="4d6d2-114">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="4d6d2-114">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="4d6d2-115">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="4d6d2-115">Click OK.</span></span>
9. <span data-ttu-id="4d6d2-116">[ジョブの開始] ボタンをクリックします。</span><span class="sxs-lookup"><span data-stu-id="4d6d2-116">Click the Start job button.</span></span>
10. <span data-ttu-id="4d6d2-117">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="4d6d2-117">Click OK.</span></span>
11. <span data-ttu-id="4d6d2-118">[進捗状況のレポート] ボタンをクリックします。</span><span class="sxs-lookup"><span data-stu-id="4d6d2-118">Click the Report progress button.</span></span>
12. <span data-ttu-id="4d6d2-119">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="4d6d2-119">Click OK.</span></span>
13. <span data-ttu-id="4d6d2-120">[次のジョブ] ボタンをクリックします。</span><span class="sxs-lookup"><span data-stu-id="4d6d2-120">Click the Next job button.</span></span>
14. <span data-ttu-id="4d6d2-121">[すべての生産ジョブの概要が表示されるように割り当て済] ボタンをクリックします。</span><span class="sxs-lookup"><span data-stu-id="4d6d2-121">Click the Assigned to see an overview of all production jobs button.</span></span>
15. <span data-ttu-id="4d6d2-122">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="4d6d2-122">Close the page.</span></span>
16. <span data-ttu-id="4d6d2-123">[休憩] ボタンをクリックします。</span><span class="sxs-lookup"><span data-stu-id="4d6d2-123">Click the Break button.</span></span>
17. <span data-ttu-id="4d6d2-124">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="4d6d2-124">In the list, find and select the desired record.</span></span>
18. <span data-ttu-id="4d6d2-125">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="4d6d2-125">Click OK.</span></span>
19. <span data-ttu-id="4d6d2-126">[終了] ボタンをクリックします。</span><span class="sxs-lookup"><span data-stu-id="4d6d2-126">Click the Leaving button.</span></span>
20. <span data-ttu-id="4d6d2-127">ログアウトする場合に選択します。</span><span class="sxs-lookup"><span data-stu-id="4d6d2-127">Select to log out.</span></span>
21. <span data-ttu-id="4d6d2-128">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="4d6d2-128">Click OK.</span></span>
22. <span data-ttu-id="4d6d2-129">WorkerTextField のフィールドで、再度ログインします。</span><span class="sxs-lookup"><span data-stu-id="4d6d2-129">In the WorkerTextField field, log in again.</span></span> <span data-ttu-id="4d6d2-130">USMF のデモ データ で、作業者「123」を選択できます。</span><span class="sxs-lookup"><span data-stu-id="4d6d2-130">You can select worker '123' in USMF demo data.</span></span>
23. <span data-ttu-id="4d6d2-131">[ログイン] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="4d6d2-131">Click Log in.</span></span>
24. <span data-ttu-id="4d6d2-132">[休憩を中止] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="4d6d2-132">Click Stop break.</span></span>
25. <span data-ttu-id="4d6d2-133">[活動] ボタンをクリックします。</span><span class="sxs-lookup"><span data-stu-id="4d6d2-133">Click the Activity button.</span></span>
26. <span data-ttu-id="4d6d2-134">[キャンセル] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="4d6d2-134">Click Cancel.</span></span>
27. <span data-ttu-id="4d6d2-135">[終了] ボタンをクリックします。</span><span class="sxs-lookup"><span data-stu-id="4d6d2-135">Click the Leaving button.</span></span>
28. <span data-ttu-id="4d6d2-136">退勤する場合に選択します。</span><span class="sxs-lookup"><span data-stu-id="4d6d2-136">Select to clock out.</span></span>
29. <span data-ttu-id="4d6d2-137">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="4d6d2-137">Click OK.</span></span>
30. <span data-ttu-id="4d6d2-138">早めに退勤する理由を選択します。</span><span class="sxs-lookup"><span data-stu-id="4d6d2-138">Select a reason why you are clocking out early.</span></span>

