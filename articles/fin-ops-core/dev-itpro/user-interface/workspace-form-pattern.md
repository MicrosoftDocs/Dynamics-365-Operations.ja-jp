---
title: ワークスペースのフォーム パターン
description: このトピックでは、ワークスペース フォーム パターンについて説明します。 ワークスペースはユーザーがタスクと特定のページに移動する主な方法です。
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
ms.openlocfilehash: 2db675bde4bc376a1dc2c2716bb1c153d8594308
ms.sourcegitcommit: 5192cfaedfd861faea63d8954d7bcc500608a225
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/30/2021
ms.locfileid: "5093710"
---
# <a name="workspace-form-pattern"></a><span data-ttu-id="3d077-104">ワークスペースのフォーム パターン</span><span class="sxs-lookup"><span data-stu-id="3d077-104">Workspace form pattern</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="3d077-105">このトピックでは、ワークスペース フォーム パターンについて説明します。</span><span class="sxs-lookup"><span data-stu-id="3d077-105">This topic discusses workspace form patterns.</span></span> <span data-ttu-id="3d077-106">ワークスペースはユーザーがタスクと特定のページに移動する主な方法です。</span><span class="sxs-lookup"><span data-stu-id="3d077-106">Workspaces are the primary way that users navigate to tasks and specific pages.</span></span> <span data-ttu-id="3d077-107">ワークスペースは、サポートされている重要な事業活動ごとに作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="3d077-107">A workspace should be created for every significant business activity that is supported.</span></span>  

## <a name="usage"></a><span data-ttu-id="3d077-108">用途</span><span class="sxs-lookup"><span data-stu-id="3d077-108">Usage</span></span>

<span data-ttu-id="3d077-109">ワークスペースは新しい概念で、ユーザーがタスクと特定のページに移動する主な方法となることを意図しています。</span><span class="sxs-lookup"><span data-stu-id="3d077-109">Workspaces are a new concept, and are meant to be the primary way that users navigate to tasks and specific pages.</span></span> <span data-ttu-id="3d077-110">ワークスペースは、サポートする重要な事業「活動」ごとに作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="3d077-110">A workspace should be created for every significant business “activity” that you want to support.</span></span> <span data-ttu-id="3d077-111">「アクティビティ」はタスクよりも細かく従来の「エリア ページ」よりさらに細分化されています。</span><span class="sxs-lookup"><span data-stu-id="3d077-111">An “activity” is less granular than a task and more granular than a legacy “area page.”</span></span> <span data-ttu-id="3d077-112">ワークスペースは、1 ページの活動の概要を提供したり、ユーザーが現在の状態、今後の作業負荷、プロセスまたはユーザーのパフォーマンスを理解するよう助けるためのものです。</span><span class="sxs-lookup"><span data-stu-id="3d077-112">A workspace is intended to provide a one-page overview of the activity, and to help users understand the current status, the upcoming workload, and the performance of the process or user.</span></span> <span data-ttu-id="3d077-113">ユーザーは、その活動の最も一般的なタスクを、ワークスペースから直接開始できるようにする必要があります。</span><span class="sxs-lookup"><span data-stu-id="3d077-113">Users should be able to start the most typical tasks for the activity directly from the workspace.</span></span> <span data-ttu-id="3d077-114">可能であれば、ユーザーは、受信した概要に基づいて直接ワークスペースで、タスクを完了する必要があります。</span><span class="sxs-lookup"><span data-stu-id="3d077-114">If possible, users should also be able to complete tasks directly in the workspace, based on the overview that they just received.</span></span> <span data-ttu-id="3d077-115">現在、2 つのワークスペース パターンがあります。</span><span class="sxs-lookup"><span data-stu-id="3d077-115">Currently, there are two workspace patterns:</span></span>

