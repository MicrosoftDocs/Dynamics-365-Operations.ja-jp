---
title: 簡易リストおよび簡易詳細のフォーム パターン
description: このトピックでは、簡易リストと詳細フォームのパターンについての情報を提供します。 このパターンは、中程度の複雑さのエンティティのデータを維持するために使用されます。
author: jasongre
manager: AnnBe
ms.date: 10/08/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: robinr
ms.search.scope: Operations
ms.custom: 16242
ms.assetid: 4c5ae424-86fe-43f1-8f94-71dfe2edfaa7
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5e32d208398e6ccf4bf525c95fd36844414952dd
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/29/2019
ms.locfileid: "368417"
---
# <a name="simple-list-and-details-form-pattern"></a><span data-ttu-id="27019-104">簡易リストおよび簡易詳細のフォーム パターン</span><span class="sxs-lookup"><span data-stu-id="27019-104">Simple List and Details form pattern</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="27019-105">このトピックでは、簡易リストと詳細フォームのパターンについての情報を提供します。</span><span class="sxs-lookup"><span data-stu-id="27019-105">This topic provides information about the Simple List and Details form pattern.</span></span> <span data-ttu-id="27019-106">このパターンは、中程度の複雑さのエンティティのデータを維持するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="27019-106">This pattern is used to maintain data for entities of medium complexity.</span></span>

<a name="usage"></a><span data-ttu-id="27019-107">用途</span><span class="sxs-lookup"><span data-stu-id="27019-107">Usage</span></span>
-----

<span data-ttu-id="27019-108">簡易リストと詳細 (SL+D) パターンは、中程度の複雑さのエンティティのデータを管理するために使用します。</span><span class="sxs-lookup"><span data-stu-id="27019-108">The Simple List and Details (SL+D) pattern is used to maintain data for entities of medium complexity.</span></span> <span data-ttu-id="27019-109">中間の複雑度であるエンティティは、6 つ以上のフィールドを持つエンティティです。</span><span class="sxs-lookup"><span data-stu-id="27019-109">Entities of medium complexity are those entities that have six or more fields.</span></span> <span data-ttu-id="27019-110">簡易リスト パターンは、フィールドが 6 つ未満の単純なエンティティに使用してください。</span><span class="sxs-lookup"><span data-stu-id="27019-110">The Simple List pattern should be used for simple entities that have fewer than six fields.</span></span> <span data-ttu-id="27019-111">依然として最大 15 フィールドのエンティティが単純なエンティティと見なされている場合、いくつかの例外があります。</span><span class="sxs-lookup"><span data-stu-id="27019-111">There are some exceptions where entities that have up to 15 fields are still considered simple entities.</span></span> <span data-ttu-id="27019-112">簡易リストと詳細パターンは、これらの条件が満たされたときに規定されます。</span><span class="sxs-lookup"><span data-stu-id="27019-112">The Simple List and Details pattern is prescribed when these conditions are met:</span></span>

-   <span data-ttu-id="27019-113">基礎となるデータには 6 つ以上のフィールドがあります。</span><span class="sxs-lookup"><span data-stu-id="27019-113">The underlying data has more than six fields.</span></span>
-   <span data-ttu-id="27019-114">子データのコレクションは 0 から 5 です。</span><span class="sxs-lookup"><span data-stu-id="27019-114">There are between zero and five child data collections.</span></span>

<span data-ttu-id="27019-115">このドキュメントでは、3 つのパターンについて説明します。</span><span class="sxs-lookup"><span data-stu-id="27019-115">Three patterns are described in this document:</span></span>

