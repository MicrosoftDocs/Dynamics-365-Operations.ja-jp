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
# <a name="class-list"></a><span data-ttu-id="5b2b4-103">クラス リスト</span><span class="sxs-lookup"><span data-stu-id="5b2b4-103">Class List</span></span>

[!include [banner](../../includes/banner.md)]

```xpp
class List extends Object
```

<span data-ttu-id="5b2b4-104">順にアクセスされる任意の数の要素を含みます。</span><span class="sxs-lookup"><span data-stu-id="5b2b4-104">Contains any number of elements that are accessed sequentially.</span></span> <span data-ttu-id="5b2b4-105">リストは、あらゆる X++ 型の値を含めることができる構造です。</span><span class="sxs-lookup"><span data-stu-id="5b2b4-105">Lists are structures that can contain values of any X++ type.</span></span> <span data-ttu-id="5b2b4-106">リスト内のすべての値は同じタイプである必要があります。</span><span class="sxs-lookup"><span data-stu-id="5b2b4-106">All the values in the list must be of the same type.</span></span>

## <a name="remarks"></a><span data-ttu-id="5b2b4-107">備考</span><span class="sxs-lookup"><span data-stu-id="5b2b4-107">Remarks</span></span>

<span data-ttu-id="5b2b4-108">リスト内の値のタイプは、リストが作成されたときに指定され、後で変更することはできません。</span><span class="sxs-lookup"><span data-stu-id="5b2b4-108">The type of the values in the list is specified when the list is created and cannot be changed afterwards.</span></span> <span data-ttu-id="5b2b4-109">リストの実装は、リスト要素のトラバーサルを非常に高速にします。</span><span class="sxs-lookup"><span data-stu-id="5b2b4-109">The implementation of lists makes traversal of the list elements very fast.</span></span> <span data-ttu-id="5b2b4-110">リストを移動するには、ListEnumerator クラスを使用します。</span><span class="sxs-lookup"><span data-stu-id="5b2b4-110">Lists can be traversed by using the ListEnumerator class.</span></span> <span data-ttu-id="5b2b4-111">ListEnumerator オブジェクトを作成するには、List.getEnumerator を使用します。</span><span class="sxs-lookup"><span data-stu-id="5b2b4-111">To create a ListEnumerator object, use List.getEnumerator.</span></span>

## <a name="examples"></a><span data-ttu-id="5b2b4-112">例</span><span class="sxs-lookup"><span data-stu-id="5b2b4-112">Examples</span></span>

<span data-ttu-id="5b2b4-113">次の例では、整数のリストを作成し、リストの説明とそれに含まれる値を出力します。</span><span class="sxs-lookup"><span data-stu-id="5b2b4-113">The following example creates a list of integers and prints out a description of the list and the values that it contains.</span></span>

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

## <a name="methods"></a><span data-ttu-id="5b2b4-114">メソッド</span><span class="sxs-lookup"><span data-stu-id="5b2b4-114">Methods</span></span>

