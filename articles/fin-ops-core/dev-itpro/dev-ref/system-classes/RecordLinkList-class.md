---
title: RecordLinkList クラス
description: このトピックでは、RecordLinkList クラスについて説明します。
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
ms.openlocfilehash: af06ffe02fe54b794074bd6d6bc997f0a0e86cfb
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502855"
---
# <a name="class-recordlinklist"></a><span data-ttu-id="f44f4-103">クラス RecordLinkList</span><span class="sxs-lookup"><span data-stu-id="f44f4-103">Class RecordLinkList</span></span>

[!include [banner](../../includes/banner.md)]

```xpp
class RecordLinkList extends Object
```

<span data-ttu-id="f44f4-104">RecordLinkList クラスは、さまざまな種類のレコードを保持することができ、キー入力も並べ替えもされていないレコード バッファーのキャッシュを動的に作成します。</span><span class="sxs-lookup"><span data-stu-id="f44f4-104">The RecordLinkList class dynamically creates a cache of record buffers that can hold records of different types, and that is not keyed or sorted.</span></span>

## <a name="remarks"></a><span data-ttu-id="f44f4-105">備考</span><span class="sxs-lookup"><span data-stu-id="f44f4-105">Remarks</span></span>

<span data-ttu-id="f44f4-106">RecordLinkList オブジェクトは、同時にさまざまなタイプのレコードを保持できる二重にリンクされたリストです。</span><span class="sxs-lookup"><span data-stu-id="f44f4-106">A recordLinkList object is a double-linked list that can hold records of different types at the same time.</span></span> <span data-ttu-id="f44f4-107">キー入力や並べ替えはされません。</span><span class="sxs-lookup"><span data-stu-id="f44f4-107">It is not keyed or sorted.</span></span> <span data-ttu-id="f44f4-108">recordLinkList オブジェクトは、同じレコードを再度取得するのではなく、異なるテーブルのレコードをパラメーターとして渡す場合に特に便利です。</span><span class="sxs-lookup"><span data-stu-id="f44f4-108">The recordLinkList object is especially useful for passing records from different tables as a parameter instead of retrieving the same records again.</span></span> <span data-ttu-id="f44f4-109">recordSortedList オブジェクトのサイズに制限はありません。</span><span class="sxs-lookup"><span data-stu-id="f44f4-109">There is no limit to the size of a recordSortedList object.</span></span> <span data-ttu-id="f44f4-110">そのサイズおよびメモリ消費を制御するのはプログラマーの責任です。</span><span class="sxs-lookup"><span data-stu-id="f44f4-110">It is the responsibility of the programmer to control its size and therefore its memory consumption.</span></span>

## <a name="examples"></a><span data-ttu-id="f44f4-111">例</span><span class="sxs-lookup"><span data-stu-id="f44f4-111">Examples</span></span>

## <a name="methods"></a><span data-ttu-id="f44f4-112">メソッド</span><span class="sxs-lookup"><span data-stu-id="f44f4-112">Methods</span></span>

