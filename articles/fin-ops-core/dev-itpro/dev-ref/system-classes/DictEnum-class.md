---
title: DictEnum クラス
description: このトピックでは、DictEnum クラスについて説明します。
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
ms.openlocfilehash: aeafb4d05a4157ae5294b1543267b833a11f965f
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502992"
---
# <a name="class-dictenum"></a>クラス DictEnum

[!include [banner](../../includes/banner.md)]

```xpp
class DictEnum extends Object
```

DictEnum クラスは、アプリケーション オブジェクト ツリー (AOT) で基本列挙の列挙値に関するメタ情報を取得します。

## <a name="remarks"></a>備考

下位互換性については、プロパティに変換される、またはプロパティから変換されるメソッドの特別な名前付け規則が使用されます。

|                 |                                |                          |
|-----------------|--------------------------------|--------------------------|
|      氏名       |            ReqDate             | 記号 (文字列として型設定) |
|      ラベル      | @SYS18075 (「要求日」) |      名前またはラベル       |
|   FeatureKey    |         ReqSchedAction         |        FeatureKey        |
|    EnumValue    |               0                |          先頭値           |
| AOT の位置 |       最初 (インデックス = 0)        |          指数           |

この例では、ActionBasicDateType 基本列挙から取得されます。 列挙に関する一般情報については、開発者ガイドを参照してください。

## <a name="examples"></a>例

## <a name="methods"></a>メソッド

| 方法                                                            | 説明                                                                                                               |
|-------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| public ConfigurationKeyId configurationKeyId()                    | 列挙値のコンフィギュレーション キー ID を返します。                                                                     |
| public int displayLength(\[boolean useLongestLabel\])             |                                                                                                                           |
| public container getCountryRegionCodes()                          |                                                                                                                           |
| public str help(\[boolean useInterfaceLanguage\])                 | この列挙型のヘルプ テキストを取得します。                                                                             |
| public str helpDefined()                                          | この列挙型に対する help プロパティの値を返します。                                                              |
| public EnumId id()                                                | 列挙値の列挙 ID を返します。                                                                            |
| public ConfigurationKeyId index2ConfigurationKey(int index)       |                                                                                                                           |
| public container index2CountryRegionCodes(int index)              |                                                                                                                           |
| public str index2Label(int index)                                 | インデックスにより指定される列挙項目のラベルを返します。                                                  |
| public str index2LabelId(int index)                               |                                                                                                                           |
| public str index2Name(int index)                                  | インデックスにより指定される列挙項目のラベルを返します。                                                  |
| public str index2Symbol(int index)                                | インデックスにより指定される列挙項目のシンボルまたは名前を返します。                                         |
| public int index2Value(int index)                                 | インデックスにより指定される列挙項目の値を返します。                                                  |
| public str label()                                                | 列挙値のラベル テキストを返します。                                                                                |
| public str labelDefined()                                         | この列挙型に対する label プロパティの値を返します。                                                             |
| public str name()                                                 | 列挙型の名前を返します。                                                                                      |
| public int name2Value(str name)                                   | ラベルにより参照される項目の列挙値を返します。                                                |
| public boolean showAsRadio()                                      | 列挙をコンボ ボックスではなくラジオ ボタンを使用して表示するかどうかを示す値を返します。 |
| public int symbol2Value(str name)                                 | シンボルまたは名前により参照される項目の列挙値を返します。                                              |
| public ConfigurationKeyId value2ConfigurationKey(int value)       | 指定した列挙値のコンフィギュレーション キー ID を返します。                                                        |
| public container value2CountryRegionCodes(int value)              |                                                                                                                           |
| public str value2Label(int value)                                 | 指定された列挙値のラベルを返します。                                                                       |
| public str value2Name(int value)                                  | 指定された列挙値の名前を返します。                                                                        |
| public str value2Symbol(int value)                                | 記号、または指定した列挙値の Name プロパティの値を返します。                                  |
| public int values()                                               | 列挙型内の項目の数を返します。                                                                           |
| ::public static str queryFilterNames2Values(QueryFilter filter)   |                                                                                                                           |
| ::public static str queryFilterValues2Names(QueryFilter filter)   |                                                                                                                           |
| ::public static str queryRangeNames2Values(QueryBuildRange range) |                                                                                                                           |
| ::public static str queryRangeValues2Names(QueryBuildRange range) |                                                                                                                           |
| ::public static int value2id(AnyType value)                       | 指定された値の列挙 ID を返します。                                                                          |
| public void new(EnumId typeId)                                    | Object クラスの新しいインスタンスを初期化します。                                                                           |