-   <span data-ttu-id="27019-116">**簡易リストと詳細 – リスト グリッド** – これは基本的な SL + D パターンです。</span><span class="sxs-lookup"><span data-stu-id="27019-116">**Simple List and Details – List Grid** – This is the basic SL+D pattern.</span></span> <span data-ttu-id="27019-117">これは既定で使用されるパターンです。</span><span class="sxs-lookup"><span data-stu-id="27019-117">This is the pattern that should be used by default.</span></span>
-   <span data-ttu-id="27019-118">**簡易リストと詳細 – 表形式のグリッド** – これはフォームの「簡易リスト」部分の中のフィールド数が予想よりも大きい場合に使用する SL + D パターン です (この記事の後半のセクション「パターンの変更」を参照)。</span><span class="sxs-lookup"><span data-stu-id="27019-118">**Simple List and Details – Tabular Grid** – This is the SL+D pattern that should be used if the number of fields in the “simple list” part of the form is larger than expected (see the "Pattern changes" section later in this article).</span></span>
-   <span data-ttu-id="27019-119">**簡易リストと詳細 – ツリー** – これはフォームの「簡易リスト」部分が実際には、ツリーである場合に使用する SL + D パターンです。</span><span class="sxs-lookup"><span data-stu-id="27019-119">**Simple List and Details – Tree** – This is the SL+D pattern that should be used if the “simple list” part of the form is actually a tree.</span></span>

## <a name="wireframe"></a><span data-ttu-id="27019-120">ワイヤーフレーム</span><span class="sxs-lookup"><span data-stu-id="27019-120">Wireframe</span></span>

<span data-ttu-id="27019-121">[![ワイヤーフレーム](./media/simplelistanddetails1-1024x575.png)](./media/simplelistanddetails1.png)</span><span class="sxs-lookup"><span data-stu-id="27019-121">[![Wireframe](./media/simplelistanddetails1-1024x575.png)](./media/simplelistanddetails1.png)</span></span>

## <a name="pattern-changes"></a><span data-ttu-id="27019-122">パターンの変更</span><span class="sxs-lookup"><span data-stu-id="27019-122">Pattern changes</span></span>
<span data-ttu-id="27019-123">Microsoft Dynamics AX 2012 以降に加えられるこのパターンへの主な変更を次に示します。</span><span class="sxs-lookup"><span data-stu-id="27019-123">Here are the main changes to this pattern since Microsoft Dynamics AX 2012:</span></span>

-   <span data-ttu-id="27019-124">上部の ActionPane ストリップ コントロールが標準の ActionPane に変換されました。</span><span class="sxs-lookup"><span data-stu-id="27019-124">The top ActionPane strip control has been converted to a standard ActionPane.</span></span>
-   <span data-ttu-id="27019-125">**新規**、**削除**、および**編集**ボタンは、フレームワークによって提供されます。</span><span class="sxs-lookup"><span data-stu-id="27019-125">**New**, **Delete**, and **Edit** buttons are provided by the framework.</span></span>
-   <span data-ttu-id="27019-126">表示モードが既定で使用されます。</span><span class="sxs-lookup"><span data-stu-id="27019-126">View mode is used by default.</span></span>
-   <span data-ttu-id="27019-127">クイック フィルター コントロールがフォームの「リスト」部分の上に追加されました。</span><span class="sxs-lookup"><span data-stu-id="27019-127">A Quick Filter control has been added above the “list” part of the form.</span></span>
-   <span data-ttu-id="27019-128">可能な限り、フォームの「リスト」部分にリスト形式のグリッドを使用します。</span><span class="sxs-lookup"><span data-stu-id="27019-128">Whenever possible, use the list-style grid for the “list” part of the form.</span></span> <span data-ttu-id="27019-129">これらの条件が満たされた場合など、表形式のグリッドは、いくつかの状況では許容できる選択肢です。</span><span class="sxs-lookup"><span data-stu-id="27019-129">A tabular grid is an acceptable alternative in some situations, such as when these conditions are met:</span></span>
    -   <span data-ttu-id="27019-130">同じタイプの複数のフィールド (たとえば、3 つの日付フィールド) は、リスト形式のグリッドで区別することはできません。</span><span class="sxs-lookup"><span data-stu-id="27019-130">Multiple fields of the same type (for example, three date fields) would not be distinguishable in the list-style grid.</span></span>
    -   <span data-ttu-id="27019-131">ユーザーのタスクは、リスト内の行 (日付の有効日またはルート ステップ番号など) の日付/数字の順序を比較することです。</span><span class="sxs-lookup"><span data-stu-id="27019-131">The user’s task is to compare a sequence of dates/numbers across rows in the list (for example, date effective dates or route step numbers).</span></span>
    -   <span data-ttu-id="27019-132">グリッド内のフィールド数は予想よりも大きくなります (各行がリスト スタイルのグリッドで 3 行以上を占める場合)。</span><span class="sxs-lookup"><span data-stu-id="27019-132">The number of fields in the grid is larger than expected (if each row takes up more than three lines in the list-style grid).</span></span>
