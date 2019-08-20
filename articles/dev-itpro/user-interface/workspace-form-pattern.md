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
ms.reviewer: sericks
ms.search.scope: Operations
ms.custom: 29151
ms.assetid: 4ca77c08-1c8f-4b0c-af55-ca89a7e8982b
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 90f1a9efbb71738b86fc77427681c3c798e4827d
ms.sourcegitcommit: 16bfa0fd08feec1647829630401ce62ce2ffa1a4
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/02/2019
ms.locfileid: "1851037"
---
# <a name="workspace-form-pattern"></a><span data-ttu-id="8f26e-105">ワークスペースのフォーム パターン</span><span class="sxs-lookup"><span data-stu-id="8f26e-105">Workspace form pattern</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="8f26e-106">このトピックでは、ワークスペース フォーム パターンについて説明します。</span><span class="sxs-lookup"><span data-stu-id="8f26e-106">This topic discusses workspace form patterns.</span></span> <span data-ttu-id="8f26e-107">ワークスペースはユーザーがタスクと特定のページに移動する主な方法です。</span><span class="sxs-lookup"><span data-stu-id="8f26e-107">Workspaces are the primary way that users navigate to tasks and specific pages.</span></span> <span data-ttu-id="8f26e-108">ワークスペースは、サポートされている重要な事業活動ごとに作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="8f26e-108">A workspace should be created for every significant business activity that is supported.</span></span>  

## <a name="usage"></a><span data-ttu-id="8f26e-109">用途</span><span class="sxs-lookup"><span data-stu-id="8f26e-109">Usage</span></span>

<span data-ttu-id="8f26e-110">ワークスペースは新しい概念で、ユーザーがタスクと特定のページに移動する主な方法となることを意図しています。</span><span class="sxs-lookup"><span data-stu-id="8f26e-110">Workspaces are a new concept, and are meant to be the primary way that users navigate to tasks and specific pages.</span></span> <span data-ttu-id="8f26e-111">ワークスペースは、サポートする重要な事業「活動」ごとに作成する必要があります。</span><span class="sxs-lookup"><span data-stu-id="8f26e-111">A workspace should be created for every significant business “activity” that you want to support.</span></span> <span data-ttu-id="8f26e-112">「アクティビティ」はタスクよりも細かく従来の「エリア ページ」よりさらに細分化されています。</span><span class="sxs-lookup"><span data-stu-id="8f26e-112">An “activity” is less granular than a task and more granular than a legacy “area page.”</span></span> <span data-ttu-id="8f26e-113">ワークスペースは、1 ページの活動の概要を提供したり、ユーザーが現在の状態、今後の作業負荷、プロセスまたはユーザーのパフォーマンスを理解するよう助けるためのものです。</span><span class="sxs-lookup"><span data-stu-id="8f26e-113">A workspace is intended to provide a one-page overview of the activity, and to help users understand the current status, the upcoming workload, and the performance of the process or user.</span></span> <span data-ttu-id="8f26e-114">ユーザーは、その活動の最も一般的なタスクを、ワークスペースから直接開始できるようにする必要があります。</span><span class="sxs-lookup"><span data-stu-id="8f26e-114">Users should be able to start the most typical tasks for the activity directly from the workspace.</span></span> <span data-ttu-id="8f26e-115">可能であれば、ユーザーは、受信した概要に基づいて直接ワークスペースで、タスクを完了する必要があります。</span><span class="sxs-lookup"><span data-stu-id="8f26e-115">If possible, users should also be able to complete tasks directly in the workspace, based on the overview that they just received.</span></span> <span data-ttu-id="8f26e-116">現在、2 つのワークスペース パターンがあります。</span><span class="sxs-lookup"><span data-stu-id="8f26e-116">Currently, there are two workspace patterns:</span></span>

