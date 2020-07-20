---
title: FormDataObject クラス
description: このトピックでは、FormDataObject クラスについて説明します。
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
ms.openlocfilehash: f719f470dd0076723e1eb0e5a23413ea914fb2b4
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502631"
---
# <a name="class-formdataobject"></a>クラス FormDataObject

[!include [banner](../../includes/banner.md)]


```xpp
class FormDataObject extends FormObject
```

FormDataObject クラスは、フィールドを表しており、フィールドを参照するコントロールがフォーム データ ソースに表示される方法に影響を与えて、ルックアップと検証の動作を変更します。

## <a name="remarks"></a>備考

プロパティを変更すると、フィールドを参照するコントロールの表示方法に影響します。 さらに、このクラスでメソッドを上書きした場合、ルックアップと検証での動作を変更できます。 個々のコントロールのプロパティの代わりに FormDataObject クラスのプロパティを使用することにより、同じフィールドのさまざまな表現が一貫して処理されることを確認します。 これにより、アップグレードも容易になります。

## <a name="examples"></a>例

## <a name="methods"></a>メソッド

| 方法                                                                                                      | 説明                                                                                                                                                             |
|-------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| public Common lookupReference(\[FormReferenceControl formReferenceControl\])                                |                                                                                                                                                                         |
| public Common resolveReference(\[FormReferenceControl formReferenceControl\])                               |                                                                                                                                                                         |
| public str resolveAmbiguousReference(\[FormControl formControl\])                                           |                                                                                                                                                                         |
| public int allowAdd(\[int value\])                                                                          | フォーム データ オブジェクトの allowAdd プロパティの値を設定するか返します。                                                                                            |
| public boolean allowEdit(\[boolean value\])                                                                 | ユーザーがコントロールの内容を修正できるかどうかを決定します。                                                                                                     |
| public FieldId dataField(\[FieldId value\])                                                                 |                                                                                                                                                                         |
| public FormDataSource datasource()                                                                          |                                                                                                                                                                         |
| public boolean editAutoPostback(\[boolean value\])                                                          |                                                                                                                                                                         |
| public boolean enabled(\[boolean value\])                                                                   | オブジェクトが有効か無効かを決定します。                                                                                                                   |
| public FieldId fieldId()                                                                                    |                                                                                                                                                                         |
| public str helpField()                                                                                      | コントロールのヘルプ テキストを返します。                                                                                                                                  |
| public str labelText()                                                                                      | コントロールのラベル テキストを返します。                                                                                                                                 |
| public boolean mandatory(\[boolean value\])                                                                 | データ フィールドが必須であるかどうかを示す値を設定するか返します。                                                                                             |
| public boolean skip(\[boolean value\])                                                                      | ユーザーが Tab キーを押して、データ ソースに関連付けられたコントロールに移動するときにコントロールがスキップされるかどうかを示す値を設定するか返します。 |
| public str toolTip()                                                                                        |                                                                                                                                                                         |
| public boolean validate()                                                                                   |                                                                                                                                                                         |
| public boolean visible(\[boolean value\])                                                                   | コントロールが表示されるかどうかを示す値を設定するか返します。                                                                                                  |
| private void OnModified(\[FormDataObject sender\], \[FormDataFieldEventArgs e\])                            |                                                                                                                                                                         |
| private void OnValidated(\[FormDataObject sender\], \[FormDataFieldEventArgs e\])                           |                                                                                                                                                                         |
| public void modified()                                                                                      | フィールドが正常に検証され、現在のレコードで変更されたことを示します。                                                                            |
| private void OnValidating(\[FormDataObject sender\], \[FormDataFieldEventArgs e\])                          |                                                                                                                                                                         |
| public void registerOverrideMethod(str methodToOverride, str objectMethodToCall, \[Object overrideObject\]) |                                                                                                                                                                         |
| public void restore()                                                                                       |                                                                                                                                                                         |
| public void lookup(FormControl formControl, str filterStr)                                                  |                                                                                                                                                                         |
| public void dataChanged()                                                                                   |                                                                                                                                                                         |
| public void jumpRef()                                                                                       |                                                                                                                                                                         |
| public void context()                                                                                       |                                                                                                                                                                         |
| public void find()                                                                                          |                                                                                                                                                                         |
| public void filter(\[str filterStr\], \[NoYes clearPrev\])                                                  |                                                                                                                                                                         |
| public void performFormLookup(xFormRun form, FormControl formControl)                                       |                                                                                                                                                                         |

