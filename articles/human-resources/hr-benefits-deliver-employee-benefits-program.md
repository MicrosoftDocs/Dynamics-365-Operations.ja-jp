---
title: 従業員手当プログラムの提供
description: この記事では、新しい福利厚生の作成時に使用する福利厚生の要素の作成方法を示します。
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: HcmBenefitElementSetup, HcmBenefit, HcmBenefitNewBenefit, HcmBenefitPlanLookup
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations, Human Resources
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Version 7.0.0, Human Resources
ms.openlocfilehash: b8631e4f8cb2947ec7e09de86a7ceb075a83a453
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 02/03/2020
ms.locfileid: "3009742"
---
# <a name="deliver-employee-benefits-program"></a><span data-ttu-id="cc7bd-103">従業員手当プログラムの提供</span><span class="sxs-lookup"><span data-stu-id="cc7bd-103">Deliver employee benefits program</span></span>

<span data-ttu-id="cc7bd-104">この記事では、新しい福利厚生の作成時に使用する福利厚生の要素の作成方法を示します。</span><span class="sxs-lookup"><span data-stu-id="cc7bd-104">This article shows you how to create benefit elements which will be used when creating a new benefit.</span></span> <span data-ttu-id="cc7bd-105">このタスクの作成に使用するデモ データの会社は USMF です。</span><span class="sxs-lookup"><span data-stu-id="cc7bd-105">The demo data company used to create this task is USMF.</span></span> <span data-ttu-id="cc7bd-106">このタスクは、報酬と給付金マネージャーのために用意されています。</span><span class="sxs-lookup"><span data-stu-id="cc7bd-106">This task is intended for a Compensation and Benefits manager.</span></span>


## <a name="create-benefit-elements"></a><span data-ttu-id="cc7bd-107">給付金の要素の作成</span><span class="sxs-lookup"><span data-stu-id="cc7bd-107">Create benefit elements</span></span>
1. <span data-ttu-id="cc7bd-108">このタスクは [福利厚生] のリスト ページから開始します。</span><span class="sxs-lookup"><span data-stu-id="cc7bd-108">This task starts from the Benefits list page.</span></span> <span data-ttu-id="cc7bd-109">そのページを開く、または福利厚生のリスト ページを検索することにより、タスクを開始します。</span><span class="sxs-lookup"><span data-stu-id="cc7bd-109">Start the task by opening that page or searching the Benefits list page.</span></span>
2. <span data-ttu-id="cc7bd-110">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="cc7bd-110">Click New.</span></span>
3. <span data-ttu-id="cc7bd-111">[タイプ] フィールドに、作成する福利厚生タイプの名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="cc7bd-111">In the Type field, Enter the name of the type of benefit you are creating..</span></span>
4. <span data-ttu-id="cc7bd-112">[説明] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="cc7bd-112">In the Description field, type a value.</span></span>
5. <span data-ttu-id="cc7bd-113">[同時登録] フィールドで、オプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="cc7bd-113">In the Concurrent enrollment field, select an option.</span></span>
    * <span data-ttu-id="cc7bd-114">複数の医療プランに登録する従業員の能力を制限するには、[種類ごとに 1 つの登録] を選択します。</span><span class="sxs-lookup"><span data-stu-id="cc7bd-114">To restrict employees' ability to enroll in multiple medical plans, select One enrollment per type.</span></span>  
