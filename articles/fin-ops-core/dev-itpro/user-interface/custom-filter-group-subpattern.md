---
title: カスタム フィルター グループのサブパターン
description: このトピックでは、カスタム フィルター グループのサブパターンについて説明します。
author: jasongre
manager: AnnBe
ms.date: 04/22/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: sericks
ms.search.scope: Operations
ms.custom: 28231
ms.assetid: 1838c10d-9172-4853-aa49-17710adf8bc1
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 71d873741b9df57a612831812406b07976f09416
ms.sourcegitcommit: 6dd2a77cae05b5b634943e4f37b7cb33c7f1da15
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/22/2020
ms.locfileid: "3281526"
---
# <a name="custom-filter-group-subpattern"></a><span data-ttu-id="a98ab-103">カスタム フィルター グループのサブパターン</span><span class="sxs-lookup"><span data-stu-id="a98ab-103">Custom Filter Group subpattern</span></span>

[!include [banner](../includes/banner.md)]

<a name="usage"></a><span data-ttu-id="a98ab-104">用途</span><span class="sxs-lookup"><span data-stu-id="a98ab-104">Usage</span></span>
-----

<span data-ttu-id="a98ab-105">このサブパターンは、グリッド セクションまたはフォーム セクションにカスタム フィルターを適用する小規模 (5 つ未満) の入力コントロールのコレクションを表示するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="a98ab-105">This subpattern is used to show a small collection of input controls (no more than five) that apply a custom filter to a grid or form section.</span></span> <span data-ttu-id="a98ab-106">カスタム フィルター グループのフィールドは次のフィールド タイプに限定される必要があり、それは入力の制約があり、クエリに適用されるというものです。</span><span class="sxs-lookup"><span data-stu-id="a98ab-106">Fields in the Custom Filter Group should be limited to the following field types, which have constrained inputs and can be applied to the query:</span></span>

-   <span data-ttu-id="a98ab-107">Lookups を使用した StringEdits</span><span class="sxs-lookup"><span data-stu-id="a98ab-107">StringEdits with Lookups</span></span>
-   <span data-ttu-id="a98ab-108">日付フィールド</span><span class="sxs-lookup"><span data-stu-id="a98ab-108">Date fields</span></span>
-   <span data-ttu-id="a98ab-109">ReferenceGroup</span><span class="sxs-lookup"><span data-stu-id="a98ab-109">ReferenceGroup</span></span>
-   <span data-ttu-id="a98ab-110">Comboboxes</span><span class="sxs-lookup"><span data-stu-id="a98ab-110">Comboboxes</span></span>
-   <span data-ttu-id="a98ab-111">チェック ボックス</span><span class="sxs-lookup"><span data-stu-id="a98ab-111">Checkboxes</span></span>
-   <span data-ttu-id="a98ab-112">クイック フィルター</span><span class="sxs-lookup"><span data-stu-id="a98ab-112">Quick Filter</span></span>

<span data-ttu-id="a98ab-113">このドキュメントでは、2 つのパターンについて説明します。</span><span class="sxs-lookup"><span data-stu-id="a98ab-113">Two patterns are described in this document.</span></span> <span data-ttu-id="a98ab-114">これらのパターンの唯一の違いは、クイック フィルター コントロールが必須かオプションかです。</span><span class="sxs-lookup"><span data-stu-id="a98ab-114">The only difference between these patterns is whether the Quick Filter control is mandatory or optional:</span></span>

-   <span data-ttu-id="a98ab-115">**カスタム フィルター**  – このサブパターンでは、QuickFilter コントロールはオプションです。</span><span class="sxs-lookup"><span data-stu-id="a98ab-115">**Custom Filters** – In this subpattern, the QuickFilter control is optional.</span></span>
-   <span data-ttu-id="a98ab-116">**カスタムおよびクイック フィルター**  – このサブパターンでは、QuickFilter コントロールは必須です。</span><span class="sxs-lookup"><span data-stu-id="a98ab-116">**Custom and Quick Filters** – In this subpattern, the QuickFilter control is mandatory.</span></span>

