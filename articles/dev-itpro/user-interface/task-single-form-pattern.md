---
title: タスク シングルのフォーム パターン
description: この記事では、タスク シングル フォームのパターンに関する情報を提供します。 このパターンは、ユーザーが複数のレコードを持つ単一のデータソースから発生したと認識するデータを表示するために以前は使用されていました。
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
ms.custom: 14634
ms.assetid: 38cb1058-ed69-4ffa-9bfd-4b65cc8d2a49
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4e0028ab8f5d84c42ac2166d1824117f92e68076
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/07/2019
ms.locfileid: "1512635"
---
# <a name="task-single-form-pattern"></a><span data-ttu-id="15c86-104">タスク シングルのフォーム パターン</span><span class="sxs-lookup"><span data-stu-id="15c86-104">Task Single form pattern</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="15c86-105">この記事では、タスク シングル フォームのパターンに関する情報を提供します。</span><span class="sxs-lookup"><span data-stu-id="15c86-105">This article provides information about the Task Single form pattern.</span></span> <span data-ttu-id="15c86-106">このパターンは、ユーザーが複数のレコードを持つ単一のデータソースから発生したと認識するデータを表示するために以前は使用されていました。</span><span class="sxs-lookup"><span data-stu-id="15c86-106">This pattern was previously used to present data that users would perceive as originating from a single data source that had multiple records.</span></span>

<a name="usage"></a><span data-ttu-id="15c86-107">用途</span><span class="sxs-lookup"><span data-stu-id="15c86-107">Usage</span></span>
-----

<span data-ttu-id="15c86-108">このタイプのフォームは、データが複数のレコードを持つ単一のデータ ソースから発生したとユーザーが認識することを表す場合に使用されました。</span><span class="sxs-lookup"><span data-stu-id="15c86-108">This type of form was used when you wanted to present data that users will perceive as originating from a single data source with multiple records.</span></span> <span data-ttu-id="15c86-109">新しいフォームの推奨パターンではありません。</span><span class="sxs-lookup"><span data-stu-id="15c86-109">This isn't a recommended pattern for new forms.</span></span> <span data-ttu-id="15c86-110">このパターンを使用する新しいフォームを作成する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="15c86-110">No new forms should be created that use this pattern.</span></span> <span data-ttu-id="15c86-111">このパターンは、レガシー フォームの構造と安定性を提供し、より現代的なフォーム パターンへの移行パスも提供します。</span><span class="sxs-lookup"><span data-stu-id="15c86-111">This pattern will provide structure and stability for legacy forms, and will also provide a migration path to more modern form patterns.</span></span>

## <a name="wireframe"></a><span data-ttu-id="15c86-112">ワイヤーフレーム</span><span class="sxs-lookup"><span data-stu-id="15c86-112">Wireframe</span></span>
<span data-ttu-id="15c86-113">[![ワイヤーフレーム](./media/tasksingle1-1024x577.png)](./media/tasksingle1.png)</span><span class="sxs-lookup"><span data-stu-id="15c86-113">[![Wireframe](./media/tasksingle1-1024x577.png)](./media/tasksingle1.png)</span></span>

## <a name="pattern-changes"></a><span data-ttu-id="15c86-114">パターンの変更</span><span class="sxs-lookup"><span data-stu-id="15c86-114">Pattern changes</span></span>
<span data-ttu-id="15c86-115">Microsoft Dynamics AX 2012 以降に加えられるこのパターンへの主な変更を次に示します。</span><span class="sxs-lookup"><span data-stu-id="15c86-115">Here are the main changes to this pattern since Microsoft Dynamics AX 2012:</span></span>

-   <span data-ttu-id="15c86-116">表示モードでフォームを開きます。</span><span class="sxs-lookup"><span data-stu-id="15c86-116">The form opens in view mode.</span></span>
-   <span data-ttu-id="15c86-117">コマンドは、ツールバー (アクション ペイン ストライプ) から標準アクション ペインに移動されています。</span><span class="sxs-lookup"><span data-stu-id="15c86-117">Commands have been moved to the standard ActionPane from a Toolbar (ActionPane strips).</span></span>
-   <span data-ttu-id="15c86-118">最初のタブの **概要** ラベルが **リスト** に変更されました。</span><span class="sxs-lookup"><span data-stu-id="15c86-118">The **Overview** label on the first tab has been changed to **List**.</span></span>
-   <span data-ttu-id="15c86-119">タブ コンテナーのコンテンツは、応答レイアウトに動的列を使用します。</span><span class="sxs-lookup"><span data-stu-id="15c86-119">The content of the tab container uses dynamic columns for a responsive layout.</span></span>

## <a name="model"></a><span data-ttu-id="15c86-120">モデル</span><span class="sxs-lookup"><span data-stu-id="15c86-120">Model</span></span>
### <a name="high-level-structure"></a><span data-ttu-id="15c86-121">高レベル構造体</span><span class="sxs-lookup"><span data-stu-id="15c86-121">High-level structure</span></span>

