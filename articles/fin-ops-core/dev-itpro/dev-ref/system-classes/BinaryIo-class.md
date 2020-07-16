---
title: BinaryIo クラス
description: このトピックでは、BinaryIo クラスについて説明します。
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
ms.openlocfilehash: bc23aa8f224926191dc3aa69ff7b965ae1259ebc
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502719"
---
# <a name="class-binaryio"></a><span data-ttu-id="d0be4-103">クラス BinaryIo</span><span class="sxs-lookup"><span data-stu-id="d0be4-103">Class BinaryIo</span></span>

[!include [banner](../../includes/banner.md)]

```xpp
class BinaryIo extends Io
```

## <a name="remarks"></a><span data-ttu-id="d0be4-104">備考</span><span class="sxs-lookup"><span data-stu-id="d0be4-104">Remarks</span></span>

## <a name="examples"></a><span data-ttu-id="d0be4-105">例</span><span class="sxs-lookup"><span data-stu-id="d0be4-105">Examples</span></span>

## <a name="methods"></a><span data-ttu-id="d0be4-106">メソッド</span><span class="sxs-lookup"><span data-stu-id="d0be4-106">Methods</span></span>

| <span data-ttu-id="d0be4-107">方法</span><span class="sxs-lookup"><span data-stu-id="d0be4-107">Method</span></span>                                  | <span data-ttu-id="d0be4-108">説明</span><span class="sxs-lookup"><span data-stu-id="d0be4-108">Description</span></span>                                                                     |
|-----------------------------------------|---------------------------------------------------------------------------------|
| <span data-ttu-id="d0be4-109">public container read()</span><span class="sxs-lookup"><span data-stu-id="d0be4-109">public container read()</span></span>                 | <span data-ttu-id="d0be4-110">Io オブジェクトから次の完全なレコードを読み取ります。</span><span class="sxs-lookup"><span data-stu-id="d0be4-110">Reads the next full record from the Io object.</span></span>                                  |
| <span data-ttu-id="d0be4-111">public IO\_Status status()</span><span class="sxs-lookup"><span data-stu-id="d0be4-111">public IO\_Status status()</span></span>              | <span data-ttu-id="d0be4-112">Io オブジェクトで実行された最後の操作のステータスを取得します。</span><span class="sxs-lookup"><span data-stu-id="d0be4-112">Retrieves the status of the last operation that was performed on the Io object.</span></span> |
| <span data-ttu-id="d0be4-113">public boolean write(VarArg values)</span><span class="sxs-lookup"><span data-stu-id="d0be4-113">public boolean write(VarArg values)</span></span>     | <span data-ttu-id="d0be4-114">単純型の値を記述します。</span><span class="sxs-lookup"><span data-stu-id="d0be4-114">Writes values of a simple type.</span></span>                                                 |
| <span data-ttu-id="d0be4-115">public boolean writeExp(container data)</span><span class="sxs-lookup"><span data-stu-id="d0be4-115">public boolean writeExp(container data)</span></span> | <span data-ttu-id="d0be4-116">コンテナのコンテンツをファイルに記述します。</span><span class="sxs-lookup"><span data-stu-id="d0be4-116">Writes the content of a container to a file.</span></span>                                    |
| <span data-ttu-id="d0be4-117">public void new(str filename, str mode)</span><span class="sxs-lookup"><span data-stu-id="d0be4-117">public void new(str filename, str mode)</span></span> | <span data-ttu-id="d0be4-118">BinaryIo クラスのインスタンスを作成します。</span><span class="sxs-lookup"><span data-stu-id="d0be4-118">Creates an instance of the BinaryIo class.</span></span>                                      |
| <span data-ttu-id="d0be4-119">public void finalize()</span><span class="sxs-lookup"><span data-stu-id="d0be4-119">public void finalize()</span></span>                  | <span data-ttu-id="d0be4-120">ファイルを閉じ、データが書き込まれている場合、ファイル バッファーをディスクにフラッシュします。</span><span class="sxs-lookup"><span data-stu-id="d0be4-120">Closes the file and, if data was written, flushes the file buffers to disk.</span></span>     |

## <a name="method-read"></a><span data-ttu-id="d0be4-121">メソッド read</span><span class="sxs-lookup"><span data-stu-id="d0be4-121">Method read</span></span>

