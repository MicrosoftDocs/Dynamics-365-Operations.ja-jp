---
title: Map クラス
description: このトピックでは、Map クラスについて説明します。
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
ms.openlocfilehash: 8c6e342b93ecd36415c707ad37fbb2a56ae56fa2
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502887"
---
# <a name="class-map"></a>クラス マップ

[!include [banner](../../includes/banner.md)]

```xpp
class Map extends Object
```

Map クラスを使うと、ある値 (キー) を別の値に関連付けることができます。

## <a name="remarks"></a>備考

キーと値の両方は、オブジェクトを含む有効な X++ タイプにすることができます。 キーのタイプと値は、マップの宣言で指定されます。 マップが実装される方法は、値へのアクセスが非常に高速であることを意味します。 複数のキーは、同じ値にマップできますが、1 つのキーは一度に 1 つの値にだけマップすることができます。 既存のキー値を持つ (キー、値) ペアを追加すると、既存のペアがそのキー値に置き換えられます。 マップ内の (キー、値) ペアは、MapEnumerator クラスを使用して移動できます。

## <a name="examples"></a>例

次の例は、マップを逆にする方法を示しています。 2 つの異なるキーによってマップされている値がない場合にのみ、マップを反転できます。 これを確認するために Map.keySet メソッドと Map.valueSet メソッドの要素数が比較されます。 それ以外の場合、要素が受信マップで移動し、結果マップに挿入されます。 切り替えを実行する関数、invertMap メソッドは、キーと値の型に関係なく機能します。

```xpp
{ 
    Map example; 
    Map invertMap(map _mapToInvert) 
    { 
        MapEnumerator en; 
        Map result =  new Map( 
            _mapToInvert.valueType(), 
            _mapToInvert.keyType()); 
        if (_mapToInvert.keySet().elements()  
            != _mapToInvert.valueSet().elements()) 
        { 
            return null; 
        } 
        en = new MapEnumerator(_mapToInvert); 
        while (en.moveNext()) 
        { 
            result.insert(en.currentValue(), en.currentKey()); 
        } 
        return result; 
    } 
    ; 
    // Fill in a few values. 
    example = new Map(Types::Integer, Types::String); 
    example.insert (1, "one"); 
    example.insert (2, "two"); 
    print invertMap(example).toString(); 
    pause; 
    // Now two keys (2 and 3) map to the same value 
    // so can't create inverse map 
    example.insert (3, "two"); 
    if (!invertMap(example)) 
    { 
        print "Could not create the map"; 
    } 
    pause; 
}
```

## <a name="methods"></a>メソッド

| 方法                                                      | 説明                                                                                     |
|-------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| public str definitionString()                               | マップの定義を含む文字列を返します。                                         |
| public Set domainSet()                                      | マップにキー (ドメイン) 値のセットを作成します。                                              |
| public Types domainType()                                   | マップ内のキー (ドメイン) 値のタイプを決定します。                                        |
| public int elements()                                       | マップ内の要素の数を返します。                                                      |
| public boolean empty()                                      | マップに (キー、値) のペアが含まれているかどうかを判定します。                                     |
| public boolean exists(AnyType keyValue)                     | 特定の値がマップ内のキーとして存在するかどうかを決定します。                               |
| public MapEnumerator getEnumerator()                        | マップ内のスキャンを可能にする、マップの列挙子を作成します。                             |
| public boolean insert(AnyType keyValue, AnyType valueValue) | マップに要素 (keyValue、valueValue ペア) を挿入します。                                    |
| public Set keySet()                                         | マップからのキー値を含むセットを返します。                                          |
| public Types keyType()                                      | マップ内のキー値のタイプを返します。                                                    |
| public AnyType lookup(AnyType keyValue)                     | 指定されたキー値によりマッピングされている値を返します。                                   |
| public container pack()                                     | Map クラスの現在のインスタンスをシリアル化します。                                               |
| public Set rangeSet()                                       | マップ内のキーによってマップされる値 (範囲) を含むセットを返します。        |
| public Types rangeType()                                    | マップ内のキーによってマップされる値 (範囲) のタイプを決定します。             |
| public boolean remove(AnyType keyValue)                     | (キー、値) ペアをマップから削除します。                                                         |
| public str toString()                                       | マップ内の (キー、値) ペアの説明を返します。                                     |
| public Set valueSet()                                       | マップ内のキーによってマップされる値を含むセットを返します。                 |
| public Types valueType()                                    | マップ内のキーによってマップされる値のタイプを返します。                         |
| public str xml(\[int indent\])                              | 現在のオブジェクトを表す XML 文字列を返します。                                       |
| ::public static Map create(container container)             | 以前の Map.pack メソッドの呼び出しで取得されたコンテナーからマップを作成します。 |
| ::public static Map createFromXML(Object xmlnode)           |                                                                                                 |
| ::public static boolean equal(Map map1, Map map2)           | 2 つのマップが等しいかどうかを判断します。                                                          |
| public void new(Types key, Types value)                     | 新しいマップを作成します                                                                              |

