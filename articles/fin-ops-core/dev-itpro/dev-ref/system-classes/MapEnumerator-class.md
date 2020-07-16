---
title: MapEnumerator クラス
description: このトピックでは、MapEnumerator クラスについて説明します。
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
ms.openlocfilehash: 874905fd9ddadadbbe46ce244495744271101280
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502884"
---
# <a name="class-mapenumerator"></a><span data-ttu-id="5f5ce-103">クラス MapEnumerator</span><span class="sxs-lookup"><span data-stu-id="5f5ce-103">Class MapEnumerator</span></span>

[!include [banner](../../includes/banner.md)]

```xpp
class MapEnumerator extends Object
```

<span data-ttu-id="5f5ce-104">MapEnumerator クラスを使用すると、マップ内の要素上を移動できます。</span><span class="sxs-lookup"><span data-stu-id="5f5ce-104">The MapEnumerator class lets you traverse through the elements in a map.</span></span>

## <a name="remarks"></a><span data-ttu-id="5f5ce-105">備考</span><span class="sxs-lookup"><span data-stu-id="5f5ce-105">Remarks</span></span>

<span data-ttu-id="5f5ce-106">マップ列挙子は、リストの最初の要素の前に開始します。</span><span class="sxs-lookup"><span data-stu-id="5f5ce-106">Map enumerators start before the first element in the list.</span></span> <span data-ttu-id="5f5ce-107">リストの最初の要素を指すようにするために MapEnumerator.moveNext メソッドを呼び出す必要があります。</span><span class="sxs-lookup"><span data-stu-id="5f5ce-107">You must call the MapEnumerator.moveNext method to make it point to the first element in the list.</span></span> <span data-ttu-id="5f5ce-108">Map.getEnumerator メソッドが呼び出されたときに、マップと同じ層で列挙子が自動的に作成されるため、MapIterator クラスではなく、MapEnumerator クラスを使用することがベスト プラクティスです。</span><span class="sxs-lookup"><span data-stu-id="5f5ce-108">It is a best practice to use the MapEnumerator class instead of the MapIterator class because enumerators are automatically created on the same tier as the map when you call the Map.getEnumerator method.</span></span> <span data-ttu-id="5f5ce-109">MapEnumerator クラスを使用すると、Called from としてマークされたコードの潜在的な問題が回避されます。反復子とマップは別々の層に置くことができます。</span><span class="sxs-lookup"><span data-stu-id="5f5ce-109">Using the MapEnumerator class avoids a potential problem in code marked as Called from, where the iterator and map can end up on separate tiers.</span></span> <span data-ttu-id="5f5ce-110">さらに、マップ列挙子はマップ反復子よりも少ないコードを必要とするためパフォーマンスが少し向上します。</span><span class="sxs-lookup"><span data-stu-id="5f5ce-110">In addition, because map enumerators require less code than map iterators, they perform slightly better.</span></span> <span data-ttu-id="5f5ce-111">マップ反復子を使用する必要がある唯一の状況は、MapIterator.delete メソッドを使用してリストから項目を削除する場合です。</span><span class="sxs-lookup"><span data-stu-id="5f5ce-111">The only situation where you have to use a map iterator, is when you want to delete items from a list by using the MapIterator.delete method.</span></span>

## <a name="examples"></a><span data-ttu-id="5f5ce-112">例</span><span class="sxs-lookup"><span data-stu-id="5f5ce-112">Examples</span></span>

## <a name="methods"></a><span data-ttu-id="5f5ce-113">メソッド</span><span class="sxs-lookup"><span data-stu-id="5f5ce-113">Methods</span></span>

