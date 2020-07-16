---
title: SetEnumerator クラス
description: このトピックでは、SetEnumerator クラスについて説明します。
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
ms.openlocfilehash: 6ddb5f3118ccd221df0c3ad81a315b14d4b48e03
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502804"
---
# <a name="class-setenumerator"></a><span data-ttu-id="e8ea9-103">クラス SetEnumerator</span><span class="sxs-lookup"><span data-stu-id="e8ea9-103">Class SetEnumerator</span></span>

[!include [banner](../../includes/banner.md)]

```xpp
class SetEnumerator extends Object
```

<span data-ttu-id="e8ea9-104">SetEnumerator クラスを使用すると、セット内の要素上を移動できます。</span><span class="sxs-lookup"><span data-stu-id="e8ea9-104">The SetEnumerator class lets you traverse the elements in a set.</span></span>

## <a name="remarks"></a><span data-ttu-id="e8ea9-105">備考</span><span class="sxs-lookup"><span data-stu-id="e8ea9-105">Remarks</span></span>

<span data-ttu-id="e8ea9-106">セット列挙子は、セットの最初の要素の前に開始します。</span><span class="sxs-lookup"><span data-stu-id="e8ea9-106">Set enumerators start before the first element in the set.</span></span> <span data-ttu-id="e8ea9-107">セットの最初の要素を指すようにするために SetEnumerator.moveNext メソッドを呼び出す必要があります。</span><span class="sxs-lookup"><span data-stu-id="e8ea9-107">You must call the SetEnumerator.moveNext method to make it point to the first element in the set.</span></span> <span data-ttu-id="e8ea9-108">ベスト プラクティスとしては、set.getEnumerator メソッドが呼び出されたときに、設定されている同じ層で列挙子が自動的に作成されるため、SetIterator クラスではなく、SetEnumerator クラスを使用します。</span><span class="sxs-lookup"><span data-stu-id="e8ea9-108">As a best practice, use the SetEnumerator class instead of the SetIterator class, because enumerators are automatically created on the same tier as the set when the set.getEnumerator method is called.</span></span> <span data-ttu-id="e8ea9-109">これにより、Caller from としてマークされたコードの潜在的な問題を回避できます。反復子とセットは別々の層に置くことができます。</span><span class="sxs-lookup"><span data-stu-id="e8ea9-109">This helps you avoid a potential problem in code that is marked as Called from, where the iterator and set can be on separate tiers.</span></span> <span data-ttu-id="e8ea9-110">さらに、セット列挙子はセット反復子よりも少ないコードを必要とするためパフォーマンスが少し向上します。</span><span class="sxs-lookup"><span data-stu-id="e8ea9-110">In addition, set enumerators require less code than set iterators and therefore perform slightly better.</span></span>

## <a name="examples"></a><span data-ttu-id="e8ea9-111">例</span><span class="sxs-lookup"><span data-stu-id="e8ea9-111">Examples</span></span>

## <a name="methods"></a><span data-ttu-id="e8ea9-112">メソッド</span><span class="sxs-lookup"><span data-stu-id="e8ea9-112">Methods</span></span>

