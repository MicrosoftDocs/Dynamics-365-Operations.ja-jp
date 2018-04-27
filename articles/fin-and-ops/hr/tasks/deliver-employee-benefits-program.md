--- 
title: "従業員手当プログラムの提供"
description: "このタスクは、新しい福利厚生の作成時に使用する福利厚生の要素の作成方法を示します。"
author: kherr75
manager: AnnBe
ms.date: 12/01/2015
ms.topic: business-process
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Operations, Talent
ms.search.region: Global
ms.author: kherr
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: c94f731cbdd62d51a21a42e8fcc86c5711c0e965
ms.contentlocale: ja-jp
ms.lasthandoff: 04/13/2018

---
# <a name="deliver-an-employee-benefits-program"></a><span data-ttu-id="85a69-103">従業員手当プログラムの提供</span><span class="sxs-lookup"><span data-stu-id="85a69-103">Deliver an employee benefits program</span></span>

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="85a69-104">このタスクは、新しい福利厚生の作成時に使用する福利厚生の要素の作成方法を示します。</span><span class="sxs-lookup"><span data-stu-id="85a69-104">This task will show you how to create benefit elements which will be used when creating a new benefit.</span></span> <span data-ttu-id="85a69-105">このタスクの作成に使用するデモ データの会社は USMF です。</span><span class="sxs-lookup"><span data-stu-id="85a69-105">The demo data company used to create this task is USMF.</span></span> <span data-ttu-id="85a69-106">このタスクは、報酬と給付金マネージャーのために用意されています。</span><span class="sxs-lookup"><span data-stu-id="85a69-106">This task is intended for a Compensation and Benefits manager.</span></span>


## <a name="create-benefit-elements"></a><span data-ttu-id="85a69-107">給付金の要素の作成</span><span class="sxs-lookup"><span data-stu-id="85a69-107">Create benefit elements</span></span>
1. <span data-ttu-id="85a69-108">このタスクは [福利厚生] のリスト ページから開始します。</span><span class="sxs-lookup"><span data-stu-id="85a69-108">This task starts from the Benefits list page.</span></span> <span data-ttu-id="85a69-109">そのページを開く、または福利厚生のリスト ページを検索することにより、タスクを開始します。</span><span class="sxs-lookup"><span data-stu-id="85a69-109">Start the task by opening that page or searching the Benefits list page.</span></span>
2. <span data-ttu-id="85a69-110">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="85a69-110">Click New.</span></span>
3. <span data-ttu-id="85a69-111">[タイプ] フィールドに、作成する福利厚生タイプの名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="85a69-111">In the Type field, Enter the name of the type of benefit you are creating..</span></span>
4. <span data-ttu-id="85a69-112">[説明] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="85a69-112">In the Description field, type a value.</span></span>
5. <span data-ttu-id="85a69-113">[同時登録] フィールドで、オプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="85a69-113">In the Concurrent enrollment field, select an option.</span></span>
    * <span data-ttu-id="85a69-114">複数の医療プランに登録する従業員の能力を制限するには、[種類ごとに 1 つの登録] を選択します。</span><span class="sxs-lookup"><span data-stu-id="85a69-114">To restrict employees' ability to enroll in multiple medical plans, select One enrollment per type.</span></span>  
6. <span data-ttu-id="85a69-115">[給与カテゴリ] フィールドで、オプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="85a69-115">In the Payroll category field, select an option.</span></span>
7. <span data-ttu-id="85a69-116">[計画] タブをクリックします</span><span class="sxs-lookup"><span data-stu-id="85a69-116">Click the Plans tab.</span></span>
8. <span data-ttu-id="85a69-117">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="85a69-117">Click New.</span></span>
9. <span data-ttu-id="85a69-118">[計画] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="85a69-118">In the Plan field, type a value.</span></span>
10. <span data-ttu-id="85a69-119">[説明] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="85a69-119">In the Description field, type a value.</span></span>
11. <span data-ttu-id="85a69-120">[タイプ] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="85a69-120">In the Type field, click the drop-down button to open the lookup.</span></span>
12. <span data-ttu-id="85a69-121">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="85a69-121">In the list, find and select the desired record.</span></span>
13. <span data-ttu-id="85a69-122">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="85a69-122">In the list, click the link in the selected row.</span></span>
14. <span data-ttu-id="85a69-123">[給与の影響] フィールドで、オプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="85a69-123">In the Payroll impact field, select an option.</span></span>
15. <span data-ttu-id="85a69-124">[オプション] タブをクリックします。</span><span class="sxs-lookup"><span data-stu-id="85a69-124">Click the Options tab.</span></span>
16. <span data-ttu-id="85a69-125">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="85a69-125">Click New.</span></span>
17. <span data-ttu-id="85a69-126">[オプション] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="85a69-126">In the Option field, type a value.</span></span>
18. <span data-ttu-id="85a69-127">[説明] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="85a69-127">In the Description field, type a value.</span></span>

## <a name="create-a-benefit"></a><span data-ttu-id="85a69-128">給付金の作成</span><span class="sxs-lookup"><span data-stu-id="85a69-128">Create a benefit</span></span>
1. <span data-ttu-id="85a69-129">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="85a69-129">Close the page.</span></span>
2. <span data-ttu-id="85a69-130">[人事管理] > [福利厚生] > [福利厚生] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="85a69-130">Go to Human resources > Benefits > Benefits.</span></span>
3. <span data-ttu-id="85a69-131">[新規] をクリックすると、ドロップ ダイアログが開きます。</span><span class="sxs-lookup"><span data-stu-id="85a69-131">Click New to open the drop dialog.</span></span>
4. <span data-ttu-id="85a69-132">[計画] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="85a69-132">In the Plan field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="85a69-133">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="85a69-133">In the list, find and select the desired record.</span></span>
6. <span data-ttu-id="85a69-134">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="85a69-134">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="85a69-135">[オプション] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="85a69-135">In the Option field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="85a69-136">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="85a69-136">In the list, find and select the desired record.</span></span>
9. <span data-ttu-id="85a69-137">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="85a69-137">In the list, click the link in the selected row.</span></span>
10. <span data-ttu-id="85a69-138">[有効開始] フィールドで、日付と時刻を入力します。</span><span class="sxs-lookup"><span data-stu-id="85a69-138">In the Effective field, enter a date and time.</span></span>
11. <span data-ttu-id="85a69-139">[福利厚生の作成] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="85a69-139">Click Create benefit.</span></span>
12. <span data-ttu-id="85a69-140">[給与の詳細] セクションの展開を切り替えます。</span><span class="sxs-lookup"><span data-stu-id="85a69-140">Toggle the expansion of the Payroll details section.</span></span>
13. <span data-ttu-id="85a69-141">[頻度] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="85a69-141">In the Frequency field, click the drop-down button to open the lookup.</span></span>
14. <span data-ttu-id="85a69-142">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="85a69-142">In the list, find and select the desired record.</span></span>
15. <span data-ttu-id="85a69-143">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="85a69-143">In the list, click the link in the selected row.</span></span>
16. <span data-ttu-id="85a69-144">[基準] フィールドで、オプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="85a69-144">In the Basis field, select an option.</span></span>
17. <span data-ttu-id="85a69-145">[金額またはレート] フィールドに数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="85a69-145">In the Amount or rate field, enter a number.</span></span>