| <span data-ttu-id="f44f4-113">方法</span><span class="sxs-lookup"><span data-stu-id="f44f4-113">Method</span></span>                                           | <span data-ttu-id="f44f4-114">説明</span><span class="sxs-lookup"><span data-stu-id="f44f4-114">Description</span></span>                                                                                                                                |
|--------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f44f4-115">public int del()</span><span class="sxs-lookup"><span data-stu-id="f44f4-115">public int del()</span></span>                                 | <span data-ttu-id="f44f4-116">リスト内の現在の位置のレコードを削除します。</span><span class="sxs-lookup"><span data-stu-id="f44f4-116">Deletes the record at the current position in the list.</span></span>                                                                                    |
| <span data-ttu-id="f44f4-117">public TableId fileId()</span><span class="sxs-lookup"><span data-stu-id="f44f4-117">public TableId fileId()</span></span>                          | <span data-ttu-id="f44f4-118">リスト内の現在の位置のレコードのテーブル ID を取得します。</span><span class="sxs-lookup"><span data-stu-id="f44f4-118">Retrieves the table ID of the record at the current position in the list.</span></span>                                                                  |
| <span data-ttu-id="f44f4-119">public boolean first(\[Common record\])</span><span class="sxs-lookup"><span data-stu-id="f44f4-119">public boolean first(\[Common record\])</span></span>          | <span data-ttu-id="f44f4-120">一覧の最初のレコードにポインターを設定し、存在する場合は、提供されるバッファーにレコードをコピーします。</span><span class="sxs-lookup"><span data-stu-id="f44f4-120">Puts the pointer on the first record in the list and, if it is present, copies the record into the buffer that is provided.</span></span>                |
| <span data-ttu-id="f44f4-121">public boolean get(Common record, \[int index\])</span><span class="sxs-lookup"><span data-stu-id="f44f4-121">public boolean get(Common record, \[int index\])</span></span> | <span data-ttu-id="f44f4-122">現在の位置、または指定された位置のレコードを、指定されたレコード バッファーにコピーします。ただし、ポインタの位置には影響しません。</span><span class="sxs-lookup"><span data-stu-id="f44f4-122">Copies the record at the current position or the specified position to the provided record buffer, without affecting the pointer position.</span></span> |
| <span data-ttu-id="f44f4-123">public int ins(Common record)</span><span class="sxs-lookup"><span data-stu-id="f44f4-123">public int ins(Common record)</span></span>                    | <span data-ttu-id="f44f4-124">リストの最後にレコードを挿入します。</span><span class="sxs-lookup"><span data-stu-id="f44f4-124">Inserts a record at the end of a list.</span></span>                                                                                                     |
| <span data-ttu-id="f44f4-125">public boolean last(\[Common record\])</span><span class="sxs-lookup"><span data-stu-id="f44f4-125">public boolean last(\[Common record\])</span></span>           | <span data-ttu-id="f44f4-126">最後のレコードにリストを配置し、レコードを指定されたレコード バッファにコピーします。</span><span class="sxs-lookup"><span data-stu-id="f44f4-126">Puts the list at the last record and copies the record to the specified record buffer.</span></span>                                                     |
| <span data-ttu-id="f44f4-127">public int len()</span><span class="sxs-lookup"><span data-stu-id="f44f4-127">public int len()</span></span>                                 | <span data-ttu-id="f44f4-128">リスト内の現在のレコード数を返します。</span><span class="sxs-lookup"><span data-stu-id="f44f4-128">Returns the current number of records in the list.</span></span>                                                                                         |
| <span data-ttu-id="f44f4-129">public boolean next(\[Common record\])</span><span class="sxs-lookup"><span data-stu-id="f44f4-129">public boolean next(\[Common record\])</span></span>           | <span data-ttu-id="f44f4-130">次のレコードにカーソルを置き、指定されたバッファーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="f44f4-130">Puts the pointer on the next record and copies it to the provided buffer.</span></span>                                                                  |
| <span data-ttu-id="f44f4-131">public Common peek()</span><span class="sxs-lookup"><span data-stu-id="f44f4-131">public Common peek()</span></span>                             | <span data-ttu-id="f44f4-132">リスト内の現在の位置のレコードを取得します。</span><span class="sxs-lookup"><span data-stu-id="f44f4-132">Retrieves the record at the current position in the list.</span></span>                                                                                  |
| <span data-ttu-id="f44f4-133">public boolean prev(\[Common record\])</span><span class="sxs-lookup"><span data-stu-id="f44f4-133">public boolean prev(\[Common record\])</span></span>           | <span data-ttu-id="f44f4-134">リスト内の前のレコードにポインターを配置し、レコードを指定されたバッファーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="f44f4-134">Puts the pointer on the previous record in the list and copies the record to the specified buffer.</span></span>                                         |
| <span data-ttu-id="f44f4-135">public void new()</span><span class="sxs-lookup"><span data-stu-id="f44f4-135">public void new()</span></span>                                | <span data-ttu-id="f44f4-136">RecordLinkList クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="f44f4-136">Initializes a new instance of the RecordLinkList class.</span></span>                                                                                    |

## <a name="method-del"></a><span data-ttu-id="f44f4-137">メソッド del</span><span class="sxs-lookup"><span data-stu-id="f44f4-137">Method del</span></span>

<span data-ttu-id="f44f4-138">リスト内の現在の位置のレコードを削除します。</span><span class="sxs-lookup"><span data-stu-id="f44f4-138">Deletes the record at the current position in the list.</span></span>

