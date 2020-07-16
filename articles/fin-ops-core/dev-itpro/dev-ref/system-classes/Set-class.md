---
title: Set クラス
description: このトピックでは、Set クラスについて説明します。
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
ms.openlocfilehash: b2ada346c1917d3efcb04b9c6018111661843e0c
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502805"
---
# <a name="class-set"></a><span data-ttu-id="156e4-103">クラスのセット</span><span class="sxs-lookup"><span data-stu-id="156e4-103">Class Set</span></span>

[!include [banner](../../includes/banner.md)]

```xpp
class Set extends Object
```

<span data-ttu-id="156e4-104">Set クラスは、格納されている要素の値が固有であり、自動的に並べ替えられるデータに応じたキー値として機能するコレクションからデータを格納して取得ために使用されます。</span><span class="sxs-lookup"><span data-stu-id="156e4-104">The Set class is used for the storage and retrieval of data from a collection in which the values of the elements contained are unique and serve as the key values according to which the data is automatically ordered.</span></span>

## <a name="remarks"></a><span data-ttu-id="156e4-105">備考</span><span class="sxs-lookup"><span data-stu-id="156e4-105">Remarks</span></span>

<span data-ttu-id="156e4-106">値は任意の X++ 型にできます。</span><span class="sxs-lookup"><span data-stu-id="156e4-106">The values may be of any X++ type.</span></span> <span data-ttu-id="156e4-107">セット内のすべての値には同じタイプが必要です。</span><span class="sxs-lookup"><span data-stu-id="156e4-107">All values in the set must have the same type.</span></span> <span data-ttu-id="156e4-108">セットにすでに保存されている値が追加されると、その値は無視され、セット内の要素の数を増加させません。</span><span class="sxs-lookup"><span data-stu-id="156e4-108">When a value that is already stored in the set is added, it is ignored and does not increase the number of elements in the set.</span></span> <span data-ttu-id="156e4-109">セットに格納された値は、SetEnumerator 型のオブジェクトを使用してスキャンできます。</span><span class="sxs-lookup"><span data-stu-id="156e4-109">The values stored in the set can be traversed by using objects of type SetEnumerator.</span></span> <span data-ttu-id="156e4-110">セットのコンテンツは、要素の効率的な検索を容易にする方法で格納されます。</span><span class="sxs-lookup"><span data-stu-id="156e4-110">The contents of a set are stored in a way that facilitates efficient look up of the elements.</span></span>

## <a name="examples"></a><span data-ttu-id="156e4-111">例</span><span class="sxs-lookup"><span data-stu-id="156e4-111">Examples</span></span>

<span data-ttu-id="156e4-112">次の例では、noConfigs セットのいずれかの値が 2 番目のセットの yesConfigs セットに含まれているかどうかを確認します。</span><span class="sxs-lookup"><span data-stu-id="156e4-112">The following example checks whether any of the values in one set, the noConfigs set, are found in a second set, the yesConfigs set.</span></span> <span data-ttu-id="156e4-113">見つかった場合は、yesConfigs セットから削除されます。</span><span class="sxs-lookup"><span data-stu-id="156e4-113">If they are, they are removed from the yesConfigs set.</span></span>

```xpp
Set             noConfigs; 
Set             yesConfigs; 
ConfigId        configId; 
SetEnumerator   se; 
; 
se = noConfigs.getEnumerator(); 
while (se.moveNext()) 
{ 
    configId    = se.current(); 
    if (yesConfigs.in(configId)) 
    { 
        yesConfigs.remove(configId); 
    } 
}
```

## <a name="methods"></a><span data-ttu-id="156e4-114">メソッド</span><span class="sxs-lookup"><span data-stu-id="156e4-114">Methods</span></span>