## <a name="method-configurationkeyid"></a>メソッド configurationKeyId

列挙値のコンフィギュレーション キー ID を返します。

```xpp
public ConfigurationKeyId configurationKeyId()
```

### <a name="return-value---configurationkeyid"></a>戻り値 - configurationKeyId

列挙のコンフィギュレーション キー ID がない場合の列挙のコンフィギュレーション キー ID は 0 (ゼロ)。

### <a name="examples---configurationkeyid"></a>例 - configurationKeyId

次の例は、列挙型のコンフィギュレーション キー ID の取得を示しています。

```xpp
DictEnum de; 
int      i; 
de = new DictEnum(enumName2Id("ActionType")); 
print int2str(de.configurationKeyId());
```

## <a name="method-displaylength"></a>メソッド displayLength

```xpp
public int displayLength([boolean useLongestLabel])
```

### <a name="parameters---displaylength"></a>パラメーター - displayLength

useLongestLabel  

### <a name="return-value---displaylength"></a>戻り値 - displayLength

## <a name="method-getcountryregioncodes"></a>メソッド getCountryRegionCodes

```xpp
public container getCountryRegionCodes()
```

### <a name="return-value---getcountryregioncodes"></a>戻り値 - getCountryRegionCodes

## <a name="method-help"></a>メソッド help

この列挙型のヘルプ テキストを取得します。

```xpp
public str help([boolean useInterfaceLanguage])
```

### <a name="parameters---help"></a>パラメーター - help

useInterfaceLanguage  

### <a name="return-value---help"></a>戻り値 - help

ヘルプ テキストを含む文字列、ヘルプ テキストが定義されていない場合、空の文字列。

### <a name="remarks---help"></a>備考 - help

ヘルプ テキストは、基本列挙のヘルプ プロパティで定義されます。

## <a name="method-helpdefined"></a>メソッド helpDefined

この列挙型に対する help プロパティの値を返します。

```xpp
public str helpDefined()
```

### <a name="return-value---helpdefined"></a>戻り値 - helpDefined

この列挙型に対する help プロパティの値。

## <a name="method-id"></a>メソッド id

列挙値の列挙 ID を返します。

```xpp
public EnumId id()
```

### <a name="return-value---id"></a>戻り値 - id

この列挙の列挙 ID。

## <a name="method-index2configurationkey"></a>メソッド index2ConfigurationKey

```xpp
public ConfigurationKeyId index2ConfigurationKey(int index)
```

### <a name="parameters---index2configurationkey"></a>パラメーター - index2ConfigurationKey

指数  

### <a name="return-value---index2configurationkey"></a>戻り値 - index2ConfigurationKey

## <a name="method-index2countryregioncodes"></a>メソッド index2CountryRegionCodes

```xpp
public container index2CountryRegionCodes(int index)
```

### <a name="parameters---index2countryregioncodes"></a>パラメーター - index2CountryRegionCodes

指数  

### <a name="return-value---index2countryregioncodes"></a>戻り値 - index2CountryRegionCodes

## <a name="method-index2label"></a>メソッド index2Label

インデックスにより指定される列挙項目のラベルを返します。

```xpp
public str index2Label(int index)
```

### <a name="parameters---index2label"></a>パラメーター - index2Label

指数  
AOT の列挙体の 0 から始まるインデックス。

### <a name="return-value---index2label"></a>戻り値 - index2Label

インデックスで指定された列挙項目のラベル。インデックスが有効な列挙項目を参照しない場合は空の文字列。

### <a name="examples---index2label"></a>例 - index2Label

次の例は、列挙型内の項目のラベルの取得を示しています。

