---
title: DictClass クラス
description: このトピックでは、DictClass クラスについて説明します。
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
ms.openlocfilehash: 6cb92115e246d36b9a641a9941e11d944b3988f9
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502729"
---
# <a name="class-dictclass"></a>クラス DictClass

[!include [banner](../../includes/banner.md)]

```xpp
class DictClass extends Object
```

DictClass クラスは、クラスに関する情報を提供します。

## <a name="remarks"></a>備考

## <a name="examples"></a>例

## <a name="methods"></a>メソッド

| 方法                                                            | 説明                                                                                                                                   |
|-------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| public AnyType callObject(str methodName, Object Called, VarArg ) | オブジェクトのメソッドを呼び出します。                                                                                                                  |
| public AnyType callStatic(str methodName, VarArg )                | 静的メソッドを呼び出します。                                                                                                                        |
| public ClassId extend()                                           | 指定されたクラスが拡張されるクラスの ID を提供します。                                                                                 |
| public List extendedBy(\[boolean allLevels\])                     | 指定されたクラスを拡張するクラスのリスト オブジェクトを提供します。                                                                         |
| public Array getAllAttributes()                                   | クラスの属性の完全なセットを取得します。                                                                                           |
| public Object getAttribute(str attribute)                         | クラス ヘッダー メタデータから最初に一致する属性を取得し、その属性を表すオブジェクト クラスのインスタンスを作成し、返します。 |
| public Array getAttributes(str attribute)                         |                                                                                                                                               |
| public ClassId id()                                               | 指定されたクラスの ID を提供します。                                                                                                        |
| public ClassId implements(int no)                                 | クラスが実装する指定されたインターフェイスの ID を示します。                                                                            |
| public int implementsCnt()                                        | クラスが実装するインターフェイスの数を示します。                                                                                   |
| public boolean isAbstract()                                       | クラスが抽象であるかどうかを示します。                                                                                                        |
| public boolean isFinal()                                          | クラスが最終であるかどうかを示します。                                                                                                           |
| public boolean isInterface()                                      | オブジェクトがインターフェイスであるかどうかを示します。                                                                                                  |
| public boolean isKernel()                                         | クラスがカーネル クラスであるかどうかを示します。                                                                                                  |
| public boolean isRunable()                                        | クラスを実行できるかどうかを示します。                                                                                                         |
| public Object makeObject(VarArg )                                 | オブジェクトを作成します。                                                                                                                            |
| public str name()                                                 | クラスの名前を提供します。                                                                                                                 |
| public str objectMethod(int methodNumber)                         | クラスの指定されたインスタンス メソッドの名前を提供します。                                                                                  |
| public int objectMethodCnt()                                      | クラスのインスタンス メソッドの数を示します。                                                                                          |
| public DictMethod objectMethodObject(int methodNumber)            | DictMethod オブジェクトを返すことで、クラス内の指定されたインスタンス メソッドに関する情報を提供します。                                           |
| public ClassRunMode RunMode()                                     | クラスが実行される場所を指定します。                                                                                                          |
| public str staticMethod(int methodNumber)                         | クラスの指定された静的メソッドの名前を提供します。                                                                                    |
| public int staticMethodCnt()                                      | クラスの静的メソッドの数を示します。                                                                                            |
| public DictMethod staticMethodObject(int methodNumber)            | DictMethod オブジェクトを返すことで、クラス内の指定された静的メソッドに関する情報を提供します。                                             |
| ::public static Array getAttributedClasses(str attribute)         |                                                                                                                                               |
| ::public static Object createObject(str className, VarArg )       |                                                                                                                                               |
| public void new(ClassId classId)                                  | Object クラスの新しいインスタンスを初期化します。                                                                                               |

## <a name="method-callobject"></a>メソッド callObject

オブジェクトのメソッドを呼び出します。

```xpp
public AnyType callObject(str methodName, Object Called, VarArg )
```

### <a name="parameters---callobject"></a>パラメータ - callObject

methodName  

<!-- -->

呼び出された  

<!-- -->


### <a name="return-value---callobject"></a>戻り値 - callObject

指定されたメソッドによって返される anytype データ型値です。

### <a name="remarks---callobject"></a>備考 - callObject