-   <span data-ttu-id="8f26e-117">**タブ付きワークスペース**: これは、Platform Update 7 で使用可能な新しいワークスペース パターンです。</span><span class="sxs-lookup"><span data-stu-id="8f26e-117">**Tabbed workspace**: This is a new workspace pattern that is being made available in Platform Update 7.</span></span> <span data-ttu-id="8f26e-118">コンテンツに水平スクロール パノラマを強制せずに、このパターンは標準タブを使用して垂直スクロール ワークスペースの開発を許可します。</span><span class="sxs-lookup"><span data-stu-id="8f26e-118">Instead of forcing a horizontally-scrolling panorama for content, this pattern uses standard tabs to allow the development of vertically-scrolling workspaces.</span></span> <span data-ttu-id="8f26e-119">これは、特に Power BI レポートをワークスペースに埋め込むために使用されています。</span><span class="sxs-lookup"><span data-stu-id="8f26e-119">This is particularly being used to embed Power BI reports into workspaces.</span></span> <span data-ttu-id="8f26e-120">これらのタブ内のコンテンツを定義するのに役立つ追加のサブパターンは、将来提供される可能性が高くなります。</span><span class="sxs-lookup"><span data-stu-id="8f26e-120">Additional subpatterns to help define content inside these tabs will likely be provided in the future.</span></span>
-   <span data-ttu-id="8f26e-121">**運用ワークスペース**: これは、ワークスペースの開発のために使用されている標準パターンです。</span><span class="sxs-lookup"><span data-stu-id="8f26e-121">**Operational workspace**: This is the standard pattern currently used for workspace development.</span></span> <span data-ttu-id="8f26e-122">許可されている一連のコンポーネントのため、このパターンは非推奨の「ワークスペース」パターンよりも優れたパフォーマンスがあります。</span><span class="sxs-lookup"><span data-stu-id="8f26e-122">Because of the set of components that are permitted in it, this pattern has superior performance over the deprecated "workspace" pattern.</span></span> <span data-ttu-id="8f26e-123">この理由および、システム内の他のワークスペースで視覚と行動の一貫性を確実にするため、このパターンを使用することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="8f26e-123">For this reason and to ensure visual and behavioral consistency with the other workspaces in the system, we recommend that you use this pattern.</span></span>
-   <span data-ttu-id="8f26e-124">(非推奨) **ワークスペース**: このパターンは、間違いがないように、念のため記載されています。</span><span class="sxs-lookup"><span data-stu-id="8f26e-124">(Deprecated) **Workspace**: This pattern is only mentioned for the sake of completeness.</span></span> <span data-ttu-id="8f26e-125">パターンを**使用しない**でください。</span><span class="sxs-lookup"><span data-stu-id="8f26e-125">Do **not** use this pattern.</span></span> <span data-ttu-id="8f26e-126">これはまもなく製品から削除されます。</span><span class="sxs-lookup"><span data-stu-id="8f26e-126">It will soon be removed from the product.</span></span>

<span data-ttu-id="8f26e-127">元のワークスペース パターンは推奨されておらず、使用すべきでないため、このトピックの残りの部分では、稼働中ワークスペース パターンとタブ付きワークスペース パターンに焦点を当てます。</span><span class="sxs-lookup"><span data-stu-id="8f26e-127">The rest of this topic will focus on the Operational workspace pattern and the Tabbed Workspace pattern, as the original Workspace pattern is deprecated and should not be used.</span></span>

## <a name="wireframe"></a><span data-ttu-id="8f26e-128">ワイヤーフレーム</span><span class="sxs-lookup"><span data-stu-id="8f26e-128">Wireframe</span></span>

### <a name="operational-workspace"></a><span data-ttu-id="8f26e-129">運用ワークスペース</span><span class="sxs-lookup"><span data-stu-id="8f26e-129">Operational workspace</span></span>

<span data-ttu-id="8f26e-130">[![ワークスペース (1)](./media/workspace1.png)](./media/workspace1.png)</span><span class="sxs-lookup"><span data-stu-id="8f26e-130">[![Workspace(1)](./media/workspace1.png)](./media/workspace1.png)</span></span>

### <a name="tabbed-workspace"></a><span data-ttu-id="8f26e-131">タブ付きワークスペース</span><span class="sxs-lookup"><span data-stu-id="8f26e-131">Tabbed workspace</span></span>

<span data-ttu-id="8f26e-132">[![ワークスペース (2)](./media/tabbedWorkspaceWireframe.png)](./media/tabbedWorkspaceWireframe.png)</span><span class="sxs-lookup"><span data-stu-id="8f26e-132">[![Workspace(2)](./media/tabbedWorkspaceWireframe.png)](./media/tabbedWorkspaceWireframe.png)</span></span>