-   <span data-ttu-id="3d077-116">**タブ付きワークスペース**: コンテンツに水平スクロール パノラマを強制せずに、このパターンは標準タブを使用して垂直スクロール ワークスペースの開発を許可します。</span><span class="sxs-lookup"><span data-stu-id="3d077-116">**Tabbed workspace**: Instead of forcing a horizontally-scrolling panorama for content, this pattern uses standard tabs to allow the development of vertically-scrolling workspaces.</span></span> <span data-ttu-id="3d077-117">これは、特に Power BI レポートをワークスペースに埋め込むために使用されています。</span><span class="sxs-lookup"><span data-stu-id="3d077-117">This is particularly being used to embed Power BI reports into workspaces.</span></span> <span data-ttu-id="3d077-118">これらのタブ内のコンテンツを定義するのに役立つ追加のサブパターンは、将来提供される可能性が高くなります。</span><span class="sxs-lookup"><span data-stu-id="3d077-118">Additional subpatterns to help define content inside these tabs will likely be provided in the future.</span></span>
-   <span data-ttu-id="3d077-119">**運用ワークスペース**: これは、ワークスペースの開発のために使用されている標準パターンです。</span><span class="sxs-lookup"><span data-stu-id="3d077-119">**Operational workspace**: This is the standard pattern currently used for workspace development.</span></span> <span data-ttu-id="3d077-120">許可されている一連のコンポーネントのため、このパターンは非推奨の「ワークスペース」パターンよりも優れたパフォーマンスがあります。</span><span class="sxs-lookup"><span data-stu-id="3d077-120">Because of the set of components that are permitted in it, this pattern has superior performance over the deprecated "workspace" pattern.</span></span> <span data-ttu-id="3d077-121">この理由および、システム内の他のワークスペースで視覚と行動の一貫性を確実にするため、このパターンを使用することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="3d077-121">For this reason and to ensure visual and behavioral consistency with the other workspaces in the system, we recommend that you use this pattern.</span></span>
-   <span data-ttu-id="3d077-122">(非推奨) **ワークスペース**: このパターンは、間違いがないように、念のため記載されています。</span><span class="sxs-lookup"><span data-stu-id="3d077-122">(Deprecated) **Workspace**: This pattern is only mentioned for the sake of completeness.</span></span> <span data-ttu-id="3d077-123">パターンを **使用しない** でください。</span><span class="sxs-lookup"><span data-stu-id="3d077-123">Do **not** use this pattern.</span></span> <span data-ttu-id="3d077-124">これはまもなく製品から削除されます。</span><span class="sxs-lookup"><span data-stu-id="3d077-124">It will soon be removed from the product.</span></span>

<span data-ttu-id="3d077-125">元のワークスペース パターンは推奨されておらず、使用すべきでないため、このトピックの残りの部分では、稼働中ワークスペース パターンとタブ付きワークスペース パターンに焦点を当てます。</span><span class="sxs-lookup"><span data-stu-id="3d077-125">The rest of this topic will focus on the Operational workspace pattern and the Tabbed Workspace pattern, as the original Workspace pattern is deprecated and should not be used.</span></span>

## <a name="wireframe"></a><span data-ttu-id="3d077-126">ワイヤーフレーム</span><span class="sxs-lookup"><span data-stu-id="3d077-126">Wireframe</span></span>

### <a name="operational-workspace"></a><span data-ttu-id="3d077-127">運用ワークスペース</span><span class="sxs-lookup"><span data-stu-id="3d077-127">Operational workspace</span></span>

<span data-ttu-id="3d077-128">[![運用ワークスペースのワイヤーフレーム](./media/workspace1.png)](./media/workspace1.png)</span><span class="sxs-lookup"><span data-stu-id="3d077-128">[![Wireframe for operational workspace](./media/workspace1.png)](./media/workspace1.png)</span></span>

### <a name="tabbed-workspace"></a><span data-ttu-id="3d077-129">タブ付きワークスペース</span><span class="sxs-lookup"><span data-stu-id="3d077-129">Tabbed workspace</span></span>

<span data-ttu-id="3d077-130">[![タブ付きワークスペースのワイヤーフレーム](./media/tabbedWorkspaceWireframe.png)](./media/tabbedWorkspaceWireframe.png)</span><span class="sxs-lookup"><span data-stu-id="3d077-130">[![Wireframe for tabbed workspace](./media/tabbedWorkspaceWireframe.png)](./media/tabbedWorkspaceWireframe.png)</span></span>

## <a name="pattern-changes-for-finance-and-operations"></a><span data-ttu-id="3d077-131">Finance and Operations 用のパターンの変更</span><span class="sxs-lookup"><span data-stu-id="3d077-131">Pattern changes for Finance and Operations</span></span>
<span data-ttu-id="3d077-132">Microsoft Dynamics AX 2012 ロール センターは、アクティビティに特化した複数のワークスペースで置き換えられました。</span><span class="sxs-lookup"><span data-stu-id="3d077-132">The Microsoft Dynamics AX 2012 Role Center has been replaced by multiple activity-focused workspaces.</span></span>

