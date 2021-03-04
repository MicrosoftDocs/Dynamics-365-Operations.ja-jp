---
title: フィルターおよびツールバーのサブパターン
description: このトピックでは、リストやグラフをホストするパノラマ セクション内のフィルターやアクションを表示する、フィルターおよびツール バーのサブパターンに関する情報を提供します。
author: jasongre
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.custom: 29191
ms.assetid: 8e32ba2f-6cc1-4bfd-9c79-42a8392fa812
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ec0d7743027cb4037102d7b0f00d6a3f744be946
ms.sourcegitcommit: 5192cfaedfd861faea63d8954d7bcc500608a225
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/30/2021
ms.locfileid: "5094227"
---
# <a name="filters-and-toolbar-subpatterns"></a><span data-ttu-id="81724-103">フィルターおよびツールバーのサブパターン</span><span class="sxs-lookup"><span data-stu-id="81724-103">Filters and Toolbar subpatterns</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="81724-104">このトピックでは、フィルターおよびツール バーのサブパターンについて説明します。</span><span class="sxs-lookup"><span data-stu-id="81724-104">This topic provides information about the Filters and Toolbar subpatterns.</span></span> <span data-ttu-id="81724-105">これらのワークスペース固有のサブパターンは、リストやグラフをホストする、パノラマ セクション内のフィルターやアクションを表示するために開発されました。</span><span class="sxs-lookup"><span data-stu-id="81724-105">These workspace-specific subpatterns have been developed to show filters and/or actions inside panorama sections that host lists and charts.</span></span>

<a name="usage"></a><span data-ttu-id="81724-106">用途</span><span class="sxs-lookup"><span data-stu-id="81724-106">Usage</span></span>
-----

<span data-ttu-id="81724-107">フィルターおよびツール バー サブパターンは、リストやグラフをホストする、パノラマ セクション内のフィルターやアクションを表示するために開発されたワークスペース固有のサブパターンです。</span><span class="sxs-lookup"><span data-stu-id="81724-107">The Filters and Toolbar subpatterns are workspace-specific subpatterns that have been developed to show filters and/or actions inside panorama sections that host lists and charts.</span></span> <span data-ttu-id="81724-108">これらのサブパターンのフィルタ処理の一部のフィールドは、次のフィールド タイプに限定される必要があります。</span><span class="sxs-lookup"><span data-stu-id="81724-108">Fields in the filtering parts of these subpatterns should be limited to the following field types.</span></span> <span data-ttu-id="81724-109">これらすべてのフィールド タイプは入力の制約を持ちクエリに適用できます。</span><span class="sxs-lookup"><span data-stu-id="81724-109">All these field types have constrained inputs and can be applied to the query.</span></span>

-   <span data-ttu-id="81724-110">Lookups を使用した StringEdits</span><span class="sxs-lookup"><span data-stu-id="81724-110">StringEdits with Lookups</span></span>
-   <span data-ttu-id="81724-111">日付フィールド</span><span class="sxs-lookup"><span data-stu-id="81724-111">Date fields</span></span>
-   <span data-ttu-id="81724-112">ReferenceGroup</span><span class="sxs-lookup"><span data-stu-id="81724-112">ReferenceGroup</span></span>
-   <span data-ttu-id="81724-113">Comboboxes</span><span class="sxs-lookup"><span data-stu-id="81724-113">Comboboxes</span></span>
-   <span data-ttu-id="81724-114">チェック ボックス</span><span class="sxs-lookup"><span data-stu-id="81724-114">Checkboxes</span></span>
-   <span data-ttu-id="81724-115">クイック フィルター</span><span class="sxs-lookup"><span data-stu-id="81724-115">Quick Filter</span></span>

<span data-ttu-id="81724-116">この記事では、2 つのサブパターンについて説明します。</span><span class="sxs-lookup"><span data-stu-id="81724-116">Two subpatterns are described in this article:</span></span>

