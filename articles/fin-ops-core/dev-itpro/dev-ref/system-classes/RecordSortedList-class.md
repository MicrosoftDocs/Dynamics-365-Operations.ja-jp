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
# <a name="class-recordsortedlist"></a>クラス RecordSortedList

[!include [banner](../../includes/banner.md)]

```xpp
class RecordSortedList extends Object
```

RecordSortedList クラスは、1 回のデータベース アクセスで複数のレコードを挿入します。

## <a name="remarks"></a>備考

特定のテーブルのデータのサブセットが必要で、現在インデックスとして存在しない順序でソートする場合は、RecordSortedList を使用します。 RecordSortedList オブジェクトは、1 つのテーブルからのレコードを保有します。 リストには、sortOrder メソッドを使用して表示されるフィールドによって定義される一意のキーがあります。 レコードは、挿入時に自動的に並べ替えられます。並べ替え順序に挿入する必要はありません。 RecordSortedList オブジェクトは、結果セットをパラメーターとして渡すのに特に役立ちます。RecordSortedList オブジェクトのサイズの制限はありませんが、完全にメモリ ベースであるため、潜在的なメモリ消費の問題があります。 InsertDatabase メソッドを呼び出す前に、RecordSortedList オブジェクトがサーバーにある必要があります。 それ以外の場合は、例外がスローされます。 レコード レベル セキュリティ (RLS) は、RecordSortedList クラスによって適用されることはできません。 RLS は、RecordInsertList クラスによって適用されます。 次のような状況では、一時テーブルよりも RecordSortedList を使用します。

-   並べ替え順序が 1 つだけ必要です。
-   レコードの数は (メモリの問題を避けるために) 高すぎるということはありません。

一時テーブル、RecordSortedList オブジェクトと比較して:

-   時間が短縮されます。
-   ディスク ベースではありません。
-   1 つのインデックスがあるのみ
-   フォームでは使用できません。
-   読み取りごとにクライアントとサーバー (グループ化された) の間で呼び出しが必要です。

## <a name="examples"></a>例

## <a name="methods"></a>メソッド

| 方法                                                        | 説明                                                                                                                                                          |
|---------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| public boolean del(Common record)                             | recordBuffer のキー フィールドと一致するキーを持つレコードを recordSortedList から削除します。                                                           |
| public boolean find(Common record)                            | レコード バッファーを、レコード バッファーの主なフィールドに一致するキーを持つレコードの内容に設定し、リストを返されるレコードに配置します。 |
| public boolean first(Common record)                           | リストをリスト内の最初のレコードに配置し、その内容をレコード バッファーにコピーします。                                                                    |
| public boolean ins(Common record, \[boolean updateIfExists\]) | 重複していない場合に、RecordSortedList に新しいレコードを挿入します。                                                                                                |
| public int len()                                              | RecordSortedList オブジェクトの現在のレコード数を返します。                                                                                                  |
| public boolean next(Common record)                            | レコード バッファーを recordSortedList の次のレコードの内容に設定し、リストを返されるレコードに配置します。                                     |
| public void new(TableId tableId, \[Common table\])            | Object クラスの新しいインスタンスを初期化します。                                                                                                                      |
| public void sortOrder(FieldId fieldId, VarArg )               | レコードが並べ替えされるフィールドを定義します。                                                                                                                  |
| public void sortOrderFromContainer(container container)       | レコードが並べ替えされるフィールドを定義します。                                                                                                                  |
| public void insertDatabase(\[Connection connection\])         | データベースに 1 回に複数のレコードを挿入します。                                                                                                           |

## <a name="method-del"></a>メソッド del

recordBuffer のキー フィールドと一致するキーを持つレコードを recordSortedList から削除します。

```xpp
public boolean del(Common record)
```

### <a name="parameters---del"></a>パラメーター - del

記録  
削除するレコードのキーの値を含むレコード バッファ。

### <a name="return-value---del"></a>戻り値 - del

レコードが削除された場合は true。それ以外の場合は false。

## <a name="method-find"></a>メソッド find

レコード バッファーを、レコード バッファーの主なフィールドに一致するキーを持つレコードの内容に設定し、リストを返されるレコードに配置します。

```xpp
public boolean find(Common record)
```

### <a name="parameters---find"></a>パラメーター - find

記録  
検索するキーの値を含むレコード バッファ。 見つかったレコードは、レコード バッファのコンテンツを置き換えます。

### <a name="return-value---find"></a>戻り値 - find

レコードが見つかる場合は true。それ以外の場合は false。

## <a name="method-first"></a>メソッド first

リストをリスト内の最初のレコードに配置し、その内容をレコード バッファーにコピーします。

```xpp
public boolean first(Common record)
```

### <a name="parameters---first"></a>パラメーター - first

記録  
リストの最初のレコードに含まれるレコード バッファ。

