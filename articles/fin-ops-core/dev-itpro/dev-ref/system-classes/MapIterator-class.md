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
# <a name="class-mapiterator"></a><span data-ttu-id="e455f-103">クラス MapIterator</span><span class="sxs-lookup"><span data-stu-id="e455f-103">Class MapIterator</span></span>

[!include [banner](../../includes/banner.md)]

```xpp
class MapIterator extends Object
```

<span data-ttu-id="e455f-104">MapIterator クラスは、マップ内の要素を反復処理するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="e455f-104">The MapIterator class is used to iterate over the elements in a map.</span></span>

## <a name="remarks"></a><span data-ttu-id="e455f-105">備考</span><span class="sxs-lookup"><span data-stu-id="e455f-105">Remarks</span></span>

<span data-ttu-id="e455f-106">マップ反復子は、マップ内で要素を反復処理するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="e455f-106">Map iterators are used to iterate over the elements in a map.</span></span> <span data-ttu-id="e455f-107">これらは、反復処理する対象となるマップにシンプルなポインターとして表示することができます。</span><span class="sxs-lookup"><span data-stu-id="e455f-107">They can be viewed as simple pointers into the maps over which they iterate.</span></span> <span data-ttu-id="e455f-108">繰り返しを開始する機能は利用可能であり、より多くの (キー、値) の組み合わせが利用可能であるかどうかを決定し、繰り返しによりポイントされる要素をフェッチします。</span><span class="sxs-lookup"><span data-stu-id="e455f-108">Functionality is available to start the iteration, determine whether more (key, value) pairs are available, and fetch the element that is pointed to by the iterator.</span></span> <span data-ttu-id="e455f-109">MapIterator クラスよりも MapEnumerator クラスを使用することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="e455f-109">It is better to use the MapEnumerator class than the MapIterator class.</span></span> <span data-ttu-id="e455f-110">マップ反復子および反復処理するマップは、同じクライアント/サーバー側にある必要があります。</span><span class="sxs-lookup"><span data-stu-id="e455f-110">Map iterators and the maps over which they iterate must be on the same client/server side.</span></span> <span data-ttu-id="e455f-111">MapIterator クラスを使用し、コードが Called from としてマークされている場合、マップと反復子が別の層で終了する可能性があり、コードは失敗します。</span><span class="sxs-lookup"><span data-stu-id="e455f-111">If you use the MapIterator class and code is marked as Called from, the map and the iterator could end up on different tiers, and the code will fail.</span></span> <span data-ttu-id="e455f-112">MapEnumerator クラスを使用する場合、列挙子はマップと同じ層に自動的に作成されます。</span><span class="sxs-lookup"><span data-stu-id="e455f-112">If you use the MapEnumerator class, the enumerator is automatically created on the same tier as the map.</span></span> <span data-ttu-id="e455f-113">また、MapIterator クラスを使用する場合、より多くおよび次のメソッドを明示的に呼び出して、マップに次の項目を移動する必要があります。</span><span class="sxs-lookup"><span data-stu-id="e455f-113">Additionally, if you use the MapIterator class, you must explicitly call the more and next methods to move to the next item in a map.</span></span> <span data-ttu-id="e455f-114">MapEnumerator クラスを使用する場合、moveNext メソッドを呼び出すだけです。</span><span class="sxs-lookup"><span data-stu-id="e455f-114">If you use the MapEnumerator class, you only have to call the moveNext method.</span></span> <span data-ttu-id="e455f-115">要素が挿入されるシーケンスは、挿入の順序を決定しません。</span><span class="sxs-lookup"><span data-stu-id="e455f-115">The sequence in which the elements are inserted does not determine the order in which they occur.</span></span> <span data-ttu-id="e455f-116">順序は、要素の順序によって定義されます。</span><span class="sxs-lookup"><span data-stu-id="e455f-116">The order is defined by the ordering of the elements.</span></span> <span data-ttu-id="e455f-117">上位キーを持つ要素の前に、下位キーを持つ要素が表示されます。</span><span class="sxs-lookup"><span data-stu-id="e455f-117">Elements that have lower keys appear before elements that have higher keys.</span></span> <span data-ttu-id="e455f-118">型の通常の順序が使用されます。</span><span class="sxs-lookup"><span data-stu-id="e455f-118">The usual ordering for the types is used.</span></span> <span data-ttu-id="e455f-119">ただし、キーがオブジェクトである場合、オブジェクトのアドレスを使用して順序が指定されるため、特定の順序を推測することはできません。</span><span class="sxs-lookup"><span data-stu-id="e455f-119">However, if the keys are objects, the addresses of the objects are used to supply the ordering, and therefore no specific ordering can be inferred.</span></span> <span data-ttu-id="e455f-120">オブジェクトのアドレスは、本来、一時的です。</span><span class="sxs-lookup"><span data-stu-id="e455f-120">The addresses of the objects are transient by nature.</span></span>

