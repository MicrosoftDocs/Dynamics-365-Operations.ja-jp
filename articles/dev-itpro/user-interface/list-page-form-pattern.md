---
title: リスト ページのフォーム パターン
description: この記事では、リスト ページのフォーム パターンに関する情報を提供します。 リスト ページには、レコードを参照するために最適化された UI の一連のデータが表示されるため、特定のレコードを検索して連携できます。
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
ms.custom: 14241
ms.assetid: c70933b1-3d6a-4e26-b9ef-d9fb1e1b29a3
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 34f25a2c7320a8028e2214a0a1ab1898cbac3d23
ms.sourcegitcommit: 574d4dda83dcab94728a3d35fc53ee7e2b90feb0
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/22/2019
ms.locfileid: "1595482"
---
# <a name="list-page-form-pattern"></a><span data-ttu-id="5f94a-104">リスト ページのフォーム パターン</span><span class="sxs-lookup"><span data-stu-id="5f94a-104">List Page form pattern</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="5f94a-105">この記事では、リスト ページのフォーム パターンに関する情報を提供します。</span><span class="sxs-lookup"><span data-stu-id="5f94a-105">This article provides information about the List Page form pattern.</span></span> <span data-ttu-id="5f94a-106">リスト ページには、レコードを参照するために最適化された UI の一連のデータが表示されるため、特定のレコードを検索して連携できます。</span><span class="sxs-lookup"><span data-stu-id="5f94a-106">A list page presents a set of data on a UI that is optimized for browsing records, so that you can find and work with a specific record.</span></span> 

<a name="usage"></a><span data-ttu-id="5f94a-107">用途</span><span class="sxs-lookup"><span data-stu-id="5f94a-107">Usage</span></span>
-----

<span data-ttu-id="5f94a-108">リスト ページには、最適化されたユーザー インターフェイスの一連のデータが表示されるため、レコードの参照、適切なレコードの検索、そのレコードでのアクションを実行できます。</span><span class="sxs-lookup"><span data-stu-id="5f94a-108">A list page presents a set of data on a user interface that is optimized so that you can browse records, find the right record, and then take an action upon that record.</span></span> <span data-ttu-id="5f94a-109">リスト ページでは、ユーザーはデータを検索、フィルタリング、並べ替えできます。</span><span class="sxs-lookup"><span data-stu-id="5f94a-109">The list page lets the user search, filter, and sort the data.</span></span> <span data-ttu-id="5f94a-110">グリッドの右側にある情報ボックスは、有効なレコードの関連データを表示します。</span><span class="sxs-lookup"><span data-stu-id="5f94a-110">FactBoxes on the right side of the grid show related data for the active record.</span></span> <span data-ttu-id="5f94a-111">レコードに関連するアクションは、ページの上部にある ActionPane に配置されます。</span><span class="sxs-lookup"><span data-stu-id="5f94a-111">Actions that are relevant to the record are located on the ActionPane at the top of the page.</span></span> <span data-ttu-id="5f94a-112">現在、このパターンの使用は、リスト ページと詳細ページの間に 1 対 1 の対応がある場合は推奨されません。</span><span class="sxs-lookup"><span data-stu-id="5f94a-112">The use of this pattern is now discouraged when there is a 1:1 correspondence between the List Page and Details page.</span></span> <span data-ttu-id="5f94a-113">現在のガイダンスは、リスト ページにバッキングの詳細ページがない場合や複数のバッキングの詳細ページがある場合 (たとえば、プロジェクト見積と販売見積が同じリスト ページにまとめられている場合など) の場合のみ、このパターンを使用することです。</span><span class="sxs-lookup"><span data-stu-id="5f94a-113">Current guidance is to use this pattern only in other situations, such as when list pages have no backing details pages or have multiple backing details page (for example, when project quotations and sales quotations are shown together in the same List Page).</span></span>

