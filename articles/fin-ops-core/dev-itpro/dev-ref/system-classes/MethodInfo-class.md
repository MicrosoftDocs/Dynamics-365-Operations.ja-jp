---
title: MethodInfo クラス
description: このトピックでは､MethodInfo クラスについて説明します。
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
ms.openlocfilehash: 0de113c74623d6f57bebb19ee713c7619706b32c
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502572"
---
# <a name="class-methodinfo"></a>クラス MethodInfo

[!include [banner](../../includes/banner.md)]

```xpp
class MethodInfo extends Object
```

指定したメソッドについて説明します。

## <a name="remarks"></a>備考

SysDictTable クラスを使用してテーブル メソッドを MethodInfo に割り当てます。 SysDictClass クラスを使用してクラス メソッドを割り当てます。 次のクラスは MethodInfo を拡張しています。

-   SysMethodInfo
-   DictMethod

## <a name="examples"></a>例

次の例では、SysDictClass::ObjectMethodObject メソッドを使用して、FormBuildDataSource クラス オブジェクトのメソッドをMethodInfo クラスのインスタンスに割り当てます。 整数値はメソッドを指定します。 MethodInfo.name メソッドは、メソッド名を返します。

```xpp
void getMethodInfo() 
{ 
    MethodInfo methodInfo; 
    SysDictClass sysDictClass; 
    str name; 
    try 
    { 
        sysDictClass = new SysDictClass(classnum(FormBuildDataSource)); 
        methodInfo = sysDictClass.objectMethodObject(1); 
        if(!methodInfo) 
        { 
            throw exception::Error; 
        } 
        name = methodInfo.name(); 
        print name; 
        pause; 
     } 
     catch (exception::Error) 
     { 
        print "The specified method does not exist"; 
        pause; 
     } 
}
```

## <a name="methods"></a>メソッド

| 方法                                                      | 説明                                                                                                                                   |
|-------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| public AccessSpecifier accessSpecifier()                    | メソッドがパブリック、保護、またはプライベートかどうかを指定します。                                                                                |
| public boolean compiledOk()                                 | メソッドがコンパイルされているかどうかを指定します。                                                                                                    |
| public TableId displayTableId()                             |                                                                                                                                               |
| public DisplayFunctionType displayType()                    | メソッドの表示機能のタイプを指定します。                                                                                              |
| public Array getAllAttributes()                             | メソッドの属性の完全なセットを取得します。                                                                                               |
| public Object getAttribute(str attribute)                   | クラス ヘッダー メタデータから最初に一致する属性を取得し、その属性を表すオブジェクト クラスのインスタンスを作成し、返します。 |
| public Array getAttributes(str attribute)                   |                                                                                                                                               |
| public boolean isAbstract()                                 | メソッドが抽象かどうかを示します。                                                                                                     |
| public boolean isStatic()                                   | メソッドが静的かどうかを指定します。                                                                                                       |
| public str name()                                           | メソッドの名前を指定します。                                                                                                               |
| public int noParms()                                        | メソッド内のパラメーターの数を指定します。                                                                                               |
| public int noVars()                                         | メソッド内の変数の数を指定します。                                                                                                |
| public int parentId()                                       | テーブル メソッドのテーブル ID またはクラス メソッドのクラス ID を指定します。                                                                 |
| public str propertyHelp()                                   | メソッドがコントロールに設定または返すヘルプ テキストを指定します。                                                                          |
| public NoYes PropertyMethod()                               | メソッドがプロパティ メソッドかどうかを指定します。                                                                                              |
| public int returnId()                                       | 値を返すメソッドについて、拡張データ型やクラスなどの特定の戻り値のデータ型の ID を指定します。                   |
| public Types returnType()                                   | メソッドの戻り値の型を指定します。                                                                                                               |
| public ClassRunMode runMode()                               | メソッドが実行される場所を指定します。                                                                                                         |
| public int varId(int variableNumber)                        | 変数を含むメソッドについて、拡張データ型や列挙値などの特定の変数のデータ型の ID を指定します。                |
| public int varIdOld(int variableNumber)                     |                                                                                                                                               |
| public Types varType(int variableNumber)                    | Types 列挙の値を使用して変数のデータ型を指定します。                                                                    |
| public void new(UtilElementType utilType, int Id, str Name) | MethodInfo クラスの新しいインスタンスを作成します。                                                                                               |
| public void setMethod(MemberFunction method)                | インスタンスを使用してアプリケーション オブジェクト ツリー (AOT) 内のノードのアプリケーション オブジェクト タイプを指定します。                            |

