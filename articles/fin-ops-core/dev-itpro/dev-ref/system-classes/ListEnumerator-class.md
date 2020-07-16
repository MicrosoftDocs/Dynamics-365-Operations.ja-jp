---
title: ListEnumerator クラス
description: このトピックでは、ListEnumerator クラスについて説明します。
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
ms.openlocfilehash: 8ecc0c940718a0de4f30660c0eaf8cf28f79e955
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502590"
---
# <a name="class-listenumerator"></a><span data-ttu-id="8e238-103">クラス ListEnumerator</span><span class="sxs-lookup"><span data-stu-id="8e238-103">Class ListEnumerator</span></span>

[!include [banner](../../includes/banner.md)]

```xpp
class ListEnumerator extends Object
```

<span data-ttu-id="8e238-104">ListEnumerator クラスを使用すると、一覧内の要素上を移動できます。</span><span class="sxs-lookup"><span data-stu-id="8e238-104">The ListEnumerator class lets you traverse the elements in a list.</span></span>

## <a name="remarks"></a><span data-ttu-id="8e238-105">備考</span><span class="sxs-lookup"><span data-stu-id="8e238-105">Remarks</span></span>

<span data-ttu-id="8e238-106">リストの列挙子は、リストの最初の要素の前に開始します。</span><span class="sxs-lookup"><span data-stu-id="8e238-106">List enumerators start before the first element in the list.</span></span> <span data-ttu-id="8e238-107">リストの最初の要素を指すようにするために ListEnumerator.moveNext メソッドを呼び出す必要があります。</span><span class="sxs-lookup"><span data-stu-id="8e238-107">You must call the ListEnumerator.moveNext method to make it point to the first element in the list.</span></span> <span data-ttu-id="8e238-108">list.getEnumerator メソッドが呼び出されたときに、リストと同じ層で列挙子が自動的に作成されるため、ListIterator クラスではなく、ListEnumerator クラスを使用することがベスト プラクティスです。</span><span class="sxs-lookup"><span data-stu-id="8e238-108">It is best practice to use the ListEnumerator class instead of the ListIterator class, because enumerators are automatically created on the same tier as the list (when the list.getEnumerator method is called).</span></span> <span data-ttu-id="8e238-109">これにより、Caller from としてマークされたコードの潜在的な問題を回避します。反復子とリストは別々の層に置くことができます。</span><span class="sxs-lookup"><span data-stu-id="8e238-109">This avoids a potential problem in code that is marked as Called from, where the iterator and list can be on separate tiers.</span></span> <span data-ttu-id="8e238-110">さらに、リスト列挙子はリスト反復子よりも少ないコードを必要とするためパフォーマンスが少し向上します。</span><span class="sxs-lookup"><span data-stu-id="8e238-110">In addition, list enumerators require less code than list iterators and therefore perform slightly better.</span></span> <span data-ttu-id="8e238-111">リスト反復子を使用する必要がある唯一の状況は、リストから項目を削除する場合です (ListIterator.delete メソッドを使用します)。</span><span class="sxs-lookup"><span data-stu-id="8e238-111">The only situation where you have to use a list iterator is if you want to delete items from a list (use the ListIterator.delete method).</span></span>

## <a name="examples"></a><span data-ttu-id="8e238-112">例</span><span class="sxs-lookup"><span data-stu-id="8e238-112">Examples</span></span>

<span data-ttu-id="8e238-113">次の例では、整数のリストを作成し、いくつかの値をその中に入れます。</span><span class="sxs-lookup"><span data-stu-id="8e238-113">The following example creates a list of integers and puts some values into it.</span></span> <span data-ttu-id="8e238-114">その後、列挙子を作成し、一覧の最初の要素、一覧の 2 番目の要素に列挙子を設定します。</span><span class="sxs-lookup"><span data-stu-id="8e238-114">It then creates an enumerator, and then sets the enumerator to the first element in the list and then the second element in the list.</span></span>

```xpp
{ 
    List list = new List(Types::Integer); 
    ListEnumerator enumerator; 
    // Add some elements to the list 
    list.addEnd(1); 
    list.addEnd(2); 
    list.addStart(3); 
    // Set the enumerator 
    enumerator = list.getEnumerator(); 
    // Print a description of the list 
    print enumerator.definitionString(); 
    // Go to beginning of enumerator 
    enumerator.reset(); 
    //Go to the first element in the List 
    enumerator.moveNext(); 
    // Print contents of first and second elements 
    // First element is 3 as this was added to start of list 
    print enumerator.toString(); 
    enumerator.moveNext(); 
    print enumerator.toString(); 
    pause; 
}
```

