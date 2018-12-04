---
title: "M クラス"
description: "文字 M で始まるシステム API クラス。"
author: RobinARH
manager: AnnBe
ms.date: 11/07/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Developer
ms.reviewer: robinr
ms.search.scope: Operations
ms.custom: 52321
ms.assetid: 954d2067-ef47-4714-ae75-23e7a5d539db
ms.search.region: Global
ms.author: robinr
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: e782d33f3748524491dace28008cd9148ae70529
ms.openlocfilehash: f08e5744f755fc2c65a40f301d8521ced7b9f3a1
ms.contentlocale: ja-jp
ms.lasthandoff: 08/09/2018

---

# <a name="m-classes"></a>M クラス

[!include [banner](../includes/banner.md)]

文字 M で始まるシステム API クラス。

<a name="class-managedeventargs"></a>クラス ManagedEventArgs
----------------------

    class ManagedEventArgs extends Object

### <a name="remarks"></a>備考

### <a name="examples"></a>例

### <a name="methods"></a>メソッド

| 方法            | 説明                                               |
|-------------------|-----------------------------------------------------------|
| public void new() | ManagedEventArgs クラスの新しいインスタンスを初期化します。 |

### <a name="method-new"></a>メソッド new

ManagedEventArgs クラスの新しいインスタンスを初期化します。

    public void new()

## <a name="class-managedeventdelegate"></a>クラス ManagedEventDelegate
    class ManagedEventDelegate extends Object

### <a name="remarks"></a>備考

### <a name="examples"></a>例

### <a name="methods"></a>メソッド

| 方法                                                                    | 説明                                                   |
|---------------------------------------------------------------------------|---------------------------------------------------------------|
| public boolean marshalExceptionsToXPP(\[boolean marshalExceptionsToXPP\]) |                                                               |
| private void new()                                                        | ManagedEventDelegate クラスの新しいインスタンスを初期化します。 |
| public void invoke(Object sender, ManagedEventArgs args)                  |                                                               |

### <a name="method-marshalexceptionstoxpp"></a>メソッド marshalExceptionsToXPP

    public boolean marshalExceptionsToXPP([boolean marshalExceptionsToXPP])

#### <a name="parameters"></a>パラメーター

marshalExceptionsToXPP  

#### <a name="return-value"></a>戻り値

### <a name="method-new"></a>メソッド new

ManagedEventDelegate クラスの新しいインスタンスを初期化します。

    private void new()

### <a name="method-invoke"></a>メソッド invoke

    public void invoke(Object sender, ManagedEventArgs args)

#### <a name="parameters"></a>パラメーター

sender  

<!-- -->

args  

## <a name="class-managedeventhandler"></a>クラス ManagedEventHandler
    class ManagedEventHandler extends Object

### <a name="remarks"></a>備考

### <a name="examples"></a>例

### <a name="methods"></a>メソッド

| 方法                                     | 説明                                     |
|--------------------------------------------|-------------------------------------------------|
| public void finalize()                     |                                                 |
| public void new(Object object, str method) | Object クラスの新しいインスタンスを初期化します。 |

### <a name="method-finalize"></a>メソッド finalize

    public void finalize()

### <a name="method-new"></a>メソッド new

Object クラスの新しいインスタンスを初期化します。

    public void new(Object object, str method)

#### <a name="parameters"></a>パラメーター

オブジェクト  

<!-- -->

メソッド  

## <a name="class-map"></a>クラス マップ
    class Map extends Object

Map クラスを使うと、ある値 (キー) を別の値に関連付けることができます。

### <a name="remarks"></a>備考

キーと値の両方は、オブジェクトを含む有効な X++ タイプにすることができます。 キーのタイプと値は、マップの宣言で指定されます。 マップが実装される方法は、値へのアクセスが非常に高速であることを意味します。 複数のキーは、同じ値にマップできますが、1 つのキーは一度に 1 つの値にだけマップすることができます。 既存のキー値を持つ (キー、値) ペアを追加すると、既存のペアがそのキー値に置き換えられます。 マップ内の (キー、値) ペアは、MapEnumerator クラスを使用して移動できます。

### <a name="examples"></a>例

次の例は、マップを逆にする方法を示しています。 2 つの異なるキーによってマップされている値がない場合にのみ、マップを反転できます。 これを確認するために Map.keySet メソッドと Map.valueSet メソッドの要素数が比較されます。 それ以外の場合、要素が受信マップで移動し、結果マップに挿入されます。 切り替えを実行する関数、invertMap メソッドは、キーと値の型に関係なく機能します。

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

### <a name="methods"></a>メソッド

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

### <a name="method-definitionstring"></a>メソッド definitionString

マップの定義を含む文字列を返します。

    public str definitionString()

#### <a name="return-value"></a>戻り値

マップの定義を含む文字列。

#### <a name="remarks"></a>備考

マップの定義。

#### <a name="examples"></a>例

次の例では、マップを作成し、マップの定義を出力します。

    { 
        Map myMap = new Map(Types::Integer, Types::String); 
        print myMap.definitionString(); 
        pause; 
    }

### <a name="method-domainset"></a>メソッド domainSet

マップにキー (ドメイン) 値のセットを作成します。

    public Set domainSet()

#### <a name="return-value"></a>戻り値

#### <a name="remarks"></a>備考

このメソッドは廃止されました。代わりに Map.keySet を使用してください。

### <a name="method-domaintype"></a>メソッド domainType

マップ内のキー (ドメイン) 値のタイプを決定します。

    public Types domainType()

#### <a name="return-value"></a>戻り値

#### <a name="remarks"></a>備考

このメソッドは廃止されました。代わりに Map.keyType を使用してください。

### <a name="method-elements"></a>メソッド elements

マップ内の要素の数を返します。

    public int elements()

#### <a name="return-value"></a>戻り値

マップ内の要素の数。

#### <a name="remarks"></a>備考

マップ内の要素の数はマップ内の異なるキー値の数と同等になります。

#### <a name="examples"></a>例

次の例では、elements メソッドを使用して、マップに要素があるかどうかを確認します。 \_マップ元が存在し、一部の要素を持っている場合、\_マップ元の値は\_マップ先へ挿入されます。

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

### <a name="method-empty"></a>メソッド empty

マップに (キー、値) のペアが含まれているかどうかを判定します。

    public boolean empty()

#### <a name="return-value"></a>戻り値

マップに要素が存在しない場合に true。それ以外の場合は false。

#### <a name="remarks"></a>備考

このメソッドは、(elements() == 0) と等価です。

### <a name="method-exists"></a>メソッド exists

特定の値がマップ内のキーとして存在するかどうかを決定します。

    public boolean exists(AnyType keyValue)

#### <a name="parameters"></a>パラメーター

keyValue  
確認する値。

#### <a name="return-value"></a>戻り値

指定されたキー値がマップ内に存在する場合は true。それ以外の場合は、false。

#### <a name="remarks"></a>備考

Map.lookup メソッドへの呼び出しを保護するには、このメソッドを使用します。 Map.lookup メソッドで、検索値が見つからなかった場合、例外が発生されます。

#### <a name="examples"></a>例

次の例では、スタイル シート内のスタイルのマップに特定のスタイルが存在するかどうかを確認します。 存在する場合は、本文のスタイルの新しい名前に置き換えられます。

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

### <a name="method-getenumerator"></a>メソッド getEnumerator

マップ内のスキャンを可能にする、マップの列挙子を作成します。

    public MapEnumerator getEnumerator()

#### <a name="return-value"></a>戻り値

マップの MapEnumerator オブジェクト。

#### <a name="examples"></a>例

次の例では \_from マップに要素があるかどうかを確認し、要素がある場合はマップの列挙子を作成します。 次に、マップが移動し、その中の要素が \_to マップに挿入されます。

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

### <a name="method-insert"></a>メソッド insert

マップに要素 (keyValue、valueValue ペア) を挿入します。

    public boolean insert(AnyType keyValue, AnyType valueValue)

#### <a name="parameters"></a>パラメーター

keyValue  
キーによりマッピングされている値。

<!-- -->

valueValue  
キーによりマッピングされている値。

#### <a name="return-value"></a>戻り値

キーがマップにまだ存在せず、マップが挿入された場合は true。それ以外の場合は、false。

#### <a name="remarks"></a>備考

キーが既にマップに存在する場合は、値が更新されます。

#### <a name="examples"></a>例

次の例では \_from マップに要素があるかどうかを確認し、要素がある場合はマップの列挙子を作成します。 マップが移動し、\_from マップから \_to マップに要素を挿入するために insert メソッドが使用されます。

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

### <a name="method-keyset"></a>メソッド keySet

マップからのキー値を含むセットを返します。

    public Set keySet()

#### <a name="return-value"></a>戻り値

キー値を含むセット。

#### <a name="examples"></a>例

次の例では、セット内の要素として検出されないキー値を持つすべての要素をマップから削除します。

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

### <a name="method-keytype"></a>メソッド keyType

マップ内のキー値のタイプを返します。

    public Types keyType()

#### <a name="return-value"></a>戻り値

キー値のタイプ。

#### <a name="remarks"></a>備考

可能な戻り値は、Types システム列挙で説明されます。 キー値のタイプは、マップの作成時に決定されます。 これは Map.new メソッドに対する最初のパラメーターとして指定されます。

### <a name="method-lookup"></a>メソッド lookup

指定されたキー値によりマッピングされている値を返します。

    public AnyType lookup(AnyType keyValue)

#### <a name="parameters"></a>パラメーター

keyValue  
検索するキー。

#### <a name="return-value"></a>戻り値

キーにより指定されている値。

#### <a name="remarks"></a>備考

マップ内にキーが見つからない場合、Map.exists メソッドを使用して取得する値が存在するかどうかを確認し例外がスローされます。

#### <a name="examples"></a>例

次の例では、スタイル シート内のスタイルのマップに特定のスタイルが存在するかどうかを確認します。 存在する場合は、本文のスタイルの新しい名前に置き換えられます。

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

### <a name="method-pack"></a>メソッド pack

Map クラスの現在のインスタンスをシリアル化します。

    public container pack()

#### <a name="return-value"></a>戻り値

Map クラスの現在のインスタンスを含むコンテナーです。

#### <a name="remarks"></a>備考

このメソッドで作成されたコンテナーには、マップの最初の要素の前に 4 つの要素が含まれます。

-   コンテナのバージョン番号
-   マップ内のキーのデータ型を識別する整数
-   マップ内の値のデータ型を識別する整数
-   マップ内の要素の数。

キーまたは値がオブジェクトになっている場合は、梱包は、各オブジェクトに対して pack メソッドを連続して呼び出し、サブコンテナーを取得することによって行われます。 pack メソッドと unpack メソッドは、X++ anytype 値を保持できません。 1 つのオプションは、anytype 値をオブジェクトまたは構造体に格納し、構造体をマップ オブジェクトの値にすることです。 Microsoft .NET System.Collections クラスは別のオプションで使用します。 Map.create メソッドを使用して、パックされたコンテナーからマップを取得できます。

#### <a name="examples"></a>例

次の例では、メソッド (conprojItemTransSalesAmount) に渡されたコンテナーからマップを作成し、いくつかの値を追加して MapEnumerator.pack を使用してマップをコンテナーにパックします。 このメソッドによって新しいコンテナーが返されます。

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

### <a name="method-rangeset"></a>メソッド rangeSet

マップ内のキーによってマップされる値 (範囲) を含むセットを返します。

    public Set rangeSet()

#### <a name="return-value"></a>戻り値

#### <a name="remarks"></a>備考

このメソッドは廃止されました。代わりに Map.valueSet を使用してください。

### <a name="method-rangetype"></a>メソッド rangeType

マップ内のキーによってマップされる値 (範囲) のタイプを決定します。

    public Types rangeType()

#### <a name="return-value"></a>戻り値

#### <a name="remarks"></a>備考

このメソッドは廃止されました。代わりに valueType を使用してください。

### <a name="method-remove"></a>メソッド remove

(キー、値) ペアをマップから削除します。

    public boolean remove(AnyType keyValue)

#### <a name="parameters"></a>パラメーター

keyValue  
削除するキーの値。

#### <a name="return-value"></a>戻り値

キーがマップ内に見つかり、要素が削除された場合は true。それ以外の場合は、false。

#### <a name="examples"></a>例

次の例では、特定のキー値がマップに存在するかどうかを確認します。 値が存在する場合は、メソッドがキーと対応する値を削除します。 このメソッドは、値が見つかった場合は true を返し、キーがマップに存在しない場合は false を返します。

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

### <a name="method-tostring"></a>メソッド toString

マップ内の (キー、値) ペアの説明を返します。

    public str toString()

#### <a name="return-value"></a>戻り値

マップの要素の説明を含む文字列。

#### <a name="examples"></a>例

次の例では、マップを作成し、いくつかの要素を追加してから、これらの要素の説明を出力します。

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

### <a name="method-valueset"></a>メソッド valueSet

マップ内のキーによってマップされる値を含むセットを返します。

    public Set valueSet()

#### <a name="return-value"></a>戻り値

マップからの値を含むセット。

#### <a name="remarks"></a>備考

すべてのキーが、別の値にマップされる場合、セット内の要素の数はマップ内の要素の数と同等になります。

### <a name="method-valuetype"></a>メソッド valueType

マップ内のキーによってマップされる値のタイプを返します。

    public Types valueType()

#### <a name="return-value"></a>戻り値

キーによってマップされる値のタイプ。

#### <a name="remarks"></a>備考

キー値のタイプは、マップの作成時に決定されます。 これは Map.new メソッドに対する最初のパラメーターとして指定されます。

### <a name="method-xml"></a>メソッド xml

