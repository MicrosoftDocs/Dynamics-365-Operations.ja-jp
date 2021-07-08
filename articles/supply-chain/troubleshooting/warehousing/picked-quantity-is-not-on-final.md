---
title: 品目がピッキングされていないため、出荷を確認できない
description: 品目がピッキングされていないため、出荷を確認できない
author: perlynne
ms.date: 04/21/2021
ms.topic: troubleshooting
ms.search.form: WHSLoadTable_WHSShipConfirm,WHSLoadPlanningListPage_WHSShipConfirm,WHSLoadPlanningWorkbench_WHSShipConfirm,WHSTransportLoad_WHSShipConfirm,WHSShipPlanningListPage_WHSShipConfirm,WHSShipmentDetails_WHSShipConfirm,WHSWorkTable_WHSShipConfirm,WHSWorkTableListPage_WHSShipConfirm,Dialog_WHSOutboundShipConfirmController_WHSOutboundShipConfirm
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: lbc
ms.search.validFrom: 2021-04-21
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: f3ebd47ffc85d4ca257b404579d60d679f7929b6
ms.sourcegitcommit: f9b145ef4a81cec81f420871b4130b05db4f4500
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/23/2021
ms.locfileid: "6301308"
---
# <a name="you-cant-confirm-a-shipment-because-items-havent-been-picked"></a><span data-ttu-id="389a0-103">品目がピッキングされていないため、出荷を確認できない</span><span class="sxs-lookup"><span data-stu-id="389a0-103">You can't confirm a shipment because items haven't been picked</span></span>

<span data-ttu-id="389a0-104">エラー コード: LoadNotPickedAndMovedToFinalShippingLocation</span><span class="sxs-lookup"><span data-stu-id="389a0-104">Error code: LoadNotPickedAndMovedToFinalShippingLocation</span></span>

## <a name="symptoms"></a><span data-ttu-id="389a0-105">現象</span><span class="sxs-lookup"><span data-stu-id="389a0-105">Symptoms</span></span>

<span data-ttu-id="389a0-106">出荷を確認しようとすると、次のエラー メッセージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="389a0-106">When you try to confirm a shipment, the system shows the following error message:</span></span>

> <span data-ttu-id="389a0-107">積荷 %1 に必要な一部の品目がまだピッキングされておらず、最終出荷場所に移動されていません。</span><span class="sxs-lookup"><span data-stu-id="389a0-107">Some of the items that are needed for load %1 have not yet been picked and moved to the final shipping location.</span></span>

<span data-ttu-id="389a0-108">したがって、積荷の出荷を確認できません。</span><span class="sxs-lookup"><span data-stu-id="389a0-108">Therefore, you can't confirm the shipment for the load.</span></span>

## <a name="cause"></a><span data-ttu-id="389a0-109">原因</span><span class="sxs-lookup"><span data-stu-id="389a0-109">Cause</span></span>

<span data-ttu-id="389a0-110">次のいずれかの条件が存在する可能性があるため、現在の状態では積荷または出荷を確認できません:</span><span class="sxs-lookup"><span data-stu-id="389a0-110">The load or shipment can't be confirmed in its current state because one of the following conditions might exist:</span></span>

- <span data-ttu-id="389a0-111">関連する作業がまだ選択されていないので、最終的な出荷場所に移動されていません。</span><span class="sxs-lookup"><span data-stu-id="389a0-111">The related work hasn't yet been picked and moved to the final shipping location.</span></span>
- <span data-ttu-id="389a0-112">作業のピッキング済数量が、積荷明細行で作成された作業数量と一致しません。</span><span class="sxs-lookup"><span data-stu-id="389a0-112">The picked work quantity doesn't match the created work quantity on the load line.</span></span>
- <span data-ttu-id="389a0-113">ウェーブ テンプレートのコンテナー詰めの使用中に、梱包場所を最終的な出荷場所として使用して、場所のディレクティブが構成されました。</span><span class="sxs-lookup"><span data-stu-id="389a0-113">The location directive has been configured with packing location as the final shipping location while using Wave template containerization.</span></span>

## <a name="resolution"></a><span data-ttu-id="389a0-114">解決策</span><span class="sxs-lookup"><span data-stu-id="389a0-114">Resolution</span></span>

<span data-ttu-id="389a0-115">積荷または出荷は現在、出荷確認に失敗した状態になっています。</span><span class="sxs-lookup"><span data-stu-id="389a0-115">The load or shipment is currently in a state where shipment confirmation fails.</span></span> <span data-ttu-id="389a0-116">この問題を解決するには、次のいずれかのタスクを実行します。</span><span class="sxs-lookup"><span data-stu-id="389a0-116">To fix this issue, complete one of the following tasks:</span></span>

