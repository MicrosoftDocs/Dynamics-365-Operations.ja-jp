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
# <a name="class-listiterator"></a><span data-ttu-id="4f16b-103">クラス ListIterator</span><span class="sxs-lookup"><span data-stu-id="4f16b-103">Class ListIterator</span></span>

[!include [banner](../../includes/banner.md)]

```xpp
class ListIterator extends Object
```

<span data-ttu-id="4f16b-104">ListIterator クラスは、一覧内の要素を反復処理するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="4f16b-104">The ListIterator class is used to iterate over the elements in a list.</span></span>

## <a name="remarks"></a><span data-ttu-id="4f16b-105">備考</span><span class="sxs-lookup"><span data-stu-id="4f16b-105">Remarks</span></span>

<span data-ttu-id="4f16b-106">リストの反復子は、反復処理する対象となるリストにポインターとして表示することができます。</span><span class="sxs-lookup"><span data-stu-id="4f16b-106">List iterators can be viewed as pointers into the lists over which they iterate.</span></span> <span data-ttu-id="4f16b-107">繰り返しを開始する機能は利用可能であり、より多くの要素が利用可能であるかどうかを決定し、繰り返しによりポイントされる要素をフェッチします。</span><span class="sxs-lookup"><span data-stu-id="4f16b-107">Functionality is available to start the iteration, determine whether more elements are available, and fetch the element that is pointed to by the iterator.</span></span> <span data-ttu-id="4f16b-108">繰り返し中に要素が発生する順序は、要素が挿入される順序によって定義されます。</span><span class="sxs-lookup"><span data-stu-id="4f16b-108">The order in which the elements occur during iteration is defined by the sequence in which the elements are inserted.</span></span> <span data-ttu-id="4f16b-109">要素を挿入するには、List.addStart、List.addEnd、または ListIterator.insert メソッドを使用します。</span><span class="sxs-lookup"><span data-stu-id="4f16b-109">Elements can be inserted by using the List.addStart, List.addEnd, or ListIterator.insert method.</span></span> <span data-ttu-id="4f16b-110">ListIterator クラスよりも ListEnumerator クラスを使用することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="4f16b-110">It is better to use the ListEnumerator class than the ListIterator class.</span></span> <span data-ttu-id="4f16b-111">反復処理するリストの反復子およびマップは、同じクライアント/サーバー側にある必要があります。</span><span class="sxs-lookup"><span data-stu-id="4f16b-111">List iterators and the maps over which they iterate must be on the same client/server side.</span></span> <span data-ttu-id="4f16b-112">ListIterator クラスを使用し、コードが Called from としてマークされている場合、リストと反復子が別の層で終了する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="4f16b-112">If you use the ListIterator class, and code is marked as Called from, it is possible that the list and the iterator will be on different tiers.</span></span> <span data-ttu-id="4f16b-113">この場合、コードは失敗します。</span><span class="sxs-lookup"><span data-stu-id="4f16b-113">In this case, the code will fail.</span></span> <span data-ttu-id="4f16b-114">ListEnumerator クラスを使用する場合、列挙子はリストと同じ層に自動的に作成されます。</span><span class="sxs-lookup"><span data-stu-id="4f16b-114">If you use the ListEnumerator class, the enumerator is automatically created on the same tier as the list.</span></span> <span data-ttu-id="4f16b-115">また、リスト内の次のアイテムに移動するには、反復子リストを使用している場合は、より多くのメソッドと次のメソッドを明示的に呼び出す必要があります。</span><span class="sxs-lookup"><span data-stu-id="4f16b-115">Additionally, to move to the next item in a list, you must explicitly call the more and next methods if you are using a list iterator.</span></span> <span data-ttu-id="4f16b-116">ListEnumerator クラスを使用する場合、moveNext メソッドを呼び出すだけです。</span><span class="sxs-lookup"><span data-stu-id="4f16b-116">If you use the ListEnumerator class, you only have to call the moveNext method.</span></span> <span data-ttu-id="4f16b-117">リスト列挙子を使用できない唯一の状況は、リストから要素を削除する必要がある場合です。</span><span class="sxs-lookup"><span data-stu-id="4f16b-117">The only situation where you cannot use a list enumerator is where you need to delete elements from a list.</span></span> <span data-ttu-id="4f16b-118">詳細については、「メソッドの削除」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="4f16b-118">For more information, see the delete method.</span></span>