## <a name="model"></a><span data-ttu-id="3d077-133">モデル</span><span class="sxs-lookup"><span data-stu-id="3d077-133">Model</span></span>

### <a name="operational-workspace--high-level-structure"></a><span data-ttu-id="3d077-134">運用ワークスペース – 高度なレベル構造</span><span class="sxs-lookup"><span data-stu-id="3d077-134">Operational workspace – High-level structure</span></span>

- <span data-ttu-id="3d077-135">デザイン</span><span class="sxs-lookup"><span data-stu-id="3d077-135">Design</span></span>

    - <span data-ttu-id="3d077-136">*アクション ウィンドウ (ActionPane) \[オプション\]*</span><span class="sxs-lookup"><span data-stu-id="3d077-136">*Action pane (ActionPane) \[Optional\]*</span></span>
    - <span data-ttu-id="3d077-137">*ワークスペース ページ フィルター グループ (グループ) \[オプション\]* – これは、[ワークスペース ページ フィルター グループ](workspace-filter-group-subpattern.md)のサブパターンを使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="3d077-137">*Workspace page filter group (Group) \[Optional\]* – This must use the [Workspace Page Filter Group](workspace-filter-group-subpattern.md) subpattern.</span></span>
    - <span data-ttu-id="3d077-138">パノラマ (タブ)</span><span class="sxs-lookup"><span data-stu-id="3d077-138">Panorama (Tab)</span></span>

        - <span data-ttu-id="3d077-139">セクション概要タイル (TabPage) – これは[セクション タイル](section-tiles-subpattern.md) サブパターンを使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="3d077-139">Section summary tiles (TabPage) – This must use the [Section Tiles](section-tiles-subpattern.md) subpattern.</span></span>
        - <span data-ttu-id="3d077-140">セクション タグ付きリスト (TabPage): これは[セクション タブ付きリスト](section-tabbed-list-subpattern.md) サブパターンを使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="3d077-140">Section tabbed list (TabPage) – This must use the [Section Tabbed List](section-tabbed-list-subpattern.md) subpattern.</span></span>
        - <span data-ttu-id="3d077-141">*セクション グラフ (TabPage) \[オプション\]* – これは[セクション 積み上げグラフ](section-stacked-chart-subpattern.md)サブパターンを使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="3d077-141">*Section charts (TabPage) \[Optional\]* – This must use the [Section Stacked Chart](section-stacked-chart-subpattern.md) subpattern.</span></span>
        - <span data-ttu-id="3d077-142">*セクション PowerBI (TabPage) \[オプション\]* – これは[セクション PowerBI](section-powerbi-subpattern.md) サブパターンを使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="3d077-142">*Section PowerBI (TabPage) \[Optional\]* – This must use the [Section PowerBI](section-powerbi-subpattern.md) subpattern.</span></span>
        - <span data-ttu-id="3d077-143">セクション関連リンク (TabPage): これは[セクション関連リンク](section-related-links-subpattern.md) サブパターンを使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="3d077-143">Section related links (TabPage) – This must use the [Section Related Links](section-related-links-subpattern.md) subpattern.</span></span>

### <a name="tabbed-workspace--high-level-structure"></a><span data-ttu-id="3d077-144">タブ付きワークスペース – 高度なレベル構造</span><span class="sxs-lookup"><span data-stu-id="3d077-144">Tabbed workspace – High-level structure</span></span>

- <span data-ttu-id="3d077-145">デザイン</span><span class="sxs-lookup"><span data-stu-id="3d077-145">Design</span></span>

    - <span data-ttu-id="3d077-146">*アクション ウィンドウ (ActionPane) \[オプション\]*</span><span class="sxs-lookup"><span data-stu-id="3d077-146">*Action pane (ActionPane) \[Optional\]*</span></span>
    - <span data-ttu-id="3d077-147">*ワークスペース ページ フィルター グループ (グループ) \[オプション\]* – これは、[ワークスペース ページ フィルター グループ](workspace-filter-group-subpattern.md)のサブパターンを使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="3d077-147">*Workspace page filter group (Group) \[Optional\]* – This must use the [Workspace Page Filter Group](workspace-filter-group-subpattern.md) subpattern.</span></span>
    - <span data-ttu-id="3d077-148">StandardTab (タブ)</span><span class="sxs-lookup"><span data-stu-id="3d077-148">StandardTab (Tab)</span></span>

        - <span data-ttu-id="3d077-149">ContentTabPage (1..N)</span><span class="sxs-lookup"><span data-stu-id="3d077-149">ContentTabPage (1..N)</span></span> 