## <a name="examples"></a><span data-ttu-id="e455f-121">例</span><span class="sxs-lookup"><span data-stu-id="e455f-121">Examples</span></span>

<span data-ttu-id="e455f-122">次の例では、マップを作成し、3 つの (キー、値) のペアを追加します。</span><span class="sxs-lookup"><span data-stu-id="e455f-122">The following example creates a map and adds three (key, value) pairs.</span></span> <span data-ttu-id="e455f-123">マップを通じて反復処理し、各マップ要素に関する情報を印刷します。</span><span class="sxs-lookup"><span data-stu-id="e455f-123">It then iterates through the map and prints information about each map element.</span></span>

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

## <a name="methods"></a><span data-ttu-id="e455f-124">メソッド</span><span class="sxs-lookup"><span data-stu-id="e455f-124">Methods</span></span>

| <span data-ttu-id="e455f-125">方法</span><span class="sxs-lookup"><span data-stu-id="e455f-125">Method</span></span>                             | <span data-ttu-id="e455f-126">説明</span><span class="sxs-lookup"><span data-stu-id="e455f-126">Description</span></span>                                                                                    |
|------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e455f-127">public str definitionString()</span><span class="sxs-lookup"><span data-stu-id="e455f-127">public str definitionString()</span></span>      | <span data-ttu-id="e455f-128">"\[int -&gt; str\] 反復子" など、反復子の型のテキスト表現を取得します。</span><span class="sxs-lookup"><span data-stu-id="e455f-128">Retrieves a textual representation of the iterator type, such as "\[int -&gt; str\] iterator".</span></span> |
| <span data-ttu-id="e455f-129">public AnyType domainValue()</span><span class="sxs-lookup"><span data-stu-id="e455f-129">public AnyType domainValue()</span></span>       | <span data-ttu-id="e455f-130">反復子により参照される (キー、値) ペアにおけるキーの値を返します。</span><span class="sxs-lookup"><span data-stu-id="e455f-130">Returns the value of the key in the (key, value) pair that is referred to by the iterator.</span></span>     |
| <span data-ttu-id="e455f-131">public boolean find(AnyType value)</span><span class="sxs-lookup"><span data-stu-id="e455f-131">public boolean find(AnyType value)</span></span> | <span data-ttu-id="e455f-132">指定したキー値を検索します。</span><span class="sxs-lookup"><span data-stu-id="e455f-132">Searches for the specified key value.</span></span>                                                          |
| <span data-ttu-id="e455f-133">public AnyType key()</span><span class="sxs-lookup"><span data-stu-id="e455f-133">public AnyType key()</span></span>               | <span data-ttu-id="e455f-134">反復子により参照される (キー、値) ペアからキーを返します。</span><span class="sxs-lookup"><span data-stu-id="e455f-134">Returns the key from the (key, value) pair that is referred to by the iterator.</span></span>                |
| <span data-ttu-id="e455f-135">public boolean more()</span><span class="sxs-lookup"><span data-stu-id="e455f-135">public boolean more()</span></span>              | <span data-ttu-id="e455f-136">反復子が有効な (キー、値 ) ペアを検出するかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="e455f-136">Determines whether the iterator finds a valid (key, value) pair.</span></span>                               |
| <span data-ttu-id="e455f-137">public AnyType rangeValue()</span><span class="sxs-lookup"><span data-stu-id="e455f-137">public AnyType rangeValue()</span></span>        | <span data-ttu-id="e455f-138">反復子により参照される (キー、値) ペアにおける値の値を返します。</span><span class="sxs-lookup"><span data-stu-id="e455f-138">Returns the value of the value in the (key, value) pair that is referred to by the iterator.</span></span>   |
| <span data-ttu-id="e455f-139">public str toString()</span><span class="sxs-lookup"><span data-stu-id="e455f-139">public str toString()</span></span>              | <span data-ttu-id="e455f-140">反復子のテキスト表現を取得します。</span><span class="sxs-lookup"><span data-stu-id="e455f-140">Retrieves a textual representation of the iterator.</span></span>                                            |
| <span data-ttu-id="e455f-141">public AnyType value()</span><span class="sxs-lookup"><span data-stu-id="e455f-141">public AnyType value()</span></span>             | <span data-ttu-id="e455f-142">反復子により参照される (キー、値) ペアから値を返します。</span><span class="sxs-lookup"><span data-stu-id="e455f-142">Returns the value from the (key, value) pair that is referred to by the iterator.</span></span>              |
| <span data-ttu-id="e455f-143">public container valuePair()</span><span class="sxs-lookup"><span data-stu-id="e455f-143">public container valuePair()</span></span>       | <span data-ttu-id="e455f-144">キーと値を保持するコンテナーを取得します。</span><span class="sxs-lookup"><span data-stu-id="e455f-144">Retrieves a container that holds the key and the value.</span></span>                                        |
| <span data-ttu-id="e455f-145">public void next()</span><span class="sxs-lookup"><span data-stu-id="e455f-145">public void next()</span></span>                 | <span data-ttu-id="e455f-146">次の (キー、値) ペアに反復子を移動します。</span><span class="sxs-lookup"><span data-stu-id="e455f-146">Moves the iterator to the next (key, value) pair.</span></span>                                              |
| <span data-ttu-id="e455f-147">public void new(Map map)</span><span class="sxs-lookup"><span data-stu-id="e455f-147">public void new(Map map)</span></span>           | <span data-ttu-id="e455f-148">マップ内の要素をスキャンできるマップの新しい反復子を作成します。</span><span class="sxs-lookup"><span data-stu-id="e455f-148">Creates a new iterator for a map that lets you traverse through the elements in the map.</span></span>       |
| <span data-ttu-id="e455f-149">public void begin()</span><span class="sxs-lookup"><span data-stu-id="e455f-149">public void begin()</span></span>                | <span data-ttu-id="e455f-150">反復子をマップの先頭に移動します。</span><span class="sxs-lookup"><span data-stu-id="e455f-150">Moves the iterator to the start of the map.</span></span>                                                    |
| <span data-ttu-id="e455f-151">public void end()</span><span class="sxs-lookup"><span data-stu-id="e455f-151">public void end()</span></span>                  | <span data-ttu-id="e455f-152">マップで最後の要素の後に反復子を移動します。</span><span class="sxs-lookup"><span data-stu-id="e455f-152">Moves the iterator past the last element in the map.</span></span>                                           |
| <span data-ttu-id="e455f-153">public void delete()</span><span class="sxs-lookup"><span data-stu-id="e455f-153">public void delete()</span></span>               | <span data-ttu-id="e455f-154">反復子によってポイントされている要素をマップから削除します。</span><span class="sxs-lookup"><span data-stu-id="e455f-154">Removes from the map the element that is pointed to by the iterator.</span></span>                           |

