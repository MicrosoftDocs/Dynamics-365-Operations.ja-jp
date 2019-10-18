---
title: マスター プランのセットアップ ウィザード
description: このトピックでは、マスター プランの設定に使用される各種重要な戦略およびパラメーターについて説明します。
author: t-benebo
manager: AnnBe
ms.date: 08/05/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: benebotg
ms.search.validFrom: 2019-05-31
ms.dyn365.ops.version: AX 10.0.0
ms.openlocfilehash: 0310ac55d35421d8ad9080739fc5a393660ce520
ms.sourcegitcommit: 261dc882710f29303b14f9be8a26d71d85d25345
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/17/2019
ms.locfileid: "1999537"
---
# <a name="master-planning-setup-wizard"></a><span data-ttu-id="85127-103">マスター プランのセットアップ ウィザード</span><span class="sxs-lookup"><span data-stu-id="85127-103">Master planning setup wizard</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="85127-104">このトピックでは、**マスター プランのセットアップ ウィザード**に関するガイドを提供します。</span><span class="sxs-lookup"><span data-stu-id="85127-104">This topic provides a guide for the **Master planning setup wizard**.</span></span> <span data-ttu-id="85127-105">パラメーターの提案が計算される方法について説明し、また異なる会社がマスター プラン パラメータ候補の計算方法について説明し、ビジネス ニーズに基づいてさまざまな企業がビジネス ニーズに基づいてマスター プランを設定する方法を示す例も示します。</span><span class="sxs-lookup"><span data-stu-id="85127-105">It explains how parameter suggestions are calculated and also provides examples that show how different companies set up master planning, based on their business needs.</span></span>

## <a name="specific-requirements-of-your-company"></a><span data-ttu-id="85127-106">会社の特定の要件</span><span class="sxs-lookup"><span data-stu-id="85127-106">Specific requirements of your company</span></span>

<span data-ttu-id="85127-107">ウィザードの最初のページで、会社の特定の要件について入力が求められます。</span><span class="sxs-lookup"><span data-stu-id="85127-107">The first page of the wizard asks about the specific requirements of your company.</span></span> <span data-ttu-id="85127-108">これらの質問に対する回答は正確である必要はありませんが、法人に対して存在する品目数と計画オーダーの大まかな概算値を提供できる必要があります。</span><span class="sxs-lookup"><span data-stu-id="85127-108">Your answers to these questions don't have to be exact, but you should be able to provide a rough approximation of the number of items and planned orders that there will be for the legal entity.</span></span> <span data-ttu-id="85127-109">回答は、選択したマスター プランだけでなく、法人に適用されるパラメーターを構成するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="85127-109">Your answers are used to configure parameters that apply to your legal entity, not just to the master plan that you selected.</span></span> <span data-ttu-id="85127-110">次のセクションでは、計算されるパラメーターと使用される式について説明します。</span><span class="sxs-lookup"><span data-stu-id="85127-110">The following sections describe the parameters that are calculated and the formulas that are used.</span></span>

### <a name="number-of-threads"></a><span data-ttu-id="85127-111">スレッド数</span><span class="sxs-lookup"><span data-stu-id="85127-111">Number of threads</span></span>

- <span data-ttu-id="85127-112">**品目のいずれかを製造する場合:** スレッド数 = 計画オーダー数 ÷ 1,000</span><span class="sxs-lookup"><span data-stu-id="85127-112">**If you manufacture any of the items:** Number of threads = Number of planned orders ÷ 1,000</span></span>
- <span data-ttu-id="85127-113">**品目のいずれかを製造するわけではない場合:** スレッド数 = 品目数 ÷ 1,000</span><span class="sxs-lookup"><span data-stu-id="85127-113">**If you don't manufacture any of the items:** Number of threads = Number of items ÷ 1,000</span></span>

<span data-ttu-id="85127-114">計算されるスレッド数が使用可能なスレッド数の 75% を超える場合、各顧客が使用可能なスレッド数の 75% に制限されます。</span><span class="sxs-lookup"><span data-stu-id="85127-114">If the number of threads that is calculated exceeds 75 percent of the available number of threads, it's capped at 75 percent of the number of threads that is available for each customer.</span></span> <span data-ttu-id="85127-115">(使用可能なスレッド数は、各顧客ごとに決定されます。)</span><span class="sxs-lookup"><span data-stu-id="85127-115">(The number of available threads will be determined for each customer.)</span></span>