callObject メソッドに渡すメソッドを含むクラスを使用して、DictClass オブジェクトのインスタンスを作成する必要があります。 攻撃者が callObject メソッドへの入力を制御できる場合、セキュリティ上のリスクが存在します。 したがって、このメソッドは、コード アクセス セキュリティで実行されます。 サーバー上でこのメソッドを呼び出すには、InteropPermission クラスからのアクセス許可が必要です。 ユーザーがこのメソッドを呼び出すコントロールで、SysDevelopment へのセキュリティ キーを設定して開発権を持っていることを確認します。

### <a name="examples---callobject"></a>例 - callObject

この例では、このクラスのグローバル インスタンスの名前が infolog である Info クラスの toString インスタンス メソッドを呼び出し、呼び出しから返された値を出力します。

```xpp
static void Job_Example_DictClass_CallObject(Args _args) 
{ 
    DictClass dictClass; 
    anytype   retVal; 
    str      resultOutput; 
    ExecutePermission perm; 
    perm = new ExecutePermission(); 
    // Grants permission to execute the DictClass.callObject method. 
    // DictClass.callObject runs under code access security. 
    perm.assert(); 
    dictClass = new DictClass(classidget(infolog)); 
    if (dictClass != null) 
    { 
        retVal       = dictClass.callObject("toString", infolog); 
        resultOutput = strfmt("Return value is %1", retVal); 
        print resultOutput; 
        pause; 
    } 
    // Closes the code access permission scope. 
    CodeAccessPermission::revertAssert(); 
}
```

## <a name="method-callstatic"></a>メソッド callStatic

静的メソッドを呼び出します。

```xpp
public AnyType callStatic(str methodName, VarArg )
```

### <a name="parameters---callstatic"></a>パラメーター - callStatic

methodName  

<!-- -->


### <a name="return-value---callstatic"></a>戻り値 - callStatic

指定されたメソッドによって返される anytype データ型値です。

### <a name="remarks---callstatic"></a>備考 - callStatic

callStatic メソッドに渡されるメソッドを含むクラスを使用して、DictClass クラスのオブジェクトのインスタンスを作成する必要があります。 攻撃者が callStatic メソッドへの入力を制御できる場合、セキュリティ上のリスクが存在します。 したがって、このメソッドは、コード アクセス セキュリティで実行されます。 サーバー上でこのメソッドを呼び出すには、ExecutePermission クラスからのアクセス許可が必要です。 ユーザーがこのメソッドを呼び出すコントロールで、SysDevelopment へのセキュリティ キーを設定して開発権を持っていることを確認します。

### <a name="examples---callstatic"></a>例 - callStatic

この例では、Session クラスの AOSClientMode メソッドを呼び出し、呼び出しから返された値を出力します。

```xpp
static void Job_Example_DictClass_CallStatic(Args _args) 
{ 
    DictClass dictClass; 
    anytype   retVal; 
    str       resultOutput; 
    ExecutePermission perm; 
    perm = new ExecutePermission(); 
    // Grants permission to execute the DictClass.callStatic method. 
    // DictClass.callStatic runs under code access security. 
    perm.assert(); 
    dictClass = new DictClass(classnum(Session)); 
    if (dictClass != null) 
    { 
        retVal       = dictClass.callStatic("AOSClientMode"); 
        resultOutput = strfmt( 
            "Return value of AOSClientMode is %1",  
            retVal); 
        print resultOutput; 
        pause; 
    } 
    // Closes the code access permission scope. 
    CodeAccessPermission::revertAssert(); 
}
```

## <a name="method-extend"></a>メソッド extend

指定されたクラスが拡張されるクラスの ID を提供します。

```xpp
public ClassId extend()
```

### <a name="return-value---extend"></a>戻り値 - extend

クラス ID を示す classID システムデータ型の値、クラスが別のクラスを拡張していない場合は 0。

## <a name="method-extendedby"></a>メソッド extendedBy

指定されたクラスを拡張するクラスのリスト オブジェクトを提供します。

```xpp
public List extendedBy([boolean allLevels])
```

### <a name="parameters---extendedby"></a>パラメーター - extendedBy

allLevels  

### <a name="return-value---extendedby"></a>戻り値 - extendedBy

クラスを拡張するクラスのリスト オブジェクト。

## <a name="method-getallattributes"></a>メソッド getAllAttributes

クラスの属性の完全なセットを取得します。

```xpp
public Array getAllAttributes()
```

### <a name="return-value---getallattributes"></a>戻り値 - getAllAttributes

クラスの SysAttribute オブジェクトの配列。

## <a name="method-getattribute"></a>メソッド getAttribute

