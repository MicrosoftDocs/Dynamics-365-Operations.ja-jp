---
title: TextIo クラス
description: このトピックでは、TextIo クラスについて説明します。
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
ms.openlocfilehash: 3fb555eb5629b90a4eec4f8af5a0451720f2abd9
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502789"
---
# <a name="class-textio"></a><span data-ttu-id="5bec7-103">クラス TextIo</span><span class="sxs-lookup"><span data-stu-id="5bec7-103">Class TextIo</span></span>

[!include [banner](../../includes/banner.md)]

```xpp
class TextIo extends CommaIo
```

<span data-ttu-id="5bec7-104">TextIo クラスには、テキスト ファイルの読み取りと書き込みを行う機能があります。</span><span class="sxs-lookup"><span data-stu-id="5bec7-104">The TextIo class provides functionality for reading and writing text files.</span></span>

## <a name="remarks"></a><span data-ttu-id="5bec7-105">備考</span><span class="sxs-lookup"><span data-stu-id="5bec7-105">Remarks</span></span>

<span data-ttu-id="5bec7-106">TextIO は、非 ANSI コード ページ ファイル I/O のサポートを提供する AsciiIO を置き換えます。</span><span class="sxs-lookup"><span data-stu-id="5bec7-106">TextIO replaces AsciiIO to provide support for non-ANSI code page file I/O.</span></span> <span data-ttu-id="5bec7-107">TextIO コンストラクターには、ファイルのコード ページを設定するための追加のオプション パラメーターがあります。</span><span class="sxs-lookup"><span data-stu-id="5bec7-107">The TextIO constructor has an additional optional parameter to set the code page of the file.</span></span> <span data-ttu-id="5bec7-108">TextIO.new メソッドには、ファイルのコード ページを指定するオプション引数があります。</span><span class="sxs-lookup"><span data-stu-id="5bec7-108">The TextIO.new method has an optional argument that specifies the code page of the file.</span></span> <span data-ttu-id="5bec7-109">既定値は UTF-16LE (Microsoft Windows ネイティブ Unicode 表現) です。</span><span class="sxs-lookup"><span data-stu-id="5bec7-109">The default value is UTF-16LE (the Microsoft Windows native Unicode representation).</span></span> <span data-ttu-id="5bec7-110">ほとんどの場合、特にエンドユーザーが Finance and Operations アプリケーション以外のテキスト エディターでファイルを編集する可能性がある場合に、これを使用することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="5bec7-110">It is best to use this in most instances, especially if end-users might edit the file in a text editor outside of the Finance and Operations application.</span></span> <span data-ttu-id="5bec7-111">詳細については、「TextIo.new」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="5bec7-111">For more information, see TextIo.new.</span></span> <span data-ttu-id="5bec7-112">ファイルが読み取られると、TextIO はファイルの最初の数バイトについてバイト順マーク (BOM) を調べて、UTF-8、UTF-16LE、および UTF-16BE を自動的に取り扱います。</span><span class="sxs-lookup"><span data-stu-id="5bec7-112">When files are read, TextIO examines the first few bytes of the file for a byte-order mark (BOM) and automatically handles UTF-8, UTF-16LE, and UTF-16BE.</span></span> <span data-ttu-id="5bec7-113">BOM が見つからない場合、ファイルは ANSI コード ページ (ACP) 形式であると見なされます。</span><span class="sxs-lookup"><span data-stu-id="5bec7-113">If no BOM is found, the file is assumed to be in the ANSI Code Page (ACP) format.</span></span>

## <a name="examples"></a><span data-ttu-id="5bec7-114">例</span><span class="sxs-lookup"><span data-stu-id="5bec7-114">Examples</span></span>

## <a name="methods"></a><span data-ttu-id="5bec7-115">メソッド</span><span class="sxs-lookup"><span data-stu-id="5bec7-115">Methods</span></span>

