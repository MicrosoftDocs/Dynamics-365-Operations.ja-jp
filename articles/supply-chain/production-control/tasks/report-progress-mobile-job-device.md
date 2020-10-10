---
title: モバイル ジョブ デバイスでの進捗のレポート
description: この手順では、ジョブ デバイスの登録フォームで生産ジョブの進行を開始してレポートする方法を示します。
author: ShylaThompson
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: JmgRegistrationTouch, JmgRegistrationTouchUserConfiguration, JmgRegistrationTouchStart, JmgRegistrationTouchReportFeedback, JmgRegistrationTouchAssignedJobs, JmgRegistrationTouchBreak, JmgRegistrationTouchLeave, JmgRegistrationTouchIndirectActivity, JmgDialogForm, JmgRegistrationTouchReportProgress, JmgFeedbackWizard, JmgJobBundleProdFeedback
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 7a56e538d18c4e458f0e40801d0f01537a2246d2
ms.sourcegitcommit: 175f9394021322c685c5b37317c2f649c81a731a
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/21/2020
ms.locfileid: "3826270"
---
# <a name="report-progress-on-a-mobile-job-device"></a><span data-ttu-id="06bf6-103">モバイル ジョブ デバイスでの進捗のレポート</span><span class="sxs-lookup"><span data-stu-id="06bf6-103">Report progress on a mobile job device</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="06bf6-104">この手順では、ジョブ デバイスの登録フォームで生産ジョブの進行を開始してレポートする方法を示します。</span><span class="sxs-lookup"><span data-stu-id="06bf6-104">This procedure shows you how to start and report progress on a production job in the job device registration form.</span></span>



<span data-ttu-id="06bf6-105">この手順を実行するには、「システム管理者」または「機械オペレーター」ロールがユーザー アカウントと関連付けられている必要があります。</span><span class="sxs-lookup"><span data-stu-id="06bf6-105">To be able to run this procedure you must have the System administator or Machine Operator role associated with the user account.</span></span>

