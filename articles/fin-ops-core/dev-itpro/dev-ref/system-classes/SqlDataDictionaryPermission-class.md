---
title: SqlDataDictionaryPermission クラス
description: このトピックでは、SqlDataDictionaryPermission クラスについて説明します。
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
ms.openlocfilehash: af3ed2311289f170328d1cc9d0f4cebcacc2333b
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502800"
---
# <a name="class-sqldatadictionarypermission"></a>クラス SqlDataDictionaryPermission

[!include [banner](../../includes/banner.md)]

```xpp
class SqlDataDictionaryPermission extends CodeAccessPermission
```

SqlDataDictionaryPermission クラスは、メソッドにアクセスする機能を制御し、特定の API のアクセス許可を確認するように設計されています。 保護されたすべての API のリストについては、「セキュリティで保護された API」を参照してください。

## <a name="remarks"></a>備考

保護された API が実行される前に、対応する CodeAccessPermission::demand メソッドが呼び出される、通常はサーバー層である、同じ層で assert メソッドを呼び出す必要があります。 次のいずれかでサーバー層のメソッドを呼び出します:

-   サーバー静的メソッド
-   RunOn クラス プロパティを使用して、サーバーで実行するように設定されているクラス インスタンス メソッド。

## <a name="examples"></a>例

次の例では、xRefNames テーブルからデータを削除します。 assert メソッドが呼び出され、コードが、ファイルに対するデータの読み取り/書き込みを行うために使用される AsciiIo クラスをインスタンス化できることが宣言されます。

```xpp
{ 
    DictTable dictTable = new DictTable(tablenum(xRefNames)); 
    str sqlTableName; 
    SqlDataDictionary sqlTable; 
    if (dictTable && dictTable.enabled()) 
    { 
        sqlTableName = dictTable.name(DbBackend::Sql); 
        sqlTable = new SqlDataDictionary(); 
        // Try to truncate only if the table does exist 
        // in the SQL database. 
        if (sqlTable.tableExist(sqlTableName)) 
        { 
            new SqlDataDictionaryPermission( 
                methodstr(SqlDataDictionary, tableTruncate)).assert(); 
            sqlTable.tableTruncate(tablenum(xRefNames)); 
            CodeAccessPermission::revertAssert(); 
        } 
    } 
}
```

## <a name="methods"></a>メソッド

| 方法                                                 | 説明                                                                      |
|--------------------------------------------------------|----------------------------------------------------------------------------------|
| public CodeAccessPermission copy()                     | 現在のアクセス許可クラス オブジェクトのコピーを作成し、返します。               |
| public boolean isSubsetOf(CodeAccessPermission target) | 現在のアクセス許可が指定したアクセス許可のサブセットかどうかを決定します。 |
| public void new(IdentifierName methodName)             | SQLDataDictionaryPermission クラスの新しいインスタンスを作成します。                 |

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

現在のアクセス許可が指定したアクセス許可のサブセットである場合は true。それ以外の場合は、false。

### <a name="remarks---issubsetof"></a>備考 - isSubsetOf

CodeAccessPermission クラスからクラスを派生させる場合に、このメソッドを上書きします。 詳細については、「」を参照してください。

## <a name="method-new"></a>メソッド new

SQLDataDictionaryPermission クラスの新しいインスタンスを作成します。

```xpp
public void new(IdentifierName methodName)
```

### <a name="parameters---new"></a>パラメーター - new

methodName  
呼び出されるメソッドの名前を表す文字列。

### <a name="examples---new"></a>例 - new

次のコード例は、xRefNames テーブルのデータを削除します。

```xpp
server static void main(Args _args) 
{ 
    DictTable dictTable = new DictTable(tablenum(xRefNames)); 
    str sqlTableName; 
    SqlDataDictionary sqlTable; 
    if (dictTable && dictTable.enabled()) 
    { 
        sqlTableName = dictTable.name(DbBackend::Sql); 
        sqlTable = new SqlDataDictionary(); 
        // Only try to truncate if the table does exist 
        // in the SQL database 
        if (sqlTable.tableExist(sqlTableName)) 
        { 
            new SqlDataDictionaryPermission( 
                methodstr(SqlDataDictionary, tableTruncate)).assert(); 
            sqlTable.tableTruncate(tablenum(xRefNames)); 
            CodeAccessPermission::revertAssert(); 
        } 
    } 
}
```

