---
title: 求人の作成と実施
description: 採用プロジェクトにより、採用プロセスの管理が容易になります。
author: andreabichsel
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: HRMRecruitingTable, HcmWorkerLookUp, HcmJobLookup, HRMRecruitingMedia, HRMRecruitingJobAd
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 556f99d34521cce70efb64c5fbababd815e8429d
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/07/2019
ms.locfileid: "1507718"
---
# <a name="develop-and-open-job-requisition"></a><span data-ttu-id="22972-103">求人の作成と実施</span><span class="sxs-lookup"><span data-stu-id="22972-103">Develop and open job requisition</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="22972-104">採用プロジェクトにより、採用プロセスの管理が容易になります。</span><span class="sxs-lookup"><span data-stu-id="22972-104">Recruitment projects help manage the recruiting process.</span></span> <span data-ttu-id="22972-105">各採用プロジェクトについて、採用するジョブ、リクルーター名、プロジェクトの状態、ジョブが存在する部門などの情報を設定できます。</span><span class="sxs-lookup"><span data-stu-id="22972-105">For each recruitment project, you can set up information, such as the job that recruiting is for, the name of the recruiter, the status of the project and the department that the job will be located in.</span></span> <span data-ttu-id="22972-106">採用プロジェクトを作成すると、プロジェクトの求人広告の書き込み、[従業員セルフサービス] ページでの求人広告の発行、雇用申請とプロジェクトの関連付け、そのプロジェクトの活動の追跡を行うことができます。</span><span class="sxs-lookup"><span data-stu-id="22972-106">After creating a recruitment project, you can write a job advertisement for the project, publish the ad on Employee self-service pages, associate applications for employment with the project, and track activities for that project.</span></span> <span data-ttu-id="22972-107">この手順の作成に使用するデモ データの会社は USMF です。</span><span class="sxs-lookup"><span data-stu-id="22972-107">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="22972-108">手順を開始するには、[人事管理] > [採用] > [採用プロジェクト] > [採用プロジェクト] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="22972-108">To begin the procedure, go to Human resources > Recruitment > Recruitment projects > Recruitment projects</span></span>

1. <span data-ttu-id="22972-109">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="22972-109">Click New.</span></span>
2. <span data-ttu-id="22972-110">[採用プロジェクト] フィールドで、値を入力します。</span><span class="sxs-lookup"><span data-stu-id="22972-110">In the Recruitment project field, type a value.</span></span>
3. <span data-ttu-id="22972-111">[説明] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="22972-111">In the Description field, type a value.</span></span>
4. <span data-ttu-id="22972-112">[採用] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="22972-112">In the Recruiter field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="22972-113">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="22972-113">In the list, find and select the desired record.</span></span>
6. <span data-ttu-id="22972-114">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="22972-114">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="22972-115">[選択] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="22972-115">Click Select.</span></span>
8. <span data-ttu-id="22972-116">[部門] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="22972-116">In the Department field, click the drop-down button to open the lookup.</span></span>
9. <span data-ttu-id="22972-117">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="22972-117">In the list, click the link in the selected row.</span></span>
10. <span data-ttu-id="22972-118">[職務] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="22972-118">In the Job field, click the drop-down button to open the lookup.</span></span>
11. <span data-ttu-id="22972-119">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="22972-119">In the list, find and select the desired record.</span></span>
12. <span data-ttu-id="22972-120">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="22972-120">In the list, click the link in the selected row.</span></span>
13. <span data-ttu-id="22972-121">[求人数] フィールドに数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="22972-121">In the Number of openings field, enter a number.</span></span>
14. <span data-ttu-id="22972-122">[採用マネージャー] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="22972-122">In the Hiring manager field, click the drop-down button to open the lookup.</span></span>
15. <span data-ttu-id="22972-123">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="22972-123">In the list, find and select the desired record.</span></span>
16. <span data-ttu-id="22972-124">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="22972-124">In the list, click the link in the selected row.</span></span>
17. <span data-ttu-id="22972-125">[選択] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="22972-125">Click Select.</span></span>
18. <span data-ttu-id="22972-126">[申込期限] フィールドに日付を入力します。</span><span class="sxs-lookup"><span data-stu-id="22972-126">In the Application deadline field, enter a date.</span></span>
19. <span data-ttu-id="22972-127">[メディア] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="22972-127">Click Media.</span></span>
    * <span data-ttu-id="22972-128">採用プロジェクトには、空いている職位の広告に使用するメディア露出の指定のオプションが含まれます。</span><span class="sxs-lookup"><span data-stu-id="22972-128">Recruitment projects include the option to specify media outlets to use to advertise open positions.</span></span>  
20. <span data-ttu-id="22972-129">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="22972-129">Click New.</span></span>
21. <span data-ttu-id="22972-130">[メディア] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="22972-130">In the Media field, click the drop-down button to open the lookup.</span></span>
22. <span data-ttu-id="22972-131">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="22972-131">In the list, click the link in the selected row.</span></span>
23. <span data-ttu-id="22972-132">[開始日] フィールドに日付を入力します。</span><span class="sxs-lookup"><span data-stu-id="22972-132">In the Start date field, enter a date.</span></span>
24. <span data-ttu-id="22972-133">[終了日] フィールドに日付を入力します。</span><span class="sxs-lookup"><span data-stu-id="22972-133">In the End date field, enter a date.</span></span>
25. <span data-ttu-id="22972-134">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="22972-134">Click Save.</span></span>
26. <span data-ttu-id="22972-135">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="22972-135">Close the page.</span></span>
27. <span data-ttu-id="22972-136">[ジョブ広告] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="22972-136">Click Job ads.</span></span>
28. <span data-ttu-id="22972-137">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="22972-137">Click Save.</span></span>
29. <span data-ttu-id="22972-138">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="22972-138">Close the page.</span></span>
30. <span data-ttu-id="22972-139">[従業員セルフ サービスに表示] のチェック ボックスをオンまたはオフにします。</span><span class="sxs-lookup"><span data-stu-id="22972-139">Check or uncheck the Display on employee self service checkbox.</span></span>
    * <span data-ttu-id="22972-140">[従業員セルフ サービスに表示します] のチェック ボックスをオンにすると、採用プロジェクトを [従業員セルフサービス] のページで従業員に対して表示します。</span><span class="sxs-lookup"><span data-stu-id="22972-140">Select the Display on employee self service check box to make the recruitment project visible to employees on their Employee self-service pages.</span></span>  
31. <span data-ttu-id="22972-141">[採用プロジェクトの状態] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="22972-141">Click Recruitment project status.</span></span>
32. <span data-ttu-id="22972-142">[開始] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="22972-142">Click Start.</span></span>
    * <span data-ttu-id="22972-143">開始済ステータスは、プロジェクトが応募を受け付ける準備が整っていることを示します。</span><span class="sxs-lookup"><span data-stu-id="22972-143">The Started status means that the project is ready to receive applications.</span></span>  
33. <span data-ttu-id="22972-144">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="22972-144">Click OK.</span></span>