## <a name="method-definitionstring"></a>メソッド definitionString

マップの定義を含む文字列を返します。

```xpp
public str definitionString()
```

### <a name="return-value---definitionstring"></a>戻り値 - definitionString

マップの定義を含む文字列。

### <a name="remarks---definitionstring"></a>備考 - definitionString

マップの定義。

### <a name="examples---definitionstring"></a>例 - definitionString

次の例では、マップを作成し、マップの定義を出力します。

```xpp
{ 
    Map myMap = new Map(Types::Integer, Types::String); 
    print myMap.definitionString(); 
    pause; 
}
```

## <a name="method-domainset"></a>メソッド domainSet

マップにキー (ドメイン) 値のセットを作成します。

```xpp
public Set domainSet()
```

### <a name="return-value---domainset"></a>戻り値 - domainSet

### <a name="remarks---domainset"></a>備考 - domainSet

このメソッドは廃止されました。代わりに Map.keySet を使用してください。

## <a name="method-domaintype"></a>メソッド domainType

マップ内のキー (ドメイン) 値のタイプを決定します。

```xpp
public Types domainType()
```

### <a name="return-value---domaintype"></a>戻り値 - domainType

### <a name="remarks---domaintype"></a>備考 - domainType

このメソッドは廃止されました。代わりに Map.keyType を使用してください。

## <a name="method-elements"></a>メソッド elements

マップ内の要素の数を返します。

```xpp
public int elements()
```

### <a name="return-value---elements"></a>戻り値 - elements

マップ内の要素の数。

### <a name="remarks---elements"></a>備考 - elements

マップ内の要素の数はマップ内の異なるキー値の数と同等になります。

### <a name="examples---elements"></a>例 - elements

次の例では、elements メソッドを使用して、マップに要素があるかどうかを確認します。 \_マップ元が存在し、一部の要素を持っている場合、\_マップ元の値は\_マップ先へ挿入されます。

```xpp
static void mergeRecsPrim( 
    Map _from, 
    Map _to 
    ) 
{ 
    MapEnumerator   me; 
    if (! _from) 
    { 
        return; 
    } 
    if (! _from.elements()) 
    { 
        return; 
    } 
    me = _from.getEnumerator(); 
    while (me.moveNext()) 
    { 
        _to.insert(me.currentKey(),me.currentValue()); 
    } 
}
```

## <a name="method-empty"></a>メソッド empty

マップに (キー、値) のペアが含まれているかどうかを判定します。

```xpp
public boolean empty()
```

### <a name="return-value---empty"></a>戻り値 - empty

マップに要素が存在しない場合に true。それ以外の場合は false。

### <a name="remarks---empty"></a>備考 - empty

このメソッドは、(elements() == 0) と等価です。

## <a name="method-exists"></a>メソッド exists

特定の値がマップ内のキーとして存在するかどうかを決定します。

```xpp
public boolean exists(AnyType keyValue)
```

