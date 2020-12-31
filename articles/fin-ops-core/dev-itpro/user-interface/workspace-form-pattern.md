---
title: ワークスペースのフォーム パターン
description: このトピックでは、ワークスペース フォーム パターンについて説明します。 ワークスペースはユーザーがタスクと特定のページに移動する主な方法です。 ワークスペースは、サポートされている重要な事業活動ごとに作成する必要があります。
author: jasongre
manager: AnnBe
ms.date: 05/23/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.custom: 29151
ms.assetid: 4ca77c08-1c8f-4b0c-af55-ca89a7e8982b
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ebe0a7213194d6bcbe9e96ed9e326586099da733
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 12/05/2020
ms.locfileid: "4684985"
---
# <a name="workspace-form-pattern"></a><span data-ttu-id="ef7c5-105">ワークスペースのフォーム パターン</span><span class="sxs-lookup"><span data-stu-id="ef7c5-105">Workspace form pattern</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ef7c5-106">このトピックでは、ワークスペース フォーム パターンについて説明します。</span><span class="sxs-lookup"><span data-stu-id="ef7c5-106">This topic discusses workspace form patterns.</span></span> <span data-ttu-id="ef7c5-107">ワークスペースはユーザーがタスクと特定のページに移動する主な方法です。</span><span class="sxs-lookup"><span data-stu-id="ef7c5-107">Workspaces are the primary way that users navigate to tasks and specific pages.</span></span> <span data-ttu-id="ef7c5-108">ワークスペースは、サポートされている重要な事業活動ごとに作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="ef7c5-108">A workspace should be created for every significant business activity that is supported.</span></span>  

## <a name="usage"></a><span data-ttu-id="ef7c5-109">用途</span><span class="sxs-lookup"><span data-stu-id="ef7c5-109">Usage</span></span>

<span data-ttu-id="ef7c5-110">ワークスペースは新しい概念で、ユーザーがタスクと特定のページに移動する主な方法となることを意図しています。</span><span class="sxs-lookup"><span data-stu-id="ef7c5-110">Workspaces are a new concept, and are meant to be the primary way that users navigate to tasks and specific pages.</span></span> <span data-ttu-id="ef7c5-111">ワークスペースは、サポートする重要な事業「活動」ごとに作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="ef7c5-111">A workspace should be created for every significant business “activity” that you want to support.</span></span> <span data-ttu-id="ef7c5-112">「アクティビティ」はタスクよりも細かく従来の「エリア ページ」よりさらに細分化されています。</span><span class="sxs-lookup"><span data-stu-id="ef7c5-112">An “activity” is less granular than a task and more granular than a legacy “area page.”</span></span> <span data-ttu-id="ef7c5-113">ワークスペースは、1 ページの活動の概要を提供したり、ユーザーが現在の状態、今後の作業負荷、プロセスまたはユーザーのパフォーマンスを理解するよう助けるためのものです。</span><span class="sxs-lookup"><span data-stu-id="ef7c5-113">A workspace is intended to provide a one-page overview of the activity, and to help users understand the current status, the upcoming workload, and the performance of the process or user.</span></span> <span data-ttu-id="ef7c5-114">ユーザーは、その活動の最も一般的なタスクを、ワークスペースから直接開始できるようにする必要があります。</span><span class="sxs-lookup"><span data-stu-id="ef7c5-114">Users should be able to start the most typical tasks for the activity directly from the workspace.</span></span> <span data-ttu-id="ef7c5-115">可能であれば、ユーザーは、受信した概要に基づいて直接ワークスペースで、タスクを完了する必要があります。</span><span class="sxs-lookup"><span data-stu-id="ef7c5-115">If possible, users should also be able to complete tasks directly in the workspace, based on the overview that they just received.</span></span> <span data-ttu-id="ef7c5-116">現在、2 つのワークスペース パターンがあります。</span><span class="sxs-lookup"><span data-stu-id="ef7c5-116">Currently, there are two workspace patterns:</span></span>

