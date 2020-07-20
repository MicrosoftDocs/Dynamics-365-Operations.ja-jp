---
title: CLRInterop クラス
description: このトピックでは、CLRInterop クラスについて説明します。
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
ms.openlocfilehash: b7dc64a05508c77e202ef69b63b99d78e694b5d8
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502718"
---
# <a name="class-clrinterop"></a>クラス CLRInterop

[!include [banner](../../includes/banner.md)]

```xpp
class CLRInterop extends Object
```

ClrInterop クラスは、タイプ マーシャ リングおよび例外処理の機能を提供するユーティリティ クラスです。 すべてのメソッドは静的であるため、クラスのインスタンス化をする必要はありません。

## <a name="remarks"></a>備考

## <a name="examples"></a>例

## <a name="methods"></a>方法

| 方法                                                                               | 説明                                                                                                                              |
|--------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| ::public static AnyType getAnyTypeForObject(CLRObject clrObject)                     | 共通言語ランタイム (CLR) オブジェクトを X++ anytype データ型の値に変換します。                                                 |
| ::public static CLRObject getLastException()                                         | 最新の CLR 例外を取得します。                                                                                                 |
| ::public static CLRObject getObjectForAnyType(AnyType anyType)                       | X++ anytype データ型の値を CLRObject データ型の値に変換します。                                                     |
| ::public static CLRObject getType(str clrTypeName)                                   |                                                                                                                                          |
| ::public static boolean isNull(CLRObject clrObject)                                  | 指定された CLRObject インスタンスが nullNothingnullptrunita null 参照 (Visual Basic では Nothing) にセットされているかどうかを確認します。            |
| ::public static CLRObject Null(str clrTypeName)                                      | nullNothingnullptrunita null 参照 (Visual Basic では Nothing) の値を持つ CLR データ型を返します。                            |
| ::public static CLRObject parseClrEnum(str clrEnumTypeName, str enumValues)          | 1 つ以上の列挙定数の名前または数値の文字列で表したものを、等価の CLRObject インスタンスに変換します。 |
| ::public static CLRObject staticInvoke(str className, str methodName, VarArg params) | CLR データ型の静的メソッドを呼び出します。                                                                                                |
| ::public static void loadAssembly(str clrAssemblyName)                               |                                                                                                                                          |
| public void new()                                                                    | CLRInterop クラスの新しいインスタンスを初期化します。                                                                                      |

## <a name="method-getanytypeforobject"></a>メソッド getAnyTypeForObject

共通言語ランタイム (CLR) オブジェクトを X++ anytype データ型の値に変換します。

```xpp
public static AnyType getAnyTypeForObject(CLRObject clrObject)
```

### <a name="parameters---getanytypeforobject"></a>パラメーター - getAnyTypeForObject

clrObject  
X++ データ型に変換する CLR オブジェクト。

### <a name="return-value---getanytypeforobject"></a>戻り値 - getAnyTypeForObject

\_オブジェクトの引数値を持つ X++ anytype データ型です。

### <a name="remarks---getanytypeforobject"></a>備考 - getAnyTypeForObject

攻撃者が getAnyTypeForObject メソッドへの入力を制御できる場合、セキュリティ上のリスクが存在します。 したがって、このメソッドは、コード アクセス セキュリティで実行されます。 サーバー上でこのメソッドを呼び出すには、アクセス許可が必要です。 ユーザーがこのメソッドを呼び出すコントロールで、SysDevelopment へのセキュリティ キーを設定して開発権限を持っていることを確認します。 引数 X++ のデータ型に変換することができない場合、Exception::ClrError タイプの例外がスローされます。

### <a name="examples---getanytypeforobject"></a>例 - getAnyTypeForObject

次の例では、CLR 文字列の値を X++ str データ型に設定します。

```xpp
{ 
    CLRObject clrObj; 
    InteropPermission perm; 
    System.String   clrStr = "Calculate total"; 
    str             s; 
```

```xpp
    perm = new InteropPermission(InteropKind::ClrInterop); 
    if (perm == null) 
    { 
        return; 
    } 
    perm.assert(); 
```