## <a name="examples"></a><span data-ttu-id="4f16b-119">例</span><span class="sxs-lookup"><span data-stu-id="4f16b-119">Examples</span></span>

<span data-ttu-id="4f16b-120">次の例では、リストとそれを指す反復子を作成します。</span><span class="sxs-lookup"><span data-stu-id="4f16b-120">The following example creates a list and an iterator to point to it.</span></span> <span data-ttu-id="4f16b-121">ListIterator クラスのさまざまなメソッドを使用して、一覧の説明と一覧内の項目を出力します。</span><span class="sxs-lookup"><span data-stu-id="4f16b-121">It then uses various methods on the ListIterator class to print a description of the list, and the items in the list.</span></span>

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

## <a name="methods"></a><span data-ttu-id="4f16b-122">メソッド</span><span class="sxs-lookup"><span data-stu-id="4f16b-122">Methods</span></span>

| <span data-ttu-id="4f16b-123">方法</span><span class="sxs-lookup"><span data-stu-id="4f16b-123">Method</span></span>                               | <span data-ttu-id="4f16b-124">説明</span><span class="sxs-lookup"><span data-stu-id="4f16b-124">Description</span></span>                                                                                    |
|--------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4f16b-125">public str definitionString()</span><span class="sxs-lookup"><span data-stu-id="4f16b-125">public str definitionString()</span></span>        | <span data-ttu-id="4f16b-126">反復子のタイプのテキスト表現を返します。</span><span class="sxs-lookup"><span data-stu-id="4f16b-126">Returns a textual representation of the type of the iterator.</span></span>                                  |
| <span data-ttu-id="4f16b-127">public AnyType insert(AnyType value)</span><span class="sxs-lookup"><span data-stu-id="4f16b-127">public AnyType insert(AnyType value)</span></span> | <span data-ttu-id="4f16b-128">反復子が現在ポイントしているリスト内の位置に新しい値を挿入します。</span><span class="sxs-lookup"><span data-stu-id="4f16b-128">Inserts a new value at the position in the list that the iterator currently points to.</span></span>         |
| <span data-ttu-id="4f16b-129">public boolean more()</span><span class="sxs-lookup"><span data-stu-id="4f16b-129">public boolean more()</span></span>                | <span data-ttu-id="4f16b-130">リスト反復子が有効な要素を指しているかどうかを判定します。</span><span class="sxs-lookup"><span data-stu-id="4f16b-130">Determines whether the list iterator points to a valid element.</span></span>                                |
| <span data-ttu-id="4f16b-131">public str toString()</span><span class="sxs-lookup"><span data-stu-id="4f16b-131">public str toString()</span></span>                | <span data-ttu-id="4f16b-132">反復子によりポイントされている現在のリスト値のテキスト形式を返します。</span><span class="sxs-lookup"><span data-stu-id="4f16b-132">Returns a textual representation of the current list value that is pointed to by the iterator.</span></span> |
| <span data-ttu-id="4f16b-133">public AnyType value()</span><span class="sxs-lookup"><span data-stu-id="4f16b-133">public AnyType value()</span></span>               | <span data-ttu-id="4f16b-134">反復子によりポイントされている値を取得します。</span><span class="sxs-lookup"><span data-stu-id="4f16b-134">Retrieves the value that is pointed to by the iterator.</span></span>                                        |
| <span data-ttu-id="4f16b-135">public void begin()</span><span class="sxs-lookup"><span data-stu-id="4f16b-135">public void begin()</span></span>                  | <span data-ttu-id="4f16b-136">反復子をリストの先頭に移動します。</span><span class="sxs-lookup"><span data-stu-id="4f16b-136">Moves the iterator to the start of the list.</span></span>                                                   |
| <span data-ttu-id="4f16b-137">public void next()</span><span class="sxs-lookup"><span data-stu-id="4f16b-137">public void next()</span></span>                   | <span data-ttu-id="4f16b-138">リストで次の要素に反復子を移動します。</span><span class="sxs-lookup"><span data-stu-id="4f16b-138">Moves the iterator to the next element in the list.</span></span>                                            |
| <span data-ttu-id="4f16b-139">public void end()</span><span class="sxs-lookup"><span data-stu-id="4f16b-139">public void end()</span></span>                    | <span data-ttu-id="4f16b-140">リストで最後の要素の後に反復子を移動します。</span><span class="sxs-lookup"><span data-stu-id="4f16b-140">Moves the iterator past the last element in the list.</span></span>                                          |
| <span data-ttu-id="4f16b-141">public void delete()</span><span class="sxs-lookup"><span data-stu-id="4f16b-141">public void delete()</span></span>                 | <span data-ttu-id="4f16b-142">反復子によってポイントされている要素を一覧から削除します。</span><span class="sxs-lookup"><span data-stu-id="4f16b-142">Removes the element that is pointed to by the iterator from the list.</span></span>                          |
| <span data-ttu-id="4f16b-143">public void new(List list)</span><span class="sxs-lookup"><span data-stu-id="4f16b-143">public void new(List list)</span></span>           | <span data-ttu-id="4f16b-144">特定のリストに対する新しい反復子を作成します。</span><span class="sxs-lookup"><span data-stu-id="4f16b-144">Creates a new iterator for a particular list.</span></span>                                                  |