- <span data-ttu-id="15c86-122">デザイン</span><span class="sxs-lookup"><span data-stu-id="15c86-122">Design</span></span>

    - <span data-ttu-id="15c86-123">ActionPane (アクション ウィンドウ)</span><span class="sxs-lookup"><span data-stu-id="15c86-123">ActionPane (Action Pane)</span></span>
    - <span data-ttu-id="15c86-124">*CustomFilter (グループ) \[オプション\]*</span><span class="sxs-lookup"><span data-stu-id="15c86-124">*CustomFilter (Group) \[Optional\]*</span></span>
    - <span data-ttu-id="15c86-125">タブ (タブ)</span><span class="sxs-lookup"><span data-stu-id="15c86-125">Tab (Tab)</span></span>

        - <span data-ttu-id="15c86-126">概要 (TabPage)</span><span class="sxs-lookup"><span data-stu-id="15c86-126">Overview (TabPage)</span></span>

            - <span data-ttu-id="15c86-127">グリッド (グリッド)</span><span class="sxs-lookup"><span data-stu-id="15c86-127">Grid (Grid)</span></span>
            - <span data-ttu-id="15c86-128">*RowExtension (グループ) \[オプション\]*</span><span class="sxs-lookup"><span data-stu-id="15c86-128">*RowExtension (Group) \[Optional\]*</span></span>

        - <span data-ttu-id="15c86-129">一般 (TabPage、0..N を繰り返します)</span><span class="sxs-lookup"><span data-stu-id="15c86-129">General (TabPage, repeats 0..N)</span></span>

    - <span data-ttu-id="15c86-130">*FooterGroup (グループ) \[オプション\]*</span><span class="sxs-lookup"><span data-stu-id="15c86-130">*FooterGroup (Group) \[Optional\]*</span></span>

### <a name="core-components"></a><span data-ttu-id="15c86-131">コア コンポーネント</span><span class="sxs-lookup"><span data-stu-id="15c86-131">Core components</span></span>

1.  <span data-ttu-id="15c86-132">**Form.Design** に TaskSingle パターンを適用します。</span><span class="sxs-lookup"><span data-stu-id="15c86-132">Apply the TaskSingle pattern on **Form.Design**.</span></span>
2.  <span data-ttu-id="15c86-133">BP 警告に対処します。</span><span class="sxs-lookup"><span data-stu-id="15c86-133">Address BP Warnings:</span></span>
    1.  <span data-ttu-id="15c86-134">**Design.Caption** は空ではありません。</span><span class="sxs-lookup"><span data-stu-id="15c86-134">**Design.Caption** isn't empty.</span></span>
    2.  <span data-ttu-id="15c86-135">このフォームは少なくとも 1 つのメニュー項目で参照される必要があります。</span><span class="sxs-lookup"><span data-stu-id="15c86-135">The form must be referenced by at least one menu item.</span></span>
    3.  <span data-ttu-id="15c86-136">**TabPage.Caption** は空ではありません。</span><span class="sxs-lookup"><span data-stu-id="15c86-136">**TabPage.Caption** isn't empty.</span></span>
    4.  <span data-ttu-id="15c86-137">**TabPage.DataSource** は空ではありません。</span><span class="sxs-lookup"><span data-stu-id="15c86-137">**TabPage.DataSource** isn't empty.</span></span>
    5.  <span data-ttu-id="15c86-138">**StaticText.Text** は空ではありません。</span><span class="sxs-lookup"><span data-stu-id="15c86-138">**StaticText.Text** isn't empty.</span></span>

### <a name="related-patterns"></a><span data-ttu-id="15c86-139">関連するパターン</span><span class="sxs-lookup"><span data-stu-id="15c86-139">Related patterns</span></span>

-   [<span data-ttu-id="15c86-140">タスク ダブル</span><span class="sxs-lookup"><span data-stu-id="15c86-140">Task Double</span></span>](task-double-form-pattern.md)

### <a name="commonly-used-subpatterns"></a><span data-ttu-id="15c86-141">一般的に使用されるサブパターン</span><span class="sxs-lookup"><span data-stu-id="15c86-141">Commonly used subpatterns</span></span>

-   [<span data-ttu-id="15c86-142">カスタム フィルター グループ</span><span class="sxs-lookup"><span data-stu-id="15c86-142">Custom Filter Group</span></span>](custom-filter-group-subpattern.md)
-   [<span data-ttu-id="15c86-143">フィールドおよびフィールド グループ</span><span class="sxs-lookup"><span data-stu-id="15c86-143">Fields and Field Groups</span></span>](fields-field-groups-subpattern.md)
-   [<span data-ttu-id="15c86-144">ツールバーおよびリスト</span><span class="sxs-lookup"><span data-stu-id="15c86-144">Toolbar and List</span></span>](toolbar-list-subpattern.md)
-   [<span data-ttu-id="15c86-145">ツールバーおよびフィールド</span><span class="sxs-lookup"><span data-stu-id="15c86-145">Toolbar and Fields</span></span>](toolbar-fields-subpattern.md)

