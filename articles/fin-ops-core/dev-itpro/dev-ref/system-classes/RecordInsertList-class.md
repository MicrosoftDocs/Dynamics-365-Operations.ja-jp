---
title: RecordInsertList クラス
description: このトピックでは、RecordInsertList クラスについて説明します。
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
ms.openlocfilehash: 6fb6d7818420113e7c5b2106857e93a4e1ee9ae8
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502856"
---
# <a name="class-recordinsertlist"></a><span data-ttu-id="eccc6-103">クラス RecordInsertList</span><span class="sxs-lookup"><span data-stu-id="eccc6-103">Class RecordInsertList</span></span>

[!include [banner](../../includes/banner.md)]

```xpp
class RecordInsertList extends Object
```

<span data-ttu-id="eccc6-104">RecordInsertList クラスは、カーネルで配列挿入機能を提供します。</span><span class="sxs-lookup"><span data-stu-id="eccc6-104">The RecordInsertList class provides array insertion capabilities in the kernel.</span></span>

## <a name="remarks"></a><span data-ttu-id="eccc6-105">備考</span><span class="sxs-lookup"><span data-stu-id="eccc6-105">Remarks</span></span>

<span data-ttu-id="eccc6-106">このクラスを使用すると、一度に複数のレコードをデータベースに挿入できます。これにより、アプリケーションとデータベース間の通信が減少します。</span><span class="sxs-lookup"><span data-stu-id="eccc6-106">This class lets you insert more than one record into the database at a time, which reduces communication between the application and the database.</span></span> <span data-ttu-id="eccc6-107">レコードは、カーネルが適切と判断したときに挿入されますが、insertDatabase、add、insertDatabase メソッドの呼び出し以前に挿入されます。</span><span class="sxs-lookup"><span data-stu-id="eccc6-107">Records are inserted only when the kernel finds the time appropriate, but they are inserted no later than the call to the insertDatabase, add, and insertDatabase methods.</span></span> <span data-ttu-id="eccc6-108">RecordInsertList.add および RecordInsertList.insertDatabase メソッドは、レコードが実際にいつ挿入されたかを追跡できるように、現在挿入されているレコードの累計数を返します。</span><span class="sxs-lookup"><span data-stu-id="eccc6-108">The RecordInsertList.add and RecordInsertList.insertDatabase methods return the accumulated number of records that are currently inserted, so that you can keep track of when the records are actually inserted.</span></span> <span data-ttu-id="eccc6-109">非 SQL ベースのテーブル (一時テーブルなど) を使用する場合、またはテーブルでの挿入方法が無効にされた (明示的に破棄されていない限り) 場合は、配列挿入操作が自動的に、従来のレコードごとの挿入に戻ります。</span><span class="sxs-lookup"><span data-stu-id="eccc6-109">The array insert operation automatically falls back to classic record-by-record inserts when non-SQL based tables are used (for example, temporary tables) or when the insert method on the table is overridden (unless it is explicitly discarded).</span></span> <span data-ttu-id="eccc6-110">RecordInsertList クラスは、RecordSortedList クラスに似ていますが、クライアント/サーバー サポートが組み込まれており (必要に応じて、ある層から別の層にデータをパッキングします)、RecordSortedList で使用できる並べ替え順序機能がありません。</span><span class="sxs-lookup"><span data-stu-id="eccc6-110">The RecordInsertList class resembles the RecordSortedList class, but it has built-in client/server support (it automatically packs data from one tier to another when this is required) and lacks the sort order features that are available in the RecordSortedList class.</span></span>

## <a name="examples"></a><span data-ttu-id="eccc6-111">例</span><span class="sxs-lookup"><span data-stu-id="eccc6-111">Examples</span></span>

<span data-ttu-id="eccc6-112">次の例では、RecordInsertList クラスを使用して ある BOM から 別の BOM に部品表 (BOM) をコピーします。</span><span class="sxs-lookup"><span data-stu-id="eccc6-112">The following example uses the RecordInsertList class to copy a bill of materials (BOM) from one BOM to another.</span></span>

