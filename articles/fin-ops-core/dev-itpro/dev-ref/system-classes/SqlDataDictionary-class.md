---
title: SqlDataDictionary クラス
description: このトピックでは、SqlDataDictionary クラスについて説明します。
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
ms.openlocfilehash: 0582ebb116bf09f00a8041b41840f6b7caf22e1e
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502801"
---
# <a name="class-sqldatadictionary"></a>クラス SqlDataDictionary

[!include [banner](../../includes/banner.md)]

```xpp
class SqlDataDictionary extends Object
```

SqlDataDictionary クラスは、データ ディクショナリ保守のメソッドのコレクションを提供します。

## <a name="remarks"></a>備考

この API には、実行時に呼び出される組み込み認証チェックがあります。 開発セキュリティ キー (SysDevelopment) にアクセスせずにユーザーが SQLDataDictionary クラスのメンバーを呼び出すと、例外が発生します。

## <a name="examples"></a>例

次の例では、UserInfo テーブルがデータベースに存在するかどうかを確認します。

```xpp
server static public void Main(Args _args) 
{ 
    SqlDataDictionary sqlDict; 
    boolean b; 
    sqlDict = new SqlDataDictionary(); 
    if (sqlDict) 
    { 
        b = sqlDict.tableExist("USERINFO"); 
        print b; 
        pause; 
    } 
}
```

## <a name="methods"></a>メソッド

| 方法                                                                                                               | 説明                                                                                                                   |
|----------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| public int indexCreate(\[TableId tableId\], \[IndexId indexId\])                                                     | テーブルのインデックスを SQL データベースで作成します。 このメソッドを使用してインデックスを再作成することもできます。 |
| public str indexCreateDDL(TableId tableId)                                                                           | テーブルのインデックスを作成するのに必要な SQL ステートメントを生成および返します。                      |
| public int indexDrop(\[TableId tableId\], \[IndexId indexId\], \[boolean onlyNonUnique\])                            | テーブルのインデックスを SQL データベースでドロップします。                                                      |
| public str name(str bmsname, \[FieldId fieldId\], \[int arrayindex\])                                                | 任意のオブジェクト名を有効な SQL データベースのオブジェクト名、つまり、現在接続されているデータベースに有効な名前に変換します。        |
| public int tableCreate(\[boolean indexes\], \[TableId tableId\])                                                     | 1 つ以上のテーブルを SQL データベース内に作成します。 また、インデックス用に作成するオプションを提供します。           |
| public str tableCreateDDL(TableId tableId)                                                                           | テーブルを作成するため SQL ステートメントを生成および返します。                                             |
| public int tableDrop(TableId tableId, \[boolean prompt\_before\_drop\])                                              | テーブルを SQL データベースでドロップします。                                                                    |
| public str tableDropDDL(TableId tableId)                                                                             | テーブルをドロップするため SQL ステートメントを生成および返します。                                               |
| public boolean tableEmpty(TableId tableId, \[str company\], \[boolean not\_this\_company\])                          | テーブルが空でない場合は true を返します。それ以外の場合は、false を返します。                                                                          |
| public boolean tableExist(str sqltablename, \[boolean use\_within\_transaction\])                                    | テーブルが存在する場合は true を返します。それ以外の場合は、false を返します。                                                                                |
| public int tableMetaData(TableId tableId)                                                                            | データ ディクショナリ メタ データで SqlDescribe テーブルを入力します。                                                                   |
| public int tableReindex(\[TableId tableId\], \[IndexId indexId\])                                                    | テーブルのインデックスを更新します。                                                                                                  |
| public int tableSynchronize(TableId tableId, \[boolean update\_dict\_info\_only\], \[boolean check\_indexes\])       | テーブルと、SQL データベースのテーブルを同期します。                                               |
| public int tableTruncate(TableId tableId, \[boolean prompt\_before\_truncate\], \[boolean truncate\_system\_table\]) | テーブルの切り詰め                                                                                    |
| public str tableTruncateDDL(TableId tableId)                                                                         | テーブルを切り詰めるため SQL ステートメントを生成および返します。                                             |
| ::public static int synchronize(\[boolean synchronize\_all\])                                                        | データ ディクショナリと、SQL データベースのデータ ディクショナリを同期します。                           |
| public void new()                                                                                                    | SqlDataDictionary クラスの新しいインスタンスを初期化します。                                                                    |
| public void tableDelete(TableId tableId)                                                                             | SQL データベースでテーブルを削除します。                                                                  |

