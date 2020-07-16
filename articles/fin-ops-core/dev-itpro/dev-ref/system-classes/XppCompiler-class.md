---
title: XppCompiler クラス
description: このトピックでは、XppCompiler クラスについて説明します。
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
ms.openlocfilehash: 14f88fa8bae3e8610f8b1b5d66ccb12de5a32872
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502772"
---
# <a name="class-xppcompiler"></a>クラス XppCompiler

[!include [banner](../../includes/banner.md)]

```xpp
class XppCompiler extends Object
```

## <a name="remarks"></a>備考

## <a name="examples"></a>例

## <a name="methods"></a>メソッド

| 方法                                 | 説明                                                                                                       |
|----------------------------------------|-------------------------------------------------------------------------------------------------------------------|
| public boolean compile(str source)     |                                                                                                                   |
| public boolean compileExpr(str source) |                                                                                                                   |
| public str dumpClass(str className)    | クラスの X++ コンパイラ情報を含む XML 文字列を作成します。                                     |
| public str dumpEnums()                 | 現在のアプリケーション内のすべての列挙値の X++ コンパイラ情報を含む XML 文字列を作成します。 |
| public str dumpTable(str tableName)    | テーブルの X++ コンパイラ情報を含む XML 文字列を作成します。                                     |
| public str errorText()                 |                                                                                                                   |
| public AnyType execute(VarArg )        |                                                                                                                   |
| public AnyType executeEx()             |                                                                                                                   |
| public void setGuidArg(Guid arg)       |                                                                                                                   |
| public void setInt64Arg(Int64 arg)     |                                                                                                                   |
| public void setDateArg(Date arg)       |                                                                                                                   |
| public void new()                      | XppCompiler クラスの新しいインスタンスを初期化します。                                                              |
| public void endArgs()                  |                                                                                                                   |
| public void startArgs()                |                                                                                                                   |
| public void setRealArg(Real arg)       |                                                                                                                   |
| public void setIntArg(int arg)         |                                                                                                                   |
| public void setStrArg(str arg)         |                                                                                                                   |

## <a name="method-compile"></a>メソッド compile

```xpp
public boolean compile(str source)
```

### <a name="parameters---compile"></a>パラメーター - compile

ソース  

### <a name="return-value---compile"></a>戻り値 - compile

## <a name="method-compileexpr"></a>メソッド compileExpr

```xpp
public boolean compileExpr(str source)
```

### <a name="parameters---compileexpr"></a>パラメーター - compileExpr

ソース  

### <a name="return-value---compileexpr"></a>戻り値 - compileExpr

## <a name="method-dumpclass"></a>メソッド dumpClass

クラスの X++ コンパイラ情報を含む XML 文字列を作成します。

```xpp
public str dumpClass(str className)
```

### <a name="parameters---dumpclass"></a>パラメーター - dumpClass

className  

### <a name="return-value---dumpclass"></a>戻り値 - dumpClass

指定したクラスの X++ コンパイラ情報

### <a name="remarks---dumpclass"></a>備考 - dumpClass

バージョンからバージョンへの警告なしで出力形式が変わる可能性があるため、このメソッドの一般的な使用は非推奨です。

## <a name="method-dumpenums"></a>メソッド dumpEnums

現在のアプリケーション内のすべての列挙値の X++ コンパイラ情報を含む XML 文字列を作成します。

```xpp
public str dumpEnums()
```

### <a name="return-value---dumpenums"></a>戻り値 - dumpEnums

現在のアプリケーション内のすべての列挙値の X++ コンパイラ情報

### <a name="remarks---dumpenums"></a>備考 - dumpEnums

バージョンからバージョンへの警告なしで出力形式が変わる可能性があるため、このメソッドの一般的な使用は非推奨です。

## <a name="method-dumptable"></a>メソッド dumpTable

テーブルの X++ コンパイラ情報を含む XML 文字列を作成します。

```xpp
public str dumpTable(str tableName)
```

### <a name="parameters---dumptable"></a>パラメーター - dumpTable

tableName  

### <a name="return-value---dumptable"></a>戻り値 - dumpTable

指定したテーブルの X++ コンパイラ情報

### <a name="remarks---dumptable"></a>備考 - dumpTable

バージョンからバージョンへの警告なしで出力形式が変わる可能性があるため、このメソッドの一般的な使用は非推奨です。

## <a name="method-errortext"></a>メソッド errorText

```xpp
public str errorText()
```

### <a name="return-value---errortext"></a>戻り値 - errorText

