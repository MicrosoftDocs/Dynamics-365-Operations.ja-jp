---
title: カスタム フィルター グループのサブパターン
description: このトピックでは、カスタム フィルター グループのサブパターンについて説明します。
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
ms.custom: 28231
ms.assetid: 1838c10d-9172-4853-aa49-17710adf8bc1
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 936c6ea31f5daf2d4f45c28bbf371c88190dd0e9
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 05/07/2019
ms.locfileid: "1537178"
---
# <a name="custom-filter-group-subpattern"></a><span data-ttu-id="a6526-103">カスタム フィルター グループのサブパターン</span><span class="sxs-lookup"><span data-stu-id="a6526-103">Custom Filter Group subpattern</span></span>

[!include [banner](../includes/banner.md)]

<a name="usage"></a><span data-ttu-id="a6526-104">用途</span><span class="sxs-lookup"><span data-stu-id="a6526-104">Usage</span></span>
-----

<span data-ttu-id="a6526-105">このサブパターンは、グリッド セクションまたはフォーム セクションにカスタム フィルターを適用する小規模 (5 つ未満) の入力コントロールのコレクションを表示するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="a6526-105">This subpattern is used to show a small collection of input controls (no more than five) that apply a custom filter to a grid or form section.</span></span> <span data-ttu-id="a6526-106">カスタム フィルター グループのフィールドは次のフィールド タイプに限定される必要があり、それは入力の制約があり、クエリに適用されるというものです。</span><span class="sxs-lookup"><span data-stu-id="a6526-106">Fields in the Custom Filter Group should be limited to the following field types, which have constrained inputs and can be applied to the query:</span></span>

-   <span data-ttu-id="a6526-107">Lookups を使用した StringEdits</span><span class="sxs-lookup"><span data-stu-id="a6526-107">StringEdits with Lookups</span></span>
-   <span data-ttu-id="a6526-108">日付フィールド</span><span class="sxs-lookup"><span data-stu-id="a6526-108">Date fields</span></span>
-   <span data-ttu-id="a6526-109">ReferenceGroup</span><span class="sxs-lookup"><span data-stu-id="a6526-109">ReferenceGroup</span></span>
-   <span data-ttu-id="a6526-110">Comboboxes</span><span class="sxs-lookup"><span data-stu-id="a6526-110">Comboboxes</span></span>
-   <span data-ttu-id="a6526-111">チェック ボックス</span><span class="sxs-lookup"><span data-stu-id="a6526-111">Checkboxes</span></span>
-   <span data-ttu-id="a6526-112">クイック フィルター</span><span class="sxs-lookup"><span data-stu-id="a6526-112">Quick Filter</span></span>

<span data-ttu-id="a6526-113">このドキュメントでは、2 つのパターンについて説明します。</span><span class="sxs-lookup"><span data-stu-id="a6526-113">Two patterns are described in this document.</span></span> <span data-ttu-id="a6526-114">これらのパターンの唯一の違いは、クイック フィルター コントロールが必須かオプションかです。</span><span class="sxs-lookup"><span data-stu-id="a6526-114">The only difference between these patterns is whether the Quick Filter control is mandatory or optional:</span></span>

-   <span data-ttu-id="a6526-115">**カスタム フィルター**  – このサブパターンでは、QuickFilter コントロールはオプションです。</span><span class="sxs-lookup"><span data-stu-id="a6526-115">**Custom Filters** – In this subpattern, the QuickFilter control is optional.</span></span>
-   <span data-ttu-id="a6526-116">**カスタムおよびクイック フィルター**  – このサブパターンでは、QuickFilter コントロールは必須です。</span><span class="sxs-lookup"><span data-stu-id="a6526-116">**Custom and Quick Filters** – In this subpattern, the QuickFilter control is mandatory.</span></span>

## <a name="wireframes"></a><span data-ttu-id="a6526-117">ワイヤーフレーム</span><span class="sxs-lookup"><span data-stu-id="a6526-117">Wireframes</span></span>
### <a name="custom-filterscustomfiltergroup1mediacustomfiltergroup1pngmediacustomfiltergroup1png"></a><span data-ttu-id="a6526-118">カスタム フィルター [![CustomFilterGroup(1)](./media/customfiltergroup1.png)](./media/customfiltergroup1.png)</span><span class="sxs-lookup"><span data-stu-id="a6526-118">Custom Filters[![CustomFilterGroup(1)](./media/customfiltergroup1.png)](./media/customfiltergroup1.png)</span></span>

### <a name="custom-and-quick-filters"></a><span data-ttu-id="a6526-119">カスタムおよびクイック フィルター</span><span class="sxs-lookup"><span data-stu-id="a6526-119">Custom and Quick Filters</span></span>

