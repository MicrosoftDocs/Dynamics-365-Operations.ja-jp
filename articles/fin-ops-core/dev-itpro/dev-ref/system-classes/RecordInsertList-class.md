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
# <a name="class-recordinsertlist"></a>クラス RecordInsertList

[!include [banner](../../includes/banner.md)]

```xpp
class RecordInsertList extends Object
```

RecordInsertList クラスは、カーネルで配列挿入機能を提供します。

## <a name="remarks"></a>備考

このクラスを使用すると、一度に複数のレコードをデータベースに挿入できます。これにより、アプリケーションとデータベース間の通信が減少します。 レコードは、カーネルが適切と判断したときに挿入されますが、insertDatabase、add、insertDatabase メソッドの呼び出し以前に挿入されます。 RecordInsertList.add および RecordInsertList.insertDatabase メソッドは、レコードが実際にいつ挿入されたかを追跡できるように、現在挿入されているレコードの累計数を返します。 非 SQL ベースのテーブル (一時テーブルなど) を使用する場合、またはテーブルでの挿入方法が無効にされた (明示的に破棄されていない限り) 場合は、配列挿入操作が自動的に、従来のレコードごとの挿入に戻ります。 RecordInsertList クラスは、RecordSortedList クラスに似ていますが、クライアント/サーバー サポートが組み込まれており (必要に応じて、ある層から別の層にデータをパッキングします)、RecordSortedList で使用できる並べ替え順序機能がありません。

## <a name="examples"></a>例

次の例では、RecordInsertList クラスを使用して ある BOM から 別の BOM に部品表 (BOM) をコピーします。

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

## <a name="methods"></a>メソッド

| 方法                                                                                                                                                                                              | 説明                                                                                       |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| public int add(Common record)                                                                                                                                                                       | データベースへのその後の挿入のために、RecordInsertList オブジェクトにレコードを追加します。            |
| public int insertDatabase()                                                                                                                                                                         | 現在の RecordInsertList オブジェクトにまだ挿入されていないすべてのレコードを挿入します。 |
| public void new(TableId tableId, \[boolean skipInsertMethod\], \[boolean skipDatabaseLog\], \[boolean skipEvents\], \[boolean skipAosValidation\], \[boolean skipRLSValidation\], \[Common table\]) | データベースに挿入するレコードを保持する新しいオブジェクトを作成します。                             |

## <a name="method-add"></a>メソッド add

データベースへのその後の挿入のために、RecordInsertList オブジェクトにレコードを追加します。

```xpp
public int add(Common record)
```

### <a name="parameters---add"></a>パラメーター - add

記録  
クラスをインスタンス化するために使用される、同じ型のデータベース バッファです。

### <a name="return-value---add"></a>戻り値 - add

レコードが正常にリストに追加されたかどうかを示す整数。

### <a name="remarks---add"></a>備考 - add

Add メソッドは、パフォーマンスの向上が見込まれる場合は常に、レコードをデータベースにフラッシュすることができます。 ただし、リスト内のすべてのレコードが挿入されることを保証するには、RecordInsertList.insertDatabase メソッドを使用します。

### <a name="examples---add"></a>例 - add

次の例では、RecordInsertList クラスを使用して BOM をある BOM から別の BOM にコピーします。 add メソッドを使用して、BOM 内のすべてのレコードが RecordInsertList オブジェクトに追加されてから、最後の呼び出しが insertDatabase メソッドに行われて、残りのすべてのレコードが挿入されます。

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

## <a name="method-insertdatabase"></a>メソッド insertDatabase

現在の RecordInsertList オブジェクトにまだ挿入されていないすべてのレコードを挿入します。

```xpp
public int insertDatabase()
```

### <a name="return-value---insertdatabase"></a>戻り値 - insertDatabase

挿入されたレコードの合計数を表す整数。

### <a name="remarks---insertdatabase"></a>備考 - insertDatabase

RecordInsertList.add メソッドは、パフォーマンスの向上が見込まれる場合は常に、レコードをデータベースにフラッシュします。

### <a name="examples---insertdatabase"></a>例 - insertDatabase

次の例では、RecordInsertList クラスを使用して BOM をある BOM から別の BOM にコピーします。 RecordInsertList.add メソッドを使用して、BOM 内のすべてのレコードが RecordInsertList クラスに追加されてから、最後の呼び出しが insertDatabase メソッドに行われて、残りのすべてのレコードが挿入されます。

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

## <a name="method-new"></a>メソッド new

データベースに挿入するレコードを保持する新しいオブジェクトを作成します。

```xpp
public void new(TableId tableId, [boolean skipInsertMethod], [boolean skipDatabaseLog], [boolean skipEvents], [boolean skipAosValidation], [boolean skipRLSValidation], [Common table])
```

### <a name="parameters---new"></a>パラメーター - new

tableId  

<!-- -->

skipInsertMethod  

<!-- -->

skipDatabaseLog  

<!-- -->

skipEvents  

<!-- -->

skipAosValidation  

<!-- -->

skipRLSValidation  

<!-- -->

テーブル  

### <a name="examples---new"></a>例 - new

次の例では、EventRuleField テーブルの新しい RecordInsertList クラスを作成します。 これらのレコードが挿入されるとテーブルの挿入メソッドが実行され、挿入がデータベース ログに記録されます。 ただし、CUD イベントは挿入用には生成されません。

```xpp
recordInsertList = new RecordInsertList( 
    tablenum(EventRuleField), 
    false, 
    false, 
    true);
```