-   <span data-ttu-id="ef7c5-117">**タブ付きワークスペース**: コンテンツに水平スクロール パノラマを強制せずに、このパターンは標準タブを使用して垂直スクロール ワークスペースの開発を許可します。</span><span class="sxs-lookup"><span data-stu-id="ef7c5-117">**Tabbed workspace**: Instead of forcing a horizontally-scrolling panorama for content, this pattern uses standard tabs to allow the development of vertically-scrolling workspaces.</span></span> <span data-ttu-id="ef7c5-118">これは、特に Power BI レポートをワークスペースに埋め込むために使用されています。</span><span class="sxs-lookup"><span data-stu-id="ef7c5-118">This is particularly being used to embed Power BI reports into workspaces.</span></span> <span data-ttu-id="ef7c5-119">これらのタブ内のコンテンツを定義するのに役立つ追加のサブパターンは、将来提供される可能性が高くなります。</span><span class="sxs-lookup"><span data-stu-id="ef7c5-119">Additional subpatterns to help define content inside these tabs will likely be provided in the future.</span></span>
-   <span data-ttu-id="ef7c5-120">**運用ワークスペース**: これは、ワークスペースの開発のために使用されている標準パターンです。</span><span class="sxs-lookup"><span data-stu-id="ef7c5-120">**Operational workspace**: This is the standard pattern currently used for workspace development.</span></span> <span data-ttu-id="ef7c5-121">許可されている一連のコンポーネントのため、このパターンは非推奨の「ワークスペース」パターンよりも優れたパフォーマンスがあります。</span><span class="sxs-lookup"><span data-stu-id="ef7c5-121">Because of the set of components that are permitted in it, this pattern has superior performance over the deprecated "workspace" pattern.</span></span> <span data-ttu-id="ef7c5-122">この理由および、システム内の他のワークスペースで視覚と行動の一貫性を確実にするため、このパターンを使用することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="ef7c5-122">For this reason and to ensure visual and behavioral consistency with the other workspaces in the system, we recommend that you use this pattern.</span></span>
-   <span data-ttu-id="ef7c5-123">(非推奨) **ワークスペース**: このパターンは、間違いがないように、念のため記載されています。</span><span class="sxs-lookup"><span data-stu-id="ef7c5-123">(Deprecated) **Workspace**: This pattern is only mentioned for the sake of completeness.</span></span> <span data-ttu-id="ef7c5-124">パターンを **使用しない** でください。</span><span class="sxs-lookup"><span data-stu-id="ef7c5-124">Do **not** use this pattern.</span></span> <span data-ttu-id="ef7c5-125">これはまもなく製品から削除されます。</span><span class="sxs-lookup"><span data-stu-id="ef7c5-125">It will soon be removed from the product.</span></span>

<span data-ttu-id="ef7c5-126">元のワークスペース パターンは推奨されておらず、使用すべきでないため、このトピックの残りの部分では、稼働中ワークスペース パターンとタブ付きワークスペース パターンに焦点を当てます。</span><span class="sxs-lookup"><span data-stu-id="ef7c5-126">The rest of this topic will focus on the Operational workspace pattern and the Tabbed Workspace pattern, as the original Workspace pattern is deprecated and should not be used.</span></span>

## <a name="wireframe"></a><span data-ttu-id="ef7c5-127">ワイヤーフレーム</span><span class="sxs-lookup"><span data-stu-id="ef7c5-127">Wireframe</span></span>

### <a name="operational-workspace"></a><span data-ttu-id="ef7c5-128">運用ワークスペース</span><span class="sxs-lookup"><span data-stu-id="ef7c5-128">Operational workspace</span></span>

<span data-ttu-id="ef7c5-129">[![運用ワークスペースのワイヤーフレーム](./media/workspace1.png)](./media/workspace1.png)</span><span class="sxs-lookup"><span data-stu-id="ef7c5-129">[![Wireframe for operational workspace](./media/workspace1.png)](./media/workspace1.png)</span></span>

### <a name="tabbed-workspace"></a><span data-ttu-id="ef7c5-130">タブ付きワークスペース</span><span class="sxs-lookup"><span data-stu-id="ef7c5-130">Tabbed workspace</span></span>

<span data-ttu-id="ef7c5-131">[![タブ付きワークスペースのワイヤーフレーム](./media/tabbedWorkspaceWireframe.png)](./media/tabbedWorkspaceWireframe.png)</span><span class="sxs-lookup"><span data-stu-id="ef7c5-131">[![Wireframe for tabbed workspace](./media/tabbedWorkspaceWireframe.png)](./media/tabbedWorkspaceWireframe.png)</span></span>

## <a name="pattern-changes-for-finance-and-operations"></a><span data-ttu-id="ef7c5-132">Finance and Operations 用のパターンの変更</span><span class="sxs-lookup"><span data-stu-id="ef7c5-132">Pattern changes for Finance and Operations</span></span>
<span data-ttu-id="ef7c5-133">Microsoft Dynamics AX 2012 ロール センターは、アクティビティに特化した複数のワークスペースで置き換えられました。</span><span class="sxs-lookup"><span data-stu-id="ef7c5-133">The Microsoft Dynamics AX 2012 Role Center has been replaced by multiple activity-focused workspaces.</span></span>