```xpp
    s = ClrInterop::getAnyTypeForObject(clrStr); 
    CodeAccessPermission::revertAssert(); 
}
```

## <a name="method-getlastexception"></a>メソッド getLastException

最新の CLR 例外を取得します。

```xpp
public static CLRObject getLastException()
```

### <a name="return-value---getlastexception"></a>戻り値 - getLastException

Exception::ClrError 型の最新の例外。それ以外の場合は、nullNothingnullptrunita null 参照 (Visual Basic では Nothing)。

### <a name="remarks---getlastexception"></a>備考 - getLastException

攻撃者が getLastException メソッドへの入力を制御できる場合、セキュリティ上のリスクが存在します。 したがって、このメソッドは、コード アクセス セキュリティで実行されます。 サーバー上でこのメソッドを呼び出すには、アクセス許可が必要です。 ユーザーがこのメソッドを呼び出すコントロールで、SysDevelopment へのセキュリティ キーを設定して開発権限を持っていることを確認します。

### <a name="examples---getlastexception"></a>例 - getLastException

次の例では、無効な形式の日付を渡します。 スローされた CLR 例外は、X++ 例外に変換された後、情報ログに出力されます。 入れ子になった例外は情報ログにも出力されます。

```xpp
static void Job2(Args _args) 
{ 
    CLRObject clrObj; 
    InteropPermission perm; 
```

```xpp
    try 
    { 
        System.DateTime::Parse( "-1/-1/-1"); 
    } 
    catch( Exception::CLRError ) 
    { 
        perm = new InteropPermission(InteropKind::ClrInterop); 
        if (perm == null) 
        { 
            return; 
        } 
        perm.assert(); 
```

```xpp
        e = ClrInterop::getLastException(); 
```

```xpp
        CodeAccessPermission::revertAssert(); 
```

```xpp
        while( e ) 
        { 
            info( e.get_Message() ); 
            e = e.get_InnerException(); 
        } 
    } 
```

```xpp
}
```

## <a name="method-getobjectforanytype"></a>メソッド getObjectForAnyType

X++ anytype データ型の値を CLRObject データ型の値に変換します。

```xpp
public static CLRObject getObjectForAnyType(AnyType anyType)
```

### <a name="parameters---getobjectforanytype"></a>パラメーター - getObjectForAnyType

anyType  
CLRObject データ型の値に変換する X++ 値。

### <a name="return-value---getobjectforanytype"></a>戻り値 - getObjectForAnyType

値 \_anytype 引数を持つ CLR オブジェクト。

### <a name="remarks---getobjectforanytype"></a>備考 - getObjectForAnyType

攻撃者が getObjectForAnyType メソッドへの入力を制御できる場合、セキュリティ上のリスクが存在します。 したがって、このメソッドは、コード アクセス セキュリティで実行されます。 サーバー上でこのメソッドを呼び出すには、アクセス許可が必要です。 ユーザーがこのメソッドを呼び出すコントロールで、SysDevelopment へのセキュリティ キーを設定して開発権限を持っていることを確認します。 引数を CLRObject 型に変換することができない場合、Exception::CLRError 型の例外がスローされます。

### <a name="examples---getobjectforanytype"></a>例 - getObjectForAnyType

次の例では、文字列値を CLR 文字列オブジェクトに変換します。

```xpp
static void Job3(Args _args) 
{ 
    CLRObject clrObj; 
    InteropPermission perm; 
    System.String s; 
```

```xpp
    perm = new InteropPermission(InteropKind::ClrInterop); 
    if (perm == null) 
    { 
        return; 
    } 
    perm.assert(); 
```

```xpp
    s = CLRInterop::getObjectForAnyType("Calculate total"); 
```

```xpp
    CodeAccessPermission::revertAssert(); 
}
```

## <a name="method-gettype"></a>メソッド getType

```xpp
public static CLRObject getType(str clrTypeName)
```

### <a name="parameters---gettype"></a>パラメーター - getType

