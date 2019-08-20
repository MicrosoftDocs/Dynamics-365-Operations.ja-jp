---
title: E クラス
description: 文字 E で始まるシステム API クラス。
author: RobinARH
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.search.scope: Operations
ms.custom: 68633
ms.assetid: c7fea535-c44d-4e78-96b2-77e180076ac9
ms.search.region: Global
ms.author: rhaertle
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 925d0b8a2c6c44b404770ce773b4b80c68b8f768
ms.sourcegitcommit: 27a98a7a0f1d2623f5236a88066f483def30889c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 08/01/2019
ms.locfileid: "1833708"
---
# <a name="e-classes"></a><span data-ttu-id="c29b0-103">E クラス</span><span class="sxs-lookup"><span data-stu-id="c29b0-103">E classes</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c29b0-104">文字 E で始まるシステム API クラス。</span><span class="sxs-lookup"><span data-stu-id="c29b0-104">System API classes that start with the letter E.</span></span>

<a name="class-editor"></a><span data-ttu-id="c29b0-105">クラス エディター</span><span class="sxs-lookup"><span data-stu-id="c29b0-105">Class Editor</span></span>
------------

    class Editor extends Object

### <a name="remarks"></a><span data-ttu-id="c29b0-106">備考</span><span class="sxs-lookup"><span data-stu-id="c29b0-106">Remarks</span></span>

### <a name="examples"></a><span data-ttu-id="c29b0-107">例</span><span class="sxs-lookup"><span data-stu-id="c29b0-107">Examples</span></span>

### <a name="methods"></a><span data-ttu-id="c29b0-108">メソッド</span><span class="sxs-lookup"><span data-stu-id="c29b0-108">Methods</span></span>