## <a name="method-indexcreate"></a>メソッド indexCreate

テーブルのインデックスを SQL データベースで作成します。 このメソッドを使用してインデックスを再作成することもできます。

```xpp
public int indexCreate([TableId tableId], [IndexId indexId])
```

### <a name="parameters---indexcreate"></a>パラメーター - indexCreate

tableId  
インデックス ハンドル (すべて0) (オプション)。

<!-- -->

indexId  
インデックス ハンドル (すべて0) (オプション)。

### <a name="return-value---indexcreate"></a>戻り値 - indexCreate

メソッドが成功した場合は 0 です。

### <a name="remarks---indexcreate"></a>備考 - indexCreate

このメソッドを使用すると、インデックスを再作成できます。 パラメーターに 0 を使用すると、すべてのテーブルまたはインデックスを指定します。

### <a name="examples---indexcreate"></a>例 - indexCreate

```xpp
{ 
    SqlDataDictionary DD = new SqlDataDictionary(); 
    DD.indexCreate(TableName2Id("Address")); 
}
```

## <a name="method-indexcreateddl"></a>メソッド indexCreateDDL

テーブルのインデックスを作成するのに必要な SQL ステートメントを生成および返します。

```xpp
public str indexCreateDDL(TableId tableId)
```

### <a name="parameters---indexcreateddl"></a>パラメーター - indexCreateDDL

tableId  
インデックスを作成する必要があるテーブル ハンドル。

### <a name="return-value---indexcreateddl"></a>戻り値 - indexCreateDDL

テーブルのインデックスを作成するための SQL ステートメントを返します。

## <a name="method-indexdrop"></a>メソッド indexDrop

テーブルのインデックスを SQL データベースでドロップします。

```xpp
public int indexDrop([TableId tableId], [IndexId indexId], [boolean onlyNonUnique])
```

### <a name="parameters---indexdrop"></a>パラメーター - indexDrop

tableId  

<!-- -->

indexId  

<!-- -->

onlyNonUnique  

### <a name="return-value---indexdrop"></a>戻り値 - indexDrop

メソッドが成功した場合は 0。

### <a name="remarks---indexdrop"></a>備考 - indexDrop

パラメーターに 0 を使用すると、すべてのテーブルまたはインデックスを指定します。

### <a name="examples---indexdrop"></a>例 - indexDrop

```xpp
{ 
    SqlDataDictionary DD = new SqlDataDictionary(); 
    DD.indexDrop(TableName2Id("Address")); 
}
```

## <a name="method-name"></a>メソッド名

任意のオブジェクト名を有効な SQL データベースのオブジェクト名、つまり、現在接続されているデータベースに有効な名前に変換します。

```xpp
public str name(str bmsname, [FieldId fieldId], [int arrayindex])
```

### <a name="parameters---name"></a>パラメーター - name

bmsname  
フィールドのインデックス (適用されない場合は 0)、つまり、分析コード \[2\] などの配列フィールドの arrayindex'th エントリです (オプション)。

<!-- -->

fieldId  
フィールドのインデックス (適用されない場合は 0)、つまり、分析コード \[2\] などの配列フィールドの arrayindex'th エントリです (オプション)。

<!-- -->

arrayindex  
フィールドのインデックス (適用されない場合は 0)、つまり、分析コード \[2\] などの配列フィールドの arrayindex'th エントリです (オプション)。

### <a name="return-value---name"></a>戻り値 - name

有効なオブジェクト名。

### <a name="remarks---name"></a>備考 - name

名前は切り捨てられる可能性があるため、固有のオブジェクト識別子が指定される場合があります。 また、3 番目のパラメータは、メソッドが配列フィールドの個別の SQL フィールド名を返すことを可能にします。

## <a name="method-tablecreate"></a>メソッド tableCreate

1 つ以上のテーブルを SQL データベース内に作成します。 また、インデックス用に作成するオプションを提供します。

