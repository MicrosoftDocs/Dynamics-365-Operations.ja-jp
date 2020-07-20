---
title: DictMethod クラス
description: このトピックでは､DictMethod クラスについて説明します。
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
ms.openlocfilehash: 51fee7fa2fd68550cf37e60d63f722954ad04a5d
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502984"
---
# <a name="class-dictmethod"></a>クラス DictMethod

[!include [banner](../../includes/banner.md)]

```xpp
class DictMethod extends MethodInfo
```

## <a name="remarks"></a>備考

## <a name="examples"></a>例

## <a name="methods"></a>メソッド

| 方法                                                      | 説明                                                                                                                                                  |
|-------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| public AccessSpecifier accessSpecifier()                    | メソッドがパブリック、保護、またはプライベートかどうかを指定します。                                                                                               |
| public str clrParameterType(int variableNumber)             |                                                                                                                                                              |
| public str clrReturnType()                                  |                                                                                                                                                              |
| public str clrVarType(int variableNumber)                   |                                                                                                                                                              |
| public boolean compiledOk()                                 | メソッドが正常にコンパイルしたかどうかを示します。                                                                                                          |
| public TableId displayId()                                  |                                                                                                                                                              |
| public DisplayFunctionType displayType()                    | メソッドの表示機能のタイプを示します。                                                                                                          |
| public boolean hasImplementation()                          | 実際のメソッドの実装がクラスにあるのか、基本クラスから派生したのかを判断します。                                                          |
| public boolean isAbstract()                                 | メソッドが抽象かどうかを示します。                                                                                                                    |
| public boolean isDelegate()                                 | メソッドがデリゲートかどうかを示します。                                                                                                                  |
| public boolean isStatic()                                   | メソッドが静的かどうかを示します。                                                                                                                      |
| public str name()                                           | メソッドの名前を取得します。                                                                                                                                 |
| public int parameterCnt()                                   | メソッドのパラメーター数を取得します。                                                                                                                |
| public int parameterId(int variableNumber)                  | 指定されたパラメータの ID を取得します。                                                                                                                      |
| public str parameterName(int variableNumber)                | 指定されたパラメータの名前を取得します。                                                                                                                    |
| public boolean parameterOptional(int variableNumber)        | メソッドの指定されたパラメーターが省略可能かどうかを示します。                                                                                         |
| public Types parameterType(int variableNumber)              |                                                                                                                                                              |
| public int parentId()                                       | メソッドを所有する親の ID を取得します。                                                                                                              |
| public str propertyHelp()                                   | メソッドに関連付けられているプロパティのヘルプ文字列を取得します。                                                                                    |
| public NoYes propertyMethod()                               | メソッドがプロパティ メソッドかどうかを示します。                                                                                                           |
| public int returnId()                                       | 値を返すメソッドについて、拡張データ型やクラスなどの特定の戻り値のデータ型の ID を指定します。                                  |
| public Types returnType()                                   | メソッドの戻り値の型を指定します。                                                                                                                              |
| public ClassRunMode runMode()                               | メソッドが実行される場所を指定します。                                                                                                                             |
| public int varCnt()                                         | メソッドの変数の数を取得します。                                                                                                                 |
| public str varName(int variableNumber)                      | 指定された変数の名前を取得します。                                                                                                                     |
| public void setMethod(MemberFunction method)                | MemberFunction クラスのインスタンスを使用して、アプリケーション オブジェクト ツリー (AOT) 内のノードのアプリケーション オブジェクト タイプを指定します。 |
| public void new(UtilElementType utilType, int id, str name) | Object クラスの新しいインスタンスを初期化します。                                                                                                              |

## <a name="method-accessspecifier"></a>メソッド accessSpecifier

メソッドがパブリック、保護、またはプライベートかどうかを指定します。

```xpp
public AccessSpecifier accessSpecifier()
```

### <a name="return-value---accessspecifier"></a>戻り値 - accessSpecifier

メソッドがパブリック、保護、またはプライベートのいずれかを指定する AccessSpecifier 列挙値です。

## <a name="method-clrparametertype"></a>メソッド clrParameterType

```xpp
public str clrParameterType(int variableNumber)
```

### <a name="parameters---clrparametertype"></a>パラメーター - clrParameterType

variableNumber  

### <a name="return-value---clrparametertype"></a>戻り値 - clrParameterType

## <a name="method-clrreturntype"></a>メソッド clrReturnType

```xpp
public str clrReturnType()
```