```xpp
void copyBOM(BOMId _FromBOM, BOMId _ToBOM) 
{ 
    RecordInsertList BOMList; 
    BOM BOM, newBOM; 
    BOMList = new RecordInsertList(tableNum(BOM)); 
    while select BOM 
    where BOM.BOMId == _FromBOM 
    { 
        newBOM.data(BOM); 
        newBOM.BOMId = _ToBOM; 
        BOMList.add(newBOM); 
    } 
    BOMList.insertDatabase(); 
}
```

## <a name="methods"></a><span data-ttu-id="eccc6-113">メソッド</span><span class="sxs-lookup"><span data-stu-id="eccc6-113">Methods</span></span>

| <span data-ttu-id="eccc6-114">方法</span><span class="sxs-lookup"><span data-stu-id="eccc6-114">Method</span></span>                                                                                                                                                                                              | <span data-ttu-id="eccc6-115">説明</span><span class="sxs-lookup"><span data-stu-id="eccc6-115">Description</span></span>                                                                                       |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="eccc6-116">public int add(Common record)</span><span class="sxs-lookup"><span data-stu-id="eccc6-116">public int add(Common record)</span></span>                                                                                                                                                                       | <span data-ttu-id="eccc6-117">データベースへのその後の挿入のために、RecordInsertList オブジェクトにレコードを追加します。</span><span class="sxs-lookup"><span data-stu-id="eccc6-117">Adds a record to a RecordInsertList object for subsequent insertion into the database.</span></span>            |
| <span data-ttu-id="eccc6-118">public int insertDatabase()</span><span class="sxs-lookup"><span data-stu-id="eccc6-118">public int insertDatabase()</span></span>                                                                                                                                                                         | <span data-ttu-id="eccc6-119">現在の RecordInsertList オブジェクトにまだ挿入されていないすべてのレコードを挿入します。</span><span class="sxs-lookup"><span data-stu-id="eccc6-119">Inserts all records that have not already been inserted into the current RecordInsertList object.</span></span> |
| <span data-ttu-id="eccc6-120">public void new(TableId tableId, \[boolean skipInsertMethod\], \[boolean skipDatabaseLog\], \[boolean skipEvents\], \[boolean skipAosValidation\], \[boolean skipRLSValidation\], \[Common table\])</span><span class="sxs-lookup"><span data-stu-id="eccc6-120">public void new(TableId tableId, \[boolean skipInsertMethod\], \[boolean skipDatabaseLog\], \[boolean skipEvents\], \[boolean skipAosValidation\], \[boolean skipRLSValidation\], \[Common table\])</span></span> | <span data-ttu-id="eccc6-121">データベースに挿入するレコードを保持する新しいオブジェクトを作成します。</span><span class="sxs-lookup"><span data-stu-id="eccc6-121">Creates a new object to hold records for insertion into the database.</span></span>                             |

## <a name="method-add"></a><span data-ttu-id="eccc6-122">メソッド add</span><span class="sxs-lookup"><span data-stu-id="eccc6-122">Method add</span></span>

<span data-ttu-id="eccc6-123">データベースへのその後の挿入のために、RecordInsertList オブジェクトにレコードを追加します。</span><span class="sxs-lookup"><span data-stu-id="eccc6-123">Adds a record to a RecordInsertList object for subsequent insertion into the database.</span></span>

```xpp
public int add(Common record)
```

### <a name="parameters---add"></a><span data-ttu-id="eccc6-124">パラメーター - add</span><span class="sxs-lookup"><span data-stu-id="eccc6-124">Parameters - add</span></span>

<span data-ttu-id="eccc6-125">記録</span><span class="sxs-lookup"><span data-stu-id="eccc6-125">record</span></span>  
<span data-ttu-id="eccc6-126">クラスをインスタンス化するために使用される、同じ型のデータベース バッファです。</span><span class="sxs-lookup"><span data-stu-id="eccc6-126">A database buffer of the same type that is used to instantiate the class.</span></span>

### <a name="return-value---add"></a><span data-ttu-id="eccc6-127">戻り値 - add</span><span class="sxs-lookup"><span data-stu-id="eccc6-127">Return Value - add</span></span>

<span data-ttu-id="eccc6-128">レコードが正常にリストに追加されたかどうかを示す整数。</span><span class="sxs-lookup"><span data-stu-id="eccc6-128">An integer that indicates whether the record has been successfully added to the list.</span></span>

### <a name="remarks---add"></a><span data-ttu-id="eccc6-129">備考 - add</span><span class="sxs-lookup"><span data-stu-id="eccc6-129">Remarks - add</span></span>

