---
title: フォーム パート セクション リストのフォーム パターン
description: この記事では、フォーム パート セクション リストのフォーム パターンについての情報を提供します。 これらのワークスペース固有のパターンは、ワークスペース内にフィルターされたリストを表示するために開発されました。
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
ms.custom: 29211
ms.assetid: 05e02e22-6b71-45f2-bacd-5e3f8ea898fb
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1488b4871bcd1d9e3c90eb85894bd80ef84fe064
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/29/2019
ms.locfileid: "368425"
---
# <a name="form-part-section-list-form-patterns"></a><span data-ttu-id="dae35-104">フォーム パート セクション リストのフォーム パターン</span><span class="sxs-lookup"><span data-stu-id="dae35-104">Form Part Section List form patterns</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="dae35-105">この記事では、フォーム パート セクション リストのフォーム パターンについての情報を提供します。</span><span class="sxs-lookup"><span data-stu-id="dae35-105">This article provides information about the Form Part Section List form patterns.</span></span> <span data-ttu-id="dae35-106">これらのワークスペース固有のパターンは、ワークスペース内にフィルターされたリストを表示するために開発されました。</span><span class="sxs-lookup"><span data-stu-id="dae35-106">These workspace-specific patterns have been developed to show filtered lists inside workspaces.</span></span>

<a name="usage"></a><span data-ttu-id="dae35-107">用途</span><span class="sxs-lookup"><span data-stu-id="dae35-107">Usage</span></span>
-----

<span data-ttu-id="dae35-108">フォーム パターン セクション リストのフォーム パターンは、フィルター処理されたリストの表示に使用されるワークスペース固有のパターンです。</span><span class="sxs-lookup"><span data-stu-id="dae35-108">The Form Part Section List form patterns are workspace-specific patterns that are used to show filtered lists.</span></span> <span data-ttu-id="dae35-109">ワークスペースのタブ付きセクションには、一連の垂直タブが含まれています。</span><span class="sxs-lookup"><span data-stu-id="dae35-109">The tabbed section of the workspace contains a set of vertical tabs.</span></span> <span data-ttu-id="dae35-110">各タブはフォーム パーツ コントロールを含み、いずれかのフォーム パーツ セクション リスト パターンを含むフォームを指します。</span><span class="sxs-lookup"><span data-stu-id="dae35-110">Each tab contains a Form Part Control that points to a form that contains one of the Form Part Section List patterns.</span></span> <span data-ttu-id="dae35-111">この記事では、2 つのパターンについて説明します。</span><span class="sxs-lookup"><span data-stu-id="dae35-111">Two patterns are described in this article:</span></span>

-   <span data-ttu-id="dae35-112">**フォーム パターン セクション リスト** – これは、既定のセクション パターンです。</span><span class="sxs-lookup"><span data-stu-id="dae35-112">**Form Part Section List** – This is the default Section pattern.</span></span> <span data-ttu-id="dae35-113">これは、フィルターやアクションを含む省略可能なヘッダー グループと共に、単一のデータのリストに使用できます。</span><span class="sxs-lookup"><span data-stu-id="dae35-113">It allows for a single list of data, together with an optional header group that contains filters and/or actions.</span></span>  <span data-ttu-id="dae35-114">ワークスペースのタブ付きセクションにある大部分のコンテンツの領域が、このパターンを使用します。</span><span class="sxs-lookup"><span data-stu-id="dae35-114">Most content areas in the tabbed section of a workspace will use this pattern.</span></span>
-   <span data-ttu-id="dae35-115">**フォーム パターン セクション リスト - ダブル** – このバリアントでは、データの 2 番目のリストをプライマリ リストの右側に表示できます。</span><span class="sxs-lookup"><span data-stu-id="dae35-115">**Form Part Section List - Double** – This variant enables a second list of data to appear to the right of the primary list.</span></span> <span data-ttu-id="dae35-116">既定では、セカンダリ リストは表示されません。</span><span class="sxs-lookup"><span data-stu-id="dae35-116">By default, the secondary list is hidden.</span></span> <span data-ttu-id="dae35-117">これを表示するには、プライマリ リストの上にあるツールバーのボタンをクリックします。</span><span class="sxs-lookup"><span data-stu-id="dae35-117">To show it, the user clicks a button on the Toolbar above the primary list.</span></span>

