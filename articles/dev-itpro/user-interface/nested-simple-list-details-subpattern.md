---
title: 入れ子になった簡易リストおよび簡易詳細のサブパターン
description: この記事では、ネストされた簡易リストと詳細 (NSL + D) サブパターンについての情報を提供します。 このサブパターンは、子エンティティが別のフォーム タイプ内に存在するとき、セカンダリ エンティティ、すなわち、その子エンティティに関する情報を表示するために使用されます。
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
ms.custom: 14741
ms.assetid: f71aa535-8480-4ed8-b0c9-404f3e6285dd
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8275d834f2620a5ed3bd7856dae2c7781183f7cc
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/15/2019
ms.locfileid: "1573154"
---
# <a name="nested-simple-list-and-details-subpattern"></a><span data-ttu-id="ee77b-104">入れ子になった簡易リストおよび簡易詳細のサブパターン</span><span class="sxs-lookup"><span data-stu-id="ee77b-104">Nested Simple List and Details subpattern</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ee77b-105">この記事では、ネストされた簡易リストと詳細 (NSL + D) サブパターンについての情報を提供します。</span><span class="sxs-lookup"><span data-stu-id="ee77b-105">This article provides information about the Nested Simple List and Details (NSL+D) subpattern.</span></span> <span data-ttu-id="ee77b-106">このサブパターンは、子エンティティが別のフォーム タイプ内に存在するとき、セカンダリ エンティティ、すなわち、その子エンティティに関する情報を表示するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="ee77b-106">This subpattern is used to display information about a secondary or child entity when that child entity is presented within another form type.</span></span>

<a name="usage"></a><span data-ttu-id="ee77b-107">用途</span><span class="sxs-lookup"><span data-stu-id="ee77b-107">Usage</span></span>
-----

<span data-ttu-id="ee77b-108">この記事では、ネストされた簡易リストと詳細 (NSL + D) サブパターンという名前の簡易リストと詳細 (SL + D) パターンの変形について説明します。</span><span class="sxs-lookup"><span data-stu-id="ee77b-108">This article describes a variant of the Simple List and Details (SL+D) pattern that is named the Nested Simple List and Details (NSL+D) subpattern.</span></span> <span data-ttu-id="ee77b-109">SL&D フォーム パターンは、フォーム上の主エンティティに関する情報の表示に使用されます。一方、NSL + D サブパターンは、別のフォーム タイプ内にその子エンティティが表示される場合、セカンダリ エンティティまたは子エンティティに関する情報の表示に使用されます。</span><span class="sxs-lookup"><span data-stu-id="ee77b-109">Whereas the SL&D form pattern is used to display information about the primary entity on the form, the NSL+D subpattern is used to display information about a secondary or child entity when that child entity is presented within another form type.</span></span> <span data-ttu-id="ee77b-110">子エンティティに関連する情報は、グリッド (10 以上のフィールド) には多すぎるが、子エンティティ自体のフォームには足りない量である必要があります。</span><span class="sxs-lookup"><span data-stu-id="ee77b-110">The amount of information that is related to the child entity should be too much for a grid (10 or more fields) but not enough for the child entity to deserve its own form.</span></span> <span data-ttu-id="ee77b-111">NSL+D サブパターンは、SL+D フォーム パターンを少し異なります。</span><span class="sxs-lookup"><span data-stu-id="ee77b-111">The NSL+D subpattern has a few differences from the SL+D form pattern:</span></span>

-   <span data-ttu-id="ee77b-112">別の NSL+D サブパターン内では NSL+D サブパターンを入れ子にしない場合があります。</span><span class="sxs-lookup"><span data-stu-id="ee77b-112">You may not nest an NSL+D subpattern within another NSL+D subpattern.</span></span>
-   <span data-ttu-id="ee77b-113">NSL + D サブパターンは、コンテキスト アクションのツール バーを使用します。</span><span class="sxs-lookup"><span data-stu-id="ee77b-113">The NSL+D subpattern uses a Toolbar for contextual actions.</span></span>
-   <span data-ttu-id="ee77b-114">NSL+D サブパターンの詳細部分は、SL+D パターンよりも単純です。</span><span class="sxs-lookup"><span data-stu-id="ee77b-114">The details portion of the NSL+D subpattern is simpler than the SL+D pattern.</span></span> <span data-ttu-id="ee77b-115">NSL + D サブパターンはグループのみ使用しますが、SL+D パターンはコンテンツをクイック タブに整理します。</span><span class="sxs-lookup"><span data-stu-id="ee77b-115">The NSL+D subpattern uses only groups, whereas the SL+D pattern organizes content into FastTabs.</span></span>

