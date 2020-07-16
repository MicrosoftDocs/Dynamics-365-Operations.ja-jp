---
title: AsciiIo クラス
description: このトピックでは、AsciiIo クラスについて説明します。
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
ms.openlocfilehash: 94dc3749f1ad3029946ee763c7f7f47f7e946be0
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502746"
---
# <a name="class-asciiio"></a><span data-ttu-id="ce557-103">クラス AsciiIo</span><span class="sxs-lookup"><span data-stu-id="ce557-103">Class AsciiIo</span></span>

[!include [banner](../../includes/banner.md)]

```xpp
class AsciiIo extends CommaIo
```

<span data-ttu-id="ce557-104">AsciiIo クラスには、ASCII ファイルの読み取りと書き込みを行う機能があります。</span><span class="sxs-lookup"><span data-stu-id="ce557-104">The AsciiIo class provides functionality for reading and writing ASCII files.</span></span>

## <a name="remarks"></a><span data-ttu-id="ce557-105">備考</span><span class="sxs-lookup"><span data-stu-id="ce557-105">Remarks</span></span>

<span data-ttu-id="ce557-106">TextIo クラスには、さまざまなコード ページを使用するファイルの読み取りと書き込みを行う機能があります。</span><span class="sxs-lookup"><span data-stu-id="ce557-106">The TextIo class provides functionality for reading and writing files that use various code pages.</span></span> <span data-ttu-id="ce557-107">AsciiIO クラスは、ANSI コード ページ (ACP) 文字のみサポートします。</span><span class="sxs-lookup"><span data-stu-id="ce557-107">The AsciiIO class supports only ANSI code page (ACP) characters.</span></span> <span data-ttu-id="ce557-108">AsciiIO クラスを使用する既存のコードは、ファイルに ACP 以外の文字が含まれている場合や、.xpo ファイルなどの Finance and Operations アプリケーションでのみ使用されるファイルの場合に TextIO クラスを使用するように変換する必要があります。</span><span class="sxs-lookup"><span data-stu-id="ce557-108">Existing code that uses the AsciiIO class must be converted to use the TextIO class if the file contains non-ACP characters, or if it is a file that is used only in a Finance and Operations application, such as an .xpo file.</span></span>

## <a name="examples"></a><span data-ttu-id="ce557-109">例</span><span class="sxs-lookup"><span data-stu-id="ce557-109">Examples</span></span>

## <a name="methods"></a><span data-ttu-id="ce557-110">メソッド</span><span class="sxs-lookup"><span data-stu-id="ce557-110">Methods</span></span>