## <a name="wireframe"></a><span data-ttu-id="5f94a-114">ワイヤーフレーム</span><span class="sxs-lookup"><span data-stu-id="5f94a-114">Wireframe</span></span>
<span data-ttu-id="5f94a-115">[![ワイヤーフレーム](./media/listpage1-1024x576.png)](./media/listpage1.png)</span><span class="sxs-lookup"><span data-stu-id="5f94a-115">[![Wireframe](./media/listpage1-1024x576.png)](./media/listpage1.png)</span></span>

## <a name="pattern-changes"></a><span data-ttu-id="5f94a-116">パターンの変更</span><span class="sxs-lookup"><span data-stu-id="5f94a-116">Pattern changes</span></span>
<span data-ttu-id="5f94a-117">Microsoft Dynamics AX 2012 以降に加えられるこのパターンへの主な変更を次に示します。</span><span class="sxs-lookup"><span data-stu-id="5f94a-117">Here are the main changes to this pattern since Microsoft Dynamics AX 2012:</span></span>

-   <span data-ttu-id="5f94a-118">FormTemplate/InteractionClass は、新しいページを構築する際にオプションになります。</span><span class="sxs-lookup"><span data-stu-id="5f94a-118">FormTemplate/InteractionClass is now optional when you build new pages.</span></span>
-   <span data-ttu-id="5f94a-119">リスト ページと詳細マスター/詳細トランザクションは、リスト ページと詳細ページで 1 対 1 の対応がある場合、1 つのフォームにマージされます。</span><span class="sxs-lookup"><span data-stu-id="5f94a-119">List Page and Details Master/Details Transaction are merged into a single form when there is a 1:1 correspondence between the List Page and Details Page.</span></span>
    -   <span data-ttu-id="5f94a-120">ユーザーが一覧と詳細の間を移動するときのパフォーマンスが向上します。</span><span class="sxs-lookup"><span data-stu-id="5f94a-120">Improves performance when the user moves between the list and details.</span></span>
    -   <span data-ttu-id="5f94a-121">バルクを初期一覧で編集できるように許可します。</span><span class="sxs-lookup"><span data-stu-id="5f94a-121">Allows for bulk editing in the initial list.</span></span>
-   <span data-ttu-id="5f94a-122">**プレビュー** ウィンドウが削除されました。</span><span class="sxs-lookup"><span data-stu-id="5f94a-122">The **Preview** pane has been eliminated.</span></span>

## <a name="model"></a><span data-ttu-id="5f94a-123">モデル</span><span class="sxs-lookup"><span data-stu-id="5f94a-123">Model</span></span>
### <a name="high-level-structure"></a><span data-ttu-id="5f94a-124">高レベル構造体</span><span class="sxs-lookup"><span data-stu-id="5f94a-124">High-level structure</span></span>

- <span data-ttu-id="5f94a-125">デザイン</span><span class="sxs-lookup"><span data-stu-id="5f94a-125">Design</span></span>

    - <span data-ttu-id="5f94a-126">ActionPane (ActionPane)</span><span class="sxs-lookup"><span data-stu-id="5f94a-126">ActionPane (ActionPane)</span></span>
    - <span data-ttu-id="5f94a-127">カスタム フィルター (グループ)</span><span class="sxs-lookup"><span data-stu-id="5f94a-127">Custom Filter (Group)</span></span>

        - <span data-ttu-id="5f94a-128">クイック フィルター (クイック フィルター)</span><span class="sxs-lookup"><span data-stu-id="5f94a-128">Quick Filter (Quick Filter)</span></span>
        - <span data-ttu-id="5f94a-129">*OtherFilters ($ フィールド)\[0..N\]*</span><span class="sxs-lookup"><span data-stu-id="5f94a-129">*OtherFilters ($Field) \[0..N\]*</span></span>

    - <span data-ttu-id="5f94a-130">グリッド (グリッド)</span><span class="sxs-lookup"><span data-stu-id="5f94a-130">Grid (Grid)</span></span>

### <a name="core-components"></a><span data-ttu-id="5f94a-131">コア コンポーネント</span><span class="sxs-lookup"><span data-stu-id="5f94a-131">Core components</span></span>

