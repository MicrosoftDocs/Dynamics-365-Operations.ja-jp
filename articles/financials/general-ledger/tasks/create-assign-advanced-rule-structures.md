---
title: 詳細ルール構造の作成と割り当て
description: このタスク ガイドでは、詳細ルール構造の作成と勘定構造への割り当てについて説明します。
author: aprilolson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DimensionConfigureAccountRuleStructure, DimensionCreateAccountRuleStructure, DimensionHierarchyAddLevel, DimensionHierarchyConstraintActivate, DimensionConfigureAccountStructure, DimensionConfigureAccountRule, DimensionCreateAccountRule, DimensionSelectAccountRuleStructure
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: dd62254c20cf5d77677d03c7d7335fb793d7f5f2
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/15/2019
ms.locfileid: "1558909"
---
# <a name="create-and-assign-advanced-rule-structures"></a><span data-ttu-id="be8d4-103">詳細ルール構造の作成と割り当て</span><span class="sxs-lookup"><span data-stu-id="be8d4-103">Create and assign advanced rule structures</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="be8d4-104">このタスク ガイドでは、詳細ルール構造の作成と勘定構造への割り当てについて説明します。</span><span class="sxs-lookup"><span data-stu-id="be8d4-104">This task guide steps through creating and assigning an advanced rule structure to an account structure.</span></span> <span data-ttu-id="be8d4-105">このガイドでは、USMF デモ会社を使用します。</span><span class="sxs-lookup"><span data-stu-id="be8d4-105">This guide uses the USMF demo company.</span></span>