<span data-ttu-id="85127-116">詳細については、[スレッド数](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/master-planning/master-planning-performance#number-of-threads) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="85127-116">For more information, see [Number of threads](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/master-planning/master-planning-performance#number-of-threads).</span></span>

### <a name="bundle-size"></a><span data-ttu-id="85127-117">バンドル サイズ</span><span class="sxs-lookup"><span data-stu-id="85127-117">Bundle size</span></span>

<span data-ttu-id="85127-118">バンドル サイズは **1** に設定されます。</span><span class="sxs-lookup"><span data-stu-id="85127-118">The bundle size will be set to **1**.</span></span> <span data-ttu-id="85127-119">この値は、マスター プランのパフォーマンスを改善するのに役立つため、多くの場合、最適な値です。</span><span class="sxs-lookup"><span data-stu-id="85127-119">This value is often the best value, because it helps improve the performance of master planning.</span></span>

<span data-ttu-id="85127-120">詳細については、[ヘルパー タスク バンドル内のタスク数](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/master-planning/master-planning-performance#number-of-tasks-in-helper-task-bundle) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="85127-120">For more information, see [Number of tasks in helper task bundle](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/master-planning/master-planning-performance#number-of-tasks-in-helper-task-bundle).</span></span>

### <a name="firming-bundle-size"></a><span data-ttu-id="85127-121">バンドル サイズを確定する</span><span class="sxs-lookup"><span data-stu-id="85127-121">Firming bundle size</span></span>

- <span data-ttu-id="85127-122">**品目のいずれかを製造する場合:** 確定バンドル サイズは、これら 2 つの値の大きい方の値に設定されます : **10** およびバンドル計算</span><span class="sxs-lookup"><span data-stu-id="85127-122">**If you manufacture any of the items:** The firming bundle size will be set to the larger of these two values: **10** and the bundle calculation</span></span>
- <span data-ttu-id="85127-123">**品目のいずれかを製造するわけではない場合 :** 確定バンドル サイズは、これら 2 つの値の大きい方の値に設定されます : **50** およびバンドル計算</span><span class="sxs-lookup"><span data-stu-id="85127-123">**If you don't manufacture any of the items:** The firming bundle size will be set to the larger of these two values: **50** and the bundle calculation</span></span>

<span data-ttu-id="85127-124">バンドル計算 = (計画オーダー数 × (確定タイム フェンス ÷ 補充タイム フェンス) ÷ スレッド数) ÷ 10</span><span class="sxs-lookup"><span data-stu-id="85127-124">Bundle calculation = (Number of planned orders × (Firming time fence ÷ Coverage time fence) ÷ Number of threads) ÷ 10</span></span>

### <a name="cache-size"></a><span data-ttu-id="85127-125">キャッシュ サイズ</span><span class="sxs-lookup"><span data-stu-id="85127-125">Cache size</span></span>

<span data-ttu-id="85127-126">キャッシュ サイズは、**最大**に設定されます。</span><span class="sxs-lookup"><span data-stu-id="85127-126">The cache size will be set to **Maximum**.</span></span> <span data-ttu-id="85127-127">この値は、マスター プランのパフォーマンスを改善するのに役立つため、多くの場合、最適な値です。</span><span class="sxs-lookup"><span data-stu-id="85127-127">This value is often the best value, because it helps improve the performance of master planning.</span></span>

<span data-ttu-id="85127-128">詳細については、[ジョブ バンドル内のジョブへの時間割り当て](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/production-control/allocate-time-jobs-job-bundle) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="85127-128">For more information, see [Allocate time to jobs in a job bundle](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/production-control/allocate-time-jobs-job-bundle).</span></span>

### <a name="manufacturing-setup"></a><span data-ttu-id="85127-129">製造の設定</span><span class="sxs-lookup"><span data-stu-id="85127-129">Manufacturing setup</span></span>

<span data-ttu-id="85127-130">品目を製造する場合、**製造の設定**ページがウィザードの後半で表示されます。</span><span class="sxs-lookup"><span data-stu-id="85127-130">If you manufacture items, a **Manufacturing setup** page will appear later in the wizard.</span></span>

## <a name="scope-of-the-current-plan"></a><span data-ttu-id="85127-131">現在の計画のスコープ</span><span class="sxs-lookup"><span data-stu-id="85127-131">Scope of the current plan</span></span>

<span data-ttu-id="85127-132">ウィザードの**現在の計画のスコープ** ページで、さまざまな要件が将来、マスター プランでどの程度考慮および計算されるかに関連する質問に答えます。</span><span class="sxs-lookup"><span data-stu-id="85127-132">On the **Scope of the current plan** page of the wizard, you answer questions that are related to how far in the future various requirements will be considered and calculated in master planning.</span></span> <span data-ttu-id="85127-133">各質問は、機能を使用するかどうか、そして機能を構成する方法を尋ねます。</span><span class="sxs-lookup"><span data-stu-id="85127-133">Each question asks whether you want to use a feature and how you want to configure it.</span></span>

<span data-ttu-id="85127-134">たとえば、予測計画機能の場合、ウィザードは「予測需要を満たす計画オーダーが提案されるように、マスター プランで予測計画を使用しますか」と尋ねます。</span><span class="sxs-lookup"><span data-stu-id="85127-134">For example, for the forecast plan feature, the wizard asks, "Do you want to use a forecast plan in master planning so that planned orders will be suggested to fulfill the forecasted demand?"</span></span>

<span data-ttu-id="85127-135">次のオプションを使用できます。</span><span class="sxs-lookup"><span data-stu-id="85127-135">The following options are available:</span></span>

- <span data-ttu-id="85127-136">**いいえ** – マスター プランは、予測を満たすための計画オーダーの提案はしません。</span><span class="sxs-lookup"><span data-stu-id="85127-136">**No** – Master planning won't suggest planned orders to fulfill a forecast.</span></span> <span data-ttu-id="85127-137">**マスター プラン** ページ (**マスター プラン \> 設定 \> 計画 \> マスター プラン**) の**タイム フェンス** タブで、ウィザードは**予測計画 (タイム フェンス)** オプションを**はい**に設定し、日数を **0** (ゼロ) に設定します。</span><span class="sxs-lookup"><span data-stu-id="85127-137">On the **Time fences** tab of the **Master plans** page (**Master planning \> Setup \> Plans \> Master plans**), the wizard will set the **Forecast plan (time fence)** option to **Yes** and set the number of days to **0** (zero).</span></span> <span data-ttu-id="85127-138">この設定は、補充グループで指定されたタイム フェンスを上書きします。</span><span class="sxs-lookup"><span data-stu-id="85127-138">This setup will override the time fence that is specified in the coverage group.</span></span> <span data-ttu-id="85127-139">日数が **0** (ゼロ) に設定されているため、この機能は使用されません。</span><span class="sxs-lookup"><span data-stu-id="85127-139">Because the number of days is set to **0** (zero), the feature won't be used.</span></span>
- <span data-ttu-id="85127-140">**はい、このマスター プランで定義されています** – 予測需要を満たすためにマスター プランが計画オーダーを提案する日数を入力できるフィールドが使用可能になります。</span><span class="sxs-lookup"><span data-stu-id="85127-140">**Yes, as defined in this master plan** – A field becomes available, where you can enter the number of days that master planning will suggest planned orders to fulfill the forecasted demand.</span></span> <span data-ttu-id="85127-141">ウィザードは**予測計画 (タイム フェンス)** オプションを**はい**に設定し、日数を**マスター プラン** ページの**タイム フェンス** タブにある**予測計画**フィールドに入力されている日数に設定します。</span><span class="sxs-lookup"><span data-stu-id="85127-141">The wizard will set the **Forecast plan (time fence)** option to **Yes** and set the number of days to the number of days that is entered in the **Forecast plan** field on the **Time fences** tab of the **Master plans** page.</span></span> <span data-ttu-id="85127-142">この設定により、補充グループで設定されている値が上書きされます。</span><span class="sxs-lookup"><span data-stu-id="85127-142">This setup will override the values that are set in the coverage groups.</span></span>
- <span data-ttu-id="85127-143">**はい、補充で定義されています** – ウィザードは**予測計画 (タイム フェンス)** オプションを**いいえ**に設定します。</span><span class="sxs-lookup"><span data-stu-id="85127-143">**Yes, as defined in the coverage** – The wizard will set the **Forecast plan (time fence)** option to **No**.</span></span> <span data-ttu-id="85127-144">補償グループで指定されたタイム フェンスは、予測の計画期間を指定するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="85127-144">The time fences that are specified in the coverage group will be used to specify how long you will plan for the forecast.</span></span>

<span data-ttu-id="85127-145">このページの残りの質問とその回答は、同じスキーマに従います。</span><span class="sxs-lookup"><span data-stu-id="85127-145">The remaining questions on this page and their answers follow the same schema:</span></span>

- <span data-ttu-id="85127-146">**いいえ** – **予測計画 (タイム フェンス)** オプションは**はい**に設定され、日数は **0** (ゼロ) に設定されます。</span><span class="sxs-lookup"><span data-stu-id="85127-146">**No** – The **Forecast plan (time fence)** option will be set to **Yes**, and the number of days will be set to **0** (zero).</span></span>
- <span data-ttu-id="85127-147">**はい、このマスター プランで定義されています** – **予測計画 (タイム フェンス)** オプションは**はい**に設定されます。</span><span class="sxs-lookup"><span data-stu-id="85127-147">**Yes, as defined in this master plan** – The **Forecast plan (time fence)** option will be set to **Yes**.</span></span> <span data-ttu-id="85127-148">入力した日数が使用され、補充グループで設定された値は上書きされます。</span><span class="sxs-lookup"><span data-stu-id="85127-148">The number of days that you enter will be used and will override the values that are set in the coverage groups.</span></span>
- <span data-ttu-id="85127-149">**はい、補充グループで定義されています** – **予測計画 (タイム フェンス)** オプションは**いいえ**に設定されます。</span><span class="sxs-lookup"><span data-stu-id="85127-149">**Yes, as defined in the coverage group** – The **Forecast plan (time fence)** option will be set to **No**.</span></span>

<span data-ttu-id="85127-150">詳細については、[ジョブのスケジューリング](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/production-control/job-scheduling) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="85127-150">For more information, see [Job scheduling](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/production-control/job-scheduling).</span></span>

## <a name="scheduling-options"></a><span data-ttu-id="85127-151">スケジューリング オプション</span><span class="sxs-lookup"><span data-stu-id="85127-151">Scheduling options</span></span>

<span data-ttu-id="85127-152">**スケジューリング オプション** ページは、「計画されている品目のいずれかを製造しますか？」に**はい**と答えた場合にのみ表示されます。</span><span class="sxs-lookup"><span data-stu-id="85127-152">The **Scheduling options** page appears only if you answered **Yes** to the "Do you manufacture any of the items planned?"</span></span> <span data-ttu-id="85127-153">ウィザードの最初のページの質問</span><span class="sxs-lookup"><span data-stu-id="85127-153">question on the first page of the wizard.</span></span>

<span data-ttu-id="85127-154">このページの最初の質問 (「個別のジョブに分割された工程をスケジュールする必要がありますか？」) に対する回答により、**マスター プラン** ページの**全般**タブ上にあるスケジューリング方法が決定されます。</span><span class="sxs-lookup"><span data-stu-id="85127-154">Your answer to the first question on this page ("Do you need to schedule operations divided into individual jobs?") determines the scheduling method on the **General** tab of the **Master plans** page.</span></span>

- <span data-ttu-id="85127-155">**はい** – ジョブのスケジューリングが使用されます。</span><span class="sxs-lookup"><span data-stu-id="85127-155">**Yes** – Job scheduling will be used.</span></span>
- <span data-ttu-id="85127-156">**いいえ** – 工程のスケジューリングが使用されます。</span><span class="sxs-lookup"><span data-stu-id="85127-156">**No** – Operations scheduling will be used.</span></span>

<span data-ttu-id="85127-157">詳細については、[工程のスケジューリング](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/production-control/operations-scheduling) および [ジョブのスケジューリング](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/production-control/job-scheduling) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="85127-157">For more information, see [Operations scheduling](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/production-control/operations-scheduling) and [Job scheduling](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/production-control/job-scheduling).</span></span>

## <a name="updates-of-demand-and-supply"></a><span data-ttu-id="85127-158">需要と供給の更新</span><span class="sxs-lookup"><span data-stu-id="85127-158">Updates of demand and supply</span></span>

<span data-ttu-id="85127-159">**需要と供給の更新** ページの質問は、確定、アクション メッセージ、および遅延に関連しています。</span><span class="sxs-lookup"><span data-stu-id="85127-159">The questions on the **Updates of demand and supply** page are related to firming, action messages, and delays.</span></span>

<span data-ttu-id="85127-160">マスター プランの設定は、前のセクションで説明されたものと同じスキーマにしたがい、回答に基づいて更新されます。</span><span class="sxs-lookup"><span data-stu-id="85127-160">The master planning setup will be updated based on your answers, according to the same schema that is described in the previous section:</span></span>

- <span data-ttu-id="85127-161">**いいえ** – **マスター プラン** ページの**タイム フェンス** オプションは**はい**に設定され、日数は **0** (ゼロ) に設定されます。</span><span class="sxs-lookup"><span data-stu-id="85127-161">**No** – The **Time fence** option on the **Master plans** page will be set to **Yes**, and the number of days will be set to **0** (zero).</span></span>
- <span data-ttu-id="85127-162">**はい、このマスター プランで定義されています** – **タイム フェンス** オプションは**はい**に設定されます。</span><span class="sxs-lookup"><span data-stu-id="85127-162">**Yes, as defined in this master plan** – The **Time fence** option will be set to **Yes**.</span></span> <span data-ttu-id="85127-163">入力した日数が使用され、補充グループで設定された値は上書きされます。</span><span class="sxs-lookup"><span data-stu-id="85127-163">The number of days that you enter will be used and will override the values that are set in the coverage groups.</span></span>
- <span data-ttu-id="85127-164">**はい、補充グループで定義されています** – **タイム フェンス** オプションは**いいえ**に設定されます。</span><span class="sxs-lookup"><span data-stu-id="85127-164">**Yes, as defined in the coverage group** – the **Time fence** option will be set to **No**.</span></span>

<span data-ttu-id="85127-165">計算済の遅延について、ウィザードの質問に対する回答により、**マスター プラン** ページの**計算済の遅延**タブ上にある対応するパラメーターが更新されます。</span><span class="sxs-lookup"><span data-stu-id="85127-165">For calculated delays, your answers to the questions in the wizard will update the corresponding parameters on the **Calculated delays** tab of the **Master plans** page.</span></span>

## <a name="summary-of-your-changes"></a><span data-ttu-id="85127-166">変更の集計</span><span class="sxs-lookup"><span data-stu-id="85127-166">Summary of your changes</span></span>

<span data-ttu-id="85127-167">ウィザードの最後のページには、応答に基づいて推奨される変更が表示されます。</span><span class="sxs-lookup"><span data-stu-id="85127-167">The last page of the wizard shows the changes that that are recommended based on your responses.</span></span> <span data-ttu-id="85127-168">セットアップした値 (**現在の設定**) と、ウィザードが推奨する値 (**新しい構成**) の両方が表示されます。</span><span class="sxs-lookup"><span data-stu-id="85127-168">It shows both the value in your setup (**Current setup**) and the value that the wizard recommends (**New configuration**).</span></span>

<span data-ttu-id="85127-169">新しいコンフィギュレーションのパラメーターを変更することもできます。</span><span class="sxs-lookup"><span data-stu-id="85127-169">You can also modify the parameters in the new configuration.</span></span> <span data-ttu-id="85127-170">パラメーターは、法人に適用されるパラメーターと、選択したマスター プランにのみ適用されるパラメーターに分けられます。</span><span class="sxs-lookup"><span data-stu-id="85127-170">The parameters are separated into parameters that apply to your legal entity and parameters that apply only to the master plan that you selected.</span></span> <span data-ttu-id="85127-171">ウィザードを使用して変更できるすべての設定パラメーターを表示するには、ページの下部にある**すべてのパラメーターを表示**を選択します。</span><span class="sxs-lookup"><span data-stu-id="85127-171">To view all the setup parameters that can be changed by using the wizard, select **Show all parameters** at the bottom of the page.</span></span> <span data-ttu-id="85127-172">その後、パラメーターを変更することができます。</span><span class="sxs-lookup"><span data-stu-id="85127-172">You can then change the parameters.</span></span>

<span data-ttu-id="85127-173">最後に、**完了**を選択すると、新しいコンフィギュレーションが適用されます。</span><span class="sxs-lookup"><span data-stu-id="85127-173">Finally, when you select **Finish**, the new configuration is applied.</span></span> <span data-ttu-id="85127-174">**キャンセル**を選択した場合、変更は適用されません。</span><span class="sxs-lookup"><span data-stu-id="85127-174">If you select **Cancel**, none of the changes are applied.</span></span>

## <a name="examples"></a><span data-ttu-id="85127-175">例</span><span class="sxs-lookup"><span data-stu-id="85127-175">Examples</span></span>

<span data-ttu-id="85127-176">このセクションでは、各業務のニーズにしたがって設定がどのように変化するかを示すために、2 つの架空の会社の設定について説明します。</span><span class="sxs-lookup"><span data-stu-id="85127-176">This section describes the setup of two fictional companies to show how the setup can change according to the needs of each business.</span></span>

### <a name="example-1-contoso-manufacturer"></a><span data-ttu-id="85127-177">例 1: コントソ マニュファクチャー</span><span class="sxs-lookup"><span data-stu-id="85127-177">Example 1: Contoso Manufacturer</span></span>

<span data-ttu-id="85127-178">コントソ マニュファクチャーはスピーカーを生産する製造会社です。</span><span class="sxs-lookup"><span data-stu-id="85127-178">Contoso Manufacturer is a manufacturing company that produces speakers.</span></span> <span data-ttu-id="85127-179">様々な仕入先から最終的にスピーカーに使用される様々な原材料やコンポーネントを購買します。</span><span class="sxs-lookup"><span data-stu-id="85127-179">It purchases the various raw materials and components that are used for the final speakers from various suppliers.</span></span> <span data-ttu-id="85127-180">供給と製造の特性を次に示します。</span><span class="sxs-lookup"><span data-stu-id="85127-180">Here are some of the characteristics of its supply and manufacturing:</span></span>

- <span data-ttu-id="85127-181">会社が製造する最終品目には、部品表 (BOM) 構造があります。</span><span class="sxs-lookup"><span data-stu-id="85127-181">The final items that the company manufactures have a bill of materials (BOM) structure.</span></span>
- <span data-ttu-id="85127-182">すべての最終品目とコンポーネントは、マスター プランによって計画されます。</span><span class="sxs-lookup"><span data-stu-id="85127-182">All final items and components are planned by master planning.</span></span> <span data-ttu-id="85127-183">手動計画は行われていません。</span><span class="sxs-lookup"><span data-stu-id="85127-183">Manual planning isn't done.</span></span>
- <span data-ttu-id="85127-184">工程の工順は、各最終品目の生産に対して定義されます。</span><span class="sxs-lookup"><span data-stu-id="85127-184">A route of operations is defined for the production of each final item.</span></span>
- <span data-ttu-id="85127-185">製造工場が最終品目を生産します。</span><span class="sxs-lookup"><span data-stu-id="85127-185">The manufacturing plant produces the final items.</span></span> <span data-ttu-id="85127-186">コンポーネントを処理するために使用されるフライス加工および穴あけ機械の数は定義されています。</span><span class="sxs-lookup"><span data-stu-id="85127-186">It has a defined number of milling and drilling machines that are used to process the components.</span></span> <span data-ttu-id="85127-187">様々なコンポーネントは、これらの機械によって処理される必要があります。</span><span class="sxs-lookup"><span data-stu-id="85127-187">The various components must be processed by these machines.</span></span>
- <span data-ttu-id="85127-188">多くの仕入先があります。</span><span class="sxs-lookup"><span data-stu-id="85127-188">There are many suppliers.</span></span> <span data-ttu-id="85127-189">品目ごとの平均リード タイムは 1 週間です。</span><span class="sxs-lookup"><span data-stu-id="85127-189">The average lead time for items is one week.</span></span> <span data-ttu-id="85127-190">同じ仕入先の品目グループのリード タイムは 7 週間です。</span><span class="sxs-lookup"><span data-stu-id="85127-190">A group of items from the same supplier will have a lead time of seven weeks.</span></span>

<span data-ttu-id="85127-191">ウィザードでは、次の値がコントソ マニュファクチャーに入力されます。</span><span class="sxs-lookup"><span data-stu-id="85127-191">In the wizard, the following values are entered for Contoso Manufacturer:</span></span>

- <span data-ttu-id="85127-192">**補充:**</span><span class="sxs-lookup"><span data-stu-id="85127-192">**Coverage:**</span></span>

    - <span data-ttu-id="85127-193">**質問:** 「計画期間の日数を指定しますか?」</span><span class="sxs-lookup"><span data-stu-id="85127-193">**Question:** "Do you want to specify the number of days of your planning horizon?"</span></span>
    - <span data-ttu-id="85127-194">**回答:** 「はい、補充グループで定義されています。」</span><span class="sxs-lookup"><span data-stu-id="85127-194">**Answer:** "Yes, as defined in the coverage groups."</span></span>

    <span data-ttu-id="85127-195">品目のリード タイムはまったく異なるため、コントソはすべての品目を将来の同じ期間に対して計画する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="85127-195">Because the lead time for items is very different, Contoso doesn't have to plan all the items for the same period in the future.</span></span> <span data-ttu-id="85127-196">品目の補充グループが作成されます。</span><span class="sxs-lookup"><span data-stu-id="85127-196">Coverage groups for the items are created.</span></span> <span data-ttu-id="85127-197">リード タイムが類似している品目は、同じ補充グループに割り当てられます。</span><span class="sxs-lookup"><span data-stu-id="85127-197">Items that have a similar lead time are assigned to the same coverage group.</span></span> <span data-ttu-id="85127-198">各補充グループの計画期間 (つまり、補充タイム フェンス) は、およそリード タイムに 1 週間のマージンを加えた長さです。</span><span class="sxs-lookup"><span data-stu-id="85127-198">The planning horizon for each coverage group (that is, the coverage time fence) is approximately the lead time plus a margin of one week.</span></span> <span data-ttu-id="85127-199">次に、マスター プランは、リード タイムに基づいて品目が事前に計画されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="85127-199">Master planning then makes sure that the items are planned in advance, based on their lead time.</span></span>

    <span data-ttu-id="85127-200">そのため、この例に対して 2 つの補充グループが作成されます。</span><span class="sxs-lookup"><span data-stu-id="85127-200">Therefore, two coverage groups will be created for this example.</span></span> <span data-ttu-id="85127-201">1 つの補充グループには 2 週間の補充タイム フェンスがあり、もう 1 つは 8 週間の補充タイム フェンスがあります。</span><span class="sxs-lookup"><span data-stu-id="85127-201">One coverage group will have a coverage time fence of two weeks, and the other will have a coverage time fence of eight weeks.</span></span>

    <span data-ttu-id="85127-202">**はい、このマスター プランで定義されています**が回答として選択されている場合、入力された日数は、すべての品目のうち最も長いリード タイムを超えている必要があります。</span><span class="sxs-lookup"><span data-stu-id="85127-202">If **Yes, as defined in this master plan** is selected as the answer, the number of days that is entered should exceed the longest lead time of all the items.</span></span> <span data-ttu-id="85127-203">ただし、これまでは複数の品目を事前に計画する必要がないため、複数の計画オーダーが計算されますが、使用されません。</span><span class="sxs-lookup"><span data-stu-id="85127-203">However, because many items don't have to be planned so far in advance, many planned orders will be calculated but never used.</span></span> <span data-ttu-id="85127-204">そのため、マスター プランのランタイムは増加します。</span><span class="sxs-lookup"><span data-stu-id="85127-204">Therefore, the master planning runtime will increase.</span></span>

- <span data-ttu-id="85127-205">**スケジューリング:**</span><span class="sxs-lookup"><span data-stu-id="85127-205">**Scheduling:**</span></span>

    - <span data-ttu-id="85127-206">**質問:** 「個別のジョブに分割された工程をスケジュールする必要がありますか?」</span><span class="sxs-lookup"><span data-stu-id="85127-206">**Question:** "Do you need to schedule operations divided into individual jobs?"</span></span>
    - <span data-ttu-id="85127-207">**回答:** 「はい。」</span><span class="sxs-lookup"><span data-stu-id="85127-207">**Answer:** "Yes."</span></span>

    <span data-ttu-id="85127-208">コントソ マニュファクチャーは、作業現場で実行される個別のジョブの計画およびスケジュールをする必要があります。</span><span class="sxs-lookup"><span data-stu-id="85127-208">Contoso Manufacturing must plan and schedule the individual jobs that will be performed on the shop floor.</span></span> <span data-ttu-id="85127-209">したがって、ジョブのスケジューリングを使用します。</span><span class="sxs-lookup"><span data-stu-id="85127-209">Therefore, it will use job scheduling.</span></span>

- <span data-ttu-id="85127-210">**能力:**</span><span class="sxs-lookup"><span data-stu-id="85127-210">**Capacity:**</span></span>

    - <span data-ttu-id="85127-211">**質問:** 「リソースの能力を使用してスケジュールしますか?」</span><span class="sxs-lookup"><span data-stu-id="85127-211">**Question:** "Do you want to schedule using the capacity of resources?"</span></span>
    - <span data-ttu-id="85127-212">**回答:** 「はい、このマスター プランで定義されています。」</span><span class="sxs-lookup"><span data-stu-id="85127-212">**Answer:** "Yes, as defined in this master plan."</span></span> <span data-ttu-id="85127-213">**10 日**が入力されます。</span><span class="sxs-lookup"><span data-stu-id="85127-213">**10 days** is entered.</span></span>

    <span data-ttu-id="85127-214">フライス加工および穴あけ機械の数は制限されています。</span><span class="sxs-lookup"><span data-stu-id="85127-214">The number of milling and drilling machines is limited.</span></span> <span data-ttu-id="85127-215">生産計画では、この制限を考慮し、リソースの能力にしたがってジョブを時間内に配置する必要があります。</span><span class="sxs-lookup"><span data-stu-id="85127-215">Production planning must take this limitation into account and arrange the jobs in time according to the capacity of the resources.</span></span> <span data-ttu-id="85127-216">つまり、スケジュールされているジョブは、リソースの制限に基づいて再計画されます。</span><span class="sxs-lookup"><span data-stu-id="85127-216">In other words, the jobs that are scheduled will be replanned based on the limitations of the resources.</span></span> <span data-ttu-id="85127-217">計画では、定義された期間に加えて、リード タイムが使用されます。</span><span class="sxs-lookup"><span data-stu-id="85127-217">Planning will use the lead time in addition to the period that is defined.</span></span> <span data-ttu-id="85127-218">(計画生産注文は重複することがあります) 品目の生産リード タイムは 7 日間であるため、マスター プランのリソース能力は 10 日間考慮されます。</span><span class="sxs-lookup"><span data-stu-id="85127-218">(Planned production orders can overlap.) Because the production lead time for the items is seven days, the capacity of the resources for master planning will be considered during 10 days.</span></span>

- <span data-ttu-id="85127-219">**優先順位:**</span><span class="sxs-lookup"><span data-stu-id="85127-219">**Sequencing:**</span></span>

    - <span data-ttu-id="85127-220">**質問:** 「生産順序の値を使用して計画オーダーの順序付けを行いますか?」</span><span class="sxs-lookup"><span data-stu-id="85127-220">**Question:** "Do you want to sequence planned orders using the product's sequence values?"</span></span>
    - <span data-ttu-id="85127-221">**回答:** 「はい、補充グループで定義されています。」</span><span class="sxs-lookup"><span data-stu-id="85127-221">**Answer:** "Yes, as defined in the coverage groups."</span></span>

    <span data-ttu-id="85127-222">工順は、各最終品目の生産に対して定義されます。</span><span class="sxs-lookup"><span data-stu-id="85127-222">A route is defined for the production of each final item.</span></span> <span data-ttu-id="85127-223">そのため、マスター プランは、定義された工順に従って注文を時間内にスケジュールします。</span><span class="sxs-lookup"><span data-stu-id="85127-223">Therefore, master planning will schedule the orders in time according to the defined routes.</span></span>

- <span data-ttu-id="85127-224">**展開:**</span><span class="sxs-lookup"><span data-stu-id="85127-224">**Explosion:**</span></span>

    - <span data-ttu-id="85127-225">**質問:** 「部品表のすべての要素の注文を計画 (すべての親アイテムおよびすべての子アイテムを計画) しますか?」</span><span class="sxs-lookup"><span data-stu-id="85127-225">**Question:** "Do you want to plan orders for all the elements in a Bill of Materials (plan for the parent and all children items)?"</span></span>
    - <span data-ttu-id="85127-226">**回答:** 「はい、補充グループで定義されています。」</span><span class="sxs-lookup"><span data-stu-id="85127-226">**Answer:** "Yes, as defined in the coverage groups."</span></span>

    <span data-ttu-id="85127-227">生産に使用するすべての品目を計画する必要があります。</span><span class="sxs-lookup"><span data-stu-id="85127-227">All the items that are used for the production must be planned.</span></span> <span data-ttu-id="85127-228">品目のリード タイムはまったく異なるため、補充グループを使用する場合は、マスター プランのパフォーマンスが向上します。</span><span class="sxs-lookup"><span data-stu-id="85127-228">Because the items have very different lead times, master planning will have better performance when it uses the coverage groups.</span></span> <span data-ttu-id="85127-229">再度、1 週間のマージンを入力し、補充と同じ時間で展開を行うことができます。</span><span class="sxs-lookup"><span data-stu-id="85127-229">Again, a margin of one week can be entered, and explosion can be done for the same time as the coverage.</span></span>

### <a name="example-2-contoso-retailer"></a><span data-ttu-id="85127-230">例 2: コントソ リテーラー</span><span class="sxs-lookup"><span data-stu-id="85127-230">Example 2: Contoso Retailer</span></span>

<span data-ttu-id="85127-231">コントソ リテーラーは、ファッション産業の流通会社です。</span><span class="sxs-lookup"><span data-stu-id="85127-231">Contoso Retailer is a distribution company in the fashion industry.</span></span> <span data-ttu-id="85127-232">売上予測に基づいて発注書を発行する必要がある場合、マスター プランを使用して計算します。</span><span class="sxs-lookup"><span data-stu-id="85127-232">It uses master planning to calculate when purchase orders should be placed, based on its forecasted sales.</span></span> <span data-ttu-id="85127-233">次にその特性の一部を説明します。</span><span class="sxs-lookup"><span data-stu-id="85127-233">Here are some of its characteristics:</span></span>

- <span data-ttu-id="85127-234">コントソ リテーラーは、需要予測を使用して売上を予測します。</span><span class="sxs-lookup"><span data-stu-id="85127-234">Contoso Retailer uses a demand forecast to predict sales.</span></span> <span data-ttu-id="85127-235">発注書は予測に従って計画されます。</span><span class="sxs-lookup"><span data-stu-id="85127-235">Purchase orders will be planned according to the forecast.</span></span>
- <span data-ttu-id="85127-236">小売店舗では、補充に要求を使用します。</span><span class="sxs-lookup"><span data-stu-id="85127-236">Retail stores use requisitions for replenishment.</span></span>
- <span data-ttu-id="85127-237">主要倉庫から各店舗までのリード タイムは、すべての商品について、約 2 週間です。</span><span class="sxs-lookup"><span data-stu-id="85127-237">The lead time from the main warehouse to each store is approximately two weeks for all items.</span></span>

<span data-ttu-id="85127-238">ウィザードでは、次の値がコントソ リテーラーに入力されます。</span><span class="sxs-lookup"><span data-stu-id="85127-238">In the wizard, the following values are entered for Contoso Retailer:</span></span>

- <span data-ttu-id="85127-239">**需要の予測:**</span><span class="sxs-lookup"><span data-stu-id="85127-239">**Forecast demand:**</span></span>

    - <span data-ttu-id="85127-240">**質問:** 「予測された需要を満たすための計画オーダーが提案されるように、マスター プランで予測計画を使用しますか ?」</span><span class="sxs-lookup"><span data-stu-id="85127-240">**Question:** "Do you want to use a forecast plan in master planning so that planned orders will be suggested to fulfill the forecasted demand?"</span></span>
    - <span data-ttu-id="85127-241">**回答:** 「はい、このマスター プランで定義されています。」</span><span class="sxs-lookup"><span data-stu-id="85127-241">**Answer:** "Yes, as defined in this master plan."</span></span>

    <span data-ttu-id="85127-242">コントソは売上を予測する需要予測が含んでいます。</span><span class="sxs-lookup"><span data-stu-id="85127-242">Contoso has included a demand forecast to predict its sales.</span></span> <span data-ttu-id="85127-243">そのため、マスター プランは、予測を満たすための計画オーダーを推奨する必要があります。</span><span class="sxs-lookup"><span data-stu-id="85127-243">Therefore, master planning must recommend planned orders to fulfill the forecast.</span></span>

- <span data-ttu-id="85127-244">**確定:**</span><span class="sxs-lookup"><span data-stu-id="85127-244">**Firming:**</span></span>

    - <span data-ttu-id="85127-245">**質問:** 「生産や発注書などについて、マスター プランにより計画オーダーを発注書ドキュメントに自動的に確定させますか?」</span><span class="sxs-lookup"><span data-stu-id="85127-245">**Question:** "Do you want master planning to automatically firm planned orders into order documents, for example production or purchase orders?"</span></span>
    - <span data-ttu-id="85127-246">**回答:** 「はい、このマスター プランで定義されています。」</span><span class="sxs-lookup"><span data-stu-id="85127-246">**Answer:** "Yes, as defined in this master plan."</span></span> <span data-ttu-id="85127-247">**1 日**が入力されます。</span><span class="sxs-lookup"><span data-stu-id="85127-247">**1 day** is entered.</span></span>

    <span data-ttu-id="85127-248">コントソ リテーラーは計画発注書から発注書を直接作成するため、計画発注書が自動的に確定されるなら便利です。</span><span class="sxs-lookup"><span data-stu-id="85127-248">Because Contoso Retailer will create purchase orders directly from the planned purchase orders, it's useful if the planned purchase orders are automatically firmed.</span></span> <span data-ttu-id="85127-249">会社はマスター プランを毎日実行しているので、1 日の確定タイム フェンスにより、翌日に必要なすべての注文が自動的に確定されます。</span><span class="sxs-lookup"><span data-stu-id="85127-249">Because the company runs master planning every day, a firming time fence of one day will automatically firm all the orders that are required for the next day.</span></span>

- <span data-ttu-id="85127-250">**承認された要求:**</span><span class="sxs-lookup"><span data-stu-id="85127-250">**Approved requisitions:**</span></span>

    - <span data-ttu-id="85127-251">**質問:** 「小売店舗に補充するため、承認された要求から需要を含めますか?」</span><span class="sxs-lookup"><span data-stu-id="85127-251">**Question:** "Do you want to include demand from approved requisitions to replenish retail stores?"</span></span>
    - <span data-ttu-id="85127-252">**回答:** 「はい、このマスター プランで定義されています。」</span><span class="sxs-lookup"><span data-stu-id="85127-252">**Answer:** "Yes, as defined in this master plan."</span></span> <span data-ttu-id="85127-253">**1 日**が入力されます。</span><span class="sxs-lookup"><span data-stu-id="85127-253">**1 day** is entered.</span></span>

    <span data-ttu-id="85127-254">コントソは、小売店舗からの承認された要求を使用して、それらの店舗を補充するための計画発注書を作成します。</span><span class="sxs-lookup"><span data-stu-id="85127-254">Contoso uses the approved requisitions from its retail stores to create planned purchase orders to replenish those stores.</span></span> <span data-ttu-id="85127-255">マスター プランは毎日実行されるため、最終日からの要求が計画に含められます。</span><span class="sxs-lookup"><span data-stu-id="85127-255">Because master planning is run every day, the requisitions from the last day will be included in the planning.</span></span>