1.  <span data-ttu-id="5f94a-132">**Form.Design** に ListPage パターンを適用します。</span><span class="sxs-lookup"><span data-stu-id="5f94a-132">Apply the ListPage pattern on **Form.Design**.</span></span>
2.  <span data-ttu-id="5f94a-133">BP 警告に対処します。</span><span class="sxs-lookup"><span data-stu-id="5f94a-133">Address BP Warnings:</span></span>
    1.  <span data-ttu-id="5f94a-134">**Design.Caption** は空ではありません。</span><span class="sxs-lookup"><span data-stu-id="5f94a-134">**Design.Caption** isn't empty.</span></span>
    2.  <span data-ttu-id="5f94a-135">このフォームは少なくとも 1 つのメニュー項目で参照される必要があります。</span><span class="sxs-lookup"><span data-stu-id="5f94a-135">The form must be referenced by at least one menu item.</span></span>
    3.  <span data-ttu-id="5f94a-136">**TabPage.Caption** は空ではありません。</span><span class="sxs-lookup"><span data-stu-id="5f94a-136">**TabPage.Caption** isn't empty.</span></span>
    4.  <span data-ttu-id="5f94a-137">**TabPage.DataSource** は空ではありません。</span><span class="sxs-lookup"><span data-stu-id="5f94a-137">**TabPage.DataSource** isn't empty.</span></span>
    5.  <span data-ttu-id="5f94a-138">このプライマリ データ ソースには、**AllowEdit**=**いいえ**、**AllowCreate**=**いいえ**、および**AllowDelete**=**はい** が含まれています。</span><span class="sxs-lookup"><span data-stu-id="5f94a-138">The primary data source has **AllowEdit**=**No**, **AllowCreate**=**No**, and **AllowDelete**=**Yes**.</span></span>
    6.  <span data-ttu-id="5f94a-139">**Grid.DefaultAction** は、子フォームを開くボタンを参照します。</span><span class="sxs-lookup"><span data-stu-id="5f94a-139">**Grid.DefaultAction** references the button that opens the child form.</span></span>
    7.  <span data-ttu-id="5f94a-140">**Grid.DefaultLabelAction** は、グリッドのコンテキスト メニューに表示するラベルを参照します。</span><span class="sxs-lookup"><span data-stu-id="5f94a-140">**Grid.DefaultLabelAction** references a label to show in the grid context menu.</span></span>

### <a name="related-patterns"></a><span data-ttu-id="5f94a-141">関連するパターン</span><span class="sxs-lookup"><span data-stu-id="5f94a-141">Related patterns</span></span>

-   [<span data-ttu-id="5f94a-142">詳細マスター</span><span class="sxs-lookup"><span data-stu-id="5f94a-142">Details Master</span></span>](details-master-form-pattern.md)
-   [<span data-ttu-id="5f94a-143">詳細トランザクション</span><span class="sxs-lookup"><span data-stu-id="5f94a-143">Details Transaction</span></span>](details-transaction-form-pattern.md)
-   [<span data-ttu-id="5f94a-144">簡易リスト</span><span class="sxs-lookup"><span data-stu-id="5f94a-144">Simple List</span></span>](simple-list-form-pattern.md)

### <a name="commonly-used-subpatterns"></a><span data-ttu-id="5f94a-145">一般的に使用されるサブパターン</span><span class="sxs-lookup"><span data-stu-id="5f94a-145">Commonly used subpatterns</span></span>

-   [<span data-ttu-id="5f94a-146">カスタム フィルター グループ</span><span class="sxs-lookup"><span data-stu-id="5f94a-146">Custom Filter Group</span></span>](custom-filter-group-subpattern.md)

