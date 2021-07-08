---
title: フォーム パターン セクション リストのフォーム パターン
description: このトピックでは、フォーム パート セクション リストのフォーム パターンに関する情報を提供します。これは、ワークスペース内にフィルタ処理されたリストを表示するために開発されました。
author: jasongre
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.custom: 29211
ms.assetid: 05e02e22-6b71-45f2-bacd-5e3f8ea898fb
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e7168179dfd64173516e07396378f813a34e8559
ms.sourcegitcommit: ff09736563d3cd2bc74c7664edd1767b218401cb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/04/2021
ms.locfileid: "6189910"
---
# <a name="form-part-section-list-form-patterns"></a><span data-ttu-id="6d80a-103">フォーム パターン セクション リストのフォーム パターン</span><span class="sxs-lookup"><span data-stu-id="6d80a-103">Form Part Section List form patterns</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6d80a-104">このトピックでは、フォーム パート セクション リストのフォーム パターンについての情報を提供します。</span><span class="sxs-lookup"><span data-stu-id="6d80a-104">This topic provides information about the Form Part Section List form patterns.</span></span> <span data-ttu-id="6d80a-105">これらのワークスペース固有のパターンは、ワークスペース内にフィルターされたリストを表示するために開発されました。</span><span class="sxs-lookup"><span data-stu-id="6d80a-105">These workspace-specific patterns have been developed to show filtered lists inside workspaces.</span></span>

## <a name="usage"></a><span data-ttu-id="6d80a-106">用途</span><span class="sxs-lookup"><span data-stu-id="6d80a-106">Usage</span></span>

<span data-ttu-id="6d80a-107">フォーム パターン セクション リストのフォーム パターンは、フィルター処理されたリストの表示に使用されるワークスペース固有のパターンです。</span><span class="sxs-lookup"><span data-stu-id="6d80a-107">The Form Part Section List form patterns are workspace-specific patterns that are used to show filtered lists.</span></span> <span data-ttu-id="6d80a-108">ワークスペースのタブ付きセクションには、一連の垂直タブが含まれています。</span><span class="sxs-lookup"><span data-stu-id="6d80a-108">The tabbed section of the workspace contains a set of vertical tabs.</span></span> <span data-ttu-id="6d80a-109">各タブはフォーム パーツ コントロールを含み、いずれかのフォーム パーツ セクション リスト パターンを含むフォームを指します。</span><span class="sxs-lookup"><span data-stu-id="6d80a-109">Each tab contains a Form Part Control that points to a form that contains one of the Form Part Section List patterns.</span></span> <span data-ttu-id="6d80a-110">この記事では、2 つのパターンについて説明します。</span><span class="sxs-lookup"><span data-stu-id="6d80a-110">Two patterns are described in this article:</span></span>

-   <span data-ttu-id="6d80a-111">**フォーム パターン セクション リスト** – これは、既定のセクション パターンです。</span><span class="sxs-lookup"><span data-stu-id="6d80a-111">**Form Part Section List** – This is the default Section pattern.</span></span> <span data-ttu-id="6d80a-112">これは、フィルターやアクションを含む省略可能なヘッダー グループと共に、単一のデータのリストに使用できます。</span><span class="sxs-lookup"><span data-stu-id="6d80a-112">It allows for a single list of data, together with an optional header group that contains filters and/or actions.</span></span>  <span data-ttu-id="6d80a-113">ワークスペースのタブ付きセクションにある大部分のコンテンツの領域が、このパターンを使用します。</span><span class="sxs-lookup"><span data-stu-id="6d80a-113">Most content areas in the tabbed section of a workspace will use this pattern.</span></span>
-   <span data-ttu-id="6d80a-114">**フォーム パターン セクション リスト - ダブル** – このバリアントでは、データの 2 番目のリストをプライマリ リストの右側に表示できます。</span><span class="sxs-lookup"><span data-stu-id="6d80a-114">**Form Part Section List - Double** – This variant enables a second list of data to appear to the right of the primary list.</span></span> <span data-ttu-id="6d80a-115">既定では、セカンダリ リストは表示されません。</span><span class="sxs-lookup"><span data-stu-id="6d80a-115">By default, the secondary list is hidden.</span></span> <span data-ttu-id="6d80a-116">これを表示するには、プライマリ リストの上にあるツールバーのボタンをクリックします。</span><span class="sxs-lookup"><span data-stu-id="6d80a-116">To show it, the user clicks a button on the Toolbar above the primary list.</span></span>