## <a name="wireframe"></a><span data-ttu-id="dae35-118">ワイヤーフレーム</span><span class="sxs-lookup"><span data-stu-id="dae35-118">Wireframe</span></span>
### <a name="form-part-section-list"></a><span data-ttu-id="dae35-119">フォーム パート セクション リスト</span><span class="sxs-lookup"><span data-stu-id="dae35-119">Form Part Section List</span></span>

<span data-ttu-id="dae35-120">[![formPartSectionListWireframe](./media/formpartsectionlistwireframe.png)](./media/formpartsectionlistwireframe.png)</span><span class="sxs-lookup"><span data-stu-id="dae35-120">[![formPartSectionListWireframe](./media/formpartsectionlistwireframe.png)](./media/formpartsectionlistwireframe.png)</span></span>

### <a name="form-part-section-list---double"></a><span data-ttu-id="dae35-121">フォーム パート セクション リスト - ダブル</span><span class="sxs-lookup"><span data-stu-id="dae35-121">Form Part Section List - Double</span></span>

<span data-ttu-id="dae35-122">[![formPartSectionListDoubleWireframe](./media/formpartsectionlistdoublewireframe.png)](./media/formpartsectionlistdoublewireframe.png)</span><span class="sxs-lookup"><span data-stu-id="dae35-122">[![formPartSectionListDoubleWireframe](./media/formpartsectionlistdoublewireframe.png)](./media/formpartsectionlistdoublewireframe.png)</span></span>

## <a name="pattern-changes-for-microsoft-dynamics-365-for-finance-and-operations"></a><span data-ttu-id="dae35-123">Microsoft Dynamics 365 for Finance and Operations 用のパターンの変更</span><span class="sxs-lookup"><span data-stu-id="dae35-123">Pattern changes for Microsoft Dynamics 365 for Finance and Operations</span></span>
<span data-ttu-id="dae35-124">これらのパターンは、Microsoft DynamicsAX 2012 では存在しませんでした。</span><span class="sxs-lookup"><span data-stu-id="dae35-124">These patterns did not exist for Microsoft Dynamics AX 2012.</span></span>

## <a name="model"></a><span data-ttu-id="dae35-125">モデル</span><span class="sxs-lookup"><span data-stu-id="dae35-125">Model</span></span>
### <a name="form-part-section-list-high-level-structure"></a><span data-ttu-id="dae35-126">フォーム パート セクション リスト: 高レベルの構造</span><span class="sxs-lookup"><span data-stu-id="dae35-126">Form Part Section List: High-level structure</span></span>

- <span data-ttu-id="dae35-127">デザイン | コンテナー</span><span class="sxs-lookup"><span data-stu-id="dae35-127">Design | Container</span></span>

    - <span data-ttu-id="dae35-128">*ヘッダー (グループ) \[オプション\]* – これは、[フィルターおよびツールバー](filters-toolbar-subpattern.md)サブパターンのいずれかを使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="dae35-128">*Header (Group) \[Optional\]* – This must use one of the [Filters and Toolbar](filters-toolbar-subpattern.md) subpatterns.</span></span>
    - <span data-ttu-id="dae35-129">グリッド</span><span class="sxs-lookup"><span data-stu-id="dae35-129">Grid</span></span>
    - <span data-ttu-id="dae35-130">*GridDefaultAction (ボタン) \[オプション\]*</span><span class="sxs-lookup"><span data-stu-id="dae35-130">*GridDefaultAction (Button) \[Optional\]*</span></span>
    - <span data-ttu-id="dae35-131">*SeeMoreButton (ボタン) \[オプション\]*</span><span class="sxs-lookup"><span data-stu-id="dae35-131">*SeeMoreButton (Button) \[Optional\]*</span></span>