## <a name="core-components"></a><span data-ttu-id="3d077-150">コア コンポーネント</span><span class="sxs-lookup"><span data-stu-id="3d077-150">Core components</span></span>

-   <span data-ttu-id="3d077-151">**Form.Design** に適切なワークスペース パターンを適用します。</span><span class="sxs-lookup"><span data-stu-id="3d077-151">Apply the appropriate Workspace pattern on **Form.Design**.</span></span>
-   <span data-ttu-id="3d077-152">BP 警告に対処します。</span><span class="sxs-lookup"><span data-stu-id="3d077-152">Address BP Warnings:</span></span>
    -   <span data-ttu-id="3d077-153">**フォーム** は少なくとも 1 つのメニュー項目で参照される必要があります。</span><span class="sxs-lookup"><span data-stu-id="3d077-153">**Form** must be referenced by at least one menu item.</span></span>
    -   <span data-ttu-id="3d077-154">**TabPage.Caption** は空ではありません (すべてのパノラマ セクションで)。</span><span class="sxs-lookup"><span data-stu-id="3d077-154">**TabPage.Caption** isn't empty (for all panorama sections).</span></span>

## <a name="commonly-used-subpatterns"></a><span data-ttu-id="3d077-155">一般的に使用されるサブパターン</span><span class="sxs-lookup"><span data-stu-id="3d077-155">Commonly used subpatterns</span></span>

- [<span data-ttu-id="3d077-156">ワークスペース ページ フィルター グループ </span><span class="sxs-lookup"><span data-stu-id="3d077-156">Workspace Page Filter Group </span></span>](workspace-filter-group-subpattern.md)
- [<span data-ttu-id="3d077-157">セクション タイル</span><span class="sxs-lookup"><span data-stu-id="3d077-157">Section Tiles</span></span>](section-tiles-subpattern.md)
- [<span data-ttu-id="3d077-158">セクション タブ付きリスト </span><span class="sxs-lookup"><span data-stu-id="3d077-158">Section Tabbed List </span></span>](section-tabbed-list-subpattern.md)
- [<span data-ttu-id="3d077-159">セクション積み上げグラフ</span><span class="sxs-lookup"><span data-stu-id="3d077-159">Section Stacked Chart</span></span>](section-stacked-chart-subpattern.md)
- [<span data-ttu-id="3d077-160">セクション PowerBI</span><span class="sxs-lookup"><span data-stu-id="3d077-160">Section PowerBI</span></span>](section-powerbi-subpattern.md)
- [<span data-ttu-id="3d077-161">セクション関連リンク</span><span class="sxs-lookup"><span data-stu-id="3d077-161">Section Related Links</span></span>](section-related-links-subpattern.md)

## <a name="related-patterns"></a><span data-ttu-id="3d077-162">関連するパターン</span><span class="sxs-lookup"><span data-stu-id="3d077-162">Related patterns</span></span>

- [<span data-ttu-id="3d077-163">フォーム パート セクション リスト</span><span class="sxs-lookup"><span data-stu-id="3d077-163">Form Part Section List</span></span>](section-list-form-pattern.md)
- [<span data-ttu-id="3d077-164">セクション グラフ</span><span class="sxs-lookup"><span data-stu-id="3d077-164">Section Chart</span></span>](section-chart-form-pattern.md)

## <a name="ux-guidelines"></a><span data-ttu-id="3d077-165">UX ガイドライン</span><span class="sxs-lookup"><span data-stu-id="3d077-165">UX guidelines</span></span>
<span data-ttu-id="3d077-166">検証チェックリストには、フォームが UX ガイドラインに準拠しているかどうかを手動で確認する手順が示されています。</span><span class="sxs-lookup"><span data-stu-id="3d077-166">The verification checklist shows the steps for manually verifying that the form complies with UX guidelines.</span></span> <span data-ttu-id="3d077-167">このチェックリストには、開発環境を通じて自動的に実施されるガイドラインは含まれていません。</span><span class="sxs-lookup"><span data-stu-id="3d077-167">This checklist doesn't include any guidelines that will be enforced automatically through the development environment.</span></span> <span data-ttu-id="3d077-168">ブラウザーでフォームを開いて、これらの手順を確認します。</span><span class="sxs-lookup"><span data-stu-id="3d077-168">Open the form in the browser, and walk through these steps.</span></span>

