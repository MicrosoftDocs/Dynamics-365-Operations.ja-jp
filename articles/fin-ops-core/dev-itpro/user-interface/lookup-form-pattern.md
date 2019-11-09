---
title: ルックアップのフォーム パターン
description: このトピックでは、ルックアップ フォームのパターンについて説明します。
author: jasongre
manager: AnnBe
ms.date: 11/09/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: sericks
ms.search.scope: Operations
ms.custom: 12911
ms.assetid: 0bc7bde2-6150-4a80-8738-9a5201b51df2
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 695997f9ed2f96a05f5f025c39fe22dc30336d45
ms.sourcegitcommit: 574309903f15eeab7911091114885b5c7279d22a
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/24/2019
ms.locfileid: "2658836"
---
# <a name="lookup-form-pattern"></a><span data-ttu-id="5ec05-103">ルックアップのフォーム パターン</span><span class="sxs-lookup"><span data-stu-id="5ec05-103">Lookup form pattern</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="5ec05-104">このトピックでは、ルックアップ フォームのパターンについて説明します。</span><span class="sxs-lookup"><span data-stu-id="5ec05-104">This topic provides information about the Lookup form pattern.</span></span> <span data-ttu-id="5ec05-105">標準フレームワークによって指定されたルックアップで正しいデータが提供されない場合や、データの高度な視覚化が必要な場合は、カスタム ルックアップ フォームを使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="5ec05-105">Custom lookup forms should be used when a standard framework-provided lookup would not provide the correct data, or when advanced visualization of the data is required.</span></span>

<a name="usage"></a><span data-ttu-id="5ec05-106">用途</span><span class="sxs-lookup"><span data-stu-id="5ec05-106">Usage</span></span>
-----

<span data-ttu-id="5ec05-107">カスタム ルックアップ フォームは、標準フレームワークによって指定されたルックアップ (通常はテーブル定義で定義された AutoLookup フィールド グループを使用して生成される)、が正しいデータを提供しない場合、またはデータの高度な視覚化が必要な場合に使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="5ec05-107">Custom lookup forms should be used when a standard framework-provided lookup (which is typically generated by using the AutoLookup field group that is defined on the table definition), would not provide the correct data, or when advanced visualization of the data is required.</span></span> <span data-ttu-id="5ec05-108">このドキュメントでは、3 つのパターンについて説明します。</span><span class="sxs-lookup"><span data-stu-id="5ec05-108">Three patterns are described in this document:</span></span>

-   <span data-ttu-id="5ec05-109">**基本のルックアップ** – これは、リストまたはツリーが 1 つだけの基本のルックアップ パターンです。オプションのカスタム フィルターとアクションもあります。</span><span class="sxs-lookup"><span data-stu-id="5ec05-109">**Lookup basic** – This is the basic Lookup pattern that has just one list or tree, and also optional custom filters and actions.</span></span>
-   <span data-ttu-id="5ec05-110">**タブ付きのルックアップ** – このルックアップ パターンは、ルックアップの複数のビューをユーザーが利用できるようにする場合に使用されます。</span><span class="sxs-lookup"><span data-stu-id="5ec05-110">**Lookup w/tabs** – This Lookup pattern is used when more than one view of the lookup can be made available to the user.</span></span> <span data-ttu-id="5ec05-111">タブ キャプションは表示されません。</span><span class="sxs-lookup"><span data-stu-id="5ec05-111">Tab captions aren't shown.</span></span> <span data-ttu-id="5ec05-112">代わりに、タブはコンボ ボックスを通じて選択されます。</span><span class="sxs-lookup"><span data-stu-id="5ec05-112">Instead, the tab is selected through a combo box.</span></span>
-   <span data-ttu-id="5ec05-113">**プレビュー付きのルックアップ** – このより高度なルックアップ パターンにより、ルックアップ グリッドの現在のレコードのプレビューが有効になります。</span><span class="sxs-lookup"><span data-stu-id="5ec05-113">**Lookup w/preview** – This more advanced Lookup pattern enables a preview of the current record in the lookup grid.</span></span>

## <a name="wireframe"></a><span data-ttu-id="5ec05-114">ワイヤーフレーム</span><span class="sxs-lookup"><span data-stu-id="5ec05-114">Wireframe</span></span>
### <a name="lookup-basic"></a><span data-ttu-id="5ec05-115">基本のルックアップ</span><span class="sxs-lookup"><span data-stu-id="5ec05-115">Lookup basic</span></span>

