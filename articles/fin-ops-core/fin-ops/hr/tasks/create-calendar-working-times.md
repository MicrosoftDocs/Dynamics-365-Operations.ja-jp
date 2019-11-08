---
title: カレンダーの作成および作業時間の生成
description: カレンダーは、運営リソースの能力と作業時間を説明します。 このトピックは、作業時間テンプレートに基づいて作業カレンダーを定義する方法について説明します。
author: andreabichsel
manager: AnnBe
ms.date: 07/09/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: OpResLifeCycleManagementWorkspace, WorkCalendarTable, WorkCalendarDate
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 1645dc42e3c7145feb3081b862c6069d9032913a
ms.sourcegitcommit: 75db3b75d35d27034f9b56e7119c9d0cb7666830
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/03/2019
ms.locfileid: "2550936"
---
# <a name="create-calendars-and-generate-working-times"></a><span data-ttu-id="87adf-104">カレンダーの作成および作業時間の生成</span><span class="sxs-lookup"><span data-stu-id="87adf-104">Create calendars and generate working times</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="87adf-105">カレンダーは、運営リソースの能力と作業時間を説明します。</span><span class="sxs-lookup"><span data-stu-id="87adf-105">Calendars describe the capacity and working times of operations resources.</span></span> <span data-ttu-id="87adf-106">このトピックは、作業時間テンプレートに基づいて作業カレンダーを定義する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="87adf-106">This topic explains how to define a work calendar based on a working time template.</span></span> <span data-ttu-id="87adf-107">デモ データ会社 USMF または独自のデータを使用してこの手順の説明を見ることができます。</span><span class="sxs-lookup"><span data-stu-id="87adf-107">You can walk through this procedure in demo data company USMF, or using your own data.</span></span>

1. <span data-ttu-id="87adf-108">ホーム ページで、**リソース ライフサイクル管理**を選択します。</span><span class="sxs-lookup"><span data-stu-id="87adf-108">On the home page, select **Resource lifecycle management**.</span></span>
2. <span data-ttu-id="87adf-109">**カレンダー**を選択します。</span><span class="sxs-lookup"><span data-stu-id="87adf-109">Select **Calendars**.</span></span>
3. <span data-ttu-id="87adf-110">**新規** を選択します。</span><span class="sxs-lookup"><span data-stu-id="87adf-110">Select **New**.</span></span>
4. <span data-ttu-id="87adf-111">**カレンダー** フィールドで、カレンダーを分類します。</span><span class="sxs-lookup"><span data-stu-id="87adf-111">In the **Calendar** field, classify your calendar.</span></span> <span data-ttu-id="87adf-112">これは、運営リソースまたはリソース グループなどのカレンダーを割り当てるときに参照として使用されるカレンダーの ID です。</span><span class="sxs-lookup"><span data-stu-id="87adf-112">This is the ID of the calendar, which is used as a reference when assigning calendars, such as to an operations resource or a resource group.</span></span>  
5. <span data-ttu-id="87adf-113">**名前**フィールドで、カレンダーに名前を付けます。</span><span class="sxs-lookup"><span data-stu-id="87adf-113">In the **Name** field, name your calendar.</span></span>
6. <span data-ttu-id="87adf-114">**標準作業日 (時)** で、数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="87adf-114">In the **Standard work day in hours** field, enter a number.</span></span>
7. <span data-ttu-id="87adf-115">行が選択されていることを確認し、アクション ウィンドウから**作業時間**を選択します。</span><span class="sxs-lookup"><span data-stu-id="87adf-115">Make sure the row is selected, then select **Working times** from the Action Pane.</span></span>
8. <span data-ttu-id="87adf-116">**作業時間の作成**を選択します。</span><span class="sxs-lookup"><span data-stu-id="87adf-116">Select **Compose working times**.</span></span> <span data-ttu-id="87adf-117">作業をスケジュールできる期間のそれぞれの日の勤務時間を生成します。</span><span class="sxs-lookup"><span data-stu-id="87adf-117">Generate working hours for each day in the period where you want to be able to schedule work.</span></span> <span data-ttu-id="87adf-118">徐々に、その他の期間にも勤務時間生成することができるようになります。</span><span class="sxs-lookup"><span data-stu-id="87adf-118">As time goes by, you can generate working times for additional periods.</span></span>  
9. <span data-ttu-id="87adf-119">**開始日**フィールドに日付を入力します。</span><span class="sxs-lookup"><span data-stu-id="87adf-119">In the **From date** field, enter a date.</span></span> <span data-ttu-id="87adf-120">このカレンダーがオープンになっている必要がある最初の日です。</span><span class="sxs-lookup"><span data-stu-id="87adf-120">This is the first day that this calendar must be open.</span></span>  
10. <span data-ttu-id="87adf-121">**終了日**フィールドに日付を入力します。</span><span class="sxs-lookup"><span data-stu-id="87adf-121">In the **To date field**, enter a date.</span></span> <span data-ttu-id="87adf-122">このカレンダーがオープンになっている最後の日です。</span><span class="sxs-lookup"><span data-stu-id="87adf-122">This is the last day that this calendar is open.</span></span>  
11. <span data-ttu-id="87adf-123">**作業時間テンプレート** フィールドで、値を入力または選択します。</span><span class="sxs-lookup"><span data-stu-id="87adf-123">In the **Working time template** field, enter or select a value.</span></span> <span data-ttu-id="87adf-124">作業時間テンプレートは曜日ごとの勤務時間を定義します。</span><span class="sxs-lookup"><span data-stu-id="87adf-124">The working time template defines the working hours for each day of the week.</span></span>  
12. <span data-ttu-id="87adf-125">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="87adf-125">Select **OK**.</span></span>
13. <span data-ttu-id="87adf-126">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="87adf-126">Close the page.</span></span>

