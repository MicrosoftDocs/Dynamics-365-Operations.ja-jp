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
# <a name="class-map"></a><span data-ttu-id="a36f8-103">クラス マップ</span><span class="sxs-lookup"><span data-stu-id="a36f8-103">Class Map</span></span>

[!include [banner](../../includes/banner.md)]

```xpp
class Map extends Object
```

<span data-ttu-id="a36f8-104">Map クラスを使うと、ある値 (キー) を別の値に関連付けることができます。</span><span class="sxs-lookup"><span data-stu-id="a36f8-104">The Map class lets to associate one value (the key) with another value.</span></span>

## <a name="remarks"></a><span data-ttu-id="a36f8-105">備考</span><span class="sxs-lookup"><span data-stu-id="a36f8-105">Remarks</span></span>

<span data-ttu-id="a36f8-106">キーと値の両方は、オブジェクトを含む有効な X++ タイプにすることができます。</span><span class="sxs-lookup"><span data-stu-id="a36f8-106">Both the key and the value can be any valid X++ type, including objects.</span></span> <span data-ttu-id="a36f8-107">キーのタイプと値は、マップの宣言で指定されます。</span><span class="sxs-lookup"><span data-stu-id="a36f8-107">The types of the key and the value are specified in the declaration of the map.</span></span> <span data-ttu-id="a36f8-108">マップが実装される方法は、値へのアクセスが非常に高速であることを意味します。</span><span class="sxs-lookup"><span data-stu-id="a36f8-108">The way in which maps are implemented means that access to the values is very fast.</span></span> <span data-ttu-id="a36f8-109">複数のキーは、同じ値にマップできますが、1 つのキーは一度に 1 つの値にだけマップすることができます。</span><span class="sxs-lookup"><span data-stu-id="a36f8-109">Multiple keys can map to the same value, but one key can map to only one value at a time.</span></span> <span data-ttu-id="a36f8-110">既存のキー値を持つ (キー、値) ペアを追加すると、既存のペアがそのキー値に置き換えられます。</span><span class="sxs-lookup"><span data-stu-id="a36f8-110">If you add a (key, value) pair that has an existing key value, it replaces the existing pair with that key value.</span></span> <span data-ttu-id="a36f8-111">マップ内の (キー、値) ペアは、MapEnumerator クラスを使用して移動できます。</span><span class="sxs-lookup"><span data-stu-id="a36f8-111">The (key, value) pairs in a map can be traversed by using the MapEnumerator class.</span></span>

## <a name="examples"></a><span data-ttu-id="a36f8-112">例</span><span class="sxs-lookup"><span data-stu-id="a36f8-112">Examples</span></span>

<span data-ttu-id="a36f8-113">次の例は、マップを逆にする方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="a36f8-113">The following example illustrates how to invert a map.</span></span> <span data-ttu-id="a36f8-114">2 つの異なるキーによってマップされている値がない場合にのみ、マップを反転できます。</span><span class="sxs-lookup"><span data-stu-id="a36f8-114">A map can be inverted only if no value is mapped to by two different keys.</span></span> <span data-ttu-id="a36f8-115">これを確認するために Map.keySet メソッドと Map.valueSet メソッドの要素数が比較されます。</span><span class="sxs-lookup"><span data-stu-id="a36f8-115">The number of elements in the Map.keySet method and the Map.valueSet method is compared to check this.</span></span> <span data-ttu-id="a36f8-116">それ以外の場合、要素が受信マップで移動し、結果マップに挿入されます。</span><span class="sxs-lookup"><span data-stu-id="a36f8-116">Otherwise, the elements are traversed in the incoming map and inserted into the result map.</span></span> <span data-ttu-id="a36f8-117">切り替えを実行する関数、invertMap メソッドは、キーと値の型に関係なく機能します。</span><span class="sxs-lookup"><span data-stu-id="a36f8-117">The function that performs the inversion, the invertMap method, works regardless of the types of the keys and values.</span></span>

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

## <a name="methods"></a><span data-ttu-id="a36f8-118">メソッド</span><span class="sxs-lookup"><span data-stu-id="a36f8-118">Methods</span></span>