| <span data-ttu-id="5b2b4-115">方法</span><span class="sxs-lookup"><span data-stu-id="5b2b4-115">Method</span></span>                                                | <span data-ttu-id="5b2b4-116">説明</span><span class="sxs-lookup"><span data-stu-id="5b2b4-116">Description</span></span>                                                                           |
|-------------------------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="5b2b4-117">public AnyType addEnd(AnyType element)</span><span class="sxs-lookup"><span data-stu-id="5b2b4-117">public AnyType addEnd(AnyType element)</span></span>                | <span data-ttu-id="5b2b4-118">リストの末尾に値を追加します。</span><span class="sxs-lookup"><span data-stu-id="5b2b4-118">Adds a value to the end of the list.</span></span>                                                  |
| <span data-ttu-id="5b2b4-119">public AnyType addStart(AnyType element)</span><span class="sxs-lookup"><span data-stu-id="5b2b4-119">public AnyType addStart(AnyType element)</span></span>              | <span data-ttu-id="5b2b4-120">リストの冒頭に値を追加します。</span><span class="sxs-lookup"><span data-stu-id="5b2b4-120">Adds a value to the start of the list.</span></span>                                                |
| <span data-ttu-id="5b2b4-121">public str definitionString()</span><span class="sxs-lookup"><span data-stu-id="5b2b4-121">public str definitionString()</span></span>                         | <span data-ttu-id="5b2b4-122">リスト内のすべての要素のタイプの説明を返します。</span><span class="sxs-lookup"><span data-stu-id="5b2b4-122">Returns a description of the type of the elements in the list.</span></span>                        |
| <span data-ttu-id="5b2b4-123">public int elements()</span><span class="sxs-lookup"><span data-stu-id="5b2b4-123">public int elements()</span></span>                                 | <span data-ttu-id="5b2b4-124">リスト内の要素の数を指定します。</span><span class="sxs-lookup"><span data-stu-id="5b2b4-124">Specifies the number of elements in a list.</span></span>                                           |
| <span data-ttu-id="5b2b4-125">public boolean empty()</span><span class="sxs-lookup"><span data-stu-id="5b2b4-125">public boolean empty()</span></span>                                | <span data-ttu-id="5b2b4-126">一覧が空であるかどうかを判定します。</span><span class="sxs-lookup"><span data-stu-id="5b2b4-126">Determines whether a list is empty.</span></span>                                                   |
| <span data-ttu-id="5b2b4-127">public boolean equalTo(List l)</span><span class="sxs-lookup"><span data-stu-id="5b2b4-127">public boolean equalTo(List l)</span></span>                        | <span data-ttu-id="5b2b4-128">一覧が現在の一覧と同じかどうかを判定します。</span><span class="sxs-lookup"><span data-stu-id="5b2b4-128">Determines whether a list is the same as the current list.</span></span>                            |
| <span data-ttu-id="5b2b4-129">public ListEnumerator getEnumerator()</span><span class="sxs-lookup"><span data-stu-id="5b2b4-129">public ListEnumerator getEnumerator()</span></span>                 | <span data-ttu-id="5b2b4-130">リストのスキャンを可能にするリストの列挙子を作成します。</span><span class="sxs-lookup"><span data-stu-id="5b2b4-130">Creates an enumerator for a list which allows you to traverse the list.</span></span>               |
| <span data-ttu-id="5b2b4-131">public container pack()</span><span class="sxs-lookup"><span data-stu-id="5b2b4-131">public container pack()</span></span>                               | <span data-ttu-id="5b2b4-132">List クラスの現在のインスタンスをシリアル化します。</span><span class="sxs-lookup"><span data-stu-id="5b2b4-132">Serializes the current instance of the List class.</span></span>                                    |
| <span data-ttu-id="5b2b4-133">public str toString()</span><span class="sxs-lookup"><span data-stu-id="5b2b4-133">public str toString()</span></span>                                 | <span data-ttu-id="5b2b4-134">リスト内の値の説明を返します。</span><span class="sxs-lookup"><span data-stu-id="5b2b4-134">Returns a description of the values in the list.</span></span>                                      |
| <span data-ttu-id="5b2b4-135">public Types typeId()</span><span class="sxs-lookup"><span data-stu-id="5b2b4-135">public Types typeId()</span></span>                                 | <span data-ttu-id="5b2b4-136">リスト内の値のタイプを返します。</span><span class="sxs-lookup"><span data-stu-id="5b2b4-136">Returns the type of the values in a list.</span></span>                                             |
| <span data-ttu-id="5b2b4-137">public str xml(\[int indent\])</span><span class="sxs-lookup"><span data-stu-id="5b2b4-137">public str xml(\[int indent\])</span></span>                        | <span data-ttu-id="5b2b4-138">現在のオブジェクトを表す XML 文字列を返します。</span><span class="sxs-lookup"><span data-stu-id="5b2b4-138">Returns an XML string that represents the current object.</span></span>                             |
| <span data-ttu-id="5b2b4-139">::public static List create(container container)</span><span class="sxs-lookup"><span data-stu-id="5b2b4-139">::public static List create(container container)</span></span>      | <span data-ttu-id="5b2b4-140">以前の List.pack メソッドの呼び出しで取得したコンテナーからリストを作成します。</span><span class="sxs-lookup"><span data-stu-id="5b2b4-140">Creates a list from the container obtained from a prior call to the List.pack method.</span></span> |
| <span data-ttu-id="5b2b4-141">::public static List createFromXML(Object xmlnode)</span><span class="sxs-lookup"><span data-stu-id="5b2b4-141">::public static List createFromXML(Object xmlnode)</span></span>    |                                                                                       |
| <span data-ttu-id="5b2b4-142">::public static boolean equal(List list1, List list2)</span><span class="sxs-lookup"><span data-stu-id="5b2b4-142">::public static boolean equal(List list1, List list2)</span></span> | <span data-ttu-id="5b2b4-143">2 つのリストが同じかどうかを判定します。</span><span class="sxs-lookup"><span data-stu-id="5b2b4-143">Determines whether two lists are identical.</span></span>                                           |
| <span data-ttu-id="5b2b4-144">::public static List merge(List list1, List list2)</span><span class="sxs-lookup"><span data-stu-id="5b2b4-144">::public static List merge(List list1, List list2)</span></span>    | <span data-ttu-id="5b2b4-145">2 つのリストを組み合わせ、新しいリストを作成します。</span><span class="sxs-lookup"><span data-stu-id="5b2b4-145">Combines two lists to create a new list.</span></span>                                              |
| <span data-ttu-id="5b2b4-146">public void appendList(List list)</span><span class="sxs-lookup"><span data-stu-id="5b2b4-146">public void appendList(List list)</span></span>                     |                                                                                       |
| <span data-ttu-id="5b2b4-147">public void new(Types Type)</span><span class="sxs-lookup"><span data-stu-id="5b2b4-147">public void new(Types Type)</span></span>                           | <span data-ttu-id="5b2b4-148">リストを作成します。</span><span class="sxs-lookup"><span data-stu-id="5b2b4-148">Creates a list.</span></span>                                                                       |

## <a name="method-addend"></a><span data-ttu-id="5b2b4-149">メソッド addEnd</span><span class="sxs-lookup"><span data-stu-id="5b2b4-149">Method addEnd</span></span>

<span data-ttu-id="5b2b4-150">リストの末尾に値を追加します。</span><span class="sxs-lookup"><span data-stu-id="5b2b4-150">Adds a value to the end of the list.</span></span>