-   <span data-ttu-id="27019-133">ヘッダー グループのフィールドは、垂直方向ではなく水平に配置されます。</span><span class="sxs-lookup"><span data-stu-id="27019-133">Fields in the header group are arranged horizontally instead of vertically.</span></span>
-   <span data-ttu-id="27019-134">情報ボックスが許可されます。</span><span class="sxs-lookup"><span data-stu-id="27019-134">FactBoxes are allowed.</span></span>
-   <span data-ttu-id="27019-135">フォーム構造が簡略化されました (BodyGroup コンテナーが削除されました)。</span><span class="sxs-lookup"><span data-stu-id="27019-135">The form structure has been simplified (the BodyGroup container has been removed).</span></span>

## <a name="model"></a><span data-ttu-id="27019-136">モデル</span><span class="sxs-lookup"><span data-stu-id="27019-136">Model</span></span>
### <a name="high-level-structure"></a><span data-ttu-id="27019-137">高レベル構造体</span><span class="sxs-lookup"><span data-stu-id="27019-137">High-level structure</span></span>

- <span data-ttu-id="27019-138">デザイン</span><span class="sxs-lookup"><span data-stu-id="27019-138">Design</span></span>

    - <span data-ttu-id="27019-139">ActionPane</span><span class="sxs-lookup"><span data-stu-id="27019-139">ActionPane</span></span>
    - <span data-ttu-id="27019-140">NavigationList (グループ)</span><span class="sxs-lookup"><span data-stu-id="27019-140">NavigationList (Group)</span></span>

        - <span data-ttu-id="27019-141">クイック フィルター</span><span class="sxs-lookup"><span data-stu-id="27019-141">Quick Filter</span></span>
        - <span data-ttu-id="27019-142">*CustomFilterGroup (グループ) \[オプション\]*</span><span class="sxs-lookup"><span data-stu-id="27019-142">*CustomFilterGroup (Group) \[Optional\]*</span></span>
        - <span data-ttu-id="27019-143">ListStyleGrid (グリッド) | ツリー | TabularGrid (グリッド)</span><span class="sxs-lookup"><span data-stu-id="27019-143">ListStyleGrid (Grid) | Tree | TabularGrid (Grid)</span></span>

    - <span data-ttu-id="27019-144">VerticalSplitter (Group) *\[Tree またはTabularGrid バリアントの場合にのみ使用可能\]*</span><span class="sxs-lookup"><span data-stu-id="27019-144">VerticalSplitter (Group) *\[only allowed for Tree or TabularGrid variants\]*</span></span>
    - <span data-ttu-id="27019-145">DetailsHeader (グループ)</span><span class="sxs-lookup"><span data-stu-id="27019-145">DetailsHeader (Group)</span></span>
    - <span data-ttu-id="27019-146">DetailsTab (タブ)</span><span class="sxs-lookup"><span data-stu-id="27019-146">DetailsTab (Tab)</span></span>

### <a name="core-components"></a><span data-ttu-id="27019-147">コア コンポーネント</span><span class="sxs-lookup"><span data-stu-id="27019-147">Core components</span></span>

