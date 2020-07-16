---
title: PerformanceMonitorCounter クラス
description: このトピックでは、PerformanceMonitorCounter クラスについて説明します。
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
ms.openlocfilehash: 4d897956c7f0f5793987cdb40419aa6235f36f7d
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502538"
---
# <a name="class-performancemonitorcounter"></a>クラス PerformanceMonitorCounter

[!include [banner](../../includes/banner.md)]

```xpp
class PerformanceMonitorCounter extends Object
```

PerformanceMonitorCounter クラスでは、特定のスナップショットの特定のインスタンスに割り当てられているカウンターを識別します。

## <a name="remarks"></a>備考

get メソッドを使用してデータを取得できます。

## <a name="examples"></a>例

## <a name="methods"></a>メソッド

| 方法                 | 説明                                                                                    |
|------------------------|------------------------------------------------------------------------------------------------|
| public int intData()   |                                                                                                |
| public str name()      |                                                                                                |
| public Time timeData() |                                                                                                |
| public str toString()  | クラス ハンドルと名前、および場合によっては追加情報を含む文字列を返します。 |

## <a name="method-intdata"></a>メソッド intData

```xpp
public int intData()
```

### <a name="return-value---intdata"></a>戻り値 - intData

## <a name="method-name"></a>メソッド名

```xpp
public str name()
```

### <a name="return-value---name"></a>戻り値 - name

## <a name="method-timedata"></a>メソッド timeData

```xpp
public Time timeData()
```

### <a name="return-value---timedata"></a>戻り値 - timeData

## <a name="method-tostring"></a>メソッド toString

クラス ハンドルと名前、および場合によっては追加情報を含む文字列を返します。

```xpp
public str toString()
```

### <a name="return-value---tostring"></a>戻り値 - toString

クラスのテキストの説明。

### <a name="remarks---tostring"></a>備考 - toString

既定では、ほとんどのクラスは、toString メソッドがクラス ハンドルおよび名前を含む文字列を返します。 ただし、一部のクラスでは、追加情報が文字列で返されます。

