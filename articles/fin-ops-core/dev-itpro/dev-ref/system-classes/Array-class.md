---
title: 配列クラス
description: このトピックでは、配列クラスについて説明します。
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
ms.openlocfilehash: 24f977b1e6d6936173f303c0eb582d0bdafb5c39
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502747"
---
# <a name="class-array"></a><span data-ttu-id="4cfbf-103">クラス配列</span><span class="sxs-lookup"><span data-stu-id="4cfbf-103">Class Array</span></span>

[!include [banner](../../includes/banner.md)]

```xpp
class Array extends Object
```

## <a name="remarks"></a><span data-ttu-id="4cfbf-104">備考</span><span class="sxs-lookup"><span data-stu-id="4cfbf-104">Remarks</span></span>

<span data-ttu-id="4cfbf-105">配列では、オブジェクトやレコードなど単一タイプの値を保持できます (X++ 言語に組み込まれている配列のデータ タイプとは異なります) 。</span><span class="sxs-lookup"><span data-stu-id="4cfbf-105">Arrays can hold values of any single type, such as objects and records (contrary to the array data type that is built into the X++ language).</span></span> <span data-ttu-id="4cfbf-106">このタイプのオブジェクトは、関数やメソッドに転送することができます。</span><span class="sxs-lookup"><span data-stu-id="4cfbf-106">Objects of this type can be transferred to functions and methods.</span></span> <span data-ttu-id="4cfbf-107">値は、順番に格納されます。</span><span class="sxs-lookup"><span data-stu-id="4cfbf-107">The values are stored sequentially.</span></span> <span data-ttu-id="4cfbf-108">配列は、必要に応じて展開されます。</span><span class="sxs-lookup"><span data-stu-id="4cfbf-108">The arrays expand as required.</span></span> <span data-ttu-id="4cfbf-109">したがって、配列の特定の分析コードは提供されません。</span><span class="sxs-lookup"><span data-stu-id="4cfbf-109">Therefore, no specific dimension of the array is supplied.</span></span>

## <a name="examples"></a><span data-ttu-id="4cfbf-110">例</span><span class="sxs-lookup"><span data-stu-id="4cfbf-110">Examples</span></span>

<span data-ttu-id="4cfbf-111">次の例では、クラスの配列を作成し、3 つのクエリ オブジェクトを配列に追加します。</span><span class="sxs-lookup"><span data-stu-id="4cfbf-111">The following example creates an array of classes and adds three query objects to the array.</span></span>

```xpp
{ 
    Array oarray = new Array (Types::Class); 
```

```xpp
    oarray.value(1, new query()); 
    oarray.value(2, new query()); 
    oarray.value(4, new query());  
    print oarray.toString(); 
    print oarray.definitionString(); 
    pause; 
}
```

## <a name="methods"></a><span data-ttu-id="4cfbf-112">メソッド</span><span class="sxs-lookup"><span data-stu-id="4cfbf-112">Methods</span></span>

