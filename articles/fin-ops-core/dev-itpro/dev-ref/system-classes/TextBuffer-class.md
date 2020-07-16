---
title: TextBuffer クラス
description: このトピックでは、TextBuffer クラスについて説明します。
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
ms.openlocfilehash: ac38afd29dbc6511333ecc5eacf9bfdc4d186419
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502790"
---
# <a name="class-textbuffer"></a><span data-ttu-id="d3eb7-103">クラス TextBuffer</span><span class="sxs-lookup"><span data-stu-id="d3eb7-103">Class TextBuffer</span></span>

[!include [banner](../../includes/banner.md)]

```xpp
class TextBuffer extends Object
```

<span data-ttu-id="d3eb7-104">TextBuffer クラスは、任意のテキスト ファイル内容を管理し、テキストを生成して操作します。</span><span class="sxs-lookup"><span data-stu-id="d3eb7-104">The TextBuffer class manages arbitrary text file content, and generates and manipulates text.</span></span>

## <a name="remarks"></a><span data-ttu-id="d3eb7-105">備考</span><span class="sxs-lookup"><span data-stu-id="d3eb7-105">Remarks</span></span>

<span data-ttu-id="d3eb7-106">このクラスは、さまざまな文字列操作、シンプルなクリップボード、ファイル インターフェイスを備えています。</span><span class="sxs-lookup"><span data-stu-id="d3eb7-106">This class features various string operations, a simple clipboard, and a file interface.</span></span>

## <a name="examples"></a><span data-ttu-id="d3eb7-107">例</span><span class="sxs-lookup"><span data-stu-id="d3eb7-107">Examples</span></span>

```xpp
static void example() 
{ 
    FileIoPermission _perm = new FileIoPermission("myfile.txt",'r'); 
    TextBuffer txtb = new TextBuffer(); 
    _perm.assert(); 
    txtb.fromFile("myfile.txt"); // Read text from file 
    txtb.toClipboard(); // Copy it to the clipboard 
}
```

## <a name="methods"></a><span data-ttu-id="d3eb7-108">メソッド</span><span class="sxs-lookup"><span data-stu-id="d3eb7-108">Methods</span></span>

