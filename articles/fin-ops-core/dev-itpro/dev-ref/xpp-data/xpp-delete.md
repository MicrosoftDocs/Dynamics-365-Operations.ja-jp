---
title: データの削除
description: このトピックでは、X++ 言語での delete および doDelete メソッドについて説明します。
author: RobinARH
manager: AnnBe
ms.date: 06/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.custom: 150273
ms.search.region: Global
ms.author: rhaertle
ms.dyn365.ops.version: AX 7.0.0
ms.search.validFrom: 2016-02-28
ms.openlocfilehash: f9d840ac13443fd95d8bae56d573454b69416fd4
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/13/2020
ms.locfileid: "4408739"
---
# <a name="delete-data"></a>データの削除

[!include [banner](../../includes/banner.md)]

データベースに格納されているテーブルから 1 つまたは複数の行を削除するため、SQL ステートメントを対話的またはソース コード内で使用することができます。

+ **[delete メソッド](#delete-method)**: 一度に 1 行を削除します。
+ **[doDelete メソッド](#do-delete-method)**: 一度に 1 行を削除します。
+ **[delete\_from ステートメント](#delete-from-statement)**  – 複数の行を同時に削除します。 **delete\_from** ステートメントを使用することにより、アプリケーションとデータベース間の通信が減少します。 したがって、パフォーマンスの向上に役立ちます。 場合によっては、このセット ベース操作をレコードごとの操作に戻すことができます。 詳細については、[セット ベースからレコード単位への操作の変換](xpp-data-perf.md)を参照してください。

## <a name="delete-method"></a><a id="delete-method"></a>delete メソッド

**delete** メソッドは、データベースから現在のレコードを削除します。 このメソッドを使用するには、**where** 句を使用して削除する行を指定します。 一度に 1 つのレコードが、指定されたテーブルから削除されます。

**delete** メソッドは上書きすることができます。 たとえば、レコードが削除される前に、追加の検証を追加する場合があります。 **削除** 方法をオーバーライドする場合、**doDelete** を呼び出すことで、**削除** メソッドの元の (ベース) バージョンを実行できます。 したがって、**doDelete** メソッドへの呼び出しは **delete** メソッドの **super()** への呼び出しに相当します。

次の例では、**where** 句を満たす NameValuePair テーブル内のすべてのレコード (つまり、**名前** フィールドの値が **Name1** と等しいすべてのレコード) がデータベースから削除されます。 一度に 1 つのレコードが削除されます。

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

次の例では、LedgerJournalTrans テーブルからレコードを削除し、関連付けられている番号順序を更新します。

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

## <a name="dodelete-method"></a><a id="do-delete-method"></a>doDelete メソッド

**delete** テーブル メソッドと同様に、**doDelete** テーブル メソッドは、データベースから現在のレコードを削除します。 **delete** テーブル メソッドがオーバーライドされていて、オーバーライドされているバージョンではなく、そのメソッドの元の (ベース) バージョンを実行する場合は **doDelete** メソッドを使用します。 したがって、**doDelete** メソッドへの呼び出しは **delete** メソッドの **super()** への呼び出しに相当します。

> [!WARNING]
> **doDelete** を呼び出すと、データベース イベント ハンドラー (たとえば **onDeleting** および **onDeleted**)、コマンド チェーン  **onDelete()**、および **delete()** の呼び出し自体を含むすべてのロジックをスキップします。 一般に、**doDelete** を使用することは不適切なプラクティスと見なされており、使用することはお勧めしません。

## <a name="delete_from-statement"></a><a id="delete-from-statement"></a>delete\_from ステートメント

**delete\_from** 演算子は、同時に複数のレコードを削除するレコード セット ベースの演算子です。 この方法は、一度に 1 つのレコードを削除するループで **delete** メソッドを使用する方法よりも効率的かつ高速になります。 **delete** メソッドをオーバーライドした場合、システムは削除される各行につき 1 回 **delete\_from** ステートメントを **delete** メソッドを呼び出すコードに解釈します。

次の例では、**名前** 列の値が **Name1** である NameValuePair テーブルのすべてのレコードを削除します。

```xpp
NameValuePair nameValuePair;
delete_from nameValuePair where nameValuePair.Name == 'Name1';
```

前の例とは対照的に、次の例では、各レコードに対してデータベース サーバーへの個別の SQL **削除** 呼び出しを発行するため、非効率的です。 **delete** メソッドが、呼び出しごとに複数のレコードを削除することはありません。

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

### <a name="a-delete-operation-that-has-an-inner-join"></a>内部結合を持つ削除操作

内部結合は **delete\_from** ステートメントではサポートされません。 したがって、修正していない **join** キーワードを **delete\_from** ステートメント上で使用することができません。 ただし、他の方法を使用して内部結合を論理的に実行できます。

次の例では、**delete\_from** メソッドと内部結合を使用するための推奨方法を示します。 この例は比較的効率的です。 ループが繰り返されるたびに個別の **delete\_from** ステートメントが発行されます。 ただし、各 **delete\_from** ステートメントでは、複数のレコード (ジョブによって削除されるすべてのレコードのサブセット) を削除できます。

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

### <a name="a-delete-operation-that-uses-the-notexists-join-keyword"></a>notexists 結合キーワードを使用する削除操作

**notexists join** キーワード ペアは **delete\_from** ステートメント内で使用することができます。 次の例の **delete\_from** ステートメントが効率的です。 **notexists join** 句を使用すると、**delete\_from** ステートメントが特定の行セットを削除できるようになります。 この例では、**delete\_from** ステートメントが子の注文明細行の行がない親の注文ヘッダー行をすべて削除します。 また、**exists join** 句を **delete\_from** ステートメント上で使用することができます。

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
