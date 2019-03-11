---
title: 詳細マスター フォーム パターン
description: このトピックでは、詳細マスター フォームのパターンについて説明します。 詳細フォームは、データ入力の基本方法です。
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
ms.custom: 12373
ms.assetid: e4518f56-57b5-4cf1-b197-3fbaea7be861
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2f8e6f7e678d0d53f5d468ac6f9de4aa7cbe8a37
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/29/2019
ms.locfileid: "369490"
---
# <a name="details-master-form-pattern"></a><span data-ttu-id="4fdcc-104">詳細マスター フォーム パターン</span><span class="sxs-lookup"><span data-stu-id="4fdcc-104">Details Master form pattern</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="4fdcc-105">このトピックでは、詳細マスター フォームのパターンについて説明します。</span><span class="sxs-lookup"><span data-stu-id="4fdcc-105">This topic provides information about the Details Master form pattern.</span></span> <span data-ttu-id="4fdcc-106">詳細フォームは、データ入力の基本方法です。</span><span class="sxs-lookup"><span data-stu-id="4fdcc-106">A details form is the primary method for entering data.</span></span>

<a name="usage"></a><span data-ttu-id="4fdcc-107">用途</span><span class="sxs-lookup"><span data-stu-id="4fdcc-107">Usage</span></span>
-----

<span data-ttu-id="4fdcc-108">詳細フォームは、データ入力の基本方法です。</span><span class="sxs-lookup"><span data-stu-id="4fdcc-108">A details form is the primary method for entering data.</span></span> <span data-ttu-id="4fdcc-109">これらのフォームにより、ユーザーはデータを表示、編集、および操作できます。</span><span class="sxs-lookup"><span data-stu-id="4fdcc-109">These forms let the user view, edit, and act upon data.</span></span> <span data-ttu-id="4fdcc-110">これらフォーム タイプのすべてのコンテンツは展開および折りたたむことのできるクイック タブとして構造化されているため、複数のクイック タブを同時に開くことができます。</span><span class="sxs-lookup"><span data-stu-id="4fdcc-110">All content on these form types is structured into FastTabs that can be expanded and collapsed, so that multiple FastTabs can be open at the same time.</span></span> <span data-ttu-id="4fdcc-111">クイック タブには、フィールドやグリッドを含めることができ、各クイック タブはローカル ツール バーを持つことができます。</span><span class="sxs-lookup"><span data-stu-id="4fdcc-111">The FastTabs can contain fields or a grid, and each FastTab can have a local toolbar.</span></span> <span data-ttu-id="4fdcc-112">このドキュメントでは、2 つのパターンについて説明します。</span><span class="sxs-lookup"><span data-stu-id="4fdcc-112">Two patterns are described in this document:</span></span>

-   <span data-ttu-id="4fdcc-113">**詳細マスター** - これは、基本の詳細マスター パターンです。</span><span class="sxs-lookup"><span data-stu-id="4fdcc-113">**Detail Master** – This is the basic Detail Master pattern.</span></span> <span data-ttu-id="4fdcc-114">これは既定で使用されるパターンです。</span><span class="sxs-lookup"><span data-stu-id="4fdcc-114">This is the pattern that you should use by default.</span></span>
-   <span data-ttu-id="4fdcc-115">**タブ付き詳細マスター** - エンティティがカテゴリにグループ化できるクイック タブ (15 以上) を多数必要とする場合は、このパターンを使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="4fdcc-115">**Detail Master w/ Tabs** – You should use this pattern when an entity requires many FastTabs (more than 15) that can be grouped into categories.</span></span>

<span data-ttu-id="4fdcc-116">どちらの場合も、グリッド ビューの構成は同じです。</span><span class="sxs-lookup"><span data-stu-id="4fdcc-116">In both cases, the grid view is structured the same.</span></span>

## <a name="wireframe"></a><span data-ttu-id="4fdcc-117">ワイヤーフレーム</span><span class="sxs-lookup"><span data-stu-id="4fdcc-117">Wireframe</span></span>
### <a name="details-master"></a><span data-ttu-id="4fdcc-118">詳細マスター</span><span class="sxs-lookup"><span data-stu-id="4fdcc-118">Details Master</span></span>

#### <a name="details-view"></a><span data-ttu-id="4fdcc-119">詳細ビュー</span><span class="sxs-lookup"><span data-stu-id="4fdcc-119">Details view</span></span>

<span data-ttu-id="4fdcc-120">[![詳細マスター ワイヤーフレーム: 詳細ビュー](./media/detailsmaster1-1024x578.png)](./media/detailsmaster1.png)</span><span class="sxs-lookup"><span data-stu-id="4fdcc-120">[![Details Master wireframe: Details view](./media/detailsmaster1-1024x578.png)](./media/detailsmaster1.png)</span></span>

#### <a name="grid-view"></a><span data-ttu-id="4fdcc-121">グリッド ビュー</span><span class="sxs-lookup"><span data-stu-id="4fdcc-121">Grid view</span></span>