| <span data-ttu-id="156e4-115">方法</span><span class="sxs-lookup"><span data-stu-id="156e4-115">Method</span></span>                                               | <span data-ttu-id="156e4-116">説明</span><span class="sxs-lookup"><span data-stu-id="156e4-116">Description</span></span>                                                                                                                       |
|------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="156e4-117">public boolean add(AnyType arg)</span><span class="sxs-lookup"><span data-stu-id="156e4-117">public boolean add(AnyType arg)</span></span>                      | <span data-ttu-id="156e4-118">セットに要素を追加します。</span><span class="sxs-lookup"><span data-stu-id="156e4-118">Adds an element to the set.</span></span>                                                                                                       |
| <span data-ttu-id="156e4-119">public str definitionString()</span><span class="sxs-lookup"><span data-stu-id="156e4-119">public str definitionString()</span></span>                        | <span data-ttu-id="156e4-120">セット内のすべての要素のタイプの説明を返します。</span><span class="sxs-lookup"><span data-stu-id="156e4-120">Returns a description of the type of the elements in the set.</span></span>                                                                     |
| <span data-ttu-id="156e4-121">public int elements()</span><span class="sxs-lookup"><span data-stu-id="156e4-121">public int elements()</span></span>                                | <span data-ttu-id="156e4-122">セット内の要素の数を返します。</span><span class="sxs-lookup"><span data-stu-id="156e4-122">Returns the number of elements in the set.</span></span>                                                                                        |
| <span data-ttu-id="156e4-123">public boolean empty()</span><span class="sxs-lookup"><span data-stu-id="156e4-123">public boolean empty()</span></span>                               | <span data-ttu-id="156e4-124">セットが空であるかどうかを判定します。</span><span class="sxs-lookup"><span data-stu-id="156e4-124">Determines whether the set is empty.</span></span>                                                                                              |
| <span data-ttu-id="156e4-125">public boolean equal(Set set)</span><span class="sxs-lookup"><span data-stu-id="156e4-125">public boolean equal(Set set)</span></span>                        | <span data-ttu-id="156e4-126">セットが現在のセットと同一かどうかを判定します。</span><span class="sxs-lookup"><span data-stu-id="156e4-126">Determines whether a set is identical to the current set.</span></span>                                                                         |
| <span data-ttu-id="156e4-127">public SetEnumerator getEnumerator()</span><span class="sxs-lookup"><span data-stu-id="156e4-127">public SetEnumerator getEnumerator()</span></span>                 | <span data-ttu-id="156e4-128">セット内のスキャンを可能にする、セットの列挙子を作成します。</span><span class="sxs-lookup"><span data-stu-id="156e4-128">Creates an enumerator for a set, which allows you to traverse the set.</span></span>                                                            |
| <span data-ttu-id="156e4-129">public boolean in(AnyType arg)</span><span class="sxs-lookup"><span data-stu-id="156e4-129">public boolean in(AnyType arg)</span></span>                       | <span data-ttu-id="156e4-130">指定された要素がセットのメンバーであるかどうかを判定します。</span><span class="sxs-lookup"><span data-stu-id="156e4-130">Determines whether a specified element is a member of the set.</span></span>                                                                    |
| <span data-ttu-id="156e4-131">public container pack()</span><span class="sxs-lookup"><span data-stu-id="156e4-131">public container pack()</span></span>                              | <span data-ttu-id="156e4-132">Set クラスの現在のインスタンスをシリアル化します。</span><span class="sxs-lookup"><span data-stu-id="156e4-132">Serializes the current instance of the Set class.</span></span>                                                                                 |
| <span data-ttu-id="156e4-133">public boolean remove(AnyType arg)</span><span class="sxs-lookup"><span data-stu-id="156e4-133">public boolean remove(AnyType arg)</span></span>                   | <span data-ttu-id="156e4-134">セットから要素を削除します。</span><span class="sxs-lookup"><span data-stu-id="156e4-134">Removes an element from the set.</span></span>                                                                                                  |
| <span data-ttu-id="156e4-135">public str toString()</span><span class="sxs-lookup"><span data-stu-id="156e4-135">public str toString()</span></span>                                | <span data-ttu-id="156e4-136">設定の内容を説明する文字列を返します。</span><span class="sxs-lookup"><span data-stu-id="156e4-136">Returns a string describing the contents of the set.</span></span>                                                                              |
| <span data-ttu-id="156e4-137">public Types typeId()</span><span class="sxs-lookup"><span data-stu-id="156e4-137">public Types typeId()</span></span>                                | <span data-ttu-id="156e4-138">セット内の値のタイプを返します。</span><span class="sxs-lookup"><span data-stu-id="156e4-138">Returns the type of the values in the set.</span></span>                                                                                        |
| <span data-ttu-id="156e4-139">public str xml(\[int indent\])</span><span class="sxs-lookup"><span data-stu-id="156e4-139">public str xml(\[int indent\])</span></span>                       | <span data-ttu-id="156e4-140">現在のオブジェクトを表す XML 文字列を返します。</span><span class="sxs-lookup"><span data-stu-id="156e4-140">Returns an XML string that represents the current object.</span></span>                                                                         |
| <span data-ttu-id="156e4-141">::public static Set create(container container)</span><span class="sxs-lookup"><span data-stu-id="156e4-141">::public static Set create(container container)</span></span>      | <span data-ttu-id="156e4-142">以前の Set.pack メソッドの呼び出しで取得したコンテナーからセットを作成します。</span><span class="sxs-lookup"><span data-stu-id="156e4-142">Creates a set from the container obtained from a prior call to the Set.pack method.</span></span>                                               |
| <span data-ttu-id="156e4-143">::public static Set createFromXML(Object xmlnode)</span><span class="sxs-lookup"><span data-stu-id="156e4-143">::public static Set createFromXML(Object xmlnode)</span></span>    |                                                                                                                                   |
| <span data-ttu-id="156e4-144">::public static Set difference(Set set1, Set set2)</span><span class="sxs-lookup"><span data-stu-id="156e4-144">::public static Set difference(Set set1, Set set2)</span></span>   | <span data-ttu-id="156e4-145">set2 で検出されない set1 の要素を含むセットを計算および取得します。</span><span class="sxs-lookup"><span data-stu-id="156e4-145">Calculates and retrieves the set containing the elements from set1 that are not found in set2.</span></span>                                    |
| <span data-ttu-id="156e4-146">::public static Set intersection(Set set1, Set set2)</span><span class="sxs-lookup"><span data-stu-id="156e4-146">::public static Set intersection(Set set1, Set set2)</span></span> | <span data-ttu-id="156e4-147">2 つのセット内で検出される同一の値を計算して返します。</span><span class="sxs-lookup"><span data-stu-id="156e4-147">Calculates and returns the identical values found in two sets.</span></span>                                                                    |
| <span data-ttu-id="156e4-148">::public static Set union(Set set1, Set set2)</span><span class="sxs-lookup"><span data-stu-id="156e4-148">::public static Set union(Set set1, Set set2)</span></span>        | <span data-ttu-id="156e4-149">指定された 2 つのセットの和集合を計算および取得します</span><span class="sxs-lookup"><span data-stu-id="156e4-149">Calculates and retrieves the union of two given sets.</span></span> <span data-ttu-id="156e4-150">これは、少なくとも 1 つのセットにある値を含むセットです。</span><span class="sxs-lookup"><span data-stu-id="156e4-150">This is the set that contains the values found in at least one of the sets.</span></span> |
| <span data-ttu-id="156e4-151">public void new(Types Type)</span><span class="sxs-lookup"><span data-stu-id="156e4-151">public void new(Types Type)</span></span>                          | <span data-ttu-id="156e4-152">指定した型の要素を含めることができるセットを作成します。</span><span class="sxs-lookup"><span data-stu-id="156e4-152">Creates a set that can contain elements of the specified type.</span></span>                                                                    |

## <a name="method-add"></a><span data-ttu-id="156e4-153">メソッド add</span><span class="sxs-lookup"><span data-stu-id="156e4-153">Method add</span></span>

<span data-ttu-id="156e4-154">セットに要素を追加します。</span><span class="sxs-lookup"><span data-stu-id="156e4-154">Adds an element to the set.</span></span>

```xpp
public boolean add(AnyType arg)
```

### <a name="parameters---add"></a><span data-ttu-id="156e4-155">パラメーター - add</span><span class="sxs-lookup"><span data-stu-id="156e4-155">Parameters - add</span></span>

<span data-ttu-id="156e4-156">arg</span><span class="sxs-lookup"><span data-stu-id="156e4-156">arg</span></span>  
<span data-ttu-id="156e4-157">セットに追加する要素。</span><span class="sxs-lookup"><span data-stu-id="156e4-157">The element to add to the set.</span></span>

### <a name="return-value---add"></a><span data-ttu-id="156e4-158">戻り値 - add</span><span class="sxs-lookup"><span data-stu-id="156e4-158">Return Value - add</span></span>

<span data-ttu-id="156e4-159">要素がセットに追加された場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="156e4-159">true if the element is added to the set; otherwise, false.</span></span>

### <a name="remarks---add"></a><span data-ttu-id="156e4-160">備考 - add</span><span class="sxs-lookup"><span data-stu-id="156e4-160">Remarks - add</span></span>

<span data-ttu-id="156e4-161">セットに追加される要素は、セットの作成時にセットに割り当てられたタイプと同じタイプでなければなりません。</span><span class="sxs-lookup"><span data-stu-id="156e4-161">The element added to a set must be of the same type as the type assigned to the set when it was created.</span></span> <span data-ttu-id="156e4-162">既にセットに存在する場合、要素は追加されません。</span><span class="sxs-lookup"><span data-stu-id="156e4-162">An element will not be added if it already exists in the set.</span></span>

### <a name="examples---add"></a><span data-ttu-id="156e4-163">例 - add</span><span class="sxs-lookup"><span data-stu-id="156e4-163">Examples - add</span></span>

<span data-ttu-id="156e4-164">次の例では、セットを作成し、いくつかの整数を追加してから、セットの内容を出力します。</span><span class="sxs-lookup"><span data-stu-id="156e4-164">The following example creates a set, adds some integers to it, and then prints out the contents of the set.</span></span>