<span data-ttu-id="d0be4-122">Io オブジェクトから次の完全なレコードを読み取ります。</span><span class="sxs-lookup"><span data-stu-id="d0be4-122">Reads the next full record from the Io object.</span></span>

```xpp
public container read()
```

### <a name="return-value---read"></a><span data-ttu-id="d0be4-123">戻り値 - read</span><span class="sxs-lookup"><span data-stu-id="d0be4-123">Return Value - read</span></span>

<span data-ttu-id="d0be4-124">入出力オブジェクトから次の完全なレコードを保持するコンテナーです。</span><span class="sxs-lookup"><span data-stu-id="d0be4-124">A container that holds the next full record from the Io object.</span></span>

### <a name="remarks---read"></a><span data-ttu-id="d0be4-125">備考 - read</span><span class="sxs-lookup"><span data-stu-id="d0be4-125">Remarks - read</span></span>

<span data-ttu-id="d0be4-126">次の完全なレコードの定義は、次のプロパティ、inFieldDelimiter、inRecordDelimiter、および inRecordLength メソッド プロパティによって制御されます。</span><span class="sxs-lookup"><span data-stu-id="d0be4-126">The definition of the next full record is controlled by the inFieldDelimiter, inRecordDelimiter, and inRecordLength method properties.</span></span> <span data-ttu-id="d0be4-127">レコードはコンテナーとして返されます。</span><span class="sxs-lookup"><span data-stu-id="d0be4-127">The record is returned as a container.</span></span> <span data-ttu-id="d0be4-128">コンテナー内の各エントリは、レコードの 1 つのフィールドと同じです。</span><span class="sxs-lookup"><span data-stu-id="d0be4-128">Each entry in the container equals one field in the record.</span></span> <span data-ttu-id="d0be4-129">そべての特殊な Io クラスには、inFieldDelimiter、inRecordDelimiter、および inRecordLength のプロパティのデフォルト設定があります。</span><span class="sxs-lookup"><span data-stu-id="d0be4-129">Every specialized Io class has default settings for the inFieldDelimiter, inRecordDelimiter, and inRecordLength properties.</span></span> <span data-ttu-id="d0be4-130">これらの既定の設定では、最も一般的な形式の入力と出力が可能です。</span><span class="sxs-lookup"><span data-stu-id="d0be4-130">These default settings enable input and output of the most common formats.</span></span> <span data-ttu-id="d0be4-131">使用する形式をサポートするために、これらの設定の調整が生じる場合があります。</span><span class="sxs-lookup"><span data-stu-id="d0be4-131">You might have to adjust these settings to support the format that you want to use.</span></span>

## <a name="method-status"></a><span data-ttu-id="d0be4-132">メソッド status</span><span class="sxs-lookup"><span data-stu-id="d0be4-132">Method status</span></span>

<span data-ttu-id="d0be4-133">Io オブジェクトで実行された最後の操作のステータスを取得します。</span><span class="sxs-lookup"><span data-stu-id="d0be4-133">Retrieves the status of the last operation that was performed on the Io object.</span></span>

```xpp
public IO_Status status()
```

### <a name="return-value---status"></a><span data-ttu-id="d0be4-134">戻り値 - status</span><span class="sxs-lookup"><span data-stu-id="d0be4-134">Return Value - status</span></span>

<span data-ttu-id="d0be4-135">IO\_Status システム列挙値としての最後の操作の状態。</span><span class="sxs-lookup"><span data-stu-id="d0be4-135">The status of the last operation as an IO\_Status system enumeration value.</span></span>

### <a name="remarks---status"></a><span data-ttu-id="d0be4-136">備考 - status</span><span class="sxs-lookup"><span data-stu-id="d0be4-136">Remarks - status</span></span>

<span data-ttu-id="d0be4-137">返される可能性のある IO\_Status の値の範囲は、Io クラスによって異なります。</span><span class="sxs-lookup"><span data-stu-id="d0be4-137">The range of possible IO\_Status values that are returned varies, depending on the Io class.</span></span>

## <a name="method-write"></a><span data-ttu-id="d0be4-138">メソッド write</span><span class="sxs-lookup"><span data-stu-id="d0be4-138">Method write</span></span>