```xpp
public AnyType addEnd(AnyType element)
```

### <a name="parameters---addend"></a><span data-ttu-id="5b2b4-151">パラメーター - addEnd</span><span class="sxs-lookup"><span data-stu-id="5b2b4-151">Parameters - addEnd</span></span>

<span data-ttu-id="5b2b4-152">要素</span><span class="sxs-lookup"><span data-stu-id="5b2b4-152">element</span></span>  
<span data-ttu-id="5b2b4-153">リストの末尾に追加する値。</span><span class="sxs-lookup"><span data-stu-id="5b2b4-153">The value to add to the end of the list.</span></span>

### <a name="return-value---addend"></a><span data-ttu-id="5b2b4-154">戻り値 - addEnd</span><span class="sxs-lookup"><span data-stu-id="5b2b4-154">Return Value - addEnd</span></span>

<span data-ttu-id="5b2b4-155">リストに追加される値。</span><span class="sxs-lookup"><span data-stu-id="5b2b4-155">The value that is added to the list.</span></span>

## <a name="method-addstart"></a><span data-ttu-id="5b2b4-156">メソッド addStart</span><span class="sxs-lookup"><span data-stu-id="5b2b4-156">Method addStart</span></span>

<span data-ttu-id="5b2b4-157">リストの冒頭に値を追加します。</span><span class="sxs-lookup"><span data-stu-id="5b2b4-157">Adds a value to the start of the list.</span></span>

```xpp
public AnyType addStart(AnyType element)
```

### <a name="parameters---addstart"></a><span data-ttu-id="5b2b4-158">パラメーター - addStart</span><span class="sxs-lookup"><span data-stu-id="5b2b4-158">Parameters - addStart</span></span>

<span data-ttu-id="5b2b4-159">要素</span><span class="sxs-lookup"><span data-stu-id="5b2b4-159">element</span></span>  
<span data-ttu-id="5b2b4-160">リストの冒頭に追加する値。</span><span class="sxs-lookup"><span data-stu-id="5b2b4-160">The value to add to the start of the list.</span></span>

### <a name="return-value---addstart"></a><span data-ttu-id="5b2b4-161">戻り値 - addStart</span><span class="sxs-lookup"><span data-stu-id="5b2b4-161">Return Value - addStart</span></span>

<span data-ttu-id="5b2b4-162">このリストに追加される値。</span><span class="sxs-lookup"><span data-stu-id="5b2b4-162">The value added to the list.</span></span>

### <a name="remarks---addstart"></a><span data-ttu-id="5b2b4-163">備考 - addStart</span><span class="sxs-lookup"><span data-stu-id="5b2b4-163">Remarks - addStart</span></span>

<span data-ttu-id="5b2b4-164">要素は、List.addEnd メソッドを使用して、リストの最後に追加できます。</span><span class="sxs-lookup"><span data-stu-id="5b2b4-164">Elements can be added to the end of the list by using the List.addEnd method.</span></span>

### <a name="examples---addstart"></a><span data-ttu-id="5b2b4-165">例 - addStart</span><span class="sxs-lookup"><span data-stu-id="5b2b4-165">Examples - addStart</span></span>

<span data-ttu-id="5b2b4-166">次の例では、整数のリストを作成し、値の 1 と 2 をリストの末尾に追加し、値 3 をリストの先頭に追加します。</span><span class="sxs-lookup"><span data-stu-id="5b2b4-166">The following example creates a list of integers, adds the values 1 and 2 to the end of the list, and then adds the value 3 to the start of the list.</span></span> <span data-ttu-id="5b2b4-167">List.toString メソッドによって返される値は {3, 1, 2} です。</span><span class="sxs-lookup"><span data-stu-id="5b2b4-167">The values that are returned by the List.toString method are {3, 1, 2}.</span></span>

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

## <a name="method-definitionstring"></a><span data-ttu-id="5b2b4-168">メソッド definitionString</span><span class="sxs-lookup"><span data-stu-id="5b2b4-168">Method definitionString</span></span>

<span data-ttu-id="5b2b4-169">リスト内のすべての要素のタイプの説明を返します。</span><span class="sxs-lookup"><span data-stu-id="5b2b4-169">Returns a description of the type of the elements in the list.</span></span>

```xpp
public str definitionString()
```

### <a name="return-value---definitionstring"></a><span data-ttu-id="5b2b4-170">戻り値 - definitionString</span><span class="sxs-lookup"><span data-stu-id="5b2b4-170">Return Value - definitionString</span></span>

<span data-ttu-id="5b2b4-171">リストの定義を含む文字列。</span><span class="sxs-lookup"><span data-stu-id="5b2b4-171">A string that contains a definition of the list.</span></span>

### <a name="remarks---definitionstring"></a><span data-ttu-id="5b2b4-172">備考 - definitionString</span><span class="sxs-lookup"><span data-stu-id="5b2b4-172">Remarks - definitionString</span></span>

<span data-ttu-id="5b2b4-173">たとえば、このメソッドは、「int の一覧」を返すことができます。</span><span class="sxs-lookup"><span data-stu-id="5b2b4-173">For example, this method could return "list of int".</span></span> <span data-ttu-id="5b2b4-174">リスト内の値の一覧を印刷するには、List.toString メソッドを使用します。</span><span class="sxs-lookup"><span data-stu-id="5b2b4-174">To print a list of the values within the list, use the List.toString method.</span></span>