| <span data-ttu-id="a36f8-119">方法</span><span class="sxs-lookup"><span data-stu-id="a36f8-119">Method</span></span>                                                      | <span data-ttu-id="a36f8-120">説明</span><span class="sxs-lookup"><span data-stu-id="a36f8-120">Description</span></span>                                                                                     |
|-------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a36f8-121">public str definitionString()</span><span class="sxs-lookup"><span data-stu-id="a36f8-121">public str definitionString()</span></span>                               | <span data-ttu-id="a36f8-122">マップの定義を含む文字列を返します。</span><span class="sxs-lookup"><span data-stu-id="a36f8-122">Returns a string that contains a definition of the map.</span></span>                                         |
| <span data-ttu-id="a36f8-123">public Set domainSet()</span><span class="sxs-lookup"><span data-stu-id="a36f8-123">public Set domainSet()</span></span>                                      | <span data-ttu-id="a36f8-124">マップにキー (ドメイン) 値のセットを作成します。</span><span class="sxs-lookup"><span data-stu-id="a36f8-124">Creates a set of the key (domain) values in a map.</span></span>                                              |
| <span data-ttu-id="a36f8-125">public Types domainType()</span><span class="sxs-lookup"><span data-stu-id="a36f8-125">public Types domainType()</span></span>                                   | <span data-ttu-id="a36f8-126">マップ内のキー (ドメイン) 値のタイプを決定します。</span><span class="sxs-lookup"><span data-stu-id="a36f8-126">Determines the type of the key (domain) values in a map.</span></span>                                        |
| <span data-ttu-id="a36f8-127">public int elements()</span><span class="sxs-lookup"><span data-stu-id="a36f8-127">public int elements()</span></span>                                       | <span data-ttu-id="a36f8-128">マップ内の要素の数を返します。</span><span class="sxs-lookup"><span data-stu-id="a36f8-128">Returns the number of elements in the map.</span></span>                                                      |
| <span data-ttu-id="a36f8-129">public boolean empty()</span><span class="sxs-lookup"><span data-stu-id="a36f8-129">public boolean empty()</span></span>                                      | <span data-ttu-id="a36f8-130">マップに (キー、値) のペアが含まれているかどうかを判定します。</span><span class="sxs-lookup"><span data-stu-id="a36f8-130">Determines whether the map contains any (key, value) pairs.</span></span>                                     |
| <span data-ttu-id="a36f8-131">public boolean exists(AnyType keyValue)</span><span class="sxs-lookup"><span data-stu-id="a36f8-131">public boolean exists(AnyType keyValue)</span></span>                     | <span data-ttu-id="a36f8-132">特定の値がマップ内のキーとして存在するかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="a36f8-132">Determines whether a particular value exists as a key in the map.</span></span>                               |
| <span data-ttu-id="a36f8-133">public MapEnumerator getEnumerator()</span><span class="sxs-lookup"><span data-stu-id="a36f8-133">public MapEnumerator getEnumerator()</span></span>                        | <span data-ttu-id="a36f8-134">マップ内のスキャンを可能にする、マップの列挙子を作成します。</span><span class="sxs-lookup"><span data-stu-id="a36f8-134">Creates an enumerator for the map, which lets you traverse the map.</span></span>                             |
| <span data-ttu-id="a36f8-135">public boolean insert(AnyType keyValue, AnyType valueValue)</span><span class="sxs-lookup"><span data-stu-id="a36f8-135">public boolean insert(AnyType keyValue, AnyType valueValue)</span></span> | <span data-ttu-id="a36f8-136">マップに要素 (keyValue、valueValue ペア) を挿入します。</span><span class="sxs-lookup"><span data-stu-id="a36f8-136">Inserts an element (keyValue, valueValue pair) into the map.</span></span>                                    |
| <span data-ttu-id="a36f8-137">public Set keySet()</span><span class="sxs-lookup"><span data-stu-id="a36f8-137">public Set keySet()</span></span>                                         | <span data-ttu-id="a36f8-138">マップからのキー値を含むセットを返します。</span><span class="sxs-lookup"><span data-stu-id="a36f8-138">Returns a set that contains the key values from a map.</span></span>                                          |
| <span data-ttu-id="a36f8-139">public Types keyType()</span><span class="sxs-lookup"><span data-stu-id="a36f8-139">public Types keyType()</span></span>                                      | <span data-ttu-id="a36f8-140">マップ内のキー値のタイプを返します。</span><span class="sxs-lookup"><span data-stu-id="a36f8-140">Returns the type of the key values in a map.</span></span>                                                    |
| <span data-ttu-id="a36f8-141">public AnyType lookup(AnyType keyValue)</span><span class="sxs-lookup"><span data-stu-id="a36f8-141">public AnyType lookup(AnyType keyValue)</span></span>                     | <span data-ttu-id="a36f8-142">指定されたキー値によりマッピングされている値を返します。</span><span class="sxs-lookup"><span data-stu-id="a36f8-142">Returns the value that is mapped to by a specified key value.</span></span>                                   |
| <span data-ttu-id="a36f8-143">public container pack()</span><span class="sxs-lookup"><span data-stu-id="a36f8-143">public container pack()</span></span>                                     | <span data-ttu-id="a36f8-144">Map クラスの現在のインスタンスをシリアル化します。</span><span class="sxs-lookup"><span data-stu-id="a36f8-144">Serializes the current instance of the Map class.</span></span>                                               |
| <span data-ttu-id="a36f8-145">public Set rangeSet()</span><span class="sxs-lookup"><span data-stu-id="a36f8-145">public Set rangeSet()</span></span>                                       | <span data-ttu-id="a36f8-146">マップ内のキーによってマップされる値 (範囲) を含むセットを返します。</span><span class="sxs-lookup"><span data-stu-id="a36f8-146">Returns a set that contains the values (ranges) that are mapped to by the keys in a map.</span></span>        |
| <span data-ttu-id="a36f8-147">public Types rangeType()</span><span class="sxs-lookup"><span data-stu-id="a36f8-147">public Types rangeType()</span></span>                                    | <span data-ttu-id="a36f8-148">マップ内のキーによってマップされる値 (範囲) のタイプを決定します。</span><span class="sxs-lookup"><span data-stu-id="a36f8-148">Determines the type of the values (ranges) that are mapped to by the keys in a map.</span></span>             |
| <span data-ttu-id="a36f8-149">public boolean remove(AnyType keyValue)</span><span class="sxs-lookup"><span data-stu-id="a36f8-149">public boolean remove(AnyType keyValue)</span></span>                     | <span data-ttu-id="a36f8-150">(キー、値) ペアをマップから削除します。</span><span class="sxs-lookup"><span data-stu-id="a36f8-150">Removes a (key, value) pair from a map.</span></span>                                                         |
| <span data-ttu-id="a36f8-151">public str toString()</span><span class="sxs-lookup"><span data-stu-id="a36f8-151">public str toString()</span></span>                                       | <span data-ttu-id="a36f8-152">マップ内の (キー、値) ペアの説明を返します。</span><span class="sxs-lookup"><span data-stu-id="a36f8-152">Returns a description of the (key, value) pairs in the map.</span></span>                                     |
| <span data-ttu-id="a36f8-153">public Set valueSet()</span><span class="sxs-lookup"><span data-stu-id="a36f8-153">public Set valueSet()</span></span>                                       | <span data-ttu-id="a36f8-154">マップ内のキーによってマップされる値を含むセットを返します。</span><span class="sxs-lookup"><span data-stu-id="a36f8-154">Returns a set that contains the values that are mapped to by the keys in a map.</span></span>                 |
| <span data-ttu-id="a36f8-155">public Types valueType()</span><span class="sxs-lookup"><span data-stu-id="a36f8-155">public Types valueType()</span></span>                                    | <span data-ttu-id="a36f8-156">マップ内のキーによってマップされる値のタイプを返します。</span><span class="sxs-lookup"><span data-stu-id="a36f8-156">Returns the type of the values that are mapped to by the keys in a map.</span></span>                         |
| <span data-ttu-id="a36f8-157">public str xml(\[int indent\])</span><span class="sxs-lookup"><span data-stu-id="a36f8-157">public str xml(\[int indent\])</span></span>                              | <span data-ttu-id="a36f8-158">現在のオブジェクトを表す XML 文字列を返します。</span><span class="sxs-lookup"><span data-stu-id="a36f8-158">Returns an XML string that represents the current object.</span></span>                                       |
| <span data-ttu-id="a36f8-159">::public static Map create(container container)</span><span class="sxs-lookup"><span data-stu-id="a36f8-159">::public static Map create(container container)</span></span>             | <span data-ttu-id="a36f8-160">以前の Map.pack メソッドの呼び出しで取得されたコンテナーからマップを作成します。</span><span class="sxs-lookup"><span data-stu-id="a36f8-160">Creates a map from the container that was obtained from a previous call to the Map.pack method.</span></span> |
| <span data-ttu-id="a36f8-161">::public static Map createFromXML(Object xmlnode)</span><span class="sxs-lookup"><span data-stu-id="a36f8-161">::public static Map createFromXML(Object xmlnode)</span></span>           |                                                                                                 |
| <span data-ttu-id="a36f8-162">::public static boolean equal(Map map1, Map map2)</span><span class="sxs-lookup"><span data-stu-id="a36f8-162">::public static boolean equal(Map map1, Map map2)</span></span>           | <span data-ttu-id="a36f8-163">2 つのマップが等しいかどうかを判断します。</span><span class="sxs-lookup"><span data-stu-id="a36f8-163">Determines whether two maps are equal.</span></span>                                                          |
| <span data-ttu-id="a36f8-164">public void new(Types key, Types value)</span><span class="sxs-lookup"><span data-stu-id="a36f8-164">public void new(Types key, Types value)</span></span>                     | <span data-ttu-id="a36f8-165">新しいマップを作成します</span><span class="sxs-lookup"><span data-stu-id="a36f8-165">Creates a new map.</span></span>                                                                              |

## <a name="method-definitionstring"></a><span data-ttu-id="a36f8-166">メソッド definitionString</span><span class="sxs-lookup"><span data-stu-id="a36f8-166">Method definitionString</span></span>

<span data-ttu-id="a36f8-167">マップの定義を含む文字列を返します。</span><span class="sxs-lookup"><span data-stu-id="a36f8-167">Returns a string that contains a definition of the map.</span></span>

