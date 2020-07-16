---
title: Editor クラス
description: このトピックでは、Editor クラスについて説明します。
author: robinarh
manager: tonyafehr
ms.date: 06/25/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.search.scope: Operations
ms.search.region: Global
ms.author: rhaertle
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a84952684ecc666ca85a5cdf31babd73d4660e5e
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502669"
---
# <a name="class-editor"></a><span data-ttu-id="04075-103">クラス エディター</span><span class="sxs-lookup"><span data-stu-id="04075-103">Class Editor</span></span>

[!include [banner](../../includes/banner.md)]


```xpp
class Editor extends Object
```

## <a name="remarks"></a><span data-ttu-id="04075-104">備考</span><span class="sxs-lookup"><span data-stu-id="04075-104">Remarks</span></span>

## <a name="examples"></a><span data-ttu-id="04075-105">例</span><span class="sxs-lookup"><span data-stu-id="04075-105">Examples</span></span>

## <a name="methods"></a><span data-ttu-id="04075-106">メソッド</span><span class="sxs-lookup"><span data-stu-id="04075-106">Methods</span></span>

| <span data-ttu-id="04075-107">方法</span><span class="sxs-lookup"><span data-stu-id="04075-107">Method</span></span>                                                                          | <span data-ttu-id="04075-108">説明</span><span class="sxs-lookup"><span data-stu-id="04075-108">Description</span></span>                                     |
|---------------------------------------------------------------------------------|-------------------------------------------------|
| <span data-ttu-id="04075-109">public int columnNo()</span><span class="sxs-lookup"><span data-stu-id="04075-109">public int columnNo()</span></span>                                                           |                                                 |
| <span data-ttu-id="04075-110">public str currentLine()</span><span class="sxs-lookup"><span data-stu-id="04075-110">public str currentLine()</span></span>                                                        |                                                 |
| <span data-ttu-id="04075-111">public int currentLineNo()</span><span class="sxs-lookup"><span data-stu-id="04075-111">public int currentLineNo()</span></span>                                                      |                                                 |
| <span data-ttu-id="04075-112">public str getLine()</span><span class="sxs-lookup"><span data-stu-id="04075-112">public str getLine()</span></span>                                                            |                                                 |
| <span data-ttu-id="04075-113">public int gotoCol(int ColumnNo)</span><span class="sxs-lookup"><span data-stu-id="04075-113">public int gotoCol(int ColumnNo)</span></span>                                                |                                                 |
| <span data-ttu-id="04075-114">public int lineNo()</span><span class="sxs-lookup"><span data-stu-id="04075-114">public int lineNo()</span></span>                                                             |                                                 |
| <span data-ttu-id="04075-115">public MarkMode markMode()</span><span class="sxs-lookup"><span data-stu-id="04075-115">public MarkMode markMode()</span></span>                                                      |                                                 |
| <span data-ttu-id="04075-116">public boolean matchCase(\[boolean UseMatchCase\])</span><span class="sxs-lookup"><span data-stu-id="04075-116">public boolean matchCase(\[boolean UseMatchCase\])</span></span>                              |                                                 |
| <span data-ttu-id="04075-117">public boolean moreLines()</span><span class="sxs-lookup"><span data-stu-id="04075-117">public boolean moreLines()</span></span>                                                      |                                                 |
| <span data-ttu-id="04075-118">public boolean moreSelectedLines()</span><span class="sxs-lookup"><span data-stu-id="04075-118">public boolean moreSelectedLines()</span></span>                                              |                                                 |
| <span data-ttu-id="04075-119">public str path()</span><span class="sxs-lookup"><span data-stu-id="04075-119">public str path()</span></span>                                                               |                                                 |
| <span data-ttu-id="04075-120">public boolean regexp(\[boolean UseRegExp\])</span><span class="sxs-lookup"><span data-stu-id="04075-120">public boolean regexp(\[boolean UseRegExp\])</span></span>                                    |                                                 |
| <span data-ttu-id="04075-121">public boolean replace(str SearchString, str ReplaceString, boolean ReplaceAll)</span><span class="sxs-lookup"><span data-stu-id="04075-121">public boolean replace(str SearchString, str ReplaceString, boolean ReplaceAll)</span></span> |                                                 |
| <span data-ttu-id="04075-122">public boolean search(str SearchString)</span><span class="sxs-lookup"><span data-stu-id="04075-122">public boolean search(str SearchString)</span></span>                                         |                                                 |
| <span data-ttu-id="04075-123">public str searchString()</span><span class="sxs-lookup"><span data-stu-id="04075-123">public str searchString()</span></span>                                                       |                                                 |
| <span data-ttu-id="04075-124">public int selectionEndCol()</span><span class="sxs-lookup"><span data-stu-id="04075-124">public int selectionEndCol()</span></span>                                                    |                                                 |
| <span data-ttu-id="04075-125">public int selectionEndLine()</span><span class="sxs-lookup"><span data-stu-id="04075-125">public int selectionEndLine()</span></span>                                                   |                                                 |
| <span data-ttu-id="04075-126">public int selectionStartCol()</span><span class="sxs-lookup"><span data-stu-id="04075-126">public int selectionStartCol()</span></span>                                                  |                                                 |
| <span data-ttu-id="04075-127">public int selectionStartLine()</span><span class="sxs-lookup"><span data-stu-id="04075-127">public int selectionStartLine()</span></span>                                                 |                                                 |
| <span data-ttu-id="04075-128">::public static Editor open (str documentPath)</span><span class="sxs-lookup"><span data-stu-id="04075-128">::public static Editor open(str documentPath)</span></span>                                   |                                                 |
| <span data-ttu-id="04075-129">public void gotoLine(int LineNo)</span><span class="sxs-lookup"><span data-stu-id="04075-129">public void gotoLine(int LineNo)</span></span>                                                |                                                 |
| <span data-ttu-id="04075-130">public void closeApplicationObjectDialog()</span><span class="sxs-lookup"><span data-stu-id="04075-130">public void closeApplicationObjectDialog()</span></span>                                      |                                                 |
| <span data-ttu-id="04075-131">public void mark(int line, int col)</span><span class="sxs-lookup"><span data-stu-id="04075-131">public void mark(int line, int col)</span></span>                                             |                                                 |
| <span data-ttu-id="04075-132">public void executeScript(str scriptName)</span><span class="sxs-lookup"><span data-stu-id="04075-132">public void executeScript(str scriptName)</span></span>                                       |                                                 |
| <span data-ttu-id="04075-133">public void nextLine()</span><span class="sxs-lookup"><span data-stu-id="04075-133">public void nextLine()</span></span>                                                          |                                                 |
| <span data-ttu-id="04075-134">public void firstSelectedLine()</span><span class="sxs-lookup"><span data-stu-id="04075-134">public void firstSelectedLine()</span></span>                                                 |                                                 |
| <span data-ttu-id="04075-135">private void new()</span><span class="sxs-lookup"><span data-stu-id="04075-135">private void new()</span></span>                                                              | <span data-ttu-id="04075-136">Editor クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="04075-136">Initializes a new instance of the Editor class.</span></span> |
| <span data-ttu-id="04075-137">public void unmark()</span><span class="sxs-lookup"><span data-stu-id="04075-137">public void unmark()</span></span>                                                            |                                                 |
| <span data-ttu-id="04075-138">public void insertString(str InsString)</span><span class="sxs-lookup"><span data-stu-id="04075-138">public void insertString(str InsString)</span></span>                                         |                                                 |
| <span data-ttu-id="04075-139">public void close()</span><span class="sxs-lookup"><span data-stu-id="04075-139">public void close()</span></span>                                                             |                                                 |
| <span data-ttu-id="04075-140">public void nextSelectedLine()</span><span class="sxs-lookup"><span data-stu-id="04075-140">public void nextSelectedLine()</span></span>                                                  |                                                 |
| <span data-ttu-id="04075-141">public void closeSearchDialog()</span><span class="sxs-lookup"><span data-stu-id="04075-141">public void closeSearchDialog()</span></span>                                                 |                                                 |
| <span data-ttu-id="04075-142">public void deleteLines(\[int noOfLines\])</span><span class="sxs-lookup"><span data-stu-id="04075-142">public void deleteLines(\[int noOfLines\])</span></span>                                      |                                                 |
| <span data-ttu-id="04075-143">public void insertLines(str InsString)</span><span class="sxs-lookup"><span data-stu-id="04075-143">public void insertLines(str InsString)</span></span>                                          |                                                 |
| <span data-ttu-id="04075-144">public void firstLine()</span><span class="sxs-lookup"><span data-stu-id="04075-144">public void firstLine()</span></span>                                                         |                                                 |
| <span data-ttu-id="04075-145">public void deleteChars(\[int noOfChars\])</span><span class="sxs-lookup"><span data-stu-id="04075-145">public void deleteChars(\[int noOfChars\])</span></span>                                      |                                                 |