### <a name="return-value---first"></a>戻り値 - first

メソッドが成功する場合は true。それ以外の場合は false。

## <a name="method-ins"></a>メソッド ins

重複していない場合に、RecordSortedList に新しいレコードを挿入します。

```xpp
public boolean ins(Common record, [boolean updateIfExists])
```

### <a name="parameters---ins"></a>パラメーター - ins

記録  
重複するレコードを破棄または置き換えるかどうか。省略可能です。 False の場合、重複している場合に、新しいレコードが破棄されます。 True の場合、新しいレコードが重複している場合、既存のレコードが置き換えられます。

<!-- -->

updateIfExists  
重複するレコードを破棄または置き換えるかどうか。省略可能です。 False の場合、重複している場合に、新しいレコードが破棄されます。 True の場合、新しいレコードが重複している場合、既存のレコードが置き換えられます。

### <a name="return-value---ins"></a>戻り値 - ins

レコードが追加または置換された場合は true。それ以外の場合は false。

## <a name="method-len"></a>メソッド len

RecordSortedList オブジェクトの現在のレコード数を返します。

```xpp
public int len()
```

### <a name="return-value---len"></a>戻り値 - len

リスト内の現在のレコード数。

## <a name="method-next"></a>メソッド next

レコード バッファーを recordSortedList の次のレコードの内容に設定し、リストを返されるレコードに配置します。

```xpp
public boolean next(Common record)
```

### <a name="parameters---next"></a>パラメーター - next

記録  
結果を受信するレコード バッファ。

### <a name="return-value---next"></a>戻り値 - next

操作が成功した場合は true。それ以外の場合は false。

## <a name="method-new"></a>メソッド new

Object クラスの新しいインスタンスを初期化します。

```xpp
public void new(TableId tableId, [Common table])
```

### <a name="parameters---new"></a>パラメーター - new

tableId  

<!-- -->

テーブル  

### <a name="remarks---new"></a>備考 - new

リストには、tableId パラメーターで指定された型のレコードを含めることができます。

### <a name="examples---new"></a>例 - new

次の例では、RecordInsertList オブジェクトを使用して、1 つのデータベース操作に 3 つのレコードを挿入します。

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

## <a name="method-sortorder"></a>メソッド sortOrder

レコードが並べ替えされるフィールドを定義します。

```xpp
public void sortOrder(FieldId fieldId, VarArg )
```

### <a name="parameters---sortorder"></a>パラメーター - sortOrder

fieldId  

<!-- -->


### <a name="remarks---sortorder"></a>備考 - sortOrder

並べ替える 1 つまたはそれ以上のフィールドを指定することができます。 このメソッドは、RecordSortedList クラスの同じインスタンスに対して 1 回だけ呼び出すことができます。 設定した後は、並べ替え順序を変更することはできません。

### <a name="examples---sortorder"></a>例 - sortOrder

次の例では、DimensionSetRuleTable テーブル レコードのリストを作成し、SetId フィールドと HierarchyId フィールドの順に並べ替えます。

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

## <a name="method-sortorderfromcontainer"></a>メソッド sortOrderFromContainer

レコードが並べ替えされるフィールドを定義します。

```xpp
public void sortOrderFromContainer(container container)
```

### <a name="parameters---sortorderfromcontainer"></a>パラメーター - sortOrderFromContainer

コンテナー  
リストをソートする必要があるフィールド。 各フィールドがフィールド ID によって指定されました。たとえば、FieldNum 機能が使われます。

### <a name="remarks---sortorderfromcontainer"></a>備考 - sortOrderFromContainer

フィールドの一覧をコンテナーに指定しない場合、RecordSortedList.sortOrder を使用します。

## <a name="method-insertdatabase"></a>メソッド insertDatabase

データベースに 1 回に複数のレコードを挿入します。

```xpp
public void insertDatabase([Connection connection])
```

### <a name="parameters---insertdatabase"></a>パラメーター - insertDatabase

connection  

### <a name="remarks---insertdatabase"></a>備考 - insertDatabase

呼び出しの後、リストのエントリは、RecordSortedList オブジェクトに残ります。 RecordSortedList クラスは、insertDatabase メソッドの呼び出し前にサーバーにある必要があります。それ以外の場合、例外が発生します。 RecId およびその他のシステム管理フィールド値には、insertDatabase メソッド呼び出しが行われるまで値が割り当てられません。 このメソッドは、次のいずれかの条件が満たされた場合、レコードごとの挿入に戻ります。

-   テーブルは SQL ストアドではありません。
-   テーブルの挿入メソッドがオーバーロードします。
-   テーブルには、メモ フィールドまたはコンテナー フィールドが含まれます。

### <a name="examples---insertdatabase"></a>例 - insertDatabase

次の例は、1 つのデータベース操作に 3 つのレコードを挿入する方法を示しています。

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

