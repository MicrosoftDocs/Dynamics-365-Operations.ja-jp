---
title: フィルターおよびツールバーのサブパターン
description: この記事では、フィルターおよびツールバーのサブパターンについて説明します。 これらのワークスペース固有のサブパターンは、リストやグラフをホストする、パノラマ セクション内のフィルターやアクションを表示するために開発されました。
author: jasongre
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: robinr
ms.search.scope: Operations
ms.custom: 29191
ms.assetid: 8e32ba2f-6cc1-4bfd-9c79-42a8392fa812
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 7f973e4d4095fe6506aa34552702e2c721a4a5d6
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/07/2019
ms.locfileid: "1506057"
---
# <a name="filters-and-toolbar-subpatterns"></a><span data-ttu-id="5295a-104">フィルターおよびツールバーのサブパターン</span><span class="sxs-lookup"><span data-stu-id="5295a-104">Filters and Toolbar subpatterns</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="5295a-105">この記事では、フィルターおよびツールバーのサブパターンについて説明します。</span><span class="sxs-lookup"><span data-stu-id="5295a-105">This article provides information about the Filters and Toolbar subpatterns.</span></span> <span data-ttu-id="5295a-106">これらのワークスペース固有のサブパターンは、リストやグラフをホストする、パノラマ セクション内のフィルターやアクションを表示するために開発されました。</span><span class="sxs-lookup"><span data-stu-id="5295a-106">These workspace-specific subpatterns have been developed to show filters and/or actions inside panorama sections that host lists and charts.</span></span>

<a name="usage"></a><span data-ttu-id="5295a-107">用途</span><span class="sxs-lookup"><span data-stu-id="5295a-107">Usage</span></span>
-----

<span data-ttu-id="5295a-108">フィルターおよびツール バー サブパターンは、リストやグラフをホストする、パノラマ セクション内のフィルターやアクションを表示するために開発されたワークスペース固有のサブパターンです。</span><span class="sxs-lookup"><span data-stu-id="5295a-108">The Filters and Toolbar subpatterns are workspace-specific subpatterns that have been developed to show filters and/or actions inside panorama sections that host lists and charts.</span></span> <span data-ttu-id="5295a-109">これらのサブパターンのフィルタ処理の一部のフィールドは、次のフィールド タイプに限定される必要があります。</span><span class="sxs-lookup"><span data-stu-id="5295a-109">Fields in the filtering parts of these subpatterns should be limited to the following field types.</span></span> <span data-ttu-id="5295a-110">これらすべてのフィールド タイプは入力の制約を持ちクエリに適用できます。</span><span class="sxs-lookup"><span data-stu-id="5295a-110">All these field types have constrained inputs and can be applied to the query.</span></span>

-   <span data-ttu-id="5295a-111">Lookups を使用した StringEdits</span><span class="sxs-lookup"><span data-stu-id="5295a-111">StringEdits with Lookups</span></span>
-   <span data-ttu-id="5295a-112">日付フィールド</span><span class="sxs-lookup"><span data-stu-id="5295a-112">Date fields</span></span>
-   <span data-ttu-id="5295a-113">ReferenceGroup</span><span class="sxs-lookup"><span data-stu-id="5295a-113">ReferenceGroup</span></span>
-   <span data-ttu-id="5295a-114">Comboboxes</span><span class="sxs-lookup"><span data-stu-id="5295a-114">Comboboxes</span></span>
-   <span data-ttu-id="5295a-115">チェック ボックス</span><span class="sxs-lookup"><span data-stu-id="5295a-115">Checkboxes</span></span>
-   <span data-ttu-id="5295a-116">クイック フィルター</span><span class="sxs-lookup"><span data-stu-id="5295a-116">Quick Filter</span></span>

<span data-ttu-id="5295a-117">この記事では、2 つのサブパターンについて説明します。</span><span class="sxs-lookup"><span data-stu-id="5295a-117">Two subpatterns are described in this article:</span></span>

-   <span data-ttu-id="5295a-118">**フィルターおよびツールバー - インライン** – このサブパターンでは、フィルタ フィールドと同じ行に定義されたアクションが表示されます。</span><span class="sxs-lookup"><span data-stu-id="5295a-118">**Filters and Toolbar - Inline** – In this subpattern, any defined actions appear on the same line as the filter fields.</span></span>
-   <span data-ttu-id="5295a-119">**フィルターおよびツールバー (積み上げ)** – このサブパターンでは、フィルタ フィールドの下の別の行に定義されたアクションが表示されます。</span><span class="sxs-lookup"><span data-stu-id="5295a-119">**Filters and Toolbar - Stacked** – In this subpattern, any defined actions appear on a separate line below the filter fields.</span></span>

