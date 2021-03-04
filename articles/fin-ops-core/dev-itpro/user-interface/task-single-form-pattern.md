---
title: タスク シングルのフォーム パターン
description: この記事では、タスク シングル フォームのパターンに関する情報を提供します。
author: jasongre
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.custom: 14634
ms.assetid: 38cb1058-ed69-4ffa-9bfd-4b65cc8d2a49
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6c1038e9ba27af93087d3fee8feaa764e08c8bcf
ms.sourcegitcommit: 5192cfaedfd861faea63d8954d7bcc500608a225
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 01/30/2021
ms.locfileid: "5094193"
---
# <a name="task-single-form-pattern"></a><span data-ttu-id="c1f0f-103">タスク シングルのフォーム パターン</span><span class="sxs-lookup"><span data-stu-id="c1f0f-103">Task Single form pattern</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c1f0f-104">この記事では、タスク シングル フォームのパターンに関する情報を提供します。</span><span class="sxs-lookup"><span data-stu-id="c1f0f-104">This article provides information about the Task Single form pattern.</span></span> <span data-ttu-id="c1f0f-105">このパターンは、ユーザーが複数のレコードを持つ単一のデータソースから発生したと認識するデータを表示するために以前は使用されていました。</span><span class="sxs-lookup"><span data-stu-id="c1f0f-105">This pattern was previously used to present data that users would perceive as originating from a single data source that had multiple records.</span></span>

<a name="usage"></a><span data-ttu-id="c1f0f-106">用途</span><span class="sxs-lookup"><span data-stu-id="c1f0f-106">Usage</span></span>
-----

<span data-ttu-id="c1f0f-107">このタイプのフォームは、データが複数のレコードを持つ単一のデータ ソースから発生したとユーザーが認識することを表す場合に使用されました。</span><span class="sxs-lookup"><span data-stu-id="c1f0f-107">This type of form was used when you wanted to present data that users will perceive as originating from a single data source with multiple records.</span></span> <span data-ttu-id="c1f0f-108">新しいフォームの推奨パターンではありません。</span><span class="sxs-lookup"><span data-stu-id="c1f0f-108">This isn't a recommended pattern for new forms.</span></span> <span data-ttu-id="c1f0f-109">このパターンを使用する新しいフォームを作成する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="c1f0f-109">No new forms should be created that use this pattern.</span></span> <span data-ttu-id="c1f0f-110">このパターンは、レガシー フォームの構造と安定性を提供し、より現代的なフォーム パターンへの移行パスも提供します。</span><span class="sxs-lookup"><span data-stu-id="c1f0f-110">This pattern will provide structure and stability for legacy forms, and will also provide a migration path to more modern form patterns.</span></span>

## <a name="wireframe"></a><span data-ttu-id="c1f0f-111">ワイヤーフレーム</span><span class="sxs-lookup"><span data-stu-id="c1f0f-111">Wireframe</span></span>
<span data-ttu-id="c1f0f-112">[![タスク シングルのフォームのワイヤーフレーム](./media/tasksingle1-1024x577.png)](./media/tasksingle1.png)</span><span class="sxs-lookup"><span data-stu-id="c1f0f-112">[![Wireframe for Task Single form](./media/tasksingle1-1024x577.png)](./media/tasksingle1.png)</span></span>

## <a name="pattern-changes"></a><span data-ttu-id="c1f0f-113">パターンの変更</span><span class="sxs-lookup"><span data-stu-id="c1f0f-113">Pattern changes</span></span>
<span data-ttu-id="c1f0f-114">Microsoft Dynamics AX 2012 以降に加えられるこのパターンへの主な変更を次に示します。</span><span class="sxs-lookup"><span data-stu-id="c1f0f-114">Here are the main changes to this pattern since Microsoft Dynamics AX 2012:</span></span>