クラス ヘッダー メタデータから最初に一致する属性を取得し、その属性を表すオブジェクト クラスのインスタンスを作成し、返します。

```xpp
public Object getAttribute(str attribute)
```

### <a name="parameters---getattribute"></a>パラメーター - getAttribute

属性  
検索の対象である属性。

### <a name="return-value---getattribute"></a>戻り値 - getAttribute

オブジェクト クラスのインスタンスとしての属性。

## <a name="method-getattributes"></a>メソッド getAttributes

```xpp
public Array getAttributes(str attribute)
```

### <a name="parameters---getattributes"></a>パラメーター - getAttributes

属性  

### <a name="return-value---getattributes"></a>戻り値 - getAttributes

## <a name="method-id"></a>メソッド id

指定されたクラスの ID を提供します。

```xpp
public ClassId id()
```

### <a name="return-value---id"></a>戻り値 - id

クラス ID を示す classId システムデータ型の値。

## <a name="method-implements"></a>メソッド implements

クラスが実装する指定されたインターフェイスの ID を示します。

```xpp
public ClassId implements(int no)
```

### <a name="parameters---implements"></a>パラメーター - implements

no  
クラス宣言内のインターフェイスの順序に基づいて、インターフェイスを指定する整数データ型。

### <a name="return-value---implements"></a>戻り値 - implements

クラス ID を示す classID システムデータ型の値。

## <a name="method-implementscnt"></a>メソッド implementsCnt

クラスが実装するインターフェイスの数を示します。

```xpp
public int implementsCnt()
```

### <a name="return-value---implementscnt"></a>戻り値 - implementsCnt

クラスが実装するインターフェイスの数の整数データ型値。

## <a name="method-isabstract"></a>メソッド isAbstract

クラスが抽象であるかどうかを示します。

```xpp
public boolean isAbstract()
```

### <a name="return-value---isabstract"></a>戻り値 - isAbstract

クラスが抽象である場合は true。それ以外の場合は、false。

## <a name="method-isfinal"></a>メソッド isFinal

クラスが最終であるかどうかを示します。

```xpp
public boolean isFinal()
```

### <a name="return-value---isfinal"></a>戻り値 - isFinal

クラスが最終である場合は true。それ以外の場合は、false。

## <a name="method-isinterface"></a>メソッド isInterface

オブジェクトがインターフェイスであるかどうかを示します。

```xpp
public boolean isInterface()
```

### <a name="return-value---isinterface"></a>戻り値 - isInterface

オブジェクトがインターフェイスである場合は true。それ以外の場合は、false。

## <a name="method-iskernel"></a>メソッド isKernel

クラスがカーネル クラスであるかどうかを示します。

```xpp
public boolean isKernel()
```

### <a name="return-value---iskernel"></a>戻り値 - isKernel

クラスがカーネル クラスの場合は true。それ以外の場合は、false。

## <a name="method-isrunable"></a>メソッド isRunable

クラスを実行できるかどうかを示します。

```xpp
public boolean isRunable()
```

### <a name="return-value---isrunable"></a>戻り値 - isRunable

クラスを実行することができる場合は true。それ以外の場合は、false。

## <a name="method-makeobject"></a>メソッド makeObject

オブジェクトを作成します。

```xpp
public Object makeObject(VarArg )
```

### <a name="parameters---makeobject"></a>パラメーター - makeObject


### <a name="return-value---makeobject"></a>戻り値 - makeObject

オブジェクト クラスのインスタンス。

### <a name="remarks---makeobject"></a>備考 - makeObject

オブジェクト クラスのインスタンスを DictClass::callObject メソッドに渡すことができます。

## <a name="method-name"></a>メソッド名

クラスの名前を提供します。

```xpp
public str name()
```

### <a name="return-value---name"></a>戻り値 - name

クラス名の文字列データ型の値。

## <a name="method-objectmethod"></a>メソッド objectMethod

クラスの指定されたインスタンス メソッドの名前を提供します。

```xpp
public str objectMethod(int methodNumber)
```

### <a name="parameters---objectmethod"></a>パラメーター - objectMethod

methodNumber  
メソッドの順序に基づいて、クラス内のメソッドを指定する整数データ型。

### <a name="return-value---objectmethod"></a>戻り値 - objectMethod

メソッド名の文字列データ型の値。

### <a name="remarks---objectmethod"></a>備考 - objectMethod

\_methodNumber パラメーターは 1 から始まります。

## <a name="method-objectmethodcnt"></a>メソッド objectMethodCnt

