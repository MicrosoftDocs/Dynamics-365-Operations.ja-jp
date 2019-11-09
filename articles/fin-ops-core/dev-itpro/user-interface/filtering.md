---
title: フィルター処理のオプション
description: このトピックでは、利用可能なフィルター処理オプションについて説明します。
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
ms.custom: 28721
ms.assetid: f5501319-dcaa-4912-9456-97a0ef2c2452
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4d5c5487d3b37aad1547ce7c5661ddfa2d561184
ms.sourcegitcommit: dd960cf07d8be791fd27c7bb72e6baa2d63ccd51
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/14/2019
ms.locfileid: "2578271"
---
# <a name="filtering-options"></a><span data-ttu-id="b248d-103">フィルター処理のオプション</span><span class="sxs-lookup"><span data-stu-id="b248d-103">Filtering options</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b248d-104">このトピックでは、利用可能なフィルター処理オプションについて説明します。</span><span class="sxs-lookup"><span data-stu-id="b248d-104">This topic explains the filtering options that are available.</span></span>

<a name="introduction"></a><span data-ttu-id="b248d-105">はじめに</span><span class="sxs-lookup"><span data-stu-id="b248d-105">Introduction</span></span>
------------

<span data-ttu-id="b248d-106">Microsoft Dynamics AX 2012 には、次のフィルタ処理オプションが用意されています。</span><span class="sxs-lookup"><span data-stu-id="b248d-106">Microsoft Dynamics AX 2012 offers the following filtering options.</span></span>

| <span data-ttu-id="b248d-107">フィルター オプション</span><span class="sxs-lookup"><span data-stu-id="b248d-107">Filter option</span></span>                         | <span data-ttu-id="b248d-108">説明</span><span class="sxs-lookup"><span data-stu-id="b248d-108">Description</span></span>                                                                                                                                                                   |
|---------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b248d-109">グリッド フィルタ</span><span class="sxs-lookup"><span data-stu-id="b248d-109">Filter by grid</span></span>                        | <span data-ttu-id="b248d-110">ユーザーは、グリッド列ヘッダーの下の入力フィールドにフィルター条件を定義します。</span><span class="sxs-lookup"><span data-stu-id="b248d-110">The user defines filter conditions in input fields below the grid column headers.</span></span>                                                                                             |
| <span data-ttu-id="b248d-111">選択フィルタ (フィールド フィルタ)</span><span class="sxs-lookup"><span data-stu-id="b248d-111">Filter by selection (filter by field)</span></span> | <span data-ttu-id="b248d-112">ユーザーはフィールド値を選択し、その値をフィルター条件として使用します。</span><span class="sxs-lookup"><span data-stu-id="b248d-112">The user selects a field value and uses that value as a filter condition.</span></span>                                                                                                     |
| <span data-ttu-id="b248d-113">高度なフィルター</span><span class="sxs-lookup"><span data-stu-id="b248d-113">Advanced filter</span></span>                       | <span data-ttu-id="b248d-114">ユーザーは、高度なフィルタリング オプション (フォームではなく列にフィルターを適用、追加のデータ ソースに参加、複数の列で並べ替えるなど) を含むダイアログ ボックスを開きます。</span><span class="sxs-lookup"><span data-stu-id="b248d-114">The user opens a dialog box that contains advanced filtering options (filter on columns, not on the form; join additional data sources; sort by multiple columns; and so on).</span></span> |

<span data-ttu-id="b248d-115">Finance and Operations は、次のフィルタ処理オプションを提供します。</span><span class="sxs-lookup"><span data-stu-id="b248d-115">Finance and Operations offers the following filtering options.</span></span>

