---
title: 給付金適格性処理
description: この手順は、給付金適格性処理が機能する方法を示します。
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysPolicySourceDocumentRuleType, SysPolicyListPage, SysPolicy, HcmBenefitEligibilityPolicy, HcmBenefit, BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations, Human Resources
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Version 7.0.0, Human Resources
ms.openlocfilehash: d23dcf4a16979b14ddf58b54e812f21e6698dfc7
ms.sourcegitcommit: ba340f836e472f13f263dec46a49847c788fca44
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/04/2020
ms.locfileid: "3430811"
---
# <a name="benefit-eligibility-process"></a><span data-ttu-id="970fa-103">給付金適格性処理</span><span class="sxs-lookup"><span data-stu-id="970fa-103">Benefit eligibility process</span></span>

<span data-ttu-id="970fa-104">この手順は、給付金適格性処理が機能する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="970fa-104">This procedure shows how the benefit eligibility process works.</span></span> <span data-ttu-id="970fa-105">プロセスが完了すると、結果を表示できます。</span><span class="sxs-lookup"><span data-stu-id="970fa-105">When the process is complete you can view the results.</span></span> <span data-ttu-id="970fa-106">この手順の作成に使用するデモ データの会社は USMF です。</span><span class="sxs-lookup"><span data-stu-id="970fa-106">The demo data company used to create this procedure is USMF.</span></span>

1. <span data-ttu-id="970fa-107">[人事管理] > [福利厚生] > [福利厚生] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="970fa-107">Go to Human resources > Benefits > Benefits.</span></span>
2. <span data-ttu-id="970fa-108">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="970fa-108">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="970fa-109">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="970fa-109">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="970fa-110">[編集] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="970fa-110">Click Edit.</span></span>
5. <span data-ttu-id="970fa-111">[適格性] フィールドで、「ルール ベース」を選択します。</span><span class="sxs-lookup"><span data-stu-id="970fa-111">In the Eligibility field, select 'Rule based'.</span></span>
6. <span data-ttu-id="970fa-112">[ルール タイプ] フィールドで、福利厚生に適用する福利厚生のポリシー ルールを選択します。</span><span class="sxs-lookup"><span data-stu-id="970fa-112">In the Rule type field, select the benefit policy rule you would like applied to the benefit.</span></span>
7. <span data-ttu-id="970fa-113">[アクション] ウィンドウで、[福利厚生] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="970fa-113">On the Action Pane, click Benefit.</span></span>
8. <span data-ttu-id="970fa-114">[適格性イベントの作成] をクリックして、ドロップ ダイアログを開きます。</span><span class="sxs-lookup"><span data-stu-id="970fa-114">Click Create eligibility event to open the drop dialog.</span></span>
9. <span data-ttu-id="970fa-115">[イベント] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="970fa-115">In the Event field, type a value.</span></span>
10. <span data-ttu-id="970fa-116">[説明] フィールドで値を入力します。</span><span class="sxs-lookup"><span data-stu-id="970fa-116">In the Description field, type a value.</span></span>
11. <span data-ttu-id="970fa-117">[イベント タイプ] フィールドで、「未処理の登録」を選択します。</span><span class="sxs-lookup"><span data-stu-id="970fa-117">In the Event type field, select 'Open enrollment'.</span></span>
12. <span data-ttu-id="970fa-118">[適用開始日] フィールドで、日時を入力します。</span><span class="sxs-lookup"><span data-stu-id="970fa-118">In the Coverage start date field, enter a date and time.</span></span>
13. <span data-ttu-id="970fa-119">[登録期間の開始日] フィールドで、日時を入力します。</span><span class="sxs-lookup"><span data-stu-id="970fa-119">In the Enrollment period start date field, enter a date and time.</span></span>
14. <span data-ttu-id="970fa-120">[登録するまでの日数] フィールドに、数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="970fa-120">In the Days to enroll field, enter a number.</span></span>
15. <span data-ttu-id="970fa-121">[イベントの作成] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="970fa-121">Click Create event.</span></span>
16. <span data-ttu-id="970fa-122">[作業者のクイックタブに追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="970fa-122">Click Add in the Workers FastTab.</span></span>
17. <span data-ttu-id="970fa-123">[タイプ別に表示] フィールドで「従業員」を選択します。</span><span class="sxs-lookup"><span data-stu-id="970fa-123">In the Show by type field, select 'Employees'.</span></span>
18. <span data-ttu-id="970fa-124">[法人別に表示] フィールドで、「現在の法人」を選択します。</span><span class="sxs-lookup"><span data-stu-id="970fa-124">In the Show by legal entity field, select 'Current legal entity'.</span></span>
19. <span data-ttu-id="970fa-125">一覧で、すべての行のマークを設定または解除します。</span><span class="sxs-lookup"><span data-stu-id="970fa-125">In the list, mark or unmark all rows.</span></span>
20. <span data-ttu-id="970fa-126">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="970fa-126">Click OK.</span></span>
21. <span data-ttu-id="970fa-127">[プロセス] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="970fa-127">Click Process.</span></span>
22. <span data-ttu-id="970fa-128">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="970fa-128">Click OK.</span></span>
23. <span data-ttu-id="970fa-129">ページを更新します。</span><span class="sxs-lookup"><span data-stu-id="970fa-129">Refresh the page.</span></span>
24. <span data-ttu-id="970fa-130">[結果の表示] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="970fa-130">Click Show results.</span></span>
25. <span data-ttu-id="970fa-131">[ステータス列フィルター] を開きます。</span><span class="sxs-lookup"><span data-stu-id="970fa-131">Open Status column filter.</span></span>
26. <span data-ttu-id="970fa-132">昇順で並べ替え</span><span class="sxs-lookup"><span data-stu-id="970fa-132">Sort A to Z</span></span>