現在のオブジェクトを表す XML 文字列を返します。

    public str xml([int indent])

#### <a name="parameters"></a>パラメーター

インデント  
返される XML 文字列のインデントの量 (省略可能)。

#### <a name="return-value"></a>戻り値

現在のオブジェクトを表す XML 文字列です。

#### <a name="remarks"></a>備考

このメソッドをオーバーライドして、その型に対して意味のある値を返すことができます。

### <a name="method-create"></a>メソッド create

以前の Map.pack メソッドの呼び出しで取得されたコンテナーからマップを作成します。

    public static Map create(container container)

#### <a name="parameters"></a>パラメーター

コンテナー  

#### <a name="return-value"></a>戻り値

Map.pack メソッドでコンテナーに梱包されたマップと同等のマップ。

#### <a name="remarks"></a>備考

キーまたは値がオブジェクトの場合、オブジェクトにはコンテナーからその内部状態を再設定するために呼び出されるアンパック メソッドが必要です。

#### <a name="examples"></a>例

次の例では、メソッド (conprojItemTransSalesAmount) に渡されたコンテナーからマップを作成し、コンテナーに値を追加してマップをパックし、新しいコンテナーとして返します。

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

### <a name="method-createfromxml"></a>メソッド createFromXML

    public static Map createFromXML(Object xmlnode)

#### <a name="parameters"></a>パラメーター

xmlnode  

#### <a name="return-value"></a>戻り値

### <a name="method-equal"></a>メソッド equal

2 つのマップが等しいかどうかを判断します。

    public static boolean equal(Map map1, Map map2)

#### <a name="parameters"></a>パラメーター

map1  
比較する 2 つ目のマップ。

<!-- -->

map2  
比較する 2 つ目のマップ。

#### <a name="return-value"></a>戻り値

2 つのマップが等しい場合は true。それ以外の場合は、false。

#### <a name="remarks"></a>備考

2 つのマップが同じ数の要素を含み、キー セットが同じで、キー セットの各キーが両方のマップの同じ値にマップされている場合、2 つのマップは同等です。

### <a name="method-new"></a>メソッド new

新しいマップを作成します

    public void new(Types key, Types value)

#### <a name="parameters"></a>パラメーター

キー  
値のタイプ。

<!-- -->

値  
値のタイプ。

#### <a name="examples"></a>例

次の例では、文字列キーを整数値にマッピングするマップを作成します。

    Map myMap = new Map(Types::String, Types::Integer);

## <a name="class-mapenumerator"></a>クラス MapEnumerator
    class MapEnumerator extends Object

MapEnumerator クラスを使用すると、マップ内の要素上を移動できます。

### <a name="remarks"></a>備考

マップ列挙子は、リストの最初の要素の前に開始します。 リストの最初の要素を指すようにするために MapEnumerator.moveNext メソッドを呼び出す必要があります。 Map.getEnumerator メソッドが呼び出されたときに、マップと同じ層で列挙子が自動的に作成されるため、MapIterator クラスではなく、MapEnumerator クラスを使用することがベスト プラクティスです。 MapEnumerator クラスを使用すると、Called from としてマークされたコードの潜在的な問題が回避されます。反復子とマップは別々の層に置くことができます。 さらに、マップ列挙子はマップ反復子よりも少ないコードを必要とするためパフォーマンスが少し向上します。 マップ反復子を使用する必要がある唯一の状況は、MapIterator.delete メソッドを使用してリストから項目を削除する場合です。

### <a name="examples"></a>例

### <a name="methods"></a>メソッド

| 方法                        | 説明                                                                                                                                       |
|-------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| public AnyType current()      | このメソッドは廃止されました。代わりに MapEnumerator.currentKey を使用してください。                                                                                    |
| public AnyType currentKey()   | 現在列挙子によってポイントされている (キー、値) ペアからキーを返します。                                                        |
| public AnyType currentValue() | 現在列挙子によってポイントされている (キー、値) ペアから値を返します。                                                      |
| public str definitionString() | 列挙子の説明を返します。 たとえば、文字列への整数のマップの列挙子は、「\[int -&gt; str\] 列挙子」を返します。 |
| public boolean moveNext()     | 列挙子が有効なマップ要素を指すかどうかを決定します。                                                                                  |
| public str toString()         | 現在のオブジェクトを表す文字列を返します。                                                                                              |
| public void new(Map map)      | Object クラスの新しいインスタンスを初期化します。                                                                                                   |
| public void reset()           | 列挙子を移動して、マップ内の最初の要素の直前をポイントします。                                                                        |

### <a name="method-current"></a>メソッド current

このメソッドは廃止されました。代わりに MapEnumerator.currentKey を使用してください。

    public AnyType current()

#### <a name="return-value"></a>戻り値

### <a name="method-currentkey"></a>メソッド currentKey

現在列挙子によってポイントされている (キー、値) ペアからキーを返します。

    public AnyType currentKey()

#### <a name="return-value"></a>戻り値

現在列挙子によってポイントされているマップ要素のキー。

#### <a name="remarks"></a>備考

CurrentKey メソッドを呼び出す前に、MapEnumerator.moveNext メソッドを呼び出す必要があります。

#### <a name="examples"></a>例

次の例では、マップ内の特定のテーブル ID を検索し、そのマップ要素のキー値を返します。

    private LabelType tableLabel(tableId _tableId) 
    { 
        LabelType     labelType; 
        MapEnumerator mapEnum; 
        mapEnum = tableAllMap.getEnumerator(); 
        while (mapEnum.moveNext()) 
        { 
            if (_tableId == mapEnum.currentValue()) 
            { 
                labelType = mapEnum.currentKey(); 
                break; 
            } 
        } 
        return labelType; 
    }

### <a name="method-currentvalue"></a>メソッド currentValue

現在列挙子によってポイントされている (キー、値) ペアから値を返します。

    public AnyType currentValue()

#### <a name="return-value"></a>戻り値

現在列挙子によってポイントされているマップ要素の値。

#### <a name="remarks"></a>備考

このメソッドを呼び出す前に、MapEnumerator.moveNext メソッドを呼び出す必要があります。

#### <a name="examples"></a>例

次の例では、マップを検索して、パラメーターとして渡された値と等しい値を持つ要素を検索します。 MapEnumerator.moveNext メソッドは、マップを反復処理するために使用され、currentValue メソッドは各値をテストしてパラメーターと一致するかどうかを確認するために使用されます。

    private LabelType tableLabel(tableId _tableId) 
    { 
        LabelType     labelType; 
        MapEnumerator mapEnum; 
        mapEnum = tableAllMap.getEnumerator(); 
        while (mapEnum.moveNext()) 
        { 
            if (_tableId == mapEnum.currentValue()) 
            { 
                labelType = mapEnum.currentKey(); 
                break; 
            } 
        } 
        return labelType; 
    }

### <a name="method-definitionstring"></a>メソッド definitionString

列挙子の説明を返します。 たとえば、文字列への整数のマップの列挙子は、「\[int -&gt; str\] 列挙子」を返します。

    public str definitionString()

#### <a name="return-value"></a>戻り値

列挙子の説明を含む文字列。

#### <a name="examples"></a>例

次の例では、マップとその列挙子を作成し、列挙子の定義を出力します。

    { 
        Map myMap = new Map(Types::Integer, Types::String); 
        MapEnumerator  enumerator; 
        int i; 
        // Add some elements to the map 
        myMap.insert(1, "Element one"); 
        myMap.insert(2, "Element two"); 
        myMap.insert(3, "Element three"); 
        myMap.insert(4, "Element Four"); 
        // Set the enumerator 
        enumerator = myMap.getEnumerator(); 
        print enumerator.definitionString(); 
        pause; 
    }

### <a name="method-movenext"></a>メソッド moveNext

列挙子が有効なマップ要素を指すかどうかを決定します。

    public boolean moveNext()

#### <a name="return-value"></a>戻り値

マップ内の現在の職位が有効な要素を保持している場合は true。それ以外の場合は false。

#### <a name="remarks"></a>備考

マップ列挙子は、マップの最初の要素の前に開始します。 マップの最初の要素を指すようにするために moveNext メソッドを呼び出す必要があります。

#### <a name="examples"></a>例

次の例では、moveNext メソッドを使用してプロジェクトに含まれるテーブルを反復処理し、テーブルの DictTable オブジェクトを含む新しいマップに追加します。 (DictTable を使用すると、テーブルに関する情報にアクセスできます。)

    { 
        Map map = Map::create( 
            SysUmlDataModel::getProjectTablesClient(projectNode)); 
        MapEnumerator enum = map.getEnumerator(); 
        TableName tableName; 
        while (enum.moveNext()) 
        { 
            tableName = enum.currentKey(); 
            map.insert(tableName, new DictTable(tablename2id(tableName))); 
        } 
        return map; 
    }

### <a name="method-tostring"></a>メソッド toString

現在のオブジェクトを表す文字列を返します。

    public str toString()

#### <a name="return-value"></a>戻り値

現在のオブジェクトを表す文字列。

#### <a name="remarks"></a>備考

既定の実装は、オブジェクトのクラス名を返します。 メソッドは派生クラスで上書きできるため、そのタイプの意味のある値が返されます。 たとえば、SysMethodInfo クラスのインスタンスは、インスタンスまたは静的などのメソッド名およびメソッドのタイプを返します。

#### <a name="examples"></a>例

次の例では、マップを作成し、最初の要素と 2 番目の要素の内容をマップに出力します。

    { 
        Map myMap = new Map(Types::Integer, Types::String); 
        MapEnumerator  enumerator; 
        int i; 
         // Add some elements to the map 
        myMap.insert(1, "Element one"); 
        myMap.insert(2, "Element two"); 
        myMap.insert(3, "Element three"); 
        myMap.insert(4, "Element Four"); 
        // Set the enumerator 
        enumerator = myMap.getEnumerator(); 
        // Go to beginning of enumerator 
        enumerator.reset(); 
        // Go to the first element in the map 
        enumerator.moveNext(); 
        // Print first item in the map 
        print enumerator.toString(); 
        // go to second element 
         enumerator.moveNext(); 
        // Print second element in map 
        print enumerator.toString(); 
        pause; 
    }

### <a name="method-new"></a>メソッド new

Object クラスの新しいインスタンスを初期化します。

    public void new(Map map)

#### <a name="parameters"></a>パラメーター

マップ  
列挙子を作成するマップ。

#### <a name="remarks"></a>備考

 メソッドは廃止されています。 代わりに Map.getEnumerator メソッドを使用します。

### <a name="method-reset"></a>メソッド reset

列挙子を移動して、マップ内の最初の要素の直前をポイントします。

    public void reset()

#### <a name="remarks"></a>備考

reset メソッドは、列挙子をセットの先頭、セットの最初の要素の前に移動します。 セットの最初の要素を指すようにするために MapEnumerator.moveNext メソッドを呼び出す必要があります。

## <a name="class-mapi"></a>クラス Mapi
    class Mapi extends Object

Mapi クラスを使用すると、Microsoft Exchange ベースのシステム、Microsoft Outlook Express、Lotus CCMail など、ほとんどの主要なメール システムでメールを送信、受信、管理できます。

### <a name="remarks"></a>備考

他の Mapi クラス、MapiMessage、MapiRecipDesc、MapiFileDesc とともに、このクラスでは、複数の受信者、添付ファイル、メッセージ テキスト、件名を指定できます。 最も簡単な方法は、マシン上に作業用のメール クライアントを設定し、いくつかの電子メール メッセージを送受信することによって正しく動作することを確認することです。 Mapi メソッドのフラグは、Mapi マクロに配置されます。 \#MAPI ステートメントと共に Mapi クラスを使用するコードにこのマクロを含めます。

### <a name="examples"></a>例