```xpp
public int tableCreate([boolean indexes], [TableId tableId])
```

### <a name="parameters---tablecreate"></a>パラメーター - tableCreate

indexes  
テーブル ハンドル (すべて0) (オプション)。

<!-- -->

tableId  
テーブル ハンドル (すべて0) (オプション)。

### <a name="return-value---tablecreate"></a>戻り値 - tableCreate

メソッドが成功した場合は 0。

### <a name="remarks---tablecreate"></a>備考 - tableCreate

低レベルのメンテナンスにのみ使用されます。

### <a name="examples---tablecreate"></a>例 - tableCreate

```xpp
{ 
    SqlDataDictionary DD = new SqlDataDictionary(); 
    DD.tableCreate(TableName2Id("Address")); 
}
```

## <a name="method-tablecreateddl"></a>メソッド tableCreateDDL

テーブルを作成するため SQL ステートメントを生成および返します。

```xpp
public str tableCreateDDL(TableId tableId)
```

### <a name="parameters---tablecreateddl"></a>パラメーター - tableCreateDDL

tableId  
作成するテーブルのテーブル ハンドルです。

### <a name="return-value---tablecreateddl"></a>戻り値 - tableCreateDDL

テーブルを作成する SQL ステートメント。

## <a name="method-tabledrop"></a>メソッド tableDrop

テーブルを SQL データベースでドロップします。

```xpp
public int tableDrop(TableId tableId, [boolean prompt_before_drop])
```

### <a name="parameters---tabledrop"></a>パラメーター - tableDrop

tableId  
テーブルを削除する前にユーザーに確認するかどうかを示すブール フラグ; オプション。 既定では、true です。

<!-- -->

prompt\_before\_drop  
テーブルを削除する前にユーザーに確認するかどうかを示すブール フラグ; オプション。 既定では、true です。

### <a name="return-value---tabledrop"></a>戻り値 - tableDrop

メソッドが成功した場合は 0。

## <a name="method-tabledropddl"></a>メソッド tableDropDDL

テーブルをドロップするため SQL ステートメントを生成および返します。

```xpp
public str tableDropDDL(TableId tableId)
```

### <a name="parameters---tabledropddl"></a>パラメーター - tableDropDDL

tableId  
削除するテーブル。

### <a name="return-value---tabledropddl"></a>戻り値 - tableDropDDL

指定されたテーブルを削除する SQL ステートメント。

## <a name="method-tableempty"></a>メソッド tableEmpty

テーブルが空でない場合は true を返します。それ以外の場合は、false を返します。

```xpp
public boolean tableEmpty(TableId tableId, [str company], [boolean not_this_company])
```

### <a name="parameters---tableempty"></a>パラメーター - tableEmpty

tableId  
true の場合、クエリーから会社に属するレコードを除外します: オプション。 既定では、false です。

<!-- -->

会社  
true の場合、クエリーから会社に属するレコードを除外します: オプション。 既定では、false です。

<!-- -->

not\_this\_company  
true の場合、クエリーから会社に属するレコードを除外します: オプション。 既定では、false です。

### <a name="return-value---tableempty"></a>戻り値 - tableEmpty

テーブルが空の場合は true。それ以外の場合は、false。

## <a name="method-tableexist"></a>メソッド tableExist

テーブルが存在する場合は true を返します。それ以外の場合は、false を返します。

```xpp
public boolean tableExist(str sqltablename, [boolean use_within_transaction])
```

### <a name="parameters---tableexist"></a>パラメーター - tableExist

sqltablename  
トランザクションを使用するかどうかを決定するブール フラグ; オプション。 既定では、false です。

<!-- -->

use\_within\_transaction  
トランザクションを使用するかどうかを決定するブール フラグ; オプション。 既定では、false です。

### <a name="return-value---tableexist"></a>戻り値 - tableExist

テーブルが存在する場合は true。それ以外の場合は、false。

## <a name="method-tablemetadata"></a>メソッド tableMetaData

データ ディクショナリ メタ データで SqlDescribe テーブルを入力します。

```xpp
public int tableMetaData(TableId tableId)
```

