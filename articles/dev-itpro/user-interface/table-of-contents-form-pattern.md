---
title: 目次のフォーム パターン
description: この記事では、目次フォームのパターンに関する情報を提供します。 このパターンは、セットアップ構成に論理的に関連する 2 つ以上のフォームが必要な場合に使用します。
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
ms.custom: 14621
ms.assetid: 1785880c-d729-43b7-bd78-9ae03bac4043
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0bedd642cd6f1c81103d793620986a6e8194ad02
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/29/2019
ms.locfileid: "369933"
---
# <a name="table-of-contents-form-pattern"></a><span data-ttu-id="5925c-104">目次のフォーム パターン</span><span class="sxs-lookup"><span data-stu-id="5925c-104">Table of Contents form pattern</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="5925c-105">この記事では、目次フォームのパターンに関する情報を提供します。</span><span class="sxs-lookup"><span data-stu-id="5925c-105">This article provides information about the Table of Contents form pattern.</span></span> <span data-ttu-id="5925c-106">このパターンは、セットアップ構成に論理的に関連する 2 つ以上のフォームが必要な場合に使用します。</span><span class="sxs-lookup"><span data-stu-id="5925c-106">This pattern should be used when two or more logically related forms are required for setup configuration.</span></span> 

<a name="usage"></a><span data-ttu-id="5925c-107">用途</span><span class="sxs-lookup"><span data-stu-id="5925c-107">Usage</span></span>
-----

<span data-ttu-id="5925c-108">目次パターンは、セットアップ構成に論理的に関連する 2 つ以上のフォームが必要な場合に使用します。</span><span class="sxs-lookup"><span data-stu-id="5925c-108">The Table of Contents pattern should be used when two or more logically related forms are required for setup configuration.</span></span> <span data-ttu-id="5925c-109">タブの垂直配置は、完了の順序を意味します。</span><span class="sxs-lookup"><span data-stu-id="5925c-109">The vertical arrangement of tabs implies the order of completion.</span></span> <span data-ttu-id="5925c-110">このフォーム パターンは、タブごとに異なるルート エンティティを持つタブ ページなど、無関係なアイテムのコレクションにも使用されます。 このフォーム パターンには、ツールバーとリスト、ネストされた簡易リストと詳細、またはフィールドとフィールド グループなどのコンテナー サブパターンに続く小さなコンテンツ領域の集合が含まれています。</span><span class="sxs-lookup"><span data-stu-id="5925c-110">This form pattern is also used for collections of unrelated items, such as tab pages that have a different root entity per tab. This form pattern contains a collection of smaller content regions, each of which follows a container subpattern such as Toolbar and List, Nested Simple List and Details, or Fields and Field Groups.</span></span>

## <a name="wireframe"></a><span data-ttu-id="5925c-111">ワイヤーフレーム</span><span class="sxs-lookup"><span data-stu-id="5925c-111">Wireframe</span></span>

<span data-ttu-id="5925c-112">[![TOC(1)](./media/toc1.png)](./media/toc1.png)</span><span class="sxs-lookup"><span data-stu-id="5925c-112">[![TOC(1)](./media/toc1.png)](./media/toc1.png)</span></span>

## <a name="pattern-changes"></a><span data-ttu-id="5925c-113">パターンの変更</span><span class="sxs-lookup"><span data-stu-id="5925c-113">Pattern changes</span></span>
<span data-ttu-id="5925c-114">Microsoft Dynamics AX 2012 以降に加えられるこのパターンへの主な変更を次に示します。</span><span class="sxs-lookup"><span data-stu-id="5925c-114">Here are the main changes to this pattern since Microsoft Dynamics AX 2012:</span></span>