| <span data-ttu-id="5f5ce-114">方法</span><span class="sxs-lookup"><span data-stu-id="5f5ce-114">Method</span></span>                        | <span data-ttu-id="5f5ce-115">説明</span><span class="sxs-lookup"><span data-stu-id="5f5ce-115">Description</span></span>                                                                                                                                       |
|-------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5f5ce-116">public AnyType current()</span><span class="sxs-lookup"><span data-stu-id="5f5ce-116">public AnyType current()</span></span>      | <span data-ttu-id="5f5ce-117">このメソッドは廃止されました。代わりに MapEnumerator.currentKey を使用してください。</span><span class="sxs-lookup"><span data-stu-id="5f5ce-117">This method is obsolete; use MapEnumerator.currentKey instead.</span></span>                                                                                    |
| <span data-ttu-id="5f5ce-118">public AnyType currentKey()</span><span class="sxs-lookup"><span data-stu-id="5f5ce-118">public AnyType currentKey()</span></span>   | <span data-ttu-id="5f5ce-119">現在列挙子によってポイントされている (キー、値) ペアからキーを返します。</span><span class="sxs-lookup"><span data-stu-id="5f5ce-119">Returns the key from the (key, value) pair that is currently pointed to by the enumerator.</span></span>                                                        |
| <span data-ttu-id="5f5ce-120">public AnyType currentValue()</span><span class="sxs-lookup"><span data-stu-id="5f5ce-120">public AnyType currentValue()</span></span> | <span data-ttu-id="5f5ce-121">現在列挙子によってポイントされている (キー、値) ペアから値を返します。</span><span class="sxs-lookup"><span data-stu-id="5f5ce-121">Returns the value from the (key, value) pair that is currently pointed to by the enumerator.</span></span>                                                      |
| <span data-ttu-id="5f5ce-122">public str definitionString()</span><span class="sxs-lookup"><span data-stu-id="5f5ce-122">public str definitionString()</span></span> | <span data-ttu-id="5f5ce-123">列挙子の説明を返します。</span><span class="sxs-lookup"><span data-stu-id="5f5ce-123">Returns a description of the enumerator.</span></span> <span data-ttu-id="5f5ce-124">たとえば、文字列への整数のマップの列挙子は、「\[int -&gt; str\] 列挙子」を返します。</span><span class="sxs-lookup"><span data-stu-id="5f5ce-124">For example, an enumerator for a map of integers to strings would return "\[int -&gt; str\] enumerator".</span></span> |
| <span data-ttu-id="5f5ce-125">public boolean moveNext()</span><span class="sxs-lookup"><span data-stu-id="5f5ce-125">public boolean moveNext()</span></span>     | <span data-ttu-id="5f5ce-126">列挙子が有効なマップ要素を指すかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="5f5ce-126">Determines whether the enumerator points to a valid map element.</span></span>                                                                                  |
| <span data-ttu-id="5f5ce-127">public str toString()</span><span class="sxs-lookup"><span data-stu-id="5f5ce-127">public str toString()</span></span>         | <span data-ttu-id="5f5ce-128">現在のオブジェクトを表す文字列を返します。</span><span class="sxs-lookup"><span data-stu-id="5f5ce-128">Returns a string that represents the current object.</span></span>                                                                                              |
| <span data-ttu-id="5f5ce-129">public void new(Map map)</span><span class="sxs-lookup"><span data-stu-id="5f5ce-129">public void new(Map map)</span></span>      | <span data-ttu-id="5f5ce-130">Object クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="5f5ce-130">Initializes a new instance of the Object class.</span></span>                                                                                                   |
| <span data-ttu-id="5f5ce-131">public void reset()</span><span class="sxs-lookup"><span data-stu-id="5f5ce-131">public void reset()</span></span>           | <span data-ttu-id="5f5ce-132">列挙子を移動して、マップ内の最初の要素の直前をポイントします。</span><span class="sxs-lookup"><span data-stu-id="5f5ce-132">Moves the enumerator to point to just before the first element in the map.</span></span>                                                                        |

## <a name="method-current"></a><span data-ttu-id="5f5ce-133">メソッド current</span><span class="sxs-lookup"><span data-stu-id="5f5ce-133">Method current</span></span>

<span data-ttu-id="5f5ce-134">このメソッドは廃止されました。代わりに MapEnumerator.currentKey を使用してください。</span><span class="sxs-lookup"><span data-stu-id="5f5ce-134">This method is obsolete; use MapEnumerator.currentKey instead.</span></span>

```xpp
public AnyType current()
```

### <a name="return-value---current"></a><span data-ttu-id="5f5ce-135">戻り値 - current</span><span class="sxs-lookup"><span data-stu-id="5f5ce-135">Return Value - current</span></span>

## <a name="method-currentkey"></a><span data-ttu-id="5f5ce-136">メソッド currentKey</span><span class="sxs-lookup"><span data-stu-id="5f5ce-136">Method currentKey</span></span>

<span data-ttu-id="5f5ce-137">現在列挙子によってポイントされている (キー、値) ペアからキーを返します。</span><span class="sxs-lookup"><span data-stu-id="5f5ce-137">Returns the key from the (key, value) pair that is currently pointed to by the enumerator.</span></span>

```xpp
public AnyType currentKey()
```

