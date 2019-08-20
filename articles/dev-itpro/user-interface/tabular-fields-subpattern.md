---
title: 表形式フィールドのサブパターン
description: この記事では、表形式フィールドのサブパターンに関する情報を提供します。 このサブパターンは、情報を表形式で効率的に表示するために使用されます。
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
ms.custom: 14761
ms.assetid: a2c38c58-b312-44b1-bf48-c40dc8518011
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a15919250f7a492b28ef5db8d1c053b3348444f0
ms.sourcegitcommit: 16bfa0fd08feec1647829630401ce62ce2ffa1a4
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/02/2019
ms.locfileid: "1851087"
---
# <a name="tabular-fields-subpattern"></a><span data-ttu-id="ea3e1-104">表形式フィールドのサブパターン</span><span class="sxs-lookup"><span data-stu-id="ea3e1-104">Tabular Fields subpattern</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ea3e1-105">この記事では、表形式フィールドのサブパターンに関する情報を提供します。</span><span class="sxs-lookup"><span data-stu-id="ea3e1-105">This article provides information about the Tabular Fields subpattern.</span></span> <span data-ttu-id="ea3e1-106">このサブパターンは、情報を表形式で効率的に表示するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="ea3e1-106">This subpattern is used to show information efficiently in a tabular format.</span></span> 

<a name="usage"></a><span data-ttu-id="ea3e1-107">用途</span><span class="sxs-lookup"><span data-stu-id="ea3e1-107">Usage</span></span>
-----

<span data-ttu-id="ea3e1-108">このサブパターンは、情報を表形式で効率的に表示するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="ea3e1-108">This subpattern is used to show information efficiently in a tabular format.</span></span> <span data-ttu-id="ea3e1-109">フィールドは、行と列を含む表に配置され、オプションで列ヘッダー、行ラベル、キャプション、およびフッターが含まれます。</span><span class="sxs-lookup"><span data-stu-id="ea3e1-109">The fields are arranged in a table that contains rows and columns, and that optionally contains column headers, row labels, a caption, and a footer.</span></span> <span data-ttu-id="ea3e1-110">表形式フィールド サブパターンは、次のコントロールに対して適用できます。</span><span class="sxs-lookup"><span data-stu-id="ea3e1-110">The Tabular Fields subpattern can be applied on the following controls:</span></span>

-   <span data-ttu-id="ea3e1-111">TabPage コントロール</span><span class="sxs-lookup"><span data-stu-id="ea3e1-111">TabPage control</span></span>
-   <span data-ttu-id="ea3e1-112">グループ コントロール</span><span class="sxs-lookup"><span data-stu-id="ea3e1-112">Group control</span></span>

## <a name="wireframes"></a><span data-ttu-id="ea3e1-113">ワイヤーフレーム</span><span class="sxs-lookup"><span data-stu-id="ea3e1-113">Wireframes</span></span>
### <a name="tabularfields1mediatabularfields1pngmediatabularfields1pngstructural-wireframe"></a><span data-ttu-id="ea3e1-114">[![TabularFields(1)](./media/tabularfields1.png)](./media/tabularfields1.png)構造ワイヤーフレーム</span><span class="sxs-lookup"><span data-stu-id="ea3e1-114">[![TabularFields(1)](./media/tabularfields1.png)](./media/tabularfields1.png)Structural wireframe</span></span>

<span data-ttu-id="ea3e1-115">[![TabularFields(2)](./media/tabularfields2.png)](./media/tabularfields2.png)</span><span class="sxs-lookup"><span data-stu-id="ea3e1-115">[![TabularFields(2)](./media/tabularfields2.png)](./media/tabularfields2.png)</span></span>

## <a name="pattern-changes"></a><span data-ttu-id="ea3e1-116">パターンの変更</span><span class="sxs-lookup"><span data-stu-id="ea3e1-116">Pattern changes</span></span>
<span data-ttu-id="ea3e1-117">Microsoft Dynamics AX の以前のリリースでは、このパターンをモデル化するための正式に許容された方法はありませんでした。</span><span class="sxs-lookup"><span data-stu-id="ea3e1-117">In previous releases of Microsoft Dynamics AX, there was no formally accepted way to model this pattern.</span></span> <span data-ttu-id="ea3e1-118">したがって、このパターンは、現在のパターンと一致するように変更する必要がある、一貫性のない多くの方法でモデル化されました。</span><span class="sxs-lookup"><span data-stu-id="ea3e1-118">Therefore, this pattern was modeled in many inconsistent ways that must be modified to match the current pattern.</span></span> <span data-ttu-id="ea3e1-119">このパターンをモデル化する最も一般的な方法は、列にグループを使用することでした。</span><span class="sxs-lookup"><span data-stu-id="ea3e1-119">The most common way to model this pattern was to use groups for columns.</span></span> <span data-ttu-id="ea3e1-120">ただし、グループが行に使用されるようになりました。</span><span class="sxs-lookup"><span data-stu-id="ea3e1-120">However, groups are now used for the rows.</span></span> <span data-ttu-id="ea3e1-121">この変更の主な理由は HTML/CSS コンストラクトにより適合することでした。この変更は、テーブルのタブ順とセマンティクスの保持にも役立ちます。</span><span class="sxs-lookup"><span data-stu-id="ea3e1-121">The primary reason for this change was to better match the HTML/CSS constructs, and it also helps keep the tab sequence and semantics of a table.</span></span>