## <a name="wireframe"></a><span data-ttu-id="5295a-120">ワイヤーフレーム</span><span class="sxs-lookup"><span data-stu-id="5295a-120">Wireframe</span></span>
### <a name="filters-and-toolbar---inline"></a><span data-ttu-id="5295a-121">フィルターおよびツールバー - インライン</span><span class="sxs-lookup"><span data-stu-id="5295a-121">Filters and Toolbar - Inline</span></span>

<span data-ttu-id="5295a-122">[![filterToolbarInlineWireframe](./media/filtertoolbarinlinewireframe.png)](./media/filtertoolbarinlinewireframe.png)</span><span class="sxs-lookup"><span data-stu-id="5295a-122">[![filterToolbarInlineWireframe](./media/filtertoolbarinlinewireframe.png)](./media/filtertoolbarinlinewireframe.png)</span></span>

### <a name="filters-and-toolbar---stacked"></a><span data-ttu-id="5295a-123">フィルターおよびツールバー - 積み上げ</span><span class="sxs-lookup"><span data-stu-id="5295a-123">Filters and Toolbar - Stacked</span></span>

<span data-ttu-id="5295a-124">[![filterToolbarStackedWireframe](./media/filtertoolbarstackedwireframe.png)](./media/filtertoolbarstackedwireframe.png)</span><span class="sxs-lookup"><span data-stu-id="5295a-124">[![filterToolbarStackedWireframe](./media/filtertoolbarstackedwireframe.png)](./media/filtertoolbarstackedwireframe.png)</span></span>

## <a name="pattern-changes-for-microsoft-dynamics-365-for-finance-and-operations"></a><span data-ttu-id="5295a-125">Microsoft Dynamics 365 for Finance and Operations 用のパターンの変更</span><span class="sxs-lookup"><span data-stu-id="5295a-125">Pattern changes for Microsoft Dynamics 365 for Finance and Operations</span></span>
<span data-ttu-id="5295a-126">これらのパターンは、Microsoft DynamicsAX 2012 では存在しませんでした。</span><span class="sxs-lookup"><span data-stu-id="5295a-126">These patterns didn't exist for Microsoft Dynamics AX 2012.</span></span>

## <a name="model"></a><span data-ttu-id="5295a-127">モデル</span><span class="sxs-lookup"><span data-stu-id="5295a-127">Model</span></span>
### <a name="filters-and-toolbar---inline-high-level-structure"></a><span data-ttu-id="5295a-128">フィルターおよびツールバー - インライン: 高度なレベル構造</span><span class="sxs-lookup"><span data-stu-id="5295a-128">Filters and Toolbar - Inline: High-level structure</span></span>

- <span data-ttu-id="5295a-129">グループ (ArrangeMethod=HorizontalLeft)</span><span class="sxs-lookup"><span data-stu-id="5295a-129">Group (ArrangeMethod=HorizontalLeft)</span></span>

    - <span data-ttu-id="5295a-130">*FilterGroup (グループ) \[オプション\]*</span><span class="sxs-lookup"><span data-stu-id="5295a-130">*FilterGroup (Group) \[Optional\]*</span></span>

        - <span data-ttu-id="5295a-131">*QuickFilter (QuickFilter) \[オプション\]*</span><span class="sxs-lookup"><span data-stu-id="5295a-131">*QuickFilter (QuickFilter) \[Optional\]*</span></span>
        - <span data-ttu-id="5295a-132">*フィールド ($ フィールド)\[0..N\]*</span><span class="sxs-lookup"><span data-stu-id="5295a-132">*FilterFIelds ($Field) \[0..N\]*</span></span>

    - <span data-ttu-id="5295a-133">*ツール バー (ActionPane) \[オプション\]*</span><span class="sxs-lookup"><span data-stu-id="5295a-133">*Toolbar (ActionPane) \[Optional\]*</span></span>

### <a name="filters-and-toolbar---stacked-high-level-structure"></a><span data-ttu-id="5295a-134">フィルターおよびツールバー - 積み上げ: 高度なレベル構造</span><span class="sxs-lookup"><span data-stu-id="5295a-134">Filters and Toolbar - Stacked: High-level structure</span></span>

