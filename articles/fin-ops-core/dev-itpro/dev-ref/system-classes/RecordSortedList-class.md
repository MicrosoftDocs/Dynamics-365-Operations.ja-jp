---
title: RecordSortedList クラス
description: このトピックでは、RecordSortedList クラスについて説明します。
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
ms.openlocfilehash: 75c8a052dd11c6e69b266c0e656d551b8059ff8c
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502854"
---
# <a name="class-recordsortedlist"></a><span data-ttu-id="64131-103">クラス RecordSortedList</span><span class="sxs-lookup"><span data-stu-id="64131-103">Class RecordSortedList</span></span>

[!include [banner](../../includes/banner.md)]

```xpp
class RecordSortedList extends Object
```

<span data-ttu-id="64131-104">RecordSortedList クラスは、1 回のデータベース アクセスで複数のレコードを挿入します。</span><span class="sxs-lookup"><span data-stu-id="64131-104">The RecordSortedList class inserts multiple records in a single database trip.</span></span>

## <a name="remarks"></a><span data-ttu-id="64131-105">備考</span><span class="sxs-lookup"><span data-stu-id="64131-105">Remarks</span></span>

<span data-ttu-id="64131-106">特定のテーブルのデータのサブセットが必要で、現在インデックスとして存在しない順序でソートする場合は、RecordSortedList を使用します。</span><span class="sxs-lookup"><span data-stu-id="64131-106">Use RecordSortedList when you want a subset of data from a particular table, and you want it sorted in an order that does not currently exist as an index.</span></span> <span data-ttu-id="64131-107">RecordSortedList オブジェクトは、1 つのテーブルからのレコードを保有します。</span><span class="sxs-lookup"><span data-stu-id="64131-107">A RecordSortedList object holds records from a single table.</span></span> <span data-ttu-id="64131-108">リストには、sortOrder メソッドを使用して表示されるフィールドによって定義される一意のキーがあります。</span><span class="sxs-lookup"><span data-stu-id="64131-108">The list has a unique key that is defined by the fields listed by using the sortOrder method.</span></span> <span data-ttu-id="64131-109">レコードは、挿入時に自動的に並べ替えられます。並べ替え順序に挿入する必要はありません。</span><span class="sxs-lookup"><span data-stu-id="64131-109">Records are automatically sorted as they are inserted, they do not have to be inserted in sort sequence.</span></span> <span data-ttu-id="64131-110">RecordSortedList オブジェクトは、結果セットをパラメーターとして渡すのに特に役立ちます。RecordSortedList オブジェクトのサイズの制限はありませんが、完全にメモリ ベースであるため、潜在的なメモリ消費の問題があります。</span><span class="sxs-lookup"><span data-stu-id="64131-110">RecordSortedList objects are particularly useful for passing a result-set as a parameter There is no limit to the size of a RecordSortedList object, but they are completely memory-based, so there are potential memory consumption problems.</span></span> <span data-ttu-id="64131-111">InsertDatabase メソッドを呼び出す前に、RecordSortedList オブジェクトがサーバーにある必要があります。</span><span class="sxs-lookup"><span data-stu-id="64131-111">RecordSortedList objects must be server-located before the insertDatabase method can be called.</span></span> <span data-ttu-id="64131-112">それ以外の場合は、例外がスローされます。</span><span class="sxs-lookup"><span data-stu-id="64131-112">Otherwise, an exception is thrown.</span></span> <span data-ttu-id="64131-113">レコード レベル セキュリティ (RLS) は、RecordSortedList クラスによって適用されることはできません。</span><span class="sxs-lookup"><span data-stu-id="64131-113">Record level security (RLS) cannot be applied by the RecordSortedList class.</span></span> <span data-ttu-id="64131-114">RLS は、RecordInsertList クラスによって適用されます。</span><span class="sxs-lookup"><span data-stu-id="64131-114">RLS is applied by the RecordInsertList class).</span></span> <span data-ttu-id="64131-115">次のような状況では、一時テーブルよりも RecordSortedList を使用します。</span><span class="sxs-lookup"><span data-stu-id="64131-115">Use a RecordSortedList in preference to a temporary table in the following situations:</span></span>

