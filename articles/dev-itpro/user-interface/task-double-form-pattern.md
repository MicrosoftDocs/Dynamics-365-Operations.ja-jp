---
title: タスク ダブルのフォーム パターン
description: この記事では、タスク ダブル フォームのパターンに関する情報を提供します。 このパターンは、以前は同じフォームに親エンティティと子エンティティを表示するために使用されていました。
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
ms.custom: 14651
ms.assetid: 9f28e5f9-efec-48c5-aaa6-b68a505c4df3
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 75b4de24af7155f42e447a8c1a9a6e28650c04b2
ms.sourcegitcommit: 16bfa0fd08feec1647829630401ce62ce2ffa1a4
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/02/2019
ms.locfileid: "1851081"
---
# <a name="task-double-form-pattern"></a><span data-ttu-id="49331-104">タスク ダブルのフォーム パターン</span><span class="sxs-lookup"><span data-stu-id="49331-104">Task Double form pattern</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="49331-105">この記事では、タスク ダブル フォームのパターンに関する情報を提供します。</span><span class="sxs-lookup"><span data-stu-id="49331-105">This article provides information about the Task Double form pattern.</span></span> <span data-ttu-id="49331-106">このパターンは、以前は同じフォームに親エンティティと子エンティティを表示するために使用されていました。</span><span class="sxs-lookup"><span data-stu-id="49331-106">This pattern was previously used to present a parent and child entity in the same form.</span></span>

<a name="usage"></a><span data-ttu-id="49331-107">用途</span><span class="sxs-lookup"><span data-stu-id="49331-107">Usage</span></span>
-----

<span data-ttu-id="49331-108">このタイプのフォームは、以前は親/子エンティティを同じフォームに表示する場合に使用されていました。</span><span class="sxs-lookup"><span data-stu-id="49331-108">This type of form has previously been used when you wanted to present parent/child entities in the same form.</span></span> <span data-ttu-id="49331-109">新しいフォームの推奨パターンではありません。</span><span class="sxs-lookup"><span data-stu-id="49331-109">This isn't a recommended pattern for new forms.</span></span> <span data-ttu-id="49331-110">このパターンを使用する新しいフォームを作成する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="49331-110">No new forms should be created that use this pattern.</span></span> <span data-ttu-id="49331-111">このパターンは、レガシー フォームの構造と安定性を提供し、より現代的なフォーム パターンへの移行パスも提供します。</span><span class="sxs-lookup"><span data-stu-id="49331-111">This pattern will provide structure and stability for legacy forms, and will also provide a migration path to more modern form patterns.</span></span>

## <a name="wireframe"></a><span data-ttu-id="49331-112">ワイヤーフレーム</span><span class="sxs-lookup"><span data-stu-id="49331-112">Wireframe</span></span>

<span data-ttu-id="49331-113">[![patternTaskDouble](./media/patterntaskdouble.png)](./media/patterntaskdouble.png)[](./media/taskdouble1.png)</span><span class="sxs-lookup"><span data-stu-id="49331-113">[![patternTaskDouble](./media/patterntaskdouble.png)](./media/patterntaskdouble.png)[](./media/taskdouble1.png)</span></span>

## <a name="pattern-changes"></a><span data-ttu-id="49331-114">パターンの変更</span><span class="sxs-lookup"><span data-stu-id="49331-114">Pattern changes</span></span>
<span data-ttu-id="49331-115">Microsoft Dynamics AX 2012 以降に加えられるこのパターンへの主な変更を次に示します。</span><span class="sxs-lookup"><span data-stu-id="49331-115">Here are the main changes to this pattern since Microsoft Dynamics AX 2012:</span></span>

