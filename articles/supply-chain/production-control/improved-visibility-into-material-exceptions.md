---
title: "材料の例外の把握"
description: "このトピックでは、製造オーダーおよびバッチ オーダーの原材料の例外をより詳細に把握する方法について説明します。"
author: johanhoffmann
manager: AnnBe
ms.date: 10/30/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: JmgShopSupervisorWorkspace
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, Operations
ms.custom: 1705903
ms.search.region: Global
ms.author: johanho
ms.search.validfrom: 2017-12-31
ms.dyn365.ops.version: 7.3
ms.translationtype: HT
ms.sourcegitcommit: 3c43a42822f291607fbc9708dd07ebf99b9d7ec4
ms.openlocfilehash: 31b94a3e7426a28377d5ffe8ba1d156b9ea5b550
ms.contentlocale: ja-jp
ms.lasthandoff: 01/26/2018

---
# <a name="visibility-into-material-exceptions"></a><span data-ttu-id="88c73-103">材料の例外の把握</span><span class="sxs-lookup"><span data-stu-id="88c73-103">Visibility into material exceptions</span></span>

<span data-ttu-id="88c73-104">[**生産フロアの管理**] ワークスペースでは、3 つのタイルを使用して、製造オーダーおよびバッチ オーダーの原材料の例外をより詳細に把握できます。</span><span class="sxs-lookup"><span data-stu-id="88c73-104">In the **Production floor management** workspace, three tiles give you better visibility into exceptions for raw materials for production orders and batch orders:</span></span>

- <span data-ttu-id="88c73-105">注意が必要な未リリースの材料明細行</span><span class="sxs-lookup"><span data-stu-id="88c73-105">Unreleased material lines needing attention</span></span>
- <span data-ttu-id="88c73-106">注意が必要な未処理のウェーブ</span><span class="sxs-lookup"><span data-stu-id="88c73-106">Unprocessed waves needing attention</span></span>
- <span data-ttu-id="88c73-107">注意が必要な未処理の倉庫作業</span><span class="sxs-lookup"><span data-stu-id="88c73-107">Open warehouse work needing attention</span></span>

<span data-ttu-id="88c73-108">3つのタイルすべてについて、部品表 (BOM) 明細行とフォーミュラ明細行の原材料予定日がワークスペース日付と比較されます。また、[**生産単位**]、[**リソース グループ**]、および [**リソース**] のフィルタと比較されます。[**自分のワークスペースのコンフィギュレーション**] メニューで設定します。</span><span class="sxs-lookup"><span data-stu-id="88c73-108">For all three tiles, the raw material date of the bill of materials (BOM) lines and formula lines is compared against the workspace date, and also against the filters for **Production unit**, **Resource group**, and **Resource** that are set on the **Configure my work space** menu.</span></span> <span data-ttu-id="88c73-109">既定値ではワークスペース日付は現在の日付が設定されていますが、調整することができます。</span><span class="sxs-lookup"><span data-stu-id="88c73-109">By default, the workspace date is set to the current date, but you can adjust it.</span></span>

<span data-ttu-id="88c73-110">未リリースの BOM 明細行またはフォーミュラ明細行は、明細行の原材料消費予定日がワークスペース日付と同じかそれより早い場合、およびワークスペースのフィルタで定義された基準を満たす場合には注意が必要です。</span><span class="sxs-lookup"><span data-stu-id="88c73-110">An unreleased BOM line or formula line requires attention if the raw material date of the line is the same as or earlier than the workspace date, and if it meets the criteria that are defined by the filters in the workspace.</span></span>

<span data-ttu-id="88c73-111">次の図の青色のバーは、リソース上でスケジュールされた生産ジョブを表しています。</span><span class="sxs-lookup"><span data-stu-id="88c73-111">In the following figure, the blue bar represents a production job that is scheduled on a resource.</span></span> <span data-ttu-id="88c73-112">ジョブは、2017 年 5 月 1 日 (2017/05/01) に開始する予定です。</span><span class="sxs-lookup"><span data-stu-id="88c73-112">The job is scheduled to start on May 1, 2017 (2017/05/01).</span></span> <span data-ttu-id="88c73-113">この日付は原材料の日付です。</span><span class="sxs-lookup"><span data-stu-id="88c73-113">This date is the raw material date.</span></span> <span data-ttu-id="88c73-114">つまり、BOM およびフォーミュラ明細行でのジョブに割り当てられた材料は、この日付に準備を完了する必要があります。</span><span class="sxs-lookup"><span data-stu-id="88c73-114">In other words, the materials that are assigned to the job on the BOM and formula lines must be ready on this date.</span></span> <span data-ttu-id="88c73-115">図のもう一方の日付、2017 年 5 月 6 日 (2017/05/06) は、ワークスペースの日付を表します。</span><span class="sxs-lookup"><span data-stu-id="88c73-115">The other date in the figure, May 6, 2017 (2017/05/06), represents the workspace date.</span></span> <span data-ttu-id="88c73-116">この例では、原材料の日付はワークスペースの日付よりも前です。</span><span class="sxs-lookup"><span data-stu-id="88c73-116">In this example, the raw material date is earlier than the workspace date.</span></span> <span data-ttu-id="88c73-117">したがって、原材料の消費が開始予定日を過ぎ、BOM およびフォーミュラ明細行が注意を要する基準を満たしています。</span><span class="sxs-lookup"><span data-stu-id="88c73-117">Therefore, the date when consumption of the raw material was supposed to start has passed, and the BOM and formula lines meet the criteria for requiring attention.</span></span>