## <a name="model"></a><span data-ttu-id="ef7c5-134">モデル</span><span class="sxs-lookup"><span data-stu-id="ef7c5-134">Model</span></span>

### <a name="operational-workspace--high-level-structure"></a><span data-ttu-id="ef7c5-135">運用ワークスペース – 高度なレベル構造</span><span class="sxs-lookup"><span data-stu-id="ef7c5-135">Operational workspace – High-level structure</span></span>

- <span data-ttu-id="ef7c5-136">デザイン</span><span class="sxs-lookup"><span data-stu-id="ef7c5-136">Design</span></span>

    - <span data-ttu-id="ef7c5-137">*アクション ウィンドウ (ActionPane) \[オプション\]*</span><span class="sxs-lookup"><span data-stu-id="ef7c5-137">*Action pane (ActionPane) \[Optional\]*</span></span>
    - <span data-ttu-id="ef7c5-138">*ワークスペース ページ フィルター グループ (グループ) \[オプション\]* – これは、[ワークスペース ページ フィルター グループ](workspace-filter-group-subpattern.md)のサブパターンを使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="ef7c5-138">*Workspace page filter group (Group) \[Optional\]* – This must use the [Workspace Page Filter Group](workspace-filter-group-subpattern.md) subpattern.</span></span>
    - <span data-ttu-id="ef7c5-139">パノラマ (タブ)</span><span class="sxs-lookup"><span data-stu-id="ef7c5-139">Panorama (Tab)</span></span>

        - <span data-ttu-id="ef7c5-140">セクション概要タイル (TabPage) – これは[セクション タイル](section-tiles-subpattern.md) サブパターンを使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="ef7c5-140">Section summary tiles (TabPage) – This must use the [Section Tiles](section-tiles-subpattern.md) subpattern.</span></span>
        - <span data-ttu-id="ef7c5-141">セクション タグ付きリスト (TabPage): これは[セクション タブ付きリスト](section-tabbed-list-subpattern.md) サブパターンを使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="ef7c5-141">Section tabbed list (TabPage) – This must use the [Section Tabbed List](section-tabbed-list-subpattern.md) subpattern.</span></span>
        - <span data-ttu-id="ef7c5-142">*セクション グラフ (TabPage) \[オプション\]* – これは[セクション 積み上げグラフ](section-stacked-chart-subpattern.md)サブパターンを使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="ef7c5-142">*Section charts (TabPage) \[Optional\]* – This must use the [Section Stacked Chart](section-stacked-chart-subpattern.md) subpattern.</span></span>
        - <span data-ttu-id="ef7c5-143">*セクション PowerBI (TabPage) \[オプション\]* – これは[セクション PowerBI](section-powerbi-subpattern.md) サブパターンを使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="ef7c5-143">*Section PowerBI (TabPage) \[Optional\]* – This must use the [Section PowerBI](section-powerbi-subpattern.md) subpattern.</span></span>
        - <span data-ttu-id="ef7c5-144">セクション関連リンク (TabPage): これは[セクション関連リンク](section-related-links-subpattern.md) サブパターンを使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="ef7c5-144">Section related links (TabPage) – This must use the [Section Related Links](section-related-links-subpattern.md) subpattern.</span></span>

### <a name="tabbed-workspace--high-level-structure"></a><span data-ttu-id="ef7c5-145">タブ付きワークスペース – 高度なレベル構造</span><span class="sxs-lookup"><span data-stu-id="ef7c5-145">Tabbed workspace – High-level structure</span></span>

- <span data-ttu-id="ef7c5-146">デザイン</span><span class="sxs-lookup"><span data-stu-id="ef7c5-146">Design</span></span>

    - <span data-ttu-id="ef7c5-147">*アクション ウィンドウ (ActionPane) \[オプション\]*</span><span class="sxs-lookup"><span data-stu-id="ef7c5-147">*Action pane (ActionPane) \[Optional\]*</span></span>
    - <span data-ttu-id="ef7c5-148">*ワークスペース ページ フィルター グループ (グループ) \[オプション\]* – これは、[ワークスペース ページ フィルター グループ](workspace-filter-group-subpattern.md)のサブパターンを使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="ef7c5-148">*Workspace page filter group (Group) \[Optional\]* – This must use the [Workspace Page Filter Group](workspace-filter-group-subpattern.md) subpattern.</span></span>
    - <span data-ttu-id="ef7c5-149">StandardTab (タブ)</span><span class="sxs-lookup"><span data-stu-id="ef7c5-149">StandardTab (Tab)</span></span>

        - <span data-ttu-id="ef7c5-150">ContentTabPage (1..N)</span><span class="sxs-lookup"><span data-stu-id="ef7c5-150">ContentTabPage (1..N)</span></span> 

