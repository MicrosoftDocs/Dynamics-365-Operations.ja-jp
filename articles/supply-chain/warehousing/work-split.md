---
title: 作業の分割
description: このトピックでは、作業分割機能に関する情報を提供します。 この機能を使用すると、複数の作業オーダーをいくつかの小さな作業オーダーに分割し、その後で複数の倉庫作業者に割り当てることができます。 これにより、複数の倉庫作業者が同じ作業を同時に選択できるようになります。
author: mirzaab
manager: tfehr
ms.date: 10/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.search.industry: WHSWorkTableListPage
ms.author: mirzaab
ms.search.validFrom: 2020-10-15
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: e74b630e72d70829938f0f34efd624509b1ba7c3
ms.sourcegitcommit: 531be324bf706ca727d777720df899d6ddd3c2d7
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/05/2020
ms.locfileid: "4432437"
---
# <a name="work-split"></a><span data-ttu-id="4d355-105">作業の分割</span><span class="sxs-lookup"><span data-stu-id="4d355-105">Work split</span></span>

<span data-ttu-id="4d355-106">作業分割機能を使用すると、複数の作業 ID (複数の行を含む作業順序) をいくつかの小さな作業 ID に分割し、それを複数の倉庫作業者に割り当てることができます。</span><span class="sxs-lookup"><span data-stu-id="4d355-106">Work split functionality lets you split large work IDs (that is, work orders that have several lines) into several smaller work IDs that you can then assign to multiple warehouse workers.</span></span> <span data-ttu-id="4d355-107">このように、複数の倉庫作業者が同じ作業作成番号を同時にピッキングすることができます。</span><span class="sxs-lookup"><span data-stu-id="4d355-107">In this way, the same work creation number can be picked simultaneously by several warehouse workers.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="4d355-108">ステータスが *未処理* または *処理中* の作業指示書のみを分割できます。</span><span class="sxs-lookup"><span data-stu-id="4d355-108">You can split only work orders that have a status of *Open* or *In-progress*.</span></span>

## <a name="turn-on-the-work-split-functionality"></a><span data-ttu-id="4d355-109">作業分割機能を有効にする</span><span class="sxs-lookup"><span data-stu-id="4d355-109">Turn on the work split functionality</span></span>

<span data-ttu-id="4d355-110">作業分割機能を使用するには、システムで機能および前提となる機能を有効にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="4d355-110">Before you can use the work split functionality, you must turn on the feature and its prerequisite feature in your system.</span></span> <span data-ttu-id="4d355-111">管理者は、[機能の管理](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) 設定を使用して、機能の状態を確認し、必要に応じて有効にすることができます。</span><span class="sxs-lookup"><span data-stu-id="4d355-111">Administrators can use the [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) settings to check the status of the features and turn them on as required.</span></span>

<span data-ttu-id="4d355-112">最初に、前提条件となる *組織全体の作業ブロック* 機能が有効になっていない場合は、オンにします。</span><span class="sxs-lookup"><span data-stu-id="4d355-112">First, turn on the prerequisite *Organization-wide work blocking* feature if it isn't already turned on.</span></span> <span data-ttu-id="4d355-113">**機能管理** ワークスペースで、この機能は次のようにリストされています:</span><span class="sxs-lookup"><span data-stu-id="4d355-113">In the **Feature management** workspace, this feature is listed in the following way:</span></span>

- <span data-ttu-id="4d355-114">**モジュール:** *倉庫管理*</span><span class="sxs-lookup"><span data-stu-id="4d355-114">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="4d355-115">**機能名:** *組織全体の作業のブロック*</span><span class="sxs-lookup"><span data-stu-id="4d355-115">**Feature name:** *Organization-wide work blocking*</span></span>

> [!NOTE]
> <span data-ttu-id="4d355-116">この機能が有効になっている場合は、すべての法人で機能をオンにすると、データ アップグレードが自動的に適用されます。</span><span class="sxs-lookup"><span data-stu-id="4d355-116">When this feature is activated, a data upgrade is automatically applied after the feature is turned on across all legal entities.</span></span>