-   <span data-ttu-id="49331-116">表示モードでフォームを開きます。</span><span class="sxs-lookup"><span data-stu-id="49331-116">The form opens in view mode.</span></span>
-   <span data-ttu-id="49331-117">上部の ActionPane ストリップ コントロールが標準の ActionPane に変換されました。</span><span class="sxs-lookup"><span data-stu-id="49331-117">The top ActionPane strip control has been converted to a standard ActionPane.</span></span>
-   <span data-ttu-id="49331-118">親タブの **概要** ラベルが **リスト** に変更されました。</span><span class="sxs-lookup"><span data-stu-id="49331-118">The **Overview** label on the parent tab has been changed to **List**.</span></span>
-   <span data-ttu-id="49331-119">タブ コンテナーの内容は、応答レイアウト用の動的列を使用します。</span><span class="sxs-lookup"><span data-stu-id="49331-119">The contents of the tab container use dynamic columns for a responsive layout.</span></span>
-   <span data-ttu-id="49331-120">子タブのリストのラベルは、**&lt;x&gt; リスト** で、ここで、**&lt;x&gt;** は、エンティティに基づいて適切な文字列に置き換えられます。</span><span class="sxs-lookup"><span data-stu-id="49331-120">The label for the child tab’s list should be **&lt;x&gt; list**, where **&lt;x&gt;** is replaced by an appropriate string, based on the entity.</span></span> <span data-ttu-id="49331-121">たとえば、子エンティティは通常請求と呼ばれ、タブのラベルは**請求リスト**である必要があります。</span><span class="sxs-lookup"><span data-stu-id="49331-121">For example, if the child entity is usually called Charges, the label for the tab should be **Charges list**.</span></span>
    -   <span data-ttu-id="49331-122">例外: 子エンティティが何らかの「リスト」である場合は、末尾に「リスト」のワードは追加できません。</span><span class="sxs-lookup"><span data-stu-id="49331-122">Exception: If the child entity is “lines” of some sort, the word “list” should not be added to the end.</span></span>

## <a name="model"></a><span data-ttu-id="49331-123">モデル</span><span class="sxs-lookup"><span data-stu-id="49331-123">Model</span></span>
### <a name="high-level-structure"></a><span data-ttu-id="49331-124">高レベル構造体</span><span class="sxs-lookup"><span data-stu-id="49331-124">High-level structure</span></span>

- <span data-ttu-id="49331-125">デザイン</span><span class="sxs-lookup"><span data-stu-id="49331-125">Design</span></span>

    - <span data-ttu-id="49331-126">ActionPane (アクション ウィンドウ)</span><span class="sxs-lookup"><span data-stu-id="49331-126">ActionPane (Action Pane)</span></span>
    - <span data-ttu-id="49331-127">*CustomFilter (グループ) \[オプション\]*</span><span class="sxs-lookup"><span data-stu-id="49331-127">*CustomFilter (Group) \[Optional\]*</span></span>
    - <span data-ttu-id="49331-128">ParentTab (Tab)</span><span class="sxs-lookup"><span data-stu-id="49331-128">ParentTab (Tab)</span></span>

        - <span data-ttu-id="49331-129">ParentList (TabPage) – **注記:** ツールバーとリストのサブパターンが使用されます。</span><span class="sxs-lookup"><span data-stu-id="49331-129">ParentList (TabPage) – **Note:** The Toolbar and List subpattern is used.</span></span>
        - <span data-ttu-id="49331-130">一般 (TabPage は 0..N を繰り返します)</span><span class="sxs-lookup"><span data-stu-id="49331-130">General (TabPage repeats 0..N)</span></span>

    - <span data-ttu-id="49331-131">*ParentFooterGroup (グループ) \[オプション\]*</span><span class="sxs-lookup"><span data-stu-id="49331-131">*ParentFooterGroup (Group) \[Optional\]*</span></span>
    - <span data-ttu-id="49331-132">HSplitter (グループ)</span><span class="sxs-lookup"><span data-stu-id="49331-132">HSplitter (Group)</span></span>
    - <span data-ttu-id="49331-133">*ChildToolbar (アクション ペイン) \[オプション\]*</span><span class="sxs-lookup"><span data-stu-id="49331-133">*ChildToolbar (ActionPane) \[Optional\]*</span></span>
    - <span data-ttu-id="49331-134">ChildTab (タブ)</span><span class="sxs-lookup"><span data-stu-id="49331-134">ChildTab (Tab)</span></span>

        - <span data-ttu-id="49331-135">ChildList (TabPage) – **注記:** ツールバーとリストのサブパターンが使用されます。</span><span class="sxs-lookup"><span data-stu-id="49331-135">ChildList (TabPage) – **Note:** The Toolbar and List subpattern is used.</span></span>
        - <span data-ttu-id="49331-136">一般 (TabPage、0..N を繰り返します)</span><span class="sxs-lookup"><span data-stu-id="49331-136">General (TabPage, repeats 0..N)</span></span>

    - <span data-ttu-id="49331-137">*ChildFooterGroup(グループ) \[オプション\]*</span><span class="sxs-lookup"><span data-stu-id="49331-137">*ChildFooterGroup (Group) \[Optional\]*</span></span>