| <span data-ttu-id="4cfbf-113">方法</span><span class="sxs-lookup"><span data-stu-id="4cfbf-113">Method</span></span>                                              | <span data-ttu-id="4cfbf-114">説明</span><span class="sxs-lookup"><span data-stu-id="4cfbf-114">Description</span></span>                                                                                         |
|-----------------------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4cfbf-115">public str definitionString()</span><span class="sxs-lookup"><span data-stu-id="4cfbf-115">public str definitionString()</span></span>                       | <span data-ttu-id="4cfbf-116">配列の定義を含む文字列を返します。</span><span class="sxs-lookup"><span data-stu-id="4cfbf-116">Returns a string that contains the definition of the array.</span></span>                                         |
| <span data-ttu-id="4cfbf-117">public boolean exists(int index)</span><span class="sxs-lookup"><span data-stu-id="4cfbf-117">public boolean exists(int index)</span></span>                    | <span data-ttu-id="4cfbf-118">特定の配列要素が有効かどうかを判定します。</span><span class="sxs-lookup"><span data-stu-id="4cfbf-118">Determines whether a particular array element is valid.</span></span>                                             |
| <span data-ttu-id="4cfbf-119">public int lastIndex()</span><span class="sxs-lookup"><span data-stu-id="4cfbf-119">public int lastIndex()</span></span>                              | <span data-ttu-id="4cfbf-120">配列に値を格納するために使用する最上位のインデックスを取得します。</span><span class="sxs-lookup"><span data-stu-id="4cfbf-120">Retrieves the highest index that is used to store a value in the array.</span></span>                             |
| <span data-ttu-id="4cfbf-121">public container pack()</span><span class="sxs-lookup"><span data-stu-id="4cfbf-121">public container pack()</span></span>                             | <span data-ttu-id="4cfbf-122">Array クラスの現在のインスタンスをシリアル化します。</span><span class="sxs-lookup"><span data-stu-id="4cfbf-122">Serializes the current instance of the Array class.</span></span>                                                 |
| <span data-ttu-id="4cfbf-123">public str toString()</span><span class="sxs-lookup"><span data-stu-id="4cfbf-123">public str toString()</span></span>                               | <span data-ttu-id="4cfbf-124">配列の内容を説明する文字列を返します。</span><span class="sxs-lookup"><span data-stu-id="4cfbf-124">Returns a string that describes the contents of the array.</span></span>                                          |
| <span data-ttu-id="4cfbf-125">public Types typeId()</span><span class="sxs-lookup"><span data-stu-id="4cfbf-125">public Types typeId()</span></span>                               | <span data-ttu-id="4cfbf-126">配列の値のデータ型を返します。</span><span class="sxs-lookup"><span data-stu-id="4cfbf-126">Returns the data type of the values in the array.</span></span>                                                   |
| <span data-ttu-id="4cfbf-127">public AnyType value(int index, \[AnyType arg\])</span><span class="sxs-lookup"><span data-stu-id="4cfbf-127">public AnyType value(int index, \[AnyType arg\])</span></span>    | <span data-ttu-id="4cfbf-128">指定したインデックスに格納される配列要素の値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="4cfbf-128">Gets or sets the value of the array element that is stored at the specified index.</span></span>                  |
| <span data-ttu-id="4cfbf-129">public str xml(\[int indent\])</span><span class="sxs-lookup"><span data-stu-id="4cfbf-129">public str xml(\[int indent\])</span></span>                      | <span data-ttu-id="4cfbf-130">現在のオブジェクトを表す XML 文字列を返します。</span><span class="sxs-lookup"><span data-stu-id="4cfbf-130">Returns an XML string that represents the current object.</span></span>                                           |
| <span data-ttu-id="4cfbf-131">::public static Array create(container container)</span><span class="sxs-lookup"><span data-stu-id="4cfbf-131">::public static Array create(container container)</span></span>   | <span data-ttu-id="4cfbf-132">以前の Array.pack メソッドの呼び出しで取得されるコンテナーから配列を作成します。</span><span class="sxs-lookup"><span data-stu-id="4cfbf-132">Creates an array from the container that is obtained from a previous call to the Array.pack method.</span></span> |
| <span data-ttu-id="4cfbf-133">::public static Array createFromXML(Object xmlnode)</span><span class="sxs-lookup"><span data-stu-id="4cfbf-133">::public static Array createFromXML(Object xmlnode)</span></span> |                                                                                                     |
| <span data-ttu-id="4cfbf-134">public void new(Types Type)</span><span class="sxs-lookup"><span data-stu-id="4cfbf-134">public void new(Types Type)</span></span>                         | <span data-ttu-id="4cfbf-135">各要素が指定されたタイプを持つ配列を作成します。</span><span class="sxs-lookup"><span data-stu-id="4cfbf-135">Creates an array in which each element has the specified type.</span></span>                                      |

## <a name="method-definitionstring"></a><span data-ttu-id="4cfbf-136">メソッド definitionString</span><span class="sxs-lookup"><span data-stu-id="4cfbf-136">Method definitionString</span></span>

<span data-ttu-id="4cfbf-137">配列の定義を含む文字列を返します。</span><span class="sxs-lookup"><span data-stu-id="4cfbf-137">Returns a string that contains the definition of the array.</span></span>

```xpp
public str definitionString()
```

### <a name="return-value---definitionstring"></a><span data-ttu-id="4cfbf-138">戻り値 - definitionString</span><span class="sxs-lookup"><span data-stu-id="4cfbf-138">Return Value - definitionString</span></span>

<span data-ttu-id="4cfbf-139">配列の定義を含む文字列。</span><span class="sxs-lookup"><span data-stu-id="4cfbf-139">A string that contains the definition of the array.</span></span>

### <a name="examples---definitionstring"></a><span data-ttu-id="4cfbf-140">例 - definitionString</span><span class="sxs-lookup"><span data-stu-id="4cfbf-140">Examples - definitionString</span></span>

<span data-ttu-id="4cfbf-141">次の例では、クラスの配列を作成し、3 つのクエリ オブジェクトを配列に追加します。</span><span class="sxs-lookup"><span data-stu-id="4cfbf-141">The following example creates an array of classes and then adds three query objects to the array.</span></span> <span data-ttu-id="4cfbf-142">definitionString メソッドを使用して、配列の定義を出力します。</span><span class="sxs-lookup"><span data-stu-id="4cfbf-142">It uses the definitionString method to print a definition of the array.</span></span>