![CustomFilterGroup(2)](./media/customfiltergroup2.png)

## <a name="model"></a><span data-ttu-id="a6526-121">モデル</span><span class="sxs-lookup"><span data-stu-id="a6526-121">Model</span></span>
### <a name="custom-filters-high-level-structure"></a><span data-ttu-id="a6526-122">カスタム フィルタ – 高レベルの構造</span><span class="sxs-lookup"><span data-stu-id="a6526-122">Custom Filters – High-level structure</span></span>

- <span data-ttu-id="a6526-123">CustomFilter (グループ)</span><span class="sxs-lookup"><span data-stu-id="a6526-123">CustomFilter (Group)</span></span>

    - <span data-ttu-id="a6526-124">*QuickFilter (QuickFilter) \[オプション\]*</span><span class="sxs-lookup"><span data-stu-id="a6526-124">*QuickFilter (QuickFilter) \[Optional\]*</span></span>
    - <span data-ttu-id="a6526-125">*フィールド グループ (グループ)\[0..N\]*</span><span class="sxs-lookup"><span data-stu-id="a6526-125">*FieldGroups (Group) \[0..N\]*</span></span>

        - <span data-ttu-id="a6526-126">フィールド ($Field) \[1..N\]</span><span class="sxs-lookup"><span data-stu-id="a6526-126">Fields ($Field) \[1..N\]</span></span>

    - <span data-ttu-id="a6526-127">*フィールド ($ フィールド)\[0..N\]*</span><span class="sxs-lookup"><span data-stu-id="a6526-127">*Fields ($Fields) \[0..N\]*</span></span>

### <a name="custom-and-quick-filters-high-level-structure"></a><span data-ttu-id="a6526-128">カスタムおよびクイック フィルター – 高レベルの構造</span><span class="sxs-lookup"><span data-stu-id="a6526-128">Custom and Quick Filters – High-level structure</span></span>

- <span data-ttu-id="a6526-129">CustomFilter (グループ)</span><span class="sxs-lookup"><span data-stu-id="a6526-129">CustomFilter (Group)</span></span>

    - <span data-ttu-id="a6526-130">QuickFilter (QuickFilter)</span><span class="sxs-lookup"><span data-stu-id="a6526-130">QuickFilter (QuickFilter)</span></span>
    - <span data-ttu-id="a6526-131">*フィールド グループ (グループ)\[0..N\]*</span><span class="sxs-lookup"><span data-stu-id="a6526-131">*FieldGroups (Group) \[0..N\]*</span></span>

        - <span data-ttu-id="a6526-132">フィールド ($Field) \[1..N\]</span><span class="sxs-lookup"><span data-stu-id="a6526-132">Fields ($Field) \[1..N\]</span></span>

    - <span data-ttu-id="a6526-133">*フィールド ($ フィールド)\[0..N\]*</span><span class="sxs-lookup"><span data-stu-id="a6526-133">*Fields ($Fields) \[0..N\]*</span></span>

### <a name="core-components"></a><span data-ttu-id="a6526-134">コア コンポーネント</span><span class="sxs-lookup"><span data-stu-id="a6526-134">Core components</span></span>

-   <span data-ttu-id="a6526-135">カスタム フィルター コンテナー パターンをグループ コントロールに適用します。</span><span class="sxs-lookup"><span data-stu-id="a6526-135">Apply a custom filter-container pattern to a Group control.</span></span>
-   <span data-ttu-id="a6526-136">BP 警告に対処します。</span><span class="sxs-lookup"><span data-stu-id="a6526-136">Address BP Warnings:</span></span>
    -   <span data-ttu-id="a6526-137">CustomFilterGroup 内の入力コントロールに DataSource または DataField を割り当てられません。</span><span class="sxs-lookup"><span data-stu-id="a6526-137">Input controls within the CustomFilterGroup should not have a DataSource or DataField assigned.</span></span>

### <a name="related-container-patterns"></a><span data-ttu-id="a6526-138">関連するコンテナー パターン</span><span class="sxs-lookup"><span data-stu-id="a6526-138">Related container patterns</span></span>

<span data-ttu-id="a6526-139">None</span><span class="sxs-lookup"><span data-stu-id="a6526-139">None</span></span>

### <a name="related-modeling"></a><span data-ttu-id="a6526-140">関連するモデリング</span><span class="sxs-lookup"><span data-stu-id="a6526-140">Related modeling</span></span>