<span data-ttu-id="4fdcc-122">[![詳細マスター ワイヤーフレーム: グリッド ビュー](./media/detailsmaster2-1024x575.png)](./media/detailsmaster2.png)</span><span class="sxs-lookup"><span data-stu-id="4fdcc-122">[![Details Master wireframe: Grid view](./media/detailsmaster2-1024x575.png)](./media/detailsmaster2.png)</span></span>

### <a name="details-master-wstandard-tabs"></a><span data-ttu-id="4fdcc-123">詳細マスター / 標準タブ</span><span class="sxs-lookup"><span data-stu-id="4fdcc-123">Details Master w/Standard Tabs</span></span>

#### <a name="details-view"></a><span data-ttu-id="4fdcc-124">詳細ビュー</span><span class="sxs-lookup"><span data-stu-id="4fdcc-124">Details view</span></span>

<span data-ttu-id="4fdcc-125">[![詳細マスター / 標準タブ ワイヤーフレーム: 詳細ビュー](./media/detailsmaster3-1024x576.png)](./media/detailsmaster3.png)</span><span class="sxs-lookup"><span data-stu-id="4fdcc-125">[![Details Master w/Standard Tabs wireframe: Details view](./media/detailsmaster3-1024x576.png)](./media/detailsmaster3.png)</span></span>

#### <a name="grid-view"></a><span data-ttu-id="4fdcc-126">グリッド ビュー</span><span class="sxs-lookup"><span data-stu-id="4fdcc-126">Grid view</span></span>

<span data-ttu-id="4fdcc-127">[![詳細マスター / 標準タブ ワイヤーフレーム: グリッド ビュー](./media/detailsmaster4-1024x575.png)](./media/detailsmaster4.png)</span><span class="sxs-lookup"><span data-stu-id="4fdcc-127">[![Details Master w/Standard Tabs wireframe: Grid view](./media/detailsmaster4-1024x575.png)](./media/detailsmaster4.png)</span></span>

## <a name="pattern-changes"></a><span data-ttu-id="4fdcc-128">パターンの変更</span><span class="sxs-lookup"><span data-stu-id="4fdcc-128">Pattern changes</span></span>
<span data-ttu-id="4fdcc-129">Microsoft Dynamics AX 2012 以降に加えられるこのパターンへの主な変更を次に示します。</span><span class="sxs-lookup"><span data-stu-id="4fdcc-129">Here are the main changes to this pattern since Microsoft Dynamics AX 2012:</span></span>

-   <span data-ttu-id="4fdcc-130">詳細ビューコンテンツの左側にリスト スタイル グリッドが追加されました。</span><span class="sxs-lookup"><span data-stu-id="4fdcc-130">Added a List style grid to the left of the Details view content.</span></span>
-   <span data-ttu-id="4fdcc-131">リスト ページと詳細マスターが 1 つのフォームにマージされました。</span><span class="sxs-lookup"><span data-stu-id="4fdcc-131">Merged List Page and Details Master into a single form.</span></span>
    -   <span data-ttu-id="4fdcc-132">一覧と詳細の間を移動するときのパフォーマンスが向上します。</span><span class="sxs-lookup"><span data-stu-id="4fdcc-132">Improves performance when moving between a list and details.</span></span>
    -   <span data-ttu-id="4fdcc-133">初期一覧で一括編集を有効にします。</span><span class="sxs-lookup"><span data-stu-id="4fdcc-133">Enables bulk editing in the initial list.</span></span>
    -   <span data-ttu-id="4fdcc-134">プレビュー ウィンドウの一覧ページの消去を許可します。</span><span class="sxs-lookup"><span data-stu-id="4fdcc-134">Allows for elimination of the list page preview pane.</span></span>
-   <span data-ttu-id="4fdcc-135">表示/編集、新規作成、削除、保存、最新の情報に更新、添付、および Excel にエクスポートの各アクションはすべてファンデーションによって提供され、ファンデーションによって提供されたボタンが削除されない限り、各アクションに明示的なアプリ ボタンを使用する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="4fdcc-135">View/Edit, New, Delete, Save, Refresh, Attachments, and Export to Excel actions are all provided by the foundation and should not have explicit app buttons unless the foundation-provided button is removed.</span></span>
-   <span data-ttu-id="4fdcc-136">以前に TOC 拡張機能を使用したマスター詳細フォームでは、標準タブ パターン付きマスター詳細を使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="4fdcc-136">Master Details forms that previously used the TOC extension should now use the Master Details w/Standard Tabs pattern.</span></span>

## <a name="model"></a><span data-ttu-id="4fdcc-137">モデル</span><span class="sxs-lookup"><span data-stu-id="4fdcc-137">Model</span></span>
### <a name="details-master-basic--high-level-structure"></a><span data-ttu-id="4fdcc-138">詳細マスター (基本) – 高レベル構造体</span><span class="sxs-lookup"><span data-stu-id="4fdcc-138">Details Master (basic) – High-level structure</span></span>