## <a name="wireframes"></a><span data-ttu-id="a98ab-117">ワイヤーフレーム</span><span class="sxs-lookup"><span data-stu-id="a98ab-117">Wireframes</span></span>
### <a name="custom-filters"></a><span data-ttu-id="a98ab-118">カスタム フィルター</span><span class="sxs-lookup"><span data-stu-id="a98ab-118">Custom Filters</span></span>

<span data-ttu-id="a98ab-119">[![カスタム フィルター](./media/customfiltergroup1.png)](./media/customfiltergroup1.png)</span><span class="sxs-lookup"><span data-stu-id="a98ab-119">[![Custom Filters](./media/customfiltergroup1.png)](./media/customfiltergroup1.png)</span></span>

### <a name="custom-and-quick-filters"></a><span data-ttu-id="a98ab-120">カスタムおよびクイック フィルター</span><span class="sxs-lookup"><span data-stu-id="a98ab-120">Custom and Quick Filters</span></span>

![カスタムおよびクイック フィルター](./media/customfiltergroup2.png)

## <a name="model"></a><span data-ttu-id="a98ab-122">モデル</span><span class="sxs-lookup"><span data-stu-id="a98ab-122">Model</span></span>
### <a name="custom-filters-high-level-structure"></a><span data-ttu-id="a98ab-123">カスタム フィルタ – 高レベルの構造</span><span class="sxs-lookup"><span data-stu-id="a98ab-123">Custom Filters – High-level structure</span></span>

- <span data-ttu-id="a98ab-124">CustomFilter (グループ)</span><span class="sxs-lookup"><span data-stu-id="a98ab-124">CustomFilter (Group)</span></span>

    - <span data-ttu-id="a98ab-125">*QuickFilter (QuickFilter) \[オプション\]*</span><span class="sxs-lookup"><span data-stu-id="a98ab-125">*QuickFilter (QuickFilter) \[Optional\]*</span></span>
    - <span data-ttu-id="a98ab-126">*フィールド グループ (グループ)\[0..N\]*</span><span class="sxs-lookup"><span data-stu-id="a98ab-126">*FieldGroups (Group) \[0..N\]*</span></span>

        - <span data-ttu-id="a98ab-127">フィールド ($Field) \[1..N\]</span><span class="sxs-lookup"><span data-stu-id="a98ab-127">Fields ($Field) \[1..N\]</span></span>

    - <span data-ttu-id="a98ab-128">*フィールド ($ フィールド)\[0..N\]*</span><span class="sxs-lookup"><span data-stu-id="a98ab-128">*Fields ($Fields) \[0..N\]*</span></span>

### <a name="custom-and-quick-filters-high-level-structure"></a><span data-ttu-id="a98ab-129">カスタムおよびクイック フィルター – 高レベルの構造</span><span class="sxs-lookup"><span data-stu-id="a98ab-129">Custom and Quick Filters – High-level structure</span></span>

- <span data-ttu-id="a98ab-130">CustomFilter (グループ)</span><span class="sxs-lookup"><span data-stu-id="a98ab-130">CustomFilter (Group)</span></span>

    - <span data-ttu-id="a98ab-131">QuickFilter (QuickFilter)</span><span class="sxs-lookup"><span data-stu-id="a98ab-131">QuickFilter (QuickFilter)</span></span>
    - <span data-ttu-id="a98ab-132">*フィールド グループ (グループ)\[0..N\]*</span><span class="sxs-lookup"><span data-stu-id="a98ab-132">*FieldGroups (Group) \[0..N\]*</span></span>

        - <span data-ttu-id="a98ab-133">フィールド ($Field) \[1..N\]</span><span class="sxs-lookup"><span data-stu-id="a98ab-133">Fields ($Field) \[1..N\]</span></span>

    - <span data-ttu-id="a98ab-134">*フィールド ($ フィールド)\[0..N\]*</span><span class="sxs-lookup"><span data-stu-id="a98ab-134">*Fields ($Fields) \[0..N\]*</span></span>

