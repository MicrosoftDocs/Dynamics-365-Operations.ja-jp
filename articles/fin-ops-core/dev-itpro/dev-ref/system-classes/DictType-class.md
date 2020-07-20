---
title: DictType クラス
description: このトピックでは、DictType クラスについて説明します。
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
ms.openlocfilehash: 36be5e4e79546ac5ba5900ddccbef6d64ecbf056
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502676"
---
# <a name="class-dicttype"></a>クラス DictType

[!include [banner](../../includes/banner.md)]

```xpp
class DictType extends Object
```

DictType クラスは、拡張データ型を管理します。

## <a name="remarks"></a>備考

SysDictType クラスは DictType を拡張します。

## <a name="examples"></a>例

## <a name="methods"></a>メソッド

| 方法                                                                | 説明                                                                                                                                                              |
|-----------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| public Alignment alignment()                                          | 拡張データ型の配置を取得します。                                                                                                                      |
| public int arraySize()                                                | 拡張データ型の配列サイズを提供します。                                                                                                                       |
| public Types baseType()                                               | タイプ列挙値を使うことで、拡張データ型の基になるデータ型を提供します。                                                                          |
| public ConfigurationKeyId configurationKeyId()                        | 拡張データ型のコンフィギュレーション キーの ID を返します。                                                                                                      |
| public int displayHeight(\[boolean useDefaults\])                     | タイプの表示の高さを取得します。                                                                                                                               |
| public int displayLength(\[boolean useDefaults\])                     |                                                                                                                                                                          |
| public EnumId enumId()                                                | 拡張データ型の基になる列挙型の ID を提供します。                                                                                        |
| public ExtendedTypeId extend()                                        | 拡張データ型が拡張される拡張データ型の ID を提供します。                                                                                           |
| public List extendedBy(\[boolean allLevels\])                         | 現在の EDT により拡張された拡張データ型 (EDT) のタイプ ID の一覧を取得します。                                                                        |
| public str formHelp()                                                 |                                                                                                                                                                          |
| public str getControlClass()                                          |                                                                                                                                                                          |
| public container getCountryRegionCodes()                              | 定義されている国/地域コードを保持するコンテナーを取得します。                                                                                              |
| public DictRelation getLookupRelation(\[int arrayIndex\])             |                                                                                                                                                                          |
| public AnyType getValue(\[int arrayIndex\])                           |                                                                                                                                                                          |
| public str help(\[int arrayIndex\], \[boolean useInterfaceLanguage\]) | 拡張データ型または指定した配列要素、または拡張データ型を拡張する拡張データ型に表示されるヘルプ テキストを提供します。       |
| public str helpDefined(\[int arrayIndex\])                            | 拡張データ型の help プロパティの値を返します。                                                                                                       |
| public ExtendedTypeId id()                                            | 拡張データ型の ID を提供します。                                                                                                                               |
| public boolean isExtendedFrom(str baseEDTName)                        | 拡張データ型が、提供される基本拡張データ型から拡張するかどうかを決定します。                                                                     |
| public int isRadioStyle()                                             | 列挙データ型に基づいている拡張データ型のスタイルがオプション ボタンまたはコンボ ボックスであるかどうかを示します。                                                |
| public str label(\[int arrayIndex\])                                  | 拡張データ型または指定した配列要素、または拡張データ型を拡張する拡張データ型のラベルに表示されるラベル テキストを提供します。 |
| public str labelDefined(\[int arrayIndex\])                           | 拡張データ型の label プロパティの値を返します。                                                                                                      |
| public str lookupTable(\[boolean useInheritedMetaData\])              |                                                                                                                                                                          |
| public str name()                                                     | 拡張データ型の名前を提供します。                                                                                                                              |
| public DictRelation relationObject(\[int arrayIndex\])                | DictRelation オブジェクトを返すことで、拡張データ型または指定された配列要素に対して定義されている関係に関する情報を提供します。                         |
| public int stringLen()                                                | 文字列データ型に基づいている拡張データ型の文字列の長さを提供します。                                                                              |
| public boolean stringRight()                                          | 文字列が文字列データ型に基づいている拡張データ型で右揃えかどうかを示します。                                                         |
| ::public static Alignment getTypeAlignment(Types type)                |                                                                                                                                                                          |
| ::public static int getTypeDisplayHeight(Types type)                  |                                                                                                                                                                          |
| ::public static int getTypeDisplayLength(Types type)                  | 組み込み型の表示の長さを取得します。                                                                                                                         |
| public void setValue(AnyType Value, \[int arrayEntry\])               |                                                                                                                                                                          |
| public void new(ExtendedTypeId typeId)                                | Object クラスの新しいインスタンスを初期化します。                                                                                                                          |
| public void setStringLen(int stringLen)                               | 文字列データ型に基づいている拡張データ型の文字列の長さを設定します。                                                                                  |
| public void setStringRight(boolean right)                             | 文字列データ型に基づいている拡張データ型の文字列の妥当性を示します。                                                                        |

