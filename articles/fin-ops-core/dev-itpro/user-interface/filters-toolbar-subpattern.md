---
title: フィルターおよびツールバーのサブパターン
description: このトピックでは、フィルターおよびツール バーのサブパターンについて説明します。 これらのワークスペース固有のサブパターンは、リストやグラフをホストする、パノラマ セクション内のフィルターやアクションを表示するために開発されました。
author: jasongre
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: sericks
ms.search.scope: Operations
ms.custom: 29191
ms.assetid: 8e32ba2f-6cc1-4bfd-9c79-42a8392fa812
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d57142136d2edefe94b379465c02bd5170f74c57
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/27/2019
ms.locfileid: "2191774"
---
# <a name="filters-and-toolbar-subpatterns"></a><span data-ttu-id="f9101-104">フィルターおよびツールバーのサブパターン</span><span class="sxs-lookup"><span data-stu-id="f9101-104">Filters and Toolbar subpatterns</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f9101-105">このトピックでは、フィルターおよびツール バーのサブパターンについて説明します。</span><span class="sxs-lookup"><span data-stu-id="f9101-105">This topic provides information about the Filters and Toolbar subpatterns.</span></span> <span data-ttu-id="f9101-106">これらのワークスペース固有のサブパターンは、リストやグラフをホストする、パノラマ セクション内のフィルターやアクションを表示するために開発されました。</span><span class="sxs-lookup"><span data-stu-id="f9101-106">These workspace-specific subpatterns have been developed to show filters and/or actions inside panorama sections that host lists and charts.</span></span>

<a name="usage"></a><span data-ttu-id="f9101-107">用途</span><span class="sxs-lookup"><span data-stu-id="f9101-107">Usage</span></span>
-----

<span data-ttu-id="f9101-108">フィルターおよびツール バー サブパターンは、リストやグラフをホストする、パノラマ セクション内のフィルターやアクションを表示するために開発されたワークスペース固有のサブパターンです。</span><span class="sxs-lookup"><span data-stu-id="f9101-108">The Filters and Toolbar subpatterns are workspace-specific subpatterns that have been developed to show filters and/or actions inside panorama sections that host lists and charts.</span></span> <span data-ttu-id="f9101-109">これらのサブパターンのフィルタ処理の一部のフィールドは、次のフィールド タイプに限定される必要があります。</span><span class="sxs-lookup"><span data-stu-id="f9101-109">Fields in the filtering parts of these subpatterns should be limited to the following field types.</span></span> <span data-ttu-id="f9101-110">これらすべてのフィールド タイプは入力の制約を持ちクエリに適用できます。</span><span class="sxs-lookup"><span data-stu-id="f9101-110">All these field types have constrained inputs and can be applied to the query.</span></span>

-   <span data-ttu-id="f9101-111">Lookups を使用した StringEdits</span><span class="sxs-lookup"><span data-stu-id="f9101-111">StringEdits with Lookups</span></span>
-   <span data-ttu-id="f9101-112">日付フィールド</span><span class="sxs-lookup"><span data-stu-id="f9101-112">Date fields</span></span>
-   <span data-ttu-id="f9101-113">ReferenceGroup</span><span class="sxs-lookup"><span data-stu-id="f9101-113">ReferenceGroup</span></span>
-   <span data-ttu-id="f9101-114">Comboboxes</span><span class="sxs-lookup"><span data-stu-id="f9101-114">Comboboxes</span></span>
-   <span data-ttu-id="f9101-115">チェック ボックス</span><span class="sxs-lookup"><span data-stu-id="f9101-115">Checkboxes</span></span>
-   <span data-ttu-id="f9101-116">クイック フィルター</span><span class="sxs-lookup"><span data-stu-id="f9101-116">Quick Filter</span></span>

<span data-ttu-id="f9101-117">この記事では、2 つのサブパターンについて説明します。</span><span class="sxs-lookup"><span data-stu-id="f9101-117">Two subpatterns are described in this article:</span></span>