-   <span data-ttu-id="81724-117">**フィルターおよびツールバー - インライン** – このサブパターンでは、フィルタ フィールドと同じ行に定義されたアクションが表示されます。</span><span class="sxs-lookup"><span data-stu-id="81724-117">**Filters and Toolbar - Inline** – In this subpattern, any defined actions appear on the same line as the filter fields.</span></span>
-   <span data-ttu-id="81724-118">**フィルターおよびツールバー (積み上げ)** – このサブパターンでは、フィルタ フィールドの下の別の行に定義されたアクションが表示されます。</span><span class="sxs-lookup"><span data-stu-id="81724-118">**Filters and Toolbar - Stacked** – In this subpattern, any defined actions appear on a separate line below the filter fields.</span></span>

## <a name="wireframe"></a><span data-ttu-id="81724-119">ワイヤーフレーム</span><span class="sxs-lookup"><span data-stu-id="81724-119">Wireframe</span></span>
### <a name="filters-and-toolbar---inline"></a><span data-ttu-id="81724-120">フィルターおよびツールバー - インライン</span><span class="sxs-lookup"><span data-stu-id="81724-120">Filters and Toolbar - Inline</span></span>

<span data-ttu-id="81724-121">[![フィルターとツール バーのワイヤフレーム -- インライン](./media/filtertoolbarinlinewireframe.png)](./media/filtertoolbarinlinewireframe.png)</span><span class="sxs-lookup"><span data-stu-id="81724-121">[![Wireframe for filters and toolbar--inline](./media/filtertoolbarinlinewireframe.png)](./media/filtertoolbarinlinewireframe.png)</span></span>

### <a name="filters-and-toolbar---stacked"></a><span data-ttu-id="81724-122">フィルターおよびツールバー - 積み上げ</span><span class="sxs-lookup"><span data-stu-id="81724-122">Filters and Toolbar - Stacked</span></span>

<span data-ttu-id="81724-123">[![フィルターとツール バーのワイヤフレーム -- 積み上げ](./media/filtertoolbarstackedwireframe.png)](./media/filtertoolbarstackedwireframe.png)</span><span class="sxs-lookup"><span data-stu-id="81724-123">[![Wireframe for filter and toolbar--stacked](./media/filtertoolbarstackedwireframe.png)](./media/filtertoolbarstackedwireframe.png)</span></span>

## <a name="model"></a><span data-ttu-id="81724-124">モデル</span><span class="sxs-lookup"><span data-stu-id="81724-124">Model</span></span>
### <a name="filters-and-toolbar---inline-high-level-structure"></a><span data-ttu-id="81724-125">フィルターおよびツールバー - インライン: 高度なレベル構造</span><span class="sxs-lookup"><span data-stu-id="81724-125">Filters and Toolbar - Inline: High-level structure</span></span>

- <span data-ttu-id="81724-126">グループ (ArrangeMethod=HorizontalLeft)</span><span class="sxs-lookup"><span data-stu-id="81724-126">Group (ArrangeMethod=HorizontalLeft)</span></span>

    - <span data-ttu-id="81724-127">*FilterGroup (グループ) \[オプション\]*</span><span class="sxs-lookup"><span data-stu-id="81724-127">*FilterGroup (Group) \[Optional\]*</span></span>

        - <span data-ttu-id="81724-128">*QuickFilter (QuickFilter) \[オプション\]*</span><span class="sxs-lookup"><span data-stu-id="81724-128">*QuickFilter (QuickFilter) \[Optional\]*</span></span>
        - <span data-ttu-id="81724-129">*フィールド ($ フィールド)\[0..N\]*</span><span class="sxs-lookup"><span data-stu-id="81724-129">*FilterFIelds ($Field) \[0..N\]*</span></span>

    - <span data-ttu-id="81724-130">*ツール バー (ActionPane) \[オプション\]*</span><span class="sxs-lookup"><span data-stu-id="81724-130">*Toolbar (ActionPane) \[Optional\]*</span></span>

### <a name="filters-and-toolbar---stacked-high-level-structure"></a><span data-ttu-id="81724-131">フィルターおよびツールバー - 積み上げ: 高度なレベル構造</span><span class="sxs-lookup"><span data-stu-id="81724-131">Filters and Toolbar - Stacked: High-level structure</span></span>