## <a name="ux-guidelines"></a><span data-ttu-id="5f94a-147">UX ガイドライン</span><span class="sxs-lookup"><span data-stu-id="5f94a-147">UX guidelines</span></span>
<span data-ttu-id="5f94a-148">検証チェックリストには、フォームが UX ガイドラインに準拠しているかどうかを手動で確認する手順が示されています。</span><span class="sxs-lookup"><span data-stu-id="5f94a-148">The verification checklist shows the steps for manually verifying that the form complies with UX guidelines.</span></span> <span data-ttu-id="5f94a-149">このチェックリストには、開発環境を通じて自動的に実施されるガイドラインは含まれていません。</span><span class="sxs-lookup"><span data-stu-id="5f94a-149">This checklist doesn't include any guidelines that will be enforced automatically through the development environment.</span></span> <span data-ttu-id="5f94a-150">ブラウザーでフォームを開いて、これらの手順を確認します。</span><span class="sxs-lookup"><span data-stu-id="5f94a-150">Open the form in the browser, and walk through these steps.</span></span> <span data-ttu-id="5f94a-151">**標準フォーム ガイドライン:**</span><span class="sxs-lookup"><span data-stu-id="5f94a-151">**Standard form guidelines:**</span></span>

-   <span data-ttu-id="5f94a-152">標準フォーム ガイドラインは、[全般的なガイドライン](general-form-guidelines.md) ドキュメントに統合されました。</span><span class="sxs-lookup"><span data-stu-id="5f94a-152">Standard form guidelines have been consolidated into the [General Form Guidelines](general-form-guidelines.md) document.</span></span>

<span data-ttu-id="5f94a-153">**リスト ページのガイドライン:**</span><span class="sxs-lookup"><span data-stu-id="5f94a-153">**List Page guidelines:**</span></span>

-   <span data-ttu-id="5f94a-154">グリッドに 15 未満のフィールドがあります。</span><span class="sxs-lookup"><span data-stu-id="5f94a-154">Have fewer than 15 fields in the grid.</span></span>
-   <span data-ttu-id="5f94a-155">最初のテキスト/データ列は、適切な詳細フォームに移動するリンクとして表示されます。</span><span class="sxs-lookup"><span data-stu-id="5f94a-155">The first textual/data column should be displayed as a link that goes to the appropriate details form.</span></span> <span data-ttu-id="5f94a-156">これを行うには、最初の列のハイパーリンクを有効にする既定のアクションがグリッドにあることを確認します。</span><span class="sxs-lookup"><span data-stu-id="5f94a-156">To do this, make sure that the grid has a default action to enable the hyperlink for the first column.</span></span>
-   <span data-ttu-id="5f94a-157">クイック フィルターは、リストの上に表示されます。</span><span class="sxs-lookup"><span data-stu-id="5f94a-157">A Quick Filter should appear above the list.</span></span> <span data-ttu-id="5f94a-158">既定では、QuickFilter はフィルター シナリオに最も可能性が高いフィールドを使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="5f94a-158">By default, the QuickFilter should use the most likely field for a filter scenario.</span></span>
-   <span data-ttu-id="5f94a-159">**新規** ボタンおよび **削除** ボタンは重複してはいけません。</span><span class="sxs-lookup"><span data-stu-id="5f94a-159">There should not be any duplicate **New** and **Delete** buttons.</span></span>
-   <span data-ttu-id="5f94a-160">リスト ページへのリンクをメイン メニューで提供する必要があります。</span><span class="sxs-lookup"><span data-stu-id="5f94a-160">A link to the List page should be provided in the Main Menu.</span></span>
-   <span data-ttu-id="5f94a-161">リスト ページを開いたときに、フォーカスがクイック フィルターにある必要があります。</span><span class="sxs-lookup"><span data-stu-id="5f94a-161">Focus should be in the Quick Filter when the list page is opened.</span></span>
-   <span data-ttu-id="5f94a-162">**ページ タイトル エリア**</span><span class="sxs-lookup"><span data-stu-id="5f94a-162">**Page title area**:</span></span>
    -   <span data-ttu-id="5f94a-163">ページ タイトルは、複数フォームの形式にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="5f94a-163">The page title should be in a plural form.</span></span>
    -   <span data-ttu-id="5f94a-164">プライマリ リスト ページについては、タイトルは、エンティティの名前である必要があります。</span><span class="sxs-lookup"><span data-stu-id="5f94a-164">For primary list pages, the title should be the name of the entity.</span></span>
    -   <span data-ttu-id="5f94a-165">セカンダリ リスト ページについては、タイトルは、活動またはステータスを反映する必要があります。</span><span class="sxs-lookup"><span data-stu-id="5f94a-165">For secondary list pages, the title should reflect an activity or status.</span></span>