## <a name="method-definitionstring"></a><span data-ttu-id="4f16b-145">メソッド definitionString</span><span class="sxs-lookup"><span data-stu-id="4f16b-145">Method definitionString</span></span>

<span data-ttu-id="4f16b-146">反復子のタイプのテキスト表現を返します。</span><span class="sxs-lookup"><span data-stu-id="4f16b-146">Returns a textual representation of the type of the iterator.</span></span>

```xpp
public str definitionString()
```

### <a name="return-value---definitionstring"></a><span data-ttu-id="4f16b-147">戻り値 - definitionString</span><span class="sxs-lookup"><span data-stu-id="4f16b-147">Return Value - definitionString</span></span>

<span data-ttu-id="4f16b-148">反復子のタイプを含む文字列。</span><span class="sxs-lookup"><span data-stu-id="4f16b-148">A string that contains the type of the iterator.</span></span>

### <a name="remarks---definitionstring"></a><span data-ttu-id="4f16b-149">備考 - definitionString</span><span class="sxs-lookup"><span data-stu-id="4f16b-149">Remarks - definitionString</span></span>

<span data-ttu-id="4f16b-150">例: int リスト反復子。</span><span class="sxs-lookup"><span data-stu-id="4f16b-150">For example: int list iterator.</span></span>

## <a name="method-insert"></a><span data-ttu-id="4f16b-151">メソッド insert</span><span class="sxs-lookup"><span data-stu-id="4f16b-151">Method insert</span></span>

<span data-ttu-id="4f16b-152">反復子が現在ポイントしているリスト内の位置に新しい値を挿入します。</span><span class="sxs-lookup"><span data-stu-id="4f16b-152">Inserts a new value at the position in the list that the iterator currently points to.</span></span>

```xpp
public AnyType insert(AnyType value)
```

### <a name="parameters---insert"></a><span data-ttu-id="4f16b-153">パラメーター - insert</span><span class="sxs-lookup"><span data-stu-id="4f16b-153">Parameters - insert</span></span>

<span data-ttu-id="4f16b-154">値</span><span class="sxs-lookup"><span data-stu-id="4f16b-154">value</span></span>  
<span data-ttu-id="4f16b-155">リストに挿入する項目の値。</span><span class="sxs-lookup"><span data-stu-id="4f16b-155">The value of the item to insert into the list.</span></span>

### <a name="return-value---insert"></a><span data-ttu-id="4f16b-156">戻り値 - insert</span><span class="sxs-lookup"><span data-stu-id="4f16b-156">Return Value - insert</span></span>

<span data-ttu-id="4f16b-157">リストに挿入された値。</span><span class="sxs-lookup"><span data-stu-id="4f16b-157">The value that was inserted into the list.</span></span>

### <a name="remarks---insert"></a><span data-ttu-id="4f16b-158">備考 - insert</span><span class="sxs-lookup"><span data-stu-id="4f16b-158">Remarks - insert</span></span>

<span data-ttu-id="4f16b-159">value パラメーターは、リストと同じタイプである必要があります。</span><span class="sxs-lookup"><span data-stu-id="4f16b-159">The value parameter must be the same type as the list.</span></span>

### <a name="examples---insert"></a><span data-ttu-id="4f16b-160">例 - insert</span><span class="sxs-lookup"><span data-stu-id="4f16b-160">Examples - insert</span></span>

