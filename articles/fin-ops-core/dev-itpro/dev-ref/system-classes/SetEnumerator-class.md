---
title: SetEnumerator クラス
description: このトピックでは、SetEnumerator クラスについて説明します。
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
ms.openlocfilehash: 6ddb5f3118ccd221df0c3ad81a315b14d4b48e03
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502804"
---
# <a name="class-setenumerator"></a>クラス SetEnumerator

[!include [banner](../../includes/banner.md)]

```xpp
class SetEnumerator extends Object
```

SetEnumerator クラスを使用すると、セット内の要素上を移動できます。

## <a name="remarks"></a>備考

セット列挙子は、セットの最初の要素の前に開始します。 セットの最初の要素を指すようにするために SetEnumerator.moveNext メソッドを呼び出す必要があります。 ベスト プラクティスとしては、set.getEnumerator メソッドが呼び出されたときに、設定されている同じ層で列挙子が自動的に作成されるため、SetIterator クラスではなく、SetEnumerator クラスを使用します。 これにより、Caller from としてマークされたコードの潜在的な問題を回避できます。反復子とセットは別々の層に置くことができます。 さらに、セット列挙子はセット反復子よりも少ないコードを必要とするためパフォーマンスが少し向上します。

## <a name="examples"></a>例

## <a name="methods"></a>メソッド

| 方法                        | 説明                                                                                                |
|-------------------------------|------------------------------------------------------------------------------------------------------------|
| public AnyType current()      | 列挙子によりポイントされている値を取得します。                                                  |
| public str definitionString() | 列挙子の説明を返します。                                                                   |
| public boolean moveNext()     | 列挙子が有効なセット要素を示すかどうかを決定します。                                             |
| public str toString()         | 列挙子が現在ポイントしているセット内の要素の内容の説明を取得します。 |
| public void reset()           | 列挙子をセットの先頭に移動します。                                                              |

## <a name="method-current"></a>メソッド current

列挙子によりポイントされている値を取得します。

```xpp
public AnyType current()
```

### <a name="return-value---current"></a>戻り値 - current

セット内で現在指定されている値。

### <a name="remarks---current"></a>備考 - current

戻り値のタイプは、セット内の項目のタイプによって決まります。 現在のメソッドを呼び出す前に、SetEnumerator.moveNext メソッドを呼び出す必要があります。

## <a name="method-definitionstring"></a>メソッド definitionString

列挙子の説明を返します。

```xpp
public str definitionString()
```

### <a name="return-value---definitionstring"></a>戻り値 - definitionString

列挙子の説明を含む文字列。

### <a name="remarks---definitionstring"></a>備考 - definitionString

たとえば、整数のセットの列挙子は、int セット列挙子を返します。

### <a name="examples---definitionstring"></a>例 - definitionString

次の例では、セットとそのセットの列挙子を作成します。 definitionString メソッドを使用して、列挙子の説明を出力します。

```xpp
{ 
    Set mySet = new Set(Types::Integer); 
    SetEnumerator enumerator; 
    int i; 
    // Add some elements to the set. 
   for (i = 0; i < 10; i++) 
    { 
        mySet.add(i); 
    } 
    // Set the enumerator. 
    enumerator = mySet.getEnumerator(); 
    print enumerator.definitionString(); 
    pause; 
}
```

## <a name="method-movenext"></a>メソッド moveNext

列挙子が有効なセット要素を示すかどうかを決定します。

```xpp
public boolean moveNext()
```

### <a name="return-value---movenext"></a>戻り値 - moveNext

セット内の現在の職位が有効な要素を保持している場合は true。それ以外の場合は、false。

### <a name="remarks---movenext"></a>備考 - moveNext

セット列挙子は、セットの最初の要素の前に開始します。 セットの最初の要素を指すようにするために moveNext メソッドを呼び出す必要があります。

## <a name="method-tostring"></a>メソッド toString

列挙子が現在ポイントしているセット内の要素の内容の説明を取得します。

```xpp
public str toString()
```

### <a name="return-value---tostring"></a>戻り値 - toString

設定の現在の要素の説明を含む文字列。

### <a name="examples---tostring"></a>例 - toString

次の例では、整数のセットを作成し、最初の要素と 2 番目の要素の内容をセットに出力します。

```xpp
{ 
    Set mySet = new Set(Types::Integer); 
    SetEnumerator  enumerator; 
    int i; 
     // Add some elements to the set. 
    for (i = 0; i < 10; i++) 
    { 
        mySet.add(i); 
    } 
    // Set the enumerator. 
    enumerator = mySet.getEnumerator(); 
    // Go to the beginning of the enumerator. 
    enumerator.reset(); 
    // Go to the first element in the set. 
    enumerator.moveNext(); 
    // Print the first item in the set. 
    print enumerator.toString(); 
    pause; 
    enumerator.moveNext(); 
    // Print the second element in the set. 
    print enumerator.toString(); 
    pause; 
}
```

## <a name="method-reset"></a>メソッド reset

列挙子をセットの先頭に移動します。

```xpp
public void reset()
```

### <a name="remarks---reset"></a>備考 - reset

reset メソッドは、列挙子をセットの先頭、セットの最初の要素の前に移動します。 セットの最初の要素を指すようにするために SetEnumerator.moveNext メソッドを呼び出す必要があります。

### <a name="examples---reset"></a>例 - reset

次の例では、セット作成し、そのセットの列挙子を作成します。 reset メソッドを使用してセットの先頭に移動し、moveNext メソッドを使用してセットの最初の要素に移動します。

```xpp
{ 
    Set mySet = new Set(Types::Integer); 
    SetEnumerator  enumerator; 
    int i; 
     // Add some elements to the set. 
    for (i = 0; i < 10; i++) 
    { 
        mySet.add(i); 
    } 
    // Set the enumerator. 
    enumerator = mySet.getEnumerator(); 
    // Go to beginning of enumerator. 
    enumerator.reset(); 
    // Go to the first element in the set. 
    enumerator.moveNext(); 
    // Print the first item in the set. 
    print enumerator.toString(); 
    pause; 
}
```

