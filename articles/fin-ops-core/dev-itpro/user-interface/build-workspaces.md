---
title: 運用ワークスペースの構築
description: このトピックでは、ワークスペースと、運用ワークスペースを構築するために使用されるパターンとサブパターンの詳細について説明します。
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
ms.custom: 27111
ms.assetid: b8ddf156-eb7c-4010-95bd-16754cb1e122
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d094af70c7d72dfcfba0b8f2351100186bfb7a65
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/27/2019
ms.locfileid: "2183065"
---
# <a name="build-operational-workspaces"></a><span data-ttu-id="ce148-103">運用ワークスペースの構築</span><span class="sxs-lookup"><span data-stu-id="ce148-103">Build operational workspaces</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ce148-104">このトピックでは、ワークスペースと、運用ワークスペースを構築するために使用されるパターンとサブパターンの詳細について説明します。</span><span class="sxs-lookup"><span data-stu-id="ce148-104">This topic provides detailed information about workspaces and the patterns and subpatterns that are used to build operational workspaces.</span></span> 

<a name="overview"></a><span data-ttu-id="ce148-105">概要</span><span class="sxs-lookup"><span data-stu-id="ce148-105">Overview</span></span>
--------

### <a name="a-workspace-is-defined-as"></a><span data-ttu-id="ce148-106">ワークスペースは、次のように定義されています。</span><span class="sxs-lookup"><span data-stu-id="ce148-106">A workspace is defined as...</span></span>

-   <span data-ttu-id="ce148-107">プライマリ ナビゲーション メカニズムの一部。</span><span class="sxs-lookup"><span data-stu-id="ce148-107">Part of the primary navigation mechanism.</span></span>
-   <span data-ttu-id="ce148-108">事業活動 (ターゲット ユーザーの作業を構成するタスクの論理グループ) をサポートするフォーム。</span><span class="sxs-lookup"><span data-stu-id="ce148-108">A form that supports a business activity (a logical group of tasks that make up the work of a target persona).</span></span>
-   <span data-ttu-id="ce148-109">単純なタスクをワークスペースで直接完了できるようにすることで、活動の初期の概要を提供し、生産性を向上させる方法。</span><span class="sxs-lookup"><span data-stu-id="ce148-109">A way to provide an initial overview and to increase productivity in the activity by allowing simple tasks to be completed directly in the workspace.</span></span>

### <a name="workspaces-have-the-following-goals"></a><span data-ttu-id="ce148-110">ワークスペースには次の目的があります...</span><span class="sxs-lookup"><span data-stu-id="ce148-110">Workspaces have the following goals...</span></span>

-   <span data-ttu-id="ce148-111">情報に基づいた意思決定をサポートするために、ユーザーがアクティビティの現在の状態を理解できるようにします。</span><span class="sxs-lookup"><span data-stu-id="ce148-111">Enable the user to understand the current state of the activity to support informed decisions.</span></span>
-   <span data-ttu-id="ce148-112">データを選択することでユーザーを深いページに移動させ、情報のないページへのラウンド トリップを回避します。</span><span class="sxs-lookup"><span data-stu-id="ce148-112">Let users navigate to deeper pages by selecting data, which avoids round-trips to pages with no information.</span></span>
-   <span data-ttu-id="ce148-113">深いページへのラウンド トリップを回避するためにワークスペースでユーザーに軽いタスクを実行させます。</span><span class="sxs-lookup"><span data-stu-id="ce148-113">Let users perform light tasks in the workspaces to avoid round-trips to deeper pages.</span></span>
-   <span data-ttu-id="ce148-114">ワークスペースを離れることなく活動を完了します。</span><span class="sxs-lookup"><span data-stu-id="ce148-114">Complete an activity without leaving the workspace.</span></span>
-   <span data-ttu-id="ce148-115">ナビゲーションの必要性が減少します。</span><span class="sxs-lookup"><span data-stu-id="ce148-115">Reduce the need for navigation.</span></span>
-   <span data-ttu-id="ce148-116">ビジュアル効果を提供します。</span><span class="sxs-lookup"><span data-stu-id="ce148-116">Provide visual impact.</span></span>
-   <span data-ttu-id="ce148-117">最小限の COGS と迅速な応答時間をもたらす規範的なパターンとベスト プラクティスを使用して構築します。</span><span class="sxs-lookup"><span data-stu-id="ce148-117">Be constructed using prescriptive patterns and best practices that lead to minimal COGS and fast response times.</span></span>

