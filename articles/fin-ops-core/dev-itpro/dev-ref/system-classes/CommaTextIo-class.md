---
title: CommaTextIo クラス
description: このトピックでは、CommaTextIo クラスについて説明します。
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
ms.openlocfilehash: 00c6a0481609cb5fc19111c68543bbd0b0156665
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502709"
---
# <a name="class-commatextio"></a><span data-ttu-id="ce6c2-103">クラス CommaTextIo</span><span class="sxs-lookup"><span data-stu-id="ce6c2-103">Class CommaTextIo</span></span>

[!include [banner](../../includes/banner.md)]

```xpp
class CommaTextIo extends Io
```

## <a name="remarks"></a><span data-ttu-id="ce6c2-104">備考</span><span class="sxs-lookup"><span data-stu-id="ce6c2-104">Remarks</span></span>

## <a name="examples"></a><span data-ttu-id="ce6c2-105">例</span><span class="sxs-lookup"><span data-stu-id="ce6c2-105">Examples</span></span>

## <a name="methods"></a><span data-ttu-id="ce6c2-106">メソッド</span><span class="sxs-lookup"><span data-stu-id="ce6c2-106">Methods</span></span>

| <span data-ttu-id="ce6c2-107">方法</span><span class="sxs-lookup"><span data-stu-id="ce6c2-107">Method</span></span>                                                    | <span data-ttu-id="ce6c2-108">説明</span><span class="sxs-lookup"><span data-stu-id="ce6c2-108">Description</span></span>                                                                                                                  |
|-----------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ce6c2-109">public int filePosition()</span><span class="sxs-lookup"><span data-stu-id="ce6c2-109">public int filePosition()</span></span>                                 |                                                                                                                              |
| <span data-ttu-id="ce6c2-110">public str inFieldDelimiter(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="ce6c2-110">public str inFieldDelimiter(\[str value\])</span></span>                | <span data-ttu-id="ce6c2-111">\*Io によってアクセスされるレコード内のフィールドを区切るために使用される区切り文字を決定します。</span><span class="sxs-lookup"><span data-stu-id="ce6c2-111">Determines the delimiter used to separate fields in records accessed by the \*Io classes.</span></span>                                    |
| <span data-ttu-id="ce6c2-112">public str inRecordDelimiter(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="ce6c2-112">public str inRecordDelimiter(\[str value\])</span></span>               | <span data-ttu-id="ce6c2-113">完全なレコードが読み込まれたかどうかを判断するために、\*Io クラスに検索する文字を決定します。</span><span class="sxs-lookup"><span data-stu-id="ce6c2-113">Determines to the \*Io classes what character or characters to search for to determine whether a full record has been read.</span></span>  |
| <span data-ttu-id="ce6c2-114">public int inRecordLength(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="ce6c2-114">public int inRecordLength(\[int value\])</span></span>                  | <span data-ttu-id="ce6c2-115">ファイル内の各レコードを読み取る文字数を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="ce6c2-115">Gets or sets the number of characters to read for each record in a file.</span></span>                                                     |
| <span data-ttu-id="ce6c2-116">public str outFieldDelimiter(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="ce6c2-116">public str outFieldDelimiter(\[str value\])</span></span>               | <span data-ttu-id="ce6c2-117">レコードのフィールドを区切るために使用されるファイルに書き込まれる文字のシーケンスを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="ce6c2-117">Gets or sets the sequence of characters that are written to a file that is used to separate the fields of a record.</span></span>          |
| <span data-ttu-id="ce6c2-118">public str outRecordDelimiter(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="ce6c2-118">public str outRecordDelimiter(\[str value\])</span></span>              | <span data-ttu-id="ce6c2-119">出力ファイルでレコードを区切る出力ファイルに書き込まれる文字のシーケンスを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="ce6c2-119">Gets or sets the sequence of characters that is written to the output files, which separate the records in the output files.</span></span> |
| <span data-ttu-id="ce6c2-120">public container read()</span><span class="sxs-lookup"><span data-stu-id="ce6c2-120">public container read()</span></span>                                   | <span data-ttu-id="ce6c2-121">Io オブジェクトから次の完全なレコードを読み取ります。</span><span class="sxs-lookup"><span data-stu-id="ce6c2-121">Reads the next full record from the Io object.</span></span>                                                                               |
| <span data-ttu-id="ce6c2-122">public IO\_Status status()</span><span class="sxs-lookup"><span data-stu-id="ce6c2-122">public IO\_Status status()</span></span>                                | <span data-ttu-id="ce6c2-123">Io オブジェクトで実行された最後の操作のステータスを取得します。</span><span class="sxs-lookup"><span data-stu-id="ce6c2-123">Retrieves the status of the last operation that was performed on the Io object.</span></span>                                              |
| <span data-ttu-id="ce6c2-124">public boolean write(VarArg values)</span><span class="sxs-lookup"><span data-stu-id="ce6c2-124">public boolean write(VarArg values)</span></span>                       | <span data-ttu-id="ce6c2-125">単純型の値を記述します。</span><span class="sxs-lookup"><span data-stu-id="ce6c2-125">Writes values of a simple type.</span></span>                                                                                              |
| <span data-ttu-id="ce6c2-126">public boolean writeExp(container data)</span><span class="sxs-lookup"><span data-stu-id="ce6c2-126">public boolean writeExp(container data)</span></span>                   | <span data-ttu-id="ce6c2-127">コンテナのコンテンツをファイルに記述します。</span><span class="sxs-lookup"><span data-stu-id="ce6c2-127">Writes the content of a container to a file.</span></span>                                                                                 |
| <span data-ttu-id="ce6c2-128">public void finalize()</span><span class="sxs-lookup"><span data-stu-id="ce6c2-128">public void finalize()</span></span>                                    | <span data-ttu-id="ce6c2-129">ファイルを閉じ、データが書き込まれている場合、ファイル バッファーをディスクにフラッシュします。</span><span class="sxs-lookup"><span data-stu-id="ce6c2-129">Closes the file and, if data was written, flushes the file buffers to disk.</span></span>                                                  |
| <span data-ttu-id="ce6c2-130">public void new(str filename, str mode, \[int codepage\])</span><span class="sxs-lookup"><span data-stu-id="ce6c2-130">public void new(str filename, str mode, \[int codepage\])</span></span> | <span data-ttu-id="ce6c2-131">Object クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="ce6c2-131">Initializes a new instance of the Object class.</span></span>                                                                              |

## <a name="method-fileposition"></a><span data-ttu-id="ce6c2-132">メソッド filePosition</span><span class="sxs-lookup"><span data-stu-id="ce6c2-132">Method filePosition</span></span>

```xpp
public int filePosition()
```

### <a name="return-value---fileposition"></a><span data-ttu-id="ce6c2-133">戻り値 - filePosition</span><span class="sxs-lookup"><span data-stu-id="ce6c2-133">Return Value - filePosition</span></span>

## <a name="method-infielddelimiter"></a><span data-ttu-id="ce6c2-134">メソッド inFieldDelimiter</span><span class="sxs-lookup"><span data-stu-id="ce6c2-134">Method inFieldDelimiter</span></span>

<span data-ttu-id="ce6c2-135">\*Io によってアクセスされるレコード内のフィールドを区切るために使用される区切り文字を決定します。</span><span class="sxs-lookup"><span data-stu-id="ce6c2-135">Determines the delimiter used to separate fields in records accessed by the \*Io classes.</span></span>

```xpp
public str inFieldDelimiter([str value])
```

### <a name="parameters---infielddelimiter"></a><span data-ttu-id="ce6c2-136">パラメーター - inFieldDelimiter</span><span class="sxs-lookup"><span data-stu-id="ce6c2-136">Parameters - inFieldDelimiter</span></span>

<span data-ttu-id="ce6c2-137">値</span><span class="sxs-lookup"><span data-stu-id="ce6c2-137">value</span></span>  

### <a name="return-value---infielddelimiter"></a><span data-ttu-id="ce6c2-138">戻り値 - inFieldDelimiter</span><span class="sxs-lookup"><span data-stu-id="ce6c2-138">Return Value - inFieldDelimiter</span></span>

<span data-ttu-id="ce6c2-139">\*Io によってアクセスされるレコード内のフィールドを区切るために使用される区切り文字。</span><span class="sxs-lookup"><span data-stu-id="ce6c2-139">The delimiter used to separate fields in records accessed by the \*Io classes.</span></span>

## <a name="method-inrecorddelimiter"></a><span data-ttu-id="ce6c2-140">メソッド inRecordDelimiter</span><span class="sxs-lookup"><span data-stu-id="ce6c2-140">Method inRecordDelimiter</span></span>

<span data-ttu-id="ce6c2-141">完全なレコードが読み込まれたかどうかを判断するために、\*Io クラスに検索する文字を決定します。</span><span class="sxs-lookup"><span data-stu-id="ce6c2-141">Determines to the \*Io classes what character or characters to search for to determine whether a full record has been read.</span></span>

```xpp
public str inRecordDelimiter([str value])
```

### <a name="parameters---inrecorddelimiter"></a><span data-ttu-id="ce6c2-142">パラメーター - inRecordDelimiter</span><span class="sxs-lookup"><span data-stu-id="ce6c2-142">Parameters - inRecordDelimiter</span></span>

<span data-ttu-id="ce6c2-143">値</span><span class="sxs-lookup"><span data-stu-id="ce6c2-143">value</span></span>  

### <a name="return-value---inrecorddelimiter"></a><span data-ttu-id="ce6c2-144">戻り値 - inRecordDelimiter</span><span class="sxs-lookup"><span data-stu-id="ce6c2-144">Return Value - inRecordDelimiter</span></span>

<span data-ttu-id="ce6c2-145">完全なレコードが読み込まれたかどうかを示す文字。</span><span class="sxs-lookup"><span data-stu-id="ce6c2-145">The character or characters that indicate whether a full record has been read.</span></span>

### <a name="remarks---inrecorddelimiter"></a><span data-ttu-id="ce6c2-146">備考 - inRecordDelimiter</span><span class="sxs-lookup"><span data-stu-id="ce6c2-146">Remarks - inRecordDelimiter</span></span>

<span data-ttu-id="ce6c2-147">標準的なテキストについては、区切り記号は改行文字です。</span><span class="sxs-lookup"><span data-stu-id="ce6c2-147">For standard text, the delimiter is a newline character.</span></span>

## <a name="method-inrecordlength"></a><span data-ttu-id="ce6c2-148">メソッド inRecordLength</span><span class="sxs-lookup"><span data-stu-id="ce6c2-148">Method inRecordLength</span></span>

<span data-ttu-id="ce6c2-149">ファイル内の各レコードを読み取る文字数を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="ce6c2-149">Gets or sets the number of characters to read for each record in a file.</span></span>

```xpp
public int inRecordLength([int value])
```

### <a name="parameters---inrecordlength"></a><span data-ttu-id="ce6c2-150">パラメーター - inRecordLength</span><span class="sxs-lookup"><span data-stu-id="ce6c2-150">Parameters - inRecordLength</span></span>

<span data-ttu-id="ce6c2-151">値</span><span class="sxs-lookup"><span data-stu-id="ce6c2-151">value</span></span>  

### <a name="return-value---inrecordlength"></a><span data-ttu-id="ce6c2-152">戻り値 - inRecordLength</span><span class="sxs-lookup"><span data-stu-id="ce6c2-152">Return Value - inRecordLength</span></span>

<span data-ttu-id="ce6c2-153">ファイル内の各レコードを読み取る文字数。</span><span class="sxs-lookup"><span data-stu-id="ce6c2-153">The number of characters to read for each record in the file.</span></span>

### <a name="remarks---inrecordlength"></a><span data-ttu-id="ce6c2-154">備考 - inRecordLength</span><span class="sxs-lookup"><span data-stu-id="ce6c2-154">Remarks - inRecordLength</span></span>

<span data-ttu-id="ce6c2-155">固定長形式になっているファイルについては、inRecordLength プロパティを使用して、各レコードに対して指定された文字数以上が読み取られていないことを保証します。</span><span class="sxs-lookup"><span data-stu-id="ce6c2-155">For files that have a fixed-length format, use the inRecordLength property to guarantee that no more than the specified number of characters are read for each record.</span></span> <span data-ttu-id="ce6c2-156">レコード フォーマットが指定された inRecordDelimiter プロパティ値で上書きされた場合、つまり、固定長が読み込まれる前に inRecordDelimiter 値が満たされている場合)、レコードは受け入れられ、追加のデータは読み込まれません。</span><span class="sxs-lookup"><span data-stu-id="ce6c2-156">If the record format is overruled by a specified inRecordDelimiter property value , that is the inRecordDelimiter value is met before the fixed length is read, the record is accepted, and no additional data is read.</span></span> <span data-ttu-id="ce6c2-157">固定数の文字を確実に読み取るには、inRecordDelimiter プロパティ値を空の文字列に設定します。</span><span class="sxs-lookup"><span data-stu-id="ce6c2-157">To guarantee that a fixed number of characters are read, set the inRecordDelimiter property value to an empty string.</span></span> <span data-ttu-id="ce6c2-158">inRecordDelimiter プロパティ値が見つからない場合、inRecordDelimiter プロパティ値は読み取れる最大文字数になります。</span><span class="sxs-lookup"><span data-stu-id="ce6c2-158">When no inRecordDelimiter property value is found, the inRecordDelimiter property value is the maximum limit of characters to read.</span></span> <span data-ttu-id="ce6c2-159">レコードの長さチェックを無効にするには、inRecordDelimiter プロパティ値をゼロに設定します。</span><span class="sxs-lookup"><span data-stu-id="ce6c2-159">Set the inRecordDelimiter property value to zero to disable the record length check.</span></span>

## <a name="method-outfielddelimiter"></a><span data-ttu-id="ce6c2-160">メソッド outFieldDelimiter</span><span class="sxs-lookup"><span data-stu-id="ce6c2-160">Method outFieldDelimiter</span></span>

<span data-ttu-id="ce6c2-161">レコードのフィールドを区切るために使用されるファイルに書き込まれる文字のシーケンスを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="ce6c2-161">Gets or sets the sequence of characters that are written to a file that is used to separate the fields of a record.</span></span>

```xpp
public str outFieldDelimiter([str value])
```

### <a name="parameters---outfielddelimiter"></a><span data-ttu-id="ce6c2-162">パラメーター - outFieldDelimiter</span><span class="sxs-lookup"><span data-stu-id="ce6c2-162">Parameters - outFieldDelimiter</span></span>

<span data-ttu-id="ce6c2-163">値</span><span class="sxs-lookup"><span data-stu-id="ce6c2-163">value</span></span>  

### <a name="return-value---outfielddelimiter"></a><span data-ttu-id="ce6c2-164">戻り値 - outFieldDelimiter</span><span class="sxs-lookup"><span data-stu-id="ce6c2-164">Return Value - outFieldDelimiter</span></span>

<span data-ttu-id="ce6c2-165">レコードのフィールドを区切るために使用されるファイルに書き込まれる文字のシーケンス。</span><span class="sxs-lookup"><span data-stu-id="ce6c2-165">The sequence of characters that are written to a file that is used to separate the fields of a record.</span></span>

## <a name="method-outrecorddelimiter"></a><span data-ttu-id="ce6c2-166">メソッド outRecordDelimiter</span><span class="sxs-lookup"><span data-stu-id="ce6c2-166">Method outRecordDelimiter</span></span>

<span data-ttu-id="ce6c2-167">出力ファイルでレコードを区切る出力ファイルに書き込まれる文字のシーケンスを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="ce6c2-167">Gets or sets the sequence of characters that is written to the output files, which separate the records in the output files.</span></span>

```xpp
public str outRecordDelimiter([str value])
```

### <a name="parameters---outrecorddelimiter"></a><span data-ttu-id="ce6c2-168">パラメーター - outRecordDelimiter</span><span class="sxs-lookup"><span data-stu-id="ce6c2-168">Parameters - outRecordDelimiter</span></span>

<span data-ttu-id="ce6c2-169">値</span><span class="sxs-lookup"><span data-stu-id="ce6c2-169">value</span></span>  

### <a name="return-value---outrecorddelimiter"></a><span data-ttu-id="ce6c2-170">戻り値 - outRecordDelimiter</span><span class="sxs-lookup"><span data-stu-id="ce6c2-170">Return Value - outRecordDelimiter</span></span>

<span data-ttu-id="ce6c2-171">出力ファイルに書き込まれる文字のシーケンス。</span><span class="sxs-lookup"><span data-stu-id="ce6c2-171">The sequence of characters that is written to the output files.</span></span>

### <a name="remarks---outrecorddelimiter"></a><span data-ttu-id="ce6c2-172">備考 - outRecordDelimiter</span><span class="sxs-lookup"><span data-stu-id="ce6c2-172">Remarks - outRecordDelimiter</span></span>

<span data-ttu-id="ce6c2-173">標準的なテキスト ファイルについては、区切り記号は改行文字です。</span><span class="sxs-lookup"><span data-stu-id="ce6c2-173">For standard text files, the delimiter is a newline character.</span></span>

## <a name="method-read"></a><span data-ttu-id="ce6c2-174">メソッド read</span><span class="sxs-lookup"><span data-stu-id="ce6c2-174">Method read</span></span>

<span data-ttu-id="ce6c2-175">Io オブジェクトから次の完全なレコードを読み取ります。</span><span class="sxs-lookup"><span data-stu-id="ce6c2-175">Reads the next full record from the Io object.</span></span>

```xpp
public container read()
```

### <a name="return-value---read"></a><span data-ttu-id="ce6c2-176">戻り値 - read</span><span class="sxs-lookup"><span data-stu-id="ce6c2-176">Return Value - read</span></span>

<span data-ttu-id="ce6c2-177">入出力オブジェクトから次の完全なレコードを保持するコンテナーです。</span><span class="sxs-lookup"><span data-stu-id="ce6c2-177">A container that holds the next full record from the Io object.</span></span>

### <a name="remarks---read"></a><span data-ttu-id="ce6c2-178">備考 - read</span><span class="sxs-lookup"><span data-stu-id="ce6c2-178">Remarks - read</span></span>

<span data-ttu-id="ce6c2-179">次の完全なレコードの定義は、次のプロパティ、inFieldDelimiter、inRecordDelimiter、および inRecordLength メソッド プロパティによって制御されます。</span><span class="sxs-lookup"><span data-stu-id="ce6c2-179">The definition of the next full record is controlled by the inFieldDelimiter, inRecordDelimiter, and inRecordLength method properties.</span></span> <span data-ttu-id="ce6c2-180">レコードはコンテナーとして返されます。</span><span class="sxs-lookup"><span data-stu-id="ce6c2-180">The record is returned as a container.</span></span> <span data-ttu-id="ce6c2-181">コンテナー内の各エントリは、レコードの 1 つのフィールドと同じです。</span><span class="sxs-lookup"><span data-stu-id="ce6c2-181">Each entry in the container equals one field in the record.</span></span> <span data-ttu-id="ce6c2-182">それぞれの特殊な Io クラスには、inFieldDelimiter、inRecordDelimiter、および inRecordLength のプロパティのデフォルト設定があります。</span><span class="sxs-lookup"><span data-stu-id="ce6c2-182">Each specialized Io class has default settings for the inFieldDelimiter, inRecordDelimiter, and inRecordLength properties.</span></span> <span data-ttu-id="ce6c2-183">これらの既定の設定では、最も一般的な形式の入力と出力が可能です。</span><span class="sxs-lookup"><span data-stu-id="ce6c2-183">These default settings enable input and output in the most common formats.</span></span> <span data-ttu-id="ce6c2-184">ただし、目的の形式をサポートするために、これらの設定の調整が生じる場合があります。</span><span class="sxs-lookup"><span data-stu-id="ce6c2-184">However, you might have to adjust these settings to support the desired format.</span></span>

## <a name="method-status"></a><span data-ttu-id="ce6c2-185">メソッド status</span><span class="sxs-lookup"><span data-stu-id="ce6c2-185">Method status</span></span>

<span data-ttu-id="ce6c2-186">Io オブジェクトで実行された最後の操作のステータスを取得します。</span><span class="sxs-lookup"><span data-stu-id="ce6c2-186">Retrieves the status of the last operation that was performed on the Io object.</span></span>

```xpp
public IO_Status status()
```

### <a name="return-value---status"></a><span data-ttu-id="ce6c2-187">戻り値 - status</span><span class="sxs-lookup"><span data-stu-id="ce6c2-187">Return Value - status</span></span>

<span data-ttu-id="ce6c2-188">IO\_Status システム列挙値としての最後の操作の状態。</span><span class="sxs-lookup"><span data-stu-id="ce6c2-188">The status of the last operation, as an IO\_Status system enumeration value.</span></span>

### <a name="remarks---status"></a><span data-ttu-id="ce6c2-189">備考 - status</span><span class="sxs-lookup"><span data-stu-id="ce6c2-189">Remarks - status</span></span>

<span data-ttu-id="ce6c2-190">返される IO\_Status の値の範囲は、Io クラスによって異なります。</span><span class="sxs-lookup"><span data-stu-id="ce6c2-190">The range of IO\_Status values that can be returned varies, depending on the Io class.</span></span>

## <a name="method-write"></a><span data-ttu-id="ce6c2-191">メソッド write</span><span class="sxs-lookup"><span data-stu-id="ce6c2-191">Method write</span></span>

<span data-ttu-id="ce6c2-192">単純型の値を記述します。</span><span class="sxs-lookup"><span data-stu-id="ce6c2-192">Writes values of a simple type.</span></span>

```xpp
public boolean write(VarArg values)
```

### <a name="parameters---write"></a><span data-ttu-id="ce6c2-193">パラメーター - write</span><span class="sxs-lookup"><span data-stu-id="ce6c2-193">Parameters - write</span></span>

<span data-ttu-id="ce6c2-194">値</span><span class="sxs-lookup"><span data-stu-id="ce6c2-194">values</span></span>  
<span data-ttu-id="ce6c2-195">単純型の値。</span><span class="sxs-lookup"><span data-stu-id="ce6c2-195">A value of a simple type.</span></span> <span data-ttu-id="ce6c2-196">単純型は、文字列、整数、実数、列挙型、日付です。</span><span class="sxs-lookup"><span data-stu-id="ce6c2-196">The simple types are string, integer, real, enum, and date.</span></span>

### <a name="return-value---write"></a><span data-ttu-id="ce6c2-197">戻り値 - write</span><span class="sxs-lookup"><span data-stu-id="ce6c2-197">Return Value - write</span></span>

<span data-ttu-id="ce6c2-198">書き込み操作が成功する場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="ce6c2-198">true if the write operation is successful; otherwise, false.</span></span> <span data-ttu-id="ce6c2-199">書き込み操作が失敗すると、ステータス メソッドを使用して、原因について確認できます。</span><span class="sxs-lookup"><span data-stu-id="ce6c2-199">If the write operation fails, you can use the status method to determine the cause.</span></span>

### <a name="remarks---write"></a><span data-ttu-id="ce6c2-200">備考 - write</span><span class="sxs-lookup"><span data-stu-id="ce6c2-200">Remarks - write</span></span>

<span data-ttu-id="ce6c2-201">このメソッドは、可変数の引数を受け入れます。</span><span class="sxs-lookup"><span data-stu-id="ce6c2-201">The method accepts a variable number of arguments.</span></span> <span data-ttu-id="ce6c2-202">指定された各値は、フィールドとして出力レコードに配置されます。</span><span class="sxs-lookup"><span data-stu-id="ce6c2-202">Each value that is specified is put into the output record as a field.</span></span> <span data-ttu-id="ce6c2-203">最初の引数は最初のフィールドであり、2 番目の引数は 2 番目のフィールドなどになります。</span><span class="sxs-lookup"><span data-stu-id="ce6c2-203">The first argument is the first field, the second argument is the second field, and so on.</span></span> <span data-ttu-id="ce6c2-204">フィールドは、outFieldDelimiter メソッドで指定される区切り記号で区切られます。</span><span class="sxs-lookup"><span data-stu-id="ce6c2-204">Fields are separated by the delimiter that is specified in the outFieldDelimiter method.</span></span> <span data-ttu-id="ce6c2-205">レコードは、outRecordDelimiter メソッドで指定される区切り記号で区切られます。</span><span class="sxs-lookup"><span data-stu-id="ce6c2-205">Records are separated by the delimiter that is specified in the outRecordDelimiter method.</span></span> <span data-ttu-id="ce6c2-206">完全なコンテナーを書き込むには、writeExp メソッドを使用します。</span><span class="sxs-lookup"><span data-stu-id="ce6c2-206">To write complete containers, use the writeExp method.</span></span>

## <a name="method-writeexp"></a><span data-ttu-id="ce6c2-207">メソッド writeExp</span><span class="sxs-lookup"><span data-stu-id="ce6c2-207">Method writeExp</span></span>

<span data-ttu-id="ce6c2-208">コンテナのコンテンツをファイルに記述します。</span><span class="sxs-lookup"><span data-stu-id="ce6c2-208">Writes the content of a container to a file.</span></span>

```xpp
public boolean writeExp(container data)
```

### <a name="parameters---writeexp"></a><span data-ttu-id="ce6c2-209">パラメーター - writeExp</span><span class="sxs-lookup"><span data-stu-id="ce6c2-209">Parameters - writeExp</span></span>

<span data-ttu-id="ce6c2-210">データ</span><span class="sxs-lookup"><span data-stu-id="ce6c2-210">data</span></span>  
<span data-ttu-id="ce6c2-211">レコードのデータを保持するコンテナー。</span><span class="sxs-lookup"><span data-stu-id="ce6c2-211">The container that holds data for the record.</span></span>

### <a name="return-value---writeexp"></a><span data-ttu-id="ce6c2-212">戻り値 - writeExp</span><span class="sxs-lookup"><span data-stu-id="ce6c2-212">Return Value - writeExp</span></span>

<span data-ttu-id="ce6c2-213">操作が成功する場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="ce6c2-213">true if the operation is successful; otherwise, false.</span></span>

### <a name="remarks---writeexp"></a><span data-ttu-id="ce6c2-214">備考 - writeExp</span><span class="sxs-lookup"><span data-stu-id="ce6c2-214">Remarks - writeExp</span></span>

<span data-ttu-id="ce6c2-215">このメソッドが false を返す場合、ステータス メソッドで原因を確認します。</span><span class="sxs-lookup"><span data-stu-id="ce6c2-215">If this method returns false, check the status method for the cause.</span></span> <span data-ttu-id="ce6c2-216">コンテナー内のエントリはフィールドとして扱われ、コンテナーは完全なレコードとして扱われます。</span><span class="sxs-lookup"><span data-stu-id="ce6c2-216">The entries in the container are treated as fields, and the container is treated as a full record.</span></span> <span data-ttu-id="ce6c2-217">フィールド区切り記号は、outFieldDelimiter メソッドで定義されています。</span><span class="sxs-lookup"><span data-stu-id="ce6c2-217">The field separator is defined in the outFieldDelimiter method.</span></span> <span data-ttu-id="ce6c2-218">レコード区切りは outRecordDelimiter メソッドで定義されます。</span><span class="sxs-lookup"><span data-stu-id="ce6c2-218">The record separator is defined in the outRecordDelimiter method.</span></span>

## <a name="method-finalize"></a><span data-ttu-id="ce6c2-219">メソッド finalize</span><span class="sxs-lookup"><span data-stu-id="ce6c2-219">Method finalize</span></span>

<span data-ttu-id="ce6c2-220">ファイルを閉じ、データが書き込まれている場合、ファイル バッファーをディスクにフラッシュします。</span><span class="sxs-lookup"><span data-stu-id="ce6c2-220">Closes the file and, if data was written, flushes the file buffers to disk.</span></span>

```xpp
public void finalize()
```

### <a name="remarks---finalize"></a><span data-ttu-id="ce6c2-221">備考 - finalize</span><span class="sxs-lookup"><span data-stu-id="ce6c2-221">Remarks - finalize</span></span>

<span data-ttu-id="ce6c2-222">このメソッドは、通常は直接呼び出されません。</span><span class="sxs-lookup"><span data-stu-id="ce6c2-222">This method is not usually called directly.</span></span> <span data-ttu-id="ce6c2-223">代わりに、オブジェクトは通常、スコープを離れることによって確定されます。</span><span class="sxs-lookup"><span data-stu-id="ce6c2-223">Instead, the object is usually finalized by leaving the scope.</span></span> <span data-ttu-id="ce6c2-224">記述された出力はオブジェクトが終了するまで無効です。</span><span class="sxs-lookup"><span data-stu-id="ce6c2-224">Written output is not valid until the object is finalized.</span></span>

## <a name="method-new"></a><span data-ttu-id="ce6c2-225">メソッド new</span><span class="sxs-lookup"><span data-stu-id="ce6c2-225">Method new</span></span>

<span data-ttu-id="ce6c2-226">Object クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="ce6c2-226">Initializes a new instance of the Object class.</span></span>

```xpp
public void new(str filename, str mode, [int codepage])
```

### <a name="parameters---new"></a><span data-ttu-id="ce6c2-227">パラメーター - new</span><span class="sxs-lookup"><span data-stu-id="ce6c2-227">Parameters - new</span></span>

<span data-ttu-id="ce6c2-228">filename</span><span class="sxs-lookup"><span data-stu-id="ce6c2-228">filename</span></span>  

<!-- -->

<span data-ttu-id="ce6c2-229">モード</span><span class="sxs-lookup"><span data-stu-id="ce6c2-229">mode</span></span>  

<!-- -->

<span data-ttu-id="ce6c2-230">codepage</span><span class="sxs-lookup"><span data-stu-id="ce6c2-230">codepage</span></span>  

### <a name="remarks---new"></a><span data-ttu-id="ce6c2-231">備考 - new</span><span class="sxs-lookup"><span data-stu-id="ce6c2-231">Remarks - new</span></span>

<span data-ttu-id="ce6c2-232">攻撃者が新しいメソッドへの入力を制御できる場合、セキュリティ上のリスクが存在します。</span><span class="sxs-lookup"><span data-stu-id="ce6c2-232">If an attacker can control input to the new method, a security risk exists.</span></span> <span data-ttu-id="ce6c2-233">したがって、このメソッドは、コード アクセス セキュリティで実行されます。</span><span class="sxs-lookup"><span data-stu-id="ce6c2-233">Therefore, this method runs under Code Access Security.</span></span> <span data-ttu-id="ce6c2-234">サーバー上でこのメソッドを呼び出すには、FileIOPermission クラスからのアクセス許可が必要です。</span><span class="sxs-lookup"><span data-stu-id="ce6c2-234">Calls to this method on the server require permission from the FileIOPermission class.</span></span> <span data-ttu-id="ce6c2-235">ユーザーがこのメソッドを呼び出すコントロールで、SysDevelopment へのセキュリティ キーを設定して開発権限を持っていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="ce6c2-235">Make sure that the user has development privileges by setting the security key to SysDevelopment on the control that calls this method.</span></span>