### <a name="return-value---currentkey"></a><span data-ttu-id="5f5ce-138">戻り値 - currentKey</span><span class="sxs-lookup"><span data-stu-id="5f5ce-138">Return Value - currentKey</span></span>

<span data-ttu-id="5f5ce-139">現在列挙子によってポイントされているマップ要素のキー。</span><span class="sxs-lookup"><span data-stu-id="5f5ce-139">The key from the map element that is currently pointed to by the enumerator.</span></span>

### <a name="remarks---currentkey"></a><span data-ttu-id="5f5ce-140">備考 - currentKey</span><span class="sxs-lookup"><span data-stu-id="5f5ce-140">Remarks - currentKey</span></span>

<span data-ttu-id="5f5ce-141">CurrentKey メソッドを呼び出す前に、MapEnumerator.moveNext メソッドを呼び出す必要があります。</span><span class="sxs-lookup"><span data-stu-id="5f5ce-141">You must call the MapEnumerator.moveNext method before you call the currentKey method.</span></span>

### <a name="examples---currentkey"></a><span data-ttu-id="5f5ce-142">例 - currentKey</span><span class="sxs-lookup"><span data-stu-id="5f5ce-142">Examples - currentKey</span></span>

<span data-ttu-id="5f5ce-143">次の例では、マップ内の特定のテーブル ID を検索し、そのマップ要素のキー値を返します。</span><span class="sxs-lookup"><span data-stu-id="5f5ce-143">The following example searches for a particular table ID in a map and then returns the key value of that map element.</span></span>

```xpp
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
```

## <a name="method-currentvalue"></a><span data-ttu-id="5f5ce-144">メソッド currentValue</span><span class="sxs-lookup"><span data-stu-id="5f5ce-144">Method currentValue</span></span>

<span data-ttu-id="5f5ce-145">現在列挙子によってポイントされている (キー、値) ペアから値を返します。</span><span class="sxs-lookup"><span data-stu-id="5f5ce-145">Returns the value from the (key, value) pair that is currently pointed to by the enumerator.</span></span>

```xpp
public AnyType currentValue()
```

### <a name="return-value---currentvalue"></a><span data-ttu-id="5f5ce-146">戻り値 - currentValue</span><span class="sxs-lookup"><span data-stu-id="5f5ce-146">Return Value - currentValue</span></span>

<span data-ttu-id="5f5ce-147">現在列挙子によってポイントされているマップ要素の値。</span><span class="sxs-lookup"><span data-stu-id="5f5ce-147">The value from the map element that is currently pointed to by the enumerator.</span></span>

### <a name="remarks---currentvalue"></a><span data-ttu-id="5f5ce-148">備考 - currentValue</span><span class="sxs-lookup"><span data-stu-id="5f5ce-148">Remarks - currentValue</span></span>

<span data-ttu-id="5f5ce-149">このメソッドを呼び出す前に、MapEnumerator.moveNext メソッドを呼び出す必要があります。</span><span class="sxs-lookup"><span data-stu-id="5f5ce-149">You must call the MapEnumerator.moveNext method before you call this method.</span></span>

### <a name="examples---currentvalue"></a><span data-ttu-id="5f5ce-150">例 - currentValue</span><span class="sxs-lookup"><span data-stu-id="5f5ce-150">Examples - currentValue</span></span>

<span data-ttu-id="5f5ce-151">次の例では、マップを検索して、パラメーターとして渡された値と等しい値を持つ要素を検索します。</span><span class="sxs-lookup"><span data-stu-id="5f5ce-151">The following example searches through a map to find an element that has a value equal to that passed in as a parameter.</span></span> <span data-ttu-id="5f5ce-152">MapEnumerator.moveNext メソッドは、マップを反復処理するために使用され、currentValue メソッドは各値をテストしてパラメーターと一致するかどうかを確認するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="5f5ce-152">The MapEnumerator.moveNext method is used to iterate through the map, and the currentValue method is used to test each value to see whether it matches the parameter.</span></span>

```xpp
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
```

## <a name="method-definitionstring"></a><span data-ttu-id="5f5ce-153">メソッド definitionString</span><span class="sxs-lookup"><span data-stu-id="5f5ce-153">Method definitionString</span></span>

<span data-ttu-id="5f5ce-154">列挙子の説明を返します。</span><span class="sxs-lookup"><span data-stu-id="5f5ce-154">Returns a description of the enumerator.</span></span> <span data-ttu-id="5f5ce-155">たとえば、文字列への整数のマップの列挙子は、「\[int -&gt; str\] 列挙子」を返します。</span><span class="sxs-lookup"><span data-stu-id="5f5ce-155">For example, an enumerator for a map of integers to strings would return "\[int -&gt; str\] enumerator".</span></span>