<span data-ttu-id="d0be4-139">単純型の値を記述します。</span><span class="sxs-lookup"><span data-stu-id="d0be4-139">Writes values of a simple type.</span></span>

```xpp
public boolean write(VarArg values)
```

### <a name="parameters---write"></a><span data-ttu-id="d0be4-140">パラメーター - write</span><span class="sxs-lookup"><span data-stu-id="d0be4-140">Parameters - write</span></span>

<span data-ttu-id="d0be4-141">値</span><span class="sxs-lookup"><span data-stu-id="d0be4-141">values</span></span>  
<span data-ttu-id="d0be4-142">単純型。</span><span class="sxs-lookup"><span data-stu-id="d0be4-142">The simple type.</span></span> <span data-ttu-id="d0be4-143">単純型は、文字列、整数、実数、列挙型、日付です。</span><span class="sxs-lookup"><span data-stu-id="d0be4-143">The simple types are string, integer, real, enum, and date.</span></span>

### <a name="return-value---write"></a><span data-ttu-id="d0be4-144">戻り値 - write</span><span class="sxs-lookup"><span data-stu-id="d0be4-144">Return Value - write</span></span>

<span data-ttu-id="d0be4-145">書き込み操作が成功する場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="d0be4-145">true if the write operation succeeds; otherwise, false.</span></span> <span data-ttu-id="d0be4-146">書き込み操作が失敗すると、ステータス メソッドで原因について確認できます。</span><span class="sxs-lookup"><span data-stu-id="d0be4-146">If the write operation is unsuccessful, you can check the status method for the cause.</span></span>

### <a name="remarks---write"></a><span data-ttu-id="d0be4-147">備考 - write</span><span class="sxs-lookup"><span data-stu-id="d0be4-147">Remarks - write</span></span>

<span data-ttu-id="d0be4-148">このメソッドは、可変数の引数を受け入れます。</span><span class="sxs-lookup"><span data-stu-id="d0be4-148">This method accepts a variable number of arguments.</span></span> <span data-ttu-id="d0be4-149">指定された各値は、フィールドとして出力レコードに配置されます。</span><span class="sxs-lookup"><span data-stu-id="d0be4-149">Each value that is specified is put into the output record as a field.</span></span> <span data-ttu-id="d0be4-150">最初の引数は最初のフィールドであり、2 番目の引数は 2 番目のフィールドなどになります。</span><span class="sxs-lookup"><span data-stu-id="d0be4-150">The first argument is the first field, the second argument is the second field, and so on.</span></span> <span data-ttu-id="d0be4-151">フィールドは、outFieldDelimiter メソッドで指定されたフィールド区切り記号で区切られます。</span><span class="sxs-lookup"><span data-stu-id="d0be4-151">The fields are separated by the field delimiter that is specified in the outFieldDelimiter method.</span></span> <span data-ttu-id="d0be4-152">各レコードは、outRecordDelimiter メソッドで指定されるレコード 区切り記号で区切られます。</span><span class="sxs-lookup"><span data-stu-id="d0be4-152">Each record is separated by the record delimiter that is specified in the outRecordDelimiter method.</span></span> <span data-ttu-id="d0be4-153">完全なコンテナーを書き込むには、writeExp メソッドを使用します。</span><span class="sxs-lookup"><span data-stu-id="d0be4-153">To write complete containers, use the writeExp method.</span></span>

## <a name="method-writeexp"></a><span data-ttu-id="d0be4-154">メソッド writeExp</span><span class="sxs-lookup"><span data-stu-id="d0be4-154">Method writeExp</span></span>

<span data-ttu-id="d0be4-155">コンテナのコンテンツをファイルに記述します。</span><span class="sxs-lookup"><span data-stu-id="d0be4-155">Writes the content of a container to a file.</span></span>

```xpp
public boolean writeExp(container data)
```

### <a name="parameters---writeexp"></a><span data-ttu-id="d0be4-156">パラメーター - writeExp</span><span class="sxs-lookup"><span data-stu-id="d0be4-156">Parameters - writeExp</span></span>