| <span data-ttu-id="d3eb7-109">方法</span><span class="sxs-lookup"><span data-stu-id="d3eb7-109">Method</span></span>                                                                 | <span data-ttu-id="d3eb7-110">説明</span><span class="sxs-lookup"><span data-stu-id="d3eb7-110">Description</span></span>                                                                                           |
|------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d3eb7-111">public boolean accept(str searchText)</span><span class="sxs-lookup"><span data-stu-id="d3eb7-111">public boolean accept(str searchText)</span></span>                                  |                                                                                                       |
| <span data-ttu-id="d3eb7-112">public int decryptOld(int cryptKey)</span><span class="sxs-lookup"><span data-stu-id="d3eb7-112">public int decryptOld(int cryptKey)</span></span>                                    |                                                                                                       |
| <span data-ttu-id="d3eb7-113">public boolean find(str searchText, \[int start\])</span><span class="sxs-lookup"><span data-stu-id="d3eb7-113">public boolean find(str searchText, \[int start\])</span></span>                     | <span data-ttu-id="d3eb7-114">TextBuffer オブジェクトで文字列式の発生を検索します。</span><span class="sxs-lookup"><span data-stu-id="d3eb7-114">Searches the TextBuffer object for any occurrence of a string expression.</span></span>                             |
| <span data-ttu-id="d3eb7-115">public boolean fromClipboard()</span><span class="sxs-lookup"><span data-stu-id="d3eb7-115">public boolean fromClipboard()</span></span>                                         | <span data-ttu-id="d3eb7-116">TextBuffer オブジェクトの内容をクリップボードの内容に置き換えます。</span><span class="sxs-lookup"><span data-stu-id="d3eb7-116">Replaces the content of the TextBuffer object with the content of the clipboard.</span></span>                      |
| <span data-ttu-id="d3eb7-117">public boolean fromFile(str filename, \[int encoding\])</span><span class="sxs-lookup"><span data-stu-id="d3eb7-117">public boolean fromFile(str filename, \[int encoding\])</span></span>                | <span data-ttu-id="d3eb7-118">TextBuffer オブジェクトの内容を指定したファイルの内容に置き換えます。</span><span class="sxs-lookup"><span data-stu-id="d3eb7-118">Replaces the content of a TextBuffer object with the content of the specified file.</span></span>                   |
| <span data-ttu-id="d3eb7-119">public str getText()</span><span class="sxs-lookup"><span data-stu-id="d3eb7-119">public str getText()</span></span>                                                   | <span data-ttu-id="d3eb7-120">TextBuffer オブジェクトの現在の内容を取得します。</span><span class="sxs-lookup"><span data-stu-id="d3eb7-120">Retrieves the current content of the TextBuffer object.</span></span>                                               |
| <span data-ttu-id="d3eb7-121">public int getValue()</span><span class="sxs-lookup"><span data-stu-id="d3eb7-121">public int getValue()</span></span>                                                  |                                                                                                       |
| <span data-ttu-id="d3eb7-122">public boolean ignoreCase(\[boolean ignoreCase\])</span><span class="sxs-lookup"><span data-stu-id="d3eb7-122">public boolean ignoreCase(\[boolean ignoreCase\])</span></span>                      |                                                                                                       |
| <span data-ttu-id="d3eb7-123">public boolean isNext(str searchText)</span><span class="sxs-lookup"><span data-stu-id="d3eb7-123">public boolean isNext(str searchText)</span></span>                                  |                                                                                                       |
| <span data-ttu-id="d3eb7-124">public int matchLen()</span><span class="sxs-lookup"><span data-stu-id="d3eb7-124">public int matchLen()</span></span>                                                  | <span data-ttu-id="d3eb7-125">TextBuffer オブジェクトで最初に一致する文字列の長さを返します。</span><span class="sxs-lookup"><span data-stu-id="d3eb7-125">Returns the string length of the first match in the TextBuffer object.</span></span>                                |
| <span data-ttu-id="d3eb7-126">public int matchPos()</span><span class="sxs-lookup"><span data-stu-id="d3eb7-126">public int matchPos()</span></span>                                                  | <span data-ttu-id="d3eb7-127">TextBuffer オブジェクトの検索文字列の 1 番目の文字の位置を返します。</span><span class="sxs-lookup"><span data-stu-id="d3eb7-127">Returns the character position of the first occurrence of the search string in the TextBuffer object.</span></span> |
| <span data-ttu-id="d3eb7-128">public str nextToken(\[boolean includeWholeLine\], \[str stopAtChar\])</span><span class="sxs-lookup"><span data-stu-id="d3eb7-128">public str nextToken(\[boolean includeWholeLine\], \[str stopAtChar\])</span></span> |                                                                                                       |
| <span data-ttu-id="d3eb7-129">public int numLines()</span><span class="sxs-lookup"><span data-stu-id="d3eb7-129">public int numLines()</span></span>                                                  | <span data-ttu-id="d3eb7-130">TextBuffer オブジェクトの明細行の数を取得します。</span><span class="sxs-lookup"><span data-stu-id="d3eb7-130">Retrieves the number of lines in the TextBuffer object.</span></span>                                               |
| <span data-ttu-id="d3eb7-131">public boolean regularExpressions(\[boolean useRegularExpressions\])</span><span class="sxs-lookup"><span data-stu-id="d3eb7-131">public boolean regularExpressions(\[boolean useRegularExpressions\])</span></span>   |                                                                                                       |
| <span data-ttu-id="d3eb7-132">public int size()</span><span class="sxs-lookup"><span data-stu-id="d3eb7-132">public int size()</span></span>                                                      |                                                                                                       |
| <span data-ttu-id="d3eb7-133">public str subStr(int start, int length)</span><span class="sxs-lookup"><span data-stu-id="d3eb7-133">public str subStr(int start, int length)</span></span>                               | <span data-ttu-id="d3eb7-134">TextBuffer オブジェクト (サブ文字列) の内容の一部を取得します。</span><span class="sxs-lookup"><span data-stu-id="d3eb7-134">Retrieves part of the content of the TextBuffer object (a substring).</span></span>                                 |
| <span data-ttu-id="d3eb7-135">public boolean toFile(str filename, \[int encoding\])</span><span class="sxs-lookup"><span data-stu-id="d3eb7-135">public boolean toFile(str filename, \[int encoding\])</span></span>                  | <span data-ttu-id="d3eb7-136">TextBuffer オブジェクトの内容をファイルに保存します。</span><span class="sxs-lookup"><span data-stu-id="d3eb7-136">Saves the content of the TextBuffer object to a file.</span></span>                                                 |
| <span data-ttu-id="d3eb7-137">public str token()</span><span class="sxs-lookup"><span data-stu-id="d3eb7-137">public str token()</span></span>                                                     |                                                                                                       |
| <span data-ttu-id="d3eb7-138">public str toString()</span><span class="sxs-lookup"><span data-stu-id="d3eb7-138">public str toString()</span></span>                                                  | <span data-ttu-id="d3eb7-139">現在のオブジェクトを表す文字列を返します。</span><span class="sxs-lookup"><span data-stu-id="d3eb7-139">Returns a string that represents the current object.</span></span>                                                  |
| <span data-ttu-id="d3eb7-140">::public static int strHashKey(str sourceString)</span><span class="sxs-lookup"><span data-stu-id="d3eb7-140">::public static int strHashKey(str sourceString)</span></span>                       |                                                                                                       |
| <span data-ttu-id="d3eb7-141">public void new()</span><span class="sxs-lookup"><span data-stu-id="d3eb7-141">public void new()</span></span>                                                      | <span data-ttu-id="d3eb7-142">TextBuffer クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="d3eb7-142">Initializes a new instance of the TextBuffer class.</span></span>                                                   |
| <span data-ttu-id="d3eb7-143">public void removeChar(str charList)</span><span class="sxs-lookup"><span data-stu-id="d3eb7-143">public void removeChar(str charList)</span></span>                                   |                                                                                                       |
| <span data-ttu-id="d3eb7-144">public void toClipboard()</span><span class="sxs-lookup"><span data-stu-id="d3eb7-144">public void toClipboard()</span></span>                                              | <span data-ttu-id="d3eb7-145">TextBuffer オブジェクトの内容をクリップボードにコピーします。</span><span class="sxs-lookup"><span data-stu-id="d3eb7-145">Copies the content of a TextBuffer object to the clipboard.</span></span>                                           |
| <span data-ttu-id="d3eb7-146">public void insert(str insertString, int position)</span><span class="sxs-lookup"><span data-stu-id="d3eb7-146">public void insert(str insertString, int position)</span></span>                     |                                                                                                       |
| <span data-ttu-id="d3eb7-147">public void setText(str string)</span><span class="sxs-lookup"><span data-stu-id="d3eb7-147">public void setText(str string)</span></span>                                        | <span data-ttu-id="d3eb7-148">既存の内容を上書きして、指定した文字列に TextBuffer オブジェクトの内容を設定します。</span><span class="sxs-lookup"><span data-stu-id="d3eb7-148">Sets the content of the TextBuffer object to the specified string, overwriting any existing content.</span></span>  |
| <span data-ttu-id="d3eb7-149">public void appendText(str string)</span><span class="sxs-lookup"><span data-stu-id="d3eb7-149">public void appendText(str string)</span></span>                                     | <span data-ttu-id="d3eb7-150">TextBuffer オブジェクトの内容に文字列を追加します。</span><span class="sxs-lookup"><span data-stu-id="d3eb7-150">Appends a string to the content of the TextBuffer object.</span></span>                                             |
| <span data-ttu-id="d3eb7-151">public void replace(str findString, str replaceString)</span><span class="sxs-lookup"><span data-stu-id="d3eb7-151">public void replace(str findString, str replaceString)</span></span>                 |                                                                                                       |
| <span data-ttu-id="d3eb7-152">public void delete(int start, int length)</span><span class="sxs-lookup"><span data-stu-id="d3eb7-152">public void delete(int start, int length)</span></span>                              |                                                                                                       |

## <a name="method-accept"></a><span data-ttu-id="d3eb7-153">メソッド accept</span><span class="sxs-lookup"><span data-stu-id="d3eb7-153">Method accept</span></span>

```xpp
public boolean accept(str searchText)
```

### <a name="parameters---accept"></a><span data-ttu-id="d3eb7-154">パラメーター - accept</span><span class="sxs-lookup"><span data-stu-id="d3eb7-154">Parameters - accept</span></span>

<span data-ttu-id="d3eb7-155">searchText</span><span class="sxs-lookup"><span data-stu-id="d3eb7-155">searchText</span></span>  

### <a name="return-value---accept"></a><span data-ttu-id="d3eb7-156">戻り値 - accept</span><span class="sxs-lookup"><span data-stu-id="d3eb7-156">Return Value - accept</span></span>