### <a name="examples---definitionstring"></a><span data-ttu-id="5b2b4-175">例 - definitionString</span><span class="sxs-lookup"><span data-stu-id="5b2b4-175">Examples - definitionString</span></span>

<span data-ttu-id="5b2b4-176">次の例では、整数のリストを作成します。</span><span class="sxs-lookup"><span data-stu-id="5b2b4-176">The following example creates a list of integers.</span></span> <span data-ttu-id="5b2b4-177">definitionString メソッドを使用して、リストの説明を出力します。</span><span class="sxs-lookup"><span data-stu-id="5b2b4-177">The definitionString method is used to print a description of the list.</span></span>

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

## <a name="method-elements"></a><span data-ttu-id="5b2b4-178">メソッド elements</span><span class="sxs-lookup"><span data-stu-id="5b2b4-178">Method elements</span></span>

<span data-ttu-id="5b2b4-179">リスト内の要素の数を指定します。</span><span class="sxs-lookup"><span data-stu-id="5b2b4-179">Specifies the number of elements in a list.</span></span>

```xpp
public int elements()
```

### <a name="return-value---elements"></a><span data-ttu-id="5b2b4-180">戻り値 - elements</span><span class="sxs-lookup"><span data-stu-id="5b2b4-180">Return Value - elements</span></span>

<span data-ttu-id="5b2b4-181">リスト内の要素の数。</span><span class="sxs-lookup"><span data-stu-id="5b2b4-181">The number of elements in the list.</span></span>

### <a name="examples---elements"></a><span data-ttu-id="5b2b4-182">例 - elements</span><span class="sxs-lookup"><span data-stu-id="5b2b4-182">Examples - elements</span></span>

<span data-ttu-id="5b2b4-183">次の例では、整数のリストを作成し、いくつかの要素を追加します。</span><span class="sxs-lookup"><span data-stu-id="5b2b4-183">The following example creates a list of integers and adds some elements to it.</span></span> <span data-ttu-id="5b2b4-184">要素メソッドは、リストに 3 つの要素があるかどうかをテストするために使用されます。</span><span class="sxs-lookup"><span data-stu-id="5b2b4-184">The elements method is used to test whether there are three elements in the list.</span></span>

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

## <a name="method-empty"></a><span data-ttu-id="5b2b4-185">メソッド empty</span><span class="sxs-lookup"><span data-stu-id="5b2b4-185">Method empty</span></span>

<span data-ttu-id="5b2b4-186">一覧が空であるかどうかを判定します。</span><span class="sxs-lookup"><span data-stu-id="5b2b4-186">Determines whether a list is empty.</span></span>

```xpp
public boolean empty()
```

### <a name="return-value---empty"></a><span data-ttu-id="5b2b4-187">戻り値 - empty</span><span class="sxs-lookup"><span data-stu-id="5b2b4-187">Return Value - empty</span></span>

<span data-ttu-id="5b2b4-188">リストが空の場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="5b2b4-188">true if the list is empty; otherwise, false.</span></span>

## <a name="method-equalto"></a><span data-ttu-id="5b2b4-189">メソッド equalTo</span><span class="sxs-lookup"><span data-stu-id="5b2b4-189">Method equalTo</span></span>

<span data-ttu-id="5b2b4-190">一覧が現在の一覧と同じかどうかを判定します。</span><span class="sxs-lookup"><span data-stu-id="5b2b4-190">Determines whether a list is the same as the current list.</span></span>

```xpp
public boolean equalTo(List l)
```

### <a name="parameters---equalto"></a><span data-ttu-id="5b2b4-191">パラメーター - equalTo</span><span class="sxs-lookup"><span data-stu-id="5b2b4-191">Parameters - equalTo</span></span>

<span data-ttu-id="5b2b4-192">l</span><span class="sxs-lookup"><span data-stu-id="5b2b4-192">l</span></span>  
<span data-ttu-id="5b2b4-193">現在のリストと比較されるリスト。</span><span class="sxs-lookup"><span data-stu-id="5b2b4-193">The list to be compared with the current list.</span></span>

### <a name="return-value---equalto"></a><span data-ttu-id="5b2b4-194">戻り値 - equalTo</span><span class="sxs-lookup"><span data-stu-id="5b2b4-194">Return Value - equalTo</span></span>

<span data-ttu-id="5b2b4-195">指定したリストが、メソッドが呼び出されたリストと同一である場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="5b2b4-195">true if the specified list is identical to the list on which the method is called; otherwise, false.</span></span>

### <a name="remarks---equalto"></a><span data-ttu-id="5b2b4-196">備考 - equalTo</span><span class="sxs-lookup"><span data-stu-id="5b2b4-196">Remarks - equalTo</span></span>

<span data-ttu-id="5b2b4-197">2 つのリストが同じ型の場合、リストは別のリストと等しくなり、要素の同じ番号を含み、同じ順序で要素が発生します。</span><span class="sxs-lookup"><span data-stu-id="5b2b4-197">A list is equal to another list if the two lists are the same type, contain the same number of elements, and the elements occur in the same order.</span></span> <span data-ttu-id="5b2b4-198">equalTo メソッドは、List.equal メソッドを使用するためのショートカットです。(this、l) と等しい。</span><span class="sxs-lookup"><span data-stu-id="5b2b4-198">The equalTo method is a shortcut for using the List.equal method: equal(this, l).</span></span>