## <a name="method-definitionstring"></a><span data-ttu-id="e455f-155">メソッド definitionString</span><span class="sxs-lookup"><span data-stu-id="e455f-155">Method definitionString</span></span>

<span data-ttu-id="e455f-156">"\[int -&gt; str\] 反復子" など、反復子の型のテキスト表現を取得します。</span><span class="sxs-lookup"><span data-stu-id="e455f-156">Retrieves a textual representation of the iterator type, such as "\[int -&gt; str\] iterator".</span></span>

```xpp
public str definitionString()
```

### <a name="return-value---definitionstring"></a><span data-ttu-id="e455f-157">戻り値 - definitionString</span><span class="sxs-lookup"><span data-stu-id="e455f-157">Return Value - definitionString</span></span>

<span data-ttu-id="e455f-158">反復子を説明する文字列。</span><span class="sxs-lookup"><span data-stu-id="e455f-158">A string that describes the iterator.</span></span>

## <a name="method-domainvalue"></a><span data-ttu-id="e455f-159">メソッド domainValue</span><span class="sxs-lookup"><span data-stu-id="e455f-159">Method domainValue</span></span>

<span data-ttu-id="e455f-160">反復子により参照される (キー、値) ペアにおけるキーの値を返します。</span><span class="sxs-lookup"><span data-stu-id="e455f-160">Returns the value of the key in the (key, value) pair that is referred to by the iterator.</span></span>

