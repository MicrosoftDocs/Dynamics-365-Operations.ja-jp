---
title: T クラス
description: 文字 T で始まるシステム API クラス。
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
ms.custom: 51774
ms.assetid: c83d7228-86a5-404b-a978-7f6d316b7b7e
ms.search.region: Global
ms.author: rhaertle
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6779bd6a7cac3d7989543f53a3fb11483da5e261
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/27/2019
ms.locfileid: "2191607"
---
# <a name="t-classes"></a><span data-ttu-id="553d4-103">T クラス</span><span class="sxs-lookup"><span data-stu-id="553d4-103">T classes</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="553d4-104">文字 T で始まるシステム API クラス。</span><span class="sxs-lookup"><span data-stu-id="553d4-104">System API classes that start with the letter T.</span></span>

<a name="class-tableextension"></a><span data-ttu-id="553d4-105">クラス TableExtension</span><span class="sxs-lookup"><span data-stu-id="553d4-105">Class TableExtension</span></span>
--------------------

    class TableExtension extends Object

### <a name="remarks"></a><span data-ttu-id="553d4-106">備考</span><span class="sxs-lookup"><span data-stu-id="553d4-106">Remarks</span></span>

### <a name="examples"></a><span data-ttu-id="553d4-107">例</span><span class="sxs-lookup"><span data-stu-id="553d4-107">Examples</span></span>

### <a name="methods"></a><span data-ttu-id="553d4-108">メソッド</span><span class="sxs-lookup"><span data-stu-id="553d4-108">Methods</span></span>

| <span data-ttu-id="553d4-109">方法</span><span class="sxs-lookup"><span data-stu-id="553d4-109">Method</span></span>                                                    | <span data-ttu-id="553d4-110">説明</span><span class="sxs-lookup"><span data-stu-id="553d4-110">Description</span></span>                                             |
|-----------------------------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="553d4-111">public void new()</span><span class="sxs-lookup"><span data-stu-id="553d4-111">public void new()</span></span>                                         | <span data-ttu-id="553d4-112">TableExtension クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="553d4-112">Initializes a new instance of the TableExtension class.</span></span> |
| <span data-ttu-id="553d4-113">public void modifiedField(Common record, FieldId fieldId)</span><span class="sxs-lookup"><span data-stu-id="553d4-113">public void modifiedField(Common record, FieldId fieldId)</span></span> |                                                         |
| <span data-ttu-id="553d4-114">public void defaultRow(Common record)</span><span class="sxs-lookup"><span data-stu-id="553d4-114">public void defaultRow(Common record)</span></span>                     |                                                         |
| <span data-ttu-id="553d4-115">public void defaultField(Common record, FieldId fieldId)</span><span class="sxs-lookup"><span data-stu-id="553d4-115">public void defaultField(Common record, FieldId fieldId)</span></span>  |                                                         |

### <a name="method-new"></a><span data-ttu-id="553d4-116">メソッド new</span><span class="sxs-lookup"><span data-stu-id="553d4-116">Method new</span></span>

<span data-ttu-id="553d4-117">TableExtension クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="553d4-117">Initializes a new instance of the TableExtension class.</span></span>

    public void new()

### <a name="method-modifiedfield"></a><span data-ttu-id="553d4-118">メソッド modifiedField</span><span class="sxs-lookup"><span data-stu-id="553d4-118">Method modifiedField</span></span>

    public void modifiedField(Common record, FieldId fieldId)

#### <a name="parameters"></a><span data-ttu-id="553d4-119">パラメーター</span><span class="sxs-lookup"><span data-stu-id="553d4-119">Parameters</span></span>

<span data-ttu-id="553d4-120">記録</span><span class="sxs-lookup"><span data-stu-id="553d4-120">record</span></span>  

<!-- -->

<span data-ttu-id="553d4-121">fieldId</span><span class="sxs-lookup"><span data-stu-id="553d4-121">fieldId</span></span>  

### <a name="method-defaultrow"></a><span data-ttu-id="553d4-122">メソッド defaultRow</span><span class="sxs-lookup"><span data-stu-id="553d4-122">Method defaultRow</span></span>

    public void defaultRow(Common record)

#### <a name="parameters"></a><span data-ttu-id="553d4-123">パラメーター</span><span class="sxs-lookup"><span data-stu-id="553d4-123">Parameters</span></span>

<span data-ttu-id="553d4-124">記録</span><span class="sxs-lookup"><span data-stu-id="553d4-124">record</span></span>  

### <a name="method-defaultfield"></a><span data-ttu-id="553d4-125">メソッド defaultField</span><span class="sxs-lookup"><span data-stu-id="553d4-125">Method defaultField</span></span>

    public void defaultField(Common record, FieldId fieldId)

#### <a name="parameters"></a><span data-ttu-id="553d4-126">パラメーター</span><span class="sxs-lookup"><span data-stu-id="553d4-126">Parameters</span></span>

<span data-ttu-id="553d4-127">記録</span><span class="sxs-lookup"><span data-stu-id="553d4-127">record</span></span>  

<!-- -->

<span data-ttu-id="553d4-128">fieldId</span><span class="sxs-lookup"><span data-stu-id="553d4-128">fieldId</span></span>  

## <a name="class-textbuffer"></a><span data-ttu-id="553d4-129">クラス TextBuffer</span><span class="sxs-lookup"><span data-stu-id="553d4-129">Class TextBuffer</span></span>
    class TextBuffer extends Object

<span data-ttu-id="553d4-130">TextBuffer クラスは、任意のテキスト ファイル内容を管理し、テキストを生成して操作します。</span><span class="sxs-lookup"><span data-stu-id="553d4-130">The TextBuffer class manages arbitrary text file content, and generates and manipulates text.</span></span>

### <a name="remarks"></a><span data-ttu-id="553d4-131">備考</span><span class="sxs-lookup"><span data-stu-id="553d4-131">Remarks</span></span>

<span data-ttu-id="553d4-132">このクラスは、さまざまな文字列操作、シンプルなクリップボード、ファイル インターフェイスを備えています。</span><span class="sxs-lookup"><span data-stu-id="553d4-132">This class features various string operations, a simple clipboard, and a file interface.</span></span>

### <a name="examples"></a><span data-ttu-id="553d4-133">例</span><span class="sxs-lookup"><span data-stu-id="553d4-133">Examples</span></span>

    static void example() 
    { 
        FileIoPermission _perm = new FileIoPermission("myfile.txt",'r'); 
        TextBuffer txtb = new TextBuffer(); 
        _perm.assert(); 
        txtb.fromFile("myfile.txt"); // Read text from file 
        txtb.toClipboard(); // Copy it to the clipboard 
    }

### <a name="methods"></a><span data-ttu-id="553d4-134">メソッド</span><span class="sxs-lookup"><span data-stu-id="553d4-134">Methods</span></span>

| <span data-ttu-id="553d4-135">方法</span><span class="sxs-lookup"><span data-stu-id="553d4-135">Method</span></span>                                                                 | <span data-ttu-id="553d4-136">説明</span><span class="sxs-lookup"><span data-stu-id="553d4-136">Description</span></span>                                                                                           |
|------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="553d4-137">public boolean accept(str searchText)</span><span class="sxs-lookup"><span data-stu-id="553d4-137">public boolean accept(str searchText)</span></span>                                  |                                                                                                       |
| <span data-ttu-id="553d4-138">public int decryptOld(int cryptKey)</span><span class="sxs-lookup"><span data-stu-id="553d4-138">public int decryptOld(int cryptKey)</span></span>                                    |                                                                                                       |
| <span data-ttu-id="553d4-139">public boolean find(str searchText, \[int start\])</span><span class="sxs-lookup"><span data-stu-id="553d4-139">public boolean find(str searchText, \[int start\])</span></span>                     | <span data-ttu-id="553d4-140">TextBuffer オブジェクトで文字列式の発生を検索します。</span><span class="sxs-lookup"><span data-stu-id="553d4-140">Searches the TextBuffer object for any occurrence of a string expression.</span></span>                             |
| <span data-ttu-id="553d4-141">public boolean fromClipboard()</span><span class="sxs-lookup"><span data-stu-id="553d4-141">public boolean fromClipboard()</span></span>                                         | <span data-ttu-id="553d4-142">TextBuffer オブジェクトの内容をクリップボードの内容に置き換えます。</span><span class="sxs-lookup"><span data-stu-id="553d4-142">Replaces the content of the TextBuffer object with the content of the clipboard.</span></span>                      |
| <span data-ttu-id="553d4-143">public boolean fromFile(str filename, \[int encoding\])</span><span class="sxs-lookup"><span data-stu-id="553d4-143">public boolean fromFile(str filename, \[int encoding\])</span></span>                | <span data-ttu-id="553d4-144">TextBuffer オブジェクトの内容を指定したファイルの内容に置き換えます。</span><span class="sxs-lookup"><span data-stu-id="553d4-144">Replaces the content of a TextBuffer object with the content of the specified file.</span></span>                   |
| <span data-ttu-id="553d4-145">public str getText()</span><span class="sxs-lookup"><span data-stu-id="553d4-145">public str getText()</span></span>                                                   | <span data-ttu-id="553d4-146">TextBuffer オブジェクトの現在の内容を取得します。</span><span class="sxs-lookup"><span data-stu-id="553d4-146">Retrieves the current content of the TextBuffer object.</span></span>                                               |
| <span data-ttu-id="553d4-147">public int getValue()</span><span class="sxs-lookup"><span data-stu-id="553d4-147">public int getValue()</span></span>                                                  |                                                                                                       |
| <span data-ttu-id="553d4-148">public boolean ignoreCase(\[boolean ignoreCase\])</span><span class="sxs-lookup"><span data-stu-id="553d4-148">public boolean ignoreCase(\[boolean ignoreCase\])</span></span>                      |                                                                                                       |
| <span data-ttu-id="553d4-149">public boolean isNext(str searchText)</span><span class="sxs-lookup"><span data-stu-id="553d4-149">public boolean isNext(str searchText)</span></span>                                  |                                                                                                       |
| <span data-ttu-id="553d4-150">public int matchLen()</span><span class="sxs-lookup"><span data-stu-id="553d4-150">public int matchLen()</span></span>                                                  | <span data-ttu-id="553d4-151">TextBuffer オブジェクトで最初に一致する文字列の長さを返します。</span><span class="sxs-lookup"><span data-stu-id="553d4-151">Returns the string length of the first match in the TextBuffer object.</span></span>                                |
| <span data-ttu-id="553d4-152">public int matchPos()</span><span class="sxs-lookup"><span data-stu-id="553d4-152">public int matchPos()</span></span>                                                  | <span data-ttu-id="553d4-153">TextBuffer オブジェクトの検索文字列の 1 番目の文字の位置を返します。</span><span class="sxs-lookup"><span data-stu-id="553d4-153">Returns the character position of the first occurrence of the search string in the TextBuffer object.</span></span> |
| <span data-ttu-id="553d4-154">public str nextToken(\[boolean includeWholeLine\], \[str stopAtChar\])</span><span class="sxs-lookup"><span data-stu-id="553d4-154">public str nextToken(\[boolean includeWholeLine\], \[str stopAtChar\])</span></span> |                                                                                                       |
| <span data-ttu-id="553d4-155">public int numLines()</span><span class="sxs-lookup"><span data-stu-id="553d4-155">public int numLines()</span></span>                                                  | <span data-ttu-id="553d4-156">TextBuffer オブジェクトの明細行の数を取得します。</span><span class="sxs-lookup"><span data-stu-id="553d4-156">Retrieves the number of lines in the TextBuffer object.</span></span>                                               |
| <span data-ttu-id="553d4-157">public boolean regularExpressions(\[boolean useRegularExpressions\])</span><span class="sxs-lookup"><span data-stu-id="553d4-157">public boolean regularExpressions(\[boolean useRegularExpressions\])</span></span>   |                                                                                                       |
| <span data-ttu-id="553d4-158">public int size()</span><span class="sxs-lookup"><span data-stu-id="553d4-158">public int size()</span></span>                                                      |                                                                                                       |
| <span data-ttu-id="553d4-159">public str subStr(int start, int length)</span><span class="sxs-lookup"><span data-stu-id="553d4-159">public str subStr(int start, int length)</span></span>                               | <span data-ttu-id="553d4-160">TextBuffer オブジェクト (サブ文字列) の内容の一部を取得します。</span><span class="sxs-lookup"><span data-stu-id="553d4-160">Retrieves part of the content of the TextBuffer object (a substring).</span></span>                                 |
| <span data-ttu-id="553d4-161">public boolean toFile(str filename, \[int encoding\])</span><span class="sxs-lookup"><span data-stu-id="553d4-161">public boolean toFile(str filename, \[int encoding\])</span></span>                  | <span data-ttu-id="553d4-162">TextBuffer オブジェクトの内容をファイルに保存します。</span><span class="sxs-lookup"><span data-stu-id="553d4-162">Saves the content of the TextBuffer object to a file.</span></span>                                                 |
| <span data-ttu-id="553d4-163">public str token()</span><span class="sxs-lookup"><span data-stu-id="553d4-163">public str token()</span></span>                                                     |                                                                                                       |
| <span data-ttu-id="553d4-164">public str toString()</span><span class="sxs-lookup"><span data-stu-id="553d4-164">public str toString()</span></span>                                                  | <span data-ttu-id="553d4-165">現在のオブジェクトを表す文字列を返します。</span><span class="sxs-lookup"><span data-stu-id="553d4-165">Returns a string that represents the current object.</span></span>                                                  |
| <span data-ttu-id="553d4-166">::public static int strHashKey(str sourceString)</span><span class="sxs-lookup"><span data-stu-id="553d4-166">::public static int strHashKey(str sourceString)</span></span>                       |                                                                                                       |
| <span data-ttu-id="553d4-167">public void new()</span><span class="sxs-lookup"><span data-stu-id="553d4-167">public void new()</span></span>                                                      | <span data-ttu-id="553d4-168">TextBuffer クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="553d4-168">Initializes a new instance of the TextBuffer class.</span></span>                                                   |
| <span data-ttu-id="553d4-169">public void removeChar(str charList)</span><span class="sxs-lookup"><span data-stu-id="553d4-169">public void removeChar(str charList)</span></span>                                   |                                                                                                       |
| <span data-ttu-id="553d4-170">public void toClipboard()</span><span class="sxs-lookup"><span data-stu-id="553d4-170">public void toClipboard()</span></span>                                              | <span data-ttu-id="553d4-171">TextBuffer オブジェクトの内容をクリップボードにコピーします。</span><span class="sxs-lookup"><span data-stu-id="553d4-171">Copies the content of a TextBuffer object to the clipboard.</span></span>                                           |
| <span data-ttu-id="553d4-172">public void insert(str insertString, int position)</span><span class="sxs-lookup"><span data-stu-id="553d4-172">public void insert(str insertString, int position)</span></span>                     |                                                                                                       |
| <span data-ttu-id="553d4-173">public void setText(str string)</span><span class="sxs-lookup"><span data-stu-id="553d4-173">public void setText(str string)</span></span>                                        | <span data-ttu-id="553d4-174">既存の内容を上書きして、指定した文字列に TextBuffer オブジェクトの内容を設定します。</span><span class="sxs-lookup"><span data-stu-id="553d4-174">Sets the content of the TextBuffer object to the specified string, overwriting any existing content.</span></span>  |
| <span data-ttu-id="553d4-175">public void appendText(str string)</span><span class="sxs-lookup"><span data-stu-id="553d4-175">public void appendText(str string)</span></span>                                     | <span data-ttu-id="553d4-176">TextBuffer オブジェクトの内容に文字列を追加します。</span><span class="sxs-lookup"><span data-stu-id="553d4-176">Appends a string to the content of the TextBuffer object.</span></span>                                             |
| <span data-ttu-id="553d4-177">public void replace(str findString, str replaceString)</span><span class="sxs-lookup"><span data-stu-id="553d4-177">public void replace(str findString, str replaceString)</span></span>                 |                                                                                                       |
| <span data-ttu-id="553d4-178">public void delete(int start, int length)</span><span class="sxs-lookup"><span data-stu-id="553d4-178">public void delete(int start, int length)</span></span>                              |                                                                                                       |

### <a name="method-accept"></a><span data-ttu-id="553d4-179">メソッド accept</span><span class="sxs-lookup"><span data-stu-id="553d4-179">Method accept</span></span>

    public boolean accept(str searchText)

#### <a name="parameters"></a><span data-ttu-id="553d4-180">パラメーター</span><span class="sxs-lookup"><span data-stu-id="553d4-180">Parameters</span></span>

<span data-ttu-id="553d4-181">searchText</span><span class="sxs-lookup"><span data-stu-id="553d4-181">searchText</span></span>  

#### <a name="return-value"></a><span data-ttu-id="553d4-182">戻り値</span><span class="sxs-lookup"><span data-stu-id="553d4-182">Return Value</span></span>

### <a name="method-decryptold"></a><span data-ttu-id="553d4-183">メソッド decryptOld</span><span class="sxs-lookup"><span data-stu-id="553d4-183">Method decryptOld</span></span>

    public int decryptOld(int cryptKey)

#### <a name="parameters"></a><span data-ttu-id="553d4-184">パラメーター</span><span class="sxs-lookup"><span data-stu-id="553d4-184">Parameters</span></span>

<span data-ttu-id="553d4-185">cryptKey</span><span class="sxs-lookup"><span data-stu-id="553d4-185">cryptKey</span></span>  

#### <a name="return-value"></a><span data-ttu-id="553d4-186">戻り値</span><span class="sxs-lookup"><span data-stu-id="553d4-186">Return Value</span></span>

### <a name="method-find"></a><span data-ttu-id="553d4-187">メソッド find</span><span class="sxs-lookup"><span data-stu-id="553d4-187">Method find</span></span>

<span data-ttu-id="553d4-188">TextBuffer オブジェクトで文字列式の発生を検索します。</span><span class="sxs-lookup"><span data-stu-id="553d4-188">Searches the TextBuffer object for any occurrence of a string expression.</span></span>

    public boolean find(str searchText, [int start])

#### <a name="parameters"></a><span data-ttu-id="553d4-189">パラメーター</span><span class="sxs-lookup"><span data-stu-id="553d4-189">Parameters</span></span>

<span data-ttu-id="553d4-190">searchText</span><span class="sxs-lookup"><span data-stu-id="553d4-190">searchText</span></span>  
<span data-ttu-id="553d4-191">各検索の開始位置を設定する数式 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="553d4-191">A numeric expression that sets the starting position for each search; optional.</span></span> <span data-ttu-id="553d4-192">このパラメータを省略すると、検索は、最初の文字位置から開始します。</span><span class="sxs-lookup"><span data-stu-id="553d4-192">If this parameter is omitted, the search starts at the first character position.</span></span>

<!-- -->

<span data-ttu-id="553d4-193">開始</span><span class="sxs-lookup"><span data-stu-id="553d4-193">start</span></span>  
<span data-ttu-id="553d4-194">各検索の開始位置を設定する数式 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="553d4-194">A numeric expression that sets the starting position for each search; optional.</span></span> <span data-ttu-id="553d4-195">このパラメータを省略すると、検索は、最初の文字位置から開始します。</span><span class="sxs-lookup"><span data-stu-id="553d4-195">If this parameter is omitted, the search starts at the first character position.</span></span>

#### <a name="return-value"></a><span data-ttu-id="553d4-196">戻り値</span><span class="sxs-lookup"><span data-stu-id="553d4-196">Return Value</span></span>

<span data-ttu-id="553d4-197">searchText が見つかった場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="553d4-197">true if searchText is found; otherwise, false.</span></span>

#### <a name="remarks"></a><span data-ttu-id="553d4-198">備考</span><span class="sxs-lookup"><span data-stu-id="553d4-198">Remarks</span></span>

<span data-ttu-id="553d4-199">このメソッドは、正規表現を使用して、大文字と小文字を区別しないテキスト比較を実行します。</span><span class="sxs-lookup"><span data-stu-id="553d4-199">This method performs a textual, case-insensitive comparison by using regular expressions.</span></span> <span data-ttu-id="553d4-200">詳細については、「一致する機能」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="553d4-200">For more information, see the match function.</span></span> <span data-ttu-id="553d4-201">大文字と小文字を区別しないようにするには、ignoreCase メソッドを使用します。</span><span class="sxs-lookup"><span data-stu-id="553d4-201">Case-insensitivity can be turned off by using the ignoreCase method.</span></span> <span data-ttu-id="553d4-202">正規表現は、regularExpressions メソッドを使用してオフにすることができます。</span><span class="sxs-lookup"><span data-stu-id="553d4-202">Regular expressions can be turned off by using the regularExpressions method.</span></span>

#### <a name="examples"></a><span data-ttu-id="553d4-203">例</span><span class="sxs-lookup"><span data-stu-id="553d4-203">Examples</span></span>

<span data-ttu-id="553d4-204">次の例では、指定した文字列の発生のすべてについて TextBuffer オブジェクトを検索し、一致が検出された位置を出力します。</span><span class="sxs-lookup"><span data-stu-id="553d4-204">The following example searches the TextBuffer object for all occurrences of a specified string and prints the position at which the match is found.</span></span>

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

### <a name="method-fromclipboard"></a><span data-ttu-id="553d4-205">メソッド fromClipboard</span><span class="sxs-lookup"><span data-stu-id="553d4-205">Method fromClipboard</span></span>

<span data-ttu-id="553d4-206">TextBuffer オブジェクトの内容をクリップボードの内容に置き換えます。</span><span class="sxs-lookup"><span data-stu-id="553d4-206">Replaces the content of the TextBuffer object with the content of the clipboard.</span></span>

    public boolean fromClipboard()

#### <a name="return-value"></a><span data-ttu-id="553d4-207">戻り値</span><span class="sxs-lookup"><span data-stu-id="553d4-207">Return Value</span></span>

<span data-ttu-id="553d4-208">置換が成功した場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="553d4-208">true if the replacement was successful; otherwise, false.</span></span>

#### <a name="examples"></a><span data-ttu-id="553d4-209">例</span><span class="sxs-lookup"><span data-stu-id="553d4-209">Examples</span></span>

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

### <a name="method-fromfile"></a><span data-ttu-id="553d4-210">メソッド fromFile</span><span class="sxs-lookup"><span data-stu-id="553d4-210">Method fromFile</span></span>

<span data-ttu-id="553d4-211">TextBuffer オブジェクトの内容を指定したファイルの内容に置き換えます。</span><span class="sxs-lookup"><span data-stu-id="553d4-211">Replaces the content of a TextBuffer object with the content of the specified file.</span></span>

    public boolean fromFile(str filename, [int encoding])

#### <a name="parameters"></a><span data-ttu-id="553d4-212">パラメーター</span><span class="sxs-lookup"><span data-stu-id="553d4-212">Parameters</span></span>

<span data-ttu-id="553d4-213">filename</span><span class="sxs-lookup"><span data-stu-id="553d4-213">filename</span></span>  
<span data-ttu-id="553d4-214">エンコードに使用できるオプション (オプション)。</span><span class="sxs-lookup"><span data-stu-id="553d4-214">The encoding option to use; optional.</span></span>

<!-- -->

<span data-ttu-id="553d4-215">encoding</span><span class="sxs-lookup"><span data-stu-id="553d4-215">encoding</span></span>  
<span data-ttu-id="553d4-216">エンコードに使用できるオプション (オプション)。</span><span class="sxs-lookup"><span data-stu-id="553d4-216">The encoding option to use; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="553d4-217">戻り値</span><span class="sxs-lookup"><span data-stu-id="553d4-217">Return Value</span></span>

<span data-ttu-id="553d4-218">フィールド操作が成功した場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="553d4-218">true if the file operation was successful; otherwise, false.</span></span>

#### <a name="remarks"></a><span data-ttu-id="553d4-219">備考</span><span class="sxs-lookup"><span data-stu-id="553d4-219">Remarks</span></span>

<span data-ttu-id="553d4-220">FileEncoding システム列挙によって提供されるエンコーディング パラメーターの可能な値は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="553d4-220">The following are possible values for the encoding parameter that are supplied by the FileEncoding system enumeration:</span></span>

-   <span data-ttu-id="553d4-221">ACP</span><span class="sxs-lookup"><span data-stu-id="553d4-221">ACP</span></span>
-   <span data-ttu-id="553d4-222">UTF8</span><span class="sxs-lookup"><span data-stu-id="553d4-222">UTF8</span></span>
-   <span data-ttu-id="553d4-223">UTF16BE</span><span class="sxs-lookup"><span data-stu-id="553d4-223">UTF16BE</span></span>
-   <span data-ttu-id="553d4-224">UTF16LE</span><span class="sxs-lookup"><span data-stu-id="553d4-224">UTF16LE</span></span>
-   <span data-ttu-id="553d4-225">GB18030</span><span class="sxs-lookup"><span data-stu-id="553d4-225">GB18030</span></span>
-   <span data-ttu-id="553d4-226">AUTO</span><span class="sxs-lookup"><span data-stu-id="553d4-226">AUTO</span></span>

<span data-ttu-id="553d4-227">ファイルの操作に失敗した場合、TextBuffer オブジェクトは変更されません。</span><span class="sxs-lookup"><span data-stu-id="553d4-227">If the file operation is unsuccessful, the TextBuffer object remains unchanged.</span></span> <span data-ttu-id="553d4-228">攻撃者が fromFile メソッドへの入力を制御できる場合、セキュリティ上のリスクが存在します。</span><span class="sxs-lookup"><span data-stu-id="553d4-228">If an attacker can control input to the fromFile method, a security risk exists.</span></span> <span data-ttu-id="553d4-229">したがって、このメソッドは、コード アクセス セキュリティで実行されます。</span><span class="sxs-lookup"><span data-stu-id="553d4-229">Therefore, this method runs under Code Access Security.</span></span> <span data-ttu-id="553d4-230">サーバー上でこのメソッドを呼び出すには、ExecutePermission クラスからのアクセス許可が必要です。</span><span class="sxs-lookup"><span data-stu-id="553d4-230">Calls to this method on the server require permission from the ExecutePermission class.</span></span> <span data-ttu-id="553d4-231">ユーザーがこのメソッドを呼び出すコントロールで、SysDevelopment へのセキュリティ キーを設定して開発権限を持っていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="553d4-231">Make sure that the user has development privileges by setting the security key to SysDevelopment on the control that calls this method.</span></span>

### <a name="method-gettext"></a><span data-ttu-id="553d4-232">メソッド getText</span><span class="sxs-lookup"><span data-stu-id="553d4-232">Method getText</span></span>

<span data-ttu-id="553d4-233">TextBuffer オブジェクトの現在の内容を取得します。</span><span class="sxs-lookup"><span data-stu-id="553d4-233">Retrieves the current content of the TextBuffer object.</span></span>

    public str getText()

#### <a name="return-value"></a><span data-ttu-id="553d4-234">戻り値</span><span class="sxs-lookup"><span data-stu-id="553d4-234">Return Value</span></span>

<span data-ttu-id="553d4-235">TextBuffer オブジェクトのコンテンツを含む文字列。</span><span class="sxs-lookup"><span data-stu-id="553d4-235">A string that contains the content of TextBuffer object.</span></span>

#### <a name="remarks"></a><span data-ttu-id="553d4-236">備考</span><span class="sxs-lookup"><span data-stu-id="553d4-236">Remarks</span></span>

<span data-ttu-id="553d4-237">TextBuffer は、新しい明細行を含むことができ、これが、返される文字列に含まれます。</span><span class="sxs-lookup"><span data-stu-id="553d4-237">The TextBuffer can contain new lines, which are then present in the returned string.</span></span>

### <a name="method-getvalue"></a><span data-ttu-id="553d4-238">メソッド getValue</span><span class="sxs-lookup"><span data-stu-id="553d4-238">Method getValue</span></span>

    public int getValue()

#### <a name="return-value"></a><span data-ttu-id="553d4-239">戻り値</span><span class="sxs-lookup"><span data-stu-id="553d4-239">Return Value</span></span>

### <a name="method-ignorecase"></a><span data-ttu-id="553d4-240">メソッド ignoreCase</span><span class="sxs-lookup"><span data-stu-id="553d4-240">Method ignoreCase</span></span>

    public boolean ignoreCase([boolean ignoreCase])

#### <a name="parameters"></a><span data-ttu-id="553d4-241">パラメーター</span><span class="sxs-lookup"><span data-stu-id="553d4-241">Parameters</span></span>

<span data-ttu-id="553d4-242">ignoreCase</span><span class="sxs-lookup"><span data-stu-id="553d4-242">ignoreCase</span></span>  

#### <a name="return-value"></a><span data-ttu-id="553d4-243">戻り値</span><span class="sxs-lookup"><span data-stu-id="553d4-243">Return Value</span></span>

### <a name="method-isnext"></a><span data-ttu-id="553d4-244">メソッド isNext</span><span class="sxs-lookup"><span data-stu-id="553d4-244">Method isNext</span></span>

    public boolean isNext(str searchText)

#### <a name="parameters"></a><span data-ttu-id="553d4-245">パラメーター</span><span class="sxs-lookup"><span data-stu-id="553d4-245">Parameters</span></span>

<span data-ttu-id="553d4-246">searchText</span><span class="sxs-lookup"><span data-stu-id="553d4-246">searchText</span></span>  

#### <a name="return-value"></a><span data-ttu-id="553d4-247">戻り値</span><span class="sxs-lookup"><span data-stu-id="553d4-247">Return Value</span></span>

### <a name="method-matchlen"></a><span data-ttu-id="553d4-248">メソッド matchLen</span><span class="sxs-lookup"><span data-stu-id="553d4-248">Method matchLen</span></span>

<span data-ttu-id="553d4-249">TextBuffer オブジェクトで最初に一致する文字列の長さを返します。</span><span class="sxs-lookup"><span data-stu-id="553d4-249">Returns the string length of the first match in the TextBuffer object.</span></span>

    public int matchLen()

#### <a name="return-value"></a><span data-ttu-id="553d4-250">戻り値</span><span class="sxs-lookup"><span data-stu-id="553d4-250">Return Value</span></span>

<span data-ttu-id="553d4-251">見つかった一致の長さ。一致するものが見つからない場合は 0 (ゼロ)。</span><span class="sxs-lookup"><span data-stu-id="553d4-251">The length of the match that is found; 0 (zero) if no match is found.</span></span>

#### <a name="remarks"></a><span data-ttu-id="553d4-252">備考</span><span class="sxs-lookup"><span data-stu-id="553d4-252">Remarks</span></span>

<span data-ttu-id="553d4-253">このメソッドは、テキスト検索の一部として使用されます (find メソッドを参照)。</span><span class="sxs-lookup"><span data-stu-id="553d4-253">This method is used as part of a text search (see the find method).</span></span>

### <a name="method-matchpos"></a><span data-ttu-id="553d4-254">メソッド matchPos</span><span class="sxs-lookup"><span data-stu-id="553d4-254">Method matchPos</span></span>

<span data-ttu-id="553d4-255">TextBuffer オブジェクトの検索文字列の 1 番目の文字の位置を返します。</span><span class="sxs-lookup"><span data-stu-id="553d4-255">Returns the character position of the first occurrence of the search string in the TextBuffer object.</span></span>

    public int matchPos()

#### <a name="return-value"></a><span data-ttu-id="553d4-256">戻り値</span><span class="sxs-lookup"><span data-stu-id="553d4-256">Return Value</span></span>

<span data-ttu-id="553d4-257">一致が見つかった位置。一致しない場合は 0 (ゼロ)。</span><span class="sxs-lookup"><span data-stu-id="553d4-257">The position at which the match is found; 0 (zero) if no match is found.</span></span>

#### <a name="remarks"></a><span data-ttu-id="553d4-258">備考</span><span class="sxs-lookup"><span data-stu-id="553d4-258">Remarks</span></span>

<span data-ttu-id="553d4-259">このメソッドは、テキスト検索の一部として使用されます (find メソッドを参照)。</span><span class="sxs-lookup"><span data-stu-id="553d4-259">This method is used as part of a text search (see the find method).</span></span>

### <a name="method-nexttoken"></a><span data-ttu-id="553d4-260">メソッド nextToken</span><span class="sxs-lookup"><span data-stu-id="553d4-260">Method nextToken</span></span>

    public str nextToken([boolean includeWholeLine], [str stopAtChar])

#### <a name="parameters"></a><span data-ttu-id="553d4-261">パラメーター</span><span class="sxs-lookup"><span data-stu-id="553d4-261">Parameters</span></span>

<span data-ttu-id="553d4-262">includeWholeLine</span><span class="sxs-lookup"><span data-stu-id="553d4-262">includeWholeLine</span></span>  

<!-- -->

<span data-ttu-id="553d4-263">stopAtChar</span><span class="sxs-lookup"><span data-stu-id="553d4-263">stopAtChar</span></span>  

#### <a name="return-value"></a><span data-ttu-id="553d4-264">戻り値</span><span class="sxs-lookup"><span data-stu-id="553d4-264">Return Value</span></span>

### <a name="method-numlines"></a><span data-ttu-id="553d4-265">メソッド numLines</span><span class="sxs-lookup"><span data-stu-id="553d4-265">Method numLines</span></span>

<span data-ttu-id="553d4-266">TextBuffer オブジェクトの明細行の数を取得します。</span><span class="sxs-lookup"><span data-stu-id="553d4-266">Retrieves the number of lines in the TextBuffer object.</span></span>

    public int numLines()

#### <a name="return-value"></a><span data-ttu-id="553d4-267">戻り値</span><span class="sxs-lookup"><span data-stu-id="553d4-267">Return Value</span></span>

<span data-ttu-id="553d4-268">コンテンツ内の行数。</span><span class="sxs-lookup"><span data-stu-id="553d4-268">The number of lines in the content.</span></span>

#### <a name="remarks"></a><span data-ttu-id="553d4-269">備考</span><span class="sxs-lookup"><span data-stu-id="553d4-269">Remarks</span></span>

<span data-ttu-id="553d4-270">行は改行 ('\\n') で区切られます。</span><span class="sxs-lookup"><span data-stu-id="553d4-270">Lines are separated by newlines ('\\n').</span></span>

#### <a name="examples"></a><span data-ttu-id="553d4-271">例</span><span class="sxs-lookup"><span data-stu-id="553d4-271">Examples</span></span>

    { 
        TextBuffer txtb = new TextBuffer(); 
        if (txtb.fromClipboard()) 
        { 
            print "Clipboard contains ",txtb.numLines()," lines."; 
        } 
    }

### <a name="method-regularexpressions"></a><span data-ttu-id="553d4-272">メソッド regularExpressions</span><span class="sxs-lookup"><span data-stu-id="553d4-272">Method regularExpressions</span></span>

    public boolean regularExpressions([boolean useRegularExpressions])

#### <a name="parameters"></a><span data-ttu-id="553d4-273">パラメーター</span><span class="sxs-lookup"><span data-stu-id="553d4-273">Parameters</span></span>

<span data-ttu-id="553d4-274">useRegularExpressions</span><span class="sxs-lookup"><span data-stu-id="553d4-274">useRegularExpressions</span></span>  

#### <a name="return-value"></a><span data-ttu-id="553d4-275">戻り値</span><span class="sxs-lookup"><span data-stu-id="553d4-275">Return Value</span></span>

### <a name="method-size"></a><span data-ttu-id="553d4-276">メソッド size</span><span class="sxs-lookup"><span data-stu-id="553d4-276">Method size</span></span>

    public int size()