-   <span data-ttu-id="c1f0f-115">表示モードでフォームを開きます。</span><span class="sxs-lookup"><span data-stu-id="c1f0f-115">The form opens in view mode.</span></span>
-   <span data-ttu-id="c1f0f-116">コマンドは、ツールバー (アクション ペイン ストライプ) から標準アクション ペインに移動されています。</span><span class="sxs-lookup"><span data-stu-id="c1f0f-116">Commands have been moved to the standard ActionPane from a Toolbar (ActionPane strips).</span></span>
-   <span data-ttu-id="c1f0f-117">最初のタブの **概要** ラベルが **リスト** に変更されました。</span><span class="sxs-lookup"><span data-stu-id="c1f0f-117">The **Overview** label on the first tab has been changed to **List**.</span></span>
-   <span data-ttu-id="c1f0f-118">タブ コンテナーのコンテンツは、応答レイアウトに動的列を使用します。</span><span class="sxs-lookup"><span data-stu-id="c1f0f-118">The content of the tab container uses dynamic columns for a responsive layout.</span></span>

## <a name="model"></a><span data-ttu-id="c1f0f-119">モデル</span><span class="sxs-lookup"><span data-stu-id="c1f0f-119">Model</span></span>
### <a name="high-level-structure"></a><span data-ttu-id="c1f0f-120">高レベル構造体</span><span class="sxs-lookup"><span data-stu-id="c1f0f-120">High-level structure</span></span>

- <span data-ttu-id="c1f0f-121">デザイン</span><span class="sxs-lookup"><span data-stu-id="c1f0f-121">Design</span></span>

    - <span data-ttu-id="c1f0f-122">ActionPane (アクション ウィンドウ)</span><span class="sxs-lookup"><span data-stu-id="c1f0f-122">ActionPane (Action Pane)</span></span>
    - <span data-ttu-id="c1f0f-123">*CustomFilter (グループ) \[オプション\]*</span><span class="sxs-lookup"><span data-stu-id="c1f0f-123">*CustomFilter (Group) \[Optional\]*</span></span>
    - <span data-ttu-id="c1f0f-124">タブ (タブ)</span><span class="sxs-lookup"><span data-stu-id="c1f0f-124">Tab (Tab)</span></span>

        - <span data-ttu-id="c1f0f-125">概要 (TabPage)</span><span class="sxs-lookup"><span data-stu-id="c1f0f-125">Overview (TabPage)</span></span>

            - <span data-ttu-id="c1f0f-126">グリッド (グリッド)</span><span class="sxs-lookup"><span data-stu-id="c1f0f-126">Grid (Grid)</span></span>
            - <span data-ttu-id="c1f0f-127">*RowExtension (グループ) \[オプション\]*</span><span class="sxs-lookup"><span data-stu-id="c1f0f-127">*RowExtension (Group) \[Optional\]*</span></span>

        - <span data-ttu-id="c1f0f-128">一般 (TabPage、0..N を繰り返します)</span><span class="sxs-lookup"><span data-stu-id="c1f0f-128">General (TabPage, repeats 0..N)</span></span>

    - <span data-ttu-id="c1f0f-129">*FooterGroup (グループ) \[オプション\]*</span><span class="sxs-lookup"><span data-stu-id="c1f0f-129">*FooterGroup (Group) \[Optional\]*</span></span>

### <a name="core-components"></a><span data-ttu-id="c1f0f-130">コア コンポーネント</span><span class="sxs-lookup"><span data-stu-id="c1f0f-130">Core components</span></span>

