---
title: 補充タイム フェンス
description: このトピックでは、計画の最適化を使用している場合に補充タイム フェンスを設定する方法について説明します。 補充タイム フェンスは、計画期間と計画限界を示します。
author: ChristianRytt
ms.date: 01/18/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ReqGroup, ReqItemTable, ReqPlanSched
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2021-01-18
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: dcb35eda718ea9b7573d8e994aa45216f8bd30a5
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/01/2021
ms.locfileid: "5836569"
---
# <a name="coverage-time-fences"></a><span data-ttu-id="a8009-104">補充タイム フェンス</span><span class="sxs-lookup"><span data-stu-id="a8009-104">Coverage time fences</span></span>

<span data-ttu-id="a8009-105">このトピックでは、計画の最適化を使用している場合に *補充タイム フェンス* を設定する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="a8009-105">This topic describes how to set up *coverage time fences* when you're using Planning Optimization.</span></span> <span data-ttu-id="a8009-106">プランナーは、計画期間 (日数で表した補充タイム フェンス) を定義し、その期間を超える需要と供給を除外できます。</span><span class="sxs-lookup"><span data-stu-id="a8009-106">Planners can define the planning horizon (the coverage time fence in days), and exclude supply and demand that falls beyond that horizon.</span></span> <span data-ttu-id="a8009-107">そのため、補充タイム フェンスを使用すると、何か月も対応する必要のない供給提案によって発生する "雑音" を防ぐのに役立ちます。</span><span class="sxs-lookup"><span data-stu-id="a8009-107">Therefore, coverage time fences help prevent "noise" that is caused by supply suggestions that you don't have to react to for months.</span></span> <span data-ttu-id="a8009-108">たとえば、通常のリード タイムをはるかに超えた来年の予測注文や顧客注文などです。</span><span class="sxs-lookup"><span data-stu-id="a8009-108">Examples include next year's forecast and customer orders that are placed far beyond the normal lead time.</span></span>

<span data-ttu-id="a8009-109">補充タイム フェンスは、需要と供給が除外される今日の日付 (または、より正確には、計画実行を行う日付) 後の日数です。</span><span class="sxs-lookup"><span data-stu-id="a8009-109">A coverage time fence is the number of days after today's date (or, more precisely, the date when you do the planning run) that supply and demand is excluded.</span></span> <span data-ttu-id="a8009-110">遅延を回避するには、補充タイム フェンスを合計リード タイムより長くする必要があります。</span><span class="sxs-lookup"><span data-stu-id="a8009-110">To help avoid delays, you must ensure that the coverage time fence is longer that the total lead time.</span></span> <span data-ttu-id="a8009-111">既定のシステム値は 100 日です。</span><span class="sxs-lookup"><span data-stu-id="a8009-111">The default system value is 100 days.</span></span>

<span data-ttu-id="a8009-112">補充タイム フェンスは、次の各レベルで指定できます:</span><span class="sxs-lookup"><span data-stu-id="a8009-112">You can specify a coverage time fence at each of the following levels:</span></span>

- <span data-ttu-id="a8009-113">**補充グループ** – 各補充グループに対して既定の補充タイム フェンスを設定できます。</span><span class="sxs-lookup"><span data-stu-id="a8009-113">**Coverage group** – You can set a default coverage time fence for each coverage group.</span></span>
- <span data-ttu-id="a8009-114">**品目補充** – 品目に割り当てられている補充グループから継承された補充タイム フェンス を上書きできます。</span><span class="sxs-lookup"><span data-stu-id="a8009-114">**Item coverage** – You can override the coverage time fence that is inherited from the coverage group that is assigned to an item.</span></span>
- <span data-ttu-id="a8009-115">**マスター プラン** – 補充グループと品目補充設定から継承した補充タイム フェンスを上書きできます。</span><span class="sxs-lookup"><span data-stu-id="a8009-115">**Master plan** – You can override the coverage time fences that are inherited from the coverage group and item coverage settings.</span></span>

<span data-ttu-id="a8009-116">次のセクションでは、各レベルで補充グループを指定する方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="a8009-116">The following sections explain how to specify a coverage group at each level.</span></span>

## <a name="set-a-coverage-time-fence-for-a-coverage-group"></a><span data-ttu-id="a8009-117">補充グループに対する補充タイム フェンスの設定</span><span class="sxs-lookup"><span data-stu-id="a8009-117">Set a coverage time fence for a coverage group</span></span>