1. <span data-ttu-id="06bf6-106">[生産管理] > [製造実行] > [ジョブ カード デバイス] に移動します。</span><span class="sxs-lookup"><span data-stu-id="06bf6-106">Go to Production control > Manufacturing execution > Job card device.</span></span>
2. <span data-ttu-id="06bf6-107">WorkerTextField のフィールドで、作業者のバッジを入力します。</span><span class="sxs-lookup"><span data-stu-id="06bf6-107">In the WorkerTextField field, enter the badge of a worker.</span></span> <span data-ttu-id="06bf6-108">USMF のデモ データに、クリスティーナ Portra の「 123 」を入力します。</span><span class="sxs-lookup"><span data-stu-id="06bf6-108">In the USMF demo data type '123' for Christina Portra..</span></span>
3. <span data-ttu-id="06bf6-109">[ログイン] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="06bf6-109">Click Log in.</span></span>
4. <span data-ttu-id="06bf6-110">[フィルター] ボタンをクリックしてください。</span><span class="sxs-lookup"><span data-stu-id="06bf6-110">Click the Filter button.</span></span>
5. <span data-ttu-id="06bf6-111">[コンフィギュレーション フィルターの適用] チェック ボックスをオンまたはオフにします。</span><span class="sxs-lookup"><span data-stu-id="06bf6-111">Check or uncheck the Apply configuration filter check box.</span></span> <span data-ttu-id="06bf6-112">フィルターを設定すると、USMF の生産単位フィルタ 110 を使用できます。</span><span class="sxs-lookup"><span data-stu-id="06bf6-112">If you set a filter you can use production unit 110 in USMF.</span></span>
6. <span data-ttu-id="06bf6-113">[生産単位] フィールドで、作業者が作業できる生産ジョブのリソース グループを選択します。</span><span class="sxs-lookup"><span data-stu-id="06bf6-113">In the Production unit field, select the ressource group for which production jobs the worker can work on.</span></span>
7. <span data-ttu-id="06bf6-114">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="06bf6-114">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="06bf6-115">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="06bf6-115">Click OK.</span></span>
9. <span data-ttu-id="06bf6-116">[ジョブの開始] ボタンをクリックします。</span><span class="sxs-lookup"><span data-stu-id="06bf6-116">Click the Start job button.</span></span>
10. <span data-ttu-id="06bf6-117">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="06bf6-117">Click OK.</span></span>
11. <span data-ttu-id="06bf6-118">[進捗状況のレポート] ボタンをクリックします。</span><span class="sxs-lookup"><span data-stu-id="06bf6-118">Click the Report progress button.</span></span>
12. <span data-ttu-id="06bf6-119">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="06bf6-119">Click OK.</span></span>
13. <span data-ttu-id="06bf6-120">[次のジョブ] ボタンをクリックします。</span><span class="sxs-lookup"><span data-stu-id="06bf6-120">Click the Next job button.</span></span>
14. <span data-ttu-id="06bf6-121">[すべての生産ジョブの概要が表示されるように割り当て済] ボタンをクリックします。</span><span class="sxs-lookup"><span data-stu-id="06bf6-121">Click the Assigned to see an overview of all production jobs button.</span></span>
15. <span data-ttu-id="06bf6-122">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="06bf6-122">Close the page.</span></span>
16. <span data-ttu-id="06bf6-123">[休憩] ボタンをクリックします。</span><span class="sxs-lookup"><span data-stu-id="06bf6-123">Click the Break button.</span></span>
17. <span data-ttu-id="06bf6-124">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="06bf6-124">In the list, find and select the desired record.</span></span>
18. <span data-ttu-id="06bf6-125">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="06bf6-125">Click OK.</span></span>
19. <span data-ttu-id="06bf6-126">[終了] ボタンをクリックします。</span><span class="sxs-lookup"><span data-stu-id="06bf6-126">Click the Leaving button.</span></span>
20. <span data-ttu-id="06bf6-127">ログアウトする場合に選択します。</span><span class="sxs-lookup"><span data-stu-id="06bf6-127">Select to log out.</span></span>
21. <span data-ttu-id="06bf6-128">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="06bf6-128">Click OK.</span></span>
22. <span data-ttu-id="06bf6-129">WorkerTextField のフィールドで、再度ログインします。</span><span class="sxs-lookup"><span data-stu-id="06bf6-129">In the WorkerTextField field, log in again.</span></span> <span data-ttu-id="06bf6-130">USMF のデモ データ で、作業者「123」を選択できます。</span><span class="sxs-lookup"><span data-stu-id="06bf6-130">You can select worker '123' in USMF demo data.</span></span>
23. <span data-ttu-id="06bf6-131">[ログイン] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="06bf6-131">Click Log in.</span></span>
24. <span data-ttu-id="06bf6-132">[休憩を中止] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="06bf6-132">Click Stop break.</span></span>
25. <span data-ttu-id="06bf6-133">[活動] ボタンをクリックします。</span><span class="sxs-lookup"><span data-stu-id="06bf6-133">Click the Activity button.</span></span>
26. <span data-ttu-id="06bf6-134">[キャンセル] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="06bf6-134">Click Cancel.</span></span>
27. <span data-ttu-id="06bf6-135">[終了] ボタンをクリックします。</span><span class="sxs-lookup"><span data-stu-id="06bf6-135">Click the Leaving button.</span></span>
28. <span data-ttu-id="06bf6-136">退勤する場合に選択します。</span><span class="sxs-lookup"><span data-stu-id="06bf6-136">Select to clock out.</span></span>
29. <span data-ttu-id="06bf6-137">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="06bf6-137">Click OK.</span></span>
30. <span data-ttu-id="06bf6-138">早めに退勤する理由を選択します。</span><span class="sxs-lookup"><span data-stu-id="06bf6-138">Select a reason why you are clocking out early.</span></span>