## <a name="method-lookupreference"></a>メソッド lookupReference

```xpp
public Common lookupReference([FormReferenceControl formReferenceControl])
```

### <a name="parameters---lookupreference"></a>パラメーター - lookupReference

formReferenceControl  

### <a name="return-value---lookupreference"></a>戻り値 - lookupReference

## <a name="method-resolvereference"></a>メソッド resolveReference

```xpp
public Common resolveReference([FormReferenceControl formReferenceControl])
```

### <a name="parameters---resolvereference"></a>パラメーター - resolveReference

formReferenceControl  

### <a name="return-value---resolvereference"></a>戻り値 - resolveReference

## <a name="method-resolveambiguousreference"></a>メソッド resolveAmbiguousReference

```xpp
public str resolveAmbiguousReference([FormControl formControl])
```

### <a name="parameters---resolveambiguousreference"></a>パラメーター - resolveAmbiguousReference

formControl  

### <a name="return-value---resolveambiguousreference"></a>戻り値 - resolveAmbiguousReference

## <a name="method-allowadd"></a>メソッド allowAdd

フォーム データ オブジェクトの allowAdd プロパティの値を設定するか返します。

```xpp
public int allowAdd([int value])
```

### <a name="parameters---allowadd"></a>パラメーター - allowAdd

値  
allowEdit プロパティに割り当てる値。

### <a name="return-value---allowadd"></a>戻り値 - allowAdd

allowAdd プロパティが No、Restricted もしくは Yes に設定されているかどうかを示す FormAllowAdd 列挙値。

### <a name="examples---allowadd"></a>例 - allowAdd

次の例は、allowAdd プロパティを取得および設定する方法を示しています。

```xpp
// fdo previously assigned to a FormDataObject object. 
// Retrieve the allowAdd property. 
nAllowAdd = fdo.allowAdd(); 
// Set the allowAdd property. 
fdo.allowAdd(FormAllowAdd::Restricted);
```

## <a name="method-allowedit"></a>メソッド allowEdit

ユーザーがコントロールの内容を修正できるかどうかを決定します。

```xpp
public boolean allowEdit([boolean value])
```

### <a name="parameters---allowedit"></a>パラメーター - allowEdit

値  
allowEdit プロパティに割り当てる値。

### <a name="return-value---allowedit"></a>戻り値 - allowEdit

コントロールを変更することができる場合は true。それ以外の場合は、false。

### <a name="remarks---allowedit"></a>備考 - allowEdit

コンテナー コントロールにこのプロパティが設定されると、コンテナー内のすべてのコントロールの変更は無効または有効になります。

### <a name="examples---allowedit"></a>例 - allowEdit

次の例は、allowEdit プロパティの値を取得および設定する方法を示しています。

```xpp
// Return the value. 
info (strfmt("allowEdit: %1", this.allowEdit())); 
// Set the value. 
this.allowEdit(false);
```

## <a name="method-datafield"></a>メソッド dataField

```xpp
public FieldId dataField([FieldId value])
```

### <a name="parameters---datafield"></a>パラメーター - dataField

値  

### <a name="return-value---datafield"></a>戻り値 - dataField

## <a name="method-datasource"></a>メソッド datasource

```xpp
public FormDataSource datasource()
```

### <a name="return-value---datasource"></a>戻り値 - datasource

## <a name="method-editautopostback"></a>メソッド editAutoPostback

```xpp
public boolean editAutoPostback([boolean value])
```

### <a name="parameters---editautopostback"></a>パラメーター - editAutoPostback

値  

### <a name="return-value---editautopostback"></a>戻り値 - editAutoPostback

## <a name="method-enabled"></a>メソッド enabled

オブジェクトが有効か無効かを決定します。

```xpp
public boolean enabled([boolean value])
```