### <a name="parameters---tablemetadata"></a>パラメーター - tableMetaData

tableId  
テーブル ハンドル。

### <a name="return-value---tablemetadata"></a>戻り値 - tableMetaData

メソッドが成功した場合は true。

## <a name="method-tablereindex"></a>メソッド tableReindex

テーブルのインデックスを更新します。

```xpp
public int tableReindex([TableId tableId], [IndexId indexId])
```

### <a name="parameters---tablereindex"></a>パラメーター - tableReindex

tableId  
インデックス ハンドル (すべて0) (オプション)。 既定では 0 です。

<!-- -->

indexId  
インデックス ハンドル (すべて0) (オプション)。 既定では 0 です。

### <a name="return-value---tablereindex"></a>戻り値 - tableReindex

メソッドが成功した場合は 0。

## <a name="method-tablesynchronize"></a>メソッド tableSynchronize

テーブルと、SQL データベースのテーブルを同期します。

```xpp
public int tableSynchronize(TableId tableId, [boolean update_dict_info_only], [boolean check_indexes])
```

### <a name="parameters---tablesynchronize"></a>パラメーター - tableSynchronize

tableId  
設定すると、テーブルのインデックスの再インデックスを実行; 省略可能。 既定では、true です。

<!-- -->

update\_dict\_info\_only  
設定すると、テーブルのインデックスの再インデックスを実行; 省略可能。 既定では、true です。

<!-- -->

check\_indexes  
設定すると、テーブルのインデックスの再インデックスを実行; 省略可能。 既定では、true です。

### <a name="return-value---tablesynchronize"></a>返り値 - tableSynchronize

メソッドが成功した場合は true。

## <a name="method-tabletruncate"></a>メソッド tableTruncate

テーブルの切り詰め

```xpp
public int tableTruncate(TableId tableId, [boolean prompt_before_truncate], [boolean truncate_system_table])
```

### <a name="parameters---tabletruncate"></a>パラメーター - tableTruncate

tableId  
選択したテーブルがシステム場合に、テーブルを切り詰めるかどうかを決定するブール フラグ; オプション。 既定では、false です。

<!-- -->

prompt\_before\_truncate  
選択したテーブルがシステム場合に、テーブルを切り詰めるかどうかを決定するブール フラグ; オプション。 既定では、false です。

<!-- -->

truncate\_system\_table  
選択したテーブルがシステム場合に、テーブルを切り詰めるかどうかを決定するブール フラグ; オプション。 既定では、false です。

### <a name="return-value---tabletruncate"></a>戻り値 - tableTruncate

メソッドが成功した場合は 0。

## <a name="method-tabletruncateddl"></a>メソッド tableTruncateDDL

テーブルを切り詰めるため SQL ステートメントを生成および返します。

```xpp
public str tableTruncateDDL(TableId tableId)
```

### <a name="parameters---tabletruncateddl"></a>パラメーター - tableTruncateDDL

tableId  
切り詰めるテーブルのテーブル ハンドルです。

### <a name="return-value---tabletruncateddl"></a>戻り値 - tableTruncateDDL

テーブルを切り詰める SQL ステートメント。

## <a name="method-synchronize"></a>メソッド synchronize

データ ディクショナリと、SQL データベースのデータ ディクショナリを同期します。

```xpp
public static int synchronize([boolean synchronize_all])
```

### <a name="parameters---synchronize"></a>パラメーター - synchronize

synchronize\_all  
すべてのテーブルを同期するかどうかを示すブール フラグ; オプション。 True の場合、このメソッドは (カーネルによって欠陥とマークされているテーブルのみでなく) すべてのテーブルを同期します。 既定では、false です。

### <a name="return-value---synchronize"></a>戻り値 - synchronize

同期が成功した場合は true。それ以外の場合は、false。

## <a name="method-new"></a>メソッド new

SqlDataDictionary クラスの新しいインスタンスを初期化します。

```xpp
public void new()
```

## <a name="method-tabledelete"></a>メソッド tableDelete

SQL データベースでテーブルを削除します。

```xpp
public void tableDelete(TableId tableId)
```

### <a name="parameters---tabledelete"></a>パラメーター - tableDelete

tableId  