### <a name="core-components"></a><span data-ttu-id="49331-138">コア コンポーネント</span><span class="sxs-lookup"><span data-stu-id="49331-138">Core components</span></span>

1.  <span data-ttu-id="49331-139">**Form.Design** にタスク ダブルのパターンを適用します。</span><span class="sxs-lookup"><span data-stu-id="49331-139">Apply the Task Double pattern on **Form.Design**.</span></span>
2.  <span data-ttu-id="49331-140">BP 警告に対処します。</span><span class="sxs-lookup"><span data-stu-id="49331-140">Address BP Warnings:</span></span>
    1.  <span data-ttu-id="49331-141">**Design.Caption** は空ではありません。</span><span class="sxs-lookup"><span data-stu-id="49331-141">**Design.Caption** isn't empty.</span></span>
    2.  <span data-ttu-id="49331-142">このフォームは少なくとも 1 つのメニュー項目で参照される必要があります。</span><span class="sxs-lookup"><span data-stu-id="49331-142">The form must be referenced by at least one menu item.</span></span>
    3.  <span data-ttu-id="49331-143">**TabPage.Caption** は空ではありません。</span><span class="sxs-lookup"><span data-stu-id="49331-143">**TabPage.Caption** isn't empty.</span></span>
    4.  <span data-ttu-id="49331-144">**TabPage.DataSource** は空ではありません。</span><span class="sxs-lookup"><span data-stu-id="49331-144">**TabPage.DataSource** isn't empty.</span></span>
    5.  <span data-ttu-id="49331-145">**StaticText.Text** は空ではありません。</span><span class="sxs-lookup"><span data-stu-id="49331-145">**StaticText.Text** isn't empty.</span></span>

### <a name="related-patterns"></a><span data-ttu-id="49331-146">関連するパターン</span><span class="sxs-lookup"><span data-stu-id="49331-146">Related patterns</span></span>

-   [<span data-ttu-id="49331-147">タスク シングル</span><span class="sxs-lookup"><span data-stu-id="49331-147">Task Single</span></span>](task-single-form-pattern.md)

### <a name="commonly-used-subpatterns"></a><span data-ttu-id="49331-148">一般的に使用されるサブパターン</span><span class="sxs-lookup"><span data-stu-id="49331-148">Commonly used subpatterns</span></span>

-   [<span data-ttu-id="49331-149">カスタム フィルター グループ</span><span class="sxs-lookup"><span data-stu-id="49331-149">Custom Filter Group</span></span>](custom-filter-group-subpattern.md)
-   [<span data-ttu-id="49331-150">フィールドおよびフィールド グループ</span><span class="sxs-lookup"><span data-stu-id="49331-150">Fields and Field Groups</span></span>](fields-field-groups-subpattern.md)
-   [<span data-ttu-id="49331-151">ツールバーおよびリスト</span><span class="sxs-lookup"><span data-stu-id="49331-151">Toolbar and List</span></span>](toolbar-list-subpattern.md)
-   [<span data-ttu-id="49331-152">ツールバーおよびフィールド</span><span class="sxs-lookup"><span data-stu-id="49331-152">Toolbar and Fields</span></span>](toolbar-fields-subpattern.md)

## <a name="ux-guidelines"></a><span data-ttu-id="49331-153">UX ガイドライン</span><span class="sxs-lookup"><span data-stu-id="49331-153">UX guidelines</span></span>
<span data-ttu-id="49331-154">検証チェックリストには、フォームが UX ガイドラインに準拠しているかどうかを手動で確認する手順が示されています。</span><span class="sxs-lookup"><span data-stu-id="49331-154">The verification checklist shows the steps for manually verifying that the form complies with UX guidelines.</span></span> <span data-ttu-id="49331-155">このチェックリストには、開発環境を通じて自動的に実施されるガイドラインは含まれていません。</span><span class="sxs-lookup"><span data-stu-id="49331-155">This checklist doesn't include any guidelines that will be enforced automatically through the development environment.</span></span> <span data-ttu-id="49331-156">ブラウザーでフォームを開いて、これらの手順を確認します。</span><span class="sxs-lookup"><span data-stu-id="49331-156">Open the form in the browser, and walk through these steps.</span></span>