```xpp
DictEnum de; 
int      i; 
de = new DictEnum(enumName2Id("ActionType")); 
for (i=0; i < de.values(); i++) 
{ 
    print int2str(i) + ", " + de.index2Label(i); 
}
```

## <a name="method-index2labelid"></a>メソッド index2LabelId

```xpp
public str index2LabelId(int index)
```

### <a name="parameters---index2labelid"></a>パラメーター - index2LabelId

指数  

### <a name="return-value---index2labelid"></a>戻り値 - index2LabelId

## <a name="method-index2name"></a>メソッド index2Name

インデックスにより指定される列挙項目のラベルを返します。

```xpp
public str index2Name(int index)
```

### <a name="parameters---index2name"></a>パラメーター - index2Name

指数  
AOT の列挙体の 0 から始まるインデックス。

### <a name="return-value---index2name"></a>戻り値 - index2Name

インデックスで指定された列挙項目のラベル。インデックスが有効な列挙項目を参照しない場合は空の文字列。

### <a name="remarks---index2name"></a>備考 - index2Name

以前のバージョンとの下位互換性については、DictEnum::value2Name の「名前」は、列挙項目のラベル プロパティを参照します。 コードを読みやすくするには、DictEnum::value2Name メソッドの代わりに DictEnum::value2Label メソッドを使用します。 AOT に示すように、列挙型項目の name プロパティの値を取得するには、DictEnum::value2Symbol メソッドを使用します。

### <a name="examples---index2name"></a>例 - index2Name

次の例は、列挙型内の項目のラベルの取得を示しています。

```xpp
DictEnum de; 
int      i; 
de = new DictEnum(enumName2Id("ActionType")); 
for (i=0; i < de.values(); i++) 
{ 
    print int2str(i) + ", " + de.index2Name(i); 
}
```

## <a name="method-index2symbol"></a>メソッド index2Symbol

インデックスにより指定される列挙項目のシンボルまたは名前を返します。

```xpp
public str index2Symbol(int index)
```

### <a name="parameters---index2symbol"></a>パラメーター - index2Symbol

指数  
AOT の列挙体の 0 から始まるインデックス。

### <a name="return-value---index2symbol"></a>戻り値 - index2Symbol

インデックスで指定される列挙型項目のシンボル。インデックスが有効な列挙型項目を参照しない場合は空の文字列。

### <a name="remarks---index2symbol"></a>備考 - index2Symbol

シンボルは、AOT の列挙型項目の Name プロパティに対応します。

### <a name="examples---index2symbol"></a>例 - index2Symbol

次の例は、列挙型内の項目の記号の取得を示しています。

```xpp
DictEnum de; 
int      i; 
de = new DictEnum(enumName2Id("ActionType")); 
for (i=0; i < de.values(); i++) 
{ 
    print int2str(i) + ", " + de.index2Symbol(i); 
}
```

## <a name="method-index2value"></a>メソッド index2Value

インデックスにより指定される列挙項目の値を返します。

```xpp
public int index2Value(int index)
```

### <a name="parameters---index2value"></a>パラメーター - index2Value

指数  
AOT の列挙体の 0 から始まるインデックス。

### <a name="return-value---index2value"></a>戻り値 - index2Value

インデックスで指定される列挙項目の値。

### <a name="examples---index2value"></a>例 - index2Value

次の例は、列挙型内の項目の値の取得を示しています。

```xpp
DictEnum de; 
int      i; 
de = new DictEnum(enumName2Id("ActionType")); 
for (i=0; i < de.values(); i++) 
{ 
    print int2str(i) + ", " + int2str(de.index2Value(i)); 
}
```

## <a name="method-label"></a>メソッド label

列挙値のラベル テキストを返します。

```xpp
public str label()
```

### <a name="return-value---label"></a>戻り値 - label

列挙型の名前。列挙の型ラベルがない場合は、空の文字列。

## <a name="method-labeldefined"></a>メソッド labelDefined

この列挙型に対する label プロパティの値を返します。

```xpp
public str labelDefined()
```

### <a name="return-value---labeldefined"></a>戻り値 - labelDefined

この列挙型に対する label プロパティの値。

## <a name="method-name"></a>メソッド名

列挙型の名前を返します。

```xpp
public str name()
```