## <a name="method-decryptold"></a><span data-ttu-id="d3eb7-157">メソッド decryptOld</span><span class="sxs-lookup"><span data-stu-id="d3eb7-157">Method decryptOld</span></span>

```xpp
public int decryptOld(int cryptKey)
```

### <a name="parameters---decryptold"></a><span data-ttu-id="d3eb7-158">パラメーター - decryptOld</span><span class="sxs-lookup"><span data-stu-id="d3eb7-158">Parameters - decryptOld</span></span>

<span data-ttu-id="d3eb7-159">cryptKey</span><span class="sxs-lookup"><span data-stu-id="d3eb7-159">cryptKey</span></span>  

### <a name="return-value---decryptold"></a><span data-ttu-id="d3eb7-160">戻り値 - decryptOld</span><span class="sxs-lookup"><span data-stu-id="d3eb7-160">Return Value - decryptOld</span></span>

## <a name="method-find"></a><span data-ttu-id="d3eb7-161">メソッド find</span><span class="sxs-lookup"><span data-stu-id="d3eb7-161">Method find</span></span>

<span data-ttu-id="d3eb7-162">TextBuffer オブジェクトで文字列式の発生を検索します。</span><span class="sxs-lookup"><span data-stu-id="d3eb7-162">Searches the TextBuffer object for any occurrence of a string expression.</span></span>

```xpp
public boolean find(str searchText, [int start])
```

### <a name="parameters---find"></a><span data-ttu-id="d3eb7-163">パラメーター - find</span><span class="sxs-lookup"><span data-stu-id="d3eb7-163">Parameters - find</span></span>

<span data-ttu-id="d3eb7-164">searchText</span><span class="sxs-lookup"><span data-stu-id="d3eb7-164">searchText</span></span>  
<span data-ttu-id="d3eb7-165">各検索の開始位置を設定する数式 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="d3eb7-165">A numeric expression that sets the starting position for each search; optional.</span></span> <span data-ttu-id="d3eb7-166">このパラメータを省略すると、検索は、最初の文字位置から開始します。</span><span class="sxs-lookup"><span data-stu-id="d3eb7-166">If this parameter is omitted, the search starts at the first character position.</span></span>

<!-- -->

<span data-ttu-id="d3eb7-167">開始</span><span class="sxs-lookup"><span data-stu-id="d3eb7-167">start</span></span>  
<span data-ttu-id="d3eb7-168">各検索の開始位置を設定する数式 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="d3eb7-168">A numeric expression that sets the starting position for each search; optional.</span></span> <span data-ttu-id="d3eb7-169">このパラメータを省略すると、検索は、最初の文字位置から開始します。</span><span class="sxs-lookup"><span data-stu-id="d3eb7-169">If this parameter is omitted, the search starts at the first character position.</span></span>

### <a name="return-value---find"></a><span data-ttu-id="d3eb7-170">戻り値 - find</span><span class="sxs-lookup"><span data-stu-id="d3eb7-170">Return Value - find</span></span>

<span data-ttu-id="d3eb7-171">searchText が見つかった場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="d3eb7-171">true if searchText is found; otherwise, false.</span></span>

### <a name="remarks---find"></a><span data-ttu-id="d3eb7-172">備考 - find</span><span class="sxs-lookup"><span data-stu-id="d3eb7-172">Remarks - find</span></span>

<span data-ttu-id="d3eb7-173">このメソッドは、正規表現を使用して、大文字と小文字を区別しないテキスト比較を実行します。</span><span class="sxs-lookup"><span data-stu-id="d3eb7-173">This method performs a textual, case-insensitive comparison by using regular expressions.</span></span> <span data-ttu-id="d3eb7-174">詳細については、「一致する機能」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="d3eb7-174">For more information, see the match function.</span></span> <span data-ttu-id="d3eb7-175">大文字と小文字を区別しないようにするには、ignoreCase メソッドを使用します。</span><span class="sxs-lookup"><span data-stu-id="d3eb7-175">Case-insensitivity can be turned off by using the ignoreCase method.</span></span> <span data-ttu-id="d3eb7-176">正規表現は、regularExpressions メソッドを使用してオフにすることができます。</span><span class="sxs-lookup"><span data-stu-id="d3eb7-176">Regular expressions can be turned off by using the regularExpressions method.</span></span>

### <a name="examples---find"></a><span data-ttu-id="d3eb7-177">例 - find</span><span class="sxs-lookup"><span data-stu-id="d3eb7-177">Examples - find</span></span>

<span data-ttu-id="d3eb7-178">次の例では、指定した文字列の発生のすべてについて TextBuffer オブジェクトを検索し、一致が検出された位置を出力します。</span><span class="sxs-lookup"><span data-stu-id="d3eb7-178">The following example searches the TextBuffer object for all occurrences of a specified string and prints the position at which the match is found.</span></span>

```xpp
int pos; 
TextBuffer textBuffer; 
textBuffer = new TextBuffer(); 
textBuffer.setText("ABC DEF GHI JKL MNO ABC ABC"); 
pos = 0; 
while (textBuffer.find("ABC",pos)) 
{ 
    print "String found at position: ", textBuffer.matchPos(); 
    pause; 
    pos = textBuffer.matchPos()+1; 
}
```

## <a name="method-fromclipboard"></a><span data-ttu-id="d3eb7-179">メソッド fromClipboard</span><span class="sxs-lookup"><span data-stu-id="d3eb7-179">Method fromClipboard</span></span>

<span data-ttu-id="d3eb7-180">TextBuffer オブジェクトの内容をクリップボードの内容に置き換えます。</span><span class="sxs-lookup"><span data-stu-id="d3eb7-180">Replaces the content of the TextBuffer object with the content of the clipboard.</span></span>

```xpp
public boolean fromClipboard()
```

### <a name="return-value---fromclipboard"></a><span data-ttu-id="d3eb7-181">戻り値 - fromClipboard</span><span class="sxs-lookup"><span data-stu-id="d3eb7-181">Return Value - fromClipboard</span></span>

<span data-ttu-id="d3eb7-182">置換が成功した場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="d3eb7-182">true if the replacement was successful; otherwise, false.</span></span>

### <a name="examples---fromclipboard"></a><span data-ttu-id="d3eb7-183">例 - fromClipboard</span><span class="sxs-lookup"><span data-stu-id="d3eb7-183">Examples - fromClipboard</span></span>