- <span data-ttu-id="5295a-135">グループ (ArrangeMethod=Vertical)</span><span class="sxs-lookup"><span data-stu-id="5295a-135">Group (ArrangeMethod=Vertical)</span></span>

    - <span data-ttu-id="5295a-136">*FilterGroup (グループ) \[オプション\]*</span><span class="sxs-lookup"><span data-stu-id="5295a-136">*FilterGroup (Group) \[Optional\]*</span></span>

        - <span data-ttu-id="5295a-137">*QuickFilter (QuickFilter) \[オプション\]*</span><span class="sxs-lookup"><span data-stu-id="5295a-137">*QuickFilter (QuickFilter) \[Optional\]*</span></span>
        - <span data-ttu-id="5295a-138">*FilterField1 ($ フィールド) \[オプション\]*</span><span class="sxs-lookup"><span data-stu-id="5295a-138">*FilterField1 ($Field) \[Optional\]*</span></span>
        - <span data-ttu-id="5295a-139">*FilterField2 ($ フィールド) \[オプション\]*</span><span class="sxs-lookup"><span data-stu-id="5295a-139">*FilterField2 ($Field) \[Optional\]*</span></span>

    - <span data-ttu-id="5295a-140">*ツール バー (ActionPane) \[オプション\]*</span><span class="sxs-lookup"><span data-stu-id="5295a-140">*Toolbar (ActionPane) \[Optional\]*</span></span>

### <a name="core-components"></a><span data-ttu-id="5295a-141">コア コンポーネント</span><span class="sxs-lookup"><span data-stu-id="5295a-141">Core components</span></span>

<span data-ttu-id="5295a-142">正しいフィルターおよびツール バーのサブパターンをコンテナー コントロールに適用します。</span><span class="sxs-lookup"><span data-stu-id="5295a-142">Apply the correct Filters and Toolbar subpattern to the container control.</span></span>

### <a name="related-container-patterns"></a><span data-ttu-id="5295a-143">関連するコンテナー パターン</span><span class="sxs-lookup"><span data-stu-id="5295a-143">Related container patterns</span></span>

-   [<span data-ttu-id="5295a-144">フォーム パート セクション リスト</span><span class="sxs-lookup"><span data-stu-id="5295a-144">Form Part Section List</span></span>](section-list-form-pattern.md)
-   [<span data-ttu-id="5295a-145">セクション グラフ</span><span class="sxs-lookup"><span data-stu-id="5295a-145">Section Chart</span></span>](section-chart-form-pattern.md)

## <a name="ux-guidelines"></a><span data-ttu-id="5295a-146">UX ガイドライン</span><span class="sxs-lookup"><span data-stu-id="5295a-146">UX guidelines</span></span>
<span data-ttu-id="5295a-147">検証チェックリストには、フォームが UX ガイドラインに準拠しているかどうかを手動で確認する手順が示されています。</span><span class="sxs-lookup"><span data-stu-id="5295a-147">The verification checklist shows the steps for manually verifying that the form complies with UX guidelines.</span></span> <span data-ttu-id="5295a-148">このチェックリストには、開発環境を通じて自動的に実施されるガイドラインは含まれていません。</span><span class="sxs-lookup"><span data-stu-id="5295a-148">This checklist doesn't include any guidelines that will be enforced automatically through the development environment.</span></span> <span data-ttu-id="5295a-149">ブラウザーでフォームを開いて、これらの手順を確認します。</span><span class="sxs-lookup"><span data-stu-id="5295a-149">Open the form in the browser, and walk through these steps.</span></span>

-   <span data-ttu-id="5295a-150">**フィルターおよびツールバーのガイドライン**</span><span class="sxs-lookup"><span data-stu-id="5295a-150">**Filters and Toolbar guidelines**</span></span>
    -   <span data-ttu-id="5295a-151">**積み上げ** バリアントは、狭いリストおよびグラフで使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="5295a-151">The **Stacked** variant should be used over narrow lists and charts.</span></span>
    -   <span data-ttu-id="5295a-152">**インライン** バリアントは、より広いリストおよびグラフで使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="5295a-152">The **Inline** variant should be used over wider lists and charts.</span></span>