<span data-ttu-id="49331-157">**標準フォーム ガイドライン:**</span><span class="sxs-lookup"><span data-stu-id="49331-157">**Standard form guidelines:**</span></span>

-   <span data-ttu-id="49331-158">標準フォーム ガイドラインは、Microsoft Dynamics AX [全般的なガイドライン](general-form-guidelines.md) ドキュメントに統合されました。</span><span class="sxs-lookup"><span data-stu-id="49331-158">Standard form guidelines have been consolidated into the Microsoft Dynamics AX [General Form Guidelines](general-form-guidelines.md) document.</span></span>

<span data-ttu-id="49331-159">**タスクの二重ガイドライン:**</span><span class="sxs-lookup"><span data-stu-id="49331-159">**Task Double guidelines:**</span></span>

-   <span data-ttu-id="49331-160">**概要** タブは、最初のタブであり、フォームを開いたときに有効になります。</span><span class="sxs-lookup"><span data-stu-id="49331-160">The **Overview** tab is the first tab and is active when the form is opened.</span></span>
-   <span data-ttu-id="49331-161">子タブコントロールの最初のタブは、**Lines list** または適切なバリエーションと呼びます。</span><span class="sxs-lookup"><span data-stu-id="49331-161">The first tab on a child tab control should be called **Lines list** or an appropriate variation.</span></span>
-   <span data-ttu-id="49331-162">親グリッドでの選択内容により子グリッド内のコンテンツが更新されます。</span><span class="sxs-lookup"><span data-stu-id="49331-162">Selection in the parent grid will update content in the child grid.</span></span>

## <a name="example"></a><span data-ttu-id="49331-163">例</span><span class="sxs-lookup"><span data-stu-id="49331-163">Example</span></span>
<span data-ttu-id="49331-164">フォーム: **HRMAbsenceTableHistory**</span><span class="sxs-lookup"><span data-stu-id="49331-164">Form: **HRMAbsenceTableHistory**</span></span> 

<span data-ttu-id="49331-165">[![タスク ダブルの例](./media/taskdouble2-1024x639.png)](./media/taskdouble2.png)</span><span class="sxs-lookup"><span data-stu-id="49331-165">[![Task Double example](./media/taskdouble2-1024x639.png)](./media/taskdouble2.png)</span></span>

## <a name="appendix"></a><span data-ttu-id="49331-166">付録</span><span class="sxs-lookup"><span data-stu-id="49331-166">Appendix</span></span>
### <a name="frequently-asked-questions"></a><span data-ttu-id="49331-167">よく寄せられる質問</span><span class="sxs-lookup"><span data-stu-id="49331-167">Frequently asked questions</span></span>

<span data-ttu-id="49331-168">このセクションには、このガイドライン/パターンに関連するよくある質問への回答があります。</span><span class="sxs-lookup"><span data-stu-id="49331-168">This section will have answers to frequently asked questions that are related to this guideline/pattern.</span></span>

### <a name="open-issues"></a><span data-ttu-id="49331-169">未処理の問題</span><span class="sxs-lookup"><span data-stu-id="49331-169">Open issues</span></span>

-   <span data-ttu-id="49331-170">なし</span><span class="sxs-lookup"><span data-stu-id="49331-170">None</span></span>

### <a name="ax-2012-content"></a><span data-ttu-id="49331-171">AX 2012 コンテンツ</span><span class="sxs-lookup"><span data-stu-id="49331-171">AX 2012 content</span></span>

<span data-ttu-id="49331-172">[![AX 2012 視覚例](./media/taskdouble3.png)](./media/taskdouble3.png)</span><span class="sxs-lookup"><span data-stu-id="49331-172">[![AX 2012 visual example](./media/taskdouble3.png)](./media/taskdouble3.png)</span></span>