### <a name="core-components"></a><span data-ttu-id="a98ab-135">コア コンポーネント</span><span class="sxs-lookup"><span data-stu-id="a98ab-135">Core components</span></span>

-   <span data-ttu-id="a98ab-136">カスタム フィルター コンテナー パターンをグループ コントロールに適用します。</span><span class="sxs-lookup"><span data-stu-id="a98ab-136">Apply a custom filter-container pattern to a Group control.</span></span>
-   <span data-ttu-id="a98ab-137">BP 警告に対処します。</span><span class="sxs-lookup"><span data-stu-id="a98ab-137">Address BP Warnings:</span></span>
    -   <span data-ttu-id="a98ab-138">CustomFilterGroup 内の入力コントロールに DataSource または DataField を割り当てられません。</span><span class="sxs-lookup"><span data-stu-id="a98ab-138">Input controls within the CustomFilterGroup should not have a DataSource or DataField assigned.</span></span>

### <a name="related-container-patterns"></a><span data-ttu-id="a98ab-139">関連するコンテナー パターン</span><span class="sxs-lookup"><span data-stu-id="a98ab-139">Related container patterns</span></span>

<span data-ttu-id="a98ab-140">None</span><span class="sxs-lookup"><span data-stu-id="a98ab-140">None</span></span>

### <a name="related-modeling"></a><span data-ttu-id="a98ab-141">関連するモデリング</span><span class="sxs-lookup"><span data-stu-id="a98ab-141">Related modeling</span></span>

<span data-ttu-id="a98ab-142">すべてのカスタム フィルターに QueryBuildRange ではなく QueryFilter を使用します。</span><span class="sxs-lookup"><span data-stu-id="a98ab-142">Use QueryFilter, not QueryBuildRange, for all custom filters.</span></span> <span data-ttu-id="a98ab-143">QueryBuildRange は、外側の結合フィールドでは正しく動作しません。</span><span class="sxs-lookup"><span data-stu-id="a98ab-143">QueryBuildRange doesn't work correctly with outer-joined fields.</span></span>

## <a name="ux-guidelines"></a><span data-ttu-id="a98ab-144">UX ガイドライン</span><span class="sxs-lookup"><span data-stu-id="a98ab-144">UX guidelines</span></span>
<span data-ttu-id="a98ab-145">検証チェックリストには、フォームが UX ガイドラインに準拠しているかどうかを手動で確認する手順が示されています。</span><span class="sxs-lookup"><span data-stu-id="a98ab-145">The verification checklist shows the steps for manually verifying that the form complies with UX guidelines.</span></span> <span data-ttu-id="a98ab-146">このチェックリストには、開発環境を通じて自動的に実施されるガイドラインは含まれていません。</span><span class="sxs-lookup"><span data-stu-id="a98ab-146">This checklist doesn't include any guidelines that will be enforced automatically through the development environment.</span></span> <span data-ttu-id="a98ab-147">ブラウザーでフォームを開いて、これらの手順を確認します。</span><span class="sxs-lookup"><span data-stu-id="a98ab-147">Open the form in a browser, and walk through these steps.</span></span>

-   <span data-ttu-id="a98ab-148">**標準フォーム ガイドライン:**</span><span class="sxs-lookup"><span data-stu-id="a98ab-148">**Standard form guidelines:**</span></span>
    -   [<span data-ttu-id="a98ab-149">フォームの全般的なガイドライン</span><span class="sxs-lookup"><span data-stu-id="a98ab-149">General form guidelines</span></span>](general-form-guidelines.md)