## <a name="core-components"></a><span data-ttu-id="ef7c5-151">コア コンポーネント</span><span class="sxs-lookup"><span data-stu-id="ef7c5-151">Core components</span></span>

-   <span data-ttu-id="ef7c5-152">**Form.Design** に適切なワークスペース パターンを適用します。</span><span class="sxs-lookup"><span data-stu-id="ef7c5-152">Apply the appropriate Workspace pattern on **Form.Design**.</span></span>
-   <span data-ttu-id="ef7c5-153">BP 警告に対処します。</span><span class="sxs-lookup"><span data-stu-id="ef7c5-153">Address BP Warnings:</span></span>
    -   <span data-ttu-id="ef7c5-154">**フォーム** は少なくとも 1 つのメニュー項目で参照される必要があります。</span><span class="sxs-lookup"><span data-stu-id="ef7c5-154">**Form** must be referenced by at least one menu item.</span></span>
    -   <span data-ttu-id="ef7c5-155">**TabPage.Caption** は空ではありません (すべてのパノラマ セクションで)。</span><span class="sxs-lookup"><span data-stu-id="ef7c5-155">**TabPage.Caption** isn't empty (for all panorama sections).</span></span>

## <a name="commonly-used-subpatterns"></a><span data-ttu-id="ef7c5-156">一般的に使用されるサブパターン</span><span class="sxs-lookup"><span data-stu-id="ef7c5-156">Commonly used subpatterns</span></span>

- [<span data-ttu-id="ef7c5-157">ワークスペース ページ フィルター グループ </span><span class="sxs-lookup"><span data-stu-id="ef7c5-157">Workspace Page Filter Group </span></span>](workspace-filter-group-subpattern.md)
- [<span data-ttu-id="ef7c5-158">セクション タイル</span><span class="sxs-lookup"><span data-stu-id="ef7c5-158">Section Tiles</span></span>](section-tiles-subpattern.md)
- [<span data-ttu-id="ef7c5-159">セクション タブ付きリスト </span><span class="sxs-lookup"><span data-stu-id="ef7c5-159">Section Tabbed List </span></span>](section-tabbed-list-subpattern.md)
- [<span data-ttu-id="ef7c5-160">セクション積み上げグラフ</span><span class="sxs-lookup"><span data-stu-id="ef7c5-160">Section Stacked Chart</span></span>](section-stacked-chart-subpattern.md)
- [<span data-ttu-id="ef7c5-161">セクション PowerBI</span><span class="sxs-lookup"><span data-stu-id="ef7c5-161">Section PowerBI</span></span>](section-powerbi-subpattern.md)
- [<span data-ttu-id="ef7c5-162">セクション関連リンク</span><span class="sxs-lookup"><span data-stu-id="ef7c5-162">Section Related Links</span></span>](section-related-links-subpattern.md)

## <a name="related-patterns"></a><span data-ttu-id="ef7c5-163">関連するパターン</span><span class="sxs-lookup"><span data-stu-id="ef7c5-163">Related patterns</span></span>

- [<span data-ttu-id="ef7c5-164">フォーム パート セクション リスト</span><span class="sxs-lookup"><span data-stu-id="ef7c5-164">Form Part Section List</span></span>](section-list-form-pattern.md)
- [<span data-ttu-id="ef7c5-165">セクション グラフ</span><span class="sxs-lookup"><span data-stu-id="ef7c5-165">Section Chart</span></span>](section-chart-form-pattern.md)

## <a name="ux-guidelines"></a><span data-ttu-id="ef7c5-166">UX ガイドライン</span><span class="sxs-lookup"><span data-stu-id="ef7c5-166">UX guidelines</span></span>
<span data-ttu-id="ef7c5-167">検証チェックリストには、フォームが UX ガイドラインに準拠しているかどうかを手動で確認する手順が示されています。</span><span class="sxs-lookup"><span data-stu-id="ef7c5-167">The verification checklist shows the steps for manually verifying that the form complies with UX guidelines.</span></span> <span data-ttu-id="ef7c5-168">このチェックリストには、開発環境を通じて自動的に実施されるガイドラインは含まれていません。</span><span class="sxs-lookup"><span data-stu-id="ef7c5-168">This checklist doesn't include any guidelines that will be enforced automatically through the development environment.</span></span> <span data-ttu-id="ef7c5-169">ブラウザーでフォームを開いて、これらの手順を確認します。</span><span class="sxs-lookup"><span data-stu-id="ef7c5-169">Open the form in the browser, and walk through these steps.</span></span>