## <a name="method-columnno"></a><span data-ttu-id="04075-146">メソッド columnNo</span><span class="sxs-lookup"><span data-stu-id="04075-146">Method columnNo</span></span>

```xpp
public int columnNo()
```

### <a name="return-value---columnno"></a><span data-ttu-id="04075-147">戻り値 - columnNo</span><span class="sxs-lookup"><span data-stu-id="04075-147">Return Value - columnNo</span></span>

## <a name="method-currentline"></a><span data-ttu-id="04075-148">メソッド currentLine</span><span class="sxs-lookup"><span data-stu-id="04075-148">Method currentLine</span></span>

```xpp
public str currentLine()
```

### <a name="return-value---currentline"></a><span data-ttu-id="04075-149">戻り値 - currentLine</span><span class="sxs-lookup"><span data-stu-id="04075-149">Return Value - currentLine</span></span>

## <a name="method-currentlineno"></a><span data-ttu-id="04075-150">メソッド currentLineNo</span><span class="sxs-lookup"><span data-stu-id="04075-150">Method currentLineNo</span></span>

```xpp
public int currentLineNo()
```

### <a name="return-value---currentlineno"></a><span data-ttu-id="04075-151">戻り値 - currentLineNo</span><span class="sxs-lookup"><span data-stu-id="04075-151">Return Value - currentLineNo</span></span>