## <a name="method-getenumerator"></a><span data-ttu-id="5b2b4-199">メソッド getEnumerator</span><span class="sxs-lookup"><span data-stu-id="5b2b4-199">Method getEnumerator</span></span>

<span data-ttu-id="5b2b4-200">リストのスキャンを可能にするリストの列挙子を作成します。</span><span class="sxs-lookup"><span data-stu-id="5b2b4-200">Creates an enumerator for a list which allows you to traverse the list.</span></span>

```xpp
public ListEnumerator getEnumerator()
```

### <a name="return-value---getenumerator"></a><span data-ttu-id="5b2b4-201">戻り値 - getEnumerator</span><span class="sxs-lookup"><span data-stu-id="5b2b4-201">Return Value - getEnumerator</span></span>

<span data-ttu-id="5b2b4-202">現在のリストの listEnumerator オブジェクト。</span><span class="sxs-lookup"><span data-stu-id="5b2b4-202">A listEnumerator object for the current list.</span></span>

## <a name="method-pack"></a><span data-ttu-id="5b2b4-203">メソッド pack</span><span class="sxs-lookup"><span data-stu-id="5b2b4-203">Method pack</span></span>

<span data-ttu-id="5b2b4-204">List クラスの現在のインスタンスをシリアル化します。</span><span class="sxs-lookup"><span data-stu-id="5b2b4-204">Serializes the current instance of the List class.</span></span>

```xpp
public container pack()
```

### <a name="return-value---pack"></a><span data-ttu-id="5b2b4-205">戻り値 - pack</span><span class="sxs-lookup"><span data-stu-id="5b2b4-205">Return Value - pack</span></span>

<span data-ttu-id="5b2b4-206">List クラスの現在のインスタンスを含むコンテナーです。</span><span class="sxs-lookup"><span data-stu-id="5b2b4-206">A container that contains the current instance of the List class.</span></span>

### <a name="remarks---pack"></a><span data-ttu-id="5b2b4-207">備考 - pack</span><span class="sxs-lookup"><span data-stu-id="5b2b4-207">Remarks - pack</span></span>

<span data-ttu-id="5b2b4-208">このメソッドで作成されたコンテナーには、リストの最初の要素の前に 3 つの要素が含まれます。</span><span class="sxs-lookup"><span data-stu-id="5b2b4-208">The container created by this method contains 3 elements before the first element from the list:</span></span>

-   <span data-ttu-id="5b2b4-209">コンテナのバージョン番号</span><span class="sxs-lookup"><span data-stu-id="5b2b4-209">A version number for the container</span></span>
-   <span data-ttu-id="5b2b4-210">リスト要素のデータ型を識別する整数</span><span class="sxs-lookup"><span data-stu-id="5b2b4-210">An integer that identifies the data type of the list elements</span></span>
-   <span data-ttu-id="5b2b4-211">リスト内の要素の数。</span><span class="sxs-lookup"><span data-stu-id="5b2b4-211">The number of elements in the list</span></span>

<span data-ttu-id="5b2b4-212">リスト内の要素がオブジェクトとなっている場合は、梱包は、各オブジェクトに対して pack メソッドを連続して呼び出し、サブコンテナーを取得することによって行われます。</span><span class="sxs-lookup"><span data-stu-id="5b2b4-212">If the elements in the list are objects, packing is performed by calling the pack method successively on each object to yield a subcontainer.</span></span> <span data-ttu-id="5b2b4-213">List.create メソッドを使用して、パックされたコンテナーからリストを取得できます。</span><span class="sxs-lookup"><span data-stu-id="5b2b4-213">The list can be retrieved from the packed container by using the List.create method.</span></span>

### <a name="examples---pack"></a><span data-ttu-id="5b2b4-214">例 - pack</span><span class="sxs-lookup"><span data-stu-id="5b2b4-214">Examples - pack</span></span>

<span data-ttu-id="5b2b4-215">次の例では、レコードのリストを作成し、新しい projReverseMarking オブジェクトを作成するためのパラメーターとしてパックされたリストに渡します。</span><span class="sxs-lookup"><span data-stu-id="5b2b4-215">The following example creates a list of records and passes in the packed list as a parameter for creating a new projReverseMarking object.</span></span>

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

## <a name="method-tostring"></a><span data-ttu-id="5b2b4-216">メソッド toString</span><span class="sxs-lookup"><span data-stu-id="5b2b4-216">Method toString</span></span>

<span data-ttu-id="5b2b4-217">リスト内の値の説明を返します。</span><span class="sxs-lookup"><span data-stu-id="5b2b4-217">Returns a description of the values in the list.</span></span>

```xpp
public str toString()
```

### <a name="return-value---tostring"></a><span data-ttu-id="5b2b4-218">戻り値 - toString</span><span class="sxs-lookup"><span data-stu-id="5b2b4-218">Return Value - toString</span></span>

