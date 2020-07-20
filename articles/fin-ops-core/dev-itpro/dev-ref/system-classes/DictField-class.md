---
title: DictField クラス
description: このトピックでは、DictField クラスについて説明します。
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
ms.openlocfilehash: 97ec4e1feb50e2d92355f3e6331b0b315d2968b6
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502990"
---
# <a name="class-dictfield"></a>クラス DictField

[!include [banner](../../includes/banner.md)]

```xpp
class DictField extends Object
```

DictField クラスは、指定されたテーブルで指定したフィールドに関する情報を提供します。

## <a name="remarks"></a>備考

## <a name="examples"></a>例

次の例は、フィールドが必須かどうかを判断するために DictField クラスのインスタンスを作成する方法を示しています。

```xpp
macrolib.dictfield 
DictField df; 
int       nFlags; 
df = new DictField(tablenum(CustTable), fieldnum(CustTable, AccountNum)); 
if (df) 
{ 
    nFlags = df.flags(); 
    if (bitTest(nFlags,#DBF_MANDATORY)) 
    { 
        print ("The field is mandatory."); 
    } 
    else 
    { 
        print ("The field is not mandatory."); 
    } 
}
```

## <a name="methods"></a>メソッド

| 方法                                                                                                                | 説明                                                                                                                               |
|-----------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| public FieldId aliasFor()                                                                                             | フィールドが別のフィールドのエイリアスの場合は、エイリアス フィールドの ID を返します。                                                            |
| public Alignment alignment()                                                                                          |                                                                                                                                           |
| public boolean allowEdit()                                                                                            |                                                                                                                                           |
| public boolean allowEditOnCreate()                                                                                    |                                                                                                                                           |
| public boolean aosAuthorization()                                                                                     |                                                                                                                                           |
| public int arrayIndex()                                                                                               |                                                                                                                                           |
| public int arraySize()                                                                                                | フィールドの配列サイズを返します (つまり、基になる拡張データ型の配列サイズ)。                               |
| public Types baseType()                                                                                               | 文字列、実数、整数、日付、時刻、列挙、またはコンテナーなど、フィールドの基本型を返します。                                        |
| public ConfigurationKeyId configurationKeyId()                                                                        | フィールドのコンフィギュレーション キーの ID を返します。                                                                                    |
| public str dateTimeTimeZoneRuleFieldName(\[int arrayindex\])                                                          |                                                                                                                                           |
| public int displayHeight(\[boolean useDefaults\])                                                                     |                                                                                                                                           |
| public int displayLength(\[boolean useDefaults\])                                                                     |                                                                                                                                           |
| public EnumId enumId()                                                                                                | フィールドが列挙型に基づいている場合は列挙型の ID を返します。                                                                |
| public int flags(\[str ext\], \[Common record\])                                                                      | フィールドのプロパティを定義する整数を返します。 DBF\_MANDATORY、などのフラグ値は、DictField マクロで定義されています。 |
| public container getCountryRegionCodes()                                                                              |                                                                                                                                           |
| public FieldId getCountryRegionContextField()                                                                         |                                                                                                                                           |
| public str getPrimaryTableForSurrogateField()                                                                         |                                                                                                                                           |
| public str groupPrompt()                                                                                              | フィールドの groupPrompt 値を返します。                                                                                              |
| public str groupPromptDefined()                                                                                       | フィールドの groupPrompt プロパティの値を返します。                                                                              |
| public str help(\[int arrayIndex\], \[boolean useInterfaceLanguage\])                                                 | フィールドについて表示されるヘルプ テキストを返します。                                                                                    |
| public str helpDefined()                                                                                              | フィールドの help プロパティの値を返します。                                                                                     |
| public FieldId id()                                                                                                   | フィールドの ID を返します。                                                                                                              |
| public boolean isIgnoreEDTRelation()                                                                                  |                                                                                                                                           |
| public boolean isMonocased()                                                                                          | フィールドが monocase であるデータベースが必要とするかどうかを示す値を返します。                                                  |
| public boolean isSql()                                                                                                | フィールドが SQL データベースにあるかどうかを示す値を返します。                                                                  |
| public boolean isSurrogateForeignKey()                                                                                |                                                                                                                                           |
| public boolean isSystem()                                                                                             | フィールドがシステム フィールドかどうかを示す値を返します。                                                                       |
| public str label(\[int arrayIndex\])                                                                                  | フィールドのラベルを返します。                                                                                                          |
| public str labelDefined()                                                                                             | フィールドの label プロパティの値を返します。                                                                                    |
| public boolean mandatory()                                                                                            |                                                                                                                                           |
| public str name(\[DbBackend db\], \[int arrayindex\], \[FieldNameGenerationMode generationMode\], \[str tableAlias\]) | フィールドの名前を返します。                                                                                                            |
| public Guid origin()                                                                                                  |                                                                                                                                           |
| public str qualifiedLabel(\[int arrayIndex\])                                                                         |                                                                                                                                           |
| public str relatedTableName()                                                                                         |                                                                                                                                           |
| public str relationContext()                                                                                          |                                                                                                                                           |
| public DictRelation relationObject(\[int arrayIndex\])                                                                | フィールドが関係のある拡張データ型に基づいている場合、フィールドの DictRelation オブジェクトを返します。                           |
| public AccessType rights(\[boolean ignoreContext\])                                                                   | このフィールドに指定されている、現在のユーザーのアクセス権を返します。                                                          |
| public int stringLen()                                                                                                | フィールドの基本型が文字列の場合、フィールドの文字列サイズを返します。                                                           |
| public TableId tableid()                                                                                              | フィールドを含むテーブルの ID を返します。                                                                                      |
| public Types type()                                                                                                   | フィールドのデータ型を返します。                                                                                                       |
| public ExtendedTypeId typeId()                                                                                        | このフィールドが拡張データ型に基づいている場合は、拡張データ型の ID を返します。                                                  |
| public boolean visible()                                                                                              |                                                                                                                                           |
| public void setLookupMode(boolean lookupMode)                                                                         |                                                                                                                                           |
| public void setSFKAutoAuthorizationMode(boolean sfkMode)                                                              |                                                                                                                                           |
| public void new(TableId tableId, FieldId fieldId, \[int arrayIndex\])                                                 | Object クラスの新しいインスタンスを初期化します。                                                                                           |