<span data-ttu-id="a8009-118">補充グループに対して補充タイム フェンスを指定すると、そのグループに属しているすべての品目 (製品) に設定が適用されます。</span><span class="sxs-lookup"><span data-stu-id="a8009-118">When you specify a coverage time fence for a coverage group, the setting applies to all items (products) that belong to that group.</span></span> <span data-ttu-id="a8009-119">ただし、特定の品目または特定のマスター プランの設定を上書きすることができます。</span><span class="sxs-lookup"><span data-stu-id="a8009-119">However, you can override the setting for specific items or specific master plans.</span></span>

<span data-ttu-id="a8009-120">補充グループの補充タイム フェンスを指定するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="a8009-120">To specify a coverage time fence for a coverage group, follow these steps.</span></span>

1. <span data-ttu-id="a8009-121">**マスター プラン \> 設定 \> 補充 \> 補充グループ** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="a8009-121">Go to **Master planning \> Setup \> Coverage \> Coverage groups**.</span></span>
1. <span data-ttu-id="a8009-122">一覧で既存の補充グループを選択するか、新しい補充グループを作成します。</span><span class="sxs-lookup"><span data-stu-id="a8009-122">Select an existing coverage group in the list, or create a new coverage group.</span></span>
1. <span data-ttu-id="a8009-123">**全般** クイックタブで、**補充タイム フェンス (日)** フィールドを補充グループの補充タイム フェンスとして使用する日数に設定します。</span><span class="sxs-lookup"><span data-stu-id="a8009-123">On the **General** FastTab, set the **Coverage time fence (days)** field to the number of days that you want to use as the coverage time fence for the coverage group.</span></span>

## <a name="set-a-coverage-time-fence-for-a-specific-item"></a><span data-ttu-id="a8009-124">特定の品目に対する補充タイム フェンスの設定</span><span class="sxs-lookup"><span data-stu-id="a8009-124">Set a coverage time fence for a specific item</span></span>

<span data-ttu-id="a8009-125">すべての品目 (製品) は補充グループに属します。</span><span class="sxs-lookup"><span data-stu-id="a8009-125">Every item (product) belongs to a coverage group.</span></span> <span data-ttu-id="a8009-126">品目に明示的に補充グループが割り当てられていない場合は、既定の補充グループが適用されます。</span><span class="sxs-lookup"><span data-stu-id="a8009-126">If no coverage group is explicitly assigned to an item, a default coverage group applies.</span></span> <span data-ttu-id="a8009-127">すべての品目は、その補充グループから補充タイム フェンスを継承します。</span><span class="sxs-lookup"><span data-stu-id="a8009-127">Every item inherits a coverage time fence from its coverage group.</span></span> <span data-ttu-id="a8009-128">ただし、このタイム フェンスは必要に応じて特定の品目に対して上書きできます。</span><span class="sxs-lookup"><span data-stu-id="a8009-128">However, you can override this time fence for specific items as you require.</span></span>

<span data-ttu-id="a8009-129">特定品目の補充タイム フェンスを指定するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="a8009-129">To specify a coverage time fence for a specific item, follow these steps.</span></span>

1. <span data-ttu-id="a8009-130">**製品管理情報 \> 製品 \> リリースされた製品** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="a8009-130">Go to **Product information management \> Products \> Released products**.</span></span>
1. <span data-ttu-id="a8009-131">グリッドで製品を選択します。</span><span class="sxs-lookup"><span data-stu-id="a8009-131">Select a product in the grid.</span></span>
1. <span data-ttu-id="a8009-132">アクション ペインの **製品** タブにある **補充** グループで、**品目補充** を選択します。</span><span class="sxs-lookup"><span data-stu-id="a8009-132">On the Action Pane, on the **Plan** tab, in the **Coverage** group, select **Item coverage**.</span></span>
1. <span data-ttu-id="a8009-133">**品目補充** ページにある **概要** タブで、補充タイム フェンスを設定するサイトの行を選択または作成します。</span><span class="sxs-lookup"><span data-stu-id="a8009-133">On the **Item coverage** page, on the **Overview** tab, select or create a row for the site where you want to set a coverage time fence.</span></span>
1. <span data-ttu-id="a8009-134">**全般** タブを選択すると、選択したサイトの設定が開きます。</span><span class="sxs-lookup"><span data-stu-id="a8009-134">Select the **General** tab to open the settings for the selected site.</span></span>
1. <span data-ttu-id="a8009-135">**補充グループ設定の上書き** チェック ボックスを選択します。</span><span class="sxs-lookup"><span data-stu-id="a8009-135">Select the **Override coverage group settings** check box.</span></span>
1. <span data-ttu-id="a8009-136">**補充タイム フェンス (日)** フィールドを、品目の補充タイム フェンスとして使用する日数に設定します。</span><span class="sxs-lookup"><span data-stu-id="a8009-136">Set the **Coverage time fence (days)** field to the number of days that you want to use as the coverage time fence for the item.</span></span>