## <a name="method-getline"></a><span data-ttu-id="04075-152">メソッド getLine</span><span class="sxs-lookup"><span data-stu-id="04075-152">Method getLine</span></span>

```xpp
public str getLine()
```

### <a name="return-value---getline"></a><span data-ttu-id="04075-153">戻り値 - getLine</span><span class="sxs-lookup"><span data-stu-id="04075-153">Return Value - getLine</span></span>

## <a name="method-gotocol"></a><span data-ttu-id="04075-154">メソッド gotoCol</span><span class="sxs-lookup"><span data-stu-id="04075-154">Method gotoCol</span></span>

```xpp
public int gotoCol(int ColumnNo)
```

### <a name="parameters---gotocol"></a><span data-ttu-id="04075-155">パラメーター - gotoCol</span><span class="sxs-lookup"><span data-stu-id="04075-155">Parameters - gotoCol</span></span>

<span data-ttu-id="04075-156">ColumnNo</span><span class="sxs-lookup"><span data-stu-id="04075-156">ColumnNo</span></span>  

### <a name="return-value---gotocol"></a><span data-ttu-id="04075-157">戻り値 - gotoCol</span><span class="sxs-lookup"><span data-stu-id="04075-157">Return Value - gotoCol</span></span>

## <a name="method-lineno"></a><span data-ttu-id="04075-158">メソッド lineNo</span><span class="sxs-lookup"><span data-stu-id="04075-158">Method lineNo</span></span>