## <a name="ux-guidelines"></a><span data-ttu-id="15c86-146">UX ガイドライン</span><span class="sxs-lookup"><span data-stu-id="15c86-146">UX guidelines</span></span>
<span data-ttu-id="15c86-147">検証チェックリストには、フォームが UX ガイドラインに準拠しているかどうかを手動で確認する手順が示されています。</span><span class="sxs-lookup"><span data-stu-id="15c86-147">The verification checklist shows you the steps for manually verifying that the form complies with UX guidelines.</span></span> <span data-ttu-id="15c86-148">このチェックリストには、開発環境を通じて自動的に実施されるガイドラインは含まれていません。</span><span class="sxs-lookup"><span data-stu-id="15c86-148">This checklist doesn't include any guidelines that will be enforced automatically through the development environment.</span></span> <span data-ttu-id="15c86-149">ブラウザーでフォームを開いて、これらの手順を確認します。</span><span class="sxs-lookup"><span data-stu-id="15c86-149">Open the form in the browser, and walk through these steps.</span></span> 

<span data-ttu-id="15c86-150">**標準フォーム ガイドライン:**</span><span class="sxs-lookup"><span data-stu-id="15c86-150">**Standard form guidelines:**</span></span>

-   <span data-ttu-id="15c86-151">標準フォーム ガイドラインは、Microsoft Dynamics AX [全般的なガイドライン](general-form-guidelines.md) ドキュメントに統合されました。</span><span class="sxs-lookup"><span data-stu-id="15c86-151">Standard form guidelines have been consolidated into the Microsoft Dynamics AX [General Form Guidelines](general-form-guidelines.md) document.</span></span>

<span data-ttu-id="15c86-152">**タスクの 1 つのガイドライン :**</span><span class="sxs-lookup"><span data-stu-id="15c86-152">**Task Single guidelines:**</span></span>

-   <span data-ttu-id="15c86-153">**概要** タブは、最初のタブであり、フォームを開いたときに有効になります。</span><span class="sxs-lookup"><span data-stu-id="15c86-153">The **Overview** tab is the first tab and is active when the form is opened.</span></span>
-   <span data-ttu-id="15c86-154">**全般** タブは 2 つ目のタブにする必要があり、ラベル **全般** が必要です。</span><span class="sxs-lookup"><span data-stu-id="15c86-154">The **General** tab must be the second tab and must have the label **General**.</span></span>

## <a name="examples"></a><span data-ttu-id="15c86-155">例</span><span class="sxs-lookup"><span data-stu-id="15c86-155">Examples</span></span>
<span data-ttu-id="15c86-156">フォーム: **LedgerJournalTable**</span><span class="sxs-lookup"><span data-stu-id="15c86-156">Form: **LedgerJournalTable**</span></span> 

<span data-ttu-id="15c86-157">[![タスク シングルの例 1](./media/tasksingle2-1024x669.png)](./media/tasksingle2.png)</span><span class="sxs-lookup"><span data-stu-id="15c86-157">[![Task Single example 1](./media/tasksingle2-1024x669.png)](./media/tasksingle2.png)</span></span> 

<span data-ttu-id="15c86-158">[![タスク シングルの例 2](./media/tasksingle3-1024x424.png)](./media/tasksingle3.png)</span><span class="sxs-lookup"><span data-stu-id="15c86-158">[![Task Single example 2](./media/tasksingle3-1024x424.png)](./media/tasksingle3.png)</span></span>

## <a name="appendix"></a><span data-ttu-id="15c86-159">付録</span><span class="sxs-lookup"><span data-stu-id="15c86-159">Appendix</span></span>
### <a name="frequently-asked-questions"></a><span data-ttu-id="15c86-160">よく寄せられる質問</span><span class="sxs-lookup"><span data-stu-id="15c86-160">Frequently asked questions</span></span>

<span data-ttu-id="15c86-161">このセクションには、このガイドライン/パターンに関連するよくある質問への回答があります。</span><span class="sxs-lookup"><span data-stu-id="15c86-161">This section will have answers to frequently asked questions that are related to this guideline/pattern.</span></span>

### <a name="open-issues"></a><span data-ttu-id="15c86-162">未処理の問題</span><span class="sxs-lookup"><span data-stu-id="15c86-162">Open issues</span></span>

-   <span data-ttu-id="15c86-163">なし</span><span class="sxs-lookup"><span data-stu-id="15c86-163">None</span></span>

### <a name="ax-2012-content"></a><span data-ttu-id="15c86-164">AX 2012 コンテンツ</span><span class="sxs-lookup"><span data-stu-id="15c86-164">AX 2012 content</span></span>

<span data-ttu-id="15c86-165">[![AX 2012 視覚例](./media/tasksingle4.png)](./media/tasksingle4.png)</span><span class="sxs-lookup"><span data-stu-id="15c86-165">[![AX 2012 visual example](./media/tasksingle4.png)](./media/tasksingle4.png)</span></span>
