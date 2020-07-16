---
title: SqlStatementExecutePermission クラス
description: このトピックでは、SqlStatementExecutePermission クラスについて説明します。
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
ms.openlocfilehash: db99dcff542b2f8d8f470734faf20a8fa438fc5f
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502799"
---
# <a name="class-sqlstatementexecutepermission"></a>クラス SqlStatementExecutePermission

[!include [banner](../../includes/banner.md)]

```xpp
class SqlStatementExecutePermission extends CodeAccessPermission
```

SQL を使用する機能をコントロールします。

## <a name="remarks"></a>備考

このクラスは、特定の API のアクセス許可をチェックするように設計されています。 保護されたすべての API のリストについては、「セキュリティで保護された API」を参照してください。 保護された API が実行される前に、対応する CodeAccessPermission::demand メソッドが呼び出される、通常はサーバー層である、同じ層で assert メソッドを呼び出す必要があります。 次のいずれかでサーバー層のメソッドを呼び出します:

-   サーバー静的メソッド �または�
-   RunOn クラス プロパティを使用して、サーバーで実行するように設定されているクラス インスタンス メソッド

## <a name="examples"></a>例

この例では、サーバー上で実行される CustTable テーブルで SQL クエリを実行します。 クエリの結果は、\_resultSet オブジェクトに格納されます。 assert メソッドが呼び出され、コードが、ファイルに対するデータの読み取り/書き込みを行うために使用される AsciiIo クラスをインスタンス化できることが宣言されます。

```xpp
server static void main(Args _args) 
{ 
    DictTable  _dictTable; 
    Connection _connection; 
    Statement  _statement; 
    str        _sql; 
    ResultSet  _resultSet; 
    SqlStatementExecutePermission _perm; 
    _dictTable = new DictTable(tableNum(CustTable)); 
    if (_dictTable != null) 
        { 
           _connection = new Connection(); 
           _sql = strfmt( "SELECT * FROM %1", _dictTable.name(DbBackend::Sql) ); 
           _perm = new SqlStatementExecutePermission(_sql); 
           // Check for permission to use the _statement. 
           _perm.assert(); 
           _statement = _connection.createStatement(); 
           _resultSet = _statement.executeQuery(_sql); 
           // End the scope of the assert call. 
           CodeAccessPermission::revertAssert(); 
        } 
}
```

## <a name="methods"></a>メソッド

| 方法                                                 | 説明                                                                      |
|--------------------------------------------------------|----------------------------------------------------------------------------------|
| public CodeAccessPermission copy()                     | 現在のアクセス許可クラス オブジェクトのコピーを作成し、返します。               |
| public boolean isSubsetOf(CodeAccessPermission target) | 現在のアクセス許可が指定したアクセス許可のサブセットかどうかを決定します。 |
| public void new(str sqlStatement)                      | SQLStatementExecutePermission クラスの新しいインスタンスを作成します。               |

## <a name="method-copy"></a>メソッド copy

現在のアクセス許可クラス オブジェクトのコピーを作成し、返します。

```xpp
public CodeAccessPermission copy()
```

### <a name="return-value---copy"></a>戻り値 - copy

現在のアクセス許可オブジェクトのコピーです。

### <a name="remarks---copy"></a>備考 - copy

CodeAccessPermission クラスからクラスを派生させる場合に、このメソッドを上書きします。 詳細については、「」を参照してください。

## <a name="method-issubsetof"></a>メソッド isSubsetOf

現在のアクセス許可が指定したアクセス許可のサブセットかどうかを決定します。

```xpp
public boolean isSubsetOf(CodeAccessPermission target)
```

### <a name="parameters---issubsetof"></a>パラメーター - isSubsetOf

target  
CodeAccessPermission クラス オブジェクト。

### <a name="return-value---issubsetof"></a>戻り値 - isSubsetOf

現在のアクセス許可が指定したアクセス許可のサブセットである場合は true。それ以外の場合は false。

### <a name="remarks---issubsetof"></a>備考 - isSubsetOf

CodeAccessPermission クラスからクラスを派生させる場合に、このメソッドを上書きします。 詳細については、「」を参照してください。

## <a name="method-new"></a>メソッド new

SQLStatementExecutePermission クラスの新しいインスタンスを作成します。

```xpp
public void new(str sqlStatement)
```

### <a name="parameters---new"></a>パラメーター - new

sqlStatement  
実行する SQL 文字列。

### <a name="examples---new"></a>例 - new

次の例では、サーバー上で実行される、CustTable テーブルで SQL クエリを実行します。 クエリの結果は、resultSet オブジェクトに格納されます。

```xpp
server static void main(Args _args) 
{ 
    DictTable  dictTable; 
    Connection connection; 
    Statement  statement; 
    str        sql; 
    ResultSet  resultSet; 
    SqlStatementExecutePermission perm; 
    dictTable = new DictTable(tableNum(CustTable)); 
    if (dictTable != null) 
        { 
           connection = new Connection(); 
           sql = strfmt( "SELECT * FROM %1", dictTable.name(DbBackend::Sql) ); 
           //Instantiate the permission class 
           perm = new SqlStatementExecutePermission(sql); 
           //check for permission to use statement 
           perm.assert(); 
           statement = connection.createStatement(); 
           resultSet = statement.executeQuery(sql); 
           //end the scope of the assert call 
           CodeAccessPermission::revertAssert(); 
        } 
}
```