<span data-ttu-id="ce148-118">[![WorkspaceDiagram\_OpWork](./media/workspacediagram_opwork.png)](./media/workspacediagram_opwork.png) これらの目標を達成するため、工程ワークスペース パターンが開発されました。</span><span class="sxs-lookup"><span data-stu-id="ce148-118">[![WorkspaceDiagram\_OpWork](./media/workspacediagram_opwork.png)](./media/workspacediagram_opwork.png) To accomplish these goals, the operation workspace pattern was developed.</span></span>

### <a name="examples"></a><span data-ttu-id="ce148-119">例</span><span class="sxs-lookup"><span data-stu-id="ce148-119">Examples</span></span>

<span data-ttu-id="ce148-120">ワークスペースの例は、**フリート管理**の**予約管理** ワークスペースです。</span><span class="sxs-lookup"><span data-stu-id="ce148-120">An example of a workspace is the **Reservation management** workspace in **Fleet management**.</span></span> <span data-ttu-id="ce148-121">メニュー項目 **FMClerkWorkspace** にアクセスすることにより取得することができます。</span><span class="sxs-lookup"><span data-stu-id="ce148-121">You can get to it by accessing the menu item **FMClerkWorkspace**.</span></span>   <span data-ttu-id="ce148-122">上記のワークスペースには、次の項目があります。</span><span class="sxs-lookup"><span data-stu-id="ce148-122">The workspace, shown above, has the following items:</span></span>

-   <span data-ttu-id="ce148-123">**集計** - タイルとグラフが含まれています。</span><span class="sxs-lookup"><span data-stu-id="ce148-123">**Summary** - Contains tiles and a chart.</span></span>
-   <span data-ttu-id="ce148-124">**レンタル** - 3 ページから成る垂直タブ コントロールが含まれています。最初のページが選択され、右端に対応する内容が表示されます。</span><span class="sxs-lookup"><span data-stu-id="ce148-124">**Rentals** - Contains a vertical tab control having three pages - the first is selected, and you can see the corresponding content on the rightmost side.</span></span>
-   <span data-ttu-id="ce148-125">**統計** - 積み上げグラフを含みます。</span><span class="sxs-lookup"><span data-stu-id="ce148-125">**Statistics** - Contains stacked charts.</span></span>
-   <span data-ttu-id="ce148-126">**関連リンク** - このユーザーと活動に関連するフォームへのグループ化された一連のメニュー項目のリンクが含まれています。</span><span class="sxs-lookup"><span data-stu-id="ce148-126">**Related links** - Contains a series of grouped menu item links to forms of relevance to this user and activity.</span></span>

<span data-ttu-id="ce148-127">全体のフォームとその中の各セクションは、UX パターンとサブパターンを使用して定義されます。</span><span class="sxs-lookup"><span data-stu-id="ce148-127">The overall form, as well as each of the sections within, are defined using UX patterns and subpatterns.</span></span> <span data-ttu-id="ce148-128">対応するパターンについては、次のセクションで詳しく説明します。</span><span class="sxs-lookup"><span data-stu-id="ce148-128">The corresponding patterns are described in detail in the following sections.</span></span>

