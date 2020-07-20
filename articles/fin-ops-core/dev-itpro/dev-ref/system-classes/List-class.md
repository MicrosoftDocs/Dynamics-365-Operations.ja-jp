---
title: 'List クラス '
description: このトピックでは、List クラスについて説明します。
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
ms.openlocfilehash: 17ff9ba3b027514d00a0dc69fbb9fc67348b461b
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502898"
---
# <a name="class-list"></a>クラス リスト

[!include [banner](../../includes/banner.md)]

```xpp
class List extends Object
```

順にアクセスされる任意の数の要素を含みます。 リストは、あらゆる X++ 型の値を含めることができる構造です。 リスト内のすべての値は同じタイプである必要があります。

## <a name="remarks"></a>備考

リスト内の値のタイプは、リストが作成されたときに指定され、後で変更することはできません。 リストの実装は、リスト要素のトラバーサルを非常に高速にします。 リストを移動するには、ListEnumerator クラスを使用します。 ListEnumerator オブジェクトを作成するには、List.getEnumerator を使用します。

## <a name="examples"></a>例

次の例では、整数のリストを作成し、リストの説明とそれに含まれる値を出力します。

```xpp
{ 
    // Create a list of integers 
    List il = new List(Types::Integer); 
    // Add some elements to the list 
    il.addEnd(1); 
    il.addEnd(2); 
    il.addStart(3); 
    // Print a description of the list 
    print il.definitionString(); 
    print il.toString(); 
    pause; 
}
```

## <a name="methods"></a>メソッド

| 方法                                                | 説明                                                                           |
|-------------------------------------------------------|---------------------------------------------------------------------------------------|
| public AnyType addEnd(AnyType element)                | リストの末尾に値を追加します。                                                  |
| public AnyType addStart(AnyType element)              | リストの冒頭に値を追加します。                                                |
| public str definitionString()                         | リスト内のすべての要素のタイプの説明を返します。                        |
| public int elements()                                 | リスト内の要素の数を指定します。                                           |
| public boolean empty()                                | 一覧が空であるかどうかを判定します。                                                   |
| public boolean equalTo(List l)                        | 一覧が現在の一覧と同じかどうかを判定します。                            |
| public ListEnumerator getEnumerator()                 | リストのスキャンを可能にするリストの列挙子を作成します。               |
| public container pack()                               | List クラスの現在のインスタンスをシリアル化します。                                    |
| public str toString()                                 | リスト内の値の説明を返します。                                      |
| public Types typeId()                                 | リスト内の値のタイプを返します。                                             |
| public str xml(\[int indent\])                        | 現在のオブジェクトを表す XML 文字列を返します。                             |
| ::public static List create(container container)      | 以前の List.pack メソッドの呼び出しで取得したコンテナーからリストを作成します。 |
| ::public static List createFromXML(Object xmlnode)    |                                                                                       |
| ::public static boolean equal(List list1, List list2) | 2 つのリストが同じかどうかを判定します。                                           |
| ::public static List merge(List list1, List list2)    | 2 つのリストを組み合わせ、新しいリストを作成します。                                              |
| public void appendList(List list)                     |                                                                                       |
| public void new(Types Type)                           | リストを作成します。                                                                       |

## <a name="method-addend"></a>メソッド addEnd

リストの末尾に値を追加します。

```xpp
public AnyType addEnd(AnyType element)
```

### <a name="parameters---addend"></a>パラメーター - addEnd

要素  
リストの末尾に追加する値。

### <a name="return-value---addend"></a>戻り値 - addEnd

リストに追加される値。

## <a name="method-addstart"></a>メソッド addStart

リストの冒頭に値を追加します。

```xpp
public AnyType addStart(AnyType element)
```

### <a name="parameters---addstart"></a>パラメーター - addStart

要素  
リストの冒頭に追加する値。

### <a name="return-value---addstart"></a>戻り値 - addStart

このリストに追加される値。

### <a name="remarks---addstart"></a>備考 - addStart

要素は、List.addEnd メソッドを使用して、リストの最後に追加できます。

### <a name="examples---addstart"></a>例 - addStart

次の例では、整数のリストを作成し、値の 1 と 2 をリストの末尾に追加し、値 3 をリストの先頭に追加します。 List.toString メソッドによって返される値は {3, 1, 2} です。

```xpp
{ 
    // Create a list of integers 
    list il = new List(Types::Integer); 
    // Add some elements to the list 
    il.addEnd(1); 
    il.addEnd(2); 
    il.addStart(3); 
    // Print a description of the list. 
    print il.definitionString(); 
    print il.toString(); 
    pause; 
}
```

## <a name="method-definitionstring"></a>メソッド definitionString

リスト内のすべての要素のタイプの説明を返します。

```xpp
public str definitionString()
```

### <a name="return-value---definitionstring"></a>戻り値 - definitionString

リストの定義を含む文字列。

### <a name="remarks---definitionstring"></a>備考 - definitionString