- <span data-ttu-id="4fdcc-139">デザイン</span><span class="sxs-lookup"><span data-stu-id="4fdcc-139">Design</span></span>

    - <span data-ttu-id="4fdcc-140">ActionPane (ActionPane)</span><span class="sxs-lookup"><span data-stu-id="4fdcc-140">ActionPane (ActionPane)</span></span>
    - <span data-ttu-id="4fdcc-141">SidePanel (グループ)</span><span class="sxs-lookup"><span data-stu-id="4fdcc-141">SidePanel (Group)</span></span>

        - <span data-ttu-id="4fdcc-142">QuickFilter</span><span class="sxs-lookup"><span data-stu-id="4fdcc-142">QuickFilter</span></span>
        - <span data-ttu-id="4fdcc-143">*CustomFilter (グループ) \[オプション\]*</span><span class="sxs-lookup"><span data-stu-id="4fdcc-143">*CustomFilters (Group) \[Optional\]*</span></span>
        - <span data-ttu-id="4fdcc-144">NavigationList (グリッド、スタイル = リスト)</span><span class="sxs-lookup"><span data-stu-id="4fdcc-144">NavigationList (Grid, Style=List)</span></span>

    - <span data-ttu-id="4fdcc-145">MainTab (Tab ShowTabs=No)</span><span class="sxs-lookup"><span data-stu-id="4fdcc-145">MainTab (Tab ShowTabs=No)</span></span>

        - <span data-ttu-id="4fdcc-146">DetailsTabPage (TabPage)</span><span class="sxs-lookup"><span data-stu-id="4fdcc-146">DetailsTabPage (TabPage)</span></span>

            - <span data-ttu-id="4fdcc-147">TitleGroup (グループ)</span><span class="sxs-lookup"><span data-stu-id="4fdcc-147">TitleGroup (Group)</span></span>

                - <span data-ttu-id="4fdcc-148">HeaderTitle (文字列)</span><span class="sxs-lookup"><span data-stu-id="4fdcc-148">HeaderTitle (String)</span></span>
                - <span data-ttu-id="4fdcc-149">*EntityStatus (グループ) \[オプション\]*</span><span class="sxs-lookup"><span data-stu-id="4fdcc-149">*EntityStatus (Group) \[Optional\]*</span></span>

                    <span data-ttu-id="4fdcc-150">StatusFields (1..N)</span><span class="sxs-lookup"><span data-stu-id="4fdcc-150">StatusFields (1..N)</span></span>

            - <span data-ttu-id="4fdcc-151">DetailsTab (タブ スタイル =FastTabs)</span><span class="sxs-lookup"><span data-stu-id="4fdcc-151">DetailsTab (Tab Style=FastTabs)</span></span>

                - <span data-ttu-id="4fdcc-152">DetailsTabPage (TabPages *反復 1..N*)</span><span class="sxs-lookup"><span data-stu-id="4fdcc-152">DetailsTabPage (TabPages *repeats 1..N*)</span></span>

        - <span data-ttu-id="4fdcc-153">GridTabPage (TabPage)</span><span class="sxs-lookup"><span data-stu-id="4fdcc-153">GridTabPage (TabPage)</span></span>

            - <span data-ttu-id="4fdcc-154">CustomFilterGroup (グループ)</span><span class="sxs-lookup"><span data-stu-id="4fdcc-154">CustomFilterGroup (Group)</span></span>

                - <span data-ttu-id="4fdcc-155">QuickFilter</span><span class="sxs-lookup"><span data-stu-id="4fdcc-155">QuickFilter</span></span>
                - <span data-ttu-id="4fdcc-156">*OtherFilters ($ フィールド)\[0..N\]*</span><span class="sxs-lookup"><span data-stu-id="4fdcc-156">*OtherFilters ($Field) \[0..N\]*</span></span>

            - <span data-ttu-id="4fdcc-157">MainGrid (グリッド)</span><span class="sxs-lookup"><span data-stu-id="4fdcc-157">MainGrid (Grid)</span></span>
            - <span data-ttu-id="4fdcc-158">MainGridDefaultAction (CommandButton)</span><span class="sxs-lookup"><span data-stu-id="4fdcc-158">MainGridDefaultAction (CommandButton)</span></span>

### <a name="details-master-wstandard-tabs--high-level-structure"></a><span data-ttu-id="4fdcc-159">詳細マスター / 標準タブの詳細 – 高度な構造</span><span class="sxs-lookup"><span data-stu-id="4fdcc-159">Details Master w/Standard Tabs – High-level structure</span></span>