1.  <span data-ttu-id="27019-148">**Form.Design** に SimpleListDetails パターンのいずれかを適用します。</span><span class="sxs-lookup"><span data-stu-id="27019-148">Apply one of the SimpleListDetails patterns on **Form.Design**.</span></span>
2.  <span data-ttu-id="27019-149">必要な BP チェックを解決します。</span><span class="sxs-lookup"><span data-stu-id="27019-149">Resolve required BP checks:</span></span>
    1.  <span data-ttu-id="27019-150">テーブルの **Name** プロパティで使用されているラベルと同じように **Design.Caption** を設定します。</span><span class="sxs-lookup"><span data-stu-id="27019-150">Set **Design.Caption** the same as the label that is used on the **Name** property of the table.</span></span>
    2.  <span data-ttu-id="27019-151">**Design.Datasource** を **Grid.Datasource** と同じに設定します。</span><span class="sxs-lookup"><span data-stu-id="27019-151">Set **Design.Datasource** the same as **Grid.Datasource**.</span></span>
    3.  <span data-ttu-id="27019-152">基本データ ソースを **InsertIfEmpty**=**No** に設定します。</span><span class="sxs-lookup"><span data-stu-id="27019-152">Set the primary data source to **InsertIfEmpty**=**No**.</span></span>
    4.  <span data-ttu-id="27019-153">プライマリ **ActionPane.DataSource** を **Grid.Datasource** と同じに設定します。</span><span class="sxs-lookup"><span data-stu-id="27019-153">Set the primary **ActionPane.DataSource** the same as **Grid.Datasource**.</span></span>
    5.  <span data-ttu-id="27019-154">**Grid.Datasource** を基本データ ソースに設定します。</span><span class="sxs-lookup"><span data-stu-id="27019-154">Set **Grid.Datasource** to the primary data source.</span></span>

### <a name="commonly-used-subpatterns"></a><span data-ttu-id="27019-155">一般的に使用されるサブパターン</span><span class="sxs-lookup"><span data-stu-id="27019-155">Commonly used subpatterns</span></span>

-   [<span data-ttu-id="27019-156">フィールドおよびフィールド グループ</span><span class="sxs-lookup"><span data-stu-id="27019-156">Fields and Field Groups</span></span>](fields-field-groups-subpattern.md)
-   [<span data-ttu-id="27019-157">ツールバーおよびリスト</span><span class="sxs-lookup"><span data-stu-id="27019-157">Toolbar and List</span></span>](toolbar-list-subpattern.md)
-   [<span data-ttu-id="27019-158">ツールバーおよびフィールド</span><span class="sxs-lookup"><span data-stu-id="27019-158">Toolbar and Fields</span></span>](toolbar-fields-subpattern.md)
-   [<span data-ttu-id="27019-159">入れ子になった簡易リストおよび詳細</span><span class="sxs-lookup"><span data-stu-id="27019-159">Nested Simple List and Details</span></span>](nested-simple-list-details-subpattern.md)

## <a name="ux-guidelines"></a><span data-ttu-id="27019-160">UX ガイドライン</span><span class="sxs-lookup"><span data-stu-id="27019-160">UX guidelines</span></span>
<span data-ttu-id="27019-161">検証チェックリストには、フォームが UX ガイドラインに準拠しているかどうかを手動で確認する手順が示されています。</span><span class="sxs-lookup"><span data-stu-id="27019-161">The verification checklist shows the steps for manually verifying that the form complies with UX guidelines.</span></span> <span data-ttu-id="27019-162">このチェックリストには、開発環境を通じて自動的に実施されるガイドラインは含まれていません。</span><span class="sxs-lookup"><span data-stu-id="27019-162">This checklist doesn't include any guidelines that will be enforced automatically through the development environment.</span></span> <span data-ttu-id="27019-163">ブラウザーでフォームを開いて、これらの手順を確認します。</span><span class="sxs-lookup"><span data-stu-id="27019-163">Open the form in the browser, and walk through these steps.</span></span> 

<span data-ttu-id="27019-164">**標準フォーム ガイドライン:**</span><span class="sxs-lookup"><span data-stu-id="27019-164">**Standard form guidelines:**</span></span>

-   <span data-ttu-id="27019-165">標準フォーム ガイドラインは、Microsoft Dynamics AX [全般的なガイドライン](general-form-guidelines.md) ドキュメントに統合されました。</span><span class="sxs-lookup"><span data-stu-id="27019-165">Standard form guidelines have been consolidated into the Microsoft Dynamics AX [General Form Guidelines](general-form-guidelines.md) document.</span></span>

<span data-ttu-id="27019-166">**簡易リスト & 詳細 ガイドライン:**</span><span class="sxs-lookup"><span data-stu-id="27019-166">**Simple list & detail guidelines:**</span></span>