-   <span data-ttu-id="a98ab-150">**カスタム フィルター グループのガイドライン**</span><span class="sxs-lookup"><span data-stu-id="a98ab-150">**Custom Filter Group guidelines:**</span></span>
    -   <span data-ttu-id="a98ab-151">すべてのコントロール (QuickFilter を除く) は制約された入力コントロールです。</span><span class="sxs-lookup"><span data-stu-id="a98ab-151">All controls (except QuickFilter) are constrained input controls.</span></span> <span data-ttu-id="a98ab-152">文字列、整数、および実数などの、自由回答式のコントロールを使用しないでください。</span><span class="sxs-lookup"><span data-stu-id="a98ab-152">Open-ended controls, such as strings, integers, and reals, should not be used.</span></span>
    -   <span data-ttu-id="a98ab-153">フィールド ラベルは、容量を節約するようオフになっています。</span><span class="sxs-lookup"><span data-stu-id="a98ab-153">Field labels are turned off to save space.</span></span> <span data-ttu-id="a98ab-154">たとえば、**未処理**、**終了済**、**転記済**、およびすべての値を持つコンボボックスに対して、ラベルは必要ありません。</span><span class="sxs-lookup"><span data-stu-id="a98ab-154">For example, no label is needed for a combobox that has the values **Open**, **Closed**, **Posted**, and All.</span></span>
        -   <span data-ttu-id="a98ab-155">ユーザーがフィルターの動作を理解するための十分なコンテキストをフィルター値が提供していない場合は、ラベルを表示します。</span><span class="sxs-lookup"><span data-stu-id="a98ab-155">Show labels when the filter values do not provide sufficient context for the user to understand what the filter does.</span></span> <span data-ttu-id="a98ab-156">たとえば、日付フィールドにはコンテキストがなく、ユーザーがどのタイプの日付が指定されているか (たとえば、**作成日**) を理解するためのラベルを必要とします。</span><span class="sxs-lookup"><span data-stu-id="a98ab-156">For example, a date field provides no context, and the user requires a label to understand what type of date is specified (for example, **Created date**).</span></span>
        -   <span data-ttu-id="a98ab-157">すべてのラベルがオフになるか、またはオンになるかです。</span><span class="sxs-lookup"><span data-stu-id="a98ab-157">Either all labels are turned off, or all labels are turned on.</span></span> <span data-ttu-id="a98ab-158">ラベルが付いていないフィルターおよびラベルの付いたフィルターを混在させないでください。</span><span class="sxs-lookup"><span data-stu-id="a98ab-158">Don't mix unlabeled filters and labeled filters.</span></span>
        -   <span data-ttu-id="a98ab-159">**例外:** チェック ボックス スタイルのブール値を使用すると、他のフィールドにラベルが表示されていなくても、ラベルを残すことができます。</span><span class="sxs-lookup"><span data-stu-id="a98ab-159">**Exception:** When you use a check box–style Boolean, the label can be left on, even though other fields don't show a label.</span></span>
    -   <span data-ttu-id="a98ab-160">カスタム フィルター グループに配置するコントロールは 5 つ以下にしてください。</span><span class="sxs-lookup"><span data-stu-id="a98ab-160">There should not be more than five controls in the custom filter group.</span></span>

## <a name="examples"></a><span data-ttu-id="a98ab-161">例</span><span class="sxs-lookup"><span data-stu-id="a98ab-161">Examples</span></span>
### <a name="custom-filters"></a><span data-ttu-id="a98ab-162">カスタム フィルター</span><span class="sxs-lookup"><span data-stu-id="a98ab-162">Custom Filters</span></span>

<span data-ttu-id="a98ab-163">フォーム: **LedgerJournalTable (TopFields)**</span><span class="sxs-lookup"><span data-stu-id="a98ab-163">Form: **LedgerJournalTable (TopFields)**</span></span> 

![カスタム フィルター](./media/customfiltergroup3.png)

### <a name="custom-and-quick-filters"></a><span data-ttu-id="a98ab-165">カスタムおよびクイック フィルター</span><span class="sxs-lookup"><span data-stu-id="a98ab-165">Custom and Quick Filters</span></span>