## <a name="method-aliasfor"></a>メソッド aliasFor

フィールドが別のフィールドのエイリアスの場合は、エイリアス フィールドの ID を返します。

```xpp
public FieldId aliasFor()
```

### <a name="return-value---aliasfor"></a>戻り値 - aliasFor

フィールドのエイリアス フィールドの ID。フィールドが別のフィールドのエイリアスでない場合は 0 (ゼロ)。

### <a name="remarks---aliasfor"></a>備考 - aliasFor

ユーザーがデータをフィールドに入力すると、そのテーブルの validateField メソッドが呼び出されます。 validateField メソッドが値に対する参照を実行することができない場合、エイリアスが存在するかどうかを確認します。 エイリアス フィールドが存在する場合、validateField メソッドでは、エイリアス フィールドで検索を実行します。

### <a name="examples---aliasfor"></a>例 - aliasFor

次の例は、フィールドのエイリアス フィールドの取得を示しています。

```xpp
DictField df; 
fieldId   fId; 
df = new DictField(tablenum(CustTable), fieldnum(CustTable, AccountNum));
if (df) 
{ 
    fId = df.aliasFor(); 
    if (0 != fId) 
    { 
        print (strfmt("Field alias: %1", fieldid2name(tablenum(CustTable), fId))); 
    } 
}
```

## <a name="method-alignment"></a>メソッド alignment

```xpp
public Alignment alignment()
```

### <a name="return-value---alignment"></a>戻り値 - alignment

## <a name="method-allowedit"></a>メソッド allowEdit

```xpp
public boolean allowEdit()
```

### <a name="return-value---allowedit"></a>戻り値 - allowEdit

## <a name="method-alloweditoncreate"></a>メソッド allowEditOnCreate

```xpp
public boolean allowEditOnCreate()
```

### <a name="return-value---alloweditoncreate"></a>戻り値 - allowEditOnCreate

## <a name="method-aosauthorization"></a>メソッド aosAuthorization