## <a name="set-a-coverage-time-fence-for-a-specific-master-plan"></a><span data-ttu-id="a8009-137">特定のマスター プランに対する補充タイム フェンスの設定</span><span class="sxs-lookup"><span data-stu-id="a8009-137">Set a coverage time fence for a specific master plan</span></span>

<span data-ttu-id="a8009-138">マスター プラン レベルで補充タイム フェンスを指定できます。</span><span class="sxs-lookup"><span data-stu-id="a8009-138">You can specify a coverage time fence at the master plan level.</span></span> <span data-ttu-id="a8009-139">このようにして、マスター プランの計算が、マスター プランに対してカバーする日数を定義します。</span><span class="sxs-lookup"><span data-stu-id="a8009-139">In this way, you define the number of days that the master planning calculation covers for a master plan.</span></span> <span data-ttu-id="a8009-140">この設定は、関連する品目および補充グループごとに定義されている補充時間設定を上書きします。</span><span class="sxs-lookup"><span data-stu-id="a8009-140">This setting overrides any coverage time settings that have been defined for each relevant item and coverage group.</span></span>

<span data-ttu-id="a8009-141">特定のマスター プランの補充タイム フェンスを指定するには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="a8009-141">To specify a coverage time fence for a specific master plan, follow these steps.</span></span>

1. <span data-ttu-id="a8009-142">**マスター プラン \> 設定 \> プラン \> マスター プラン** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="a8009-142">Go to **Master planning \> Setup \> Plans \> Master plans**.</span></span>
1. <span data-ttu-id="a8009-143">一覧で既存のマスター プランを選択するか、新しいマスター プランを作成します。</span><span class="sxs-lookup"><span data-stu-id="a8009-143">Select an existing master plan in the list, or create a new master plan.</span></span>
1. <span data-ttu-id="a8009-144">**タイム フェンス (日)** クイックタブで、**補充** オプションを *はい* に設定します。</span><span class="sxs-lookup"><span data-stu-id="a8009-144">On the **Time fences in days** FastTab, set the **Coverage** option to *Yes*.</span></span> <span data-ttu-id="a8009-145">次に、オプションの下のフィールドに、マスター プランの補充タイム フェンスとして使用する日数を入力します。</span><span class="sxs-lookup"><span data-stu-id="a8009-145">Then, in the field under the option, enter the number of days that you want to use as the coverage time fence for the master plan.</span></span>

## <a name="considerations-for-coverage-time-fences"></a><span data-ttu-id="a8009-146">補充タイム フェンスに関する考慮事項</span><span class="sxs-lookup"><span data-stu-id="a8009-146">Considerations for coverage time fences</span></span>

<span data-ttu-id="a8009-147">補充タイム フェンスを設定する際には、次の点を考慮してください:</span><span class="sxs-lookup"><span data-stu-id="a8009-147">As you're setting up coverage time fences, consider the following points:</span></span>

