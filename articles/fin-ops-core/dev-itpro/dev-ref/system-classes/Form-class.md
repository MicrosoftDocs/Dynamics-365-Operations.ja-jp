---
title: Form クラス
description: このトピックでは、Form クラスについて説明します。
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
ms.openlocfilehash: 1a0c9f25d7529b393f401cf14989d8e59f7f53a4
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502978"
---
# <a name="class-form"></a>クラス フォーム

[!include [banner](../../includes/banner.md)]

```xpp
class Form extends TreeNode
```

フォーム クラスは、デザイン時のフォームのインスタンスを表します。

## <a name="remarks"></a>備考

## <a name="examples"></a>例

## <a name="methods"></a>メソッド

| 方法                                                                                                                           | 説明                                                                                                               |
|----------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| public FormBuildControl addControl(FormControlType controlType, str controlName)                                                 |                                                                                                                           |
| public FormBuildControl addControlEx(str controlClass, str controlName, \[FormBuildControl insertAfter\], \[boolean pushFront\]) |                                                                                                                           |
| public FormBuildDataSource addDataSource(str name, \[str tableName\])                                                            |                                                                                                                           |
| public List rootFormDataSources()                                                                                                |                                                                                                                           |
| public FormBuildDesign addDesign(str name)                                                                                       |                                                                                                                           |
| public Query query(str queryName)                                                                                                |                                                                                                                           |
| public boolean allowPreLoading(\[boolean value\])                                                                                | 関連付けられた FormRun インスタンスの作成時にプリロードされたインスタンスを使用できるかどうかを決定するブール値。 |
| public boolean autoCacheUpdate(\[boolean value\])                                                                                |                                                                                                                           |
| public str changedBy(\[str value\])                                                                                              | アプリケーション オブジェクトを最後に変更したユーザーの名前を取得または設定します。                                                |
| public Date changedDate(\[Date value\])                                                                                          | アプリケーション オブジェクトが最後に変更された日付を取得または設定します。                                                             |
| public str changedTime(\[str value\])                                                                                            | アプリケーション オブジェクトが最後に変更された時刻を取得または設定します。                                                             |
| public ChangeGroupMode changeGroupMode(\[ChangeGroupMode value\])                                                                |                                                                                                                           |
| public str createdBy(\[str value\])                                                                                              | アプリケーション オブジェクトを作成したユーザーの名前を取得または設定します。                                                     |
| public Date creationDate(\[Date value\])                                                                                         | アプリケーション オブジェクトが作成された日付を取得または設定します。                                                                  |
| public str creationTime(\[str value\])                                                                                           |                                                                                                                           |
| public FormBuildDataSource dataSource(AnyType objectSet)                                                                         |                                                                                                                           |
| public int dataSourceCount()                                                                                                     |                                                                                                                           |
| public FormBuildDesign design(\[int designNo\])                                                                                  |                                                                                                                           |
| public int formTemplate(\[int value\])                                                                                           |                                                                                                                           |
| public str interactionClass(\[str value\])                                                                                       |                                                                                                                           |
| public boolean isLoadedForInference()                                                                                            |                                                                                                                           |
| public str name(\[str value\])                                                                                                   | フォーム、レポート、テーブル、クエリ、または別の MSDAX アプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。 |
| public Guid origin(\[Guid value\])                                                                                               |                                                                                                                           |
| ::public static boolean formKernelObjectHasMethod (Object kernelObject, str methodName)                                           |                                                                                                                           |
| ::public static boolean formObjectSetHasMethod (FormObjectSet formObjectSet, str methodName)                                      |                                                                                                                           |
| ::public static boolean formRunHasMethod (xFormRun formRun, str methodName)                                                       |                                                                                                                           |
| ::public static str getSetupUserQueryElementName (MenuItemType menuItemType, str menuItemName)                                    |                                                                                                                           |
| public void new(\[str name\], \[boolean buildMode\])                                                                             | Form クラスの新しいインスタンスを初期化します。                                                                             |
| public void inInitializeDesign(\[boolean value\])                                                                                |                                                                                                                           |
| public void save()                                                                                                               |                                                                                                                           |
| public void load(str name, \[boolean buildMode\])                                                                                |                                                                                                                           |
| public void finalize()                                                                                                           |                                                                                                                           |

## <a name="method-addcontrol"></a>メソッド addControl

```xpp
public FormBuildControl addControl(FormControlType controlType, str controlName)
```

### <a name="parameters---addcontrol"></a>パラメーター - addControl

controlType  

<!-- -->

controlName  

### <a name="return-value---addcontrol"></a>戻り値 - addControl

## <a name="method-addcontrolex"></a>メソッド addControlEx

```xpp
public FormBuildControl addControlEx(str controlClass, str controlName, [FormBuildControl insertAfter], [boolean pushFront])
```

### <a name="parameters---addcontrolex"></a>パラメーター - addControlEx

controlClass  

<!-- -->

controlName  