```xpp
public int lineNo()
```

### <a name="return-value---lineno"></a><span data-ttu-id="04075-159">戻り値 - lineNo</span><span class="sxs-lookup"><span data-stu-id="04075-159">Return Value - lineNo</span></span>

## <a name="method-markmode"></a><span data-ttu-id="04075-160">メソッド markMode</span><span class="sxs-lookup"><span data-stu-id="04075-160">Method markMode</span></span>

```xpp
public MarkMode markMode()
```

### <a name="return-value---markmode"></a><span data-ttu-id="04075-161">戻り値 - markMode</span><span class="sxs-lookup"><span data-stu-id="04075-161">Return Value - markMode</span></span>

## <a name="method-matchcase"></a><span data-ttu-id="04075-162">メソッド matchCase</span><span class="sxs-lookup"><span data-stu-id="04075-162">Method matchCase</span></span>

```xpp
public boolean matchCase([boolean UseMatchCase])
```

### <a name="parameters---matchcase"></a><span data-ttu-id="04075-163">パラメーター - matchCase</span><span class="sxs-lookup"><span data-stu-id="04075-163">Parameters - matchCase</span></span>

<span data-ttu-id="04075-164">UseMatchCase</span><span class="sxs-lookup"><span data-stu-id="04075-164">UseMatchCase</span></span>  

### <a name="return-value---matchcase"></a><span data-ttu-id="04075-165">戻り値 - matchCase</span><span class="sxs-lookup"><span data-stu-id="04075-165">Return Value - matchCase</span></span>

## <a name="method-morelines"></a><span data-ttu-id="04075-166">メソッド moreLines</span><span class="sxs-lookup"><span data-stu-id="04075-166">Method moreLines</span></span>

```xpp
public boolean moreLines()
```

### <a name="return-value---morelines"></a><span data-ttu-id="04075-167">戻り値 - moreLines</span><span class="sxs-lookup"><span data-stu-id="04075-167">Return Value - moreLines</span></span>

## <a name="method-moreselectedlines"></a><span data-ttu-id="04075-168">メソッド moreSelectedLines</span><span class="sxs-lookup"><span data-stu-id="04075-168">Method moreSelectedLines</span></span>

```xpp
public boolean moreSelectedLines()
```

### <a name="return-value---moreselectedlines"></a><span data-ttu-id="04075-169">戻り値 - moreSelectedLines</span><span class="sxs-lookup"><span data-stu-id="04075-169">Return Value - moreSelectedLines</span></span>

## <a name="method-path"></a><span data-ttu-id="04075-170">メソッド path</span><span class="sxs-lookup"><span data-stu-id="04075-170">Method path</span></span>

```xpp
public str path()
```

### <a name="return-value---path"></a><span data-ttu-id="04075-171">戻り値 - path</span><span class="sxs-lookup"><span data-stu-id="04075-171">Return Value - path</span></span>

## <a name="method-regexp"></a><span data-ttu-id="04075-172">メソッド regexp</span><span class="sxs-lookup"><span data-stu-id="04075-172">Method regexp</span></span>

```xpp
public boolean regexp([boolean UseRegExp])
```

### <a name="parameters---regexp"></a><span data-ttu-id="04075-173">パラメーター - regexp</span><span class="sxs-lookup"><span data-stu-id="04075-173">Parameters - regexp</span></span>

<span data-ttu-id="04075-174">UseRegExp</span><span class="sxs-lookup"><span data-stu-id="04075-174">UseRegExp</span></span>  

### <a name="return-value---regexp"></a><span data-ttu-id="04075-175">戻り値 - regexp</span><span class="sxs-lookup"><span data-stu-id="04075-175">Return Value - regexp</span></span>