-   <span data-ttu-id="f9101-118">**フィルターおよびツールバー - インライン** – このサブパターンでは、フィルタ フィールドと同じ行に定義されたアクションが表示されます。</span><span class="sxs-lookup"><span data-stu-id="f9101-118">**Filters and Toolbar - Inline** – In this subpattern, any defined actions appear on the same line as the filter fields.</span></span>
-   <span data-ttu-id="f9101-119">**フィルターおよびツールバー (積み上げ)** – このサブパターンでは、フィルタ フィールドの下の別の行に定義されたアクションが表示されます。</span><span class="sxs-lookup"><span data-stu-id="f9101-119">**Filters and Toolbar - Stacked** – In this subpattern, any defined actions appear on a separate line below the filter fields.</span></span>

## <a name="wireframe"></a><span data-ttu-id="f9101-120">ワイヤーフレーム</span><span class="sxs-lookup"><span data-stu-id="f9101-120">Wireframe</span></span>
### <a name="filters-and-toolbar---inline"></a><span data-ttu-id="f9101-121">フィルターおよびツールバー - インライン</span><span class="sxs-lookup"><span data-stu-id="f9101-121">Filters and Toolbar - Inline</span></span>

<span data-ttu-id="f9101-122">[![filterToolbarInlineWireframe](./media/filtertoolbarinlinewireframe.png)](./media/filtertoolbarinlinewireframe.png)</span><span class="sxs-lookup"><span data-stu-id="f9101-122">[![filterToolbarInlineWireframe](./media/filtertoolbarinlinewireframe.png)](./media/filtertoolbarinlinewireframe.png)</span></span>

### <a name="filters-and-toolbar---stacked"></a><span data-ttu-id="f9101-123">フィルターおよびツールバー - 積み上げ</span><span class="sxs-lookup"><span data-stu-id="f9101-123">Filters and Toolbar - Stacked</span></span>

<span data-ttu-id="f9101-124">[![filterToolbarStackedWireframe](./media/filtertoolbarstackedwireframe.png)](./media/filtertoolbarstackedwireframe.png)</span><span class="sxs-lookup"><span data-stu-id="f9101-124">[![filterToolbarStackedWireframe](./media/filtertoolbarstackedwireframe.png)](./media/filtertoolbarstackedwireframe.png)</span></span>

## <a name="model"></a><span data-ttu-id="f9101-125">モデル</span><span class="sxs-lookup"><span data-stu-id="f9101-125">Model</span></span>
### <a name="filters-and-toolbar---inline-high-level-structure"></a><span data-ttu-id="f9101-126">フィルターおよびツールバー - インライン: 高度なレベル構造</span><span class="sxs-lookup"><span data-stu-id="f9101-126">Filters and Toolbar - Inline: High-level structure</span></span>

- <span data-ttu-id="f9101-127">グループ (ArrangeMethod=HorizontalLeft)</span><span class="sxs-lookup"><span data-stu-id="f9101-127">Group (ArrangeMethod=HorizontalLeft)</span></span>

    - <span data-ttu-id="f9101-128">*FilterGroup (グループ) \[オプション\]*</span><span class="sxs-lookup"><span data-stu-id="f9101-128">*FilterGroup (Group) \[Optional\]*</span></span>

        - <span data-ttu-id="f9101-129">*QuickFilter (QuickFilter) \[オプション\]*</span><span class="sxs-lookup"><span data-stu-id="f9101-129">*QuickFilter (QuickFilter) \[Optional\]*</span></span>
        - <span data-ttu-id="f9101-130">*フィールド ($ フィールド)\[0..N\]*</span><span class="sxs-lookup"><span data-stu-id="f9101-130">*FilterFIelds ($Field) \[0..N\]*</span></span>

    - <span data-ttu-id="f9101-131">*ツール バー (ActionPane) \[オプション\]*</span><span class="sxs-lookup"><span data-stu-id="f9101-131">*Toolbar (ActionPane) \[Optional\]*</span></span>

### <a name="filters-and-toolbar---stacked-high-level-structure"></a><span data-ttu-id="f9101-132">フィルターおよびツールバー - 積み上げ: 高度なレベル構造</span><span class="sxs-lookup"><span data-stu-id="f9101-132">Filters and Toolbar - Stacked: High-level structure</span></span>