### <a name="parameters---enabled"></a>パラメーター - enabled

値  
コントロールが有効かどうかを指定するブール値; オプション。

### <a name="return-value---enabled"></a>戻り値 - enabled

オブジェクトが有効である場合は true。それ以外の場合は、false。

### <a name="remarks---enabled"></a>備考 - enabled

有効になっているプロパティを使用すると、実行時にコントロールを有効または無効にできます。 たとえば、アプリケーションの現在の状態には適用されないオブジェクトを無効にすることができます。 また、読み取り専用情報を提供するエラー メッセージなど、表示のためにのみ使用されるコントロールを無効にすることもできます。

### <a name="examples---enabled"></a>例 - enabled

次の例は、コントロールの有効なプロパティを取得および設定する方法を示しています。

```xpp
// Return the value of the enabled property. 
info(strfmt("enabled: %1", this.enabled())); 
// Set the enabled property. 
this.enabled(false);
```

## <a name="method-fieldid"></a>メソッド fieldId

```xpp
public FieldId fieldId()
```

### <a name="return-value---fieldid"></a>戻り値 - fieldId

## <a name="method-helpfield"></a>メソッド helpField

コントロールのヘルプ テキストを返します。

```xpp
public str helpField()
```

### <a name="return-value---helpfield"></a>戻り値 - helpField

コントロールのヘルプ テキスト。コントロールにヘルプ テキストがない場合は空の文字列。

### <a name="examples---helpfield"></a>例 - helpField

次の例は、helpField メソッドの使用方法を示しています。

```xpp
str strHelp; 
strHelp = this.helpField();
```

## <a name="method-labeltext"></a>メソッド labelText

コントロールのラベル テキストを返します。

```xpp
public str labelText()
```

### <a name="return-value---labeltext"></a>戻り値 - labelText

コントロールのラベル テキスト。コントロールにラベル テキストがない場合は空の文字列。

## <a name="method-mandatory"></a>メソッド mandatory

データ フィールドが必須であるかどうかを示す値を設定するか返します。

```xpp
public boolean mandatory([boolean value])
```

### <a name="parameters---mandatory"></a>パラメーター - mandatory

値  
フィールドの必須プロパティに割り当てる値。

### <a name="return-value---mandatory"></a>戻り値 - mandatory

フィールドが必須項目である場合は true。それ以外の場合は、false。

### <a name="examples---mandatory"></a>例 - mandatory

次の例は、フィールドの必須プロパティを取得および設定する方法を示しています。

```xpp
// Return the value of the mandatory property. 
info (strfmt("mandatory: %1", fdo.mandatory())); 
// Set the value of the mandatory property. 
fdo.mandatory(false);
```

## <a name="method-skip"></a>メソッド skip

ユーザーが Tab キーを押して、データ ソースに関連付けられたコントロールに移動するときにコントロールがスキップされるかどうかを示す値を設定するか返します。

```xpp
public boolean skip([boolean value])
```

### <a name="parameters---skip"></a>パラメーター - skip

値  
コントロールに関連付けられているデータ ソースの skip プロパティに割り当てる値 (オプション)。

### <a name="return-value---skip"></a>戻り値 - skip

データ ソースに関連付けられているコントロールに移動するためユーザーが TAB キーを押すと、コントロールがスキップされる場合は true。それ以外の場合は、false。

### <a name="remarks---skip"></a>備考 - skip

有効なプロパティが true であり、allowEdit プロパティが false であり、省略プロパティが true の場合は、ユーザーは、コントロールの内容を変更することはできませんが、コントロールの内容をコピーもできます。 コントロールのスキップ値が true またはデータ ソースのスキップ値が true の場合、コントロールはスキップされます。

### <a name="examples---skip"></a>例 - skip

以下は、コントロールのデータ ソースのスキップ プロパティを取得および設定する方法を示しています。

```xpp
// Return the value of the skip property. 
info(strfmt("skip: %1", this.skip())); 
// Set the value of the skip property. 
this.skip(true);
```

## <a name="method-tooltip"></a>メソッド toolTip

```xpp
public str toolTip()
```