<span data-ttu-id="5ec05-116">[![基本ルックアップ フォームのワイヤーフレーム](./media/lookupform1.png)](./media/lookupform1.png)</span><span class="sxs-lookup"><span data-stu-id="5ec05-116">[![Wireframe of basic lookup form](./media/lookupform1.png)](./media/lookupform1.png)</span></span>

### <a name="lookup-with-tabs"></a><span data-ttu-id="5ec05-117">タブ付きルックアップ</span><span class="sxs-lookup"><span data-stu-id="5ec05-117">Lookup with tabs</span></span>

<span data-ttu-id="5ec05-118">[![タブ付きルックアップ フォームのワイヤーフレーム](./media/lookupform2.png)](./media/lookupform2.png)</span><span class="sxs-lookup"><span data-stu-id="5ec05-118">[![Wireframe of lookup form with tabs](./media/lookupform2.png)](./media/lookupform2.png)</span></span>

### <a name="lookup-with-preview"></a><span data-ttu-id="5ec05-119">プレビューによるルックアップ</span><span class="sxs-lookup"><span data-stu-id="5ec05-119">Lookup with preview</span></span>

<span data-ttu-id="5ec05-120">[![プレビューによるルックアップ フォームのワイヤーフレーム](./media/lookupform3.png)](./media/lookupform3.png)</span><span class="sxs-lookup"><span data-stu-id="5ec05-120">[![Wireframe of lookup form with preview](./media/lookupform3.png)](./media/lookupform3.png)</span></span>

## <a name="pattern-changes"></a><span data-ttu-id="5ec05-121">パターンの変更</span><span class="sxs-lookup"><span data-stu-id="5ec05-121">Pattern changes</span></span>
<span data-ttu-id="5ec05-122">Microsoft Dynamics AX 2012 以降に加えられるこのパターンへの変更を次に示します。</span><span class="sxs-lookup"><span data-stu-id="5ec05-122">Here are the changes to this pattern since Microsoft Dynamics AX 2012:</span></span>

-   <span data-ttu-id="5ec05-123">タブは非表示になり、コンボ ボックスで管理されている必要があります。</span><span class="sxs-lookup"><span data-stu-id="5ec05-123">Tabs should be hidden and controlled by a combo box.</span></span>
-   <span data-ttu-id="5ec05-124">必要に応じてスプリッター/プレビューを追加します。</span><span class="sxs-lookup"><span data-stu-id="5ec05-124">Optionally add a splitter/preview.</span></span>

## <a name="model"></a><span data-ttu-id="5ec05-125">モデル</span><span class="sxs-lookup"><span data-stu-id="5ec05-125">Model</span></span>
### <a name="lookup-basic--high-level-structure"></a><span data-ttu-id="5ec05-126">基本のルックアップ – 高度なレベル構造</span><span class="sxs-lookup"><span data-stu-id="5ec05-126">Lookup basic – High-level structure</span></span>

- <span data-ttu-id="5ec05-127">デザイン</span><span class="sxs-lookup"><span data-stu-id="5ec05-127">Design</span></span>

    - <span data-ttu-id="5ec05-128">*CustomFilter (グループ) \[オプション\]*</span><span class="sxs-lookup"><span data-stu-id="5ec05-128">*CustomFilter (Group) \[Optional\]*</span></span>
    - <span data-ttu-id="5ec05-129">グリッド | ツリー | ListView</span><span class="sxs-lookup"><span data-stu-id="5ec05-129">Grid | Tree | ListView</span></span>
    - <span data-ttu-id="5ec05-130">*LookupActions (グループ) \[オプション\]*</span><span class="sxs-lookup"><span data-stu-id="5ec05-130">*LookupActions (Group) \[Optional\]*</span></span>

### <a name="lookup-wtabs--high-level-structure"></a><span data-ttu-id="5ec05-131">タブ付きルックアップ – 高度なレベル構造</span><span class="sxs-lookup"><span data-stu-id="5ec05-131">Lookup w/tabs – High-level structure</span></span>