## <a name="method-replace"></a><span data-ttu-id="04075-176">メソッド replace</span><span class="sxs-lookup"><span data-stu-id="04075-176">Method replace</span></span>

```xpp
public boolean replace(str SearchString, str ReplaceString, boolean ReplaceAll)
```

### <a name="parameters---replace"></a><span data-ttu-id="04075-177">パラメーター - replace</span><span class="sxs-lookup"><span data-stu-id="04075-177">Parameters - replace</span></span>

<span data-ttu-id="04075-178">SearchString</span><span class="sxs-lookup"><span data-stu-id="04075-178">SearchString</span></span>  

<!-- -->

<span data-ttu-id="04075-179">ReplaceString</span><span class="sxs-lookup"><span data-stu-id="04075-179">ReplaceString</span></span>  

<!-- -->

<span data-ttu-id="04075-180">ReplaceAll</span><span class="sxs-lookup"><span data-stu-id="04075-180">ReplaceAll</span></span>  

### <a name="return-value---replace"></a><span data-ttu-id="04075-181">戻り値 - replace</span><span class="sxs-lookup"><span data-stu-id="04075-181">Return Value - replace</span></span>

## <a name="method-search"></a><span data-ttu-id="04075-182">メソッド search</span><span class="sxs-lookup"><span data-stu-id="04075-182">Method search</span></span>

```xpp
public boolean search(str SearchString)
```

### <a name="parameters---search"></a><span data-ttu-id="04075-183">パラメーター - search</span><span class="sxs-lookup"><span data-stu-id="04075-183">Parameters - search</span></span>

<span data-ttu-id="04075-184">SearchString</span><span class="sxs-lookup"><span data-stu-id="04075-184">SearchString</span></span>  

### <a name="return-value---search"></a><span data-ttu-id="04075-185">戻り値 - search</span><span class="sxs-lookup"><span data-stu-id="04075-185">Return Value - search</span></span>

## <a name="method-searchstring"></a><span data-ttu-id="04075-186">メソッド searchString</span><span class="sxs-lookup"><span data-stu-id="04075-186">Method searchString</span></span>

```xpp
public str searchString()
```

### <a name="return-value---searchstring"></a><span data-ttu-id="04075-187">戻り値 - searchString</span><span class="sxs-lookup"><span data-stu-id="04075-187">Return Value - searchString</span></span>

## <a name="method-selectionendcol"></a><span data-ttu-id="04075-188">メソッド selectionEndCol</span><span class="sxs-lookup"><span data-stu-id="04075-188">Method selectionEndCol</span></span>

```xpp
public int selectionEndCol()
```

### <a name="return-value---selectionendcol"></a><span data-ttu-id="04075-189">戻り値 - selectionEndCol</span><span class="sxs-lookup"><span data-stu-id="04075-189">Return Value - selectionEndCol</span></span>

## <a name="method-selectionendline"></a><span data-ttu-id="04075-190">メソッド selectionEndLine</span><span class="sxs-lookup"><span data-stu-id="04075-190">Method selectionEndLine</span></span>

```xpp
public int selectionEndLine()
```

### <a name="return-value---selectionendline"></a><span data-ttu-id="04075-191">戻り値 - selectionEndLine</span><span class="sxs-lookup"><span data-stu-id="04075-191">Return Value - selectionEndLine</span></span>

## <a name="method-selectionstartcol"></a><span data-ttu-id="04075-192">メソッド selectionStartCol</span><span class="sxs-lookup"><span data-stu-id="04075-192">Method selectionStartCol</span></span>

```xpp
public int selectionStartCol()
```

### <a name="return-value---selectionstartcol"></a><span data-ttu-id="04075-193">戻り値 - selectionStartCol</span><span class="sxs-lookup"><span data-stu-id="04075-193">Return Value - selectionStartCol</span></span>

## <a name="method-selectionstartline"></a><span data-ttu-id="04075-194">メソッド selectionStartLine</span><span class="sxs-lookup"><span data-stu-id="04075-194">Method selectionStartLine</span></span>