## <a name="pattern-changes-for-microsoft-dynamics-365-for-finance-and-operations"></a><span data-ttu-id="8f26e-133">Microsoft Dynamics 365 for Finance and Operations 用のパターンの変更</span><span class="sxs-lookup"><span data-stu-id="8f26e-133">Pattern changes for Microsoft Dynamics 365 for Finance and Operations</span></span>
<span data-ttu-id="8f26e-134">Microsoft Dynamics AX 2012 ロール センターは、アクティビティに特化した複数のワークスペースで置き換えられました。</span><span class="sxs-lookup"><span data-stu-id="8f26e-134">The Microsoft Dynamics AX 2012 Role Center has been replaced by multiple activity-focused workspaces.</span></span>

## <a name="model"></a><span data-ttu-id="8f26e-135">モデル</span><span class="sxs-lookup"><span data-stu-id="8f26e-135">Model</span></span>

### <a name="operational-workspace--high-level-structure"></a><span data-ttu-id="8f26e-136">運用ワークスペース – 高度なレベル構造</span><span class="sxs-lookup"><span data-stu-id="8f26e-136">Operational workspace – High-level structure</span></span>

- <span data-ttu-id="8f26e-137">デザイン</span><span class="sxs-lookup"><span data-stu-id="8f26e-137">Design</span></span>

    - <span data-ttu-id="8f26e-138">*アクション ウィンドウ (ActionPane) \[オプション\]*</span><span class="sxs-lookup"><span data-stu-id="8f26e-138">*Action pane (ActionPane) \[Optional\]*</span></span>
    - <span data-ttu-id="8f26e-139">*ワークスペース ページ フィルター グループ (グループ) \[オプション\]* – これは、[ワークスペース ページ フィルター グループ](workspace-filter-group-subpattern.md)のサブパターンを使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="8f26e-139">*Workspace page filter group (Group) \[Optional\]* – This must use the [Workspace Page Filter Group](workspace-filter-group-subpattern.md) subpattern.</span></span>
    - <span data-ttu-id="8f26e-140">パノラマ (タブ)</span><span class="sxs-lookup"><span data-stu-id="8f26e-140">Panorama (Tab)</span></span>

        - <span data-ttu-id="8f26e-141">セクション概要タイル (TabPage) – これは[セクション タイル](section-tiles-subpattern.md) サブパターンを使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="8f26e-141">Section summary tiles (TabPage) – This must use the [Section Tiles](section-tiles-subpattern.md) subpattern.</span></span>
        - <span data-ttu-id="8f26e-142">セクション タグ付きリスト (TabPage): これは[セクション タブ付きリスト](section-tabbed-list-subpattern.md) サブパターンを使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="8f26e-142">Section tabbed list (TabPage) – This must use the [Section Tabbed List](section-tabbed-list-subpattern.md) subpattern.</span></span>
        - <span data-ttu-id="8f26e-143">*セクション グラフ (TabPage) \[オプション\]* – これは[セクション 積み上げグラフ](section-stacked-chart-subpattern.md)サブパターンを使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="8f26e-143">*Section charts (TabPage) \[Optional\]* – This must use the [Section Stacked Chart](section-stacked-chart-subpattern.md) subpattern.</span></span>
        - <span data-ttu-id="8f26e-144">*セクション PowerBI (TabPage) \[オプション\]* – これは[セクション PowerBI](section-powerbi-subpattern.md) サブパターンを使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="8f26e-144">*Section PowerBI (TabPage) \[Optional\]* – This must use the [Section PowerBI](section-powerbi-subpattern.md) subpattern.</span></span>
        - <span data-ttu-id="8f26e-145">セクション関連リンク (TabPage): これは[セクション関連リンク](section-related-links-subpattern.md) サブパターンを使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="8f26e-145">Section related links (TabPage) – This must use the [Section Related Links](section-related-links-subpattern.md) subpattern.</span></span>

### <a name="tabbed-workspace--high-level-structure"></a><span data-ttu-id="8f26e-146">タブ付きワークスペース – 高度なレベル構造</span><span class="sxs-lookup"><span data-stu-id="8f26e-146">Tabbed workspace – High-level structure</span></span>

- <span data-ttu-id="8f26e-147">デザイン</span><span class="sxs-lookup"><span data-stu-id="8f26e-147">Design</span></span>

    - <span data-ttu-id="8f26e-148">*アクション ウィンドウ (ActionPane) \[オプション\]*</span><span class="sxs-lookup"><span data-stu-id="8f26e-148">*Action pane (ActionPane) \[Optional\]*</span></span>
    - <span data-ttu-id="8f26e-149">*ワークスペース ページ フィルター グループ (グループ) \[オプション\]* – これは、[ワークスペース ページ フィルター グループ](workspace-filter-group-subpattern.md)のサブパターンを使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="8f26e-149">*Workspace page filter group (Group) \[Optional\]* – This must use the [Workspace Page Filter Group](workspace-filter-group-subpattern.md) subpattern.</span></span>
    - <span data-ttu-id="8f26e-150">StandardTab (タブ)</span><span class="sxs-lookup"><span data-stu-id="8f26e-150">StandardTab (Tab)</span></span>

        - <span data-ttu-id="8f26e-151">ContentTabPage (1..N)</span><span class="sxs-lookup"><span data-stu-id="8f26e-151">ContentTabPage (1..N)</span></span> 