| <span data-ttu-id="b248d-116">フィルター オプション</span><span class="sxs-lookup"><span data-stu-id="b248d-116">Filter option</span></span>         | <span data-ttu-id="b248d-117">説明</span><span class="sxs-lookup"><span data-stu-id="b248d-117">Description</span></span>                                                                                                                                |
|-----------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b248d-118">フィルター ウィンドウ</span><span class="sxs-lookup"><span data-stu-id="b248d-118">Filter Pane</span></span>           | <span data-ttu-id="b248d-119">左からスライドし、対象となるコンテンツに適用できる複数のフィルター基準を含むインライン ウィンドウです。</span><span class="sxs-lookup"><span data-stu-id="b248d-119">An inline pane that slides in from the left, and that contains multiple filter criteria that can be applied to the targeted content.</span></span>       |
| <span data-ttu-id="b248d-120">QuickFilter</span><span class="sxs-lookup"><span data-stu-id="b248d-120">QuickFilter</span></span>           | <span data-ttu-id="b248d-121">フレームワークによって指定されたフィルタリング機構が任意のリストまたはグリッドの上に表示されると、高速で単一列のフィルター処理を提供します。</span><span class="sxs-lookup"><span data-stu-id="b248d-121">A framework-provided filtering mechanism that can appear above any list or grid, and that provides fast single-column filtering.</span></span>           |
| <span data-ttu-id="b248d-122">グリッド列のフィルター処理</span><span class="sxs-lookup"><span data-stu-id="b248d-122">Grid column filtering</span></span> | <span data-ttu-id="b248d-123">ユーザーは、フィルター条件を定義し、グリッド列ヘッダーから開くドロップ ダイアログを使用して、単一列ソートを実行できます。</span><span class="sxs-lookup"><span data-stu-id="b248d-123">The user can define filter conditions and perform single-column sorting by using a drop dialog that is opened from the grid column header.</span></span> |
| <span data-ttu-id="b248d-124">高度なフィルター/並べ替え</span><span class="sxs-lookup"><span data-stu-id="b248d-124">Advanced filter/sort</span></span>  | <span data-ttu-id="b248d-125">たいていの高度なフィルターのシナリオでは、Dynamics AX 2012 から移行された**高度なフィルター**は引き続き使用可能です。</span><span class="sxs-lookup"><span data-stu-id="b248d-125">For most advanced filtering scenarios, the migrated **Advanced filter** form from Dynamics AX 2012 is still available.</span></span>                     |

## <a name="filter-expressions"></a><span data-ttu-id="b248d-126">フィルター式</span><span class="sxs-lookup"><span data-stu-id="b248d-126">Filter expressions</span></span>
<span data-ttu-id="b248d-127">Finance and Operations アプリでのフィルター処理と Dynamics AX 2012 でのフィルター処理の重要な違いの 1 つは、フィルター値が定義されてるときにクエリ記号が使用される方法です (たとえば、「\*」と 0 文字以上を照合させるか、「..」を使用して一致する値の範囲を指定します)。</span><span class="sxs-lookup"><span data-stu-id="b248d-127">One important difference between filtering in Finance and Operations apps and filtering in Dynamics AX 2012 is related to the way that query symbols are used when filter values are defined (for example, "\*" to match 0 or more characters, or ".." to specify a range of values to match).</span></span> <span data-ttu-id="b248d-128">Dynamics AX 2012 では、これらの記号がフィルター処理中にはっきりと表示されます。</span><span class="sxs-lookup"><span data-stu-id="b248d-128">In Dynamics AX 2012, these symbols are highly visible during the filtering experience.</span></span> <span data-ttu-id="b248d-129">たとえば、グリッド オプションによるフィルターについては、ユーザーがフィールドで**含む**演算子を選択した場合、ワイルドカード文字 (\*) を現在の式の各終わりに追加することにより、システムはその演算子を変換します。</span><span class="sxs-lookup"><span data-stu-id="b248d-129">For example, for the filter by grid option, if a user selects the **contains** operator on a field, the system translates that operator by adding wildcard characters (\*) to each end of the current expression.</span></span> <span data-ttu-id="b248d-130">現在のバージョンでは、クエリ記号は選択された演算子によって暗黙的に指定され、ユーザー インターフェイスに挿入されません。</span><span class="sxs-lookup"><span data-stu-id="b248d-130">In the current version, the query symbols are implied by the selected operator and aren't injected into the user interface.</span></span> <span data-ttu-id="b248d-131">これにより、より直観的で簡単なフィルター処理がユーザーに提供されます。</span><span class="sxs-lookup"><span data-stu-id="b248d-131">This makes filtering more intuitive and simpler for users.</span></span> <span data-ttu-id="b248d-132">特定のクエリ記号を使用して追加のフィルター条件を指定するユーザーに、またはより複雑な条件を入力する必要があるユーザーについては、各データ タイプに対して **一致**演算子が提供されます。</span><span class="sxs-lookup"><span data-stu-id="b248d-132">For users who want to specify additional filter conditions by using specific query symbols, or users who must enter more complex conditions, the **matches** operator is provided for each data type.</span></span> <span data-ttu-id="b248d-133">その他のすべての演算子については、クエリ記号はリテラルとして解釈されます。</span><span class="sxs-lookup"><span data-stu-id="b248d-133">For all other operators, the query symbols are interpreted as literals.</span></span> <span data-ttu-id="b248d-134">たとえば、フィルター条件「名が A と一致する」は、名が A の文字で始まるすべてのレコードを検出します。ただし、フィルター条件「名が A\*である」は、名が文字どおり「A\*」に等しいレコードを検出します。</span><span class="sxs-lookup"><span data-stu-id="b248d-134">For example, the filter condition "First name MATCHES A" finds all records where the first name starts with the letter A. However, the filter condition "First Name IS A\*" finds records where the first name is literally equal to "A\*."</span></span> <span data-ttu-id="b248d-135">次のテーブルは、クライアントが Finance and Operations アプリのフィルター演算子と Dynamics AX 2012 クエリ構文の間でどのように変換するかを示しています。</span><span class="sxs-lookup"><span data-stu-id="b248d-135">The following table shows how the client translates between Finance and Operations apps filter operators and Dynamics AX 2012 query syntax.</span></span>

