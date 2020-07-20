---
title: DataSourceMethodInfo クラス
description: このトピックでは、DataSourceMethodInfo クラスについて説明します。
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
ms.openlocfilehash: b79fb1c929cf94d65eb8950526cfc979353e37f8
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502734"
---
# <a name="class-datasourcemethodinfo"></a>クラス DataSourceMethodInfo

[!include [banner](../../includes/banner.md)]

```xpp
class DataSourceMethodInfo extends Object
```

## <a name="remarks"></a>備考

## <a name="examples"></a>例

## <a name="methods"></a>メソッド

| 方法                                                                                                           | 説明                                     |
|------------------------------------------------------------------------------------------------------------------|-------------------------------------------------|
| public DisplayFunctionType displayType()                                                                         |                                                 |
| public boolean isStatic()                                                                                        |                                                 |
| public str name()                                                                                                |                                                 |
| public Types returnType()                                                                                        |                                                 |
| public int returnTypeId()                                                                                        |                                                 |
| public void new(str name, DisplayFunctionType displayType, Types returnType, int returnTypeId, boolean isStatic) | Object クラスの新しいインスタンスを初期化します。 |
| public void finalize()                                                                                           |                                                 |

## <a name="method-displaytype"></a>メソッド displayType

```xpp
public DisplayFunctionType displayType()
```

### <a name="return-value---displaytype"></a>戻り値 - displayType

## <a name="method-isstatic"></a>メソッド isStatic

```xpp
public boolean isStatic()
```

### <a name="return-value---isstatic"></a>戻り値 - isStatic

## <a name="method-name"></a>メソッド名

```xpp
public str name()
```

### <a name="return-value---name"></a>戻り値 - name

## <a name="method-returntype"></a>メソッド returnType

```xpp
public Types returnType()
```

### <a name="return-value---returntype"></a>戻り値 - returnType

## <a name="method-returntypeid"></a>メソッド returnTypeId

```xpp
public int returnTypeId()
```

### <a name="return-value---returntypeid"></a>戻り値 - returnTypeId

## <a name="method-new"></a>メソッド new

Object クラスの新しいインスタンスを初期化します。

```xpp
public void new(str name, DisplayFunctionType displayType, Types returnType, int returnTypeId, boolean isStatic)
```

### <a name="parameters---new"></a>パラメーター - new

名前  

<!-- -->

displayType  

<!-- -->

returnType  

<!-- -->

returnTypeId  

<!-- -->

isStatic  

## <a name="method-finalize"></a>メソッド finalize

```xpp
public void finalize()
```