-   <span data-ttu-id="27019-167">ページには、エンティティを正確に説明するフォーム キャプションが表示される必要があります。</span><span class="sxs-lookup"><span data-stu-id="27019-167">The page should display a Form Caption that accurately describes the entity.</span></span>
    -   <span data-ttu-id="27019-168">フォーム キャプションは、複数形にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="27019-168">The Form Caption should be in plural form.</span></span>
-   <span data-ttu-id="27019-169">**新規** ボタンまたは **削除** ボタンは重複してはいけません。</span><span class="sxs-lookup"><span data-stu-id="27019-169">There should not be duplicate **New** or **Delete** buttons.</span></span>
-   <span data-ttu-id="27019-170">既定では、クイック フィルターは名前または説明列を使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="27019-170">By default, the Quick Filter should use the name or description column.</span></span>
-   <span data-ttu-id="27019-171">カスタム フィルタのガイドラインは、カスタム フィルタ グループのサブパターン ドキュメントに統合されました。</span><span class="sxs-lookup"><span data-stu-id="27019-171">Guidelines for custom filters have been consolidated into the Custom Filter Group subpattern document.</span></span>
    -   <span data-ttu-id="27019-172">SL&D フォームには、カスタム フィルター フィールドを 2 つ以下にしてください。</span><span class="sxs-lookup"><span data-stu-id="27019-172">There should be no more than two custom filter fields in a SL&D form.</span></span>
-   <span data-ttu-id="27019-173">フォームの左端には、テーブル形式のグリッド、リスト スタイルのグリッド、またはツリー コントロールが必要です。</span><span class="sxs-lookup"><span data-stu-id="27019-173">There should be a tabular grid, a list-style grid, or a tree control on the left edge of the form.</span></span>
    -   <span data-ttu-id="27019-174">リスト スタイル グリッドには、リスト スタイル グリッドの各レコードに 3 行 (行) 以下で表示する必要があります。</span><span class="sxs-lookup"><span data-stu-id="27019-174">List-style grids should display no more than three rows (lines) for each record in the List-style grid.</span></span> <span data-ttu-id="27019-175">通常は IDと説明だけで十分です。</span><span class="sxs-lookup"><span data-stu-id="27019-175">Typically, just the ID and Description are sufficient.</span></span>
    -   <span data-ttu-id="27019-176">2 つのフィールドと 5 つのフィールドの間に左側のリストを使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="27019-176">Between two and five fields should be used for the list on the left.</span></span>
    -   <span data-ttu-id="27019-177">表形式のグリッドは、いくつかの固有の状況で使用できますが、通常お勧めしません。</span><span class="sxs-lookup"><span data-stu-id="27019-177">A tabular grid can be used in some unique situations but isn't generally recommended.</span></span>
        -   <span data-ttu-id="27019-178">表形式のグリッドを使用している場合、編集**不可能**にすることはできません。</span><span class="sxs-lookup"><span data-stu-id="27019-178">If a tabular grid is used, it should **not** be editable.</span></span>
    -   <span data-ttu-id="27019-179">データが存在しないとき、グリッドまたはツリー コントロールは新しいレコードを自動的に追加できません。</span><span class="sxs-lookup"><span data-stu-id="27019-179">When there is no data, the grid or tree control should not automatically add a new record.</span></span>
-   <span data-ttu-id="27019-180">**詳細**セクションがフォームの右側に表示されます :</span><span class="sxs-lookup"><span data-stu-id="27019-180">A **Details** section should be displayed on the right of the form:</span></span>
    -   <span data-ttu-id="27019-181">リスト フィールド (リスト、表形式のグリッド、ツリーのいずれかから) は、ヘッダー グループの最初のフィールドにする必要があります。</span><span class="sxs-lookup"><span data-stu-id="27019-181">The list fields (whether they are from a list, tabular grid, or tree) should be the first fields in Header Group.</span></span> <span data-ttu-id="27019-182">グリッドやツリーに表示される順序と同じ順序で表示されるため、ユーザーはフィールドのラベルを編集して表示できます。</span><span class="sxs-lookup"><span data-stu-id="27019-182">They should appear in the same order that they appear in the grid or tree, so that the user can edit and see the labels of the fields.</span></span>