<!-- -->

insertAfter  

<!-- -->

pushFront  

### <a name="return-value---addcontrolex"></a>戻り値 - addControlEx

## <a name="method-adddatasource"></a>メソッド addDataSource

```xpp
public FormBuildDataSource addDataSource(str name, [str tableName])
```

### <a name="parameters---adddatasource"></a>パラメーター - addDataSource

名前  

<!-- -->

tableName  

### <a name="return-value---adddatasource"></a>戻り値 - addDataSource

## <a name="method-rootformdatasources"></a>メソッド rootFormDataSources

```xpp
public List rootFormDataSources()
```

### <a name="return-value---rootformdatasources"></a>戻り値 - rootFormDataSources

## <a name="method-adddesign"></a>メソッド addDesign

```xpp
public FormBuildDesign addDesign(str name)
```

### <a name="parameters---adddesign"></a>パラメーター - addDesign

名前  

### <a name="return-value---adddesign"></a>戻り値 - addDesign

## <a name="method-query"></a>メソッド query

```xpp
public Query query(str queryName)
```

### <a name="parameters---query"></a>パラメーター - query

queryName  

### <a name="return-value---query"></a>戻り値 - query

## <a name="method-allowpreloading"></a>メソッド allowPreLoading

関連付けられた FormRun インスタンスの作成時にプリロードされたインスタンスを使用できるかどうかを決定するブール値。

```xpp
public boolean allowPreLoading([boolean value])
```

### <a name="parameters---allowpreloading"></a>パラメーター - allowPreLoading

値  
関連付けられた FormRun インスタンスが作成されるときにプリロードされたインスタンスを使用できる場合は true。それ以外の場合は、false。

### <a name="return-value---allowpreloading"></a>戻り値 - allowPreLoading

関連付けられた FormRun インスタンスが作成されるときにプリロードされたインスタンスを使用できる場合は true。それ以外の場合は、false。

## <a name="method-autocacheupdate"></a>メソッド autoCacheUpdate

```xpp
public boolean autoCacheUpdate([boolean value])
```

### <a name="parameters---autocacheupdate"></a>パラメーター - autoCacheUpdate

値  

### <a name="return-value---autocacheupdate"></a>戻り値 - autoCacheUpdate

## <a name="method-changedby"></a>メソッド changedBy

アプリケーション オブジェクトを最後に変更したユーザーの名前を取得または設定します。

```xpp
public str changedBy([str value])
```

### <a name="parameters---changedby"></a>パラメーター - changedBy

値  

### <a name="return-value---changedby"></a>戻り値 - changedBy

ユーザーの名前。

## <a name="method-changeddate"></a>メソッド changedDate

アプリケーション オブジェクトが最後に変更された日付を取得または設定します。

```xpp
public Date changedDate([Date value])
```

### <a name="parameters---changeddate"></a>パラメーター - changedDate

値  

### <a name="return-value---changeddate"></a>戻り値 - changedDate

アプリケーション オブジェクトが最後に変更された日付。

## <a name="method-changedtime"></a>メソッド changedTime

アプリケーション オブジェクトが最後に変更された時刻を取得または設定します。

```xpp
public str changedTime([str value])
```

### <a name="parameters---changedtime"></a>パラメーター - changedTime

値  

### <a name="return-value---changedtime"></a>戻り値 - changedTime

アプリケーション オブジェクトが最後に変更された時間。

## <a name="method-changegroupmode"></a>メソッド changeGroupMode

```xpp
public ChangeGroupMode changeGroupMode([ChangeGroupMode value])
```

### <a name="parameters---changegroupmode"></a>パラメーター - changeGroupMode

値  

### <a name="return-value---changegroupmode"></a>戻り値 - changeGroupMode

## <a name="method-createdby"></a>メソッド createdBy

アプリケーション オブジェクトを作成したユーザーの名前を取得または設定します。

```xpp
public str createdBy([str value])
```

### <a name="parameters---createdby"></a>パラメーター - createdBy

値  

### <a name="return-value---createdby"></a>戻り値 - createdBy

ユーザーの名前。

## <a name="method-creationdate"></a>メソッド creationDate

アプリケーション オブジェクトが作成された日付を取得または設定します。

```xpp
public Date creationDate([Date value])
```

### <a name="parameters---creationdate"></a>パラメーター - creationDate

値  

### <a name="return-value---creationdate"></a>戻り値 - creationDate

アプリケーション オブジェクトが作成された日付。

## <a name="method-creationtime"></a>メソッド creationTime

```xpp
public str creationTime([str value])
```

### <a name="parameters---creationtime"></a>パラメーター - creationTime

値  

### <a name="return-value---creationtime"></a>戻り値 - creationTime

## <a name="method-datasource"></a>メソッド dataSource

```xpp
public FormBuildDataSource dataSource(AnyType objectSet)
```

### <a name="parameters---datasource"></a>パラメーター - dataSource

objectSet  