### <a name="form-part-section-list---double-high-level-structure"></a><span data-ttu-id="dae35-132">フォーム パート セクション リスト - ダブル: 高レベルの構造</span><span class="sxs-lookup"><span data-stu-id="dae35-132">Form Part Section List - Double: High-level structure</span></span>

- <span data-ttu-id="dae35-133">デザイン | コンテナー</span><span class="sxs-lookup"><span data-stu-id="dae35-133">Design | Container</span></span>

    - <span data-ttu-id="dae35-134">PrimaryGroup (グループ)</span><span class="sxs-lookup"><span data-stu-id="dae35-134">PrimaryGroup (Group)</span></span>

        - <span data-ttu-id="dae35-135">*ヘッダー (グループ) \[オプション\]* – これは、[フィルターおよびツールバー](filters-toolbar-subpattern.md)サブパターンのいずれかを使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="dae35-135">*Header (Group) \[Optional\]* – This must use one of the [Filters and Toolbar](filters-toolbar-subpattern.md) subpatterns.</span></span>
        - <span data-ttu-id="dae35-136">グリッド</span><span class="sxs-lookup"><span data-stu-id="dae35-136">Grid</span></span>
        - <span data-ttu-id="dae35-137">*GridDefaultAction (ボタン) \[オプション\]*</span><span class="sxs-lookup"><span data-stu-id="dae35-137">*GridDefaultAction (Button) \[Optional\]*</span></span>
        - <span data-ttu-id="dae35-138">*SeeMoreButton (ボタン) \[オプション\]*</span><span class="sxs-lookup"><span data-stu-id="dae35-138">*SeeMoreButton (Button) \[Optional\]*</span></span>

    - <span data-ttu-id="dae35-139">SecondaryGroup (グループ)</span><span class="sxs-lookup"><span data-stu-id="dae35-139">SecondaryGroup (Group)</span></span>

        - <span data-ttu-id="dae35-140">*ヘッダー (グループ) \[オプション\]* – これは、[フィルターおよびツールバー](filters-toolbar-subpattern.md)サブパターンのいずれかを使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="dae35-140">*Header (Group) \[Optional\]* – This must use one of the [Filters and Toolbar](filters-toolbar-subpattern.md) subpatterns.</span></span>
        - <span data-ttu-id="dae35-141">グリッド</span><span class="sxs-lookup"><span data-stu-id="dae35-141">Grid</span></span>
        - <span data-ttu-id="dae35-142">*GridDefaultAction (ボタン) \[オプション\]*</span><span class="sxs-lookup"><span data-stu-id="dae35-142">*GridDefaultAction (Button) \[Optional\]*</span></span>
        - <span data-ttu-id="dae35-143">*SeeMoreButton (ボタン) \[オプション\]*</span><span class="sxs-lookup"><span data-stu-id="dae35-143">*SeeMoreButton (Button) \[Optional\]*</span></span>

### <a name="core-components"></a><span data-ttu-id="dae35-144">コア コンポーネント</span><span class="sxs-lookup"><span data-stu-id="dae35-144">Core components</span></span>

1.  <span data-ttu-id="dae35-145">**Form.Design** に適切なフォーム パターン セクション リストのパターンを適用します。</span><span class="sxs-lookup"><span data-stu-id="dae35-145">Apply the appropriate Form Part Section List pattern on **Form.Design**.</span></span>
2.  <span data-ttu-id="dae35-146">バッキング運用ワークスペース フォームで、対応する垂直タブのフォーム パーツ コントロールを設定して、このフォームを指定するメニュー項目を指定します。</span><span class="sxs-lookup"><span data-stu-id="dae35-146">In the backing Operational workspace form, set the Form Part control on the corresponding vertical tab to point to a menu item that points to this form.</span></span>

### <a name="related-container-patterns"></a><span data-ttu-id="dae35-147">関連するコンテナー パターン</span><span class="sxs-lookup"><span data-stu-id="dae35-147">Related container patterns</span></span>

-   [<span data-ttu-id="dae35-148">セクション タブ付きリスト</span><span class="sxs-lookup"><span data-stu-id="dae35-148">Section Tabbed List</span></span>](section-tabbed-list-subpattern.md)
-   [<span data-ttu-id="dae35-149">フィルターおよびツールバー</span><span class="sxs-lookup"><span data-stu-id="dae35-149">Filters and Toolbar</span></span>](filters-toolbar-subpattern.md)