## <a name="model"></a><span data-ttu-id="ea3e1-122">モデル</span><span class="sxs-lookup"><span data-stu-id="ea3e1-122">Model</span></span>
### <a name="high-level-structure"></a><span data-ttu-id="ea3e1-123">高レベル構造体</span><span class="sxs-lookup"><span data-stu-id="ea3e1-123">High-level structure</span></span>

- <span data-ttu-id="ea3e1-124">TabularFields (グループ\*)</span><span class="sxs-lookup"><span data-stu-id="ea3e1-124">TabularFields (Group\*)</span></span>

    - <span data-ttu-id="ea3e1-125">CaptionGroup (Group)</span><span class="sxs-lookup"><span data-stu-id="ea3e1-125">CaptionGroup (Group)</span></span>

        - <span data-ttu-id="ea3e1-126">*TableCaption (StaticText) \[オプション\]*</span><span class="sxs-lookup"><span data-stu-id="ea3e1-126">*TableCaption (StaticText) \[Optional\]*</span></span>

    - <span data-ttu-id="ea3e1-127">TableHeaderRow (グループ)</span><span class="sxs-lookup"><span data-stu-id="ea3e1-127">TableHeaderRow (Group)</span></span>

        - <span data-ttu-id="ea3e1-128">*Column0Label (静的テキスト) \[オプション\]* – **注記:** この静的テキストは、col0、空白の row0 で入力されます。</span><span class="sxs-lookup"><span data-stu-id="ea3e1-128">*Column0Label (StaticText) \[Optional\]* – **Note:** This static text fills col0, row0 with a blank.</span></span>
        - <span data-ttu-id="ea3e1-129">ColumnLabels (StaticText) \[1..N\] – **注記:** これらは通常の列ヘッダーです。</span><span class="sxs-lookup"><span data-stu-id="ea3e1-129">ColumnLabels (StaticText) \[1..N\] – **Note:** These are the normal column headers.</span></span>

    - <span data-ttu-id="ea3e1-130">TableRows (グループ) \[1..N\]</span><span class="sxs-lookup"><span data-stu-id="ea3e1-130">TableRows (Group) \[1..N\]</span></span>

        - <span data-ttu-id="ea3e1-131">*RowLabel (StaticText) \[オプション\]*</span><span class="sxs-lookup"><span data-stu-id="ea3e1-131">*RowLabel (StaticText) \[Optional\]*</span></span>
        - <span data-ttu-id="ea3e1-132">RowValues ($Field) \[1..N\] または SecondaryColumnLabel (StaticText) \[1..N\]</span><span class="sxs-lookup"><span data-stu-id="ea3e1-132">RowValues ($Field) \[1..N\] OR SecondaryColumnLabel (StaticText) \[1..N\]</span></span>

    - <span data-ttu-id="ea3e1-133">TableFooterGroup (グループ)</span><span class="sxs-lookup"><span data-stu-id="ea3e1-133">TableFooterGroup (Group)</span></span>

        - <span data-ttu-id="ea3e1-134">*Column0Label (StaticText) \[オプション\]* – **注記:** この静的テキストは、col0、空白のフッターで入力されます。</span><span class="sxs-lookup"><span data-stu-id="ea3e1-134">*Column0Label (StaticText) \[Optional\]* – **Note:** This static text fills col0, footer with a blank.</span></span>
        - <span data-ttu-id="ea3e1-135">*RowValues ($ フィールド)\[0..N\]* – **注記:** すべてのフッター フィールドは表示モードです。</span><span class="sxs-lookup"><span data-stu-id="ea3e1-135">*RowValues ($Field) \[0..N\]* – **Note:** All the footer fields are in view mode.</span></span>

<span data-ttu-id="ea3e1-136">表の最上位レベルのフィールドにある 4 つのグループは必須となる構造的な要素であることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="ea3e1-136">Note that the four groups in the top-level tabular fields are mandatory structural elements.</span></span> <span data-ttu-id="ea3e1-137">ただし、それらすべてのグループ例外の行 (グループ) の内容はオプションです。</span><span class="sxs-lookup"><span data-stu-id="ea3e1-137">However, the contents of all those groups exception the Rows (Group) are optional.</span></span> <span data-ttu-id="ea3e1-138">また、表形式のフィールドは TabPage コントロールで使用することもできることに注意してください。</span><span class="sxs-lookup"><span data-stu-id="ea3e1-138">Additionally, note that Tabular Fields can also be used on a TabPage control.</span></span> <span data-ttu-id="ea3e1-139">構造はここに示す構造と同じです。</span><span class="sxs-lookup"><span data-stu-id="ea3e1-139">The structure is the same as the structure that is shown here.</span></span>

