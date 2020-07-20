---
title: Statement クラス
description: このトピックでは、Statement クラスについて説明します。
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
ms.openlocfilehash: 85fe4a09e8c6b0f041869418da5921a489b95fd9
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502796"
---
# <a name="class-statement"></a>クラスの明細書

[!include [banner](../../includes/banner.md)]

```xpp
class Statement extends Object
```

Statement クラスは、静的 SQL ステートメントを実行し、生成された結果を取得します。

## <a name="remarks"></a>備考

明細書ごとに 1 つだけ、任意の時点で開くことができます。 したがって、1 つの ResultSet の読み込みが別の ResultSet の読み込みとインターリーブされている場合は、それぞれ異なるステートメントによって生成されている必要があります。 レコードとフィールド レベルのセキュリティは、明細書クラスでは適用されません。 したがって、明示的なセキュリティ検証を行わずにユーザーに返されるデータを公開していないことを、確認してください。 すべての実行可能な明細メソッドは現在 ResultSet で開いている場合明細書は暗黙的に閉じます。

## <a name="examples"></a>例

```xpp
static void example() 
{ 
    Connection Con; 
    Statement Stmt; 
    ResultSet R; 
    SqlStatementExecutePermission perm; 
    str sql = 'SELECT VALUE FROM SQLSYSTEMVARIABLES'; 
    Con = new Connection(); 
    Stmt = Con.createStatement(); 
    perm = new SqlStatementExecutePermission(sql); 
    perm.assert(); 
    R = Stmt.executeQuery(sql); 
    while ( R.next() ) 
    { 
        print R.getString(1); 
    } 
}
```

## <a name="methods"></a>メソッド

| 方法                                       | 説明                                                                                       |
|----------------------------------------------|---------------------------------------------------------------------------------------------------|
| public ResultSet executeQuery(str statement) | インスタンスの the を返す SQL ステートメントを実行します。                                       |
| public int executeUpdate(str statement)      | SQL INSERT、UPDATE、または DELETE ステートメントを実行します。                                               |
| public int getLastError()                    | 最後の SQL 操作の SQL データベース バックエンドによって返されたエラー コードを取得します。         |
| public str getLastErrorText()                | 最後の SQL 操作の SQL データベース バックエンドによって返されたエラー テキストを取得します。 |
| public int getMaxFieldSize()                 | 現在の列の最大サイズ制限を返します (ある場合)。                                            |
| public void close()                          | ステートメント オブジェクトのデータベースのリソースを解放します。                                            |
| public void setMaxFieldSize(int max)         | 列の最大サイズ制限を設定します。                                                               |

## <a name="method-executequery"></a>メソッド executeQuery

インスタンスの the を返す SQL ステートメントを実行します。

```xpp
public ResultSet executeQuery(str statement)
```

### <a name="parameters---executequery"></a>パラメーター - executeQuery

明細書  
結果セットを取得するために使用される SQL ステートメントを含む文字列。

### <a name="return-value---executequery"></a>戻り値 - executeQuery

クエリから返されたデータを含むオブジェクト。

### <a name="remarks---executequery"></a>備考 - executeQuery

ユーザーが executeQuery メソッドへの入力を制御すると、SQL インジェクション攻撃が発生する可能性があります。 したがって、このメソッドは、コード アクセス セキュリティで実行されます。 サーバー上でこのメソッドを呼び出すには、 からのアクセス許可が必要です。 SQL ステートメントを実行するための安全な方法は次のとおりです。

-   クエリ
-   ビュー
-   X++ select ステートメント

レコード レベル セキュリティは、明細書クラスでは適用されません。 データがユーザーに公開されている場合は、明示的セキュリティ検証を実行します。

### <a name="examples---executequery"></a>例 - executeQuery