## <a name="method-accessspecifier"></a>メソッド accessSpecifier

メソッドがパブリック、保護、またはプライベートかどうかを指定します。

```xpp
public AccessSpecifier accessSpecifier()
```

### <a name="return-value---accessspecifier"></a>戻り値 - accessSpecifier

メソッドがパブリック、保護、またはプライベートのいずれかを指定する AccessSpecifier 列挙型値です。

## <a name="method-compiledok"></a>メソッド compiledOk

メソッドがコンパイルされているかどうかを指定します。

```xpp
public boolean compiledOk()
```

### <a name="return-value---compiledok"></a>戻り値 - compiledOk

メソッドがコンパイル済みの場合は true。それ以外の場合は、false。

## <a name="method-displaytableid"></a>メソッド displayTableId

```xpp
public TableId displayTableId()
```

### <a name="return-value---displaytableid"></a>戻り値 - displayTableId

## <a name="method-displaytype"></a>メソッド displayType

メソッドの表示機能のタイプを指定します。

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
| RecordGet | このメソッドは、レコードを取得します。                   |
| RecordSet | このメソッドは、レコードを設定します。                   |
| セット       | このメソッドは、編集メソッドです。               |

## <a name="method-getallattributes"></a>メソッド getAllAttributes

メソッドの属性の完全なセットを取得します。

```xpp
public Array getAllAttributes()
```

### <a name="return-value---getallattributes"></a>戻り値 - getAllAttributes

メソッドの SysAttribute オブジェクトの配列。

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

## <a name="method-isabstract"></a>メソッド isAbstract

メソッドが抽象かどうかを示します。

```xpp
public boolean isAbstract()
```

### <a name="return-value---isabstract"></a>戻り値 - isAbstract

メソッドが抽象である場合は true。それ以外の場合は、false。

### <a name="remarks---isabstract"></a>備考 - isAbstract

抽象メソッドは宣言されていますが、親クラスで実装されていません。 詳細については、「メソッド モディファイア」を参照してください。

## <a name="method-isstatic"></a>メソッド isStatic

メソッドが静的かどうかを指定します。

```xpp
public boolean isStatic()
```

### <a name="return-value---isstatic"></a>戻り値 - isStatic

メソッドが静的である場合は true。それ以外の場合は、false。

### <a name="remarks---isstatic"></a>備考 - isStatic

詳細については、「静的メソッド」を参照してください。

## <a name="method-name"></a>メソッド名

メソッドの名前を指定します。

```xpp
public str name()
```

### <a name="return-value---name"></a>戻り値 - name

メソッド名を示す文字列。

## <a name="method-noparms"></a>メソッド noParms

メソッド内のパラメーターの数を指定します。

```xpp
public int noParms()
```

### <a name="return-value---noparms"></a>戻り値 - noParms

メソッド内のパラメータの数を示す整数値。

## <a name="method-novars"></a>メソッド noVars

メソッド内の変数の数を指定します。

```xpp
public int noVars()
```

### <a name="return-value---novars"></a>戻り値 - noVars

メソッド内の変数の数を示す整数値。

## <a name="method-parentid"></a>メソッド parentId

テーブル メソッドのテーブル ID またはクラス メソッドのクラス ID を指定します。

```xpp
public int parentId()
```

### <a name="return-value---parentid"></a>戻り値 - parentId

