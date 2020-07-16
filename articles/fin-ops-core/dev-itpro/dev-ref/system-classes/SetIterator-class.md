---
title: SetIterator クラス
description: このトピックでは、SetIterator クラスについて説明します。
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
ms.openlocfilehash: c2a1fef139dee2773f94d8581e2509ef4bb70e79
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502803"
---
# <a name="class-setiterator"></a><span data-ttu-id="672a2-103">クラス SetIterator</span><span class="sxs-lookup"><span data-stu-id="672a2-103">Class SetIterator</span></span>

[!include [banner](../../includes/banner.md)]

```xpp
class SetIterator extends Object
```

<span data-ttu-id="672a2-104">SetIterator クラスを使用すると、セット内の要素を反復処理できます。</span><span class="sxs-lookup"><span data-stu-id="672a2-104">The SetIterator class allows you to iterate over the elements in a set.</span></span>

## <a name="remarks"></a><span data-ttu-id="672a2-105">備考</span><span class="sxs-lookup"><span data-stu-id="672a2-105">Remarks</span></span>

<span data-ttu-id="672a2-106">セットの反復子は、反復処理する対象となるセットにポインターとして表示することができます。</span><span class="sxs-lookup"><span data-stu-id="672a2-106">Set iterators may be viewed as pointers into the sets over which they iterate.</span></span> <span data-ttu-id="672a2-107">繰り返しを開始し、より多くの要素が利用可能であるかどうかを決定し、さらに繰り返しによりポイントされる要素をフェッチする機能が利用可能です。</span><span class="sxs-lookup"><span data-stu-id="672a2-107">Functionality is available to start the iteration, to determine whether more elements are available, and to fetch the element pointed to by the iterator.</span></span> <span data-ttu-id="672a2-108">新しく作成されるセット反復子は、セットの最初の要素に配置されます。</span><span class="sxs-lookup"><span data-stu-id="672a2-108">Newly created set iterators are positioned at the first element in the set.</span></span> <span data-ttu-id="672a2-109">繰り返し中に要素が出現する順序は、要素が挿入される順序ではなく、要素の順序によって定義されます。</span><span class="sxs-lookup"><span data-stu-id="672a2-109">The order in which the elements occur during iteration is defined not by the sequence in which the elements are inserted, but by the ordering of the elements.</span></span> <span data-ttu-id="672a2-110">より下位の値の要素は、上位の値の要素の前に表示されます。</span><span class="sxs-lookup"><span data-stu-id="672a2-110">Elements with lower values appear before elements with higher values.</span></span> <span data-ttu-id="672a2-111">型の通常の順序が使用されます。</span><span class="sxs-lookup"><span data-stu-id="672a2-111">The usual ordering for the types is used.</span></span> <span data-ttu-id="672a2-112">構成要素がオブジェクトである場合、順序を指定するのにオブジェクトのアドレスが使用されます。</span><span class="sxs-lookup"><span data-stu-id="672a2-112">If the constituent elements are objects; however, the addresses of the objects are used to supply the ordering.</span></span> <span data-ttu-id="672a2-113">特定の注文が推測される可能性はありません。</span><span class="sxs-lookup"><span data-stu-id="672a2-113">No specific ordering may consequently be inferred.</span></span> <span data-ttu-id="672a2-114">オブジェクトのアドレスは、本来、一時的です。</span><span class="sxs-lookup"><span data-stu-id="672a2-114">The addresses of the objects are transient by nature.</span></span> <span data-ttu-id="672a2-115">SetIterator クラスではなく、そのクラスを使用することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="672a2-115">It is best practice to use the class instead of the SetIterator class.</span></span> <span data-ttu-id="672a2-116">これにより、別の層の反復子を使用して 1 つの層のセットにアクセスする場合に問題を回避できます。</span><span class="sxs-lookup"><span data-stu-id="672a2-116">This avoids problems if you are accessing the set on one tier with an iterator on another tier.</span></span> <span data-ttu-id="672a2-117">セット反復子および反復処理するセットは、同じクライアント/サーバー側にある必要があります。</span><span class="sxs-lookup"><span data-stu-id="672a2-117">Set iterators and the sets over which they iterate must be on the same client/server side.</span></span> <span data-ttu-id="672a2-118">SetIterator を使用し、コードが Called from としてマークされている場合、セットと反復子が別の層で終了しており、コードが失敗する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="672a2-118">If you use SetIterator and code is marked as Called from, it is possible that the set and the iterator will end up on different tiers, and the code will fail.</span></span> <span data-ttu-id="672a2-119">SetEnumerator を使用する場合、列挙子はセットと同じ層に自動的に作成されます。</span><span class="sxs-lookup"><span data-stu-id="672a2-119">If you use SetEnumerator, the enumerator is automatically created on the same tier as the set.</span></span> <span data-ttu-id="672a2-120">また、セット内の次のアイテムに移動するには、反復子セットを使用している場合は、より多くのメソッドと次のメソッドを明示的に呼び出す必要があります。</span><span class="sxs-lookup"><span data-stu-id="672a2-120">Also, to move to the next item in a set, you must explicitly call the more and next methods if you are using a set iterator.</span></span> <span data-ttu-id="672a2-121">SetEnumerator を使用する場合、moveNext メソッドを呼び出すだけです。</span><span class="sxs-lookup"><span data-stu-id="672a2-121">If you use SetEnumerator, you only have to call moveNext method.</span></span>

