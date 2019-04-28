---
title: プロジェクト タイムシートの入力
description: この手順で、空のタイム シートのフォームを使用して、タイム シートを作成できます。
author: andreabichsel
manager: AnnBe
ms.date: 11/10/2016
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Operations, Talent
ms.search.region: Global
ms.search.industry: Service industries
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 3f1be02f0080ee23359ad905b1e997d8cd5adfd2
ms.sourcegitcommit: 608e68b603afef9eb98d8fb25e90109c2473ef87
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/19/2019
ms.locfileid: "859140"
---
# <a name="enter-project-timesheets"></a><span data-ttu-id="c4504-103">プロジェクト タイムシートの入力</span><span class="sxs-lookup"><span data-stu-id="c4504-103">Enter project timesheets</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="c4504-104">この手順で、空のタイム シートのフォームを使用して、タイム シートを作成できます。</span><span class="sxs-lookup"><span data-stu-id="c4504-104">This procedure lets you create a timesheet by using an empty timesheet form.</span></span> <span data-ttu-id="c4504-105">新しいタイムシートは、以前のタイム シート、またはプロジェクトおよび [お気に入り] ページの活動の割り当てからの情報に基づくこともできます。</span><span class="sxs-lookup"><span data-stu-id="c4504-105">The new timesheet can be based on information from a previous timesheet, or from project and activity assignments in the My favorites page.</span></span> <span data-ttu-id="c4504-106">既定では、[すべてのタイムシート] リスト ページに現在のタイム シートをすべて表示します。</span><span class="sxs-lookup"><span data-stu-id="c4504-106">By default, the All timesheets list page displays all your timesheets for the current period.</span></span> <span data-ttu-id="c4504-107">期間またはプロジェクトでタイムシートの一覧をフィルター処理、または他の作業者に代わって作成されたタイム シートを表示する場合にも、[自分のタイムシート] ページの [表示] フィールドのドロップダウン リストを使用できます。</span><span class="sxs-lookup"><span data-stu-id="c4504-107">You can use the drop-down list for the Show field in the My timesheets page to filter the timesheet list by time period or project, or to view timesheets that were created on behalf of other workers.</span></span> <span data-ttu-id="c4504-108">この手順の作成に使用するデモ データの会社は USSI です。</span><span class="sxs-lookup"><span data-stu-id="c4504-108">The demo data company used to create this procedure is USSI.</span></span> <span data-ttu-id="c4504-109">この手順を開始するには、[プロジェクト管理] および [会計] > [タイムシート] > [自分のタイムシート] に移動します。</span><span class="sxs-lookup"><span data-stu-id="c4504-109">To begin this procedure, go to Project management and accounting > Timesheets >My timesheets</span></span>

1. <span data-ttu-id="c4504-110">新しいタイムシートを入力するには、[新規] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="c4504-110">To enter a new timesheet, click New.</span></span>
    * <span data-ttu-id="c4504-111">リソースのドロップダウン リストは既定で、現在のユーザーに割り当てられている作業者を示します。</span><span class="sxs-lookup"><span data-stu-id="c4504-111">The Resource drop-down list shows the worker assigned to the current user, by default.</span></span>  
    * <span data-ttu-id="c4504-112">ユーザーがデリゲートとして指定されている場合は、ユーザーが代わりにタイムシートを入力できるように名前が表示されます。</span><span class="sxs-lookup"><span data-stu-id="c4504-112">If the user is designated as a delegate, this will list the names so that a user can enter a timesheet on their behalf.</span></span>  
2. <span data-ttu-id="c4504-113">[日付] フィールドに日付を入力します。</span><span class="sxs-lookup"><span data-stu-id="c4504-113">In the Date field, enter a date.</span></span>
    * <span data-ttu-id="c4504-114">このオプションを選択した場合、新しいタイムシートの行はお気に入りとしてコンフィギュレーションされたタイムシートの設定を使用して作成されます。</span><span class="sxs-lookup"><span data-stu-id="c4504-114">If this option is selected, new timesheet lines will be created by using the timesheet settings that were configured as favorites.</span></span>  
