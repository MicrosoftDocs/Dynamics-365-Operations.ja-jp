--- 
title: "詳細ルール構造の作成と割り当て"
description: "このタスク ガイドでは、詳細ルール構造の作成と勘定構造への割り当てについて説明します。"
author: aprilolson
manager: AnnBe
ms.date: 10/26/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 42b474302f5a930c3f7969317ba68cb3f22acd91
ms.contentlocale: ja-jp
ms.lasthandoff: 04/13/2018

---
# <a name="create-and-assign-advanced-rule-structures"></a><span data-ttu-id="555d6-103">詳細ルール構造の作成と割り当て</span><span class="sxs-lookup"><span data-stu-id="555d6-103">Create and assign advanced rule structures</span></span>

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="555d6-104">このタスク ガイドでは、詳細ルール構造の作成と勘定構造への割り当てについて説明します。</span><span class="sxs-lookup"><span data-stu-id="555d6-104">This task guide steps through creating and assigning an advanced rule structure to an account structure.</span></span> <span data-ttu-id="555d6-105">このガイドでは、USMF デモ会社を使用します。</span><span class="sxs-lookup"><span data-stu-id="555d6-105">This guide uses the USMF demo company.</span></span>


## <a name="create-an-advanced-rule-structure"></a><span data-ttu-id="555d6-106">詳細なルール構造の作成</span><span class="sxs-lookup"><span data-stu-id="555d6-106">Create an advanced rule structure</span></span>
1. <span data-ttu-id="555d6-107">[総勘定元帳] > [勘定科目表] > [構造] > [詳細ルール構造] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="555d6-107">Go to General ledger > Chart of accounts > Structures > Advanced rule structures.</span></span>
2. <span data-ttu-id="555d6-108">[新規] をクリックすると、ドロップ ダイアログが開きます。</span><span class="sxs-lookup"><span data-stu-id="555d6-108">Click New to open the drop dialog.</span></span>
3. <span data-ttu-id="555d6-109">[詳細ルール構造] フィールドにルール構造を説明する名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="555d6-109">In the Advanced rule structure field, type a name to describe the rule structure.</span></span>
4. <span data-ttu-id="555d6-110">[説明] フィールドに構造を説明する値を入力します。</span><span class="sxs-lookup"><span data-stu-id="555d6-110">In the Description field, type a value to describe the structure.</span></span>
5. <span data-ttu-id="555d6-111">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="555d6-111">Click OK.</span></span>
6. <span data-ttu-id="555d6-112">[区分の追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="555d6-112">Click Add segment.</span></span>
7. <span data-ttu-id="555d6-113">区分リストで、財務分析コードを選択します。</span><span class="sxs-lookup"><span data-stu-id="555d6-113">In the list of segments, select a financial dimension.</span></span>
    * <span data-ttu-id="555d6-114">たとえば [店舗] です。</span><span class="sxs-lookup"><span data-stu-id="555d6-114">For example, Store.</span></span>  
8. <span data-ttu-id="555d6-115">[区分の追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="555d6-115">Click Add segment.</span></span>
9. <span data-ttu-id="555d6-116">一覧で、詳細ルール構造を表示するリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="555d6-116">In the list, click the link of the advanced rule structure to view it.</span></span>
10. <span data-ttu-id="555d6-117">[有効化] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="555d6-117">Click Activate.</span></span>
11. <span data-ttu-id="555d6-118">[有効化] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="555d6-118">Click Activate.</span></span>

## <a name="apply-an-advanced-rule-structure-to-an-account-structure"></a><span data-ttu-id="555d6-119">詳細ルール構造の勘定構造への適用</span><span class="sxs-lookup"><span data-stu-id="555d6-119">Apply an advanced rule structure to an account structure</span></span>
1. <span data-ttu-id="555d6-120">フォームを閉じます。</span><span class="sxs-lookup"><span data-stu-id="555d6-120">Close the form.</span></span>
2. <span data-ttu-id="555d6-121">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="555d6-121">Close the page.</span></span>
3. <span data-ttu-id="555d6-122">[総勘定元帳] > [勘定科目表] > [構造] > [勘定構造のコンフィギュレーション] に移動します。</span><span class="sxs-lookup"><span data-stu-id="555d6-122">Go to General ledger > Chart of accounts > Structures > Configure account structures.</span></span>
4. <span data-ttu-id="555d6-123">一覧で、詳細ルールを適用する勘定構造を検索し選択します。</span><span class="sxs-lookup"><span data-stu-id="555d6-123">In the list, find and select the account structure you want to apply the advanced rule to.</span></span>
5. <span data-ttu-id="555d6-124">勘定構造の名前をクリックして開きます。</span><span class="sxs-lookup"><span data-stu-id="555d6-124">Click the name of the account structure to open it.</span></span>
6. <span data-ttu-id="555d6-125">[編集] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="555d6-125">Click Edit.</span></span>
    * <span data-ttu-id="555d6-126">[詳細ルール] をクリックすると、勘定構造を [ドラフト モード] に設定するよう要求されます。</span><span class="sxs-lookup"><span data-stu-id="555d6-126">You can also click Advanced rules and you will be prompted to put the account structure in Draft mode.</span></span>  
7. <span data-ttu-id="555d6-127">[詳細ルール] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="555d6-127">Click Advanced rules.</span></span>
8. <span data-ttu-id="555d6-128">[新規] をクリックすると、ドロップ ダイアログが開きます。</span><span class="sxs-lookup"><span data-stu-id="555d6-128">Click New to open the drop dialog.</span></span>
9. <span data-ttu-id="555d6-129">[詳細ルール] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="555d6-129">In the Advanced rule field, type a value.</span></span>
10. <span data-ttu-id="555d6-130">[名前] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="555d6-130">In the Name field, type a value.</span></span>
11. <span data-ttu-id="555d6-131">[作成] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="555d6-131">Click Create.</span></span>
12. <span data-ttu-id="555d6-132">[新しい基準の追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="555d6-132">Click Add new criteria.</span></span>
13. <span data-ttu-id="555d6-133">[適用箇所] フィールドで、主勘定または財務分析コードを選択します。</span><span class="sxs-lookup"><span data-stu-id="555d6-133">In the Where field, select main account or a financial dimension.</span></span>
14. <span data-ttu-id="555d6-134">[演算子] フィールドで、「is between」や「includes」などのオプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="555d6-134">In the Operator field, select an option, such as is between and includes.</span></span>
15. <span data-ttu-id="555d6-135">[値] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="555d6-135">In the Value field, type a value.</span></span>
16. <span data-ttu-id="555d6-136">[終了日] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="555d6-136">In the through field, type a value.</span></span>
17. <span data-ttu-id="555d6-137">[追加] をクリックしてドロップ ダイアログを開きます。</span><span class="sxs-lookup"><span data-stu-id="555d6-137">Click Add to open the drop dialog.</span></span>
18. <span data-ttu-id="555d6-138">一覧で、入力した基準と一致した場合に使用する詳細ルール構造を検索します。</span><span class="sxs-lookup"><span data-stu-id="555d6-138">In the list, find the advanced rule structure you want to use when the criteria you entered is met.</span></span>
19. <span data-ttu-id="555d6-139">[追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="555d6-139">Click Add.</span></span>
20. <span data-ttu-id="555d6-140">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="555d6-140">Close the page.</span></span>
21. <span data-ttu-id="555d6-141">[有効化] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="555d6-141">Click Activate.</span></span>
22. <span data-ttu-id="555d6-142">[有効化] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="555d6-142">Click Activate.</span></span>


