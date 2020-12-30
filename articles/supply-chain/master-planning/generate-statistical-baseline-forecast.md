---
title: 統計ベースライン予測の生成
description: このトピックは、需要予測の計算に使用されるパラメーターおよびフィルターについて説明しています。
author: roxanadiaconu
manager: tfehr
ms.date: 07/08/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqDemPlanCreateForecastDialog
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 72683
ms.assetid: 42190463-2a64-4f63-b653-10cac3df0692
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: db0ac2d56db46f283716df6615e404a5354f8d3e
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/13/2020
ms.locfileid: "4432206"
---
# <a name="generate-a-statistical-baseline-forecast"></a><span data-ttu-id="729a1-103">統計ベースライン予測の生成</span><span class="sxs-lookup"><span data-stu-id="729a1-103">Generate a statistical baseline forecast</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="729a1-104">このトピックは、需要予測の計算に使用されるパラメーターおよびフィルターについて説明しています。</span><span class="sxs-lookup"><span data-stu-id="729a1-104">This topic provides information about the parameters and filters that are used in the calculation of demand forecasting.</span></span> 

<span data-ttu-id="729a1-105">ベースライン予測を作成するとき、計算に使用されるパラメーターとフィルターを最初に指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="729a1-105">When you create a baseline forecast, you must first specify the parameters and filters that are used in the calculation.</span></span> <span data-ttu-id="729a1-106">たとえば、特定の会社について、翌月について、また選択した品目グループについて、過去 1 年のトランザクション データに基づいて、需要を見積もるベースライン予測を作成できます。</span><span class="sxs-lookup"><span data-stu-id="729a1-106">For example, you can create a baseline forecast that estimates demand based on transaction data from the past year for a specific company, for the coming month, and for a selected group of items.</span></span> 

<span data-ttu-id="729a1-107">需要予測の生成へは、**マスター プラン &gt; 予測 &gt; 需要予測 &gt; 統計ベースライン予測の生成** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="729a1-107">To generate a demand forecast, go to **Master planning &gt; Forecasting &gt; Demand forecasting &gt; Generate statistical baseline forecast**.</span></span> 

<span data-ttu-id="729a1-108">予測バケットは予測生成時に選択できます。</span><span class="sxs-lookup"><span data-stu-id="729a1-108">The forecast bucket can be selected at forecast generation time.</span></span> <span data-ttu-id="729a1-109">利用可能な値は、"日、週" および "月" です。</span><span class="sxs-lookup"><span data-stu-id="729a1-109">The available values are: Day, Week, and Month.</span></span> 

<span data-ttu-id="729a1-110">予測されている生成するバケットの数は、**予測期間** フィールドに設定されています。</span><span class="sxs-lookup"><span data-stu-id="729a1-110">The number of buckets to generate a forecast for is set in the **Forecast horizon** field.</span></span> 

<span data-ttu-id="729a1-111">予測方法が **履歴需要の上書き** に設定されている場合、履歴期間の終了は無視されます。</span><span class="sxs-lookup"><span data-stu-id="729a1-111">When the forecast strategy is set to **Copy over historical demand**, the end of the historical horizon is ignored.</span></span> <span data-ttu-id="729a1-112">システムでは需要予測に、**履歴期間** にある **開始日** フィールドにセットされた日付から、**予測期間** フィールドに指定されたバケットの数をコピー します。</span><span class="sxs-lookup"><span data-stu-id="729a1-112">The system copies the number of buckets specified in the **Forecast horizon** field to the forecast demand, starting from the date set in the **From date** field under **Historical horizon**.</span></span> <span data-ttu-id="729a1-113">特定の日付以前から履歴需要をコピーして、生産のスケジューリング者は二つの方法で来四半期の計画を行うことができます:</span><span class="sxs-lookup"><span data-stu-id="729a1-113">By copying historical demand from a certain date forward, production planners can make the plan for the next quarter in two ways:</span></span>

-   <span data-ttu-id="729a1-114">昨年の同じ四半期の需要をコピーすることで。</span><span class="sxs-lookup"><span data-stu-id="729a1-114">By copying the demand from the same quarter last year.</span></span>
-   <span data-ttu-id="729a1-115">前の四半期の需要をコピーすることで。</span><span class="sxs-lookup"><span data-stu-id="729a1-115">By copying the demand from the previous quarter.</span></span>