## <a name="method-alignment"></a>メソッド alignment

拡張データ型の配置を取得します。

```xpp
public Alignment alignment()
```

### <a name="return-value---alignment"></a>戻り値 - alignment

拡張データ型の配置。

## <a name="method-arraysize"></a>メソッド arraySize

拡張データ型の配列サイズを提供します。

```xpp
public int arraySize()
```

### <a name="return-value---arraysize"></a>戻り値 - arraySize

配列サイズの整数値。拡張データ型に配列要素がない場合は 1 。

### <a name="examples---arraysize"></a>例 - arraySize

次の例では、arraySize メソッドは XMLMapDimension 拡張データ型の配列のサイズを返します。

```xpp
    DictType dicttype; 
    int i; 
    dicttype = new DictType(extendedTypeNum(XMLMapDimension)); 
    for (i = 1;  i < dicttype.arraySize(); i++) 
    { 
        print dicttype.label(i); 
        pause; 
    }
```

## <a name="method-basetype"></a>メソッド baseType

タイプ列挙値を使うことで、拡張データ型の基になるデータ型を提供します。

```xpp
public Types baseType()
```

### <a name="return-value---basetype"></a>戻り値 - baseType

データ型を示すタイプ列挙値。

### <a name="remarks---basetype"></a>備考 - baseType

Global::Enum2Value メソッドを使用して、戻り値を文字列に変換することができます。

## <a name="method-configurationkeyid"></a>メソッド configurationKeyId

拡張データ型のコンフィギュレーション キーの ID を返します。

```xpp
public ConfigurationKeyId configurationKeyId()
```

### <a name="return-value---configurationkeyid"></a>戻り値 - configurationKeyId

拡張データ型のコンフィギュレーション キーの ID。

## <a name="method-displayheight"></a>メソッド displayHeight

タイプの表示の高さを取得します。

```xpp
public int displayHeight([boolean useDefaults])
```

### <a name="parameters---displayheight"></a>パラメーター - displayHeight

useDefaults  
タイプに長さがない場合に既定値を使用するかどうかを示すブール値。

### <a name="return-value---displayheight"></a>戻り値 - displayHeight

タイプの表示の高さ。

## <a name="method-displaylength"></a>メソッド displayLength

```xpp
public int displayLength([boolean useDefaults])
```

### <a name="parameters---displaylength"></a>パラメーター - displayLength

useDefaults  

### <a name="return-value---displaylength"></a>戻り値 - displayLength

## <a name="method-enumid"></a>メソッド enumId

拡張データ型の基になる列挙型の ID を提供します。

```xpp
public EnumId enumId()
```

### <a name="return-value---enumid"></a>戻り値 - enumId

拡張データ型の基になる列挙タイプのID。拡張データ型が列挙値に基づかない場合は 0 (ゼロ)。

### <a name="remarks---enumid"></a>備考 - enumId

baseType メソッドを使用すると、拡張データ タイプのデータ タイプを判断することができます。

## <a name="method-extend"></a>メソッド extend

拡張データ型が拡張される拡張データ型の ID を提供します。

```xpp
public ExtendedTypeId extend()
```

### <a name="return-value---extend"></a>戻り値 - extend

拡張データ型を超えた拡張データ型の ID。拡張データ型が拡張データ型を超えていない場合は 0 (ゼロ)。

### <a name="examples---extend"></a>例 - extend

次の例では、拡張メソッドは ABCPercentA 拡張データ型が拡張する拡張データ型の ID を返します。

```xpp
    DictType dicttype; 
    dicttype = new DictType(extendedTypeNum(ABCPercentA)); 
    print dicttype.name() + " extends: " + extendedTypeId2Name(dicttype.extend());
```

## <a name="method-extendedby"></a>メソッド extendedBy