-   <span data-ttu-id="64131-116">並べ替え順序が 1 つだけ必要です。</span><span class="sxs-lookup"><span data-stu-id="64131-116">Only one sort order is needed.</span></span>
-   <span data-ttu-id="64131-117">レコードの数は (メモリの問題を避けるために) 高すぎるということはありません。</span><span class="sxs-lookup"><span data-stu-id="64131-117">The number of records is not too high (to avoid memory problems).</span></span>

<span data-ttu-id="64131-118">一時テーブル、RecordSortedList オブジェクトと比較して:</span><span class="sxs-lookup"><span data-stu-id="64131-118">Compared to temporary tables, RecordSortedList objects:</span></span>

-   <span data-ttu-id="64131-119">時間が短縮されます。</span><span class="sxs-lookup"><span data-stu-id="64131-119">Are faster.</span></span>
-   <span data-ttu-id="64131-120">ディスク ベースではありません。</span><span class="sxs-lookup"><span data-stu-id="64131-120">Are not disk-based.</span></span>
-   <span data-ttu-id="64131-121">1 つのインデックスがあるのみ</span><span class="sxs-lookup"><span data-stu-id="64131-121">Only have one index.</span></span>
-   <span data-ttu-id="64131-122">フォームでは使用できません。</span><span class="sxs-lookup"><span data-stu-id="64131-122">Cannot be used in forms.</span></span>
-   <span data-ttu-id="64131-123">読み取りごとにクライアントとサーバー (グループ化された) の間で呼び出しが必要です。</span><span class="sxs-lookup"><span data-stu-id="64131-123">Require a call between the client and server per (grouped) read.</span></span>

## <a name="examples"></a><span data-ttu-id="64131-124">例</span><span class="sxs-lookup"><span data-stu-id="64131-124">Examples</span></span>

## <a name="methods"></a><span data-ttu-id="64131-125">メソッド</span><span class="sxs-lookup"><span data-stu-id="64131-125">Methods</span></span>