## <a name="wireframe"></a><span data-ttu-id="ee77b-116">ワイヤーフレーム</span><span class="sxs-lookup"><span data-stu-id="ee77b-116">Wireframe</span></span>
<span data-ttu-id="ee77b-117">[![patternNSLD](./media/patternnsld.png)](./media/patternnsld.png)[](./media/nestedsimplelistanddetails1.png)</span><span class="sxs-lookup"><span data-stu-id="ee77b-117">[![patternNSLD](./media/patternnsld.png)](./media/patternnsld.png)[](./media/nestedsimplelistanddetails1.png)</span></span>

## <a name="pattern-changes-for-microsoft-dynamics-365-for-finance-and-operations"></a><span data-ttu-id="ee77b-118">Microsoft Dynamics 365 for Finance and Operations 用のパターンの変更</span><span class="sxs-lookup"><span data-stu-id="ee77b-118">Pattern changes for Microsoft Dynamics 365 for Finance and Operations</span></span>
<span data-ttu-id="ee77b-119">Microsoft Dynamics AX 2012 以降に加えられるこのパターンへの主な変更を次に示します。</span><span class="sxs-lookup"><span data-stu-id="ee77b-119">Here are the main changes to this pattern since Microsoft Dynamics AX 2012:</span></span>

-   <span data-ttu-id="ee77b-120">このパターンは新しいものです。</span><span class="sxs-lookup"><span data-stu-id="ee77b-120">This pattern is new.</span></span> <span data-ttu-id="ee77b-121">SL+D パターンへのパターンの変更は、[簡易リストと詳細](simple-list-details-form-pattern.md)パターン ドキュメントで確認できます。</span><span class="sxs-lookup"><span data-stu-id="ee77b-121">Any pattern changes to the SL+D pattern can be found in the [Simple List and Details](simple-list-details-form-pattern.md) pattern document.</span></span>

## <a name="model"></a><span data-ttu-id="ee77b-122">モデル</span><span class="sxs-lookup"><span data-stu-id="ee77b-122">Model</span></span>
### <a name="high-level-structure"></a><span data-ttu-id="ee77b-123">高レベル構造体</span><span class="sxs-lookup"><span data-stu-id="ee77b-123">High-level structure</span></span>

- <span data-ttu-id="ee77b-124">&lt;コンテナ&gt;</span><span class="sxs-lookup"><span data-stu-id="ee77b-124">&lt;Container&gt;</span></span>

    - <span data-ttu-id="ee77b-125">ActionPane (ActionPane Style=Strip)</span><span class="sxs-lookup"><span data-stu-id="ee77b-125">ActionPane (ActionPane Style=Strip)</span></span>
    - <span data-ttu-id="ee77b-126">ContainerBody (グループの列 = 2)</span><span class="sxs-lookup"><span data-stu-id="ee77b-126">ContainerBody (Group Columns=2)</span></span>

        - <span data-ttu-id="ee77b-127">ListContainer (グループ)</span><span class="sxs-lookup"><span data-stu-id="ee77b-127">ListContainer (Group)</span></span>

            - <span data-ttu-id="ee77b-128">グリッド | ツリー | ListView</span><span class="sxs-lookup"><span data-stu-id="ee77b-128">Grid | Tree | ListView</span></span>

        - <span data-ttu-id="ee77b-129">DetailsContainer (グループ)</span><span class="sxs-lookup"><span data-stu-id="ee77b-129">DetailsContainer (Group)</span></span>

            - <span data-ttu-id="ee77b-130">DetailsHeader (グループ)</span><span class="sxs-lookup"><span data-stu-id="ee77b-130">DetailsHeader (Group)</span></span>
            - <span data-ttu-id="ee77b-131">*DetailsGroup (グループ) \[オプション\]*</span><span class="sxs-lookup"><span data-stu-id="ee77b-131">*DetailsGroup (Group) \[Optional\]*</span></span>

### <a name="core-components"></a><span data-ttu-id="ee77b-132">コア コンポーネント</span><span class="sxs-lookup"><span data-stu-id="ee77b-132">Core components</span></span>

