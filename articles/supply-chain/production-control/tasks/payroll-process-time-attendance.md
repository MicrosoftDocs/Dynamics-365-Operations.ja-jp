---
title: "時刻と出勤の給与プロセスの有効化"
description: "この手順は、時刻と出勤の給与プロセスを有効にする方法を示します。"
author: johanhoffmann
manager: AnnBe
ms.date: 02/12/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 020bcb71d9b8495e61f3cf83c073771d6f2b2f26
ms.contentlocale: ja-jp
ms.lasthandoff: 04/13/2018

---
# <a name="enable-the-payroll-process-for-time-and-attendance"></a><span data-ttu-id="c475f-103">時刻と出勤の給与プロセスの有効化</span><span class="sxs-lookup"><span data-stu-id="c475f-103">Enable the payroll process for time and attendance</span></span>

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="c475f-104">この手順は、時刻と出勤の給与プロセスを有効にする方法を示します。</span><span class="sxs-lookup"><span data-stu-id="c475f-104">This procedure shows how to enable the payroll process for time and attendance.</span></span> <span data-ttu-id="c475f-105">この手順の作成に使用するデモ データの会社は USMF です。</span><span class="sxs-lookup"><span data-stu-id="c475f-105">The demo data company used to create this procedure is USMF.</span></span>


## <a name="create-a-pay-type-with-a-related-pay-rate"></a><span data-ttu-id="c475f-106">関連する支払レートを使用して新しい支払タイプを作成する</span><span class="sxs-lookup"><span data-stu-id="c475f-106">Create a pay type with a related pay rate</span></span>
1. <span data-ttu-id="c475f-107">[時刻と出勤] > [設定] > [給与] > [支払タイプ]</span><span class="sxs-lookup"><span data-stu-id="c475f-107">Time and attendance > Setup > Payroll > Pay types</span></span>
2. <span data-ttu-id="c475f-108">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="c475f-108">Click New.</span></span>
3. <span data-ttu-id="c475f-109">[支払タイプ] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="c475f-109">In the Pay type field, type a value.</span></span>
4. <span data-ttu-id="c475f-110">[説明] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="c475f-110">In the Description field, type a value.</span></span>
5. <span data-ttu-id="c475f-111">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="c475f-111">Click Save.</span></span>
6. <span data-ttu-id="c475f-112">[レート] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="c475f-112">Click Rates.</span></span>
    * <span data-ttu-id="c475f-113">支払タイプのレートは、特定の時間間隔に対して設定され、個々のレートを従業員に対して指定できます。</span><span class="sxs-lookup"><span data-stu-id="c475f-113">Rates for pay types are set up for specific time intervals, and individual rates can be created for workers.</span></span> <span data-ttu-id="c475f-114">時間と出勤の支払タイプのレートを必ず作成する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="c475f-114">It is not always necessary to create rates for pay types in time and attendance.</span></span> <span data-ttu-id="c475f-115">この情報は、すでに従業員の給与を生成するときに使用される給与システムに存在する場合があります。</span><span class="sxs-lookup"><span data-stu-id="c475f-115">This information may already exist in the payroll system that is used to generate wages.</span></span>  
7. <span data-ttu-id="c475f-116">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="c475f-116">Click New.</span></span>
8. <span data-ttu-id="c475f-117">一覧で、選択された行をマークします。</span><span class="sxs-lookup"><span data-stu-id="c475f-117">In the list, mark the selected row.</span></span>
9. <span data-ttu-id="c475f-118">[レート] フィールドに数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="c475f-118">In the Rate field, enter a number.</span></span>
10. <span data-ttu-id="c475f-119">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="c475f-119">Click Save.</span></span>

## <a name="create-a-pay-agreement"></a><span data-ttu-id="c475f-120">支払協定の作成</span><span class="sxs-lookup"><span data-stu-id="c475f-120">Create a pay agreement</span></span>
1. <span data-ttu-id="c475f-121">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="c475f-121">Close the page.</span></span>
2. <span data-ttu-id="c475f-122">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="c475f-122">Close the page.</span></span>
3. <span data-ttu-id="c475f-123">[支払協定] に移動します。</span><span class="sxs-lookup"><span data-stu-id="c475f-123">Go to Pay agreements.</span></span>
    * <span data-ttu-id="c475f-124">[時刻と出勤] > [設定] > [支払協定]</span><span class="sxs-lookup"><span data-stu-id="c475f-124">Time and attendance > Setup > Pay agreements</span></span>  
4. <span data-ttu-id="c475f-125">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="c475f-125">Click New.</span></span>
5. <span data-ttu-id="c475f-126">[支払協定] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="c475f-126">In the Pay agreement field, type a value.</span></span>
6. <span data-ttu-id="c475f-127">[説明] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="c475f-127">In the Description field, type a value.</span></span>
7. <span data-ttu-id="c475f-128">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="c475f-128">Click Save.</span></span>
8. <span data-ttu-id="c475f-129">[契約明細行] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="c475f-129">Click Agreement lines.</span></span>
9. <span data-ttu-id="c475f-130">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="c475f-130">Click New.</span></span>
10. <span data-ttu-id="c475f-131">一覧で、選択された行をマークします。</span><span class="sxs-lookup"><span data-stu-id="c475f-131">In the list, mark the selected row.</span></span>
11. <span data-ttu-id="c475f-132">[プロファイル タイプ] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="c475f-132">In the Profile type field, enter or select a value.</span></span>
12. <span data-ttu-id="c475f-133">[支払タイプ] フィールドで値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="c475f-133">In the Pay type field, enter or select a value.</span></span>

## <a name="set-up-pay-agreement-for-time-and-registration-worker"></a><span data-ttu-id="c475f-134">時間登録作業者の支払協定を設定する</span><span class="sxs-lookup"><span data-stu-id="c475f-134">Set up pay agreement for time and registration worker</span></span>
1. <span data-ttu-id="c475f-135">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="c475f-135">Close the page.</span></span>
2. <span data-ttu-id="c475f-136">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="c475f-136">Close the page.</span></span>
3. <span data-ttu-id="c475f-137">[時間登録作業者] に移動します。</span><span class="sxs-lookup"><span data-stu-id="c475f-137">Go to Time registration workers.</span></span>
    * <span data-ttu-id="c475f-138">[時刻と出勤] > [設定] > [時間登録作業者]</span><span class="sxs-lookup"><span data-stu-id="c475f-138">Time and attendance > Setup > Time registration workers</span></span>  
4. <span data-ttu-id="c475f-139">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="c475f-139">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="c475f-140">[雇用] タブをクリックします。</span><span class="sxs-lookup"><span data-stu-id="c475f-140">Click the Employment tab.</span></span>
6. <span data-ttu-id="c475f-141">[時間登録] セクションを展開します。</span><span class="sxs-lookup"><span data-stu-id="c475f-141">Expand the Time registration section.</span></span>
7. <span data-ttu-id="c475f-142">[編集] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="c475f-142">Click Edit.</span></span>
8. <span data-ttu-id="c475f-143">[支払協定] フィールドで値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="c475f-143">In the Pay agreement field, enter or select a value.</span></span>