<span data-ttu-id="d0be4-157">データ</span><span class="sxs-lookup"><span data-stu-id="d0be4-157">data</span></span>  
<span data-ttu-id="d0be4-158">レコードのデータを保持するコンテナー。</span><span class="sxs-lookup"><span data-stu-id="d0be4-158">The container that holds data for the record.</span></span>

### <a name="return-value---writeexp"></a><span data-ttu-id="d0be4-159">戻り値 - writeExp</span><span class="sxs-lookup"><span data-stu-id="d0be4-159">Return Value - writeExp</span></span>

<span data-ttu-id="d0be4-160">操作が成功する場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="d0be4-160">true if the operation is successful; otherwise, false.</span></span>

### <a name="remarks---writeexp"></a><span data-ttu-id="d0be4-161">備考 - writeExp</span><span class="sxs-lookup"><span data-stu-id="d0be4-161">Remarks - writeExp</span></span>

<span data-ttu-id="d0be4-162">このメソッドが false を返す場合、ステータス メソッドで原因を確認します。</span><span class="sxs-lookup"><span data-stu-id="d0be4-162">If this method returns false, check the status method for the cause.</span></span> <span data-ttu-id="d0be4-163">コンテナー内のエントリはフィールドとして扱われ、コンテナーは完全なレコードとして扱われます。</span><span class="sxs-lookup"><span data-stu-id="d0be4-163">The entries in the container are treated as fields, and the container is treated as a full record.</span></span> <span data-ttu-id="d0be4-164">フィールド区切り記号は、outFieldDelimiter メソッドで定義されています。</span><span class="sxs-lookup"><span data-stu-id="d0be4-164">The field separator is defined in the outFieldDelimiter method.</span></span> <span data-ttu-id="d0be4-165">レコード区切りは outRecordDelimiter メソッドで定義されます。</span><span class="sxs-lookup"><span data-stu-id="d0be4-165">The record separator is defined in the outRecordDelimiter method.</span></span>

## <a name="method-new"></a><span data-ttu-id="d0be4-166">メソッド new</span><span class="sxs-lookup"><span data-stu-id="d0be4-166">Method new</span></span>

<span data-ttu-id="d0be4-167">BinaryIo クラスのインスタンスを作成します。</span><span class="sxs-lookup"><span data-stu-id="d0be4-167">Creates an instance of the BinaryIo class.</span></span>

```xpp
public void new(str filename, str mode)
```

### <a name="parameters---new"></a><span data-ttu-id="d0be4-168">パラメーター - new</span><span class="sxs-lookup"><span data-stu-id="d0be4-168">Parameters - new</span></span>

<span data-ttu-id="d0be4-169">filename</span><span class="sxs-lookup"><span data-stu-id="d0be4-169">filename</span></span>  
<span data-ttu-id="d0be4-170">BinaryIo クラスのインスタンスを作成するために使用するモード。</span><span class="sxs-lookup"><span data-stu-id="d0be4-170">The mode to use to create the instance of the BinaryIo class.</span></span>

<!-- -->

<span data-ttu-id="d0be4-171">モード</span><span class="sxs-lookup"><span data-stu-id="d0be4-171">mode</span></span>  
<span data-ttu-id="d0be4-172">BinaryIo クラスのインスタンスを作成するために使用するモード。</span><span class="sxs-lookup"><span data-stu-id="d0be4-172">The mode to use to create the instance of the BinaryIo class.</span></span>

### <a name="remarks---new"></a><span data-ttu-id="d0be4-173">備考 - new</span><span class="sxs-lookup"><span data-stu-id="d0be4-173">Remarks - new</span></span>

<span data-ttu-id="d0be4-174">攻撃者が新しいメソッドへの入力を制御できる場合、セキュリティ上のリスクが存在します。</span><span class="sxs-lookup"><span data-stu-id="d0be4-174">If an attacker can control input to the new method, a security risk exists.</span></span> <span data-ttu-id="d0be4-175">したがって、このメソッドはクラス下で実行されます。</span><span class="sxs-lookup"><span data-stu-id="d0be4-175">Therefore, this method runs under class.</span></span> <span data-ttu-id="d0be4-176">ユーザーがこのメソッドを呼び出すコントロールで、SysDevelopment へのセキュリティ キーを設定して開発権限を持っていることを確認します。</span><span class="sxs-lookup"><span data-stu-id="d0be4-176">Make sure that the user has development privileges by setting the security key to SysDevelopment on the control that calls this method.</span></span>