たとえば、このメソッドは、「int の一覧」を返すことができます。 リスト内の値の一覧を印刷するには、List.toString メソッドを使用します。

### <a name="examples---definitionstring"></a>例 - definitionString

次の例では、整数のリストを作成します。 definitionString メソッドを使用して、リストの説明を出力します。

```xpp
{ 
    // Create a list of integers 
    List il = new List(Types::Integer); 
    // Add some elements to the list 
    il.addEnd(1); 
    il.addEnd(2); 
    il.addStart(3); 
    // Print a description ofvthe list 
    print il.definitionString(); 
    print il.toString(); 
    pause; 
}
```

## <a name="method-elements"></a>メソッド elements

リスト内の要素の数を指定します。

```xpp
public int elements()
```

### <a name="return-value---elements"></a>戻り値 - elements

リスト内の要素の数。

### <a name="examples---elements"></a>例 - elements

次の例では、整数のリストを作成し、いくつかの要素を追加します。 要素メソッドは、リストに 3 つの要素があるかどうかをテストするために使用されます。

```xpp
{ 
    List il = new List(Types::Integer); 
    il.addStart(1); 
    il.addStart(2); 
    il.addStart(3); 
    if (il.elements() != 3) 
    { 
        print "Something is wrong..."; 
    } 
}
```

## <a name="method-empty"></a>メソッド empty

一覧が空であるかどうかを判定します。

```xpp
public boolean empty()
```

### <a name="return-value---empty"></a>戻り値 - empty

リストが空の場合は true。それ以外の場合は、false。

## <a name="method-equalto"></a>メソッド equalTo

一覧が現在の一覧と同じかどうかを判定します。

```xpp
public boolean equalTo(List l)
```

### <a name="parameters---equalto"></a>パラメーター - equalTo

l  
現在のリストと比較されるリスト。

### <a name="return-value---equalto"></a>戻り値 - equalTo

指定したリストが、メソッドが呼び出されたリストと同一である場合は true。それ以外の場合は、false。

### <a name="remarks---equalto"></a>備考 - equalTo

2 つのリストが同じ型の場合、リストは別のリストと等しくなり、要素の同じ番号を含み、同じ順序で要素が発生します。 equalTo メソッドは、List.equal メソッドを使用するためのショートカットです。(this、l) と等しい。

## <a name="method-getenumerator"></a>メソッド getEnumerator

リストのスキャンを可能にするリストの列挙子を作成します。

```xpp
public ListEnumerator getEnumerator()
```

### <a name="return-value---getenumerator"></a>戻り値 - getEnumerator

現在のリストの listEnumerator オブジェクト。

## <a name="method-pack"></a>メソッド pack

List クラスの現在のインスタンスをシリアル化します。

```xpp
public container pack()
```

### <a name="return-value---pack"></a>戻り値 - pack

List クラスの現在のインスタンスを含むコンテナーです。

### <a name="remarks---pack"></a>備考 - pack

このメソッドで作成されたコンテナーには、リストの最初の要素の前に 3 つの要素が含まれます。

-   コンテナのバージョン番号
-   リスト要素のデータ型を識別する整数
-   リスト内の要素の数。

リスト内の要素がオブジェクトとなっている場合は、梱包は、各オブジェクトに対して pack メソッドを連続して呼び出し、サブコンテナーを取得することによって行われます。 List.create メソッドを使用して、パックされたコンテナーからリストを取得できます。

### <a name="examples---pack"></a>例 - pack

次の例では、レコードのリストを作成し、新しい projReverseMarking オブジェクトを作成するためのパラメーターとしてパックされたリストに渡します。

```xpp
public boolean canClose() 
{ 
    ProjReverseMarking      projReverseMarking; 
    boolean                 canClose; 
    List                    list; 
    canClose = super(); 
    if (element.closedOk() && canClose) 
    { 
        List = new List(Types::Record); 
        while select tmpFrmVirtualLines 
        { 
            list.addEnd(tmpFrmVirtualLines); 
        } 
        projReverseMarking = new ProjReverseMarking(list.pack()); 
        projReverseMarking.run(); 
    } 
    return canClose; 
}
```

## <a name="method-tostring"></a>メソッド toString

リスト内の値の説明を返します。

```xpp
public str toString()
```

### <a name="return-value---tostring"></a>戻り値 - toString

リストの要素の値を説明する文字列。

### <a name="remarks---tostring"></a>備考 - toString

リスト内の要素のタイプの説明を印刷するには、List.definitionString メソッドを使用します。

### <a name="examples---tostring"></a>例 - toString

次の例では、整数のリストを作成します。 toString メソッドを使用して、リストにある値の説明を出力します。

```xpp
{ 
    // Create a list of integers 
    List il = new List(Types::Integer); 
    // Add some elements to the list 
    il.addEnd(1); 
    il.addEnd(2); 
    il.addStart(3); 
    // Print a description of the list 
    print il.definitionString(); 
    print il.toString(); 
    pause; 
}
```