<span data-ttu-id="4f16b-161">次の例では、10 個のアイテムを持つリストを作成し、ListIterator.insert メソッドを使用してリスト内の 3 番目のアイテムとして新しい値を挿入します。</span><span class="sxs-lookup"><span data-stu-id="4f16b-161">The following example creates a list that has ten items and then uses the ListIterator.insert method to insert a new value as the third item in the list.</span></span>

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

## <a name="method-more"></a><span data-ttu-id="4f16b-162">メソッド more</span><span class="sxs-lookup"><span data-stu-id="4f16b-162">Method more</span></span>

<span data-ttu-id="4f16b-163">リスト反復子が有効な要素を指しているかどうかを判定します。</span><span class="sxs-lookup"><span data-stu-id="4f16b-163">Determines whether the list iterator points to a valid element.</span></span>

```xpp
public boolean more()
```

### <a name="return-value---more"></a><span data-ttu-id="4f16b-164">戻り値 - more</span><span class="sxs-lookup"><span data-stu-id="4f16b-164">Return Value - more</span></span>

<span data-ttu-id="4f16b-165">リスト反復子が有効な要素を指定する場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="4f16b-165">true if the list iterator points to a valid element; otherwise, false.</span></span>

### <a name="remarks---more"></a><span data-ttu-id="4f16b-166">備考 - more</span><span class="sxs-lookup"><span data-stu-id="4f16b-166">Remarks - more</span></span>

<span data-ttu-id="4f16b-167">このメソッドが false を返すときに要素にアクセスしようとするとエラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="4f16b-167">Attempting to access an element when this method returns false will cause an error.</span></span>

### <a name="examples---more"></a><span data-ttu-id="4f16b-168">例 - more</span><span class="sxs-lookup"><span data-stu-id="4f16b-168">Examples - more</span></span>

<span data-ttu-id="4f16b-169">次の例では、ListIterator.more メソッドを使用してリストに要素があるかどうかを確認し、リスト内のすべての要素の値を出力する while ループを実行します。</span><span class="sxs-lookup"><span data-stu-id="4f16b-169">The following example uses the ListIterator.more method to check whether there are more elements in the list and then runs through the while loop, which prints the values of all the elements in the list.</span></span>

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

## <a name="method-tostring"></a><span data-ttu-id="4f16b-170">メソッド toString</span><span class="sxs-lookup"><span data-stu-id="4f16b-170">Method toString</span></span>

<span data-ttu-id="4f16b-171">反復子によりポイントされている現在のリスト値のテキスト形式を返します。</span><span class="sxs-lookup"><span data-stu-id="4f16b-171">Returns a textual representation of the current list value that is pointed to by the iterator.</span></span>

```xpp
public str toString()
```

### <a name="return-value---tostring"></a><span data-ttu-id="4f16b-172">戻り値 - toString</span><span class="sxs-lookup"><span data-stu-id="4f16b-172">Return Value - toString</span></span>

<span data-ttu-id="4f16b-173">現在の値の説明を含む文字列。</span><span class="sxs-lookup"><span data-stu-id="4f16b-173">A string that contains a description of the current value.</span></span>

### <a name="remarks---tostring"></a><span data-ttu-id="4f16b-174">備考 - toString</span><span class="sxs-lookup"><span data-stu-id="4f16b-174">Remarks - toString</span></span>

<span data-ttu-id="4f16b-175">反復子がリスト内の最初の要素を指している場合、文字列には "(開始)\[値\]" という形式の文字列が含まれます。反復子が要素を指していない場合 (つまり、more() メソッドが false を返す場合)、返される次の文字列は: (終了) になります。</span><span class="sxs-lookup"><span data-stu-id="4f16b-175">If the iterator points to the first element in the list, the string will contain an indication of this, in the form "(begin)\[value\]" If the iterator does not point to an element (that is, the more() method returns false), the following string returned is: (end).</span></span> <span data-ttu-id="4f16b-176">反復子が値をポイントしている場合、文字列は "\[値\]" で、値が要素値の文字列表現です。</span><span class="sxs-lookup"><span data-stu-id="4f16b-176">If the iterator points to a value, the string is "\[value\]", where value is a string representation of the element value.</span></span>