### <a name="core-components"></a><span data-ttu-id="ea3e1-140">コア コンポーネント</span><span class="sxs-lookup"><span data-stu-id="ea3e1-140">Core components</span></span>

<span data-ttu-id="ea3e1-141">トップレベルのグループやタブ ページに表形式フィールドのパターンを適用します。</span><span class="sxs-lookup"><span data-stu-id="ea3e1-141">Apply the Tabular Fields pattern on the top-level group or tab page.</span></span> <span data-ttu-id="ea3e1-142">パターン エラーと問題に対処します。</span><span class="sxs-lookup"><span data-stu-id="ea3e1-142">Address the pattern errors and problems.</span></span>

## <a name="ux-guidelines"></a><span data-ttu-id="ea3e1-143">UX ガイドライン</span><span class="sxs-lookup"><span data-stu-id="ea3e1-143">UX guidelines</span></span>
<span data-ttu-id="ea3e1-144">手動での検証は必要ありません。</span><span class="sxs-lookup"><span data-stu-id="ea3e1-144">No manual verification is required.</span></span>

## <a name="examples"></a><span data-ttu-id="ea3e1-145">例</span><span class="sxs-lookup"><span data-stu-id="ea3e1-145">Examples</span></span>
<span data-ttu-id="ea3e1-146">フォーム: **LedgerJournalTransVendPaym** **(残高)** (**買掛金勘定** &gt; **仕訳帳** &gt; **支払仕訳帳** &gt; **明細行**)</span><span class="sxs-lookup"><span data-stu-id="ea3e1-146">Form: **LedgerJournalTransVendPaym** **(Balances)** (**Accounts payable** &gt; **Journals** &gt; **Payment journal** &gt; **Lines**)</span></span> 

<span data-ttu-id="ea3e1-147">[![TabularFields(3)](./media/tabularfields3.png)](./media/tabularfields3.png)</span><span class="sxs-lookup"><span data-stu-id="ea3e1-147">[![TabularFields(3)](./media/tabularfields3.png)](./media/tabularfields3.png)</span></span>

## <a name="resources"></a><span data-ttu-id="ea3e1-148">リソース</span><span class="sxs-lookup"><span data-stu-id="ea3e1-148">Resources</span></span>
### <a name="typically-used-by-patterns"></a><span data-ttu-id="ea3e1-149">通常、パターンによって使用される</span><span class="sxs-lookup"><span data-stu-id="ea3e1-149">Typically used by patterns</span></span>

-   [<span data-ttu-id="ea3e1-150">簡易リストと詳細</span><span class="sxs-lookup"><span data-stu-id="ea3e1-150">Simple List and Details</span></span>](simple-list-details-form-pattern.md)
-   [<span data-ttu-id="ea3e1-151">目次</span><span class="sxs-lookup"><span data-stu-id="ea3e1-151">Table of Contents</span></span>](table-of-contents-form-pattern.md)
-   [<span data-ttu-id="ea3e1-152">詳細マスター</span><span class="sxs-lookup"><span data-stu-id="ea3e1-152">Details Master</span></span>](details-master-form-pattern.md)
-   [<span data-ttu-id="ea3e1-153">詳細トランザクション</span><span class="sxs-lookup"><span data-stu-id="ea3e1-153">Details Transaction</span></span>](details-transaction-form-pattern.md)

## <a name="appendix"></a><span data-ttu-id="ea3e1-154">付録</span><span class="sxs-lookup"><span data-stu-id="ea3e1-154">Appendix</span></span>
### <a name="frequently-asked-questions"></a><span data-ttu-id="ea3e1-155">よく寄せられる質問</span><span class="sxs-lookup"><span data-stu-id="ea3e1-155">Frequently asked questions</span></span>

<span data-ttu-id="ea3e1-156">このセクションには、このガイドライン/パターンに関連するよくある質問への回答があります。</span><span class="sxs-lookup"><span data-stu-id="ea3e1-156">This section will have answers to frequently asked questions that are related to this guideline/pattern.</span></span>

-   <span data-ttu-id="ea3e1-157">**表形式のフィールド レイアウトの作成方法を変更する理由は何ですか?**</span><span class="sxs-lookup"><span data-stu-id="ea3e1-157">**Why are we changing how the tabular field layout is created?**</span></span>
    -   <span data-ttu-id="ea3e1-158">HTML でレイアウトを実現するには、HTML レイアウトの動作方法に合わせる必要があります。</span><span class="sxs-lookup"><span data-stu-id="ea3e1-158">To accomplish the layout in HTML, we must align with the way that HTML layout works.</span></span> <span data-ttu-id="ea3e1-159">HTML レイアウトは、列ごとではなく行ごとにグループ化します。</span><span class="sxs-lookup"><span data-stu-id="ea3e1-159">HTML layout groups by rows, not by columns.</span></span>

### <a name="open-issues"></a><span data-ttu-id="ea3e1-160">未処理の問題</span><span class="sxs-lookup"><span data-stu-id="ea3e1-160">Open issues</span></span>

-   <span data-ttu-id="ea3e1-161">None</span><span class="sxs-lookup"><span data-stu-id="ea3e1-161">None</span></span>