| <span data-ttu-id="64131-126">方法</span><span class="sxs-lookup"><span data-stu-id="64131-126">Method</span></span>                                                        | <span data-ttu-id="64131-127">説明</span><span class="sxs-lookup"><span data-stu-id="64131-127">Description</span></span>                                                                                                                                                          |
|---------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="64131-128">public boolean del(Common record)</span><span class="sxs-lookup"><span data-stu-id="64131-128">public boolean del(Common record)</span></span>                             | <span data-ttu-id="64131-129">recordBuffer のキー フィールドと一致するキーを持つレコードを recordSortedList から削除します。</span><span class="sxs-lookup"><span data-stu-id="64131-129">Removes a record that has a key that matches the key fields in the recordBuffer from the recordSortedList.</span></span>                                                           |
| <span data-ttu-id="64131-130">public boolean find(Common record)</span><span class="sxs-lookup"><span data-stu-id="64131-130">public boolean find(Common record)</span></span>                            | <span data-ttu-id="64131-131">レコード バッファーを、レコード バッファーの主なフィールドに一致するキーを持つレコードの内容に設定し、リストを返されるレコードに配置します。</span><span class="sxs-lookup"><span data-stu-id="64131-131">Sets the record buffer to the contents of the record that has a key that matches the key fields in the record buffer, and positions the list to the record returned.</span></span> |
| <span data-ttu-id="64131-132">public boolean first(Common record)</span><span class="sxs-lookup"><span data-stu-id="64131-132">public boolean first(Common record)</span></span>                           | <span data-ttu-id="64131-133">リストをリスト内の最初のレコードに配置し、その内容をレコード バッファーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="64131-133">Positions the list to the first record in the list, and copies its contents to the record buffer.</span></span>                                                                    |
| <span data-ttu-id="64131-134">public boolean ins(Common record, \[boolean updateIfExists\])</span><span class="sxs-lookup"><span data-stu-id="64131-134">public boolean ins(Common record, \[boolean updateIfExists\])</span></span> | <span data-ttu-id="64131-135">重複していない場合に、RecordSortedList に新しいレコードを挿入します。</span><span class="sxs-lookup"><span data-stu-id="64131-135">Inserts a new record in a RecordSortedList, unless it is a duplicate.</span></span>                                                                                                |
| <span data-ttu-id="64131-136">public int len()</span><span class="sxs-lookup"><span data-stu-id="64131-136">public int len()</span></span>                                              | <span data-ttu-id="64131-137">RecordSortedList オブジェクトの現在のレコード数を返します。</span><span class="sxs-lookup"><span data-stu-id="64131-137">Returns the current number of records in a RecordSortedList object.</span></span>                                                                                                  |
| <span data-ttu-id="64131-138">public boolean next(Common record)</span><span class="sxs-lookup"><span data-stu-id="64131-138">public boolean next(Common record)</span></span>                            | <span data-ttu-id="64131-139">レコード バッファーを recordSortedList の次のレコードの内容に設定し、リストを返されるレコードに配置します。</span><span class="sxs-lookup"><span data-stu-id="64131-139">Sets the record buffer to the contents of the next record in the recordSortedList and positions the list to the record returned.</span></span>                                     |
| <span data-ttu-id="64131-140">public void new(TableId tableId, \[Common table\])</span><span class="sxs-lookup"><span data-stu-id="64131-140">public void new(TableId tableId, \[Common table\])</span></span>            | <span data-ttu-id="64131-141">Object クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="64131-141">Initializes a new instance of the Object class.</span></span>                                                                                                                      |
| <span data-ttu-id="64131-142">public void sortOrder(FieldId fieldId, VarArg )</span><span class="sxs-lookup"><span data-stu-id="64131-142">public void sortOrder(FieldId fieldId, VarArg )</span></span>               | <span data-ttu-id="64131-143">レコードが並べ替えされるフィールドを定義します。</span><span class="sxs-lookup"><span data-stu-id="64131-143">Defines the fields on which the records are sorted.</span></span>                                                                                                                  |
| <span data-ttu-id="64131-144">public void sortOrderFromContainer(container container)</span><span class="sxs-lookup"><span data-stu-id="64131-144">public void sortOrderFromContainer(container container)</span></span>       | <span data-ttu-id="64131-145">レコードが並べ替えされるフィールドを定義します。</span><span class="sxs-lookup"><span data-stu-id="64131-145">Defines the fields on which the records are sorted.</span></span>                                                                                                                  |
| <span data-ttu-id="64131-146">public void insertDatabase(\[Connection connection\])</span><span class="sxs-lookup"><span data-stu-id="64131-146">public void insertDatabase(\[Connection connection\])</span></span>         | <span data-ttu-id="64131-147">データベースに 1 回に複数のレコードを挿入します。</span><span class="sxs-lookup"><span data-stu-id="64131-147">Inserts multiple records on a single trip to the database.</span></span>                                                                                                           |

## <a name="method-del"></a><span data-ttu-id="64131-148">メソッド del</span><span class="sxs-lookup"><span data-stu-id="64131-148">Method del</span></span>

<span data-ttu-id="64131-149">recordBuffer のキー フィールドと一致するキーを持つレコードを recordSortedList から削除します。</span><span class="sxs-lookup"><span data-stu-id="64131-149">Removes a record that has a key that matches the key fields in the recordBuffer from the recordSortedList.</span></span>

```xpp
public boolean del(Common record)
```

### <a name="parameters---del"></a><span data-ttu-id="64131-150">パラメーター - del</span><span class="sxs-lookup"><span data-stu-id="64131-150">Parameters - del</span></span>

<span data-ttu-id="64131-151">記録</span><span class="sxs-lookup"><span data-stu-id="64131-151">record</span></span>  
<span data-ttu-id="64131-152">削除するレコードのキーの値を含むレコード バッファ。</span><span class="sxs-lookup"><span data-stu-id="64131-152">A record buffer that contains the key values of the record to be deleted.</span></span>