- <span data-ttu-id="389a0-117">積荷明細行を確認し、関連するすべての作業が最後の出荷場所で完了し、数量も一致していることを確認します。</span><span class="sxs-lookup"><span data-stu-id="389a0-117">Review your load lines and make sure that all the related work has been completed at the final shipping location, and that the quantities match.</span></span>
- <span data-ttu-id="389a0-118">最終的な出荷場所として梱包場所を使用するように作成した作業 ID をキャンセルし、場所のディレクティブを変更し、積荷を再リリースします。</span><span class="sxs-lookup"><span data-stu-id="389a0-118">Cancel the work IDs that have been created with the packing location as the final shipping location, reconfigure the location directive, and rerelease the load.</span></span>

### <a name="review-your-load-lines-and-make-sure-that-all-the-related-work-has-been-completed-at-the-final-shipping-location-and-that-the-quantities-match"></a><span data-ttu-id="389a0-119">積荷明細行を確認し、関連するすべての作業が最後の出荷場所で完了し、数量も一致していることを確認します</span><span class="sxs-lookup"><span data-stu-id="389a0-119">Review your load lines and make sure that all the related work has been completed at the final shipping location, and that the quantities match</span></span>

<span data-ttu-id="389a0-120">次の手順を使用して積荷明細行を確認し、関連するすべての作業が最後の出荷場所で完了し、数量も一致していることを確認します。</span><span class="sxs-lookup"><span data-stu-id="389a0-120">Use the following procedure to review your load lines and make sure that all the related work has been completed at the final shipping location, and that the quantities match.</span></span>

1. <span data-ttu-id="389a0-121">**倉庫管理 \> 積荷 \> すべての積荷** に移動します。</span><span class="sxs-lookup"><span data-stu-id="389a0-121">Go to **Warehouse management \> Loads \> All loads**.</span></span>
1. <span data-ttu-id="389a0-122">発送が確認できない積荷を選択します。</span><span class="sxs-lookup"><span data-stu-id="389a0-122">Select the load that the shipment can't be confirmed for.</span></span>
1. <span data-ttu-id="389a0-123">**積荷明細行** クイックタブで、積荷明細行を選択します。</span><span class="sxs-lookup"><span data-stu-id="389a0-123">On the **Load lines** FastTab, select the load line.</span></span>
1. <span data-ttu-id="389a0-124">**作業作成数量** フィールドの値を記録します。</span><span class="sxs-lookup"><span data-stu-id="389a0-124">Make a note of the value of the **Work created quantity** field.</span></span>
1. <span data-ttu-id="389a0-125">アクション ウィンドウの、**積荷** タブの、**関連情報** グループで、**作業** を選択します。</span><span class="sxs-lookup"><span data-stu-id="389a0-125">On the Action Pane, on the **Loads** tab, in the **Related information** group, select **Work**.</span></span>
1. <span data-ttu-id="389a0-126">作業が最後の出荷場所で完了し、作業のピッキング済数量が積荷明細行で作成された作業数量と一致していることを確認します。</span><span class="sxs-lookup"><span data-stu-id="389a0-126">Verify that the work has been completed at the final shipping location, and that the picked work quantity matches the created work quantity on the load line.</span></span>
1. <span data-ttu-id="389a0-127">すべての積荷明細行に対してこの手順を繰り返して、すべての基準が満たされていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="389a0-127">Repeat this procedure for all load lines to make sure that all criteria are met.</span></span>

### <a name="cancel-the-work-ids-that-have-been-created-with-the-packing-location-as-the-final-shipping-location-reconfigure-the-location-directive-and-rerelease-the-load"></a><span data-ttu-id="389a0-128">最終的な出荷場所として梱包場所を使用するように作成した作業 ID をキャンセルし、場所のディレクティブを変更し、積荷を再リリースする</span><span class="sxs-lookup"><span data-stu-id="389a0-128">Cancel the work IDs that have been created with the packing location as the final shipping location, reconfigure the location directive, and rerelease the load</span></span>

<span data-ttu-id="389a0-129">次の手順を使用して、梱包場所を自動コンテナ詰めが設定された最終的な配置場所とする作業 ID をキャンセルします。</span><span class="sxs-lookup"><span data-stu-id="389a0-129">Use the following procedure to cancel the work IDs that have the packing location as the final put location with automated containerization in place.</span></span>

1. <span data-ttu-id="389a0-130">**倉庫管理 \> 定期処理のタスク \> クリーンアップ \> 作業のキャンセル** の順に移動します。</span><span class="sxs-lookup"><span data-stu-id="389a0-130">Go to **Warehouse management \> Periodic tasks \> Clean up \> Cancel work**.</span></span>
1. <span data-ttu-id="389a0-131">**作業のキャンセル** ダイアログ ボックスが開きます。</span><span class="sxs-lookup"><span data-stu-id="389a0-131">The **Cancel work** dialog opens.</span></span> <span data-ttu-id="389a0-132">**作業 ID** フィールドで、キャンセルする作業の ID を指定します。</span><span class="sxs-lookup"><span data-stu-id="389a0-132">In the **Work ID** field, specify the ID of the work that you want to cancel.</span></span> <span data-ttu-id="389a0-133">選択した作業 ID は、**作業状態** の値が *開く*、*処理中*、*処理済*、*結合済*、または *クローズ済* であることが必要です。</span><span class="sxs-lookup"><span data-stu-id="389a0-133">The selected work ID must have a **Work status** value of *Open*, *In progress*, *Canceled*, *Combined*, or *Closed*.</span></span>
1. <span data-ttu-id="389a0-134">**OK** を選択します。</span><span class="sxs-lookup"><span data-stu-id="389a0-134">Select **OK**.</span></span>
1. <span data-ttu-id="389a0-135">**はい** を選択して、作業をキャンセルすることを確認します。</span><span class="sxs-lookup"><span data-stu-id="389a0-135">Select **Yes** to confirm that you want to cancel the work.</span></span>
1. <span data-ttu-id="389a0-136">必要に応じて他の作業 ID に対して、この手順を繰り返します。</span><span class="sxs-lookup"><span data-stu-id="389a0-136">Repeat this procedure for the other work IDs as needed.</span></span>