```xpp
{ 
    TextBuffer txtb = new textBuffer(); 
    FileIoPermission perm; 
    #define.ExampleFile(@"c:\test.txt") 
    #define.ExampleOpenMode("w") 
    // Set code access permission to help protect the use of 
    // TextBuffer.tofile 
    perm = new FileIoPermission(#ExampleFile, #ExampleOpenMode); 
    perm.assert(); 
    if ( txtb.fromClipboard() ) 
    { 
        // Got text from clipboard - save it to file 
        txtb.toFile(#ExampleFile); 
    } 
    // Close the code access permission scope. 
    CodeAccessPermission::revertAssert(); 
}
```

## <a name="method-fromfile"></a><span data-ttu-id="d3eb7-184">メソッド fromFile</span><span class="sxs-lookup"><span data-stu-id="d3eb7-184">Method fromFile</span></span>

<span data-ttu-id="d3eb7-185">TextBuffer オブジェクトの内容を指定したファイルの内容に置き換えます。</span><span class="sxs-lookup"><span data-stu-id="d3eb7-185">Replaces the content of a TextBuffer object with the content of the specified file.</span></span>

```xpp
public boolean fromFile(str filename, [int encoding])
```

### <a name="parameters---fromfile"></a><span data-ttu-id="d3eb7-186">パラメーター - fromFile</span><span class="sxs-lookup"><span data-stu-id="d3eb7-186">Parameters - fromFile</span></span>

<span data-ttu-id="d3eb7-187">filename</span><span class="sxs-lookup"><span data-stu-id="d3eb7-187">filename</span></span>  
<span data-ttu-id="d3eb7-188">エンコードに使用できるオプション (オプション)。</span><span class="sxs-lookup"><span data-stu-id="d3eb7-188">The encoding option to use; optional.</span></span>

<!-- -->

<span data-ttu-id="d3eb7-189">encoding</span><span class="sxs-lookup"><span data-stu-id="d3eb7-189">encoding</span></span>  
<span data-ttu-id="d3eb7-190">エンコードに使用できるオプション (オプション)。</span><span class="sxs-lookup"><span data-stu-id="d3eb7-190">The encoding option to use; optional.</span></span>

### <a name="return-value---fromfile"></a><span data-ttu-id="d3eb7-191">戻り値 - fromFile</span><span class="sxs-lookup"><span data-stu-id="d3eb7-191">Return Value - fromFile</span></span>

<span data-ttu-id="d3eb7-192">フィールド操作が成功した場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="d3eb7-192">true if the file operation was successful; otherwise, false.</span></span>

### <a name="remarks---fromfile"></a><span data-ttu-id="d3eb7-193">備考 - fromFile</span><span class="sxs-lookup"><span data-stu-id="d3eb7-193">Remarks - fromFile</span></span>

<span data-ttu-id="d3eb7-194">FileEncoding システム列挙によって提供されるエンコーディング パラメーターの可能な値は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="d3eb7-194">The following are possible values for the encoding parameter that are supplied by the FileEncoding system enumeration:</span></span>

-   <span data-ttu-id="d3eb7-195">ACP</span><span class="sxs-lookup"><span data-stu-id="d3eb7-195">ACP</span></span>
-   <span data-ttu-id="d3eb7-196">UTF8</span><span class="sxs-lookup"><span data-stu-id="d3eb7-196">UTF8</span></span>
-   <span data-ttu-id="d3eb7-197">UTF16BE</span><span class="sxs-lookup"><span data-stu-id="d3eb7-197">UTF16BE</span></span>
-   <span data-ttu-id="d3eb7-198">UTF16LE</span><span class="sxs-lookup"><span data-stu-id="d3eb7-198">UTF16LE</span></span>
-   <span data-ttu-id="d3eb7-199">GB18030</span><span class="sxs-lookup"><span data-stu-id="d3eb7-199">GB18030</span></span>
-   <span data-ttu-id="d3eb7-200">AUTO</span><span class="sxs-lookup"><span data-stu-id="d3eb7-200">AUTO</span></span>

<span data-ttu-id="d3eb7-201">ファイルの操作に失敗した場合、TextBuffer オブジェクトは変更されません。</span><span class="sxs-lookup"><span data-stu-id="d3eb7-201">If the file operation is unsuccessful, the TextBuffer object remains unchanged.</span></span> <span data-ttu-id="d3eb7-202">攻撃者が fromFile メソッドへの入力を制御できる場合、セキュリティ上のリスクが存在します。</span><span class="sxs-lookup"><span data-stu-id="d3eb7-202">If an attacker can control input to the fromFile method, a security risk exists.</span></span> <span data-ttu-id="d3eb7-203">したがって、このメソッドは、コード アクセス セキュリティで実行されます。</span><span class="sxs-lookup"><span data-stu-id="d3eb7-203">Therefore, this method runs under Code Access Security.</span></span> <span data-ttu-id="d3eb7-204">サーバー上でこのメソッドを呼び出すには、ExecutePermission クラスからのアクセス許可が必要です。</span><span class="sxs-lookup"><span data-stu-id="d3eb7-204">Calls to this method on the server require permission from the ExecutePermission class.</span></span> <span data-ttu-id="d3eb7-205">ユーザーがこのメソッドを呼び出すコントロールで、SysDevelopment へのセキュリティ キーを設定して開発権限を持っていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="d3eb7-205">Make sure that the user has development privileges by setting the security key to SysDevelopment on the control that calls this method.</span></span>

## <a name="method-gettext"></a><span data-ttu-id="d3eb7-206">メソッド getText</span><span class="sxs-lookup"><span data-stu-id="d3eb7-206">Method getText</span></span>

<span data-ttu-id="d3eb7-207">TextBuffer オブジェクトの現在の内容を取得します。</span><span class="sxs-lookup"><span data-stu-id="d3eb7-207">Retrieves the current content of the TextBuffer object.</span></span>

```xpp
public str getText()
```

### <a name="return-value---gettext"></a><span data-ttu-id="d3eb7-208">戻り値 - getText</span><span class="sxs-lookup"><span data-stu-id="d3eb7-208">Return Value - getText</span></span>

<span data-ttu-id="d3eb7-209">TextBuffer オブジェクトのコンテンツを含む文字列。</span><span class="sxs-lookup"><span data-stu-id="d3eb7-209">A string that contains the content of TextBuffer object.</span></span>

### <a name="remarks---gettext"></a><span data-ttu-id="d3eb7-210">備考 - getText</span><span class="sxs-lookup"><span data-stu-id="d3eb7-210">Remarks - getText</span></span>