| <span data-ttu-id="e8ea9-113">方法</span><span class="sxs-lookup"><span data-stu-id="e8ea9-113">Method</span></span>                        | <span data-ttu-id="e8ea9-114">説明</span><span class="sxs-lookup"><span data-stu-id="e8ea9-114">Description</span></span>                                                                                                |
|-------------------------------|------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e8ea9-115">public AnyType current()</span><span class="sxs-lookup"><span data-stu-id="e8ea9-115">public AnyType current()</span></span>      | <span data-ttu-id="e8ea9-116">列挙子によりポイントされている値を取得します。</span><span class="sxs-lookup"><span data-stu-id="e8ea9-116">Retrieves the value that is pointed to by the enumerator.</span></span>                                                  |
| <span data-ttu-id="e8ea9-117">public str definitionString()</span><span class="sxs-lookup"><span data-stu-id="e8ea9-117">public str definitionString()</span></span> | <span data-ttu-id="e8ea9-118">列挙子の説明を返します。</span><span class="sxs-lookup"><span data-stu-id="e8ea9-118">Returns a description of the enumerator.</span></span>                                                                   |
| <span data-ttu-id="e8ea9-119">public boolean moveNext()</span><span class="sxs-lookup"><span data-stu-id="e8ea9-119">public boolean moveNext()</span></span>     | <span data-ttu-id="e8ea9-120">列挙子が有効なセット要素を示すかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="e8ea9-120">Determines whether the enumerator denotes a valid set element.</span></span>                                             |
| <span data-ttu-id="e8ea9-121">public str toString()</span><span class="sxs-lookup"><span data-stu-id="e8ea9-121">public str toString()</span></span>         | <span data-ttu-id="e8ea9-122">列挙子が現在ポイントしているセット内の要素の内容の説明を取得します。</span><span class="sxs-lookup"><span data-stu-id="e8ea9-122">Retrieves a description of the contents of the element in the set that the enumerator currently points to.</span></span> |
| <span data-ttu-id="e8ea9-123">public void reset()</span><span class="sxs-lookup"><span data-stu-id="e8ea9-123">public void reset()</span></span>           | <span data-ttu-id="e8ea9-124">列挙子をセットの先頭に移動します。</span><span class="sxs-lookup"><span data-stu-id="e8ea9-124">Moves the enumerator to the start of the set.</span></span>                                                              |

## <a name="method-current"></a><span data-ttu-id="e8ea9-125">メソッド current</span><span class="sxs-lookup"><span data-stu-id="e8ea9-125">Method current</span></span>

<span data-ttu-id="e8ea9-126">列挙子によりポイントされている値を取得します。</span><span class="sxs-lookup"><span data-stu-id="e8ea9-126">Retrieves the value that is pointed to by the enumerator.</span></span>

```xpp
public AnyType current()
```

### <a name="return-value---current"></a><span data-ttu-id="e8ea9-127">戻り値 - current</span><span class="sxs-lookup"><span data-stu-id="e8ea9-127">Return Value - current</span></span>

<span data-ttu-id="e8ea9-128">セット内で現在指定されている値。</span><span class="sxs-lookup"><span data-stu-id="e8ea9-128">The value that is currently pointed to in the set.</span></span>

### <a name="remarks---current"></a><span data-ttu-id="e8ea9-129">備考 - current</span><span class="sxs-lookup"><span data-stu-id="e8ea9-129">Remarks - current</span></span>

<span data-ttu-id="e8ea9-130">戻り値のタイプは、セット内の項目のタイプによって決まります。</span><span class="sxs-lookup"><span data-stu-id="e8ea9-130">The type of the return value is determined by the type of items in the set.</span></span> <span data-ttu-id="e8ea9-131">現在のメソッドを呼び出す前に、SetEnumerator.moveNext メソッドを呼び出す必要があります。</span><span class="sxs-lookup"><span data-stu-id="e8ea9-131">You must call the SetEnumerator.moveNext method before you call the current method.</span></span>

## <a name="method-definitionstring"></a><span data-ttu-id="e8ea9-132">メソッド definitionString</span><span class="sxs-lookup"><span data-stu-id="e8ea9-132">Method definitionString</span></span>

<span data-ttu-id="e8ea9-133">列挙子の説明を返します。</span><span class="sxs-lookup"><span data-stu-id="e8ea9-133">Returns a description of the enumerator.</span></span>

```xpp
public str definitionString()
```

### <a name="return-value---definitionstring"></a><span data-ttu-id="e8ea9-134">戻り値 - definitionString</span><span class="sxs-lookup"><span data-stu-id="e8ea9-134">Return Value - definitionString</span></span>

<span data-ttu-id="e8ea9-135">列挙子の説明を含む文字列。</span><span class="sxs-lookup"><span data-stu-id="e8ea9-135">A string that contains a description of the enumerator.</span></span>