| <span data-ttu-id="c29b0-109">方法</span><span class="sxs-lookup"><span data-stu-id="c29b0-109">Method</span></span>                                                                          | <span data-ttu-id="c29b0-110">説明</span><span class="sxs-lookup"><span data-stu-id="c29b0-110">Description</span></span>                                     |
|---------------------------------------------------------------------------------|-------------------------------------------------|
| <span data-ttu-id="c29b0-111">public int columnNo()</span><span class="sxs-lookup"><span data-stu-id="c29b0-111">public int columnNo()</span></span>                                                           |                                                 |
| <span data-ttu-id="c29b0-112">public str currentLine()</span><span class="sxs-lookup"><span data-stu-id="c29b0-112">public str currentLine()</span></span>                                                        |                                                 |
| <span data-ttu-id="c29b0-113">public int currentLineNo()</span><span class="sxs-lookup"><span data-stu-id="c29b0-113">public int currentLineNo()</span></span>                                                      |                                                 |
| <span data-ttu-id="c29b0-114">public str getLine()</span><span class="sxs-lookup"><span data-stu-id="c29b0-114">public str getLine()</span></span>                                                            |                                                 |
| <span data-ttu-id="c29b0-115">public int gotoCol(int ColumnNo)</span><span class="sxs-lookup"><span data-stu-id="c29b0-115">public int gotoCol(int ColumnNo)</span></span>                                                |                                                 |
| <span data-ttu-id="c29b0-116">public int lineNo()</span><span class="sxs-lookup"><span data-stu-id="c29b0-116">public int lineNo()</span></span>                                                             |                                                 |
| <span data-ttu-id="c29b0-117">public MarkMode markMode()</span><span class="sxs-lookup"><span data-stu-id="c29b0-117">public MarkMode markMode()</span></span>                                                      |                                                 |
| <span data-ttu-id="c29b0-118">public boolean matchCase(\[boolean UseMatchCase\])</span><span class="sxs-lookup"><span data-stu-id="c29b0-118">public boolean matchCase(\[boolean UseMatchCase\])</span></span>                              |                                                 |
| <span data-ttu-id="c29b0-119">public boolean moreLines()</span><span class="sxs-lookup"><span data-stu-id="c29b0-119">public boolean moreLines()</span></span>                                                      |                                                 |
| <span data-ttu-id="c29b0-120">public boolean moreSelectedLines()</span><span class="sxs-lookup"><span data-stu-id="c29b0-120">public boolean moreSelectedLines()</span></span>                                              |                                                 |
| <span data-ttu-id="c29b0-121">public str path()</span><span class="sxs-lookup"><span data-stu-id="c29b0-121">public str path()</span></span>                                                               |                                                 |
| <span data-ttu-id="c29b0-122">public boolean regexp(\[boolean UseRegExp\])</span><span class="sxs-lookup"><span data-stu-id="c29b0-122">public boolean regexp(\[boolean UseRegExp\])</span></span>                                    |                                                 |
| <span data-ttu-id="c29b0-123">public boolean replace(str SearchString, str ReplaceString, boolean ReplaceAll)</span><span class="sxs-lookup"><span data-stu-id="c29b0-123">public boolean replace(str SearchString, str ReplaceString, boolean ReplaceAll)</span></span> |                                                 |
| <span data-ttu-id="c29b0-124">public boolean search(str SearchString)</span><span class="sxs-lookup"><span data-stu-id="c29b0-124">public boolean search(str SearchString)</span></span>                                         |                                                 |
| <span data-ttu-id="c29b0-125">public str searchString()</span><span class="sxs-lookup"><span data-stu-id="c29b0-125">public str searchString()</span></span>                                                       |                                                 |
| <span data-ttu-id="c29b0-126">public int selectionEndCol()</span><span class="sxs-lookup"><span data-stu-id="c29b0-126">public int selectionEndCol()</span></span>                                                    |                                                 |
| <span data-ttu-id="c29b0-127">public int selectionEndLine()</span><span class="sxs-lookup"><span data-stu-id="c29b0-127">public int selectionEndLine()</span></span>                                                   |                                                 |
| <span data-ttu-id="c29b0-128">public int selectionStartCol()</span><span class="sxs-lookup"><span data-stu-id="c29b0-128">public int selectionStartCol()</span></span>                                                  |                                                 |
| <span data-ttu-id="c29b0-129">public int selectionStartLine()</span><span class="sxs-lookup"><span data-stu-id="c29b0-129">public int selectionStartLine()</span></span>                                                 |                                                 |
| <span data-ttu-id="c29b0-130">::public static Editor open (str documentPath)</span><span class="sxs-lookup"><span data-stu-id="c29b0-130">::public static Editor open(str documentPath)</span></span>                                   |                                                 |
| <span data-ttu-id="c29b0-131">public void gotoLine(int LineNo)</span><span class="sxs-lookup"><span data-stu-id="c29b0-131">public void gotoLine(int LineNo)</span></span>                                                |                                                 |
| <span data-ttu-id="c29b0-132">public void closeApplicationObjectDialog()</span><span class="sxs-lookup"><span data-stu-id="c29b0-132">public void closeApplicationObjectDialog()</span></span>                                      |                                                 |
| <span data-ttu-id="c29b0-133">public void mark(int line, int col)</span><span class="sxs-lookup"><span data-stu-id="c29b0-133">public void mark(int line, int col)</span></span>                                             |                                                 |
| <span data-ttu-id="c29b0-134">public void executeScript(str scriptName)</span><span class="sxs-lookup"><span data-stu-id="c29b0-134">public void executeScript(str scriptName)</span></span>                                       |                                                 |
| <span data-ttu-id="c29b0-135">public void nextLine()</span><span class="sxs-lookup"><span data-stu-id="c29b0-135">public void nextLine()</span></span>                                                          |                                                 |
| <span data-ttu-id="c29b0-136">public void firstSelectedLine()</span><span class="sxs-lookup"><span data-stu-id="c29b0-136">public void firstSelectedLine()</span></span>                                                 |                                                 |
| <span data-ttu-id="c29b0-137">private void new()</span><span class="sxs-lookup"><span data-stu-id="c29b0-137">private void new()</span></span>                                                              | <span data-ttu-id="c29b0-138">Editor クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="c29b0-138">Initializes a new instance of the Editor class.</span></span> |
| <span data-ttu-id="c29b0-139">public void unmark()</span><span class="sxs-lookup"><span data-stu-id="c29b0-139">public void unmark()</span></span>                                                            |                                                 |
| <span data-ttu-id="c29b0-140">public void insertString(str InsString)</span><span class="sxs-lookup"><span data-stu-id="c29b0-140">public void insertString(str InsString)</span></span>                                         |                                                 |
| <span data-ttu-id="c29b0-141">public void close()</span><span class="sxs-lookup"><span data-stu-id="c29b0-141">public void close()</span></span>                                                             |                                                 |
| <span data-ttu-id="c29b0-142">public void nextSelectedLine()</span><span class="sxs-lookup"><span data-stu-id="c29b0-142">public void nextSelectedLine()</span></span>                                                  |                                                 |
| <span data-ttu-id="c29b0-143">public void closeSearchDialog()</span><span class="sxs-lookup"><span data-stu-id="c29b0-143">public void closeSearchDialog()</span></span>                                                 |                                                 |
| <span data-ttu-id="c29b0-144">public void deleteLines(\[int noOfLines\])</span><span class="sxs-lookup"><span data-stu-id="c29b0-144">public void deleteLines(\[int noOfLines\])</span></span>                                      |                                                 |
| <span data-ttu-id="c29b0-145">public void insertLines(str InsString)</span><span class="sxs-lookup"><span data-stu-id="c29b0-145">public void insertLines(str InsString)</span></span>                                          |                                                 |
| <span data-ttu-id="c29b0-146">public void firstLine()</span><span class="sxs-lookup"><span data-stu-id="c29b0-146">public void firstLine()</span></span>                                                         |                                                 |
| <span data-ttu-id="c29b0-147">public void deleteChars(\[int noOfChars\])</span><span class="sxs-lookup"><span data-stu-id="c29b0-147">public void deleteChars(\[int noOfChars\])</span></span>                                      |                                                 |

### <a name="method-columnno"></a><span data-ttu-id="c29b0-148">メソッド columnNo</span><span class="sxs-lookup"><span data-stu-id="c29b0-148">Method columnNo</span></span>

    public int columnNo()

#### <a name="return-value"></a><span data-ttu-id="c29b0-149">戻り値</span><span class="sxs-lookup"><span data-stu-id="c29b0-149">Return Value</span></span>