## <a name="method-execute"></a>メソッド execute

```xpp
public AnyType execute(VarArg )
```

### <a name="parameters---execute"></a>パラメーター - execute


### <a name="return-value---execute"></a>戻り値 - execute

### <a name="remarks---execute"></a>備考 - execute

XppCompiler オブジェクトは実行時にコードをコンパイルすることができます。 これはセキュリティ リスクをもたらします。 したがって、メソッドは、コード アクセス セキュリティで実行されます。 サーバー上でこのメソッドを呼び出すには、ExecutePermission クラスからのアクセス許可が必要です。 ユーザーがこのメソッドを呼び出すコントロールで、SysDevelopment へのセキュリティ キーを設定して開発権限を持っていることを確認します。

### <a name="examples---execute"></a>例 - execute

次の例では、execute メソッドを呼び出して、指定されたバッファをコンパイルして実行します。

```xpp
void XppCompilerExecuteExample(Common _buf) 
{ 
    XppCompiler       xpp; 
    ExecutePermission perm; 
    perm = new ExecutePermission(); 
    if (perm == null) 
    { 
        return; 
    } 
    perm.assert(); 
    xpp = new XppCompiler(); 
    if (xpp != null) 
    { 
        xpp.execute(_buf); 
    } 
    CodeAccessPermission::revertAssert(); 
}
```

## <a name="method-executeex"></a>メソッド executeEx

```xpp
public AnyType executeEx()
```

### <a name="return-value---executeex"></a>戻り値 - executeEx

### <a name="remarks---executeex"></a>備考 - executeEx

XppCompiler オブジェクトは実行時にコードをコンパイルすることができます。 これはセキュリティ リスクをもたらします。 したがって、executeEx メソッドは、コード アクセス セキュリティで実行されます。 サーバー上でこのメソッドを呼び出すには、ExecutePermission クラスからのアクセス許可が必要です。 ユーザーがこのメソッドを呼び出すコントロールで、SysDevelopment へのセキュリティ キーを設定して開発権限を持っていることを確認します。

### <a name="examples---executeex"></a>例 - executeEx

```xpp
void XppCompilerExecuteExExample() 
{ 
    XppCompiler       xpp; 
    ExecutePermission perm; 
    perm = new ExecutePermission(); 
    if (perm == null) 
    { 
        return; 
    } 
    perm.assert(); 
    xpp = new XppCompiler(); 
    if (xpp != null) 
    { 
        xpp.executeEx(); 
    } 
    CodeAccessPermission::revertAssert(); 
}
```

## <a name="method-setguidarg"></a>メソッド setGuidArg

```xpp
public void setGuidArg(Guid arg)
```

### <a name="parameters---setguidarg"></a>パラメーター - setGuidArg

arg  

## <a name="method-setint64arg"></a>メソッド setInt64Arg

```xpp
public void setInt64Arg(Int64 arg)
```

### <a name="parameters---setint64arg"></a>パラメーター - setInt64Arg

arg  

## <a name="method-setdatearg"></a>メソッド setDateArg

```xpp
public void setDateArg(Date arg)
```

### <a name="parameters---setdatearg"></a>パラメーター - setDateArg

arg  

## <a name="method-new"></a>メソッド new

XppCompiler クラスの新しいインスタンスを初期化します。

```xpp
public void new()
```

### <a name="remarks---new"></a>備考 - new

XppCompiler クラスのインスタンスは、実行時にコードをコンパイルできます。 これはセキュリティ リスクを提示するため、新しいメソッドはコード アクセス セキュリティで実行されます。 サーバー上でこのメソッドを呼び出すには、ExecutePermission クラスからのアクセス許可が必要です。

## <a name="method-endargs"></a>メソッド endArgs

```xpp
public void endArgs()
```

## <a name="method-startargs"></a>メソッド startArgs

```xpp
public void startArgs()
```

## <a name="method-setrealarg"></a>メソッド setRealArg

```xpp
public void setRealArg(Real arg)
```

### <a name="parameters---setrealarg"></a>パラメーター - setRealArg

arg  

## <a name="method-setintarg"></a>メソッド setIntArg

```xpp
public void setIntArg(int arg)
```

### <a name="parameters---setintarg"></a>パラメーター - setIntArg

arg  

## <a name="method-setstrarg"></a>メソッド setStrArg

```xpp
public void setStrArg(str arg)
```

### <a name="parameters---setstrarg"></a>パラメーター - setStrArg

arg  