## <a name="core-components"></a><span data-ttu-id="8f26e-152">コア コンポーネント</span><span class="sxs-lookup"><span data-stu-id="8f26e-152">Core components</span></span>

-   <span data-ttu-id="8f26e-153">**Form.Design** に適切なワークスペース パターンを適用します。</span><span class="sxs-lookup"><span data-stu-id="8f26e-153">Apply the appropriate Workspace pattern on **Form.Design**.</span></span>
-   <span data-ttu-id="8f26e-154">BP 警告に対処します。</span><span class="sxs-lookup"><span data-stu-id="8f26e-154">Address BP Warnings:</span></span>
    -   <span data-ttu-id="8f26e-155">**フォーム**は少なくとも 1 つのメニュー項目で参照される必要があります。</span><span class="sxs-lookup"><span data-stu-id="8f26e-155">**Form** must be referenced by at least one menu item.</span></span>
    -   <span data-ttu-id="8f26e-156">**TabPage.Caption** は空ではありません (すべてのパノラマ セクションで)。</span><span class="sxs-lookup"><span data-stu-id="8f26e-156">**TabPage.Caption** isn't empty (for all panorama sections).</span></span>

## <a name="commonly-used-subpatterns"></a><span data-ttu-id="8f26e-157">一般的に使用されるサブパターン</span><span class="sxs-lookup"><span data-stu-id="8f26e-157">Commonly used subpatterns</span></span>

- [<span data-ttu-id="8f26e-158">ワークスペース ページ フィルター グループ </span><span class="sxs-lookup"><span data-stu-id="8f26e-158">Workspace Page Filter Group </span></span>](workspace-filter-group-subpattern.md)
- [<span data-ttu-id="8f26e-159">セクション タイル</span><span class="sxs-lookup"><span data-stu-id="8f26e-159">Section Tiles</span></span>](section-tiles-subpattern.md)
- [<span data-ttu-id="8f26e-160">セクション タブ付きリスト </span><span class="sxs-lookup"><span data-stu-id="8f26e-160">Section Tabbed List </span></span>](section-tabbed-list-subpattern.md)
- [<span data-ttu-id="8f26e-161">セクション積み上げグラフ</span><span class="sxs-lookup"><span data-stu-id="8f26e-161">Section Stacked Chart</span></span>](section-stacked-chart-subpattern.md)
- [<span data-ttu-id="8f26e-162">セクション PowerBI</span><span class="sxs-lookup"><span data-stu-id="8f26e-162">Section PowerBI</span></span>](section-powerbi-subpattern.md)
- [<span data-ttu-id="8f26e-163">セクション関連リンク</span><span class="sxs-lookup"><span data-stu-id="8f26e-163">Section Related Links</span></span>](section-related-links-subpattern.md)

## <a name="related-patterns"></a><span data-ttu-id="8f26e-164">関連するパターン</span><span class="sxs-lookup"><span data-stu-id="8f26e-164">Related patterns</span></span>

- [<span data-ttu-id="8f26e-165">フォーム パート セクション リスト</span><span class="sxs-lookup"><span data-stu-id="8f26e-165">Form Part Section List</span></span>](section-list-form-pattern.md)
- [<span data-ttu-id="8f26e-166">セクション グラフ</span><span class="sxs-lookup"><span data-stu-id="8f26e-166">Section Chart</span></span>](section-chart-form-pattern.md)

