---
title: 接続クラス
description: このトピックでは、接続クラスについて説明します。
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
ms.openlocfilehash: 8ad277098946056d4fc9c8b12010404a616af0a0
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502706"
---
# <a name="class-connection"></a>クラス接続

[!include [banner](../../includes/banner.md)]

```xpp
class Connection extends Object
```

接続クラスは、SQL ステートメントを実行して結果を返す現在のデータベース セッションを確立します。

## <a name="remarks"></a>備考

次のクラスは Connection クラスを拡張しています。

-   OdbcConnection
-   OciConnection
-   UserConnection

## <a name="examples"></a>例

次の例では、createStatement メソッドはステートメント オブジェクトを初期化します。 Statement.executeQuery メソッドは、SQL ステートメントを実行し、ResultSet オブジェクトに取得したデータを格納します。

```xpp
server static void main(Args args) 
{ 
    Connection con = new Connection(); 
    Statement stmt = con.createStatement(); 
    ResultSet r; 
    str sql; 
    SqlStatementExecutePermission perm; 
```

```xpp
    sql = strfmt('SELECT VALUE FROM SQLSYSTEMVARIABLES'); 
```

```xpp
    // Set code access permission to help protect the use of 
    // Statement.executeUpdate. 
    perm = new SqlStatementExecutePermission(sql); 
    perm.assert(); 
```

```xpp
    try 
    { 
        r = stmt.executeQuery(sql); 
        while (r.next()) 
        { 
            print r.getString(1); 
            pause; 
        } 
    } 
    catch (exception::Error) 
    { 
        print "An error occurred in the query."; 
        pause; 
    } 
    // Code access permission scope ends here. 
    CodeAccessPermission::revertAssert(); 
}
```

## <a name="methods"></a>メソッド

| 方法                                                                                                           | 説明                                                                                                                                                                             |
|------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| public Statement createStatement(\[ResultSetType resultSetType\], \[ResultSetConcurrency resultSetConcurrency\]) | SQL ステートメントの実行に使用されるステートメント オブジェクトを作成します。                                                                                                                    |
| public int odbcGetInfoInt(int InfoId)                                                                            | ODBC ドライバに関する情報と接続に関連付けられているデータのソースを取得する SQLGetInfo Open Database Connectivity (ODBC) 関数へのインターフェイスを提供します。 |
| public int odbcGetInfoLong(int InfoId)                                                                           | ODBC ドライバに関する情報と接続に関連付けられているデータのソースを取得する SQLGetInfo ODBC 関数へのインターフェイスを提供します。                              |
| public str odbcGetInfoStr(int InfoId)                                                                            | ODBC ドライバに関する情報と接続に関連付けられているデータのソースを文字列形式で取得する SQLGetInfo ODBC 関数へのインターフェイスを提供します。           |
| public str toString()                                                                                            | 接続オブジェクトを文字列に変換します。                                                                                                                                             |
| public int ttsLevel()                                                                                            | トランザクションを開始するために使用する ttsbegin メソッドの最後の呼び出しの数を返します。                                                                                        |
| public boolean isInTransactionScope()                                                                            |                                                                                                                                                                                         |
| public void finalize()                                                                                           |                                                                                                                                                                                         |
| public void transactionScopeAbort()                                                                              |                                                                                                                                                                                         |
| public void ttsNotifyCommit()                                                                                    | ttscommit メソッドが呼び出されると呼び出されます。                                                                                                                                          |
| public void transactionScopeBegin()                                                                              |                                                                                                                                                                                         |
| public void transactionScopeCommit()                                                                             |                                                                                                                                                                                         |
| public void ttsNotifyBegin()                                                                                     |                                                                                                                                                                                         |
| public void ttsbegin()                                                                                           | トランザクションを開始します。                                                                                                                                                                   |
| public void ttsabort()                                                                                           | トランザクションに関連する変更を破棄し、データベースを元の状態にロールバックします。                                                                              |
| public void new()                                                                                                | Connection クラスの新しいインスタンスを初期化します。                                                                                                                                     |
| public void ttsNotifyAbort()                                                                                     | 例外がスローされると呼び出されます。                                                                                                                                                  |
| public void ttscommit()                                                                                          | トランザクションに関連付けられている変更をデータベースにコミットします。                                                                                                             |