## <a name="patterns-and-subpatterns"></a><span data-ttu-id="ce148-129">パターンおよびサブパターン</span><span class="sxs-lookup"><span data-stu-id="ce148-129">Patterns and subpatterns</span></span>
<span data-ttu-id="ce148-130">オペレーション ワークスペースを作成するときは、その目的に合わせて定義されたパターンとサブパターンを使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="ce148-130">When building an operational workspace, you must use the patterns and subpatterns defined for that purpose.</span></span> <span data-ttu-id="ce148-131">これらのパターンとサブパターンは以下で説明します。</span><span class="sxs-lookup"><span data-stu-id="ce148-131">These patterns and subpatterns are described below.</span></span> <span data-ttu-id="ce148-132">一般に、コントロールがパターンの構造内で引用されている場合、共通名 (ControlType) \[カーディナリティ\]と示されます。カーディナリティが指定されていない場合、項目が 1 回だけ要求されます。</span><span class="sxs-lookup"><span data-stu-id="ce148-132">In general, when a control is cited within a pattern's structure, it'll be described as: Common name (ControlType) \[cardinality\] If cardinality isn't specified, then the item is required exactly once.</span></span> <span data-ttu-id="ce148-133">非常に単純なパターンおよびサブパターンでは構造ツリーが省略されています。</span><span class="sxs-lookup"><span data-stu-id="ce148-133">Very simple patterns and subpatterns have the structural tree omitted.</span></span>

### <a name="patterns"></a><span data-ttu-id="ce148-134">パターン</span><span class="sxs-lookup"><span data-stu-id="ce148-134">Patterns</span></span>

<span data-ttu-id="ce148-135">運用ワークスペースで使用するトップレベルのパターンがあります。</span><span class="sxs-lookup"><span data-stu-id="ce148-135">There are the top-level patterns for use with operational workspaces.</span></span>

#### <a name="workspace-operational"></a><span data-ttu-id="ce148-136">作業可能なワークスペース</span><span class="sxs-lookup"><span data-stu-id="ce148-136">Workspace Operational</span></span>

<span data-ttu-id="ce148-137">これは主な運用ワークスペース パターンであり、運用ワークスペース フォームの**設計**ノードに適用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="ce148-137">This is the primary operational workspace pattern and should be applied to the **Design** node of the operational workspace form.</span></span> <span data-ttu-id="ce148-138">次の構造を指定します。</span><span class="sxs-lookup"><span data-stu-id="ce148-138">It'll prescribe the following structure:</span></span>

-   <span data-ttu-id="ce148-139">デザイン</span><span class="sxs-lookup"><span data-stu-id="ce148-139">Design</span></span>
    -   <span data-ttu-id="ce148-140">ActionPane (ActionPane) \[0..\*\]</span><span class="sxs-lookup"><span data-stu-id="ce148-140">ActionPane (ActionPane) \[0..\*\]</span></span>
    -   <span data-ttu-id="ce148-141">ワークスペース ページ フィルター グループ (グループ) \[0..1\]</span><span class="sxs-lookup"><span data-stu-id="ce148-141">Workspace Page Filter Group (Group) \[0..1\]</span></span>
        -   <span data-ttu-id="ce148-142">サブパターン: ワークスペース ページ フィルター グループ</span><span class="sxs-lookup"><span data-stu-id="ce148-142">Subpattern: Workspace Page Filter Group</span></span>
    -   <span data-ttu-id="ce148-143">パノラマ (タブ)</span><span class="sxs-lookup"><span data-stu-id="ce148-143">Panorama (Tab)</span></span>
        -   <span data-ttu-id="ce148-144">セクション概要タイル (TabPage)</span><span class="sxs-lookup"><span data-stu-id="ce148-144">Section Summary Tiles (TabPage)</span></span>
            -   <span data-ttu-id="ce148-145">サブパターン: セクション タイル</span><span class="sxs-lookup"><span data-stu-id="ce148-145">Subpattern: Section tiles</span></span>
        -   <span data-ttu-id="ce148-146">セクション タブ付きリスト (TabPage)</span><span class="sxs-lookup"><span data-stu-id="ce148-146">Section Tabbed List (TabPage)</span></span>
            -   <span data-ttu-id="ce148-147">サブパターン: セクション タブ付きリスト</span><span class="sxs-lookup"><span data-stu-id="ce148-147">Subpattern: Section Tabbed List</span></span>
        -   <span data-ttu-id="ce148-148">セクション グラフ (TabPage) \[0..1\]</span><span class="sxs-lookup"><span data-stu-id="ce148-148">Section Charts (TabPage) \[0..1\]</span></span>
            -   <span data-ttu-id="ce148-149">サブパターン: セクション積み上げグラフ</span><span class="sxs-lookup"><span data-stu-id="ce148-149">Subpattern: Section Stacked Chart</span></span>
        -   <span data-ttu-id="ce148-150">セクション関連リンク (TabPage)</span><span class="sxs-lookup"><span data-stu-id="ce148-150">Section Related Links (TabPage)</span></span>
            -   <span data-ttu-id="ce148-151">サブパターン: セクション関連リンク</span><span class="sxs-lookup"><span data-stu-id="ce148-151">Subpattern: Section Related Links</span></span>