## <a name="ux-guidelines"></a><span data-ttu-id="8f26e-167">UX ガイドライン</span><span class="sxs-lookup"><span data-stu-id="8f26e-167">UX guidelines</span></span>
<span data-ttu-id="8f26e-168">検証チェックリストには、フォームが UX ガイドラインに準拠しているかどうかを手動で確認する手順が示されています。</span><span class="sxs-lookup"><span data-stu-id="8f26e-168">The verification checklist shows the steps for manually verifying that the form complies with UX guidelines.</span></span> <span data-ttu-id="8f26e-169">このチェックリストには、開発環境を通じて自動的に実施されるガイドラインは含まれていません。</span><span class="sxs-lookup"><span data-stu-id="8f26e-169">This checklist doesn't include any guidelines that will be enforced automatically through the development environment.</span></span> <span data-ttu-id="8f26e-170">ブラウザーでフォームを開いて、これらの手順を確認します。</span><span class="sxs-lookup"><span data-stu-id="8f26e-170">Open the form in the browser, and walk through these steps.</span></span>

-   <span data-ttu-id="8f26e-171">標準フォーム ガイドライン</span><span class="sxs-lookup"><span data-stu-id="8f26e-171">Standard form guidelines</span></span>
    -   <span data-ttu-id="8f26e-172">標準フォーム ガイドラインは、[全般的なガイドライン](general-form-guidelines.md) ドキュメントに統合されました。</span><span class="sxs-lookup"><span data-stu-id="8f26e-172">Standard form guidelines have been consolidated into the [General Form Guidelines](general-form-guidelines.md) document.</span></span>
-   <span data-ttu-id="8f26e-173">ワークスペース フォームのガイドライン</span><span class="sxs-lookup"><span data-stu-id="8f26e-173">Workspace form guidelines</span></span>
    -   <span data-ttu-id="8f26e-174">ページ タイトルには名詞句を使用し、一般的な単語は避けてください。</span><span class="sxs-lookup"><span data-stu-id="8f26e-174">Use a noun phase for the page title, and avoid general words.</span></span> <span data-ttu-id="8f26e-175">ページ タイトルは、エリア ページのタイトルと重複することはできません。</span><span class="sxs-lookup"><span data-stu-id="8f26e-175">The page title should not duplicate the title of an area page.</span></span>
    -   <span data-ttu-id="8f26e-176">ページ タイトルは、ユーザーが考えている名詞で始まる必要があります。</span><span class="sxs-lookup"><span data-stu-id="8f26e-176">The page title should begin with the noun that users would have in mind.</span></span>
    -   <span data-ttu-id="8f26e-177">すべてのセクションはタイトルを持つ必要があります。</span><span class="sxs-lookup"><span data-stu-id="8f26e-177">All sections must have a title.</span></span>
    -   <span data-ttu-id="8f26e-178">セクションは、通常 2 から 4 つの標準タイルの幅の範囲です。</span><span class="sxs-lookup"><span data-stu-id="8f26e-178">A section typically spans the width of two to four standard tiles.</span></span>
    -   <span data-ttu-id="8f26e-179">FormPartControl を使用してコンテンツを表示するセクションは、FormPartControl で **HeightMode** を **SizeToAvailable** に設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="8f26e-179">Any section that uses a FormPartControl to display content should have **HeightMode** set to **SizeToAvailable** on the FormPartControl.</span></span>
-   <span data-ttu-id="8f26e-180">操作</span><span class="sxs-lookup"><span data-stu-id="8f26e-180">Actions</span></span>
    -   <span data-ttu-id="8f26e-181">使用頻度の高いコマンドのみを含めます。</span><span class="sxs-lookup"><span data-stu-id="8f26e-181">Include only frequently used commands.</span></span>
    -   <span data-ttu-id="8f26e-182">アクション ウィンドウのアクションは、ワークスペース全体に関連付ける必要があります (ワークスペースの特定のセクションではありません)。</span><span class="sxs-lookup"><span data-stu-id="8f26e-182">Actions on the Action Pane should be related to the whole workspace (not a specific section of it).</span></span>
        -   <span data-ttu-id="8f26e-183">**例外:** 非常に頻繁に使用されている場合、**概要**セクションには、単一の「新規」アクションをタイルとして配置することができます。</span><span class="sxs-lookup"><span data-stu-id="8f26e-183">**Exception:** A single "New" action can be put as a tile in the **Summary** section if it's very frequently used.</span></span>
    -   <span data-ttu-id="8f26e-184">ドロップダウン メニューで、同じコマンドの変動をグループ化します。</span><span class="sxs-lookup"><span data-stu-id="8f26e-184">Group variations of the same command on drop-down menus.</span></span>
        -   <span data-ttu-id="8f26e-185">**例:** 新しい販売見積、新しい販売注文、新しい返品注文</span><span class="sxs-lookup"><span data-stu-id="8f26e-185">**Examples:** New sales quote, New sales order, New return order</span></span>