-   <span data-ttu-id="5f94a-166">**グリッド**</span><span class="sxs-lookup"><span data-stu-id="5f94a-166">**Grid**:</span></span>
    -   <span data-ttu-id="5f94a-167">トランザクションのエンティティについては、**ID** フィールドが最初の列になり、次がマスタ エンティティ **ID** および **名前** フィールドになる必要があります。</span><span class="sxs-lookup"><span data-stu-id="5f94a-167">For transactional entities, the **ID** field should be the first column, followed by the master entity **ID** and **Name** fields.</span></span>
    -   <span data-ttu-id="5f94a-168">マスタ エンティティについては、**名前**フィールドが最初の列になり、次が **ID** フィールドになる必要があります。</span><span class="sxs-lookup"><span data-stu-id="5f94a-168">For master entities, the **Name** field should be the first column, followed by the **ID** field.</span></span>
-   <span data-ttu-id="5f94a-169">**ActionPane** ガイドラインは、ActionPane ガイドライン セクションの Dynamics AX 「[フォームの全般的なガイドライン](general-form-guidelines.md)」ドキュメントに統合されました。</span><span class="sxs-lookup"><span data-stu-id="5f94a-169">**ActionPane** guidelines have been consolidated into the Dynamics AX [General Form Guidelines ](general-form-guidelines.md) document in the ActionPane guidelines section.</span></span>
-   <span data-ttu-id="5f94a-170">**情報ボックス**ガイドラインは、[情報ボックスのフォーム パターン](factbox-form-patterns.md) ドキュメントに統合されました。</span><span class="sxs-lookup"><span data-stu-id="5f94a-170">**FactBox** guidelines have been consolidated into the [FactBox Form Patterns](factbox-form-patterns.md) document.</span></span>

## <a name="examples"></a><span data-ttu-id="5f94a-171">例</span><span class="sxs-lookup"><span data-stu-id="5f94a-171">Examples</span></span>
<span data-ttu-id="5f94a-172">フォーム: **SalesTableListPage** [![リスト ページの例](./media/listpage2-1024x510.png)](./media/listpage2.png)</span><span class="sxs-lookup"><span data-stu-id="5f94a-172">Form: **SalesTableListPage** [![List Page example](./media/listpage2-1024x510.png)](./media/listpage2.png)</span></span>

## <a name="appendix"></a><span data-ttu-id="5f94a-173">付録</span><span class="sxs-lookup"><span data-stu-id="5f94a-173">Appendix</span></span>
### <a name="frequently-asked-questions"></a><span data-ttu-id="5f94a-174">よく寄せられる質問</span><span class="sxs-lookup"><span data-stu-id="5f94a-174">Frequently asked questions</span></span>

<span data-ttu-id="5f94a-175">このセクションには、このガイドライン/パターンに関連するよくある質問への回答があります。</span><span class="sxs-lookup"><span data-stu-id="5f94a-175">This section will have answers to frequently asked questions that are related to this guideline/pattern.</span></span>