clrTypeName  

### <a name="return-value---gettype"></a>戻り値 - getType

## <a name="method-isnull"></a>メソッド isNull

指定された CLRObject インスタンスが nullNothingnullptrunita null 参照 (Visual Basic では Nothing) にセットされているかどうかを確認します。

```xpp
public static boolean isNull(CLRObject clrObject)
```

### <a name="parameters---isnull"></a>パラメーター - isNull

clrObject  
評価する CLRObject インスタンスです。

### <a name="return-value---isnull"></a>戻り値 - isNull

指定された CLRObject インスタンスが nullNothingnullptrunita null 参照 (Visual Basic では Nothing) にセットされた場合または初期化されていない場合は true。

### <a name="remarks---isnull"></a>備考 - isNull

CLR データ型が nullNothingnullptrunita null 参照 (Visual Basic では Nothing) であるかどうかを評価する条件ステートメントでは、X++ nullNothingnullptrunita null 参照 (Visual Basic では Nothing) の代わりに isNull メソッドを使用する必要があります。

### <a name="examples---isnull"></a>例 - isNull

次の例では、CLR 文字列データ型を nullNothingnullptrunita null 参照 (Visual Basic では Nothing) に設定し、タイプ値を CLR オブジェクトに割り当てます。 isNull メソッドを呼び出し、情報ログに結果を出力します。

```xpp
static void Job5(Args _args) 
{ 
    System.String nullStr; 
```

```xpp
    nullStr = CLRInterop::Null("System.String"); 
```

```xpp
    print CLRInterop::isNull(nullStr); 
}
```

## <a name="method-null"></a>メソッド Null

nullNothingnullptrunita null 参照 (Visual Basic では Nothing) の値を持つ CLR データ型を返します。

```xpp
public static CLRObject Null(str clrTypeName)
```

### <a name="parameters---null"></a>パラメーター - Null

clrTypeName  
nullNothingnullptrunita null参照 (Visual Basic では Nothing) に設定する必要がある CLR データ型。

### <a name="return-value---null"></a>戻り値 - Null

指定された CLR データ型の CLRObject インスタンス。

### <a name="remarks---null"></a>備考 - Null

X++ で CLR データ型を NullNothingnullptrunita null 参照 (Visual Basic では Nothing) に直接設定する場合は、カーネル参照を nullNothingnullptrunita null 参照 (Visual Basic では Nothing) にのみ設定します。 これにより、CLR データ型として型を使用することができなくなります。 CLRInterop:null("yourType") に CLR データ型を割り当てると、静的メソッド呼び出しのパラメーターとして、実行時にタイプを解析できます。

### <a name="examples---null"></a>例 - Null

次の例では、CLR 文字列型を nullNothingnullptrunita null 参照 (Visual Basic では Nothing) に設定し、タイプ値を CLR オブジェクトに割り当てます。

```xpp
static void Job5(Args _args) 
{ 
    System.String nullStr; 
```

```xpp
    nullStr = CLRInterop::Null("System.String"); 
```

```xpp
    print CLRInterop::isInitialized(nullStr); 
    print CLRInterop::isNull(nullStr); 
}
```

## <a name="method-parseclrenum"></a>メソッド parseClrEnum

1 つ以上の列挙定数の名前または数値の文字列で表したものを、等価の CLRObject インスタンスに変換します。

```xpp
public static CLRObject parseClrEnum(str clrEnumTypeName, str enumValues)
```

### <a name="parameters---parseclrenum"></a>パラメーター - parseClrEnum

clrEnumTypeName  
変換する名前または値を含む文字列。

<!-- -->

enumValues  
変換する名前または値を含む文字列。

### <a name="return-value---parseclrenum"></a>戻り値 - parseClrEnum

指定した CLR 列挙値を含む CLRObject インスタンスです。

### <a name="remarks---parseclrenum"></a>備考 - parseClrEnum