```xpp
{ 
    // Create a set of integers 
    Set is = new Set (Types::Integer); 
    int i; 
    ;  
    // Add values 0 to 9 to the set 
    for (i = 0; i < 10; i++) 
    { 
        is.add(i); 
    } 
    print is.toString(); 
    pause; 
}
```

## <a name="method-definitionstring"></a><span data-ttu-id="156e4-165">メソッド definitionString</span><span class="sxs-lookup"><span data-stu-id="156e4-165">Method definitionString</span></span>

<span data-ttu-id="156e4-166">セット内のすべての要素のタイプの説明を返します。</span><span class="sxs-lookup"><span data-stu-id="156e4-166">Returns a description of the type of the elements in the set.</span></span>

```xpp
public str definitionString()
```

### <a name="return-value---definitionstring"></a><span data-ttu-id="156e4-167">戻り値 - definitionString</span><span class="sxs-lookup"><span data-stu-id="156e4-167">Return Value - definitionString</span></span>

<span data-ttu-id="156e4-168">設定の定義を含む文字列。</span><span class="sxs-lookup"><span data-stu-id="156e4-168">A string that contains a definition of the set.</span></span>

### <a name="remarks---definitionstring"></a><span data-ttu-id="156e4-169">備考 - definitionString</span><span class="sxs-lookup"><span data-stu-id="156e4-169">Remarks - definitionString</span></span>

<span data-ttu-id="156e4-170">セット内の値の一覧を印刷するには、Set.toString を使用します。</span><span class="sxs-lookup"><span data-stu-id="156e4-170">To print a list of the values within the set, use Set.toString.</span></span>

### <a name="examples---definitionstring"></a><span data-ttu-id="156e4-171">例 - definitionString</span><span class="sxs-lookup"><span data-stu-id="156e4-171">Examples - definitionString</span></span>

<span data-ttu-id="156e4-172">次の例では、整数のセットを作成します。</span><span class="sxs-lookup"><span data-stu-id="156e4-172">The following example creates a set of integers.</span></span> <span data-ttu-id="156e4-173">definitionString メソッドを使用して、セットの説明を出力します。</span><span class="sxs-lookup"><span data-stu-id="156e4-173">The definitionString method is used to print a description of the set.</span></span>

```xpp
{ 
    // Declare a set of integers 
    Set is = new Set (Types::Integer);  
    ; 
    // Add some integers to the set 
    print is.add(1); 
    print is.add(2); 
    print is.add(1); 
    // Print a description of the set 
    print is.definitionString(); 
    // Print a description of the set elements 
    print is.toString(); 
    pause; 
}
```

## <a name="method-elements"></a><span data-ttu-id="156e4-174">メソッド elements</span><span class="sxs-lookup"><span data-stu-id="156e4-174">Method elements</span></span>

<span data-ttu-id="156e4-175">セット内の要素の数を返します。</span><span class="sxs-lookup"><span data-stu-id="156e4-175">Returns the number of elements in the set.</span></span>

```xpp
public int elements()
```

### <a name="return-value---elements"></a><span data-ttu-id="156e4-176">戻り値 - elements</span><span class="sxs-lookup"><span data-stu-id="156e4-176">Return Value - elements</span></span>

<span data-ttu-id="156e4-177">セット内の要素の数。</span><span class="sxs-lookup"><span data-stu-id="156e4-177">The number of elements in the set.</span></span>

### <a name="examples---elements"></a><span data-ttu-id="156e4-178">例 - elements</span><span class="sxs-lookup"><span data-stu-id="156e4-178">Examples - elements</span></span>

<span data-ttu-id="156e4-179">次の例では、セットの内容をコンテナーにパックします。</span><span class="sxs-lookup"><span data-stu-id="156e4-179">The following example packs the contents of a set into a container.</span></span> <span data-ttu-id="156e4-180">要素メソッドは、セットに任意のコンテンツが含まれているかどうかをテストするために使用されます。</span><span class="sxs-lookup"><span data-stu-id="156e4-180">The elements method is used to test whether the set has any contents.</span></span> <span data-ttu-id="156e4-181">コンテンツがない場合は、nullNothingnullptrunita null 参照 (Visual Basic ではなしになる) コンテナーが返されます。</span><span class="sxs-lookup"><span data-stu-id="156e4-181">If there are no contents, a nullNothingnullptrunita null reference (Nothing in Visual Basic) container is returned.</span></span>

```xpp
public static container intSet2Con(Set _intSet) 
{ 
    SetEnumerator se; 
    container     intCon; 
    ; 
    if (!_intSet || !_intSet.elements()) 
    { 
        return conNull(); 
    } 
    se = _intSet.getEnumerator(); 
    while (se.moveNext()) 
    { 
        intCon += se.current(); 
    } 
    return intCon; 
}
```

## <a name="method-empty"></a><span data-ttu-id="156e4-182">メソッド empty</span><span class="sxs-lookup"><span data-stu-id="156e4-182">Method empty</span></span>

<span data-ttu-id="156e4-183">セットが空であるかどうかを判定します。</span><span class="sxs-lookup"><span data-stu-id="156e4-183">Determines whether the set is empty.</span></span>

```xpp
public boolean empty()
```

### <a name="return-value---empty"></a><span data-ttu-id="156e4-184">戻り値 - empty</span><span class="sxs-lookup"><span data-stu-id="156e4-184">Return Value - empty</span></span>

<span data-ttu-id="156e4-185">セットが空の場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="156e4-185">true if the set is empty; otherwise, false.</span></span>

### <a name="remarks---empty"></a><span data-ttu-id="156e4-186">備考 - empty</span><span class="sxs-lookup"><span data-stu-id="156e4-186">Remarks - empty</span></span>

<span data-ttu-id="156e4-187">これは、(elements() == 0) と等価です。</span><span class="sxs-lookup"><span data-stu-id="156e4-187">This is equivalent to (elements() == 0).</span></span>

### <a name="examples---empty"></a><span data-ttu-id="156e4-188">例 - empty</span><span class="sxs-lookup"><span data-stu-id="156e4-188">Examples - empty</span></span>

<span data-ttu-id="156e4-189">次の例では、セットに要素があるかどうかをテストします。</span><span class="sxs-lookup"><span data-stu-id="156e4-189">The following example tests whether there are any elements in a set.</span></span>

```xpp
{ 
    Set mySet = new Set(Types::Integer); 
    ; 
    // ... 
    if (mySet.empty()) 
    { 
        print "There are no values in the set"; 
    } 
}
```

## <a name="method-equal"></a><span data-ttu-id="156e4-190">メソッド equal</span><span class="sxs-lookup"><span data-stu-id="156e4-190">Method equal</span></span>

<span data-ttu-id="156e4-191">セットが現在のセットと同一かどうかを判定します。</span><span class="sxs-lookup"><span data-stu-id="156e4-191">Determines whether a set is identical to the current set.</span></span>

