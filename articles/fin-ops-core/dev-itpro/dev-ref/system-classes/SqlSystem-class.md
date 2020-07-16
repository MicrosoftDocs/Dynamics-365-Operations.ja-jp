---
title: SqlSystem クラス
description: このトピックでは、SqlSystem クラスについて説明します。
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
ms.openlocfilehash: b7deeb330dea4de64044fdd3140959d1b1d7f85e
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502797"
---
# <a name="class-sqlsystem"></a>クラス SqlSystem

[!include [banner](../../includes/banner.md)]

```xpp
class SqlSystem extends Object
```

SqlSystem クラスには、有効な SQL システムに関する情報 (通常はログイン情報) が含まれます。

## <a name="remarks"></a>備考

## <a name="examples"></a>例

## <a name="methods"></a>メソッド

| 方法                                                                                                                                   | 説明                                                                                             |
|------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------|
| public LoginProperty createLoginProperty()                                                                                               | データベースにログイン プロパティを作成します。                                       |
| public DatabaseId databaseId()                                                                                                           | SQL データベースのバックエンドとして使用されるデータベースの仕入先の ID を返します。          |
| public str databaseName()                                                                                                                | SQL データベースのバックエンドとして使用されるデータベースの仕入先の名前を返します。                               |
| public boolean dbRequestedUnicodeEnabled()                                                                                               | Unicode がデータベースでサポートされているかどうかを示す値を取得します。                             |
| public str filenameDeadlocks(str Userid)                                                                                                 | デッドロックのトレース ログ ファイルに固有のユーザーの名前を取得します。                                        |
| public str filenameQuerytimelimit(str Userid)                                                                                            | ユーザー固有の querytime 期限ログ ファイルの名前を取得します。                                        |
| public str filenameSqlTrace(str Userid)                                                                                                  | 特定のユーザーの SQL トレース ログ ファイルのファイル名を取得します。                                     |
| public str filenameWarnings(str Userid)                                                                                                  | 警告ログ ファイルに固有のユーザーの名前を取得します。                                              |
| public str logfileName(\[boolean fromCommandline\])                                                                                      | 標準的な SQL エラー ログ ファイルの名前を取得します。                            |
| public str loginConnectString()                                                                                                          | ODBC の完全な接続文字列を取得します。                                                              |
| public str loginDatabase()                                                                                                               | 現在接続されているデータベースの名前を取得します。                                              |
| public str loginDSN()                                                                                                                    | データベースに接続するために使用される Open Database Connectivity (ODBC) データ ソース名 (DSN) を取得します。 |
| public str loginName()                                                                                                                   | データベースにログインするために使用されるユーザー名を取得します。                                         |
| public str loginServer()                                                                                                                 | 現在接続されているデータベース サーバーの名前を取得します。                                       |
| public str monocaseFmt(\[TableId tableId\], \[FieldId fieldId\], \[boolean includingFieldName\], \[boolean considerSystemVariables\])    | 文字列を 1 つのケースにキャストするために使用される書式文字列を取得します ("NLS\_LOWER(%1)" など)。    |
| public str sqlLiteral(AnyType data, \[boolean forWhereClause\], \[boolean likeOperand\], \[boolean rightJustify\], \[int stringLength\]) | SQL タイプを修正するため入力 AX データ型を書式設定します。                                                      |
| ::public static boolean clusteredIndexes()                                                                                               |                                                                                                         |
| ::public static str databaseBackendDesc()                                                                                                |                                                                                                         |
| ::public static DatabaseId databaseBackendId()                                                                                           |                                                                                                         |
| ::public static str databaseBackendName()                                                                                                |                                                                                                         |
| ::public static DatabaseCLI databaseCallLevelInterface()                                                                                 |                                                                                                         |
| ::public static int databaseHints(\[int new\_hint\_value\])                                                                              |                                                                                                         |
| ::public static boolean functionalIndexes()                                                                                              |                                                                                                         |
| ::public static str modelDatabaseBackendName()                                                                                           | 現在接続されているモデル データベース AOS の名前を取得します。                                    |
| ::public static str managedConnectionString()                                                                                            |                                                                                                         |
| public void new()                                                                                                                        | SqlSystem クラスの新しいインスタンスを初期化します。                                                      |
| public void logfileWrite(str Text)                                                                                                       | テキスト文字列を標準 SQL エラー ログファイルに記述します。                         |