### <a name="return-value---del"></a><span data-ttu-id="64131-153">戻り値 - del</span><span class="sxs-lookup"><span data-stu-id="64131-153">Return Value - del</span></span>

<span data-ttu-id="64131-154">レコードが削除された場合は true。それ以外の場合は false。</span><span class="sxs-lookup"><span data-stu-id="64131-154">true if a record was removed; otherwise false.</span></span>

## <a name="method-find"></a><span data-ttu-id="64131-155">メソッド find</span><span class="sxs-lookup"><span data-stu-id="64131-155">Method find</span></span>

<span data-ttu-id="64131-156">レコード バッファーを、レコード バッファーの主なフィールドに一致するキーを持つレコードの内容に設定し、リストを返されるレコードに配置します。</span><span class="sxs-lookup"><span data-stu-id="64131-156">Sets the record buffer to the contents of the record that has a key that matches the key fields in the record buffer, and positions the list to the record returned.</span></span>

```xpp
public boolean find(Common record)
```

### <a name="parameters---find"></a><span data-ttu-id="64131-157">パラメーター - find</span><span class="sxs-lookup"><span data-stu-id="64131-157">Parameters - find</span></span>

<span data-ttu-id="64131-158">記録</span><span class="sxs-lookup"><span data-stu-id="64131-158">record</span></span>  
<span data-ttu-id="64131-159">検索するキーの値を含むレコード バッファ。</span><span class="sxs-lookup"><span data-stu-id="64131-159">A record buffer that contains the key values to be searched for.</span></span> <span data-ttu-id="64131-160">見つかったレコードは、レコード バッファのコンテンツを置き換えます。</span><span class="sxs-lookup"><span data-stu-id="64131-160">The record found will replace the contents of the record buffer.</span></span>

### <a name="return-value---find"></a><span data-ttu-id="64131-161">戻り値 - find</span><span class="sxs-lookup"><span data-stu-id="64131-161">Return Value - find</span></span>

<span data-ttu-id="64131-162">レコードが見つかる場合は true。それ以外の場合は false。</span><span class="sxs-lookup"><span data-stu-id="64131-162">true if a record is found; otherwise false.</span></span>

## <a name="method-first"></a><span data-ttu-id="64131-163">メソッド first</span><span class="sxs-lookup"><span data-stu-id="64131-163">Method first</span></span>

<span data-ttu-id="64131-164">リストをリスト内の最初のレコードに配置し、その内容をレコード バッファーにコピーします。</span><span class="sxs-lookup"><span data-stu-id="64131-164">Positions the list to the first record in the list, and copies its contents to the record buffer.</span></span>

```xpp
public boolean first(Common record)
```

### <a name="parameters---first"></a><span data-ttu-id="64131-165">パラメーター - first</span><span class="sxs-lookup"><span data-stu-id="64131-165">Parameters - first</span></span>

<span data-ttu-id="64131-166">記録</span><span class="sxs-lookup"><span data-stu-id="64131-166">record</span></span>  
<span data-ttu-id="64131-167">リストの最初のレコードに含まれるレコード バッファ。</span><span class="sxs-lookup"><span data-stu-id="64131-167">A record buffer to contain first record in list.</span></span>

### <a name="return-value---first"></a><span data-ttu-id="64131-168">戻り値 - first</span><span class="sxs-lookup"><span data-stu-id="64131-168">Return Value - first</span></span>

<span data-ttu-id="64131-169">メソッドが成功する場合は true。それ以外の場合は false。</span><span class="sxs-lookup"><span data-stu-id="64131-169">true if the method is successful; otherwise false.</span></span>

## <a name="method-ins"></a><span data-ttu-id="64131-170">メソッド ins</span><span class="sxs-lookup"><span data-stu-id="64131-170">Method ins</span></span>

<span data-ttu-id="64131-171">重複していない場合に、RecordSortedList に新しいレコードを挿入します。</span><span class="sxs-lookup"><span data-stu-id="64131-171">Inserts a new record in a RecordSortedList, unless it is a duplicate.</span></span>

```xpp
public boolean ins(Common record, [boolean updateIfExists])
```

