---
title: S クラス
description: 文字 S で始まるシステム API クラス。
author: RobinARH
manager: AnnBe
ms.date: 11/07/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.search.scope: Operations
ms.custom: 51751
ms.assetid: cb7c0fd3-34ec-407b-ad78-1007a67d70d5
ms.search.region: Global
ms.author: rhaertle
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 18f889ce6d00379d6c1851eb4c32cdc899815550
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/27/2019
ms.locfileid: "2191609"
---
# <a name="s-classes"></a><span data-ttu-id="50445-103">S クラス</span><span class="sxs-lookup"><span data-stu-id="50445-103">S classes</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="50445-104">文字 S で始まるシステム API クラス。</span><span class="sxs-lookup"><span data-stu-id="50445-104">System API classes that start with the letter S.</span></span>

<a name="class-scannerclass"></a><span data-ttu-id="50445-105">クラス ScannerClass</span><span class="sxs-lookup"><span data-stu-id="50445-105">Class ScannerClass</span></span>
------------------

    class ScannerClass extends Object

### <a name="remarks"></a><span data-ttu-id="50445-106">備考</span><span class="sxs-lookup"><span data-stu-id="50445-106">Remarks</span></span>

### <a name="examples"></a><span data-ttu-id="50445-107">例</span><span class="sxs-lookup"><span data-stu-id="50445-107">Examples</span></span>

### <a name="methods"></a><span data-ttu-id="50445-108">メソッド</span><span class="sxs-lookup"><span data-stu-id="50445-108">Methods</span></span>

| <span data-ttu-id="50445-109">方法</span><span class="sxs-lookup"><span data-stu-id="50445-109">Method</span></span>                                                                                       | <span data-ttu-id="50445-110">説明</span><span class="sxs-lookup"><span data-stu-id="50445-110">Description</span></span>                                     |
|----------------------------------------------------------------------------------------------|-------------------------------------------------|
| <span data-ttu-id="50445-111">public int col()</span><span class="sxs-lookup"><span data-stu-id="50445-111">public int col()</span></span>                                                                             |                                                 |
| <span data-ttu-id="50445-112">public Date dateValue()</span><span class="sxs-lookup"><span data-stu-id="50445-112">public Date dateValue()</span></span>                                                                      |                                                 |
| <span data-ttu-id="50445-113">public int firstSymbol()</span><span class="sxs-lookup"><span data-stu-id="50445-113">public int firstSymbol()</span></span>                                                                     |                                                 |
| <span data-ttu-id="50445-114">public Int64 int64Value()</span><span class="sxs-lookup"><span data-stu-id="50445-114">public Int64 int64Value()</span></span>                                                                    |                                                 |
| <span data-ttu-id="50445-115">public int intValue()</span><span class="sxs-lookup"><span data-stu-id="50445-115">public int intValue()</span></span>                                                                        |                                                 |
| <span data-ttu-id="50445-116">public int line()</span><span class="sxs-lookup"><span data-stu-id="50445-116">public int line()</span></span>                                                                            |                                                 |
| <span data-ttu-id="50445-117">public int nextSymbol()</span><span class="sxs-lookup"><span data-stu-id="50445-117">public int nextSymbol()</span></span>                                                                      |                                                 |
| <span data-ttu-id="50445-118">public Real realValue()</span><span class="sxs-lookup"><span data-stu-id="50445-118">public Real realValue()</span></span>                                                                      |                                                 |
| <span data-ttu-id="50445-119">public int startColumn()</span><span class="sxs-lookup"><span data-stu-id="50445-119">public int startColumn()</span></span>                                                                     |                                                 |
| <span data-ttu-id="50445-120">public str string()</span><span class="sxs-lookup"><span data-stu-id="50445-120">public str string()</span></span>                                                                          |                                                 |
| <span data-ttu-id="50445-121">public str strValue()</span><span class="sxs-lookup"><span data-stu-id="50445-121">public str strValue()</span></span>                                                                        |                                                 |
| <span data-ttu-id="50445-122">public void localMacroDefine(str text, int startLine, int startPos, int endLine, int endPos)</span><span class="sxs-lookup"><span data-stu-id="50445-122">public void localMacroDefine(str text, int startLine, int startPos, int endLine, int endPos)</span></span> |                                                 |
| <span data-ttu-id="50445-123">public void lineComment(str text, int startLine, int startPos, int endLine, int endPos)</span><span class="sxs-lookup"><span data-stu-id="50445-123">public void lineComment(str text, int startLine, int startPos, int endLine, int endPos)</span></span>      |                                                 |
| <span data-ttu-id="50445-124">public void macroDefine(str text, int startLine, int startPos, int endLine, int endPos)</span><span class="sxs-lookup"><span data-stu-id="50445-124">public void macroDefine(str text, int startLine, int startPos, int endLine, int endPos)</span></span>      |                                                 |
| <span data-ttu-id="50445-125">public void new(str source)</span><span class="sxs-lookup"><span data-stu-id="50445-125">public void new(str source)</span></span>                                                                  | <span data-ttu-id="50445-126">Object クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="50445-126">Initializes a new instance of the Object class.</span></span> |
| <span data-ttu-id="50445-127">public void comment(str text, int startLine, int startPos, int endLine, int endPos)</span><span class="sxs-lookup"><span data-stu-id="50445-127">public void comment(str text, int startLine, int startPos, int endLine, int endPos)</span></span>          |                                                 |

### <a name="method-col"></a><span data-ttu-id="50445-128">メソッド col</span><span class="sxs-lookup"><span data-stu-id="50445-128">Method col</span></span>

    public int col()

#### <a name="return-value"></a><span data-ttu-id="50445-129">戻り値</span><span class="sxs-lookup"><span data-stu-id="50445-129">Return Value</span></span>

### <a name="method-datevalue"></a><span data-ttu-id="50445-130">メソッド dateValue</span><span class="sxs-lookup"><span data-stu-id="50445-130">Method dateValue</span></span>

    public Date dateValue()

#### <a name="return-value"></a><span data-ttu-id="50445-131">戻り値</span><span class="sxs-lookup"><span data-stu-id="50445-131">Return Value</span></span>

### <a name="method-firstsymbol"></a><span data-ttu-id="50445-132">メソッド firstSymbol</span><span class="sxs-lookup"><span data-stu-id="50445-132">Method firstSymbol</span></span>

    public int firstSymbol()

#### <a name="return-value"></a><span data-ttu-id="50445-133">戻り値</span><span class="sxs-lookup"><span data-stu-id="50445-133">Return Value</span></span>

### <a name="method-int64value"></a><span data-ttu-id="50445-134">メソッド int64Value</span><span class="sxs-lookup"><span data-stu-id="50445-134">Method int64Value</span></span>

    public Int64 int64Value()

#### <a name="return-value"></a><span data-ttu-id="50445-135">戻り値</span><span class="sxs-lookup"><span data-stu-id="50445-135">Return Value</span></span>

### <a name="method-intvalue"></a><span data-ttu-id="50445-136">メソッド intValue</span><span class="sxs-lookup"><span data-stu-id="50445-136">Method intValue</span></span>

    public int intValue()

#### <a name="return-value"></a><span data-ttu-id="50445-137">戻り値</span><span class="sxs-lookup"><span data-stu-id="50445-137">Return Value</span></span>

### <a name="method-line"></a><span data-ttu-id="50445-138">メソッド line</span><span class="sxs-lookup"><span data-stu-id="50445-138">Method line</span></span>

    public int line()

#### <a name="return-value"></a><span data-ttu-id="50445-139">戻り値</span><span class="sxs-lookup"><span data-stu-id="50445-139">Return Value</span></span>

### <a name="method-nextsymbol"></a><span data-ttu-id="50445-140">メソッド nextSymbol</span><span class="sxs-lookup"><span data-stu-id="50445-140">Method nextSymbol</span></span>

    public int nextSymbol()

#### <a name="return-value"></a><span data-ttu-id="50445-141">戻り値</span><span class="sxs-lookup"><span data-stu-id="50445-141">Return Value</span></span>

### <a name="method-realvalue"></a><span data-ttu-id="50445-142">メソッド realValue</span><span class="sxs-lookup"><span data-stu-id="50445-142">Method realValue</span></span>

    public Real realValue()

#### <a name="return-value"></a><span data-ttu-id="50445-143">戻り値</span><span class="sxs-lookup"><span data-stu-id="50445-143">Return Value</span></span>

### <a name="method-startcolumn"></a><span data-ttu-id="50445-144">メソッド startColumn</span><span class="sxs-lookup"><span data-stu-id="50445-144">Method startColumn</span></span>

    public int startColumn()

#### <a name="return-value"></a><span data-ttu-id="50445-145">戻り値</span><span class="sxs-lookup"><span data-stu-id="50445-145">Return Value</span></span>

### <a name="method-string"></a><span data-ttu-id="50445-146">メソッド string</span><span class="sxs-lookup"><span data-stu-id="50445-146">Method string</span></span>

    public str string()

#### <a name="return-value"></a><span data-ttu-id="50445-147">戻り値</span><span class="sxs-lookup"><span data-stu-id="50445-147">Return Value</span></span>

### <a name="method-strvalue"></a><span data-ttu-id="50445-148">メソッド strValue</span><span class="sxs-lookup"><span data-stu-id="50445-148">Method strValue</span></span>

    public str strValue()

#### <a name="return-value"></a><span data-ttu-id="50445-149">戻り値</span><span class="sxs-lookup"><span data-stu-id="50445-149">Return Value</span></span>

### <a name="method-localmacrodefine"></a><span data-ttu-id="50445-150">メソッド localMacroDefine</span><span class="sxs-lookup"><span data-stu-id="50445-150">Method localMacroDefine</span></span>

    public void localMacroDefine(str text, int startLine, int startPos, int endLine, int endPos)

#### <a name="parameters"></a><span data-ttu-id="50445-151">パラメーター</span><span class="sxs-lookup"><span data-stu-id="50445-151">Parameters</span></span>

<span data-ttu-id="50445-152">テキスト</span><span class="sxs-lookup"><span data-stu-id="50445-152">text</span></span>  

<!-- -->

<span data-ttu-id="50445-153">startLine</span><span class="sxs-lookup"><span data-stu-id="50445-153">startLine</span></span>  

<!-- -->

<span data-ttu-id="50445-154">startPos</span><span class="sxs-lookup"><span data-stu-id="50445-154">startPos</span></span>  

<!-- -->

<span data-ttu-id="50445-155">endLine</span><span class="sxs-lookup"><span data-stu-id="50445-155">endLine</span></span>  

<!-- -->

<span data-ttu-id="50445-156">endPos</span><span class="sxs-lookup"><span data-stu-id="50445-156">endPos</span></span>  

### <a name="method-linecomment"></a><span data-ttu-id="50445-157">メソッド lineComment</span><span class="sxs-lookup"><span data-stu-id="50445-157">Method lineComment</span></span>

    public void lineComment(str text, int startLine, int startPos, int endLine, int endPos)

#### <a name="parameters"></a><span data-ttu-id="50445-158">パラメーター</span><span class="sxs-lookup"><span data-stu-id="50445-158">Parameters</span></span>

<span data-ttu-id="50445-159">テキスト</span><span class="sxs-lookup"><span data-stu-id="50445-159">text</span></span>  

<!-- -->

<span data-ttu-id="50445-160">startLine</span><span class="sxs-lookup"><span data-stu-id="50445-160">startLine</span></span>  

<!-- -->

<span data-ttu-id="50445-161">startPos</span><span class="sxs-lookup"><span data-stu-id="50445-161">startPos</span></span>  

<!-- -->

<span data-ttu-id="50445-162">endLine</span><span class="sxs-lookup"><span data-stu-id="50445-162">endLine</span></span>  

<!-- -->

<span data-ttu-id="50445-163">endPos</span><span class="sxs-lookup"><span data-stu-id="50445-163">endPos</span></span>  

### <a name="method-macrodefine"></a><span data-ttu-id="50445-164">メソッド macroDefine</span><span class="sxs-lookup"><span data-stu-id="50445-164">Method macroDefine</span></span>

    public void macroDefine(str text, int startLine, int startPos, int endLine, int endPos)

#### <a name="parameters"></a><span data-ttu-id="50445-165">パラメーター</span><span class="sxs-lookup"><span data-stu-id="50445-165">Parameters</span></span>

<span data-ttu-id="50445-166">テキスト</span><span class="sxs-lookup"><span data-stu-id="50445-166">text</span></span>  

<!-- -->

<span data-ttu-id="50445-167">startLine</span><span class="sxs-lookup"><span data-stu-id="50445-167">startLine</span></span>  

<!-- -->

<span data-ttu-id="50445-168">startPos</span><span class="sxs-lookup"><span data-stu-id="50445-168">startPos</span></span>  

<!-- -->

<span data-ttu-id="50445-169">endLine</span><span class="sxs-lookup"><span data-stu-id="50445-169">endLine</span></span>  

<!-- -->

<span data-ttu-id="50445-170">endPos</span><span class="sxs-lookup"><span data-stu-id="50445-170">endPos</span></span>  

### <a name="method-new"></a><span data-ttu-id="50445-171">メソッド new</span><span class="sxs-lookup"><span data-stu-id="50445-171">Method new</span></span>

<span data-ttu-id="50445-172">Object クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="50445-172">Initializes a new instance of the Object class.</span></span>

    public void new(str source)

#### <a name="parameters"></a><span data-ttu-id="50445-173">パラメーター</span><span class="sxs-lookup"><span data-stu-id="50445-173">Parameters</span></span>

<span data-ttu-id="50445-174">ソース</span><span class="sxs-lookup"><span data-stu-id="50445-174">source</span></span>  

### <a name="method-comment"></a><span data-ttu-id="50445-175">メソッド comment</span><span class="sxs-lookup"><span data-stu-id="50445-175">Method comment</span></span>

    public void comment(str text, int startLine, int startPos, int endLine, int endPos)

#### <a name="parameters"></a><span data-ttu-id="50445-176">パラメーター</span><span class="sxs-lookup"><span data-stu-id="50445-176">Parameters</span></span>

<span data-ttu-id="50445-177">テキスト</span><span class="sxs-lookup"><span data-stu-id="50445-177">text</span></span>  

<!-- -->

<span data-ttu-id="50445-178">startLine</span><span class="sxs-lookup"><span data-stu-id="50445-178">startLine</span></span>  

<!-- -->

<span data-ttu-id="50445-179">startPos</span><span class="sxs-lookup"><span data-stu-id="50445-179">startPos</span></span>  

<!-- -->

<span data-ttu-id="50445-180">endLine</span><span class="sxs-lookup"><span data-stu-id="50445-180">endLine</span></span>  

<!-- -->

<span data-ttu-id="50445-181">endPos</span><span class="sxs-lookup"><span data-stu-id="50445-181">endPos</span></span>  

## <a name="class-searchparm"></a><span data-ttu-id="50445-182">クラス SearchParm</span><span class="sxs-lookup"><span data-stu-id="50445-182">Class SearchParm</span></span>
    class SearchParm extends Object

<span data-ttu-id="50445-183">SearchParm クラスは、カーネルと sysTreeSearch クラス間のインターフェイスとして機能し、アプリケーション オブジェクト ツリー (AOT) で検索できるようにします。</span><span class="sxs-lookup"><span data-stu-id="50445-183">The SearchParm class serves as an interface between the kernel and the sysTreeSearch class, and enables searches in the  Application Object Tree (AOT).</span></span>

### <a name="remarks"></a><span data-ttu-id="50445-184">備考</span><span class="sxs-lookup"><span data-stu-id="50445-184">Remarks</span></span>

### <a name="examples"></a><span data-ttu-id="50445-185">例</span><span class="sxs-lookup"><span data-stu-id="50445-185">Examples</span></span>

### <a name="methods"></a><span data-ttu-id="50445-186">メソッド</span><span class="sxs-lookup"><span data-stu-id="50445-186">Methods</span></span>

| <span data-ttu-id="50445-187">方法</span><span class="sxs-lookup"><span data-stu-id="50445-187">Method</span></span>                                          | <span data-ttu-id="50445-188">説明</span><span class="sxs-lookup"><span data-stu-id="50445-188">Description</span></span> |
|-------------------------------------------------|-------------|
| <span data-ttu-id="50445-189">public str nodeName(\[str name\])</span><span class="sxs-lookup"><span data-stu-id="50445-189">public str nodeName(\[str name\])</span></span>               |             |
| <span data-ttu-id="50445-190">public int nodeType(\[int type\])</span><span class="sxs-lookup"><span data-stu-id="50445-190">public int nodeType(\[int type\])</span></span>               |             |
| <span data-ttu-id="50445-191">public str nodeTypeArray()</span><span class="sxs-lookup"><span data-stu-id="50445-191">public str nodeTypeArray()</span></span>                      |             |
| <span data-ttu-id="50445-192">public str propertyName(\[str name\])</span><span class="sxs-lookup"><span data-stu-id="50445-192">public str propertyName(\[str name\])</span></span>           |             |
| <span data-ttu-id="50445-193">public str propertyValue(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="50445-193">public str propertyValue(\[str value\])</span></span>         |             |
| <span data-ttu-id="50445-194">public str replaceString(\[str replaceString\])</span><span class="sxs-lookup"><span data-stu-id="50445-194">public str replaceString(\[str replaceString\])</span></span> |             |
| <span data-ttu-id="50445-195">public int searchFlag(\[int flag\])</span><span class="sxs-lookup"><span data-stu-id="50445-195">public int searchFlag(\[int flag\])</span></span>             |             |
| <span data-ttu-id="50445-196">public str searchString(\[str searchString\])</span><span class="sxs-lookup"><span data-stu-id="50445-196">public str searchString(\[str searchString\])</span></span>   |             |
| <span data-ttu-id="50445-197">public int searchType(\[int type\])</span><span class="sxs-lookup"><span data-stu-id="50445-197">public int searchType(\[int type\])</span></span>             |             |
| <span data-ttu-id="50445-198">public boolean startSearch()</span><span class="sxs-lookup"><span data-stu-id="50445-198">public boolean startSearch()</span></span>                    |             |
| <span data-ttu-id="50445-199">public TreeNode topNode(\[TreeNode node\])</span><span class="sxs-lookup"><span data-stu-id="50445-199">public TreeNode topNode(\[TreeNode node\])</span></span>      |             |
| <span data-ttu-id="50445-200">public str topNodeName(\[str name\])</span><span class="sxs-lookup"><span data-stu-id="50445-200">public str topNodeName(\[str name\])</span></span>            |             |
| <span data-ttu-id="50445-201">public int topNodeType(\[int type\])</span><span class="sxs-lookup"><span data-stu-id="50445-201">public int topNodeType(\[int type\])</span></span>            |             |
| <span data-ttu-id="50445-202">public void preSearch()</span><span class="sxs-lookup"><span data-stu-id="50445-202">public void preSearch()</span></span>                         |             |
| <span data-ttu-id="50445-203">public void killSearch()</span><span class="sxs-lookup"><span data-stu-id="50445-203">public void killSearch()</span></span>                        |             |

### <a name="method-nodename"></a><span data-ttu-id="50445-204">メソッド nodeName</span><span class="sxs-lookup"><span data-stu-id="50445-204">Method nodeName</span></span>

    public str nodeName([str name])

#### <a name="parameters"></a><span data-ttu-id="50445-205">パラメーター</span><span class="sxs-lookup"><span data-stu-id="50445-205">Parameters</span></span>

<span data-ttu-id="50445-206">名前</span><span class="sxs-lookup"><span data-stu-id="50445-206">name</span></span>  

#### <a name="return-value"></a><span data-ttu-id="50445-207">戻り値</span><span class="sxs-lookup"><span data-stu-id="50445-207">Return Value</span></span>

### <a name="method-nodetype"></a><span data-ttu-id="50445-208">メソッド nodeType</span><span class="sxs-lookup"><span data-stu-id="50445-208">Method nodeType</span></span>

    public int nodeType([int type])

#### <a name="parameters"></a><span data-ttu-id="50445-209">パラメーター</span><span class="sxs-lookup"><span data-stu-id="50445-209">Parameters</span></span>

<span data-ttu-id="50445-210">タイプ</span><span class="sxs-lookup"><span data-stu-id="50445-210">type</span></span>  

#### <a name="return-value"></a><span data-ttu-id="50445-211">戻り値</span><span class="sxs-lookup"><span data-stu-id="50445-211">Return Value</span></span>

### <a name="method-nodetypearray"></a><span data-ttu-id="50445-212">メソッド nodeTypeArray</span><span class="sxs-lookup"><span data-stu-id="50445-212">Method nodeTypeArray</span></span>

    public str nodeTypeArray()

#### <a name="return-value"></a><span data-ttu-id="50445-213">戻り値</span><span class="sxs-lookup"><span data-stu-id="50445-213">Return Value</span></span>

### <a name="method-propertyname"></a><span data-ttu-id="50445-214">メソッド propertyName</span><span class="sxs-lookup"><span data-stu-id="50445-214">Method propertyName</span></span>

    public str propertyName([str name])

#### <a name="parameters"></a><span data-ttu-id="50445-215">パラメーター</span><span class="sxs-lookup"><span data-stu-id="50445-215">Parameters</span></span>

<span data-ttu-id="50445-216">名前</span><span class="sxs-lookup"><span data-stu-id="50445-216">name</span></span>  

#### <a name="return-value"></a><span data-ttu-id="50445-217">戻り値</span><span class="sxs-lookup"><span data-stu-id="50445-217">Return Value</span></span>

### <a name="method-propertyvalue"></a><span data-ttu-id="50445-218">メソッド propertyValue</span><span class="sxs-lookup"><span data-stu-id="50445-218">Method propertyValue</span></span>

    public str propertyValue([str value])

#### <a name="parameters"></a><span data-ttu-id="50445-219">パラメーター</span><span class="sxs-lookup"><span data-stu-id="50445-219">Parameters</span></span>

<span data-ttu-id="50445-220">値</span><span class="sxs-lookup"><span data-stu-id="50445-220">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="50445-221">戻り値</span><span class="sxs-lookup"><span data-stu-id="50445-221">Return Value</span></span>

### <a name="method-replacestring"></a><span data-ttu-id="50445-222">メソッド replaceString</span><span class="sxs-lookup"><span data-stu-id="50445-222">Method replaceString</span></span>

    public str replaceString([str replaceString])

#### <a name="parameters"></a><span data-ttu-id="50445-223">パラメーター</span><span class="sxs-lookup"><span data-stu-id="50445-223">Parameters</span></span>

<span data-ttu-id="50445-224">replaceString</span><span class="sxs-lookup"><span data-stu-id="50445-224">replaceString</span></span>  

#### <a name="return-value"></a><span data-ttu-id="50445-225">戻り値</span><span class="sxs-lookup"><span data-stu-id="50445-225">Return Value</span></span>

### <a name="method-searchflag"></a><span data-ttu-id="50445-226">メソッド searchFlag</span><span class="sxs-lookup"><span data-stu-id="50445-226">Method searchFlag</span></span>

    public int searchFlag([int flag])

#### <a name="parameters"></a><span data-ttu-id="50445-227">パラメーター</span><span class="sxs-lookup"><span data-stu-id="50445-227">Parameters</span></span>

<span data-ttu-id="50445-228">flag</span><span class="sxs-lookup"><span data-stu-id="50445-228">flag</span></span>  

#### <a name="return-value"></a><span data-ttu-id="50445-229">戻り値</span><span class="sxs-lookup"><span data-stu-id="50445-229">Return Value</span></span>

### <a name="method-searchstring"></a><span data-ttu-id="50445-230">メソッド searchString</span><span class="sxs-lookup"><span data-stu-id="50445-230">Method searchString</span></span>

    public str searchString([str searchString])

#### <a name="parameters"></a><span data-ttu-id="50445-231">パラメーター</span><span class="sxs-lookup"><span data-stu-id="50445-231">Parameters</span></span>

<span data-ttu-id="50445-232">searchString</span><span class="sxs-lookup"><span data-stu-id="50445-232">searchString</span></span>  

#### <a name="return-value"></a><span data-ttu-id="50445-233">戻り値</span><span class="sxs-lookup"><span data-stu-id="50445-233">Return Value</span></span>

### <a name="method-searchtype"></a><span data-ttu-id="50445-234">メソッド searchType</span><span class="sxs-lookup"><span data-stu-id="50445-234">Method searchType</span></span>

    public int searchType([int type])

#### <a name="parameters"></a><span data-ttu-id="50445-235">パラメーター</span><span class="sxs-lookup"><span data-stu-id="50445-235">Parameters</span></span>

<span data-ttu-id="50445-236">タイプ</span><span class="sxs-lookup"><span data-stu-id="50445-236">type</span></span>  

#### <a name="return-value"></a><span data-ttu-id="50445-237">戻り値</span><span class="sxs-lookup"><span data-stu-id="50445-237">Return Value</span></span>

### <a name="method-startsearch"></a><span data-ttu-id="50445-238">メソッド startSearch</span><span class="sxs-lookup"><span data-stu-id="50445-238">Method startSearch</span></span>

    public boolean startSearch()

#### <a name="return-value"></a><span data-ttu-id="50445-239">戻り値</span><span class="sxs-lookup"><span data-stu-id="50445-239">Return Value</span></span>

### <a name="method-topnode"></a><span data-ttu-id="50445-240">メソッド topNode</span><span class="sxs-lookup"><span data-stu-id="50445-240">Method topNode</span></span>

    public TreeNode topNode([TreeNode node])

#### <a name="parameters"></a><span data-ttu-id="50445-241">パラメーター</span><span class="sxs-lookup"><span data-stu-id="50445-241">Parameters</span></span>

<span data-ttu-id="50445-242">node</span><span class="sxs-lookup"><span data-stu-id="50445-242">node</span></span>  

#### <a name="return-value"></a><span data-ttu-id="50445-243">戻り値</span><span class="sxs-lookup"><span data-stu-id="50445-243">Return Value</span></span>

### <a name="method-topnodename"></a><span data-ttu-id="50445-244">メソッド topNodeName</span><span class="sxs-lookup"><span data-stu-id="50445-244">Method topNodeName</span></span>

    public str topNodeName([str name])

#### <a name="parameters"></a><span data-ttu-id="50445-245">パラメーター</span><span class="sxs-lookup"><span data-stu-id="50445-245">Parameters</span></span>

<span data-ttu-id="50445-246">名前</span><span class="sxs-lookup"><span data-stu-id="50445-246">name</span></span>  

#### <a name="return-value"></a><span data-ttu-id="50445-247">戻り値</span><span class="sxs-lookup"><span data-stu-id="50445-247">Return Value</span></span>

### <a name="method-topnodetype"></a><span data-ttu-id="50445-248">メソッド topNodeType</span><span class="sxs-lookup"><span data-stu-id="50445-248">Method topNodeType</span></span>

    public int topNodeType([int type])

#### <a name="parameters"></a><span data-ttu-id="50445-249">パラメーター</span><span class="sxs-lookup"><span data-stu-id="50445-249">Parameters</span></span>

<span data-ttu-id="50445-250">タイプ</span><span class="sxs-lookup"><span data-stu-id="50445-250">type</span></span>  

#### <a name="return-value"></a><span data-ttu-id="50445-251">戻り値</span><span class="sxs-lookup"><span data-stu-id="50445-251">Return Value</span></span>

### <a name="method-presearch"></a><span data-ttu-id="50445-252">メソッド preSearch</span><span class="sxs-lookup"><span data-stu-id="50445-252">Method preSearch</span></span>

    public void preSearch()

### <a name="method-killsearch"></a><span data-ttu-id="50445-253">メソッド killSearch</span><span class="sxs-lookup"><span data-stu-id="50445-253">Method killSearch</span></span>

    public void killSearch()

## <a name="class-securenode"></a><span data-ttu-id="50445-254">クラス SecureNode</span><span class="sxs-lookup"><span data-stu-id="50445-254">Class SecureNode</span></span>
    class SecureNode extends TreeNode

<span data-ttu-id="50445-255">SecureNode クラスを使用すると、X++ コードとメタデータの作成、読み取り、更新、および削除を行うことができます。</span><span class="sxs-lookup"><span data-stu-id="50445-255">The SecureNode class lets you create, read, update, and delete X++ code and metadata.</span></span>

### <a name="remarks"></a><span data-ttu-id="50445-256">備考</span><span class="sxs-lookup"><span data-stu-id="50445-256">Remarks</span></span>

<span data-ttu-id="50445-257">この API が呼び出される前に、ユーザーが開発セキュリティ キー (SysDevelopment) にアクセスできることを確認します。</span><span class="sxs-lookup"><span data-stu-id="50445-257">Make sure that the user has access to the development security key (SysDevelopment) before this API is called.</span></span>

### <a name="examples"></a><span data-ttu-id="50445-258">例</span><span class="sxs-lookup"><span data-stu-id="50445-258">Examples</span></span>

### <a name="methods"></a><span data-ttu-id="50445-259">メソッド</span><span class="sxs-lookup"><span data-stu-id="50445-259">Methods</span></span>

| <span data-ttu-id="50445-260">方法</span><span class="sxs-lookup"><span data-stu-id="50445-260">Method</span></span>                                                                          | <span data-ttu-id="50445-261">説明</span><span class="sxs-lookup"><span data-stu-id="50445-261">Description</span></span>                                                             |
|---------------------------------------------------------------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="50445-262">public boolean checkAccessRights()</span><span class="sxs-lookup"><span data-stu-id="50445-262">public boolean checkAccessRights()</span></span>                                              |                                                                         |
| <span data-ttu-id="50445-263">public ConfigurationKeyId configurationKey(\[ConfigurationKeyId value\])</span><span class="sxs-lookup"><span data-stu-id="50445-263">public ConfigurationKeyId configurationKey(\[ConfigurationKeyId value\])</span></span>        | <span data-ttu-id="50445-264">コントロールに割り当てられるコンフィギュレーション キーを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="50445-264">Gets or sets the configuration key that is assigned to the control.</span></span>     |
| <span data-ttu-id="50445-265">public ConfigurationKeyId countryConfigurationkey(\[ConfigurationKeyId value\])</span><span class="sxs-lookup"><span data-stu-id="50445-265">public ConfigurationKeyId countryConfigurationkey(\[ConfigurationKeyId value\])</span></span> |                                                                         |
| <span data-ttu-id="50445-266">public boolean extendedDataSecurity(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="50445-266">public boolean extendedDataSecurity(\[boolean value\])</span></span>                          |                                                                         |
| <span data-ttu-id="50445-267">public boolean isWeb()</span><span class="sxs-lookup"><span data-stu-id="50445-267">public boolean isWeb()</span></span>                                                          |                                                                         |
| <span data-ttu-id="50445-268">public int neededAccessLevel(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="50445-268">public int neededAccessLevel(\[int value\])</span></span>                                     | <span data-ttu-id="50445-269">MenuFunction クラスの neededAccessLevel プロパティを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="50445-269">Gets or sets the neededAccessLevel property for the MenuFunction class.</span></span> |
| <span data-ttu-id="50445-270">public SecurityKeyId securityKey(\[SecurityKeyId value\])</span><span class="sxs-lookup"><span data-stu-id="50445-270">public SecurityKeyId securityKey(\[SecurityKeyId value\])</span></span>                       |                                                                         |
| <span data-ttu-id="50445-271">public ConfigurationKeyId webConfigurationkey(\[ConfigurationKeyId value\])</span><span class="sxs-lookup"><span data-stu-id="50445-271">public ConfigurationKeyId webConfigurationkey(\[ConfigurationKeyId value\])</span></span>     |                                                                         |

### <a name="method-checkaccessrights"></a><span data-ttu-id="50445-272">メソッド checkAccessRights</span><span class="sxs-lookup"><span data-stu-id="50445-272">Method checkAccessRights</span></span>

    public boolean checkAccessRights()

#### <a name="return-value"></a><span data-ttu-id="50445-273">戻り値</span><span class="sxs-lookup"><span data-stu-id="50445-273">Return Value</span></span>

### <a name="method-configurationkey"></a><span data-ttu-id="50445-274">メソッド configurationKey</span><span class="sxs-lookup"><span data-stu-id="50445-274">Method configurationKey</span></span>

<span data-ttu-id="50445-275">コントロールに割り当てられるコンフィギュレーション キーを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="50445-275">Gets or sets the configuration key that is assigned to the control.</span></span>

    public ConfigurationKeyId configurationKey([ConfigurationKeyId value])

#### <a name="parameters"></a><span data-ttu-id="50445-276">パラメーター</span><span class="sxs-lookup"><span data-stu-id="50445-276">Parameters</span></span>

<span data-ttu-id="50445-277">値</span><span class="sxs-lookup"><span data-stu-id="50445-277">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="50445-278">戻り値</span><span class="sxs-lookup"><span data-stu-id="50445-278">Return Value</span></span>

<span data-ttu-id="50445-279">コントロールに割り当てられるコンフィギュレーションの ID。</span><span class="sxs-lookup"><span data-stu-id="50445-279">The identifier of the configuration key that is assigned to the control.</span></span>

#### <a name="remarks"></a><span data-ttu-id="50445-280">備考</span><span class="sxs-lookup"><span data-stu-id="50445-280">Remarks</span></span>

<span data-ttu-id="50445-281">コンフィギュレーション キーは、このコントロールを表示するかどうかを決定するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="50445-281">The configuration key is used to determine whether this control can be displayed.</span></span> <span data-ttu-id="50445-282">コンフィギュレーション キーがシステムで無効な場合、コントロールはフォームで表示されません。</span><span class="sxs-lookup"><span data-stu-id="50445-282">If the configuration key is disabled in the system, the control is not displayed in the form.</span></span>

### <a name="method-countryconfigurationkey"></a><span data-ttu-id="50445-283">メソッド countryConfigurationkey</span><span class="sxs-lookup"><span data-stu-id="50445-283">Method countryConfigurationkey</span></span>

    public ConfigurationKeyId countryConfigurationkey([ConfigurationKeyId value])

#### <a name="parameters"></a><span data-ttu-id="50445-284">パラメーター</span><span class="sxs-lookup"><span data-stu-id="50445-284">Parameters</span></span>

<span data-ttu-id="50445-285">値</span><span class="sxs-lookup"><span data-stu-id="50445-285">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="50445-286">戻り値</span><span class="sxs-lookup"><span data-stu-id="50445-286">Return Value</span></span>

### <a name="method-extendeddatasecurity"></a><span data-ttu-id="50445-287">メソッド extendedDataSecurity</span><span class="sxs-lookup"><span data-stu-id="50445-287">Method extendedDataSecurity</span></span>

    public boolean extendedDataSecurity([boolean value])

#### <a name="parameters"></a><span data-ttu-id="50445-288">パラメーター</span><span class="sxs-lookup"><span data-stu-id="50445-288">Parameters</span></span>

<span data-ttu-id="50445-289">値</span><span class="sxs-lookup"><span data-stu-id="50445-289">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="50445-290">戻り値</span><span class="sxs-lookup"><span data-stu-id="50445-290">Return Value</span></span>

### <a name="method-isweb"></a><span data-ttu-id="50445-291">メソッド isWeb</span><span class="sxs-lookup"><span data-stu-id="50445-291">Method isWeb</span></span>

    public boolean isWeb()

#### <a name="return-value"></a><span data-ttu-id="50445-292">戻り値</span><span class="sxs-lookup"><span data-stu-id="50445-292">Return Value</span></span>

### <a name="method-neededaccesslevel"></a><span data-ttu-id="50445-293">メソッド neededAccessLevel</span><span class="sxs-lookup"><span data-stu-id="50445-293">Method neededAccessLevel</span></span>

<span data-ttu-id="50445-294">MenuFunction クラスの neededAccessLevel プロパティを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="50445-294">Gets or sets the neededAccessLevel property for the MenuFunction class.</span></span>

    public int neededAccessLevel([int value])

#### <a name="parameters"></a><span data-ttu-id="50445-295">パラメーター</span><span class="sxs-lookup"><span data-stu-id="50445-295">Parameters</span></span>

<span data-ttu-id="50445-296">値</span><span class="sxs-lookup"><span data-stu-id="50445-296">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="50445-297">戻り値</span><span class="sxs-lookup"><span data-stu-id="50445-297">Return Value</span></span>

<span data-ttu-id="50445-298">neededAccessLevel プロパティの現在の値。</span><span class="sxs-lookup"><span data-stu-id="50445-298">The current value of the neededAccessLevel property.</span></span>

#### <a name="remarks"></a><span data-ttu-id="50445-299">備考</span><span class="sxs-lookup"><span data-stu-id="50445-299">Remarks</span></span>

<span data-ttu-id="50445-300">AccessType システム列挙値の使用可能な値は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="50445-300">The possible values for the AccessType system enumeration value are as follows:</span></span>

-   <span data-ttu-id="50445-301">AccessType::NoAccess。</span><span class="sxs-lookup"><span data-stu-id="50445-301">AccessType::NoAccess.</span></span>
-   <span data-ttu-id="50445-302">AccessType::View。</span><span class="sxs-lookup"><span data-stu-id="50445-302">AccessType::View.</span></span>
-   <span data-ttu-id="50445-303">AccessType::Edit。</span><span class="sxs-lookup"><span data-stu-id="50445-303">AccessType::Edit.</span></span>
-   <span data-ttu-id="50445-304">AccessType::Add。</span><span class="sxs-lookup"><span data-stu-id="50445-304">AccessType::Add.</span></span>
-   <span data-ttu-id="50445-305">AccessType::Delete。</span><span class="sxs-lookup"><span data-stu-id="50445-305">AccessType::Delete.</span></span>

### <a name="method-securitykey"></a><span data-ttu-id="50445-306">メソッド securityKey</span><span class="sxs-lookup"><span data-stu-id="50445-306">Method securityKey</span></span>

    public SecurityKeyId securityKey([SecurityKeyId value])

#### <a name="parameters"></a><span data-ttu-id="50445-307">パラメーター</span><span class="sxs-lookup"><span data-stu-id="50445-307">Parameters</span></span>

<span data-ttu-id="50445-308">値</span><span class="sxs-lookup"><span data-stu-id="50445-308">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="50445-309">戻り値</span><span class="sxs-lookup"><span data-stu-id="50445-309">Return Value</span></span>

### <a name="method-webconfigurationkey"></a><span data-ttu-id="50445-310">メソッド webConfigurationkey</span><span class="sxs-lookup"><span data-stu-id="50445-310">Method webConfigurationkey</span></span>

    public ConfigurationKeyId webConfigurationkey([ConfigurationKeyId value])

#### <a name="parameters"></a><span data-ttu-id="50445-311">パラメーター</span><span class="sxs-lookup"><span data-stu-id="50445-311">Parameters</span></span>

<span data-ttu-id="50445-312">値</span><span class="sxs-lookup"><span data-stu-id="50445-312">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="50445-313">戻り値</span><span class="sxs-lookup"><span data-stu-id="50445-313">Return Value</span></span>

## <a name="class-securitycontext"></a><span data-ttu-id="50445-314">クラス SecurityContext</span><span class="sxs-lookup"><span data-stu-id="50445-314">Class SecurityContext</span></span>
    class SecurityContext extends Object

### <a name="remarks"></a><span data-ttu-id="50445-315">備考</span><span class="sxs-lookup"><span data-stu-id="50445-315">Remarks</span></span>

### <a name="examples"></a><span data-ttu-id="50445-316">例</span><span class="sxs-lookup"><span data-stu-id="50445-316">Examples</span></span>

### <a name="methods"></a><span data-ttu-id="50445-317">メソッド</span><span class="sxs-lookup"><span data-stu-id="50445-317">Methods</span></span>

| <span data-ttu-id="50445-318">方法</span><span class="sxs-lookup"><span data-stu-id="50445-318">Method</span></span>                                                                                                | <span data-ttu-id="50445-319">説明</span><span class="sxs-lookup"><span data-stu-id="50445-319">Description</span></span> |
|-------------------------------------------------------------------------------------------------------|-------------|
| <span data-ttu-id="50445-320">public boolean isTableOperationAllowed(int tableId, StatementType operation, \[DataAreaId dataArea\])</span><span class="sxs-lookup"><span data-stu-id="50445-320">public boolean isTableOperationAllowed(int tableId, StatementType operation, \[DataAreaId dataArea\])</span></span> |             |
| <span data-ttu-id="50445-321">::public static SecurityContext current()</span><span class="sxs-lookup"><span data-stu-id="50445-321">::public static SecurityContext current()</span></span>                                                             |             |
| <span data-ttu-id="50445-322">::public static SecurityContext constructFromEntryPoint(SecurableType type, str name, str childName)</span><span class="sxs-lookup"><span data-stu-id="50445-322">::public static SecurityContext constructFromEntryPoint(SecurableType type, str name, str childName)</span></span>  |             |
| <span data-ttu-id="50445-323">public boolean equal(SecurityContext context)</span><span class="sxs-lookup"><span data-stu-id="50445-323">public boolean equal(SecurityContext context)</span></span>                                                         |             |
| <span data-ttu-id="50445-324">public SecurableType securableType()</span><span class="sxs-lookup"><span data-stu-id="50445-324">public SecurableType securableType()</span></span>                                                                  |             |
| <span data-ttu-id="50445-325">public str securableName()</span><span class="sxs-lookup"><span data-stu-id="50445-325">public str securableName()</span></span>                                                                            |             |
| <span data-ttu-id="50445-326">public str securableChildName()</span><span class="sxs-lookup"><span data-stu-id="50445-326">public str securableChildName()</span></span>                                                                       |             |
| <span data-ttu-id="50445-327">public void push()</span><span class="sxs-lookup"><span data-stu-id="50445-327">public void push()</span></span>                                                                                    |             |
| <span data-ttu-id="50445-328">::public static void pop()</span><span class="sxs-lookup"><span data-stu-id="50445-328">::public static void pop()</span></span>                                                                            |             |
| <span data-ttu-id="50445-329">private void new()</span><span class="sxs-lookup"><span data-stu-id="50445-329">private void new()</span></span>                                                                                    |             |

### <a name="method-istableoperationallowed"></a><span data-ttu-id="50445-330">メソッド isTableOperationAllowed</span><span class="sxs-lookup"><span data-stu-id="50445-330">Method isTableOperationAllowed</span></span>

    public boolean isTableOperationAllowed(int tableId, StatementType operation, [DataAreaId dataArea])

#### <a name="parameters"></a><span data-ttu-id="50445-331">パラメーター</span><span class="sxs-lookup"><span data-stu-id="50445-331">Parameters</span></span>

<span data-ttu-id="50445-332">tableId</span><span class="sxs-lookup"><span data-stu-id="50445-332">tableId</span></span>  

<!-- -->

<span data-ttu-id="50445-333">工程</span><span class="sxs-lookup"><span data-stu-id="50445-333">operation</span></span>  

<!-- -->

<span data-ttu-id="50445-334">dataArea</span><span class="sxs-lookup"><span data-stu-id="50445-334">dataArea</span></span>  

#### <a name="return-value"></a><span data-ttu-id="50445-335">戻り値</span><span class="sxs-lookup"><span data-stu-id="50445-335">Return Value</span></span>

### <a name="method-current"></a><span data-ttu-id="50445-336">メソッド current</span><span class="sxs-lookup"><span data-stu-id="50445-336">Method current</span></span>

    public static SecurityContext current()

#### <a name="return-value"></a><span data-ttu-id="50445-337">戻り値</span><span class="sxs-lookup"><span data-stu-id="50445-337">Return Value</span></span>

### <a name="method-constructfromentrypoint"></a><span data-ttu-id="50445-338">メソッド constructFromEntryPoint</span><span class="sxs-lookup"><span data-stu-id="50445-338">Method constructFromEntryPoint</span></span>

    public static SecurityContext constructFromEntryPoint(SecurableType type, str name, str childName)

#### <a name="parameters"></a><span data-ttu-id="50445-339">パラメーター</span><span class="sxs-lookup"><span data-stu-id="50445-339">Parameters</span></span>

<span data-ttu-id="50445-340">タイプ</span><span class="sxs-lookup"><span data-stu-id="50445-340">type</span></span>  

<!-- -->

<span data-ttu-id="50445-341">名前</span><span class="sxs-lookup"><span data-stu-id="50445-341">name</span></span>  

<!-- -->

<span data-ttu-id="50445-342">childName</span><span class="sxs-lookup"><span data-stu-id="50445-342">childName</span></span>  

#### <a name="return-value"></a><span data-ttu-id="50445-343">戻り値</span><span class="sxs-lookup"><span data-stu-id="50445-343">Return Value</span></span>

### <a name="method-equal"></a><span data-ttu-id="50445-344">メソッド equal</span><span class="sxs-lookup"><span data-stu-id="50445-344">Method equal</span></span>

    public boolean equal(SecurityContext context)

#### <a name="parameters"></a><span data-ttu-id="50445-345">パラメーター</span><span class="sxs-lookup"><span data-stu-id="50445-345">Parameters</span></span>

<span data-ttu-id="50445-346">context</span><span class="sxs-lookup"><span data-stu-id="50445-346">context</span></span>  

#### <a name="return-value"></a><span data-ttu-id="50445-347">戻り値</span><span class="sxs-lookup"><span data-stu-id="50445-347">Return Value</span></span>

### <a name="method-securabletype"></a><span data-ttu-id="50445-348">メソッド securableType</span><span class="sxs-lookup"><span data-stu-id="50445-348">Method securableType</span></span>

    public SecurableType securableType()

#### <a name="return-value"></a><span data-ttu-id="50445-349">戻り値</span><span class="sxs-lookup"><span data-stu-id="50445-349">Return Value</span></span>

### <a name="method-securablename"></a><span data-ttu-id="50445-350">メソッド securableName</span><span class="sxs-lookup"><span data-stu-id="50445-350">Method securableName</span></span>

    public str securableName()

#### <a name="return-value"></a><span data-ttu-id="50445-351">戻り値</span><span class="sxs-lookup"><span data-stu-id="50445-351">Return Value</span></span>

### <a name="method-securablechildname"></a><span data-ttu-id="50445-352">メソッド securableChildName</span><span class="sxs-lookup"><span data-stu-id="50445-352">Method securableChildName</span></span>

    public str securableChildName()

#### <a name="return-value"></a><span data-ttu-id="50445-353">戻り値</span><span class="sxs-lookup"><span data-stu-id="50445-353">Return Value</span></span>

### <a name="method-push"></a><span data-ttu-id="50445-354">メソッド push</span><span class="sxs-lookup"><span data-stu-id="50445-354">Method push</span></span>

    public void push()

### <a name="method-pop"></a><span data-ttu-id="50445-355">メソッド pop</span><span class="sxs-lookup"><span data-stu-id="50445-355">Method pop</span></span>

    public static void pop()

### <a name="method-new"></a><span data-ttu-id="50445-356">メソッド new</span><span class="sxs-lookup"><span data-stu-id="50445-356">Method new</span></span>

    private void new()

## <a name="class-securitypolicy"></a><span data-ttu-id="50445-357">クラス SecurityPolicy</span><span class="sxs-lookup"><span data-stu-id="50445-357">Class SecurityPolicy</span></span>
    class SecurityPolicy extends Object

<span data-ttu-id="50445-358">SecurityPolicy クラスには、セキュリティ ポリシーに関する情報が含まれます。</span><span class="sxs-lookup"><span data-stu-id="50445-358">The SecurityPolicy class holds the information about the security policies.</span></span>

### <a name="remarks"></a><span data-ttu-id="50445-359">備考</span><span class="sxs-lookup"><span data-stu-id="50445-359">Remarks</span></span>

### <a name="examples"></a><span data-ttu-id="50445-360">例</span><span class="sxs-lookup"><span data-stu-id="50445-360">Examples</span></span>

### <a name="methods"></a><span data-ttu-id="50445-361">方法</span><span class="sxs-lookup"><span data-stu-id="50445-361">Methods</span></span>

| <span data-ttu-id="50445-362">方法</span><span class="sxs-lookup"><span data-stu-id="50445-362">Method</span></span>                                                                 | <span data-ttu-id="50445-363">説明</span><span class="sxs-lookup"><span data-stu-id="50445-363">Description</span></span>                                             |
|------------------------------------------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="50445-364">::public static void synchronizeAllPolicies()</span><span class="sxs-lookup"><span data-stu-id="50445-364">::public static void synchronizeAllPolicies()</span></span>                          |                                                         |
| <span data-ttu-id="50445-365">::public static void synchronizePolicy(UtilElementName securityPolicy)</span><span class="sxs-lookup"><span data-stu-id="50445-365">::public static void synchronizePolicy(UtilElementName securityPolicy)</span></span> |                                                         |
| <span data-ttu-id="50445-366">public void new()</span><span class="sxs-lookup"><span data-stu-id="50445-366">public void new()</span></span>                                                      | <span data-ttu-id="50445-367">SecurityPolicy クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="50445-367">Initializes a new instance of the SecurityPolicy class.</span></span> |

### <a name="method-synchronizeallpolicies"></a><span data-ttu-id="50445-368">メソッド synchronizeAllPolicies</span><span class="sxs-lookup"><span data-stu-id="50445-368">Method synchronizeAllPolicies</span></span>

    public static void synchronizeAllPolicies()

### <a name="method-synchronizepolicy"></a><span data-ttu-id="50445-369">メソッド synchronizePolicy</span><span class="sxs-lookup"><span data-stu-id="50445-369">Method synchronizePolicy</span></span>

    public static void synchronizePolicy(UtilElementName securityPolicy)

#### <a name="parameters"></a><span data-ttu-id="50445-370">パラメーター</span><span class="sxs-lookup"><span data-stu-id="50445-370">Parameters</span></span>

<span data-ttu-id="50445-371">securityPolicy</span><span class="sxs-lookup"><span data-stu-id="50445-371">securityPolicy</span></span>  

### <a name="method-new"></a><span data-ttu-id="50445-372">メソッド new</span><span class="sxs-lookup"><span data-stu-id="50445-372">Method new</span></span>

<span data-ttu-id="50445-373">SecurityPolicy クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="50445-373">Initializes a new instance of the SecurityPolicy class.</span></span>

    public void new()

## <a name="class-securityrights"></a><span data-ttu-id="50445-374">クラス SecurityRights</span><span class="sxs-lookup"><span data-stu-id="50445-374">Class SecurityRights</span></span>
    class SecurityRights extends Object

<span data-ttu-id="50445-375">SecurityRights クラスには、セキュリティの権利とアクセス許可の管理に関する情報が含まれます。</span><span class="sxs-lookup"><span data-stu-id="50445-375">The SecurityRights class holds the information about the security rights and permissions management.</span></span>

### <a name="remarks"></a><span data-ttu-id="50445-376">備考</span><span class="sxs-lookup"><span data-stu-id="50445-376">Remarks</span></span>

### <a name="examples"></a><span data-ttu-id="50445-377">例</span><span class="sxs-lookup"><span data-stu-id="50445-377">Examples</span></span>

### <a name="methods"></a><span data-ttu-id="50445-378">メソッド</span><span class="sxs-lookup"><span data-stu-id="50445-378">Methods</span></span>

| <span data-ttu-id="50445-379">方法</span><span class="sxs-lookup"><span data-stu-id="50445-379">Method</span></span>                                                                                                                                                                                 | <span data-ttu-id="50445-380">説明</span><span class="sxs-lookup"><span data-stu-id="50445-380">Description</span></span>                                                            |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| <span data-ttu-id="50445-381">public boolean hasDataServiceAccess(SecurableName name, StatementType operation, \[SecurableChildName fieldName\])</span><span class="sxs-lookup"><span data-stu-id="50445-381">public boolean hasDataServiceAccess(SecurableName name, StatementType operation, \[SecurableChildName fieldName\])</span></span>                                                                     |                                                                        |
| <span data-ttu-id="50445-382">public boolean hasDataServiceMethodAccess(SecurableName name, StatementType operation, SecurableChildName methodName)</span><span class="sxs-lookup"><span data-stu-id="50445-382">public boolean hasDataServiceMethodAccess(SecurableName name, StatementType operation, SecurableChildName methodName)</span></span>                                                                  |                                                                        |
| <span data-ttu-id="50445-383">public AccessRight dataManagementAccessRight(SecurableName dataEntityName, \[SecurableChildName fieldName\])</span><span class="sxs-lookup"><span data-stu-id="50445-383">public AccessRight dataManagementAccessRight(SecurableName dataEntityName, \[SecurableChildName fieldName\])</span></span>                                                                           |                                                                        |
| <span data-ttu-id="50445-384">public str listDataServiceAccess(SecurableName name, \[SecurableChildName context\])</span><span class="sxs-lookup"><span data-stu-id="50445-384">public str listDataServiceAccess(SecurableName name, \[SecurableChildName context\])</span></span>                                                                                                   |                                                                        |
| <span data-ttu-id="50445-385">public AccessRight fieldAccessRight(TableName tableName, FieldName fieldName, \[Common record\], \[DataAreaId dataArea\], \[boolean includeDerived\], \[AutoAuthzMode autoAuthzMode\])</span><span class="sxs-lookup"><span data-stu-id="50445-385">public AccessRight fieldAccessRight(TableName tableName, FieldName fieldName, \[Common record\], \[DataAreaId dataArea\], \[boolean includeDerived\], \[AutoAuthzMode autoAuthzMode\])</span></span> | <span data-ttu-id="50445-386">テーブルのフィールドのアクセス権を取得します。</span><span class="sxs-lookup"><span data-stu-id="50445-386">Retrieves the access rights for the field of the table.</span></span>                |
| <span data-ttu-id="50445-387">public AccessRight formControlAccessRight(FormName form, UtilElementName control, \[Common record\], \[DataAreaId dataArea\])</span><span class="sxs-lookup"><span data-stu-id="50445-387">public AccessRight formControlAccessRight(FormName form, UtilElementName control, \[Common record\], \[DataAreaId dataArea\])</span></span>                                                          | <span data-ttu-id="50445-388">フォーム コントロールのアクセス権を取得します。</span><span class="sxs-lookup"><span data-stu-id="50445-388">Retrieves the access rights for the form control.</span></span>                      |
| <span data-ttu-id="50445-389">public container getSelectableCompanies()</span><span class="sxs-lookup"><span data-stu-id="50445-389">public container getSelectableCompanies()</span></span>                                                                                                                                              |                                                                        |
| <span data-ttu-id="50445-390">public boolean hasMenuAccess(MenuName menu, \[boolean isWebMenu\])</span><span class="sxs-lookup"><span data-stu-id="50445-390">public boolean hasMenuAccess(MenuName menu, \[boolean isWebMenu\])</span></span>                                                                                                                     | <span data-ttu-id="50445-391">ユーザーが指定されたメニューにアクセスできるかどうかをチェックします。</span><span class="sxs-lookup"><span data-stu-id="50445-391">Checks whether the user has access to the specified menu.</span></span>              |
| <span data-ttu-id="50445-392">public boolean hasMenuItemAccess(SecurableType type, MenuItemName menuItem, \[Common record\], \[DataAreaId dataArea\])</span><span class="sxs-lookup"><span data-stu-id="50445-392">public boolean hasMenuItemAccess(SecurableType type, MenuItemName menuItem, \[Common record\], \[DataAreaId dataArea\])</span></span>                                                                | <span data-ttu-id="50445-393">ユーザーが指定されたメニュー項目にアクセスできるかどうかをチェックします。</span><span class="sxs-lookup"><span data-stu-id="50445-393">Checks whether the user has access to the specified menu item.</span></span>         |
| <span data-ttu-id="50445-394">public boolean SysObsoleteAttribute(ClassName class, MethodName method)</span><span class="sxs-lookup"><span data-stu-id="50445-394">public boolean SysObsoleteAttribute(ClassName class, MethodName method)</span></span>                                                                                                                |                                                                        |
| <span data-ttu-id="50445-395">public boolean hasServiceOperationAccess(UtilElementName service, UtilElementName operation)</span><span class="sxs-lookup"><span data-stu-id="50445-395">public boolean hasServiceOperationAccess(UtilElementName service, UtilElementName operation)</span></span>                                                                                           | <span data-ttu-id="50445-396">ユーザーが指定されたサービス操作にアクセスできるかどうかをチェックします。</span><span class="sxs-lookup"><span data-stu-id="50445-396">Checks whether the user has access to the specified service operation.</span></span> |
| <span data-ttu-id="50445-397">public boolean isDeveloper()</span><span class="sxs-lookup"><span data-stu-id="50445-397">public boolean isDeveloper()</span></span>                                                                                                                                                           |                                                                        |
| <span data-ttu-id="50445-398">public boolean isSystemAdministrator()</span><span class="sxs-lookup"><span data-stu-id="50445-398">public boolean isSystemAdministrator()</span></span>                                                                                                                                                 | <span data-ttu-id="50445-399">現在のユーザーがシステム管理者であるかどうかを確認します。</span><span class="sxs-lookup"><span data-stu-id="50445-399">Checks whether the current user is a system administrator.</span></span>             |
| <span data-ttu-id="50445-400">public AccessRight menuItemAccessRight(SecurableType type, MenuItemName menuItem, \[DataAreaId dataArea\])</span><span class="sxs-lookup"><span data-stu-id="50445-400">public AccessRight menuItemAccessRight(SecurableType type, MenuItemName menuItem, \[DataAreaId dataArea\])</span></span>                                                                             | <span data-ttu-id="50445-401">メニュー項目のアクセス権を取得します。</span><span class="sxs-lookup"><span data-stu-id="50445-401">Retrieves the access rights for the menu item.</span></span>                         |
| <span data-ttu-id="50445-402">public AccessRight tableAccessRight(TableName tableName, \[Common record\], \[DataAreaId dataArea\], \[boolean includeDerived\], \[AutoAuthzMode autoAuthzMode\])</span><span class="sxs-lookup"><span data-stu-id="50445-402">public AccessRight tableAccessRight(TableName tableName, \[Common record\], \[DataAreaId dataArea\], \[boolean includeDerived\], \[AutoAuthzMode autoAuthzMode\])</span></span>                      | <span data-ttu-id="50445-403">テーブルのアクセス権を取得します。</span><span class="sxs-lookup"><span data-stu-id="50445-403">Retrieves the access rights for the table.</span></span>                             |
| <span data-ttu-id="50445-404">public SecurityTableRights tableFieldAccessRights(TableName tableName, \[Common record\], \[DataAreaId dataArea\], \[boolean includeDerived\], \[AutoAuthzMode autoAuthzMode\])</span><span class="sxs-lookup"><span data-stu-id="50445-404">public SecurityTableRights tableFieldAccessRights(TableName tableName, \[Common record\], \[DataAreaId dataArea\], \[boolean includeDerived\], \[AutoAuthzMode autoAuthzMode\])</span></span>        | <span data-ttu-id="50445-405">テーブルのフィールド アクセス権を取得します。</span><span class="sxs-lookup"><span data-stu-id="50445-405">Retrieves the field access rights for the table.</span></span>                       |
| <span data-ttu-id="50445-406">public Set variableAccessFields(TableName tableName, \[AccessRight targetAccess\], \[DataAreaId dataArea\])</span><span class="sxs-lookup"><span data-stu-id="50445-406">public Set variableAccessFields(TableName tableName, \[AccessRight targetAccess\], \[DataAreaId dataArea\])</span></span>                                                                            | <span data-ttu-id="50445-407">一連のテーブル フィールド ID を取得します。</span><span class="sxs-lookup"><span data-stu-id="50445-407">Retrieves a set of the table field IDs.</span></span>                                |
| <span data-ttu-id="50445-408">public AccessRight webContentAccessRight(SecurableType type, WebContentItemName name)</span><span class="sxs-lookup"><span data-stu-id="50445-408">public AccessRight webContentAccessRight(SecurableType type, WebContentItemName name)</span></span>                                                                                                  | <span data-ttu-id="50445-409">Web コンテンツ項目のアクセス権を取得します。</span><span class="sxs-lookup"><span data-stu-id="50445-409">Retrieves the access rights for the web content item.</span></span>                  |
| <span data-ttu-id="50445-410">::public static SecurityRights construct()</span><span class="sxs-lookup"><span data-stu-id="50445-410">::public static SecurityRights construct()</span></span>                                                                                                                                             | <span data-ttu-id="50445-411">現在のユーザーの新しいセキュリティ権限インスタンスを作成します。</span><span class="sxs-lookup"><span data-stu-id="50445-411">Creates a new security rights instance for the current user.</span></span>           |
| <span data-ttu-id="50445-412">::public static SecurityRights newUser(UserId user)</span><span class="sxs-lookup"><span data-stu-id="50445-412">::public static SecurityRights newUser(UserId user)</span></span>                                                                                                                                    | <span data-ttu-id="50445-413">特定のユーザーの新しいセキュリティ権限インスタンスを作成します。</span><span class="sxs-lookup"><span data-stu-id="50445-413">Creates a new security rights instance for the specified user.</span></span>         |
| <span data-ttu-id="50445-414">private void new()</span><span class="sxs-lookup"><span data-stu-id="50445-414">private void new()</span></span>                                                                                                                                                                     | <span data-ttu-id="50445-415">SecurityRights クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="50445-415">Initializes a new instance of the SecurityRights class.</span></span>                |
| <span data-ttu-id="50445-416">public void populateSelectableCompanies()</span><span class="sxs-lookup"><span data-stu-id="50445-416">public void populateSelectableCompanies()</span></span>                                                                                                                                              | <span data-ttu-id="50445-417">選択できる会社を取得します。</span><span class="sxs-lookup"><span data-stu-id="50445-417">Populates the selectable companies.</span></span>                                    |

### <a name="method-hasdataserviceaccess"></a><span data-ttu-id="50445-418">メソッド hasDataServiceAccess</span><span class="sxs-lookup"><span data-stu-id="50445-418">Method hasDataServiceAccess</span></span>

    public boolean hasDataServiceAccess(SecurableName name, StatementType operation, [SecurableChildName fieldName])

#### <a name="parameters"></a><span data-ttu-id="50445-419">パラメーター</span><span class="sxs-lookup"><span data-stu-id="50445-419">Parameters</span></span>

<span data-ttu-id="50445-420">名前</span><span class="sxs-lookup"><span data-stu-id="50445-420">name</span></span>  

<!-- -->

<span data-ttu-id="50445-421">工程</span><span class="sxs-lookup"><span data-stu-id="50445-421">operation</span></span>  

<!-- -->

<span data-ttu-id="50445-422">fieldName</span><span class="sxs-lookup"><span data-stu-id="50445-422">fieldName</span></span>  

#### <a name="return-value"></a><span data-ttu-id="50445-423">戻り値</span><span class="sxs-lookup"><span data-stu-id="50445-423">Return Value</span></span>

### <a name="method-hasdataservicemethodaccess"></a><span data-ttu-id="50445-424">メソッド hasDataServiceMethodAccess</span><span class="sxs-lookup"><span data-stu-id="50445-424">Method hasDataServiceMethodAccess</span></span>

    public boolean hasDataServiceMethodAccess(SecurableName name, StatementType operation, SecurableChildName methodName)

#### <a name="parameters"></a><span data-ttu-id="50445-425">パラメーター</span><span class="sxs-lookup"><span data-stu-id="50445-425">Parameters</span></span>

<span data-ttu-id="50445-426">名前</span><span class="sxs-lookup"><span data-stu-id="50445-426">name</span></span>  

<!-- -->

<span data-ttu-id="50445-427">工程</span><span class="sxs-lookup"><span data-stu-id="50445-427">operation</span></span>  

<!-- -->

<span data-ttu-id="50445-428">methodName</span><span class="sxs-lookup"><span data-stu-id="50445-428">methodName</span></span>  

#### <a name="return-value"></a><span data-ttu-id="50445-429">戻り値</span><span class="sxs-lookup"><span data-stu-id="50445-429">Return Value</span></span>

### <a name="method-datamanagementaccessright"></a><span data-ttu-id="50445-430">メソッド dataManagementAccessRight</span><span class="sxs-lookup"><span data-stu-id="50445-430">Method dataManagementAccessRight</span></span>

    public AccessRight dataManagementAccessRight(SecurableName dataEntityName, [SecurableChildName fieldName])

#### <a name="parameters"></a><span data-ttu-id="50445-431">パラメーター</span><span class="sxs-lookup"><span data-stu-id="50445-431">Parameters</span></span>

<span data-ttu-id="50445-432">dataEntityName</span><span class="sxs-lookup"><span data-stu-id="50445-432">dataEntityName</span></span>  

<!-- -->

<span data-ttu-id="50445-433">fieldName</span><span class="sxs-lookup"><span data-stu-id="50445-433">fieldName</span></span>  

#### <a name="return-value"></a><span data-ttu-id="50445-434">戻り値</span><span class="sxs-lookup"><span data-stu-id="50445-434">Return Value</span></span>

### <a name="method-listdataserviceaccess"></a><span data-ttu-id="50445-435">メソッド listDataServiceAccess</span><span class="sxs-lookup"><span data-stu-id="50445-435">Method listDataServiceAccess</span></span>

    public str listDataServiceAccess(SecurableName name, [SecurableChildName context])

#### <a name="parameters"></a><span data-ttu-id="50445-436">パラメーター</span><span class="sxs-lookup"><span data-stu-id="50445-436">Parameters</span></span>

<span data-ttu-id="50445-437">名前</span><span class="sxs-lookup"><span data-stu-id="50445-437">name</span></span>  

<!-- -->

<span data-ttu-id="50445-438">context</span><span class="sxs-lookup"><span data-stu-id="50445-438">context</span></span>  

#### <a name="return-value"></a><span data-ttu-id="50445-439">戻り値</span><span class="sxs-lookup"><span data-stu-id="50445-439">Return Value</span></span>

### <a name="method-fieldaccessright"></a><span data-ttu-id="50445-440">メソッド fieldAccessRight</span><span class="sxs-lookup"><span data-stu-id="50445-440">Method fieldAccessRight</span></span>

<span data-ttu-id="50445-441">テーブルのフィールドのアクセス権を取得します。</span><span class="sxs-lookup"><span data-stu-id="50445-441">Retrieves the access rights for the field of the table.</span></span>

    public AccessRight fieldAccessRight(TableName tableName, FieldName fieldName, [Common record], [DataAreaId dataArea], [boolean includeDerived], [AutoAuthzMode autoAuthzMode])

#### <a name="parameters"></a><span data-ttu-id="50445-442">パラメーター</span><span class="sxs-lookup"><span data-stu-id="50445-442">Parameters</span></span>

<span data-ttu-id="50445-443">tableName</span><span class="sxs-lookup"><span data-stu-id="50445-443">tableName</span></span>  

<!-- -->

<span data-ttu-id="50445-444">fieldName</span><span class="sxs-lookup"><span data-stu-id="50445-444">fieldName</span></span>  

<!-- -->

<span data-ttu-id="50445-445">記録</span><span class="sxs-lookup"><span data-stu-id="50445-445">record</span></span>  

<!-- -->

<span data-ttu-id="50445-446">dataArea</span><span class="sxs-lookup"><span data-stu-id="50445-446">dataArea</span></span>  

<!-- -->

<span data-ttu-id="50445-447">includeDerived</span><span class="sxs-lookup"><span data-stu-id="50445-447">includeDerived</span></span>  

<!-- -->

<span data-ttu-id="50445-448">autoAuthzMode</span><span class="sxs-lookup"><span data-stu-id="50445-448">autoAuthzMode</span></span>  

#### <a name="return-value"></a><span data-ttu-id="50445-449">戻り値</span><span class="sxs-lookup"><span data-stu-id="50445-449">Return Value</span></span>

<span data-ttu-id="50445-450">テーブルのフィールドの AccesRight インスタンス。</span><span class="sxs-lookup"><span data-stu-id="50445-450">The AccesRight instance for the field of the table.</span></span>

### <a name="method-formcontrolaccessright"></a><span data-ttu-id="50445-451">メソッド formControlAccessRight</span><span class="sxs-lookup"><span data-stu-id="50445-451">Method formControlAccessRight</span></span>

<span data-ttu-id="50445-452">フォーム コントロールのアクセス権を取得します。</span><span class="sxs-lookup"><span data-stu-id="50445-452">Retrieves the access rights for the form control.</span></span>

    public AccessRight formControlAccessRight(FormName form, UtilElementName control, [Common record], [DataAreaId dataArea])

#### <a name="parameters"></a><span data-ttu-id="50445-453">パラメーター</span><span class="sxs-lookup"><span data-stu-id="50445-453">Parameters</span></span>

<span data-ttu-id="50445-454">フォーム</span><span class="sxs-lookup"><span data-stu-id="50445-454">form</span></span>  

<!-- -->

<span data-ttu-id="50445-455">control</span><span class="sxs-lookup"><span data-stu-id="50445-455">control</span></span>  

<!-- -->

<span data-ttu-id="50445-456">記録</span><span class="sxs-lookup"><span data-stu-id="50445-456">record</span></span>  

<!-- -->

<span data-ttu-id="50445-457">dataArea</span><span class="sxs-lookup"><span data-stu-id="50445-457">dataArea</span></span>  

#### <a name="return-value"></a><span data-ttu-id="50445-458">戻り値</span><span class="sxs-lookup"><span data-stu-id="50445-458">Return Value</span></span>

<span data-ttu-id="50445-459">フォーム コントロールの AccesRight インスタンス。</span><span class="sxs-lookup"><span data-stu-id="50445-459">The AccesRight instance for the form control.</span></span>

### <a name="method-getselectablecompanies"></a><span data-ttu-id="50445-460">メソッド getSelectableCompanies</span><span class="sxs-lookup"><span data-stu-id="50445-460">Method getSelectableCompanies</span></span>

    public container getSelectableCompanies()

#### <a name="return-value"></a><span data-ttu-id="50445-461">戻り値</span><span class="sxs-lookup"><span data-stu-id="50445-461">Return Value</span></span>

### <a name="method-hasmenuaccess"></a><span data-ttu-id="50445-462">メソッド hasMenuAccess</span><span class="sxs-lookup"><span data-stu-id="50445-462">Method hasMenuAccess</span></span>

<span data-ttu-id="50445-463">ユーザーが指定されたメニューにアクセスできるかどうかをチェックします。</span><span class="sxs-lookup"><span data-stu-id="50445-463">Checks whether the user has access to the specified menu.</span></span>

    public boolean hasMenuAccess(MenuName menu, [boolean isWebMenu])

#### <a name="parameters"></a><span data-ttu-id="50445-464">パラメーター</span><span class="sxs-lookup"><span data-stu-id="50445-464">Parameters</span></span>

<span data-ttu-id="50445-465">メニュー</span><span class="sxs-lookup"><span data-stu-id="50445-465">menu</span></span>  

<!-- -->

<span data-ttu-id="50445-466">isWebMenu</span><span class="sxs-lookup"><span data-stu-id="50445-466">isWebMenu</span></span>  

#### <a name="return-value"></a><span data-ttu-id="50445-467">戻り値</span><span class="sxs-lookup"><span data-stu-id="50445-467">Return Value</span></span>

<span data-ttu-id="50445-468">ユーザーがメニューへのアクセス権を持つ場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="50445-468">true if the user has access to the menu; otherwise, false.</span></span>

### <a name="method-hasmenuitemaccess"></a><span data-ttu-id="50445-469">メソッド hasMenuItemAccess</span><span class="sxs-lookup"><span data-stu-id="50445-469">Method hasMenuItemAccess</span></span>

<span data-ttu-id="50445-470">ユーザーが指定されたメニュー項目にアクセスできるかどうかをチェックします。</span><span class="sxs-lookup"><span data-stu-id="50445-470">Checks whether the user has access to the specified menu item.</span></span>

    public boolean hasMenuItemAccess(SecurableType type, MenuItemName menuItem, [Common record], [DataAreaId dataArea])

#### <a name="parameters"></a><span data-ttu-id="50445-471">パラメーター</span><span class="sxs-lookup"><span data-stu-id="50445-471">Parameters</span></span>

<span data-ttu-id="50445-472">タイプ</span><span class="sxs-lookup"><span data-stu-id="50445-472">type</span></span>  

<!-- -->

<span data-ttu-id="50445-473">menuItem</span><span class="sxs-lookup"><span data-stu-id="50445-473">menuItem</span></span>  

<!-- -->

<span data-ttu-id="50445-474">記録</span><span class="sxs-lookup"><span data-stu-id="50445-474">record</span></span>  

<!-- -->

<span data-ttu-id="50445-475">dataArea</span><span class="sxs-lookup"><span data-stu-id="50445-475">dataArea</span></span>  

#### <a name="return-value"></a><span data-ttu-id="50445-476">戻り値</span><span class="sxs-lookup"><span data-stu-id="50445-476">Return Value</span></span>

<span data-ttu-id="50445-477">ユーザーがメニュー項目へのアクセス権を持つ場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="50445-477">true if the user has access to the menu item; otherwise, false.</span></span>

### <a name="method-sysobsoleteattribute"></a><span data-ttu-id="50445-478">メソッド SysObsoleteAttribute</span><span class="sxs-lookup"><span data-stu-id="50445-478">Method SysObsoleteAttribute</span></span>

    public boolean SysObsoleteAttribute(ClassName class, MethodName method)

#### <a name="parameters"></a><span data-ttu-id="50445-479">パラメーター</span><span class="sxs-lookup"><span data-stu-id="50445-479">Parameters</span></span>

<span data-ttu-id="50445-480">クラス</span><span class="sxs-lookup"><span data-stu-id="50445-480">class</span></span>  

<!-- -->

<span data-ttu-id="50445-481">メソッド</span><span class="sxs-lookup"><span data-stu-id="50445-481">method</span></span>  

#### <a name="return-value"></a><span data-ttu-id="50445-482">戻り値</span><span class="sxs-lookup"><span data-stu-id="50445-482">Return Value</span></span>

### <a name="method-hasserviceoperationaccess"></a><span data-ttu-id="50445-483">メソッド hasServiceOperationAccess</span><span class="sxs-lookup"><span data-stu-id="50445-483">Method hasServiceOperationAccess</span></span>

<span data-ttu-id="50445-484">ユーザーが指定されたサービス操作にアクセスできるかどうかをチェックします。</span><span class="sxs-lookup"><span data-stu-id="50445-484">Checks whether the user has access to the specified service operation.</span></span>

    public boolean hasServiceOperationAccess(UtilElementName service, UtilElementName operation)

#### <a name="parameters"></a><span data-ttu-id="50445-485">パラメーター</span><span class="sxs-lookup"><span data-stu-id="50445-485">Parameters</span></span>

<span data-ttu-id="50445-486">サービス</span><span class="sxs-lookup"><span data-stu-id="50445-486">service</span></span>  

<!-- -->

<span data-ttu-id="50445-487">工程</span><span class="sxs-lookup"><span data-stu-id="50445-487">operation</span></span>  

#### <a name="return-value"></a><span data-ttu-id="50445-488">戻り値</span><span class="sxs-lookup"><span data-stu-id="50445-488">Return Value</span></span>

<span data-ttu-id="50445-489">ユーザーがサービス操作へのアクセス権を持つ場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="50445-489">true if user has access to the service operation; otherwise, false.</span></span>

### <a name="method-isdeveloper"></a><span data-ttu-id="50445-490">メソッド isDeveloper</span><span class="sxs-lookup"><span data-stu-id="50445-490">Method isDeveloper</span></span>

    public boolean isDeveloper()

#### <a name="return-value"></a><span data-ttu-id="50445-491">戻り値</span><span class="sxs-lookup"><span data-stu-id="50445-491">Return Value</span></span>

### <a name="method-issystemadministrator"></a><span data-ttu-id="50445-492">メソッド isSystemAdministrator</span><span class="sxs-lookup"><span data-stu-id="50445-492">Method isSystemAdministrator</span></span>

<span data-ttu-id="50445-493">現在のユーザーがシステム管理者であるかどうかを確認します。</span><span class="sxs-lookup"><span data-stu-id="50445-493">Checks whether the current user is a system administrator.</span></span>

    public boolean isSystemAdministrator()

#### <a name="return-value"></a><span data-ttu-id="50445-494">戻り値</span><span class="sxs-lookup"><span data-stu-id="50445-494">Return Value</span></span>

<span data-ttu-id="50445-495">現在のユーザーがシステム管理者である場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="50445-495">true if the current user is a system administrator; otherwise, false.</span></span>

### <a name="method-menuitemaccessright"></a><span data-ttu-id="50445-496">メソッド menuItemAccessRight</span><span class="sxs-lookup"><span data-stu-id="50445-496">Method menuItemAccessRight</span></span>

<span data-ttu-id="50445-497">メニュー項目のアクセス権を取得します。</span><span class="sxs-lookup"><span data-stu-id="50445-497">Retrieves the access rights for the menu item.</span></span>

    public AccessRight menuItemAccessRight(SecurableType type, MenuItemName menuItem, [DataAreaId dataArea])

#### <a name="parameters"></a><span data-ttu-id="50445-498">パラメーター</span><span class="sxs-lookup"><span data-stu-id="50445-498">Parameters</span></span>

<span data-ttu-id="50445-499">タイプ</span><span class="sxs-lookup"><span data-stu-id="50445-499">type</span></span>  

<!-- -->

<span data-ttu-id="50445-500">menuItem</span><span class="sxs-lookup"><span data-stu-id="50445-500">menuItem</span></span>  

<!-- -->

<span data-ttu-id="50445-501">dataArea</span><span class="sxs-lookup"><span data-stu-id="50445-501">dataArea</span></span>  

#### <a name="return-value"></a><span data-ttu-id="50445-502">戻り値</span><span class="sxs-lookup"><span data-stu-id="50445-502">Return Value</span></span>

<span data-ttu-id="50445-503">項目の AccesRight インスタンス。</span><span class="sxs-lookup"><span data-stu-id="50445-503">The AccesRight instance for the item.</span></span>

### <a name="method-tableaccessright"></a><span data-ttu-id="50445-504">メソッド tableAccessRight</span><span class="sxs-lookup"><span data-stu-id="50445-504">Method tableAccessRight</span></span>

<span data-ttu-id="50445-505">テーブルのアクセス権を取得します。</span><span class="sxs-lookup"><span data-stu-id="50445-505">Retrieves the access rights for the table.</span></span>

    public AccessRight tableAccessRight(TableName tableName, [Common record], [DataAreaId dataArea], [boolean includeDerived], [AutoAuthzMode autoAuthzMode])

#### <a name="parameters"></a><span data-ttu-id="50445-506">パラメーター</span><span class="sxs-lookup"><span data-stu-id="50445-506">Parameters</span></span>

<span data-ttu-id="50445-507">tableName</span><span class="sxs-lookup"><span data-stu-id="50445-507">tableName</span></span>  

<!-- -->

<span data-ttu-id="50445-508">記録</span><span class="sxs-lookup"><span data-stu-id="50445-508">record</span></span>  

<!-- -->

<span data-ttu-id="50445-509">dataArea</span><span class="sxs-lookup"><span data-stu-id="50445-509">dataArea</span></span>  

<!-- -->

<span data-ttu-id="50445-510">includeDerived</span><span class="sxs-lookup"><span data-stu-id="50445-510">includeDerived</span></span>  

<!-- -->

<span data-ttu-id="50445-511">autoAuthzMode</span><span class="sxs-lookup"><span data-stu-id="50445-511">autoAuthzMode</span></span>  

#### <a name="return-value"></a><span data-ttu-id="50445-512">戻り値</span><span class="sxs-lookup"><span data-stu-id="50445-512">Return Value</span></span>

<span data-ttu-id="50445-513">テーブルの AccesRight インスタンス。</span><span class="sxs-lookup"><span data-stu-id="50445-513">The AccesRight instance for the table.</span></span>

### <a name="method-tablefieldaccessrights"></a><span data-ttu-id="50445-514">メソッド tableFieldAccessRights</span><span class="sxs-lookup"><span data-stu-id="50445-514">Method tableFieldAccessRights</span></span>

<span data-ttu-id="50445-515">テーブルのフィールド アクセス権を取得します。</span><span class="sxs-lookup"><span data-stu-id="50445-515">Retrieves the field access rights for the table.</span></span>

    public SecurityTableRights tableFieldAccessRights(TableName tableName, [Common record], [DataAreaId dataArea], [boolean includeDerived], [AutoAuthzMode autoAuthzMode])

#### <a name="parameters"></a><span data-ttu-id="50445-516">パラメーター</span><span class="sxs-lookup"><span data-stu-id="50445-516">Parameters</span></span>

<span data-ttu-id="50445-517">tableName</span><span class="sxs-lookup"><span data-stu-id="50445-517">tableName</span></span>  

<!-- -->

<span data-ttu-id="50445-518">記録</span><span class="sxs-lookup"><span data-stu-id="50445-518">record</span></span>  

<!-- -->

<span data-ttu-id="50445-519">dataArea</span><span class="sxs-lookup"><span data-stu-id="50445-519">dataArea</span></span>  

<!-- -->

<span data-ttu-id="50445-520">includeDerived</span><span class="sxs-lookup"><span data-stu-id="50445-520">includeDerived</span></span>  

<!-- -->

<span data-ttu-id="50445-521">autoAuthzMode</span><span class="sxs-lookup"><span data-stu-id="50445-521">autoAuthzMode</span></span>  

#### <a name="return-value"></a><span data-ttu-id="50445-522">戻り値</span><span class="sxs-lookup"><span data-stu-id="50445-522">Return Value</span></span>

<span data-ttu-id="50445-523">テーブルの SecurityTableRights インスタンス。</span><span class="sxs-lookup"><span data-stu-id="50445-523">The SecurityTableRights instance for the table.</span></span>

### <a name="method-variableaccessfields"></a><span data-ttu-id="50445-524">メソッド variableAccessFields</span><span class="sxs-lookup"><span data-stu-id="50445-524">Method variableAccessFields</span></span>

<span data-ttu-id="50445-525">一連のテーブル フィールド ID を取得します。</span><span class="sxs-lookup"><span data-stu-id="50445-525">Retrieves a set of the table field IDs.</span></span>

    public Set variableAccessFields(TableName tableName, [AccessRight targetAccess], [DataAreaId dataArea])

#### <a name="parameters"></a><span data-ttu-id="50445-526">パラメーター</span><span class="sxs-lookup"><span data-stu-id="50445-526">Parameters</span></span>

<span data-ttu-id="50445-527">tableName</span><span class="sxs-lookup"><span data-stu-id="50445-527">tableName</span></span>  

<!-- -->

<span data-ttu-id="50445-528">targetAccess</span><span class="sxs-lookup"><span data-stu-id="50445-528">targetAccess</span></span>  

<!-- -->

<span data-ttu-id="50445-529">dataArea</span><span class="sxs-lookup"><span data-stu-id="50445-529">dataArea</span></span>  

#### <a name="return-value"></a><span data-ttu-id="50445-530">戻り値</span><span class="sxs-lookup"><span data-stu-id="50445-530">Return Value</span></span>

<span data-ttu-id="50445-531">一連のテーブル フィールド ID。</span><span class="sxs-lookup"><span data-stu-id="50445-531">A set of the table field IDs.</span></span>

### <a name="method-webcontentaccessright"></a><span data-ttu-id="50445-532">メソッド webContentAccessRight</span><span class="sxs-lookup"><span data-stu-id="50445-532">Method webContentAccessRight</span></span>

<span data-ttu-id="50445-533">Web コンテンツ項目のアクセス権を取得します。</span><span class="sxs-lookup"><span data-stu-id="50445-533">Retrieves the access rights for the web content item.</span></span>

    public AccessRight webContentAccessRight(SecurableType type, WebContentItemName name)

#### <a name="parameters"></a><span data-ttu-id="50445-534">パラメーター</span><span class="sxs-lookup"><span data-stu-id="50445-534">Parameters</span></span>

<span data-ttu-id="50445-535">タイプ</span><span class="sxs-lookup"><span data-stu-id="50445-535">type</span></span>  

<!-- -->

<span data-ttu-id="50445-536">名前</span><span class="sxs-lookup"><span data-stu-id="50445-536">name</span></span>  

#### <a name="return-value"></a><span data-ttu-id="50445-537">戻り値</span><span class="sxs-lookup"><span data-stu-id="50445-537">Return Value</span></span>

<span data-ttu-id="50445-538">項目の AccesRight インスタンス。</span><span class="sxs-lookup"><span data-stu-id="50445-538">The AccesRight instance for the item.</span></span>

### <a name="method-construct"></a><span data-ttu-id="50445-539">メソッド construct</span><span class="sxs-lookup"><span data-stu-id="50445-539">Method construct</span></span>

<span data-ttu-id="50445-540">現在のユーザーの新しいセキュリティ権限インスタンスを作成します。</span><span class="sxs-lookup"><span data-stu-id="50445-540">Creates a new security rights instance for the current user.</span></span>

    public static SecurityRights construct()

#### <a name="return-value"></a><span data-ttu-id="50445-541">戻り値</span><span class="sxs-lookup"><span data-stu-id="50445-541">Return Value</span></span>

<span data-ttu-id="50445-542">作成された SecurityRights インスタンスです。</span><span class="sxs-lookup"><span data-stu-id="50445-542">The SecurityRights instance that was created.</span></span>

### <a name="method-newuser"></a><span data-ttu-id="50445-543">メソッド newUser</span><span class="sxs-lookup"><span data-stu-id="50445-543">Method newUser</span></span>

<span data-ttu-id="50445-544">特定のユーザーの新しいセキュリティ権限インスタンスを作成します。</span><span class="sxs-lookup"><span data-stu-id="50445-544">Creates a new security rights instance for the specified user.</span></span>

    public static SecurityRights newUser(UserId user)

#### <a name="parameters"></a><span data-ttu-id="50445-545">パラメーター</span><span class="sxs-lookup"><span data-stu-id="50445-545">Parameters</span></span>

<span data-ttu-id="50445-546">ユーザー</span><span class="sxs-lookup"><span data-stu-id="50445-546">user</span></span>  

#### <a name="return-value"></a><span data-ttu-id="50445-547">戻り値</span><span class="sxs-lookup"><span data-stu-id="50445-547">Return Value</span></span>

<span data-ttu-id="50445-548">作成された SecurityRights インスタンスです。</span><span class="sxs-lookup"><span data-stu-id="50445-548">The SecurityRights instance that was created.</span></span>

### <a name="method-new"></a><span data-ttu-id="50445-549">メソッド new</span><span class="sxs-lookup"><span data-stu-id="50445-549">Method new</span></span>

<span data-ttu-id="50445-550">SecurityRights クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="50445-550">Initializes a new instance of the SecurityRights class.</span></span>

    private void new()

### <a name="method-populateselectablecompanies"></a><span data-ttu-id="50445-551">メソッド populateSelectableCompanies</span><span class="sxs-lookup"><span data-stu-id="50445-551">Method populateSelectableCompanies</span></span>

<span data-ttu-id="50445-552">選択できる会社を取得します。</span><span class="sxs-lookup"><span data-stu-id="50445-552">Populates the selectable companies.</span></span>

    public void populateSelectableCompanies()

## <a name="class-securityskipflush"></a><span data-ttu-id="50445-553">クラス SecuritySkipFlush</span><span class="sxs-lookup"><span data-stu-id="50445-553">Class SecuritySkipFlush</span></span>
    class SecuritySkipFlush extends Object

### <a name="remarks"></a><span data-ttu-id="50445-554">備考</span><span class="sxs-lookup"><span data-stu-id="50445-554">Remarks</span></span>

### <a name="examples"></a><span data-ttu-id="50445-555">例</span><span class="sxs-lookup"><span data-stu-id="50445-555">Examples</span></span>

### <a name="methods"></a><span data-ttu-id="50445-556">メソッド</span><span class="sxs-lookup"><span data-stu-id="50445-556">Methods</span></span>

| <span data-ttu-id="50445-557">方法</span><span class="sxs-lookup"><span data-stu-id="50445-557">Method</span></span>              | <span data-ttu-id="50445-558">説明</span><span class="sxs-lookup"><span data-stu-id="50445-558">Description</span></span>                                                |
|---------------------|------------------------------------------------------------|
| <span data-ttu-id="50445-559">public void clear()</span><span class="sxs-lookup"><span data-stu-id="50445-559">public void clear()</span></span> |                                                            |
| <span data-ttu-id="50445-560">public void new()</span><span class="sxs-lookup"><span data-stu-id="50445-560">public void new()</span></span>   | <span data-ttu-id="50445-561">SecuritySkipFlush クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="50445-561">Initializes a new instance of the SecuritySkipFlush class.</span></span> |
| <span data-ttu-id="50445-562">public void set()</span><span class="sxs-lookup"><span data-stu-id="50445-562">public void set()</span></span>   |                                                            |

### <a name="method-clear"></a><span data-ttu-id="50445-563">メソッド clear</span><span class="sxs-lookup"><span data-stu-id="50445-563">Method clear</span></span>

    public void clear()

### <a name="method-new"></a><span data-ttu-id="50445-564">メソッド new</span><span class="sxs-lookup"><span data-stu-id="50445-564">Method new</span></span>

<span data-ttu-id="50445-565">SecuritySkipFlush クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="50445-565">Initializes a new instance of the SecuritySkipFlush class.</span></span>

    public void new()

### <a name="method-set"></a><span data-ttu-id="50445-566">メソッド set</span><span class="sxs-lookup"><span data-stu-id="50445-566">Method set</span></span>

    public void set()

## <a name="class-securitytablerights"></a><span data-ttu-id="50445-567">クラス SecurityTableRights</span><span class="sxs-lookup"><span data-stu-id="50445-567">Class SecurityTableRights</span></span>
    class SecurityTableRights extends Object

<span data-ttu-id="50445-568">SecurityTableRights クラスには、テーブル セキュリティ権限に関する情報が含まれます。</span><span class="sxs-lookup"><span data-stu-id="50445-568">The SecurityTableRights class holds the information about the table security rights.</span></span>

### <a name="remarks"></a><span data-ttu-id="50445-569">備考</span><span class="sxs-lookup"><span data-stu-id="50445-569">Remarks</span></span>

### <a name="examples"></a><span data-ttu-id="50445-570">例</span><span class="sxs-lookup"><span data-stu-id="50445-570">Examples</span></span>

### <a name="methods"></a><span data-ttu-id="50445-571">メソッド</span><span class="sxs-lookup"><span data-stu-id="50445-571">Methods</span></span>

| <span data-ttu-id="50445-572">方法</span><span class="sxs-lookup"><span data-stu-id="50445-572">Method</span></span>                                                   | <span data-ttu-id="50445-573">説明</span><span class="sxs-lookup"><span data-stu-id="50445-573">Description</span></span>                                               |
|----------------------------------------------------------|-----------------------------------------------------------|
| <span data-ttu-id="50445-574">public AccessRight fieldAccessRight(FieldName fieldName)</span><span class="sxs-lookup"><span data-stu-id="50445-574">public AccessRight fieldAccessRight(FieldName fieldName)</span></span> | <span data-ttu-id="50445-575">テーブルのフィールドのアクセス権を取得します。</span><span class="sxs-lookup"><span data-stu-id="50445-575">Gets the access rights for the field of the table.</span></span>        |
| <span data-ttu-id="50445-576">public AccessRight tableAccessRight()</span><span class="sxs-lookup"><span data-stu-id="50445-576">public AccessRight tableAccessRight()</span></span>                    | <span data-ttu-id="50445-577">テーブルのアクセス権を取得します。</span><span class="sxs-lookup"><span data-stu-id="50445-577">Gets the access rights for the table.</span></span>                     |
| <span data-ttu-id="50445-578">private void new()</span><span class="sxs-lookup"><span data-stu-id="50445-578">private void new()</span></span>                                       | <span data-ttu-id="50445-579">SecurityTableRights クラスのインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="50445-579">Initializes an instance of the SecurityTableRights class.</span></span> |

### <a name="method-fieldaccessright"></a><span data-ttu-id="50445-580">メソッド fieldAccessRight</span><span class="sxs-lookup"><span data-stu-id="50445-580">Method fieldAccessRight</span></span>

<span data-ttu-id="50445-581">テーブルのフィールドのアクセス権を取得します。</span><span class="sxs-lookup"><span data-stu-id="50445-581">Gets the access rights for the field of the table.</span></span>

    public AccessRight fieldAccessRight(FieldName fieldName)

#### <a name="parameters"></a><span data-ttu-id="50445-582">パラメーター</span><span class="sxs-lookup"><span data-stu-id="50445-582">Parameters</span></span>

<span data-ttu-id="50445-583">fieldName</span><span class="sxs-lookup"><span data-stu-id="50445-583">fieldName</span></span>  

#### <a name="return-value"></a><span data-ttu-id="50445-584">戻り値</span><span class="sxs-lookup"><span data-stu-id="50445-584">Return Value</span></span>

<span data-ttu-id="50445-585">フィールドの AccesRight インスタンス。</span><span class="sxs-lookup"><span data-stu-id="50445-585">The AccesRight instance for the field.</span></span>

### <a name="method-tableaccessright"></a><span data-ttu-id="50445-586">メソッド tableAccessRight</span><span class="sxs-lookup"><span data-stu-id="50445-586">Method tableAccessRight</span></span>

<span data-ttu-id="50445-587">テーブルのアクセス権を取得します。</span><span class="sxs-lookup"><span data-stu-id="50445-587">Gets the access rights for the table.</span></span>

    public AccessRight tableAccessRight()

#### <a name="return-value"></a><span data-ttu-id="50445-588">戻り値</span><span class="sxs-lookup"><span data-stu-id="50445-588">Return Value</span></span>

<span data-ttu-id="50445-589">テーブルの AccesRight インスタンス。</span><span class="sxs-lookup"><span data-stu-id="50445-589">The AccesRight instance for the table.</span></span>

### <a name="method-new"></a><span data-ttu-id="50445-590">メソッド new</span><span class="sxs-lookup"><span data-stu-id="50445-590">Method new</span></span>

<span data-ttu-id="50445-591">SecurityTableRights クラスのインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="50445-591">Initializes an instance of the SecurityTableRights class.</span></span>

    private void new()

## <a name="class-securityutil"></a><span data-ttu-id="50445-592">クラス SecurityUtil</span><span class="sxs-lookup"><span data-stu-id="50445-592">Class SecurityUtil</span></span>
    class SecurityUtil extends Object

### <a name="remarks"></a><span data-ttu-id="50445-593">備考</span><span class="sxs-lookup"><span data-stu-id="50445-593">Remarks</span></span>

### <a name="examples"></a><span data-ttu-id="50445-594">例</span><span class="sxs-lookup"><span data-stu-id="50445-594">Examples</span></span>

### <a name="methods"></a><span data-ttu-id="50445-595">方法</span><span class="sxs-lookup"><span data-stu-id="50445-595">Methods</span></span>

| <span data-ttu-id="50445-596">方法</span><span class="sxs-lookup"><span data-stu-id="50445-596">Method</span></span>                                                                                                                 | <span data-ttu-id="50445-597">説明</span><span class="sxs-lookup"><span data-stu-id="50445-597">Description</span></span>                                                                |
|------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| <span data-ttu-id="50445-598">::public static boolean isImplicitFlushMode()</span><span class="sxs-lookup"><span data-stu-id="50445-598">::public static boolean isImplicitFlushMode()</span></span>                                                                          | <span data-ttu-id="50445-599">暗黙的なセキュリティ フラッシュ モードがオンであるかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="50445-599">Indicates whether implicit security flushing mode is on.</span></span>                   |
| <span data-ttu-id="50445-600">::public static int getRoleEffectiveAccess(Int64 roleID, str secObjectName, int secObjectType, str secObjectChildName)</span><span class="sxs-lookup"><span data-stu-id="50445-600">::public static int getRoleEffectiveAccess(Int64 roleID, str secObjectName, int secObjectType, str secObjectChildName)</span></span> | <span data-ttu-id="50445-601">セキュリティ保護可能なオブジェクトのロール値の有効なアクセスを取得します。</span><span class="sxs-lookup"><span data-stu-id="50445-601">Retrieves an effective access for role value of securable object.</span></span>          |
| <span data-ttu-id="50445-602">::public static container getRolePermissions(Int64 roleID)</span><span class="sxs-lookup"><span data-stu-id="50445-602">::public static container getRolePermissions(Int64 roleID)</span></span>                                                             | <span data-ttu-id="50445-603">セキュリティ保護可能なオブジェクトのコンテナーおよび有効なアクセスを取得します。</span><span class="sxs-lookup"><span data-stu-id="50445-603">Gets a container of securable objects and their effective access.</span></span>          |
| <span data-ttu-id="50445-604">::public static boolean sysAdminMode(\[boolean active\])</span><span class="sxs-lookup"><span data-stu-id="50445-604">::public static boolean sysAdminMode(\[boolean active\])</span></span>                                                               | <span data-ttu-id="50445-605">セキュリティ管理者モードを取得および設定します。</span><span class="sxs-lookup"><span data-stu-id="50445-605">Gets and sets the security administrator mode.</span></span>                             |
| <span data-ttu-id="50445-606">::public static void refreshRolePermissions(Int64 roleID)</span><span class="sxs-lookup"><span data-stu-id="50445-606">::public static void refreshRolePermissions(Int64 roleID)</span></span>                                                              | <span data-ttu-id="50445-607">セキュリティ保護可能なオブジェクトの指定されたロールの有効なアクセスを取得します。</span><span class="sxs-lookup"><span data-stu-id="50445-607">Retrieves the effective access of a specified role for a securable object.</span></span> |
| <span data-ttu-id="50445-608">::public static void runSecondPassAutoInference()</span><span class="sxs-lookup"><span data-stu-id="50445-608">::public static void runSecondPassAutoInference()</span></span>                                                                      | <span data-ttu-id="50445-609">2 つ目の合格自動推定が実行されます。</span><span class="sxs-lookup"><span data-stu-id="50445-609">Runs the second pass auto inference.</span></span>                                       |
| <span data-ttu-id="50445-610">::public static void flushPermissions()</span><span class="sxs-lookup"><span data-stu-id="50445-610">::public static void flushPermissions()</span></span>                                                                                | <span data-ttu-id="50445-611">アクセス許可をフラッシュします。</span><span class="sxs-lookup"><span data-stu-id="50445-611">Flushes the permissions.</span></span>                                                   |
| <span data-ttu-id="50445-612">public void new()</span><span class="sxs-lookup"><span data-stu-id="50445-612">public void new()</span></span>                                                                                                      | <span data-ttu-id="50445-613">SecurityUtil クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="50445-613">Initializes a new instance of the SecurityUtil class.</span></span>                      |
| <span data-ttu-id="50445-614">::public static void flushAll()</span><span class="sxs-lookup"><span data-stu-id="50445-614">::public static void flushAll()</span></span>                                                                                        |                                                                            |

### <a name="method-isimplicitflushmode"></a><span data-ttu-id="50445-615">メソッド isImplicitFlushMode</span><span class="sxs-lookup"><span data-stu-id="50445-615">Method isImplicitFlushMode</span></span>

<span data-ttu-id="50445-616">暗黙的なセキュリティ フラッシュ モードがオンであるかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="50445-616">Indicates whether implicit security flushing mode is on.</span></span>

    public static boolean isImplicitFlushMode()

#### <a name="return-value"></a><span data-ttu-id="50445-617">戻り値</span><span class="sxs-lookup"><span data-stu-id="50445-617">Return Value</span></span>

<span data-ttu-id="50445-618">ブール値。</span><span class="sxs-lookup"><span data-stu-id="50445-618">A Boolean value.</span></span>

### <a name="method-getroleeffectiveaccess"></a><span data-ttu-id="50445-619">メソッド getRoleEffectiveAccess</span><span class="sxs-lookup"><span data-stu-id="50445-619">Method getRoleEffectiveAccess</span></span>

<span data-ttu-id="50445-620">セキュリティ保護可能なオブジェクトのロール値の有効なアクセスを取得します。</span><span class="sxs-lookup"><span data-stu-id="50445-620">Retrieves an effective access for role value of securable object.</span></span>

    public static int getRoleEffectiveAccess(Int64 roleID, str secObjectName, int secObjectType, str secObjectChildName)

#### <a name="parameters"></a><span data-ttu-id="50445-621">パラメーター</span><span class="sxs-lookup"><span data-stu-id="50445-621">Parameters</span></span>

<span data-ttu-id="50445-622">roleID</span><span class="sxs-lookup"><span data-stu-id="50445-622">roleID</span></span>  

<!-- -->

<span data-ttu-id="50445-623">secObjectName</span><span class="sxs-lookup"><span data-stu-id="50445-623">secObjectName</span></span>  

<!-- -->

<span data-ttu-id="50445-624">secObjectType</span><span class="sxs-lookup"><span data-stu-id="50445-624">secObjectType</span></span>  

<!-- -->

<span data-ttu-id="50445-625">secObjectChildName</span><span class="sxs-lookup"><span data-stu-id="50445-625">secObjectChildName</span></span>  

#### <a name="return-value"></a><span data-ttu-id="50445-626">戻り値</span><span class="sxs-lookup"><span data-stu-id="50445-626">Return Value</span></span>

<span data-ttu-id="50445-627">有効なアクセス値。</span><span class="sxs-lookup"><span data-stu-id="50445-627">The effective access value.</span></span>

### <a name="method-getrolepermissions"></a><span data-ttu-id="50445-628">メソッド getRolePermissions</span><span class="sxs-lookup"><span data-stu-id="50445-628">Method getRolePermissions</span></span>

<span data-ttu-id="50445-629">セキュリティ保護可能なオブジェクトのコンテナーおよび有効なアクセスを取得します。</span><span class="sxs-lookup"><span data-stu-id="50445-629">Gets a container of securable objects and their effective access.</span></span>

    public static container getRolePermissions(Int64 roleID)

#### <a name="parameters"></a><span data-ttu-id="50445-630">パラメーター</span><span class="sxs-lookup"><span data-stu-id="50445-630">Parameters</span></span>

<span data-ttu-id="50445-631">roleID</span><span class="sxs-lookup"><span data-stu-id="50445-631">roleID</span></span>  
<span data-ttu-id="50445-632">ロール ID。</span><span class="sxs-lookup"><span data-stu-id="50445-632">The role ID.</span></span>

#### <a name="return-value"></a><span data-ttu-id="50445-633">戻り値</span><span class="sxs-lookup"><span data-stu-id="50445-633">Return Value</span></span>

<span data-ttu-id="50445-634">セキュリティ保護可能なオブジェクトのコンテナーと、有効なアクセスです。</span><span class="sxs-lookup"><span data-stu-id="50445-634">A container of securable objects and their effective access.</span></span>

### <a name="method-sysadminmode"></a><span data-ttu-id="50445-635">メソッド sysAdminMode</span><span class="sxs-lookup"><span data-stu-id="50445-635">Method sysAdminMode</span></span>

<span data-ttu-id="50445-636">セキュリティ管理者モードを取得および設定します。</span><span class="sxs-lookup"><span data-stu-id="50445-636">Gets and sets the security administrator mode.</span></span>

    public static boolean sysAdminMode([boolean active])

#### <a name="parameters"></a><span data-ttu-id="50445-637">パラメーター</span><span class="sxs-lookup"><span data-stu-id="50445-637">Parameters</span></span>

<span data-ttu-id="50445-638">有効</span><span class="sxs-lookup"><span data-stu-id="50445-638">active</span></span>  
<span data-ttu-id="50445-639">ブール値。</span><span class="sxs-lookup"><span data-stu-id="50445-639">A Boolean value.</span></span>

#### <a name="return-value"></a><span data-ttu-id="50445-640">戻り値</span><span class="sxs-lookup"><span data-stu-id="50445-640">Return Value</span></span>

<span data-ttu-id="50445-641">セキュリティ管理者モードの古い状態。</span><span class="sxs-lookup"><span data-stu-id="50445-641">The old state of the security administrator mode.</span></span>

### <a name="method-refreshrolepermissions"></a><span data-ttu-id="50445-642">メソッド refreshRolePermissions</span><span class="sxs-lookup"><span data-stu-id="50445-642">Method refreshRolePermissions</span></span>

<span data-ttu-id="50445-643">セキュリティ保護可能なオブジェクトの指定されたロールの有効なアクセスを取得します。</span><span class="sxs-lookup"><span data-stu-id="50445-643">Retrieves the effective access of a specified role for a securable object.</span></span>

    public static void refreshRolePermissions(Int64 roleID)

#### <a name="parameters"></a><span data-ttu-id="50445-644">パラメーター</span><span class="sxs-lookup"><span data-stu-id="50445-644">Parameters</span></span>

<span data-ttu-id="50445-645">roleID</span><span class="sxs-lookup"><span data-stu-id="50445-645">roleID</span></span>  

### <a name="method-runsecondpassautoinference"></a><span data-ttu-id="50445-646">メソッド runSecondPassAutoInference</span><span class="sxs-lookup"><span data-stu-id="50445-646">Method runSecondPassAutoInference</span></span>

<span data-ttu-id="50445-647">2 つ目の合格自動推定が実行されます。</span><span class="sxs-lookup"><span data-stu-id="50445-647">Runs the second pass auto inference.</span></span>

    public static void runSecondPassAutoInference()

### <a name="method-flushpermissions"></a><span data-ttu-id="50445-648">メソッド flushPermissions</span><span class="sxs-lookup"><span data-stu-id="50445-648">Method flushPermissions</span></span>

<span data-ttu-id="50445-649">アクセス許可をフラッシュします。</span><span class="sxs-lookup"><span data-stu-id="50445-649">Flushes the permissions.</span></span>

    public static void flushPermissions()

### <a name="method-new"></a><span data-ttu-id="50445-650">メソッド new</span><span class="sxs-lookup"><span data-stu-id="50445-650">Method new</span></span>

<span data-ttu-id="50445-651">SecurityUtil クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="50445-651">Initializes a new instance of the SecurityUtil class.</span></span>

    public void new()

### <a name="method-flushall"></a><span data-ttu-id="50445-652">メソッド flushAll</span><span class="sxs-lookup"><span data-stu-id="50445-652">Method flushAll</span></span>

    public static void flushAll()

## <a name="class-segmententeredeventargs"></a><span data-ttu-id="50445-653">クラス SegmentEnteredEventArgs</span><span class="sxs-lookup"><span data-stu-id="50445-653">Class SegmentEnteredEventArgs</span></span>
    class SegmentEnteredEventArgs extends Object

### <a name="remarks"></a><span data-ttu-id="50445-654">備考</span><span class="sxs-lookup"><span data-stu-id="50445-654">Remarks</span></span>

### <a name="examples"></a><span data-ttu-id="50445-655">例</span><span class="sxs-lookup"><span data-stu-id="50445-655">Examples</span></span>

### <a name="methods"></a><span data-ttu-id="50445-656">メソッド</span><span class="sxs-lookup"><span data-stu-id="50445-656">Methods</span></span>

| <span data-ttu-id="50445-657">方法</span><span class="sxs-lookup"><span data-stu-id="50445-657">Method</span></span>                                                   | <span data-ttu-id="50445-658">説明</span><span class="sxs-lookup"><span data-stu-id="50445-658">Description</span></span> |
|----------------------------------------------------------|-------------|
| <span data-ttu-id="50445-659">public boolean isAllValuesEnabled(\[boolean enabled\])</span><span class="sxs-lookup"><span data-stu-id="50445-659">public boolean isAllValuesEnabled(\[boolean enabled\])</span></span>   |             |
| <span data-ttu-id="50445-660">public boolean isMRUEnabled(\[boolean enabled\])</span><span class="sxs-lookup"><span data-stu-id="50445-660">public boolean isMRUEnabled(\[boolean enabled\])</span></span>         |             |
| <span data-ttu-id="50445-661">public boolean isValidValuesEnabled(\[boolean enabled\])</span><span class="sxs-lookup"><span data-stu-id="50445-661">public boolean isValidValuesEnabled(\[boolean enabled\])</span></span> |             |

### <a name="method-isallvaluesenabled"></a><span data-ttu-id="50445-662">メソッド isAllValuesEnabled</span><span class="sxs-lookup"><span data-stu-id="50445-662">Method isAllValuesEnabled</span></span>

    public boolean isAllValuesEnabled([boolean enabled])

#### <a name="parameters"></a><span data-ttu-id="50445-663">パラメーター</span><span class="sxs-lookup"><span data-stu-id="50445-663">Parameters</span></span>

<span data-ttu-id="50445-664">有効</span><span class="sxs-lookup"><span data-stu-id="50445-664">enabled</span></span>  

#### <a name="return-value"></a><span data-ttu-id="50445-665">戻り値</span><span class="sxs-lookup"><span data-stu-id="50445-665">Return Value</span></span>

### <a name="method-ismruenabled"></a><span data-ttu-id="50445-666">メソッド isMRUEnabled</span><span class="sxs-lookup"><span data-stu-id="50445-666">Method isMRUEnabled</span></span>

    public boolean isMRUEnabled([boolean enabled])

#### <a name="parameters"></a><span data-ttu-id="50445-667">パラメーター</span><span class="sxs-lookup"><span data-stu-id="50445-667">Parameters</span></span>

<span data-ttu-id="50445-668">有効</span><span class="sxs-lookup"><span data-stu-id="50445-668">enabled</span></span>  

#### <a name="return-value"></a><span data-ttu-id="50445-669">戻り値</span><span class="sxs-lookup"><span data-stu-id="50445-669">Return Value</span></span>

### <a name="method-isvalidvaluesenabled"></a><span data-ttu-id="50445-670">メソッド isValidValuesEnabled</span><span class="sxs-lookup"><span data-stu-id="50445-670">Method isValidValuesEnabled</span></span>

    public boolean isValidValuesEnabled([boolean enabled])

#### <a name="parameters"></a><span data-ttu-id="50445-671">パラメーター</span><span class="sxs-lookup"><span data-stu-id="50445-671">Parameters</span></span>

<span data-ttu-id="50445-672">有効</span><span class="sxs-lookup"><span data-stu-id="50445-672">enabled</span></span>  

#### <a name="return-value"></a><span data-ttu-id="50445-673">戻り値</span><span class="sxs-lookup"><span data-stu-id="50445-673">Return Value</span></span>

## <a name="class-segmentvaluechangedeventargs"></a><span data-ttu-id="50445-674">クラス SegmentValueChangedEventArgs</span><span class="sxs-lookup"><span data-stu-id="50445-674">Class SegmentValueChangedEventArgs</span></span>
    class SegmentValueChangedEventArgs extends Object

### <a name="remarks"></a><span data-ttu-id="50445-675">備考</span><span class="sxs-lookup"><span data-stu-id="50445-675">Remarks</span></span>

### <a name="examples"></a><span data-ttu-id="50445-676">例</span><span class="sxs-lookup"><span data-stu-id="50445-676">Examples</span></span>

### <a name="methods"></a><span data-ttu-id="50445-677">メソッド</span><span class="sxs-lookup"><span data-stu-id="50445-677">Methods</span></span>

| <span data-ttu-id="50445-678">方法</span><span class="sxs-lookup"><span data-stu-id="50445-678">Method</span></span>                       | <span data-ttu-id="50445-679">説明</span><span class="sxs-lookup"><span data-stu-id="50445-679">Description</span></span> |
|------------------------------|-------------|
| <span data-ttu-id="50445-680">public FormSegment segment()</span><span class="sxs-lookup"><span data-stu-id="50445-680">public FormSegment segment()</span></span> |             |
| <span data-ttu-id="50445-681">public AnyType selectedTag()</span><span class="sxs-lookup"><span data-stu-id="50445-681">public AnyType selectedTag()</span></span> |             |

### <a name="method-segment"></a><span data-ttu-id="50445-682">メソッド segment</span><span class="sxs-lookup"><span data-stu-id="50445-682">Method segment</span></span>

    public FormSegment segment()

#### <a name="return-value"></a><span data-ttu-id="50445-683">戻り値</span><span class="sxs-lookup"><span data-stu-id="50445-683">Return Value</span></span>

### <a name="method-selectedtag"></a><span data-ttu-id="50445-684">メソッド selectedTag</span><span class="sxs-lookup"><span data-stu-id="50445-684">Method selectedTag</span></span>

    public AnyType selectedTag()

#### <a name="return-value"></a><span data-ttu-id="50445-685">戻り値</span><span class="sxs-lookup"><span data-stu-id="50445-685">Return Value</span></span>

## <a name="class-sequence"></a><span data-ttu-id="50445-686">クラスの順序</span><span class="sxs-lookup"><span data-stu-id="50445-686">Class Sequence</span></span>
    class Sequence extends Object

<span data-ttu-id="50445-687">Sequence クラスを使用すると、通常は何らかの順序または伝票番号の生成のために、主要なトランザクション スコープ外でトランザクションを実行できます。</span><span class="sxs-lookup"><span data-stu-id="50445-687">The Sequence class lets you perform transactions outside the main transaction scope, typically for some kind of sequence, or voucher number generation.</span></span>

### <a name="remarks"></a><span data-ttu-id="50445-688">備考</span><span class="sxs-lookup"><span data-stu-id="50445-688">Remarks</span></span>

<span data-ttu-id="50445-689">接続には、メインユーザー接続、補助システム接続、ユーザー接続の 3 種類があります。</span><span class="sxs-lookup"><span data-stu-id="50445-689">There are three kinds of connections: The main user connection, an auxiliary system connection, and user connections.</span></span> <span data-ttu-id="50445-690">最初のものはアプリケーション ロジック用に使用されます。</span><span class="sxs-lookup"><span data-stu-id="50445-690">The first is used for the application logic.</span></span> <span data-ttu-id="50445-691">2 番目は、内部シーケンス番号の生成 (特に組み込みフィールド RecId) に使用されます。</span><span class="sxs-lookup"><span data-stu-id="50445-691">The second is used for internal sequence number generation (specifically the built-in field RecId).</span></span> <span data-ttu-id="50445-692">3 番目はアプリケーションが別々の接続を維持するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="50445-692">The third is used for the application maintained separate connections.</span></span> <span data-ttu-id="50445-693">このクラスは、番号生成のための補助システム接続へのインターフェイスを提供します。</span><span class="sxs-lookup"><span data-stu-id="50445-693">This class provides an interface to the auxiliary system connection for number generation.</span></span> <span data-ttu-id="50445-694">ただし、これはアプリケーションの使用するメソッドまたは柔軟性、さらにカーネルの順序番号の生成で同時実行の問題を回避するため、UserConnection クラスを使用する方がより良いソリューションになる可能性があります。</span><span class="sxs-lookup"><span data-stu-id="50445-694">However, it may be a better solution to use the UserConnection class, as this is the method the application uses or flexibility, and to avoid concurrency problems with the kernel's sequence number generation.</span></span>

### <a name="examples"></a><span data-ttu-id="50445-695">例</span><span class="sxs-lookup"><span data-stu-id="50445-695">Examples</span></span>

    static void example() 
    { 
        Sequence S = new Sequence("mySequence",1,100,10000); 
        print S.nextval(10);           // 100 in current company (the subkey) 
        print S.nextval(10);           // 110 in current company (the subkey) 
        print S.nextval(1,"MMM");      // 100 in subkey "MMM" 
        print S.nextval(1,"MMM");      // 101 in subkey "MMM" 
    }

### <a name="methods"></a><span data-ttu-id="50445-696">メソッド</span><span class="sxs-lookup"><span data-stu-id="50445-696">Methods</span></span>

| <span data-ttu-id="50445-697">方法</span><span class="sxs-lookup"><span data-stu-id="50445-697">Method</span></span>                                                                                                        | <span data-ttu-id="50445-698">説明</span><span class="sxs-lookup"><span data-stu-id="50445-698">Description</span></span>                                                                                 |
|---------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="50445-699">public Int64 currval(\[str Subkey1\], \[int Subkey2\])</span><span class="sxs-lookup"><span data-stu-id="50445-699">public Int64 currval(\[str Subkey1\], \[int Subkey2\])</span></span>                                                        | <span data-ttu-id="50445-700">カウンター値の増加なしで、シーケンスから現在の順序番号を取得します。</span><span class="sxs-lookup"><span data-stu-id="50445-700">Gets the current sequence number from the sequence, without incrementing the counter value.</span></span> |
| <span data-ttu-id="50445-701">public Int64 nextval(Int64 Increment, \[str Subkey1\], \[int Subkey2\])</span><span class="sxs-lookup"><span data-stu-id="50445-701">public Int64 nextval(Int64 Increment, \[str Subkey1\], \[int Subkey2\])</span></span>                                       | <span data-ttu-id="50445-702">シーケンスから次の順序番号を返し、カウンター値を増分します。</span><span class="sxs-lookup"><span data-stu-id="50445-702">Returns the next sequence number from the sequence and then increments the counter value.</span></span>   |
| <span data-ttu-id="50445-703">public void new(str Name, int Id, Int64 InitialValue, Int64 MaxValue, \[boolean Cycle\], \[Int64 CacheSize\])</span><span class="sxs-lookup"><span data-stu-id="50445-703">public void new(str Name, int Id, Int64 InitialValue, Int64 MaxValue, \[boolean Cycle\], \[Int64 CacheSize\])</span></span> | <span data-ttu-id="50445-704">Object クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="50445-704">Initializes a new instance of the Object class.</span></span>                                             |

### <a name="method-currval"></a><span data-ttu-id="50445-705">メソッド currval</span><span class="sxs-lookup"><span data-stu-id="50445-705">Method currval</span></span>

<span data-ttu-id="50445-706">カウンター値の増加なしで、シーケンスから現在の順序番号を取得します。</span><span class="sxs-lookup"><span data-stu-id="50445-706">Gets the current sequence number from the sequence, without incrementing the counter value.</span></span>

    public Int64 currval([str Subkey1], [int Subkey2])

#### <a name="parameters"></a><span data-ttu-id="50445-707">パラメーター</span><span class="sxs-lookup"><span data-stu-id="50445-707">Parameters</span></span>

<span data-ttu-id="50445-708">Subkey1</span><span class="sxs-lookup"><span data-stu-id="50445-708">Subkey1</span></span>  

<!-- -->

<span data-ttu-id="50445-709">Subkey2</span><span class="sxs-lookup"><span data-stu-id="50445-709">Subkey2</span></span>  

#### <a name="return-value"></a><span data-ttu-id="50445-710">戻り値</span><span class="sxs-lookup"><span data-stu-id="50445-710">Return Value</span></span>

<span data-ttu-id="50445-711">シーケンスの現在のシーケンス番号。</span><span class="sxs-lookup"><span data-stu-id="50445-711">The current sequence number from the sequence.</span></span>

### <a name="method-nextval"></a><span data-ttu-id="50445-712">メソッド nextval</span><span class="sxs-lookup"><span data-stu-id="50445-712">Method nextval</span></span>

<span data-ttu-id="50445-713">シーケンスから次の順序番号を返し、カウンター値を増分します。</span><span class="sxs-lookup"><span data-stu-id="50445-713">Returns the next sequence number from the sequence and then increments the counter value.</span></span>

    public Int64 nextval(Int64 Increment, [str Subkey1], [int Subkey2])

#### <a name="parameters"></a><span data-ttu-id="50445-714">パラメーター</span><span class="sxs-lookup"><span data-stu-id="50445-714">Parameters</span></span>

<span data-ttu-id="50445-715">増分</span><span class="sxs-lookup"><span data-stu-id="50445-715">Increment</span></span>  

<!-- -->

<span data-ttu-id="50445-716">Subkey1</span><span class="sxs-lookup"><span data-stu-id="50445-716">Subkey1</span></span>  

<!-- -->

<span data-ttu-id="50445-717">Subkey2</span><span class="sxs-lookup"><span data-stu-id="50445-717">Subkey2</span></span>  

#### <a name="return-value"></a><span data-ttu-id="50445-718">戻り値</span><span class="sxs-lookup"><span data-stu-id="50445-718">Return Value</span></span>

<span data-ttu-id="50445-719">利用可能な次の順序番号。</span><span class="sxs-lookup"><span data-stu-id="50445-719">The next sequence number available.</span></span>

### <a name="method-new"></a><span data-ttu-id="50445-720">メソッド new</span><span class="sxs-lookup"><span data-stu-id="50445-720">Method new</span></span>

<span data-ttu-id="50445-721">Object クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="50445-721">Initializes a new instance of the Object class.</span></span>

    public void new(str Name, int Id, Int64 InitialValue, Int64 MaxValue, [boolean Cycle], [Int64 CacheSize])

#### <a name="parameters"></a><span data-ttu-id="50445-722">パラメーター</span><span class="sxs-lookup"><span data-stu-id="50445-722">Parameters</span></span>

<span data-ttu-id="50445-723">氏名</span><span class="sxs-lookup"><span data-stu-id="50445-723">Name</span></span>  

<!-- -->

<span data-ttu-id="50445-724">ID</span><span class="sxs-lookup"><span data-stu-id="50445-724">Id</span></span>  

<!-- -->

<span data-ttu-id="50445-725">InitialValue</span><span class="sxs-lookup"><span data-stu-id="50445-725">InitialValue</span></span>  

<!-- -->

<span data-ttu-id="50445-726">MaxValue</span><span class="sxs-lookup"><span data-stu-id="50445-726">MaxValue</span></span>  

<!-- -->

<span data-ttu-id="50445-727">サイクル</span><span class="sxs-lookup"><span data-stu-id="50445-727">Cycle</span></span>  

<!-- -->

<span data-ttu-id="50445-728">CacheSize</span><span class="sxs-lookup"><span data-stu-id="50445-728">CacheSize</span></span>  

## <a name="class-set"></a><span data-ttu-id="50445-729">クラスのセット</span><span class="sxs-lookup"><span data-stu-id="50445-729">Class Set</span></span>
    class Set extends Object

<span data-ttu-id="50445-730">Set クラスは、格納されている要素の値が固有であり、自動的に並べ替えられるデータに応じたキー値として機能するコレクションからデータを格納して取得ために使用されます。</span><span class="sxs-lookup"><span data-stu-id="50445-730">The Set class is used for the storage and retrieval of data from a collection in which the values of the elements contained are unique and serve as the key values according to which the data is automatically ordered.</span></span>

### <a name="remarks"></a><span data-ttu-id="50445-731">備考</span><span class="sxs-lookup"><span data-stu-id="50445-731">Remarks</span></span>

<span data-ttu-id="50445-732">値は任意の X++ 型にできます。</span><span class="sxs-lookup"><span data-stu-id="50445-732">The values may be of any X++ type.</span></span> <span data-ttu-id="50445-733">セット内のすべての値には同じタイプが必要です。</span><span class="sxs-lookup"><span data-stu-id="50445-733">All values in the set must have the same type.</span></span> <span data-ttu-id="50445-734">セットにすでに保存されている値が追加されると、その値は無視され、セット内の要素の数を増加させません。</span><span class="sxs-lookup"><span data-stu-id="50445-734">When a value that is already stored in the set is added, it is ignored and does not increase the number of elements in the set.</span></span> <span data-ttu-id="50445-735">セットに格納された値は、SetEnumerator 型のオブジェクトを使用してスキャンできます。</span><span class="sxs-lookup"><span data-stu-id="50445-735">The values stored in the set can be traversed by using objects of type SetEnumerator.</span></span> <span data-ttu-id="50445-736">セットのコンテンツは、要素の効率的な検索を容易にする方法で格納されます。</span><span class="sxs-lookup"><span data-stu-id="50445-736">The contents of a set are stored in a way that facilitates efficient look up of the elements.</span></span>

### <a name="examples"></a><span data-ttu-id="50445-737">例</span><span class="sxs-lookup"><span data-stu-id="50445-737">Examples</span></span>

<span data-ttu-id="50445-738">次の例では、noConfigs セットのいずれかの値が 2 番目のセットの yesConfigs セットに含まれているかどうかを確認します。</span><span class="sxs-lookup"><span data-stu-id="50445-738">The following example checks whether any of the values in one set, the noConfigs set, are found in a second set, the yesConfigs set.</span></span> <span data-ttu-id="50445-739">見つかった場合は、yesConfigs セットから削除されます。</span><span class="sxs-lookup"><span data-stu-id="50445-739">If they are, they are removed from the yesConfigs set.</span></span>

    Set             noConfigs; 
    Set             yesConfigs; 
    ConfigId        configId; 
    SetEnumerator   se; 
    ; 
    se = noConfigs.getEnumerator(); 
    while (se.moveNext()) 
    { 
        configId    = se.current(); 
        if (yesConfigs.in(configId)) 
        { 
            yesConfigs.remove(configId); 
        } 
    }

### <a name="methods"></a><span data-ttu-id="50445-740">メソッド</span><span class="sxs-lookup"><span data-stu-id="50445-740">Methods</span></span>

| <span data-ttu-id="50445-741">方法</span><span class="sxs-lookup"><span data-stu-id="50445-741">Method</span></span>                                               | <span data-ttu-id="50445-742">説明</span><span class="sxs-lookup"><span data-stu-id="50445-742">Description</span></span>                                                                                                                       |
|------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="50445-743">public boolean add(AnyType arg)</span><span class="sxs-lookup"><span data-stu-id="50445-743">public boolean add(AnyType arg)</span></span>                      | <span data-ttu-id="50445-744">セットに要素を追加します。</span><span class="sxs-lookup"><span data-stu-id="50445-744">Adds an element to the set.</span></span>                                                                                                       |
| <span data-ttu-id="50445-745">public str definitionString()</span><span class="sxs-lookup"><span data-stu-id="50445-745">public str definitionString()</span></span>                        | <span data-ttu-id="50445-746">セット内のすべての要素のタイプの説明を返します。</span><span class="sxs-lookup"><span data-stu-id="50445-746">Returns a description of the type of the elements in the set.</span></span>                                                                     |
| <span data-ttu-id="50445-747">public int elements()</span><span class="sxs-lookup"><span data-stu-id="50445-747">public int elements()</span></span>                                | <span data-ttu-id="50445-748">セット内の要素の数を返します。</span><span class="sxs-lookup"><span data-stu-id="50445-748">Returns the number of elements in the set.</span></span>                                                                                        |
| <span data-ttu-id="50445-749">public boolean empty()</span><span class="sxs-lookup"><span data-stu-id="50445-749">public boolean empty()</span></span>                               | <span data-ttu-id="50445-750">セットが空であるかどうかを判定します。</span><span class="sxs-lookup"><span data-stu-id="50445-750">Determines whether the set is empty.</span></span>                                                                                              |
| <span data-ttu-id="50445-751">public boolean equal(Set set)</span><span class="sxs-lookup"><span data-stu-id="50445-751">public boolean equal(Set set)</span></span>                        | <span data-ttu-id="50445-752">セットが現在のセットと同一かどうかを判定します。</span><span class="sxs-lookup"><span data-stu-id="50445-752">Determines whether a set is identical to the current set.</span></span>                                                                         |
| <span data-ttu-id="50445-753">public SetEnumerator getEnumerator()</span><span class="sxs-lookup"><span data-stu-id="50445-753">public SetEnumerator getEnumerator()</span></span>                 | <span data-ttu-id="50445-754">セット内のスキャンを可能にする、セットの列挙子を作成します。</span><span class="sxs-lookup"><span data-stu-id="50445-754">Creates an enumerator for a set, which allows you to traverse the set.</span></span>                                                            |
| <span data-ttu-id="50445-755">public boolean in(AnyType arg)</span><span class="sxs-lookup"><span data-stu-id="50445-755">public boolean in(AnyType arg)</span></span>                       | <span data-ttu-id="50445-756">指定された要素がセットのメンバーであるかどうかを判定します。</span><span class="sxs-lookup"><span data-stu-id="50445-756">Determines whether a specified element is a member of the set.</span></span>                                                                    |
| <span data-ttu-id="50445-757">public container pack()</span><span class="sxs-lookup"><span data-stu-id="50445-757">public container pack()</span></span>                              | <span data-ttu-id="50445-758">Set クラスの現在のインスタンスをシリアル化します。</span><span class="sxs-lookup"><span data-stu-id="50445-758">Serializes the current instance of the Set class.</span></span>                                                                                 |
| <span data-ttu-id="50445-759">public boolean remove(AnyType arg)</span><span class="sxs-lookup"><span data-stu-id="50445-759">public boolean remove(AnyType arg)</span></span>                   | <span data-ttu-id="50445-760">セットから要素を削除します。</span><span class="sxs-lookup"><span data-stu-id="50445-760">Removes an element from the set.</span></span>                                                                                                  |
| <span data-ttu-id="50445-761">public str toString()</span><span class="sxs-lookup"><span data-stu-id="50445-761">public str toString()</span></span>                                | <span data-ttu-id="50445-762">設定の内容を説明する文字列を返します。</span><span class="sxs-lookup"><span data-stu-id="50445-762">Returns a string describing the contents of the set.</span></span>                                                                              |
| <span data-ttu-id="50445-763">public Types typeId()</span><span class="sxs-lookup"><span data-stu-id="50445-763">public Types typeId()</span></span>                                | <span data-ttu-id="50445-764">セット内の値のタイプを返します。</span><span class="sxs-lookup"><span data-stu-id="50445-764">Returns the type of the values in the set.</span></span>                                                                                        |
| <span data-ttu-id="50445-765">public str xml(\[int indent\])</span><span class="sxs-lookup"><span data-stu-id="50445-765">public str xml(\[int indent\])</span></span>                       | <span data-ttu-id="50445-766">現在のオブジェクトを表す XML 文字列を返します。</span><span class="sxs-lookup"><span data-stu-id="50445-766">Returns an XML string that represents the current object.</span></span>                                                                         |
| <span data-ttu-id="50445-767">::public static Set create(container container)</span><span class="sxs-lookup"><span data-stu-id="50445-767">::public static Set create(container container)</span></span>      | <span data-ttu-id="50445-768">以前の Set.pack メソッドの呼び出しで取得したコンテナーからセットを作成します。</span><span class="sxs-lookup"><span data-stu-id="50445-768">Creates a set from the container obtained from a prior call to the Set.pack method.</span></span>                                               |
| <span data-ttu-id="50445-769">::public static Set createFromXML(Object xmlnode)</span><span class="sxs-lookup"><span data-stu-id="50445-769">::public static Set createFromXML(Object xmlnode)</span></span>    |                                                                                                                                   |
| <span data-ttu-id="50445-770">::public static Set difference(Set set1, Set set2)</span><span class="sxs-lookup"><span data-stu-id="50445-770">::public static Set difference(Set set1, Set set2)</span></span>   | <span data-ttu-id="50445-771">set2 で検出されない set1 の要素を含むセットを計算および取得します。</span><span class="sxs-lookup"><span data-stu-id="50445-771">Calculates and retrieves the set containing the elements from set1 that are not found in set2.</span></span>                                    |
| <span data-ttu-id="50445-772">::public static Set intersection(Set set1, Set set2)</span><span class="sxs-lookup"><span data-stu-id="50445-772">::public static Set intersection(Set set1, Set set2)</span></span> | <span data-ttu-id="50445-773">2 つのセット内で検出される同一の値を計算して返します。</span><span class="sxs-lookup"><span data-stu-id="50445-773">Calculates and returns the identical values found in two sets.</span></span>                                                                    |
| <span data-ttu-id="50445-774">::public static Set union(Set set1, Set set2)</span><span class="sxs-lookup"><span data-stu-id="50445-774">::public static Set union(Set set1, Set set2)</span></span>        | <span data-ttu-id="50445-775">指定された 2 つのセットの和集合を計算および取得します</span><span class="sxs-lookup"><span data-stu-id="50445-775">Calculates and retrieves the union of two given sets.</span></span> <span data-ttu-id="50445-776">これは、少なくとも 1 つのセットにある値を含むセットです。</span><span class="sxs-lookup"><span data-stu-id="50445-776">This is the set that contains the values found in at least one of the sets.</span></span> |
| <span data-ttu-id="50445-777">public void new(Types Type)</span><span class="sxs-lookup"><span data-stu-id="50445-777">public void new(Types Type)</span></span>                          | <span data-ttu-id="50445-778">指定した型の要素を含めることができるセットを作成します。</span><span class="sxs-lookup"><span data-stu-id="50445-778">Creates a set that can contain elements of the specified type.</span></span>                                                                    |

### <a name="method-add"></a><span data-ttu-id="50445-779">メソッド add</span><span class="sxs-lookup"><span data-stu-id="50445-779">Method add</span></span>

<span data-ttu-id="50445-780">セットに要素を追加します。</span><span class="sxs-lookup"><span data-stu-id="50445-780">Adds an element to the set.</span></span>

    public boolean add(AnyType arg)

#### <a name="parameters"></a><span data-ttu-id="50445-781">パラメーター</span><span class="sxs-lookup"><span data-stu-id="50445-781">Parameters</span></span>

<span data-ttu-id="50445-782">arg</span><span class="sxs-lookup"><span data-stu-id="50445-782">arg</span></span>  
<span data-ttu-id="50445-783">セットに追加する要素。</span><span class="sxs-lookup"><span data-stu-id="50445-783">The element to add to the set.</span></span>

#### <a name="return-value"></a><span data-ttu-id="50445-784">戻り値</span><span class="sxs-lookup"><span data-stu-id="50445-784">Return Value</span></span>

<span data-ttu-id="50445-785">要素がセットに追加された場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="50445-785">true if the element is added to the set; otherwise, false.</span></span>

#### <a name="remarks"></a><span data-ttu-id="50445-786">備考</span><span class="sxs-lookup"><span data-stu-id="50445-786">Remarks</span></span>

<span data-ttu-id="50445-787">セットに追加される要素は、セットの作成時にセットに割り当てられたタイプと同じタイプでなければなりません。</span><span class="sxs-lookup"><span data-stu-id="50445-787">The element added to a set must be of the same type as the type assigned to the set when it was created.</span></span> <span data-ttu-id="50445-788">既にセットに存在する場合、要素は追加されません。</span><span class="sxs-lookup"><span data-stu-id="50445-788">An element will not be added if it already exists in the set.</span></span>

#### <a name="examples"></a><span data-ttu-id="50445-789">例</span><span class="sxs-lookup"><span data-stu-id="50445-789">Examples</span></span>

<span data-ttu-id="50445-790">次の例では、セットを作成し、いくつかの整数を追加してから、セットの内容を出力します。</span><span class="sxs-lookup"><span data-stu-id="50445-790">The following example creates a set, adds some integers to it, and then prints out the contents of the set.</span></span>

    { 
        // Create a set of integers 
        Set is = new Set (Types::Integer); 
        int i; 
        ;  
        // Add values 0 to 9 to the set 
        for (i = 0; i < 10; i++) 
        { 
            is.add(i); 
        } 
        print is.toString(); 
        pause; 
    }

### <a name="method-definitionstring"></a><span data-ttu-id="50445-791">メソッド definitionString</span><span class="sxs-lookup"><span data-stu-id="50445-791">Method definitionString</span></span>

<span data-ttu-id="50445-792">セット内のすべての要素のタイプの説明を返します。</span><span class="sxs-lookup"><span data-stu-id="50445-792">Returns a description of the type of the elements in the set.</span></span>

    public str definitionString()

#### <a name="return-value"></a><span data-ttu-id="50445-793">戻り値</span><span class="sxs-lookup"><span data-stu-id="50445-793">Return Value</span></span>

<span data-ttu-id="50445-794">設定の定義を含む文字列。</span><span class="sxs-lookup"><span data-stu-id="50445-794">A string that contains a definition of the set.</span></span>

#### <a name="remarks"></a><span data-ttu-id="50445-795">備考</span><span class="sxs-lookup"><span data-stu-id="50445-795">Remarks</span></span>

<span data-ttu-id="50445-796">セット内の値の一覧を印刷するには、Set.toString を使用します。</span><span class="sxs-lookup"><span data-stu-id="50445-796">To print a list of the values within the set, use Set.toString.</span></span>

#### <a name="examples"></a><span data-ttu-id="50445-797">例</span><span class="sxs-lookup"><span data-stu-id="50445-797">Examples</span></span>

<span data-ttu-id="50445-798">次の例では、整数のセットを作成します。</span><span class="sxs-lookup"><span data-stu-id="50445-798">The following example creates a set of integers.</span></span> <span data-ttu-id="50445-799">definitionString メソッドを使用して、セットの説明を出力します。</span><span class="sxs-lookup"><span data-stu-id="50445-799">The definitionString method is used to print a description of the set.</span></span>

    { 
        // Declare a set of integers 
        Set is = new Set (Types::Integer);  
        ; 
        // Add some integers to the set 
        print is.add(1); 
        print is.add(2); 
        print is.add(1); 
        // Print a description of the set 
        print is.definitionString(); 
        // Print a description of the set elements 
        print is.toString(); 
        pause; 
    }

### <a name="method-elements"></a><span data-ttu-id="50445-800">メソッド elements</span><span class="sxs-lookup"><span data-stu-id="50445-800">Method elements</span></span>

<span data-ttu-id="50445-801">セット内の要素の数を返します。</span><span class="sxs-lookup"><span data-stu-id="50445-801">Returns the number of elements in the set.</span></span>

    public int elements()

#### <a name="return-value"></a><span data-ttu-id="50445-802">戻り値</span><span class="sxs-lookup"><span data-stu-id="50445-802">Return Value</span></span>

<span data-ttu-id="50445-803">セット内の要素の数。</span><span class="sxs-lookup"><span data-stu-id="50445-803">The number of elements in the set.</span></span>

#### <a name="examples"></a><span data-ttu-id="50445-804">例</span><span class="sxs-lookup"><span data-stu-id="50445-804">Examples</span></span>

<span data-ttu-id="50445-805">次の例では、セットの内容をコンテナーにパックします。</span><span class="sxs-lookup"><span data-stu-id="50445-805">The following example packs the contents of a set into a container.</span></span> <span data-ttu-id="50445-806">要素メソッドは、セットに任意のコンテンツが含まれているかどうかをテストするために使用されます。</span><span class="sxs-lookup"><span data-stu-id="50445-806">The elements method is used to test whether the set has any contents.</span></span> <span data-ttu-id="50445-807">コンテンツがない場合は、nullNothingnullptrunita null 参照 (Visual Basic ではなしになる) コンテナーが返されます。</span><span class="sxs-lookup"><span data-stu-id="50445-807">If there are no contents, a nullNothingnullptrunita null reference (Nothing in Visual Basic) container is returned.</span></span>

    public static container intSet2Con(Set _intSet) 
    { 
        SetEnumerator se; 
        container     intCon; 
        ; 
        if (!_intSet || !_intSet.elements()) 
        { 
            return conNull(); 
        } 
        se = _intSet.getEnumerator(); 
        while (se.moveNext()) 
        { 
            intCon += se.current(); 
        } 
        return intCon; 
    }

### <a name="method-empty"></a><span data-ttu-id="50445-808">メソッド empty</span><span class="sxs-lookup"><span data-stu-id="50445-808">Method empty</span></span>

<span data-ttu-id="50445-809">セットが空であるかどうかを判定します。</span><span class="sxs-lookup"><span data-stu-id="50445-809">Determines whether the set is empty.</span></span>

    public boolean empty()

#### <a name="return-value"></a><span data-ttu-id="50445-810">戻り値</span><span class="sxs-lookup"><span data-stu-id="50445-810">Return Value</span></span>

<span data-ttu-id="50445-811">セットが空の場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="50445-811">true if the set is empty; otherwise, false.</span></span>

#### <a name="remarks"></a><span data-ttu-id="50445-812">備考</span><span class="sxs-lookup"><span data-stu-id="50445-812">Remarks</span></span>

<span data-ttu-id="50445-813">これは、(elements() == 0) と等価です。</span><span class="sxs-lookup"><span data-stu-id="50445-813">This is equivalent to (elements() == 0).</span></span>

#### <a name="examples"></a><span data-ttu-id="50445-814">例</span><span class="sxs-lookup"><span data-stu-id="50445-814">Examples</span></span>

<span data-ttu-id="50445-815">次の例では、セットに要素があるかどうかをテストします。</span><span class="sxs-lookup"><span data-stu-id="50445-815">The following example tests whether there are any elements in a set.</span></span>

    { 
        Set mySet = new Set(Types::Integer); 
        ; 
        // ... 
        if (mySet.empty()) 
        { 
            print "There are no values in the set"; 
        } 
    }

### <a name="method-equal"></a><span data-ttu-id="50445-816">メソッド equal</span><span class="sxs-lookup"><span data-stu-id="50445-816">Method equal</span></span>

<span data-ttu-id="50445-817">セットが現在のセットと同一かどうかを判定します。</span><span class="sxs-lookup"><span data-stu-id="50445-817">Determines whether a set is identical to the current set.</span></span>

    public boolean equal(Set set)

#### <a name="parameters"></a><span data-ttu-id="50445-818">パラメーター</span><span class="sxs-lookup"><span data-stu-id="50445-818">Parameters</span></span>

<span data-ttu-id="50445-819">set</span><span class="sxs-lookup"><span data-stu-id="50445-819">set</span></span>  
<span data-ttu-id="50445-820">現在のセットと比較されるセット。</span><span class="sxs-lookup"><span data-stu-id="50445-820">The set to be compared with the current set.</span></span>

#### <a name="return-value"></a><span data-ttu-id="50445-821">戻り値</span><span class="sxs-lookup"><span data-stu-id="50445-821">Return Value</span></span>

<span data-ttu-id="50445-822">そのセットが現在のセットと同じである場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="50445-822">true if the set is the same as the current set; otherwise, false.</span></span>

#### <a name="remarks"></a><span data-ttu-id="50445-823">備考</span><span class="sxs-lookup"><span data-stu-id="50445-823">Remarks</span></span>

<span data-ttu-id="50445-824">2 つのセットが等しくなるためには、それらには同じタイプおよび同じ数の要素があり、すべての要素は同じである必要があります。</span><span class="sxs-lookup"><span data-stu-id="50445-824">For two sets to be equal, they must have the same type and the same number of elements, and all elements must be the same.</span></span>

#### <a name="examples"></a><span data-ttu-id="50445-825">例</span><span class="sxs-lookup"><span data-stu-id="50445-825">Examples</span></span>

<span data-ttu-id="50445-826">次の例では、2 つの整数セットを作成し、それらにいくつかの値を追加し、それらを比較してセットが同じかどうかを確認します。</span><span class="sxs-lookup"><span data-stu-id="50445-826">The following example creates two sets of integers, adds some values to them, and then compares them to see whether the sets are the same.</span></span>

    { 
        Set is1 = new Set (Types::Integer); 
        Set is2 = new Set (Types::Integer); 
        ; 
        is1.add(1); 
        is1.add(2); 
        is1.add(3); 
        is2.add(2); 
        is2.add(4); 
        if (is1.equal(is2)) 
        { 
            print "The sets are equal"; 
            pause; 
        } 
        else 
        { 
             print "The sets are not equal"; 
             pause; 
         } 
    }

### <a name="method-getenumerator"></a><span data-ttu-id="50445-827">メソッド getEnumerator</span><span class="sxs-lookup"><span data-stu-id="50445-827">Method getEnumerator</span></span>

<span data-ttu-id="50445-828">セット内のスキャンを可能にする、セットの列挙子を作成します。</span><span class="sxs-lookup"><span data-stu-id="50445-828">Creates an enumerator for a set, which allows you to traverse the set.</span></span>

    public SetEnumerator getEnumerator()

#### <a name="return-value"></a><span data-ttu-id="50445-829">戻り値</span><span class="sxs-lookup"><span data-stu-id="50445-829">Return Value</span></span>

<span data-ttu-id="50445-830">現在のセットの SetEnumerator オブジェクト。</span><span class="sxs-lookup"><span data-stu-id="50445-830">A SetEnumerator object for the current set.</span></span>

#### <a name="examples"></a><span data-ttu-id="50445-831">例</span><span class="sxs-lookup"><span data-stu-id="50445-831">Examples</span></span>

<span data-ttu-id="50445-832">次の例では、セットの内容をコンテナーにパックします。</span><span class="sxs-lookup"><span data-stu-id="50445-832">The following example packs the contents of a set into a container.</span></span> <span data-ttu-id="50445-833">getEnumerator メソッドは、セットの列挙子を作成するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="50445-833">The getEnumerator method is used to create an enumerator for the set.</span></span> <span data-ttu-id="50445-834">したがって、セット内の要素を横断してコンテナーに追加することができます。</span><span class="sxs-lookup"><span data-stu-id="50445-834">Therefore, that the elements in the set can be traversed and added to the container.</span></span>

    public static container intSet2Con(Set _intSet) 
    { 
        SetEnumerator se; 
        container     intCon; 
        ; 
        if (!_intSet || !_intSet.elements()) 
        { 
            return conNull(); 
        } 
        se = _intSet.getEnumerator(); 
        while (se.moveNext()) 
        { 
            intCon += se.current(); 
        } 
        return intCon; 
    }

### <a name="method-in"></a><span data-ttu-id="50445-835">メソッド in</span><span class="sxs-lookup"><span data-stu-id="50445-835">Method in</span></span>

<span data-ttu-id="50445-836">指定された要素がセットのメンバーであるかどうかを判定します。</span><span class="sxs-lookup"><span data-stu-id="50445-836">Determines whether a specified element is a member of the set.</span></span>

    public boolean in(AnyType arg)

#### <a name="parameters"></a><span data-ttu-id="50445-837">パラメーター</span><span class="sxs-lookup"><span data-stu-id="50445-837">Parameters</span></span>

<span data-ttu-id="50445-838">arg</span><span class="sxs-lookup"><span data-stu-id="50445-838">arg</span></span>  
<span data-ttu-id="50445-839">チェックする要素。</span><span class="sxs-lookup"><span data-stu-id="50445-839">The element to check.</span></span> <span data-ttu-id="50445-840">要素のタイプは、セットの指定されたタイプと同じである必要があります。</span><span class="sxs-lookup"><span data-stu-id="50445-840">The type of the element must be the same as the type that was specified for the set.</span></span>

#### <a name="return-value"></a><span data-ttu-id="50445-841">戻り値</span><span class="sxs-lookup"><span data-stu-id="50445-841">Return Value</span></span>

<span data-ttu-id="50445-842">指定した要素がセット内で見つかる場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="50445-842">true if the specified element is found in the set; otherwise, false.</span></span>

#### <a name="examples"></a><span data-ttu-id="50445-843">例</span><span class="sxs-lookup"><span data-stu-id="50445-843">Examples</span></span>

<span data-ttu-id="50445-844">次の例では、in メソッドが false を返す場合、バージョン コントロール システム内の特定の変更リストの内容を読み込みます。</span><span class="sxs-lookup"><span data-stu-id="50445-844">The following example loads the contents a particular change list in the version control system, if the in method returns false.</span></span> <span data-ttu-id="50445-845">changeSet セットには、コンテンツが既にロードされている変更リスト番号のリストが含まれています。</span><span class="sxs-lookup"><span data-stu-id="50445-845">The changeSet set contains a list of the change list numbers that already have the content loaded.</span></span>

    public void pageActivated() 
    { 
        SysVersionControlTmpItem contentsAddition; 
        if (!changeSet.in(changes.ChangeNumber)) 
        { 
            startLengthyOperation(); 
            contentsAddition = versioncontrol.getChangeNumberContents( 
                changes.ChangeNumber); 
            while select contentsAddition 
            { 
                contentsItem.data(contentsAddition); 
                contentsItem.insert(); 
            } 
            contents_ds.executeQuery(); 
            changeSet.add(changes.ChangeNumber); 
        } 
        super(); 
    }

### <a name="method-pack"></a><span data-ttu-id="50445-846">メソッド pack</span><span class="sxs-lookup"><span data-stu-id="50445-846">Method pack</span></span>

<span data-ttu-id="50445-847">Set クラスの現在のインスタンスをシリアル化します。</span><span class="sxs-lookup"><span data-stu-id="50445-847">Serializes the current instance of the Set class.</span></span>

    public container pack()

#### <a name="return-value"></a><span data-ttu-id="50445-848">戻り値</span><span class="sxs-lookup"><span data-stu-id="50445-848">Return Value</span></span>

<span data-ttu-id="50445-849">Set クラスの現在のインスタンスを含むコンテナーです。</span><span class="sxs-lookup"><span data-stu-id="50445-849">A container that contains the current instance of the Set class.</span></span>

#### <a name="remarks"></a><span data-ttu-id="50445-850">備考</span><span class="sxs-lookup"><span data-stu-id="50445-850">Remarks</span></span>

<span data-ttu-id="50445-851">このメソッドで作成されたコンテナーには、セットの最初の要素の前に 3 つの要素が含まれます。</span><span class="sxs-lookup"><span data-stu-id="50445-851">The container created by this method contains 3 elements before the first element from the set:</span></span>

-   <span data-ttu-id="50445-852">コンテナのバージョン番号</span><span class="sxs-lookup"><span data-stu-id="50445-852">A version number for the container</span></span>
-   <span data-ttu-id="50445-853">セット要素のデータ型を識別する整数</span><span class="sxs-lookup"><span data-stu-id="50445-853">An integer that identifies the data type of the set elements</span></span>
-   <span data-ttu-id="50445-854">セット内の要素の数。</span><span class="sxs-lookup"><span data-stu-id="50445-854">The number of elements in the set</span></span>

<span data-ttu-id="50445-855">キーまたは値がオブジェクトになっている場合は、各オブジェクトに対して pack メソッドが呼び出され、サブコンテナーを作成します。</span><span class="sxs-lookup"><span data-stu-id="50445-855">If the keys or the values are objects, the pack method is called on each object to create a subcontainer.</span></span> <span data-ttu-id="50445-856">Set::create method を使用することにより、結果のコンテナから新しいセットを作成することができます。</span><span class="sxs-lookup"><span data-stu-id="50445-856">You can create a new set from the resulting container by using the Set::create method.</span></span>

#### <a name="examples"></a><span data-ttu-id="50445-857">例</span><span class="sxs-lookup"><span data-stu-id="50445-857">Examples</span></span>

<span data-ttu-id="50445-858">次の例では、10 個の整数のセットを作成し、それをコンテナーにパックし、元の内容と同じ内容の新しいセットを作成します。</span><span class="sxs-lookup"><span data-stu-id="50445-858">The following example creates a set of 10 integers, packs it into a container, and then creates a new set with contents identical to the original one.</span></span>

    { 
        Set is1, is = new Set (Types::Integer); 
        int i; 
        container packedSet; 
        ; 
        // Create a set containing the first 10 integers. 
        for (i = 1; i <= 10; i++) 
        { 
            is.add(i); 
        } 
        // Pack it down in a container... 
        packedSet = is.pack(); 
        // ... and restore it 
        is1 = Set::create(packedSet); 
        print is1.toString(); 
        pause; 
    }

### <a name="method-remove"></a><span data-ttu-id="50445-859">メソッド remove</span><span class="sxs-lookup"><span data-stu-id="50445-859">Method remove</span></span>

<span data-ttu-id="50445-860">セットから要素を削除します。</span><span class="sxs-lookup"><span data-stu-id="50445-860">Removes an element from the set.</span></span>

    public boolean remove(AnyType arg)

#### <a name="parameters"></a><span data-ttu-id="50445-861">パラメーター</span><span class="sxs-lookup"><span data-stu-id="50445-861">Parameters</span></span>

<span data-ttu-id="50445-862">arg</span><span class="sxs-lookup"><span data-stu-id="50445-862">arg</span></span>  
<span data-ttu-id="50445-863">削除する要素。</span><span class="sxs-lookup"><span data-stu-id="50445-863">The element to remove.</span></span>

#### <a name="return-value"></a><span data-ttu-id="50445-864">戻り値</span><span class="sxs-lookup"><span data-stu-id="50445-864">Return Value</span></span>

<span data-ttu-id="50445-865">要素が見つかり削除された場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="50445-865">true if the element was found and removed; otherwise, false.</span></span>

#### <a name="examples"></a><span data-ttu-id="50445-866">例</span><span class="sxs-lookup"><span data-stu-id="50445-866">Examples</span></span>

<span data-ttu-id="50445-867">次の例では、noConfigs セットのいずれかの値が 2 番目のセットの yesConfigs セットに含まれているかどうかを確認します。</span><span class="sxs-lookup"><span data-stu-id="50445-867">The following example checks whether any of the values in one set, the noConfigs set, are found in a second set, the yesConfigs set.</span></span> <span data-ttu-id="50445-868">見つかった場合は、yesConfigs セットから削除されます。</span><span class="sxs-lookup"><span data-stu-id="50445-868">If they are found, they are removed from the yesConfigs set.</span></span>

    Set             noConfigs; 
    Set             yesConfigs; 
    ConfigId        configId; 
    SetEnumerator   se; 
    ; 
    se = noConfigs.getEnumerator(); 
    while (se.moveNext()) 
    { 
        configId    = se.current(); 
        if (yesConfigs.in(configId)) 
        { 
            yesConfigs.remove(configId); 
        } 
    }

### <a name="method-tostring"></a><span data-ttu-id="50445-869">メソッド toString</span><span class="sxs-lookup"><span data-stu-id="50445-869">Method toString</span></span>

<span data-ttu-id="50445-870">設定の内容を説明する文字列を返します。</span><span class="sxs-lookup"><span data-stu-id="50445-870">Returns a string describing the contents of the set.</span></span>

    public str toString()

#### <a name="return-value"></a><span data-ttu-id="50445-871">戻り値</span><span class="sxs-lookup"><span data-stu-id="50445-871">Return Value</span></span>

<span data-ttu-id="50445-872">設定の内容を説明する文字列。</span><span class="sxs-lookup"><span data-stu-id="50445-872">A string that describes the contents of the set.</span></span>

#### <a name="remarks"></a><span data-ttu-id="50445-873">備考</span><span class="sxs-lookup"><span data-stu-id="50445-873">Remarks</span></span>

<span data-ttu-id="50445-874">を使用して、セット内の単一要素の説明を取得します。</span><span class="sxs-lookup"><span data-stu-id="50445-874">Use the to get the description of a single element within a set.</span></span>

#### <a name="examples"></a><span data-ttu-id="50445-875">例</span><span class="sxs-lookup"><span data-stu-id="50445-875">Examples</span></span>

<span data-ttu-id="50445-876">次の例では、文字列のセットを作成し、そのセットの説明とセット内容の説明を出力します。</span><span class="sxs-lookup"><span data-stu-id="50445-876">The following example creates a set of strings, and then prints out a description of the set and a description of the set contents.</span></span>

    { 
        // Declare a set of strings 
        Set names = new Set (Types::String); 
        ; 
        // Add some values to the set. 
        names.add("Peter"); 
        names.add("Paul"); 
        names.add("Mary"); 
        print names.definitionString(); 
        print names.toString(); 
        pause; 
    }

### <a name="method-typeid"></a><span data-ttu-id="50445-877">メソッド typeId</span><span class="sxs-lookup"><span data-stu-id="50445-877">Method typeId</span></span>

<span data-ttu-id="50445-878">セット内の値のタイプを返します。</span><span class="sxs-lookup"><span data-stu-id="50445-878">Returns the type of the values in the set.</span></span>

    public Types typeId()

#### <a name="return-value"></a><span data-ttu-id="50445-879">戻り値</span><span class="sxs-lookup"><span data-stu-id="50445-879">Return Value</span></span>

<span data-ttu-id="50445-880">セット内の値のタイプ。</span><span class="sxs-lookup"><span data-stu-id="50445-880">The type of the values in the set.</span></span>

#### <a name="remarks"></a><span data-ttu-id="50445-881">備考</span><span class="sxs-lookup"><span data-stu-id="50445-881">Remarks</span></span>

<span data-ttu-id="50445-882">構成要素のタイプは、そのセットが作成されるときに決定される。</span><span class="sxs-lookup"><span data-stu-id="50445-882">The type of the constituent elements is determined when the set is created.</span></span>

#### <a name="examples"></a><span data-ttu-id="50445-883">例</span><span class="sxs-lookup"><span data-stu-id="50445-883">Examples</span></span>

<span data-ttu-id="50445-884">次の例では、既存のセットと同じタイプの新しいセットをインスタンス化します。</span><span class="sxs-lookup"><span data-stu-id="50445-884">The following example instantiates a new set with the same type as an existing set.</span></span>

    { 
        Set set1 = new Set(Types::Integer); 
        Set set2; 
       ; 
        set2 = new Set(set1.typeId()); 
        print set2.typeId(); 
        pause; 
    }

### <a name="method-xml"></a><span data-ttu-id="50445-885">メソッド xml</span><span class="sxs-lookup"><span data-stu-id="50445-885">Method xml</span></span>

<span data-ttu-id="50445-886">現在のオブジェクトを表す XML 文字列を返します。</span><span class="sxs-lookup"><span data-stu-id="50445-886">Returns an XML string that represents the current object.</span></span>

    public str xml([int indent])

#### <a name="parameters"></a><span data-ttu-id="50445-887">パラメーター</span><span class="sxs-lookup"><span data-stu-id="50445-887">Parameters</span></span>

<span data-ttu-id="50445-888">インデント</span><span class="sxs-lookup"><span data-stu-id="50445-888">indent</span></span>  
<span data-ttu-id="50445-889">返された XML 文字列のインデントの量 (省略可能)。</span><span class="sxs-lookup"><span data-stu-id="50445-889">The amount of indentation of the returned XML string; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="50445-890">戻り値</span><span class="sxs-lookup"><span data-stu-id="50445-890">Return Value</span></span>

<span data-ttu-id="50445-891">現在のオブジェクトを表す XML 文字列です。</span><span class="sxs-lookup"><span data-stu-id="50445-891">An XML string that represents the current object.</span></span>

#### <a name="remarks"></a><span data-ttu-id="50445-892">備考</span><span class="sxs-lookup"><span data-stu-id="50445-892">Remarks</span></span>

<span data-ttu-id="50445-893">このメソッドをオーバーライドして、その型に対して意味のある値を返すことができます。</span><span class="sxs-lookup"><span data-stu-id="50445-893">This method can be overridden to return values that are meaningful for that type.</span></span>

### <a name="method-create"></a><span data-ttu-id="50445-894">メソッド create</span><span class="sxs-lookup"><span data-stu-id="50445-894">Method create</span></span>

<span data-ttu-id="50445-895">以前の Set.pack メソッドの呼び出しで取得したコンテナーからセットを作成します。</span><span class="sxs-lookup"><span data-stu-id="50445-895">Creates a set from the container obtained from a prior call to the Set.pack method.</span></span>

    public static Set create(container container)

#### <a name="parameters"></a><span data-ttu-id="50445-896">パラメーター</span><span class="sxs-lookup"><span data-stu-id="50445-896">Parameters</span></span>

<span data-ttu-id="50445-897">コンテナー</span><span class="sxs-lookup"><span data-stu-id="50445-897">container</span></span>  
<span data-ttu-id="50445-898">パックされたセットを保持するコンテナー。</span><span class="sxs-lookup"><span data-stu-id="50445-898">The container that holds the packed set.</span></span>

#### <a name="return-value"></a><span data-ttu-id="50445-899">戻り値</span><span class="sxs-lookup"><span data-stu-id="50445-899">Return Value</span></span>

<span data-ttu-id="50445-900">コンテナーに梱包されたものと同じセット。</span><span class="sxs-lookup"><span data-stu-id="50445-900">A set equal to the one that was packed into the container.</span></span>

#### <a name="remarks"></a><span data-ttu-id="50445-901">備考</span><span class="sxs-lookup"><span data-stu-id="50445-901">Remarks</span></span>

<span data-ttu-id="50445-902">値がオブジェクトの場合、オブジェクトにはコンテナーからその内部状態を再設定するために呼び出されるアンパック メソッドが必要です。</span><span class="sxs-lookup"><span data-stu-id="50445-902">If the values are objects, the objects must have an unpack method that is called to reestablish their internal state from the container.</span></span>

#### <a name="examples"></a><span data-ttu-id="50445-903">例</span><span class="sxs-lookup"><span data-stu-id="50445-903">Examples</span></span>

<span data-ttu-id="50445-904">次の例では、セットを作成し、それをコンテナーにパックします。</span><span class="sxs-lookup"><span data-stu-id="50445-904">The following example creates a set and packs it into a container.</span></span> <span data-ttu-id="50445-905">次に、create メソッドを使用してコンテナーを展開し、元のセットと同じセットを作成します。</span><span class="sxs-lookup"><span data-stu-id="50445-905">The create method is then used to unpack the container and create a set identical to the original one.</span></span>

    { 
        Set is1, is = new Set (Types::Integer); 
        int i; 
        container packedSet; 
        ; 
        // Add 10 integers (0 - 9) to the set 
        for (i = 1; i <= 10; i++) 
        { 
            is.add(i); 
        } 
        // Pack the set into a container... 
        packedSet = is.pack(); 
        // ... and restore it 
        is1 = Set::create(packedSet); 
        print is1.toString(); 
        pause; 
    }

### <a name="method-createfromxml"></a><span data-ttu-id="50445-906">メソッド createFromXML</span><span class="sxs-lookup"><span data-stu-id="50445-906">Method createFromXML</span></span>

    public static Set createFromXML(Object xmlnode)

#### <a name="parameters"></a><span data-ttu-id="50445-907">パラメーター</span><span class="sxs-lookup"><span data-stu-id="50445-907">Parameters</span></span>

<span data-ttu-id="50445-908">xmlnode</span><span class="sxs-lookup"><span data-stu-id="50445-908">xmlnode</span></span>  

#### <a name="return-value"></a><span data-ttu-id="50445-909">戻り値</span><span class="sxs-lookup"><span data-stu-id="50445-909">Return Value</span></span>

### <a name="method-difference"></a><span data-ttu-id="50445-910">メソッド difference</span><span class="sxs-lookup"><span data-stu-id="50445-910">Method difference</span></span>

<span data-ttu-id="50445-911">set2 で検出されない set1 の要素を含むセットを計算および取得します。</span><span class="sxs-lookup"><span data-stu-id="50445-911">Calculates and retrieves the set containing the elements from set1 that are not found in set2.</span></span>

    public static Set difference(Set set1, Set set2)

#### <a name="parameters"></a><span data-ttu-id="50445-912">パラメーター</span><span class="sxs-lookup"><span data-stu-id="50445-912">Parameters</span></span>

<span data-ttu-id="50445-913">set1</span><span class="sxs-lookup"><span data-stu-id="50445-913">set1</span></span>  
<span data-ttu-id="50445-914">チェックするセット。</span><span class="sxs-lookup"><span data-stu-id="50445-914">The set to check.</span></span>

<!-- -->

<span data-ttu-id="50445-915">set2</span><span class="sxs-lookup"><span data-stu-id="50445-915">set2</span></span>  
<span data-ttu-id="50445-916">チェックするセット。</span><span class="sxs-lookup"><span data-stu-id="50445-916">The set to check.</span></span>

#### <a name="return-value"></a><span data-ttu-id="50445-917">戻り値</span><span class="sxs-lookup"><span data-stu-id="50445-917">Return Value</span></span>

<span data-ttu-id="50445-918">set2 で検出されない set1 の要素を含むセット。</span><span class="sxs-lookup"><span data-stu-id="50445-918">A set containing the elements from set1 that are not found in set2.</span></span>

#### <a name="remarks"></a><span data-ttu-id="50445-919">備考</span><span class="sxs-lookup"><span data-stu-id="50445-919">Remarks</span></span>

<span data-ttu-id="50445-920">比較される 2 つのセットは、同じタイプでなければなりません。</span><span class="sxs-lookup"><span data-stu-id="50445-920">The two sets to be compared must be of the same type.</span></span>

#### <a name="examples"></a><span data-ttu-id="50445-921">例</span><span class="sxs-lookup"><span data-stu-id="50445-921">Examples</span></span>

<span data-ttu-id="50445-922">次の例では、整数 1､2 および 3 を含む 1 つのセットと、整数 2 および 4 を含む 1 つのセットを作成します。</span><span class="sxs-lookup"><span data-stu-id="50445-922">The following example creates one set that contains the integers 1, 2, and 3, and one set that contains the integers 2 and 4.</span></span> <span data-ttu-id="50445-923">差異メソッドは、最初のセット内の 2 番目のセット (1 および 3) にない要素を含むセットを作成するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="50445-923">The difference method is used to create a set that contains the elements in the first set that are not in the second set (1 and 3).</span></span>

    { 
        Set is = new Set (Types::Integer); 
        Set is2, is1 = new Set (Types::Integer); 
        ; 
        is.add(1); 
        is.add(2); 
        is.add(3); 
        is1.add(2); 
        is1.add(4); 
        is2 = Set::difference(is, is1); 
        // prints "{1, 3}" 
        print is2.toString(); 
        pause; 
    }

### <a name="method-intersection"></a><span data-ttu-id="50445-924">メソッド intersection</span><span class="sxs-lookup"><span data-stu-id="50445-924">Method intersection</span></span>

<span data-ttu-id="50445-925">2 つのセット内で検出される同一の値を計算して返します。</span><span class="sxs-lookup"><span data-stu-id="50445-925">Calculates and returns the identical values found in two sets.</span></span>

    public static Set intersection(Set set1, Set set2)

#### <a name="parameters"></a><span data-ttu-id="50445-926">パラメーター</span><span class="sxs-lookup"><span data-stu-id="50445-926">Parameters</span></span>

<span data-ttu-id="50445-927">set1</span><span class="sxs-lookup"><span data-stu-id="50445-927">set1</span></span>  
<span data-ttu-id="50445-928">比較する 2 番目のセット。</span><span class="sxs-lookup"><span data-stu-id="50445-928">The second set to be compared.</span></span>

<!-- -->

<span data-ttu-id="50445-929">set2</span><span class="sxs-lookup"><span data-stu-id="50445-929">set2</span></span>  
<span data-ttu-id="50445-930">比較する 2 番目のセット。</span><span class="sxs-lookup"><span data-stu-id="50445-930">The second set to be compared.</span></span>

#### <a name="return-value"></a><span data-ttu-id="50445-931">戻り値</span><span class="sxs-lookup"><span data-stu-id="50445-931">Return Value</span></span>

<span data-ttu-id="50445-932">両方のセットで検出された要素を含むセット。</span><span class="sxs-lookup"><span data-stu-id="50445-932">A set containing the elements found in both sets.</span></span>

#### <a name="examples"></a><span data-ttu-id="50445-933">例</span><span class="sxs-lookup"><span data-stu-id="50445-933">Examples</span></span>

<span data-ttu-id="50445-934">次の例では、2 つの整数セットを作成し、それらにいくつかの値を追加します。</span><span class="sxs-lookup"><span data-stu-id="50445-934">The following example creates two sets of integers and adds some values to them.</span></span> <span data-ttu-id="50445-935">両方のセットに含まれている値の一覧を出力します。</span><span class="sxs-lookup"><span data-stu-id="50445-935">It then prints a list of the values that are that is contained in both sets.</span></span>

    { 
        Set is = new Set (Types::Integer); 
        Set is2, is1 = new Set (Types::Integer); 
        ; 
        is.add(1); 
        is.add(2); 
        is.add(3); 
        is1.add(2); 
        is1.add(4); 
        is2 = Set::intersection(is, is1); 
        // Prints "{2}" because 2 is contained in both is and is2. 
        print is2.toString(); 
    }

### <a name="method-union"></a><span data-ttu-id="50445-936">メソッド union</span><span class="sxs-lookup"><span data-stu-id="50445-936">Method union</span></span>

<span data-ttu-id="50445-937">指定された 2 つのセットの和集合を計算および取得します</span><span class="sxs-lookup"><span data-stu-id="50445-937">Calculates and retrieves the union of two given sets.</span></span> <span data-ttu-id="50445-938">これは、少なくとも 1 つのセットにある値を含むセットです。</span><span class="sxs-lookup"><span data-stu-id="50445-938">This is the set that contains the values found in at least one of the sets.</span></span>

    public static Set union(Set set1, Set set2)

#### <a name="parameters"></a><span data-ttu-id="50445-939">パラメーター</span><span class="sxs-lookup"><span data-stu-id="50445-939">Parameters</span></span>

<span data-ttu-id="50445-940">set1</span><span class="sxs-lookup"><span data-stu-id="50445-940">set1</span></span>  
<span data-ttu-id="50445-941">比較される 2 つのセットのうちの 2 番目のセット。</span><span class="sxs-lookup"><span data-stu-id="50445-941">The second of the two sets that are compared.</span></span>

<!-- -->

<span data-ttu-id="50445-942">set2</span><span class="sxs-lookup"><span data-stu-id="50445-942">set2</span></span>  
<span data-ttu-id="50445-943">比較される 2 つのセットのうちの 2 番目のセット。</span><span class="sxs-lookup"><span data-stu-id="50445-943">The second of the two sets that are compared.</span></span>

#### <a name="return-value"></a><span data-ttu-id="50445-944">戻り値</span><span class="sxs-lookup"><span data-stu-id="50445-944">Return Value</span></span>

<span data-ttu-id="50445-945">set1 または set2 で検出された要素を含むセット。</span><span class="sxs-lookup"><span data-stu-id="50445-945">The set containing elements found in set1 or set2.</span></span>

#### <a name="remarks"></a><span data-ttu-id="50445-946">備考</span><span class="sxs-lookup"><span data-stu-id="50445-946">Remarks</span></span>

<span data-ttu-id="50445-947">比較される 2 つのセットは、同じタイプでなければなりません。</span><span class="sxs-lookup"><span data-stu-id="50445-947">The two sets that are compared must be of the same type.</span></span>

#### <a name="examples"></a><span data-ttu-id="50445-948">例</span><span class="sxs-lookup"><span data-stu-id="50445-948">Examples</span></span>

<span data-ttu-id="50445-949">次の例では、2 つの整数セットを作成し、それらにいくつかの値を追加します。</span><span class="sxs-lookup"><span data-stu-id="50445-949">The following example creates two sets of integers and adds some values to them.</span></span> <span data-ttu-id="50445-950">セットのいずれかに含まれるすべての値を含む新しいセットを作成します。</span><span class="sxs-lookup"><span data-stu-id="50445-950">It then creates a new set that contains all the values that are contained in either of the sets.</span></span>

    { 
        Set is = new Set (Types::Integer); 
        Set is2, is1 = new Set (Types::Integer); 
        ; 
        is.add(1); 
        is.add(2); 
        is.add(3); 
        is1.add(2); 
        is1.add(4); 
        is2 = Set::union(is, is1); 
        // Prints "{1, 2, 3, 4}". 
        print is2.toString(); 
        pause; 
    }

### <a name="method-new"></a><span data-ttu-id="50445-951">メソッド new</span><span class="sxs-lookup"><span data-stu-id="50445-951">Method new</span></span>

<span data-ttu-id="50445-952">指定した型の要素を含めることができるセットを作成します。</span><span class="sxs-lookup"><span data-stu-id="50445-952">Creates a set that can contain elements of the specified type.</span></span>

    public void new(Types Type)

#### <a name="parameters"></a><span data-ttu-id="50445-953">パラメーター</span><span class="sxs-lookup"><span data-stu-id="50445-953">Parameters</span></span>

<span data-ttu-id="50445-954">種類</span><span class="sxs-lookup"><span data-stu-id="50445-954">Type</span></span>  
<span data-ttu-id="50445-955">セット内の要素のタイプ。</span><span class="sxs-lookup"><span data-stu-id="50445-955">The type of the elements within the set.</span></span>

#### <a name="remarks"></a><span data-ttu-id="50445-956">備考</span><span class="sxs-lookup"><span data-stu-id="50445-956">Remarks</span></span>

<span data-ttu-id="50445-957">セットが作成された後、セットのタイプを変更することはできません。</span><span class="sxs-lookup"><span data-stu-id="50445-957">The type of the set cannot be changed after the set has been created.</span></span>

#### <a name="examples"></a><span data-ttu-id="50445-958">例</span><span class="sxs-lookup"><span data-stu-id="50445-958">Examples</span></span>

<span data-ttu-id="50445-959">次の例では、一連の整数とオブジェクトのセットを作成します。</span><span class="sxs-lookup"><span data-stu-id="50445-959">The following example creates a set of integers and a set of objects.</span></span>

    { 
        // Create a set of integers. 
        Set is = new Set (Types::Integer); 
        // Create a set of objects. 
        Set os = new Set (Types::Class); 
    }

## <a name="class-setenumerator"></a><span data-ttu-id="50445-960">クラス SetEnumerator</span><span class="sxs-lookup"><span data-stu-id="50445-960">Class SetEnumerator</span></span>
    class SetEnumerator extends Object

<span data-ttu-id="50445-961">SetEnumerator クラスを使用すると、セット内の要素上を移動できます。</span><span class="sxs-lookup"><span data-stu-id="50445-961">The SetEnumerator class lets you traverse the elements in a set.</span></span>

### <a name="remarks"></a><span data-ttu-id="50445-962">備考</span><span class="sxs-lookup"><span data-stu-id="50445-962">Remarks</span></span>

<span data-ttu-id="50445-963">セット列挙子は、セットの最初の要素の前に開始します。</span><span class="sxs-lookup"><span data-stu-id="50445-963">Set enumerators start before the first element in the set.</span></span> <span data-ttu-id="50445-964">セットの最初の要素を指すようにするために SetEnumerator.moveNext メソッドを呼び出す必要があります。</span><span class="sxs-lookup"><span data-stu-id="50445-964">You must call the SetEnumerator.moveNext method to make it point to the first element in the set.</span></span> <span data-ttu-id="50445-965">ベスト プラクティスとしては、set.getEnumerator メソッドが呼び出されたときに、設定されている同じ層で列挙子が自動的に作成されるため、SetIterator クラスではなく、SetEnumerator クラスを使用します。</span><span class="sxs-lookup"><span data-stu-id="50445-965">As a best practice, use the SetEnumerator class instead of the SetIterator class, because enumerators are automatically created on the same tier as the set when the set.getEnumerator method is called.</span></span> <span data-ttu-id="50445-966">これにより、Caller from としてマークされたコードの潜在的な問題を回避できます。反復子とセットは別々の層に置くことができます。</span><span class="sxs-lookup"><span data-stu-id="50445-966">This helps you avoid a potential problem in code that is marked as Called from, where the iterator and set can be on separate tiers.</span></span> <span data-ttu-id="50445-967">さらに、セット列挙子はセット反復子よりも少ないコードを必要とするためパフォーマンスが少し向上します。</span><span class="sxs-lookup"><span data-stu-id="50445-967">In addition, set enumerators require less code than set iterators and therefore perform slightly better.</span></span>

### <a name="examples"></a><span data-ttu-id="50445-968">例</span><span class="sxs-lookup"><span data-stu-id="50445-968">Examples</span></span>

### <a name="methods"></a><span data-ttu-id="50445-969">メソッド</span><span class="sxs-lookup"><span data-stu-id="50445-969">Methods</span></span>

| <span data-ttu-id="50445-970">方法</span><span class="sxs-lookup"><span data-stu-id="50445-970">Method</span></span>                        | <span data-ttu-id="50445-971">説明</span><span class="sxs-lookup"><span data-stu-id="50445-971">Description</span></span>                                                                                                |
|-------------------------------|------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="50445-972">public AnyType current()</span><span class="sxs-lookup"><span data-stu-id="50445-972">public AnyType current()</span></span>      | <span data-ttu-id="50445-973">列挙子によりポイントされている値を取得します。</span><span class="sxs-lookup"><span data-stu-id="50445-973">Retrieves the value that is pointed to by the enumerator.</span></span>                                                  |
| <span data-ttu-id="50445-974">public str definitionString()</span><span class="sxs-lookup"><span data-stu-id="50445-974">public str definitionString()</span></span> | <span data-ttu-id="50445-975">列挙子の説明を返します。</span><span class="sxs-lookup"><span data-stu-id="50445-975">Returns a description of the enumerator.</span></span>                                                                   |
| <span data-ttu-id="50445-976">public boolean moveNext()</span><span class="sxs-lookup"><span data-stu-id="50445-976">public boolean moveNext()</span></span>     | <span data-ttu-id="50445-977">列挙子が有効なセット要素を示すかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="50445-977">Determines whether the enumerator denotes a valid set element.</span></span>                                             |
| <span data-ttu-id="50445-978">public str toString()</span><span class="sxs-lookup"><span data-stu-id="50445-978">public str toString()</span></span>         | <span data-ttu-id="50445-979">列挙子が現在ポイントしているセット内の要素の内容の説明を取得します。</span><span class="sxs-lookup"><span data-stu-id="50445-979">Retrieves a description of the contents of the element in the set that the enumerator currently points to.</span></span> |
| <span data-ttu-id="50445-980">public void reset()</span><span class="sxs-lookup"><span data-stu-id="50445-980">public void reset()</span></span>           | <span data-ttu-id="50445-981">列挙子をセットの先頭に移動します。</span><span class="sxs-lookup"><span data-stu-id="50445-981">Moves the enumerator to the start of the set.</span></span>                                                              |

### <a name="method-current"></a><span data-ttu-id="50445-982">メソッド current</span><span class="sxs-lookup"><span data-stu-id="50445-982">Method current</span></span>

<span data-ttu-id="50445-983">列挙子によりポイントされている値を取得します。</span><span class="sxs-lookup"><span data-stu-id="50445-983">Retrieves the value that is pointed to by the enumerator.</span></span>

    public AnyType current()

#### <a name="return-value"></a><span data-ttu-id="50445-984">戻り値</span><span class="sxs-lookup"><span data-stu-id="50445-984">Return Value</span></span>

<span data-ttu-id="50445-985">セット内で現在指定されている値。</span><span class="sxs-lookup"><span data-stu-id="50445-985">The value that is currently pointed to in the set.</span></span>

#### <a name="remarks"></a><span data-ttu-id="50445-986">備考</span><span class="sxs-lookup"><span data-stu-id="50445-986">Remarks</span></span>

<span data-ttu-id="50445-987">戻り値のタイプは、セット内の項目のタイプによって決まります。</span><span class="sxs-lookup"><span data-stu-id="50445-987">The type of the return value is determined by the type of items in the set.</span></span> <span data-ttu-id="50445-988">現在のメソッドを呼び出す前に、SetEnumerator.moveNext メソッドを呼び出す必要があります。</span><span class="sxs-lookup"><span data-stu-id="50445-988">You must call the SetEnumerator.moveNext method before you call the current method.</span></span>

### <a name="method-definitionstring"></a><span data-ttu-id="50445-989">メソッド definitionString</span><span class="sxs-lookup"><span data-stu-id="50445-989">Method definitionString</span></span>

<span data-ttu-id="50445-990">列挙子の説明を返します。</span><span class="sxs-lookup"><span data-stu-id="50445-990">Returns a description of the enumerator.</span></span>

    public str definitionString()

#### <a name="return-value"></a><span data-ttu-id="50445-991">戻り値</span><span class="sxs-lookup"><span data-stu-id="50445-991">Return Value</span></span>

<span data-ttu-id="50445-992">列挙子の説明を含む文字列。</span><span class="sxs-lookup"><span data-stu-id="50445-992">A string that contains a description of the enumerator.</span></span>

#### <a name="remarks"></a><span data-ttu-id="50445-993">備考</span><span class="sxs-lookup"><span data-stu-id="50445-993">Remarks</span></span>

<span data-ttu-id="50445-994">たとえば、整数のセットの列挙子は、int セット列挙子を返します。</span><span class="sxs-lookup"><span data-stu-id="50445-994">For example, an enumerator for a set of integers would return "int set enumerator".</span></span>

#### <a name="examples"></a><span data-ttu-id="50445-995">例</span><span class="sxs-lookup"><span data-stu-id="50445-995">Examples</span></span>

<span data-ttu-id="50445-996">次の例では、セットとそのセットの列挙子を作成します。</span><span class="sxs-lookup"><span data-stu-id="50445-996">The following example creates a set and an enumerator for the set.</span></span> <span data-ttu-id="50445-997">definitionString メソッドを使用して、列挙子の説明を出力します。</span><span class="sxs-lookup"><span data-stu-id="50445-997">The definitionString method is used to print a description of the enumerator.</span></span>

    { 
        Set mySet = new Set(Types::Integer); 
        SetEnumerator enumerator; 
        int i; 
        // Add some elements to the set. 
       for (i = 0; i < 10; i++) 
        { 
            mySet.add(i); 
        } 
        // Set the enumerator. 
        enumerator = mySet.getEnumerator(); 
        print enumerator.definitionString(); 
        pause; 
    }

### <a name="method-movenext"></a><span data-ttu-id="50445-998">メソッド moveNext</span><span class="sxs-lookup"><span data-stu-id="50445-998">Method moveNext</span></span>

<span data-ttu-id="50445-999">列挙子が有効なセット要素を示すかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="50445-999">Determines whether the enumerator denotes a valid set element.</span></span>

    public boolean moveNext()

#### <a name="return-value"></a><span data-ttu-id="50445-1000">戻り値</span><span class="sxs-lookup"><span data-stu-id="50445-1000">Return Value</span></span>

<span data-ttu-id="50445-1001">セット内の現在の職位が有効な要素を保持している場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="50445-1001">true if the current position in the set holds a valid element; otherwise, false.</span></span>

#### <a name="remarks"></a><span data-ttu-id="50445-1002">備考</span><span class="sxs-lookup"><span data-stu-id="50445-1002">Remarks</span></span>

<span data-ttu-id="50445-1003">セット列挙子は、セットの最初の要素の前に開始します。</span><span class="sxs-lookup"><span data-stu-id="50445-1003">Set enumerators start before the first element in the set.</span></span> <span data-ttu-id="50445-1004">セットの最初の要素を指すようにするために moveNext メソッドを呼び出す必要があります。</span><span class="sxs-lookup"><span data-stu-id="50445-1004">You must call the moveNext method to make it point to the first element in the set.</span></span>

### <a name="method-tostring"></a><span data-ttu-id="50445-1005">メソッド toString</span><span class="sxs-lookup"><span data-stu-id="50445-1005">Method toString</span></span>

<span data-ttu-id="50445-1006">列挙子が現在ポイントしているセット内の要素の内容の説明を取得します。</span><span class="sxs-lookup"><span data-stu-id="50445-1006">Retrieves a description of the contents of the element in the set that the enumerator currently points to.</span></span>

    public str toString()

#### <a name="return-value"></a><span data-ttu-id="50445-1007">戻り値</span><span class="sxs-lookup"><span data-stu-id="50445-1007">Return Value</span></span>

<span data-ttu-id="50445-1008">設定の現在の要素の説明を含む文字列。</span><span class="sxs-lookup"><span data-stu-id="50445-1008">A string that contains a description of the current element in the set.</span></span>

#### <a name="examples"></a><span data-ttu-id="50445-1009">例</span><span class="sxs-lookup"><span data-stu-id="50445-1009">Examples</span></span>

<span data-ttu-id="50445-1010">次の例では、整数のセットを作成し、最初の要素と 2 番目の要素の内容をセットに出力します。</span><span class="sxs-lookup"><span data-stu-id="50445-1010">The following example creates a set of integers, and then prints the content of the first and second elements in the set.</span></span>

    { 
        Set mySet = new Set(Types::Integer); 
        SetEnumerator  enumerator; 
        int i; 
         // Add some elements to the set. 
        for (i = 0; i < 10; i++) 
        { 
            mySet.add(i); 
        } 
        // Set the enumerator. 
        enumerator = mySet.getEnumerator(); 
        // Go to the beginning of the enumerator. 
        enumerator.reset(); 
        // Go to the first element in the set. 
        enumerator.moveNext(); 
        // Print the first item in the set. 
        print enumerator.toString(); 
        pause; 
        enumerator.moveNext(); 
        // Print the second element in the set. 
        print enumerator.toString(); 
        pause; 
    }

### <a name="method-reset"></a><span data-ttu-id="50445-1011">メソッド reset</span><span class="sxs-lookup"><span data-stu-id="50445-1011">Method reset</span></span>

<span data-ttu-id="50445-1012">列挙子をセットの先頭に移動します。</span><span class="sxs-lookup"><span data-stu-id="50445-1012">Moves the enumerator to the start of the set.</span></span>

    public void reset()

#### <a name="remarks"></a><span data-ttu-id="50445-1013">備考</span><span class="sxs-lookup"><span data-stu-id="50445-1013">Remarks</span></span>

<span data-ttu-id="50445-1014">reset メソッドは、列挙子をセットの先頭、セットの最初の要素の前に移動します。</span><span class="sxs-lookup"><span data-stu-id="50445-1014">The reset method moves the enumerator to the start of the set, in front of the first element in the set.</span></span> <span data-ttu-id="50445-1015">セットの最初の要素を指すようにするために SetEnumerator.moveNext メソッドを呼び出す必要があります。</span><span class="sxs-lookup"><span data-stu-id="50445-1015">You must call the SetEnumerator.moveNext method to make it point to the first element in the set.</span></span>

#### <a name="examples"></a><span data-ttu-id="50445-1016">例</span><span class="sxs-lookup"><span data-stu-id="50445-1016">Examples</span></span>

<span data-ttu-id="50445-1017">次の例では、セット作成し、そのセットの列挙子を作成します。</span><span class="sxs-lookup"><span data-stu-id="50445-1017">The following example creates a set and then creates an enumerator for the set.</span></span> <span data-ttu-id="50445-1018">reset メソッドを使用してセットの先頭に移動し、moveNext メソッドを使用してセットの最初の要素に移動します。</span><span class="sxs-lookup"><span data-stu-id="50445-1018">It uses the reset method to move to the start of the set and then uses the moveNext method to move to the first element in the set.</span></span>

    { 
        Set mySet = new Set(Types::Integer); 
        SetEnumerator  enumerator; 
        int i; 
         // Add some elements to the set. 
        for (i = 0; i < 10; i++) 
        { 
            mySet.add(i); 
        } 
        // Set the enumerator. 
        enumerator = mySet.getEnumerator(); 
        // Go to beginning of enumerator. 
        enumerator.reset(); 
        // Go to the first element in the set. 
        enumerator.moveNext(); 
        // Print the first item in the set. 
        print enumerator.toString(); 
        pause; 
    }

## <a name="class-setiterator"></a><span data-ttu-id="50445-1019">クラス SetIterator</span><span class="sxs-lookup"><span data-stu-id="50445-1019">Class SetIterator</span></span>
    class SetIterator extends Object

<span data-ttu-id="50445-1020">SetIterator クラスを使用すると、セット内の要素を反復処理できます。</span><span class="sxs-lookup"><span data-stu-id="50445-1020">The SetIterator class allows you to iterate over the elements in a set.</span></span>

### <a name="remarks"></a><span data-ttu-id="50445-1021">備考</span><span class="sxs-lookup"><span data-stu-id="50445-1021">Remarks</span></span>

<span data-ttu-id="50445-1022">セットの反復子は、反復処理する対象となるセットにポインターとして表示することができます。</span><span class="sxs-lookup"><span data-stu-id="50445-1022">Set iterators may be viewed as pointers into the sets over which they iterate.</span></span> <span data-ttu-id="50445-1023">繰り返しを開始し、より多くの要素が利用可能であるかどうかを決定し、さらに繰り返しによりポイントされる要素をフェッチする機能が利用可能です。</span><span class="sxs-lookup"><span data-stu-id="50445-1023">Functionality is available to start the iteration, to determine whether more elements are available, and to fetch the element pointed to by the iterator.</span></span> <span data-ttu-id="50445-1024">新しく作成されるセット反復子は、セットの最初の要素に配置されます。</span><span class="sxs-lookup"><span data-stu-id="50445-1024">Newly created set iterators are positioned at the first element in the set.</span></span> <span data-ttu-id="50445-1025">繰り返し中に要素が出現する順序は、要素が挿入される順序ではなく、要素の順序によって定義されます。</span><span class="sxs-lookup"><span data-stu-id="50445-1025">The order in which the elements occur during iteration is defined not by the sequence in which the elements are inserted, but by the ordering of the elements.</span></span> <span data-ttu-id="50445-1026">より下位の値の要素は、上位の値の要素の前に表示されます。</span><span class="sxs-lookup"><span data-stu-id="50445-1026">Elements with lower values appear before elements with higher values.</span></span> <span data-ttu-id="50445-1027">型の通常の順序が使用されます。</span><span class="sxs-lookup"><span data-stu-id="50445-1027">The usual ordering for the types is used.</span></span> <span data-ttu-id="50445-1028">構成要素がオブジェクトである場合、順序を指定するのにオブジェクトのアドレスが使用されます。</span><span class="sxs-lookup"><span data-stu-id="50445-1028">If the constituent elements are objects; however, the addresses of the objects are used to supply the ordering.</span></span> <span data-ttu-id="50445-1029">特定の注文が推測される可能性はありません。</span><span class="sxs-lookup"><span data-stu-id="50445-1029">No specific ordering may consequently be inferred.</span></span> <span data-ttu-id="50445-1030">オブジェクトのアドレスは、本来、一時的です。</span><span class="sxs-lookup"><span data-stu-id="50445-1030">The addresses of the objects are transient by nature.</span></span> <span data-ttu-id="50445-1031">SetIterator クラスではなく、そのクラスを使用することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="50445-1031">It is best practice to use the class instead of the SetIterator class.</span></span> <span data-ttu-id="50445-1032">これにより、別の層の反復子を使用して 1 つの層のセットにアクセスする場合に問題を回避できます。</span><span class="sxs-lookup"><span data-stu-id="50445-1032">This avoids problems if you are accessing the set on one tier with an iterator on another tier.</span></span> <span data-ttu-id="50445-1033">セット反復子および反復処理するセットは、同じクライアント/サーバー側にある必要があります。</span><span class="sxs-lookup"><span data-stu-id="50445-1033">Set iterators and the sets over which they iterate must be on the same client/server side.</span></span> <span data-ttu-id="50445-1034">SetIterator を使用し、コードが Called from としてマークされている場合、セットと反復子が別の層で終了しており、コードが失敗する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="50445-1034">If you use SetIterator and code is marked as Called from, it is possible that the set and the iterator will end up on different tiers, and the code will fail.</span></span> <span data-ttu-id="50445-1035">SetEnumerator を使用する場合、列挙子はセットと同じ層に自動的に作成されます。</span><span class="sxs-lookup"><span data-stu-id="50445-1035">If you use SetEnumerator, the enumerator is automatically created on the same tier as the set.</span></span> <span data-ttu-id="50445-1036">また、セット内の次のアイテムに移動するには、反復子セットを使用している場合は、より多くのメソッドと次のメソッドを明示的に呼び出す必要があります。</span><span class="sxs-lookup"><span data-stu-id="50445-1036">Also, to move to the next item in a set, you must explicitly call the more and next methods if you are using a set iterator.</span></span> <span data-ttu-id="50445-1037">SetEnumerator を使用する場合、moveNext メソッドを呼び出すだけです。</span><span class="sxs-lookup"><span data-stu-id="50445-1037">If you use SetEnumerator, you only have to call moveNext method.</span></span>

### <a name="examples"></a><span data-ttu-id="50445-1038">例</span><span class="sxs-lookup"><span data-stu-id="50445-1038">Examples</span></span>

<span data-ttu-id="50445-1039">次の例では、整数のセットを作成し、4 つの値をその中に追加します。</span><span class="sxs-lookup"><span data-stu-id="50445-1039">The following example creates a set of integers and then adds four values to it.</span></span> <span data-ttu-id="50445-1040">各セット要素に関する情報を出力しているセットを通じて反復処理します。</span><span class="sxs-lookup"><span data-stu-id="50445-1040">It then iterates through the set that is printing out information about each set element.</span></span>

        Set s1 = new Set (Types::Integer); 
        int theElement; 
        SetIterator it; 
        ; 
        // Add some elements. 
        s1.add(3); 
        s1.add(4); 
        s1.add(13); 
        s1.add(1); 
        // Start a traversal of the elements in the set. 
        it = new SetIterator(s1); 
        // Prints "(begin)[1]". 
        print it.toString(); 
        // The elements are fetched in the order: 1, 3, 4, 13. 
        while (it.more()) 
        { 
            theElement = it.value(); 
            print theElement; 
             // Fetch the next element. 
            it.next(); 
        } 
        pause; 
    }

### <a name="methods"></a><span data-ttu-id="50445-1041">メソッド</span><span class="sxs-lookup"><span data-stu-id="50445-1041">Methods</span></span>

| <span data-ttu-id="50445-1042">方法</span><span class="sxs-lookup"><span data-stu-id="50445-1042">Method</span></span>                        | <span data-ttu-id="50445-1043">説明</span><span class="sxs-lookup"><span data-stu-id="50445-1043">Description</span></span>                                                                                            |
|-------------------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="50445-1044">public str definitionString()</span><span class="sxs-lookup"><span data-stu-id="50445-1044">public str definitionString()</span></span> | <span data-ttu-id="50445-1045">反復子のタイプのテキスト表現を返します。</span><span class="sxs-lookup"><span data-stu-id="50445-1045">Returns a textual representation of the type of the iterator.</span></span>                                          |
| <span data-ttu-id="50445-1046">public boolean more()</span><span class="sxs-lookup"><span data-stu-id="50445-1046">public boolean more()</span></span>         | <span data-ttu-id="50445-1047">反復子が有効なセット要素を示すかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="50445-1047">Determines whether the iterator denotes a valid set element.</span></span>                                           |
| <span data-ttu-id="50445-1048">public str toString()</span><span class="sxs-lookup"><span data-stu-id="50445-1048">public str toString()</span></span>         | <span data-ttu-id="50445-1049">反復子によりポイントされているセット内の現在の要素のテキスト形式を返します。</span><span class="sxs-lookup"><span data-stu-id="50445-1049">Returns a textual representation of the current element in the set that is pointed to by the iterator.</span></span> |
| <span data-ttu-id="50445-1050">public AnyType value()</span><span class="sxs-lookup"><span data-stu-id="50445-1050">public AnyType value()</span></span>        | <span data-ttu-id="50445-1051">反復子がポイントしている値を取得します。</span><span class="sxs-lookup"><span data-stu-id="50445-1051">Retrieves the value that the iterator is pointing to.</span></span>                                                  |
| <span data-ttu-id="50445-1052">public void next()</span><span class="sxs-lookup"><span data-stu-id="50445-1052">public void next()</span></span>            | <span data-ttu-id="50445-1053">次の要素に反復子を移動します。</span><span class="sxs-lookup"><span data-stu-id="50445-1053">Moves the iterator to the next element.</span></span>                                                                |
| <span data-ttu-id="50445-1054">public void new(Set set)</span><span class="sxs-lookup"><span data-stu-id="50445-1054">public void new(Set set)</span></span>      | <span data-ttu-id="50445-1055">セットに対する新しい反復子を作成します。</span><span class="sxs-lookup"><span data-stu-id="50445-1055">Creates a new iterator for a set.</span></span>                                                                      |
| <span data-ttu-id="50445-1056">public void begin()</span><span class="sxs-lookup"><span data-stu-id="50445-1056">public void begin()</span></span>           | <span data-ttu-id="50445-1057">反復子をセットの先頭に移動します。</span><span class="sxs-lookup"><span data-stu-id="50445-1057">Moves the iterator to the start of the set.</span></span>                                                            |
| <span data-ttu-id="50445-1058">public void delete()</span><span class="sxs-lookup"><span data-stu-id="50445-1058">public void delete()</span></span>          | <span data-ttu-id="50445-1059">セットの反復子によってポイントされている要素を削除します。</span><span class="sxs-lookup"><span data-stu-id="50445-1059">Removes the element that is pointed to by the iterator of the set.</span></span>                                     |
| <span data-ttu-id="50445-1060">public void end()</span><span class="sxs-lookup"><span data-stu-id="50445-1060">public void end()</span></span>             | <span data-ttu-id="50445-1061">セットで最後の要素の後に反復子を移動します。</span><span class="sxs-lookup"><span data-stu-id="50445-1061">Moves the iterator past the last element in the set.</span></span>                                                   |

### <a name="method-definitionstring"></a><span data-ttu-id="50445-1062">メソッド definitionString</span><span class="sxs-lookup"><span data-stu-id="50445-1062">Method definitionString</span></span>

<span data-ttu-id="50445-1063">反復子のタイプのテキスト表現を返します。</span><span class="sxs-lookup"><span data-stu-id="50445-1063">Returns a textual representation of the type of the iterator.</span></span>

    public str definitionString()

#### <a name="return-value"></a><span data-ttu-id="50445-1064">戻り値</span><span class="sxs-lookup"><span data-stu-id="50445-1064">Return Value</span></span>

<span data-ttu-id="50445-1065">反復子のタイプを示す文字列。</span><span class="sxs-lookup"><span data-stu-id="50445-1065">A string that indicates the type of the iterator.</span></span>

### <a name="method-more"></a><span data-ttu-id="50445-1066">メソッド more</span><span class="sxs-lookup"><span data-stu-id="50445-1066">Method more</span></span>

<span data-ttu-id="50445-1067">反復子が有効なセット要素を示すかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="50445-1067">Determines whether the iterator denotes a valid set element.</span></span>

    public boolean more()

#### <a name="return-value"></a><span data-ttu-id="50445-1068">戻り値</span><span class="sxs-lookup"><span data-stu-id="50445-1068">Return Value</span></span>

<span data-ttu-id="50445-1069">反復子が有効な要素を表す場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="50445-1069">true if the iterator denotes a valid element; otherwise, false.</span></span>

#### <a name="remarks"></a><span data-ttu-id="50445-1070">備考</span><span class="sxs-lookup"><span data-stu-id="50445-1070">Remarks</span></span>

<span data-ttu-id="50445-1071">このメソッドが false を返すときに反復子が指す要素にアクセスしようとするとエラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="50445-1071">Attempting to access an element that is pointed to by an iterator when this method returns false will result in an error.</span></span> <span data-ttu-id="50445-1072">このメソッドは、反復子が有効な要素を指しているかどうかだけをチェックします。</span><span class="sxs-lookup"><span data-stu-id="50445-1072">This method will check only whether the iterator points to a valid element.</span></span> <span data-ttu-id="50445-1073">セットにより多くの要素があるかどうかは確認されません。</span><span class="sxs-lookup"><span data-stu-id="50445-1073">It will not check whether there are more elements in the set.</span></span>

#### <a name="examples"></a><span data-ttu-id="50445-1074">例</span><span class="sxs-lookup"><span data-stu-id="50445-1074">Examples</span></span>

<span data-ttu-id="50445-1075">次の例では、SetIterator.more メソッドを使用して、while ループを実行する前にセット内に要素があるかどうかを確認します。これにより、奇数要素がすべてセットから削除されます。</span><span class="sxs-lookup"><span data-stu-id="50445-1075">The following example uses the SetIterator.more method to check whether there are more elements in the set before it runs through the while loop, which deletes all the odd elements from the set.</span></span>

    { 
        Set iset = new Set (Types::Integer); 
        SetIterator it; 
        int i; 
        ; 
        for (i = 1; i <= 10; i++) 
        { 
            iset.add(i); 
        } 
        // Delete all odd elements 
        it = new SetIterator(iset); 
        while (it.more()) 
        { 
            if (it.value() mod 2 != 0) 
            { 
                // The value is odd. Delete and skip to next element. 
                it.delete(); 
            } 
            else 
            { 
                it.next(); 
            } 
        } 
        print iset.toString(); 
        pause; 
    }

### <a name="method-tostring"></a><span data-ttu-id="50445-1076">メソッド toString</span><span class="sxs-lookup"><span data-stu-id="50445-1076">Method toString</span></span>

<span data-ttu-id="50445-1077">反復子によりポイントされているセット内の現在の要素のテキスト形式を返します。</span><span class="sxs-lookup"><span data-stu-id="50445-1077">Returns a textual representation of the current element in the set that is pointed to by the iterator.</span></span>

    public str toString()

#### <a name="return-value"></a><span data-ttu-id="50445-1078">戻り値</span><span class="sxs-lookup"><span data-stu-id="50445-1078">Return Value</span></span>

<span data-ttu-id="50445-1079">設定の現在の要素のテキスト形式表記である文字列。</span><span class="sxs-lookup"><span data-stu-id="50445-1079">A string that is the textual representation of the current element in the set.</span></span>

#### <a name="remarks"></a><span data-ttu-id="50445-1080">備考</span><span class="sxs-lookup"><span data-stu-id="50445-1080">Remarks</span></span>

<span data-ttu-id="50445-1081">反復子がセット内の最初の要素を指している場合、その文字列には "(開始)\[値\]" という形式の指示が含まれます。反復子が要素を指していない場合(つまり、more() が false を返す場合)、返される文字列は "(終了)" になります。反復子が値を指す場合、文字列は "\[値\]" になります。値は要素値の文字列表現です。</span><span class="sxs-lookup"><span data-stu-id="50445-1081">If the iterator points to the first element in the set, the string will contain an indication of this, in the following format: "(begin)\[value\]" If the iterator does not point to an element (that is, if more() returns false), the string returned is: "(end)" If the iterator points to a value the string is: "\[value\]" where value is a string representation of the element value.</span></span>

#### <a name="examples"></a><span data-ttu-id="50445-1082">例</span><span class="sxs-lookup"><span data-stu-id="50445-1082">Examples</span></span>

<span data-ttu-id="50445-1083">次の例では、SetIterator.toString メソッドを使用して、反復子がセットのスキャンを開始する前にポイントする、そのセットの値の説明を出力します。</span><span class="sxs-lookup"><span data-stu-id="50445-1083">The following example uses the SetIterator.toString method to print a description of the value in the set that the iterator points to before it starts traversing the set.</span></span>

    { 
        Set s1 = new Set (Types::Integer); 
        int theElement; 
        SetIterator it; 
        // Add some elements 
        s1.add(3); 
        s1.add(4); 
        s1.add(13); 
        s1.add(1);  
        // Start a traversal of the elements in the set 
        it = new SetIterator(s1); 
        // The elements are fetched in the order: 1, 3, 4, 13 
        print it.toString(); // Prints "(begin)[1]" 
        while (it.more()) 
        { 
            theElement = it.value(); 
            print theElement; 
            // Fetch the next element 
            it.next(); 
        } 
        pause; 
    }

### <a name="method-value"></a><span data-ttu-id="50445-1084">メソッド value</span><span class="sxs-lookup"><span data-stu-id="50445-1084">Method value</span></span>

<span data-ttu-id="50445-1085">反復子がポイントしている値を取得します。</span><span class="sxs-lookup"><span data-stu-id="50445-1085">Retrieves the value that the iterator is pointing to.</span></span>

    public AnyType value()

#### <a name="return-value"></a><span data-ttu-id="50445-1086">戻り値</span><span class="sxs-lookup"><span data-stu-id="50445-1086">Return Value</span></span>

<span data-ttu-id="50445-1087">反復子で示される値。</span><span class="sxs-lookup"><span data-stu-id="50445-1087">The value denoted by the iterator.</span></span>

#### <a name="remarks"></a><span data-ttu-id="50445-1088">備考</span><span class="sxs-lookup"><span data-stu-id="50445-1088">Remarks</span></span>

<span data-ttu-id="50445-1089">SetIterator.more を使用して、set 要素のキー値を取得する前に要素が存在するかどうかを確認します。</span><span class="sxs-lookup"><span data-stu-id="50445-1089">Use SetIterator.more to check whether an element exists before trying to retrieve the key value of the set element.</span></span>

#### <a name="examples"></a><span data-ttu-id="50445-1090">例</span><span class="sxs-lookup"><span data-stu-id="50445-1090">Examples</span></span>

<span data-ttu-id="50445-1091">次の例では、SetIterator.value メソッドを使用して、セット内の現在の項目の値を出力します。</span><span class="sxs-lookup"><span data-stu-id="50445-1091">The following example uses the SetIterator.value method to print the value of the current item in the set.</span></span>

    { 
        Set s1 = new Set (Types::Integer); 
        SetIterator it; 
        // Add some elements 
        s1.add(3); 
        s1.add(4); 
        s1.add(13); 
        s1.add(1);  
        // Start a traversal of the elements in the set 
        it = new SetIterator(s1); 
        // Prints "(begin)[1]" 
        print it.toString();  
        // The elements are fetched in the order: 1, 3, 4, 13 
        while (it.more()) 
        { 
            print it.value(); 
            // Fetch the next element 
            it.next(); 
        } 
        pause; 
    }

### <a name="method-next"></a><span data-ttu-id="50445-1092">メソッド next</span><span class="sxs-lookup"><span data-stu-id="50445-1092">Method next</span></span>

<span data-ttu-id="50445-1093">次の要素に反復子を移動します。</span><span class="sxs-lookup"><span data-stu-id="50445-1093">Moves the iterator to the next element.</span></span>

    public void next()

#### <a name="remarks"></a><span data-ttu-id="50445-1094">備考</span><span class="sxs-lookup"><span data-stu-id="50445-1094">Remarks</span></span>

<span data-ttu-id="50445-1095">SetIterator.more を使用して、反復子が有効な要素を指しているかどうかを判断します。</span><span class="sxs-lookup"><span data-stu-id="50445-1095">Use SetIterator.more to determine whether the iterator points to a valid element.</span></span>

#### <a name="examples"></a><span data-ttu-id="50445-1096">例</span><span class="sxs-lookup"><span data-stu-id="50445-1096">Examples</span></span>

<span data-ttu-id="50445-1097">次の例では、SetIterator.next メソッドを使用して、反復子をセット内の次の要素に移動し、別の要素が存在するかどうかをテストし、別の要素がある場合はその値をコンテナーに追加します。</span><span class="sxs-lookup"><span data-stu-id="50445-1097">The following example uses the SetIterator.next method to move the iterator to the next element in the set, before testing whether there is another element, and if there is another element, adding the value to a container.</span></span>

    static public void saveSequence(classId _classId, Set _sequence) 
    { 
        SysCheckListItemTable sysCheckListItemTable; 
        SetIterator           si; 
        container             con = connull(); 
        if (_sequence) 
        { 
            si = new SetIterator(_sequence); 
            si.begin(); 
            while (si.more()) 
            { 
                 con += si.value(); 
                 si.next(); 
            } 
        } 
        //... 
    }

### <a name="method-new"></a><span data-ttu-id="50445-1098">メソッド new</span><span class="sxs-lookup"><span data-stu-id="50445-1098">Method new</span></span>

<span data-ttu-id="50445-1099">セットに対する新しい反復子を作成します。</span><span class="sxs-lookup"><span data-stu-id="50445-1099">Creates a new iterator for a set.</span></span>

    public void new(Set set)

#### <a name="parameters"></a><span data-ttu-id="50445-1100">パラメーター</span><span class="sxs-lookup"><span data-stu-id="50445-1100">Parameters</span></span>

<span data-ttu-id="50445-1101">set</span><span class="sxs-lookup"><span data-stu-id="50445-1101">set</span></span>  
<span data-ttu-id="50445-1102">繰り返し処理するセット。</span><span class="sxs-lookup"><span data-stu-id="50445-1102">The set to iterate over.</span></span>

#### <a name="remarks"></a><span data-ttu-id="50445-1103">備考</span><span class="sxs-lookup"><span data-stu-id="50445-1103">Remarks</span></span>

<span data-ttu-id="50445-1104">反復子は、セットが空でない場合、セットの最初の値に配置されます。</span><span class="sxs-lookup"><span data-stu-id="50445-1104">The iterator is positioned at the first value in the set, if the set is not empty.</span></span>

#### <a name="examples"></a><span data-ttu-id="50445-1105">例</span><span class="sxs-lookup"><span data-stu-id="50445-1105">Examples</span></span>

<span data-ttu-id="50445-1106">次の例では、整数のセットを作成し、セットの反復子を作成します。</span><span class="sxs-lookup"><span data-stu-id="50445-1106">The following example creates a set of integers and then creates an iterator for that set</span></span>

    Set s1 = new Set (Types::Integer); 
    SetIterator it; 
    it = new SetIterator(s1);

### <a name="method-begin"></a><span data-ttu-id="50445-1107">メソッド begin</span><span class="sxs-lookup"><span data-stu-id="50445-1107">Method begin</span></span>

<span data-ttu-id="50445-1108">反復子をセットの先頭に移動します。</span><span class="sxs-lookup"><span data-stu-id="50445-1108">Moves the iterator to the start of the set.</span></span>

    public void begin()

#### <a name="remarks"></a><span data-ttu-id="50445-1109">備考</span><span class="sxs-lookup"><span data-stu-id="50445-1109">Remarks</span></span>

<span data-ttu-id="50445-1110">新しく作成されるセット反復子は、セットの最初の要素に配置されます。</span><span class="sxs-lookup"><span data-stu-id="50445-1110">Newly created set iterators are positioned at the first element in the set.</span></span> <span data-ttu-id="50445-1111">通常はセットを反復処理する前に begin メソッドを呼び出す必要はありません。後でポインタをリセットしたい場合にのみ、その操作を行う必要があります。</span><span class="sxs-lookup"><span data-stu-id="50445-1111">Typically, you do not need to call the begin method before you start to iterate through the set; you need to do that only if you want to reset the pointer later on.</span></span>

#### <a name="examples"></a><span data-ttu-id="50445-1112">例</span><span class="sxs-lookup"><span data-stu-id="50445-1112">Examples</span></span>

<span data-ttu-id="50445-1113">次の例では、指定されたインターフェイス、つまり \_id クラスを実装するクラスのクラス ID のセットを返します。</span><span class="sxs-lookup"><span data-stu-id="50445-1113">The following example returns set of class IDs of the classes that implement the specified interface, that is, the \_id class.</span></span> <span data-ttu-id="50445-1114">スーパークラスの場合、反復子は設定からクラスを削除するために使用され、\_onlyLeafClasses パラメーターは true に設定されます。</span><span class="sxs-lookup"><span data-stu-id="50445-1114">An iterator is used to remove classes from the set if they are superclasses, and the \_onlyLeafClasses parameter is set to true.</span></span> <span data-ttu-id="50445-1115">開始メソッドを使用して、セットからスーパークラスが削除された後に反復子をリセットします。</span><span class="sxs-lookup"><span data-stu-id="50445-1115">The begin method is used to reset the iterator after the superclasses have been removed from the set.</span></span>

    public static Set getImplements( 
        classId _id,  
        boolean _onlyLeafClasses = true) 
    { 
        Dictionary dictionary = new Dictionary(); 
        SysDictClass sysDictClass; 
        boolean removed; 
        Set set = new Set(Types::Integer); 
        SetIterator setIterator = new SetIterator(set); 
        int i; 
        for (i=1;i<=dictionary.classCnt();i++) 
        { 
            sysDictClass = new SysDictClass(dictionary.classCnt2Id(i)); 
            if (sysDictClass.isImplementing(_id)) 
            { 
                set.add(sysDictClass.id()); 
            } 
        } 
        //No superclasses included in return set 
        if (_onlyLeafClasses) 
        { 
            // begin method not needed here; only for clarity 
            setIterator.begin();  
            while (setIterator.more()) 
            { 
                removed = false; 
                sysDictClass = new SysDictClass(setIterator.value()); 
                while (sysDictClass.extend()) 
                { 
                    removed = removed | set.remove(sysDictClass.extend()); 
                    sysDictClass = new SysDictClass(sysDictClass.extend()); 
                } 
                if (removed) 
                { 
                    // Restart search 
                    setIterator.begin();  
                } 
                else 
                { 
                    setIterator.next(); 
                } 
            } 
        } 
        return set; 
    }

### <a name="method-delete"></a><span data-ttu-id="50445-1116">メソッド delete</span><span class="sxs-lookup"><span data-stu-id="50445-1116">Method delete</span></span>

<span data-ttu-id="50445-1117">セットの反復子によってポイントされている要素を削除します。</span><span class="sxs-lookup"><span data-stu-id="50445-1117">Removes the element that is pointed to by the iterator of the set.</span></span>

    public void delete()

#### <a name="remarks"></a><span data-ttu-id="50445-1118">備考</span><span class="sxs-lookup"><span data-stu-id="50445-1118">Remarks</span></span>

<span data-ttu-id="50445-1119">反復子は、このメソッドを呼び出した後に次の要素を指します。</span><span class="sxs-lookup"><span data-stu-id="50445-1119">The iterator will point to the next element after calling this method.</span></span>

#### <a name="examples"></a><span data-ttu-id="50445-1120">例</span><span class="sxs-lookup"><span data-stu-id="50445-1120">Examples</span></span>

<span data-ttu-id="50445-1121">次の例では、すべての奇数要素をセットから削除します。</span><span class="sxs-lookup"><span data-stu-id="50445-1121">The following example deletes all the odd elements from the set.</span></span>

    { 
        Set iset = new Set (Types::Integer); 
        SetIterator it; 
        int i; 
        for (i = 1; i <= 10; i++) 
        { 
            iset.add(i); 
        } 
        // Delete all odd elements 
        it = new SetIterator(iset); 
        while (it.more()) 
        { 
            if (it.value() mod 2 != 0) 
            { 
                // The value is odd. Delete and skip to next element. 
                it.delete(); 
            } 
            else 
            { 
                it.next(); 
            } 
        } 
        print iset.toString(); 
        pause; 
    }

### <a name="method-end"></a><span data-ttu-id="50445-1122">メソッド end</span><span class="sxs-lookup"><span data-stu-id="50445-1122">Method end</span></span>

<span data-ttu-id="50445-1123">セットで最後の要素の後に反復子を移動します。</span><span class="sxs-lookup"><span data-stu-id="50445-1123">Moves the iterator past the last element in the set.</span></span>

    public void end()

#### <a name="remarks"></a><span data-ttu-id="50445-1124">備考</span><span class="sxs-lookup"><span data-stu-id="50445-1124">Remarks</span></span>

<span data-ttu-id="50445-1125">このメソッドを実行した後、より多くのメソッドは false を返します。</span><span class="sxs-lookup"><span data-stu-id="50445-1125">After executing this method, the more method will return false.</span></span>

## <a name="class-skipaosvalidationpermission"></a><span data-ttu-id="50445-1126">クラス SkipAOSValidationPermission</span><span class="sxs-lookup"><span data-stu-id="50445-1126">Class SkipAOSValidationPermission</span></span>
    class SkipAOSValidationPermission extends CodeAccessPermission

<span data-ttu-id="50445-1127">SkipAOSValidationPermission クラスは、AOS 検証を省略して、特定の API のアクセス許可をチェックする機能を制御します。</span><span class="sxs-lookup"><span data-stu-id="50445-1127">The SkipAOSValidationPermission class controls the ability to skip AOS validation and check permissions for specific APIs.</span></span>

### <a name="remarks"></a><span data-ttu-id="50445-1128">備考</span><span class="sxs-lookup"><span data-stu-id="50445-1128">Remarks</span></span>

<span data-ttu-id="50445-1129">保護されたすべての API のリストについては、「セキュリティで保護された API」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="50445-1129">For a list of all protected APIs, see Secured APIs.</span></span> <span data-ttu-id="50445-1130">保護された API が実行される前に、対応する CodeAccessPermission.demand メソッドが呼び出される、通常はサーバー層である、同じ層で assert メソッドを呼び出す必要があります。</span><span class="sxs-lookup"><span data-stu-id="50445-1130">You must call the assert method on the same tier, usually the server tier, that the corresponding CodeAccessPermission.demand method is called on before the protected API is executed.</span></span> <span data-ttu-id="50445-1131">次のいずれかでサーバー層のメソッドを呼び出します。サーバー静的メソッド または RunOn クラス プロパティを使用してサーバー上で実行するように設定されているクラス インスタンス メソッド。</span><span class="sxs-lookup"><span data-stu-id="50445-1131">Call a method on the server tier from one of the following: A server static method –or– A class instance method that is set to run on the server by using the RunOn class property.</span></span>

### <a name="examples"></a><span data-ttu-id="50445-1132">例</span><span class="sxs-lookup"><span data-stu-id="50445-1132">Examples</span></span>

### <a name="methods"></a><span data-ttu-id="50445-1133">メソッド</span><span class="sxs-lookup"><span data-stu-id="50445-1133">Methods</span></span>

| <span data-ttu-id="50445-1134">方法</span><span class="sxs-lookup"><span data-stu-id="50445-1134">Method</span></span>                                                 | <span data-ttu-id="50445-1135">説明</span><span class="sxs-lookup"><span data-stu-id="50445-1135">Description</span></span>                                                                                                         |
|--------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="50445-1136">public CodeAccessPermission copy()</span><span class="sxs-lookup"><span data-stu-id="50445-1136">public CodeAccessPermission copy()</span></span>                     | <span data-ttu-id="50445-1137">アクセス許可クラス オブジェクトのコピーを作成し、返します。</span><span class="sxs-lookup"><span data-stu-id="50445-1137">Creates and returns a copy of a permission class object.</span></span>                                                            |
| <span data-ttu-id="50445-1138">public boolean isSubsetOf(CodeAccessPermission target)</span><span class="sxs-lookup"><span data-stu-id="50445-1138">public boolean isSubsetOf(CodeAccessPermission target)</span></span> | <span data-ttu-id="50445-1139">派生クラスによって上書きされたときに、現在のアクセス許可が指定されたアクセス許可のサブセットであるかどうかを判断します。</span><span class="sxs-lookup"><span data-stu-id="50445-1139">Determines whether a current permission is a subset of the specified permission when overridden by a derived class.</span></span> |
| <span data-ttu-id="50445-1140">public void new()</span><span class="sxs-lookup"><span data-stu-id="50445-1140">public void new()</span></span>                                      | <span data-ttu-id="50445-1141">SkipAOSValidationPermission クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="50445-1141">Initializes a new instance of the SkipAOSValidationPermission class.</span></span>                                                |

### <a name="method-copy"></a><span data-ttu-id="50445-1142">メソッド copy</span><span class="sxs-lookup"><span data-stu-id="50445-1142">Method copy</span></span>

<span data-ttu-id="50445-1143">アクセス許可クラス オブジェクトのコピーを作成し、返します。</span><span class="sxs-lookup"><span data-stu-id="50445-1143">Creates and returns a copy of a permission class object.</span></span>

    public CodeAccessPermission copy()

#### <a name="return-value"></a><span data-ttu-id="50445-1144">戻り値</span><span class="sxs-lookup"><span data-stu-id="50445-1144">Return Value</span></span>

<span data-ttu-id="50445-1145">現在の派生クラスオブジェクトのコピーです。</span><span class="sxs-lookup"><span data-stu-id="50445-1145">A copy of the derived class object.</span></span>

#### <a name="remarks"></a><span data-ttu-id="50445-1146">備考</span><span class="sxs-lookup"><span data-stu-id="50445-1146">Remarks</span></span>

<span data-ttu-id="50445-1147">API のセキュリティをさらに強化するプロセスの一部として、このメソッドをオーバーライドすることができます。</span><span class="sxs-lookup"><span data-stu-id="50445-1147">You can override this method as part of the process of making an API more secure.</span></span> <span data-ttu-id="50445-1148">詳細については、「」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="50445-1148">For more information, see .</span></span>

### <a name="method-issubsetof"></a><span data-ttu-id="50445-1149">メソッド isSubsetOf</span><span class="sxs-lookup"><span data-stu-id="50445-1149">Method isSubsetOf</span></span>

<span data-ttu-id="50445-1150">派生クラスによって上書きされたときに、現在のアクセス許可が指定されたアクセス許可のサブセットであるかどうかを判断します。</span><span class="sxs-lookup"><span data-stu-id="50445-1150">Determines whether a current permission is a subset of the specified permission when overridden by a derived class.</span></span>

    public boolean isSubsetOf(CodeAccessPermission target)

#### <a name="parameters"></a><span data-ttu-id="50445-1151">パラメーター</span><span class="sxs-lookup"><span data-stu-id="50445-1151">Parameters</span></span>

<span data-ttu-id="50445-1152">target</span><span class="sxs-lookup"><span data-stu-id="50445-1152">target</span></span>  
<span data-ttu-id="50445-1153">CodeAccessPermission クラス オブジェクト。</span><span class="sxs-lookup"><span data-stu-id="50445-1153">A CodeAccessPermission class object.</span></span>

#### <a name="return-value"></a><span data-ttu-id="50445-1154">戻り値</span><span class="sxs-lookup"><span data-stu-id="50445-1154">Return Value</span></span>

<span data-ttu-id="50445-1155">現在のアクセス許可が指定したアクセス許可のサブセットである場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="50445-1155">true if a current permission is a subset of a specified permission; otherwise, false.</span></span>

#### <a name="remarks"></a><span data-ttu-id="50445-1156">備考</span><span class="sxs-lookup"><span data-stu-id="50445-1156">Remarks</span></span>

<span data-ttu-id="50445-1157">API のセキュリティをさらに強化するプロセスの一部として、メソッドをオーバーライドすることができます。</span><span class="sxs-lookup"><span data-stu-id="50445-1157">You can override the method as part of the process of making an API more secure.</span></span> <span data-ttu-id="50445-1158">詳細については、「」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="50445-1158">For more information, see .</span></span>

### <a name="method-new"></a><span data-ttu-id="50445-1159">メソッド new</span><span class="sxs-lookup"><span data-stu-id="50445-1159">Method new</span></span>

<span data-ttu-id="50445-1160">SkipAOSValidationPermission クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="50445-1160">Initializes a new instance of the SkipAOSValidationPermission class.</span></span>

    public void new()

#### <a name="examples"></a><span data-ttu-id="50445-1161">例</span><span class="sxs-lookup"><span data-stu-id="50445-1161">Examples</span></span>

<span data-ttu-id="50445-1162">次のコード例は、SkipAOSValidationPermission クラスのインスタンスを作成する方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="50445-1162">The following code example demonstrates how to create an instance of the SkipAOSValidationPermission class.</span></span>

    server static void main(Args args) 
    { 
        SkipAOSValidationPermission perm; 
        ; 
        perm = new SkipAOSValidationPermission(); 
    }

## <a name="class-sqldatadictionary"></a><span data-ttu-id="50445-1163">クラス SqlDataDictionary</span><span class="sxs-lookup"><span data-stu-id="50445-1163">Class SqlDataDictionary</span></span>
    class SqlDataDictionary extends Object

<span data-ttu-id="50445-1164">SqlDataDictionary クラスは、データ ディクショナリ保守のメソッドのコレクションを提供します。</span><span class="sxs-lookup"><span data-stu-id="50445-1164">The SqlDataDictionary class provides a collection of methods for data dictionary maintenance.</span></span>

### <a name="remarks"></a><span data-ttu-id="50445-1165">備考</span><span class="sxs-lookup"><span data-stu-id="50445-1165">Remarks</span></span>

<span data-ttu-id="50445-1166">この API には、実行時に呼び出される組み込み認証チェックがあります。</span><span class="sxs-lookup"><span data-stu-id="50445-1166">This API has a built-in authorization check that is invoked at run time.</span></span> <span data-ttu-id="50445-1167">開発セキュリティ キー (SysDevelopment) にアクセスせずにユーザーが SQLDataDictionary クラスのメンバーを呼び出すと、例外が発生します。</span><span class="sxs-lookup"><span data-stu-id="50445-1167">Calls to members of the SQLDataDictionary class by users without access to the development security key (SysDevelopment) results in an exception.</span></span>

### <a name="examples"></a><span data-ttu-id="50445-1168">例</span><span class="sxs-lookup"><span data-stu-id="50445-1168">Examples</span></span>

<span data-ttu-id="50445-1169">次の例では、UserInfo テーブルがデータベースに存在するかどうかを確認します。</span><span class="sxs-lookup"><span data-stu-id="50445-1169">The following example checks whether the UserInfo table exists in the database.</span></span>

    server static public void Main(Args _args) 
    { 
        SqlDataDictionary sqlDict; 
        boolean b; 
        sqlDict = new SqlDataDictionary(); 
        if (sqlDict) 
        { 
            b = sqlDict.tableExist("USERINFO"); 
            print b; 
            pause; 
        } 
    }

### <a name="methods"></a><span data-ttu-id="50445-1170">メソッド</span><span class="sxs-lookup"><span data-stu-id="50445-1170">Methods</span></span>

| <span data-ttu-id="50445-1171">方法</span><span class="sxs-lookup"><span data-stu-id="50445-1171">Method</span></span>                                                                                                               | <span data-ttu-id="50445-1172">説明</span><span class="sxs-lookup"><span data-stu-id="50445-1172">Description</span></span>                                                                                                                   |
|----------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="50445-1173">public int indexCreate(\[TableId tableId\], \[IndexId indexId\])</span><span class="sxs-lookup"><span data-stu-id="50445-1173">public int indexCreate(\[TableId tableId\], \[IndexId indexId\])</span></span>                                                     | <span data-ttu-id="50445-1174">テーブルのインデックスを SQL データベースで作成します。</span><span class="sxs-lookup"><span data-stu-id="50445-1174">Creates the indexes of a table in the SQL database.</span></span> <span data-ttu-id="50445-1175">このメソッドを使用してインデックスを再作成することもできます。</span><span class="sxs-lookup"><span data-stu-id="50445-1175">You can also use this method to re-create indexes.</span></span> |
| <span data-ttu-id="50445-1176">public str indexCreateDDL(TableId tableId)</span><span class="sxs-lookup"><span data-stu-id="50445-1176">public str indexCreateDDL(TableId tableId)</span></span>                                                                           | <span data-ttu-id="50445-1177">テーブルのインデックスを作成するのに必要な SQL ステートメントを生成および返します。</span><span class="sxs-lookup"><span data-stu-id="50445-1177">Generates and returns the SQL statements needed to create the indexes of a table.</span></span>                      |
| <span data-ttu-id="50445-1178">public int indexDrop(\[TableId tableId\], \[IndexId indexId\], \[boolean onlyNonUnique\])</span><span class="sxs-lookup"><span data-stu-id="50445-1178">public int indexDrop(\[TableId tableId\], \[IndexId indexId\], \[boolean onlyNonUnique\])</span></span>                            | <span data-ttu-id="50445-1179">テーブルのインデックスを SQL データベースでドロップします。</span><span class="sxs-lookup"><span data-stu-id="50445-1179">Drops the indexes of a table in the SQL database.</span></span>                                                      |
| <span data-ttu-id="50445-1180">public str name(str bmsname, \[FieldId fieldId\], \[int arrayindex\])</span><span class="sxs-lookup"><span data-stu-id="50445-1180">public str name(str bmsname, \[FieldId fieldId\], \[int arrayindex\])</span></span>                                                | <span data-ttu-id="50445-1181">任意のオブジェクト名を有効な SQL データベースのオブジェクト名、つまり、現在接続されているデータベースに有効な名前に変換します。</span><span class="sxs-lookup"><span data-stu-id="50445-1181">Translates any object name into a valid SQL database object-name; that is, valid for the database currently connected.</span></span>        |
| <span data-ttu-id="50445-1182">public int tableCreate(\[boolean indexes\], \[TableId tableId\])</span><span class="sxs-lookup"><span data-stu-id="50445-1182">public int tableCreate(\[boolean indexes\], \[TableId tableId\])</span></span>                                                     | <span data-ttu-id="50445-1183">1 つ以上のテーブルを SQL データベース内に作成します。</span><span class="sxs-lookup"><span data-stu-id="50445-1183">Creates one or more  tables in the SQL database.</span></span> <span data-ttu-id="50445-1184">また、インデックス用に作成するオプションを提供します。</span><span class="sxs-lookup"><span data-stu-id="50445-1184">Also, provides an option to create for index.</span></span>           |
| <span data-ttu-id="50445-1185">public str tableCreateDDL(TableId tableId)</span><span class="sxs-lookup"><span data-stu-id="50445-1185">public str tableCreateDDL(TableId tableId)</span></span>                                                                           | <span data-ttu-id="50445-1186">テーブルを作成するため SQL ステートメントを生成および返します。</span><span class="sxs-lookup"><span data-stu-id="50445-1186">Generates and returns the SQL statement to create a table.</span></span>                                             |
| <span data-ttu-id="50445-1187">public int tableDrop(TableId tableId, \[boolean prompt\_before\_drop\])</span><span class="sxs-lookup"><span data-stu-id="50445-1187">public int tableDrop(TableId tableId, \[boolean prompt\_before\_drop\])</span></span>                                              | <span data-ttu-id="50445-1188">テーブルを SQL データベースでドロップします。</span><span class="sxs-lookup"><span data-stu-id="50445-1188">Drops the  table in the SQL database.</span></span>                                                                    |
| <span data-ttu-id="50445-1189">public str tableDropDDL(TableId tableId)</span><span class="sxs-lookup"><span data-stu-id="50445-1189">public str tableDropDDL(TableId tableId)</span></span>                                                                             | <span data-ttu-id="50445-1190">テーブルをドロップするため SQL ステートメントを生成および返します。</span><span class="sxs-lookup"><span data-stu-id="50445-1190">Generates and returns the SQL statement to drop a table.</span></span>                                               |
| <span data-ttu-id="50445-1191">public boolean tableEmpty(TableId tableId, \[str company\], \[boolean not\_this\_company\])</span><span class="sxs-lookup"><span data-stu-id="50445-1191">public boolean tableEmpty(TableId tableId, \[str company\], \[boolean not\_this\_company\])</span></span>                          | <span data-ttu-id="50445-1192">テーブルが空でない場合は true を返します。それ以外の場合は、false を返します。</span><span class="sxs-lookup"><span data-stu-id="50445-1192">Returns true if table is not empty; otherwise false.</span></span>                                                                          |
| <span data-ttu-id="50445-1193">public boolean tableExist(str sqltablename, \[boolean use\_within\_transaction\])</span><span class="sxs-lookup"><span data-stu-id="50445-1193">public boolean tableExist(str sqltablename, \[boolean use\_within\_transaction\])</span></span>                                    | <span data-ttu-id="50445-1194">テーブルが存在する場合は true を返します。それ以外の場合は、false を返します。</span><span class="sxs-lookup"><span data-stu-id="50445-1194">Returns true if table exists; otherwise false.</span></span>                                                                                |
| <span data-ttu-id="50445-1195">public int tableMetaData(TableId tableId)</span><span class="sxs-lookup"><span data-stu-id="50445-1195">public int tableMetaData(TableId tableId)</span></span>                                                                            | <span data-ttu-id="50445-1196">データ ディクショナリ メタ データで SqlDescribe テーブルを入力します。</span><span class="sxs-lookup"><span data-stu-id="50445-1196">Fills the SqlDescribe table with data dictionary meta data.</span></span>                                                                   |
| <span data-ttu-id="50445-1197">public int tableReindex(\[TableId tableId\], \[IndexId indexId\])</span><span class="sxs-lookup"><span data-stu-id="50445-1197">public int tableReindex(\[TableId tableId\], \[IndexId indexId\])</span></span>                                                    | <span data-ttu-id="50445-1198">テーブルのインデックスを更新します。</span><span class="sxs-lookup"><span data-stu-id="50445-1198">Updates index for the table.</span></span>                                                                                                  |
| <span data-ttu-id="50445-1199">public int tableSynchronize(TableId tableId, \[boolean update\_dict\_info\_only\], \[boolean check\_indexes\])</span><span class="sxs-lookup"><span data-stu-id="50445-1199">public int tableSynchronize(TableId tableId, \[boolean update\_dict\_info\_only\], \[boolean check\_indexes\])</span></span>       | <span data-ttu-id="50445-1200">テーブルと、SQL データベースのテーブルを同期します。</span><span class="sxs-lookup"><span data-stu-id="50445-1200">Synchronizes the  table and the table of the SQL database.</span></span>                                               |
| <span data-ttu-id="50445-1201">public int tableTruncate(TableId tableId, \[boolean prompt\_before\_truncate\], \[boolean truncate\_system\_table\])</span><span class="sxs-lookup"><span data-stu-id="50445-1201">public int tableTruncate(TableId tableId, \[boolean prompt\_before\_truncate\], \[boolean truncate\_system\_table\])</span></span> | <span data-ttu-id="50445-1202">テーブルの切り詰め</span><span class="sxs-lookup"><span data-stu-id="50445-1202">Truncates the  table.</span></span>                                                                                    |
| <span data-ttu-id="50445-1203">public str tableTruncateDDL(TableId tableId)</span><span class="sxs-lookup"><span data-stu-id="50445-1203">public str tableTruncateDDL(TableId tableId)</span></span>                                                                         | <span data-ttu-id="50445-1204">テーブルを切り詰めるため SQL ステートメントを生成および返します。</span><span class="sxs-lookup"><span data-stu-id="50445-1204">Generates and returns a SQL statement to truncate a table.</span></span>                                             |
| <span data-ttu-id="50445-1205">::public static int synchronize(\[boolean synchronize\_all\])</span><span class="sxs-lookup"><span data-stu-id="50445-1205">::public static int synchronize(\[boolean synchronize\_all\])</span></span>                                                        | <span data-ttu-id="50445-1206">データ ディクショナリと、SQL データベースのデータ ディクショナリを同期します。</span><span class="sxs-lookup"><span data-stu-id="50445-1206">Synchronizes the  data dictionary and the data dictionary of the SQL database.</span></span>                           |
| <span data-ttu-id="50445-1207">public void new()</span><span class="sxs-lookup"><span data-stu-id="50445-1207">public void new()</span></span>                                                                                                    | <span data-ttu-id="50445-1208">SqlDataDictionary クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="50445-1208">Initializes a new instance of the SqlDataDictionary class.</span></span>                                                                    |
| <span data-ttu-id="50445-1209">public void tableDelete(TableId tableId)</span><span class="sxs-lookup"><span data-stu-id="50445-1209">public void tableDelete(TableId tableId)</span></span>                                                                             | <span data-ttu-id="50445-1210">SQL データベースでテーブルを削除します。</span><span class="sxs-lookup"><span data-stu-id="50445-1210">Deletes the  table in the SQL database.</span></span>                                                                  |

### <a name="method-indexcreate"></a><span data-ttu-id="50445-1211">メソッド indexCreate</span><span class="sxs-lookup"><span data-stu-id="50445-1211">Method indexCreate</span></span>

<span data-ttu-id="50445-1212">テーブルのインデックスを SQL データベースで作成します。</span><span class="sxs-lookup"><span data-stu-id="50445-1212">Creates the indexes of a table in the SQL database.</span></span> <span data-ttu-id="50445-1213">このメソッドを使用してインデックスを再作成することもできます。</span><span class="sxs-lookup"><span data-stu-id="50445-1213">You can also use this method to re-create indexes.</span></span>

    public int indexCreate([TableId tableId], [IndexId indexId])

#### <a name="parameters"></a><span data-ttu-id="50445-1214">パラメーター</span><span class="sxs-lookup"><span data-stu-id="50445-1214">Parameters</span></span>

<span data-ttu-id="50445-1215">tableId</span><span class="sxs-lookup"><span data-stu-id="50445-1215">tableId</span></span>  
<span data-ttu-id="50445-1216">インデックス ハンドル (すべて0) (オプション)。</span><span class="sxs-lookup"><span data-stu-id="50445-1216">The index handle (0 for all); optional.</span></span>

<!-- -->

<span data-ttu-id="50445-1217">indexId</span><span class="sxs-lookup"><span data-stu-id="50445-1217">indexId</span></span>  
<span data-ttu-id="50445-1218">インデックス ハンドル (すべて0) (オプション)。</span><span class="sxs-lookup"><span data-stu-id="50445-1218">The index handle (0 for all); optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="50445-1219">戻り値</span><span class="sxs-lookup"><span data-stu-id="50445-1219">Return Value</span></span>

<span data-ttu-id="50445-1220">メソッドが成功した場合は 0 です。</span><span class="sxs-lookup"><span data-stu-id="50445-1220">0 if the method succeeds.</span></span>

#### <a name="remarks"></a><span data-ttu-id="50445-1221">備考</span><span class="sxs-lookup"><span data-stu-id="50445-1221">Remarks</span></span>

<span data-ttu-id="50445-1222">このメソッドを使用すると、インデックスを再作成できます。</span><span class="sxs-lookup"><span data-stu-id="50445-1222">This method can be used to re-create indexes.</span></span> <span data-ttu-id="50445-1223">パラメーターに 0 を使用すると、すべてのテーブルまたはインデックスを指定します。</span><span class="sxs-lookup"><span data-stu-id="50445-1223">Use 0 for the parameters to indicate all tables or indexes.</span></span>

#### <a name="examples"></a><span data-ttu-id="50445-1224">例</span><span class="sxs-lookup"><span data-stu-id="50445-1224">Examples</span></span>

    { 
        SqlDataDictionary DD = new SqlDataDictionary(); 
        DD.indexCreate(TableName2Id("Address")); 
    }

### <a name="method-indexcreateddl"></a><span data-ttu-id="50445-1225">メソッド indexCreateDDL</span><span class="sxs-lookup"><span data-stu-id="50445-1225">Method indexCreateDDL</span></span>

<span data-ttu-id="50445-1226">テーブルのインデックスを作成するのに必要な SQL ステートメントを生成および返します。</span><span class="sxs-lookup"><span data-stu-id="50445-1226">Generates and returns the SQL statements needed to create the indexes of a table.</span></span>

    public str indexCreateDDL(TableId tableId)

#### <a name="parameters"></a><span data-ttu-id="50445-1227">パラメーター</span><span class="sxs-lookup"><span data-stu-id="50445-1227">Parameters</span></span>

<span data-ttu-id="50445-1228">tableId</span><span class="sxs-lookup"><span data-stu-id="50445-1228">tableId</span></span>  
<span data-ttu-id="50445-1229">インデックスを作成する必要があるテーブル ハンドル。</span><span class="sxs-lookup"><span data-stu-id="50445-1229">The table handle that the index should be created for.</span></span>

#### <a name="return-value"></a><span data-ttu-id="50445-1230">戻り値</span><span class="sxs-lookup"><span data-stu-id="50445-1230">Return Value</span></span>

<span data-ttu-id="50445-1231">テーブルのインデックスを作成するための SQL ステートメントを返します。</span><span class="sxs-lookup"><span data-stu-id="50445-1231">Returns SQL statements to create the indexes of the  table.</span></span>

### <a name="method-indexdrop"></a><span data-ttu-id="50445-1232">メソッド indexDrop</span><span class="sxs-lookup"><span data-stu-id="50445-1232">Method indexDrop</span></span>

<span data-ttu-id="50445-1233">テーブルのインデックスを SQL データベースでドロップします。</span><span class="sxs-lookup"><span data-stu-id="50445-1233">Drops the indexes of a table in the SQL database.</span></span>

    public int indexDrop([TableId tableId], [IndexId indexId], [boolean onlyNonUnique])

#### <a name="parameters"></a><span data-ttu-id="50445-1234">パラメーター</span><span class="sxs-lookup"><span data-stu-id="50445-1234">Parameters</span></span>

<span data-ttu-id="50445-1235">tableId</span><span class="sxs-lookup"><span data-stu-id="50445-1235">tableId</span></span>  

<!-- -->

<span data-ttu-id="50445-1236">indexId</span><span class="sxs-lookup"><span data-stu-id="50445-1236">indexId</span></span>  

<!-- -->

<span data-ttu-id="50445-1237">onlyNonUnique</span><span class="sxs-lookup"><span data-stu-id="50445-1237">onlyNonUnique</span></span>  

#### <a name="return-value"></a><span data-ttu-id="50445-1238">戻り値</span><span class="sxs-lookup"><span data-stu-id="50445-1238">Return Value</span></span>

<span data-ttu-id="50445-1239">メソッドが成功した場合は 0。</span><span class="sxs-lookup"><span data-stu-id="50445-1239">Zero if the method succeeds.</span></span>

#### <a name="remarks"></a><span data-ttu-id="50445-1240">備考</span><span class="sxs-lookup"><span data-stu-id="50445-1240">Remarks</span></span>

<span data-ttu-id="50445-1241">パラメーターに 0 を使用すると、すべてのテーブルまたはインデックスを指定します。</span><span class="sxs-lookup"><span data-stu-id="50445-1241">Use 0 for the parameters to indicate all tables or indexes.</span></span>

#### <a name="examples"></a><span data-ttu-id="50445-1242">例</span><span class="sxs-lookup"><span data-stu-id="50445-1242">Examples</span></span>

    { 
        SqlDataDictionary DD = new SqlDataDictionary(); 
        DD.indexDrop(TableName2Id("Address")); 
    }

### <a name="method-name"></a><span data-ttu-id="50445-1243">メソッド名</span><span class="sxs-lookup"><span data-stu-id="50445-1243">Method name</span></span>

<span data-ttu-id="50445-1244">任意のオブジェクト名を有効な SQL データベースのオブジェクト名、つまり、現在接続されているデータベースに有効な名前に変換します。</span><span class="sxs-lookup"><span data-stu-id="50445-1244">Translates any object name into a valid SQL database object-name; that is, valid for the database currently connected.</span></span>

    public str name(str bmsname, [FieldId fieldId], [int arrayindex])

#### <a name="parameters"></a><span data-ttu-id="50445-1245">パラメーター</span><span class="sxs-lookup"><span data-stu-id="50445-1245">Parameters</span></span>

<span data-ttu-id="50445-1246">bmsname</span><span class="sxs-lookup"><span data-stu-id="50445-1246">bmsname</span></span>  
<span data-ttu-id="50445-1247">フィールドのインデックス (適用されない場合は 0)、つまり、分析コード \[2\] などの配列フィールドの arrayindex'th エントリです (オプション)。</span><span class="sxs-lookup"><span data-stu-id="50445-1247">A field index (0 for not applicable), that is, an array field's arrayindex'th entry, such as Dimension\[2\]; optional.</span></span>

<!-- -->

<span data-ttu-id="50445-1248">fieldId</span><span class="sxs-lookup"><span data-stu-id="50445-1248">fieldId</span></span>  
<span data-ttu-id="50445-1249">フィールドのインデックス (適用されない場合は 0)、つまり、分析コード \[2\] などの配列フィールドの arrayindex'th エントリです (オプション)。</span><span class="sxs-lookup"><span data-stu-id="50445-1249">A field index (0 for not applicable), that is, an array field's arrayindex'th entry, such as Dimension\[2\]; optional.</span></span>

<!-- -->

<span data-ttu-id="50445-1250">arrayindex</span><span class="sxs-lookup"><span data-stu-id="50445-1250">arrayindex</span></span>  
<span data-ttu-id="50445-1251">フィールドのインデックス (適用されない場合は 0)、つまり、分析コード \[2\] などの配列フィールドの arrayindex'th エントリです (オプション)。</span><span class="sxs-lookup"><span data-stu-id="50445-1251">A field index (0 for not applicable), that is, an array field's arrayindex'th entry, such as Dimension\[2\]; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="50445-1252">戻り値</span><span class="sxs-lookup"><span data-stu-id="50445-1252">Return Value</span></span>

<span data-ttu-id="50445-1253">有効なオブジェクト名。</span><span class="sxs-lookup"><span data-stu-id="50445-1253">The valid object name.</span></span>

#### <a name="remarks"></a><span data-ttu-id="50445-1254">備考</span><span class="sxs-lookup"><span data-stu-id="50445-1254">Remarks</span></span>

<span data-ttu-id="50445-1255">名前は切り捨てられる可能性があるため、固有のオブジェクト識別子が指定される場合があります。</span><span class="sxs-lookup"><span data-stu-id="50445-1255">Because names may be truncated, a unique object identifier may be supplied.</span></span> <span data-ttu-id="50445-1256">また、3 番目のパラメータは、メソッドが配列フィールドの個別の SQL フィールド名を返すことを可能にします。</span><span class="sxs-lookup"><span data-stu-id="50445-1256">Also, a third parameter enables the method to return discrete SQL field names for  array fields.</span></span>

### <a name="method-tablecreate"></a><span data-ttu-id="50445-1257">メソッド tableCreate</span><span class="sxs-lookup"><span data-stu-id="50445-1257">Method tableCreate</span></span>

<span data-ttu-id="50445-1258">1 つ以上のテーブルを SQL データベース内に作成します。</span><span class="sxs-lookup"><span data-stu-id="50445-1258">Creates one or more  tables in the SQL database.</span></span> <span data-ttu-id="50445-1259">また、インデックス用に作成するオプションを提供します。</span><span class="sxs-lookup"><span data-stu-id="50445-1259">Also, provides an option to create for index.</span></span>

    public int tableCreate([boolean indexes], [TableId tableId])

#### <a name="parameters"></a><span data-ttu-id="50445-1260">パラメーター</span><span class="sxs-lookup"><span data-stu-id="50445-1260">Parameters</span></span>

<span data-ttu-id="50445-1261">indexes</span><span class="sxs-lookup"><span data-stu-id="50445-1261">indexes</span></span>  
<span data-ttu-id="50445-1262">テーブル ハンドル (すべて0) (オプション)。</span><span class="sxs-lookup"><span data-stu-id="50445-1262">The table handle (0 for all); optional.</span></span>

<!-- -->

<span data-ttu-id="50445-1263">tableId</span><span class="sxs-lookup"><span data-stu-id="50445-1263">tableId</span></span>  
<span data-ttu-id="50445-1264">テーブル ハンドル (すべて0) (オプション)。</span><span class="sxs-lookup"><span data-stu-id="50445-1264">The table handle (0 for all); optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="50445-1265">戻り値</span><span class="sxs-lookup"><span data-stu-id="50445-1265">Return Value</span></span>

<span data-ttu-id="50445-1266">メソッドが成功した場合は 0。</span><span class="sxs-lookup"><span data-stu-id="50445-1266">Zero if the method succeeds.</span></span>

#### <a name="remarks"></a><span data-ttu-id="50445-1267">備考</span><span class="sxs-lookup"><span data-stu-id="50445-1267">Remarks</span></span>

<span data-ttu-id="50445-1268">低レベルのメンテナンスにのみ使用されます。</span><span class="sxs-lookup"><span data-stu-id="50445-1268">Used for low-level maintenance only.</span></span>

#### <a name="examples"></a><span data-ttu-id="50445-1269">例</span><span class="sxs-lookup"><span data-stu-id="50445-1269">Examples</span></span>

    { 
        SqlDataDictionary DD = new SqlDataDictionary(); 
        DD.tableCreate(TableName2Id("Address")); 
    }

### <a name="method-tablecreateddl"></a><span data-ttu-id="50445-1270">メソッド tableCreateDDL</span><span class="sxs-lookup"><span data-stu-id="50445-1270">Method tableCreateDDL</span></span>

<span data-ttu-id="50445-1271">テーブルを作成するため SQL ステートメントを生成および返します。</span><span class="sxs-lookup"><span data-stu-id="50445-1271">Generates and returns the SQL statement to create a table.</span></span>

    public str tableCreateDDL(TableId tableId)

#### <a name="parameters"></a><span data-ttu-id="50445-1272">パラメーター</span><span class="sxs-lookup"><span data-stu-id="50445-1272">Parameters</span></span>

<span data-ttu-id="50445-1273">tableId</span><span class="sxs-lookup"><span data-stu-id="50445-1273">tableId</span></span>  
<span data-ttu-id="50445-1274">作成するテーブルのテーブル ハンドルです。</span><span class="sxs-lookup"><span data-stu-id="50445-1274">The table handle of the table to be created.</span></span>

#### <a name="return-value"></a><span data-ttu-id="50445-1275">戻り値</span><span class="sxs-lookup"><span data-stu-id="50445-1275">Return Value</span></span>

<span data-ttu-id="50445-1276">テーブルを作成する SQL ステートメント。</span><span class="sxs-lookup"><span data-stu-id="50445-1276">The SQL statement to create a table.</span></span>

### <a name="method-tabledrop"></a><span data-ttu-id="50445-1277">メソッド tableDrop</span><span class="sxs-lookup"><span data-stu-id="50445-1277">Method tableDrop</span></span>

<span data-ttu-id="50445-1278">テーブルを SQL データベースでドロップします。</span><span class="sxs-lookup"><span data-stu-id="50445-1278">Drops the  table in the SQL database.</span></span>

    public int tableDrop(TableId tableId, [boolean prompt_before_drop])

#### <a name="parameters"></a><span data-ttu-id="50445-1279">パラメーター</span><span class="sxs-lookup"><span data-stu-id="50445-1279">Parameters</span></span>

<span data-ttu-id="50445-1280">tableId</span><span class="sxs-lookup"><span data-stu-id="50445-1280">tableId</span></span>  
<span data-ttu-id="50445-1281">テーブルを削除する前にユーザーに確認するかどうかを示すブール フラグ; オプション。</span><span class="sxs-lookup"><span data-stu-id="50445-1281">A boolean flag that determines whether to ask user before dropping the table; optional.</span></span> <span data-ttu-id="50445-1282">既定では、true です。</span><span class="sxs-lookup"><span data-stu-id="50445-1282">By default, true.</span></span>

<!-- -->

<span data-ttu-id="50445-1283">prompt\_before\_drop</span><span class="sxs-lookup"><span data-stu-id="50445-1283">prompt\_before\_drop</span></span>  
<span data-ttu-id="50445-1284">テーブルを削除する前にユーザーに確認するかどうかを示すブール フラグ; オプション。</span><span class="sxs-lookup"><span data-stu-id="50445-1284">A boolean flag that determines whether to ask user before dropping the table; optional.</span></span> <span data-ttu-id="50445-1285">既定では、true です。</span><span class="sxs-lookup"><span data-stu-id="50445-1285">By default, true.</span></span>

#### <a name="return-value"></a><span data-ttu-id="50445-1286">戻り値</span><span class="sxs-lookup"><span data-stu-id="50445-1286">Return Value</span></span>

<span data-ttu-id="50445-1287">メソッドが成功した場合は 0。</span><span class="sxs-lookup"><span data-stu-id="50445-1287">Zero if the method succeeds.</span></span>

### <a name="method-tabledropddl"></a><span data-ttu-id="50445-1288">メソッド tableDropDDL</span><span class="sxs-lookup"><span data-stu-id="50445-1288">Method tableDropDDL</span></span>

<span data-ttu-id="50445-1289">テーブルをドロップするため SQL ステートメントを生成および返します。</span><span class="sxs-lookup"><span data-stu-id="50445-1289">Generates and returns the SQL statement to drop a table.</span></span>

    public str tableDropDDL(TableId tableId)

#### <a name="parameters"></a><span data-ttu-id="50445-1290">パラメーター</span><span class="sxs-lookup"><span data-stu-id="50445-1290">Parameters</span></span>

<span data-ttu-id="50445-1291">tableId</span><span class="sxs-lookup"><span data-stu-id="50445-1291">tableId</span></span>  
<span data-ttu-id="50445-1292">削除するテーブル。</span><span class="sxs-lookup"><span data-stu-id="50445-1292">The table to be dropped.</span></span>

#### <a name="return-value"></a><span data-ttu-id="50445-1293">戻り値</span><span class="sxs-lookup"><span data-stu-id="50445-1293">Return Value</span></span>

<span data-ttu-id="50445-1294">指定されたテーブルを削除する SQL ステートメント。</span><span class="sxs-lookup"><span data-stu-id="50445-1294">The SQL statement that drops the specified  table.</span></span>

### <a name="method-tableempty"></a><span data-ttu-id="50445-1295">メソッド tableEmpty</span><span class="sxs-lookup"><span data-stu-id="50445-1295">Method tableEmpty</span></span>

<span data-ttu-id="50445-1296">テーブルが空でない場合は true を返します。それ以外の場合は、false を返します。</span><span class="sxs-lookup"><span data-stu-id="50445-1296">Returns true if table is not empty; otherwise false.</span></span>

    public boolean tableEmpty(TableId tableId, [str company], [boolean not_this_company])

#### <a name="parameters"></a><span data-ttu-id="50445-1297">パラメーター</span><span class="sxs-lookup"><span data-stu-id="50445-1297">Parameters</span></span>

<span data-ttu-id="50445-1298">tableId</span><span class="sxs-lookup"><span data-stu-id="50445-1298">tableId</span></span>  
<span data-ttu-id="50445-1299">true の場合、クエリーから会社に属するレコードを除外します: オプション。</span><span class="sxs-lookup"><span data-stu-id="50445-1299">If true excludes records that belongs to the company from the query; optional.</span></span> <span data-ttu-id="50445-1300">既定では、false です。</span><span class="sxs-lookup"><span data-stu-id="50445-1300">By default, false.</span></span>

<!-- -->

<span data-ttu-id="50445-1301">会社</span><span class="sxs-lookup"><span data-stu-id="50445-1301">company</span></span>  
<span data-ttu-id="50445-1302">true の場合、クエリーから会社に属するレコードを除外します: オプション。</span><span class="sxs-lookup"><span data-stu-id="50445-1302">If true excludes records that belongs to the company from the query; optional.</span></span> <span data-ttu-id="50445-1303">既定では、false です。</span><span class="sxs-lookup"><span data-stu-id="50445-1303">By default, false.</span></span>

<!-- -->

<span data-ttu-id="50445-1304">not\_this\_company</span><span class="sxs-lookup"><span data-stu-id="50445-1304">not\_this\_company</span></span>  
<span data-ttu-id="50445-1305">true の場合、クエリーから会社に属するレコードを除外します: オプション。</span><span class="sxs-lookup"><span data-stu-id="50445-1305">If true excludes records that belongs to the company from the query; optional.</span></span> <span data-ttu-id="50445-1306">既定では、false です。</span><span class="sxs-lookup"><span data-stu-id="50445-1306">By default, false.</span></span>

#### <a name="return-value"></a><span data-ttu-id="50445-1307">戻り値</span><span class="sxs-lookup"><span data-stu-id="50445-1307">Return Value</span></span>

<span data-ttu-id="50445-1308">テーブルが空の場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="50445-1308">true if the table empty; otherwise, false.</span></span>

### <a name="method-tableexist"></a><span data-ttu-id="50445-1309">メソッド tableExist</span><span class="sxs-lookup"><span data-stu-id="50445-1309">Method tableExist</span></span>

<span data-ttu-id="50445-1310">テーブルが存在する場合は true を返します。それ以外の場合は、false を返します。</span><span class="sxs-lookup"><span data-stu-id="50445-1310">Returns true if table exists; otherwise false.</span></span>

    public boolean tableExist(str sqltablename, [boolean use_within_transaction])

#### <a name="parameters"></a><span data-ttu-id="50445-1311">パラメーター</span><span class="sxs-lookup"><span data-stu-id="50445-1311">Parameters</span></span>

<span data-ttu-id="50445-1312">sqltablename</span><span class="sxs-lookup"><span data-stu-id="50445-1312">sqltablename</span></span>  
<span data-ttu-id="50445-1313">トランザクションを使用するかどうかを決定するブール フラグ; オプション。</span><span class="sxs-lookup"><span data-stu-id="50445-1313">A boolean flag that determines whether transactions are to be used; optional.</span></span> <span data-ttu-id="50445-1314">既定では、false です。</span><span class="sxs-lookup"><span data-stu-id="50445-1314">By default, false.</span></span>

<!-- -->

<span data-ttu-id="50445-1315">use\_within\_transaction</span><span class="sxs-lookup"><span data-stu-id="50445-1315">use\_within\_transaction</span></span>  
<span data-ttu-id="50445-1316">トランザクションを使用するかどうかを決定するブール フラグ; オプション。</span><span class="sxs-lookup"><span data-stu-id="50445-1316">A boolean flag that determines whether transactions are to be used; optional.</span></span> <span data-ttu-id="50445-1317">既定では、false です。</span><span class="sxs-lookup"><span data-stu-id="50445-1317">By default, false.</span></span>

#### <a name="return-value"></a><span data-ttu-id="50445-1318">戻り値</span><span class="sxs-lookup"><span data-stu-id="50445-1318">Return Value</span></span>

<span data-ttu-id="50445-1319">テーブルが存在する場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="50445-1319">true if the table exists; otherwise, false.</span></span>

### <a name="method-tablemetadata"></a><span data-ttu-id="50445-1320">メソッド tableMetaData</span><span class="sxs-lookup"><span data-stu-id="50445-1320">Method tableMetaData</span></span>

<span data-ttu-id="50445-1321">データ ディクショナリ メタ データで SqlDescribe テーブルを入力します。</span><span class="sxs-lookup"><span data-stu-id="50445-1321">Fills the SqlDescribe table with data dictionary meta data.</span></span>

    public int tableMetaData(TableId tableId)

#### <a name="parameters"></a><span data-ttu-id="50445-1322">パラメーター</span><span class="sxs-lookup"><span data-stu-id="50445-1322">Parameters</span></span>

<span data-ttu-id="50445-1323">tableId</span><span class="sxs-lookup"><span data-stu-id="50445-1323">tableId</span></span>  
<span data-ttu-id="50445-1324">テーブル ハンドル。</span><span class="sxs-lookup"><span data-stu-id="50445-1324">The table handle.</span></span>

#### <a name="return-value"></a><span data-ttu-id="50445-1325">戻り値</span><span class="sxs-lookup"><span data-stu-id="50445-1325">Return Value</span></span>

<span data-ttu-id="50445-1326">メソッドが成功した場合は true。</span><span class="sxs-lookup"><span data-stu-id="50445-1326">true if the method succeeds.</span></span>

### <a name="method-tablereindex"></a><span data-ttu-id="50445-1327">メソッド tableReindex</span><span class="sxs-lookup"><span data-stu-id="50445-1327">Method tableReindex</span></span>

<span data-ttu-id="50445-1328">テーブルのインデックスを更新します。</span><span class="sxs-lookup"><span data-stu-id="50445-1328">Updates index for the table.</span></span>

    public int tableReindex([TableId tableId], [IndexId indexId])

#### <a name="parameters"></a><span data-ttu-id="50445-1329">パラメーター</span><span class="sxs-lookup"><span data-stu-id="50445-1329">Parameters</span></span>

<span data-ttu-id="50445-1330">tableId</span><span class="sxs-lookup"><span data-stu-id="50445-1330">tableId</span></span>  
<span data-ttu-id="50445-1331">インデックス ハンドル (すべて0) (オプション)。</span><span class="sxs-lookup"><span data-stu-id="50445-1331">The index handle (0 for all); optional.</span></span> <span data-ttu-id="50445-1332">既定では 0 です。</span><span class="sxs-lookup"><span data-stu-id="50445-1332">By default, 0.</span></span>

<!-- -->

<span data-ttu-id="50445-1333">indexId</span><span class="sxs-lookup"><span data-stu-id="50445-1333">indexId</span></span>  
<span data-ttu-id="50445-1334">インデックス ハンドル (すべて0) (オプション)。</span><span class="sxs-lookup"><span data-stu-id="50445-1334">The index handle (0 for all); optional.</span></span> <span data-ttu-id="50445-1335">既定では 0 です。</span><span class="sxs-lookup"><span data-stu-id="50445-1335">By default, 0.</span></span>

#### <a name="return-value"></a><span data-ttu-id="50445-1336">戻り値</span><span class="sxs-lookup"><span data-stu-id="50445-1336">Return Value</span></span>

<span data-ttu-id="50445-1337">メソッドが成功した場合は 0。</span><span class="sxs-lookup"><span data-stu-id="50445-1337">Zero if the method succeeds.</span></span>

### <a name="method-tablesynchronize"></a><span data-ttu-id="50445-1338">メソッド tableSynchronize</span><span class="sxs-lookup"><span data-stu-id="50445-1338">Method tableSynchronize</span></span>

<span data-ttu-id="50445-1339">テーブルと、SQL データベースのテーブルを同期します。</span><span class="sxs-lookup"><span data-stu-id="50445-1339">Synchronizes the  table and the table of the SQL database.</span></span>

    public int tableSynchronize(TableId tableId, [boolean update_dict_info_only], [boolean check_indexes])

#### <a name="parameters"></a><span data-ttu-id="50445-1340">パラメーター</span><span class="sxs-lookup"><span data-stu-id="50445-1340">Parameters</span></span>

<span data-ttu-id="50445-1341">tableId</span><span class="sxs-lookup"><span data-stu-id="50445-1341">tableId</span></span>  
<span data-ttu-id="50445-1342">設定すると、テーブルのインデックスの再インデックスを実行; 省略可能。</span><span class="sxs-lookup"><span data-stu-id="50445-1342">When set forces reindex of the table indexes; optional.</span></span> <span data-ttu-id="50445-1343">既定では、true です。</span><span class="sxs-lookup"><span data-stu-id="50445-1343">By default, true.</span></span>

<!-- -->

<span data-ttu-id="50445-1344">update\_dict\_info\_only</span><span class="sxs-lookup"><span data-stu-id="50445-1344">update\_dict\_info\_only</span></span>  
<span data-ttu-id="50445-1345">設定すると、テーブルのインデックスの再インデックスを実行; 省略可能。</span><span class="sxs-lookup"><span data-stu-id="50445-1345">When set forces reindex of the table indexes; optional.</span></span> <span data-ttu-id="50445-1346">既定では、true です。</span><span class="sxs-lookup"><span data-stu-id="50445-1346">By default, true.</span></span>

<!-- -->

<span data-ttu-id="50445-1347">check\_indexes</span><span class="sxs-lookup"><span data-stu-id="50445-1347">check\_indexes</span></span>  
<span data-ttu-id="50445-1348">設定すると、テーブルのインデックスの再インデックスを実行; 省略可能。</span><span class="sxs-lookup"><span data-stu-id="50445-1348">When set forces reindex of the table indexes; optional.</span></span> <span data-ttu-id="50445-1349">既定では、true です。</span><span class="sxs-lookup"><span data-stu-id="50445-1349">By default, true.</span></span>

#### <a name="return-value"></a><span data-ttu-id="50445-1350">戻り値</span><span class="sxs-lookup"><span data-stu-id="50445-1350">Return Value</span></span>

<span data-ttu-id="50445-1351">メソッドが成功した場合は true。</span><span class="sxs-lookup"><span data-stu-id="50445-1351">true if the method succeeds.</span></span>

### <a name="method-tabletruncate"></a><span data-ttu-id="50445-1352">メソッド tableTruncate</span><span class="sxs-lookup"><span data-stu-id="50445-1352">Method tableTruncate</span></span>

<span data-ttu-id="50445-1353">テーブルの切り詰め</span><span class="sxs-lookup"><span data-stu-id="50445-1353">Truncates the  table.</span></span>

    public int tableTruncate(TableId tableId, [boolean prompt_before_truncate], [boolean truncate_system_table])

#### <a name="parameters"></a><span data-ttu-id="50445-1354">パラメーター</span><span class="sxs-lookup"><span data-stu-id="50445-1354">Parameters</span></span>

<span data-ttu-id="50445-1355">tableId</span><span class="sxs-lookup"><span data-stu-id="50445-1355">tableId</span></span>  
<span data-ttu-id="50445-1356">選択したテーブルがシステム場合に、テーブルを切り詰めるかどうかを決定するブール フラグ; オプション。</span><span class="sxs-lookup"><span data-stu-id="50445-1356">A boolean flag that determines whether to truncate table in case if selected table is system; optional.</span></span> <span data-ttu-id="50445-1357">既定では、false です。</span><span class="sxs-lookup"><span data-stu-id="50445-1357">By default, false.</span></span>

<!-- -->

<span data-ttu-id="50445-1358">prompt\_before\_truncate</span><span class="sxs-lookup"><span data-stu-id="50445-1358">prompt\_before\_truncate</span></span>  
<span data-ttu-id="50445-1359">選択したテーブルがシステム場合に、テーブルを切り詰めるかどうかを決定するブール フラグ; オプション。</span><span class="sxs-lookup"><span data-stu-id="50445-1359">A boolean flag that determines whether to truncate table in case if selected table is system; optional.</span></span> <span data-ttu-id="50445-1360">既定では、false です。</span><span class="sxs-lookup"><span data-stu-id="50445-1360">By default, false.</span></span>

<!-- -->

<span data-ttu-id="50445-1361">truncate\_system\_table</span><span class="sxs-lookup"><span data-stu-id="50445-1361">truncate\_system\_table</span></span>  
<span data-ttu-id="50445-1362">選択したテーブルがシステム場合に、テーブルを切り詰めるかどうかを決定するブール フラグ; オプション。</span><span class="sxs-lookup"><span data-stu-id="50445-1362">A boolean flag that determines whether to truncate table in case if selected table is system; optional.</span></span> <span data-ttu-id="50445-1363">既定では、false です。</span><span class="sxs-lookup"><span data-stu-id="50445-1363">By default, false.</span></span>

#### <a name="return-value"></a><span data-ttu-id="50445-1364">戻り値</span><span class="sxs-lookup"><span data-stu-id="50445-1364">Return Value</span></span>

<span data-ttu-id="50445-1365">メソッドが成功した場合は 0。</span><span class="sxs-lookup"><span data-stu-id="50445-1365">Zero if the method succeeds.</span></span>

### <a name="method-tabletruncateddl"></a><span data-ttu-id="50445-1366">メソッド tableTruncateDDL</span><span class="sxs-lookup"><span data-stu-id="50445-1366">Method tableTruncateDDL</span></span>

<span data-ttu-id="50445-1367">テーブルを切り詰めるため SQL ステートメントを生成および返します。</span><span class="sxs-lookup"><span data-stu-id="50445-1367">Generates and returns a SQL statement to truncate a table.</span></span>

    public str tableTruncateDDL(TableId tableId)

#### <a name="parameters"></a><span data-ttu-id="50445-1368">パラメーター</span><span class="sxs-lookup"><span data-stu-id="50445-1368">Parameters</span></span>

<span data-ttu-id="50445-1369">tableId</span><span class="sxs-lookup"><span data-stu-id="50445-1369">tableId</span></span>  
<span data-ttu-id="50445-1370">切り詰めるテーブルのテーブル ハンドルです。</span><span class="sxs-lookup"><span data-stu-id="50445-1370">The table handle of the table to be truncated.</span></span>

#### <a name="return-value"></a><span data-ttu-id="50445-1371">戻り値</span><span class="sxs-lookup"><span data-stu-id="50445-1371">Return Value</span></span>

<span data-ttu-id="50445-1372">テーブルを切り詰める SQL ステートメント。</span><span class="sxs-lookup"><span data-stu-id="50445-1372">The SQL statement to truncate the table.</span></span>

### <a name="method-synchronize"></a><span data-ttu-id="50445-1373">メソッド synchronize</span><span class="sxs-lookup"><span data-stu-id="50445-1373">Method synchronize</span></span>

<span data-ttu-id="50445-1374">データ ディクショナリと、SQL データベースのデータ ディクショナリを同期します。</span><span class="sxs-lookup"><span data-stu-id="50445-1374">Synchronizes the  data dictionary and the data dictionary of the SQL database.</span></span>

    public static int synchronize([boolean synchronize_all])

#### <a name="parameters"></a><span data-ttu-id="50445-1375">パラメーター</span><span class="sxs-lookup"><span data-stu-id="50445-1375">Parameters</span></span>

<span data-ttu-id="50445-1376">synchronize\_all</span><span class="sxs-lookup"><span data-stu-id="50445-1376">synchronize\_all</span></span>  
<span data-ttu-id="50445-1377">すべてのテーブルを同期するかどうかを示すブール フラグ; オプション。</span><span class="sxs-lookup"><span data-stu-id="50445-1377">A boolean flag that determines whether to synchronize all tables; optional.</span></span> <span data-ttu-id="50445-1378">True の場合、このメソッドは (カーネルによって欠陥とマークされているテーブルのみでなく) すべてのテーブルを同期します。</span><span class="sxs-lookup"><span data-stu-id="50445-1378">If true, this method synchronizes all tables (instead of only those marked dirty by the  kernel).</span></span> <span data-ttu-id="50445-1379">既定では、false です。</span><span class="sxs-lookup"><span data-stu-id="50445-1379">By default, false.</span></span>

#### <a name="return-value"></a><span data-ttu-id="50445-1380">戻り値</span><span class="sxs-lookup"><span data-stu-id="50445-1380">Return Value</span></span>

<span data-ttu-id="50445-1381">同期が成功した場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="50445-1381">true if synchronization was successful; otherwise false.</span></span>

### <a name="method-new"></a><span data-ttu-id="50445-1382">メソッド new</span><span class="sxs-lookup"><span data-stu-id="50445-1382">Method new</span></span>

<span data-ttu-id="50445-1383">SqlDataDictionary クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="50445-1383">Initializes a new instance of the SqlDataDictionary class.</span></span>

    public void new()

### <a name="method-tabledelete"></a><span data-ttu-id="50445-1384">メソッド tableDelete</span><span class="sxs-lookup"><span data-stu-id="50445-1384">Method tableDelete</span></span>

<span data-ttu-id="50445-1385">SQL データベースでテーブルを削除します。</span><span class="sxs-lookup"><span data-stu-id="50445-1385">Deletes the  table in the SQL database.</span></span>

    public void tableDelete(TableId tableId)

#### <a name="parameters"></a><span data-ttu-id="50445-1386">パラメーター</span><span class="sxs-lookup"><span data-stu-id="50445-1386">Parameters</span></span>

<span data-ttu-id="50445-1387">tableId</span><span class="sxs-lookup"><span data-stu-id="50445-1387">tableId</span></span>  

## <a name="class-sqldatadictionarypermission"></a><span data-ttu-id="50445-1388">クラス SqlDataDictionaryPermission</span><span class="sxs-lookup"><span data-stu-id="50445-1388">Class SqlDataDictionaryPermission</span></span>
    class SqlDataDictionaryPermission extends CodeAccessPermission

<span data-ttu-id="50445-1389">SqlDataDictionaryPermission クラスは、メソッドにアクセスする機能を制御し、特定の API のアクセス許可を確認するように設計されています。</span><span class="sxs-lookup"><span data-stu-id="50445-1389">The SqlDataDictionaryPermission class controls the ability to access the methods on the and is designed to check permissions for specific APIs.</span></span> <span data-ttu-id="50445-1390">保護されたすべての API のリストについては、「セキュリティで保護された API」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="50445-1390">For a list of all protected APIs, see Secured APIs.</span></span>

### <a name="remarks"></a><span data-ttu-id="50445-1391">備考</span><span class="sxs-lookup"><span data-stu-id="50445-1391">Remarks</span></span>

<span data-ttu-id="50445-1392">保護された API が実行される前に、対応する CodeAccessPermission::demand メソッドが呼び出される、通常はサーバー層である、同じ層で assert メソッドを呼び出す必要があります。</span><span class="sxs-lookup"><span data-stu-id="50445-1392">You must call the assert method on the same tier, usually the server tier, that the corresponding CodeAccessPermission::demand method is called on before the protected API is executed.</span></span> <span data-ttu-id="50445-1393">次のいずれかでサーバー層のメソッドを呼び出します:</span><span class="sxs-lookup"><span data-stu-id="50445-1393">Call a method on the server tier from one of the following:</span></span>

-   <span data-ttu-id="50445-1394">サーバー静的メソッド</span><span class="sxs-lookup"><span data-stu-id="50445-1394">A server static method</span></span>
-   <span data-ttu-id="50445-1395">RunOn クラス プロパティを使用して、サーバーで実行するように設定されているクラス インスタンス メソッド。</span><span class="sxs-lookup"><span data-stu-id="50445-1395">A class instance method that is set to run on the server by using the RunOn class property.</span></span>

### <a name="examples"></a><span data-ttu-id="50445-1396">例</span><span class="sxs-lookup"><span data-stu-id="50445-1396">Examples</span></span>

<span data-ttu-id="50445-1397">次の例では、xRefNames テーブルからデータを削除します。</span><span class="sxs-lookup"><span data-stu-id="50445-1397">The following example deletes data from the xRefNames table.</span></span> <span data-ttu-id="50445-1398">assert メソッドが呼び出され、コードが、ファイルに対するデータの読み取り/書き込みを行うために使用される AsciiIo クラスをインスタンス化できることが宣言されます。</span><span class="sxs-lookup"><span data-stu-id="50445-1398">The assert method is called to declare that the code can then instantiate the AsciiIo class that is used to read and write data to a file.</span></span>

    { 
        DictTable dictTable = new DictTable(tablenum(xRefNames)); 
        str sqlTableName; 
        SqlDataDictionary sqlTable; 
        if (dictTable && dictTable.enabled()) 
        { 
            sqlTableName = dictTable.name(DbBackend::Sql); 
            sqlTable = new SqlDataDictionary(); 
            // Try to truncate only if the table does exist 
            // in the SQL database. 
            if (sqlTable.tableExist(sqlTableName)) 
            { 
                new SqlDataDictionaryPermission( 
                    methodstr(SqlDataDictionary, tableTruncate)).assert(); 
                sqlTable.tableTruncate(tablenum(xRefNames)); 
                CodeAccessPermission::revertAssert(); 
            } 
        } 
    }

### <a name="methods"></a><span data-ttu-id="50445-1399">メソッド</span><span class="sxs-lookup"><span data-stu-id="50445-1399">Methods</span></span>

| <span data-ttu-id="50445-1400">方法</span><span class="sxs-lookup"><span data-stu-id="50445-1400">Method</span></span>                                                 | <span data-ttu-id="50445-1401">説明</span><span class="sxs-lookup"><span data-stu-id="50445-1401">Description</span></span>                                                                      |
|--------------------------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="50445-1402">public CodeAccessPermission copy()</span><span class="sxs-lookup"><span data-stu-id="50445-1402">public CodeAccessPermission copy()</span></span>                     | <span data-ttu-id="50445-1403">現在のアクセス許可クラス オブジェクトのコピーを作成し、返します。</span><span class="sxs-lookup"><span data-stu-id="50445-1403">Creates and returns a copy of the current permission class object.</span></span>               |
| <span data-ttu-id="50445-1404">public boolean isSubsetOf(CodeAccessPermission target)</span><span class="sxs-lookup"><span data-stu-id="50445-1404">public boolean isSubsetOf(CodeAccessPermission target)</span></span> | <span data-ttu-id="50445-1405">現在のアクセス許可が指定したアクセス許可のサブセットかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="50445-1405">Determines whether a current permission is a subset of the specified permission.</span></span> |
| <span data-ttu-id="50445-1406">public void new(IdentifierName methodName)</span><span class="sxs-lookup"><span data-stu-id="50445-1406">public void new(IdentifierName methodName)</span></span>             | <span data-ttu-id="50445-1407">SQLDataDictionaryPermission クラスの新しいインスタンスを作成します。</span><span class="sxs-lookup"><span data-stu-id="50445-1407">Creates a new instance of the SQLDataDictionaryPermission class.</span></span>                 |

### <a name="method-copy"></a><span data-ttu-id="50445-1408">メソッド copy</span><span class="sxs-lookup"><span data-stu-id="50445-1408">Method copy</span></span>

<span data-ttu-id="50445-1409">現在のアクセス許可クラス オブジェクトのコピーを作成し、返します。</span><span class="sxs-lookup"><span data-stu-id="50445-1409">Creates and returns a copy of the current permission class object.</span></span>

    public CodeAccessPermission copy()

#### <a name="return-value"></a><span data-ttu-id="50445-1410">戻り値</span><span class="sxs-lookup"><span data-stu-id="50445-1410">Return Value</span></span>

<span data-ttu-id="50445-1411">現在のアクセス許可オブジェクトのコピーです。</span><span class="sxs-lookup"><span data-stu-id="50445-1411">A copy of the current permission object.</span></span>

#### <a name="remarks"></a><span data-ttu-id="50445-1412">備考</span><span class="sxs-lookup"><span data-stu-id="50445-1412">Remarks</span></span>

<span data-ttu-id="50445-1413">CodeAccessPermission クラスからクラスを派生させる場合に、このメソッドを上書きします。</span><span class="sxs-lookup"><span data-stu-id="50445-1413">You override this method when you derive a class from the CodeAccessPermission class.</span></span> <span data-ttu-id="50445-1414">詳細については、「」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="50445-1414">For more information, see .</span></span>

### <a name="method-issubsetof"></a><span data-ttu-id="50445-1415">メソッド isSubsetOf</span><span class="sxs-lookup"><span data-stu-id="50445-1415">Method isSubsetOf</span></span>

<span data-ttu-id="50445-1416">現在のアクセス許可が指定したアクセス許可のサブセットかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="50445-1416">Determines whether a current permission is a subset of the specified permission.</span></span>

    public boolean isSubsetOf(CodeAccessPermission target)

#### <a name="parameters"></a><span data-ttu-id="50445-1417">パラメーター</span><span class="sxs-lookup"><span data-stu-id="50445-1417">Parameters</span></span>

<span data-ttu-id="50445-1418">target</span><span class="sxs-lookup"><span data-stu-id="50445-1418">target</span></span>  
<span data-ttu-id="50445-1419">CodeAccessPermission クラス オブジェクト。</span><span class="sxs-lookup"><span data-stu-id="50445-1419">A CodeAccessPermission class object.</span></span>

#### <a name="return-value"></a><span data-ttu-id="50445-1420">戻り値</span><span class="sxs-lookup"><span data-stu-id="50445-1420">Return Value</span></span>

<span data-ttu-id="50445-1421">現在のアクセス許可が指定したアクセス許可のサブセットである場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="50445-1421">true if a current permission is a subset of a specified permission; otherwise, false.</span></span>

#### <a name="remarks"></a><span data-ttu-id="50445-1422">備考</span><span class="sxs-lookup"><span data-stu-id="50445-1422">Remarks</span></span>

<span data-ttu-id="50445-1423">CodeAccessPermission クラスからクラスを派生させる場合に、このメソッドを上書きします。</span><span class="sxs-lookup"><span data-stu-id="50445-1423">You override this method when you derive a class from the CodeAccessPermission class.</span></span> <span data-ttu-id="50445-1424">詳細については、「」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="50445-1424">For more information, see .</span></span>

### <a name="method-new"></a><span data-ttu-id="50445-1425">メソッド new</span><span class="sxs-lookup"><span data-stu-id="50445-1425">Method new</span></span>

<span data-ttu-id="50445-1426">SQLDataDictionaryPermission クラスの新しいインスタンスを作成します。</span><span class="sxs-lookup"><span data-stu-id="50445-1426">Creates a new instance of the SQLDataDictionaryPermission class.</span></span>

    public void new(IdentifierName methodName)

#### <a name="parameters"></a><span data-ttu-id="50445-1427">パラメーター</span><span class="sxs-lookup"><span data-stu-id="50445-1427">Parameters</span></span>

<span data-ttu-id="50445-1428">methodName</span><span class="sxs-lookup"><span data-stu-id="50445-1428">methodName</span></span>  
<span data-ttu-id="50445-1429">呼び出されるメソッドの名前を表す文字列。</span><span class="sxs-lookup"><span data-stu-id="50445-1429">The string that represents the name of the method to be called.</span></span>

#### <a name="examples"></a><span data-ttu-id="50445-1430">例</span><span class="sxs-lookup"><span data-stu-id="50445-1430">Examples</span></span>

<span data-ttu-id="50445-1431">次のコード例は、xRefNames テーブルのデータを削除します。</span><span class="sxs-lookup"><span data-stu-id="50445-1431">The following code example deletes the data in the xRefNames table.</span></span>

    server static void main(Args _args) 
    { 
        DictTable dictTable = new DictTable(tablenum(xRefNames)); 
        str sqlTableName; 
        SqlDataDictionary sqlTable; 
        if (dictTable && dictTable.enabled()) 
        { 
            sqlTableName = dictTable.name(DbBackend::Sql); 
            sqlTable = new SqlDataDictionary(); 
            // Only try to truncate if the table does exist 
            // in the SQL database 
            if (sqlTable.tableExist(sqlTableName)) 
            { 
                new SqlDataDictionaryPermission( 
                    methodstr(SqlDataDictionary, tableTruncate)).assert(); 
                sqlTable.tableTruncate(tablenum(xRefNames)); 
                CodeAccessPermission::revertAssert(); 
            } 
        } 
    }

## <a name="class-sqlstatementexecutepermission"></a><span data-ttu-id="50445-1432">クラス SqlStatementExecutePermission</span><span class="sxs-lookup"><span data-stu-id="50445-1432">Class SqlStatementExecutePermission</span></span>
    class SqlStatementExecutePermission extends CodeAccessPermission

<span data-ttu-id="50445-1433">SQL を使用する機能をコントロールします。</span><span class="sxs-lookup"><span data-stu-id="50445-1433">Controls the ability to use SQL.</span></span>

### <a name="remarks"></a><span data-ttu-id="50445-1434">備考</span><span class="sxs-lookup"><span data-stu-id="50445-1434">Remarks</span></span>

<span data-ttu-id="50445-1435">このクラスは、特定の API のアクセス許可をチェックするように設計されています。</span><span class="sxs-lookup"><span data-stu-id="50445-1435">This class is designed to check permissions for specific APIs.</span></span> <span data-ttu-id="50445-1436">保護されたすべての API のリストについては、「セキュリティで保護された API」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="50445-1436">For a list of all protected APIs, see Secured APIs.</span></span> <span data-ttu-id="50445-1437">保護された API が実行される前に、対応する CodeAccessPermission::demand メソッドが呼び出される、通常はサーバー層である、同じ層で assert メソッドを呼び出す必要があります。</span><span class="sxs-lookup"><span data-stu-id="50445-1437">You must call the assert method on the same tier, usually the server tier, that the corresponding CodeAccessPermission::demand method is called on before the protected API is executed.</span></span> <span data-ttu-id="50445-1438">次のいずれかでサーバー層のメソッドを呼び出します:</span><span class="sxs-lookup"><span data-stu-id="50445-1438">Call a method on the server tier from one of the following:</span></span>

-   <span data-ttu-id="50445-1439">サーバー静的メソッドまたは</span><span class="sxs-lookup"><span data-stu-id="50445-1439">A server static method –or–</span></span>
-   <span data-ttu-id="50445-1440">RunOn クラス プロパティを使用して、サーバーで実行するように設定されているクラス インスタンス メソッド</span><span class="sxs-lookup"><span data-stu-id="50445-1440">A class instance method that is set to run on the server by using the RunOn class property</span></span>

### <a name="examples"></a><span data-ttu-id="50445-1441">例</span><span class="sxs-lookup"><span data-stu-id="50445-1441">Examples</span></span>

<span data-ttu-id="50445-1442">この例では、サーバー上で実行される CustTable テーブルで SQL クエリを実行します。</span><span class="sxs-lookup"><span data-stu-id="50445-1442">This example performs an SQL query on the CustTable table, which runs on the server.</span></span> <span data-ttu-id="50445-1443">クエリの結果は、\_resultSet オブジェクトに格納されます。</span><span class="sxs-lookup"><span data-stu-id="50445-1443">The result of the query is stored in the \_resultSet object.</span></span> <span data-ttu-id="50445-1444">assert メソッドが呼び出され、コードが、ファイルに対するデータの読み取り/書き込みを行うために使用される AsciiIo クラスをインスタンス化できることが宣言されます。</span><span class="sxs-lookup"><span data-stu-id="50445-1444">The assert method is called to declare that the code can then instantiate the AsciiIo class that is used to read and write data to a file.</span></span>

    server static void main(Args _args) 
    { 
        DictTable  _dictTable; 
        Connection _connection; 
        Statement  _statement; 
        str        _sql; 
        ResultSet  _resultSet; 
        SqlStatementExecutePermission _perm; 
        _dictTable = new DictTable(tableNum(CustTable)); 
        if (_dictTable != null) 
            { 
               _connection = new Connection(); 
               _sql = strfmt( "SELECT * FROM %1", _dictTable.name(DbBackend::Sql) ); 
               _perm = new SqlStatementExecutePermission(_sql); 
               // Check for permission to use the _statement. 
               _perm.assert(); 
               _statement = _connection.createStatement(); 
               _resultSet = _statement.executeQuery(_sql); 
               // End the scope of the assert call. 
               CodeAccessPermission::revertAssert(); 
            } 
    }

### <a name="methods"></a><span data-ttu-id="50445-1445">メソッド</span><span class="sxs-lookup"><span data-stu-id="50445-1445">Methods</span></span>

| <span data-ttu-id="50445-1446">方法</span><span class="sxs-lookup"><span data-stu-id="50445-1446">Method</span></span>                                                 | <span data-ttu-id="50445-1447">説明</span><span class="sxs-lookup"><span data-stu-id="50445-1447">Description</span></span>                                                                      |
|--------------------------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="50445-1448">public CodeAccessPermission copy()</span><span class="sxs-lookup"><span data-stu-id="50445-1448">public CodeAccessPermission copy()</span></span>                     | <span data-ttu-id="50445-1449">現在のアクセス許可クラス オブジェクトのコピーを作成し、返します。</span><span class="sxs-lookup"><span data-stu-id="50445-1449">Creates and returns a copy of the current permission class object.</span></span>               |
| <span data-ttu-id="50445-1450">public boolean isSubsetOf(CodeAccessPermission target)</span><span class="sxs-lookup"><span data-stu-id="50445-1450">public boolean isSubsetOf(CodeAccessPermission target)</span></span> | <span data-ttu-id="50445-1451">現在のアクセス許可が指定したアクセス許可のサブセットかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="50445-1451">Determines whether a current permission is a subset of the specified permission.</span></span> |
| <span data-ttu-id="50445-1452">public void new(str sqlStatement)</span><span class="sxs-lookup"><span data-stu-id="50445-1452">public void new(str sqlStatement)</span></span>                      | <span data-ttu-id="50445-1453">SQLStatementExecutePermission クラスの新しいインスタンスを作成します。</span><span class="sxs-lookup"><span data-stu-id="50445-1453">Creates a new instance of the SQLStatementExecutePermission class.</span></span>               |

### <a name="method-copy"></a><span data-ttu-id="50445-1454">メソッド copy</span><span class="sxs-lookup"><span data-stu-id="50445-1454">Method copy</span></span>

<span data-ttu-id="50445-1455">現在のアクセス許可クラス オブジェクトのコピーを作成し、返します。</span><span class="sxs-lookup"><span data-stu-id="50445-1455">Creates and returns a copy of the current permission class object.</span></span>

    public CodeAccessPermission copy()

#### <a name="return-value"></a><span data-ttu-id="50445-1456">戻り値</span><span class="sxs-lookup"><span data-stu-id="50445-1456">Return Value</span></span>

<span data-ttu-id="50445-1457">現在のアクセス許可オブジェクトのコピーです。</span><span class="sxs-lookup"><span data-stu-id="50445-1457">A copy of the current permission object.</span></span>

#### <a name="remarks"></a><span data-ttu-id="50445-1458">備考</span><span class="sxs-lookup"><span data-stu-id="50445-1458">Remarks</span></span>

<span data-ttu-id="50445-1459">CodeAccessPermission クラスからクラスを派生させる場合に、このメソッドを上書きします。</span><span class="sxs-lookup"><span data-stu-id="50445-1459">You override this method when you derive a class from the CodeAccessPermission class.</span></span> <span data-ttu-id="50445-1460">詳細については、「」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="50445-1460">For more information, see .</span></span>

### <a name="method-issubsetof"></a><span data-ttu-id="50445-1461">メソッド isSubsetOf</span><span class="sxs-lookup"><span data-stu-id="50445-1461">Method isSubsetOf</span></span>

<span data-ttu-id="50445-1462">現在のアクセス許可が指定したアクセス許可のサブセットかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="50445-1462">Determines whether a current permission is a subset of the specified permission.</span></span>

    public boolean isSubsetOf(CodeAccessPermission target)

#### <a name="parameters"></a><span data-ttu-id="50445-1463">パラメーター</span><span class="sxs-lookup"><span data-stu-id="50445-1463">Parameters</span></span>

<span data-ttu-id="50445-1464">target</span><span class="sxs-lookup"><span data-stu-id="50445-1464">target</span></span>  
<span data-ttu-id="50445-1465">CodeAccessPermission クラス オブジェクト。</span><span class="sxs-lookup"><span data-stu-id="50445-1465">A CodeAccessPermission class object.</span></span>

#### <a name="return-value"></a><span data-ttu-id="50445-1466">戻り値</span><span class="sxs-lookup"><span data-stu-id="50445-1466">Return Value</span></span>

<span data-ttu-id="50445-1467">現在のアクセス許可が指定したアクセス許可のサブセットである場合は true。それ以外の場合は false。</span><span class="sxs-lookup"><span data-stu-id="50445-1467">true if a current permission is a subset of a specified permission; otherwise false.</span></span>

#### <a name="remarks"></a><span data-ttu-id="50445-1468">備考</span><span class="sxs-lookup"><span data-stu-id="50445-1468">Remarks</span></span>

<span data-ttu-id="50445-1469">CodeAccessPermission クラスからクラスを派生させる場合に、このメソッドを上書きします。</span><span class="sxs-lookup"><span data-stu-id="50445-1469">You override this method when you derive a class from the CodeAccessPermission class.</span></span> <span data-ttu-id="50445-1470">詳細については、「」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="50445-1470">For more information, see .</span></span>

### <a name="method-new"></a><span data-ttu-id="50445-1471">メソッド new</span><span class="sxs-lookup"><span data-stu-id="50445-1471">Method new</span></span>

<span data-ttu-id="50445-1472">SQLStatementExecutePermission クラスの新しいインスタンスを作成します。</span><span class="sxs-lookup"><span data-stu-id="50445-1472">Creates a new instance of the SQLStatementExecutePermission class.</span></span>

    public void new(str sqlStatement)

#### <a name="parameters"></a><span data-ttu-id="50445-1473">パラメーター</span><span class="sxs-lookup"><span data-stu-id="50445-1473">Parameters</span></span>

<span data-ttu-id="50445-1474">sqlStatement</span><span class="sxs-lookup"><span data-stu-id="50445-1474">sqlStatement</span></span>  
<span data-ttu-id="50445-1475">実行する SQL 文字列。</span><span class="sxs-lookup"><span data-stu-id="50445-1475">The SQL string to be executed.</span></span>

#### <a name="examples"></a><span data-ttu-id="50445-1476">例</span><span class="sxs-lookup"><span data-stu-id="50445-1476">Examples</span></span>

<span data-ttu-id="50445-1477">次の例では、サーバー上で実行される、CustTable テーブルで SQL クエリを実行します。</span><span class="sxs-lookup"><span data-stu-id="50445-1477">The following example performs an SQL query on the CustTable table, which runs on the server.</span></span> <span data-ttu-id="50445-1478">クエリの結果は、resultSet オブジェクトに格納されます。</span><span class="sxs-lookup"><span data-stu-id="50445-1478">The result of the query is stored in the resultSet object.</span></span>

    server static void main(Args _args) 
    { 
        DictTable  dictTable; 
        Connection connection; 
        Statement  statement; 
        str        sql; 
        ResultSet  resultSet; 
        SqlStatementExecutePermission perm; 
        dictTable = new DictTable(tableNum(CustTable)); 
        if (dictTable != null) 
            { 
               connection = new Connection(); 
               sql = strfmt( "SELECT * FROM %1", dictTable.name(DbBackend::Sql) ); 
               //Instantiate the permission class 
               perm = new SqlStatementExecutePermission(sql); 
               //check for permission to use statement 
               perm.assert(); 
               statement = connection.createStatement(); 
               resultSet = statement.executeQuery(sql); 
               //end the scope of the assert call 
               CodeAccessPermission::revertAssert(); 
            } 
    }

## <a name="class-sqlsyncpending"></a><span data-ttu-id="50445-1479">クラス SqlSyncPending</span><span class="sxs-lookup"><span data-stu-id="50445-1479">Class SqlSyncPending</span></span>
    class SqlSyncPending extends Object

### <a name="remarks"></a><span data-ttu-id="50445-1480">備考</span><span class="sxs-lookup"><span data-stu-id="50445-1480">Remarks</span></span>

### <a name="examples"></a><span data-ttu-id="50445-1481">例</span><span class="sxs-lookup"><span data-stu-id="50445-1481">Examples</span></span>

### <a name="methods"></a><span data-ttu-id="50445-1482">メソッド</span><span class="sxs-lookup"><span data-stu-id="50445-1482">Methods</span></span>

| <span data-ttu-id="50445-1483">方法</span><span class="sxs-lookup"><span data-stu-id="50445-1483">Method</span></span>                                               | <span data-ttu-id="50445-1484">説明</span><span class="sxs-lookup"><span data-stu-id="50445-1484">Description</span></span>                                             |
|------------------------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="50445-1485">public ConfigurationKeyId configurationKeyTouched()</span><span class="sxs-lookup"><span data-stu-id="50445-1485">public ConfigurationKeyId configurationKeyTouched()</span></span>  |                                                         |
| <span data-ttu-id="50445-1486">public boolean databaseTouched(\[boolean newValue\])</span><span class="sxs-lookup"><span data-stu-id="50445-1486">public boolean databaseTouched(\[boolean newValue\])</span></span> |                                                         |
| <span data-ttu-id="50445-1487">public ExtendedTypeId extendedDataTypeTouched()</span><span class="sxs-lookup"><span data-stu-id="50445-1487">public ExtendedTypeId extendedDataTypeTouched()</span></span>      |                                                         |
| <span data-ttu-id="50445-1488">public TableId indexesTouched()</span><span class="sxs-lookup"><span data-stu-id="50445-1488">public TableId indexesTouched()</span></span>                      |                                                         |
| <span data-ttu-id="50445-1489">public TableId relationTouched()</span><span class="sxs-lookup"><span data-stu-id="50445-1489">public TableId relationTouched()</span></span>                     |                                                         |
| <span data-ttu-id="50445-1490">public TableId tableDeleted()</span><span class="sxs-lookup"><span data-stu-id="50445-1490">public TableId tableDeleted()</span></span>                        |                                                         |
| <span data-ttu-id="50445-1491">public TableId tableTouched()</span><span class="sxs-lookup"><span data-stu-id="50445-1491">public TableId tableTouched()</span></span>                        |                                                         |
| <span data-ttu-id="50445-1492">public void new()</span><span class="sxs-lookup"><span data-stu-id="50445-1492">public void new()</span></span>                                    | <span data-ttu-id="50445-1493">SqlSyncPending クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="50445-1493">Initializes a new instance of the SqlSyncPending class.</span></span> |

### <a name="method-configurationkeytouched"></a><span data-ttu-id="50445-1494">メソッド configurationKeyTouched</span><span class="sxs-lookup"><span data-stu-id="50445-1494">Method configurationKeyTouched</span></span>

    public ConfigurationKeyId configurationKeyTouched()

#### <a name="return-value"></a><span data-ttu-id="50445-1495">戻り値</span><span class="sxs-lookup"><span data-stu-id="50445-1495">Return Value</span></span>

### <a name="method-databasetouched"></a><span data-ttu-id="50445-1496">メソッド databaseTouched</span><span class="sxs-lookup"><span data-stu-id="50445-1496">Method databaseTouched</span></span>

    public boolean databaseTouched([boolean newValue])

#### <a name="parameters"></a><span data-ttu-id="50445-1497">パラメーター</span><span class="sxs-lookup"><span data-stu-id="50445-1497">Parameters</span></span>

<span data-ttu-id="50445-1498">newValue</span><span class="sxs-lookup"><span data-stu-id="50445-1498">newValue</span></span>  

#### <a name="return-value"></a><span data-ttu-id="50445-1499">戻り値</span><span class="sxs-lookup"><span data-stu-id="50445-1499">Return Value</span></span>

### <a name="method-extendeddatatypetouched"></a><span data-ttu-id="50445-1500">メソッド extendedDataTypeTouched</span><span class="sxs-lookup"><span data-stu-id="50445-1500">Method extendedDataTypeTouched</span></span>

    public ExtendedTypeId extendedDataTypeTouched()

#### <a name="return-value"></a><span data-ttu-id="50445-1501">戻り値</span><span class="sxs-lookup"><span data-stu-id="50445-1501">Return Value</span></span>

### <a name="method-indexestouched"></a><span data-ttu-id="50445-1502">メソッド indexesTouched</span><span class="sxs-lookup"><span data-stu-id="50445-1502">Method indexesTouched</span></span>

    public TableId indexesTouched()

#### <a name="return-value"></a><span data-ttu-id="50445-1503">戻り値</span><span class="sxs-lookup"><span data-stu-id="50445-1503">Return Value</span></span>

### <a name="method-relationtouched"></a><span data-ttu-id="50445-1504">メソッド relationTouched</span><span class="sxs-lookup"><span data-stu-id="50445-1504">Method relationTouched</span></span>

    public TableId relationTouched()

#### <a name="return-value"></a><span data-ttu-id="50445-1505">戻り値</span><span class="sxs-lookup"><span data-stu-id="50445-1505">Return Value</span></span>

### <a name="method-tabledeleted"></a><span data-ttu-id="50445-1506">メソッド tableDeleted</span><span class="sxs-lookup"><span data-stu-id="50445-1506">Method tableDeleted</span></span>

    public TableId tableDeleted()

#### <a name="return-value"></a><span data-ttu-id="50445-1507">戻り値</span><span class="sxs-lookup"><span data-stu-id="50445-1507">Return Value</span></span>

### <a name="method-tabletouched"></a><span data-ttu-id="50445-1508">メソッド tableTouched</span><span class="sxs-lookup"><span data-stu-id="50445-1508">Method tableTouched</span></span>

    public TableId tableTouched()

#### <a name="return-value"></a><span data-ttu-id="50445-1509">戻り値</span><span class="sxs-lookup"><span data-stu-id="50445-1509">Return Value</span></span>

### <a name="method-new"></a><span data-ttu-id="50445-1510">メソッド new</span><span class="sxs-lookup"><span data-stu-id="50445-1510">Method new</span></span>

<span data-ttu-id="50445-1511">SqlSyncPending クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="50445-1511">Initializes a new instance of the SqlSyncPending class.</span></span>

    public void new()

## <a name="class-sqlsystem"></a><span data-ttu-id="50445-1512">クラス SqlSystem</span><span class="sxs-lookup"><span data-stu-id="50445-1512">Class SqlSystem</span></span>
    class SqlSystem extends Object

<span data-ttu-id="50445-1513">SqlSystem クラスには、有効な SQL システムに関する情報 (通常はログイン情報) が含まれます。</span><span class="sxs-lookup"><span data-stu-id="50445-1513">The SqlSystem class holds information about the active SQL system, typically login information.</span></span>

### <a name="remarks"></a><span data-ttu-id="50445-1514">備考</span><span class="sxs-lookup"><span data-stu-id="50445-1514">Remarks</span></span>

### <a name="examples"></a><span data-ttu-id="50445-1515">例</span><span class="sxs-lookup"><span data-stu-id="50445-1515">Examples</span></span>

### <a name="methods"></a><span data-ttu-id="50445-1516">メソッド</span><span class="sxs-lookup"><span data-stu-id="50445-1516">Methods</span></span>

| <span data-ttu-id="50445-1517">方法</span><span class="sxs-lookup"><span data-stu-id="50445-1517">Method</span></span>                                                                                                                                   | <span data-ttu-id="50445-1518">説明</span><span class="sxs-lookup"><span data-stu-id="50445-1518">Description</span></span>                                                                                             |
|------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="50445-1519">public LoginProperty createLoginProperty()</span><span class="sxs-lookup"><span data-stu-id="50445-1519">public LoginProperty createLoginProperty()</span></span>                                                                                               | <span data-ttu-id="50445-1520">データベースにログイン プロパティを作成します。</span><span class="sxs-lookup"><span data-stu-id="50445-1520">Creates the login property to the  database.</span></span>                                       |
| <span data-ttu-id="50445-1521">public DatabaseId databaseId()</span><span class="sxs-lookup"><span data-stu-id="50445-1521">public DatabaseId databaseId()</span></span>                                                                                                           | <span data-ttu-id="50445-1522">SQL データベースのバックエンドとして使用されるデータベースの仕入先の ID を返します。</span><span class="sxs-lookup"><span data-stu-id="50445-1522">Returns the  ID for the database vendor used as the SQL database backend.</span></span>          |
| <span data-ttu-id="50445-1523">public str databaseName()</span><span class="sxs-lookup"><span data-stu-id="50445-1523">public str databaseName()</span></span>                                                                                                                | <span data-ttu-id="50445-1524">SQL データベースのバックエンドとして使用されるデータベースの仕入先の名前を返します。</span><span class="sxs-lookup"><span data-stu-id="50445-1524">Returns the name of the database vendor used as the SQL database backend.</span></span>                               |
| <span data-ttu-id="50445-1525">public boolean dbRequestedUnicodeEnabled()</span><span class="sxs-lookup"><span data-stu-id="50445-1525">public boolean dbRequestedUnicodeEnabled()</span></span>                                                                                               | <span data-ttu-id="50445-1526">Unicode がデータベースでサポートされているかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="50445-1526">Retrieves the value that indicates if Unicode is supported in the database.</span></span>                             |
| <span data-ttu-id="50445-1527">public str filenameDeadlocks(str Userid)</span><span class="sxs-lookup"><span data-stu-id="50445-1527">public str filenameDeadlocks(str Userid)</span></span>                                                                                                 | <span data-ttu-id="50445-1528">デッドロックのトレース ログ ファイルに固有のユーザーの名前を取得します。</span><span class="sxs-lookup"><span data-stu-id="50445-1528">Retrieves the name of the user specific deadlocks trace logfile.</span></span>                                        |
| <span data-ttu-id="50445-1529">public str filenameQuerytimelimit(str Userid)</span><span class="sxs-lookup"><span data-stu-id="50445-1529">public str filenameQuerytimelimit(str Userid)</span></span>                                                                                            | <span data-ttu-id="50445-1530">ユーザー固有の querytime 期限ログ ファイルの名前を取得します。</span><span class="sxs-lookup"><span data-stu-id="50445-1530">Retrieves the name of the user specific querytime limit logfile.</span></span>                                        |
| <span data-ttu-id="50445-1531">public str filenameSqlTrace(str Userid)</span><span class="sxs-lookup"><span data-stu-id="50445-1531">public str filenameSqlTrace(str Userid)</span></span>                                                                                                  | <span data-ttu-id="50445-1532">特定のユーザーの SQL トレース ログ ファイルのファイル名を取得します。</span><span class="sxs-lookup"><span data-stu-id="50445-1532">Retrieves the filename of the SQL trace log file for specific user.</span></span>                                     |
| <span data-ttu-id="50445-1533">public str filenameWarnings(str Userid)</span><span class="sxs-lookup"><span data-stu-id="50445-1533">public str filenameWarnings(str Userid)</span></span>                                                                                                  | <span data-ttu-id="50445-1534">警告ログ ファイルに固有のユーザーの名前を取得します。</span><span class="sxs-lookup"><span data-stu-id="50445-1534">Retrieves the name of the user specific warnings log file.</span></span>                                              |
| <span data-ttu-id="50445-1535">public str logfileName(\[boolean fromCommandline\])</span><span class="sxs-lookup"><span data-stu-id="50445-1535">public str logfileName(\[boolean fromCommandline\])</span></span>                                                                                      | <span data-ttu-id="50445-1536">標準的な SQL エラー ログ ファイルの名前を取得します。</span><span class="sxs-lookup"><span data-stu-id="50445-1536">Retrieves the name of the standard  SQL error log file.</span></span>                            |
| <span data-ttu-id="50445-1537">public str loginConnectString()</span><span class="sxs-lookup"><span data-stu-id="50445-1537">public str loginConnectString()</span></span>                                                                                                          | <span data-ttu-id="50445-1538">ODBC の完全な接続文字列を取得します。</span><span class="sxs-lookup"><span data-stu-id="50445-1538">Retrieves the full ODBC connection string.</span></span>                                                              |
| <span data-ttu-id="50445-1539">public str loginDatabase()</span><span class="sxs-lookup"><span data-stu-id="50445-1539">public str loginDatabase()</span></span>                                                                                                               | <span data-ttu-id="50445-1540">現在接続されているデータベースの名前を取得します。</span><span class="sxs-lookup"><span data-stu-id="50445-1540">Retrieves the name of the database currently connected to.</span></span>                                              |
| <span data-ttu-id="50445-1541">public str loginDSN()</span><span class="sxs-lookup"><span data-stu-id="50445-1541">public str loginDSN()</span></span>                                                                                                                    | <span data-ttu-id="50445-1542">データベースに接続するために使用される Open Database Connectivity (ODBC) データ ソース名 (DSN) を取得します。</span><span class="sxs-lookup"><span data-stu-id="50445-1542">Retrieves the open database connectivity (ODBC) data source name (DSN) used to connect to the database.</span></span> |
| <span data-ttu-id="50445-1543">public str loginName()</span><span class="sxs-lookup"><span data-stu-id="50445-1543">public str loginName()</span></span>                                                                                                                   | <span data-ttu-id="50445-1544">データベースにログインするために使用されるユーザー名を取得します。</span><span class="sxs-lookup"><span data-stu-id="50445-1544">Retrieves the user name that is used to log-in to the database.</span></span>                                         |
| <span data-ttu-id="50445-1545">public str loginServer()</span><span class="sxs-lookup"><span data-stu-id="50445-1545">public str loginServer()</span></span>                                                                                                                 | <span data-ttu-id="50445-1546">現在接続されているデータベース サーバーの名前を取得します。</span><span class="sxs-lookup"><span data-stu-id="50445-1546">Retrieves the name of the database server currently connected to.</span></span>                                       |
| <span data-ttu-id="50445-1547">public str monocaseFmt(\[TableId tableId\], \[FieldId fieldId\], \[boolean includingFieldName\], \[boolean considerSystemVariables\])</span><span class="sxs-lookup"><span data-stu-id="50445-1547">public str monocaseFmt(\[TableId tableId\], \[FieldId fieldId\], \[boolean includingFieldName\], \[boolean considerSystemVariables\])</span></span>    | <span data-ttu-id="50445-1548">文字列を 1 つのケースにキャストするために使用される書式文字列を取得します ("NLS\_LOWER(%1)" など)。</span><span class="sxs-lookup"><span data-stu-id="50445-1548">Retrieves the format string that is used for casting the string to one case (e.g. "NLS\_LOWER(%1)").</span></span>    |
| <span data-ttu-id="50445-1549">public str sqlLiteral(AnyType data, \[boolean forWhereClause\], \[boolean likeOperand\], \[boolean rightJustify\], \[int stringLength\])</span><span class="sxs-lookup"><span data-stu-id="50445-1549">public str sqlLiteral(AnyType data, \[boolean forWhereClause\], \[boolean likeOperand\], \[boolean rightJustify\], \[int stringLength\])</span></span> | <span data-ttu-id="50445-1550">SQL タイプを修正するため入力 AX データ型を書式設定します。</span><span class="sxs-lookup"><span data-stu-id="50445-1550">Formats the input AX datatype to correct SQL type.</span></span>                                                      |
| <span data-ttu-id="50445-1551">::public static boolean clusteredIndexes()</span><span class="sxs-lookup"><span data-stu-id="50445-1551">::public static boolean clusteredIndexes()</span></span>                                                                                               |                                                                                                         |
| <span data-ttu-id="50445-1552">::public static str databaseBackendDesc()</span><span class="sxs-lookup"><span data-stu-id="50445-1552">::public static str databaseBackendDesc()</span></span>                                                                                                |                                                                                                         |
| <span data-ttu-id="50445-1553">::public static DatabaseId databaseBackendId()</span><span class="sxs-lookup"><span data-stu-id="50445-1553">::public static DatabaseId databaseBackendId()</span></span>                                                                                           |                                                                                                         |
| <span data-ttu-id="50445-1554">::public static str databaseBackendName()</span><span class="sxs-lookup"><span data-stu-id="50445-1554">::public static str databaseBackendName()</span></span>                                                                                                |                                                                                                         |
| <span data-ttu-id="50445-1555">::public static DatabaseCLI databaseCallLevelInterface()</span><span class="sxs-lookup"><span data-stu-id="50445-1555">::public static DatabaseCLI databaseCallLevelInterface()</span></span>                                                                                 |                                                                                                         |
| <span data-ttu-id="50445-1556">::public static int databaseHints(\[int new\_hint\_value\])</span><span class="sxs-lookup"><span data-stu-id="50445-1556">::public static int databaseHints(\[int new\_hint\_value\])</span></span>                                                                              |                                                                                                         |
| <span data-ttu-id="50445-1557">::public static boolean functionalIndexes()</span><span class="sxs-lookup"><span data-stu-id="50445-1557">::public static boolean functionalIndexes()</span></span>                                                                                              |                                                                                                         |
| <span data-ttu-id="50445-1558">::public static str modelDatabaseBackendName()</span><span class="sxs-lookup"><span data-stu-id="50445-1558">::public static str modelDatabaseBackendName()</span></span>                                                                                           | <span data-ttu-id="50445-1559">現在接続されているモデル データベース AOS の名前を取得します。</span><span class="sxs-lookup"><span data-stu-id="50445-1559">Retrieves the name of the model database AOS currently connected to.</span></span>                                    |
| <span data-ttu-id="50445-1560">::public static str managedConnectionString()</span><span class="sxs-lookup"><span data-stu-id="50445-1560">::public static str managedConnectionString()</span></span>                                                                                            |                                                                                                         |
| <span data-ttu-id="50445-1561">public void new()</span><span class="sxs-lookup"><span data-stu-id="50445-1561">public void new()</span></span>                                                                                                                        | <span data-ttu-id="50445-1562">SqlSystem クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="50445-1562">Initializes a new instance of the SqlSystem class.</span></span>                                                      |
| <span data-ttu-id="50445-1563">public void logfileWrite(str Text)</span><span class="sxs-lookup"><span data-stu-id="50445-1563">public void logfileWrite(str Text)</span></span>                                                                                                       | <span data-ttu-id="50445-1564">テキスト文字列を標準 SQL エラー ログファイルに記述します。</span><span class="sxs-lookup"><span data-stu-id="50445-1564">Writes a text string into the standard  SQL error logfile.</span></span>                         |

### <a name="method-createloginproperty"></a><span data-ttu-id="50445-1565">メソッド createLoginProperty</span><span class="sxs-lookup"><span data-stu-id="50445-1565">Method createLoginProperty</span></span>

<span data-ttu-id="50445-1566">データベースにログイン プロパティを作成します。</span><span class="sxs-lookup"><span data-stu-id="50445-1566">Creates the login property to the  database.</span></span>

    public LoginProperty createLoginProperty()

#### <a name="return-value"></a><span data-ttu-id="50445-1567">戻り値</span><span class="sxs-lookup"><span data-stu-id="50445-1567">Return Value</span></span>

<span data-ttu-id="50445-1568">作成されたログイン プロパティ。</span><span class="sxs-lookup"><span data-stu-id="50445-1568">The login property that was created.</span></span>

### <a name="method-databaseid"></a><span data-ttu-id="50445-1569">メソッド databaseId</span><span class="sxs-lookup"><span data-stu-id="50445-1569">Method databaseId</span></span>

<span data-ttu-id="50445-1570">SQL データベースのバックエンドとして使用されるデータベースの仕入先の ID を返します。</span><span class="sxs-lookup"><span data-stu-id="50445-1570">Returns the  ID for the database vendor used as the SQL database backend.</span></span>

    public DatabaseId databaseId()

#### <a name="return-value"></a><span data-ttu-id="50445-1571">戻り値</span><span class="sxs-lookup"><span data-stu-id="50445-1571">Return Value</span></span>

<span data-ttu-id="50445-1572">SQL データベースのバックエンドとして使用されるデータベースの仕入先の ID。</span><span class="sxs-lookup"><span data-stu-id="50445-1572">The  ID for the database vendor used as the SQL database backend.</span></span>

#### <a name="remarks"></a><span data-ttu-id="50445-1573">備考</span><span class="sxs-lookup"><span data-stu-id="50445-1573">Remarks</span></span>

<span data-ttu-id="50445-1574">データベースの仕入先が、何らかの理由で特定できない場合、列挙 DbBackend::UNKNOWN が返されます。</span><span class="sxs-lookup"><span data-stu-id="50445-1574">If the database vendor cannot be determined for any reason, the enumeration DbBackend::UNKNOWN is returned.</span></span>

### <a name="method-databasename"></a><span data-ttu-id="50445-1575">メソッド databaseName</span><span class="sxs-lookup"><span data-stu-id="50445-1575">Method databaseName</span></span>

<span data-ttu-id="50445-1576">SQL データベースのバックエンドとして使用されるデータベースの仕入先の名前を返します。</span><span class="sxs-lookup"><span data-stu-id="50445-1576">Returns the name of the database vendor used as the SQL database backend.</span></span>

    public str databaseName()

#### <a name="return-value"></a><span data-ttu-id="50445-1577">戻り値</span><span class="sxs-lookup"><span data-stu-id="50445-1577">Return Value</span></span>

<span data-ttu-id="50445-1578">SQL データベースのバックエンドとして使用されるデータベースの仕入先の名前。</span><span class="sxs-lookup"><span data-stu-id="50445-1578">The name of the database vendor used as the SQL database backend.</span></span>

### <a name="method-dbrequestedunicodeenabled"></a><span data-ttu-id="50445-1579">メソッド dbRequestedUnicodeEnabled</span><span class="sxs-lookup"><span data-stu-id="50445-1579">Method dbRequestedUnicodeEnabled</span></span>

<span data-ttu-id="50445-1580">Unicode がデータベースでサポートされているかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="50445-1580">Retrieves the value that indicates if Unicode is supported in the database.</span></span>

    public boolean dbRequestedUnicodeEnabled()

#### <a name="return-value"></a><span data-ttu-id="50445-1581">戻り値</span><span class="sxs-lookup"><span data-stu-id="50445-1581">Return Value</span></span>

<span data-ttu-id="50445-1582">Unicode がデータベースでサポートされているかどうかを示す値。</span><span class="sxs-lookup"><span data-stu-id="50445-1582">The value that indicates if Unicode is supported in the database.</span></span>

### <a name="method-filenamedeadlocks"></a><span data-ttu-id="50445-1583">メソッド filenameDeadlocks</span><span class="sxs-lookup"><span data-stu-id="50445-1583">Method filenameDeadlocks</span></span>

<span data-ttu-id="50445-1584">デッドロックのトレース ログ ファイルに固有のユーザーの名前を取得します。</span><span class="sxs-lookup"><span data-stu-id="50445-1584">Retrieves the name of the user specific deadlocks trace logfile.</span></span>

    public str filenameDeadlocks(str Userid)

#### <a name="parameters"></a><span data-ttu-id="50445-1585">パラメーター</span><span class="sxs-lookup"><span data-stu-id="50445-1585">Parameters</span></span>

<span data-ttu-id="50445-1586">Userid</span><span class="sxs-lookup"><span data-stu-id="50445-1586">Userid</span></span>  

#### <a name="return-value"></a><span data-ttu-id="50445-1587">戻り値</span><span class="sxs-lookup"><span data-stu-id="50445-1587">Return Value</span></span>

<span data-ttu-id="50445-1588">デッドロックのトレース ログ ファイルに固有のユーザーの名前。</span><span class="sxs-lookup"><span data-stu-id="50445-1588">The name of the user specific to deadlocks trace log file.</span></span>

### <a name="method-filenamequerytimelimit"></a><span data-ttu-id="50445-1589">メソッド filenameQuerytimelimit</span><span class="sxs-lookup"><span data-stu-id="50445-1589">Method filenameQuerytimelimit</span></span>

<span data-ttu-id="50445-1590">ユーザー固有の querytime 期限ログ ファイルの名前を取得します。</span><span class="sxs-lookup"><span data-stu-id="50445-1590">Retrieves the name of the user specific querytime limit logfile.</span></span>

    public str filenameQuerytimelimit(str Userid)

#### <a name="parameters"></a><span data-ttu-id="50445-1591">パラメーター</span><span class="sxs-lookup"><span data-stu-id="50445-1591">Parameters</span></span>

<span data-ttu-id="50445-1592">Userid</span><span class="sxs-lookup"><span data-stu-id="50445-1592">Userid</span></span>  

#### <a name="return-value"></a><span data-ttu-id="50445-1593">戻り値</span><span class="sxs-lookup"><span data-stu-id="50445-1593">Return Value</span></span>

<span data-ttu-id="50445-1594">ユーザー固有の querytime 期限ログ ファイルの名前。</span><span class="sxs-lookup"><span data-stu-id="50445-1594">The name of the user specific querytime limit logfile.</span></span>

### <a name="method-filenamesqltrace"></a><span data-ttu-id="50445-1595">メソッド filenameSqlTrace</span><span class="sxs-lookup"><span data-stu-id="50445-1595">Method filenameSqlTrace</span></span>

<span data-ttu-id="50445-1596">特定のユーザーの SQL トレース ログ ファイルのファイル名を取得します。</span><span class="sxs-lookup"><span data-stu-id="50445-1596">Retrieves the filename of the SQL trace log file for specific user.</span></span>

    public str filenameSqlTrace(str Userid)

#### <a name="parameters"></a><span data-ttu-id="50445-1597">パラメーター</span><span class="sxs-lookup"><span data-stu-id="50445-1597">Parameters</span></span>

<span data-ttu-id="50445-1598">Userid</span><span class="sxs-lookup"><span data-stu-id="50445-1598">Userid</span></span>  
<span data-ttu-id="50445-1599">ユーザー ID。</span><span class="sxs-lookup"><span data-stu-id="50445-1599">The User Id.</span></span>

#### <a name="return-value"></a><span data-ttu-id="50445-1600">戻り値</span><span class="sxs-lookup"><span data-stu-id="50445-1600">Return Value</span></span>

<span data-ttu-id="50445-1601">SQL 追跡ログのファイル名。</span><span class="sxs-lookup"><span data-stu-id="50445-1601">The filename of SQL trace log.</span></span>

### <a name="method-filenamewarnings"></a><span data-ttu-id="50445-1602">メソッド filenameWarnings</span><span class="sxs-lookup"><span data-stu-id="50445-1602">Method filenameWarnings</span></span>

<span data-ttu-id="50445-1603">警告ログ ファイルに固有のユーザーの名前を取得します。</span><span class="sxs-lookup"><span data-stu-id="50445-1603">Retrieves the name of the user specific warnings log file.</span></span>

    public str filenameWarnings(str Userid)

#### <a name="parameters"></a><span data-ttu-id="50445-1604">パラメーター</span><span class="sxs-lookup"><span data-stu-id="50445-1604">Parameters</span></span>

<span data-ttu-id="50445-1605">Userid</span><span class="sxs-lookup"><span data-stu-id="50445-1605">Userid</span></span>  
<span data-ttu-id="50445-1606">関係ユーザーの識別子。</span><span class="sxs-lookup"><span data-stu-id="50445-1606">The identifier of interested user.</span></span>

#### <a name="return-value"></a><span data-ttu-id="50445-1607">戻り値</span><span class="sxs-lookup"><span data-stu-id="50445-1607">Return Value</span></span>

<span data-ttu-id="50445-1608">警告ログ ファイルに固有のユーザーの名前。</span><span class="sxs-lookup"><span data-stu-id="50445-1608">The name of the user specific warnings log file.</span></span>

### <a name="method-logfilename"></a><span data-ttu-id="50445-1609">メソッド logfileName</span><span class="sxs-lookup"><span data-stu-id="50445-1609">Method logfileName</span></span>

<span data-ttu-id="50445-1610">標準的な SQL エラー ログ ファイルの名前を取得します。</span><span class="sxs-lookup"><span data-stu-id="50445-1610">Retrieves the name of the standard  SQL error log file.</span></span>

    public str logfileName([boolean fromCommandline])

#### <a name="parameters"></a><span data-ttu-id="50445-1611">パラメーター</span><span class="sxs-lookup"><span data-stu-id="50445-1611">Parameters</span></span>

<span data-ttu-id="50445-1612">fromCommandline</span><span class="sxs-lookup"><span data-stu-id="50445-1612">fromCommandline</span></span>  
<span data-ttu-id="50445-1613">ブール値。</span><span class="sxs-lookup"><span data-stu-id="50445-1613">A boolean value.</span></span> <span data-ttu-id="50445-1614">パラメーターとしてゼロ以外の値を渡すと、コマンド ラインで渡されるログファイル名が呼び出しにより返されます (オプション)。</span><span class="sxs-lookup"><span data-stu-id="50445-1614">Passing a non-zero value as parameter makes the call return the logfile name passed on the command line; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="50445-1615">戻り値</span><span class="sxs-lookup"><span data-stu-id="50445-1615">Return Value</span></span>

<span data-ttu-id="50445-1616">標準 SQL エラー ログ ファイルのファイル名。</span><span class="sxs-lookup"><span data-stu-id="50445-1616">The file name of the standard  SQL error log file.</span></span>

#### <a name="remarks"></a><span data-ttu-id="50445-1617">備考</span><span class="sxs-lookup"><span data-stu-id="50445-1617">Remarks</span></span>

<span data-ttu-id="50445-1618">バージョン 2.11 以降では、空の文字列が返されます (下位互換性のため)。</span><span class="sxs-lookup"><span data-stu-id="50445-1618">In version 2.11 or higher, an empty string is returned (for backward compatibility).</span></span> <span data-ttu-id="50445-1619">ログ ファイル名を取得するには、filenameSqlError メソッドを使用します。</span><span class="sxs-lookup"><span data-stu-id="50445-1619">Use the filenameSqlError method to retrieve the log file name.</span></span>

### <a name="method-loginconnectstring"></a><span data-ttu-id="50445-1620">メソッド loginConnectString</span><span class="sxs-lookup"><span data-stu-id="50445-1620">Method loginConnectString</span></span>

<span data-ttu-id="50445-1621">ODBC の完全な接続文字列を取得します。</span><span class="sxs-lookup"><span data-stu-id="50445-1621">Retrieves the full ODBC connection string.</span></span>

    public str loginConnectString()

#### <a name="return-value"></a><span data-ttu-id="50445-1622">戻り値</span><span class="sxs-lookup"><span data-stu-id="50445-1622">Return Value</span></span>

<span data-ttu-id="50445-1623">ODBC の完全な接続文字列。</span><span class="sxs-lookup"><span data-stu-id="50445-1623">The full ODBC connection string.</span></span>

### <a name="method-logindatabase"></a><span data-ttu-id="50445-1624">メソッド loginDatabase</span><span class="sxs-lookup"><span data-stu-id="50445-1624">Method loginDatabase</span></span>

<span data-ttu-id="50445-1625">現在接続されているデータベースの名前を取得します。</span><span class="sxs-lookup"><span data-stu-id="50445-1625">Retrieves the name of the database currently connected to.</span></span>

    public str loginDatabase()

#### <a name="return-value"></a><span data-ttu-id="50445-1626">戻り値</span><span class="sxs-lookup"><span data-stu-id="50445-1626">Return Value</span></span>

<span data-ttu-id="50445-1627">現在接続されているデータベースの名前。</span><span class="sxs-lookup"><span data-stu-id="50445-1627">The name of the database currently connected to.</span></span>

#### <a name="examples"></a><span data-ttu-id="50445-1628">例</span><span class="sxs-lookup"><span data-stu-id="50445-1628">Examples</span></span>

    { 
        SqlSystem SqlSystem = new SqlSystem(); 
        print SqlSystem.loginDatabase(); 
    }

### <a name="method-logindsn"></a><span data-ttu-id="50445-1629">メソッド loginDSN</span><span class="sxs-lookup"><span data-stu-id="50445-1629">Method loginDSN</span></span>

<span data-ttu-id="50445-1630">データベースに接続するために使用される Open Database Connectivity (ODBC) データ ソース名 (DSN) を取得します。</span><span class="sxs-lookup"><span data-stu-id="50445-1630">Retrieves the open database connectivity (ODBC) data source name (DSN) used to connect to the database.</span></span>

    public str loginDSN()

#### <a name="return-value"></a><span data-ttu-id="50445-1631">戻り値</span><span class="sxs-lookup"><span data-stu-id="50445-1631">Return Value</span></span>

<span data-ttu-id="50445-1632">データベースへの接続に使用される ODBC データ ソース名の名前。</span><span class="sxs-lookup"><span data-stu-id="50445-1632">The name of the ODBC data source name that is used for connecting to the database.</span></span>

#### <a name="remarks"></a><span data-ttu-id="50445-1633">備考</span><span class="sxs-lookup"><span data-stu-id="50445-1633">Remarks</span></span>

<span data-ttu-id="50445-1634">既定の DSN は「BMSDSN」です。</span><span class="sxs-lookup"><span data-stu-id="50445-1634">The default DSN is "BMSDSN".</span></span>

#### <a name="examples"></a><span data-ttu-id="50445-1635">例</span><span class="sxs-lookup"><span data-stu-id="50445-1635">Examples</span></span>

    { 
        SqlSystem SqlSystem = new SqlSystem(); 
        print SqlSystem.loginDSN(); 
    }

### <a name="method-loginname"></a><span data-ttu-id="50445-1636">メソッド loginName</span><span class="sxs-lookup"><span data-stu-id="50445-1636">Method loginName</span></span>

<span data-ttu-id="50445-1637">データベースにログインするために使用されるユーザー名を取得します。</span><span class="sxs-lookup"><span data-stu-id="50445-1637">Retrieves the user name that is used to log-in to the database.</span></span>

    public str loginName()

#### <a name="return-value"></a><span data-ttu-id="50445-1638">戻り値</span><span class="sxs-lookup"><span data-stu-id="50445-1638">Return Value</span></span>

<span data-ttu-id="50445-1639">データベースにログインするために使用されるユーザー名。</span><span class="sxs-lookup"><span data-stu-id="50445-1639">The user name that is used to log-in to the database.</span></span>

#### <a name="examples"></a><span data-ttu-id="50445-1640">例</span><span class="sxs-lookup"><span data-stu-id="50445-1640">Examples</span></span>

    { 
        SqlSystem SqlSystem = new SqlSystem(); 
        print SqlSystem.loginName(); 
    }

### <a name="method-loginserver"></a><span data-ttu-id="50445-1641">メソッド loginServer</span><span class="sxs-lookup"><span data-stu-id="50445-1641">Method loginServer</span></span>

<span data-ttu-id="50445-1642">現在接続されているデータベース サーバーの名前を取得します。</span><span class="sxs-lookup"><span data-stu-id="50445-1642">Retrieves the name of the database server currently connected to.</span></span>

    public str loginServer()

#### <a name="return-value"></a><span data-ttu-id="50445-1643">戻り値</span><span class="sxs-lookup"><span data-stu-id="50445-1643">Return Value</span></span>

<span data-ttu-id="50445-1644">現在接続されているデータベースの名前。</span><span class="sxs-lookup"><span data-stu-id="50445-1644">The name of the database currently connected to.</span></span>

#### <a name="remarks"></a><span data-ttu-id="50445-1645">備考</span><span class="sxs-lookup"><span data-stu-id="50445-1645">Remarks</span></span>

<span data-ttu-id="50445-1646">データベースがサーバーの概念をサポートしていない場合は、空の文字列が返されます。</span><span class="sxs-lookup"><span data-stu-id="50445-1646">An empty string is returned if the database does not support a server concept.</span></span>

#### <a name="examples"></a><span data-ttu-id="50445-1647">例</span><span class="sxs-lookup"><span data-stu-id="50445-1647">Examples</span></span>

    { 
        SqlSystem SqlSystem = new SqlSystem(); 
        print SqlSystem.loginServer(); 
    }

### <a name="method-monocasefmt"></a><span data-ttu-id="50445-1648">メソッド monocaseFmt</span><span class="sxs-lookup"><span data-stu-id="50445-1648">Method monocaseFmt</span></span>

<span data-ttu-id="50445-1649">文字列を 1 つのケースにキャストするために使用される書式文字列を取得します ("NLS\_LOWER(%1)" など)。</span><span class="sxs-lookup"><span data-stu-id="50445-1649">Retrieves the format string that is used for casting the string to one case (e.g. "NLS\_LOWER(%1)").</span></span>

    public str monocaseFmt([TableId tableId], [FieldId fieldId], [boolean includingFieldName], [boolean considerSystemVariables])

#### <a name="parameters"></a><span data-ttu-id="50445-1650">パラメーター</span><span class="sxs-lookup"><span data-stu-id="50445-1650">Parameters</span></span>

<span data-ttu-id="50445-1651">tableId</span><span class="sxs-lookup"><span data-stu-id="50445-1651">tableId</span></span>  

<!-- -->

<span data-ttu-id="50445-1652">fieldId</span><span class="sxs-lookup"><span data-stu-id="50445-1652">fieldId</span></span>  

<!-- -->

<span data-ttu-id="50445-1653">includingFieldName</span><span class="sxs-lookup"><span data-stu-id="50445-1653">includingFieldName</span></span>  

<!-- -->

<span data-ttu-id="50445-1654">considerSystemVariables</span><span class="sxs-lookup"><span data-stu-id="50445-1654">considerSystemVariables</span></span>  

#### <a name="return-value"></a><span data-ttu-id="50445-1655">戻り値</span><span class="sxs-lookup"><span data-stu-id="50445-1655">Return Value</span></span>

<span data-ttu-id="50445-1656">文字列を 1 つのケースにキャストするために使用される書式文字列。</span><span class="sxs-lookup"><span data-stu-id="50445-1656">The format string that is used for casting the string to one case.</span></span>

#### <a name="remarks"></a><span data-ttu-id="50445-1657">備考</span><span class="sxs-lookup"><span data-stu-id="50445-1657">Remarks</span></span>

<span data-ttu-id="50445-1658">プレースホルダの Finance and Operations アプリケーション スタイルが使用されます (「%1」など)。</span><span class="sxs-lookup"><span data-stu-id="50445-1658">Finance and Operations application style for placeholder(s) is used (i.e. "%1").</span></span>

### <a name="method-sqlliteral"></a><span data-ttu-id="50445-1659">メソッド sqlLiteral</span><span class="sxs-lookup"><span data-stu-id="50445-1659">Method sqlLiteral</span></span>

<span data-ttu-id="50445-1660">SQL タイプを修正するため入力 AX データ型を書式設定します。</span><span class="sxs-lookup"><span data-stu-id="50445-1660">Formats the input AX datatype to correct SQL type.</span></span>

    public str sqlLiteral(AnyType data, [boolean forWhereClause], [boolean likeOperand], [boolean rightJustify], [int stringLength])

#### <a name="parameters"></a><span data-ttu-id="50445-1661">パラメーター</span><span class="sxs-lookup"><span data-stu-id="50445-1661">Parameters</span></span>

<span data-ttu-id="50445-1662">データ</span><span class="sxs-lookup"><span data-stu-id="50445-1662">data</span></span>  
<span data-ttu-id="50445-1663">文字列の長さ。</span><span class="sxs-lookup"><span data-stu-id="50445-1663">The length of the string.</span></span> <span data-ttu-id="50445-1664">既定ではゼロに等しくなります。</span><span class="sxs-lookup"><span data-stu-id="50445-1664">By default equals zero.</span></span>

<!-- -->

<span data-ttu-id="50445-1665">forWhereClause</span><span class="sxs-lookup"><span data-stu-id="50445-1665">forWhereClause</span></span>  
<span data-ttu-id="50445-1666">文字列の長さ。</span><span class="sxs-lookup"><span data-stu-id="50445-1666">The length of the string.</span></span> <span data-ttu-id="50445-1667">既定ではゼロに等しくなります。</span><span class="sxs-lookup"><span data-stu-id="50445-1667">By default equals zero.</span></span>

<!-- -->

<span data-ttu-id="50445-1668">likeOperand</span><span class="sxs-lookup"><span data-stu-id="50445-1668">likeOperand</span></span>  
<span data-ttu-id="50445-1669">文字列の長さ。</span><span class="sxs-lookup"><span data-stu-id="50445-1669">The length of the string.</span></span> <span data-ttu-id="50445-1670">既定ではゼロに等しくなります。</span><span class="sxs-lookup"><span data-stu-id="50445-1670">By default equals zero.</span></span>

<!-- -->

<span data-ttu-id="50445-1671">rightJustify</span><span class="sxs-lookup"><span data-stu-id="50445-1671">rightJustify</span></span>  
<span data-ttu-id="50445-1672">文字列の長さ。</span><span class="sxs-lookup"><span data-stu-id="50445-1672">The length of the string.</span></span> <span data-ttu-id="50445-1673">既定ではゼロに等しくなります。</span><span class="sxs-lookup"><span data-stu-id="50445-1673">By default equals zero.</span></span>

<!-- -->

<span data-ttu-id="50445-1674">stringLength</span><span class="sxs-lookup"><span data-stu-id="50445-1674">stringLength</span></span>  
<span data-ttu-id="50445-1675">文字列の長さ。</span><span class="sxs-lookup"><span data-stu-id="50445-1675">The length of the string.</span></span> <span data-ttu-id="50445-1676">既定ではゼロに等しくなります。</span><span class="sxs-lookup"><span data-stu-id="50445-1676">By default equals zero.</span></span>

#### <a name="return-value"></a><span data-ttu-id="50445-1677">戻り値</span><span class="sxs-lookup"><span data-stu-id="50445-1677">Return Value</span></span>

<span data-ttu-id="50445-1678">書式設定された SQL 型文字列。</span><span class="sxs-lookup"><span data-stu-id="50445-1678">The formatted SQL type string.</span></span>

### <a name="method-clusteredindexes"></a><span data-ttu-id="50445-1679">メソッド clusteredIndexes</span><span class="sxs-lookup"><span data-stu-id="50445-1679">Method clusteredIndexes</span></span>

    public static boolean clusteredIndexes()

#### <a name="return-value"></a><span data-ttu-id="50445-1680">戻り値</span><span class="sxs-lookup"><span data-stu-id="50445-1680">Return Value</span></span>

### <a name="method-databasebackenddesc"></a><span data-ttu-id="50445-1681">メソッド databaseBackendDesc</span><span class="sxs-lookup"><span data-stu-id="50445-1681">Method databaseBackendDesc</span></span>

    public static str databaseBackendDesc()

#### <a name="return-value"></a><span data-ttu-id="50445-1682">戻り値</span><span class="sxs-lookup"><span data-stu-id="50445-1682">Return Value</span></span>

### <a name="method-databasebackendid"></a><span data-ttu-id="50445-1683">メソッド databaseBackendId</span><span class="sxs-lookup"><span data-stu-id="50445-1683">Method databaseBackendId</span></span>

    public static DatabaseId databaseBackendId()

#### <a name="return-value"></a><span data-ttu-id="50445-1684">戻り値</span><span class="sxs-lookup"><span data-stu-id="50445-1684">Return Value</span></span>

### <a name="method-databasebackendname"></a><span data-ttu-id="50445-1685">メソッド databaseBackendName</span><span class="sxs-lookup"><span data-stu-id="50445-1685">Method databaseBackendName</span></span>

    public static str databaseBackendName()

#### <a name="return-value"></a><span data-ttu-id="50445-1686">戻り値</span><span class="sxs-lookup"><span data-stu-id="50445-1686">Return Value</span></span>

### <a name="method-databasecalllevelinterface"></a><span data-ttu-id="50445-1687">メソッド databaseCallLevelInterface</span><span class="sxs-lookup"><span data-stu-id="50445-1687">Method databaseCallLevelInterface</span></span>

    public static DatabaseCLI databaseCallLevelInterface()

#### <a name="return-value"></a><span data-ttu-id="50445-1688">戻り値</span><span class="sxs-lookup"><span data-stu-id="50445-1688">Return Value</span></span>

### <a name="method-databasehints"></a><span data-ttu-id="50445-1689">メソッド databaseHints</span><span class="sxs-lookup"><span data-stu-id="50445-1689">Method databaseHints</span></span>

    public static int databaseHints([int new_hint_value])

#### <a name="parameters"></a><span data-ttu-id="50445-1690">パラメーター</span><span class="sxs-lookup"><span data-stu-id="50445-1690">Parameters</span></span>

<span data-ttu-id="50445-1691">new\_hint\_value</span><span class="sxs-lookup"><span data-stu-id="50445-1691">new\_hint\_value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="50445-1692">戻り値</span><span class="sxs-lookup"><span data-stu-id="50445-1692">Return Value</span></span>

### <a name="method-functionalindexes"></a><span data-ttu-id="50445-1693">メソッド functionalIndexes</span><span class="sxs-lookup"><span data-stu-id="50445-1693">Method functionalIndexes</span></span>

    public static boolean functionalIndexes()

#### <a name="return-value"></a><span data-ttu-id="50445-1694">戻り値</span><span class="sxs-lookup"><span data-stu-id="50445-1694">Return Value</span></span>

### <a name="method-modeldatabasebackendname"></a><span data-ttu-id="50445-1695">メソッド modelDatabaseBackendName</span><span class="sxs-lookup"><span data-stu-id="50445-1695">Method modelDatabaseBackendName</span></span>

<span data-ttu-id="50445-1696">現在接続されているモデル データベース AOS の名前を取得します。</span><span class="sxs-lookup"><span data-stu-id="50445-1696">Retrieves the name of the model database AOS currently connected to.</span></span>

    public static str modelDatabaseBackendName()

#### <a name="return-value"></a><span data-ttu-id="50445-1697">戻り値</span><span class="sxs-lookup"><span data-stu-id="50445-1697">Return Value</span></span>

<span data-ttu-id="50445-1698">現在接続されているモデル データベースの名前。</span><span class="sxs-lookup"><span data-stu-id="50445-1698">The name of the model database currently connected to.</span></span>

### <a name="method-managedconnectionstring"></a><span data-ttu-id="50445-1699">メソッド managedConnectionString</span><span class="sxs-lookup"><span data-stu-id="50445-1699">Method managedConnectionString</span></span>

    public static str managedConnectionString()

#### <a name="return-value"></a><span data-ttu-id="50445-1700">戻り値</span><span class="sxs-lookup"><span data-stu-id="50445-1700">Return Value</span></span>

### <a name="method-new"></a><span data-ttu-id="50445-1701">メソッド new</span><span class="sxs-lookup"><span data-stu-id="50445-1701">Method new</span></span>

<span data-ttu-id="50445-1702">SqlSystem クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="50445-1702">Initializes a new instance of the SqlSystem class.</span></span>

    public void new()

### <a name="method-logfilewrite"></a><span data-ttu-id="50445-1703">メソッド logfileWrite</span><span class="sxs-lookup"><span data-stu-id="50445-1703">Method logfileWrite</span></span>

<span data-ttu-id="50445-1704">テキスト文字列を標準 SQL エラー ログファイルに記述します。</span><span class="sxs-lookup"><span data-stu-id="50445-1704">Writes a text string into the standard  SQL error logfile.</span></span>

    public void logfileWrite(str Text)

#### <a name="parameters"></a><span data-ttu-id="50445-1705">パラメーター</span><span class="sxs-lookup"><span data-stu-id="50445-1705">Parameters</span></span>

<span data-ttu-id="50445-1706">テキスト</span><span class="sxs-lookup"><span data-stu-id="50445-1706">Text</span></span>  
<span data-ttu-id="50445-1707">ログファイルに書き込むテキスト (ブックマークなど)。</span><span class="sxs-lookup"><span data-stu-id="50445-1707">The text (for example, a bookmark) to write to the logfile.</span></span>

#### <a name="remarks"></a><span data-ttu-id="50445-1708">備考</span><span class="sxs-lookup"><span data-stu-id="50445-1708">Remarks</span></span>

<span data-ttu-id="50445-1709">あらゆる種類のエラー状況 (ログ ファイルに記録される) に従い、現在のシナリオを説明する個人用ブックマークを挿入します。</span><span class="sxs-lookup"><span data-stu-id="50445-1709">Following an error situation of any kind (which is logged in the logfile), you may want to insert a personal bookmark that explains the current scenario.</span></span>

#### <a name="examples"></a><span data-ttu-id="50445-1710">例</span><span class="sxs-lookup"><span data-stu-id="50445-1710">Examples</span></span>

    static void myExample(Args _args) 
    { 
        SqlSystem SqlSystem; 
        SqlSystem = new SqlSystem(); 
        SqlSystem.logfileWrite("Recheck the returned data."); 
    }

## <a name="class-ssrsreportautodesignnode"></a><span data-ttu-id="50445-1711">クラス SSRSReportAutoDesignNode</span><span class="sxs-lookup"><span data-stu-id="50445-1711">Class SSRSReportAutoDesignNode</span></span>
    class SSRSReportAutoDesignNode extends SSRSReportDesignNode

### <a name="remarks"></a><span data-ttu-id="50445-1712">備考</span><span class="sxs-lookup"><span data-stu-id="50445-1712">Remarks</span></span>

### <a name="examples"></a><span data-ttu-id="50445-1713">例</span><span class="sxs-lookup"><span data-stu-id="50445-1713">Examples</span></span>

### <a name="methods"></a><span data-ttu-id="50445-1714">メソッド</span><span class="sxs-lookup"><span data-stu-id="50445-1714">Methods</span></span>

| <span data-ttu-id="50445-1715">方法</span><span class="sxs-lookup"><span data-stu-id="50445-1715">Method</span></span>                                              | <span data-ttu-id="50445-1716">説明</span><span class="sxs-lookup"><span data-stu-id="50445-1716">Description</span></span>                                                                        |
|-----------------------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="50445-1717">public str getCrossReferences()</span><span class="sxs-lookup"><span data-stu-id="50445-1717">public str getCrossReferences()</span></span>                     | <span data-ttu-id="50445-1718">指定した SSRSReportDesignNode オブジェクトを使用することで相互参照を取得します。</span><span class="sxs-lookup"><span data-stu-id="50445-1718">Retrieves the cross-references by using the specified SSRSReportDesignNode object.</span></span> |
| <span data-ttu-id="50445-1719">public void setCrossReferences(str crossReferences)</span><span class="sxs-lookup"><span data-stu-id="50445-1719">public void setCrossReferences(str crossReferences)</span></span> | <span data-ttu-id="50445-1720">指定した SSRSReportDesignNode オブジェクトを使用して相互参照を設定します。</span><span class="sxs-lookup"><span data-stu-id="50445-1720">Sets the cross-references by using the specified SSRSReportDesignNode object.</span></span>      |

### <a name="method-getcrossreferences"></a><span data-ttu-id="50445-1721">メソッド getCrossReferences</span><span class="sxs-lookup"><span data-stu-id="50445-1721">Method getCrossReferences</span></span>

<span data-ttu-id="50445-1722">指定した SSRSReportDesignNode オブジェクトを使用することで相互参照を取得します。</span><span class="sxs-lookup"><span data-stu-id="50445-1722">Retrieves the cross-references by using the specified SSRSReportDesignNode object.</span></span>

    public str getCrossReferences()

#### <a name="return-value"></a><span data-ttu-id="50445-1723">戻り値</span><span class="sxs-lookup"><span data-stu-id="50445-1723">Return Value</span></span>

<span data-ttu-id="50445-1724">XML 形式での相互参照。</span><span class="sxs-lookup"><span data-stu-id="50445-1724">The cross-references in XML format.</span></span>

### <a name="method-setcrossreferences"></a><span data-ttu-id="50445-1725">メソッド setCrossReferences</span><span class="sxs-lookup"><span data-stu-id="50445-1725">Method setCrossReferences</span></span>

<span data-ttu-id="50445-1726">指定した SSRSReportDesignNode オブジェクトを使用して相互参照を設定します。</span><span class="sxs-lookup"><span data-stu-id="50445-1726">Sets the cross-references by using the specified SSRSReportDesignNode object.</span></span>

    public void setCrossReferences(str crossReferences)

#### <a name="parameters"></a><span data-ttu-id="50445-1727">パラメーター</span><span class="sxs-lookup"><span data-stu-id="50445-1727">Parameters</span></span>

<span data-ttu-id="50445-1728">crossReferences</span><span class="sxs-lookup"><span data-stu-id="50445-1728">crossReferences</span></span>  
<span data-ttu-id="50445-1729">XML 形式での相互参照。</span><span class="sxs-lookup"><span data-stu-id="50445-1729">The cross-references in XML format.</span></span>

#### <a name="remarks"></a><span data-ttu-id="50445-1730">備考</span><span class="sxs-lookup"><span data-stu-id="50445-1730">Remarks</span></span>

<span data-ttu-id="50445-1731">このメソッドは、指定された SSRSReportDesignNode オブジェクトに格納されている相互参照 XML のみを更新します。</span><span class="sxs-lookup"><span data-stu-id="50445-1731">This method only updates the cross-reference XML stored on the specified SSRSReportDesignNode object.</span></span> <span data-ttu-id="50445-1732">相互参照システムは更新されません。</span><span class="sxs-lookup"><span data-stu-id="50445-1732">It does not update the cross-reference system.</span></span>

## <a name="class-ssrsreportconceptnode"></a><span data-ttu-id="50445-1733">クラス SSRSReportConceptNode</span><span class="sxs-lookup"><span data-stu-id="50445-1733">Class SSRSReportConceptNode</span></span>
    class SSRSReportConceptNode extends xResourceNode

<span data-ttu-id="50445-1734">SSRSReportConceptNode クラスを使うと、アプリケーション オブジェクト ツリー (AOT) の SSRS レポート、データ ソース、スタイル テンプレート、イメージを作成、読み取り、更新、削除できます。</span><span class="sxs-lookup"><span data-stu-id="50445-1734">The SSRSReportConceptNode class lets you create, read, update, and delete SSRS reports, data sources, style templates, and images in the  Application Object Tree (AOT).</span></span>

### <a name="remarks"></a><span data-ttu-id="50445-1735">備考</span><span class="sxs-lookup"><span data-stu-id="50445-1735">Remarks</span></span>

<span data-ttu-id="50445-1736">ユーザーがこの API を呼び出す前に、開発セキュリティ キー (SysDevelopment) にアクセスできることを確認します。</span><span class="sxs-lookup"><span data-stu-id="50445-1736">Make sure that the user has access to the development security key (SysDevelopment) before calling this API.</span></span>

### <a name="examples"></a><span data-ttu-id="50445-1737">例</span><span class="sxs-lookup"><span data-stu-id="50445-1737">Examples</span></span>

### <a name="methods"></a><span data-ttu-id="50445-1738">メソッド</span><span class="sxs-lookup"><span data-stu-id="50445-1738">Methods</span></span>

| <span data-ttu-id="50445-1739">方法</span><span class="sxs-lookup"><span data-stu-id="50445-1739">Method</span></span>                                                     | <span data-ttu-id="50445-1740">説明</span><span class="sxs-lookup"><span data-stu-id="50445-1740">Description</span></span>                                                                   |
|------------------------------------------------------------|-------------------------------------------------------------------------------|
| <span data-ttu-id="50445-1741">public str AOTgetSource()</span><span class="sxs-lookup"><span data-stu-id="50445-1741">public str AOTgetSource()</span></span>                                  | <span data-ttu-id="50445-1742">このノードのソース コードを返します。</span><span class="sxs-lookup"><span data-stu-id="50445-1742">Returns the source code of this node.</span></span>                                         |
| <span data-ttu-id="50445-1743">public str getCrossReferences()</span><span class="sxs-lookup"><span data-stu-id="50445-1743">public str getCrossReferences()</span></span>                            | <span data-ttu-id="50445-1744">指定した SSRSReportConceptNode オブジェクトによる相互参照を取得します。</span><span class="sxs-lookup"><span data-stu-id="50445-1744">Retrieves the cross-references by the specified SSRSReportConceptNode object.</span></span> |
| <span data-ttu-id="50445-1745">public void allowCaching(\[boolean allow\])</span><span class="sxs-lookup"><span data-stu-id="50445-1745">public void allowCaching(\[boolean allow\])</span></span>                |                                                                               |
| <span data-ttu-id="50445-1746">public void setCrossReferences(str crossReferences)</span><span class="sxs-lookup"><span data-stu-id="50445-1746">public void setCrossReferences(str crossReferences)</span></span>        | <span data-ttu-id="50445-1747">指定した SSRSReportConceptNode オブジェクトによる相互参照を設定します。</span><span class="sxs-lookup"><span data-stu-id="50445-1747">Sets the cross-references by the specified SSRSReportConceptNode object.</span></span>      |
| <span data-ttu-id="50445-1748">public void AOTsetSource(str source, \[boolean isStatic\])</span><span class="sxs-lookup"><span data-stu-id="50445-1748">public void AOTsetSource(str source, \[boolean isStatic\])</span></span> | <span data-ttu-id="50445-1749">このノードのソース コードを設定します。</span><span class="sxs-lookup"><span data-stu-id="50445-1749">Sets the source code of this node.</span></span>                                            |

### <a name="method-aotgetsource"></a><span data-ttu-id="50445-1750">メソッド AOTgetSource</span><span class="sxs-lookup"><span data-stu-id="50445-1750">Method AOTgetSource</span></span>

<span data-ttu-id="50445-1751">このノードのソース コードを返します。</span><span class="sxs-lookup"><span data-stu-id="50445-1751">Returns the source code of this node.</span></span>

    public str AOTgetSource()

#### <a name="return-value"></a><span data-ttu-id="50445-1752">戻り値</span><span class="sxs-lookup"><span data-stu-id="50445-1752">Return Value</span></span>

<span data-ttu-id="50445-1753">ソース コードが含まれている場合の文字列、それ以外の場合、nullNothingnullptrunita null 参照 (Visual Basic にはなし)。</span><span class="sxs-lookup"><span data-stu-id="50445-1753">The string that contains the source code, if any; otherwise, nullNothingnullptrunita null reference (Nothing in Visual Basic).</span></span>

#### <a name="remarks"></a><span data-ttu-id="50445-1754">備考</span><span class="sxs-lookup"><span data-stu-id="50445-1754">Remarks</span></span>

<span data-ttu-id="50445-1755">この関数はソース コードを持つノードによってオーバーライドされます。</span><span class="sxs-lookup"><span data-stu-id="50445-1755">This function is overridden by nodes that have source code.</span></span>

### <a name="method-getcrossreferences"></a><span data-ttu-id="50445-1756">メソッド getCrossReferences</span><span class="sxs-lookup"><span data-stu-id="50445-1756">Method getCrossReferences</span></span>

<span data-ttu-id="50445-1757">指定した SSRSReportConceptNode オブジェクトによる相互参照を取得します。</span><span class="sxs-lookup"><span data-stu-id="50445-1757">Retrieves the cross-references by the specified SSRSReportConceptNode object.</span></span>

    public str getCrossReferences()

#### <a name="return-value"></a><span data-ttu-id="50445-1758">戻り値</span><span class="sxs-lookup"><span data-stu-id="50445-1758">Return Value</span></span>

<span data-ttu-id="50445-1759">XML 形式 で指定した SSRSReportConceptNode オブジェクトによる相互参照。</span><span class="sxs-lookup"><span data-stu-id="50445-1759">The cross-references by the specified SSRSReportConceptNode object in XML format.</span></span>

### <a name="method-allowcaching"></a><span data-ttu-id="50445-1760">メソッド allowCaching</span><span class="sxs-lookup"><span data-stu-id="50445-1760">Method allowCaching</span></span>

    public void allowCaching([boolean allow])

#### <a name="parameters"></a><span data-ttu-id="50445-1761">パラメーター</span><span class="sxs-lookup"><span data-stu-id="50445-1761">Parameters</span></span>

<span data-ttu-id="50445-1762">allow</span><span class="sxs-lookup"><span data-stu-id="50445-1762">allow</span></span>  

### <a name="method-setcrossreferences"></a><span data-ttu-id="50445-1763">メソッド setCrossReferences</span><span class="sxs-lookup"><span data-stu-id="50445-1763">Method setCrossReferences</span></span>

<span data-ttu-id="50445-1764">指定した SSRSReportConceptNode オブジェクトによる相互参照を設定します。</span><span class="sxs-lookup"><span data-stu-id="50445-1764">Sets the cross-references by the specified SSRSReportConceptNode object.</span></span>

    public void setCrossReferences(str crossReferences)

#### <a name="parameters"></a><span data-ttu-id="50445-1765">パラメーター</span><span class="sxs-lookup"><span data-stu-id="50445-1765">Parameters</span></span>

<span data-ttu-id="50445-1766">crossReferences</span><span class="sxs-lookup"><span data-stu-id="50445-1766">crossReferences</span></span>  
<span data-ttu-id="50445-1767">XML 形式 で指定した SSRSReportConceptNode オブジェクトによる相互参照。</span><span class="sxs-lookup"><span data-stu-id="50445-1767">The cross-references by the specified SSRSReportConceptNode object in XML format.</span></span>

#### <a name="remarks"></a><span data-ttu-id="50445-1768">備考</span><span class="sxs-lookup"><span data-stu-id="50445-1768">Remarks</span></span>

<span data-ttu-id="50445-1769">このメソッドは、指定された SSRSReportConceptNode オブジェクトに格納されている相互参照 XML のみを更新します。</span><span class="sxs-lookup"><span data-stu-id="50445-1769">This method only updates the cross-reference XML stored on the specified SSRSReportConceptNode object.</span></span> <span data-ttu-id="50445-1770">相互参照システムは更新されません。</span><span class="sxs-lookup"><span data-stu-id="50445-1770">It does not update the cross-reference system.</span></span>

### <a name="method-aotsetsource"></a><span data-ttu-id="50445-1771">メソッド AOTsetSource</span><span class="sxs-lookup"><span data-stu-id="50445-1771">Method AOTsetSource</span></span>

<span data-ttu-id="50445-1772">このノードのソース コードを設定します。</span><span class="sxs-lookup"><span data-stu-id="50445-1772">Sets the source code of this node.</span></span>

    public void AOTsetSource(str source, [boolean isStatic])

#### <a name="parameters"></a><span data-ttu-id="50445-1773">パラメーター</span><span class="sxs-lookup"><span data-stu-id="50445-1773">Parameters</span></span>

<span data-ttu-id="50445-1774">ソース</span><span class="sxs-lookup"><span data-stu-id="50445-1774">source</span></span>  
<span data-ttu-id="50445-1775">メソッドが静的かどうかを指定する値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="50445-1775">The value that specifies whether the method is static; optional.</span></span>

<!-- -->

<span data-ttu-id="50445-1776">isStatic</span><span class="sxs-lookup"><span data-stu-id="50445-1776">isStatic</span></span>  
<span data-ttu-id="50445-1777">メソッドが静的かどうかを指定する値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="50445-1777">The value that specifies whether the method is static; optional.</span></span>

#### <a name="remarks"></a><span data-ttu-id="50445-1778">備考</span><span class="sxs-lookup"><span data-stu-id="50445-1778">Remarks</span></span>

<span data-ttu-id="50445-1779">このメソッドは、ソース コードを持つノードによって上書きされます。</span><span class="sxs-lookup"><span data-stu-id="50445-1779">This method is overridden by nodes that have source code.</span></span>

## <a name="class-ssrsreportdesignnode"></a><span data-ttu-id="50445-1780">クラス SSRSReportDesignNode</span><span class="sxs-lookup"><span data-stu-id="50445-1780">Class SSRSReportDesignNode</span></span>
    class SSRSReportDesignNode extends xResourceNode

<span data-ttu-id="50445-1781">SSRSReportDesignNode クラスを使うと、アプリケーション オブジェクト ツリー (AOT) の Microsoft SQL Server Reporting Services レポート、データ ソース、スタイル テンプレート、イメージを作成、読み取り、更新、削除できます。</span><span class="sxs-lookup"><span data-stu-id="50445-1781">The SSRSReportDesignNode class lets you create, read, update, and delete Microsoft SQL Server Reporting Services reports, data sources, style templates, and images in the  Application Object Tree (AOT).</span></span>

### <a name="remarks"></a><span data-ttu-id="50445-1782">備考</span><span class="sxs-lookup"><span data-stu-id="50445-1782">Remarks</span></span>

<span data-ttu-id="50445-1783">ユーザーがこの API を呼び出す前に、開発セキュリティ キー (SysDevelopment) にアクセスできることを確認します。</span><span class="sxs-lookup"><span data-stu-id="50445-1783">Make sure that the user has access to the development security key (SysDevelopment) before calling this API.</span></span>

### <a name="examples"></a><span data-ttu-id="50445-1784">例</span><span class="sxs-lookup"><span data-stu-id="50445-1784">Examples</span></span>

### <a name="methods"></a><span data-ttu-id="50445-1785">メソッド</span><span class="sxs-lookup"><span data-stu-id="50445-1785">Methods</span></span>

| <span data-ttu-id="50445-1786">方法</span><span class="sxs-lookup"><span data-stu-id="50445-1786">Method</span></span>                                              | <span data-ttu-id="50445-1787">説明</span><span class="sxs-lookup"><span data-stu-id="50445-1787">Description</span></span>                                                                  |
|-----------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="50445-1788">public str getCrossReferences()</span><span class="sxs-lookup"><span data-stu-id="50445-1788">public str getCrossReferences()</span></span>                     | <span data-ttu-id="50445-1789">指定した SSRSReportDesignNode オブジェクトによる相互参照を取得します。</span><span class="sxs-lookup"><span data-stu-id="50445-1789">Retrieves the cross-references by the specified SSRSReportDesignNode object.</span></span> |
| <span data-ttu-id="50445-1790">public void setCrossReferences(str crossReferences)</span><span class="sxs-lookup"><span data-stu-id="50445-1790">public void setCrossReferences(str crossReferences)</span></span> | <span data-ttu-id="50445-1791">指定した SSRSReportDesignNode オブジェクトによる相互参照を設定します。</span><span class="sxs-lookup"><span data-stu-id="50445-1791">Sets the cross-references by the specified SSRSReportDesignNode object.</span></span>      |

### <a name="method-getcrossreferences"></a><span data-ttu-id="50445-1792">メソッド getCrossReferences</span><span class="sxs-lookup"><span data-stu-id="50445-1792">Method getCrossReferences</span></span>

<span data-ttu-id="50445-1793">指定した SSRSReportDesignNode オブジェクトによる相互参照を取得します。</span><span class="sxs-lookup"><span data-stu-id="50445-1793">Retrieves the cross-references by the specified SSRSReportDesignNode object.</span></span>

    public str getCrossReferences()

#### <a name="return-value"></a><span data-ttu-id="50445-1794">戻り値</span><span class="sxs-lookup"><span data-stu-id="50445-1794">Return Value</span></span>

<span data-ttu-id="50445-1795">XML 形式 で指定した SSRSReportDesignNode オブジェクトによる相互参照。</span><span class="sxs-lookup"><span data-stu-id="50445-1795">The cross-references by the specified SSRSReportDesignNode object in XML format.</span></span>

### <a name="method-setcrossreferences"></a><span data-ttu-id="50445-1796">メソッド setCrossReferences</span><span class="sxs-lookup"><span data-stu-id="50445-1796">Method setCrossReferences</span></span>

<span data-ttu-id="50445-1797">指定した SSRSReportDesignNode オブジェクトによる相互参照を設定します。</span><span class="sxs-lookup"><span data-stu-id="50445-1797">Sets the cross-references by the specified SSRSReportDesignNode object.</span></span>

    public void setCrossReferences(str crossReferences)

#### <a name="parameters"></a><span data-ttu-id="50445-1798">パラメーター</span><span class="sxs-lookup"><span data-stu-id="50445-1798">Parameters</span></span>

<span data-ttu-id="50445-1799">crossReferences</span><span class="sxs-lookup"><span data-stu-id="50445-1799">crossReferences</span></span>  
<span data-ttu-id="50445-1800">XML 形式 で指定した SSRSReportDesignNode オブジェクトによる相互参照。</span><span class="sxs-lookup"><span data-stu-id="50445-1800">The cross-references by the specified SSRSReportDesignNode object in XML format.</span></span>

#### <a name="remarks"></a><span data-ttu-id="50445-1801">備考</span><span class="sxs-lookup"><span data-stu-id="50445-1801">Remarks</span></span>

<span data-ttu-id="50445-1802">このメソッドは、指定された SSRSReportDesignNode オブジェクトに格納されている相互参照 XML のみを更新します。</span><span class="sxs-lookup"><span data-stu-id="50445-1802">This method only updates the cross-reference XML stored on the specified SSRSReportDesignNode object.</span></span> <span data-ttu-id="50445-1803">相互参照システムは更新されません。</span><span class="sxs-lookup"><span data-stu-id="50445-1803">It does not update the cross-reference system.</span></span>

## <a name="class-ssrsreportprecisiondesignnode"></a><span data-ttu-id="50445-1804">クラス SSRSReportPrecisionDesignNode</span><span class="sxs-lookup"><span data-stu-id="50445-1804">Class SSRSReportPrecisionDesignNode</span></span>
    class SSRSReportPrecisionDesignNode extends SSRSReportDesignNode

### <a name="remarks"></a><span data-ttu-id="50445-1805">備考</span><span class="sxs-lookup"><span data-stu-id="50445-1805">Remarks</span></span>

### <a name="examples"></a><span data-ttu-id="50445-1806">例</span><span class="sxs-lookup"><span data-stu-id="50445-1806">Examples</span></span>

### <a name="methods"></a><span data-ttu-id="50445-1807">メソッド</span><span class="sxs-lookup"><span data-stu-id="50445-1807">Methods</span></span>

| <span data-ttu-id="50445-1808">方法</span><span class="sxs-lookup"><span data-stu-id="50445-1808">Method</span></span>                                              | <span data-ttu-id="50445-1809">説明</span><span class="sxs-lookup"><span data-stu-id="50445-1809">Description</span></span>                                                                  |
|-----------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="50445-1810">public str getCrossReferences()</span><span class="sxs-lookup"><span data-stu-id="50445-1810">public str getCrossReferences()</span></span>                     | <span data-ttu-id="50445-1811">指定した SSRSReportDesignNode オブジェクトへの相互参照を取得します。</span><span class="sxs-lookup"><span data-stu-id="50445-1811">Retrieves the cross-references to the specified SSRSReportDesignNode object.</span></span> |
| <span data-ttu-id="50445-1812">public void setCrossReferences(str crossReferences)</span><span class="sxs-lookup"><span data-stu-id="50445-1812">public void setCrossReferences(str crossReferences)</span></span> | <span data-ttu-id="50445-1813">指定した SSRSReportDesignNode オブジェクトに相互参照を設定します。</span><span class="sxs-lookup"><span data-stu-id="50445-1813">Sets the cross-references to the specified SSRSReportDesignNode object.</span></span>      |

### <a name="method-getcrossreferences"></a><span data-ttu-id="50445-1814">メソッド getCrossReferences</span><span class="sxs-lookup"><span data-stu-id="50445-1814">Method getCrossReferences</span></span>

<span data-ttu-id="50445-1815">指定した SSRSReportDesignNode オブジェクトへの相互参照を取得します。</span><span class="sxs-lookup"><span data-stu-id="50445-1815">Retrieves the cross-references to the specified SSRSReportDesignNode object.</span></span>

    public str getCrossReferences()

#### <a name="return-value"></a><span data-ttu-id="50445-1816">戻り値</span><span class="sxs-lookup"><span data-stu-id="50445-1816">Return Value</span></span>

<span data-ttu-id="50445-1817">XML 形式 で指定した SSRSReportDesignNode オブジェクトに対する相互参照。</span><span class="sxs-lookup"><span data-stu-id="50445-1817">The cross-references to the specified SSRSReportDesignNode object in XML format.</span></span>

### <a name="method-setcrossreferences"></a><span data-ttu-id="50445-1818">メソッド setCrossReferences</span><span class="sxs-lookup"><span data-stu-id="50445-1818">Method setCrossReferences</span></span>

<span data-ttu-id="50445-1819">指定した SSRSReportDesignNode オブジェクトに相互参照を設定します。</span><span class="sxs-lookup"><span data-stu-id="50445-1819">Sets the cross-references to the specified SSRSReportDesignNode object.</span></span>

    public void setCrossReferences(str crossReferences)

#### <a name="parameters"></a><span data-ttu-id="50445-1820">パラメーター</span><span class="sxs-lookup"><span data-stu-id="50445-1820">Parameters</span></span>

<span data-ttu-id="50445-1821">crossReferences</span><span class="sxs-lookup"><span data-stu-id="50445-1821">crossReferences</span></span>  
<span data-ttu-id="50445-1822">XML 形式 で指定した SSRSReportDesignNode オブジェクトに対する相互参照。</span><span class="sxs-lookup"><span data-stu-id="50445-1822">The cross-references to the specified SSRSReportDesignNode object in XML format.</span></span>

#### <a name="remarks"></a><span data-ttu-id="50445-1823">備考</span><span class="sxs-lookup"><span data-stu-id="50445-1823">Remarks</span></span>

<span data-ttu-id="50445-1824">このメソッドは、指定された SSRSReportDesignNode オブジェクトに格納されている相互参照 XML のみを更新します。</span><span class="sxs-lookup"><span data-stu-id="50445-1824">This method only updates the cross-reference XML that is stored on the specified SSRSReportDesignNode object.</span></span> <span data-ttu-id="50445-1825">相互参照システムは更新されません。</span><span class="sxs-lookup"><span data-stu-id="50445-1825">It does not update the cross-reference system.</span></span>

## <a name="class-statement"></a><span data-ttu-id="50445-1826">クラスの明細書</span><span class="sxs-lookup"><span data-stu-id="50445-1826">Class Statement</span></span>
    class Statement extends Object

<span data-ttu-id="50445-1827">Statement クラスは、静的 SQL ステートメントを実行し、生成された結果を取得します。</span><span class="sxs-lookup"><span data-stu-id="50445-1827">The Statement class executes a static SQL statement and obtains the results it produces.</span></span>

### <a name="remarks"></a><span data-ttu-id="50445-1828">備考</span><span class="sxs-lookup"><span data-stu-id="50445-1828">Remarks</span></span>

<span data-ttu-id="50445-1829">明細書ごとに 1 つだけ、任意の時点で開くことができます。</span><span class="sxs-lookup"><span data-stu-id="50445-1829">Only one per Statement can be open at any point in time.</span></span> <span data-ttu-id="50445-1830">したがって、1 つの ResultSet の読み込みが別の ResultSet の読み込みとインターリーブされている場合は、それぞれ異なるステートメントによって生成されている必要があります。</span><span class="sxs-lookup"><span data-stu-id="50445-1830">Therefore, if the reading of one ResultSet is interleaved with the reading of another, each must have been generated by different Statements.</span></span> <span data-ttu-id="50445-1831">レコードとフィールド レベルのセキュリティは、明細書クラスでは適用されません。</span><span class="sxs-lookup"><span data-stu-id="50445-1831">Record and field level securities are not enforced on the Statement class.</span></span> <span data-ttu-id="50445-1832">したがって、明示的なセキュリティ検証を行わずにユーザーに返されるデータを公開していないことを、確認してください。</span><span class="sxs-lookup"><span data-stu-id="50445-1832">Therefore, make sure you are not exposing data returned to the user without doing explicit security validation.</span></span> <span data-ttu-id="50445-1833">すべての実行可能な明細メソッドは現在 ResultSet で開いている場合明細書は暗黙的に閉じます。</span><span class="sxs-lookup"><span data-stu-id="50445-1833">All statement executed methods implicitly close a statement's current ResultSet if an open one exists.</span></span>

### <a name="examples"></a><span data-ttu-id="50445-1834">例</span><span class="sxs-lookup"><span data-stu-id="50445-1834">Examples</span></span>

    static void example() 
    { 
        Connection Con; 
        Statement Stmt; 
        ResultSet R; 
        SqlStatementExecutePermission perm; 
        str sql = 'SELECT VALUE FROM SQLSYSTEMVARIABLES'; 
        Con = new Connection(); 
        Stmt = Con.createStatement(); 
        perm = new SqlStatementExecutePermission(sql); 
        perm.assert(); 
        R = Stmt.executeQuery(sql); 
        while ( R.next() ) 
        { 
            print R.getString(1); 
        } 
    }

### <a name="methods"></a><span data-ttu-id="50445-1835">メソッド</span><span class="sxs-lookup"><span data-stu-id="50445-1835">Methods</span></span>

| <span data-ttu-id="50445-1836">方法</span><span class="sxs-lookup"><span data-stu-id="50445-1836">Method</span></span>                                       | <span data-ttu-id="50445-1837">説明</span><span class="sxs-lookup"><span data-stu-id="50445-1837">Description</span></span>                                                                                       |
|----------------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="50445-1838">public ResultSet executeQuery(str statement)</span><span class="sxs-lookup"><span data-stu-id="50445-1838">public ResultSet executeQuery(str statement)</span></span> | <span data-ttu-id="50445-1839">インスタンスの the を返す SQL ステートメントを実行します。</span><span class="sxs-lookup"><span data-stu-id="50445-1839">Executes an SQL statement that returns an instance of the .</span></span>                                       |
| <span data-ttu-id="50445-1840">public int executeUpdate(str statement)</span><span class="sxs-lookup"><span data-stu-id="50445-1840">public int executeUpdate(str statement)</span></span>      | <span data-ttu-id="50445-1841">SQL INSERT、UPDATE、または DELETE ステートメントを実行します。</span><span class="sxs-lookup"><span data-stu-id="50445-1841">Executes a SQL INSERT, UPDATE, or DELETE statement.</span></span>                                               |
| <span data-ttu-id="50445-1842">public int getLastError()</span><span class="sxs-lookup"><span data-stu-id="50445-1842">public int getLastError()</span></span>                    | <span data-ttu-id="50445-1843">最後の SQL 操作の SQL データベース バックエンドによって返されたエラー コードを取得します。</span><span class="sxs-lookup"><span data-stu-id="50445-1843">Retrieves the error code returned by the SQL database backend for the last SQL operation.</span></span>         |
| <span data-ttu-id="50445-1844">public str getLastErrorText()</span><span class="sxs-lookup"><span data-stu-id="50445-1844">public str getLastErrorText()</span></span>                | <span data-ttu-id="50445-1845">最後の SQL 操作の SQL データベース バックエンドによって返されたエラー テキストを取得します。</span><span class="sxs-lookup"><span data-stu-id="50445-1845">Retrieves the error text that is returned by the SQL database backend for the last SQL operation.</span></span> |
| <span data-ttu-id="50445-1846">public int getMaxFieldSize()</span><span class="sxs-lookup"><span data-stu-id="50445-1846">public int getMaxFieldSize()</span></span>                 | <span data-ttu-id="50445-1847">現在の列の最大サイズ制限を返します (ある場合)。</span><span class="sxs-lookup"><span data-stu-id="50445-1847">Returns the current maximum column size limit, if any.</span></span>                                            |
| <span data-ttu-id="50445-1848">public void close()</span><span class="sxs-lookup"><span data-stu-id="50445-1848">public void close()</span></span>                          | <span data-ttu-id="50445-1849">ステートメント オブジェクトのデータベースのリソースを解放します。</span><span class="sxs-lookup"><span data-stu-id="50445-1849">Releases the database resources of a statement object.</span></span>                                            |
| <span data-ttu-id="50445-1850">public void setMaxFieldSize(int max)</span><span class="sxs-lookup"><span data-stu-id="50445-1850">public void setMaxFieldSize(int max)</span></span>         | <span data-ttu-id="50445-1851">列の最大サイズ制限を設定します。</span><span class="sxs-lookup"><span data-stu-id="50445-1851">Sets the maximum column size limit.</span></span>                                                               |

### <a name="method-executequery"></a><span data-ttu-id="50445-1852">メソッド executeQuery</span><span class="sxs-lookup"><span data-stu-id="50445-1852">Method executeQuery</span></span>

<span data-ttu-id="50445-1853">インスタンスの the を返す SQL ステートメントを実行します。</span><span class="sxs-lookup"><span data-stu-id="50445-1853">Executes an SQL statement that returns an instance of the .</span></span>

    public ResultSet executeQuery(str statement)

#### <a name="parameters"></a><span data-ttu-id="50445-1854">パラメーター</span><span class="sxs-lookup"><span data-stu-id="50445-1854">Parameters</span></span>

<span data-ttu-id="50445-1855">明細書</span><span class="sxs-lookup"><span data-stu-id="50445-1855">statement</span></span>  
<span data-ttu-id="50445-1856">結果セットを取得するために使用される SQL ステートメントを含む文字列。</span><span class="sxs-lookup"><span data-stu-id="50445-1856">The string that contains the SQL statement that is used to retrieve the result set.</span></span>

#### <a name="return-value"></a><span data-ttu-id="50445-1857">戻り値</span><span class="sxs-lookup"><span data-stu-id="50445-1857">Return Value</span></span>

<span data-ttu-id="50445-1858">クエリから返されたデータを含むオブジェクト。</span><span class="sxs-lookup"><span data-stu-id="50445-1858">The object that contains the data returned from the query.</span></span>

#### <a name="remarks"></a><span data-ttu-id="50445-1859">備考</span><span class="sxs-lookup"><span data-stu-id="50445-1859">Remarks</span></span>

<span data-ttu-id="50445-1860">ユーザーが executeQuery メソッドへの入力を制御すると、SQL インジェクション攻撃が発生する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="50445-1860">If users control input to the executeQuery method, an SQL injection threat can occur.</span></span> <span data-ttu-id="50445-1861">したがって、このメソッドは、コード アクセス セキュリティで実行されます。</span><span class="sxs-lookup"><span data-stu-id="50445-1861">Therefore, this method runs under Code Access Security.</span></span> <span data-ttu-id="50445-1862">サーバー上でこのメソッドを呼び出すには、 からのアクセス許可が必要です。</span><span class="sxs-lookup"><span data-stu-id="50445-1862">Calls to this method on the server require permission from the .</span></span> <span data-ttu-id="50445-1863">SQL ステートメントを実行するための安全な方法は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="50445-1863">The following are safer alternatives for executing SQL statements:</span></span>

-   <span data-ttu-id="50445-1864">クエリ</span><span class="sxs-lookup"><span data-stu-id="50445-1864">Queries</span></span>
-   <span data-ttu-id="50445-1865">ビュー</span><span class="sxs-lookup"><span data-stu-id="50445-1865">Views</span></span>
-   <span data-ttu-id="50445-1866">X++ select ステートメント</span><span class="sxs-lookup"><span data-stu-id="50445-1866">X++ select statements</span></span>

<span data-ttu-id="50445-1867">レコード レベル セキュリティは、明細書クラスでは適用されません。</span><span class="sxs-lookup"><span data-stu-id="50445-1867">Record level security is not enforced on the Statement class.</span></span> <span data-ttu-id="50445-1868">データがユーザーに公開されている場合は、明示的セキュリティ検証を実行します。</span><span class="sxs-lookup"><span data-stu-id="50445-1868">If data is exposed to the user, perform explicit security validation.</span></span>

#### <a name="examples"></a><span data-ttu-id="50445-1869">例</span><span class="sxs-lookup"><span data-stu-id="50445-1869">Examples</span></span>

<span data-ttu-id="50445-1870">次の例では、サーバー上で実行される、CustTable で SQL クエリを実行します。</span><span class="sxs-lookup"><span data-stu-id="50445-1870">The following example performs an SQL query on CustTable, which runs on the server.</span></span> <span data-ttu-id="50445-1871">クエリの結果は、resultSet オブジェクトに格納されます。</span><span class="sxs-lookup"><span data-stu-id="50445-1871">The result of the query is stored in the resultSet object.</span></span>

    server static void main(Args _args) 
    { 
        DictTable  dictTable; 
        Connection connection; 
        Statement  statement; 
        str        sql; 
        ResultSet  resultSet; 
        SqlStatementExecutePermission perm; 
        dictTable = new DictTable(tableNum(CustTable)); 
        if (dictTable != null) 
            { 
               connection = new Connection(); 
               sql = strfmt( "SELECT * FROM %1", dictTable.name(DbBackend::Sql) ); 
               perm = new SqlStatementExecutePermission(sql); 
               // Check for permission to use the statement. 
               perm.assert(); 
               statement = connection.createStatement(); 
               resultSet = statement.executeQuery(sql); 
               // End the scope of the assert call. 
               CodeAccessPermission::revertAssert(); 
            } 
    }

### <a name="method-executeupdate"></a><span data-ttu-id="50445-1872">メソッド executeUpdate</span><span class="sxs-lookup"><span data-stu-id="50445-1872">Method executeUpdate</span></span>

<span data-ttu-id="50445-1873">SQL INSERT、UPDATE、または DELETE ステートメントを実行します。</span><span class="sxs-lookup"><span data-stu-id="50445-1873">Executes a SQL INSERT, UPDATE, or DELETE statement.</span></span>

    public int executeUpdate(str statement)

#### <a name="parameters"></a><span data-ttu-id="50445-1874">パラメーター</span><span class="sxs-lookup"><span data-stu-id="50445-1874">Parameters</span></span>

<span data-ttu-id="50445-1875">明細書</span><span class="sxs-lookup"><span data-stu-id="50445-1875">statement</span></span>  
<span data-ttu-id="50445-1876">データベースに渡される SQL ステートメントを含む文字列。</span><span class="sxs-lookup"><span data-stu-id="50445-1876">The string that contains the SQL statement being passed to the database.</span></span>

#### <a name="return-value"></a><span data-ttu-id="50445-1877">戻り値</span><span class="sxs-lookup"><span data-stu-id="50445-1877">Return Value</span></span>

<span data-ttu-id="50445-1878">更新された行数。それ以外は、何も返さない SQL ステートメントの 0 (ゼロ)。</span><span class="sxs-lookup"><span data-stu-id="50445-1878">An updated row count; otherwise, 0 (zero) for SQL statements that return nothing.</span></span>

#### <a name="remarks"></a><span data-ttu-id="50445-1879">備考</span><span class="sxs-lookup"><span data-stu-id="50445-1879">Remarks</span></span>

<span data-ttu-id="50445-1880">SQLDDL ステートメントなど、何も返さない SQL ステートメントを実行することもできます。</span><span class="sxs-lookup"><span data-stu-id="50445-1880">SQL statements that return nothing, such as SQLDDL statements, can also be executed.</span></span> <span data-ttu-id="50445-1881">ユーザーが executeUpdate メソッドへの入力を制御すると、SQL インジェクション攻撃が発生する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="50445-1881">If users control input to the executeUpdate method, an SQL injection thread can occur.</span></span> <span data-ttu-id="50445-1882">したがって、このメソッドは、コード アクセス セキュリティで実行されます。</span><span class="sxs-lookup"><span data-stu-id="50445-1882">Therefore, this method runs under Code Access Security.</span></span> <span data-ttu-id="50445-1883">サーバー上でこのメソッドを呼び出すには、 からのアクセス許可が必要です。</span><span class="sxs-lookup"><span data-stu-id="50445-1883">Calls to this method on the server require permission from the .</span></span> <span data-ttu-id="50445-1884">データベースとやり取りするための安全な方法は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="50445-1884">The following are safer alternatives for interacting with the database:</span></span>

-   <span data-ttu-id="50445-1885">クエリ</span><span class="sxs-lookup"><span data-stu-id="50445-1885">Queries</span></span>
-   <span data-ttu-id="50445-1886">ビュー</span><span class="sxs-lookup"><span data-stu-id="50445-1886">Views</span></span>
-   <span data-ttu-id="50445-1887">X++ select ステートメント</span><span class="sxs-lookup"><span data-stu-id="50445-1887">X++ select statements</span></span>

<span data-ttu-id="50445-1888">レコード レベル セキュリティは、明細書クラスでは適用されません。</span><span class="sxs-lookup"><span data-stu-id="50445-1888">Record level security is not enforced on the Statement class.</span></span> <span data-ttu-id="50445-1889">データがユーザーに公開されている場合は、明示的セキュリティ検証を実行します。</span><span class="sxs-lookup"><span data-stu-id="50445-1889">If data is exposed to the user, perform explicit security validation.</span></span>

### <a name="method-getlasterror"></a><span data-ttu-id="50445-1890">メソッド getLastError</span><span class="sxs-lookup"><span data-stu-id="50445-1890">Method getLastError</span></span>

<span data-ttu-id="50445-1891">最後の SQL 操作の SQL データベース バックエンドによって返されたエラー コードを取得します。</span><span class="sxs-lookup"><span data-stu-id="50445-1891">Retrieves the error code returned by the SQL database backend for the last SQL operation.</span></span>

    public int getLastError()

#### <a name="return-value"></a><span data-ttu-id="50445-1892">戻り値</span><span class="sxs-lookup"><span data-stu-id="50445-1892">Return Value</span></span>

<span data-ttu-id="50445-1893">最後の SQL 操作の SQL データベース バックエンドによって返されたエラー コード。成功の場合は 0 です。</span><span class="sxs-lookup"><span data-stu-id="50445-1893">The error code returned by the SQL database backend for the last SQL operation; or 0 for success.</span></span>

#### <a name="examples"></a><span data-ttu-id="50445-1894">例</span><span class="sxs-lookup"><span data-stu-id="50445-1894">Examples</span></span>

    static void StatementGetLastError()  
    { 
        str sql, sql2; 
        UserConnection Connection = new UserConnection(); 
        Statement Statement = Connection.createStatement(); 
        boolean clear_infolog = false; 
        print "-Delete-a-non-existing-record-(valid statement)-----------"; 
        sql = "delete from zipcode where Recid = 2"; 
        new SqlStatementExecutePermission(sql).assert(); 
        Statement.executeUpdate(sql); 
        print " Error code was: ", Statement.getLastError(); 
        print " Error message was '", Statement.getLastErrorText(), "'"; 
        try 
        { 
            print "\n"; 
            print "-Delete-from-a-non-existing-table-(invalid statement)---    --"; 
            sql2 = "delete from StrangeTable07"; 
            new SqlStatementExecutePermission(sql2).assert(); 
            Statement.executeUpdate(sql2); 
        } 
        catch (exception::Error) 
        { 
            print "Exception was caught:"; 
            print " Error code was: ", Statement.getLastError(); 
            print " Error message was '", Statement.getLastErrorText(), "'"; 
        } 
        CodeAccessPermission::revertAssert(); 
        pause; 
    }

### <a name="method-getlasterrortext"></a><span data-ttu-id="50445-1895">メソッド getLastErrorText</span><span class="sxs-lookup"><span data-stu-id="50445-1895">Method getLastErrorText</span></span>

<span data-ttu-id="50445-1896">最後の SQL 操作の SQL データベース バックエンドによって返されたエラー テキストを取得します。</span><span class="sxs-lookup"><span data-stu-id="50445-1896">Retrieves the error text that is returned by the SQL database backend for the last SQL operation.</span></span>

    public str getLastErrorText()

#### <a name="return-value"></a><span data-ttu-id="50445-1897">戻り値</span><span class="sxs-lookup"><span data-stu-id="50445-1897">Return Value</span></span>

<span data-ttu-id="50445-1898">最後の SQL 操作の SQL データベースによって提供されるエラー テキスト。</span><span class="sxs-lookup"><span data-stu-id="50445-1898">The error text that is provided by the SQL database for the last SQL operation.</span></span>

### <a name="method-getmaxfieldsize"></a><span data-ttu-id="50445-1899">メソッド getMaxFieldSize</span><span class="sxs-lookup"><span data-stu-id="50445-1899">Method getMaxFieldSize</span></span>

<span data-ttu-id="50445-1900">現在の列の最大サイズ制限を返します (ある場合)。</span><span class="sxs-lookup"><span data-stu-id="50445-1900">Returns the current maximum column size limit, if any.</span></span>

    public int getMaxFieldSize()

#### <a name="return-value"></a><span data-ttu-id="50445-1901">戻り値</span><span class="sxs-lookup"><span data-stu-id="50445-1901">Return Value</span></span>

<span data-ttu-id="50445-1902">現在の列の最大サイズ制限。0 は無制限を意味します。</span><span class="sxs-lookup"><span data-stu-id="50445-1902">The current maximum column size limit; 0 means unlimited.</span></span>

#### <a name="remarks"></a><span data-ttu-id="50445-1903">備考</span><span class="sxs-lookup"><span data-stu-id="50445-1903">Remarks</span></span>

<span data-ttu-id="50445-1904">maxFieldSize の制限 (バイト単位) は、任意の列の値に対して返されるデータの最大量です。binary、varbinary、longvarbinary、char、varchar、および longvarchar 列にのみ適用されます。</span><span class="sxs-lookup"><span data-stu-id="50445-1904">The maxFieldSize limit (in bytes) is the maximum amount of data returned for any column value; it only applies to binary, varbinary, longvarbinary, char, varchar, and longvarchar columns.</span></span> <span data-ttu-id="50445-1905">制限を超過した場合、余分なデータは通知なしに破棄されます。</span><span class="sxs-lookup"><span data-stu-id="50445-1905">If the limit is exceeded, the excess data is silently discarded.</span></span>

### <a name="method-close"></a><span data-ttu-id="50445-1906">メソッド close</span><span class="sxs-lookup"><span data-stu-id="50445-1906">Method close</span></span>

<span data-ttu-id="50445-1907">ステートメント オブジェクトのデータベースのリソースを解放します。</span><span class="sxs-lookup"><span data-stu-id="50445-1907">Releases the database resources of a statement object.</span></span>

    public void close()

### <a name="method-setmaxfieldsize"></a><span data-ttu-id="50445-1908">メソッド setMaxFieldSize</span><span class="sxs-lookup"><span data-stu-id="50445-1908">Method setMaxFieldSize</span></span>

<span data-ttu-id="50445-1909">列の最大サイズ制限を設定します。</span><span class="sxs-lookup"><span data-stu-id="50445-1909">Sets the maximum column size limit.</span></span>

    public void setMaxFieldSize(int max)

#### <a name="parameters"></a><span data-ttu-id="50445-1910">パラメーター</span><span class="sxs-lookup"><span data-stu-id="50445-1910">Parameters</span></span>

<span data-ttu-id="50445-1911">最大</span><span class="sxs-lookup"><span data-stu-id="50445-1911">max</span></span>  
<span data-ttu-id="50445-1912">列の新しい最大サイズ制限。0 は無制限を意味します。</span><span class="sxs-lookup"><span data-stu-id="50445-1912">The new max column size limit; 0 means unlimited.</span></span>

#### <a name="remarks"></a><span data-ttu-id="50445-1913">備考</span><span class="sxs-lookup"><span data-stu-id="50445-1913">Remarks</span></span>

<span data-ttu-id="50445-1914">maxFieldSize の制限 (バイト単位) は、任意の列の値に対して返されるデータのサイズを制限するように設定されています。binary、varbinary、longvarbinary、char、varchar、および longvarchar フィールドにのみ適用されます。</span><span class="sxs-lookup"><span data-stu-id="50445-1914">The maxFieldSize limit (in bytes) is set to limit the size of data that can be returned for any column value; it only applies to binary, varbinary, longvarbinary, char, varchar, and longvarchar fields.</span></span> <span data-ttu-id="50445-1915">制限を超過した場合、余分なデータは通知なしに破棄されます。</span><span class="sxs-lookup"><span data-stu-id="50445-1915">If the limit is exceeded, the excess data is silently discarded.</span></span> <span data-ttu-id="50445-1916">最大可搬性については、256 より大きい値を使用します。</span><span class="sxs-lookup"><span data-stu-id="50445-1916">For maximum portability, use values greater than 256.</span></span>

## <a name="class-struct"></a><span data-ttu-id="50445-1917">クラス構造体</span><span class="sxs-lookup"><span data-stu-id="50445-1917">Class Struct</span></span>
    class Struct extends Object

<span data-ttu-id="50445-1918">構造体は、特定のエンティティに関する情報をグループ化するために、任意の X++ 型の複数値を保持します。</span><span class="sxs-lookup"><span data-stu-id="50445-1918">A struct holds several values of any X++ type, to group the information about a specific entity.</span></span>

### <a name="remarks"></a><span data-ttu-id="50445-1919">備考</span><span class="sxs-lookup"><span data-stu-id="50445-1919">Remarks</span></span>

<span data-ttu-id="50445-1920">構造体 (略構造) は、すべての X++ 型の複数値を保持できるエンティティです。</span><span class="sxs-lookup"><span data-stu-id="50445-1920">A struct (short for structure) is an entity that can hold several values of any X++ type.</span></span> <span data-ttu-id="50445-1921">構造体は、特定のエンティティに関する情報をグループ化するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="50445-1921">Structs are used to group information about a specific entity.</span></span> <span data-ttu-id="50445-1922">たとえば、顧客の名前、年齢、および住所に関する情報を格納し、それからこの複合情報を 1つの項目として扱う場合があります。</span><span class="sxs-lookup"><span data-stu-id="50445-1922">For example, you might want to store information about a customer's name, age and address and then treat this compound information as one item.</span></span> <span data-ttu-id="50445-1923">構造体内の項目は、データ型と名前で指定されます。</span><span class="sxs-lookup"><span data-stu-id="50445-1923">The items in a struct are specified by a data type and a name.</span></span> <span data-ttu-id="50445-1924">項目は、new メソッドを使用して構造体が作成される場合に追加されるか、add メソッドを使用して構造体が作成された後に作成されます。</span><span class="sxs-lookup"><span data-stu-id="50445-1924">Items are added when the struct is created by using the new method, or they are created after the struct has been created by using the add method.</span></span> <span data-ttu-id="50445-1925">Add メソッドを使用して品目を追加する場合は、同時に品目の値を指定し、この値からデータ型が推測されます。</span><span class="sxs-lookup"><span data-stu-id="50445-1925">If you add an item by using the add method, you specify the value for the item at the same time, and the data type is inferred from this value.</span></span> <span data-ttu-id="50445-1926">構造体のインスタンス化中に品目を追加する場合は、値または valueIndex メソッドを使用して、値を割り当てる必要があります。</span><span class="sxs-lookup"><span data-stu-id="50445-1926">If you add an item during the instantiation of the struct, you need to use the value or the valueIndex method to assign a value to it.</span></span> <span data-ttu-id="50445-1927">構造体内の項目は、文字列型、整数型、実数型、日付型、コンテナー型、レコード型、クラス型など、型システムの列挙型にあるデータ型のいずれでもかまいません。</span><span class="sxs-lookup"><span data-stu-id="50445-1927">The items in a struct can be of any of the data types found in the Types system enum, including: string, integer, real, date, container, record, and class.</span></span> <span data-ttu-id="50445-1928">構造体内の項目は、項目名のアルファベット順に並べられます。</span><span class="sxs-lookup"><span data-stu-id="50445-1928">The items in a struct are arranged in alphabetical order of the item names.</span></span> <span data-ttu-id="50445-1929">構造体のフィールドは、fields、fieldName、および fieldType メソッドを使用してスキャンできます。</span><span class="sxs-lookup"><span data-stu-id="50445-1929">The fields in a struct can be traversed by using the fields, fieldName, and fieldType methods.</span></span> <span data-ttu-id="50445-1930">構造体は、コンテナーに梱包し、後で Struct::create メソッドを使用して復元できます。</span><span class="sxs-lookup"><span data-stu-id="50445-1930">Structs can be packed into containers and later restored by using the Struct::create method.</span></span> <span data-ttu-id="50445-1931">構造体には、X++ コンテナーとのいくつかの類似点があります。</span><span class="sxs-lookup"><span data-stu-id="50445-1931">Structs have some similarities to X++ containers.</span></span> <span data-ttu-id="50445-1932">ただし、コンテナーは値の型であり、X++ 言語に組み込まれています。</span><span class="sxs-lookup"><span data-stu-id="50445-1932">However, a container is a value type and is built into the X++ language.</span></span> <span data-ttu-id="50445-1933">入れ子になったコンテナを作成することができますが、入れ子になった構造体は作成することができません。</span><span class="sxs-lookup"><span data-stu-id="50445-1933">You can create nested containers, but you cannot create nested structs.</span></span> <span data-ttu-id="50445-1934">X++ クラスは、構造とほぼ同じ方法で情報を保管することができます。</span><span class="sxs-lookup"><span data-stu-id="50445-1934">X++ classes can store information in much the same way as structs.</span></span> <span data-ttu-id="50445-1935">クラスはデータを操作する方法を供給することができますが、構造体のための該当する機能は提供されておらず、上書きまたは拡張の概念はありません。</span><span class="sxs-lookup"><span data-stu-id="50445-1935">But although classes can supply methods to manipulate the data, no such facility is provided for structs, and there is no concept of overriding or extension.</span></span> <span data-ttu-id="50445-1936">クラスは AOT でのみ作成できますが、構造体は作成されたコードのコンテキスト内にのみ存在します。</span><span class="sxs-lookup"><span data-stu-id="50445-1936">Classes can only be created in the AOT, but structs exist solely in the context of the code in which they are created.</span></span> <span data-ttu-id="50445-1937">クラス メンバーの変数はクラス専用なので、アクセサー関数はクラスの外部から使用される値のためにコード化されている必要があります。</span><span class="sxs-lookup"><span data-stu-id="50445-1937">Class member variables are private to the class, so accessor functions must be coded for them for the values to be used from outside the class.</span></span> <span data-ttu-id="50445-1938">構造体内の項目は一般にアクセス可能です。</span><span class="sxs-lookup"><span data-stu-id="50445-1938">The items within a struct are publicly accessible.</span></span>

### <a name="examples"></a><span data-ttu-id="50445-1939">例</span><span class="sxs-lookup"><span data-stu-id="50445-1939">Examples</span></span>

<span data-ttu-id="50445-1940">次の例では、2 つの項目を含む構造体を作成し、その項目に値を割り当てます。</span><span class="sxs-lookup"><span data-stu-id="50445-1940">The following example creates a struct with two items and then assigns values to those items.</span></span> <span data-ttu-id="50445-1941">Struct.add メソッドを使用して新しい項目が追加されます。項目のデータ型は割り当てられた値から推測されます。</span><span class="sxs-lookup"><span data-stu-id="50445-1941">A new item is then added by using the Struct.add method; the data type of the item is inferred from the value assigned to it.</span></span> <span data-ttu-id="50445-1942">次に、構造体はコンテナーに梱包され、元の構造体のコピーである新しい構造体を作成するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="50445-1942">The struct is then packed into a container and used to create a new struct, a copy of the original struct.</span></span>

    { 
        Struct s = new struct ("int age; str name"); 
        Struct copy; 
        container c; 
        int i; 
        // Add values to the items 
        s.value("age", 25); 
        s.value("name", "Jane Dow"); 
      // Add a new item; data type is inferred from value 
        s.add("Shoesize", 45); 
        // Print the definition of the struct 
        print s.definitionString(); 
        // Prints the type and name of all items in the struct 
        for (i =  1;   i <= s.fields();i++) 
        { 
             print s.fieldType(i), " ", s.fieldName(i); 
        }  
        // Pack the struct into a container and restore it into copy 
        c = s.pack(); 
        copy = Struct::create(c); 
        print copy.definitionString(); 
        pause; 
    }

### <a name="methods"></a><span data-ttu-id="50445-1943">メソッド</span><span class="sxs-lookup"><span data-stu-id="50445-1943">Methods</span></span>

| <span data-ttu-id="50445-1944">方法</span><span class="sxs-lookup"><span data-stu-id="50445-1944">Method</span></span>                                                        | <span data-ttu-id="50445-1945">説明</span><span class="sxs-lookup"><span data-stu-id="50445-1945">Description</span></span>                                                                                   |
|---------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="50445-1946">public boolean add(str fieldName, AnyType value)</span><span class="sxs-lookup"><span data-stu-id="50445-1946">public boolean add(str fieldName, AnyType value)</span></span>              | <span data-ttu-id="50445-1947">構造体に新しい項目を追加し、指定した値を割り当てます。</span><span class="sxs-lookup"><span data-stu-id="50445-1947">Adds a new item to the struct and assigns the specified value to it.</span></span>                          |
| <span data-ttu-id="50445-1948">public str definitionString()</span><span class="sxs-lookup"><span data-stu-id="50445-1948">public str definitionString()</span></span>                                 | <span data-ttu-id="50445-1949">構造体の要素の名前およびタイプの説明を返します。</span><span class="sxs-lookup"><span data-stu-id="50445-1949">Returns a description of the names and types of the elements in the struct.</span></span>                   |
| <span data-ttu-id="50445-1950">public boolean exists(str fieldName)</span><span class="sxs-lookup"><span data-stu-id="50445-1950">public boolean exists(str fieldName)</span></span>                          | <span data-ttu-id="50445-1951">特定の項目が構造体に存在するかどうかを判定します。</span><span class="sxs-lookup"><span data-stu-id="50445-1951">Determines whether a particular item exists in a struct.</span></span>                                      |
| <span data-ttu-id="50445-1952">public str fieldName(int index)</span><span class="sxs-lookup"><span data-stu-id="50445-1952">public str fieldName(int index)</span></span>                               | <span data-ttu-id="50445-1953">指定された位置にある構造体内の項目の名前を返します。</span><span class="sxs-lookup"><span data-stu-id="50445-1953">Returns the name of the item in the struct at the specified position.</span></span>                         |
| <span data-ttu-id="50445-1954">public int fields()</span><span class="sxs-lookup"><span data-stu-id="50445-1954">public int fields()</span></span>                                           | <span data-ttu-id="50445-1955">構造体内の項目の数を返します。</span><span class="sxs-lookup"><span data-stu-id="50445-1955">Returns the number of items in the struct.</span></span>                                                    |
| <span data-ttu-id="50445-1956">public Types fieldType(int index)</span><span class="sxs-lookup"><span data-stu-id="50445-1956">public Types fieldType(int index)</span></span>                             | <span data-ttu-id="50445-1957">指定された位置にある構造体内の項目のデータ型を返します。</span><span class="sxs-lookup"><span data-stu-id="50445-1957">Returns the data type of the item in the struct at the specified position.</span></span>                    |
| <span data-ttu-id="50445-1958">public int index(str fieldName)</span><span class="sxs-lookup"><span data-stu-id="50445-1958">public int index(str fieldName)</span></span>                               | <span data-ttu-id="50445-1959">名前に基づいて構造体の項目の位置を計算します。</span><span class="sxs-lookup"><span data-stu-id="50445-1959">Calculates the position of an item in the struct based on its name.</span></span>                           |
| <span data-ttu-id="50445-1960">public container pack()</span><span class="sxs-lookup"><span data-stu-id="50445-1960">public container pack()</span></span>                                       | <span data-ttu-id="50445-1961">Struct クラスの現在のインスタンスをシリアル化します。</span><span class="sxs-lookup"><span data-stu-id="50445-1961">Serializes the current instance of the Struct class.</span></span>                                          |
| <span data-ttu-id="50445-1962">public boolean remove(str fieldName)</span><span class="sxs-lookup"><span data-stu-id="50445-1962">public boolean remove(str fieldName)</span></span>                          | <span data-ttu-id="50445-1963">構造体から品目を削除します。</span><span class="sxs-lookup"><span data-stu-id="50445-1963">Removes an item from a struct.</span></span>                                                                |
| <span data-ttu-id="50445-1964">public str toString()</span><span class="sxs-lookup"><span data-stu-id="50445-1964">public str toString()</span></span>                                         | <span data-ttu-id="50445-1965">構造体の内容を説明する文字列を返します。</span><span class="sxs-lookup"><span data-stu-id="50445-1965">Returns a string that describes the contents of the struct.</span></span>                                   |
| <span data-ttu-id="50445-1966">public AnyType value(str fieldName, \[AnyType value\])</span><span class="sxs-lookup"><span data-stu-id="50445-1966">public AnyType value(str fieldName, \[AnyType value\])</span></span>        | <span data-ttu-id="50445-1967">構造体で指定される品目の値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="50445-1967">Gets or sets the value for a specified item in a struct.</span></span>                                      |
| <span data-ttu-id="50445-1968">public str valueImage(int index)</span><span class="sxs-lookup"><span data-stu-id="50445-1968">public str valueImage(int index)</span></span>                              | <span data-ttu-id="50445-1969">構造体内の特定の位置にある品目の値を説明する文字列を返します。</span><span class="sxs-lookup"><span data-stu-id="50445-1969">Returns a string that describes the value of the item at a particular position in the struct.</span></span> |
| <span data-ttu-id="50445-1970">public AnyType valueIndex(int index, \[AnyType value\])</span><span class="sxs-lookup"><span data-stu-id="50445-1970">public AnyType valueIndex(int index, \[AnyType value\])</span></span>       | <span data-ttu-id="50445-1971">構造体で指定される位置での品目の値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="50445-1971">Gets or sets the value of the item at a specified position in a struct.</span></span>                       |
| <span data-ttu-id="50445-1972">public str xml(\[int indent\])</span><span class="sxs-lookup"><span data-stu-id="50445-1972">public str xml(\[int indent\])</span></span>                                | <span data-ttu-id="50445-1973">現在のオブジェクトを表す XML 文字列を返します。</span><span class="sxs-lookup"><span data-stu-id="50445-1973">Returns an XML string that represents the current object.</span></span>                                     |
| <span data-ttu-id="50445-1974">::public static Struct create(container container)</span><span class="sxs-lookup"><span data-stu-id="50445-1974">::public static Struct create(container container)</span></span>            | <span data-ttu-id="50445-1975">以前の Struct.pack の呼び出しで取得されたコンテナーから構造体を作成します。</span><span class="sxs-lookup"><span data-stu-id="50445-1975">Creates a struct from a container that is obtained from a prior call to Struct.pack.</span></span>          |
| <span data-ttu-id="50445-1976">::public static Struct createFromXML(Object xmlnode)</span><span class="sxs-lookup"><span data-stu-id="50445-1976">::public static Struct createFromXML(Object xmlnode)</span></span>          |                                                                                               |
| <span data-ttu-id="50445-1977">::public static boolean equal(Struct struct1, Struct struct2)</span><span class="sxs-lookup"><span data-stu-id="50445-1977">::public static boolean equal(Struct struct1, Struct struct2)</span></span> | <span data-ttu-id="50445-1978">2 つの構造体が等しいかどうかを判断します。</span><span class="sxs-lookup"><span data-stu-id="50445-1978">Determines whether two structs are equal.</span></span>                                                     |
| <span data-ttu-id="50445-1979">::public static Struct merge(Struct struct1, Struct struct2)</span><span class="sxs-lookup"><span data-stu-id="50445-1979">::public static Struct merge(Struct struct1, Struct struct2)</span></span>  | <span data-ttu-id="50445-1980">2 つの構造体を組み合わせ、新しい構造体を作成します。</span><span class="sxs-lookup"><span data-stu-id="50445-1980">Combines two structs to create a new struct.</span></span>                                                  |
| <span data-ttu-id="50445-1981">public void new(VarArg specifier)</span><span class="sxs-lookup"><span data-stu-id="50445-1981">public void new(VarArg specifier)</span></span>                             | <span data-ttu-id="50445-1982">構造体を作成します。</span><span class="sxs-lookup"><span data-stu-id="50445-1982">Creates a struct.</span></span>                                                                             |

### <a name="method-add"></a><span data-ttu-id="50445-1983">メソッド add</span><span class="sxs-lookup"><span data-stu-id="50445-1983">Method add</span></span>

<span data-ttu-id="50445-1984">構造体に新しい項目を追加し、指定した値を割り当てます。</span><span class="sxs-lookup"><span data-stu-id="50445-1984">Adds a new item to the struct and assigns the specified value to it.</span></span>

    public boolean add(str fieldName, AnyType value)

#### <a name="parameters"></a><span data-ttu-id="50445-1985">パラメーター</span><span class="sxs-lookup"><span data-stu-id="50445-1985">Parameters</span></span>

<span data-ttu-id="50445-1986">fieldName</span><span class="sxs-lookup"><span data-stu-id="50445-1986">fieldName</span></span>  
<span data-ttu-id="50445-1987">新しい項目に割り当てる値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="50445-1987">The value to assign to the new item.</span></span> <span data-ttu-id="50445-1988">この値は、アイテムのタイプを定義します。</span><span class="sxs-lookup"><span data-stu-id="50445-1988">This value defines the type of the item.</span></span>

<!-- -->

<span data-ttu-id="50445-1989">値</span><span class="sxs-lookup"><span data-stu-id="50445-1989">value</span></span>  
<span data-ttu-id="50445-1990">新しい項目に割り当てる値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="50445-1990">The value to assign to the new item.</span></span> <span data-ttu-id="50445-1991">この値は、アイテムのタイプを定義します。</span><span class="sxs-lookup"><span data-stu-id="50445-1991">This value defines the type of the item.</span></span>

#### <a name="return-value"></a><span data-ttu-id="50445-1992">戻り値</span><span class="sxs-lookup"><span data-stu-id="50445-1992">Return Value</span></span>

<span data-ttu-id="50445-1993">値が構造体に追加された場合は true。値を追加することができなかった場合は (既に構造体に存在していた場合は) false。</span><span class="sxs-lookup"><span data-stu-id="50445-1993">true if the value has been added to the struct; false if the value could not be added (if it already existed in the struct).</span></span>

#### <a name="remarks"></a><span data-ttu-id="50445-1994">備考</span><span class="sxs-lookup"><span data-stu-id="50445-1994">Remarks</span></span>

<span data-ttu-id="50445-1995">値のタイプは値の内容から推測されます。</span><span class="sxs-lookup"><span data-stu-id="50445-1995">The type of the value is inferred from content of the value.</span></span> <span data-ttu-id="50445-1996">構造体内の項目は、項目名に従ってアルファベット順に並べられます。</span><span class="sxs-lookup"><span data-stu-id="50445-1996">The items in a struct are arranged in alphabetical order according to the item names.</span></span> <span data-ttu-id="50445-1997">構造体の項目の値は、Struct.value メソッドまたは Struct.valueIndex メソッドを使用して変更できます。</span><span class="sxs-lookup"><span data-stu-id="50445-1997">The value of an item in a struct can be changed by using the Struct.value or the Struct.valueIndex method.</span></span>

#### <a name="examples"></a><span data-ttu-id="50445-1998">例</span><span class="sxs-lookup"><span data-stu-id="50445-1998">Examples</span></span>

<span data-ttu-id="50445-1999">次の例では、名前および年齢フィールドの 2 つの項目を持つ構造体を作成し、それらの項目に値を割り当てます。</span><span class="sxs-lookup"><span data-stu-id="50445-1999">The following example creates a struct with two items name and age fields and assigns values to those items.</span></span> <span data-ttu-id="50445-2000">その後、add メソッドを使用して、43 という値の shoeSize 変数が追加項目として作成されます。</span><span class="sxs-lookup"><span data-stu-id="50445-2000">The add method is then used to create an additional item the shoeSize variable, with a value of 43.</span></span> <span data-ttu-id="50445-2001">値のタイプによって、新しい項目のタイプ int が決まります。</span><span class="sxs-lookup"><span data-stu-id="50445-2001">The type of the value determines the type of the new item, int.</span></span>

    { 
        Struct s = new Struct ("str name; int age"); 
        // Prints number of items (2) 
        print s.fields(); 
        // Values are assigned to the two items 
        s.value("name", "John"); 
        s.value("age", 34); 
        //Another item is added to the struct 
        s.add("shoeSize", 43); 
        // Prints number of item (3) 
        print s.fields(); 
        // Prints a description of the items in the struct 
        print s.definitionString(); 
        pause; 
    }

### <a name="method-definitionstring"></a><span data-ttu-id="50445-2002">メソッド definitionString</span><span class="sxs-lookup"><span data-stu-id="50445-2002">Method definitionString</span></span>

<span data-ttu-id="50445-2003">構造体の要素の名前およびタイプの説明を返します。</span><span class="sxs-lookup"><span data-stu-id="50445-2003">Returns a description of the names and types of the elements in the struct.</span></span>

    public str definitionString()

#### <a name="return-value"></a><span data-ttu-id="50445-2004">戻り値</span><span class="sxs-lookup"><span data-stu-id="50445-2004">Return Value</span></span>

<span data-ttu-id="50445-2005">構造体の定義を含む文字列。</span><span class="sxs-lookup"><span data-stu-id="50445-2005">A string that contains a definition of the struct.</span></span>

#### <a name="remarks"></a><span data-ttu-id="50445-2006">備考</span><span class="sxs-lookup"><span data-stu-id="50445-2006">Remarks</span></span>

<span data-ttu-id="50445-2007">definitionString メソッドを使用すると、構文 newStruct = new struct(oldStruct.definitionString()); を用いて構造体のコピーを作成することができます。</span><span class="sxs-lookup"><span data-stu-id="50445-2007">You can use the definitionString method to create a copy of a struct by using the syntax: newStruct = new struct(oldStruct.definitionString());</span></span>

### <a name="method-exists"></a><span data-ttu-id="50445-2008">メソッド exists</span><span class="sxs-lookup"><span data-stu-id="50445-2008">Method exists</span></span>

<span data-ttu-id="50445-2009">特定の項目が構造体に存在するかどうかを判定します。</span><span class="sxs-lookup"><span data-stu-id="50445-2009">Determines whether a particular item exists in a struct.</span></span>

    public boolean exists(str fieldName)

#### <a name="parameters"></a><span data-ttu-id="50445-2010">パラメーター</span><span class="sxs-lookup"><span data-stu-id="50445-2010">Parameters</span></span>

<span data-ttu-id="50445-2011">fieldName</span><span class="sxs-lookup"><span data-stu-id="50445-2011">fieldName</span></span>  
<span data-ttu-id="50445-2012">チェックするアイテムの名前。</span><span class="sxs-lookup"><span data-stu-id="50445-2012">The name of the item to check for.</span></span>

#### <a name="return-value"></a><span data-ttu-id="50445-2013">戻り値</span><span class="sxs-lookup"><span data-stu-id="50445-2013">Return Value</span></span>

<span data-ttu-id="50445-2014">項目が構造体内に存在する場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="50445-2014">true if the item exists in the struct; otherwise, false.</span></span>

#### <a name="examples"></a><span data-ttu-id="50445-2015">例</span><span class="sxs-lookup"><span data-stu-id="50445-2015">Examples</span></span>

<span data-ttu-id="50445-2016">次の例では、特定の項目が構造体に存在するかどうかを検査し、存在しない場合は、項目を追加し、Struct.add メソッドを使用して項目に値を割り当てます。</span><span class="sxs-lookup"><span data-stu-id="50445-2016">The following example tests whether a particular item exists in a struct, and if not, it adds the item and assigns a value to it using the Struct.add method.</span></span>

    client server static void setProp( 
        Struct     properties, 
        str        name, 
        anytype   value 
        ) 
    { 
        if (! properties.exists(name)) 
        { 
            properties.add(name,nullValue(value)); 
        } 
        properties.value(name,value); 
    }

### <a name="method-fieldname"></a><span data-ttu-id="50445-2017">メソッド fieldName</span><span class="sxs-lookup"><span data-stu-id="50445-2017">Method fieldName</span></span>

<span data-ttu-id="50445-2018">指定された位置にある構造体内の項目の名前を返します。</span><span class="sxs-lookup"><span data-stu-id="50445-2018">Returns the name of the item in the struct at the specified position.</span></span>

    public str fieldName(int index)

#### <a name="parameters"></a><span data-ttu-id="50445-2019">パラメーター</span><span class="sxs-lookup"><span data-stu-id="50445-2019">Parameters</span></span>

<span data-ttu-id="50445-2020">指数</span><span class="sxs-lookup"><span data-stu-id="50445-2020">index</span></span>  
<span data-ttu-id="50445-2021">項目名を取得する構造体内の位置。</span><span class="sxs-lookup"><span data-stu-id="50445-2021">The position in the struct at which you want to retrieve the item name.</span></span>

#### <a name="return-value"></a><span data-ttu-id="50445-2022">戻り値</span><span class="sxs-lookup"><span data-stu-id="50445-2022">Return Value</span></span>

<span data-ttu-id="50445-2023">インデックスで指定された位置にある項目の名前。</span><span class="sxs-lookup"><span data-stu-id="50445-2023">The name of the item at the position specified by index.</span></span>

#### <a name="remarks"></a><span data-ttu-id="50445-2024">備考</span><span class="sxs-lookup"><span data-stu-id="50445-2024">Remarks</span></span>

<span data-ttu-id="50445-2025">インデックスが見つからない場合は、空の文字列が返されます。</span><span class="sxs-lookup"><span data-stu-id="50445-2025">If index is not found, an empty string is returned.</span></span>

#### <a name="examples"></a><span data-ttu-id="50445-2026">例</span><span class="sxs-lookup"><span data-stu-id="50445-2026">Examples</span></span>

<span data-ttu-id="50445-2027">次の例では、コンテナーから構造体を作成し、Struct.fields メソッドを使用してコンテナーの内容を反復処理します。</span><span class="sxs-lookup"><span data-stu-id="50445-2027">The following example creates a struct from a container and then uses the Struct.fields method to iterate through the contents of the container.</span></span> <span data-ttu-id="50445-2028">fieldName メソッドは、構造体の各項目の名前をテストするために使用され、この名前の値に応じて特定のアクションが実行されます。</span><span class="sxs-lookup"><span data-stu-id="50445-2028">The fieldName method is used to test the name of each item in the struct, and a specific action is run depending on the value of this name.</span></span>

    boolean unpack(container packed) 
    { 
        Struct      unpackedProperties; 
        container   structCon; 
        Counter     i; 
        [#currentList,structCon] = packed; 
        unpackedProperties = Struct::create(structCon); 
        for (i=1;i<=unpackedProperties.fields();i++) 
        { 
            switch (unpackedProperties.fieldName(i)) 
            { 
                case #closedOk: 
                    break; 
                case #PropertyCaption: 
                    if (! dialogForm  
                        || dialogForm  
                        && ! dialogForm.form().design().caption()) 
                        this.caption(unpackedProperties.valueIndex(i)); 
                    break; 
                case #dialogFormname: 
                    // Do nothing 
                    break; 
                case #PropertyAlwaysOnTop: 
                    this.alwaysOnTop(unpackedProperties.valueIndex(i)); 
                    break; 
                case #PropertyWindowType: 
                    this.windowType(unpackedProperties.valueIndex(i)); 
                    break; 
                case #defaultButton: 
                    this.defaultButton(unpackedProperties.valueIndex(i)); 
                    break; 
                default: 
                    throw error(strfmt( 
                        "@SYS67326",unpackedProperties.fieldName(i), 
                         classId2Name(classidget(this)))); 
            } 
        } 
        return true; 
    }

### <a name="method-fields"></a><span data-ttu-id="50445-2029">メソッド fields</span><span class="sxs-lookup"><span data-stu-id="50445-2029">Method fields</span></span>

<span data-ttu-id="50445-2030">構造体内の項目の数を返します。</span><span class="sxs-lookup"><span data-stu-id="50445-2030">Returns the number of items in the struct.</span></span>

    public int fields()

#### <a name="return-value"></a><span data-ttu-id="50445-2031">戻り値</span><span class="sxs-lookup"><span data-stu-id="50445-2031">Return Value</span></span>

<span data-ttu-id="50445-2032">構造体内の項目の数。</span><span class="sxs-lookup"><span data-stu-id="50445-2032">The number of items in the struct.</span></span>

#### <a name="remarks"></a><span data-ttu-id="50445-2033">備考</span><span class="sxs-lookup"><span data-stu-id="50445-2033">Remarks</span></span>

<span data-ttu-id="50445-2034">構造体内の項目の位置を見つけるには、Struct.index メソッドを使用します。</span><span class="sxs-lookup"><span data-stu-id="50445-2034">To find the position of an item in a struct, use the Struct.index method.</span></span>

#### <a name="examples"></a><span data-ttu-id="50445-2035">例</span><span class="sxs-lookup"><span data-stu-id="50445-2035">Examples</span></span>

<span data-ttu-id="50445-2036">次の例では、コンテナーから構造体を作成し、フィールド メソッドを使用してコンテナーの内容を反復処理します。</span><span class="sxs-lookup"><span data-stu-id="50445-2036">The following example creates a struct from a container and then uses the fields method to iterate through the contents of the container.</span></span>

    boolean unpack(container packed) 
    { 
        Struct      unpackedProperties; 
        container   structCon; 
        Counter     i; 
        [#currentList,structCon] = packed; 
        unpackedProperties = Struct::create(structCon); 
        for (i=1;i<=unpackedProperties.fields();i++) 
        { 
            switch (unpackedProperties.fieldName(i)) 
            { 
                case #closedOk: 
                    break; 
                case #PropertyCaption: 
                    if (! dialogForm  
                        || dialogForm  
                        && ! dialogForm.form().design().caption()) 
                        this.caption(unpackedProperties.valueIndex(i)); 
                    break; 
                case #dialogFormname: 
                    // Do nothing 
                    break; 
                case #PropertyAlwaysOnTop: 
                    this.alwaysOnTop(unpackedProperties.valueIndex(i)); 
                    break; 
                case #PropertyWindowType: 
                    this.windowType(unpackedProperties.valueIndex(i)); 
                    break; 
                case #defaultButton: 
                    this.defaultButton(unpackedProperties.valueIndex(i)); 
                    break; 
                default: 
                    throw error(strfmt( 
                        "@SYS67326",unpackedProperties.fieldName(i), 
                         classId2Name(classidget(this)))); 
            } 
        } 
        return true; 
    }

### <a name="method-fieldtype"></a><span data-ttu-id="50445-2037">メソッド fieldType</span><span class="sxs-lookup"><span data-stu-id="50445-2037">Method fieldType</span></span>

<span data-ttu-id="50445-2038">指定された位置にある構造体内の項目のデータ型を返します。</span><span class="sxs-lookup"><span data-stu-id="50445-2038">Returns the data type of the item in the struct at the specified position.</span></span>

    public Types fieldType(int index)

#### <a name="parameters"></a><span data-ttu-id="50445-2039">パラメーター</span><span class="sxs-lookup"><span data-stu-id="50445-2039">Parameters</span></span>

<span data-ttu-id="50445-2040">指数</span><span class="sxs-lookup"><span data-stu-id="50445-2040">index</span></span>  
<span data-ttu-id="50445-2041">データ型を取得する構造体内の位置。</span><span class="sxs-lookup"><span data-stu-id="50445-2041">The position in the struct that you want to retrieve the data type for.</span></span>

#### <a name="return-value"></a><span data-ttu-id="50445-2042">戻り値</span><span class="sxs-lookup"><span data-stu-id="50445-2042">Return Value</span></span>

<span data-ttu-id="50445-2043">インデックスで指定された位置にある項目のデータ型。</span><span class="sxs-lookup"><span data-stu-id="50445-2043">The data type of the item at the position specified by index.</span></span>

#### <a name="remarks"></a><span data-ttu-id="50445-2044">備考</span><span class="sxs-lookup"><span data-stu-id="50445-2044">Remarks</span></span>

<span data-ttu-id="50445-2045">可能な値は、システム列挙で提供されます。</span><span class="sxs-lookup"><span data-stu-id="50445-2045">The possible values are supplied by the system enum.</span></span> <span data-ttu-id="50445-2046">インデックスが見つからない場合は、返す値は Types::void です。</span><span class="sxs-lookup"><span data-stu-id="50445-2046">If index is not found, the return value is Types::void.</span></span> <span data-ttu-id="50445-2047">Struct.index メソッドを使用することにより、構造体内の特定の品目の位置を決定することができます。</span><span class="sxs-lookup"><span data-stu-id="50445-2047">You can determine the position of a particular item in a struct by using the Struct.index method</span></span>

### <a name="method-index"></a><span data-ttu-id="50445-2048">メソッド index</span><span class="sxs-lookup"><span data-stu-id="50445-2048">Method index</span></span>

<span data-ttu-id="50445-2049">名前に基づいて構造体の項目の位置を計算します。</span><span class="sxs-lookup"><span data-stu-id="50445-2049">Calculates the position of an item in the struct based on its name.</span></span>

    public int index(str fieldName)

#### <a name="parameters"></a><span data-ttu-id="50445-2050">パラメーター</span><span class="sxs-lookup"><span data-stu-id="50445-2050">Parameters</span></span>

<span data-ttu-id="50445-2051">fieldName</span><span class="sxs-lookup"><span data-stu-id="50445-2051">fieldName</span></span>  
<span data-ttu-id="50445-2052">位置を返す項目の名前。</span><span class="sxs-lookup"><span data-stu-id="50445-2052">The name of the item for which to return the position.</span></span>

#### <a name="return-value"></a><span data-ttu-id="50445-2053">戻り値</span><span class="sxs-lookup"><span data-stu-id="50445-2053">Return Value</span></span>

<span data-ttu-id="50445-2054">項目の位置。</span><span class="sxs-lookup"><span data-stu-id="50445-2054">The position of the item.</span></span>

#### <a name="remarks"></a><span data-ttu-id="50445-2055">備考</span><span class="sxs-lookup"><span data-stu-id="50445-2055">Remarks</span></span>

<span data-ttu-id="50445-2056">構造体内の項目は、項目名に従ってアルファベット順に並べられます。</span><span class="sxs-lookup"><span data-stu-id="50445-2056">The items in a struct are arranged in alphabetical order according to the item names.</span></span> <span data-ttu-id="50445-2057">fieldName という名前の項目がない場合は、0 が返されます。</span><span class="sxs-lookup"><span data-stu-id="50445-2057">If there is no item with the name fieldName, 0 is returned.</span></span>

### <a name="method-pack"></a><span data-ttu-id="50445-2058">メソッド pack</span><span class="sxs-lookup"><span data-stu-id="50445-2058">Method pack</span></span>

<span data-ttu-id="50445-2059">Struct クラスの現在のインスタンスをシリアル化します。</span><span class="sxs-lookup"><span data-stu-id="50445-2059">Serializes the current instance of the Struct class.</span></span>

    public container pack()

#### <a name="return-value"></a><span data-ttu-id="50445-2060">戻り値</span><span class="sxs-lookup"><span data-stu-id="50445-2060">Return Value</span></span>

<span data-ttu-id="50445-2061">Struct クラスの現在のインスタンスを含むコンテナーです。</span><span class="sxs-lookup"><span data-stu-id="50445-2061">A container that contains the current instance of the Struct class.</span></span>

#### <a name="remarks"></a><span data-ttu-id="50445-2062">備考</span><span class="sxs-lookup"><span data-stu-id="50445-2062">Remarks</span></span>

<span data-ttu-id="50445-2063">pack メソッドは、オブジェクトを保持する各フィールドで呼び出され、(サブ) コンテナーを生成します。</span><span class="sxs-lookup"><span data-stu-id="50445-2063">The pack method is called on each field that holds an object, to yield a (sub) container.</span></span> <span data-ttu-id="50445-2064">構造体は、Struct.create メソッドを使用してコンテナーから再作成できます。</span><span class="sxs-lookup"><span data-stu-id="50445-2064">The struct may be recreated from the container by using the Struct.create method.</span></span>

#### <a name="examples"></a><span data-ttu-id="50445-2065">例</span><span class="sxs-lookup"><span data-stu-id="50445-2065">Examples</span></span>

<span data-ttu-id="50445-2066">次の例では、2 つの項目 (名前と年齢) を持つ構造体を作成し、項目に値を追加します。</span><span class="sxs-lookup"><span data-stu-id="50445-2066">The following example creates a struct with two items in it (name and age), and then adds values to the items.</span></span> <span data-ttu-id="50445-2067">構造体はコンテナーに梱包され、このコンテナーが使用されて新しい構造体が作成されます。</span><span class="sxs-lookup"><span data-stu-id="50445-2067">The struct is packed into a container, and this container is then used to create a new struct.</span></span>

    {  
        container packedStruct;  
        Struct s1, s = new Struct ("str name; int age"); 
        s.value ("name", "Jane Dow");  
        s.value ("age", 34); 
        // Struct is packed into a container 
        packedStruct = s.pack();  
        // A new struct is created from the container 
        s1 = Struct::create(packedStruct); 
        // Both structs have the same contents 
        print s.toString();  
        print s1.toString();  
        pause;  
    }

### <a name="method-remove"></a><span data-ttu-id="50445-2068">メソッド remove</span><span class="sxs-lookup"><span data-stu-id="50445-2068">Method remove</span></span>

<span data-ttu-id="50445-2069">構造体から品目を削除します。</span><span class="sxs-lookup"><span data-stu-id="50445-2069">Removes an item from a struct.</span></span>

    public boolean remove(str fieldName)

#### <a name="parameters"></a><span data-ttu-id="50445-2070">パラメーター</span><span class="sxs-lookup"><span data-stu-id="50445-2070">Parameters</span></span>

<span data-ttu-id="50445-2071">fieldName</span><span class="sxs-lookup"><span data-stu-id="50445-2071">fieldName</span></span>  
<span data-ttu-id="50445-2072">削除する項目の名前。</span><span class="sxs-lookup"><span data-stu-id="50445-2072">The name of the item you want to remove.</span></span>

#### <a name="return-value"></a><span data-ttu-id="50445-2073">戻り値</span><span class="sxs-lookup"><span data-stu-id="50445-2073">Return Value</span></span>

<span data-ttu-id="50445-2074">項目が見つかった (そして削除された) 場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="50445-2074">true if the item was found (and removed); otherwise, false.</span></span>

#### <a name="remarks"></a><span data-ttu-id="50445-2075">備考</span><span class="sxs-lookup"><span data-stu-id="50445-2075">Remarks</span></span>

<span data-ttu-id="50445-2076">fieldName パラメーターに指定する名前は、構造体のインスタンス化で指定されたアイテムの名前または Struct.add メソッドを使用して追加されたアイテムの名前でなければなりません。</span><span class="sxs-lookup"><span data-stu-id="50445-2076">The name you specify for the fieldName parameter must be the name of the item as it was specified in the instantiation of the struct or the name of the item as it was added using the Struct.add method.</span></span> <span data-ttu-id="50445-2077">名前は引用符 (" ") で囲む必要があります。</span><span class="sxs-lookup"><span data-stu-id="50445-2077">The name must be enclosed in quotes (" ").</span></span>

#### <a name="examples"></a><span data-ttu-id="50445-2078">例</span><span class="sxs-lookup"><span data-stu-id="50445-2078">Examples</span></span>

<span data-ttu-id="50445-2079">次の例では、2 つの項目を含む構造体を作成し、これらの項目の説明を出力します。</span><span class="sxs-lookup"><span data-stu-id="50445-2079">The following example creates a struct with two items in it and prints a description of these items.</span></span> <span data-ttu-id="50445-2080">品目のいずれかは、メソッドの削除を使用して削除されます。</span><span class="sxs-lookup"><span data-stu-id="50445-2080">One of the items is then removed by using the remove method.</span></span>

    { 
        Struct s = new Struct ("str name; int age"); 
        // Values are assigned to the two items 
        s.value("name", "John"); 
        s.value("age", 34); 
        // Prints a description of the items in the struct 
        print s.definitionString(); 
        pause; 
        // Removes the name field 
        s.remove("name"); 
        // Describes remaining items in the struct 
        print s.definitionString(); 
        pause; 
    }

### <a name="method-tostring"></a><span data-ttu-id="50445-2081">メソッド toString</span><span class="sxs-lookup"><span data-stu-id="50445-2081">Method toString</span></span>

<span data-ttu-id="50445-2082">構造体の内容を説明する文字列を返します。</span><span class="sxs-lookup"><span data-stu-id="50445-2082">Returns a string that describes the contents of the struct.</span></span>

    public str toString()

#### <a name="return-value"></a><span data-ttu-id="50445-2083">戻り値</span><span class="sxs-lookup"><span data-stu-id="50445-2083">Return Value</span></span>

<span data-ttu-id="50445-2084">構造体の内容を説明する文字列。</span><span class="sxs-lookup"><span data-stu-id="50445-2084">A string that describes the contents of the struct.</span></span>

### <a name="method-value"></a><span data-ttu-id="50445-2085">メソッド value</span><span class="sxs-lookup"><span data-stu-id="50445-2085">Method value</span></span>

<span data-ttu-id="50445-2086">構造体で指定される品目の値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="50445-2086">Gets or sets the value for a specified item in a struct.</span></span>

    public AnyType value(str fieldName, [AnyType value])

#### <a name="parameters"></a><span data-ttu-id="50445-2087">パラメーター</span><span class="sxs-lookup"><span data-stu-id="50445-2087">Parameters</span></span>

<span data-ttu-id="50445-2088">fieldName</span><span class="sxs-lookup"><span data-stu-id="50445-2088">fieldName</span></span>  
<span data-ttu-id="50445-2089">項目に割り当てる値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="50445-2089">The value to assign to the item; optional.</span></span>

<!-- -->

<span data-ttu-id="50445-2090">値</span><span class="sxs-lookup"><span data-stu-id="50445-2090">value</span></span>  
<span data-ttu-id="50445-2091">項目に割り当てる値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="50445-2091">The value to assign to the item; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="50445-2092">戻り値</span><span class="sxs-lookup"><span data-stu-id="50445-2092">Return Value</span></span>

<span data-ttu-id="50445-2093">指定項目の値。</span><span class="sxs-lookup"><span data-stu-id="50445-2093">The value of the specified item.</span></span>

#### <a name="remarks"></a><span data-ttu-id="50445-2094">備考</span><span class="sxs-lookup"><span data-stu-id="50445-2094">Remarks</span></span>

<span data-ttu-id="50445-2095">構造体内で指定された名前に項目がない場合は例外が発生します。</span><span class="sxs-lookup"><span data-stu-id="50445-2095">An exception is raised if there is no item with the specified name in the struct.</span></span> <span data-ttu-id="50445-2096">構造体内の項目名は、Struct.fieldName メソッドを使用して取得できます。</span><span class="sxs-lookup"><span data-stu-id="50445-2096">The name of an item in a struct may be retrieved by using the Struct.fieldName method.</span></span> <span data-ttu-id="50445-2097">Struct.add メソッドを使用することにより、新しい品目を構造体に追加すると同時に値を割り当てることができます。</span><span class="sxs-lookup"><span data-stu-id="50445-2097">You can add a new item to a struct and assign a value to it at the same time by using the Struct.add method.</span></span> <span data-ttu-id="50445-2098">構造体内の位置に基づいてアイテムに新しい値を割り当てるには、Struct.valueIndex メソッドを使用します。</span><span class="sxs-lookup"><span data-stu-id="50445-2098">To assign a new value to an item based on its position in the struct, use the Struct.valueIndex method.</span></span>

#### <a name="examples"></a><span data-ttu-id="50445-2099">例</span><span class="sxs-lookup"><span data-stu-id="50445-2099">Examples</span></span>

<span data-ttu-id="50445-2100">次の例では、2 つの項目を含む構造体を作成し、value メソッドを使用してこれらの 2 つの項目に値を割り当てます。</span><span class="sxs-lookup"><span data-stu-id="50445-2100">The following example creates a struct with two items in it and then uses the value method to assign values to those two items.</span></span>

    { 
        Struct s = new Struct ("str name; int age"); 
        // Set the values 
        s.value("name", "Jane Dow"); 
        s.value("age", 34); 
        // Print the values 
        print s.value("name"); 
        print s.value("age"); 
        pause; 
    }

### <a name="method-valueimage"></a><span data-ttu-id="50445-2101">メソッド valueImage</span><span class="sxs-lookup"><span data-stu-id="50445-2101">Method valueImage</span></span>

<span data-ttu-id="50445-2102">構造体内の特定の位置にある品目の値を説明する文字列を返します。</span><span class="sxs-lookup"><span data-stu-id="50445-2102">Returns a string that describes the value of the item at a particular position in the struct.</span></span>

    public str valueImage(int index)

#### <a name="parameters"></a><span data-ttu-id="50445-2103">パラメーター</span><span class="sxs-lookup"><span data-stu-id="50445-2103">Parameters</span></span>

<span data-ttu-id="50445-2104">指数</span><span class="sxs-lookup"><span data-stu-id="50445-2104">index</span></span>  
<span data-ttu-id="50445-2105">説明を返す項目の位置。</span><span class="sxs-lookup"><span data-stu-id="50445-2105">The position of the item that you want to return a description for.</span></span>

#### <a name="return-value"></a><span data-ttu-id="50445-2106">戻り値</span><span class="sxs-lookup"><span data-stu-id="50445-2106">Return Value</span></span>

<span data-ttu-id="50445-2107">品目の価値を説明する文字列。</span><span class="sxs-lookup"><span data-stu-id="50445-2107">A string that describes the value of the item.</span></span>

#### <a name="remarks"></a><span data-ttu-id="50445-2108">備考</span><span class="sxs-lookup"><span data-stu-id="50445-2108">Remarks</span></span>

<span data-ttu-id="50445-2109">構造体内の項目は、項目の名前に従ってアルファベット順に表示されます。</span><span class="sxs-lookup"><span data-stu-id="50445-2109">The items in a struct are in alphabetical order according to the names of the items.</span></span> <span data-ttu-id="50445-2110">インデックスで指定された位置に項目がない場合は例外が発生します。</span><span class="sxs-lookup"><span data-stu-id="50445-2110">If there is no item at the position specified by index, an exception is raised.</span></span>

### <a name="method-valueindex"></a><span data-ttu-id="50445-2111">メソッド valueIndex</span><span class="sxs-lookup"><span data-stu-id="50445-2111">Method valueIndex</span></span>

<span data-ttu-id="50445-2112">構造体で指定される位置での品目の値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="50445-2112">Gets or sets the value of the item at a specified position in a struct.</span></span>

    public AnyType valueIndex(int index, [AnyType value])

#### <a name="parameters"></a><span data-ttu-id="50445-2113">パラメーター</span><span class="sxs-lookup"><span data-stu-id="50445-2113">Parameters</span></span>

<span data-ttu-id="50445-2114">指数</span><span class="sxs-lookup"><span data-stu-id="50445-2114">index</span></span>  
<span data-ttu-id="50445-2115">インデックスで指定された位置のアイテムに割り当てる値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="50445-2115">The value to assign to the item at the position specified by index; optional.</span></span>

<!-- -->

<span data-ttu-id="50445-2116">値</span><span class="sxs-lookup"><span data-stu-id="50445-2116">value</span></span>  
<span data-ttu-id="50445-2117">インデックスで指定された位置のアイテムに割り当てる値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="50445-2117">The value to assign to the item at the position specified by index; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="50445-2118">戻り値</span><span class="sxs-lookup"><span data-stu-id="50445-2118">Return Value</span></span>

<span data-ttu-id="50445-2119">インデックスで指定された位置にある項目の値。</span><span class="sxs-lookup"><span data-stu-id="50445-2119">The value of the item at the position specified by index.</span></span>

#### <a name="remarks"></a><span data-ttu-id="50445-2120">備考</span><span class="sxs-lookup"><span data-stu-id="50445-2120">Remarks</span></span>

<span data-ttu-id="50445-2121">インデックスで指定された位置に項目がない場合は例外が発生します。</span><span class="sxs-lookup"><span data-stu-id="50445-2121">An exception is raised if there is no item at the position specified by index.</span></span> <span data-ttu-id="50445-2122">構造体内の項目の位置は、Struct.index メソッドを使用して取得できます。</span><span class="sxs-lookup"><span data-stu-id="50445-2122">The position of an item in a struct can be retrieved by using the Struct.index method.</span></span>

### <a name="method-xml"></a><span data-ttu-id="50445-2123">メソッド xml</span><span class="sxs-lookup"><span data-stu-id="50445-2123">Method xml</span></span>

<span data-ttu-id="50445-2124">現在のオブジェクトを表す XML 文字列を返します。</span><span class="sxs-lookup"><span data-stu-id="50445-2124">Returns an XML string that represents the current object.</span></span>

    public str xml([int indent])

#### <a name="parameters"></a><span data-ttu-id="50445-2125">パラメーター</span><span class="sxs-lookup"><span data-stu-id="50445-2125">Parameters</span></span>

<span data-ttu-id="50445-2126">インデント</span><span class="sxs-lookup"><span data-stu-id="50445-2126">indent</span></span>  
<span data-ttu-id="50445-2127">返された XML 文字列のインデントの量 (省略可能)。</span><span class="sxs-lookup"><span data-stu-id="50445-2127">The amount of indentation of the returned XML string; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="50445-2128">戻り値</span><span class="sxs-lookup"><span data-stu-id="50445-2128">Return Value</span></span>

<span data-ttu-id="50445-2129">現在のオブジェクトを表す XML 文字列です。</span><span class="sxs-lookup"><span data-stu-id="50445-2129">An XML string that represents the current object.</span></span>

#### <a name="remarks"></a><span data-ttu-id="50445-2130">備考</span><span class="sxs-lookup"><span data-stu-id="50445-2130">Remarks</span></span>

<span data-ttu-id="50445-2131">このメソッドをオーバーライドして、その型に対して意味のある値を返すことができます。</span><span class="sxs-lookup"><span data-stu-id="50445-2131">This method can be overridden to return values that are meaningful for that type.</span></span>

### <a name="method-create"></a><span data-ttu-id="50445-2132">メソッド create</span><span class="sxs-lookup"><span data-stu-id="50445-2132">Method create</span></span>

<span data-ttu-id="50445-2133">以前の Struct.pack の呼び出しで取得されたコンテナーから構造体を作成します。</span><span class="sxs-lookup"><span data-stu-id="50445-2133">Creates a struct from a container that is obtained from a prior call to Struct.pack.</span></span>

    public static Struct create(container container)

#### <a name="parameters"></a><span data-ttu-id="50445-2134">パラメーター</span><span class="sxs-lookup"><span data-stu-id="50445-2134">Parameters</span></span>

<span data-ttu-id="50445-2135">コンテナー</span><span class="sxs-lookup"><span data-stu-id="50445-2135">container</span></span>  
<span data-ttu-id="50445-2136">梱包済みの構造体を含むコンテナーです。</span><span class="sxs-lookup"><span data-stu-id="50445-2136">A container that contains the packed struct.</span></span>

#### <a name="return-value"></a><span data-ttu-id="50445-2137">戻り値</span><span class="sxs-lookup"><span data-stu-id="50445-2137">Return Value</span></span>

<span data-ttu-id="50445-2138">特定のコンテナーに梱包されたものと同じ構造体。</span><span class="sxs-lookup"><span data-stu-id="50445-2138">A struct equal to the one that was packed into the specified container.</span></span>

#### <a name="remarks"></a><span data-ttu-id="50445-2139">備考</span><span class="sxs-lookup"><span data-stu-id="50445-2139">Remarks</span></span>

<span data-ttu-id="50445-2140">構造体にオブジェクトが含まれている場合、これらのオブジェクトにはコンテナーからその内部状態を再設定するために呼び出されるアンパック メソッドが必要です。</span><span class="sxs-lookup"><span data-stu-id="50445-2140">If the struct contains objects, these objects must have an unpack method that is called to re-establish their internal state from the container.</span></span>

#### <a name="examples"></a><span data-ttu-id="50445-2141">例</span><span class="sxs-lookup"><span data-stu-id="50445-2141">Examples</span></span>

<span data-ttu-id="50445-2142">次の例では、2 つの項目 (名前と年齢) を持つ構造体を作成し、項目に値を追加します。</span><span class="sxs-lookup"><span data-stu-id="50445-2142">The following example creates a struct with two items in it (name and age), and then adds values to the items.</span></span> <span data-ttu-id="50445-2143">構造体はコンテナーに梱包され、このコンテナーは開梱されて新しい構造体が作成されます。</span><span class="sxs-lookup"><span data-stu-id="50445-2143">The struct is packed into a container, and this container is then unpacked to create a new struct.</span></span>

    {  
        container packedStruct;  
        Struct s1, s = new Struct ("str name; int age"); 
        s.value ("name", "Jane Dow");  
        s.value ("age", 34); 
        // Struct is packed into a container 
        packedStruct = s.pack();  
        // A new struct is created from the container 
        s1 = Struct::create(packedStruct); 
        // Both structs have the same contents 
        print s.toString();  
        print s1.toString();  
        pause;  
    }

### <a name="method-createfromxml"></a><span data-ttu-id="50445-2144">メソッド createFromXML</span><span class="sxs-lookup"><span data-stu-id="50445-2144">Method createFromXML</span></span>

    public static Struct createFromXML(Object xmlnode)

#### <a name="parameters"></a><span data-ttu-id="50445-2145">パラメーター</span><span class="sxs-lookup"><span data-stu-id="50445-2145">Parameters</span></span>

<span data-ttu-id="50445-2146">xmlnode</span><span class="sxs-lookup"><span data-stu-id="50445-2146">xmlnode</span></span>  

#### <a name="return-value"></a><span data-ttu-id="50445-2147">戻り値</span><span class="sxs-lookup"><span data-stu-id="50445-2147">Return Value</span></span>

### <a name="method-equal"></a><span data-ttu-id="50445-2148">メソッド equal</span><span class="sxs-lookup"><span data-stu-id="50445-2148">Method equal</span></span>

<span data-ttu-id="50445-2149">2 つの構造体が等しいかどうかを判断します。</span><span class="sxs-lookup"><span data-stu-id="50445-2149">Determines whether two structs are equal.</span></span>

    public static boolean equal(Struct struct1, Struct struct2)

#### <a name="parameters"></a><span data-ttu-id="50445-2150">パラメーター</span><span class="sxs-lookup"><span data-stu-id="50445-2150">Parameters</span></span>

<span data-ttu-id="50445-2151">struct1</span><span class="sxs-lookup"><span data-stu-id="50445-2151">struct1</span></span>  
<span data-ttu-id="50445-2152">比較される 2 つの構造体のうちの 2 番目の構造体。</span><span class="sxs-lookup"><span data-stu-id="50445-2152">The second of the two structs to be compared.</span></span>

<!-- -->

<span data-ttu-id="50445-2153">struct2</span><span class="sxs-lookup"><span data-stu-id="50445-2153">struct2</span></span>  
<span data-ttu-id="50445-2154">比較される 2 つの構造体のうちの 2 番目の構造体。</span><span class="sxs-lookup"><span data-stu-id="50445-2154">The second of the two structs to be compared.</span></span>

#### <a name="return-value"></a><span data-ttu-id="50445-2155">戻り値</span><span class="sxs-lookup"><span data-stu-id="50445-2155">Return Value</span></span>

<span data-ttu-id="50445-2156">構造体が等しい場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="50445-2156">true if the structs are equal; otherwise, false.</span></span>

#### <a name="remarks"></a><span data-ttu-id="50445-2157">備考</span><span class="sxs-lookup"><span data-stu-id="50445-2157">Remarks</span></span>

<span data-ttu-id="50445-2158">同じ数のフィールドを持ち、フィールド名が同じで、各フィールドが同じ型で同じ値を持つ場合、2 つの構造体は同等です。</span><span class="sxs-lookup"><span data-stu-id="50445-2158">Two structs are equal if they have the same number of fields, the field names are the same, and each field is the same type and has the same value.</span></span>

### <a name="method-merge"></a><span data-ttu-id="50445-2159">メソッド merge</span><span class="sxs-lookup"><span data-stu-id="50445-2159">Method merge</span></span>

<span data-ttu-id="50445-2160">2 つの構造体を組み合わせ、新しい構造体を作成します。</span><span class="sxs-lookup"><span data-stu-id="50445-2160">Combines two structs to create a new struct.</span></span>

    public static Struct merge(Struct struct1, Struct struct2)

#### <a name="parameters"></a><span data-ttu-id="50445-2161">パラメーター</span><span class="sxs-lookup"><span data-stu-id="50445-2161">Parameters</span></span>

<span data-ttu-id="50445-2162">struct1</span><span class="sxs-lookup"><span data-stu-id="50445-2162">struct1</span></span>  
<span data-ttu-id="50445-2163">新しい構造体を作成するために最初の構造体の最後に追加される構造体。</span><span class="sxs-lookup"><span data-stu-id="50445-2163">The struct that will be added to the end of the first struct to create a new struct.</span></span>

<!-- -->

<span data-ttu-id="50445-2164">struct2</span><span class="sxs-lookup"><span data-stu-id="50445-2164">struct2</span></span>  
<span data-ttu-id="50445-2165">新しい構造体を作成するために最初の構造体の最後に追加される構造体。</span><span class="sxs-lookup"><span data-stu-id="50445-2165">The struct that will be added to the end of the first struct to create a new struct.</span></span>

#### <a name="return-value"></a><span data-ttu-id="50445-2166">戻り値</span><span class="sxs-lookup"><span data-stu-id="50445-2166">Return Value</span></span>

<span data-ttu-id="50445-2167">新しい構造体。</span><span class="sxs-lookup"><span data-stu-id="50445-2167">The new struct.</span></span>

#### <a name="remarks"></a><span data-ttu-id="50445-2168">備考</span><span class="sxs-lookup"><span data-stu-id="50445-2168">Remarks</span></span>

<span data-ttu-id="50445-2169">struct2 は struct1 の最後に追加されます。</span><span class="sxs-lookup"><span data-stu-id="50445-2169">struct2 is added to the end of struct1.</span></span> <span data-ttu-id="50445-2170">つまり、新しい構造体の項目の順序は、項目名のアルファベット順に並べられた struct1 のすべての項目と、項目名のアルファベット順に並べられた struct2 のすべての項目です。</span><span class="sxs-lookup"><span data-stu-id="50445-2170">This means that the order of the items in the new struct will be: all the items in struct1, arranged in alphabetical order of the item names, followed by all the items in struct2, arranged in alphabetical order of the item names.</span></span> <span data-ttu-id="50445-2171">両方の構造体に同じ名前を持つ品目が含まれている場合は、最初の構造体からの品目のみが含まれるようになります。</span><span class="sxs-lookup"><span data-stu-id="50445-2171">If both structs contain an item with the same name, only the item from the first struct will be included.</span></span>

#### <a name="examples"></a><span data-ttu-id="50445-2172">例</span><span class="sxs-lookup"><span data-stu-id="50445-2172">Examples</span></span>

<span data-ttu-id="50445-2173">次の例では、person と address という 2 つの構造体を作成し、それらを allInfo という新しい構造体にマージします。</span><span class="sxs-lookup"><span data-stu-id="50445-2173">The following example creates two structs called person and address, and then merges them into a new struct called allInfo.</span></span>

    { 
        container packedStruct; 
        Struct person = new Struct ("str name; int age"); 
        Struct address = new Struct ("str street; str city; str country"); 
        Struct allInfo; 
        person.value ("name", "Jane Dow"); 
        person.value ("age", 34); 
        address.value ("street", "Downing street 10"); 
        address.value ("country", "Great Britain"); 
        address.value ("city", " London"); 
        allInfo = Struct::merge(person, address); 
        print allInfo.toString(); 
        pause; 
    }

### <a name="method-new"></a><span data-ttu-id="50445-2174">メソッド new</span><span class="sxs-lookup"><span data-stu-id="50445-2174">Method new</span></span>

<span data-ttu-id="50445-2175">構造体を作成します。</span><span class="sxs-lookup"><span data-stu-id="50445-2175">Creates a struct.</span></span>

    public void new(VarArg specifier)

#### <a name="parameters"></a><span data-ttu-id="50445-2176">パラメーター</span><span class="sxs-lookup"><span data-stu-id="50445-2176">Parameters</span></span>

<span data-ttu-id="50445-2177">指定子</span><span class="sxs-lookup"><span data-stu-id="50445-2177">specifier</span></span>  
<span data-ttu-id="50445-2178">文字列として品目の名前の後には、品目のデータ型を指定した 1 つ以上の組み合わせ。</span><span class="sxs-lookup"><span data-stu-id="50445-2178">One or more pairs that specify the data type of an item followed by the name of the item as a string.</span></span>

#### <a name="remarks"></a><span data-ttu-id="50445-2179">備考</span><span class="sxs-lookup"><span data-stu-id="50445-2179">Remarks</span></span>

<span data-ttu-id="50445-2180">項目のデータ型は、プリミティブ データ型の名前を使用するか、システム列挙を使用して指定できます。</span><span class="sxs-lookup"><span data-stu-id="50445-2180">The data type of the item can be specified using the name of a primitive data type or by using the system enum.</span></span> <span data-ttu-id="50445-2181">構造体内の項目は、文字列型、整数型、実数型、日付型、コンテナー型、レコード型、クラス型など、型システムの列挙型にあるデータ型のいずれでもかまいません。</span><span class="sxs-lookup"><span data-stu-id="50445-2181">The items in a struct can be of any of the data types found in the Types system enum, including: string, integer, real, date, container, record, and class.</span></span> <span data-ttu-id="50445-2182">以下の例に説明されているように、Struct.definitionString メソッドを使用して新しい構造体を作成し、構造体のコピーを作成することができます。</span><span class="sxs-lookup"><span data-stu-id="50445-2182">You can create a copy of a struct by using the Struct.definitionString method to create a new struct, as illustrated in the example below.</span></span> <span data-ttu-id="50445-2183">構造体を作成した後は、Struct.add メソッドを使用して新しい項目を追加し、Struct.value または Struct.valueIndex メソッドを使用して構造体に項目の値を設定することができます。</span><span class="sxs-lookup"><span data-stu-id="50445-2183">After you have created a struct, you can add new items using the Struct.add method and set the value of items in the struct by using the Struct.value or Struct.valueIndex method.</span></span>

#### <a name="examples"></a><span data-ttu-id="50445-2184">例</span><span class="sxs-lookup"><span data-stu-id="50445-2184">Examples</span></span>

<span data-ttu-id="50445-2185">次の例では、同じ定義を持つ 2 つの構造体を作成し、2 つの値と追加の項目および値をその 1 つ (s1) に追加します。</span><span class="sxs-lookup"><span data-stu-id="50445-2185">The following example creates two structs with the same definition and then adds 2 values and an additional item and value to one of them (s1).</span></span> <span data-ttu-id="50445-2186">この構造体をコピーして、Struct.definitionString メソッドを使用することにより新しい構造体を作成します。</span><span class="sxs-lookup"><span data-stu-id="50445-2186">This struct is then copied to create a new struct by using the Struct.definitionString method.</span></span>

    { 
        Struct s1, s2, s3; 
        // The two constructors below create the same struct 
        s1 = new Struct(Types::Integer, "age", Types::String, "name"); 
        s2 = new Struct ("int age; str name"); 
        // Print the definitions 
        print s1.definitionString(); 
        print s2.definitionString(); 
        s1.value("age", 25); 
        s1.value("name", "Jane Dow"); 
        // Add a field at runtime 
        s1.add("Shoesize", 45); 
        print s1.definitionString(); 
        print s1.toString(); 
        // Create a container with age, name and shoesize, 
        // using definitionString 
        s3 = new struct(s1.definitionString()); 
        print s3.definitionString(); 
        pause; 
    }

## <a name="class-surrogatefkreplacementhelper"></a><span data-ttu-id="50445-2187">クラス SurrogateFKReplacementHelper</span><span class="sxs-lookup"><span data-stu-id="50445-2187">Class SurrogateFKReplacementHelper</span></span>
    class SurrogateFKReplacementHelper extends Object

### <a name="remarks"></a><span data-ttu-id="50445-2188">備考</span><span class="sxs-lookup"><span data-stu-id="50445-2188">Remarks</span></span>

### <a name="examples"></a><span data-ttu-id="50445-2189">例</span><span class="sxs-lookup"><span data-stu-id="50445-2189">Examples</span></span>

### <a name="methods"></a><span data-ttu-id="50445-2190">メソッド</span><span class="sxs-lookup"><span data-stu-id="50445-2190">Methods</span></span>

| <span data-ttu-id="50445-2191">方法</span><span class="sxs-lookup"><span data-stu-id="50445-2191">Method</span></span>                                                                                                                                                                                                             | <span data-ttu-id="50445-2192">説明</span><span class="sxs-lookup"><span data-stu-id="50445-2192">Description</span></span>                                     |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------|
| <span data-ttu-id="50445-2193">public Map addDefaultRequiredJoins(QueryBuildDataSource foreignKeyQueryBuildDataSource, str replacementFieldGroupName)</span><span class="sxs-lookup"><span data-stu-id="50445-2193">public Map addDefaultRequiredJoins(QueryBuildDataSource foreignKeyQueryBuildDataSource, str replacementFieldGroupName)</span></span>                                                                                             |                                                 |
| <span data-ttu-id="50445-2194">public Map addRequiredJoins(List requiredJoinsAsRelationPathList, QueryBuildDataSource foreignKeyQueryBuildDataSource, str replacementFieldGroupName)</span><span class="sxs-lookup"><span data-stu-id="50445-2194">public Map addRequiredJoins(List requiredJoinsAsRelationPathList, QueryBuildDataSource foreignKeyQueryBuildDataSource, str replacementFieldGroupName)</span></span>                                                              |                                                 |
| <span data-ttu-id="50445-2195">public List displayBindings(str replacementFieldGroupName, \[boolean distinctBindingsOnly\])</span><span class="sxs-lookup"><span data-stu-id="50445-2195">public List displayBindings(str replacementFieldGroupName, \[boolean distinctBindingsOnly\])</span></span>                                                                                                                       |                                                 |
| <span data-ttu-id="50445-2196">public List displayValuesFromQueryRun(QueryRun queryRun, str replacementFieldGroupName, \[boolean isRootPrimaryKeyDataSource\], \[boolean trimSecuredValues\], \[boolean distinctBindingsOnly\])</span><span class="sxs-lookup"><span data-stu-id="50445-2196">public List displayValuesFromQueryRun(QueryRun queryRun, str replacementFieldGroupName, \[boolean isRootPrimaryKeyDataSource\], \[boolean trimSecuredValues\], \[boolean distinctBindingsOnly\])</span></span>                   |                                                 |
| <span data-ttu-id="50445-2197">public List displayValuesFromRecID(Int64 recIDValue, str replacementFieldGroupName, \[boolean trimSecuredValues\], \[boolean distinctBindingsOnly\])</span><span class="sxs-lookup"><span data-stu-id="50445-2197">public List displayValuesFromRecID(Int64 recIDValue, str replacementFieldGroupName, \[boolean trimSecuredValues\], \[boolean distinctBindingsOnly\])</span></span>                                                               |                                                 |
| <span data-ttu-id="50445-2198">public List displayValuesFromRootDS(QueryBuildDataSource rootQueryBuildDataSource, boolean isPrimaryKeyDataSource, str replacementFieldGroupName, \[boolean trimSecuredValues\], \[boolean distinctBindingsOnly\])</span><span class="sxs-lookup"><span data-stu-id="50445-2198">public List displayValuesFromRootDS(QueryBuildDataSource rootQueryBuildDataSource, boolean isPrimaryKeyDataSource, str replacementFieldGroupName, \[boolean trimSecuredValues\], \[boolean distinctBindingsOnly\])</span></span> |                                                 |
| <span data-ttu-id="50445-2199">public FilterValue displayValue(Common resolvedCursor, FieldBinding displayBinding, \[boolean isRootPrimaryKeyDataSource\])</span><span class="sxs-lookup"><span data-stu-id="50445-2199">public FilterValue displayValue(Common resolvedCursor, FieldBinding displayBinding, \[boolean isRootPrimaryKeyDataSource\])</span></span>                                                                                        |                                                 |
| <span data-ttu-id="50445-2200">public str extendedDataType()</span><span class="sxs-lookup"><span data-stu-id="50445-2200">public str extendedDataType()</span></span>                                                                                                                                                                                      |                                                 |
| <span data-ttu-id="50445-2201">public Query generateResolveReferenceQuery(List requiredJoinsAsRelationPathList, List filterValuesAsFilterValueList)</span><span class="sxs-lookup"><span data-stu-id="50445-2201">public Query generateResolveReferenceQuery(List requiredJoinsAsRelationPathList, List filterValuesAsFilterValueList)</span></span>                                                                                               |                                                 |
| <span data-ttu-id="50445-2202">public boolean isResolvedReferenceAmbiguous(Query query)</span><span class="sxs-lookup"><span data-stu-id="50445-2202">public boolean isResolvedReferenceAmbiguous(Query query)</span></span>                                                                                                                                                           |                                                 |
| <span data-ttu-id="50445-2203">public str primaryKeyTableName()</span><span class="sxs-lookup"><span data-stu-id="50445-2203">public str primaryKeyTableName()</span></span>                                                                                                                                                                                   |                                                 |
| <span data-ttu-id="50445-2204">public Map queryBuildDataSourceBindingsForQuery(Query query, str replacementFieldGroupName, \[boolean isRootPrimaryKeyDataSource\])</span><span class="sxs-lookup"><span data-stu-id="50445-2204">public Map queryBuildDataSourceBindingsForQuery(Query query, str replacementFieldGroupName, \[boolean isRootPrimaryKeyDataSource\])</span></span>                                                                                |                                                 |
| <span data-ttu-id="50445-2205">public Map queryBuildDataSourceBindingsForRootDS(QueryBuildDataSource rootQueryBuildDataSource, boolean isPrimaryKeyDataSource, str replacementFieldGroupName)</span><span class="sxs-lookup"><span data-stu-id="50445-2205">public Map queryBuildDataSourceBindingsForRootDS(QueryBuildDataSource rootQueryBuildDataSource, boolean isPrimaryKeyDataSource, str replacementFieldGroupName)</span></span>                                                     |                                                 |
| <span data-ttu-id="50445-2206">public Common resolveReference(Query query, \[boolean ignoreAmbiguousReference\])</span><span class="sxs-lookup"><span data-stu-id="50445-2206">public Common resolveReference(Query query, \[boolean ignoreAmbiguousReference\])</span></span>                                                                                                                                  |                                                 |
| <span data-ttu-id="50445-2207">public FieldBinding surrogateForeignKeyFieldBinding()</span><span class="sxs-lookup"><span data-stu-id="50445-2207">public FieldBinding surrogateForeignKeyFieldBinding()</span></span>                                                                                                                                                              |                                                 |
| <span data-ttu-id="50445-2208">::public static SurrogateFKReplacementHelper construct(FieldBinding surrogateForeignKeyBinding)</span><span class="sxs-lookup"><span data-stu-id="50445-2208">::public static SurrogateFKReplacementHelper construct(FieldBinding surrogateForeignKeyBinding)</span></span>                                                                                                                    |                                                 |
| <span data-ttu-id="50445-2209">::public static SurrogateFKReplacementHelper constructForEDT(str edtName)</span><span class="sxs-lookup"><span data-stu-id="50445-2209">::public static SurrogateFKReplacementHelper constructForEDT(str edtName)</span></span>                                                                                                                                          |                                                 |
| <span data-ttu-id="50445-2210">::public static SurrogateFKReplacementHelper constructForPKTable(str pkTableName)</span><span class="sxs-lookup"><span data-stu-id="50445-2210">::public static SurrogateFKReplacementHelper constructForPKTable(str pkTableName)</span></span>                                                                                                                                  |                                                 |
| <span data-ttu-id="50445-2211">::public static str defaultPrimaryKeyQueryDataSourceName()</span><span class="sxs-lookup"><span data-stu-id="50445-2211">::public static str defaultPrimaryKeyQueryDataSourceName()</span></span>                                                                                                                                                         |                                                 |
| <span data-ttu-id="50445-2212">::public static str DEPRECATED\_WorkflowCaption(str tableName, str fieldName, Int64 recIDValue)</span><span class="sxs-lookup"><span data-stu-id="50445-2212">::public static str DEPRECATED\_WorkflowCaption(str tableName, str fieldName, Int64 recIDValue)</span></span>                                                                                                                    |                                                 |
| <span data-ttu-id="50445-2213">::public static str implicitReplacementFieldGroupName()</span><span class="sxs-lookup"><span data-stu-id="50445-2213">::public static str implicitReplacementFieldGroupName()</span></span>                                                                                                                                                            |                                                 |
| <span data-ttu-id="50445-2214">private void new(FieldBinding surrogateForeignKeyBinding)</span><span class="sxs-lookup"><span data-stu-id="50445-2214">private void new(FieldBinding surrogateForeignKeyBinding)</span></span>                                                                                                                                                          | <span data-ttu-id="50445-2215">Object クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="50445-2215">Initializes a new instance of the Object class.</span></span> |

### <a name="method-adddefaultrequiredjoins"></a><span data-ttu-id="50445-2216">メソッド addDefaultRequiredJoins</span><span class="sxs-lookup"><span data-stu-id="50445-2216">Method addDefaultRequiredJoins</span></span>

    public Map addDefaultRequiredJoins(QueryBuildDataSource foreignKeyQueryBuildDataSource, str replacementFieldGroupName)

#### <a name="parameters"></a><span data-ttu-id="50445-2217">パラメーター</span><span class="sxs-lookup"><span data-stu-id="50445-2217">Parameters</span></span>

<span data-ttu-id="50445-2218">foreignKeyQueryBuildDataSource</span><span class="sxs-lookup"><span data-stu-id="50445-2218">foreignKeyQueryBuildDataSource</span></span>  

<!-- -->

<span data-ttu-id="50445-2219">replacementFieldGroupName</span><span class="sxs-lookup"><span data-stu-id="50445-2219">replacementFieldGroupName</span></span>  

#### <a name="return-value"></a><span data-ttu-id="50445-2220">戻り値</span><span class="sxs-lookup"><span data-stu-id="50445-2220">Return Value</span></span>

### <a name="method-addrequiredjoins"></a><span data-ttu-id="50445-2221">メソッド addRequiredJoins</span><span class="sxs-lookup"><span data-stu-id="50445-2221">Method addRequiredJoins</span></span>

    public Map addRequiredJoins(List requiredJoinsAsRelationPathList, QueryBuildDataSource foreignKeyQueryBuildDataSource, str replacementFieldGroupName)

#### <a name="parameters"></a><span data-ttu-id="50445-2222">パラメーター</span><span class="sxs-lookup"><span data-stu-id="50445-2222">Parameters</span></span>

<span data-ttu-id="50445-2223">requiredJoinsAsRelationPathList</span><span class="sxs-lookup"><span data-stu-id="50445-2223">requiredJoinsAsRelationPathList</span></span>  

<!-- -->

<span data-ttu-id="50445-2224">foreignKeyQueryBuildDataSource</span><span class="sxs-lookup"><span data-stu-id="50445-2224">foreignKeyQueryBuildDataSource</span></span>  

<!-- -->

<span data-ttu-id="50445-2225">replacementFieldGroupName</span><span class="sxs-lookup"><span data-stu-id="50445-2225">replacementFieldGroupName</span></span>  

#### <a name="return-value"></a><span data-ttu-id="50445-2226">戻り値</span><span class="sxs-lookup"><span data-stu-id="50445-2226">Return Value</span></span>

### <a name="method-displaybindings"></a><span data-ttu-id="50445-2227">メソッド displayBindings</span><span class="sxs-lookup"><span data-stu-id="50445-2227">Method displayBindings</span></span>

    public List displayBindings(str replacementFieldGroupName, [boolean distinctBindingsOnly])

#### <a name="parameters"></a><span data-ttu-id="50445-2228">パラメーター</span><span class="sxs-lookup"><span data-stu-id="50445-2228">Parameters</span></span>

<span data-ttu-id="50445-2229">replacementFieldGroupName</span><span class="sxs-lookup"><span data-stu-id="50445-2229">replacementFieldGroupName</span></span>  

<!-- -->

<span data-ttu-id="50445-2230">distinctBindingsOnly</span><span class="sxs-lookup"><span data-stu-id="50445-2230">distinctBindingsOnly</span></span>  

#### <a name="return-value"></a><span data-ttu-id="50445-2231">戻り値</span><span class="sxs-lookup"><span data-stu-id="50445-2231">Return Value</span></span>

### <a name="method-displayvaluesfromqueryrun"></a><span data-ttu-id="50445-2232">メソッド displayValuesFromQueryRun</span><span class="sxs-lookup"><span data-stu-id="50445-2232">Method displayValuesFromQueryRun</span></span>

    public List displayValuesFromQueryRun(QueryRun queryRun, str replacementFieldGroupName, [boolean isRootPrimaryKeyDataSource], [boolean trimSecuredValues], [boolean distinctBindingsOnly])

#### <a name="parameters"></a><span data-ttu-id="50445-2233">パラメーター</span><span class="sxs-lookup"><span data-stu-id="50445-2233">Parameters</span></span>

<span data-ttu-id="50445-2234">queryRun</span><span class="sxs-lookup"><span data-stu-id="50445-2234">queryRun</span></span>  

<!-- -->

<span data-ttu-id="50445-2235">replacementFieldGroupName</span><span class="sxs-lookup"><span data-stu-id="50445-2235">replacementFieldGroupName</span></span>  

<!-- -->

<span data-ttu-id="50445-2236">isRootPrimaryKeyDataSource</span><span class="sxs-lookup"><span data-stu-id="50445-2236">isRootPrimaryKeyDataSource</span></span>  

<!-- -->

<span data-ttu-id="50445-2237">trimSecuredValues</span><span class="sxs-lookup"><span data-stu-id="50445-2237">trimSecuredValues</span></span>  

<!-- -->

<span data-ttu-id="50445-2238">distinctBindingsOnly</span><span class="sxs-lookup"><span data-stu-id="50445-2238">distinctBindingsOnly</span></span>  

#### <a name="return-value"></a><span data-ttu-id="50445-2239">戻り値</span><span class="sxs-lookup"><span data-stu-id="50445-2239">Return Value</span></span>

### <a name="method-displayvaluesfromrecid"></a><span data-ttu-id="50445-2240">メソッド displayValuesFromRecID</span><span class="sxs-lookup"><span data-stu-id="50445-2240">Method displayValuesFromRecID</span></span>

    public List displayValuesFromRecID(Int64 recIDValue, str replacementFieldGroupName, [boolean trimSecuredValues], [boolean distinctBindingsOnly])

#### <a name="parameters"></a><span data-ttu-id="50445-2241">パラメーター</span><span class="sxs-lookup"><span data-stu-id="50445-2241">Parameters</span></span>

<span data-ttu-id="50445-2242">recIDValue</span><span class="sxs-lookup"><span data-stu-id="50445-2242">recIDValue</span></span>  

<!-- -->

<span data-ttu-id="50445-2243">replacementFieldGroupName</span><span class="sxs-lookup"><span data-stu-id="50445-2243">replacementFieldGroupName</span></span>  

<!-- -->

<span data-ttu-id="50445-2244">trimSecuredValues</span><span class="sxs-lookup"><span data-stu-id="50445-2244">trimSecuredValues</span></span>  

<!-- -->

<span data-ttu-id="50445-2245">distinctBindingsOnly</span><span class="sxs-lookup"><span data-stu-id="50445-2245">distinctBindingsOnly</span></span>  

#### <a name="return-value"></a><span data-ttu-id="50445-2246">戻り値</span><span class="sxs-lookup"><span data-stu-id="50445-2246">Return Value</span></span>

### <a name="method-displayvaluesfromrootds"></a><span data-ttu-id="50445-2247">メソッド displayValuesFromRootDS</span><span class="sxs-lookup"><span data-stu-id="50445-2247">Method displayValuesFromRootDS</span></span>

    public List displayValuesFromRootDS(QueryBuildDataSource rootQueryBuildDataSource, boolean isPrimaryKeyDataSource, str replacementFieldGroupName, [boolean trimSecuredValues], [boolean distinctBindingsOnly])

#### <a name="parameters"></a><span data-ttu-id="50445-2248">パラメーター</span><span class="sxs-lookup"><span data-stu-id="50445-2248">Parameters</span></span>

<span data-ttu-id="50445-2249">rootQueryBuildDataSource</span><span class="sxs-lookup"><span data-stu-id="50445-2249">rootQueryBuildDataSource</span></span>  

<!-- -->

<span data-ttu-id="50445-2250">isPrimaryKeyDataSource</span><span class="sxs-lookup"><span data-stu-id="50445-2250">isPrimaryKeyDataSource</span></span>  

<!-- -->

<span data-ttu-id="50445-2251">replacementFieldGroupName</span><span class="sxs-lookup"><span data-stu-id="50445-2251">replacementFieldGroupName</span></span>  

<!-- -->

<span data-ttu-id="50445-2252">trimSecuredValues</span><span class="sxs-lookup"><span data-stu-id="50445-2252">trimSecuredValues</span></span>  

<!-- -->

<span data-ttu-id="50445-2253">distinctBindingsOnly</span><span class="sxs-lookup"><span data-stu-id="50445-2253">distinctBindingsOnly</span></span>  

#### <a name="return-value"></a><span data-ttu-id="50445-2254">戻り値</span><span class="sxs-lookup"><span data-stu-id="50445-2254">Return Value</span></span>

### <a name="method-displayvalue"></a><span data-ttu-id="50445-2255">メソッド displayValue</span><span class="sxs-lookup"><span data-stu-id="50445-2255">Method displayValue</span></span>

    public FilterValue displayValue(Common resolvedCursor, FieldBinding displayBinding, [boolean isRootPrimaryKeyDataSource])

#### <a name="parameters"></a><span data-ttu-id="50445-2256">パラメーター</span><span class="sxs-lookup"><span data-stu-id="50445-2256">Parameters</span></span>

<span data-ttu-id="50445-2257">resolvedCursor</span><span class="sxs-lookup"><span data-stu-id="50445-2257">resolvedCursor</span></span>  

<!-- -->

<span data-ttu-id="50445-2258">displayBinding</span><span class="sxs-lookup"><span data-stu-id="50445-2258">displayBinding</span></span>  

<!-- -->

<span data-ttu-id="50445-2259">isRootPrimaryKeyDataSource</span><span class="sxs-lookup"><span data-stu-id="50445-2259">isRootPrimaryKeyDataSource</span></span>  

#### <a name="return-value"></a><span data-ttu-id="50445-2260">戻り値</span><span class="sxs-lookup"><span data-stu-id="50445-2260">Return Value</span></span>

### <a name="method-extendeddatatype"></a><span data-ttu-id="50445-2261">メソッド extendedDataType</span><span class="sxs-lookup"><span data-stu-id="50445-2261">Method extendedDataType</span></span>

    public str extendedDataType()

#### <a name="return-value"></a><span data-ttu-id="50445-2262">戻り値</span><span class="sxs-lookup"><span data-stu-id="50445-2262">Return Value</span></span>

### <a name="method-generateresolvereferencequery"></a><span data-ttu-id="50445-2263">メソッド generateResolveReferenceQuery</span><span class="sxs-lookup"><span data-stu-id="50445-2263">Method generateResolveReferenceQuery</span></span>

    public Query generateResolveReferenceQuery(List requiredJoinsAsRelationPathList, List filterValuesAsFilterValueList)

#### <a name="parameters"></a><span data-ttu-id="50445-2264">パラメーター</span><span class="sxs-lookup"><span data-stu-id="50445-2264">Parameters</span></span>

<span data-ttu-id="50445-2265">requiredJoinsAsRelationPathList</span><span class="sxs-lookup"><span data-stu-id="50445-2265">requiredJoinsAsRelationPathList</span></span>  

<!-- -->

<span data-ttu-id="50445-2266">filterValuesAsFilterValueList</span><span class="sxs-lookup"><span data-stu-id="50445-2266">filterValuesAsFilterValueList</span></span>  

#### <a name="return-value"></a><span data-ttu-id="50445-2267">戻り値</span><span class="sxs-lookup"><span data-stu-id="50445-2267">Return Value</span></span>

### <a name="method-isresolvedreferenceambiguous"></a><span data-ttu-id="50445-2268">メソッド isResolvedReferenceAmbiguous</span><span class="sxs-lookup"><span data-stu-id="50445-2268">Method isResolvedReferenceAmbiguous</span></span>

    public boolean isResolvedReferenceAmbiguous(Query query)

#### <a name="parameters"></a><span data-ttu-id="50445-2269">パラメーター</span><span class="sxs-lookup"><span data-stu-id="50445-2269">Parameters</span></span>

<span data-ttu-id="50445-2270">クエリ</span><span class="sxs-lookup"><span data-stu-id="50445-2270">query</span></span>  

#### <a name="return-value"></a><span data-ttu-id="50445-2271">戻り値</span><span class="sxs-lookup"><span data-stu-id="50445-2271">Return Value</span></span>

### <a name="method-primarykeytablename"></a><span data-ttu-id="50445-2272">メソッド primaryKeyTableName</span><span class="sxs-lookup"><span data-stu-id="50445-2272">Method primaryKeyTableName</span></span>

    public str primaryKeyTableName()

#### <a name="return-value"></a><span data-ttu-id="50445-2273">戻り値</span><span class="sxs-lookup"><span data-stu-id="50445-2273">Return Value</span></span>

### <a name="method-querybuilddatasourcebindingsforquery"></a><span data-ttu-id="50445-2274">メソッド queryBuildDataSourceBindingsForQuery</span><span class="sxs-lookup"><span data-stu-id="50445-2274">Method queryBuildDataSourceBindingsForQuery</span></span>

    public Map queryBuildDataSourceBindingsForQuery(Query query, str replacementFieldGroupName, [boolean isRootPrimaryKeyDataSource])

#### <a name="parameters"></a><span data-ttu-id="50445-2275">パラメーター</span><span class="sxs-lookup"><span data-stu-id="50445-2275">Parameters</span></span>

<span data-ttu-id="50445-2276">クエリ</span><span class="sxs-lookup"><span data-stu-id="50445-2276">query</span></span>  

<!-- -->

<span data-ttu-id="50445-2277">replacementFieldGroupName</span><span class="sxs-lookup"><span data-stu-id="50445-2277">replacementFieldGroupName</span></span>  

<!-- -->

<span data-ttu-id="50445-2278">isRootPrimaryKeyDataSource</span><span class="sxs-lookup"><span data-stu-id="50445-2278">isRootPrimaryKeyDataSource</span></span>  

#### <a name="return-value"></a><span data-ttu-id="50445-2279">戻り値</span><span class="sxs-lookup"><span data-stu-id="50445-2279">Return Value</span></span>

### <a name="method-querybuilddatasourcebindingsforrootds"></a><span data-ttu-id="50445-2280">メソッド queryBuildDataSourceBindingsForRootDS</span><span class="sxs-lookup"><span data-stu-id="50445-2280">Method queryBuildDataSourceBindingsForRootDS</span></span>

    public Map queryBuildDataSourceBindingsForRootDS(QueryBuildDataSource rootQueryBuildDataSource, boolean isPrimaryKeyDataSource, str replacementFieldGroupName)

#### <a name="parameters"></a><span data-ttu-id="50445-2281">パラメーター</span><span class="sxs-lookup"><span data-stu-id="50445-2281">Parameters</span></span>

<span data-ttu-id="50445-2282">rootQueryBuildDataSource</span><span class="sxs-lookup"><span data-stu-id="50445-2282">rootQueryBuildDataSource</span></span>  

<!-- -->

<span data-ttu-id="50445-2283">isPrimaryKeyDataSource</span><span class="sxs-lookup"><span data-stu-id="50445-2283">isPrimaryKeyDataSource</span></span>  

<!-- -->

<span data-ttu-id="50445-2284">replacementFieldGroupName</span><span class="sxs-lookup"><span data-stu-id="50445-2284">replacementFieldGroupName</span></span>  

#### <a name="return-value"></a><span data-ttu-id="50445-2285">戻り値</span><span class="sxs-lookup"><span data-stu-id="50445-2285">Return Value</span></span>

### <a name="method-resolvereference"></a><span data-ttu-id="50445-2286">メソッド resolveReference</span><span class="sxs-lookup"><span data-stu-id="50445-2286">Method resolveReference</span></span>

    public Common resolveReference(Query query, [boolean ignoreAmbiguousReference])

#### <a name="parameters"></a><span data-ttu-id="50445-2287">パラメーター</span><span class="sxs-lookup"><span data-stu-id="50445-2287">Parameters</span></span>

<span data-ttu-id="50445-2288">クエリ</span><span class="sxs-lookup"><span data-stu-id="50445-2288">query</span></span>  

<!-- -->

<span data-ttu-id="50445-2289">ignoreAmbiguousReference</span><span class="sxs-lookup"><span data-stu-id="50445-2289">ignoreAmbiguousReference</span></span>  

#### <a name="return-value"></a><span data-ttu-id="50445-2290">戻り値</span><span class="sxs-lookup"><span data-stu-id="50445-2290">Return Value</span></span>

### <a name="method-surrogateforeignkeyfieldbinding"></a><span data-ttu-id="50445-2291">メソッド surrogateForeignKeyFieldBinding</span><span class="sxs-lookup"><span data-stu-id="50445-2291">Method surrogateForeignKeyFieldBinding</span></span>

    public FieldBinding surrogateForeignKeyFieldBinding()

#### <a name="return-value"></a><span data-ttu-id="50445-2292">戻り値</span><span class="sxs-lookup"><span data-stu-id="50445-2292">Return Value</span></span>

### <a name="method-construct"></a><span data-ttu-id="50445-2293">メソッド construct</span><span class="sxs-lookup"><span data-stu-id="50445-2293">Method construct</span></span>

    public static SurrogateFKReplacementHelper construct(FieldBinding surrogateForeignKeyBinding)

#### <a name="parameters"></a><span data-ttu-id="50445-2294">パラメーター</span><span class="sxs-lookup"><span data-stu-id="50445-2294">Parameters</span></span>

<span data-ttu-id="50445-2295">surrogateForeignKeyBinding</span><span class="sxs-lookup"><span data-stu-id="50445-2295">surrogateForeignKeyBinding</span></span>  

#### <a name="return-value"></a><span data-ttu-id="50445-2296">戻り値</span><span class="sxs-lookup"><span data-stu-id="50445-2296">Return Value</span></span>

### <a name="method-constructforedt"></a><span data-ttu-id="50445-2297">メソッド constructForEDT</span><span class="sxs-lookup"><span data-stu-id="50445-2297">Method constructForEDT</span></span>

    public static SurrogateFKReplacementHelper constructForEDT(str edtName)

#### <a name="parameters"></a><span data-ttu-id="50445-2298">パラメーター</span><span class="sxs-lookup"><span data-stu-id="50445-2298">Parameters</span></span>

<span data-ttu-id="50445-2299">edtName</span><span class="sxs-lookup"><span data-stu-id="50445-2299">edtName</span></span>  

#### <a name="return-value"></a><span data-ttu-id="50445-2300">戻り値</span><span class="sxs-lookup"><span data-stu-id="50445-2300">Return Value</span></span>

### <a name="method-constructforpktable"></a><span data-ttu-id="50445-2301">メソッド constructForPKTable</span><span class="sxs-lookup"><span data-stu-id="50445-2301">Method constructForPKTable</span></span>

    public static SurrogateFKReplacementHelper constructForPKTable(str pkTableName)

#### <a name="parameters"></a><span data-ttu-id="50445-2302">パラメーター</span><span class="sxs-lookup"><span data-stu-id="50445-2302">Parameters</span></span>

<span data-ttu-id="50445-2303">pkTableName</span><span class="sxs-lookup"><span data-stu-id="50445-2303">pkTableName</span></span>  

#### <a name="return-value"></a><span data-ttu-id="50445-2304">戻り値</span><span class="sxs-lookup"><span data-stu-id="50445-2304">Return Value</span></span>

### <a name="method-defaultprimarykeyquerydatasourcename"></a><span data-ttu-id="50445-2305">メソッド defaultPrimaryKeyQueryDataSourceName</span><span class="sxs-lookup"><span data-stu-id="50445-2305">Method defaultPrimaryKeyQueryDataSourceName</span></span>

    public static str defaultPrimaryKeyQueryDataSourceName()

#### <a name="return-value"></a><span data-ttu-id="50445-2306">戻り値</span><span class="sxs-lookup"><span data-stu-id="50445-2306">Return Value</span></span>

### <a name="method-deprecated_workflowcaption"></a><span data-ttu-id="50445-2307">メソッド DEPRECATED\_WorkflowCaption</span><span class="sxs-lookup"><span data-stu-id="50445-2307">Method DEPRECATED\_WorkflowCaption</span></span>

    public static str DEPRECATED_WorkflowCaption(str tableName, str fieldName, Int64 recIDValue)

#### <a name="parameters"></a><span data-ttu-id="50445-2308">パラメーター</span><span class="sxs-lookup"><span data-stu-id="50445-2308">Parameters</span></span>

<span data-ttu-id="50445-2309">tableName</span><span class="sxs-lookup"><span data-stu-id="50445-2309">tableName</span></span>  

<!-- -->

<span data-ttu-id="50445-2310">fieldName</span><span class="sxs-lookup"><span data-stu-id="50445-2310">fieldName</span></span>  

<!-- -->

<span data-ttu-id="50445-2311">recIDValue</span><span class="sxs-lookup"><span data-stu-id="50445-2311">recIDValue</span></span>  

#### <a name="return-value"></a><span data-ttu-id="50445-2312">戻り値</span><span class="sxs-lookup"><span data-stu-id="50445-2312">Return Value</span></span>

### <a name="method-implicitreplacementfieldgroupname"></a><span data-ttu-id="50445-2313">メソッド implicitReplacementFieldGroupName</span><span class="sxs-lookup"><span data-stu-id="50445-2313">Method implicitReplacementFieldGroupName</span></span>

    public static str implicitReplacementFieldGroupName()

#### <a name="return-value"></a><span data-ttu-id="50445-2314">戻り値</span><span class="sxs-lookup"><span data-stu-id="50445-2314">Return Value</span></span>

### <a name="method-new"></a><span data-ttu-id="50445-2315">メソッド new</span><span class="sxs-lookup"><span data-stu-id="50445-2315">Method new</span></span>

<span data-ttu-id="50445-2316">Object クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="50445-2316">Initializes a new instance of the Object class.</span></span>

    private void new(FieldBinding surrogateForeignKeyBinding)

#### <a name="parameters"></a><span data-ttu-id="50445-2317">パラメーター</span><span class="sxs-lookup"><span data-stu-id="50445-2317">Parameters</span></span>

<span data-ttu-id="50445-2318">surrogateForeignKeyBinding</span><span class="sxs-lookup"><span data-stu-id="50445-2318">surrogateForeignKeyBinding</span></span>  

## <a name="class-sysglobalobjectcache"></a><span data-ttu-id="50445-2319">クラス SysGlobalObjectCache</span><span class="sxs-lookup"><span data-stu-id="50445-2319">Class SysGlobalObjectCache</span></span>
    class SysGlobalObjectCache extends Object

### <a name="remarks"></a><span data-ttu-id="50445-2320">備考</span><span class="sxs-lookup"><span data-stu-id="50445-2320">Remarks</span></span>

### <a name="examples"></a><span data-ttu-id="50445-2321">例</span><span class="sxs-lookup"><span data-stu-id="50445-2321">Examples</span></span>

### <a name="methods"></a><span data-ttu-id="50445-2322">メソッド</span><span class="sxs-lookup"><span data-stu-id="50445-2322">Methods</span></span>

| <span data-ttu-id="50445-2323">方法</span><span class="sxs-lookup"><span data-stu-id="50445-2323">Method</span></span>                                                                           | <span data-ttu-id="50445-2324">説明</span><span class="sxs-lookup"><span data-stu-id="50445-2324">Description</span></span>                                                   |
|----------------------------------------------------------------------------------|---------------------------------------------------------------|
| <span data-ttu-id="50445-2325">public container find(GlobalObjectCacheScope scope, container key)</span><span class="sxs-lookup"><span data-stu-id="50445-2325">public container find(GlobalObjectCacheScope scope, container key)</span></span>               |                                                               |
| <span data-ttu-id="50445-2326">public void finalize()</span><span class="sxs-lookup"><span data-stu-id="50445-2326">public void finalize()</span></span>                                                           |                                                               |
| <span data-ttu-id="50445-2327">public void remove(GlobalObjectCacheScope scope, container key)</span><span class="sxs-lookup"><span data-stu-id="50445-2327">public void remove(GlobalObjectCacheScope scope, container key)</span></span>                  |                                                               |
| <span data-ttu-id="50445-2328">public void print(GlobalObjectCacheScope scope)</span><span class="sxs-lookup"><span data-stu-id="50445-2328">public void print(GlobalObjectCacheScope scope)</span></span>                                  |                                                               |
| <span data-ttu-id="50445-2329">public void clear(GlobalObjectCacheScope scope)</span><span class="sxs-lookup"><span data-stu-id="50445-2329">public void clear(GlobalObjectCacheScope scope)</span></span>                                  |                                                               |
| <span data-ttu-id="50445-2330">::public static void clearAllCaches()</span><span class="sxs-lookup"><span data-stu-id="50445-2330">::public static void clearAllCaches()</span></span>                                            |                                                               |
| <span data-ttu-id="50445-2331">public void new()</span><span class="sxs-lookup"><span data-stu-id="50445-2331">public void new()</span></span>                                                                | <span data-ttu-id="50445-2332">SysGlobalObjectCache クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="50445-2332">Initializes a new instance of the SysGlobalObjectCache class.</span></span> |
| <span data-ttu-id="50445-2333">public void insert(GlobalObjectCacheScope scope, container key, container value)</span><span class="sxs-lookup"><span data-stu-id="50445-2333">public void insert(GlobalObjectCacheScope scope, container key, container value)</span></span> |                                                               |

### <a name="method-find"></a><span data-ttu-id="50445-2334">メソッド find</span><span class="sxs-lookup"><span data-stu-id="50445-2334">Method find</span></span>

    public container find(GlobalObjectCacheScope scope, container key)

#### <a name="parameters"></a><span data-ttu-id="50445-2335">パラメーター</span><span class="sxs-lookup"><span data-stu-id="50445-2335">Parameters</span></span>

<span data-ttu-id="50445-2336">scope</span><span class="sxs-lookup"><span data-stu-id="50445-2336">scope</span></span>  

<!-- -->

<span data-ttu-id="50445-2337">キー</span><span class="sxs-lookup"><span data-stu-id="50445-2337">key</span></span>  

#### <a name="return-value"></a><span data-ttu-id="50445-2338">戻り値</span><span class="sxs-lookup"><span data-stu-id="50445-2338">Return Value</span></span>

### <a name="method-finalize"></a><span data-ttu-id="50445-2339">メソッド finalize</span><span class="sxs-lookup"><span data-stu-id="50445-2339">Method finalize</span></span>

    public void finalize()

### <a name="method-remove"></a><span data-ttu-id="50445-2340">メソッド remove</span><span class="sxs-lookup"><span data-stu-id="50445-2340">Method remove</span></span>

    public void remove(GlobalObjectCacheScope scope, container key)

#### <a name="parameters"></a><span data-ttu-id="50445-2341">パラメーター</span><span class="sxs-lookup"><span data-stu-id="50445-2341">Parameters</span></span>

<span data-ttu-id="50445-2342">scope</span><span class="sxs-lookup"><span data-stu-id="50445-2342">scope</span></span>  

<!-- -->

<span data-ttu-id="50445-2343">キー</span><span class="sxs-lookup"><span data-stu-id="50445-2343">key</span></span>  

### <a name="method-print"></a><span data-ttu-id="50445-2344">メソッド print</span><span class="sxs-lookup"><span data-stu-id="50445-2344">Method print</span></span>

    public void print(GlobalObjectCacheScope scope)

#### <a name="parameters"></a><span data-ttu-id="50445-2345">パラメーター</span><span class="sxs-lookup"><span data-stu-id="50445-2345">Parameters</span></span>

<span data-ttu-id="50445-2346">scope</span><span class="sxs-lookup"><span data-stu-id="50445-2346">scope</span></span>  

### <a name="method-clear"></a><span data-ttu-id="50445-2347">メソッド clear</span><span class="sxs-lookup"><span data-stu-id="50445-2347">Method clear</span></span>

    public void clear(GlobalObjectCacheScope scope)

#### <a name="parameters"></a><span data-ttu-id="50445-2348">パラメーター</span><span class="sxs-lookup"><span data-stu-id="50445-2348">Parameters</span></span>

<span data-ttu-id="50445-2349">scope</span><span class="sxs-lookup"><span data-stu-id="50445-2349">scope</span></span>  

### <a name="method-clearallcaches"></a><span data-ttu-id="50445-2350">メソッド clearAllCaches</span><span class="sxs-lookup"><span data-stu-id="50445-2350">Method clearAllCaches</span></span>

    public static void clearAllCaches()

### <a name="method-new"></a><span data-ttu-id="50445-2351">メソッド new</span><span class="sxs-lookup"><span data-stu-id="50445-2351">Method new</span></span>

<span data-ttu-id="50445-2352">SysGlobalObjectCache クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="50445-2352">Initializes a new instance of the SysGlobalObjectCache class.</span></span>

    public void new()

### <a name="method-insert"></a><span data-ttu-id="50445-2353">メソッド insert</span><span class="sxs-lookup"><span data-stu-id="50445-2353">Method insert</span></span>

    public void insert(GlobalObjectCacheScope scope, container key, container value)

#### <a name="parameters"></a><span data-ttu-id="50445-2354">パラメーター</span><span class="sxs-lookup"><span data-stu-id="50445-2354">Parameters</span></span>

<span data-ttu-id="50445-2355">scope</span><span class="sxs-lookup"><span data-stu-id="50445-2355">scope</span></span>  

<!-- -->

<span data-ttu-id="50445-2356">キー</span><span class="sxs-lookup"><span data-stu-id="50445-2356">key</span></span>  

<!-- -->

<span data-ttu-id="50445-2357">値</span><span class="sxs-lookup"><span data-stu-id="50445-2357">value</span></span>  

## <a name="class-systemmonitor"></a><span data-ttu-id="50445-2358">クラス SystemMonitor</span><span class="sxs-lookup"><span data-stu-id="50445-2358">Class SystemMonitor</span></span>
    class SystemMonitor extends Object

### <a name="remarks"></a><span data-ttu-id="50445-2359">備考</span><span class="sxs-lookup"><span data-stu-id="50445-2359">Remarks</span></span>

### <a name="examples"></a><span data-ttu-id="50445-2360">例</span><span class="sxs-lookup"><span data-stu-id="50445-2360">Examples</span></span>

### <a name="methods"></a><span data-ttu-id="50445-2361">方法</span><span class="sxs-lookup"><span data-stu-id="50445-2361">Methods</span></span>

| <span data-ttu-id="50445-2362">方法</span><span class="sxs-lookup"><span data-stu-id="50445-2362">Method</span></span>                                                                | <span data-ttu-id="50445-2363">説明</span><span class="sxs-lookup"><span data-stu-id="50445-2363">Description</span></span>                                            |
|-----------------------------------------------------------------------|--------------------------------------------------------|
| <span data-ttu-id="50445-2364">::public static container allClientCounters()</span><span class="sxs-lookup"><span data-stu-id="50445-2364">::public static container allClientCounters()</span></span>                         |                                                        |
| <span data-ttu-id="50445-2365">::public static container allServerCounters()</span><span class="sxs-lookup"><span data-stu-id="50445-2365">::public static container allServerCounters()</span></span>                         |                                                        |
| <span data-ttu-id="50445-2366">::public static int getClientCounter(SystemMonitorCounter counter)</span><span class="sxs-lookup"><span data-stu-id="50445-2366">::public static int getClientCounter(SystemMonitorCounter counter)</span></span>    |                                                        |
| <span data-ttu-id="50445-2367">::public static container getClientInternals()</span><span class="sxs-lookup"><span data-stu-id="50445-2367">::public static container getClientInternals()</span></span>                        |                                                        |
| <span data-ttu-id="50445-2368">::public static int getCounter(SystemMonitorCounter counter)</span><span class="sxs-lookup"><span data-stu-id="50445-2368">::public static int getCounter(SystemMonitorCounter counter)</span></span>          |                                                        |
| <span data-ttu-id="50445-2369">::public static int getServerCounter(SystemMonitorCounter counter)</span><span class="sxs-lookup"><span data-stu-id="50445-2369">::public static int getServerCounter(SystemMonitorCounter counter)</span></span>    |                                                        |
| <span data-ttu-id="50445-2370">::public static container getServerInternals()</span><span class="sxs-lookup"><span data-stu-id="50445-2370">::public static container getServerInternals()</span></span>                        |                                                        |
| <span data-ttu-id="50445-2371">::public static boolean isRunning()</span><span class="sxs-lookup"><span data-stu-id="50445-2371">::public static boolean isRunning()</span></span>                                   |                                                        |
| <span data-ttu-id="50445-2372">::public static boolean isServerCounter(SystemMonitorCounter counter)</span><span class="sxs-lookup"><span data-stu-id="50445-2372">::public static boolean isServerCounter(SystemMonitorCounter counter)</span></span> |                                                        |
| <span data-ttu-id="50445-2373">::public static container sqlDump()</span><span class="sxs-lookup"><span data-stu-id="50445-2373">::public static container sqlDump()</span></span>                                   |                                                        |
| <span data-ttu-id="50445-2374">::public static void systemDump(boolean includeSQL)</span><span class="sxs-lookup"><span data-stu-id="50445-2374">::public static void systemDump(boolean includeSQL)</span></span>                   |                                                        |
| <span data-ttu-id="50445-2375">::public static void start()</span><span class="sxs-lookup"><span data-stu-id="50445-2375">::public static void start()</span></span>                                          |                                                        |
| <span data-ttu-id="50445-2376">::public static void resetServer()</span><span class="sxs-lookup"><span data-stu-id="50445-2376">::public static void resetServer()</span></span>                                    |                                                        |
| <span data-ttu-id="50445-2377">::public static void stop()</span><span class="sxs-lookup"><span data-stu-id="50445-2377">::public static void stop()</span></span>                                           |                                                        |
| <span data-ttu-id="50445-2378">public void new()</span><span class="sxs-lookup"><span data-stu-id="50445-2378">public void new()</span></span>                                                     | <span data-ttu-id="50445-2379">SystemMonitor クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="50445-2379">Initializes a new instance of the SystemMonitor class.</span></span> |
| <span data-ttu-id="50445-2380">public void finalize()</span><span class="sxs-lookup"><span data-stu-id="50445-2380">public void finalize()</span></span>                                                |                                                        |
| <span data-ttu-id="50445-2381">::public static void reset()</span><span class="sxs-lookup"><span data-stu-id="50445-2381">::public static void reset()</span></span>                                          |                                                        |
| <span data-ttu-id="50445-2382">::public static void resetClient()</span><span class="sxs-lookup"><span data-stu-id="50445-2382">::public static void resetClient()</span></span>                                    |                                                        |

### <a name="method-allclientcounters"></a><span data-ttu-id="50445-2383">メソッド allClientCounters</span><span class="sxs-lookup"><span data-stu-id="50445-2383">Method allClientCounters</span></span>

    public static container allClientCounters()

#### <a name="return-value"></a><span data-ttu-id="50445-2384">戻り値</span><span class="sxs-lookup"><span data-stu-id="50445-2384">Return Value</span></span>

### <a name="method-allservercounters"></a><span data-ttu-id="50445-2385">メソッド allServerCounters</span><span class="sxs-lookup"><span data-stu-id="50445-2385">Method allServerCounters</span></span>

    public static container allServerCounters()

#### <a name="return-value"></a><span data-ttu-id="50445-2386">戻り値</span><span class="sxs-lookup"><span data-stu-id="50445-2386">Return Value</span></span>

### <a name="method-getclientcounter"></a><span data-ttu-id="50445-2387">メソッド getClientCounter</span><span class="sxs-lookup"><span data-stu-id="50445-2387">Method getClientCounter</span></span>

    public static int getClientCounter(SystemMonitorCounter counter)

#### <a name="parameters"></a><span data-ttu-id="50445-2388">パラメーター</span><span class="sxs-lookup"><span data-stu-id="50445-2388">Parameters</span></span>

<span data-ttu-id="50445-2389">counter</span><span class="sxs-lookup"><span data-stu-id="50445-2389">counter</span></span>  

#### <a name="return-value"></a><span data-ttu-id="50445-2390">戻り値</span><span class="sxs-lookup"><span data-stu-id="50445-2390">Return Value</span></span>

### <a name="method-getclientinternals"></a><span data-ttu-id="50445-2391">メソッド getClientInternals</span><span class="sxs-lookup"><span data-stu-id="50445-2391">Method getClientInternals</span></span>

    public static container getClientInternals()

#### <a name="return-value"></a><span data-ttu-id="50445-2392">戻り値</span><span class="sxs-lookup"><span data-stu-id="50445-2392">Return Value</span></span>

### <a name="method-getcounter"></a><span data-ttu-id="50445-2393">メソッド getCounter</span><span class="sxs-lookup"><span data-stu-id="50445-2393">Method getCounter</span></span>

    public static int getCounter(SystemMonitorCounter counter)

#### <a name="parameters"></a><span data-ttu-id="50445-2394">パラメーター</span><span class="sxs-lookup"><span data-stu-id="50445-2394">Parameters</span></span>

<span data-ttu-id="50445-2395">counter</span><span class="sxs-lookup"><span data-stu-id="50445-2395">counter</span></span>  

#### <a name="return-value"></a><span data-ttu-id="50445-2396">戻り値</span><span class="sxs-lookup"><span data-stu-id="50445-2396">Return Value</span></span>

### <a name="method-getservercounter"></a><span data-ttu-id="50445-2397">メソッド getServerCounter</span><span class="sxs-lookup"><span data-stu-id="50445-2397">Method getServerCounter</span></span>

    public static int getServerCounter(SystemMonitorCounter counter)

#### <a name="parameters"></a><span data-ttu-id="50445-2398">パラメーター</span><span class="sxs-lookup"><span data-stu-id="50445-2398">Parameters</span></span>

<span data-ttu-id="50445-2399">counter</span><span class="sxs-lookup"><span data-stu-id="50445-2399">counter</span></span>  

#### <a name="return-value"></a><span data-ttu-id="50445-2400">戻り値</span><span class="sxs-lookup"><span data-stu-id="50445-2400">Return Value</span></span>

### <a name="method-getserverinternals"></a><span data-ttu-id="50445-2401">メソッド getServerInternals</span><span class="sxs-lookup"><span data-stu-id="50445-2401">Method getServerInternals</span></span>

    public static container getServerInternals()

#### <a name="return-value"></a><span data-ttu-id="50445-2402">戻り値</span><span class="sxs-lookup"><span data-stu-id="50445-2402">Return Value</span></span>

### <a name="method-isrunning"></a><span data-ttu-id="50445-2403">メソッド isRunning</span><span class="sxs-lookup"><span data-stu-id="50445-2403">Method isRunning</span></span>

    public static boolean isRunning()

#### <a name="return-value"></a><span data-ttu-id="50445-2404">戻り値</span><span class="sxs-lookup"><span data-stu-id="50445-2404">Return Value</span></span>

### <a name="method-isservercounter"></a><span data-ttu-id="50445-2405">メソッド isServerCounter</span><span class="sxs-lookup"><span data-stu-id="50445-2405">Method isServerCounter</span></span>

    public static boolean isServerCounter(SystemMonitorCounter counter)

#### <a name="parameters"></a><span data-ttu-id="50445-2406">パラメーター</span><span class="sxs-lookup"><span data-stu-id="50445-2406">Parameters</span></span>

<span data-ttu-id="50445-2407">counter</span><span class="sxs-lookup"><span data-stu-id="50445-2407">counter</span></span>  

#### <a name="return-value"></a><span data-ttu-id="50445-2408">戻り値</span><span class="sxs-lookup"><span data-stu-id="50445-2408">Return Value</span></span>

### <a name="method-sqldump"></a><span data-ttu-id="50445-2409">メソッド sqlDump</span><span class="sxs-lookup"><span data-stu-id="50445-2409">Method sqlDump</span></span>

    public static container sqlDump()

#### <a name="return-value"></a><span data-ttu-id="50445-2410">戻り値</span><span class="sxs-lookup"><span data-stu-id="50445-2410">Return Value</span></span>

### <a name="method-systemdump"></a><span data-ttu-id="50445-2411">メソッド systemDump</span><span class="sxs-lookup"><span data-stu-id="50445-2411">Method systemDump</span></span>

    public static void systemDump(boolean includeSQL)

#### <a name="parameters"></a><span data-ttu-id="50445-2412">パラメーター</span><span class="sxs-lookup"><span data-stu-id="50445-2412">Parameters</span></span>

<span data-ttu-id="50445-2413">includeSQL</span><span class="sxs-lookup"><span data-stu-id="50445-2413">includeSQL</span></span>  

### <a name="method-start"></a><span data-ttu-id="50445-2414">メソッド start</span><span class="sxs-lookup"><span data-stu-id="50445-2414">Method start</span></span>

    public static void start()

### <a name="method-resetserver"></a><span data-ttu-id="50445-2415">メソッド resetServer</span><span class="sxs-lookup"><span data-stu-id="50445-2415">Method resetServer</span></span>

    public static void resetServer()

### <a name="method-stop"></a><span data-ttu-id="50445-2416">メソッド stop</span><span class="sxs-lookup"><span data-stu-id="50445-2416">Method stop</span></span>

    public static void stop()

### <a name="method-new"></a><span data-ttu-id="50445-2417">メソッド new</span><span class="sxs-lookup"><span data-stu-id="50445-2417">Method new</span></span>

<span data-ttu-id="50445-2418">SystemMonitor クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="50445-2418">Initializes a new instance of the SystemMonitor class.</span></span>

    public void new()

### <a name="method-finalize"></a><span data-ttu-id="50445-2419">メソッド finalize</span><span class="sxs-lookup"><span data-stu-id="50445-2419">Method finalize</span></span>

    public void finalize()

### <a name="method-reset"></a><span data-ttu-id="50445-2420">メソッド reset</span><span class="sxs-lookup"><span data-stu-id="50445-2420">Method reset</span></span>

    public static void reset()

### <a name="method-resetclient"></a><span data-ttu-id="50445-2421">メソッド resetClient</span><span class="sxs-lookup"><span data-stu-id="50445-2421">Method resetClient</span></span>

    public static void resetClient()

## <a name="class-systemsequence"></a><span data-ttu-id="50445-2422">クラス systemSequence</span><span class="sxs-lookup"><span data-stu-id="50445-2422">Class systemSequence</span></span>
    class systemSequence extends Object

<span data-ttu-id="50445-2423">systemSequence クラスは、システム シーケンス ジェネレータを手動で制御し、すべての SQL テーブルに対して一意の RecIds を提供します。</span><span class="sxs-lookup"><span data-stu-id="50445-2423">The systemSequence class takes manual control of the system sequence generator and delivers unique RecIds for all SQL tables.</span></span>

### <a name="remarks"></a><span data-ttu-id="50445-2424">備考</span><span class="sxs-lookup"><span data-stu-id="50445-2424">Remarks</span></span>

<span data-ttu-id="50445-2425">SQL テーブルにレコードが挿入されると、各レコードが関連付けられている会社に関係なく、各レコードに一意の RecId が割り当てられます。</span><span class="sxs-lookup"><span data-stu-id="50445-2425">When records are inserted into SQL tables, a unique RecId is assigned to each record—regardless of the company each record is associated with.</span></span> <span data-ttu-id="50445-2426">このクラスを使用するときは十分に注意してください。データの整合性が失われる可能性があります。</span><span class="sxs-lookup"><span data-stu-id="50445-2426">Use extreme caution when you use this class—data integrity could be destroyed.</span></span> <span data-ttu-id="50445-2427">このクラスは、通常、データのインポートやエクスポート ルーチン、または非常に大きなジョブに使用されます。</span><span class="sxs-lookup"><span data-stu-id="50445-2427">This class is typically used for data import or export routines, or for very large jobs.</span></span> <span data-ttu-id="50445-2428">レコード ID は、int64 データ型の値です。</span><span class="sxs-lookup"><span data-stu-id="50445-2428">The record ID is an int64 data type value.</span></span> <span data-ttu-id="50445-2429">レコード ID が割り当てられる範囲は、5637144576 から 2 ^ 63 (9223372036854775808) までです。</span><span class="sxs-lookup"><span data-stu-id="50445-2429">The range in which record IDs are allocated is from 5637144576 to 2^63 (9223372036854775808).</span></span> <span data-ttu-id="50445-2430">大きい未使用の RecId 範囲が作成された場合、途中で RecId がなくなることがあります。</span><span class="sxs-lookup"><span data-stu-id="50445-2430">RecIds can be used up prematurely if large, unused ranges of RecIds are created.</span></span> <span data-ttu-id="50445-2431">使用されている Recid 範囲の間にある未使用の RecId 範囲を再利用するのは、非常に複雑なプロセスです。</span><span class="sxs-lookup"><span data-stu-id="50445-2431">Reclaiming unused ranges of RecIds that lie between used ranges of RecIds is a very complicated process.</span></span>

### <a name="examples"></a><span data-ttu-id="50445-2432">例</span><span class="sxs-lookup"><span data-stu-id="50445-2432">Examples</span></span>

<span data-ttu-id="50445-2433">次の例では、CustTable テーブルの int64max 値を予約しています。</span><span class="sxs-lookup"><span data-stu-id="50445-2433">The following example reserves the int64max value for the CustTable table.</span></span>

    static public void Main(Args _args) 
    { 
        systemSequence seq; 
        seq = new SystemSequence(); 
        if (seq) 
        { 
            // Allocate 20 recordIds for CustTable table. 
            seq.reserveValues(20, tablenum(CustTable)); 
            // Suspend automatic recId allocation. 
            Seq.suspendRecIds(tablenum(CustTable)); 
            // Manually generate recIds in the range allocated. 
            // Remove the recId suspension. 
            Seq.removeRecIdSuspension(); 
          } 
    }

### <a name="methods"></a><span data-ttu-id="50445-2434">メソッド</span><span class="sxs-lookup"><span data-stu-id="50445-2434">Methods</span></span>

| <span data-ttu-id="50445-2435">方法</span><span class="sxs-lookup"><span data-stu-id="50445-2435">Method</span></span>                                                             | <span data-ttu-id="50445-2436">説明</span><span class="sxs-lookup"><span data-stu-id="50445-2436">Description</span></span>                                                                                                                     |
|--------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="50445-2437">public Int64 flushValues(TableId tableId)</span><span class="sxs-lookup"><span data-stu-id="50445-2437">public Int64 flushValues(TableId tableId)</span></span>                          | <span data-ttu-id="50445-2438">指定されたテーブルのシステム シーケンス キャッシュから予約された recIds をフラッシュします。</span><span class="sxs-lookup"><span data-stu-id="50445-2438">Flushes the reserved recIds from the System Sequence cache for a given table</span></span>                                                    |
| <span data-ttu-id="50445-2439">public Int64 reserveTransids(Int64 nReserved, \[TableId tableId\])</span><span class="sxs-lookup"><span data-stu-id="50445-2439">public Int64 reserveTransids(Int64 nReserved, \[TableId tableId\])</span></span> |                                                                                                                                 |
| <span data-ttu-id="50445-2440">public Int64 reserveValues(Int64 nReserved, TableId tableId)</span><span class="sxs-lookup"><span data-stu-id="50445-2440">public Int64 reserveValues(Int64 nReserved, TableId tableId)</span></span>       | <span data-ttu-id="50445-2441">recIds の自動割り当てが中断されている場合に、新しいレコードに割り当てることのできる recIds の範囲を事前割り当てします。</span><span class="sxs-lookup"><span data-stu-id="50445-2441">Preallocates a range of recIds that can be allocated to new records when the automatic assignment of recIds has been suspended.</span></span> |
| <span data-ttu-id="50445-2442">public void suspendTransIds(TableId tableId)</span><span class="sxs-lookup"><span data-stu-id="50445-2442">public void suspendTransIds(TableId tableId)</span></span>                       |                                                                                                                                 |
| <span data-ttu-id="50445-2443">public void suspendRecIds(TableId tableId)</span><span class="sxs-lookup"><span data-stu-id="50445-2443">public void suspendRecIds(TableId tableId)</span></span>                         |                                                                                                                                 |
| <span data-ttu-id="50445-2444">public void removeRecIdSuspension(\[TableId tableId\])</span><span class="sxs-lookup"><span data-stu-id="50445-2444">public void removeRecIdSuspension(\[TableId tableId\])</span></span>             |                                                                                                                                 |
| <span data-ttu-id="50445-2445">public void new()</span><span class="sxs-lookup"><span data-stu-id="50445-2445">public void new()</span></span>                                                  | <span data-ttu-id="50445-2446">systemSequence クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="50445-2446">Initializes a new instance of the systemSequence class.</span></span>                                                                         |
| <span data-ttu-id="50445-2447">public void removeTransIdSuspension(\[TableId tableId\])</span><span class="sxs-lookup"><span data-stu-id="50445-2447">public void removeTransIdSuspension(\[TableId tableId\])</span></span>           |                                                                                                                                 |

### <a name="method-flushvalues"></a><span data-ttu-id="50445-2448">メソッド flushValues</span><span class="sxs-lookup"><span data-stu-id="50445-2448">Method flushValues</span></span>

<span data-ttu-id="50445-2449">指定されたテーブルのシステム シーケンス キャッシュから予約された recIds をフラッシュします。</span><span class="sxs-lookup"><span data-stu-id="50445-2449">Flushes the reserved recIds from the System Sequence cache for a given table</span></span>

    public Int64 flushValues(TableId tableId)

#### <a name="parameters"></a><span data-ttu-id="50445-2450">パラメーター</span><span class="sxs-lookup"><span data-stu-id="50445-2450">Parameters</span></span>

<span data-ttu-id="50445-2451">tableId</span><span class="sxs-lookup"><span data-stu-id="50445-2451">tableId</span></span>  

#### <a name="return-value"></a><span data-ttu-id="50445-2452">戻り値</span><span class="sxs-lookup"><span data-stu-id="50445-2452">Return Value</span></span>

<span data-ttu-id="50445-2453">キャッシュからフラッシュされた recIds の数。</span><span class="sxs-lookup"><span data-stu-id="50445-2453">The number of recIds flushed from the cache.</span></span>

#### <a name="remarks"></a><span data-ttu-id="50445-2454">備考</span><span class="sxs-lookup"><span data-stu-id="50445-2454">Remarks</span></span>

<span data-ttu-id="50445-2455">テーブルへのその後挿入によりテーブルの recId が予約され、システム シーケンス キャッシュにはテーブルの recId の予約済み範囲が入力されます。</span><span class="sxs-lookup"><span data-stu-id="50445-2455">Subsequent inserts on the table reserve the recIds for the table and System Sequence cache is populated with the reserved range of recIds for the table.</span></span>

### <a name="method-reservetransids"></a><span data-ttu-id="50445-2456">メソッド reserveTransids</span><span class="sxs-lookup"><span data-stu-id="50445-2456">Method reserveTransids</span></span>

    public Int64 reserveTransids(Int64 nReserved, [TableId tableId])

#### <a name="parameters"></a><span data-ttu-id="50445-2457">パラメーター</span><span class="sxs-lookup"><span data-stu-id="50445-2457">Parameters</span></span>

<span data-ttu-id="50445-2458">nReserved</span><span class="sxs-lookup"><span data-stu-id="50445-2458">nReserved</span></span>  

<!-- -->

<span data-ttu-id="50445-2459">tableId</span><span class="sxs-lookup"><span data-stu-id="50445-2459">tableId</span></span>  

#### <a name="return-value"></a><span data-ttu-id="50445-2460">戻り値</span><span class="sxs-lookup"><span data-stu-id="50445-2460">Return Value</span></span>

### <a name="method-reservevalues"></a><span data-ttu-id="50445-2461">メソッド reserveValues</span><span class="sxs-lookup"><span data-stu-id="50445-2461">Method reserveValues</span></span>

<span data-ttu-id="50445-2462">recIds の自動割り当てが中断されている場合に、新しいレコードに割り当てることのできる recIds の範囲を事前割り当てします。</span><span class="sxs-lookup"><span data-stu-id="50445-2462">Preallocates a range of recIds that can be allocated to new records when the automatic assignment of recIds has been suspended.</span></span>

    public Int64 reserveValues(Int64 nReserved, TableId tableId)

#### <a name="parameters"></a><span data-ttu-id="50445-2463">パラメーター</span><span class="sxs-lookup"><span data-stu-id="50445-2463">Parameters</span></span>

<span data-ttu-id="50445-2464">nReserved</span><span class="sxs-lookup"><span data-stu-id="50445-2464">nReserved</span></span>  

<!-- -->

<span data-ttu-id="50445-2465">tableId</span><span class="sxs-lookup"><span data-stu-id="50445-2465">tableId</span></span>  

#### <a name="return-value"></a><span data-ttu-id="50445-2466">戻り値</span><span class="sxs-lookup"><span data-stu-id="50445-2466">Return Value</span></span>

<span data-ttu-id="50445-2467">最初に使用可能な予約済み recId。</span><span class="sxs-lookup"><span data-stu-id="50445-2467">The first usable reserved recId.</span></span>

#### <a name="remarks"></a><span data-ttu-id="50445-2468">備考</span><span class="sxs-lookup"><span data-stu-id="50445-2468">Remarks</span></span>

<span data-ttu-id="50445-2469">予約した recIds の範囲は、すぐに予約されています。</span><span class="sxs-lookup"><span data-stu-id="50445-2469">The range of recIds that you reserved are reserved immediately.</span></span>

### <a name="method-suspendtransids"></a><span data-ttu-id="50445-2470">メソッド suspendTransIds</span><span class="sxs-lookup"><span data-stu-id="50445-2470">Method suspendTransIds</span></span>

    public void suspendTransIds(TableId tableId)

#### <a name="parameters"></a><span data-ttu-id="50445-2471">パラメーター</span><span class="sxs-lookup"><span data-stu-id="50445-2471">Parameters</span></span>

<span data-ttu-id="50445-2472">tableId</span><span class="sxs-lookup"><span data-stu-id="50445-2472">tableId</span></span>  

### <a name="method-suspendrecids"></a><span data-ttu-id="50445-2473">メソッド suspendRecIds</span><span class="sxs-lookup"><span data-stu-id="50445-2473">Method suspendRecIds</span></span>

    public void suspendRecIds(TableId tableId)

#### <a name="parameters"></a><span data-ttu-id="50445-2474">パラメーター</span><span class="sxs-lookup"><span data-stu-id="50445-2474">Parameters</span></span>

<span data-ttu-id="50445-2475">tableId</span><span class="sxs-lookup"><span data-stu-id="50445-2475">tableId</span></span>  

### <a name="method-removerecidsuspension"></a><span data-ttu-id="50445-2476">メソッド removeRecIdSuspension</span><span class="sxs-lookup"><span data-stu-id="50445-2476">Method removeRecIdSuspension</span></span>

    public void removeRecIdSuspension([TableId tableId])

#### <a name="parameters"></a><span data-ttu-id="50445-2477">パラメーター</span><span class="sxs-lookup"><span data-stu-id="50445-2477">Parameters</span></span>

<span data-ttu-id="50445-2478">tableId</span><span class="sxs-lookup"><span data-stu-id="50445-2478">tableId</span></span>  

### <a name="method-new"></a><span data-ttu-id="50445-2479">メソッド new</span><span class="sxs-lookup"><span data-stu-id="50445-2479">Method new</span></span>

<span data-ttu-id="50445-2480">systemSequence クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="50445-2480">Initializes a new instance of the systemSequence class.</span></span>

    public void new()

### <a name="method-removetransidsuspension"></a><span data-ttu-id="50445-2481">メソッド removeTransIdSuspension</span><span class="sxs-lookup"><span data-stu-id="50445-2481">Method removeTransIdSuspension</span></span>

    public void removeTransIdSuspension([TableId tableId])

#### <a name="parameters"></a><span data-ttu-id="50445-2482">パラメーター</span><span class="sxs-lookup"><span data-stu-id="50445-2482">Parameters</span></span>

<span data-ttu-id="50445-2483">tableId</span><span class="sxs-lookup"><span data-stu-id="50445-2483">tableId</span></span>  