## <a name="method-typeid"></a>メソッド typeId

リスト内の値のタイプを返します。

```xpp
public Types typeId()
```

### <a name="return-value---typeid"></a>戻り値 - typeId

リスト要素のタイプ。

### <a name="remarks---typeid"></a>備考 - typeId

リストのタイプは、リストが作成されるときに指定され、リストの存続期間中は同じままです。

## <a name="method-xml"></a>メソッド xml

現在のオブジェクトを表す XML 文字列を返します。

```xpp
public str xml([int indent])
```

### <a name="parameters---xml"></a>パラメーター - xml

インデント  
返された XML 文字列のインデントの量 (省略可能)。

### <a name="return-value---xml"></a>戻り値 - xml

現在のオブジェクトを表す XML 文字列です。

### <a name="remarks---xml"></a>備考 - xml

このメソッドをオーバーライドして、その型に対して意味のある値を返すことができます。

## <a name="method-create"></a>メソッド create

以前の List.pack メソッドの呼び出しで取得したコンテナーからリストを作成します。

```xpp
public static List create(container container)
```

### <a name="parameters---create"></a>パラメーター - create

コンテナー  
パックされたリストを保持するコンテナー。

### <a name="return-value---create"></a>戻り値 - create

コンテナーに梱包されたものと同一のリスト。

### <a name="examples---create"></a>例 - create

次の例では、リストを作成し、それをコンテナーにパックします。 次に、create メソッドを使用してコンテナーを展開し、元のリストと同じリストを作成します。

```xpp
{ 
    List il = new List(Types::Integer); 
    List newList; 
    container packedList; 
    // Add some elements 
    il.addEnd(1); 
    il.addEnd(2); 
    il.addEnd(3); 
    // Pack the list into a container 
    packedList = il.pack(); 
    newList = list::create(packedList); 
    // Prints <1, 2, 3> 
    print newList.toString(); 
    pause; 
}
```

## <a name="method-createfromxml"></a>メソッド createFromXML

```xpp
public static List createFromXML(Object xmlnode)
```

### <a name="parameters---createfromxml"></a>パラメーター - createFromXML

xmlnode  

### <a name="return-value---createfromxml"></a>戻り値 - createFromXML

## <a name="method-equal"></a>メソッド equal

2 つのリストが同じかどうかを判定します。

```xpp
public static boolean equal(List list1, List list2)
```

### <a name="parameters---equal"></a>パラメーター - equal

list1  
比較する 2 番目のリスト。

<!-- -->

list2  
比較する 2 番目のリスト。

### <a name="return-value---equal"></a>戻り値 - equal

2 つのリストが同一である場合は true。それ以外の場合は、false。

### <a name="remarks---equal"></a>備考 - equal

2 つのリストが同じ型の場合、リストは別のリストと等しくなり、要素の同じ番号を含み、同じ順序で要素が発生します。

## <a name="method-merge"></a>メソッド merge

2 つのリストを組み合わせ、新しいリストを作成します。

```xpp
public static List merge(List list1, List list2)
```

### <a name="parameters---merge"></a>パラメーター - merge

list1  
新しいリストを作成するために最初のリストの最後に追加されるリスト。

<!-- -->

list2  
新しいリストを作成するために最初のリストの最後に追加されるリスト。

### <a name="return-value---merge"></a>戻り値 - merge

新しいリスト。

### <a name="remarks---merge"></a>備考 - merge

リストのタイプは同じにする必要があります。

### <a name="examples---merge"></a>例 - merge

次の例では、2 つの整数値のリストを作成し、それらをマージして新しいリストを作成し、新しい組み合わせリストに値を出力します。

```xpp
{ 
    List list1  = new List(Types::Integer); 
    List list2  = new List(Types::Integer); 
    List combinedList  = new List(Types::Integer); 
    int  i; 
    for(i=1; i<6; i++) 
    { 
        List1.addEnd(i); 
    } 
     for(i=6; i<11; i++) 
    { 
        List2.addEnd(i); 
    } 
    combinedList = List::merge(list1, list2); 
    print combinedList.toString(); 
    pause; 
}
```

## <a name="method-appendlist"></a>メソッド appendList

```xpp
public void appendList(List list)
```

### <a name="parameters---appendlist"></a>パラメーター - appendList

リスト  

## <a name="method-new"></a>メソッド new

リストを作成します。

```xpp
public void new(Types Type)
```

### <a name="parameters---new"></a>パラメーター - new

種類  
リスト内の要素が持つべきタイプ。

### <a name="remarks---new"></a>備考 - new

Type パラメーターの使用可能な値は、Type システム列挙によって提供されます。 リストを作成した後、そのリストに含まれている要素のタイプを変更することはできません。

### <a name="examples---new"></a>例 - new

次の例では、文字列のリストを作成します。

```xpp
{ 
    // Creates a list of integers. 
    List il = new List(Types::String); 
}
```

