---
title: データの削除
description: このトピックでは、X++ 言語での delete および doDelete メソッドについて説明します。
author: RobinARH
ms.date: 06/16/2020
ms.topic: article
audience: Developer
ms.reviewer: rhaertle
ms.custom: 150273
ms.search.region: Global
ms.author: rhaertle
ms.dyn365.ops.version: AX 7.0.0
ms.search.validFrom: 2016-02-28
ms.openlocfilehash: 55ac358b36f98afeed9c7d69dbf189b98eb2b711
ms.sourcegitcommit: e4992c57eea4c15ac052e9d65dddae625e3528f9
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/07/2021
ms.locfileid: "5865971"
---
# <a name="delete-data"></a><span data-ttu-id="82b59-103">データの削除</span><span class="sxs-lookup"><span data-stu-id="82b59-103">Delete data</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="82b59-104">データベースに格納されているテーブルから 1 つまたは複数の行を削除するため、SQL ステートメントを対話的またはソース コード内で使用することができます。</span><span class="sxs-lookup"><span data-stu-id="82b59-104">You can use SQL statements, either interactively or in source code, to delete one or more rows from tables that are stored in the database.</span></span>

+ <span data-ttu-id="82b59-105">**[delete メソッド](#delete-method)**: 一度に 1 行を削除します。</span><span class="sxs-lookup"><span data-stu-id="82b59-105">**[delete method](#delete-method)** – Delete one row at a time.</span></span>
+ <span data-ttu-id="82b59-106">**[doDelete メソッド](#do-delete-method)**: 一度に 1 行を削除します。</span><span class="sxs-lookup"><span data-stu-id="82b59-106">**[doDelete method](#do-delete-method)** – Delete one row at a time.</span></span>
+ <span data-ttu-id="82b59-107">**[delete\_from ステートメント](#delete-from-statement)**  – 複数の行を同時に削除します。</span><span class="sxs-lookup"><span data-stu-id="82b59-107">**[delete\_from statement](#delete-from-statement)** – Delete multiple rows at the same time.</span></span> <span data-ttu-id="82b59-108">**delete\_from** ステートメントを使用することにより、アプリケーションとデータベース間の通信が減少します。</span><span class="sxs-lookup"><span data-stu-id="82b59-108">By using the **delete\_from** statement, you reduce communication between the application and the database.</span></span> <span data-ttu-id="82b59-109">したがって、パフォーマンスの向上に役立ちます。</span><span class="sxs-lookup"><span data-stu-id="82b59-109">Therefore, you help increase performance.</span></span> <span data-ttu-id="82b59-110">場合によっては、このセット ベース操作をレコードごとの操作に戻すことができます。</span><span class="sxs-lookup"><span data-stu-id="82b59-110">In some situations, this set-based operation can fall back to a record-by-record operation.</span></span> <span data-ttu-id="82b59-111">詳細については、[セット ベースからレコード単位への操作の変換](xpp-data-perf.md)を参照してください。</span><span class="sxs-lookup"><span data-stu-id="82b59-111">For more information, see [Conversion of operations from set-based to record-by-record](xpp-data-perf.md).</span></span>

## <a name="delete-method"></a><a id="delete-method"></a><span data-ttu-id="82b59-112">delete メソッド</span><span class="sxs-lookup"><span data-stu-id="82b59-112">delete method</span></span>

<span data-ttu-id="82b59-113">**delete** メソッドは、データベースから現在のレコードを削除します。</span><span class="sxs-lookup"><span data-stu-id="82b59-113">The **delete** method deletes the current record from the database.</span></span> <span data-ttu-id="82b59-114">このメソッドを使用するには、**where** 句を使用して削除する行を指定します。</span><span class="sxs-lookup"><span data-stu-id="82b59-114">To use this method, use a **where** clause to specify the rows to delete.</span></span> <span data-ttu-id="82b59-115">一度に 1 つのレコードが、指定されたテーブルから削除されます。</span><span class="sxs-lookup"><span data-stu-id="82b59-115">One record at a time is then removed from the specified table.</span></span>

<span data-ttu-id="82b59-116">**delete** メソッドは上書きすることができます。</span><span class="sxs-lookup"><span data-stu-id="82b59-116">The **delete** method can be overridden.</span></span> <span data-ttu-id="82b59-117">たとえば、レコードが削除される前に、追加の検証を追加する場合があります。</span><span class="sxs-lookup"><span data-stu-id="82b59-117">For example, you might want to add extra validation before records are deleted.</span></span> <span data-ttu-id="82b59-118">**削除** 方法をオーバーライドする場合、**doDelete** を呼び出すことで、**削除** メソッドの元の (ベース) バージョンを実行できます。</span><span class="sxs-lookup"><span data-stu-id="82b59-118">If you override the **delete** method, you can run the original (base) version of the **delete** method by calling the **doDelete** method.</span></span> <span data-ttu-id="82b59-119">したがって、**doDelete** メソッドへの呼び出しは **delete** メソッドの **super()** への呼び出しに相当します。</span><span class="sxs-lookup"><span data-stu-id="82b59-119">Therefore, a call to the **doDelete** method is equivalent to a call to **super()** in the **delete** method.</span></span>

<span data-ttu-id="82b59-120">次の例では、**where** 句を満たす NameValuePair テーブル内のすべてのレコード (つまり、**名前** フィールドの値が **Name1** と等しいすべてのレコード) がデータベースから削除されます。</span><span class="sxs-lookup"><span data-stu-id="82b59-120">In the following example, all records in the NameValuePair table that satisfy the **where** clause (that is, all records where the value of the **Name** field equals **Name1**) are deleted from the database.</span></span> <span data-ttu-id="82b59-121">一度に 1 つのレコードが削除されます。</span><span class="sxs-lookup"><span data-stu-id="82b59-121">One record is deleted at a time.</span></span>

```xpp
ttsBegin;
    NameValuePair nameValuePair;

    while select forUpdate nameValuePair
        where nameValuePair.Name == 'Name1'
    {
        nameValuePair.delete();
    }
ttsCommit;
```

<span data-ttu-id="82b59-122">次の例では、LedgerJournalTrans テーブルからレコードを削除し、関連付けられている番号順序を更新します。</span><span class="sxs-lookup"><span data-stu-id="82b59-122">The following example deletes records from the LedgerJournalTrans table and updates the associated number sequence.</span></span>

```xpp
int counter = 0;
str _journalNum = '';
str _voucher = '';
LedgerJournalTrans ledgerJournalTrans;
LedgerJournalTable ledgerJournalTable;

ttsBegin;
    while select forUpdate ledgerJournalTrans
        index hint NumVoucherIdx
        where ledgerJournalTrans.journalNum == _journalNum
            && ledgerJournalTrans.voucher == _voucher
    {
        ledgerJournalTrans.doDelete();
        counter++;
    }

    if (counter && ledgerJournalTable.journalType != LedgerJournalType::Periodic)
    {
        NumberSeq::release(ledgerJournalTable.voucherSeries, _voucher);
    }
ttsCommit;
```

## <a name="dodelete-method"></a><a id="do-delete-method"></a><span data-ttu-id="82b59-123">doDelete メソッド</span><span class="sxs-lookup"><span data-stu-id="82b59-123">doDelete method</span></span>

<span data-ttu-id="82b59-124">**delete** テーブル メソッドと同様に、**doDelete** テーブル メソッドは、データベースから現在のレコードを削除します。</span><span class="sxs-lookup"><span data-stu-id="82b59-124">Like the **delete** table method, the **doDelete** table method deletes the current record from the database.</span></span> <span data-ttu-id="82b59-125">**delete** テーブル メソッドがオーバーライドされていて、オーバーライドされているバージョンではなく、そのメソッドの元の (ベース) バージョンを実行する場合は **doDelete** メソッドを使用します。</span><span class="sxs-lookup"><span data-stu-id="82b59-125">Use the **doDelete** method if the **delete** table method has been overridden, and you want to run the original (base) version of that method instead of the overridden version.</span></span> <span data-ttu-id="82b59-126">したがって、**doDelete** メソッドへの呼び出しは **delete** メソッドの **super()** への呼び出しに相当します。</span><span class="sxs-lookup"><span data-stu-id="82b59-126">Therefore, a call to the **doDelete** method is equivalent to a call to **super()** in the **delete** method.</span></span>

> [!WARNING]
> <span data-ttu-id="82b59-127">**doDelete** を呼び出すと、データベース イベント ハンドラー (たとえば **onDeleting** および **onDeleted**)、コマンド チェーン  **onDelete()**、および **delete()** の呼び出し自体を含むすべてのロジックをスキップします。</span><span class="sxs-lookup"><span data-stu-id="82b59-127">A call to **doDelete** skips all logic, including database event handlers (for example, **onDeleting** and **onDeleted**), chain-of-command **onDelete()**, and the **delete()** call itself.</span></span> <span data-ttu-id="82b59-128">一般に、**doDelete** を使用することは不適切なプラクティスと見なされており、使用することはお勧めしません。</span><span class="sxs-lookup"><span data-stu-id="82b59-128">It's generally considered bad practice to use **doDelete**, and we don't recommend that you use it.</span></span>

## <a name="delete_from-statement"></a><a id="delete-from-statement"></a><span data-ttu-id="82b59-129">delete\_from ステートメント</span><span class="sxs-lookup"><span data-stu-id="82b59-129">delete\_from statement</span></span>

<span data-ttu-id="82b59-130">**delete\_from** 演算子は、同時に複数のレコードを削除するレコード セット ベースの演算子です。</span><span class="sxs-lookup"><span data-stu-id="82b59-130">The **delete\_from** operator is a record set–based operator that removes multiple records at the same time.</span></span> <span data-ttu-id="82b59-131">この方法は、一度に 1 つのレコードを削除するループで **delete** メソッドを使用する方法よりも効率的かつ高速になります。</span><span class="sxs-lookup"><span data-stu-id="82b59-131">This approach can be more efficient and faster than an approach that uses the **delete** method in a loop to delete one record at a time.</span></span> <span data-ttu-id="82b59-132">**delete** メソッドをオーバーライドした場合、システムは削除される各行につき 1 回 **delete\_from** ステートメントを **delete** メソッドを呼び出すコードに解釈します。</span><span class="sxs-lookup"><span data-stu-id="82b59-132">If you've overridden the **delete** method, the system interprets the **delete\_from** statement into code that calls the **delete** method one time for each row that is deleted.</span></span>

<span data-ttu-id="82b59-133">次の例では、**名前** 列の値が **Name1** である NameValuePair テーブルのすべてのレコードを削除します。</span><span class="sxs-lookup"><span data-stu-id="82b59-133">The following example deletes all records in the NameValuePair table where the value in the **Name** column is **Name1**.</span></span>

```xpp
NameValuePair nameValuePair;
delete_from nameValuePair where nameValuePair.Name == 'Name1';
```

<span data-ttu-id="82b59-134">前の例とは対照的に、次の例では、各レコードに対してデータベース サーバーへの個別の SQL **削除** 呼び出しを発行するため、非効率的です。</span><span class="sxs-lookup"><span data-stu-id="82b59-134">In contrast to the previous example, the following example is inefficient, because it issues a separate SQL **delete** call to the database server for each record.</span></span> <span data-ttu-id="82b59-135">**delete** メソッドが、呼び出しごとに複数のレコードを削除することはありません。</span><span class="sxs-lookup"><span data-stu-id="82b59-135">The **delete** method never deletes more than one record per call.</span></span>

```xpp
// Example of inefficient code.
MyWidgetTable tabWidget; // extends xRecord.
ttsBegin;
    while select forUpdate tabWidget
        where tabWidget .quantity <= 100
    {
        tabWidget.delete();
    }
ttsCommit;
```

### <a name="a-delete-operation-that-has-an-inner-join"></a><span data-ttu-id="82b59-136">内部結合を持つ削除操作</span><span class="sxs-lookup"><span data-stu-id="82b59-136">A delete operation that has an inner join</span></span>

<span data-ttu-id="82b59-137">内部結合は **delete\_from** ステートメントではサポートされません。</span><span class="sxs-lookup"><span data-stu-id="82b59-137">Inner joins aren't supported on the **delete\_from** statement.</span></span> <span data-ttu-id="82b59-138">したがって、修正していない **join** キーワードを **delete\_from** ステートメント上で使用することができません。</span><span class="sxs-lookup"><span data-stu-id="82b59-138">Therefore, you can't use the unmodified **join** keyword on the **delete\_from** statement.</span></span> <span data-ttu-id="82b59-139">ただし、他の方法を使用して内部結合を論理的に実行できます。</span><span class="sxs-lookup"><span data-stu-id="82b59-139">However, you can logically perform an inner join by using other techniques.</span></span>

<span data-ttu-id="82b59-140">次の例では、**delete\_from** メソッドと内部結合を使用するための推奨方法を示します。</span><span class="sxs-lookup"><span data-stu-id="82b59-140">The following example shows the recommended way to use the **delete\_from** method and inner joins.</span></span> <span data-ttu-id="82b59-141">この例は比較的効率的です。</span><span class="sxs-lookup"><span data-stu-id="82b59-141">This example is relatively efficient.</span></span> <span data-ttu-id="82b59-142">ループが繰り返されるたびに個別の **delete\_from** ステートメントが発行されます。</span><span class="sxs-lookup"><span data-stu-id="82b59-142">It issues a separate **delete\_from** statement for each loop iteration.</span></span> <span data-ttu-id="82b59-143">ただし、各 **delete\_from** ステートメントでは、複数のレコード (ジョブによって削除されるすべてのレコードのサブセット) を削除できます。</span><span class="sxs-lookup"><span data-stu-id="82b59-143">However, each **delete\_from** statement can delete multiple records (a subset of all the records that the job deletes).</span></span>

```xpp
MyWidgetTable tabWidget; // extends xRecord.
ttsBegin;
while select from tabGalaxy
    where tabGalaxy .isTrusted == 0
{
    delete_from tabWidget
        where tabWidget .GalaxyRecId == tabGalaxy .RecId;
}
ttsCommit;
```

### <a name="a-delete-operation-that-uses-the-notexists-join-keyword"></a><span data-ttu-id="82b59-144">notexists 結合キーワードを使用する削除操作</span><span class="sxs-lookup"><span data-stu-id="82b59-144">A delete operation that uses the notexists join keyword</span></span>

<span data-ttu-id="82b59-145">**notexists join** キーワード ペアは **delete\_from** ステートメント内で使用することができます。</span><span class="sxs-lookup"><span data-stu-id="82b59-145">You can use the **notexists join** keyword pair in a **delete\_from** statement.</span></span> <span data-ttu-id="82b59-146">次の例の **delete\_from** ステートメントが効率的です。</span><span class="sxs-lookup"><span data-stu-id="82b59-146">The **delete\_from** statements in the following example are efficient.</span></span> <span data-ttu-id="82b59-147">**notexists join** 句を使用すると、**delete\_from** ステートメントが特定の行セットを削除できるようになります。</span><span class="sxs-lookup"><span data-stu-id="82b59-147">The **notexists join** clause enables the **delete\_from** statement to delete a specific set of rows.</span></span> <span data-ttu-id="82b59-148">この例では、**delete\_from** ステートメントが子の注文明細行の行がない親の注文ヘッダー行をすべて削除します。</span><span class="sxs-lookup"><span data-stu-id="82b59-148">In this example, the **delete\_from** statement removes all parent-order header rows that there are no child-order line rows for.</span></span> <span data-ttu-id="82b59-149">また、**exists join** 句を **delete\_from** ステートメント上で使用することができます。</span><span class="sxs-lookup"><span data-stu-id="82b59-149">You can also use the **exists join** clause on the **delete\_from** statement.</span></span>

```xpp
static void DeleteFromNotexists3bJob(Args _args)
{
    GmTabOrderHeader tabOHeader;
    GmTabOrderLine tabOLine;
    AddressState tabAddressState;
    str 127 sOH_Info;
    str 127 sOL_Data;
    int64 i64OHRecId;
    delete_from tabOLine;
    delete_from tabOHeader;
    // Inserts into parent table.
    sOH_Info = "Albert needs tires.";
    insert_recordset tabOHeader
        (OH_Info)
        select firstOnly sOH_Info from tabAddressState;
    sOH_Info = "Benson wants plastic.";
    insert_recordset tabOHeader
        (OH_Info)
        select firstOnly sOH_Info from tabAddressState;
    // Obtain a OrderHeader RecId,
    // use it to insert one child row.
    sOL_Data = "4 re-treads.";
    while select firstOnly tabOHeader
        order by OH_Info
        where tabOHeader .OH_Info like "A*"
    {
        i64OHRecId = tabOHeader .RecId;
        insert_recordset tabOLine
            (OL_Data ,OrderHeaderRecId)
            select firstOnly
                sOL_Data ,i64OHRecId
                from tabAddressState;
        break;
    }
    // Before the delete notexists.
    // Display all parent, and then all child rows.
    while select tabOHeader
        order by OH_Info
    {
        info(strFmt("Before: OHeader:  OH_Info==%1 , RecId==%2"
            ,tabOHeader .OH_Info ,tabOHeader .RecId));
    }
    while select tabOLine
        order by OL_Data
    {
        info(strFmt("Before: OLine:  OL_Data==%1 , OrderHeaderRecId==%2"
            ,tabOLine .OL_Data ,tabOLine .OrderHeaderRecId));
    }
    // Delete_From NotExists Join, to remove from the
    // parent table all order headers without children.
    delete_from tabOHeader
        notexists join tabOLine
            where tabOHeader .RecId ==
                tabOLine .OrderHeaderRecId;
    info(strFmt("%1 is the number of childless OHeader records deleted."
        ,tabOHeader.rowCount()));
    // After the delete notexists.
    // Display all parent, and then all child rows.
    info("- - - - - - - - - - - - - - -");
    while select tabOHeader
        order by OH_Info
    {
        info(strFmt("After: OHeader:  OH_Info==%1 , RecId==%2"
            ,tabOHeader .OH_Info ,tabOHeader .RecId));
    }
    while select tabOLine
        order by OL_Data
    {
        info(strFmt("After: OLine:  OL_Data==%1 , OrderHeaderRecId==%2"
            ,tabOLine .OL_Data ,tabOLine .OrderHeaderRecId));
    }

/**************  Actual Infolog output
Message (12:54:14 pm)
Before: OHeader:  OH_Info==Albert needs tires. , RecId==5637144608
Before: OHeader:  OH_Info==Benson wants plastic. , RecId==5637144609
Before: OLine:  OL_Data==4 re-treads. , OrderHeaderRecId==5637144608
1 is the number of childless OHeader records deleted.
- - - - - - - - - - - - - - -
After: OHeader:  OH_Info==Albert needs tires. , RecId==5637144608
After: OLine:  OL_Data==4 re-treads. , OrderHeaderRecId==5637144608
**************/
}
```


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]