<span data-ttu-id="eccc6-130">Add メソッドは、パフォーマンスの向上が見込まれる場合は常に、レコードをデータベースにフラッシュすることができます。</span><span class="sxs-lookup"><span data-stu-id="eccc6-130">The add method can flush records to the database whenever this will speed up performance.</span></span> <span data-ttu-id="eccc6-131">ただし、リスト内のすべてのレコードが挿入されることを保証するには、RecordInsertList.insertDatabase メソッドを使用します。</span><span class="sxs-lookup"><span data-stu-id="eccc6-131">However, to guarantee that all records in the list are inserted, use the RecordInsertList.insertDatabase method.</span></span>

### <a name="examples---add"></a><span data-ttu-id="eccc6-132">例 - add</span><span class="sxs-lookup"><span data-stu-id="eccc6-132">Examples - add</span></span>

<span data-ttu-id="eccc6-133">次の例では、RecordInsertList クラスを使用して BOM をある BOM から別の BOM にコピーします。</span><span class="sxs-lookup"><span data-stu-id="eccc6-133">The following example uses the RecordInsertList class to copy a BOM from one BOM to another.</span></span> <span data-ttu-id="eccc6-134">add メソッドを使用して、BOM 内のすべてのレコードが RecordInsertList オブジェクトに追加されてから、最後の呼び出しが insertDatabase メソッドに行われて、残りのすべてのレコードが挿入されます。</span><span class="sxs-lookup"><span data-stu-id="eccc6-134">The add method is used to add all the records in the BOM to the RecordInsertList object before a final call is made to the insertDatabase method to insert all remaining records.</span></span>

```xpp
void copyBOM(BOMId _FromBOM, BOMId _ToBOM) 
{ 
    RecordInsertList BOMList; 
    BOM BOM, newBOM; 
    BOMList = new RecordInsertList(tableNum(BOM)); 
    while select BOM 
    where BOM.BOMId == _FromBOM 
    { 
        newBOM.data(BOM); 
        newBOM.BOMId = _ToBOM; 
        BOMList.add(newBOM); 
    } 
    BOMList.insertDatabase(); 
}
```

## <a name="method-insertdatabase"></a><span data-ttu-id="eccc6-135">メソッド insertDatabase</span><span class="sxs-lookup"><span data-stu-id="eccc6-135">Method insertDatabase</span></span>

<span data-ttu-id="eccc6-136">現在の RecordInsertList オブジェクトにまだ挿入されていないすべてのレコードを挿入します。</span><span class="sxs-lookup"><span data-stu-id="eccc6-136">Inserts all records that have not already been inserted into the current RecordInsertList object.</span></span>

```xpp
public int insertDatabase()
```

### <a name="return-value---insertdatabase"></a><span data-ttu-id="eccc6-137">戻り値 - insertDatabase</span><span class="sxs-lookup"><span data-stu-id="eccc6-137">Return Value - insertDatabase</span></span>

<span data-ttu-id="eccc6-138">挿入されたレコードの合計数を表す整数。</span><span class="sxs-lookup"><span data-stu-id="eccc6-138">An integer that represents the total number of records that were inserted.</span></span>

### <a name="remarks---insertdatabase"></a><span data-ttu-id="eccc6-139">備考 - insertDatabase</span><span class="sxs-lookup"><span data-stu-id="eccc6-139">Remarks - insertDatabase</span></span>

<span data-ttu-id="eccc6-140">RecordInsertList.add メソッドは、パフォーマンスの向上が見込まれる場合は常に、レコードをデータベースにフラッシュします。</span><span class="sxs-lookup"><span data-stu-id="eccc6-140">The RecordInsertList.add method flushes records to the database whenever this will speed up performance.</span></span>

### <a name="examples---insertdatabase"></a><span data-ttu-id="eccc6-141">例 - insertDatabase</span><span class="sxs-lookup"><span data-stu-id="eccc6-141">Examples - insertDatabase</span></span>