```xpp
public str definitionString()
```

### <a name="return-value---definitionstring"></a><span data-ttu-id="a36f8-168">戻り値 - definitionString</span><span class="sxs-lookup"><span data-stu-id="a36f8-168">Return Value - definitionString</span></span>

<span data-ttu-id="a36f8-169">マップの定義を含む文字列。</span><span class="sxs-lookup"><span data-stu-id="a36f8-169">A string that contains the definition of the map.</span></span>

### <a name="remarks---definitionstring"></a><span data-ttu-id="a36f8-170">備考 - definitionString</span><span class="sxs-lookup"><span data-stu-id="a36f8-170">Remarks - definitionString</span></span>

<span data-ttu-id="a36f8-171">マップの定義。</span><span class="sxs-lookup"><span data-stu-id="a36f8-171">The definition of the map.</span></span>

### <a name="examples---definitionstring"></a><span data-ttu-id="a36f8-172">例 - definitionString</span><span class="sxs-lookup"><span data-stu-id="a36f8-172">Examples - definitionString</span></span>

<span data-ttu-id="a36f8-173">次の例では、マップを作成し、マップの定義を出力します。</span><span class="sxs-lookup"><span data-stu-id="a36f8-173">The following example creates a map and then prints the definition of the map.</span></span>

```xpp
{ 
    Map myMap = new Map(Types::Integer, Types::String); 
    print myMap.definitionString(); 
    pause; 
}
```

## <a name="method-domainset"></a><span data-ttu-id="a36f8-174">メソッド domainSet</span><span class="sxs-lookup"><span data-stu-id="a36f8-174">Method domainSet</span></span>

<span data-ttu-id="a36f8-175">マップにキー (ドメイン) 値のセットを作成します。</span><span class="sxs-lookup"><span data-stu-id="a36f8-175">Creates a set of the key (domain) values in a map.</span></span>

```xpp
public Set domainSet()
```

### <a name="return-value---domainset"></a><span data-ttu-id="a36f8-176">戻り値 - domainSet</span><span class="sxs-lookup"><span data-stu-id="a36f8-176">Return Value - domainSet</span></span>

### <a name="remarks---domainset"></a><span data-ttu-id="a36f8-177">備考 - domainSet</span><span class="sxs-lookup"><span data-stu-id="a36f8-177">Remarks - domainSet</span></span>

<span data-ttu-id="a36f8-178">このメソッドは廃止されました。代わりに Map.keySet を使用してください。</span><span class="sxs-lookup"><span data-stu-id="a36f8-178">This method is obsolete; use the Map.keySet method instead.</span></span>

## <a name="method-domaintype"></a><span data-ttu-id="a36f8-179">メソッド domainType</span><span class="sxs-lookup"><span data-stu-id="a36f8-179">Method domainType</span></span>

<span data-ttu-id="a36f8-180">マップ内のキー (ドメイン) 値のタイプを決定します。</span><span class="sxs-lookup"><span data-stu-id="a36f8-180">Determines the type of the key (domain) values in a map.</span></span>

```xpp
public Types domainType()
```

### <a name="return-value---domaintype"></a><span data-ttu-id="a36f8-181">戻り値 - domainType</span><span class="sxs-lookup"><span data-stu-id="a36f8-181">Return Value - domainType</span></span>

### <a name="remarks---domaintype"></a><span data-ttu-id="a36f8-182">備考 - domainType</span><span class="sxs-lookup"><span data-stu-id="a36f8-182">Remarks - domainType</span></span>

<span data-ttu-id="a36f8-183">このメソッドは廃止されました。代わりに Map.keyType を使用してください。</span><span class="sxs-lookup"><span data-stu-id="a36f8-183">This method is obsolete; use the Map.keyType method instead.</span></span>

## <a name="method-elements"></a><span data-ttu-id="a36f8-184">メソッド elements</span><span class="sxs-lookup"><span data-stu-id="a36f8-184">Method elements</span></span>

<span data-ttu-id="a36f8-185">マップ内の要素の数を返します。</span><span class="sxs-lookup"><span data-stu-id="a36f8-185">Returns the number of elements in the map.</span></span>

```xpp
public int elements()
```

### <a name="return-value---elements"></a><span data-ttu-id="a36f8-186">戻り値 - elements</span><span class="sxs-lookup"><span data-stu-id="a36f8-186">Return Value - elements</span></span>

<span data-ttu-id="a36f8-187">マップ内の要素の数。</span><span class="sxs-lookup"><span data-stu-id="a36f8-187">The number of elements in the map.</span></span>

### <a name="remarks---elements"></a><span data-ttu-id="a36f8-188">備考 - elements</span><span class="sxs-lookup"><span data-stu-id="a36f8-188">Remarks - elements</span></span>

<span data-ttu-id="a36f8-189">マップ内の要素の数はマップ内の異なるキー値の数と同等になります。</span><span class="sxs-lookup"><span data-stu-id="a36f8-189">The number of elements in the map is equal to the number of different key values in the map.</span></span>

### <a name="examples---elements"></a><span data-ttu-id="a36f8-190">例 - elements</span><span class="sxs-lookup"><span data-stu-id="a36f8-190">Examples - elements</span></span>

<span data-ttu-id="a36f8-191">次の例では、elements メソッドを使用して、マップに要素があるかどうかを確認します。</span><span class="sxs-lookup"><span data-stu-id="a36f8-191">The following example uses the elements method to check whether a map has any elements.</span></span> <span data-ttu-id="a36f8-192">\_マップ元が存在し、一部の要素を持っている場合、\_マップ元の値は\_マップ先へ挿入されます。</span><span class="sxs-lookup"><span data-stu-id="a36f8-192">If the \_from map exists and has some elements, the values from the \_from map are inserted into the \_to map.</span></span>

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

## <a name="method-empty"></a><span data-ttu-id="a36f8-193">メソッド empty</span><span class="sxs-lookup"><span data-stu-id="a36f8-193">Method empty</span></span>

<span data-ttu-id="a36f8-194">マップに (キー、値) のペアが含まれているかどうかを判定します。</span><span class="sxs-lookup"><span data-stu-id="a36f8-194">Determines whether the map contains any (key, value) pairs.</span></span>

```xpp
public boolean empty()
```

### <a name="return-value---empty"></a><span data-ttu-id="a36f8-195">戻り値 - empty</span><span class="sxs-lookup"><span data-stu-id="a36f8-195">Return Value - empty</span></span>

<span data-ttu-id="a36f8-196">マップに要素が存在しない場合に true。それ以外の場合は false。</span><span class="sxs-lookup"><span data-stu-id="a36f8-196">true if the map does not contain any elements; otherwise, false.</span></span>

### <a name="remarks---empty"></a><span data-ttu-id="a36f8-197">備考 - empty</span><span class="sxs-lookup"><span data-stu-id="a36f8-197">Remarks - empty</span></span>

<span data-ttu-id="a36f8-198">このメソッドは、(elements() == 0) と等価です。</span><span class="sxs-lookup"><span data-stu-id="a36f8-198">This method is equivalent to (elements() == 0).</span></span>

## <a name="method-exists"></a><span data-ttu-id="a36f8-199">メソッド exists</span><span class="sxs-lookup"><span data-stu-id="a36f8-199">Method exists</span></span>