- <span data-ttu-id="81724-132">グループ (ArrangeMethod=Vertical)</span><span class="sxs-lookup"><span data-stu-id="81724-132">Group (ArrangeMethod=Vertical)</span></span>

    - <span data-ttu-id="81724-133">*FilterGroup (グループ) \[オプション\]*</span><span class="sxs-lookup"><span data-stu-id="81724-133">*FilterGroup (Group) \[Optional\]*</span></span>

        - <span data-ttu-id="81724-134">*QuickFilter (QuickFilter) \[オプション\]*</span><span class="sxs-lookup"><span data-stu-id="81724-134">*QuickFilter (QuickFilter) \[Optional\]*</span></span>
        - <span data-ttu-id="81724-135">*FilterField1 ($ フィールド) \[オプション\]*</span><span class="sxs-lookup"><span data-stu-id="81724-135">*FilterField1 ($Field) \[Optional\]*</span></span>
        - <span data-ttu-id="81724-136">*FilterField2 ($ フィールド) \[オプション\]*</span><span class="sxs-lookup"><span data-stu-id="81724-136">*FilterField2 ($Field) \[Optional\]*</span></span>

    - <span data-ttu-id="81724-137">*ツール バー (ActionPane) \[オプション\]*</span><span class="sxs-lookup"><span data-stu-id="81724-137">*Toolbar (ActionPane) \[Optional\]*</span></span>

### <a name="core-components"></a><span data-ttu-id="81724-138">コア コンポーネント</span><span class="sxs-lookup"><span data-stu-id="81724-138">Core components</span></span>

<span data-ttu-id="81724-139">正しいフィルターおよびツール バーのサブパターンをコンテナー コントロールに適用します。</span><span class="sxs-lookup"><span data-stu-id="81724-139">Apply the correct Filters and Toolbar subpattern to the container control.</span></span>

### <a name="related-container-patterns"></a><span data-ttu-id="81724-140">関連するコンテナー パターン</span><span class="sxs-lookup"><span data-stu-id="81724-140">Related container patterns</span></span>

-   [<span data-ttu-id="81724-141">フォーム パート セクション リスト</span><span class="sxs-lookup"><span data-stu-id="81724-141">Form Part Section List</span></span>](section-list-form-pattern.md)
-   [<span data-ttu-id="81724-142">セクション グラフ</span><span class="sxs-lookup"><span data-stu-id="81724-142">Section Chart</span></span>](section-chart-form-pattern.md)

## <a name="ux-guidelines"></a><span data-ttu-id="81724-143">UX ガイドライン</span><span class="sxs-lookup"><span data-stu-id="81724-143">UX guidelines</span></span>
<span data-ttu-id="81724-144">検証チェックリストには、フォームが UX ガイドラインに準拠しているかどうかを手動で確認する手順が示されています。</span><span class="sxs-lookup"><span data-stu-id="81724-144">The verification checklist shows the steps for manually verifying that the form complies with UX guidelines.</span></span> <span data-ttu-id="81724-145">このチェックリストには、開発環境を通じて自動的に実施されるガイドラインは含まれていません。</span><span class="sxs-lookup"><span data-stu-id="81724-145">This checklist doesn't include any guidelines that will be enforced automatically through the development environment.</span></span> <span data-ttu-id="81724-146">ブラウザーでフォームを開いて、これらの手順を確認します。</span><span class="sxs-lookup"><span data-stu-id="81724-146">Open the form in the browser, and walk through these steps.</span></span>

-   <span data-ttu-id="81724-147">**フィルターおよびツールバーのガイドライン**</span><span class="sxs-lookup"><span data-stu-id="81724-147">**Filters and Toolbar guidelines**</span></span>
    -   <span data-ttu-id="81724-148">**積み上げ** バリアントは、狭いリストおよびグラフで使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="81724-148">The **Stacked** variant should be used over narrow lists and charts.</span></span>
    -   <span data-ttu-id="81724-149">**インライン** バリアントは、より広いリストおよびグラフで使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="81724-149">The **Inline** variant should be used over wider lists and charts.</span></span>