<span data-ttu-id="389a0-137">詳細については、[例外処理のために倉庫作業をキャンセル](../../warehousing/cancel-warehouse-work.md) を参照してください。</span><span class="sxs-lookup"><span data-stu-id="389a0-137">For more information, see [Cancel warehouse work for exception handling](../../warehousing/cancel-warehouse-work.md).</span></span>

<span data-ttu-id="389a0-138">次の手順に従って、自動コンテナ詰めがウェーブ テンプレートに設定されているときに、梱包場所を最終的な出荷場所として使用しないよう、場所のディレクティブを再構成します。</span><span class="sxs-lookup"><span data-stu-id="389a0-138">Use the following procedure to reconfigure the location directive so it won't use the packing location as the final shipping location when automated containerization is set up for the wave template.</span></span>

1. <span data-ttu-id="389a0-139">**倉庫管理 \> 設定 \> 場所のディレクティブ** に移動します。</span><span class="sxs-lookup"><span data-stu-id="389a0-139">Go to **Warehouse management \> Setup \> Location directives**.</span></span>
1. <span data-ttu-id="389a0-140">**ワーク オーダー タイプ** フィールドで、*販売注文* を選択します。</span><span class="sxs-lookup"><span data-stu-id="389a0-140">In the **Work order type** field, select *Sales orders*.</span></span>
1. <span data-ttu-id="389a0-141">自動コンテナ詰めに使用している場所のディレクティブを選択します。</span><span class="sxs-lookup"><span data-stu-id="389a0-141">Select the location directive you are using for automated containerization.</span></span>
1. <span data-ttu-id="389a0-142">**場所ディレクティブ アクション** クイックタブ ツールバーで、**クエリの編集** を選択します。</span><span class="sxs-lookup"><span data-stu-id="389a0-142">On the **Location Directive Actions** FastTab toolbar, select **Edit query**.</span></span>
1. <span data-ttu-id="389a0-143">クエリ エディター ダイアログボックスの **範囲** タブで、**フィールド** が *場所プロファイル* に設定されている行を検索し、その行の **基準** フィールドが **場所タイプ** が *梱包* である場所プロファイルに設定されていないか確認します。</span><span class="sxs-lookup"><span data-stu-id="389a0-143">In the query editor dialog, on the **Range** tab, find the row where **Field** is set to *Location profile*, and verify that the **Criteria** field for that row is not set to a location profile that has a **Location type** of *Packing*.</span></span> <span data-ttu-id="389a0-144">**基準** フィールドを調整し、最終的な配置場所を修正します。</span><span class="sxs-lookup"><span data-stu-id="389a0-144">Adjust the **Criteria** field to correct the final put location.</span></span>

<span data-ttu-id="389a0-145">次の手順を使用して積荷を再リリースし、最終的な出荷場所が正しい作業 ID を作成します。</span><span class="sxs-lookup"><span data-stu-id="389a0-145">Use the following procedure to rerelease the load and create work IDs with the correct final shipping location.</span></span>

1. <span data-ttu-id="389a0-146">**倉庫管理 \> 積荷 \> 積荷計画ワークベンチ** に移動します。</span><span class="sxs-lookup"><span data-stu-id="389a0-146">Go to **Warehouse management \> Loads \> Load planning workbench**.</span></span>
1. <span data-ttu-id="389a0-147">**積荷** セクションで、リリースする必要がある積荷を検索します。</span><span class="sxs-lookup"><span data-stu-id="389a0-147">In the **Loads** section, find the load that needs to be released.</span></span>
1. <span data-ttu-id="389a0-148">**積荷** セクションのツールバーで、**リリース \> 倉庫へのリリース** を選択し、選択した積荷を倉庫にリリースします。</span><span class="sxs-lookup"><span data-stu-id="389a0-148">On the **Loads** section toolbar, select **Release \> Release to warehouse** to release the selected load to the warehouse.</span></span>
1. <span data-ttu-id="389a0-149">必要に応じて他の積荷に対して、この手順を繰り返します。</span><span class="sxs-lookup"><span data-stu-id="389a0-149">Repeat this procedure for the other loads as needed.</span></span>