<span data-ttu-id="a98ab-166">フォーム: **CustTable** **(CustomFilterGroup)**</span><span class="sxs-lookup"><span data-stu-id="a98ab-166">Form: **CustTable** **(CustomFilterGroup)**</span></span> 

<span data-ttu-id="a98ab-167">[![カスタムおよびクイック フィルター](./media/customfiltergroup4.png)](./media/customfiltergroup4.png)</span><span class="sxs-lookup"><span data-stu-id="a98ab-167">[![Custom and Quick Filters](./media/customfiltergroup4.png)](./media/customfiltergroup4.png)</span></span>

## <a name="resources"></a><span data-ttu-id="a98ab-168">リソース</span><span class="sxs-lookup"><span data-stu-id="a98ab-168">Resources</span></span>
### <a name="typically-used-by-form-patterns"></a><span data-ttu-id="a98ab-169">通常、フォームのパターンによって使用される</span><span class="sxs-lookup"><span data-stu-id="a98ab-169">Typically used by form patterns</span></span>

-   <span data-ttu-id="a98ab-170">簡易リスト</span><span class="sxs-lookup"><span data-stu-id="a98ab-170">Simple List</span></span>
-   <span data-ttu-id="a98ab-171">詳細マスター</span><span class="sxs-lookup"><span data-stu-id="a98ab-171">Details Master</span></span>
-   <span data-ttu-id="a98ab-172">詳細トランザクション</span><span class="sxs-lookup"><span data-stu-id="a98ab-172">Details Transaction</span></span>
-   <span data-ttu-id="a98ab-173">リスト ページ</span><span class="sxs-lookup"><span data-stu-id="a98ab-173">List Page</span></span>

## <a name="appendix"></a><span data-ttu-id="a98ab-174">付録</span><span class="sxs-lookup"><span data-stu-id="a98ab-174">Appendix</span></span>
### <a name="frequently-asked-questions"></a><span data-ttu-id="a98ab-175">よく寄せられる質問</span><span class="sxs-lookup"><span data-stu-id="a98ab-175">Frequently asked questions</span></span>

<span data-ttu-id="a98ab-176">このセクションには、このガイドライン/パターンに関連するよくある質問への回答があります。</span><span class="sxs-lookup"><span data-stu-id="a98ab-176">This section will have answers to frequently asked questions that are related to this guideline/pattern.</span></span>

-   <span data-ttu-id="a98ab-177">**法人には、何をすればいいですか?**</span><span class="sxs-lookup"><span data-stu-id="a98ab-177">**What do I do with the legal entity?**</span></span>
    -   <span data-ttu-id="a98ab-178">「法人」は、カスタム フィルター グループに属する典型的なカスタム フィルターです。</span><span class="sxs-lookup"><span data-stu-id="a98ab-178">“Legal entity” is a typical custom filter that belongs in the Custom Filter Group.</span></span>
-   <span data-ttu-id="a98ab-179">**カスタム フィルターはリストのツールバーの上に置く必要がありますか。**</span><span class="sxs-lookup"><span data-stu-id="a98ab-179">**Should the custom filter be above the toolbar of a list?**</span></span>
    -   <span data-ttu-id="a98ab-180">カスタム フィルターは、ツールバーのコマンドと同様にリストにより直接影響を与えるため、可能な限りグリッドの近くに属するものと考えています。</span><span class="sxs-lookup"><span data-stu-id="a98ab-180">We think that the custom filter belongs as close to the grid as possible, because it more directly affects the list, just as the commands in the toolbar do.</span></span> <span data-ttu-id="a98ab-181">また、この位置は、異なるページ パターンにわたって要素の一貫した論理的な順序にします。</span><span class="sxs-lookup"><span data-stu-id="a98ab-181">Additionally, this position makes the logical order of the elements consistent across different page patterns.</span></span>

### <a name="open-issues"></a><span data-ttu-id="a98ab-182">未処理の問題</span><span class="sxs-lookup"><span data-stu-id="a98ab-182">Open issues</span></span>