#### <a name="form-part-section-list"></a><span data-ttu-id="ce148-152">フォーム パート セクション リスト</span><span class="sxs-lookup"><span data-stu-id="ce148-152">Form Part Section List</span></span>

<span data-ttu-id="ce148-153">このパターンは、リストを含む**フォーム パート**フォームに使用されます。</span><span class="sxs-lookup"><span data-stu-id="ce148-153">This pattern is used for **Form Part** forms containing a list.</span></span> <span data-ttu-id="ce148-154">これらのリストは、Worksapce 運用パターンのセクション タブ付きリスト TabPage 内で参照されます。</span><span class="sxs-lookup"><span data-stu-id="ce148-154">These lists are referenced within the Section Tabbed LIst TabPage in the Worksapce Operational pattern.</span></span>

-   <span data-ttu-id="ce148-155">デザイン</span><span class="sxs-lookup"><span data-stu-id="ce148-155">Design</span></span>
    -   <span data-ttu-id="ce148-156">ヘッダー グループ (グループ) \[0..1\]</span><span class="sxs-lookup"><span data-stu-id="ce148-156">Header Group (Group) \[0..1\]</span></span>
        -   <span data-ttu-id="ce148-157">サブパターン: フィルターおよびツール バー - インラインまたはサブパターン: フィルターおよびツール バー - 積み上げ</span><span class="sxs-lookup"><span data-stu-id="ce148-157">Subpattern: Filters and toolbar - Inline OR Subpattern: Filters and Toolbar - Stacked</span></span>
    -   <span data-ttu-id="ce148-158">コンテンツ グリッド (グリッド)</span><span class="sxs-lookup"><span data-stu-id="ce148-158">Content Grid (Grid)</span></span>
    -   <span data-ttu-id="ce148-159">既定のアクション ボタン ($Button - ボタンの種類) \[0..1\]</span><span class="sxs-lookup"><span data-stu-id="ce148-159">Default Action Button ($Button - any type of button) \[0..1\]</span></span>
    -   <span data-ttu-id="ce148-160">すべてのメニュー項目 (MenuFunctionButton) \[0..1\] を参照してください</span><span class="sxs-lookup"><span data-stu-id="ce148-160">See All Menu Item (MenuFunctionButton) \[0..1\]</span></span>

#### <a name="hub-part-chart"></a><span data-ttu-id="ce148-161">ハブ パート グラフ</span><span class="sxs-lookup"><span data-stu-id="ce148-161">Hub Part Chart</span></span>

<span data-ttu-id="ce148-162">このパターンは、チャート コントロールを含む**フォーム パート**フォームに使用されます。</span><span class="sxs-lookup"><span data-stu-id="ce148-162">This pattern is used for **Form Part** forms containing a chart control.</span></span> <span data-ttu-id="ce148-163">これらのチャート フォームは、2 つのサブパターン、セクション タイルとセクション積み上げグラフで参照されます。</span><span class="sxs-lookup"><span data-stu-id="ce148-163">These chart forms are referenced within two subpatterns: Section Tiles and Section Stacked Chart.</span></span> <span data-ttu-id="ce148-164">厳密に 1 つのグラフ コントロールが必要です。</span><span class="sxs-lookup"><span data-stu-id="ce148-164">It requires exactly one Chart control.</span></span>

### <a name="subpatterns"></a><span data-ttu-id="ce148-165">サブパターン</span><span class="sxs-lookup"><span data-stu-id="ce148-165">Subpatterns</span></span>

#### <a name="workspace-page-filter-group"></a><span data-ttu-id="ce148-166">ワークスペース ページ フィルター グループ</span><span class="sxs-lookup"><span data-stu-id="ce148-166">Workspace Page Filter Group</span></span>