## <a name="examples"></a><span data-ttu-id="672a2-122">例</span><span class="sxs-lookup"><span data-stu-id="672a2-122">Examples</span></span>

<span data-ttu-id="672a2-123">次の例では、整数のセットを作成し、4 つの値をその中に追加します。</span><span class="sxs-lookup"><span data-stu-id="672a2-123">The following example creates a set of integers and then adds four values to it.</span></span> <span data-ttu-id="672a2-124">各セット要素に関する情報を出力しているセットを通じて反復処理します。</span><span class="sxs-lookup"><span data-stu-id="672a2-124">It then iterates through the set that is printing out information about each set element.</span></span>

```xpp
    Set s1 = new Set (Types::Integer); 
    int theElement; 
    SetIterator it; 
    ; 
    // Add some elements. 
    s1.add(3); 
    s1.add(4); 
    s1.add(13); 
    s1.add(1); 
    // Start a traversal of the elements in the set. 
    it = new SetIterator(s1); 
    // Prints "(begin)[1]". 
    print it.toString(); 
    // The elements are fetched in the order: 1, 3, 4, 13. 
    while (it.more()) 
    { 
        theElement = it.value(); 
        print theElement; 
         // Fetch the next element. 
        it.next(); 
    } 
    pause; 
}
```

## <a name="methods"></a><span data-ttu-id="672a2-125">メソッド</span><span class="sxs-lookup"><span data-stu-id="672a2-125">Methods</span></span>