<span data-ttu-id="4d355-117">次に、次の手順に従って、*作業分割* 機能を有効にします。</span><span class="sxs-lookup"><span data-stu-id="4d355-117">Next, turn on the *Work split* feature, which is listed in the following way:</span></span>

- <span data-ttu-id="4d355-118">**モジュール:** *倉庫管理*</span><span class="sxs-lookup"><span data-stu-id="4d355-118">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="4d355-119">**機能名:** *作業分割*</span><span class="sxs-lookup"><span data-stu-id="4d355-119">**Feature name:** *Work split*</span></span>

## <a name="enhancements-to-the-work-details-and-all-work-pages"></a><span data-ttu-id="4d355-120">[作業の詳細] ページと [すべての作業] ページの拡張</span><span class="sxs-lookup"><span data-stu-id="4d355-120">Enhancements to the Work details and All work pages</span></span>

<span data-ttu-id="4d355-121">*作業分割* 機能によって、**作業の詳細** ページと **すべての作業** ページのアクション ウィンドウの **作業** タブに、次の 2 つのボタンが追加されます。</span><span class="sxs-lookup"><span data-stu-id="4d355-121">The *Work split* feature adds the following two buttons to the **Work** tab on the Action Pane of the **Work details** and **All work** pages:</span></span>

- <span data-ttu-id="4d355-122">**作業分割**: 現在の作業 ID を別々の作業員が処理できる複数の小さい作業 ID に分割します。</span><span class="sxs-lookup"><span data-stu-id="4d355-122">**Split work** – Split the current work ID into multiple smaller work IDs that can be processed by separate workers.</span></span>
- <span data-ttu-id="4d355-123">**作業分割セッションのキャンセル**: 作業分割セッションをキャンセルし、作業を処理できるようにします。</span><span class="sxs-lookup"><span data-stu-id="4d355-123">**Cancel work split session** – Cancel the work split session, and make the work available for processing.</span></span>

<span data-ttu-id="4d355-124">![作業分割と作業分割セッションのキャンセル ボタン](media/Work_split_buttons.png "作業分割と作業分割セッションのキャンセル ボタン")</span><span class="sxs-lookup"><span data-stu-id="4d355-124">![Split work and Cancel work split session buttons](media/Work_split_buttons.png "Split work and Cancel work split session buttons")</span></span>