```xpp
public AnyType domainValue()
```

### <a name="return-value---domainvalue"></a><span data-ttu-id="e455f-161">戻り値 - domainValue</span><span class="sxs-lookup"><span data-stu-id="e455f-161">Return Value - domainValue</span></span>

<span data-ttu-id="e455f-162">反復子によって現在参照されているマップ要素の最初の項目の値。</span><span class="sxs-lookup"><span data-stu-id="e455f-162">The value of the first item in the map element that is currently referred to by the iterator.</span></span>

## <a name="method-find"></a><span data-ttu-id="e455f-163">メソッド find</span><span class="sxs-lookup"><span data-stu-id="e455f-163">Method find</span></span>

<span data-ttu-id="e455f-164">指定したキー値を検索します。</span><span class="sxs-lookup"><span data-stu-id="e455f-164">Searches for the specified key value.</span></span>

```xpp
public boolean find(AnyType value)
```

### <a name="parameters---find"></a><span data-ttu-id="e455f-165">パラメーター - find</span><span class="sxs-lookup"><span data-stu-id="e455f-165">Parameters - find</span></span>

<span data-ttu-id="e455f-166">値</span><span class="sxs-lookup"><span data-stu-id="e455f-166">value</span></span>  
<span data-ttu-id="e455f-167">検索する値。</span><span class="sxs-lookup"><span data-stu-id="e455f-167">The value to search for.</span></span>

### <a name="return-value---find"></a><span data-ttu-id="e455f-168">戻り値 - find</span><span class="sxs-lookup"><span data-stu-id="e455f-168">Return Value - find</span></span>

<span data-ttu-id="e455f-169">値が見つかった場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="e455f-169">true if the value is found; otherwise, false.</span></span>

### <a name="remarks---find"></a><span data-ttu-id="e455f-170">備考 - find</span><span class="sxs-lookup"><span data-stu-id="e455f-170">Remarks - find</span></span>

<span data-ttu-id="e455f-171">True が返された場合、このメソッドは、反復子を要素に配置します。それ以外の場合、MapIterator.more メソッドは false を返します。</span><span class="sxs-lookup"><span data-stu-id="e455f-171">If true is returned, the method positions the iterator at the element; otherwise, the MapIterator.more method returns false.</span></span>

## <a name="method-key"></a><span data-ttu-id="e455f-172">メソッド key</span><span class="sxs-lookup"><span data-stu-id="e455f-172">Method key</span></span>

<span data-ttu-id="e455f-173">反復子により参照される (キー、値) ペアからキーを返します。</span><span class="sxs-lookup"><span data-stu-id="e455f-173">Returns the key from the (key, value) pair that is referred to by the iterator.</span></span>

```xpp
public AnyType key()
```

### <a name="return-value---key"></a><span data-ttu-id="e455f-174">戻り値 - key</span><span class="sxs-lookup"><span data-stu-id="e455f-174">Return Value - key</span></span>

<span data-ttu-id="e455f-175">マップ反復子によって示されるマップ エントリのキー値。</span><span class="sxs-lookup"><span data-stu-id="e455f-175">The key value of the map entry that is denoted by the iterator.</span></span>

### <a name="remarks---key"></a><span data-ttu-id="e455f-176">備考 - key</span><span class="sxs-lookup"><span data-stu-id="e455f-176">Remarks - key</span></span>

<span data-ttu-id="e455f-177">マップ要素のキー値を取得する前に要素が存在するかどうかをテストするには、SetIterator.more メソッドを使用します。</span><span class="sxs-lookup"><span data-stu-id="e455f-177">Use the SetIterator.more method to test whether an element exists before you try to retrieve the key value of the map element.</span></span>

### <a name="examples---key"></a><span data-ttu-id="e455f-178">例 - key</span><span class="sxs-lookup"><span data-stu-id="e455f-178">Examples - key</span></span>