### <a name="return-value---name"></a>戻り値 - name

列挙型の名前。

## <a name="method-name2value"></a>メソッド name2Value

ラベルにより参照される項目の列挙値を返します。

```xpp
public int name2Value(str name)
```

### <a name="parameters---name2value"></a>パラメーター - name2Value

名前  
列挙値が取得されている列挙型のラベル。

### <a name="return-value---name2value"></a>戻り値 - name2Value

名前の列挙値。名前が有効な列挙ラベルでない場合は 255 です。

### <a name="remarks---name2value"></a>備考 - name2Value

以前のバージョンとの下位互換性については、名前はラベルを表します。 ラべルの無い列挙項目は、DictEnum::name2Value メソッドを使用して見つけることができません。

## <a name="method-showasradio"></a>メソッド showAsRadio

列挙をコンボ ボックスではなくラジオ ボタンを使用して表示するかどうかを示す値を返します。

```xpp
public boolean showAsRadio()
```

### <a name="return-value---showasradio"></a>戻り値 - showAsRadio

列挙スタイルがオプション ボタンである場合は true。それ以外の場合は、false。

## <a name="method-symbol2value"></a>メソッド symbol2Value

シンボルまたは名前により参照される項目の列挙値を返します。

```xpp
public int symbol2Value(str name)
```

### <a name="parameters---symbol2value"></a>パラメーター - symbol2Value

名前  
列挙値が取得されている列挙体のシンボルまたは名前。

### <a name="return-value---symbol2value"></a>戻り値 - symbol2Value

名前の列挙値。名前が有効な列挙でない場合は 255 です。

## <a name="method-value2configurationkey"></a>メソッド value2ConfigurationKey

指定した列挙値のコンフィギュレーション キー ID を返します。

```xpp
public ConfigurationKeyId value2ConfigurationKey(int value)
```

### <a name="parameters---value2configurationkey"></a>パラメーター - value2ConfigurationKey

値  
コンフィギュレーション キーが取得されている列挙型の整数値。

### <a name="return-value---value2configurationkey"></a>戻り値 - value2ConfigurationKey

値のコンフィギュレーション キーがない場合または値が有効な列挙出ない場合の値のコンフィギュレーション キー ID は 0 (ゼロ)。

## <a name="method-value2countryregioncodes"></a>メソッド value2CountryRegionCodes

```xpp
public container value2CountryRegionCodes(int value)
```

### <a name="parameters---value2countryregioncodes"></a>パラメーター - value2CountryRegionCodes

値  

### <a name="return-value---value2countryregioncodes"></a>戻り値 - value2CountryRegionCodes

## <a name="method-value2label"></a>メソッド value2Label

指定された列挙値のラベルを返します。

```xpp
public str value2Label(int value)
```

### <a name="parameters---value2label"></a>パラメーター - value2Label

値  
ラベルが取得されている列挙型の整数値。

### <a name="return-value---value2label"></a>戻り値 - value2Label

値のラベル。値または値のラベルがない場合は空の文字列は有効な列挙型ではありません。

### <a name="remarks---value2label"></a>備考 - value2Label

列挙型の品目は、ラベルを挿入する必要がありません。 このメソッドを使用して、値が列挙に存在するかどうかを判断はできません。 列挙に値が存在するかどうかを確認するには、DictEnum::value2Symbol メソッドを使用します。

## <a name="method-value2name"></a>メソッド value2Name

指定された列挙値の名前を返します。

```xpp
public str value2Name(int value)
```

### <a name="parameters---value2name"></a>パラメーター - value2Name

値  
ラベルが取得されている列挙型の整数値。

### <a name="return-value---value2name"></a>戻り値 - value2Name

値の名前。値または値の名前がない場合は空の文字列は有効な列挙型ではありません。

### <a name="remarks---value2name"></a>備考 - value2Name

列挙型に値が存在するかどうかを確認するには、代わりに value2Symbol メソッドを使用します。 列挙項目にラベルを付ける必要はないため、value2Name メソッドを使用して値が列挙型にあるかどうかを判断することはできません。

## <a name="method-value2symbol"></a>メソッド value2Symbol