```xpp
public int selectionStartLine()
```

### <a name="return-value---selectionstartline"></a><span data-ttu-id="04075-195">戻り値 - selectionStartLine</span><span class="sxs-lookup"><span data-stu-id="04075-195">Return Value - selectionStartLine</span></span>

## <a name="method-open"></a><span data-ttu-id="04075-196">メソッド open</span><span class="sxs-lookup"><span data-stu-id="04075-196">Method open</span></span>

```xpp
public static Editor open(str documentPath)
```

### <a name="parameters---open"></a><span data-ttu-id="04075-197">パラメーター - open</span><span class="sxs-lookup"><span data-stu-id="04075-197">Parameters - open</span></span>

<span data-ttu-id="04075-198">documentPath</span><span class="sxs-lookup"><span data-stu-id="04075-198">documentPath</span></span>  

### <a name="return-value---open"></a><span data-ttu-id="04075-199">戻り値 - open</span><span class="sxs-lookup"><span data-stu-id="04075-199">Return Value - open</span></span>

## <a name="method-gotoline"></a><span data-ttu-id="04075-200">メソッド gotoLine</span><span class="sxs-lookup"><span data-stu-id="04075-200">Method gotoLine</span></span>

```xpp
public void gotoLine(int LineNo)
```

### <a name="parameters---gotoline"></a><span data-ttu-id="04075-201">パラメーター - gotoLine</span><span class="sxs-lookup"><span data-stu-id="04075-201">Parameters - gotoLine</span></span>

<span data-ttu-id="04075-202">LineNo</span><span class="sxs-lookup"><span data-stu-id="04075-202">LineNo</span></span>  

## <a name="method-closeapplicationobjectdialog"></a><span data-ttu-id="04075-203">メソッド closeApplicationObjectDialog</span><span class="sxs-lookup"><span data-stu-id="04075-203">Method closeApplicationObjectDialog</span></span>

```xpp
public void closeApplicationObjectDialog()
```

## <a name="method-mark"></a><span data-ttu-id="04075-204">メソッド mark</span><span class="sxs-lookup"><span data-stu-id="04075-204">Method mark</span></span>

```xpp
public void mark(int line, int col)
```

### <a name="parameters---mark"></a><span data-ttu-id="04075-205">パラメーター - mark</span><span class="sxs-lookup"><span data-stu-id="04075-205">Parameters - mark</span></span>

<span data-ttu-id="04075-206">明細行</span><span class="sxs-lookup"><span data-stu-id="04075-206">line</span></span>  

<!-- -->

<span data-ttu-id="04075-207">col</span><span class="sxs-lookup"><span data-stu-id="04075-207">col</span></span>  

## <a name="method-executescript"></a><span data-ttu-id="04075-208">メソッド executeScript</span><span class="sxs-lookup"><span data-stu-id="04075-208">Method executeScript</span></span>

```xpp
public void executeScript(str scriptName)
```

### <a name="parameters---executescript"></a><span data-ttu-id="04075-209">パラメーター - executeScript</span><span class="sxs-lookup"><span data-stu-id="04075-209">Parameters - executeScript</span></span>

<span data-ttu-id="04075-210">scriptName</span><span class="sxs-lookup"><span data-stu-id="04075-210">scriptName</span></span>  

## <a name="method-nextline"></a><span data-ttu-id="04075-211">メソッド nextLine</span><span class="sxs-lookup"><span data-stu-id="04075-211">Method nextLine</span></span>

```xpp
public void nextLine()
```

## <a name="method-firstselectedline"></a><span data-ttu-id="04075-212">メソッド firstSelectedLine</span><span class="sxs-lookup"><span data-stu-id="04075-212">Method firstSelectedLine</span></span>

```xpp
public void firstSelectedLine()
```

