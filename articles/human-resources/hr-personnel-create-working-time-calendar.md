---
title: カレンダーの作成および作業時間の生成
description: カレンダーは、運営リソースの能力と作業時間を説明します。 この記事は、作業時間テンプレートに基づいて作業カレンダーを定義する方法について説明します。
author: andreabichsel
ms.date: 07/09/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: OpResLifeCycleManagementWorkspace, WorkCalendarTable, WorkCalendarDate, HcmPersonnelManagementWorkspace, WrkCtrGroupDateCalendar, WrkCtrDateCalendar
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f28e11613cb9e10b258e1c373890505fb6e71d29
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/31/2021
ms.locfileid: "5804916"
---
# <a name="create-calendars-and-generate-working-times"></a><span data-ttu-id="1d315-104">カレンダーの作成および作業時間の生成</span><span class="sxs-lookup"><span data-stu-id="1d315-104">Create calendars and generate working times</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]



<span data-ttu-id="1d315-105">カレンダーは、運営リソースの能力と作業時間を説明します。</span><span class="sxs-lookup"><span data-stu-id="1d315-105">Calendars describe the capacity and working times of operations resources.</span></span> <span data-ttu-id="1d315-106">この記事は、作業時間テンプレートに基づいて作業カレンダーを定義する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="1d315-106">This article explains how to define a work calendar based on a working time template.</span></span> <span data-ttu-id="1d315-107">デモ データ会社 USMF または独自のデータを使用してこの手順の説明を見ることができます。</span><span class="sxs-lookup"><span data-stu-id="1d315-107">You can walk through this procedure in demo data company USMF, or using your own data.</span></span>

1. <span data-ttu-id="1d315-108">ホーム ページで、**リソース ライフサイクル管理** を選択します。</span><span class="sxs-lookup"><span data-stu-id="1d315-108">On the home page, select **Resource lifecycle management**.</span></span>
2. <span data-ttu-id="1d315-109">**カレンダー** を選択します。</span><span class="sxs-lookup"><span data-stu-id="1d315-109">Select **Calendars**.</span></span>
3. <span data-ttu-id="1d315-110">**新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="1d315-110">Select **New**.</span></span>
4. <span data-ttu-id="1d315-111">**カレンダー** フィールドで、カレンダーを分類します。</span><span class="sxs-lookup"><span data-stu-id="1d315-111">In the **Calendar** field, classify your calendar.</span></span> <span data-ttu-id="1d315-112">これは、運営リソースまたはリソース グループなどのカレンダーを割り当てるときに参照として使用されるカレンダーの ID です。</span><span class="sxs-lookup"><span data-stu-id="1d315-112">This is the ID of the calendar, which is used as a reference when assigning calendars, such as to an operations resource or a resource group.</span></span>  
5. <span data-ttu-id="1d315-113">**名前** フィールドで、カレンダーに名前を付けます。</span><span class="sxs-lookup"><span data-stu-id="1d315-113">In the **Name** field, name your calendar.</span></span>
6. <span data-ttu-id="1d315-114">**標準作業日 (時)** で、数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="1d315-114">In the **Standard work day in hours** field, enter a number.</span></span>
7. <span data-ttu-id="1d315-115">行が選択されていることを確認し、アクション ウィンドウから **作業時間** を選択します。</span><span class="sxs-lookup"><span data-stu-id="1d315-115">Make sure the row is selected, then select **Working times** from the Action Pane.</span></span>
8. <span data-ttu-id="1d315-116">**作業時間の作成** を選択します。</span><span class="sxs-lookup"><span data-stu-id="1d315-116">Select **Compose working times**.</span></span> <span data-ttu-id="1d315-117">作業をスケジュールできる期間のそれぞれの日の勤務時間を生成します。</span><span class="sxs-lookup"><span data-stu-id="1d315-117">Generate working hours for each day in the period where you want to be able to schedule work.</span></span> <span data-ttu-id="1d315-118">徐々に、その他の期間にも勤務時間生成することができるようになります。</span><span class="sxs-lookup"><span data-stu-id="1d315-118">As time goes by, you can generate working times for additional periods.</span></span>  
9. <span data-ttu-id="1d315-119">**開始日** フィールドに日付を入力します。</span><span class="sxs-lookup"><span data-stu-id="1d315-119">In the **From date** field, enter a date.</span></span> <span data-ttu-id="1d315-120">このカレンダーがオープンになっている必要がある最初の日です。</span><span class="sxs-lookup"><span data-stu-id="1d315-120">This is the first day that this calendar must be open.</span></span>  
10. <span data-ttu-id="1d315-121">**終了日** フィールドに日付を入力します。</span><span class="sxs-lookup"><span data-stu-id="1d315-121">In the **To date field**, enter a date.</span></span> <span data-ttu-id="1d315-122">このカレンダーがオープンになっている最後の日です。</span><span class="sxs-lookup"><span data-stu-id="1d315-122">This is the last day that this calendar is open.</span></span>  
11. <span data-ttu-id="1d315-123">**作業時間テンプレート** フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="1d315-123">In the **Working time template** field, enter or select a value.</span></span> <span data-ttu-id="1d315-124">作業時間テンプレートは曜日ごとの勤務時間を定義します。</span><span class="sxs-lookup"><span data-stu-id="1d315-124">The working time template defines the working hours for each day of the week.</span></span>  
12. <span data-ttu-id="1d315-125">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="1d315-125">Select **OK**.</span></span>
13. <span data-ttu-id="1d315-126">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="1d315-126">Close the page.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]