## <a name="wireframe"></a><span data-ttu-id="6d80a-117">ワイヤーフレーム</span><span class="sxs-lookup"><span data-stu-id="6d80a-117">Wireframe</span></span>
### <a name="form-part-section-list"></a><span data-ttu-id="6d80a-118">フォーム パート セクション リスト</span><span class="sxs-lookup"><span data-stu-id="6d80a-118">Form Part Section List</span></span>

<span data-ttu-id="6d80a-119">[![フォーム パターン セクション リストのフォーム パターンのワイヤーフレーム](./media/formpartsectionlistwireframe.png)](./media/formpartsectionlistwireframe.png)</span><span class="sxs-lookup"><span data-stu-id="6d80a-119">[![Wireframe for Form Part Section List form pattern](./media/formpartsectionlistwireframe.png)](./media/formpartsectionlistwireframe.png)</span></span>

### <a name="form-part-section-list---double"></a><span data-ttu-id="6d80a-120">フォーム パート セクション リスト - ダブル</span><span class="sxs-lookup"><span data-stu-id="6d80a-120">Form Part Section List - Double</span></span>

<span data-ttu-id="6d80a-121">[![フォーム パターン セクション リスト -- ダブル のフォーム パターンのワイヤーフレーム](./media/formpartsectionlistdoublewireframe.png)](./media/formpartsectionlistdoublewireframe.png)</span><span class="sxs-lookup"><span data-stu-id="6d80a-121">[![Wireframe for Form Part Section List--Double form pattern](./media/formpartsectionlistdoublewireframe.png)](./media/formpartsectionlistdoublewireframe.png)</span></span>

## <a name="pattern-changes-for-finance-and-operations"></a><span data-ttu-id="6d80a-122">Finance and Operations 用のパターンの変更</span><span class="sxs-lookup"><span data-stu-id="6d80a-122">Pattern changes for Finance and Operations</span></span>
<span data-ttu-id="6d80a-123">これらのパターンは、Microsoft Dynamics AX 2012 では存在しませんでした。</span><span class="sxs-lookup"><span data-stu-id="6d80a-123">These patterns did not exist for Microsoft Dynamics AX 2012.</span></span>

## <a name="model"></a><span data-ttu-id="6d80a-124">モデル</span><span class="sxs-lookup"><span data-stu-id="6d80a-124">Model</span></span>
### <a name="form-part-section-list-high-level-structure"></a><span data-ttu-id="6d80a-125">フォーム パート セクション リスト: 高レベルの構造</span><span class="sxs-lookup"><span data-stu-id="6d80a-125">Form Part Section List: High-level structure</span></span>

- <span data-ttu-id="6d80a-126">デザイン | コンテナー</span><span class="sxs-lookup"><span data-stu-id="6d80a-126">Design | Container</span></span>

    - <span data-ttu-id="6d80a-127">*ヘッダー (グループ) \[オプション\]* – これは、[フィルターおよびツールバー](filters-toolbar-subpattern.md)サブパターンのいずれかを使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="6d80a-127">*Header (Group) \[Optional\]* – This must use one of the [Filters and Toolbar](filters-toolbar-subpattern.md) subpatterns.</span></span>
    - <span data-ttu-id="6d80a-128">グリッド</span><span class="sxs-lookup"><span data-stu-id="6d80a-128">Grid</span></span>
    - <span data-ttu-id="6d80a-129">*GridDefaultAction (ボタン) \[オプション\]*</span><span class="sxs-lookup"><span data-stu-id="6d80a-129">*GridDefaultAction (Button) \[Optional\]*</span></span>
    - <span data-ttu-id="6d80a-130">*SeeMoreButton (ボタン) \[オプション\]*</span><span class="sxs-lookup"><span data-stu-id="6d80a-130">*SeeMoreButton (Button) \[Optional\]*</span></span>