| <span data-ttu-id="672a2-126">方法</span><span class="sxs-lookup"><span data-stu-id="672a2-126">Method</span></span>                        | <span data-ttu-id="672a2-127">説明</span><span class="sxs-lookup"><span data-stu-id="672a2-127">Description</span></span>                                                                                            |
|-------------------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="672a2-128">public str definitionString()</span><span class="sxs-lookup"><span data-stu-id="672a2-128">public str definitionString()</span></span> | <span data-ttu-id="672a2-129">反復子のタイプのテキスト表現を返します。</span><span class="sxs-lookup"><span data-stu-id="672a2-129">Returns a textual representation of the type of the iterator.</span></span>                                          |
| <span data-ttu-id="672a2-130">public boolean more()</span><span class="sxs-lookup"><span data-stu-id="672a2-130">public boolean more()</span></span>         | <span data-ttu-id="672a2-131">反復子が有効なセット要素を示すかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="672a2-131">Determines whether the iterator denotes a valid set element.</span></span>                                           |
| <span data-ttu-id="672a2-132">public str toString()</span><span class="sxs-lookup"><span data-stu-id="672a2-132">public str toString()</span></span>         | <span data-ttu-id="672a2-133">反復子によりポイントされているセット内の現在の要素のテキスト形式を返します。</span><span class="sxs-lookup"><span data-stu-id="672a2-133">Returns a textual representation of the current element in the set that is pointed to by the iterator.</span></span> |
| <span data-ttu-id="672a2-134">public AnyType value()</span><span class="sxs-lookup"><span data-stu-id="672a2-134">public AnyType value()</span></span>        | <span data-ttu-id="672a2-135">反復子がポイントしている値を取得します。</span><span class="sxs-lookup"><span data-stu-id="672a2-135">Retrieves the value that the iterator is pointing to.</span></span>                                                  |
| <span data-ttu-id="672a2-136">public void next()</span><span class="sxs-lookup"><span data-stu-id="672a2-136">public void next()</span></span>            | <span data-ttu-id="672a2-137">次の要素に反復子を移動します。</span><span class="sxs-lookup"><span data-stu-id="672a2-137">Moves the iterator to the next element.</span></span>                                                                |
| <span data-ttu-id="672a2-138">public void new(Set set)</span><span class="sxs-lookup"><span data-stu-id="672a2-138">public void new(Set set)</span></span>      | <span data-ttu-id="672a2-139">セットに対する新しい反復子を作成します。</span><span class="sxs-lookup"><span data-stu-id="672a2-139">Creates a new iterator for a set.</span></span>                                                                      |
| <span data-ttu-id="672a2-140">public void begin()</span><span class="sxs-lookup"><span data-stu-id="672a2-140">public void begin()</span></span>           | <span data-ttu-id="672a2-141">反復子をセットの先頭に移動します。</span><span class="sxs-lookup"><span data-stu-id="672a2-141">Moves the iterator to the start of the set.</span></span>                                                            |
| <span data-ttu-id="672a2-142">public void delete()</span><span class="sxs-lookup"><span data-stu-id="672a2-142">public void delete()</span></span>          | <span data-ttu-id="672a2-143">セットの反復子によってポイントされている要素を削除します。</span><span class="sxs-lookup"><span data-stu-id="672a2-143">Removes the element that is pointed to by the iterator of the set.</span></span>                                     |
| <span data-ttu-id="672a2-144">public void end()</span><span class="sxs-lookup"><span data-stu-id="672a2-144">public void end()</span></span>             | <span data-ttu-id="672a2-145">セットで最後の要素の後に反復子を移動します。</span><span class="sxs-lookup"><span data-stu-id="672a2-145">Moves the iterator past the last element in the set.</span></span>                                                   |

## <a name="method-definitionstring"></a><span data-ttu-id="672a2-146">メソッド definitionString</span><span class="sxs-lookup"><span data-stu-id="672a2-146">Method definitionString</span></span>

<span data-ttu-id="672a2-147">反復子のタイプのテキスト表現を返します。</span><span class="sxs-lookup"><span data-stu-id="672a2-147">Returns a textual representation of the type of the iterator.</span></span>

```xpp
public str definitionString()
```

### <a name="return-value---definitionstring"></a><span data-ttu-id="672a2-148">戻り値 - definitionString</span><span class="sxs-lookup"><span data-stu-id="672a2-148">Return Value - definitionString</span></span>

<span data-ttu-id="672a2-149">反復子のタイプを示す文字列。</span><span class="sxs-lookup"><span data-stu-id="672a2-149">A string that indicates the type of the iterator.</span></span>

## <a name="method-more"></a><span data-ttu-id="672a2-150">メソッド more</span><span class="sxs-lookup"><span data-stu-id="672a2-150">Method more</span></span>

<span data-ttu-id="672a2-151">反復子が有効なセット要素を示すかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="672a2-151">Determines whether the iterator denotes a valid set element.</span></span>

```xpp
public boolean more()
```

### <a name="return-value---more"></a><span data-ttu-id="672a2-152">戻り値 - more</span><span class="sxs-lookup"><span data-stu-id="672a2-152">Return Value - more</span></span>

<span data-ttu-id="672a2-153">反復子が有効な要素を表す場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="672a2-153">true if the iterator denotes a valid element; otherwise, false.</span></span>

### <a name="remarks---more"></a><span data-ttu-id="672a2-154">備考 - more</span><span class="sxs-lookup"><span data-stu-id="672a2-154">Remarks - more</span></span>

<span data-ttu-id="672a2-155">このメソッドが false を返すときに反復子が指す要素にアクセスしようとするとエラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="672a2-155">Attempting to access an element that is pointed to by an iterator when this method returns false will result in an error.</span></span> <span data-ttu-id="672a2-156">このメソッドは、反復子が有効な要素を指しているかどうかだけをチェックします。</span><span class="sxs-lookup"><span data-stu-id="672a2-156">This method will check only whether the iterator points to a valid element.</span></span> <span data-ttu-id="672a2-157">セットにより多くの要素があるかどうかは確認されません。</span><span class="sxs-lookup"><span data-stu-id="672a2-157">It will not check whether there are more elements in the set.</span></span>