### <a name="return-value---clrreturntype"></a>戻り値 - clrReturnType

## <a name="method-clrvartype"></a>メソッド clrVarType

```xpp
public str clrVarType(int variableNumber)
```

### <a name="parameters---clrvartype"></a>パラメーター - clrVarType

variableNumber  

### <a name="return-value---clrvartype"></a>戻り値 - clrVarType

## <a name="method-compiledok"></a>メソッド compiledOk

メソッドが正常にコンパイルしたかどうかを示します。

```xpp
public boolean compiledOk()
```

### <a name="return-value---compiledok"></a>戻り値 - compiledOk

メソッドが正常にコンパイルされる場合は true。それ以外の場合は、false。

## <a name="method-displayid"></a>メソッド displayId

```xpp
public TableId displayId()
```

### <a name="return-value---displayid"></a>戻り値 - displayId

## <a name="method-displaytype"></a>メソッド displayType

メソッドの表示機能のタイプを示します。

```xpp
public DisplayFunctionType displayType()
```

### <a name="return-value---displaytype"></a>戻り値 - displayType

メソッドの表示機能のタイプを示す DisplayFunctionType 列挙値。

### <a name="remarks---displaytype"></a>備考 - displayType

次のテーブルに、displayType メソッドによって返される可能な値を示します。

|           |                                             |
|-----------|---------------------------------------------|
| 取得       | このメソッドは表示メソッドです。             |
| None      | このメソッドは、表示メソッドまたは編集メソッドではありません。 |
| RecordGet | このメソッドは、レコードを取得します。              |
| RecordSet | このメソッドは、レコードを設定します。                   |
| セット       | このメソッドは、編集メソッドです。               |

## <a name="method-hasimplementation"></a>メソッド hasImplementation

実際のメソッドの実装がクラスにあるのか、基本クラスから派生したのかを判断します。

```xpp
public boolean hasImplementation()
```

### <a name="return-value---hasimplementation"></a>戻り値 - hasImplementation

メソッドがクラス上に実装される場合は true。それ以外の場合は、false。

## <a name="method-isabstract"></a>メソッド isAbstract

メソッドが抽象かどうかを示します。

```xpp
public boolean isAbstract()
```

### <a name="return-value---isabstract"></a>戻り値 - isAbstract

メソッドが抽象である場合は true。それ以外の場合は、false。

## <a name="method-isdelegate"></a>メソッド isDelegate

メソッドがデリゲートかどうかを示します。

```xpp
public boolean isDelegate()
```

### <a name="return-value---isdelegate"></a>戻り値 - isDelegate

メソッドがデリゲートされる場合は true。それ以外の場合は、false。

## <a name="method-isstatic"></a>メソッド isStatic

メソッドが静的かどうかを示します。

```xpp
public boolean isStatic()
```

### <a name="return-value---isstatic"></a>戻り値 - isStatic

メソッドが静的である場合は true。それ以外の場合は、false。

## <a name="method-name"></a>メソッド名

メソッドの名前を取得します。

```xpp
public str name()
```

### <a name="return-value---name"></a>戻り値 - name

メソッドの名前。

## <a name="method-parametercnt"></a>メソッド parameterCnt

メソッドのパラメーター数を取得します。

```xpp
public int parameterCnt()
```

### <a name="return-value---parametercnt"></a>戻り値 - parameterCnt

メソッドのパラメーター数を取得。

## <a name="method-parameterid"></a>メソッド parameterId

指定されたパラメータの ID を取得します。

```xpp
public int parameterId(int variableNumber)
```

### <a name="parameters---parameterid"></a>パラメーター - parameterId

variableNumber  
メソッドのパラメーター リストへの 1 から始まるインデックス。

### <a name="return-value---parameterid"></a>戻り値 - parameterId

指定されたパラメーターの ID。

## <a name="method-parametername"></a>メソッド parameterName

指定されたパラメータの名前を取得します。

```xpp
public str parameterName(int variableNumber)
```

### <a name="parameters---parametername"></a>パラメーター - parameterName

variableNumber  
メソッドのパラメーター リストへの 1 から始まるインデックス。

### <a name="return-value---parametername"></a>戻り値 - parameterName

指定されたパラメーターの名前。

## <a name="method-parameteroptional"></a>メソッド parameterOptional

メソッドの指定されたパラメーターが省略可能かどうかを示します。

```xpp
public boolean parameterOptional(int variableNumber)
```

### <a name="parameters---parameteroptional"></a>パラメーター - parameterOptional