-   <span data-ttu-id="ef7c5-170">標準フォーム ガイドライン</span><span class="sxs-lookup"><span data-stu-id="ef7c5-170">Standard form guidelines</span></span>
    -   <span data-ttu-id="ef7c5-171">標準フォーム ガイドラインは、[全般的なガイドライン](general-form-guidelines.md) ドキュメントに統合されました。</span><span class="sxs-lookup"><span data-stu-id="ef7c5-171">Standard form guidelines have been consolidated into the [General Form Guidelines](general-form-guidelines.md) document.</span></span>
-   <span data-ttu-id="ef7c5-172">ワークスペース フォームのガイドライン</span><span class="sxs-lookup"><span data-stu-id="ef7c5-172">Workspace form guidelines</span></span>
    -   <span data-ttu-id="ef7c5-173">ページ タイトルには名詞句を使用し、一般的な単語は避けてください。</span><span class="sxs-lookup"><span data-stu-id="ef7c5-173">Use a noun phase for the page title, and avoid general words.</span></span> <span data-ttu-id="ef7c5-174">ページ タイトルは、エリア ページのタイトルと重複することはできません。</span><span class="sxs-lookup"><span data-stu-id="ef7c5-174">The page title should not duplicate the title of an area page.</span></span>
    -   <span data-ttu-id="ef7c5-175">ページ タイトルは、ユーザーが考えている名詞で始まる必要があります。</span><span class="sxs-lookup"><span data-stu-id="ef7c5-175">The page title should begin with the noun that users would have in mind.</span></span>
    -   <span data-ttu-id="ef7c5-176">すべてのセクションはタイトルを持つ必要があります。</span><span class="sxs-lookup"><span data-stu-id="ef7c5-176">All sections must have a title.</span></span>
    -   <span data-ttu-id="ef7c5-177">セクションは、通常 2 から 4 つの標準タイルの幅の範囲です。</span><span class="sxs-lookup"><span data-stu-id="ef7c5-177">A section typically spans the width of two to four standard tiles.</span></span>
    -   <span data-ttu-id="ef7c5-178">FormPartControl を使用してコンテンツを表示するセクションは、FormPartControl で **HeightMode** を **SizeToAvailable** に設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="ef7c5-178">Any section that uses a FormPartControl to display content should have **HeightMode** set to **SizeToAvailable** on the FormPartControl.</span></span>
-   <span data-ttu-id="ef7c5-179">操作</span><span class="sxs-lookup"><span data-stu-id="ef7c5-179">Actions</span></span>
    -   <span data-ttu-id="ef7c5-180">使用頻度の高いコマンドのみを含めます。</span><span class="sxs-lookup"><span data-stu-id="ef7c5-180">Include only frequently used commands.</span></span>
    -   <span data-ttu-id="ef7c5-181">アクション ウィンドウのアクションは、ワークスペース全体に関連付ける必要があります (ワークスペースの特定のセクションではありません)。</span><span class="sxs-lookup"><span data-stu-id="ef7c5-181">Actions on the Action Pane should be related to the whole workspace (not a specific section of it).</span></span>
        -   <span data-ttu-id="ef7c5-182">**例外:** 非常に頻繁に使用されている場合、**概要** セクションには、単一の「新規」アクションをタイルとして配置することができます。</span><span class="sxs-lookup"><span data-stu-id="ef7c5-182">**Exception:** A single "New" action can be put as a tile in the **Summary** section if it's very frequently used.</span></span>
    -   <span data-ttu-id="ef7c5-183">ドロップダウン メニューで、同じコマンドの変動をグループ化します。</span><span class="sxs-lookup"><span data-stu-id="ef7c5-183">Group variations of the same command on drop-down menus.</span></span>
        -   <span data-ttu-id="ef7c5-184">**例:** 新しい販売見積、新しい販売注文、新しい返品注文</span><span class="sxs-lookup"><span data-stu-id="ef7c5-184">**Examples:** New sales quote, New sales order, New return order</span></span>