<span data-ttu-id="a36f8-200">特定の値がマップ内のキーとして存在するかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="a36f8-200">Determines whether a particular value exists as a key in the map.</span></span>

```xpp
public boolean exists(AnyType keyValue)
```

### <a name="parameters---exists"></a><span data-ttu-id="a36f8-201">パラメーター - exists</span><span class="sxs-lookup"><span data-stu-id="a36f8-201">Parameters - exists</span></span>

<span data-ttu-id="a36f8-202">keyValue</span><span class="sxs-lookup"><span data-stu-id="a36f8-202">keyValue</span></span>  
<span data-ttu-id="a36f8-203">確認する値。</span><span class="sxs-lookup"><span data-stu-id="a36f8-203">The value to check for.</span></span>

### <a name="return-value---exists"></a><span data-ttu-id="a36f8-204">戻り値 - exists</span><span class="sxs-lookup"><span data-stu-id="a36f8-204">Return Value - exists</span></span>

<span data-ttu-id="a36f8-205">指定されたキー値がマップ内に存在する場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="a36f8-205">true if the specified key value exists in the map; otherwise, false.</span></span>

### <a name="remarks---exists"></a><span data-ttu-id="a36f8-206">備考 - exists</span><span class="sxs-lookup"><span data-stu-id="a36f8-206">Remarks - exists</span></span>

<span data-ttu-id="a36f8-207">Map.lookup メソッドへの呼び出しを保護するには、このメソッドを使用します。</span><span class="sxs-lookup"><span data-stu-id="a36f8-207">Use this method to guard calls to the Map.lookup method.</span></span> <span data-ttu-id="a36f8-208">Map.lookup メソッドで、検索値が見つからなかった場合、例外が発生されます。</span><span class="sxs-lookup"><span data-stu-id="a36f8-208">If the Map.lookup method does not find the value that it is looking for, it throws an exception.</span></span>

### <a name="examples---exists"></a><span data-ttu-id="a36f8-209">例 - exists</span><span class="sxs-lookup"><span data-stu-id="a36f8-209">Examples - exists</span></span>

<span data-ttu-id="a36f8-210">次の例では、スタイル シート内のスタイルのマップに特定のスタイルが存在するかどうかを確認します。</span><span class="sxs-lookup"><span data-stu-id="a36f8-210">The following example checks whether a particular style exists in a map of styles in a style sheet.</span></span> <span data-ttu-id="a36f8-211">存在する場合は、本文のスタイルの新しい名前に置き換えられます。</span><span class="sxs-lookup"><span data-stu-id="a36f8-211">If it does, a new name is substituted for the body style.</span></span>

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

## <a name="method-getenumerator"></a><span data-ttu-id="a36f8-212">メソッド getEnumerator</span><span class="sxs-lookup"><span data-stu-id="a36f8-212">Method getEnumerator</span></span>

<span data-ttu-id="a36f8-213">マップ内のスキャンを可能にする、マップの列挙子を作成します。</span><span class="sxs-lookup"><span data-stu-id="a36f8-213">Creates an enumerator for the map, which lets you traverse the map.</span></span>

```xpp
public MapEnumerator getEnumerator()
```

### <a name="return-value---getenumerator"></a><span data-ttu-id="a36f8-214">戻り値 - getEnumerator</span><span class="sxs-lookup"><span data-stu-id="a36f8-214">Return Value - getEnumerator</span></span>

<span data-ttu-id="a36f8-215">マップの MapEnumerator オブジェクト。</span><span class="sxs-lookup"><span data-stu-id="a36f8-215">A MapEnumerator object for the map.</span></span>

### <a name="examples---getenumerator"></a><span data-ttu-id="a36f8-216">例 - getEnumerator</span><span class="sxs-lookup"><span data-stu-id="a36f8-216">Examples - getEnumerator</span></span>

<span data-ttu-id="a36f8-217">次の例では \_from マップに要素があるかどうかを確認し、要素がある場合はマップの列挙子を作成します。</span><span class="sxs-lookup"><span data-stu-id="a36f8-217">The following example checks whether the \_from map has any elements and creates an enumerator for the map if it has any elements.</span></span> <span data-ttu-id="a36f8-218">次に、マップが移動し、その中の要素が \_to マップに挿入されます。</span><span class="sxs-lookup"><span data-stu-id="a36f8-218">The map is then traversed, and the elements in it are inserted into the \_to map.</span></span>

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

## <a name="method-insert"></a><span data-ttu-id="a36f8-219">メソッド insert</span><span class="sxs-lookup"><span data-stu-id="a36f8-219">Method insert</span></span>

<span data-ttu-id="a36f8-220">マップに要素 (keyValue、valueValue ペア) を挿入します。</span><span class="sxs-lookup"><span data-stu-id="a36f8-220">Inserts an element (keyValue, valueValue pair) into the map.</span></span>

```xpp
public boolean insert(AnyType keyValue, AnyType valueValue)
```

### <a name="parameters---insert"></a><span data-ttu-id="a36f8-221">パラメーター - insert</span><span class="sxs-lookup"><span data-stu-id="a36f8-221">Parameters - insert</span></span>

<span data-ttu-id="a36f8-222">keyValue</span><span class="sxs-lookup"><span data-stu-id="a36f8-222">keyValue</span></span>  
<span data-ttu-id="a36f8-223">キーによりマッピングされている値。</span><span class="sxs-lookup"><span data-stu-id="a36f8-223">The value that is mapped to by the key.</span></span>

<!-- -->

<span data-ttu-id="a36f8-224">valueValue</span><span class="sxs-lookup"><span data-stu-id="a36f8-224">valueValue</span></span>  
<span data-ttu-id="a36f8-225">キーによりマッピングされている値。</span><span class="sxs-lookup"><span data-stu-id="a36f8-225">The value that is mapped to by the key.</span></span>

### <a name="return-value---insert"></a><span data-ttu-id="a36f8-226">戻り値 - insert</span><span class="sxs-lookup"><span data-stu-id="a36f8-226">Return Value - insert</span></span>

<span data-ttu-id="a36f8-227">キーがマップにまだ存在せず、マップが挿入された場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="a36f8-227">true if the key did not already exist in the map and has been inserted; otherwise, false.</span></span>

### <a name="remarks---insert"></a><span data-ttu-id="a36f8-228">備考 - insert</span><span class="sxs-lookup"><span data-stu-id="a36f8-228">Remarks - insert</span></span>

<span data-ttu-id="a36f8-229">キーが既にマップに存在する場合は、値が更新されます。</span><span class="sxs-lookup"><span data-stu-id="a36f8-229">If the key already exists in the map, the value is updated.</span></span>

### <a name="examples---insert"></a><span data-ttu-id="a36f8-230">例 - insert</span><span class="sxs-lookup"><span data-stu-id="a36f8-230">Examples - insert</span></span>

<span data-ttu-id="a36f8-231">次の例では \_from マップに要素があるかどうかを確認し、要素がある場合はマップの列挙子を作成します。</span><span class="sxs-lookup"><span data-stu-id="a36f8-231">The following example checks whether the \_from map has any elements and creates an enumerator for the map if it has any elements.</span></span> <span data-ttu-id="a36f8-232">マップが移動し、\_from マップから \_to マップに要素を挿入するために insert メソッドが使用されます。</span><span class="sxs-lookup"><span data-stu-id="a36f8-232">The map is traversed, and the insert method is used to insert the elements from the \_from map into the \_to map.</span></span>

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