## <a name="method-new"></a><span data-ttu-id="04075-213">メソッド new</span><span class="sxs-lookup"><span data-stu-id="04075-213">Method new</span></span>

<span data-ttu-id="04075-214">Editor クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="04075-214">Initializes a new instance of the Editor class.</span></span>

```xpp
private void new()
```

## <a name="method-unmark"></a><span data-ttu-id="04075-215">メソッド unmark</span><span class="sxs-lookup"><span data-stu-id="04075-215">Method unmark</span></span>

```xpp
public void unmark()
```

## <a name="method-insertstring"></a><span data-ttu-id="04075-216">メソッド insertString</span><span class="sxs-lookup"><span data-stu-id="04075-216">Method insertString</span></span>

```xpp
public void insertString(str InsString)
```

### <a name="parameters---insertstring"></a><span data-ttu-id="04075-217">パラメーター - insertString</span><span class="sxs-lookup"><span data-stu-id="04075-217">Parameters - insertString</span></span>

<span data-ttu-id="04075-218">InsString</span><span class="sxs-lookup"><span data-stu-id="04075-218">InsString</span></span>  

## <a name="method-close"></a><span data-ttu-id="04075-219">メソッド close</span><span class="sxs-lookup"><span data-stu-id="04075-219">Method close</span></span>

```xpp
public void close()
```

## <a name="method-nextselectedline"></a><span data-ttu-id="04075-220">メソッド nextSelectedLine</span><span class="sxs-lookup"><span data-stu-id="04075-220">Method nextSelectedLine</span></span>

```xpp
public void nextSelectedLine()
```

## <a name="method-closesearchdialog"></a><span data-ttu-id="04075-221">メソッド closeSearchDialog</span><span class="sxs-lookup"><span data-stu-id="04075-221">Method closeSearchDialog</span></span>

```xpp
public void closeSearchDialog()
```

## <a name="method-deletelines"></a><span data-ttu-id="04075-222">メソッド deleteLines</span><span class="sxs-lookup"><span data-stu-id="04075-222">Method deleteLines</span></span>

```xpp
public void deleteLines([int noOfLines])
```

### <a name="parameters---deletelines"></a><span data-ttu-id="04075-223">パラメーター - deleteLines</span><span class="sxs-lookup"><span data-stu-id="04075-223">Parameters - deleteLines</span></span>

<span data-ttu-id="04075-224">noOfLines</span><span class="sxs-lookup"><span data-stu-id="04075-224">noOfLines</span></span>  

## <a name="method-insertlines"></a><span data-ttu-id="04075-225">メソッド insertLines</span><span class="sxs-lookup"><span data-stu-id="04075-225">Method insertLines</span></span>

```xpp
public void insertLines(str InsString)
```

### <a name="parameters---insertlines"></a><span data-ttu-id="04075-226">パラメーター - insertLines</span><span class="sxs-lookup"><span data-stu-id="04075-226">Parameters - insertLines</span></span>

<span data-ttu-id="04075-227">InsString</span><span class="sxs-lookup"><span data-stu-id="04075-227">InsString</span></span>  

## <a name="method-firstline"></a><span data-ttu-id="04075-228">メソッド firstLine</span><span class="sxs-lookup"><span data-stu-id="04075-228">Method firstLine</span></span>

```xpp
public void firstLine()
```

## <a name="method-deletechars"></a><span data-ttu-id="04075-229">メソッド deleteChars</span><span class="sxs-lookup"><span data-stu-id="04075-229">Method deleteChars</span></span>

```xpp
public void deleteChars([int noOfChars])
```

### <a name="parameters---deletechars"></a><span data-ttu-id="04075-230">パラメーター - deleteChars</span><span class="sxs-lookup"><span data-stu-id="04075-230">Parameters - deleteChars</span></span>

<span data-ttu-id="04075-231">noOfChars</span><span class="sxs-lookup"><span data-stu-id="04075-231">noOfChars</span></span>  