<span data-ttu-id="e455f-179">次の例では、マップを反復処理し、マップ内のすべての要素の説明を返します。</span><span class="sxs-lookup"><span data-stu-id="e455f-179">The following example iterates through a map and returns a description of all the elements in the map.</span></span>

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

## <a name="method-more"></a><span data-ttu-id="e455f-180">メソッド more</span><span class="sxs-lookup"><span data-stu-id="e455f-180">Method more</span></span>

<span data-ttu-id="e455f-181">反復子が有効な (キー、値 ) ペアを検出するかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="e455f-181">Determines whether the iterator finds a valid (key, value) pair.</span></span>

```xpp
public boolean more()
```

### <a name="return-value---more"></a><span data-ttu-id="e455f-182">戻り値 - more</span><span class="sxs-lookup"><span data-stu-id="e455f-182">Return Value - more</span></span>

<span data-ttu-id="e455f-183">より多くの (キー、値) の組み合わせがマップで使用可能な場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="e455f-183">true if more (key, value) pairs are available in the map; otherwise, false.</span></span>

### <a name="remarks---more"></a><span data-ttu-id="e455f-184">備考 - more</span><span class="sxs-lookup"><span data-stu-id="e455f-184">Remarks - more</span></span>

<span data-ttu-id="e455f-185">more メソッドが false を返すときに反復子が指す要素にアクセスしようとするとエラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="e455f-185">If you try to access an element that is pointed to by an iterator when the more method returns false, you receive an error.</span></span> <span data-ttu-id="e455f-186">より多くのメソッドは、反復子が有効な要素を指しているかどうかだけをテストします。</span><span class="sxs-lookup"><span data-stu-id="e455f-186">The more method only tests whether the iterator points to a valid element.</span></span> <span data-ttu-id="e455f-187">マップにより多くの要素があるかどうかはテストされません。</span><span class="sxs-lookup"><span data-stu-id="e455f-187">It does not test whether there are more elements in the map.</span></span>

### <a name="examples---more"></a><span data-ttu-id="e455f-188">例 - more</span><span class="sxs-lookup"><span data-stu-id="e455f-188">Examples - more</span></span>

<span data-ttu-id="e455f-189">次の例では、more メソッドを使用してマップ内の要素がまだ存在するかどうかを調べることによって、マップを反復処理します。</span><span class="sxs-lookup"><span data-stu-id="e455f-189">The following example iterates through a map by using the more method to check whether there are still elements in the map.</span></span> <span data-ttu-id="e455f-190">マップ内のすべての要素の説明を返します。</span><span class="sxs-lookup"><span data-stu-id="e455f-190">It then returns a description of all the elements in the map.</span></span>

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

## <a name="method-rangevalue"></a><span data-ttu-id="e455f-191">メソッド rangeValue</span><span class="sxs-lookup"><span data-stu-id="e455f-191">Method rangeValue</span></span>

<span data-ttu-id="e455f-192">反復子により参照される (キー、値) ペアにおける値の値を返します。</span><span class="sxs-lookup"><span data-stu-id="e455f-192">Returns the value of the value in the (key, value) pair that is referred to by the iterator.</span></span>

```xpp
public AnyType rangeValue()
```

### <a name="return-value---rangevalue"></a><span data-ttu-id="e455f-193">戻り値 - rangeValue</span><span class="sxs-lookup"><span data-stu-id="e455f-193">Return Value - rangeValue</span></span>

<span data-ttu-id="e455f-194">反復子によって現在参照されているマップ要素の 2 番目の項目の値。</span><span class="sxs-lookup"><span data-stu-id="e455f-194">The value of the second item in the map element that is currently referred to by the iterator.</span></span>

### <a name="remarks---rangevalue"></a><span data-ttu-id="e455f-195">備考 - rangeValue</span><span class="sxs-lookup"><span data-stu-id="e455f-195">Remarks - rangeValue</span></span>

<span data-ttu-id="e455f-196">rangeValue メソッドは MapIterator.value メソッドと同じ機能を持ちますが、domainValue メソッドに対応するメソッドとして使用できます。</span><span class="sxs-lookup"><span data-stu-id="e455f-196">The rangeValue method has the same functionality as the MapIterator.value method, but it is available as a counterpart to the domainValue method.</span></span>