- <span data-ttu-id="4fdcc-160">デザイン</span><span class="sxs-lookup"><span data-stu-id="4fdcc-160">Design</span></span>

    - <span data-ttu-id="4fdcc-161">ActionPane (ActionPane)</span><span class="sxs-lookup"><span data-stu-id="4fdcc-161">ActionPane (ActionPane)</span></span>
    - <span data-ttu-id="4fdcc-162">SidePanel (グループ)</span><span class="sxs-lookup"><span data-stu-id="4fdcc-162">SidePanel (Group)</span></span>

        - <span data-ttu-id="4fdcc-163">QuickFilter</span><span class="sxs-lookup"><span data-stu-id="4fdcc-163">QuickFilter</span></span>
        - <span data-ttu-id="4fdcc-164">*CustomFilter (グループ) \[オプション\]*</span><span class="sxs-lookup"><span data-stu-id="4fdcc-164">*CustomFilters (Group) \[Optional\]*</span></span>
        - <span data-ttu-id="4fdcc-165">NavigationList (グリッド、スタイル = リスト)</span><span class="sxs-lookup"><span data-stu-id="4fdcc-165">NavigationList (Grid, Style=List)</span></span>

    - <span data-ttu-id="4fdcc-166">MainTab (Tab ShowTabs=No)</span><span class="sxs-lookup"><span data-stu-id="4fdcc-166">MainTab (Tab ShowTabs=No)</span></span>

        - <span data-ttu-id="4fdcc-167">DetailsTabPage (TabPage)</span><span class="sxs-lookup"><span data-stu-id="4fdcc-167">DetailsTabPage (TabPage)</span></span>

            - <span data-ttu-id="4fdcc-168">TitleGroup (グループ)</span><span class="sxs-lookup"><span data-stu-id="4fdcc-168">TitleGroup (Group)</span></span>

                - <span data-ttu-id="4fdcc-169">HeaderTitle (文字列)</span><span class="sxs-lookup"><span data-stu-id="4fdcc-169">HeaderTitle (String)</span></span>
                - <span data-ttu-id="4fdcc-170">*EntityStatus (グループ) \[オプション\]*</span><span class="sxs-lookup"><span data-stu-id="4fdcc-170">*EntityStatus (Group) \[Optional\]*</span></span>

                    - <span data-ttu-id="4fdcc-171">StatusFields (1…N)</span><span class="sxs-lookup"><span data-stu-id="4fdcc-171">StatusFields (1…N)</span></span>

            - <span data-ttu-id="4fdcc-172">CategoryTab (タブ スタイル = タブ)</span><span class="sxs-lookup"><span data-stu-id="4fdcc-172">CategoryTab (Tab Style=Tabs)</span></span>

                - <span data-ttu-id="4fdcc-173">CategoryTabPage (TabPages *反復 3..N*)</span><span class="sxs-lookup"><span data-stu-id="4fdcc-173">CategoryTabPage (TabPages *repeats 3..N*)</span></span>

                    - <span data-ttu-id="4fdcc-174">TabHeader (グループ)</span><span class="sxs-lookup"><span data-stu-id="4fdcc-174">TabHeader (Group)</span></span>
                    - <span data-ttu-id="4fdcc-175">DetailsTab (タブ スタイル =FastTabs)</span><span class="sxs-lookup"><span data-stu-id="4fdcc-175">DetailsTab (Tab Style=FastTabs)</span></span>

                        - <span data-ttu-id="4fdcc-176">DetailsTabPage (TabPages *反復 1..N*)</span><span class="sxs-lookup"><span data-stu-id="4fdcc-176">DetailsTabPage (TabPages *repeats 1..N*)</span></span>

        - <span data-ttu-id="4fdcc-177">GridTabPage (TabPage)</span><span class="sxs-lookup"><span data-stu-id="4fdcc-177">GridTabPage (TabPage)</span></span>

            - <span data-ttu-id="4fdcc-178">CustomFilterGroup (グループ)</span><span class="sxs-lookup"><span data-stu-id="4fdcc-178">CustomFilterGroup (Group)</span></span>

                - <span data-ttu-id="4fdcc-179">QuickFilter</span><span class="sxs-lookup"><span data-stu-id="4fdcc-179">QuickFilter</span></span>
                - <span data-ttu-id="4fdcc-180">*OtherFilters ($ フィールド)\[0..N\]*</span><span class="sxs-lookup"><span data-stu-id="4fdcc-180">*OtherFilters ($Field) \[0..N\]*</span></span>

            - <span data-ttu-id="4fdcc-181">MainGrid (グリッド)</span><span class="sxs-lookup"><span data-stu-id="4fdcc-181">MainGrid (Grid)</span></span>
            - <span data-ttu-id="4fdcc-182">MainGridDefaultAction (CommandButton)</span><span class="sxs-lookup"><span data-stu-id="4fdcc-182">MainGridDefaultAction (CommandButton)</span></span>

### <a name="core-components"></a><span data-ttu-id="4fdcc-183">コア コンポーネント</span><span class="sxs-lookup"><span data-stu-id="4fdcc-183">Core components</span></span>

1.  <span data-ttu-id="4fdcc-184">**Form.Design** に DetailsMaster パターンを適用します。</span><span class="sxs-lookup"><span data-stu-id="4fdcc-184">Apply the DetailsMaster pattern on **Form.Design**.</span></span>
2.  <span data-ttu-id="4fdcc-185">BP 警告に対処します。</span><span class="sxs-lookup"><span data-stu-id="4fdcc-185">Address BP Warnings:</span></span>
    1.  <span data-ttu-id="4fdcc-186">**Design.Caption** は空ではありません。</span><span class="sxs-lookup"><span data-stu-id="4fdcc-186">**Design.Caption** isn't empty.</span></span>
    2.  <span data-ttu-id="4fdcc-187">フォームは少なくとも 1 つのメニュー項目で参照される必要があります。</span><span class="sxs-lookup"><span data-stu-id="4fdcc-187">Form must be referenced by at least one menu item.</span></span>
    3.  <span data-ttu-id="4fdcc-188">**TabPage.Caption** は空ではありません。</span><span class="sxs-lookup"><span data-stu-id="4fdcc-188">**TabPage.Caption** isn't empty.</span></span>

