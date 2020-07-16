---
title: FormBuildDataSource クラス
description: このトピックでは、FormBuildDataSource クラスについて説明します。
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
ms.openlocfilehash: c90d337d4b017e616e25893a1de3d7ceb542bcb7
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502969"
---
# <a name="class-formbuilddatasource"></a>クラス FormBuildDataSource

[!include [banner](../../includes/banner.md)]

```xpp
class FormBuildDataSource extends FormBuildObjectSet
```

FormBuildDataSource クラスを使用すると、X++ コードとメタデータの作成、読み取り、更新、および削除を行うことができます。

## <a name="remarks"></a>備考

この API が呼び出される前に、ユーザーが開発セキュリティ キー (SysDevelopment) にアクセスできることを確認します。

## <a name="examples"></a>例

## <a name="methods"></a>メソッド

| 方法                                                                            | 説明                                                                                                               |
|-----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| public FormBuildDataSource addReferenceDataSource(str name, \[str joinRelation\]) |                                                                                                                           |
| public boolean allowCheck(\[boolean value\])                                      |                                                                                                                           |
| public boolean allowCreate(\[boolean value\])                                     |                                                                                                                           |
| public boolean allowDeferredLoad(\[boolean value\])                               |                                                                                                                           |
| public boolean allowDelete(\[boolean value\])                                     |                                                                                                                           |
| public boolean allowEdit(\[boolean value\])                                       | ユーザーがコントロールの内容を変更できるかどうかを決定します。                                                       |
| public boolean autoNotify(\[boolean value\])                                      |                                                                                                                           |
| public boolean autoQuery(\[boolean value\])                                       |                                                                                                                           |
| public boolean autoSearch(\[boolean value\])                                      |                                                                                                                           |
| public FormBuildDataSource baseDataSource()                                       |                                                                                                                           |
| public str company(\[str value\])                                                 |                                                                                                                           |
| public FieldId counterField(\[FieldId value\])                                    |                                                                                                                           |
| public boolean crossCompanyAutoQuery(\[boolean value\])                           |                                                                                                                           |
| public boolean delayActive(\[boolean value\])                                     |                                                                                                                           |
| public int extends(\[AnyType value\])                                             |                                                                                                                           |
| public str GetXppILImplementation()                                               |                                                                                                                           |
| public IndexId index(\[IndexId value\])                                           |                                                                                                                           |
| public boolean insertAtEnd(\[boolean value\])                                     |                                                                                                                           |
| public boolean insertIfEmpty(\[boolean value\])                                   |                                                                                                                           |
| public boolean isBaseDataSource()                                                 |                                                                                                                           |
| public boolean isInheritanceDataSource()                                          |                                                                                                                           |
| public boolean isMasterDataSource()                                               |                                                                                                                           |
| public str joinRelation(\[str value\])                                            |                                                                                                                           |
| public int joinSource(\[AnyType value\])                                          |                                                                                                                           |
| public int linkType(\[int value\])                                                |                                                                                                                           |
| public FormBuildDataSource masterDataSource()                                     |                                                                                                                           |
| public int maxAccessRight(\[int value\])                                          |                                                                                                                           |
| public int maxRecordsToLoad(\[int value\])                                        |                                                                                                                           |
| public str name(\[str value\])                                                    | フォーム、レポート、テーブル、クエリ、または別の MSDAX アプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。 |
| public boolean onlyFetchActive(\[boolean value\])                                 |                                                                                                                           |
| public int optionalRecordMode(\[int value\])                                      |                                                                                                                           |
| public int startPosition(\[int value\])                                           |                                                                                                                           |
| public TableId table(\[TableId value\])                                           | オブジェクトに関連付けられているテーブル ID を取得または設定します。                                                                     |
| public int validTimeStateAutoQuery(\[int value\])                                 |                                                                                                                           |
| public int validTimeStateUpdate(\[int value\])                                    |                                                                                                                           |
| public void RegisterXppDataFieldILImplementation(str fieldName, str className)    |                                                                                                                           |
| public void RegisterXppILImplementation(str className)                            |                                                                                                                           |
| public void SetDataLinkType(QueryDataLinkType linkType, str parentDataSource)     |                                                                                                                           |