<span data-ttu-id="ce148-167">このサブパターンは、運用ワークスペースパターンのワークスペース ページ フィルター グループで参照されます。</span><span class="sxs-lookup"><span data-stu-id="ce148-167">This subpattern is referenced in the pattern Workspace Operational, in Workspace Page Filter Group.</span></span> <span data-ttu-id="ce148-168">これは、単一の入力コントロールに使用でき、ワークスペースを全体としてフィルター処理するために使用できます。</span><span class="sxs-lookup"><span data-stu-id="ce148-168">It allows for a single input control, which can be used to filter the workspace as a whole.</span></span>

#### <a name="section-tiles"></a><span data-ttu-id="ce148-169">セクション タイル</span><span class="sxs-lookup"><span data-stu-id="ce148-169">Section Tiles</span></span>

<span data-ttu-id="ce148-170">このサブパターンは、運用ワークスペースパターンのセクション概要タイルで参照されます。</span><span class="sxs-lookup"><span data-stu-id="ce148-170">This subpattern is referenced in the pattern Workspace Operational, in Section Summary tiles.</span></span> <span data-ttu-id="ce148-171">これはタイルとグラフの両方に使用できます。</span><span class="sxs-lookup"><span data-stu-id="ce148-171">It allows for both tiles and charts.</span></span> <span data-ttu-id="ce148-172">任意の順序で、これらの任意の数を定義できます。</span><span class="sxs-lookup"><span data-stu-id="ce148-172">Any number of those can be defined, in any order.</span></span> <span data-ttu-id="ce148-173">タイルは TileButton コントロールで定義され、チャートはフォーム パーツ コントロールで定義されます。</span><span class="sxs-lookup"><span data-stu-id="ce148-173">Tiles are defined with TileButton controls, and charts are defined with Form Part controls.</span></span> <span data-ttu-id="ce148-174">チャート フォーム パーツは、タイルが表示された状態で正しくチャートが流れるように、通常のタイルの分析コードと一致する必要があります。</span><span class="sxs-lookup"><span data-stu-id="ce148-174">A chart Form Part must have dimensions that match those of a normal tile, to ensure the chart flows correctly with the tiles displayed.</span></span>

#### <a name="section-tabbed-list"></a><span data-ttu-id="ce148-175">セクション タブ付きリスト</span><span class="sxs-lookup"><span data-stu-id="ce148-175">Section Tabbed List</span></span>

<span data-ttu-id="ce148-176">このサブパターンは、運用ワークスペースパターンのセクションタブ付きリンクで参照されます。</span><span class="sxs-lookup"><span data-stu-id="ce148-176">This subpattern is referenced in the pattern Workspace Operational, in Section Tabbed List.</span></span> <span data-ttu-id="ce148-177">これは、モデル化する複数のリスト コンテナーに使用でき、それぞれ最終的に目的のリストを含むフォームを指定するフォーム パーツを参照します。</span><span class="sxs-lookup"><span data-stu-id="ce148-177">It allows for multiple list containers to be modeled, each of which ultimately references a Form Part that points to a form containing the desired list.</span></span> <span data-ttu-id="ce148-178">次の構造が必要です。</span><span class="sxs-lookup"><span data-stu-id="ce148-178">It requires the following structure:</span></span>

-   <span data-ttu-id="ce148-179">タブ付きの一覧 (タブ)</span><span class="sxs-lookup"><span data-stu-id="ce148-179">Tabbed List (Tab)</span></span>
    -   <span data-ttu-id="ce148-180">Tabbed List Page (TabPage) \[0..\*\]</span><span class="sxs-lookup"><span data-stu-id="ce148-180">Tabbed List Page (TabPage) \[0..\*\]</span></span>
        -   <span data-ttu-id="ce148-181">フォーム パート セクション リスト (FormPartControl)。</span><span class="sxs-lookup"><span data-stu-id="ce148-181">Form Part Section List (FormPartControl).</span></span> <span data-ttu-id="ce148-182">**注記**: 参照されるフォームは、フォームのパターン、フォーム パート セクション リストを使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="ce148-182">**Note**: The referenced form must use the form pattern, Form Part Section List.</span></span>

