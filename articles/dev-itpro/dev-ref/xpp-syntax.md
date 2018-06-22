---
title: "X++ 構文"
description: "このトピックには、X++ の構文リファレンスが含まれています。"
author: RobinARH
manager: AnnBe
ms.date: 11/03/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Developer
ms.reviewer: robinr
ms.search.scope: Operations
ms.custom: 72211
ms.assetid: bb238a46-3a43-4f3c-a9b6-86b26e988881
ms.search.region: Global
ms.author: robinr
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: ea5c999dc8739a65b42e4be9f07f535c07f40d25
ms.contentlocale: ja-jp
ms.lasthandoff: 05/08/2018

---

# <a name="x-syntax"></a><span data-ttu-id="9ebda-103">X++ 構文</span><span class="sxs-lookup"><span data-stu-id="9ebda-103">X++ syntax</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="9ebda-104">このトピックには、X++ の構文リファレンスが含まれています。</span><span class="sxs-lookup"><span data-stu-id="9ebda-104">This topic contains the syntax reference for X++.</span></span> 

<a name="x-keywords"></a><span data-ttu-id="9ebda-105">X++ キーワード</span><span class="sxs-lookup"><span data-stu-id="9ebda-105">X++ Keywords</span></span>
------------

<span data-ttu-id="9ebda-106">次の表に示す X++ キーワードは予約されています。</span><span class="sxs-lookup"><span data-stu-id="9ebda-106">The X++ keywords shown in the following table are reserved.</span></span> <span data-ttu-id="9ebda-107">これらのキーワードは、他の目的に使用することはできません。</span><span class="sxs-lookup"><span data-stu-id="9ebda-107">These keywords cannot be used for any other purpose.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="9ebda-108">予約語</span><span class="sxs-lookup"><span data-stu-id="9ebda-108">Reserved word</span></span></th>
<th><span data-ttu-id="9ebda-109">説明</span><span class="sxs-lookup"><span data-stu-id="9ebda-109">Description</span></span></th>
<th><span data-ttu-id="9ebda-110">詳細情報</span><span class="sxs-lookup"><span data-stu-id="9ebda-110">More information</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9ebda-111"><strong>!</strong></span><span class="sxs-lookup"><span data-stu-id="9ebda-111"><strong>!</strong></span></span></td>
<td><span data-ttu-id="9ebda-112">ありません。</span><span class="sxs-lookup"><span data-stu-id="9ebda-112">Not.</span></span></td>
<td><span data-ttu-id="9ebda-113">リレーショナル演算子</span><span class="sxs-lookup"><span data-stu-id="9ebda-113">Relational Operators</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9ebda-114"><strong>!=</strong></span><span class="sxs-lookup"><span data-stu-id="9ebda-114"><strong>!=</strong></span></span></td>
<td><span data-ttu-id="9ebda-115">非等値演算子 (等しくない)。</span><span class="sxs-lookup"><span data-stu-id="9ebda-115">Inequality operator (not equal to).</span></span></td>
<td><span data-ttu-id="9ebda-116">リレーショナル演算子</span><span class="sxs-lookup"><span data-stu-id="9ebda-116">Relational Operators</span></span></td>
</tr>
<tr class="odd">
<td><strong>#</strong></td>
<td><span data-ttu-id="9ebda-117">マクロ名に接頭語を付けます。</span><span class="sxs-lookup"><span data-stu-id="9ebda-117">Prefix on macro names.</span></span></td>
<td><span data-ttu-id="9ebda-118">方法: #define および #if を使用してマクロをテストする</span><span class="sxs-lookup"><span data-stu-id="9ebda-118">How to: Use #define and #if to Test a Macro</span></span></td>
</tr>
<tr class="even">
<td><strong>&amp;</strong></td>
<td><span data-ttu-id="9ebda-119">バイナリ AND。</span><span class="sxs-lookup"><span data-stu-id="9ebda-119">Binary AND.</span></span></td>
<td><span data-ttu-id="9ebda-120">算術演算子</span><span class="sxs-lookup"><span data-stu-id="9ebda-120">Arithmetic Operators</span></span></td>
</tr>
<tr class="odd">
<td><strong>&amp;&amp;</strong></td>
<td><span data-ttu-id="9ebda-121">論理 AND。</span><span class="sxs-lookup"><span data-stu-id="9ebda-121">Logical AND.</span></span></td>
<td><span data-ttu-id="9ebda-122">リレーショナル演算子</span><span class="sxs-lookup"><span data-stu-id="9ebda-122">Relational Operators</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9ebda-123"><strong>(</strong></span><span class="sxs-lookup"><span data-stu-id="9ebda-123"><strong>(</strong></span></span></td>
<td><span data-ttu-id="9ebda-124">関数呼び出し演算子は、関数呼び出しの開始を示します。</span><span class="sxs-lookup"><span data-stu-id="9ebda-124">Function call operator, which indicates the beginning of the function call.</span></span></td>
<td></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9ebda-125"><strong>)</strong></span><span class="sxs-lookup"><span data-stu-id="9ebda-125"><strong>)</strong></span></span></td>
<td><span data-ttu-id="9ebda-126">関数呼び出し演算子は、関数呼び出しの終了を示します。</span><span class="sxs-lookup"><span data-stu-id="9ebda-126">Function call operator, which indicates the end of the function call.</span></span></td>
<td></td>
</tr>
<tr class="even">
<td><strong><em></strong></td>
<td><span data-ttu-id="9ebda-127">乗算します。</span><span class="sxs-lookup"><span data-stu-id="9ebda-127">Multiply.</span></span> <span data-ttu-id="9ebda-128">アスタリスク (<span class="code"></em></span>) は、X++ SQL でも使用されます。</span><span class="sxs-lookup"><span data-stu-id="9ebda-128">The asterisk (<span class="code"></em></span>) is also used in X++ SQL.</span></span> <span data-ttu-id="9ebda-129">1 つの使用方法は、<code>select</code> ステートメントにおいてテーブルのすべてのフィールドを示すことです。</span><span class="sxs-lookup"><span data-stu-id="9ebda-129">One use is to signify all fields from the tables on a <code>select</code> statement.</span></span> <span data-ttu-id="9ebda-130">もう 1 つの使用法は、<code>like</code>演算子を持つワイルドカードとして、あらゆる種類の 0 から複数の文字表すことです。</span><span class="sxs-lookup"><span data-stu-id="9ebda-130">Another use is as a wildcard with the <code>like</code> operator, to signify 0 to many characters of any kind.</span></span> <span data-ttu-id="9ebda-131"><code>like</code> 演算子は、<span class="code">?</span> も使用します</span><span class="sxs-lookup"><span data-stu-id="9ebda-131">The <code>like</code> operator also uses the <span class="code">?</span></span></span> <span data-ttu-id="9ebda-132">文字。</span><span class="sxs-lookup"><span data-stu-id="9ebda-132">character.</span></span></td>
<td><span data-ttu-id="9ebda-133">算術演算子</span><span class="sxs-lookup"><span data-stu-id="9ebda-133">Arithmetic Operators</span></span></td>
</tr>
<tr class="odd">
<td><strong>^</strong></td>
<td><span data-ttu-id="9ebda-134">バイナリ XOR。</span><span class="sxs-lookup"><span data-stu-id="9ebda-134">Binary XOR.</span></span></td>
<td><span data-ttu-id="9ebda-135">算術演算子</span><span class="sxs-lookup"><span data-stu-id="9ebda-135">Arithmetic Operators</span></span></td>
</tr>
<tr class="even">
<td><strong>|</strong></td>
<td><span data-ttu-id="9ebda-136">バイナリ OR。</span><span class="sxs-lookup"><span data-stu-id="9ebda-136">Binary OR.</span></span></td>
<td><span data-ttu-id="9ebda-137">算術演算子</span><span class="sxs-lookup"><span data-stu-id="9ebda-137">Arithmetic Operators</span></span></td>
</tr>
<tr class="odd">
<td><strong>||</strong></td>
<td><span data-ttu-id="9ebda-138">論理 OR。</span><span class="sxs-lookup"><span data-stu-id="9ebda-138">Logical OR.</span></span></td>
<td><span data-ttu-id="9ebda-139">リレーショナル演算子</span><span class="sxs-lookup"><span data-stu-id="9ebda-139">Relational Operators</span></span></td>
</tr>
<tr class="even">
<td><strong>~</strong></td>
<td><span data-ttu-id="9ebda-140">ありません。</span><span class="sxs-lookup"><span data-stu-id="9ebda-140">Not.</span></span></td>
<td><span data-ttu-id="9ebda-141">算術演算子</span><span class="sxs-lookup"><span data-stu-id="9ebda-141">Arithmetic Operators</span></span></td>
</tr>
<tr class="odd">
<td><strong>+</strong></td>
<td><span data-ttu-id="9ebda-142">プラス。</span><span class="sxs-lookup"><span data-stu-id="9ebda-142">Plus.</span></span></td>
<td><span data-ttu-id="9ebda-143">算術演算子</span><span class="sxs-lookup"><span data-stu-id="9ebda-143">Arithmetic Operators</span></span></td>
</tr>
<tr class="even">
<td><strong>++</strong></td>
<td><span data-ttu-id="9ebda-144">増分。</span><span class="sxs-lookup"><span data-stu-id="9ebda-144">Increment.</span></span></td>
<td><span data-ttu-id="9ebda-145">代入演算子</span><span class="sxs-lookup"><span data-stu-id="9ebda-145">Assignment Operators</span></span></td>
</tr>
<tr class="odd">
<td><strong>+=</strong></td>
<td><span data-ttu-id="9ebda-146">割り当ての追加。</span><span class="sxs-lookup"><span data-stu-id="9ebda-146">Additive assignment.</span></span></td>
<td><span data-ttu-id="9ebda-147">代入演算子</span><span class="sxs-lookup"><span data-stu-id="9ebda-147">Assignment Operators</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9ebda-148"><strong>、</strong></span><span class="sxs-lookup"><span data-stu-id="9ebda-148"><strong>,</strong></span></span></td>
<td><span data-ttu-id="9ebda-149">コンマ演算子。</span><span class="sxs-lookup"><span data-stu-id="9ebda-149">Comma operator.</span></span> <span data-ttu-id="9ebda-150">コンマで区切られた式は、左から右に評価されます。</span><span class="sxs-lookup"><span data-stu-id="9ebda-150">Expressions separated by commas are evaluated left-to-right.</span></span></td>
<td></td>
</tr>
<tr class="odd">
<td><strong>-</strong></td>
<td><span data-ttu-id="9ebda-151">マイナス。</span><span class="sxs-lookup"><span data-stu-id="9ebda-151">Minus.</span></span></td>
<td><span data-ttu-id="9ebda-152">算術演算子</span><span class="sxs-lookup"><span data-stu-id="9ebda-152">Arithmetic Operators</span></span></td>
</tr>
<tr class="even">
<td><strong>--</strong></td>
<td><span data-ttu-id="9ebda-153">デクリメント演算子。</span><span class="sxs-lookup"><span data-stu-id="9ebda-153">Decrement operator.</span></span></td>
<td><span data-ttu-id="9ebda-154">代入演算子</span><span class="sxs-lookup"><span data-stu-id="9ebda-154">Assignment Operators</span></span></td>
</tr>
<tr class="odd">
<td><strong>-=</strong></td>
<td><span data-ttu-id="9ebda-155">減算する割り当て。</span><span class="sxs-lookup"><span data-stu-id="9ebda-155">Subtractive assignment.</span></span></td>
<td><span data-ttu-id="9ebda-156">代入演算子</span><span class="sxs-lookup"><span data-stu-id="9ebda-156">Assignment Operators</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9ebda-157"><strong>。</strong></span><span class="sxs-lookup"><span data-stu-id="9ebda-157"><strong>.</strong></span></span></td>
<td><span data-ttu-id="9ebda-158">クラス メンバー アクセス演算子、たとえば、<code>formRun.run</code> は、クラス型 <code>FormRun</code> のオブジェクトの <code>run</code> メソッドにアクセスします。</span><span class="sxs-lookup"><span data-stu-id="9ebda-158">Class member access operator, for example, <code>formRun.run</code> accesses the <code>run</code> method of an object of the class type <code>FormRun</code>.</span></span></td>
<td></td>
</tr>
<tr class="odd">
<td><strong>/</strong></td>
<td><span data-ttu-id="9ebda-159">分割。</span><span class="sxs-lookup"><span data-stu-id="9ebda-159">Divide.</span></span></td>
<td><span data-ttu-id="9ebda-160">算術演算子</span><span class="sxs-lookup"><span data-stu-id="9ebda-160">Arithmetic Operators</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9ebda-161"><strong>&lt;/strong&gt;</span><span class="sxs-lookup"><span data-stu-id="9ebda-161"><strong>&lt;/strong&gt;</span></span></td>
<td><span data-ttu-id="9ebda-162">文字列でエスケープします。</span><span class="sxs-lookup"><span data-stu-id="9ebda-162">Escape in strings.</span></span> <span data-ttu-id="9ebda-163">余分な引用符およびタブの <span class="code">\t</span> などの特定の文字をエスケープします。</span><span class="sxs-lookup"><span data-stu-id="9ebda-163">Escapes extra quotation marks, and certain letters such as <span class="code">\t</span> for tab.</span></span></td>
<td></td>
</tr>
<tr class="odd">
<td><strong>@</strong></td>
<td><span data-ttu-id="9ebda-164">キーワードのエスケープです。</span><span class="sxs-lookup"><span data-stu-id="9ebda-164">Escape of keywords.</span></span> <span data-ttu-id="9ebda-165">たとえば、<span class="code">str<xref href="abstract" data-throw-if-not-resolved="False" data-raw-source="@abstract"></xref>;</span> は <strong>@</strong> 記号なしではコンパイルに失敗します 。</span><span class="sxs-lookup"><span data-stu-id="9ebda-165">For example, <span class="code">str <xref href="abstract" data-throw-if-not-resolved="False" data-raw-source="@abstract"></xref>;</span> would fail to compile without the <strong>@</strong> sign.</span></span> <span data-ttu-id="9ebda-166">また \ エスケープ文字の効果を否定すること、およびソース コード内の 1 つ以上の明細行にまたがる文字列を有効にすることによってリテラル文字列にも影響を及ぼします。</span><span class="sxs-lookup"><span data-stu-id="9ebda-166">Also affects literal strings, by negating the effect of the \ escape character, and by enabling the string to span more than one line in the source code.</span></span> <span data-ttu-id="9ebda-167">新しい行は 16 進数 0x0A の 1 文字で表され、これは一般に改行と呼ばれます。</span><span class="sxs-lookup"><span data-stu-id="9ebda-167">The new line is represented by one character of hexadecimal 0x0A, which is commonly called a line feed.</span></span> <span data-ttu-id="9ebda-168">0x0D0A のように 16 進数 0x0D のキャリッジ リターン文字は含まれません。</span><span class="sxs-lookup"><span data-stu-id="9ebda-168">No carriage return character of hexadecimal 0x0D is included, as in 0x0D0A.</span></span></td>
<td></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9ebda-169"><strong>: </strong></span><span class="sxs-lookup"><span data-stu-id="9ebda-169"><strong>:</strong></span></span></td>
<td><span data-ttu-id="9ebda-170">フィールド申告またはラベル指定子。</span><span class="sxs-lookup"><span data-stu-id="9ebda-170">Field declaration or label specifier.</span></span> <span data-ttu-id="9ebda-171">コロン (<span class="code">:</span>) 文字も <code>switch</code> 明細書で使用されます。</span><span class="sxs-lookup"><span data-stu-id="9ebda-171">The colon (<span class="code">:</span>) character is also used on the <code>switch</code> statement.</span></span></td>
<td></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9ebda-172"><strong>::</strong></span><span class="sxs-lookup"><span data-stu-id="9ebda-172"><strong>::</strong></span></span></td>
<td><span data-ttu-id="9ebda-173">静的 (class) メソッド: <span class="code">ClassName::methodName</span> を呼び出すときに使用します。</span><span class="sxs-lookup"><span data-stu-id="9ebda-173">Used to call static (class) methods: <span class="code">ClassName::methodName</span>.</span></span></td>
<td></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9ebda-174"><strong>;</strong></span><span class="sxs-lookup"><span data-stu-id="9ebda-174"><strong>;</strong></span></span></td>
<td><span data-ttu-id="9ebda-175">ステートメントを終了します。</span><span class="sxs-lookup"><span data-stu-id="9ebda-175">Terminates statements.</span></span> <span data-ttu-id="9ebda-176"><code>for</code> ループまたは文の区切り記号として使用されます。</span><span class="sxs-lookup"><span data-stu-id="9ebda-176">Used in <code>for</code> loops or as a separator of statements.</span></span></td>
<td></td>
</tr>
<tr class="odd">
<td><strong>&lt;</strong></td>
<td><span data-ttu-id="9ebda-177">より小さい。</span><span class="sxs-lookup"><span data-stu-id="9ebda-177">Less than.</span></span></td>
<td><span data-ttu-id="9ebda-178">リレーショナル演算子</span><span class="sxs-lookup"><span data-stu-id="9ebda-178">Relational Operators</span></span></td>
</tr>
<tr class="even">
<td><strong>&lt;&lt;</strong></td>
<td><span data-ttu-id="9ebda-179">左 Shift。</span><span class="sxs-lookup"><span data-stu-id="9ebda-179">Left shift.</span></span></td>
<td><span data-ttu-id="9ebda-180">算術演算子</span><span class="sxs-lookup"><span data-stu-id="9ebda-180">Arithmetic Operators</span></span></td>
</tr>
<tr class="odd">
<td><strong>&lt;=</strong></td>
<td><span data-ttu-id="9ebda-181">以下。</span><span class="sxs-lookup"><span data-stu-id="9ebda-181">Less than or equal.</span></span></td>
<td><span data-ttu-id="9ebda-182">算術演算子</span><span class="sxs-lookup"><span data-stu-id="9ebda-182">Arithmetic Operators</span></span></td>
</tr>
<tr class="even">
<td><strong>=</strong></td>
<td><span data-ttu-id="9ebda-183">代入演算子。</span><span class="sxs-lookup"><span data-stu-id="9ebda-183">Assignment operator.</span></span> <span data-ttu-id="9ebda-184">&quot;<strong>=</strong>&quot; の左側の引数は、右側の引数の値に設定されます。</span><span class="sxs-lookup"><span data-stu-id="9ebda-184">The argument to the left of &quot;<strong>=</strong>&quot; is set to the value of the argument to the right.</span></span></td>
<td><span data-ttu-id="9ebda-185">代入演算子</span><span class="sxs-lookup"><span data-stu-id="9ebda-185">Assignment Operators</span></span></td>
</tr>
<tr class="odd">
<td><strong>==</strong></td>
<td><span data-ttu-id="9ebda-186">両方の式が等しい場合は、true を返します。</span><span class="sxs-lookup"><span data-stu-id="9ebda-186">Returns true if both expressions are equal.</span></span></td>
<td><span data-ttu-id="9ebda-187">リレーショナル演算子</span><span class="sxs-lookup"><span data-stu-id="9ebda-187">Relational Operators</span></span></td>
</tr>
<tr class="even">
<td><strong>&gt;</strong></td>
<td><span data-ttu-id="9ebda-188">より大きい。</span><span class="sxs-lookup"><span data-stu-id="9ebda-188">Greater than.</span></span></td>
<td><span data-ttu-id="9ebda-189">リレーショナル演算子</span><span class="sxs-lookup"><span data-stu-id="9ebda-189">Relational Operators</span></span></td>
</tr>
<tr class="odd">
<td><strong>&gt;=</strong></td>
<td><span data-ttu-id="9ebda-190">以上。</span><span class="sxs-lookup"><span data-stu-id="9ebda-190">Greater than or equal.</span></span></td>
<td><span data-ttu-id="9ebda-191">リレーショナル演算子</span><span class="sxs-lookup"><span data-stu-id="9ebda-191">Relational Operators</span></span></td>
</tr>
<tr class="even">
<td><strong>&gt;&gt;</strong></td>
<td><span data-ttu-id="9ebda-192">右 Shift</span><span class="sxs-lookup"><span data-stu-id="9ebda-192">Right shift.</span></span></td>
<td><span data-ttu-id="9ebda-193">算術演算子</span><span class="sxs-lookup"><span data-stu-id="9ebda-193">Arithmetic Operators</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9ebda-194"><strong>?</strong></span><span class="sxs-lookup"><span data-stu-id="9ebda-194"><strong>?</strong></span></span></td>
<td><span data-ttu-id="9ebda-195">三項演算子。</span><span class="sxs-lookup"><span data-stu-id="9ebda-195">Ternary operator.</span></span> <span data-ttu-id="9ebda-196">疑問符 (<span class="code">?</span>) 文字は、<code>like</code> 演算子がどのような種類の文字でも正確に表すために使用されます。</span><span class="sxs-lookup"><span data-stu-id="9ebda-196">The question mark (<span class="code">?</span>) character is also used by the <code>like</code> operator to signify exactly one character of any kind.</span></span> <span data-ttu-id="9ebda-197"><code>like</code> 演算子は、<span class="code"><em></span> 文字も使用します。</span><span class="sxs-lookup"><span data-stu-id="9ebda-197">The <code>like</code> operator also uses the <span class="code"><em></span> character.</span></span></td>
<td><span data-ttu-id="9ebda-198">三項演算子 (?)</span><span class="sxs-lookup"><span data-stu-id="9ebda-198">Ternary Operator (?)</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9ebda-199"><strong>[</strong></span><span class="sxs-lookup"><span data-stu-id="9ebda-199"><strong>[</strong></span></span></td>
<td><span data-ttu-id="9ebda-200">配列宣言子、開きます。</span><span class="sxs-lookup"><span data-stu-id="9ebda-200">Array declarator, open.</span></span> <span data-ttu-id="9ebda-201">&quot;<strong>]</strong>&quot; とともに使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="9ebda-201">Must be used with &quot;<strong>]</strong>&quot;.</span></span></td>
<td></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9ebda-202"><strong>]</strong></span><span class="sxs-lookup"><span data-stu-id="9ebda-202"><strong>]</strong></span></span></td>
<td><span data-ttu-id="9ebda-203">配列宣言子、閉じます。</span><span class="sxs-lookup"><span data-stu-id="9ebda-203">Array declarator, close.</span></span> <span data-ttu-id="9ebda-204">&quot;<strong>[</strong>&quot; とともに使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="9ebda-204">Must be used with &quot;<strong>[</strong>&quot;.</span></span></td>
<td></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9ebda-205"><strong>{</strong></span><span class="sxs-lookup"><span data-stu-id="9ebda-205"><strong>{</strong></span></span></td>
<td><span data-ttu-id="9ebda-206">ステートメントの番号の先頭を示します。</span><span class="sxs-lookup"><span data-stu-id="9ebda-206">Indicates the beginning of a number of statements.</span></span> <span data-ttu-id="9ebda-207">これらのステートメントの最後には、&quot;<strong>}</strong>&quot; が続かなければなりません。</span><span class="sxs-lookup"><span data-stu-id="9ebda-207">The last of these statements must be followed by a &quot;<strong>}</strong>&quot;.</span></span></td>
<td></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9ebda-208"><strong>}</strong></span><span class="sxs-lookup"><span data-stu-id="9ebda-208"><strong>}</strong></span></span></td>
<td><span data-ttu-id="9ebda-209">ステートメントの番号の最後を示します。</span><span class="sxs-lookup"><span data-stu-id="9ebda-209">Indicates the end of a number of statements.</span></span> <span data-ttu-id="9ebda-210">&quot;<strong>{</strong>&quot; は、これらのステートメントの最初よりも前にある必要があります。</span><span class="sxs-lookup"><span data-stu-id="9ebda-210">A &quot;<strong>{</strong>&quot; must appear before the first of these statements.</span></span></td>
<td></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9ebda-211"><strong>抽象</strong></span><span class="sxs-lookup"><span data-stu-id="9ebda-211"><strong>abstract</strong></span></span></td>
<td><span data-ttu-id="9ebda-212">クラスとメソッドのモディファイア。</span><span class="sxs-lookup"><span data-stu-id="9ebda-212">Class and method modifier.</span></span> <span data-ttu-id="9ebda-213"><strong>抽象</strong>クラスは<strong>新規</strong>キーワードで構築することはできません。</span><span class="sxs-lookup"><span data-stu-id="9ebda-213">An <strong>abstract</strong> class cannot be constructed with the <strong>new</strong> keyword.</span></span> <span data-ttu-id="9ebda-214"><strong>抽象</strong>メソッドを呼び出すことはできません。</span><span class="sxs-lookup"><span data-stu-id="9ebda-214">An <strong>abstract</strong> method cannot be called.</span></span> <span data-ttu-id="9ebda-215">テーブルは、AOT で<span class="ui">抽象</span>プロパティを<span class="ui">はい</span>に設定するか、<code>DictTable</code> クラスを使用して、抽象として変更することもできます。</span><span class="sxs-lookup"><span data-stu-id="9ebda-215">A table can also be modified as abstract by setting its <span class="ui">Abstract</span> property to <span class="ui">Yes</span> in the AOT, or by using the <code>DictTable</code> class.</span></span> <span data-ttu-id="9ebda-216"><span class="ui">抽象</span> プロパティの既定値は <span class="ui">いいえ</span> であり、別のテーブルによりテーブルが拡張されない限り設定することはできません。</span><span class="sxs-lookup"><span data-stu-id="9ebda-216">The <span class="ui">Abstract</span> property defaults to <span class="ui">No</span>, and it cannot be set unless the table is extended by another table.</span></span> <span data-ttu-id="9ebda-217">抽象テーブルの各行は、派生テーブルに依存する行が必要です。</span><span class="sxs-lookup"><span data-stu-id="9ebda-217">Each row in an abstract table must have a dependent row in a derived table.</span></span> <span data-ttu-id="9ebda-218">これは、抽象テーブルの各行が <span class="ui">InstanceRelationType</span> プロパティ フィールドで 0 より大きい値を持つことを意味します。</span><span class="sxs-lookup"><span data-stu-id="9ebda-218">This means that each row in an abstract table has a value greater than 0 (zero) in its <span class="ui">InstanceRelationType</span> property field.</span></span> <span data-ttu-id="9ebda-219">マーキングを抽象としてマークすることによる他の効果はありません。</span><span class="sxs-lookup"><span data-stu-id="9ebda-219">There are no other effects from marking a table as abstract.</span></span> <span data-ttu-id="9ebda-220">非公式に、プログラマは <span class="term">concrete</span> という用語を使用して<strong>抽象</strong>ではないクラスを記述します。</span><span class="sxs-lookup"><span data-stu-id="9ebda-220">Informally, programmers often use the term <span class="term">concrete</span> to describe a class that is non-<strong>abstract</strong>.</span></span></td>
<td><span data-ttu-id="9ebda-221">メソッド モディファイアー テーブル継承の概要</span><span class="sxs-lookup"><span data-stu-id="9ebda-221">Method Modifiers Table Inheritance Overview</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9ebda-222"><strong>anytype</strong></span><span class="sxs-lookup"><span data-stu-id="9ebda-222"><strong>anytype</strong></span></span></td>
<td><span data-ttu-id="9ebda-223">このメソッドは任意のデータ型を返すことができます。</span><span class="sxs-lookup"><span data-stu-id="9ebda-223">The method can return any data type.</span></span></td>
<td><span data-ttu-id="9ebda-224">Anytype</span><span class="sxs-lookup"><span data-stu-id="9ebda-224">Anytype</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9ebda-225"><strong>利用品目</strong></span><span class="sxs-lookup"><span data-stu-id="9ebda-225"><strong>as</strong></span></span></td>
<td><span data-ttu-id="9ebda-226">派生クラス変数に基本クラス変数を割り当てるときに必要です。</span><span class="sxs-lookup"><span data-stu-id="9ebda-226">Needed when you assign a base class variable to a derived class variable.</span></span> <span data-ttu-id="9ebda-227">たとえば、<code>Base</code>クラスを<strong>拡張</strong>する指定された <code>Derived</code> クラスでは、明細書の<code>myDerived = myBase as Derived;</code> は <strong>as</strong> キーワードを使用して、コンパイラ エラーを避けます。</span><span class="sxs-lookup"><span data-stu-id="9ebda-227">For example, given a <code>Derived</code> class that <strong>extends</strong> a <code>Base</code> class, the statement <code>myDerived = myBase as Derived;</code> avoids a compiler error by using the <strong>as</strong> keyword.</span></span> <span data-ttu-id="9ebda-228">このキーワードは、ベース テーブル変数を派生テーブル変数に割り当てるときにも適用されます。</span><span class="sxs-lookup"><span data-stu-id="9ebda-228">This keyword also applies when you assign a base table variable to a derived table variable.</span></span></td>
<td><span data-ttu-id="9ebda-229">式の演算子: 継承の Is および As</span><span class="sxs-lookup"><span data-stu-id="9ebda-229">Expression Operators: Is and As for Inheritance</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9ebda-230"><strong>asc</strong></span><span class="sxs-lookup"><span data-stu-id="9ebda-230"><strong>asc</strong></span></span></td>
<td><span data-ttu-id="9ebda-231"><code>select</code>ステートメント <code>order</code> <code>by</code> または <code>group</code> <code>by</code> 句のオプション。</span><span class="sxs-lookup"><span data-stu-id="9ebda-231">An option on the <code>order</code> <code>by</code> or <code>group</code> <code>by</code> clause in a <code>select</code> statement.</span></span> <span data-ttu-id="9ebda-232">並べ替えは昇順です。</span><span class="sxs-lookup"><span data-stu-id="9ebda-232">The sorting is ascending.</span></span></td>
<td><span data-ttu-id="9ebda-233">ステートメント構文の選択</span><span class="sxs-lookup"><span data-stu-id="9ebda-233">Select Statement Syntax</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9ebda-234"><strong>時刻</strong></span><span class="sxs-lookup"><span data-stu-id="9ebda-234"><strong>at</strong></span></span></td>
<td><span data-ttu-id="9ebda-235">印刷ウィンドウの位置を指定します。</span><span class="sxs-lookup"><span data-stu-id="9ebda-235">Specifies the position of a print window.</span></span></td>
<td><span data-ttu-id="9ebda-236">ステートメントの印刷</span><span class="sxs-lookup"><span data-stu-id="9ebda-236">Print Statements</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9ebda-237"><strong>平均</strong></span><span class="sxs-lookup"><span data-stu-id="9ebda-237"><strong>avg</strong></span></span></td>
<td><span data-ttu-id="9ebda-238"><code>select</code> ステートメント内の <code>group by</code> 句により指定された行からフィールドの平均を返します。</span><span class="sxs-lookup"><span data-stu-id="9ebda-238">Returns the average of the fields from the rows specified by the <code>group by</code> clause in a <code>select</code> statement.</span></span></td>
<td><span data-ttu-id="9ebda-239">ステートメント構文の選択</span><span class="sxs-lookup"><span data-stu-id="9ebda-239">Select Statement Syntax</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9ebda-240"><strong>分割</strong></span><span class="sxs-lookup"><span data-stu-id="9ebda-240"><strong>break</strong></span></span></td>
<td><span data-ttu-id="9ebda-241">コード ブロックをすぐに終了します。</span><span class="sxs-lookup"><span data-stu-id="9ebda-241">Immediate exit from code block.</span></span></td>
<td><span data-ttu-id="9ebda-242">Break ステートメント</span><span class="sxs-lookup"><span data-stu-id="9ebda-242">Break Statements</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9ebda-243"><strong>ブレークポイント</strong></span><span class="sxs-lookup"><span data-stu-id="9ebda-243"><strong>breakpoint</strong></span></span></td>
<td><span data-ttu-id="9ebda-244">デバッグのために設定されているブレークポイントを表します。</span><span class="sxs-lookup"><span data-stu-id="9ebda-244">Represents a breakpoint that is set for debugging purposes.</span></span> <span data-ttu-id="9ebda-245">コードにブレークポイントを設定するには、次のように記述します。<code>breakpoint;</code></span><span class="sxs-lookup"><span data-stu-id="9ebda-245">To set a breakpoint in your code, write: <code>breakpoint;</code></span></span></td>
<td></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9ebda-246"><strong>作成者</strong></span><span class="sxs-lookup"><span data-stu-id="9ebda-246"><strong>by</strong></span></span></td>
<td><span data-ttu-id="9ebda-247">グループ化と並べ替えの基準となる予約語の一部。</span><span class="sxs-lookup"><span data-stu-id="9ebda-247">Part of a reserved term, such as group by and order by.</span></span></td>
<td></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9ebda-248"><strong>byref</strong></span><span class="sxs-lookup"><span data-stu-id="9ebda-248"><strong>byref</strong></span></span></td>
<td><span data-ttu-id="9ebda-249">呼び出されたメソッドに渡されるパラメーターが、値ではなく参照 (アドレス) により渡されることを指定します。</span><span class="sxs-lookup"><span data-stu-id="9ebda-249">Specifies that the parameter being passed to the called method is being passed by reference (address), instead of by value.</span></span> <span data-ttu-id="9ebda-250"><strong>Byref</strong> は、参照によってパラメータをとる .NET メソッドを呼び出すときに X++ で使用されます (C# のキーワード <strong>out</strong> or <strong>ref</strong> など)。</span><span class="sxs-lookup"><span data-stu-id="9ebda-250"><strong>Byref</strong> is used in X++ when calling a .NET method that takes a parameter by reference (such as with the C# keywords <strong>out</strong> or <strong>ref</strong>).</span></span></td>
<td><span data-ttu-id="9ebda-251">方法: CLR Interop に byref キーワードを使用します。</span><span class="sxs-lookup"><span data-stu-id="9ebda-251">How to: Use the byref Keyword for CLR Interop.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9ebda-252"><strong>Case など)。</strong></span><span class="sxs-lookup"><span data-stu-id="9ebda-252"><strong>case</strong></span></span></td>
<td><span data-ttu-id="9ebda-253"><code>switch</code> ステートメント内の選択。</span><span class="sxs-lookup"><span data-stu-id="9ebda-253">Selection within a <code>switch</code> statement.</span></span></td>
<td><span data-ttu-id="9ebda-254">Switch ステートメント</span><span class="sxs-lookup"><span data-stu-id="9ebda-254">Switch Statements</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9ebda-255"><strong>catch</strong></span><span class="sxs-lookup"><span data-stu-id="9ebda-255"><strong>catch</strong></span></span></td>
<td><span data-ttu-id="9ebda-256">例外処理で使用されます。</span><span class="sxs-lookup"><span data-stu-id="9ebda-256">Used in exception handling.</span></span></td>
<td><span data-ttu-id="9ebda-257">トライおよびキャッチ キーワードの例外処理</span><span class="sxs-lookup"><span data-stu-id="9ebda-257">Exception Handling with try and catch Keywords</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9ebda-258"><strong>changeCompany</strong></span><span class="sxs-lookup"><span data-stu-id="9ebda-258"><strong>changeCompany</strong></span></span></td>
<td><span data-ttu-id="9ebda-259">データベース設定を別の会社に変更します。</span><span class="sxs-lookup"><span data-stu-id="9ebda-259">Changes database settings to another company.</span></span></td>
<td><span data-ttu-id="9ebda-260">会社の設計パターンを変更する</span><span class="sxs-lookup"><span data-stu-id="9ebda-260">Change Company Design Pattern</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9ebda-261"><strong>クラス</strong></span><span class="sxs-lookup"><span data-stu-id="9ebda-261"><strong>class</strong></span></span></td>
<td><span data-ttu-id="9ebda-262">クラスを宣言します。</span><span class="sxs-lookup"><span data-stu-id="9ebda-262">Declares a class.</span></span></td>
<td><span data-ttu-id="9ebda-263">X++ のクラス</span><span class="sxs-lookup"><span data-stu-id="9ebda-263">Classes in X++</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9ebda-264"><strong>クライアント</strong></span><span class="sxs-lookup"><span data-stu-id="9ebda-264"><strong>client</strong></span></span></td>
<td><span data-ttu-id="9ebda-265">メソッド モディファイアー｡</span><span class="sxs-lookup"><span data-stu-id="9ebda-265">Method modifier.</span></span></td>
<td><span data-ttu-id="9ebda-266">メソッド モディファイアー</span><span class="sxs-lookup"><span data-stu-id="9ebda-266">Method Modifiers</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9ebda-267"><strong>コンテナー</strong></span><span class="sxs-lookup"><span data-stu-id="9ebda-267"><strong>container</strong></span></span></td>
<td><span data-ttu-id="9ebda-268">型 <code>container</code> の変数を指定します。</span><span class="sxs-lookup"><span data-stu-id="9ebda-268">Specifies a variable of type <code>container</code>.</span></span></td>
<td><span data-ttu-id="9ebda-269">コンテナー</span><span class="sxs-lookup"><span data-stu-id="9ebda-269">Containers</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9ebda-270"><strong>続行</strong></span><span class="sxs-lookup"><span data-stu-id="9ebda-270"><strong>continue</strong></span></span></td>
<td><span data-ttu-id="9ebda-271">ループの次の繰り返しを強制します。</span><span class="sxs-lookup"><span data-stu-id="9ebda-271">Forces the next iteration of a loop.</span></span></td>
<td><span data-ttu-id="9ebda-272">明細書の続行</span><span class="sxs-lookup"><span data-stu-id="9ebda-272">Continue Statements</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9ebda-273"><strong>カウント</strong></span><span class="sxs-lookup"><span data-stu-id="9ebda-273"><strong>count</strong></span></span></td>
<td><span data-ttu-id="9ebda-274"><code>select</code> ステートメント内の <code>group by</code> 句により指定された行からレコードの数を返します。</span><span class="sxs-lookup"><span data-stu-id="9ebda-274">Returns the number of records from the rows specified by the <code>group by</code> clause in a <code>select</code> statement.</span></span></td>
<td><span data-ttu-id="9ebda-275">ステートメント構文の選択</span><span class="sxs-lookup"><span data-stu-id="9ebda-275">Select Statement Syntax</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9ebda-276"><strong>crossCompany</strong></span><span class="sxs-lookup"><span data-stu-id="9ebda-276"><strong>crossCompany</strong></span></span></td>
<td><span data-ttu-id="9ebda-277"><code>select</code> 明細書は、ユーザーが読み取りを承認されているすべての会社のデータを戻します。</span><span class="sxs-lookup"><span data-stu-id="9ebda-277">Causes a <code>select</code> statement to return data for all companies that the user is authorized to read from.</span></span></td>
<td><span data-ttu-id="9ebda-278">会社間の X++ Code の基礎</span><span class="sxs-lookup"><span data-stu-id="9ebda-278">Cross-Company X++ Code Basics</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9ebda-279"><strong>日付</strong></span><span class="sxs-lookup"><span data-stu-id="9ebda-279"><strong>date</strong></span></span></td>
<td><span data-ttu-id="9ebda-280">型 <code>date</code> の変数を指定します。</span><span class="sxs-lookup"><span data-stu-id="9ebda-280">Specifies a variable of type <code>date</code>.</span></span></td>
<td><span data-ttu-id="9ebda-281">日付</span><span class="sxs-lookup"><span data-stu-id="9ebda-281">Dates</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9ebda-282"><strong>既定</strong></span><span class="sxs-lookup"><span data-stu-id="9ebda-282"><strong>default</strong></span></span></td>
<td><span data-ttu-id="9ebda-283"><code>switch</code>明細書内の既定ケース</span><span class="sxs-lookup"><span data-stu-id="9ebda-283">Default case within <code>switch</code> statements.</span></span></td>
<td><span data-ttu-id="9ebda-284">Switch ステートメント</span><span class="sxs-lookup"><span data-stu-id="9ebda-284">Switch Statements</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9ebda-285"><strong>デリゲート</strong></span><span class="sxs-lookup"><span data-stu-id="9ebda-285"><strong>delegate</strong></span></span></td>
<td><span data-ttu-id="9ebda-286">他のクラスのメソッドへの複数の参照を格納し、これを行うように求められる場合にメソッドを呼び出すことができるクラス メンバー。</span><span class="sxs-lookup"><span data-stu-id="9ebda-286">A class member that is able to store multiple references to methods in other classes, and to call all those methods when prompted to do so.</span></span> <span data-ttu-id="9ebda-287">デリゲートは、次のようなさまざまな種類のメソッドへの参照を保存できます。</span><span class="sxs-lookup"><span data-stu-id="9ebda-287">A delegate can store references to various kinds of methods including the following:</span></span>
<ul>
<li><span data-ttu-id="9ebda-288">X++ クラスの静的メソッド</span><span class="sxs-lookup"><span data-stu-id="9ebda-288">static methods on X++ classes</span></span></li>
<li><span data-ttu-id="9ebda-289">X++ クラスのインスタンス メソッド</span><span class="sxs-lookup"><span data-stu-id="9ebda-289">instance methods on X++ classes</span></span></li>
<li><span data-ttu-id="9ebda-290">.NET Framework クラスのメソッド</span><span class="sxs-lookup"><span data-stu-id="9ebda-290">methods on .NET Framework classes</span></span></li>
</ul></td>
<td><span data-ttu-id="9ebda-291">イベント用語およびキーワード X++、C# 比較: イベント</span><span class="sxs-lookup"><span data-stu-id="9ebda-291">Event Terminology and Keywords X++, C# Comparison: Event</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9ebda-292"><strong>delete_from</strong></span><span class="sxs-lookup"><span data-stu-id="9ebda-292"><strong>delete_from</strong></span></span></td>
<td><span data-ttu-id="9ebda-293">同時に複数のレコードをデータベースから削除できます。</span><span class="sxs-lookup"><span data-stu-id="9ebda-293">Allows you to delete multiple records from the database at the same time.</span></span></td>
<td><span data-ttu-id="9ebda-294">delete_from</span><span class="sxs-lookup"><span data-stu-id="9ebda-294">delete_from</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9ebda-295"><strong>desc</strong></span><span class="sxs-lookup"><span data-stu-id="9ebda-295"><strong>desc</strong></span></span></td>
<td><span data-ttu-id="9ebda-296"><code>select</code> ステートメント <code>order by</code> または <code>group by</code> 句のオプション。</span><span class="sxs-lookup"><span data-stu-id="9ebda-296">An option on the <code>order by</code> or <code>group by</code> clause in a <code>select</code> statement.</span></span> <span data-ttu-id="9ebda-297">並べ替えは降順です。</span><span class="sxs-lookup"><span data-stu-id="9ebda-297">The sorting is descending.</span></span></td>
<td><span data-ttu-id="9ebda-298">ステートメント構文の選択</span><span class="sxs-lookup"><span data-stu-id="9ebda-298">Select Statement Syntax</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9ebda-299"><strong>表示</strong></span><span class="sxs-lookup"><span data-stu-id="9ebda-299"><strong>display</strong></span></span></td>
<td><span data-ttu-id="9ebda-300">メソッド モディファイアー｡</span><span class="sxs-lookup"><span data-stu-id="9ebda-300">Method modifier.</span></span></td>
<td><span data-ttu-id="9ebda-301">メソッド モディファイアー</span><span class="sxs-lookup"><span data-stu-id="9ebda-301">Method Modifiers</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9ebda-302"><strong>div</strong></span><span class="sxs-lookup"><span data-stu-id="9ebda-302"><strong>div</strong></span></span></td>
<td><span data-ttu-id="9ebda-303">整数除算。</span><span class="sxs-lookup"><span data-stu-id="9ebda-303">Integer division.</span></span></td>
<td><span data-ttu-id="9ebda-304">算術演算子</span><span class="sxs-lookup"><span data-stu-id="9ebda-304">Arithmetic Operators</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9ebda-305"><strong>実行</strong></span><span class="sxs-lookup"><span data-stu-id="9ebda-305"><strong>do</strong></span></span></td>
<td><span data-ttu-id="9ebda-306">ループ<code>do...while</code>の開始</span><span class="sxs-lookup"><span data-stu-id="9ebda-306">Beginning of a <code>do...while</code> loop.</span></span></td>
<td><span data-ttu-id="9ebda-307">while Loops を実行</span><span class="sxs-lookup"><span data-stu-id="9ebda-307">Do...while Loops</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9ebda-308"><strong>編集</strong></span><span class="sxs-lookup"><span data-stu-id="9ebda-308"><strong>edit</strong></span></span></td>
<td><span data-ttu-id="9ebda-309">メソッド モディファイアー｡</span><span class="sxs-lookup"><span data-stu-id="9ebda-309">Method modifier.</span></span></td>
<td><span data-ttu-id="9ebda-310">メソッド モディファイアー</span><span class="sxs-lookup"><span data-stu-id="9ebda-310">Method Modifiers</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9ebda-311"><strong>その他</strong></span><span class="sxs-lookup"><span data-stu-id="9ebda-311"><strong>else</strong></span></span></td>
<td><span data-ttu-id="9ebda-312">条件付き実行 (<code>if...else</code>)。</span><span class="sxs-lookup"><span data-stu-id="9ebda-312">Conditional execution (<code>if...else</code>).</span></span></td>
<td><span data-ttu-id="9ebda-313">if および if ... else ステートメント</span><span class="sxs-lookup"><span data-stu-id="9ebda-313">if and if ... else Statements</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9ebda-314"><strong>eventHandler</strong></span><span class="sxs-lookup"><span data-stu-id="9ebda-314"><strong>eventHandler</strong></span></span></td>
<td><span data-ttu-id="9ebda-315"><span class="code">+=</span> or <span class="code">-=</span> 演算子を使用して、デリゲートのメソッドの参照を追加または削除するたびに使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="9ebda-315">Must be used each time you either add or delete a method reference from a delegate by using the <span class="code">+=</span> or <span class="code">-=</span> operator.</span></span> <span data-ttu-id="9ebda-316">例: <span class="code">myDelegate += eventHandler(OtherClass::myStaticMethod);</span></span><span class="sxs-lookup"><span data-stu-id="9ebda-316">For example: <span class="code">myDelegate += eventHandler(OtherClass::myStaticMethod);</span></span></span></td>
<td><span data-ttu-id="9ebda-317">イベント用語およびキーワード X++、C# 比較: イベント</span><span class="sxs-lookup"><span data-stu-id="9ebda-317">Event Terminology and Keywords X++, C# Comparison: Event</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9ebda-318"><strong>あり</strong></span><span class="sxs-lookup"><span data-stu-id="9ebda-318"><strong>exists</strong></span></span></td>
<td><span data-ttu-id="9ebda-319"><code>select</code> 文の <code>join</code> 句で使用されます。</span><span class="sxs-lookup"><span data-stu-id="9ebda-319">Used with <code>join</code> clauses in <code>select</code> statements.</span></span></td>
<td><span data-ttu-id="9ebda-320">ステートメント構文の選択</span><span class="sxs-lookup"><span data-stu-id="9ebda-320">Select Statement Syntax</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9ebda-321"><strong>拡張</strong></span><span class="sxs-lookup"><span data-stu-id="9ebda-321"><strong>extends</strong></span></span></td>
<td><span data-ttu-id="9ebda-322">クラスまたはインターフェイス申告句。</span><span class="sxs-lookup"><span data-stu-id="9ebda-322">A class or interface declaration clause.</span></span> <span data-ttu-id="9ebda-323">クラスが明示的に別のクラスを拡張しない場合、クラスは <code>Object</code> クラスの拡張を検討します (&quot;オブジェクトを拡張&quot; と記述した場合のように)。</span><span class="sxs-lookup"><span data-stu-id="9ebda-323">If your class does not explicitly extend another class, your class is considered to extend the <code>Object</code> class (as if you had written &quot;extends Object&quot;).</span></span></td>
<td><span data-ttu-id="9ebda-324">サブクラスを作成しています</span><span class="sxs-lookup"><span data-stu-id="9ebda-324">Creating a Subclass</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9ebda-325"><strong>いいえ</strong></span><span class="sxs-lookup"><span data-stu-id="9ebda-325"><strong>false</strong></span></span></td>
<td><span data-ttu-id="9ebda-326">ブール型リテラル。</span><span class="sxs-lookup"><span data-stu-id="9ebda-326">Boolean literal.</span></span></td>
<td><span data-ttu-id="9ebda-327">ブール型</span><span class="sxs-lookup"><span data-stu-id="9ebda-327">Booleans</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9ebda-328"><strong>最終</strong></span><span class="sxs-lookup"><span data-stu-id="9ebda-328"><strong>final</strong></span></span></td>
<td><span data-ttu-id="9ebda-329">クラスとメソッドのモディファイア。</span><span class="sxs-lookup"><span data-stu-id="9ebda-329">Class and method modifier.</span></span></td>
<td><span data-ttu-id="9ebda-330">メソッド モディファイアー</span><span class="sxs-lookup"><span data-stu-id="9ebda-330">Method Modifiers</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9ebda-331"><strong>firstFast</strong></span><span class="sxs-lookup"><span data-stu-id="9ebda-331"><strong>firstFast</strong></span></span></td>
<td><span data-ttu-id="9ebda-332"><code>select</code> 文で使用され、最初の行のフェッチを高速化します。</span><span class="sxs-lookup"><span data-stu-id="9ebda-332">Used in <code>select</code> statements to speed up the fetch for the first row.</span></span></td>
<td><span data-ttu-id="9ebda-333">ステートメント構文の選択</span><span class="sxs-lookup"><span data-stu-id="9ebda-333">Select Statement Syntax</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9ebda-334"><strong>firstOnly</strong></span><span class="sxs-lookup"><span data-stu-id="9ebda-334"><strong>firstOnly</strong></span></span></td>
<td><span data-ttu-id="9ebda-335">最初のレコードだけをフェッチするために <code>select</code> 文で使用されます。</span><span class="sxs-lookup"><span data-stu-id="9ebda-335">Used in <code>select</code> statements to fetch only the first record.</span></span> <span data-ttu-id="9ebda-336"><code>firstOnly</code> キーワードは、X++ SQL <code>select</code> ステートメントによって最大 1 つのレコードの取得されることを保証しません。</span><span class="sxs-lookup"><span data-stu-id="9ebda-336">The <code>firstOnly</code> keyword does not guarantee that a maximum of one record is retrieved by an X++ SQL <code>select</code> statement.</span></span> <span data-ttu-id="9ebda-337">AOS が <code>EntireTable</code> キャッシュを使用し、<code>select</code> ステートメントのデータ要求を満たすことができる場合は、<code>firstOnly</code> キーワードは無視されます。</span><span class="sxs-lookup"><span data-stu-id="9ebda-337">If the AOS can use the <code>EntireTable</code> cache to satisfy the data demands of the <code>select</code> statement, the <code>firstOnly</code> keyword is ignored.</span></span></td>
<td><span data-ttu-id="9ebda-338">ステートメント構文セットに基づくキャッシュを選択</span><span class="sxs-lookup"><span data-stu-id="9ebda-338">Select Statement Syntax Set-based Caching</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9ebda-339"><strong>firstOnly10</strong></span><span class="sxs-lookup"><span data-stu-id="9ebda-339"><strong>firstOnly10</strong></span></span></td>
<td><span data-ttu-id="9ebda-340"><strong>firstOnly</strong> と同じ。ただし、1 行ではなく 10 行を返します。</span><span class="sxs-lookup"><span data-stu-id="9ebda-340">Same as <strong>firstOnly</strong>, except returns 10 rows instead of one.</span></span></td>
<td></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9ebda-341"><strong>firstOnly100</strong></span><span class="sxs-lookup"><span data-stu-id="9ebda-341"><strong>firstOnly100</strong></span></span></td>
<td><span data-ttu-id="9ebda-342"><strong>firstOnly</strong> と同じ。ただし、1 行ではなく 100 行を返します。</span><span class="sxs-lookup"><span data-stu-id="9ebda-342">Same as <strong>firstOnly</strong>, except returns 100 rows instead of one.</span></span></td>
<td></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9ebda-343"><strong>firstOnly1000</strong></span><span class="sxs-lookup"><span data-stu-id="9ebda-343"><strong>firstOnly1000</strong></span></span></td>
<td><span data-ttu-id="9ebda-344"><strong>firstOnly</strong> と同じ。ただし、1 行ではなく 1000 行を返します。</span><span class="sxs-lookup"><span data-stu-id="9ebda-344">Same as <strong>firstOnly</strong>, except returns 1000 rows instead of one.</span></span></td>
<td></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9ebda-345"><strong>フラッシュ</strong></span><span class="sxs-lookup"><span data-stu-id="9ebda-345"><strong>flush</strong></span></span></td>
<td><span data-ttu-id="9ebda-346">テーブル キャッシュ全体をクリアします。</span><span class="sxs-lookup"><span data-stu-id="9ebda-346">Clears an entire table cache.</span></span> <span data-ttu-id="9ebda-347"><code>flush</code> ステートメントの構文を次に示します: <code>YourTable ytBuffer;</code>  <code>flush ytBuffer;</code></span><span class="sxs-lookup"><span data-stu-id="9ebda-347">Here is the syntax for the <code>flush</code> statement: <code>YourTable ytBuffer;</code>  <code>flush ytBuffer;</code></span></span></td>
<td><span data-ttu-id="9ebda-348">セット ベースのキャッシュ</span><span class="sxs-lookup"><span data-stu-id="9ebda-348">Set-based Caching</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9ebda-349"><strong>の</strong></span><span class="sxs-lookup"><span data-stu-id="9ebda-349"><strong>for</strong></span></span></td>
<td><span data-ttu-id="9ebda-350">ループの繰り返し用。</span><span class="sxs-lookup"><span data-stu-id="9ebda-350">For loop iteration.</span></span></td>
<td><span data-ttu-id="9ebda-351">ループ用</span><span class="sxs-lookup"><span data-stu-id="9ebda-351">For Loops</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9ebda-352"><strong>forceLiterals</strong></span><span class="sxs-lookup"><span data-stu-id="9ebda-352"><strong>forceLiterals</strong></span></span></td>
<td><span data-ttu-id="9ebda-353"><code>select</code> 文で使用され、最適化時に <code>where</code> 句で使用される実際の値を Microsoft SQL Server データベースに公開しないようにカーネルに指示します。</span><span class="sxs-lookup"><span data-stu-id="9ebda-353">Used in <code>select</code> statements to reveal actual values that are used in <code>where</code> clauses to the Microsoft SQL Server database at the time of optimization.</span></span></td>
<td><span data-ttu-id="9ebda-354">ステートメント構文の選択</span><span class="sxs-lookup"><span data-stu-id="9ebda-354">Select Statement Syntax</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9ebda-355"><strong>forceNestedLoop</strong></span><span class="sxs-lookup"><span data-stu-id="9ebda-355"><strong>forceNestedLoop</strong></span></span></td>
<td><span data-ttu-id="9ebda-356">SQL Server データベースがネストループ アルゴリズムを使用して、<code>join</code> を含む特定の SQL ステートメントを処理するよう強制します。</span><span class="sxs-lookup"><span data-stu-id="9ebda-356">Forces the SQL Server database to use a nested-loop algorithm to process a particular SQL statement containing a <code>join</code>.</span></span></td>
<td><span data-ttu-id="9ebda-357">ステートメント構文の選択</span><span class="sxs-lookup"><span data-stu-id="9ebda-357">Select Statement Syntax</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9ebda-358"><strong>forcePlaceholders</strong></span><span class="sxs-lookup"><span data-stu-id="9ebda-358"><strong>forcePlaceholders</strong></span></span></td>
<td><span data-ttu-id="9ebda-359"> <code>select</code> 文で使用され、最適化時に <code>where</code> 句で使用される実際の値を Microsoft SQL Server データベースに公開しないようにカーネルに指示します。</span><span class="sxs-lookup"><span data-stu-id="9ebda-359">Used in <code>select</code> statements to instruct the kernel not to reveal the actual values used in <code>where</code> clauses to the Microsoft SQL Server database at the time of optimization.</span></span></td>
<td><span data-ttu-id="9ebda-360">ステートメント構文の選択</span><span class="sxs-lookup"><span data-stu-id="9ebda-360">Select Statement Syntax</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9ebda-361"><strong>forceSelectOrder</strong></span><span class="sxs-lookup"><span data-stu-id="9ebda-361"><strong>forceSelectOrder</strong></span></span></td>
<td><span data-ttu-id="9ebda-362">SQL Server データベースが指定した順序で結合内のテーブルにアクセスするよう強制します。</span><span class="sxs-lookup"><span data-stu-id="9ebda-362">Forces the SQL Server database to access the tables in a join in the specified order.</span></span></td>
<td><span data-ttu-id="9ebda-363">ステートメント構文の選択</span><span class="sxs-lookup"><span data-stu-id="9ebda-363">Select Statement Syntax</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9ebda-364"><strong>forUpdate</strong></span><span class="sxs-lookup"><span data-stu-id="9ebda-364"><strong>forUpdate</strong></span></span></td>
<td><span data-ttu-id="9ebda-365">更新専用のレコードを選択します。</span><span class="sxs-lookup"><span data-stu-id="9ebda-365">Selects records exclusively for update.</span></span> <span data-ttu-id="9ebda-366">フェッチされたレコードに対して実行される操作は更新です。</span><span class="sxs-lookup"><span data-stu-id="9ebda-366">The operation to be performed on the records that are fetched is an update.</span></span> <span data-ttu-id="9ebda-367">基になるデータベースによっては、レコードが他のユーザーのためにロックされることがあります。</span><span class="sxs-lookup"><span data-stu-id="9ebda-367">Depending on the underlying database, the records may be locked for other users.</span></span></td>
<td><span data-ttu-id="9ebda-368">ステートメント構文の選択</span><span class="sxs-lookup"><span data-stu-id="9ebda-368">Select Statement Syntax</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9ebda-369"><strong>開始</strong></span><span class="sxs-lookup"><span data-stu-id="9ebda-369"><strong>from</strong></span></span></td>
<td><span data-ttu-id="9ebda-370"><code>select</code> ステートメントの部分。</span><span class="sxs-lookup"><span data-stu-id="9ebda-370">Part of a <code>select</code> statement.</span></span> <span data-ttu-id="9ebda-371"><code>from</code> 句は、列が存在するテーブルを指定します。</span><span class="sxs-lookup"><span data-stu-id="9ebda-371">The <code>from</code> clause specifies the table in which the columns exists.</span></span></td>
<td><span data-ttu-id="9ebda-372">ステートメント構文の選択</span><span class="sxs-lookup"><span data-stu-id="9ebda-372">Select Statement Syntax</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9ebda-373"><strong>グループ</strong></span><span class="sxs-lookup"><span data-stu-id="9ebda-373"><strong>group</strong></span></span></td>
<td><span data-ttu-id="9ebda-374"><code>select</code> ステートメントの <code>group by</code> 句の一部。</span><span class="sxs-lookup"><span data-stu-id="9ebda-374">Part of the <code>group by</code> clause in a <code>select</code> statement.</span></span></td>
<td><span data-ttu-id="9ebda-375">ステートメント構文の選択</span><span class="sxs-lookup"><span data-stu-id="9ebda-375">Select Statement Syntax</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9ebda-376"><strong>次の場合</strong></span><span class="sxs-lookup"><span data-stu-id="9ebda-376"><strong>if</strong></span></span></td>
<td><span data-ttu-id="9ebda-377">条件付き実行。</span><span class="sxs-lookup"><span data-stu-id="9ebda-377">Conditional execution.</span></span></td>
<td><span data-ttu-id="9ebda-378">if および if ... else ステートメント</span><span class="sxs-lookup"><span data-stu-id="9ebda-378">if and if ... else Statements</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9ebda-379"><strong>実装</strong></span><span class="sxs-lookup"><span data-stu-id="9ebda-379"><strong>implements</strong></span></span></td>
<td><span data-ttu-id="9ebda-380">インターフェイスを実装します。</span><span class="sxs-lookup"><span data-stu-id="9ebda-380">Implements an interface.</span></span></td>
<td><span data-ttu-id="9ebda-381">インターフェイスの概要</span><span class="sxs-lookup"><span data-stu-id="9ebda-381">Interfaces Overview</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9ebda-382"><strong>insert_recordset</strong></span><span class="sxs-lookup"><span data-stu-id="9ebda-382"><strong>insert_recordset</strong></span></span></td>
<td><span data-ttu-id="9ebda-383">単一のサーバー トリップで、1 つ以上のテーブルのデータを 1 つの行先テーブルにコピーします。</span><span class="sxs-lookup"><span data-stu-id="9ebda-383">Copies data from one or more tables into one resulting destination table on a single server trip.</span></span></td>
<td><span data-ttu-id="9ebda-384">insert_recordset</span><span class="sxs-lookup"><span data-stu-id="9ebda-384">insert_recordset</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9ebda-385"><strong>int</strong></span><span class="sxs-lookup"><span data-stu-id="9ebda-385"><strong>int</strong></span></span></td>
<td><span data-ttu-id="9ebda-386">型 <code>integer</code> の変数を指定します (32 ビット)。</span><span class="sxs-lookup"><span data-stu-id="9ebda-386">Specifies a variable of type <code>integer</code> (32-bit).</span></span></td>
<td><span data-ttu-id="9ebda-387">整数</span><span class="sxs-lookup"><span data-stu-id="9ebda-387">Integers</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9ebda-388"><strong>int64</strong></span><span class="sxs-lookup"><span data-stu-id="9ebda-388"><strong>int64</strong></span></span></td>
<td><span data-ttu-id="9ebda-389">型 <code>integer</code> の変数を指定します (64 ビット)。</span><span class="sxs-lookup"><span data-stu-id="9ebda-389">Specifies a variable of type <code>integer</code> (64-bit).</span></span></td>
<td><span data-ttu-id="9ebda-390">整数</span><span class="sxs-lookup"><span data-stu-id="9ebda-390">Integers</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9ebda-391"><strong>インターフェイス</strong></span><span class="sxs-lookup"><span data-stu-id="9ebda-391"><strong>interface</strong></span></span></td>
<td><span data-ttu-id="9ebda-392">インターフェイスの宣言。</span><span class="sxs-lookup"><span data-stu-id="9ebda-392">Interface declaration.</span></span></td>
<td><span data-ttu-id="9ebda-393">インターフェイスの概要</span><span class="sxs-lookup"><span data-stu-id="9ebda-393">Interfaces Overview</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9ebda-394"><strong>は</strong></span><span class="sxs-lookup"><span data-stu-id="9ebda-394"><strong>is</strong></span></span></td>
<td><span data-ttu-id="9ebda-395">クラス変数によって照会されるオブジェクトが指定されたクラスから継承するか、または指定されたクラスのものであるかを確認します。</span><span class="sxs-lookup"><span data-stu-id="9ebda-395">Asks whether the object referenced by a class variable either inherits from the given class or is of the given class.</span></span> <span data-ttu-id="9ebda-396">たとえば、<code>Base</code>クラスを<strong>拡張</strong>する指定された <code>Derived</code> クラスでは、式の <code>(myDerived is Base)</code> は <strong>true</strong> を返します。</span><span class="sxs-lookup"><span data-stu-id="9ebda-396">For example, given a <code>Derived</code> class that <strong>extends</strong> a <code>Base</code> class, the expression <code>(myDerived is Base)</code> returns <strong>true</strong>.</span></span> <span data-ttu-id="9ebda-397">このキーワードは、クラスの継承とテーブルの継承に適用されます。</span><span class="sxs-lookup"><span data-stu-id="9ebda-397">This keyword applies to class inheritance and table inheritance.</span></span></td>
<td><span data-ttu-id="9ebda-398">式の演算子: 継承の Is および As</span><span class="sxs-lookup"><span data-stu-id="9ebda-398">Expression Operators: Is and As for Inheritance</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9ebda-399"><strong>結合</strong></span><span class="sxs-lookup"><span data-stu-id="9ebda-399"><strong>join</strong></span></span></td>
<td><span data-ttu-id="9ebda-400">テーブルは、両方のテーブルに共通の列に結合されます。</span><span class="sxs-lookup"><span data-stu-id="9ebda-400">Tables are joined on columns common to both tables.</span></span> <span data-ttu-id="9ebda-401">結合を使用することにより複数のテーブルに基づく単一の結果セットを生成することができます。</span><span class="sxs-lookup"><span data-stu-id="9ebda-401">You can generate a single result set based on multiple tables through the use of joins.</span></span></td>
<td><span data-ttu-id="9ebda-402">ステートメント構文の選択</span><span class="sxs-lookup"><span data-stu-id="9ebda-402">Select Statement Syntax</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9ebda-403"><strong>等号</strong></span><span class="sxs-lookup"><span data-stu-id="9ebda-403"><strong>like</strong></span></span></td>
<td><span data-ttu-id="9ebda-404">ワイルドカード文字 \* および ? を使って、パターンにより一致をテストします。</span><span class="sxs-lookup"><span data-stu-id="9ebda-404">Tests for matches by pattern, with wildcard symbols \* and ?.</span></span> <span data-ttu-id="9ebda-405"><code>like</code> 演算子の右側の文字列は、バックスラッシュを表すのに 4 つのバックスラッシュ文字を使用する必要があります。</span><span class="sxs-lookup"><span data-stu-id="9ebda-405">The string on the right side of the <code>like</code> operator must use four backslash characters to represent one backslash.</span></span> <span data-ttu-id="9ebda-406">例は以下に:</span><span class="sxs-lookup"><span data-stu-id="9ebda-406">Examples follow:</span></span>
<ul>
<li><span data-ttu-id="9ebda-407"><span class="code">(&quot;&amp;quot; like &quot;</em>&lt;em&gt;&quot; )</span> // false に解決されています。</span><span class="sxs-lookup"><span data-stu-id="9ebda-407"><span class="code">(&quot;&amp;quot; like &quot;</em>&lt;em&gt;&quot; )</span> //Resolves to false.</span></span></li>
<li><span data-ttu-id="9ebda-408"><span class="code">(&quot;&amp;quot; like &quot;</em>\*&quot;)</span> // true に解決されています。</span><span class="sxs-lookup"><span data-stu-id="9ebda-408"><span class="code">(&quot;&amp;quot; like &quot;</em>\*&quot;)</span> //Resolves to true.</span></span></li>
</ul></td>
<td><span data-ttu-id="9ebda-409">リレーショナル演算子</span><span class="sxs-lookup"><span data-stu-id="9ebda-409">Relational Operators</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9ebda-410"><strong>maxof</strong></span><span class="sxs-lookup"><span data-stu-id="9ebda-410"><strong>maxof</strong></span></span></td>
<td><span data-ttu-id="9ebda-411"><code>group by</code> 句により指定された行からフィールドの最大値を返します。</span><span class="sxs-lookup"><span data-stu-id="9ebda-411">Returns the maximum of the fields from the rows specified by the <code>group by</code> clause.</span></span></td>
<td><span data-ttu-id="9ebda-412">ステートメント構文の選択</span><span class="sxs-lookup"><span data-stu-id="9ebda-412">Select Statement Syntax</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9ebda-413"><strong>minof</strong></span><span class="sxs-lookup"><span data-stu-id="9ebda-413"><strong>minof</strong></span></span></td>
<td><span data-ttu-id="9ebda-414"><code>group by</code> 句により指定された行からフィールドの最小値を返します。</span><span class="sxs-lookup"><span data-stu-id="9ebda-414">Returns the minimum of the fields from the rows specified by the <code>group by</code> clause.</span></span></td>
<td><span data-ttu-id="9ebda-415">ステートメント構文の選択</span><span class="sxs-lookup"><span data-stu-id="9ebda-415">Select Statement Syntax</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9ebda-416"><strong>mod</strong></span><span class="sxs-lookup"><span data-stu-id="9ebda-416"><strong>mod</strong></span></span></td>
<td><span data-ttu-id="9ebda-417">左側の expression1 の整数剰余を右側の expression2 で除算したものを返します。</span><span class="sxs-lookup"><span data-stu-id="9ebda-417">Returns the integer remainder of the left expression1 divided by the right expression2.</span></span> <span data-ttu-id="9ebda-418">非公式に、これは剰余演算子と呼ばれることもあります。</span><span class="sxs-lookup"><span data-stu-id="9ebda-418">Informally this is sometimes called the modulo operator.</span></span> <span data-ttu-id="9ebda-419"><code>((12 mod 7) == 5)</code> は true。</span><span class="sxs-lookup"><span data-stu-id="9ebda-419"><code>((12 mod 7) == 5)</code> is true.</span></span></td>
<td></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9ebda-420"><strong>新規</strong></span><span class="sxs-lookup"><span data-stu-id="9ebda-420"><strong>new</strong></span></span></td>
<td><span data-ttu-id="9ebda-421">演算子。</span><span class="sxs-lookup"><span data-stu-id="9ebda-421">Operator.</span></span> <span data-ttu-id="9ebda-422">指定されたクラス/インタフェース参照変数と割り当て互換性のある匿名クラスのインスタンスを作成するか、配列のメモリを割り当てます。</span><span class="sxs-lookup"><span data-stu-id="9ebda-422">Creates an instance of an anonymous class that is assignment-compatible with the named class/interface reference variables, or allocates memory for an array.</span></span></td>
<td></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9ebda-423"><strong>次へ</strong></span><span class="sxs-lookup"><span data-stu-id="9ebda-423"><strong>next</strong></span></span></td>
<td><span data-ttu-id="9ebda-424">テーブルの次のレコードをフェッチします。</span><span class="sxs-lookup"><span data-stu-id="9ebda-424">Fetches the next record in a table.</span></span></td>
<td></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9ebda-425"><strong>noFetch</strong></span><span class="sxs-lookup"><span data-stu-id="9ebda-425"><strong>noFetch</strong></span></span></td>
<td><span data-ttu-id="9ebda-426">現時点でフェッチされるレコードがないことを示します。</span><span class="sxs-lookup"><span data-stu-id="9ebda-426">Indicates that no records are to be fetched at present.</span></span></td>
<td><span data-ttu-id="9ebda-427">ステートメント構文の選択</span><span class="sxs-lookup"><span data-stu-id="9ebda-427">Select Statement Syntax</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9ebda-428"><strong>notExists</strong></span><span class="sxs-lookup"><span data-stu-id="9ebda-428"><strong>notExists</strong></span></span></td>
<td><span data-ttu-id="9ebda-429"><code>select</code> 文の <code>join</code> 句で使用されます。</span><span class="sxs-lookup"><span data-stu-id="9ebda-429">Used with <code>join</code> clauses in <code>select</code> statements.</span></span></td>
<td><span data-ttu-id="9ebda-430">ステートメント構文の選択</span><span class="sxs-lookup"><span data-stu-id="9ebda-430">Select Statement Syntax</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9ebda-431"><strong>NULL</strong></span><span class="sxs-lookup"><span data-stu-id="9ebda-431"><strong>null</strong></span></span></td>
<td><span data-ttu-id="9ebda-432">記号定数。</span><span class="sxs-lookup"><span data-stu-id="9ebda-432">Symbolic constant.</span></span></td>
<td></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9ebda-433"><strong>optimisticLock</strong></span><span class="sxs-lookup"><span data-stu-id="9ebda-433"><strong>optimisticLock</strong></span></span></td>
<td><span data-ttu-id="9ebda-434">テーブルに異なる値が設定されていても、オプティミスティック同時実行制御でステートメントを実行するよう強制します。</span><span class="sxs-lookup"><span data-stu-id="9ebda-434">Forces a statement to run with optimistic concurrency control, even if a different value is set on the table.</span></span></td>
<td><span data-ttu-id="9ebda-435">ステートメント構文の選択</span><span class="sxs-lookup"><span data-stu-id="9ebda-435">Select Statement Syntax</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9ebda-436"><strong>注文</strong></span><span class="sxs-lookup"><span data-stu-id="9ebda-436"><strong>order</strong></span></span></td>
<td><span data-ttu-id="9ebda-437"><code>select</code> ステートメントの <code>order by</code> 句の一部。</span><span class="sxs-lookup"><span data-stu-id="9ebda-437">Part of the <code>order by</code> clause in a <code>select</code> statement.</span></span></td>
<td><span data-ttu-id="9ebda-438">ステートメント構文の選択</span><span class="sxs-lookup"><span data-stu-id="9ebda-438">Select Statement Syntax</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9ebda-439"><strong>外部</strong></span><span class="sxs-lookup"><span data-stu-id="9ebda-439"><strong>outer</strong></span></span></td>
<td><span data-ttu-id="9ebda-440"><span class="keyword">外部結合</span>。</span><span class="sxs-lookup"><span data-stu-id="9ebda-440"><span class="keyword">outer join</span>.</span></span></td>
<td><span data-ttu-id="9ebda-441">ステートメント構文の選択</span><span class="sxs-lookup"><span data-stu-id="9ebda-441">Select Statement Syntax</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9ebda-442"><strong>一時停止</strong></span><span class="sxs-lookup"><span data-stu-id="9ebda-442"><strong>pause</strong></span></span></td>
<td><span data-ttu-id="9ebda-443">ジョブの実行を停止させます。</span><span class="sxs-lookup"><span data-stu-id="9ebda-443">Halts the execution of a job.</span></span> <span data-ttu-id="9ebda-444">実行を続行する必要があるかどうかを確認するメッセージが表示されます。</span><span class="sxs-lookup"><span data-stu-id="9ebda-444">The user is asked to state whether execution should continue.</span></span></td>
<td><span data-ttu-id="9ebda-445">ステートメントの選択</span><span class="sxs-lookup"><span data-stu-id="9ebda-445">Select Statements</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9ebda-446"><strong>pessimisticLock</strong></span><span class="sxs-lookup"><span data-stu-id="9ebda-446"><strong>pessimisticLock</strong></span></span></td>
<td><span data-ttu-id="9ebda-447">テーブルに異なる値が設定されていても、ペシミスティック同時実行制御でステートメントを実行するよう強制します。</span><span class="sxs-lookup"><span data-stu-id="9ebda-447">Forces a statement to run with pessimistic concurrency control, even if a different value is set on the table.</span></span></td>
<td><span data-ttu-id="9ebda-448">ステートメント構文の選択</span><span class="sxs-lookup"><span data-stu-id="9ebda-448">Select Statement Syntax</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9ebda-449"><strong>印刷</strong></span><span class="sxs-lookup"><span data-stu-id="9ebda-449"><strong>print</strong></span></span></td>
<td><span data-ttu-id="9ebda-450">スクリーン上にディスプレイ出力を表示できます。</span><span class="sxs-lookup"><span data-stu-id="9ebda-450">Allows you to display output on the screen.</span></span></td>
<td><span data-ttu-id="9ebda-451">ステートメントの印刷</span><span class="sxs-lookup"><span data-stu-id="9ebda-451">Print Statements</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9ebda-452"><strong>プライベート</strong></span><span class="sxs-lookup"><span data-stu-id="9ebda-452"><strong>private</strong></span></span></td>
<td><span data-ttu-id="9ebda-453">メソッドのアクセス修飾子。</span><span class="sxs-lookup"><span data-stu-id="9ebda-453">Method access modifier.</span></span></td>
<td><span data-ttu-id="9ebda-454">メソッド アクセス制御</span><span class="sxs-lookup"><span data-stu-id="9ebda-454">Method Access Control</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9ebda-455"><strong>保護</strong></span><span class="sxs-lookup"><span data-stu-id="9ebda-455"><strong>protected</strong></span></span></td>
<td><span data-ttu-id="9ebda-456">メソッドのアクセス修飾子。</span><span class="sxs-lookup"><span data-stu-id="9ebda-456">Method access modifier.</span></span></td>
<td><span data-ttu-id="9ebda-457">メソッド アクセス制御</span><span class="sxs-lookup"><span data-stu-id="9ebda-457">Method Access Control</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9ebda-458"><strong>パブリック</strong></span><span class="sxs-lookup"><span data-stu-id="9ebda-458"><strong>public</strong></span></span></td>
<td><span data-ttu-id="9ebda-459">メソッドのアクセス修飾子。</span><span class="sxs-lookup"><span data-stu-id="9ebda-459">Method access modifier.</span></span></td>
<td><span data-ttu-id="9ebda-460">メソッド アクセス制御</span><span class="sxs-lookup"><span data-stu-id="9ebda-460">Method Access Control</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9ebda-461"><strong>実質</strong></span><span class="sxs-lookup"><span data-stu-id="9ebda-461"><strong>real</strong></span></span></td>
<td><span data-ttu-id="9ebda-462">型 <code>real</code> の変数を指定します。</span><span class="sxs-lookup"><span data-stu-id="9ebda-462">Specifies a variable of type <code>real</code>.</span></span></td>
<td><span data-ttu-id="9ebda-463">Reals</span><span class="sxs-lookup"><span data-stu-id="9ebda-463">Reals</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9ebda-464"><strong>repeatableRead</strong></span><span class="sxs-lookup"><span data-stu-id="9ebda-464"><strong>repeatableRead</strong></span></span></td>
<td><span data-ttu-id="9ebda-465">現在の取引が完了するまで、現在の取引内のロジックによって読み取られたデータを変更できる他の取引がないことを指定します。</span><span class="sxs-lookup"><span data-stu-id="9ebda-465">Specifies that no other transactions can modify data that has been read by logic inside the current transaction, until after the current transaction completes.</span></span> <span data-ttu-id="9ebda-466">明示的なトランザクションは <strong>ttsAbort</strong> または最も外側の <strong>ttsCommit</strong> で完了します。</span><span class="sxs-lookup"><span data-stu-id="9ebda-466">An explicit transaction completes at either <strong>ttsAbort</strong> or at the outermost <strong>ttsCommit</strong>.</span></span> <span data-ttu-id="9ebda-467">スタンドアロンの <strong>select</strong> 明細書では、トランザクション期間は <strong>select</strong> コマンドの期間です。</span><span class="sxs-lookup"><span data-stu-id="9ebda-467">For a stand-alone <strong>select</strong> statement, the transaction duration is the duration of the <strong>select</strong> command.</span></span> <span data-ttu-id="9ebda-468">ただし、X++ コードで表示されるこのキーワードなしでも (データベースがテーブルをどのようにスキャンするかに応じて)、データベースは時に、個々の<strong>選択</strong>ステートメントの <strong>repeatableRead</strong> と同等のものを実施します。</span><span class="sxs-lookup"><span data-stu-id="9ebda-468">However, the database sometimes enforces the equivalent of <strong>repeatableRead</strong> in individual <strong>select</strong> statements even without this keyword appearing in your X++ code (depending on how the database decides to scan the tables).</span></span></td>
<td><span data-ttu-id="9ebda-469">詳細については、「基になるリレーショナル データベース製品のドキュメント」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="9ebda-469">For more information, see the documentation for the underlying relational database product.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9ebda-470"><strong>再試行</strong></span><span class="sxs-lookup"><span data-stu-id="9ebda-470"><strong>retry</strong></span></span></td>
<td><span data-ttu-id="9ebda-471">例外処理で使用されます。</span><span class="sxs-lookup"><span data-stu-id="9ebda-471">Used in exception handling.</span></span></td>
<td><span data-ttu-id="9ebda-472">トライおよびキャッチ キーワードの例外処理</span><span class="sxs-lookup"><span data-stu-id="9ebda-472">Exception Handling with try and catch Keywords</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9ebda-473"><strong>戻る</strong></span><span class="sxs-lookup"><span data-stu-id="9ebda-473"><strong>return</strong></span></span></td>
<td><span data-ttu-id="9ebda-474">メソッドから終了します。</span><span class="sxs-lookup"><span data-stu-id="9ebda-474">Exits from a method.</span></span></td>
<td><span data-ttu-id="9ebda-475">メソッドの宣言</span><span class="sxs-lookup"><span data-stu-id="9ebda-475">Declaration of Methods</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9ebda-476"><strong>リバース</strong></span><span class="sxs-lookup"><span data-stu-id="9ebda-476"><strong>reverse</strong></span></span></td>
<td><span data-ttu-id="9ebda-477">レコードが逆の順序で返されます。</span><span class="sxs-lookup"><span data-stu-id="9ebda-477">Records are returned in reverse order.</span></span></td>
<td><span data-ttu-id="9ebda-478">ステートメント構文の選択</span><span class="sxs-lookup"><span data-stu-id="9ebda-478">Select Statement Syntax</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9ebda-479"><strong>選択</strong></span><span class="sxs-lookup"><span data-stu-id="9ebda-479"><strong>select</strong></span></span></td>
<td><span data-ttu-id="9ebda-480"><code>select</code> 句は、結果セットに表示される列またはビューを指定します。</span><span class="sxs-lookup"><span data-stu-id="9ebda-480">The <code>select</code> clause designates which columns or views are shown in the result set.</span></span></td>
<td><span data-ttu-id="9ebda-481">ステートメントの選択</span><span class="sxs-lookup"><span data-stu-id="9ebda-481">Select Statements</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9ebda-482"><strong>サーバー</strong></span><span class="sxs-lookup"><span data-stu-id="9ebda-482"><strong>server</strong></span></span></td>
<td><span data-ttu-id="9ebda-483">メソッド モディファイアー｡</span><span class="sxs-lookup"><span data-stu-id="9ebda-483">Method modifier.</span></span></td>
<td><span data-ttu-id="9ebda-484">メソッド モディファイアー</span><span class="sxs-lookup"><span data-stu-id="9ebda-484">Method Modifiers</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9ebda-485"><strong>設定</strong></span><span class="sxs-lookup"><span data-stu-id="9ebda-485"><strong>setting</strong></span></span></td>
<td><span data-ttu-id="9ebda-486"><span class="code">update_recordset</span> コマンドで使用されます。</span><span class="sxs-lookup"><span data-stu-id="9ebda-486">Used with the <span class="code">update_recordset</span> command.</span></span></td>
<td><span data-ttu-id="9ebda-487">update_recordset</span><span class="sxs-lookup"><span data-stu-id="9ebda-487">update_recordset</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9ebda-488"><strong>静的</strong></span><span class="sxs-lookup"><span data-stu-id="9ebda-488"><strong>static</strong></span></span></td>
<td><span data-ttu-id="9ebda-489">静的メソッドはインスタンス変数を参照できません (静的変数のみ)。クラスのインスタンスではなく、クラス名を使用して呼び出すことができます (&quot;<code>MyClass.aStaticProcedure</code>&quot;)。</span><span class="sxs-lookup"><span data-stu-id="9ebda-489">Static methods may not refer to instance variables (only to static variables); may be invoked by using the class name rather than on an instance of the class (&quot;<code>MyClass.aStaticProcedure</code>&quot;).</span></span></td>
<td><span data-ttu-id="9ebda-490">メソッド モディファイアー</span><span class="sxs-lookup"><span data-stu-id="9ebda-490">Method Modifiers</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9ebda-491"><strong>str</strong></span><span class="sxs-lookup"><span data-stu-id="9ebda-491"><strong>str</strong></span></span></td>
<td><span data-ttu-id="9ebda-492">型 <code>string</code> の変数を指定します。</span><span class="sxs-lookup"><span data-stu-id="9ebda-492">Specifies a variable of type <code>string</code>.</span></span></td>
<td><span data-ttu-id="9ebda-493">文字列</span><span class="sxs-lookup"><span data-stu-id="9ebda-493">Strings</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9ebda-494"><strong>合計</strong></span><span class="sxs-lookup"><span data-stu-id="9ebda-494"><strong>sum</strong></span></span></td>
<td><span data-ttu-id="9ebda-495"><code>select</code> ステートメント内の <code>group by</code> 句により指定された行からフィールドの合計を返します。</span><span class="sxs-lookup"><span data-stu-id="9ebda-495">Returns the sum of the fields from the rows specified by the <code>group by</code> clause in a <code>select</code> statement.</span></span></td>
<td><span data-ttu-id="9ebda-496">ステートメント構文の選択</span><span class="sxs-lookup"><span data-stu-id="9ebda-496">Select Statement Syntax</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9ebda-497"><strong>スーパー</strong></span><span class="sxs-lookup"><span data-stu-id="9ebda-497"><strong>super</strong></span></span></td>
<td><span data-ttu-id="9ebda-498">現在のメソッドによって上書きされたメソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="9ebda-498">Calls the method that was overridden by the current method.</span></span></td>
<td><span data-ttu-id="9ebda-499">テーブル メソッド</span><span class="sxs-lookup"><span data-stu-id="9ebda-499">Table Methods</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9ebda-500"><strong>切り替え</strong></span><span class="sxs-lookup"><span data-stu-id="9ebda-500"><strong>switch</strong></span></span></td>
<td><span data-ttu-id="9ebda-501">選択ステートメントを切り替えます。</span><span class="sxs-lookup"><span data-stu-id="9ebda-501">Switch selection statement.</span></span></td>
<td><span data-ttu-id="9ebda-502">Switch ステートメント</span><span class="sxs-lookup"><span data-stu-id="9ebda-502">Switch Statements</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9ebda-503"><strong>tableLock</strong></span><span class="sxs-lookup"><span data-stu-id="9ebda-503"><strong>tableLock</strong></span></span></td>
<td><span data-ttu-id="9ebda-504">Obsolete; <strong>tableLock</strong> はクエリで使用できなくなりました。</span><span class="sxs-lookup"><span data-stu-id="9ebda-504">Obsolete; <strong>tableLock</strong> is no longer available.</span></span></td>
<td></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9ebda-505"><strong>この</strong></span><span class="sxs-lookup"><span data-stu-id="9ebda-505"><strong>this</strong></span></span></td>
<td><span data-ttu-id="9ebda-506">クラスの現在のインスタンスへの参照。</span><span class="sxs-lookup"><span data-stu-id="9ebda-506">A reference to the current instance of the class.</span></span> <span data-ttu-id="9ebda-507">クラスのメソッド内の X++ コードで使用されます。</span><span class="sxs-lookup"><span data-stu-id="9ebda-507">Used in X++ code inside a method of the class.</span></span> <span data-ttu-id="9ebda-508">Usクラスの<em>メソッド</em> メンバーを参照するのに使用されますが、クラスの<em>フィールド</em> メンバーは参照されません。<code>public str getFullName()</code></span><span class="sxs-lookup"><span data-stu-id="9ebda-508">Used to reference <em>method</em> members of the class, but not <em>field</em> members of the class.<code>public str getFullName()</code></span></span>  <span data-ttu-id="9ebda-509"><span class="code">{</span>  <span class="code">    // 次のステートメントは 'this' なしではコンパイルできません。</span></span><span class="sxs-lookup"><span data-stu-id="9ebda-509"><span class="code">{</span>  <span class="code">    // Next statement fails to compile without &#39;this.&#39;.</span></span></span>  <span data-ttu-id="9ebda-510"><code>    return this.concatenateFirstAndLastNames();</code>  <span class="code">}</span></span><span class="sxs-lookup"><span data-stu-id="9ebda-510"><code>    return this.concatenateFirstAndLastNames();</code>  <span class="code">}</span></span></span></td>
<td><span data-ttu-id="9ebda-511"><code>element</code> という名前のシステム変数とほぼ同様です。</span><span class="sxs-lookup"><span data-stu-id="9ebda-511">Loosely similar to the system variable that is named <code>element</code>.</span></span> <span data-ttu-id="9ebda-512">フォーム コントロール メソッドの <code>element</code> を使用して、格納フォームを参照します。</span><span class="sxs-lookup"><span data-stu-id="9ebda-512">You use <code>element</code> in form control methods to reference the containing form.</span></span> <span data-ttu-id="9ebda-513">詳細については、「フォームの変数を使用」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="9ebda-513">For more information, see Using Variables with Forms.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9ebda-514"><strong>スロー</strong></span><span class="sxs-lookup"><span data-stu-id="9ebda-514"><strong>throw</strong></span></span></td>
<td><span data-ttu-id="9ebda-515">例外処理で使用されます。</span><span class="sxs-lookup"><span data-stu-id="9ebda-515">Used in exception handling.</span></span></td>
<td><span data-ttu-id="9ebda-516">トライおよびキャッチ キーワードの例外処理</span><span class="sxs-lookup"><span data-stu-id="9ebda-516">Exception Handling with try and catch Keywords</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9ebda-517"><strong>はい</strong></span><span class="sxs-lookup"><span data-stu-id="9ebda-517"><strong>true</strong></span></span></td>
<td><span data-ttu-id="9ebda-518">ブール型リテラル。</span><span class="sxs-lookup"><span data-stu-id="9ebda-518">Boolean literal.</span></span></td>
<td><span data-ttu-id="9ebda-519">ブール型</span><span class="sxs-lookup"><span data-stu-id="9ebda-519">Booleans</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9ebda-520"><strong>実行</strong></span><span class="sxs-lookup"><span data-stu-id="9ebda-520"><strong>try</strong></span></span></td>
<td><span data-ttu-id="9ebda-521">例外処理で使用されます。</span><span class="sxs-lookup"><span data-stu-id="9ebda-521">Used in exception handling.</span></span></td>
<td><span data-ttu-id="9ebda-522">トライおよびキャッチ キーワードの例外処理</span><span class="sxs-lookup"><span data-stu-id="9ebda-522">Exception Handling with try and catch Keywords</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9ebda-523"><strong>ttsAbort</strong></span><span class="sxs-lookup"><span data-stu-id="9ebda-523"><strong>ttsAbort</strong></span></span></td>
<td><span data-ttu-id="9ebda-524">現在のトランザクションのすべての変更を破棄します。</span><span class="sxs-lookup"><span data-stu-id="9ebda-524">Discards all changes in the current transaction.</span></span></td>
<td><span data-ttu-id="9ebda-525">トランザクションの整合性</span><span class="sxs-lookup"><span data-stu-id="9ebda-525">Transaction Integrity</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9ebda-526"><strong>ttsBegin</strong></span><span class="sxs-lookup"><span data-stu-id="9ebda-526"><strong>ttsBegin</strong></span></span></td>
<td><span data-ttu-id="9ebda-527">トランザクションの開始をマークします。</span><span class="sxs-lookup"><span data-stu-id="9ebda-527">Marks the beginning of a transaction.</span></span></td>
<td><span data-ttu-id="9ebda-528">トランザクションの整合性</span><span class="sxs-lookup"><span data-stu-id="9ebda-528">Transaction Integrity</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9ebda-529"><strong>ttsCommit</strong></span><span class="sxs-lookup"><span data-stu-id="9ebda-529"><strong>ttsCommit</strong></span></span></td>
<td><span data-ttu-id="9ebda-530">トランザクションの終了をマークします。</span><span class="sxs-lookup"><span data-stu-id="9ebda-530">Marks the end of a transaction.</span></span></td>
<td><span data-ttu-id="9ebda-531">トランザクションの整合性</span><span class="sxs-lookup"><span data-stu-id="9ebda-531">Transaction Integrity</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9ebda-532"><strong>update_recordset</strong></span><span class="sxs-lookup"><span data-stu-id="9ebda-532"><strong>update_recordset</strong></span></span></td>
<td><span data-ttu-id="9ebda-533">1 回の工程内で行セットの操作を許可します。</span><span class="sxs-lookup"><span data-stu-id="9ebda-533">Allows the manipulation of row sets within one operation.</span></span></td>
<td><span data-ttu-id="9ebda-534">update_recordset</span><span class="sxs-lookup"><span data-stu-id="9ebda-534">update_recordset</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9ebda-535"><strong>validTimeState</strong></span><span class="sxs-lookup"><span data-stu-id="9ebda-535"><strong>validTimeState</strong></span></span></td>
<td><span data-ttu-id="9ebda-536">X++ SQL <code>select</code> 明細書により有効時間状態テーブルから取得される行をフィルター処理します。</span><span class="sxs-lookup"><span data-stu-id="9ebda-536">Filters rows that are retrieved from a valid time state table by an X++ SQL <code>select</code> statement.</span></span> <span data-ttu-id="9ebda-537">例: <span class="code">xMyTable; から validTimeState(myDateEffective) *を選択</span> ... または ...  <span class="code">xMyTable; から validTimeState(myDateFrom, myDateTo)* を選択</span></span><span class="sxs-lookup"><span data-stu-id="9ebda-537">For example: <span class="code">select validTimeState(myDateEffective) * from xMyTable;</span> ...or...  <span class="code">select validTimeState(myDateFrom, myDateTo) * from xMyTable;</span></span></span></td>
<td><span data-ttu-id="9ebda-538">有効時間状態テーブルが読み取りおよび書き込み操作に及ぼす影響</span><span class="sxs-lookup"><span data-stu-id="9ebda-538">Effects of Valid Time State Tables on Read and Write Operations</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9ebda-539"><strong>無効</strong></span><span class="sxs-lookup"><span data-stu-id="9ebda-539"><strong>void</strong></span></span></td>
<td><span data-ttu-id="9ebda-540">値を返さないメソッドを示します。</span><span class="sxs-lookup"><span data-stu-id="9ebda-540">Identifies a method that does not return a value.</span></span></td>
<td><span data-ttu-id="9ebda-541">メソッドの宣言</span><span class="sxs-lookup"><span data-stu-id="9ebda-541">Declaration of Methods</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9ebda-542"><strong>WHERE</strong></span><span class="sxs-lookup"><span data-stu-id="9ebda-542"><strong>where</strong></span></span></td>
<td><span data-ttu-id="9ebda-543"><code>select</code> ステートメントの部分。</span><span class="sxs-lookup"><span data-stu-id="9ebda-543">Part of a <code>select</code> statement.</span></span> <span data-ttu-id="9ebda-544"><code>where</code> 句は、満たす必要がある条件を指定します。つまり、その結果に含める行です。</span><span class="sxs-lookup"><span data-stu-id="9ebda-544">The <code>where</code> clause specifies the conditions to be satisfied; that is, the rows that you want to include in the result.</span></span></td>
<td><span data-ttu-id="9ebda-545">ステートメント構文の選択</span><span class="sxs-lookup"><span data-stu-id="9ebda-545">Select Statement Syntax</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9ebda-546"><strong>中に</strong></span><span class="sxs-lookup"><span data-stu-id="9ebda-546"><strong>while</strong></span></span></td>
<td><span data-ttu-id="9ebda-547">繰り返しのステートメント。</span><span class="sxs-lookup"><span data-stu-id="9ebda-547">Iteration statement.</span></span> <span data-ttu-id="9ebda-548">テスト条件が該当する時は、明細書またはブロックを繰り返し実行します。</span><span class="sxs-lookup"><span data-stu-id="9ebda-548">Executes a statement or block repeatedly when a test condition is true.</span></span></td>
<td><span data-ttu-id="9ebda-549">While Loop while select ステートメント</span><span class="sxs-lookup"><span data-stu-id="9ebda-549">While Loops while select Statements</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9ebda-550"><strong>ウィンドウ</strong></span><span class="sxs-lookup"><span data-stu-id="9ebda-550"><strong>window</strong></span></span></td>
<td><span data-ttu-id="9ebda-551">出力ウィンドウのサイズを変更できます。</span><span class="sxs-lookup"><span data-stu-id="9ebda-551">Allows you to alter the size of the output window.</span></span></td>
<td><span data-ttu-id="9ebda-552">ステートメントの印刷</span><span class="sxs-lookup"><span data-stu-id="9ebda-552">Print Statements</span></span></td>
</tr>
</tbody>
</table>

## <a name="expressions-syntax"></a><span data-ttu-id="9ebda-553">式の構文</span><span class="sxs-lookup"><span data-stu-id="9ebda-553">Expressions Syntax</span></span>
<span data-ttu-id="9ebda-554">X++ の式は数学的または論理的ないずれかの方法で使用されます。</span><span class="sxs-lookup"><span data-stu-id="9ebda-554">An expression in X++ is used in either a mathematical or logical way.</span></span> <span data-ttu-id="9ebda-555">式は、言語のデータ型に基づいて作成されます。つまり、ある式はある型の値を返します。</span><span class="sxs-lookup"><span data-stu-id="9ebda-555">Expressions are built on the data types of the language; that is, an expression returns a value of some type.</span></span> <span data-ttu-id="9ebda-556">この値は、計算、代入、条件文などで使用できます。</span><span class="sxs-lookup"><span data-stu-id="9ebda-556">This value can be used in calculations, assignments, conditional statements, and so on.</span></span>

### <a name="ebnf-description-of-expressions-in-x"></a><span data-ttu-id="9ebda-557">EBNF Description of Expressions in X++</span><span class="sxs-lookup"><span data-stu-id="9ebda-557">EBNF Description of Expressions in X++</span></span>

|                    |   |                                                             |
|--------------------|---|-------------------------------------------------------------|
|     <span data-ttu-id="9ebda-558">式</span><span class="sxs-lookup"><span data-stu-id="9ebda-558">Expression</span></span>     | = | <span data-ttu-id="9ebda-559">簡易式  \[RelationalOperator Simple-expression \]</span><span class="sxs-lookup"><span data-stu-id="9ebda-559">Simple-expression \[RelationalOperator Simple-expression \]</span></span> |
| <span data-ttu-id="9ebda-560">RelationalOperator</span><span class="sxs-lookup"><span data-stu-id="9ebda-560">RelationalOperator</span></span> | = |                              =                              |
| <span data-ttu-id="9ebda-561">簡易式</span><span class="sxs-lookup"><span data-stu-id="9ebda-561">Simple-expression</span></span>  | = |                   <span data-ttu-id="9ebda-562">簡易式 \[ +</span><span class="sxs-lookup"><span data-stu-id="9ebda-562">Simple-expression \[ +</span></span>                    |
|        <span data-ttu-id="9ebda-563">期間</span><span class="sxs-lookup"><span data-stu-id="9ebda-563">Term</span></span>        | = |           <span data-ttu-id="9ebda-564">Compfactor {複数演算子 CompFactor }</span><span class="sxs-lookup"><span data-stu-id="9ebda-564">Compfactor { Mult-operator CompFactor }</span></span>           |
|   <span data-ttu-id="9ebda-565">複数演算子</span><span class="sxs-lookup"><span data-stu-id="9ebda-565">Mult-operator</span></span>    | = |                             \*                              |
|     <span data-ttu-id="9ebda-566">CompFactor</span><span class="sxs-lookup"><span data-stu-id="9ebda-566">CompFactor</span></span>     | = |                        <span data-ttu-id="9ebda-567">\[ !</span><span class="sxs-lookup"><span data-stu-id="9ebda-567">\[ !</span></span> <span data-ttu-id="9ebda-568">\] \[ -</span><span class="sxs-lookup"><span data-stu-id="9ebda-568">\] \[ -</span></span>                         |
|       <span data-ttu-id="9ebda-569">係数</span><span class="sxs-lookup"><span data-stu-id="9ebda-569">Factor</span></span>       | = |                           <span data-ttu-id="9ebda-570">リテラル</span><span class="sxs-lookup"><span data-stu-id="9ebda-570">Literal</span></span>                           |
|        <span data-ttu-id="9ebda-571">列挙</span><span class="sxs-lookup"><span data-stu-id="9ebda-571">Enum</span></span>        | = |                     <span data-ttu-id="9ebda-572">EnumName :: リテラル</span><span class="sxs-lookup"><span data-stu-id="9ebda-572">EnumName :: Literal</span></span>                     |
|      <span data-ttu-id="9ebda-573">変動</span><span class="sxs-lookup"><span data-stu-id="9ebda-573">Variable</span></span>      | = |    <span data-ttu-id="9ebda-574">識別子 \[ \[ 式 \] \] \[ .</span><span class="sxs-lookup"><span data-stu-id="9ebda-574">Identifier \[ \[ Expression \] \] \[ .</span></span> <span data-ttu-id="9ebda-575">式 \]</span><span class="sxs-lookup"><span data-stu-id="9ebda-575">Expression \]</span></span>     |
|    <span data-ttu-id="9ebda-576">FunctionCall</span><span class="sxs-lookup"><span data-stu-id="9ebda-576">FunctionCall</span></span>    | = |                      <span data-ttu-id="9ebda-577">\[ 式 (.</span><span class="sxs-lookup"><span data-stu-id="9ebda-577">\[ Expression (.</span></span>                       |
|   <span data-ttu-id="9ebda-578">If 式</span><span class="sxs-lookup"><span data-stu-id="9ebda-578">If-expression</span></span>    | = |            <span data-ttu-id="9ebda-579">Expression ?</span><span class="sxs-lookup"><span data-stu-id="9ebda-579">Expression ?</span></span> <span data-ttu-id="9ebda-580">式 : 式</span><span class="sxs-lookup"><span data-stu-id="9ebda-580">Expression : Expression</span></span>             |

<span data-ttu-id="9ebda-581">意味の制限が前述の構文に適用されます。</span><span class="sxs-lookup"><span data-stu-id="9ebda-581">Semantic restrictions apply on the preceding syntax.</span></span> <span data-ttu-id="9ebda-582">:: 演算子を使用するメソッドを呼び出すことはできません。</span><span class="sxs-lookup"><span data-stu-id="9ebda-582">You cannot call any method using the :: operator.</span></span> <span data-ttu-id="9ebda-583">同様に、アーカイブ オブジェクトなしで、つまりメソッドなどの中でなければ、**this** キーワードを使用することはできません。</span><span class="sxs-lookup"><span data-stu-id="9ebda-583">Similarly, you cannot use the **this** keyword without an active object; that is, if you are not within a method and so on.</span></span>

### <a name="examples"></a><span data-ttu-id="9ebda-584">例</span><span class="sxs-lookup"><span data-stu-id="9ebda-584">Examples</span></span>

| <span data-ttu-id="9ebda-585">式の例</span><span class="sxs-lookup"><span data-stu-id="9ebda-585">Example of expression</span></span>                                       | <span data-ttu-id="9ebda-586">説明</span><span class="sxs-lookup"><span data-stu-id="9ebda-586">Description</span></span>                                                                                                                                    |
|-------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| `1`                                                         | <span data-ttu-id="9ebda-587">整数リテラル。</span><span class="sxs-lookup"><span data-stu-id="9ebda-587">An integer literal.</span></span>                                                                                                                            |
| <span data-ttu-id="9ebda-588">NoYes::No</span><span class="sxs-lookup"><span data-stu-id="9ebda-588">NoYes::No</span></span>                                                   | <span data-ttu-id="9ebda-589">列挙参照。</span><span class="sxs-lookup"><span data-stu-id="9ebda-589">An enum-reference.</span></span>                                                                                                                             |
| `A`                                                         | <span data-ttu-id="9ebda-590">変数の参照。</span><span class="sxs-lookup"><span data-stu-id="9ebda-590">A variable-reference.</span></span>                                                                                                                          |
| <span data-ttu-id="9ebda-591">Debtor::Find("1")</span><span class="sxs-lookup"><span data-stu-id="9ebda-591">Debtor::Find("1")</span></span>                                           | <span data-ttu-id="9ebda-592">静的メソッドの呼び出し (顧客変数を返す)。</span><span class="sxs-lookup"><span data-stu-id="9ebda-592">A static method-call (returns a customer variable).</span></span>                                                                                            |
| <span data-ttu-id="9ebda-593">(A &gt; 3 ?</span><span class="sxs-lookup"><span data-stu-id="9ebda-593">(A &gt; 3 ?</span></span> <span data-ttu-id="9ebda-594">true : false)</span><span class="sxs-lookup"><span data-stu-id="9ebda-594">true : false)</span></span>                                   | <span data-ttu-id="9ebda-595">**true** または **false** を返す if 式です。</span><span class="sxs-lookup"><span data-stu-id="9ebda-595">An if-expression that returns **true** or **false**.</span></span>                                                                                           |
| <span data-ttu-id="9ebda-596">(CustTable.Account == 「100」の CustTable を選択します)。NameRef</span><span class="sxs-lookup"><span data-stu-id="9ebda-596">(select CustTable where CustTable.Account == "100").NameRef</span></span> | <span data-ttu-id="9ebda-597">選択式。</span><span class="sxs-lookup"><span data-stu-id="9ebda-597">A select-expression.</span></span> <span data-ttu-id="9ebda-598">顧客テーブルで nameref フィールドを返します。</span><span class="sxs-lookup"><span data-stu-id="9ebda-598">Returns the nameref field in the customer table.</span></span> <span data-ttu-id="9ebda-599">これは文字列です</span><span class="sxs-lookup"><span data-stu-id="9ebda-599">This is a string.</span></span>                                                        |
| <span data-ttu-id="9ebda-600">A &gt;= B</span><span class="sxs-lookup"><span data-stu-id="9ebda-600">A &gt;= B</span></span>                                                   | <span data-ttu-id="9ebda-601">論理式。</span><span class="sxs-lookup"><span data-stu-id="9ebda-601">A logical expression.</span></span> <span data-ttu-id="9ebda-602">**true** または **false** を返します。</span><span class="sxs-lookup"><span data-stu-id="9ebda-602">Returns **true** or **false**.</span></span>                                                                                           |
| <span data-ttu-id="9ebda-603">A + B</span><span class="sxs-lookup"><span data-stu-id="9ebda-603">A + B</span></span>                                                       | <span data-ttu-id="9ebda-604">算術式です。</span><span class="sxs-lookup"><span data-stu-id="9ebda-604">An arithmetic expression.</span></span> <span data-ttu-id="9ebda-605">合計 A と B。</span><span class="sxs-lookup"><span data-stu-id="9ebda-605">Sums A and B.</span></span>                                                                                                        |
| <span data-ttu-id="9ebda-606">A + B / C</span><span class="sxs-lookup"><span data-stu-id="9ebda-606">A + B / C</span></span>                                                   | <span data-ttu-id="9ebda-607">B/C を計算し、これを A に追加します。</span><span class="sxs-lookup"><span data-stu-id="9ebda-607">Calculates B/C, and then adds this to A.</span></span>                                                                                                       |
| <span data-ttu-id="9ebda-608">~A + this.Value()</span><span class="sxs-lookup"><span data-stu-id="9ebda-608">~A + this.Value()</span></span>                                           | <span data-ttu-id="9ebda-609">A 以外のバイナリと、スコープ (this) 内のオブジェクトのメソッド呼び出し値の結果を合計します。</span><span class="sxs-lookup"><span data-stu-id="9ebda-609">Sums binary not A and the result of the method-call Value on the object in scope (this).</span></span>                                                       |
| <span data-ttu-id="9ebda-610">Debtor::Find("1").NameRef</span><span class="sxs-lookup"><span data-stu-id="9ebda-610">Debtor::Find("1").NameRef</span></span>                                   | <span data-ttu-id="9ebda-611">検出された顧客レコードの NameRef フィールドを返します。</span><span class="sxs-lookup"><span data-stu-id="9ebda-611">Returns the NameRef field of the found customer record.</span></span>                                                                                        |
| <span data-ttu-id="9ebda-612">Debtor::Find("1").Balance()</span><span class="sxs-lookup"><span data-stu-id="9ebda-612">Debtor::Find("1").Balance()</span></span>                                 | <span data-ttu-id="9ebda-613">顧客テーブルの `Balance` へのメソッド呼び出し (Debtor::Find は、顧客を返す)。</span><span class="sxs-lookup"><span data-stu-id="9ebda-613">A method call to `Balance` in the customer table (Debtor::Find returns a customer).</span></span> <span data-ttu-id="9ebda-614">口座番号 1 の顧客の残高を返します。</span><span class="sxs-lookup"><span data-stu-id="9ebda-614">Returns the balance of the customer with account number 1.</span></span> |

## <a name="ebnf-overview"></a><span data-ttu-id="9ebda-615">EBNF 概要</span><span class="sxs-lookup"><span data-stu-id="9ebda-615">EBNF Overview</span></span>
<span data-ttu-id="9ebda-616">Extended Backus Naur Form (EBNF) は metalanguage あり、このガイドでは言語構文を説明するために使用されています。</span><span class="sxs-lookup"><span data-stu-id="9ebda-616">Extended Backus Naur Form (EBNF) is a metalanguage and is used in this guide to describe the language syntax.</span></span> <span data-ttu-id="9ebda-617">EBNF 定義は生産ルール、非ターミナル、およびターミナルで構成されます。</span><span class="sxs-lookup"><span data-stu-id="9ebda-617">An EBNF definition consists of production rules, nonterminals, and terminals.</span></span> <span data-ttu-id="9ebda-618">重要な用語は次のテーブルに表示されます。</span><span class="sxs-lookup"><span data-stu-id="9ebda-618">The key terms are shown in the following table.</span></span>


|    <span data-ttu-id="9ebda-619">重要な用語</span><span class="sxs-lookup"><span data-stu-id="9ebda-619">Key terms</span></span>     |       <span data-ttu-id="9ebda-620">例</span><span class="sxs-lookup"><span data-stu-id="9ebda-620">Example</span></span>        |                                                                                                          <span data-ttu-id="9ebda-621">説明</span><span class="sxs-lookup"><span data-stu-id="9ebda-621">Description</span></span>                                                                                                          |
|------------------|----------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|    <span data-ttu-id="9ebda-622">ターミナル</span><span class="sxs-lookup"><span data-stu-id="9ebda-622">Terminals</span></span>     |      <span data-ttu-id="9ebda-623">Work\_Team</span><span class="sxs-lookup"><span data-stu-id="9ebda-623">Work\_Team</span></span>      |                                                                           <span data-ttu-id="9ebda-624">ターミナルは、変更しない 1 文字または文字の文字列です。</span><span class="sxs-lookup"><span data-stu-id="9ebda-624">A terminal is one character or a string of characters that never change.</span></span>                                                                            |
|   <span data-ttu-id="9ebda-625">非ターミナル</span><span class="sxs-lookup"><span data-stu-id="9ebda-625">Nonterminals</span></span>   |      `Employee`      | <span data-ttu-id="9ebda-626">非ターミナルは、生産ルールまたはテキストの説明のいずれかによって定義された言語の有効な文の一部の説明です。</span><span class="sxs-lookup"><span data-stu-id="9ebda-626">A nonterminal is a description of part of a valid sentence in the language that is defined either by a production rule or a textual description.</span></span> <span data-ttu-id="9ebda-627">非ターミナル記号は、1 つまたは複数のターミナル記号にいつでも展開できます。</span><span class="sxs-lookup"><span data-stu-id="9ebda-627">A nonterminal symbol can always be expanded to one or more terminal symbols.</span></span> |
| <span data-ttu-id="9ebda-628">生産ルール</span><span class="sxs-lookup"><span data-stu-id="9ebda-628">Production rules</span></span> | <span data-ttu-id="9ebda-629">従業員 = 開発者</span><span class="sxs-lookup"><span data-stu-id="9ebda-629">Employee = Developer</span></span> |                                                                                                            <span data-ttu-id="9ebda-630">テスト担当者</span><span class="sxs-lookup"><span data-stu-id="9ebda-630">Tester</span></span>                                                                                                             |

### <a name="example"></a><span data-ttu-id="9ebda-631">例</span><span class="sxs-lookup"><span data-stu-id="9ebda-631">Example</span></span>

<span data-ttu-id="9ebda-632">Work\_Team = Manager Employee {, Employee}  Employee = Developer | Tester この例は Work\_Team を `Manager` および一人またはそれ以上の `Employees` で構成されるように定義します。</span><span class="sxs-lookup"><span data-stu-id="9ebda-632">Work\_Team = Manager Employee {, Employee}  Employee = Developer | Tester This example defines a Work\_Team as consisting of a `Manager` and one or more `Employees`.</span></span> <span data-ttu-id="9ebda-633">`Employee` は、`Developer`、または `Tester` として定義されています。</span><span class="sxs-lookup"><span data-stu-id="9ebda-633">An `Employee` is defined as being a `Developer`, or a `Tester`.</span></span> <span data-ttu-id="9ebda-634">この例で使用されているシンボルについては、次の表で説明します。</span><span class="sxs-lookup"><span data-stu-id="9ebda-634">The symbols used in the example are described in the following table.</span></span>

### <a name="special-symbols-in-ebnf"></a><span data-ttu-id="9ebda-635">EBNF の特殊記号</span><span class="sxs-lookup"><span data-stu-id="9ebda-635">Special Symbols in EBNF</span></span>

|         <span data-ttu-id="9ebda-636">記号</span><span class="sxs-lookup"><span data-stu-id="9ebda-636">Symbol</span></span>          |                                                               <span data-ttu-id="9ebda-637">説明</span><span class="sxs-lookup"><span data-stu-id="9ebda-637">Description</span></span>                                                               |
|-------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
|  <span data-ttu-id="9ebda-638">(<em>式</em>)</span><span class="sxs-lookup"><span data-stu-id="9ebda-638">(<em>Expression</em>)</span></span>  | <span data-ttu-id="9ebda-639">かっこには、記号 (ターミナルおよび非ターミナル) がまとめて保持されます。</span><span class="sxs-lookup"><span data-stu-id="9ebda-639">Parentheses hold the symbols (terminals and nonterminals) together.</span></span> <span data-ttu-id="9ebda-640">生産ルールの右側の任意の場所に配置できます。</span><span class="sxs-lookup"><span data-stu-id="9ebda-640">They can be placed anywhere on the right side of a production rule.</span></span> |
|  <span data-ttu-id="9ebda-641"><em>Expression1</em></span><span class="sxs-lookup"><span data-stu-id="9ebda-641"><em>Expression1</em></span></span>   |                                                          <span data-ttu-id="9ebda-642"><em>Expression2</em></span><span class="sxs-lookup"><span data-stu-id="9ebda-642"><em>Expression2</em></span></span>                                                           |
| <span data-ttu-id="9ebda-643">\[<em>式</em>\]</span><span class="sxs-lookup"><span data-stu-id="9ebda-643">\[<em>Expression</em>\]</span></span> |               <span data-ttu-id="9ebda-644">オプション: \[ と \] の間の項目はオプションです。</span><span class="sxs-lookup"><span data-stu-id="9ebda-644">Optional: The items between \[ and \] are optional.</span></span> <span data-ttu-id="9ebda-645">すべてまたはいずれかの項目に括弧が含まれます。</span><span class="sxs-lookup"><span data-stu-id="9ebda-645">All or none of the items in the brackets are included.</span></span>                |
|      <span data-ttu-id="9ebda-646">{Expression}</span><span class="sxs-lookup"><span data-stu-id="9ebda-646">{Expression}</span></span>       |                     <span data-ttu-id="9ebda-647">繰り返し: { と } の間の項目はオプションですが、必要な回数繰り返し実行できます。</span><span class="sxs-lookup"><span data-stu-id="9ebda-647">Repeat: The items between { and } are optional, but can be repeated as many times as necessary.</span></span>                     |

<span data-ttu-id="9ebda-648">たとえば、自転車のために購入するアクセサリがサドル、飲料水ボトル ホルダー、ベル、およびクラクションから成る場合、ベルまたはクラクションのいずれか、および 0 個、1 個、または複数の飲料水ボトル ホルダー、さらにちょうど 1 つのサドルを持つことができ、この場合以下のように表されます: 自転車\_アクセサリ = サドル\[ベル | クラクション\]{飲料水\_ボトル\_ホルダー} この文法は次の選択を定義します。`saddle`  `saddle bell`  `saddle horn`  サドル 飲料水\_ボトル\_ホルダー  サドル ベル 飲料水\_ボトル\_ホルダー  サドル ベル 飲料水\_ボトル\_ホルダー 飲料水\_ボトル\_ホルダーなど。</span><span class="sxs-lookup"><span data-stu-id="9ebda-648">For example, if the accessories you buy for your bicycle consist of a saddle, water-bottle holders, bells, and horns, and you could have either a bell or a horn, and zero, one, or more water bottle holders, and exactly one saddle, this could be expressed as: Bicycle\_Accessories = saddle \[bell | horn\] {water\_bottle\_holders} This grammar defines the following possibilities: `saddle`  `saddle bell`  `saddle horn`  saddle water\_bottle\_holder  saddle bell water\_bottle\_holder  saddle bell water\_bottle\_holder water\_bottle\_holder And so on.</span></span>

## <a name="x-grammar"></a><span data-ttu-id="9ebda-649">X++ 文法</span><span class="sxs-lookup"><span data-stu-id="9ebda-649">X++ Grammar</span></span>
<span data-ttu-id="9ebda-650">このトピックでは、X++ 言語の正式な文法を示します。</span><span class="sxs-lookup"><span data-stu-id="9ebda-650">This topic shows the formal grammar of the X++ language.</span></span>

### <a name="how-to-interpret-the-formal-bnf-grammar"></a><span data-ttu-id="9ebda-651">正式な BNF 文法を解釈する方法</span><span class="sxs-lookup"><span data-stu-id="9ebda-651">How to Interpret the Formal BNF Grammar</span></span>

<span data-ttu-id="9ebda-652">このセクションでは、Backus Naur Form (BNF) の X++ の文法について説明します。</span><span class="sxs-lookup"><span data-stu-id="9ebda-652">This section describes the grammar of X++ in Backus Naur Form (BNF).</span></span> <span data-ttu-id="9ebda-653">次に、BNF の小さな例について説明します。</span><span class="sxs-lookup"><span data-stu-id="9ebda-653">A small example of BNF is described here.</span></span>

<span data-ttu-id="9ebda-654">BNF コード</span><span class="sxs-lookup"><span data-stu-id="9ebda-654">BNF code</span></span>

<span data-ttu-id="9ebda-655">解釈</span><span class="sxs-lookup"><span data-stu-id="9ebda-655">Interpretation</span></span>

<span data-ttu-id="9ebda-656">コードのコピー</span><span class="sxs-lookup"><span data-stu-id="9ebda-656">Copy Code</span></span>

    AA ::= BB  CC_SYM
    BB ::= JJ_SYM
       ::= KK_SYM

 

<span data-ttu-id="9ebda-657">`AA` は生産ルールの名前です。</span><span class="sxs-lookup"><span data-stu-id="9ebda-657">`AA` is the name of a production rule.</span></span> <span data-ttu-id="9ebda-658">`AA` は `BB` が必要で、続いて CC\_SYM となります。</span><span class="sxs-lookup"><span data-stu-id="9ebda-658">An `AA` requires a `BB`, followed by a CC\_SYM.</span></span> <span data-ttu-id="9ebda-659">`BB` も生産ルールです。</span><span class="sxs-lookup"><span data-stu-id="9ebda-659">A `BB` is also a production rule.</span></span> <span data-ttu-id="9ebda-660">したがって、`BB` はターミナルではありません。</span><span class="sxs-lookup"><span data-stu-id="9ebda-660">Therefore, `BB` is not a terminal.</span></span> <span data-ttu-id="9ebda-661">`BB` は、JJ\_SYM または KK\_SYM のいずれかである必要があります。</span><span class="sxs-lookup"><span data-stu-id="9ebda-661">`BB` must be either a JJ\_SYM or a KK\_SYM.</span></span> <span data-ttu-id="9ebda-662">JJ\_SYM と KK\_SYM の両方は他の生産ルールの名前ではないためターミナルです。</span><span class="sxs-lookup"><span data-stu-id="9ebda-662">Both JJ\_SYM and KK\_SYM are terminals because they are not the names of any other production rules.</span></span> <span data-ttu-id="9ebda-663">CC\_SYM もターミナルです。</span><span class="sxs-lookup"><span data-stu-id="9ebda-663">CC\_SYM is also a terminal.</span></span>

<span data-ttu-id="9ebda-664">X++ の文法の BNF で、ターミナルのほとんどに名前の接尾語として \_SYM があります。</span><span class="sxs-lookup"><span data-stu-id="9ebda-664">In the BNF for X++ grammar, most of the terminals have \_SYM as the suffix of their name.</span></span>

### <a name="the-formal-x-grammar-in-bnf"></a><span data-ttu-id="9ebda-665">BNF での正式な X++ 文法</span><span class="sxs-lookup"><span data-stu-id="9ebda-665">The Formal X++ Grammar in BNF</span></span>

<span data-ttu-id="9ebda-666">このセクションには、X++文法を定義する BNF が含まれています。</span><span class="sxs-lookup"><span data-stu-id="9ebda-666">This section contains the BNF that defines the grammar of X++.</span></span>

<span data-ttu-id="9ebda-667">コードのコピー</span><span class="sxs-lookup"><span data-stu-id="9ebda-667">Copy Code</span></span>

    CMPL_UNIT ::= RETTYPEID  FUNC_HDR  FUNC_HEAD  BODY
              ::= RETTYPEID  DATA_HDR  CLASS_DECL
              ::= EXPR_HDR  IF_EXPR  SEMIOPT
              ::= RETTYPEID  FUNC_HDR  EVENT_DECL  BODY
    SEMIOPT ::= SEMICOLON_SYM
            ::= 
    CLASS_DECL ::= CLASS_HEADER  LEFTBR_SYM  DCL_EVENTMAP  DCL_LIST  RIGHTBR_SYM
    CLASS_HEADER ::= ATTRIBUTE_DEF  CLASS_MODIFIERS  CLASSORINTERFACE  STD_ID  EXTENDS  IMPLEMENTS
    ATTRIBUTE_DEF ::= LEFT_BRKT_SYM  ATTRIBUTE_INIT  ATTRIBUTE_LIST  RETTYPEID  RGHT_BRKT_SYM
                  ::= 
    ATTRIBUTE_INIT ::= 
                   .
    ATTRIBUTE_LIST ::= ATTRIBUTE
                   ::= ATTRIBUTE_LIST  LIST_SEP_SYM  ATTRIBUTE
    ATTRIBUTE ::= STD_ID
              ::= ATTRIBUTE_WITH_ARGS_BEGINS  ATTRIBUTE_WITH_ARGS_ENDS
    ATTRIBUTE_WITH_ARGS_BEGINS ::= STD_ID  LEFT_PAR_SYM
    ATTRIBUTE_WITH_ARGS_ENDS ::= ATTRIBUTE_ARGS  RGHT_PAR_SYM
    ATTRIBUTE_ARGS ::= ATTRIBUTE_CONSTANT
                   ::= ATTRIBUTE_ARGS  LIST_SEP_SYM  ATTRIBUTE_CONSTANT
    ATTRIBUTE_CONSTANT ::= INT_SYM
                       ::= DBL_SYM
                       ::= STR_SYM
                       ::= DATE_SYM
                       ::= DATETIME_SYM
                       ::= STD_ID  DBLCOLON_SYM  STD_ID
                       ::= TRUE_SYM
                       ::= FALSE_SYM
                       ::= INT64_SYM
                       ::= ATTRIBUTE_INTRINSIC
    ATTRIBUTE_INTRINSIC ::= INTRI_ID  LEFT_PAR_SYM  IARGS  RGHT_PAR_SYM
    CLASSORINTERFACE ::= CLASS_SYM
                     ::= INTERFACE_SYM
    CLASS_MODIFIERS ::= CLASS_MODS
                    ::= 
    CLASS_MODS ::= CLASS_MODIFIER
               ::= CLASS_MODS  RETTYPEID  CLASS_MODIFIER
    CLASS_MODIFIER ::= PUBLIC_SYM
                   ::= FINAL_SYM
                   ::= STATIC_SYM
                   ::= ABSTRACT_SYM
                   ::= PRIVATE_SYM
    EXTENDS ::= EXTENDS_SYM  STD_ID
            ::= 
    IMPLEMENTS ::= IMPLEMENTS_SYM  IMPLEMENTLIST
               ::= 
    IMPLEMENTLIST ::= STD_ID
                  ::= IMPLEMENTLIST  LIST_SEP_SYM  STD_ID
    DCL_EVENTMAP ::= 
    EVENT_DECL ::= ATTRIBUTE_DEF  EVENT_HEADER  PARM_DCL_LIST
    EVENT_HEADER ::= EVENT_MODIFIER  VOID_TYPE_SYM  STD_ID
    EVENT_MODIFIER ::= EVENT_SYM
    FUNC_HEAD ::= ATTRIBUTE_DEF  FUNCNAME  PARM_DCL_LIST
    FUNCNAME ::= FUNCTYPE  STD_ID
    FUNCTYPE ::= FUNC_MODIFIERS  DECL_TYPE
    FUNC_MODIFIERS ::= FUNC_MODS
                   ::= 
    FUNC_MODS ::= RETTYPEID  FUNC_MODIFIER
              ::= FUNC_MODS  RETTYPEID  FUNC_MODIFIER
    FUNC_MODIFIER ::= PUBLIC_SYM
                  ::= PRIVATE_SYM
                  ::= PROTECTED_SYM
                  ::= FINAL_SYM
                  ::= STATIC_SYM
                  ::= ABSTRACT_SYM
                  ::= DISPLAY_SYM
                  ::= EDIT_SYM
                  ::= SERVER_SYM
                  ::= CLIENT_SYM
    BODY ::= LEFTBR_SYM  DCL_FUNC_LIST  SEMIOPT  SECAUTHZCHECK  STMTLIST  SECAUTHZEND  RIGHTBR_SYM
    SECAUTHZCHECK ::= 
    SECAUTHZEND ::= 
    RETTYPEID ::= 
    FUNCTION_DEF ::= FUNC_HEADER  PARM_DCL_LIST  LOCAL_BODY
    FUNC_HEADER ::= DECL_TYPE  STD_ID
    PARM_DCL_LIST ::= RETTYPEID  PARM_START  PARM_LIST_OPT  RGHT_PAR_SYM  RETTYPEID
    PARM_START ::= LEFT_PAR_SYM
    PARM_LIST_OPT ::= PARM_LIST
                  ::= 
    PARM_LIST ::= DCL_INIT
              ::= PARM_LIST  LIST_SEP_SYM  DCL_INIT
    LOCAL_BODY ::= LEFTBR_SYM  DCL_LIST  SEMIOPT  STMTLIST  RETTYPEID  RIGHTBR_SYM
    DCL_LIST ::= DCL_LIST2
             ::= 
    DCL_LIST2 ::= DCL_STMT
              ::= DCL_LIST2  DCL_STMT
    DCL_FUNC_LIST ::= DCL_FUNC_LIST2
                  ::= 
    DCL_FUNC_LIST2 ::= DCL_STMT
                   ::= FUNCTION_DEF
                   ::= DCL_FUNC_LIST2  DCL_STMT
                   ::= DCL_FUNC_LIST2  FUNCTION_DEF
    DCL_STMT ::= DCL_INIT_LIST  RETTYPEID  SEMICOLON_SYM
    DCL_INIT_LIST ::= DCL_INIT
                  ::= DCL_CLIST  ASG_CLAUSE
    DCL_CLIST ::= DCL_INIT_LIST  LIST_SEP_SYM  STD_ID  ARR_DCL_IDX
    DCL_INIT ::= DECL  ASG_CLAUSE
    DECL ::= DECL_TYPE  STD_ID  ARR_DCL_IDX
    DECL_TYPE ::= STR_TYPE_SYM  STR_LEN
              ::= INT_TYPE_SYM
              ::= DBL_TYPE_SYM
              ::= DATE_TYPE_SYM
              ::= DATETIME_TYPE_SYM
              ::= TYPE_ID
              ::= QUEUE_TYPE_SYM
              ::= VOID_TYPE_SYM
              ::= ANY_TYPE_SYM
              ::= GUID_TYPE_SYM
              ::= INT64_TYPE_SYM
              ::= CLR_TYPE
    CLR_TYPE ::= CLR_NAMESPACE  TYPE_ID  CLR_ARRAY_TYPE_EXT
             ::= CLR_NAMESPACE  CLR_TYPE
    CLR_NAMESPACE ::= TYPE_ID  PERIOD_SYM
    CLR_ARRAY_TYPE_EXT ::= CLR_ARRAY_SPEC
                       ::= 
    CLR_ARRAY_SPEC ::= CLR_ARRAY_PART
                   ::= CLR_ARRAY_SPEC  CLR_ARRAY_PART
    CLR_ARRAY_PART ::= CLR_ARRAY_LEFT_PART  CLR_RECTANGULAR_LIST  RGHT_BRKT_SYM
    CLR_ARRAY_LEFT_PART ::= LEFT_BRKT_SYM
    CLR_RECTANGULAR_LIST ::= CLR_COMMA_LIST
                         ::= 
    CLR_COMMA_LIST ::= LIST_SEP_SYM
                   ::= CLR_COMMA_LIST  LIST_SEP_SYM
    STR_LEN ::= INT_SYM
            ::= 
    ARR_DCL_IDX ::= LEFT_BRKT_SYM  RANGE  ARRAY_MEM  RGHT_BRKT_SYM
                ::= 
    RANGE ::= IF_EXPR
          ::= 
    ARRAY_MEM ::= LIST_SEP_SYM  IF_EXPR
              ::= 
    ASG_CLAUSE ::= INIT_START  IF_EXPR
               ::= 
    INIT_START ::= ASG_SYM
    ASG_STMT ::= LVAL_FLD  ASSIGN  IF_EXPR
             ::= LVAL_LIST  ASG_SYM  IF_EXPR
             ::= LVAL_FLD  ASG_INC_DEC
             ::= ASG_INC_DEC  LVAL_FLD
             ::= LVAL_FLD  ASG_EVENT_HANDLER
    ASSIGN ::= ASG_SYM
           ::= ASGINC_SYM
           ::= ASGDEC_SYM
    ASG_INCDEC ::= ASGINC_SYM
               ::= ASGDEC_SYM
    ASG_EVENT_HANDLER ::= ASG_INCDEC  EVENTHANDLER_SYM  LEFT_PAR_SYM  QUALIFIER  STD_ID  RGHT_PAR_SYM
      ::= ASG_INCDEC  EVENTHANDLER_SYM  LEFT_PAR_SYM  STD_ID  DBLCOLON_SYM  STD_ID  RGHT_PAR_SYM
      ::= ASG_INCDEC  EVENTHANDLER_SYM  LEFT_PAR_SYM  QUALIFIER  EVAL_CLR_TYPE  DBLCOLON_SYM  STD_ID  RGHT_PAR_SYM
    ASG_INC_DEC ::= INC_SYM
                ::= DEC_SYM
    LVAL_FLD ::= FIELD
    LVAL_START ::= LEFT_BRKT_SYM
    LVAL_LIST ::= LVAL_START  LVALUES  RGHT_BRKT_SYM
    LVALUE ::= FIELD
    LVALUES ::= LVALUE
            ::= LVALUES  NEXTLVAL  LVALUE
    NEXTLVAL ::= LIST_SEP_SYM
    IF_EXPR ::= COND_TRUE  IF_EXPR
            ::= BOOL_EXPR
    COND_TRUE ::= COND_TEST  IF_EXPR  COLON_SYM
    COND_TEST ::= BOOL_EXPR  QUEST_SYM
    BOOL_EXPR ::= BOOL_EXPR  LOGOP  EXPR
              ::= EXPR
    LOGOP ::= AND_SYM
          ::= OR_SYM
    EXPR ::= SMPL_EXPR  RELOP  SMPL_EXPR
         ::= SMPL_EXPR  AS_SYM  STD_ID
         ::= SMPL_EXPR  IS_SYM  STD_ID
         ::= SMPL_EXPR  AS_SYM  EVAL_CLR_TYPE
         ::= SMPL_EXPR  IS_SYM  EVAL_CLR_TYPE
         ::= SMPL_EXPR
    RELOP ::= LT_SYM
          ::= LE_SYM
          ::= EQ_SYM
          ::= NE_SYM
          ::= GT_SYM
          ::= GE_SYM
          ::= LIKE_SYM
    SMPL_EXPR ::= SMPL_EXPR  ADDOP  TERM
              ::= TERM
    ADDOP ::= PLUS_SYM
          ::= MINUS_SYM
          ::= PHYSOR_SYM
    TERM ::= TERM  MULOP  CMPL_FACT
         ::= CMPL_FACT
    MULOP ::= MULT_SYM
          ::= DIV_SYM
          ::= MOD_SYM
          ::= INTDIV_SYM
          ::= SHIFTL_SYM
          ::= SHIFTR_SYM
          ::= PHYSAND_SYM
          ::= PHYSXOR_SYM
    CMPL_FACT ::= NOT_SYM  SGND_FACT
              ::= SGND_FACT
    SGND_FACT ::= SIGNOP  FACTOR
              ::= FACTOR
    SIGNOP ::= UMINUS_SYM
           ::= PHYSNOT_SYM
    FACTOR ::= LEFT_PAR_SYM  IF_EXPR  RGHT_PAR_SYM
           ::= CONSTANT
           ::= FIELD
           ::= DIRSEARCH
           ::= FUNCTION
           ::= INTRINSICS
           ::= EVAL
           ::= CONLITTERAL
           ::= NEW_CLR_ARRAY
    NEW_CLR_ARRAY ::= NEW_SYM  EVAL_CLR_TYPE  NEW_CLR_ARRAY_PART  LEFT_PAR_SYM  RGHT_PAR_SYM
    NEW_CLR_ARRAY_PART ::= CLR_SIZED_ARRAY  CLR_NOSIZED_ARRAY_SPEC
    CLR_SIZED_ARRAY ::= LEFT_BRKT_SYM  CLR_SMPL_EXPR_COMMA_LIST  RGHT_BRKT_SYM
    CLR_SMPL_EXPR_COMMA_LIST ::= SMPL_EXPR
      ::= CLR_SMPL_EXPR_COMMA_LIST  LIST_SEP_SYM  SMPL_EXPR
    CLR_NOSIZED_ARRAY_SPEC ::= CLR_NOSIZED_ARRAY_LIST
                           ::= 
    CLR_NOSIZED_ARRAY_LIST ::= CLR_NOSIZED_ARRAY
                           ::= CLR_NOSIZED_ARRAY_LIST  CLR_NOSIZED_ARRAY
    CLR_NOSIZED_ARRAY ::= LEFT_BRKT_SYM  CLR_EMPTY_COMMA_LIST  RGHT_BRKT_SYM
    CLR_EMPTY_COMMA_LIST ::= CLR_EMPTY_RECT_COMMA_LIST
                         ::= 
    CLR_EMPTY_RECT_COMMA_LIST ::= LIST_SEP_SYM
                              ::= CLR_EMPTY_RECT_COMMA_LIST  LIST_SEP_SYM
    CONLITTERAL ::= LEFT_BRKT_SYM  IF_EXPR  EXPR_LIST  RGHT_BRKT_SYM
    CONSTANT ::= INT_SYM
             ::= DBL_SYM
             ::= STR_SYM
             ::= DATE_SYM
             ::= DATETIME_SYM
             ::= STD_ID  DBLCOLON_SYM  STD_ID
             ::= TRUE_SYM
             ::= FALSE_SYM
             ::= NULL_SYM
             ::= INT64_SYM
             ::= QUALIFIER  EVAL_CLR_TYPE  DBLCOLON_SYM  STD_ID
             ::= QUALIFIER  STD_ID  DBLCOLON_SYM  STD_ID
    DIRSEARCH ::= DIRS_HEADER  PERIOD_SYM  STD_ID  ARR_IDX
              ::= DIRS_HEADER  PERIOD_SYM  FLD_NUM  ARR_IDX
    DIRS_HEADER ::= LEFT_PAR_SYM  SET_DIRS  FIND_JOIN  RGHT_PAR_SYM
    SET_DIRS ::= 
    FIELD ::= QUALIFIER  STD_ID  ARR_IDX
          ::= QUALIFIER  FLD_NUM  ARR_IDX
          ::= STD_ID  ARR_IDX
    QUALIFIER ::= EVAL  PERIOD_SYM
              ::= STD_ID  PERIOD_SYM
    FLD_NUM ::= LEFT_PAR_SYM  IF_EXPR  RGHT_PAR_SYM
    ARR_IDX ::= LEFT_BRKT_SYM  SMPL_EXPR  RGHT_BRKT_SYM
            ::= 
    EXPR_LIST ::= EXPR_LIST2
              ::= 
    EXPR_LIST2 ::= LIST_SEP_SYM  IF_EXPR
               ::= EXPR_LIST2  LIST_SEP_SYM  IF_EXPR
    FUNCTION ::= FUNC_ID  LEFT_PAR_SYM  EVAL_FUNCTION_NAME  PAR_LIST  RGHT_PAR_SYM
    EVAL_FUNCTION_NAME ::= 
    EVAL_NAME ::= EVAL_ID  LEFT_PAR_SYM
              ::= STD_ID  LEFT_PAR_SYM
              ::= STD_ID  DBLCOLON_SYM  STD_ID  LEFT_PAR_SYM
              ::= SUPER_SYM  LEFT_PAR_SYM
              ::= NEW_SYM  STD_ID  LEFT_PAR_SYM
              ::= NEW_SYM  EVAL_CLR_TYPE  LEFT_PAR_SYM
              ::= QUALIFIER  EVAL_CLR_TYPE  DBLCOLON_SYM  STD_ID  LEFT_PAR_SYM
              ::= QUALIFIER  STD_ID  LEFT_PAR_SYM
              ::= QUALIFIER  STD_ID  DBLCOLON_SYM  STD_ID  LEFT_PAR_SYM
    EVAL_CLR_TYPE ::= NAMESPACE  STD_ID
                  ::= NAMESPACE  EVAL_CLR_TYPE
    NAMESPACE ::= STD_ID  PERIOD_SYM
    EVAL ::= EVAL_NAME  PAR_LIST  RGHT_PAR_SYM
    PAR_LIST ::= PRM_LIST
             ::= 
    PRM_LIST ::= PAR_ELEM
             ::= PRM_LIST  LIST_SEP_SYM  PAR_ELEM
    PAR_ELEM ::= IF_EXPR
             ::= BYREF_SYM  FIELD
    INTRINSICS ::= INTRI_ID  LEFT_PAR_SYM  IARGS  RGHT_PAR_SYM
    IARGS ::= STD_ID
          ::= STR_SYM
          ::= STD_ID  LIST_SEP_SYM  STD_ID
          ::= 
    STMTLIST ::= STATEMENTS
             ::= 
    STATEMENTS ::= STATEMENT
               ::= STATEMENTS  STATEMENT
    STATEMENT ::= COMPOUND_STMT
              ::= WHILE_STMT
              ::= FOR_STMT
              ::= DO_STMT
              ::= SEARCH_STMT
              ::= FIND_STMT
              ::= PRINT_STMT
              ::= WINDOW_STMT
              ::= IF_STMT
              ::= SWITCH_STMT
              ::= EXPR_STMT
              ::= PAUSE_STMT
              ::= BP_CLAUSE
              ::= BREAK_STMT
              ::= CONTINUE_STMT
              ::= RETURN_CLAUSE
              ::= MOVE_REC_STMT
              ::= THROW_STMT
              ::= TRY_STMT
              ::= RETRY_STMT
              ::= TTS_STMT
              ::= FLUSH_STMT
              ::= TBLLOCK_STMT
              ::= CHANGE_STMT
              ::= UPDATE_STMT
              ::= INSERT_STMT
              ::= UNCHECKED_STMT
    COMPOUND_STMT ::= LEFTBR_SYM  STMTLIST  RIGHTBR_SYM
    THROW_STMT ::= THROW_SYM  IF_EXPR  SEMICOLON_SYM
    TRY_STMT ::= TRY_BLOCK  CATCH_LIST
    TRY_BLOCK ::= TRY_START  STATEMENT
    TRY_START ::= TRY_SYM
    CATCH_LIST ::= CATCH_STMT
               ::= CATCH_LIST  CATCH_STMT
    CATCH_STMT ::= CATCH_EXPR  PRE_CATCH  STATEMENT  POST_CATCH
    CATCH_EXPR ::= CATCH_SYM  LEFT_PAR_SYM  IF_EXPR  RGHT_PAR_SYM
      ::= CATCH_SYM  LEFT_PAR_SYM  IF_EXPR  LIST_SEP_SYM  TABLEINSTANCE  RGHT_PAR_SYM
      ::= CATCH_SYM
    PRE_CATCH ::= 
    POST_CATCH ::= 
    TABLEINSTANCE ::= INSTANCENAME
    INSTANCENAME ::= QUALIFIER  STD_ID  ARR_IDX
                 ::= STD_ID  ARR_IDX
    RETRY_STMT ::= RETRY_SYM  SEMICOLON_SYM
    WHILE_STMT ::= WHILE_TEST  STATEMENT
    WHILE_TEST ::= WHILE  LEFT_PAR_SYM  IF_EXPR  RGHT_PAR_SYM
    WHILE ::= WHILE_SYM
    DO_STMT ::= DO_BODY  DO_TEST  SEMICOLON_SYM
    DO_BODY ::= DO_HEADER  STATEMENT
    DO_HEADER ::= DO_SYM
    DO_TEST ::= WHILE_SYM  LEFT_PAR_SYM  IF_EXPR  RGHT_PAR_SYM
    FOR_STMT ::= FOR_HEADER  STATEMENT
    FOR_HEADER ::= FOR_TEST  SEMICOLON_SYM  FOR_ASG  RGHT_PAR_SYM
    FOR_TEST ::= FOR_INIT  SEMICOLON_SYM  IF_EXPR
    FOR_INIT ::= FOR_SYM  LEFT_PAR_SYM  FOR_ASG
    FOR_ASG ::= LVAL_FLD  ASSIGN  IF_EXPR
            ::= LVAL_FLD  ASG_INC_DEC
            ::= ASG_INC_DEC  LVAL_FLD
    JOIN_LIST ::= JOIN_SPECS
              ::= 
    JOIN_SPECS ::= JOIN_SPEC
               ::= JOIN_SPECS  JOIN_SPEC
    JOIN_SPEC ::= JOIN_ORDER  WHERE  IF_EXPR
              ::= JOIN_ORDER
    JOIN_ORDER ::= JOIN_USING
               ::= JOIN_USING  ORDER_GROUP
    JOIN_USING ::= JOIN_CLAUSE  USING_INDEX  STD_ID
               ::= JOIN_CLAUSE  USING_INDEX  HINT_SYM  STD_ID
               ::= JOIN_CLAUSE
    JOIN_CLAUSE ::= OUTER  JOIN_SYM  SELECTOPT  TABLE
    OUTER ::= OUTER_SYM
          ::= EXISTS_SYM
          ::= NOTEXISTS_SYM
          ::= 
    SEARCH_STMT ::= SEARCH_JOIN  STATEMENT
    SEARCH_JOIN ::= SEARCH_WHERE  JOIN_LIST
    SEARCH_WHERE ::= SEARCH_ORDER  WHERE  IF_EXPR
                 ::= SEARCH_ORDER
    WHERE ::= WHERE_SYM
    SUM_ELEM ::= SUM_FUNC  LEFT_PAR_SYM  STD_ID  RGHT_PAR_SYM
    SUM_FUNC ::= SUM_SYM
             ::= AVG_SYM
             ::= CNT_SYM
             ::= MINOF_SYM
             ::= MAXOF_SYM
    SEARCH_ORDER ::= SEARCH_USING
                 ::= SEARCH_USING  ORDER_GROUP
    ORDER_GROUP ::= ORDERBY_CLAUSE  OPT_GROUPBY
                ::= GROUPBY_CLAUSE  OPT_ORDERBY
    OPT_GROUPBY ::= GROUPBY_CLAUSE
                ::= 
    OPT_ORDERBY ::= ORDERBY_CLAUSE
                ::= 
    ORDERBY_CLAUSE ::= ORDER_SYM  OPT_BY  ORDER_ELEM
                   ::= ORDERBY_CLAUSE  LIST_SEP_SYM  ORDER_ELEM
    GROUPBY_CLAUSE ::= GROUP_SYM  OPT_BY  ORDER_ELEM
                   ::= GROUPBY_CLAUSE  LIST_SEP_SYM  ORDER_ELEM
    ORDER_ELEM ::= STD_ID  INDEX  DIRECTION
               ::= ORDER_QUALIFIER  STD_ID  INDEX  DIRECTION
    ORDER_QUALIFIER ::= STD_ID  PERIOD_SYM
    INDEX ::= LEFT_BRKT_SYM  INT_SYM  RGHT_BRKT_SYM
          ::= 
    DIRECTION ::= ASCEND_SYM
              ::= DESCEND_SYM
              ::= 
    OPT_BY ::= BY_SYM
           ::= 
    SEARCH_USING ::= SEARCH_CLAUSE  USING_INDEX  STD_ID
                 ::= SEARCH_CLAUSE  USING_INDEX  HINT_SYM  STD_ID
                 ::= SEARCH_CLAUSE
    USING_INDEX ::= INDEX_SYM
    SEARCH_CLAUSE ::= WHILE_SYM  SELECT_SYM  SELECTOPT  CROSSCOMPANY_CLAUSE  VALIDTIMESTATE_CLAUSE  TABLE
    CROSSCOMPANY_CLAUSE ::= CROSSCOMPANY_SYM
                        ::= CROSSCOMPANY_SYM  COLON_SYM  STD_ID
                        ::= 
    VALIDTIMESTATE_CLAUSE ::= VALIDTIMESTATE_SYM  LEFT_PAR_SYM  STD_ID  LIST_SEP_SYM  STD_ID  RGHT_PAR_SYM
      ::= VALIDTIMESTATE_SYM  LEFT_PAR_SYM  STD_ID  RGHT_PAR_SYM
      ::= 
    SELECTOPT ::= 
              ::= SELECTOPT  REVERSE_SYM
              ::= SELECTOPT  FIRSTFAST_SYM
              ::= SELECTOPT  FIRSTONLY_SYM
              ::= SELECTOPT  FIRSTONLY_SYM1
              ::= SELECTOPT  FIRSTONLY_SYM10
              ::= SELECTOPT  FIRSTONLY_SYM100
              ::= SELECTOPT  FIRSTONLY_SYM1000
              ::= SELECTOPT  FORUPDATE_SYM
              ::= SELECTOPT  NOFETCH_SYM
              ::= SELECTOPT  FORCE_SELECT_ORDER_SYM
              ::= SELECTOPT  FORCE_NESTED_LOOP_SYM
              ::= SELECTOPT  FORCE_LITERALS_SYM
              ::= SELECTOPT  FORCE_PLACEHOLDERS_SYM
              ::= SELECTOPT  REPEATABLEREAD_SYM
              ::= SELECTOPT  OPTIMISTICLOCK_SYM
              ::= SELECTOPT  PESSIMISTICLOCK_SYM
              ::= SELECTOPT  GENERATEONLY_SYM
    FIND_STMT ::= FIND_JOIN  SEMICOLON_SYM
    FIND_JOIN ::= FIND_WHERE  JOIN_LIST
    FIND_WHERE ::= FIND_ORDER  WHERE  IF_EXPR
               ::= FIND_ORDER
    FIND_ORDER ::= FIND_USING
               ::= FIND_USING  ORDER_GROUP
    FIND_USING ::= FIND_TABLE  USING_INDEX  STD_ID
               ::= FIND_TABLE  USING_INDEX  HINT_SYM  STD_ID
               ::= FIND_TABLE
    FIND_TABLE ::= SELECT_SYM  SELECTOPT  CROSSCOMPANY_CLAUSE  VALIDTIMESTATE_CLAUSE  TABLE
      ::= DELETE_SYM  SELECTOPT  CROSSCOMPANY_CLAUSE  VALIDTIMESTATE_CLAUSE  TABLE
    TABLE ::= FLD_LIST  OPT_FROM
    FLD_LIST ::= MULT_SYM
             ::= FIELD_LIST
    FIELD_LIST ::= FIELD_SPEC
               ::= FIELD_LIST  LIST_SEP_SYM  FIELD_SPEC
    FIELD_SPEC ::= STD_ID  INDEX
               ::= SUM_ELEM
    OPT_FROM ::= FROM_SYM  STD_ID
             ::= 
    SETFIELDSMODE ::= 
    UPDATE_STMT ::= UPDATETABLE  SET_SYM  SETFIELDSMODE  FIELDASSIGNMENTS  OPT_WHERE  JOIN_LIST  SEMICOLON_SYM
    UPDATETABLE ::= UPDATE_SYM  SELECTOPT  CROSSCOMPANY_CLAUSE  STD_ID
    OPT_WHERE ::= WHERE  IF_EXPR
              ::= 
    FIELDASSIGNMENTS ::= FIELDASSIGNMENTS  LIST_SEP_SYM  FIELDASSIGNMENT
                     ::= FIELDASSIGNMENT
    FIELDASSIGNMENT ::= STD_ID  INDEX  ASG_SYM  IF_EXPR
    INSERT_PART ::= INSERT_SYM  CROSSCOMPANY_CLAUSE  INSERT_NAME  LEFT_PAR_SYM  INSERTFIELDLIST  RGHT_PAR_SYM
    INSERT_NAME ::= STD_ID
    INSERT_STMT ::= INSERT_PART  FIND_JOIN  SEMICOLON_SYM
    INSERTFIELDLIST ::= INSERTFIELD
                    ::= INSERTFIELDLIST  LIST_SEP_SYM  INSERTFIELD
    INSERTFIELD ::= STD_ID  INDEX
    PRINT_STMT ::= PRINT_CLAUSE  AT_CLAUSE  SEMICOLON_SYM
    PRINT_CLAUSE ::= PRINT  IF_EXPR  EXPR_LIST
    PRINT ::= PRINT_SYM
    AT_CLAUSE ::= AT_SYM  IF_EXPR  LIST_SEP_SYM  IF_EXPR
              ::= 
    WINDOW_STMT ::= WINDOW_SYM  IF_EXPR  LIST_SEP_SYM  IF_EXPR  AT_CLAUSE  SEMICOLON_SYM
    IF_STMT ::= ELSE_STMT
            ::= IF_CONDS
    IF_CONDS ::= IF_COND  STATEMENT
    IF_COND ::= IF_SYM  LEFT_PAR_SYM  IF_EXPR  RGHT_PAR_SYM
    ELSE_STMT ::= ELSE  STATEMENT
    ELSE ::= IF_CONDS  ELSE_SYM
    SWITCH_STMT ::= CASE_LIST  RIGHTBR_SYM
    CASE_LIST ::= SWITCH_SYM  LEFT_PAR_SYM  IF_EXPR  RGHT_PAR_SYM  LEFTBR_SYM
              ::= CASE_TESTS  STMTLIST
    CASE_TESTS ::= CASE_HEADER  COLON_SYM
               ::= CASE_LIST  DEFAULT_SYM  COLON_SYM
    CASE_HEADER ::= CASE  IF_EXPR
                ::= CASEALT  IF_EXPR
    CASE ::= CASE_LIST  CASE_SYM
    CASEALT ::= CASE_HEADER  LIST_SEP_SYM
    EXPR_STMT ::= ASG_STMT  SEMICOLON_SYM
              ::= FUNCTION  SEMICOLON_SYM
              ::= INTRINSICS  SEMICOLON_SYM
              ::= EVAL  SEMICOLON_SYM
    PAUSE_STMT ::= PAUSE_SYM  SEMICOLON_SYM
    BP_CLAUSE ::= BP_SYM  SEMICOLON_SYM
    BREAK_STMT ::= BREAK_SYM  SEMICOLON_SYM
    CONTINUE_STMT ::= CONTINUE_SYM  SEMICOLON_SYM
    RETURN_CLAUSE ::= RETURN_SYM  SEMICOLON_SYM
                  ::= RETURN_SYM  IF_EXPR  SEMICOLON_SYM
    TTS_STMT ::= TTSABORT_SYM  SEMICOLON_SYM
             ::= TTSBEGIN_SYM  SEMICOLON_SYM
             ::= TTSEND_SYM  SEMICOLON_SYM
    FLUSH_STMT ::= FLUSH  ID_LIST  SEMICOLON_SYM
    FLUSH ::= FLUSH_SYM
    TBLLOCK_STMT ::= TABLELOCK  ID_LIST  SEMICOLON_SYM
    TABLELOCK ::= TABLELOCK_SYM
    ID_LIST ::= STD_ID
            ::= ID_LIST  LIST_SEP_SYM  STD_ID
    MOVE_REC_STMT ::= NEXT_SYM  TABLE  SEMICOLON_SYM
    CHANGE_STMT ::= CHANGE_HEADER  STATEMENT
    CHANGE_HEADER ::= CHANGE  LEFT_PAR_SYM  IF_EXPR  RGHT_PAR_SYM
    CHANGE ::= CHANGECOMP_SYM
           ::= CHANGESITE_SYM
    UNCHECKED_STMT ::= UNCHECKED_HEADER  STATEMENT
    UNCHECKED_HEADER ::= UNCHECKED_SYM  LEFT_PAR_SYM  IF_EXPR  RGHT_PAR_SYM

 

## <a name="x-language-syntax-is-stricter-in-microsoft-dynamics-ax-2012"></a><span data-ttu-id="9ebda-668">X++ 言語の構文は Microsoft Dynamics AX 2012 では厳密です</span><span class="sxs-lookup"><span data-stu-id="9ebda-668">X++ Language Syntax is Stricter in Microsoft Dynamics AX 2012</span></span>
<span data-ttu-id="9ebda-669">Microsoft Dynamics AX 2012 以降では、X++ の構文ルールが以前のバージョンの製品より厳しくなっています。</span><span class="sxs-lookup"><span data-stu-id="9ebda-669">Starting in Microsoft Dynamics AX 2012, the syntax rules for X++ are stricter than in previous versions of the product.</span></span> <span data-ttu-id="9ebda-670">このトピックでは、構文の変更について説明します。</span><span class="sxs-lookup"><span data-stu-id="9ebda-670">This topic describes the syntax changes.</span></span>

### <a name="table-of-x-syntax-changes"></a><span data-ttu-id="9ebda-671">X++ 構文変更のテーブル</span><span class="sxs-lookup"><span data-stu-id="9ebda-671">Table of X++ Syntax Changes</span></span>

<span data-ttu-id="9ebda-672">次のテーブルに、Microsoft Dynamics AX 2012 で始まる構文の変更の一覧を示します。</span><span class="sxs-lookup"><span data-stu-id="9ebda-672">The following table displays a list of syntax changes that start in Microsoft Dynamics AX 2012.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="9ebda-673">面</span><span class="sxs-lookup"><span data-stu-id="9ebda-673">Area</span></span></th>
<th><span data-ttu-id="9ebda-674">構文ルール</span><span class="sxs-lookup"><span data-stu-id="9ebda-674">Syntax rule</span></span></th>
<th><span data-ttu-id="9ebda-675">Microsoft Dynamics AX 2012 より前</span><span class="sxs-lookup"><span data-stu-id="9ebda-675">Before Microsoft Dynamics AX 2012</span></span></th>
<th><span data-ttu-id="9ebda-676">Microsoft Dynamics AX 2012 以降</span><span class="sxs-lookup"><span data-stu-id="9ebda-676">Starting with Microsoft Dynamics AX 2012</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9ebda-677">エスケープ</span><span class="sxs-lookup"><span data-stu-id="9ebda-677">Escape</span></span></td>
<td><span data-ttu-id="9ebda-678">バックスラッシュ文字 <span class="code">&lt;/span&gt; は、認識されないエスケープとしてコンパイラで拒否されます</span><span class="sxs-lookup"><span data-stu-id="9ebda-678">The backslash character <span class="code">&lt;/span&gt; is rejected by the compiler for unrecognized escapes</span></span></td>
<td><span data-ttu-id="9ebda-679">コンパイラは、&quot;31\12\2002&quot; を受け付けていましたが、実行時にリテラル文字列は異なる値として解釈されました。</span><span class="sxs-lookup"><span data-stu-id="9ebda-679">The compiler used to accept &quot;31\12\2002&quot;, but during run time the literal string was interpreted as a different value.</span></span></td>
<td><span data-ttu-id="9ebda-680">現在、次の X++ ステートメントはコンパイラによって拒否されます: <span class="code">str myDateString = &quot;31\12\2002&quot;;</span>。正しい構文は、<span class="code">&quot;31\12\2002&quot;</span>です。</span><span class="sxs-lookup"><span data-stu-id="9ebda-680">Now the following X++ statement is rejected by the compiler: <span class="code">str myDateString = &quot;31\12\2002&quot;;</span> The proper syntax is <span class="code">&quot;31\12\2002&quot;</span>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9ebda-681">例外</span><span class="sxs-lookup"><span data-stu-id="9ebda-681">Exceptions</span></span></td>
<td><span data-ttu-id="9ebda-682">再試行は、catch ブロックの外部で使用できなくなった</span><span class="sxs-lookup"><span data-stu-id="9ebda-682">Retry is no longer allowed outside of a catch block</span></span></td>
<td><span data-ttu-id="9ebda-683"><strong>catch</strong> ブロックの外に <strong>retry</strong> キーワードを書き込むことができました。</span><span class="sxs-lookup"><span data-stu-id="9ebda-683">It was possible to write the <strong>retry</strong> keyword outside of a <strong>catch</strong> block.</span></span> <span data-ttu-id="9ebda-684">これにより、実行時に<strong>再試行</strong>に達したときにプログラムが終了しました。</span><span class="sxs-lookup"><span data-stu-id="9ebda-684">This caused the program to end when the <strong>retry</strong> was reached during runtime.</span></span></td>
<td><span data-ttu-id="9ebda-685">現在は、<strong>再試行</strong>が <strong>catch</strong> ブロック内部でのみ発生するようになりました。</span><span class="sxs-lookup"><span data-stu-id="9ebda-685">Now <strong>retry</strong> can occur only inside a <strong>catch</strong> block.</span></span> <span data-ttu-id="9ebda-686">詳細については、「トライおよびキャッチ キーワードで例外処理」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="9ebda-686">For more information, see Exception Handling with try and catch Keywords.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9ebda-687">例外</span><span class="sxs-lookup"><span data-stu-id="9ebda-687">Exceptions</span></span></td>
<td><span data-ttu-id="9ebda-688"><code>int</code> 値だけをスローおよび取得できるようになります</span><span class="sxs-lookup"><span data-stu-id="9ebda-688">Now you can throw and catch only <code>int</code> values</span></span></td>
<td><span data-ttu-id="9ebda-689"><code>throw &quot;hello world&quot;;</code> などの文字列および日付のようなスカラー式をスローでき、コンパイル エラーが発生しませんでした。</span><span class="sxs-lookup"><span data-stu-id="9ebda-689">It was possible to throw scalar expressions like strings and dates, such as <code>throw &quot;hello world&quot;;</code>, and get no compile error.</span></span> <span data-ttu-id="9ebda-690">実行時には、<span class="code">catch {print(&quot;Catch worked.&quot;);}</span> などの特定の値で装飾されていない<code>catch</code>ブロックによって捉えることが可能です。</span><span class="sxs-lookup"><span data-stu-id="9ebda-690">At runtime this was catch-able by a <code>catch</code> block that was not decorated with any specific value, such as <span class="code">catch {print(&quot;Catch worked.&quot;);}</span>.</span></span></td>
<td><span data-ttu-id="9ebda-691">現在、<strong>throw</strong> キーワードで配置できる唯一の式は、<code>int</code> です。</span><span class="sxs-lookup"><span data-stu-id="9ebda-691">Now the only expression you can put on the <strong>throw</strong> keyword is an <code>int</code>.</span></span> <span data-ttu-id="9ebda-692">多くの場合、スローするための最もよい方法は、<span class="code">Global::error(&quot;説明&quot;);</span>。</span><span class="sxs-lookup"><span data-stu-id="9ebda-692">Often the best thing to throw is <span class="code">Global::error(&quot;Explanation&quot;);</span>.</span></span> <span data-ttu-id="9ebda-693">多くの場合、見つけるための最もよい方法は、<code>Exception</code> 列挙の要素です。</span><span class="sxs-lookup"><span data-stu-id="9ebda-693">Often the best thing to catch is an element of the <code>Exception</code> enum.</span></span> <span data-ttu-id="9ebda-694">詳細については、「トライおよびキャッチ キーワードで例外処理」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="9ebda-694">For more information, see Exception Handling with try and catch Keywords.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9ebda-695">継承</span><span class="sxs-lookup"><span data-stu-id="9ebda-695">Inheritance</span></span></td>
<td><span data-ttu-id="9ebda-696">ダウン キャストは明示的にできるようになりました。</span><span class="sxs-lookup"><span data-stu-id="9ebda-696">Downcasting can now be explicit.</span></span>
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="9ebda-697"><strong>メモ</strong></span><span class="sxs-lookup"><span data-stu-id="9ebda-697"><strong>Note</strong></span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9ebda-698">暗黙的なダウンキャストを回避することがプログラミングのベスト プラクティスです。</span><span class="sxs-lookup"><span data-stu-id="9ebda-698">It is good programming practice to avoid implicit downcasts.</span></span></td>
</tr>
</tbody>
</table></td>
<td><span data-ttu-id="9ebda-699">単純な代入演算子である等号記号 (<code>=</code>) で派生オブジェクトに基本オブジェクトを代入することができました。</span><span class="sxs-lookup"><span data-stu-id="9ebda-699">It was possible to assign a base object to a derived object with the simple assignment operator, which is the equals sign (<code>=</code>).</span></span> <span data-ttu-id="9ebda-700">コンパイラはこれらの割り当てを受け入れましたが、実行時に不適切なダウンキャスト割り当てを誤って使用するとエラーが発生しました。</span><span class="sxs-lookup"><span data-stu-id="9ebda-700">The compiler accepted these assignments, but during run time any misuse of an improper downcast assignment caused an error.</span></span></td>
<td><span data-ttu-id="9ebda-701">現在は、ダウンキャストは明示的にできるようになりました。</span><span class="sxs-lookup"><span data-stu-id="9ebda-701">Now all downcasts can be explicit.</span></span> <span data-ttu-id="9ebda-702">これは、演算子と<strong>して</strong>新しく実行されます。</span><span class="sxs-lookup"><span data-stu-id="9ebda-702">This is accomplished with the new <strong>as</strong> expression operator.</span></span> <span data-ttu-id="9ebda-703"><strong>as</strong> キーワードによる明示的なダウンキャストは、<code>ThingClass</code> が <code>Object</code> で拡張する次のコード例で示されています。<code>ThingClass myThing = new ThingClass();</code><code>Object myObject = myThing;</code><code>myThing = myObject as ThingClass; // Explicit downcast, good.</code> 詳細については、式の演算子: 継承の Is および As を参照してください。</span><span class="sxs-lookup"><span data-stu-id="9ebda-703">Explicit downcasting with the <strong>as</strong> keyword is illustrated by the following code example, in which <code>ThingClass</code> extends <code>Object</code>: <code>ThingClass myThing = new ThingClass();</code>  <code>Object myObject = myThing;</code>  <code>myThing = myObject as ThingClass; // Explicit downcast, good.</code> For more information, see Expression Operators: Is and As for Inheritance.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9ebda-704">継承</span><span class="sxs-lookup"><span data-stu-id="9ebda-704">Inheritance</span></span></td>
<td><span data-ttu-id="9ebda-705">基本メソッドの上書きへのアクセスを、基本メソッドより減らすことはできません。</span><span class="sxs-lookup"><span data-stu-id="9ebda-705">Override of a base method cannot be less accessible than the base method</span></span></td>
<td><span data-ttu-id="9ebda-706">基本メソッドを <strong>protected</strong> で修飾して、メソッドのオーバーライドを <strong>private</strong> とすることができました。</span><span class="sxs-lookup"><span data-stu-id="9ebda-706">It was possible to have a base method be decorated with <strong>protected</strong> and yet have an override of that method be <strong>private</strong>.</span></span></td>
<td><span data-ttu-id="9ebda-707">現在は、基本メソッドが<strong>保護されている</strong>場合、オーバーライド メソッドは<strong>保護</strong>または<strong>パブリック</strong>のいずれかでなければならず、<strong>プライベート</strong>にできません。</span><span class="sxs-lookup"><span data-stu-id="9ebda-707">Now when a base method is <strong>protected</strong>, the override method must be either <strong>protected</strong> or <strong>public</strong>, and the override method cannot be <strong>private</strong>.</span></span> <span data-ttu-id="9ebda-708">この方法の詳細については、「メソッド アクセス コントロール」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="9ebda-708">For more information, see Method Access Control.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9ebda-709">継承</span><span class="sxs-lookup"><span data-stu-id="9ebda-709">Inheritance</span></span></td>
<td><span data-ttu-id="9ebda-710">基本メソッドのオーバーライドは、基本メソッドとまったく同じ戻り値の型とパラメータ署名にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="9ebda-710">Override of a base method must have the exact same return type and parameter signature as the base method</span></span></td>
<td><span data-ttu-id="9ebda-711">基本クラスに、すべてのテーブルの基準となっている <code>Common</code> テーブルのパラメーターを入力するメソッドがあったと仮定します。</span><span class="sxs-lookup"><span data-stu-id="9ebda-711">Suppose a base class had a method that inputs a parameter of the <code>Common</code> table, which is the base of all tables.</span></span> <span data-ttu-id="9ebda-712">派生クラスでは、代わりに <code>MyTable</code> を入力するメソッドをオーバーライド可能でした。</span><span class="sxs-lookup"><span data-stu-id="9ebda-712">In a derived class it was possible to override the method to instead input <code>MyTable</code>.</span></span></td>
<td><span data-ttu-id="9ebda-713">現在、基本メソッドとそのオーバーライド メソッドのパラメーター署名は、正確に一致する必要があります。</span><span class="sxs-lookup"><span data-stu-id="9ebda-713">Now the parameter signatures of the base method and its override method must match exactly.</span></span> <span data-ttu-id="9ebda-714">また、戻り値の型が正確に一致する必要があります。</span><span class="sxs-lookup"><span data-stu-id="9ebda-714">Also, the return types must match exactly.</span></span> <span data-ttu-id="9ebda-715">詳細については、「メソッドの上書き」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="9ebda-715">For more information, see Overriding a Method.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9ebda-716">インターフェイス</span><span class="sxs-lookup"><span data-stu-id="9ebda-716">Interfaces</span></span></td>
<td><span data-ttu-id="9ebda-717">インターフェイス メソッドの実装はパラメーター署名と完全に一致する必要があります。</span><span class="sxs-lookup"><span data-stu-id="9ebda-717">Implementation of an interface method must match the parameter signature exactly</span></span></td>
<td><span data-ttu-id="9ebda-718">インターフェイスに、<code>int</code> のパラメーターを入力するメソッドがあると仮定します。</span><span class="sxs-lookup"><span data-stu-id="9ebda-718">Suppose an interface had a method that input a parameter of an <code>int</code>.</span></span> <span data-ttu-id="9ebda-719">インターフェイスを実装するクラスでは、メソッドを <code>str</code> のパラメーターで記述可能でした。</span><span class="sxs-lookup"><span data-stu-id="9ebda-719">In a class that implements the interface, it was possible to write the method with a parameter of a <code>str</code>.</span></span></td>
<td><span data-ttu-id="9ebda-720">現在、メソッドのパラメーター署名は、インターフェイスとクラスのメソッドの実装の間で正確に一致する必要があります。</span><span class="sxs-lookup"><span data-stu-id="9ebda-720">Now the parameter signatures of the method must exactly match between the interface and the implementation of the method on a class.</span></span> <span data-ttu-id="9ebda-721">また、戻り値の型が正確に一致する必要があります。</span><span class="sxs-lookup"><span data-stu-id="9ebda-721">Also, the return types must match exactly.</span></span> <span data-ttu-id="9ebda-722">詳細については、「インターフェイスの概要」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="9ebda-722">For more information, see Interfaces Overview.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9ebda-723">インターフェイス</span><span class="sxs-lookup"><span data-stu-id="9ebda-723">Interfaces</span></span></td>
<td><span data-ttu-id="9ebda-724">インターフェイスを実装する非抽象基本クラスは、実装の派生クラスに依存できません。</span><span class="sxs-lookup"><span data-stu-id="9ebda-724">A non-abstract base class that implements an interface cannot rely on a derived class for that implementation</span></span></td>
<td><span data-ttu-id="9ebda-725">基本クラスでインターフェイスを実装するとき、インターフェイスのメソッドが派生クラスによって実装された場合、基本クラスでそのメソッドを実装しないことが可能でした。</span><span class="sxs-lookup"><span data-stu-id="9ebda-725">When a base class implements an interface, it was possible for the class to not implement the methods of the interface if a derived class implemented the methods.</span></span> <span data-ttu-id="9ebda-726">唯一の制限は、クラスで、<code>new</code> コンストラクター メソッドを呼び出せないことでした。</span><span class="sxs-lookup"><span data-stu-id="9ebda-726">The only limitation was that the <code>new</code> constructor method could not be called on the class.</span></span></td>
<td><span data-ttu-id="9ebda-727">現在は、コンパイラによって、インターフェイスを実装するすべてのクラスは、インターフェイスのすべてのメソッドの完全な実装を持つまたは継承することが必須とされています。</span><span class="sxs-lookup"><span data-stu-id="9ebda-727">Now the compiler requires that every class that implements an interface must have or inherit a complete implementation of every method of the interface.</span></span> <span data-ttu-id="9ebda-728">詳細については、X++、C# の比較: オブジェクト指向プログラミングを参照してください。</span><span class="sxs-lookup"><span data-stu-id="9ebda-728">For more information, see X++, C# Comparison: Object Oriented Programming.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9ebda-729">モディファイア</span><span class="sxs-lookup"><span data-stu-id="9ebda-729">Modifiers</span></span></td>
<td><span data-ttu-id="9ebda-730"><strong>静的</strong>修飾子をインターフェイスに適用しないでください</span><span class="sxs-lookup"><span data-stu-id="9ebda-730">The <strong>static</strong> modifier should not be applied to an interface</span></span></td>
<td><span data-ttu-id="9ebda-731"><span class="code">静的インターフェイス IMyInterface {}</span> を書き込むことができましたが、このコンテキストでは意味がないため、<strong>static</strong> モディファイアーに影響はありませんでした。</span><span class="sxs-lookup"><span data-stu-id="9ebda-731">It was possible to write <span class="code">static interface IMyInterface {}</span>, but the <strong>static</strong> modifier had no effect because it makes no sense in this context.</span></span></td>
<td><span data-ttu-id="9ebda-732">Dynamics AX 2009 以降、X++ コンパイラがインターフェイス宣言上で<strong>静的</strong>モディファイアーの許可をやめることがあります。</span><span class="sxs-lookup"><span data-stu-id="9ebda-732">Sometime after Dynamics AX 2009 the X++ compiler might stop allowing the <strong>static</strong> modifier on interface declarations.</span></span> <span data-ttu-id="9ebda-733">詳細については、「インターフェイスの概要」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="9ebda-733">For more information, see Interfaces Overview.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9ebda-734">モディファイア</span><span class="sxs-lookup"><span data-stu-id="9ebda-734">Modifiers</span></span></td>
<td><span data-ttu-id="9ebda-735"><strong>静的</strong>修飾子を <code>new</code> コンストラクターに適用する必要があります</span><span class="sxs-lookup"><span data-stu-id="9ebda-735">The <strong>static</strong> modifier must not be applied to the <code>new</code> constructor</span></span></td>
<td><span data-ttu-id="9ebda-736"><strong>静的</strong>モディファイアーを <code>new</code> コンストラクター メソッドの宣言に適用することができました。</span><span class="sxs-lookup"><span data-stu-id="9ebda-736">It was possible to apply the <strong>static</strong> modifier to the declaration of the <code>new</code> constructor method.</span></span> <span data-ttu-id="9ebda-737">これにより、<code>new MyClass();</code> が NULL 操作として動作するようになりました。</span><span class="sxs-lookup"><span data-stu-id="9ebda-737">This caused <code>new MyClass();</code> to behave as a null operation.</span></span> <span data-ttu-id="9ebda-738">代わりに、ステートメント <span class="code">MyClass::new();</span> が静的な <code>new</code> メソッドを呼び出しますが、オブジェクトを構築しません。</span><span class="sxs-lookup"><span data-stu-id="9ebda-738">Instead, the statement <span class="code">MyClass::new();</span> would call the static <code>new</code> method, but that would not construct an object.</span></span></td>
<td><span data-ttu-id="9ebda-739">現在は、<strong>静的</strong>モディファイアーが <code>new</code> メソッドに適用されるときにコンパイラはエラーを発行します。</span><span class="sxs-lookup"><span data-stu-id="9ebda-739">Now the compiler issues an error when the <strong>static</strong> modifier is applied to the <code>new</code> method.</span></span> <span data-ttu-id="9ebda-740">詳細については、「コンストラクター」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="9ebda-740">For more information, see Constructors.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9ebda-741">モディファイア</span><span class="sxs-lookup"><span data-stu-id="9ebda-741">Modifiers</span></span></td>
<td><span data-ttu-id="9ebda-742">各メソッドで明示的なアクセス修飾子を使用</span><span class="sxs-lookup"><span data-stu-id="9ebda-742">Use an explicit access modifier on each method</span></span></td>
<td><span data-ttu-id="9ebda-743">過去には、<span class="ui">AOT</span> &gt; <span class="ui">クラス</span> &gt; <em>MyClass</em> &gt; <span class="ui">新しいメソッド</span>のメニュー項目で、アクセス修飾子のないメソッドを作成していました。</span><span class="sxs-lookup"><span data-stu-id="9ebda-743">In the past the menu item of <span class="ui">AOT</span> &gt; <span class="ui">Classes</span> &gt; <em>MyClass</em> &gt; <span class="ui">New Method</span> created the method without any access modifier.</span></span> <span data-ttu-id="9ebda-744">これは、メソッドが暗黙的に<strong>パブリック </strong>であることを意味しましたが、一部の X++ 開発者は既定を完全に認識していない可能性があります。</span><span class="sxs-lookup"><span data-stu-id="9ebda-744">This meant that the method was implicitly <strong>public</strong>, although some X++ developers might not have been fully aware of the default.</span></span> <span data-ttu-id="9ebda-745">開発者がメソッドが呼び出される可能性のあるあらゆる場所を調べる必要があり、メソッドのコードを修正しなければならなかったときに、これにより余分な作業が後で発生しました。</span><span class="sxs-lookup"><span data-stu-id="9ebda-745">This created extra work later when a developer needed to modify the code in the method, because the developer had to research everywhere that the method might be called from.</span></span></td>
<td><span data-ttu-id="9ebda-746">現在は、<span class="ui">新しいメソッド</span>のメニュー項目において新しいメソッドの自動宣言に <strong>private</strong> キーワードが明示的に含まれています。</span><span class="sxs-lookup"><span data-stu-id="9ebda-746">Now the <span class="ui">New Method</span> menu item explicitly includes the <strong>private</strong> keyword in its automatic declaration of the new method.</span></span> <span data-ttu-id="9ebda-747">開発者は、必要に応じて別のモディファイアーを入力することができます。</span><span class="sxs-lookup"><span data-stu-id="9ebda-747">The developer can type in a different modifier if appropriate.</span></span> <span data-ttu-id="9ebda-748">詳細については、「メソッド モディファイア」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="9ebda-748">For more information, see Method Modifiers.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9ebda-749">パラメーター</span><span class="sxs-lookup"><span data-stu-id="9ebda-749">Parameters</span></span></td>
<td><span data-ttu-id="9ebda-750"><code>new</code> コンストラクターの呼び出しで指定されるパラメーターは、<code>new</code> コンストラクター メソッドのパラメーターと一致する必要があります</span><span class="sxs-lookup"><span data-stu-id="9ebda-750">Parameters given in a call to a <code>new</code> constructor method must match the parameters on the <code>new</code> constructor method</span></span></td>
<td><span data-ttu-id="9ebda-751"><code>new</code> メソッドがパラメーターを入力しないために宣言された場合でも、<code>new</code> コンストラクター メソッドの呼び出しで複数のパラメーターを渡すことができました。</span><span class="sxs-lookup"><span data-stu-id="9ebda-751">It was possible to pass in multiple parameters on call to a <code>new</code> constructor method even when the <code>new</code> method was declared to input no parameters.</span></span></td>
<td><span data-ttu-id="9ebda-752">現在は、<code>new</code> メソッドへの呼び出しは、宣言された <code>new</code> メソッドのパラメーター署名と正確に一致する必要があります。</span><span class="sxs-lookup"><span data-stu-id="9ebda-752">Now the call to the <code>new</code> method must exactly match the declared parameter signature of the <code>new</code> method.</span></span> <span data-ttu-id="9ebda-753">詳細については、「サブクラスの作成」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="9ebda-753">For more information, see Creating a Subclass.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9ebda-754">パラメーター</span><span class="sxs-lookup"><span data-stu-id="9ebda-754">Parameters</span></span></td>
<td><span data-ttu-id="9ebda-755">既定値を持つパラメーターは、既定値がないすべてのパラメーターの後でなければなりません</span><span class="sxs-lookup"><span data-stu-id="9ebda-755">Parameters with default values must come after all parameters that do not have default values</span></span></td>
<td><span data-ttu-id="9ebda-756">2 つのパラメーターで取得するメソッドを宣言して、最初のパラメーターのみに既定値を提供させるようにできました。</span><span class="sxs-lookup"><span data-stu-id="9ebda-756">It was possible to declare a method that takes in two parameters, and have only the first parameter offer a default value.</span></span> <span data-ttu-id="9ebda-757">この目的はありませんでした。</span><span class="sxs-lookup"><span data-stu-id="9ebda-757">There was no purpose to this.</span></span> <span data-ttu-id="9ebda-758">呼び出しが 2 番目のパラメーターの値を指定する必要があり、1 番目のパラメーターを省略できないため、最初のパラメーターの既定値を受け入れる方法はありませんでした。</span><span class="sxs-lookup"><span data-stu-id="9ebda-758">There was no way to accept the default of the first parameter because the call must specify a value for the second parameter and cannot omit the first parameter.</span></span></td>
<td><span data-ttu-id="9ebda-759">現在は、メソッドの宣言において、既定値を提供するパラメーターは提供しないすべてのパラメーターの後に配置する必要があります。</span><span class="sxs-lookup"><span data-stu-id="9ebda-759">Now in the declaration of a method, any parameter that offers a default value must come after all the parameters that do not.</span></span> <span data-ttu-id="9ebda-760">詳細については、次のトピックを参照してください。</span><span class="sxs-lookup"><span data-stu-id="9ebda-760">For more information, see the following topics:</span></span>
<ul>
<li><span data-ttu-id="9ebda-761">オプションのパラメーターの使用</span><span class="sxs-lookup"><span data-stu-id="9ebda-761">Using Optional Parameters</span></span></li>
<li><span data-ttu-id="9ebda-762">パラメーターのベスト プラクティス</span><span class="sxs-lookup"><span data-stu-id="9ebda-762">Best Practices for Parameters</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9ebda-763">パラメーター</span><span class="sxs-lookup"><span data-stu-id="9ebda-763">Parameters</span></span></td>
<td><span data-ttu-id="9ebda-764">メソッドのオーバーライドには、オーバーライドされたメソッドとして同じ既定のパラメータが必要です。</span><span class="sxs-lookup"><span data-stu-id="9ebda-764">Override of a method must have the same default parameters as the overridden method</span></span></td>
<td><span data-ttu-id="9ebda-765">メソッドを <span class="code">public void myMethod(int i=22){}</span> として、オーバーライドを <span class="code">public void myMethod(){}</span> として宣言することができました。</span><span class="sxs-lookup"><span data-stu-id="9ebda-765">It was possible to declare a method as <span class="code">public void myMethod(int i=22){}</span> and the override as <span class="code">public void myMethod(){}</span>.</span></span> <span data-ttu-id="9ebda-766">ただし、オーバーライド メソッドが <code>derivedObject(333);</code> として呼び出された場合はエラーが発生しました。</span><span class="sxs-lookup"><span data-stu-id="9ebda-766">But if the override method was called as <code>derivedObject(333);</code> an error occurred.</span></span></td>
<td><span data-ttu-id="9ebda-767">現在、オーバーライド メソッドは、オーバーライドされたメソッドで宣言されている順序と同じ順序で同じパラメーターの型を一覧表示する必要があります。</span><span class="sxs-lookup"><span data-stu-id="9ebda-767">Now the override method must list the same parameter types in the same sequence that they are declared in the overridden method.</span></span> <span data-ttu-id="9ebda-768">詳細については、「メソッドの上書き」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="9ebda-768">For more information, see Overriding a Method.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9ebda-769">プリプロセッサ</span><span class="sxs-lookup"><span data-stu-id="9ebda-769">Preprocessor</span></span></td>
<td><span data-ttu-id="9ebda-770">コメント内の <strong>TODO</strong> は、コメントの最初の行で、最初の空白ではない文字にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="9ebda-770">A <strong>TODO</strong> in a comment must be the first non-whitespace in the first line of the comment</span></span></td>
<td><span data-ttu-id="9ebda-771">複数行 <span class="code">/* ... */</span> タスク コメントで、最初のコメント行の後の他のテキストの後に <strong>TODO</strong> キーワードが出現した場合でも、<strong>TODO</strong> を検出するために使用する X++ プリプロセッサ。</span><span class="sxs-lookup"><span data-stu-id="9ebda-771">The X++ preprocessor used to detect the <strong>TODO</strong> keyword in a multi-line <span class="code">/* ... */</span> task comment even when the <strong>TODO</strong> appeared after other text after the first comment line.</span></span></td>
<td><span data-ttu-id="9ebda-772">現在は、<strong>TODO</strong> がコメントの最初の行に表示される場合、およびコメントの最初の空白ではない文字として表示される場合のみ、X++ プリプロセッサが <strong>TODO</strong> キーワードを検出します。</span><span class="sxs-lookup"><span data-stu-id="9ebda-772">Now the X++ preprocessor detects the <strong>TODO</strong> keyword only if <strong>TODO</strong> appears on the first line of the comment, and as the first non-whitespace in the comment.</span></span> <span data-ttu-id="9ebda-773">詳細については、「X++ 開発者タスクに対する TODO コメント」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="9ebda-773">For more information, see TODO Comments for X++ Developer Tasks.</span></span></td>
</tr>
</tbody>
</table>



<a name="additional-resources"></a><span data-ttu-id="9ebda-774">その他のリソース</span><span class="sxs-lookup"><span data-stu-id="9ebda-774">Additional resources</span></span>
--------

[<span data-ttu-id="9ebda-775">X++ 言語リファレンス</span><span class="sxs-lookup"><span data-stu-id="9ebda-775">X++ Language Reference</span></span>](xpp-language-reference.md)




