---
title: QueryFilter クラス
description: このトピックでは、QueryFilter クラスについて説明します。
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
ms.openlocfilehash: d3ef7ac6dcdccddd7d7f2c25d7ef1627351bdce6
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502862"
---
# <a name="class-queryfilter"></a>クラス QueryFilter

[!include [banner](../../includes/banner.md)]

```xpp
class QueryFilter extends Object
```

## <a name="remarks"></a>備考

## <a name="examples"></a>例

## <a name="methods"></a>メソッド

| 方法                                                        | 説明                                          |
|---------------------------------------------------------------|------------------------------------------------------|
| public QueryBuildDataSource dataSource()                      |                                                      |
| public FieldName field()                                      |                                                      |
| public QueryRangeType rangeType(\[QueryRangeType rangeType\]) |                                                      |
| public int status(\[int status\])                             |                                                      |
| public str toString()                                         | 現在のオブジェクトを表す文字列を返します。 |
| public str value(\[str value\])                               |                                                      |
| public void finalize()                                        |                                                      |

## <a name="method-datasource"></a>メソッド dataSource

```xpp
public QueryBuildDataSource dataSource()
```

### <a name="return-value---datasource"></a>戻り値 - dataSource

## <a name="method-field"></a>メソッド field

```xpp
public FieldName field()
```

### <a name="return-value---field"></a>戻り値 - field

## <a name="method-rangetype"></a>メソッド rangeType

```xpp
public QueryRangeType rangeType([QueryRangeType rangeType])
```

### <a name="parameters---rangetype"></a>パラメーター - rangeType

rangeType  

### <a name="return-value---rangetype"></a>戻り値 - rangeType

## <a name="method-status"></a>メソッド status

```xpp
public int status([int status])
```

### <a name="parameters---status"></a>パラメーター - status

状態  

### <a name="return-value---status"></a>戻り値 - status

## <a name="method-tostring"></a>メソッド toString

現在のオブジェクトを表す文字列を返します。

```xpp
public str toString()
```

### <a name="return-value---tostring"></a>戻り値 - toString

現在のオブジェクトを表す文字列。

### <a name="remarks---tostring"></a>備考 - toString

既定の実装は、オブジェクトのクラス名を返します。 メソッドは派生クラスで上書きできるため、そのタイプの意味のある値が返されます。 たとえば、SysMethodInfo クラスのインスタンスは、インスタンスまたは静的などのメソッド名およびメソッドのタイプを返します。

## <a name="method-value"></a>メソッド value

```xpp
public str value([str value])
```

### <a name="parameters---value"></a>パラメーター - value

値  

### <a name="return-value---value"></a>戻り値 - value

## <a name="method-finalize"></a>メソッド finalize

```xpp
public void finalize()
```