### <a name="parameters---ins"></a><span data-ttu-id="64131-172">パラメーター - ins</span><span class="sxs-lookup"><span data-stu-id="64131-172">Parameters - ins</span></span>

<span data-ttu-id="64131-173">記録</span><span class="sxs-lookup"><span data-stu-id="64131-173">record</span></span>  
<span data-ttu-id="64131-174">重複するレコードを破棄または置き換えるかどうか。省略可能です。</span><span class="sxs-lookup"><span data-stu-id="64131-174">Whether to discard or replace duplicate records; optional.</span></span> <span data-ttu-id="64131-175">False の場合、重複している場合に、新しいレコードが破棄されます。</span><span class="sxs-lookup"><span data-stu-id="64131-175">If false, the new record will be discarded if it is a duplicate.</span></span> <span data-ttu-id="64131-176">True の場合、新しいレコードが重複している場合、既存のレコードが置き換えられます。</span><span class="sxs-lookup"><span data-stu-id="64131-176">If true, the new record will replace an existing record if it is a duplicate.</span></span>

<!-- -->

<span data-ttu-id="64131-177">updateIfExists</span><span class="sxs-lookup"><span data-stu-id="64131-177">updateIfExists</span></span>  
<span data-ttu-id="64131-178">重複するレコードを破棄または置き換えるかどうか。省略可能です。</span><span class="sxs-lookup"><span data-stu-id="64131-178">Whether to discard or replace duplicate records; optional.</span></span> <span data-ttu-id="64131-179">False の場合、重複している場合に、新しいレコードが破棄されます。</span><span class="sxs-lookup"><span data-stu-id="64131-179">If false, the new record will be discarded if it is a duplicate.</span></span> <span data-ttu-id="64131-180">True の場合、新しいレコードが重複している場合、既存のレコードが置き換えられます。</span><span class="sxs-lookup"><span data-stu-id="64131-180">If true, the new record will replace an existing record if it is a duplicate.</span></span>

### <a name="return-value---ins"></a><span data-ttu-id="64131-181">戻り値 - ins</span><span class="sxs-lookup"><span data-stu-id="64131-181">Return Value - ins</span></span>

<span data-ttu-id="64131-182">レコードが追加または置換された場合は true。それ以外の場合は false。</span><span class="sxs-lookup"><span data-stu-id="64131-182">true if the record was added or replaced; otherwise false.</span></span>

## <a name="method-len"></a><span data-ttu-id="64131-183">メソッド len</span><span class="sxs-lookup"><span data-stu-id="64131-183">Method len</span></span>

<span data-ttu-id="64131-184">RecordSortedList オブジェクトの現在のレコード数を返します。</span><span class="sxs-lookup"><span data-stu-id="64131-184">Returns the current number of records in a RecordSortedList object.</span></span>

```xpp
public int len()
```

### <a name="return-value---len"></a><span data-ttu-id="64131-185">戻り値 - len</span><span class="sxs-lookup"><span data-stu-id="64131-185">Return Value - len</span></span>

<span data-ttu-id="64131-186">リスト内の現在のレコード数。</span><span class="sxs-lookup"><span data-stu-id="64131-186">The current number of records in the list.</span></span>

## <a name="method-next"></a><span data-ttu-id="64131-187">メソッド next</span><span class="sxs-lookup"><span data-stu-id="64131-187">Method next</span></span>

<span data-ttu-id="64131-188">レコード バッファーを recordSortedList の次のレコードの内容に設定し、リストを返されるレコードに配置します。</span><span class="sxs-lookup"><span data-stu-id="64131-188">Sets the record buffer to the contents of the next record in the recordSortedList and positions the list to the record returned.</span></span>

```xpp
public boolean next(Common record)
```

### <a name="parameters---next"></a><span data-ttu-id="64131-189">パラメーター - next</span><span class="sxs-lookup"><span data-stu-id="64131-189">Parameters - next</span></span>

<span data-ttu-id="64131-190">記録</span><span class="sxs-lookup"><span data-stu-id="64131-190">record</span></span>  
<span data-ttu-id="64131-191">結果を受信するレコード バッファ。</span><span class="sxs-lookup"><span data-stu-id="64131-191">A record buffer to receive the result.</span></span>