```xpp
public boolean equal(Set set)
```

### <a name="parameters---equal"></a><span data-ttu-id="156e4-192">パラメーター - equal</span><span class="sxs-lookup"><span data-stu-id="156e4-192">Parameters - equal</span></span>

<span data-ttu-id="156e4-193">set</span><span class="sxs-lookup"><span data-stu-id="156e4-193">set</span></span>  
<span data-ttu-id="156e4-194">現在のセットと比較されるセット。</span><span class="sxs-lookup"><span data-stu-id="156e4-194">The set to be compared with the current set.</span></span>

### <a name="return-value---equal"></a><span data-ttu-id="156e4-195">戻り値 - equal</span><span class="sxs-lookup"><span data-stu-id="156e4-195">Return Value - equal</span></span>

<span data-ttu-id="156e4-196">そのセットが現在のセットと同じである場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="156e4-196">true if the set is the same as the current set; otherwise, false.</span></span>

### <a name="remarks---equal"></a><span data-ttu-id="156e4-197">備考 - equal</span><span class="sxs-lookup"><span data-stu-id="156e4-197">Remarks - equal</span></span>

<span data-ttu-id="156e4-198">2 つのセットが等しくなるためには、それらには同じタイプおよび同じ数の要素があり、すべての要素は同じである必要があります。</span><span class="sxs-lookup"><span data-stu-id="156e4-198">For two sets to be equal, they must have the same type and the same number of elements, and all elements must be the same.</span></span>

### <a name="examples---equal"></a><span data-ttu-id="156e4-199">例 - equal</span><span class="sxs-lookup"><span data-stu-id="156e4-199">Examples - equal</span></span>

<span data-ttu-id="156e4-200">次の例では、2 つの整数セットを作成し、それらにいくつかの値を追加し、それらを比較してセットが同じかどうかを確認します。</span><span class="sxs-lookup"><span data-stu-id="156e4-200">The following example creates two sets of integers, adds some values to them, and then compares them to see whether the sets are the same.</span></span>

```xpp
{ 
    Set is1 = new Set (Types::Integer); 
    Set is2 = new Set (Types::Integer); 
    ; 
    is1.add(1); 
    is1.add(2); 
    is1.add(3); 
    is2.add(2); 
    is2.add(4); 
    if (is1.equal(is2)) 
    { 
        print "The sets are equal"; 
        pause; 
    } 
    else 
    { 
         print "The sets are not equal"; 
         pause; 
     } 
}
```

## <a name="method-getenumerator"></a><span data-ttu-id="156e4-201">メソッド getEnumerator</span><span class="sxs-lookup"><span data-stu-id="156e4-201">Method getEnumerator</span></span>

<span data-ttu-id="156e4-202">セット内のスキャンを可能にする、セットの列挙子を作成します。</span><span class="sxs-lookup"><span data-stu-id="156e4-202">Creates an enumerator for a set, which allows you to traverse the set.</span></span>

```xpp
public SetEnumerator getEnumerator()
```

### <a name="return-value---getenumerator"></a><span data-ttu-id="156e4-203">戻り値 - getEnumerator</span><span class="sxs-lookup"><span data-stu-id="156e4-203">Return Value - getEnumerator</span></span>

<span data-ttu-id="156e4-204">現在のセットの SetEnumerator オブジェクト。</span><span class="sxs-lookup"><span data-stu-id="156e4-204">A SetEnumerator object for the current set.</span></span>

### <a name="examples---getenumerator"></a><span data-ttu-id="156e4-205">例 - getEnumerator</span><span class="sxs-lookup"><span data-stu-id="156e4-205">Examples - getEnumerator</span></span>

<span data-ttu-id="156e4-206">次の例では、セットの内容をコンテナーにパックします。</span><span class="sxs-lookup"><span data-stu-id="156e4-206">The following example packs the contents of a set into a container.</span></span> <span data-ttu-id="156e4-207">getEnumerator メソッドは、セットの列挙子を作成するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="156e4-207">The getEnumerator method is used to create an enumerator for the set.</span></span> <span data-ttu-id="156e4-208">したがって、セット内の要素を横断してコンテナーに追加することができます。</span><span class="sxs-lookup"><span data-stu-id="156e4-208">Therefore, that the elements in the set can be traversed and added to the container.</span></span>

```xpp
public static container intSet2Con(Set _intSet) 
{ 
    SetEnumerator se; 
    container     intCon; 
    ; 
    if (!_intSet || !_intSet.elements()) 
    { 
        return conNull(); 
    } 
    se = _intSet.getEnumerator(); 
    while (se.moveNext()) 
    { 
        intCon += se.current(); 
    } 
    return intCon; 
}
```

## <a name="method-in"></a><span data-ttu-id="156e4-209">メソッド in</span><span class="sxs-lookup"><span data-stu-id="156e4-209">Method in</span></span>

<span data-ttu-id="156e4-210">指定された要素がセットのメンバーであるかどうかを判定します。</span><span class="sxs-lookup"><span data-stu-id="156e4-210">Determines whether a specified element is a member of the set.</span></span>

```xpp
public boolean in(AnyType arg)
```

### <a name="parameters---in"></a><span data-ttu-id="156e4-211">パラメーター - in</span><span class="sxs-lookup"><span data-stu-id="156e4-211">Parameters - in</span></span>

<span data-ttu-id="156e4-212">arg</span><span class="sxs-lookup"><span data-stu-id="156e4-212">arg</span></span>  
<span data-ttu-id="156e4-213">チェックする要素。</span><span class="sxs-lookup"><span data-stu-id="156e4-213">The element to check.</span></span> <span data-ttu-id="156e4-214">要素のタイプは、セットの指定されたタイプと同じである必要があります。</span><span class="sxs-lookup"><span data-stu-id="156e4-214">The type of the element must be the same as the type that was specified for the set.</span></span>

### <a name="return-value---in"></a><span data-ttu-id="156e4-215">戻り値 - in</span><span class="sxs-lookup"><span data-stu-id="156e4-215">Return Value - in</span></span>

<span data-ttu-id="156e4-216">指定した要素がセット内で見つかる場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="156e4-216">true if the specified element is found in the set; otherwise, false.</span></span>

### <a name="examples---in"></a><span data-ttu-id="156e4-217">例 - in</span><span class="sxs-lookup"><span data-stu-id="156e4-217">Examples - in</span></span>

<span data-ttu-id="156e4-218">次の例では、in メソッドが false を返す場合、バージョン コントロール システム内の特定の変更リストの内容を読み込みます。</span><span class="sxs-lookup"><span data-stu-id="156e4-218">The following example loads the contents a particular change list in the version control system, if the in method returns false.</span></span> <span data-ttu-id="156e4-219">changeSet セットには、コンテンツが既にロードされている変更リスト番号のリストが含まれています。</span><span class="sxs-lookup"><span data-stu-id="156e4-219">The changeSet set contains a list of the change list numbers that already have the content loaded.</span></span>

