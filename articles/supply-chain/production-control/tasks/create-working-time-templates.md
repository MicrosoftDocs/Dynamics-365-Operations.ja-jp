---
title: 作業時間テンプレートの作成
description: 作業時間テンプレートは、週の中の勤務時間の定義や、ある期間の作業時間の生成に使用されます。
author: sorenva
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: OpResLifeCycleManagementWorkspace, WorkTimeTable, WorkTimeCopyDayDialog, WorkPeriodTemplate
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: sorenand
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ed1981b7c1427c902f237f0aa95f63e89bc345ab
ms.sourcegitcommit: fa99a36c3d30d0c0577fd3f63ed6bf2f71599e40
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/20/2021
ms.locfileid: "5920932"
---
# <a name="create-working-time-templates"></a><span data-ttu-id="51f92-103">作業時間テンプレートの作成</span><span class="sxs-lookup"><span data-stu-id="51f92-103">Create working time templates</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="51f92-104">作業時間テンプレートは、週の中の勤務時間の定義や、ある期間の作業時間の生成に使用されます。</span><span class="sxs-lookup"><span data-stu-id="51f92-104">Working time templates define the working hours throughout a week and are used to generate working times for a period of time.</span></span> <span data-ttu-id="51f92-105">この手順は、作業時間の間隔を分類するための作業時間のスケジューリングのプロパティを使用して作業時間テンプレートを定義する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="51f92-105">This procedure shows you how to define a working time template using working time scheduling properties for categorizing working time intervals.</span></span> <span data-ttu-id="51f92-106">デモ データ会社 USMF または独自のデータを使用してこの手順の説明を見ることができます。</span><span class="sxs-lookup"><span data-stu-id="51f92-106">You can walk through this procedure in demo data company USMF, or using your own data.</span></span>

1. <span data-ttu-id="51f92-107">**ワークスペース > リソース ライフサイクル管理** の順にクリックします。</span><span class="sxs-lookup"><span data-stu-id="51f92-107">Go to **Workspaces > Resource lifecycle management**.</span></span>
1. <span data-ttu-id="51f92-108">**作業時間テンプレート** を選択します。</span><span class="sxs-lookup"><span data-stu-id="51f92-108">Select **Working time templates**.</span></span>

## <a name="create-working-time-template"></a><span data-ttu-id="51f92-109">作業時間テンプレートの作成</span><span class="sxs-lookup"><span data-stu-id="51f92-109">Create working time template</span></span>

1. <span data-ttu-id="51f92-110">**新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="51f92-110">Select **New**.</span></span>
1. <span data-ttu-id="51f92-111">**作業時間テンプレート** フィールドで、値を入力します。</span><span class="sxs-lookup"><span data-stu-id="51f92-111">In the **Working time template** field, type a value.</span></span>
1. <span data-ttu-id="51f92-112">**名前** フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="51f92-112">In the **Name** field, type a value.</span></span>
1. <span data-ttu-id="51f92-113">**月曜日** セクションを展開します。</span><span class="sxs-lookup"><span data-stu-id="51f92-113">Expand the **Monday** section.</span></span>
1. <span data-ttu-id="51f92-114">**追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="51f92-114">Select **Add**.</span></span>
1. <span data-ttu-id="51f92-115">**ソース** フィールドに時刻を入力します。</span><span class="sxs-lookup"><span data-stu-id="51f92-115">In the **From** field, enter a time.</span></span>
    * <span data-ttu-id="51f92-116">午前の作業開始時間を指定します。</span><span class="sxs-lookup"><span data-stu-id="51f92-116">Specify the time when work begins in the morning.</span></span>  
1. <span data-ttu-id="51f92-117">**ターゲット** フィールドに時刻を入力します。</span><span class="sxs-lookup"><span data-stu-id="51f92-117">In the **To** field, enter a time.</span></span>
    * <span data-ttu-id="51f92-118">作業者の昼休みの時間を指定します。</span><span class="sxs-lookup"><span data-stu-id="51f92-118">Specify the time when workers break for lunch.</span></span>  
1. <span data-ttu-id="51f92-119">**追加** を選択します。</span><span class="sxs-lookup"><span data-stu-id="51f92-119">Select **Add**.</span></span>
1. <span data-ttu-id="51f92-120">**ソース** フィールドに時刻を入力します。</span><span class="sxs-lookup"><span data-stu-id="51f92-120">In the **From** field, enter a time.</span></span>
    * <span data-ttu-id="51f92-121">作業が昼食後に再開する時間を指定します。</span><span class="sxs-lookup"><span data-stu-id="51f92-121">Specify the time when work resumes after lunch.</span></span>  
1. <span data-ttu-id="51f92-122">**ターゲット** フィールドに時刻を入力します。</span><span class="sxs-lookup"><span data-stu-id="51f92-122">In the **To** field, enter a time.</span></span>
    * <span data-ttu-id="51f92-123">作業日の終了を指定します。</span><span class="sxs-lookup"><span data-stu-id="51f92-123">Specify the end of the work day.</span></span>  