### <a name="return-value---tooltip"></a>戻り値 - toolTip

## <a name="method-validate"></a>メソッド validate

```xpp
public boolean validate()
```

### <a name="return-value---validate"></a>戻り値 - validate

## <a name="method-visible"></a>メソッド visible

コントロールが表示されるかどうかを示す値を設定するか返します。

```xpp
public boolean visible([boolean value])
```

### <a name="parameters---visible"></a>パラメーター - visible

値  
コントロールの表示設定に割り当てられている値。

### <a name="return-value---visible"></a>戻り値 - visible

コントロールが可視である場合は true。それ以外の場合は false。 既定は true です。

### <a name="remarks---visible"></a>備考 - visible

データ ソース フィールドを参照するコントロールは、コントロールおよび基になるデータ ソース フィールドの両方で Visible プロパティが true に設定されている場合にのみ表示されます。 コントロールの代わりに、データ ソース フィールドのプロパティを設定する場合、フォーム全体で、このフィールドは一貫して処理されることが保証されます。 これにより、アップグレードが容易になります。

## <a name="method-onmodified"></a>メソッド OnModified

```xpp
private void OnModified([FormDataObject sender], [FormDataFieldEventArgs e])
```

### <a name="parameters---onmodified"></a>パラメーター - OnModified

sender  

<!-- -->

e  

## <a name="method-onvalidated"></a>メソッド OnValidated

```xpp
private void OnValidated([FormDataObject sender], [FormDataFieldEventArgs e])
```

### <a name="parameters---onvalidated"></a>パラメーター - OnValidated

sender  

<!-- -->

e  

## <a name="method-modified"></a>メソッド modified

フィールドが正常に検証され、現在のレコードで変更されたことを示します。

```xpp
public void modified()
```

### <a name="remarks---modified"></a>備考 - modified

このメソッドは、検証メソッドが true を返した場合、コントロールの変更されたメソッドから呼び出されます。 このメソッドをオーバーライドして、修正された値に基づく他の値の再計算を許可することができます。 super() メソッドの呼び出しは、テーブルの modifiedField メソッドが呼び出されることを保証します。 変更済は現在のレコードのフィールドの値が変更されたことを意味しますが、レコードが保存されるまでこの値はデータベースに書き込まれません。

## <a name="method-onvalidating"></a>メソッド OnValidating

```xpp
private void OnValidating([FormDataObject sender], [FormDataFieldEventArgs e])
```

### <a name="parameters---onvalidating"></a>パラメーター - OnValidating

sender  

<!-- -->

e  

## <a name="method-registeroverridemethod"></a>メソッド registerOverrideMethod

```xpp
public void registerOverrideMethod(str methodToOverride, str objectMethodToCall, [Object overrideObject])
```

### <a name="parameters---registeroverridemethod"></a>パラメーター - registerOverrideMethod

methodToOverride  

<!-- -->

objectMethodToCall  

<!-- -->

overrideObject  

## <a name="method-restore"></a>メソッド restore

```xpp
public void restore()
```

## <a name="method-lookup"></a>メソッド lookup

```xpp
public void lookup(FormControl formControl, str filterStr)
```

### <a name="parameters---lookup"></a>パラメーター - lookup

formControl  

<!-- -->

filterStr  

## <a name="method-datachanged"></a>メソッド dataChanged

```xpp
public void dataChanged()
```

## <a name="method-jumpref"></a>メソッド jumpRef

```xpp
public void jumpRef()
```

## <a name="method-context"></a>メソッド context

```xpp
public void context()
```

## <a name="method-find"></a>メソッド find

```xpp
public void find()
```

## <a name="method-filter"></a>メソッド filter

```xpp
public void filter([str filterStr], [NoYes clearPrev])
```

### <a name="parameters---filter"></a>パラメーター - filter

filterStr  

<!-- -->

clearPrev  

## <a name="method-performformlookup"></a>メソッド performFormLookup

```xpp
public void performFormLookup(xFormRun form, FormControl formControl)
```

### <a name="parameters---performformlookup"></a>パラメーター - performFormLookup

フォーム  

<!-- -->

formControl  

