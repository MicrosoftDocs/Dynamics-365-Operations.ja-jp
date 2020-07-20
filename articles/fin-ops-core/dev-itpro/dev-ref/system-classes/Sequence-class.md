---
title: Sequence クラス
description: このトピックでは、Sequence クラスについて説明します。
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
ms.openlocfilehash: 0e656a131b2058f8f155d42a4ace5bc578221894
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502806"
---
# <a name="class-sequence"></a>クラスの順序

[!include [banner](../../includes/banner.md)]

```xpp
class Sequence extends Object
```

Sequence クラスを使用すると、通常は何らかの順序または伝票番号の生成のために、主要なトランザクション スコープ外でトランザクションを実行できます。

## <a name="remarks"></a>備考

接続には、メインユーザー接続、補助システム接続、ユーザー接続の 3 種類があります。 最初のものはアプリケーション ロジック用に使用されます。 2 番目は、内部シーケンス番号の生成 (特に組み込みフィールド RecId) に使用されます。 3 番目はアプリケーションが別々の接続を維持するために使用されます。 このクラスは、番号生成のための補助システム接続へのインターフェイスを提供します。 ただし、これはアプリケーションの使用するメソッドまたは柔軟性、さらにカーネルの順序番号の生成で同時実行の問題を回避するため、UserConnection クラスを使用する方がより良いソリューションになる可能性があります。

## <a name="examples"></a>例

```xpp
static void example() 
{ 
    Sequence S = new Sequence("mySequence",1,100,10000); 
    print S.nextval(10);           // 100 in current company (the subkey) 
    print S.nextval(10);           // 110 in current company (the subkey) 
    print S.nextval(1,"MMM");      // 100 in subkey "MMM" 
    print S.nextval(1,"MMM");      // 101 in subkey "MMM" 
}
```

## <a name="methods"></a>メソッド

| 方法                                                                                                        | 説明                                                                                 |
|---------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| public Int64 currval(\[str Subkey1\], \[int Subkey2\])                                                        | カウンター値の増加なしで、シーケンスから現在の順序番号を取得します。 |
| public Int64 nextval(Int64 Increment, \[str Subkey1\], \[int Subkey2\])                                       | シーケンスから次の順序番号を返し、カウンター値を増分します。   |
| public void new(str Name, int Id, Int64 InitialValue, Int64 MaxValue, \[boolean Cycle\], \[Int64 CacheSize\]) | Object クラスの新しいインスタンスを初期化します。                                             |

## <a name="method-currval"></a>メソッド currval

カウンター値の増加なしで、シーケンスから現在の順序番号を取得します。

```xpp
public Int64 currval([str Subkey1], [int Subkey2])
```

### <a name="parameters---currval"></a>パラメーター - currval

Subkey1  

<!-- -->

Subkey2  

### <a name="return-value---currval"></a>戻り値 - currval

シーケンスの現在のシーケンス番号。

## <a name="method-nextval"></a>メソッド nextval

シーケンスから次の順序番号を返し、カウンター値を増分します。

```xpp
public Int64 nextval(Int64 Increment, [str Subkey1], [int Subkey2])
```

### <a name="parameters---nextval"></a>パラメーター - nextval

増分  

<!-- -->

Subkey1  

<!-- -->

Subkey2  

### <a name="return-value---nextval"></a>戻り値 - nextval

利用可能な次の順序番号。

## <a name="method-new"></a>メソッド new

Object クラスの新しいインスタンスを初期化します。

```xpp
public void new(str Name, int Id, Int64 InitialValue, Int64 MaxValue, [boolean Cycle], [Int64 CacheSize])
```

### <a name="parameters---new"></a>パラメーター - new

氏名  

<!-- -->

ID  

<!-- -->

InitialValue  

<!-- -->

MaxValue  

<!-- -->

サイクル  

<!-- -->

CacheSize  

