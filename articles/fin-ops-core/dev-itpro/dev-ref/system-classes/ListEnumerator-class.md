---
title: ListEnumerator クラス
description: このトピックでは、ListEnumerator クラスについて説明します。
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
ms.openlocfilehash: 8ecc0c940718a0de4f30660c0eaf8cf28f79e955
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502590"
---
# <a name="class-listenumerator"></a>クラス ListEnumerator

[!include [banner](../../includes/banner.md)]

```xpp
class ListEnumerator extends Object
```

ListEnumerator クラスを使用すると、一覧内の要素上を移動できます。

## <a name="remarks"></a>備考

リストの列挙子は、リストの最初の要素の前に開始します。 リストの最初の要素を指すようにするために ListEnumerator.moveNext メソッドを呼び出す必要があります。 list.getEnumerator メソッドが呼び出されたときに、リストと同じ層で列挙子が自動的に作成されるため、ListIterator クラスではなく、ListEnumerator クラスを使用することがベスト プラクティスです。 これにより、Caller from としてマークされたコードの潜在的な問題を回避します。反復子とリストは別々の層に置くことができます。 さらに、リスト列挙子はリスト反復子よりも少ないコードを必要とするためパフォーマンスが少し向上します。 リスト反復子を使用する必要がある唯一の状況は、リストから項目を削除する場合です (ListIterator.delete メソッドを使用します)。

## <a name="examples"></a>例

次の例では、整数のリストを作成し、いくつかの値をその中に入れます。 その後、列挙子を作成し、一覧の最初の要素、一覧の 2 番目の要素に列挙子を設定します。

```xpp
{ 
    List list = new List(Types::Integer); 
    ListEnumerator enumerator; 
    // Add some elements to the list 
    list.addEnd(1); 
    list.addEnd(2); 
    list.addStart(3); 
    // Set the enumerator 
    enumerator = list.getEnumerator(); 
    // Print a description of the list 
    print enumerator.definitionString(); 
    // Go to beginning of enumerator 
    enumerator.reset(); 
    //Go to the first element in the List 
    enumerator.moveNext(); 
    // Print contents of first and second elements 
    // First element is 3 as this was added to start of list 
    print enumerator.toString(); 
    enumerator.moveNext(); 
    print enumerator.toString(); 
    pause; 
}
```

## <a name="methods"></a>メソッド

| 方法                        | 説明                                                                                                   |
|-------------------------------|---------------------------------------------------------------------------------------------------------------|
| public AnyType current()      | 列挙子によりポイントされている値を取得します。                                                     |
| public str definitionString() | 列挙子の説明を返します。                                                                      |
| public boolean moveNext()     | 列挙子が有効なリスト要素を示すかどうかを決定します。                                               |
| public str toString()         | 列挙子が現在ポイントしているリスト内の要素の内容の説明を返します。 |
| public void reset()           | 列挙子をリストの先頭に移動します。                                                                |

## <a name="method-current"></a>メソッド current

列挙子によりポイントされている値を取得します。

```xpp
public AnyType current()
```

### <a name="return-value---current"></a>戻り値 - current

リスト内で現在指定されている値。 戻り値のタイプは、リスト内の項目のタイプによって決まります。

### <a name="examples---current"></a>例 - current

次の例では、リストを反復処理し、dimensionTopic 変数を現在のリスト要素の値に設定します。

```xpp
public DimensionTopic firstDimensionTopic() 
{ 
    DimensionTopic  dimensionTopic; 
    ListEnumerator  enumerator; 
    enumerator = this.getTopicsEnumerator(); 
    if (enumerator.moveNext()) 
    { 
        dimensionTopic = enumerator.current(); 
    } 
    return dimensionTopic; 
}
```

## <a name="method-definitionstring"></a>メソッド definitionString

列挙子の説明を返します。

```xpp
public str definitionString()
```

### <a name="return-value---definitionstring"></a>戻り値 - definitionString

列挙子の説明を含む文字列。

### <a name="remarks---definitionstring"></a>備考 - definitionString