## <a name="method-addreferencedatasource"></a>メソッド addReferenceDataSource

```xpp
public FormBuildDataSource addReferenceDataSource(str name, [str joinRelation])
```

### <a name="parameters---addreferencedatasource"></a>パラメーター - addReferenceDataSource

名前  

<!-- -->

joinRelation  

### <a name="return-value---addreferencedatasource"></a>戻り値 - addReferenceDataSource

## <a name="method-allowcheck"></a>メソッド allowCheck

```xpp
public boolean allowCheck([boolean value])
```

### <a name="parameters---allowcheck"></a>パラメーター - allowCheck

値  

### <a name="return-value---allowcheck"></a>戻り値 - allowCheck

## <a name="method-allowcreate"></a>メソッド allowCreate

```xpp
public boolean allowCreate([boolean value])
```

### <a name="parameters---allowcreate"></a>パラメーター - allowCreate

値  

### <a name="return-value---allowcreate"></a>戻り値 - allowCreate

## <a name="method-allowdeferredload"></a>メソッド allowDeferredLoad

```xpp
public boolean allowDeferredLoad([boolean value])
```

### <a name="parameters---allowdeferredload"></a>パラメーター - allowDeferredLoad

値  

### <a name="return-value---allowdeferredload"></a>戻り値 - allowDeferredLoad

## <a name="method-allowdelete"></a>メソッド allowDelete

```xpp
public boolean allowDelete([boolean value])
```

### <a name="parameters---allowdelete"></a>パラメーター - allowDelete

値  

### <a name="return-value---allowdelete"></a>戻り値 - allowDelete

## <a name="method-allowedit"></a>メソッド allowEdit

ユーザーがコントロールの内容を変更できるかどうかを決定します。

```xpp
public boolean allowEdit([boolean value])
```

### <a name="parameters---allowedit"></a>パラメーター - allowEdit

値  

### <a name="return-value---allowedit"></a>戻り値 - allowEdit

コントロールを編集することができる場合は true。それ以外の場合は、false。

### <a name="remarks---allowedit"></a>備考 - allowEdit

コンテナー コントロールにこのプロパティが設定されると、コンテナー内のすべてのコントロールの変更は無効または有効になります。

## <a name="method-autonotify"></a>メソッド autoNotify

```xpp
public boolean autoNotify([boolean value])
```

### <a name="parameters---autonotify"></a>パラメーター - autoNotify

値  

### <a name="return-value---autonotify"></a>戻り値 - autoNotify

## <a name="method-autoquery"></a>メソッド autoQuery

```xpp
public boolean autoQuery([boolean value])
```

### <a name="parameters---autoquery"></a>パラメーター - autoQuery

値  

### <a name="return-value---autoquery"></a>戻り値 - autoQuery

## <a name="method-autosearch"></a>メソッド autoSearch

```xpp
public boolean autoSearch([boolean value])
```

### <a name="parameters---autosearch"></a>パラメーター - autoSearch

値  

### <a name="return-value---autosearch"></a>戻り値 - autoSearch

## <a name="method-basedatasource"></a>メソッド baseDataSource

```xpp
public FormBuildDataSource baseDataSource()
```

### <a name="return-value---basedatasource"></a>戻り値 - baseDataSource

## <a name="method-company"></a>メソッド company

```xpp
public str company([str value])
```

### <a name="parameters---company"></a>パラメーター - company

値  

### <a name="return-value---company"></a>戻り値 - company

## <a name="method-counterfield"></a>メソッド counterField

```xpp
public FieldId counterField([FieldId value])
```

### <a name="parameters---counterfield"></a>パラメーター - counterField

値  

### <a name="return-value---counterfield"></a>戻り値 - counterField

## <a name="method-crosscompanyautoquery"></a>メソッド crossCompanyAutoQuery