- <span data-ttu-id="a8009-148">補充タイム フェンスは、マスター プランの入力データにのみ影響します。</span><span class="sxs-lookup"><span data-stu-id="a8009-148">Coverage time fences affect only input data for master planning.</span></span> <span data-ttu-id="a8009-149">遅延が発生した場合、結果として生じる計画オーダーの日付は、今日の日付に補充タイム フェンスを加えた日付より後になることがあります。</span><span class="sxs-lookup"><span data-stu-id="a8009-149">If delays occur, the resulting planned orders might have a date that is after today's date plus the coverage time fence.</span></span>
- <span data-ttu-id="a8009-150">補充タイム フェンスはカレンダー日で指定されます。</span><span class="sxs-lookup"><span data-stu-id="a8009-150">Coverage time fences are specified in calendar days.</span></span> <span data-ttu-id="a8009-151">稼働日を使用するカレンダーは、タイム フェンスの計算に影響しません。</span><span class="sxs-lookup"><span data-stu-id="a8009-151">Calendars that use working days won't affect the time fence calculation.</span></span> <span data-ttu-id="a8009-152">たとえば、週末が稼働日カレンダーで休業日として設定されている場合でも、常に 1 週間は 7 日と見なされます。</span><span class="sxs-lookup"><span data-stu-id="a8009-152">For example, a week is always considered seven days, even if weekends are set up as closed days in the working time calendar.</span></span>
- <span data-ttu-id="a8009-153">補充タイム フェンス外の需要と供給に対して、要求トランザクションは生成されません。</span><span class="sxs-lookup"><span data-stu-id="a8009-153">Requirement transactions won't be generated for any supply and demand that falls outside the coverage time fence.</span></span>
- <span data-ttu-id="a8009-154">承認済の需要と供給が補充タイム フェンス外にある場合は、エンジンには読み込まれません。</span><span class="sxs-lookup"><span data-stu-id="a8009-154">If any approved supply and demand falls outside the coverage time fence, it won't be loaded into the engine.</span></span> <span data-ttu-id="a8009-155">したがって、補充がトリガーされることはなく、遅延は計算されません。</span><span class="sxs-lookup"><span data-stu-id="a8009-155">Therefore, it won't trigger any replenishment, and delays won't be calculated.</span></span> <span data-ttu-id="a8009-156">それでも、この需要と供給はシステムから消さないでください。</span><span class="sxs-lookup"><span data-stu-id="a8009-156">Nevertheless, this supply and demand should not be wiped from the system.</span></span>
- <span data-ttu-id="a8009-157">補充タイム フェンス外にある場合、安全在庫数量の変動 (最小キーから) は無視されます。</span><span class="sxs-lookup"><span data-stu-id="a8009-157">Variations in safety stock quantities (from minimum keys) will be ignored if they fall outside the coverage time fence.</span></span>
- <span data-ttu-id="a8009-158">計算された指定出荷日が補充タイム フェンス内にない場合、企業内需要は無視されます。</span><span class="sxs-lookup"><span data-stu-id="a8009-158">Intercompany demand will be ignored if the requested ship date that is calculated isn't inside the coverage time fence.</span></span> <span data-ttu-id="a8009-159">組み込みマスター プランの場合、企業内需要は補充タイム フェンスで制限されないことに注意してください。</span><span class="sxs-lookup"><span data-stu-id="a8009-159">Note that, for built-in master planning, intercompany demand isn't limited by the coverage time fence.</span></span>
- <span data-ttu-id="a8009-160">予算日が補充タイム フェンス内にない場合、需要予測は無視されます。</span><span class="sxs-lookup"><span data-stu-id="a8009-160">Demand forecasts will be ignored if the budget date isn't inside the coverage time fence.</span></span> <span data-ttu-id="a8009-161">組み込みマスター プランの場合、需要予測は補充タイム フェンスで制限されないことに注意してください。</span><span class="sxs-lookup"><span data-stu-id="a8009-161">Note that, for built-in master planning, demand forecasts aren't limited by the coverage time fence.</span></span>
- <span data-ttu-id="a8009-162">計画の最適化は、タイム ゾーンに対応しています。</span><span class="sxs-lookup"><span data-stu-id="a8009-162">Planning Optimization is time zone–aware.</span></span> <span data-ttu-id="a8009-163">需要と供給サイトのタイム ゾーンと、計画実行の時間を考慮します。</span><span class="sxs-lookup"><span data-stu-id="a8009-163">It considers the time zone at the supply and demand sites, and the time of the planning run.</span></span> <span data-ttu-id="a8009-164">たとえば、マスター プランが 10 月 15 日の午前 11 時にデンマーク (GMT+1 タイム ゾーン) のサイトからトリガーされ、10 日間の補充タイム フェンスが使用されます。</span><span class="sxs-lookup"><span data-stu-id="a8009-164">For example, master planning is triggered at 11 AM on October 15 from a site in Denmark (GMT+1 time zone), and a coverage time fence of ten days is used.</span></span> <span data-ttu-id="a8009-165">この場合、シアトル (GMT-8 タイム ゾーン) のサイトからの需要と供給は、10 月 25 日の午前 2 時まで含まれます (= マスター プランがトリガーから 9 時間のタイム ゾーン差を差し引いた 24 時間の 10 日間)。</span><span class="sxs-lookup"><span data-stu-id="a8009-165">In this case, supply and demand from a site in Seattle (GMT-8 time zone) is included until 2 AM on October 25 (= ten 24-hour days after master planning was triggered, minus the time zone difference of nine hours).</span></span> <span data-ttu-id="a8009-166">組み込みのマスター プラン エンジンではタイム フェンスの日付だけが考慮されることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="a8009-166">Note that the built-in master planning engine considers only the date of the time fence.</span></span> <span data-ttu-id="a8009-167">したがって、結果は異なる場合があります。</span><span class="sxs-lookup"><span data-stu-id="a8009-167">Therefore, the result can differ.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]