| <span data-ttu-id="5bec7-116">方法</span><span class="sxs-lookup"><span data-stu-id="5bec7-116">Method</span></span>                                                    | <span data-ttu-id="5bec7-117">説明</span><span class="sxs-lookup"><span data-stu-id="5bec7-117">Description</span></span>                                                                                                        |
|-----------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5bec7-118">public str inFieldDelimiter(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="5bec7-118">public str inFieldDelimiter(\[str value\])</span></span>                | <span data-ttu-id="5bec7-119">TextIO オブジェクトによって表される入力ファイルのフィールド区切り記号に使用される文字を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="5bec7-119">Gets or sets the character that is used for the field delimiter of an input file represented by a TextIO object.</span></span>   |
| <span data-ttu-id="5bec7-120">public str inRecordDelimiter(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="5bec7-120">public str inRecordDelimiter(\[str value\])</span></span>               | <span data-ttu-id="5bec7-121">TextIO オブジェクトによって表される入力ファイルのレコード区切り記号に使用される文字を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="5bec7-121">Gets or sets the character that is used for the record delimiter of an input file represented by a TextIO object.</span></span>  |
| <span data-ttu-id="5bec7-122">public int inRecordLength(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="5bec7-122">public int inRecordLength(\[int value\])</span></span>                  | <span data-ttu-id="5bec7-123">入力ファイルのレコードの長さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="5bec7-123">Gets or sets the record length for an input file.</span></span>                                                                  |
| <span data-ttu-id="5bec7-124">public str outFieldDelimiter(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="5bec7-124">public str outFieldDelimiter(\[str value\])</span></span>               | <span data-ttu-id="5bec7-125">TextIO オブジェクトによって表される出力ファイルのフィールド区切り記号に使用される文字を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="5bec7-125">Gets or sets the character that is used for the field delimiter of an output file represented by a TextIO object.</span></span>  |
| <span data-ttu-id="5bec7-126">public str outRecordDelimiter(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="5bec7-126">public str outRecordDelimiter(\[str value\])</span></span>              | <span data-ttu-id="5bec7-127">TextIO オブジェクトによって表される出力ファイルのレコード区切り記号に使用される文字を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="5bec7-127">Gets or sets the character that is used for the record delimiter of an output file represented by a TextIO object.</span></span> |
| <span data-ttu-id="5bec7-128">public container read()</span><span class="sxs-lookup"><span data-stu-id="5bec7-128">public container read()</span></span>                                   | <span data-ttu-id="5bec7-129">TextIO オブジェクトから次の完全なレコードを読み取ります。</span><span class="sxs-lookup"><span data-stu-id="5bec7-129">Reads the next full record from a TextIO object.</span></span>                                                                   |
| <span data-ttu-id="5bec7-130">public IO\_Status status()</span><span class="sxs-lookup"><span data-stu-id="5bec7-130">public IO\_Status status()</span></span>                                | <span data-ttu-id="5bec7-131">TextIo オブジェクトで実行された最後の操作のステータスを取得します。</span><span class="sxs-lookup"><span data-stu-id="5bec7-131">Retrieves the status of the last operation performed on a TextIo object.</span></span>                                           |
| <span data-ttu-id="5bec7-132">public boolean write(VarArg values)</span><span class="sxs-lookup"><span data-stu-id="5bec7-132">public boolean write(VarArg values)</span></span>                       | <span data-ttu-id="5bec7-133">TextIO オブジェクトによって表されるファイルにデータを記述します。</span><span class="sxs-lookup"><span data-stu-id="5bec7-133">Writes data to a file represented by a TextIO object.</span></span>                                                              |
| <span data-ttu-id="5bec7-134">public boolean writeChar(int int)</span><span class="sxs-lookup"><span data-stu-id="5bec7-134">public boolean writeChar(int int)</span></span>                         | <span data-ttu-id="5bec7-135">Unicode 文字をファイルに記述します。</span><span class="sxs-lookup"><span data-stu-id="5bec7-135">Writes a Unicode character to a file.</span></span>                                                                              |
| <span data-ttu-id="5bec7-136">public boolean writeExp(container data)</span><span class="sxs-lookup"><span data-stu-id="5bec7-136">public boolean writeExp(container data)</span></span>                   | <span data-ttu-id="5bec7-137">TextIO オブジェクトによって表されるファイルにコンテナの内容を記述します。</span><span class="sxs-lookup"><span data-stu-id="5bec7-137">Writes the contents of a container to a file represented by a TextIO object.</span></span>                                       |
| <span data-ttu-id="5bec7-138">public boolean writeRaw(str data)</span><span class="sxs-lookup"><span data-stu-id="5bec7-138">public boolean writeRaw(str data)</span></span>                         | <span data-ttu-id="5bec7-139">予約済み。</span><span class="sxs-lookup"><span data-stu-id="5bec7-139">Reserved.</span></span>                                                                                                          |
| <span data-ttu-id="5bec7-140">public void new(str filename, str mode, \[int codepage\])</span><span class="sxs-lookup"><span data-stu-id="5bec7-140">public void new(str filename, str mode, \[int codepage\])</span></span> | <span data-ttu-id="5bec7-141">TextIO クラスの新しいインスタンスを作成します。</span><span class="sxs-lookup"><span data-stu-id="5bec7-141">Creates a new instance of the TextIO class.</span></span>                                                                        |
| <span data-ttu-id="5bec7-142">public void finalize()</span><span class="sxs-lookup"><span data-stu-id="5bec7-142">public void finalize()</span></span>                                    | <span data-ttu-id="5bec7-143">ファイルを閉じ、データが書き込まれている場合、ファイル バッファーをディスクにフラッシュします。</span><span class="sxs-lookup"><span data-stu-id="5bec7-143">Closes the file and, if data was written, flushes the file buffers to disk.</span></span>                                        |

## <a name="method-infielddelimiter"></a><span data-ttu-id="5bec7-144">メソッド inFieldDelimiter</span><span class="sxs-lookup"><span data-stu-id="5bec7-144">Method inFieldDelimiter</span></span>

<span data-ttu-id="5bec7-145">TextIO オブジェクトによって表される入力ファイルのフィールド区切り記号に使用される文字を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="5bec7-145">Gets or sets the character that is used for the field delimiter of an input file represented by a TextIO object.</span></span>

```xpp
public str inFieldDelimiter([str value])
```

### <a name="parameters---infielddelimiter"></a><span data-ttu-id="5bec7-146">パラメーター - inFieldDelimiter</span><span class="sxs-lookup"><span data-stu-id="5bec7-146">Parameters - inFieldDelimiter</span></span>

<span data-ttu-id="5bec7-147">値</span><span class="sxs-lookup"><span data-stu-id="5bec7-147">value</span></span>  
<span data-ttu-id="5bec7-148">フィールドの区切り記号として使用される文字 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="5bec7-148">The character to be used as the field delimiter; optional.</span></span>

### <a name="return-value---infielddelimiter"></a><span data-ttu-id="5bec7-149">戻り値 - inFieldDelimiter</span><span class="sxs-lookup"><span data-stu-id="5bec7-149">Return Value - inFieldDelimiter</span></span>

<span data-ttu-id="5bec7-150">フィールドの区切り記号として使用される文字。</span><span class="sxs-lookup"><span data-stu-id="5bec7-150">The character used as the field delimiter.</span></span>

### <a name="remarks---infielddelimiter"></a><span data-ttu-id="5bec7-151">備考 - inFieldDelimiter</span><span class="sxs-lookup"><span data-stu-id="5bec7-151">Remarks - inFieldDelimiter</span></span>

<span data-ttu-id="5bec7-152">出力ファイルのフィールド区切り記号を設定するには、次を使用します。</span><span class="sxs-lookup"><span data-stu-id="5bec7-152">To set the field delimiter for an output file, use</span></span>

### <a name="examples---infielddelimiter"></a><span data-ttu-id="5bec7-153">例 - inFieldDelimiter</span><span class="sxs-lookup"><span data-stu-id="5bec7-153">Examples - inFieldDelimiter</span></span>

<span data-ttu-id="5bec7-154">次の例では、入力ファイルのフィールド区切り記号を '\\r\\n' に設定します.</span><span class="sxs-lookup"><span data-stu-id="5bec7-154">The following example sets the field delimiter for an input file to '\\r\\n'.</span></span>

```xpp
protected void openFile() 
{ 
    #define.delimiter('\r\n') 
    super(); 
    importFile.inFieldDelimiter(#delimiter); 
}
```

## <a name="method-inrecorddelimiter"></a><span data-ttu-id="5bec7-155">メソッド inRecordDelimiter</span><span class="sxs-lookup"><span data-stu-id="5bec7-155">Method inRecordDelimiter</span></span>

<span data-ttu-id="5bec7-156">TextIO オブジェクトによって表される入力ファイルのレコード区切り記号に使用される文字を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="5bec7-156">Gets or sets the character that is used for the record delimiter of an input file represented by a TextIO object.</span></span>

```xpp
public str inRecordDelimiter([str value])
```

### <a name="parameters---inrecorddelimiter"></a><span data-ttu-id="5bec7-157">パラメーター - inRecordDelimiter</span><span class="sxs-lookup"><span data-stu-id="5bec7-157">Parameters - inRecordDelimiter</span></span>

<span data-ttu-id="5bec7-158">値</span><span class="sxs-lookup"><span data-stu-id="5bec7-158">value</span></span>  
<span data-ttu-id="5bec7-159">オプションでレコードの区切り記号として使用される文字。</span><span class="sxs-lookup"><span data-stu-id="5bec7-159">The character to be used as the record delimiter; optional.</span></span>

### <a name="return-value---inrecorddelimiter"></a><span data-ttu-id="5bec7-160">戻り値 - inRecordDelimiter</span><span class="sxs-lookup"><span data-stu-id="5bec7-160">Return Value - inRecordDelimiter</span></span>

<span data-ttu-id="5bec7-161">レコードの区切り記号として使用される文字。</span><span class="sxs-lookup"><span data-stu-id="5bec7-161">The character used as the record delimiter.</span></span>

### <a name="remarks---inrecorddelimiter"></a><span data-ttu-id="5bec7-162">備考 - inRecordDelimiter</span><span class="sxs-lookup"><span data-stu-id="5bec7-162">Remarks - inRecordDelimiter</span></span>

<span data-ttu-id="5bec7-163">出力ファイルのレコード区切り記号を設定するには、次を使用します。</span><span class="sxs-lookup"><span data-stu-id="5bec7-163">To set the record delimiter for an output file, use the .</span></span>

### <a name="examples---inrecorddelimiter"></a><span data-ttu-id="5bec7-164">例 - inRecordDelimiter</span><span class="sxs-lookup"><span data-stu-id="5bec7-164">Examples - inRecordDelimiter</span></span>

<span data-ttu-id="5bec7-165">次の例では、レコード区切り記号を 128 に設定します。</span><span class="sxs-lookup"><span data-stu-id="5bec7-165">The following example sets the record delimiter to 128.</span></span>

```xpp
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
```

## <a name="method-inrecordlength"></a><span data-ttu-id="5bec7-166">メソッド inRecordLength</span><span class="sxs-lookup"><span data-stu-id="5bec7-166">Method inRecordLength</span></span>

<span data-ttu-id="5bec7-167">入力ファイルのレコードの長さを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="5bec7-167">Gets or sets the record length for an input file.</span></span>

```xpp
public int inRecordLength([int value])
```

### <a name="parameters---inrecordlength"></a><span data-ttu-id="5bec7-168">パラメーター - inRecordLength</span><span class="sxs-lookup"><span data-stu-id="5bec7-168">Parameters - inRecordLength</span></span>

<span data-ttu-id="5bec7-169">値</span><span class="sxs-lookup"><span data-stu-id="5bec7-169">value</span></span>  
<span data-ttu-id="5bec7-170">入力ファイルのレコードの長さ (オプション)。</span><span class="sxs-lookup"><span data-stu-id="5bec7-170">The record length for the input file; optional.</span></span>

### <a name="return-value---inrecordlength"></a><span data-ttu-id="5bec7-171">戻り値 - inRecordLength</span><span class="sxs-lookup"><span data-stu-id="5bec7-171">Return Value - inRecordLength</span></span>

<span data-ttu-id="5bec7-172">入力ファイルのレコードの長さ。</span><span class="sxs-lookup"><span data-stu-id="5bec7-172">The record length for the input file.</span></span>

### <a name="remarks---inrecordlength"></a><span data-ttu-id="5bec7-173">備考 - inRecordLength</span><span class="sxs-lookup"><span data-stu-id="5bec7-173">Remarks - inRecordLength</span></span>

<span data-ttu-id="5bec7-174">固定長形式になっているファイルについては、inRecordLength プロパティを使用して、各レコードに対して指定された文字数以上が読み取られていないことを確認します。</span><span class="sxs-lookup"><span data-stu-id="5bec7-174">For files that have a fixed-length format, use the inRecordLength property to ensure that no more than the specified number of characters are read for each record.</span></span> <span data-ttu-id="5bec7-175">レコード フォーマットが指定された inRecordDelimiter プロパティ値で上書きされた場合、つまり、固定長が読み込まれる前に inRecordDelimiter 値が満たされている場合)、レコードは受け入れられ、追加のデータは読み込まれません。</span><span class="sxs-lookup"><span data-stu-id="5bec7-175">If the record format is overruled by a specified inRecordDelimiter property value, that is the inRecordDelimiter value is met before the fixed length is read, the record is accepted, and no further data is read.</span></span> <span data-ttu-id="5bec7-176">固定数の文字を確実に読み取るには、inRecordDelimiter プロパティ値を空の文字列に設定します。</span><span class="sxs-lookup"><span data-stu-id="5bec7-176">To ensure that a fixed number of characters are read, set the inRecordDelimiter property value to an empty string.</span></span> <span data-ttu-id="5bec7-177">inRecordDelimiter プロパティ値が見つからない場合、inRecordDelimiter プロパティ値は読み取れる最大文字数になります。</span><span class="sxs-lookup"><span data-stu-id="5bec7-177">When no inRecordDelimiter property value is found, the inRecordDelimiter property value is the maximum limit of characters to read.</span></span> <span data-ttu-id="5bec7-178">レコードの長さチェックを無効にするには、inRecordDelimiter プロパティ値をゼロに設定します。</span><span class="sxs-lookup"><span data-stu-id="5bec7-178">Set the inRecordDelimiter property value to zero to disable the record length check.</span></span>

### <a name="examples---inrecordlength"></a><span data-ttu-id="5bec7-179">例 - inRecordLength</span><span class="sxs-lookup"><span data-stu-id="5bec7-179">Examples - inRecordLength</span></span>

<span data-ttu-id="5bec7-180">次の例では、レコードの長さを 128 に設定します。</span><span class="sxs-lookup"><span data-stu-id="5bec7-180">The following example sets the record length to 128.</span></span>

```xpp
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
```

## <a name="method-outfielddelimiter"></a><span data-ttu-id="5bec7-181">メソッド outFieldDelimiter</span><span class="sxs-lookup"><span data-stu-id="5bec7-181">Method outFieldDelimiter</span></span>

<span data-ttu-id="5bec7-182">TextIO オブジェクトによって表される出力ファイルのフィールド区切り記号に使用される文字を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="5bec7-182">Gets or sets the character that is used for the field delimiter of an output file represented by a TextIO object.</span></span>

```xpp
public str outFieldDelimiter([str value])
```

### <a name="parameters---outfielddelimiter"></a><span data-ttu-id="5bec7-183">パラメーター - outFieldDelimiter</span><span class="sxs-lookup"><span data-stu-id="5bec7-183">Parameters - outFieldDelimiter</span></span>

<span data-ttu-id="5bec7-184">値</span><span class="sxs-lookup"><span data-stu-id="5bec7-184">value</span></span>  
<span data-ttu-id="5bec7-185">フィールドの区切り記号として使用される文字 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="5bec7-185">The character to be used as the field delimiter; optional.</span></span>

### <a name="return-value---outfielddelimiter"></a><span data-ttu-id="5bec7-186">戻り値 - outFieldDelimiter</span><span class="sxs-lookup"><span data-stu-id="5bec7-186">Return Value - outFieldDelimiter</span></span>

<span data-ttu-id="5bec7-187">フィールドの区切り記号として使用される文字。</span><span class="sxs-lookup"><span data-stu-id="5bec7-187">The character used as the field delimiter.</span></span>

### <a name="remarks---outfielddelimiter"></a><span data-ttu-id="5bec7-188">備考 - outFieldDelimiter</span><span class="sxs-lookup"><span data-stu-id="5bec7-188">Remarks - outFieldDelimiter</span></span>

<span data-ttu-id="5bec7-189">入力ファイルのフィールド区切り記号を設定するには、次を使用します。</span><span class="sxs-lookup"><span data-stu-id="5bec7-189">To set the field delimiter for an input file, use the .</span></span>

### <a name="examples---outfielddelimiter"></a><span data-ttu-id="5bec7-190">例 - outFieldDelimiter</span><span class="sxs-lookup"><span data-stu-id="5bec7-190">Examples - outFieldDelimiter</span></span>

<span data-ttu-id="5bec7-191">次の例では、出力ファイルのフィールド区切り記号を ' ' (なし) に設定します。</span><span class="sxs-lookup"><span data-stu-id="5bec7-191">The following example sets the field delimiter to ' ' (nothing) for an output file.</span></span>

```xpp
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
```

## <a name="method-outrecorddelimiter"></a><span data-ttu-id="5bec7-192">メソッド outRecordDelimiter</span><span class="sxs-lookup"><span data-stu-id="5bec7-192">Method outRecordDelimiter</span></span>

<span data-ttu-id="5bec7-193">TextIO オブジェクトによって表される出力ファイルのレコード区切り記号に使用される文字を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="5bec7-193">Gets or sets the character that is used for the record delimiter of an output file represented by a TextIO object.</span></span>

```xpp
public str outRecordDelimiter([str value])
```

### <a name="parameters---outrecorddelimiter"></a><span data-ttu-id="5bec7-194">パラメーター - outRecordDelimiter</span><span class="sxs-lookup"><span data-stu-id="5bec7-194">Parameters - outRecordDelimiter</span></span>

<span data-ttu-id="5bec7-195">値</span><span class="sxs-lookup"><span data-stu-id="5bec7-195">value</span></span>  
<span data-ttu-id="5bec7-196">オプションでレコードの区切り記号として使用される文字。</span><span class="sxs-lookup"><span data-stu-id="5bec7-196">The character to be used as the record delimiter; optional.</span></span>

### <a name="return-value---outrecorddelimiter"></a><span data-ttu-id="5bec7-197">戻り値 - outRecordDelimiter</span><span class="sxs-lookup"><span data-stu-id="5bec7-197">Return Value - outRecordDelimiter</span></span>

<span data-ttu-id="5bec7-198">レコードの区切り記号として使用される文字。</span><span class="sxs-lookup"><span data-stu-id="5bec7-198">The character used as the record delimiter.</span></span>

### <a name="remarks---outrecorddelimiter"></a><span data-ttu-id="5bec7-199">備考 - outRecordDelimiter</span><span class="sxs-lookup"><span data-stu-id="5bec7-199">Remarks - outRecordDelimiter</span></span>

<span data-ttu-id="5bec7-200">入力ファイルのレコード区切り記号を設定するには、次を使用します。</span><span class="sxs-lookup"><span data-stu-id="5bec7-200">To set the record delimiter for an input file, use the .</span></span>

### <a name="examples---outrecorddelimiter"></a><span data-ttu-id="5bec7-201">例 - outFieldDelimiter</span><span class="sxs-lookup"><span data-stu-id="5bec7-201">Examples - outRecordDelimiter</span></span>

<span data-ttu-id="5bec7-202">次の例では、出力ファイルのレコード区切り記号を '\\r\\n'' に設定します。</span><span class="sxs-lookup"><span data-stu-id="5bec7-202">The following example sets the record delimiter for an output file to '\\r\\n'.</span></span>

```xpp
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
```

## <a name="method-read"></a><span data-ttu-id="5bec7-203">メソッド read</span><span class="sxs-lookup"><span data-stu-id="5bec7-203">Method read</span></span>

<span data-ttu-id="5bec7-204">TextIO オブジェクトから次の完全なレコードを読み取ります。</span><span class="sxs-lookup"><span data-stu-id="5bec7-204">Reads the next full record from a TextIO object.</span></span>

```xpp
public container read()
```

### <a name="return-value---read"></a><span data-ttu-id="5bec7-205">戻り値 - read</span><span class="sxs-lookup"><span data-stu-id="5bec7-205">Return Value - read</span></span>

<span data-ttu-id="5bec7-206">1 つのレコードを保持するコンテナーです。</span><span class="sxs-lookup"><span data-stu-id="5bec7-206">A container that holds one record.</span></span>

### <a name="remarks---read"></a><span data-ttu-id="5bec7-207">備考 - read</span><span class="sxs-lookup"><span data-stu-id="5bec7-207">Remarks - read</span></span>

<span data-ttu-id="5bec7-208">コンテナー内の各エントリは、レコードの 1 つのフィールドと同じです。</span><span class="sxs-lookup"><span data-stu-id="5bec7-208">Each entry in the container equals one field in the record.</span></span> <span data-ttu-id="5bec7-209">次の完全なレコードの定義は、次のプロパティ、inFieldDelimiter、inRecordDelimiter、および inRecordLength プロパティによって制御されます。</span><span class="sxs-lookup"><span data-stu-id="5bec7-209">The definition of the next full record is controlled by the inFieldDelimiter, inRecordDelimiter, and inRecordLength properties.</span></span> <span data-ttu-id="5bec7-210">これらのプロパティには、最も一般的な形式の入力と出力を可能にする既定値があります。</span><span class="sxs-lookup"><span data-stu-id="5bec7-210">These properties have default values that allow input and output of the most common formats.</span></span> <span data-ttu-id="5bec7-211">inFieldDelimiter、inRecordDelimiter、および inRecordLength メソッドを使用して、プロパティを調整する必要がある場合があります。</span><span class="sxs-lookup"><span data-stu-id="5bec7-211">It might be necessary to adjust the properties by using the inFieldDelimiter, inRecordDelimiter, and inRecordLength methods.</span></span>

### <a name="examples---read"></a><span data-ttu-id="5bec7-212">例 - read</span><span class="sxs-lookup"><span data-stu-id="5bec7-212">Examples - read</span></span>

<span data-ttu-id="5bec7-213">次の例では、ファイルからレコードを読み取り、conpeek 関数を使用してレコードから値を抽出します。</span><span class="sxs-lookup"><span data-stu-id="5bec7-213">The following example reads a record from a file and uses the conpeek function to extract values from the record.</span></span>

```xpp
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
```

## <a name="method-status"></a><span data-ttu-id="5bec7-214">メソッド status</span><span class="sxs-lookup"><span data-stu-id="5bec7-214">Method status</span></span>

<span data-ttu-id="5bec7-215">TextIo オブジェクトで実行された最後の操作のステータスを取得します。</span><span class="sxs-lookup"><span data-stu-id="5bec7-215">Retrieves the status of the last operation performed on a TextIo object.</span></span>

```xpp
public IO_Status status()
```

### <a name="return-value---status"></a><span data-ttu-id="5bec7-216">戻り値 - status</span><span class="sxs-lookup"><span data-stu-id="5bec7-216">Return Value - status</span></span>

<span data-ttu-id="5bec7-217">最後の操作の状態。</span><span class="sxs-lookup"><span data-stu-id="5bec7-217">The status of the last operation.</span></span>

### <a name="examples---status"></a><span data-ttu-id="5bec7-218">例 - status</span><span class="sxs-lookup"><span data-stu-id="5bec7-218">Examples - status</span></span>

<span data-ttu-id="5bec7-219">次の例では、ファイルが存在しない場合、またはファイルの最後の操作が、IO\_Status::Ok 列挙値のステータスを持たない場合にエラーをスローします。</span><span class="sxs-lookup"><span data-stu-id="5bec7-219">The following example throws an error if a file does not exist or if the last operation on the file did not have a status of the IO\_Status::Ok enumeration value.</span></span>

```xpp
protected void checkDiskFileStatus() 
{ 
    if (!diskFile || diskFile.status() != IO_Status::Ok) 
    { 
        throw error(strfmt("@SYS76826", diskFileName)); 
    } 
}
```

## <a name="method-write"></a><span data-ttu-id="5bec7-220">メソッド write</span><span class="sxs-lookup"><span data-stu-id="5bec7-220">Method write</span></span>

<span data-ttu-id="5bec7-221">TextIO オブジェクトによって表されるファイルにデータを記述します。</span><span class="sxs-lookup"><span data-stu-id="5bec7-221">Writes data to a file represented by a TextIO object.</span></span>

```xpp
public boolean write(VarArg values)
```

### <a name="parameters---write"></a><span data-ttu-id="5bec7-222">パラメーター - write</span><span class="sxs-lookup"><span data-stu-id="5bec7-222">Parameters - write</span></span>

<span data-ttu-id="5bec7-223">値</span><span class="sxs-lookup"><span data-stu-id="5bec7-223">values</span></span>  
<span data-ttu-id="5bec7-224">ファイルに書き込む値。</span><span class="sxs-lookup"><span data-stu-id="5bec7-224">The values to write to the file.</span></span> <span data-ttu-id="5bec7-225">値はさまざまなデータ型にすることができます。</span><span class="sxs-lookup"><span data-stu-id="5bec7-225">The values can be of different data types.</span></span>

### <a name="return-value---write"></a><span data-ttu-id="5bec7-226">戻り値 - write</span><span class="sxs-lookup"><span data-stu-id="5bec7-226">Return Value - write</span></span>

<span data-ttu-id="5bec7-227">書き込み操作が成功する場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="5bec7-227">true if the write operation succeeds; otherwise, false.</span></span>

### <a name="remarks---write"></a><span data-ttu-id="5bec7-228">備考 - write</span><span class="sxs-lookup"><span data-stu-id="5bec7-228">Remarks - write</span></span>

<span data-ttu-id="5bec7-229">書き込み操作が失敗した場合は、その原因を突き止めるために使用できます。</span><span class="sxs-lookup"><span data-stu-id="5bec7-229">If the write operation fails, can be used to ascertain the cause.</span></span> <span data-ttu-id="5bec7-230">書き込みメソッドは、可変数の引数を受け入れます。</span><span class="sxs-lookup"><span data-stu-id="5bec7-230">The write method accepts a variable number of arguments.</span></span> <span data-ttu-id="5bec7-231">各値は、フィールドとして出力レコードに配置されます。</span><span class="sxs-lookup"><span data-stu-id="5bec7-231">Each value is put into the output record as a field.</span></span> <span data-ttu-id="5bec7-232">フィールドは、で指定されたフィールド区切り記号で区切られます。</span><span class="sxs-lookup"><span data-stu-id="5bec7-232">The fields are separated by the field delimiter specified by the .</span></span> <span data-ttu-id="5bec7-233">各レコードは、によって指定された区切り記号で区切られます。</span><span class="sxs-lookup"><span data-stu-id="5bec7-233">Each record is separated by the delimiter specified by the .</span></span> <span data-ttu-id="5bec7-234">完全なコンテナーを書き込むには、次を使用します。</span><span class="sxs-lookup"><span data-stu-id="5bec7-234">To write complete containers, use the .</span></span>

## <a name="method-writechar"></a><span data-ttu-id="5bec7-235">メソッド writeChar</span><span class="sxs-lookup"><span data-stu-id="5bec7-235">Method writeChar</span></span>

<span data-ttu-id="5bec7-236">Unicode 文字をファイルに記述します。</span><span class="sxs-lookup"><span data-stu-id="5bec7-236">Writes a Unicode character to a file.</span></span>

```xpp
public boolean writeChar(int int)
```

### <a name="parameters---writechar"></a><span data-ttu-id="5bec7-237">パラメーター - writeChar</span><span class="sxs-lookup"><span data-stu-id="5bec7-237">Parameters - writeChar</span></span>

<span data-ttu-id="5bec7-238">int</span><span class="sxs-lookup"><span data-stu-id="5bec7-238">int</span></span>  

### <a name="return-value---writechar"></a><span data-ttu-id="5bec7-239">戻り値 - writeChar</span><span class="sxs-lookup"><span data-stu-id="5bec7-239">Return Value - writeChar</span></span>

<span data-ttu-id="5bec7-240">書き込み操作が成功する場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="5bec7-240">true if the write operation succeeds; otherwise, false.</span></span>

### <a name="remarks---writechar"></a><span data-ttu-id="5bec7-241">備考 - writeChar</span><span class="sxs-lookup"><span data-stu-id="5bec7-241">Remarks - writeChar</span></span>

<span data-ttu-id="5bec7-242">書き込み操作が失敗した場合は、原因を突き止めるために TextIO.status メソッドを使用することができます。</span><span class="sxs-lookup"><span data-stu-id="5bec7-242">If the write operation fails, the TextIO.status method can be used to check for the cause.</span></span> <span data-ttu-id="5bec7-243">複数の値を書き込んだり、さまざまな種類のデータをファイルに書き込むには、TextIO.write メソッドを使用します。</span><span class="sxs-lookup"><span data-stu-id="5bec7-243">To write multiple values or to write data of different types to a file, use the TextIO.write method.</span></span>

## <a name="method-writeexp"></a><span data-ttu-id="5bec7-244">メソッド writeExp</span><span class="sxs-lookup"><span data-stu-id="5bec7-244">Method writeExp</span></span>

<span data-ttu-id="5bec7-245">TextIO オブジェクトによって表されるファイルにコンテナの内容を記述します。</span><span class="sxs-lookup"><span data-stu-id="5bec7-245">Writes the contents of a container to a file represented by a TextIO object.</span></span>

```xpp
public boolean writeExp(container data)
```

### <a name="parameters---writeexp"></a><span data-ttu-id="5bec7-246">パラメーター - writeExp</span><span class="sxs-lookup"><span data-stu-id="5bec7-246">Parameters - writeExp</span></span>

<span data-ttu-id="5bec7-247">データ</span><span class="sxs-lookup"><span data-stu-id="5bec7-247">data</span></span>  
<span data-ttu-id="5bec7-248">ファイルへの書き込みのデータを持つコンテナーです。</span><span class="sxs-lookup"><span data-stu-id="5bec7-248">The container that has data to write to the file.</span></span>

### <a name="return-value---writeexp"></a><span data-ttu-id="5bec7-249">戻り値 - writeExp</span><span class="sxs-lookup"><span data-stu-id="5bec7-249">Return Value - writeExp</span></span>

<span data-ttu-id="5bec7-250">書き込み操作が成功する場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="5bec7-250">true if the write operation succeeds; otherwise, false.</span></span>

### <a name="remarks---writeexp"></a><span data-ttu-id="5bec7-251">備考 - writeExp</span><span class="sxs-lookup"><span data-stu-id="5bec7-251">Remarks - writeExp</span></span>

<span data-ttu-id="5bec7-252">書き込み操作が失敗した場合は、原因を突き止めるために TextIO.status メソッドを使用することができます。</span><span class="sxs-lookup"><span data-stu-id="5bec7-252">If the write operation fails, the TextIo.status Method can be used to ascertain the cause.</span></span> <span data-ttu-id="5bec7-253">コンテナー内のエントリは、outFieldDelimiter メソッドで設定された区切り文字で区切られます。</span><span class="sxs-lookup"><span data-stu-id="5bec7-253">Entries in the container are separated by the delimiter set by the outFieldDelimiter method.</span></span> <span data-ttu-id="5bec7-254">コンテナーは、outRecordDelimiter メソッドで設定された区切り文字で区切られます。</span><span class="sxs-lookup"><span data-stu-id="5bec7-254">Containers are separated by the delimiter set by the outRecordDelimiter method.</span></span>

## <a name="method-writeraw"></a><span data-ttu-id="5bec7-255">メソッド writeRaw</span><span class="sxs-lookup"><span data-stu-id="5bec7-255">Method writeRaw</span></span>

<span data-ttu-id="5bec7-256">予約済み。</span><span class="sxs-lookup"><span data-stu-id="5bec7-256">Reserved.</span></span>

```xpp
public boolean writeRaw(str data)
```

### <a name="parameters---writeraw"></a><span data-ttu-id="5bec7-257">パラメーター - writeRaw</span><span class="sxs-lookup"><span data-stu-id="5bec7-257">Parameters - writeRaw</span></span>

<span data-ttu-id="5bec7-258">データ</span><span class="sxs-lookup"><span data-stu-id="5bec7-258">data</span></span>  

### <a name="return-value---writeraw"></a><span data-ttu-id="5bec7-259">戻り値 - writeRaw</span><span class="sxs-lookup"><span data-stu-id="5bec7-259">Return Value - writeRaw</span></span>

## <a name="method-new"></a><span data-ttu-id="5bec7-260">メソッド new</span><span class="sxs-lookup"><span data-stu-id="5bec7-260">Method new</span></span>

<span data-ttu-id="5bec7-261">TextIO クラスの新しいインスタンスを作成します。</span><span class="sxs-lookup"><span data-stu-id="5bec7-261">Creates a new instance of the TextIO class.</span></span>

```xpp
public void new(str filename, str mode, [int codepage])
```

### <a name="parameters---new"></a><span data-ttu-id="5bec7-262">パラメーター - new</span><span class="sxs-lookup"><span data-stu-id="5bec7-262">Parameters - new</span></span>

<span data-ttu-id="5bec7-263">filename</span><span class="sxs-lookup"><span data-stu-id="5bec7-263">filename</span></span>  
<span data-ttu-id="5bec7-264">ファイルから読み込まれる、またはファイルに書き込まれる文字セットのコード ページ番号。</span><span class="sxs-lookup"><span data-stu-id="5bec7-264">The code page number for the character set to be read from or written to the file.</span></span> <span data-ttu-id="5bec7-265">既定値は 1200 (UTF-16LE) です。</span><span class="sxs-lookup"><span data-stu-id="5bec7-265">The default value is 1200 (UTF-16LE).</span></span> <span data-ttu-id="5bec7-266">このパラメーターはオプションです。</span><span class="sxs-lookup"><span data-stu-id="5bec7-266">This parameter is optional.</span></span> <span data-ttu-id="5bec7-267">以下に示す値は、最も一般的な値です。これらのオプションの詳細については、 [the list](https://go.microsoft.com/fwlink/?LinkID=78282&clcid=0x409)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="5bec7-267">Following are the most common values: For more information about these options, see [the list](https://go.microsoft.com/fwlink/?LinkID=78282&clcid=0x409).</span></span> <span data-ttu-id="5bec7-268">無効なコード ページが要求された場合にエラーが報告されます。</span><span class="sxs-lookup"><span data-stu-id="5bec7-268">An error is reported if an invalid code page is requested.</span></span> <span data-ttu-id="5bec7-269">コンピューターにインストールされていない場合、コード ページは「無効」としてレポートされることに注意します (さまざまなコード ページがクライアントとサーバーにインストールされている場合があります)。</span><span class="sxs-lookup"><span data-stu-id="5bec7-269">Notice that a code page is reported as "invalid" if it is not installed on the computer (different code pages may be installed on the client and server).</span></span> <span data-ttu-id="5bec7-270">たとえば、コンピューターの ACP がギリシャ語でない、またはギリシャ語のサポートがコントロール パネル &gt;地域オプションを使用して読み込まれない限り、ギリシャ語のコード ページ 1253 の指定は失敗します。</span><span class="sxs-lookup"><span data-stu-id="5bec7-270">For example, specifying code page 1253 for Greek fails unless the computer's ACP is Greek or Greek language support has been loaded by using Control Panel &gt; Regional Options.</span></span>

<!-- -->

<span data-ttu-id="5bec7-271">モード</span><span class="sxs-lookup"><span data-stu-id="5bec7-271">mode</span></span>  
<span data-ttu-id="5bec7-272">ファイルから読み込まれる、またはファイルに書き込まれる文字セットのコード ページ番号。</span><span class="sxs-lookup"><span data-stu-id="5bec7-272">The code page number for the character set to be read from or written to the file.</span></span> <span data-ttu-id="5bec7-273">既定値は 1200 (UTF-16LE) です。</span><span class="sxs-lookup"><span data-stu-id="5bec7-273">The default value is 1200 (UTF-16LE).</span></span> <span data-ttu-id="5bec7-274">このパラメーターはオプションです。</span><span class="sxs-lookup"><span data-stu-id="5bec7-274">This parameter is optional.</span></span> <span data-ttu-id="5bec7-275">以下に示す値は、最も一般的な値です。これらのオプションの詳細については、 [the list](https://go.microsoft.com/fwlink/?LinkID=78282&clcid=0x409)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="5bec7-275">Following are the most common values: For more information about these options, see [the list](https://go.microsoft.com/fwlink/?LinkID=78282&clcid=0x409).</span></span> <span data-ttu-id="5bec7-276">無効なコード ページが要求された場合にエラーが報告されます。</span><span class="sxs-lookup"><span data-stu-id="5bec7-276">An error is reported if an invalid code page is requested.</span></span> <span data-ttu-id="5bec7-277">コンピューターにインストールされていない場合、コード ページは「無効」としてレポートされることに注意します (さまざまなコード ページがクライアントとサーバーにインストールされている場合があります)。</span><span class="sxs-lookup"><span data-stu-id="5bec7-277">Notice that a code page is reported as "invalid" if it is not installed on the computer (different code pages may be installed on the client and server).</span></span> <span data-ttu-id="5bec7-278">たとえば、コンピューターの ACP がギリシャ語でない、またはギリシャ語のサポートがコントロール パネル &gt;地域オプションを使用して読み込まれない限り、ギリシャ語のコード ページ 1253 の指定は失敗します。</span><span class="sxs-lookup"><span data-stu-id="5bec7-278">For example, specifying code page 1253 for Greek fails unless the computer's ACP is Greek or Greek language support has been loaded by using Control Panel &gt; Regional Options.</span></span>

<!-- -->

<span data-ttu-id="5bec7-279">codepage</span><span class="sxs-lookup"><span data-stu-id="5bec7-279">codepage</span></span>  
<span data-ttu-id="5bec7-280">ファイルから読み込まれる、またはファイルに書き込まれる文字セットのコード ページ番号。</span><span class="sxs-lookup"><span data-stu-id="5bec7-280">The code page number for the character set to be read from or written to the file.</span></span> <span data-ttu-id="5bec7-281">既定値は 1200 (UTF-16LE) です。</span><span class="sxs-lookup"><span data-stu-id="5bec7-281">The default value is 1200 (UTF-16LE).</span></span> <span data-ttu-id="5bec7-282">このパラメーターはオプションです。</span><span class="sxs-lookup"><span data-stu-id="5bec7-282">This parameter is optional.</span></span> <span data-ttu-id="5bec7-283">以下に示す値は、最も一般的な値です。これらのオプションの詳細については、 [the list](https://go.microsoft.com/fwlink/?LinkID=78282&clcid=0x409)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="5bec7-283">Following are the most common values: For more information about these options, see [the list](https://go.microsoft.com/fwlink/?LinkID=78282&clcid=0x409).</span></span> <span data-ttu-id="5bec7-284">無効なコード ページが要求された場合にエラーが報告されます。</span><span class="sxs-lookup"><span data-stu-id="5bec7-284">An error is reported if an invalid code page is requested.</span></span> <span data-ttu-id="5bec7-285">コンピューターにインストールされていない場合、コード ページは「無効」としてレポートされることに注意します (さまざまなコード ページがクライアントとサーバーにインストールされている場合があります)。</span><span class="sxs-lookup"><span data-stu-id="5bec7-285">Notice that a code page is reported as "invalid" if it is not installed on the computer (different code pages may be installed on the client and server).</span></span> <span data-ttu-id="5bec7-286">たとえば、コンピューターの ACP がギリシャ語でない、またはギリシャ語のサポートがコントロール パネル &gt;地域オプションを使用して読み込まれない限り、ギリシャ語のコード ページ 1253 の指定は失敗します。</span><span class="sxs-lookup"><span data-stu-id="5bec7-286">For example, specifying code page 1253 for Greek fails unless the computer's ACP is Greek or Greek language support has been loaded by using Control Panel &gt; Regional Options.</span></span>

### <a name="remarks---new"></a><span data-ttu-id="5bec7-287">備考 - new</span><span class="sxs-lookup"><span data-stu-id="5bec7-287">Remarks - new</span></span>

<span data-ttu-id="5bec7-288">ランタイム エラーは、現在開いているモードに対応しないメソッドでファイルにアクセスすると発生します (たとえば、読み取りモード ファイルに書き込もうとした場合など)。</span><span class="sxs-lookup"><span data-stu-id="5bec7-288">A run-time error occurs if the file is accessed with a method that does not correspond to the current opened mode (for example, you try to write to a read-mode file).</span></span> <span data-ttu-id="5bec7-289">攻撃者が新しいメソッドへの入力を制御できる場合、セキュリティ上のリスクが存在します。</span><span class="sxs-lookup"><span data-stu-id="5bec7-289">If an attacker can control input to the new method, a security risk exists.</span></span> <span data-ttu-id="5bec7-290">このメソッドは、コード アクセス セキュリティで実行されます。</span><span class="sxs-lookup"><span data-stu-id="5bec7-290">This method runs under Code Access Security.</span></span> <span data-ttu-id="5bec7-291">サーバー上でこのメソッドを呼び出すには、FileIoPermission クラスからのアクセス許可が必要です。</span><span class="sxs-lookup"><span data-stu-id="5bec7-291">Calls to this method on the server require permission from the FileIoPermission class.</span></span> <span data-ttu-id="5bec7-292">ユーザーがこのメソッドを呼び出すコントロールで、SysDevelopment へのセキュリティ キーを設定して開発権限があることを確認します。</span><span class="sxs-lookup"><span data-stu-id="5bec7-292">Ensure that the user has development privileges by setting the security key to SysDevelopment on the control that calls this method.</span></span> <span data-ttu-id="5bec7-293">次のテーブルは、\_codePage パラメーターに指定できる、より一般的なコード ページの一部を示しています。</span><span class="sxs-lookup"><span data-stu-id="5bec7-293">The following table describes some of the more common code pages that might be specified for the \_codePage parameter.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="5bec7-294">0</span><span class="sxs-lookup"><span data-stu-id="5bec7-294">0</span></span></td>
<td><span data-ttu-id="5bec7-295">ANSI コード ページ (ACP)</span><span class="sxs-lookup"><span data-stu-id="5bec7-295">ANSI code page (ACP)</span></span></td>
<td><span data-ttu-id="5bec7-296">ユーザー&#39;の現在の言語の文字のみをサポートするコード ページ。</span><span class="sxs-lookup"><span data-stu-id="5bec7-296">The code page that supports only characters in the user&#39;s current language.</span></span> <span data-ttu-id="5bec7-297">コード ページは、多言語データを含む可能性のあるものや、異なるコード ページを使用して 2 つのシステム間で転送される単一言語データ用には適していません。</span><span class="sxs-lookup"><span data-stu-id="5bec7-297">The code page is unsuitable for anything that might contain multilingual data or for monolingual data that might be transferred between two systems by using different code pages.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5bec7-298">437</span><span class="sxs-lookup"><span data-stu-id="5bec7-298">437</span></span></td>
<td><span data-ttu-id="5bec7-299">OEM コード ページ 437</span><span class="sxs-lookup"><span data-stu-id="5bec7-299">OEM code page 437</span></span></td>
<td><span data-ttu-id="5bec7-300">IBM PC または MS-DOS コード ページ 437。</span><span class="sxs-lookup"><span data-stu-id="5bec7-300">The IBM PC or MS-DOS code page 437.</span></span> <span data-ttu-id="5bec7-301">これは、CP437 と省略されることが多く、DOS-US や OEM-US とも呼ばれます。</span><span class="sxs-lookup"><span data-stu-id="5bec7-301">It is often abbreviated as CP437 and also called DOS-US or OEM-US.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5bec7-302">850</span><span class="sxs-lookup"><span data-stu-id="5bec7-302">850</span></span></td>
<td><span data-ttu-id="5bec7-303">コード ページ 850</span><span class="sxs-lookup"><span data-stu-id="5bec7-303">Code page 850</span></span></td>
<td><span data-ttu-id="5bec7-304">西ヨーロッパで MS-DOS などのオペレーティング システムで使用されていたコード ページ。</span><span class="sxs-lookup"><span data-stu-id="5bec7-304">A code page that was used in Western Europe running on operating systems, such as MS-DOS.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5bec7-305">1200</span><span class="sxs-lookup"><span data-stu-id="5bec7-305">1200</span></span></td>
<td><span data-ttu-id="5bec7-306">UTF-16LE</span><span class="sxs-lookup"><span data-stu-id="5bec7-306">UTF-16LE</span></span></td>
<td><span data-ttu-id="5bec7-307">Microsoft Windows x86 システムでのネイティブ Unicode 表現。</span><span class="sxs-lookup"><span data-stu-id="5bec7-307">The native Unicode representation on Microsoft Windows x86 systems.</span></span> <span data-ttu-id="5bec7-308">ほとんどすべての文字は 16 ビットとして保存されます。</span><span class="sxs-lookup"><span data-stu-id="5bec7-308">Almost all characters are stored as 16 bit.</span></span> <span data-ttu-id="5bec7-309">一部の中国語文字には、32 ビットが必要です。</span><span class="sxs-lookup"><span data-stu-id="5bec7-309">Some Chinese characters require 32 bit.</span></span> <span data-ttu-id="5bec7-310">文字の残りの部分を読み取ると、識別バイト オーダー マークが書き込まれ、検査され、次に破棄されます。</span><span class="sxs-lookup"><span data-stu-id="5bec7-310">An identifying byte-order mark is written, examined, and then discarded when the rest of the character is read.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5bec7-311">1201</span><span class="sxs-lookup"><span data-stu-id="5bec7-311">1201</span></span></td>
<td><span data-ttu-id="5bec7-312">UTF-16BE</span><span class="sxs-lookup"><span data-stu-id="5bec7-312">UTF-16BE</span></span></td>
<td><span data-ttu-id="5bec7-313">UTF-16LE と同じですが、バイトスワップします。</span><span class="sxs-lookup"><span data-stu-id="5bec7-313">The same as UTF-16LE but byte-swapped.</span></span> <span data-ttu-id="5bec7-314">下位から上位ではなく左から右へバイトを格納する x86 以外のシステムとの互換性のために使用されます。</span><span class="sxs-lookup"><span data-stu-id="5bec7-314">Used for compatibility with some non-x86 systems, which store bytes from left-to-right instead of low-order to high-order.</span></span> <span data-ttu-id="5bec7-315">文字の残りの部分を読み取ると、識別バイト オーダー マークが最初に書き込まれ、検査され、次に破棄されます。</span><span class="sxs-lookup"><span data-stu-id="5bec7-315">An identifying byte-order mark is written first, examined, and then discarded when the rest of the character is read.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5bec7-316">65001</span><span class="sxs-lookup"><span data-stu-id="5bec7-316">65001</span></span></td>
<td><span data-ttu-id="5bec7-317">UTF-8</span><span class="sxs-lookup"><span data-stu-id="5bec7-317">UTF-8</span></span></td>
<td><span data-ttu-id="5bec7-318">バイト ストリームしやすい方法で Unicode を保存します。</span><span class="sxs-lookup"><span data-stu-id="5bec7-318">Stores Unicode in a byte-stream�friendly way:</span></span>
<ul>
<li><span data-ttu-id="5bec7-319">ASCII 文字は、1 バイトです。</span><span class="sxs-lookup"><span data-stu-id="5bec7-319">ASCII characters are 1 byte</span></span></li>
<li><span data-ttu-id="5bec7-320">欧州のアルファベット (基本分音記号を含む) は文字あたり 2 バイト</span><span class="sxs-lookup"><span data-stu-id="5bec7-320">European alphabets (including basic diacritics) are 2 bytes per character</span></span></li>
<li><span data-ttu-id="5bec7-321">中国語、日本語、韓国語の場合、文字あたり 3 バイト必要</span><span class="sxs-lookup"><span data-stu-id="5bec7-321">Chinese, Japanese, and Korean require 3 bytes per character</span></span></li>
</ul>
<span data-ttu-id="5bec7-322">このコード ページは、ファイルに含まれているASCIIの割合が非常に高く、その他の文字が比較的少なく、スペースを節約することが重要な場合に適しています。</span><span class="sxs-lookup"><span data-stu-id="5bec7-322">This code page is a good choice when a file contains a very high percentage of ASCII, relatively few other characters, and it is important to save space.</span></span> <span data-ttu-id="5bec7-323">たとえば、.xpo ファイルは、UTF-8 に格納されます。</span><span class="sxs-lookup"><span data-stu-id="5bec7-323">For example, .xpo files are stored in UTF-8.</span></span> <span data-ttu-id="5bec7-324">UTF-8 ファイルは、3 バイトのバイト順序マーク列で始まり、この項目が最初に書き込まれます。</span><span class="sxs-lookup"><span data-stu-id="5bec7-324">UTF-8 files begin with a 3-byte byte-order mark sequence, which is the first item written.</span></span> <span data-ttu-id="5bec7-325">それを調べてから、文字の残りの部分を読み取ると破棄されます。</span><span class="sxs-lookup"><span data-stu-id="5bec7-325">It is examined, and then discarded when the rest of the character is read.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5bec7-326">54936</span><span class="sxs-lookup"><span data-stu-id="5bec7-326">54936</span></span></td>
<td><span data-ttu-id="5bec7-327">GB-18030</span><span class="sxs-lookup"><span data-stu-id="5bec7-327">GB-18030</span></span></td>
<td><span data-ttu-id="5bec7-328">中国政府によって求められている GB-18030 文字表現でデータを格納します。</span><span class="sxs-lookup"><span data-stu-id="5bec7-328">Stores data in the GB-18030 character representation that is required by the Chinese government.</span></span> <span data-ttu-id="5bec7-329">バイト順序マークは書き込まれません。</span><span class="sxs-lookup"><span data-stu-id="5bec7-329">No byte-order mark is written.</span></span> <span data-ttu-id="5bec7-330">これらのファイルは、ファイルに GB-2312 のレパートリー外の文字が含まれていない限り、コード ページ 20936 (GB-2312、中国語 (簡体) システム用の ACP) で記述されたファイルと区別できません。</span><span class="sxs-lookup"><span data-stu-id="5bec7-330">These files cannot be distinguished from those written in code page 20936 (GB-2312, which is the ACP for Simplified Chinese systems) unless the file contains characters outside the repertoire of GB-2312.</span></span></td>
</tr>
</tbody>
</table>

### <a name="examples---new"></a><span data-ttu-id="5bec7-331">例 - new</span><span class="sxs-lookup"><span data-stu-id="5bec7-331">Examples - new</span></span>

<span data-ttu-id="5bec7-332">次の例では、コード ページ 850 エンコードを使用して、読み取りモードで filename という名前のファイルにアクセスする TextIO オブジェクトを作成します。</span><span class="sxs-lookup"><span data-stu-id="5bec7-332">The following example creates a TextIO object to access a file that is named filename in read mode by using code page 850 encoding.</span></span>

```xpp
protected void openFile(str _fileOpen = #io_read) 
{ 
    importFile = new TextIo(filename, _fileOpen, 850); 
    if (! importFile) 
    { 
        throw error(strfmt("@SYS18678", filename)); 
    } 
}
```

## <a name="method-finalize"></a><span data-ttu-id="5bec7-333">メソッド finalize</span><span class="sxs-lookup"><span data-stu-id="5bec7-333">Method finalize</span></span>

<span data-ttu-id="5bec7-334">ファイルを閉じ、データが書き込まれている場合、ファイル バッファーをディスクにフラッシュします。</span><span class="sxs-lookup"><span data-stu-id="5bec7-334">Closes the file and, if data was written, flushes the file buffers to disk.</span></span>

```xpp
public void finalize()
```

### <a name="remarks---finalize"></a><span data-ttu-id="5bec7-335">備考 - finalize</span><span class="sxs-lookup"><span data-stu-id="5bec7-335">Remarks - finalize</span></span>

<span data-ttu-id="5bec7-336">通常、TextIO オブジェクトは、スコープを離れることによって確定されます。</span><span class="sxs-lookup"><span data-stu-id="5bec7-336">The TextIO object is usually finalized by leaving the scope.</span></span> <span data-ttu-id="5bec7-337">確定メソッドは、通常は直接呼び出されません。</span><span class="sxs-lookup"><span data-stu-id="5bec7-337">The finalize method is not usually directly called.</span></span> <span data-ttu-id="5bec7-338">TextIO オブジェクトが確定済みになるまで、ファイルに書き込まれる出力は無効です。</span><span class="sxs-lookup"><span data-stu-id="5bec7-338">Output written to the file is not valid until the TextIO object is finalized.</span></span>