### <a name="examples---tostring"></a><span data-ttu-id="4f16b-177">例 - toString</span><span class="sxs-lookup"><span data-stu-id="4f16b-177">Examples - toString</span></span>

<span data-ttu-id="4f16b-178">次の例では、リスト内の 2 つの値の値の説明を表示します。</span><span class="sxs-lookup"><span data-stu-id="4f16b-178">The following example prints the following description of the values of the two values in a list:</span></span>

1.  <span data-ttu-id="4f16b-179">(開始) \[2\]</span><span class="sxs-lookup"><span data-stu-id="4f16b-179">(begin) \[2\]</span></span>
2.  <span data-ttu-id="4f16b-180">\[1\]</span><span class="sxs-lookup"><span data-stu-id="4f16b-180">\[1\]</span></span>

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

## <a name="method-value"></a><span data-ttu-id="4f16b-181">メソッド value</span><span class="sxs-lookup"><span data-stu-id="4f16b-181">Method value</span></span>

<span data-ttu-id="4f16b-182">反復子によりポイントされている値を取得します。</span><span class="sxs-lookup"><span data-stu-id="4f16b-182">Retrieves the value that is pointed to by the iterator.</span></span>

```xpp
public AnyType value()
```

### <a name="return-value---value"></a><span data-ttu-id="4f16b-183">戻り値 - value</span><span class="sxs-lookup"><span data-stu-id="4f16b-183">Return Value - value</span></span>

<span data-ttu-id="4f16b-184">反復子によりポイントされている値。</span><span class="sxs-lookup"><span data-stu-id="4f16b-184">The value that is pointed to by the iterator.</span></span>

### <a name="remarks---value"></a><span data-ttu-id="4f16b-185">備考 - value</span><span class="sxs-lookup"><span data-stu-id="4f16b-185">Remarks - value</span></span>

<span data-ttu-id="4f16b-186">リスト要素の値を取得する前に、ListIterator.more メソッドを使用して要素が存在するかどうかをテストします。</span><span class="sxs-lookup"><span data-stu-id="4f16b-186">Before you try to retrieve the value of a list element, use the ListIterator.more method to test whether an element exists.</span></span>

## <a name="method-begin"></a><span data-ttu-id="4f16b-187">メソッド begin</span><span class="sxs-lookup"><span data-stu-id="4f16b-187">Method begin</span></span>

<span data-ttu-id="4f16b-188">反復子をリストの先頭に移動します。</span><span class="sxs-lookup"><span data-stu-id="4f16b-188">Moves the iterator to the start of the list.</span></span>

```xpp
public void begin()
```

## <a name="method-next"></a><span data-ttu-id="4f16b-189">メソッド next</span><span class="sxs-lookup"><span data-stu-id="4f16b-189">Method next</span></span>

<span data-ttu-id="4f16b-190">リストで次の要素に反復子を移動します。</span><span class="sxs-lookup"><span data-stu-id="4f16b-190">Moves the iterator to the next element in the list.</span></span>

```xpp
public void next()
```

### <a name="remarks---next"></a><span data-ttu-id="4f16b-191">備考 - next</span><span class="sxs-lookup"><span data-stu-id="4f16b-191">Remarks - next</span></span>

<span data-ttu-id="4f16b-192">ListIterator.more メソッドを使用して、反復子が有効な要素を指しているかどうかを判断します。</span><span class="sxs-lookup"><span data-stu-id="4f16b-192">Use the ListIterator.more method to determine whether the iterator points to a valid element.</span></span>

### <a name="examples---next"></a><span data-ttu-id="4f16b-193">例 - next</span><span class="sxs-lookup"><span data-stu-id="4f16b-193">Examples - next</span></span>

<span data-ttu-id="4f16b-194">次の例では、ListIterator.next メソッドを使用して、各要素の値が出力されるときにリストをスキャンします。</span><span class="sxs-lookup"><span data-stu-id="4f16b-194">The following example uses the ListIterator.next method to traverse a list as the value of each element is printed.</span></span>

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

## <a name="method-end"></a><span data-ttu-id="4f16b-195">メソッド end</span><span class="sxs-lookup"><span data-stu-id="4f16b-195">Method end</span></span>

<span data-ttu-id="4f16b-196">リストで最後の要素の後に反復子を移動します。</span><span class="sxs-lookup"><span data-stu-id="4f16b-196">Moves the iterator past the last element in the list.</span></span>