-   <span data-ttu-id="5925c-115">Content Body 子コンテナーは、応答レイアウトに動的列を使用します。</span><span class="sxs-lookup"><span data-stu-id="5925c-115">The Content Body child container uses dynamic columns for a responsive layout.</span></span>
-   <span data-ttu-id="5925c-116">オプションの二次命令がタイトル グループの下に追加されました。</span><span class="sxs-lookup"><span data-stu-id="5925c-116">An optional secondary instruction has been added under the Title Group.</span></span>

## <a name="model"></a><span data-ttu-id="5925c-117">モデル</span><span class="sxs-lookup"><span data-stu-id="5925c-117">Model</span></span>
### <a name="high-level-structure"></a><span data-ttu-id="5925c-118">高レベル構造体</span><span class="sxs-lookup"><span data-stu-id="5925c-118">High-level structure</span></span>

- <span data-ttu-id="5925c-119">デザイン</span><span class="sxs-lookup"><span data-stu-id="5925c-119">Design</span></span>

    - <span data-ttu-id="5925c-120">タブ (スタイル = VerticalTabs)</span><span class="sxs-lookup"><span data-stu-id="5925c-120">Tab (Style=VerticalTabs)</span></span>

        - <span data-ttu-id="5925c-121">TabPage *\[1..N 回繰り返し\]*</span><span class="sxs-lookup"><span data-stu-id="5925c-121">TabPage *\[repeats 1..N times\]*</span></span>

            - <span data-ttu-id="5925c-122">タイトル (グループ)</span><span class="sxs-lookup"><span data-stu-id="5925c-122">Title (Group)</span></span>

                - <span data-ttu-id="5925c-123">MainInstruction (StaticText)</span><span class="sxs-lookup"><span data-stu-id="5925c-123">MainInstruction (StaticText)</span></span>
                - <span data-ttu-id="5925c-124">*SecondaryInstruction (StaticText) \[オプション\]*</span><span class="sxs-lookup"><span data-stu-id="5925c-124">*SecondaryInstruction (StaticText) \[Optional\]*</span></span>

            - <span data-ttu-id="5925c-125">本文 (グループ) | FastTabContent (タブ)</span><span class="sxs-lookup"><span data-stu-id="5925c-125">Body (Group) | FastTabContent (Tab)</span></span>

### <a name="core-components"></a><span data-ttu-id="5925c-126">コア コンポーネント</span><span class="sxs-lookup"><span data-stu-id="5925c-126">Core components</span></span>

-   <span data-ttu-id="5925c-127">**Form.Design** に TableOfContents パターンを適用します。</span><span class="sxs-lookup"><span data-stu-id="5925c-127">Apply the TableOfContents pattern on **Form.Design**.</span></span>
-   <span data-ttu-id="5925c-128">BP 警告に対処します。</span><span class="sxs-lookup"><span data-stu-id="5925c-128">Address BP Warnings:</span></span>
    -   <span data-ttu-id="5925c-129">**Design.Caption** は空ではありません。</span><span class="sxs-lookup"><span data-stu-id="5925c-129">**Design.Caption** isn't empty.</span></span>
    -   <span data-ttu-id="5925c-130">このフォームは少なくとも 1 つのメニュー項目で参照される必要があります。</span><span class="sxs-lookup"><span data-stu-id="5925c-130">The form must be referenced by at least one menu item.</span></span>
    -   <span data-ttu-id="5925c-131">**TabPage.Caption** は空ではありません。</span><span class="sxs-lookup"><span data-stu-id="5925c-131">**TabPage.Caption** isn't empty.</span></span>
    -   <span data-ttu-id="5925c-132">**TabPage.DataSource** は空ではありません。</span><span class="sxs-lookup"><span data-stu-id="5925c-132">**TabPage.DataSource** isn't empty.</span></span>
    -   <span data-ttu-id="5925c-133">**StaticText.Text** は空ではありません。</span><span class="sxs-lookup"><span data-stu-id="5925c-133">**StaticText.Text** isn't empty.</span></span>

