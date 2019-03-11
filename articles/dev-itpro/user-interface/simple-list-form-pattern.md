---
title: 簡易リストのフォーム パターン
description: この記事では、簡易リストのフォームのパターンに関する情報を提供します。 このパターンは、単純なエンティティのデータを維持するために使用されます。
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
ms.custom: 16261
ms.assetid: 47f02822-51d5-4db2-8d99-2706548301e5
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 24b1065af3910f79ae6864e95d9175f72ecb2240
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/29/2019
ms.locfileid: "368750"
---
# <a name="simple-list-form-pattern"></a><span data-ttu-id="b1cf0-104">簡易リストのフォーム パターン</span><span class="sxs-lookup"><span data-stu-id="b1cf0-104">Simple List form pattern</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b1cf0-105">この記事では、簡易リストのフォームのパターンに関する情報を提供します。</span><span class="sxs-lookup"><span data-stu-id="b1cf0-105">This article provides information about the Simple List form pattern.</span></span> <span data-ttu-id="b1cf0-106">このパターンは、単純なエンティティのデータを維持するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="b1cf0-106">This pattern is used to maintain data for simple entities.</span></span>

<a name="usage"></a><span data-ttu-id="b1cf0-107">用途</span><span class="sxs-lookup"><span data-stu-id="b1cf0-107">Usage</span></span>
-----

<span data-ttu-id="b1cf0-108">簡易リスト パターンは簡易エンティティのデータを管理するために使用します。</span><span class="sxs-lookup"><span data-stu-id="b1cf0-108">The Simple List pattern is used to maintain data for simple entities.</span></span> <span data-ttu-id="b1cf0-109">簡易エンティティは、フィールドが 6 つ以下で、親/子関係のないエンティティです。</span><span class="sxs-lookup"><span data-stu-id="b1cf0-109">Simple entities are entities that have six or fewer fields and no parent/child relationships.</span></span> <span data-ttu-id="b1cf0-110">依然として最大 15 フィールドのエンティティが単純なエンティティと見なされている場合、いくつかの例外があります。</span><span class="sxs-lookup"><span data-stu-id="b1cf0-110">There are some exceptions where entities that have up to 15 fields are still considered simple entities.</span></span>

## <a name="wireframe"></a><span data-ttu-id="b1cf0-111">ワイヤーフレーム</span><span class="sxs-lookup"><span data-stu-id="b1cf0-111">Wireframe</span></span>

<span data-ttu-id="b1cf0-112">[![ワイヤーフレーム](./media/simplelist1-1024x578.png)](./media/simplelist1.png)</span><span class="sxs-lookup"><span data-stu-id="b1cf0-112">[![Wireframe](./media/simplelist1-1024x578.png)](./media/simplelist1.png)</span></span>

## <a name="pattern-changes"></a><span data-ttu-id="b1cf0-113">パターンの変更</span><span class="sxs-lookup"><span data-stu-id="b1cf0-113">Pattern changes</span></span>
<span data-ttu-id="b1cf0-114">Microsoft Dynamics AX 2012 以降に加えられるこのパターンへの主な変更を次に示します。</span><span class="sxs-lookup"><span data-stu-id="b1cf0-114">Here are the main changes to this pattern since Microsoft Dynamics AX 2012:</span></span>