```xpp
public boolean crossCompanyAutoQuery([boolean value])
```

### <a name="parameters---crosscompanyautoquery"></a>パラメーター - crossCompanyAutoQuery

値  

### <a name="return-value---crosscompanyautoquery"></a>戻り値 - crossCompanyAutoQuery

## <a name="method-delayactive"></a>メソッド delayActive

```xpp
public boolean delayActive([boolean value])
```

### <a name="parameters---delayactive"></a>パラメーター - delayActive

値  

### <a name="return-value---delayactive"></a>戻り値 - delayActive

## <a name="method-extends"></a>メソッド extends

```xpp
public int extends([AnyType value])
```

### <a name="parameters---extends"></a>パラメーター - extends

値  

### <a name="return-value---extends"></a>戻り値 - extends

## <a name="method-getxppilimplementation"></a>メソッド GetXppILImplementation

```xpp
public str GetXppILImplementation()
```

### <a name="return-value---getxppilimplementation"></a>戻り値 - GetXppILImplementation

## <a name="method-index"></a>メソッド index

```xpp
public IndexId index([IndexId value])
```

### <a name="parameters---index"></a>パラメーター - index

値  

### <a name="return-value---index"></a>戻り値 - index

## <a name="method-insertatend"></a>メソッド insertAtEnd

```xpp
public boolean insertAtEnd([boolean value])
```

### <a name="parameters---insertatend"></a>パラメーター - insertAtEnd

値  

### <a name="return-value---insertatend"></a>戻り値 - insertAtEnd

## <a name="method-insertifempty"></a>メソッド insertIfEmpty

```xpp
public boolean insertIfEmpty([boolean value])
```

### <a name="parameters---insertifempty"></a>パラメーター - insertIfEmpty

値  

### <a name="return-value---insertifempty"></a>戻り値 - insertIfEmpty

## <a name="method-isbasedatasource"></a>メソッド isBaseDataSource

```xpp
public boolean isBaseDataSource()
```

### <a name="return-value---isbasedatasource"></a>戻り値 - isBaseDataSource

## <a name="method-isinheritancedatasource"></a>メソッド isInheritanceDataSource

```xpp
public boolean isInheritanceDataSource()
```

### <a name="return-value---isinheritancedatasource"></a>戻り値 - isInheritanceDataSource

## <a name="method-ismasterdatasource"></a>メソッド isMasterDataSource

```xpp
public boolean isMasterDataSource()
```

### <a name="return-value---ismasterdatasource"></a>戻り値 - isMasterDataSource

## <a name="method-joinrelation"></a>メソッド joinRelation

```xpp
public str joinRelation([str value])
```

### <a name="parameters---joinrelation"></a>パラメーター - joinRelation

値  

### <a name="return-value---joinrelation"></a>戻り値 - joinRelation

## <a name="method-joinsource"></a>メソッド joinSource

```xpp
public int joinSource([AnyType value])
```

### <a name="parameters---joinsource"></a>パラメーター - joinSource

値  

### <a name="return-value---joinsource"></a>戻り値 - joinSource

## <a name="method-linktype"></a>メソッド linkType

```xpp
public int linkType([int value])
```

### <a name="parameters---linktype"></a>パラメーター - linkType

値  

### <a name="return-value---linktype"></a>戻り値 - linkType

## <a name="method-masterdatasource"></a>メソッド masterDataSource

```xpp
public FormBuildDataSource masterDataSource()
```

### <a name="return-value---masterdatasource"></a>戻り値 - masterDataSource

## <a name="method-maxaccessright"></a>メソッド maxAccessRight

```xpp
public int maxAccessRight([int value])
```

### <a name="parameters---maxaccessright"></a>パラメーター - maxAccessRight

値  

### <a name="return-value---maxaccessright"></a>戻り値 - maxAccessRight

## <a name="method-maxrecordstoload"></a>メソッド maxRecordsToLoad

```xpp
public int maxRecordsToLoad([int value])
```