1.  <span data-ttu-id="c1f0f-131">**Form.Design** に TaskSingle パターンを適用します。</span><span class="sxs-lookup"><span data-stu-id="c1f0f-131">Apply the TaskSingle pattern on **Form.Design**.</span></span>
2.  <span data-ttu-id="c1f0f-132">BP 警告に対処します。</span><span class="sxs-lookup"><span data-stu-id="c1f0f-132">Address BP Warnings:</span></span>
    1.  <span data-ttu-id="c1f0f-133">**Design.Caption** は空ではありません。</span><span class="sxs-lookup"><span data-stu-id="c1f0f-133">**Design.Caption** isn't empty.</span></span>
    2.  <span data-ttu-id="c1f0f-134">このフォームは少なくとも 1 つのメニュー項目で参照される必要があります。</span><span class="sxs-lookup"><span data-stu-id="c1f0f-134">The form must be referenced by at least one menu item.</span></span>
    3.  <span data-ttu-id="c1f0f-135">**TabPage.Caption** は空ではありません。</span><span class="sxs-lookup"><span data-stu-id="c1f0f-135">**TabPage.Caption** isn't empty.</span></span>
    4.  <span data-ttu-id="c1f0f-136">**TabPage.DataSource** は空ではありません。</span><span class="sxs-lookup"><span data-stu-id="c1f0f-136">**TabPage.DataSource** isn't empty.</span></span>
    5.  <span data-ttu-id="c1f0f-137">**StaticText.Text** は空ではありません。</span><span class="sxs-lookup"><span data-stu-id="c1f0f-137">**StaticText.Text** isn't empty.</span></span>

### <a name="related-patterns"></a><span data-ttu-id="c1f0f-138">関連するパターン</span><span class="sxs-lookup"><span data-stu-id="c1f0f-138">Related patterns</span></span>

-   [<span data-ttu-id="c1f0f-139">タスク ダブル</span><span class="sxs-lookup"><span data-stu-id="c1f0f-139">Task Double</span></span>](task-double-form-pattern.md)

### <a name="commonly-used-subpatterns"></a><span data-ttu-id="c1f0f-140">一般的に使用されるサブパターン</span><span class="sxs-lookup"><span data-stu-id="c1f0f-140">Commonly used subpatterns</span></span>

-   [<span data-ttu-id="c1f0f-141">カスタム フィルター グループ</span><span class="sxs-lookup"><span data-stu-id="c1f0f-141">Custom Filter Group</span></span>](custom-filter-group-subpattern.md)
-   [<span data-ttu-id="c1f0f-142">フィールドおよびフィールド グループ</span><span class="sxs-lookup"><span data-stu-id="c1f0f-142">Fields and Field Groups</span></span>](fields-field-groups-subpattern.md)
-   [<span data-ttu-id="c1f0f-143">ツールバーおよびリスト</span><span class="sxs-lookup"><span data-stu-id="c1f0f-143">Toolbar and List</span></span>](toolbar-list-subpattern.md)
-   [<span data-ttu-id="c1f0f-144">ツールバーおよびフィールド</span><span class="sxs-lookup"><span data-stu-id="c1f0f-144">Toolbar and Fields</span></span>](toolbar-fields-subpattern.md)

## <a name="ux-guidelines"></a><span data-ttu-id="c1f0f-145">UX ガイドライン</span><span class="sxs-lookup"><span data-stu-id="c1f0f-145">UX guidelines</span></span>
<span data-ttu-id="c1f0f-146">検証チェックリストには、フォームが UX ガイドラインに準拠しているかどうかを手動で確認する手順が示されています。</span><span class="sxs-lookup"><span data-stu-id="c1f0f-146">The verification checklist shows you the steps for manually verifying that the form complies with UX guidelines.</span></span> <span data-ttu-id="c1f0f-147">このチェックリストには、開発環境を通じて自動的に実施されるガイドラインは含まれていません。</span><span class="sxs-lookup"><span data-stu-id="c1f0f-147">This checklist doesn't include any guidelines that will be enforced automatically through the development environment.</span></span> <span data-ttu-id="c1f0f-148">ブラウザーでフォームを開いて、これらの手順を確認します。</span><span class="sxs-lookup"><span data-stu-id="c1f0f-148">Open the form in the browser, and walk through these steps.</span></span> 

<span data-ttu-id="c1f0f-149">**標準フォーム ガイドライン:**</span><span class="sxs-lookup"><span data-stu-id="c1f0f-149">**Standard form guidelines:**</span></span>