- <span data-ttu-id="f9101-133">グループ (ArrangeMethod=Vertical)</span><span class="sxs-lookup"><span data-stu-id="f9101-133">Group (ArrangeMethod=Vertical)</span></span>

    - <span data-ttu-id="f9101-134">*FilterGroup (グループ) \[オプション\]*</span><span class="sxs-lookup"><span data-stu-id="f9101-134">*FilterGroup (Group) \[Optional\]*</span></span>

        - <span data-ttu-id="f9101-135">*QuickFilter (QuickFilter) \[オプション\]*</span><span class="sxs-lookup"><span data-stu-id="f9101-135">*QuickFilter (QuickFilter) \[Optional\]*</span></span>
        - <span data-ttu-id="f9101-136">*FilterField1 ($ フィールド) \[オプション\]*</span><span class="sxs-lookup"><span data-stu-id="f9101-136">*FilterField1 ($Field) \[Optional\]*</span></span>
        - <span data-ttu-id="f9101-137">*FilterField2 ($ フィールド) \[オプション\]*</span><span class="sxs-lookup"><span data-stu-id="f9101-137">*FilterField2 ($Field) \[Optional\]*</span></span>

    - <span data-ttu-id="f9101-138">*ツール バー (ActionPane) \[オプション\]*</span><span class="sxs-lookup"><span data-stu-id="f9101-138">*Toolbar (ActionPane) \[Optional\]*</span></span>

### <a name="core-components"></a><span data-ttu-id="f9101-139">コア コンポーネント</span><span class="sxs-lookup"><span data-stu-id="f9101-139">Core components</span></span>

<span data-ttu-id="f9101-140">正しいフィルターおよびツール バーのサブパターンをコンテナー コントロールに適用します。</span><span class="sxs-lookup"><span data-stu-id="f9101-140">Apply the correct Filters and Toolbar subpattern to the container control.</span></span>

### <a name="related-container-patterns"></a><span data-ttu-id="f9101-141">関連するコンテナー パターン</span><span class="sxs-lookup"><span data-stu-id="f9101-141">Related container patterns</span></span>

-   [<span data-ttu-id="f9101-142">フォーム パート セクション リスト</span><span class="sxs-lookup"><span data-stu-id="f9101-142">Form Part Section List</span></span>](section-list-form-pattern.md)
-   [<span data-ttu-id="f9101-143">セクション グラフ</span><span class="sxs-lookup"><span data-stu-id="f9101-143">Section Chart</span></span>](section-chart-form-pattern.md)

## <a name="ux-guidelines"></a><span data-ttu-id="f9101-144">UX ガイドライン</span><span class="sxs-lookup"><span data-stu-id="f9101-144">UX guidelines</span></span>
<span data-ttu-id="f9101-145">検証チェックリストには、フォームが UX ガイドラインに準拠しているかどうかを手動で確認する手順が示されています。</span><span class="sxs-lookup"><span data-stu-id="f9101-145">The verification checklist shows the steps for manually verifying that the form complies with UX guidelines.</span></span> <span data-ttu-id="f9101-146">このチェックリストには、開発環境を通じて自動的に実施されるガイドラインは含まれていません。</span><span class="sxs-lookup"><span data-stu-id="f9101-146">This checklist doesn't include any guidelines that will be enforced automatically through the development environment.</span></span> <span data-ttu-id="f9101-147">ブラウザーでフォームを開いて、これらの手順を確認します。</span><span class="sxs-lookup"><span data-stu-id="f9101-147">Open the form in the browser, and walk through these steps.</span></span>

-   <span data-ttu-id="f9101-148">**フィルターおよびツールバーのガイドライン**</span><span class="sxs-lookup"><span data-stu-id="f9101-148">**Filters and Toolbar guidelines**</span></span>
    -   <span data-ttu-id="f9101-149">**積み上げ** バリアントは、狭いリストおよびグラフで使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="f9101-149">The **Stacked** variant should be used over narrow lists and charts.</span></span>
    -   <span data-ttu-id="f9101-150">**インライン** バリアントは、より広いリストおよびグラフで使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="f9101-150">The **Inline** variant should be used over wider lists and charts.</span></span>