### <a name="commonly-used-subpatterns"></a><span data-ttu-id="5925c-134">一般的に使用されるサブパターン</span><span class="sxs-lookup"><span data-stu-id="5925c-134">Commonly used subpatterns</span></span>

<span data-ttu-id="5925c-135">各 BodyGroup では、コンテンツ セクションのテーブルの内容に対して、次のコンテナー パターンのいずれかを使用します。</span><span class="sxs-lookup"><span data-stu-id="5925c-135">Each BodyGroup will use one of the following container patterns for the content in the Table of Contents section:</span></span>

-   [<span data-ttu-id="5925c-136">フィールドおよびフィールド グループ</span><span class="sxs-lookup"><span data-stu-id="5925c-136">Fields and Field Groups</span></span>](fields-field-groups-subpattern.md)
-   [<span data-ttu-id="5925c-137">ツールバーおよびリスト</span><span class="sxs-lookup"><span data-stu-id="5925c-137">Toolbar and List</span></span>](toolbar-list-subpattern.md)
-   [<span data-ttu-id="5925c-138">ツールバーおよびフィールド</span><span class="sxs-lookup"><span data-stu-id="5925c-138">Toolbar and Fields</span></span>](toolbar-fields-subpattern.md)
-   [<span data-ttu-id="5925c-139">入れ子になった簡易リストおよび詳細</span><span class="sxs-lookup"><span data-stu-id="5925c-139">Nested Simple List and Details</span></span>](nested-simple-list-details-subpattern.md)
-   [<span data-ttu-id="5925c-140">表形式フィールド</span><span class="sxs-lookup"><span data-stu-id="5925c-140">Tabular Fields</span></span>](tabular-fields-subpattern.md)
-   [<span data-ttu-id="5925c-141">リスト パネル</span><span class="sxs-lookup"><span data-stu-id="5925c-141">List Panel</span></span>](list-panel-subpattern.md)

## <a name="ux-guidelines"></a><span data-ttu-id="5925c-142">UX ガイドライン</span><span class="sxs-lookup"><span data-stu-id="5925c-142">UX guidelines</span></span>
<span data-ttu-id="5925c-143">検証チェックリストには、フォームが UX ガイドラインに準拠しているかどうかを手動で確認する手順が示されています。</span><span class="sxs-lookup"><span data-stu-id="5925c-143">The verification checklist shows the steps for manually verifying that the form complies with UX guidelines.</span></span> <span data-ttu-id="5925c-144">このチェックリストには、開発環境を通じて自動的に実施されるガイドラインは含まれていません。</span><span class="sxs-lookup"><span data-stu-id="5925c-144">This checklist doesn't include any guidelines that will be enforced automatically through the development environment.</span></span> <span data-ttu-id="5925c-145">ブラウザーでフォームを開いて、これらの手順を確認します。</span><span class="sxs-lookup"><span data-stu-id="5925c-145">Open the form in the browser, and walk through these steps.</span></span> 

<span data-ttu-id="5925c-146">**標準フォーム ガイドライン:**</span><span class="sxs-lookup"><span data-stu-id="5925c-146">**Standard form guidelines:**</span></span>

-   <span data-ttu-id="5925c-147">標準フォーム ガイドラインは、Microsoft Dynamics AX [全般的なガイドライン](general-form-guidelines.md) ドキュメントに統合されました。</span><span class="sxs-lookup"><span data-stu-id="5925c-147">Standard form guidelines have been consolidated into the Microsoft Dynamics AX [General Form Guidelines](general-form-guidelines.md) document.</span></span>

<span data-ttu-id="5925c-148">**目次 ガイドライン:**</span><span class="sxs-lookup"><span data-stu-id="5925c-148">**Table of contents guidelines:**</span></span>