-   <span data-ttu-id="3d077-169">標準フォーム ガイドライン</span><span class="sxs-lookup"><span data-stu-id="3d077-169">Standard form guidelines</span></span>
    -   <span data-ttu-id="3d077-170">標準フォーム ガイドラインは、[全般的なガイドライン](general-form-guidelines.md) ドキュメントに統合されました。</span><span class="sxs-lookup"><span data-stu-id="3d077-170">Standard form guidelines have been consolidated into the [General Form Guidelines](general-form-guidelines.md) document.</span></span>
-   <span data-ttu-id="3d077-171">ワークスペース フォームのガイドライン</span><span class="sxs-lookup"><span data-stu-id="3d077-171">Workspace form guidelines</span></span>
    -   <span data-ttu-id="3d077-172">ページ タイトルには名詞句を使用し、一般的な単語は避けてください。</span><span class="sxs-lookup"><span data-stu-id="3d077-172">Use a noun phase for the page title, and avoid general words.</span></span> <span data-ttu-id="3d077-173">ページ タイトルは、エリア ページのタイトルと重複することはできません。</span><span class="sxs-lookup"><span data-stu-id="3d077-173">The page title should not duplicate the title of an area page.</span></span>
    -   <span data-ttu-id="3d077-174">ページ タイトルは、ユーザーが考えている名詞で始まる必要があります。</span><span class="sxs-lookup"><span data-stu-id="3d077-174">The page title should begin with the noun that users would have in mind.</span></span>
    -   <span data-ttu-id="3d077-175">すべてのセクションはタイトルを持つ必要があります。</span><span class="sxs-lookup"><span data-stu-id="3d077-175">All sections must have a title.</span></span>
    -   <span data-ttu-id="3d077-176">セクションは、通常 2 から 4 つの標準タイルの幅の範囲です。</span><span class="sxs-lookup"><span data-stu-id="3d077-176">A section typically spans the width of two to four standard tiles.</span></span>
    -   <span data-ttu-id="3d077-177">FormPartControl を使用してコンテンツを表示するセクションは、FormPartControl で **HeightMode** を **SizeToAvailable** に設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="3d077-177">Any section that uses a FormPartControl to display content should have **HeightMode** set to **SizeToAvailable** on the FormPartControl.</span></span>
-   <span data-ttu-id="3d077-178">操作</span><span class="sxs-lookup"><span data-stu-id="3d077-178">Actions</span></span>
    -   <span data-ttu-id="3d077-179">使用頻度の高いコマンドのみを含めます。</span><span class="sxs-lookup"><span data-stu-id="3d077-179">Include only frequently used commands.</span></span>
    -   <span data-ttu-id="3d077-180">アクション ウィンドウのアクションは、ワークスペース全体に関連付ける必要があります (ワークスペースの特定のセクションではありません)。</span><span class="sxs-lookup"><span data-stu-id="3d077-180">Actions on the Action Pane should be related to the whole workspace (not a specific section of it).</span></span>
        -   <span data-ttu-id="3d077-181">**例外:** 非常に頻繁に使用されている場合、**概要** セクションには、単一の「新規」アクションをタイルとして配置することができます。</span><span class="sxs-lookup"><span data-stu-id="3d077-181">**Exception:** A single "New" action can be put as a tile in the **Summary** section if it's very frequently used.</span></span>
    -   <span data-ttu-id="3d077-182">ドロップダウン メニューで、同じコマンドの変動をグループ化します。</span><span class="sxs-lookup"><span data-stu-id="3d077-182">Group variations of the same command on drop-down menus.</span></span>
        -   <span data-ttu-id="3d077-183">**例:** 新しい販売見積、新しい販売注文、新しい返品注文</span><span class="sxs-lookup"><span data-stu-id="3d077-183">**Examples:** New sales quote, New sales order, New return order</span></span>
