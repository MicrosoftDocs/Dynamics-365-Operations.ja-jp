---
title: 作業時間カレンダーの作成
description: Dynamics 365 Human Resources で、作業時間カレンダー、休日、および非作業時間を定義します。
author: andreabichsel
manager: AnnBe
ms.date: 04/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: dc209b62836011b18362f78b63cdd3fcda884dc3
ms.sourcegitcommit: 79f8aa2c0b166a423db9b8503da53e96e3fc43dc
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/01/2020
ms.locfileid: "3198030"
---
# <a name="create-a-working-time-calendar"></a><span data-ttu-id="0071e-103">作業時間カレンダーの作成</span><span class="sxs-lookup"><span data-stu-id="0071e-103">Create a working time calendar</span></span>

<span data-ttu-id="0071e-104">Dynamics 365 Human Resources で、作業時間カレンダーには、組織内で従業員が勤務している日数と時間が表示されます。</span><span class="sxs-lookup"><span data-stu-id="0071e-104">A working time calendar in Dynamics 365 Human Resources shows the days and hours that employees work in your organization.</span></span> <span data-ttu-id="0071e-105">従業員が休暇申請を提出した場合、休日や休業日を気にする必要はありません。</span><span class="sxs-lookup"><span data-stu-id="0071e-105">When an employee submits a time-off request, they don't have to worry about holidays and closures.</span></span>

<span data-ttu-id="0071e-106">休暇申請を効率化するには、組織に対して次の項目を構成します。</span><span class="sxs-lookup"><span data-stu-id="0071e-106">To streamline time-off requests, configure these items for your organization:</span></span>

- <span data-ttu-id="0071e-107">作業時間カレンダー</span><span class="sxs-lookup"><span data-stu-id="0071e-107">Working time calendar</span></span>
- <span data-ttu-id="0071e-108">休日および休業日</span><span class="sxs-lookup"><span data-stu-id="0071e-108">Holidays and closures</span></span>
- <span data-ttu-id="0071e-109">非作業時間</span><span class="sxs-lookup"><span data-stu-id="0071e-109">Non-work time</span></span>

<span data-ttu-id="0071e-110">最後の 2 つの項目は、作業時間カレンダーを設定している間に追加できます。</span><span class="sxs-lookup"><span data-stu-id="0071e-110">You can add the last two items while you're setting up a working time calendar.</span></span> <span data-ttu-id="0071e-111">個別に構成または更新を行うこともできます。</span><span class="sxs-lookup"><span data-stu-id="0071e-111">You can also configure or update them separately.</span></span>

## <a name="set-up-a-working-time-calendar"></a><span data-ttu-id="0071e-112">作業時間カレンダーの設定</span><span class="sxs-lookup"><span data-stu-id="0071e-112">Set up a working time calendar</span></span>

<span data-ttu-id="0071e-113">作業日数と時間を示す、少なくとも 1 つの作業時間カレンダーを設定します。</span><span class="sxs-lookup"><span data-stu-id="0071e-113">Set up at least one working time calendar that shows your days and hours of operation.</span></span> <span data-ttu-id="0071e-114">複数の国や地域に拠点がある場合は、それぞれの拠点に対して作業時間カレンダーを設定することもできます。</span><span class="sxs-lookup"><span data-stu-id="0071e-114">If you have locations in multiple countries and regions, you might want to set up a working time calendar for each area.</span></span>

1. <span data-ttu-id="0071e-115">**組織管理**ページで、**カレンダー**を選択します。</span><span class="sxs-lookup"><span data-stu-id="0071e-115">On the **Organization administration** page, select **Calendars**.</span></span>

2. <span data-ttu-id="0071e-116">**新規**を選択し、カレンダーに名前と説明を入力します。</span><span class="sxs-lookup"><span data-stu-id="0071e-116">Select **New** and enter a name and description for your calendar.</span></span>

3. <span data-ttu-id="0071e-117">**生成オプション**で、組織の作業日数を選択し、作業時間を入力します。</span><span class="sxs-lookup"><span data-stu-id="0071e-117">Under **Generation options**, select the work days for your organization and enter work times.</span></span> 
   - <span data-ttu-id="0071e-118">休日または休業日を追加するには、**休日および休業日**の横にある**追加**ボタンを選択します。</span><span class="sxs-lookup"><span data-stu-id="0071e-118">To add a holiday or closure, select the **Add** button next to **Holidays and closures**.</span></span>
   - <span data-ttu-id="0071e-119">昼食や休憩などの非作業時間を追加するには、**非作業時間**で**追加**を選択し、名前と時間の範囲を入力します。</span><span class="sxs-lookup"><span data-stu-id="0071e-119">To add non-work time, like lunches or breaks, select **Add** under **NON-WORK TIME** and enter the name and time range.</span></span>