-   <span data-ttu-id="5925c-149">補足命令が表示されている場合は、文例の完全で簡潔な文で構成され、終端の句読点が付きます。</span><span class="sxs-lookup"><span data-stu-id="5925c-149">The supplemental instruction, if it's shown, is composed of a complete, concise sentence in sentence case and has end punctuation.</span></span>
-   <span data-ttu-id="5925c-150">TOC タブは、情報の入力に通常使用されるのと同じ順序で表示されます。</span><span class="sxs-lookup"><span data-stu-id="5925c-150">TOC tabs should appear in the same sequence that is typically used to enter information.</span></span>
-   <span data-ttu-id="5925c-151">別のフォームの特定のタスクのコンテキストでフォームが開かれていない限り、フォームを開いたときにリストの最初のタブを強調表示する必要があります。</span><span class="sxs-lookup"><span data-stu-id="5925c-151">The first tab in the list should be highlighted when the form is opened, unless the form is opened in the context of a specific task from another form.</span></span>
-   <span data-ttu-id="5925c-152">目次コンテンツの**コンテンツ領域**は、主に 3 つのパターンのいずれかです (単純な一覧、単純なリストと詳細、または単純な詳細)。</span><span class="sxs-lookup"><span data-stu-id="5925c-152">The **content area** for the TOC content should primarily be one of three patterns: Simple List, Simple List and Details, or Simple Details.</span></span>
    -   <span data-ttu-id="5925c-153">簡易リスト コンテンツは、サブパターン ガイドラインに従う必要があります。</span><span class="sxs-lookup"><span data-stu-id="5925c-153">Simple List content should follow the subpattern guidelines.</span></span>
    -   <span data-ttu-id="5925c-154">簡易リストと詳細のコンテンツは、[入れ子になった簡易リストと詳細](nested-simple-list-details-subpattern.md)サブパターン ガイドラインに従う必要があります。</span><span class="sxs-lookup"><span data-stu-id="5925c-154">Simple List and Details content should follow the [Nested Simple List and Details](nested-simple-list-details-subpattern.md) subpattern guidelines.</span></span>
    -   <span data-ttu-id="5925c-155">簡易明細コンテンツは、[ツール バーとフィールド](toolbar-fields-subpattern.md) サブパターン ガイドラインに従う必要があります。</span><span class="sxs-lookup"><span data-stu-id="5925c-155">Simple Details content should follow the [Toolbar and Fields](toolbar-fields-subpattern.md) subpattern guidelines.</span></span>
    -   <span data-ttu-id="5925c-156">FastTabs は Dynamics AX [全般的なフォーム ガイドライン](general-form-guidelines.md) ドキュメントの FastTab ガイドラインに従う必要があります。</span><span class="sxs-lookup"><span data-stu-id="5925c-156">FastTabs should follow the FastTab guidelines in the Dynamics AX [General Form Guidelines ](general-form-guidelines.md) document.</span></span>
    -   <span data-ttu-id="5925c-157">タブ ページのツールバーに表示されるアクション。</span><span class="sxs-lookup"><span data-stu-id="5925c-157">Actions appearing on a Toolbar on a tab page.</span></span>
-   <span data-ttu-id="5925c-158">TOC フォームには、次の項目は**ありません**:</span><span class="sxs-lookup"><span data-stu-id="5925c-158">A TOC form should **not** have the following:</span></span>
    -   <span data-ttu-id="5925c-159">標準の ActionPane に対するアプリケーション アクション。</span><span class="sxs-lookup"><span data-stu-id="5925c-159">Application actions on a standard ActionPane.</span></span> <span data-ttu-id="5925c-160">(フレームワーク アクションのみを必要とします。)</span><span class="sxs-lookup"><span data-stu-id="5925c-160">(It should have only framework actions.)</span></span>
    -   <span data-ttu-id="5925c-161">情報ボックス。</span><span class="sxs-lookup"><span data-stu-id="5925c-161">FactBoxes.</span></span>
    -   <span data-ttu-id="5925c-162">TOC タブ ページ上の標準タブ。</span><span class="sxs-lookup"><span data-stu-id="5925c-162">Standard tabs on a TOC tab page.</span></span>