### <a name="form-part-section-list---double-high-level-structure"></a><span data-ttu-id="6d80a-131">フォーム パート セクション リスト - ダブル: 高レベルの構造</span><span class="sxs-lookup"><span data-stu-id="6d80a-131">Form Part Section List - Double: High-level structure</span></span>

- <span data-ttu-id="6d80a-132">デザイン | コンテナー</span><span class="sxs-lookup"><span data-stu-id="6d80a-132">Design | Container</span></span>

    - <span data-ttu-id="6d80a-133">PrimaryGroup (グループ)</span><span class="sxs-lookup"><span data-stu-id="6d80a-133">PrimaryGroup (Group)</span></span>

        - <span data-ttu-id="6d80a-134">*ヘッダー (グループ) \[オプション\]* – これは、[フィルターおよびツールバー](filters-toolbar-subpattern.md)サブパターンのいずれかを使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="6d80a-134">*Header (Group) \[Optional\]* – This must use one of the [Filters and Toolbar](filters-toolbar-subpattern.md) subpatterns.</span></span>
        - <span data-ttu-id="6d80a-135">グリッド</span><span class="sxs-lookup"><span data-stu-id="6d80a-135">Grid</span></span>
        - <span data-ttu-id="6d80a-136">*GridDefaultAction (ボタン) \[オプション\]*</span><span class="sxs-lookup"><span data-stu-id="6d80a-136">*GridDefaultAction (Button) \[Optional\]*</span></span>
        - <span data-ttu-id="6d80a-137">*SeeMoreButton (ボタン) \[オプション\]*</span><span class="sxs-lookup"><span data-stu-id="6d80a-137">*SeeMoreButton (Button) \[Optional\]*</span></span>

    - <span data-ttu-id="6d80a-138">SecondaryGroup (グループ)</span><span class="sxs-lookup"><span data-stu-id="6d80a-138">SecondaryGroup (Group)</span></span>

        - <span data-ttu-id="6d80a-139">*ヘッダー (グループ) \[オプション\]* – これは、[フィルターおよびツールバー](filters-toolbar-subpattern.md)サブパターンのいずれかを使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="6d80a-139">*Header (Group) \[Optional\]* – This must use one of the [Filters and Toolbar](filters-toolbar-subpattern.md) subpatterns.</span></span>
        - <span data-ttu-id="6d80a-140">グリッド</span><span class="sxs-lookup"><span data-stu-id="6d80a-140">Grid</span></span>
        - <span data-ttu-id="6d80a-141">*GridDefaultAction (ボタン) \[オプション\]*</span><span class="sxs-lookup"><span data-stu-id="6d80a-141">*GridDefaultAction (Button) \[Optional\]*</span></span>
        - <span data-ttu-id="6d80a-142">*SeeMoreButton (ボタン) \[オプション\]*</span><span class="sxs-lookup"><span data-stu-id="6d80a-142">*SeeMoreButton (Button) \[Optional\]*</span></span>

### <a name="core-components"></a><span data-ttu-id="6d80a-143">コア コンポーネント</span><span class="sxs-lookup"><span data-stu-id="6d80a-143">Core components</span></span>

1.  <span data-ttu-id="6d80a-144">**Form.Design** に適切なフォーム パターン セクション リストのパターンを適用します。</span><span class="sxs-lookup"><span data-stu-id="6d80a-144">Apply the appropriate Form Part Section List pattern on **Form.Design**.</span></span>
2.  <span data-ttu-id="6d80a-145">バッキング運用ワークスペース フォームで、対応する垂直タブのフォーム パーツ コントロールを設定して、このフォームを指定するメニュー項目を指定します。</span><span class="sxs-lookup"><span data-stu-id="6d80a-145">In the backing Operational workspace form, set the Form Part control on the corresponding vertical tab to point to a menu item that points to this form.</span></span>

### <a name="related-container-patterns"></a><span data-ttu-id="6d80a-146">関連するコンテナー パターン</span><span class="sxs-lookup"><span data-stu-id="6d80a-146">Related container patterns</span></span>

-   [<span data-ttu-id="6d80a-147">セクション タブ付きリスト</span><span class="sxs-lookup"><span data-stu-id="6d80a-147">Section Tabbed List</span></span>](section-tabbed-list-subpattern.md)
-   [<span data-ttu-id="6d80a-148">フィルターおよびツールバー</span><span class="sxs-lookup"><span data-stu-id="6d80a-148">Filters and Toolbar</span></span>](filters-toolbar-subpattern.md)

