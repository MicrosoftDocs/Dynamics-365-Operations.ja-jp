---
title: ListPage クラス
description: このトピックでは、ListPage クラスについて説明します。
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
ms.openlocfilehash: 80b57cf4369574cde992b2c98305f3bd398830ae
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502585"
---
# <a name="class-listpage"></a>クラス ListPage

[!include [banner](../../includes/banner.md)]

```xpp
class ListPage extends Page
```

## <a name="remarks"></a>備考

## <a name="examples"></a>例

## <a name="methods"></a>メソッド

| 方法                                                                      | 説明                                       |
|-----------------------------------------------------------------------------|---------------------------------------------------|
| public str actionPaneControlParameters(str controlName, \[str parameters\]) |                                                   |
| public Array activeActionPaneTabNames()                                     | 指定された有効なタブの名前を取得します。        |
| public str caption(\[str value\])                                           |                                                   |
| public ListPageArgs listPageArgs()                                          |                                                   |
| public int listPageFieldDataField(str fieldName)                            |                                                   |
| public Array listPageFieldNames()                                           |                                                   |
| public int listPageFieldTableId(str fieldName)                              |                                                   |
| public boolean listPageFieldVisible(str fieldName, \[boolean visible\])     |                                                   |
| public str modeledQueryName(\[str value\])                                  |                                                   |
| public void new()                                                           | ListPage クラスの新しいインスタンスを初期化します。 |

## <a name="method-actionpanecontrolparameters"></a>メソッド actionPaneControlParameters

```xpp
public str actionPaneControlParameters(str controlName, [str parameters])
```

### <a name="parameters---actionpanecontrolparameters"></a>パラメーター - actionPaneControlParameters

controlName  

<!-- -->

パラメータ  

### <a name="return-value---actionpanecontrolparameters"></a>戻り値 - actionPaneControlParameters

## <a name="method-activeactionpanetabnames"></a>メソッド activeActionPaneTabNames

指定された有効なタブの名前を取得します。

```xpp
public Array activeActionPaneTabNames()
```

### <a name="return-value---activeactionpanetabnames"></a>戻り値 - activeActionPaneTabNames

アクティブなタブの名前を含む配列です。

## <a name="method-caption"></a>メソッド caption

```xpp
public str caption([str value])
```

### <a name="parameters---caption"></a>パラメーター - caption

値  

### <a name="return-value---caption"></a>戻り値 - caption

## <a name="method-listpageargs"></a>メソッド listPageArgs

```xpp
public ListPageArgs listPageArgs()
```

### <a name="return-value---listpageargs"></a>戻り値 - listPageArgs

## <a name="method-listpagefielddatafield"></a>メソッド listPageFieldDataField

```xpp
public int listPageFieldDataField(str fieldName)
```

### <a name="parameters---listpagefielddatafield"></a>パラメーター - listPageFieldDataField

fieldName  

### <a name="return-value---listpagefielddatafield"></a>戻り値 - listPageFieldDataField

## <a name="method-listpagefieldnames"></a>メソッド listPageFieldNames

```xpp
public Array listPageFieldNames()
```

### <a name="return-value---listpagefieldnames"></a>戻り値 - listPageFieldNames

## <a name="method-listpagefieldtableid"></a>メソッド listPageFieldTableId

```xpp
public int listPageFieldTableId(str fieldName)
```

### <a name="parameters---listpagefieldtableid"></a>パラメーター - listPageFieldTableId

fieldName  

### <a name="return-value---listpagefieldtableid"></a>戻り値 - listPageFieldTableId

## <a name="method-listpagefieldvisible"></a>メソッド listPageFieldVisible

```xpp
public boolean listPageFieldVisible(str fieldName, [boolean visible])
```

### <a name="parameters---listpagefieldvisible"></a>パラメーター - listPageFieldVisible

fieldName  

<!-- -->

表示  

### <a name="return-value---listpagefieldvisible"></a>戻り値 - listPageFieldVisible

## <a name="method-modeledqueryname"></a>メソッド modeledQueryName

```xpp
public str modeledQueryName([str value])
```

### <a name="parameters---modeledqueryname"></a>パラメーター - modeledQueryName

値  

### <a name="return-value---modeledqueryname"></a>戻り値 - modeledQueryName

## <a name="method-new"></a>メソッド new

ListPage クラスの新しいインスタンスを初期化します。

```xpp
public void new()
```