## <a name="method-keyset"></a><span data-ttu-id="a36f8-233">メソッド keySet</span><span class="sxs-lookup"><span data-stu-id="a36f8-233">Method keySet</span></span>

<span data-ttu-id="a36f8-234">マップからのキー値を含むセットを返します。</span><span class="sxs-lookup"><span data-stu-id="a36f8-234">Returns a set that contains the key values from a map.</span></span>

```xpp
public Set keySet()
```

### <a name="return-value---keyset"></a><span data-ttu-id="a36f8-235">戻り値 - keySet</span><span class="sxs-lookup"><span data-stu-id="a36f8-235">Return Value - keySet</span></span>

<span data-ttu-id="a36f8-236">キー値を含むセット。</span><span class="sxs-lookup"><span data-stu-id="a36f8-236">A set that contains the key values.</span></span>

### <a name="examples---keyset"></a><span data-ttu-id="a36f8-237">例 - keySet</span><span class="sxs-lookup"><span data-stu-id="a36f8-237">Examples - keySet</span></span>

<span data-ttu-id="a36f8-238">次の例では、セット内の要素として検出されないキー値を持つすべての要素をマップから削除します。</span><span class="sxs-lookup"><span data-stu-id="a36f8-238">The following example deletes all elements from a map that have key values that are not found as elements in a set.</span></span>

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

## <a name="method-keytype"></a><span data-ttu-id="a36f8-239">メソッド keyType</span><span class="sxs-lookup"><span data-stu-id="a36f8-239">Method keyType</span></span>

<span data-ttu-id="a36f8-240">マップ内のキー値のタイプを返します。</span><span class="sxs-lookup"><span data-stu-id="a36f8-240">Returns the type of the key values in a map.</span></span>

```xpp
public Types keyType()
```

### <a name="return-value---keytype"></a><span data-ttu-id="a36f8-241">戻り値 - keyType</span><span class="sxs-lookup"><span data-stu-id="a36f8-241">Return Value - keyType</span></span>

<span data-ttu-id="a36f8-242">キー値のタイプ。</span><span class="sxs-lookup"><span data-stu-id="a36f8-242">The type of the key values.</span></span>

### <a name="remarks---keytype"></a><span data-ttu-id="a36f8-243">備考 - keyType</span><span class="sxs-lookup"><span data-stu-id="a36f8-243">Remarks - keyType</span></span>

<span data-ttu-id="a36f8-244">可能な戻り値は、Types システム列挙で説明されます。</span><span class="sxs-lookup"><span data-stu-id="a36f8-244">The possible return values are outlined by the Types system enum.</span></span> <span data-ttu-id="a36f8-245">キー値のタイプは、マップの作成時に決定されます。</span><span class="sxs-lookup"><span data-stu-id="a36f8-245">The type of the key values is determined when the map is constructed.</span></span> <span data-ttu-id="a36f8-246">これは Map.new メソッドに対する最初のパラメーターとして指定されます。</span><span class="sxs-lookup"><span data-stu-id="a36f8-246">It is supplied as the first parameter to the Map.new method.</span></span>

## <a name="method-lookup"></a><span data-ttu-id="a36f8-247">メソッド lookup</span><span class="sxs-lookup"><span data-stu-id="a36f8-247">Method lookup</span></span>

<span data-ttu-id="a36f8-248">指定されたキー値によりマッピングされている値を返します。</span><span class="sxs-lookup"><span data-stu-id="a36f8-248">Returns the value that is mapped to by a specified key value.</span></span>

```xpp
public AnyType lookup(AnyType keyValue)
```

### <a name="parameters---lookup"></a><span data-ttu-id="a36f8-249">パラメーター - lookup</span><span class="sxs-lookup"><span data-stu-id="a36f8-249">Parameters - lookup</span></span>

<span data-ttu-id="a36f8-250">keyValue</span><span class="sxs-lookup"><span data-stu-id="a36f8-250">keyValue</span></span>  
<span data-ttu-id="a36f8-251">検索するキー。</span><span class="sxs-lookup"><span data-stu-id="a36f8-251">The key to find.</span></span>

### <a name="return-value---lookup"></a><span data-ttu-id="a36f8-252">戻り値 - lookup</span><span class="sxs-lookup"><span data-stu-id="a36f8-252">Return Value - lookup</span></span>

<span data-ttu-id="a36f8-253">キーにより指定されている値。</span><span class="sxs-lookup"><span data-stu-id="a36f8-253">The value that is mapped to by the specified key.</span></span>

### <a name="remarks---lookup"></a><span data-ttu-id="a36f8-254">戻り値 - lookup</span><span class="sxs-lookup"><span data-stu-id="a36f8-254">Remarks - lookup</span></span>

<span data-ttu-id="a36f8-255">マップ内にキーが見つからない場合、Map.exists メソッドを使用して取得する値が存在するかどうかを確認し例外がスローされます。</span><span class="sxs-lookup"><span data-stu-id="a36f8-255">An exception is thrown if the key is not found in the map, so check whether the value that you want to retrieve exists by using the Map.exists method.</span></span>

### <a name="examples---lookup"></a><span data-ttu-id="a36f8-256">例 - lookup</span><span class="sxs-lookup"><span data-stu-id="a36f8-256">Examples - lookup</span></span>

<span data-ttu-id="a36f8-257">次の例では、スタイル シート内のスタイルのマップに特定のスタイルが存在するかどうかを確認します。</span><span class="sxs-lookup"><span data-stu-id="a36f8-257">The following example checks whether a particular style exists in a map of styles in a style sheet.</span></span> <span data-ttu-id="a36f8-258">存在する場合は、本文のスタイルの新しい名前に置き換えられます。</span><span class="sxs-lookup"><span data-stu-id="a36f8-258">If it does, a new name is substituted for the body style.</span></span>

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

## <a name="method-pack"></a><span data-ttu-id="a36f8-259">メソッド pack</span><span class="sxs-lookup"><span data-stu-id="a36f8-259">Method pack</span></span>

<span data-ttu-id="a36f8-260">Map クラスの現在のインスタンスをシリアル化します。</span><span class="sxs-lookup"><span data-stu-id="a36f8-260">Serializes the current instance of the Map class.</span></span>

```xpp
public container pack()
```

### <a name="return-value---pack"></a><span data-ttu-id="a36f8-261">戻り値 - pack</span><span class="sxs-lookup"><span data-stu-id="a36f8-261">Return Value - pack</span></span>

<span data-ttu-id="a36f8-262">Map クラスの現在のインスタンスを含むコンテナーです。</span><span class="sxs-lookup"><span data-stu-id="a36f8-262">A container that contains the current instance of the Map class.</span></span>

### <a name="remarks---pack"></a><span data-ttu-id="a36f8-263">備考 - pack</span><span class="sxs-lookup"><span data-stu-id="a36f8-263">Remarks - pack</span></span>

<span data-ttu-id="a36f8-264">このメソッドで作成されたコンテナーには、マップの最初の要素の前に 4 つの要素が含まれます。</span><span class="sxs-lookup"><span data-stu-id="a36f8-264">The container created by this method contains 4 elements before the first element from the map:</span></span>