### <a name="method-currentline"></a><span data-ttu-id="c29b0-150">メソッド currentLine</span><span class="sxs-lookup"><span data-stu-id="c29b0-150">Method currentLine</span></span>

    public str currentLine()

#### <a name="return-value"></a><span data-ttu-id="c29b0-151">戻り値</span><span class="sxs-lookup"><span data-stu-id="c29b0-151">Return Value</span></span>

### <a name="method-currentlineno"></a><span data-ttu-id="c29b0-152">メソッド currentLineNo</span><span class="sxs-lookup"><span data-stu-id="c29b0-152">Method currentLineNo</span></span>

    public int currentLineNo()

#### <a name="return-value"></a><span data-ttu-id="c29b0-153">戻り値</span><span class="sxs-lookup"><span data-stu-id="c29b0-153">Return Value</span></span>

### <a name="method-getline"></a><span data-ttu-id="c29b0-154">メソッド getLine</span><span class="sxs-lookup"><span data-stu-id="c29b0-154">Method getLine</span></span>

    public str getLine()

#### <a name="return-value"></a><span data-ttu-id="c29b0-155">戻り値</span><span class="sxs-lookup"><span data-stu-id="c29b0-155">Return Value</span></span>

### <a name="method-gotocol"></a><span data-ttu-id="c29b0-156">メソッド gotoCol</span><span class="sxs-lookup"><span data-stu-id="c29b0-156">Method gotoCol</span></span>

    public int gotoCol(int ColumnNo)

#### <a name="parameters"></a><span data-ttu-id="c29b0-157">パラメーター</span><span class="sxs-lookup"><span data-stu-id="c29b0-157">Parameters</span></span>

<span data-ttu-id="c29b0-158">ColumnNo</span><span class="sxs-lookup"><span data-stu-id="c29b0-158">ColumnNo</span></span>  

#### <a name="return-value"></a><span data-ttu-id="c29b0-159">戻り値</span><span class="sxs-lookup"><span data-stu-id="c29b0-159">Return Value</span></span>

### <a name="method-lineno"></a><span data-ttu-id="c29b0-160">メソッド lineNo</span><span class="sxs-lookup"><span data-stu-id="c29b0-160">Method lineNo</span></span>

    public int lineNo()

#### <a name="return-value"></a><span data-ttu-id="c29b0-161">戻り値</span><span class="sxs-lookup"><span data-stu-id="c29b0-161">Return Value</span></span>

### <a name="method-markmode"></a><span data-ttu-id="c29b0-162">メソッド markMode</span><span class="sxs-lookup"><span data-stu-id="c29b0-162">Method markMode</span></span>

    public MarkMode markMode()

#### <a name="return-value"></a><span data-ttu-id="c29b0-163">戻り値</span><span class="sxs-lookup"><span data-stu-id="c29b0-163">Return Value</span></span>

### <a name="method-matchcase"></a><span data-ttu-id="c29b0-164">メソッド matchCase</span><span class="sxs-lookup"><span data-stu-id="c29b0-164">Method matchCase</span></span>

    public boolean matchCase([boolean UseMatchCase])

#### <a name="parameters"></a><span data-ttu-id="c29b0-165">パラメーター</span><span class="sxs-lookup"><span data-stu-id="c29b0-165">Parameters</span></span>

<span data-ttu-id="c29b0-166">UseMatchCase</span><span class="sxs-lookup"><span data-stu-id="c29b0-166">UseMatchCase</span></span>  

#### <a name="return-value"></a><span data-ttu-id="c29b0-167">戻り値</span><span class="sxs-lookup"><span data-stu-id="c29b0-167">Return Value</span></span>

### <a name="method-morelines"></a><span data-ttu-id="c29b0-168">メソッド moreLines</span><span class="sxs-lookup"><span data-stu-id="c29b0-168">Method moreLines</span></span>

    public boolean moreLines()

#### <a name="return-value"></a><span data-ttu-id="c29b0-169">戻り値</span><span class="sxs-lookup"><span data-stu-id="c29b0-169">Return Value</span></span>

### <a name="method-moreselectedlines"></a><span data-ttu-id="c29b0-170">メソッド moreSelectedLines</span><span class="sxs-lookup"><span data-stu-id="c29b0-170">Method moreSelectedLines</span></span>

    public boolean moreSelectedLines()

#### <a name="return-value"></a><span data-ttu-id="c29b0-171">戻り値</span><span class="sxs-lookup"><span data-stu-id="c29b0-171">Return Value</span></span>

### <a name="method-path"></a><span data-ttu-id="c29b0-172">メソッド path</span><span class="sxs-lookup"><span data-stu-id="c29b0-172">Method path</span></span>

    public str path()

#### <a name="return-value"></a><span data-ttu-id="c29b0-173">戻り値</span><span class="sxs-lookup"><span data-stu-id="c29b0-173">Return Value</span></span>

### <a name="method-regexp"></a><span data-ttu-id="c29b0-174">メソッド regexp</span><span class="sxs-lookup"><span data-stu-id="c29b0-174">Method regexp</span></span>

    public boolean regexp([boolean UseRegExp])

#### <a name="parameters"></a><span data-ttu-id="c29b0-175">パラメーター</span><span class="sxs-lookup"><span data-stu-id="c29b0-175">Parameters</span></span>