-   <span data-ttu-id="27019-183">簡易リストと詳細フォームにこれらの要素を含めることは**できません**:</span><span class="sxs-lookup"><span data-stu-id="27019-183">Simple List and Detail forms must **not** have these elements:</span></span>
    -   <span data-ttu-id="27019-184">グループ フィールドへの標準タブ</span><span class="sxs-lookup"><span data-stu-id="27019-184">Standard tabs to group fields</span></span>

## <a name="examples"></a><span data-ttu-id="27019-185">例</span><span class="sxs-lookup"><span data-stu-id="27019-185">Examples</span></span>
### <a name="simple-list-and-details--list-grid"></a><span data-ttu-id="27019-186">簡易リストと詳細 – リスト グリッド</span><span class="sxs-lookup"><span data-stu-id="27019-186">Simple List and Details – List Grid</span></span>

<span data-ttu-id="27019-187">フォーム: **PaymTerm**</span><span class="sxs-lookup"><span data-stu-id="27019-187">Form: **PaymTerm**</span></span> 

<span data-ttu-id="27019-188">[![簡易リストおよび簡易詳細 – リスト グリッドの例](./media/simplelistanddetails2-1024x558.png)](./media/simplelistanddetails2.png)</span><span class="sxs-lookup"><span data-stu-id="27019-188">[![Simple List and Details – List Grid example](./media/simplelistanddetails2-1024x558.png)](./media/simplelistanddetails2.png)</span></span>

### <a name="simple-list-and-details--tabular-grid"></a><span data-ttu-id="27019-189">簡易リストと詳細 – 表形式のグリッド</span><span class="sxs-lookup"><span data-stu-id="27019-189">Simple List and Details – Tabular Grid</span></span>

<span data-ttu-id="27019-190">フォーム: **ExchangeRate**</span><span class="sxs-lookup"><span data-stu-id="27019-190">Form: **ExchangeRate**</span></span> 

<span data-ttu-id="27019-191">[![簡易リストおよび簡易詳細 - 表形式のグリッドの例](./media/simplelistanddetails3-1024x557.png)](./media/simplelistanddetails3.png)</span><span class="sxs-lookup"><span data-stu-id="27019-191">[![Simple List and Details - Tabular Grid example](./media/simplelistanddetails3-1024x557.png)](./media/simplelistanddetails3.png)</span></span>

### <a name="simple-list-and-details--tree"></a><span data-ttu-id="27019-192">簡易リストと詳細 – ツリー</span><span class="sxs-lookup"><span data-stu-id="27019-192">Simple List and Details – Tree</span></span>

<span data-ttu-id="27019-193">フォーム: **FiscalCalendars**</span><span class="sxs-lookup"><span data-stu-id="27019-193">Form: **FiscalCalendars**</span></span> 

<span data-ttu-id="27019-194">[![簡易リストおよび簡易詳細 – 表形式のグリッドの例](./media/simplelistanddetails4-1024x507.png)](./media/simplelistanddetails4.png)</span><span class="sxs-lookup"><span data-stu-id="27019-194">[![Simple List and Details – Tabular Grid example](./media/simplelistanddetails4-1024x507.png)](./media/simplelistanddetails4.png)</span></span>

## <a name="appendix"></a><span data-ttu-id="27019-195">付録</span><span class="sxs-lookup"><span data-stu-id="27019-195">Appendix</span></span>
### <a name="frequently-asked-questions"></a><span data-ttu-id="27019-196">よく寄せられる質問</span><span class="sxs-lookup"><span data-stu-id="27019-196">Frequently asked questions</span></span>

<span data-ttu-id="27019-197">このセクションには、このガイドライン/パターンに関連するよくある質問への回答があります。</span><span class="sxs-lookup"><span data-stu-id="27019-197">This section will have answers to frequently asked questions that are related to this guideline/pattern.</span></span>