- <span data-ttu-id="5ec05-132">デザイン</span><span class="sxs-lookup"><span data-stu-id="5ec05-132">Design</span></span>

    - <span data-ttu-id="5ec05-133">*CustomFilter (グループ) \[オプション\]*</span><span class="sxs-lookup"><span data-stu-id="5ec05-133">*CustomFilter (Group) \[Optional\]*</span></span>
    - <span data-ttu-id="5ec05-134">LookupTab (タブ)</span><span class="sxs-lookup"><span data-stu-id="5ec05-134">LookupTab (Tab)</span></span>

        - <span data-ttu-id="5ec05-135">LookupTabPage (TabPage、反復 1..N)</span><span class="sxs-lookup"><span data-stu-id="5ec05-135">LookupTabPage (TabPage, repeats 1..N)</span></span>

            - <span data-ttu-id="5ec05-136">グリッド | ツリー | ListView</span><span class="sxs-lookup"><span data-stu-id="5ec05-136">Grid | Tree | ListView</span></span>

    - <span data-ttu-id="5ec05-137">*LookupActions (グループ) \[オプション\]*</span><span class="sxs-lookup"><span data-stu-id="5ec05-137">*LookupActions (Group) \[Optional\]*</span></span>

### <a name="lookup-wpreview--high-level-structure"></a><span data-ttu-id="5ec05-138">プレビュー付きルックアップ – 高度なレベル構造</span><span class="sxs-lookup"><span data-stu-id="5ec05-138">Lookup w/preview – High-level structure</span></span>

- <span data-ttu-id="5ec05-139">デザイン</span><span class="sxs-lookup"><span data-stu-id="5ec05-139">Design</span></span>

    - <span data-ttu-id="5ec05-140">*CustomFilter (グループ) \[オプション\]*</span><span class="sxs-lookup"><span data-stu-id="5ec05-140">*CustomFilter (Group) \[Optional\]*</span></span>
    - <span data-ttu-id="5ec05-141">LookupContent (グループ)</span><span class="sxs-lookup"><span data-stu-id="5ec05-141">LookupContent (Group)</span></span>

        - <span data-ttu-id="5ec05-142">グリッド | ツリー | ListView</span><span class="sxs-lookup"><span data-stu-id="5ec05-142">Grid | Tree | ListView</span></span>

    - <span data-ttu-id="5ec05-143">VerticalSplitter (Group)</span><span class="sxs-lookup"><span data-stu-id="5ec05-143">VerticalSplitter (Group)</span></span>

        - <span data-ttu-id="5ec05-144">プレビュー (グループ)</span><span class="sxs-lookup"><span data-stu-id="5ec05-144">Preview (Group)</span></span>

    - <span data-ttu-id="5ec05-145">LookupActions (ActionPane)</span><span class="sxs-lookup"><span data-stu-id="5ec05-145">LookupActions (ActionPane)</span></span>

### <a name="core-components"></a><span data-ttu-id="5ec05-146">コア コンポーネント</span><span class="sxs-lookup"><span data-stu-id="5ec05-146">Core components</span></span>

-   <span data-ttu-id="5ec05-147">Form.Design にルックアップ パターンを適用します。</span><span class="sxs-lookup"><span data-stu-id="5ec05-147">Apply the Lookup pattern on Form.Design.</span></span>
-   <span data-ttu-id="5ec05-148">BP 警告に対処します。</span><span class="sxs-lookup"><span data-stu-id="5ec05-148">Address BP Warnings:</span></span>
    -   <span data-ttu-id="5ec05-149">EDT.FormHelp は、Style=Lookup であるフォームを参照しなければなりません。</span><span class="sxs-lookup"><span data-stu-id="5ec05-149">EDT.FormHelp must reference a form where Style=Lookup.</span></span>

### <a name="commonly-used-subpatterns"></a><span data-ttu-id="5ec05-150">一般的に使用されるサブパターン</span><span class="sxs-lookup"><span data-stu-id="5ec05-150">Commonly used subpatterns</span></span>

-   [<span data-ttu-id="5ec05-151">カスタム フィルター グループ</span><span class="sxs-lookup"><span data-stu-id="5ec05-151">Custom Filter Group</span></span>](custom-filter-group-subpattern.md)

## <a name="ux-guidelines"></a><span data-ttu-id="5ec05-152">UX ガイドライン</span><span class="sxs-lookup"><span data-stu-id="5ec05-152">UX guidelines</span></span>
<span data-ttu-id="5ec05-153">検証チェックリストには、フォームが UX ガイドラインに準拠しているかどうかを手動で確認する手順が示されています。</span><span class="sxs-lookup"><span data-stu-id="5ec05-153">The verification checklist shows the steps for manually verifying that the form complies with UX guidelines.</span></span> <span data-ttu-id="5ec05-154">このチェックリストには、開発環境を通じて自動的に実施されるガイドラインは含まれていません。</span><span class="sxs-lookup"><span data-stu-id="5ec05-154">This checklist doesn't include any guidelines that will be enforced automatically through the development environment.</span></span> <span data-ttu-id="5ec05-155">ブラウザーでフォームを開いて、これらの手順を確認します。</span><span class="sxs-lookup"><span data-stu-id="5ec05-155">Open the form in a browser, and walk through these steps.</span></span> <span data-ttu-id="5ec05-156">**標準フォーム ガイドライン**</span><span class="sxs-lookup"><span data-stu-id="5ec05-156">**Standard form guidelines**</span></span>