### <a name="examples---more"></a><span data-ttu-id="672a2-158">例 - more</span><span class="sxs-lookup"><span data-stu-id="672a2-158">Examples - more</span></span>

<span data-ttu-id="672a2-159">次の例では、SetIterator.more メソッドを使用して、while ループを実行する前にセット内に要素があるかどうかを確認します。これにより、奇数要素がすべてセットから削除されます。</span><span class="sxs-lookup"><span data-stu-id="672a2-159">The following example uses the SetIterator.more method to check whether there are more elements in the set before it runs through the while loop, which deletes all the odd elements from the set.</span></span>

```xpp
{ 
    Set iset = new Set (Types::Integer); 
    SetIterator it; 
    int i; 
    ; 
    for (i = 1; i <= 10; i++) 
    { 
        iset.add(i); 
    } 
    // Delete all odd elements 
    it = new SetIterator(iset); 
    while (it.more()) 
    { 
        if (it.value() mod 2 != 0) 
        { 
            // The value is odd. Delete and skip to next element. 
            it.delete(); 
        } 
        else 
        { 
            it.next(); 
        } 
    } 
    print iset.toString(); 
    pause; 
}
```

## <a name="method-tostring"></a><span data-ttu-id="672a2-160">メソッド toString</span><span class="sxs-lookup"><span data-stu-id="672a2-160">Method toString</span></span>

<span data-ttu-id="672a2-161">反復子によりポイントされているセット内の現在の要素のテキスト形式を返します。</span><span class="sxs-lookup"><span data-stu-id="672a2-161">Returns a textual representation of the current element in the set that is pointed to by the iterator.</span></span>

```xpp
public str toString()
```

### <a name="return-value---tostring"></a><span data-ttu-id="672a2-162">戻り値 - toString</span><span class="sxs-lookup"><span data-stu-id="672a2-162">Return Value - toString</span></span>

<span data-ttu-id="672a2-163">設定の現在の要素のテキスト形式表記である文字列。</span><span class="sxs-lookup"><span data-stu-id="672a2-163">A string that is the textual representation of the current element in the set.</span></span>

### <a name="remarks---tostring"></a><span data-ttu-id="672a2-164">備考 - toString</span><span class="sxs-lookup"><span data-stu-id="672a2-164">Remarks - toString</span></span>

<span data-ttu-id="672a2-165">反復子がセット内の最初の要素を指している場合、その文字列には "(開始)\[値\]" という形式の指示が含まれます。反復子が要素を指していない場合(つまり、more() が false を返す場合)、返される文字列は "(終了)" になります。反復子が値を指す場合、文字列は "\[値\]" になります。値は要素値の文字列表現です。</span><span class="sxs-lookup"><span data-stu-id="672a2-165">If the iterator points to the first element in the set, the string will contain an indication of this, in the following format: "(begin)\[value\]" If the iterator does not point to an element (that is, if more() returns false), the string returned is: "(end)" If the iterator points to a value the string is: "\[value\]" where value is a string representation of the element value.</span></span>

### <a name="examples---tostring"></a><span data-ttu-id="672a2-166">例 - toString</span><span class="sxs-lookup"><span data-stu-id="672a2-166">Examples - toString</span></span>

<span data-ttu-id="672a2-167">次の例では、SetIterator.toString メソッドを使用して、反復子がセットのスキャンを開始する前にポイントする、そのセットの値の説明を出力します。</span><span class="sxs-lookup"><span data-stu-id="672a2-167">The following example uses the SetIterator.toString method to print a description of the value in the set that the iterator points to before it starts traversing the set.</span></span>

```xpp
{ 
    Set s1 = new Set (Types::Integer); 
    int theElement; 
    SetIterator it; 
    // Add some elements 
    s1.add(3); 
    s1.add(4); 
    s1.add(13); 
    s1.add(1);  
    // Start a traversal of the elements in the set 
    it = new SetIterator(s1); 
    // The elements are fetched in the order: 1, 3, 4, 13 
    print it.toString(); // Prints "(begin)[1]" 
    while (it.more()) 
    { 
        theElement = it.value(); 
        print theElement; 
        // Fetch the next element 
        it.next(); 
    } 
    pause; 
}
```