```xpp
{ 
    Array oarray = new Array (Types::Class); 
```

```xpp
    oarray.value(1, new query()); 
    oarray.value(2, new query()); 
    oarray.value(4, new query());  
    print oarray.definitionString(); 
    pause; 
}
```

## <a name="method-exists"></a><span data-ttu-id="4cfbf-143">メソッド exists</span><span class="sxs-lookup"><span data-stu-id="4cfbf-143">Method exists</span></span>

<span data-ttu-id="4cfbf-144">特定の配列要素が有効かどうかを判定します。</span><span class="sxs-lookup"><span data-stu-id="4cfbf-144">Determines whether a particular array element is valid.</span></span>

```xpp
public boolean exists(int index)
```

### <a name="parameters---exists"></a><span data-ttu-id="4cfbf-145">パラメーター - exists</span><span class="sxs-lookup"><span data-stu-id="4cfbf-145">Parameters - exists</span></span>

<span data-ttu-id="4cfbf-146">指数</span><span class="sxs-lookup"><span data-stu-id="4cfbf-146">index</span></span>  
<span data-ttu-id="4cfbf-147">テスト対象の配列要素。</span><span class="sxs-lookup"><span data-stu-id="4cfbf-147">The array element to test.</span></span>

### <a name="return-value---exists"></a><span data-ttu-id="4cfbf-148">戻り値 - exists</span><span class="sxs-lookup"><span data-stu-id="4cfbf-148">Return Value - exists</span></span>

<span data-ttu-id="4cfbf-149">インデックスにより指定される配列要素が有効な場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="4cfbf-149">true if the array element that is pointed to by the index is valid; otherwise, false.</span></span>

### <a name="examples---exists"></a><span data-ttu-id="4cfbf-150">例 - exists</span><span class="sxs-lookup"><span data-stu-id="4cfbf-150">Examples - exists</span></span>

<span data-ttu-id="4cfbf-151">次の例では、exists メソッドを使用して、配列内のさまざまな要素が有効かどうかをテストします。</span><span class="sxs-lookup"><span data-stu-id="4cfbf-151">The following example uses the exists method to test whether various elements in an array are valid.</span></span>

```xpp
{ 
    array a = new array(types::Integer); 
```

```xpp
    a.value(1, 23); 
```

```xpp
    print a.value(1); 
    pause; 
    if (a.exists(7)) // No, only element 1 is initialized 
    { 
        print a.value(7); 
```

```xpp
    } 
    else  
    { 
        print "Value does not exist"; 
    } 
    pause; 
```

```xpp
    //Array positions 2 to 9 padded with default values 
    a.value(10, 55); 
```

```xpp
    if (a.exists(7)) // Yes, elements 1..10 now initialized 
    { 
        print a.value(7); 
    } 
    else  
    { 
        print "Value does not exist"; 
    } 
    pause; 
}
```

## <a name="method-lastindex"></a><span data-ttu-id="4cfbf-152">メソッド lastIndex</span><span class="sxs-lookup"><span data-stu-id="4cfbf-152">Method lastIndex</span></span>

<span data-ttu-id="4cfbf-153">配列に値を格納するために使用する最上位のインデックスを取得します。</span><span class="sxs-lookup"><span data-stu-id="4cfbf-153">Retrieves the highest index that is used to store a value in the array.</span></span>

```xpp
public int lastIndex()
```

### <a name="return-value---lastindex"></a><span data-ttu-id="4cfbf-154">戻り値 - lastIndex</span><span class="sxs-lookup"><span data-stu-id="4cfbf-154">Return Value - lastIndex</span></span>

<span data-ttu-id="4cfbf-155">値を格納するために使用する最上位のインデックスを表す整数。</span><span class="sxs-lookup"><span data-stu-id="4cfbf-155">An integer that represents the highest index that is used to store a value.</span></span>

### <a name="examples---lastindex"></a><span data-ttu-id="4cfbf-156">例 - lastIndex</span><span class="sxs-lookup"><span data-stu-id="4cfbf-156">Examples - lastIndex</span></span>

<span data-ttu-id="4cfbf-157">次の例では、lastIndex メソッドを使用して配列の最後の要素を見つけ、この要素の後に新しい値を追加します。</span><span class="sxs-lookup"><span data-stu-id="4cfbf-157">The following example uses the lastIndex method to find the last element in the array and then add a new value after this element.</span></span>

