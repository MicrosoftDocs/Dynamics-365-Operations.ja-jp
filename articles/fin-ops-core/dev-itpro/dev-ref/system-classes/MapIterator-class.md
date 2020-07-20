---
title: MapIterator クラス
description: このトピックでは、MapIterator クラスについて説明します。
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
ms.openlocfilehash: adbc42748c457979a30937d8e5a6214071a89237
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502883"
---
# <a name="class-mapiterator"></a>クラス MapIterator

[!include [banner](../../includes/banner.md)]

```xpp
class MapIterator extends Object
```

MapIterator クラスは、マップ内の要素を反復処理するために使用されます。

## <a name="remarks"></a>備考

マップ反復子は、マップ内で要素を反復処理するために使用されます。 これらは、反復処理する対象となるマップにシンプルなポインターとして表示することができます。 繰り返しを開始する機能は利用可能であり、より多くの (キー、値) の組み合わせが利用可能であるかどうかを決定し、繰り返しによりポイントされる要素をフェッチします。 MapIterator クラスよりも MapEnumerator クラスを使用することをお勧めします。 マップ反復子および反復処理するマップは、同じクライアント/サーバー側にある必要があります。 MapIterator クラスを使用し、コードが Called from としてマークされている場合、マップと反復子が別の層で終了する可能性があり、コードは失敗します。 MapEnumerator クラスを使用する場合、列挙子はマップと同じ層に自動的に作成されます。 また、MapIterator クラスを使用する場合、より多くおよび次のメソッドを明示的に呼び出して、マップに次の項目を移動する必要があります。 MapEnumerator クラスを使用する場合、moveNext メソッドを呼び出すだけです。 要素が挿入されるシーケンスは、挿入の順序を決定しません。 順序は、要素の順序によって定義されます。 上位キーを持つ要素の前に、下位キーを持つ要素が表示されます。 型の通常の順序が使用されます。 ただし、キーがオブジェクトである場合、オブジェクトのアドレスを使用して順序が指定されるため、特定の順序を推測することはできません。 オブジェクトのアドレスは、本来、一時的です。

## <a name="examples"></a>例

次の例では、マップを作成し、3 つの (キー、値) のペアを追加します。 マップを通じて反復処理し、各マップ要素に関する情報を印刷します。

```xpp
{ 
    Map iim = new Map(Types::Integer, Types::Class); 
    MapIterator it; 
    // Add some elements into the map 
    iim.insert(1, new query()); 
    iim.insert(2, new query()); 
    iim.insert(4, new query()); 
    // Create a map iterator 
    it = new MapIterator (iim); 
    // Print "[int -> class] iterator" 
    print it.definitionString();     
    // Go on for as long as elements are found in the map 
    while (it.more()) 
    { 
        // Print each key (1, 2, 4) 
        print it.key();  
        // Print text representation of each value 
        print it.value().toString();  
        // Fetch next element in map 
        it.next(); 
    } 
    pause; 
}
```

## <a name="methods"></a>メソッド

| 方法                             | 説明                                                                                    |
|------------------------------------|------------------------------------------------------------------------------------------------|
| public str definitionString()      | "\[int -&gt; str\] 反復子" など、反復子の型のテキスト表現を取得します。 |
| public AnyType domainValue()       | 反復子により参照される (キー、値) ペアにおけるキーの値を返します。     |
| public boolean find(AnyType value) | 指定したキー値を検索します。                                                          |
| public AnyType key()               | 反復子により参照される (キー、値) ペアからキーを返します。                |
| public boolean more()              | 反復子が有効な (キー、値 ) ペアを検出するかどうかを決定します。                               |
| public AnyType rangeValue()        | 反復子により参照される (キー、値) ペアにおける値の値を返します。   |
| public str toString()              | 反復子のテキスト表現を取得します。                                            |
| public AnyType value()             | 反復子により参照される (キー、値) ペアから値を返します。              |
| public container valuePair()       | キーと値を保持するコンテナーを取得します。                                        |
| public void next()                 | 次の (キー、値) ペアに反復子を移動します。                                              |
| public void new(Map map)           | マップ内の要素をスキャンできるマップの新しい反復子を作成します。       |
| public void begin()                | 反復子をマップの先頭に移動します。                                                    |
| public void end()                  | マップで最後の要素の後に反復子を移動します。                                           |
| public void delete()               | 反復子によってポイントされている要素をマップから削除します。                           |