<span data-ttu-id="5b2b4-219">リストの要素の値を説明する文字列。</span><span class="sxs-lookup"><span data-stu-id="5b2b4-219">A string that describes the values of the elements in the list.</span></span>

### <a name="remarks---tostring"></a><span data-ttu-id="5b2b4-220">備考 - toString</span><span class="sxs-lookup"><span data-stu-id="5b2b4-220">Remarks - toString</span></span>

<span data-ttu-id="5b2b4-221">リスト内の要素のタイプの説明を印刷するには、List.definitionString メソッドを使用します。</span><span class="sxs-lookup"><span data-stu-id="5b2b4-221">To print a description of the type of the elements in the list, use the List.definitionString method.</span></span>

### <a name="examples---tostring"></a><span data-ttu-id="5b2b4-222">例 - toString</span><span class="sxs-lookup"><span data-stu-id="5b2b4-222">Examples - toString</span></span>

<span data-ttu-id="5b2b4-223">次の例では、整数のリストを作成します。</span><span class="sxs-lookup"><span data-stu-id="5b2b4-223">The following example creates a list of integers.</span></span> <span data-ttu-id="5b2b4-224">toString メソッドを使用して、リストにある値の説明を出力します。</span><span class="sxs-lookup"><span data-stu-id="5b2b4-224">The toString method is used to print a description of the values in the list.</span></span>

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

## <a name="method-typeid"></a><span data-ttu-id="5b2b4-225">メソッド typeId</span><span class="sxs-lookup"><span data-stu-id="5b2b4-225">Method typeId</span></span>

<span data-ttu-id="5b2b4-226">リスト内の値のタイプを返します。</span><span class="sxs-lookup"><span data-stu-id="5b2b4-226">Returns the type of the values in a list.</span></span>

```xpp
public Types typeId()
```

### <a name="return-value---typeid"></a><span data-ttu-id="5b2b4-227">戻り値 - typeId</span><span class="sxs-lookup"><span data-stu-id="5b2b4-227">Return Value - typeId</span></span>

<span data-ttu-id="5b2b4-228">リスト要素のタイプ。</span><span class="sxs-lookup"><span data-stu-id="5b2b4-228">The type of the list elements.</span></span>

### <a name="remarks---typeid"></a><span data-ttu-id="5b2b4-229">備考 - typeId</span><span class="sxs-lookup"><span data-stu-id="5b2b4-229">Remarks - typeId</span></span>

<span data-ttu-id="5b2b4-230">リストのタイプは、リストが作成されるときに指定され、リストの存続期間中は同じままです。</span><span class="sxs-lookup"><span data-stu-id="5b2b4-230">The type of the list is specified when the list is created, and remains the same throughout the life of the list.</span></span>

## <a name="method-xml"></a><span data-ttu-id="5b2b4-231">メソッド xml</span><span class="sxs-lookup"><span data-stu-id="5b2b4-231">Method xml</span></span>

<span data-ttu-id="5b2b4-232">現在のオブジェクトを表す XML 文字列を返します。</span><span class="sxs-lookup"><span data-stu-id="5b2b4-232">Returns an XML string that represents the current object.</span></span>

```xpp
public str xml([int indent])
```

### <a name="parameters---xml"></a><span data-ttu-id="5b2b4-233">パラメーター - xml</span><span class="sxs-lookup"><span data-stu-id="5b2b4-233">Parameters - xml</span></span>

<span data-ttu-id="5b2b4-234">インデント</span><span class="sxs-lookup"><span data-stu-id="5b2b4-234">indent</span></span>  
<span data-ttu-id="5b2b4-235">返された XML 文字列のインデントの量 (省略可能)。</span><span class="sxs-lookup"><span data-stu-id="5b2b4-235">The amount of indentation of the returned XML string; optional.</span></span>

### <a name="return-value---xml"></a><span data-ttu-id="5b2b4-236">戻り値 - xml</span><span class="sxs-lookup"><span data-stu-id="5b2b4-236">Return Value - xml</span></span>

<span data-ttu-id="5b2b4-237">現在のオブジェクトを表す XML 文字列です。</span><span class="sxs-lookup"><span data-stu-id="5b2b4-237">An XML string that represents the current object.</span></span>

### <a name="remarks---xml"></a><span data-ttu-id="5b2b4-238">備考 - xml</span><span class="sxs-lookup"><span data-stu-id="5b2b4-238">Remarks - xml</span></span>

<span data-ttu-id="5b2b4-239">このメソッドをオーバーライドして、その型に対して意味のある値を返すことができます。</span><span class="sxs-lookup"><span data-stu-id="5b2b4-239">This method can be overridden to return values that are meaningful for that type.</span></span>

## <a name="method-create"></a><span data-ttu-id="5b2b4-240">メソッド create</span><span class="sxs-lookup"><span data-stu-id="5b2b4-240">Method create</span></span>

<span data-ttu-id="5b2b4-241">以前の List.pack メソッドの呼び出しで取得したコンテナーからリストを作成します。</span><span class="sxs-lookup"><span data-stu-id="5b2b4-241">Creates a list from the container obtained from a prior call to the List.pack method.</span></span>

```xpp
public static List create(container container)
```

### <a name="parameters---create"></a><span data-ttu-id="5b2b4-242">パラメーター - create</span><span class="sxs-lookup"><span data-stu-id="5b2b4-242">Parameters - create</span></span>

