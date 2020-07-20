---
title: ListIterator クラス
description: このトピックでは、ListIterator クラスについて説明します。
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
ms.openlocfilehash: d4e2364ef151f377418ab1225df7e01a6bbe5192
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502894"
---
# <a name="class-listiterator"></a>クラス ListIterator

[!include [banner](../../includes/banner.md)]

```xpp
class ListIterator extends Object
```

ListIterator クラスは、一覧内の要素を反復処理するために使用されます。

## <a name="remarks"></a>備考

リストの反復子は、反復処理する対象となるリストにポインターとして表示することができます。 繰り返しを開始する機能は利用可能であり、より多くの要素が利用可能であるかどうかを決定し、繰り返しによりポイントされる要素をフェッチします。 繰り返し中に要素が発生する順序は、要素が挿入される順序によって定義されます。 要素を挿入するには、List.addStart、List.addEnd、または ListIterator.insert メソッドを使用します。 ListIterator クラスよりも ListEnumerator クラスを使用することをお勧めします。 反復処理するリストの反復子およびマップは、同じクライアント/サーバー側にある必要があります。 ListIterator クラスを使用し、コードが Called from としてマークされている場合、リストと反復子が別の層で終了する可能性があります。 この場合、コードは失敗します。 ListEnumerator クラスを使用する場合、列挙子はリストと同じ層に自動的に作成されます。 また、リスト内の次のアイテムに移動するには、反復子リストを使用している場合は、より多くのメソッドと次のメソッドを明示的に呼び出す必要があります。 ListEnumerator クラスを使用する場合、moveNext メソッドを呼び出すだけです。 リスト列挙子を使用できない唯一の状況は、リストから要素を削除する必要がある場合です。 詳細については、「メソッドの削除」を参照してください。

## <a name="examples"></a>例

次の例では、リストとそれを指す反復子を作成します。 ListIterator クラスのさまざまなメソッドを使用して、一覧の説明と一覧内の項目を出力します。

```xpp
{ 
    List il = new List(types::Integer); 
    ListIterator it; 
    // Add some elements into the list. 
    il.addStart(1); 
    il.addStart(2); 
    il.addStart(4);  
    // Create a list iterator to traverse the values. 
    it = new ListIterator (il);  
    // Prints "int list iterator". 
    print it.definitionString();  
    // Prints "(begin)[4]". 
    print it.toString();  
    // Go on for as long as elements are found in the list. 
    // Prints 4, 2, 1. 
    while (it.more()) 
    { 
        print it.value(); 
        it.next(); 
    } 
    // Prints (end). 
    print it.toString(); 
    pause; 
}
```

## <a name="methods"></a>メソッド

| 方法                               | 説明                                                                                    |
|--------------------------------------|------------------------------------------------------------------------------------------------|
| public str definitionString()        | 反復子のタイプのテキスト表現を返します。                                  |
| public AnyType insert(AnyType value) | 反復子が現在ポイントしているリスト内の位置に新しい値を挿入します。         |
| public boolean more()                | リスト反復子が有効な要素を指しているかどうかを判定します。                                |
| public str toString()                | 反復子によりポイントされている現在のリスト値のテキスト形式を返します。 |
| public AnyType value()               | 反復子によりポイントされている値を取得します。                                        |
| public void begin()                  | 反復子をリストの先頭に移動します。                                                   |
| public void next()                   | リストで次の要素に反復子を移動します。                                            |
| public void end()                    | リストで最後の要素の後に反復子を移動します。                                          |
| public void delete()                 | 反復子によってポイントされている要素を一覧から削除します。                          |
| public void new(List list)           | 特定のリストに対する新しい反復子を作成します。                                                  |

## <a name="method-definitionstring"></a>メソッド definitionString

反復子のタイプのテキスト表現を返します。

```xpp
public str definitionString()
```

### <a name="return-value---definitionstring"></a>戻り値 - definitionString

反復子のタイプを含む文字列。

### <a name="remarks---definitionstring"></a>備考 - definitionString

例: int リスト反復子。

## <a name="method-insert"></a>メソッド insert

反復子が現在ポイントしているリスト内の位置に新しい値を挿入します。

```xpp
public AnyType insert(AnyType value)
```

### <a name="parameters---insert"></a>パラメーター - insert

値  
リストに挿入する項目の値。

### <a name="return-value---insert"></a>戻り値 - insert

リストに挿入された値。

### <a name="remarks---insert"></a>備考 - insert

value パラメーターは、リストと同じタイプである必要があります。

### <a name="examples---insert"></a>例 - insert

次の例では、10 個のアイテムを持つリストを作成し、ListIterator.insert メソッドを使用してリスト内の 3 番目のアイテムとして新しい値を挿入します。

```xpp
{ 
    List il = new List(Types::Integer); 
    ListIterator it; 
    int i; 
    int j = 25; 
    // Insert values 1 to 10 into the list 
    for (i = 1; i <= 10; i++) 
    { 
        il.addEnd(i); 
    } 
    // Go to the 3rd element in the list 
    it = new ListIterator(il); 
    it.begin(); 
    it.next(); 
    it.next(); 
    // Insert a new value (25) 
    it.insert(j); 
  it.begin(); 
    // Print all values in the list. 
    // 25 is the third value in the list 
    while (it.more()) 
    { 
        print it.value(); 
        it.next();  
    } 
    pause; 
}
```

