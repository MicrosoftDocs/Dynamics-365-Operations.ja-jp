---
title: InitialQueryParameter クラス
description: このトピックでは、InitialQueryParameter クラスについて説明します。
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
ms.openlocfilehash: 419ff1a480309f1874ed8b11dfc5aa4ecf0d4219
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502897"
---
# <a name="class-initialqueryparameter"></a>クラス InitialQueryParameter

[!include [banner](../../includes/banner.md)]

```xpp
class InitialQueryParameter extends Object
```

## <a name="remarks"></a>備考

## <a name="examples"></a>例

## <a name="methods"></a>メソッド

| 方法                                                                                                       | 説明                                                    |
|--------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|
| public boolean applyQuery(FormDataSource datasource)                                                         |                                                                |
| public str dataSourceName(\[str dataSourceName\])                                                            |                                                                |
| public str modeledQueryName(\[str modeledQueryName\])                                                        |                                                                |
| public Query query(\[Query query\])                                                                          |                                                                |
| ::public static InitialQueryParameter createByModeledQueryName(str modeledQueryName, \[str dataSourceName\]) |                                                                |
| ::public static InitialQueryParameter createByQuery(Query query, \[str dataSourceName\])                     |                                                                |
| public void finalize()                                                                                       |                                                                |
| public void new()                                                                                            | InitialQueryParameter クラスの新しいインスタンスを初期化します。 |

## <a name="method-applyquery"></a>メソッド applyQuery

```xpp
public boolean applyQuery(FormDataSource datasource)
```

### <a name="parameters---applyquery"></a>パラメーター - applyQuery

datasource  

### <a name="return-value---applyquery"></a>戻り値 - applyQuery

## <a name="method-datasourcename"></a>メソッド dataSourceName

```xpp
public str dataSourceName([str dataSourceName])
```

### <a name="parameters---datasourcename"></a>パラメーター - dataSourceName

dataSourceName  

### <a name="return-value---datasourcename"></a>戻り値 - dataSourceName

## <a name="method-modeledqueryname"></a>メソッド modeledQueryName

```xpp
public str modeledQueryName([str modeledQueryName])
```

### <a name="parameters---modeledqueryname"></a>パラメーター - modeledQueryName

modeledQueryName  

### <a name="return-value---modeledqueryname"></a>戻り値 - modeledQueryName

## <a name="method-query"></a>メソッド query

```xpp
public Query query([Query query])
```

### <a name="parameters---query"></a>パラメーター - query

クエリ  

### <a name="return-value---query"></a>戻り値 - query

## <a name="method-createbymodeledqueryname"></a>メソッド createByModeledQueryName

```xpp
public static InitialQueryParameter createByModeledQueryName(str modeledQueryName, [str dataSourceName])
```

### <a name="parameters---createbymodeledqueryname"></a>パラメーター - createByModeledQueryName

modeledQueryName  

<!-- -->

dataSourceName  

### <a name="return-value---createbymodeledqueryname"></a>戻り値 - createByModeledQueryName

## <a name="method-createbyquery"></a>メソッド createByQuery

```xpp
public static InitialQueryParameter createByQuery(Query query, [str dataSourceName])
```

### <a name="parameters---createbyquery"></a>パラメーター - createByQuery

クエリ  

<!-- -->

dataSourceName  

### <a name="return-value---createbyquery"></a>戻り値 - createByQuery

## <a name="method-finalize"></a>メソッド finalize

```xpp
public void finalize()
```

## <a name="method-new"></a>メソッド new

InitialQueryParameter クラスの新しいインスタンスを初期化します。

```xpp
public void new()
```

