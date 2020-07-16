---
title: Io クラス
description: このトピックでは、Io クラスについて説明します。
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
ms.openlocfilehash: 439fe4d333ee6f0b04b20404eccae7d9f11a9182
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502896"
---
# <a name="class-io"></a><span data-ttu-id="6a2e9-103">クラス入出力</span><span class="sxs-lookup"><span data-stu-id="6a2e9-103">Class Io</span></span>

[!include [banner](../../includes/banner.md)]

```xpp
class Io extends Object
```

<span data-ttu-id="6a2e9-104">Io クラスは、外部ファイルにアクセスするための、ファイル固有の Io クラスの基本クラスとして機能します。</span><span class="sxs-lookup"><span data-stu-id="6a2e9-104">The Io class serves as the base class for the format-specific Io classes, which are used to access external files.</span></span>

## <a name="remarks"></a><span data-ttu-id="6a2e9-105">備考</span><span class="sxs-lookup"><span data-stu-id="6a2e9-105">Remarks</span></span>

<span data-ttu-id="6a2e9-106">基本的な Io クラスには、実際のデータ入出力機能はありませんが、形式固有の Io クラスの基本クラスとして動作します。</span><span class="sxs-lookup"><span data-stu-id="6a2e9-106">The basic Io class features no actual data I/O but works as base class for the format-specific Io classes.</span></span> <span data-ttu-id="6a2e9-107">ここでは、すべての Io クラスに共通するメソッドについて説明します。</span><span class="sxs-lookup"><span data-stu-id="6a2e9-107">The methods that are common to all Io classes are described here.</span></span> <span data-ttu-id="6a2e9-108">形式固有の機能およびメンバー機能の動作については、各 I/O クラスのドキュメントを参照してください。</span><span class="sxs-lookup"><span data-stu-id="6a2e9-108">For format-specific features and behavior of the member functions, refer to the documentation for each of the I/O classes.</span></span> <span data-ttu-id="6a2e9-109">異なるフォーマットの外部ファイルの読み書きをサポートするため、MorphX はコンマで区切られたファイル、コンマで区切られた 7 ビット ファイル、バイナリ ファイル、およびプレーン テキスト ファイルのためのさまざまな Io クラスを備えています。</span><span class="sxs-lookup"><span data-stu-id="6a2e9-109">To support reading and writing of different formats of external files, MorphX features a range of different Io classes for comma-separated files, for comma-separated 7 bit files, for binary files, and for plain-text files.</span></span>

## <a name="examples"></a><span data-ttu-id="6a2e9-110">例</span><span class="sxs-lookup"><span data-stu-id="6a2e9-110">Examples</span></span>

## <a name="methods"></a><span data-ttu-id="6a2e9-111">メソッド</span><span class="sxs-lookup"><span data-stu-id="6a2e9-111">Methods</span></span>