記号、または指定した列挙値の Name プロパティの値を返します。

```xpp
public str value2Symbol(int value)
```

### <a name="parameters---value2symbol"></a>パラメーター - value2Symbol

値  
記号が取得されている列挙型の整数値。

### <a name="return-value---value2symbol"></a>戻り値 - value2Symbol

値のシンボルまたは名前。値が有効な列挙体でない場合は空の文字列。

### <a name="remarks---value2symbol"></a>備考 - value2Symbol

列挙型の値には、記号が必要です。 このメソッドを使用すると、戻り値が空の文字列かどうかを調べることによって、列挙値が存在するかどうかを判断できます。

## <a name="method-values"></a>メソッド values

列挙型内の項目の数を返します。

```xpp
public int values()
```

### <a name="return-value---values"></a>戻り値 - values

列挙型内の項目の数。

### <a name="remarks---values"></a>備考 - values

値は一意でなければならないので、値の数は品目の数と同じです。

### <a name="examples---values"></a>例 - values

次の例は、列挙内の項目の数を取得し、その値をループ内で使用する方法を示しています。

```xpp
DictEnum de; 
int      i; 
de = new DictEnum(enumName2Id("ActionType")); 
for (i=0; i < de.values(); i++) 
{ 
    print int2str(i) + ", " + de.index2Name(i); 
}
```

## <a name="method-queryfilternames2values"></a>メソッド queryFilterNames2Values

```xpp
public static str queryFilterNames2Values(QueryFilter filter)
```

### <a name="parameters---queryfilternames2values"></a>パラメーター - queryFilterNames2Values

フィルター  

### <a name="return-value---queryfilternames2values"></a>戻り値 - queryFilterNames2Valuese

## <a name="method-queryfiltervalues2names"></a>メソッド queryFilterValues2Names

```xpp
public static str queryFilterValues2Names(QueryFilter filter)
```

### <a name="parameters---queryfiltervalues2names"></a>パラメーター - queryFilterValues2Names

フィルター  

### <a name="return-value---queryfiltervalues2names"></a>戻り値 - queryFilterValues2Names

## <a name="method-queryrangenames2values"></a>メソッド queryRangeNames2Values

```xpp
public static str queryRangeNames2Values(QueryBuildRange range)
```

### <a name="parameters---queryrangenames2values"></a>パラメーター - queryRangeNames2Values

範囲  

### <a name="return-value---queryrangenames2values"></a>戻り値 - queryRangeNames2Values

## <a name="method-queryrangevalues2names"></a>メソッド queryRangeValues2Names

```xpp
public static str queryRangeValues2Names(QueryBuildRange range)
```

### <a name="parameters---queryrangevalues2names"></a>パラメーター - queryRangeValues2Names

範囲  

### <a name="return-value---queryrangevalues2names"></a>戻り値 - queryRangeValues2Names

## <a name="method-value2id"></a>メソッド value2id

指定された値の列挙 ID を返します。

```xpp
public static int value2id(AnyType value)
```

### <a name="parameters---value2id"></a>パラメーター - value2id

値  
列挙 ID が照会されている値。 value パラメーターは、任意のタイプを指定できます。

### <a name="return-value---value2id"></a>戻り値 - value2id

値が列挙の場合は値の列挙型 ID。それ以外の場合は 0 (ゼロ) です。

### <a name="remarks---value2id"></a>備考 - value2id

value パラメーターは、任意のタイプを指定できます。

## <a name="method-new"></a>メソッド new

Object クラスの新しいインスタンスを初期化します。

```xpp
public void new(EnumId typeId)
```

### <a name="parameters---new"></a>パラメーター - new

typeId  
列挙の ID。

### <a name="remarks---new"></a>備考 - new

無効な enum ID を指定した場合は、コンストラクターは失敗しません。 ただし、DictEnum インスタンスを使用すると、実行時エラーが発生します。 EnumID 値は符号なし整数なので、常に 0 ～ 65535 の範囲であることに注意してください。

### <a name="examples---new"></a>例 - new

次の例では、DictEnum クラスのインスタンスを作成します。

```xpp
DictEnum de; 
de = new DictEnum(enumName2Id("ActionType"));
```