-   <span data-ttu-id="8f26e-186">フィルター</span><span class="sxs-lookup"><span data-stu-id="8f26e-186">Filters</span></span>
    -   <span data-ttu-id="8f26e-187">ワークスペース上に、0 ~ 5 つのフィルター フィールドが許されます。</span><span class="sxs-lookup"><span data-stu-id="8f26e-187">Zero to five filter fields are allowed on a workspace.</span></span>
        -   <span data-ttu-id="8f26e-188">単一フィールドのみ、そのページのタイトルの下に追加することができます。</span><span class="sxs-lookup"><span data-stu-id="8f26e-188">Only a single field can be put under the page title</span></span>
        -   <span data-ttu-id="8f26e-189">残りのフィルターは、ワークスペースの構成ダイアログにある必要があります。</span><span class="sxs-lookup"><span data-stu-id="8f26e-189">The remaining filters must be in a workspace configuration dialog.</span></span>

## <a name="example"></a><span data-ttu-id="8f26e-190">例</span><span class="sxs-lookup"><span data-stu-id="8f26e-190">Example</span></span>

### <a name="operational-workspace"></a><span data-ttu-id="8f26e-191">運用ワークスペース</span><span class="sxs-lookup"><span data-stu-id="8f26e-191">Operational workspace</span></span>

<span data-ttu-id="8f26e-192">フォーム: **FMClerkWorkspace**</span><span class="sxs-lookup"><span data-stu-id="8f26e-192">Form: **FMClerkWorkspace**</span></span> 

<span data-ttu-id="8f26e-193">[![ワークスペース (3)](./media/workspace3.png)](./media/workspace3.png)</span><span class="sxs-lookup"><span data-stu-id="8f26e-193">[![Workspace(3)](./media/workspace3.png)](./media/workspace3.png)</span></span>

## <a name="frequently-asked-questions"></a><span data-ttu-id="8f26e-194">よく寄せられる質問</span><span class="sxs-lookup"><span data-stu-id="8f26e-194">Frequently asked questions</span></span>

<span data-ttu-id="8f26e-195">このセクションには、このガイドライン/パターンに関連するよくある質問への回答があります。</span><span class="sxs-lookup"><span data-stu-id="8f26e-195">This section will have answers to frequently asked questions that are related to this guideline/pattern.</span></span>

## <a name="open-issues"></a><span data-ttu-id="8f26e-196">未処理の問題</span><span class="sxs-lookup"><span data-stu-id="8f26e-196">Open issues</span></span>

-   <span data-ttu-id="8f26e-197">なし</span><span class="sxs-lookup"><span data-stu-id="8f26e-197">None</span></span>

## <a name="ax-2012-content"></a><span data-ttu-id="8f26e-198">AX 2012 コンテンツ</span><span class="sxs-lookup"><span data-stu-id="8f26e-198">AX 2012 content</span></span>

### <a name="ax-2012-links"></a><span data-ttu-id="8f26e-199">AX 2012 リンク</span><span class="sxs-lookup"><span data-stu-id="8f26e-199">AX 2012 links</span></span>

-   <span data-ttu-id="8f26e-200">[MSDN ロール センター ページ参照 \[AX 2012\]](https://msdn.microsoft.com/library/cc558235.aspx)</span><span class="sxs-lookup"><span data-stu-id="8f26e-200">[MSDN Role Center Page Reference \[AX 2012\]](https://msdn.microsoft.com/library/cc558235.aspx)</span></span>
-   <span data-ttu-id="8f26e-201">[MSDN ロール センター ユーザー エクスペリエンス ガイドライン \[AX 2012\]](https://msdn.microsoft.com/library/gg886608.aspx)</span><span class="sxs-lookup"><span data-stu-id="8f26e-201">[MSDN Role Center User Experience Guidelines \[AX 2012\]](https://msdn.microsoft.com/library/gg886608.aspx)</span></span>

### <a name="ax-2012-example"></a><span data-ttu-id="8f26e-202">AX 2012 の例</span><span class="sxs-lookup"><span data-stu-id="8f26e-202">AX 2012 example</span></span>

<span data-ttu-id="8f26e-203">[![ワークスペース (5)](./media/workspace5.png)](./media/workspace5.png)</span><span class="sxs-lookup"><span data-stu-id="8f26e-203">[![Workspace(5)](./media/workspace5.png)](./media/workspace5.png)</span></span>