| <span data-ttu-id="6a2e9-112">方法</span><span class="sxs-lookup"><span data-stu-id="6a2e9-112">Method</span></span>                                       | <span data-ttu-id="6a2e9-113">説明</span><span class="sxs-lookup"><span data-stu-id="6a2e9-113">Description</span></span>                                                                                                                  |
|----------------------------------------------|------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6a2e9-114">public str inFieldDelimiter(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="6a2e9-114">public str inFieldDelimiter(\[str value\])</span></span>   | <span data-ttu-id="6a2e9-115">\*Io によってアクセスされるレコード内のフィールドを区切るために使用される区切り文字を決定します。</span><span class="sxs-lookup"><span data-stu-id="6a2e9-115">Determines the delimiter used to separate fields in records accessed by the \*Io classes.</span></span>                                    |
| <span data-ttu-id="6a2e9-116">public str inRecordDelimiter(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="6a2e9-116">public str inRecordDelimiter(\[str value\])</span></span>  | <span data-ttu-id="6a2e9-117">完全なレコードが読み込まれたかどうかを判断するために、\*Io クラスに検索する文字を決定します。</span><span class="sxs-lookup"><span data-stu-id="6a2e9-117">Determines to the \*Io classes what character or characters to search for to determine whether a full record has been read.</span></span>  |
| <span data-ttu-id="6a2e9-118">public int inRecordLength(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="6a2e9-118">public int inRecordLength(\[int value\])</span></span>     | <span data-ttu-id="6a2e9-119">ファイル内の各レコードを読み取る文字数を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="6a2e9-119">Gets or sets the number of characters to read for each record in a file.</span></span>                                                     |
| <span data-ttu-id="6a2e9-120">public str outFieldDelimiter(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="6a2e9-120">public str outFieldDelimiter(\[str value\])</span></span>  | <span data-ttu-id="6a2e9-121">レコードのフィールドを区切るために使用されるファイルに書き込まれる文字のシーケンスを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="6a2e9-121">Gets or sets the sequence of characters that are written to a file that is used to separate the fields of a record.</span></span>          |
| <span data-ttu-id="6a2e9-122">public str outRecordDelimiter(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="6a2e9-122">public str outRecordDelimiter(\[str value\])</span></span> | <span data-ttu-id="6a2e9-123">出力ファイルでレコードを区切る出力ファイルに書き込まれる文字のシーケンスを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="6a2e9-123">Gets or sets the sequence of characters that is written to the output files, which separate the records in the output files.</span></span> |
| <span data-ttu-id="6a2e9-124">public container read()</span><span class="sxs-lookup"><span data-stu-id="6a2e9-124">public container read()</span></span>                      | <span data-ttu-id="6a2e9-125">Io オブジェクトから次の完全なレコードを読み取ります。</span><span class="sxs-lookup"><span data-stu-id="6a2e9-125">Reads the next full record from the Io object.</span></span>                                                                               |
| <span data-ttu-id="6a2e9-126">public IO\_Status status()</span><span class="sxs-lookup"><span data-stu-id="6a2e9-126">public IO\_Status status()</span></span>                   | <span data-ttu-id="6a2e9-127">Io オブジェクトで実行された最後の操作のステータスを取得します。</span><span class="sxs-lookup"><span data-stu-id="6a2e9-127">Retrieves the status of the last operation performed on the Io object.</span></span>                                                       |
| <span data-ttu-id="6a2e9-128">public boolean write(VarArg values)</span><span class="sxs-lookup"><span data-stu-id="6a2e9-128">public boolean write(VarArg values)</span></span>          | <span data-ttu-id="6a2e9-129">単純型の値を記述します。</span><span class="sxs-lookup"><span data-stu-id="6a2e9-129">Writes values of a simple type.</span></span>                                                                                              |
| <span data-ttu-id="6a2e9-130">public boolean writeExp(container data)</span><span class="sxs-lookup"><span data-stu-id="6a2e9-130">public boolean writeExp(container data)</span></span>      | <span data-ttu-id="6a2e9-131">コンテナのコンテンツをそのファイルに記述します。</span><span class="sxs-lookup"><span data-stu-id="6a2e9-131">Writes the content of a container to the file.</span></span>                                                                               |
| <span data-ttu-id="6a2e9-132">public void finalize()</span><span class="sxs-lookup"><span data-stu-id="6a2e9-132">public void finalize()</span></span>                       | <span data-ttu-id="6a2e9-133">ファイルを閉じ、データが書き込まれている場合、ファイル バッファーをディスクにフラッシュします。</span><span class="sxs-lookup"><span data-stu-id="6a2e9-133">Closes the file and, if data was written, flushes the file buffers to disk.</span></span>                                                  |
| <span data-ttu-id="6a2e9-134">public void new(str filename, str mode)</span><span class="sxs-lookup"><span data-stu-id="6a2e9-134">public void new(str filename, str mode)</span></span>      | <span data-ttu-id="6a2e9-135">Io クラスの新しいインスタンスを作成します。</span><span class="sxs-lookup"><span data-stu-id="6a2e9-135">Creates a new instance of the Io class.</span></span>                                                                                      |

## <a name="method-infielddelimiter"></a><span data-ttu-id="6a2e9-136">メソッド inFieldDelimiter</span><span class="sxs-lookup"><span data-stu-id="6a2e9-136">Method inFieldDelimiter</span></span>

<span data-ttu-id="6a2e9-137">\*Io によってアクセスされるレコード内のフィールドを区切るために使用される区切り文字を決定します。</span><span class="sxs-lookup"><span data-stu-id="6a2e9-137">Determines the delimiter used to separate fields in records accessed by the \*Io classes.</span></span>

```xpp
public str inFieldDelimiter([str value])
```

### <a name="parameters---infielddelimiter"></a><span data-ttu-id="6a2e9-138">パラメーター - inFieldDelimiter</span><span class="sxs-lookup"><span data-stu-id="6a2e9-138">Parameters - inFieldDelimiter</span></span>

<span data-ttu-id="6a2e9-139">値</span><span class="sxs-lookup"><span data-stu-id="6a2e9-139">value</span></span>  

### <a name="return-value---infielddelimiter"></a><span data-ttu-id="6a2e9-140">戻り値 - inFieldDelimiter</span><span class="sxs-lookup"><span data-stu-id="6a2e9-140">Return Value - inFieldDelimiter</span></span>

<span data-ttu-id="6a2e9-141">\*Io によってアクセスされるレコード内のフィールドを区切るために使用される区切り文字。</span><span class="sxs-lookup"><span data-stu-id="6a2e9-141">The delimiter used to separate fields in records accessed by the \*Io classes.</span></span>

## <a name="method-inrecorddelimiter"></a><span data-ttu-id="6a2e9-142">メソッド inRecordDelimiter</span><span class="sxs-lookup"><span data-stu-id="6a2e9-142">Method inRecordDelimiter</span></span>

<span data-ttu-id="6a2e9-143">完全なレコードが読み込まれたかどうかを判断するために、\*Io クラスに検索する文字を決定します。</span><span class="sxs-lookup"><span data-stu-id="6a2e9-143">Determines to the \*Io classes what character or characters to search for to determine whether a full record has been read.</span></span>

```xpp
public str inRecordDelimiter([str value])
```

### <a name="parameters---inrecorddelimiter"></a><span data-ttu-id="6a2e9-144">パラメーター - inRecordDelimiter</span><span class="sxs-lookup"><span data-stu-id="6a2e9-144">Parameters - inRecordDelimiter</span></span>

<span data-ttu-id="6a2e9-145">値</span><span class="sxs-lookup"><span data-stu-id="6a2e9-145">value</span></span>  

### <a name="return-value---inrecorddelimiter"></a><span data-ttu-id="6a2e9-146">戻り値 - inRecordDelimiter</span><span class="sxs-lookup"><span data-stu-id="6a2e9-146">Return Value - inRecordDelimiter</span></span>

<span data-ttu-id="6a2e9-147">完全なレコードが読み込まれたかどうかを示す文字。</span><span class="sxs-lookup"><span data-stu-id="6a2e9-147">The character or characters that indicate whether a full record has been read.</span></span>

### <a name="remarks---inrecorddelimiter"></a><span data-ttu-id="6a2e9-148">備考 - inRecordDelimiter</span><span class="sxs-lookup"><span data-stu-id="6a2e9-148">Remarks - inRecordDelimiter</span></span>

<span data-ttu-id="6a2e9-149">標準的なテキストについては、区切り記号は改行文字です。</span><span class="sxs-lookup"><span data-stu-id="6a2e9-149">For standard text, the delimiter is a newline character.</span></span>

## <a name="method-inrecordlength"></a><span data-ttu-id="6a2e9-150">メソッド inRecordLength</span><span class="sxs-lookup"><span data-stu-id="6a2e9-150">Method inRecordLength</span></span>

<span data-ttu-id="6a2e9-151">ファイル内の各レコードを読み取る文字数を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="6a2e9-151">Gets or sets the number of characters to read for each record in a file.</span></span>

```xpp
public int inRecordLength([int value])
```

### <a name="parameters---inrecordlength"></a><span data-ttu-id="6a2e9-152">パラメーター - inRecordLength</span><span class="sxs-lookup"><span data-stu-id="6a2e9-152">Parameters - inRecordLength</span></span>

<span data-ttu-id="6a2e9-153">値</span><span class="sxs-lookup"><span data-stu-id="6a2e9-153">value</span></span>  

### <a name="return-value---inrecordlength"></a><span data-ttu-id="6a2e9-154">戻り値 - inRecordLength</span><span class="sxs-lookup"><span data-stu-id="6a2e9-154">Return Value - inRecordLength</span></span>

<span data-ttu-id="6a2e9-155">ファイル内の各レコードを読み取る文字数。</span><span class="sxs-lookup"><span data-stu-id="6a2e9-155">The number of characters to read for each record in the file.</span></span>

### <a name="remarks---inrecordlength"></a><span data-ttu-id="6a2e9-156">備考 - inRecordLength</span><span class="sxs-lookup"><span data-stu-id="6a2e9-156">Remarks - inRecordLength</span></span>

<span data-ttu-id="6a2e9-157">固定長形式になっているファイルについては、inRecordLength プロパティを使用して、各レコードに対して指定された文字数以上が読み取られていないことを保証します。</span><span class="sxs-lookup"><span data-stu-id="6a2e9-157">For files that have a fixed-length format, use the inRecordLength property to guarantee that no more than the specified number of characters are read for each record.</span></span> <span data-ttu-id="6a2e9-158">レコード フォーマットが指定された inRecordDelimiter プロパティ値で上書きされた場合、つまり、固定長が読み込まれる前に inRecordDelimiter 値が満たされている場合)、レコードは受け入れられ、追加のデータは読み込まれません。</span><span class="sxs-lookup"><span data-stu-id="6a2e9-158">If the record format is overruled by a specified inRecordDelimiter property value , that is the inRecordDelimiter value is met before the fixed length is read, the record is accepted, and no additional data is read.</span></span> <span data-ttu-id="6a2e9-159">固定数の文字を確実に読み取るには、inRecordDelimiter プロパティ値を空の文字列に設定します。</span><span class="sxs-lookup"><span data-stu-id="6a2e9-159">To guarantee that a fixed number of characters are read, set the inRecordDelimiter property value to an empty string.</span></span> <span data-ttu-id="6a2e9-160">inRecordDelimiter プロパティ値が見つからない場合、inRecordDelimiter プロパティ値は読み取れる最大文字数になります。</span><span class="sxs-lookup"><span data-stu-id="6a2e9-160">When no inRecordDelimiter property value is found, the inRecordDelimiter property value is the maximum limit of characters to read.</span></span> <span data-ttu-id="6a2e9-161">レコードの長さチェックを無効にするには、inRecordDelimiter プロパティ値をゼロに設定します。</span><span class="sxs-lookup"><span data-stu-id="6a2e9-161">Set the inRecordDelimiter property value to zero to disable the record length check.</span></span>

## <a name="method-outfielddelimiter"></a><span data-ttu-id="6a2e9-162">メソッド outFieldDelimiter</span><span class="sxs-lookup"><span data-stu-id="6a2e9-162">Method outFieldDelimiter</span></span>

<span data-ttu-id="6a2e9-163">レコードのフィールドを区切るために使用されるファイルに書き込まれる文字のシーケンスを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="6a2e9-163">Gets or sets the sequence of characters that are written to a file that is used to separate the fields of a record.</span></span>

```xpp
public str outFieldDelimiter([str value])
```

### <a name="parameters---outfielddelimiter"></a><span data-ttu-id="6a2e9-164">パラメーター - outFieldDelimiter</span><span class="sxs-lookup"><span data-stu-id="6a2e9-164">Parameters - outFieldDelimiter</span></span>

<span data-ttu-id="6a2e9-165">値</span><span class="sxs-lookup"><span data-stu-id="6a2e9-165">value</span></span>  

### <a name="return-value---outfielddelimiter"></a><span data-ttu-id="6a2e9-166">戻り値 - outFieldDelimiter</span><span class="sxs-lookup"><span data-stu-id="6a2e9-166">Return Value - outFieldDelimiter</span></span>

<span data-ttu-id="6a2e9-167">レコードのフィールドを区切るために使用されるファイルに書き込まれる文字のシーケンス。</span><span class="sxs-lookup"><span data-stu-id="6a2e9-167">The sequence of characters that are written to a file that is used to separate the fields of a record.</span></span>

## <a name="method-outrecorddelimiter"></a><span data-ttu-id="6a2e9-168">メソッド outRecordDelimiter</span><span class="sxs-lookup"><span data-stu-id="6a2e9-168">Method outRecordDelimiter</span></span>

<span data-ttu-id="6a2e9-169">出力ファイルでレコードを区切る出力ファイルに書き込まれる文字のシーケンスを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="6a2e9-169">Gets or sets the sequence of characters that is written to the output files, which separate the records in the output files.</span></span>

```xpp
public str outRecordDelimiter([str value])
```

### <a name="parameters---outrecorddelimiter"></a><span data-ttu-id="6a2e9-170">パラメーター - outRecordDelimiter</span><span class="sxs-lookup"><span data-stu-id="6a2e9-170">Parameters - outRecordDelimiter</span></span>

<span data-ttu-id="6a2e9-171">値</span><span class="sxs-lookup"><span data-stu-id="6a2e9-171">value</span></span>  

### <a name="return-value---outrecorddelimiter"></a><span data-ttu-id="6a2e9-172">戻り値 - outRecordDelimiter</span><span class="sxs-lookup"><span data-stu-id="6a2e9-172">Return Value - outRecordDelimiter</span></span>

<span data-ttu-id="6a2e9-173">出力ファイルに書き込まれる文字のシーケンス。</span><span class="sxs-lookup"><span data-stu-id="6a2e9-173">The sequence of characters that is written to the output files.</span></span>

### <a name="remarks---outrecorddelimiter"></a><span data-ttu-id="6a2e9-174">備考 - outRecordDelimiter</span><span class="sxs-lookup"><span data-stu-id="6a2e9-174">Remarks - outRecordDelimiter</span></span>

<span data-ttu-id="6a2e9-175">標準的なテキスト ファイルについては、区切り記号は改行文字です。</span><span class="sxs-lookup"><span data-stu-id="6a2e9-175">For standard text files, the delimiter is a newline character.</span></span>

## <a name="method-read"></a><span data-ttu-id="6a2e9-176">メソッド read</span><span class="sxs-lookup"><span data-stu-id="6a2e9-176">Method read</span></span>

<span data-ttu-id="6a2e9-177">Io オブジェクトから次の完全なレコードを読み取ります。</span><span class="sxs-lookup"><span data-stu-id="6a2e9-177">Reads the next full record from the Io object.</span></span>

```xpp
public container read()
```

### <a name="return-value---read"></a><span data-ttu-id="6a2e9-178">戻り値 - read</span><span class="sxs-lookup"><span data-stu-id="6a2e9-178">Return Value - read</span></span>

<span data-ttu-id="6a2e9-179">入出力オブジェクトから次の完全なレコードを保持するコンテナーです。</span><span class="sxs-lookup"><span data-stu-id="6a2e9-179">A container that holds the next full record from the Io object.</span></span>

### <a name="remarks---read"></a><span data-ttu-id="6a2e9-180">備考 - read</span><span class="sxs-lookup"><span data-stu-id="6a2e9-180">Remarks - read</span></span>

<span data-ttu-id="6a2e9-181">次の完全なレコードの定義は、次のプロパティ、inFieldDelimiter、inRecordDelimiter、および inRecordLength メソッド プロパティによって制御されます。</span><span class="sxs-lookup"><span data-stu-id="6a2e9-181">The definition of the next full record is controlled by the inFieldDelimiter, inRecordDelimiter, and inRecordLength method properties.</span></span> <span data-ttu-id="6a2e9-182">レコードはコンテナーとして返されます。</span><span class="sxs-lookup"><span data-stu-id="6a2e9-182">The record is returned as a container.</span></span> <span data-ttu-id="6a2e9-183">コンテナー内の各エントリは、レコードの 1 つのフィールドと同じです。</span><span class="sxs-lookup"><span data-stu-id="6a2e9-183">Each entry in the container equals one field in the record.</span></span> <span data-ttu-id="6a2e9-184">それぞれの特殊な Io クラスは、inFieldDelimiter、inRecordDelimiter、および inRecordLength のデフォルト設定を使用し、最も一般的な形式の入出力を可能にします。</span><span class="sxs-lookup"><span data-stu-id="6a2e9-184">Each of the specialized Io classes has default settings for inFieldDelimiter, inRecordDelimiter, and inRecordLength enabling input and output of the most common formats.</span></span> <span data-ttu-id="6a2e9-185">目的の形式をサポートするために、これらの設定の調整が生じる場合があります。</span><span class="sxs-lookup"><span data-stu-id="6a2e9-185">You might have to adjust these to support the wanted format.</span></span>

### <a name="examples---read"></a><span data-ttu-id="6a2e9-186">例 - read</span><span class="sxs-lookup"><span data-stu-id="6a2e9-186">Examples - read</span></span>

<span data-ttu-id="6a2e9-187">このメソッドは、run メソッドの使用方法を示します。</span><span class="sxs-lookup"><span data-stu-id="6a2e9-187">This method demonstrates the use of the run method.</span></span> <span data-ttu-id="6a2e9-188">ただし、次の例は、クラス、フォーム、またはその他のオブジェクトのコンテキストで実行される必要があるため、ジョブはコンパイルされません。</span><span class="sxs-lookup"><span data-stu-id="6a2e9-188">However, the following example will not compile in a job as it must be run in the context of a class, form, or other object.</span></span>

```xpp
static void Job1(Args _args) 
{ 
    FileIoPermission _perm; 
    AsciiIo myfileio; 
    Container c; 
    _perm = new FileIoPermission("myfile.txt","r"); 
    myfileio = new AsciiIo("myfile.txt","r"); 
    while(myfileio.status()==IO_Status::OK) 
    { 
        c = myfileio.read(); 
        // ...do something with the container 
    } 
}
```

## <a name="method-status"></a><span data-ttu-id="6a2e9-189">メソッド status</span><span class="sxs-lookup"><span data-stu-id="6a2e9-189">Method status</span></span>

<span data-ttu-id="6a2e9-190">Io オブジェクトで実行された最後の操作のステータスを取得します。</span><span class="sxs-lookup"><span data-stu-id="6a2e9-190">Retrieves the status of the last operation performed on the Io object.</span></span>

```xpp
public IO_Status status()
```

### <a name="return-value---status"></a><span data-ttu-id="6a2e9-191">戻り値 - status</span><span class="sxs-lookup"><span data-stu-id="6a2e9-191">Return Value - status</span></span>

<span data-ttu-id="6a2e9-192">IO\_Status システム列挙値としての最後の操作の状態。</span><span class="sxs-lookup"><span data-stu-id="6a2e9-192">The status of the last operation, as an IO\_Status system enumeration value.</span></span>

### <a name="remarks---status"></a><span data-ttu-id="6a2e9-193">備考 - status</span><span class="sxs-lookup"><span data-stu-id="6a2e9-193">Remarks - status</span></span>

<span data-ttu-id="6a2e9-194">返される可能性のある IO\_Status 値の範囲はクラスによって異なります。</span><span class="sxs-lookup"><span data-stu-id="6a2e9-194">The range of possible IO\_Status values returned varies among Io Classes.</span></span>

### <a name="examples---status"></a><span data-ttu-id="6a2e9-195">例 - status</span><span class="sxs-lookup"><span data-stu-id="6a2e9-195">Examples - status</span></span>

```xpp
static void myExample(Args _args) 
{ 
    Io myIo; 
    //.. create io object and perform some operations 
    if (myIo.status()==IO_Status::OK) 
    { 
        // ...go ahead - last operation was successful 
    } 
}
```

## <a name="method-write"></a><span data-ttu-id="6a2e9-196">メソッド write</span><span class="sxs-lookup"><span data-stu-id="6a2e9-196">Method write</span></span>

<span data-ttu-id="6a2e9-197">単純型の値を記述します。</span><span class="sxs-lookup"><span data-stu-id="6a2e9-197">Writes values of a simple type.</span></span>

```xpp
public boolean write(VarArg values)
```

### <a name="parameters---write"></a><span data-ttu-id="6a2e9-198">パラメーター - write</span><span class="sxs-lookup"><span data-stu-id="6a2e9-198">Parameters - write</span></span>

<span data-ttu-id="6a2e9-199">値</span><span class="sxs-lookup"><span data-stu-id="6a2e9-199">values</span></span>  
<span data-ttu-id="6a2e9-200">単純型は、文字列、整数、実数、列挙型、日付です。</span><span class="sxs-lookup"><span data-stu-id="6a2e9-200">The simple types are string, integer, real, enum, and date.</span></span>

### <a name="return-value---write"></a><span data-ttu-id="6a2e9-201">戻り値 - write</span><span class="sxs-lookup"><span data-stu-id="6a2e9-201">Return Value - write</span></span>

<span data-ttu-id="6a2e9-202">書き込み操作が成功する場合は true。それ以外の場合は false。</span><span class="sxs-lookup"><span data-stu-id="6a2e9-202">true if the write operation succeeds; otherwise false.</span></span> <span data-ttu-id="6a2e9-203">書き込みが失敗した場合は、ステータス メソッドがその原因を調べることができます。</span><span class="sxs-lookup"><span data-stu-id="6a2e9-203">If the write failed, the status method could be checked for the cause.</span></span>

### <a name="remarks---write"></a><span data-ttu-id="6a2e9-204">備考 - write</span><span class="sxs-lookup"><span data-stu-id="6a2e9-204">Remarks - write</span></span>

<span data-ttu-id="6a2e9-205">このメソッドは、可変数の引数を受け入れます。</span><span class="sxs-lookup"><span data-stu-id="6a2e9-205">The method accepts a variable number of arguments.</span></span> <span data-ttu-id="6a2e9-206">指定された各値は、フィールドとして出力レコードに配置されます。</span><span class="sxs-lookup"><span data-stu-id="6a2e9-206">Each value specified is put into the output record as a field.</span></span> <span data-ttu-id="6a2e9-207">最初のフィールドとしての最初の引数、2 番目のフィールドとしての 2 番目の引数など。</span><span class="sxs-lookup"><span data-stu-id="6a2e9-207">The first argument as the first field, the second argument as the second field, and so on.</span></span> <span data-ttu-id="6a2e9-208">フィールドは、outFieldDelimiter メソッドで指定されたフィールド区切り記号で区切られます。</span><span class="sxs-lookup"><span data-stu-id="6a2e9-208">The fields are separated with the field delimiter that is specified in the outFieldDelimiter method.</span></span> <span data-ttu-id="6a2e9-209">各レコードは、outRecordDelimiter 方法で区切られます。</span><span class="sxs-lookup"><span data-stu-id="6a2e9-209">Each record is separated by the outRecordDelimiter method.</span></span> <span data-ttu-id="6a2e9-210">完全なコンテナーを書き込むには、writeExp メソッドを使用します。</span><span class="sxs-lookup"><span data-stu-id="6a2e9-210">To write complete containers, use the writeExp method.</span></span>

## <a name="method-writeexp"></a><span data-ttu-id="6a2e9-211">メソッド writeExp</span><span class="sxs-lookup"><span data-stu-id="6a2e9-211">Method writeExp</span></span>

<span data-ttu-id="6a2e9-212">コンテナのコンテンツをそのファイルに記述します。</span><span class="sxs-lookup"><span data-stu-id="6a2e9-212">Writes the content of a container to the file.</span></span>

```xpp
public boolean writeExp(container data)
```

### <a name="parameters---writeexp"></a><span data-ttu-id="6a2e9-213">パラメーター - writeExp</span><span class="sxs-lookup"><span data-stu-id="6a2e9-213">Parameters - writeExp</span></span>

<span data-ttu-id="6a2e9-214">データ</span><span class="sxs-lookup"><span data-stu-id="6a2e9-214">data</span></span>  
<span data-ttu-id="6a2e9-215">レコードのデータを含むコンテナー。</span><span class="sxs-lookup"><span data-stu-id="6a2e9-215">The container with data for the record.</span></span>

### <a name="return-value---writeexp"></a><span data-ttu-id="6a2e9-216">戻り値 - writeExp</span><span class="sxs-lookup"><span data-stu-id="6a2e9-216">Return Value - writeExp</span></span>

<span data-ttu-id="6a2e9-217">操作が成功した場合は true。それ以外の場合は false。</span><span class="sxs-lookup"><span data-stu-id="6a2e9-217">true if the operation succeeded; otherwise false.</span></span>

### <a name="remarks---writeexp"></a><span data-ttu-id="6a2e9-218">備考 - writeExp</span><span class="sxs-lookup"><span data-stu-id="6a2e9-218">Remarks - writeExp</span></span>

<span data-ttu-id="6a2e9-219">このメソッドが false を返す場合、ステータス メソッドで原因を確認します。</span><span class="sxs-lookup"><span data-stu-id="6a2e9-219">If this method returns false, check the status method for the cause.</span></span> <span data-ttu-id="6a2e9-220">コンテナー内のエントリはフィールドとして扱われ、コンテナーは完全なレコードとして扱われます。</span><span class="sxs-lookup"><span data-stu-id="6a2e9-220">The entries in the container are treated as fields, and the container is treated as a full record.</span></span> <span data-ttu-id="6a2e9-221">フィールド区切り記号は、outFieldDelimiter メソッドで定義されています。</span><span class="sxs-lookup"><span data-stu-id="6a2e9-221">The field separator is defined in the outFieldDelimiter method.</span></span> <span data-ttu-id="6a2e9-222">レコード区切りは outRecordDelimiter メソッドで定義されます。</span><span class="sxs-lookup"><span data-stu-id="6a2e9-222">The record separator is defined in the outRecordDelimiter method.</span></span>

### <a name="examples---writeexp"></a><span data-ttu-id="6a2e9-223">例 - writeExp</span><span class="sxs-lookup"><span data-stu-id="6a2e9-223">Examples - writeExp</span></span>

```xpp
static void testMethod(Args _args) 
{ 
    FileIOPermission _perm; 
    container c; 
    CommaIo myfile; 
    _perm = new FileIOPermission("myfile.txt","w"); 
    _perm.assert(); 
    myfile = new CommaIo("myfile.txt","w"); 
    // Assign the entries in the container according to record layout. 
    c = [1,"MyText",1.324,"Last field"]; 
    // write this record according to file format (record/field delimiters). 
    myfile.writeExp(c); 
}
```

## <a name="method-finalize"></a><span data-ttu-id="6a2e9-224">メソッド finalize</span><span class="sxs-lookup"><span data-stu-id="6a2e9-224">Method finalize</span></span>

<span data-ttu-id="6a2e9-225">ファイルを閉じ、データが書き込まれている場合、ファイル バッファーをディスクにフラッシュします。</span><span class="sxs-lookup"><span data-stu-id="6a2e9-225">Closes the file and, if data was written, flushes the file buffers to disk.</span></span>

```xpp
public void finalize()
```

### <a name="remarks---finalize"></a><span data-ttu-id="6a2e9-226">備考 - finalize</span><span class="sxs-lookup"><span data-stu-id="6a2e9-226">Remarks - finalize</span></span>

<span data-ttu-id="6a2e9-227">オブジェクトは、通常、スコープから離れることによって確定されるため、確定は通常は直接呼び出されません。</span><span class="sxs-lookup"><span data-stu-id="6a2e9-227">The object is typically finalized by leaving the scope, so finalize is typically not called directly.</span></span> <span data-ttu-id="6a2e9-228">記述された出力はオブジェクトの終了前は無効です。</span><span class="sxs-lookup"><span data-stu-id="6a2e9-228">Written output will not be valid before the object is finalized.</span></span>

## <a name="method-new"></a><span data-ttu-id="6a2e9-229">メソッド new</span><span class="sxs-lookup"><span data-stu-id="6a2e9-229">Method new</span></span>

<span data-ttu-id="6a2e9-230">Io クラスの新しいインスタンスを作成します。</span><span class="sxs-lookup"><span data-stu-id="6a2e9-230">Creates a new instance of the Io class.</span></span>

```xpp
public void new(str filename, str mode)
```

### <a name="parameters---new"></a><span data-ttu-id="6a2e9-231">パラメーター - new</span><span class="sxs-lookup"><span data-stu-id="6a2e9-231">Parameters - new</span></span>

<span data-ttu-id="6a2e9-232">filename</span><span class="sxs-lookup"><span data-stu-id="6a2e9-232">filename</span></span>  
<span data-ttu-id="6a2e9-233">ファイルを開く必要があるモード。</span><span class="sxs-lookup"><span data-stu-id="6a2e9-233">The mode in which the file should be opened.</span></span>

<!-- -->

<span data-ttu-id="6a2e9-234">モード</span><span class="sxs-lookup"><span data-stu-id="6a2e9-234">mode</span></span>  
<span data-ttu-id="6a2e9-235">ファイルを開く必要があるモード。</span><span class="sxs-lookup"><span data-stu-id="6a2e9-235">The mode in which the file should be opened.</span></span>

### <a name="remarks---new"></a><span data-ttu-id="6a2e9-236">備考 - new</span><span class="sxs-lookup"><span data-stu-id="6a2e9-236">Remarks - new</span></span>

<span data-ttu-id="6a2e9-237">mode パラメーターは、次のモードのいずれかになります。</span><span class="sxs-lookup"><span data-stu-id="6a2e9-237">The mode parameter can be one of the following modes:</span></span>

-   <span data-ttu-id="6a2e9-238">R � 読み取り</span><span class="sxs-lookup"><span data-stu-id="6a2e9-238">R � read</span></span>
-   <span data-ttu-id="6a2e9-239">W � 書き込み</span><span class="sxs-lookup"><span data-stu-id="6a2e9-239">W � write</span></span>
-   <span data-ttu-id="6a2e9-240">A � 追加 (意味 W)</span><span class="sxs-lookup"><span data-stu-id="6a2e9-240">A � append (implies W)</span></span>
-   <span data-ttu-id="6a2e9-241">T � 翻訳 (テキスト)</span><span class="sxs-lookup"><span data-stu-id="6a2e9-241">T � translate (text)</span></span>
-   <span data-ttu-id="6a2e9-242">B � バイナリ</span><span class="sxs-lookup"><span data-stu-id="6a2e9-242">B � binary</span></span>

<span data-ttu-id="6a2e9-243">ランタイム エラーは、現在開いているモードに対応しないメソッドでファイルにアクセスすると発生します (たとえば、読み取りモード ファイルに書き込もうとした場合など)。</span><span class="sxs-lookup"><span data-stu-id="6a2e9-243">A run-time error occurs if the file is accessed with a method that does not correspond to the current opened mode (for example, if an attempt is made to write to a read-mode file).</span></span> <span data-ttu-id="6a2e9-244">攻撃者が新しいメソッドへの入力を制御できる場合、セキュリティ上のリスクが存在します。</span><span class="sxs-lookup"><span data-stu-id="6a2e9-244">If an attacker can control input to the new method, a security risk exists.</span></span> <span data-ttu-id="6a2e9-245">したがって、このメソッドは、コード アクセス セキュリティで実行されます。</span><span class="sxs-lookup"><span data-stu-id="6a2e9-245">Therefore, this method runs under Code Access Security.</span></span> <span data-ttu-id="6a2e9-246">サーバー上でこのメソッドを呼び出すには、アクセス許可が必要です。</span><span class="sxs-lookup"><span data-stu-id="6a2e9-246">Calls to this method on the server require permission.</span></span> <span data-ttu-id="6a2e9-247">.</span><span class="sxs-lookup"><span data-stu-id="6a2e9-247">.</span></span> <span data-ttu-id="6a2e9-248">ユーザーがこのメソッドを呼び出すコントロールで、SysDevelopment へのセキュリティ キーを設定して開発権限があることを確認します。</span><span class="sxs-lookup"><span data-stu-id="6a2e9-248">Ensure that the user has development privileges by setting the security key to SysDevelopment on the control that calls this method.</span></span>

### <a name="examples---new"></a><span data-ttu-id="6a2e9-249">例 - new</span><span class="sxs-lookup"><span data-stu-id="6a2e9-249">Examples - new</span></span>

<span data-ttu-id="6a2e9-250">この例では、Io クラスを使用して ExampleFile に書き込みます。</span><span class="sxs-lookup"><span data-stu-id="6a2e9-250">This example uses the Io class to write to ExampleFile.</span></span>

```xpp
void IoExample() 
{ 
    Io io; 
    container con; 
    FileIoPermission perm; 
    #define.ExampleFile(@"c:\test.txt") 
    #define.ExampleOpenMode("w") 
    // Grants permission to execute the 
    // Io.new method. 
    // Io.new runs under code access security. 
    perm = new FileIoPermission(#ExampleFile, #ExampleOpenMode); 
    if (perm == null) 
    { 
        return; 
    } 
    perm.assert(); 
    io = new Io(#ExampleFile, #ExampleOpenMode); 
    if (io != null) 
    { 
        io.write("Test"); 
    } 
    // Close the code access permission scope. 
    CodeAccessPermission::revertAssert(); 
}
```