### <a name="examples---new"></a><span data-ttu-id="d0be4-177">例 - new</span><span class="sxs-lookup"><span data-stu-id="d0be4-177">Examples - new</span></span>

<span data-ttu-id="d0be4-178">この例では、BinaryIo クラスを使用して、ExampleFile のテキスト ファイルからデータを読み込みます。</span><span class="sxs-lookup"><span data-stu-id="d0be4-178">This example uses the BinaryIo class to read data from the ExampleFile text file.</span></span>

```xpp
static void BinaryIoExampleW2(Args _args)
{     
    #define.ExampleFile(@"D:\Writers\GeneMi\_Junk\TestW.BinaryIo")
    #define.ExampleOpenModeW("w")
    #define.ExampleOpenModeR("r")
    BinaryIo binaryIoObject;
    container con1;
    str sConRecs;
    FileIoPermission perm;
```

```xpp
    // Set the code access permission to help protect the use of
    // the BinaryIo.new method.
    perm = new FileIoPermission(#ExampleFile, #ExampleOpenModeW);
    if (perm == null)
    {
        return;
    }
    perm.assert();
```

```xpp
    // Overwrites the file if it already exists; restarts it as empty.
    binaryIoObject = new BinaryIo(#ExampleFile, #ExampleOpenModeW);
    if (binaryIoObject != null)
    {
        info("w binaryIoObject is NOT null, Good.");
        binaryIoObject.write("hello world");
        binaryIoObject.write("goodbye solar system");
    }
    else
    {
        warning("w binaryIoObject is NULL, Bad.");
    }
```

```xpp
    binaryIoObject.finalize();
    binaryIoObject = null;
    // Close the file, w?
    // BinaryIo instance can only read files in that
    // are in the exact same esoteric format that BinaryIo
    // writes files to.
    // binaryIoObject = new BinaryIo(#ExampleFile, #ExampleOpenModeR);
    if (binaryIoObject != null)
    {
         info("r binaryIoObject is NOT null, Good.");
         while (true)
        {
            con1 = binaryIoObject.read();
            if (con1 == conNull())
            {
                info("r, no more records.");
                break;
            }
            sConRecs = con2Str(con1);
            info(sConRecs);
        }
    }
    else
    {
         warning("r binaryIoObject is NULL, Bad.");
    }
    binaryIoObject.finalize();
    binaryIoObject = null;
    WINAPI::deleteFile(#ExampleFile);
     // Clean up after the job.
    CodeAccessPermission::revertAssert();
 }
/*** Output copied from Infolog:Message (11:22:16 am)w binaryIoObject is NOT null, Good.r binaryIoObject is NOT null, Good.hello worldgoodbye solar systemr, no more records.***/
```

## <a name="method-finalize"></a><span data-ttu-id="d0be4-179">メソッド finalize</span><span class="sxs-lookup"><span data-stu-id="d0be4-179">Method finalize</span></span>

<span data-ttu-id="d0be4-180">ファイルを閉じ、データが書き込まれている場合、ファイル バッファーをディスクにフラッシュします。</span><span class="sxs-lookup"><span data-stu-id="d0be4-180">Closes the file and, if data was written, flushes the file buffers to disk.</span></span>

```xpp
public void finalize()
```

### <a name="remarks---finalize"></a><span data-ttu-id="d0be4-181">備考 - finalize</span><span class="sxs-lookup"><span data-stu-id="d0be4-181">Remarks - finalize</span></span>

<span data-ttu-id="d0be4-182">通常、スコープを離れることでオブジェクトを確定します。</span><span class="sxs-lookup"><span data-stu-id="d0be4-182">Typically, you finalize the object by leaving the scope.</span></span> <span data-ttu-id="d0be4-183">したがって、確定メソッドは、通常は直接呼び出されません。</span><span class="sxs-lookup"><span data-stu-id="d0be4-183">Therefore, the finalize method is not usually called directly.</span></span> <span data-ttu-id="d0be4-184">記述された出力はオブジェクトが終了するまで無効です。</span><span class="sxs-lookup"><span data-stu-id="d0be4-184">Written output is not valid until the object is finalized.</span></span>