<span data-ttu-id="c29b0-176">UseRegExp</span><span class="sxs-lookup"><span data-stu-id="c29b0-176">UseRegExp</span></span>  

#### <a name="return-value"></a><span data-ttu-id="c29b0-177">戻り値</span><span class="sxs-lookup"><span data-stu-id="c29b0-177">Return Value</span></span>

### <a name="method-replace"></a><span data-ttu-id="c29b0-178">メソッド replace</span><span class="sxs-lookup"><span data-stu-id="c29b0-178">Method replace</span></span>

    public boolean replace(str SearchString, str ReplaceString, boolean ReplaceAll)

#### <a name="parameters"></a><span data-ttu-id="c29b0-179">パラメーター</span><span class="sxs-lookup"><span data-stu-id="c29b0-179">Parameters</span></span>

<span data-ttu-id="c29b0-180">SearchString</span><span class="sxs-lookup"><span data-stu-id="c29b0-180">SearchString</span></span>  

<!-- -->

<span data-ttu-id="c29b0-181">ReplaceString</span><span class="sxs-lookup"><span data-stu-id="c29b0-181">ReplaceString</span></span>  

<!-- -->

<span data-ttu-id="c29b0-182">ReplaceAll</span><span class="sxs-lookup"><span data-stu-id="c29b0-182">ReplaceAll</span></span>  

#### <a name="return-value"></a><span data-ttu-id="c29b0-183">戻り値</span><span class="sxs-lookup"><span data-stu-id="c29b0-183">Return Value</span></span>

### <a name="method-search"></a><span data-ttu-id="c29b0-184">メソッド search</span><span class="sxs-lookup"><span data-stu-id="c29b0-184">Method search</span></span>

    public boolean search(str SearchString)

#### <a name="parameters"></a><span data-ttu-id="c29b0-185">パラメーター</span><span class="sxs-lookup"><span data-stu-id="c29b0-185">Parameters</span></span>

<span data-ttu-id="c29b0-186">SearchString</span><span class="sxs-lookup"><span data-stu-id="c29b0-186">SearchString</span></span>  

#### <a name="return-value"></a><span data-ttu-id="c29b0-187">戻り値</span><span class="sxs-lookup"><span data-stu-id="c29b0-187">Return Value</span></span>

### <a name="method-searchstring"></a><span data-ttu-id="c29b0-188">メソッド searchString</span><span class="sxs-lookup"><span data-stu-id="c29b0-188">Method searchString</span></span>

    public str searchString()

#### <a name="return-value"></a><span data-ttu-id="c29b0-189">戻り値</span><span class="sxs-lookup"><span data-stu-id="c29b0-189">Return Value</span></span>

### <a name="method-selectionendcol"></a><span data-ttu-id="c29b0-190">メソッド selectionEndCol</span><span class="sxs-lookup"><span data-stu-id="c29b0-190">Method selectionEndCol</span></span>

    public int selectionEndCol()

#### <a name="return-value"></a><span data-ttu-id="c29b0-191">戻り値</span><span class="sxs-lookup"><span data-stu-id="c29b0-191">Return Value</span></span>

### <a name="method-selectionendline"></a><span data-ttu-id="c29b0-192">メソッド selectionEndLine</span><span class="sxs-lookup"><span data-stu-id="c29b0-192">Method selectionEndLine</span></span>

    public int selectionEndLine()

#### <a name="return-value"></a><span data-ttu-id="c29b0-193">戻り値</span><span class="sxs-lookup"><span data-stu-id="c29b0-193">Return Value</span></span>

### <a name="method-selectionstartcol"></a><span data-ttu-id="c29b0-194">メソッド selectionStartCol</span><span class="sxs-lookup"><span data-stu-id="c29b0-194">Method selectionStartCol</span></span>

    public int selectionStartCol()

#### <a name="return-value"></a><span data-ttu-id="c29b0-195">戻り値</span><span class="sxs-lookup"><span data-stu-id="c29b0-195">Return Value</span></span>

### <a name="method-selectionstartline"></a><span data-ttu-id="c29b0-196">メソッド selectionStartLine</span><span class="sxs-lookup"><span data-stu-id="c29b0-196">Method selectionStartLine</span></span>

    public int selectionStartLine()

#### <a name="return-value"></a><span data-ttu-id="c29b0-197">戻り値</span><span class="sxs-lookup"><span data-stu-id="c29b0-197">Return Value</span></span>

### <a name="method-open"></a><span data-ttu-id="c29b0-198">メソッド open</span><span class="sxs-lookup"><span data-stu-id="c29b0-198">Method open</span></span>

    public static Editor open(str documentPath)

#### <a name="parameters"></a><span data-ttu-id="c29b0-199">パラメーター</span><span class="sxs-lookup"><span data-stu-id="c29b0-199">Parameters</span></span>

<span data-ttu-id="c29b0-200">documentPath</span><span class="sxs-lookup"><span data-stu-id="c29b0-200">documentPath</span></span>  

#### <a name="return-value"></a><span data-ttu-id="c29b0-201">戻り値</span><span class="sxs-lookup"><span data-stu-id="c29b0-201">Return Value</span></span>