-   <span data-ttu-id="a98ab-183">**カスタム フィルター グループに詳細表示/簡易表示を許可していますか。例: BudgetAnalysisInquiry\_PSN**</span><span class="sxs-lookup"><span data-stu-id="a98ab-183">**Do we allow Show More/Less in the Custom Filter Group? An example is BudgetAnalysisInquiry\_PSN.**</span></span>
    -   <span data-ttu-id="a98ab-184">いいえ、現在それはカスタム コンテナーになります。</span><span class="sxs-lookup"><span data-stu-id="a98ab-184">No, that will currently be a custom container.</span></span> <span data-ttu-id="a98ab-185">十分な例を行う場合は、新しいコンテナー サブパターンを追加する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="a98ab-185">If we have enough examples, we might add a new container subpattern.</span></span>
-   <span data-ttu-id="a98ab-186">**パターンは制約付き入力値を許可する入力可能タイプを制限しますか。**</span><span class="sxs-lookup"><span data-stu-id="a98ab-186">**Does the pattern limit the possible input types to those that allow constrained input values?**</span></span>
    -   <span data-ttu-id="a98ab-187">このパターンは現在のところどの入力も受け入れますが、値に制約のない入力はガイドラインに反します。</span><span class="sxs-lookup"><span data-stu-id="a98ab-187">The pattern currently allows any input, but it's against guidelines to have inputs that have unconstrained values.</span></span>
-   <span data-ttu-id="a98ab-188">**グループをカスタム フィルター グループとして使用できるようにしますか。**</span><span class="sxs-lookup"><span data-stu-id="a98ab-188">**Do we allow groups to be used as custom filter groups?**</span></span>
    -   <span data-ttu-id="a98ab-189">移行を容易にするとともに、カスタム フィルター グループの場所を特定できるようにしました。</span><span class="sxs-lookup"><span data-stu-id="a98ab-189">We do allow them now, to make migration easier and to identify Custom Filter group locations.</span></span> <span data-ttu-id="a98ab-190">ただし、これらの状況でフィールドの小さなセットのみを使用することをお勧めします (および最終的にはこれを強制する場合があります)。</span><span class="sxs-lookup"><span data-stu-id="a98ab-190">However, we encourage you to use only a small set of fields in these situations (and we might eventually enforce this).</span></span>

### <a name="ax-2012-content"></a><span data-ttu-id="a98ab-191">AX 2012 コンテンツ</span><span class="sxs-lookup"><span data-stu-id="a98ab-191">AX 2012 content</span></span>

#### <a name="ax-2012-links"></a><span data-ttu-id="a98ab-192">AX 2012 リンク</span><span class="sxs-lookup"><span data-stu-id="a98ab-192">AX 2012 links</span></span>

-   [<span data-ttu-id="a98ab-193">MSDN AX 2012 フィルター ウィンドウにコントロールを追加する方法</span><span class="sxs-lookup"><span data-stu-id="a98ab-193">MSDN AX 2012 How to Add Controls to the Filter Pane</span></span>](https://msdn.microsoft.com/library/cc577231.aspx)
-   [<span data-ttu-id="a98ab-194">MSDN AX 2012 リスト ページの概要 – セクション フィルター ウィンドウ</span><span class="sxs-lookup"><span data-stu-id="a98ab-194">MSDN AX 2012 List Page Overview – section Filter Pane</span></span>](https://msdn.microsoft.com/library/cc616937.aspx)

#### <a name="ax-2012-example"></a><span data-ttu-id="a98ab-195">AX 2012 の例</span><span class="sxs-lookup"><span data-stu-id="a98ab-195">AX 2012 example</span></span>

<span data-ttu-id="a98ab-196">[![例](./media/customfiltergroup5.png)](./media/customfiltergroup5.png)</span><span class="sxs-lookup"><span data-stu-id="a98ab-196">[![Example](./media/customfiltergroup5.png)](./media/customfiltergroup5.png)</span></span>
