---
title: NumberSequence クラス
description: このトピックでは、SecurityPolicy クラスについて説明します。
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
ms.openlocfilehash: b9c14759063527bce8fa04af114ddcaf76d7704b
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502568"
---
# <a name="class-numbersequence"></a>クラス NumberSequence

[!include [banner](../../includes/banner.md)]


```xpp
class NumberSequence extends Object
```

## <a name="remarks"></a>備考

## <a name="examples"></a>例

## <a name="methods"></a>メソッド

| 方法                                                                                                                                                                | 説明                                             |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------|
| ::public static int getNextNumber(Connection connection, Int64 numbersequencerecordid, Int64 globaltransid, str userid, int sessionid, DateTime sessionLoginDateTime) |                                                         |
| public void new()                                                                                                                                                     | NumberSequence クラスの新しいインスタンスを初期化します。 |

## <a name="method-getnextnumber"></a>メソッド getNextNumber

```xpp
public static int getNextNumber(Connection connection, Int64 numbersequencerecordid, Int64 globaltransid, str userid, int sessionid, DateTime sessionLoginDateTime)
```

### <a name="parameters---getnextnumber"></a>パラメーター - getNextNumber

connection  

<!-- -->

numbersequencerecordid  

<!-- -->

globaltransid  

<!-- -->

userid  

<!-- -->

sessionid  

<!-- -->

sessionLoginDateTime  

### <a name="return-value---getnextnumber"></a>返り値 - getNextNumber

## <a name="method-new"></a>メソッド new

NumberSequence クラスの新しいインスタンスを初期化します。

```xpp
public void new()
```