```xpp
public void pageActivated() 
{ 
    SysVersionControlTmpItem contentsAddition; 
    if (!changeSet.in(changes.ChangeNumber)) 
    { 
        startLengthyOperation(); 
        contentsAddition = versioncontrol.getChangeNumberContents( 
            changes.ChangeNumber); 
        while select contentsAddition 
        { 
            contentsItem.data(contentsAddition); 
            contentsItem.insert(); 
        } 
        contents_ds.executeQuery(); 
        changeSet.add(changes.ChangeNumber); 
    } 
    super(); 
}
```

## <a name="method-pack"></a><span data-ttu-id="156e4-220">メソッド pack</span><span class="sxs-lookup"><span data-stu-id="156e4-220">Method pack</span></span>

<span data-ttu-id="156e4-221">Set クラスの現在のインスタンスをシリアル化します。</span><span class="sxs-lookup"><span data-stu-id="156e4-221">Serializes the current instance of the Set class.</span></span>

```xpp
public container pack()
```

### <a name="return-value---pack"></a><span data-ttu-id="156e4-222">戻り値 - pack</span><span class="sxs-lookup"><span data-stu-id="156e4-222">Return Value - pack</span></span>

<span data-ttu-id="156e4-223">Set クラスの現在のインスタンスを含むコンテナーです。</span><span class="sxs-lookup"><span data-stu-id="156e4-223">A container that contains the current instance of the Set class.</span></span>

### <a name="remarks---pack"></a><span data-ttu-id="156e4-224">備考 - pack</span><span class="sxs-lookup"><span data-stu-id="156e4-224">Remarks - pack</span></span>

<span data-ttu-id="156e4-225">このメソッドで作成されたコンテナーには、セットの最初の要素の前に 3 つの要素が含まれます。</span><span class="sxs-lookup"><span data-stu-id="156e4-225">The container created by this method contains 3 elements before the first element from the set:</span></span>

-   <span data-ttu-id="156e4-226">コンテナのバージョン番号</span><span class="sxs-lookup"><span data-stu-id="156e4-226">A version number for the container</span></span>
-   <span data-ttu-id="156e4-227">セット要素のデータ型を識別する整数</span><span class="sxs-lookup"><span data-stu-id="156e4-227">An integer that identifies the data type of the set elements</span></span>
-   <span data-ttu-id="156e4-228">セット内の要素の数。</span><span class="sxs-lookup"><span data-stu-id="156e4-228">The number of elements in the set</span></span>

<span data-ttu-id="156e4-229">キーまたは値がオブジェクトになっている場合は、各オブジェクトに対して pack メソッドが呼び出され、サブコンテナーを作成します。</span><span class="sxs-lookup"><span data-stu-id="156e4-229">If the keys or the values are objects, the pack method is called on each object to create a subcontainer.</span></span> <span data-ttu-id="156e4-230">Set::create method を使用することにより、結果のコンテナから新しいセットを作成することができます。</span><span class="sxs-lookup"><span data-stu-id="156e4-230">You can create a new set from the resulting container by using the Set::create method.</span></span>

### <a name="examples---pack"></a><span data-ttu-id="156e4-231">例 - pack</span><span class="sxs-lookup"><span data-stu-id="156e4-231">Examples - pack</span></span>

<span data-ttu-id="156e4-232">次の例では、10 個の整数のセットを作成し、それをコンテナーにパックし、元の内容と同じ内容の新しいセットを作成します。</span><span class="sxs-lookup"><span data-stu-id="156e4-232">The following example creates a set of 10 integers, packs it into a container, and then creates a new set with contents identical to the original one.</span></span>

```xpp
{ 
    Set is1, is = new Set (Types::Integer); 
    int i; 
    container packedSet; 
    ; 
    // Create a set containing the first 10 integers. 
    for (i = 1; i <= 10; i++) 
    { 
        is.add(i); 
    } 
    // Pack it down in a container... 
    packedSet = is.pack(); 
    // ... and restore it 
    is1 = Set::create(packedSet); 
    print is1.toString(); 
    pause; 
}
```

## <a name="method-remove"></a><span data-ttu-id="156e4-233">メソッド remove</span><span class="sxs-lookup"><span data-stu-id="156e4-233">Method remove</span></span>

<span data-ttu-id="156e4-234">セットから要素を削除します。</span><span class="sxs-lookup"><span data-stu-id="156e4-234">Removes an element from the set.</span></span>

```xpp
public boolean remove(AnyType arg)
```

### <a name="parameters---remove"></a><span data-ttu-id="156e4-235">パラメーター - remove</span><span class="sxs-lookup"><span data-stu-id="156e4-235">Parameters - remove</span></span>

<span data-ttu-id="156e4-236">arg</span><span class="sxs-lookup"><span data-stu-id="156e4-236">arg</span></span>  
<span data-ttu-id="156e4-237">削除する要素。</span><span class="sxs-lookup"><span data-stu-id="156e4-237">The element to remove.</span></span>

### <a name="return-value---remove"></a><span data-ttu-id="156e4-238">戻り値 - remove</span><span class="sxs-lookup"><span data-stu-id="156e4-238">Return Value - remove</span></span>

<span data-ttu-id="156e4-239">要素が見つかり削除された場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="156e4-239">true if the element was found and removed; otherwise, false.</span></span>

### <a name="examples---remove"></a><span data-ttu-id="156e4-240">例 - remove</span><span class="sxs-lookup"><span data-stu-id="156e4-240">Examples - remove</span></span>

<span data-ttu-id="156e4-241">次の例では、noConfigs セットのいずれかの値が 2 番目のセットの yesConfigs セットに含まれているかどうかを確認します。</span><span class="sxs-lookup"><span data-stu-id="156e4-241">The following example checks whether any of the values in one set, the noConfigs set, are found in a second set, the yesConfigs set.</span></span> <span data-ttu-id="156e4-242">見つかった場合は、yesConfigs セットから削除されます。</span><span class="sxs-lookup"><span data-stu-id="156e4-242">If they are found, they are removed from the yesConfigs set.</span></span>

```xpp
Set             noConfigs; 
Set             yesConfigs; 
ConfigId        configId; 
SetEnumerator   se; 
; 
se = noConfigs.getEnumerator(); 
while (se.moveNext()) 
{ 
    configId    = se.current(); 
    if (yesConfigs.in(configId)) 
    { 
        yesConfigs.remove(configId); 
    } 
}
```

## <a name="method-tostring"></a><span data-ttu-id="156e4-243">メソッド toString</span><span class="sxs-lookup"><span data-stu-id="156e4-243">Method toString</span></span>

<span data-ttu-id="156e4-244">設定の内容を説明する文字列を返します。</span><span class="sxs-lookup"><span data-stu-id="156e4-244">Returns a string describing the contents of the set.</span></span>

```xpp
public str toString()
```