#### <a name="section-stacked-chart"></a><span data-ttu-id="ce148-183">セクション積み上げグラフ</span><span class="sxs-lookup"><span data-stu-id="ce148-183">Section Stacked Chart</span></span>

<span data-ttu-id="ce148-184">このサブパターンは、運用ワークスペースパターンのセクション積み上げグラフで参照されます。</span><span class="sxs-lookup"><span data-stu-id="ce148-184">This subpattern is referenced in the pattern Workspace Operational, in Section Stacked Chart.</span></span> <span data-ttu-id="ce148-185">これは最大 2 つのグラフに使用でき、垂直積み上げ方向で表示されます。</span><span class="sxs-lookup"><span data-stu-id="ce148-185">It allows for up to two charts, which will be rendered in a vertically stacked orientation.</span></span> <span data-ttu-id="ce148-186">次の構造が必要です。</span><span class="sxs-lookup"><span data-stu-id="ce148-186">It requires the following structure:</span></span>

-   <span data-ttu-id="ce148-187">タブ ページ (TabPage)</span><span class="sxs-lookup"><span data-stu-id="ce148-187">Tab page (TabPage)</span></span>
    -   <span data-ttu-id="ce148-188">最初のグラフ FormPart (FormPartControl) \[0..1\]</span><span class="sxs-lookup"><span data-stu-id="ce148-188">First Chart FormPart (FormPartControl) \[0..1\]</span></span>
    -   <span data-ttu-id="ce148-189">2 番目のグラフ FormPart (FormPartControl) \[0..1\]</span><span class="sxs-lookup"><span data-stu-id="ce148-189">Second Chart FormPart (FormPartControl) \[0..1\]</span></span>

#### <a name="section-related-links"></a><span data-ttu-id="ce148-190">セクション関連リンク</span><span class="sxs-lookup"><span data-stu-id="ce148-190">Section Related Links</span></span>

<span data-ttu-id="ce148-191">このサブパターンは、運用ワークスペースパターンのセクション関連リンクで参照されます。</span><span class="sxs-lookup"><span data-stu-id="ce148-191">This subpattern is referenced in the pattern Workspace Operational, in Section Related Links.</span></span> <span data-ttu-id="ce148-192">これは 1 レベルの入れ子を持つ、一連のリンクに使用できます。</span><span class="sxs-lookup"><span data-stu-id="ce148-192">It allows for a series of links, with one level of nesting permitted.</span></span> <span data-ttu-id="ce148-193">次の構造が必要です。</span><span class="sxs-lookup"><span data-stu-id="ce148-193">It requires the following structure:</span></span>

-   <span data-ttu-id="ce148-194">タブ ページ (TabPage)</span><span class="sxs-lookup"><span data-stu-id="ce148-194">Tab page (TabPage)</span></span>
    -   <span data-ttu-id="ce148-195">メニュー機能ボタン (MenuFunctionButton) \[0..\*\]</span><span class="sxs-lookup"><span data-stu-id="ce148-195">Menu Function Button (MenuFunctionButton) \[0..\*\]</span></span>
    -   <span data-ttu-id="ce148-196">リンク グループ (グループ) \[0..\*\]</span><span class="sxs-lookup"><span data-stu-id="ce148-196">Links Group (Group) \[0..\*\]</span></span>
        -   <span data-ttu-id="ce148-197">メニュー機能ボタン (MenuFunctionButton) \[1..\*\]</span><span class="sxs-lookup"><span data-stu-id="ce148-197">Menu Function Button (MenuFunctionButton) \[1..\*\]</span></span>

#### <a name="filters-and-toolbar--inline"></a><span data-ttu-id="ce148-198">フィルターおよびツールバー – インライン</span><span class="sxs-lookup"><span data-stu-id="ce148-198">Filters and Toolbar – Inline</span></span>