## <a name="method-createloginproperty"></a>メソッド createLoginProperty

データベースにログイン プロパティを作成します。

```xpp
public LoginProperty createLoginProperty()
```

### <a name="return-value---createloginproperty"></a>戻り値 - createLoginProperty

作成されたログイン プロパティ。

## <a name="method-databaseid"></a>メソッド databaseId

SQL データベースのバックエンドとして使用されるデータベースの仕入先の ID を返します。

```xpp
public DatabaseId databaseId()
```

### <a name="return-value---databaseid"></a>戻り値 - databaseId

SQL データベースのバックエンドとして使用されるデータベースの仕入先の ID。

### <a name="remarks---databaseid"></a>備考 - databaseId

データベースの仕入先が、何らかの理由で特定できない場合、列挙 DbBackend::UNKNOWN が返されます。

## <a name="method-databasename"></a>メソッド databaseName

SQL データベースのバックエンドとして使用されるデータベースの仕入先の名前を返します。

```xpp
public str databaseName()
```

### <a name="return-value---databasename"></a>戻り値 - databaseName

SQL データベースのバックエンドとして使用されるデータベースの仕入先の名前。

## <a name="method-dbrequestedunicodeenabled"></a>メソッド dbRequestedUnicodeEnabled

Unicode がデータベースでサポートされているかどうかを示す値を取得します。

```xpp
public boolean dbRequestedUnicodeEnabled()
```

### <a name="return-value---dbrequestedunicodeenabled"></a>戻り値 - dbRequestedUnicodeEnabled

Unicode がデータベースでサポートされているかどうかを示す値。

## <a name="method-filenamedeadlocks"></a>メソッド filenameDeadlocks

デッドロックのトレース ログ ファイルに固有のユーザーの名前を取得します。

```xpp
public str filenameDeadlocks(str Userid)
```

### <a name="parameters---filenamedeadlocks"></a>パラメーター - filenameDeadlocks

Userid  

### <a name="return-value---filenamedeadlocks"></a>戻り値 - filenameDeadlocks

デッドロックのトレース ログ ファイルに固有のユーザーの名前。

## <a name="method-filenamequerytimelimit"></a>メソッド filenameQuerytimelimit

ユーザー固有の querytime 期限ログ ファイルの名前を取得します。

```xpp
public str filenameQuerytimelimit(str Userid)
```

### <a name="parameters---filenamequerytimelimit"></a>パラメーター - filenameQuerytimelimit

Userid  

### <a name="return-value---filenamequerytimelimit"></a>戻り値 - filenameQuerytimelimit

ユーザー固有の querytime 期限ログ ファイルの名前。

## <a name="method-filenamesqltrace"></a>メソッド filenameSqlTrace

特定のユーザーの SQL トレース ログ ファイルのファイル名を取得します。

```xpp
public str filenameSqlTrace(str Userid)
```

### <a name="parameters---filenamesqltrace"></a>パラメーター - filenameSqlTrace

Userid  
ユーザー ID。

### <a name="return-value---filenamesqltrace"></a>戻り値 - filenameSqlTrace

SQL 追跡ログのファイル名。

## <a name="method-filenamewarnings"></a>メソッド filenameWarnings

警告ログ ファイルに固有のユーザーの名前を取得します。

```xpp
public str filenameWarnings(str Userid)
```

### <a name="parameters---filenamewarnings"></a>パラメーター - filenameWarnings

Userid  
関係ユーザーの識別子。

### <a name="return-value---filenamewarnings"></a>戻り値 - filenameWarnings

警告ログ ファイルに固有のユーザーの名前。

## <a name="method-logfilename"></a>メソッド logfileName

標準的な SQL エラー ログ ファイルの名前を取得します。

```xpp
public str logfileName([boolean fromCommandline])
```