```xpp
public boolean aosAuthorization()
```

### <a name="return-value---aosauthorization"></a>戻り値 - aosAuthorization

## <a name="method-arrayindex"></a>メソッド arrayIndex

```xpp
public int arrayIndex()
```

### <a name="return-value---arrayindex"></a>戻り値 - arrayIndex

## <a name="method-arraysize"></a>メソッド arraySize

フィールドの配列サイズを返します (つまり、基になる拡張データ型の配列サイズ)。

```xpp
public int arraySize()
```

### <a name="return-value---arraysize"></a>戻り値 - arraySize

フィールドの配列サイズ。このフィールドが配列ではない場合は 1 です。

### <a name="examples---arraysize"></a>例 - arraySize

次の例は、フィールドの配列サイズの取得を示しています。

```xpp
DictField df; 
Types     t; 
df = new DictField(tablenum(CustTable), fieldnum(CustTable, AccountNum));  
if (df) 
{ 
    print strfmt("The arraySize is %1.", df.arraySize()); 
}
```

## <a name="method-basetype"></a>メソッド baseType

文字列、実数、整数、日付、時刻、列挙、またはコンテナーなど、フィールドの基本型を返します。

```xpp
public Types baseType()
```

### <a name="return-value---basetype"></a>戻り値 - baseType

フィールドのタイプを指定するタイプ値。

### <a name="examples---basetype"></a>例 - baseType

次の例は、フィールドの基準タイプの取得を示しています。

```xpp
DictField df;
df = new DictField(tablenum(CustTable), fieldnum(CustTable, AccountNum)); 
if (df)
{
    print strfmt("The field type is %1.", df.baseType());
}
```

## <a name="method-configurationkeyid"></a>メソッド configurationKeyId

フィールドのコンフィギュレーション キーの ID を返します。

```xpp
public ConfigurationKeyId configurationKeyId()
```

### <a name="return-value---configurationkeyid"></a>戻り値 - configurationKeyId

フィールドのコンフィギュレーション キーの ID。フィールドのコンフィギュレーション キーがない場合は 0 (ゼロ)。

### <a name="examples---configurationkeyid"></a>例 - configurationKeyId

次の例は、フィールドのコンフィギュレーション キー ID とコンフィギュレーション キー名の取得を示しています。

```xpp
DictField df; 
configurationKeyId cki; 
DictConfigurationKey dck; 
df = new DictField(tablenum(BankAccountTable), fieldnum(BankAccountTable, CustPaymFeePost)); 
if (df) 
{ 
    cki = df.configurationKeyId(); 
    //    print df.helpDefined(); 
    if (0 != cki) 
    { 
        dck = new DictConfigurationKey(cki); 
        if (dck) 
        print strfmt("The configuration key is %1.", dck.name()); 
    } 
    else 
    { 
        print "No configuration key"; 
    } 
}
```

## <a name="method-datetimetimezonerulefieldname"></a>メソッド dateTimeTimeZoneRuleFieldName

```xpp
public str dateTimeTimeZoneRuleFieldName([int arrayindex])
```

### <a name="parameters---datetimetimezonerulefieldname"></a>パラメーター - dateTimeTimeZoneRuleFieldName

arrayindex  

### <a name="return-value---datetimetimezonerulefieldname"></a>戻り値 - dateTimeTimeZoneRuleFieldName

## <a name="method-displayheight"></a>メソッド displayHeight

```xpp
public int displayHeight([boolean useDefaults])
```

### <a name="parameters---displayheight"></a>パラメーター - displayHeight

useDefaults  

### <a name="return-value---displayheight"></a>戻り値 - displayHeight

## <a name="method-displaylength"></a>メソッド displayLength

```xpp
public int displayLength([boolean useDefaults])
```

### <a name="parameters---displaylength"></a>パラメーター - displayLength

useDefaults  

### <a name="return-value---displaylength"></a>戻り値 - displayLength

## <a name="method-enumid"></a>メソッド enumId

フィールドが列挙型に基づいている場合は列挙型の ID を返します。

```xpp
public EnumId enumId()
```

### <a name="return-value---enumid"></a>戻り値 - enumId