-   <span data-ttu-id="81724-150">**フィルター**</span><span class="sxs-lookup"><span data-stu-id="81724-150">**Filters**</span></span>
    -   <span data-ttu-id="81724-151">2 つ以下のフィルター フィールドをフィルター グループで使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="81724-151">No more than two filter fields should be used in a Filter group.</span></span> <span data-ttu-id="81724-152">2 つ以上のフィルター フィールドが必要な場合、ツールバーのアクションを使用して、より多くのフィルター フィールドがあるドロップ ダイアログを開くことができます。</span><span class="sxs-lookup"><span data-stu-id="81724-152">If you require more than two filter fields, an action on the Toolbar can be used to open a Drop Dialog that has more filter fields.</span></span>
    -   <span data-ttu-id="81724-153">フィルター フィールドにはラベルを使用しないでください。</span><span class="sxs-lookup"><span data-stu-id="81724-153">The filter fields should not have labels.</span></span> <span data-ttu-id="81724-154">コンテキストは、フィールド値から明白でなければなりません。</span><span class="sxs-lookup"><span data-stu-id="81724-154">The context should be obvious from the field value.</span></span>
    -   <span data-ttu-id="81724-155">フィルター フィールドの幅を合わせて、セクションがセクション内のグリッドまたはグラフよりも大きくならないようにする必要があります。また、フィルターに余分なスクロールバーが発生しないようにする必要があります。</span><span class="sxs-lookup"><span data-stu-id="81724-155">The combined width of filter fields should not cause the section to become larger than the grid or chart in the section, and should not cause an extra scrollbar on the filters.</span></span>
-   <span data-ttu-id="81724-156">**操作**</span><span class="sxs-lookup"><span data-stu-id="81724-156">**Actions**</span></span>
    -   <span data-ttu-id="81724-157">ワークスペースでユーザーのタスク完了を支援する使用頻度の高いコマンドのみを含めます。</span><span class="sxs-lookup"><span data-stu-id="81724-157">Include only frequently used commands that help users complete tasks in the workspace.</span></span>
    -   <span data-ttu-id="81724-158">3 つ以下のアクションをツール バーに表示する必要があります。</span><span class="sxs-lookup"><span data-stu-id="81724-158">No more than three actions should appear on the Toolbar.</span></span> <span data-ttu-id="81724-159">ツールバーの 1 つのアクションは、最大 3 つの追加アクションのドロップダウン リストとして使用できます。</span><span class="sxs-lookup"><span data-stu-id="81724-159">One action on the Toolbar can be used as a drop-down list of up to three additional actions.</span></span>

## <a name="examples"></a><span data-ttu-id="81724-160">例</span><span class="sxs-lookup"><span data-stu-id="81724-160">Examples</span></span>
### <a name="filters-and-toolbar---inline"></a><span data-ttu-id="81724-161">フィルターおよびツールバー - インライン</span><span class="sxs-lookup"><span data-stu-id="81724-161">Filters and Toolbar - Inline</span></span>

<span data-ttu-id="81724-162">フォーム: **HcmWorkforceManagement** &gt; **HcmOpenPositionsPart** (**すべてのワークスペース** &gt; **要員管理**)</span><span class="sxs-lookup"><span data-stu-id="81724-162">Form: **HcmWorkforceManagement**  &gt; **HcmOpenPositionsPart** (**All workspaces** &gt; **Workforce management**)</span></span> 

<span data-ttu-id="81724-163">[![フィルターとツールバーの例 -- インライン](./media/filtertoolbarinline.png)](./media/filtertoolbarinline.png)</span><span class="sxs-lookup"><span data-stu-id="81724-163">[![Example of filter and toolbar--inline](./media/filtertoolbarinline.png)](./media/filtertoolbarinline.png)</span></span>

### <a name="filters-and-toolbar---stacked"></a><span data-ttu-id="81724-164">フィルターおよびツールバー - 積み上げ</span><span class="sxs-lookup"><span data-stu-id="81724-164">Filters and Toolbar - Stacked</span></span>

<span data-ttu-id="81724-165">フォーム: **HcmWorkforceManagement** &gt; **HcmWorkerOnLeaveListPart** (**すべてのワークスペース** &gt; **要員管理**)</span><span class="sxs-lookup"><span data-stu-id="81724-165">Form: **HcmWorkforceManagement** &gt; **HcmWorkerOnLeaveListPart** (**All workspaces** &gt; **Workforce management**)</span></span> 