## <a name="method-definitionstring"></a>メソッド definitionString

"\[int -&gt; str\] 反復子" など、反復子の型のテキスト表現を取得します。

```xpp
public str definitionString()
```

### <a name="return-value---definitionstring"></a>戻り値 - definitionString

反復子を説明する文字列。

## <a name="method-domainvalue"></a>メソッド domainValue

反復子により参照される (キー、値) ペアにおけるキーの値を返します。

```xpp
public AnyType domainValue()
```

### <a name="return-value---domainvalue"></a>戻り値 - domainValue

反復子によって現在参照されているマップ要素の最初の項目の値。

## <a name="method-find"></a>メソッド find

指定したキー値を検索します。

```xpp
public boolean find(AnyType value)
```

### <a name="parameters---find"></a>パラメーター - find

値  
検索する値。

### <a name="return-value---find"></a>戻り値 - find

値が見つかった場合は true。それ以外の場合は、false。

### <a name="remarks---find"></a>備考 - find

True が返された場合、このメソッドは、反復子を要素に配置します。それ以外の場合、MapIterator.more メソッドは false を返します。

## <a name="method-key"></a>メソッド key

反復子により参照される (キー、値) ペアからキーを返します。

```xpp
public AnyType key()
```

### <a name="return-value---key"></a>戻り値 - key

マップ反復子によって示されるマップ エントリのキー値。

### <a name="remarks---key"></a>備考 - key

マップ要素のキー値を取得する前に要素が存在するかどうかをテストするには、SetIterator.more メソッドを使用します。

### <a name="examples---key"></a>例 - key

次の例では、マップを反復処理し、マップ内のすべての要素の説明を返します。

```xpp
static str writeMap (Map m) 
{ 
    MapIterator it = new MapIterator(m); 
    str result; 
    while (it.more()) 
    { 
        result += it.key() + '\n' + it.value() + '\n'; 
        it.next(); 
    } 
    return result; 
}
```

## <a name="method-more"></a>メソッド more

反復子が有効な (キー、値 ) ペアを検出するかどうかを決定します。

```xpp
public boolean more()
```

### <a name="return-value---more"></a>戻り値 - more

より多くの (キー、値) の組み合わせがマップで使用可能な場合は true。それ以外の場合は、false。

### <a name="remarks---more"></a>備考 - more

more メソッドが false を返すときに反復子が指す要素にアクセスしようとするとエラーが発生します。 より多くのメソッドは、反復子が有効な要素を指しているかどうかだけをテストします。 マップにより多くの要素があるかどうかはテストされません。

### <a name="examples---more"></a>例 - more

次の例では、more メソッドを使用してマップ内の要素がまだ存在するかどうかを調べることによって、マップを反復処理します。 マップ内のすべての要素の説明を返します。

```xpp
static str writeMap (Map m) 
{ 
    MapIterator it = new MapIterator(m); 
    str result; 
    while (it.more()) 
    { 
        result += it.key() + '\n' + it.value() + '\n'; 
        it.next(); 
    } 
    return result; 
}
```

## <a name="method-rangevalue"></a>メソッド rangeValue

反復子により参照される (キー、値) ペアにおける値の値を返します。

```xpp
public AnyType rangeValue()
```

### <a name="return-value---rangevalue"></a>戻り値 - rangeValue

反復子によって現在参照されているマップ要素の 2 番目の項目の値。

### <a name="remarks---rangevalue"></a>備考 - rangeValue

rangeValue メソッドは MapIterator.value メソッドと同じ機能を持ちますが、domainValue メソッドに対応するメソッドとして使用できます。

## <a name="method-tostring"></a>メソッド toString

反復子のテキスト表現を取得します。

```xpp
public str toString()
```

### <a name="return-value---tostring"></a>戻り値 - toString

反復子を説明する文字列。

### <a name="remarks---tostring"></a>備考 - toString

反復子がセット内の最初の要素をポイントする場合、文字列にはこの表現が次のフォームで含まれます: "(開始)\[ *値*\]" 反復子が要素をポイントしている場合 (つまり、MapIterator.more メソッドが false を返す場合)、返される文字列は「(終了)」になります。 反復子が値をポイントしている場合、文字列は "\[*値*\]" で、*値*が要素値の文字列表現です。

### <a name="examples---tostring"></a>例 - toString

