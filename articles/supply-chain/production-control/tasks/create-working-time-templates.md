--- 
title: "作業時間テンプレートの作成"
description: "作業時間テンプレートは、週の中の勤務時間の定義や、ある期間の作業時間の生成に使用されます。"
author: sorenva
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: OpResLifeCycleManagementWorkspace, WorkTimeTable, WorkTimeCopyDayDialog
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: sorenand
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: 46c1e871133b51105386ac3b647432d0c36a6998
ms.contentlocale: ja-jp
ms.lasthandoff: 09/14/2018

---
# <a name="create-working-time-templates"></a><span data-ttu-id="9eb4e-103">作業時間テンプレートの作成</span><span class="sxs-lookup"><span data-stu-id="9eb4e-103">Create working time templates</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="9eb4e-104">作業時間テンプレートは、週の中の勤務時間の定義や、ある期間の作業時間の生成に使用されます。</span><span class="sxs-lookup"><span data-stu-id="9eb4e-104">Working time templates define the working hours throughout a week and are used to generate working times for a period of time.</span></span> <span data-ttu-id="9eb4e-105">この手順は、作業時間の間隔を分類するための作業時間のスケジューリングのプロパティを使用して作業時間テンプレートを定義する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="9eb4e-105">This procedure shows you how to define a working time template using working time scheduling properties for categorizing working time intervals.</span></span> <span data-ttu-id="9eb4e-106">デモ データ会社 USMF または独自のデータを使用してこの手順の説明を見ることができます。</span><span class="sxs-lookup"><span data-stu-id="9eb4e-106">You can walk through this procedure in demo data company USMF, or using your own data.</span></span>

1. <span data-ttu-id="9eb4e-107">[すべてのワークスペース] > [リソース ライフサイクル管理] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="9eb4e-107">Go to All workspaces > Resource lifecycle management.</span></span>
2. <span data-ttu-id="9eb4e-108">[作業時間] テンプレートをクリックします。</span><span class="sxs-lookup"><span data-stu-id="9eb4e-108">Click Working time templates.</span></span>