-   <span data-ttu-id="5295a-153">**フィルター**</span><span class="sxs-lookup"><span data-stu-id="5295a-153">**Filters**</span></span>
    -   <span data-ttu-id="5295a-154">2 つ以下のフィルター フィールドをフィルター グループで使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="5295a-154">No more than two filter fields should be used in a Filter group.</span></span> <span data-ttu-id="5295a-155">2 つ以上のフィルター フィールドが必要な場合、ツールバーのアクションを使用して、より多くのフィルター フィールドがあるドロップ ダイアログを開くことができます。</span><span class="sxs-lookup"><span data-stu-id="5295a-155">If you require more than two filter fields, an action on the Toolbar can be used to open a Drop Dialog that has more filter fields.</span></span>
    -   <span data-ttu-id="5295a-156">フィルター フィールドにはラベルを使用しないでください。</span><span class="sxs-lookup"><span data-stu-id="5295a-156">The filter fields should not have labels.</span></span> <span data-ttu-id="5295a-157">コンテキストは、フィールド値から明白でなければなりません。</span><span class="sxs-lookup"><span data-stu-id="5295a-157">The context should be obvious from the field value.</span></span>
    -   <span data-ttu-id="5295a-158">フィルター フィールドの幅を合わせて、セクションがセクション内のグリッドまたはグラフよりも大きくならないようにする必要があります。また、フィルターに余分なスクロールバーが発生しないようにする必要があります。</span><span class="sxs-lookup"><span data-stu-id="5295a-158">The combined width of filter fields should not cause the section to become larger than the grid or chart in the section, and should not cause an extra scrollbar on the filters.</span></span>
-   <span data-ttu-id="5295a-159">**操作**</span><span class="sxs-lookup"><span data-stu-id="5295a-159">**Actions**</span></span>
    -   <span data-ttu-id="5295a-160">ワークスペースでユーザーのタスク完了を支援する使用頻度の高いコマンドのみを含めます。</span><span class="sxs-lookup"><span data-stu-id="5295a-160">Include only frequently used commands that help users complete tasks in the workspace.</span></span>
    -   <span data-ttu-id="5295a-161">3 つ以下のアクションをツール バーに表示する必要があります。</span><span class="sxs-lookup"><span data-stu-id="5295a-161">No more than three actions should appear on the Toolbar.</span></span> <span data-ttu-id="5295a-162">ツールバーの 1 つのアクションは、最大 3 つの追加アクションのドロップダウン リストとして使用できます。</span><span class="sxs-lookup"><span data-stu-id="5295a-162">One action on the Toolbar can be used as a drop-down list of up to three additional actions.</span></span>

## <a name="examples"></a><span data-ttu-id="5295a-163">例</span><span class="sxs-lookup"><span data-stu-id="5295a-163">Examples</span></span>
### <a name="filters-and-toolbar---inline"></a><span data-ttu-id="5295a-164">フィルターおよびツールバー - インライン</span><span class="sxs-lookup"><span data-stu-id="5295a-164">Filters and Toolbar - Inline</span></span>

<span data-ttu-id="5295a-165">フォーム: **HcmWorkforceManagement** &gt; **HcmOpenPositionsPart** (**すべてのワークスペース** &gt; **要員管理**)</span><span class="sxs-lookup"><span data-stu-id="5295a-165">Form: **HcmWorkforceManagement**  &gt; **HcmOpenPositionsPart** (**All workspaces** &gt; **Workforce management**)</span></span> 

<span data-ttu-id="5295a-166">[![filterToolbarInline](./media/filtertoolbarinline.png)](./media/filtertoolbarinline.png)</span><span class="sxs-lookup"><span data-stu-id="5295a-166">[![filterToolbarInline](./media/filtertoolbarinline.png)](./media/filtertoolbarinline.png)</span></span>

### <a name="filters-and-toolbar---stacked"></a><span data-ttu-id="5295a-167">フィルターおよびツールバー - 積み上げ</span><span class="sxs-lookup"><span data-stu-id="5295a-167">Filters and Toolbar - Stacked</span></span>

<span data-ttu-id="5295a-168">フォーム: **HcmWorkforceManagement** &gt; **HcmWorkerOnLeaveListPart** (**すべてのワークスペース** &gt; **要員管理**)</span><span class="sxs-lookup"><span data-stu-id="5295a-168">Form: **HcmWorkforceManagement** &gt; **HcmWorkerOnLeaveListPart** (**All workspaces** &gt; **Workforce management**)</span></span> 