次の例では、整数またはクラス マップを反復処理し、各マップ要素に関する情報を出力します。 MapIterator.toString メソッドを使用して各マップ要素でのクラスのテキスト表現を返します。

```xpp
{ 
    Map iim = new Map(Types::Integer, Types::Class); 
    MapIterator it; 
    // Add some elements into the map 
    iim.insert(1, new query()); 
    iim.insert(2, new query()); 
    iim.insert(4, new query()); 
    // Create a map iterator 
    it = new MapIterator (iim); 
    // Go on for as long as elements are found in the map 
    while (it.more()) 
    { 
        // Print each key (1, 2, 4) 
        print it.key();  
        // Print text representation of each value 
        print it.value().toString();  
        // Fetch next element in map 
        it.next(); 
    } 
    pause; 
}
```

## <a name="method-value"></a>メソッド value

反復子により参照される (キー、値) ペアから値を返します。

```xpp
public AnyType value()
```

### <a name="return-value---value"></a>戻り値 - value

マップ反復子によって示されるマップ要素からの値。

### <a name="remarks---value"></a>備考 - value

マップ要素のキー値を取得する前に要素が存在するかどうかをテストするには、MapIterator.more メソッドを使用します。

### <a name="examples---value"></a>例 - value

次の例では、マップを反復処理し、マップ内のすべての要素のリストを返します。

```xpp
static str writeMap (Map m) 
{ 
    MapIterator it = new MapIterator(m); 
    str result; 
    while (it.more()) 
    { 
        result += it.key() + '\n' + it.value() + '\n'; 
        it.next(); 
    } 
    return result; 
}
```

## <a name="method-valuepair"></a>メソッド valuePair

キーと値を保持するコンテナーを取得します。

```xpp
public container valuePair()
```

### <a name="return-value---valuepair"></a>戻り値 - valuePair

キーと値を保持するコンテナーです。

### <a name="remarks---valuepair"></a>備考 - valuePair

オブジェクトをコンテナーに配置することはできません。 したがって、キーまたは値のいずれかがオブジェクトである場合、例外が発生します。

## <a name="method-next"></a>メソッド next

次の (キー、値) ペアに反復子を移動します。

```xpp
public void next()
```

### <a name="remarks---next"></a>備考 - next

MapIterator.more メソッドを使用すると、マップ内にさらに要素があるかどうか判断することができます。

### <a name="examples---next"></a>例 - next

次の例では、next メソッドを使用してマップを反復処理し、マップ内のすべての要素のリストを返します。

```xpp
static str writeMap (Map m) 
{ 
    MapIterator it = new MapIterator(m); 
    str result; 
    while (it.more()) 
    { 
        result += it.key() + '\n' + it.value() + '\n'; 
        it.next(); 
    } 
    return result; 
}
```

## <a name="method-new"></a>メソッド new

マップ内の要素をスキャンできるマップの新しい反復子を作成します。

```xpp
public void new(Map map)
```

### <a name="parameters---new"></a>パラメーター - new

マップ  
反復子を作成するマップ。

### <a name="remarks---new"></a>備考 - new

反復子は、マップが空でない場合、マップの最初の値に配置されます。

### <a name="examples---new"></a>例 - new

次の例では、(整数、クラス) のペアのマップを作成し、マップを移動する反復子を作成します。

```xpp
Map iim = new Map(Types::Integer, Types::Class); 
MapIterator it; 
it = new MapIterator (iim);
```

## <a name="method-begin"></a>メソッド begin

反復子をマップの先頭に移動します。

```xpp
public void begin()
```

### <a name="remarks---begin"></a>備考 - begin

新しく作成されるマップ反復子は、マップの最初の要素に配置されるため、セットを通じて反復する前に開始メソッドを呼び出す必要はありません。 ポインターをリセットする場合は、開始メソッドを呼び出す必要があります。

## <a name="method-end"></a>メソッド end

マップで最後の要素の後に反復子を移動します。

```xpp
public void end()
```

### <a name="remarks---end"></a>備考 - end

このメソッドを実行すると、MapIterator.more メソッドが false に戻ります。

## <a name="method-delete"></a>メソッド delete

反復子によってポイントされている要素をマップから削除します。

```xpp
public void delete()
```

### <a name="remarks---delete"></a>備考 - delete

反復子は、delete メソッドが呼び出された後に次の要素を指します。