## <a name="ux-guidelines"></a><span data-ttu-id="6d80a-149">UX ガイドライン</span><span class="sxs-lookup"><span data-stu-id="6d80a-149">UX guidelines</span></span>
<span data-ttu-id="6d80a-150">検証チェックリストには、フォームが UX ガイドラインに準拠しているかどうかを手動で確認する手順が示されています。</span><span class="sxs-lookup"><span data-stu-id="6d80a-150">The verification checklist shows the steps for manually verifying that the form complies with UX guidelines.</span></span> <span data-ttu-id="6d80a-151">このチェックリストには、開発環境を通じて自動的に実施されるガイドラインは含まれていません。</span><span class="sxs-lookup"><span data-stu-id="6d80a-151">This checklist doesn't include any guidelines that will be enforced automatically through the development environment.</span></span> <span data-ttu-id="6d80a-152">ブラウザーでフォームを開いて、これらの手順を確認します。</span><span class="sxs-lookup"><span data-stu-id="6d80a-152">Open the form in the browser, and walk through these steps.</span></span>

-   <span data-ttu-id="6d80a-153">**フォームの全般的なガイドライン**</span><span class="sxs-lookup"><span data-stu-id="6d80a-153">**General form guidelines**</span></span>
    -   <span data-ttu-id="6d80a-154">標準フォーム ガイドラインは、[全般的なガイドライン](general-form-guidelines.md) ドキュメントに統合されました。</span><span class="sxs-lookup"><span data-stu-id="6d80a-154">Standard form guidelines have been consolidated into the [General Form Guidelines](general-form-guidelines.md) document.</span></span>
-   <span data-ttu-id="6d80a-155">**パターン固有のガイドライン**</span><span class="sxs-lookup"><span data-stu-id="6d80a-155">**Pattern-specific guidelines**</span></span>
    -   <span data-ttu-id="6d80a-156">バックアップ フォームが存在し、特にすべてのレコードが一覧表示されていない場合に、**詳細情報** ボタンは、ユーザーが完全に一覧表示できるように、一覧の下部に表示されます。</span><span class="sxs-lookup"><span data-stu-id="6d80a-156">If a backing form exists, and especially if not all the records are shown in the list, a **See more** button should appear at the bottom of the list, so that the user can see the full list.</span></span>
    -   <span data-ttu-id="6d80a-157">リストの上には、最大 2 つの重要なフィルターが存在します。</span><span class="sxs-lookup"><span data-stu-id="6d80a-157">Up to two important filters exist above the list.</span></span>
    -   <span data-ttu-id="6d80a-158">リストの上には、頻繁に使用される最大で 3 つのアクションがあります。</span><span class="sxs-lookup"><span data-stu-id="6d80a-158">Up to three frequently used actions exist above the list.</span></span>
-   <span data-ttu-id="6d80a-159">**グリッド**</span><span class="sxs-lookup"><span data-stu-id="6d80a-159">**Grid**</span></span>
    -   <span data-ttu-id="6d80a-160">リストは、興味のある、比較的小規模のデータまでフィルター処理されます。</span><span class="sxs-lookup"><span data-stu-id="6d80a-160">Lists are filtered down to an interesting, relatively small set of data.</span></span>
    -   <span data-ttu-id="6d80a-161">リストのグリッドには、行ごとに 3 つまでの明細行があります。</span><span class="sxs-lookup"><span data-stu-id="6d80a-161">List grids have no more than three lines of data per row.</span></span>
    -   <span data-ttu-id="6d80a-162">カード グリッドには 4 つのフィールドしか表示されません (イメージは含まれません)。</span><span class="sxs-lookup"><span data-stu-id="6d80a-162">Card grids show no more than four fields (not including an image).</span></span>
    -   <span data-ttu-id="6d80a-163">表形式グリッドには、8 つを超えるフィールドが表示されます。</span><span class="sxs-lookup"><span data-stu-id="6d80a-163">Tabular grids show no more than eight fields.</span></span>