```xpp
{ 
    Array myArray = new Array(Types::Integer); 
    int newValue; 
```

```xpp
    // Other code - values are added to myArray 
    // and a value is assigned to newValue 
```

```xpp
    myArray.value(myArray.lastIndex()+1, newValue); 
}
```

## <a name="method-pack"></a><span data-ttu-id="4cfbf-158">メソッド pack</span><span class="sxs-lookup"><span data-stu-id="4cfbf-158">Method pack</span></span>

<span data-ttu-id="4cfbf-159">Array クラスの現在のインスタンスをシリアル化します。</span><span class="sxs-lookup"><span data-stu-id="4cfbf-159">Serializes the current instance of the Array class.</span></span>

```xpp
public container pack()
```

### <a name="return-value---pack"></a><span data-ttu-id="4cfbf-160">戻り値 - pack</span><span class="sxs-lookup"><span data-stu-id="4cfbf-160">Return Value - pack</span></span>

<span data-ttu-id="4cfbf-161">Array クラスの現在のインスタンスを含むコンテナーです。</span><span class="sxs-lookup"><span data-stu-id="4cfbf-161">A container that contains the current instance of the Array class.</span></span>

### <a name="remarks---pack"></a><span data-ttu-id="4cfbf-162">備考 - pack</span><span class="sxs-lookup"><span data-stu-id="4cfbf-162">Remarks - pack</span></span>

<span data-ttu-id="4cfbf-163">このメソッドで作成されたコンテナーには、配列の最初の要素の前に 3 つの要素が含まれます。</span><span class="sxs-lookup"><span data-stu-id="4cfbf-163">The container created by this method contains three elements before the first element from the array:</span></span>

-   <span data-ttu-id="4cfbf-164">コンテナのバージョン番号。</span><span class="sxs-lookup"><span data-stu-id="4cfbf-164">A version number for the container.</span></span>
-   <span data-ttu-id="4cfbf-165">配列要素のデータ型を識別する整数。</span><span class="sxs-lookup"><span data-stu-id="4cfbf-165">An integer that identifies the data type of the array elements.</span></span>
-   <span data-ttu-id="4cfbf-166">この配列の要素の数。</span><span class="sxs-lookup"><span data-stu-id="4cfbf-166">The number of elements in the array.</span></span>

<span data-ttu-id="4cfbf-167">配列の値がオブジェクトになっている場合は、各オブジェクトに対して pack メソッドが呼び出され、サブコンテナーを取得します。</span><span class="sxs-lookup"><span data-stu-id="4cfbf-167">If the values of the array are objects, the pack method is called on each object to yield a subcontainer.</span></span>

### <a name="examples---pack"></a><span data-ttu-id="4cfbf-168">例 - pack</span><span class="sxs-lookup"><span data-stu-id="4cfbf-168">Examples - pack</span></span>

<span data-ttu-id="4cfbf-169">次の例では、整数の配列を作成し、それにいくつかの値を追加します。</span><span class="sxs-lookup"><span data-stu-id="4cfbf-169">The following example creates an array of integers and adds some values to it.</span></span> <span data-ttu-id="4cfbf-170">pack メソッドを使用して配列をコンテナーにパックし、コンテナーを使用して新しい配列を作成します。</span><span class="sxs-lookup"><span data-stu-id="4cfbf-170">The pack method is used to pack the array into a container, and the container is then used to create a new array.</span></span>

```xpp
{ 
    int i; 
    container packedArray; 
    // Create an integer array 
    Array ia = new Array (Types::Integer); 
    Array iacopy; 
```

```xpp
    // Write some elements in it 
    for (i = 1; i< 10; i++) 
    { 
        ia.value(i, i*2); 
    } 
```

```xpp
    // Pack the array 
    packedArray = ia.pack(); 
```

```xpp
    // Unpack the array  
    iacopy = Array::create(packedArray); 
```

```xpp
    // Check the values 
    for (i = 1; i< 10; i++) 
    { 
        if (iacopy.value(i) != 2*i) 
        { 
            print "Error!"; 
        } 
    } 
    pause; 
}
```

## <a name="method-tostring"></a><span data-ttu-id="4cfbf-171">メソッド toString</span><span class="sxs-lookup"><span data-stu-id="4cfbf-171">Method toString</span></span>

<span data-ttu-id="4cfbf-172">配列の内容を説明する文字列を返します。</span><span class="sxs-lookup"><span data-stu-id="4cfbf-172">Returns a string that describes the contents of the array.</span></span>

```xpp
public str toString()
```

