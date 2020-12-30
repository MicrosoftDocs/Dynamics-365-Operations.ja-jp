---
title: マスター プランのトラブルシューティング
description: このトピックでは、マスター プランを操作する際に発生する可能性がある問題の修正方法について説明します。
author: SmithaNataraj
manager: tfehr
ms.date: 11/04/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: smnatara
ms.search.validFrom: 2020-11-04
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: d1492854b7d2da480942800e378be9d2bb60bb1f
ms.sourcegitcommit: deb711c92251ed48cdf20ea514d03461c26a2262
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/25/2020
ms.locfileid: "4645068"
---
# <a name="troubleshoot-master-planning"></a><span data-ttu-id="e2d4f-103">マスター プランのトラブルシューティング</span><span class="sxs-lookup"><span data-stu-id="e2d4f-103">Troubleshoot master planning</span></span>

<span data-ttu-id="e2d4f-104">このトピックでは、マスター プランを操作する際に発生する可能性がある問題の修正方法について説明します。</span><span class="sxs-lookup"><span data-stu-id="e2d4f-104">This topic describes how to fix issues that you might encounter while you work with master planning.</span></span>

## <a name="bill-of-materials-explosion-behaves-differently-for-firmed-production-orders-and-for-estimated-production-orders-for-manually-created-work"></a><span data-ttu-id="e2d4f-105">部品表の展開は、確定した製造オーダーと、手動で作成された作業の見積製造オーダーの間で動作が異なります。</span><span class="sxs-lookup"><span data-stu-id="e2d4f-105">Bill of materials explosion behaves differently for firmed production orders and for estimated production orders for manually created work.</span></span>

### <a name="issue-description"></a><span data-ttu-id="e2d4f-106">問題の説明</span><span class="sxs-lookup"><span data-stu-id="e2d4f-106">Issue description</span></span>

<span data-ttu-id="e2d4f-107">製造オーダーを確定すると、部品表 (BOM) を展開しても品目が展開されません。</span><span class="sxs-lookup"><span data-stu-id="e2d4f-107">When a production order is firmed, the items aren't exploded when you explode the bill of materials (BOM).</span></span> <span data-ttu-id="e2d4f-108">ただし、手動で作業指示を作成してから製造オーダーを見積すると、品目が展開されます。</span><span class="sxs-lookup"><span data-stu-id="e2d4f-108">However, when you manually create a work order and then estimate the production order, the items are exploded.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="e2d4f-109">問題の解決</span><span class="sxs-lookup"><span data-stu-id="e2d4f-109">Issue resolution</span></span>

<span data-ttu-id="e2d4f-110">システムは正常に機能しています。</span><span class="sxs-lookup"><span data-stu-id="e2d4f-110">The system is working as expected.</span></span> <span data-ttu-id="e2d4f-111">製造オーダーが確定されたときに発生する展開は計画オーダーを指していますが、この場合、計画オーダーが現在確定されていることを示しているわけではありません。</span><span class="sxs-lookup"><span data-stu-id="e2d4f-111">The explosion that occurs when the production order is firmed will point to the planned order, but it doesn't appear that the planned order is currently firmed in this case.</span></span> <span data-ttu-id="e2d4f-112">ただし、製造オーダーが見積済みの場合は、計画オーダーが存在しないリリース済製造オーダーから展開が開始されます。</span><span class="sxs-lookup"><span data-stu-id="e2d4f-112">However, if the production order has been estimated, the explosion is triggered from the released production order where no planned order exists.</span></span>

## <a name="the-delay-value-isnt-updated-when-i-reschedule-a-planned-order"></a><span data-ttu-id="e2d4f-113">計画オーダーを再スケジューリングする場合、遅延値は更新されません。</span><span class="sxs-lookup"><span data-stu-id="e2d4f-113">The Delay value isn't updated when I reschedule a planned order.</span></span>

<span data-ttu-id="e2d4f-114">計画オーダーの遅延を更新するには、計画オーダーの **再スケジュール** ダイアログ ボックスを開きます。</span><span class="sxs-lookup"><span data-stu-id="e2d4f-114">To update the delay for planned orders, open the **Rescheduling** dialog box for the planned order.</span></span> <span data-ttu-id="e2d4f-115">**展開** クイック タブで、**再スケジュール後に展開を実行する** オプションが *はい* に設定されていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="e2d4f-115">On the **Explosion** FastTab, make sure that the **Perform explosion after rescheduling** option is set to *Yes*.</span></span>

## <a name="production-scheduling-doesnt-consider-the-safety-margins-that-are-set-on-the-item-coverage-for-pegged-supply"></a><span data-ttu-id="e2d4f-116">生産のスケジューリングでは、ペギングされた供給に対して品目補充で設定されている安全マージンは考慮されません。</span><span class="sxs-lookup"><span data-stu-id="e2d4f-116">Production scheduling doesn't consider the safety margins that are set on the item coverage for pegged supply.</span></span>

### <a name="issue-description"></a><span data-ttu-id="e2d4f-117">問題の説明</span><span class="sxs-lookup"><span data-stu-id="e2d4f-117">Issue description</span></span>