### <a name="related-patterns"></a><span data-ttu-id="4fdcc-189">関連するパターン</span><span class="sxs-lookup"><span data-stu-id="4fdcc-189">Related patterns</span></span>

-   [<span data-ttu-id="4fdcc-190">詳細トランザクション</span><span class="sxs-lookup"><span data-stu-id="4fdcc-190">Details Transaction</span></span>](details-transaction-form-pattern.md)
-   [<span data-ttu-id="4fdcc-191">簡易リストと詳細</span><span class="sxs-lookup"><span data-stu-id="4fdcc-191">Simple List and Details</span></span>](simple-list-details-form-pattern.md)

### <a name="commonly-used-subpatterns"></a><span data-ttu-id="4fdcc-192">一般的に使用されるサブパターン</span><span class="sxs-lookup"><span data-stu-id="4fdcc-192">Commonly used subpatterns</span></span>

-   [<span data-ttu-id="4fdcc-193">フィールドおよびフィールド グループ</span><span class="sxs-lookup"><span data-stu-id="4fdcc-193">Fields and Field Groups</span></span>](fields-field-groups-subpattern.md)
-   [<span data-ttu-id="4fdcc-194">ツールバーおよびリスト</span><span class="sxs-lookup"><span data-stu-id="4fdcc-194">Toolbar and List</span></span>](toolbar-list-subpattern.md)
-   [<span data-ttu-id="4fdcc-195">ツールバーおよびフィールド</span><span class="sxs-lookup"><span data-stu-id="4fdcc-195">Toolbar and Fields</span></span>](toolbar-fields-subpattern.md)
-   [<span data-ttu-id="4fdcc-196">入れ子になった簡易リストおよび詳細</span><span class="sxs-lookup"><span data-stu-id="4fdcc-196">Nested Simple List and Details</span></span>](nested-simple-list-details-subpattern.md)
-   [<span data-ttu-id="4fdcc-197">カスタム フィルター グループ</span><span class="sxs-lookup"><span data-stu-id="4fdcc-197">Custom Filter Group</span></span>](custom-filter-group-subpattern.md)

## <a name="ux-guidelines"></a><span data-ttu-id="4fdcc-198">UX ガイドライン</span><span class="sxs-lookup"><span data-stu-id="4fdcc-198">UX guidelines</span></span>
<span data-ttu-id="4fdcc-199">検証チェックリストには、フォームが UX ガイドラインに準拠しているかどうかを手動で確認する手順が示されています。</span><span class="sxs-lookup"><span data-stu-id="4fdcc-199">The verification checklist shows the steps for manually verifying that the form complies with UX guidelines.</span></span> <span data-ttu-id="4fdcc-200">このチェックリストには、開発環境を通じて自動的に実施されるガイドラインは含まれていません。</span><span class="sxs-lookup"><span data-stu-id="4fdcc-200">This checklist doesn't include any guidelines that will be enforced automatically through the development environment.</span></span> <span data-ttu-id="4fdcc-201">ブラウザーでフォームを開いて、これらの手順を確認します。</span><span class="sxs-lookup"><span data-stu-id="4fdcc-201">Open the form in a browser, and walk through these steps.</span></span> <span data-ttu-id="4fdcc-202">**標準フォーム ガイドライン:**</span><span class="sxs-lookup"><span data-stu-id="4fdcc-202">**Standard form guidelines:**</span></span>

-   <span data-ttu-id="4fdcc-203">標準フォーム ガイドラインは、Microsoft Dynamics AX [全般的なガイドライン](general-form-guidelines.md) ドキュメントに統合されました。</span><span class="sxs-lookup"><span data-stu-id="4fdcc-203">Standard form guidelines have been consolidated into the Microsoft Dynamics AX [General Form Guidelines](general-form-guidelines.md) document.</span></span>

<span data-ttu-id="4fdcc-204">**詳細マスターガイドライン**</span><span class="sxs-lookup"><span data-stu-id="4fdcc-204">**Detail Master guidelines:**</span></span>