![原材料日付がワークスペース日付より前の生産ジョブの例](./media/improved-visibility.png)

## <a name="unreleased-material-lines-needing-attention"></a><span data-ttu-id="88c73-119">注意が必要な未リリースの材料明細行</span><span class="sxs-lookup"><span data-stu-id="88c73-119">Unreleased material lines needing attention</span></span>

<span data-ttu-id="88c73-120">BOM またはフォーミュラ明細行は、3 つの方法で倉庫にリリースすることができます:</span><span class="sxs-lookup"><span data-stu-id="88c73-120">A BOM or formula line can be released to the warehouse in three ways:</span></span>

- <span data-ttu-id="88c73-121">製造オーダーまたはバッチ オーダーの一部として</span><span class="sxs-lookup"><span data-stu-id="88c73-121">As part of a production order or batch order release</span></span>
- <span data-ttu-id="88c73-122">手動リリースとして</span><span class="sxs-lookup"><span data-stu-id="88c73-122">As a manual release</span></span>
- <span data-ttu-id="88c73-123">バッチ ジョブを自動的に実行する</span><span class="sxs-lookup"><span data-stu-id="88c73-123">Automatically through a batch job</span></span>

<span data-ttu-id="88c73-124">詳細については次を参照してください [BOM とフォーミュラ明細行を倉庫にリリース](releasing-bom-and-formula-lines-to-warehouse.md)。</span><span class="sxs-lookup"><span data-stu-id="88c73-124">For more information, see [Release BOM and formula lines to the warehouse](releasing-bom-and-formula-lines-to-warehouse.md).</span></span> 

<span data-ttu-id="88c73-125">BOM またはフォーミュラ明細行がリリースされていないか、一部のみがリリースされていて、ワークスペースの日付とフィルタ条件が満たされている場合、その明細行は、 [**注意が必要な未リリースの材料明細行**] タイルに表示される番号の計算に含まれます。</span><span class="sxs-lookup"><span data-stu-id="88c73-125">If a BOM or formula line hasn't been released or has been only partly released, and if the date and filter criteria of the workspace are met, the line is included in the calculation of the number that appears on the **Unreleased material lines needing attention** tile.</span></span>

<span data-ttu-id="88c73-126">タイルを選択すると、[**倉庫にリリース**] ページが開きます。</span><span class="sxs-lookup"><span data-stu-id="88c73-126">When you select the tile, the **Release to warehouse** page is opened.</span></span> <span data-ttu-id="88c73-127">このページには、未リリースの BOM およびフォーミュラ明細行の数がタイルの番号で示されます。</span><span class="sxs-lookup"><span data-stu-id="88c73-127">This page shows the number of unreleased BOM and formula lines that is indicated by the number on the tile.</span></span> <span data-ttu-id="88c73-128">リリース前の明細行は、上部のグリッドに表示されます。</span><span class="sxs-lookup"><span data-stu-id="88c73-128">The unreleased lines appear in the upper grid.</span></span> <span data-ttu-id="88c73-129">このグリッドは、最初に明細行に対して見積もられた量、すでにリリースされた量、およびまだリリースされなければならない残りの量を示します。</span><span class="sxs-lookup"><span data-stu-id="88c73-129">This grid shows the quantity that was originally estimated for the line, the quantity that has already been released, and the remaining quantity that must still be released.</span></span> <span data-ttu-id="88c73-130">下部のグリッドに上部グリッドから明細行を追加できます。</span><span class="sxs-lookup"><span data-stu-id="88c73-130">You can add lines from the upper grid to the lower grid.</span></span> <span data-ttu-id="88c73-131">下部グリッドから、選択した明細行を倉庫にリリースすることができます。</span><span class="sxs-lookup"><span data-stu-id="88c73-131">From the lower grid, you can then release the selected lines to the warehouse.</span></span> <span data-ttu-id="88c73-132">下部のグリッドからは、部分的な量のみがリリースされるように数量を調整してリリースすることもできます。</span><span class="sxs-lookup"><span data-stu-id="88c73-132">From the lower grid, you can also adjust the quantity to release so that only a partial quantity is released.</span></span>

## <a name="unprocessed-waves-needing-attention"></a><span data-ttu-id="88c73-133">注意が必要な未処理のウェーブ</span><span class="sxs-lookup"><span data-stu-id="88c73-133">Unprocessed waves needing attention</span></span>