| <span data-ttu-id="b248d-136">フィルター演算子</span><span class="sxs-lookup"><span data-stu-id="b248d-136">Filter operator</span></span>                      | <span data-ttu-id="b248d-137">Finance and Operations アプリのクエリ構文</span><span class="sxs-lookup"><span data-stu-id="b248d-137">Finance and Operations apps query syntax</span></span> |
|--------------------------------------|------------------------------------------|
| <span data-ttu-id="b248d-138">「円」である、または「円」と等しい</span><span class="sxs-lookup"><span data-stu-id="b248d-138">Is “circle” /  Is equal to “circle”</span></span>        | <span data-ttu-id="b248d-139">“circle”</span><span class="sxs-lookup"><span data-stu-id="b248d-139">“circle”</span></span>                                    |
| <span data-ttu-id="b248d-140">「円」ではない、または「円」と等しくない</span><span class="sxs-lookup"><span data-stu-id="b248d-140">Is not “circle” / Is not equal to “circle”</span></span> | <span data-ttu-id="b248d-141">“!circle”</span><span class="sxs-lookup"><span data-stu-id="b248d-141">“!circle”</span></span>                                   |
| <span data-ttu-id="b248d-142">「円」、「四角」、「サークルスクエア」のいずれか</span><span class="sxs-lookup"><span data-stu-id="b248d-142">Is one of “circle”, “square”, “circlesquare”</span></span>     | <span data-ttu-id="b248d-143">“circle,square,circlesquare”</span><span class="sxs-lookup"><span data-stu-id="b248d-143">“circle,square,circlesquare”</span></span>                         |
| <span data-ttu-id="b248d-144">「円」が含まれています。</span><span class="sxs-lookup"><span data-stu-id="b248d-144">Contains “circle”</span></span>                       | <span data-ttu-id="b248d-145">“\*circle\*”</span><span class="sxs-lookup"><span data-stu-id="b248d-145">“\*circle\*”</span></span>                                |
| <span data-ttu-id="b248d-146">「サークル」は含まない</span><span class="sxs-lookup"><span data-stu-id="b248d-146">Does not contain “circle”</span></span>               | <span data-ttu-id="b248d-147">“!\*circle\*”</span><span class="sxs-lookup"><span data-stu-id="b248d-147">“!\*circle\*”</span></span>                               |
| <span data-ttu-id="b248d-148">「サークル」で始まる</span><span class="sxs-lookup"><span data-stu-id="b248d-148">Begins with “circle”</span></span>                    | <span data-ttu-id="b248d-149">“circle\*”</span><span class="sxs-lookup"><span data-stu-id="b248d-149">“circle\*”</span></span>                                  |
| <span data-ttu-id="b248d-150">「円」 の後に/「円」 より大きい</span><span class="sxs-lookup"><span data-stu-id="b248d-150">After “circle” / Greater than “circle”</span></span>     | <span data-ttu-id="b248d-151">“&gt;circle”</span><span class="sxs-lookup"><span data-stu-id="b248d-151">“&gt;circle”</span></span>                                |
| <span data-ttu-id="b248d-152">「円」以上</span><span class="sxs-lookup"><span data-stu-id="b248d-152">Greater than or equal “circle”</span></span>          | <span data-ttu-id="b248d-153">“circle..”</span><span class="sxs-lookup"><span data-stu-id="b248d-153">“circle..”</span></span>                                  |
| <span data-ttu-id="b248d-154">「サークル」の前 / 「サークル」より小さい</span><span class="sxs-lookup"><span data-stu-id="b248d-154">Before “circle” / Less than “circle”</span></span>       | <span data-ttu-id="b248d-155">“&lt;circle”</span><span class="sxs-lookup"><span data-stu-id="b248d-155">“&lt;circle”</span></span>                                |
| <span data-ttu-id="b248d-156">「円」以下</span><span class="sxs-lookup"><span data-stu-id="b248d-156">Less than or equal “circle”</span></span>             | <span data-ttu-id="b248d-157">“..circle”</span><span class="sxs-lookup"><span data-stu-id="b248d-157">“..circle”</span></span>                                  |
| <span data-ttu-id="b248d-158">「四角」と「円」の間</span><span class="sxs-lookup"><span data-stu-id="b248d-158">Between “square” and “circle”</span></span>              | <span data-ttu-id="b248d-159">“square..circle”</span><span class="sxs-lookup"><span data-stu-id="b248d-159">“square..circle”</span></span>                               |

