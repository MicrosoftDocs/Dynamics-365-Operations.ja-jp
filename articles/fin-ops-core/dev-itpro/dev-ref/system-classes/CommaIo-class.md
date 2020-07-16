---
title: CommaIo クラス
description: このトピックでは、CommaIo クラスについて説明します。
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
ms.openlocfilehash: 0b06da10de9d8e11e70e69b209ff5aa85b514f46
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502710"
---
# <a name="class-commaio"></a><span data-ttu-id="2fdec-103">クラス CommaIo</span><span class="sxs-lookup"><span data-stu-id="2fdec-103">Class CommaIo</span></span>

[!include [banner](../../includes/banner.md)]

```xpp
class CommaIo extends Io
```

<span data-ttu-id="2fdec-104">CommaIo クラスには、コンマ区切りファイルの読み取りと書き込みを行う機能があります。</span><span class="sxs-lookup"><span data-stu-id="2fdec-104">The CommaIo class provides functionality for reading and writing comma-separated files.</span></span>

## <a name="remarks"></a><span data-ttu-id="2fdec-105">備考</span><span class="sxs-lookup"><span data-stu-id="2fdec-105">Remarks</span></span>

<span data-ttu-id="2fdec-106">このクラスは、CommaTextIo クラスに置き換えられました。</span><span class="sxs-lookup"><span data-stu-id="2fdec-106">This class has been replaced by the CommaTextIo class.</span></span>

## <a name="examples"></a><span data-ttu-id="2fdec-107">例</span><span class="sxs-lookup"><span data-stu-id="2fdec-107">Examples</span></span>

## <a name="methods"></a><span data-ttu-id="2fdec-108">メソッド</span><span class="sxs-lookup"><span data-stu-id="2fdec-108">Methods</span></span>