## <a name="replicate-working-times-to-all-week-days"></a><span data-ttu-id="51f92-124">作業時間を平日すべてに複製</span><span class="sxs-lookup"><span data-stu-id="51f92-124">Replicate working times to all week days</span></span>

1. <span data-ttu-id="51f92-125">**日数のコピー** を選択します。</span><span class="sxs-lookup"><span data-stu-id="51f92-125">Select **Copy day**.</span></span>
    * <span data-ttu-id="51f92-126">月曜日から火曜日まで勤務時間の定義をコピーします。</span><span class="sxs-lookup"><span data-stu-id="51f92-126">Copy the working times definitions from Monday to Tuesday.</span></span>  
1. <span data-ttu-id="51f92-127">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="51f92-127">Select **OK**.</span></span>
1. <span data-ttu-id="51f92-128">**日数のコピー** を選択します。</span><span class="sxs-lookup"><span data-stu-id="51f92-128">Select **Copy day**.</span></span>
    * <span data-ttu-id="51f92-129">月曜日から水曜日まで勤務時間の定義をコピーします。</span><span class="sxs-lookup"><span data-stu-id="51f92-129">Copy the working times definitions from Monday to Wednesday.</span></span>  
1. <span data-ttu-id="51f92-130">**終了日** フィールドで、オプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="51f92-130">In the **To weekday** field, select an option.</span></span>
1. <span data-ttu-id="51f92-131">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="51f92-131">Select **OK**.</span></span>
1. <span data-ttu-id="51f92-132">**日数のコピー** を選択します。</span><span class="sxs-lookup"><span data-stu-id="51f92-132">Select **Copy day**.</span></span>
    * <span data-ttu-id="51f92-133">月曜日から木曜日まで勤務時間の定義をコピーします。</span><span class="sxs-lookup"><span data-stu-id="51f92-133">Copy the working times definitions from Monday to Thursday.</span></span>  
1. <span data-ttu-id="51f92-134">**終了日** フィールドで、オプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="51f92-134">In the **To weekday** field, select an option.</span></span>
1. <span data-ttu-id="51f92-135">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="51f92-135">Select **OK**.</span></span>
1. <span data-ttu-id="51f92-136">**日数のコピー** を選択します。</span><span class="sxs-lookup"><span data-stu-id="51f92-136">Select **Copy day**.</span></span>
    * <span data-ttu-id="51f92-137">月曜日から金曜日まで勤務時間の定義をコピーします。</span><span class="sxs-lookup"><span data-stu-id="51f92-137">Copy the working times definitions from Monday to Friday.</span></span>  
1. <span data-ttu-id="51f92-138">**終了日** フィールドで、オプションを選択します。</span><span class="sxs-lookup"><span data-stu-id="51f92-138">In the **To weekday** field, select an option.</span></span>
1. <span data-ttu-id="51f92-139">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="51f92-139">Select **OK**.</span></span>

## <a name="define-time-slots-for-special-operations"></a><span data-ttu-id="51f92-140">特別工程のタイム スロットを定義</span><span class="sxs-lookup"><span data-stu-id="51f92-140">Define time slots for special operations</span></span>

1. <span data-ttu-id="51f92-141">**金曜日** セクションを展開します。</span><span class="sxs-lookup"><span data-stu-id="51f92-141">Expand the **Friday** section.</span></span>
1. <span data-ttu-id="51f92-142">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="51f92-142">In the list, find and select the desired record.</span></span>
1. <span data-ttu-id="51f92-143">**プロパティ** フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="51f92-143">In the **Property** field, enter or select a value.</span></span>
1. <span data-ttu-id="51f92-144">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="51f92-144">In the list, find and select the desired record.</span></span>
1. <span data-ttu-id="51f92-145">**プロパティ** フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="51f92-145">In the **Property** field, enter or select a value.</span></span>

## <a name="mark-weekend-days-as-closed-for-pickup"></a><span data-ttu-id="51f92-146">週末日を払出不可としてマーク</span><span class="sxs-lookup"><span data-stu-id="51f92-146">Mark weekend days as closed for pickup</span></span>

1. <span data-ttu-id="51f92-147">**土曜日** セクションを展開します。</span><span class="sxs-lookup"><span data-stu-id="51f92-147">Expand the **Saturday** section.</span></span>
1. <span data-ttu-id="51f92-148">**払出不可** フィールドで、*はい* を選択します。</span><span class="sxs-lookup"><span data-stu-id="51f92-148">Select *Yes* in the **Closed for pickup** field.</span></span>
1. <span data-ttu-id="51f92-149">**日曜日** セクションを展開します。</span><span class="sxs-lookup"><span data-stu-id="51f92-149">Expand the **Sunday** section.</span></span>
1. <span data-ttu-id="51f92-150">**払出不可** フィールドで、*はい* を選択します。</span><span class="sxs-lookup"><span data-stu-id="51f92-150">Select *Yes* in the **Closed for pickup** field.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]