### <a name="return-value---tostring"></a><span data-ttu-id="4cfbf-173">戻り値 - toString</span><span class="sxs-lookup"><span data-stu-id="4cfbf-173">Return Value - toString</span></span>

<span data-ttu-id="4cfbf-174">配列の内容を説明する文字列。</span><span class="sxs-lookup"><span data-stu-id="4cfbf-174">A string that describes the contents of the array.</span></span>

### <a name="examples---tostring"></a><span data-ttu-id="4cfbf-175">例 - toString</span><span class="sxs-lookup"><span data-stu-id="4cfbf-175">Examples - toString</span></span>

<span data-ttu-id="4cfbf-176">次の例では、整数の配列を作成し、それにいくつかの値を追加します。</span><span class="sxs-lookup"><span data-stu-id="4cfbf-176">The following example creates an array of integers and adds some values to it.</span></span> <span data-ttu-id="4cfbf-177">toString メソッドは、配列が保持する値を出力するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="4cfbf-177">The toString method is used to print the values that the array holds.</span></span>

```xpp
{ 
    Array     myArray; 
```

```xpp
    Set set1 = new Set(Types::Integer); 
    Set set2 = new Set(Types::Integer); 
    int i; 
```


```xpp
    myArray = new Array(Types::Integer); 
```

```xpp
    // Add some values to the array. 
    for (i = 1; i< 10; i++) 
    { 
        myArray.value(i, i*2); 
    } 
```

```xpp
    // Print out the values in the array. 
    print myArray.toString(); 
    pause; 
}
```

## <a name="method-typeid"></a><span data-ttu-id="4cfbf-178">メソッド typeId</span><span class="sxs-lookup"><span data-stu-id="4cfbf-178">Method typeId</span></span>

<span data-ttu-id="4cfbf-179">配列の値のデータ型を返します。</span><span class="sxs-lookup"><span data-stu-id="4cfbf-179">Returns the data type of the values in the array.</span></span>

```xpp
public Types typeId()
```

### <a name="return-value---typeid"></a><span data-ttu-id="4cfbf-180">戻り値 - typeId</span><span class="sxs-lookup"><span data-stu-id="4cfbf-180">Return Value - typeId</span></span>

<span data-ttu-id="4cfbf-181">配列の要素のデータ型。</span><span class="sxs-lookup"><span data-stu-id="4cfbf-181">The data type of the elements in the array.</span></span>

### <a name="remarks---typeid"></a><span data-ttu-id="4cfbf-182">備考 - typeId</span><span class="sxs-lookup"><span data-stu-id="4cfbf-182">Remarks - typeId</span></span>

<span data-ttu-id="4cfbf-183">タイプは配列の寿命を通して同じままです。</span><span class="sxs-lookup"><span data-stu-id="4cfbf-183">The type remains the same throughout the life of the array.</span></span> <span data-ttu-id="4cfbf-184">タイプは、配列の作成時に指定されます。</span><span class="sxs-lookup"><span data-stu-id="4cfbf-184">The type is specified when the array is created.</span></span>

### <a name="examples---typeid"></a><span data-ttu-id="4cfbf-185">例 - typeId</span><span class="sxs-lookup"><span data-stu-id="4cfbf-185">Examples - typeId</span></span>

<span data-ttu-id="4cfbf-186">次の例では、特定の配列要素が存在するかどうかをテストします。</span><span class="sxs-lookup"><span data-stu-id="4cfbf-186">The following example tests whether a particular array element exists.</span></span> <span data-ttu-id="4cfbf-187">存在しない場合、配列に追加する必要がある新しい値のタイプを指定するために typeId メソッドが使用されます。</span><span class="sxs-lookup"><span data-stu-id="4cfbf-187">If it does not exist, the typeId method is used to specify the type of the new value that should be added to the array.</span></span>

```xpp
public anytype getArrayValue(Array a, int _index) 
{ 
    if (! a.exists(_index)) 
    { 
        a.value(_index,nullValueFromType(a.typeId())); 
    } 
```

```xpp
    return a.value(_index); 
}
```

## <a name="method-value"></a><span data-ttu-id="4cfbf-188">メソッド value</span><span class="sxs-lookup"><span data-stu-id="4cfbf-188">Method value</span></span>

<span data-ttu-id="4cfbf-189">指定したインデックスに格納される配列要素の値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="4cfbf-189">Gets or sets the value of the array element that is stored at the specified index.</span></span>

```xpp
public AnyType value(int index, [AnyType arg])
```

### <a name="parameters---value"></a><span data-ttu-id="4cfbf-190">パラメーター - value</span><span class="sxs-lookup"><span data-stu-id="4cfbf-190">Parameters - value</span></span>