<span data-ttu-id="5b2b4-243">コンテナー</span><span class="sxs-lookup"><span data-stu-id="5b2b4-243">container</span></span>  
<span data-ttu-id="5b2b4-244">パックされたリストを保持するコンテナー。</span><span class="sxs-lookup"><span data-stu-id="5b2b4-244">The container that holds the packed list.</span></span>

### <a name="return-value---create"></a><span data-ttu-id="5b2b4-245">戻り値 - create</span><span class="sxs-lookup"><span data-stu-id="5b2b4-245">Return Value - create</span></span>

<span data-ttu-id="5b2b4-246">コンテナーに梱包されたものと同一のリスト。</span><span class="sxs-lookup"><span data-stu-id="5b2b4-246">A list identical to the one that was packed into the container.</span></span>

### <a name="examples---create"></a><span data-ttu-id="5b2b4-247">例 - create</span><span class="sxs-lookup"><span data-stu-id="5b2b4-247">Examples - create</span></span>

<span data-ttu-id="5b2b4-248">次の例では、リストを作成し、それをコンテナーにパックします。</span><span class="sxs-lookup"><span data-stu-id="5b2b4-248">The following example creates a list and packs it into a container.</span></span> <span data-ttu-id="5b2b4-249">次に、create メソッドを使用してコンテナーを展開し、元のリストと同じリストを作成します。</span><span class="sxs-lookup"><span data-stu-id="5b2b4-249">The create method is then used to unpack the container and create a list identical to the original one.</span></span>

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

## <a name="method-createfromxml"></a><span data-ttu-id="5b2b4-250">メソッド createFromXML</span><span class="sxs-lookup"><span data-stu-id="5b2b4-250">Method createFromXML</span></span>

```xpp
public static List createFromXML(Object xmlnode)
```

### <a name="parameters---createfromxml"></a><span data-ttu-id="5b2b4-251">パラメーター - createFromXML</span><span class="sxs-lookup"><span data-stu-id="5b2b4-251">Parameters - createFromXML</span></span>

<span data-ttu-id="5b2b4-252">xmlnode</span><span class="sxs-lookup"><span data-stu-id="5b2b4-252">xmlnode</span></span>  

### <a name="return-value---createfromxml"></a><span data-ttu-id="5b2b4-253">戻り値 - createFromXML</span><span class="sxs-lookup"><span data-stu-id="5b2b4-253">Return Value - createFromXML</span></span>

## <a name="method-equal"></a><span data-ttu-id="5b2b4-254">メソッド equal</span><span class="sxs-lookup"><span data-stu-id="5b2b4-254">Method equal</span></span>

<span data-ttu-id="5b2b4-255">2 つのリストが同じかどうかを判定します。</span><span class="sxs-lookup"><span data-stu-id="5b2b4-255">Determines whether two lists are identical.</span></span>

```xpp
public static boolean equal(List list1, List list2)
```

### <a name="parameters---equal"></a><span data-ttu-id="5b2b4-256">パラメーター - equal</span><span class="sxs-lookup"><span data-stu-id="5b2b4-256">Parameters - equal</span></span>

<span data-ttu-id="5b2b4-257">list1</span><span class="sxs-lookup"><span data-stu-id="5b2b4-257">list1</span></span>  
<span data-ttu-id="5b2b4-258">比較する 2 番目のリスト。</span><span class="sxs-lookup"><span data-stu-id="5b2b4-258">The second list to be compared.</span></span>

<!-- -->

<span data-ttu-id="5b2b4-259">list2</span><span class="sxs-lookup"><span data-stu-id="5b2b4-259">list2</span></span>  
<span data-ttu-id="5b2b4-260">比較する 2 番目のリスト。</span><span class="sxs-lookup"><span data-stu-id="5b2b4-260">The second list to be compared.</span></span>

### <a name="return-value---equal"></a><span data-ttu-id="5b2b4-261">戻り値 - equal</span><span class="sxs-lookup"><span data-stu-id="5b2b4-261">Return Value - equal</span></span>

<span data-ttu-id="5b2b4-262">2 つのリストが同一である場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="5b2b4-262">true if the two lists are identical; otherwise, false.</span></span>

### <a name="remarks---equal"></a><span data-ttu-id="5b2b4-263">備考 - equal</span><span class="sxs-lookup"><span data-stu-id="5b2b4-263">Remarks - equal</span></span>

<span data-ttu-id="5b2b4-264">2 つのリストが同じ型の場合、リストは別のリストと等しくなり、要素の同じ番号を含み、同じ順序で要素が発生します。</span><span class="sxs-lookup"><span data-stu-id="5b2b4-264">A list is equal to another list if the two lists are the same type, contain the same number of elements, and the elements occur in the same order.</span></span>

## <a name="method-merge"></a><span data-ttu-id="5b2b4-265">メソッド merge</span><span class="sxs-lookup"><span data-stu-id="5b2b4-265">Method merge</span></span>

<span data-ttu-id="5b2b4-266">2 つのリストを組み合わせ、新しいリストを作成します。</span><span class="sxs-lookup"><span data-stu-id="5b2b4-266">Combines two lists to create a new list.</span></span>