3. <span data-ttu-id="c4504-115">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="c4504-115">Click OK.</span></span>
4. <span data-ttu-id="c4504-116">[新しい明細行] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="c4504-116">Click New line.</span></span>
5. <span data-ttu-id="c4504-117">一覧で、選択された行をマークします。</span><span class="sxs-lookup"><span data-stu-id="c4504-117">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="c4504-118">[法人] フィールドでは、既定で現在の [法人] が表示されます。</span><span class="sxs-lookup"><span data-stu-id="c4504-118">The Legal Entity field displays the current Legal entity by default.</span></span>   
6. <span data-ttu-id="c4504-119">[プロジェクト] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="c4504-119">In the Project field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="c4504-120">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="c4504-120">In the list, find and select the desired record.</span></span>
8. <span data-ttu-id="c4504-121">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="c4504-121">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="c4504-122">[活動] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="c4504-122">In the Activity field, click the drop-down button to open the lookup.</span></span>
10. <span data-ttu-id="c4504-123">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="c4504-123">In the list, find and select the desired record.</span></span>
11. <span data-ttu-id="c4504-124">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="c4504-124">In the list, click the link in the selected row.</span></span>
12. <span data-ttu-id="c4504-125">[カテゴリ] フィールドで、ドロップ ダウン ボタンをクリックし、ルックアップを開きます。</span><span class="sxs-lookup"><span data-stu-id="c4504-125">In the Category field, click the drop-down button to open the lookup.</span></span>
13. <span data-ttu-id="c4504-126">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="c4504-126">In the list, find and select the desired record.</span></span>
14. <span data-ttu-id="c4504-127">一覧で、選択された行のリンクをクリックします。</span><span class="sxs-lookup"><span data-stu-id="c4504-127">In the list, click the link in the selected row.</span></span>
15. <span data-ttu-id="c4504-128">毎日の勤務時間を入力します。</span><span class="sxs-lookup"><span data-stu-id="c4504-128">Enter the number of hours worked each day.</span></span>
    * <span data-ttu-id="c4504-129">時間は、小数点形式で入力する必要があります。</span><span class="sxs-lookup"><span data-stu-id="c4504-129">Hours should be entered in a decimal format.</span></span>  <span data-ttu-id="c4504-130">たとえば、2 時間 15 分間働いたら、2.25 を入力します。</span><span class="sxs-lookup"><span data-stu-id="c4504-130">For example, if you worked for two hours and fifteen minutes, enter 2.25.</span></span>   
16. <span data-ttu-id="c4504-131">毎日の勤務時間を入力します。</span><span class="sxs-lookup"><span data-stu-id="c4504-131">Enter the number of hours worked each day.</span></span>
    * <span data-ttu-id="c4504-132">時間は、小数点形式で入力する必要があります。</span><span class="sxs-lookup"><span data-stu-id="c4504-132">Hours should be entered in a decimal format.</span></span>  <span data-ttu-id="c4504-133">たとえば、2 時間 15 分間働いたら、2.25 を入力します。</span><span class="sxs-lookup"><span data-stu-id="c4504-133">For example, if you worked for two hours and fifteen minutes, enter 2.25.</span></span>   
17. <span data-ttu-id="c4504-134">毎日の勤務時間を入力します。</span><span class="sxs-lookup"><span data-stu-id="c4504-134">Enter the number of hours worked each day.</span></span>
    * <span data-ttu-id="c4504-135">時間は、小数点形式で入力する必要があります。</span><span class="sxs-lookup"><span data-stu-id="c4504-135">Hours should be entered in a decimal format.</span></span>  <span data-ttu-id="c4504-136">たとえば、2 時間 15 分間働いたら、2.25 を入力します。</span><span class="sxs-lookup"><span data-stu-id="c4504-136">For example, if you worked for two hours and fifteen minutes, enter 2.25.</span></span>   
18. <span data-ttu-id="c4504-137">毎日の勤務時間を入力します。</span><span class="sxs-lookup"><span data-stu-id="c4504-137">Enter the number of hours worked each day.</span></span>
    * <span data-ttu-id="c4504-138">時間は、小数点形式で入力する必要があります。</span><span class="sxs-lookup"><span data-stu-id="c4504-138">Hours should be entered in a decimal format.</span></span>  <span data-ttu-id="c4504-139">たとえば、2 時間 15 分間働いたら、2.25 を入力します。</span><span class="sxs-lookup"><span data-stu-id="c4504-139">For example, if you worked for two hours and fifteen minutes, enter 2.25.</span></span>   
19. <span data-ttu-id="c4504-140">毎日の勤務時間を入力します。</span><span class="sxs-lookup"><span data-stu-id="c4504-140">Enter the number of hours worked each day.</span></span>
    * <span data-ttu-id="c4504-141">時間は、小数点形式で入力する必要があります。</span><span class="sxs-lookup"><span data-stu-id="c4504-141">Hours should be entered in a decimal format.</span></span>  <span data-ttu-id="c4504-142">たとえば、2 時間 15 分間働いたら、2.25 を入力します。</span><span class="sxs-lookup"><span data-stu-id="c4504-142">For example, if you worked for two hours and fifteen minutes, enter 2.25.</span></span>   
    * <span data-ttu-id="c4504-143">[行の詳細] で、次のオプションを選択できます。o 税および財務分析コードに関する情報を追加します。</span><span class="sxs-lookup"><span data-stu-id="c4504-143">In Line details, the following options are available:  o  Add information about taxes and financial dimensions.</span></span>  <span data-ttu-id="c4504-144">o    タイムシート行に関するコメントを追加します。</span><span class="sxs-lookup"><span data-stu-id="c4504-144">o    Add comments about the timesheet line.</span></span>  
20. <span data-ttu-id="c4504-145">[ワークフロー] をクリックすると、ドロップ ダイアログを開きます。</span><span class="sxs-lookup"><span data-stu-id="c4504-145">Click Workflow to open the drop dialog.</span></span>
21. <span data-ttu-id="c4504-146">[送信] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="c4504-146">Click Submit.</span></span>
22. <span data-ttu-id="c4504-147">[送信] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="c4504-147">Click Submit.</span></span>

