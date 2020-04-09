---
title: ベースライン予測の作成
description: タイム シリーズの予測モデルを使用するか、または履歴需要をコピーするかのいずれかの方法を使用して、生産計画担当者はベースライン予測を作成できます。
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqIntercompanyPlanningGroupSetup, ReqIntercompanyPlanningGroupAllocKeys, ReqDemPlanForecastParameters, ReqDemPlanCreateForecastDialog, SysQueryForm, ReqDemPlanForecastViewer
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 85d687c0c21112f815bb5cf28b0af5501d299c12
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 03/18/2020
ms.locfileid: "3148127"
---
# <a name="create-a-baseline-forecast"></a><span data-ttu-id="c4363-103">ベースライン予測の作成</span><span class="sxs-lookup"><span data-stu-id="c4363-103">Create a baseline forecast</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="c4363-104">タイム シリーズの予測モデルを使用するか、または履歴需要をコピーするかのいずれかの方法を使用して、生産計画担当者はベースライン予測を作成できます。</span><span class="sxs-lookup"><span data-stu-id="c4363-104">A production planner can create a baseline forecast either by using time series forecast models or by copying the historical demand.</span></span> <span data-ttu-id="c4363-105">この手順では、需要履歴をコピーし、1 つの品目配賦キーを使用してすべての製品のベースライン予測を作成する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="c4363-105">This procedure shows how to copy the historical demand to create a baseline forecast for all products using one item allocation key.</span></span> 


## <a name="set-up-an-item-allocation-key"></a><span data-ttu-id="c4363-106">品目配賦キーの設定</span><span class="sxs-lookup"><span data-stu-id="c4363-106">Set up an item allocation key</span></span>
1. <span data-ttu-id="c4363-107">[マスター プラン] > [設定] > [会社間計画グループ] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="c4363-107">Go to Master planning > Setup > Intercompany planning groups.</span></span>
2. <span data-ttu-id="c4363-108">クイック フィルターを使用して、レコードを見つけます。</span><span class="sxs-lookup"><span data-stu-id="c4363-108">Use the Quick Filter to find records.</span></span> <span data-ttu-id="c4363-109">たとえば、値「10」を含む [名前] フィールドをフィルター処理します。</span><span class="sxs-lookup"><span data-stu-id="c4363-109">For example, filter on the Name field with a value of '10'.</span></span>
    * <span data-ttu-id="c4363-110">需要予測は法人間で実行されます。</span><span class="sxs-lookup"><span data-stu-id="c4363-110">Demand forecasting runs across legal entities.</span></span> <span data-ttu-id="c4363-111">このため、1 件の会社間計画グループの予測を生成するために使用するすべての会社を設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="c4363-111">That's why you need to set up all the companies for which you want to generate forecasts in one intercompany planning group.</span></span>  
3. <span data-ttu-id="c4363-112">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="c4363-112">In the list, find and select the desired record.</span></span>
4. <span data-ttu-id="c4363-113">[品目配賦キー] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="c4363-113">Click Item allocation keys.</span></span>
    * <span data-ttu-id="c4363-114">予測を作成するために使用するすべての品目配賦キーを選択します。</span><span class="sxs-lookup"><span data-stu-id="c4363-114">Select all the item allocation keys for which you want to create forecasts.</span></span>  
5. <span data-ttu-id="c4363-115">一覧で、選択された行をマークします。</span><span class="sxs-lookup"><span data-stu-id="c4363-115">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="c4363-116">D_Aloc の品目配賦キーを選択します。</span><span class="sxs-lookup"><span data-stu-id="c4363-116">Select D_Aloc item allocation key.</span></span>  
6. <span data-ttu-id="c4363-117">[>] を選択します。</span><span class="sxs-lookup"><span data-stu-id="c4363-117">Click >.</span></span>
7. <span data-ttu-id="c4363-118">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="c4363-118">Close the page.</span></span>
8. <span data-ttu-id="c4363-119">ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="c4363-119">Close the page.</span></span>