## <a name="method-tostring"></a><span data-ttu-id="e455f-197">メソッド toString</span><span class="sxs-lookup"><span data-stu-id="e455f-197">Method toString</span></span>

<span data-ttu-id="e455f-198">反復子のテキスト表現を取得します。</span><span class="sxs-lookup"><span data-stu-id="e455f-198">Retrieves a textual representation of the iterator.</span></span>

```xpp
public str toString()
```

### <a name="return-value---tostring"></a><span data-ttu-id="e455f-199">戻り値 - toString</span><span class="sxs-lookup"><span data-stu-id="e455f-199">Return Value - toString</span></span>

<span data-ttu-id="e455f-200">反復子を説明する文字列。</span><span class="sxs-lookup"><span data-stu-id="e455f-200">The string that describes the iterator.</span></span>

### <a name="remarks---tostring"></a><span data-ttu-id="e455f-201">備考 - toString</span><span class="sxs-lookup"><span data-stu-id="e455f-201">Remarks - toString</span></span>

<span data-ttu-id="e455f-202">反復子がセット内の最初の要素をポイントする場合、文字列にはこの表現が次のフォームで含まれます: "(開始)\[ *値*\]"</span><span class="sxs-lookup"><span data-stu-id="e455f-202">If the iterator points to the first element in the set, the string will contain an indication of this, in the form: "(begin)\[ *value*\]".</span></span> <span data-ttu-id="e455f-203">反復子が要素をポイントしている場合 (つまり、MapIterator.more メソッドが false を返す場合)、返される文字列は「(終了)」になります。</span><span class="sxs-lookup"><span data-stu-id="e455f-203">If the iterator does not point to an element (that is, if the MapIterator.more method returns false), the string that is returned is "(end)".</span></span> <span data-ttu-id="e455f-204">反復子が値をポイントしている場合、文字列は "\[*値*\]" で、*値*が要素値の文字列表現です。</span><span class="sxs-lookup"><span data-stu-id="e455f-204">If the iterator points to a value, the string is "\[ *value*\]", where *value* is a string representation of the element value.</span></span>

### <a name="examples---tostring"></a><span data-ttu-id="e455f-205">例 - toString</span><span class="sxs-lookup"><span data-stu-id="e455f-205">Examples - toString</span></span>

<span data-ttu-id="e455f-206">次の例では、整数またはクラス マップを反復処理し、各マップ要素に関する情報を出力します。</span><span class="sxs-lookup"><span data-stu-id="e455f-206">The following example iterates through an integer or class map, and prints information about each map element.</span></span> <span data-ttu-id="e455f-207">MapIterator.toString メソッドを使用して各マップ要素でのクラスのテキスト表現を返します。</span><span class="sxs-lookup"><span data-stu-id="e455f-207">It uses the MapIterator.toString method to return a textual representation of the class in each map element.</span></span>

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

## <a name="method-value"></a><span data-ttu-id="e455f-208">メソッド value</span><span class="sxs-lookup"><span data-stu-id="e455f-208">Method value</span></span>

<span data-ttu-id="e455f-209">反復子により参照される (キー、値) ペアから値を返します。</span><span class="sxs-lookup"><span data-stu-id="e455f-209">Returns the value from the (key, value) pair that is referred to by the iterator.</span></span>

```xpp
public AnyType value()
```

### <a name="return-value---value"></a><span data-ttu-id="e455f-210">戻り値 - value</span><span class="sxs-lookup"><span data-stu-id="e455f-210">Return Value - value</span></span>

<span data-ttu-id="e455f-211">マップ反復子によって示されるマップ要素からの値。</span><span class="sxs-lookup"><span data-stu-id="e455f-211">The value from the map element that is denoted by the map iterator.</span></span>

### <a name="remarks---value"></a><span data-ttu-id="e455f-212">備考 - value</span><span class="sxs-lookup"><span data-stu-id="e455f-212">Remarks - value</span></span>

<span data-ttu-id="e455f-213">マップ要素のキー値を取得する前に要素が存在するかどうかをテストするには、MapIterator.more メソッドを使用します。</span><span class="sxs-lookup"><span data-stu-id="e455f-213">Use the MapIterator.more method to test whether an element exists before you try to retrieve the key value of the map element.</span></span>