-   <span data-ttu-id="5ec05-157">標準フォーム ガイドラインは、[全般的なガイドライン](general-form-guidelines.md) ドキュメントに統合されました。</span><span class="sxs-lookup"><span data-stu-id="5ec05-157">Standard form guidelines have been consolidated into the [General Form Guidelines](general-form-guidelines.md) document.</span></span>

<span data-ttu-id="5ec05-158">**ルックアップのガイドライン**</span><span class="sxs-lookup"><span data-stu-id="5ec05-158">**Lookup guidelines**</span></span>

-   <span data-ttu-id="5ec05-159">**グリッド**ガイドラインは、グリッドガイドライン セクションの [フォームの全般的なガイドライン](general-form-guidelines.md) ドキュメントに統合されました。</span><span class="sxs-lookup"><span data-stu-id="5ec05-159">**Grid** guidelines have been consolidated into the [General Form Guidelines ](general-form-guidelines.md) document, in the Grid guidelines section.</span></span>
-   <span data-ttu-id="5ec05-160">ルックアップ内に別の「ビュー」(タブ) を表示する必要がある場合は、コンボ ボックスを使用して、ユーザーがタブを切り替えるようにします。</span><span class="sxs-lookup"><span data-stu-id="5ec05-160">If you must show different “views” (tabs) within the lookup, use a combo box to let the user to switch between tabs.</span></span>
-   <span data-ttu-id="5ec05-161">必要に応じてルックアップでツリー ビューを使用することができます。</span><span class="sxs-lookup"><span data-stu-id="5ec05-161">You can optionally use a tree view in the lookup.</span></span> <span data-ttu-id="5ec05-162">また、ツリー内のデータの追加フィールドの表示が複雑であるため、標準のグリッドを提供することも検討します。</span><span class="sxs-lookup"><span data-stu-id="5ec05-162">Also consider providing a standard grid because of the complexity that is involved in showing additional fields of data in a tree.</span></span>
-   <span data-ttu-id="5ec05-163">グリッドに 5 つ以上の列を持たないでください。</span><span class="sxs-lookup"><span data-stu-id="5ec05-163">Don't have more than five columns in the grid.</span></span> <span data-ttu-id="5ec05-164">ルックアップはすべての列を表示するようにサイズ変更されるので、5 列は非常に広いです。</span><span class="sxs-lookup"><span data-stu-id="5ec05-164">The lookup resizes to show all columns, so five columns is very wide.</span></span>
-   <span data-ttu-id="5ec05-165">**オプション プレビュー領域**:</span><span class="sxs-lookup"><span data-stu-id="5ec05-165">The **optional preview area**:</span></span>
    -   <span data-ttu-id="5ec05-166">領域は、ユーザーが複数の類似レコードから選択する場合に役立ちます。</span><span class="sxs-lookup"><span data-stu-id="5ec05-166">The area should help the user choose between two or more records that are similar.</span></span> <span data-ttu-id="5ec05-167">たとえば、John Smith という名前の 2 人の従業員がいる場合、プレビューはこれら 2 人をユーザーが区別できるよう、十分な情報を提供する必要があります。</span><span class="sxs-lookup"><span data-stu-id="5ec05-167">For example, if you have two employees who are named John Smith, the preview should provide enough information to help the user differentiate these two people.</span></span>
    -   <span data-ttu-id="5ec05-168">プレビューでは編集可能なフィールドを表示しないでください。</span><span class="sxs-lookup"><span data-stu-id="5ec05-168">Don't show editable fields in the preview.</span></span>
-   <span data-ttu-id="5ec05-169">**カスタム フィルター** ガイドラインは [カスタム フィルター グループ](custom-filter-group-subpattern.md) サブパターン ドキュメントに統合されています。</span><span class="sxs-lookup"><span data-stu-id="5ec05-169">**Custom filter** guidelines have been consolidated into the [Custom Filter Group](custom-filter-group-subpattern.md) subpattern document.</span></span>