```xpp
public int del()
```

### <a name="return-value---del"></a><span data-ttu-id="f44f4-139">戻り値 - del</span><span class="sxs-lookup"><span data-stu-id="f44f4-139">Return Value - del</span></span>

<span data-ttu-id="f44f4-140">リストに残っているレコードの数。</span><span class="sxs-lookup"><span data-stu-id="f44f4-140">The number of records that remain in the list.</span></span>

## <a name="method-fileid"></a><span data-ttu-id="f44f4-141">メソッド fileId</span><span class="sxs-lookup"><span data-stu-id="f44f4-141">Method fileId</span></span>

<span data-ttu-id="f44f4-142">リスト内の現在の位置のレコードのテーブル ID を取得します。</span><span class="sxs-lookup"><span data-stu-id="f44f4-142">Retrieves the table ID of the record at the current position in the list.</span></span>

```xpp
public TableId fileId()
```

### <a name="return-value---fileid"></a><span data-ttu-id="f44f4-143">戻り値 - fileId</span><span class="sxs-lookup"><span data-stu-id="f44f4-143">Return Value - fileId</span></span>

<span data-ttu-id="f44f4-144">テーブル ID。</span><span class="sxs-lookup"><span data-stu-id="f44f4-144">The table ID.</span></span>

## <a name="method-first"></a><span data-ttu-id="f44f4-145">メソッド first</span><span class="sxs-lookup"><span data-stu-id="f44f4-145">Method first</span></span>

<span data-ttu-id="f44f4-146">一覧の最初のレコードにポインターを設定し、存在する場合は、提供されるバッファーにレコードをコピーします。</span><span class="sxs-lookup"><span data-stu-id="f44f4-146">Puts the pointer on the first record in the list and, if it is present, copies the record into the buffer that is provided.</span></span>

```xpp
public boolean first([Common record])
```

### <a name="parameters---first"></a><span data-ttu-id="f44f4-147">パラメーター - first</span><span class="sxs-lookup"><span data-stu-id="f44f4-147">Parameters - first</span></span>

<span data-ttu-id="f44f4-148">記録</span><span class="sxs-lookup"><span data-stu-id="f44f4-148">record</span></span>  
<span data-ttu-id="f44f4-149">結果を含むレコード バッファ (オプション)。</span><span class="sxs-lookup"><span data-stu-id="f44f4-149">The record buffer that will contain the result; optional.</span></span>

### <a name="return-value---first"></a><span data-ttu-id="f44f4-150">戻り値 - first</span><span class="sxs-lookup"><span data-stu-id="f44f4-150">Return Value - first</span></span>

<span data-ttu-id="f44f4-151">メソッドが成功する場合は true。レコードが存在しない場合は false。</span><span class="sxs-lookup"><span data-stu-id="f44f4-151">true if the method succeeds; false if no records exist.</span></span>

## <a name="method-get"></a><span data-ttu-id="f44f4-152">メソッド get</span><span class="sxs-lookup"><span data-stu-id="f44f4-152">Method get</span></span>

<span data-ttu-id="f44f4-153">現在の位置、または指定された位置のレコードを、指定されたレコード バッファーにコピーします。ただし、ポインタの位置には影響しません。</span><span class="sxs-lookup"><span data-stu-id="f44f4-153">Copies the record at the current position or the specified position to the provided record buffer, without affecting the pointer position.</span></span>

```xpp
public boolean get(Common record, [int index])
```

### <a name="parameters---get"></a><span data-ttu-id="f44f4-154">パラメーター - get</span><span class="sxs-lookup"><span data-stu-id="f44f4-154">Parameters - get</span></span>

<span data-ttu-id="f44f4-155">記録</span><span class="sxs-lookup"><span data-stu-id="f44f4-155">record</span></span>  
<span data-ttu-id="f44f4-156">現在のレコードが取得されていない場合に取得するリスト内のレコードの番号 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="f44f4-156">The number of the record in the list to retrieve if the current record is not being retrieved; optional.</span></span>

<!-- -->