たとえば、整数のリストの列挙子は、int リスト列挙子を返します。

### <a name="examples---definitionstring"></a>例 - definitionString

次の例では、リストとそのリストの列挙子を作成します。 definitionString メソッドを使用して、列挙子の説明を出力します。

```xpp
{ 
    List list = new List(Types::Integer); 
    ListEnumerator  enumerator; 
    ; 
    // Add some elements to the list 
    list.addEnd(1); 
    list.addEnd(2); 
    list.addStart(3); 
    // Set the enumerator 
    enumerator = list.getEnumerator(); 
    print enumerator.definitionString(); 
    pause; 
}
```

## <a name="method-movenext"></a>メソッド moveNext

列挙子が有効なリスト要素を示すかどうかを決定します。

```xpp
public boolean moveNext()
```

### <a name="return-value---movenext"></a>戻り値 - moveNext

リスト内の現在の職位が有効な要素を保持している場合は true。それ以外の場合は、false。

### <a name="remarks---movenext"></a>備考 - moveNext

リストの列挙子は、リストの最初の要素の前に開始します。 リストの最初の要素を指すようにするために moveNext メソッドを呼び出す必要があります。

### <a name="examples---movenext"></a>例 - moveNext

次の例では、moveNext メソッドを使用してリスト内に別の要素があるかどうかを確認し、dimensionTopic 変数を現在のリスト要素の値に設定します。

```xpp
public DimensionTopic firstDimensionTopic() 
{ 
    DimensionTopic  dimensionTopic; 
    ListEnumerator  enumerator; 
    enumerator = this.getTopicsEnumerator(); 
    if (enumerator.moveNext()) 
    { 
        dimensionTopic = enumerator.current(); 
    } 
    return dimensionTopic; 
}
```

## <a name="method-tostring"></a>メソッド toString

列挙子が現在ポイントしているリスト内の要素の内容の説明を返します。

```xpp
public str toString()
```

### <a name="return-value---tostring"></a>戻り値 - toString

現在のリスト要素の説明を含む文字列。

### <a name="examples---tostring"></a>例 - toString

次の例では、リストを作成し、最初の要素と 2 番目の要素の内容をリストに出力します。

```xpp
{ 
    List list = new List(Types::Integer); 
    ListEnumerator  enumerator; 
    // Add some elements to the list 
    list.addEnd(1); 
    list.addEnd(2); 
    list.addStart(3); 
    // Set the enumerator 
    enumerator = list.getEnumerator(); 
    // Go to beginning of enumerator 
    enumerator.reset(); 
    //Go to the first element in the List 
    enumerator.moveNext(); 
    // First element is 3 as this was added to start of list 
    print enumerator.toString(); 
    pause; 
    enumerator.moveNext(); 
    //Print second element in list (1) 
    print enumerator.toString(); 
    pause; 
}
```

## <a name="method-reset"></a>メソッド reset

列挙子をリストの先頭に移動します。

```xpp
public void reset()
```

### <a name="remarks---reset"></a>備考 - reset

reset メソッドは、列挙子をリストの先頭、リストの最初の要素の前に移動します。 リストの最初の要素を指すようにするために ListEnumerator.moveNext メソッドを呼び出す必要があります。

### <a name="examples---reset"></a>例 - reset

次の例では、リストを作成し、そのリストの列挙子を作成します。 reset メソッドを使用して一覧の先頭に移動し、moveNext メソッドを使用して一覧の最初の要素に移動します。

```xpp
{ 
    List list = new List(Types::Integer); 
    ListEnumerator  enumerator; 
    // Add some elements to the list 
    list.addEnd(1); 
    list.addEnd(2); 
    list.addStart(3); 
    // Set the enumerator 
    enumerator = list.getEnumerator(); 
    // Go to beginning of enumerator 
    enumerator.reset(); 
    //Go to the first element in the List 
    enumerator.moveNext(); 
    // First element is 3 as this was added to start of list 
    print enumerator.toString(); 
    pause; 
}
```