-   <span data-ttu-id="a36f8-265">コンテナのバージョン番号</span><span class="sxs-lookup"><span data-stu-id="a36f8-265">A version number for the container</span></span>
-   <span data-ttu-id="a36f8-266">マップ内のキーのデータ型を識別する整数</span><span class="sxs-lookup"><span data-stu-id="a36f8-266">An integer that identifies the data type of the keys in the map</span></span>
-   <span data-ttu-id="a36f8-267">マップ内の値のデータ型を識別する整数</span><span class="sxs-lookup"><span data-stu-id="a36f8-267">An integer that identifies the data type of the values in the map</span></span>
-   <span data-ttu-id="a36f8-268">マップ内の要素の数。</span><span class="sxs-lookup"><span data-stu-id="a36f8-268">The number of elements in the map</span></span>

<span data-ttu-id="a36f8-269">キーまたは値がオブジェクトになっている場合は、梱包は、各オブジェクトに対して pack メソッドを連続して呼び出し、サブコンテナーを取得することによって行われます。</span><span class="sxs-lookup"><span data-stu-id="a36f8-269">If the keys or the values are objects, packing is performed by calling the pack method successively on each object to yield a subcontainer.</span></span> <span data-ttu-id="a36f8-270">pack メソッドと unpack メソッドは、X++ anytype 値を保持できません。</span><span class="sxs-lookup"><span data-stu-id="a36f8-270">The pack and unpack methods cannot preserve X++ anytype values.</span></span> <span data-ttu-id="a36f8-271">1 つのオプションは、anytype 値をオブジェクトまたは構造体に格納し、構造体をマップ オブジェクトの値にすることです。</span><span class="sxs-lookup"><span data-stu-id="a36f8-271">One option is to put the anytype values into objects or structs, and have the structs be the values in the Map object.</span></span> <span data-ttu-id="a36f8-272">Microsoft .NET System.Collections クラスは別のオプションで使用します。</span><span class="sxs-lookup"><span data-stu-id="a36f8-272">Use of Microsoft .NET System.Collections classes is another option.</span></span> <span data-ttu-id="a36f8-273">Map.create メソッドを使用して、パックされたコンテナーからマップを取得できます。</span><span class="sxs-lookup"><span data-stu-id="a36f8-273">The map can be retrieved from the packed container by using the Map.create method.</span></span>

### <a name="examples---pack"></a><span data-ttu-id="a36f8-274">例 - pack</span><span class="sxs-lookup"><span data-stu-id="a36f8-274">Examples - pack</span></span>

<span data-ttu-id="a36f8-275">次の例では、メソッド (conprojItemTransSalesAmount) に渡されたコンテナーからマップを作成し、いくつかの値を追加して MapEnumerator.pack を使用してマップをコンテナーにパックします。</span><span class="sxs-lookup"><span data-stu-id="a36f8-275">The following example creates a map from a container that is passed into the method (conprojItemTransSalesAmount), adds some values to it, and then uses MapEnumerator.pack to pack the map into a container.</span></span> <span data-ttu-id="a36f8-276">このメソッドによって新しいコンテナーが返されます。</span><span class="sxs-lookup"><span data-stu-id="a36f8-276">The new container is then returned by the method.</span></span>

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

## <a name="method-rangeset"></a><span data-ttu-id="a36f8-277">メソッド rangeSet</span><span class="sxs-lookup"><span data-stu-id="a36f8-277">Method rangeSet</span></span>

<span data-ttu-id="a36f8-278">マップ内のキーによってマップされる値 (範囲) を含むセットを返します。</span><span class="sxs-lookup"><span data-stu-id="a36f8-278">Returns a set that contains the values (ranges) that are mapped to by the keys in a map.</span></span>

```xpp
public Set rangeSet()
```

### <a name="return-value---rangeset"></a><span data-ttu-id="a36f8-279">戻り値 - rangeSet</span><span class="sxs-lookup"><span data-stu-id="a36f8-279">Return Value - rangeSet</span></span>

### <a name="remarks---rangeset"></a><span data-ttu-id="a36f8-280">戻り値 - rangeSet</span><span class="sxs-lookup"><span data-stu-id="a36f8-280">Remarks - rangeSet</span></span>

<span data-ttu-id="a36f8-281">このメソッドは廃止されました。代わりに Map.valueSet を使用してください。</span><span class="sxs-lookup"><span data-stu-id="a36f8-281">This method is obsolete; use the Map.valueSet method instead.</span></span>

## <a name="method-rangetype"></a><span data-ttu-id="a36f8-282">メソッド rangeType</span><span class="sxs-lookup"><span data-stu-id="a36f8-282">Method rangeType</span></span>

<span data-ttu-id="a36f8-283">マップ内のキーによってマップされる値 (範囲) のタイプを決定します。</span><span class="sxs-lookup"><span data-stu-id="a36f8-283">Determines the type of the values (ranges) that are mapped to by the keys in a map.</span></span>

```xpp
public Types rangeType()
```

### <a name="return-value---rangetype"></a><span data-ttu-id="a36f8-284">戻り値 - rangeType</span><span class="sxs-lookup"><span data-stu-id="a36f8-284">Return Value - rangeType</span></span>

### <a name="remarks---rangetype"></a><span data-ttu-id="a36f8-285">備考 - rangeType</span><span class="sxs-lookup"><span data-stu-id="a36f8-285">Remarks - rangeType</span></span>

<span data-ttu-id="a36f8-286">このメソッドは廃止されました。代わりに valueType を使用してください。</span><span class="sxs-lookup"><span data-stu-id="a36f8-286">This method is obsolete; use the valueType method instead.</span></span>

## <a name="method-remove"></a><span data-ttu-id="a36f8-287">メソッド remove</span><span class="sxs-lookup"><span data-stu-id="a36f8-287">Method remove</span></span>

<span data-ttu-id="a36f8-288">(キー、値) ペアをマップから削除します。</span><span class="sxs-lookup"><span data-stu-id="a36f8-288">Removes a (key, value) pair from a map.</span></span>

```xpp
public boolean remove(AnyType keyValue)
```

### <a name="parameters---remove"></a><span data-ttu-id="a36f8-289">パラメーター - remove</span><span class="sxs-lookup"><span data-stu-id="a36f8-289">Parameters - remove</span></span>

<span data-ttu-id="a36f8-290">keyValue</span><span class="sxs-lookup"><span data-stu-id="a36f8-290">keyValue</span></span>  
<span data-ttu-id="a36f8-291">削除するキーの値。</span><span class="sxs-lookup"><span data-stu-id="a36f8-291">The value of the key to delete.</span></span>

### <a name="return-value---remove"></a><span data-ttu-id="a36f8-292">戻り値 - remove</span><span class="sxs-lookup"><span data-stu-id="a36f8-292">Return Value - remove</span></span>

<span data-ttu-id="a36f8-293">キーがマップ内に見つかり、要素が削除された場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="a36f8-293">true if the key was found in the map and the element has been deleted; otherwise, false.</span></span>

### <a name="examples---remove"></a><span data-ttu-id="a36f8-294">例 - remove</span><span class="sxs-lookup"><span data-stu-id="a36f8-294">Examples - remove</span></span>