1.  <span data-ttu-id="ee77b-133">NestedSimpleListDetails サブパターンをコンテナー コントロールに適用します。</span><span class="sxs-lookup"><span data-stu-id="ee77b-133">Apply the NestedSimpleListDetails subpattern to the container control.</span></span>
2.  <span data-ttu-id="ee77b-134">必要な BP チェックを解決します。</span><span class="sxs-lookup"><span data-stu-id="ee77b-134">Resolve the required BP checks:</span></span>
    1.  <span data-ttu-id="ee77b-135">**Grid.Datasource=&lt;セカンダリ データ ソース&gt;** に設定します。</span><span class="sxs-lookup"><span data-stu-id="ee77b-135">Set **Grid.Datasource=&lt;secondary data source&gt;**.</span></span>
    2.  <span data-ttu-id="ee77b-136">グリッド データ ソース **InsertIfEmpty**=**No** を設定します。</span><span class="sxs-lookup"><span data-stu-id="ee77b-136">Set grid data source **InsertIfEmpty**=**No**.</span></span>
    3.  <span data-ttu-id="ee77b-137">**ActionPane.DataSource**=**&lt;グリッドと同じデータ ソース&gt;** を設定します。</span><span class="sxs-lookup"><span data-stu-id="ee77b-137">Set **ActionPane.DataSource**=**&lt;same data source as grid&gt;**.</span></span>
    4.  <span data-ttu-id="ee77b-138">ツール バー コマンドの追加プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="ee77b-138">Set Toolbar Command Add properties.</span></span>
    5.  <span data-ttu-id="ee77b-139">ツール バー コマンドの削除プロパティを設定します。</span><span class="sxs-lookup"><span data-stu-id="ee77b-139">Set Toolbar Command Remove properties.</span></span>
    6.  <span data-ttu-id="ee77b-140">グリッドのデータ ソースが読み取り専用の場合は、ツールバーに**追加**/**削除**ボタンがあることを確認します。</span><span class="sxs-lookup"><span data-stu-id="ee77b-140">If the grid data source is read-only, make sure that there are no **Add**/**Remove** buttons on the Toolbar.</span></span>

## <a name="ux-guidelines"></a><span data-ttu-id="ee77b-141">UX ガイドライン</span><span class="sxs-lookup"><span data-stu-id="ee77b-141">UX guidelines</span></span>
<span data-ttu-id="ee77b-142">検証チェックリストには、フォームが UX ガイドラインに準拠しているかどうかを手動で確認する手順が示されています。</span><span class="sxs-lookup"><span data-stu-id="ee77b-142">The verification checklist shows the steps for manually verifying that the form complies with the UX guidelines.</span></span> <span data-ttu-id="ee77b-143">このチェックリストには、開発環境を通じて自動的に実施されるガイドラインは含まれていません。</span><span class="sxs-lookup"><span data-stu-id="ee77b-143">This checklist doesn't include any guidelines that will be enforced automatically through the development environment.</span></span> <span data-ttu-id="ee77b-144">ブラウザーでフォームを開いて、これらの手順を確認します。</span><span class="sxs-lookup"><span data-stu-id="ee77b-144">Open the form in a browser, and walk through these steps.</span></span>

<span data-ttu-id="ee77b-145">**標準フォーム ガイドライン**</span><span class="sxs-lookup"><span data-stu-id="ee77b-145">**Standard form guidelines**</span></span>

-   <span data-ttu-id="ee77b-146">標準フォーム ガイドラインは、[全般的なガイドライン](general-form-guidelines.md) ドキュメントに統合されました。</span><span class="sxs-lookup"><span data-stu-id="ee77b-146">Standard form guidelines have been consolidated into the [General Form Guidelines](general-form-guidelines.md) document.</span></span>

<span data-ttu-id="ee77b-147">**入れ子になった簡易リスト & 詳細ガイドライン**</span><span class="sxs-lookup"><span data-stu-id="ee77b-147">**Nested simple list & detail guidelines**</span></span>

-   <span data-ttu-id="ee77b-148">**新規** ボタンまたは **削除** ボタンは重複してはいけません。</span><span class="sxs-lookup"><span data-stu-id="ee77b-148">There should not be duplicate **New** or **Delete** buttons.</span></span>
-   <span data-ttu-id="ee77b-149">**グリッド**は、パターンのリスト部分に使用します。</span><span class="sxs-lookup"><span data-stu-id="ee77b-149">If a **grid** is used for the list portion of the pattern:</span></span>
    -   <span data-ttu-id="ee77b-150">グリッドは、**list-style** グリッドにする必要があります。</span><span class="sxs-lookup"><span data-stu-id="ee77b-150">The grid should be a **list-style** grid.</span></span>
    -   <span data-ttu-id="ee77b-151">リスト スタイル グリッドでは、リスト スタイル グリッドの各レコードに 3 行 (行) まで表示します。</span><span class="sxs-lookup"><span data-stu-id="ee77b-151">List-style grids should display no more than three rows (lines) for each record in the List style grid.</span></span> <span data-ttu-id="ee77b-152">通常は IDと説明だけで十分です。</span><span class="sxs-lookup"><span data-stu-id="ee77b-152">Typically, just the ID and Description are sufficient.</span></span>
    -   <span data-ttu-id="ee77b-153">データが存在しないとき、グリッド コントロールは新しいレコードを自動的に追加できません。</span><span class="sxs-lookup"><span data-stu-id="ee77b-153">When there is no data, the grid control should not automatically add a new record.</span></span>