次の例では、サーバー上で実行される、CustTable で SQL クエリを実行します。 クエリの結果は、resultSet オブジェクトに格納されます。

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
           perm = new SqlStatementExecutePermission(sql); 
           // Check for permission to use the statement. 
           perm.assert(); 
           statement = connection.createStatement(); 
           resultSet = statement.executeQuery(sql); 
           // End the scope of the assert call. 
           CodeAccessPermission::revertAssert(); 
        } 
}
```

## <a name="method-executeupdate"></a>メソッド executeUpdate

SQL INSERT、UPDATE、または DELETE ステートメントを実行します。

```xpp
public int executeUpdate(str statement)
```

### <a name="parameters---executeupdate"></a>パラメーター - executeUpdate

明細書  
データベースに渡される SQL ステートメントを含む文字列。

### <a name="return-value---executeupdate"></a>戻り値 - executeUpdate

更新された行数。それ以外は、何も返さない SQL ステートメントの 0 (ゼロ)。

### <a name="remarks---executeupdate"></a>備考 - executeUpdate

SQLDDL ステートメントなど、何も返さない SQL ステートメントを実行することもできます。 ユーザーが executeUpdate メソッドへの入力を制御すると、SQL インジェクション攻撃が発生する可能性があります。 したがって、このメソッドは、コード アクセス セキュリティで実行されます。 サーバー上でこのメソッドを呼び出すには、 からのアクセス許可が必要です。 データベースとやり取りするための安全な方法は次のとおりです。

-   クエリ
-   ビュー
-   X++ select ステートメント

レコード レベル セキュリティは、明細書クラスでは適用されません。 データがユーザーに公開されている場合は、明示的セキュリティ検証を実行します。

## <a name="method-getlasterror"></a>メソッド getLastError

最後の SQL 操作の SQL データベース バックエンドによって返されたエラー コードを取得します。

```xpp
public int getLastError()
```

### <a name="return-value---getlasterror"></a>戻り値 - getLastError

最後の SQL 操作の SQL データベース バックエンドによって返されたエラー コード。成功の場合は 0 です。

### <a name="examples---getlasterror"></a>例 - getLastError

```xpp
static void StatementGetLastError()  
{ 
    str sql, sql2; 
    UserConnection Connection = new UserConnection(); 
    Statement Statement = Connection.createStatement(); 
    boolean clear_infolog = false; 
    print "-Delete-a-non-existing-record-(valid statement)-----------"; 
    sql = "delete from zipcode where Recid = 2"; 
    new SqlStatementExecutePermission(sql).assert(); 
    Statement.executeUpdate(sql); 
    print " Error code was: ", Statement.getLastError(); 
    print " Error message was '", Statement.getLastErrorText(), "'"; 
    try 
    { 
        print "\n"; 
        print "-Delete-from-a-non-existing-table-(invalid statement)---    --"; 
        sql2 = "delete from StrangeTable07"; 
        new SqlStatementExecutePermission(sql2).assert(); 
        Statement.executeUpdate(sql2); 
    } 
    catch (exception::Error) 
    { 
        print "Exception was caught:"; 
        print " Error code was: ", Statement.getLastError(); 
        print " Error message was '", Statement.getLastErrorText(), "'"; 
    } 
    CodeAccessPermission::revertAssert(); 
    pause; 
}
```

## <a name="method-getlasterrortext"></a>メソッド getLastErrorText

最後の SQL 操作の SQL データベース バックエンドによって返されたエラー テキストを取得します。

```xpp
public str getLastErrorText()
```

### <a name="return-value---getlasterrortext"></a>戻り値 - getLastErrorText

最後の SQL 操作の SQL データベースによって提供されるエラー テキスト。

## <a name="method-getmaxfieldsize"></a>メソッド getMaxFieldSize

現在の列の最大サイズ制限を返します (ある場合)。

```xpp
public int getMaxFieldSize()
```

### <a name="return-value---getmaxfieldsize"></a>戻り値 - getMaxFieldSize

現在の列の最大サイズ制限。0 は無制限を意味します。

### <a name="remarks---getmaxfieldsize"></a>備考 - getMaxFieldSize

maxFieldSize の制限 (バイト単位) は、任意の列の値に対して返されるデータの最大量です。binary、varbinary、longvarbinary、char、varchar、および longvarchar 列にのみ適用されます。 制限を超過した場合、余分なデータは通知なしに破棄されます。

## <a name="method-close"></a>メソッド close

ステートメント オブジェクトのデータベースのリソースを解放します。

```xpp
public void close()
```

## <a name="method-setmaxfieldsize"></a>メソッド setMaxFieldSize

列の最大サイズ制限を設定します。

```xpp
public void setMaxFieldSize(int max)
```

### <a name="parameters---setmaxfieldsize"></a>パラメーター - setMaxFieldSize

最大  
列の新しい最大サイズ制限。0 は無制限を意味します。

### <a name="remarks---setmaxfieldsize"></a>備考 - setMaxFieldSize

maxFieldSize の制限 (バイト単位) は、任意の列の値に対して返されるデータのサイズを制限するように設定されています。binary、varbinary、longvarbinary、char、varchar、および longvarchar フィールドにのみ適用されます。 制限を超過した場合、余分なデータは通知なしに破棄されます。 最大可搬性については、256 より大きい値を使用します。