<span data-ttu-id="4cfbf-191">指数</span><span class="sxs-lookup"><span data-stu-id="4cfbf-191">index</span></span>  
<span data-ttu-id="4cfbf-192">指定されたオフセットで配列要素に割り当てる値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="4cfbf-192">The value to assign to the array element at the specified offset; optional.</span></span>

<!-- -->

<span data-ttu-id="4cfbf-193">arg</span><span class="sxs-lookup"><span data-stu-id="4cfbf-193">arg</span></span>  
<span data-ttu-id="4cfbf-194">指定されたオフセットで配列要素に割り当てる値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="4cfbf-194">The value to assign to the array element at the specified offset; optional.</span></span>

### <a name="return-value---value"></a><span data-ttu-id="4cfbf-195">戻り値 - value</span><span class="sxs-lookup"><span data-stu-id="4cfbf-195">Return Value - value</span></span>

<span data-ttu-id="4cfbf-196">指定したオフセットに格納されている値。</span><span class="sxs-lookup"><span data-stu-id="4cfbf-196">The value that is stored at the specified offset.</span></span>

### <a name="remarks---value"></a><span data-ttu-id="4cfbf-197">備考 - value</span><span class="sxs-lookup"><span data-stu-id="4cfbf-197">Remarks - value</span></span>

<span data-ttu-id="4cfbf-198">戻り値のタイプは、配列のタイプと同じです。</span><span class="sxs-lookup"><span data-stu-id="4cfbf-198">The return type is the same as the type of the array.</span></span> <span data-ttu-id="4cfbf-199">値を持つ最後のインデックスを超えるインデックスで値を読み取ろうとすると、例外がスローされます。</span><span class="sxs-lookup"><span data-stu-id="4cfbf-199">If an attempt is made to read a value at an index that is beyond the last index that has a value, an exception is thrown.</span></span> <span data-ttu-id="4cfbf-200">値が実在しない位置に書き込まれる場合、前の要素とその実在しない位置との間にあるすべての位置に既定値が入力され、配列が展開されます。</span><span class="sxs-lookup"><span data-stu-id="4cfbf-200">If a value is written to a nonexistent location, all locations between the previous element and the nonexistent location are filled with default values, and the array is expanded.</span></span>

### <a name="examples---value"></a><span data-ttu-id="4cfbf-201">例 - value</span><span class="sxs-lookup"><span data-stu-id="4cfbf-201">Examples - value</span></span>

<span data-ttu-id="4cfbf-202">次の例では、整数の配列を作成し、value メソッドを使用して値を配列に追加します。</span><span class="sxs-lookup"><span data-stu-id="4cfbf-202">The following example creates an array of integers and then uses the value method to add some values to the array.</span></span> <span data-ttu-id="4cfbf-203">値のメソッドを使用して配列内で格納されている値を取得し、それらをテストします。</span><span class="sxs-lookup"><span data-stu-id="4cfbf-203">It then uses the value method to get the values that are stored in the array and test them.</span></span>

```xpp
{ 
     int i; 
    // Create an integer array 
    Array ia = new Array (Types::Integer); 
```

```xpp
    // Write some elements in it 
    for (i = 1; i< 10; i++) 
    { 
        ia.value(i, i*2); 
    } 
```

```xpp
    // Check the values 
    for (i = 1; i< 10; i++) 
    { 
        if (ia.value(i) != 2*i) 
        { 
            print "Error!"; 
        } 
    } 
    pause; 
}
```

## <a name="method-xml"></a><span data-ttu-id="4cfbf-204">メソッド xml</span><span class="sxs-lookup"><span data-stu-id="4cfbf-204">Method xml</span></span>

<span data-ttu-id="4cfbf-205">現在のオブジェクトを表す XML 文字列を返します。</span><span class="sxs-lookup"><span data-stu-id="4cfbf-205">Returns an XML string that represents the current object.</span></span>

```xpp
public str xml([int indent])
```

### <a name="parameters---xml"></a><span data-ttu-id="4cfbf-206">パラメーター - xml</span><span class="sxs-lookup"><span data-stu-id="4cfbf-206">Parameters - xml</span></span>

<span data-ttu-id="4cfbf-207">インデント</span><span class="sxs-lookup"><span data-stu-id="4cfbf-207">indent</span></span>  
<span data-ttu-id="4cfbf-208">返された XML 文字列のインデントの量 (省略可能)。</span><span class="sxs-lookup"><span data-stu-id="4cfbf-208">The amount of indentation of the returned XML string; optional.</span></span>

### <a name="return-value---xml"></a><span data-ttu-id="4cfbf-209">戻り値 - xml</span><span class="sxs-lookup"><span data-stu-id="4cfbf-209">Return Value - xml</span></span>