<span data-ttu-id="f44f4-157">指数</span><span class="sxs-lookup"><span data-stu-id="f44f4-157">index</span></span>  
<span data-ttu-id="f44f4-158">現在のレコードが取得されていない場合に取得するリスト内のレコードの番号 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="f44f4-158">The number of the record in the list to retrieve if the current record is not being retrieved; optional.</span></span>

### <a name="return-value---get"></a><span data-ttu-id="f44f4-159">戻り値 - get</span><span class="sxs-lookup"><span data-stu-id="f44f4-159">Return Value - get</span></span>

<span data-ttu-id="f44f4-160">レコードを取得できる場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="f44f4-160">true if a record could be retrieved; otherwise, false.</span></span>

## <a name="method-ins"></a><span data-ttu-id="f44f4-161">メソッド ins</span><span class="sxs-lookup"><span data-stu-id="f44f4-161">Method ins</span></span>

<span data-ttu-id="f44f4-162">リストの最後にレコードを挿入します。</span><span class="sxs-lookup"><span data-stu-id="f44f4-162">Inserts a record at the end of a list.</span></span>

```xpp
public int ins(Common record)
```

### <a name="parameters---ins"></a><span data-ttu-id="f44f4-163">パラメーター - ins</span><span class="sxs-lookup"><span data-stu-id="f44f4-163">Parameters - ins</span></span>

<span data-ttu-id="f44f4-164">記録</span><span class="sxs-lookup"><span data-stu-id="f44f4-164">record</span></span>  
<span data-ttu-id="f44f4-165">挿入するレコードを保持するために使用するレコード バッファ。</span><span class="sxs-lookup"><span data-stu-id="f44f4-165">The record buffer that is used to hold the record to insert.</span></span>

### <a name="return-value---ins"></a><span data-ttu-id="f44f4-166">戻り値 - ins</span><span class="sxs-lookup"><span data-stu-id="f44f4-166">Return Value - ins</span></span>

<span data-ttu-id="f44f4-167">リスト内の要素の数。</span><span class="sxs-lookup"><span data-stu-id="f44f4-167">The number of elements in the list.</span></span>

## <a name="method-last"></a><span data-ttu-id="f44f4-168">メソッド last</span><span class="sxs-lookup"><span data-stu-id="f44f4-168">Method last</span></span>

<span data-ttu-id="f44f4-169">最後のレコードにリストを配置し、レコードを指定されたレコード バッファにコピーします。</span><span class="sxs-lookup"><span data-stu-id="f44f4-169">Puts the list at the last record and copies the record to the specified record buffer.</span></span>

```xpp
public boolean last([Common record])
```

### <a name="parameters---last"></a><span data-ttu-id="f44f4-170">パラメーター - last</span><span class="sxs-lookup"><span data-stu-id="f44f4-170">Parameters - last</span></span>

<span data-ttu-id="f44f4-171">記録</span><span class="sxs-lookup"><span data-stu-id="f44f4-171">record</span></span>  
<span data-ttu-id="f44f4-172">取得されたレコードを保持するために使用するレコード バッファ、オプション。</span><span class="sxs-lookup"><span data-stu-id="f44f4-172">A record buffer that is used to hold the record that is retrieved; optional.</span></span>

### <a name="return-value---last"></a><span data-ttu-id="f44f4-173">戻り値 - last</span><span class="sxs-lookup"><span data-stu-id="f44f4-173">Return Value - last</span></span>

<span data-ttu-id="f44f4-174">メソッドが成功する場合は true。リスト内にレコードが存在しない場合は false。</span><span class="sxs-lookup"><span data-stu-id="f44f4-174">true if the method succeeds; false if there are no records in the list.</span></span>

## <a name="method-len"></a><span data-ttu-id="f44f4-175">メソッド len</span><span class="sxs-lookup"><span data-stu-id="f44f4-175">Method len</span></span>

<span data-ttu-id="f44f4-176">リスト内の現在のレコード数を返します。</span><span class="sxs-lookup"><span data-stu-id="f44f4-176">Returns the current number of records in the list.</span></span>

```xpp
public int len()
```

### <a name="return-value---len"></a><span data-ttu-id="f44f4-177">戻り値 - len</span><span class="sxs-lookup"><span data-stu-id="f44f4-177">Return Value - len</span></span>