| <span data-ttu-id="ce557-111">方法</span><span class="sxs-lookup"><span data-stu-id="ce557-111">Method</span></span>                                       | <span data-ttu-id="ce557-112">説明</span><span class="sxs-lookup"><span data-stu-id="ce557-112">Description</span></span>                                                                                                                      |
|----------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ce557-113">public str inFieldDelimiter(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="ce557-113">public str inFieldDelimiter(\[str value\])</span></span>   | <span data-ttu-id="ce557-114">AsciiIO オブジェクトによって表される入力ファイルのフィールド区切り記号として使用される文字を設定または取得します。</span><span class="sxs-lookup"><span data-stu-id="ce557-114">Sets or retrieves the character that is used as the field delimiter of an input file that is represented by an AsciiIO object.</span></span>   |
| <span data-ttu-id="ce557-115">public str inRecordDelimiter(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="ce557-115">public str inRecordDelimiter(\[str value\])</span></span>  | <span data-ttu-id="ce557-116">AsciiIO オブジェクトによって表される入力ファイルのレコード区切り記号として使用される文字を設定または取得します。</span><span class="sxs-lookup"><span data-stu-id="ce557-116">Sets or retrieves the character that is used as the record delimiter of an input file that is represented by an AsciiIO object.</span></span>  |
| <span data-ttu-id="ce557-117">public int inRecordLength(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="ce557-117">public int inRecordLength(\[int value\])</span></span>     | <span data-ttu-id="ce557-118">入力ファイルのレコードの長さを設定または取得します。</span><span class="sxs-lookup"><span data-stu-id="ce557-118">Sets or retrieves the record length for an input file.</span></span>                                                                           |
| <span data-ttu-id="ce557-119">public str outFieldDelimiter(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="ce557-119">public str outFieldDelimiter(\[str value\])</span></span>  | <span data-ttu-id="ce557-120">AsciiIO オブジェクトによって表される出力ファイルのフィールド区切り記号として使用される文字を設定または取得します。</span><span class="sxs-lookup"><span data-stu-id="ce557-120">Sets or retrieves the character that is used as the field delimiter of an output file that is represented by an AsciiIO object.</span></span>  |
| <span data-ttu-id="ce557-121">public str outRecordDelimiter(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="ce557-121">public str outRecordDelimiter(\[str value\])</span></span> | <span data-ttu-id="ce557-122">AsciiIO オブジェクトによって表される出力ファイルのレコード区切り記号として使用される文字を設定または取得します。</span><span class="sxs-lookup"><span data-stu-id="ce557-122">Sets or retrieves the character that is used as the record delimiter of an output file that is represented by an AsciiIO object.</span></span> |
| <span data-ttu-id="ce557-123">public container read()</span><span class="sxs-lookup"><span data-stu-id="ce557-123">public container read()</span></span>                      | <span data-ttu-id="ce557-124">Io オブジェクトから次の完全なレコードを読み取ります。</span><span class="sxs-lookup"><span data-stu-id="ce557-124">Reads the next full record from the Io object.</span></span>                                                                                   |
| <span data-ttu-id="ce557-125">public IO\_Status status()</span><span class="sxs-lookup"><span data-stu-id="ce557-125">public IO\_Status status()</span></span>                   | <span data-ttu-id="ce557-126">ファイルでの最後の操作のステータスを返します。</span><span class="sxs-lookup"><span data-stu-id="ce557-126">Returns the status of the last operation on the file.</span></span>                                                                            |
| <span data-ttu-id="ce557-127">public boolean write(VarArg values)</span><span class="sxs-lookup"><span data-stu-id="ce557-127">public boolean write(VarArg values)</span></span>          | <span data-ttu-id="ce557-128">単純型の値を記述します。</span><span class="sxs-lookup"><span data-stu-id="ce557-128">Writes values of a simple type.</span></span>                                                                                                  |
| <span data-ttu-id="ce557-129">public boolean writeChar(int int)</span><span class="sxs-lookup"><span data-stu-id="ce557-129">public boolean writeChar(int int)</span></span>            |                                                                                                                                  |
| <span data-ttu-id="ce557-130">public boolean writeExp(container data)</span><span class="sxs-lookup"><span data-stu-id="ce557-130">public boolean writeExp(container data)</span></span>      | <span data-ttu-id="ce557-131">コンテナのコンテンツをファイルに記述します。</span><span class="sxs-lookup"><span data-stu-id="ce557-131">Writes the content of a container to a file.</span></span>                                                                                     |
| <span data-ttu-id="ce557-132">public boolean writeRaw(str data)</span><span class="sxs-lookup"><span data-stu-id="ce557-132">public boolean writeRaw(str data)</span></span>            |                                                                                                                                  |
| <span data-ttu-id="ce557-133">public void finalize()</span><span class="sxs-lookup"><span data-stu-id="ce557-133">public void finalize()</span></span>                       | <span data-ttu-id="ce557-134">ファイルを閉じ、ファイル バッファーをディスクにフラッシュします。</span><span class="sxs-lookup"><span data-stu-id="ce557-134">Closes the file and then flushes the file buffers to disk.</span></span>                                                                       |
| <span data-ttu-id="ce557-135">public void new(str filename, str mode)</span><span class="sxs-lookup"><span data-stu-id="ce557-135">public void new(str filename, str mode)</span></span>      | <span data-ttu-id="ce557-136">AsciiIo クラスのインスタンスを作成します。</span><span class="sxs-lookup"><span data-stu-id="ce557-136">Creates an instance of the AsciiIo class.</span></span>                                                                                        |

## <a name="method-infielddelimiter"></a><span data-ttu-id="ce557-137">メソッド inFieldDelimiter</span><span class="sxs-lookup"><span data-stu-id="ce557-137">Method inFieldDelimiter</span></span>

<span data-ttu-id="ce557-138">AsciiIO オブジェクトによって表される入力ファイルのフィールド区切り記号として使用される文字を設定または取得します。</span><span class="sxs-lookup"><span data-stu-id="ce557-138">Sets or retrieves the character that is used as the field delimiter of an input file that is represented by an AsciiIO object.</span></span>

```xpp
public str inFieldDelimiter([str value])
```

### <a name="parameters---infielddelimiter"></a><span data-ttu-id="ce557-139">パラメーター - inFieldDelimiter</span><span class="sxs-lookup"><span data-stu-id="ce557-139">Parameters - inFieldDelimiter</span></span>

<span data-ttu-id="ce557-140">値</span><span class="sxs-lookup"><span data-stu-id="ce557-140">value</span></span>  
<span data-ttu-id="ce557-141">フィールドの区切り記号として割り当てられる文字。</span><span class="sxs-lookup"><span data-stu-id="ce557-141">The character to assign as the field delimiter.</span></span>

### <a name="return-value---infielddelimiter"></a><span data-ttu-id="ce557-142">戻り値 - inFieldDelimiter</span><span class="sxs-lookup"><span data-stu-id="ce557-142">Return Value - inFieldDelimiter</span></span>

<span data-ttu-id="ce557-143">フィールドの区切り記号として使用される文字。</span><span class="sxs-lookup"><span data-stu-id="ce557-143">The character that is used as the field delimiter.</span></span>

## <a name="method-inrecorddelimiter"></a><span data-ttu-id="ce557-144">メソッド inRecordDelimiter</span><span class="sxs-lookup"><span data-stu-id="ce557-144">Method inRecordDelimiter</span></span>

<span data-ttu-id="ce557-145">AsciiIO オブジェクトによって表される入力ファイルのレコード区切り記号として使用される文字を設定または取得します。</span><span class="sxs-lookup"><span data-stu-id="ce557-145">Sets or retrieves the character that is used as the record delimiter of an input file that is represented by an AsciiIO object.</span></span>

```xpp
public str inRecordDelimiter([str value])
```

### <a name="parameters---inrecorddelimiter"></a><span data-ttu-id="ce557-146">パラメーター - inRecordDelimiter</span><span class="sxs-lookup"><span data-stu-id="ce557-146">Parameters - inRecordDelimiter</span></span>

<span data-ttu-id="ce557-147">値</span><span class="sxs-lookup"><span data-stu-id="ce557-147">value</span></span>  
<span data-ttu-id="ce557-148">レコードの区切り記号として割り当てられる文字。</span><span class="sxs-lookup"><span data-stu-id="ce557-148">The character to assign as the record delimiter.</span></span>

### <a name="return-value---inrecorddelimiter"></a><span data-ttu-id="ce557-149">戻り値 - inRecordDelimiter</span><span class="sxs-lookup"><span data-stu-id="ce557-149">Return Value - inRecordDelimiter</span></span>

<span data-ttu-id="ce557-150">レコードの区切り記号として使用される文字。</span><span class="sxs-lookup"><span data-stu-id="ce557-150">The character that is used as the record delimiter.</span></span>

### <a name="remarks---inrecorddelimiter"></a><span data-ttu-id="ce557-151">備考 - inRecordDelimiter</span><span class="sxs-lookup"><span data-stu-id="ce557-151">Remarks - inRecordDelimiter</span></span>

<span data-ttu-id="ce557-152">標準的なテキストについては、区切り記号は改行文字です。</span><span class="sxs-lookup"><span data-stu-id="ce557-152">For standard text, the delimiter is a newline character.</span></span>

## <a name="method-inrecordlength"></a><span data-ttu-id="ce557-153">メソッド inRecordLength</span><span class="sxs-lookup"><span data-stu-id="ce557-153">Method inRecordLength</span></span>

<span data-ttu-id="ce557-154">入力ファイルのレコードの長さを設定または取得します。</span><span class="sxs-lookup"><span data-stu-id="ce557-154">Sets or retrieves the record length for an input file.</span></span>

```xpp
public int inRecordLength([int value])
```

### <a name="parameters---inrecordlength"></a><span data-ttu-id="ce557-155">パラメーター - inRecordLength</span><span class="sxs-lookup"><span data-stu-id="ce557-155">Parameters - inRecordLength</span></span>

<span data-ttu-id="ce557-156">値</span><span class="sxs-lookup"><span data-stu-id="ce557-156">value</span></span>  
<span data-ttu-id="ce557-157">入力ファイルのレコード長として割り当てる値。</span><span class="sxs-lookup"><span data-stu-id="ce557-157">The value to assign as the record length for the input file.</span></span>

### <a name="return-value---inrecordlength"></a><span data-ttu-id="ce557-158">戻り値 - inRecordLength</span><span class="sxs-lookup"><span data-stu-id="ce557-158">Return Value - inRecordLength</span></span>

<span data-ttu-id="ce557-159">入力ファイルのレコードの長さ。</span><span class="sxs-lookup"><span data-stu-id="ce557-159">The record length for the input file.</span></span>

### <a name="remarks---inrecordlength"></a><span data-ttu-id="ce557-160">備考 - inRecordLength</span><span class="sxs-lookup"><span data-stu-id="ce557-160">Remarks - inRecordLength</span></span>

<span data-ttu-id="ce557-161">固定長形式になっているファイルについては、inRecordLength プロパティを使用して、各レコードに対して指定された文字数以上が読み取られていないことを保証します。</span><span class="sxs-lookup"><span data-stu-id="ce557-161">For files that have a fixed-length format, use the inRecordLength property to guarantee that no more than the specified number of characters is read for each record.</span></span> <span data-ttu-id="ce557-162">レコード フォーマットが指定された inRecordDelimiter プロパティ値で上書きされた場合 (つまり、固定長が読み込まれる前に inRecordDelimiter 値が満たされている場合)、レコードは受け入れられ、それ以上のデータは読み込まれません。</span><span class="sxs-lookup"><span data-stu-id="ce557-162">If the record format is overruled by a specified inRecordDelimiter property value (in other words, if the inRecordDelimiter value is met before the fixed length is read), the record is accepted, and no more data is read.</span></span> <span data-ttu-id="ce557-163">固定数の文字を確実に読み取るには、inRecordDelimiter プロパティ値を空の文字列に設定します。</span><span class="sxs-lookup"><span data-stu-id="ce557-163">To make sure that a fixed number of characters is read, set the inRecordDelimiter property value to an empty string.</span></span> <span data-ttu-id="ce557-164">inRecordDelimiter プロパティ値が見つからない場合、inRecordDelimiter プロパティ値は読み取れる最大文字数になります。</span><span class="sxs-lookup"><span data-stu-id="ce557-164">When no inRecordDelimiter property value is found, the inRecordDelimiter property value is the maximum limit of characters to read.</span></span> <span data-ttu-id="ce557-165">レコードの長さのチェックを無効にするには、inRecordDelimiter プロパティ値を 0 (ゼロ) に設定します。</span><span class="sxs-lookup"><span data-stu-id="ce557-165">Set the inRecordDelimiter property value to 0 (zero) to disable the check of the record length.</span></span>

## <a name="method-outfielddelimiter"></a><span data-ttu-id="ce557-166">メソッド outFieldDelimiter</span><span class="sxs-lookup"><span data-stu-id="ce557-166">Method outFieldDelimiter</span></span>

<span data-ttu-id="ce557-167">AsciiIO オブジェクトによって表される出力ファイルのフィールド区切り記号として使用される文字を設定または取得します。</span><span class="sxs-lookup"><span data-stu-id="ce557-167">Sets or retrieves the character that is used as the field delimiter of an output file that is represented by an AsciiIO object.</span></span>

```xpp
public str outFieldDelimiter([str value])
```

### <a name="parameters---outfielddelimiter"></a><span data-ttu-id="ce557-168">パラメーター - outFieldDelimiter</span><span class="sxs-lookup"><span data-stu-id="ce557-168">Parameters - outFieldDelimiter</span></span>

<span data-ttu-id="ce557-169">値</span><span class="sxs-lookup"><span data-stu-id="ce557-169">value</span></span>  
<span data-ttu-id="ce557-170">フィールドの区切り記号として割り当てられる文字。</span><span class="sxs-lookup"><span data-stu-id="ce557-170">The character to assign as the field delimiter.</span></span>

### <a name="return-value---outfielddelimiter"></a><span data-ttu-id="ce557-171">戻り値 - outFieldDelimiter</span><span class="sxs-lookup"><span data-stu-id="ce557-171">Return Value - outFieldDelimiter</span></span>

<span data-ttu-id="ce557-172">フィールドの区切り記号として使用される文字。</span><span class="sxs-lookup"><span data-stu-id="ce557-172">The character that is used as the field delimiter.</span></span>

## <a name="method-outrecorddelimiter"></a><span data-ttu-id="ce557-173">メソッド outRecordDelimiter</span><span class="sxs-lookup"><span data-stu-id="ce557-173">Method outRecordDelimiter</span></span>

<span data-ttu-id="ce557-174">AsciiIO オブジェクトによって表される出力ファイルのレコード区切り記号として使用される文字を設定または取得します。</span><span class="sxs-lookup"><span data-stu-id="ce557-174">Sets or retrieves the character that is used as the record delimiter of an output file that is represented by an AsciiIO object.</span></span>

```xpp
public str outRecordDelimiter([str value])
```

### <a name="parameters---outrecorddelimiter"></a><span data-ttu-id="ce557-175">パラメーター - outRecordDelimiter</span><span class="sxs-lookup"><span data-stu-id="ce557-175">Parameters - outRecordDelimiter</span></span>

<span data-ttu-id="ce557-176">値</span><span class="sxs-lookup"><span data-stu-id="ce557-176">value</span></span>  
<span data-ttu-id="ce557-177">レコードの区切り記号として割り当てられる文字。</span><span class="sxs-lookup"><span data-stu-id="ce557-177">The character to assign as the record delimiter.</span></span>

### <a name="return-value---outrecorddelimiter"></a><span data-ttu-id="ce557-178">戻り値 - outRecordDelimiter</span><span class="sxs-lookup"><span data-stu-id="ce557-178">Return Value - outRecordDelimiter</span></span>

<span data-ttu-id="ce557-179">レコードの区切り記号として使用される文字。</span><span class="sxs-lookup"><span data-stu-id="ce557-179">The character that is used as the record delimiter.</span></span>

### <a name="remarks---outrecorddelimiter"></a><span data-ttu-id="ce557-180">備考 - outRecordDelimiter</span><span class="sxs-lookup"><span data-stu-id="ce557-180">Remarks - outRecordDelimiter</span></span>

<span data-ttu-id="ce557-181">標準的なテキスト ファイルについては、区切り記号は改行文字です。</span><span class="sxs-lookup"><span data-stu-id="ce557-181">For standard text files, the delimiter is a newline character.</span></span>

## <a name="method-read"></a><span data-ttu-id="ce557-182">メソッド read</span><span class="sxs-lookup"><span data-stu-id="ce557-182">Method read</span></span>

<span data-ttu-id="ce557-183">Io オブジェクトから次の完全なレコードを読み取ります。</span><span class="sxs-lookup"><span data-stu-id="ce557-183">Reads the next full record from the Io object.</span></span>

```xpp
public container read()
```

### <a name="return-value---read"></a><span data-ttu-id="ce557-184">戻り値 - read</span><span class="sxs-lookup"><span data-stu-id="ce557-184">Return Value - read</span></span>

<span data-ttu-id="ce557-185">Io オブジェクトからの次の完全なレコード。</span><span class="sxs-lookup"><span data-stu-id="ce557-185">The next full record from the Io object.</span></span>

### <a name="remarks---read"></a><span data-ttu-id="ce557-186">備考 - read</span><span class="sxs-lookup"><span data-stu-id="ce557-186">Remarks - read</span></span>

<span data-ttu-id="ce557-187">次の完全なレコードの定義は、次のプロパティ、inFieldDelimiter、inRecordDelimiter、および inRecordLength によって制御されます。</span><span class="sxs-lookup"><span data-stu-id="ce557-187">The definition of the next full record is controlled by the following properties: inFieldDelimiter, inRecordDelimiter, and inRecordLength.</span></span> <span data-ttu-id="ce557-188">レコードはコンテナーとして返されます。</span><span class="sxs-lookup"><span data-stu-id="ce557-188">The record is returned as a container.</span></span> <span data-ttu-id="ce557-189">コンテナー内の各エントリは、レコードの 1 つのフィールドを表します。</span><span class="sxs-lookup"><span data-stu-id="ce557-189">Each entry in the container represents one field in the record.</span></span> <span data-ttu-id="ce557-190">それぞれの特殊な Io クラスには、inFieldDelimiter、inRecordDelimiter、および inRecordLength のデフォルト設定があります。</span><span class="sxs-lookup"><span data-stu-id="ce557-190">Each of the specialized Io classes has default settings for inFieldDelimiter, inRecordDelimiter, and inRecordLength.</span></span> <span data-ttu-id="ce557-191">これらの設定では、最も一般的な形式の入力と出力が可能です。</span><span class="sxs-lookup"><span data-stu-id="ce557-191">These settings allow for input and output of the most common formats.</span></span> <span data-ttu-id="ce557-192">ただし、目的の形式をサポートするために、これらの設定の調整が生じる場合があります。</span><span class="sxs-lookup"><span data-stu-id="ce557-192">However, you might have to adjust these settings to support the desired format.</span></span>

## <a name="method-status"></a><span data-ttu-id="ce557-193">メソッド status</span><span class="sxs-lookup"><span data-stu-id="ce557-193">Method status</span></span>

<span data-ttu-id="ce557-194">ファイルでの最後の操作のステータスを返します。</span><span class="sxs-lookup"><span data-stu-id="ce557-194">Returns the status of the last operation on the file.</span></span>

```xpp
public IO_Status status()
```

### <a name="return-value---status"></a><span data-ttu-id="ce557-195">戻り値 - status</span><span class="sxs-lookup"><span data-stu-id="ce557-195">Return Value - status</span></span>

<span data-ttu-id="ce557-196">最後のファイル操作の状態。</span><span class="sxs-lookup"><span data-stu-id="ce557-196">The status of the last file operation.</span></span>

## <a name="method-write"></a><span data-ttu-id="ce557-197">メソッド write</span><span class="sxs-lookup"><span data-stu-id="ce557-197">Method write</span></span>

<span data-ttu-id="ce557-198">単純型の値を記述します。</span><span class="sxs-lookup"><span data-stu-id="ce557-198">Writes values of a simple type.</span></span>

```xpp
public boolean write(VarArg values)
```

### <a name="parameters---write"></a><span data-ttu-id="ce557-199">パラメーター - write</span><span class="sxs-lookup"><span data-stu-id="ce557-199">Parameters - write</span></span>

<span data-ttu-id="ce557-200">値</span><span class="sxs-lookup"><span data-stu-id="ce557-200">values</span></span>  
<span data-ttu-id="ce557-201">1 つ以上の値の、各単純型は、フィールドの区切り記号で区切られています。</span><span class="sxs-lookup"><span data-stu-id="ce557-201">One or more values, each of a simple type, separated by a field delimiter.</span></span> <span data-ttu-id="ce557-202">単純型は、文字列、整数、実数、列挙型、日付です。</span><span class="sxs-lookup"><span data-stu-id="ce557-202">The simple types are string, integer, real, enum, and date.</span></span>

### <a name="return-value---write"></a><span data-ttu-id="ce557-203">戻り値 - write</span><span class="sxs-lookup"><span data-stu-id="ce557-203">Return Value - write</span></span>

<span data-ttu-id="ce557-204">書き込み操作が成功する場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="ce557-204">true if the write operation succeeds; otherwise, false.</span></span> <span data-ttu-id="ce557-205">書き込み操作が失敗すると、ステータスをチェックし、原因について確認できます。</span><span class="sxs-lookup"><span data-stu-id="ce557-205">If the write operation fails, you can check the status to learn the cause.</span></span>

### <a name="remarks---write"></a><span data-ttu-id="ce557-206">備考 - write</span><span class="sxs-lookup"><span data-stu-id="ce557-206">Remarks - write</span></span>

<span data-ttu-id="ce557-207">このメソッドは、可変数の引数を受け入れます。</span><span class="sxs-lookup"><span data-stu-id="ce557-207">The method accepts a variable number of arguments.</span></span> <span data-ttu-id="ce557-208">指定された各値は、フィールドとして出力レコードに配置されます: 最初のフィールドとしての最初の引数、2 番目のフィールドとしての 2 番目の引数など。</span><span class="sxs-lookup"><span data-stu-id="ce557-208">Each value that is specified is put into the output record as a field: the first argument as the first field, the second argument as the second field, and so on.</span></span> <span data-ttu-id="ce557-209">フィールドは、outFieldDelimiter メソッドで指定される区切り記号で区切られます。</span><span class="sxs-lookup"><span data-stu-id="ce557-209">Fields are separated by the delimiter that is specified in the outFieldDelimiter method.</span></span> <span data-ttu-id="ce557-210">レコードは、outRecordDelimiter メソッドで指定される区切り記号で区切られます。</span><span class="sxs-lookup"><span data-stu-id="ce557-210">Records are separated by the delimiter that is specified in the outRecordDelimiter method.</span></span> <span data-ttu-id="ce557-211">完全なコンテナーを書き込むには、writeExp メソッドを使用します。</span><span class="sxs-lookup"><span data-stu-id="ce557-211">To write complete containers, use the writeExp method.</span></span>

## <a name="method-writechar"></a><span data-ttu-id="ce557-212">メソッド writeChar</span><span class="sxs-lookup"><span data-stu-id="ce557-212">Method writeChar</span></span>

```xpp
public boolean writeChar(int int)
```

### <a name="parameters---writechar"></a><span data-ttu-id="ce557-213">パラメーター - writeChar</span><span class="sxs-lookup"><span data-stu-id="ce557-213">Parameters - writeChar</span></span>

<span data-ttu-id="ce557-214">int</span><span class="sxs-lookup"><span data-stu-id="ce557-214">int</span></span>  

### <a name="return-value---writechar"></a><span data-ttu-id="ce557-215">戻り値 - writeChar</span><span class="sxs-lookup"><span data-stu-id="ce557-215">Return Value - writeChar</span></span>

## <a name="method-writeexp"></a><span data-ttu-id="ce557-216">メソッド writeExp</span><span class="sxs-lookup"><span data-stu-id="ce557-216">Method writeExp</span></span>

<span data-ttu-id="ce557-217">コンテナのコンテンツをファイルに記述します。</span><span class="sxs-lookup"><span data-stu-id="ce557-217">Writes the content of a container to a file.</span></span>

```xpp
public boolean writeExp(container data)
```

### <a name="parameters---writeexp"></a><span data-ttu-id="ce557-218">パラメーター - writeExp</span><span class="sxs-lookup"><span data-stu-id="ce557-218">Parameters - writeExp</span></span>

<span data-ttu-id="ce557-219">データ</span><span class="sxs-lookup"><span data-stu-id="ce557-219">data</span></span>  
<span data-ttu-id="ce557-220">レコードのデータを保持するコンテナー。</span><span class="sxs-lookup"><span data-stu-id="ce557-220">The container that holds data for the record.</span></span>

### <a name="return-value---writeexp"></a><span data-ttu-id="ce557-221">戻り値 - writeExp</span><span class="sxs-lookup"><span data-stu-id="ce557-221">Return Value - writeExp</span></span>

<span data-ttu-id="ce557-222">操作が成功する場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="ce557-222">true if the operation succeeds; otherwise, false.</span></span> <span data-ttu-id="ce557-223">工程が失敗すると、ステータスをチェックし原因について確認します。</span><span class="sxs-lookup"><span data-stu-id="ce557-223">If the operation fails, check the status to learn the cause.</span></span>

### <a name="remarks---writeexp"></a><span data-ttu-id="ce557-224">備考 - writeExp</span><span class="sxs-lookup"><span data-stu-id="ce557-224">Remarks - writeExp</span></span>

<span data-ttu-id="ce557-225">コンテナー内のエントリはフィールドとして扱われます。</span><span class="sxs-lookup"><span data-stu-id="ce557-225">The entries in the container are treated as fields.</span></span> <span data-ttu-id="ce557-226">コンテナーは、完全なレコードとして扱われます。</span><span class="sxs-lookup"><span data-stu-id="ce557-226">The container is treated as a full record.</span></span> <span data-ttu-id="ce557-227">フィールドは、outFieldDelimiter メソッドで指定される区切り記号で区切られます。</span><span class="sxs-lookup"><span data-stu-id="ce557-227">Fields are separated by the delimiter that is specified in the outFieldDelimiter method.</span></span> <span data-ttu-id="ce557-228">レコードは、outRecordDelimiter メソッドで指定される区切り記号で区切られます。</span><span class="sxs-lookup"><span data-stu-id="ce557-228">Records are separated by the delimiter that is specified in the outRecordDelimiter method.</span></span>

## <a name="method-writeraw"></a><span data-ttu-id="ce557-229">メソッド writeRaw</span><span class="sxs-lookup"><span data-stu-id="ce557-229">Method writeRaw</span></span>

```xpp
public boolean writeRaw(str data)
```

### <a name="parameters---writeraw"></a><span data-ttu-id="ce557-230">パラメーター - writeRaw</span><span class="sxs-lookup"><span data-stu-id="ce557-230">Parameters - writeRaw</span></span>

<span data-ttu-id="ce557-231">データ</span><span class="sxs-lookup"><span data-stu-id="ce557-231">data</span></span>  

### <a name="return-value---writeraw"></a><span data-ttu-id="ce557-232">戻り値 - writeRaw</span><span class="sxs-lookup"><span data-stu-id="ce557-232">Return Value - writeRaw</span></span>

## <a name="method-finalize"></a><span data-ttu-id="ce557-233">メソッド finalize</span><span class="sxs-lookup"><span data-stu-id="ce557-233">Method finalize</span></span>

<span data-ttu-id="ce557-234">ファイルを閉じ、ファイル バッファーをディスクにフラッシュします。</span><span class="sxs-lookup"><span data-stu-id="ce557-234">Closes the file and then flushes the file buffers to disk.</span></span>

```xpp
public void finalize()
```

### <a name="remarks---finalize"></a><span data-ttu-id="ce557-235">備考 - finalize</span><span class="sxs-lookup"><span data-stu-id="ce557-235">Remarks - finalize</span></span>

<span data-ttu-id="ce557-236">AsciiIo オブジェクトは通常そのスコープの終了後に確定されます。</span><span class="sxs-lookup"><span data-stu-id="ce557-236">An AsciiIo object is usually finalized after its scope has ended.</span></span> <span data-ttu-id="ce557-237">このメソッドは、通常は直接呼び出されません。</span><span class="sxs-lookup"><span data-stu-id="ce557-237">This method is not usually called directly.</span></span> <span data-ttu-id="ce557-238">AsciiIo オブジェクトが確定済みになるまで、ファイルに書き込まれる出力は無効です。</span><span class="sxs-lookup"><span data-stu-id="ce557-238">Output that is written to the file is not valid until the AsciiIo object is finalized.</span></span>

## <a name="method-new"></a><span data-ttu-id="ce557-239">メソッド new</span><span class="sxs-lookup"><span data-stu-id="ce557-239">Method new</span></span>

<span data-ttu-id="ce557-240">AsciiIo クラスのインスタンスを作成します。</span><span class="sxs-lookup"><span data-stu-id="ce557-240">Creates an instance of the AsciiIo class.</span></span>

```xpp
public void new(str filename, str mode)
```

### <a name="parameters---new"></a><span data-ttu-id="ce557-241">パラメーター - new</span><span class="sxs-lookup"><span data-stu-id="ce557-241">Parameters - new</span></span>

<span data-ttu-id="ce557-242">filename</span><span class="sxs-lookup"><span data-stu-id="ce557-242">filename</span></span>  
<span data-ttu-id="ce557-243">AsciiIo クラスのこのインスタンスを作成するために使用するモード。</span><span class="sxs-lookup"><span data-stu-id="ce557-243">The mode to use to create this instance of the AsciiIo class.</span></span>

<!-- -->

<span data-ttu-id="ce557-244">モード</span><span class="sxs-lookup"><span data-stu-id="ce557-244">mode</span></span>  
<span data-ttu-id="ce557-245">AsciiIo クラスのこのインスタンスを作成するために使用するモード。</span><span class="sxs-lookup"><span data-stu-id="ce557-245">The mode to use to create this instance of the AsciiIo class.</span></span>

### <a name="remarks---new"></a><span data-ttu-id="ce557-246">備考 - new</span><span class="sxs-lookup"><span data-stu-id="ce557-246">Remarks - new</span></span>

<span data-ttu-id="ce557-247">攻撃者が新しいメソッドへの入力を制御できる場合、セキュリティ上のリスクが存在します。</span><span class="sxs-lookup"><span data-stu-id="ce557-247">If an attacker can control input to the new method, a security risk exists.</span></span> <span data-ttu-id="ce557-248">したがって、このメソッドは、コード アクセス セキュリティで実行されます。</span><span class="sxs-lookup"><span data-stu-id="ce557-248">Therefore, this method runs under Code Access Security.</span></span> <span data-ttu-id="ce557-249">サーバー上でこのメソッドを呼び出すには、FileIOPermission クラスからのアクセス許可が必要です。</span><span class="sxs-lookup"><span data-stu-id="ce557-249">Calls to this method on the server require permission from the FileIOPermission class.</span></span> <span data-ttu-id="ce557-250">ユーザーがこのメソッドを呼び出すコントロールで、SysDevelopment へのセキュリティ キーを設定して開発権限を持っていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="ce557-250">Make sure that the user has development privileges by setting the security key to SysDevelopment on the control that calls this method.</span></span>

### <a name="examples---new"></a><span data-ttu-id="ce557-251">例 - new</span><span class="sxs-lookup"><span data-stu-id="ce557-251">Examples - new</span></span>

<span data-ttu-id="ce557-252">次の例では、AsciiIo クラスを使用してテキスト ファイルから読み込みます。</span><span class="sxs-lookup"><span data-stu-id="ce557-252">The following example uses the AsciiIo class to read from a text file.</span></span>

```xpp
void AsciiIoExample() 
{ 
    AsciiIo asciiIo; 
    container con; 
    FileIoPermission perm; 
```

```xpp
    #define.ExampleFile(@"c:\test.txt") 
    #define.ExampleOpenMode("r") 
```

```xpp
    // The AsciiIo.new method runs under code access permission. 
    perm = new FileIoPermission(#ExampleFile, #ExampleOpenMode); 
    if (perm == null) 
    { 
        return; 
    } 
```

```xpp
    // Code access permission scope starts here. 
     perm.assert(); 
```

```xpp
     asciiIo = new AsciiIo(#ExampleFile, #ExampleOpenMode); 
    if (asciiIo != null) 
    { 
          con = asciiIo.read(); 
    } 
    // Closes the code access permission scope. 
    CodeAccessPermission::revertAssert(); 
}
```