> [!IMPORTANT]
> <span data-ttu-id="4d355-125">**作業分割** ボタンは、次のいずれかの条件が満たされている場合には使用できません。</span><span class="sxs-lookup"><span data-stu-id="4d355-125">The **Split work** button won't be available if any of the following conditions are met:</span></span>
>
> - <span data-ttu-id="4d355-126">作業ステータスが *未処理* または *処理中* 以外になっている。</span><span class="sxs-lookup"><span data-stu-id="4d355-126">The work status is something other than *Open* or *In progress*.</span></span>
> - <span data-ttu-id="4d355-127">作業 ID にコンテナー ID が関連付けられている。</span><span class="sxs-lookup"><span data-stu-id="4d355-127">A container ID is associated with the work ID.</span></span> <span data-ttu-id="4d355-128">(コンテナーは、物理的なアクションを必要とするため体系的に分割することはできません)。</span><span class="sxs-lookup"><span data-stu-id="4d355-128">(A container can't be systematically split, because it requires physical actions.)</span></span>
> - <span data-ttu-id="4d355-129">作業は、クラスターに関連付けられています。</span><span class="sxs-lookup"><span data-stu-id="4d355-129">The work is associated with a cluster.</span></span>
> - <span data-ttu-id="4d355-130">作業指示書タイプが次のいずれかのタイプ以外になっている。</span><span class="sxs-lookup"><span data-stu-id="4d355-130">The work order type is something other than one of the following types:</span></span>
>
>    - <span data-ttu-id="4d355-131">販売注文</span><span class="sxs-lookup"><span data-stu-id="4d355-131">Sales orders</span></span>
>    - <span data-ttu-id="4d355-132">原材料のピッキング</span><span class="sxs-lookup"><span data-stu-id="4d355-132">Raw material picking</span></span>
>    - <span data-ttu-id="4d355-133">移動の出庫</span><span class="sxs-lookup"><span data-stu-id="4d355-133">Transfer issue</span></span>
>
> - <span data-ttu-id="4d355-134">作業が現在別のユーザーによって分割されている。</span><span class="sxs-lookup"><span data-stu-id="4d355-134">The work is currently being split by another user.</span></span> <span data-ttu-id="4d355-135">別のユーザーによって既に分割されている作業の分割ページを開こうとすると、エラー メッセージ "ID \#\#\#\# の作業は現在分割中です。</span><span class="sxs-lookup"><span data-stu-id="4d355-135">If you try to open the splitting page for work that is already being split by another user, you receive the following error message: "The work with ID \#\#\#\# is currently being split.</span></span> <span data-ttu-id="4d355-136">数分後に再試行してください。</span><span class="sxs-lookup"><span data-stu-id="4d355-136">Retry in a few minutes.</span></span> <span data-ttu-id="4d355-137">このメッセージが引き続き表示される場合は、スーパーバイザーに連絡してください" が表示されます。</span><span class="sxs-lookup"><span data-stu-id="4d355-137">If you continue to receive this message, contact a supervisor."</span></span>

<span data-ttu-id="4d355-138">新しい作業ブロックの理由 *分割作業* は、作業 ID が分割処理中であることを示します。</span><span class="sxs-lookup"><span data-stu-id="4d355-138">A new work blocking reason, *Split work*, indicates when the work ID is in the process of being split.</span></span> <span data-ttu-id="4d355-139">ユーザーが作業を実行しようとした場合、**分割作業** ページとウェアハウス アプリの両方に表示されます。</span><span class="sxs-lookup"><span data-stu-id="4d355-139">It's shown both on the **Split work** page and in the warehouse app if a user tries to run the work.</span></span> <span data-ttu-id="4d355-140">ブロックの理由を使用する場合、作業 ID の **ブロックされたウェーブ** フィールドの名前が **ブロック** に変わります。</span><span class="sxs-lookup"><span data-stu-id="4d355-140">When blocking reasons are used, the name of the **Blocked wave** field from the work ID is changed to **Blocked**.</span></span>

## <a name="initiate-a-work-split"></a><span data-ttu-id="4d355-141">作業分割の開始</span><span class="sxs-lookup"><span data-stu-id="4d355-141">Initiate a work split</span></span>

<span data-ttu-id="4d355-142">この機能により、作業 ID から作業明細行を分割するための新しい **分割作業** ページが追加されます。</span><span class="sxs-lookup"><span data-stu-id="4d355-142">The feature adds a new **Split work** page that lets users split work lines from the work ID.</span></span> <span data-ttu-id="4d355-143">ページが最初に開かれたときに、作業ステータスが *未処理* で分割可能な明細行が表示されます。</span><span class="sxs-lookup"><span data-stu-id="4d355-143">When the page is first opened, it shows lines that have a work status of *Open* and that are available to be split.</span></span> <span data-ttu-id="4d355-144">アクション ウィンドウで、**作業分割** を選択して、選択した作業を処理します。</span><span class="sxs-lookup"><span data-stu-id="4d355-144">On the Action Pane, select **Split work** to process the selected work.</span></span>

<span data-ttu-id="4d355-145">作業を分割するには、次の手順を実行します。</span><span class="sxs-lookup"><span data-stu-id="4d355-145">To split work, follow these steps.</span></span>

1. <span data-ttu-id="4d355-146">次の作業ページのいずれかを開きます。</span><span class="sxs-lookup"><span data-stu-id="4d355-146">Open one of the following work pages:</span></span>

    - <span data-ttu-id="4d355-147">**作業の詳細** (**倉庫管理 \> 作業 \> 作業の詳細**)</span><span class="sxs-lookup"><span data-stu-id="4d355-147">**Work details** (**Warehouse management \> Work \> Work details**)</span></span>
    - <span data-ttu-id="4d355-148">**すべての作業** (**倉庫管理 \> 作業 \> すべての作業**)</span><span class="sxs-lookup"><span data-stu-id="4d355-148">**All work** (**Warehouse management \> Work \> All work**)</span></span>

1. <span data-ttu-id="4d355-149">グリッドで、分割する作業 ID を選択します。</span><span class="sxs-lookup"><span data-stu-id="4d355-149">In the grid, select a work ID to split.</span></span> <span data-ttu-id="4d355-150">**作業指示書タイプ** フィールドには、次のいずれかの値を設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="4d355-150">The **Work order type** field must be set to one of the following values:</span></span>

    - <span data-ttu-id="4d355-151">販売注文</span><span class="sxs-lookup"><span data-stu-id="4d355-151">Sales orders</span></span>
    - <span data-ttu-id="4d355-152">原材料のピッキング</span><span class="sxs-lookup"><span data-stu-id="4d355-152">Raw material picking</span></span>
    - <span data-ttu-id="4d355-153">移動の出庫</span><span class="sxs-lookup"><span data-stu-id="4d355-153">Transfer issue</span></span>

1. <span data-ttu-id="4d355-154">アクション ウィンドウの **作業** タブの、**作業** グループで、**作業分割** を選択します。</span><span class="sxs-lookup"><span data-stu-id="4d355-154">On the Action Pane, on the **Work** tab, in the **Work** group, select **Split work**.</span></span>

    <span data-ttu-id="4d355-155">**作業分割** ページが表示され、分割できる作業明細行が表示されます。</span><span class="sxs-lookup"><span data-stu-id="4d355-155">The **Split work** page appears and shows the work lines that are open and available to be split.</span></span> <span data-ttu-id="4d355-156">既定では、使用可能な作業行のみが表示されます。</span><span class="sxs-lookup"><span data-stu-id="4d355-156">By default, only available work lines are shown.</span></span> <span data-ttu-id="4d355-157">作業 ID のすべての明細行 (たとえば作業タイプが *プット* である明細行) を表示するには、グリッドの上部にある **すべての行の表示** チェック ボックスをオンにします。</span><span class="sxs-lookup"><span data-stu-id="4d355-157">To view all lines for the work ID (for example, lines that have a work type of *Put*), select the **Show all lines** check box above the grid.</span></span>

    <span data-ttu-id="4d355-158">"このページを分割して終了するまで、ユーザーはこの作業を処理できません" というメッセージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="4d355-158">The following message is shown: "Users can't process lines of the work until you finish splitting and close this page."</span></span>

    <span data-ttu-id="4d355-159">現在の作業の **作業ブロック理由** フィールドが *作業分割* に設定され、その作業がブロックされます。</span><span class="sxs-lookup"><span data-stu-id="4d355-159">The **Work blocking reason** field for the current work will be set to *Split work*, and the work will be blocked.</span></span>

    <span data-ttu-id="4d355-160">![ブロックの理由](media/Blocking_reason.png "ブロックの理由")</span><span class="sxs-lookup"><span data-stu-id="4d355-160">![Blocking reason](media/Blocking_reason.png "Blocking reason")</span></span>

1. <span data-ttu-id="4d355-161">現在の作業 ID から削除する明細行を選択し、新しい作業 ID に追加します。</span><span class="sxs-lookup"><span data-stu-id="4d355-161">Select the lines to remove from the current work ID and add to a new work ID.</span></span> <span data-ttu-id="4d355-162">以下のイベントが発生します :</span><span class="sxs-lookup"><span data-stu-id="4d355-162">The following events occur:</span></span>

    - <span data-ttu-id="4d355-163">作業を分割すると、元の作業 ID の選択した明細行がキャンセルされ、新しい作業 ID にコピーされます。</span><span class="sxs-lookup"><span data-stu-id="4d355-163">When you split the work, the selected line or lines from the original work ID are canceled and then copied to a new work ID.</span></span>
    - <span data-ttu-id="4d355-164">既存の作業テンプレート構造と、プット (および将来のピック/プット) の場所も保持されます。</span><span class="sxs-lookup"><span data-stu-id="4d355-164">The existing work template structure and the location of the put (and also future pick/put pairs) are preserved.</span></span> <span data-ttu-id="4d355-165">次の作業 ID フィールドの値は、元の作業から新しい作業にコピーされます。</span><span class="sxs-lookup"><span data-stu-id="4d355-165">Values for the following work ID fields are copied from the original work to the new work:</span></span>

        - <span data-ttu-id="4d355-166">貨物 ID</span><span class="sxs-lookup"><span data-stu-id="4d355-166">Load ID</span></span>
        - <span data-ttu-id="4d355-167">出荷 ID</span><span class="sxs-lookup"><span data-stu-id="4d355-167">Shipment ID</span></span>
        - <span data-ttu-id="4d355-168">作業指示書タイプ</span><span class="sxs-lookup"><span data-stu-id="4d355-168">Work order type</span></span>
        - <span data-ttu-id="4d355-169">注文番号</span><span class="sxs-lookup"><span data-stu-id="4d355-169">Order number</span></span>
        - <span data-ttu-id="4d355-170">サイト</span><span class="sxs-lookup"><span data-stu-id="4d355-170">Site</span></span>
        - <span data-ttu-id="4d355-171">倉庫</span><span class="sxs-lookup"><span data-stu-id="4d355-171">Warehouse</span></span>
        - <span data-ttu-id="4d355-172">作業の優先順位</span><span class="sxs-lookup"><span data-stu-id="4d355-172">Work priority</span></span>
        - <span data-ttu-id="4d355-173">作業プール ID</span><span class="sxs-lookup"><span data-stu-id="4d355-173">Work pool ID</span></span>
        - <span data-ttu-id="4d355-174">ウェーブ ID</span><span class="sxs-lookup"><span data-stu-id="4d355-174">Wave ID</span></span>
        - <span data-ttu-id="4d355-175">作業作成数</span><span class="sxs-lookup"><span data-stu-id="4d355-175">Work creation number</span></span>

    - <span data-ttu-id="4d355-176">次のフィールドは、新しい作業 ID にコピーされません。</span><span class="sxs-lookup"><span data-stu-id="4d355-176">The following fields aren't copied to the new work ID:</span></span>

        - <span data-ttu-id="4d355-177">**作業 ID**: 適切な番号順序から新しい作業 ID が生成されます。</span><span class="sxs-lookup"><span data-stu-id="4d355-177">**Work ID** – A new work ID is generated from the appropriate number sequence.</span></span>
        - <span data-ttu-id="4d355-178">**作業ステータス**: このフィールドは、*未処理* に設定されます。</span><span class="sxs-lookup"><span data-stu-id="4d355-178">**Work status** – This field is set to *Open*.</span></span>
        - <span data-ttu-id="4d355-179">**ロック元**: このフィールドは、最初は空白に設定されます。</span><span class="sxs-lookup"><span data-stu-id="4d355-179">**Locked by** – This field is initially set to blank.</span></span>
        - <span data-ttu-id="4d355-180">**ターゲット ライセンス プレート ID**: このフィールドは空白のままになります。</span><span class="sxs-lookup"><span data-stu-id="4d355-180">**Target license plate ID** – This field is left blank.</span></span>
        - <span data-ttu-id="4d355-181">**作成日時**: このフィールドは、現在の日付と時刻に設定されます。</span><span class="sxs-lookup"><span data-stu-id="4d355-181">**Created date and time** – This field is set to the current date and time.</span></span>
        - <span data-ttu-id="4d355-182">**ブロックされたウェーブ/固定**: このフィールドは、元の作業 ID と新しい作業 ID に対して再計算されます。</span><span class="sxs-lookup"><span data-stu-id="4d355-182">**Blocked wave/frozen** – This field is recomputed for the original work ID and the new work ID.</span></span>

1. <span data-ttu-id="4d355-183">アクション ウィンドウで、**作業分割** を選択します。</span><span class="sxs-lookup"><span data-stu-id="4d355-183">On the Action Pane, select **Split work**.</span></span>

<span data-ttu-id="4d355-184">作業が分割されている間、"処理中です - 作業分割" というメッセージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="4d355-184">While the work is being split, the following message is shown: "Processing operation - Split work".</span></span> <span data-ttu-id="4d355-185">このメッセージが表示されている間は、メッセージ ボックスで **キャンセル** を選択することにより、操作を取り消すことができます。</span><span class="sxs-lookup"><span data-stu-id="4d355-185">While this message is visible, you can cancel the operation by selecting **Cancel** in the message box.</span></span>

<span data-ttu-id="4d355-186">**すべての明細行を表示** チェック ボックスをオフにすると、分割およびキャンセルされた行はグリッドに表示されなくなります。</span><span class="sxs-lookup"><span data-stu-id="4d355-186">If the **Show all lines** check box is cleared, the line that was split off and canceled will no longer appear in the grid.</span></span> <span data-ttu-id="4d355-187">このチェック ボックスがオンになっている場合は、その明細行の **作業ステータス** フィールドの値が *キャンセル済* に変更されていることを確認する必要があります。</span><span class="sxs-lookup"><span data-stu-id="4d355-187">If the check box is selected, you should see that the value of the **Work status** field for that line has changed to *Canceled*.</span></span>

<span data-ttu-id="4d355-188">次の通知は、新しい作業 ID が作成されたことを示します: "元の作業 \#\#\#\# からの分割によって作業 \#\#\#\# が作成されました"。</span><span class="sxs-lookup"><span data-stu-id="4d355-188">The following notification is shown to indicate that the new work ID has been created: "Work \#\#\#\# has been created by splitting off from original work \#\#\#\#."</span></span>

<span data-ttu-id="4d355-189">元の作業 ID (*プット* 明細行など) の他の作業明細行は、キャンセルされた作業明細行を反映するために、必要に応じて調整されます。</span><span class="sxs-lookup"><span data-stu-id="4d355-189">Other work lines from the original work ID (such as *Put* lines) will be adjusted as required to reflect the lines of work that have been canceled.</span></span> <span data-ttu-id="4d355-190">たとえば、*プット* 明細行の数量が 15 であって、*ピック* 明細行の合計数量が 10 である元の作業 ID がキャンセルされた場合、元の作業 ID の新しい *プット* 数量は 5 になります。</span><span class="sxs-lookup"><span data-stu-id="4d355-190">For example, if the original work ID had a *Put* line for a quantity of 15, and *Pick* lines that have a total quantity of 10 were canceled, the new *Put* quantity on the original work ID will now be 5.</span></span>

<span data-ttu-id="4d355-191">新しい作業をすぐにユーザーに割り当てることはできません。</span><span class="sxs-lookup"><span data-stu-id="4d355-191">The new work won't immediately be assigned to any user.</span></span> <span data-ttu-id="4d355-192">ただし、必要に応じて **作業の詳細** ページの標準機能を使用することにより、ユーザーにそれを割り当てることができます。</span><span class="sxs-lookup"><span data-stu-id="4d355-192">However, you can assign it to a user now, as required, by using the standard functionality of the **Work details** page.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="4d355-193">2 つ以上の使用可能な作業明細行を含む作業 ID のみを分割できます。</span><span class="sxs-lookup"><span data-stu-id="4d355-193">You can split only work IDs that contain two or more available work lines.</span></span> <span data-ttu-id="4d355-194">作業明細行が 1 つしかない場合に **作業分割** を選択すると、"最初の作業では少なくとも 1 つの作業明細行を保持する必要があります" というエラー メッセージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="4d355-194">If you select **Split work** when there is only one work line, you will receive the following error message: "At least one work line must remain on initial work."</span></span> <span data-ttu-id="4d355-195">この場合、分割は行われません。</span><span class="sxs-lookup"><span data-stu-id="4d355-195">In this case, no splitting will occur.</span></span>

## <a name="finish-a-work-split"></a><span data-ttu-id="4d355-196">作業分割の完了</span><span class="sxs-lookup"><span data-stu-id="4d355-196">Finish a work split</span></span>

<span data-ttu-id="4d355-197">作業分割を完了するには、*作業分割* ブロックの理由を削除する必要があります。</span><span class="sxs-lookup"><span data-stu-id="4d355-197">To finish splitting work, the *Split work* blocking reason must be removed.</span></span> <span data-ttu-id="4d355-198">この手順を実行するには、次の 2 つの方法があります。</span><span class="sxs-lookup"><span data-stu-id="4d355-198">There are two ways to complete this step:</span></span>

- <span data-ttu-id="4d355-199">作業を分割しているユーザーは、右上隅の **閉じる** ボタン (**X**) を選択することによって **作業分割** ページを閉じます。</span><span class="sxs-lookup"><span data-stu-id="4d355-199">The user who is splitting the work closes the **Split work** page by selecting the **Close** button (**X**) in the upper-right corner.</span></span> <span data-ttu-id="4d355-200">ページを閉じると、*作業分割* ブロックの理由が削除されます。</span><span class="sxs-lookup"><span data-stu-id="4d355-200">When the page is closed, the *Split Work* blocking reason will be removed.</span></span> <span data-ttu-id="4d355-201">この作業の *ブロック* 状態が再計算され、この作業に対してブロックの理由が残っていない場合、その作業はブロック解除されます。</span><span class="sxs-lookup"><span data-stu-id="4d355-201">The *Blocked* state of this work will be recomputed and, if there are no remaining blocking reasons for this work, the work will be unblocked.</span></span>
- <span data-ttu-id="4d355-202">ユーザーは作業 ID を開いて、アクション ウィンドウの **作業分割セッションのキャンセル** ボタンを選択します。</span><span class="sxs-lookup"><span data-stu-id="4d355-202">Any user opens the work ID and selects the **Cancel work split session** button on the Action Pane.</span></span> <span data-ttu-id="4d355-203">*作業分割* ブロックの理由が削除され、**作業分割** ページが閉じられた場合と同様に、この作業の *ブロック* 状態が再計算されます。</span><span class="sxs-lookup"><span data-stu-id="4d355-203">The *Split work* blocking reason will be removed, and the *Blocked* state of this work will be recomputed, just as when the **Split work** page is closed.</span></span>

<span data-ttu-id="4d355-204">*作業分割* ブロック理由が削除されると、モバイル デバイスで作業を実行できるようになります。ただし、**ブロック** 状態が作業 ID で *いいえ* に設定されている場合に限ります。</span><span class="sxs-lookup"><span data-stu-id="4d355-204">After the *Split work* blocking reason is removed, the work can be run on the mobile device, provided that the **Blocked** state is set to *No* on the work ID.</span></span>

## <a name="user-blocking-on-the-warehouse-app"></a><span data-ttu-id="4d355-205">ウェアハウス アプリでのユーザーのブロック</span><span class="sxs-lookup"><span data-stu-id="4d355-205">User blocking on the warehouse app</span></span>

<span data-ttu-id="4d355-206">分割された作業 ID に対して、ウェアハウス アプリを使用してピッキング作業を実行しようとすると、"ID \#\#\#\# の作業は現在分割されています" というエラー メッセージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="4d355-206">If you try to use the warehouse app to run picking work against a work ID that is being split, you will receive the following error message: "The work with ID \#\#\#\# is currently being split."</span></span> <span data-ttu-id="4d355-207">このメッセージが表示された場合は、**キャンセル** を選択します。</span><span class="sxs-lookup"><span data-stu-id="4d355-207">If you receive this message, select **Cancel**.</span></span> <span data-ttu-id="4d355-208">その後、他の作業の処理を続行できます。</span><span class="sxs-lookup"><span data-stu-id="4d355-208">You can then continue to process other work.</span></span>

## <a name="other-blocked-operations"></a><span data-ttu-id="4d355-209">他のブロックされた操作</span><span class="sxs-lookup"><span data-stu-id="4d355-209">Other blocked operations</span></span>

<span data-ttu-id="4d355-210">分割されている作業に関連する作業明細行、作業在庫トランザクション、または補充リンクを変更する工程が失敗し、"ID \#\#\#\# の作業は現在分割されています" というエラー メッセージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="4d355-210">Any operations that modify work lines, work inventory transactions, or replenishment links that are related to work that is being split will fail, and the following error message will be shown: "The work with ID \#\#\#\# is currently being split."</span></span>