### <a name="return-value---tostring"></a><span data-ttu-id="156e4-245">戻り値 - toString</span><span class="sxs-lookup"><span data-stu-id="156e4-245">Return Value - toString</span></span>

<span data-ttu-id="156e4-246">設定の内容を説明する文字列。</span><span class="sxs-lookup"><span data-stu-id="156e4-246">A string that describes the contents of the set.</span></span>

### <a name="remarks---tostring"></a><span data-ttu-id="156e4-247">備考 - toString</span><span class="sxs-lookup"><span data-stu-id="156e4-247">Remarks - toString</span></span>

<span data-ttu-id="156e4-248">を使用して、セット内の単一要素の説明を取得します。</span><span class="sxs-lookup"><span data-stu-id="156e4-248">Use the to get the description of a single element within a set.</span></span>

### <a name="examples---tostring"></a><span data-ttu-id="156e4-249">例 - toString</span><span class="sxs-lookup"><span data-stu-id="156e4-249">Examples - toString</span></span>

<span data-ttu-id="156e4-250">次の例では、文字列のセットを作成し、そのセットの説明とセット内容の説明を出力します。</span><span class="sxs-lookup"><span data-stu-id="156e4-250">The following example creates a set of strings, and then prints out a description of the set and a description of the set contents.</span></span>

```xpp
{ 
    // Declare a set of strings 
    Set names = new Set (Types::String); 
    ; 
    // Add some values to the set. 
    names.add("Peter"); 
    names.add("Paul"); 
    names.add("Mary"); 
    print names.definitionString(); 
    print names.toString(); 
    pause; 
}
```

## <a name="method-typeid"></a><span data-ttu-id="156e4-251">メソッド typeId</span><span class="sxs-lookup"><span data-stu-id="156e4-251">Method typeId</span></span>

<span data-ttu-id="156e4-252">セット内の値のタイプを返します。</span><span class="sxs-lookup"><span data-stu-id="156e4-252">Returns the type of the values in the set.</span></span>

```xpp
public Types typeId()
```

### <a name="return-value---typeid"></a><span data-ttu-id="156e4-253">戻り値 - typeId</span><span class="sxs-lookup"><span data-stu-id="156e4-253">Return Value - typeId</span></span>

<span data-ttu-id="156e4-254">セット内の値のタイプ。</span><span class="sxs-lookup"><span data-stu-id="156e4-254">The type of the values in the set.</span></span>

### <a name="remarks---typeid"></a><span data-ttu-id="156e4-255">備考 - typeId</span><span class="sxs-lookup"><span data-stu-id="156e4-255">Remarks - typeId</span></span>

<span data-ttu-id="156e4-256">構成要素のタイプは、そのセットが作成されるときに決定される。</span><span class="sxs-lookup"><span data-stu-id="156e4-256">The type of the constituent elements is determined when the set is created.</span></span>

### <a name="examples---typeid"></a><span data-ttu-id="156e4-257">例 - typeId</span><span class="sxs-lookup"><span data-stu-id="156e4-257">Examples - typeId</span></span>

<span data-ttu-id="156e4-258">次の例では、既存のセットと同じタイプの新しいセットをインスタンス化します。</span><span class="sxs-lookup"><span data-stu-id="156e4-258">The following example instantiates a new set with the same type as an existing set.</span></span>

```xpp
{ 
    Set set1 = new Set(Types::Integer); 
    Set set2; 
   ; 
    set2 = new Set(set1.typeId()); 
    print set2.typeId(); 
    pause; 
}
```

## <a name="method-xml"></a><span data-ttu-id="156e4-259">メソッド xml</span><span class="sxs-lookup"><span data-stu-id="156e4-259">Method xml</span></span>

<span data-ttu-id="156e4-260">現在のオブジェクトを表す XML 文字列を返します。</span><span class="sxs-lookup"><span data-stu-id="156e4-260">Returns an XML string that represents the current object.</span></span>

```xpp
public str xml([int indent])
```

### <a name="parameters---xml"></a><span data-ttu-id="156e4-261">パラメーター - xml</span><span class="sxs-lookup"><span data-stu-id="156e4-261">Parameters - xml</span></span>

<span data-ttu-id="156e4-262">インデント</span><span class="sxs-lookup"><span data-stu-id="156e4-262">indent</span></span>  
<span data-ttu-id="156e4-263">返された XML 文字列のインデントの量 (省略可能)。</span><span class="sxs-lookup"><span data-stu-id="156e4-263">The amount of indentation of the returned XML string; optional.</span></span>

### <a name="return-value---xml"></a><span data-ttu-id="156e4-264">戻り値 - xml</span><span class="sxs-lookup"><span data-stu-id="156e4-264">Return Value - xml</span></span>

<span data-ttu-id="156e4-265">現在のオブジェクトを表す XML 文字列です。</span><span class="sxs-lookup"><span data-stu-id="156e4-265">An XML string that represents the current object.</span></span>

### <a name="remarks---xml"></a><span data-ttu-id="156e4-266">備考 - xml</span><span class="sxs-lookup"><span data-stu-id="156e4-266">Remarks - xml</span></span>

<span data-ttu-id="156e4-267">このメソッドをオーバーライドして、その型に対して意味のある値を返すことができます。</span><span class="sxs-lookup"><span data-stu-id="156e4-267">This method can be overridden to return values that are meaningful for that type.</span></span>

## <a name="method-create"></a><span data-ttu-id="156e4-268">メソッド create</span><span class="sxs-lookup"><span data-stu-id="156e4-268">Method create</span></span>

<span data-ttu-id="156e4-269">以前の Set.pack メソッドの呼び出しで取得したコンテナーからセットを作成します。</span><span class="sxs-lookup"><span data-stu-id="156e4-269">Creates a set from the container obtained from a prior call to the Set.pack method.</span></span>

```xpp
public static Set create(container container)
```

### <a name="parameters---create"></a><span data-ttu-id="156e4-270">パラメーター - create</span><span class="sxs-lookup"><span data-stu-id="156e4-270">Parameters - create</span></span>

<span data-ttu-id="156e4-271">コンテナー</span><span class="sxs-lookup"><span data-stu-id="156e4-271">container</span></span>  
<span data-ttu-id="156e4-272">パックされたセットを保持するコンテナー。</span><span class="sxs-lookup"><span data-stu-id="156e4-272">The container that holds the packed set.</span></span>

### <a name="return-value---create"></a><span data-ttu-id="156e4-273">戻り値 - create</span><span class="sxs-lookup"><span data-stu-id="156e4-273">Return Value - create</span></span>

<span data-ttu-id="156e4-274">コンテナーに梱包されたものと同じセット。</span><span class="sxs-lookup"><span data-stu-id="156e4-274">A set equal to the one that was packed into the container.</span></span>

### <a name="remarks---create"></a><span data-ttu-id="156e4-275">備考 - create</span><span class="sxs-lookup"><span data-stu-id="156e4-275">Remarks - create</span></span>