<span data-ttu-id="729a1-116">生産計画の混乱を回避するために、一定数の予測バケットは凍結できます。</span><span class="sxs-lookup"><span data-stu-id="729a1-116">To prevent confusion in the production plans, a certain number of forecast buckets can be frozen.</span></span> <span data-ttu-id="729a1-117">この番号は、**凍結タイム フェンス** フィールドに設定されます。</span><span class="sxs-lookup"><span data-stu-id="729a1-117">This number is set in the **Freeze time fence** field.</span></span> <span data-ttu-id="729a1-118">**調整された需要予測** ページで、その値が変更されないよう視覚的表示があり、凍結するバケットのセルは無効になります。</span><span class="sxs-lookup"><span data-stu-id="729a1-118">On the **Adjusted demand forecast** page, the cells for the frozen buckets are disabled, to give a visual indication that those values should not be changed.</span></span> 

<span data-ttu-id="729a1-119">ベースライン需要予測の開始日は、現在の日付または将来の日付である必要はありません。</span><span class="sxs-lookup"><span data-stu-id="729a1-119">The start date for the baseline demand forecast doesn’t have to be the current date or a date in the future.</span></span> <span data-ttu-id="729a1-120">別の開始日を設定するには、**ベースライン予測開始日 - 開始日** フィールドを使用します。</span><span class="sxs-lookup"><span data-stu-id="729a1-120">To set a different start date, use the **Baseline forecast start date - From date** field.</span></span> <span data-ttu-id="729a1-121">たとえば、6 月に、翌年の予測を生成できます。</span><span class="sxs-lookup"><span data-stu-id="729a1-121">For example, in June, users can generate a forecast for the next year.</span></span> <span data-ttu-id="729a1-122">履歴需要およびベースラインの開始時の予測バケットが存在しないため、予測は正確ではない場合があります。</span><span class="sxs-lookup"><span data-stu-id="729a1-122">Because the forecast buckets between the end of historical demand and the start of the baseline are missing, the predictions might not be accurate.</span></span> <span data-ttu-id="729a1-123">需要予測サービスを使用している場合、欠落したギャップを埋める 4 つの方法があります。</span><span class="sxs-lookup"><span data-stu-id="729a1-123">If you are using the Demand forecasting service, there are four ways in which you can fill in the missing gaps.</span></span> <span data-ttu-id="729a1-124">**需要予測パラメーター** ページで、MISSING\_VALUE\_SUBSTITUTION のパラメーターを設定して使用する方法を選択できます。</span><span class="sxs-lookup"><span data-stu-id="729a1-124">You can choose the method that you want by setting the MISSING\_VALUE\_SUBSTITUTION parameter on the **Demand forecasting parameters** page.</span></span> 

> [!NOTE]
> <span data-ttu-id="729a1-125">欠落値の代入は、履歴データの開始日と終了日の間にあるデータのギャップに対してのみ有効です。</span><span class="sxs-lookup"><span data-stu-id="729a1-125">Missing value substitution only works for the gaps in data in between the start and end dates for historical data.</span></span> <span data-ttu-id="729a1-126">最後の物理データ ポイントの前または後にデータを入力するのではなく、実際の既存のデータポイント間の外挿としてのみ機能します。</span><span class="sxs-lookup"><span data-stu-id="729a1-126">It will not fill in data before or after the last physical data point, it only acts as extrapolation between actual existing data points.</span></span> 

<span data-ttu-id="729a1-127">**ベースラインの予測の開始日** - **開始日** フィールドは、予測バケットの先頭に設定する必要があります。たとえば、米国で予測バケットが週の場合、日曜日。</span><span class="sxs-lookup"><span data-stu-id="729a1-127">The **Baseline forecast start date** - **From date** field has to be set to the beginning of a forecast bucket, for example, in the United States, a Sunday if the forecasting bucket is the week.</span></span> <span data-ttu-id="729a1-128">システムは、**ベースライン予測の開始日** - **開始日** フィールドを、予測バケットの先頭に合わせて自動的に調整します。</span><span class="sxs-lookup"><span data-stu-id="729a1-128">The system automatically adjusts the **Baseline forecast start date** - **From date** field to match the beginning of a forecast bucket.</span></span> 