-   <span data-ttu-id="b1cf0-115">上部の ActionPane ストリップ コントロールが標準の ActionPane に変換されました。</span><span class="sxs-lookup"><span data-stu-id="b1cf0-115">The top ActionPane strip control has been converted to a standard ActionPane.</span></span>
-   <span data-ttu-id="b1cf0-116">**新規**、**削除**、および**編集**ボタンは、フレームワークによって提供されます。</span><span class="sxs-lookup"><span data-stu-id="b1cf0-116">**New**, **Delete**, and **Edit** buttons are provided by the framework.</span></span>
-   <span data-ttu-id="b1cf0-117">表示モードが既定で使用されます。</span><span class="sxs-lookup"><span data-stu-id="b1cf0-117">View mode is used by default.</span></span>
-   <span data-ttu-id="b1cf0-118">グリッドの上にクイック フィルターが追加されました。</span><span class="sxs-lookup"><span data-stu-id="b1cf0-118">A Quick Filter has been added above the grid.</span></span>
-   <span data-ttu-id="b1cf0-119">フォームが依存関係があるフォームとして使用されているとき、親フォームのレコード コンテキストがフォーム キャプションの上に自動的に表示されます。</span><span class="sxs-lookup"><span data-stu-id="b1cf0-119">When the form is used as a dependent form, the parent form record context is automatically shown above the form caption.</span></span>
    -   <span data-ttu-id="b1cf0-120">依存関係があるフォームを使用するためのページ タイトル グループは、フレームワークを提供するため削除されました。</span><span class="sxs-lookup"><span data-stu-id="b1cf0-120">The page title group for dependent form usage was removed, because it will be provided by the framework.</span></span>
-   <span data-ttu-id="b1cf0-121">このパターンでは、グリッド内での複数選択が可能です。</span><span class="sxs-lookup"><span data-stu-id="b1cf0-121">The pattern allows for multiple selections in the grid.</span></span>

## <a name="model"></a><span data-ttu-id="b1cf0-122">モデル</span><span class="sxs-lookup"><span data-stu-id="b1cf0-122">Model</span></span>
### <a name="high-level-structure"></a><span data-ttu-id="b1cf0-123">高レベル構造体</span><span class="sxs-lookup"><span data-stu-id="b1cf0-123">High-level structure</span></span>

- <span data-ttu-id="b1cf0-124">デザイン</span><span class="sxs-lookup"><span data-stu-id="b1cf0-124">Design</span></span>

    - <span data-ttu-id="b1cf0-125">ActionPane (ActionPane)</span><span class="sxs-lookup"><span data-stu-id="b1cf0-125">ActionPane (ActionPane)</span></span>
    - <span data-ttu-id="b1cf0-126">カスタム フィルター (グループ)</span><span class="sxs-lookup"><span data-stu-id="b1cf0-126">Custom Filter (Group)</span></span>

        - <span data-ttu-id="b1cf0-127">クイック フィルター (クイック フィルター)</span><span class="sxs-lookup"><span data-stu-id="b1cf0-127">Quick Filter (Quick Filter)</span></span>
        - <span data-ttu-id="b1cf0-128">*OtherFilters ($ フィールド)\[0..N\]*</span><span class="sxs-lookup"><span data-stu-id="b1cf0-128">*OtherFilters ($Field) \[0..N\]*</span></span>

    - <span data-ttu-id="b1cf0-129">TabularGrid (グリッド)</span><span class="sxs-lookup"><span data-stu-id="b1cf0-129">TabularGrid (Grid)</span></span>
    - <span data-ttu-id="b1cf0-130">*フッター (グループ) \[オプション\]*</span><span class="sxs-lookup"><span data-stu-id="b1cf0-130">*Footer (Group) \[Optional\]*</span></span>

### <a name="core-components"></a><span data-ttu-id="b1cf0-131">コア コンポーネント</span><span class="sxs-lookup"><span data-stu-id="b1cf0-131">Core components</span></span>