-   <span data-ttu-id="27019-198">**ツール バーのアクションにあるアイコンはいつ使うのでしょうか?**</span><span class="sxs-lookup"><span data-stu-id="27019-198">**When do I use icons on actions in the toolbars?**</span></span>
    -   <span data-ttu-id="27019-199">[一般的なフォーム ガイドライン](general-form-guidelines.md) ドキュメントでボタン画像ガイドラインを参照してください。</span><span class="sxs-lookup"><span data-stu-id="27019-199">See the Button Image Guidelines in the [General Form Guidelines](general-form-guidelines.md) document.</span></span>

### <a name="open-issues"></a><span data-ttu-id="27019-200">未処理の問題</span><span class="sxs-lookup"><span data-stu-id="27019-200">Open issues</span></span>

-   <span data-ttu-id="27019-201">**開発者は ListStyleGrid と TabularGrid パターン間をどのように移動できますか。**</span><span class="sxs-lookup"><span data-stu-id="27019-201">**How can a developer move between the ListStyleGrid and the TabularGrid patterns?**</span></span>
    -   <span data-ttu-id="27019-202">現在、開発者は手動でパターン間を移動する必要があります。</span><span class="sxs-lookup"><span data-stu-id="27019-202">Currently, developers must manually move between the patterns.</span></span>
-   <span data-ttu-id="27019-203">**FastTabs のないモデリングを詳細本文内で許可しますか。**</span><span class="sxs-lookup"><span data-stu-id="27019-203">**Are we going to allow modeling without FastTabs in the details body?**</span></span>
    -   <span data-ttu-id="27019-204">詳細本文内でクイック タブが必要ですが、クイック タブが 1 つだけ表示される場合は最終的にクイック タブ ヘッダーを非表示にする予定です。</span><span class="sxs-lookup"><span data-stu-id="27019-204">Although we require FastTabs in the details body, we plan to eventually hide the FastTab header if only one FastTab is visible.</span></span>
-   <span data-ttu-id="27019-205">**利息フォームなどの従来の状況でクイック タブ ルールの例外を許可する方法。**</span><span class="sxs-lookup"><span data-stu-id="27019-205">**How do we allow for exceptions to the FastTab rule for legacy situations such as the Interest form?**</span></span>
    -   <span data-ttu-id="27019-206">可能な限り、SL&Dパターンに合わせてフォームをリファクターします (**利息** フォームが完了したとき)。</span><span class="sxs-lookup"><span data-stu-id="27019-206">Whenever possible, refactor the form to fit the SL&D pattern (as the **Interest** form has done).</span></span> <span data-ttu-id="27019-207">それ以外の場合、カスタム コンテナーを使用します。</span><span class="sxs-lookup"><span data-stu-id="27019-207">Otherwise, use custom containers.</span></span>
-   <span data-ttu-id="27019-208">**UI のフィールドのハイパーリンクを防ぐ方法。**</span><span class="sxs-lookup"><span data-stu-id="27019-208">**How do we prevent hyperlinks on fields in the UI?**</span></span>
    -   <span data-ttu-id="27019-209">一部のフィールドでは、UI でハイパーリンクを防ぐため **IgnoreEDTRelation 設定**=**はい**にできます。</span><span class="sxs-lookup"><span data-stu-id="27019-209">For some fields, you can **set IgnoreEDTRelation**=**Yes** to prevent hyperlinks in the UI.</span></span> <span data-ttu-id="27019-210">(プラットフォーム構成 17 の時点で) いずれにしても、入力コントロールで **EnableFormRef**=**No** を設定してハイパーリンクを無効にできます。</span><span class="sxs-lookup"><span data-stu-id="27019-210">Regardless (as of Platform update 17), you can set **EnableFormRef**=**No** on an input control to disable a hyperlink.</span></span>

### <a name="ax-2012-content"></a><span data-ttu-id="27019-211">AX 2012 コンテンツ</span><span class="sxs-lookup"><span data-stu-id="27019-211">AX 2012 content</span></span>

<span data-ttu-id="27019-212">[![AX 2012 の例](./media/simplelistanddetails5.png)](./media/simplelistanddetails5.png)</span><span class="sxs-lookup"><span data-stu-id="27019-212">[![AX 2012 example](./media/simplelistanddetails5.png)](./media/simplelistanddetails5.png)</span></span>