<span data-ttu-id="f44f4-178">リスト内のレコードの数。</span><span class="sxs-lookup"><span data-stu-id="f44f4-178">The number of records in the list.</span></span>

## <a name="method-next"></a><span data-ttu-id="f44f4-179">メソッド next</span><span class="sxs-lookup"><span data-stu-id="f44f4-179">Method next</span></span>

<span data-ttu-id="f44f4-180">次のレコードにカーソルを置き、指定されたバッファーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="f44f4-180">Puts the pointer on the next record and copies it to the provided buffer.</span></span>

```xpp
public boolean next([Common record])
```

### <a name="parameters---next"></a><span data-ttu-id="f44f4-181">パラメーター - next</span><span class="sxs-lookup"><span data-stu-id="f44f4-181">Parameters - next</span></span>

<span data-ttu-id="f44f4-182">記録</span><span class="sxs-lookup"><span data-stu-id="f44f4-182">record</span></span>  
<span data-ttu-id="f44f4-183">ポジションにあるレコードと同じ型のレコード バッファ (オプション)。</span><span class="sxs-lookup"><span data-stu-id="f44f4-183">The record buffer of same type as the record at the position; optional.</span></span>

### <a name="return-value---next"></a><span data-ttu-id="f44f4-184">戻り値 - next</span><span class="sxs-lookup"><span data-stu-id="f44f4-184">Return Value - next</span></span>

<span data-ttu-id="f44f4-185">メソッドが成功する場合は true。さらにレコードが存在しない場合は false。</span><span class="sxs-lookup"><span data-stu-id="f44f4-185">true if the method succeeds; false if there are no more records.</span></span>

## <a name="method-peek"></a><span data-ttu-id="f44f4-186">メソッド peek</span><span class="sxs-lookup"><span data-stu-id="f44f4-186">Method peek</span></span>

<span data-ttu-id="f44f4-187">リスト内の現在の位置のレコードを取得します。</span><span class="sxs-lookup"><span data-stu-id="f44f4-187">Retrieves the record at the current position in the list.</span></span>

```xpp
public Common peek()
```

### <a name="return-value---peek"></a><span data-ttu-id="f44f4-188">戻り値 - peek</span><span class="sxs-lookup"><span data-stu-id="f44f4-188">Return Value - peek</span></span>

<span data-ttu-id="f44f4-189">レコードが見つかった場合のレコード バッファ。</span><span class="sxs-lookup"><span data-stu-id="f44f4-189">A record buffer if the record is found.</span></span>

## <a name="method-prev"></a><span data-ttu-id="f44f4-190">メソッド prev</span><span class="sxs-lookup"><span data-stu-id="f44f4-190">Method prev</span></span>

<span data-ttu-id="f44f4-191">リスト内の前のレコードにポインターを配置し、レコードを指定されたバッファーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="f44f4-191">Puts the pointer on the previous record in the list and copies the record to the specified buffer.</span></span>

```xpp
public boolean prev([Common record])
```

### <a name="parameters---prev"></a><span data-ttu-id="f44f4-192">パラメーター - prev</span><span class="sxs-lookup"><span data-stu-id="f44f4-192">Parameters - prev</span></span>

<span data-ttu-id="f44f4-193">記録</span><span class="sxs-lookup"><span data-stu-id="f44f4-193">record</span></span>  
<span data-ttu-id="f44f4-194">コピーするレコードと同じ型のレコード バッファ (オプション)。</span><span class="sxs-lookup"><span data-stu-id="f44f4-194">The record buffer of the same type as the record to copy; optional.</span></span>

### <a name="return-value---prev"></a><span data-ttu-id="f44f4-195">戻り値 - prev</span><span class="sxs-lookup"><span data-stu-id="f44f4-195">Return Value - prev</span></span>

<span data-ttu-id="f44f4-196">ポインターが最初のレコード上にない場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="f44f4-196">true if the pointer is not at the first record; otherwise, false.</span></span>

## <a name="method-new"></a><span data-ttu-id="f44f4-197">メソッド new</span><span class="sxs-lookup"><span data-stu-id="f44f4-197">Method new</span></span>

<span data-ttu-id="f44f4-198">RecordLinkList クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="f44f4-198">Initializes a new instance of the RecordLinkList class.</span></span>

```xpp
public void new()
```