次の例は、このクラスを使用して電子メール メッセージを送信する方法を示しています。

    static void example() 
    { 
        #Mapi 
        Mapi m = new Mapi(); 
        MapiMessage msg = new MapiMessage(); 
        MapiRecipDesc recip = new MapiRecipDesc(); 
        // Set up the recipient. 
        recip.Name("someone"); 
        recip.RecipClass(#MAPI_TO); 
        msg.setRecipNo(1,recip); 
        // Log on using default profile. 
        m.Logon("","",#MAPI_USE_DEFAULT); 
        // Send the mail, and allow the user to modify the 
        // Subject, Text and Recipients in the Send Mail Dialog. 
        m.SendMail(msg,#MAPI_DIALOG); 
        // Log off. 
        m.Logoff(); 
    }

### <a name="methods"></a>メソッド

| 方法                                                                         | 説明                                                                                          |
|--------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| public int deleteMail(str messageID)                                           | メッセージ ストアから指定されたメッセージを削除します。                                                |
| public str findNext(\[str messageType\], \[str seedMessageID\], \[int flags\]) | メッセージ店舗で最初または次のメッセージを検索します。                                                |
| public int logoff()                                                            | メール システムからログオフすることができます。                                                                    |
| public int logon(str profileName, str password, int flags)                     | 指定されたプロファイルとパスワードを使用して、メール システムにログオンします。                              |
| public MapiMessage readMail(str messageID, \[int flags\])                      | メッセージ ストアからメッセージを取得します。                                                          |
| public MapiRecipDesc resolveName(str mame, int flags)                          | ユーザーが入力したメッセージ受信者の名前を一意のアドレス一覧エントリに変換します。 |
| public int saveMail(MapiMessage message, int flags, str messageId)             | メッセージ ストアにメッセージを保存します。                                                                |
| public int sendMail(MapiMessage message, \[int flags\])                        | 特定の受信者にメッセージを送信します。                                                         |
| public int status()                                                            | 最後の Mapi 操作のステータスを取得します。                                                     |
| public void new()                                                              | Mapi クラスのインスタンスを初期化します。                                                           |
| public void finalize()                                                         |                                                                                                      |

### <a name="method-deletemail"></a>メソッド deleteMail

メッセージ ストアから指定されたメッセージを削除します。

    public int deleteMail(str messageID)

#### <a name="parameters"></a>パラメーター

messageID  
削除するメッセージの一意のメッセージ ID。

#### <a name="return-value"></a>戻り値

状態 \#SUCCESS\_SUCCES またはエラー コード。これは \#MAPI マクロにあります。

#### <a name="remarks"></a>備考

メッセージ ID は、findNext メソッドを使用して取得できます。

### <a name="method-findnext"></a>メソッド findNext

メッセージ店舗で最初または次のメッセージを検索します。

    public str findNext([str messageType], [str seedMessageID], [int flags])

#### <a name="parameters"></a>パラメーター

messageType  
先入れ先出し (FIFO) を示すフラグまたは未読; オプション。 このパラメーターには、次の 2 つの値があります。

<!-- -->

seedMessageID  
先入れ先出し (FIFO) を示すフラグまたは未読; オプション。 このパラメーターには、次の 2 つの値があります。

<!-- -->

flags  
先入れ先出し (FIFO) を示すフラグまたは未読; オプション。 このパラメーターには、次の 2 つの値があります。

#### <a name="return-value"></a>戻り値

見つかったメッセージのメッセージ ID。メッセージが見つからない場合は空の文字列です。

#### <a name="remarks"></a>備考

このメソッドを呼び出して最初のメッセージを検索し、続く呼び出しを発行して次のメッセージを取得します。 このメソッドを呼び出した後、status メソッドを使用して Mapi エラーを確認します。

### <a name="method-logoff"></a>メソッド logoff

メール システムからログオフすることができます。

    public int logoff()

#### <a name="return-value"></a>戻り値

状態 \#SUCCESS\_SUCCESS またはエラー コード。これは \#MAPI マクロにあります。

### <a name="method-logon"></a>メソッド logon

指定されたプロファイルとパスワードを使用して、メール システムにログオンします。

    public int logon(str profileName, str password, int flags)

#### <a name="parameters"></a>パラメーター

profileName  
フラグの一覧。 有効なフラグは次のとおりです。

<!-- -->

パスワード  
フラグの一覧。 有効なフラグは次のとおりです。

<!-- -->

flags  
フラグの一覧。 有効なフラグは次のとおりです。

#### <a name="return-value"></a>戻り値

ログオンに成功した場合は、状態 \#SUCCESS\_SUCCESS です。そうでない場合は、エラー コードを返します。これは、\#MAPI マクロにあります。

#### <a name="remarks"></a>備考

ログオンするための簡単で一般的な方法は、既定のプロファイルを使用してログオンする \#MAPI\_USE\_DEFAULT フラグを指定することです。

### <a name="method-readmail"></a>メソッド readMail

メッセージ ストアからメッセージを取得します。

    public MapiMessage readMail(str messageID, [int flags])

#### <a name="parameters"></a>パラメーター

messageID  
フラグの一覧 (オプション)。 有効なフラグは次のとおりです。

<!-- -->

flags  
フラグの一覧 (オプション)。 有効なフラグは次のとおりです。

#### <a name="return-value"></a>戻り値

取得された MapiMessage オブジェクト、または nullNothingnullptrunita null 参照 (Visual Basic では Nothing)。

### <a name="method-resolvename"></a>メソッド resolveName

ユーザーが入力したメッセージ受信者の名前を一意のアドレス一覧エントリに変換します。

    public MapiRecipDesc resolveName(str mame, int flags)

#### <a name="parameters"></a>パラメーター

mame  
フラグの一覧。 有効なフラグは次のとおりです。

<!-- -->

flags  
フラグの一覧。 有効なフラグは次のとおりです。

#### <a name="return-value"></a>戻り値

明確なアドレス一覧エントリを持つ MapiRecipDesc クラス オブジェクト。

### <a name="method-savemail"></a>メソッド saveMail

メッセージ ストアにメッセージを保存します。

    public int saveMail(MapiMessage message, int flags, str messageId)

#### <a name="parameters"></a>パラメーター

メッセージ  
取得するメッセージの一意の ID。

<!-- -->

flags  
取得するメッセージの一意の ID。

<!-- -->

messageId  
取得するメッセージの一意の ID。

#### <a name="return-value"></a>戻り値

状態 \#SUCCESS\_SUCCESS または \#MAPI マクロのエラー コード。

### <a name="method-sendmail"></a>メソッド sendMail

特定の受信者にメッセージを送信します。

    public int sendMail(MapiMessage message, [int flags])

#### <a name="parameters"></a>パラメーター

メッセージ  
フラグの一覧 (オプション)。 有効なフラグは次のとおりです。

<!-- -->

flags  
フラグの一覧 (オプション)。 有効なフラグは次のとおりです。

#### <a name="return-value"></a>戻り値

状態 \#SUCCESS\_SUCCESS または \#MAPI マクロのエラー コード。

### <a name="method-status"></a>メソッド status

最後の Mapi 操作のステータスを取得します。

    public int status()

#### <a name="return-value"></a>戻り値

最後の Mapi 操作のステータス コード。

#### <a name="remarks"></a>備考

ステータス コードは \#MAPI マクロにあります。

### <a name="method-new"></a>メソッド new

Mapi クラスのインスタンスを初期化します。

    public void new()

### <a name="method-finalize"></a>メソッド finalize

    public void finalize()

## <a name="class-mapiex"></a>クラス MapiEx
    class MapiEx extends Object

### <a name="remarks"></a>備考

### <a name="examples"></a>例

### <a name="methods"></a>メソッド

| 方法                                                          | 説明                                     |
|-----------------------------------------------------------------|-------------------------------------------------|
| public MapiExAppointment getAppointmentFromEntryId(str entryID) |                                                 |
| public MapiExContact getContactFromEntryId(str entryID)         |                                                 |
| public int getCurrentUser()                                     |                                                 |
| public str getCurrentUserEmail()                                |                                                 |
| public str getCurrentUserEntryId()                              |                                                 |
| public str getCurrentUserName()                                 |                                                 |
| public MapiExMail getMailFromEntryId(str entryID)               |                                                 |
| public MapiExTask getTaskFromEntryId(str entryID)               |                                                 |
| public int logon(str profileName, str password, int flags)      |                                                 |
| public boolean mapiInitialised()                                |                                                 |
| public boolean openMessageStore(str str)                        |                                                 |
| public void finalize()                                          |                                                 |
| public void new()                                               | MapiEx クラスの新しいインスタンスを初期化します。 |
| public void logout()                                            |                                                 |

### <a name="method-getappointmentfromentryid"></a>メソッド getAppointmentFromEntryId

    public MapiExAppointment getAppointmentFromEntryId(str entryID)

#### <a name="parameters"></a>パラメーター

entryID  

#### <a name="return-value"></a>戻り値

### <a name="method-getcontactfromentryid"></a>メソッド getContactFromEntryId

    public MapiExContact getContactFromEntryId(str entryID)

#### <a name="parameters"></a>パラメーター

entryID  

#### <a name="return-value"></a>戻り値

### <a name="method-getcurrentuser"></a>メソッド getCurrentUser

    public int getCurrentUser()

#### <a name="return-value"></a>戻り値

### <a name="method-getcurrentuseremail"></a>メソッド getCurrentUserEmail

    public str getCurrentUserEmail()

#### <a name="return-value"></a>戻り値

### <a name="method-getcurrentuserentryid"></a>メソッド getCurrentUserEntryId

    public str getCurrentUserEntryId()

#### <a name="return-value"></a>戻り値

### <a name="method-getcurrentusername"></a>メソッド getCurrentUserName

    public str getCurrentUserName()

#### <a name="return-value"></a>戻り値

### <a name="method-getmailfromentryid"></a>メソッド getMailFromEntryId

    public MapiExMail getMailFromEntryId(str entryID)

#### <a name="parameters"></a>パラメーター

entryID  

#### <a name="return-value"></a>戻り値

### <a name="method-gettaskfromentryid"></a>メソッド getTaskFromEntryId

    public MapiExTask getTaskFromEntryId(str entryID)

#### <a name="parameters"></a>パラメーター

entryID  

#### <a name="return-value"></a>戻り値

### <a name="method-logon"></a>メソッド logon

    public int logon(str profileName, str password, int flags)

#### <a name="parameters"></a>パラメーター

profileName  

<!-- -->

パスワード  

<!-- -->

flags  

#### <a name="return-value"></a>戻り値

### <a name="method-mapiinitialised"></a>メソッド mapiInitialised

    public boolean mapiInitialised()

#### <a name="return-value"></a>戻り値

### <a name="method-openmessagestore"></a>メソッド openMessageStore

    public boolean openMessageStore(str str)

#### <a name="parameters"></a>パラメーター

str  

#### <a name="return-value"></a>戻り値

### <a name="method-finalize"></a>メソッド finalize

    public void finalize()

### <a name="method-new"></a>メソッド new

MapiEx クラスの新しいインスタンスを初期化します。

    public void new()

### <a name="method-logout"></a>メソッド logout

    public void logout()

## <a name="class-mapiexappointment"></a>クラス MapiExAppointment
    class MapiExAppointment extends MapiExMessage

### <a name="remarks"></a>備考

### <a name="examples"></a>例

### <a name="methods"></a>メソッド

| 方法                                                 | 説明                                                |
|--------------------------------------------------------|------------------------------------------------------------|
| public str addRecipient(str email, str name, int type) |                                                            |
| public str entryId()                                   |                                                            |
| public str getGlobalObjectId()                         |                                                            |
| public boolean getRecipient(int index)                 |                                                            |
| public int getRecipientCount()                         |                                                            |
| public str getRecipientDisplayName()                   |                                                            |
| public str getRecipientEmailAddress()                  |                                                            |
| public str getRecipientEntryId()                       |                                                            |
| public boolean getRecipients()                         |                                                            |
| public str getRecipientSMTPAddress()                   |                                                            |
| public int getRecipientType()                          |                                                            |
| public str getSenderEmail()                            |                                                            |
| public str getSenderName()                             |                                                            |
| public str removeRecipient(str email, int type)        |                                                            |
| public boolean save()                                  |                                                            |
| public boolean setBody(str body)                       |                                                            |
| public void new()                                      | MapiExAppointment クラスの新しいインスタンスを初期化します。 |
| public void close()                                    |                                                            |
| public void finalize()                                 |                                                            |

### <a name="method-addrecipient"></a>メソッド addRecipient

    public str addRecipient(str email, str name, int type)

#### <a name="parameters"></a>パラメーター

電子メール  

<!-- -->

名前  

<!-- -->

タイプ  

#### <a name="return-value"></a>戻り値

### <a name="method-entryid"></a>メソッド entryId

    public str entryId()

#### <a name="return-value"></a>戻り値

### <a name="method-getglobalobjectid"></a>メソッド getGlobalObjectId

    public str getGlobalObjectId()

#### <a name="return-value"></a>戻り値

### <a name="method-getrecipient"></a>メソッド getRecipient

    public boolean getRecipient(int index)

#### <a name="parameters"></a>パラメーター

指数  

#### <a name="return-value"></a>戻り値

### <a name="method-getrecipientcount"></a>メソッド getRecipientCount

    public int getRecipientCount()

#### <a name="return-value"></a>戻り値

### <a name="method-getrecipientdisplayname"></a>メソッド getRecipientDisplayName

    public str getRecipientDisplayName()

#### <a name="return-value"></a>戻り値

### <a name="method-getrecipientemailaddress"></a>メソッド getRecipientEmailAddress

    public str getRecipientEmailAddress()

#### <a name="return-value"></a>戻り値

### <a name="method-getrecipiententryid"></a>メソッド getRecipientEntryId

    public str getRecipientEntryId()

#### <a name="return-value"></a>戻り値

### <a name="method-getrecipients"></a>メソッド getRecipients

    public boolean getRecipients()

#### <a name="return-value"></a>戻り値

### <a name="method-getrecipientsmtpaddress"></a>メソッド getRecipientSMTPAddress

    public str getRecipientSMTPAddress()

#### <a name="return-value"></a>戻り値

### <a name="method-getrecipienttype"></a>メソッド getRecipientType

    public int getRecipientType()

#### <a name="return-value"></a>戻り値

### <a name="method-getsenderemail"></a>メソッド getSenderEmail

    public str getSenderEmail()

#### <a name="return-value"></a>戻り値

### <a name="method-getsendername"></a>メソッド getSenderName

    public str getSenderName()

#### <a name="return-value"></a>戻り値

### <a name="method-removerecipient"></a>メソッド removeRecipient

    public str removeRecipient(str email, int type)

#### <a name="parameters"></a>パラメーター

電子メール  

<!-- -->

タイプ  

#### <a name="return-value"></a>戻り値

### <a name="method-save"></a>メソッド save

    public boolean save()

#### <a name="return-value"></a>戻り値

### <a name="method-setbody"></a>メソッド setBody

    public boolean setBody(str body)

#### <a name="parameters"></a>パラメーター

body  

#### <a name="return-value"></a>戻り値

### <a name="method-new"></a>メソッド new

MapiExAppointment クラスの新しいインスタンスを初期化します。

    public void new()

### <a name="method-close"></a>メソッド close

    public void close()

### <a name="method-finalize"></a>メソッド finalize

    public void finalize()

## <a name="class-mapiexcontact"></a>クラス MapiExContact
    class MapiExContact extends MapiExMessage

### <a name="remarks"></a>備考

### <a name="examples"></a>例

### <a name="methods"></a>メソッド

| 方法                            | 説明                                            |
|-----------------------------------|--------------------------------------------------------|
| public str entryId()              |                                                        |
| public str getBody()              |                                                        |
| public str getEmail1()            |                                                        |
| public str getEmail1DisplayName() |                                                        |
| public str getEmail1Type()        |                                                        |
| public str getEmail2()            |                                                        |
| public str getEmail2DisplayName() |                                                        |
| public str getEmail2Type()        |                                                        |
| public str getEmail3()            |                                                        |
| public str getEmail3DisplayName() |                                                        |
| public str getEmail3Type()        |                                                        |
| public str getIMAddress()         |                                                        |
| public boolean save()             |                                                        |
| public boolean setBody(str body)  |                                                        |
| public void close()               |                                                        |
| public void finalize()            |                                                        |
| public void new()                 | MapiExContact クラスの新しいインスタンスを初期化します。 |

### <a name="method-entryid"></a>メソッド entryId

    public str entryId()

#### <a name="return-value"></a>戻り値

### <a name="method-getbody"></a>メソッド getBody

    public str getBody()

#### <a name="return-value"></a>戻り値

### <a name="method-getemail1"></a>メソッド getEmail1

    public str getEmail1()

#### <a name="return-value"></a>戻り値

### <a name="method-getemail1displayname"></a>メソッド getEmail1DisplayName

    public str getEmail1DisplayName()

#### <a name="return-value"></a>戻り値

### <a name="method-getemail1type"></a>メソッド getEmail1Type

    public str getEmail1Type()

#### <a name="return-value"></a>戻り値

### <a name="method-getemail2"></a>メソッド getEmail2

    public str getEmail2()

#### <a name="return-value"></a>戻り値

### <a name="method-getemail2displayname"></a>メソッド getEmail2DisplayName

    public str getEmail2DisplayName()

#### <a name="return-value"></a>戻り値

### <a name="method-getemail2type"></a>メソッド getEmail2Type

    public str getEmail2Type()

#### <a name="return-value"></a>戻り値

### <a name="method-getemail3"></a>メソッド getEmail3

    public str getEmail3()

#### <a name="return-value"></a>戻り値

### <a name="method-getemail3displayname"></a>メソッド getEmail3DisplayName

    public str getEmail3DisplayName()

#### <a name="return-value"></a>戻り値

### <a name="method-getemail3type"></a>メソッド getEmail3Type

    public str getEmail3Type()

#### <a name="return-value"></a>戻り値

### <a name="method-getimaddress"></a>メソッド getIMAddress

    public str getIMAddress()

#### <a name="return-value"></a>戻り値

### <a name="method-save"></a>メソッド save

    public boolean save()

#### <a name="return-value"></a>戻り値

### <a name="method-setbody"></a>メソッド setBody

    public boolean setBody(str body)

#### <a name="parameters"></a>パラメーター

body  

#### <a name="return-value"></a>戻り値

### <a name="method-close"></a>メソッド close

    public void close()

### <a name="method-finalize"></a>メソッド finalize

    public void finalize()

### <a name="method-new"></a>メソッド new

MapiExContact クラスの新しいインスタンスを初期化します。

    public void new()

## <a name="class-mapiexmail"></a>クラス MapiExMail
    class MapiExMail extends MapiExMessage

### <a name="remarks"></a>備考

### <a name="examples"></a>例

### <a name="methods"></a>メソッド

| 方法                                                 | 説明                                         |
|--------------------------------------------------------|-----------------------------------------------------|
| public str addRecipient(str email, str name, int type) |                                                     |
| public str entryId()                                   |                                                     |
| public boolean getRecipient(int index)                 |                                                     |
| public int getRecipientCount()                         |                                                     |
| public str getRecipientDisplayName()                   |                                                     |
| public str getRecipientEmailAddress()                  |                                                     |
| public str getRecipientEntryId()                       |                                                     |
| public boolean getRecipients()                         |                                                     |
| public str getRecipientSMTPAddress()                   |                                                     |
| public int getRecipientType()                          |                                                     |
| public str getSenderEmail()                            |                                                     |
| public str getSenderName()                             |                                                     |
| public str removeRecipient(str email, int type)        |                                                     |
| public boolean save()                                  |                                                     |
| public boolean saveMsgToFile(str fileName)             |                                                     |
| public boolean send()                                  |                                                     |
| public boolean setBody(str body)                       |                                                     |
| public void finalize()                                 |                                                     |
| public void close()                                    |                                                     |
| public void new()                                      | MapiExMail クラスの新しいインスタンスを初期化します。 |

### <a name="method-addrecipient"></a>メソッド addRecipient

    public str addRecipient(str email, str name, int type)

#### <a name="parameters"></a>パラメーター

電子メール  

<!-- -->

名前  

<!-- -->

タイプ  

#### <a name="return-value"></a>戻り値

### <a name="method-entryid"></a>メソッド entryId

    public str entryId()

#### <a name="return-value"></a>戻り値

### <a name="method-getrecipient"></a>メソッド getRecipient

    public boolean getRecipient(int index)

#### <a name="parameters"></a>パラメーター

指数  

#### <a name="return-value"></a>戻り値

### <a name="method-getrecipientcount"></a>メソッド getRecipientCount

    public int getRecipientCount()

#### <a name="return-value"></a>戻り値

### <a name="method-getrecipientdisplayname"></a>メソッド getRecipientDisplayName

    public str getRecipientDisplayName()

#### <a name="return-value"></a>戻り値

### <a name="method-getrecipientemailaddress"></a>メソッド getRecipientEmailAddress

    public str getRecipientEmailAddress()

#### <a name="return-value"></a>戻り値

### <a name="method-getrecipiententryid"></a>メソッド getRecipientEntryId

    public str getRecipientEntryId()

#### <a name="return-value"></a>戻り値

### <a name="method-getrecipients"></a>メソッド getRecipients

    public boolean getRecipients()

#### <a name="return-value"></a>戻り値

### <a name="method-getrecipientsmtpaddress"></a>メソッド getRecipientSMTPAddress

    public str getRecipientSMTPAddress()

#### <a name="return-value"></a>戻り値

### <a name="method-getrecipienttype"></a>メソッド getRecipientType

    public int getRecipientType()

#### <a name="return-value"></a>戻り値

### <a name="method-getsenderemail"></a>メソッド getSenderEmail

    public str getSenderEmail()

#### <a name="return-value"></a>戻り値

### <a name="method-getsendername"></a>メソッド getSenderName

    public str getSenderName()

#### <a name="return-value"></a>戻り値

### <a name="method-removerecipient"></a>メソッド removeRecipient

    public str removeRecipient(str email, int type)

#### <a name="parameters"></a>パラメーター

電子メール  

<!-- -->

タイプ  

#### <a name="return-value"></a>戻り値

### <a name="method-save"></a>メソッド save

    public boolean save()

#### <a name="return-value"></a>戻り値

### <a name="method-savemsgtofile"></a>メソッド saveMsgToFile

    public boolean saveMsgToFile(str fileName)

#### <a name="parameters"></a>パラメーター

fileName  

#### <a name="return-value"></a>戻り値

### <a name="method-send"></a>メソッド send

    public boolean send()

#### <a name="return-value"></a>戻り値

### <a name="method-setbody"></a>メソッド setBody

    public boolean setBody(str body)

#### <a name="parameters"></a>パラメーター

body  

#### <a name="return-value"></a>戻り値

### <a name="method-finalize"></a>メソッド finalize

    public void finalize()

### <a name="method-close"></a>メソッド close

    public void close()

### <a name="method-new"></a>メソッド new

MapiExMail クラスの新しいインスタンスを初期化します。

    public void new()

## <a name="class-mapiexmessage"></a>クラス MapiExMessage
    class MapiExMessage extends Object

### <a name="remarks"></a>備考

### <a name="examples"></a>例

### <a name="methods"></a>メソッド

| 方法                           | 説明                                            |
|----------------------------------|--------------------------------------------------------|
| public str entryId()             |                                                        |
| public str getBody()             |                                                        |
| public boolean save()            |                                                        |
| public boolean setBody(str body) |                                                        |
| public void new()                | MapiExMessage クラスの新しいインスタンスを初期化します。 |
| public void finalize()           |                                                        |
| public void close()              |                                                        |

### <a name="method-entryid"></a>メソッド entryId

    public str entryId()

#### <a name="return-value"></a>戻り値

### <a name="method-getbody"></a>メソッド getBody

    public str getBody()

#### <a name="return-value"></a>戻り値

### <a name="method-save"></a>メソッド save

    public boolean save()

#### <a name="return-value"></a>戻り値

### <a name="method-setbody"></a>メソッド setBody

    public boolean setBody(str body)

#### <a name="parameters"></a>パラメーター

body  

#### <a name="return-value"></a>戻り値

### <a name="method-new"></a>メソッド new

MapiExMessage クラスの新しいインスタンスを初期化します。

    public void new()

### <a name="method-finalize"></a>メソッド finalize

    public void finalize()

### <a name="method-close"></a>メソッド close

    public void close()

## <a name="class-mapiextask"></a>クラス MapiExTask
    class MapiExTask extends MapiExMessage

### <a name="remarks"></a>備考

### <a name="examples"></a>例

### <a name="methods"></a>メソッド

| 方法                           | 説明                                         |
|----------------------------------|-----------------------------------------------------|
| public str entryId()             |                                                     |
| public str getBody()             |                                                     |
| public boolean save()            |                                                     |
| public boolean setBody(str body) |                                                     |
| public void finalize()           |                                                     |
| public void close()              |                                                     |
| public void new()                | MapiExTask クラスの新しいインスタンスを初期化します。 |

### <a name="method-entryid"></a>メソッド entryId

    public str entryId()

#### <a name="return-value"></a>戻り値

### <a name="method-getbody"></a>メソッド getBody

    public str getBody()

#### <a name="return-value"></a>戻り値

### <a name="method-save"></a>メソッド save

    public boolean save()

#### <a name="return-value"></a>戻り値

### <a name="method-setbody"></a>メソッド setBody

    public boolean setBody(str body)

#### <a name="parameters"></a>パラメーター

body  

#### <a name="return-value"></a>戻り値

### <a name="method-finalize"></a>メソッド finalize

    public void finalize()

### <a name="method-close"></a>メソッド close

    public void close()

### <a name="method-new"></a>メソッド new

MapiExTask クラスの新しいインスタンスを初期化します。

    public void new()

## <a name="class-mapifiledesc"></a>クラス MapiFileDesc
    class MapiFileDesc extends Object

MapiFileDesc クラスは、メッセージに関連付けられているファイルを取得および設定します。

### <a name="remarks"></a>備考

ファイルの説明は、ファイルの 2 つのタイプの情報で構成されています。

-   ディスク上のファイルをポイントするパス メソッド
-   fileName メソッドには、ユーザーに表示されるファイル名が含まれます。

### <a name="examples"></a>例

    static void example() 
    { 
        MapiMessage msg = New MapiMessage(); 
        MapiFileDesc attach = new MapiFileDesc(); 
        attach.Path("C:\\files\\myfile.txt"); 
    }

### <a name="methods"></a>メソッド

| 方法                                | 説明                                           |
|---------------------------------------|-------------------------------------------------------|
| public str fileName(\[str filename\]) |                                                       |
| public str path(\[str thePath\])      |                                                       |
| public void new()                     | MapiFileDesc クラスの新しいインスタンスを初期化します。 |
| public void finalize()                |                                                       |

### <a name="method-filename"></a>メソッド fileName

    public str fileName([str filename])

#### <a name="parameters"></a>パラメーター

filename  

#### <a name="return-value"></a>戻り値

### <a name="method-path"></a>メソッド path

    public str path([str thePath])

#### <a name="parameters"></a>パラメーター

thePath  

#### <a name="return-value"></a>戻り値

### <a name="method-new"></a>メソッド new

MapiFileDesc クラスの新しいインスタンスを初期化します。

    public void new()

### <a name="method-finalize"></a>メソッド finalize

    public void finalize()

## <a name="class-mapimessage"></a>クラス MapiMessage
    class MapiMessage extends Object

MapiMessage クラスには、MAPI システムから送受信されるメッセージが含まれています。 メッセージには、件名、テキスト、受信者情報、および添付ファイル情報が含まれます。

### <a name="remarks"></a>備考

メッセージを送受信するとき、メッセージは、MapiMessage対象として MAPI システムとの間を渡されます。

### <a name="examples"></a>例

### <a name="methods"></a>メソッド

| 方法                                                        | 説明                                                                                             |
|---------------------------------------------------------------|---------------------------------------------------------------------------------------------------------|
| public str conversationID(\[str conversationId\])             | メッセージが所属する会話スレッドを識別する文字列を取得または設定します。           |
| public str dateReceived(\[Date theDate\])                     | メッセージを受信した日付を返します。                                                         |
| public int flags(\[int flags\])                               | メッセージ ステータス フラグのビットを設定または取得します。                                                       |
| public MapiFileDesc getFileNo(int fileNo)                     | メッセージからの添付ファイルを取得します。                                                                  |
| public MapiRecipDesc getRecipNo(int recipentNo)               | MapiRecipDesc オブジェクトにあるメッセージの受信者に関する情報を取得します。                              |
| public str messageType(\[str messageType\])                   | IPM (個人間メッセージ) タイプではないメッセージを示す文字列を取得または設定します。 |
| public int numFiles(\[int numFiles\])                         |                                                                                                         |
| public int numRecips(\[int numRecips\])                       |                                                                                                         |
| public MapiRecipDesc originator(\[MapiRecipDesc originator\]) |                                                                                                         |
| public str subject(\[str subject\])                           |                                                                                                         |
| public str text(\[str text\])                                 |                                                                                                         |
| public void new()                                             | MapiMessage クラスのインスタンスを初期化します。                                                       |
| public void finalize()                                        |                                                                                                         |
| public void setRecipNo(int recipNo, MapiRecipDesc recipient)  | メッセージに受信者を追加します。                                                                        |
| public void setFileNo(int fileNo, MapiFileDesc file)          | メッセージの添付ファイルを設定します。                                                                 |

### <a name="method-conversationid"></a>メソッド conversationID

メッセージが所属する会話スレッドを識別する文字列を取得または設定します。

    public str conversationID([str conversationId])

#### <a name="parameters"></a>パラメーター

conversationId  
会話スレッドの ID。省略可能。

#### <a name="return-value"></a>戻り値

メッセージが所属する会話スレッドを識別する文字列。

#### <a name="remarks"></a>備考

メッセージング システムの中には、無視してこのメンバーを返さないものがあります。

### <a name="method-datereceived"></a>メソッド dateReceived

メッセージを受信した日付を返します。

    public str dateReceived([Date theDate])

#### <a name="parameters"></a>パラメーター

theDate  
メッセージを受信した日付 (オプション)。

#### <a name="return-value"></a>戻り値

メッセージが受信された日付を示す文字列。

#### <a name="remarks"></a>備考

返される文字列の形式は、YYYY/MM/DD HH:MMであり、24時間制を使用します。

### <a name="method-flags"></a>メソッド flags

メッセージ ステータス フラグのビットを設定または取得します。

    public int flags([int flags])

#### <a name="parameters"></a>パラメーター

flags  
メッセージ ステータス フラグ (オプション)。

#### <a name="return-value"></a>戻り値

メッセージ ステータス フラグのビット。

#### <a name="remarks"></a>備考

次のフラグを設定できます。

-   \#MAPI\_RECEIPT\_REQUESTED – 受領通知のリクエストが要求されました。 クライアント アプリケーションは、メッセージを送信するときにこのビットを設定します。
-   \#MAPI\_SENT – メッセージが送信されました。
-   \#MAPI\_UNREAD – メッセージが未読です。

### <a name="method-getfileno"></a>メソッド getFileNo

メッセージからの添付ファイルを取得します。

    public MapiFileDesc getFileNo(int fileNo)

#### <a name="parameters"></a>パラメーター

fileNo  
取得する添付ファイルのインデックス。 インデックスは 1 から始まり、numFiles メソッドを使用して添付ファイルの総数を取得できます。

#### <a name="return-value"></a>戻り値

添付ファイルに関する情報を含む MapiFileDesc オブジェクトを返します。

#### <a name="remarks"></a>備考

添付ファイルは、MapiFileDesc オブジェクトで返されます。

#### <a name="examples"></a>例

    { 
        MapiFileDesc attachment; 
        MapiMessage message; 
        // Retrieve message. 
        // ...  
        if (message.NumFiles() >= 1) 
        { 
            attachment = message.GetFileNo(1); 
        } 
    }

### <a name="method-getrecipno"></a>メソッド getRecipNo

MapiRecipDesc オブジェクトにあるメッセージの受信者に関する情報を取得します。

    public MapiRecipDesc getRecipNo(int recipentNo)

#### <a name="parameters"></a>パラメーター

recipentNo  
取得する受信者の番号。 番号付けは 1 から始まり、numRecips メソッドを使用して受信者の総数を読み込むことができます。

#### <a name="return-value"></a>戻り値

受信者または nullNothingnullptrunita null 参照 (Visual Basic にはなし) を説明する MapiRecipDesc オブジェクト。

### <a name="method-messagetype"></a>メソッド messageType

IPM (個人間メッセージ) タイプではないメッセージを示す文字列を取得または設定します。

    public str messageType([str messageType])

#### <a name="parameters"></a>パラメーター

messageType  
メッセージに設定する messageType 値 (オプション)。

#### <a name="return-value"></a>戻り値

messagetype 文字列。

#### <a name="remarks"></a>備考

アプリケーションは、IPM ではないメッセージのメッセージ タイプを選択できます。 IPM だけをサポートするクライアントは、メッセージを読むときに MessageType メンバーを無視し、メッセージを送信するときに空にすることができます。

### <a name="method-numfiles"></a>メソッド numFiles

    public int numFiles([int numFiles])

#### <a name="parameters"></a>パラメーター

numFiles  

#### <a name="return-value"></a>戻り値

### <a name="method-numrecips"></a>メソッド numRecips

    public int numRecips([int numRecips])

#### <a name="parameters"></a>パラメーター

numRecips  

#### <a name="return-value"></a>戻り値

### <a name="method-originator"></a>メソッド originator

    public MapiRecipDesc originator([MapiRecipDesc originator])

#### <a name="parameters"></a>パラメーター

originator  

#### <a name="return-value"></a>戻り値

### <a name="method-subject"></a>メソッド subject

    public str subject([str subject])

#### <a name="parameters"></a>パラメーター

subject  

#### <a name="return-value"></a>戻り値

### <a name="method-text"></a>メソッド text

    public str text([str text])

#### <a name="parameters"></a>パラメーター

テキスト  

#### <a name="return-value"></a>戻り値

### <a name="method-new"></a>メソッド new

MapiMessage クラスのインスタンスを初期化します。

    public void new()

### <a name="method-finalize"></a>メソッド finalize

    public void finalize()

### <a name="method-setrecipno"></a>メソッド setRecipNo

メッセージに受信者を追加します。

    public void setRecipNo(int recipNo, MapiRecipDesc recipient)

#### <a name="parameters"></a>パラメーター

recipNo  
受信者を説明する MapiRecipDesc オブジェクト。

<!-- -->

recipient  
受信者を説明する MapiRecipDesc オブジェクト。

#### <a name="remarks"></a>備考

正しい MapiRecipDesc オブジェクトをユーザーが入力した名前から取得する必要がある場合は、resolveName メソッドを使用します。

### <a name="method-setfileno"></a>メソッド setFileNo

メッセージの添付ファイルを設定します。

    public void setFileNo(int fileNo, MapiFileDesc file)

#### <a name="parameters"></a>パラメーター

fileNo  
添付ファイルを説明する MapiFileDesc オブジェクト。

<!-- -->

ファイル  
添付ファイルを説明する MapiFileDesc オブジェクト。

#### <a name="remarks"></a>備考

添付ファイルには、1 から始まる番号が付けられます。 したがって、最初の添付ファイルには番号 1 を付ける必要があります。 numFiles メソッドを呼び出してアタッチメントの数を取得することができます。

#### <a name="examples"></a>例

    { 
        MapiMessage msg = new MapiMessage(); 
        MapiFileDesc attachment = new MapiFileDesc(); 
        attachment.Path("C:\\files\\info.txt"); 
        msg.SetFileNo(1,attachment); 
    }

## <a name="class-mapirecipdesc"></a>クラス MapiRecipDesc
    class MapiRecipDesc extends Object

### <a name="remarks"></a>備考

### <a name="examples"></a>例

### <a name="methods"></a>メソッド

| 方法                                    | 説明                                                                                                                                   |
|-------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| public str address(\[str Address\])       |                                                                                                                                               |
| public str name(\[str Name\])             | フォーム、レポート、テーブル、クエリ、または別の Finance and Operations アプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。 |
| public int recipClass(\[int RecipClass\]) |                                                                                                                                               |
| public void new()                         | MapiRecipDesc クラスの新しいインスタンスを初期化します。                                                                                        |
| public void finalize()                    |                                                                                                                                               |

### <a name="method-address"></a>メソッド address

    public str address([str Address])

#### <a name="parameters"></a>パラメーター

アドレス  

#### <a name="return-value"></a>戻り値

### <a name="method-name"></a>メソッド名

フォーム、レポート、テーブル、クエリ、または別の Finance and Operations アプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。

    public str name([str Name])

#### <a name="parameters"></a>パラメーター

氏名  

#### <a name="return-value"></a>戻り値

アプリケーション オブジェクトを識別するためにコードで使用される名前。

#### <a name="remarks"></a>備考

オブジェクトの名前プロパティ値は、コードの競合を避けるために、次の基準を満たしている必要があります。

-   文字で始めます。
-   250 文字を超えないでください。
-   数字とアンダースコア文字を含めることができます。
-   句読点やスペースを含めることはできません。
-   テーブルは、拡張データ型、基本列挙型、クラスなどの他のパブリック オブジェクトと同じ名前を持つことはできません。

### <a name="method-recipclass"></a>メソッド recipClass

    public int recipClass([int RecipClass])

#### <a name="parameters"></a>パラメーター

RecipClass  

#### <a name="return-value"></a>戻り値

### <a name="method-new"></a>メソッド new

MapiRecipDesc クラスの新しいインスタンスを初期化します。

    public void new()

### <a name="method-finalize"></a>メソッド finalize

    public void finalize()

## <a name="class-mapiterator"></a>クラス MapIterator
    class MapIterator extends Object

MapIterator クラスは、マップ内の要素を反復処理するために使用されます。

### <a name="remarks"></a>備考

マップ反復子は、マップ内で要素を反復処理するために使用されます。 これらは、反復処理する対象となるマップにシンプルなポインターとして表示することができます。 繰り返しを開始する機能は利用可能であり、より多くの (キー、値) の組み合わせが利用可能であるかどうかを決定し、繰り返しによりポイントされる要素をフェッチします。 MapIterator クラスよりも MapEnumerator クラスを使用することをお勧めします。 マップ反復子および反復処理するマップは、同じクライアント/サーバー側にある必要があります。 MapIterator クラスを使用し、コードが Called from としてマークされている場合、マップと反復子が別の層で終了する可能性があり、コードは失敗します。 MapEnumerator クラスを使用する場合、列挙子はマップと同じ層に自動的に作成されます。 また、MapIterator クラスを使用する場合、より多くおよび次のメソッドを明示的に呼び出して、マップに次の項目を移動する必要があります。 MapEnumerator クラスを使用する場合、moveNext メソッドを呼び出すだけです。 要素が挿入されるシーケンスは、挿入の順序を決定しません。 順序は、要素の順序によって定義されます。 上位キーを持つ要素の前に、下位キーを持つ要素が表示されます。 型の通常の順序が使用されます。 ただし、キーがオブジェクトである場合、オブジェクトのアドレスを使用して順序が指定されるため、特定の順序を推測することはできません。 オブジェクトのアドレスは、本来、一時的です。

### <a name="examples"></a>例

次の例では、マップを作成し、3 つの (キー、値) のペアを追加します。 マップを通じて反復処理し、各マップ要素に関する情報を印刷します。

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

### <a name="methods"></a>メソッド

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

### <a name="method-definitionstring"></a>メソッド definitionString

"\[int -&gt; str\] 反復子" など、反復子の型のテキスト表現を取得します。

    public str definitionString()

#### <a name="return-value"></a>戻り値

反復子を説明する文字列。

### <a name="method-domainvalue"></a>メソッド domainValue

反復子により参照される (キー、値) ペアにおけるキーの値を返します。

    public AnyType domainValue()

#### <a name="return-value"></a>戻り値

反復子によって現在参照されているマップ要素の最初の項目の値。

### <a name="method-find"></a>メソッド find

指定したキー値を検索します。

    public boolean find(AnyType value)

#### <a name="parameters"></a>パラメーター

値  
検索する値。

#### <a name="return-value"></a>戻り値

値が見つかった場合は true。それ以外の場合は、false。

#### <a name="remarks"></a>備考

True が返された場合、このメソッドは、反復子を要素に配置します。それ以外の場合、MapIterator.more メソッドは false を返します。

### <a name="method-key"></a>メソッド key

反復子により参照される (キー、値) ペアからキーを返します。

    public AnyType key()

#### <a name="return-value"></a>戻り値

マップ反復子によって示されるマップ エントリのキー値。

#### <a name="remarks"></a>備考

マップ要素のキー値を取得する前に要素が存在するかどうかをテストするには、SetIterator.more メソッドを使用します。

#### <a name="examples"></a>例

次の例では、マップを反復処理し、マップ内のすべての要素の説明を返します。

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

### <a name="method-more"></a>メソッド more

反復子が有効な (キー、値 ) ペアを検出するかどうかを決定します。

    public boolean more()

#### <a name="return-value"></a>戻り値

より多くの (キー、値) の組み合わせがマップで使用可能な場合は true。それ以外の場合は、false。

#### <a name="remarks"></a>備考

more メソッドが false を返すときに反復子が指す要素にアクセスしようとするとエラーが発生します。 より多くのメソッドは、反復子が有効な要素を指しているかどうかだけをテストします。 マップにより多くの要素があるかどうかはテストされません。

#### <a name="examples"></a>例

次の例では、more メソッドを使用してマップ内の要素がまだ存在するかどうかを調べることによって、マップを反復処理します。 マップ内のすべての要素の説明を返します。

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

### <a name="method-rangevalue"></a>メソッド rangeValue

反復子により参照される (キー、値) ペアにおける値の値を返します。

    public AnyType rangeValue()

#### <a name="return-value"></a>戻り値

反復子によって現在参照されているマップ要素の 2 番目の項目の値。

#### <a name="remarks"></a>備考

rangeValue メソッドは MapIterator.value メソッドと同じ機能を持ちますが、domainValue メソッドに対応するメソッドとして使用できます。

### <a name="method-tostring"></a>メソッド toString

反復子のテキスト表現を取得します。

    public str toString()

#### <a name="return-value"></a>戻り値

反復子を説明する文字列。

#### <a name="remarks"></a>備考

反復子がセット内の最初の要素をポイントする場合、文字列にはこの表現が次のフォームで含まれます: "(開始)\[ *値*\]" 反復子が要素をポイントしている場合 (つまり、MapIterator.more メソッドが false を返す場合)、返される文字列は「(終了)」になります。 反復子が値をポイントしている場合、文字列は "\[*値*\]" で、*値*が要素値の文字列表現です。

#### <a name="examples"></a>例

次の例では、整数またはクラス マップを反復処理し、各マップ要素に関する情報を出力します。 MapIterator.toString メソッドを使用して各マップ要素でのクラスのテキスト表現を返します。

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

### <a name="method-value"></a>メソッド value

反復子により参照される (キー、値) ペアから値を返します。

    public AnyType value()

#### <a name="return-value"></a>戻り値

マップ反復子によって示されるマップ要素からの値。

#### <a name="remarks"></a>備考

マップ要素のキー値を取得する前に要素が存在するかどうかをテストするには、MapIterator.more メソッドを使用します。

#### <a name="examples"></a>例

次の例では、マップを反復処理し、マップ内のすべての要素のリストを返します。

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

### <a name="method-valuepair"></a>メソッド valuePair

キーと値を保持するコンテナーを取得します。

    public container valuePair()

#### <a name="return-value"></a>戻り値

キーと値を保持するコンテナーです。

#### <a name="remarks"></a>備考

オブジェクトをコンテナーに配置することはできません。 したがって、キーまたは値のいずれかがオブジェクトである場合、例外が発生します。

### <a name="method-next"></a>メソッド next

次の (キー、値) ペアに反復子を移動します。

    public void next()

#### <a name="remarks"></a>備考

MapIterator.more メソッドを使用すると、マップ内にさらに要素があるかどうか判断することができます。

#### <a name="examples"></a>例

次の例では、next メソッドを使用してマップを反復処理し、マップ内のすべての要素のリストを返します。

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

### <a name="method-new"></a>メソッド new

マップ内の要素をスキャンできるマップの新しい反復子を作成します。

    public void new(Map map)

#### <a name="parameters"></a>パラメーター

マップ  
反復子を作成するマップ。

#### <a name="remarks"></a>備考

反復子は、マップが空でない場合、マップの最初の値に配置されます。

#### <a name="examples"></a>例

次の例では、(整数、クラス) のペアのマップを作成し、マップを移動する反復子を作成します。

    Map iim = new Map(Types::Integer, Types::Class); 
    MapIterator it; 
    it = new MapIterator (iim);

### <a name="method-begin"></a>メソッド begin

反復子をマップの先頭に移動します。

    public void begin()

#### <a name="remarks"></a>備考

新しく作成されるマップ反復子は、マップの最初の要素に配置されるため、セットを通じて反復する前に開始メソッドを呼び出す必要はありません。 ポインターをリセットする場合は、開始メソッドを呼び出す必要があります。

### <a name="method-end"></a>メソッド end

マップで最後の要素の後に反復子を移動します。

    public void end()

#### <a name="remarks"></a>備考

このメソッドを実行すると、MapIterator.more メソッドが false に戻ります。

### <a name="method-delete"></a>メソッド delete

反復子によってポイントされている要素をマップから削除します。

    public void delete()

#### <a name="remarks"></a>備考

反復子は、delete メソッドが呼び出された後に次の要素を指します。

## <a name="class-memberfunction"></a>クラス MemberFunction
    class MemberFunction extends TreeNode

MemberFunction クラスは、フォーム、レポート、クラスなどの Finance and Operations アプリケーション オブジェクト ツリー (AOT) で指定されたノードに関する情報を提供します。

### <a name="remarks"></a>備考

このクラスでは、作成、読み取り、更新、および X++ コードとメタデータを削除できます。 この API が呼び出される前に、ユーザーが開発セキュリティ キー (SysDevelopment) にアクセスできることを確認します。 ::findNode メソッドを使用すると MemberFunction クラスのインスタンスにノードを割り当てることができます。

### <a name="examples"></a>例

次の例では、TreeNode::findNode メソッドを使用して、AddressSelectForm.callerDataSource メソッドのノードを MemberFunction クラスのインスタンスに割り当てます。 MemberFunction.AOTgetSource メソッドは、メソッドのソース コードを返します。

    void getMemberFunction() 
    { 
        MemberFunction memberFunction; 
        str name; 
        boolean isStatic; 
        str source; 
        try 
        { 
            memberFunction = TreeNode::findNode( 
               '\\Classes\\AddressSelectForm\\callerDataSource'); 
            if(!memberFunction) 
            { 
                throw exception::Error; 
            } 
            source = memberFunction.AOTgetSource(); 
            print source; 
            pause; 
        } 
        catch (exception::Error) 
        { 
            print "The specified node does not exist."; 
            pause; 
            } 
        } 
    }

### <a name="methods"></a>メソッド

| 方法                                                     | 説明                                                                                                                             |
|------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| public str AOTgetSource()                                  | クラスやメソッドなど、AOT 内で指定したノードのソース コードを提供します。                                                    |
| public boolean canAddEventHandler()                        |                                                                                                                                         |
| public boolean isEvent()                                   |                                                                                                                                         |
| public boolean isStatic()                                  | メソッドが静的かどうかを示します。                                                                                                   |
| public str name(\[str value\])                             | フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。 |
| public void AOTedit(\[int Line\], \[int Column\])          | AOT で指定したノードの適切なエディタを開きます。                                                                           |
| public void new()                                          | MemberFunction クラスの新しいインスタンスを初期化します。                                                                                 |
| public void AOTsetSource(str source, \[boolean isStatic\]) | クラスやメソッドなど、AOT 内で指定したノードのソース コードを設定します。                                                        |

### <a name="method-aotgetsource"></a>メソッド AOTgetSource

クラスやメソッドなど、AOT 内で指定したノードのソース コードを提供します。

    public str AOTgetSource()

#### <a name="return-value"></a>戻り値

ソース コードの文字列値、ノードにソース コードが含まれていない場合、nullNothingnullptrunita null 参照 (Visual Basic にはなし)。

### <a name="method-canaddeventhandler"></a>メソッド canAddEventHandler

    public boolean canAddEventHandler()

#### <a name="return-value"></a>戻り値

### <a name="method-isevent"></a>メソッド isEvent

    public boolean isEvent()

#### <a name="return-value"></a>戻り値

### <a name="method-isstatic"></a>メソッド isStatic

メソッドが静的かどうかを示します。

    public boolean isStatic()

#### <a name="return-value"></a>戻り値

メソッドが静的である場合は true。それ以外の場合は、false。

#### <a name="remarks"></a>備考

このメソッドは、AOT の指定されたノード (フォーム、レポート、クラスなど) に関連付けられます。 このメソッドは、主に MemberFunction :: AOTsetSource メソッドと組み合わせて使用されます。

### <a name="method-name"></a>メソッド名

フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。

    public str name([str value])

#### <a name="parameters"></a>パラメーター

値  
ノードを指定する文字列、オプション。

#### <a name="return-value"></a>戻り値

アプリケーション オブジェクトを識別するためにコードで使用される名前。

#### <a name="remarks"></a>備考

オブジェクトの名前プロパティ値は、コードの競合を避けるために、次の基準を満たしている必要があります。

-   文字で始めます。
-   250 文字を超えていません。
-   数字とアンダースコア (\_) 文字を含めることができます。
-   句読点やスペースを含めることはできません。
-   テーブルは、拡張データ型、基本列挙型、およびクラスなどの他のパブリック オブジェクトと同じ名前を持つことはできません。

### <a name="method-aotedit"></a>メソッド AOTedit

AOT で指定したノードの適切なエディタを開きます。

    public void AOTedit([int Line], [int Column])

#### <a name="parameters"></a>パラメーター

明細行  
カーソルの列の位置を指定する整数。オプション。

<!-- -->

円柱  
カーソルの列の位置を指定する整数。オプション。

### <a name="method-new"></a>メソッド new

MemberFunction クラスの新しいインスタンスを初期化します。

    public void new()

### <a name="method-aotsetsource"></a>メソッド AOTsetSource

クラスやメソッドなど、AOT 内で指定したノードのソース コードを設定します。

    public void AOTsetSource(str source, [boolean isStatic])

#### <a name="parameters"></a>パラメーター

ソース  
ブール値: 静的メソッドの場合は true、インスタンス メソッドの場合は false; オプション。

<!-- -->

isStatic  
ブール値: 静的メソッドの場合は true、インスタンス メソッドの場合は false; オプション。

## <a name="class-menu"></a>クラス メニュー
    class Menu extends TreeNode

メニュー システム クラスを使用すると、Finance and OperationsMenu オブジェクトのいずれかをコードから構成および実行できます。

### <a name="remarks"></a>備考

TreeNode システム クラスは、Finance and Operations アプリケーション オブジェクト ツリー (AOT) で、メニューへのより一般的なアプローチとして機能します。 サブメニューやメニュー項目などのメニュー内容を作成または操作するには、Menu クラスを使用します。 このクラスでは、作成、読み取り、更新、および X++ コードとメタデータを削除できます。 この API が呼び出される前に、ユーザーが開発セキュリティ キー (SysDevelopment) にアクセスできることを確認します。

### <a name="examples"></a>例

### <a name="methods"></a>メソッド

| 方法                                                                   | 説明                                                                                                               |
|--------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| public str changedBy(\[str value\])                                      | アプリケーション オブジェクトを最後に変更したユーザーの名前を取得または設定します。                                                |
| public Date changedDate(\[Date value\])                                  | アプリケーション オブジェクトが最後に変更された日付を取得または設定します。                                                             |
| public str changedTime(\[str value\])                                    | アプリケーション オブジェクトが最後に変更された時刻を取得または設定します。                                                             |
| public ConfigurationKeyId configurationKey(\[ConfigurationKeyId value\]) | コントロールに割り当てられるコンフィギュレーション キーを取得または設定します。                                                       |
| public str countryRegionCodes(\[str value\])                             |                                                                                                                           |
| public str createdBy(\[str value\])                                      | アプリケーション オブジェクトを作成したユーザーの名前を取得または設定します。                                                     |
| public Date creationDate(\[Date value\])                                 | アプリケーション オブジェクトが作成された日付を取得または設定します。                                                                  |
| public str creationTime(\[str value\])                                   |                                                                                                                           |
| public str disabledImage(\[str value\])                                  | コントロールの無効な画像を取得または設定します。                                                                            |
| public int disabledImageLocation(\[int value\])                          |                                                                                                                           |
| public int disabledResource(\[int value\])                               | 無効なボタン画像として使用する画像リソース ID を取得または設定します。                                            |
| public int imageLocation(\[int value\])                                  |                                                                                                                           |
| public str label(\[str value\])                                          | コントロールのラベルを取得または設定します。                                                                                     |
| public str menuFunctionName(\[str name\])                                |                                                                                                                           |
| public str menuItemName(\[str value\])                                   |                                                                                                                           |
| public MenuItemType menuItemType(\[MenuItemType value\])                 |                                                                                                                           |
| public str menuName()                                                    |                                                                                                                           |
| public str name(\[str value\])                                           | フォーム、レポート、テーブル、クエリ、または別の MSDAX アプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。 |
| public int neededAccessLevel(\[int value\])                              | MenuFunction クラスの neededAccessLevel プロパティを取得または設定します。                                                   |
| public str normalImage(\[str value\])                                    |                                                                                                                           |
| public int normalResource(\[int value\])                                 |                                                                                                                           |
| public Guid origin(\[Guid value\])                                       |                                                                                                                           |
| public str parameter(\[str parameter\])                                  |                                                                                                                           |
| public str parameters(\[str value\])                                     | MenuFunction クラスで実行されるオブジェクトに渡されるパラメータの一覧を取得または設定します。                    |
| public SecurityKeyId securityKey(\[SecurityKeyId value\])                |                                                                                                                           |
| public boolean setCompany(\[boolean value\])                             |                                                                                                                           |
| public str shortCut(\[str value\])                                       |                                                                                                                           |
| public boolean showParentModule(\[boolean value\])                       |                                                                                                                           |
| public boolean visible(\[boolean value\])                                |                                                                                                                           |
| public str webTarget(\[str value\])                                      |                                                                                                                           |
| public void save()                                                       |                                                                                                                           |
| public void new(str Name)                                                | TreeNode クラスの新しいインスタンスを初期化します。                                                                         |
| public void makeWebMenu(Object outputClass)                              |                                                                                                                           |
| public void addMenuitem(xMenuFunction menuFunction)                      | メニューにメニュー項目を追加します。                                                                                             |
| public void setTreeNodeName(str name)                                    |                                                                                                                           |
| public void addMenuReference(Menu menu)                                  |                                                                                                                           |
| public void addSubmenu(str name)                                         | メニューにサブメニューを追加します。                                                                                               |
| public void addSeparator()                                               | メニューにメニューの区切りを追加します。                                                                                        |

### <a name="method-changedby"></a>メソッド changedBy

アプリケーション オブジェクトを最後に変更したユーザーの名前を取得または設定します。

    public str changedBy([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

ユーザーの名前。

### <a name="method-changeddate"></a>メソッド changedDate

アプリケーション オブジェクトが最後に変更された日付を取得または設定します。

    public Date changedDate([Date value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

アプリケーション オブジェクトが最後に変更された日付。

### <a name="method-changedtime"></a>メソッド changedTime

アプリケーション オブジェクトが最後に変更された時刻を取得または設定します。

    public str changedTime([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

アプリケーション オブジェクトが最後に変更された時間。

### <a name="method-configurationkey"></a>メソッド configurationKey

コントロールに割り当てられるコンフィギュレーション キーを取得または設定します。

    public ConfigurationKeyId configurationKey([ConfigurationKeyId value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

コントロールに割り当てられるコンフィギュレーションの ID。

#### <a name="remarks"></a>備考

コンフィギュレーション キーは、このコントロールを表示するかどうかを決定するために使用されます。 コンフィギュレーション キーがシステムで無効な場合、コントロールはフォームで表示されません。

### <a name="method-countryregioncodes"></a>メソッド countryRegionCodes

    public str countryRegionCodes([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-createdby"></a>メソッド createdBy

アプリケーション オブジェクトを作成したユーザーの名前を取得または設定します。

    public str createdBy([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

ユーザーの名前。

### <a name="method-creationdate"></a>メソッド creationDate

アプリケーション オブジェクトが作成された日付を取得または設定します。

    public Date creationDate([Date value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

アプリケーション オブジェクトが作成された日付。

### <a name="method-creationtime"></a>メソッド creationTime

    public str creationTime([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-disabledimage"></a>メソッド disabledImage

コントロールの無効な画像を取得または設定します。

    public str disabledImage([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

画像ファイルのフル ネーム。 システムは、GDI でサポートされているすべてのイメージ形式をサポートしています。

#### <a name="remarks"></a>備考

このプロパティは、disabledResource プロパティに優先します。 これらのプロパティの両方が設定されている場合に使用されます。

### <a name="method-disabledimagelocation"></a>メソッド disabledImageLocation

    public int disabledImageLocation([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-disabledresource"></a>メソッド disabledResource

無効なボタン画像として使用する画像リソース ID を取得または設定します。

    public int disabledResource([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

無効なボタン画像として使用する画像リソース ID。 アイコンとビットマップ イメージの両方がサポートされます。

### <a name="method-imagelocation"></a>メソッド imageLocation

    public int imageLocation([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-label"></a>メソッド label

コントロールのラベルを取得または設定します。

    public str label([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

ラベル文字列の現在の値。

#### <a name="remarks"></a>備考

ラベルは、コントロール内に表示されているテキストまたはそれに隣接するテキストを指定します。 ラベルのプロパティ値は 250 文字を超えることはできません。

### <a name="method-menufunctionname"></a>メソッド menuFunctionName

    public str menuFunctionName([str name])

#### <a name="parameters"></a>パラメーター

名前  

#### <a name="return-value"></a>戻り値

### <a name="method-menuitemname"></a>メソッド menuItemName

    public str menuItemName([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-menuitemtype"></a>メソッド menuItemType

    public MenuItemType menuItemType([MenuItemType value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-menuname"></a>メソッド menuName

    public str menuName()

#### <a name="return-value"></a>戻り値

### <a name="method-name"></a>メソッド名

フォーム、レポート、テーブル、クエリ、または別の MSDAX アプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。

    public str name([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

アプリケーション オブジェクトを識別するためにコードで使用される名前。

#### <a name="remarks"></a>備考

オブジェクトの名前プロパティ値は、コードの競合を避けるために、次の基準を満たしている必要があります。

-   文字で始めます。
-   250 文字を超えないでください。
-   数字とアンダースコア文字を含めることができます。
-   句読点やスペースを含めることはできません。
-   テーブルは、拡張データ型、基本列挙型、クラスなどの他のパブリック オブジェクトと同じ名前を持つことはできません。

### <a name="method-neededaccesslevel"></a>メソッド neededAccessLevel

MenuFunction クラスの neededAccessLevel プロパティを取得または設定します。

    public int neededAccessLevel([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

neededAccessLevel プロパティの現在の値。

#### <a name="remarks"></a>備考

AccessType システム列挙値の使用可能な値は次のとおりです。

-   AccessType::NoAccess.
-   AccessType::View.
-   AccessType::Edit.
-   AccessType::Add.
-   AccessType::Delete.

### <a name="method-normalimage"></a>メソッド normalImage

    public str normalImage([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-normalresource"></a>メソッド normalResource

    public int normalResource([int value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-origin"></a>メソッド origin

    public Guid origin([Guid value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-parameter"></a>メソッド parameter

    public str parameter([str parameter])

#### <a name="parameters"></a>パラメーター

パラメーター  

#### <a name="return-value"></a>戻り値

### <a name="method-parameters"></a>メソッド parameters

MenuFunction クラスで実行されるオブジェクトに渡されるパラメータの一覧を取得または設定します。

    public str parameters([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

オブジェクトに渡されるパラメーターのリスト。

#### <a name="remarks"></a>備考

パラメータ文字列形式は、パラメーター 1 = 値 1、パラメーター 2 = 値 2、.... というようになります。 オブジェクトは、渡された未認識のパラメーターを無視します。

### <a name="method-securitykey"></a>メソッド securityKey

    public SecurityKeyId securityKey([SecurityKeyId value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-setcompany"></a>メソッド setCompany

    public boolean setCompany([boolean value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-shortcut"></a>メソッド shortCut

    public str shortCut([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-showparentmodule"></a>メソッド showParentModule

    public boolean showParentModule([boolean value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-visible"></a>メソッド visible

    public boolean visible([boolean value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-webtarget"></a>メソッド webTarget

    public str webTarget([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-save"></a>メソッド save

    public void save()

### <a name="method-new"></a>メソッド new

TreeNode クラスの新しいインスタンスを初期化します。

    public void new(str Name)

#### <a name="parameters"></a>パラメーター

氏名  

### <a name="method-makewebmenu"></a>メソッド makeWebMenu

    public void makeWebMenu(Object outputClass)

#### <a name="parameters"></a>パラメーター

outputClass  

### <a name="method-addmenuitem"></a>メソッド addMenuitem

メニューにメニュー項目を追加します。

    public void addMenuitem(xMenuFunction menuFunction)

#### <a name="parameters"></a>パラメーター

menuFunction  
追加するメニュー項目。

### <a name="method-settreenodename"></a>メソッド setTreeNodeName

    public void setTreeNodeName(str name)

#### <a name="parameters"></a>パラメーター

名前  

### <a name="method-addmenureference"></a>メソッド addMenuReference

    public void addMenuReference(Menu menu)

#### <a name="parameters"></a>パラメーター

メニュー  

### <a name="method-addsubmenu"></a>メソッド addSubmenu

メニューにサブメニューを追加します。

    public void addSubmenu(str name)

#### <a name="parameters"></a>パラメーター

名前  
メニューに追加するサブメニューの名前に評価される文字列式。

### <a name="method-addseparator"></a>メソッド addSeparator

メニューにメニューの区切りを追加します。

    public void addSeparator()

## <a name="class-menuitem"></a>クラス MenuItem
    class MenuItem extends TreeNode

MenuItem クラスを使用すると、X++ コードとメタデータの作成、読み取り、更新、および削除を行うことができます。

### <a name="remarks"></a>備考

メニュー項目は、メニュー機能のユーザー インターフェイスを表します。 メニュー項目は、ユーザーがメニュー項目を選択するときに実行される MenuFunction オブジェクトにリンクされます。 この API が呼び出される前に、ユーザーが開発セキュリティ キー (SysDevelopment) にアクセスできることを確認します。

### <a name="examples"></a>例

### <a name="methods"></a>メソッド

| 方法                                                     | 説明                                                                                                                                   |
|------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| public str allowRootNavigation(\[str value\])              |                                                                                                                                               |
| public boolean isDisplayedInContentArea(\[boolean value\]) |                                                                                                                                               |
| public str label(\[str name\])                             |                                                                                                                                               |
| public str menuFunctionName(\[str name\])                  |                                                                                                                                               |
| public str menuItemName(\[str value\])                     |                                                                                                                                               |
| public MenuItemType menuItemType(\[MenuItemType value\])   |                                                                                                                                               |
| public str name(\[str value\])                             | フォーム、レポート、テーブル、クエリ、または別の Finance and Operations アプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。 |
| public str parameter(\[str parameter\])                    |                                                                                                                                               |
| public str parameters(\[str value\])                       | MenuFunction クラスで実行されるオブジェクトに渡されるパラメータの一覧を取得または設定します。                                        |
| public str shortCut(\[str value\])                         |                                                                                                                                               |
| public boolean showParentModule(\[boolean value\])         |                                                                                                                                               |
| public boolean visible(\[boolean value\])                  |                                                                                                                                               |
| public str webTarget(\[str value\])                        |                                                                                                                                               |

### <a name="method-allowrootnavigation"></a>メソッド allowRootNavigation

    public str allowRootNavigation([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-isdisplayedincontentarea"></a>メソッド isDisplayedInContentArea

    public boolean isDisplayedInContentArea([boolean value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-label"></a>メソッド label

    public str label([str name])

#### <a name="parameters"></a>パラメーター

名前  

#### <a name="return-value"></a>戻り値

### <a name="method-menufunctionname"></a>メソッド menuFunctionName

    public str menuFunctionName([str name])

#### <a name="parameters"></a>パラメーター

名前  

#### <a name="return-value"></a>戻り値

### <a name="method-menuitemname"></a>メソッド menuItemName

    public str menuItemName([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-menuitemtype"></a>メソッド menuItemType

    public MenuItemType menuItemType([MenuItemType value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-name"></a>メソッド名

フォーム、レポート、テーブル、クエリ、または別の Finance and Operations アプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。

    public str name([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

アプリケーション オブジェクトを識別するためにコードで使用される名前。

#### <a name="remarks"></a>備考

オブジェクトの名前プロパティ値は、コードの競合を避けるために、次の基準を満たしている必要があります。

-   文字で始めます。
-   250 文字を超えないでください。
-   数字とアンダースコア文字を含めることができます。
-   句読点やスペースを含めることはできません。
-   テーブルは、拡張データ型、基本列挙型、クラスなどの他のパブリック オブジェクトと同じ名前を持つことはできません。

### <a name="method-parameter"></a>メソッド parameter

    public str parameter([str parameter])

#### <a name="parameters"></a>パラメーター

パラメーター  

#### <a name="return-value"></a>戻り値

### <a name="method-parameters"></a>メソッド parameters

MenuFunction クラスで実行されるオブジェクトに渡されるパラメータの一覧を取得または設定します。

    public str parameters([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

オブジェクトに渡されるパラメーターのリスト。

#### <a name="remarks"></a>備考

パラメータ文字列形式は、パラメーター 1 = 値 1、パラメーター 2 = 値 2、.... というようになります。 オブジェクトは、渡された未認識のパラメーターを無視します。

### <a name="method-shortcut"></a>メソッド shortCut

    public str shortCut([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-showparentmodule"></a>メソッド showParentModule

    public boolean showParentModule([boolean value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-visible"></a>メソッド visible

    public boolean visible([boolean value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

### <a name="method-webtarget"></a>メソッド webTarget

    public str webTarget([str value])

#### <a name="parameters"></a>パラメーター

値  

#### <a name="return-value"></a>戻り値

## <a name="class-menureference"></a>クラス MenuReference
    class MenuReference extends TreeNode

MenuReference クラスを使用すると、X++ コードとメタデータの作成、読み取り、更新、および削除を行うことができます。

### <a name="remarks"></a>備考

### <a name="examples"></a>例

### <a name="methods"></a>メソッド

| 方法                | 説明 |
|-----------------------|-------------|
| public str menuName() |             |

### <a name="method-menuname"></a>メソッド menuName

    public str menuName()

#### <a name="return-value"></a>戻り値

## <a name="class-messagewin"></a>クラス MessageWin
    class MessageWin extends Object

MessageWin クラスを使用すると、Finance and Operations 開発環境の messageWindow クラスにアクセスできます。

### <a name="remarks"></a>備考

さらに MessageWin オブジェクトをインスタンス化することができますが、画面上に同一のメッセージ ウィンドウを参照します。

### <a name="examples"></a>例

### <a name="methods"></a>メソッド

| 方法                        | 説明                                           |
|-------------------------------|-------------------------------------------------------|
| public void clear()           | メッセージ ウィンドウをクリアします。                            |
| public void activate()        | メッセージ ウィンドウを現在のアクティブ ウィンドウにします。 |
| public void addLine(str line) | 行をメッセージ ウィンドウに記述します。                  |

### <a name="method-clear"></a>メソッド clear

メッセージ ウィンドウをクリアします。

    public void clear()

### <a name="method-activate"></a>メソッド activate

メッセージ ウィンドウを現在のアクティブ ウィンドウにします。

    public void activate()

#### <a name="remarks"></a>備考

バージョン 2.11 より前に、行が追加されたり内容が消去されるとメッセージ ウィンドウがフォーカスを取得します。 バージョン 2.11 以降では、開発者は、メッセージ ウィンドウを一番上のウィンドウにするためにこのメソッドを呼び出す必要があります。

### <a name="method-addline"></a>メソッド addLine

行をメッセージ ウィンドウに記述します。

    public void addLine(str line)

#### <a name="parameters"></a>パラメーター

明細行  
メッセージ ウィンドウへの書き込み明細行を含む文字列。

## <a name="class-methodinfo"></a>クラス MethodInfo
    class MethodInfo extends Object

指定したメソッドについて説明します。

### <a name="remarks"></a>備考

SysDictTable クラスを使用してテーブル メソッドを MethodInfo に割り当てます。 SysDictClass クラスを使用してクラス メソッドを割り当てます。 次のクラスは MethodInfo を拡張しています。

-   SysMethodInfo
-   DictMethod

### <a name="examples"></a>例

次の例では、SysDictClass::ObjectMethodObject メソッドを使用して、FormBuildDataSource クラス オブジェクトのメソッドをMethodInfo クラスのインスタンスに割り当てます。 整数値はメソッドを指定します。 MethodInfo.name メソッドは、メソッド名を返します。

    void getMethodInfo() 
    { 
        MethodInfo methodInfo; 
        SysDictClass sysDictClass; 
        str name; 
        try 
        { 
            sysDictClass = new SysDictClass(classnum(FormBuildDataSource)); 
            methodInfo = sysDictClass.objectMethodObject(1); 
            if(!methodInfo) 
            { 
                throw exception::Error; 
            } 
            name = methodInfo.name(); 
            print name; 
            pause; 
         } 
         catch (exception::Error) 
         { 
            print "The specified method does not exist"; 
            pause; 
         } 
    }

### <a name="methods"></a>メソッド

| 方法                                                      | 説明                                                                                                                                   |
|-------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| public AccessSpecifier accessSpecifier()                    | メソッドがパブリック、保護、またはプライベートかどうかを指定します。                                                                                |
| public boolean compiledOk()                                 | メソッドがコンパイルされているかどうかを指定します。                                                                                                    |
| public TableId displayTableId()                             |                                                                                                                                               |
| public DisplayFunctionType displayType()                    | メソッドの表示機能のタイプを指定します。                                                                                              |
| public Array getAllAttributes()                             | メソッドの属性の完全なセットを取得します。                                                                                               |
| public Object getAttribute(str attribute)                   | クラス ヘッダー メタデータから最初に一致する属性を取得し、その属性を表すオブジェクト クラスのインスタンスを作成し、返します。 |
| public Array getAttributes(str attribute)                   |                                                                                                                                               |
| public boolean isAbstract()                                 | メソッドが抽象かどうかを示します。                                                                                                     |
| public boolean isStatic()                                   | メソッドが静的かどうかを指定します。                                                                                                       |
| public str name()                                           | メソッドの名前を指定します。                                                                                                               |
| public int noParms()                                        | メソッド内のパラメーターの数を指定します。                                                                                               |
| public int noVars()                                         | メソッド内の変数の数を指定します。                                                                                                |
| public int parentId()                                       | テーブル メソッドのテーブル ID またはクラス メソッドのクラス ID を指定します。                                                                 |
| public str propertyHelp()                                   | メソッドがコントロールに設定または返すヘルプ テキストを指定します。                                                                          |
| public NoYes PropertyMethod()                               | メソッドがプロパティ メソッドかどうかを指定します。                                                                                              |
| public int returnId()                                       | 値を返すメソッドについて、拡張データ型やクラスなどの特定の戻り値のデータ型の ID を指定します。                   |
| public Types returnType()                                   | メソッドの戻り値の型を指定します。                                                                                                               |
| public ClassRunMode runMode()                               | メソッドが実行される場所を指定します。                                                                                                         |
| public int varId(int variableNumber)                        | 変数を含むメソッドについて、拡張データ型や列挙値などの特定の変数のデータ型の ID を指定します。                |
| public int varIdOld(int variableNumber)                     |                                                                                                                                               |
| public Types varType(int variableNumber)                    | Types 列挙の値を使用して変数のデータ型を指定します。                                                                    |
| public void new(UtilElementType utilType, int Id, str Name) | MethodInfo クラスの新しいインスタンスを作成します。                                                                                               |
| public void setMethod(MemberFunction method)                | インスタンスを使用してアプリケーション オブジェクト ツリー (AOT) 内のノードのアプリケーション オブジェクト タイプを指定します。                            |

### <a name="method-accessspecifier"></a>メソッド accessSpecifier

メソッドがパブリック、保護、またはプライベートかどうかを指定します。

    public AccessSpecifier accessSpecifier()

#### <a name="return-value"></a>戻り値

メソッドがパブリック、保護、またはプライベートのいずれかを指定する AccessSpecifier 列挙型値です。

### <a name="method-compiledok"></a>メソッド compiledOk

メソッドがコンパイルされているかどうかを指定します。

    public boolean compiledOk()

#### <a name="return-value"></a>戻り値

メソッドがコンパイル済みの場合は true。それ以外の場合は、false。

### <a name="method-displaytableid"></a>メソッド displayTableId

    public TableId displayTableId()

#### <a name="return-value"></a>戻り値

### <a name="method-displaytype"></a>メソッド displayType

メソッドの表示機能のタイプを指定します。

    public DisplayFunctionType displayType()

#### <a name="return-value"></a>戻り値

メソッドの表示機能のタイプを示す DisplayFunctionType 列挙値。

#### <a name="remarks"></a>備考

次のテーブルに、displayType メソッドによって返される可能な値を示します。

|           |                                             |
|-----------|---------------------------------------------|
| 取得       | このメソッドは表示メソッドです。             |
| None      | このメソッドは、表示メソッドまたは編集メソッドではありません。 |
| RecordGet | このメソッドは、レコードを取得します。                   |
| RecordSet | このメソッドは、レコードを設定します。                   |
| セット       | このメソッドは、編集メソッドです。               |

### <a name="method-getallattributes"></a>メソッド getAllAttributes

メソッドの属性の完全なセットを取得します。

    public Array getAllAttributes()

#### <a name="return-value"></a>戻り値

メソッドの SysAttribute オブジェクトの配列。

### <a name="method-getattribute"></a>メソッド getAttribute

クラス ヘッダー メタデータから最初に一致する属性を取得し、その属性を表すオブジェクト クラスのインスタンスを作成し、返します。

    public Object getAttribute(str attribute)

#### <a name="parameters"></a>パラメーター

属性  
検索の対象である属性。

#### <a name="return-value"></a>戻り値

オブジェクト クラスのインスタンスとしての属性。

### <a name="method-getattributes"></a>メソッド getAttributes

    public Array getAttributes(str attribute)

#### <a name="parameters"></a>パラメーター

属性  

#### <a name="return-value"></a>戻り値

### <a name="method-isabstract"></a>メソッド isAbstract

メソッドが抽象かどうかを示します。

    public boolean isAbstract()

#### <a name="return-value"></a>戻り値

メソッドが抽象である場合は true。それ以外の場合は、false。

#### <a name="remarks"></a>備考

抽象メソッドは宣言されていますが、親クラスで実装されていません。 詳細については、「メソッド モディファイア」を参照してください。

### <a name="method-isstatic"></a>メソッド isStatic

メソッドが静的かどうかを指定します。

    public boolean isStatic()

#### <a name="return-value"></a>戻り値

メソッドが静的である場合は true。それ以外の場合は、false。

#### <a name="remarks"></a>備考

詳細については、「静的メソッド」を参照してください。

### <a name="method-name"></a>メソッド名

メソッドの名前を指定します。

    public str name()

#### <a name="return-value"></a>戻り値

メソッド名を示す文字列。

### <a name="method-noparms"></a>メソッド noParms

メソッド内のパラメーターの数を指定します。

    public int noParms()

#### <a name="return-value"></a>戻り値

メソッド内のパラメータの数を示す整数値。

### <a name="method-novars"></a>メソッド noVars

メソッド内の変数の数を指定します。

    public int noVars()

#### <a name="return-value"></a>戻り値

メソッド内の変数の数を示す整数値。

### <a name="method-parentid"></a>メソッド parentId

テーブル メソッドのテーブル ID またはクラス メソッドのクラス ID を指定します。

    public int parentId()

#### <a name="return-value"></a>戻り値

テーブル ID またはクラス ID を示す整数値。

### <a name="method-propertyhelp"></a>メソッド propertyHelp

メソッドがコントロールに設定または返すヘルプ テキストを指定します。

    public str propertyHelp()

#### <a name="return-value"></a>戻り値

ヘルプ テキストを含む文字列。

### <a name="method-propertymethod"></a>メソッド PropertyMethod

メソッドがプロパティ メソッドかどうかを指定します。

    public NoYes PropertyMethod()

#### <a name="return-value"></a>戻り値

メソッドがプロパティ メソッドの場合は 1、それ以外の場合は、0 です。

#### <a name="remarks"></a>備考

プロパティ メソッドは、プロパティを設定または返します。

### <a name="method-returnid"></a>メソッド returnId

値を返すメソッドについて、拡張データ型やクラスなどの特定の戻り値のデータ型の ID を指定します。

    public int returnId()

#### <a name="return-value"></a>戻り値

戻り値のデータ型の ID を示す整数値。

#### <a name="remarks"></a>備考

データ型に ID がない場合またはメソッドが値を返さない場合、戻り値は 0 です。

### <a name="method-returntype"></a>メソッド returnType

メソッドの戻り値の型を指定します。

    public Types returnType()

#### <a name="return-value"></a>戻り値

メソッドの戻り値を示すタイプ列挙値。

#### <a name="remarks"></a>備考

表示される値は次のとおりです。 :

-   AnyType
-   BLOB
-   クラス
-   コンテナー
-   日
-   日時
-   列挙
-   グリッド
-   Int64
-   整数
-   実数
-   レコード
-   RString
-   文字列
-   UserType
-   VarString
-   無効

### <a name="method-runmode"></a>メソッド runMode

メソッドが実行される場所を指定します。

    public ClassRunMode runMode()

#### <a name="return-value"></a>戻り値

メソッドが実行される場所を示す ClassRunMode 列挙値。

#### <a name="remarks"></a>備考

表示される値は次のとおりです。

-   呼び出された
-   クライアント
-   ClientorServer
-   サーバー

### <a name="method-varid"></a>メソッド varId

変数を含むメソッドについて、拡張データ型や列挙値などの特定の変数のデータ型の ID を指定します。

    public int varId(int variableNumber)

#### <a name="parameters"></a>パラメーター

variableNumber  
メソッドに一覧表示されている変数の順序に基づいてメソッド変数を指定する整数値。

#### <a name="return-value"></a>戻り値

変数のデータ型 ID を示す整数値。

#### <a name="remarks"></a>備考

データ型に ID がない場合またはメソッドに変数がない場合、戻り値は 0 です。

### <a name="method-varidold"></a>メソッド varIdOld

    public int varIdOld(int variableNumber)

#### <a name="parameters"></a>パラメーター

variableNumber  

#### <a name="return-value"></a>戻り値

### <a name="method-vartype"></a>メソッド varType

Types 列挙の値を使用して変数のデータ型を指定します。

    public Types varType(int variableNumber)

#### <a name="parameters"></a>パラメーター

variableNumber  
メソッドに一覧表示されている変数の順序に基づいてメソッド変数を指定する整数。

#### <a name="return-value"></a>戻り値

変数のデータ型を示すタイプ列挙値。

#### <a name="remarks"></a>備考

以下は使用可能な値です。

-   AnyType
-   BLOB
-   クラス
-   コンテナー
-   日
-   日時
-   列挙
-   グリッド
-   Int64
-   整数
-   実数
-   レコード
-   RString
-   文字列
-   UserType
-   VarString
-   無効

### <a name="method-new"></a>メソッド new

MethodInfo クラスの新しいインスタンスを作成します。

    public void new(UtilElementType utilType, int Id, str Name)

#### <a name="parameters"></a>パラメーター

utilType  
要素の名前を指定する文字列。

<!-- -->

ID  
要素の名前を指定する文字列。

<!-- -->

氏名  
要素の名前を指定する文字列。

### <a name="method-setmethod"></a>メソッド setMethod

アプリケーション オブジェクト ツリー (AOT) 内のノードのアプリケーション オブジェクト タイプを指定します。

    public void setMethod(MemberFunction method)

#### <a name="parameters"></a>パラメーター

メソッド  
AOT 内のノードを表す MemberFunction クラスのインスタンス。

## <a name="class-modifyfieldeventargs"></a>クラス ModifyFieldEventArgs
    class ModifyFieldEventArgs extends DataEventArgs

### <a name="remarks"></a>備考

### <a name="examples"></a>例

### <a name="methods"></a>メソッド

| 方法                       | 説明 |
|------------------------------|-------------|
| public int parmFieldId()     |             |
| public void new(int fieldId) |             |

### <a name="method-parmfieldid"></a>メソッド parmFieldId

    public int parmFieldId()

#### <a name="return-value"></a>戻り値

### <a name="method-new"></a>メソッド new

    public void new(int fieldId)

#### <a name="parameters"></a>パラメーター

fieldId  

## <a name="class-modifyfieldvalueeventargs"></a>クラス ModifyFieldValueEventArgs
    class ModifyFieldValueEventArgs extends DataEventArgs

### <a name="remarks"></a>備考

### <a name="examples"></a>例

### <a name="methods"></a>メソッド

| 方法                                         | 説明 |
|------------------------------------------------|-------------|
| public str parmFieldName()                     |             |
| public int parmArrayIndex()                    |             |
| public void new(str fieldName, int arrayIndex) |             |

### <a name="method-parmfieldname"></a>メソッド parmFieldName

    public str parmFieldName()

#### <a name="return-value"></a>戻り値

### <a name="method-parmarrayindex"></a>メソッド parmArrayIndex

    public int parmArrayIndex()

#### <a name="return-value"></a>戻り値

### <a name="method-new"></a>メソッド new

    public void new(str fieldName, int arrayIndex)

#### <a name="parameters"></a>パラメーター

fieldName  

<!-- -->

arrayIndex  

## <a name="class-multiselectioncontext"></a>クラス MultiSelectionContext
    class MultiSelectionContext extends Object

### <a name="remarks"></a>備考

### <a name="examples"></a>例

### <a name="methods"></a>メソッド

| 方法                   | 説明                                                    |
|--------------------------|----------------------------------------------------------------|
| public Common getFirst() |                                                                |
| public Common getNext()  |                                                                |
| private void new()       | MultiSelectionContext クラスの新しいインスタンスを初期化します。 |

### <a name="method-getfirst"></a>メソッド getFirst

    public Common getFirst()

#### <a name="return-value"></a>戻り値

### <a name="method-getnext"></a>メソッド getNext

    public Common getNext()

#### <a name="return-value"></a>戻り値

### <a name="method-new"></a>メソッド new

MultiSelectionContext クラスの新しいインスタンスを初期化します。

    private void new()