<span data-ttu-id="156e4-276">値がオブジェクトの場合、オブジェクトにはコンテナーからその内部状態を再設定するために呼び出されるアンパック メソッドが必要です。</span><span class="sxs-lookup"><span data-stu-id="156e4-276">If the values are objects, the objects must have an unpack method that is called to reestablish their internal state from the container.</span></span>

### <a name="examples---create"></a><span data-ttu-id="156e4-277">例 - create</span><span class="sxs-lookup"><span data-stu-id="156e4-277">Examples - create</span></span>

<span data-ttu-id="156e4-278">次の例では、セットを作成し、それをコンテナーにパックします。</span><span class="sxs-lookup"><span data-stu-id="156e4-278">The following example creates a set and packs it into a container.</span></span> <span data-ttu-id="156e4-279">次に、create メソッドを使用してコンテナーを展開し、元のセットと同じセットを作成します。</span><span class="sxs-lookup"><span data-stu-id="156e4-279">The create method is then used to unpack the container and create a set identical to the original one.</span></span>

```xpp
{ 
    Set is1, is = new Set (Types::Integer); 
    int i; 
    container packedSet; 
    ; 
    // Add 10 integers (0 - 9) to the set 
    for (i = 1; i <= 10; i++) 
    { 
        is.add(i); 
    } 
    // Pack the set into a container... 
    packedSet = is.pack(); 
    // ... and restore it 
    is1 = Set::create(packedSet); 
    print is1.toString(); 
    pause; 
}
```

## <a name="method-createfromxml"></a><span data-ttu-id="156e4-280">メソッド createFromXML</span><span class="sxs-lookup"><span data-stu-id="156e4-280">Method createFromXML</span></span>

```xpp
public static Set createFromXML(Object xmlnode)
```

### <a name="parameters---createfromxml"></a><span data-ttu-id="156e4-281">パラメータ - createFromXML</span><span class="sxs-lookup"><span data-stu-id="156e4-281">Parameters - createFromXML</span></span>

<span data-ttu-id="156e4-282">xmlnode</span><span class="sxs-lookup"><span data-stu-id="156e4-282">xmlnode</span></span>  

### <a name="return-value---createfromxml"></a><span data-ttu-id="156e4-283">戻り値 - createFromXML</span><span class="sxs-lookup"><span data-stu-id="156e4-283">Return Value - createFromXML</span></span>

## <a name="method-difference"></a><span data-ttu-id="156e4-284">メソッド difference</span><span class="sxs-lookup"><span data-stu-id="156e4-284">Method difference</span></span>

<span data-ttu-id="156e4-285">set2 で検出されない set1 の要素を含むセットを計算および取得します。</span><span class="sxs-lookup"><span data-stu-id="156e4-285">Calculates and retrieves the set containing the elements from set1 that are not found in set2.</span></span>

```xpp
public static Set difference(Set set1, Set set2)
```

### <a name="parameters---difference"></a><span data-ttu-id="156e4-286">パラメーター - difference</span><span class="sxs-lookup"><span data-stu-id="156e4-286">Parameters - difference</span></span>

<span data-ttu-id="156e4-287">set1</span><span class="sxs-lookup"><span data-stu-id="156e4-287">set1</span></span>  
<span data-ttu-id="156e4-288">チェックするセット。</span><span class="sxs-lookup"><span data-stu-id="156e4-288">The set to check.</span></span>

<!-- -->

<span data-ttu-id="156e4-289">set2</span><span class="sxs-lookup"><span data-stu-id="156e4-289">set2</span></span>  
<span data-ttu-id="156e4-290">チェックするセット。</span><span class="sxs-lookup"><span data-stu-id="156e4-290">The set to check.</span></span>

### <a name="return-value---difference"></a><span data-ttu-id="156e4-291">戻り値 - difference</span><span class="sxs-lookup"><span data-stu-id="156e4-291">Return Value - difference</span></span>

<span data-ttu-id="156e4-292">set2 で検出されない set1 の要素を含むセット。</span><span class="sxs-lookup"><span data-stu-id="156e4-292">A set containing the elements from set1 that are not found in set2.</span></span>

### <a name="remarks---difference"></a><span data-ttu-id="156e4-293">備考 - difference</span><span class="sxs-lookup"><span data-stu-id="156e4-293">Remarks - difference</span></span>

<span data-ttu-id="156e4-294">比較される 2 つのセットは、同じタイプでなければなりません。</span><span class="sxs-lookup"><span data-stu-id="156e4-294">The two sets to be compared must be of the same type.</span></span>

### <a name="examples---difference"></a><span data-ttu-id="156e4-295">例 - difference</span><span class="sxs-lookup"><span data-stu-id="156e4-295">Examples - difference</span></span>

<span data-ttu-id="156e4-296">次の例では、整数 1､2 および 3 を含む 1 つのセットと、整数 2 および 4 を含む 1 つのセットを作成します。</span><span class="sxs-lookup"><span data-stu-id="156e4-296">The following example creates one set that contains the integers 1, 2, and 3, and one set that contains the integers 2 and 4.</span></span> <span data-ttu-id="156e4-297">差異メソッドは、最初のセット内の 2 番目のセット (1 および 3) にない要素を含むセットを作成するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="156e4-297">The difference method is used to create a set that contains the elements in the first set that are not in the second set (1 and 3).</span></span>

```xpp
{ 
    Set is = new Set (Types::Integer); 
    Set is2, is1 = new Set (Types::Integer); 
    ; 
    is.add(1); 
    is.add(2); 
    is.add(3); 
    is1.add(2); 
    is1.add(4); 
    is2 = Set::difference(is, is1); 
    // prints "{1, 3}" 
    print is2.toString(); 
    pause; 
}
```

## <a name="method-intersection"></a><span data-ttu-id="156e4-298">メソッド intersection</span><span class="sxs-lookup"><span data-stu-id="156e4-298">Method intersection</span></span>

<span data-ttu-id="156e4-299">2 つのセット内で検出される同一の値を計算して返します。</span><span class="sxs-lookup"><span data-stu-id="156e4-299">Calculates and returns the identical values found in two sets.</span></span>

```xpp
public static Set intersection(Set set1, Set set2)
```

### <a name="parameters---intersection"></a><span data-ttu-id="156e4-300">パラメーター - intersection</span><span class="sxs-lookup"><span data-stu-id="156e4-300">Parameters - intersection</span></span>

<span data-ttu-id="156e4-301">set1</span><span class="sxs-lookup"><span data-stu-id="156e4-301">set1</span></span>  
<span data-ttu-id="156e4-302">比較する 2 番目のセット。</span><span class="sxs-lookup"><span data-stu-id="156e4-302">The second set to be compared.</span></span>

<!-- -->

<span data-ttu-id="156e4-303">set2</span><span class="sxs-lookup"><span data-stu-id="156e4-303">set2</span></span>  
<span data-ttu-id="156e4-304">比較する 2 番目のセット。</span><span class="sxs-lookup"><span data-stu-id="156e4-304">The second set to be compared.</span></span>