テーブル ID またはクラス ID を示す整数値。

## <a name="method-propertyhelp"></a>メソッド propertyHelp

メソッドがコントロールに設定または返すヘルプ テキストを指定します。

```xpp
public str propertyHelp()
```

### <a name="return-value---propertyhelp"></a>戻り値 - propertyHelp

ヘルプ テキストを含む文字列。

## <a name="method-propertymethod"></a>メソッド PropertyMethod

メソッドがプロパティ メソッドかどうかを指定します。

```xpp
public NoYes PropertyMethod()
```

### <a name="return-value---propertymethod"></a>戻り値 - PropertyMethod

メソッドがプロパティ メソッドの場合は 1、それ以外の場合は、0 です。

### <a name="remarks---propertymethod"></a>備考 - PropertyMethod

プロパティ メソッドは、プロパティを設定または返します。

## <a name="method-returnid"></a>メソッド returnId

値を返すメソッドについて、拡張データ型やクラスなどの特定の戻り値のデータ型の ID を指定します。

```xpp
public int returnId()
```

### <a name="return-value---returnid"></a>戻り値 - returnId

戻り値のデータ型の ID を示す整数値。

### <a name="remarks---returnid"></a>備考 - returnId

データ型に ID がない場合またはメソッドが値を返さない場合、戻り値は 0 です。

## <a name="method-returntype"></a>メソッド returnType

メソッドの戻り値の型を指定します。

```xpp
public Types returnType()
```

### <a name="return-value---returntype"></a>戻り値 - returnType

メソッドの戻り値を示すタイプ列挙値。

### <a name="remarks---returntype"></a>備考 - returnType

表示される値は次のとおりです。 :

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

## <a name="method-varid"></a>メソッド varId

変数を含むメソッドについて、拡張データ型や列挙値などの特定の変数のデータ型の ID を指定します。

```xpp
public int varId(int variableNumber)
```

### <a name="parameters---varid"></a>パラメーター - varId

variableNumber  
メソッドに一覧表示されている変数の順序に基づいてメソッド変数を指定する整数値。

### <a name="return-value---varid"></a>戻り値 - varid

変数のデータ型 ID を示す整数値。

### <a name="remarks---varid"></a>備考 - varid

データ型に ID がない場合またはメソッドに変数がない場合、戻り値は 0 です。

## <a name="method-varidold"></a>メソッド varIdOld

```xpp
public int varIdOld(int variableNumber)
```

### <a name="parameters---varidold"></a>パラメーター - varIdOld

variableNumber  

### <a name="return-value---varidold"></a>戻り値 - varldOld

## <a name="method-vartype"></a>メソッド varType

Types 列挙の値を使用して変数のデータ型を指定します。

```xpp
public Types varType(int variableNumber)
```

### <a name="parameters---vartype"></a>パラメーター - varType

variableNumber  
メソッドに一覧表示されている変数の順序に基づいてメソッド変数を指定する整数。

### <a name="return-value---vartype"></a>戻り値 - varType

変数のデータ型を示すタイプ列挙値。

### <a name="remarks---vartype"></a>備考 - varType

以下は使用可能な値です。

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

## <a name="method-new"></a>メソッド new

MethodInfo クラスの新しいインスタンスを作成します。

```xpp
public void new(UtilElementType utilType, int Id, str Name)
```

### <a name="parameters---new"></a>パラメーター - new

utilType  
要素の名前を指定する文字列。

<!-- -->

ID  
要素の名前を指定する文字列。

<!-- -->

氏名  
要素の名前を指定する文字列。

## <a name="method-setmethod"></a>メソッド setMethod

アプリケーション オブジェクト ツリー (AOT) 内のノードのアプリケーション オブジェクト タイプを指定します。

```xpp
public void setMethod(MemberFunction method)
```

### <a name="parameters---setmethod"></a>パラメーター - setMethod

メソッド  
AOT 内のノードを表す MemberFunction クラスのインスタンス。