<span data-ttu-id="d3eb7-211">TextBuffer は、新しい明細行を含むことができ、これが、返される文字列に含まれます。</span><span class="sxs-lookup"><span data-stu-id="d3eb7-211">The TextBuffer can contain new lines, which are then present in the returned string.</span></span>

## <a name="method-getvalue"></a><span data-ttu-id="d3eb7-212">メソッド getValue</span><span class="sxs-lookup"><span data-stu-id="d3eb7-212">Method getValue</span></span>

```xpp
public int getValue()
```

### <a name="return-value---getvalue"></a><span data-ttu-id="d3eb7-213">戻り値 - getValue</span><span class="sxs-lookup"><span data-stu-id="d3eb7-213">Return Value - getValue</span></span>

## <a name="method-ignorecase"></a><span data-ttu-id="d3eb7-214">メソッド ignoreCase</span><span class="sxs-lookup"><span data-stu-id="d3eb7-214">Method ignoreCase</span></span>

```xpp
public boolean ignoreCase([boolean ignoreCase])
```

### <a name="parameters---ignorecase"></a><span data-ttu-id="d3eb7-215">パラメーター - ignoreCase</span><span class="sxs-lookup"><span data-stu-id="d3eb7-215">Parameters - ignoreCase</span></span>

<span data-ttu-id="d3eb7-216">ignoreCase</span><span class="sxs-lookup"><span data-stu-id="d3eb7-216">ignoreCase</span></span>  

### <a name="return-value---ignorecase"></a><span data-ttu-id="d3eb7-217">戻り値 - ignoreCase</span><span class="sxs-lookup"><span data-stu-id="d3eb7-217">Return Value - ignoreCase</span></span>

## <a name="method-isnext"></a><span data-ttu-id="d3eb7-218">メソッド isNext</span><span class="sxs-lookup"><span data-stu-id="d3eb7-218">Method isNext</span></span>

```xpp
public boolean isNext(str searchText)
```

### <a name="parameters---isnext"></a><span data-ttu-id="d3eb7-219">パラメーター - isNext</span><span class="sxs-lookup"><span data-stu-id="d3eb7-219">Parameters - isNext</span></span>

<span data-ttu-id="d3eb7-220">searchText</span><span class="sxs-lookup"><span data-stu-id="d3eb7-220">searchText</span></span>  

### <a name="return-value---isnext"></a><span data-ttu-id="d3eb7-221">戻り値 - isNext</span><span class="sxs-lookup"><span data-stu-id="d3eb7-221">Return Value - isNext</span></span>

## <a name="method-matchlen"></a><span data-ttu-id="d3eb7-222">メソッド matchLen</span><span class="sxs-lookup"><span data-stu-id="d3eb7-222">Method matchLen</span></span>

<span data-ttu-id="d3eb7-223">TextBuffer オブジェクトで最初に一致する文字列の長さを返します。</span><span class="sxs-lookup"><span data-stu-id="d3eb7-223">Returns the string length of the first match in the TextBuffer object.</span></span>

```xpp
public int matchLen()
```

### <a name="return-value---matchlen"></a><span data-ttu-id="d3eb7-224">戻り値 - matchLen</span><span class="sxs-lookup"><span data-stu-id="d3eb7-224">Return Value - matchLen</span></span>

<span data-ttu-id="d3eb7-225">見つかった一致の長さ。一致するものが見つからない場合は 0 (ゼロ)。</span><span class="sxs-lookup"><span data-stu-id="d3eb7-225">The length of the match that is found; 0 (zero) if no match is found.</span></span>

### <a name="remarks---matchlen"></a><span data-ttu-id="d3eb7-226">備考 - matchLen</span><span class="sxs-lookup"><span data-stu-id="d3eb7-226">Remarks - matchLen</span></span>

<span data-ttu-id="d3eb7-227">このメソッドは、テキスト検索の一部として使用されます (find メソッドを参照)。</span><span class="sxs-lookup"><span data-stu-id="d3eb7-227">This method is used as part of a text search (see the find method).</span></span>

## <a name="method-matchpos"></a><span data-ttu-id="d3eb7-228">メソッド matchPos</span><span class="sxs-lookup"><span data-stu-id="d3eb7-228">Method matchPos</span></span>

<span data-ttu-id="d3eb7-229">TextBuffer オブジェクトの検索文字列の 1 番目の文字の位置を返します。</span><span class="sxs-lookup"><span data-stu-id="d3eb7-229">Returns the character position of the first occurrence of the search string in the TextBuffer object.</span></span>

```xpp
public int matchPos()
```

### <a name="return-value---matchpos"></a><span data-ttu-id="d3eb7-230">戻り値 - matchPos</span><span class="sxs-lookup"><span data-stu-id="d3eb7-230">Return Value - matchPos</span></span>

<span data-ttu-id="d3eb7-231">一致が見つかった位置。一致しない場合は 0 (ゼロ)。</span><span class="sxs-lookup"><span data-stu-id="d3eb7-231">The position at which the match is found; 0 (zero) if no match is found.</span></span>

### <a name="remarks---matchpos"></a><span data-ttu-id="d3eb7-232">備考 - matchPos</span><span class="sxs-lookup"><span data-stu-id="d3eb7-232">Remarks - matchPos</span></span>

<span data-ttu-id="d3eb7-233">このメソッドは、テキスト検索の一部として使用されます (find メソッドを参照)。</span><span class="sxs-lookup"><span data-stu-id="d3eb7-233">This method is used as part of a text search (see the find method).</span></span>

## <a name="method-nexttoken"></a><span data-ttu-id="d3eb7-234">メソッド nextToken</span><span class="sxs-lookup"><span data-stu-id="d3eb7-234">Method nextToken</span></span>

```xpp
public str nextToken([boolean includeWholeLine], [str stopAtChar])
```

### <a name="parameters---nexttoken"></a><span data-ttu-id="d3eb7-235">パラメーター - nextToken</span><span class="sxs-lookup"><span data-stu-id="d3eb7-235">Parameters - nextToken</span></span>

<span data-ttu-id="d3eb7-236">includeWholeLine</span><span class="sxs-lookup"><span data-stu-id="d3eb7-236">includeWholeLine</span></span>  

<!-- -->

<span data-ttu-id="d3eb7-237">stopAtChar</span><span class="sxs-lookup"><span data-stu-id="d3eb7-237">stopAtChar</span></span>  

### <a name="return-value---nexttoken"></a><span data-ttu-id="d3eb7-238">戻り値 - nextToken</span><span class="sxs-lookup"><span data-stu-id="d3eb7-238">Return Value - nextToken</span></span>