### <a name="parameters---maxrecordstoload"></a>パラメーター - maxRecordsToLoad

値  

### <a name="return-value---maxrecordstoload"></a>戻り値 - maxRecordsToLoad

## <a name="method-name"></a>メソッド名

フォーム、レポート、テーブル、クエリ、または別の MSDAX アプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。

```xpp
public str name([str value])
```

### <a name="parameters---name"></a>パラメーター - name

値  

### <a name="return-value---name"></a>戻り値 - name

アプリケーション オブジェクトを識別するためにコードで使用される名前。

### <a name="remarks---name"></a>備考 - 名前

オブジェクトの名前プロパティ値は、コードの競合を避けるために、次の基準を満たしている必要があります。

-   文字で始めます。
-   250 文字を超えないでください。
-   数字とアンダースコア文字を含めることができます。
-   句読点やスペースを含めることはできません。
-   テーブルは、拡張データ型、基本列挙型、クラスなどの他のパブリック オブジェクトと同じ名前を持つことはできません。

## <a name="method-onlyfetchactive"></a>メソッド onlyFetchActive

```xpp
public boolean onlyFetchActive([boolean value])
```

### <a name="parameters---onlyfetchactive"></a>パラメーター - onlyFetchActive

値  

### <a name="return-value---onlyfetchactive"></a>戻り値 - onlyFetchActive

## <a name="method-optionalrecordmode"></a>メソッド optionalRecordMode

```xpp
public int optionalRecordMode([int value])
```

### <a name="parameters---optionalrecordmode"></a>パラメーター - optionalRecordMode

値  

### <a name="return-value---optionalrecordmode"></a>戻り値 - optionalRecordMode

## <a name="method-startposition"></a>メソッド startPosition

```xpp
public int startPosition([int value])
```

### <a name="parameters---startposition"></a>パラメーター - startPosition

値  

### <a name="return-value---startposition"></a>戻り値 - startPosition

## <a name="method-table"></a>メソッド table

オブジェクトに関連付けられているテーブル ID を取得または設定します。

```xpp
public TableId table([TableId value])
```

### <a name="parameters---table"></a>パラメーター - table

値  

### <a name="return-value---table"></a>戻り値 - toBlob

オブジェクトに関連付けられたテーブル ID の現在の値。

## <a name="method-validtimestateautoquery"></a>メソッド validTimeStateAutoQuery

```xpp
public int validTimeStateAutoQuery([int value])
```

### <a name="parameters---validtimestateautoquery"></a>パラメーター - validTimeStateAutoQuery

値  

### <a name="return-value---validtimestateautoquery"></a>戻り値 - validTimeStateAutoQuery

## <a name="method-validtimestateupdate"></a>メソッド validTimeStateUpdate

```xpp
public int validTimeStateUpdate([int value])
```

### <a name="parameters---validtimestateupdate"></a>パラメーター - validTimeStateUpdate

値  

### <a name="return-value---validtimestateupdate"></a>戻り値 - validTimeStateUpdate

## <a name="method-registerxppdatafieldilimplementation"></a>メソッド RegisterXppDataFieldILImplementation

```xpp
public void RegisterXppDataFieldILImplementation(str fieldName, str className)
```

### <a name="parameters---registerxppdatafieldilimplementation"></a>パラメーター - RegisterXppDataFieldILImplementation

fieldName  

<!-- -->

className  

## <a name="method-registerxppilimplementation"></a>メソッド RegisterXppILImplementation

```xpp
public void RegisterXppILImplementation(str className)
```

### <a name="parameters---registerxppilimplementation"></a>パラメーター - RegisterXppILImplementation

className  

## <a name="method-setdatalinktype"></a>メソッド SetDataLinkType

```xpp
public void SetDataLinkType(QueryDataLinkType linkType, str parentDataSource)
```

### <a name="parameters---setdatalinktype"></a>パラメーター - SetDataLinkType

linkType  

<!-- -->

parentDataSource  

