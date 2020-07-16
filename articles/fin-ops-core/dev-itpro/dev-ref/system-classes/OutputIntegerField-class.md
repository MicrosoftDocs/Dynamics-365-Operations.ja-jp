---
title: OutputIntegerField クラス
description: このトピックでは、OutputIntegerField クラスについて説明します。
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
ms.openlocfilehash: 06cfd2d27f24581ba7b8e267705dd0f4c8baddd3
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502548"
---
# <a name="class-outputintegerfield"></a>クラス OutputIntegerField

[!include [banner](../../includes/banner.md)]

```xpp
class OutputIntegerField extends OutputField
```

## <a name="remarks"></a>備考

## <a name="examples"></a>例

## <a name="methods"></a>メソッド

| 方法                        | 説明                                                 |
|-------------------------------|-------------------------------------------------------------|
| public int displaceNegative() |                                                             |
| public boolean negative()     |                                                             |
| public str toString()         | 現在のオブジェクトを表す文字列を返します。        |
| public int value()            |                                                             |
| public void new()             | OutputIntegerField クラスの新しいインスタンスを初期化します。 |

## <a name="method-displacenegative"></a>メソッド displaceNegative

```xpp
public int displaceNegative()
```

### <a name="return-value---displacenegative"></a>戻り値 - displaceNegative

## <a name="method-negative"></a>メソッド negative

```xpp
public boolean negative()
```

### <a name="return-value---negative"></a>戻り値 - negative

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

OutputIntegerField クラスの新しいインスタンスを初期化します。

```xpp
public void new()
```