フィールドが列挙型に基づいている場合は列挙型 ID。それ以外の場合は 0 (ゼロ) です。

### <a name="examples---enumid"></a>例 - enumId

次の例は、列挙型 ID と列挙型に基づくフィールドの列挙型名の取得を示しています。

```xpp
DictField df; 
DictEnum  de; 
enumId    id; 
df = new DictField(tablenum(CustTable), fieldnum(CustTable, AccountNum)); 
if (df) 
{ 
    id = df.enumId(); 
    if (0 != id) 
    { 
        de = new DictEnum(id); 
        if (de) 
        { 
            print de.name(); 
        } 
    } 
}
```

## <a name="method-flags"></a>メソッド flags

フィールドのプロパティを定義する整数を返します。 DBF\_MANDATORY、などのフラグ値は、DictField マクロで定義されています。

```xpp
public int flags([str ext], [Common record])
```

### <a name="parameters---flags"></a>パラメーター - flags

ext  

<!-- -->

記録  

### <a name="return-value---flags"></a>戻り値 - flags

各ビットが、フィールド フラグに対応している整数値。

### <a name="remarks---flags"></a>備考 - flags

Global::bitTest メソッドまたは & 演算子を使用して、個々のフラグ値を確認します。

### <a name="examples---flags"></a>例 - flags

次の例は、フィールドが必須かどうかを判断するためにフィールドのフラグを取得する方法を示しています。

```xpp
macrolib.dictfield 
DictField df; 
int       nFlags; 
df = new DictField(tablenum(CustTable), fieldnum(CustTable, AccountNum)); 
if (df) 
{ 
    nFlags = df.flags(); 
    if (bitTest(nFlags,#DBF_MANDATORY)) 
    { 
        print ("The field is mandatory."); 
    } 
    else 
    { 
        print ("The field is not mandatory."); 
    } 
}
```

## <a name="method-getcountryregioncodes"></a>メソッド getCountryRegionCodes

```xpp
public container getCountryRegionCodes()
```

### <a name="return-value---getcountryregioncodes"></a>戻り値 - getCountryRegionCodes

## <a name="method-getcountryregioncontextfield"></a>メソッド getCountryRegionContextField

```xpp
public FieldId getCountryRegionContextField()
```

### <a name="return-value---getcountryregioncontextfield"></a>戻り値 - getCountryRegionContextField

## <a name="method-getprimarytableforsurrogatefield"></a>メソッド getPrimaryTableForSurrogateField

```xpp
public str getPrimaryTableForSurrogateField()
```

### <a name="return-value---getprimarytableforsurrogatefield"></a>戻り値 - getPrimaryTableForSurrogateField

## <a name="method-groupprompt"></a>メソッド groupPrompt

フィールドの groupPrompt 値を返します。

```xpp
public str groupPrompt()
```

### <a name="return-value---groupprompt"></a>戻り値 - groupPrompt

フィールドの groupPrompt 値。

## <a name="method-grouppromptdefined"></a>メソッド groupPromptDefined

フィールドの groupPrompt プロパティの値を返します。

```xpp
public str groupPromptDefined()
```

### <a name="return-value---grouppromptdefined"></a>戻り値 - groupPromptDefined

テーブルに対する groupPrompt プロパティの値。

## <a name="method-help"></a>メソッド help

フィールドについて表示されるヘルプ テキストを返します。

```xpp
public str help([int arrayIndex], [boolean useInterfaceLanguage])
```

### <a name="parameters---help"></a>パラメーター - help

arrayIndex  
ヘルプ テキストにユーザー インターフェイス言語を使用するかどうかを示すブール値; オプション。

<!-- -->

useInterfaceLanguage  
ヘルプ テキストにユーザー インターフェイス言語を使用するかどうかを示すブール値; オプション。

### <a name="return-value---help"></a>戻り値 - help

ヘルプ テキストまたはフィールドの継承されたヘルプ テキスト。

### <a name="remarks---help"></a>備考 - help

フィールドのヘルプ テキストが定義されていない場合、該当する場合に、このメソッドはフィールドに使用される、拡張データ型のヘルプ テキストを返します。 配列のエントリが指定されている場合、このメソッドは、配列要素のヘルプ テキストを返します。