-   <span data-ttu-id="3d077-184">フィルター</span><span class="sxs-lookup"><span data-stu-id="3d077-184">Filters</span></span>
    -   <span data-ttu-id="3d077-185">ワークスペース上に、0 ~ 5 つのフィルター フィールドが許されます。</span><span class="sxs-lookup"><span data-stu-id="3d077-185">Zero to five filter fields are allowed on a workspace.</span></span>
        -   <span data-ttu-id="3d077-186">単一フィールドのみ、そのページのタイトルの下に追加することができます。</span><span class="sxs-lookup"><span data-stu-id="3d077-186">Only a single field can be put under the page title</span></span>
        -   <span data-ttu-id="3d077-187">残りのフィルターは、ワークスペースの構成ダイアログにある必要があります。</span><span class="sxs-lookup"><span data-stu-id="3d077-187">The remaining filters must be in a workspace configuration dialog.</span></span>

## <a name="example"></a><span data-ttu-id="3d077-188">例</span><span class="sxs-lookup"><span data-stu-id="3d077-188">Example</span></span>

### <a name="operational-workspace"></a><span data-ttu-id="3d077-189">運用ワークスペース</span><span class="sxs-lookup"><span data-stu-id="3d077-189">Operational workspace</span></span>

<span data-ttu-id="3d077-190">フォーム: **FMClerkWorkspace**</span><span class="sxs-lookup"><span data-stu-id="3d077-190">Form: **FMClerkWorkspace**</span></span> 

<span data-ttu-id="3d077-191">[![運用ワークスペースの例](./media/workspace3.png)](./media/workspace3.png)</span><span class="sxs-lookup"><span data-stu-id="3d077-191">[![Operational workspace example](./media/workspace3.png)](./media/workspace3.png)</span></span>

## <a name="frequently-asked-questions"></a><span data-ttu-id="3d077-192">よく寄せられる質問</span><span class="sxs-lookup"><span data-stu-id="3d077-192">Frequently asked questions</span></span>

<span data-ttu-id="3d077-193">このセクションには、このガイドライン/パターンに関連するよくある質問への回答があります。</span><span class="sxs-lookup"><span data-stu-id="3d077-193">This section will have answers to frequently asked questions that are related to this guideline/pattern.</span></span>

## <a name="open-issues"></a><span data-ttu-id="3d077-194">未処理の問題</span><span class="sxs-lookup"><span data-stu-id="3d077-194">Open issues</span></span>

-   <span data-ttu-id="3d077-195">なし</span><span class="sxs-lookup"><span data-stu-id="3d077-195">None</span></span>

## <a name="ax-2012-content"></a><span data-ttu-id="3d077-196">AX 2012 コンテンツ</span><span class="sxs-lookup"><span data-stu-id="3d077-196">AX 2012 content</span></span>

### <a name="ax-2012-links"></a><span data-ttu-id="3d077-197">AX 2012 リンク</span><span class="sxs-lookup"><span data-stu-id="3d077-197">AX 2012 links</span></span>

-   <span data-ttu-id="3d077-198">[MSDN ロール センター ページ参照 \[AX 2012\]](https://msdn.microsoft.com/library/cc558235.aspx)</span><span class="sxs-lookup"><span data-stu-id="3d077-198">[MSDN Role Center Page Reference \[AX 2012\]](https://msdn.microsoft.com/library/cc558235.aspx)</span></span>
-   <span data-ttu-id="3d077-199">[MSDN ロール センター ユーザー エクスペリエンス ガイドライン \[AX 2012\]](https://msdn.microsoft.com/library/gg886608.aspx)</span><span class="sxs-lookup"><span data-stu-id="3d077-199">[MSDN Role Center User Experience Guidelines \[AX 2012\]](https://msdn.microsoft.com/library/gg886608.aspx)</span></span>

### <a name="ax-2012-example"></a><span data-ttu-id="3d077-200">AX 2012 の例</span><span class="sxs-lookup"><span data-stu-id="3d077-200">AX 2012 example</span></span>

<span data-ttu-id="3d077-201">[![前のバージョンのワークスペースの例](./media/workspace5.png)](./media/workspace5.png)</span><span class="sxs-lookup"><span data-stu-id="3d077-201">[![Previous version workspace example](./media/workspace5.png)](./media/workspace5.png)</span></span>