1.  <span data-ttu-id="b1cf0-132">**Form.Design** に SimpleList パターンを適用します。</span><span class="sxs-lookup"><span data-stu-id="b1cf0-132">Apply the SimpleList pattern on **Form.Design**.</span></span>
2.  <span data-ttu-id="b1cf0-133">BP 警告に対処します。</span><span class="sxs-lookup"><span data-stu-id="b1cf0-133">Address BP Warnings:</span></span>
    1.  <span data-ttu-id="b1cf0-134">**Design.Caption** は空ではありません。</span><span class="sxs-lookup"><span data-stu-id="b1cf0-134">**Design.Caption** isn't empty.</span></span>
    2.  <span data-ttu-id="b1cf0-135">**Design.DataSource** は空ではありません。</span><span class="sxs-lookup"><span data-stu-id="b1cf0-135">**Design.DataSource** isn't empty.</span></span>
    3.  <span data-ttu-id="b1cf0-136">**Grid.Datasource** を設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="b1cf0-136">**Grid.Datasource** must be set.</span></span>
    4.  <span data-ttu-id="b1cf0-137">このフォームは少なくとも 1 つのメニュー項目で参照される必要があります。</span><span class="sxs-lookup"><span data-stu-id="b1cf0-137">The form must be referenced by at least one menu item.</span></span>
    5.  <span data-ttu-id="b1cf0-138">**Design.Datasource** は **Grid.Datasource** と同じに設定されます。</span><span class="sxs-lookup"><span data-stu-id="b1cf0-138">**Design.Datasource** is set the same as **Grid.Datasource**.</span></span>
    6.  <span data-ttu-id="b1cf0-139">プライマリ データ ソースのテーブルの主キー フィールドには、**IgnoreEDTRelation**=**はい** が含まれています。</span><span class="sxs-lookup"><span data-stu-id="b1cf0-139">The primary key field of the primary data source’s table has **IgnoreEDTRelation**=**Yes**.</span></span>
    7.  <span data-ttu-id="b1cf0-140">グリッドには 15 個以上のフィールドが含めることはできません。</span><span class="sxs-lookup"><span data-stu-id="b1cf0-140">The grid must not contain more than 15 fields.</span></span>

### <a name="commonly-used-subpatterns"></a><span data-ttu-id="b1cf0-141">一般的に使用されるサブパターン</span><span class="sxs-lookup"><span data-stu-id="b1cf0-141">Commonly used subpatterns</span></span>

-   [<span data-ttu-id="b1cf0-142">カスタム フィルター グループ</span><span class="sxs-lookup"><span data-stu-id="b1cf0-142">Custom Filter Group</span></span>](custom-filter-group-subpattern.md)

## <a name="ux-guidelines"></a><span data-ttu-id="b1cf0-143">UX ガイドライン</span><span class="sxs-lookup"><span data-stu-id="b1cf0-143">UX guidelines</span></span>
<span data-ttu-id="b1cf0-144">検証チェックリストには、フォームが UX ガイドラインに準拠しているかどうかを手動で確認する手順が示されています。</span><span class="sxs-lookup"><span data-stu-id="b1cf0-144">The verification checklist shows the steps for manually verifying that the form complies with UX guidelines.</span></span> <span data-ttu-id="b1cf0-145">このチェックリストには、開発環境を通じて自動的に実施されるガイドラインは含まれていません。</span><span class="sxs-lookup"><span data-stu-id="b1cf0-145">This checklist doesn't include any guidelines that will be enforced automatically through the development environment.</span></span> <span data-ttu-id="b1cf0-146">ブラウザーでフォームを開いて、これらの手順を確認します。</span><span class="sxs-lookup"><span data-stu-id="b1cf0-146">Open the form in the browser, and walk through these steps.</span></span> 

<span data-ttu-id="b1cf0-147">**標準フォーム ガイドライン:**</span><span class="sxs-lookup"><span data-stu-id="b1cf0-147">**Standard form guidelines:**</span></span>

-   <span data-ttu-id="b1cf0-148">標準フォーム ガイドラインは、Microsoft Dynamics AX [全般的なガイドライン](general-form-guidelines.md) ドキュメントに統合されました。</span><span class="sxs-lookup"><span data-stu-id="b1cf0-148">Standard form guidelines have been consolidated into the Microsoft Dynamics AX [General Form Guidelines](general-form-guidelines.md) document.</span></span>

<span data-ttu-id="b1cf0-149">**簡易リスト ガイドライン:**</span><span class="sxs-lookup"><span data-stu-id="b1cf0-149">**Simple list guidelines:**</span></span>