<span data-ttu-id="a36f8-295">次の例では、特定のキー値がマップに存在するかどうかを確認します。</span><span class="sxs-lookup"><span data-stu-id="a36f8-295">The following example checks whether a particular key value exists in a map.</span></span> <span data-ttu-id="a36f8-296">値が存在する場合は、メソッドがキーと対応する値を削除します。</span><span class="sxs-lookup"><span data-stu-id="a36f8-296">If the value exists, the method deletes the key and its corresponding value.</span></span> <span data-ttu-id="a36f8-297">このメソッドは、値が見つかった場合は true を返し、キーがマップに存在しない場合は false を返します。</span><span class="sxs-lookup"><span data-stu-id="a36f8-297">The method returns true if the value was found and false if the key did not exist in the map.</span></span>

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

## <a name="method-tostring"></a><span data-ttu-id="a36f8-298">メソッド toString</span><span class="sxs-lookup"><span data-stu-id="a36f8-298">Method toString</span></span>

<span data-ttu-id="a36f8-299">マップ内の (キー、値) ペアの説明を返します。</span><span class="sxs-lookup"><span data-stu-id="a36f8-299">Returns a description of the (key, value) pairs in the map.</span></span>

```xpp
public str toString()
```

### <a name="return-value---tostring"></a><span data-ttu-id="a36f8-300">戻り値 - toString</span><span class="sxs-lookup"><span data-stu-id="a36f8-300">Return Value - toString</span></span>

<span data-ttu-id="a36f8-301">マップの要素の説明を含む文字列。</span><span class="sxs-lookup"><span data-stu-id="a36f8-301">A string that contains a description of the elements in the map.</span></span>

### <a name="examples---tostring"></a><span data-ttu-id="a36f8-302">例 - toString</span><span class="sxs-lookup"><span data-stu-id="a36f8-302">Examples - toString</span></span>

<span data-ttu-id="a36f8-303">次の例では、マップを作成し、いくつかの要素を追加してから、これらの要素の説明を出力します。</span><span class="sxs-lookup"><span data-stu-id="a36f8-303">The following example creates a map, adds some elements to it, and then prints a description of these elements.</span></span>

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

## <a name="method-valueset"></a><span data-ttu-id="a36f8-304">メソッド valueSet</span><span class="sxs-lookup"><span data-stu-id="a36f8-304">Method valueSet</span></span>

<span data-ttu-id="a36f8-305">マップ内のキーによってマップされる値を含むセットを返します。</span><span class="sxs-lookup"><span data-stu-id="a36f8-305">Returns a set that contains the values that are mapped to by the keys in a map.</span></span>

```xpp
public Set valueSet()
```

### <a name="return-value---valueset"></a><span data-ttu-id="a36f8-306">戻り値 - valueSet</span><span class="sxs-lookup"><span data-stu-id="a36f8-306">Return Value - valueSet</span></span>

<span data-ttu-id="a36f8-307">マップからの値を含むセット。</span><span class="sxs-lookup"><span data-stu-id="a36f8-307">A set that contains the values from the map.</span></span>

### <a name="remarks---valueset"></a><span data-ttu-id="a36f8-308">備考 - valueSet</span><span class="sxs-lookup"><span data-stu-id="a36f8-308">Remarks - valueSet</span></span>

<span data-ttu-id="a36f8-309">すべてのキーが、別の値にマップされる場合、セット内の要素の数はマップ内の要素の数と同等になります。</span><span class="sxs-lookup"><span data-stu-id="a36f8-309">If all the keys map to different values, the number of elements in the set is equal to the number of elements in the map.</span></span>

## <a name="method-valuetype"></a><span data-ttu-id="a36f8-310">メソッド valueType</span><span class="sxs-lookup"><span data-stu-id="a36f8-310">Method valueType</span></span>

<span data-ttu-id="a36f8-311">マップ内のキーによってマップされる値のタイプを返します。</span><span class="sxs-lookup"><span data-stu-id="a36f8-311">Returns the type of the values that are mapped to by the keys in a map.</span></span>

```xpp
public Types valueType()
```

### <a name="return-value---valuetype"></a><span data-ttu-id="a36f8-312">戻り値 - valueType</span><span class="sxs-lookup"><span data-stu-id="a36f8-312">Return Value - valueType</span></span>

<span data-ttu-id="a36f8-313">キーによってマップされる値のタイプ。</span><span class="sxs-lookup"><span data-stu-id="a36f8-313">The type of the values that are mapped to by the keys.</span></span>

### <a name="remarks---valuetype"></a><span data-ttu-id="a36f8-314">備考 - valueType</span><span class="sxs-lookup"><span data-stu-id="a36f8-314">Remarks - valueType</span></span>

<span data-ttu-id="a36f8-315">キー値のタイプは、マップの作成時に決定されます。</span><span class="sxs-lookup"><span data-stu-id="a36f8-315">The type of the key values is determined when the map is constructed.</span></span> <span data-ttu-id="a36f8-316">これは Map.new メソッドに対する最初のパラメーターとして指定されます。</span><span class="sxs-lookup"><span data-stu-id="a36f8-316">It is supplied as the first parameter to the Map.new method.</span></span>

## <a name="method-xml"></a><span data-ttu-id="a36f8-317">メソッド xml</span><span class="sxs-lookup"><span data-stu-id="a36f8-317">Method xml</span></span>

<span data-ttu-id="a36f8-318">現在のオブジェクトを表す XML 文字列を返します。</span><span class="sxs-lookup"><span data-stu-id="a36f8-318">Returns an XML string that represents the current object.</span></span>

```xpp
public str xml([int indent])
```

### <a name="parameters---xml"></a><span data-ttu-id="a36f8-319">パラメーター - xml</span><span class="sxs-lookup"><span data-stu-id="a36f8-319">Parameters - xml</span></span>

<span data-ttu-id="a36f8-320">インデント</span><span class="sxs-lookup"><span data-stu-id="a36f8-320">indent</span></span>  
<span data-ttu-id="a36f8-321">返される XML 文字列のインデントの量 (省略可能)。</span><span class="sxs-lookup"><span data-stu-id="a36f8-321">The amount of indentation of the XML string that is returned; optional.</span></span>

### <a name="return-value---xml"></a><span data-ttu-id="a36f8-322">戻り値 - xml</span><span class="sxs-lookup"><span data-stu-id="a36f8-322">Return Value - xml</span></span>

<span data-ttu-id="a36f8-323">現在のオブジェクトを表す XML 文字列です。</span><span class="sxs-lookup"><span data-stu-id="a36f8-323">An XML string that represents the current object.</span></span>

### <a name="remarks---xml"></a><span data-ttu-id="a36f8-324">備考 - xml</span><span class="sxs-lookup"><span data-stu-id="a36f8-324">Remarks - xml</span></span>

<span data-ttu-id="a36f8-325">このメソッドをオーバーライドして、その型に対して意味のある値を返すことができます。</span><span class="sxs-lookup"><span data-stu-id="a36f8-325">This method can be overridden to return values that are meaningful for that type.</span></span>

## <a name="method-create"></a><span data-ttu-id="a36f8-326">メソッド create</span><span class="sxs-lookup"><span data-stu-id="a36f8-326">Method create</span></span>

