---
title: Enumerator クラス
description: このトピックでは、Enumerator クラスについて説明します。
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
ms.openlocfilehash: e3c5d3f2fcf69fd8ae298308ccdde686db568617
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502981"
---
# <a name="class-enumerator"></a>クラス列挙子

[!include [banner](../../includes/banner.md)]

```xpp
class Enumerator extends Object
```

## <a name="remarks"></a>備考

## <a name="examples"></a>例

## <a name="methods"></a>メソッド

| 方法                        | 説明                                          |
|-------------------------------|------------------------------------------------------|
| public AnyType current()      |                                                      |
| public str definitionString() |                                                      |
| public boolean moveNext()     |                                                      |
| public str toString()         | 現在のオブジェクトを表す文字列を返します。 |
| public void reset()           |                                                      |

## <a name="method-current"></a>メソッド current

```xpp
public AnyType current()
```

### <a name="return-value---current"></a>戻り値 - current

## <a name="method-definitionstring"></a>メソッド definitionString

```xpp
public str definitionString()
```

### <a name="return-value---definitionstring"></a>戻り値 - definitionString

## <a name="method-movenext"></a>メソッド moveNext

```xpp
public boolean moveNext()
```

### <a name="return-value---movenext"></a>戻り値 - moveNext

## <a name="method-tostring"></a>メソッド toString

現在のオブジェクトを表す文字列を返します。

```xpp
public str toString()
```

### <a name="return-value---tostring"></a>戻り値 - toString

現在のオブジェクトを表す文字列。

### <a name="remarks---tostring"></a>備考 - toString

既定の実装は、オブジェクトのクラス名を返します。 メソッドは派生クラスで上書きできるため、そのタイプの意味のある値が返されます。 たとえば、SysMethodInfo クラスのインスタンスは、インスタンスまたは静的などのメソッド名およびメソッドのタイプを返します。

## <a name="method-reset"></a>メソッド reset

```xpp
public void reset()
```