#### <a name="return-value"></a><span data-ttu-id="553d4-277">戻り値</span><span class="sxs-lookup"><span data-stu-id="553d4-277">Return Value</span></span>

### <a name="method-substr"></a><span data-ttu-id="553d4-278">メソッド subStr</span><span class="sxs-lookup"><span data-stu-id="553d4-278">Method subStr</span></span>

<span data-ttu-id="553d4-279">TextBuffer オブジェクト (サブ文字列) の内容の一部を取得します。</span><span class="sxs-lookup"><span data-stu-id="553d4-279">Retrieves part of the content of the TextBuffer object (a substring).</span></span>

    public str subStr(int start, int length)

#### <a name="parameters"></a><span data-ttu-id="553d4-280">パラメーター</span><span class="sxs-lookup"><span data-stu-id="553d4-280">Parameters</span></span>

<span data-ttu-id="553d4-281">開始</span><span class="sxs-lookup"><span data-stu-id="553d4-281">start</span></span>  
<span data-ttu-id="553d4-282">目的のサブ文字列の長さ。</span><span class="sxs-lookup"><span data-stu-id="553d4-282">The length of the desired substring.</span></span>

<!-- -->

<span data-ttu-id="553d4-283">length</span><span class="sxs-lookup"><span data-stu-id="553d4-283">length</span></span>  
<span data-ttu-id="553d4-284">目的のサブ文字列の長さ。</span><span class="sxs-lookup"><span data-stu-id="553d4-284">The length of the desired substring.</span></span>

#### <a name="return-value"></a><span data-ttu-id="553d4-285">戻り値</span><span class="sxs-lookup"><span data-stu-id="553d4-285">Return Value</span></span>

<span data-ttu-id="553d4-286">TextBuffer オブジェクト コンテンツの指定された部分を含む文字列。</span><span class="sxs-lookup"><span data-stu-id="553d4-286">A string that contains the specified part of the TextBuffer object content.</span></span>

#### <a name="remarks"></a><span data-ttu-id="553d4-287">備考</span><span class="sxs-lookup"><span data-stu-id="553d4-287">Remarks</span></span>

<span data-ttu-id="553d4-288">部分文字列の開始位置を指定するときは、コンテンツの最初の文字に 1 を、2 番目の文字に 2 というように使用します。</span><span class="sxs-lookup"><span data-stu-id="553d4-288">When you specify the start position for substring, use 1 for the first character in the content, 2 for the second character, and so on.</span></span>

#### <a name="examples"></a><span data-ttu-id="553d4-289">例</span><span class="sxs-lookup"><span data-stu-id="553d4-289">Examples</span></span>

    { 
        TextBuffer txtb = new TextBuffer(); 
        str mystr; 
        if (txtb.fromClipboard()) 
        { 
            mystr = txtb.subStr(10,15);  
            // 15 long substring starting at position 10. 
        } 
    }

### <a name="method-tofile"></a><span data-ttu-id="553d4-290">メソッド toFile</span><span class="sxs-lookup"><span data-stu-id="553d4-290">Method toFile</span></span>

<span data-ttu-id="553d4-291">TextBuffer オブジェクトの内容をファイルに保存します。</span><span class="sxs-lookup"><span data-stu-id="553d4-291">Saves the content of the TextBuffer object to a file.</span></span>

    public boolean toFile(str filename, [int encoding])

#### <a name="parameters"></a><span data-ttu-id="553d4-292">パラメーター</span><span class="sxs-lookup"><span data-stu-id="553d4-292">Parameters</span></span>

<span data-ttu-id="553d4-293">filename</span><span class="sxs-lookup"><span data-stu-id="553d4-293">filename</span></span>  

<!-- -->

<span data-ttu-id="553d4-294">encoding</span><span class="sxs-lookup"><span data-stu-id="553d4-294">encoding</span></span>  

#### <a name="return-value"></a><span data-ttu-id="553d4-295">戻り値</span><span class="sxs-lookup"><span data-stu-id="553d4-295">Return Value</span></span>

<span data-ttu-id="553d4-296">操作が成功する場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="553d4-296">true if the operation is successful; otherwise, false.</span></span>

#### <a name="remarks"></a><span data-ttu-id="553d4-297">備考</span><span class="sxs-lookup"><span data-stu-id="553d4-297">Remarks</span></span>

<span data-ttu-id="553d4-298">指定したファイルが既に存在する場合は、確認なしで上書きされます。</span><span class="sxs-lookup"><span data-stu-id="553d4-298">If the specified file already exists, it is overwritten without confirmation.</span></span> <span data-ttu-id="553d4-299">攻撃者が toFile メソッドへの入力を制御できる場合、セキュリティ上のリスクが存在します。</span><span class="sxs-lookup"><span data-stu-id="553d4-299">If an attacker can control input to the toFile method, a security risk exists.</span></span> <span data-ttu-id="553d4-300">したがって、このメソッドは、コード アクセス セキュリティで実行されます。</span><span class="sxs-lookup"><span data-stu-id="553d4-300">Therefore, this method runs under Code Access Security.</span></span> <span data-ttu-id="553d4-301">サーバー上でこのメソッドを呼び出すには、ExecutePermission クラスからのアクセス許可が必要です。</span><span class="sxs-lookup"><span data-stu-id="553d4-301">Calls to this method on the server require permission from the ExecutePermission class.</span></span> <span data-ttu-id="553d4-302">ユーザーがこのメソッドを呼び出すコントロールで、SysDevelopment へのセキュリティ キーを設定して開発権限を持っていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="553d4-302">Make sure that the user has development privileges by setting the security key to SysDevelopment on the control that calls this method.</span></span>

### <a name="method-token"></a><span data-ttu-id="553d4-303">メソッド token</span><span class="sxs-lookup"><span data-stu-id="553d4-303">Method token</span></span>

    public str token()

#### <a name="return-value"></a><span data-ttu-id="553d4-304">戻り値</span><span class="sxs-lookup"><span data-stu-id="553d4-304">Return Value</span></span>

### <a name="method-tostring"></a><span data-ttu-id="553d4-305">メソッド toString</span><span class="sxs-lookup"><span data-stu-id="553d4-305">Method toString</span></span>

<span data-ttu-id="553d4-306">現在のオブジェクトを表す文字列を返します。</span><span class="sxs-lookup"><span data-stu-id="553d4-306">Returns a string that represents the current object.</span></span>

    public str toString()

#### <a name="return-value"></a><span data-ttu-id="553d4-307">戻り値</span><span class="sxs-lookup"><span data-stu-id="553d4-307">Return Value</span></span>

<span data-ttu-id="553d4-308">現在のオブジェクトを表す文字列。</span><span class="sxs-lookup"><span data-stu-id="553d4-308">A string that represents the current object.</span></span>

#### <a name="remarks"></a><span data-ttu-id="553d4-309">備考</span><span class="sxs-lookup"><span data-stu-id="553d4-309">Remarks</span></span>

<span data-ttu-id="553d4-310">既定の実装は、オブジェクトのクラス名を返します。</span><span class="sxs-lookup"><span data-stu-id="553d4-310">The default implementation returns the class name of the object.</span></span> <span data-ttu-id="553d4-311">メソッドは派生クラスで上書きできるため、そのタイプの意味のある値が返されます。</span><span class="sxs-lookup"><span data-stu-id="553d4-311">The method can be overridden in a derived class so that it returns values that are meaningful for that type.</span></span> <span data-ttu-id="553d4-312">たとえば、SysMethodInfo クラスのインスタンスは、インスタンスまたは静的などのメソッド名およびメソッドのタイプを返します。</span><span class="sxs-lookup"><span data-stu-id="553d4-312">For example, an instance of the SysMethodInfo class returns the method name and type of the method, such as instance or static.</span></span>

### <a name="method-strhashkey"></a><span data-ttu-id="553d4-313">メソッド strHashKey</span><span class="sxs-lookup"><span data-stu-id="553d4-313">Method strHashKey</span></span>

    public static int strHashKey(str sourceString)

#### <a name="parameters"></a><span data-ttu-id="553d4-314">パラメーター</span><span class="sxs-lookup"><span data-stu-id="553d4-314">Parameters</span></span>

<span data-ttu-id="553d4-315">sourceString</span><span class="sxs-lookup"><span data-stu-id="553d4-315">sourceString</span></span>  

#### <a name="return-value"></a><span data-ttu-id="553d4-316">戻り値</span><span class="sxs-lookup"><span data-stu-id="553d4-316">Return Value</span></span>

### <a name="method-new"></a><span data-ttu-id="553d4-317">メソッド new</span><span class="sxs-lookup"><span data-stu-id="553d4-317">Method new</span></span>

<span data-ttu-id="553d4-318">TextBuffer クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="553d4-318">Initializes a new instance of the TextBuffer class.</span></span>

    public void new()

### <a name="method-removechar"></a><span data-ttu-id="553d4-319">メソッド removeChar</span><span class="sxs-lookup"><span data-stu-id="553d4-319">Method removeChar</span></span>

    public void removeChar(str charList)

#### <a name="parameters"></a><span data-ttu-id="553d4-320">パラメーター</span><span class="sxs-lookup"><span data-stu-id="553d4-320">Parameters</span></span>

<span data-ttu-id="553d4-321">charList</span><span class="sxs-lookup"><span data-stu-id="553d4-321">charList</span></span>  

### <a name="method-toclipboard"></a><span data-ttu-id="553d4-322">メソッド toClipboard</span><span class="sxs-lookup"><span data-stu-id="553d4-322">Method toClipboard</span></span>

<span data-ttu-id="553d4-323">TextBuffer オブジェクトの内容をクリップボードにコピーします。</span><span class="sxs-lookup"><span data-stu-id="553d4-323">Copies the content of a TextBuffer object to the clipboard.</span></span>

    public void toClipboard()

### <a name="method-insert"></a><span data-ttu-id="553d4-324">メソッド insert</span><span class="sxs-lookup"><span data-stu-id="553d4-324">Method insert</span></span>

    public void insert(str insertString, int position)

#### <a name="parameters"></a><span data-ttu-id="553d4-325">パラメーター</span><span class="sxs-lookup"><span data-stu-id="553d4-325">Parameters</span></span>

<span data-ttu-id="553d4-326">insertString</span><span class="sxs-lookup"><span data-stu-id="553d4-326">insertString</span></span>  

<!-- -->

<span data-ttu-id="553d4-327">職位</span><span class="sxs-lookup"><span data-stu-id="553d4-327">position</span></span>  

### <a name="method-settext"></a><span data-ttu-id="553d4-328">メソッド setText</span><span class="sxs-lookup"><span data-stu-id="553d4-328">Method setText</span></span>

<span data-ttu-id="553d4-329">既存の内容を上書きして、指定した文字列に TextBuffer オブジェクトの内容を設定します。</span><span class="sxs-lookup"><span data-stu-id="553d4-329">Sets the content of the TextBuffer object to the specified string, overwriting any existing content.</span></span>

    public void setText(str string)

#### <a name="parameters"></a><span data-ttu-id="553d4-330">パラメーター</span><span class="sxs-lookup"><span data-stu-id="553d4-330">Parameters</span></span>

<span data-ttu-id="553d4-331">string</span><span class="sxs-lookup"><span data-stu-id="553d4-331">string</span></span>  
<span data-ttu-id="553d4-332">TextBuffer オブジェクトの新しいテキストを含む文字列。</span><span class="sxs-lookup"><span data-stu-id="553d4-332">A string that contains the new text for the TextBuffer object.</span></span>

#### <a name="remarks"></a><span data-ttu-id="553d4-333">備考</span><span class="sxs-lookup"><span data-stu-id="553d4-333">Remarks</span></span>

<span data-ttu-id="553d4-334">TextBuffer オブジェクトに任意のコンテンツが含まれている場合は、新しいコンテンツで上書きされます。</span><span class="sxs-lookup"><span data-stu-id="553d4-334">If the TextBuffer object contains any content, it is overwritten by the new content.</span></span>

#### <a name="examples"></a><span data-ttu-id="553d4-335">例</span><span class="sxs-lookup"><span data-stu-id="553d4-335">Examples</span></span>

    { 
        TextBuffer txtb = new TextBuffer(); 
        txtb.setText("This is the first text."); 
        // Now txtb contains exactly that text. 
    }

### <a name="method-appendtext"></a><span data-ttu-id="553d4-336">メソッド appendText</span><span class="sxs-lookup"><span data-stu-id="553d4-336">Method appendText</span></span>

<span data-ttu-id="553d4-337">TextBuffer オブジェクトの内容に文字列を追加します。</span><span class="sxs-lookup"><span data-stu-id="553d4-337">Appends a string to the content of the TextBuffer object.</span></span>

    public void appendText(str string)

#### <a name="parameters"></a><span data-ttu-id="553d4-338">パラメーター</span><span class="sxs-lookup"><span data-stu-id="553d4-338">Parameters</span></span>

<span data-ttu-id="553d4-339">string</span><span class="sxs-lookup"><span data-stu-id="553d4-339">string</span></span>  
<span data-ttu-id="553d4-340">追加する文字列。</span><span class="sxs-lookup"><span data-stu-id="553d4-340">The string to append.</span></span>

#### <a name="examples"></a><span data-ttu-id="553d4-341">例</span><span class="sxs-lookup"><span data-stu-id="553d4-341">Examples</span></span>

    { 
        TextBuffer txtb = new TextBuffer(); 
        txtb.setText("[One]"); 
        txtb.appendText("[Another]"); 
        print txtb.getText(); // Will print "[One][Another]" 
    }

### <a name="method-replace"></a><span data-ttu-id="553d4-342">メソッド replace</span><span class="sxs-lookup"><span data-stu-id="553d4-342">Method replace</span></span>

    public void replace(str findString, str replaceString)

#### <a name="parameters"></a><span data-ttu-id="553d4-343">パラメーター</span><span class="sxs-lookup"><span data-stu-id="553d4-343">Parameters</span></span>

<span data-ttu-id="553d4-344">findString</span><span class="sxs-lookup"><span data-stu-id="553d4-344">findString</span></span>  

<!-- -->

<span data-ttu-id="553d4-345">replaceString</span><span class="sxs-lookup"><span data-stu-id="553d4-345">replaceString</span></span>  

### <a name="method-delete"></a><span data-ttu-id="553d4-346">メソッド delete</span><span class="sxs-lookup"><span data-stu-id="553d4-346">Method delete</span></span>

    public void delete(int start, int length)

#### <a name="parameters"></a><span data-ttu-id="553d4-347">パラメーター</span><span class="sxs-lookup"><span data-stu-id="553d4-347">Parameters</span></span>

<span data-ttu-id="553d4-348">開始</span><span class="sxs-lookup"><span data-stu-id="553d4-348">start</span></span>  

<!-- -->

<span data-ttu-id="553d4-349">length</span><span class="sxs-lookup"><span data-stu-id="553d4-349">length</span></span>  

## <a name="class-textio"></a><span data-ttu-id="553d4-350">クラス TextIo</span><span class="sxs-lookup"><span data-stu-id="553d4-350">Class TextIo</span></span>
    class TextIo extends CommaIo

<span data-ttu-id="553d4-351">TextIo クラスには、テキスト ファイルの読み取りと書き込みを行う機能があります。</span><span class="sxs-lookup"><span data-stu-id="553d4-351">The TextIo class provides functionality for reading and writing text files.</span></span>

### <a name="remarks"></a><span data-ttu-id="553d4-352">備考</span><span class="sxs-lookup"><span data-stu-id="553d4-352">Remarks</span></span>

<span data-ttu-id="553d4-353">TextIO は、非 ANSI コード ページ ファイル I/O のサポートを提供する AsciiIO を置き換えます。</span><span class="sxs-lookup"><span data-stu-id="553d4-353">TextIO replaces AsciiIO to provide support for non-ANSI code page file I/O.</span></span> <span data-ttu-id="553d4-354">TextIO コンストラクターには、ファイルのコード ページを設定するための追加のオプション パラメーターがあります。</span><span class="sxs-lookup"><span data-stu-id="553d4-354">The TextIO constructor has an additional optional parameter to set the code page of the file.</span></span> <span data-ttu-id="553d4-355">TextIO.new メソッドには、ファイルのコード ページを指定するオプション引数があります。</span><span class="sxs-lookup"><span data-stu-id="553d4-355">The TextIO.new method has an optional argument that specifies the code page of the file.</span></span> <span data-ttu-id="553d4-356">既定値は UTF-16LE (Microsoft Windows ネイティブ Unicode 表現) です。</span><span class="sxs-lookup"><span data-stu-id="553d4-356">The default value is UTF-16LE (the Microsoft Windows native Unicode representation).</span></span> <span data-ttu-id="553d4-357">ほとんどの場合、特にエンドユーザーが Finance and Operations アプリケーション以外のテキスト エディターでファイルを編集する可能性がある場合に、これを使用することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="553d4-357">It is best to use this in most instances, especially if end-users might edit the file in a text editor outside of the Finance and Operations application.</span></span> <span data-ttu-id="553d4-358">詳細については、「TextIo.new」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="553d4-358">For more information, see TextIo.new.</span></span> <span data-ttu-id="553d4-359">ファイルが読み取られると、TextIO はファイルの最初の数バイトについてバイト順マーク (BOM) を調べて、UTF-8、UTF-16LE、および UTF-16BE を自動的に取り扱います。</span><span class="sxs-lookup"><span data-stu-id="553d4-359">When files are read, TextIO examines the first few bytes of the file for a byte-order mark (BOM) and automatically handles UTF-8, UTF-16LE, and UTF-16BE.</span></span> <span data-ttu-id="553d4-360">BOM が見つからない場合、ファイルは ANSI コード ページ (ACP) 形式であると見なされます。</span><span class="sxs-lookup"><span data-stu-id="553d4-360">If no BOM is found, the file is assumed to be in the ANSI Code Page (ACP) format.</span></span>

### <a name="examples"></a><span data-ttu-id="553d4-361">例</span><span class="sxs-lookup"><span data-stu-id="553d4-361">Examples</span></span>

### <a name="methods"></a><span data-ttu-id="553d4-362">メソッド</span><span class="sxs-lookup"><span data-stu-id="553d4-362">Methods</span></span>