## <a name="examples"></a><span data-ttu-id="5ec05-170">例</span><span class="sxs-lookup"><span data-stu-id="5ec05-170">Examples</span></span>
### <a name="lookup-basic"></a><span data-ttu-id="5ec05-171">基本のルックアップ</span><span class="sxs-lookup"><span data-stu-id="5ec05-171">Lookup basic</span></span>

<span data-ttu-id="5ec05-172">フォーム: **SysLanguageLookup** (ナビゲーション バーで**設定** &gt; **ユーザー設定**をクリックします。)</span><span class="sxs-lookup"><span data-stu-id="5ec05-172">Form: **SysLanguageLookup** (Click **Settings** &gt; **User settings** on the navigation bar.)</span></span> 

<span data-ttu-id="5ec05-173">[![基本ルックアップの例](./media/lookupform4.png)](./media/lookupform4.png)</span><span class="sxs-lookup"><span data-stu-id="5ec05-173">[![Example of basic lookup](./media/lookupform4.png)](./media/lookupform4.png)</span></span>

### <a name="lookup-with-tabs"></a><span data-ttu-id="5ec05-174">タブ付きルックアップ</span><span class="sxs-lookup"><span data-stu-id="5ec05-174">Lookup with tabs</span></span>

<span data-ttu-id="5ec05-175">フォーム: **CaseCategoryLookup** (**共通** &gt; **共通** &gt; **ケース** &gt; **すべてのケース**の順にクリックして、詳細に移動するケースを選択します。)</span><span class="sxs-lookup"><span data-stu-id="5ec05-175">Form: **CaseCategoryLookup** (Click **Common** &gt; **Common** &gt; **Cases** &gt; **All cases**, and then select a case to go to the details.)</span></span> 

![タブ付きルックアップ フォームの例](./media/lookupform5.png)

### <a name="lookup-with-preview"></a><span data-ttu-id="5ec05-177">プレビューによるルックアップ</span><span class="sxs-lookup"><span data-stu-id="5ec05-177">Lookup with preview</span></span>