## <a name="set-up-the-demand-forecasting-paramters"></a><span data-ttu-id="c4363-120">需要予測のパラメーターの設定</span><span class="sxs-lookup"><span data-stu-id="c4363-120">Set up the demand forecasting paramters</span></span>
1. <span data-ttu-id="c4363-121">[マスター プラン] > [設定] > [需要予測] > [需要予測のパラメーター] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="c4363-121">Go to Master planning > Setup > Demand forecasting > Demand forecasting parameters.</span></span>
2. <span data-ttu-id="c4363-122">予測アルゴリズム パラメータ セクションを展開します。</span><span class="sxs-lookup"><span data-stu-id="c4363-122">Expand the Forecast algorithm parameters section.</span></span>
3. <span data-ttu-id="c4363-123">[予測生成戦略] フィールドで、[履歴需要の上書き] を選択します。</span><span class="sxs-lookup"><span data-stu-id="c4363-123">In the Forecast generation strategy field, select 'Copy over historical demand'.</span></span>
4. <span data-ttu-id="c4363-124">[保存] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="c4363-124">Click Save.</span></span>

## <a name="create-a-baseline-forecast"></a><span data-ttu-id="c4363-125">ベースライン予測の作成</span><span class="sxs-lookup"><span data-stu-id="c4363-125">Create a baseline forecast</span></span>
1. <span data-ttu-id="c4363-126">[マスター プラン] > [予測] > [需要予測] > [統計ベースライン予測の生成] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="c4363-126">Go to Master planning > Forecasting > Demand forecasting > Generate statistical baseline forecast.</span></span>
2. <span data-ttu-id="c4363-127">[開始日] フィールドに日付を入力します。</span><span class="sxs-lookup"><span data-stu-id="c4363-127">In the From date field, enter a date.</span></span>
    * <span data-ttu-id="c4363-128">2015 年 1 月 1 日以降の販売注文がある場合、その日付を入力します。</span><span class="sxs-lookup"><span data-stu-id="c4363-128">If you have sales orders starting from January 1, 2015, enter this date.</span></span> <span data-ttu-id="c4363-129">ない場合、販売注文の最も早い日付を入力します。</span><span class="sxs-lookup"><span data-stu-id="c4363-129">If you don't, enter the earliest date of your sales orders.</span></span>  
3. <span data-ttu-id="c4363-130">[終了日] フィールドで、日付を入力します。</span><span class="sxs-lookup"><span data-stu-id="c4363-130">In the To date field, enter a date.</span></span>
    * <span data-ttu-id="c4363-131">販売注文の終了日を入力します。例「2015-03-31」。</span><span class="sxs-lookup"><span data-stu-id="c4363-131">Enter the last date of your sales orders, for example '2015-03-31'.</span></span>  
4. <span data-ttu-id="c4363-132">[開始日] フィールドに日付を入力します。</span><span class="sxs-lookup"><span data-stu-id="c4363-132">In the From date field, enter a date.</span></span>
    * <span data-ttu-id="c4363-133">「2015-04-01」と入力します。</span><span class="sxs-lookup"><span data-stu-id="c4363-133">Enter '2015-04-01'.</span></span> <span data-ttu-id="c4363-134">この日付は、次の予測バケットの開始日として自動的に計算されます。</span><span class="sxs-lookup"><span data-stu-id="c4363-134">This date will be automatically calculated as the start date of the next forecasting bucket.</span></span>  
5. <span data-ttu-id="c4363-135">[対象に含めるレコード] セクションを展開します。</span><span class="sxs-lookup"><span data-stu-id="c4363-135">Expand the Records to include section.</span></span>
6. <span data-ttu-id="c4363-136">[フィルター] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="c4363-136">Click Filter.</span></span>
7. <span data-ttu-id="c4363-137">一覧で、選択された行をマークします。</span><span class="sxs-lookup"><span data-stu-id="c4363-137">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="c4363-138">[会社間計画グループ] フィールドの行をマークします。</span><span class="sxs-lookup"><span data-stu-id="c4363-138">Mark the row where Field = Intercompany planning group.</span></span>  
8. <span data-ttu-id="c4363-139">[基準] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="c4363-139">In the Criteria field, type a value.</span></span>
    * <span data-ttu-id="c4363-140">会社間計画グループを入力します。たとえば、最初のタスクに使用した「10」を入力します。</span><span class="sxs-lookup"><span data-stu-id="c4363-140">Type the intercompany planning group, for example, 10, that you used in the first task.</span></span>  