現在の EDT により拡張された拡張データ型 (EDT) のタイプ ID の一覧を取得します。

```xpp
public List extendedBy([boolean allLevels])
```

### <a name="parameters---extendedby"></a>パラメーター - extendedBy

allLevels  

### <a name="return-value---extendedby"></a>戻り値 - extendedBy

現在の EDT により拡張された EDT のタイプ ID の一覧。

## <a name="method-formhelp"></a>メソッド formHelp

```xpp
public str formHelp()
```

### <a name="return-value---formhelp"></a>戻り値 - formHelp

## <a name="method-getcontrolclass"></a>メソッド getControlClass

```xpp
public str getControlClass()
```

### <a name="return-value---getcontrolclass"></a>戻り値 - getControlClass

## <a name="method-getcountryregioncodes"></a>メソッド getCountryRegionCodes

定義されている国/地域コードを保持するコンテナーを取得します。

```xpp
public container getCountryRegionCodes()
```

### <a name="return-value---getcountryregioncodes"></a>戻り値 - getCountryRegionCodes

国/地域コードを保持するコンテナーです。

## <a name="method-getlookuprelation"></a>メソッド getLookupRelation

```xpp
public DictRelation getLookupRelation([int arrayIndex])
```

### <a name="parameters---getlookuprelation"></a>パラメーター - getLookupRelation

arrayIndex  

### <a name="return-value---getlookuprelation"></a>戻り値 - getLookupRelation

## <a name="method-getvalue"></a>メソッド getValue

```xpp
public AnyType getValue([int arrayIndex])
```

### <a name="parameters---getvalue"></a>パラメーター - getValue

arrayIndex  

### <a name="return-value---getvalue"></a>戻り値 - getValue

## <a name="method-help"></a>メソッド help

拡張データ型または指定した配列要素、または拡張データ型を拡張する拡張データ型に表示されるヘルプ テキストを提供します。

```xpp
public str help([int arrayIndex], [boolean useInterfaceLanguage])
```

### <a name="parameters---help"></a>パラメーター - help

arrayIndex  
ユーザー インターフェイス言語がヘルプ テキストに使用されているかどうかを示すブール値; オプション。

<!-- -->

useInterfaceLanguage  
ユーザー インターフェイス言語がヘルプ テキストに使用されているかどうかを示すブール値; オプション。

### <a name="return-value---help"></a>戻り値 - help

拡張データ型に表示されるヘルプ テキストの文字列値、または arrayEntry 値が提供される場合の配列要素。 ヘルプ テキストは、AOT 内の拡張データ型のヘルプ テキスト プロパティ、またはアプリケーション オブジェクト ツリー (AOT) 内の配列要素に対応します。 拡張データ型にヘルプ テキストがないとき、このメソッドは、拡張データ型が拡張する拡張データ型に対して定義されているヘルプ テキストを返します。

## <a name="method-helpdefined"></a>メソッド helpDefined

拡張データ型の help プロパティの値を返します。

```xpp
public str helpDefined([int arrayIndex])
```

### <a name="parameters---helpdefined"></a>パラメーター - helpDefined

arrayIndex  

### <a name="return-value---helpdefined"></a>戻り値 - helpDefined

拡張データ型の場合は help プロパティの値、arrayEntry 値が指定されている場合は配列要素の値。 ヘルプ テキストは、AOT 内の拡張データ型のヘルプ テキスト プロパティ、または AOT 内の array 要素に対応します。

## <a name="method-id"></a>メソッド id

拡張データ型の ID を提供します。

```xpp
public ExtendedTypeId id()
```

### <a name="return-value---id"></a>戻り値 - id

拡張データ型の ID を示すデータ型の値です。

## <a name="method-isextendedfrom"></a>メソッド isExtendedFrom

拡張データ型が、提供される基本拡張データ型から拡張するかどうかを決定します。

```xpp
public boolean isExtendedFrom(str baseEDTName)
```

### <a name="parameters---isextendedfrom"></a>パラメーター - isExtendedFrom

baseEDTName  
拡張データ型の名前。

### <a name="return-value---isextendedfrom"></a>戻り値 - isExtendedFrom

用意された基本拡張データ型から拡張データ型が拡張される場合は true。それ以外の場合は、false。

## <a name="method-isradiostyle"></a>メソッド isRadioStyle