<span data-ttu-id="4cfbf-210">現在のオブジェクトを表す XML 文字列です。</span><span class="sxs-lookup"><span data-stu-id="4cfbf-210">An XML string that represents the current object.</span></span>

### <a name="remarks---xml"></a><span data-ttu-id="4cfbf-211">備考 - xml</span><span class="sxs-lookup"><span data-stu-id="4cfbf-211">Remarks - xml</span></span>

<span data-ttu-id="4cfbf-212">このメソッドをオーバーライドして、特定の型に対して意味のある値を返すことができます。</span><span class="sxs-lookup"><span data-stu-id="4cfbf-212">This method can be overridden to return values that are meaningful for a particular type.</span></span>

## <a name="method-create"></a><span data-ttu-id="4cfbf-213">メソッド create</span><span class="sxs-lookup"><span data-stu-id="4cfbf-213">Method create</span></span>

<span data-ttu-id="4cfbf-214">以前の Array.pack メソッドの呼び出しで取得されるコンテナーから配列を作成します。</span><span class="sxs-lookup"><span data-stu-id="4cfbf-214">Creates an array from the container that is obtained from a previous call to the Array.pack method.</span></span>

```xpp
public static Array create(container container)
```

### <a name="parameters---create"></a><span data-ttu-id="4cfbf-215">パラメーター - create</span><span class="sxs-lookup"><span data-stu-id="4cfbf-215">Parameters - create</span></span>

<span data-ttu-id="4cfbf-216">コンテナー</span><span class="sxs-lookup"><span data-stu-id="4cfbf-216">container</span></span>  
<span data-ttu-id="4cfbf-217">Array.pack メソッドを使用して作成されるコンテナーです。</span><span class="sxs-lookup"><span data-stu-id="4cfbf-217">A container that is created by using the Array.pack method.</span></span> <span data-ttu-id="4cfbf-218">コンテナーを展開して配列を作成します。</span><span class="sxs-lookup"><span data-stu-id="4cfbf-218">The container is unpacked to create an array.</span></span>

### <a name="return-value---create"></a><span data-ttu-id="4cfbf-219">戻り値 - create</span><span class="sxs-lookup"><span data-stu-id="4cfbf-219">Return Value - create</span></span>

<span data-ttu-id="4cfbf-220">指定したコンテナーの内容を保持する配列です。</span><span class="sxs-lookup"><span data-stu-id="4cfbf-220">An array that holds the contents of the specified container.</span></span>

### <a name="remarks---create"></a><span data-ttu-id="4cfbf-221">備考 - create</span><span class="sxs-lookup"><span data-stu-id="4cfbf-221">Remarks - create</span></span>

<span data-ttu-id="4cfbf-222">配列の値がオブジェクトの場合、オブジェクトにはコンテナーからその内部状態を再設定するために呼び出される Array.unpack メソッドが必要です。</span><span class="sxs-lookup"><span data-stu-id="4cfbf-222">If the values in the array are objects, the objects must have an Array.unpack method that is called to reestablish their internal state from a container.</span></span>

### <a name="examples---create"></a><span data-ttu-id="4cfbf-223">例 - create</span><span class="sxs-lookup"><span data-stu-id="4cfbf-223">Examples - create</span></span>

<span data-ttu-id="4cfbf-224">次の例では、配列を作成し、2 つのセットを追加します。</span><span class="sxs-lookup"><span data-stu-id="4cfbf-224">The following example creates an array and adds two sets to it.</span></span> <span data-ttu-id="4cfbf-225">配列がパックされ、それを使用して、新しい配列が作成されます。</span><span class="sxs-lookup"><span data-stu-id="4cfbf-225">The array is packed and then used to create a new array.</span></span>

```xpp
{ 
    Array     myArray; 
    Array     newArray; 
    container packedArray; 
```

```xpp
    Set set1 = new Set(Types::Integer); 
    Set set2 = new Set(Types::Integer); 
    int i; 
    int j; 
```

```xpp
    myArray = new Array(Types::Class); 
```

```xpp
    // Add some values to the set1 and set2 
    for (i = 0; i < 10; i++) 
    { 
        set1.add(i); 
        j = i+3; 
        set2.add(j); 
    } 
```

```xpp
    // Add set1 and set2 to myArray 
    myArray.value(1, set1); 
    myArray.value(2, set2); 
```

```xpp
    // Pack the myArray into a container 
    packedArray = myArray.pack(); 
```

```xpp
    // Create a new array from the container 
    if(packedArray != connull()) 
    { 
        newArray = Array::create(packedArray); 
    } 
```