-   <span data-ttu-id="b1cf0-150">既定では、クイック フィルターは名前または説明列を使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="b1cf0-150">By default, the Quick Filter should use the name or description column.</span></span>
-   <span data-ttu-id="b1cf0-151">リストには最大 15 の列を表示できます。</span><span class="sxs-lookup"><span data-stu-id="b1cf0-151">The list can display up to 15 columns.</span></span>

    <span data-ttu-id="b1cf0-152">**注記:** このガイドラインは AX 2012 から緩和されています。</span><span class="sxs-lookup"><span data-stu-id="b1cf0-152">**Note:** This guideline has been relaxed from AX 2012.</span></span>

-   <span data-ttu-id="b1cf0-153">**新規** ボタンまたは **削除** ボタンは重複してはいけません。</span><span class="sxs-lookup"><span data-stu-id="b1cf0-153">There should not be any duplicate **New** or **Delete** buttons.</span></span>
-   <span data-ttu-id="b1cf0-154">ページ タイトルは、複数フォームの形式にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="b1cf0-154">The page title should be in a plural form.</span></span>
-   <span data-ttu-id="b1cf0-155">データが存在しないとき、グリッドは新しいレコードを自動的に追加できません。</span><span class="sxs-lookup"><span data-stu-id="b1cf0-155">When there is no data, the grid should not automatically add a new record.</span></span>

## <a name="examples"></a><span data-ttu-id="b1cf0-156">例</span><span class="sxs-lookup"><span data-stu-id="b1cf0-156">Examples</span></span>
<span data-ttu-id="b1cf0-157">フォーム: **CustGroup**</span><span class="sxs-lookup"><span data-stu-id="b1cf0-157">Form: **CustGroup**</span></span> 

<span data-ttu-id="b1cf0-158">[![簡易リストの例](./media/simplelist2-1024x524.png)](./media/simplelist2.png)</span><span class="sxs-lookup"><span data-stu-id="b1cf0-158">[![Simple List example](./media/simplelist2-1024x524.png)](./media/simplelist2.png)</span></span> 

<span data-ttu-id="b1cf0-159">**注記:** 将来のクライアントの成果物では、グリッド線を右端と下端に延長する予定です。</span><span class="sxs-lookup"><span data-stu-id="b1cf0-159">**Note:** We plan to extend the grid lines to the right and bottom edges in a future client deliverable.</span></span>

## <a name="appendix"></a><span data-ttu-id="b1cf0-160">付録</span><span class="sxs-lookup"><span data-stu-id="b1cf0-160">Appendix</span></span>
### <a name="frequently-asked-questions"></a><span data-ttu-id="b1cf0-161">よく寄せられる質問</span><span class="sxs-lookup"><span data-stu-id="b1cf0-161">Frequently asked questions</span></span>

<span data-ttu-id="b1cf0-162">このセクションには、このガイドライン/パターンに関連するよくある質問への回答があります。</span><span class="sxs-lookup"><span data-stu-id="b1cf0-162">This section will have answers to frequently asked questions that are related to this guideline/pattern.</span></span>

### <a name="open-issues"></a><span data-ttu-id="b1cf0-163">未処理の問題</span><span class="sxs-lookup"><span data-stu-id="b1cf0-163">Open issues</span></span>

<span data-ttu-id="b1cf0-164">この時点ではありません。</span><span class="sxs-lookup"><span data-stu-id="b1cf0-164">None at this time.</span></span>

### <a name="ax-2012-content"></a><span data-ttu-id="b1cf0-165">AX 2012 コンテンツ</span><span class="sxs-lookup"><span data-stu-id="b1cf0-165">AX 2012 content</span></span>

<span data-ttu-id="b1cf0-166">[![AX 2012 の例](./media/simplelist3.png)](./media/simplelist3.png)</span><span class="sxs-lookup"><span data-stu-id="b1cf0-166">[![AX 2012 example](./media/simplelist3.png)](./media/simplelist3.png)</span></span>