### <a name="return-value---next"></a><span data-ttu-id="64131-192">戻り値 - next</span><span class="sxs-lookup"><span data-stu-id="64131-192">Return Value - next</span></span>

<span data-ttu-id="64131-193">操作が成功した場合は true。それ以外の場合は false。</span><span class="sxs-lookup"><span data-stu-id="64131-193">true if the operation was successful; otherwise false.</span></span>

## <a name="method-new"></a><span data-ttu-id="64131-194">メソッド new</span><span class="sxs-lookup"><span data-stu-id="64131-194">Method new</span></span>

<span data-ttu-id="64131-195">Object クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="64131-195">Initializes a new instance of the Object class.</span></span>

```xpp
public void new(TableId tableId, [Common table])
```

### <a name="parameters---new"></a><span data-ttu-id="64131-196">パラメーター - new</span><span class="sxs-lookup"><span data-stu-id="64131-196">Parameters - new</span></span>

<span data-ttu-id="64131-197">tableId</span><span class="sxs-lookup"><span data-stu-id="64131-197">tableId</span></span>  

<!-- -->

<span data-ttu-id="64131-198">テーブル</span><span class="sxs-lookup"><span data-stu-id="64131-198">table</span></span>  

### <a name="remarks---new"></a><span data-ttu-id="64131-199">備考 - new</span><span class="sxs-lookup"><span data-stu-id="64131-199">Remarks - new</span></span>

<span data-ttu-id="64131-200">リストには、tableId パラメーターで指定された型のレコードを含めることができます。</span><span class="sxs-lookup"><span data-stu-id="64131-200">The list can contain records of the type that is specified by the tableId parameter.</span></span>

### <a name="examples---new"></a><span data-ttu-id="64131-201">例 - new</span><span class="sxs-lookup"><span data-stu-id="64131-201">Examples - new</span></span>

<span data-ttu-id="64131-202">次の例では、RecordInsertList オブジェクトを使用して、1 つのデータベース操作に 3 つのレコードを挿入します。</span><span class="sxs-lookup"><span data-stu-id="64131-202">The following example uses a RecordInsertList object to insert three records in a single database operation.</span></span>

```xpp
{ 
    RecordSortedList recordSortedList; 
    CustTable        custTable; 
    recordSortedList = new RecordSortedList(tablenum(CustTable)); 
    recordSortedList.sortOrder(fieldnum(custTable,AccountNum)); 
    ttsbegin; 
    // Prepare record #1 for insertion. 
    custTable.AccountNum = '1000'; 
    custTable.CreditMax = 10000.0; 
    recordSortedList.ins(custTable); 
    // Prepare record #2 for insertion. 
    custTable.AccountNum = '2000'; 
    custTable.CreditMax = 500.0; 
    recordSortedList.ins(custTable); 
    // Prepare record #3 for insertion. 
    custTable.AccountNum = '3000'; 
    custTable.CreditMax = 9999999.9; 
    recordSortedList.ins(custTable); 
    // All 3 records inserted in one database operation. 
    recordSortedList.insertDatabase();   
    ttscommit; 
}
```

## <a name="method-sortorder"></a><span data-ttu-id="64131-203">メソッド sortOrder</span><span class="sxs-lookup"><span data-stu-id="64131-203">Method sortOrder</span></span>

<span data-ttu-id="64131-204">レコードが並べ替えされるフィールドを定義します。</span><span class="sxs-lookup"><span data-stu-id="64131-204">Defines the fields on which the records are sorted.</span></span>

```xpp
public void sortOrder(FieldId fieldId, VarArg )
```

### <a name="parameters---sortorder"></a><span data-ttu-id="64131-205">パラメーター - sortOrder</span><span class="sxs-lookup"><span data-stu-id="64131-205">Parameters - sortOrder</span></span>

<span data-ttu-id="64131-206">fieldId</span><span class="sxs-lookup"><span data-stu-id="64131-206">fieldId</span></span>  