### <a name="examples---value"></a><span data-ttu-id="e455f-214">例 - value</span><span class="sxs-lookup"><span data-stu-id="e455f-214">Examples - value</span></span>

<span data-ttu-id="e455f-215">次の例では、マップを反復処理し、マップ内のすべての要素のリストを返します。</span><span class="sxs-lookup"><span data-stu-id="e455f-215">The following example iterates through a map and returns a list of all the elements in the map.</span></span>

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

## <a name="method-valuepair"></a><span data-ttu-id="e455f-216">メソッド valuePair</span><span class="sxs-lookup"><span data-stu-id="e455f-216">Method valuePair</span></span>

<span data-ttu-id="e455f-217">キーと値を保持するコンテナーを取得します。</span><span class="sxs-lookup"><span data-stu-id="e455f-217">Retrieves a container that holds the key and the value.</span></span>

```xpp
public container valuePair()
```

### <a name="return-value---valuepair"></a><span data-ttu-id="e455f-218">戻り値 - valuePair</span><span class="sxs-lookup"><span data-stu-id="e455f-218">Return Value - valuePair</span></span>

<span data-ttu-id="e455f-219">キーと値を保持するコンテナーです。</span><span class="sxs-lookup"><span data-stu-id="e455f-219">A container that holds the key and the value.</span></span>

### <a name="remarks---valuepair"></a><span data-ttu-id="e455f-220">備考 - valuePair</span><span class="sxs-lookup"><span data-stu-id="e455f-220">Remarks - valuePair</span></span>

<span data-ttu-id="e455f-221">オブジェクトをコンテナーに配置することはできません。</span><span class="sxs-lookup"><span data-stu-id="e455f-221">Objects cannot reside in containers.</span></span> <span data-ttu-id="e455f-222">したがって、キーまたは値のいずれかがオブジェクトである場合、例外が発生します。</span><span class="sxs-lookup"><span data-stu-id="e455f-222">Therefore, an exception is raised if either the key or the value is an object.</span></span>

## <a name="method-next"></a><span data-ttu-id="e455f-223">メソッド next</span><span class="sxs-lookup"><span data-stu-id="e455f-223">Method next</span></span>

<span data-ttu-id="e455f-224">次の (キー、値) ペアに反復子を移動します。</span><span class="sxs-lookup"><span data-stu-id="e455f-224">Moves the iterator to the next (key, value) pair.</span></span>

```xpp
public void next()
```

### <a name="remarks---next"></a><span data-ttu-id="e455f-225">備考 - next</span><span class="sxs-lookup"><span data-stu-id="e455f-225">Remarks - next</span></span>

<span data-ttu-id="e455f-226">MapIterator.more メソッドを使用すると、マップ内にさらに要素があるかどうか判断することができます。</span><span class="sxs-lookup"><span data-stu-id="e455f-226">You can use the MapIterator.more method to determine whether there are any more elements in the map.</span></span>

### <a name="examples---next"></a><span data-ttu-id="e455f-227">例 - next</span><span class="sxs-lookup"><span data-stu-id="e455f-227">Examples - next</span></span>

<span data-ttu-id="e455f-228">次の例では、next メソッドを使用してマップを反復処理し、マップ内のすべての要素のリストを返します。</span><span class="sxs-lookup"><span data-stu-id="e455f-228">The following example uses the next method to iterate through a map and returns a list of all the elements in the map.</span></span>

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

## <a name="method-new"></a><span data-ttu-id="e455f-229">メソッド new</span><span class="sxs-lookup"><span data-stu-id="e455f-229">Method new</span></span>

<span data-ttu-id="e455f-230">マップ内の要素をスキャンできるマップの新しい反復子を作成します。</span><span class="sxs-lookup"><span data-stu-id="e455f-230">Creates a new iterator for a map that lets you traverse through the elements in the map.</span></span>

```xpp
public void new(Map map)
```

### <a name="parameters---new"></a><span data-ttu-id="e455f-231">パラメーター - new</span><span class="sxs-lookup"><span data-stu-id="e455f-231">Parameters - new</span></span>