-   <span data-ttu-id="c1f0f-150">標準フォーム ガイドラインは、Microsoft Dynamics AX [全般的なガイドライン](general-form-guidelines.md) ドキュメントに統合されました。</span><span class="sxs-lookup"><span data-stu-id="c1f0f-150">Standard form guidelines have been consolidated into the Microsoft Dynamics AX [General Form Guidelines](general-form-guidelines.md) document.</span></span>

<span data-ttu-id="c1f0f-151">**タスクの 1 つのガイドライン :**</span><span class="sxs-lookup"><span data-stu-id="c1f0f-151">**Task Single guidelines:**</span></span>

-   <span data-ttu-id="c1f0f-152">**概要** タブは、最初のタブであり、フォームを開いたときに有効になります。</span><span class="sxs-lookup"><span data-stu-id="c1f0f-152">The **Overview** tab is the first tab and is active when the form is opened.</span></span>
-   <span data-ttu-id="c1f0f-153">**全般** タブは 2 つ目のタブにする必要があり、ラベル **全般** が必要です。</span><span class="sxs-lookup"><span data-stu-id="c1f0f-153">The **General** tab must be the second tab and must have the label **General**.</span></span>

## <a name="examples"></a><span data-ttu-id="c1f0f-154">例</span><span class="sxs-lookup"><span data-stu-id="c1f0f-154">Examples</span></span>
<span data-ttu-id="c1f0f-155">フォーム: **LedgerJournalTable**</span><span class="sxs-lookup"><span data-stu-id="c1f0f-155">Form: **LedgerJournalTable**</span></span> 

<span data-ttu-id="c1f0f-156">[![タスク シングルの例 1](./media/tasksingle2-1024x669.png)](./media/tasksingle2.png)</span><span class="sxs-lookup"><span data-stu-id="c1f0f-156">[![Task Single example 1](./media/tasksingle2-1024x669.png)](./media/tasksingle2.png)</span></span> 

<span data-ttu-id="c1f0f-157">[![タスク シングルの例 2](./media/tasksingle3-1024x424.png)](./media/tasksingle3.png)</span><span class="sxs-lookup"><span data-stu-id="c1f0f-157">[![Task Single example 2](./media/tasksingle3-1024x424.png)](./media/tasksingle3.png)</span></span>

## <a name="appendix"></a><span data-ttu-id="c1f0f-158">付録</span><span class="sxs-lookup"><span data-stu-id="c1f0f-158">Appendix</span></span>
### <a name="frequently-asked-questions"></a><span data-ttu-id="c1f0f-159">よく寄せられる質問</span><span class="sxs-lookup"><span data-stu-id="c1f0f-159">Frequently asked questions</span></span>

<span data-ttu-id="c1f0f-160">このセクションには、このガイドライン/パターンに関連するよくある質問への回答があります。</span><span class="sxs-lookup"><span data-stu-id="c1f0f-160">This section will have answers to frequently asked questions that are related to this guideline/pattern.</span></span>

### <a name="open-issues"></a><span data-ttu-id="c1f0f-161">未処理の問題</span><span class="sxs-lookup"><span data-stu-id="c1f0f-161">Open issues</span></span>

-   <span data-ttu-id="c1f0f-162">なし</span><span class="sxs-lookup"><span data-stu-id="c1f0f-162">None</span></span>

### <a name="ax-2012-content"></a><span data-ttu-id="c1f0f-163">AX 2012 コンテンツ</span><span class="sxs-lookup"><span data-stu-id="c1f0f-163">AX 2012 content</span></span>

<span data-ttu-id="c1f0f-164">[![前のバージョンのビジュアルの例](./media/tasksingle4.png)](./media/tasksingle4.png)</span><span class="sxs-lookup"><span data-stu-id="c1f0f-164">[![Previous version visual example](./media/tasksingle4.png)](./media/tasksingle4.png)</span></span>