<span data-ttu-id="ce148-199">このサブパターンは、ヘッダー グループのフォーム パターン セクション リストのパターンで参照されます。</span><span class="sxs-lookup"><span data-stu-id="ce148-199">This subpattern is referenced in the pattern Form Part Section List, in Header Group.</span></span> <span data-ttu-id="ce148-200">これは、すべての同じ行で一部のフィルターとツール バーに使用できます。</span><span class="sxs-lookup"><span data-stu-id="ce148-200">It allows for some filters and a toolbar, all on the same line.</span></span> <span data-ttu-id="ce148-201">次の構造が必要です。</span><span class="sxs-lookup"><span data-stu-id="ce148-201">It requires the following structure:</span></span>

-   <span data-ttu-id="ce148-202">グループ (グループ)</span><span class="sxs-lookup"><span data-stu-id="ce148-202">Group (Group)</span></span>
    -   <span data-ttu-id="ce148-203">フィルタ グループ (グループ) \[0..1\]</span><span class="sxs-lookup"><span data-stu-id="ce148-203">Filter Group (Group) \[0..1\]</span></span>
        -   <span data-ttu-id="ce148-204">簡易フィルター (QuickFilterControl) \[0..1\]</span><span class="sxs-lookup"><span data-stu-id="ce148-204">Quick Filter (QuickFilterControl) \[0..1\]</span></span>
        -   <span data-ttu-id="ce148-205">カスタム フィルター フィールド ($フィールド - フィールドの任意の種類) \[0..\*\]</span><span class="sxs-lookup"><span data-stu-id="ce148-205">Custom Filter Fields ($Field – any type of field) \[0..\*\]</span></span>
    -   <span data-ttu-id="ce148-206">ツールバー (ActionPane) \[0..1\]</span><span class="sxs-lookup"><span data-stu-id="ce148-206">Toolbar (ActionPane) \[0..1\]</span></span>

#### <a name="filters-and-toolbar---stacked"></a><span data-ttu-id="ce148-207">フィルターおよびツールバー - 積み上げ</span><span class="sxs-lookup"><span data-stu-id="ce148-207">Filters and Toolbar - Stacked</span></span>

<span data-ttu-id="ce148-208">このサブパターンは、ヘッダー グループのフォーム パターン セクション リスト パターンで参照されます。このサブパターンでは、1 つの行に複数のフィルター フィールドとこれらのフィルターの下の 1 つの行に 1 つのツールバーが許されます。</span><span class="sxs-lookup"><span data-stu-id="ce148-208">This subpattern is referenced in the pattern Form Part Section List, in the Header Group, It allows for some filter fields on one line, and a toolbar on a line below those filters.</span></span> <span data-ttu-id="ce148-209">次の構造が必要です。</span><span class="sxs-lookup"><span data-stu-id="ce148-209">It requires the following structure:</span></span>

-   <span data-ttu-id="ce148-210">グループ (グループ)</span><span class="sxs-lookup"><span data-stu-id="ce148-210">Group (Group)</span></span>
    -   <span data-ttu-id="ce148-211">フィルタ グループ (グループ) \[0..1\]</span><span class="sxs-lookup"><span data-stu-id="ce148-211">Filter Group (Group) \[0..1\]</span></span>
        -   <span data-ttu-id="ce148-212">簡易フィルター (QuickFilterControl) \[0..1\]</span><span class="sxs-lookup"><span data-stu-id="ce148-212">Quick Filter (QuickFilterControl) \[0..1\]</span></span>
        -   <span data-ttu-id="ce148-213">フィルター フィールド 1 ($Field - フィールドの任意の種類) \[0..1\]</span><span class="sxs-lookup"><span data-stu-id="ce148-213">Filter Field 1 ($Field - any type of field) \[0..1\]</span></span>
        -   <span data-ttu-id="ce148-214">フィルター フィールド 2 ($Field - フィールドの任意の種類) \[0..1\]</span><span class="sxs-lookup"><span data-stu-id="ce148-214">Filter Field 2 ($Field - any type of field) \[0..1\]</span></span>
    -   <span data-ttu-id="ce148-215">ツールバー (ActionPane) \[0..1\]</span><span class="sxs-lookup"><span data-stu-id="ce148-215">Toolbar (ActionPane) \[0..1\]</span></span>

### <a name="future-best-practices-check"></a><span data-ttu-id="ce148-216">将来のベスト プラクティスの確認</span><span class="sxs-lookup"><span data-stu-id="ce148-216">Future best practices check</span></span>

