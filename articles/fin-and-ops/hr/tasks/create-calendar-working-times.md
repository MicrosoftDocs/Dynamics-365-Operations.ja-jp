---
title: カレンダーの作成および作業時間の生成
description: カレンダーは、運営リソースの能力と作業時間を説明します。
author: kherr75
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: OpResLifeCycleManagementWorkspace, WorkCalendarTable, WorkCalendarDate
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kherr
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 8a556367857890acdb926ed29518cf2f2f2b92ea
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/29/2019
ms.locfileid: "336017"
---
# <a name="create-calendar-and-generate-working-times"></a><span data-ttu-id="0c515-103">カレンダーの作成および作業時間の生成</span><span class="sxs-lookup"><span data-stu-id="0c515-103">Create calendar and generate working times</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="0c515-104">カレンダーは、運営リソースの能力と作業時間を説明します。</span><span class="sxs-lookup"><span data-stu-id="0c515-104">Calendars describe the capacity and working times of operations resources.</span></span> <span data-ttu-id="0c515-105">この手順は、作業時間テンプレートに基づいて作業カレンダーを定義するのに便利です。</span><span class="sxs-lookup"><span data-stu-id="0c515-105">This procedure will help you define a work calendar based on a working time template.</span></span> <span data-ttu-id="0c515-106">デモ データ会社 USMF または独自のデータを使用してこの手順の説明を見ることができます。</span><span class="sxs-lookup"><span data-stu-id="0c515-106">You can walk through this procedure in demo data company USMF, or using your own data.</span></span>

1. <span data-ttu-id="0c515-107">[すべてのワークスペース] > [リソース ライフサイクル管理] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="0c515-107">Go to All workspaces > Resource lifecycle management.</span></span>
2. <span data-ttu-id="0c515-108">[カレンダー] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="0c515-108">Click Calendars.</span></span>
3. <span data-ttu-id="0c515-109">[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="0c515-109">Click New.</span></span>
4. <span data-ttu-id="0c515-110">[カレンダー] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="0c515-110">In the Calendar field, type a value.</span></span>
    * <span data-ttu-id="0c515-111">これは、運営リソースまたはリソース グループなどのカレンダーを割り当てるときに参照として使用されるカレンダーの ID です。</span><span class="sxs-lookup"><span data-stu-id="0c515-111">This is the ID of the calendar, which is used as a reference when assigning calendars, such as to an operations resource or a resource group.</span></span>  
5. <span data-ttu-id="0c515-112">[名前] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="0c515-112">In the Name field, type a value.</span></span>
6. <span data-ttu-id="0c515-113">[標準作業日 (時)] で、数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="0c515-113">In the Standard work day in hours field, enter a number.</span></span>
7. <span data-ttu-id="0c515-114">一覧で、選択された行をマークします。</span><span class="sxs-lookup"><span data-stu-id="0c515-114">In the list, mark the selected row.</span></span>
8. <span data-ttu-id="0c515-115">[作業時間] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="0c515-115">Click Working times.</span></span>
9. <span data-ttu-id="0c515-116">[作業時間の作成] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="0c515-116">Click Compose working times.</span></span>
    * <span data-ttu-id="0c515-117">作業をスケジュールできる期間のそれぞれの日の勤務時間を生成します。</span><span class="sxs-lookup"><span data-stu-id="0c515-117">Generate working hours for each day in the period where you want to be able to schedule work.</span></span> <span data-ttu-id="0c515-118">徐々に、その他の期間にも勤務時間生成することができるようになります。</span><span class="sxs-lookup"><span data-stu-id="0c515-118">As time goes by, you can generate working times for additional periods.</span></span>  
10. <span data-ttu-id="0c515-119">[開始日] フィールドに日付を入力します。</span><span class="sxs-lookup"><span data-stu-id="0c515-119">In the From date field, enter a date.</span></span>
    * <span data-ttu-id="0c515-120">このカレンダーがオープンになっている必要がある最初の日です。</span><span class="sxs-lookup"><span data-stu-id="0c515-120">This is the first day that this calendar must be open.</span></span>  
11. <span data-ttu-id="0c515-121">[終了日] フィールドで、日付を入力します。</span><span class="sxs-lookup"><span data-stu-id="0c515-121">In the To date field, enter a date.</span></span>
    * <span data-ttu-id="0c515-122">このカレンダーがオープンになっている最後の日です。</span><span class="sxs-lookup"><span data-stu-id="0c515-122">This is the last day that this calendar is open.</span></span>  
12. <span data-ttu-id="0c515-123">[作業時間テンプレート] フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="0c515-123">In the Working time template field, enter or select a value.</span></span>
    * <span data-ttu-id="0c515-124">作業時間テンプレートは曜日ごとの勤務時間を定義します。</span><span class="sxs-lookup"><span data-stu-id="0c515-124">The working time template defines the working hours for each day of the week.</span></span>  
13. <span data-ttu-id="0c515-125">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="0c515-125">Click OK.</span></span>
14. <span data-ttu-id="0c515-126">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="0c515-126">Close the page.</span></span>