<span data-ttu-id="a36f8-327">以前の Map.pack メソッドの呼び出しで取得されたコンテナーからマップを作成します。</span><span class="sxs-lookup"><span data-stu-id="a36f8-327">Creates a map from the container that was obtained from a previous call to the Map.pack method.</span></span>

```xpp
public static Map create(container container)
```

### <a name="parameters---create"></a><span data-ttu-id="a36f8-328">パラメーター - create</span><span class="sxs-lookup"><span data-stu-id="a36f8-328">Parameters - create</span></span>

<span data-ttu-id="a36f8-329">コンテナー</span><span class="sxs-lookup"><span data-stu-id="a36f8-329">container</span></span>  

### <a name="return-value---create"></a><span data-ttu-id="a36f8-330">戻り値 - create</span><span class="sxs-lookup"><span data-stu-id="a36f8-330">Return Value - create</span></span>

<span data-ttu-id="a36f8-331">Map.pack メソッドでコンテナーに梱包されたマップと同等のマップ。</span><span class="sxs-lookup"><span data-stu-id="a36f8-331">A map that is equal to the map that was packed into the container by the Map.pack method.</span></span>

### <a name="remarks---create"></a><span data-ttu-id="a36f8-332">備考 - create</span><span class="sxs-lookup"><span data-stu-id="a36f8-332">Remarks - create</span></span>

<span data-ttu-id="a36f8-333">キーまたは値がオブジェクトの場合、オブジェクトにはコンテナーからその内部状態を再設定するために呼び出されるアンパック メソッドが必要です。</span><span class="sxs-lookup"><span data-stu-id="a36f8-333">If the keys or values are objects, the objects must have an unpack method that is called to re-establish their internal state from the container.</span></span>

### <a name="examples---create"></a><span data-ttu-id="a36f8-334">例 - create</span><span class="sxs-lookup"><span data-stu-id="a36f8-334">Examples - create</span></span>

<span data-ttu-id="a36f8-335">次の例では、メソッド (conprojItemTransSalesAmount) に渡されたコンテナーからマップを作成し、コンテナーに値を追加してマップをパックし、新しいコンテナーとして返します。</span><span class="sxs-lookup"><span data-stu-id="a36f8-335">The following example creates a map from a container that is passed into the method (conprojItemTransSalesAmount), adds some values to the container, and then packs the map and returns it as a new container.</span></span>

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

## <a name="method-createfromxml"></a><span data-ttu-id="a36f8-336">メソッド createFromXML</span><span class="sxs-lookup"><span data-stu-id="a36f8-336">Method createFromXML</span></span>

```xpp
public static Map createFromXML(Object xmlnode)
```

### <a name="parameters---createfromxml"></a><span data-ttu-id="a36f8-337">パラメータ - createFromXML</span><span class="sxs-lookup"><span data-stu-id="a36f8-337">Parameters - createFromXML</span></span>

<span data-ttu-id="a36f8-338">xmlnode</span><span class="sxs-lookup"><span data-stu-id="a36f8-338">xmlnode</span></span>  

### <a name="return-value---createfromxml"></a><span data-ttu-id="a36f8-339">戻り値 - createFromXML</span><span class="sxs-lookup"><span data-stu-id="a36f8-339">Return Value - createFromXML</span></span>

## <a name="method-equal"></a><span data-ttu-id="a36f8-340">メソッド equal</span><span class="sxs-lookup"><span data-stu-id="a36f8-340">Method equal</span></span>

<span data-ttu-id="a36f8-341">2 つのマップが等しいかどうかを判断します。</span><span class="sxs-lookup"><span data-stu-id="a36f8-341">Determines whether two maps are equal.</span></span>

```xpp
public static boolean equal(Map map1, Map map2)
```

### <a name="parameters---equal"></a><span data-ttu-id="a36f8-342">パラメーター - equal</span><span class="sxs-lookup"><span data-stu-id="a36f8-342">Parameters - equal</span></span>

<span data-ttu-id="a36f8-343">map1</span><span class="sxs-lookup"><span data-stu-id="a36f8-343">map1</span></span>  
<span data-ttu-id="a36f8-344">比較する 2 つ目のマップ。</span><span class="sxs-lookup"><span data-stu-id="a36f8-344">The second map to compare.</span></span>

<!-- -->

<span data-ttu-id="a36f8-345">map2</span><span class="sxs-lookup"><span data-stu-id="a36f8-345">map2</span></span>  
<span data-ttu-id="a36f8-346">比較する 2 つ目のマップ。</span><span class="sxs-lookup"><span data-stu-id="a36f8-346">The second map to compare.</span></span>

### <a name="return-value---equal"></a><span data-ttu-id="a36f8-347">戻り値 - equal</span><span class="sxs-lookup"><span data-stu-id="a36f8-347">Return Value - equal</span></span>

<span data-ttu-id="a36f8-348">2 つのマップが等しい場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="a36f8-348">true if the two maps are equal; otherwise, false.</span></span>

### <a name="remarks---equal"></a><span data-ttu-id="a36f8-349">備考 - equal</span><span class="sxs-lookup"><span data-stu-id="a36f8-349">Remarks - equal</span></span>

<span data-ttu-id="a36f8-350">2 つのマップが同じ数の要素を含み、キー セットが同じで、キー セットの各キーが両方のマップの同じ値にマップされている場合、2 つのマップは同等です。</span><span class="sxs-lookup"><span data-stu-id="a36f8-350">Two maps are equal if they contain the same number of elements, their key sets are the same, and each key in the key set maps to the same value in both maps.</span></span>

## <a name="method-new"></a><span data-ttu-id="a36f8-351">メソッド new</span><span class="sxs-lookup"><span data-stu-id="a36f8-351">Method new</span></span>

<span data-ttu-id="a36f8-352">新しいマップを作成します</span><span class="sxs-lookup"><span data-stu-id="a36f8-352">Creates a new map.</span></span>

```xpp
public void new(Types key, Types value)
```

### <a name="parameters---new"></a><span data-ttu-id="a36f8-353">パラメーター - new</span><span class="sxs-lookup"><span data-stu-id="a36f8-353">Parameters - new</span></span>

<span data-ttu-id="a36f8-354">キー</span><span class="sxs-lookup"><span data-stu-id="a36f8-354">key</span></span>  
<span data-ttu-id="a36f8-355">値のタイプ。</span><span class="sxs-lookup"><span data-stu-id="a36f8-355">The type of the values.</span></span>

<!-- -->

<span data-ttu-id="a36f8-356">値</span><span class="sxs-lookup"><span data-stu-id="a36f8-356">value</span></span>  
<span data-ttu-id="a36f8-357">値のタイプ。</span><span class="sxs-lookup"><span data-stu-id="a36f8-357">The type of the values.</span></span>

### <a name="examples---new"></a><span data-ttu-id="a36f8-358">例 - new</span><span class="sxs-lookup"><span data-stu-id="a36f8-358">Examples - new</span></span>

<span data-ttu-id="a36f8-359">次の例では、文字列キーを整数値にマッピングするマップを作成します。</span><span class="sxs-lookup"><span data-stu-id="a36f8-359">The following example creates a map that maps string keys to integer values.</span></span>

```xpp
Map myMap = new Map(Types::String, Types::Integer);
```