<!-- -->


### <a name="remarks---sortorder"></a><span data-ttu-id="64131-207">備考 - sortOrder</span><span class="sxs-lookup"><span data-stu-id="64131-207">Remarks - sortOrder</span></span>

<span data-ttu-id="64131-208">並べ替える 1 つまたはそれ以上のフィールドを指定することができます。</span><span class="sxs-lookup"><span data-stu-id="64131-208">You can specify one or more fields to sort on.</span></span> <span data-ttu-id="64131-209">このメソッドは、RecordSortedList クラスの同じインスタンスに対して 1 回だけ呼び出すことができます。</span><span class="sxs-lookup"><span data-stu-id="64131-209">This method can only be called one time on the same instance of the RecordSortedList class.</span></span> <span data-ttu-id="64131-210">設定した後は、並べ替え順序を変更することはできません。</span><span class="sxs-lookup"><span data-stu-id="64131-210">You cannot change the sorting order after it has been set.</span></span>

### <a name="examples---sortorder"></a><span data-ttu-id="64131-211">例 - sortOrder</span><span class="sxs-lookup"><span data-stu-id="64131-211">Examples - sortOrder</span></span>

<span data-ttu-id="64131-212">次の例では、DimensionSetRuleTable テーブル レコードのリストを作成し、SetId フィールドと HierarchyId フィールドの順に並べ替えます。</span><span class="sxs-lookup"><span data-stu-id="64131-212">The following example creates a list of DimensionSetRuleTable table records, and then sorts them by the SetId field, and then by the HierarchyId field.</span></span>

```xpp
static RecordSortedList initRulesList() 
{ 
    RecordSortedList list; 
    list = new RecordSortedList(tablenum(DimensionSetRuleTable)); 
    list.sortOrder( 
        fieldnum(DimensionSetRuleTable, SetId),  
        fieldnum(DimensionSetRuleTable, HierarchyId)); 
    return list; 
}
```

## <a name="method-sortorderfromcontainer"></a><span data-ttu-id="64131-213">メソッド sortOrderFromContainer</span><span class="sxs-lookup"><span data-stu-id="64131-213">Method sortOrderFromContainer</span></span>

<span data-ttu-id="64131-214">レコードが並べ替えされるフィールドを定義します。</span><span class="sxs-lookup"><span data-stu-id="64131-214">Defines the fields on which the records are sorted.</span></span>

```xpp
public void sortOrderFromContainer(container container)
```

### <a name="parameters---sortorderfromcontainer"></a><span data-ttu-id="64131-215">パラメーター - sortOrderFromContainer</span><span class="sxs-lookup"><span data-stu-id="64131-215">Parameters - sortOrderFromContainer</span></span>

<span data-ttu-id="64131-216">コンテナー</span><span class="sxs-lookup"><span data-stu-id="64131-216">container</span></span>  
<span data-ttu-id="64131-217">リストをソートする必要があるフィールド。</span><span class="sxs-lookup"><span data-stu-id="64131-217">The fields on which the list should be sorted.</span></span> <span data-ttu-id="64131-218">各フィールドがフィールド ID によって指定されました。たとえば、FieldNum 機能が使われます。</span><span class="sxs-lookup"><span data-stu-id="64131-218">Each field is specified by a field ID; for example, by using the FieldNum function.</span></span>

### <a name="remarks---sortorderfromcontainer"></a><span data-ttu-id="64131-219">備考 - sortOrderFromContainer</span><span class="sxs-lookup"><span data-stu-id="64131-219">Remarks - sortOrderFromContainer</span></span>

<span data-ttu-id="64131-220">フィールドの一覧をコンテナーに指定しない場合、RecordSortedList.sortOrder を使用します。</span><span class="sxs-lookup"><span data-stu-id="64131-220">If you do not have to supply the field list in a container, use RecordSortedList.sortOrder.</span></span>

## <a name="method-insertdatabase"></a><span data-ttu-id="64131-221">メソッド insertDatabase</span><span class="sxs-lookup"><span data-stu-id="64131-221">Method insertDatabase</span></span>