## <a name="examples"></a><span data-ttu-id="5925c-163">例</span><span class="sxs-lookup"><span data-stu-id="5925c-163">Examples</span></span>
<span data-ttu-id="5925c-164">フォーム: **CustParameters**</span><span class="sxs-lookup"><span data-stu-id="5925c-164">Form: **CustParameters**</span></span> 

<span data-ttu-id="5925c-165">[![TOC(2)](./media/toc2.png)](./media/toc2.png)</span><span class="sxs-lookup"><span data-stu-id="5925c-165">[![TOC(2)](./media/toc2.png)](./media/toc2.png)</span></span>

## <a name="appendix"></a><span data-ttu-id="5925c-166">付録</span><span class="sxs-lookup"><span data-stu-id="5925c-166">Appendix</span></span>
### <a name="frequently-asked-questions"></a><span data-ttu-id="5925c-167">よく寄せられる質問</span><span class="sxs-lookup"><span data-stu-id="5925c-167">Frequently asked questions</span></span>

<span data-ttu-id="5925c-168">このセクションには、このガイドライン/パターンに関連するよくある質問への回答があります。</span><span class="sxs-lookup"><span data-stu-id="5925c-168">This section will have answers to frequently asked questions that are related to this guideline/pattern.</span></span>

-   <span data-ttu-id="5925c-169">**グローバルボタンで何をすればいいですか?**</span><span class="sxs-lookup"><span data-stu-id="5925c-169">**What do I do with ‘Global’ buttons?**</span></span>
    -   <span data-ttu-id="5925c-170">データを初期化したり、サービス間で情報を同期させるためにボタンが必要な場合がいくつかあります。</span><span class="sxs-lookup"><span data-stu-id="5925c-170">There have been several cases where a button is required in order to initialize data or sync information between services.</span></span> <span data-ttu-id="5925c-171">このパターンでは標準アクション ウィンドウのシステム ボタンのみを許可するので、これらのボタンは次のいずれかの場所に移動することをお勧めします:</span><span class="sxs-lookup"><span data-stu-id="5925c-171">Because we allow only system buttons on the standard Action Pane in this pattern, we recommend that these buttons go in one of two places:</span></span>
        -   <span data-ttu-id="5925c-172">アクションが最も密接に関連しているタブ ページです。</span><span class="sxs-lookup"><span data-stu-id="5925c-172">On the tab page that the action is most closely related to.</span></span>
        -   <span data-ttu-id="5925c-173">場所が存在しない場合は、パターンの最初のタブ ページのツールバーに表示されます。</span><span class="sxs-lookup"><span data-stu-id="5925c-173">If a place doesn’t exist, on a toolbar on the first tab page of the pattern.</span></span>

### <a name="open-issues"></a><span data-ttu-id="5925c-174">未処理の問題</span><span class="sxs-lookup"><span data-stu-id="5925c-174">Open issues</span></span>

-   <span data-ttu-id="5925c-175">なし</span><span class="sxs-lookup"><span data-stu-id="5925c-175">None</span></span>

### <a name="ax-2012-content"></a><span data-ttu-id="5925c-176">AX 2012 コンテンツ</span><span class="sxs-lookup"><span data-stu-id="5925c-176">AX 2012 content</span></span>

<span data-ttu-id="5925c-177">[![TOC(3)](./media/toc3.png)](./media/toc3.png)</span><span class="sxs-lookup"><span data-stu-id="5925c-177">[![TOC(3)](./media/toc3.png)](./media/toc3.png)</span></span>

<span data-ttu-id="5925c-178">[![TOC(4)](./media/toc4.png)](./media/toc4.png)</span><span class="sxs-lookup"><span data-stu-id="5925c-178">[![TOC(4)](./media/toc4.png)](./media/toc4.png)</span></span>