## <a name="method-more"></a>メソッド more

リスト反復子が有効な要素を指しているかどうかを判定します。

```xpp
public boolean more()
```

### <a name="return-value---more"></a>戻り値 - more

リスト反復子が有効な要素を指定する場合は true。それ以外の場合は、false。

### <a name="remarks---more"></a>備考 - more

このメソッドが false を返すときに要素にアクセスしようとするとエラーが発生します。

### <a name="examples---more"></a>例 - more

次の例では、ListIterator.more メソッドを使用してリストに要素があるかどうかを確認し、リスト内のすべての要素の値を出力する while ループを実行します。

```xpp
{ 
    List il = new List(Types::Integer); 
    ListIterator it; 
    int i; 
    // Add some elements 
    for (i = 1; i <= 10; i++) 
    { 
        il.addEnd(i); 
    } 
    // Traverse the list 
    it = new ListIterator(il); 
    while (it.more()) 
    { 
        print it.value(); 
        it.next(); // Skip to the next element 
    } 
    pause; 
}
```

## <a name="method-tostring"></a>メソッド toString

反復子によりポイントされている現在のリスト値のテキスト形式を返します。

```xpp
public str toString()
```

### <a name="return-value---tostring"></a>戻り値 - toString

現在の値の説明を含む文字列。

### <a name="remarks---tostring"></a>備考 - toString

反復子がリスト内の最初の要素を指している場合、文字列には "(開始)\[値\]" という形式の文字列が含まれます。反復子が要素を指していない場合 (つまり、more() メソッドが false を返す場合)、返される次の文字列は: (終了) になります。 反復子が値をポイントしている場合、文字列は "\[値\]" で、値が要素値の文字列表現です。

### <a name="examples---tostring"></a>例 - toString

次の例では、リスト内の 2 つの値の値の説明を表示します。

1.  (開始) \[2\]
2.  \[1\]

<!-- -->

```xpp
{ 
    List li = new List(Types::Integer); 
    ListIterator it = new ListIterator(li); 
    li.addStart(1); 
    li.addStart(2); // This is now the first value 
    it.begin(); 
    print it.toString(); 
    it.next(); 
    print it.toString(); 
    pause; 
}
```

## <a name="method-value"></a>メソッド value

反復子によりポイントされている値を取得します。

```xpp
public AnyType value()
```

### <a name="return-value---value"></a>戻り値 - value

反復子によりポイントされている値。

### <a name="remarks---value"></a>備考 - value

リスト要素の値を取得する前に、ListIterator.more メソッドを使用して要素が存在するかどうかをテストします。

## <a name="method-begin"></a>メソッド begin

反復子をリストの先頭に移動します。

```xpp
public void begin()
```

## <a name="method-next"></a>メソッド next

リストで次の要素に反復子を移動します。

```xpp
public void next()
```

### <a name="remarks---next"></a>備考 - next

ListIterator.more メソッドを使用して、反復子が有効な要素を指しているかどうかを判断します。

### <a name="examples---next"></a>例 - next

次の例では、ListIterator.next メソッドを使用して、各要素の値が出力されるときにリストをスキャンします。

```xpp
{ 
    List il = new List(Types::Integer); 
    ListIterator it; 
    int i; 
    // Add some elements 
    for (i = 1; i <= 10; i++) 
    { 
        il.addEnd(i); 
    } 
    // Traverse the list 
    it = new ListIterator(il); 
    while (it.more()) 
    { 
        print it.value(); 
        // Move to the next element 
        it.next();  
    } 
    pause; 
}
```

## <a name="method-end"></a>メソッド end

リストで最後の要素の後に反復子を移動します。

```xpp
public void end()
```

### <a name="remarks---end"></a>備考 - end

このメソッドが実行すると、ListIterator.more メソッドが false に戻ります。

## <a name="method-delete"></a>メソッド delete

反復子によってポイントされている要素を一覧から削除します。

```xpp
public void delete()
```

### <a name="remarks---delete"></a>備考 - delete

反復子は、この削除の後に次の要素を指します。

### <a name="examples---delete"></a>例 - delete

次の例では、3 つの要素を含むリストを作成し、リスト内の要素の説明を出力します。 一覧の最初の要素を削除し、残りの要素の説明を印刷します。

```xpp
{ 
    List li = new List(Types::Integer); 
    ListIterator it; 
    li.addStart(1); 
    li.addStart(2); 
    li.addStart(3); 
    print li.toString(); 
    it = new ListIterator(li); 
    it.delete(); 
    print li.toString(); 
    pause; 
}
```

## <a name="method-new"></a>メソッド new

特定のリストに対する新しい反復子を作成します。

```xpp
public void new(List list)
```

### <a name="parameters---new"></a>パラメーター - new

リスト  
反復子を作成するリスト。

### <a name="remarks---new"></a>備考 - new

反復子は、リストが空でない場合、リストの最初の値に配置されます。 反復子および繰り返すリストは、同じクライアント/サーバー側にする必要があります。

### <a name="examples---new"></a>例 - new

次の例では、整数リストの反復子を作成します。

```xpp
List il = new List(types::Integer); 
ListIterator it; 
it = new ListIterator (il);
```