### <a name="method-gotoline"></a><span data-ttu-id="c29b0-202">メソッド gotoLine</span><span class="sxs-lookup"><span data-stu-id="c29b0-202">Method gotoLine</span></span>

    public void gotoLine(int LineNo)

#### <a name="parameters"></a><span data-ttu-id="c29b0-203">パラメーター</span><span class="sxs-lookup"><span data-stu-id="c29b0-203">Parameters</span></span>

<span data-ttu-id="c29b0-204">LineNo</span><span class="sxs-lookup"><span data-stu-id="c29b0-204">LineNo</span></span>  

### <a name="method-closeapplicationobjectdialog"></a><span data-ttu-id="c29b0-205">メソッド closeApplicationObjectDialog</span><span class="sxs-lookup"><span data-stu-id="c29b0-205">Method closeApplicationObjectDialog</span></span>

    public void closeApplicationObjectDialog()

### <a name="method-mark"></a><span data-ttu-id="c29b0-206">メソッド mark</span><span class="sxs-lookup"><span data-stu-id="c29b0-206">Method mark</span></span>

    public void mark(int line, int col)

#### <a name="parameters"></a><span data-ttu-id="c29b0-207">パラメーター</span><span class="sxs-lookup"><span data-stu-id="c29b0-207">Parameters</span></span>

<span data-ttu-id="c29b0-208">明細行</span><span class="sxs-lookup"><span data-stu-id="c29b0-208">line</span></span>  

<!-- -->

<span data-ttu-id="c29b0-209">col</span><span class="sxs-lookup"><span data-stu-id="c29b0-209">col</span></span>  

### <a name="method-executescript"></a><span data-ttu-id="c29b0-210">メソッド executeScript</span><span class="sxs-lookup"><span data-stu-id="c29b0-210">Method executeScript</span></span>

    public void executeScript(str scriptName)

#### <a name="parameters"></a><span data-ttu-id="c29b0-211">パラメーター</span><span class="sxs-lookup"><span data-stu-id="c29b0-211">Parameters</span></span>

<span data-ttu-id="c29b0-212">scriptName</span><span class="sxs-lookup"><span data-stu-id="c29b0-212">scriptName</span></span>  

### <a name="method-nextline"></a><span data-ttu-id="c29b0-213">メソッド nextLine</span><span class="sxs-lookup"><span data-stu-id="c29b0-213">Method nextLine</span></span>

    public void nextLine()

### <a name="method-firstselectedline"></a><span data-ttu-id="c29b0-214">メソッド firstSelectedLine</span><span class="sxs-lookup"><span data-stu-id="c29b0-214">Method firstSelectedLine</span></span>

    public void firstSelectedLine()

### <a name="method-new"></a><span data-ttu-id="c29b0-215">メソッド new</span><span class="sxs-lookup"><span data-stu-id="c29b0-215">Method new</span></span>

<span data-ttu-id="c29b0-216">Editor クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="c29b0-216">Initializes a new instance of the Editor class.</span></span>

    private void new()

### <a name="method-unmark"></a><span data-ttu-id="c29b0-217">メソッド unmark</span><span class="sxs-lookup"><span data-stu-id="c29b0-217">Method unmark</span></span>

    public void unmark()

### <a name="method-insertstring"></a><span data-ttu-id="c29b0-218">メソッド insertString</span><span class="sxs-lookup"><span data-stu-id="c29b0-218">Method insertString</span></span>

    public void insertString(str InsString)

#### <a name="parameters"></a><span data-ttu-id="c29b0-219">パラメーター</span><span class="sxs-lookup"><span data-stu-id="c29b0-219">Parameters</span></span>

<span data-ttu-id="c29b0-220">InsString</span><span class="sxs-lookup"><span data-stu-id="c29b0-220">InsString</span></span>  

### <a name="method-close"></a><span data-ttu-id="c29b0-221">メソッド close</span><span class="sxs-lookup"><span data-stu-id="c29b0-221">Method close</span></span>

    public void close()

### <a name="method-nextselectedline"></a><span data-ttu-id="c29b0-222">メソッド nextSelectedLine</span><span class="sxs-lookup"><span data-stu-id="c29b0-222">Method nextSelectedLine</span></span>

    public void nextSelectedLine()

### <a name="method-closesearchdialog"></a><span data-ttu-id="c29b0-223">メソッド closeSearchDialog</span><span class="sxs-lookup"><span data-stu-id="c29b0-223">Method closeSearchDialog</span></span>

    public void closeSearchDialog()

### <a name="method-deletelines"></a><span data-ttu-id="c29b0-224">メソッド deleteLines</span><span class="sxs-lookup"><span data-stu-id="c29b0-224">Method deleteLines</span></span>

    public void deleteLines([int noOfLines])

#### <a name="parameters"></a><span data-ttu-id="c29b0-225">パラメーター</span><span class="sxs-lookup"><span data-stu-id="c29b0-225">Parameters</span></span>

<span data-ttu-id="c29b0-226">noOfLines</span><span class="sxs-lookup"><span data-stu-id="c29b0-226">noOfLines</span></span>  

### <a name="method-insertlines"></a><span data-ttu-id="c29b0-227">メソッド insertLines</span><span class="sxs-lookup"><span data-stu-id="c29b0-227">Method insertLines</span></span>

    public void insertLines(str InsString)