### <a name="parameters---logfilename"></a>パラメーター - logfileName

fromCommandline  
ブール値。 パラメーターとしてゼロ以外の値を渡すと、コマンド ラインで渡されるログファイル名が呼び出しにより返されます (オプション)。

### <a name="return-value---logfilename"></a>戻り値 - logfileName

標準 SQL エラー ログ ファイルのファイル名。

### <a name="remarks---logfilename"></a>備考 - logfileName

バージョン 2.11 以降では、空の文字列が返されます (下位互換性のため)。 ログ ファイル名を取得するには、filenameSqlError メソッドを使用します。

## <a name="method-loginconnectstring"></a>メソッド loginConnectString

ODBC の完全な接続文字列を取得します。

```xpp
public str loginConnectString()
```

### <a name="return-value---loginconnectstring"></a>戻り値 - loginConnectString

ODBC の完全な接続文字列。

## <a name="method-logindatabase"></a>メソッド loginDatabase

現在接続されているデータベースの名前を取得します。

```xpp
public str loginDatabase()
```

### <a name="return-value---logindatabase"></a>戻り値 - loginDatabase

現在接続されているデータベースの名前。

### <a name="examples---logindatabase"></a>例 - loginDatabase

```xpp
{ 
    SqlSystem SqlSystem = new SqlSystem(); 
    print SqlSystem.loginDatabase(); 
}
```

## <a name="method-logindsn"></a>メソッド loginDSN

データベースに接続するために使用される Open Database Connectivity (ODBC) データ ソース名 (DSN) を取得します。

```xpp
public str loginDSN()
```

### <a name="return-value---logindsn"></a>戻り値 - loginDSN

データベースへの接続に使用される ODBC データ ソース名の名前。

### <a name="remarks---logindsn"></a>備考 - loginDSN

既定の DSN は「BMSDSN」です。

### <a name="examples---logindsn"></a>例 - loginDSN

```xpp
{ 
    SqlSystem SqlSystem = new SqlSystem(); 
    print SqlSystem.loginDSN(); 
}
```

## <a name="method-loginname"></a>メソッド loginName

データベースにログインするために使用されるユーザー名を取得します。

```xpp
public str loginName()
```

### <a name="return-value---loginname"></a>戻り値 - loginName

データベースにログインするために使用されるユーザー名。

### <a name="examples---loginname"></a>例 - loginName

```xpp
{ 
    SqlSystem SqlSystem = new SqlSystem(); 
    print SqlSystem.loginName(); 
}
```

## <a name="method-loginserver"></a>メソッド loginServer

現在接続されているデータベース サーバーの名前を取得します。

```xpp
public str loginServer()
```

### <a name="return-value---loginserver"></a>戻り値 - loginServer

現在接続されているデータベースの名前。

### <a name="remarks---loginserver"></a>備考 - loginServer

データベースがサーバーの概念をサポートしていない場合は、空の文字列が返されます。

### <a name="examples---loginserver"></a>例 - loginServer

```xpp
{ 
    SqlSystem SqlSystem = new SqlSystem(); 
    print SqlSystem.loginServer(); 
}
```

## <a name="method-monocasefmt"></a>メソッド monocaseFmt

文字列を 1 つのケースにキャストするために使用される書式文字列を取得します ("NLS\_LOWER(%1)" など)。

```xpp
public str monocaseFmt([TableId tableId], [FieldId fieldId], [boolean includingFieldName], [boolean considerSystemVariables])
```

### <a name="parameters---monocasefmt"></a>パラメーター - monocaseFmt

tableId  

<!-- -->

fieldId  

<!-- -->

includingFieldName  

<!-- -->

considerSystemVariables  

### <a name="return-value---monocasefmt"></a>戻り値 - monocaseFmt

文字列を 1 つのケースにキャストするために使用される書式文字列。

### <a name="remarks---monocasefmt"></a>備考 - monocaseFmt

プレースホルダーの Finance and Operations アプリケーション スタイルが使用されます ("%1" など)。

## <a name="method-sqlliteral"></a>メソッド sqlLiteral