-   <span data-ttu-id="ee77b-154">**詳細**セクションがコンテナー本体の右側に表示されます:</span><span class="sxs-lookup"><span data-stu-id="ee77b-154">A **details** section that is displayed on the right of the Container Body:</span></span>
    -   <span data-ttu-id="ee77b-155">グリッドに表示されているのと同じ順序で、グリッドの列を Details Header Group の最初のフィールドとして表示します。</span><span class="sxs-lookup"><span data-stu-id="ee77b-155">Display the grid columns as the first fields in the Details Header Group, in the same order that they are displayed in the grid.</span></span>
    -   <span data-ttu-id="ee77b-156">レコードが追加されるとき、フォーカスは詳細セクションの最初のフィールドに移動するはずです。</span><span class="sxs-lookup"><span data-stu-id="ee77b-156">When a record is added, focus should go to the first field in the details section.</span></span>

## <a name="examples"></a><span data-ttu-id="ee77b-157">例</span><span class="sxs-lookup"><span data-stu-id="ee77b-157">Examples</span></span>
<span data-ttu-id="ee77b-158">フォーム: **HcmJob** (**TaskTabPage**) [![入れ子になった簡易リストおよび詳細サブパターンの例](./media/nestedsimplelistanddetails2.png)](./media/nestedsimplelistanddetails2.png)</span><span class="sxs-lookup"><span data-stu-id="ee77b-158">Form: **HcmJob** (**TaskTabPage**) [![Nested Simple List and Details sub-pattern example](./media/nestedsimplelistanddetails2.png)](./media/nestedsimplelistanddetails2.png)</span></span>

## <a name="resources"></a><span data-ttu-id="ee77b-159">リソース</span><span class="sxs-lookup"><span data-stu-id="ee77b-159">Resources</span></span>
### <a name="typically-used-by-patterns"></a><span data-ttu-id="ee77b-160">通常、パターンによって使用される</span><span class="sxs-lookup"><span data-stu-id="ee77b-160">Typically used by patterns</span></span>

-   [<span data-ttu-id="ee77b-161">簡易リストと詳細</span><span class="sxs-lookup"><span data-stu-id="ee77b-161">Simple List and Details</span></span>](simple-list-details-form-pattern.md)
-   [<span data-ttu-id="ee77b-162">目次</span><span class="sxs-lookup"><span data-stu-id="ee77b-162">Table of Contents</span></span>](table-of-contents-form-pattern.md)
-   [<span data-ttu-id="ee77b-163">詳細マスター</span><span class="sxs-lookup"><span data-stu-id="ee77b-163">Details Master</span></span>](details-master-form-pattern.md)
-   [<span data-ttu-id="ee77b-164">詳細トランザクション</span><span class="sxs-lookup"><span data-stu-id="ee77b-164">Details Transaction</span></span>](details-transaction-form-pattern.md)

## <a name="appendix"></a><span data-ttu-id="ee77b-165">付録</span><span class="sxs-lookup"><span data-stu-id="ee77b-165">Appendix</span></span>
### <a name="frequently-asked-questions"></a><span data-ttu-id="ee77b-166">よく寄せられる質問</span><span class="sxs-lookup"><span data-stu-id="ee77b-166">Frequently asked questions</span></span>

<span data-ttu-id="ee77b-167">このセクションには、このガイドライン/パターンに関連するよくある質問への回答があります。</span><span class="sxs-lookup"><span data-stu-id="ee77b-167">This section will have answers to frequently asked questions that are related to this guideline/pattern.</span></span>

### <a name="open-issues"></a><span data-ttu-id="ee77b-168">未処理の問題</span><span class="sxs-lookup"><span data-stu-id="ee77b-168">Open issues</span></span>

-   <span data-ttu-id="ee77b-169">**入れ子になったパターンの詳細領域には、クイック タブを配置すべきではありません。フレームワークが確認/適用します。**</span><span class="sxs-lookup"><span data-stu-id="ee77b-169">**The details area of the nested pattern should not have FastTabs. The framework should verify/enforce this.**</span></span>
    -   <span data-ttu-id="ee77b-170">現在のところ、このパターン内ではタブの種類を許可していません。</span><span class="sxs-lookup"><span data-stu-id="ee77b-170">Currently we aren't allowing tabs of any kind inside this pattern.</span></span>

### <a name="ax-2012-content"></a><span data-ttu-id="ee77b-171">AX 2012 コンテンツ</span><span class="sxs-lookup"><span data-stu-id="ee77b-171">AX 2012 content</span></span>

<span data-ttu-id="ee77b-172">[![AX 2012 の例](./media/nestedsimplelistanddetails3.png)](./media/nestedsimplelistanddetails3.png)</span><span class="sxs-lookup"><span data-stu-id="ee77b-172">[![AX 2012 example](./media/nestedsimplelistanddetails3.png)](./media/nestedsimplelistanddetails3.png)</span></span>