<span data-ttu-id="b248d-160">先行するテンプレートと一致しないクエリ構文は、**一致**演算子として解釈されます。</span><span class="sxs-lookup"><span data-stu-id="b248d-160">Any query syntax that doesn't match the preceding templates is interpreted as the **matches** operator.</span></span>

## <a name="filter-pane"></a><span data-ttu-id="b248d-161">フィルター ウィンドウ</span><span class="sxs-lookup"><span data-stu-id="b248d-161">Filter Pane</span></span>
<span data-ttu-id="b248d-162">フィルタ ウィンドウは、完全なページ一覧をフィルター処理する使いやすいインターフェイスを提供します。</span><span class="sxs-lookup"><span data-stu-id="b248d-162">The Filter Pane provides an easy-to-use interface for filtering full page lists.</span></span> <span data-ttu-id="b248d-163">フィルタ ウィンドウは、フィルター処理するデータがユーザーに表示されるように、画面の左側からスライド インし、ページのコンテンツを右側にプッシュするインライン ウィンドウです。</span><span class="sxs-lookup"><span data-stu-id="b248d-163">The Filter Pane is an inline pane that slides in from the left side of the screen and pushes the page content to the right, so that users can see the data that they want to filter.</span></span> <span data-ttu-id="b248d-164">ユーザーは、ページの左側にあるシステム定義の **フィルターの表示** ボタンをクリックして、このフィルター メカニズムを開きます。</span><span class="sxs-lookup"><span data-stu-id="b248d-164">Users open this filter mechanism by clicking the system-defined **Show filters** button on the left side of the page.</span></span> <span data-ttu-id="b248d-165">開いた後、フィルター ウィンドウは、ユーザーが新しいページに移動するまで、または**フィルターの非表示**ボタンを使用してユーザーがフィルター ウィンドウを閉じるまで、フィルター ウィンドウは表示されたままになります。</span><span class="sxs-lookup"><span data-stu-id="b248d-165">After it has been opened, the Filter Pane remains visible until the user goes to a new page, or until the user closes the Filter Pane by using the **Hide filters** button.</span></span>

### <a name="when-is-the-filter-pane-available"></a><span data-ttu-id="b248d-166">フィルタ ウィンドウはいつ使用可能になりますか ?</span><span class="sxs-lookup"><span data-stu-id="b248d-166">When is the Filter Pane available?</span></span>

<span data-ttu-id="b248d-167">現在、フィルター ウィンドウは、次のフォームを除くすべてのフォームが使用できます。</span><span class="sxs-lookup"><span data-stu-id="b248d-167">Currently, the Filter Pane is available for all forms except the following forms:</span></span>

-   <span data-ttu-id="b248d-168">ドロップ ダイアログ</span><span class="sxs-lookup"><span data-stu-id="b248d-168">Drop dialogs</span></span>
-   <span data-ttu-id="b248d-169">ダイアログ</span><span class="sxs-lookup"><span data-stu-id="b248d-169">Dialogs</span></span>
-   <span data-ttu-id="b248d-170">拡張プレビュー</span><span class="sxs-lookup"><span data-stu-id="b248d-170">Enhanced previews</span></span>
-   <span data-ttu-id="b248d-171">ルックアップ</span><span class="sxs-lookup"><span data-stu-id="b248d-171">Lookups</span></span>
-   <span data-ttu-id="b248d-172">フォーム パーツ</span><span class="sxs-lookup"><span data-stu-id="b248d-172">Form parts</span></span>
-   <span data-ttu-id="b248d-173">パート</span><span class="sxs-lookup"><span data-stu-id="b248d-173">Parts</span></span>
-   <span data-ttu-id="b248d-174">目次フォーム タイプ</span><span class="sxs-lookup"><span data-stu-id="b248d-174">Table of contents form type</span></span>
-   <span data-ttu-id="b248d-175">データ ソースがないフォーム</span><span class="sxs-lookup"><span data-stu-id="b248d-175">Forms that have no data sources</span></span>

<span data-ttu-id="b248d-176">**注記:** 特定のフォームおよびフォーム タイプでのフィルタ ウィンドウの可用性が発展しているので、このリストは変更される可能性があります。</span><span class="sxs-lookup"><span data-stu-id="b248d-176">**Note:** The availability of the Filter Pane on particular forms and form types is evolving, so this list might change.</span></span>