<span data-ttu-id="a6526-141">すべてのカスタム フィルターに QueryBuildRange ではなく QueryFilter を使用します。</span><span class="sxs-lookup"><span data-stu-id="a6526-141">Use QueryFilter, not QueryBuildRange, for all custom filters.</span></span> <span data-ttu-id="a6526-142">QueryBuildRange は、外側の結合フィールドでは正しく動作しません。</span><span class="sxs-lookup"><span data-stu-id="a6526-142">QueryBuildRange doesn't work correctly with outer-joined fields.</span></span>

## <a name="ux-guidelines"></a><span data-ttu-id="a6526-143">UX ガイドライン</span><span class="sxs-lookup"><span data-stu-id="a6526-143">UX guidelines</span></span>
<span data-ttu-id="a6526-144">検証チェックリストには、フォームが UX ガイドラインに準拠しているかどうかを手動で確認する手順が示されています。</span><span class="sxs-lookup"><span data-stu-id="a6526-144">The verification checklist shows the steps for manually verifying that the form complies with UX guidelines.</span></span> <span data-ttu-id="a6526-145">このチェックリストには、開発環境を通じて自動的に実施されるガイドラインは含まれていません。</span><span class="sxs-lookup"><span data-stu-id="a6526-145">This checklist doesn't include any guidelines that will be enforced automatically through the development environment.</span></span> <span data-ttu-id="a6526-146">ブラウザーでフォームを開いて、これらの手順を確認します。</span><span class="sxs-lookup"><span data-stu-id="a6526-146">Open the form in a browser, and walk through these steps.</span></span>

-   <span data-ttu-id="a6526-147">**標準フォーム ガイドライン:**</span><span class="sxs-lookup"><span data-stu-id="a6526-147">**Standard form guidelines:**</span></span>
    -   [<span data-ttu-id="a6526-148">フォームの全般的なガイドライン</span><span class="sxs-lookup"><span data-stu-id="a6526-148">General form guidelines</span></span>](general-form-guidelines.md)
-   <span data-ttu-id="a6526-149">**カスタム フィルター グループのガイドライン**</span><span class="sxs-lookup"><span data-stu-id="a6526-149">**Custom Filter Group guidelines:**</span></span>
    -   <span data-ttu-id="a6526-150">すべてのコントロール (QuickFilter を除く) は制約された入力コントロールです。</span><span class="sxs-lookup"><span data-stu-id="a6526-150">All controls (except QuickFilter) are constrained input controls.</span></span> <span data-ttu-id="a6526-151">文字列、整数、および実数などの、自由回答式のコントロールを使用しないでください。</span><span class="sxs-lookup"><span data-stu-id="a6526-151">Open-ended controls, such as strings, integers, and reals, should not be used.</span></span>
    -   <span data-ttu-id="a6526-152">フィールド ラベルは、容量を節約するようオフになっています。</span><span class="sxs-lookup"><span data-stu-id="a6526-152">Field labels are turned off to save space.</span></span> <span data-ttu-id="a6526-153">たとえば、**未処理**、**終了済**、**転記済**、およびすべての値を持つコンボボックスに対して、ラベルは必要ありません。</span><span class="sxs-lookup"><span data-stu-id="a6526-153">For example, no label is needed for a combobox that has the values **Open**, **Closed**, **Posted**, and All.</span></span>
        -   <span data-ttu-id="a6526-154">ユーザーがフィルターの動作を理解するための十分なコンテキストをフィルター値が提供していない場合は、ラベルを表示します。</span><span class="sxs-lookup"><span data-stu-id="a6526-154">Show labels when the filter values do not provide sufficient context for the user to understand what the filter does.</span></span> <span data-ttu-id="a6526-155">たとえば、日付フィールドにはコンテキストがなく、ユーザーがどのタイプの日付が指定されているか (たとえば、**作成日**) を理解するためのラベルを必要とします。</span><span class="sxs-lookup"><span data-stu-id="a6526-155">For example, a date field provides no context, and the user requires a label to understand what type of date is specified (for example, **Created date**).</span></span>
        -   <span data-ttu-id="a6526-156">すべてのラベルがオフになるか、またはオンになるかです。</span><span class="sxs-lookup"><span data-stu-id="a6526-156">Either all labels are turned off, or all labels are turned on.</span></span> <span data-ttu-id="a6526-157">ラベルが付いていないフィルターおよびラベルの付いたフィルターを混在させないでください。</span><span class="sxs-lookup"><span data-stu-id="a6526-157">Don't mix unlabeled filters and labeled filters.</span></span>
        -   <span data-ttu-id="a6526-158">**例外:** チェック ボックス スタイルのブール値を使用すると、他のフィールドにラベルが表示されていなくても、ラベルを残すことができます。</span><span class="sxs-lookup"><span data-stu-id="a6526-158">**Exception:** When you use a check box–style Boolean, the label can be left on, even though other fields don't show a label.</span></span>
    -   <span data-ttu-id="a6526-159">カスタム フィルター グループに配置するコントロールは 5 つ以下にしてください。</span><span class="sxs-lookup"><span data-stu-id="a6526-159">There should not be more than five controls in the custom filter group.</span></span>