## <a name="methods"></a><span data-ttu-id="8e238-115">メソッド</span><span class="sxs-lookup"><span data-stu-id="8e238-115">Methods</span></span>

| <span data-ttu-id="8e238-116">方法</span><span class="sxs-lookup"><span data-stu-id="8e238-116">Method</span></span>                        | <span data-ttu-id="8e238-117">説明</span><span class="sxs-lookup"><span data-stu-id="8e238-117">Description</span></span>                                                                                                   |
|-------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8e238-118">public AnyType current()</span><span class="sxs-lookup"><span data-stu-id="8e238-118">public AnyType current()</span></span>      | <span data-ttu-id="8e238-119">列挙子によりポイントされている値を取得します。</span><span class="sxs-lookup"><span data-stu-id="8e238-119">Retrieves the value that is pointed to by the enumerator.</span></span>                                                     |
| <span data-ttu-id="8e238-120">public str definitionString()</span><span class="sxs-lookup"><span data-stu-id="8e238-120">public str definitionString()</span></span> | <span data-ttu-id="8e238-121">列挙子の説明を返します。</span><span class="sxs-lookup"><span data-stu-id="8e238-121">Returns a description of the enumerator.</span></span>                                                                      |
| <span data-ttu-id="8e238-122">public boolean moveNext()</span><span class="sxs-lookup"><span data-stu-id="8e238-122">public boolean moveNext()</span></span>     | <span data-ttu-id="8e238-123">列挙子が有効なリスト要素を示すかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="8e238-123">Determines whether the enumerator denotes a valid list element.</span></span>                                               |
| <span data-ttu-id="8e238-124">public str toString()</span><span class="sxs-lookup"><span data-stu-id="8e238-124">public str toString()</span></span>         | <span data-ttu-id="8e238-125">列挙子が現在ポイントしているリスト内の要素の内容の説明を返します。</span><span class="sxs-lookup"><span data-stu-id="8e238-125">Returns a description of the content of the element in the list that the enumerator is currently pointing to.</span></span> |
| <span data-ttu-id="8e238-126">public void reset()</span><span class="sxs-lookup"><span data-stu-id="8e238-126">public void reset()</span></span>           | <span data-ttu-id="8e238-127">列挙子をリストの先頭に移動します。</span><span class="sxs-lookup"><span data-stu-id="8e238-127">Moves the enumerator to the start of the list.</span></span>                                                                |

## <a name="method-current"></a><span data-ttu-id="8e238-128">メソッド current</span><span class="sxs-lookup"><span data-stu-id="8e238-128">Method current</span></span>

<span data-ttu-id="8e238-129">列挙子によりポイントされている値を取得します。</span><span class="sxs-lookup"><span data-stu-id="8e238-129">Retrieves the value that is pointed to by the enumerator.</span></span>

```xpp
public AnyType current()
```

### <a name="return-value---current"></a><span data-ttu-id="8e238-130">戻り値 - current</span><span class="sxs-lookup"><span data-stu-id="8e238-130">Return Value - current</span></span>

<span data-ttu-id="8e238-131">リスト内で現在指定されている値。</span><span class="sxs-lookup"><span data-stu-id="8e238-131">The value that is currently pointed to in the list.</span></span> <span data-ttu-id="8e238-132">戻り値のタイプは、リスト内の項目のタイプによって決まります。</span><span class="sxs-lookup"><span data-stu-id="8e238-132">The type of the return value is determined by the type of the items in the list.</span></span>

### <a name="examples---current"></a><span data-ttu-id="8e238-133">例 - current</span><span class="sxs-lookup"><span data-stu-id="8e238-133">Examples - current</span></span>

<span data-ttu-id="8e238-134">次の例では、リストを反復処理し、dimensionTopic 変数を現在のリスト要素の値に設定します。</span><span class="sxs-lookup"><span data-stu-id="8e238-134">The following example iterates through the list and sets the dimensionTopic variable to the value of the current list element.</span></span>

```xpp
public DimensionTopic firstDimensionTopic() 
{ 
    DimensionTopic  dimensionTopic; 
    ListEnumerator  enumerator; 
    enumerator = this.getTopicsEnumerator(); 
    if (enumerator.moveNext()) 
    { 
        dimensionTopic = enumerator.current(); 
    } 
    return dimensionTopic; 
}
```

## <a name="method-definitionstring"></a><span data-ttu-id="8e238-135">メソッド definitionString</span><span class="sxs-lookup"><span data-stu-id="8e238-135">Method definitionString</span></span>