### <a name="parameters---exists"></a>パラメーター - exists

keyValue  
確認する値。

### <a name="return-value---exists"></a>戻り値 - exists

指定されたキー値がマップ内に存在する場合は true。それ以外の場合は、false。

### <a name="remarks---exists"></a>備考 - exists

Map.lookup メソッドへの呼び出しを保護するには、このメソッドを使用します。 Map.lookup メソッドで、検索値が見つからなかった場合、例外が発生されます。

### <a name="examples---exists"></a>例 - exists

次の例では、スタイル シート内のスタイルのマップに特定のスタイルが存在するかどうかを確認します。 存在する場合は、本文のスタイルの新しい名前に置き換えられます。

```xpp
static void renameStyle(Map stylesheet, str fromName, str toName) 
{ 
    str body; 
    if (stylesheet.exists(fromName)) 
    { 
        body = stylesheet.lookup (fromName); 
        stylesheet.remove (fromName); 
        stylesheet.insert (toName, body); 
    } 
    else 
    { 
        info (fromName); 
    } 
}
```

## <a name="method-getenumerator"></a>メソッド getEnumerator

マップ内のスキャンを可能にする、マップの列挙子を作成します。

```xpp
public MapEnumerator getEnumerator()
```

### <a name="return-value---getenumerator"></a>戻り値 - getEnumerator

マップの MapEnumerator オブジェクト。

### <a name="examples---getenumerator"></a>例 - getEnumerator

次の例では \_from マップに要素があるかどうかを確認し、要素がある場合はマップの列挙子を作成します。 次に、マップが移動し、その中の要素が \_to マップに挿入されます。

```xpp
static void mergeRecsPrim( 
    Map _from, 
    Map _to 
    ) 
{ 
    MapEnumerator   me; 
    if (! _from) 
    { 
        return; 
    } 
    if (! _from.elements()) 
    { 
        return; 
    } 
    me = _from.getEnumerator(); 
    while (me.moveNext()) 
    { 
        _to.insert(me.currentKey(),me.currentValue()); 
    } 
}
```

## <a name="method-insert"></a>メソッド insert

マップに要素 (keyValue、valueValue ペア) を挿入します。

```xpp
public boolean insert(AnyType keyValue, AnyType valueValue)
```

### <a name="parameters---insert"></a>パラメーター - insert

keyValue  
キーによりマッピングされている値。

<!-- -->

valueValue  
キーによりマッピングされている値。

### <a name="return-value---insert"></a>戻り値 - insert

キーがマップにまだ存在せず、マップが挿入された場合は true。それ以外の場合は、false。

### <a name="remarks---insert"></a>備考 - insert

キーが既にマップに存在する場合は、値が更新されます。

### <a name="examples---insert"></a>例 - insert

次の例では \_from マップに要素があるかどうかを確認し、要素がある場合はマップの列挙子を作成します。 マップが移動し、\_from マップから \_to マップに要素を挿入するために insert メソッドが使用されます。

```xpp
static void mergeRecsPrim( 
    Map _from, 
    Map _to 
    ) 
{ 
    MapEnumerator   me; 
    if (! _from) 
    { 
        return; 
    } 
    if (! _from.elements()) 
    { 
        return; 
    } 
    me = _from.getEnumerator(); 
    while (me.moveNext()) 
    { 
        _to.insert(me.currentKey(),me.currentValue()); 
    } 
}
```

## <a name="method-keyset"></a>メソッド keySet

マップからのキー値を含むセットを返します。

```xpp
public Set keySet()
```

### <a name="return-value---keyset"></a>戻り値 - keySet

キー値を含むセット。

### <a name="examples---keyset"></a>例 - keySet

次の例では、セット内の要素として検出されないキー値を持つすべての要素をマップから削除します。