## <a name="create-an-advanced-rule-structure"></a><span data-ttu-id="be8d4-106">詳細なルール構造の作成</span><span class="sxs-lookup"><span data-stu-id="be8d4-106">Create an advanced rule structure</span></span>
1. <span data-ttu-id="be8d4-107">[総勘定元帳] > [勘定科目表] > [構造] > [詳細ルール構造] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="be8d4-107">Go to General ledger > Chart of accounts > Structures > Advanced rule structures.</span></span>
2. <span data-ttu-id="be8d4-108">[新規] をクリックすると、ドロップ ダイアログが開きます。</span><span class="sxs-lookup"><span data-stu-id="be8d4-108">Click New to open the drop dialog.</span></span>
3. <span data-ttu-id="be8d4-109">[詳細ルール構造] フィールドにルール構造を説明する名前を入力します。</span><span class="sxs-lookup"><span data-stu-id="be8d4-109">In the Advanced rule structure field, type a name to descritbe the rule structure.</span></span>
4. <span data-ttu-id="be8d4-110">[説明] フィールドに構造を説明する値を入力します。</span><span class="sxs-lookup"><span data-stu-id="be8d4-110">In the Description field, type a value to describe the structure.</span></span>
5. <span data-ttu-id="be8d4-111">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="be8d4-111">Click OK.</span></span>
6. <span data-ttu-id="be8d4-112">[区分の追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="be8d4-112">Click Add segment.</span></span>
7. <span data-ttu-id="be8d4-113">区分リストで、財務分析コードを選択します。</span><span class="sxs-lookup"><span data-stu-id="be8d4-113">In the list of segments, select a financial dimension.</span></span>
    * <span data-ttu-id="be8d4-114">たとえば [店舗] です。</span><span class="sxs-lookup"><span data-stu-id="be8d4-114">For example, Store.</span></span>  
8. <span data-ttu-id="be8d4-115">[区分の追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="be8d4-115">Click Add segment.</span></span>
9. <span data-ttu-id="be8d4-116">一覧で、詳細ルール構造を表示するリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="be8d4-116">In the list, click the link of the advanced rule structure to view it.</span></span>
10. <span data-ttu-id="be8d4-117">[有効化] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="be8d4-117">Click Activate.</span></span>
11. <span data-ttu-id="be8d4-118">[有効化] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="be8d4-118">Click Activate.</span></span>

## <a name="apply-an-advanced-rule-structure-to-an-account-structure"></a><span data-ttu-id="be8d4-119">詳細ルール構造の勘定構造への適用</span><span class="sxs-lookup"><span data-stu-id="be8d4-119">Apply an advanced rule structure to an account structure</span></span>
1. <span data-ttu-id="be8d4-120">フォームを閉じます。</span><span class="sxs-lookup"><span data-stu-id="be8d4-120">Close the form.</span></span>
2. <span data-ttu-id="be8d4-121">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="be8d4-121">Close the page.</span></span>
3. <span data-ttu-id="be8d4-122">[総勘定元帳] > [勘定科目表] > [構造] > [勘定構造のコンフィギュレーション] に移動します。</span><span class="sxs-lookup"><span data-stu-id="be8d4-122">Go to General ledger > Chart of accounts > Structures > Configure account structures.</span></span>
4. <span data-ttu-id="be8d4-123">一覧で、詳細ルールを適用する勘定構造を検索し選択します。</span><span class="sxs-lookup"><span data-stu-id="be8d4-123">In the list, find and select the account structure you want to apply the advanced rule to.</span></span>
5. <span data-ttu-id="be8d4-124">勘定構造の名前をクリックして開きます。</span><span class="sxs-lookup"><span data-stu-id="be8d4-124">Click the name of the account structure to open it.</span></span>
6. <span data-ttu-id="be8d4-125">[編集] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="be8d4-125">Click Edit.</span></span>
    * <span data-ttu-id="be8d4-126">[詳細ルール] をクリックすると、勘定構造を [ドラフト モード] に設定するよう要求されます。</span><span class="sxs-lookup"><span data-stu-id="be8d4-126">You can also click Advanced rules and you will be prompted to put the account structure in Draft mode.</span></span>  
7. <span data-ttu-id="be8d4-127">[詳細ルール] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="be8d4-127">Click Advanced rules.</span></span>
8. <span data-ttu-id="be8d4-128">[新規] をクリックすると、ドロップ ダイアログが開きます。</span><span class="sxs-lookup"><span data-stu-id="be8d4-128">Click New to open the drop dialog.</span></span>
9. <span data-ttu-id="be8d4-129">[詳細ルール] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="be8d4-129">In the Advanced rule field, type a value.</span></span>
10. <span data-ttu-id="be8d4-130">[名前] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="be8d4-130">In the Name field, type a value.</span></span>
11. <span data-ttu-id="be8d4-131">[作成] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="be8d4-131">Click Create.</span></span>
12. <span data-ttu-id="be8d4-132">[新しい基準の追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="be8d4-132">Click Add new criteria.</span></span>
13. <span data-ttu-id="be8d4-133">[適用箇所] フィールドで、主勘定または財務分析コードを選択します。</span><span class="sxs-lookup"><span data-stu-id="be8d4-133">In the Where field, select main account or a financial dimension.</span></span>
14. <span data-ttu-id="be8d4-134">[演算子] フィールドで、「is between」や「includes」などのオプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="be8d4-134">In the Operator field, select an option, such as is between and includes.</span></span>
15. <span data-ttu-id="be8d4-135">[値] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="be8d4-135">In the Value field, type a value.</span></span>
16. <span data-ttu-id="be8d4-136">[終了日] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="be8d4-136">In the through field, type a value.</span></span>
17. <span data-ttu-id="be8d4-137">[追加] をクリックしてドロップ ダイアログを開きます。</span><span class="sxs-lookup"><span data-stu-id="be8d4-137">Click Add to open the drop dialog.</span></span>
18. <span data-ttu-id="be8d4-138">一覧で、入力した基準と一致した場合に使用する詳細ルール構造を検索します。</span><span class="sxs-lookup"><span data-stu-id="be8d4-138">In the list, find the advanced rule structure you want to use when the criteria you entered is met.</span></span>
19. <span data-ttu-id="be8d4-139">[追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="be8d4-139">Click Add.</span></span>
20. <span data-ttu-id="be8d4-140">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="be8d4-140">Close the page.</span></span>
21. <span data-ttu-id="be8d4-141">[有効化] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="be8d4-141">Click Activate.</span></span>
22. <span data-ttu-id="be8d4-142">[有効化] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="be8d4-142">Click Activate.</span></span>