### <a name="examples---help"></a>例 - help

次の例は、フィールドのヘルプ テキストの取得を示しています。

```xpp
DictField df; 
df = new DictField(tablenum(CustTable), fieldnum(CustTable, AccountNum)); 
if (df) 
{ 
    print df.help(); 
}
```

## <a name="method-helpdefined"></a>メソッド helpDefined

フィールドの help プロパティの値を返します。

```xpp
public str helpDefined()
```

### <a name="return-value---helpdefined"></a>戻り値 - helpDefined

フィールドに対する help プロパティの値。

### <a name="remarks---helpdefined"></a>備考 - helpDefined

ヘルプ メソッドとは異なり、フィールドが拡張データ型に基づいていて、ヘルプ テキストが定義されていない場合、helpDefined メソッドは拡張データ型のヘルプ テキストを返しません。

### <a name="examples---helpdefined"></a>例 - helpDefined

次の例は、フィールドの定義済ヘルプ テキストの取得を示しています。

```xpp
DictField df; 
df = new DictField(tablenum(CustTable), fieldnum(CustTable, AccountNum)); 
if (df) 
{ 
    print df.helpDefined(); 
}
```

## <a name="method-id"></a>メソッド id

フィールドの ID を返します。

```xpp
public FieldId id()
```

### <a name="return-value---id"></a>戻り値 - id

フィールドの ID。

### <a name="examples---id"></a>例 - id

次の例では、フィールドの ID を取得します。

```xpp
DictField df; 
df = new DictField(tablenum(CustTable), fieldnum(CustTable, AccountNum)); 
if (df) 
{ 
    print df.id(); 
}
```

## <a name="method-isignoreedtrelation"></a>メソッド isIgnoreEDTRelation

```xpp
public boolean isIgnoreEDTRelation()
```

### <a name="return-value---isignoreedtrelation"></a>戻り値 - isIgnoreEDTRelation

## <a name="method-ismonocased"></a>メソッド isMonocased

フィールドが monocase であるデータベースが必要とするかどうかを示す値を返します。

```xpp
public boolean isMonocased()
```

### <a name="return-value---ismonocased"></a>戻り値 - isMonocased

フィールドが monocase である場合は true。それ以外の場合は、false。

## <a name="method-issql"></a>メソッド isSql

フィールドが SQL データベースにあるかどうかを示す値を返します。

```xpp
public boolean isSql()
```

### <a name="return-value---issql"></a>戻り値 - isSql

フィールドが SQL データベースである場合は true。それ以外の場合は、false。

### <a name="examples---issql"></a>例 - isSql

次の例では、フィールドが SQL データベースにあるかどうかを判断します。

```xpp
    DictField df; 
    df = new DictField(tablenum(CustTable), fieldnum(CustTable, AccountNum)); 
    if (df) 
    { 
    if (df.isSql()) 
    { 
        print ("Field is in SQL database"); 
    } 
    else 
    { 
        print ("Field is not in SQL database"); 
    } 
    }
```

## <a name="method-issurrogateforeignkey"></a>メソッド isSurrogateForeignKey

```xpp
public boolean isSurrogateForeignKey()
```

### <a name="return-value---issurrogateforeignkey"></a>戻り値 - isSurrogateForeignKey

## <a name="method-issystem"></a>メソッド isSystem

フィールドがシステム フィールドかどうかを示す値を返します。

```xpp
public boolean isSystem()
```

### <a name="return-value---issystem"></a>戻り値 - isSystem

フィールドがシステム フィールドである場合は true。それ以外の場合は、false。

## <a name="method-label"></a>メソッド label

フィールドのラベルを返します。

```xpp
public str label([int arrayIndex])
```

### <a name="parameters---label"></a>パラメーター - label

arrayIndex  

### <a name="return-value---label"></a>戻り値 - label

フィールドのラベルまたは継承されたラベル値。

### <a name="remarks---label"></a>備考 - label

フィールドのラベルが指定されていない場合、該当する場合に、このメソッドはフィールドに使用される、拡張データ型のラベルを返します。 配列のエントリが指定されている場合、このメソッドは、配列要素のラベルを返します。