<span data-ttu-id="88c73-134">BOM またはフォーミュラ明細行がリリースされると、生産ウェーブ テンプレートの構成に応じて、新しい生産ウェーブまたは既存のオープン ウェーブのいずれかに追加されます。</span><span class="sxs-lookup"><span data-stu-id="88c73-134">When a BOM or formula line is released, it's added to either a new production wave or an existing open wave, depending on the configuration of the production wave template.</span></span> <span data-ttu-id="88c73-135">ウェーブ テンプレートの構成により、BOM またはフォーミュラ明細行が解放されたときに自動的に処理されるよう、ウェーブを設定することもできます。</span><span class="sxs-lookup"><span data-stu-id="88c73-135">Through the configuration of the wave template, you can also set up a wave so that it's automatically processed when a BOM or formula line is released.</span></span> <span data-ttu-id="88c73-136">ウェーブが処理されるときは、原材料ピッキング用の倉庫作業が生成されます。</span><span class="sxs-lookup"><span data-stu-id="88c73-136">When the wave is processed, warehouse work for raw material picking is generated.</span></span> <span data-ttu-id="88c73-137">ウェーブ テンプレートがリリース時に処理されないように設定されている場合、ウェーブは未処理の状態のままです。</span><span class="sxs-lookup"><span data-stu-id="88c73-137">If the wave template is configured so that waves aren't processed at the time of release, the wave remains in an unprocessed state.</span></span> <span data-ttu-id="88c73-138">[**注意が必要な未処理のウェーブ**] タイルは、未処理のウェーブの倉庫にリリースされ、ワークスペース日付より早い、または同じ原材料日付を持つ BOM およびフォーミュラ明細行の数を表示します。</span><span class="sxs-lookup"><span data-stu-id="88c73-138">The **Unprocessed waves needing attention** tile shows the number of BOM and formula lines that have been released to the warehouse on unprocessed waves, and that have a raw material date that is earlier than or the same as the workspace date.</span></span> <span data-ttu-id="88c73-139">明細行は、ワークスぺースのフィルターに適用される運営リソースによっても消費されなければなりません。</span><span class="sxs-lookup"><span data-stu-id="88c73-139">The lines must also be consumed by an operation resource that applies to the filter of the workspace.</span></span>

<span data-ttu-id="88c73-140">タイルが選択されている場合、[**すべての生産ウェーブ**] ページが開かれます。</span><span class="sxs-lookup"><span data-stu-id="88c73-140">When the tile is selected, the **All production waves** page is opened.</span></span> <span data-ttu-id="88c73-141">このページは、リリースされた BOM からのウェーブ明細行およびタイルの条件を満たすフォーミュラ明細行を含むオープンウェーブの数によってフィルター処理されます。</span><span class="sxs-lookup"><span data-stu-id="88c73-141">This page is filtered by the number of open waves that contain wave lines from released BOM and formula lines that meet the criteria for the tile.</span></span> <span data-ttu-id="88c73-142">[**すべての生産ウェーブ**] ページから、手動でウェーブを処理できます。</span><span class="sxs-lookup"><span data-stu-id="88c73-142">From the **All production waves** page, you can manually process the wave.</span></span>

## <a name="open-warehouse-work-needing-attention"></a><span data-ttu-id="88c73-143">注意が必要な未処理の倉庫作業</span><span class="sxs-lookup"><span data-stu-id="88c73-143">Open warehouse work needing attention</span></span>

<span data-ttu-id="88c73-144">[**注意が必要な未処理の倉庫作業**] タイルは、未処理の作業がある倉庫にリリースされ、ワークスペース日付より早い、または同じ原材料日付を持つ BOM およびフォーミュラ明細行の数を表示します。</span><span class="sxs-lookup"><span data-stu-id="88c73-144">The **Open warehouse work needing attention** tile shows the number of BOM and formula lines that have been released to the warehouse, that have unprocessed work, and that have a raw material date that is earlier than or the same as the workspace date.</span></span> <span data-ttu-id="88c73-145">明細行は、ワークスぺースのフィルターに適用される運営リソースによっても消費されなければなりません。</span><span class="sxs-lookup"><span data-stu-id="88c73-145">The lines must also be consumed by an operation resource that applies to the filter of the workspace.</span></span>

<span data-ttu-id="88c73-146">タイルが選択されている場合、[**すべての作業**] ページが開かれます。</span><span class="sxs-lookup"><span data-stu-id="88c73-146">When the tile is selected, the **All work** page is opened.</span></span> <span data-ttu-id="88c73-147">このページは、リリースされた BOM からの作業明細行およびタイルの条件を満たすフォーミュラ明細行を含むオープン作業ヘッダーの数によってフィルター処理されます。</span><span class="sxs-lookup"><span data-stu-id="88c73-147">This page is filtered by the number of open work headers that contain work lines from released BOM and formula lines that meet the criteria for the tile.</span></span> <span data-ttu-id="88c73-148">[**すべての作業**] ページから、手動で作業を処理できます。</span><span class="sxs-lookup"><span data-stu-id="88c73-148">From the **All work** page, you can manually process the work.</span></span>