```xpp
public void deleteItems(Set _set, Map _map) 
{ 
    Set             deletedSet; 
    SetEnumerator   enumerator; 
    // deletedSet contains all key values from 
    // _map that are not values in _set 
    deletedSet = Set::difference(_map.keySet(), _set); 
    enumerator = deletedSet.getEnumerator(); 
    while (enumerator.moveNext()) 
    { 
        // Deletes elements from map with key 
        // values matching values in deletedSet 
        _map.remove(enumerator.current()); 
    } 
}
```

## <a name="method-keytype"></a>メソッド keyType

マップ内のキー値のタイプを返します。

```xpp
public Types keyType()
```

### <a name="return-value---keytype"></a>戻り値 - keyType

キー値のタイプ。

### <a name="remarks---keytype"></a>備考 - keyType

可能な戻り値は、Types システム列挙で説明されます。 キー値のタイプは、マップの作成時に決定されます。 これは Map.new メソッドに対する最初のパラメーターとして指定されます。

## <a name="method-lookup"></a>メソッド lookup

指定されたキー値によりマッピングされている値を返します。

```xpp
public AnyType lookup(AnyType keyValue)
```

### <a name="parameters---lookup"></a>パラメーター - lookup

keyValue  
検索するキー。

### <a name="return-value---lookup"></a>戻り値 - lookup

キーにより指定されている値。

### <a name="remarks---lookup"></a>戻り値 - lookup

マップ内にキーが見つからない場合、Map.exists メソッドを使用して取得する値が存在するかどうかを確認し例外がスローされます。

### <a name="examples---lookup"></a>例 - lookup

次の例では、スタイル シート内のスタイルのマップに特定のスタイルが存在するかどうかを確認します。 存在する場合は、本文のスタイルの新しい名前に置き換えられます。

```xpp
static void renameStyle(Map stylesheet, str fromName, str toName) 
{ 
    str body; 
    if (stylesheet.exists(fromName)) 
    { 
        body = stylesheet.lookup (fromName); 
        stylesheet.remove (fromName); 
        stylesheet.insert (toName, body); 
    } 
    else 
    { 
        info (fromName); 
    } 
}
```

## <a name="method-pack"></a>メソッド pack

Map クラスの現在のインスタンスをシリアル化します。

```xpp
public container pack()
```

### <a name="return-value---pack"></a>戻り値 - pack

Map クラスの現在のインスタンスを含むコンテナーです。

### <a name="remarks---pack"></a>備考 - pack

このメソッドで作成されたコンテナーには、マップの最初の要素の前に 4 つの要素が含まれます。

-   コンテナのバージョン番号
-   マップ内のキーのデータ型を識別する整数
-   マップ内の値のデータ型を識別する整数
-   マップ内の要素の数。

キーまたは値がオブジェクトになっている場合は、梱包は、各オブジェクトに対して pack メソッドを連続して呼び出し、サブコンテナーを取得することによって行われます。 pack メソッドと unpack メソッドは、X++ anytype 値を保持できません。 1 つのオプションは、anytype 値をオブジェクトまたは構造体に格納し、構造体をマップ オブジェクトの値にすることです。 Microsoft .NET System.Collections クラスは別のオプションで使用します。 Map.create メソッドを使用して、パックされたコンテナーからマップを取得できます。

### <a name="examples---pack"></a>例 - pack

次の例では、メソッド (conprojItemTransSalesAmount) に渡されたコンテナーからマップを作成し、いくつかの値を追加して MapEnumerator.pack を使用してマップをコンテナーにパックします。 このメソッドによって新しいコンテナーが返されます。