| <span data-ttu-id="2fdec-109">方法</span><span class="sxs-lookup"><span data-stu-id="2fdec-109">Method</span></span>                                       | <span data-ttu-id="2fdec-110">説明</span><span class="sxs-lookup"><span data-stu-id="2fdec-110">Description</span></span>                                                                                                                  |
|----------------------------------------------|------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2fdec-111">public int filePosition()</span><span class="sxs-lookup"><span data-stu-id="2fdec-111">public int filePosition()</span></span>                    |                                                                                                                              |
| <span data-ttu-id="2fdec-112">public str inFieldDelimiter(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="2fdec-112">public str inFieldDelimiter(\[str value\])</span></span>   | <span data-ttu-id="2fdec-113">\*Io によってアクセスされるレコード内のフィールドを区切るために使用される区切り文字を決定します。</span><span class="sxs-lookup"><span data-stu-id="2fdec-113">Determines the delimiter used to separate fields in records accessed by the \*Io classes.</span></span>                                    |
| <span data-ttu-id="2fdec-114">public str inRecordDelimiter(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="2fdec-114">public str inRecordDelimiter(\[str value\])</span></span>  | <span data-ttu-id="2fdec-115">完全なレコードが読み込まれたかどうかを判断するために、\*Io クラスに検索する文字を決定します。</span><span class="sxs-lookup"><span data-stu-id="2fdec-115">Determines to the \*Io classes what character or characters to search for to determine whether a full record has been read.</span></span>  |
| <span data-ttu-id="2fdec-116">public int inRecordLength(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="2fdec-116">public int inRecordLength(\[int value\])</span></span>     | <span data-ttu-id="2fdec-117">ファイル内の各レコードを読み取る文字数を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="2fdec-117">Gets or sets the number of characters to read for each record in a file.</span></span>                                                     |
| <span data-ttu-id="2fdec-118">public str outFieldDelimiter(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="2fdec-118">public str outFieldDelimiter(\[str value\])</span></span>  | <span data-ttu-id="2fdec-119">レコードのフィールドを区切るために使用されるファイルに書き込まれる文字のシーケンスを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="2fdec-119">Gets or sets the sequence of characters that are written to a file that is used to separate the fields of a record.</span></span>          |
| <span data-ttu-id="2fdec-120">public str outRecordDelimiter(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="2fdec-120">public str outRecordDelimiter(\[str value\])</span></span> | <span data-ttu-id="2fdec-121">出力ファイルでレコードを区切る出力ファイルに書き込まれる文字のシーケンスを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="2fdec-121">Gets or sets the sequence of characters that is written to the output files, which separate the records in the output files.</span></span> |
| <span data-ttu-id="2fdec-122">public container read()</span><span class="sxs-lookup"><span data-stu-id="2fdec-122">public container read()</span></span>                      | <span data-ttu-id="2fdec-123">Io オブジェクトから次の完全なレコードを読み取ります。</span><span class="sxs-lookup"><span data-stu-id="2fdec-123">Reads the next full record from the Io object.</span></span>                                                                               |
| <span data-ttu-id="2fdec-124">public IO\_Status status()</span><span class="sxs-lookup"><span data-stu-id="2fdec-124">public IO\_Status status()</span></span>                   | <span data-ttu-id="2fdec-125">Io オブジェクトで実行された最後の操作のステータスを取得します。</span><span class="sxs-lookup"><span data-stu-id="2fdec-125">Retrieves the status of the last operation that was performed on the Io object.</span></span>                                              |
| <span data-ttu-id="2fdec-126">public boolean write(VarArg values)</span><span class="sxs-lookup"><span data-stu-id="2fdec-126">public boolean write(VarArg values)</span></span>          | <span data-ttu-id="2fdec-127">単純型の値を記述します。</span><span class="sxs-lookup"><span data-stu-id="2fdec-127">Writes values of a simple type.</span></span>                                                                                              |
| <span data-ttu-id="2fdec-128">public boolean writeExp(container data)</span><span class="sxs-lookup"><span data-stu-id="2fdec-128">public boolean writeExp(container data)</span></span>      | <span data-ttu-id="2fdec-129">コンテナのコンテンツをファイルに記述します。</span><span class="sxs-lookup"><span data-stu-id="2fdec-129">Writes the content of a container to a file.</span></span>                                                                                 |
| <span data-ttu-id="2fdec-130">public void new(str filename, str mode)</span><span class="sxs-lookup"><span data-stu-id="2fdec-130">public void new(str filename, str mode)</span></span>      | <span data-ttu-id="2fdec-131">CommaIo クラスの新しいオブジェクトを作成します。</span><span class="sxs-lookup"><span data-stu-id="2fdec-131">Creates a new object of the CommaIo class.</span></span>                                                                                   |
| <span data-ttu-id="2fdec-132">public void finalize()</span><span class="sxs-lookup"><span data-stu-id="2fdec-132">public void finalize()</span></span>                       | <span data-ttu-id="2fdec-133">ファイルを閉じ、データが書き込まれている場合、ファイル バッファーをディスクにフラッシュします。</span><span class="sxs-lookup"><span data-stu-id="2fdec-133">Closes the file and, if data was written, flushes the file buffers to disk.</span></span>                                                  |

## <a name="method-fileposition"></a><span data-ttu-id="2fdec-134">メソッド filePosition</span><span class="sxs-lookup"><span data-stu-id="2fdec-134">Method filePosition</span></span>

```xpp
public int filePosition()
```

### <a name="return-value---fileposition"></a><span data-ttu-id="2fdec-135">戻り値 - filePosition</span><span class="sxs-lookup"><span data-stu-id="2fdec-135">Return Value - filePosition</span></span>

## <a name="method-infielddelimiter"></a><span data-ttu-id="2fdec-136">メソッド inFieldDelimiter</span><span class="sxs-lookup"><span data-stu-id="2fdec-136">Method inFieldDelimiter</span></span>

<span data-ttu-id="2fdec-137">\*Io によってアクセスされるレコード内のフィールドを区切るために使用される区切り文字を決定します。</span><span class="sxs-lookup"><span data-stu-id="2fdec-137">Determines the delimiter used to separate fields in records accessed by the \*Io classes.</span></span>

```xpp
public str inFieldDelimiter([str value])
```

### <a name="parameters---infielddelimiter"></a><span data-ttu-id="2fdec-138">パラメーター - inFieldDelimiter</span><span class="sxs-lookup"><span data-stu-id="2fdec-138">Parameters - inFieldDelimiter</span></span>

<span data-ttu-id="2fdec-139">値</span><span class="sxs-lookup"><span data-stu-id="2fdec-139">value</span></span>  

### <a name="return-value---infielddelimiter"></a><span data-ttu-id="2fdec-140">戻り値 - inFieldDelimiter</span><span class="sxs-lookup"><span data-stu-id="2fdec-140">Return Value - inFieldDelimiter</span></span>

<span data-ttu-id="2fdec-141">\*Io によってアクセスされるレコード内のフィールドを区切るために使用される区切り文字。</span><span class="sxs-lookup"><span data-stu-id="2fdec-141">The delimiter used to separate fields in records accessed by the \*Io classes.</span></span>

## <a name="method-inrecorddelimiter"></a><span data-ttu-id="2fdec-142">メソッド inRecordDelimiter</span><span class="sxs-lookup"><span data-stu-id="2fdec-142">Method inRecordDelimiter</span></span>

<span data-ttu-id="2fdec-143">完全なレコードが読み込まれたかどうかを判断するために、\*Io クラスに検索する文字を決定します。</span><span class="sxs-lookup"><span data-stu-id="2fdec-143">Determines to the \*Io classes what character or characters to search for to determine whether a full record has been read.</span></span>

```xpp
public str inRecordDelimiter([str value])
```

### <a name="parameters---inrecorddelimiter"></a><span data-ttu-id="2fdec-144">パラメーター - inRecordDelimiter</span><span class="sxs-lookup"><span data-stu-id="2fdec-144">Parameters - inRecordDelimiter</span></span>

<span data-ttu-id="2fdec-145">値</span><span class="sxs-lookup"><span data-stu-id="2fdec-145">value</span></span>  

### <a name="return-value---inrecorddelimiter"></a><span data-ttu-id="2fdec-146">戻り値 - inRecordDelimiter</span><span class="sxs-lookup"><span data-stu-id="2fdec-146">Return Value - inRecordDelimiter</span></span>

<span data-ttu-id="2fdec-147">完全なレコードが読み込まれたかどうかを示す文字。</span><span class="sxs-lookup"><span data-stu-id="2fdec-147">The character or characters that indicate whether a full record has been read.</span></span>

### <a name="remarks---inrecorddelimiter"></a><span data-ttu-id="2fdec-148">備考 - inRecordDelimiter</span><span class="sxs-lookup"><span data-stu-id="2fdec-148">Remarks - inRecordDelimiter</span></span>

<span data-ttu-id="2fdec-149">標準的なテキストについては、区切り記号は改行文字です。</span><span class="sxs-lookup"><span data-stu-id="2fdec-149">For standard text, the delimiter is a newline character.</span></span>

## <a name="method-inrecordlength"></a><span data-ttu-id="2fdec-150">メソッド inRecordLength</span><span class="sxs-lookup"><span data-stu-id="2fdec-150">Method inRecordLength</span></span>

<span data-ttu-id="2fdec-151">ファイル内の各レコードを読み取る文字数を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="2fdec-151">Gets or sets the number of characters to read for each record in a file.</span></span>

```xpp
public int inRecordLength([int value])
```

### <a name="parameters---inrecordlength"></a><span data-ttu-id="2fdec-152">パラメーター - inRecordLength</span><span class="sxs-lookup"><span data-stu-id="2fdec-152">Parameters - inRecordLength</span></span>

<span data-ttu-id="2fdec-153">値</span><span class="sxs-lookup"><span data-stu-id="2fdec-153">value</span></span>  

### <a name="return-value---inrecordlength"></a><span data-ttu-id="2fdec-154">戻り値 - inRecordLength</span><span class="sxs-lookup"><span data-stu-id="2fdec-154">Return Value - inRecordLength</span></span>

<span data-ttu-id="2fdec-155">ファイル内の各レコードを読み取る文字数。</span><span class="sxs-lookup"><span data-stu-id="2fdec-155">The number of characters to read for each record in the file.</span></span>

### <a name="remarks---inrecordlength"></a><span data-ttu-id="2fdec-156">備考 - inRecordLength</span><span class="sxs-lookup"><span data-stu-id="2fdec-156">Remarks - inRecordLength</span></span>

<span data-ttu-id="2fdec-157">固定長形式になっているファイルについては、inRecordLength プロパティを使用して、各レコードに対して指定された文字数以上が読み取られていないことを保証します。</span><span class="sxs-lookup"><span data-stu-id="2fdec-157">For files that have a fixed-length format, use the inRecordLength property to guarantee that no more than the specified number of characters are read for each record.</span></span> <span data-ttu-id="2fdec-158">レコード フォーマットが指定された inRecordDelimiter プロパティ値で上書きされた場合、つまり、固定長が読み込まれる前に inRecordDelimiter 値が満たされている場合)、レコードは受け入れられ、追加のデータは読み込まれません。</span><span class="sxs-lookup"><span data-stu-id="2fdec-158">If the record format is overruled by a specified inRecordDelimiter property value , that is the inRecordDelimiter value is met before the fixed length is read, the record is accepted, and no additional data is read.</span></span> <span data-ttu-id="2fdec-159">固定数の文字を確実に読み取るには、inRecordDelimiter プロパティ値を空の文字列に設定します。</span><span class="sxs-lookup"><span data-stu-id="2fdec-159">To ensure that a fixed number of characters are read, set the inRecordDelimiter property value to an empty string.</span></span> <span data-ttu-id="2fdec-160">inRecordDelimiter プロパティ値が見つからない場合、inRecordDelimiter プロパティ値は読み取れる最大文字数になります。</span><span class="sxs-lookup"><span data-stu-id="2fdec-160">When no inRecordDelimiter property value is found, the inRecordDelimiter property value is the maximum limit of characters to read.</span></span> <span data-ttu-id="2fdec-161">レコードの長さチェックを無効にするには、inRecordDelimiter プロパティ値をゼロに設定します。</span><span class="sxs-lookup"><span data-stu-id="2fdec-161">Set the inRecordDelimiter property value to zero to disable the record length check.</span></span>

## <a name="method-outfielddelimiter"></a><span data-ttu-id="2fdec-162">メソッド outFieldDelimiter</span><span class="sxs-lookup"><span data-stu-id="2fdec-162">Method outFieldDelimiter</span></span>

<span data-ttu-id="2fdec-163">レコードのフィールドを区切るために使用されるファイルに書き込まれる文字のシーケンスを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="2fdec-163">Gets or sets the sequence of characters that are written to a file that is used to separate the fields of a record.</span></span>

```xpp
public str outFieldDelimiter([str value])
```

### <a name="parameters---outfielddelimiter"></a><span data-ttu-id="2fdec-164">パラメーター - outFieldDelimiter</span><span class="sxs-lookup"><span data-stu-id="2fdec-164">Parameters - outFieldDelimiter</span></span>

<span data-ttu-id="2fdec-165">値</span><span class="sxs-lookup"><span data-stu-id="2fdec-165">value</span></span>  

### <a name="return-value---outfielddelimiter"></a><span data-ttu-id="2fdec-166">戻り値 - outFieldDelimiter</span><span class="sxs-lookup"><span data-stu-id="2fdec-166">Return Value - outFieldDelimiter</span></span>

<span data-ttu-id="2fdec-167">レコードのフィールドを区切るために使用されるファイルに書き込まれる文字のシーケンス。</span><span class="sxs-lookup"><span data-stu-id="2fdec-167">The sequence of characters that are written to a file that is used to separate the fields of a record.</span></span>

## <a name="method-outrecorddelimiter"></a><span data-ttu-id="2fdec-168">メソッド outRecordDelimiter</span><span class="sxs-lookup"><span data-stu-id="2fdec-168">Method outRecordDelimiter</span></span>

<span data-ttu-id="2fdec-169">出力ファイルでレコードを区切る出力ファイルに書き込まれる文字のシーケンスを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="2fdec-169">Gets or sets the sequence of characters that is written to the output files, which separate the records in the output files.</span></span>

```xpp
public str outRecordDelimiter([str value])
```

### <a name="parameters---outrecorddelimiter"></a><span data-ttu-id="2fdec-170">パラメーター - outRecordDelimiter</span><span class="sxs-lookup"><span data-stu-id="2fdec-170">Parameters - outRecordDelimiter</span></span>

<span data-ttu-id="2fdec-171">値</span><span class="sxs-lookup"><span data-stu-id="2fdec-171">value</span></span>  

### <a name="return-value---outrecorddelimiter"></a><span data-ttu-id="2fdec-172">戻り値 - outRecordDelimiter</span><span class="sxs-lookup"><span data-stu-id="2fdec-172">Return Value - outRecordDelimiter</span></span>

<span data-ttu-id="2fdec-173">出力ファイルに書き込まれる文字のシーケンス。</span><span class="sxs-lookup"><span data-stu-id="2fdec-173">The sequence of characters that is written to the output files.</span></span>

### <a name="remarks---outrecorddelimiter"></a><span data-ttu-id="2fdec-174">備考 - outRecordDelimiter</span><span class="sxs-lookup"><span data-stu-id="2fdec-174">Remarks - outRecordDelimiter</span></span>

<span data-ttu-id="2fdec-175">標準的なテキスト ファイルについては、区切り記号は改行文字です。</span><span class="sxs-lookup"><span data-stu-id="2fdec-175">For standard text files, the delimiter is a newline character.</span></span>

## <a name="method-read"></a><span data-ttu-id="2fdec-176">メソッド read</span><span class="sxs-lookup"><span data-stu-id="2fdec-176">Method read</span></span>

<span data-ttu-id="2fdec-177">Io オブジェクトから次の完全なレコードを読み取ります。</span><span class="sxs-lookup"><span data-stu-id="2fdec-177">Reads the next full record from the Io object.</span></span>

```xpp
public container read()
```

### <a name="return-value---read"></a><span data-ttu-id="2fdec-178">戻り値 - read</span><span class="sxs-lookup"><span data-stu-id="2fdec-178">Return Value - read</span></span>

<span data-ttu-id="2fdec-179">Io オブジェクトからの次の完全なレコード。</span><span class="sxs-lookup"><span data-stu-id="2fdec-179">The next full record from the Io object.</span></span>

### <a name="remarks---read"></a><span data-ttu-id="2fdec-180">備考 - read</span><span class="sxs-lookup"><span data-stu-id="2fdec-180">Remarks - read</span></span>

<span data-ttu-id="2fdec-181">次の完全なレコードの定義は、次のプロパティ、inFieldDelimiter、inRecordDelimiter、および inRecordLength プロパティによって制御されます。</span><span class="sxs-lookup"><span data-stu-id="2fdec-181">The definition of the next full record is controlled by the inFieldDelimiter, inRecordDelimiter, and inRecordLength properties.</span></span> <span data-ttu-id="2fdec-182">レコードはコンテナーとして返されます。</span><span class="sxs-lookup"><span data-stu-id="2fdec-182">The record is returned as a container.</span></span> <span data-ttu-id="2fdec-183">コンテナー内の各エントリは、レコードの 1 つのフィールドと同じです。</span><span class="sxs-lookup"><span data-stu-id="2fdec-183">Each entry in the container equals one field in the record.</span></span> <span data-ttu-id="2fdec-184">それぞれの特殊な Io クラスでは、inFieldDelimiter、inRecordDelimiter、および inRecordLength のプロパティのデフォルト設定を使用し、最も一般的な形式の入出力を有効にします。</span><span class="sxs-lookup"><span data-stu-id="2fdec-184">Each specialized Io class has default settings for the inFieldDelimiter, inRecordDelimiter, and inRecordLength properties to enable input and output in the most common formats.</span></span> <span data-ttu-id="2fdec-185">ただし、目的の形式をサポートするために、これらの設定の調整が生じる場合があります。</span><span class="sxs-lookup"><span data-stu-id="2fdec-185">However, you might have to adjust these settings to support the desired format.</span></span>

## <a name="method-status"></a><span data-ttu-id="2fdec-186">メソッド status</span><span class="sxs-lookup"><span data-stu-id="2fdec-186">Method status</span></span>

<span data-ttu-id="2fdec-187">Io オブジェクトで実行された最後の操作のステータスを取得します。</span><span class="sxs-lookup"><span data-stu-id="2fdec-187">Retrieves the status of the last operation that was performed on the Io object.</span></span>

```xpp
public IO_Status status()
```

### <a name="return-value---status"></a><span data-ttu-id="2fdec-188">戻り値 - status</span><span class="sxs-lookup"><span data-stu-id="2fdec-188">Return Value - status</span></span>

<span data-ttu-id="2fdec-189">最後の操作の状態。システム列挙形式。</span><span class="sxs-lookup"><span data-stu-id="2fdec-189">The status of the last operation, in the form of a system enumeration.</span></span>

### <a name="remarks---status"></a><span data-ttu-id="2fdec-190">備考 - status</span><span class="sxs-lookup"><span data-stu-id="2fdec-190">Remarks - status</span></span>

<span data-ttu-id="2fdec-191">戻り値は、IO\_ステータス システムの列挙によって表されます。</span><span class="sxs-lookup"><span data-stu-id="2fdec-191">The return value is represented by the IO\_Status system enumeration.</span></span> <span data-ttu-id="2fdec-192">可能性のある IO\_Status 値の範囲はクラスによって異なります。</span><span class="sxs-lookup"><span data-stu-id="2fdec-192">The range of possible IO\_Status values varies among Io classes.</span></span>

### <a name="examples---status"></a><span data-ttu-id="2fdec-193">例 - status</span><span class="sxs-lookup"><span data-stu-id="2fdec-193">Examples - status</span></span>

<span data-ttu-id="2fdec-194">この例は、状態メソッドを使用する方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="2fdec-194">This example shows how to use the status method.</span></span> <span data-ttu-id="2fdec-195">ただし、この例は、クラス、フォーム、またはその他のオブジェクトのコンテキストで実行される必要があるため、ジョブはコンパイルされません。</span><span class="sxs-lookup"><span data-stu-id="2fdec-195">However, this example will not compile in a job, because it must be run in the context of a class, form, or other object.</span></span>

```xpp
{ 
    // Create an Io object and perform some operations. 
    if (myIo.status() == IO_Status::OK) 
    { 
        // Go ahead - the last operation was successful. 
    } 
}
```

## <a name="method-write"></a><span data-ttu-id="2fdec-196">メソッド write</span><span class="sxs-lookup"><span data-stu-id="2fdec-196">Method write</span></span>

<span data-ttu-id="2fdec-197">単純型の値を記述します。</span><span class="sxs-lookup"><span data-stu-id="2fdec-197">Writes values of a simple type.</span></span>

```xpp
public boolean write(VarArg values)
```

### <a name="parameters---write"></a><span data-ttu-id="2fdec-198">パラメーター - write</span><span class="sxs-lookup"><span data-stu-id="2fdec-198">Parameters - write</span></span>

<span data-ttu-id="2fdec-199">値</span><span class="sxs-lookup"><span data-stu-id="2fdec-199">values</span></span>  
<span data-ttu-id="2fdec-200">1 つ以上の値の、各単純型は、フィールドの区切り記号で区切られています。</span><span class="sxs-lookup"><span data-stu-id="2fdec-200">One or more values, each of a simple type, separated by a field delimiter.</span></span> <span data-ttu-id="2fdec-201">単純型は、文字列、整数、実数、列挙型、日付です。</span><span class="sxs-lookup"><span data-stu-id="2fdec-201">The simple types are string, integer, real, enum, and date.</span></span>

### <a name="return-value---write"></a><span data-ttu-id="2fdec-202">戻り値 - write</span><span class="sxs-lookup"><span data-stu-id="2fdec-202">Return Value - write</span></span>

<span data-ttu-id="2fdec-203">書き込み操作が成功する場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="2fdec-203">true if the write operation succeeds; otherwise, false.</span></span> <span data-ttu-id="2fdec-204">工程が失敗すると、ステータスをチェックし障害について確認できます。</span><span class="sxs-lookup"><span data-stu-id="2fdec-204">If the operation fails, you can check the status to learn the cause of the failure.</span></span>

### <a name="remarks---write"></a><span data-ttu-id="2fdec-205">備考 - write</span><span class="sxs-lookup"><span data-stu-id="2fdec-205">Remarks - write</span></span>

<span data-ttu-id="2fdec-206">このメソッドは、可変数の引数を受け入れます。</span><span class="sxs-lookup"><span data-stu-id="2fdec-206">The method accepts a variable number of arguments.</span></span> <span data-ttu-id="2fdec-207">指定された各値は、フィールドとして出力レコードに配置されます。</span><span class="sxs-lookup"><span data-stu-id="2fdec-207">Each value that is specified is put into the output record as a field.</span></span> <span data-ttu-id="2fdec-208">最初の引数は最初のフィールドになり、2 番目の引数は 2 番目のフィールドなどになります。</span><span class="sxs-lookup"><span data-stu-id="2fdec-208">The first argument becomes the first field, the second argument becomes the second field, and so on.</span></span> <span data-ttu-id="2fdec-209">フィールドは、outFieldDelimiter メソッドで指定されるフィールド区切り記号で区切られます。</span><span class="sxs-lookup"><span data-stu-id="2fdec-209">Fields are separated by the field delimiter that is specified in the outFieldDelimiter method.</span></span> <span data-ttu-id="2fdec-210">レコードは、outRecordDelimiter メソッドを使用して指定される区切り記号で区切られます。</span><span class="sxs-lookup"><span data-stu-id="2fdec-210">Records are separated by the delimiter that is specified by using the outRecordDelimiter method.</span></span> <span data-ttu-id="2fdec-211">完全なコンテナーを書き込むには、writeExp メソッドを使用します。</span><span class="sxs-lookup"><span data-stu-id="2fdec-211">To write complete containers, use the writeExp method.</span></span>

## <a name="method-writeexp"></a><span data-ttu-id="2fdec-212">メソッド writeExp</span><span class="sxs-lookup"><span data-stu-id="2fdec-212">Method writeExp</span></span>

<span data-ttu-id="2fdec-213">コンテナのコンテンツをファイルに記述します。</span><span class="sxs-lookup"><span data-stu-id="2fdec-213">Writes the content of a container to a file.</span></span>

```xpp
public boolean writeExp(container data)
```

### <a name="parameters---writeexp"></a><span data-ttu-id="2fdec-214">パラメーター - writeExp</span><span class="sxs-lookup"><span data-stu-id="2fdec-214">Parameters - writeExp</span></span>

<span data-ttu-id="2fdec-215">データ</span><span class="sxs-lookup"><span data-stu-id="2fdec-215">data</span></span>  
<span data-ttu-id="2fdec-216">レコードのデータを保持するコンテナー。</span><span class="sxs-lookup"><span data-stu-id="2fdec-216">The container that holds data for the record.</span></span>

### <a name="return-value---writeexp"></a><span data-ttu-id="2fdec-217">戻り値 - writeExp</span><span class="sxs-lookup"><span data-stu-id="2fdec-217">Return Value - writeExp</span></span>

<span data-ttu-id="2fdec-218">操作が成功する場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="2fdec-218">true if the operation succeeds; otherwise, false.</span></span> <span data-ttu-id="2fdec-219">工程が失敗すると、ステータスをチェックし障害について確認できます。</span><span class="sxs-lookup"><span data-stu-id="2fdec-219">If the operation fails, you can check the status to learn the cause of the failure.</span></span>

### <a name="remarks---writeexp"></a><span data-ttu-id="2fdec-220">備考 - writeExp</span><span class="sxs-lookup"><span data-stu-id="2fdec-220">Remarks - writeExp</span></span>

<span data-ttu-id="2fdec-221">コンテナー内のエントリはフィールドとして扱われます。</span><span class="sxs-lookup"><span data-stu-id="2fdec-221">The entries in the container are treated as fields.</span></span> <span data-ttu-id="2fdec-222">コンテナー自体は、完全なレコードとして扱われます。</span><span class="sxs-lookup"><span data-stu-id="2fdec-222">The container itself is treated as a full record.</span></span> <span data-ttu-id="2fdec-223">フィールドは、outFieldDelimiter メソッドを使用して指定される区切り記号で区切られます。</span><span class="sxs-lookup"><span data-stu-id="2fdec-223">Fields are separated by the delimiter that is specified by using the outFieldDelimiter method.</span></span> <span data-ttu-id="2fdec-224">レコードは、outRecordDelimiter メソッドを使用して指定される区切り記号で区切られます。</span><span class="sxs-lookup"><span data-stu-id="2fdec-224">Records are separated by the delimiter that is specified by using the outRecordDelimiter method.</span></span>

### <a name="examples---writeexp"></a><span data-ttu-id="2fdec-225">例 - writeExp</span><span class="sxs-lookup"><span data-stu-id="2fdec-225">Examples - writeExp</span></span>

<span data-ttu-id="2fdec-226">この例では、CommaIO オブジェクトを使用してサンプル ファイルから読み取ります。</span><span class="sxs-lookup"><span data-stu-id="2fdec-226">This example uses a CommaIO object to read from the example file.</span></span>

```xpp
{ 
    container c; 
    CommaIo myfile; 
    FileIoPermission perm; 
```

```xpp
    #define.ExampleFile(@"c:\myfile.txt") 
    #define.ExampleOpenMode("w") 
```

```xpp
    // Set code access permission to help protect the use 
    // of CommaIO.new 
    perm = new FileIoPermission(#ExampleFile, #ExampleOpenMode); 
    perm.assert(); 
```

```xpp
    myfile = new CommaIo(#ExampleFile, #ExampleOpenMode); 
```

```xpp
    // Assign the entries in the container according to record layout. 
    c = [1,"MyText",1.324,"Last field"]; 
    // Write this record according to file format  
    // (record/field delimiters). 
    myfile.writeExp(c); 
```

```xpp
    // Close the code access permission. 
    CodeAccessPermission::revertAssert(); 
}
```

## <a name="method-new"></a><span data-ttu-id="2fdec-227">メソッド new</span><span class="sxs-lookup"><span data-stu-id="2fdec-227">Method new</span></span>

<span data-ttu-id="2fdec-228">CommaIo クラスの新しいオブジェクトを作成します。</span><span class="sxs-lookup"><span data-stu-id="2fdec-228">Creates a new object of the CommaIo class.</span></span>

```xpp
public void new(str filename, str mode)
```

### <a name="parameters---new"></a><span data-ttu-id="2fdec-229">パラメーター - new</span><span class="sxs-lookup"><span data-stu-id="2fdec-229">Parameters - new</span></span>

<span data-ttu-id="2fdec-230">filename</span><span class="sxs-lookup"><span data-stu-id="2fdec-230">filename</span></span>  
<span data-ttu-id="2fdec-231">ファイルを開く必要があるモード。</span><span class="sxs-lookup"><span data-stu-id="2fdec-231">The mode that the file should be opened in.</span></span> <span data-ttu-id="2fdec-232">次のようにモードを指定します。</span><span class="sxs-lookup"><span data-stu-id="2fdec-232">Specify the mode as follows:</span></span>

<!-- -->

<span data-ttu-id="2fdec-233">モード</span><span class="sxs-lookup"><span data-stu-id="2fdec-233">mode</span></span>  
<span data-ttu-id="2fdec-234">ファイルを開く必要があるモード。</span><span class="sxs-lookup"><span data-stu-id="2fdec-234">The mode that the file should be opened in.</span></span> <span data-ttu-id="2fdec-235">次のようにモードを指定します。</span><span class="sxs-lookup"><span data-stu-id="2fdec-235">Specify the mode as follows:</span></span>

### <a name="remarks---new"></a><span data-ttu-id="2fdec-236">備考 - new</span><span class="sxs-lookup"><span data-stu-id="2fdec-236">Remarks - new</span></span>

<span data-ttu-id="2fdec-237">ランタイム エラーは、現在のモードに対応していないメソッドを使用してファイルにアクセスした場合に発生します。</span><span class="sxs-lookup"><span data-stu-id="2fdec-237">A run-time error occurs if the file is accessed by using a method that does not correspond to the current mode.</span></span> <span data-ttu-id="2fdec-238">たとえば、ユーザーが読み取りモードで開いているファイルへの書き込みしようとすると、エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="2fdec-238">For example, an error occurs if a user tries to write to a file that is opened in read mode.</span></span> <span data-ttu-id="2fdec-239">攻撃者がこのメソッドへの入力を制御できる場合、セキュリティ上のリスクが存在します。</span><span class="sxs-lookup"><span data-stu-id="2fdec-239">If an attacker can control input to this method, a security risk exists.</span></span> <span data-ttu-id="2fdec-240">したがって、このメソッドは、コード アクセス セキュリティで実行されます。</span><span class="sxs-lookup"><span data-stu-id="2fdec-240">Therefore, this method runs under Code Access Security.</span></span> <span data-ttu-id="2fdec-241">サーバー上でこのメソッドを呼び出すには、FileIOPermission クラスからのアクセス許可が必要です。</span><span class="sxs-lookup"><span data-stu-id="2fdec-241">Calls to this method on the server require permission from the FileIOPermission class.</span></span> <span data-ttu-id="2fdec-242">ユーザーがこのメソッドを呼び出すコントロールで、SysDevelopment へのセキュリティ キーを設定して開発権限を持っていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="2fdec-242">Make sure that the user has development privileges by setting the security key to SysDevelopment on the control that calls this method.</span></span>

### <a name="examples---new"></a><span data-ttu-id="2fdec-243">例 - new</span><span class="sxs-lookup"><span data-stu-id="2fdec-243">Examples - new</span></span>

<span data-ttu-id="2fdec-244">次の例では、CommaIO オブジェクトを使用して ExampleFile ファイルから読み取ります。</span><span class="sxs-lookup"><span data-stu-id="2fdec-244">The following example uses a CommaIO object to read from the ExampleFile file.</span></span>

```xpp
{ 
    CommaIo         io; 
    container       con; 
    FileIoPermission perm; 
```

```xpp
    #define.ExampleFile(@"c:\test.txt") 
    #define.ExampleOpenMode("r") 
```

```xpp
    perm = new FileIoPermission(#ExampleFile, #ExampleOpenMode); 
    if (perm == null) 
    { 
        return; 
    } 
    // Grants permission to execute the CommaIo.new method. 
    // CommaIo.new runs under code access security. 
    perm.assert(); 
```

```xpp
    io = new CommaIo(#ExampleFile, #ExampleOpenMode); 
    if (io != null) 
    { 
        con = io.read(); 
    } 
```

```xpp
    // Close the code access permission scope. 
    CodeAccessPermission::revertAssert(); 
}
```

## <a name="method-finalize"></a><span data-ttu-id="2fdec-245">メソッド finalize</span><span class="sxs-lookup"><span data-stu-id="2fdec-245">Method finalize</span></span>

<span data-ttu-id="2fdec-246">ファイルを閉じ、データが書き込まれている場合、ファイル バッファーをディスクにフラッシュします。</span><span class="sxs-lookup"><span data-stu-id="2fdec-246">Closes the file and, if data was written, flushes the file buffers to disk.</span></span>

```xpp
public void finalize()
```

### <a name="remarks---finalize"></a><span data-ttu-id="2fdec-247">備考 - finalize</span><span class="sxs-lookup"><span data-stu-id="2fdec-247">Remarks - finalize</span></span>

<span data-ttu-id="2fdec-248">このメソッドは通常は直接呼び出されません。代わりに、オブジェクトはスコープを離れることによって確定されます。</span><span class="sxs-lookup"><span data-stu-id="2fdec-248">This method is not usually called directly; instead, the object is finalized by leaving the scope.</span></span> <span data-ttu-id="2fdec-249">記述された出力はオブジェクトが終了するまで無効です。</span><span class="sxs-lookup"><span data-stu-id="2fdec-249">The written output is not valid until the object is finalized.</span></span>