## <a name="method-numlines"></a><span data-ttu-id="d3eb7-239">メソッド numLines</span><span class="sxs-lookup"><span data-stu-id="d3eb7-239">Method numLines</span></span>

<span data-ttu-id="d3eb7-240">TextBuffer オブジェクトの明細行の数を取得します。</span><span class="sxs-lookup"><span data-stu-id="d3eb7-240">Retrieves the number of lines in the TextBuffer object.</span></span>

```xpp
public int numLines()
```

### <a name="return-value---numlines"></a><span data-ttu-id="d3eb7-241">戻り値 - numLines</span><span class="sxs-lookup"><span data-stu-id="d3eb7-241">Return Value - numLines</span></span>

<span data-ttu-id="d3eb7-242">コンテンツ内の行数。</span><span class="sxs-lookup"><span data-stu-id="d3eb7-242">The number of lines in the content.</span></span>

### <a name="remarks---numlines"></a><span data-ttu-id="d3eb7-243">備考 - numLines</span><span class="sxs-lookup"><span data-stu-id="d3eb7-243">Remarks - numLines</span></span>

<span data-ttu-id="d3eb7-244">行は改行 ('\\n') で区切られます。</span><span class="sxs-lookup"><span data-stu-id="d3eb7-244">Lines are separated by newlines ('\\n').</span></span>

### <a name="examples---numlines"></a><span data-ttu-id="d3eb7-245">例 - numLines</span><span class="sxs-lookup"><span data-stu-id="d3eb7-245">Examples - numLines</span></span>

```xpp
{ 
    TextBuffer txtb = new TextBuffer(); 
    if (txtb.fromClipboard()) 
    { 
        print "Clipboard contains ",txtb.numLines()," lines."; 
    } 
}
```

## <a name="method-regularexpressions"></a><span data-ttu-id="d3eb7-246">メソッド regularExpressions</span><span class="sxs-lookup"><span data-stu-id="d3eb7-246">Method regularExpressions</span></span>

```xpp
public boolean regularExpressions([boolean useRegularExpressions])
```

### <a name="parameters---regularexpressions"></a><span data-ttu-id="d3eb7-247">パラメーター - regularExpressions</span><span class="sxs-lookup"><span data-stu-id="d3eb7-247">Parameters - regularExpressions</span></span>

<span data-ttu-id="d3eb7-248">useRegularExpressions</span><span class="sxs-lookup"><span data-stu-id="d3eb7-248">useRegularExpressions</span></span>  

### <a name="return-value---regularexpressions"></a><span data-ttu-id="d3eb7-249">戻り値 - regularExpressions</span><span class="sxs-lookup"><span data-stu-id="d3eb7-249">Return Value - regularExpressions</span></span>

## <a name="method-size"></a><span data-ttu-id="d3eb7-250">メソッド size</span><span class="sxs-lookup"><span data-stu-id="d3eb7-250">Method size</span></span>

```xpp
public int size()
```

### <a name="return-value---size"></a><span data-ttu-id="d3eb7-251">戻り値 - size</span><span class="sxs-lookup"><span data-stu-id="d3eb7-251">Return Value - size</span></span>

## <a name="method-substr"></a><span data-ttu-id="d3eb7-252">メソッド subStr</span><span class="sxs-lookup"><span data-stu-id="d3eb7-252">Method subStr</span></span>

<span data-ttu-id="d3eb7-253">TextBuffer オブジェクト (サブ文字列) の内容の一部を取得します。</span><span class="sxs-lookup"><span data-stu-id="d3eb7-253">Retrieves part of the content of the TextBuffer object (a substring).</span></span>

```xpp
public str subStr(int start, int length)
```

### <a name="parameters---substr"></a><span data-ttu-id="d3eb7-254">パラメーター - subStr</span><span class="sxs-lookup"><span data-stu-id="d3eb7-254">Parameters - subStr</span></span>

<span data-ttu-id="d3eb7-255">開始</span><span class="sxs-lookup"><span data-stu-id="d3eb7-255">start</span></span>  
<span data-ttu-id="d3eb7-256">目的のサブ文字列の長さ。</span><span class="sxs-lookup"><span data-stu-id="d3eb7-256">The length of the desired substring.</span></span>

<!-- -->

<span data-ttu-id="d3eb7-257">length</span><span class="sxs-lookup"><span data-stu-id="d3eb7-257">length</span></span>  
<span data-ttu-id="d3eb7-258">目的のサブ文字列の長さ。</span><span class="sxs-lookup"><span data-stu-id="d3eb7-258">The length of the desired substring.</span></span>

### <a name="return-value---substr"></a><span data-ttu-id="d3eb7-259">戻り値 - subStr</span><span class="sxs-lookup"><span data-stu-id="d3eb7-259">Return Value - subStr</span></span>

<span data-ttu-id="d3eb7-260">TextBuffer オブジェクト コンテンツの指定された部分を含む文字列。</span><span class="sxs-lookup"><span data-stu-id="d3eb7-260">A string that contains the specified part of the TextBuffer object content.</span></span>

### <a name="remarks---substr"></a><span data-ttu-id="d3eb7-261">備考 - subStr</span><span class="sxs-lookup"><span data-stu-id="d3eb7-261">Remarks - subStr</span></span>

<span data-ttu-id="d3eb7-262">部分文字列の開始位置を指定するときは、コンテンツの最初の文字に 1 を、2 番目の文字に 2 というように使用します。</span><span class="sxs-lookup"><span data-stu-id="d3eb7-262">When you specify the start position for substring, use 1 for the first character in the content, 2 for the second character, and so on.</span></span>

### <a name="examples---substr"></a><span data-ttu-id="d3eb7-263">例 - subStr</span><span class="sxs-lookup"><span data-stu-id="d3eb7-263">Examples - subStr</span></span>

```xpp
{ 
    TextBuffer txtb = new TextBuffer(); 
    str mystr; 
    if (txtb.fromClipboard()) 
    { 
        mystr = txtb.subStr(10,15);  
        // 15 long substring starting at position 10. 
    } 
}
```

## <a name="method-tofile"></a><span data-ttu-id="d3eb7-264">メソッド toFile</span><span class="sxs-lookup"><span data-stu-id="d3eb7-264">Method toFile</span></span>

<span data-ttu-id="d3eb7-265">TextBuffer オブジェクトの内容をファイルに保存します。</span><span class="sxs-lookup"><span data-stu-id="d3eb7-265">Saves the content of the TextBuffer object to a file.</span></span>

```xpp
public boolean toFile(str filename, [int encoding])
```