```xpp
server static container salesAmountDisplayCache( 
    container   _conprojItemTrans, 
    container   _conprojItemTransSalesAmount, 
    TransDate   _ledgerFromDate, 
    TransDate   _ledgerToDate) 
{ 
    ProjItemTrans    projItemTrans; 
    Set              setprojItemTrans; 
    Map              mapprojItemTransSalesAmount; 
    SetIterator      si; 
    if(_conprojItemTrans) 
    { 
        setprojItemTrans = Set::create(_conprojItemTrans); 
    } 
    if(_conprojItemTransSalesAmount) 
    { 
        mapprojItemTransSalesAmount = Map::create( 
            _conprojItemTransSalesAmount); 
    } 
    si = new SetIterator(setprojItemTrans); 
    si.begin(); 
    while (si.more()) 
    { 
        projItemTrans = ProjItemTrans::find(si.value()); 
        mapprojItemTransSalesAmount.insert( 
            si.value(),  
            projItemTrans.salesAmount( 
                projItemTrans, 
               _ledgerFromDate, 
               _ledgerToDate)); 
        si.next(); 
    } 
    return mapprojItemTransSalesAmount.pack(); 
}
```

## <a name="method-rangeset"></a>メソッド rangeSet

マップ内のキーによってマップされる値 (範囲) を含むセットを返します。

```xpp
public Set rangeSet()
```

### <a name="return-value---rangeset"></a>戻り値 - rangeSet

### <a name="remarks---rangeset"></a>戻り値 - rangeSet

このメソッドは廃止されました。代わりに Map.valueSet を使用してください。

## <a name="method-rangetype"></a>メソッド rangeType

マップ内のキーによってマップされる値 (範囲) のタイプを決定します。

```xpp
public Types rangeType()
```

### <a name="return-value---rangetype"></a>戻り値 - rangeType

### <a name="remarks---rangetype"></a>備考 - rangeType

このメソッドは廃止されました。代わりに valueType を使用してください。

## <a name="method-remove"></a>メソッド remove

(キー、値) ペアをマップから削除します。

```xpp
public boolean remove(AnyType keyValue)
```

### <a name="parameters---remove"></a>パラメーター - remove

keyValue  
削除するキーの値。

### <a name="return-value---remove"></a>戻り値 - remove

キーがマップ内に見つかり、要素が削除された場合は true。それ以外の場合は、false。

### <a name="examples---remove"></a>例 - remove

次の例では、特定のキー値がマップに存在するかどうかを確認します。 値が存在する場合は、メソッドがキーと対応する値を削除します。 このメソッドは、値が見つかった場合は true を返し、キーがマップに存在しない場合は false を返します。

```xpp
public boolean clear(str owner) 
{ 
    // maps is a class variable 
    if (maps.exists(owner)) 
    { 
        maps.remove(owner); 
    } 
    else 
    { 
        return false; 
    } 
    return true; 
}
```

## <a name="method-tostring"></a>メソッド toString

マップ内の (キー、値) ペアの説明を返します。

```xpp
public str toString()
```

### <a name="return-value---tostring"></a>戻り値 - toString

マップの要素の説明を含む文字列。

### <a name="examples---tostring"></a>例 - toString

次の例では、マップを作成し、いくつかの要素を追加してから、これらの要素の説明を出力します。

```xpp
{ 
    Map myMap = new Map(Types::Integer, Types::String); 
    // Add some elements to the map 
    myMap.insert(1, "Element one"); 
    myMap.insert(2, "Element two"); 
    myMap.insert(3, "Element three"); 
    myMap.insert(4, "Element Four"); 
    print myMap.toString(); 
    pause; 
}
```

## <a name="method-valueset"></a>メソッド valueSet

マップ内のキーによってマップされる値を含むセットを返します。

```xpp
public Set valueSet()
```

### <a name="return-value---valueset"></a>戻り値 - valueSet

マップからの値を含むセット。

### <a name="remarks---valueset"></a>備考 - valueSet

すべてのキーが、別の値にマップされる場合、セット内の要素の数はマップ内の要素の数と同等になります。

## <a name="method-valuetype"></a>メソッド valueType

マップ内のキーによってマップされる値のタイプを返します。

```xpp
public Types valueType()
```

### <a name="return-value---valuetype"></a>戻り値 - valueType

キーによってマップされる値のタイプ。

### <a name="remarks---valuetype"></a>備考 - valueType

キー値のタイプは、マップの作成時に決定されます。 これは Map.new メソッドに対する最初のパラメーターとして指定されます。