<span data-ttu-id="e455f-232">マップ</span><span class="sxs-lookup"><span data-stu-id="e455f-232">map</span></span>  
<span data-ttu-id="e455f-233">反復子を作成するマップ。</span><span class="sxs-lookup"><span data-stu-id="e455f-233">The map for which to create an iterator.</span></span>

### <a name="remarks---new"></a><span data-ttu-id="e455f-234">備考 - new</span><span class="sxs-lookup"><span data-stu-id="e455f-234">Remarks - new</span></span>

<span data-ttu-id="e455f-235">反復子は、マップが空でない場合、マップの最初の値に配置されます。</span><span class="sxs-lookup"><span data-stu-id="e455f-235">The iterator is positioned at the first value in the map if the map is not empty.</span></span>

### <a name="examples---new"></a><span data-ttu-id="e455f-236">例 - new</span><span class="sxs-lookup"><span data-stu-id="e455f-236">Examples - new</span></span>

<span data-ttu-id="e455f-237">次の例では、(整数、クラス) のペアのマップを作成し、マップを移動する反復子を作成します。</span><span class="sxs-lookup"><span data-stu-id="e455f-237">The following example creates a map of (integer, class) pairs and then creates an iterator to traverse the map.</span></span>

```xpp
Map iim = new Map(Types::Integer, Types::Class); 
MapIterator it; 
it = new MapIterator (iim);
```

## <a name="method-begin"></a><span data-ttu-id="e455f-238">メソッド begin</span><span class="sxs-lookup"><span data-stu-id="e455f-238">Method begin</span></span>

<span data-ttu-id="e455f-239">反復子をマップの先頭に移動します。</span><span class="sxs-lookup"><span data-stu-id="e455f-239">Moves the iterator to the start of the map.</span></span>

```xpp
public void begin()
```

### <a name="remarks---begin"></a><span data-ttu-id="e455f-240">備考 - begin</span><span class="sxs-lookup"><span data-stu-id="e455f-240">Remarks - begin</span></span>

<span data-ttu-id="e455f-241">新しく作成されるマップ反復子は、マップの最初の要素に配置されるため、セットを通じて反復する前に開始メソッドを呼び出す必要はありません。</span><span class="sxs-lookup"><span data-stu-id="e455f-241">Newly created map iterators are positioned at the first element in the map, so you do not have to call the begin method before you iterate through the set.</span></span> <span data-ttu-id="e455f-242">ポインターをリセットする場合は、開始メソッドを呼び出す必要があります。</span><span class="sxs-lookup"><span data-stu-id="e455f-242">You must call the begin method if you want to reset the pointer.</span></span>

## <a name="method-end"></a><span data-ttu-id="e455f-243">メソッド end</span><span class="sxs-lookup"><span data-stu-id="e455f-243">Method end</span></span>

<span data-ttu-id="e455f-244">マップで最後の要素の後に反復子を移動します。</span><span class="sxs-lookup"><span data-stu-id="e455f-244">Moves the iterator past the last element in the map.</span></span>

```xpp
public void end()
```

### <a name="remarks---end"></a><span data-ttu-id="e455f-245">備考 - end</span><span class="sxs-lookup"><span data-stu-id="e455f-245">Remarks - end</span></span>

<span data-ttu-id="e455f-246">このメソッドを実行すると、MapIterator.more メソッドが false に戻ります。</span><span class="sxs-lookup"><span data-stu-id="e455f-246">After this method runs, the MapIterator.more method will return false.</span></span>

## <a name="method-delete"></a><span data-ttu-id="e455f-247">メソッド delete</span><span class="sxs-lookup"><span data-stu-id="e455f-247">Method delete</span></span>

<span data-ttu-id="e455f-248">反復子によってポイントされている要素をマップから削除します。</span><span class="sxs-lookup"><span data-stu-id="e455f-248">Removes from the map the element that is pointed to by the iterator.</span></span>

```xpp
public void delete()
```

### <a name="remarks---delete"></a><span data-ttu-id="e455f-249">備考 - delete</span><span class="sxs-lookup"><span data-stu-id="e455f-249">Remarks - delete</span></span>

<span data-ttu-id="e455f-250">反復子は、delete メソッドが呼び出された後に次の要素を指します。</span><span class="sxs-lookup"><span data-stu-id="e455f-250">The iterator points to the next element after the delete method is invoked.</span></span>