#### <a name="parameters"></a><span data-ttu-id="c29b0-228">パラメーター</span><span class="sxs-lookup"><span data-stu-id="c29b0-228">Parameters</span></span>

<span data-ttu-id="c29b0-229">InsString</span><span class="sxs-lookup"><span data-stu-id="c29b0-229">InsString</span></span>  

### <a name="method-firstline"></a><span data-ttu-id="c29b0-230">メソッド firstLine</span><span class="sxs-lookup"><span data-stu-id="c29b0-230">Method firstLine</span></span>

    public void firstLine()

### <a name="method-deletechars"></a><span data-ttu-id="c29b0-231">メソッド deleteChars</span><span class="sxs-lookup"><span data-stu-id="c29b0-231">Method deleteChars</span></span>

    public void deleteChars([int noOfChars])

#### <a name="parameters"></a><span data-ttu-id="c29b0-232">パラメーター</span><span class="sxs-lookup"><span data-stu-id="c29b0-232">Parameters</span></span>

<span data-ttu-id="c29b0-233">noOfChars</span><span class="sxs-lookup"><span data-stu-id="c29b0-233">noOfChars</span></span>  

## <a name="class-enumerator"></a><span data-ttu-id="c29b0-234">クラス列挙子</span><span class="sxs-lookup"><span data-stu-id="c29b0-234">Class Enumerator</span></span>
    class Enumerator extends Object

### <a name="remarks"></a><span data-ttu-id="c29b0-235">備考</span><span class="sxs-lookup"><span data-stu-id="c29b0-235">Remarks</span></span>

### <a name="examples"></a><span data-ttu-id="c29b0-236">例</span><span class="sxs-lookup"><span data-stu-id="c29b0-236">Examples</span></span>

### <a name="methods"></a><span data-ttu-id="c29b0-237">メソッド</span><span class="sxs-lookup"><span data-stu-id="c29b0-237">Methods</span></span>

| <span data-ttu-id="c29b0-238">方法</span><span class="sxs-lookup"><span data-stu-id="c29b0-238">Method</span></span>                        | <span data-ttu-id="c29b0-239">説明</span><span class="sxs-lookup"><span data-stu-id="c29b0-239">Description</span></span>                                          |
|-------------------------------|------------------------------------------------------|
| <span data-ttu-id="c29b0-240">public AnyType current()</span><span class="sxs-lookup"><span data-stu-id="c29b0-240">public AnyType current()</span></span>      |                                                      |
| <span data-ttu-id="c29b0-241">public str definitionString()</span><span class="sxs-lookup"><span data-stu-id="c29b0-241">public str definitionString()</span></span> |                                                      |
| <span data-ttu-id="c29b0-242">public boolean moveNext()</span><span class="sxs-lookup"><span data-stu-id="c29b0-242">public boolean moveNext()</span></span>     |                                                      |
| <span data-ttu-id="c29b0-243">public str toString()</span><span class="sxs-lookup"><span data-stu-id="c29b0-243">public str toString()</span></span>         | <span data-ttu-id="c29b0-244">現在のオブジェクトを表す文字列を返します。</span><span class="sxs-lookup"><span data-stu-id="c29b0-244">Returns a string that represents the current object.</span></span> |
| <span data-ttu-id="c29b0-245">public void reset()</span><span class="sxs-lookup"><span data-stu-id="c29b0-245">public void reset()</span></span>           |                                                      |

### <a name="method-current"></a><span data-ttu-id="c29b0-246">メソッド current</span><span class="sxs-lookup"><span data-stu-id="c29b0-246">Method current</span></span>

    public AnyType current()

#### <a name="return-value"></a><span data-ttu-id="c29b0-247">戻り値</span><span class="sxs-lookup"><span data-stu-id="c29b0-247">Return Value</span></span>

### <a name="method-definitionstring"></a><span data-ttu-id="c29b0-248">メソッド definitionString</span><span class="sxs-lookup"><span data-stu-id="c29b0-248">Method definitionString</span></span>

    public str definitionString()

#### <a name="return-value"></a><span data-ttu-id="c29b0-249">戻り値</span><span class="sxs-lookup"><span data-stu-id="c29b0-249">Return Value</span></span>

### <a name="method-movenext"></a><span data-ttu-id="c29b0-250">メソッド moveNext</span><span class="sxs-lookup"><span data-stu-id="c29b0-250">Method moveNext</span></span>

    public boolean moveNext()

#### <a name="return-value"></a><span data-ttu-id="c29b0-251">戻り値</span><span class="sxs-lookup"><span data-stu-id="c29b0-251">Return Value</span></span>

### <a name="method-tostring"></a><span data-ttu-id="c29b0-252">メソッド toString</span><span class="sxs-lookup"><span data-stu-id="c29b0-252">Method toString</span></span>

<span data-ttu-id="c29b0-253">現在のオブジェクトを表す文字列を返します。</span><span class="sxs-lookup"><span data-stu-id="c29b0-253">Returns a string that represents the current object.</span></span>

    public str toString()

#### <a name="return-value"></a><span data-ttu-id="c29b0-254">戻り値</span><span class="sxs-lookup"><span data-stu-id="c29b0-254">Return Value</span></span>