<span data-ttu-id="e2d4f-118">マスター プランでは安全マージンが考慮されます。</span><span class="sxs-lookup"><span data-stu-id="e2d4f-118">Master planning considers the safety margins.</span></span> <span data-ttu-id="e2d4f-119">ただし、計画製造オーダーのスケジューリング時に安全マージンは無視されます。</span><span class="sxs-lookup"><span data-stu-id="e2d4f-119">However, the safety margins are ignored when planned production orders are scheduled.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="e2d4f-120">問題の解決</span><span class="sxs-lookup"><span data-stu-id="e2d4f-120">Issue resolution</span></span>

<span data-ttu-id="e2d4f-121">マージンは、マスター プラン中にのみ考慮され、手動のスケジューリングでは考慮されません。</span><span class="sxs-lookup"><span data-stu-id="e2d4f-121">Margins are considered only during master planning, not during manual scheduling.</span></span> <span data-ttu-id="e2d4f-122">マージンは、計画フェーズでバッファーとして機能するように設計されており、実際のプロセスのために "マージン" を提供します。</span><span class="sxs-lookup"><span data-stu-id="e2d4f-122">Margins are designed to act as a buffer during the planning phase, to give some "margin" for the actual process.</span></span>

<span data-ttu-id="e2d4f-123">目的の結果を得るには、マージンを削除します。</span><span class="sxs-lookup"><span data-stu-id="e2d4f-123">To get the desired result, you can remove the margin.</span></span> <span data-ttu-id="e2d4f-124">次に、目的の時間 (待ち時間など) を含めるように工順を更新する必要があります。</span><span class="sxs-lookup"><span data-stu-id="e2d4f-124">The route must then be updated so that it includes the desired time (for example, as queue time).</span></span> <span data-ttu-id="e2d4f-125">その後、マスター プランと手動のスケジューリングの両方で同じ結果が生成される必要があります。</span><span class="sxs-lookup"><span data-stu-id="e2d4f-125">Both master planning and manual scheduling should then produce the same result.</span></span>

## <a name="planned-orders-are-generated-even-though-we-have-items-in-stock-and-production-orders-already-exist-for-them"></a><span data-ttu-id="e2d4f-126">在庫および製造オーダーの品目が既に存在している場合でも、計画オーダーが生成されます。</span><span class="sxs-lookup"><span data-stu-id="e2d4f-126">Planned orders are generated even though we have items in stock and production orders already exist for them.</span></span>

<span data-ttu-id="e2d4f-127">この問題を解決するには、**補充グループ** ページで該当するグループの **プラス在庫日数** の値を大きくします。</span><span class="sxs-lookup"><span data-stu-id="e2d4f-127">You might be able to fix this issue by increasing the **Positive days** value for the relevant groups on the **Coverage group** page.</span></span> <span data-ttu-id="e2d4f-128">この変更により、需要に手持在庫を使用できるかどうかがシステムによって判断されます。</span><span class="sxs-lookup"><span data-stu-id="e2d4f-128">This change will cause the system to determine whether on-hand inventory can be used for the demand.</span></span> <span data-ttu-id="e2d4f-129">この場合、在庫のある品目に対して新しい計画オーダーは生成されません。</span><span class="sxs-lookup"><span data-stu-id="e2d4f-129">Then a new planned order won't be generated for the items that are in stock.</span></span>

## <a name="master-planning-doesnt-seem-to-respect-capacity-limitations-and-is-scheduling-more-than-the-available-capacity"></a><span data-ttu-id="e2d4f-130">マスター プランがキャパシティ制限を考慮していないように見え、利用可能なキャパシティを超えてスケジューリングしています。</span><span class="sxs-lookup"><span data-stu-id="e2d4f-130">Master planning doesn't seem to respect capacity limitations and is scheduling more than the available capacity.</span></span>

### <a name="issue-description"></a><span data-ttu-id="e2d4f-131">問題の説明</span><span class="sxs-lookup"><span data-stu-id="e2d4f-131">Issue description</span></span>

<span data-ttu-id="e2d4f-132">有限キャパシティを持つ工程スケジューリングを使用していて、工順がリソース グループと個々のリソースの両方で混在する要件を指定している場合は、アルゴリズムがキャパシティ競合を検証する方法のため、予約超過の可能性が小さくなります。</span><span class="sxs-lookup"><span data-stu-id="e2d4f-132">When you use operation scheduling where there is finite capacity, and where the route specifies a mix of requirements for both a resource group and individual resources, there is a small chance of overbooking because of the way that the algorithm validates for capacity conflicts.</span></span> <span data-ttu-id="e2d4f-133">この予約超過は、ヘルパーを使用してマスター プランを実行するときに発生する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="e2d4f-133">This overbooking can occur when you use helpers to run master planning.</span></span> <span data-ttu-id="e2d4f-134">実行時間が比較的短いジョブが多数存在する場合に、この問題が発生する可能性が最も高くなります。</span><span class="sxs-lookup"><span data-stu-id="e2d4f-134">It's most likely to occur if there are many jobs that have a relatively short runtime.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="e2d4f-135">問題の解決</span><span class="sxs-lookup"><span data-stu-id="e2d4f-135">Issue resolution</span></span>