```xpp
public void end()
```

### <a name="remarks---end"></a><span data-ttu-id="4f16b-197">備考 - end</span><span class="sxs-lookup"><span data-stu-id="4f16b-197">Remarks - end</span></span>

<span data-ttu-id="4f16b-198">このメソッドが実行すると、ListIterator.more メソッドが false に戻ります。</span><span class="sxs-lookup"><span data-stu-id="4f16b-198">After this method runs, the ListIterator.more method will return false.</span></span>

## <a name="method-delete"></a><span data-ttu-id="4f16b-199">メソッド delete</span><span class="sxs-lookup"><span data-stu-id="4f16b-199">Method delete</span></span>

<span data-ttu-id="4f16b-200">反復子によってポイントされている要素を一覧から削除します。</span><span class="sxs-lookup"><span data-stu-id="4f16b-200">Removes the element that is pointed to by the iterator from the list.</span></span>

```xpp
public void delete()
```

### <a name="remarks---delete"></a><span data-ttu-id="4f16b-201">備考 - delete</span><span class="sxs-lookup"><span data-stu-id="4f16b-201">Remarks - delete</span></span>

<span data-ttu-id="4f16b-202">反復子は、この削除の後に次の要素を指します。</span><span class="sxs-lookup"><span data-stu-id="4f16b-202">The iterator will point to the next element after the deletion.</span></span>

### <a name="examples---delete"></a><span data-ttu-id="4f16b-203">例 - delete</span><span class="sxs-lookup"><span data-stu-id="4f16b-203">Examples - delete</span></span>

<span data-ttu-id="4f16b-204">次の例では、3 つの要素を含むリストを作成し、リスト内の要素の説明を出力します。</span><span class="sxs-lookup"><span data-stu-id="4f16b-204">The following example creates a list that contains three elements and prints a description of the elements in the list.</span></span> <span data-ttu-id="4f16b-205">一覧の最初の要素を削除し、残りの要素の説明を印刷します。</span><span class="sxs-lookup"><span data-stu-id="4f16b-205">It then deletes the first element in the list and prints a description of the remaining elements.</span></span>

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

## <a name="method-new"></a><span data-ttu-id="4f16b-206">メソッド new</span><span class="sxs-lookup"><span data-stu-id="4f16b-206">Method new</span></span>

<span data-ttu-id="4f16b-207">特定のリストに対する新しい反復子を作成します。</span><span class="sxs-lookup"><span data-stu-id="4f16b-207">Creates a new iterator for a particular list.</span></span>

```xpp
public void new(List list)
```

### <a name="parameters---new"></a><span data-ttu-id="4f16b-208">パラメーター - new</span><span class="sxs-lookup"><span data-stu-id="4f16b-208">Parameters - new</span></span>

<span data-ttu-id="4f16b-209">リスト</span><span class="sxs-lookup"><span data-stu-id="4f16b-209">list</span></span>  
<span data-ttu-id="4f16b-210">反復子を作成するリスト。</span><span class="sxs-lookup"><span data-stu-id="4f16b-210">The list for which to create an iterator.</span></span>

### <a name="remarks---new"></a><span data-ttu-id="4f16b-211">備考 - new</span><span class="sxs-lookup"><span data-stu-id="4f16b-211">Remarks - new</span></span>

<span data-ttu-id="4f16b-212">反復子は、リストが空でない場合、リストの最初の値に配置されます。</span><span class="sxs-lookup"><span data-stu-id="4f16b-212">The iterator is positioned at the first value in the list, if the list is not empty.</span></span> <span data-ttu-id="4f16b-213">反復子および繰り返すリストは、同じクライアント/サーバー側にする必要があります。</span><span class="sxs-lookup"><span data-stu-id="4f16b-213">Iterators and the lists that they iterate over must be on the same client/server side.</span></span>

### <a name="examples---new"></a><span data-ttu-id="4f16b-214">例 - new</span><span class="sxs-lookup"><span data-stu-id="4f16b-214">Examples - new</span></span>

<span data-ttu-id="4f16b-215">次の例では、整数リストの反復子を作成します。</span><span class="sxs-lookup"><span data-stu-id="4f16b-215">The following example creates an iterator for a list of integers.</span></span>

```xpp
List il = new List(types::Integer); 
ListIterator it; 
it = new ListIterator (il);
```