<span data-ttu-id="81724-166">[![フィルターとツールバーの例 -- 積み上げ](./media/filtertoolbarstacked.png)](./media/filtertoolbarstacked.png)</span><span class="sxs-lookup"><span data-stu-id="81724-166">[![Example of filter and toolbar--stacked](./media/filtertoolbarstacked.png)](./media/filtertoolbarstacked.png)</span></span>

## <a name="appendix"></a><span data-ttu-id="81724-167">付録</span><span class="sxs-lookup"><span data-stu-id="81724-167">Appendix</span></span>
### <a name="frequently-asked-questions"></a><span data-ttu-id="81724-168">よく寄せられる質問</span><span class="sxs-lookup"><span data-stu-id="81724-168">Frequently asked questions</span></span>

<span data-ttu-id="81724-169">このセクションには、このガイドライン/パターンに関連するよくある質問への回答があります。</span><span class="sxs-lookup"><span data-stu-id="81724-169">This section will have answers to frequently asked questions that are related to this guideline/pattern.</span></span>

### <a name="open-issues"></a><span data-ttu-id="81724-170">未処理の問題</span><span class="sxs-lookup"><span data-stu-id="81724-170">Open issues</span></span>

<span data-ttu-id="81724-171">**なぜインライン バリアントはフィルター フィールドの任意の数を許可するのに、積み上げバリアントは最大 3 つまで許可するのでしょうか (QuickFilter および 2 つのカスタム フィルター)?**</span><span class="sxs-lookup"><span data-stu-id="81724-171">**Why does the Inline variant allow for an arbitrary number of filter fields, but the Stacked variant allows a maximum of three (a QuickFilter and two custom filters)?**</span></span>

<span data-ttu-id="81724-172">この不一致には 2 つの要因が関係します。</span><span class="sxs-lookup"><span data-stu-id="81724-172">Two factors contribute to this discrepancy:</span></span>

-   <span data-ttu-id="81724-173">UX のガイドラインは、これらのセクションに最大 2 つのフィルターを指定しています (それらのフィルターの一つは QuickFilter となる場合があります)。</span><span class="sxs-lookup"><span data-stu-id="81724-173">A UX guideline specifies a maximum of two filters in these sections (and one of those filters could be a QuickFilter).</span></span> <span data-ttu-id="81724-174">したがって、Stacked バリアントは、ガイドラインにより一層準拠しています。</span><span class="sxs-lookup"><span data-stu-id="81724-174">Therefore, the Stacked variant more closely complies with the guideline.</span></span>
-   <span data-ttu-id="81724-175">積み上げバリアントのフィールド数は、審美的な理由から制限されています。</span><span class="sxs-lookup"><span data-stu-id="81724-175">The number of fields in the Stacked variant is limited for aesthetic reasons.</span></span> <span data-ttu-id="81724-176">このバリアントのフィルター フィールドは、それらの下に表示されるリスト/チャートの全幅を占めることを意図しているため、その幅は **SizeToAvailable** です。</span><span class="sxs-lookup"><span data-stu-id="81724-176">The filter fields in this variant are intended to take up the full width of the list/chart that appears below them, and their width is therefore **SizeToAvailable**.</span></span> <span data-ttu-id="81724-177">このバリアントを限られたリストを超えて使用すると、その使用の目的にしたがって、2 つを超えるフィルター フィールドが使用された場合には、その設定によって非常に限られたフィルター フィールドが発生する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="81724-177">When this variant is used above narrow lists, as it's intended to be used, that setting can cause very narrow filter fields when more than two filter fields are used.</span></span> <span data-ttu-id="81724-178">インライン バリアントは、幅広いグラフ/リストの上で使用するためのものです。</span><span class="sxs-lookup"><span data-stu-id="81724-178">The Inline variant is intended to be used above wider charts/lists.</span></span> <span data-ttu-id="81724-179">したがって、元のパターン定義では、任意の数のフィールドが許可されていました。</span><span class="sxs-lookup"><span data-stu-id="81724-179">Therefore, the original pattern definition allowed for an arbitrary number of fields.</span></span> <span data-ttu-id="81724-180">ただし、今後 2 つのバリエーション間で許可されているフィルター フィールドの数におけるこの不一致に対応する予定です。</span><span class="sxs-lookup"><span data-stu-id="81724-180">Nevertheless, we do plan to address this discrepancy in the number of allowed filter fields between the two variations in the future.</span></span>
