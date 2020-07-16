---
title: OutputShapeField クラス
description: このトピックでは、OutputShapeField クラスについて説明します。
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
ms.openlocfilehash: 9afdc6732f011f88cacf37f450303d96c8833081
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502882"
---
# <a name="class-outputshapefield"></a>クラス OutputShapeField

[!include [banner](../../includes/banner.md)]

```xpp
class OutputShapeField extends OutputField
```

## <a name="remarks"></a>備考

## <a name="examples"></a>例

## <a name="methods"></a>メソッド

| 方法                       | 説明                                               |
|------------------------------|-----------------------------------------------------------|
| public int borderWidth()     |                                                           |
| public LineType lineType()   |                                                           |
| public ShapeType shapeType() |                                                           |
| public str toString()        | 現在のオブジェクトを表す文字列を返します。      |
| public int value()           |                                                           |
| public void new()            | OutputShapeField クラスの新しいインスタンスを初期化します。 |

## <a name="method-borderwidth"></a>メソッド borderWidth

```xpp
public int borderWidth()
```

### <a name="return-value---borderwidth"></a>戻り値 - borderWidth

## <a name="method-linetype"></a>メソッド lineType

```xpp
public LineType lineType()
```

### <a name="return-value---linetype"></a>戻り値 - lineType

## <a name="method-shapetype"></a>メソッド shapeType

```xpp
public ShapeType shapeType()
```

### <a name="return-value---shapetype"></a>戻り値 - shapeType

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
public int value()
```

### <a name="return-value---value"></a>戻り値 - value

## <a name="method-new"></a>メソッド new

OutputShapeField クラスの新しいインスタンスを初期化します。

```xpp
public void new()
```