### <a name="what-data-does-the-filter-pane-work-on"></a><span data-ttu-id="b248d-177">どのようなデータにフィルタ ウィンドウは有効か ?</span><span class="sxs-lookup"><span data-stu-id="b248d-177">What data does the Filter Pane work on?</span></span>

<span data-ttu-id="b248d-178">フィルター ウィンドウはページ リスト全体を対象としているため、フォーム上の最初のマスター データ ソースに (内部/外部結合によって) 直接結合されているテーブルとフィールドでのみ動作します。</span><span class="sxs-lookup"><span data-stu-id="b248d-178">Because the Filter Pane is targeted at full page lists, it works only on the tables and fields that are directly joined (by inner/outer joins) to the first master data source on the form.</span></span> <span data-ttu-id="b248d-179">このフィルター処理メカニズムは、セカンダリ コレクションのフィルター処理、または他のルート データ ソースとその直接結合されたデータ ソースのフィルター処理を目的としたものではありません。</span><span class="sxs-lookup"><span data-stu-id="b248d-179">This filtering mechanism isn't intended for filtering on secondary collections, or for filtering on other root data sources and their directly joined data sources.</span></span> <span data-ttu-id="b248d-180">その他のフィルター処理メカニズム (クイック フィルター、グリッド列のフィルター処理など) は、これら他の要件を満たすために使用できます。</span><span class="sxs-lookup"><span data-stu-id="b248d-180">Other filtering mechanisms (QuickFilter, grid column filtering, and so on) are available to meet these other requirements.</span></span>

### <a name="what-fields-are-initially-shown-in-the-filter-pane"></a><span data-ttu-id="b248d-181">どのようなフィールドがフィルタ ウィンドウに最初に表示されますか。</span><span class="sxs-lookup"><span data-stu-id="b248d-181">What fields are initially shown in the Filter Pane?</span></span>

<span data-ttu-id="b248d-182">フィルタ ウィンドウに最初に表示されるフィールドが選択される方法を次に示します。</span><span class="sxs-lookup"><span data-stu-id="b248d-182">Here is how the fields that are initially shown in the Filter Pane are selected:</span></span>