| <span data-ttu-id="553d4-363">方法</span><span class="sxs-lookup"><span data-stu-id="553d4-363">Method</span></span>                                                    | <span data-ttu-id="553d4-364">説明</span><span class="sxs-lookup"><span data-stu-id="553d4-364">Description</span></span>                                                                                                        |
|-----------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="553d4-365">public str inFieldDelimiter(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="553d4-365">public str inFieldDelimiter(\[str value\])</span></span>                | <span data-ttu-id="553d4-366">TextIO オブジェクトによって表される入力ファイルのフィールド区切り記号に使用される文字を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="553d4-366">Gets or sets the character that is used for the field delimiter of an input file represented by a TextIO object.</span></span>   |
| <span data-ttu-id="553d4-367">public str inRecordDelimiter(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="553d4-367">public str inRecordDelimiter(\[str value\])</span></span>               | <span data-ttu-id="553d4-368">TextIO オブジェクトによって表される入力ファイルのレコード区切り記号に使用される文字を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="553d4-368">Gets or sets the character that is used for the record delimiter of an input file represented by a TextIO object.</span></span>  |
| <span data-ttu-id="553d4-369">public int inRecordLength(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="553d4-369">public int inRecordLength(\[int value\])</span></span>                  | <span data-ttu-id="553d4-370">入力ファイルのレコードの長さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="553d4-370">Gets or sets the record length for an input file.</span></span>                                                                  |
| <span data-ttu-id="553d4-371">public str outFieldDelimiter(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="553d4-371">public str outFieldDelimiter(\[str value\])</span></span>               | <span data-ttu-id="553d4-372">TextIO オブジェクトによって表される出力ファイルのフィールド区切り記号に使用される文字を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="553d4-372">Gets or sets the character that is used for the field delimiter of an output file represented by a TextIO object.</span></span>  |
| <span data-ttu-id="553d4-373">public str outRecordDelimiter(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="553d4-373">public str outRecordDelimiter(\[str value\])</span></span>              | <span data-ttu-id="553d4-374">TextIO オブジェクトによって表される出力ファイルのレコード区切り記号に使用される文字を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="553d4-374">Gets or sets the character that is used for the record delimiter of an output file represented by a TextIO object.</span></span> |
| <span data-ttu-id="553d4-375">public container read()</span><span class="sxs-lookup"><span data-stu-id="553d4-375">public container read()</span></span>                                   | <span data-ttu-id="553d4-376">TextIO オブジェクトから次の完全なレコードを読み取ります。</span><span class="sxs-lookup"><span data-stu-id="553d4-376">Reads the next full record from a TextIO object.</span></span>                                                                   |
| <span data-ttu-id="553d4-377">public IO\_Status status()</span><span class="sxs-lookup"><span data-stu-id="553d4-377">public IO\_Status status()</span></span>                                | <span data-ttu-id="553d4-378">TextIo オブジェクトで実行された最後の操作のステータスを取得します。</span><span class="sxs-lookup"><span data-stu-id="553d4-378">Retrieves the status of the last operation performed on a TextIo object.</span></span>                                           |
| <span data-ttu-id="553d4-379">public boolean write(VarArg values)</span><span class="sxs-lookup"><span data-stu-id="553d4-379">public boolean write(VarArg values)</span></span>                       | <span data-ttu-id="553d4-380">TextIO オブジェクトによって表されるファイルにデータを記述します。</span><span class="sxs-lookup"><span data-stu-id="553d4-380">Writes data to a file represented by a TextIO object.</span></span>                                                              |
| <span data-ttu-id="553d4-381">public boolean writeChar(int int)</span><span class="sxs-lookup"><span data-stu-id="553d4-381">public boolean writeChar(int int)</span></span>                         | <span data-ttu-id="553d4-382">Unicode 文字をファイルに記述します。</span><span class="sxs-lookup"><span data-stu-id="553d4-382">Writes a Unicode character to a file.</span></span>                                                                              |
| <span data-ttu-id="553d4-383">public boolean writeExp(container data)</span><span class="sxs-lookup"><span data-stu-id="553d4-383">public boolean writeExp(container data)</span></span>                   | <span data-ttu-id="553d4-384">TextIO オブジェクトによって表されるファイルにコンテナの内容を記述します。</span><span class="sxs-lookup"><span data-stu-id="553d4-384">Writes the contents of a container to a file represented by a TextIO object.</span></span>                                       |
| <span data-ttu-id="553d4-385">public boolean writeRaw(str data)</span><span class="sxs-lookup"><span data-stu-id="553d4-385">public boolean writeRaw(str data)</span></span>                         | <span data-ttu-id="553d4-386">予約済み。</span><span class="sxs-lookup"><span data-stu-id="553d4-386">Reserved.</span></span>                                                                                                          |
| <span data-ttu-id="553d4-387">public void new(str filename, str mode, \[int codepage\])</span><span class="sxs-lookup"><span data-stu-id="553d4-387">public void new(str filename, str mode, \[int codepage\])</span></span> | <span data-ttu-id="553d4-388">TextIO クラスの新しいインスタンスを作成します。</span><span class="sxs-lookup"><span data-stu-id="553d4-388">Creates a new instance of the TextIO class.</span></span>                                                                        |
| <span data-ttu-id="553d4-389">public void finalize()</span><span class="sxs-lookup"><span data-stu-id="553d4-389">public void finalize()</span></span>                                    | <span data-ttu-id="553d4-390">ファイルを閉じ、データが書き込まれている場合、ファイル バッファーをディスクにフラッシュします。</span><span class="sxs-lookup"><span data-stu-id="553d4-390">Closes the file and, if data was written, flushes the file buffers to disk.</span></span>                                        |

### <a name="method-infielddelimiter"></a><span data-ttu-id="553d4-391">メソッド inFieldDelimiter</span><span class="sxs-lookup"><span data-stu-id="553d4-391">Method inFieldDelimiter</span></span>

<span data-ttu-id="553d4-392">TextIO オブジェクトによって表される入力ファイルのフィールド区切り記号に使用される文字を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="553d4-392">Gets or sets the character that is used for the field delimiter of an input file represented by a TextIO object.</span></span>

    public str inFieldDelimiter([str value])

#### <a name="parameters"></a><span data-ttu-id="553d4-393">パラメーター</span><span class="sxs-lookup"><span data-stu-id="553d4-393">Parameters</span></span>

<span data-ttu-id="553d4-394">値</span><span class="sxs-lookup"><span data-stu-id="553d4-394">value</span></span>  
<span data-ttu-id="553d4-395">フィールドの区切り記号として使用される文字 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="553d4-395">The character to be used as the field delimiter; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="553d4-396">戻り値</span><span class="sxs-lookup"><span data-stu-id="553d4-396">Return Value</span></span>

<span data-ttu-id="553d4-397">フィールドの区切り記号として使用される文字。</span><span class="sxs-lookup"><span data-stu-id="553d4-397">The character used as the field delimiter.</span></span>

#### <a name="remarks"></a><span data-ttu-id="553d4-398">備考</span><span class="sxs-lookup"><span data-stu-id="553d4-398">Remarks</span></span>

<span data-ttu-id="553d4-399">出力ファイルのフィールド区切り記号を設定するには、次を使用します。</span><span class="sxs-lookup"><span data-stu-id="553d4-399">To set the field delimiter for an output file, use</span></span>

#### <a name="examples"></a><span data-ttu-id="553d4-400">例</span><span class="sxs-lookup"><span data-stu-id="553d4-400">Examples</span></span>

<span data-ttu-id="553d4-401">次の例では、入力ファイルのフィールド区切り記号を '\\r\\n' に設定します.</span><span class="sxs-lookup"><span data-stu-id="553d4-401">The following example sets the field delimiter for an input file to '\\r\\n'.</span></span>

    protected void openFile() 
    { 
        #define.delimiter('\r\n') 
        super(); 
        importFile.inFieldDelimiter(#delimiter); 
    }

### <a name="method-inrecorddelimiter"></a><span data-ttu-id="553d4-402">メソッド inRecordDelimiter</span><span class="sxs-lookup"><span data-stu-id="553d4-402">Method inRecordDelimiter</span></span>

<span data-ttu-id="553d4-403">TextIO オブジェクトによって表される入力ファイルのレコード区切り記号に使用される文字を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="553d4-403">Gets or sets the character that is used for the record delimiter of an input file represented by a TextIO object.</span></span>

    public str inRecordDelimiter([str value])

#### <a name="parameters"></a><span data-ttu-id="553d4-404">パラメーター</span><span class="sxs-lookup"><span data-stu-id="553d4-404">Parameters</span></span>

<span data-ttu-id="553d4-405">値</span><span class="sxs-lookup"><span data-stu-id="553d4-405">value</span></span>  
<span data-ttu-id="553d4-406">オプションでレコードの区切り記号として使用される文字。</span><span class="sxs-lookup"><span data-stu-id="553d4-406">The character to be used as the record delimiter; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="553d4-407">戻り値</span><span class="sxs-lookup"><span data-stu-id="553d4-407">Return Value</span></span>

<span data-ttu-id="553d4-408">レコードの区切り記号として使用される文字。</span><span class="sxs-lookup"><span data-stu-id="553d4-408">The character used as the record delimiter.</span></span>

#### <a name="remarks"></a><span data-ttu-id="553d4-409">備考</span><span class="sxs-lookup"><span data-stu-id="553d4-409">Remarks</span></span>

<span data-ttu-id="553d4-410">出力ファイルのレコード区切り記号を設定するには、次を使用します。</span><span class="sxs-lookup"><span data-stu-id="553d4-410">To set the record delimiter for an output file, use the .</span></span>

#### <a name="examples"></a><span data-ttu-id="553d4-411">例</span><span class="sxs-lookup"><span data-stu-id="553d4-411">Examples</span></span>

<span data-ttu-id="553d4-412">次の例では、レコード区切り記号を 128 に設定します。</span><span class="sxs-lookup"><span data-stu-id="553d4-412">The following example sets the record delimiter to 128.</span></span>

    boolean openFile() 
    { 
        boolean ret = false; 
        int     recordLength = 128; 
        int     numOflastCharacter = 255; 
        textFile = new TextIo(filename, 'r'); 
        if (textFile) 
        { 
            if (textFile.status()) 
            { 
                throw error("@SYS52680"); 
            } 
            textFile.inFieldDelimiter(num2char(numOflastCharacter)); 
            textFile.inRecordDelimiter(num2char(numOflastCharacter)); 
            textFile.inRecordLength(recordLength); 
            ret = true; 
        } 
        return ret; 
    }

### <a name="method-inrecordlength"></a><span data-ttu-id="553d4-413">メソッド inRecordLength</span><span class="sxs-lookup"><span data-stu-id="553d4-413">Method inRecordLength</span></span>

<span data-ttu-id="553d4-414">入力ファイルのレコードの長さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="553d4-414">Gets or sets the record length for an input file.</span></span>

    public int inRecordLength([int value])

#### <a name="parameters"></a><span data-ttu-id="553d4-415">パラメーター</span><span class="sxs-lookup"><span data-stu-id="553d4-415">Parameters</span></span>

<span data-ttu-id="553d4-416">値</span><span class="sxs-lookup"><span data-stu-id="553d4-416">value</span></span>  
<span data-ttu-id="553d4-417">入力ファイルのレコードの長さ (オプション)。</span><span class="sxs-lookup"><span data-stu-id="553d4-417">The record length for the input file; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="553d4-418">戻り値</span><span class="sxs-lookup"><span data-stu-id="553d4-418">Return Value</span></span>

<span data-ttu-id="553d4-419">入力ファイルのレコードの長さ。</span><span class="sxs-lookup"><span data-stu-id="553d4-419">The record length for the input file.</span></span>

#### <a name="remarks"></a><span data-ttu-id="553d4-420">備考</span><span class="sxs-lookup"><span data-stu-id="553d4-420">Remarks</span></span>

<span data-ttu-id="553d4-421">固定長形式になっているファイルについては、inRecordLength プロパティを使用して、各レコードに対して指定された文字数以上が読み取られていないことを確認します。</span><span class="sxs-lookup"><span data-stu-id="553d4-421">For files that have a fixed-length format, use the inRecordLength property to ensure that no more than the specified number of characters are read for each record.</span></span> <span data-ttu-id="553d4-422">レコード フォーマットが指定された inRecordDelimiter プロパティ値で上書きされた場合、つまり、固定長が読み込まれる前に inRecordDelimiter 値が満たされている場合)、レコードは受け入れられ、追加のデータは読み込まれません。</span><span class="sxs-lookup"><span data-stu-id="553d4-422">If the record format is overruled by a specified inRecordDelimiter property value, that is the inRecordDelimiter value is met before the fixed length is read, the record is accepted, and no further data is read.</span></span> <span data-ttu-id="553d4-423">固定数の文字を確実に読み取るには、inRecordDelimiter プロパティ値を空の文字列に設定します。</span><span class="sxs-lookup"><span data-stu-id="553d4-423">To ensure that a fixed number of characters are read, set the inRecordDelimiter property value to an empty string.</span></span> <span data-ttu-id="553d4-424">inRecordDelimiter プロパティ値が見つからない場合、inRecordDelimiter プロパティ値は読み取れる最大文字数になります。</span><span class="sxs-lookup"><span data-stu-id="553d4-424">When no inRecordDelimiter property value is found, the inRecordDelimiter property value is the maximum limit of characters to read.</span></span> <span data-ttu-id="553d4-425">レコードの長さチェックを無効にするには、inRecordDelimiter プロパティ値をゼロに設定します。</span><span class="sxs-lookup"><span data-stu-id="553d4-425">Set the inRecordDelimiter property value to zero to disable the record length check.</span></span>

#### <a name="examples"></a><span data-ttu-id="553d4-426">例</span><span class="sxs-lookup"><span data-stu-id="553d4-426">Examples</span></span>

<span data-ttu-id="553d4-427">次の例では、レコードの長さを 128 に設定します。</span><span class="sxs-lookup"><span data-stu-id="553d4-427">The following example sets the record length to 128.</span></span>

    boolean openFile() 
    { 
        boolean ret = false; 
        int     recordLength = 128; 
        int     numOflastCharacter = 255; 
        textFile = new TextIo(filename, 'r'); 
        if (textFile) 
        { 
            if (textFile.status()) 
            { 
                throw error("@SYS52680"); 
            } 
            textFile.inFieldDelimiter(num2char(numOflastCharacter)); 
            textFile.inRecordDelimiter(num2char(numOflastCharacter)); 
            textFile.inRecordLength(recordLength); 
            ret = true; 
        } 
        return ret; 
    }

### <a name="method-outfielddelimiter"></a><span data-ttu-id="553d4-428">メソッド outFieldDelimiter</span><span class="sxs-lookup"><span data-stu-id="553d4-428">Method outFieldDelimiter</span></span>

<span data-ttu-id="553d4-429">TextIO オブジェクトによって表される出力ファイルのフィールド区切り記号に使用される文字を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="553d4-429">Gets or sets the character that is used for the field delimiter of an output file represented by a TextIO object.</span></span>

    public str outFieldDelimiter([str value])

#### <a name="parameters"></a><span data-ttu-id="553d4-430">パラメーター</span><span class="sxs-lookup"><span data-stu-id="553d4-430">Parameters</span></span>

<span data-ttu-id="553d4-431">値</span><span class="sxs-lookup"><span data-stu-id="553d4-431">value</span></span>  
<span data-ttu-id="553d4-432">フィールドの区切り記号として使用される文字 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="553d4-432">The character to be used as the field delimiter; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="553d4-433">戻り値</span><span class="sxs-lookup"><span data-stu-id="553d4-433">Return Value</span></span>

<span data-ttu-id="553d4-434">フィールドの区切り記号として使用される文字。</span><span class="sxs-lookup"><span data-stu-id="553d4-434">The character used as the field delimiter.</span></span>

#### <a name="remarks"></a><span data-ttu-id="553d4-435">備考</span><span class="sxs-lookup"><span data-stu-id="553d4-435">Remarks</span></span>

<span data-ttu-id="553d4-436">入力ファイルのフィールド区切り記号を設定するには、次を使用します。</span><span class="sxs-lookup"><span data-stu-id="553d4-436">To set the field delimiter for an input file, use the .</span></span>

#### <a name="examples"></a><span data-ttu-id="553d4-437">例</span><span class="sxs-lookup"><span data-stu-id="553d4-437">Examples</span></span>

<span data-ttu-id="553d4-438">次の例では、出力ファイルのフィールド区切り記号を ' ' (なし) に設定します。</span><span class="sxs-lookup"><span data-stu-id="553d4-438">The following example sets the field delimiter to ' ' (nothing) for an output file.</span></span>

    void defineFile() 
    { 
        diskFile = new TextIo(diskFileName,'W'); 
        if (!diskFile) 
        { 
            throw error("@SYS26757"); 
        } 
        diskFile.outRecordDelimiter('\r\n'); 
        diskFile.outFieldDelimiter(''); 
    }

### <a name="method-outrecorddelimiter"></a><span data-ttu-id="553d4-439">メソッド outRecordDelimiter</span><span class="sxs-lookup"><span data-stu-id="553d4-439">Method outRecordDelimiter</span></span>

<span data-ttu-id="553d4-440">TextIO オブジェクトによって表される出力ファイルのレコード区切り記号に使用される文字を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="553d4-440">Gets or sets the character that is used for the record delimiter of an output file represented by a TextIO object.</span></span>

    public str outRecordDelimiter([str value])

#### <a name="parameters"></a><span data-ttu-id="553d4-441">パラメーター</span><span class="sxs-lookup"><span data-stu-id="553d4-441">Parameters</span></span>

<span data-ttu-id="553d4-442">値</span><span class="sxs-lookup"><span data-stu-id="553d4-442">value</span></span>  
<span data-ttu-id="553d4-443">オプションでレコードの区切り記号として使用される文字。</span><span class="sxs-lookup"><span data-stu-id="553d4-443">The character to be used as the record delimiter; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="553d4-444">戻り値</span><span class="sxs-lookup"><span data-stu-id="553d4-444">Return Value</span></span>

<span data-ttu-id="553d4-445">レコードの区切り記号として使用される文字。</span><span class="sxs-lookup"><span data-stu-id="553d4-445">The character used as the record delimiter.</span></span>

#### <a name="remarks"></a><span data-ttu-id="553d4-446">備考</span><span class="sxs-lookup"><span data-stu-id="553d4-446">Remarks</span></span>

<span data-ttu-id="553d4-447">入力ファイルのレコード区切り記号を設定するには、次を使用します。</span><span class="sxs-lookup"><span data-stu-id="553d4-447">To set the record delimiter for an input file, use the .</span></span>

#### <a name="examples"></a><span data-ttu-id="553d4-448">例</span><span class="sxs-lookup"><span data-stu-id="553d4-448">Examples</span></span>

<span data-ttu-id="553d4-449">次の例では、出力ファイルのレコード区切り記号を '\\r\\n'' に設定します。</span><span class="sxs-lookup"><span data-stu-id="553d4-449">The following example sets the record delimiter for an output file to '\\r\\n'.</span></span>

    void defineFile() 
    { 
        diskFile = new TextIo(diskFileName,'W'); 
        if (!diskFile) 
        { 
            throw error("@SYS26757"); 
        } 
        diskFile.outRecordDelimiter('\r\n'); 
        diskFile.outFieldDelimiter(''); 
    }

### <a name="method-read"></a><span data-ttu-id="553d4-450">メソッド read</span><span class="sxs-lookup"><span data-stu-id="553d4-450">Method read</span></span>

<span data-ttu-id="553d4-451">TextIO オブジェクトから次の完全なレコードを読み取ります。</span><span class="sxs-lookup"><span data-stu-id="553d4-451">Reads the next full record from a TextIO object.</span></span>

    public container read()

#### <a name="return-value"></a><span data-ttu-id="553d4-452">戻り値</span><span class="sxs-lookup"><span data-stu-id="553d4-452">Return Value</span></span>

<span data-ttu-id="553d4-453">1 つのレコードを保持するコンテナーです。</span><span class="sxs-lookup"><span data-stu-id="553d4-453">A container that holds one record.</span></span>

#### <a name="remarks"></a><span data-ttu-id="553d4-454">備考</span><span class="sxs-lookup"><span data-stu-id="553d4-454">Remarks</span></span>

<span data-ttu-id="553d4-455">コンテナー内の各エントリは、レコードの 1 つのフィールドと同じです。</span><span class="sxs-lookup"><span data-stu-id="553d4-455">Each entry in the container equals one field in the record.</span></span> <span data-ttu-id="553d4-456">次の完全なレコードの定義は、次のプロパティ、inFieldDelimiter、inRecordDelimiter、および inRecordLength プロパティによって制御されます。</span><span class="sxs-lookup"><span data-stu-id="553d4-456">The definition of the next full record is controlled by the inFieldDelimiter, inRecordDelimiter, and inRecordLength properties.</span></span> <span data-ttu-id="553d4-457">これらのプロパティには、最も一般的な形式の入力と出力を可能にする既定値があります。</span><span class="sxs-lookup"><span data-stu-id="553d4-457">These properties have default values that allow input and output of the most common formats.</span></span> <span data-ttu-id="553d4-458">inFieldDelimiter、inRecordDelimiter、および inRecordLength メソッドを使用して、プロパティを調整する必要がある場合があります。</span><span class="sxs-lookup"><span data-stu-id="553d4-458">It might be necessary to adjust the properties by using the inFieldDelimiter, inRecordDelimiter, and inRecordLength methods.</span></span>

#### <a name="examples"></a><span data-ttu-id="553d4-459">例</span><span class="sxs-lookup"><span data-stu-id="553d4-459">Examples</span></span>

<span data-ttu-id="553d4-460">次の例では、ファイルからレコードを読み取り、conpeek 関数を使用してレコードから値を抽出します。</span><span class="sxs-lookup"><span data-stu-id="553d4-460">The following example reads a record from a file and uses the conpeek function to extract values from the record.</span></span>

    public void run() 
    { 
        container         fileRecord; 
        IntrastatToProdCom intrastatToProdCom; 
        if (filename) 
        { 
            this.initializeFile(); 
            fileRecord = prodComFile.read(); 
            ttsbegin; 
            while (fileRecord) 
            { 
                intrastatToProdCom.IntrastatItemCodeID = conpeek(fileRecord, 1); 
                intrastatToProdCom.InventProdComCodeID = conpeek (fileRecord, 2); 
                intrastatToProdCom.ValidFromYear = conpeek (fileRecord, 3); 
                intrastatToProdCom.ValidTillYear = conpeek (fileRecord, 4); 
                intrastatToProdCom.insert(); 
                filerecord = prodComFile.read(); 
            } 
            ttscommit; 
        } 
    }

### <a name="method-status"></a><span data-ttu-id="553d4-461">メソッド status</span><span class="sxs-lookup"><span data-stu-id="553d4-461">Method status</span></span>

<span data-ttu-id="553d4-462">TextIo オブジェクトで実行された最後の操作のステータスを取得します。</span><span class="sxs-lookup"><span data-stu-id="553d4-462">Retrieves the status of the last operation performed on a TextIo object.</span></span>

    public IO_Status status()

#### <a name="return-value"></a><span data-ttu-id="553d4-463">戻り値</span><span class="sxs-lookup"><span data-stu-id="553d4-463">Return Value</span></span>

<span data-ttu-id="553d4-464">最後の操作の状態。</span><span class="sxs-lookup"><span data-stu-id="553d4-464">The status of the last operation.</span></span>

#### <a name="examples"></a><span data-ttu-id="553d4-465">例</span><span class="sxs-lookup"><span data-stu-id="553d4-465">Examples</span></span>

<span data-ttu-id="553d4-466">次の例では、ファイルが存在しない場合、またはファイルの最後の操作が、IO\_Status::Ok 列挙値のステータスを持たない場合にエラーをスローします。</span><span class="sxs-lookup"><span data-stu-id="553d4-466">The following example throws an error if a file does not exist or if the last operation on the file did not have a status of the IO\_Status::Ok enumeration value.</span></span>

    protected void checkDiskFileStatus() 
    { 
        if (!diskFile || diskFile.status() != IO_Status::Ok) 
        { 
            throw error(strfmt("@SYS76826", diskFileName)); 
        } 
    }

### <a name="method-write"></a><span data-ttu-id="553d4-467">メソッド write</span><span class="sxs-lookup"><span data-stu-id="553d4-467">Method write</span></span>

<span data-ttu-id="553d4-468">TextIO オブジェクトによって表されるファイルにデータを記述します。</span><span class="sxs-lookup"><span data-stu-id="553d4-468">Writes data to a file represented by a TextIO object.</span></span>

    public boolean write(VarArg values)

#### <a name="parameters"></a><span data-ttu-id="553d4-469">パラメーター</span><span class="sxs-lookup"><span data-stu-id="553d4-469">Parameters</span></span>

<span data-ttu-id="553d4-470">値</span><span class="sxs-lookup"><span data-stu-id="553d4-470">values</span></span>  
<span data-ttu-id="553d4-471">ファイルに書き込む値。</span><span class="sxs-lookup"><span data-stu-id="553d4-471">The values to write to the file.</span></span> <span data-ttu-id="553d4-472">値はさまざまなデータ型にすることができます。</span><span class="sxs-lookup"><span data-stu-id="553d4-472">The values can be of different data types.</span></span>

#### <a name="return-value"></a><span data-ttu-id="553d4-473">戻り値</span><span class="sxs-lookup"><span data-stu-id="553d4-473">Return Value</span></span>

<span data-ttu-id="553d4-474">書き込み操作が成功する場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="553d4-474">true if the write operation succeeds; otherwise, false.</span></span>

#### <a name="remarks"></a><span data-ttu-id="553d4-475">備考</span><span class="sxs-lookup"><span data-stu-id="553d4-475">Remarks</span></span>

<span data-ttu-id="553d4-476">書き込み操作が失敗した場合は、その原因を突き止めるために使用できます。</span><span class="sxs-lookup"><span data-stu-id="553d4-476">If the write operation fails, can be used to ascertain the cause.</span></span> <span data-ttu-id="553d4-477">書き込みメソッドは、可変数の引数を受け入れます。</span><span class="sxs-lookup"><span data-stu-id="553d4-477">The write method accepts a variable number of arguments.</span></span> <span data-ttu-id="553d4-478">各値は、フィールドとして出力レコードに配置されます。</span><span class="sxs-lookup"><span data-stu-id="553d4-478">Each value is put into the output record as a field.</span></span> <span data-ttu-id="553d4-479">フィールドは、で指定されたフィールド区切り記号で区切られます。</span><span class="sxs-lookup"><span data-stu-id="553d4-479">The fields are separated by the field delimiter specified by the .</span></span> <span data-ttu-id="553d4-480">各レコードは、によって指定された区切り記号で区切られます。</span><span class="sxs-lookup"><span data-stu-id="553d4-480">Each record is separated by the delimiter specified by the .</span></span> <span data-ttu-id="553d4-481">完全なコンテナーを書き込むには、次を使用します。</span><span class="sxs-lookup"><span data-stu-id="553d4-481">To write complete containers, use the .</span></span>

### <a name="method-writechar"></a><span data-ttu-id="553d4-482">メソッド writeChar</span><span class="sxs-lookup"><span data-stu-id="553d4-482">Method writeChar</span></span>

<span data-ttu-id="553d4-483">Unicode 文字をファイルに記述します。</span><span class="sxs-lookup"><span data-stu-id="553d4-483">Writes a Unicode character to a file.</span></span>

    public boolean writeChar(int int)

#### <a name="parameters"></a><span data-ttu-id="553d4-484">パラメーター</span><span class="sxs-lookup"><span data-stu-id="553d4-484">Parameters</span></span>

<span data-ttu-id="553d4-485">int</span><span class="sxs-lookup"><span data-stu-id="553d4-485">int</span></span>  

#### <a name="return-value"></a><span data-ttu-id="553d4-486">戻り値</span><span class="sxs-lookup"><span data-stu-id="553d4-486">Return Value</span></span>

<span data-ttu-id="553d4-487">書き込み操作が成功する場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="553d4-487">true if the write operation succeeds; otherwise, false.</span></span>

#### <a name="remarks"></a><span data-ttu-id="553d4-488">備考</span><span class="sxs-lookup"><span data-stu-id="553d4-488">Remarks</span></span>

<span data-ttu-id="553d4-489">書き込み操作が失敗した場合は、原因を突き止めるために TextIO.status メソッドを使用することができます。</span><span class="sxs-lookup"><span data-stu-id="553d4-489">If the write operation fails, the TextIO.status method can be used to check for the cause.</span></span> <span data-ttu-id="553d4-490">複数の値を書き込んだり、さまざまな種類のデータをファイルに書き込むには、TextIO.write メソッドを使用します。</span><span class="sxs-lookup"><span data-stu-id="553d4-490">To write multiple values or to write data of different types to a file, use the TextIO.write method.</span></span>

### <a name="method-writeexp"></a><span data-ttu-id="553d4-491">メソッド writeExp</span><span class="sxs-lookup"><span data-stu-id="553d4-491">Method writeExp</span></span>

<span data-ttu-id="553d4-492">TextIO オブジェクトによって表されるファイルにコンテナの内容を記述します。</span><span class="sxs-lookup"><span data-stu-id="553d4-492">Writes the contents of a container to a file represented by a TextIO object.</span></span>

    public boolean writeExp(container data)

#### <a name="parameters"></a><span data-ttu-id="553d4-493">パラメーター</span><span class="sxs-lookup"><span data-stu-id="553d4-493">Parameters</span></span>

<span data-ttu-id="553d4-494">データ</span><span class="sxs-lookup"><span data-stu-id="553d4-494">data</span></span>  
<span data-ttu-id="553d4-495">ファイルへの書き込みのデータを持つコンテナーです。</span><span class="sxs-lookup"><span data-stu-id="553d4-495">The container that has data to write to the file.</span></span>

#### <a name="return-value"></a><span data-ttu-id="553d4-496">戻り値</span><span class="sxs-lookup"><span data-stu-id="553d4-496">Return Value</span></span>

<span data-ttu-id="553d4-497">書き込み操作が成功する場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="553d4-497">true if the write operation succeeds; otherwise, false.</span></span>

#### <a name="remarks"></a><span data-ttu-id="553d4-498">備考</span><span class="sxs-lookup"><span data-stu-id="553d4-498">Remarks</span></span>

<span data-ttu-id="553d4-499">書き込み操作が失敗した場合は、原因を突き止めるために TextIO.status メソッドを使用することができます。</span><span class="sxs-lookup"><span data-stu-id="553d4-499">If the write operation fails, the TextIo.status Method can be used to ascertain the cause.</span></span> <span data-ttu-id="553d4-500">コンテナー内のエントリは、outFieldDelimiter メソッドで設定された区切り文字で区切られます。</span><span class="sxs-lookup"><span data-stu-id="553d4-500">Entries in the container are separated by the delimiter set by the outFieldDelimiter method.</span></span> <span data-ttu-id="553d4-501">コンテナーは、outRecordDelimiter メソッドで設定された区切り文字で区切られます。</span><span class="sxs-lookup"><span data-stu-id="553d4-501">Containers are separated by the delimiter set by the outRecordDelimiter method.</span></span>

### <a name="method-writeraw"></a><span data-ttu-id="553d4-502">メソッド writeRaw</span><span class="sxs-lookup"><span data-stu-id="553d4-502">Method writeRaw</span></span>

<span data-ttu-id="553d4-503">予約済み。</span><span class="sxs-lookup"><span data-stu-id="553d4-503">Reserved.</span></span>

    public boolean writeRaw(str data)

#### <a name="parameters"></a><span data-ttu-id="553d4-504">パラメーター</span><span class="sxs-lookup"><span data-stu-id="553d4-504">Parameters</span></span>

<span data-ttu-id="553d4-505">データ</span><span class="sxs-lookup"><span data-stu-id="553d4-505">data</span></span>  

#### <a name="return-value"></a><span data-ttu-id="553d4-506">戻り値</span><span class="sxs-lookup"><span data-stu-id="553d4-506">Return Value</span></span>

### <a name="method-new"></a><span data-ttu-id="553d4-507">メソッド new</span><span class="sxs-lookup"><span data-stu-id="553d4-507">Method new</span></span>

<span data-ttu-id="553d4-508">TextIO クラスの新しいインスタンスを作成します。</span><span class="sxs-lookup"><span data-stu-id="553d4-508">Creates a new instance of the TextIO class.</span></span>

    public void new(str filename, str mode, [int codepage])

#### <a name="parameters"></a><span data-ttu-id="553d4-509">パラメーター</span><span class="sxs-lookup"><span data-stu-id="553d4-509">Parameters</span></span>

<span data-ttu-id="553d4-510">filename</span><span class="sxs-lookup"><span data-stu-id="553d4-510">filename</span></span>  
<span data-ttu-id="553d4-511">ファイルから読み込まれる、またはファイルに書き込まれる文字セットのコード ページ番号。</span><span class="sxs-lookup"><span data-stu-id="553d4-511">The code page number for the character set to be read from or written to the file.</span></span> <span data-ttu-id="553d4-512">既定値は 1200 (UTF-16LE) です。</span><span class="sxs-lookup"><span data-stu-id="553d4-512">The default value is 1200 (UTF-16LE).</span></span> <span data-ttu-id="553d4-513">このパラメーターはオプションです。</span><span class="sxs-lookup"><span data-stu-id="553d4-513">This parameter is optional.</span></span> <span data-ttu-id="553d4-514">以下に示す値は、最も一般的な値です。これらのオプションの詳細については、 [the list](https://go.microsoft.com/fwlink/?LinkID=78282&clcid=0x409)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="553d4-514">Following are the most common values: For more information about these options, see [the list](https://go.microsoft.com/fwlink/?LinkID=78282&clcid=0x409).</span></span> <span data-ttu-id="553d4-515">無効なコード ページが要求された場合にエラーが報告されます。</span><span class="sxs-lookup"><span data-stu-id="553d4-515">An error is reported if an invalid code page is requested.</span></span> <span data-ttu-id="553d4-516">コンピューターにインストールされていない場合、コード ページは「無効」としてレポートされることに注意します (さまざまなコード ページがクライアントとサーバーにインストールされている場合があります)。</span><span class="sxs-lookup"><span data-stu-id="553d4-516">Notice that a code page is reported as "invalid" if it is not installed on the computer (different code pages may be installed on the client and server).</span></span> <span data-ttu-id="553d4-517">たとえば、コンピューターの ACP がギリシャ語でない、またはギリシャ語のサポートがコントロール パネル &gt;地域オプションを使用して読み込まれない限り、ギリシャ語のコード ページ 1253 の指定は失敗します。</span><span class="sxs-lookup"><span data-stu-id="553d4-517">For example, specifying code page 1253 for Greek fails unless the computer's ACP is Greek or Greek language support has been loaded by using Control Panel &gt; Regional Options.</span></span>

<!-- -->

<span data-ttu-id="553d4-518">モード</span><span class="sxs-lookup"><span data-stu-id="553d4-518">mode</span></span>  
<span data-ttu-id="553d4-519">ファイルから読み込まれる、またはファイルに書き込まれる文字セットのコード ページ番号。</span><span class="sxs-lookup"><span data-stu-id="553d4-519">The code page number for the character set to be read from or written to the file.</span></span> <span data-ttu-id="553d4-520">既定値は 1200 (UTF-16LE) です。</span><span class="sxs-lookup"><span data-stu-id="553d4-520">The default value is 1200 (UTF-16LE).</span></span> <span data-ttu-id="553d4-521">このパラメーターはオプションです。</span><span class="sxs-lookup"><span data-stu-id="553d4-521">This parameter is optional.</span></span> <span data-ttu-id="553d4-522">以下に示す値は、最も一般的な値です。これらのオプションの詳細については、 [the list](https://go.microsoft.com/fwlink/?LinkID=78282&clcid=0x409)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="553d4-522">Following are the most common values: For more information about these options, see [the list](https://go.microsoft.com/fwlink/?LinkID=78282&clcid=0x409).</span></span> <span data-ttu-id="553d4-523">無効なコード ページが要求された場合にエラーが報告されます。</span><span class="sxs-lookup"><span data-stu-id="553d4-523">An error is reported if an invalid code page is requested.</span></span> <span data-ttu-id="553d4-524">コンピューターにインストールされていない場合、コード ページは「無効」としてレポートされることに注意します (さまざまなコード ページがクライアントとサーバーにインストールされている場合があります)。</span><span class="sxs-lookup"><span data-stu-id="553d4-524">Notice that a code page is reported as "invalid" if it is not installed on the computer (different code pages may be installed on the client and server).</span></span> <span data-ttu-id="553d4-525">たとえば、コンピューターの ACP がギリシャ語でない、またはギリシャ語のサポートがコントロール パネル &gt;地域オプションを使用して読み込まれない限り、ギリシャ語のコード ページ 1253 の指定は失敗します。</span><span class="sxs-lookup"><span data-stu-id="553d4-525">For example, specifying code page 1253 for Greek fails unless the computer's ACP is Greek or Greek language support has been loaded by using Control Panel &gt; Regional Options.</span></span>

<!-- -->

<span data-ttu-id="553d4-526">codepage</span><span class="sxs-lookup"><span data-stu-id="553d4-526">codepage</span></span>  
<span data-ttu-id="553d4-527">ファイルから読み込まれる、またはファイルに書き込まれる文字セットのコード ページ番号。</span><span class="sxs-lookup"><span data-stu-id="553d4-527">The code page number for the character set to be read from or written to the file.</span></span> <span data-ttu-id="553d4-528">既定値は 1200 (UTF-16LE) です。</span><span class="sxs-lookup"><span data-stu-id="553d4-528">The default value is 1200 (UTF-16LE).</span></span> <span data-ttu-id="553d4-529">このパラメーターはオプションです。</span><span class="sxs-lookup"><span data-stu-id="553d4-529">This parameter is optional.</span></span> <span data-ttu-id="553d4-530">以下に示す値は、最も一般的な値です。これらのオプションの詳細については、 [the list](https://go.microsoft.com/fwlink/?LinkID=78282&clcid=0x409)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="553d4-530">Following are the most common values: For more information about these options, see [the list](https://go.microsoft.com/fwlink/?LinkID=78282&clcid=0x409).</span></span> <span data-ttu-id="553d4-531">無効なコード ページが要求された場合にエラーが報告されます。</span><span class="sxs-lookup"><span data-stu-id="553d4-531">An error is reported if an invalid code page is requested.</span></span> <span data-ttu-id="553d4-532">コンピューターにインストールされていない場合、コード ページは「無効」としてレポートされることに注意します (さまざまなコード ページがクライアントとサーバーにインストールされている場合があります)。</span><span class="sxs-lookup"><span data-stu-id="553d4-532">Notice that a code page is reported as "invalid" if it is not installed on the computer (different code pages may be installed on the client and server).</span></span> <span data-ttu-id="553d4-533">たとえば、コンピューターの ACP がギリシャ語でない、またはギリシャ語のサポートがコントロール パネル &gt;地域オプションを使用して読み込まれない限り、ギリシャ語のコード ページ 1253 の指定は失敗します。</span><span class="sxs-lookup"><span data-stu-id="553d4-533">For example, specifying code page 1253 for Greek fails unless the computer's ACP is Greek or Greek language support has been loaded by using Control Panel &gt; Regional Options.</span></span>

#### <a name="remarks"></a><span data-ttu-id="553d4-534">備考</span><span class="sxs-lookup"><span data-stu-id="553d4-534">Remarks</span></span>

<span data-ttu-id="553d4-535">ランタイム エラーは、現在開いているモードに対応しないメソッドでファイルにアクセスすると発生します (たとえば、読み取りモード ファイルに書き込もうとした場合など)。</span><span class="sxs-lookup"><span data-stu-id="553d4-535">A run-time error occurs if the file is accessed with a method that does not correspond to the current opened mode (for example, you try to write to a read-mode file).</span></span> <span data-ttu-id="553d4-536">攻撃者が新しいメソッドへの入力を制御できる場合、セキュリティ上のリスクが存在します。</span><span class="sxs-lookup"><span data-stu-id="553d4-536">If an attacker can control input to the new method, a security risk exists.</span></span> <span data-ttu-id="553d4-537">このメソッドは、コード アクセス セキュリティで実行されます。</span><span class="sxs-lookup"><span data-stu-id="553d4-537">This method runs under Code Access Security.</span></span> <span data-ttu-id="553d4-538">サーバー上でこのメソッドを呼び出すには、FileIoPermission クラスからのアクセス許可が必要です。</span><span class="sxs-lookup"><span data-stu-id="553d4-538">Calls to this method on the server require permission from the FileIoPermission class.</span></span> <span data-ttu-id="553d4-539">ユーザーがこのメソッドを呼び出すコントロールで、SysDevelopment へのセキュリティ キーを設定して開発権限があることを確認します。</span><span class="sxs-lookup"><span data-stu-id="553d4-539">Ensure that the user has development privileges by setting the security key to SysDevelopment on the control that calls this method.</span></span> <span data-ttu-id="553d4-540">次のテーブルは、\_codePage パラメーターに指定できる、より一般的なコード ページの一部を示しています。</span><span class="sxs-lookup"><span data-stu-id="553d4-540">The following table describes some of the more common code pages that might be specified for the \_codePage parameter.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="553d4-541">0</span><span class="sxs-lookup"><span data-stu-id="553d4-541">0</span></span></td>
<td><span data-ttu-id="553d4-542">ANSI コード ページ (ACP)</span><span class="sxs-lookup"><span data-stu-id="553d4-542">ANSI code page (ACP)</span></span></td>
<td><span data-ttu-id="553d4-543">ユーザー&#39;の現在の言語の文字のみをサポートするコード ページ。</span><span class="sxs-lookup"><span data-stu-id="553d4-543">The code page that supports only characters in the user&#39;s current language.</span></span> <span data-ttu-id="553d4-544">コード ページは、多言語データを含む可能性のあるものや、異なるコード ページを使用して 2 つのシステム間で転送される単一言語データ用には適していません。</span><span class="sxs-lookup"><span data-stu-id="553d4-544">The code page is unsuitable for anything that might contain multilingual data or for monolingual data that might be transferred between two systems by using different code pages.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="553d4-545">437</span><span class="sxs-lookup"><span data-stu-id="553d4-545">437</span></span></td>
<td><span data-ttu-id="553d4-546">OEM コード ページ 437</span><span class="sxs-lookup"><span data-stu-id="553d4-546">OEM code page 437</span></span></td>
<td><span data-ttu-id="553d4-547">IBM PC または MS-DOS コード ページ 437。</span><span class="sxs-lookup"><span data-stu-id="553d4-547">The IBM PC or MS-DOS code page 437.</span></span> <span data-ttu-id="553d4-548">これは、CP437 と省略されることが多く、DOS-US や OEM-US とも呼ばれます。</span><span class="sxs-lookup"><span data-stu-id="553d4-548">It is often abbreviated as CP437 and also called DOS-US or OEM-US.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="553d4-549">850</span><span class="sxs-lookup"><span data-stu-id="553d4-549">850</span></span></td>
<td><span data-ttu-id="553d4-550">コード ページ 850</span><span class="sxs-lookup"><span data-stu-id="553d4-550">Code page 850</span></span></td>
<td><span data-ttu-id="553d4-551">西ヨーロッパで MS-DOS などのオペレーティング システムで使用されていたコード ページ。</span><span class="sxs-lookup"><span data-stu-id="553d4-551">A code page that was used in Western Europe running on operating systems, such as MS-DOS.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="553d4-552">1200</span><span class="sxs-lookup"><span data-stu-id="553d4-552">1200</span></span></td>
<td><span data-ttu-id="553d4-553">UTF-16LE</span><span class="sxs-lookup"><span data-stu-id="553d4-553">UTF-16LE</span></span></td>
<td><span data-ttu-id="553d4-554">Microsoft Windows x86 システムでのネイティブ Unicode 表現。</span><span class="sxs-lookup"><span data-stu-id="553d4-554">The native Unicode representation on Microsoft Windows x86 systems.</span></span> <span data-ttu-id="553d4-555">ほとんどすべての文字は 16 ビットとして保存されます。</span><span class="sxs-lookup"><span data-stu-id="553d4-555">Almost all characters are stored as 16 bit.</span></span> <span data-ttu-id="553d4-556">一部の中国語文字には、32 ビットが必要です。</span><span class="sxs-lookup"><span data-stu-id="553d4-556">Some Chinese characters require 32 bit.</span></span> <span data-ttu-id="553d4-557">文字の残りの部分を読み取ると、識別バイト オーダー マークが書き込まれ、検査され、次に破棄されます。</span><span class="sxs-lookup"><span data-stu-id="553d4-557">An identifying byte-order mark is written, examined, and then discarded when the rest of the character is read.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="553d4-558">1201</span><span class="sxs-lookup"><span data-stu-id="553d4-558">1201</span></span></td>
<td><span data-ttu-id="553d4-559">UTF-16BE</span><span class="sxs-lookup"><span data-stu-id="553d4-559">UTF-16BE</span></span></td>
<td><span data-ttu-id="553d4-560">UTF-16LE と同じですが、バイトスワップします。</span><span class="sxs-lookup"><span data-stu-id="553d4-560">The same as UTF-16LE but byte-swapped.</span></span> <span data-ttu-id="553d4-561">下位から上位ではなく左から右へバイトを格納する x86 以外のシステムとの互換性のために使用されます。</span><span class="sxs-lookup"><span data-stu-id="553d4-561">Used for compatibility with some non-x86 systems, which store bytes from left-to-right instead of low-order to high-order.</span></span> <span data-ttu-id="553d4-562">文字の残りの部分を読み取ると、識別バイト オーダー マークが最初に書き込まれ、検査され、次に破棄されます。</span><span class="sxs-lookup"><span data-stu-id="553d4-562">An identifying byte-order mark is written first, examined, and then discarded when the rest of the character is read.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="553d4-563">65001</span><span class="sxs-lookup"><span data-stu-id="553d4-563">65001</span></span></td>
<td><span data-ttu-id="553d4-564">UTF-8</span><span class="sxs-lookup"><span data-stu-id="553d4-564">UTF-8</span></span></td>
<td><span data-ttu-id="553d4-565">バイト ストリームしやすい方法で Unicode を保存します。</span><span class="sxs-lookup"><span data-stu-id="553d4-565">Stores Unicode in a byte-stream–friendly way:</span></span>
<ul>
<li><span data-ttu-id="553d4-566">ASCII 文字は、1 バイトです。</span><span class="sxs-lookup"><span data-stu-id="553d4-566">ASCII characters are 1 byte</span></span></li>
<li><span data-ttu-id="553d4-567">欧州のアルファベット (基本分音記号を含む) は文字あたり 2 バイト</span><span class="sxs-lookup"><span data-stu-id="553d4-567">European alphabets (including basic diacritics) are 2 bytes per character</span></span></li>
<li><span data-ttu-id="553d4-568">中国語、日本語、韓国語の場合、文字あたり 3 バイト必要</span><span class="sxs-lookup"><span data-stu-id="553d4-568">Chinese, Japanese, and Korean require 3 bytes per character</span></span></li>
</ul>
<span data-ttu-id="553d4-569">このコード ページは、ファイルに含まれているASCIIの割合が非常に高く、その他の文字が比較的少なく、スペースを節約することが重要な場合に適しています。</span><span class="sxs-lookup"><span data-stu-id="553d4-569">This code page is a good choice when a file contains a very high percentage of ASCII, relatively few other characters, and it is important to save space.</span></span> <span data-ttu-id="553d4-570">たとえば、.xpo ファイルは、UTF-8 に格納されます。</span><span class="sxs-lookup"><span data-stu-id="553d4-570">For example, .xpo files are stored in UTF-8.</span></span> <span data-ttu-id="553d4-571">UTF-8 ファイルは、3 バイトのバイト順序マーク列で始まり、この項目が最初に書き込まれます。</span><span class="sxs-lookup"><span data-stu-id="553d4-571">UTF-8 files begin with a 3-byte byte-order mark sequence, which is the first item written.</span></span> <span data-ttu-id="553d4-572">それを調べてから、文字の残りの部分を読み取ると破棄されます。</span><span class="sxs-lookup"><span data-stu-id="553d4-572">It is examined, and then discarded when the rest of the character is read.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="553d4-573">54936</span><span class="sxs-lookup"><span data-stu-id="553d4-573">54936</span></span></td>
<td><span data-ttu-id="553d4-574">GB-18030</span><span class="sxs-lookup"><span data-stu-id="553d4-574">GB-18030</span></span></td>
<td><span data-ttu-id="553d4-575">中国政府によって求められている GB-18030 文字表現でデータを格納します。</span><span class="sxs-lookup"><span data-stu-id="553d4-575">Stores data in the GB-18030 character representation that is required by the Chinese government.</span></span> <span data-ttu-id="553d4-576">バイト順序マークは書き込まれません。</span><span class="sxs-lookup"><span data-stu-id="553d4-576">No byte-order mark is written.</span></span> <span data-ttu-id="553d4-577">これらのファイルは、ファイルに GB-2312 のレパートリー外の文字が含まれていない限り、コード ページ 20936 (GB-2312、中国語 (簡体) システム用の ACP) で記述されたファイルと区別できません。</span><span class="sxs-lookup"><span data-stu-id="553d4-577">These files cannot be distinguished from those written in code page 20936 (GB-2312, which is the ACP for Simplified Chinese systems) unless the file contains characters outside the repertoire of GB-2312.</span></span></td>
</tr>
</tbody>
</table>

#### <a name="examples"></a><span data-ttu-id="553d4-578">例</span><span class="sxs-lookup"><span data-stu-id="553d4-578">Examples</span></span>

<span data-ttu-id="553d4-579">次の例では、コード ページ 850 エンコードを使用して、読み取りモードで filename という名前のファイルにアクセスする TextIO オブジェクトを作成します。</span><span class="sxs-lookup"><span data-stu-id="553d4-579">The following example creates a TextIO object to access a file that is named filename in read mode by using code page 850 encoding.</span></span>

    protected void openFile(str _fileOpen = #io_read) 
    { 
        importFile = new TextIo(filename, _fileOpen, 850); 
        if (! importFile) 
        { 
            throw error(strfmt("@SYS18678", filename)); 
        } 
    }

### <a name="method-finalize"></a><span data-ttu-id="553d4-580">メソッド finalize</span><span class="sxs-lookup"><span data-stu-id="553d4-580">Method finalize</span></span>

<span data-ttu-id="553d4-581">ファイルを閉じ、データが書き込まれている場合、ファイル バッファーをディスクにフラッシュします。</span><span class="sxs-lookup"><span data-stu-id="553d4-581">Closes the file and, if data was written, flushes the file buffers to disk.</span></span>

    public void finalize()

#### <a name="remarks"></a><span data-ttu-id="553d4-582">備考</span><span class="sxs-lookup"><span data-stu-id="553d4-582">Remarks</span></span>

<span data-ttu-id="553d4-583">通常、TextIO オブジェクトは、スコープを離れることによって確定されます。</span><span class="sxs-lookup"><span data-stu-id="553d4-583">The TextIO object is usually finalized by leaving the scope.</span></span> <span data-ttu-id="553d4-584">確定メソッドは、通常は直接呼び出されません。</span><span class="sxs-lookup"><span data-stu-id="553d4-584">The finalize method is not usually directly called.</span></span> <span data-ttu-id="553d4-585">TextIO オブジェクトが確定済みになるまで、ファイルに書き込まれる出力は無効です。</span><span class="sxs-lookup"><span data-stu-id="553d4-585">Output written to the file is not valid until the TextIO object is finalized.</span></span>

## <a name="class-tilereference"></a><span data-ttu-id="553d4-586">クラス TileReference</span><span class="sxs-lookup"><span data-stu-id="553d4-586">Class TileReference</span></span>
    class TileReference extends TreeNode

### <a name="remarks"></a><span data-ttu-id="553d4-587">備考</span><span class="sxs-lookup"><span data-stu-id="553d4-587">Remarks</span></span>

### <a name="examples"></a><span data-ttu-id="553d4-588">例</span><span class="sxs-lookup"><span data-stu-id="553d4-588">Examples</span></span>

### <a name="methods"></a><span data-ttu-id="553d4-589">メソッド</span><span class="sxs-lookup"><span data-stu-id="553d4-589">Methods</span></span>

| <span data-ttu-id="553d4-590">方法</span><span class="sxs-lookup"><span data-stu-id="553d4-590">Method</span></span>                                              | <span data-ttu-id="553d4-591">説明</span><span class="sxs-lookup"><span data-stu-id="553d4-591">Description</span></span> |
|-----------------------------------------------------|-------------|
| <span data-ttu-id="553d4-592">public str tile()</span><span class="sxs-lookup"><span data-stu-id="553d4-592">public str tile()</span></span>                                   |             |
| <span data-ttu-id="553d4-593">public int copyCallerQuery()</span><span class="sxs-lookup"><span data-stu-id="553d4-593">public int copyCallerQuery()</span></span>                        |             |
| <span data-ttu-id="553d4-594">public int formViewOption()</span><span class="sxs-lookup"><span data-stu-id="553d4-594">public int formViewOption()</span></span>                         |             |
| <span data-ttu-id="553d4-595">public int openMode()</span><span class="sxs-lookup"><span data-stu-id="553d4-595">public int openMode()</span></span>                               |             |
| <span data-ttu-id="553d4-596">public str parameters()</span><span class="sxs-lookup"><span data-stu-id="553d4-596">public str parameters()</span></span>                             |             |
| <span data-ttu-id="553d4-597">public boolean isFound()</span><span class="sxs-lookup"><span data-stu-id="553d4-597">public boolean isFound()</span></span>                            |             |
| <span data-ttu-id="553d4-598">public ConfigurationKeyId configurationKeyId()</span><span class="sxs-lookup"><span data-stu-id="553d4-598">public ConfigurationKeyId configurationKeyId()</span></span>      |             |
| <span data-ttu-id="553d4-599">public ConfigurationKeyId countryConfigurationKey()</span><span class="sxs-lookup"><span data-stu-id="553d4-599">public ConfigurationKeyId countryConfigurationKey()</span></span> |             |
| <span data-ttu-id="553d4-600">public str countryRegionCodes()</span><span class="sxs-lookup"><span data-stu-id="553d4-600">public str countryRegionCodes()</span></span>                     |             |
| <span data-ttu-id="553d4-601">public str helpText()</span><span class="sxs-lookup"><span data-stu-id="553d4-601">public str helpText()</span></span>                               |             |
| <span data-ttu-id="553d4-602">public int imageLocation()</span><span class="sxs-lookup"><span data-stu-id="553d4-602">public int imageLocation()</span></span>                          |             |
| <span data-ttu-id="553d4-603">public str kpiName()</span><span class="sxs-lookup"><span data-stu-id="553d4-603">public str kpiName()</span></span>                                |             |
| <span data-ttu-id="553d4-604">public MenuItemType menuItemType()</span><span class="sxs-lookup"><span data-stu-id="553d4-604">public MenuItemType menuItemType()</span></span>                  |             |
| <span data-ttu-id="553d4-605">public str menuItemName()</span><span class="sxs-lookup"><span data-stu-id="553d4-605">public str menuItemName()</span></span>                           |             |
| <span data-ttu-id="553d4-606">public str normalImage()</span><span class="sxs-lookup"><span data-stu-id="553d4-606">public str normalImage()</span></span>                            |             |
| <span data-ttu-id="553d4-607">public int size()</span><span class="sxs-lookup"><span data-stu-id="553d4-607">public int size()</span></span>                                   |             |
| <span data-ttu-id="553d4-608">public int tileType()</span><span class="sxs-lookup"><span data-stu-id="553d4-608">public int tileType()</span></span>                               |             |
| <span data-ttu-id="553d4-609">public int tileDisplay()</span><span class="sxs-lookup"><span data-stu-id="553d4-609">public int tileDisplay()</span></span>                            |             |
| <span data-ttu-id="553d4-610">public int buttonDisplay()</span><span class="sxs-lookup"><span data-stu-id="553d4-610">public int buttonDisplay()</span></span>                          |             |
| <span data-ttu-id="553d4-611">public str url()</span><span class="sxs-lookup"><span data-stu-id="553d4-611">public str url()</span></span>                                    |             |
| <span data-ttu-id="553d4-612">public str label()</span><span class="sxs-lookup"><span data-stu-id="553d4-612">public str label()</span></span>                                  |             |
| <span data-ttu-id="553d4-613">public int refreshFrequency()</span><span class="sxs-lookup"><span data-stu-id="553d4-613">public int refreshFrequency()</span></span>                       |             |
| <span data-ttu-id="553d4-614">public int applyFilter()</span><span class="sxs-lookup"><span data-stu-id="553d4-614">public int applyFilter()</span></span>                            |             |
| <span data-ttu-id="553d4-615">public int allowUserCacheRefresh()</span><span class="sxs-lookup"><span data-stu-id="553d4-615">public int allowUserCacheRefresh()</span></span>                  |             |
| <span data-ttu-id="553d4-616">public str query()</span><span class="sxs-lookup"><span data-stu-id="553d4-616">public str query()</span></span>                                  |             |
| <span data-ttu-id="553d4-617">public boolean visible(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="553d4-617">public boolean visible(\[boolean value\])</span></span>           |             |

### <a name="method-tile"></a><span data-ttu-id="553d4-618">メソッド tile</span><span class="sxs-lookup"><span data-stu-id="553d4-618">Method tile</span></span>

    public str tile()

#### <a name="return-value"></a><span data-ttu-id="553d4-619">戻り値</span><span class="sxs-lookup"><span data-stu-id="553d4-619">Return Value</span></span>

### <a name="method-copycallerquery"></a><span data-ttu-id="553d4-620">メソッド copyCallerQuery</span><span class="sxs-lookup"><span data-stu-id="553d4-620">Method copyCallerQuery</span></span>

    public int copyCallerQuery()

#### <a name="return-value"></a><span data-ttu-id="553d4-621">戻り値</span><span class="sxs-lookup"><span data-stu-id="553d4-621">Return Value</span></span>

### <a name="method-formviewoption"></a><span data-ttu-id="553d4-622">メソッド formViewOption</span><span class="sxs-lookup"><span data-stu-id="553d4-622">Method formViewOption</span></span>

    public int formViewOption()

#### <a name="return-value"></a><span data-ttu-id="553d4-623">戻り値</span><span class="sxs-lookup"><span data-stu-id="553d4-623">Return Value</span></span>

### <a name="method-openmode"></a><span data-ttu-id="553d4-624">メソッド openMode</span><span class="sxs-lookup"><span data-stu-id="553d4-624">Method openMode</span></span>

    public int openMode()

#### <a name="return-value"></a><span data-ttu-id="553d4-625">戻り値</span><span class="sxs-lookup"><span data-stu-id="553d4-625">Return Value</span></span>

### <a name="method-parameters"></a><span data-ttu-id="553d4-626">メソッド parameters</span><span class="sxs-lookup"><span data-stu-id="553d4-626">Method parameters</span></span>

    public str parameters()

#### <a name="return-value"></a><span data-ttu-id="553d4-627">戻り値</span><span class="sxs-lookup"><span data-stu-id="553d4-627">Return Value</span></span>

### <a name="method-isfound"></a><span data-ttu-id="553d4-628">メソッド isFound</span><span class="sxs-lookup"><span data-stu-id="553d4-628">Method isFound</span></span>

    public boolean isFound()

#### <a name="return-value"></a><span data-ttu-id="553d4-629">戻り値</span><span class="sxs-lookup"><span data-stu-id="553d4-629">Return Value</span></span>

### <a name="method-configurationkeyid"></a><span data-ttu-id="553d4-630">メソッド configurationKeyId</span><span class="sxs-lookup"><span data-stu-id="553d4-630">Method configurationKeyId</span></span>

    public ConfigurationKeyId configurationKeyId()

#### <a name="return-value"></a><span data-ttu-id="553d4-631">戻り値</span><span class="sxs-lookup"><span data-stu-id="553d4-631">Return Value</span></span>

### <a name="method-countryconfigurationkey"></a><span data-ttu-id="553d4-632">メソッド countryConfigurationKey</span><span class="sxs-lookup"><span data-stu-id="553d4-632">Method countryConfigurationKey</span></span>

    public ConfigurationKeyId countryConfigurationKey()

#### <a name="return-value"></a><span data-ttu-id="553d4-633">戻り値</span><span class="sxs-lookup"><span data-stu-id="553d4-633">Return Value</span></span>

### <a name="method-countryregioncodes"></a><span data-ttu-id="553d4-634">メソッド countryRegionCodes</span><span class="sxs-lookup"><span data-stu-id="553d4-634">Method countryRegionCodes</span></span>

    public str countryRegionCodes()

#### <a name="return-value"></a><span data-ttu-id="553d4-635">戻り値</span><span class="sxs-lookup"><span data-stu-id="553d4-635">Return Value</span></span>

### <a name="method-helptext"></a><span data-ttu-id="553d4-636">メソッド helpText</span><span class="sxs-lookup"><span data-stu-id="553d4-636">Method helpText</span></span>

    public str helpText()

#### <a name="return-value"></a><span data-ttu-id="553d4-637">戻り値</span><span class="sxs-lookup"><span data-stu-id="553d4-637">Return Value</span></span>

### <a name="method-imagelocation"></a><span data-ttu-id="553d4-638">メソッド imageLocation</span><span class="sxs-lookup"><span data-stu-id="553d4-638">Method imageLocation</span></span>

    public int imageLocation()

#### <a name="return-value"></a><span data-ttu-id="553d4-639">戻り値</span><span class="sxs-lookup"><span data-stu-id="553d4-639">Return Value</span></span>

### <a name="method-kpiname"></a><span data-ttu-id="553d4-640">メソッド kpiName</span><span class="sxs-lookup"><span data-stu-id="553d4-640">Method kpiName</span></span>

    public str kpiName()

#### <a name="return-value"></a><span data-ttu-id="553d4-641">戻り値</span><span class="sxs-lookup"><span data-stu-id="553d4-641">Return Value</span></span>

### <a name="method-menuitemtype"></a><span data-ttu-id="553d4-642">メソッド menuItemType</span><span class="sxs-lookup"><span data-stu-id="553d4-642">Method menuItemType</span></span>

    public MenuItemType menuItemType()

#### <a name="return-value"></a><span data-ttu-id="553d4-643">戻り値</span><span class="sxs-lookup"><span data-stu-id="553d4-643">Return Value</span></span>

### <a name="method-menuitemname"></a><span data-ttu-id="553d4-644">メソッド menuItemName</span><span class="sxs-lookup"><span data-stu-id="553d4-644">Method menuItemName</span></span>

    public str menuItemName()

#### <a name="return-value"></a><span data-ttu-id="553d4-645">戻り値</span><span class="sxs-lookup"><span data-stu-id="553d4-645">Return Value</span></span>

### <a name="method-normalimage"></a><span data-ttu-id="553d4-646">メソッド normalImage</span><span class="sxs-lookup"><span data-stu-id="553d4-646">Method normalImage</span></span>

    public str normalImage()

#### <a name="return-value"></a><span data-ttu-id="553d4-647">戻り値</span><span class="sxs-lookup"><span data-stu-id="553d4-647">Return Value</span></span>

### <a name="method-size"></a><span data-ttu-id="553d4-648">メソッド size</span><span class="sxs-lookup"><span data-stu-id="553d4-648">Method size</span></span>

    public int size()

#### <a name="return-value"></a><span data-ttu-id="553d4-649">戻り値</span><span class="sxs-lookup"><span data-stu-id="553d4-649">Return Value</span></span>

### <a name="method-tiletype"></a><span data-ttu-id="553d4-650">メソッド tileType</span><span class="sxs-lookup"><span data-stu-id="553d4-650">Method tileType</span></span>

    public int tileType()

#### <a name="return-value"></a><span data-ttu-id="553d4-651">戻り値</span><span class="sxs-lookup"><span data-stu-id="553d4-651">Return Value</span></span>

### <a name="method-tiledisplay"></a><span data-ttu-id="553d4-652">メソッド tileDisplay</span><span class="sxs-lookup"><span data-stu-id="553d4-652">Method tileDisplay</span></span>

    public int tileDisplay()

#### <a name="return-value"></a><span data-ttu-id="553d4-653">戻り値</span><span class="sxs-lookup"><span data-stu-id="553d4-653">Return Value</span></span>

### <a name="method-buttondisplay"></a><span data-ttu-id="553d4-654">メソッド buttonDisplay</span><span class="sxs-lookup"><span data-stu-id="553d4-654">Method buttonDisplay</span></span>

    public int buttonDisplay()

#### <a name="return-value"></a><span data-ttu-id="553d4-655">戻り値</span><span class="sxs-lookup"><span data-stu-id="553d4-655">Return Value</span></span>

### <a name="method-url"></a><span data-ttu-id="553d4-656">メソッド url</span><span class="sxs-lookup"><span data-stu-id="553d4-656">Method url</span></span>

    public str url()

#### <a name="return-value"></a><span data-ttu-id="553d4-657">戻り値</span><span class="sxs-lookup"><span data-stu-id="553d4-657">Return Value</span></span>

### <a name="method-label"></a><span data-ttu-id="553d4-658">メソッド label</span><span class="sxs-lookup"><span data-stu-id="553d4-658">Method label</span></span>

    public str label()

#### <a name="return-value"></a><span data-ttu-id="553d4-659">戻り値</span><span class="sxs-lookup"><span data-stu-id="553d4-659">Return Value</span></span>

### <a name="method-refreshfrequency"></a><span data-ttu-id="553d4-660">メソッド refreshFrequency</span><span class="sxs-lookup"><span data-stu-id="553d4-660">Method refreshFrequency</span></span>

    public int refreshFrequency()

#### <a name="return-value"></a><span data-ttu-id="553d4-661">戻り値</span><span class="sxs-lookup"><span data-stu-id="553d4-661">Return Value</span></span>

### <a name="method-applyfilter"></a><span data-ttu-id="553d4-662">メソッド applyFilter</span><span class="sxs-lookup"><span data-stu-id="553d4-662">Method applyFilter</span></span>

    public int applyFilter()

#### <a name="return-value"></a><span data-ttu-id="553d4-663">戻り値</span><span class="sxs-lookup"><span data-stu-id="553d4-663">Return Value</span></span>

### <a name="method-allowusercacherefresh"></a><span data-ttu-id="553d4-664">メソッド allowUserCacheRefresh</span><span class="sxs-lookup"><span data-stu-id="553d4-664">Method allowUserCacheRefresh</span></span>

    public int allowUserCacheRefresh()

#### <a name="return-value"></a><span data-ttu-id="553d4-665">戻り値</span><span class="sxs-lookup"><span data-stu-id="553d4-665">Return Value</span></span>

### <a name="method-query"></a><span data-ttu-id="553d4-666">メソッド query</span><span class="sxs-lookup"><span data-stu-id="553d4-666">Method query</span></span>

    public str query()

#### <a name="return-value"></a><span data-ttu-id="553d4-667">戻り値</span><span class="sxs-lookup"><span data-stu-id="553d4-667">Return Value</span></span>

### <a name="method-visible"></a><span data-ttu-id="553d4-668">メソッド visible</span><span class="sxs-lookup"><span data-stu-id="553d4-668">Method visible</span></span>

    public boolean visible([boolean value])

#### <a name="parameters"></a><span data-ttu-id="553d4-669">パラメーター</span><span class="sxs-lookup"><span data-stu-id="553d4-669">Parameters</span></span>

<span data-ttu-id="553d4-670">値</span><span class="sxs-lookup"><span data-stu-id="553d4-670">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="553d4-671">戻り値</span><span class="sxs-lookup"><span data-stu-id="553d4-671">Return Value</span></span>

## <a name="class-treenode"></a><span data-ttu-id="553d4-672">クラス TreeNode</span><span class="sxs-lookup"><span data-stu-id="553d4-672">Class TreeNode</span></span>
    class TreeNode extends Object

<span data-ttu-id="553d4-673">TreeNode クラスは、アプリケーション オブジェクト ツリー (AOT) 内のノードを取得し、表します。</span><span class="sxs-lookup"><span data-stu-id="553d4-673">The TreeNode class retrieves and represents any node in the Application Object Tree (AOT).</span></span>

### <a name="remarks"></a><span data-ttu-id="553d4-674">備考</span><span class="sxs-lookup"><span data-stu-id="553d4-674">Remarks</span></span>

<span data-ttu-id="553d4-675">このクラスとそれを拡張するクラスを使用すると、作成、読み取り、更新、および X++ コードとメタデータの削除を行うことができます。</span><span class="sxs-lookup"><span data-stu-id="553d4-675">This class, and the classes that extend it, enable you to create, read, update, and delete X++ code and metadata.</span></span> <span data-ttu-id="553d4-676">ユーザーがこの API またはこのクラスから派生した API を呼び出す前に、開発セキュリティ キー (SysDevelopment) にアクセスできることを確認します。</span><span class="sxs-lookup"><span data-stu-id="553d4-676">Make sure that the user has access to the development security key (SysDevelopment) before calling this API or APIs that are derived from this class.</span></span> <span data-ttu-id="553d4-677">TreeNode クラスを使用すると、AOT 内の任意のノードへのハンドルを取得できます。</span><span class="sxs-lookup"><span data-stu-id="553d4-677">The TreeNode class can be used to get a handle to any node in the AOT.</span></span> <span data-ttu-id="553d4-678">TreeNode クラスは、AOT内の任意の種類のノードへの参照となることができる一般的なクラスです。</span><span class="sxs-lookup"><span data-stu-id="553d4-678">The TreeNode class is a generic class in that it can be a reference to any type of node in the AOT.</span></span> <span data-ttu-id="553d4-679">このクラスには、AOT のショートカット メニューの一部の機能へのアクセスを提供することに加えて、ツリーで操作するために使用するメソッドも含まれます。</span><span class="sxs-lookup"><span data-stu-id="553d4-679">In addition to providing access to some of the functions on the shortcut menu of the AOT, this class also contains methods that are used to maneuver in the tree.</span></span> <span data-ttu-id="553d4-680">TreeNodeTraverser クラスは、AOT 内のナビゲーションでも役立ちます。</span><span class="sxs-lookup"><span data-stu-id="553d4-680">The TreeNodeTraverser class is also useful in navigating in the AOT.</span></span> <span data-ttu-id="553d4-681">TreeNode::findNode および TreeNode::rootNode メソッドは treeNode オブジェクトを返します。これらのオブジェクトから、その他のノードを操作できます。</span><span class="sxs-lookup"><span data-stu-id="553d4-681">The TreeNode::findNode and TreeNode::rootNode methods return a treeNode object from which you can maneuver to any other node.</span></span>

### <a name="examples"></a><span data-ttu-id="553d4-682">例</span><span class="sxs-lookup"><span data-stu-id="553d4-682">Examples</span></span>

### <a name="methods"></a><span data-ttu-id="553d4-683">メソッド</span><span class="sxs-lookup"><span data-stu-id="553d4-683">Methods</span></span>

| <span data-ttu-id="553d4-684">方法</span><span class="sxs-lookup"><span data-stu-id="553d4-684">Method</span></span>                                                                                                                                              | <span data-ttu-id="553d4-685">説明</span><span class="sxs-lookup"><span data-stu-id="553d4-685">Description</span></span>                                                                                                                                                          |
|-----------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="553d4-686">public TreeNode SysObsoleteAttribute(UtilElementName name)</span><span class="sxs-lookup"><span data-stu-id="553d4-686">public TreeNode SysObsoleteAttribute(UtilElementName name)</span></span>                                                                                          |                                                                                                                                                                      |
| <span data-ttu-id="553d4-687">public TreeNode SysObsoleteAttribute(str name, Types type)</span><span class="sxs-lookup"><span data-stu-id="553d4-687">public TreeNode SysObsoleteAttribute(str name, Types type)</span></span>                                                                                          |                                                                                                                                                                      |
| <span data-ttu-id="553d4-688">public TreeNode SysObsoleteAttribute()</span><span class="sxs-lookup"><span data-stu-id="553d4-688">public TreeNode SysObsoleteAttribute()</span></span>                                                                                                              |                                                                                                                                                                      |
| <span data-ttu-id="553d4-689">public TreeNode SysObsoleteAttribute(int nodetype)</span><span class="sxs-lookup"><span data-stu-id="553d4-689">public TreeNode SysObsoleteAttribute(int nodetype)</span></span>                                                                                                  |                                                                                                                                                                      |
| <span data-ttu-id="553d4-690">public boolean AOTAllowEdit()</span><span class="sxs-lookup"><span data-stu-id="553d4-690">public boolean AOTAllowEdit()</span></span>                                                                                                                       |                                                                                                                                                                      |
| <span data-ttu-id="553d4-691">public int AOTbitmapId()</span><span class="sxs-lookup"><span data-stu-id="553d4-691">public int AOTbitmapId()</span></span>                                                                                                                            | <span data-ttu-id="553d4-692">ツリー ノードのビットマップのリソース ID を返します。</span><span class="sxs-lookup"><span data-stu-id="553d4-692">Returns the resource ID of the bitmap of the tree node.</span></span>                                                                                                              |
| <span data-ttu-id="553d4-693">public int AOTchildNodeCount()</span><span class="sxs-lookup"><span data-stu-id="553d4-693">public int AOTchildNodeCount()</span></span>                                                                                                                      | <span data-ttu-id="553d4-694">指定されたツリー ノードにある子ノードの数をカウントします。</span><span class="sxs-lookup"><span data-stu-id="553d4-694">Counts the number of child nodes that a given tree node has.</span></span>                                                                                                         |
| <span data-ttu-id="553d4-695">public boolean SysObsoleteAttribute(\[int flag\], \[boolean forceNoXRef\], \[boolean fastMode\])</span><span class="sxs-lookup"><span data-stu-id="553d4-695">public boolean SysObsoleteAttribute(\[int flag\], \[boolean forceNoXRef\], \[boolean fastMode\])</span></span>                                                    |                                                                                                                                                                      |
| <span data-ttu-id="553d4-696">public boolean AOTDrop(TreeNode sourcenode, \[TreeNode after\])</span><span class="sxs-lookup"><span data-stu-id="553d4-696">public boolean AOTDrop(TreeNode sourcenode, \[TreeNode after\])</span></span>                                                                                     | <span data-ttu-id="553d4-697">指定されたツリー ノードのコピーを TreeNode オブジェクトの子として作成します。</span><span class="sxs-lookup"><span data-stu-id="553d4-697">Creates a copy of a specified tree node as a child to the TreeNode object.</span></span>                                                                                           |
| <span data-ttu-id="553d4-698">public TreeNode AOTDuplicate()</span><span class="sxs-lookup"><span data-stu-id="553d4-698">public TreeNode AOTDuplicate()</span></span>                                                                                                                      |                                                                                                                                                                      |
| <span data-ttu-id="553d4-699">public TreeNode AOTfindChild(str name, \[int nodeType\])</span><span class="sxs-lookup"><span data-stu-id="553d4-699">public TreeNode AOTfindChild(str name, \[int nodeType\])</span></span>                                                                                            | <span data-ttu-id="553d4-700">このノードの指定した子ノードを検索します。</span><span class="sxs-lookup"><span data-stu-id="553d4-700">Finds the specified child node of this node.</span></span>                                                                                                                         |
| <span data-ttu-id="553d4-701">public TreeNode AOTfirstChild()</span><span class="sxs-lookup"><span data-stu-id="553d4-701">public TreeNode AOTfirstChild()</span></span>                                                                                                                     | <span data-ttu-id="553d4-702">ツリー ノードの最初の子ノードを取得します。</span><span class="sxs-lookup"><span data-stu-id="553d4-702">Retrieves the first child of the tree node.</span></span>                                                                                                                          |
| <span data-ttu-id="553d4-703">public TreeNode AOTfirstChildEx(\[boolean loadFullNode\])</span><span class="sxs-lookup"><span data-stu-id="553d4-703">public TreeNode AOTfirstChildEx(\[boolean loadFullNode\])</span></span>                                                                                           |                                                                                                                                                                      |
| <span data-ttu-id="553d4-704">public int AOTgetExecutableLineCount()</span><span class="sxs-lookup"><span data-stu-id="553d4-704">public int AOTgetExecutableLineCount()</span></span>                                                                                                              | <span data-ttu-id="553d4-705">このノードのコードの実行可能な行の数を返します。</span><span class="sxs-lookup"><span data-stu-id="553d4-705">Returns the number of executable lines of code for this node.</span></span>                                                                                                        |
| <span data-ttu-id="553d4-706">public Set AOTgetExecutableLines()</span><span class="sxs-lookup"><span data-stu-id="553d4-706">public Set AOTgetExecutableLines()</span></span>                                                                                                                  | <span data-ttu-id="553d4-707">このノードのコードの実行可能な行を返します。</span><span class="sxs-lookup"><span data-stu-id="553d4-707">Returns the executable lines of code for this node.</span></span>                                                                                                                  |
| <span data-ttu-id="553d4-708">public int AOTGetModel()</span><span class="sxs-lookup"><span data-stu-id="553d4-708">public int AOTGetModel()</span></span>                                                                                                                            |                                                                                                                                                                      |
| <span data-ttu-id="553d4-709">public str AOTgetProperties(\[boolean includeInvisible\], \[boolean includeReadOnly\], \[boolean includeNonExportable\])</span><span class="sxs-lookup"><span data-stu-id="553d4-709">public str AOTgetProperties(\[boolean includeInvisible\], \[boolean includeReadOnly\], \[boolean includeNonExportable\])</span></span>                            | <span data-ttu-id="553d4-710">ツリー ノードのプロパティを含む文字列を返します。</span><span class="sxs-lookup"><span data-stu-id="553d4-710">Returns a string containing the properties of the tree node.</span></span>                                                                                                         |
| <span data-ttu-id="553d4-711">public Struct AOTgetPropertiesExt(\[str filter\])</span><span class="sxs-lookup"><span data-stu-id="553d4-711">public Struct AOTgetPropertiesExt(\[str filter\])</span></span>                                                                                                   |                                                                                                                                                                      |
| <span data-ttu-id="553d4-712">public AnyType AOTgetProperty(str name)</span><span class="sxs-lookup"><span data-stu-id="553d4-712">public AnyType AOTgetProperty(str name)</span></span>                                                                                                             |                                                                                                                                                                      |
| <span data-ttu-id="553d4-713">public str AOTgetSource()</span><span class="sxs-lookup"><span data-stu-id="553d4-713">public str AOTgetSource()</span></span>                                                                                                                           | <span data-ttu-id="553d4-714">このノードのソース コードを返します。</span><span class="sxs-lookup"><span data-stu-id="553d4-714">Returns the source code of this node.</span></span>                                                                                                                                |
| <span data-ttu-id="553d4-715">public boolean AOTIncludeInCompare()</span><span class="sxs-lookup"><span data-stu-id="553d4-715">public boolean AOTIncludeInCompare()</span></span>                                                                                                                |                                                                                                                                                                      |
| <span data-ttu-id="553d4-716">public boolean AOTIsDirty()</span><span class="sxs-lookup"><span data-stu-id="553d4-716">public boolean AOTIsDirty()</span></span>                                                                                                                         |                                                                                                                                                                      |
| <span data-ttu-id="553d4-717">public boolean AOTIsOld()</span><span class="sxs-lookup"><span data-stu-id="553d4-717">public boolean AOTIsOld()</span></span>                                                                                                                           | <span data-ttu-id="553d4-718">このノードが、古いモデル ストアにあるファイルのものかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="553d4-718">Indicates whether this node is from a file found in the old model store.</span></span>                                                                                             |
| <span data-ttu-id="553d4-719">public boolean AOTIsPersisted()</span><span class="sxs-lookup"><span data-stu-id="553d4-719">public boolean AOTIsPersisted()</span></span>                                                                                                                     | <span data-ttu-id="553d4-720">このノードがモデル ストアに保持されているかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="553d4-720">Indicates whether this node has been persisted in the model store.</span></span>                                                                                                   |
| <span data-ttu-id="553d4-721">public boolean AOTIsProxyNode()</span><span class="sxs-lookup"><span data-stu-id="553d4-721">public boolean AOTIsProxyNode()</span></span>                                                                                                                     |                                                                                                                                                                      |
| <span data-ttu-id="553d4-722">public TreeNodeIterator AOTiterator()</span><span class="sxs-lookup"><span data-stu-id="553d4-722">public TreeNodeIterator AOTiterator()</span></span>                                                                                                               | <span data-ttu-id="553d4-723">ツリー ノードの子ノードを反復処理するために使用できるオブジェクトを返します。</span><span class="sxs-lookup"><span data-stu-id="553d4-723">Returns an object which can be used to iterate the child nodes of the tree node.</span></span>                                                                                     |
| <span data-ttu-id="553d4-724">public KernelHelpType AOTKernelHelpType()</span><span class="sxs-lookup"><span data-stu-id="553d4-724">public KernelHelpType AOTKernelHelpType()</span></span>                                                                                                           |                                                                                                                                                                      |
| <span data-ttu-id="553d4-725">public UtilEntryLevel AOTLayer()</span><span class="sxs-lookup"><span data-stu-id="553d4-725">public UtilEntryLevel AOTLayer()</span></span>                                                                                                                    | <span data-ttu-id="553d4-726">ツリー ノードのレイヤーを返します。</span><span class="sxs-lookup"><span data-stu-id="553d4-726">Returns the layer of the tree node.</span></span>                                                                                                                                  |
| <span data-ttu-id="553d4-727">public Set AOTLayers(\[boolean old\])</span><span class="sxs-lookup"><span data-stu-id="553d4-727">public Set AOTLayers(\[boolean old\])</span></span>                                                                                                               | <span data-ttu-id="553d4-728">そのツリー ノードで定義されているレイヤーのコレクションを返します。</span><span class="sxs-lookup"><span data-stu-id="553d4-728">Returns a collection of the layers the tree node is defined in.</span></span>                                                                                                      |
| <span data-ttu-id="553d4-729">public str AOTname()</span><span class="sxs-lookup"><span data-stu-id="553d4-729">public str AOTname()</span></span>                                                                                                                                | <span data-ttu-id="553d4-730">ノードの name プロパティの値を返します。</span><span class="sxs-lookup"><span data-stu-id="553d4-730">Returns the value of the name property of the node.</span></span>                                                                                                                  |
| <span data-ttu-id="553d4-731">public int AOTnewWindow()</span><span class="sxs-lookup"><span data-stu-id="553d4-731">public int AOTnewWindow()</span></span>                                                                                                                           | <span data-ttu-id="553d4-732">ルートとして新しい AOT ツリー ウィンドウをツリー ノードで開きます。</span><span class="sxs-lookup"><span data-stu-id="553d4-732">Opens a new AOT tree window with the tree node as the root.</span></span>                                                                                                          |
| <span data-ttu-id="553d4-733">public TreeNode AOTnextSibling()</span><span class="sxs-lookup"><span data-stu-id="553d4-733">public TreeNode AOTnextSibling()</span></span>                                                                                                                    | <span data-ttu-id="553d4-734">ツリー ノードと同じレベルにある次のノードを返します。</span><span class="sxs-lookup"><span data-stu-id="553d4-734">Returns the next node on the same level as the tree node.</span></span>                                                                                                            |
| <span data-ttu-id="553d4-735">public boolean AOTObjectNode()</span><span class="sxs-lookup"><span data-stu-id="553d4-735">public boolean AOTObjectNode()</span></span>                                                                                                                      | <span data-ttu-id="553d4-736">ノードがアプリケーション オブジェクトであるかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="553d4-736">Indicates whether the node is an application object.</span></span>                                                                                                                 |
| <span data-ttu-id="553d4-737">public int AOToverlayBitmapId()</span><span class="sxs-lookup"><span data-stu-id="553d4-737">public int AOToverlayBitmapId()</span></span>                                                                                                                     | <span data-ttu-id="553d4-738">このノードに関連付けられた AOT のオーバーレイのリソース ID を返します。</span><span class="sxs-lookup"><span data-stu-id="553d4-738">Returns the resource ID of the overlay in the AOT associated with this node.</span></span>                                                                                         |
| <span data-ttu-id="553d4-739">public TreeNode AOTparent()</span><span class="sxs-lookup"><span data-stu-id="553d4-739">public TreeNode AOTparent()</span></span>                                                                                                                         | <span data-ttu-id="553d4-740">ツリー ノードの親ノードを返します。</span><span class="sxs-lookup"><span data-stu-id="553d4-740">Returns the parent node of the tree node.</span></span>                                                                                                                            |
| <span data-ttu-id="553d4-741">public TreeNode AOTprevious()</span><span class="sxs-lookup"><span data-stu-id="553d4-741">public TreeNode AOTprevious()</span></span>                                                                                                                       | <span data-ttu-id="553d4-742">このツリー ノードの前の兄弟を返します。</span><span class="sxs-lookup"><span data-stu-id="553d4-742">Returns the previous sibling of this tree node.</span></span>                                                                                                                      |
| <span data-ttu-id="553d4-743">public boolean SysObsoleteAttribute(str name)</span><span class="sxs-lookup"><span data-stu-id="553d4-743">public boolean SysObsoleteAttribute(str name)</span></span>                                                                                                       |                                                                                                                                                                      |
| <span data-ttu-id="553d4-744">public str AOTtoolTip()</span><span class="sxs-lookup"><span data-stu-id="553d4-744">public str AOTtoolTip()</span></span>                                                                                                                             | <span data-ttu-id="553d4-745">そのツリー ノードに関連付けられているツールヒントを返します。</span><span class="sxs-lookup"><span data-stu-id="553d4-745">Returns the tool tip associated with the tree node.</span></span>                                                                                                                  |
| <span data-ttu-id="553d4-746">public str AOTToString()</span><span class="sxs-lookup"><span data-stu-id="553d4-746">public str AOTToString()</span></span>                                                                                                                            |                                                                                                                                                                      |
| <span data-ttu-id="553d4-747">public str AOTtypeStr()</span><span class="sxs-lookup"><span data-stu-id="553d4-747">public str AOTtypeStr()</span></span>                                                                                                                             | <span data-ttu-id="553d4-748">XPO ファイルで使用される要素タイプの文字列の内部コードを返します。</span><span class="sxs-lookup"><span data-stu-id="553d4-748">Returns the internal string code for the element type used in XPO files.</span></span>                                                                                             |
| <span data-ttu-id="553d4-749">public UtilFileType AOTUtilFileType()</span><span class="sxs-lookup"><span data-stu-id="553d4-749">public UtilFileType AOTUtilFileType()</span></span>                                                                                                               | <span data-ttu-id="553d4-750">TreeNode オブジェクトの UtilFileType 列挙型の値を取得します。</span><span class="sxs-lookup"><span data-stu-id="553d4-750">Retrieves the value of the UtilFileType enumeration type for the TreeNode object.</span></span> <span data-ttu-id="553d4-751">UtilFileType は、どのファイルの種類にアプリケーション オブジェクトが格納されているかを示します。</span><span class="sxs-lookup"><span data-stu-id="553d4-751">The UtilFileType indicates which kind of file the application object is stored in.</span></span> |
| <span data-ttu-id="553d4-752">public int applObjectId()</span><span class="sxs-lookup"><span data-stu-id="553d4-752">public int applObjectId()</span></span>                                                                                                                           | <span data-ttu-id="553d4-753">該当する場合は、アプリケーション オブジェクト ID を返します。</span><span class="sxs-lookup"><span data-stu-id="553d4-753">Returns the application object ID, if applicable.</span></span>                                                                                                                    |
| <span data-ttu-id="553d4-754">public int applObjectLayerMask()</span><span class="sxs-lookup"><span data-stu-id="553d4-754">public int applObjectLayerMask()</span></span>                                                                                                                    | <span data-ttu-id="553d4-755">この要素を含むレイヤーを指定するビットを返します。</span><span class="sxs-lookup"><span data-stu-id="553d4-755">Returns a bitmask that specifies which layers contain this element.</span></span>                                                                                                  |
| <span data-ttu-id="553d4-756">public int applObjectOldLayerMask()</span><span class="sxs-lookup"><span data-stu-id="553d4-756">public int applObjectOldLayerMask()</span></span>                                                                                                                 | <span data-ttu-id="553d4-757">ベースライン モデル ストアでこの要素を含むレイヤーを指定するビットマスクを返します。</span><span class="sxs-lookup"><span data-stu-id="553d4-757">Returns a bitmask that specifies which layers contain this element in the baseline model store.</span></span>                                                                      |
| <span data-ttu-id="553d4-758">public TreeNode getNodeInLayer(UtilEntryLevel layer, \[boolean old\])</span><span class="sxs-lookup"><span data-stu-id="553d4-758">public TreeNode getNodeInLayer(UtilEntryLevel layer, \[boolean old\])</span></span>                                                                               | <span data-ttu-id="553d4-759">指定したレイヤーからツリー ノードのバージョンを取得します。</span><span class="sxs-lookup"><span data-stu-id="553d4-759">Retrieves a version of the tree node from a specified layer.</span></span>                                                                                                         |
| <span data-ttu-id="553d4-760">public Int64 hashKey()</span><span class="sxs-lookup"><span data-stu-id="553d4-760">public Int64 hashKey()</span></span>                                                                                                                              |                                                                                                                                                                      |
| <span data-ttu-id="553d4-761">public TreeNode makeCopy()</span><span class="sxs-lookup"><span data-stu-id="553d4-761">public TreeNode makeCopy()</span></span>                                                                                                                          |                                                                                                                                                                      |
| <span data-ttu-id="553d4-762">public str newObjectName(\[str oldName\])</span><span class="sxs-lookup"><span data-stu-id="553d4-762">public str newObjectName(\[str oldName\])</span></span>                                                                                                           | <span data-ttu-id="553d4-763">新しい要素の名前を含む文字列を返します。</span><span class="sxs-lookup"><span data-stu-id="553d4-763">Returns a string that contains the name of the new element.</span></span>                                                                                                          |
| <span data-ttu-id="553d4-764">public str toString()</span><span class="sxs-lookup"><span data-stu-id="553d4-764">public str toString()</span></span>                                                                                                                               | <span data-ttu-id="553d4-765">現在のオブジェクトを表す文字列を返します。</span><span class="sxs-lookup"><span data-stu-id="553d4-765">Returns a string that represents the current object.</span></span>                                                                                                                 |
| <span data-ttu-id="553d4-766">public str treeNodeName()</span><span class="sxs-lookup"><span data-stu-id="553d4-766">public str treeNodeName()</span></span>                                                                                                                           | <span data-ttu-id="553d4-767">ツリー ノードの名前を返します。</span><span class="sxs-lookup"><span data-stu-id="553d4-767">Returns the name of the tree node.</span></span>                                                                                                                                   |
| <span data-ttu-id="553d4-768">public str treeNodePath()</span><span class="sxs-lookup"><span data-stu-id="553d4-768">public str treeNodePath()</span></span>                                                                                                                           | <span data-ttu-id="553d4-769">アプリケーション オブジェクト ツリー (AOT) 内のツリー ノードに固有のパスを返します。</span><span class="sxs-lookup"><span data-stu-id="553d4-769">Returns the unique path to the tree node within the Application Object Tree (AOT).</span></span>                                                                                   |
| <span data-ttu-id="553d4-770">public TreeNodeType treeNodeType()</span><span class="sxs-lookup"><span data-stu-id="553d4-770">public TreeNodeType treeNodeType()</span></span>                                                                                                                  | <span data-ttu-id="553d4-771">ツリー ノードのリフレクション情報を提供する TreeNodeType クラスのインスタンスを取得します。</span><span class="sxs-lookup"><span data-stu-id="553d4-771">Retrieves an instance of a TreeNodeType class that provides reflection information for the tree node.</span></span>                                                                |
| <span data-ttu-id="553d4-772">public int updateNodePermissions(boolean throwExceptions)</span><span class="sxs-lookup"><span data-stu-id="553d4-772">public int updateNodePermissions(boolean throwExceptions)</span></span>                                                                                           |                                                                                                                                                                      |
| <span data-ttu-id="553d4-773">public UtilElements utilElement()</span><span class="sxs-lookup"><span data-stu-id="553d4-773">public UtilElements utilElement()</span></span>                                                                                                                   | <span data-ttu-id="553d4-774">ノードに関連する UtilElements レコードを返します。</span><span class="sxs-lookup"><span data-stu-id="553d4-774">Returns a UtilElements record that is related to the node.</span></span>                                                                                                           |
| <span data-ttu-id="553d4-775">public UtilIdElements utilIdElement()</span><span class="sxs-lookup"><span data-stu-id="553d4-775">public UtilIdElements utilIdElement()</span></span>                                                                                                               | <span data-ttu-id="553d4-776">ノードに関連する UtilIdElements レコードを返します。</span><span class="sxs-lookup"><span data-stu-id="553d4-776">Returns a UtilIdElements record that is related to the node.</span></span>                                                                                                         |
| <span data-ttu-id="553d4-777">public boolean validateNameCharacters(str name)</span><span class="sxs-lookup"><span data-stu-id="553d4-777">public boolean validateNameCharacters(str name)</span></span>                                                                                                     |                                                                                                                                                                      |
| <span data-ttu-id="553d4-778">::public static TreeNode findNode(str path)</span><span class="sxs-lookup"><span data-stu-id="553d4-778">::public static TreeNode findNode(str path)</span></span>                                                                                                         | <span data-ttu-id="553d4-779">アプリケーション オブジェクト ツリー (AOT) の指定されたノードを返します。</span><span class="sxs-lookup"><span data-stu-id="553d4-779">Returns a specified node in the Application Object Tree (AOT).</span></span>                                                                                                       |
| <span data-ttu-id="553d4-780">::public static str generateObjectName(str template)</span><span class="sxs-lookup"><span data-stu-id="553d4-780">::public static str generateObjectName(str template)</span></span>                                                                                                |                                                                                                                                                                      |
| <span data-ttu-id="553d4-781">::public static int getMaximumNodeNameLength(int modelElementTypeId)</span><span class="sxs-lookup"><span data-stu-id="553d4-781">::public static int getMaximumNodeNameLength(int modelElementTypeId)</span></span>                                                                                |                                                                                                                                                                      |
| <span data-ttu-id="553d4-782">::public static boolean isNodeReferenceValid(TreeNode treeNode)</span><span class="sxs-lookup"><span data-stu-id="553d4-782">::public static boolean isNodeReferenceValid(TreeNode treeNode)</span></span>                                                                                     |                                                                                                                                                                      |
| <span data-ttu-id="553d4-783">::public static boolean isValidObjectName(str name)</span><span class="sxs-lookup"><span data-stu-id="553d4-783">::public static boolean isValidObjectName(str name)</span></span>                                                                                                 | <span data-ttu-id="553d4-784">引数として渡された文字列をアプリケーション オブジェクト ツリー (AOT) 内のノードの名前として使用できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="553d4-784">Determines whether the string passed as an argument can be used as a name for a node in the Application Object Tree (AOT).</span></span>                                           |
| <span data-ttu-id="553d4-785">::public static TreeNode rootNode()</span><span class="sxs-lookup"><span data-stu-id="553d4-785">::public static TreeNode rootNode()</span></span>                                                                                                                 | <span data-ttu-id="553d4-786">AOT のルート ノードを返します。</span><span class="sxs-lookup"><span data-stu-id="553d4-786">Returns the root node of the AOT.</span></span>                                                                                                                                    |
| <span data-ttu-id="553d4-787">public void SysObsoleteAttribute()</span><span class="sxs-lookup"><span data-stu-id="553d4-787">public void SysObsoleteAttribute()</span></span>                                                                                                                  |                                                                                                                                                                      |
| <span data-ttu-id="553d4-788">public void treeNodeRelease()</span><span class="sxs-lookup"><span data-stu-id="553d4-788">public void treeNodeRelease()</span></span>                                                                                                                       | <span data-ttu-id="553d4-789">ツリー ノードが明示的に解放されます。</span><span class="sxs-lookup"><span data-stu-id="553d4-789">Releases the tree node explicitly.</span></span>                                                                                                                                   |
| <span data-ttu-id="553d4-790">public void SysObsoleteAttribute(str name, xRefKind xrefKind, int lineNumber, int columNumber, \[XRefReference xrefRef\], \[ClassId parentTypeId\])</span><span class="sxs-lookup"><span data-stu-id="553d4-790">public void SysObsoleteAttribute(str name, xRefKind xrefKind, int lineNumber, int columNumber, \[XRefReference xrefRef\], \[ClassId parentTypeId\])</span></span> |                                                                                                                                                                      |
| <span data-ttu-id="553d4-791">public void AOTrun()</span><span class="sxs-lookup"><span data-stu-id="553d4-791">public void AOTrun()</span></span>                                                                                                                                | <span data-ttu-id="553d4-792">アプリケーション オブジェクト ツリー (AOT) でこのノードとそのサブツリーをコンパイルします。</span><span class="sxs-lookup"><span data-stu-id="553d4-792">Compiles this node and its subtree in the Application Object Tree (AOT).</span></span>                                                                                             |
| <span data-ttu-id="553d4-793">public void SysObsoleteAttribute()</span><span class="sxs-lookup"><span data-stu-id="553d4-793">public void SysObsoleteAttribute()</span></span>                                                                                                                  |                                                                                                                                                                      |
| <span data-ttu-id="553d4-794">public void AOTrefresh()</span><span class="sxs-lookup"><span data-stu-id="553d4-794">public void AOTrefresh()</span></span>                                                                                                                            | <span data-ttu-id="553d4-795">.aod ファイルを最新版に変更することによりノードを更新します。</span><span class="sxs-lookup"><span data-stu-id="553d4-795">Refreshes the node with the latest changes to the .aod file.</span></span>                                                                                                         |
| <span data-ttu-id="553d4-796">public void SysObsoleteAttribute(Struct struct1)</span><span class="sxs-lookup"><span data-stu-id="553d4-796">public void SysObsoleteAttribute(Struct struct1)</span></span>                                                                                                    |                                                                                                                                                                      |
| <span data-ttu-id="553d4-797">public void SysObsoleteAttribute(str properties)</span><span class="sxs-lookup"><span data-stu-id="553d4-797">public void SysObsoleteAttribute(str properties)</span></span>                                                                                                    |                                                                                                                                                                      |
| <span data-ttu-id="553d4-798">public void AOTconfigure()</span><span class="sxs-lookup"><span data-stu-id="553d4-798">public void AOTconfigure()</span></span>                                                                                                                          |                                                                                                                                                                      |
| <span data-ttu-id="553d4-799">public void AOTload()</span><span class="sxs-lookup"><span data-stu-id="553d4-799">public void AOTload()</span></span>                                                                                                                               | <span data-ttu-id="553d4-800">オブジェクトが読み込み済みであるか確認します。</span><span class="sxs-lookup"><span data-stu-id="553d4-800">Ensures that the object is loaded.</span></span>                                                                                                                                   |
| <span data-ttu-id="553d4-801">public void treeNodeExport(str filename, \[int flag\])</span><span class="sxs-lookup"><span data-stu-id="553d4-801">public void treeNodeExport(str filename, \[int flag\])</span></span>                                                                                              | <span data-ttu-id="553d4-802">アプリケーション オブジェクト ツリー (AOT) からノードとサブツリーをエキスポートします。</span><span class="sxs-lookup"><span data-stu-id="553d4-802">Exports this node and its subtree from the Application Object Tree (AOT).</span></span>                                                                                            |
| <span data-ttu-id="553d4-803">public void SysObsoleteAttribute(str source, \[boolean isStatic\])</span><span class="sxs-lookup"><span data-stu-id="553d4-803">public void SysObsoleteAttribute(str source, \[boolean isStatic\])</span></span>                                                                                  |                                                                                                                                                                      |
| <span data-ttu-id="553d4-804">public void AOTendXref()</span><span class="sxs-lookup"><span data-stu-id="553d4-804">public void AOTendXref()</span></span>                                                                                                                            |                                                                                                                                                                      |
| <span data-ttu-id="553d4-805">public void AOTmessageLine(str text, int linenumber)</span><span class="sxs-lookup"><span data-stu-id="553d4-805">public void AOTmessageLine(str text, int linenumber)</span></span>                                                                                                | <span data-ttu-id="553d4-806">アプリケーション オブジェクト ツリー (AOT) のメッセージ ウィンドウにテキストを記述します。</span><span class="sxs-lookup"><span data-stu-id="553d4-806">Writes text to the Application Object Tree (AOT) Message window.</span></span>                                                                                                     |
| <span data-ttu-id="553d4-807">public void SysObsoleteAttribute(str name, AnyType value)</span><span class="sxs-lookup"><span data-stu-id="553d4-807">public void SysObsoleteAttribute(str name, AnyType value)</span></span>                                                                                           |                                                                                                                                                                      |
| <span data-ttu-id="553d4-808">public void AOTrestore(\[boolean forceReload\])</span><span class="sxs-lookup"><span data-stu-id="553d4-808">public void AOTrestore(\[boolean forceReload\])</span></span>                                                                                                     | <span data-ttu-id="553d4-809">該当する場合は、ディスクからこのノードを再読み込みします。</span><span class="sxs-lookup"><span data-stu-id="553d4-809">Reloads this node from the disk, if applicable.</span></span>                                                                                                                      |
| <span data-ttu-id="553d4-810">public void AOTregenerate()</span><span class="sxs-lookup"><span data-stu-id="553d4-810">public void AOTregenerate()</span></span>                                                                                                                         |                                                                                                                                                                      |
| <span data-ttu-id="553d4-811">public void AOTmakeXref(\[int flag\], \[boolean xRefAll\])</span><span class="sxs-lookup"><span data-stu-id="553d4-811">public void AOTmakeXref(\[int flag\], \[boolean xRefAll\])</span></span>                                                                                          | <span data-ttu-id="553d4-812">このノードとそのサブツリーを AOT でコンパイルし、相互参照システムを更新します。</span><span class="sxs-lookup"><span data-stu-id="553d4-812">Compiles this node and its subtree in the AOT, updating the cross-reference system.</span></span>                                                                                  |
| <span data-ttu-id="553d4-813">public void AOTedit(\[int Line\], \[int Column\])</span><span class="sxs-lookup"><span data-stu-id="553d4-813">public void AOTedit(\[int Line\], \[int Column\])</span></span>                                                                                                   | <span data-ttu-id="553d4-814">このノードの適切なエディタを開きます。</span><span class="sxs-lookup"><span data-stu-id="553d4-814">Opens the appropriate editor for this node.</span></span>                                                                                                                          |
| <span data-ttu-id="553d4-815">public void AOTshowProperties()</span><span class="sxs-lookup"><span data-stu-id="553d4-815">public void AOTshowProperties()</span></span>                                                                                                                     | <span data-ttu-id="553d4-816">プロパティ シートを開いて、(まだ開かれていない場合) このノードのプロパティを表示します。</span><span class="sxs-lookup"><span data-stu-id="553d4-816">Opens the property sheet (if not already open) and shows the properties for this node.</span></span>                                                                               |
| <span data-ttu-id="553d4-817">public void AOTinsert(TreeNode parent, \[TreeNode after\], \[boolean doNotDuplicate\])</span><span class="sxs-lookup"><span data-stu-id="553d4-817">public void AOTinsert(TreeNode parent, \[TreeNode after\], \[boolean doNotDuplicate\])</span></span>                                                              | <span data-ttu-id="553d4-818">このノードのサブノード間にノードを挿入します。</span><span class="sxs-lookup"><span data-stu-id="553d4-818">Inserts a node among the subnodes of this node.</span></span>                                                                                                                      |
| <span data-ttu-id="553d4-819">public void new()</span><span class="sxs-lookup"><span data-stu-id="553d4-819">public void new()</span></span>                                                                                                                                   | <span data-ttu-id="553d4-820">TreeNode クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="553d4-820">Initializes a new instance of the TreeNode class.</span></span>                                                                                                                    |
| <span data-ttu-id="553d4-821">public void AOTMove(TreeNode parent, \[TreeNode after\])</span><span class="sxs-lookup"><span data-stu-id="553d4-821">public void AOTMove(TreeNode parent, \[TreeNode after\])</span></span>                                                                                            |                                                                                                                                                                      |
| <span data-ttu-id="553d4-822">public void SysObsoleteAttribute(int modelId)</span><span class="sxs-lookup"><span data-stu-id="553d4-822">public void SysObsoleteAttribute(int modelId)</span></span>                                                                                                       |                                                                                                                                                                      |

### <a name="method-sysobsoleteattribute"></a><span data-ttu-id="553d4-823">メソッド SysObsoleteAttribute</span><span class="sxs-lookup"><span data-stu-id="553d4-823">Method SysObsoleteAttribute</span></span>

    public TreeNode SysObsoleteAttribute(UtilElementName name)

#### <a name="parameters"></a><span data-ttu-id="553d4-824">パラメーター</span><span class="sxs-lookup"><span data-stu-id="553d4-824">Parameters</span></span>

<span data-ttu-id="553d4-825">名前</span><span class="sxs-lookup"><span data-stu-id="553d4-825">name</span></span>  

#### <a name="return-value"></a><span data-ttu-id="553d4-826">戻り値</span><span class="sxs-lookup"><span data-stu-id="553d4-826">Return Value</span></span>

### <a name="method-sysobsoleteattribute"></a><span data-ttu-id="553d4-827">メソッド SysObsoleteAttribute</span><span class="sxs-lookup"><span data-stu-id="553d4-827">Method SysObsoleteAttribute</span></span>

    public TreeNode SysObsoleteAttribute(str name, Types type)

#### <a name="parameters"></a><span data-ttu-id="553d4-828">パラメーター</span><span class="sxs-lookup"><span data-stu-id="553d4-828">Parameters</span></span>

<span data-ttu-id="553d4-829">名前</span><span class="sxs-lookup"><span data-stu-id="553d4-829">name</span></span>  

<!-- -->

<span data-ttu-id="553d4-830">タイプ</span><span class="sxs-lookup"><span data-stu-id="553d4-830">type</span></span>  

#### <a name="return-value"></a><span data-ttu-id="553d4-831">戻り値</span><span class="sxs-lookup"><span data-stu-id="553d4-831">Return Value</span></span>

### <a name="method-sysobsoleteattribute"></a><span data-ttu-id="553d4-832">メソッド SysObsoleteAttribute</span><span class="sxs-lookup"><span data-stu-id="553d4-832">Method SysObsoleteAttribute</span></span>

    public TreeNode SysObsoleteAttribute()

#### <a name="return-value"></a><span data-ttu-id="553d4-833">戻り値</span><span class="sxs-lookup"><span data-stu-id="553d4-833">Return Value</span></span>

### <a name="method-sysobsoleteattribute"></a><span data-ttu-id="553d4-834">メソッド SysObsoleteAttribute</span><span class="sxs-lookup"><span data-stu-id="553d4-834">Method SysObsoleteAttribute</span></span>

    public TreeNode SysObsoleteAttribute(int nodetype)

#### <a name="parameters"></a><span data-ttu-id="553d4-835">パラメーター</span><span class="sxs-lookup"><span data-stu-id="553d4-835">Parameters</span></span>

<span data-ttu-id="553d4-836">nodetype</span><span class="sxs-lookup"><span data-stu-id="553d4-836">nodetype</span></span>  

#### <a name="return-value"></a><span data-ttu-id="553d4-837">戻り値</span><span class="sxs-lookup"><span data-stu-id="553d4-837">Return Value</span></span>

### <a name="method-aotallowedit"></a><span data-ttu-id="553d4-838">メソッド AOTAllowEdit</span><span class="sxs-lookup"><span data-stu-id="553d4-838">Method AOTAllowEdit</span></span>

    public boolean AOTAllowEdit()

#### <a name="return-value"></a><span data-ttu-id="553d4-839">戻り値</span><span class="sxs-lookup"><span data-stu-id="553d4-839">Return Value</span></span>

### <a name="method-aotbitmapid"></a><span data-ttu-id="553d4-840">メソッド AOTbitmapId</span><span class="sxs-lookup"><span data-stu-id="553d4-840">Method AOTbitmapId</span></span>

<span data-ttu-id="553d4-841">ツリー ノードのビットマップのリソース ID を返します。</span><span class="sxs-lookup"><span data-stu-id="553d4-841">Returns the resource ID of the bitmap of the tree node.</span></span>

    public int AOTbitmapId()

#### <a name="return-value"></a><span data-ttu-id="553d4-842">戻り値</span><span class="sxs-lookup"><span data-stu-id="553d4-842">Return Value</span></span>

<span data-ttu-id="553d4-843">ツリー ノードのビットマップのリソース ID。</span><span class="sxs-lookup"><span data-stu-id="553d4-843">The resource ID of the bitmap of the tree node.</span></span>

#### <a name="examples"></a><span data-ttu-id="553d4-844">例</span><span class="sxs-lookup"><span data-stu-id="553d4-844">Examples</span></span>

<span data-ttu-id="553d4-845">次の例では、アプリケーション オブジェクト ツリー (AOT) 内の拡張データ型ノードのリソース ID を出力します。</span><span class="sxs-lookup"><span data-stu-id="553d4-845">The following example prints the resource ID of the Extended Data Types node in the Application Object Tree (AOT).</span></span>

    #AOT 
    static void myJobAOTbitmapId(Args _args) 
    { 
        treeNode treeNode = TreeNode::findNode(#ExtendedDataTypesPath); 
        print treeNode.AOTbitmapId(); 
        pause; 
    }

<span data-ttu-id="553d4-846">このジョブは整数 895 を出力します。</span><span class="sxs-lookup"><span data-stu-id="553d4-846">This job will print the integer 895.</span></span> <span data-ttu-id="553d4-847">チュートリアルのリソース フォームを実行すると、ビットマップを参照し、それが AOT 内での拡張データ型に使用されるものと同じであることが分かります。</span><span class="sxs-lookup"><span data-stu-id="553d4-847">If you run the Tutorial resources form, you can see the bitmap and verify that it is the same as the one that is used for Extended Data Types in the AOT.</span></span>

### <a name="method-aotchildnodecount"></a><span data-ttu-id="553d4-848">メソッド AOTchildNodeCount</span><span class="sxs-lookup"><span data-stu-id="553d4-848">Method AOTchildNodeCount</span></span>

<span data-ttu-id="553d4-849">指定されたツリー ノードにある子ノードの数をカウントします。</span><span class="sxs-lookup"><span data-stu-id="553d4-849">Counts the number of child nodes that a given tree node has.</span></span>

    public int AOTchildNodeCount()

#### <a name="return-value"></a><span data-ttu-id="553d4-850">戻り値</span><span class="sxs-lookup"><span data-stu-id="553d4-850">Return Value</span></span>

<span data-ttu-id="553d4-851">ツリー ノードの子ノードの数を示す整数。</span><span class="sxs-lookup"><span data-stu-id="553d4-851">An integer that indicates the number of child nodes for the tree node.</span></span>

#### <a name="examples"></a><span data-ttu-id="553d4-852">例</span><span class="sxs-lookup"><span data-stu-id="553d4-852">Examples</span></span>

<span data-ttu-id="553d4-853">次の例では、アプリケーション オブジェクト ツリー (AOT) のメニュー アイテム ノードの下に表示される子ノードの数を出力します。</span><span class="sxs-lookup"><span data-stu-id="553d4-853">The following example prints the number of child nodes that appear under the Menu Items node in the Application Object Tree (AOT).</span></span>

    #AOT 
    static void myJobAOTchildNodeCount(Args _args) 
    { 
        treeNode treeNode = TreeNode::findNode(#MenuItemsPath); 
        print "Number of nodes below Menu Items: ", treeNode.AOTchildNodeCount(); 
        pause; 
    }

### <a name="method-sysobsoleteattribute"></a><span data-ttu-id="553d4-854">メソッド SysObsoleteAttribute</span><span class="sxs-lookup"><span data-stu-id="553d4-854">Method SysObsoleteAttribute</span></span>

    public boolean SysObsoleteAttribute([int flag], [boolean forceNoXRef], [boolean fastMode])

#### <a name="parameters"></a><span data-ttu-id="553d4-855">パラメーター</span><span class="sxs-lookup"><span data-stu-id="553d4-855">Parameters</span></span>

<span data-ttu-id="553d4-856">flag</span><span class="sxs-lookup"><span data-stu-id="553d4-856">flag</span></span>  

<!-- -->

<span data-ttu-id="553d4-857">forceNoXRef</span><span class="sxs-lookup"><span data-stu-id="553d4-857">forceNoXRef</span></span>  

<!-- -->

<span data-ttu-id="553d4-858">fastMode</span><span class="sxs-lookup"><span data-stu-id="553d4-858">fastMode</span></span>  

#### <a name="return-value"></a><span data-ttu-id="553d4-859">戻り値</span><span class="sxs-lookup"><span data-stu-id="553d4-859">Return Value</span></span>

### <a name="method-aotdrop"></a><span data-ttu-id="553d4-860">メソッド AOTDrop</span><span class="sxs-lookup"><span data-stu-id="553d4-860">Method AOTDrop</span></span>

<span data-ttu-id="553d4-861">指定されたツリー ノードのコピーを TreeNode オブジェクトの子として作成します。</span><span class="sxs-lookup"><span data-stu-id="553d4-861">Creates a copy of a specified tree node as a child to the TreeNode object.</span></span>

    public boolean AOTDrop(TreeNode sourcenode, [TreeNode after])

#### <a name="parameters"></a><span data-ttu-id="553d4-862">パラメーター</span><span class="sxs-lookup"><span data-stu-id="553d4-862">Parameters</span></span>

<span data-ttu-id="553d4-863">sourcenode</span><span class="sxs-lookup"><span data-stu-id="553d4-863">sourcenode</span></span>  
<span data-ttu-id="553d4-864">ソースが後で挿入されるツリー ノードの子ノード (オプション)。</span><span class="sxs-lookup"><span data-stu-id="553d4-864">The child node of the tree node that the source should be inserted after; optional.</span></span>

<!-- -->

<span data-ttu-id="553d4-865">以後</span><span class="sxs-lookup"><span data-stu-id="553d4-865">after</span></span>  
<span data-ttu-id="553d4-866">ソースが後で挿入されるツリー ノードの子ノード (オプション)。</span><span class="sxs-lookup"><span data-stu-id="553d4-866">The child node of the tree node that the source should be inserted after; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="553d4-867">戻り値</span><span class="sxs-lookup"><span data-stu-id="553d4-867">Return Value</span></span>

<span data-ttu-id="553d4-868">ドロップ操作が成功した場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="553d4-868">true if the drop operation was successful; otherwise, false.</span></span>

#### <a name="examples"></a><span data-ttu-id="553d4-869">例</span><span class="sxs-lookup"><span data-stu-id="553d4-869">Examples</span></span>

<span data-ttu-id="553d4-870">次の例では、tutorial\_Form\_Controls フォームの underTab:Tab の最後のノードとして、tabPage:CopyOfContainers ツリー ノードを作成します。</span><span class="sxs-lookup"><span data-stu-id="553d4-870">The following example creates the tabPage:CopyOfContainers tree node as the last node underTab:Tab in the tutorial\_Form\_Controls form.</span></span>

    #AOT 
    static void myJobAOTDrop(Args _args) 
    { 
        treeNode treeNodeTab; 
        treeNode treeNodeTabPageContainers; 
        treeNodeTab = TreeNode::findNode(#FormsPath + '\\' +  
            formStr(tutorial_form_controls)+ '\\Designs\\Design\\[Tab:Tab]'); 
        treeNodeTabPageContainers = TreeNode::findNode(#FormsPath + '\\' +  
            formStr(tutorial_form_controls)+  
            '\\Designs\\Design\\[Tab:Tab]\\[TabPage:Containers]'); 
        if (treeNodeTab && treeNodeTabPageContainers) 
        { 
            // Drop the TabPage:Containers node on the Tab:Tab node. 
            print treeNodeTab.AOTDrop(treeNodeTabPageContainers); 
        } 
        else 
        { 
            print "Could not find treeNodeTab or treeNodeTabPageContainers"; 
        } 
        pause; 
    }

### <a name="method-aotduplicate"></a><span data-ttu-id="553d4-871">メソッド AOTDuplicate</span><span class="sxs-lookup"><span data-stu-id="553d4-871">Method AOTDuplicate</span></span>

    public TreeNode AOTDuplicate()

#### <a name="return-value"></a><span data-ttu-id="553d4-872">戻り値</span><span class="sxs-lookup"><span data-stu-id="553d4-872">Return Value</span></span>

### <a name="method-aotfindchild"></a><span data-ttu-id="553d4-873">メソッド AOTfindChild</span><span class="sxs-lookup"><span data-stu-id="553d4-873">Method AOTfindChild</span></span>

<span data-ttu-id="553d4-874">このノードの指定した子ノードを検索します。</span><span class="sxs-lookup"><span data-stu-id="553d4-874">Finds the specified child node of this node.</span></span>

    public TreeNode AOTfindChild(str name, [int nodeType])

#### <a name="parameters"></a><span data-ttu-id="553d4-875">パラメーター</span><span class="sxs-lookup"><span data-stu-id="553d4-875">Parameters</span></span>

<span data-ttu-id="553d4-876">名前</span><span class="sxs-lookup"><span data-stu-id="553d4-876">name</span></span>  

<!-- -->

<span data-ttu-id="553d4-877">nodeType</span><span class="sxs-lookup"><span data-stu-id="553d4-877">nodeType</span></span>  

#### <a name="return-value"></a><span data-ttu-id="553d4-878">戻り値</span><span class="sxs-lookup"><span data-stu-id="553d4-878">Return Value</span></span>

<span data-ttu-id="553d4-879">指定した TreeNode。</span><span class="sxs-lookup"><span data-stu-id="553d4-879">The specified TreeNode.</span></span>

### <a name="method-aotfirstchild"></a><span data-ttu-id="553d4-880">メソッド AOTfirstChild</span><span class="sxs-lookup"><span data-stu-id="553d4-880">Method AOTfirstChild</span></span>

<span data-ttu-id="553d4-881">ツリー ノードの最初の子ノードを取得します。</span><span class="sxs-lookup"><span data-stu-id="553d4-881">Retrieves the first child of the tree node.</span></span>

    public TreeNode AOTfirstChild()

#### <a name="return-value"></a><span data-ttu-id="553d4-882">戻り値</span><span class="sxs-lookup"><span data-stu-id="553d4-882">Return Value</span></span>

<span data-ttu-id="553d4-883">ツリー ノードの最初の子ノード。</span><span class="sxs-lookup"><span data-stu-id="553d4-883">The first child node of the tree node.</span></span>

### <a name="method-aotfirstchildex"></a><span data-ttu-id="553d4-884">メソッド AOTfirstChildEx</span><span class="sxs-lookup"><span data-stu-id="553d4-884">Method AOTfirstChildEx</span></span>

    public TreeNode AOTfirstChildEx([boolean loadFullNode])

#### <a name="parameters"></a><span data-ttu-id="553d4-885">パラメーター</span><span class="sxs-lookup"><span data-stu-id="553d4-885">Parameters</span></span>

<span data-ttu-id="553d4-886">loadFullNode</span><span class="sxs-lookup"><span data-stu-id="553d4-886">loadFullNode</span></span>  

#### <a name="return-value"></a><span data-ttu-id="553d4-887">戻り値</span><span class="sxs-lookup"><span data-stu-id="553d4-887">Return Value</span></span>

### <a name="method-aotgetexecutablelinecount"></a><span data-ttu-id="553d4-888">メソッド AOTgetExecutableLineCount</span><span class="sxs-lookup"><span data-stu-id="553d4-888">Method AOTgetExecutableLineCount</span></span>

<span data-ttu-id="553d4-889">このノードのコードの実行可能な行の数を返します。</span><span class="sxs-lookup"><span data-stu-id="553d4-889">Returns the number of executable lines of code for this node.</span></span>

    public int AOTgetExecutableLineCount()

#### <a name="return-value"></a><span data-ttu-id="553d4-890">戻り値</span><span class="sxs-lookup"><span data-stu-id="553d4-890">Return Value</span></span>

<span data-ttu-id="553d4-891">存在する場合のこのノードの実行可能コード行数。存在しない場合は、ゼロ。</span><span class="sxs-lookup"><span data-stu-id="553d4-891">The number of executable lines of code for this node if any; otherwise, zero.</span></span>

#### <a name="remarks"></a><span data-ttu-id="553d4-892">備考</span><span class="sxs-lookup"><span data-stu-id="553d4-892">Remarks</span></span>

<span data-ttu-id="553d4-893">この関数は、ソースコードを持つノードによってオーバーライドされるメソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="553d4-893">This function calls a method which is overridden by nodes which have source code.</span></span>

### <a name="method-aotgetexecutablelines"></a><span data-ttu-id="553d4-894">メソッド AOTgetExecutableLines</span><span class="sxs-lookup"><span data-stu-id="553d4-894">Method AOTgetExecutableLines</span></span>

<span data-ttu-id="553d4-895">このノードのコードの実行可能な行を返します。</span><span class="sxs-lookup"><span data-stu-id="553d4-895">Returns the executable lines of code for this node.</span></span>

    public Set AOTgetExecutableLines()

#### <a name="return-value"></a><span data-ttu-id="553d4-896">戻り値</span><span class="sxs-lookup"><span data-stu-id="553d4-896">Return Value</span></span>

<span data-ttu-id="553d4-897">このノードに実行可能なコード行が含まれているセット オブジェクト; それ以外の場合は、nullNothingnullptrunita null 参照 (Visual Basic にはなし)。</span><span class="sxs-lookup"><span data-stu-id="553d4-897">A Set object containing the executable lines of code for this node if any; otherwise, nullNothingnullptrunita null reference (Nothing in Visual Basic).</span></span>

#### <a name="remarks"></a><span data-ttu-id="553d4-898">備考</span><span class="sxs-lookup"><span data-stu-id="553d4-898">Remarks</span></span>

<span data-ttu-id="553d4-899">この関数は、ソースコードを持つノードによってオーバーライドされるメソッドを呼び出します。</span><span class="sxs-lookup"><span data-stu-id="553d4-899">This function calls a method which is overridden by nodes which have source code.</span></span>

### <a name="method-aotgetmodel"></a><span data-ttu-id="553d4-900">メソッド AOTGetModel</span><span class="sxs-lookup"><span data-stu-id="553d4-900">Method AOTGetModel</span></span>

    public int AOTGetModel()

#### <a name="return-value"></a><span data-ttu-id="553d4-901">戻り値</span><span class="sxs-lookup"><span data-stu-id="553d4-901">Return Value</span></span>

### <a name="method-aotgetproperties"></a><span data-ttu-id="553d4-902">メソッド AOTgetProperties</span><span class="sxs-lookup"><span data-stu-id="553d4-902">Method AOTgetProperties</span></span>

<span data-ttu-id="553d4-903">ツリー ノードのプロパティを含む文字列を返します。</span><span class="sxs-lookup"><span data-stu-id="553d4-903">Returns a string containing the properties of the tree node.</span></span>

    public str AOTgetProperties([boolean includeInvisible], [boolean includeReadOnly], [boolean includeNonExportable])

#### <a name="parameters"></a><span data-ttu-id="553d4-904">パラメーター</span><span class="sxs-lookup"><span data-stu-id="553d4-904">Parameters</span></span>

<span data-ttu-id="553d4-905">includeInvisible</span><span class="sxs-lookup"><span data-stu-id="553d4-905">includeInvisible</span></span>  

<!-- -->

<span data-ttu-id="553d4-906">includeReadOnly</span><span class="sxs-lookup"><span data-stu-id="553d4-906">includeReadOnly</span></span>  

<!-- -->

<span data-ttu-id="553d4-907">includeNonExportable</span><span class="sxs-lookup"><span data-stu-id="553d4-907">includeNonExportable</span></span>  

#### <a name="return-value"></a><span data-ttu-id="553d4-908">戻り値</span><span class="sxs-lookup"><span data-stu-id="553d4-908">Return Value</span></span>

<span data-ttu-id="553d4-909">ツリー ノードのプロパティを含む文字列。</span><span class="sxs-lookup"><span data-stu-id="553d4-909">A string containing the properties of the tree node.</span></span>

#### <a name="examples"></a><span data-ttu-id="553d4-910">例</span><span class="sxs-lookup"><span data-stu-id="553d4-910">Examples</span></span>

<span data-ttu-id="553d4-911">次の例では、一時テーブルのリストを示します。</span><span class="sxs-lookup"><span data-stu-id="553d4-911">The following example provides a list of temporary tables.</span></span>

    { 
        #aot 
        #properties 
        TreeNode        tn = TreeNode::findNode(#TablesPath); 
        str             tableName; 
        str             temporaryProperty; 
        tn = tn.AOTfirstChild(); 
        while (tn) 
        { 
            tableName = findProperty(tn.AOTgetProperties(), #PropertyName); 
            temporaryProperty = findProperty( 
                tn.AOTgetProperties(), 
                #PropertyTemporary); 
            info (strfmt( 
                'Table %1 has the temporary property specified as %2', 
                tableName, temporaryProperty)); 
            tn = tn.AOTnextSibling(); 
        } 
    }

### <a name="method-aotgetpropertiesext"></a><span data-ttu-id="553d4-912">メソッド AOTgetPropertiesExt</span><span class="sxs-lookup"><span data-stu-id="553d4-912">Method AOTgetPropertiesExt</span></span>

    public Struct AOTgetPropertiesExt([str filter])

#### <a name="parameters"></a><span data-ttu-id="553d4-913">パラメーター</span><span class="sxs-lookup"><span data-stu-id="553d4-913">Parameters</span></span>

<span data-ttu-id="553d4-914">フィルター</span><span class="sxs-lookup"><span data-stu-id="553d4-914">filter</span></span>  

#### <a name="return-value"></a><span data-ttu-id="553d4-915">戻り値</span><span class="sxs-lookup"><span data-stu-id="553d4-915">Return Value</span></span>

### <a name="method-aotgetproperty"></a><span data-ttu-id="553d4-916">メソッド AOTgetProperty</span><span class="sxs-lookup"><span data-stu-id="553d4-916">Method AOTgetProperty</span></span>

    public AnyType AOTgetProperty(str name)

#### <a name="parameters"></a><span data-ttu-id="553d4-917">パラメーター</span><span class="sxs-lookup"><span data-stu-id="553d4-917">Parameters</span></span>

<span data-ttu-id="553d4-918">名前</span><span class="sxs-lookup"><span data-stu-id="553d4-918">name</span></span>  

#### <a name="return-value"></a><span data-ttu-id="553d4-919">戻り値</span><span class="sxs-lookup"><span data-stu-id="553d4-919">Return Value</span></span>

### <a name="method-aotgetsource"></a><span data-ttu-id="553d4-920">メソッド AOTgetSource</span><span class="sxs-lookup"><span data-stu-id="553d4-920">Method AOTgetSource</span></span>

<span data-ttu-id="553d4-921">このノードのソース コードを返します。</span><span class="sxs-lookup"><span data-stu-id="553d4-921">Returns the source code of this node.</span></span>

    public str AOTgetSource()

#### <a name="return-value"></a><span data-ttu-id="553d4-922">戻り値</span><span class="sxs-lookup"><span data-stu-id="553d4-922">Return Value</span></span>

<span data-ttu-id="553d4-923">ソース コードが含まれている場合の文字列、それ以外の場合、nullNothingnullptrunita null 参照 (Visual Basic にはなし)。</span><span class="sxs-lookup"><span data-stu-id="553d4-923">The string that contains source code if any; otherwise, nullNothingnullptrunita null reference (Nothing in Visual Basic).</span></span>

#### <a name="remarks"></a><span data-ttu-id="553d4-924">備考</span><span class="sxs-lookup"><span data-stu-id="553d4-924">Remarks</span></span>

<span data-ttu-id="553d4-925">この関数はソース コードを持つノードによってオーバーライドされます。</span><span class="sxs-lookup"><span data-stu-id="553d4-925">This function is overridden by nodes which have source code.</span></span>

### <a name="method-aotincludeincompare"></a><span data-ttu-id="553d4-926">メソッド AOTIncludeInCompare</span><span class="sxs-lookup"><span data-stu-id="553d4-926">Method AOTIncludeInCompare</span></span>

    public boolean AOTIncludeInCompare()

#### <a name="return-value"></a><span data-ttu-id="553d4-927">戻り値</span><span class="sxs-lookup"><span data-stu-id="553d4-927">Return Value</span></span>

### <a name="method-aotisdirty"></a><span data-ttu-id="553d4-928">メソッド AOTIsDirty</span><span class="sxs-lookup"><span data-stu-id="553d4-928">Method AOTIsDirty</span></span>

    public boolean AOTIsDirty()

#### <a name="return-value"></a><span data-ttu-id="553d4-929">戻り値</span><span class="sxs-lookup"><span data-stu-id="553d4-929">Return Value</span></span>

### <a name="method-aotisold"></a><span data-ttu-id="553d4-930">メソッド AOTIsOld</span><span class="sxs-lookup"><span data-stu-id="553d4-930">Method AOTIsOld</span></span>

<span data-ttu-id="553d4-931">このノードが、古いモデル ストアにあるファイルのものかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="553d4-931">Indicates whether this node is from a file found in the old model store.</span></span>

    public boolean AOTIsOld()

#### <a name="return-value"></a><span data-ttu-id="553d4-932">戻り値</span><span class="sxs-lookup"><span data-stu-id="553d4-932">Return Value</span></span>

<span data-ttu-id="553d4-933">このノードが古いモデル ストアに由来する場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="553d4-933">true if this node is from the old model store; otherwise false.</span></span>

### <a name="method-aotispersisted"></a><span data-ttu-id="553d4-934">メソッド AOTIsPersisted</span><span class="sxs-lookup"><span data-stu-id="553d4-934">Method AOTIsPersisted</span></span>

<span data-ttu-id="553d4-935">このノードがモデル ストアに保持されているかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="553d4-935">Indicates whether this node has been persisted in the model store.</span></span>

    public boolean AOTIsPersisted()

#### <a name="return-value"></a><span data-ttu-id="553d4-936">戻り値</span><span class="sxs-lookup"><span data-stu-id="553d4-936">Return Value</span></span>

<span data-ttu-id="553d4-937">このノードが保持された場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="553d4-937">true if this node has been persisted; otherwise false.</span></span>

#### <a name="remarks"></a><span data-ttu-id="553d4-938">備考</span><span class="sxs-lookup"><span data-stu-id="553d4-938">Remarks</span></span>

<span data-ttu-id="553d4-939">メソッドがツリーノードでサポートされていない場合、このメソッドは例外をスローします。</span><span class="sxs-lookup"><span data-stu-id="553d4-939">This method throws an exception if the method is not supported for the tree node.</span></span> <span data-ttu-id="553d4-940">このメソッドがサポートされているかどうかを判断するには、TreeNode.TreeNodeType().isModelElement() メソッドを使用します。</span><span class="sxs-lookup"><span data-stu-id="553d4-940">Use the TreeNode.TreeNodeType().isModelElement() method to determine if the method is supported.</span></span>

### <a name="method-aotisproxynode"></a><span data-ttu-id="553d4-941">メソッド AOTIsProxyNode</span><span class="sxs-lookup"><span data-stu-id="553d4-941">Method AOTIsProxyNode</span></span>

    public boolean AOTIsProxyNode()

#### <a name="return-value"></a><span data-ttu-id="553d4-942">戻り値</span><span class="sxs-lookup"><span data-stu-id="553d4-942">Return Value</span></span>

### <a name="method-aotiterator"></a><span data-ttu-id="553d4-943">メソッド AOTiterator</span><span class="sxs-lookup"><span data-stu-id="553d4-943">Method AOTiterator</span></span>

<span data-ttu-id="553d4-944">ツリー ノードの子ノードを反復処理するために使用できるオブジェクトを返します。</span><span class="sxs-lookup"><span data-stu-id="553d4-944">Returns an object which can be used to iterate the child nodes of the tree node.</span></span>

    public TreeNodeIterator AOTiterator()

#### <a name="return-value"></a><span data-ttu-id="553d4-945">戻り値</span><span class="sxs-lookup"><span data-stu-id="553d4-945">Return Value</span></span>

<span data-ttu-id="553d4-946">ツリー ノードの子を反復処理するために使用する TreeNodeIterator オブジェクト。</span><span class="sxs-lookup"><span data-stu-id="553d4-946">The TreeNodeIterator object used to iterate the children of the tree node.</span></span>

### <a name="method-aotkernelhelptype"></a><span data-ttu-id="553d4-947">メソッド AOTKernelHelpType</span><span class="sxs-lookup"><span data-stu-id="553d4-947">Method AOTKernelHelpType</span></span>

    public KernelHelpType AOTKernelHelpType()

#### <a name="return-value"></a><span data-ttu-id="553d4-948">戻り値</span><span class="sxs-lookup"><span data-stu-id="553d4-948">Return Value</span></span>

### <a name="method-aotlayer"></a><span data-ttu-id="553d4-949">メソッド AOTLayer</span><span class="sxs-lookup"><span data-stu-id="553d4-949">Method AOTLayer</span></span>

<span data-ttu-id="553d4-950">ツリー ノードのレイヤーを返します。</span><span class="sxs-lookup"><span data-stu-id="553d4-950">Returns the layer of the tree node.</span></span>

    public UtilEntryLevel AOTLayer()

#### <a name="return-value"></a><span data-ttu-id="553d4-951">戻り値</span><span class="sxs-lookup"><span data-stu-id="553d4-951">Return Value</span></span>

<span data-ttu-id="553d4-952">このノードが存在するレイヤー。</span><span class="sxs-lookup"><span data-stu-id="553d4-952">The layer that this node resides in.</span></span>

#### <a name="remarks"></a><span data-ttu-id="553d4-953">備考</span><span class="sxs-lookup"><span data-stu-id="553d4-953">Remarks</span></span>

<span data-ttu-id="553d4-954">メソッドがツリーノードでサポートされていない場合、このメソッドは例外をスローします。</span><span class="sxs-lookup"><span data-stu-id="553d4-954">This method throws an exception if the method is not supported for the tree node.</span></span> <span data-ttu-id="553d4-955">このメソッドがサポートされているかどうかを判断するには、TreeNode.TreeNodeType().isLayerAware() メソッドを使用します。</span><span class="sxs-lookup"><span data-stu-id="553d4-955">Use the TreeNode.TreeNodeType().isLayerAware() method to determine if the method is supported.</span></span>

### <a name="method-aotlayers"></a><span data-ttu-id="553d4-956">メソッド AOTLayers</span><span class="sxs-lookup"><span data-stu-id="553d4-956">Method AOTLayers</span></span>

<span data-ttu-id="553d4-957">そのツリー ノードで定義されているレイヤーのコレクションを返します。</span><span class="sxs-lookup"><span data-stu-id="553d4-957">Returns a collection of the layers the tree node is defined in.</span></span>

    public Set AOTLayers([boolean old])

#### <a name="parameters"></a><span data-ttu-id="553d4-958">パラメーター</span><span class="sxs-lookup"><span data-stu-id="553d4-958">Parameters</span></span>

<span data-ttu-id="553d4-959">old</span><span class="sxs-lookup"><span data-stu-id="553d4-959">old</span></span>  
<span data-ttu-id="553d4-960">古いモデル ストアからツリー ノード定義のレイヤーを返すかどうかを示すブール値; オプション。</span><span class="sxs-lookup"><span data-stu-id="553d4-960">A Boolean value that indicates whether to return the layers of the tree node definitions from the old model store; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="553d4-961">戻り値</span><span class="sxs-lookup"><span data-stu-id="553d4-961">Return Value</span></span>

<span data-ttu-id="553d4-962">レイヤーを持つセット オブジェクト。</span><span class="sxs-lookup"><span data-stu-id="553d4-962">A Set object with the layers.</span></span>

#### <a name="remarks"></a><span data-ttu-id="553d4-963">備考</span><span class="sxs-lookup"><span data-stu-id="553d4-963">Remarks</span></span>

<span data-ttu-id="553d4-964">メソッドがツリーノードでサポートされていない場合、このメソッドは例外をスローします。</span><span class="sxs-lookup"><span data-stu-id="553d4-964">This method throws an exception if the method is not supported for the tree node.</span></span> <span data-ttu-id="553d4-965">このメソッドがサポートされているかどうかを判断するには、TreeNode.TreeNodeType().isLayerAware() メソッドを使用します。</span><span class="sxs-lookup"><span data-stu-id="553d4-965">Use the TreeNode.TreeNodeType().isLayerAware() method to determine if the method is supported.</span></span>

### <a name="method-aotname"></a><span data-ttu-id="553d4-966">メソッド AOTname</span><span class="sxs-lookup"><span data-stu-id="553d4-966">Method AOTname</span></span>

<span data-ttu-id="553d4-967">ノードの name プロパティの値を返します。</span><span class="sxs-lookup"><span data-stu-id="553d4-967">Returns the value of the name property of the node.</span></span>

    public str AOTname()

#### <a name="return-value"></a><span data-ttu-id="553d4-968">戻り値</span><span class="sxs-lookup"><span data-stu-id="553d4-968">Return Value</span></span>

<span data-ttu-id="553d4-969">name プロパティの値を含む文字列</span><span class="sxs-lookup"><span data-stu-id="553d4-969">The string that contains the value of the name property</span></span>

#### <a name="remarks"></a><span data-ttu-id="553d4-970">備考</span><span class="sxs-lookup"><span data-stu-id="553d4-970">Remarks</span></span>

<span data-ttu-id="553d4-971">ほとんどの場合、メソッド TreeNodeName と同じ結果が得られます。</span><span class="sxs-lookup"><span data-stu-id="553d4-971">In most cases, this yields the same result as the method TreeNodeName.</span></span>

#### <a name="examples"></a><span data-ttu-id="553d4-972">例</span><span class="sxs-lookup"><span data-stu-id="553d4-972">Examples</span></span>

<span data-ttu-id="553d4-973">次の例では、ツリー ノードの最初の子の名前を出力します。</span><span class="sxs-lookup"><span data-stu-id="553d4-973">The following example prints out the name of the first child of the tree node.</span></span>

    static void Job(Args _args) 
    { 
        treeNode t = infolog.findNode('\\Reports\\AssetAcquisition\\Designs\\ReportDesign1\\AutoDesignSpecs'); 
        t = t.AOTfirstChild(); 
        print "treeNodeName: " + t.treeNodeName(); 
        print "AOTName:" + t.AOTName(); 
        pause; 
    }

### <a name="method-aotnewwindow"></a><span data-ttu-id="553d4-974">メソッド AOTnewWindow</span><span class="sxs-lookup"><span data-stu-id="553d4-974">Method AOTnewWindow</span></span>

<span data-ttu-id="553d4-975">ルートとして新しい AOT ツリー ウィンドウをツリー ノードで開きます。</span><span class="sxs-lookup"><span data-stu-id="553d4-975">Opens a new AOT tree window with the tree node as the root.</span></span>

    public int AOTnewWindow()

#### <a name="return-value"></a><span data-ttu-id="553d4-976">戻り値</span><span class="sxs-lookup"><span data-stu-id="553d4-976">Return Value</span></span>

### <a name="method-aotnextsibling"></a><span data-ttu-id="553d4-977">メソッド AOTnextSibling</span><span class="sxs-lookup"><span data-stu-id="553d4-977">Method AOTnextSibling</span></span>

<span data-ttu-id="553d4-978">ツリー ノードと同じレベルにある次のノードを返します。</span><span class="sxs-lookup"><span data-stu-id="553d4-978">Returns the next node on the same level as the tree node.</span></span>

    public TreeNode AOTnextSibling()

#### <a name="return-value"></a><span data-ttu-id="553d4-979">戻り値</span><span class="sxs-lookup"><span data-stu-id="553d4-979">Return Value</span></span>

<span data-ttu-id="553d4-980">現在のツリー ノードと同じレベルにある次のノード。</span><span class="sxs-lookup"><span data-stu-id="553d4-980">The next node on the same level as the current tree node.</span></span>

### <a name="method-aotobjectnode"></a><span data-ttu-id="553d4-981">メソッド AOTObjectNode</span><span class="sxs-lookup"><span data-stu-id="553d4-981">Method AOTObjectNode</span></span>

<span data-ttu-id="553d4-982">ノードがアプリケーション オブジェクトであるかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="553d4-982">Indicates whether the node is an application object.</span></span>

    public boolean AOTObjectNode()

#### <a name="return-value"></a><span data-ttu-id="553d4-983">戻り値</span><span class="sxs-lookup"><span data-stu-id="553d4-983">Return Value</span></span>

<span data-ttu-id="553d4-984">ノードがアプリケーション オブジェクトである場合は true。それ以外の場合は false。</span><span class="sxs-lookup"><span data-stu-id="553d4-984">true if the node is an application object; otherwise false.</span></span>

#### <a name="remarks"></a><span data-ttu-id="553d4-985">備考</span><span class="sxs-lookup"><span data-stu-id="553d4-985">Remarks</span></span>

<span data-ttu-id="553d4-986">フォームまたはレポートは、アプリケーション オブジェクトです。</span><span class="sxs-lookup"><span data-stu-id="553d4-986">A form or report is an application object.</span></span> <span data-ttu-id="553d4-987">フォーム、またはその他のサブパートのコントロールはありません。</span><span class="sxs-lookup"><span data-stu-id="553d4-987">A control on a form, or any other subpart, is not.</span></span>

### <a name="method-aotoverlaybitmapid"></a><span data-ttu-id="553d4-988">メソッド AOToverlayBitmapId</span><span class="sxs-lookup"><span data-stu-id="553d4-988">Method AOToverlayBitmapId</span></span>

<span data-ttu-id="553d4-989">このノードに関連付けられた AOT のオーバーレイのリソース ID を返します。</span><span class="sxs-lookup"><span data-stu-id="553d4-989">Returns the resource ID of the overlay in the AOT associated with this node.</span></span>

    public int AOToverlayBitmapId()

#### <a name="return-value"></a><span data-ttu-id="553d4-990">戻り値</span><span class="sxs-lookup"><span data-stu-id="553d4-990">Return Value</span></span>

<span data-ttu-id="553d4-991">このノードに関連付けられた AOT のオーバーレイのリソース ID。</span><span class="sxs-lookup"><span data-stu-id="553d4-991">The resource ID of the overlay in the AOT associated with this node.</span></span>

### <a name="method-aotparent"></a><span data-ttu-id="553d4-992">メソッド AOTparent</span><span class="sxs-lookup"><span data-stu-id="553d4-992">Method AOTparent</span></span>

<span data-ttu-id="553d4-993">ツリー ノードの親ノードを返します。</span><span class="sxs-lookup"><span data-stu-id="553d4-993">Returns the parent node of the tree node.</span></span>

    public TreeNode AOTparent()

#### <a name="return-value"></a><span data-ttu-id="553d4-994">戻り値</span><span class="sxs-lookup"><span data-stu-id="553d4-994">Return Value</span></span>

<span data-ttu-id="553d4-995">ツリー ノードの親ノード。</span><span class="sxs-lookup"><span data-stu-id="553d4-995">The parent node of the tree node.</span></span>

### <a name="method-aotprevious"></a><span data-ttu-id="553d4-996">メソッド AOTprevious</span><span class="sxs-lookup"><span data-stu-id="553d4-996">Method AOTprevious</span></span>

<span data-ttu-id="553d4-997">このツリー ノードの前の兄弟を返します。</span><span class="sxs-lookup"><span data-stu-id="553d4-997">Returns the previous sibling of this tree node.</span></span>

    public TreeNode AOTprevious()

#### <a name="return-value"></a><span data-ttu-id="553d4-998">戻り値</span><span class="sxs-lookup"><span data-stu-id="553d4-998">Return Value</span></span>

<span data-ttu-id="553d4-999">同じレベルにある、このツリー ノードの前のツリー ノード。</span><span class="sxs-lookup"><span data-stu-id="553d4-999">The previous tree node relative to this one on the same level.</span></span>

### <a name="method-sysobsoleteattribute"></a><span data-ttu-id="553d4-1000">メソッド SysObsoleteAttribute</span><span class="sxs-lookup"><span data-stu-id="553d4-1000">Method SysObsoleteAttribute</span></span>

    public boolean SysObsoleteAttribute(str name)

#### <a name="parameters"></a><span data-ttu-id="553d4-1001">パラメーター</span><span class="sxs-lookup"><span data-stu-id="553d4-1001">Parameters</span></span>

<span data-ttu-id="553d4-1002">名前</span><span class="sxs-lookup"><span data-stu-id="553d4-1002">name</span></span>  

#### <a name="return-value"></a><span data-ttu-id="553d4-1003">戻り値</span><span class="sxs-lookup"><span data-stu-id="553d4-1003">Return Value</span></span>

### <a name="method-aottooltip"></a><span data-ttu-id="553d4-1004">メソッド AOTtoolTip</span><span class="sxs-lookup"><span data-stu-id="553d4-1004">Method AOTtoolTip</span></span>

<span data-ttu-id="553d4-1005">そのツリー ノードに関連付けられているツールヒントを返します。</span><span class="sxs-lookup"><span data-stu-id="553d4-1005">Returns the tool tip associated with the tree node.</span></span>

    public str AOTtoolTip()

#### <a name="return-value"></a><span data-ttu-id="553d4-1006">戻り値</span><span class="sxs-lookup"><span data-stu-id="553d4-1006">Return Value</span></span>

<span data-ttu-id="553d4-1007">ツール チップを含む文字列。</span><span class="sxs-lookup"><span data-stu-id="553d4-1007">The string that contains the tool tip.</span></span>

### <a name="method-aottostring"></a><span data-ttu-id="553d4-1008">メソッド AOTToString</span><span class="sxs-lookup"><span data-stu-id="553d4-1008">Method AOTToString</span></span>

    public str AOTToString()

#### <a name="return-value"></a><span data-ttu-id="553d4-1009">戻り値</span><span class="sxs-lookup"><span data-stu-id="553d4-1009">Return Value</span></span>

### <a name="method-aottypestr"></a><span data-ttu-id="553d4-1010">メソッド AOTtypeStr</span><span class="sxs-lookup"><span data-stu-id="553d4-1010">Method AOTtypeStr</span></span>

<span data-ttu-id="553d4-1011">XPO ファイルで使用される要素タイプの文字列の内部コードを返します。</span><span class="sxs-lookup"><span data-stu-id="553d4-1011">Returns the internal string code for the element type used in XPO files.</span></span>

    public str AOTtypeStr()

#### <a name="return-value"></a><span data-ttu-id="553d4-1012">戻り値</span><span class="sxs-lookup"><span data-stu-id="553d4-1012">Return Value</span></span>

<span data-ttu-id="553d4-1013">ツリー ノードのタイプを含む文字列。</span><span class="sxs-lookup"><span data-stu-id="553d4-1013">The string that contains the tree node type.</span></span>

### <a name="method-aotutilfiletype"></a><span data-ttu-id="553d4-1014">メソッド AOTUtilFileType</span><span class="sxs-lookup"><span data-stu-id="553d4-1014">Method AOTUtilFileType</span></span>

<span data-ttu-id="553d4-1015">TreeNode オブジェクトの UtilFileType 列挙型の値を取得します。</span><span class="sxs-lookup"><span data-stu-id="553d4-1015">Retrieves the value of the UtilFileType enumeration type for the TreeNode object.</span></span> <span data-ttu-id="553d4-1016">UtilFileType は、どのファイルの種類にアプリケーション オブジェクトが格納されているかを示します。</span><span class="sxs-lookup"><span data-stu-id="553d4-1016">The UtilFileType indicates which kind of file the application object is stored in.</span></span>

    public UtilFileType AOTUtilFileType()

#### <a name="return-value"></a><span data-ttu-id="553d4-1017">戻り値</span><span class="sxs-lookup"><span data-stu-id="553d4-1017">Return Value</span></span>

<span data-ttu-id="553d4-1018">ツリー ノードの UtilFileType 列挙値。</span><span class="sxs-lookup"><span data-stu-id="553d4-1018">The value of the UtilFileType enumeration for the tree node.</span></span> <span data-ttu-id="553d4-1019">可能な値を次の一覧に示します。</span><span class="sxs-lookup"><span data-stu-id="553d4-1019">The possible values are in the following list.</span></span> <span data-ttu-id="553d4-1020">UtilFileType::Application は、要素 (フォーム、レポート、クエリ、テーブルなど) が .aod ファイルに保存されていることを意味します。</span><span class="sxs-lookup"><span data-stu-id="553d4-1020">UtilFileType::Application means that the element is stored in the .aod file (form, report, query, table, and so on).</span></span> <span data-ttu-id="553d4-1021">UtilFileType::ApplicationCodeDocumentation は、要素が .add ファイルに保存されていることを意味します。</span><span class="sxs-lookup"><span data-stu-id="553d4-1021">UtilFileType::ApplicationCodeDocumentation means that the element is stored in the .add file.</span></span> <span data-ttu-id="553d4-1022">UtilFileType::ApplicationHelp は、要素が .ahd ファイルに保存されていることを意味します。</span><span class="sxs-lookup"><span data-stu-id="553d4-1022">UtilFileType::ApplicationHelp means that the element is stored in the .ahd file.</span></span> <span data-ttu-id="553d4-1023">UtilFileType::KernelHelp は、要素が .akh ファイルに保存されていることを意味します。</span><span class="sxs-lookup"><span data-stu-id="553d4-1023">UtilFileType::KernelHelp means that the element is stored in the .akh file.</span></span>

#### <a name="examples"></a><span data-ttu-id="553d4-1024">例</span><span class="sxs-lookup"><span data-stu-id="553d4-1024">Examples</span></span>

<span data-ttu-id="553d4-1025">次の例では、各 UtilFileType の TreeNode オブジェクトを検索し、UtilFileType のパスを Infolog に出力します。</span><span class="sxs-lookup"><span data-stu-id="553d4-1025">The following example finds a TreeNode object of each UtilFileType, and then prints the path of the UtilFileType to the Infolog.</span></span>

    static void myJob(Args _args) 
    { 
        treeNode tn; 
        tn = treeNode::findNode("\\Forms"); 
        tn = tn.AOTfirstChild(); 
        info(strfmt( 
             "Path: %1 \nUtilFileType: %2", 
             tn.treeNodePath(), 
             tn.AOTUtilFileType())); 
        tn = treeNode::findNode("\\System Documentation"); 
        tn = tn.AOTfirstChild(); 
        tn = tn.AOTfirstChild(); 
        info(strfmt( 
             "Path: %1 \nUtilFileType: %2", 
             tn.treeNodePath(), 
             tn.AOTUtilFileType())); 
        tn = treeNode::findNode("\\Application Developer Documentation"); 
        tn = tn.AOTfirstChild(); 
        tn = tn.AOTfirstChild(); 
        info(strfmt( 
            "Path: %1 \nUtilFileType: %2", 
            tn.treeNodePath(), 
            tn.AOTUtilFileType())); 
        tn = treeNode::findNode("\\Application Documentation"); 
        tn = tn.AOTfirstChild(); 
        tn = tn.AOTfirstChild(); 
        info(strfmt( 
            "Path: %1 \nUtilFileType: %2", 
            tn.treeNodePath(), 
            tn.AOTUtilFileType())); 
    }

### <a name="method-applobjectid"></a><span data-ttu-id="553d4-1026">メソッド applObjectId</span><span class="sxs-lookup"><span data-stu-id="553d4-1026">Method applObjectId</span></span>

<span data-ttu-id="553d4-1027">該当する場合は、アプリケーション オブジェクト ID を返します。</span><span class="sxs-lookup"><span data-stu-id="553d4-1027">Returns the application object ID, if applicable.</span></span>

    public int applObjectId()

#### <a name="return-value"></a><span data-ttu-id="553d4-1028">戻り値</span><span class="sxs-lookup"><span data-stu-id="553d4-1028">Return Value</span></span>

<span data-ttu-id="553d4-1029">アプリケーション オブジェクトの ID。</span><span class="sxs-lookup"><span data-stu-id="553d4-1029">The ID of the application object.</span></span>

### <a name="method-applobjectlayermask"></a><span data-ttu-id="553d4-1030">メソッド applObjectLayerMask</span><span class="sxs-lookup"><span data-stu-id="553d4-1030">Method applObjectLayerMask</span></span>

<span data-ttu-id="553d4-1031">この要素を含むレイヤーを指定するビットを返します。</span><span class="sxs-lookup"><span data-stu-id="553d4-1031">Returns a bitmask that specifies which layers contain this element.</span></span>

    public int applObjectLayerMask()

#### <a name="return-value"></a><span data-ttu-id="553d4-1032">戻り値</span><span class="sxs-lookup"><span data-stu-id="553d4-1032">Return Value</span></span>

<span data-ttu-id="553d4-1033">この要素を含むレイヤーを指定するビット。</span><span class="sxs-lookup"><span data-stu-id="553d4-1033">A bitmask that specifies which layers contain this element.</span></span>

### <a name="method-applobjectoldlayermask"></a><span data-ttu-id="553d4-1034">メソッド applObjectOldLayerMask</span><span class="sxs-lookup"><span data-stu-id="553d4-1034">Method applObjectOldLayerMask</span></span>

<span data-ttu-id="553d4-1035">ベースライン モデル ストアでこの要素を含むレイヤーを指定するビットマスクを返します。</span><span class="sxs-lookup"><span data-stu-id="553d4-1035">Returns a bitmask that specifies which layers contain this element in the baseline model store.</span></span>

    public int applObjectOldLayerMask()

#### <a name="return-value"></a><span data-ttu-id="553d4-1036">戻り値</span><span class="sxs-lookup"><span data-stu-id="553d4-1036">Return Value</span></span>

<span data-ttu-id="553d4-1037">この要素を含むレイヤーを指定するビット。</span><span class="sxs-lookup"><span data-stu-id="553d4-1037">A bitmask that specifies which layers contain this element.</span></span>

### <a name="method-getnodeinlayer"></a><span data-ttu-id="553d4-1038">メソッド getNodeInLayer</span><span class="sxs-lookup"><span data-stu-id="553d4-1038">Method getNodeInLayer</span></span>

<span data-ttu-id="553d4-1039">指定したレイヤーからツリー ノードのバージョンを取得します。</span><span class="sxs-lookup"><span data-stu-id="553d4-1039">Retrieves a version of the tree node from a specified layer.</span></span>

    public TreeNode getNodeInLayer(UtilEntryLevel layer, [boolean old])

#### <a name="parameters"></a><span data-ttu-id="553d4-1040">パラメーター</span><span class="sxs-lookup"><span data-stu-id="553d4-1040">Parameters</span></span>

<span data-ttu-id="553d4-1041"> レイヤー</span><span class="sxs-lookup"><span data-stu-id="553d4-1041">layer</span></span>  
<span data-ttu-id="553d4-1042">古いモデル ストアのレイヤー ファイルからノードを取得する必要があるかどうかを指定する値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="553d4-1042">The value specifying whether or not the node should be retrieved from the layer file in the old model store; optional.</span></span>

<!-- -->

<span data-ttu-id="553d4-1043">old</span><span class="sxs-lookup"><span data-stu-id="553d4-1043">old</span></span>  
<span data-ttu-id="553d4-1044">古いモデル ストアのレイヤー ファイルからノードを取得する必要があるかどうかを指定する値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="553d4-1044">The value specifying whether or not the node should be retrieved from the layer file in the old model store; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="553d4-1045">戻り値</span><span class="sxs-lookup"><span data-stu-id="553d4-1045">Return Value</span></span>

<span data-ttu-id="553d4-1046">新しい TreeNode。</span><span class="sxs-lookup"><span data-stu-id="553d4-1046">The new TreeNode.</span></span>

#### <a name="remarks"></a><span data-ttu-id="553d4-1047">備考</span><span class="sxs-lookup"><span data-stu-id="553d4-1047">Remarks</span></span>

<span data-ttu-id="553d4-1048">メソッドがツリーノードでサポートされていない場合、このメソッドは例外をスローします。</span><span class="sxs-lookup"><span data-stu-id="553d4-1048">This method throws an exception if the method is not supported for the tree node.</span></span> <span data-ttu-id="553d4-1049">このメソッドがサポートされているかどうかを判断するには、TreeNode.TreeNodeType().isGetNodeInLayerSupported メソッドを使用します。</span><span class="sxs-lookup"><span data-stu-id="553d4-1049">Use the TreeNode.TreeNodeType().isGetNodeInLayerSupported method to determine if the method is supported.</span></span>

### <a name="method-hashkey"></a><span data-ttu-id="553d4-1050">メソッド hashKey</span><span class="sxs-lookup"><span data-stu-id="553d4-1050">Method hashKey</span></span>

    public Int64 hashKey()

#### <a name="return-value"></a><span data-ttu-id="553d4-1051">戻り値</span><span class="sxs-lookup"><span data-stu-id="553d4-1051">Return Value</span></span>

### <a name="method-makecopy"></a><span data-ttu-id="553d4-1052">メソッド makeCopy</span><span class="sxs-lookup"><span data-stu-id="553d4-1052">Method makeCopy</span></span>

    public TreeNode makeCopy()

#### <a name="return-value"></a><span data-ttu-id="553d4-1053">戻り値</span><span class="sxs-lookup"><span data-stu-id="553d4-1053">Return Value</span></span>

### <a name="method-newobjectname"></a><span data-ttu-id="553d4-1054">メソッド newObjectName</span><span class="sxs-lookup"><span data-stu-id="553d4-1054">Method newObjectName</span></span>

<span data-ttu-id="553d4-1055">新しい要素の名前を含む文字列を返します。</span><span class="sxs-lookup"><span data-stu-id="553d4-1055">Returns a string that contains the name of the new element.</span></span>

    public str newObjectName([str oldName])

#### <a name="parameters"></a><span data-ttu-id="553d4-1056">パラメーター</span><span class="sxs-lookup"><span data-stu-id="553d4-1056">Parameters</span></span>

<span data-ttu-id="553d4-1057">oldName</span><span class="sxs-lookup"><span data-stu-id="553d4-1057">oldName</span></span>  
<span data-ttu-id="553d4-1058">ノードの新しい名前 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="553d4-1058">The new name of the node; optional.</span></span> <span data-ttu-id="553d4-1059">引数が渡されなかった場合、新しいノード名は、子ノード タイプによって決定されます。</span><span class="sxs-lookup"><span data-stu-id="553d4-1059">If no argument is passed, the new node name is determined by the child node type.</span></span>

#### <a name="return-value"></a><span data-ttu-id="553d4-1060">戻り値</span><span class="sxs-lookup"><span data-stu-id="553d4-1060">Return Value</span></span>

<span data-ttu-id="553d4-1061">新しい要素の名前を含む文字列。</span><span class="sxs-lookup"><span data-stu-id="553d4-1061">The string that contains the name of the new element.</span></span>

#### <a name="remarks"></a><span data-ttu-id="553d4-1062">備考</span><span class="sxs-lookup"><span data-stu-id="553d4-1062">Remarks</span></span>

<span data-ttu-id="553d4-1063">引数が渡されなかった場合、新しいノード名は、子ノード タイプによって決定されます。</span><span class="sxs-lookup"><span data-stu-id="553d4-1063">If no argument is passed, the new node name is determined by the child node type.</span></span> <span data-ttu-id="553d4-1064">たとえば、TreeNode に子としてフォームがある場合、引数なしのこのメソッドの呼び出しは「Form1」を返します。</span><span class="sxs-lookup"><span data-stu-id="553d4-1064">For example, if the TreeNode has forms as children, calling this method without an argument will return "Form1".</span></span> <span data-ttu-id="553d4-1065">ツリー ノードに複数の子ノードがある場合は、メソッドは "object" という文字列を返します。</span><span class="sxs-lookup"><span data-stu-id="553d4-1065">If the tree node has several child node types, the method returns the string "object".</span></span>

#### <a name="examples"></a><span data-ttu-id="553d4-1066">例</span><span class="sxs-lookup"><span data-stu-id="553d4-1066">Examples</span></span>

<span data-ttu-id="553d4-1067">次の Treenode.newObjectName の呼び出しでは、データ ディクショナリ ノードに複数のオブジェクト型を表す子があるため、「object」が返されます。</span><span class="sxs-lookup"><span data-stu-id="553d4-1067">The following call to Treenode.newObjectName returns "object" because the data dictionary node has children that represent several object types.</span></span>

    { 
        TreeNode t; 
        str s; 
        t = TreeNode::findNode("\Data dictionary"); 
        s = t.newObjectName(); 
        print s; 
        pause; 
    }

### <a name="method-tostring"></a><span data-ttu-id="553d4-1068">メソッド toString</span><span class="sxs-lookup"><span data-stu-id="553d4-1068">Method toString</span></span>

<span data-ttu-id="553d4-1069">現在のオブジェクトを表す文字列を返します。</span><span class="sxs-lookup"><span data-stu-id="553d4-1069">Returns a string that represents the current object.</span></span>

    public str toString()

#### <a name="return-value"></a><span data-ttu-id="553d4-1070">戻り値</span><span class="sxs-lookup"><span data-stu-id="553d4-1070">Return Value</span></span>

<span data-ttu-id="553d4-1071">現在のオブジェクトを表す文字列。</span><span class="sxs-lookup"><span data-stu-id="553d4-1071">A string that represents the current object.</span></span>

#### <a name="remarks"></a><span data-ttu-id="553d4-1072">備考</span><span class="sxs-lookup"><span data-stu-id="553d4-1072">Remarks</span></span>

<span data-ttu-id="553d4-1073">既定の実装は、オブジェクトのクラス名を返します。</span><span class="sxs-lookup"><span data-stu-id="553d4-1073">The default implementation returns the class name of the object.</span></span> <span data-ttu-id="553d4-1074">メソッドは派生クラスで上書きできるため、そのタイプの意味のある値が返されます。</span><span class="sxs-lookup"><span data-stu-id="553d4-1074">The method can be overridden in a derived class to return values that are meaningful for that type.</span></span> <span data-ttu-id="553d4-1075">たとえば、クラスのインスタンスは、インスタンスまたは静的などの、メソッド名およびメソッドのタイプを返します。</span><span class="sxs-lookup"><span data-stu-id="553d4-1075">For example, an instance of the class returns the method name and type of the method, such as instance or static.</span></span>

### <a name="method-treenodename"></a><span data-ttu-id="553d4-1076">メソッド treeNodeName</span><span class="sxs-lookup"><span data-stu-id="553d4-1076">Method treeNodeName</span></span>

<span data-ttu-id="553d4-1077">ツリー ノードの名前を返します。</span><span class="sxs-lookup"><span data-stu-id="553d4-1077">Returns the name of the tree node.</span></span>

    public str treeNodeName()

#### <a name="return-value"></a><span data-ttu-id="553d4-1078">戻り値</span><span class="sxs-lookup"><span data-stu-id="553d4-1078">Return Value</span></span>

<span data-ttu-id="553d4-1079">ツリー ノードの名前を含む文字列。</span><span class="sxs-lookup"><span data-stu-id="553d4-1079">The string that contains the name of the tree node.</span></span>

### <a name="method-treenodepath"></a><span data-ttu-id="553d4-1080">メソッド treeNodePath</span><span class="sxs-lookup"><span data-stu-id="553d4-1080">Method treeNodePath</span></span>

<span data-ttu-id="553d4-1081">アプリケーション オブジェクト ツリー (AOT) 内のツリー ノードに固有のパスを返します。</span><span class="sxs-lookup"><span data-stu-id="553d4-1081">Returns the unique path to the tree node within the Application Object Tree (AOT).</span></span>

    public str treeNodePath()

#### <a name="return-value"></a><span data-ttu-id="553d4-1082">戻り値</span><span class="sxs-lookup"><span data-stu-id="553d4-1082">Return Value</span></span>

<span data-ttu-id="553d4-1083">AOT 内のツリー ノードの一意のパスを返します。</span><span class="sxs-lookup"><span data-stu-id="553d4-1083">Returns the unique path of the tree node in the AOT.</span></span>

#### <a name="examples"></a><span data-ttu-id="553d4-1084">例</span><span class="sxs-lookup"><span data-stu-id="553d4-1084">Examples</span></span>

<span data-ttu-id="553d4-1085">次の例では、各 UtilFileType の TreeNode オブジェクトを検索し、UtilFileType のパスを Infolog に出力します。</span><span class="sxs-lookup"><span data-stu-id="553d4-1085">The following example finds a TreeNode object of each UtilFileType and prints the path of the UtilFileType to the Infolog.</span></span>

    static void myJob(Args _args) 
    { 
        treeNode tn; 
        tn = treeNode::findNode("\\Forms"); 
        tn = tn.AOTfirstChild(); 
        info(strfmt( 
             "Path: %1 \nUtilFileType: %2", 
             tn.treeNodePath(), 
             tn.AOTUtilFileType())); 
        tn = treeNode::findNode("\\System Documentation"); 
        tn = tn.AOTfirstChild(); 
        tn = tn.AOTfirstChild(); 
        info(strfmt( 
             "Path: %1 \nUtilFileType: %2", 
             tn.treeNodePath(), 
             tn.AOTUtilFileType())); 
        tn = treeNode::findNode("\\Application Developer Documentation"); 
        tn = tn.AOTfirstChild(); 
        tn = tn.AOTfirstChild(); 
        info(strfmt( 
            "Path: %1 \nUtilFileType: %2", 
            tn.treeNodePath(), 
            tn.AOTUtilFileType())); 
        tn = treeNode::findNode("\\Application Documentation"); 
        tn = tn.AOTfirstChild(); 
        tn = tn.AOTfirstChild(); 
        info(strfmt( 
            "Path: %1 \nUtilFileType: %2", 
            tn.treeNodePath(), 
            tn.AOTUtilFileType())); 
    }

### <a name="method-treenodetype"></a><span data-ttu-id="553d4-1086">メソッド treeNodeType</span><span class="sxs-lookup"><span data-stu-id="553d4-1086">Method treeNodeType</span></span>

<span data-ttu-id="553d4-1087">ツリー ノードのリフレクション情報を提供する TreeNodeType クラスのインスタンスを取得します。</span><span class="sxs-lookup"><span data-stu-id="553d4-1087">Retrieves an instance of a TreeNodeType class that provides reflection information for the tree node.</span></span>

    public TreeNodeType treeNodeType()

#### <a name="return-value"></a><span data-ttu-id="553d4-1088">戻り値</span><span class="sxs-lookup"><span data-stu-id="553d4-1088">Return Value</span></span>

<span data-ttu-id="553d4-1089">TreeNodeType クラスのインスタンス。</span><span class="sxs-lookup"><span data-stu-id="553d4-1089">An instance of a TreeNodeType class.</span></span>

### <a name="method-updatenodepermissions"></a><span data-ttu-id="553d4-1090">メソッド updateNodePermissions</span><span class="sxs-lookup"><span data-stu-id="553d4-1090">Method updateNodePermissions</span></span>

    public int updateNodePermissions(boolean throwExceptions)

#### <a name="parameters"></a><span data-ttu-id="553d4-1091">パラメーター</span><span class="sxs-lookup"><span data-stu-id="553d4-1091">Parameters</span></span>

<span data-ttu-id="553d4-1092">throwExceptions</span><span class="sxs-lookup"><span data-stu-id="553d4-1092">throwExceptions</span></span>  

#### <a name="return-value"></a><span data-ttu-id="553d4-1093">戻り値</span><span class="sxs-lookup"><span data-stu-id="553d4-1093">Return Value</span></span>

### <a name="method-utilelement"></a><span data-ttu-id="553d4-1094">メソッド utilElement</span><span class="sxs-lookup"><span data-stu-id="553d4-1094">Method utilElement</span></span>

<span data-ttu-id="553d4-1095">ノードに関連する UtilElements レコードを返します。</span><span class="sxs-lookup"><span data-stu-id="553d4-1095">Returns a UtilElements record that is related to the node.</span></span>

    public UtilElements utilElement()

#### <a name="return-value"></a><span data-ttu-id="553d4-1096">戻り値</span><span class="sxs-lookup"><span data-stu-id="553d4-1096">Return Value</span></span>

<span data-ttu-id="553d4-1097">ノードに関連する UtilElements レコード。</span><span class="sxs-lookup"><span data-stu-id="553d4-1097">The UtilElements record that is related to the node.</span></span>

#### <a name="remarks"></a><span data-ttu-id="553d4-1098">備考</span><span class="sxs-lookup"><span data-stu-id="553d4-1098">Remarks</span></span>

<span data-ttu-id="553d4-1099">メソッドがツリーノードでサポートされていない場合、このメソッドは例外をスローします。</span><span class="sxs-lookup"><span data-stu-id="553d4-1099">This method throws an exception if the method is not supported for the tree node.</span></span>

### <a name="method-utilidelement"></a><span data-ttu-id="553d4-1100">メソッド utilIdElement</span><span class="sxs-lookup"><span data-stu-id="553d4-1100">Method utilIdElement</span></span>

<span data-ttu-id="553d4-1101">ノードに関連する UtilIdElements レコードを返します。</span><span class="sxs-lookup"><span data-stu-id="553d4-1101">Returns a UtilIdElements record that is related to the node.</span></span>

    public UtilIdElements utilIdElement()

#### <a name="return-value"></a><span data-ttu-id="553d4-1102">戻り値</span><span class="sxs-lookup"><span data-stu-id="553d4-1102">Return Value</span></span>

<span data-ttu-id="553d4-1103">ノードに関連する UtilIdElements レコード。</span><span class="sxs-lookup"><span data-stu-id="553d4-1103">The UtilIdElements record that is related to the node.</span></span>

#### <a name="remarks"></a><span data-ttu-id="553d4-1104">備考</span><span class="sxs-lookup"><span data-stu-id="553d4-1104">Remarks</span></span>

<span data-ttu-id="553d4-1105">メソッドがツリーノードでサポートされていない場合、このメソッドは例外をスローします。</span><span class="sxs-lookup"><span data-stu-id="553d4-1105">This method throws an exception if the method is not supported for the tree node.</span></span>

### <a name="method-validatenamecharacters"></a><span data-ttu-id="553d4-1106">メソッド validateNameCharacters</span><span class="sxs-lookup"><span data-stu-id="553d4-1106">Method validateNameCharacters</span></span>

    public boolean validateNameCharacters(str name)

#### <a name="parameters"></a><span data-ttu-id="553d4-1107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="553d4-1107">Parameters</span></span>

<span data-ttu-id="553d4-1108">名前</span><span class="sxs-lookup"><span data-stu-id="553d4-1108">name</span></span>  

#### <a name="return-value"></a><span data-ttu-id="553d4-1109">戻り値</span><span class="sxs-lookup"><span data-stu-id="553d4-1109">Return Value</span></span>

### <a name="method-findnode"></a><span data-ttu-id="553d4-1110">メソッド findNode</span><span class="sxs-lookup"><span data-stu-id="553d4-1110">Method findNode</span></span>

<span data-ttu-id="553d4-1111">アプリケーション オブジェクト ツリー (AOT) の指定されたノードを返します。</span><span class="sxs-lookup"><span data-stu-id="553d4-1111">Returns a specified node in the Application Object Tree (AOT).</span></span>

    public static TreeNode findNode(str path)

#### <a name="parameters"></a><span data-ttu-id="553d4-1112">パラメーター</span><span class="sxs-lookup"><span data-stu-id="553d4-1112">Parameters</span></span>

<span data-ttu-id="553d4-1113">path</span><span class="sxs-lookup"><span data-stu-id="553d4-1113">path</span></span>  
<span data-ttu-id="553d4-1114">検索で使用されるパスを示す文字列。</span><span class="sxs-lookup"><span data-stu-id="553d4-1114">A string that indicates the path that is used in the search.</span></span>

#### <a name="return-value"></a><span data-ttu-id="553d4-1115">戻り値</span><span class="sxs-lookup"><span data-stu-id="553d4-1115">Return Value</span></span>

<span data-ttu-id="553d4-1116">指定されたパスのノードが存在しない場合の、要求された TreeNode オブジェクトまたは nullNothingnullptrunita null 参照 (Visual Basic ではなし)。</span><span class="sxs-lookup"><span data-stu-id="553d4-1116">The requested TreeNode object or nullNothingnullptrunita null reference (Nothing in Visual Basic) if no node with the specified path exists.</span></span>

#### <a name="remarks"></a><span data-ttu-id="553d4-1117">備考</span><span class="sxs-lookup"><span data-stu-id="553d4-1117">Remarks</span></span>

<span data-ttu-id="553d4-1118">TreeNode オブジェクトを取得する別の方法は、Info.getNode メソッドを使用することです。</span><span class="sxs-lookup"><span data-stu-id="553d4-1118">Another way of getting a TreeNode object is by using the Info.getNode method.</span></span> <span data-ttu-id="553d4-1119">2 つのメソッド間の重要な違いは、Info.getNode メソッドが AOT から分離されているノードを提供するのに対して一方 findNode メソッドは AOT のノードを返します。</span><span class="sxs-lookup"><span data-stu-id="553d4-1119">An important difference between the two methods is that the Info.getNode method will give you a node that is detached from the AOT, whereas the findNode method will return the node in the AOT.</span></span> <span data-ttu-id="553d4-1120">つまり、Info.getNode メソッドから返されるノードは親ノードを持たず、findNode メソッドから返されるノードは親ノードを持ちます。</span><span class="sxs-lookup"><span data-stu-id="553d4-1120">This means that the node that is returned by the Info.getNode method will not have a parent node, whereas the one returned by the findNode method will have a parent node.</span></span>

#### <a name="examples"></a><span data-ttu-id="553d4-1121">例</span><span class="sxs-lookup"><span data-stu-id="553d4-1121">Examples</span></span>

<span data-ttu-id="553d4-1122">次の例では、TreeNode::findNode メソッドが呼び出される時に検出される ツリー ノードの名前を取得します。</span><span class="sxs-lookup"><span data-stu-id="553d4-1122">The following example retrieves the name of the tree node that is found the TreeNode::findNode method is called.</span></span> <span data-ttu-id="553d4-1123">この例では、TreeNode.findNode メソッドを呼び出す前に、ユーザーに必要なセキュリティ キーがあるかどうかを確認します。</span><span class="sxs-lookup"><span data-stu-id="553d4-1123">This example checks whether the user has the required security key before it calls the TreeNode.findNode method.</span></span>

    server static public void Main(Args _args) 
    { 
        TreeNode tn; 
        str name; 
        tn = TreeNode::findNode(@"\Classes"); 
        if (tn) 
        { 
            name = tn.treeNodeName(); 
        } 
    }

### <a name="method-generateobjectname"></a><span data-ttu-id="553d4-1124">メソッド generateObjectName</span><span class="sxs-lookup"><span data-stu-id="553d4-1124">Method generateObjectName</span></span>

    public static str generateObjectName(str template)

#### <a name="parameters"></a><span data-ttu-id="553d4-1125">パラメーター</span><span class="sxs-lookup"><span data-stu-id="553d4-1125">Parameters</span></span>

<span data-ttu-id="553d4-1126">テンプレート</span><span class="sxs-lookup"><span data-stu-id="553d4-1126">template</span></span>  

#### <a name="return-value"></a><span data-ttu-id="553d4-1127">戻り値</span><span class="sxs-lookup"><span data-stu-id="553d4-1127">Return Value</span></span>

### <a name="method-getmaximumnodenamelength"></a><span data-ttu-id="553d4-1128">メソッド getMaximumNodeNameLength</span><span class="sxs-lookup"><span data-stu-id="553d4-1128">Method getMaximumNodeNameLength</span></span>

    public static int getMaximumNodeNameLength(int modelElementTypeId)

#### <a name="parameters"></a><span data-ttu-id="553d4-1129">パラメーター</span><span class="sxs-lookup"><span data-stu-id="553d4-1129">Parameters</span></span>

<span data-ttu-id="553d4-1130">modelElementTypeId</span><span class="sxs-lookup"><span data-stu-id="553d4-1130">modelElementTypeId</span></span>  

#### <a name="return-value"></a><span data-ttu-id="553d4-1131">戻り値</span><span class="sxs-lookup"><span data-stu-id="553d4-1131">Return Value</span></span>

### <a name="method-isnodereferencevalid"></a><span data-ttu-id="553d4-1132">メソッド isNodeReferenceValid</span><span class="sxs-lookup"><span data-stu-id="553d4-1132">Method isNodeReferenceValid</span></span>

    public static boolean isNodeReferenceValid(TreeNode treeNode)

#### <a name="parameters"></a><span data-ttu-id="553d4-1133">パラメーター</span><span class="sxs-lookup"><span data-stu-id="553d4-1133">Parameters</span></span>

<span data-ttu-id="553d4-1134">treeNode</span><span class="sxs-lookup"><span data-stu-id="553d4-1134">treeNode</span></span>  

#### <a name="return-value"></a><span data-ttu-id="553d4-1135">戻り値</span><span class="sxs-lookup"><span data-stu-id="553d4-1135">Return Value</span></span>

### <a name="method-isvalidobjectname"></a><span data-ttu-id="553d4-1136">メソッド isValidObjectName</span><span class="sxs-lookup"><span data-stu-id="553d4-1136">Method isValidObjectName</span></span>

<span data-ttu-id="553d4-1137">引数として渡された文字列をアプリケーション オブジェクト ツリー (AOT) 内のノードの名前として使用できるかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="553d4-1137">Determines whether the string passed as an argument can be used as a name for a node in the Application Object Tree (AOT).</span></span>

    public static boolean isValidObjectName(str name)

#### <a name="parameters"></a><span data-ttu-id="553d4-1138">パラメーター</span><span class="sxs-lookup"><span data-stu-id="553d4-1138">Parameters</span></span>

<span data-ttu-id="553d4-1139">名前</span><span class="sxs-lookup"><span data-stu-id="553d4-1139">name</span></span>  
<span data-ttu-id="553d4-1140">検証するツリー ノードの名前を含む文字列。</span><span class="sxs-lookup"><span data-stu-id="553d4-1140">The string that contains the tree node name to validate.</span></span>

#### <a name="return-value"></a><span data-ttu-id="553d4-1141">戻り値</span><span class="sxs-lookup"><span data-stu-id="553d4-1141">Return Value</span></span>

<span data-ttu-id="553d4-1142">各条件が一致している場合は true。それ以外の場合は false。</span><span class="sxs-lookup"><span data-stu-id="553d4-1142">true if each condition is met; otherwise false.</span></span>

#### <a name="remarks"></a><span data-ttu-id="553d4-1143">備考</span><span class="sxs-lookup"><span data-stu-id="553d4-1143">Remarks</span></span>

<span data-ttu-id="553d4-1144">候補者の名前は、次の条件を満たす必要があります:</span><span class="sxs-lookup"><span data-stu-id="553d4-1144">A candidate name must meet the following conditions:</span></span>

-   <span data-ttu-id="553d4-1145">最初の文字は数字、記号ではない文字でなければなりません。</span><span class="sxs-lookup"><span data-stu-id="553d4-1145">The first character must be a letter.</span></span>
-   <span data-ttu-id="553d4-1146">文字、数字、またはアンダースコアだけを含めることができます。</span><span class="sxs-lookup"><span data-stu-id="553d4-1146">It can only contain letters, numbers or an underscore.</span></span>
-   <span data-ttu-id="553d4-1147">トークンに対して評価してはなりません。</span><span class="sxs-lookup"><span data-stu-id="553d4-1147">It must not evaluate to a token.</span></span>

<span data-ttu-id="553d4-1148">このメソッドは、同じ名前の要素がすでに存在するかどうかをチェックしません。</span><span class="sxs-lookup"><span data-stu-id="553d4-1148">This method does not check if an element of the same name already exists.</span></span> <span data-ttu-id="553d4-1149">これは引数が AOT オブジェクトの有効な名前であることのみを検証します。</span><span class="sxs-lookup"><span data-stu-id="553d4-1149">It only validates that the argument is a valid name for an AOT object.</span></span> <span data-ttu-id="553d4-1150">重複する名前は、クラス、テーブル、拡張データ型または列挙内では存在しません。</span><span class="sxs-lookup"><span data-stu-id="553d4-1150">Duplicate names may not exist within classes, tables, extended data types, or enums.</span></span>

#### <a name="examples"></a><span data-ttu-id="553d4-1151">例</span><span class="sxs-lookup"><span data-stu-id="553d4-1151">Examples</span></span>

<span data-ttu-id="553d4-1152">次の例では、有効な引数と無効な引数の例を示しています。</span><span class="sxs-lookup"><span data-stu-id="553d4-1152">The following example gives examples of valid and invalid arguments.</span></span>

    boolean validName; 
    validName = TreeNode::isValidObjectName('ValidName'); //true 
    validName = TreeNode::isValidObjectName('Name with spaces'); //false 
    validName = TreeNode::isValidObjectName('4StartsWithDigit'); //false 
    validName = TreeNode::isValidObjectName('Illegal;Character'); //false 
    validName = TreeNode::isValidObjectName('if'); // false (token name)

### <a name="method-rootnode"></a><span data-ttu-id="553d4-1153">メソッド rootNode</span><span class="sxs-lookup"><span data-stu-id="553d4-1153">Method rootNode</span></span>

<span data-ttu-id="553d4-1154">AOT のルート ノードを返します。</span><span class="sxs-lookup"><span data-stu-id="553d4-1154">Returns the root node of the AOT.</span></span>

    public static TreeNode rootNode()

#### <a name="return-value"></a><span data-ttu-id="553d4-1155">戻り値</span><span class="sxs-lookup"><span data-stu-id="553d4-1155">Return Value</span></span>

<span data-ttu-id="553d4-1156">AOT のルート ノード。</span><span class="sxs-lookup"><span data-stu-id="553d4-1156">The root node of the AOT.</span></span>

#### <a name="remarks"></a><span data-ttu-id="553d4-1157">備考</span><span class="sxs-lookup"><span data-stu-id="553d4-1157">Remarks</span></span>

<span data-ttu-id="553d4-1158">このメソッドは、同様の機能を rootNode メソッドに提供します。</span><span class="sxs-lookup"><span data-stu-id="553d4-1158">The method provides similar functionality to the rootNode method.</span></span>

### <a name="method-sysobsoleteattribute"></a><span data-ttu-id="553d4-1159">メソッド SysObsoleteAttribute</span><span class="sxs-lookup"><span data-stu-id="553d4-1159">Method SysObsoleteAttribute</span></span>

    public void SysObsoleteAttribute()

### <a name="method-treenoderelease"></a><span data-ttu-id="553d4-1160">メソッド treeNodeRelease</span><span class="sxs-lookup"><span data-stu-id="553d4-1160">Method treeNodeRelease</span></span>

<span data-ttu-id="553d4-1161">ツリー ノードが明示的に解放されます。</span><span class="sxs-lookup"><span data-stu-id="553d4-1161">Releases the tree node explicitly.</span></span>

    public void treeNodeRelease()

#### <a name="remarks"></a><span data-ttu-id="553d4-1162">備考</span><span class="sxs-lookup"><span data-stu-id="553d4-1162">Remarks</span></span>

<span data-ttu-id="553d4-1163">ガベージコレクターが自動的にオブジェクトをアンロードするので、通常、オブジェクトを明示的にアンロードする必要はありません。</span><span class="sxs-lookup"><span data-stu-id="553d4-1163">Usually you do not have to explicitly unload objects, because the garbage collector will do it automatically.</span></span> <span data-ttu-id="553d4-1164">ただし、ツリー ノードは、通常 AOT にリンクされているため、ガベージ コレクションではありません。</span><span class="sxs-lookup"><span data-stu-id="553d4-1164">However, because tree nodes are ordinarily linked to the AOT, they are not garbage-collected.</span></span> <span data-ttu-id="553d4-1165">同じ方法で多くのツリー ノードでこのメソッドを実行する場合、リソースを要求する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="553d4-1165">If you run this method on many tree nodes in the same execution, it can be demanding on resources.</span></span> <span data-ttu-id="553d4-1166">ガベージ コレクターがツリー ノードを削除できるようにするには、作業中にツリー ノードをアンロードする必要があります。</span><span class="sxs-lookup"><span data-stu-id="553d4-1166">You should unload the tree nodes as you go along to give the garbage collector a chance to remove them.</span></span> <span data-ttu-id="553d4-1167">このメソッドを呼び出す前に、そのツリー ノードとそのサブノードに対するすべての参照を削除してください。</span><span class="sxs-lookup"><span data-stu-id="553d4-1167">Make sure to remove all references to the tree node and its subnodes before you call this method.</span></span> <span data-ttu-id="553d4-1168">このメソッドを呼び出す必要があるかどうかを判断するには、TreeNode.TreeNodeType().isConsumingMemory メソッドを使用します。</span><span class="sxs-lookup"><span data-stu-id="553d4-1168">Use the TreeNode.TreeNodeType().isConsumingMemory method to determine if you need to call this method.</span></span>

### <a name="method-sysobsoleteattribute"></a><span data-ttu-id="553d4-1169">メソッド SysObsoleteAttribute</span><span class="sxs-lookup"><span data-stu-id="553d4-1169">Method SysObsoleteAttribute</span></span>

    public void SysObsoleteAttribute(str name, xRefKind xrefKind, int lineNumber, int columNumber, [XRefReference xrefRef], [ClassId parentTypeId])

#### <a name="parameters"></a><span data-ttu-id="553d4-1170">パラメーター</span><span class="sxs-lookup"><span data-stu-id="553d4-1170">Parameters</span></span>

<span data-ttu-id="553d4-1171">名前</span><span class="sxs-lookup"><span data-stu-id="553d4-1171">name</span></span>  

<!-- -->

<span data-ttu-id="553d4-1172">xrefKind</span><span class="sxs-lookup"><span data-stu-id="553d4-1172">xrefKind</span></span>  

<!-- -->

<span data-ttu-id="553d4-1173">lineNumber</span><span class="sxs-lookup"><span data-stu-id="553d4-1173">lineNumber</span></span>  

<!-- -->

<span data-ttu-id="553d4-1174">columNumber</span><span class="sxs-lookup"><span data-stu-id="553d4-1174">columNumber</span></span>  

<!-- -->

<span data-ttu-id="553d4-1175">xrefRef</span><span class="sxs-lookup"><span data-stu-id="553d4-1175">xrefRef</span></span>  

<!-- -->

<span data-ttu-id="553d4-1176">parentTypeId</span><span class="sxs-lookup"><span data-stu-id="553d4-1176">parentTypeId</span></span>  

### <a name="method-aotrun"></a><span data-ttu-id="553d4-1177">メソッド AOTrun</span><span class="sxs-lookup"><span data-stu-id="553d4-1177">Method AOTrun</span></span>

<span data-ttu-id="553d4-1178">アプリケーション オブジェクト ツリー (AOT) でこのノードとそのサブツリーをコンパイルします。</span><span class="sxs-lookup"><span data-stu-id="553d4-1178">Compiles this node and its subtree in the Application Object Tree (AOT).</span></span>

    public void AOTrun()

### <a name="method-sysobsoleteattribute"></a><span data-ttu-id="553d4-1179">メソッド SysObsoleteAttribute</span><span class="sxs-lookup"><span data-stu-id="553d4-1179">Method SysObsoleteAttribute</span></span>

    public void SysObsoleteAttribute()

### <a name="method-aotrefresh"></a><span data-ttu-id="553d4-1180">メソッド AOTrefresh</span><span class="sxs-lookup"><span data-stu-id="553d4-1180">Method AOTrefresh</span></span>

<span data-ttu-id="553d4-1181">.aod ファイルを最新版に変更することによりノードを更新します。</span><span class="sxs-lookup"><span data-stu-id="553d4-1181">Refreshes the node with the latest changes to the .aod file.</span></span>

    public void AOTrefresh()

### <a name="method-sysobsoleteattribute"></a><span data-ttu-id="553d4-1182">メソッド SysObsoleteAttribute</span><span class="sxs-lookup"><span data-stu-id="553d4-1182">Method SysObsoleteAttribute</span></span>

    public void SysObsoleteAttribute(Struct struct1)

#### <a name="parameters"></a><span data-ttu-id="553d4-1183">パラメーター</span><span class="sxs-lookup"><span data-stu-id="553d4-1183">Parameters</span></span>

<span data-ttu-id="553d4-1184">struct1</span><span class="sxs-lookup"><span data-stu-id="553d4-1184">struct1</span></span>  

### <a name="method-sysobsoleteattribute"></a><span data-ttu-id="553d4-1185">メソッド SysObsoleteAttribute</span><span class="sxs-lookup"><span data-stu-id="553d4-1185">Method SysObsoleteAttribute</span></span>

    public void SysObsoleteAttribute(str properties)

#### <a name="parameters"></a><span data-ttu-id="553d4-1186">パラメーター</span><span class="sxs-lookup"><span data-stu-id="553d4-1186">Parameters</span></span>

<span data-ttu-id="553d4-1187">プロパティ</span><span class="sxs-lookup"><span data-stu-id="553d4-1187">properties</span></span>  

### <a name="method-aotconfigure"></a><span data-ttu-id="553d4-1188">メソッド AOTconfigure</span><span class="sxs-lookup"><span data-stu-id="553d4-1188">Method AOTconfigure</span></span>

    public void AOTconfigure()

### <a name="method-aotload"></a><span data-ttu-id="553d4-1189">メソッド AOTload</span><span class="sxs-lookup"><span data-stu-id="553d4-1189">Method AOTload</span></span>

<span data-ttu-id="553d4-1190">オブジェクトが読み込み済みであるか確認します。</span><span class="sxs-lookup"><span data-stu-id="553d4-1190">Ensures that the object is loaded.</span></span>

    public void AOTload()

### <a name="method-treenodeexport"></a><span data-ttu-id="553d4-1191">メソッド treeNodeExport</span><span class="sxs-lookup"><span data-stu-id="553d4-1191">Method treeNodeExport</span></span>

<span data-ttu-id="553d4-1192">アプリケーション オブジェクト ツリー (AOT) からノードとサブツリーをエキスポートします。</span><span class="sxs-lookup"><span data-stu-id="553d4-1192">Exports this node and its subtree from the Application Object Tree (AOT).</span></span>

    public void treeNodeExport(str filename, [int flag])

#### <a name="parameters"></a><span data-ttu-id="553d4-1193">パラメーター</span><span class="sxs-lookup"><span data-stu-id="553d4-1193">Parameters</span></span>

<span data-ttu-id="553d4-1194">filename</span><span class="sxs-lookup"><span data-stu-id="553d4-1194">filename</span></span>  

<!-- -->

<span data-ttu-id="553d4-1195">flag</span><span class="sxs-lookup"><span data-stu-id="553d4-1195">flag</span></span>  

#### <a name="remarks"></a><span data-ttu-id="553d4-1196">備考</span><span class="sxs-lookup"><span data-stu-id="553d4-1196">Remarks</span></span>

<span data-ttu-id="553d4-1197">攻撃者がこのメソッドへの入力を制御できる場合、セキュリティ上のリスクが存在します。</span><span class="sxs-lookup"><span data-stu-id="553d4-1197">If an attacker can control input to this method, a security risk exists.</span></span> <span data-ttu-id="553d4-1198">したがって、このメソッドは、コード アクセス セキュリティで実行されます。</span><span class="sxs-lookup"><span data-stu-id="553d4-1198">Therefore, this method runs under Code Access Security.</span></span> <span data-ttu-id="553d4-1199">サーバー上でこのメソッドを呼び出すには、 からのアクセス許可が必要です。</span><span class="sxs-lookup"><span data-stu-id="553d4-1199">Calls to this method on the server require permission from the .</span></span> <span data-ttu-id="553d4-1200">ユーザーがこのメソッドを呼び出すコントロールで、SysDevelopment へのセキュリティ キーを設定して開発権限があることを確認します。</span><span class="sxs-lookup"><span data-stu-id="553d4-1200">Ensure that the user has development privileges by setting the security key to SysDevelopment on the control that calls this method.</span></span>

#### <a name="examples"></a><span data-ttu-id="553d4-1201">例</span><span class="sxs-lookup"><span data-stu-id="553d4-1201">Examples</span></span>

<span data-ttu-id="553d4-1202">この例では、treeNodeExport メソッドを使用して、ExampleClass クラスを .xpo ファイルにエクスポートします。</span><span class="sxs-lookup"><span data-stu-id="553d4-1202">This example uses the treeNodeExport method to export the ExampleClass class to an .xpo file.</span></span>

    void TreeNodeExample() 
    { 
        TreeNode treeNode; 
        TreeNode childNode; 
        FileIoPermission perm; 
        #define.ExportFile(@"c:\TreeNodeExportExampleClass.xpo") 
        #define.ExportMode("w") 
        perm = new FileIoPermission(#ExportFile, #ExportMode); 
        if (perm == null) 
        { 
            return; 
        } 
        perm.assert(); 
        treeNode = TreeNode::findNode(@"\Classes"); 
        if (treeNode != null) 
        { 
            childNode = treeNode.AOTfindChild(@"ExampleClass"); 
            // BP deviation documented. 
            childNode.treeNodeExport(#ExportFile); 
        } 
        CodeAccessPermission::revertAssert(); 
    }

### <a name="method-sysobsoleteattribute"></a><span data-ttu-id="553d4-1203">メソッド SysObsoleteAttribute</span><span class="sxs-lookup"><span data-stu-id="553d4-1203">Method SysObsoleteAttribute</span></span>

    public void SysObsoleteAttribute(str source, [boolean isStatic])

#### <a name="parameters"></a><span data-ttu-id="553d4-1204">パラメーター</span><span class="sxs-lookup"><span data-stu-id="553d4-1204">Parameters</span></span>

<span data-ttu-id="553d4-1205">ソース</span><span class="sxs-lookup"><span data-stu-id="553d4-1205">source</span></span>  

<!-- -->

<span data-ttu-id="553d4-1206">isStatic</span><span class="sxs-lookup"><span data-stu-id="553d4-1206">isStatic</span></span>  

### <a name="method-aotendxref"></a><span data-ttu-id="553d4-1207">メソッド AOTendXref</span><span class="sxs-lookup"><span data-stu-id="553d4-1207">Method AOTendXref</span></span>

    public void AOTendXref()

### <a name="method-aotmessageline"></a><span data-ttu-id="553d4-1208">メソッド AOTmessageLine</span><span class="sxs-lookup"><span data-stu-id="553d4-1208">Method AOTmessageLine</span></span>

<span data-ttu-id="553d4-1209">アプリケーション オブジェクト ツリー (AOT) のメッセージ ウィンドウにテキストを記述します。</span><span class="sxs-lookup"><span data-stu-id="553d4-1209">Writes text to the Application Object Tree (AOT) Message window.</span></span>

    public void AOTmessageLine(str text, int linenumber)

#### <a name="parameters"></a><span data-ttu-id="553d4-1210">パラメーター</span><span class="sxs-lookup"><span data-stu-id="553d4-1210">Parameters</span></span>

<span data-ttu-id="553d4-1211">テキスト</span><span class="sxs-lookup"><span data-stu-id="553d4-1211">text</span></span>  
<span data-ttu-id="553d4-1212">無視される整数。</span><span class="sxs-lookup"><span data-stu-id="553d4-1212">An integer that is ignored.</span></span> <span data-ttu-id="553d4-1213">出力メッセージ ウィンドウでは書かれたテキストが特定の行番号に指定されていません。</span><span class="sxs-lookup"><span data-stu-id="553d4-1213">It does not currently direct the written text to a specific line number in the output Message window.</span></span>

<!-- -->

<span data-ttu-id="553d4-1214">linenumber</span><span class="sxs-lookup"><span data-stu-id="553d4-1214">linenumber</span></span>  
<span data-ttu-id="553d4-1215">無視される整数。</span><span class="sxs-lookup"><span data-stu-id="553d4-1215">An integer that is ignored.</span></span> <span data-ttu-id="553d4-1216">出力メッセージ ウィンドウでは書かれたテキストが特定の行番号に指定されていません。</span><span class="sxs-lookup"><span data-stu-id="553d4-1216">It does not currently direct the written text to a specific line number in the output Message window.</span></span>

#### <a name="remarks"></a><span data-ttu-id="553d4-1217">備考</span><span class="sxs-lookup"><span data-stu-id="553d4-1217">Remarks</span></span>

<span data-ttu-id="553d4-1218">このメソッドは、テキストを出力するために使用されます。そのためユーザーは後でメッセージ ウィンドウ内のそのテキスト行をダブルクリックすると、このノードに関して何らかのアクションが発生します。</span><span class="sxs-lookup"><span data-stu-id="553d4-1218">This method is intended to be used to output text so that when the user later double-clicks that line of text in the message window, some action will happen regarding this node.</span></span>

#### <a name="examples"></a><span data-ttu-id="553d4-1219">例</span><span class="sxs-lookup"><span data-stu-id="553d4-1219">Examples</span></span>

<span data-ttu-id="553d4-1220">次の例では、フォームが TreeNode からこのメソッドを継承するために、フォーム オブジェクトに対して AOTmessageLine メソッドを実行します。</span><span class="sxs-lookup"><span data-stu-id="553d4-1220">The following example executes the AOTmessageLine method on a Form object, because Form inherits this method from TreeNode.</span></span>

    static void JobAOTmessageLineDemo(Args _args) 
    { 
        Form f = new Form('testAOTMessageLine'); 
        // 
        f.AOTmessageLine('test message 1a',1); 
        f.AOTmessageLine('test message 2a',2); 
        f.AOTmessageLine('test message 3a',3); 
        f.AOTmessageLine('test message 1b',1); 
        f.AOTmessageLine('test message 2b',2); 
        f.AOTmessageLine('test message 3b',3); 
        f.AOTmessageLine('test message 2c',2); 
        // 
        /******* 
        Actual Output in the Message window 
        (the 7 identical lines): 
        test message 2c 
        test message 2c 
        test message 2c 
        test message 2c 
        test message 2c 
        test message 2c 
        test message 2c 
        *******/ 
    }

### <a name="method-sysobsoleteattribute"></a><span data-ttu-id="553d4-1221">メソッド SysObsoleteAttribute</span><span class="sxs-lookup"><span data-stu-id="553d4-1221">Method SysObsoleteAttribute</span></span>

    public void SysObsoleteAttribute(str name, AnyType value)

#### <a name="parameters"></a><span data-ttu-id="553d4-1222">パラメーター</span><span class="sxs-lookup"><span data-stu-id="553d4-1222">Parameters</span></span>

<span data-ttu-id="553d4-1223">名前</span><span class="sxs-lookup"><span data-stu-id="553d4-1223">name</span></span>  

<!-- -->

<span data-ttu-id="553d4-1224">値</span><span class="sxs-lookup"><span data-stu-id="553d4-1224">value</span></span>  

### <a name="method-aotrestore"></a><span data-ttu-id="553d4-1225">メソッド AOTrestore</span><span class="sxs-lookup"><span data-stu-id="553d4-1225">Method AOTrestore</span></span>

<span data-ttu-id="553d4-1226">該当する場合は、ディスクからこのノードを再読み込みします。</span><span class="sxs-lookup"><span data-stu-id="553d4-1226">Reloads this node from the disk, if applicable.</span></span>

    public void AOTrestore([boolean forceReload])

#### <a name="parameters"></a><span data-ttu-id="553d4-1227">パラメーター</span><span class="sxs-lookup"><span data-stu-id="553d4-1227">Parameters</span></span>

<span data-ttu-id="553d4-1228">forceReload</span><span class="sxs-lookup"><span data-stu-id="553d4-1228">forceReload</span></span>  

### <a name="method-aotregenerate"></a><span data-ttu-id="553d4-1229">メソッド AOTregenerate</span><span class="sxs-lookup"><span data-stu-id="553d4-1229">Method AOTregenerate</span></span>

    public void AOTregenerate()

### <a name="method-aotmakexref"></a><span data-ttu-id="553d4-1230">メソッド AOTmakeXref</span><span class="sxs-lookup"><span data-stu-id="553d4-1230">Method AOTmakeXref</span></span>

<span data-ttu-id="553d4-1231">このノードとそのサブツリーを AOT でコンパイルし、相互参照システムを更新します。</span><span class="sxs-lookup"><span data-stu-id="553d4-1231">Compiles this node and its subtree in the AOT, updating the cross-reference system.</span></span>

    public void AOTmakeXref([int flag], [boolean xRefAll])

#### <a name="parameters"></a><span data-ttu-id="553d4-1232">パラメーター</span><span class="sxs-lookup"><span data-stu-id="553d4-1232">Parameters</span></span>

<span data-ttu-id="553d4-1233">flag</span><span class="sxs-lookup"><span data-stu-id="553d4-1233">flag</span></span>  

<!-- -->

<span data-ttu-id="553d4-1234">xRefAll</span><span class="sxs-lookup"><span data-stu-id="553d4-1234">xRefAll</span></span>  

#### <a name="remarks"></a><span data-ttu-id="553d4-1235">備考</span><span class="sxs-lookup"><span data-stu-id="553d4-1235">Remarks</span></span>

<span data-ttu-id="553d4-1236">このメソッドは、任意の場所で呼び出すことができます。</span><span class="sxs-lookup"><span data-stu-id="553d4-1236">This method can be called at any:</span></span>

-   <span data-ttu-id="553d4-1237">リスト ノード (AOT、テーブル、フォーム、プロジェクトのルート、およびグループ)</span><span class="sxs-lookup"><span data-stu-id="553d4-1237">list node (such as AOT, Tables, Forms, Project roots, and groups)</span></span>
-   <span data-ttu-id="553d4-1238">アプリケーション オブジェクト (テーブルやフォームなど)</span><span class="sxs-lookup"><span data-stu-id="553d4-1238">Application Object (such as a Table or Form)</span></span>
-   <span data-ttu-id="553d4-1239">メソッドの分岐</span><span class="sxs-lookup"><span data-stu-id="553d4-1239">methods branch</span></span>
-   <span data-ttu-id="553d4-1240">メソッド</span><span class="sxs-lookup"><span data-stu-id="553d4-1240">method</span></span>

### <a name="method-aotedit"></a><span data-ttu-id="553d4-1241">メソッド AOTedit</span><span class="sxs-lookup"><span data-stu-id="553d4-1241">Method AOTedit</span></span>

<span data-ttu-id="553d4-1242">このノードの適切なエディタを開きます。</span><span class="sxs-lookup"><span data-stu-id="553d4-1242">Opens the appropriate editor for this node.</span></span>

    public void AOTedit([int Line], [int Column])

#### <a name="parameters"></a><span data-ttu-id="553d4-1243">パラメーター</span><span class="sxs-lookup"><span data-stu-id="553d4-1243">Parameters</span></span>

<span data-ttu-id="553d4-1244">明細行</span><span class="sxs-lookup"><span data-stu-id="553d4-1244">Line</span></span>  
<span data-ttu-id="553d4-1245">カーソル位置の列 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="553d4-1245">The column of the cursor position; optional.</span></span>

<!-- -->

<span data-ttu-id="553d4-1246">円柱</span><span class="sxs-lookup"><span data-stu-id="553d4-1246">Column</span></span>  
<span data-ttu-id="553d4-1247">カーソル位置の列 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="553d4-1247">The column of the cursor position; optional.</span></span>

#### <a name="remarks"></a><span data-ttu-id="553d4-1248">備考</span><span class="sxs-lookup"><span data-stu-id="553d4-1248">Remarks</span></span>

<span data-ttu-id="553d4-1249">ノードがメソッドである場合は、コード エディタが開きます。</span><span class="sxs-lookup"><span data-stu-id="553d4-1249">If the node is a method, the code editor will open.</span></span> <span data-ttu-id="553d4-1250">ノードがドキュメンテーションの対象である場合は、ヘルプ エディタが開きます。</span><span class="sxs-lookup"><span data-stu-id="553d4-1250">If the node is a documentation object, the Help editor will open.</span></span>

#### <a name="examples"></a><span data-ttu-id="553d4-1251">例</span><span class="sxs-lookup"><span data-stu-id="553d4-1251">Examples</span></span>

<span data-ttu-id="553d4-1252">次のコード例は、X++ エディターを開き、クラス Tax のクラス宣言を表示し、ポインタを 6 行目、8 列目に配置します。</span><span class="sxs-lookup"><span data-stu-id="553d4-1252">The following code example opens the X++ editor, shows the class declaration of the class Tax, and positions the pointer at line 6, column 8.</span></span>

    #AOT 
    static void myJobAOTEdit(Args _args) 
    { 
        treeNode treeNode; 
        treeNode = TreeNode::findNode(#ClassesPath + '\\' + classStr(Tax)+ '\\ClassDeclaration'); 
        if (treeNode) 
        { 
            treeNode.AOTedit(6,8); 
        } 
        else 
        { 
            print "Could not find treeNode"; 
        } 
        pause; 
    }

### <a name="method-aotshowproperties"></a><span data-ttu-id="553d4-1253">メソッド AOTshowProperties</span><span class="sxs-lookup"><span data-stu-id="553d4-1253">Method AOTshowProperties</span></span>

<span data-ttu-id="553d4-1254">プロパティ シートを開いて、(まだ開かれていない場合) このノードのプロパティを表示します。</span><span class="sxs-lookup"><span data-stu-id="553d4-1254">Opens the property sheet (if not already open) and shows the properties for this node.</span></span>

    public void AOTshowProperties()

### <a name="method-aotinsert"></a><span data-ttu-id="553d4-1255">メソッド AOTinsert</span><span class="sxs-lookup"><span data-stu-id="553d4-1255">Method AOTinsert</span></span>

<span data-ttu-id="553d4-1256">このノードのサブノード間にノードを挿入します。</span><span class="sxs-lookup"><span data-stu-id="553d4-1256">Inserts a node among the subnodes of this node.</span></span>

    public void AOTinsert(TreeNode parent, [TreeNode after], [boolean doNotDuplicate])

#### <a name="parameters"></a><span data-ttu-id="553d4-1257">パラメーター</span><span class="sxs-lookup"><span data-stu-id="553d4-1257">Parameters</span></span>

<span data-ttu-id="553d4-1258">parent</span><span class="sxs-lookup"><span data-stu-id="553d4-1258">parent</span></span>  

<!-- -->

<span data-ttu-id="553d4-1259">以後</span><span class="sxs-lookup"><span data-stu-id="553d4-1259">after</span></span>  

<!-- -->

<span data-ttu-id="553d4-1260">doNotDuplicate</span><span class="sxs-lookup"><span data-stu-id="553d4-1260">doNotDuplicate</span></span>  

### <a name="method-new"></a><span data-ttu-id="553d4-1261">メソッド new</span><span class="sxs-lookup"><span data-stu-id="553d4-1261">Method new</span></span>

<span data-ttu-id="553d4-1262">TreeNode クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="553d4-1262">Initializes a new instance of the TreeNode class.</span></span>

    public void new()

### <a name="method-aotmove"></a><span data-ttu-id="553d4-1263">メソッド AOTMove</span><span class="sxs-lookup"><span data-stu-id="553d4-1263">Method AOTMove</span></span>

    public void AOTMove(TreeNode parent, [TreeNode after])

#### <a name="parameters"></a><span data-ttu-id="553d4-1264">パラメーター</span><span class="sxs-lookup"><span data-stu-id="553d4-1264">Parameters</span></span>

<span data-ttu-id="553d4-1265">parent</span><span class="sxs-lookup"><span data-stu-id="553d4-1265">parent</span></span>  

<!-- -->

<span data-ttu-id="553d4-1266">以後</span><span class="sxs-lookup"><span data-stu-id="553d4-1266">after</span></span>  

### <a name="method-sysobsoleteattribute"></a><span data-ttu-id="553d4-1267">メソッド SysObsoleteAttribute</span><span class="sxs-lookup"><span data-stu-id="553d4-1267">Method SysObsoleteAttribute</span></span>

    public void SysObsoleteAttribute(int modelId)

#### <a name="parameters"></a><span data-ttu-id="553d4-1268">パラメーター</span><span class="sxs-lookup"><span data-stu-id="553d4-1268">Parameters</span></span>

<span data-ttu-id="553d4-1269">modelId</span><span class="sxs-lookup"><span data-stu-id="553d4-1269">modelId</span></span>  

## <a name="class-treenodeiterator"></a><span data-ttu-id="553d4-1270">クラス TreeNodeIterator</span><span class="sxs-lookup"><span data-stu-id="553d4-1270">Class TreeNodeIterator</span></span>
    class TreeNodeIterator extends Object

<span data-ttu-id="553d4-1271">TreeNodeIterator クラスは、ツリー ノードの子ノード上を移動します。</span><span class="sxs-lookup"><span data-stu-id="553d4-1271">The TreeNodeIterator class traverses the child nodes of a tree node.</span></span>

### <a name="remarks"></a><span data-ttu-id="553d4-1272">備考</span><span class="sxs-lookup"><span data-stu-id="553d4-1272">Remarks</span></span>

### <a name="examples"></a><span data-ttu-id="553d4-1273">例</span><span class="sxs-lookup"><span data-stu-id="553d4-1273">Examples</span></span>

<span data-ttu-id="553d4-1274">次の例では、ルート ノードのすべての子ノードの名前を出力します。</span><span class="sxs-lookup"><span data-stu-id="553d4-1274">The following example prints the names of all child nodes of the root node.</span></span>

    static void example()  
    { 
        treeNode myTreeNode; 
        xInfo xi = new xInfo(); 
        void printChildNames (treeNode t) 
        { 
            treeNode child; 
            treenodeIterator it; 
            it = t.AOTiterator(); 
            child = it.next(); 
            while (child) 
            { 
                print child.treeNodeName(); 
                child = it.next(); 
            } 
        } 
        myTreeNode = xi.rootNode(); 
        printChildNames(myTreeNode); 
        pause; 
    }

### <a name="methods"></a><span data-ttu-id="553d4-1275">メソッド</span><span class="sxs-lookup"><span data-stu-id="553d4-1275">Methods</span></span>

| <span data-ttu-id="553d4-1276">方法</span><span class="sxs-lookup"><span data-stu-id="553d4-1276">Method</span></span>                 | <span data-ttu-id="553d4-1277">説明</span><span class="sxs-lookup"><span data-stu-id="553d4-1277">Description</span></span>                                                                                            |
|------------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="553d4-1278">public TreeNode next()</span><span class="sxs-lookup"><span data-stu-id="553d4-1278">public TreeNode next()</span></span> | <span data-ttu-id="553d4-1279">子ノードの一覧の次の要素を取得します。</span><span class="sxs-lookup"><span data-stu-id="553d4-1279">Retrieves the next element in the list of child nodes.</span></span>                                                 |
| <span data-ttu-id="553d4-1280">public void reset()</span><span class="sxs-lookup"><span data-stu-id="553d4-1280">public void reset()</span></span>    | <span data-ttu-id="553d4-1281">次のメソッドの次の呼び出しが一覧の最初の子ノードを返すように反復子をリセットします。</span><span class="sxs-lookup"><span data-stu-id="553d4-1281">Resets the iterator so that the next call to the next method returns the first child node in the list.</span></span> |

### <a name="method-next"></a><span data-ttu-id="553d4-1282">メソッド next</span><span class="sxs-lookup"><span data-stu-id="553d4-1282">Method next</span></span>

<span data-ttu-id="553d4-1283">子ノードの一覧の次の要素を取得します。</span><span class="sxs-lookup"><span data-stu-id="553d4-1283">Retrieves the next element in the list of child nodes.</span></span>

    public TreeNode next()

#### <a name="return-value"></a><span data-ttu-id="553d4-1284">戻り値</span><span class="sxs-lookup"><span data-stu-id="553d4-1284">Return Value</span></span>

<span data-ttu-id="553d4-1285">ツリー内の次の子ノード。</span><span class="sxs-lookup"><span data-stu-id="553d4-1285">The next child node in the tree.</span></span>

### <a name="method-reset"></a><span data-ttu-id="553d4-1286">メソッド reset</span><span class="sxs-lookup"><span data-stu-id="553d4-1286">Method reset</span></span>

<span data-ttu-id="553d4-1287">次のメソッドの次の呼び出しが一覧の最初の子ノードを返すように反復子をリセットします。</span><span class="sxs-lookup"><span data-stu-id="553d4-1287">Resets the iterator so that the next call to the next method returns the first child node in the list.</span></span>

    public void reset()

## <a name="class-treenodetype"></a><span data-ttu-id="553d4-1288">クラス TreeNodeType</span><span class="sxs-lookup"><span data-stu-id="553d4-1288">Class TreeNodeType</span></span>
    class TreeNodeType extends Object

<span data-ttu-id="553d4-1289">TreeNodeType クラスは、TreeNode クラスのタイプに関する情報を取得します。</span><span class="sxs-lookup"><span data-stu-id="553d4-1289">The TreeNodeType class retrieves information about types of TreeNode classes.</span></span>

### <a name="remarks"></a><span data-ttu-id="553d4-1290">備考</span><span class="sxs-lookup"><span data-stu-id="553d4-1290">Remarks</span></span>

<span data-ttu-id="553d4-1291">このクラスを使用すると、TreeNode クラスのインスタンスを反映させることができます。</span><span class="sxs-lookup"><span data-stu-id="553d4-1291">This class enable you to reflect on a TreeNode class instance.</span></span> <span data-ttu-id="553d4-1292">リフレクション情報は、TreeNode クラスのインスタンスに固有ではありません。</span><span class="sxs-lookup"><span data-stu-id="553d4-1292">The reflection information is not specific to an instance of a TreeNode class.</span></span> <span data-ttu-id="553d4-1293">同じ NodeType を持つすべての TreeNode インスタンスは、同じ TreeNodeType を共有します。</span><span class="sxs-lookup"><span data-stu-id="553d4-1293">All TreeNode instances with the same NodeType share the same TreeNodeType.</span></span> <span data-ttu-id="553d4-1294">TreeNode.TreeNodeType メソッドは、リフレクション情報を含む treeNodeType オブジェクトを返します。</span><span class="sxs-lookup"><span data-stu-id="553d4-1294">The TreeNode.TreeNodeType method return a treeNodeType object with the reflection information.</span></span>

### <a name="examples"></a><span data-ttu-id="553d4-1295">例</span><span class="sxs-lookup"><span data-stu-id="553d4-1295">Examples</span></span>

### <a name="methods"></a><span data-ttu-id="553d4-1296">メソッド</span><span class="sxs-lookup"><span data-stu-id="553d4-1296">Methods</span></span>

| <span data-ttu-id="553d4-1297">方法</span><span class="sxs-lookup"><span data-stu-id="553d4-1297">Method</span></span>                                     | <span data-ttu-id="553d4-1298">説明</span><span class="sxs-lookup"><span data-stu-id="553d4-1298">Description</span></span>                                                                                            |
|--------------------------------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="553d4-1299">public int id()</span><span class="sxs-lookup"><span data-stu-id="553d4-1299">public int id()</span></span>                            | <span data-ttu-id="553d4-1300">タイプの ID を返します。</span><span class="sxs-lookup"><span data-stu-id="553d4-1300">Returns the type's ID.</span></span>                                                                                 |
| <span data-ttu-id="553d4-1301">public boolean isConsumingMemory()</span><span class="sxs-lookup"><span data-stu-id="553d4-1301">public boolean isConsumingMemory()</span></span>         | <span data-ttu-id="553d4-1302">このノード タイプのインスタンスが手動で解放が必要なメモリを消費するかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="553d4-1302">Indicates whether instances of this node type are consuming memory that needs to be manually released.</span></span> |
| <span data-ttu-id="553d4-1303">public boolean isGetNodeInLayerSupported()</span><span class="sxs-lookup"><span data-stu-id="553d4-1303">public boolean isGetNodeInLayerSupported()</span></span> | <span data-ttu-id="553d4-1304">このノード タイプのインスタンスが TreeNode.GetNodeInLayer メソッドをサポートするかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="553d4-1304">Indicates whether instances of this node type support the TreeNode.GetNodeInLayer method.</span></span>              |
| <span data-ttu-id="553d4-1305">public boolean isLayerAware()</span><span class="sxs-lookup"><span data-stu-id="553d4-1305">public boolean isLayerAware()</span></span>              | <span data-ttu-id="553d4-1306">このノード タイプのインスタンスが AOT でレイヤーで修飾されているかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="553d4-1306">Indicates whether instances of this node type are decorated with layers in the AOT.</span></span>                    |
| <span data-ttu-id="553d4-1307">public boolean isModelElement()</span><span class="sxs-lookup"><span data-stu-id="553d4-1307">public boolean isModelElement()</span></span>            | <span data-ttu-id="553d4-1308">このノード タイプのインスタンスがモデル要素かどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="553d4-1308">Indicates whether instances of this node type are model-elements.</span></span>                                      |
| <span data-ttu-id="553d4-1309">public boolean isRootElement()</span><span class="sxs-lookup"><span data-stu-id="553d4-1309">public boolean isRootElement()</span></span>             | <span data-ttu-id="553d4-1310">このノード タイプのインスタンスがルート要素かどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="553d4-1310">Indicates whether instances of this node type are root-elements.</span></span>                                       |
| <span data-ttu-id="553d4-1311">public boolean isUtilElement()</span><span class="sxs-lookup"><span data-stu-id="553d4-1311">public boolean isUtilElement()</span></span>             | <span data-ttu-id="553d4-1312">このノード タイプのインスタンスがユーティリティ要素かどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="553d4-1312">Indicates whether instances of this node type are util-elements.</span></span>                                       |
| <span data-ttu-id="553d4-1313">public boolean isVCSControllableElement()</span><span class="sxs-lookup"><span data-stu-id="553d4-1313">public boolean isVCSControllableElement()</span></span>  |                                                                                                        |
| <span data-ttu-id="553d4-1314">private void new()</span><span class="sxs-lookup"><span data-stu-id="553d4-1314">private void new()</span></span>                         | <span data-ttu-id="553d4-1315">TreeNodeType クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="553d4-1315">Initializes a new instance of the TreeNodeType class.</span></span>                                                  |

### <a name="method-id"></a><span data-ttu-id="553d4-1316">メソッド id</span><span class="sxs-lookup"><span data-stu-id="553d4-1316">Method id</span></span>

<span data-ttu-id="553d4-1317">タイプの ID を返します。</span><span class="sxs-lookup"><span data-stu-id="553d4-1317">Returns the type's ID.</span></span>

    public int id()

#### <a name="return-value"></a><span data-ttu-id="553d4-1318">戻り値</span><span class="sxs-lookup"><span data-stu-id="553d4-1318">Return Value</span></span>

<span data-ttu-id="553d4-1319">TreeNodeType の ID。</span><span class="sxs-lookup"><span data-stu-id="553d4-1319">The ID of the TreeNodeType.</span></span>

### <a name="method-isconsumingmemory"></a><span data-ttu-id="553d4-1320">メソッド isConsumingMemory</span><span class="sxs-lookup"><span data-stu-id="553d4-1320">Method isConsumingMemory</span></span>

<span data-ttu-id="553d4-1321">このノード タイプのインスタンスが手動で解放が必要なメモリを消費するかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="553d4-1321">Indicates whether instances of this node type are consuming memory that needs to be manually released.</span></span>

    public boolean isConsumingMemory()

#### <a name="return-value"></a><span data-ttu-id="553d4-1322">戻り値</span><span class="sxs-lookup"><span data-stu-id="553d4-1322">Return Value</span></span>

<span data-ttu-id="553d4-1323">このタイプのツリー ノードがメモリを消費する場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="553d4-1323">true if tree nodes of this type consumes memory; otherwise, false.</span></span>

#### <a name="remarks"></a><span data-ttu-id="553d4-1324">備考</span><span class="sxs-lookup"><span data-stu-id="553d4-1324">Remarks</span></span>

<span data-ttu-id="553d4-1325">このタイプの TreeNode インスタンスで作業した後は、TreeNode.TreeNodeRelease メソッドを呼び出して、消費されたメモリを解放することが重要です。</span><span class="sxs-lookup"><span data-stu-id="553d4-1325">After working with TreeNode instances of this type it is important to call the TreeNode.TreeNodeRelease method to release any consumed memory.</span></span> <span data-ttu-id="553d4-1326">これを行わないと、メモリ不足の例外が発生します。</span><span class="sxs-lookup"><span data-stu-id="553d4-1326">Failure to do this will result in out-of-memory exceptions.</span></span> <span data-ttu-id="553d4-1327">構成階層における TreeNode クラスの全てのインスタンスがガベージ コレクションになる前に、TreeNode.TreeNodeRelease メソッドを呼び出さないでください。</span><span class="sxs-lookup"><span data-stu-id="553d4-1327">Do not call the TreeNode.TreeNodeRelease method before all instances of TreeNode classes in the composition hierarchy has been garbage collected.</span></span> <span data-ttu-id="553d4-1328">たとえば、MyClass.myMethod の TreeNode がまだある場合、MyClass で TreeNode.TreeNodeRelease() メソッドを呼び出さないでください。</span><span class="sxs-lookup"><span data-stu-id="553d4-1328">For example, do not call the TreeNode.TreeNodeRelease() method on MyClass, if you still have a TreeNode instance of MyClass.myMethod.</span></span>

### <a name="method-isgetnodeinlayersupported"></a><span data-ttu-id="553d4-1329">メソッド isGetNodeInLayerSupported</span><span class="sxs-lookup"><span data-stu-id="553d4-1329">Method isGetNodeInLayerSupported</span></span>

<span data-ttu-id="553d4-1330">このノード タイプのインスタンスが TreeNode.GetNodeInLayer メソッドをサポートするかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="553d4-1330">Indicates whether instances of this node type support the TreeNode.GetNodeInLayer method.</span></span>

    public boolean isGetNodeInLayerSupported()

#### <a name="return-value"></a><span data-ttu-id="553d4-1331">戻り値</span><span class="sxs-lookup"><span data-stu-id="553d4-1331">Return Value</span></span>

<span data-ttu-id="553d4-1332">このタイプのツリー ノードが TreeNode.GetNodeInLayer メソッドをサポートする場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="553d4-1332">true if tree nodes of this type support the TreeNode.GetNodeInLayer method; otherwise, false.</span></span>

### <a name="method-islayeraware"></a><span data-ttu-id="553d4-1333">メソッド isLayerAware</span><span class="sxs-lookup"><span data-stu-id="553d4-1333">Method isLayerAware</span></span>

<span data-ttu-id="553d4-1334">このノード タイプのインスタンスが AOT でレイヤーで修飾されているかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="553d4-1334">Indicates whether instances of this node type are decorated with layers in the AOT.</span></span>

    public boolean isLayerAware()

#### <a name="return-value"></a><span data-ttu-id="553d4-1335">戻り値</span><span class="sxs-lookup"><span data-stu-id="553d4-1335">Return Value</span></span>

<span data-ttu-id="553d4-1336">このタイプのツリー ノードがレイヤーで修飾された場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="553d4-1336">true if tree nodes of this type are decorated with layers; otherwise, false.</span></span>

#### <a name="remarks"></a><span data-ttu-id="553d4-1337">備考</span><span class="sxs-lookup"><span data-stu-id="553d4-1337">Remarks</span></span>

<span data-ttu-id="553d4-1338">このタイプのツリー ノードは、AOTLayer メソッドと AOTLayers メソッドをサポートします。</span><span class="sxs-lookup"><span data-stu-id="553d4-1338">Tree nodes of this type support the AOTLayer and AOTLayers methods.</span></span>

### <a name="method-ismodelelement"></a><span data-ttu-id="553d4-1339">メソッド isModelElement</span><span class="sxs-lookup"><span data-stu-id="553d4-1339">Method isModelElement</span></span>

<span data-ttu-id="553d4-1340">このノード タイプのインスタンスがモデル要素かどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="553d4-1340">Indicates whether instances of this node type are model-elements.</span></span>

    public boolean isModelElement()

#### <a name="return-value"></a><span data-ttu-id="553d4-1341">戻り値</span><span class="sxs-lookup"><span data-stu-id="553d4-1341">Return Value</span></span>

<span data-ttu-id="553d4-1342">このタイプのツリー ノードがモデル要素である場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="553d4-1342">true if tree nodes of this type are model-elements; otherwise, false.</span></span>

#### <a name="remarks"></a><span data-ttu-id="553d4-1343">備考</span><span class="sxs-lookup"><span data-stu-id="553d4-1343">Remarks</span></span>

<span data-ttu-id="553d4-1344">モデル要素は、モデル ストアに保持される (または保持できる) ツリー ノードです。</span><span class="sxs-lookup"><span data-stu-id="553d4-1344">A model-element is a tree node that is (or can be) persisted in the model store.</span></span> <span data-ttu-id="553d4-1345">各モデル要素ツリー ノードについては、1 つのレコードはモデル ストアの ModelElements テーブル内に表示されます。</span><span class="sxs-lookup"><span data-stu-id="553d4-1345">For each model-element tree node one record can be found in the ModelElements table in the model store.</span></span> <span data-ttu-id="553d4-1346">モデル要素は、AOT 内で含まれているモデルの名前で視覚的に修飾されます。</span><span class="sxs-lookup"><span data-stu-id="553d4-1346">Model-elements are visually decorated with the name of the Model they are contained by in the AOT.</span></span>

### <a name="method-isrootelement"></a><span data-ttu-id="553d4-1347">メソッド isRootElement</span><span class="sxs-lookup"><span data-stu-id="553d4-1347">Method isRootElement</span></span>

<span data-ttu-id="553d4-1348">このノード タイプのインスタンスがルート要素かどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="553d4-1348">Indicates whether instances of this node type are root-elements.</span></span>

    public boolean isRootElement()

#### <a name="return-value"></a><span data-ttu-id="553d4-1349">戻り値</span><span class="sxs-lookup"><span data-stu-id="553d4-1349">Return Value</span></span>

<span data-ttu-id="553d4-1350">このタイプのツリー ノードがルート要素である場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="553d4-1350">true if tree nodes of this type are root-elements; otherwise, false.</span></span>

#### <a name="remarks"></a><span data-ttu-id="553d4-1351">備考</span><span class="sxs-lookup"><span data-stu-id="553d4-1351">Remarks</span></span>

<span data-ttu-id="553d4-1352">ルート要素は、ツリー ノードの構成階層のルートです。</span><span class="sxs-lookup"><span data-stu-id="553d4-1352">A root-element is the root in a composition hierarchy of tree nodes.</span></span> <span data-ttu-id="553d4-1353">ルート要素は、モデル要素の親を持つことはありません。</span><span class="sxs-lookup"><span data-stu-id="553d4-1353">A root-element never has a model-element parent.</span></span> <span data-ttu-id="553d4-1354">例には、MyTable、MyClass、MyForm が含まれます。</span><span class="sxs-lookup"><span data-stu-id="553d4-1354">Examples include MyTable, MyClass, MyForm.</span></span>

### <a name="method-isutilelement"></a><span data-ttu-id="553d4-1355">メソッド isUtilElement</span><span class="sxs-lookup"><span data-stu-id="553d4-1355">Method isUtilElement</span></span>

<span data-ttu-id="553d4-1356">このノード タイプのインスタンスがユーティリティ要素かどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="553d4-1356">Indicates whether instances of this node type are util-elements.</span></span>

    public boolean isUtilElement()

#### <a name="return-value"></a><span data-ttu-id="553d4-1357">戻り値</span><span class="sxs-lookup"><span data-stu-id="553d4-1357">Return Value</span></span>

<span data-ttu-id="553d4-1358">このタイプのツリー ノードがユーティリティ要素である場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="553d4-1358">true if tree nodes of this type are util-elements; otherwise, false.</span></span>

#### <a name="remarks"></a><span data-ttu-id="553d4-1359">備考</span><span class="sxs-lookup"><span data-stu-id="553d4-1359">Remarks</span></span>

<span data-ttu-id="553d4-1360">ユーティリティ要素は UtilElements と UtilIdElements ビューからアクセスできるツリー ノードです。</span><span class="sxs-lookup"><span data-stu-id="553d4-1360">An util-element is a tree node that can be accessed via the UtilElements and UtilIdElements views.</span></span> <span data-ttu-id="553d4-1361">Util 要素はモデル要素のサブセットです。</span><span class="sxs-lookup"><span data-stu-id="553d4-1361">Util-elements are a subset of model-elements.</span></span>

### <a name="method-isvcscontrollableelement"></a><span data-ttu-id="553d4-1362">メソッド isVCSControllableElement</span><span class="sxs-lookup"><span data-stu-id="553d4-1362">Method isVCSControllableElement</span></span>

    public boolean isVCSControllableElement()

#### <a name="return-value"></a><span data-ttu-id="553d4-1363">戻り値</span><span class="sxs-lookup"><span data-stu-id="553d4-1363">Return Value</span></span>

### <a name="method-new"></a><span data-ttu-id="553d4-1364">メソッド new</span><span class="sxs-lookup"><span data-stu-id="553d4-1364">Method new</span></span>

<span data-ttu-id="553d4-1365">TreeNodeType クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="553d4-1365">Initializes a new instance of the TreeNodeType class.</span></span>

    private void new()