<span data-ttu-id="c29b0-255">現在のオブジェクトを表す文字列。</span><span class="sxs-lookup"><span data-stu-id="c29b0-255">A string that represents the current object.</span></span>

#### <a name="remarks"></a><span data-ttu-id="c29b0-256">備考</span><span class="sxs-lookup"><span data-stu-id="c29b0-256">Remarks</span></span>

<span data-ttu-id="c29b0-257">既定の実装は、オブジェクトのクラス名を返します。</span><span class="sxs-lookup"><span data-stu-id="c29b0-257">The default implementation returns the class name of the object.</span></span> <span data-ttu-id="c29b0-258">メソッドは派生クラスで上書きできるため、そのタイプの意味のある値が返されます。</span><span class="sxs-lookup"><span data-stu-id="c29b0-258">The method can be overridden in a derived class to return values that are meaningful for that type.</span></span> <span data-ttu-id="c29b0-259">たとえば、SysMethodInfo クラスのインスタンスは、インスタンスまたは静的などのメソッド名およびメソッドのタイプを返します。</span><span class="sxs-lookup"><span data-stu-id="c29b0-259">For example, an instance of the SysMethodInfo class returns the method name and type of the method, such as instance or static.</span></span>

### <a name="method-reset"></a><span data-ttu-id="c29b0-260">メソッド reset</span><span class="sxs-lookup"><span data-stu-id="c29b0-260">Method reset</span></span>

    public void reset()

## <a name="class-executepermission"></a><span data-ttu-id="c29b0-261">クラス ExecutePermission</span><span class="sxs-lookup"><span data-stu-id="c29b0-261">Class ExecutePermission</span></span>
    class ExecutePermission extends CodeAccessPermission

<span data-ttu-id="c29b0-262">ExecutePermission クラスは、X++ コードの実行を制御します。</span><span class="sxs-lookup"><span data-stu-id="c29b0-262">The ExecutePermission class controls the execution of X++ code.</span></span>

### <a name="remarks"></a><span data-ttu-id="c29b0-263">備考</span><span class="sxs-lookup"><span data-stu-id="c29b0-263">Remarks</span></span>

<span data-ttu-id="c29b0-264">このクラスは、特定の API のアクセス許可をチェックするように設計されています。</span><span class="sxs-lookup"><span data-stu-id="c29b0-264">This class is designed to check permissions for specific APIs.</span></span> <span data-ttu-id="c29b0-265">アクセス許可によって保護されているすべての API のリストについては、「セキュリティで保護された API」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="c29b0-265">For a list of all APIs that are protected by permissions, see Secured APIs.</span></span> <span data-ttu-id="c29b0-266">保護された API が実行される前に、対応する CodeAccessPermission::dema メソッドが呼び出される同じ層 (通常はサーバー層) で assert メソッドを呼び出す必要があります。</span><span class="sxs-lookup"><span data-stu-id="c29b0-266">Before the protected API is executed, you must call the assert method on the same tier (which is usually the server tier) that the corresponding CodeAccessPermission::demand method is called on.</span></span> <span data-ttu-id="c29b0-267">次のいずれかの方法でサーバー層のメソッドを呼び出します:</span><span class="sxs-lookup"><span data-stu-id="c29b0-267">Call a method on the server tier from one of the following methods:</span></span>

-   <span data-ttu-id="c29b0-268">サーバー静的メソッド</span><span class="sxs-lookup"><span data-stu-id="c29b0-268">A server static method</span></span>
-   <span data-ttu-id="c29b0-269">RunOn クラス プロパティを使用して、サーバーで実行するように設定されているクラス インスタンス メソッド</span><span class="sxs-lookup"><span data-stu-id="c29b0-269">A class instance method that is set to run on the server by using the RunOn class property</span></span>

### <a name="examples"></a><span data-ttu-id="c29b0-270">例</span><span class="sxs-lookup"><span data-stu-id="c29b0-270">Examples</span></span>

<span data-ttu-id="c29b0-271">次のコード例は、ExecutePermission クラスの新しいインスタンスを示しています。</span><span class="sxs-lookup"><span data-stu-id="c29b0-271">The following code example shows a new instance of the ExecutePermission class.</span></span> <span data-ttu-id="c29b0-272">assert メソッドが呼び出され、コードが Thread.new メソッドを呼び出して新規スレッドを作成できることが宣言されます。</span><span class="sxs-lookup"><span data-stu-id="c29b0-272">The assert method is called to declare that the code can then call the Thread.new method to create a new thread.</span></span>

    server static void main(Args args) 
    { 
        Thread _t; 
        ExecutePermission _perm; 
        _perm = new ExecutePermission(); 
        if (!_perm) 
        { 
            return; 
        } 
        _perm.assert(); 
        // Invoke the protected API. 
         _t = new Thread(); 
        // Call member methods. 
        if (_t) 
        { 
            _t.removeOnComplete(true); 
            _t.run(classnum(SysCodeProfiler), identifierstr(transferFile)); 
        } 
        // Optionally, call revertAssert() to limit scope of assert. 
        CodeAccessPermission::revertAssert(); 
    }

### <a name="methods"></a><span data-ttu-id="c29b0-273">メソッド</span><span class="sxs-lookup"><span data-stu-id="c29b0-273">Methods</span></span>