<span data-ttu-id="eccc6-142">次の例では、RecordInsertList クラスを使用して BOM をある BOM から別の BOM にコピーします。</span><span class="sxs-lookup"><span data-stu-id="eccc6-142">The following example uses the RecordInsertList class to copy a BOM from one BOM to another.</span></span> <span data-ttu-id="eccc6-143">RecordInsertList.add メソッドを使用して、BOM 内のすべてのレコードが RecordInsertList クラスに追加されてから、最後の呼び出しが insertDatabase メソッドに行われて、残りのすべてのレコードが挿入されます。</span><span class="sxs-lookup"><span data-stu-id="eccc6-143">The RecordInsertList.add method is used to add all the records in the BOM to the RecordInsertList class before a final call is made to the insertDatabase method to insert all remaining records.</span></span>

```xpp
void copyBOM(BOMId _FromBOM, BOMId _ToBOM) 
{ 
    RecordInsertList BOMList; 
    BOM BOM, newBOM; 
    BOMList = new RecordInsertList(tableNum(BOM)); 
    while select BOM 
    where BOM.BOMId == _FromBOM 
    { 
        newBOM.data(BOM); 
        newBOM.BOMId = _ToBOM; 
        BOMList.add(newBOM); 
    } 
    BOMList.insertDatabase(); 
}
```

## <a name="method-new"></a><span data-ttu-id="eccc6-144">メソッド new</span><span class="sxs-lookup"><span data-stu-id="eccc6-144">Method new</span></span>

<span data-ttu-id="eccc6-145">データベースに挿入するレコードを保持する新しいオブジェクトを作成します。</span><span class="sxs-lookup"><span data-stu-id="eccc6-145">Creates a new object to hold records for insertion into the database.</span></span>

```xpp
public void new(TableId tableId, [boolean skipInsertMethod], [boolean skipDatabaseLog], [boolean skipEvents], [boolean skipAosValidation], [boolean skipRLSValidation], [Common table])
```

### <a name="parameters---new"></a><span data-ttu-id="eccc6-146">パラメーター - new</span><span class="sxs-lookup"><span data-stu-id="eccc6-146">Parameters - new</span></span>

<span data-ttu-id="eccc6-147">tableId</span><span class="sxs-lookup"><span data-stu-id="eccc6-147">tableId</span></span>  

<!-- -->

<span data-ttu-id="eccc6-148">skipInsertMethod</span><span class="sxs-lookup"><span data-stu-id="eccc6-148">skipInsertMethod</span></span>  

<!-- -->

<span data-ttu-id="eccc6-149">skipDatabaseLog</span><span class="sxs-lookup"><span data-stu-id="eccc6-149">skipDatabaseLog</span></span>  

<!-- -->

<span data-ttu-id="eccc6-150">skipEvents</span><span class="sxs-lookup"><span data-stu-id="eccc6-150">skipEvents</span></span>  

<!-- -->

<span data-ttu-id="eccc6-151">skipAosValidation</span><span class="sxs-lookup"><span data-stu-id="eccc6-151">skipAosValidation</span></span>  

<!-- -->

<span data-ttu-id="eccc6-152">skipRLSValidation</span><span class="sxs-lookup"><span data-stu-id="eccc6-152">skipRLSValidation</span></span>  

<!-- -->

<span data-ttu-id="eccc6-153">テーブル</span><span class="sxs-lookup"><span data-stu-id="eccc6-153">table</span></span>  

### <a name="examples---new"></a><span data-ttu-id="eccc6-154">例 - new</span><span class="sxs-lookup"><span data-stu-id="eccc6-154">Examples - new</span></span>

<span data-ttu-id="eccc6-155">次の例では、EventRuleField テーブルの新しい RecordInsertList クラスを作成します。</span><span class="sxs-lookup"><span data-stu-id="eccc6-155">The following example creates a new RecordInsertList class for the EventRuleField table.</span></span> <span data-ttu-id="eccc6-156">これらのレコードが挿入されるとテーブルの挿入メソッドが実行され、挿入がデータベース ログに記録されます。</span><span class="sxs-lookup"><span data-stu-id="eccc6-156">The insert method for the table is run when these records are inserted, and the insertion is recorded in the database log.</span></span> <span data-ttu-id="eccc6-157">ただし、CUD イベントは挿入用には生成されません。</span><span class="sxs-lookup"><span data-stu-id="eccc6-157">However, CUD events are not generated for the insertion.</span></span>

```xpp
recordInsertList = new RecordInsertList( 
    tablenum(EventRuleField), 
    false, 
    false, 
    true);
```