<span data-ttu-id="5295a-169">[![filterToolbarStacked](./media/filtertoolbarstacked.png)](./media/filtertoolbarstacked.png)</span><span class="sxs-lookup"><span data-stu-id="5295a-169">[![filterToolbarStacked](./media/filtertoolbarstacked.png)](./media/filtertoolbarstacked.png)</span></span>

## <a name="appendix"></a><span data-ttu-id="5295a-170">付録</span><span class="sxs-lookup"><span data-stu-id="5295a-170">Appendix</span></span>
### <a name="frequently-asked-questions"></a><span data-ttu-id="5295a-171">よく寄せられる質問</span><span class="sxs-lookup"><span data-stu-id="5295a-171">Frequently asked questions</span></span>

<span data-ttu-id="5295a-172">このセクションには、このガイドライン/パターンに関連するよくある質問への回答があります。</span><span class="sxs-lookup"><span data-stu-id="5295a-172">This section will have answers to frequently asked questions that are related to this guideline/pattern.</span></span>

### <a name="open-issues"></a><span data-ttu-id="5295a-173">未処理の問題</span><span class="sxs-lookup"><span data-stu-id="5295a-173">Open issues</span></span>

<span data-ttu-id="5295a-174">**なぜインライン バリアントはフィルター フィールドの任意の数を許可するのに、積み上げバリアントは最大 3 つまで許可するのでしょうか (QuickFilter および 2 つのカスタム フィルター)?**</span><span class="sxs-lookup"><span data-stu-id="5295a-174">**Why does the Inline variant allow for an arbitrary number of filter fields, but the Stacked variant allows a maximum of three (a QuickFilter and two custom filters)?**</span></span>

<span data-ttu-id="5295a-175">この不一致には 2 つの要因が関係します。</span><span class="sxs-lookup"><span data-stu-id="5295a-175">Two factors contribute to this discrepancy:</span></span>

-   <span data-ttu-id="5295a-176">UX のガイドラインは、これらのセクションに最大 2 つのフィルターを指定しています (それらのフィルターの一つは QuickFilter となる場合があります)。</span><span class="sxs-lookup"><span data-stu-id="5295a-176">A UX guideline specifies a maximum of two filters in these sections (and one of those filters could be a QuickFilter).</span></span> <span data-ttu-id="5295a-177">したがって、Stacked バリアントは、ガイドラインにより一層準拠しています。</span><span class="sxs-lookup"><span data-stu-id="5295a-177">Therefore, the Stacked variant more closely complies with the guideline.</span></span>
-   <span data-ttu-id="5295a-178">積み上げバリアントのフィールド数は、審美的な理由から制限されています。</span><span class="sxs-lookup"><span data-stu-id="5295a-178">The number of fields in the Stacked variant is limited for aesthetic reasons.</span></span> <span data-ttu-id="5295a-179">このバリアントのフィルター フィールドは、それらの下に表示されるリスト/チャートの全幅を占めることを意図しているため、その幅は **SizeToAvailable** です。</span><span class="sxs-lookup"><span data-stu-id="5295a-179">The filter fields in this variant are intended to take up the full width of the list/chart that appears below them, and their width is therefore **SizeToAvailable**.</span></span> <span data-ttu-id="5295a-180">このバリアントを限られたリストを超えて使用すると、その使用の目的にしたがって、2 つを超えるフィルター フィールドが使用された場合には、その設定によって非常に限られたフィルター フィールドが発生する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="5295a-180">When this variant is used above narrow lists, as it's intended to be used, that setting can cause very narrow filter fields when more than two filter fields are used.</span></span> <span data-ttu-id="5295a-181">インライン バリアントは、幅広いグラフ/リストの上で使用するためのものです。</span><span class="sxs-lookup"><span data-stu-id="5295a-181">The Inline variant is intended to be used above wider charts/lists.</span></span> <span data-ttu-id="5295a-182">したがって、元のパターン定義では、任意の数のフィールドが許可されていました。</span><span class="sxs-lookup"><span data-stu-id="5295a-182">Therefore, the original pattern definition allowed for an arbitrary number of fields.</span></span> <span data-ttu-id="5295a-183">ただし、今後 2 つのバリエーション間で許可されているフィルター フィールドの数におけるこの不一致に対応する予定です。</span><span class="sxs-lookup"><span data-stu-id="5295a-183">Nevertheless, we do plan to address this discrepancy in the number of allowed filter fields between the two variations in the future.</span></span>