<span data-ttu-id="e2d4f-136">工程のスケジューリングに対して予約超過を行わないことが必須である場合、**マスター プラン パラメーター** ページで **工程のスケジューリングの正確な有限キャパシティ** オプションをオンにして、マスター プランのスケジューリングの一部を行うことができます。</span><span class="sxs-lookup"><span data-stu-id="e2d4f-136">If it's essential that no overbooking occur for operation scheduling, you can make the scheduling part of master planning single-threaded by turning on the **Accurate finite capacity for Operation Scheduling** option on the **Master planning parameters** page.</span></span> <span data-ttu-id="e2d4f-137">このオプションは、既定では使用できません。</span><span class="sxs-lookup"><span data-stu-id="e2d4f-137">This option isn't available by default.</span></span> <span data-ttu-id="e2d4f-138">この機能は、パーソナル化機能を使用してページに手動で追加する必要があります。</span><span class="sxs-lookup"><span data-stu-id="e2d4f-138">You must manually add it to the page by using personalization features.</span></span> <span data-ttu-id="e2d4f-139">このオプションを使用すると、並列処理が行われないため、スケジューリングの実行速度が遅くなります。</span><span class="sxs-lookup"><span data-stu-id="e2d4f-139">When you use this option, scheduling will run more slowly because of the lack of parallel processing.</span></span>

## <a name="planned-orders-take-a-long-time-to-update"></a><span data-ttu-id="e2d4f-140">計画オーダーの更新には長い時間がかかります。</span><span class="sxs-lookup"><span data-stu-id="e2d4f-140">Planned orders take a long time to update.</span></span>

### <a name="issue-description"></a><span data-ttu-id="e2d4f-141">問題の説明</span><span class="sxs-lookup"><span data-stu-id="e2d4f-141">Issue description</span></span>

<span data-ttu-id="e2d4f-142">計画オーダーの要求数量または出荷日、あるいはその両方を更新する場合、更新を保存するために、通常はオーダーあたり少なくとも 30 秒かかります。</span><span class="sxs-lookup"><span data-stu-id="e2d4f-142">When updating the requirement quantity and/or delivery date on a planned order, it typically takes at least 30 seconds per order to save the update.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="e2d4f-143">問題の解決</span><span class="sxs-lookup"><span data-stu-id="e2d4f-143">Issue resolution</span></span>

<span data-ttu-id="e2d4f-144">これは、組み込みのマスター プラン エンジンに関する既知の問題です。</span><span class="sxs-lookup"><span data-stu-id="e2d4f-144">This is a known issue with the built-in master planning engine.</span></span> <span data-ttu-id="e2d4f-145">編集中に BOM 構造を通じた基になる自動展開によって発生します。</span><span class="sxs-lookup"><span data-stu-id="e2d4f-145">It is caused by the underlying auto explosion through the BOM structure during edits.</span></span> <span data-ttu-id="e2d4f-146">この問題は、計画の最適化で修正されます。計画の最適化では、プランナーが関連するオーダーを更新および承認し、必要に応じて計画実行をトリガーして基になる BOM 構造の計画オーダーを更新できます。</span><span class="sxs-lookup"><span data-stu-id="e2d4f-146">This issue is addressed in Planning Optimization, where a planner can update and approve the relevant orders and, when desired, trigger a planning run to update planned orders for the underlying BOM structure.</span></span>

<span data-ttu-id="e2d4f-147">組み込みのマスター プラン エンジンを使用してパフォーマンスを向上させる方法の 1 つは、次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="e2d4f-147">One way to improve performance with the built-in master planning engine is to do the following:</span></span>

1. <span data-ttu-id="e2d4f-148">**マスター プラン \> 設定 \> プラン \> マスター プラン** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="e2d4f-148">Go to **Master planning \> Setup \> Plans \> Master plans**.</span></span>
1. <span data-ttu-id="e2d4f-149">プランを選択します。</span><span class="sxs-lookup"><span data-stu-id="e2d4f-149">Select a plan.</span></span>
1. <span data-ttu-id="e2d4f-150">**タイム フェンス (日)** クイックタブを展開します。</span><span class="sxs-lookup"><span data-stu-id="e2d4f-150">Expand the **Time fence in days** FastTab.</span></span>
1. <span data-ttu-id="e2d4f-151">**展開** を *はい* に設定し、この設定の下にあるフィールドを 0 (ゼロ) に設定します。</span><span class="sxs-lookup"><span data-stu-id="e2d4f-151">Set **Explosion** to *Yes*, and set the field below this setting to 0 (zero).</span></span>

> [!NOTE]
> <span data-ttu-id="e2d4f-152">これにより、このマスター プランに対して実行される展開の期間が 1 日に制限されます。</span><span class="sxs-lookup"><span data-stu-id="e2d4f-152">This will limit the period for explosions performed for this master plan to a single day.</span></span>
