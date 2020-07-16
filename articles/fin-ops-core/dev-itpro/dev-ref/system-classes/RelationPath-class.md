---
title: RelationPath クラス
description: このトピックでは、RelationPath クラスについて説明します。
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
ms.openlocfilehash: e244ee5943113f51635e7a8b47545329d77276d6
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502852"
---
# <a name="class-relationpath"></a>クラス RelationPath

[!include [banner](../../includes/banner.md)]

```xpp
class RelationPath extends Object
```

## <a name="remarks"></a>備考

## <a name="examples"></a>例

## <a name="methods"></a>メソッド

| 方法                                                                                        | 説明                                           |
|-----------------------------------------------------------------------------------------------|-------------------------------------------------------|
| public boolean isEqualTo(RelationPath otherRelationPath)                                      |                                                       |
| public boolean isPathCyclical(boolean excludePathRootTable)                                   |                                                       |
| public boolean isPathValid()                                                                  |                                                       |
| public List pathAsList()                                                                      |                                                       |
| public str pathAsString(\[str delimiter\])                                                    |                                                       |
| public str pathRelativeTable()                                                                |                                                       |
| public str pathRootTable()                                                                    |                                                       |
| ::public static RelationPath construct(RelationPath sourceRelationPath)                       |                                                       |
| ::public static RelationPath constructFromPathList(str pathRootTableName, List relationPath)  |                                                       |
| ::public static RelationPath constructFromPathString(str pathRootTableName, str relationPath) |                                                       |
| private void new()                                                                            | RelationPath クラスの新しいインスタンスを初期化します。 |
| public void trimPathAtFront()                                                                 |                                                       |
| public void trimPathAtEnd()                                                                   |                                                       |

## <a name="method-isequalto"></a>メソッド isEqualTo

```xpp
public boolean isEqualTo(RelationPath otherRelationPath)
```

### <a name="parameters---isequalto"></a>パラメーター - isEqualTo

otherRelationPath  

### <a name="return-value---isequalto"></a>戻り値 - isEqualTo

## <a name="method-ispathcyclical"></a>メソッド isPathCyclical

```xpp
public boolean isPathCyclical(boolean excludePathRootTable)
```

### <a name="parameters---ispathcyclical"></a>パラメーター - isPathCyclical

excludePathRootTable  

### <a name="return-value---ispathcyclical"></a>戻り値 - isPathCyclical

## <a name="method-ispathvalid"></a>メソッド isPathValid

```xpp
public boolean isPathValid()
```

### <a name="return-value---ispathvalid"></a>戻り値 - isPathValid

## <a name="method-pathaslist"></a>メソッド pathAsList

```xpp
public List pathAsList()
```

### <a name="return-value---pathaslist"></a>戻り値 - pathAsList

## <a name="method-pathasstring"></a>メソッド pathAsString

```xpp
public str pathAsString([str delimiter])
```

### <a name="parameters---pathasstring"></a>パラメーター - pathAsString

delimiter  

### <a name="return-value---pathasstring"></a>戻り値 - pathAsString

## <a name="method-pathrelativetable"></a>メソッド pathRelativeTable

```xpp
public str pathRelativeTable()
```

### <a name="return-value---pathrelativetable"></a>戻り値 - pathRelativeTable

## <a name="method-pathroottable"></a>メソッド pathRootTable

```xpp
public str pathRootTable()
```

### <a name="return-value---pathroottable"></a>戻り値 - pathRootTable

## <a name="method-construct"></a>メソッド construct

```xpp
public static RelationPath construct(RelationPath sourceRelationPath)
```

### <a name="parameters---construct"></a>パラメーター - construct

sourceRelationPath  

### <a name="return-value---construct"></a>戻り値 - construct

## <a name="method-constructfrompathlist"></a>メソッド constructFromPathList

```xpp
public static RelationPath constructFromPathList(str pathRootTableName, List relationPath)
```

### <a name="parameters---constructfrompathlist"></a>パラメーター - constructFromPathList

pathRootTableName  

<!-- -->

relationPath  

### <a name="return-value---constructfrompathlist"></a>戻り値 - constructFromPathList

## <a name="method-constructfrompathstring"></a>メソッド constructFromPathString

```xpp
public static RelationPath constructFromPathString(str pathRootTableName, str relationPath)
```

### <a name="parameters---constructfrompathstring"></a>パラメーター - constructFromPathString

pathRootTableName  

<!-- -->

relationPath  

### <a name="return-value---constructfrompathstring"></a>戻り値 - constructFromPathString

## <a name="method-new"></a>メソッド new

RelationPath クラスの新しいインスタンスを初期化します。

```xpp
private void new()
```

## <a name="method-trimpathatfront"></a>メソッド trimPathAtFront

```xpp
public void trimPathAtFront()
```

## <a name="method-trimpathatend"></a>メソッド trimPathAtEnd

```xpp
public void trimPathAtEnd()
```