## <a name="ux-guidelines"></a><span data-ttu-id="dae35-150">UX ガイドライン</span><span class="sxs-lookup"><span data-stu-id="dae35-150">UX guidelines</span></span>
<span data-ttu-id="dae35-151">検証チェックリストには、フォームが UX ガイドラインに準拠しているかどうかを手動で確認する手順が示されています。</span><span class="sxs-lookup"><span data-stu-id="dae35-151">The verification checklist shows the steps for manually verifying that the form complies with UX guidelines.</span></span> <span data-ttu-id="dae35-152">このチェックリストには、開発環境を通じて自動的に実施されるガイドラインは含まれていません。</span><span class="sxs-lookup"><span data-stu-id="dae35-152">This checklist doesn't include any guidelines that will be enforced automatically through the development environment.</span></span> <span data-ttu-id="dae35-153">ブラウザーでフォームを開いて、これらの手順を確認します。</span><span class="sxs-lookup"><span data-stu-id="dae35-153">Open the form in the browser, and walk through these steps.</span></span>

-   <span data-ttu-id="dae35-154">**フォームの全般的なガイドライン**</span><span class="sxs-lookup"><span data-stu-id="dae35-154">**General form guidelines**</span></span>
    -   <span data-ttu-id="dae35-155">標準フォーム ガイドラインは、[全般的なガイドライン](general-form-guidelines.md) ドキュメントに統合されました。</span><span class="sxs-lookup"><span data-stu-id="dae35-155">Standard form guidelines have been consolidated into the [General Form Guidelines](general-form-guidelines.md) document.</span></span>
-   <span data-ttu-id="dae35-156">**パターン固有のガイドライン**</span><span class="sxs-lookup"><span data-stu-id="dae35-156">**Pattern-specific guidelines**</span></span>
    -   <span data-ttu-id="dae35-157">バックアップ フォームが存在し、特にすべてのレコードが一覧表示されていない場合に、**詳細情報** ボタンは、ユーザーが完全に一覧表示できるように、一覧の下部に表示されます。</span><span class="sxs-lookup"><span data-stu-id="dae35-157">If a backing form exists, and especially if not all the records are shown in the list, a **See more** button should appear at the bottom of the list, so that the user can see the full list.</span></span>
    -   <span data-ttu-id="dae35-158">リストの上には、最大 2 つの重要なフィルターが存在します。</span><span class="sxs-lookup"><span data-stu-id="dae35-158">Up to two important filters exist above the list.</span></span>
    -   <span data-ttu-id="dae35-159">リストの上には、頻繁に使用される最大で 3 つのアクションがあります。</span><span class="sxs-lookup"><span data-stu-id="dae35-159">Up to three frequently used actions exist above the list.</span></span>
-   <span data-ttu-id="dae35-160">**グリッド**</span><span class="sxs-lookup"><span data-stu-id="dae35-160">**Grid**</span></span>
    -   <span data-ttu-id="dae35-161">リストは、興味のある、比較的小規模のデータまでフィルター処理されます。</span><span class="sxs-lookup"><span data-stu-id="dae35-161">Lists are filtered down to an interesting, relatively small set of data.</span></span>
    -   <span data-ttu-id="dae35-162">リストのグリッドには、行ごとに 3 つまでの明細行があります。</span><span class="sxs-lookup"><span data-stu-id="dae35-162">List grids have no more than three lines of data per row.</span></span>
    -   <span data-ttu-id="dae35-163">カード グリッドには 4 つのフィールドしか表示されません (イメージは含まれません)。</span><span class="sxs-lookup"><span data-stu-id="dae35-163">Card grids show no more than four fields (not including an image).</span></span>
    -   <span data-ttu-id="dae35-164">表形式グリッドには、8 つを超えるフィールドが表示されます。</span><span class="sxs-lookup"><span data-stu-id="dae35-164">Tabular grids show no more than eight fields.</span></span>