列挙データ型に基づいている拡張データ型のスタイルがオプション ボタンまたはコンボ ボックスであるかどうかを示します。

```xpp
public int isRadioStyle()
```

### <a name="return-value---isradiostyle"></a>戻り値 - isRadioStyle

スタイルがオプション ボタンである場合は 1、それ以外の場合は 0 (ゼロ) です。

## <a name="method-label"></a>メソッド label

拡張データ型または指定した配列要素、または拡張データ型を拡張する拡張データ型のラベルに表示されるラベル テキストを提供します。

```xpp
public str label([int arrayIndex])
```

### <a name="parameters---label"></a>パラメーター - label

arrayIndex  

### <a name="return-value---label"></a>戻り値 - label

拡張データ タイプの場合に表示されるラベル、または arrayEntry 値が指定されている場合は配列要素のラベル。 拡張データ型にラベルがないとき、このメソッドは、拡張データ型が拡張する拡張データ型に対して定義されているラベルを返します。

### <a name="remarks---label"></a>備考 - label

返されるラベルは、AOT の拡張データ型または配列要素のラベル プロパティに対応します。

## <a name="method-labeldefined"></a>メソッド labelDefined

拡張データ型の label プロパティの値を返します。

```xpp
public str labelDefined([int arrayIndex])
```

### <a name="parameters---labeldefined"></a>パラメーター - labelDefined

arrayIndex  

### <a name="return-value---labeldefined"></a>戻り値 - labelDefined

拡張データ型の場合は label プロパティの値、arrayEntry 値が指定されている場合は配列要素の値。

### <a name="remarks---labeldefined"></a>備考 - labelDefined

戻り値は、AOT 内の拡張データ型のラベルプロパティ、またはAOT 内の array 要素に対応します。

## <a name="method-lookuptable"></a>メソッド lookupTable

```xpp
public str lookupTable([boolean useInheritedMetaData])
```

### <a name="parameters---lookuptable"></a>パラメーター - lookupTable

useInheritedMetaData  

### <a name="return-value---lookuptable"></a>戻り値 - lookupTable

## <a name="method-name"></a>メソッド名

拡張データ型の名前を提供します。

```xpp
public str name()
```

### <a name="return-value---name"></a>戻り値 - name

名前の文字列値。 名前は、AOT 内の拡張データ型の名前プロパティに対応します。

## <a name="method-relationobject"></a>メソッド relationObject

DictRelation オブジェクトを返すことで、拡張データ型または指定された配列要素に対して定義されている関係に関する情報を提供します。

```xpp
public DictRelation relationObject([int arrayIndex])
```

### <a name="parameters---relationobject"></a>パラメーター - relationObject

arrayIndex  

### <a name="return-value---relationobject"></a>戻り値 - relationObject

関係に関する情報を提供する DictRelation オブジェクト。

### <a name="remarks---relationobject"></a>備考 - relationObject

拡張データ型および配列要素に対して関係が定義されていない場合、DictRelation インスタンスを後続使用すると、実行時にエラーが発生します。

### <a name="examples---relationobject"></a>例 - relationObject

次の例では、relationObject メソッドは XMLMapDimension 拡張データ型の DictRelation オブジェクトを返します。

```xpp
    DictType dicttype; 
    DictRelation dictrelation; 
    dicttype = new DictType(extendedTypeNum(XMLMapDimension)); 
    dictrelation = dicttype.relationObject(); 
    if(dictrelation) 
    { 
        print "Relation lines: " + int2str(dictrelation.lines()); 
    } 
    else 
    { 
        print "No relations defined."; 
     }
```

## <a name="method-stringlen"></a>メソッド stringLen

文字列データ型に基づいている拡張データ型の文字列の長さを提供します。

```xpp
public int stringLen()
```

### <a name="return-value---stringlen"></a>戻り値 - stringLen

文字列の長さを示す整数。拡張データ型が文字列データ型に基づいていない場合は 0 (ゼロ) 。

## <a name="method-stringright"></a>メソッド stringRight

文字列が文字列データ型に基づいている拡張データ型で右揃えかどうかを示します。

```xpp
public boolean stringRight()
```

### <a name="return-value---stringright"></a>戻り値 - stringRight

文字列が右揃えの場合は true。それ以外の場合は、false。

### <a name="remarks---stringright"></a>備考 - stringRight

戻り値は、AOT 内の拡張データ型の調整プロパティに対応します。