### <a name="parameters---tofile"></a><span data-ttu-id="d3eb7-266">パラメーター - toFile</span><span class="sxs-lookup"><span data-stu-id="d3eb7-266">Parameters - toFile</span></span>

<span data-ttu-id="d3eb7-267">filename</span><span class="sxs-lookup"><span data-stu-id="d3eb7-267">filename</span></span>  

<!-- -->

<span data-ttu-id="d3eb7-268">encoding</span><span class="sxs-lookup"><span data-stu-id="d3eb7-268">encoding</span></span>  

### <a name="return-value---tofile"></a><span data-ttu-id="d3eb7-269">戻り値 - toFile</span><span class="sxs-lookup"><span data-stu-id="d3eb7-269">Return Value - toFile</span></span>

<span data-ttu-id="d3eb7-270">操作が成功する場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="d3eb7-270">true if the operation is successful; otherwise, false.</span></span>

### <a name="remarks---tofile"></a><span data-ttu-id="d3eb7-271">備考 - toFile</span><span class="sxs-lookup"><span data-stu-id="d3eb7-271">Remarks - toFile</span></span>

<span data-ttu-id="d3eb7-272">指定したファイルが既に存在する場合は、確認なしで上書きされます。</span><span class="sxs-lookup"><span data-stu-id="d3eb7-272">If the specified file already exists, it is overwritten without confirmation.</span></span> <span data-ttu-id="d3eb7-273">攻撃者が toFile メソッドへの入力を制御できる場合、セキュリティ上のリスクが存在します。</span><span class="sxs-lookup"><span data-stu-id="d3eb7-273">If an attacker can control input to the toFile method, a security risk exists.</span></span> <span data-ttu-id="d3eb7-274">したがって、このメソッドは、コード アクセス セキュリティで実行されます。</span><span class="sxs-lookup"><span data-stu-id="d3eb7-274">Therefore, this method runs under Code Access Security.</span></span> <span data-ttu-id="d3eb7-275">サーバー上でこのメソッドを呼び出すには、ExecutePermission クラスからのアクセス許可が必要です。</span><span class="sxs-lookup"><span data-stu-id="d3eb7-275">Calls to this method on the server require permission from the ExecutePermission class.</span></span> <span data-ttu-id="d3eb7-276">ユーザーがこのメソッドを呼び出すコントロールで、SysDevelopment へのセキュリティ キーを設定して開発権限を持っていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="d3eb7-276">Make sure that the user has development privileges by setting the security key to SysDevelopment on the control that calls this method.</span></span>

## <a name="method-token"></a><span data-ttu-id="d3eb7-277">メソッド token</span><span class="sxs-lookup"><span data-stu-id="d3eb7-277">Method token</span></span>

```xpp
public str token()
```

### <a name="return-value---token"></a><span data-ttu-id="d3eb7-278">戻り値 - token</span><span class="sxs-lookup"><span data-stu-id="d3eb7-278">Return Value - token</span></span>

## <a name="method-tostring"></a><span data-ttu-id="d3eb7-279">メソッド toString</span><span class="sxs-lookup"><span data-stu-id="d3eb7-279">Method toString</span></span>

<span data-ttu-id="d3eb7-280">現在のオブジェクトを表す文字列を返します。</span><span class="sxs-lookup"><span data-stu-id="d3eb7-280">Returns a string that represents the current object.</span></span>

```xpp
public str toString()
```

### <a name="return-value---tostring"></a><span data-ttu-id="d3eb7-281">戻り値 - toString</span><span class="sxs-lookup"><span data-stu-id="d3eb7-281">Return Value - toString</span></span>

<span data-ttu-id="d3eb7-282">現在のオブジェクトを表す文字列。</span><span class="sxs-lookup"><span data-stu-id="d3eb7-282">A string that represents the current object.</span></span>

### <a name="remarks---tostring"></a><span data-ttu-id="d3eb7-283">備考 - toString</span><span class="sxs-lookup"><span data-stu-id="d3eb7-283">Remarks - toString</span></span>

<span data-ttu-id="d3eb7-284">既定の実装は、オブジェクトのクラス名を返します。</span><span class="sxs-lookup"><span data-stu-id="d3eb7-284">The default implementation returns the class name of the object.</span></span> <span data-ttu-id="d3eb7-285">メソッドは派生クラスで上書きできるため、そのタイプの意味のある値が返されます。</span><span class="sxs-lookup"><span data-stu-id="d3eb7-285">The method can be overridden in a derived class so that it returns values that are meaningful for that type.</span></span> <span data-ttu-id="d3eb7-286">たとえば、SysMethodInfo クラスのインスタンスは、インスタンスまたは静的などのメソッド名およびメソッドのタイプを返します。</span><span class="sxs-lookup"><span data-stu-id="d3eb7-286">For example, an instance of the SysMethodInfo class returns the method name and type of the method, such as instance or static.</span></span>

## <a name="method-strhashkey"></a><span data-ttu-id="d3eb7-287">メソッド strHashKey</span><span class="sxs-lookup"><span data-stu-id="d3eb7-287">Method strHashKey</span></span>

```xpp
public static int strHashKey(str sourceString)
```

### <a name="parameters---strhashkey"></a><span data-ttu-id="d3eb7-288">パラメーター - strHashKey</span><span class="sxs-lookup"><span data-stu-id="d3eb7-288">Parameters - strHashKey</span></span>

<span data-ttu-id="d3eb7-289">sourceString</span><span class="sxs-lookup"><span data-stu-id="d3eb7-289">sourceString</span></span>  

### <a name="return-value---strhashkey"></a><span data-ttu-id="d3eb7-290">戻り値 - strHashKey</span><span class="sxs-lookup"><span data-stu-id="d3eb7-290">Return Value - strHashKey</span></span>

## <a name="method-new"></a><span data-ttu-id="d3eb7-291">メソッド new</span><span class="sxs-lookup"><span data-stu-id="d3eb7-291">Method new</span></span>

<span data-ttu-id="d3eb7-292">TextBuffer クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="d3eb7-292">Initializes a new instance of the TextBuffer class.</span></span>

```xpp
public void new()
```

## <a name="method-removechar"></a><span data-ttu-id="d3eb7-293">メソッド removeChar</span><span class="sxs-lookup"><span data-stu-id="d3eb7-293">Method removeChar</span></span>

```xpp
public void removeChar(str charList)
```

### <a name="parameters---removechar"></a><span data-ttu-id="d3eb7-294">パラメーター - removeChar</span><span class="sxs-lookup"><span data-stu-id="d3eb7-294">Parameters - removeChar</span></span>