### <a name="remarks---definitionstring"></a><span data-ttu-id="e8ea9-136">備考 - definitionString</span><span class="sxs-lookup"><span data-stu-id="e8ea9-136">Remarks - definitionString</span></span>

<span data-ttu-id="e8ea9-137">たとえば、整数のセットの列挙子は、int セット列挙子を返します。</span><span class="sxs-lookup"><span data-stu-id="e8ea9-137">For example, an enumerator for a set of integers would return "int set enumerator".</span></span>

### <a name="examples---definitionstring"></a><span data-ttu-id="e8ea9-138">例 - definitionString</span><span class="sxs-lookup"><span data-stu-id="e8ea9-138">Examples - definitionString</span></span>

<span data-ttu-id="e8ea9-139">次の例では、セットとそのセットの列挙子を作成します。</span><span class="sxs-lookup"><span data-stu-id="e8ea9-139">The following example creates a set and an enumerator for the set.</span></span> <span data-ttu-id="e8ea9-140">definitionString メソッドを使用して、列挙子の説明を出力します。</span><span class="sxs-lookup"><span data-stu-id="e8ea9-140">The definitionString method is used to print a description of the enumerator.</span></span>

```xpp
{ 
    Set mySet = new Set(Types::Integer); 
    SetEnumerator enumerator; 
    int i; 
    // Add some elements to the set. 
   for (i = 0; i < 10; i++) 
    { 
        mySet.add(i); 
    } 
    // Set the enumerator. 
    enumerator = mySet.getEnumerator(); 
    print enumerator.definitionString(); 
    pause; 
}
```

## <a name="method-movenext"></a><span data-ttu-id="e8ea9-141">メソッド moveNext</span><span class="sxs-lookup"><span data-stu-id="e8ea9-141">Method moveNext</span></span>

<span data-ttu-id="e8ea9-142">列挙子が有効なセット要素を示すかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="e8ea9-142">Determines whether the enumerator denotes a valid set element.</span></span>

```xpp
public boolean moveNext()
```

### <a name="return-value---movenext"></a><span data-ttu-id="e8ea9-143">戻り値 - moveNext</span><span class="sxs-lookup"><span data-stu-id="e8ea9-143">Return Value - moveNext</span></span>

<span data-ttu-id="e8ea9-144">セット内の現在の職位が有効な要素を保持している場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="e8ea9-144">true if the current position in the set holds a valid element; otherwise, false.</span></span>

### <a name="remarks---movenext"></a><span data-ttu-id="e8ea9-145">備考 - moveNext</span><span class="sxs-lookup"><span data-stu-id="e8ea9-145">Remarks - moveNext</span></span>

<span data-ttu-id="e8ea9-146">セット列挙子は、セットの最初の要素の前に開始します。</span><span class="sxs-lookup"><span data-stu-id="e8ea9-146">Set enumerators start before the first element in the set.</span></span> <span data-ttu-id="e8ea9-147">セットの最初の要素を指すようにするために moveNext メソッドを呼び出す必要があります。</span><span class="sxs-lookup"><span data-stu-id="e8ea9-147">You must call the moveNext method to make it point to the first element in the set.</span></span>

## <a name="method-tostring"></a><span data-ttu-id="e8ea9-148">メソッド toString</span><span class="sxs-lookup"><span data-stu-id="e8ea9-148">Method toString</span></span>

<span data-ttu-id="e8ea9-149">列挙子が現在ポイントしているセット内の要素の内容の説明を取得します。</span><span class="sxs-lookup"><span data-stu-id="e8ea9-149">Retrieves a description of the contents of the element in the set that the enumerator currently points to.</span></span>

```xpp
public str toString()
```

### <a name="return-value---tostring"></a><span data-ttu-id="e8ea9-150">戻り値 - toString</span><span class="sxs-lookup"><span data-stu-id="e8ea9-150">Return Value - toString</span></span>