クラスのインスタンス メソッドの数を示します。

```xpp
public int objectMethodCnt()
```

### <a name="return-value---objectmethodcnt"></a>戻り値 - objectMethodCnt

クラス内のインスタンス メソッドの数を示す整数値。

## <a name="method-objectmethodobject"></a>メソッド objectMethodObject

DictMethod オブジェクトを返すことで、クラス内の指定されたインスタンス メソッドに関する情報を提供します。

```xpp
public DictMethod objectMethodObject(int methodNumber)
```

### <a name="parameters---objectmethodobject"></a>パラメーター - objectMethodObject

methodNumber  
メソッドの順序に基づいて、クラス内のメソッドを指定する整数データ型。 番号付けは 1 から開始します。

### <a name="return-value---objectmethodobject"></a>戻り値 - objectMethodObject

クラス内の指定されたメソッドに関する情報を含む DictMethod オブジェクト。

### <a name="remarks---objectmethodobject"></a>備考 - objectMethodObject

\_methodNumber パラメーターは 1 から始まります。

## <a name="method-runmode"></a>メソッド RunMode

クラスが実行される場所を指定します。

```xpp
public ClassRunMode RunMode()
```

### <a name="return-value---runmode"></a>戻り値 - RunMode

クラスが実行される場所を示す ClassRunMode システム列挙値。

### <a name="remarks---runmode"></a>備考 - RunMode

可能な戻り値は次のとおりです。

-   呼び出された値。
-   Client 値。
-   ClientorServer 値。
-   サーバーの値。

## <a name="method-staticmethod"></a>メソッド staticMethod

クラスの指定された静的メソッドの名前を提供します。

```xpp
public str staticMethod(int methodNumber)
```

### <a name="parameters---staticmethod"></a>パラメーター - staticMethod

methodNumber  
メソッドの順序に基づいて、クラス内のメソッドを指定する整数データ型。

### <a name="return-value---staticmethod"></a>戻り値 - staticMethod

メソッド名の文字列データ型の値。

### <a name="remarks---staticmethod"></a>備考 - staticMethod

\_methodNumber パラメーターは 1 から始まります。

## <a name="method-staticmethodcnt"></a>メソッド staticMethodCnt

クラスの静的メソッドの数を示します。

```xpp
public int staticMethodCnt()
```

### <a name="return-value---staticmethodcnt"></a>戻り値 - staticMethodCnt

クラスの静的メソッドの数を示す整数。

## <a name="method-staticmethodobject"></a>メソッド staticMethodObject

DictMethod オブジェクトを返すことで、クラス内の指定された静的メソッドに関する情報を提供します。

```xpp
public DictMethod staticMethodObject(int methodNumber)
```

### <a name="parameters---staticmethodobject"></a>パラメーター - staticMethodObject

methodNumber  
メソッドの順序に基づいて、クラス内のメソッドを指定する整数データ型。

### <a name="return-value---staticmethodobject"></a>戻り値 - staticMethodObject

クラス内の指定されたメソッドに関する情報を含む DictMethod オブジェクト。

### <a name="remarks---staticmethodobject"></a>備考 - staticMethodObject

\_methodNumber パラメーターは 1 から始まります。

## <a name="method-getattributedclasses"></a>メソッド getAttributedClasses

```xpp
public static Array getAttributedClasses(str attribute)
```

### <a name="parameters---getattributedclasses"></a>パラメーター - getAttributedClasses

属性  

### <a name="return-value---getattributedclasses"></a>戻り値 - getAttributedClasses

## <a name="method-createobject"></a>メソッド createObject

```xpp
public static Object createObject(str className, VarArg )
```

### <a name="parameters---createobject"></a>パラメーター - createObject

className  

<!-- -->


### <a name="return-value---createobject"></a>戻り値 - createObject

## <a name="method-new"></a>メソッド new

Object クラスの新しいインスタンスを初期化します。

```xpp
public void new(ClassId classId)
```

### <a name="parameters---new"></a>パラメーター - new

classId  
クラスのシステム ID を示す classId システムデータ型の値。

### <a name="remarks---new"></a>備考 - new

クラス ID は符号なし整数なので、常に 0 から 65535 の範囲です。 無効なクラス ID が渡された場合は、このメソッドは失敗しません。 ClassNum 組み込み関数を使用して、クラス ID の代わりにクラス名をメソッドに渡すことができます。 詳細については、「組み込み関数」を参照してください。

