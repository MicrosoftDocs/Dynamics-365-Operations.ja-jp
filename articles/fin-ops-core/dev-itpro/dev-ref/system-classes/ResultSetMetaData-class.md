---
title: ResultSetMetaData クラス
description: このトピックでは、ResultSetMetaData クラスについて説明します。
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
ms.openlocfilehash: ffed55c3fa017e132105e4b799588d26206629a4
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502822"
---
# <a name="class-resultsetmetadata"></a>クラス ResultSetMetaData

[!include [banner](../../includes/banner.md)]

```xpp
class ResultSetMetaData extends Object
```

## <a name="remarks"></a>備考

## <a name="examples"></a>例

## <a name="methods"></a>メソッド

| 方法                                        | 説明 |
|-----------------------------------------------|-------------|
| public int getColumnCount()                   |             |
| public int getColumnDisplaySize(int ColumnID) |             |
| public str getColumnName(int ColumnID)        |             |
| public int getColumnType(int ColumnID)        |             |
| public int getPrecision(int ColumnID)         |             |
| public int getScale(int ColumnID)             |             |
| public int isNullable(int ColumnID)           |             |

## <a name="method-getcolumncount"></a>メソッド getColumnCount

```xpp
public int getColumnCount()
```

### <a name="return-value---getcolumncount"></a>戻り値 - getColumnCount

## <a name="method-getcolumndisplaysize"></a>メソッド getColumnDisplaySize

```xpp
public int getColumnDisplaySize(int ColumnID)
```

### <a name="parameters---getcolumndisplaysize"></a>パラメーター - getColumnDisplaySize

ColumnID  

### <a name="return-value---getcolumndisplaysize"></a>戻り値 - getColumnDisplaySize

## <a name="method-getcolumnname"></a>メソッド getColumnName

```xpp
public str getColumnName(int ColumnID)
```

### <a name="parameters---getcolumnname"></a>パラメーター - getColumnName

ColumnID  

### <a name="return-value---getcolumnname"></a>戻り値 - getColumnName

## <a name="method-getcolumntype"></a>メソッド getColumnType

```xpp
public int getColumnType(int ColumnID)
```

### <a name="parameters---getcolumntype"></a>パラメーター - getColumnType

ColumnID  

### <a name="return-value---getcolumntype"></a>戻り値 - getColumnType

## <a name="method-getprecision"></a>メソッド getPrecision

```xpp
public int getPrecision(int ColumnID)
```

### <a name="parameters---getprecision"></a>パラメーター - getPrecision

ColumnID  

### <a name="return-value---getprecision"></a>戻り値 - getPrecision

## <a name="method-getscale"></a>メソッド getScale

```xpp
public int getScale(int ColumnID)
```

### <a name="parameters---getscale"></a>パラメーター - getScale

ColumnID  

### <a name="return-value---getscale"></a>戻り値 - getScale

## <a name="method-isnullable"></a>メソッド isNullable

```xpp
public int isNullable(int ColumnID)
```

### <a name="parameters---isnullable"></a>パラメーター - isNullable

ColumnID  

### <a name="return-value---isnullable"></a>戻り値 - isNullable