```xpp
public static List merge(List list1, List list2)
```

### <a name="parameters---merge"></a><span data-ttu-id="5b2b4-267">パラメーター - merge</span><span class="sxs-lookup"><span data-stu-id="5b2b4-267">Parameters - merge</span></span>

<span data-ttu-id="5b2b4-268">list1</span><span class="sxs-lookup"><span data-stu-id="5b2b4-268">list1</span></span>  
<span data-ttu-id="5b2b4-269">新しいリストを作成するために最初のリストの最後に追加されるリスト。</span><span class="sxs-lookup"><span data-stu-id="5b2b4-269">The list that will be added to the end of the first to create the new list.</span></span>

<!-- -->

<span data-ttu-id="5b2b4-270">list2</span><span class="sxs-lookup"><span data-stu-id="5b2b4-270">list2</span></span>  
<span data-ttu-id="5b2b4-271">新しいリストを作成するために最初のリストの最後に追加されるリスト。</span><span class="sxs-lookup"><span data-stu-id="5b2b4-271">The list that will be added to the end of the first to create the new list.</span></span>

### <a name="return-value---merge"></a><span data-ttu-id="5b2b4-272">戻り値 - merge</span><span class="sxs-lookup"><span data-stu-id="5b2b4-272">Return Value - merge</span></span>

<span data-ttu-id="5b2b4-273">新しいリスト。</span><span class="sxs-lookup"><span data-stu-id="5b2b4-273">The new list.</span></span>

### <a name="remarks---merge"></a><span data-ttu-id="5b2b4-274">備考 - merge</span><span class="sxs-lookup"><span data-stu-id="5b2b4-274">Remarks - merge</span></span>

<span data-ttu-id="5b2b4-275">リストのタイプは同じにする必要があります。</span><span class="sxs-lookup"><span data-stu-id="5b2b4-275">The types of the lists must be the same.</span></span>

### <a name="examples---merge"></a><span data-ttu-id="5b2b4-276">例 - merge</span><span class="sxs-lookup"><span data-stu-id="5b2b4-276">Examples - merge</span></span>

<span data-ttu-id="5b2b4-277">次の例では、2 つの整数値のリストを作成し、それらをマージして新しいリストを作成し、新しい組み合わせリストに値を出力します。</span><span class="sxs-lookup"><span data-stu-id="5b2b4-277">The following example creates two lists of integer values, merges them to create a new list, and then prints out the values in the new combined list.</span></span>

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

## <a name="method-appendlist"></a><span data-ttu-id="5b2b4-278">メソッド appendList</span><span class="sxs-lookup"><span data-stu-id="5b2b4-278">Method appendList</span></span>

```xpp
public void appendList(List list)
```

### <a name="parameters---appendlist"></a><span data-ttu-id="5b2b4-279">パラメーター - appendList</span><span class="sxs-lookup"><span data-stu-id="5b2b4-279">Parameters - appendList</span></span>

<span data-ttu-id="5b2b4-280">リスト</span><span class="sxs-lookup"><span data-stu-id="5b2b4-280">list</span></span>  

## <a name="method-new"></a><span data-ttu-id="5b2b4-281">メソッド new</span><span class="sxs-lookup"><span data-stu-id="5b2b4-281">Method new</span></span>

<span data-ttu-id="5b2b4-282">リストを作成します。</span><span class="sxs-lookup"><span data-stu-id="5b2b4-282">Creates a list.</span></span>

```xpp
public void new(Types Type)
```

### <a name="parameters---new"></a><span data-ttu-id="5b2b4-283">パラメーター - new</span><span class="sxs-lookup"><span data-stu-id="5b2b4-283">Parameters - new</span></span>

<span data-ttu-id="5b2b4-284">種類</span><span class="sxs-lookup"><span data-stu-id="5b2b4-284">Type</span></span>  
<span data-ttu-id="5b2b4-285">リスト内の要素が持つべきタイプ。</span><span class="sxs-lookup"><span data-stu-id="5b2b4-285">The type that the elements in the list should have.</span></span>

### <a name="remarks---new"></a><span data-ttu-id="5b2b4-286">備考 - new</span><span class="sxs-lookup"><span data-stu-id="5b2b4-286">Remarks - new</span></span>

<span data-ttu-id="5b2b4-287">Type パラメーターの使用可能な値は、Type システム列挙によって提供されます。</span><span class="sxs-lookup"><span data-stu-id="5b2b4-287">The possible values for the Type parameter are supplied by the Types system enum.</span></span> <span data-ttu-id="5b2b4-288">リストを作成した後、そのリストに含まれている要素のタイプを変更することはできません。</span><span class="sxs-lookup"><span data-stu-id="5b2b4-288">After you have created a list, you cannot change the type of the elements it contains.</span></span>

### <a name="examples---new"></a><span data-ttu-id="5b2b4-289">例 - new</span><span class="sxs-lookup"><span data-stu-id="5b2b4-289">Examples - new</span></span>

<span data-ttu-id="5b2b4-290">次の例では、文字列のリストを作成します。</span><span class="sxs-lookup"><span data-stu-id="5b2b4-290">The following example creates a list of strings.</span></span>

```xpp
{ 
    // Creates a list of integers. 
    List il = new List(Types::String); 
}
```