```xpp
public str definitionString()
```

### <a name="return-value---definitionstring"></a><span data-ttu-id="5f5ce-156">戻り値 - definitionString</span><span class="sxs-lookup"><span data-stu-id="5f5ce-156">Return Value - definitionString</span></span>

<span data-ttu-id="5f5ce-157">列挙子の説明を含む文字列。</span><span class="sxs-lookup"><span data-stu-id="5f5ce-157">A string that contains a description of the enumerator.</span></span>

### <a name="examples---definitionstring"></a><span data-ttu-id="5f5ce-158">例 - definitionString</span><span class="sxs-lookup"><span data-stu-id="5f5ce-158">Examples - definitionString</span></span>

<span data-ttu-id="5f5ce-159">次の例では、マップとその列挙子を作成し、列挙子の定義を出力します。</span><span class="sxs-lookup"><span data-stu-id="5f5ce-159">The following example creates a map and an enumerator for it, and then it prints out a definition of the enumerator.</span></span>

```xpp
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
```

## <a name="method-movenext"></a><span data-ttu-id="5f5ce-160">メソッド moveNext</span><span class="sxs-lookup"><span data-stu-id="5f5ce-160">Method moveNext</span></span>

<span data-ttu-id="5f5ce-161">列挙子が有効なマップ要素を指すかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="5f5ce-161">Determines whether the enumerator points to a valid map element.</span></span>

```xpp
public boolean moveNext()
```

### <a name="return-value---movenext"></a><span data-ttu-id="5f5ce-162">戻り値 - moveNext</span><span class="sxs-lookup"><span data-stu-id="5f5ce-162">Return Value - moveNext</span></span>

<span data-ttu-id="5f5ce-163">マップ内の現在の職位が有効な要素を保持している場合は true。それ以外の場合は false。</span><span class="sxs-lookup"><span data-stu-id="5f5ce-163">true if the current position in the map holds a valid element; otherwise false.</span></span>

### <a name="remarks---movenext"></a><span data-ttu-id="5f5ce-164">備考 - moveNext</span><span class="sxs-lookup"><span data-stu-id="5f5ce-164">Remarks - moveNext</span></span>

<span data-ttu-id="5f5ce-165">マップ列挙子は、マップの最初の要素の前に開始します。</span><span class="sxs-lookup"><span data-stu-id="5f5ce-165">Map enumerators start before the first element in the map.</span></span> <span data-ttu-id="5f5ce-166">マップの最初の要素を指すようにするために moveNext メソッドを呼び出す必要があります。</span><span class="sxs-lookup"><span data-stu-id="5f5ce-166">You must call the moveNext method to make it point to the first element in the map.</span></span>

### <a name="examples---movenext"></a><span data-ttu-id="5f5ce-167">例 - moveNext</span><span class="sxs-lookup"><span data-stu-id="5f5ce-167">Examples - moveNext</span></span>

<span data-ttu-id="5f5ce-168">次の例では、moveNext メソッドを使用してプロジェクトに含まれるテーブルを反復処理し、テーブルの DictTable オブジェクトを含む新しいマップに追加します。</span><span class="sxs-lookup"><span data-stu-id="5f5ce-168">The following example uses the moveNext method to iterate over the tables that are contained in a project and adds them to a new map that contains a DictTable object for each table.</span></span> <span data-ttu-id="5f5ce-169">(DictTable を使用すると、テーブルに関する情報にアクセスできます。)</span><span class="sxs-lookup"><span data-stu-id="5f5ce-169">(DictTable lets you access information about a table.)</span></span>

```xpp
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
```

## <a name="method-tostring"></a><span data-ttu-id="5f5ce-170">メソッド toString</span><span class="sxs-lookup"><span data-stu-id="5f5ce-170">Method toString</span></span>

<span data-ttu-id="5f5ce-171">現在のオブジェクトを表す文字列を返します。</span><span class="sxs-lookup"><span data-stu-id="5f5ce-171">Returns a string that represents the current object.</span></span>

```xpp
public str toString()
```

### <a name="return-value---tostring"></a><span data-ttu-id="5f5ce-172">戻り値 - toString</span><span class="sxs-lookup"><span data-stu-id="5f5ce-172">Return Value - toString</span></span>

<span data-ttu-id="5f5ce-173">現在のオブジェクトを表す文字列。</span><span class="sxs-lookup"><span data-stu-id="5f5ce-173">A string that represents the current object.</span></span>