<span data-ttu-id="729a1-129">**ベースライン予測開始日** - **開始日** フィールドは、過去の日付に設定できます。</span><span class="sxs-lookup"><span data-stu-id="729a1-129">The **Baseline forecast start date** - **From date** field can be set to a date in in the past.</span></span> <span data-ttu-id="729a1-130">つまり、過去の需要予測を生成できます。</span><span class="sxs-lookup"><span data-stu-id="729a1-130">In other words, it is possible to generate a demand forecast in the past.</span></span> <span data-ttu-id="729a1-131">これはユーザーが予測サービス パラメーターを調整でき、過去に生成した統計予測を実際の履歴需要と一致できるため便利です。</span><span class="sxs-lookup"><span data-stu-id="729a1-131">This is useful, because it lets users adjust the forecast service parameters so that the statistical forecast generated in the past matches the actual historical demand.</span></span> <span data-ttu-id="729a1-132">ユーザーは、将来の統計ベースライン予測を生成する場合に、これらのパラメータの設定を使用できます。</span><span class="sxs-lookup"><span data-stu-id="729a1-132">Users can then continue using these parameter settings to generate a statistical baseline forecast for the future.</span></span> 

<span data-ttu-id="729a1-133">**手動調整を需要予測に転送** のチェック ボックスがオンの場合、新しい ベースライン予測に以前の需要予測繰り返しの手動調整を自動的に適用できます。</span><span class="sxs-lookup"><span data-stu-id="729a1-133">Manual adjustments made in previous demand forecasting iterations can be automatically applied to the new baseline forecast if the **Transfer manual adjustments to the demand forecas** t check box is selected.</span></span> <span data-ttu-id="729a1-134">チェック ボックスがオフの場合、手動調整がベースライン予測に追加されませんが、削除もされません。</span><span class="sxs-lookup"><span data-stu-id="729a1-134">If the check box is cleared, the manual adjustments are not added to the baseline forecast – but they are not deleted.</span></span> <span data-ttu-id="729a1-135">予測の手動調整は、予測のインポート時に **ベースライン需要予測に対して行われた手動調整の保存** のチェックボックスを オフにした場合にのみ、削除することができます。</span><span class="sxs-lookup"><span data-stu-id="729a1-135">Manual adjustments made to a forecast can be deleted only at forecast import time, by clearing the **Save the manual adjustments made to the baseline demand forecast** check box.</span></span> <span data-ttu-id="729a1-136">手動調整は認証時に保存されます。</span><span class="sxs-lookup"><span data-stu-id="729a1-136">Manual adjustments are saved at authorization time.</span></span> <span data-ttu-id="729a1-137">したがって、ユーザーが予測の手動調整を行い、Supply Chain Management で予測を承認しない場合は変更が失われます。</span><span class="sxs-lookup"><span data-stu-id="729a1-137">Therefore, if a user makes manual adjustments to the forecast, but doesn’t authorize the forecast back to Supply Chain Management, the changes are lost.</span></span> <span data-ttu-id="729a1-138">手動調整に関する詳細、および動作については、[調整された需要予測の承認](authorize-adjusted-forecast.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="729a1-138">For more information about manual adjustments and how they work, see [Authorize an adjusted forecast](authorize-adjusted-forecast.md).</span></span> 

<span data-ttu-id="729a1-139">需要予測の生成には、ユーザーが生成された予測を識別できるように、名前とコメントをつけられます。</span><span class="sxs-lookup"><span data-stu-id="729a1-139">A demand forecast generation can have a name and comments to help users identify the forecast that has been generated.</span></span> <span data-ttu-id="729a1-140">これらの値は、**統計ベースライン予測の生成履歴** ページの予測生成の履歴に表示されます。</span><span class="sxs-lookup"><span data-stu-id="729a1-140">These values are visible in forecast generation history on the **Statistical baseline forecast generation history** page.</span></span> 

<span data-ttu-id="729a1-141">会社間計画グループ、品目配賦キーおよびその他のフィルタは予測生成時に適用できます。</span><span class="sxs-lookup"><span data-stu-id="729a1-141">The intercompany planning group, item allocation keys, and other filters can be applied at forecast generation time.</span></span> <span data-ttu-id="729a1-142">これらはパフォーマンスの改善、または管理しやすいチャンクにデータを分割するのに使用できます。</span><span class="sxs-lookup"><span data-stu-id="729a1-142">These can be used to improve performance or to split the data into manageable chunks.</span></span> <span data-ttu-id="729a1-143">ただし品目配賦キーをクエリで選択した場合でも、会社間計画グループに関連付けられない品目配賦キーのメンバーに対して需要予測は生成されない事に、注意してください。</span><span class="sxs-lookup"><span data-stu-id="729a1-143">However, note that a demand forecast is not generated for the members of any item allocation key that is not associated with an intercompany planning group, even if the item allocation key is selected in the query.</span></span> 

> [!TIP]
> <span data-ttu-id="729a1-144">場合によっては、需要予測の生成中、または予測の生成がセッション ログなしで完了した際に、エラーが発生する場合があります。</span><span class="sxs-lookup"><span data-stu-id="729a1-144">Sometimes users might receive errors while generating a demand forecast, or forecast generation is completed with no session log.</span></span> <span data-ttu-id="729a1-145">これは、予測の生成に以前に使用されたクエリのデータが残っている場合に発生することがあります。</span><span class="sxs-lookup"><span data-stu-id="729a1-145">This can happen because of leftover data in the query that was previously used for forecast generation.</span></span> <span data-ttu-id="729a1-146">この問題を解決するには、**選択** をクリックして **クエリ** ページを開き、**リセット** を選択して、ベースライン予測を再生成します。</span><span class="sxs-lookup"><span data-stu-id="729a1-146">To resolve this issue, click **Select** to open the **Query** page, select **Reset**, and then regenerate the baseline forecast.</span></span> 

<span data-ttu-id="729a1-147">たとえば 1 つの品目または 1 つの品目配賦キーを一度に生成する場合など、大きい 1 つの品目の予測が生成されない場合や、パフォーマンスを向上させるために、**マスタ プラン - 設定 - 需要予測** - **需要予測のパラメーター - Azure Machine Learning** のタブで **要求応答モードの使用** のチェック ボックスを選択できます。</span><span class="sxs-lookup"><span data-stu-id="729a1-147">If the forecast is not generated for a big set of items, but, for example, for one item or one item allocation key at a time, then in order to get better performance, you can select the **Use request response mode** check box on the **Master planning - Setup - Demand forecasting** - **Demand forecasting parameters - Azure Machine Learning** tab.</span></span>

> [!NOTE]
> <span data-ttu-id="729a1-148">フラットである可能性のある予測は、履歴時間枠 (毎月の予測で 3 年間などのパターンを選択するために最低 3 つの期間) でなければならない履歴データが原因である可能性があります。</span><span class="sxs-lookup"><span data-stu-id="729a1-148">A potentially flat looking forecast can be due to the historical data that has to be of a longer historical timeframe (a minimum 3 of time periods in order to pick out patterns, such as 3 years with monthly forecast).</span></span> <span data-ttu-id="729a1-149">より良い結果を得るには、時間の範囲の粒度を変更するか、時間の範囲を増やします。</span><span class="sxs-lookup"><span data-stu-id="729a1-149">To get a better result, you can try changing the granularity of the time range or increase the time range.</span></span>

<a name="additional-resources"></a><span data-ttu-id="729a1-150">追加リソース</span><span class="sxs-lookup"><span data-stu-id="729a1-150">Additional resources</span></span>
--------

- [<span data-ttu-id="729a1-151">需要予測の設定</span><span class="sxs-lookup"><span data-stu-id="729a1-151">Demand forecasting setup</span></span>](demand-forecasting-setup.md)

- [<span data-ttu-id="729a1-152">ベースライン予測に対して手動調整を行う</span><span class="sxs-lookup"><span data-stu-id="729a1-152">Make manual adjustments to the baseline forecast</span></span>](manual-adjustments-baseline-forecast.md)

- [<span data-ttu-id="729a1-153">調整された需要予測の承認</span><span class="sxs-lookup"><span data-stu-id="729a1-153">Authorize an adjusted forecast</span></span>](authorize-adjusted-forecast.md)