SQL タイプを修正するため入力 AX データ型を書式設定します。

```xpp
public str sqlLiteral(AnyType data, [boolean forWhereClause], [boolean likeOperand], [boolean rightJustify], [int stringLength])
```

### <a name="parameters---sqlliteral"></a>パラメーター - sqlLiteral

データ  
文字列の長さ。 既定ではゼロに等しくなります。

<!-- -->

forWhereClause  
文字列の長さ。 既定ではゼロに等しくなります。

<!-- -->

likeOperand  
文字列の長さ。 既定ではゼロに等しくなります。

<!-- -->

rightJustify  
文字列の長さ。 既定ではゼロに等しくなります。

<!-- -->

stringLength  
文字列の長さ。 既定ではゼロに等しくなります。

### <a name="return-value---sqlliteral"></a>戻り値 - sqlLiteral

書式設定された SQL 型文字列。

## <a name="method-clusteredindexes"></a>メソッド clusteredIndexes

```xpp
public static boolean clusteredIndexes()
```

### <a name="return-value---clusteredindexes"></a>戻り値 - clusteredIndexes

## <a name="method-databasebackenddesc"></a>メソッド databaseBackendDesc

```xpp
public static str databaseBackendDesc()
```

### <a name="return-value---databasebackenddesc"></a>戻り値 - databaseBackendDesc

## <a name="method-databasebackendid"></a>メソッド databaseBackendId

```xpp
public static DatabaseId databaseBackendId()
```

### <a name="return-value---databasebackendid"></a>戻り値 - databaseBackendId

## <a name="method-databasebackendname"></a>メソッド databaseBackendName

```xpp
public static str databaseBackendName()
```

### <a name="return-value---databasebackendname"></a>戻り値 - databaseBackendName

## <a name="method-databasecalllevelinterface"></a>メソッド databaseCallLevelInterface

```xpp
public static DatabaseCLI databaseCallLevelInterface()
```

### <a name="return-value---databasecalllevelinterface"></a>戻り値 - databaseCallLevelInterface

## <a name="method-databasehints"></a>メソッド databaseHints

```xpp
public static int databaseHints([int new_hint_value])
```

### <a name="parameters---databasehints"></a>パラメーター - databaseHints

new\_hint\_value  

### <a name="return-value---databasehints"></a>戻り値 - databaseHints

## <a name="method-functionalindexes"></a>メソッド functionalIndexes

```xpp
public static boolean functionalIndexes()
```

### <a name="return-value---functionalindexes"></a>戻り値 - functionalIndexes

## <a name="method-modeldatabasebackendname"></a>メソッド modelDatabaseBackendName

現在接続されているモデル データベース AOS の名前を取得します。

```xpp
public static str modelDatabaseBackendName()
```

### <a name="return-value---modeldatabasebackendname"></a>戻り値 - modelDatabaseBackendName

現在接続されているモデル データベースの名前。

## <a name="method-managedconnectionstring"></a>メソッド managedConnectionString

```xpp
public static str managedConnectionString()
```

### <a name="return-value---managedconnectionstring"></a>戻り値 - managedConnectionString

## <a name="method-new"></a>メソッド new

SqlSystem クラスの新しいインスタンスを初期化します。

```xpp
public void new()
```

## <a name="method-logfilewrite"></a>メソッド logfileWrite

テキスト文字列を標準 SQL エラー ログファイルに記述します。

```xpp
public void logfileWrite(str Text)
```

### <a name="parameters---logfilewrite"></a>パラメーター - logfileWrite

テキスト  
ログファイルに書き込むテキスト (ブックマークなど)。

### <a name="remarks---logfilewrite"></a>備考 - logfileWrite

あらゆる種類のエラー状況 (ログ ファイルに記録される) に従い、現在のシナリオを説明する個人用ブックマークを挿入します。

### <a name="examples---logfilewrite"></a>例 - logfileWrite

```xpp
static void myExample(Args _args) 
{ 
    SqlSystem SqlSystem; 
    SqlSystem = new SqlSystem(); 
    SqlSystem.logfileWrite("Recheck the returned data."); 
}
```