<span data-ttu-id="e8ea9-151">設定の現在の要素の説明を含む文字列。</span><span class="sxs-lookup"><span data-stu-id="e8ea9-151">A string that contains a description of the current element in the set.</span></span>

### <a name="examples---tostring"></a><span data-ttu-id="e8ea9-152">例 - toString</span><span class="sxs-lookup"><span data-stu-id="e8ea9-152">Examples - toString</span></span>

<span data-ttu-id="e8ea9-153">次の例では、整数のセットを作成し、最初の要素と 2 番目の要素の内容をセットに出力します。</span><span class="sxs-lookup"><span data-stu-id="e8ea9-153">The following example creates a set of integers, and then prints the content of the first and second elements in the set.</span></span>

```xpp
{ 
    Set mySet = new Set(Types::Integer); 
    SetEnumerator  enumerator; 
    int i; 
     // Add some elements to the set. 
    for (i = 0; i < 10; i++) 
    { 
        mySet.add(i); 
    } 
    // Set the enumerator. 
    enumerator = mySet.getEnumerator(); 
    // Go to the beginning of the enumerator. 
    enumerator.reset(); 
    // Go to the first element in the set. 
    enumerator.moveNext(); 
    // Print the first item in the set. 
    print enumerator.toString(); 
    pause; 
    enumerator.moveNext(); 
    // Print the second element in the set. 
    print enumerator.toString(); 
    pause; 
}
```

## <a name="method-reset"></a><span data-ttu-id="e8ea9-154">メソッド reset</span><span class="sxs-lookup"><span data-stu-id="e8ea9-154">Method reset</span></span>

<span data-ttu-id="e8ea9-155">列挙子をセットの先頭に移動します。</span><span class="sxs-lookup"><span data-stu-id="e8ea9-155">Moves the enumerator to the start of the set.</span></span>

```xpp
public void reset()
```

### <a name="remarks---reset"></a><span data-ttu-id="e8ea9-156">備考 - reset</span><span class="sxs-lookup"><span data-stu-id="e8ea9-156">Remarks - reset</span></span>

<span data-ttu-id="e8ea9-157">reset メソッドは、列挙子をセットの先頭、セットの最初の要素の前に移動します。</span><span class="sxs-lookup"><span data-stu-id="e8ea9-157">The reset method moves the enumerator to the start of the set, in front of the first element in the set.</span></span> <span data-ttu-id="e8ea9-158">セットの最初の要素を指すようにするために SetEnumerator.moveNext メソッドを呼び出す必要があります。</span><span class="sxs-lookup"><span data-stu-id="e8ea9-158">You must call the SetEnumerator.moveNext method to make it point to the first element in the set.</span></span>

### <a name="examples---reset"></a><span data-ttu-id="e8ea9-159">例 - reset</span><span class="sxs-lookup"><span data-stu-id="e8ea9-159">Examples - reset</span></span>

<span data-ttu-id="e8ea9-160">次の例では、セット作成し、そのセットの列挙子を作成します。</span><span class="sxs-lookup"><span data-stu-id="e8ea9-160">The following example creates a set and then creates an enumerator for the set.</span></span> <span data-ttu-id="e8ea9-161">reset メソッドを使用してセットの先頭に移動し、moveNext メソッドを使用してセットの最初の要素に移動します。</span><span class="sxs-lookup"><span data-stu-id="e8ea9-161">It uses the reset method to move to the start of the set and then uses the moveNext method to move to the first element in the set.</span></span>

```xpp
{ 
    Set mySet = new Set(Types::Integer); 
    SetEnumerator  enumerator; 
    int i; 
     // Add some elements to the set. 
    for (i = 0; i < 10; i++) 
    { 
        mySet.add(i); 
    } 
    // Set the enumerator. 
    enumerator = mySet.getEnumerator(); 
    // Go to beginning of enumerator. 
    enumerator.reset(); 
    // Go to the first element in the set. 
    enumerator.moveNext(); 
    // Print the first item in the set. 
    print enumerator.toString(); 
    pause; 
}
```