variableNumber  
メソッドのパラメーター リストへの 1 から始まるインデックス。

### <a name="return-value---parameteroptional"></a>戻り値 - parameterOptional

パラメーターがオプションである場合は true。それ以外の場合は false。

## <a name="method-parametertype"></a>メソッド parameterType

```xpp
public Types parameterType(int variableNumber)
```

### <a name="parameters---parametertype"></a>パラメーター - parameterType

variableNumber  

### <a name="return-value---parametertype"></a>戻り値 - parameterType

## <a name="method-parentid"></a>メソッド parentId

メソッドを所有する親の ID を取得します。

```xpp
public int parentId()
```

### <a name="return-value---parentid"></a>戻り値 - parentId

メソッドを所有する親の ID。

## <a name="method-propertyhelp"></a>メソッド propertyHelp

メソッドに関連付けられているプロパティのヘルプ文字列を取得します。

```xpp
public str propertyHelp()
```

### <a name="return-value---propertyhelp"></a>戻り値 - propertyHelp

メソッドに関連付けられているプロパティのヘルプ文字列。ヘルプ文字列がない場合は、空の文字列。

### <a name="remarks---propertyhelp"></a>備考 - propertyHelp

このメソッドは、DictMethod::propertyMethod メソッドを呼び出して、メソッドがプロパティ メソッドかどうかを判定します。

## <a name="method-propertymethod"></a>メソッド propertyMethod

メソッドがプロパティ メソッドかどうかを示します。

```xpp
public NoYes propertyMethod()
```

### <a name="return-value---propertymethod"></a>戻り値 - propertyMethod

メソッドがプロパティ メソッドである場合は NoYes::No 列挙値、それ以外の場合は NoYes::Yes 列挙値。

## <a name="method-returnid"></a>メソッド returnId

値を返すメソッドについて、拡張データ型やクラスなどの特定の戻り値のデータ型の ID を指定します。

```xpp
public int returnId()
```

### <a name="return-value---returnid"></a>戻り値 - returnId

戻り値のデータ型の ID。データ型に ID がない場合またはメソッドが値を返さない場合は 0 (ゼロ) です。

## <a name="method-returntype"></a>メソッド returnType

メソッドの戻り値の型を指定します。

```xpp
public Types returnType()
```

### <a name="return-value---returntype"></a>戻り値 - returnType

メソッドの戻り値を示すタイプ列挙値。

### <a name="remarks---returntype"></a>備考 - returnType

表示される値は次のとおりです。

-   AnyType
-   BLOB
-   クラス
-   コンテナー
-   日
-   日時
-   列挙
-   グリッド
-   Int64
-   整数
-   実数
-   レコード
-   RString
-   文字列
-   UserType
-   VarString
-   無効

## <a name="method-runmode"></a>メソッド runMode

メソッドが実行される場所を指定します。

```xpp
public ClassRunMode runMode()
```

### <a name="return-value---runmode"></a>戻り値 - runMode

メソッドが実行される場所を示す ClassRunMode 列挙値。

### <a name="remarks---runmode"></a>備考 - runMode

表示される値は次のとおりです。

-   呼び出された
-   クライアント
-   ClientorServer
-   サーバー

## <a name="method-varcnt"></a>メソッド varCnt

メソッドの変数の数を取得します。

```xpp
public int varCnt()
```

### <a name="return-value---varcnt"></a>戻り値 - varCnt

メソッドのローカル変数と継承変数の数。

## <a name="method-varname"></a>メソッド varName

指定された変数の名前を取得します。

```xpp
public str varName(int variableNumber)
```

### <a name="parameters---varname"></a>パラメーター - varName

variableNumber  
メソッドの変数リストへの 1 から始まるインデックス。

### <a name="return-value---varname"></a>戻り値 - varName

指定された変数の名前。

## <a name="method-setmethod"></a>メソッド setMethod

MemberFunction クラスのインスタンスを使用して、アプリケーション オブジェクト ツリー (AOT) 内のノードのアプリケーション オブジェクト タイプを指定します。

```xpp
public void setMethod(MemberFunction method)
```

### <a name="parameters---setmethod"></a>パラメーター - setMethod

メソッド  
AOT 内のノードを表す MemberFunction クラスのインスタンス。

## <a name="method-new"></a>メソッド new

Object クラスの新しいインスタンスを初期化します。

```xpp
public void new(UtilElementType utilType, int id, str name)
```

### <a name="parameters---new"></a>パラメーター - new

utilType  

<!-- -->

id  

<!-- -->

名前  