## <a name="method-labeldefined"></a>メソッド labelDefined

フィールドの label プロパティの値を返します。

```xpp
public str labelDefined()
```

### <a name="return-value---labeldefined"></a>戻り値 - labelDefined

テーブルの label プロパティの値。テーブルのラベル テキストがない場合は空の文字列。

### <a name="remarks---labeldefined"></a>備考 - labelDefined

label メソッドとは異なり、フィールドが拡張データ型に基づいていて、ラベルが定義されていない場合、labelDefined メソッドは拡張データ型のラベルを返しません。

### <a name="examples---labeldefined"></a>例 - labelDefined

次の例は、フィールドの定義済ラベルの取得を示しています。

```xpp
DictField df; 
df = new DictField(tablenum(CustTable), fieldnum(CustTable, AccountNum)); 
if (df) 
{ 
    print df.labelDefined(); 
}
```

## <a name="method-mandatory"></a>メソッド mandatory

```xpp
public boolean mandatory()
```

### <a name="return-value---mandatory"></a>戻り値 - mandatory

## <a name="method-name"></a>メソッド名

フィールドの名前を返します。

```xpp
public str name([DbBackend db], [int arrayindex], [FieldNameGenerationMode generationMode], [str tableAlias])
```

### <a name="parameters---name"></a>パラメーター - 名前

db  
テーブルのエイリアス (省略可能)。

<!-- -->

arrayindex  
テーブルのエイリアス (省略可能)。

<!-- -->

generationMode  
テーブルのエイリアス (省略可能)。

<!-- -->

tableAlias  
テーブルのエイリアス (省略可能)。

### <a name="return-value---name"></a>戻り値 - name

フィールドの名前。

### <a name="examples---name"></a>例 - 名前

次の例は、フィールドの名前の取得を示しています。

```xpp
DictField df; 
df = new DictField(tablenum(CustTable), fieldnum(CustTable, AccountNum)); 
if (df) 
{ 
    print df.name(); 
}
```

## <a name="method-origin"></a>メソッド origin

```xpp
public Guid origin()
```

### <a name="return-value---origin"></a>戻り値 - origin

## <a name="method-qualifiedlabel"></a>メソッド qualifiedLabel

```xpp
public str qualifiedLabel([int arrayIndex])
```

### <a name="parameters---qualifiedlabel"></a>パラメーター - qualifiedLabel

arrayIndex  

### <a name="return-value---qualifiedlabel"></a>戻り値 - qualifiedLabel

## <a name="method-relatedtablename"></a>メソッド relatedTableName

```xpp
public str relatedTableName()
```

### <a name="return-value---relatedtablename"></a>戻り値 - relatedTableName

## <a name="method-relationcontext"></a>メソッド relationContext

```xpp
public str relationContext()
```

### <a name="return-value---relationcontext"></a>戻り値 - relationContext

## <a name="method-relationobject"></a>メソッド relationObject

フィールドが関係のある拡張データ型に基づいている場合、フィールドの DictRelation オブジェクトを返します。

```xpp
public DictRelation relationObject([int arrayIndex])
```

### <a name="parameters---relationobject"></a>パラメーター - relationObject

arrayIndex  

### <a name="return-value---relationobject"></a>戻り値 - relationObject

フィールドの関係を表す DictRelation オブジェクト。フィールドに関係が定義されていない場合、またはフィールドが拡張データ型に基づいていない場合は null、Nothing、nullptr、unit、null 参照 (Visual Basic では Nothing)。

## <a name="method-rights"></a>メソッド rights

このフィールドに指定されている、現在のユーザーのアクセス権を返します。

```xpp
public AccessType rights([boolean ignoreContext])
```

### <a name="parameters---rights"></a>パラメーター - rights

ignoreContext  

### <a name="return-value---rights"></a>戻り値 - rights

このフィールドに指定されている、現在のユーザーのアクセス権。

### <a name="remarks---rights"></a>備考 - rights

これは、AccessType 列挙型の値の 1 つです。

## <a name="method-stringlen"></a>メソッド stringLen

フィールドの基本型が文字列の場合、フィールドの文字列サイズを返します。

```xpp
public int stringLen()
```