## <a name="method-value"></a><span data-ttu-id="672a2-168">メソッド value</span><span class="sxs-lookup"><span data-stu-id="672a2-168">Method value</span></span>

<span data-ttu-id="672a2-169">反復子がポイントしている値を取得します。</span><span class="sxs-lookup"><span data-stu-id="672a2-169">Retrieves the value that the iterator is pointing to.</span></span>

```xpp
public AnyType value()
```

### <a name="return-value---value"></a><span data-ttu-id="672a2-170">戻り値 - value</span><span class="sxs-lookup"><span data-stu-id="672a2-170">Return Value - value</span></span>

<span data-ttu-id="672a2-171">反復子で示される値。</span><span class="sxs-lookup"><span data-stu-id="672a2-171">The value denoted by the iterator.</span></span>

### <a name="remarks---value"></a><span data-ttu-id="672a2-172">備考 - value</span><span class="sxs-lookup"><span data-stu-id="672a2-172">Remarks - value</span></span>

<span data-ttu-id="672a2-173">SetIterator.more を使用して、set 要素のキー値を取得する前に要素が存在するかどうかを確認します。</span><span class="sxs-lookup"><span data-stu-id="672a2-173">Use SetIterator.more to check whether an element exists before trying to retrieve the key value of the set element.</span></span>

### <a name="examples---value"></a><span data-ttu-id="672a2-174">例 - value</span><span class="sxs-lookup"><span data-stu-id="672a2-174">Examples - value</span></span>

<span data-ttu-id="672a2-175">次の例では、SetIterator.value メソッドを使用して、セット内の現在の項目の値を出力します。</span><span class="sxs-lookup"><span data-stu-id="672a2-175">The following example uses the SetIterator.value method to print the value of the current item in the set.</span></span>

```xpp
{ 
    Set s1 = new Set (Types::Integer); 
    SetIterator it; 
    // Add some elements 
    s1.add(3); 
    s1.add(4); 
    s1.add(13); 
    s1.add(1);  
    // Start a traversal of the elements in the set 
    it = new SetIterator(s1); 
    // Prints "(begin)[1]" 
    print it.toString();  
    // The elements are fetched in the order: 1, 3, 4, 13 
    while (it.more()) 
    { 
        print it.value(); 
        // Fetch the next element 
        it.next(); 
    } 
    pause; 
}
```

## <a name="method-next"></a><span data-ttu-id="672a2-176">メソッド next</span><span class="sxs-lookup"><span data-stu-id="672a2-176">Method next</span></span>

<span data-ttu-id="672a2-177">次の要素に反復子を移動します。</span><span class="sxs-lookup"><span data-stu-id="672a2-177">Moves the iterator to the next element.</span></span>

```xpp
public void next()
```

### <a name="remarks---next"></a><span data-ttu-id="672a2-178">備考 - next</span><span class="sxs-lookup"><span data-stu-id="672a2-178">Remarks - next</span></span>

<span data-ttu-id="672a2-179">SetIterator.more を使用して、反復子が有効な要素を指しているかどうかを判断します。</span><span class="sxs-lookup"><span data-stu-id="672a2-179">Use SetIterator.more to determine whether the iterator points to a valid element.</span></span>

### <a name="examples---next"></a><span data-ttu-id="672a2-180">例 - next</span><span class="sxs-lookup"><span data-stu-id="672a2-180">Examples - next</span></span>

<span data-ttu-id="672a2-181">次の例では、SetIterator.next メソッドを使用して、反復子をセット内の次の要素に移動し、別の要素が存在するかどうかをテストし、別の要素がある場合はその値をコンテナーに追加します。</span><span class="sxs-lookup"><span data-stu-id="672a2-181">The following example uses the SetIterator.next method to move the iterator to the next element in the set, before testing whether there is another element, and if there is another element, adding the value to a container.</span></span>