9. <span data-ttu-id="c4363-141">一覧で、目的のレコードを見つけ、選択します。</span><span class="sxs-lookup"><span data-stu-id="c4363-141">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="c4363-142">[品目配賦キー] フィールドの行を選択します。</span><span class="sxs-lookup"><span data-stu-id="c4363-142">Select the row where Field = Item allocation key.</span></span>  
10. <span data-ttu-id="c4363-143">[基準] フィールドに値を入力します。</span><span class="sxs-lookup"><span data-stu-id="c4363-143">In the Criteria field, type a value.</span></span>
11. <span data-ttu-id="c4363-144">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="c4363-144">Click OK.</span></span>
12. <span data-ttu-id="c4363-145">[詳細パラメーター] セクションを展開します。</span><span class="sxs-lookup"><span data-stu-id="c4363-145">Expand the Advanced parameters section.</span></span>
13. <span data-ttu-id="c4363-146">[予測バケット] フィールドで [月] を選択します。</span><span class="sxs-lookup"><span data-stu-id="c4363-146">In the Forecast bucket field, select 'Month'.</span></span>
14. <span data-ttu-id="c4363-147">[予測期間] フィールドに「3」を入力します。</span><span class="sxs-lookup"><span data-stu-id="c4363-147">In the Forecast horizon field, enter '3'.</span></span>
15. <span data-ttu-id="c4363-148">[凍結タイム フェンス] フィールドに「1」を入力します。</span><span class="sxs-lookup"><span data-stu-id="c4363-148">In the Freeze time fence field, enter '1'.</span></span>
16. <span data-ttu-id="c4363-149">[OK] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="c4363-149">Click OK.</span></span>

## <a name="visualize-the-demand-forecast"></a><span data-ttu-id="c4363-150">需要予測の視覚化</span><span class="sxs-lookup"><span data-stu-id="c4363-150">Visualize the demand forecast</span></span>
1. <span data-ttu-id="c4363-151">[マスター プラン] > [予測] > [需要予測] > [調整された需要予測] の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="c4363-151">Go to Master planning > Forecasting > Demand forecasting > Adjusted demand forecast.</span></span>
2. <span data-ttu-id="c4363-152">集計ビュー テーブルで、行 1、行 2 のセルを選択します。</span><span class="sxs-lookup"><span data-stu-id="c4363-152">In the aggregated view table, select the cell in row 1, column 2.</span></span> <span data-ttu-id="c4363-153">これは、作成した予測の 2 番目の月です。</span><span class="sxs-lookup"><span data-stu-id="c4363-153">This is the second month for which you have created forecast.</span></span>
3. <span data-ttu-id="c4363-154">QtyCell に「400」を設定します。</span><span class="sxs-lookup"><span data-stu-id="c4363-154">Set QtyCell to '400'.</span></span>
    * <span data-ttu-id="c4363-155">セルでは、予測された以外の数、例えば「400」を入力します。</span><span class="sxs-lookup"><span data-stu-id="c4363-155">In the cell, enter a different number than the one that was forecasted, for example, 400.</span></span>  
4. <span data-ttu-id="c4363-156">予測に手動調整を実行しました。</span><span class="sxs-lookup"><span data-stu-id="c4363-156">You have made a manual adjustment to the forecast.</span></span> <span data-ttu-id="c4363-157">次の手順ではグラフィカル インジケータに注意します。</span><span class="sxs-lookup"><span data-stu-id="c4363-157">Notice the graphical indication in the next step.</span></span>
5. <span data-ttu-id="c4363-158">[予測明細行の詳細] をクリックします。</span><span class="sxs-lookup"><span data-stu-id="c4363-158">Click Forecast line details.</span></span>
    * <span data-ttu-id="c4363-159">このページでは、正確性の値、履歴需要および予測を確認できます。</span><span class="sxs-lookup"><span data-stu-id="c4363-159">In this page, you can see the accuracy values, historical demand, and forecast.</span></span> <span data-ttu-id="c4363-160">予測にも変更を加えることができます。</span><span class="sxs-lookup"><span data-stu-id="c4363-160">You can make changes to the forecast as well.</span></span>  