## <a name="create-working-time-template"></a><span data-ttu-id="9eb4e-109">作業時間テンプレートの作成</span><span class="sxs-lookup"><span data-stu-id="9eb4e-109">Create working time template</span></span>
1. <span data-ttu-id="9eb4e-110">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="9eb4e-110">Click New.</span></span>
2. <span data-ttu-id="9eb4e-111">[作業時間テンプレート] フィールドで、値を入力します。</span><span class="sxs-lookup"><span data-stu-id="9eb4e-111">In the Working time template field, type a value.</span></span>
3. <span data-ttu-id="9eb4e-112">[名前] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="9eb4e-112">In the Name field, type a value.</span></span>
4. <span data-ttu-id="9eb4e-113">[月曜日] セクションを展開します。</span><span class="sxs-lookup"><span data-stu-id="9eb4e-113">Expand the Monday section.</span></span>
5. <span data-ttu-id="9eb4e-114">[追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="9eb4e-114">Click Add.</span></span>
6. <span data-ttu-id="9eb4e-115">[ソース] フィールドに時刻を入力します。</span><span class="sxs-lookup"><span data-stu-id="9eb4e-115">In the From field, enter a time.</span></span>
    * <span data-ttu-id="9eb4e-116">午前の作業開始時間を指定します。</span><span class="sxs-lookup"><span data-stu-id="9eb4e-116">Specify the time when work begins in the morning.</span></span>  
7. <span data-ttu-id="9eb4e-117">[ターゲット] フィールドに時刻を入力します。</span><span class="sxs-lookup"><span data-stu-id="9eb4e-117">In the To field, enter a time.</span></span>
    * <span data-ttu-id="9eb4e-118">作業者の昼休みの時間を指定します。</span><span class="sxs-lookup"><span data-stu-id="9eb4e-118">Specify the time when workers break for lunch.</span></span>  
8. <span data-ttu-id="9eb4e-119">[追加] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="9eb4e-119">Click Add.</span></span>
9. <span data-ttu-id="9eb4e-120">[ソース] フィールドに時刻を入力します。</span><span class="sxs-lookup"><span data-stu-id="9eb4e-120">In the From field, enter a time.</span></span>
    * <span data-ttu-id="9eb4e-121">作業が昼食後に再開する時間を指定します。</span><span class="sxs-lookup"><span data-stu-id="9eb4e-121">Specify the time when work resumes after lunch.</span></span>  
10. <span data-ttu-id="9eb4e-122">[ターゲット] フィールドに時刻を入力します。</span><span class="sxs-lookup"><span data-stu-id="9eb4e-122">In the To field, enter a time.</span></span>
    * <span data-ttu-id="9eb4e-123">作業日の終了を指定します。</span><span class="sxs-lookup"><span data-stu-id="9eb4e-123">Specify the end of the work day.</span></span>  

## <a name="replicate-working-times-to-all-week-days"></a><span data-ttu-id="9eb4e-124">作業時間を平日すべてに複製</span><span class="sxs-lookup"><span data-stu-id="9eb4e-124">Replicate working times to all week days</span></span>
1. <span data-ttu-id="9eb4e-125">[日数のコピー] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="9eb4e-125">Click Copy day.</span></span>
    * <span data-ttu-id="9eb4e-126">月曜日から火曜日まで勤務時間の定義をコピーします。</span><span class="sxs-lookup"><span data-stu-id="9eb4e-126">Copy the working times definitions from Monday to Tuesday.</span></span>  
2. <span data-ttu-id="9eb4e-127">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="9eb4e-127">Click OK.</span></span>
3. <span data-ttu-id="9eb4e-128">[日数のコピー] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="9eb4e-128">Click Copy day.</span></span>
    * <span data-ttu-id="9eb4e-129">月曜日から水曜日まで勤務時間の定義をコピーします。</span><span class="sxs-lookup"><span data-stu-id="9eb4e-129">Copy the working times definitions from Monday to Wednesday.</span></span>  
4. <span data-ttu-id="9eb4e-130">[終了日] フィールドで、オプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="9eb4e-130">In the To weekday field, select an option.</span></span>
5. <span data-ttu-id="9eb4e-131">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="9eb4e-131">Click OK.</span></span>
6. <span data-ttu-id="9eb4e-132">[日数のコピー] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="9eb4e-132">Click Copy day.</span></span>
    * <span data-ttu-id="9eb4e-133">月曜日から木曜日まで勤務時間の定義をコピーします。</span><span class="sxs-lookup"><span data-stu-id="9eb4e-133">Copy the working times definitions from Monday to Thursday.</span></span>  
7. <span data-ttu-id="9eb4e-134">[終了日] フィールドで、オプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="9eb4e-134">In the To weekday field, select an option.</span></span>
8. <span data-ttu-id="9eb4e-135">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="9eb4e-135">Click OK.</span></span>
9. <span data-ttu-id="9eb4e-136">[日数のコピー] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="9eb4e-136">Click Copy day.</span></span>
    * <span data-ttu-id="9eb4e-137">月曜日から金曜日まで勤務時間の定義をコピーします。</span><span class="sxs-lookup"><span data-stu-id="9eb4e-137">Copy the working times definitions from Monday to Friday.</span></span>  
10. <span data-ttu-id="9eb4e-138">[終了日] フィールドで、オプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="9eb4e-138">In the To weekday field, select an option.</span></span>
11. <span data-ttu-id="9eb4e-139">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="9eb4e-139">Click OK.</span></span>

## <a name="define-time-slots-for-special-operations"></a><span data-ttu-id="9eb4e-140">特別工程のタイム スロットを定義</span><span class="sxs-lookup"><span data-stu-id="9eb4e-140">Define time slots for special operations</span></span>
1. <span data-ttu-id="9eb4e-141">[金曜日] セクションを展開します。</span><span class="sxs-lookup"><span data-stu-id="9eb4e-141">Expand the Friday section.</span></span>
2. <span data-ttu-id="9eb4e-142">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="9eb4e-142">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="9eb4e-143">[プロパティ] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="9eb4e-143">In the Property field, enter or select a value.</span></span>
4. <span data-ttu-id="9eb4e-144">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="9eb4e-144">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="9eb4e-145">[プロパティ] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="9eb4e-145">In the Property field, enter or select a value.</span></span>

## <a name="mark-weekend-days-as-closed-for-pickup"></a><span data-ttu-id="9eb4e-146">週末日を払出不可としてマーク</span><span class="sxs-lookup"><span data-stu-id="9eb4e-146">Mark weekend days as closed for pickup</span></span>
1. <span data-ttu-id="9eb4e-147">[土曜日] セクションを展開します。</span><span class="sxs-lookup"><span data-stu-id="9eb4e-147">Expand the Saturday section.</span></span>
2. <span data-ttu-id="9eb4e-148">[払出不可] フィールドで [はい] を選択します。</span><span class="sxs-lookup"><span data-stu-id="9eb4e-148">Select Yes in the Closed for pickup field.</span></span>
3. <span data-ttu-id="9eb4e-149">[日曜日] セクションを展開します。</span><span class="sxs-lookup"><span data-stu-id="9eb4e-149">Expand the Sunday section.</span></span>
4. <span data-ttu-id="9eb4e-150">[払出不可] フィールドで [はい] を選択します。</span><span class="sxs-lookup"><span data-stu-id="9eb4e-150">Select Yes in the Closed for pickup field.</span></span>