<span data-ttu-id="d3eb7-295">charList</span><span class="sxs-lookup"><span data-stu-id="d3eb7-295">charList</span></span>  

## <a name="method-toclipboard"></a><span data-ttu-id="d3eb7-296">メソッド toClipboard</span><span class="sxs-lookup"><span data-stu-id="d3eb7-296">Method toClipboard</span></span>

<span data-ttu-id="d3eb7-297">TextBuffer オブジェクトの内容をクリップボードにコピーします。</span><span class="sxs-lookup"><span data-stu-id="d3eb7-297">Copies the content of a TextBuffer object to the clipboard.</span></span>

```xpp
public void toClipboard()
```

## <a name="method-insert"></a><span data-ttu-id="d3eb7-298">メソッド insert</span><span class="sxs-lookup"><span data-stu-id="d3eb7-298">Method insert</span></span>

```xpp
public void insert(str insertString, int position)
```

### <a name="parameters---insert"></a><span data-ttu-id="d3eb7-299">パラメーター - insert</span><span class="sxs-lookup"><span data-stu-id="d3eb7-299">Parameters - insert</span></span>

<span data-ttu-id="d3eb7-300">insertString</span><span class="sxs-lookup"><span data-stu-id="d3eb7-300">insertString</span></span>  

<!-- -->

<span data-ttu-id="d3eb7-301">職位</span><span class="sxs-lookup"><span data-stu-id="d3eb7-301">position</span></span>  

## <a name="method-settext"></a><span data-ttu-id="d3eb7-302">メソッド setText</span><span class="sxs-lookup"><span data-stu-id="d3eb7-302">Method setText</span></span>

<span data-ttu-id="d3eb7-303">既存の内容を上書きして、指定した文字列に TextBuffer オブジェクトの内容を設定します。</span><span class="sxs-lookup"><span data-stu-id="d3eb7-303">Sets the content of the TextBuffer object to the specified string, overwriting any existing content.</span></span>

```xpp
public void setText(str string)
```

### <a name="parameters---settext"></a><span data-ttu-id="d3eb7-304">パラメーター - setText</span><span class="sxs-lookup"><span data-stu-id="d3eb7-304">Parameters - setText</span></span>

<span data-ttu-id="d3eb7-305">文字列</span><span class="sxs-lookup"><span data-stu-id="d3eb7-305">string</span></span>  
<span data-ttu-id="d3eb7-306">TextBuffer オブジェクトの新しいテキストを含む文字列。</span><span class="sxs-lookup"><span data-stu-id="d3eb7-306">A string that contains the new text for the TextBuffer object.</span></span>

### <a name="remarks---settext"></a><span data-ttu-id="d3eb7-307">備考 - setText</span><span class="sxs-lookup"><span data-stu-id="d3eb7-307">Remarks - setText</span></span>

<span data-ttu-id="d3eb7-308">TextBuffer オブジェクトに任意のコンテンツが含まれている場合は、新しいコンテンツで上書きされます。</span><span class="sxs-lookup"><span data-stu-id="d3eb7-308">If the TextBuffer object contains any content, it is overwritten by the new content.</span></span>

### <a name="examples---settext"></a><span data-ttu-id="d3eb7-309">例 - setText</span><span class="sxs-lookup"><span data-stu-id="d3eb7-309">Examples - setText</span></span>

```xpp
{ 
    TextBuffer txtb = new TextBuffer(); 
    txtb.setText("This is the first text."); 
    // Now txtb contains exactly that text. 
}
```

## <a name="method-appendtext"></a><span data-ttu-id="d3eb7-310">メソッド appendText</span><span class="sxs-lookup"><span data-stu-id="d3eb7-310">Method appendText</span></span>

<span data-ttu-id="d3eb7-311">TextBuffer オブジェクトの内容に文字列を追加します。</span><span class="sxs-lookup"><span data-stu-id="d3eb7-311">Appends a string to the content of the TextBuffer object.</span></span>

```xpp
public void appendText(str string)
```

### <a name="parameters---appendtext"></a><span data-ttu-id="d3eb7-312">パラメーター - appendText</span><span class="sxs-lookup"><span data-stu-id="d3eb7-312">Parameters - appendText</span></span>

<span data-ttu-id="d3eb7-313">文字列</span><span class="sxs-lookup"><span data-stu-id="d3eb7-313">string</span></span>  
<span data-ttu-id="d3eb7-314">追加する文字列。</span><span class="sxs-lookup"><span data-stu-id="d3eb7-314">The string to append.</span></span>

### <a name="examples---appendtext"></a><span data-ttu-id="d3eb7-315">例 - appendText</span><span class="sxs-lookup"><span data-stu-id="d3eb7-315">Examples - appendText</span></span>

```xpp
{ 
    TextBuffer txtb = new TextBuffer(); 
    txtb.setText("[One]"); 
    txtb.appendText("[Another]"); 
    print txtb.getText(); // Will print "[One][Another]" 
}
```

## <a name="method-replace"></a><span data-ttu-id="d3eb7-316">メソッド replace</span><span class="sxs-lookup"><span data-stu-id="d3eb7-316">Method replace</span></span>

```xpp
public void replace(str findString, str replaceString)
```

### <a name="parameters---replace"></a><span data-ttu-id="d3eb7-317">パラメーター - replace</span><span class="sxs-lookup"><span data-stu-id="d3eb7-317">Parameters - replace</span></span>

<span data-ttu-id="d3eb7-318">findString</span><span class="sxs-lookup"><span data-stu-id="d3eb7-318">findString</span></span>  

<!-- -->

<span data-ttu-id="d3eb7-319">replaceString</span><span class="sxs-lookup"><span data-stu-id="d3eb7-319">replaceString</span></span>  

## <a name="method-delete"></a><span data-ttu-id="d3eb7-320">メソッド delete</span><span class="sxs-lookup"><span data-stu-id="d3eb7-320">Method delete</span></span>

```xpp
public void delete(int start, int length)
```

### <a name="parameters---delete"></a><span data-ttu-id="d3eb7-321">パラメーター - delete</span><span class="sxs-lookup"><span data-stu-id="d3eb7-321">Parameters - delete</span></span>

<span data-ttu-id="d3eb7-322">開始</span><span class="sxs-lookup"><span data-stu-id="d3eb7-322">start</span></span>  

<!-- -->

<span data-ttu-id="d3eb7-323">length</span><span class="sxs-lookup"><span data-stu-id="d3eb7-323">length</span></span>  