```xpp
static public void saveSequence(classId _classId, Set _sequence) 
{ 
    SysCheckListItemTable sysCheckListItemTable; 
    SetIterator           si; 
    container             con = connull(); 
    if (_sequence) 
    { 
        si = new SetIterator(_sequence); 
        si.begin(); 
        while (si.more()) 
        { 
             con += si.value(); 
             si.next(); 
        } 
    } 
    //... 
}
```

## <a name="method-new"></a><span data-ttu-id="672a2-182">メソッド new</span><span class="sxs-lookup"><span data-stu-id="672a2-182">Method new</span></span>

<span data-ttu-id="672a2-183">セットに対する新しい反復子を作成します。</span><span class="sxs-lookup"><span data-stu-id="672a2-183">Creates a new iterator for a set.</span></span>

```xpp
public void new(Set set)
```

### <a name="parameters---new"></a><span data-ttu-id="672a2-184">パラメーター - new</span><span class="sxs-lookup"><span data-stu-id="672a2-184">Parameters - new</span></span>

<span data-ttu-id="672a2-185">set</span><span class="sxs-lookup"><span data-stu-id="672a2-185">set</span></span>  
<span data-ttu-id="672a2-186">繰り返し処理するセット。</span><span class="sxs-lookup"><span data-stu-id="672a2-186">The set to iterate over.</span></span>

### <a name="remarks---new"></a><span data-ttu-id="672a2-187">備考 - new</span><span class="sxs-lookup"><span data-stu-id="672a2-187">Remarks - new</span></span>

<span data-ttu-id="672a2-188">反復子は、セットが空でない場合、セットの最初の値に配置されます。</span><span class="sxs-lookup"><span data-stu-id="672a2-188">The iterator is positioned at the first value in the set, if the set is not empty.</span></span>

### <a name="examples---new"></a><span data-ttu-id="672a2-189">例 - new</span><span class="sxs-lookup"><span data-stu-id="672a2-189">Examples - new</span></span>

<span data-ttu-id="672a2-190">次の例では、整数のセットを作成し、セットの反復子を作成します。</span><span class="sxs-lookup"><span data-stu-id="672a2-190">The following example creates a set of integers and then creates an iterator for that set</span></span>

```xpp
Set s1 = new Set (Types::Integer); 
SetIterator it; 
it = new SetIterator(s1);
```

## <a name="method-begin"></a><span data-ttu-id="672a2-191">メソッド begin</span><span class="sxs-lookup"><span data-stu-id="672a2-191">Method begin</span></span>

<span data-ttu-id="672a2-192">反復子をセットの先頭に移動します。</span><span class="sxs-lookup"><span data-stu-id="672a2-192">Moves the iterator to the start of the set.</span></span>

```xpp
public void begin()
```

### <a name="remarks---begin"></a><span data-ttu-id="672a2-193">備考 - begin</span><span class="sxs-lookup"><span data-stu-id="672a2-193">Remarks - begin</span></span>

<span data-ttu-id="672a2-194">新しく作成されるセット反復子は、セットの最初の要素に配置されます。</span><span class="sxs-lookup"><span data-stu-id="672a2-194">Newly created set iterators are positioned at the first element in the set.</span></span> <span data-ttu-id="672a2-195">通常はセットを反復処理する前に begin メソッドを呼び出す必要はありません。後でポインタをリセットしたい場合にのみ、その操作を行う必要があります。</span><span class="sxs-lookup"><span data-stu-id="672a2-195">Typically, you do not need to call the begin method before you start to iterate through the set; you need to do that only if you want to reset the pointer later on.</span></span>

### <a name="examples---begin"></a><span data-ttu-id="672a2-196">例 - begin</span><span class="sxs-lookup"><span data-stu-id="672a2-196">Examples - begin</span></span>

<span data-ttu-id="672a2-197">次の例では、指定されたインターフェイス、つまり \_id クラスを実装するクラスのクラス ID のセットを返します。</span><span class="sxs-lookup"><span data-stu-id="672a2-197">The following example returns set of class IDs of the classes that implement the specified interface, that is, the \_id class.</span></span> <span data-ttu-id="672a2-198">スーパークラスの場合、反復子は設定からクラスを削除するために使用され、\_onlyLeafClasses パラメーターは true に設定されます。</span><span class="sxs-lookup"><span data-stu-id="672a2-198">An iterator is used to remove classes from the set if they are superclasses, and the \_onlyLeafClasses parameter is set to true.</span></span> <span data-ttu-id="672a2-199">開始メソッドを使用して、セットからスーパークラスが削除された後に反復子をリセットします。</span><span class="sxs-lookup"><span data-stu-id="672a2-199">The begin method is used to reset the iterator after the superclasses have been removed from the set.</span></span>