1.  <span data-ttu-id="b248d-183">現在クエリ上に存在するすべての範囲/フィルター (非表示でないフィルター/範囲のみが表示されます) で使用されます。</span><span class="sxs-lookup"><span data-stu-id="b248d-183">All ranges/filters that currently exist on the query (only non-hidden filters/ranges are shown) are used.</span></span>
2.  <span data-ttu-id="b248d-184">範囲フィルターがクエリに現在存在しない場合、1 つ目のマスター データ ソースからのプライマリ インデックスのフィールドが使用されます。</span><span class="sxs-lookup"><span data-stu-id="b248d-184">If no ranges filters currently exist on the query, the fields from the primary index from the first master data source are used.</span></span>
3.  <span data-ttu-id="b248d-185">1 つ目のマスタ データ ソースからのプライマリ インデックスのフィールドがない場合は、1 つ目のマスタ データ ソースで直接定義されている TitleFields が使用されます。</span><span class="sxs-lookup"><span data-stu-id="b248d-185">If there are no fields from the primary index from the first master data source, the TitleFields that are defined directly on the first master data source are used.</span></span>  <span data-ttu-id="b248d-186">TitleFields が定義されていない場合は、既定のフィールドは表示されません。</span><span class="sxs-lookup"><span data-stu-id="b248d-186">If no TitleFields are defined, no default fields are shown.</span></span> <span data-ttu-id="b248d-187">(現在、最初のマスター データ ソースが別のテーブル (たとえばテーブル B) を拡張している場合、テーブル B の TitleField は表示されませんが、今後そのチェックを追加する予定です。)</span><span class="sxs-lookup"><span data-stu-id="b248d-187">(Currently, if the first master data source extends another table (for example, table B), we don't show the TitleFields from table B. However, we plan to add that check in the future.)</span></span>

### <a name="can-i-control-the-default-fields-that-appear-in-the-filter-pane"></a><span data-ttu-id="b248d-188">フィルター ウィンドウに表示される既定のフィールドを制御できますか。</span><span class="sxs-lookup"><span data-stu-id="b248d-188">Can I control the default fields that appear in the Filter Pane?</span></span>

<span data-ttu-id="b248d-189">開発者は、そのフィールドの空のフィルターをクエリに追加することで、特定のフィールドがフィルター ウィンドウに表示されるようにすることができます。</span><span class="sxs-lookup"><span data-stu-id="b248d-189">Developers can make sure that a particular field appears in the Filter Pane by adding an empty filter for that field to the query.</span></span> <span data-ttu-id="b248d-190">例については、フォーム init() にフィルター転記 super() を追加する **FmCustomer** フォームを参照してください。</span><span class="sxs-lookup"><span data-stu-id="b248d-190">For an example, see the **FmCustomer** form, which adds the filters post super() in form init().</span></span> <span data-ttu-id="b248d-191">空のフィールドがフィルター ウィンドウに表示されることを保証するために追加された後、フィルター ウィンドウのフィールドは常にクエリで明示的なものになり、TitleFields や最初のマスター データ ソースのプライマリ インデックスからのフィールドになりません。</span><span class="sxs-lookup"><span data-stu-id="b248d-191">Note that after an empty field has been added to guarantee that it appears in the Filter Pane, the fields in the Filter Pane will always be those that are explicitly on the query, and will never be the TitleFields or fields from the primary index on the first master data source.</span></span>

### <a name="i-dont-want-users-to-be-able-to-filter-on-a-specific-field-or-modify-an-existing-filter-how-do-i-accomplish-this"></a><span data-ttu-id="b248d-192">ユーザーは特定のフィールドのフィルター処理または既存のフィルターを変更できません。</span><span class="sxs-lookup"><span data-stu-id="b248d-192">I don’t want users to be able to filter on a specific field or modify an existing filter.</span></span> <span data-ttu-id="b248d-193">これをどのように完了しますか。</span><span class="sxs-lookup"><span data-stu-id="b248d-193">How do I accomplish this?</span></span>

<span data-ttu-id="b248d-194">開発者は、フィルタのステータスを変更することで、ユーザーが特定のフィールドでフィルタを変更/追加できるかどうかに影響を与える可能性があります。</span><span class="sxs-lookup"><span data-stu-id="b248d-194">Developers can affect whether users can modify/add filters on certain fields by changing the status of the filters.</span></span> <span data-ttu-id="b248d-195">使用可能な値は、次の **RangeStatus** 列挙型です。</span><span class="sxs-lookup"><span data-stu-id="b248d-195">The allowed values are in the **RangeStatus** enum:</span></span>

1.  <span data-ttu-id="b248d-196">**開く (既定)** – ユーザーはこのフィルターを表示および変更できます。</span><span class="sxs-lookup"><span data-stu-id="b248d-196">**Open (default)** – The user can see and modify this filter.</span></span>
2.  <span data-ttu-id="b248d-197">**ロック済** – ユーザーはフィルター値を表示できますが、変更することはできません。</span><span class="sxs-lookup"><span data-stu-id="b248d-197">**Locked** – The user can see the filter value but can't modify it.</span></span> <span data-ttu-id="b248d-198">ユーザーはこの列に別のフィルターを追加することもできません。</span><span class="sxs-lookup"><span data-stu-id="b248d-198">The user also can't add another filter on this column.</span></span>
3.  <span data-ttu-id="b248d-199">**非表示** – ユーザーは、この列にフィルターがあることを確認できません。</span><span class="sxs-lookup"><span data-stu-id="b248d-199">**Hidden** – The user can't see that there is a filter on this column.</span></span> <span data-ttu-id="b248d-200">ユーザーはこの列に別のフィルターを追加することもできません。</span><span class="sxs-lookup"><span data-stu-id="b248d-200">The user also can't add another filter on this column.</span></span>

### <a name="can-i-control-the-fields-that-appear-in-the-add-a-filter-field-list-in-the-filter-pane"></a><span data-ttu-id="b248d-201">フィルター ウィンドウのフィルター フィールド リストの追加に表示されるフィールドを制御できますか。</span><span class="sxs-lookup"><span data-stu-id="b248d-201">Can I control the fields that appear in the Add a filter field list in the Filter Pane?</span></span>

<span data-ttu-id="b248d-202">**フィルター フィールドの追加** リストに表示されるフィールドは、フォームの最初のマスター データ ソースを含むクエリのフィルター設定可能なすべてのフィールドです。</span><span class="sxs-lookup"><span data-stu-id="b248d-202">The fields that appear in the **Add a filter field** list are all the filterable fields from the query that involves the first master data source on the form.</span></span> <span data-ttu-id="b248d-203">したがって、開発者はこのリストに表示されるフィールドを制御することはできません。</span><span class="sxs-lookup"><span data-stu-id="b248d-203">Therefore, developers can't control the fields that appear in this list.</span></span> <span data-ttu-id="b248d-204">通常、予期しないフィールドが表示される場合、またはフィルターを適用するフィールドが見つからない場合、予定しているフィールドは異なるマスター データ ソース (最初のデータ ソースではない) 上にあるか、または子コレクション上のいずれかにあります。</span><span class="sxs-lookup"><span data-stu-id="b248d-204">Usually, if you see unexpected fields or can't find the fields that you want to filter on, the fields that you're expecting are either on a different master data source (not the first) or on a child collection.</span></span>

### <a name="how-is-the-filter-pane-used"></a><span data-ttu-id="b248d-205">フィルタ ウィンドウはどのように使用されますか。</span><span class="sxs-lookup"><span data-stu-id="b248d-205">How is the Filter Pane used?</span></span>

<span data-ttu-id="b248d-206">フィルタ ウィンドウは、単純で簡単に使用できます。</span><span class="sxs-lookup"><span data-stu-id="b248d-206">The Filter Pane is simple and straightforward to use.</span></span> <span data-ttu-id="b248d-207">最初に、各フィルター フィールドに関連付けられているリストで、フィルター演算子を選択します。</span><span class="sxs-lookup"><span data-stu-id="b248d-207">First, select a filtering operator in the list that is associated with each filter field.</span></span> <span data-ttu-id="b248d-208">表示される演算子のセットは、フィールドのデータ型によって異なることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="b248d-208">Note that the set of operators that appears depends on the data type of the field.</span></span> <span data-ttu-id="b248d-209">フィルター条件に適切な値を入力して **適用** をクリックします。</span><span class="sxs-lookup"><span data-stu-id="b248d-209">Then enter an appropriate value for the filter condition, and click **Apply**.</span></span> <span data-ttu-id="b248d-210">フォームは、指定したフィルター基準に基づいて更新されます。</span><span class="sxs-lookup"><span data-stu-id="b248d-210">The form is updated based on the filter criteria that you specified.</span></span>

## <a name="quickfilter"></a><span data-ttu-id="b248d-211">QuickFilter</span><span class="sxs-lookup"><span data-stu-id="b248d-211">QuickFilter</span></span>
<span data-ttu-id="b248d-212">Dynamics AX 2012 では、QuickFilter がリスト ページにのみ自動的に追加されるフレームワーク コントロールでした。</span><span class="sxs-lookup"><span data-stu-id="b248d-212">In Dynamics AX 2012, the QuickFilter was a framework control that was automatically added only to list pages.</span></span> <span data-ttu-id="b248d-213">Finance and Operations アプリでは、QuickFilter はシステム内で任意のグリッドに関連付けることができるモデル化されたコントロールになっています。</span><span class="sxs-lookup"><span data-stu-id="b248d-213">In Finance and Operations apps, the QuickFilter is now a modeled control that can be associated with any grid in the system.</span></span> <span data-ttu-id="b248d-214">ユーザーが入力を開始すると、列セレクター ドロップダウンが表示され、フィルターが適用される列に向かってユーザーがガイドされます。</span><span class="sxs-lookup"><span data-stu-id="b248d-214">As the user starts to type, a column selector drop-down appears to guide the user toward the column that the filter will be applied to.</span></span> <span data-ttu-id="b248d-215">開発者は QuickFilter の既定の列も指定できます。</span><span class="sxs-lookup"><span data-stu-id="b248d-215">The developer can also specify the default column for the QuickFilter.</span></span> <span data-ttu-id="b248d-216">開発者によって列が指定されていない場合は、グリッドにフィルター処理される最初のフィールドが既定の列です。</span><span class="sxs-lookup"><span data-stu-id="b248d-216">If no column is specified by the developer, the default column is the first field that can be filtered in the grid.</span></span> <span data-ttu-id="b248d-217">[![QuickFilter コントロール](./media/3_filter.png)](./media/3_filter.png)</span><span class="sxs-lookup"><span data-stu-id="b248d-217">[![QuickFilter control](./media/3_filter.png)](./media/3_filter.png)</span></span>

### <a name="why-dont-i-have-a-column-selector-in-my-quickfilter"></a><span data-ttu-id="b248d-218">自分の QuickFilter 内に列セレクターがないのはなぜですか。</span><span class="sxs-lookup"><span data-stu-id="b248d-218">Why don't I have a column selector in my QuickFilter?</span></span>

<span data-ttu-id="b248d-219">列セレクターは、グリッドに接続されている QuickFilter にのみ表示されます。</span><span class="sxs-lookup"><span data-stu-id="b248d-219">Column selectors are shown only for QuickFilters that are attached to grids.</span></span> <span data-ttu-id="b248d-220">列の選択が表示されていない場合は、ほとんどの場合は、QuickFilter の **TargetControl** プロパティは空白になります。</span><span class="sxs-lookup"><span data-stu-id="b248d-220">If you don't see a column selector, the most likely reason is that the **TargetControl** property on the QuickFilter is blank.</span></span> <span data-ttu-id="b248d-221">このプロパティは、操作対象のグリッドを指している必要があります。</span><span class="sxs-lookup"><span data-stu-id="b248d-221">This property must point to the grid that it should operate on.</span></span> <span data-ttu-id="b248d-222">**TargetControl** プロパティが正しく設定されていますが、列のセレクターが表示されていない場合、グリッドにフィルター処理可能な列がない可能性があります。</span><span class="sxs-lookup"><span data-stu-id="b248d-222">If the **TargetControl** property is set correctly, but you don't see a column selector, you might not have any filterable columns in your grid.</span></span> <span data-ttu-id="b248d-223">テキスト以外のコントロール (イメージなど) に加えて、データ メソッドにバインドされているコントロールはフィルター処理できません。</span><span class="sxs-lookup"><span data-stu-id="b248d-223">In addition to non-text controls (such as images), controls that are bound to data methods aren't filterable.</span></span>

### <a name="can-i-use-the-quickfilter-to-filter-other-collection-controls-such-as-trees"></a><span data-ttu-id="b248d-224">QuickFilter を使用して他のコレクション コントロール (ツリーなど) をフィルターできますか？</span><span class="sxs-lookup"><span data-stu-id="b248d-224">Can I use the QuickFilter to filter other collection controls (such as trees)?</span></span>

<span data-ttu-id="b248d-225">はい、QuickFilter を使用して他のコレクション コントロールをフィルター処理することができますが、フィルター処理を手動で接続する必要があります。</span><span class="sxs-lookup"><span data-stu-id="b248d-225">Yes, you can use the QuickFilter to filter other collection controls, but you must manually wire up the filtering.</span></span> <span data-ttu-id="b248d-226">一般的な手順を次に示します。</span><span class="sxs-lookup"><span data-stu-id="b248d-226">Here are the general steps:</span></span>

-   <span data-ttu-id="b248d-227">**TargetControl** プロパティを空白のままにします。</span><span class="sxs-lookup"><span data-stu-id="b248d-227">Leave the **TargetControl** property blank.</span></span>
-   <span data-ttu-id="b248d-228">QuickFilter で **applyFilter()** メソッドをオーバーライドします。</span><span class="sxs-lookup"><span data-stu-id="b248d-228">Override the **applyFilter()** method on the QuickFilter.</span></span>
-   <span data-ttu-id="b248d-229">目的のフィルター処理を実行するためメソッド内にコードを記述します。</span><span class="sxs-lookup"><span data-stu-id="b248d-229">Write code in that method to perform the desired filtering.</span></span>

## <a name="grid-column-header-filteringsorting"></a><span data-ttu-id="b248d-230">グリッド列のヘッダーのフィルター処理/並べ替え</span><span class="sxs-lookup"><span data-stu-id="b248d-230">Grid column header filtering/sorting</span></span>
<span data-ttu-id="b248d-231">Finance and Operations アプリでは、グリッド フィルター エクスペリエンスは Microsoft Excel での体験により近く調整されています。</span><span class="sxs-lookup"><span data-stu-id="b248d-231">In Finance and Operations apps, the grid filtering experience is more closely aligned with the experience in Microsoft Excel.</span></span> <span data-ttu-id="b248d-232">ユーザーが列のヘッダーをクリックするとき (フィルター処理できる列の場合) 、ドロップ ダイアログが表示され、ユーザーはそのダイアログを使用して列をフィルター処理できます。</span><span class="sxs-lookup"><span data-stu-id="b248d-232">When the user clicks a column header (for columns that can be filtered), a drop dialog appears, and the user can use it to filter the column.</span></span> <span data-ttu-id="b248d-233">ここでのフィルタリング経験は、フィルター ウィンドウでのフィルタリング経験を模倣します。</span><span class="sxs-lookup"><span data-stu-id="b248d-233">The filtering experience here mimics the filtering experience in the Filter Pane.</span></span> <span data-ttu-id="b248d-234">また、現在選択されている列に基づくグリッドをソートするオプションがあります。</span><span class="sxs-lookup"><span data-stu-id="b248d-234">Additionally, there are options to sort the grid based on the column that is currently selected.</span></span> <span data-ttu-id="b248d-235">[![グリッド フィルタのスクリーン ショット](./media/4_filter.png)](./media/4_filter.png)</span><span class="sxs-lookup"><span data-stu-id="b248d-235">[![Screen shot of grid filtering](./media/4_filter.png)](./media/4_filter.png)</span></span>