## <a name="method-xml"></a>メソッド xml

現在のオブジェクトを表す XML 文字列を返します。

```xpp
public str xml([int indent])
```

### <a name="parameters---xml"></a>パラメーター - xml

インデント  
返される XML 文字列のインデントの量 (省略可能)。

### <a name="return-value---xml"></a>戻り値 - xml

現在のオブジェクトを表す XML 文字列です。

### <a name="remarks---xml"></a>備考 - xml

このメソッドをオーバーライドして、その型に対して意味のある値を返すことができます。

## <a name="method-create"></a>メソッド create

以前の Map.pack メソッドの呼び出しで取得されたコンテナーからマップを作成します。

```xpp
public static Map create(container container)
```

### <a name="parameters---create"></a>パラメーター - create

コンテナー  

### <a name="return-value---create"></a>戻り値 - create

Map.pack メソッドでコンテナーに梱包されたマップと同等のマップ。

### <a name="remarks---create"></a>備考 - create

キーまたは値がオブジェクトの場合、オブジェクトにはコンテナーからその内部状態を再設定するために呼び出されるアンパック メソッドが必要です。

### <a name="examples---create"></a>例 - create

次の例では、メソッド (conprojItemTransSalesAmount) に渡されたコンテナーからマップを作成し、コンテナーに値を追加してマップをパックし、新しいコンテナーとして返します。

```xpp
server static container salesAmountDisplayCache( 
    container   _conprojItemTrans, 
    container   _conprojItemTransSalesAmount, 
    TransDate   _ledgerFromDate, 
    TransDate   _ledgerToDate) 
{ 
    ProjItemTrans    projItemTrans; 
    Set              setprojItemTrans; 
    Map              mapprojItemTransSalesAmount; 
    SetIterator      si; 
    if(_conprojItemTrans) 
    { 
        setprojItemTrans = Set::create(_conprojItemTrans); 
    } 
    if(_conprojItemTransSalesAmount) 
    { 
        mapprojItemTransSalesAmount = Map::create( 
            _conprojItemTransSalesAmount); 
    } 
    si = new SetIterator(setprojItemTrans); 
    si.begin(); 
    while (si.more()) 
    { 
        projItemTrans = ProjItemTrans::find(si.value()); 
        mapprojItemTransSalesAmount.insert( 
            si.value(),  
            projItemTrans.salesAmount( 
                projItemTrans, 
               _ledgerFromDate, 
               _ledgerToDate)); 
        si.next(); 
    } 
    return mapprojItemTransSalesAmount.pack(); 
}
```

## <a name="method-createfromxml"></a>メソッド createFromXML

```xpp
public static Map createFromXML(Object xmlnode)
```

### <a name="parameters---createfromxml"></a>パラメータ - createFromXML

xmlnode  

### <a name="return-value---createfromxml"></a>戻り値 - createFromXML

## <a name="method-equal"></a>メソッド equal

2 つのマップが等しいかどうかを判断します。

```xpp
public static boolean equal(Map map1, Map map2)
```

### <a name="parameters---equal"></a>パラメーター - equal

map1  
比較する 2 つ目のマップ。

<!-- -->

map2  
比較する 2 つ目のマップ。

### <a name="return-value---equal"></a>戻り値 - equal

2 つのマップが等しい場合は true。それ以外の場合は、false。

### <a name="remarks---equal"></a>備考 - equal

2 つのマップが同じ数の要素を含み、キー セットが同じで、キー セットの各キーが両方のマップの同じ値にマップされている場合、2 つのマップは同等です。

## <a name="method-new"></a>メソッド new

新しいマップを作成します

```xpp
public void new(Types key, Types value)
```

### <a name="parameters---new"></a>パラメーター - new

キー  
値のタイプ。

<!-- -->

値  
値のタイプ。

### <a name="examples---new"></a>例 - new

次の例では、文字列キーを整数値にマッピングするマップを作成します。

```xpp
Map myMap = new Map(Types::String, Types::Integer);
```