<span data-ttu-id="8e238-136">列挙子の説明を返します。</span><span class="sxs-lookup"><span data-stu-id="8e238-136">Returns a description of the enumerator.</span></span>

```xpp
public str definitionString()
```

### <a name="return-value---definitionstring"></a><span data-ttu-id="8e238-137">戻り値 - definitionString</span><span class="sxs-lookup"><span data-stu-id="8e238-137">Return Value - definitionString</span></span>

<span data-ttu-id="8e238-138">列挙子の説明を含む文字列。</span><span class="sxs-lookup"><span data-stu-id="8e238-138">A string that contains a description of the enumerator.</span></span>

### <a name="remarks---definitionstring"></a><span data-ttu-id="8e238-139">備考 - definitionString</span><span class="sxs-lookup"><span data-stu-id="8e238-139">Remarks - definitionString</span></span>

<span data-ttu-id="8e238-140">たとえば、整数のリストの列挙子は、int リスト列挙子を返します。</span><span class="sxs-lookup"><span data-stu-id="8e238-140">For example, an enumerator for a list of integers would return int list enumerator.</span></span>

### <a name="examples---definitionstring"></a><span data-ttu-id="8e238-141">例 - definitionString</span><span class="sxs-lookup"><span data-stu-id="8e238-141">Examples - definitionString</span></span>

<span data-ttu-id="8e238-142">次の例では、リストとそのリストの列挙子を作成します。</span><span class="sxs-lookup"><span data-stu-id="8e238-142">The following example creates a list and an enumerator for the list.</span></span> <span data-ttu-id="8e238-143">definitionString メソッドを使用して、列挙子の説明を出力します。</span><span class="sxs-lookup"><span data-stu-id="8e238-143">It uses the definitionString method to print a description of the enumerator.</span></span>

```xpp
{ 
    List list = new List(Types::Integer); 
    ListEnumerator  enumerator; 
    ; 
    // Add some elements to the list 
    list.addEnd(1); 
    list.addEnd(2); 
    list.addStart(3); 
    // Set the enumerator 
    enumerator = list.getEnumerator(); 
    print enumerator.definitionString(); 
    pause; 
}
```

## <a name="method-movenext"></a><span data-ttu-id="8e238-144">メソッド moveNext</span><span class="sxs-lookup"><span data-stu-id="8e238-144">Method moveNext</span></span>

<span data-ttu-id="8e238-145">列挙子が有効なリスト要素を示すかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="8e238-145">Determines whether the enumerator denotes a valid list element.</span></span>

```xpp
public boolean moveNext()
```

### <a name="return-value---movenext"></a><span data-ttu-id="8e238-146">戻り値 - moveNext</span><span class="sxs-lookup"><span data-stu-id="8e238-146">Return Value - moveNext</span></span>

<span data-ttu-id="8e238-147">リスト内の現在の職位が有効な要素を保持している場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="8e238-147">true if the current position in the list holds a valid element; otherwise, false.</span></span>

### <a name="remarks---movenext"></a><span data-ttu-id="8e238-148">備考 - moveNext</span><span class="sxs-lookup"><span data-stu-id="8e238-148">Remarks - moveNext</span></span>

<span data-ttu-id="8e238-149">リストの列挙子は、リストの最初の要素の前に開始します。</span><span class="sxs-lookup"><span data-stu-id="8e238-149">List enumerators start before the first element in the list.</span></span> <span data-ttu-id="8e238-150">リストの最初の要素を指すようにするために moveNext メソッドを呼び出す必要があります。</span><span class="sxs-lookup"><span data-stu-id="8e238-150">You must call the moveNext method to make it point to the first element in the list.</span></span>

### <a name="examples---movenext"></a><span data-ttu-id="8e238-151">例 - moveNext</span><span class="sxs-lookup"><span data-stu-id="8e238-151">Examples - moveNext</span></span>

<span data-ttu-id="8e238-152">次の例では、moveNext メソッドを使用してリスト内に別の要素があるかどうかを確認し、dimensionTopic 変数を現在のリスト要素の値に設定します。</span><span class="sxs-lookup"><span data-stu-id="8e238-152">The following example uses the moveNext method to check whether there is another element in the list and then sets the dimensionTopic variable to the value of the current list element.</span></span>

```xpp
public DimensionTopic firstDimensionTopic() 
{ 
    DimensionTopic  dimensionTopic; 
    ListEnumerator  enumerator; 
    enumerator = this.getTopicsEnumerator(); 
    if (enumerator.moveNext()) 
    { 
        dimensionTopic = enumerator.current(); 
    } 
    return dimensionTopic; 
}
```