-   <span data-ttu-id="6d80a-164">**フォーム パターン セクション リスト - ダブルのガイドライン**</span><span class="sxs-lookup"><span data-stu-id="6d80a-164">**Form Part Section List - Double guidelines**</span></span>
    -   <span data-ttu-id="6d80a-165">両方のリストにアクションやフィルターがある場合は、両方のリストには、同じ [フィルターおよびツールバー](filters-toolbar-subpattern.md) サブパターン (積み上げバリアントまたはインライン バリアント) がある必要があります。</span><span class="sxs-lookup"><span data-stu-id="6d80a-165">If both lists have actions and/or filters, both list must use the same [Filters and Toolbar](filters-toolbar-subpattern.md) subpattern (either the Stacked variant or the Inline variant).</span></span>

## <a name="examples"></a><span data-ttu-id="6d80a-166">例</span><span class="sxs-lookup"><span data-stu-id="6d80a-166">Examples</span></span>
### <a name="form-part-section-list"></a><span data-ttu-id="6d80a-167">フォーム パート セクション リスト</span><span class="sxs-lookup"><span data-stu-id="6d80a-167">Form Part Section List</span></span>

<span data-ttu-id="6d80a-168">フォーム: **PurchOrderProcessReceiptsWorkspace** &gt; **PurchOrdersWithDelayedReceiptsPart** (**すべてのワークスペース** &gt; **発注書入庫とフォローアップ**)</span><span class="sxs-lookup"><span data-stu-id="6d80a-168">Form: **PurchOrderProcessReceiptsWorkspace** &gt; **PurchOrdersWithDelayedReceiptsPart** (**All workspaces** &gt; **Purchase order receipt and follow-up**)</span></span> 

<span data-ttu-id="6d80a-169">[![フォーム パート セクション リストの例](./media/formpartsectionlistexample.png)](./media/formpartsectionlistexample.png)</span><span class="sxs-lookup"><span data-stu-id="6d80a-169">[![Form Part Section List example](./media/formpartsectionlistexample.png)](./media/formpartsectionlistexample.png)</span></span>

### <a name="form-part-section-list---double"></a><span data-ttu-id="6d80a-170">フォーム パート セクション リスト - ダブル</span><span class="sxs-lookup"><span data-stu-id="6d80a-170">Form Part Section List - Double</span></span>

<span data-ttu-id="6d80a-171">フォーム: **BudgetTrackingWorkspace** &gt; **BudgetTransactionPart** (**すべてのワークスペース** &gt; **元帳予算および予測**)</span><span class="sxs-lookup"><span data-stu-id="6d80a-171">Form: **BudgetTrackingWorkspace** &gt; **BudgetTransactionPart** (**All workspaces** &gt; **Ledger budgets and forecasts**)</span></span> 

<span data-ttu-id="6d80a-172">[![フォーム パート セクション リスト -- ダブルの例](./media/formpartsectionlistdoubleexample.png)](./media/formpartsectionlistdoubleexample.png)</span><span class="sxs-lookup"><span data-stu-id="6d80a-172">[![Form Part Section List--Double example](./media/formpartsectionlistdoubleexample.png)](./media/formpartsectionlistdoubleexample.png)</span></span>

## <a name="appendix"></a><span data-ttu-id="6d80a-173">付録</span><span class="sxs-lookup"><span data-stu-id="6d80a-173">Appendix</span></span>
### <a name="frequently-asked-questions"></a><span data-ttu-id="6d80a-174">よく寄せられる質問</span><span class="sxs-lookup"><span data-stu-id="6d80a-174">Frequently asked questions</span></span>

<span data-ttu-id="6d80a-175">このセクションには、このガイドライン/パターンに関連するよくある質問への回答があります。</span><span class="sxs-lookup"><span data-stu-id="6d80a-175">This section will have answers to frequently asked questions that are related to this guideline/pattern.</span></span>

### <a name="open-issues"></a><span data-ttu-id="6d80a-176">未処理の問題</span><span class="sxs-lookup"><span data-stu-id="6d80a-176">Open issues</span></span>

<span data-ttu-id="6d80a-177">None</span><span class="sxs-lookup"><span data-stu-id="6d80a-177">None</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]