## <a name="method-createstatement"></a>メソッド createStatement

SQL ステートメントの実行に使用されるステートメント オブジェクトを作成します。

```xpp
public Statement createStatement([ResultSetType resultSetType], [ResultSetConcurrency resultSetConcurrency])
```

### <a name="parameters---createstatement"></a>パラメータ - createStatement

resultSetType  
既定で読み取り専用を指定する ResultSetConcurrency 列挙。

<!-- -->

resultSetConcurrency  
既定で読み取り専用を指定する ResultSetConcurrency 列挙。

### <a name="return-value---createstatement"></a>戻り値 - createStatement

新しいステートメント オブジェクトであるデータ型の値です。

### <a name="remarks---createstatement"></a>備考 - createStatement

createStatement メソッドを使用して SQL ステートメントを作成し、ユーザーがステートメントへの入力を制御できるようにすると、SQL インジェクション脅威の危険性があります。 詳細については [SQL インジェクション](https://go.microsoft.com/fwlink/?LinkId=114986) を参照してください。 AOT、ビュー、および X++ Select ステートメントでは、SQL ステートメントを実行するための安全な代替手段として、クエリ要素を使用することができます。

## <a name="method-odbcgetinfoint"></a>メソッド odbcGetInfoInt

ODBC ドライバに関する情報と接続に関連付けられているデータのソースを取得する SQLGetInfo Open Database Connectivity (ODBC) 関数へのインターフェイスを提供します。

```xpp
public int odbcGetInfoInt(int InfoId)
```

### <a name="parameters---odbcgetinfoint"></a>パラメーター - odbcGetInfoInt

InfoId  
ODBC 標準に従って要求された情報の ID を指定する整数。

### <a name="return-value---odbcgetinfoint"></a>戻り値 - odbcGetInfoInt

取得される情報の整数値。

### <a name="examples---odbcgetinfoint"></a>例 - odbcGetInfoInt

次の例では、odbcGetInfoInt メソッドは列名の最大の長さの整数値を返します。

```xpp
void getConnection() 
{ 
    Connection con; 
    Statement stmt; 
    int info; 
```

```xpp
    #define.SQL_MAX_COLUMN_NAME_LEN(30) 
    con = new Connection(); 
```

```xpp
    try 
    { 
        info = con.odbcGetInfoInt(#SQL_MAX_COLUMN_NAME_LEN); 
```

```xpp
        print info; 
        pause; 
     } 
```

```xpp
    catch(exception::Error) 
    { 
        print "An error occurred."; 
```

```xpp
    } 
```

```xpp
}
```

## <a name="method-odbcgetinfolong"></a>メソッド odbcGetInfoLong

ODBC ドライバに関する情報と接続に関連付けられているデータのソースを取得する SQLGetInfo ODBC 関数へのインターフェイスを提供します。

```xpp
public int odbcGetInfoLong(int InfoId)
```

### <a name="parameters---odbcgetinfolong"></a>パラメーター - odbcGetInfoLong

InfoId  
ODBC 標準による要求された情報の ID を指定する整数データ型です。

### <a name="return-value---odbcgetinfolong"></a>戻り値 - odbcGetInfoLong

取得される情報の整数データ型値です。

### <a name="remarks---odbcgetinfolong"></a>備考 - odbcGetInfoLong

このメソッドは 32 ビット整数を取得し、整数として返します。

### <a name="examples---odbcgetinfolong"></a>例 - odbcGetInfoLong

次の例では、odbcGetInfoLong メソッドは行の最大サイズの整数を返します。

```xpp
void getConnection() 
{ 
    Connection con; 
    Statement stmt; 
    int info; 
```

```xpp
    #define.SQL_MAX_ROW_SIZE(104) 
    con = new Connection(); 
```

```xpp
    try 
    { 
        info = con.odbcGetInfoLong(#SQL_MAX_ROW_SIZE); 
```

```xpp
        print info; 
        pause; 
     } 
```

```xpp
    catch(exception::Error) 
    { 
        print "An error occurred."; 
```

```xpp
    } 
```

```xpp
}
```

## <a name="method-odbcgetinfostr"></a>メソッド odbcGetInfoStr

ODBC ドライバに関する情報と接続に関連付けられているデータのソースを文字列形式で取得する SQLGetInfo ODBC 関数へのインターフェイスを提供します。

```xpp
public str odbcGetInfoStr(int InfoId)
```

### <a name="parameters---odbcgetinfostr"></a>パラメーター - odbcGetInfoStr

InfoId  
ODBC 標準による要求された情報の ID を指定する整数データ型です。

### <a name="return-value---odbcgetinfostr"></a>戻り値 - odbcGetInfoStr

取得される情報の文字列データ型値。

### <a name="examples---odbcgetinfostr"></a>例 - odbcGetInfoStr

次の例では、odbcGetInfoStr メソッドはデータベース管理システムの名前を返します。

```xpp
void getConnection() 
{ 
    Connection con; 
    str info; 
```

```xpp
    #define.SQL_DBMS_NAME(17) 
    con = new Connection(); 
```

```xpp
    try 
    { 
        info = con.odbcGetInfoStr(#SQL_DBMS_NAME); 
```

```xpp
        print info; 
        pause; 
     } 
```

```xpp
    catch(exception::Error) 
    { 
        print "An error occurred."; 
    } 
}
```

## <a name="method-tostring"></a>メソッド toString

接続オブジェクトを文字列に変換します。

```xpp
public str toString()
```

### <a name="return-value---tostring"></a>戻り値 - toString

接続オブジェクトの文字列値。

## <a name="method-ttslevel"></a>メソッド ttsLevel

トランザクションを開始するために使用する ttsbegin メソッドの最後の呼び出しの数を返します。

```xpp
public int ttsLevel()
```

### <a name="return-value---ttslevel"></a>戻り値 - ttsLevel

ttsbegin メソッドに最後の呼び出しの番号を示す整数値。 たとえば、ttsLevel メソッドが ttsbegin メソッドへの 3 回目の呼び出し後に呼び出されると、戻り値は 3 になります。

## <a name="method-isintransactionscope"></a>メソッド isInTransactionScope

```xpp
public boolean isInTransactionScope()
```

### <a name="return-value---isintransactionscope"></a>戻り値 - isInTransactionScope

## <a name="method-finalize"></a>メソッド finalize

```xpp
public void finalize()
```

## <a name="method-transactionscopeabort"></a>メソッド transactionScopeAbort

```xpp
public void transactionScopeAbort()
```

## <a name="method-ttsnotifycommit"></a>メソッド ttsNotifyCommit

ttscommit メソッドが呼び出されると呼び出されます。

```xpp
public void ttsNotifyCommit()
```

## <a name="method-transactionscopebegin"></a>メソッド transactionScopeBegin

```xpp
public void transactionScopeBegin()
```

## <a name="method-transactionscopecommit"></a>メソッド transactionScopeCommit

```xpp
public void transactionScopeCommit()
```

## <a name="method-ttsnotifybegin"></a>メソッド ttsNotifyBegin

```xpp
public void ttsNotifyBegin()
```

## <a name="method-ttsbegin"></a>メソッド ttsbegin

トランザクションを開始します。

```xpp
public void ttsbegin()
```

## <a name="method-ttsabort"></a>メソッド ttsabort

トランザクションに関連する変更を破棄し、データベースを元の状態にロールバックします。

```xpp
public void ttsabort()
```

## <a name="method-new"></a>メソッド new

Connection クラスの新しいインスタンスを初期化します。

```xpp
public void new()
```

## <a name="method-ttsnotifyabort"></a>メソッド ttsNotifyAbort

例外がスローされると呼び出されます。

```xpp
public void ttsNotifyAbort()
```

## <a name="method-ttscommit"></a>メソッド ttscommit

トランザクションに関連付けられている変更をデータベースにコミットします。

```xpp
public void ttscommit()
```