-   <span data-ttu-id="4fdcc-205">**新規** ボタンおよび **削除** ボタンは重複してはいけません。</span><span class="sxs-lookup"><span data-stu-id="4fdcc-205">There should not be any duplicate **New** and **Delete** buttons.</span></span>
-   <span data-ttu-id="4fdcc-206">従来のタブではなく、フィールドをグループ化するのにクイック タブを使用する必要がありますか。</span><span class="sxs-lookup"><span data-stu-id="4fdcc-206">Should use FastTabs to group the fields instead of traditional tabs.</span></span> <span data-ttu-id="4fdcc-207">詳細マスター / 標準タブ パターンは、関連するこれらのクイック タブを従来のタブにグループ化します。</span><span class="sxs-lookup"><span data-stu-id="4fdcc-207">The Details Master w/Standard Tabs pattern groups these related FastTabs into traditional tabs.</span></span>
    -   <span data-ttu-id="4fdcc-208">**既定**の状態で、最初のクイック タブのコンテンツはスクロールせずに完全に表示される必要があります。</span><span class="sxs-lookup"><span data-stu-id="4fdcc-208">In its **default** state, the content of the first FastTab should be fully visible without scrolling.</span></span>
    -   <span data-ttu-id="4fdcc-209">**クイック タブ**ガイドラインは、[フォームの全般的なガイドライン](general-form-guidelines.md) ドキュメントに統合されました。</span><span class="sxs-lookup"><span data-stu-id="4fdcc-209">**FastTabs** guidelines have been consolidated into the [General Form Guidelines ](general-form-guidelines.md) document.</span></span>
-   <span data-ttu-id="4fdcc-210">**ActionPane** ガイドラインは、ActionPane ガイドライン セクションの[フォームの全般的なガイドライン](general-form-guidelines.md) ドキュメントに統合されました。</span><span class="sxs-lookup"><span data-stu-id="4fdcc-210">**ActionPane** guidelines have been consolidated into the [General Form Guidelines ](general-form-guidelines.md) document, in the ActionPane guidelines section.</span></span>
-   <span data-ttu-id="4fdcc-211">**ページ タイトル エリア:**</span><span class="sxs-lookup"><span data-stu-id="4fdcc-211">**Page title area:**</span></span>
    -   <span data-ttu-id="4fdcc-212">"&lt;ID&gt; : &lt;Description&gt;" という形式を使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="4fdcc-212">The following format should be used: "&lt;ID&gt; : &lt;Description&gt;"</span></span>
    -   <span data-ttu-id="4fdcc-213">リスト ページが詳細ページにマージされている場合は、詳細ページへのリンクをメイン メニューで提供する必要があります。</span><span class="sxs-lookup"><span data-stu-id="4fdcc-213">A link to the Details page should be provided in the Main Menu when the List page has been merged into the Details page.</span></span>
    -   <span data-ttu-id="4fdcc-214">ページ タイトルは、複数フォームの形式にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="4fdcc-214">The page title should be in a plural form.</span></span>
-   <span data-ttu-id="4fdcc-215">**情報ボックス**ガイドラインは、[情報ボックスのフォーム パターン](factbox-form-patterns.md) ドキュメントに統合されました。</span><span class="sxs-lookup"><span data-stu-id="4fdcc-215">**FactBox** guidelines have been consolidated into the [FactBox Form Patterns](factbox-form-patterns.md) document.</span></span>
-   <span data-ttu-id="4fdcc-216">**ナビゲーション リスト グリッド:**</span><span class="sxs-lookup"><span data-stu-id="4fdcc-216">**Navigation list grid:**</span></span>
    -   <span data-ttu-id="4fdcc-217">リスト スタイル グリッドは、グリッド行内に行が 3 行以上にまたがるフィールドはありません。</span><span class="sxs-lookup"><span data-stu-id="4fdcc-217">The list style grid should not have fields within a grid row that cause the row to span more than three lines.</span></span>
        -   <span data-ttu-id="4fdcc-218">通常は IDと説明だけで十分です。</span><span class="sxs-lookup"><span data-stu-id="4fdcc-218">Typically, just the ID and Description are sufficient.</span></span>
        -   <span data-ttu-id="4fdcc-219">2 つ以上のフィールドが必要です。</span><span class="sxs-lookup"><span data-stu-id="4fdcc-219">There should be at least two fields.</span></span>