\_enumValues パラメーターには、値、名前付き定数、またはコンマ (,) で区切られた名前付き定数の一覧が含まれています。 1 つ以上の空白スペースは、\_enumValues の各値、名前、またはコンマの前か後に置くことができます。 \_enumValues が一覧の場合、戻り値は、ビット単位の OR 演算と組み合わされた指定された名前の値です。

### <a name="examples---parseclrenum"></a>例 - parseClrEnum

次の例では、列挙子の値を月曜日の文字列値に変換し、Infolog の値を出力します。

```xpp
static void Job6(Args _args) 
{ 
    System.DayOfWeek    dayOfWeek; 
    System.Type         dayOfWeekType; 
```

```xpp
    dayOfWeek = CLRInterop::parseClrEnum( "System.DayOfWeek", "Monday"); 
```

```xpp
    dayOfWeekType = dayOfWeek.GetType(); 
```

```xpp
    info( dayOfWeek.ToString() ); 
}
```

## <a name="method-staticinvoke"></a>メソッド staticInvoke

CLR データ型の静的メソッドを呼び出します。

```xpp
public static CLRObject staticInvoke(str className, str methodName, VarArg params)
```

### <a name="parameters---staticinvoke"></a>パラメーター - staticInvoke

className  
\_methodName パラメーターで指定されるメソッドの引数 (引数がある場合)。

<!-- -->

methodName  
\_methodName パラメーターで指定されるメソッドの引数 (引数がある場合)。

<!-- -->

params  
\_methodName パラメーターで指定されるメソッドの引数 (引数がある場合)。

### <a name="return-value---staticinvoke"></a>戻り値 - staticInvoke

静的 CLR メソッドによって返される値を含む CLRObject。それ以外の場合、nullNothingnullptrunita null 参照 (Visual Basic では Nothing)。

### <a name="remarks---staticinvoke"></a>備考 - staticInvoke

攻撃者が staticInvoke メソッドへの入力を制御できる場合、セキュリティ上のリスクが存在します。 したがって、このメソッドは、コード アクセス セキュリティで実行されます。 サーバー上でこのメソッドを呼び出すには、アクセス許可が必要です。 ユーザーがこのメソッドを呼び出すコントロールで、SysDevelopment へのセキュリティ キーを設定して開発権限を持っていることを確認します。 get\_Now メソッドを呼び出すときにエラーが発生した場合は、Exception::ClrError 例外がスローされます。

### <a name="examples---staticinvoke"></a>例 - staticInvoke

次の例では、System.DateTime CLR クラスの get\_Now メソッドを呼び出し、結果を Infolog に出力します。

```xpp
static void Job7(Args _args) 
{ 
    CLRObject clrObj; 
    InteropPermission perm; 
    System.DateTime dateTime; 
```

```xpp
    perm = new InteropPermission(InteropKind::ClrInterop); 
    if (perm == null) 
    { 
        return; 
    } 
    perm.assert(); 
```

```xpp
    dateTime = CLRInterop::staticInvoke( 
                   "System.DateTime", 
                   "get_Now" ); 
    info(dateTime.ToString()); 
    CodeAccessPermission::revertAssert(); 
```

```xpp
    pause; 
```

```xpp
    // This is the same code using CLR syntax. 
    // dateTime = System.DateTime::get_Now(); 
    // info(dateTime.ToString()); 
}
```

## <a name="method-loadassembly"></a>メソッド loadAssembly

```xpp
public static void loadAssembly(str clrAssemblyName)
```

### <a name="parameters---loadassembly"></a>パラメーター - loadAssembly

clrAssemblyName  

## <a name="method-new"></a>メソッド new

CLRInterop クラスの新しいインスタンスを初期化します。

```xpp
public void new()
```

### <a name="remarks---new"></a>備考 - new

CLRInterop クラスのすべてのメンバーは静的です。 このクラスをインスタンス化する必要はありません。 攻撃者が新しいメソッドへの入力を制御できる場合、セキュリティ上のリスクが存在します。 したがって、このメソッドは、コード アクセス セキュリティで実行されます。 サーバー上でこのメソッドを呼び出すには、InteropPermission クラスからのアクセス許可が必要です。