### <a name="remarks---tostring"></a><span data-ttu-id="5f5ce-174">備考 - toString</span><span class="sxs-lookup"><span data-stu-id="5f5ce-174">Remarks - toString</span></span>

<span data-ttu-id="5f5ce-175">既定の実装は、オブジェクトのクラス名を返します。</span><span class="sxs-lookup"><span data-stu-id="5f5ce-175">The default implementation returns the class name of the object.</span></span> <span data-ttu-id="5f5ce-176">メソッドは派生クラスで上書きできるため、そのタイプの意味のある値が返されます。</span><span class="sxs-lookup"><span data-stu-id="5f5ce-176">The method can be overridden in a derived class to return values that are meaningful for that type.</span></span> <span data-ttu-id="5f5ce-177">たとえば、SysMethodInfo クラスのインスタンスは、インスタンスまたは静的などのメソッド名およびメソッドのタイプを返します。</span><span class="sxs-lookup"><span data-stu-id="5f5ce-177">For example, an instance of the SysMethodInfo class returns the method name and type of the method, such as instance or static.</span></span>

### <a name="examples---tostring"></a><span data-ttu-id="5f5ce-178">例 - toString</span><span class="sxs-lookup"><span data-stu-id="5f5ce-178">Examples - toString</span></span>

<span data-ttu-id="5f5ce-179">次の例では、マップを作成し、最初の要素と 2 番目の要素の内容をマップに出力します。</span><span class="sxs-lookup"><span data-stu-id="5f5ce-179">The following example creates a map, and then prints the content of the first and second elements in the map.</span></span>

```xpp
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
```

## <a name="method-new"></a><span data-ttu-id="5f5ce-180">メソッド new</span><span class="sxs-lookup"><span data-stu-id="5f5ce-180">Method new</span></span>

<span data-ttu-id="5f5ce-181">Object クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="5f5ce-181">Initializes a new instance of the Object class.</span></span>

```xpp
public void new(Map map)
```

### <a name="parameters---new"></a><span data-ttu-id="5f5ce-182">パラメーター - new</span><span class="sxs-lookup"><span data-stu-id="5f5ce-182">Parameters - new</span></span>

<span data-ttu-id="5f5ce-183">マップ</span><span class="sxs-lookup"><span data-stu-id="5f5ce-183">map</span></span>  
<span data-ttu-id="5f5ce-184">列挙子を作成するマップ。</span><span class="sxs-lookup"><span data-stu-id="5f5ce-184">The map for which to create an enumerator.</span></span>

### <a name="remarks---new"></a><span data-ttu-id="5f5ce-185">備考 - new</span><span class="sxs-lookup"><span data-stu-id="5f5ce-185">Remarks - new</span></span>

<span data-ttu-id="5f5ce-186"> メソッドは廃止されています。</span><span class="sxs-lookup"><span data-stu-id="5f5ce-186">This method is obsolete.</span></span> <span data-ttu-id="5f5ce-187">代わりに Map.getEnumerator メソッドを使用します。</span><span class="sxs-lookup"><span data-stu-id="5f5ce-187">Use the Map.getEnumerator method instead.</span></span>

## <a name="method-reset"></a><span data-ttu-id="5f5ce-188">メソッド reset</span><span class="sxs-lookup"><span data-stu-id="5f5ce-188">Method reset</span></span>

<span data-ttu-id="5f5ce-189">列挙子を移動して、マップ内の最初の要素の直前をポイントします。</span><span class="sxs-lookup"><span data-stu-id="5f5ce-189">Moves the enumerator to point to just before the first element in the map.</span></span>

```xpp
public void reset()
```

### <a name="remarks---reset"></a><span data-ttu-id="5f5ce-190">備考 - reset</span><span class="sxs-lookup"><span data-stu-id="5f5ce-190">Remarks - reset</span></span>

<span data-ttu-id="5f5ce-191">reset メソッドは、列挙子をセットの先頭、セットの最初の要素の前に移動します。</span><span class="sxs-lookup"><span data-stu-id="5f5ce-191">The reset method moves the enumerator to the start of the set, before the first element in the set.</span></span> <span data-ttu-id="5f5ce-192">セットの最初の要素を指すようにするために MapEnumerator.moveNext メソッドを呼び出す必要があります。</span><span class="sxs-lookup"><span data-stu-id="5f5ce-192">You must call the MapEnumerator.moveNext method to make it point to the first element in the set.</span></span>