-   <span data-ttu-id="4fdcc-220">**グリッド ビュー:**</span><span class="sxs-lookup"><span data-stu-id="4fdcc-220">**Grid view:**</span></span>
    -   <span data-ttu-id="4fdcc-221">グリッドには 2 〜 15 個のフィールドがあります。</span><span class="sxs-lookup"><span data-stu-id="4fdcc-221">The grid has 2 to 15 fields.</span></span> <span data-ttu-id="4fdcc-222">通常はすべての必須フィールドが含まれているので、グリッド内にレコードを作成できます。</span><span class="sxs-lookup"><span data-stu-id="4fdcc-222">Typically, all mandatory fields are included, so that records can be created in the grid.</span></span>
    -   <span data-ttu-id="4fdcc-223">リンクされているフィールドを使用すると、ユーザーは選択したレコードの詳細を開くことができます。</span><span class="sxs-lookup"><span data-stu-id="4fdcc-223">A linked field lets the user open the details for the selected record.</span></span>
    -   <span data-ttu-id="4fdcc-224">クイック フィルターの既定値は、フィルター シナリオに最も可能性が高いフィールドに設定されます。</span><span class="sxs-lookup"><span data-stu-id="4fdcc-224">The Quick filter should default to the most likely field for a filter scenario.</span></span>
    -   <span data-ttu-id="4fdcc-225">**グリッド:**</span><span class="sxs-lookup"><span data-stu-id="4fdcc-225">**Grid:**</span></span>
        -   <span data-ttu-id="4fdcc-226">**ID** フィールドは最初の列にする必要があります (グリッドで必要な場合)。</span><span class="sxs-lookup"><span data-stu-id="4fdcc-226">The **ID** field should be the first column (if it's needed in the grid).</span></span> <span data-ttu-id="4fdcc-227">それ以外の場合、**名前** フィールドは最初の列にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="4fdcc-227">Otherwise, the **Name** field should be the first column.</span></span>
        -   <span data-ttu-id="4fdcc-228">追加のグリッド ガイドラインは、グリッド ガイドライン セクションの [全般的なフォームのガイドライン](general-form-guidelines.md) ドキュメントに統合されました。</span><span class="sxs-lookup"><span data-stu-id="4fdcc-228">Additional grid guidelines have been consolidated into the [General Form Guidelines ](general-form-guidelines.md) document, in the Grid guidelines section.</span></span>

## <a name="examples"></a><span data-ttu-id="4fdcc-229">例</span><span class="sxs-lookup"><span data-stu-id="4fdcc-229">Examples</span></span>
### <a name="details-master-basic"></a><span data-ttu-id="4fdcc-230">詳細マスター (基本)</span><span class="sxs-lookup"><span data-stu-id="4fdcc-230">Details Master (basic)</span></span>

<span data-ttu-id="4fdcc-231">フォーム: **CustTable**</span><span class="sxs-lookup"><span data-stu-id="4fdcc-231">Form: **CustTable**</span></span>

#### <a name="details-view-navigation-list-off"></a><span data-ttu-id="4fdcc-232">詳細ビュー (ナビゲーション リスト オフ)</span><span class="sxs-lookup"><span data-stu-id="4fdcc-232">Details view (navigation list off)</span></span>

<span data-ttu-id="4fdcc-233">[![詳細マスター (基本) の例: 詳細ビュー (ナビゲーション リスト オフ)](./media/detailsmaster5-1024x510.png)](./media/detailsmaster5.png)</span><span class="sxs-lookup"><span data-stu-id="4fdcc-233">[![Details Master (basic) example: Details view (navigation list off)](./media/detailsmaster5-1024x510.png)](./media/detailsmaster5.png)</span></span>

#### <a name="details-view-navigation-list-on"></a><span data-ttu-id="4fdcc-234">詳細ビュー (ナビゲーション リスト オン)</span><span class="sxs-lookup"><span data-stu-id="4fdcc-234">Details view (navigation list on)</span></span>

<span data-ttu-id="4fdcc-235">[![詳細マスター (基本) の例: 詳細ビュー (ナビゲーション リスト オン)](./media/detailsmaster6-1024x509.png)](./media/detailsmaster6.png)</span><span class="sxs-lookup"><span data-stu-id="4fdcc-235">[![Details Master (basic) example: Details view (navigation list on)](./media/detailsmaster6-1024x509.png)](./media/detailsmaster6.png)</span></span>

#### <a name="grid-view"></a><span data-ttu-id="4fdcc-236">グリッド ビュー</span><span class="sxs-lookup"><span data-stu-id="4fdcc-236">Grid view</span></span>

<span data-ttu-id="4fdcc-237">[![詳細マスター (基本) の例: グリッド ビュー](./media/detailsmaster7-1024x509.png)](./media/detailsmaster7.png)</span><span class="sxs-lookup"><span data-stu-id="4fdcc-237">[![Details Master (basic) example: Grid view](./media/detailsmaster7-1024x509.png)](./media/detailsmaster7.png)</span></span>

### <a name="details-master-wstandard-tabs"></a><span data-ttu-id="4fdcc-238">詳細マスター / 標準タブ</span><span class="sxs-lookup"><span data-stu-id="4fdcc-238">Details Master w/Standard Tabs</span></span>

<span data-ttu-id="4fdcc-239">フォーム: **HcmWorker**</span><span class="sxs-lookup"><span data-stu-id="4fdcc-239">Form: **HcmWorker**</span></span>

#### <a name="details-view-navigation-list-off"></a><span data-ttu-id="4fdcc-240">詳細ビュー (ナビゲーション リスト オフ)</span><span class="sxs-lookup"><span data-stu-id="4fdcc-240">Details view (navigation list off)</span></span>

<span data-ttu-id="4fdcc-241">[![詳細マスター / 標準タブの例: 詳細ビュー (ナビゲーション リスト オフ)](./media/detailsmaster8-1024x508.png)](./media/detailsmaster8.png)</span><span class="sxs-lookup"><span data-stu-id="4fdcc-241">[![Details Master w/Standard Tabs example: Details view (navigation list off)](./media/detailsmaster8-1024x508.png)](./media/detailsmaster8.png)</span></span>

#### <a name="details-view-navigation-list-on"></a><span data-ttu-id="4fdcc-242">詳細ビュー (ナビゲーション リスト オン)</span><span class="sxs-lookup"><span data-stu-id="4fdcc-242">Details view (navigation list on)</span></span>

<span data-ttu-id="4fdcc-243">[![詳細マスター / 標準タブの例: 詳細ビュー (ナビゲーション リスト オン)](./media/detailsmaster9-1024x508.png)](./media/detailsmaster9.png)</span><span class="sxs-lookup"><span data-stu-id="4fdcc-243">[![Details Master w/Standard Tabs example: Details view (navigation list on)](./media/detailsmaster9-1024x508.png)](./media/detailsmaster9.png)</span></span>

#### <a name="grid-view"></a><span data-ttu-id="4fdcc-244">グリッド ビュー</span><span class="sxs-lookup"><span data-stu-id="4fdcc-244">Grid view</span></span>

<span data-ttu-id="4fdcc-245">[![詳細マスター / 標準タブ例: グリッド ビュー](./media/detailsmaster10-1024x509.png)](./media/detailsmaster10.png)</span><span class="sxs-lookup"><span data-stu-id="4fdcc-245">[![Details Master w/Standard Tabs example: Grid view](./media/detailsmaster10-1024x509.png)](./media/detailsmaster10.png)</span></span>

## <a name="appendix"></a><span data-ttu-id="4fdcc-246">付録</span><span class="sxs-lookup"><span data-stu-id="4fdcc-246">Appendix</span></span>
### <a name="frequently-asked-questions"></a><span data-ttu-id="4fdcc-247">よく寄せられる質問</span><span class="sxs-lookup"><span data-stu-id="4fdcc-247">Frequently asked questions</span></span>

<span data-ttu-id="4fdcc-248">このセクションには、このガイドライン/パターンに関連するよくある質問への回答があります。</span><span class="sxs-lookup"><span data-stu-id="4fdcc-248">This section will have answers to frequently asked questions that are related to this guideline/pattern.</span></span>

### <a name="open-issues"></a><span data-ttu-id="4fdcc-249">未処理の問題</span><span class="sxs-lookup"><span data-stu-id="4fdcc-249">Open issues</span></span>

<span data-ttu-id="4fdcc-250">なし。</span><span class="sxs-lookup"><span data-stu-id="4fdcc-250">None.</span></span>

### <a name="ax-2012-content"></a><span data-ttu-id="4fdcc-251">AX 2012 コンテンツ</span><span class="sxs-lookup"><span data-stu-id="4fdcc-251">AX 2012 content</span></span>

#### <a name="ax-2012-links"></a><span data-ttu-id="4fdcc-252">AX 2012 リンク</span><span class="sxs-lookup"><span data-stu-id="4fdcc-252">AX 2012 links</span></span>
-   [<span data-ttu-id="4fdcc-253">AX 2012 MSDN 詳細のフォーム</span><span class="sxs-lookup"><span data-stu-id="4fdcc-253">AX 2012 MSDN Details Forms</span></span>](http://msdn.microsoft.com/EN-US/library/hh397318.aspx)

#### <a name="ax-2012-example"></a><span data-ttu-id="4fdcc-254">AX 2012 の例</span><span class="sxs-lookup"><span data-stu-id="4fdcc-254">AX 2012 example</span></span>

##### <a name="details-master-basic"></a><span data-ttu-id="4fdcc-255">詳細マスター (基本)</span><span class="sxs-lookup"><span data-stu-id="4fdcc-255">Details Master (basic)</span></span>

<span data-ttu-id="4fdcc-256">[![AX 2012 の例: 詳細マスター (基本) 1](./media/detailsmaster11-1024x647.png)](./media/detailsmaster11.png)</span><span class="sxs-lookup"><span data-stu-id="4fdcc-256">[![AX 2012 example: Details Master (basic) 1](./media/detailsmaster11-1024x647.png)](./media/detailsmaster11.png)</span></span> 

<span data-ttu-id="4fdcc-257">[![AX 2012 の例: 詳細マスター (基本) 2](./media/detailsmaster12-1024x647.png)](./media/detailsmaster12.png)</span><span class="sxs-lookup"><span data-stu-id="4fdcc-257">[![AX 2012 example: Details Master (basic) 2](./media/detailsmaster12-1024x647.png)](./media/detailsmaster12.png)</span></span>

##### <a name="details-master-wstandard-tabs"></a><span data-ttu-id="4fdcc-258">詳細マスター / 標準タブ</span><span class="sxs-lookup"><span data-stu-id="4fdcc-258">Details Master w/Standard Tabs</span></span>

<span data-ttu-id="4fdcc-259">[![AXAX 2012 の例: 詳細マスターと標準タブ 1](./media/detailsmaster13-1024x726.png)](./media/detailsmaster13.png)</span><span class="sxs-lookup"><span data-stu-id="4fdcc-259">[![AX 2012 example: Details Master w/Standard Tabs 1](./media/detailsmaster13-1024x726.png)](./media/detailsmaster13.png)</span></span> 

<span data-ttu-id="4fdcc-260">[![AX 2012 の例: 詳細マスターと標準タブ 2](./media/detailsmaster14-1024x620.png)](./media/detailsmaster14.png)</span><span class="sxs-lookup"><span data-stu-id="4fdcc-260">[![AX 2012 example: Details Master w/Standard Tabs 2](./media/detailsmaster14-1024x620.png)](./media/detailsmaster14.png)</span></span>



