---
title: Random クラス
description: このトピックでは、Random クラスについて説明します。
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
ms.openlocfilehash: e2203d2f8d3ecfb952e5a77e2cb4d5077115ad45
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502857"
---
# <a name="class-random"></a>クラス ランダム

[!include [banner](../../includes/banner.md)]


```xpp
class Random extends Object
```

Random クラスは、ランダムな番号を生成します。

## <a name="remarks"></a>備考

このクラスはグローバル ランダム ジェネレーターで機能するため、個々のランダム オブジェクトは相互に干渉します。 したがって、特定のランダム オブジェクトの数列を予測することはできません。

## <a name="examples"></a>例

次の例では、100 個のランダムな番号を出力します。

```xpp
static void example() 
{ 
    Random myRand = new Random(); 
    int i; 
    for(i=0;i<100;i++) 
    { 
        print myRand.nextInt(); 
    } 
}
```

## <a name="methods"></a>メソッド

| 方法               | 説明                                               |
|----------------------|-----------------------------------------------------------|
| public int nextInt() | ランダム ジェネレーターの次のランダムな数を返します。 |
| public void new()    | Random クラスの新しいインスタンスを初期化します。           |

## <a name="method-nextint"></a>メソッド nextInt

ランダム ジェネレーターの次のランダムな数を返します。

```xpp
public int nextInt()
```

### <a name="return-value---nextint"></a>戻り値 - nextInt

ランダム ジェネレーターの次のランダムな整数。

### <a name="remarks---nextint"></a>備考 - nextInt

値は 0 〜 32767 (0x7FFF) の範囲内になります。

## <a name="method-new"></a>メソッド new

Random クラスの新しいインスタンスを初期化します。

```xpp
public void new()
```