### <a name="return-value---intersection"></a><span data-ttu-id="156e4-305">戻り値 - intersection</span><span class="sxs-lookup"><span data-stu-id="156e4-305">Return Value - intersection</span></span>

<span data-ttu-id="156e4-306">両方のセットで検出された要素を含むセット。</span><span class="sxs-lookup"><span data-stu-id="156e4-306">A set containing the elements found in both sets.</span></span>

### <a name="examples---intersection"></a><span data-ttu-id="156e4-307">例 - intersection</span><span class="sxs-lookup"><span data-stu-id="156e4-307">Examples - intersection</span></span>

<span data-ttu-id="156e4-308">次の例では、2 つの整数セットを作成し、それらにいくつかの値を追加します。</span><span class="sxs-lookup"><span data-stu-id="156e4-308">The following example creates two sets of integers and adds some values to them.</span></span> <span data-ttu-id="156e4-309">両方のセットに含まれている値の一覧を出力します。</span><span class="sxs-lookup"><span data-stu-id="156e4-309">It then prints a list of the values that are that is contained in both sets.</span></span>

```xpp
{ 
    Set is = new Set (Types::Integer); 
    Set is2, is1 = new Set (Types::Integer); 
    ; 
    is.add(1); 
    is.add(2); 
    is.add(3); 
    is1.add(2); 
    is1.add(4); 
    is2 = Set::intersection(is, is1); 
    // Prints "{2}" because 2 is contained in both is and is2. 
    print is2.toString(); 
}
```

## <a name="method-union"></a><span data-ttu-id="156e4-310">メソッド union</span><span class="sxs-lookup"><span data-stu-id="156e4-310">Method union</span></span>

<span data-ttu-id="156e4-311">指定された 2 つのセットの和集合を計算および取得します</span><span class="sxs-lookup"><span data-stu-id="156e4-311">Calculates and retrieves the union of two given sets.</span></span> <span data-ttu-id="156e4-312">これは、少なくとも 1 つのセットにある値を含むセットです。</span><span class="sxs-lookup"><span data-stu-id="156e4-312">This is the set that contains the values found in at least one of the sets.</span></span>

```xpp
public static Set union(Set set1, Set set2)
```

### <a name="parameters---union"></a><span data-ttu-id="156e4-313">パラメーター - union</span><span class="sxs-lookup"><span data-stu-id="156e4-313">Parameters - union</span></span>

<span data-ttu-id="156e4-314">set1</span><span class="sxs-lookup"><span data-stu-id="156e4-314">set1</span></span>  
<span data-ttu-id="156e4-315">比較される 2 つのセットのうちの 2 番目のセット。</span><span class="sxs-lookup"><span data-stu-id="156e4-315">The second of the two sets that are compared.</span></span>

<!-- -->

<span data-ttu-id="156e4-316">set2</span><span class="sxs-lookup"><span data-stu-id="156e4-316">set2</span></span>  
<span data-ttu-id="156e4-317">比較される 2 つのセットのうちの 2 番目のセット。</span><span class="sxs-lookup"><span data-stu-id="156e4-317">The second of the two sets that are compared.</span></span>

### <a name="return-value---union"></a><span data-ttu-id="156e4-318">戻り値 - union</span><span class="sxs-lookup"><span data-stu-id="156e4-318">Return Value - union</span></span>

<span data-ttu-id="156e4-319">set1 または set2 で検出された要素を含むセット。</span><span class="sxs-lookup"><span data-stu-id="156e4-319">The set containing elements found in set1 or set2.</span></span>

### <a name="remarks---union"></a><span data-ttu-id="156e4-320">備考 - union</span><span class="sxs-lookup"><span data-stu-id="156e4-320">Remarks - union</span></span>

<span data-ttu-id="156e4-321">比較される 2 つのセットは、同じタイプでなければなりません。</span><span class="sxs-lookup"><span data-stu-id="156e4-321">The two sets that are compared must be of the same type.</span></span>

### <a name="examples---union"></a><span data-ttu-id="156e4-322">例 - union</span><span class="sxs-lookup"><span data-stu-id="156e4-322">Examples - union</span></span>

<span data-ttu-id="156e4-323">次の例では、2 つの整数セットを作成し、それらにいくつかの値を追加します。</span><span class="sxs-lookup"><span data-stu-id="156e4-323">The following example creates two sets of integers and adds some values to them.</span></span> <span data-ttu-id="156e4-324">セットのいずれかに含まれるすべての値を含む新しいセットを作成します。</span><span class="sxs-lookup"><span data-stu-id="156e4-324">It then creates a new set that contains all the values that are contained in either of the sets.</span></span>

```xpp
{ 
    Set is = new Set (Types::Integer); 
    Set is2, is1 = new Set (Types::Integer); 
    ; 
    is.add(1); 
    is.add(2); 
    is.add(3); 
    is1.add(2); 
    is1.add(4); 
    is2 = Set::union(is, is1); 
    // Prints "{1, 2, 3, 4}". 
    print is2.toString(); 
    pause; 
}
```

## <a name="method-new"></a><span data-ttu-id="156e4-325">メソッド new</span><span class="sxs-lookup"><span data-stu-id="156e4-325">Method new</span></span>

<span data-ttu-id="156e4-326">指定した型の要素を含めることができるセットを作成します。</span><span class="sxs-lookup"><span data-stu-id="156e4-326">Creates a set that can contain elements of the specified type.</span></span>

```xpp
public void new(Types Type)
```

### <a name="parameters---new"></a><span data-ttu-id="156e4-327">パラメーター - new</span><span class="sxs-lookup"><span data-stu-id="156e4-327">Parameters - new</span></span>

<span data-ttu-id="156e4-328">種類</span><span class="sxs-lookup"><span data-stu-id="156e4-328">Type</span></span>  
<span data-ttu-id="156e4-329">セット内の要素のタイプ。</span><span class="sxs-lookup"><span data-stu-id="156e4-329">The type of the elements within the set.</span></span>

### <a name="remarks---new"></a><span data-ttu-id="156e4-330">備考 - new</span><span class="sxs-lookup"><span data-stu-id="156e4-330">Remarks - new</span></span>

<span data-ttu-id="156e4-331">セットが作成された後、セットのタイプを変更することはできません。</span><span class="sxs-lookup"><span data-stu-id="156e4-331">The type of the set cannot be changed after the set has been created.</span></span>

### <a name="examples---new"></a><span data-ttu-id="156e4-332">例 - new</span><span class="sxs-lookup"><span data-stu-id="156e4-332">Examples - new</span></span>

<span data-ttu-id="156e4-333">次の例では、一連の整数とオブジェクトのセットを作成します。</span><span class="sxs-lookup"><span data-stu-id="156e4-333">The following example creates a set of integers and a set of objects.</span></span>

```xpp
{ 
    // Create a set of integers. 
    Set is = new Set (Types::Integer); 
    // Create a set of objects. 
    Set os = new Set (Types::Class); 
}
```