-   <span data-ttu-id="5f94a-176">**フォームを移行する時、プレビュー ウィンドウで何をすればよいでしょうか?**</span><span class="sxs-lookup"><span data-stu-id="5f94a-176">**What do I do with the Preview pane when I migrate the form?**</span></span>

    <span data-ttu-id="5f94a-177">次のいずれかを実行することができます。</span><span class="sxs-lookup"><span data-stu-id="5f94a-177">You can do one of the following:</span></span>

    -   <span data-ttu-id="5f94a-178">必要なくなった場合は、**プレビュー** ウィンドウを完全に削除します。</span><span class="sxs-lookup"><span data-stu-id="5f94a-178">Remove the **Preview** pane altogether if it no longer makes sense.</span></span>
    -   <span data-ttu-id="5f94a-179">大きいヘッダーを削除して、**プレビュー** ウィンドウをそのまま残します。</span><span class="sxs-lookup"><span data-stu-id="5f94a-179">Remove the large header, and leave the **Preview** pane as is.</span></span>
    -   <span data-ttu-id="5f94a-180">現在の **プレビュー** ウィンドウが高すぎる場合、複数の論理情報ボックスに分割します。</span><span class="sxs-lookup"><span data-stu-id="5f94a-180">Split the **Preview** pane into multiple logical FactBoxes if the current one is too tall.</span></span>
        -   <span data-ttu-id="5f94a-181">トランザクション プレビューでは、明細行は独自の情報ボックスに入り、5 つの明細行に限定される必要があります。</span><span class="sxs-lookup"><span data-stu-id="5f94a-181">For a transaction preview, the lines would go into their own FactBox and should be limited to five lines.</span></span>
        -   <span data-ttu-id="5f94a-182">トランザクションのプレビューでは、情報ボックス カード パターンへの明細行の再作業をします。その明細行は数に集計され、ユーザーが数値上にカーソルを置いたときに、明細行グリッドが拡張プレビューに表示されます。</span><span class="sxs-lookup"><span data-stu-id="5f94a-182">For a transaction preview, rework the lines into a FactBox card pattern, where the lines are summarized into a count and a lines grid is shown in an enhanced preview when the user hovers over the count value.</span></span>

### <a name="open-issues"></a><span data-ttu-id="5f94a-183">未処理の問題</span><span class="sxs-lookup"><span data-stu-id="5f94a-183">Open issues</span></span>

-   <span data-ttu-id="5f94a-184">**セカンダリ リスト ページの処理方法**</span><span class="sxs-lookup"><span data-stu-id="5f94a-184">**How to handle secondary list pages**</span></span>
    -   <span data-ttu-id="5f94a-185">ナビゲーションに残ります (アプリケーションの変更は必要なし)。</span><span class="sxs-lookup"><span data-stu-id="5f94a-185">Stay in navigation (no app changes needed).</span></span>
    -   <span data-ttu-id="5f94a-186">(将来のフレームワークのサポートが追加された後に) ロールに合わせたビューを作成します 。</span><span class="sxs-lookup"><span data-stu-id="5f94a-186">Create role-tailored views (after future framework support is added).</span></span>

### <a name="ax-2012-content"></a><span data-ttu-id="5f94a-187">AX 2012 コンテンツ</span><span class="sxs-lookup"><span data-stu-id="5f94a-187">AX 2012 content</span></span>

#### <a name="ax-2012-links"></a><span data-ttu-id="5f94a-188">AX 2012 リンク</span><span class="sxs-lookup"><span data-stu-id="5f94a-188">AX 2012 links</span></span>

-   [<span data-ttu-id="5f94a-189">MSDN AX 2012 リスト ページのユーザー エクスペリエンスのガイドライン</span><span class="sxs-lookup"><span data-stu-id="5f94a-189">MSDN AX 2012 List Page User Experience Guidelines</span></span>](https://msdn.microsoft.com/library/gg853328.aspx)
-   [<span data-ttu-id="5f94a-190">MSDN AX 2012 リスト ページ フォーム</span><span class="sxs-lookup"><span data-stu-id="5f94a-190">MSDN AX 2012 List Page Forms</span></span>](https://msdn.microsoft.com/library/cc635077.aspx)

#### <a name="ax-2012-example"></a><span data-ttu-id="5f94a-191">AX 2012 の例</span><span class="sxs-lookup"><span data-stu-id="5f94a-191">AX 2012 example</span></span>

<span data-ttu-id="5f94a-192">[![AX 2012 の例](./media/listpage3-1024x671.png)](./media/listpage3.png)</span><span class="sxs-lookup"><span data-stu-id="5f94a-192">[![AX 2012 example](./media/listpage3-1024x671.png)](./media/listpage3.png)</span></span>