| <span data-ttu-id="c29b0-274">方法</span><span class="sxs-lookup"><span data-stu-id="c29b0-274">Method</span></span>                                                 | <span data-ttu-id="c29b0-275">説明</span><span class="sxs-lookup"><span data-stu-id="c29b0-275">Description</span></span>                                                                      |
|--------------------------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="c29b0-276">public CodeAccessPermission copy()</span><span class="sxs-lookup"><span data-stu-id="c29b0-276">public CodeAccessPermission copy()</span></span>                     | <span data-ttu-id="c29b0-277">現在のアクセス許可クラス オブジェクトのコピーを作成し、返します。</span><span class="sxs-lookup"><span data-stu-id="c29b0-277">Creates and returns a copy of the current permission class object.</span></span>               |
| <span data-ttu-id="c29b0-278">public boolean isSubsetOf(CodeAccessPermission target)</span><span class="sxs-lookup"><span data-stu-id="c29b0-278">public boolean isSubsetOf(CodeAccessPermission target)</span></span> | <span data-ttu-id="c29b0-279">現在のアクセス許可が指定したアクセス許可のサブセットかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="c29b0-279">Determines whether a current permission is a subset of the specified permission.</span></span> |
| <span data-ttu-id="c29b0-280">public void new()</span><span class="sxs-lookup"><span data-stu-id="c29b0-280">public void new()</span></span>                                      | <span data-ttu-id="c29b0-281">ExecutePermission クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="c29b0-281">Initializes a new instance of the ExecutePermission class.</span></span>                       |

### <a name="method-copy"></a><span data-ttu-id="c29b0-282">メソッド copy</span><span class="sxs-lookup"><span data-stu-id="c29b0-282">Method copy</span></span>

<span data-ttu-id="c29b0-283">現在のアクセス許可クラス オブジェクトのコピーを作成し、返します。</span><span class="sxs-lookup"><span data-stu-id="c29b0-283">Creates and returns a copy of the current permission class object.</span></span>

    public CodeAccessPermission copy()

#### <a name="return-value"></a><span data-ttu-id="c29b0-284">戻り値</span><span class="sxs-lookup"><span data-stu-id="c29b0-284">Return Value</span></span>

<span data-ttu-id="c29b0-285">現在のアクセス許可オブジェクトのコピーです。</span><span class="sxs-lookup"><span data-stu-id="c29b0-285">A copy of the current permission object.</span></span>

#### <a name="remarks"></a><span data-ttu-id="c29b0-286">備考</span><span class="sxs-lookup"><span data-stu-id="c29b0-286">Remarks</span></span>

<span data-ttu-id="c29b0-287">CodeAccessPermission クラスからクラスを派生させる場合に、このメソッドを上書きします。</span><span class="sxs-lookup"><span data-stu-id="c29b0-287">You override this method when you derive a class from the CodeAccessPermission class.</span></span>

### <a name="method-issubsetof"></a><span data-ttu-id="c29b0-288">メソッド isSubsetOf</span><span class="sxs-lookup"><span data-stu-id="c29b0-288">Method isSubsetOf</span></span>

<span data-ttu-id="c29b0-289">現在のアクセス許可が指定したアクセス許可のサブセットかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="c29b0-289">Determines whether a current permission is a subset of the specified permission.</span></span>

    public boolean isSubsetOf(CodeAccessPermission target)

#### <a name="parameters"></a><span data-ttu-id="c29b0-290">パラメーター</span><span class="sxs-lookup"><span data-stu-id="c29b0-290">Parameters</span></span>

<span data-ttu-id="c29b0-291">target</span><span class="sxs-lookup"><span data-stu-id="c29b0-291">target</span></span>  
<span data-ttu-id="c29b0-292">CodeAccessPermission クラス オブジェクト。</span><span class="sxs-lookup"><span data-stu-id="c29b0-292">A CodeAccessPermission class object.</span></span>

#### <a name="return-value"></a><span data-ttu-id="c29b0-293">戻り値</span><span class="sxs-lookup"><span data-stu-id="c29b0-293">Return Value</span></span>

<span data-ttu-id="c29b0-294">現在のアクセス許可が指定したアクセス許可のサブセットである場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="c29b0-294">true if a current permission is a subset of the specified permission; otherwise, false.</span></span>

#### <a name="remarks"></a><span data-ttu-id="c29b0-295">備考</span><span class="sxs-lookup"><span data-stu-id="c29b0-295">Remarks</span></span>

<span data-ttu-id="c29b0-296">CodeAccessPermission クラスからクラスを派生させる場合に、このメソッドを上書きします。</span><span class="sxs-lookup"><span data-stu-id="c29b0-296">You override this method when you derive a class from the CodeAccessPermission class.</span></span>

### <a name="method-new"></a><span data-ttu-id="c29b0-297">メソッド new</span><span class="sxs-lookup"><span data-stu-id="c29b0-297">Method new</span></span>

<span data-ttu-id="c29b0-298">ExecutePermission クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="c29b0-298">Initializes a new instance of the ExecutePermission class.</span></span> <span data-ttu-id="c29b0-299">終了。</span><span class="sxs-lookup"><span data-stu-id="c29b0-299">End.</span></span>

    public void new()