-   <span data-ttu-id="f9101-151">**フィルター**</span><span class="sxs-lookup"><span data-stu-id="f9101-151">**Filters**</span></span>
    -   <span data-ttu-id="f9101-152">2 つ以下のフィルター フィールドをフィルター グループで使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="f9101-152">No more than two filter fields should be used in a Filter group.</span></span> <span data-ttu-id="f9101-153">2 つ以上のフィルター フィールドが必要な場合、ツールバーのアクションを使用して、より多くのフィルター フィールドがあるドロップ ダイアログを開くことができます。</span><span class="sxs-lookup"><span data-stu-id="f9101-153">If you require more than two filter fields, an action on the Toolbar can be used to open a Drop Dialog that has more filter fields.</span></span>
    -   <span data-ttu-id="f9101-154">フィルター フィールドにはラベルを使用しないでください。</span><span class="sxs-lookup"><span data-stu-id="f9101-154">The filter fields should not have labels.</span></span> <span data-ttu-id="f9101-155">コンテキストは、フィールド値から明白でなければなりません。</span><span class="sxs-lookup"><span data-stu-id="f9101-155">The context should be obvious from the field value.</span></span>
    -   <span data-ttu-id="f9101-156">フィルター フィールドの幅を合わせて、セクションがセクション内のグリッドまたはグラフよりも大きくならないようにする必要があります。また、フィルターに余分なスクロールバーが発生しないようにする必要があります。</span><span class="sxs-lookup"><span data-stu-id="f9101-156">The combined width of filter fields should not cause the section to become larger than the grid or chart in the section, and should not cause an extra scrollbar on the filters.</span></span>
-   <span data-ttu-id="f9101-157">**操作**</span><span class="sxs-lookup"><span data-stu-id="f9101-157">**Actions**</span></span>
    -   <span data-ttu-id="f9101-158">ワークスペースでユーザーのタスク完了を支援する使用頻度の高いコマンドのみを含めます。</span><span class="sxs-lookup"><span data-stu-id="f9101-158">Include only frequently used commands that help users complete tasks in the workspace.</span></span>
    -   <span data-ttu-id="f9101-159">3 つ以下のアクションをツール バーに表示する必要があります。</span><span class="sxs-lookup"><span data-stu-id="f9101-159">No more than three actions should appear on the Toolbar.</span></span> <span data-ttu-id="f9101-160">ツールバーの 1 つのアクションは、最大 3 つの追加アクションのドロップダウン リストとして使用できます。</span><span class="sxs-lookup"><span data-stu-id="f9101-160">One action on the Toolbar can be used as a drop-down list of up to three additional actions.</span></span>

## <a name="examples"></a><span data-ttu-id="f9101-161">例</span><span class="sxs-lookup"><span data-stu-id="f9101-161">Examples</span></span>
### <a name="filters-and-toolbar---inline"></a><span data-ttu-id="f9101-162">フィルターおよびツールバー - インライン</span><span class="sxs-lookup"><span data-stu-id="f9101-162">Filters and Toolbar - Inline</span></span>

<span data-ttu-id="f9101-163">フォーム: **HcmWorkforceManagement** &gt; **HcmOpenPositionsPart** (**すべてのワークスペース** &gt; **要員管理**)</span><span class="sxs-lookup"><span data-stu-id="f9101-163">Form: **HcmWorkforceManagement**  &gt; **HcmOpenPositionsPart** (**All workspaces** &gt; **Workforce management**)</span></span> 

<span data-ttu-id="f9101-164">[![filterToolbarInline](./media/filtertoolbarinline.png)](./media/filtertoolbarinline.png)</span><span class="sxs-lookup"><span data-stu-id="f9101-164">[![filterToolbarInline](./media/filtertoolbarinline.png)](./media/filtertoolbarinline.png)</span></span>

### <a name="filters-and-toolbar---stacked"></a><span data-ttu-id="f9101-165">フィルターおよびツールバー - 積み上げ</span><span class="sxs-lookup"><span data-stu-id="f9101-165">Filters and Toolbar - Stacked</span></span>

<span data-ttu-id="f9101-166">フォーム: **HcmWorkforceManagement** &gt; **HcmWorkerOnLeaveListPart** (**すべてのワークスペース** &gt; **要員管理**)</span><span class="sxs-lookup"><span data-stu-id="f9101-166">Form: **HcmWorkforceManagement** &gt; **HcmWorkerOnLeaveListPart** (**All workspaces** &gt; **Workforce management**)</span></span> 

<span data-ttu-id="f9101-167">[![filterToolbarStacked](./media/filtertoolbarstacked.png)](./media/filtertoolbarstacked.png)</span><span class="sxs-lookup"><span data-stu-id="f9101-167">[![filterToolbarStacked](./media/filtertoolbarstacked.png)](./media/filtertoolbarstacked.png)</span></span>