-   <span data-ttu-id="ef7c5-185">フィルター</span><span class="sxs-lookup"><span data-stu-id="ef7c5-185">Filters</span></span>
    -   <span data-ttu-id="ef7c5-186">ワークスペース上に、0 ~ 5 つのフィルター フィールドが許されます。</span><span class="sxs-lookup"><span data-stu-id="ef7c5-186">Zero to five filter fields are allowed on a workspace.</span></span>
        -   <span data-ttu-id="ef7c5-187">単一フィールドのみ、そのページのタイトルの下に追加することができます。</span><span class="sxs-lookup"><span data-stu-id="ef7c5-187">Only a single field can be put under the page title</span></span>
        -   <span data-ttu-id="ef7c5-188">残りのフィルターは、ワークスペースの構成ダイアログにある必要があります。</span><span class="sxs-lookup"><span data-stu-id="ef7c5-188">The remaining filters must be in a workspace configuration dialog.</span></span>

## <a name="example"></a><span data-ttu-id="ef7c5-189">例</span><span class="sxs-lookup"><span data-stu-id="ef7c5-189">Example</span></span>

### <a name="operational-workspace"></a><span data-ttu-id="ef7c5-190">運用ワークスペース</span><span class="sxs-lookup"><span data-stu-id="ef7c5-190">Operational workspace</span></span>

<span data-ttu-id="ef7c5-191">フォーム: **FMClerkWorkspace**</span><span class="sxs-lookup"><span data-stu-id="ef7c5-191">Form: **FMClerkWorkspace**</span></span> 

<span data-ttu-id="ef7c5-192">[![運用ワークスペースの例](./media/workspace3.png)](./media/workspace3.png)</span><span class="sxs-lookup"><span data-stu-id="ef7c5-192">[![Operational workspace example](./media/workspace3.png)](./media/workspace3.png)</span></span>

## <a name="frequently-asked-questions"></a><span data-ttu-id="ef7c5-193">よく寄せられる質問</span><span class="sxs-lookup"><span data-stu-id="ef7c5-193">Frequently asked questions</span></span>

<span data-ttu-id="ef7c5-194">このセクションには、このガイドライン/パターンに関連するよくある質問への回答があります。</span><span class="sxs-lookup"><span data-stu-id="ef7c5-194">This section will have answers to frequently asked questions that are related to this guideline/pattern.</span></span>

## <a name="open-issues"></a><span data-ttu-id="ef7c5-195">未処理の問題</span><span class="sxs-lookup"><span data-stu-id="ef7c5-195">Open issues</span></span>

-   <span data-ttu-id="ef7c5-196">なし</span><span class="sxs-lookup"><span data-stu-id="ef7c5-196">None</span></span>

## <a name="ax-2012-content"></a><span data-ttu-id="ef7c5-197">AX 2012 コンテンツ</span><span class="sxs-lookup"><span data-stu-id="ef7c5-197">AX 2012 content</span></span>

### <a name="ax-2012-links"></a><span data-ttu-id="ef7c5-198">AX 2012 リンク</span><span class="sxs-lookup"><span data-stu-id="ef7c5-198">AX 2012 links</span></span>

-   <span data-ttu-id="ef7c5-199">[MSDN ロール センター ページ参照 \[AX 2012\]](https://msdn.microsoft.com/library/cc558235.aspx)</span><span class="sxs-lookup"><span data-stu-id="ef7c5-199">[MSDN Role Center Page Reference \[AX 2012\]](https://msdn.microsoft.com/library/cc558235.aspx)</span></span>
-   <span data-ttu-id="ef7c5-200">[MSDN ロール センター ユーザー エクスペリエンス ガイドライン \[AX 2012\]](https://msdn.microsoft.com/library/gg886608.aspx)</span><span class="sxs-lookup"><span data-stu-id="ef7c5-200">[MSDN Role Center User Experience Guidelines \[AX 2012\]](https://msdn.microsoft.com/library/gg886608.aspx)</span></span>

### <a name="ax-2012-example"></a><span data-ttu-id="ef7c5-201">AX 2012 の例</span><span class="sxs-lookup"><span data-stu-id="ef7c5-201">AX 2012 example</span></span>

<span data-ttu-id="ef7c5-202">[![前のバージョンのワークスペースの例](./media/workspace5.png)](./media/workspace5.png)</span><span class="sxs-lookup"><span data-stu-id="ef7c5-202">[![Previous version workspace example](./media/workspace5.png)](./media/workspace5.png)</span></span>