```xpp
public static Set getImplements( 
    classId _id,  
    boolean _onlyLeafClasses = true) 
{ 
    Dictionary dictionary = new Dictionary(); 
    SysDictClass sysDictClass; 
    boolean removed; 
    Set set = new Set(Types::Integer); 
    SetIterator setIterator = new SetIterator(set); 
    int i; 
    for (i=1;i<=dictionary.classCnt();i++) 
    { 
        sysDictClass = new SysDictClass(dictionary.classCnt2Id(i)); 
        if (sysDictClass.isImplementing(_id)) 
        { 
            set.add(sysDictClass.id()); 
        } 
    } 
    //No superclasses included in return set 
    if (_onlyLeafClasses) 
    { 
        // begin method not needed here; only for clarity 
        setIterator.begin();  
        while (setIterator.more()) 
        { 
            removed = false; 
            sysDictClass = new SysDictClass(setIterator.value()); 
            while (sysDictClass.extend()) 
            { 
                removed = removed | set.remove(sysDictClass.extend()); 
                sysDictClass = new SysDictClass(sysDictClass.extend()); 
            } 
            if (removed) 
            { 
                // Restart search 
                setIterator.begin();  
            } 
            else 
            { 
                setIterator.next(); 
            } 
        } 
    } 
    return set; 
}
```

## <a name="method-delete"></a><span data-ttu-id="672a2-200">メソッド delete</span><span class="sxs-lookup"><span data-stu-id="672a2-200">Method delete</span></span>

<span data-ttu-id="672a2-201">セットの反復子によってポイントされている要素を削除します。</span><span class="sxs-lookup"><span data-stu-id="672a2-201">Removes the element that is pointed to by the iterator of the set.</span></span>

```xpp
public void delete()
```

### <a name="remarks---delete"></a><span data-ttu-id="672a2-202">備考 - delete</span><span class="sxs-lookup"><span data-stu-id="672a2-202">Remarks - delete</span></span>

<span data-ttu-id="672a2-203">反復子は、このメソッドを呼び出した後に次の要素を指します。</span><span class="sxs-lookup"><span data-stu-id="672a2-203">The iterator will point to the next element after calling this method.</span></span>

### <a name="examples---delete"></a><span data-ttu-id="672a2-204">例 - delete</span><span class="sxs-lookup"><span data-stu-id="672a2-204">Examples - delete</span></span>

<span data-ttu-id="672a2-205">次の例では、すべての奇数要素をセットから削除します。</span><span class="sxs-lookup"><span data-stu-id="672a2-205">The following example deletes all the odd elements from the set.</span></span>

```xpp
{ 
    Set iset = new Set (Types::Integer); 
    SetIterator it; 
    int i; 
    for (i = 1; i <= 10; i++) 
    { 
        iset.add(i); 
    } 
    // Delete all odd elements 
    it = new SetIterator(iset); 
    while (it.more()) 
    { 
        if (it.value() mod 2 != 0) 
        { 
            // The value is odd. Delete and skip to next element. 
            it.delete(); 
        } 
        else 
        { 
            it.next(); 
        } 
    } 
    print iset.toString(); 
    pause; 
}
```

## <a name="method-end"></a><span data-ttu-id="672a2-206">メソッド end</span><span class="sxs-lookup"><span data-stu-id="672a2-206">Method end</span></span>

<span data-ttu-id="672a2-207">セットで最後の要素の後に反復子を移動します。</span><span class="sxs-lookup"><span data-stu-id="672a2-207">Moves the iterator past the last element in the set.</span></span>

```xpp
public void end()
```

### <a name="remarks---end"></a><span data-ttu-id="672a2-208">備考 - end</span><span class="sxs-lookup"><span data-stu-id="672a2-208">Remarks - end</span></span>

<span data-ttu-id="672a2-209">このメソッドを実行した後、より多くのメソッドは false を返します。</span><span class="sxs-lookup"><span data-stu-id="672a2-209">After executing this method, the more method will return false.</span></span>