### <a name="return-value---datasource"></a>戻り値 - dataSource

## <a name="method-datasourcecount"></a>メソッド dataSourceCount

```xpp
public int dataSourceCount()
```

### <a name="return-value---datasourcecount"></a>戻り値 - dataSourceCount

## <a name="method-design"></a>メソッド design

```xpp
public FormBuildDesign design([int designNo])
```

### <a name="parameters---design"></a>パラメーター - design

designNo  

### <a name="return-value---design"></a>戻り値 - design

## <a name="method-formtemplate"></a>メソッド formTemplate

```xpp
public int formTemplate([int value])
```

### <a name="parameters---formtemplate"></a>パラメーター - formTemplate

値  

### <a name="return-value---formtemplate"></a>戻り値 - formTemplate

## <a name="method-interactionclass"></a>メソッド interactionClass

```xpp
public str interactionClass([str value])
```

### <a name="parameters---interactionclass"></a>パラメーター - interactionClass

値  

### <a name="return-value---interactionclass"></a>戻り値 - interactionClass

## <a name="method-isloadedforinference"></a>メソッド isLoadedForInference

```xpp
public boolean isLoadedForInference()
```

### <a name="return-value---isloadedforinference"></a>戻り値 - isLoadedForInference

## <a name="method-name"></a>メソッド名

フォーム、レポート、テーブル、クエリ、または別の MSDAX アプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。

```xpp
public str name([str value])
```

### <a name="parameters---name"></a>パラメーター - name

値  

### <a name="return-value---name"></a>戻り値 - name

アプリケーション オブジェクトを識別するためにコードで使用される名前。

### <a name="remarks---name"></a>備考 - name

オブジェクトの名前プロパティ値は、コードの競合を避けるために、次の基準を満たしている必要があります。

-   文字で始めます。
-   250 文字を超えないでください。
-   数字とアンダースコア文字を含めることができます。
-   句読点やスペースを含めることはできません。
-   テーブルは、拡張データ型、基本列挙型、クラスなどの他のパブリック オブジェクトと同じ名前を持つことはできません。

## <a name="method-origin"></a>メソッド origin

```xpp
public Guid origin([Guid value])
```

### <a name="parameters---origin"></a>パラメーター - origin

値  

### <a name="return-value---origin"></a>戻り値 - origin

## <a name="method-formkernelobjecthasmethod"></a>メソッド formKernelObjectHasMethod

```xpp
public static boolean formKernelObjectHasMethod(Object kernelObject, str methodName)
```

### <a name="parameters---formkernelobjecthasmethod"></a>パラメーター - formKernelObjectHasMethod

kernelObject  

<!-- -->

methodName  

### <a name="return-value---formkernelobjecthasmethod"></a>戻り値 - formKernelObjectHasMethod

## <a name="method-formobjectsethasmethod"></a>メソッド formObjectSetHasMethod

```xpp
public static boolean formObjectSetHasMethod(FormObjectSet formObjectSet, str methodName)
```

### <a name="parameters---formobjectsethasmethod"></a>パラメーター - formObjectSetHasMethod

formObjectSet  

<!-- -->

methodName  

### <a name="return-value---formobjectsethasmethod"></a>戻り値 - formObjectSetHasMethod

## <a name="method-formrunhasmethod"></a>メソッド formRunHasMethod

```xpp
public static boolean formRunHasMethod(xFormRun formRun, str methodName)
```

### <a name="parameters---formrunhasmethod"></a>パラメーター - formRunHasMethod

formRun  

<!-- -->

methodName  

### <a name="return-value---formrunhasmethod"></a>戻り値 - formRunHasMethod

## <a name="method-getsetupuserqueryelementname"></a>メソッド getSetupUserQueryElementName

```xpp
public static str getSetupUserQueryElementName(MenuItemType menuItemType, str menuItemName)
```

### <a name="parameters---getsetupuserqueryelementname"></a>パラメーター - getSetupUserQueryElementName

menuItemType  

<!-- -->

menuItemName  

### <a name="return-value---getsetupuserqueryelementname"></a>戻り値 - getSetupUserQueryElementName

## <a name="method-new"></a>メソッド new

Form クラスの新しいインスタンスを初期化します。

```xpp
public void new([str name], [boolean buildMode])
```

### <a name="parameters---new"></a>パラメーター - new

名前  

<!-- -->

buildMode  

## <a name="method-ininitializedesign"></a>メソッド inInitializeDesign

```xpp
public void inInitializeDesign([boolean value])
```

### <a name="parameters---ininitializedesign"></a>パラメーター - inInitializeDesign

値  

## <a name="method-save"></a>メソッド save

```xpp
public void save()
```

## <a name="method-load"></a>メソッド load

```xpp
public void load(str name, [boolean buildMode])
```

### <a name="parameters---load"></a>パラメーター - load

名前  

<!-- -->

buildMode  

## <a name="method-finalize"></a>メソッド finalize

```xpp
public void finalize()
```