<span data-ttu-id="64131-222">データベースに 1 回に複数のレコードを挿入します。</span><span class="sxs-lookup"><span data-stu-id="64131-222">Inserts multiple records on a single trip to the database.</span></span>

```xpp
public void insertDatabase([Connection connection])
```

### <a name="parameters---insertdatabase"></a><span data-ttu-id="64131-223">パラメーター - insertDatabase</span><span class="sxs-lookup"><span data-stu-id="64131-223">Parameters - insertDatabase</span></span>

<span data-ttu-id="64131-224">connection</span><span class="sxs-lookup"><span data-stu-id="64131-224">connection</span></span>  

### <a name="remarks---insertdatabase"></a><span data-ttu-id="64131-225">備考 - insertDatabase</span><span class="sxs-lookup"><span data-stu-id="64131-225">Remarks - insertDatabase</span></span>

<span data-ttu-id="64131-226">呼び出しの後、リストのエントリは、RecordSortedList オブジェクトに残ります。</span><span class="sxs-lookup"><span data-stu-id="64131-226">After the call, the list entries remain in the RecordSortedList object.</span></span> <span data-ttu-id="64131-227">RecordSortedList クラスは、insertDatabase メソッドの呼び出し前にサーバーにある必要があります。それ以外の場合、例外が発生します。</span><span class="sxs-lookup"><span data-stu-id="64131-227">The RecordSortedList class must be located on the server before the insertDatabase method is called; otherwise, an exception is thrown.</span></span> <span data-ttu-id="64131-228">RecId およびその他のシステム管理フィールド値には、insertDatabase メソッド呼び出しが行われるまで値が割り当てられません。</span><span class="sxs-lookup"><span data-stu-id="64131-228">RecIds and other system-maintained fields are not assigned values until the insertDatabase method call is made.</span></span> <span data-ttu-id="64131-229">このメソッドは、次のいずれかの条件が満たされた場合、レコードごとの挿入に戻ります。</span><span class="sxs-lookup"><span data-stu-id="64131-229">The method reverts to a record by record insert if any of the following conditions are met:</span></span>

-   <span data-ttu-id="64131-230">テーブルは SQL ストアドではありません。</span><span class="sxs-lookup"><span data-stu-id="64131-230">The table is not SQL-stored.</span></span>
-   <span data-ttu-id="64131-231">テーブルの挿入メソッドがオーバーロードします。</span><span class="sxs-lookup"><span data-stu-id="64131-231">The insert method for the table is overloaded.</span></span>
-   <span data-ttu-id="64131-232">テーブルには、メモ フィールドまたはコンテナー フィールドが含まれます。</span><span class="sxs-lookup"><span data-stu-id="64131-232">The table includes memo or container fields.</span></span>

### <a name="examples---insertdatabase"></a><span data-ttu-id="64131-233">例 - insertDatabase</span><span class="sxs-lookup"><span data-stu-id="64131-233">Examples - insertDatabase</span></span>

<span data-ttu-id="64131-234">次の例は、1 つのデータベース操作に 3 つのレコードを挿入する方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="64131-234">The following example shows how to insert three records in a single database operation.</span></span>

```xpp
{ 
    RecordSortedList recordSortedList; 
    CustTable        custTable; 
    recordSortedList = new RecordSortedList(tablenum(CustTable)); 
    recordSortedList.sortOrder(fieldnum(custTable,AccountNum)); 
    ttsbegin; 
    // Prepare record #1 for insertion. 
    custTable.AccountNum = '1000'; 
    custTable.CreditMax = 10000.0; 
    recordSortedList.ins(custTable); 
    // Prepare record #2 for insertion. 
    custTable.AccountNum = '2000'; 
    custTable.CreditMax = 500.0; 
    recordSortedList.ins(custTable); 
    // Prepare record #3 for insertion. 
    custTable.AccountNum = '3000'; 
    custTable.CreditMax = 9999999.9; 
    recordSortedList.ins(custTable); 
    // All three records inserted in one database operation. 
    recordSortedList.insertDatabase();   
    ttscommit; 
}
```