### <a name="return-value---stringlen"></a>戻り値 - stringLen

フィールドの基本型が文字列の場合、フィールドの文字列サイズ。それ以外の場合は 0 (ゼロ) です。

### <a name="examples---stringlen"></a>例 - stringLen

次の例は、フィールドの文字列の長さを取得する方法を示しています。

```xpp
DictField df; 
df = new DictField(tablenum(CustTable), fieldnum(CustTable, AccountNum)); 
if (df) 
{ 
    print strfmt("The string length is %1.", df.stringLen()); 
}
```

## <a name="method-tableid"></a>メソッド tableid

フィールドを含むテーブルの ID を返します。

```xpp
public TableId tableid()
```

### <a name="return-value---tableid"></a>戻り値 - tableid

フィールドを含むテーブルの ID。

### <a name="examples---tableid"></a>例 - tableid

次の例は、フィールドのテーブル ID の取得を示しています。

```xpp
DictField df; 
df = new DictField(tablenum(CustTable), fieldnum(CustTable, AccountNum)); 
if (df) 
{ 
    print df.tableid(); 
}
```

## <a name="method-type"></a>メソッドのタイプ

フィールドのデータ型を返します。

```xpp
public Types type()
```

### <a name="return-value---type"></a>戻り値 - type

フィールドのタイプを指定するタイプ値。

### <a name="remarks---type"></a>備考 - タイプ

このフィールドが拡張データ型に基づいている場合は、このメソッドの戻り値として Types::UserType が返されます。

### <a name="examples---type"></a>例 - タイプ

次の例は、フィールドのタイプの取得を示しています。

```xpp
DictField df; 
df = new DictField(tablenum(CustTable), fieldnum(CustTable, AccountNum)); 
if (df) 
{ 
    print df.type(); 
}
```

## <a name="method-typeid"></a>メソッド typeId

このフィールドが拡張データ型に基づいている場合は、拡張データ型の ID を返します。

```xpp
public ExtendedTypeId typeId()
```

### <a name="return-value---typeid"></a>戻り値 - typeId

フィールドが拡張データ型に基づいている場合は、拡張データ型の ID。それ以外の場合は 0 (ゼロ)。

### <a name="examples---typeid"></a>例 - typeId

次の例は、フィールドの拡張データ型 ID の取得を示しています。

```xpp
DictField df; 
extendedTypeId eti; 
DictType  dt; 
df = new DictField(tablenum(CustTable), fieldnum(CustTable, AccountNum)); 
if (df) 
{ 
   eti = df.typeId(); 
   if (0 != eti) 
   { 
        dt = new DictType(eti); 
        if (dt) 
        { 
            print strfmt("The field is based on %1.", dt.name()); 
        } 
   } 
   else 
   { 
        print "The field is not based on an extended data type."; 
   } 
}
```

## <a name="method-visible"></a>メソッド visible

```xpp
public boolean visible()
```

### <a name="return-value---visible"></a>戻り値 - visible

## <a name="method-setlookupmode"></a>メソッド setLookupMode

```xpp
public void setLookupMode(boolean lookupMode)
```

### <a name="parameters---setlookupmode"></a>パラメーター - setLookupMode

lookupMode  

## <a name="method-setsfkautoauthorizationmode"></a>メソッド setSFKAutoAuthorizationMode

```xpp
public void setSFKAutoAuthorizationMode(boolean sfkMode)
```

### <a name="parameters---setsfkautoauthorizationmode"></a>パラメーター - setSFKAutoAuthorizationMode

sfkMode  

## <a name="method-new"></a>メソッド new

Object クラスの新しいインスタンスを初期化します。

```xpp
public void new(TableId tableId, FieldId fieldId, [int arrayIndex])
```

### <a name="parameters---new"></a>パラメーター - new

tableId  

<!-- -->

fieldId  

<!-- -->

arrayIndex  

### <a name="examples---new"></a>例 - new

次の例は、DictField クラスのインスタンスを作成する方法を示しています。

```xpp
DictField df; 
df = new DictField(tablenum(CustTable), fieldnum(CustTable, AccountNum)); 
// Check df for successful creation before proceeding. 
if (!df) 
{ 
// Take error action. 
}
```