```xpp
    // Test that newArray has same contents as myArray 
    print newArray.definitionString(); 
    print newArray.toString(); 
    pause; 
}
```

## <a name="method-createfromxml"></a><span data-ttu-id="4cfbf-226">メソッド createFromXML</span><span class="sxs-lookup"><span data-stu-id="4cfbf-226">Method createFromXML</span></span>

```xpp
public static Array createFromXML(Object xmlnode)
```

### <a name="parameters---createfromxml"></a><span data-ttu-id="4cfbf-227">パラメータ - createFromXML</span><span class="sxs-lookup"><span data-stu-id="4cfbf-227">Parameters - createFromXML</span></span>

<span data-ttu-id="4cfbf-228">xmlnode</span><span class="sxs-lookup"><span data-stu-id="4cfbf-228">xmlnode</span></span>  

### <a name="return-value---createfromxml"></a><span data-ttu-id="4cfbf-229">戻り値 - createFromXML</span><span class="sxs-lookup"><span data-stu-id="4cfbf-229">Return Value - createFromXML</span></span>

## <a name="method-new"></a><span data-ttu-id="4cfbf-230">メソッド new</span><span class="sxs-lookup"><span data-stu-id="4cfbf-230">Method new</span></span>

<span data-ttu-id="4cfbf-231">各要素が指定されたタイプを持つ配列を作成します。</span><span class="sxs-lookup"><span data-stu-id="4cfbf-231">Creates an array in which each element has the specified type.</span></span>

```xpp
public void new(Types Type)
```

### <a name="parameters---new"></a><span data-ttu-id="4cfbf-232">パラメーター - new</span><span class="sxs-lookup"><span data-stu-id="4cfbf-232">Parameters - new</span></span>

<span data-ttu-id="4cfbf-233">種類</span><span class="sxs-lookup"><span data-stu-id="4cfbf-233">Type</span></span>  
<span data-ttu-id="4cfbf-234">配列要素のデータ型。</span><span class="sxs-lookup"><span data-stu-id="4cfbf-234">The data type of the array elements.</span></span>

### <a name="remarks---new"></a><span data-ttu-id="4cfbf-235">備考 - new</span><span class="sxs-lookup"><span data-stu-id="4cfbf-235">Remarks - new</span></span>

<span data-ttu-id="4cfbf-236">可能な値は、Types システム列挙に使用可能な値です。</span><span class="sxs-lookup"><span data-stu-id="4cfbf-236">The possible values are those that are available for the Types system enumeration:</span></span>

-   <span data-ttu-id="4cfbf-237">AnyType</span><span class="sxs-lookup"><span data-stu-id="4cfbf-237">AnyType</span></span>
-   <span data-ttu-id="4cfbf-238">BLOB</span><span class="sxs-lookup"><span data-stu-id="4cfbf-238">BLOB</span></span>
-   <span data-ttu-id="4cfbf-239">クラス</span><span class="sxs-lookup"><span data-stu-id="4cfbf-239">Class</span></span>
-   <span data-ttu-id="4cfbf-240">コンテナー</span><span class="sxs-lookup"><span data-stu-id="4cfbf-240">Container</span></span>
-   <span data-ttu-id="4cfbf-241">日</span><span class="sxs-lookup"><span data-stu-id="4cfbf-241">Date</span></span>
-   <span data-ttu-id="4cfbf-242">日時</span><span class="sxs-lookup"><span data-stu-id="4cfbf-242">DateTime</span></span>
-   <span data-ttu-id="4cfbf-243">Enum</span><span class="sxs-lookup"><span data-stu-id="4cfbf-243">Enum</span></span>
-   <span data-ttu-id="4cfbf-244">Guid</span><span class="sxs-lookup"><span data-stu-id="4cfbf-244">Guid</span></span>
-   <span data-ttu-id="4cfbf-245">Int64</span><span class="sxs-lookup"><span data-stu-id="4cfbf-245">Int64</span></span>
-   <span data-ttu-id="4cfbf-246">整数</span><span class="sxs-lookup"><span data-stu-id="4cfbf-246">Integer</span></span>

### <a name="examples---new"></a><span data-ttu-id="4cfbf-247">例 - new</span><span class="sxs-lookup"><span data-stu-id="4cfbf-247">Examples - new</span></span>

<span data-ttu-id="4cfbf-248">次の例では、整数の配列を作成します。</span><span class="sxs-lookup"><span data-stu-id="4cfbf-248">The following example creates an array of integers.</span></span>

```xpp
Array intArray = new Array(Types::Integer);
```