<span data-ttu-id="5ec05-178">フォーム: **HcmWorkerLookup** (**人事管理** &gt; **共通** &gt; **組織** &gt; **職位** &gt; **職位**の順にクリックし、詳細に移動するレコードをクリックします。</span><span class="sxs-lookup"><span data-stu-id="5ec05-178">Form: **HcmWorkerLookup** (Click **Human resources** &gt; **Common** &gt; **Organization** &gt; **Positions** &gt; **Positions**, and then click a record to go to the details.</span></span> <span data-ttu-id="5ec05-179">**作業者の割り当て** FastTab を展開し、**新規**をクリックして、次に**ワーカー**フィールドにドロップダウンの矢印をクリックします。</span><span class="sxs-lookup"><span data-stu-id="5ec05-179">Expand the **Worker assignment** FastTab, click **New**, and then click the drop-down arrow in the **Worker** field.)</span></span> 

<span data-ttu-id="5ec05-180">[![プレビューによるルックアップ フォームの例](./media/lookupform6.png)](./media/lookupform6.png)</span><span class="sxs-lookup"><span data-stu-id="5ec05-180">[![Example of lookup form with preview](./media/lookupform6.png)](./media/lookupform6.png)</span></span>

## <a name="appendix"></a><span data-ttu-id="5ec05-181">付録</span><span class="sxs-lookup"><span data-stu-id="5ec05-181">Appendix</span></span>
### <a name="frequently-asked-questions"></a><span data-ttu-id="5ec05-182">よく寄せられる質問</span><span class="sxs-lookup"><span data-stu-id="5ec05-182">Frequently asked questions</span></span>

<span data-ttu-id="5ec05-183">このセクションには、このガイドライン/パターンに関連するよくある質問への回答があります。</span><span class="sxs-lookup"><span data-stu-id="5ec05-183">This section will have answers to frequently asked questions that are related to this guideline/pattern.</span></span>

-   <span data-ttu-id="5ec05-184">**タブ付きのルックアップ パターンのタブを切り替える方法。**</span><span class="sxs-lookup"><span data-stu-id="5ec05-184">**How do I switch between tabs in the Lookup w/tabs pattern?**</span></span>
    -   <span data-ttu-id="5ec05-185">タブ付きルックアップ パターンは、Tab コントロールで **ShowTabs** を **No** に意図的に設定します。</span><span class="sxs-lookup"><span data-stu-id="5ec05-185">The Lookup w/tabs pattern intentionally sets **ShowTabs** to **No** on the Tab control.</span></span> <span data-ttu-id="5ec05-186">これらのフォームは、カスタム フィルター グループ内のバインドされていないコンボ ボックスをモデル化するためのものです。</span><span class="sxs-lookup"><span data-stu-id="5ec05-186">These forms are meant to model an unbound combo box in the custom filter group.</span></span> <span data-ttu-id="5ec05-187">このコンボ ボックスは、タブ ヘッダーの代わりにタブを切り替えるために使用されます。</span><span class="sxs-lookup"><span data-stu-id="5ec05-187">This combo box is used instead of tab headers to switch tabs.</span></span>
    -   <span data-ttu-id="5ec05-188">これを行うには、次の手順に従います。</span><span class="sxs-lookup"><span data-stu-id="5ec05-188">To do this, follow these steps:</span></span>
        1.  <span data-ttu-id="5ec05-189">フォーム **run()** の **SysLookup::tab2ComboBox** メソッド転記 **super** を呼び出し、コンボ ボックスにルックアップに表示されているタブからキャプションを設定します。</span><span class="sxs-lookup"><span data-stu-id="5ec05-189">Call the **SysLookup::tab2ComboBox** method post **super** in form **run()** to populate the combo box with captions from visible tabs in the lookup.</span></span>

                // Generate view combobox based on tabs
                tab2ComboBoxItemMap = SysLookup::tab2ComboBox(Tab, switchView);

        2.  <span data-ttu-id="5ec05-190">コンボ ボックスで **modified()** をオーバーライドし、コンボ ボックスで選択した値に基づいて表示されるタブを更新します。</span><span class="sxs-lookup"><span data-stu-id="5ec05-190">Override **modified()** on the combo box to update the visible tab, based on the selected value in the combo box.</span></span>

                Tab.tabChanged(Tab.tabValue(), tab2ComboBoxItemMap.lookup(this.selection()));

### <a name="open-issues"></a><span data-ttu-id="5ec05-191">未処理の問題</span><span class="sxs-lookup"><span data-stu-id="5ec05-191">Open issues</span></span>

-   <span data-ttu-id="5ec05-192">**最近使用した値をルックアップに組み込むことはできますか。**</span><span class="sxs-lookup"><span data-stu-id="5ec05-192">**Can we incorporate the most recently used values into lookups?**</span></span>
    -   <span data-ttu-id="5ec05-193">アプリのモデリングは、今すぐこの作業を行うことができます (通貨のルックアップなど)。</span><span class="sxs-lookup"><span data-stu-id="5ec05-193">App modeling can make this work right now (for example, the Currency lookup).</span></span> <span data-ttu-id="5ec05-194">この機能の全般的なフレームワークの今後のサポートを検討しています。</span><span class="sxs-lookup"><span data-stu-id="5ec05-194">We are considering general framework support for this feature in the future.</span></span>

### <a name="ax-2012-content"></a><span data-ttu-id="5ec05-195">AX 2012 コンテンツ</span><span class="sxs-lookup"><span data-stu-id="5ec05-195">AX 2012 content</span></span>

<span data-ttu-id="5ec05-196">**SysLanguageLookup (基本のルックアップ)**</span><span class="sxs-lookup"><span data-stu-id="5ec05-196">**SysLanguageLookup (Lookup basic)**</span></span> 

![基本ルックアップ フォームの例](./media/lookupform7.png) 

<span data-ttu-id="5ec05-198">**CaseCategoryLookup (タブ付きルックアップ)**</span><span class="sxs-lookup"><span data-stu-id="5ec05-198">**CaseCategoryLookup (Lookup with tabs)**</span></span> 

<span data-ttu-id="5ec05-199">[![タブ付きルックアップ フォームの例](./media/lookupform8.png)](./media/lookupform8.png)</span><span class="sxs-lookup"><span data-stu-id="5ec05-199">[![Example of lookup form with tabs](./media/lookupform8.png)](./media/lookupform8.png)</span></span> 

<span data-ttu-id="5ec05-200">**HcmWorkerLookup (プレビューによるルックアップ)**</span><span class="sxs-lookup"><span data-stu-id="5ec05-200">**HcmWorkerLookup (Lookup with preview)**</span></span> 

![プレビューによるルックアップ フォームの例](./media/lookupform9.png)