## <a name="examples"></a><span data-ttu-id="a6526-160">例</span><span class="sxs-lookup"><span data-stu-id="a6526-160">Examples</span></span>
### <a name="custom-filters"></a><span data-ttu-id="a6526-161">カスタム フィルター</span><span class="sxs-lookup"><span data-stu-id="a6526-161">Custom Filters</span></span>

<span data-ttu-id="a6526-162">フォーム: **LedgerJournalTable (TopFields)**</span><span class="sxs-lookup"><span data-stu-id="a6526-162">Form: **LedgerJournalTable (TopFields)**</span></span> 

![CustomFilterGroup(3)](./media/customfiltergroup3.png)

### <a name="custom-and-quick-filters"></a><span data-ttu-id="a6526-164">カスタムおよびクイック フィルター</span><span class="sxs-lookup"><span data-stu-id="a6526-164">Custom and Quick Filters</span></span>

<span data-ttu-id="a6526-165">フォーム: **CustTable** **(CustomFilterGroup)**</span><span class="sxs-lookup"><span data-stu-id="a6526-165">Form: **CustTable** **(CustomFilterGroup)**</span></span> 

<span data-ttu-id="a6526-166">[![CustomFilterGroup(4)](./media/customfiltergroup4.png)](./media/customfiltergroup4.png)</span><span class="sxs-lookup"><span data-stu-id="a6526-166">[![CustomFilterGroup(4)](./media/customfiltergroup4.png)](./media/customfiltergroup4.png)</span></span>

## <a name="resources"></a><span data-ttu-id="a6526-167">リソース</span><span class="sxs-lookup"><span data-stu-id="a6526-167">Resources</span></span>
### <a name="typically-used-by-form-patterns"></a><span data-ttu-id="a6526-168">通常、フォームのパターンによって使用される</span><span class="sxs-lookup"><span data-stu-id="a6526-168">Typically used by form patterns</span></span>

-   <span data-ttu-id="a6526-169">簡易リスト</span><span class="sxs-lookup"><span data-stu-id="a6526-169">Simple List</span></span>
-   <span data-ttu-id="a6526-170">詳細マスター</span><span class="sxs-lookup"><span data-stu-id="a6526-170">Details Master</span></span>
-   <span data-ttu-id="a6526-171">詳細トランザクション</span><span class="sxs-lookup"><span data-stu-id="a6526-171">Details Transaction</span></span>
-   <span data-ttu-id="a6526-172">リスト ページ</span><span class="sxs-lookup"><span data-stu-id="a6526-172">List Page</span></span>

## <a name="appendix"></a><span data-ttu-id="a6526-173">付録</span><span class="sxs-lookup"><span data-stu-id="a6526-173">Appendix</span></span>
### <a name="frequently-asked-questions"></a><span data-ttu-id="a6526-174">よく寄せられる質問</span><span class="sxs-lookup"><span data-stu-id="a6526-174">Frequently asked questions</span></span>

<span data-ttu-id="a6526-175">このセクションには、このガイドライン/パターンに関連するよくある質問への回答があります。</span><span class="sxs-lookup"><span data-stu-id="a6526-175">This section will have answers to frequently asked questions that are related to this guideline/pattern.</span></span>

-   <span data-ttu-id="a6526-176">**法人には、何をすればいいですか?**</span><span class="sxs-lookup"><span data-stu-id="a6526-176">**What do I do with the legal entity?**</span></span>
    -   <span data-ttu-id="a6526-177">「法人」は、カスタム フィルター グループに属する典型的なカスタム フィルターです。</span><span class="sxs-lookup"><span data-stu-id="a6526-177">“Legal entity” is a typical custom filter that belongs in the Custom Filter Group.</span></span>