## <a name="method-tostring"></a><span data-ttu-id="8e238-153">メソッド toString</span><span class="sxs-lookup"><span data-stu-id="8e238-153">Method toString</span></span>

<span data-ttu-id="8e238-154">列挙子が現在ポイントしているリスト内の要素の内容の説明を返します。</span><span class="sxs-lookup"><span data-stu-id="8e238-154">Returns a description of the content of the element in the list that the enumerator is currently pointing to.</span></span>

```xpp
public str toString()
```

### <a name="return-value---tostring"></a><span data-ttu-id="8e238-155">戻り値 - toString</span><span class="sxs-lookup"><span data-stu-id="8e238-155">Return Value - toString</span></span>

<span data-ttu-id="8e238-156">現在のリスト要素の説明を含む文字列。</span><span class="sxs-lookup"><span data-stu-id="8e238-156">A string that contains a description of the current list element.</span></span>

### <a name="examples---tostring"></a><span data-ttu-id="8e238-157">例 - toString</span><span class="sxs-lookup"><span data-stu-id="8e238-157">Examples - toString</span></span>

<span data-ttu-id="8e238-158">次の例では、リストを作成し、最初の要素と 2 番目の要素の内容をリストに出力します。</span><span class="sxs-lookup"><span data-stu-id="8e238-158">The following example creates a list, and then prints the content of the first and second elements in the list.</span></span>

```xpp
{ 
    List list = new List(Types::Integer); 
    ListEnumerator  enumerator; 
    // Add some elements to the list 
    list.addEnd(1); 
    list.addEnd(2); 
    list.addStart(3); 
    // Set the enumerator 
    enumerator = list.getEnumerator(); 
    // Go to beginning of enumerator 
    enumerator.reset(); 
    //Go to the first element in the List 
    enumerator.moveNext(); 
    // First element is 3 as this was added to start of list 
    print enumerator.toString(); 
    pause; 
    enumerator.moveNext(); 
    //Print second element in list (1) 
    print enumerator.toString(); 
    pause; 
}
```

## <a name="method-reset"></a><span data-ttu-id="8e238-159">メソッド reset</span><span class="sxs-lookup"><span data-stu-id="8e238-159">Method reset</span></span>

<span data-ttu-id="8e238-160">列挙子をリストの先頭に移動します。</span><span class="sxs-lookup"><span data-stu-id="8e238-160">Moves the enumerator to the start of the list.</span></span>

```xpp
public void reset()
```

### <a name="remarks---reset"></a><span data-ttu-id="8e238-161">備考 - reset</span><span class="sxs-lookup"><span data-stu-id="8e238-161">Remarks - reset</span></span>

<span data-ttu-id="8e238-162">reset メソッドは、列挙子をリストの先頭、リストの最初の要素の前に移動します。</span><span class="sxs-lookup"><span data-stu-id="8e238-162">The reset method moves the enumerator to the start of the list, before the first element in the list.</span></span> <span data-ttu-id="8e238-163">リストの最初の要素を指すようにするために ListEnumerator.moveNext メソッドを呼び出す必要があります。</span><span class="sxs-lookup"><span data-stu-id="8e238-163">You must call the ListEnumerator.moveNext method to make it point to the first element in the list.</span></span>

### <a name="examples---reset"></a><span data-ttu-id="8e238-164">例 - reset</span><span class="sxs-lookup"><span data-stu-id="8e238-164">Examples - reset</span></span>

<span data-ttu-id="8e238-165">次の例では、リストを作成し、そのリストの列挙子を作成します。</span><span class="sxs-lookup"><span data-stu-id="8e238-165">The following example creates a list and then an enumerator for the list.</span></span> <span data-ttu-id="8e238-166">reset メソッドを使用して一覧の先頭に移動し、moveNext メソッドを使用して一覧の最初の要素に移動します。</span><span class="sxs-lookup"><span data-stu-id="8e238-166">It uses the reset method to move to the start of the list and then uses the moveNext method to move to the first element in the list.</span></span>

```xpp
{ 
    List list = new List(Types::Integer); 
    ListEnumerator  enumerator; 
    // Add some elements to the list 
    list.addEnd(1); 
    list.addEnd(2); 
    list.addStart(3); 
    // Set the enumerator 
    enumerator = list.getEnumerator(); 
    // Go to beginning of enumerator 
    enumerator.reset(); 
    //Go to the first element in the List 
    enumerator.moveNext(); 
    // First element is 3 as this was added to start of list 
    print enumerator.toString(); 
    pause; 
}
```