4. <span data-ttu-id="0071e-120">**日数**で、**生成**を選択して、カレンダーに日数を生成します。</span><span class="sxs-lookup"><span data-stu-id="0071e-120">Under **Days**, select **Generate** to generate the days in your calendar.</span></span> <span data-ttu-id="0071e-121">カレンダーに日付範囲を入力し、**日数の生成**を選択します。</span><span class="sxs-lookup"><span data-stu-id="0071e-121">Enter the date range for your calendar and then select **Generate days**.</span></span>

5. <span data-ttu-id="0071e-122">作業スケジュールを追加するには、**作業スケジュール**で、**追加**を選択し、各作業スケジュールに時刻を入力します。</span><span class="sxs-lookup"><span data-stu-id="0071e-122">To add work schedules, under **Work schedule**, select **Add** and then enter the times for each work schedule.</span></span>

## <a name="configure-holidays-and-closures"></a><span data-ttu-id="0071e-123">休日および休業日の構成</span><span class="sxs-lookup"><span data-stu-id="0071e-123">Configure holidays and closures</span></span>

<span data-ttu-id="0071e-124">休日および休業日は、作業時間カレンダーから個別に追加または変更できます。</span><span class="sxs-lookup"><span data-stu-id="0071e-124">You can add or change holidays and closures separately from a working time calendar.</span></span>

1. <span data-ttu-id="0071e-125">**組織管理**ページで、**休日および休業日**を選択します。</span><span class="sxs-lookup"><span data-stu-id="0071e-125">On the **Organization administration** page, select **Holidays and closures**.</span></span>

2. <span data-ttu-id="0071e-126">**新規** を選択し、休日および休業日に名前と日付を入力します。</span><span class="sxs-lookup"><span data-stu-id="0071e-126">Select **New** and enter a name and date for the holiday or closure.</span></span>

## <a name="configure-non-work-time"></a><span data-ttu-id="0071e-127">非作業時間の構成</span><span class="sxs-lookup"><span data-stu-id="0071e-127">Configure non-work time</span></span>

<span data-ttu-id="0071e-128">非作業時間は、作業時間カレンダーから個別に追加または変更できます。</span><span class="sxs-lookup"><span data-stu-id="0071e-128">You can add or change non-work times separately from a working time calendar.</span></span>

1. <span data-ttu-id="0071e-129">**組織管理**ページで、**非作業時間**を選択します。</span><span class="sxs-lookup"><span data-stu-id="0071e-129">On the **Organization administration** page, select **Non-work time**.</span></span>

2. <span data-ttu-id="0071e-130">**新規**を選択し、非作業時間に名前と時間範囲を入力します。</span><span class="sxs-lookup"><span data-stu-id="0071e-130">Select **New** and enter a name and time range for the non-work time.</span></span>

<span data-ttu-id="0071e-131">休暇および欠勤の休日の修正プレビュー機能を有効にした場合、Human Resources は休日と休業日を使用して、カレンダーに登録されている従業員に対して調整する日数を決定します。</span><span class="sxs-lookup"><span data-stu-id="0071e-131">If you've enabled the Leave and absence bank holiday corrections preview feature, Human Resources uses holidays and closure dates to determine the number of days to adjust for employees enrolled in the calendar.</span></span>

## <a name="see-also"></a><span data-ttu-id="0071e-132">参照</span><span class="sxs-lookup"><span data-stu-id="0071e-132">See also</span></span>

- [<span data-ttu-id="0071e-133">休暇の概要</span><span class="sxs-lookup"><span data-stu-id="0071e-133">Leave and absence overview</span></span>](hr-leave-and-absence-overview.md)
- [<span data-ttu-id="0071e-134">休暇タイプのコンフィギュレーション</span><span class="sxs-lookup"><span data-stu-id="0071e-134">Configure leave and absence types</span></span>](hr-leave-and-absence-types.md)