-   <span data-ttu-id="dae35-165">**フォーム パターン セクション リスト - ダブルのガイドライン**</span><span class="sxs-lookup"><span data-stu-id="dae35-165">**Form Part Section List - Double guidelines**</span></span>
    -   <span data-ttu-id="dae35-166">両方のリストにアクションやフィルターがある場合は、両方のリストには、同じ [フィルターおよびツールバー](filters-toolbar-subpattern.md) サブパターン (積み上げバリアントまたはインライン バリアント) がある必要があります。</span><span class="sxs-lookup"><span data-stu-id="dae35-166">If both lists have actions and/or filters, both list must use the same [Filters and Toolbar](filters-toolbar-subpattern.md) subpattern (either the Stacked variant or the Inline variant).</span></span>

## <a name="examples"></a><span data-ttu-id="dae35-167">例</span><span class="sxs-lookup"><span data-stu-id="dae35-167">Examples</span></span>
### <a name="form-part-section-list"></a><span data-ttu-id="dae35-168">フォーム パート セクション リスト</span><span class="sxs-lookup"><span data-stu-id="dae35-168">Form Part Section List</span></span>

<span data-ttu-id="dae35-169">フォーム: **PurchOrderProcessReceiptsWorkspace** &gt; **PurchOrdersWithDelayedReceiptsPart** (**すべてのワークスペース** &gt; **発注書入庫とフォローアップ**)</span><span class="sxs-lookup"><span data-stu-id="dae35-169">Form: **PurchOrderProcessReceiptsWorkspace** &gt; **PurchOrdersWithDelayedReceiptsPart** (**All workspaces** &gt; **Purchase order receipt and follow-up**)</span></span> 

<span data-ttu-id="dae35-170">[![formPartSectionListExample](./media/formpartsectionlistexample.png)](./media/formpartsectionlistexample.png)</span><span class="sxs-lookup"><span data-stu-id="dae35-170">[![formPartSectionListExample](./media/formpartsectionlistexample.png)](./media/formpartsectionlistexample.png)</span></span>

### <a name="form-part-section-list---double"></a><span data-ttu-id="dae35-171">フォーム パート セクション リスト - ダブル</span><span class="sxs-lookup"><span data-stu-id="dae35-171">Form Part Section List - Double</span></span>

<span data-ttu-id="dae35-172">フォーム: **BudgetTrackingWorkspace** &gt; **BudgetTransactionPart** (**すべてのワークスペース** &gt; **元帳予算および予測**)</span><span class="sxs-lookup"><span data-stu-id="dae35-172">Form: **BudgetTrackingWorkspace** &gt; **BudgetTransactionPart** (**All workspaces** &gt; **Ledger budgets and forecasts**)</span></span> 

<span data-ttu-id="dae35-173">[![formPartSectionListDoubleExample](./media/formpartsectionlistdoubleexample.png)](./media/formpartsectionlistdoubleexample.png)</span><span class="sxs-lookup"><span data-stu-id="dae35-173">[![formPartSectionListDoubleExample](./media/formpartsectionlistdoubleexample.png)](./media/formpartsectionlistdoubleexample.png)</span></span>

## <a name="appendix"></a><span data-ttu-id="dae35-174">付録</span><span class="sxs-lookup"><span data-stu-id="dae35-174">Appendix</span></span>
### <a name="frequently-asked-questions"></a><span data-ttu-id="dae35-175">よく寄せられる質問</span><span class="sxs-lookup"><span data-stu-id="dae35-175">Frequently asked questions</span></span>

<span data-ttu-id="dae35-176">このセクションには、このガイドライン/パターンに関連するよくある質問への回答があります。</span><span class="sxs-lookup"><span data-stu-id="dae35-176">This section will have answers to frequently asked questions that are related to this guideline/pattern.</span></span>

### <a name="open-issues"></a><span data-ttu-id="dae35-177">未処理の問題</span><span class="sxs-lookup"><span data-stu-id="dae35-177">Open issues</span></span>

<span data-ttu-id="dae35-178">None</span><span class="sxs-lookup"><span data-stu-id="dae35-178">None</span></span>