<span data-ttu-id="ce148-217">最終的にワークスペース用に構築されるベストプラクティス (BP) チェックがいくつかあります。</span><span class="sxs-lookup"><span data-stu-id="ce148-217">There are a few best practice (BP) checks that will eventually be built for workspaces.</span></span> <span data-ttu-id="ce148-218">これらのチェックは、パフォーマンスや設計上の理由から強く推奨されるアイテムについてユーザーに指導することを目的としています。</span><span class="sxs-lookup"><span data-stu-id="ce148-218">These checks are intended to provide guidance to the user about items that are strongly recommended for performance or design reasons.</span></span>

#### <a name="filters-are-covered-by-indexes"></a><span data-ttu-id="ce148-219">インデックスの対象となるフィルター</span><span class="sxs-lookup"><span data-stu-id="ce148-219">Filters are covered by indexes</span></span>

<span data-ttu-id="ce148-220">このチェックは、ワークスペース全体のフィルタ上のフィールドとして使用するようにモデル化されたフィールドがすべてインデックスでカバーされるようにするためのものです。</span><span class="sxs-lookup"><span data-stu-id="ce148-220">This check is intended to ensure that any field that is modeled for use as a field on a workspace-wide filter is covered by an index.</span></span> <span data-ttu-id="ce148-221">これにより、ユーザーがこれらのフィルターを利用した際のパフォーマンスが向上します。</span><span class="sxs-lookup"><span data-stu-id="ce148-221">This will help ensure that performance remains superior when users are taking advantage of these filters.</span></span>

#### <a name="chart-parts-only-contain-olap-charts"></a><span data-ttu-id="ce148-222">OLAP チャートのみが含まれているグラフ部品</span><span class="sxs-lookup"><span data-stu-id="ce148-222">Chart parts only contain OLAP charts</span></span>

<span data-ttu-id="ce148-223">ワークスペースにチャットが含まれているときは、そのチャットは分離したフォームとしてモデル化され、そのフォームはフォーム パーツ コントロールを使用してワークスペース上で参照されます。</span><span class="sxs-lookup"><span data-stu-id="ce148-223">When a workspace contains a chat, that chart is be modeled as a separate form, and that form is referenced on the workspace via a Form Part control.</span></span> <span data-ttu-id="ce148-224">このチェックの目的は、ワークスペースから最終的に参照されるチャートが OLAP データのみを使用するようにすることです。</span><span class="sxs-lookup"><span data-stu-id="ce148-224">The intent of this check is to ensure that any such charts ultimately referenced from a workspace are only using OLAP data.</span></span>

#### <a name="count-tiles-have-queries-defined"></a><span data-ttu-id="ce148-225">カウント タイルにはクエリが定義されています</span><span class="sxs-lookup"><span data-stu-id="ce148-225">Count tiles have queries defined</span></span>

<span data-ttu-id="ce148-226">これらのフォームは通常複数のカウント タイルを含むため、タイル キャッシュ システムは、ワークスペースのパフォーマンスを向上させるために実装されています。</span><span class="sxs-lookup"><span data-stu-id="ce148-226">A tile caching system has been implemented to improve performance of workspaces, as these forms generally contain several count tiles.</span></span> <span data-ttu-id="ce148-227">キャッシュ システムと共に正常に作動するこれらのカウント タイルについては、各タイルにはクエリが定義されている必要があります。</span><span class="sxs-lookup"><span data-stu-id="ce148-227">For these count tiles to work correctly with the caching system, each tile must have a query defined.</span></span> <span data-ttu-id="ce148-228">そのクエリは、タイル、またはタイルによって参照されるメニュー項目で定義されます。</span><span class="sxs-lookup"><span data-stu-id="ce148-228">That query may be defined on the tile or on the menu item referenced by the tile.</span></span> <span data-ttu-id="ce148-229">この BP チェックの目的は、すべてのカウント タイルについてこれらの 2 つの場所のいずれかにクエリが確実に定義されるようにすることです。</span><span class="sxs-lookup"><span data-stu-id="ce148-229">The intent of this BP check is to ensure a query is defined in one of these two locations for all count tiles.</span></span>