6. <span data-ttu-id="cc7bd-115">[給与カテゴリ] フィールドで、オプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="cc7bd-115">In the Payroll category field, select an option.</span></span>
7. <span data-ttu-id="cc7bd-116">[計画] タブをクリックします</span><span class="sxs-lookup"><span data-stu-id="cc7bd-116">Click the Plans tab.</span></span>
8. <span data-ttu-id="cc7bd-117">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="cc7bd-117">Click New.</span></span>
9. <span data-ttu-id="cc7bd-118">[計画] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="cc7bd-118">In the Plan field, type a value.</span></span>
10. <span data-ttu-id="cc7bd-119">[説明] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="cc7bd-119">In the Description field, type a value.</span></span>
11. <span data-ttu-id="cc7bd-120">[タイプ] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="cc7bd-120">In the Type field, click the drop-down button to open the lookup.</span></span>
12. <span data-ttu-id="cc7bd-121">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="cc7bd-121">In the list, find and select the desired record.</span></span>
13. <span data-ttu-id="cc7bd-122">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="cc7bd-122">In the list, click the link in the selected row.</span></span>
14. <span data-ttu-id="cc7bd-123">[給与の影響] フィールドで、オプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="cc7bd-123">In the Payroll impact field, select an option.</span></span>
15. <span data-ttu-id="cc7bd-124">[オプション] タブをクリックします。</span><span class="sxs-lookup"><span data-stu-id="cc7bd-124">Click the Options tab.</span></span>
16. <span data-ttu-id="cc7bd-125">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="cc7bd-125">Click New.</span></span>
17. <span data-ttu-id="cc7bd-126">[オプション] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="cc7bd-126">In the Option field, type a value.</span></span>
18. <span data-ttu-id="cc7bd-127">[説明] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="cc7bd-127">In the Description field, type a value.</span></span>

## <a name="create-a-benefit"></a><span data-ttu-id="cc7bd-128">給付金の作成</span><span class="sxs-lookup"><span data-stu-id="cc7bd-128">Create a benefit</span></span>
1. <span data-ttu-id="cc7bd-129">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="cc7bd-129">Close the page.</span></span>
2. <span data-ttu-id="cc7bd-130">[人事管理] > [福利厚生] > [福利厚生] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="cc7bd-130">Go to Human resources > Benefits > Benefits.</span></span>
3. <span data-ttu-id="cc7bd-131">[新規] をクリックすると、ドロップ ダイアログが開きます。</span><span class="sxs-lookup"><span data-stu-id="cc7bd-131">Click New to open the drop dialog.</span></span>
4. <span data-ttu-id="cc7bd-132">[計画] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="cc7bd-132">In the Plan field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="cc7bd-133">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="cc7bd-133">In the list, find and select the desired record.</span></span>
6. <span data-ttu-id="cc7bd-134">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="cc7bd-134">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="cc7bd-135">[オプション] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="cc7bd-135">In the Option field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="cc7bd-136">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="cc7bd-136">In the list, find and select the desired record.</span></span>
9. <span data-ttu-id="cc7bd-137">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="cc7bd-137">In the list, click the link in the selected row.</span></span>
10. <span data-ttu-id="cc7bd-138">[有効開始] フィールドで、日付と時刻を入力します。</span><span class="sxs-lookup"><span data-stu-id="cc7bd-138">In the Effective field, enter a date and time.</span></span>
11. <span data-ttu-id="cc7bd-139">[福利厚生の作成] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="cc7bd-139">Click Create benefit.</span></span>
12. <span data-ttu-id="cc7bd-140">[給与の詳細] セクションの展開を切り替えます。</span><span class="sxs-lookup"><span data-stu-id="cc7bd-140">Toggle the expansion of the Payroll details section.</span></span>
13. <span data-ttu-id="cc7bd-141">[頻度] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="cc7bd-141">In the Frequency field, click the drop-down button to open the lookup.</span></span>
14. <span data-ttu-id="cc7bd-142">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="cc7bd-142">In the list, find and select the desired record.</span></span>
15. <span data-ttu-id="cc7bd-143">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="cc7bd-143">In the list, click the link in the selected row.</span></span>
16. <span data-ttu-id="cc7bd-144">[基準] フィールドで、オプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="cc7bd-144">In the Basis field, select an option.</span></span>
17. <span data-ttu-id="cc7bd-145">[金額またはレート] フィールドに数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="cc7bd-145">In the Amount or rate field, enter a number.</span></span>