-   <span data-ttu-id="a6526-178">**カスタム フィルターはリストのツールバーの上に置く必要がありますか。**</span><span class="sxs-lookup"><span data-stu-id="a6526-178">**Should the custom filter be above the toolbar of a list?**</span></span>
    -   <span data-ttu-id="a6526-179">カスタム フィルターは、ツールバーのコマンドと同様にリストにより直接影響を与えるため、可能な限りグリッドの近くに属するものと考えています。</span><span class="sxs-lookup"><span data-stu-id="a6526-179">We think that the custom filter belongs as close to the grid as possible, because it more directly affects the list, just as the commands in the toolbar do.</span></span> <span data-ttu-id="a6526-180">また、この位置は、異なるページ パターンにわたって要素の一貫した論理的な順序にします。</span><span class="sxs-lookup"><span data-stu-id="a6526-180">Additionally, this position makes the logical order of the elements consistent across different page patterns.</span></span>

### <a name="open-issues"></a><span data-ttu-id="a6526-181">未処理の問題</span><span class="sxs-lookup"><span data-stu-id="a6526-181">Open issues</span></span>

-   <span data-ttu-id="a6526-182">**カスタム フィルター グループに詳細表示/簡易表示を許可していますか。例: BudgetAnalysisInquiry\_PSN**</span><span class="sxs-lookup"><span data-stu-id="a6526-182">**Do we allow Show More/Less in the Custom Filter Group? An example is BudgetAnalysisInquiry\_PSN.**</span></span>
    -   <span data-ttu-id="a6526-183">いいえ、現在それはカスタム コンテナーになります。</span><span class="sxs-lookup"><span data-stu-id="a6526-183">No, that will currently be a custom container.</span></span> <span data-ttu-id="a6526-184">十分な例を行う場合は、新しいコンテナー サブパターンを追加する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="a6526-184">If we have enough examples, we might add a new container subpattern.</span></span>
-   <span data-ttu-id="a6526-185">**パターンは制約付き入力値を許可する入力可能タイプを制限しますか。**</span><span class="sxs-lookup"><span data-stu-id="a6526-185">**Does the pattern limit the possible input types to those that allow constrained input values?**</span></span>
    -   <span data-ttu-id="a6526-186">このパターンは現在のところどの入力も受け入れますが、値に制約のない入力はガイドラインに反します。</span><span class="sxs-lookup"><span data-stu-id="a6526-186">The pattern currently allows any input, but it's against guidelines to have inputs that have unconstrained values.</span></span>
-   <span data-ttu-id="a6526-187">**グループをカスタム フィルター グループとして使用できるようにしますか。**</span><span class="sxs-lookup"><span data-stu-id="a6526-187">**Do we allow groups to be used as custom filter groups?**</span></span>
    -   <span data-ttu-id="a6526-188">移行を容易にするとともに、カスタム フィルター グループの場所を特定できるようにしました。</span><span class="sxs-lookup"><span data-stu-id="a6526-188">We do allow them now, to make migration easier and to identify Custom Filter group locations.</span></span> <span data-ttu-id="a6526-189">ただし、これらの状況でフィールドの小さなセットのみを使用することをお勧めします (および最終的にはこれを強制する場合があります)。</span><span class="sxs-lookup"><span data-stu-id="a6526-189">However, we encourage you to use only a small set of fields in these situations (and we might eventually enforce this).</span></span>

### <a name="ax-2012-content"></a><span data-ttu-id="a6526-190">AX 2012 コンテンツ</span><span class="sxs-lookup"><span data-stu-id="a6526-190">AX 2012 content</span></span>

#### <a name="ax-2012-links"></a><span data-ttu-id="a6526-191">AX 2012 リンク</span><span class="sxs-lookup"><span data-stu-id="a6526-191">AX 2012 links</span></span>

-   [<span data-ttu-id="a6526-192">MSDN AX 2012 フィルター ウィンドウにコントロールを追加する方法</span><span class="sxs-lookup"><span data-stu-id="a6526-192">MSDN AX 2012 How to Add Controls to the Filter Pane</span></span>](http://msdn.microsoft.com/EN-US/library/cc577231.aspx)
-   [<span data-ttu-id="a6526-193">MSDN AX 2012 リスト ページの概要 – セクション フィルター ウィンドウ</span><span class="sxs-lookup"><span data-stu-id="a6526-193">MSDN AX 2012 List Page Overview – section Filter Pane</span></span>](http://msdn.microsoft.com/EN-US/library/cc616937.aspx)

#### <a name="ax-2012-example"></a><span data-ttu-id="a6526-194">AX 2012 の例</span><span class="sxs-lookup"><span data-stu-id="a6526-194">AX 2012 example</span></span>

<span data-ttu-id="a6526-195">[![CustomFilterGroup(5)](./media/customfiltergroup5.png)](./media/customfiltergroup5.png)</span><span class="sxs-lookup"><span data-stu-id="a6526-195">[![CustomFilterGroup(5)](./media/customfiltergroup5.png)](./media/customfiltergroup5.png)</span></span>