## <a name="appendix"></a><span data-ttu-id="f9101-168">付録</span><span class="sxs-lookup"><span data-stu-id="f9101-168">Appendix</span></span>
### <a name="frequently-asked-questions"></a><span data-ttu-id="f9101-169">よく寄せられる質問</span><span class="sxs-lookup"><span data-stu-id="f9101-169">Frequently asked questions</span></span>

<span data-ttu-id="f9101-170">このセクションには、このガイドライン/パターンに関連するよくある質問への回答があります。</span><span class="sxs-lookup"><span data-stu-id="f9101-170">This section will have answers to frequently asked questions that are related to this guideline/pattern.</span></span>

### <a name="open-issues"></a><span data-ttu-id="f9101-171">未処理の問題</span><span class="sxs-lookup"><span data-stu-id="f9101-171">Open issues</span></span>

<span data-ttu-id="f9101-172">**なぜインライン バリアントはフィルター フィールドの任意の数を許可するのに、積み上げバリアントは最大 3 つまで許可するのでしょうか (QuickFilter および 2 つのカスタム フィルター)?**</span><span class="sxs-lookup"><span data-stu-id="f9101-172">**Why does the Inline variant allow for an arbitrary number of filter fields, but the Stacked variant allows a maximum of three (a QuickFilter and two custom filters)?**</span></span>

<span data-ttu-id="f9101-173">この不一致には 2 つの要因が関係します。</span><span class="sxs-lookup"><span data-stu-id="f9101-173">Two factors contribute to this discrepancy:</span></span>

-   <span data-ttu-id="f9101-174">UX のガイドラインは、これらのセクションに最大 2 つのフィルターを指定しています (それらのフィルターの一つは QuickFilter となる場合があります)。</span><span class="sxs-lookup"><span data-stu-id="f9101-174">A UX guideline specifies a maximum of two filters in these sections (and one of those filters could be a QuickFilter).</span></span> <span data-ttu-id="f9101-175">したがって、Stacked バリアントは、ガイドラインにより一層準拠しています。</span><span class="sxs-lookup"><span data-stu-id="f9101-175">Therefore, the Stacked variant more closely complies with the guideline.</span></span>
-   <span data-ttu-id="f9101-176">積み上げバリアントのフィールド数は、審美的な理由から制限されています。</span><span class="sxs-lookup"><span data-stu-id="f9101-176">The number of fields in the Stacked variant is limited for aesthetic reasons.</span></span> <span data-ttu-id="f9101-177">このバリアントのフィルター フィールドは、それらの下に表示されるリスト/チャートの全幅を占めることを意図しているため、その幅は **SizeToAvailable** です。</span><span class="sxs-lookup"><span data-stu-id="f9101-177">The filter fields in this variant are intended to take up the full width of the list/chart that appears below them, and their width is therefore **SizeToAvailable**.</span></span> <span data-ttu-id="f9101-178">このバリアントを限られたリストを超えて使用すると、その使用の目的にしたがって、2 つを超えるフィルター フィールドが使用された場合には、その設定によって非常に限られたフィルター フィールドが発生する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="f9101-178">When this variant is used above narrow lists, as it's intended to be used, that setting can cause very narrow filter fields when more than two filter fields are used.</span></span> <span data-ttu-id="f9101-179">インライン バリアントは、幅広いグラフ/リストの上で使用するためのものです。</span><span class="sxs-lookup"><span data-stu-id="f9101-179">The Inline variant is intended to be used above wider charts/lists.</span></span> <span data-ttu-id="f9101-180">したがって、元のパターン定義では、任意の数のフィールドが許可されていました。</span><span class="sxs-lookup"><span data-stu-id="f9101-180">Therefore, the original pattern definition allowed for an arbitrary number of fields.</span></span> <span data-ttu-id="f9101-181">ただし、今後 2 つのバリエーション間で許可されているフィルター フィールドの数におけるこの不一致に対応する予定です。</span><span class="sxs-lookup"><span data-stu-id="f9101-181">Nevertheless, we do plan to address this discrepancy in the number of allowed filter fields between the two variations in the future.</span></span>