## <a name="method-gettypealignment"></a>メソッド getTypeAlignment

```xpp
public static Alignment getTypeAlignment(Types type)
```

### <a name="parameters---gettypealignment"></a>パラメーター - getTypeAlignment

タイプ  

### <a name="return-value---gettypealignment"></a>戻り値 - getTypeAlignment

## <a name="method-gettypedisplayheight"></a>メソッド getTypeDisplayHeight

```xpp
public static int getTypeDisplayHeight(Types type)
```

### <a name="parameters---gettypedisplayheight"></a>パラメーター - getTypeDisplayHeight

タイプ  

### <a name="return-value---gettypedisplayheight"></a>戻り値 - getTypeDisplayHeight

## <a name="method-gettypedisplaylength"></a>メソッド getTypeDisplayLength

組み込み型の表示の長さを取得します。

```xpp
public static int getTypeDisplayLength(Types type)
```

### <a name="parameters---gettypedisplaylength"></a>パラメーター - getTypeDisplayLength

タイプ  
タイプ。

### <a name="return-value---gettypedisplaylength"></a>戻り値 - getTypeDisplayLength

組み込み型の表示の長さ。

## <a name="method-setvalue"></a>メソッド setValue

```xpp
public void setValue(AnyType Value, [int arrayEntry])
```

### <a name="parameters---setvalue"></a>パラメーター - setValue

先頭値  

<!-- -->

arrayEntry  

## <a name="method-new"></a>メソッド new

Object クラスの新しいインスタンスを初期化します。

```xpp
public void new(ExtendedTypeId typeId)
```

### <a name="parameters---new"></a>パラメーター - new

typeId  
拡張データ型の ID を示すデータ型です。

### <a name="remarks---new"></a>備考 - new

TypeId 値が無効な拡張データ型 ID である場合にこのコンストラクターは失敗しません。ただし、DictType インスタンスを使用すると、実行時にエラーが発生します。 extendedTypeNum 関数を使用して、ID の代わりに拡張データ タイプの名前を渡すことができます。

### <a name="examples---new"></a>例 - new

次の例は、DictType クラスのインスタンスを作成する方法を示しています。

```xpp
    DictType dicttype; 
    dicttype = new DictType(extendedTypeNum(ABCModelType));
```

## <a name="method-setstringlen"></a>メソッド setStringLen

文字列データ型に基づいている拡張データ型の文字列の長さを設定します。

```xpp
public void setStringLen(int stringLen)
```

### <a name="parameters---setstringlen"></a>パラメーター - setStringLen

stringLen  
文字列の長さを示す整数。

### <a name="remarks---setstringlen"></a>備考 - setStringLen

このメソッドを使用すると、X++ コードとメタデータを作成、読み込み、更新、および削除ができます。 この API が呼び出される前に、ユーザーが開発セキュリティ キー (SysDevelopment) にアクセスできることを確認します。 文字列の長さは、AOT 内の拡張データ型 StringSize プロパティに対応します。

### <a name="examples---setstringlen"></a>例 - setStringLen

次の例では、AccountName 拡張データ型の StringSize プロパティを 10 に設定します。

```xpp
server static public void Main(Args _args) 
{ 
    DictType  dt; 
    dt = new DictType(ExtendedTypeNum(AccountName)); 
    if (dt) 
    { 
        dt.setStringLen(10); 
    } 
}
```

## <a name="method-setstringright"></a>メソッド setStringRight

文字列データ型に基づいている拡張データ型の文字列の妥当性を示します。

```xpp
public void setStringRight(boolean right)
```

### <a name="parameters---setstringright"></a>パラメーター - setStringRight

権限  
ブール値: 右揃え文字列の場合は true、左揃え文字列の場合は false。

### <a name="remarks---setstringright"></a>備考 - setStringRight

このメソッドを使用すると、X++ コードとメタデータを作成、読み込み、更新、および削除ができます。 この API が呼び出される前に、ユーザーが開発セキュリティ キー (SysDevelopment) にアクセスできることを確認します。

### <a name="examples---setstringright"></a>例 - setStringRight

次の例では、AccountName 拡張データ型の正当性を設定します。

```xpp
server static public void Main(Args _args) 
{ 
    DictType dt; 
    dt = new DictType(ExtendedTypeNum(AccountName)); 
    if (dt) 
    { 
        dt.setStringRight(true); 
    } 
}
```

