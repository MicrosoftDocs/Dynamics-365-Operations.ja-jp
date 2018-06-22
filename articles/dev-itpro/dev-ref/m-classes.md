---
title: "M クラス"
description: "文字 M で始まるシステム API クラス。"
author: RobinARH
manager: AnnBe
ms.date: 11/07/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Developer
ms.reviewer: robinr
ms.search.scope: Operations
ms.custom: 52321
ms.assetid: 954d2067-ef47-4714-ae75-23e7a5d539db
ms.search.region: Global
ms.author: robinr
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 1c3d70b68d42185bf135b14e4190707104bf6bf9
ms.contentlocale: ja-jp
ms.lasthandoff: 05/08/2018

---

# <a name="m-classes"></a><span data-ttu-id="f7b4f-103">M クラス</span><span class="sxs-lookup"><span data-stu-id="f7b4f-103">M Classes</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f7b4f-104">文字 M で始まるシステム API クラス。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-104">System API classes that start with the letter M.</span></span>

<a name="class-managedeventargs"></a><span data-ttu-id="f7b4f-105">クラス ManagedEventArgs</span><span class="sxs-lookup"><span data-stu-id="f7b4f-105">Class ManagedEventArgs</span></span>
----------------------

    class ManagedEventArgs extends Object

### <a name="remarks"></a><span data-ttu-id="f7b4f-106">備考</span><span class="sxs-lookup"><span data-stu-id="f7b4f-106">Remarks</span></span>

### <a name="examples"></a><span data-ttu-id="f7b4f-107">例</span><span class="sxs-lookup"><span data-stu-id="f7b4f-107">Examples</span></span>

### <a name="methods"></a><span data-ttu-id="f7b4f-108">メソッド</span><span class="sxs-lookup"><span data-stu-id="f7b4f-108">Methods</span></span>

| <span data-ttu-id="f7b4f-109">方法</span><span class="sxs-lookup"><span data-stu-id="f7b4f-109">Method</span></span>            | <span data-ttu-id="f7b4f-110">説明</span><span class="sxs-lookup"><span data-stu-id="f7b4f-110">Description</span></span>                                               |
|-------------------|-----------------------------------------------------------|
| <span data-ttu-id="f7b4f-111">public void new()</span><span class="sxs-lookup"><span data-stu-id="f7b4f-111">public void new()</span></span> | <span data-ttu-id="f7b4f-112">ManagedEventArgs クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-112">Initializes a new instance of the ManagedEventArgs class.</span></span> |

### <a name="method-new"></a><span data-ttu-id="f7b4f-113">メソッド new</span><span class="sxs-lookup"><span data-stu-id="f7b4f-113">Method new</span></span>

<span data-ttu-id="f7b4f-114">ManagedEventArgs クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-114">Initializes a new instance of the ManagedEventArgs class.</span></span>

    public void new()

## <a name="class-managedeventdelegate"></a><span data-ttu-id="f7b4f-115">クラス ManagedEventDelegate</span><span class="sxs-lookup"><span data-stu-id="f7b4f-115">Class ManagedEventDelegate</span></span>
    class ManagedEventDelegate extends Object

### <a name="remarks"></a><span data-ttu-id="f7b4f-116">備考</span><span class="sxs-lookup"><span data-stu-id="f7b4f-116">Remarks</span></span>

### <a name="examples"></a><span data-ttu-id="f7b4f-117">例</span><span class="sxs-lookup"><span data-stu-id="f7b4f-117">Examples</span></span>

### <a name="methods"></a><span data-ttu-id="f7b4f-118">メソッド</span><span class="sxs-lookup"><span data-stu-id="f7b4f-118">Methods</span></span>

| <span data-ttu-id="f7b4f-119">方法</span><span class="sxs-lookup"><span data-stu-id="f7b4f-119">Method</span></span>                                                                    | <span data-ttu-id="f7b4f-120">説明</span><span class="sxs-lookup"><span data-stu-id="f7b4f-120">Description</span></span>                                                   |
|---------------------------------------------------------------------------|---------------------------------------------------------------|
| <span data-ttu-id="f7b4f-121">public boolean marshalExceptionsToXPP(\[boolean marshalExceptionsToXPP\])</span><span class="sxs-lookup"><span data-stu-id="f7b4f-121">public boolean marshalExceptionsToXPP(\[boolean marshalExceptionsToXPP\])</span></span> |                                                               |
| <span data-ttu-id="f7b4f-122">private void new()</span><span class="sxs-lookup"><span data-stu-id="f7b4f-122">private void new()</span></span>                                                        | <span data-ttu-id="f7b4f-123">ManagedEventDelegate クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-123">Initializes a new instance of the ManagedEventDelegate class.</span></span> |
| <span data-ttu-id="f7b4f-124">public void invoke(Object sender, ManagedEventArgs args)</span><span class="sxs-lookup"><span data-stu-id="f7b4f-124">public void invoke(Object sender, ManagedEventArgs args)</span></span>                  |                                                               |

### <a name="method-marshalexceptionstoxpp"></a><span data-ttu-id="f7b4f-125">メソッド marshalExceptionsToXPP</span><span class="sxs-lookup"><span data-stu-id="f7b4f-125">Method marshalExceptionsToXPP</span></span>

    public boolean marshalExceptionsToXPP([boolean marshalExceptionsToXPP])

#### <a name="parameters"></a><span data-ttu-id="f7b4f-126">パラメーター</span><span class="sxs-lookup"><span data-stu-id="f7b4f-126">Parameters</span></span>

<span data-ttu-id="f7b4f-127">marshalExceptionsToXPP</span><span class="sxs-lookup"><span data-stu-id="f7b4f-127">marshalExceptionsToXPP</span></span>  

#### <a name="return-value"></a><span data-ttu-id="f7b4f-128">戻り値</span><span class="sxs-lookup"><span data-stu-id="f7b4f-128">Return Value</span></span>

### <a name="method-new"></a><span data-ttu-id="f7b4f-129">メソッド new</span><span class="sxs-lookup"><span data-stu-id="f7b4f-129">Method new</span></span>

<span data-ttu-id="f7b4f-130">ManagedEventDelegate クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-130">Initializes a new instance of the ManagedEventDelegate class.</span></span>

    private void new()

### <a name="method-invoke"></a><span data-ttu-id="f7b4f-131">メソッド invoke</span><span class="sxs-lookup"><span data-stu-id="f7b4f-131">Method invoke</span></span>

    public void invoke(Object sender, ManagedEventArgs args)

#### <a name="parameters"></a><span data-ttu-id="f7b4f-132">パラメーター</span><span class="sxs-lookup"><span data-stu-id="f7b4f-132">Parameters</span></span>

<span data-ttu-id="f7b4f-133">sender</span><span class="sxs-lookup"><span data-stu-id="f7b4f-133">sender</span></span>  

<!-- -->

<span data-ttu-id="f7b4f-134">args</span><span class="sxs-lookup"><span data-stu-id="f7b4f-134">args</span></span>  

## <a name="class-managedeventhandler"></a><span data-ttu-id="f7b4f-135">クラス ManagedEventHandler</span><span class="sxs-lookup"><span data-stu-id="f7b4f-135">Class ManagedEventHandler</span></span>
    class ManagedEventHandler extends Object

### <a name="remarks"></a><span data-ttu-id="f7b4f-136">備考</span><span class="sxs-lookup"><span data-stu-id="f7b4f-136">Remarks</span></span>

### <a name="examples"></a><span data-ttu-id="f7b4f-137">例</span><span class="sxs-lookup"><span data-stu-id="f7b4f-137">Examples</span></span>

### <a name="methods"></a><span data-ttu-id="f7b4f-138">メソッド</span><span class="sxs-lookup"><span data-stu-id="f7b4f-138">Methods</span></span>

| <span data-ttu-id="f7b4f-139">方法</span><span class="sxs-lookup"><span data-stu-id="f7b4f-139">Method</span></span>                                     | <span data-ttu-id="f7b4f-140">説明</span><span class="sxs-lookup"><span data-stu-id="f7b4f-140">Description</span></span>                                     |
|--------------------------------------------|-------------------------------------------------|
| <span data-ttu-id="f7b4f-141">public void finalize()</span><span class="sxs-lookup"><span data-stu-id="f7b4f-141">public void finalize()</span></span>                     |                                                 |
| <span data-ttu-id="f7b4f-142">public void new(Object object, str method)</span><span class="sxs-lookup"><span data-stu-id="f7b4f-142">public void new(Object object, str method)</span></span> | <span data-ttu-id="f7b4f-143">Object クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-143">Initializes a new instance of the Object class.</span></span> |

### <a name="method-finalize"></a><span data-ttu-id="f7b4f-144">メソッド finalize</span><span class="sxs-lookup"><span data-stu-id="f7b4f-144">Method finalize</span></span>

    public void finalize()

### <a name="method-new"></a><span data-ttu-id="f7b4f-145">メソッド new</span><span class="sxs-lookup"><span data-stu-id="f7b4f-145">Method new</span></span>

<span data-ttu-id="f7b4f-146">Object クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-146">Initializes a new instance of the Object class.</span></span>

    public void new(Object object, str method)

#### <a name="parameters"></a><span data-ttu-id="f7b4f-147">パラメーター</span><span class="sxs-lookup"><span data-stu-id="f7b4f-147">Parameters</span></span>

<span data-ttu-id="f7b4f-148">オブジェクト</span><span class="sxs-lookup"><span data-stu-id="f7b4f-148">object</span></span>  

<!-- -->

<span data-ttu-id="f7b4f-149">メソッド</span><span class="sxs-lookup"><span data-stu-id="f7b4f-149">method</span></span>  

## <a name="class-map"></a><span data-ttu-id="f7b4f-150">クラス マップ</span><span class="sxs-lookup"><span data-stu-id="f7b4f-150">Class Map</span></span>
    class Map extends Object

<span data-ttu-id="f7b4f-151">Map クラスを使うと、ある値 (キー) を別の値に関連付けることができます。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-151">The Map class lets to associate one value (the key) with another value.</span></span>

### <a name="remarks"></a><span data-ttu-id="f7b4f-152">備考</span><span class="sxs-lookup"><span data-stu-id="f7b4f-152">Remarks</span></span>

<span data-ttu-id="f7b4f-153">キーと値の両方は、オブジェクトを含む有効な X++ タイプにすることができます。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-153">Both the key and the value can be any valid X++ type, including objects.</span></span> <span data-ttu-id="f7b4f-154">キーのタイプと値は、マップの宣言で指定されます。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-154">The types of the key and the value are specified in the declaration of the map.</span></span> <span data-ttu-id="f7b4f-155">マップが実装される方法は、値へのアクセスが非常に高速であることを意味します。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-155">The way in which maps are implemented means that access to the values is very fast.</span></span> <span data-ttu-id="f7b4f-156">複数のキーは、同じ値にマップできますが、1 つのキーは一度に 1 つの値にだけマップすることができます。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-156">Multiple keys can map to the same value, but one key can map to only one value at a time.</span></span> <span data-ttu-id="f7b4f-157">既存のキー値を持つ (キー、値) ペアを追加すると、既存のペアがそのキー値に置き換えられます。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-157">If you add a (key, value) pair that has an existing key value, it replaces the existing pair with that key value.</span></span> <span data-ttu-id="f7b4f-158">マップ内の (キー、値) ペアは、MapEnumerator クラスを使用して移動できます。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-158">The (key, value) pairs in a map can be traversed by using the MapEnumerator class.</span></span>

### <a name="examples"></a><span data-ttu-id="f7b4f-159">例</span><span class="sxs-lookup"><span data-stu-id="f7b4f-159">Examples</span></span>

<span data-ttu-id="f7b4f-160">次の例は、マップを逆にする方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-160">The following example illustrates how to invert a map.</span></span> <span data-ttu-id="f7b4f-161">2 つの異なるキーによってマップされている値がない場合にのみ、マップを反転できます。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-161">A map can be inverted only if no value is mapped to by two different keys.</span></span> <span data-ttu-id="f7b4f-162">これを確認するために Map.keySet メソッドと Map.valueSet メソッドの要素数が比較されます。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-162">The number of elements in the Map.keySet method and the Map.valueSet method is compared to check this.</span></span> <span data-ttu-id="f7b4f-163">それ以外の場合、要素が受信マップで移動し、結果マップに挿入されます。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-163">Otherwise, the elements are traversed in the incoming map and inserted into the result map.</span></span> <span data-ttu-id="f7b4f-164">切り替えを実行する関数、invertMap メソッドは、キーと値の型に関係なく機能します。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-164">The function that performs the inversion, the invertMap method, works regardless of the types of the keys and values.</span></span>

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

### <a name="methods"></a><span data-ttu-id="f7b4f-165">メソッド</span><span class="sxs-lookup"><span data-stu-id="f7b4f-165">Methods</span></span>

| <span data-ttu-id="f7b4f-166">方法</span><span class="sxs-lookup"><span data-stu-id="f7b4f-166">Method</span></span>                                                      | <span data-ttu-id="f7b4f-167">説明</span><span class="sxs-lookup"><span data-stu-id="f7b4f-167">Description</span></span>                                                                                     |
|-------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f7b4f-168">public str definitionString()</span><span class="sxs-lookup"><span data-stu-id="f7b4f-168">public str definitionString()</span></span>                               | <span data-ttu-id="f7b4f-169">マップの定義を含む文字列を返します。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-169">Returns a string that contains a definition of the map.</span></span>                                         |
| <span data-ttu-id="f7b4f-170">public Set domainSet()</span><span class="sxs-lookup"><span data-stu-id="f7b4f-170">public Set domainSet()</span></span>                                      | <span data-ttu-id="f7b4f-171">マップにキー (ドメイン) 値のセットを作成します。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-171">Creates a set of the key (domain) values in a map.</span></span>                                              |
| <span data-ttu-id="f7b4f-172">public Types domainType()</span><span class="sxs-lookup"><span data-stu-id="f7b4f-172">public Types domainType()</span></span>                                   | <span data-ttu-id="f7b4f-173">マップ内のキー (ドメイン) 値のタイプを決定します。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-173">Determines the type of the key (domain) values in a map.</span></span>                                        |
| <span data-ttu-id="f7b4f-174">public int elements()</span><span class="sxs-lookup"><span data-stu-id="f7b4f-174">public int elements()</span></span>                                       | <span data-ttu-id="f7b4f-175">マップ内の要素の数を返します。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-175">Returns the number of elements in the map.</span></span>                                                      |
| <span data-ttu-id="f7b4f-176">public boolean empty()</span><span class="sxs-lookup"><span data-stu-id="f7b4f-176">public boolean empty()</span></span>                                      | <span data-ttu-id="f7b4f-177">マップに (キー、値) のペアが含まれているかどうかを判定します。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-177">Determines whether the map contains any (key, value) pairs.</span></span>                                     |
| <span data-ttu-id="f7b4f-178">public boolean exists(AnyType keyValue)</span><span class="sxs-lookup"><span data-stu-id="f7b4f-178">public boolean exists(AnyType keyValue)</span></span>                     | <span data-ttu-id="f7b4f-179">特定の値がマップ内のキーとして存在するかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-179">Determines whether a particular value exists as a key in the map.</span></span>                               |
| <span data-ttu-id="f7b4f-180">public MapEnumerator getEnumerator()</span><span class="sxs-lookup"><span data-stu-id="f7b4f-180">public MapEnumerator getEnumerator()</span></span>                        | <span data-ttu-id="f7b4f-181">マップ内のスキャンを可能にする、マップの列挙子を作成します。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-181">Creates an enumerator for the map, which lets you traverse the map.</span></span>                             |
| <span data-ttu-id="f7b4f-182">public boolean insert(AnyType keyValue, AnyType valueValue)</span><span class="sxs-lookup"><span data-stu-id="f7b4f-182">public boolean insert(AnyType keyValue, AnyType valueValue)</span></span> | <span data-ttu-id="f7b4f-183">マップに要素 (keyValue、valueValue ペア) を挿入します。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-183">Inserts an element (keyValue, valueValue pair) into the map.</span></span>                                    |
| <span data-ttu-id="f7b4f-184">public Set keySet()</span><span class="sxs-lookup"><span data-stu-id="f7b4f-184">public Set keySet()</span></span>                                         | <span data-ttu-id="f7b4f-185">マップからのキー値を含むセットを返します。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-185">Returns a set that contains the key values from a map.</span></span>                                          |
| <span data-ttu-id="f7b4f-186">public Types keyType()</span><span class="sxs-lookup"><span data-stu-id="f7b4f-186">public Types keyType()</span></span>                                      | <span data-ttu-id="f7b4f-187">マップ内のキー値のタイプを返します。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-187">Returns the type of the key values in a map.</span></span>                                                    |
| <span data-ttu-id="f7b4f-188">public AnyType lookup(AnyType keyValue)</span><span class="sxs-lookup"><span data-stu-id="f7b4f-188">public AnyType lookup(AnyType keyValue)</span></span>                     | <span data-ttu-id="f7b4f-189">指定されたキー値によりマッピングされている値を返します。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-189">Returns the value that is mapped to by a specified key value.</span></span>                                   |
| <span data-ttu-id="f7b4f-190">public container pack()</span><span class="sxs-lookup"><span data-stu-id="f7b4f-190">public container pack()</span></span>                                     | <span data-ttu-id="f7b4f-191">Map クラスの現在のインスタンスをシリアル化します。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-191">Serializes the current instance of the Map class.</span></span>                                               |
| <span data-ttu-id="f7b4f-192">public Set rangeSet()</span><span class="sxs-lookup"><span data-stu-id="f7b4f-192">public Set rangeSet()</span></span>                                       | <span data-ttu-id="f7b4f-193">マップ内のキーによってマップされる値 (範囲) を含むセットを返します。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-193">Returns a set that contains the values (ranges) that are mapped to by the keys in a map.</span></span>        |
| <span data-ttu-id="f7b4f-194">public Types rangeType()</span><span class="sxs-lookup"><span data-stu-id="f7b4f-194">public Types rangeType()</span></span>                                    | <span data-ttu-id="f7b4f-195">マップ内のキーによってマップされる値 (範囲) のタイプを決定します。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-195">Determines the type of the values (ranges) that are mapped to by the keys in a map.</span></span>             |
| <span data-ttu-id="f7b4f-196">public boolean remove(AnyType keyValue)</span><span class="sxs-lookup"><span data-stu-id="f7b4f-196">public boolean remove(AnyType keyValue)</span></span>                     | <span data-ttu-id="f7b4f-197">(キー、値) ペアをマップから削除します。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-197">Removes a (key, value) pair from a map.</span></span>                                                         |
| <span data-ttu-id="f7b4f-198">public str toString()</span><span class="sxs-lookup"><span data-stu-id="f7b4f-198">public str toString()</span></span>                                       | <span data-ttu-id="f7b4f-199">マップ内の (キー、値) ペアの説明を返します。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-199">Returns a description of the (key, value) pairs in the map.</span></span>                                     |
| <span data-ttu-id="f7b4f-200">public Set valueSet()</span><span class="sxs-lookup"><span data-stu-id="f7b4f-200">public Set valueSet()</span></span>                                       | <span data-ttu-id="f7b4f-201">マップ内のキーによってマップされる値を含むセットを返します。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-201">Returns a set that contains the values that are mapped to by the keys in a map.</span></span>                 |
| <span data-ttu-id="f7b4f-202">public Types valueType()</span><span class="sxs-lookup"><span data-stu-id="f7b4f-202">public Types valueType()</span></span>                                    | <span data-ttu-id="f7b4f-203">マップ内のキーによってマップされる値のタイプを返します。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-203">Returns the type of the values that are mapped to by the keys in a map.</span></span>                         |
| <span data-ttu-id="f7b4f-204">public str xml(\[int indent\])</span><span class="sxs-lookup"><span data-stu-id="f7b4f-204">public str xml(\[int indent\])</span></span>                              | <span data-ttu-id="f7b4f-205">現在のオブジェクトを表す XML 文字列を返します。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-205">Returns an XML string that represents the current object.</span></span>                                       |
| <span data-ttu-id="f7b4f-206">::public static Map create(container container)</span><span class="sxs-lookup"><span data-stu-id="f7b4f-206">::public static Map create(container container)</span></span>             | <span data-ttu-id="f7b4f-207">以前の Map.pack メソッドの呼び出しで取得されたコンテナーからマップを作成します。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-207">Creates a map from the container that was obtained from a previous call to the Map.pack method.</span></span> |
| <span data-ttu-id="f7b4f-208">::public static Map createFromXML(Object xmlnode)</span><span class="sxs-lookup"><span data-stu-id="f7b4f-208">::public static Map createFromXML(Object xmlnode)</span></span>           |                                                                                                 |
| <span data-ttu-id="f7b4f-209">::public static boolean equal(Map map1, Map map2)</span><span class="sxs-lookup"><span data-stu-id="f7b4f-209">::public static boolean equal(Map map1, Map map2)</span></span>           | <span data-ttu-id="f7b4f-210">2 つのマップが等しいかどうかを判断します。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-210">Determines whether two maps are equal.</span></span>                                                          |
| <span data-ttu-id="f7b4f-211">public void new(Types key, Types value)</span><span class="sxs-lookup"><span data-stu-id="f7b4f-211">public void new(Types key, Types value)</span></span>                     | <span data-ttu-id="f7b4f-212">新しいマップを作成します</span><span class="sxs-lookup"><span data-stu-id="f7b4f-212">Creates a new map.</span></span>                                                                              |

### <a name="method-definitionstring"></a><span data-ttu-id="f7b4f-213">メソッド definitionString</span><span class="sxs-lookup"><span data-stu-id="f7b4f-213">Method definitionString</span></span>

<span data-ttu-id="f7b4f-214">マップの定義を含む文字列を返します。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-214">Returns a string that contains a definition of the map.</span></span>

    public str definitionString()

#### <a name="return-value"></a><span data-ttu-id="f7b4f-215">戻り値</span><span class="sxs-lookup"><span data-stu-id="f7b4f-215">Return Value</span></span>

<span data-ttu-id="f7b4f-216">マップの定義を含む文字列。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-216">A string that contains the definition of the map.</span></span>

#### <a name="remarks"></a><span data-ttu-id="f7b4f-217">備考</span><span class="sxs-lookup"><span data-stu-id="f7b4f-217">Remarks</span></span>

<span data-ttu-id="f7b4f-218">マップの定義。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-218">The definition of the map.</span></span>

#### <a name="examples"></a><span data-ttu-id="f7b4f-219">例</span><span class="sxs-lookup"><span data-stu-id="f7b4f-219">Examples</span></span>

<span data-ttu-id="f7b4f-220">次の例では、マップを作成し、マップの定義を出力します。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-220">The following example creates a map and then prints the definition of the map.</span></span>

    { 
        Map myMap = new Map(Types::Integer, Types::String); 
        print myMap.definitionString(); 
        pause; 
    }

### <a name="method-domainset"></a><span data-ttu-id="f7b4f-221">メソッド domainSet</span><span class="sxs-lookup"><span data-stu-id="f7b4f-221">Method domainSet</span></span>

<span data-ttu-id="f7b4f-222">マップにキー (ドメイン) 値のセットを作成します。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-222">Creates a set of the key (domain) values in a map.</span></span>

    public Set domainSet()

#### <a name="return-value"></a><span data-ttu-id="f7b4f-223">戻り値</span><span class="sxs-lookup"><span data-stu-id="f7b4f-223">Return Value</span></span>

#### <a name="remarks"></a><span data-ttu-id="f7b4f-224">備考</span><span class="sxs-lookup"><span data-stu-id="f7b4f-224">Remarks</span></span>

<span data-ttu-id="f7b4f-225">このメソッドは廃止されました。代わりに Map.keySet を使用してください。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-225">This method is obsolete; use the Map.keySet method instead.</span></span>

### <a name="method-domaintype"></a><span data-ttu-id="f7b4f-226">メソッド domainType</span><span class="sxs-lookup"><span data-stu-id="f7b4f-226">Method domainType</span></span>

<span data-ttu-id="f7b4f-227">マップ内のキー (ドメイン) 値のタイプを決定します。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-227">Determines the type of the key (domain) values in a map.</span></span>

    public Types domainType()

#### <a name="return-value"></a><span data-ttu-id="f7b4f-228">戻り値</span><span class="sxs-lookup"><span data-stu-id="f7b4f-228">Return Value</span></span>

#### <a name="remarks"></a><span data-ttu-id="f7b4f-229">備考</span><span class="sxs-lookup"><span data-stu-id="f7b4f-229">Remarks</span></span>

<span data-ttu-id="f7b4f-230">このメソッドは廃止されました。代わりに Map.keyType を使用してください。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-230">This method is obsolete; use the Map.keyType method instead.</span></span>

### <a name="method-elements"></a><span data-ttu-id="f7b4f-231">メソッド elements</span><span class="sxs-lookup"><span data-stu-id="f7b4f-231">Method elements</span></span>

<span data-ttu-id="f7b4f-232">マップ内の要素の数を返します。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-232">Returns the number of elements in the map.</span></span>

    public int elements()

#### <a name="return-value"></a><span data-ttu-id="f7b4f-233">戻り値</span><span class="sxs-lookup"><span data-stu-id="f7b4f-233">Return Value</span></span>

<span data-ttu-id="f7b4f-234">マップ内の要素の数。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-234">The number of elements in the map.</span></span>

#### <a name="remarks"></a><span data-ttu-id="f7b4f-235">備考</span><span class="sxs-lookup"><span data-stu-id="f7b4f-235">Remarks</span></span>

<span data-ttu-id="f7b4f-236">マップ内の要素の数はマップ内の異なるキー値の数と同等になります。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-236">The number of elements in the map is equal to the number of different key values in the map.</span></span>

#### <a name="examples"></a><span data-ttu-id="f7b4f-237">例</span><span class="sxs-lookup"><span data-stu-id="f7b4f-237">Examples</span></span>

<span data-ttu-id="f7b4f-238">次の例では、elements メソッドを使用して、マップに要素があるかどうかを確認します。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-238">The following example uses the elements method to check whether a map has any elements.</span></span> <span data-ttu-id="f7b4f-239">\_マップ元が存在し、一部の要素を持っている場合、\_マップ元の値は\_マップ先へ挿入されます。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-239">If the \_from map exists and has some elements, the values from the \_from map are inserted into the \_to map.</span></span>

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

### <a name="method-empty"></a><span data-ttu-id="f7b4f-240">メソッド empty</span><span class="sxs-lookup"><span data-stu-id="f7b4f-240">Method empty</span></span>

<span data-ttu-id="f7b4f-241">マップに (キー、値) のペアが含まれているかどうかを判定します。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-241">Determines whether the map contains any (key, value) pairs.</span></span>

    public boolean empty()

#### <a name="return-value"></a><span data-ttu-id="f7b4f-242">戻り値</span><span class="sxs-lookup"><span data-stu-id="f7b4f-242">Return Value</span></span>

<span data-ttu-id="f7b4f-243">マップに要素が存在しない場合に true。それ以外の場合は false。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-243">true if the map does not contain any elements; otherwise, false.</span></span>

#### <a name="remarks"></a><span data-ttu-id="f7b4f-244">備考</span><span class="sxs-lookup"><span data-stu-id="f7b4f-244">Remarks</span></span>

<span data-ttu-id="f7b4f-245">このメソッドは、(elements() == 0) と等価です。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-245">This method is equivalent to (elements() == 0).</span></span>

### <a name="method-exists"></a><span data-ttu-id="f7b4f-246">メソッド exists</span><span class="sxs-lookup"><span data-stu-id="f7b4f-246">Method exists</span></span>

<span data-ttu-id="f7b4f-247">特定の値がマップ内のキーとして存在するかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-247">Determines whether a particular value exists as a key in the map.</span></span>

    public boolean exists(AnyType keyValue)

#### <a name="parameters"></a><span data-ttu-id="f7b4f-248">パラメーター</span><span class="sxs-lookup"><span data-stu-id="f7b4f-248">Parameters</span></span>

<span data-ttu-id="f7b4f-249">keyValue</span><span class="sxs-lookup"><span data-stu-id="f7b4f-249">keyValue</span></span>  
<span data-ttu-id="f7b4f-250">確認する値。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-250">The value to check for.</span></span>

#### <a name="return-value"></a><span data-ttu-id="f7b4f-251">戻り値</span><span class="sxs-lookup"><span data-stu-id="f7b4f-251">Return Value</span></span>

<span data-ttu-id="f7b4f-252">指定されたキー値がマップ内に存在する場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-252">true if the specified key value exists in the map; otherwise, false.</span></span>

#### <a name="remarks"></a><span data-ttu-id="f7b4f-253">備考</span><span class="sxs-lookup"><span data-stu-id="f7b4f-253">Remarks</span></span>

<span data-ttu-id="f7b4f-254">Map.lookup メソッドへの呼び出しを保護するには、このメソッドを使用します。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-254">Use this method to guard calls to the Map.lookup method.</span></span> <span data-ttu-id="f7b4f-255">Map.lookup メソッドで、検索値が見つからなかった場合、例外が発生されます。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-255">If the Map.lookup method does not find the value that it is looking for, it throws an exception.</span></span>

#### <a name="examples"></a><span data-ttu-id="f7b4f-256">例</span><span class="sxs-lookup"><span data-stu-id="f7b4f-256">Examples</span></span>

<span data-ttu-id="f7b4f-257">次の例では、スタイル シート内のスタイルのマップに特定のスタイルが存在するかどうかを確認します。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-257">The following example checks whether a particular style exists in a map of styles in a style sheet.</span></span> <span data-ttu-id="f7b4f-258">存在する場合は、本文のスタイルの新しい名前に置き換えられます。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-258">If it does, a new name is substituted for the body style.</span></span>

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

### <a name="method-getenumerator"></a><span data-ttu-id="f7b4f-259">メソッド getEnumerator</span><span class="sxs-lookup"><span data-stu-id="f7b4f-259">Method getEnumerator</span></span>

<span data-ttu-id="f7b4f-260">マップ内のスキャンを可能にする、マップの列挙子を作成します。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-260">Creates an enumerator for the map, which lets you traverse the map.</span></span>

    public MapEnumerator getEnumerator()

#### <a name="return-value"></a><span data-ttu-id="f7b4f-261">戻り値</span><span class="sxs-lookup"><span data-stu-id="f7b4f-261">Return Value</span></span>

<span data-ttu-id="f7b4f-262">マップの MapEnumerator オブジェクト。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-262">A MapEnumerator object for the map.</span></span>

#### <a name="examples"></a><span data-ttu-id="f7b4f-263">例</span><span class="sxs-lookup"><span data-stu-id="f7b4f-263">Examples</span></span>

<span data-ttu-id="f7b4f-264">次の例では \_from マップに要素があるかどうかを確認し、要素がある場合はマップの列挙子を作成します。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-264">The following example checks whether the \_from map has any elements and creates an enumerator for the map if it has any elements.</span></span> <span data-ttu-id="f7b4f-265">次に、マップが移動し、その中の要素が \_to マップに挿入されます。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-265">The map is then traversed, and the elements in it are inserted into the \_to map.</span></span>

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

### <a name="method-insert"></a><span data-ttu-id="f7b4f-266">メソッド insert</span><span class="sxs-lookup"><span data-stu-id="f7b4f-266">Method insert</span></span>

<span data-ttu-id="f7b4f-267">マップに要素 (keyValue、valueValue ペア) を挿入します。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-267">Inserts an element (keyValue, valueValue pair) into the map.</span></span>

    public boolean insert(AnyType keyValue, AnyType valueValue)

#### <a name="parameters"></a><span data-ttu-id="f7b4f-268">パラメーター</span><span class="sxs-lookup"><span data-stu-id="f7b4f-268">Parameters</span></span>

<span data-ttu-id="f7b4f-269">keyValue</span><span class="sxs-lookup"><span data-stu-id="f7b4f-269">keyValue</span></span>  
<span data-ttu-id="f7b4f-270">キーによりマッピングされている値。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-270">The value that is mapped to by the key.</span></span>

<!-- -->

<span data-ttu-id="f7b4f-271">valueValue</span><span class="sxs-lookup"><span data-stu-id="f7b4f-271">valueValue</span></span>  
<span data-ttu-id="f7b4f-272">キーによりマッピングされている値。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-272">The value that is mapped to by the key.</span></span>

#### <a name="return-value"></a><span data-ttu-id="f7b4f-273">戻り値</span><span class="sxs-lookup"><span data-stu-id="f7b4f-273">Return Value</span></span>

<span data-ttu-id="f7b4f-274">キーがマップにまだ存在せず、マップが挿入された場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-274">true if the key did not already exist in the map and has been inserted; otherwise, false.</span></span>

#### <a name="remarks"></a><span data-ttu-id="f7b4f-275">備考</span><span class="sxs-lookup"><span data-stu-id="f7b4f-275">Remarks</span></span>

<span data-ttu-id="f7b4f-276">キーが既にマップに存在する場合は、値が更新されます。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-276">If the key already exists in the map, the value is updated.</span></span>

#### <a name="examples"></a><span data-ttu-id="f7b4f-277">例</span><span class="sxs-lookup"><span data-stu-id="f7b4f-277">Examples</span></span>

<span data-ttu-id="f7b4f-278">次の例では \_from マップに要素があるかどうかを確認し、要素がある場合はマップの列挙子を作成します。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-278">The following example checks whether the \_from map has any elements and creates an enumerator for the map if it has any elements.</span></span> <span data-ttu-id="f7b4f-279">マップが移動し、\_from マップから \_to マップに要素を挿入するために insert メソッドが使用されます。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-279">The map is traversed, and the insert method is used to insert the elements from the \_from map into the \_to map.</span></span>

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

### <a name="method-keyset"></a><span data-ttu-id="f7b4f-280">メソッド keySet</span><span class="sxs-lookup"><span data-stu-id="f7b4f-280">Method keySet</span></span>

<span data-ttu-id="f7b4f-281">マップからのキー値を含むセットを返します。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-281">Returns a set that contains the key values from a map.</span></span>

    public Set keySet()

#### <a name="return-value"></a><span data-ttu-id="f7b4f-282">戻り値</span><span class="sxs-lookup"><span data-stu-id="f7b4f-282">Return Value</span></span>

<span data-ttu-id="f7b4f-283">キー値を含むセット。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-283">A set that contains the key values.</span></span>

#### <a name="examples"></a><span data-ttu-id="f7b4f-284">例</span><span class="sxs-lookup"><span data-stu-id="f7b4f-284">Examples</span></span>

<span data-ttu-id="f7b4f-285">次の例では、セット内の要素として検出されないキー値を持つすべての要素をマップから削除します。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-285">The following example deletes all elements from a map that have key values that are not found as elements in a set.</span></span>

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

### <a name="method-keytype"></a><span data-ttu-id="f7b4f-286">メソッド keyType</span><span class="sxs-lookup"><span data-stu-id="f7b4f-286">Method keyType</span></span>

<span data-ttu-id="f7b4f-287">マップ内のキー値のタイプを返します。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-287">Returns the type of the key values in a map.</span></span>

    public Types keyType()

#### <a name="return-value"></a><span data-ttu-id="f7b4f-288">戻り値</span><span class="sxs-lookup"><span data-stu-id="f7b4f-288">Return Value</span></span>

<span data-ttu-id="f7b4f-289">キー値のタイプ。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-289">The type of the key values.</span></span>

#### <a name="remarks"></a><span data-ttu-id="f7b4f-290">備考</span><span class="sxs-lookup"><span data-stu-id="f7b4f-290">Remarks</span></span>

<span data-ttu-id="f7b4f-291">可能な戻り値は、Types システム列挙で説明されます。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-291">The possible return values are outlined by the Types system enum.</span></span> <span data-ttu-id="f7b4f-292">キー値のタイプは、マップの作成時に決定されます。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-292">The type of the key values is determined when the map is constructed.</span></span> <span data-ttu-id="f7b4f-293">これは Map.new メソッドに対する最初のパラメーターとして指定されます。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-293">It is supplied as the first parameter to the Map.new method.</span></span>

### <a name="method-lookup"></a><span data-ttu-id="f7b4f-294">メソッド lookup</span><span class="sxs-lookup"><span data-stu-id="f7b4f-294">Method lookup</span></span>

<span data-ttu-id="f7b4f-295">指定されたキー値によりマッピングされている値を返します。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-295">Returns the value that is mapped to by a specified key value.</span></span>

    public AnyType lookup(AnyType keyValue)

#### <a name="parameters"></a><span data-ttu-id="f7b4f-296">パラメーター</span><span class="sxs-lookup"><span data-stu-id="f7b4f-296">Parameters</span></span>

<span data-ttu-id="f7b4f-297">keyValue</span><span class="sxs-lookup"><span data-stu-id="f7b4f-297">keyValue</span></span>  
<span data-ttu-id="f7b4f-298">検索するキー。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-298">The key to find.</span></span>

#### <a name="return-value"></a><span data-ttu-id="f7b4f-299">戻り値</span><span class="sxs-lookup"><span data-stu-id="f7b4f-299">Return Value</span></span>

<span data-ttu-id="f7b4f-300">キーにより指定されている値。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-300">The value that is mapped to by the specified key.</span></span>

#### <a name="remarks"></a><span data-ttu-id="f7b4f-301">備考</span><span class="sxs-lookup"><span data-stu-id="f7b4f-301">Remarks</span></span>

<span data-ttu-id="f7b4f-302">マップ内にキーが見つからない場合、Map.exists メソッドを使用して取得する値が存在するかどうかを確認し例外がスローされます。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-302">An exception is thrown if the key is not found in the map, so check whether the value that you want to retrieve exists by using the Map.exists method.</span></span>

#### <a name="examples"></a><span data-ttu-id="f7b4f-303">例</span><span class="sxs-lookup"><span data-stu-id="f7b4f-303">Examples</span></span>

<span data-ttu-id="f7b4f-304">次の例では、スタイル シート内のスタイルのマップに特定のスタイルが存在するかどうかを確認します。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-304">The following example checks whether a particular style exists in a map of styles in a style sheet.</span></span> <span data-ttu-id="f7b4f-305">存在する場合は、本文のスタイルの新しい名前に置き換えられます。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-305">If it does, a new name is substituted for the body style.</span></span>

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

### <a name="method-pack"></a><span data-ttu-id="f7b4f-306">メソッド pack</span><span class="sxs-lookup"><span data-stu-id="f7b4f-306">Method pack</span></span>

<span data-ttu-id="f7b4f-307">Map クラスの現在のインスタンスをシリアル化します。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-307">Serializes the current instance of the Map class.</span></span>

    public container pack()

#### <a name="return-value"></a><span data-ttu-id="f7b4f-308">戻り値</span><span class="sxs-lookup"><span data-stu-id="f7b4f-308">Return Value</span></span>

<span data-ttu-id="f7b4f-309">Map クラスの現在のインスタンスを含むコンテナーです。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-309">A container that contains the current instance of the Map class.</span></span>

#### <a name="remarks"></a><span data-ttu-id="f7b4f-310">備考</span><span class="sxs-lookup"><span data-stu-id="f7b4f-310">Remarks</span></span>

<span data-ttu-id="f7b4f-311">このメソッドで作成されたコンテナーには、マップの最初の要素の前に 4 つの要素が含まれます。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-311">The container created by this method contains 4 elements before the first element from the map:</span></span>

-   <span data-ttu-id="f7b4f-312">コンテナのバージョン番号</span><span class="sxs-lookup"><span data-stu-id="f7b4f-312">A version number for the container</span></span>
-   <span data-ttu-id="f7b4f-313">マップ内のキーのデータ型を識別する整数</span><span class="sxs-lookup"><span data-stu-id="f7b4f-313">An integer that identifies the data type of the keys in the map</span></span>
-   <span data-ttu-id="f7b4f-314">マップ内の値のデータ型を識別する整数</span><span class="sxs-lookup"><span data-stu-id="f7b4f-314">An integer that identifies the data type of the values in the map</span></span>
-   <span data-ttu-id="f7b4f-315">マップ内の要素の数。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-315">The number of elements in the map</span></span>

<span data-ttu-id="f7b4f-316">キーまたは値がオブジェクトになっている場合は、梱包は、各オブジェクトに対して pack メソッドを連続して呼び出し、サブコンテナーを取得することによって行われます。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-316">If the keys or the values are objects, packing is performed by calling the pack method successively on each object to yield a subcontainer.</span></span> <span data-ttu-id="f7b4f-317">pack メソッドと unpack メソッドは、X++ anytype 値を保持できません。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-317">The pack and unpack methods cannot preserve X++ anytype values.</span></span> <span data-ttu-id="f7b4f-318">1 つのオプションは、anytype 値をオブジェクトまたは構造体に格納し、構造体をマップ オブジェクトの値にすることです。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-318">One option is to put the anytype values into objects or structs, and have the structs be the values in the Map object.</span></span> <span data-ttu-id="f7b4f-319">Microsoft .NET System.Collections クラスは別のオプションで使用します。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-319">Use of Microsoft .NET System.Collections classes is another option.</span></span> <span data-ttu-id="f7b4f-320">Map.create メソッドを使用して、パックされたコンテナーからマップを取得できます。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-320">The map can be retrieved from the packed container by using the Map.create method.</span></span>

#### <a name="examples"></a><span data-ttu-id="f7b4f-321">例</span><span class="sxs-lookup"><span data-stu-id="f7b4f-321">Examples</span></span>

<span data-ttu-id="f7b4f-322">次の例では、メソッド (conprojItemTransSalesAmount) に渡されたコンテナーからマップを作成し、いくつかの値を追加して MapEnumerator.pack を使用してマップをコンテナーにパックします。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-322">The following example creates a map from a container that is passed into the method (conprojItemTransSalesAmount), adds some values to it, and then uses MapEnumerator.pack to pack the map into a container.</span></span> <span data-ttu-id="f7b4f-323">このメソッドによって新しいコンテナーが返されます。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-323">The new container is then returned by the method.</span></span>

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

### <a name="method-rangeset"></a><span data-ttu-id="f7b4f-324">メソッド rangeSet</span><span class="sxs-lookup"><span data-stu-id="f7b4f-324">Method rangeSet</span></span>

<span data-ttu-id="f7b4f-325">マップ内のキーによってマップされる値 (範囲) を含むセットを返します。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-325">Returns a set that contains the values (ranges) that are mapped to by the keys in a map.</span></span>

    public Set rangeSet()

#### <a name="return-value"></a><span data-ttu-id="f7b4f-326">戻り値</span><span class="sxs-lookup"><span data-stu-id="f7b4f-326">Return Value</span></span>

#### <a name="remarks"></a><span data-ttu-id="f7b4f-327">備考</span><span class="sxs-lookup"><span data-stu-id="f7b4f-327">Remarks</span></span>

<span data-ttu-id="f7b4f-328">このメソッドは廃止されました。代わりに Map.valueSet を使用してください。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-328">This method is obsolete; use the Map.valueSet method instead.</span></span>

### <a name="method-rangetype"></a><span data-ttu-id="f7b4f-329">メソッド rangeType</span><span class="sxs-lookup"><span data-stu-id="f7b4f-329">Method rangeType</span></span>

<span data-ttu-id="f7b4f-330">マップ内のキーによってマップされる値 (範囲) のタイプを決定します。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-330">Determines the type of the values (ranges) that are mapped to by the keys in a map.</span></span>

    public Types rangeType()

#### <a name="return-value"></a><span data-ttu-id="f7b4f-331">戻り値</span><span class="sxs-lookup"><span data-stu-id="f7b4f-331">Return Value</span></span>

#### <a name="remarks"></a><span data-ttu-id="f7b4f-332">備考</span><span class="sxs-lookup"><span data-stu-id="f7b4f-332">Remarks</span></span>

<span data-ttu-id="f7b4f-333">このメソッドは廃止されました。代わりに valueType を使用してください。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-333">This method is obsolete; use the valueType method instead.</span></span>

### <a name="method-remove"></a><span data-ttu-id="f7b4f-334">メソッド remove</span><span class="sxs-lookup"><span data-stu-id="f7b4f-334">Method remove</span></span>

<span data-ttu-id="f7b4f-335">(キー、値) ペアをマップから削除します。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-335">Removes a (key, value) pair from a map.</span></span>

    public boolean remove(AnyType keyValue)

#### <a name="parameters"></a><span data-ttu-id="f7b4f-336">パラメーター</span><span class="sxs-lookup"><span data-stu-id="f7b4f-336">Parameters</span></span>

<span data-ttu-id="f7b4f-337">keyValue</span><span class="sxs-lookup"><span data-stu-id="f7b4f-337">keyValue</span></span>  
<span data-ttu-id="f7b4f-338">削除するキーの値。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-338">The value of the key to delete.</span></span>

#### <a name="return-value"></a><span data-ttu-id="f7b4f-339">戻り値</span><span class="sxs-lookup"><span data-stu-id="f7b4f-339">Return Value</span></span>

<span data-ttu-id="f7b4f-340">キーがマップ内に見つかり、要素が削除された場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-340">true if the key was found in the map and the element has been deleted; otherwise, false.</span></span>

#### <a name="examples"></a><span data-ttu-id="f7b4f-341">例</span><span class="sxs-lookup"><span data-stu-id="f7b4f-341">Examples</span></span>

<span data-ttu-id="f7b4f-342">次の例では、特定のキー値がマップに存在するかどうかを確認します。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-342">The following example checks whether a particular key value exists in a map.</span></span> <span data-ttu-id="f7b4f-343">値が存在する場合は、メソッドがキーと対応する値を削除します。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-343">If the value exists, the method deletes the key and its corresponding value.</span></span> <span data-ttu-id="f7b4f-344">このメソッドは、値が見つかった場合は true を返し、キーがマップに存在しない場合は false を返します。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-344">The method returns true if the value was found and false if the key did not exist in the map.</span></span>

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

### <a name="method-tostring"></a><span data-ttu-id="f7b4f-345">メソッド toString</span><span class="sxs-lookup"><span data-stu-id="f7b4f-345">Method toString</span></span>

<span data-ttu-id="f7b4f-346">マップ内の (キー、値) ペアの説明を返します。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-346">Returns a description of the (key, value) pairs in the map.</span></span>

    public str toString()

#### <a name="return-value"></a><span data-ttu-id="f7b4f-347">戻り値</span><span class="sxs-lookup"><span data-stu-id="f7b4f-347">Return Value</span></span>

<span data-ttu-id="f7b4f-348">マップの要素の説明を含む文字列。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-348">A string that contains a description of the elements in the map.</span></span>

#### <a name="examples"></a><span data-ttu-id="f7b4f-349">例</span><span class="sxs-lookup"><span data-stu-id="f7b4f-349">Examples</span></span>

<span data-ttu-id="f7b4f-350">次の例では、マップを作成し、いくつかの要素を追加してから、これらの要素の説明を出力します。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-350">The following example creates a map, adds some elements to it, and then prints a description of these elements.</span></span>

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

### <a name="method-valueset"></a><span data-ttu-id="f7b4f-351">メソッド valueSet</span><span class="sxs-lookup"><span data-stu-id="f7b4f-351">Method valueSet</span></span>

<span data-ttu-id="f7b4f-352">マップ内のキーによってマップされる値を含むセットを返します。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-352">Returns a set that contains the values that are mapped to by the keys in a map.</span></span>

    public Set valueSet()

#### <a name="return-value"></a><span data-ttu-id="f7b4f-353">戻り値</span><span class="sxs-lookup"><span data-stu-id="f7b4f-353">Return Value</span></span>

<span data-ttu-id="f7b4f-354">マップからの値を含むセット。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-354">A set that contains the values from the map.</span></span>

#### <a name="remarks"></a><span data-ttu-id="f7b4f-355">備考</span><span class="sxs-lookup"><span data-stu-id="f7b4f-355">Remarks</span></span>

<span data-ttu-id="f7b4f-356">すべてのキーが、別の値にマップされる場合、セット内の要素の数はマップ内の要素の数と同等になります。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-356">If all the keys map to different values, the number of elements in the set is equal to the number of elements in the map.</span></span>

### <a name="method-valuetype"></a><span data-ttu-id="f7b4f-357">メソッド valueType</span><span class="sxs-lookup"><span data-stu-id="f7b4f-357">Method valueType</span></span>

<span data-ttu-id="f7b4f-358">マップ内のキーによってマップされる値のタイプを返します。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-358">Returns the type of the values that are mapped to by the keys in a map.</span></span>

    public Types valueType()

#### <a name="return-value"></a><span data-ttu-id="f7b4f-359">戻り値</span><span class="sxs-lookup"><span data-stu-id="f7b4f-359">Return Value</span></span>

<span data-ttu-id="f7b4f-360">キーによってマップされる値のタイプ。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-360">The type of the values that are mapped to by the keys.</span></span>

#### <a name="remarks"></a><span data-ttu-id="f7b4f-361">備考</span><span class="sxs-lookup"><span data-stu-id="f7b4f-361">Remarks</span></span>

<span data-ttu-id="f7b4f-362">キー値のタイプは、マップの作成時に決定されます。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-362">The type of the key values is determined when the map is constructed.</span></span> <span data-ttu-id="f7b4f-363">これは Map.new メソッドに対する最初のパラメーターとして指定されます。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-363">It is supplied as the first parameter to the Map.new method.</span></span>

### <a name="method-xml"></a><span data-ttu-id="f7b4f-364">メソッド xml</span><span class="sxs-lookup"><span data-stu-id="f7b4f-364">Method xml</span></span>

<span data-ttu-id="f7b4f-365">現在のオブジェクトを表す XML 文字列を返します。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-365">Returns an XML string that represents the current object.</span></span>

    public str xml([int indent])

#### <a name="parameters"></a><span data-ttu-id="f7b4f-366">パラメーター</span><span class="sxs-lookup"><span data-stu-id="f7b4f-366">Parameters</span></span>

<span data-ttu-id="f7b4f-367">インデント</span><span class="sxs-lookup"><span data-stu-id="f7b4f-367">indent</span></span>  
<span data-ttu-id="f7b4f-368">返される XML 文字列のインデントの量 (省略可能)。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-368">The amount of indentation of the XML string that is returned; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="f7b4f-369">戻り値</span><span class="sxs-lookup"><span data-stu-id="f7b4f-369">Return Value</span></span>

<span data-ttu-id="f7b4f-370">現在のオブジェクトを表す XML 文字列です。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-370">An XML string that represents the current object.</span></span>

#### <a name="remarks"></a><span data-ttu-id="f7b4f-371">備考</span><span class="sxs-lookup"><span data-stu-id="f7b4f-371">Remarks</span></span>

<span data-ttu-id="f7b4f-372">このメソッドをオーバーライドして、その型に対して意味のある値を返すことができます。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-372">This method can be overridden to return values that are meaningful for that type.</span></span>

### <a name="method-create"></a><span data-ttu-id="f7b4f-373">メソッド create</span><span class="sxs-lookup"><span data-stu-id="f7b4f-373">Method create</span></span>

<span data-ttu-id="f7b4f-374">以前の Map.pack メソッドの呼び出しで取得されたコンテナーからマップを作成します。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-374">Creates a map from the container that was obtained from a previous call to the Map.pack method.</span></span>

    public static Map create(container container)

#### <a name="parameters"></a><span data-ttu-id="f7b4f-375">パラメーター</span><span class="sxs-lookup"><span data-stu-id="f7b4f-375">Parameters</span></span>

<span data-ttu-id="f7b4f-376">コンテナー</span><span class="sxs-lookup"><span data-stu-id="f7b4f-376">container</span></span>  

#### <a name="return-value"></a><span data-ttu-id="f7b4f-377">戻り値</span><span class="sxs-lookup"><span data-stu-id="f7b4f-377">Return Value</span></span>

<span data-ttu-id="f7b4f-378">Map.pack メソッドでコンテナーに梱包されたマップと同等のマップ。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-378">A map that is equal to the map that was packed into the container by the Map.pack method.</span></span>

#### <a name="remarks"></a><span data-ttu-id="f7b4f-379">備考</span><span class="sxs-lookup"><span data-stu-id="f7b4f-379">Remarks</span></span>

<span data-ttu-id="f7b4f-380">キーまたは値がオブジェクトの場合、オブジェクトにはコンテナーからその内部状態を再設定するために呼び出されるアンパック メソッドが必要です。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-380">If the keys or values are objects, the objects must have an unpack method that is called to re-establish their internal state from the container.</span></span>

#### <a name="examples"></a><span data-ttu-id="f7b4f-381">例</span><span class="sxs-lookup"><span data-stu-id="f7b4f-381">Examples</span></span>

<span data-ttu-id="f7b4f-382">次の例では、メソッド (conprojItemTransSalesAmount) に渡されたコンテナーからマップを作成し、コンテナーに値を追加してマップをパックし、新しいコンテナーとして返します。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-382">The following example creates a map from a container that is passed into the method (conprojItemTransSalesAmount), adds some values to the container, and then packs the map and returns it as a new container.</span></span>

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

### <a name="method-createfromxml"></a><span data-ttu-id="f7b4f-383">メソッド createFromXML</span><span class="sxs-lookup"><span data-stu-id="f7b4f-383">Method createFromXML</span></span>

    public static Map createFromXML(Object xmlnode)

#### <a name="parameters"></a><span data-ttu-id="f7b4f-384">パラメーター</span><span class="sxs-lookup"><span data-stu-id="f7b4f-384">Parameters</span></span>

<span data-ttu-id="f7b4f-385">xmlnode</span><span class="sxs-lookup"><span data-stu-id="f7b4f-385">xmlnode</span></span>  

#### <a name="return-value"></a><span data-ttu-id="f7b4f-386">戻り値</span><span class="sxs-lookup"><span data-stu-id="f7b4f-386">Return Value</span></span>

### <a name="method-equal"></a><span data-ttu-id="f7b4f-387">メソッド equal</span><span class="sxs-lookup"><span data-stu-id="f7b4f-387">Method equal</span></span>

<span data-ttu-id="f7b4f-388">2 つのマップが等しいかどうかを判断します。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-388">Determines whether two maps are equal.</span></span>

    public static boolean equal(Map map1, Map map2)

#### <a name="parameters"></a><span data-ttu-id="f7b4f-389">パラメーター</span><span class="sxs-lookup"><span data-stu-id="f7b4f-389">Parameters</span></span>

<span data-ttu-id="f7b4f-390">map1</span><span class="sxs-lookup"><span data-stu-id="f7b4f-390">map1</span></span>  
<span data-ttu-id="f7b4f-391">比較する 2 つ目のマップ。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-391">The second map to compare.</span></span>

<!-- -->

<span data-ttu-id="f7b4f-392">map2</span><span class="sxs-lookup"><span data-stu-id="f7b4f-392">map2</span></span>  
<span data-ttu-id="f7b4f-393">比較する 2 つ目のマップ。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-393">The second map to compare.</span></span>

#### <a name="return-value"></a><span data-ttu-id="f7b4f-394">戻り値</span><span class="sxs-lookup"><span data-stu-id="f7b4f-394">Return Value</span></span>

<span data-ttu-id="f7b4f-395">2 つのマップが等しい場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-395">true if the two maps are equal; otherwise, false.</span></span>

#### <a name="remarks"></a><span data-ttu-id="f7b4f-396">備考</span><span class="sxs-lookup"><span data-stu-id="f7b4f-396">Remarks</span></span>

<span data-ttu-id="f7b4f-397">2 つのマップが同じ数の要素を含み、キー セットが同じで、キー セットの各キーが両方のマップの同じ値にマップされている場合、2 つのマップは同等です。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-397">Two maps are equal if they contain the same number of elements, their key sets are the same, and each key in the key set maps to the same value in both maps.</span></span>

### <a name="method-new"></a><span data-ttu-id="f7b4f-398">メソッド new</span><span class="sxs-lookup"><span data-stu-id="f7b4f-398">Method new</span></span>

<span data-ttu-id="f7b4f-399">新しいマップを作成します</span><span class="sxs-lookup"><span data-stu-id="f7b4f-399">Creates a new map.</span></span>

    public void new(Types key, Types value)

#### <a name="parameters"></a><span data-ttu-id="f7b4f-400">パラメーター</span><span class="sxs-lookup"><span data-stu-id="f7b4f-400">Parameters</span></span>

<span data-ttu-id="f7b4f-401">キー</span><span class="sxs-lookup"><span data-stu-id="f7b4f-401">key</span></span>  
<span data-ttu-id="f7b4f-402">値のタイプ。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-402">The type of the values.</span></span>

<!-- -->

<span data-ttu-id="f7b4f-403">値</span><span class="sxs-lookup"><span data-stu-id="f7b4f-403">value</span></span>  
<span data-ttu-id="f7b4f-404">値のタイプ。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-404">The type of the values.</span></span>

#### <a name="examples"></a><span data-ttu-id="f7b4f-405">例</span><span class="sxs-lookup"><span data-stu-id="f7b4f-405">Examples</span></span>

<span data-ttu-id="f7b4f-406">次の例では、文字列キーを整数値にマッピングするマップを作成します。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-406">The following example creates a map that maps string keys to integer values.</span></span>

    Map myMap = new Map(Types::String, Types::Integer);

## <a name="class-mapenumerator"></a><span data-ttu-id="f7b4f-407">クラス MapEnumerator</span><span class="sxs-lookup"><span data-stu-id="f7b4f-407">Class MapEnumerator</span></span>
    class MapEnumerator extends Object

<span data-ttu-id="f7b4f-408">MapEnumerator クラスを使用すると、マップ内の要素上を移動できます。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-408">The MapEnumerator class lets you traverse through the elements in a map.</span></span>

### <a name="remarks"></a><span data-ttu-id="f7b4f-409">備考</span><span class="sxs-lookup"><span data-stu-id="f7b4f-409">Remarks</span></span>

<span data-ttu-id="f7b4f-410">マップ列挙子は、リストの最初の要素の前に開始します。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-410">Map enumerators start before the first element in the list.</span></span> <span data-ttu-id="f7b4f-411">リストの最初の要素を指すようにするために MapEnumerator.moveNext メソッドを呼び出す必要があります。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-411">You must call the MapEnumerator.moveNext method to make it point to the first element in the list.</span></span> <span data-ttu-id="f7b4f-412">Map.getEnumerator メソッドが呼び出されたときに、マップと同じ層で列挙子が自動的に作成されるため、MapIterator クラスではなく、MapEnumerator クラスを使用することがベスト プラクティスです。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-412">It is a best practice to use the MapEnumerator class instead of the MapIterator class because enumerators are automatically created on the same tier as the map when you call the Map.getEnumerator method.</span></span> <span data-ttu-id="f7b4f-413">MapEnumerator クラスを使用すると、Called from としてマークされたコードの潜在的な問題が回避されます。反復子とマップは別々の層に置くことができます。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-413">Using the MapEnumerator class avoids a potential problem in code marked as Called from, where the iterator and map can end up on separate tiers.</span></span> <span data-ttu-id="f7b4f-414">さらに、マップ列挙子はマップ反復子よりも少ないコードを必要とするためパフォーマンスが少し向上します。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-414">In addition, because map enumerators require less code than map iterators, they perform slightly better.</span></span> <span data-ttu-id="f7b4f-415">マップ反復子を使用する必要がある唯一の状況は、MapIterator.delete メソッドを使用してリストから項目を削除する場合です。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-415">The only situation where you have to use a map iterator, is when you want to delete items from a list by using the MapIterator.delete method.</span></span>

### <a name="examples"></a><span data-ttu-id="f7b4f-416">例</span><span class="sxs-lookup"><span data-stu-id="f7b4f-416">Examples</span></span>

### <a name="methods"></a><span data-ttu-id="f7b4f-417">メソッド</span><span class="sxs-lookup"><span data-stu-id="f7b4f-417">Methods</span></span>

| <span data-ttu-id="f7b4f-418">方法</span><span class="sxs-lookup"><span data-stu-id="f7b4f-418">Method</span></span>                        | <span data-ttu-id="f7b4f-419">説明</span><span class="sxs-lookup"><span data-stu-id="f7b4f-419">Description</span></span>                                                                                                                                       |
|-------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f7b4f-420">public AnyType current()</span><span class="sxs-lookup"><span data-stu-id="f7b4f-420">public AnyType current()</span></span>      | <span data-ttu-id="f7b4f-421">このメソッドは廃止されました。代わりに MapEnumerator.currentKey を使用してください。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-421">This method is obsolete; use MapEnumerator.currentKey instead.</span></span>                                                                                    |
| <span data-ttu-id="f7b4f-422">public AnyType currentKey()</span><span class="sxs-lookup"><span data-stu-id="f7b4f-422">public AnyType currentKey()</span></span>   | <span data-ttu-id="f7b4f-423">現在列挙子によってポイントされている (キー、値) ペアからキーを返します。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-423">Returns the key from the (key, value) pair that is currently pointed to by the enumerator.</span></span>                                                        |
| <span data-ttu-id="f7b4f-424">public AnyType currentValue()</span><span class="sxs-lookup"><span data-stu-id="f7b4f-424">public AnyType currentValue()</span></span> | <span data-ttu-id="f7b4f-425">現在列挙子によってポイントされている (キー、値) ペアから値を返します。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-425">Returns the value from the (key, value) pair that is currently pointed to by the enumerator.</span></span>                                                      |
| <span data-ttu-id="f7b4f-426">public str definitionString()</span><span class="sxs-lookup"><span data-stu-id="f7b4f-426">public str definitionString()</span></span> | <span data-ttu-id="f7b4f-427">列挙子の説明を返します。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-427">Returns a description of the enumerator.</span></span> <span data-ttu-id="f7b4f-428">たとえば、文字列への整数のマップの列挙子は、「\[int -&gt; str\] 列挙子」を返します。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-428">For example, an enumerator for a map of integers to strings would return "\[int -&gt; str\] enumerator".</span></span> |
| <span data-ttu-id="f7b4f-429">public boolean moveNext()</span><span class="sxs-lookup"><span data-stu-id="f7b4f-429">public boolean moveNext()</span></span>     | <span data-ttu-id="f7b4f-430">列挙子が有効なマップ要素を指すかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-430">Determines whether the enumerator points to a valid map element.</span></span>                                                                                  |
| <span data-ttu-id="f7b4f-431">public str toString()</span><span class="sxs-lookup"><span data-stu-id="f7b4f-431">public str toString()</span></span>         | <span data-ttu-id="f7b4f-432">現在のオブジェクトを表す文字列を返します。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-432">Returns a string that represents the current object.</span></span>                                                                                              |
| <span data-ttu-id="f7b4f-433">public void new(Map map)</span><span class="sxs-lookup"><span data-stu-id="f7b4f-433">public void new(Map map)</span></span>      | <span data-ttu-id="f7b4f-434">Object クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-434">Initializes a new instance of the Object class.</span></span>                                                                                                   |
| <span data-ttu-id="f7b4f-435">public void reset()</span><span class="sxs-lookup"><span data-stu-id="f7b4f-435">public void reset()</span></span>           | <span data-ttu-id="f7b4f-436">列挙子を移動して、マップ内の最初の要素の直前をポイントします。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-436">Moves the enumerator to point to just before the first element in the map.</span></span>                                                                        |

### <a name="method-current"></a><span data-ttu-id="f7b4f-437">メソッド current</span><span class="sxs-lookup"><span data-stu-id="f7b4f-437">Method current</span></span>

<span data-ttu-id="f7b4f-438">このメソッドは廃止されました。代わりに MapEnumerator.currentKey を使用してください。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-438">This method is obsolete; use MapEnumerator.currentKey instead.</span></span>

    public AnyType current()

#### <a name="return-value"></a><span data-ttu-id="f7b4f-439">戻り値</span><span class="sxs-lookup"><span data-stu-id="f7b4f-439">Return Value</span></span>

### <a name="method-currentkey"></a><span data-ttu-id="f7b4f-440">メソッド currentKey</span><span class="sxs-lookup"><span data-stu-id="f7b4f-440">Method currentKey</span></span>

<span data-ttu-id="f7b4f-441">現在列挙子によってポイントされている (キー、値) ペアからキーを返します。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-441">Returns the key from the (key, value) pair that is currently pointed to by the enumerator.</span></span>

    public AnyType currentKey()

#### <a name="return-value"></a><span data-ttu-id="f7b4f-442">戻り値</span><span class="sxs-lookup"><span data-stu-id="f7b4f-442">Return Value</span></span>

<span data-ttu-id="f7b4f-443">現在列挙子によってポイントされているマップ要素のキー。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-443">The key from the map element that is currently pointed to by the enumerator.</span></span>

#### <a name="remarks"></a><span data-ttu-id="f7b4f-444">備考</span><span class="sxs-lookup"><span data-stu-id="f7b4f-444">Remarks</span></span>

<span data-ttu-id="f7b4f-445">CurrentKey メソッドを呼び出す前に、MapEnumerator.moveNext メソッドを呼び出す必要があります。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-445">You must call the MapEnumerator.moveNext method before you call the currentKey method.</span></span>

#### <a name="examples"></a><span data-ttu-id="f7b4f-446">例</span><span class="sxs-lookup"><span data-stu-id="f7b4f-446">Examples</span></span>

<span data-ttu-id="f7b4f-447">次の例では、マップ内の特定のテーブル ID を検索し、そのマップ要素のキー値を返します。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-447">The following example searches for a particular table ID in a map and then returns the key value of that map element.</span></span>

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

### <a name="method-currentvalue"></a><span data-ttu-id="f7b4f-448">メソッド currentValue</span><span class="sxs-lookup"><span data-stu-id="f7b4f-448">Method currentValue</span></span>

<span data-ttu-id="f7b4f-449">現在列挙子によってポイントされている (キー、値) ペアから値を返します。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-449">Returns the value from the (key, value) pair that is currently pointed to by the enumerator.</span></span>

    public AnyType currentValue()

#### <a name="return-value"></a><span data-ttu-id="f7b4f-450">戻り値</span><span class="sxs-lookup"><span data-stu-id="f7b4f-450">Return Value</span></span>

<span data-ttu-id="f7b4f-451">現在列挙子によってポイントされているマップ要素の値。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-451">The value from the map element that is currently pointed to by the enumerator.</span></span>

#### <a name="remarks"></a><span data-ttu-id="f7b4f-452">備考</span><span class="sxs-lookup"><span data-stu-id="f7b4f-452">Remarks</span></span>

<span data-ttu-id="f7b4f-453">このメソッドを呼び出す前に、MapEnumerator.moveNext メソッドを呼び出す必要があります。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-453">You must call the MapEnumerator.moveNext method before you call this method.</span></span>

#### <a name="examples"></a><span data-ttu-id="f7b4f-454">例</span><span class="sxs-lookup"><span data-stu-id="f7b4f-454">Examples</span></span>

<span data-ttu-id="f7b4f-455">次の例では、マップを検索して、パラメーターとして渡された値と等しい値を持つ要素を検索します。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-455">The following example searches through a map to find an element that has a value equal to that passed in as a parameter.</span></span> <span data-ttu-id="f7b4f-456">MapEnumerator.moveNext メソッドは、マップを反復処理するために使用され、currentValue メソッドは各値をテストしてパラメーターと一致するかどうかを確認するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-456">The MapEnumerator.moveNext method is used to iterate through the map, and the currentValue method is used to test each value to see whether it matches the parameter.</span></span>

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

### <a name="method-definitionstring"></a><span data-ttu-id="f7b4f-457">メソッド definitionString</span><span class="sxs-lookup"><span data-stu-id="f7b4f-457">Method definitionString</span></span>

<span data-ttu-id="f7b4f-458">列挙子の説明を返します。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-458">Returns a description of the enumerator.</span></span> <span data-ttu-id="f7b4f-459">たとえば、文字列への整数のマップの列挙子は、「\[int -&gt; str\] 列挙子」を返します。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-459">For example, an enumerator for a map of integers to strings would return "\[int -&gt; str\] enumerator".</span></span>

    public str definitionString()

#### <a name="return-value"></a><span data-ttu-id="f7b4f-460">戻り値</span><span class="sxs-lookup"><span data-stu-id="f7b4f-460">Return Value</span></span>

<span data-ttu-id="f7b4f-461">列挙子の説明を含む文字列。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-461">A string that contains a description of the enumerator.</span></span>

#### <a name="examples"></a><span data-ttu-id="f7b4f-462">例</span><span class="sxs-lookup"><span data-stu-id="f7b4f-462">Examples</span></span>

<span data-ttu-id="f7b4f-463">次の例では、マップとその列挙子を作成し、列挙子の定義を出力します。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-463">The following example creates a map and an enumerator for it, and then it prints out a definition of the enumerator.</span></span>

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

### <a name="method-movenext"></a><span data-ttu-id="f7b4f-464">メソッド moveNext</span><span class="sxs-lookup"><span data-stu-id="f7b4f-464">Method moveNext</span></span>

<span data-ttu-id="f7b4f-465">列挙子が有効なマップ要素を指すかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-465">Determines whether the enumerator points to a valid map element.</span></span>

    public boolean moveNext()

#### <a name="return-value"></a><span data-ttu-id="f7b4f-466">戻り値</span><span class="sxs-lookup"><span data-stu-id="f7b4f-466">Return Value</span></span>

<span data-ttu-id="f7b4f-467">マップ内の現在の職位が有効な要素を保持している場合は true。それ以外の場合は false。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-467">true if the current position in the map holds a valid element; otherwise false.</span></span>

#### <a name="remarks"></a><span data-ttu-id="f7b4f-468">備考</span><span class="sxs-lookup"><span data-stu-id="f7b4f-468">Remarks</span></span>

<span data-ttu-id="f7b4f-469">マップ列挙子は、マップの最初の要素の前に開始します。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-469">Map enumerators start before the first element in the map.</span></span> <span data-ttu-id="f7b4f-470">マップの最初の要素を指すようにするために moveNext メソッドを呼び出す必要があります。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-470">You must call the moveNext method to make it point to the first element in the map.</span></span>

#### <a name="examples"></a><span data-ttu-id="f7b4f-471">例</span><span class="sxs-lookup"><span data-stu-id="f7b4f-471">Examples</span></span>

<span data-ttu-id="f7b4f-472">次の例では、moveNext メソッドを使用してプロジェクトに含まれるテーブルを反復処理し、テーブルの DictTable オブジェクトを含む新しいマップに追加します。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-472">The following example uses the moveNext method to iterate over the tables that are contained in a project and adds them to a new map that contains a DictTable object for each table.</span></span> <span data-ttu-id="f7b4f-473">(DictTable を使用すると、テーブルに関する情報にアクセスできます。)</span><span class="sxs-lookup"><span data-stu-id="f7b4f-473">(DictTable lets you access information about a table.)</span></span>

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

### <a name="method-tostring"></a><span data-ttu-id="f7b4f-474">メソッド toString</span><span class="sxs-lookup"><span data-stu-id="f7b4f-474">Method toString</span></span>

<span data-ttu-id="f7b4f-475">現在のオブジェクトを表す文字列を返します。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-475">Returns a string that represents the current object.</span></span>

    public str toString()

#### <a name="return-value"></a><span data-ttu-id="f7b4f-476">戻り値</span><span class="sxs-lookup"><span data-stu-id="f7b4f-476">Return Value</span></span>

<span data-ttu-id="f7b4f-477">現在のオブジェクトを表す文字列。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-477">A string that represents the current object.</span></span>

#### <a name="remarks"></a><span data-ttu-id="f7b4f-478">備考</span><span class="sxs-lookup"><span data-stu-id="f7b4f-478">Remarks</span></span>

<span data-ttu-id="f7b4f-479">既定の実装は、オブジェクトのクラス名を返します。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-479">The default implementation returns the class name of the object.</span></span> <span data-ttu-id="f7b4f-480">メソッドは派生クラスで上書きできるため、そのタイプの意味のある値が返されます。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-480">The method can be overridden in a derived class to return values that are meaningful for that type.</span></span> <span data-ttu-id="f7b4f-481">たとえば、SysMethodInfo クラスのインスタンスは、インスタンスまたは静的などのメソッド名およびメソッドのタイプを返します。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-481">For example, an instance of the SysMethodInfo class returns the method name and type of the method, such as instance or static.</span></span>

#### <a name="examples"></a><span data-ttu-id="f7b4f-482">例</span><span class="sxs-lookup"><span data-stu-id="f7b4f-482">Examples</span></span>

<span data-ttu-id="f7b4f-483">次の例では、マップを作成し、最初の要素と 2 番目の要素の内容をマップに出力します。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-483">The following example creates a map, and then prints the content of the first and second elements in the map.</span></span>

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

### <a name="method-new"></a><span data-ttu-id="f7b4f-484">メソッド new</span><span class="sxs-lookup"><span data-stu-id="f7b4f-484">Method new</span></span>

<span data-ttu-id="f7b4f-485">Object クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-485">Initializes a new instance of the Object class.</span></span>

    public void new(Map map)

#### <a name="parameters"></a><span data-ttu-id="f7b4f-486">パラメーター</span><span class="sxs-lookup"><span data-stu-id="f7b4f-486">Parameters</span></span>

<span data-ttu-id="f7b4f-487">マップ</span><span class="sxs-lookup"><span data-stu-id="f7b4f-487">map</span></span>  
<span data-ttu-id="f7b4f-488">列挙子を作成するマップ。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-488">The map for which to create an enumerator.</span></span>

#### <a name="remarks"></a><span data-ttu-id="f7b4f-489">備考</span><span class="sxs-lookup"><span data-stu-id="f7b4f-489">Remarks</span></span>

<span data-ttu-id="f7b4f-490"> メソッドは廃止されています。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-490">This method is obsolete.</span></span> <span data-ttu-id="f7b4f-491">代わりに Map.getEnumerator メソッドを使用します。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-491">Use the Map.getEnumerator method instead.</span></span>

### <a name="method-reset"></a><span data-ttu-id="f7b4f-492">メソッド reset</span><span class="sxs-lookup"><span data-stu-id="f7b4f-492">Method reset</span></span>

<span data-ttu-id="f7b4f-493">列挙子を移動して、マップ内の最初の要素の直前をポイントします。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-493">Moves the enumerator to point to just before the first element in the map.</span></span>

    public void reset()

#### <a name="remarks"></a><span data-ttu-id="f7b4f-494">備考</span><span class="sxs-lookup"><span data-stu-id="f7b4f-494">Remarks</span></span>

<span data-ttu-id="f7b4f-495">reset メソッドは、列挙子をセットの先頭、セットの最初の要素の前に移動します。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-495">The reset method moves the enumerator to the start of the set, before the first element in the set.</span></span> <span data-ttu-id="f7b4f-496">セットの最初の要素を指すようにするために MapEnumerator.moveNext メソッドを呼び出す必要があります。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-496">You must call the MapEnumerator.moveNext method to make it point to the first element in the set.</span></span>

## <a name="class-mapi"></a><span data-ttu-id="f7b4f-497">クラス Mapi</span><span class="sxs-lookup"><span data-stu-id="f7b4f-497">Class Mapi</span></span>
    class Mapi extends Object

<span data-ttu-id="f7b4f-498">Mapi クラスを使用すると、Microsoft Exchange ベースのシステム、Microsoft Outlook Express、Lotus CCMail など、ほとんどの主要なメール システムでメールを送信、受信、管理できます。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-498">The Mapi class enables email to be sent, received, and managed in most major mail systems, such as Microsoft Exchange–based systems, Microsoft Outlook Express, and Lotus CCMail.</span></span>

### <a name="remarks"></a><span data-ttu-id="f7b4f-499">備考</span><span class="sxs-lookup"><span data-stu-id="f7b4f-499">Remarks</span></span>

<span data-ttu-id="f7b4f-500">他の Mapi クラス、MapiMessage、MapiRecipDesc、MapiFileDesc とともに、このクラスでは、複数の受信者、添付ファイル、メッセージ テキスト、件名を指定できます。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-500">Together with the other Mapi classes, MapiMessage, MapiRecipDesc, and MapiFileDesc, this class lets you specify multiple recipients, file attachments, message text, and a subject.</span></span> <span data-ttu-id="f7b4f-501">最も簡単な方法は、マシン上に作業用のメール クライアントを設定し、いくつかの電子メール メッセージを送受信することによって正しく動作することを確認することです。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-501">The easiest approach is to set up a working mail client on the machine, and make sure that this works correctly order by sending and receiving a few email messages.</span></span> <span data-ttu-id="f7b4f-502">Mapi メソッドのフラグは、Mapi マクロに配置されます。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-502">Flags for the Mapi methods are located in the Mapi macro.</span></span> <span data-ttu-id="f7b4f-503">\#MAPI ステートメントと共に Mapi クラスを使用するコードにこのマクロを含めます。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-503">You include this macro in code where you use the Mapi classes together with the \#MAPI statement.</span></span>

### <a name="examples"></a><span data-ttu-id="f7b4f-504">例</span><span class="sxs-lookup"><span data-stu-id="f7b4f-504">Examples</span></span>

<span data-ttu-id="f7b4f-505">次の例は、このクラスを使用して電子メール メッセージを送信する方法を示しています。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-505">The following example shows how to send an email message by using this class.</span></span>

    static void example() 
    { 
        #Mapi 
        Mapi m = new Mapi(); 
        MapiMessage msg = new MapiMessage(); 
        MapiRecipDesc recip = new MapiRecipDesc(); 
        // Set up the recipient. 
        recip.Name("someone"); 
        recip.RecipClass(#MAPI_TO); 
        msg.setRecipNo(1,recip); 
        // Log on using default profile. 
        m.Logon("","",#MAPI_USE_DEFAULT); 
        // Send the mail, and allow the user to modify the 
        // Subject, Text and Recipients in the Send Mail Dialog. 
        m.SendMail(msg,#MAPI_DIALOG); 
        // Log off. 
        m.Logoff(); 
    }

### <a name="methods"></a><span data-ttu-id="f7b4f-506">メソッド</span><span class="sxs-lookup"><span data-stu-id="f7b4f-506">Methods</span></span>

| <span data-ttu-id="f7b4f-507">方法</span><span class="sxs-lookup"><span data-stu-id="f7b4f-507">Method</span></span>                                                                         | <span data-ttu-id="f7b4f-508">説明</span><span class="sxs-lookup"><span data-stu-id="f7b4f-508">Description</span></span>                                                                                          |
|--------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f7b4f-509">public int deleteMail(str messageID)</span><span class="sxs-lookup"><span data-stu-id="f7b4f-509">public int deleteMail(str messageID)</span></span>                                           | <span data-ttu-id="f7b4f-510">メッセージ ストアから指定されたメッセージを削除します。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-510">Removes the specified message from the message store.</span></span>                                                |
| <span data-ttu-id="f7b4f-511">public str findNext(\[str messageType\], \[str seedMessageID\], \[int flags\])</span><span class="sxs-lookup"><span data-stu-id="f7b4f-511">public str findNext(\[str messageType\], \[str seedMessageID\], \[int flags\])</span></span> | <span data-ttu-id="f7b4f-512">メッセージ店舗で最初または次のメッセージを検索します。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-512">Finds the first or next message in the message store.</span></span>                                                |
| <span data-ttu-id="f7b4f-513">public int logoff()</span><span class="sxs-lookup"><span data-stu-id="f7b4f-513">public int logoff()</span></span>                                                            | <span data-ttu-id="f7b4f-514">メール システムからログオフすることができます。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-514">Lets you log off the mail system.</span></span>                                                                    |
| <span data-ttu-id="f7b4f-515">public int logon(str profileName, str password, int flags)</span><span class="sxs-lookup"><span data-stu-id="f7b4f-515">public int logon(str profileName, str password, int flags)</span></span>                     | <span data-ttu-id="f7b4f-516">指定されたプロファイルとパスワードを使用して、メール システムにログオンします。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-516">Logs on to the mail system by using the specified profile and password.</span></span>                              |
| <span data-ttu-id="f7b4f-517">public MapiMessage readMail(str messageID, \[int flags\])</span><span class="sxs-lookup"><span data-stu-id="f7b4f-517">public MapiMessage readMail(str messageID, \[int flags\])</span></span>                      | <span data-ttu-id="f7b4f-518">メッセージ ストアからメッセージを取得します。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-518">Retrieves a message from the message store.</span></span>                                                          |
| <span data-ttu-id="f7b4f-519">public MapiRecipDesc resolveName(str mame, int flags)</span><span class="sxs-lookup"><span data-stu-id="f7b4f-519">public MapiRecipDesc resolveName(str mame, int flags)</span></span>                          | <span data-ttu-id="f7b4f-520">ユーザーが入力したメッセージ受信者の名前を一意のアドレス一覧エントリに変換します。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-520">Transforms the message recipient's name, as entered by a user, to an unambiguous address list entry.</span></span> |
| <span data-ttu-id="f7b4f-521">public int saveMail(MapiMessage message, int flags, str messageId)</span><span class="sxs-lookup"><span data-stu-id="f7b4f-521">public int saveMail(MapiMessage message, int flags, str messageId)</span></span>             | <span data-ttu-id="f7b4f-522">メッセージ ストアにメッセージを保存します。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-522">Saves a message to the message store.</span></span>                                                                |
| <span data-ttu-id="f7b4f-523">public int sendMail(MapiMessage message, \[int flags\])</span><span class="sxs-lookup"><span data-stu-id="f7b4f-523">public int sendMail(MapiMessage message, \[int flags\])</span></span>                        | <span data-ttu-id="f7b4f-524">特定の受信者にメッセージを送信します。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-524">Sends a message to the specified recipients.</span></span>                                                         |
| <span data-ttu-id="f7b4f-525">public int status()</span><span class="sxs-lookup"><span data-stu-id="f7b4f-525">public int status()</span></span>                                                            | <span data-ttu-id="f7b4f-526">最後の Mapi 操作のステータスを取得します。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-526">Retrieves the status of the last Mapi operation.</span></span>                                                     |
| <span data-ttu-id="f7b4f-527">public void new()</span><span class="sxs-lookup"><span data-stu-id="f7b4f-527">public void new()</span></span>                                                              | <span data-ttu-id="f7b4f-528">Mapi クラスのインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-528">Initializes an instance of the Mapi class.</span></span>                                                           |
| <span data-ttu-id="f7b4f-529">public void finalize()</span><span class="sxs-lookup"><span data-stu-id="f7b4f-529">public void finalize()</span></span>                                                         |                                                                                                      |

### <a name="method-deletemail"></a><span data-ttu-id="f7b4f-530">メソッド deleteMail</span><span class="sxs-lookup"><span data-stu-id="f7b4f-530">Method deleteMail</span></span>

<span data-ttu-id="f7b4f-531">メッセージ ストアから指定されたメッセージを削除します。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-531">Removes the specified message from the message store.</span></span>

    public int deleteMail(str messageID)

#### <a name="parameters"></a><span data-ttu-id="f7b4f-532">パラメーター</span><span class="sxs-lookup"><span data-stu-id="f7b4f-532">Parameters</span></span>

<span data-ttu-id="f7b4f-533">messageID</span><span class="sxs-lookup"><span data-stu-id="f7b4f-533">messageID</span></span>  
<span data-ttu-id="f7b4f-534">削除するメッセージの一意のメッセージ ID。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-534">The unique message ID for the message to delete.</span></span>

#### <a name="return-value"></a><span data-ttu-id="f7b4f-535">戻り値</span><span class="sxs-lookup"><span data-stu-id="f7b4f-535">Return Value</span></span>

<span data-ttu-id="f7b4f-536">状態 \#SUCCESS\_SUCCES またはエラー コード。これは \#MAPI マクロにあります。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-536">The status \#SUCCESS\_SUCCES or an error code, which can be found in the \#MAPI macro.</span></span>

#### <a name="remarks"></a><span data-ttu-id="f7b4f-537">備考</span><span class="sxs-lookup"><span data-stu-id="f7b4f-537">Remarks</span></span>

<span data-ttu-id="f7b4f-538">メッセージ ID は、findNext メソッドを使用して取得できます。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-538">The message ID can be retrieved by using the findNext method.</span></span>

### <a name="method-findnext"></a><span data-ttu-id="f7b4f-539">メソッド findNext</span><span class="sxs-lookup"><span data-stu-id="f7b4f-539">Method findNext</span></span>

<span data-ttu-id="f7b4f-540">メッセージ店舗で最初または次のメッセージを検索します。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-540">Finds the first or next message in the message store.</span></span>

    public str findNext([str messageType], [str seedMessageID], [int flags])

#### <a name="parameters"></a><span data-ttu-id="f7b4f-541">パラメーター</span><span class="sxs-lookup"><span data-stu-id="f7b4f-541">Parameters</span></span>

<span data-ttu-id="f7b4f-542">messageType</span><span class="sxs-lookup"><span data-stu-id="f7b4f-542">messageType</span></span>  
<span data-ttu-id="f7b4f-543">先入れ先出し (FIFO) を示すフラグまたは未読; オプション。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-543">Flags that indicate first in, first out (FIFO) or unread; optional.</span></span> <span data-ttu-id="f7b4f-544">このパラメーターには、次の 2 つの値があります。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-544">This parameter has two possible values:</span></span>

<!-- -->

<span data-ttu-id="f7b4f-545">seedMessageID</span><span class="sxs-lookup"><span data-stu-id="f7b4f-545">seedMessageID</span></span>  
<span data-ttu-id="f7b4f-546">先入れ先出し (FIFO) を示すフラグまたは未読; オプション。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-546">Flags that indicate first in, first out (FIFO) or unread; optional.</span></span> <span data-ttu-id="f7b4f-547">このパラメーターには、次の 2 つの値があります。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-547">This parameter has two possible values:</span></span>

<!-- -->

<span data-ttu-id="f7b4f-548">flags</span><span class="sxs-lookup"><span data-stu-id="f7b4f-548">flags</span></span>  
<span data-ttu-id="f7b4f-549">先入れ先出し (FIFO) を示すフラグまたは未読; オプション。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-549">Flags that indicate first in, first out (FIFO) or unread; optional.</span></span> <span data-ttu-id="f7b4f-550">このパラメーターには、次の 2 つの値があります。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-550">This parameter has two possible values:</span></span>

#### <a name="return-value"></a><span data-ttu-id="f7b4f-551">戻り値</span><span class="sxs-lookup"><span data-stu-id="f7b4f-551">Return Value</span></span>

<span data-ttu-id="f7b4f-552">見つかったメッセージのメッセージ ID。メッセージが見つからない場合は空の文字列です。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-552">The message ID of the message that is found; an empty string if no message is found.</span></span>

#### <a name="remarks"></a><span data-ttu-id="f7b4f-553">備考</span><span class="sxs-lookup"><span data-stu-id="f7b4f-553">Remarks</span></span>

<span data-ttu-id="f7b4f-554">このメソッドを呼び出して最初のメッセージを検索し、続く呼び出しを発行して次のメッセージを取得します。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-554">Call this method to find the first message, and then issue subsequent calls to obtain the following messages.</span></span> <span data-ttu-id="f7b4f-555">このメソッドを呼び出した後、status メソッドを使用して Mapi エラーを確認します。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-555">Use the status method to check for Mapi errors after you call this method.</span></span>

### <a name="method-logoff"></a><span data-ttu-id="f7b4f-556">メソッド logoff</span><span class="sxs-lookup"><span data-stu-id="f7b4f-556">Method logoff</span></span>

<span data-ttu-id="f7b4f-557">メール システムからログオフすることができます。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-557">Lets you log off the mail system.</span></span>

    public int logoff()

#### <a name="return-value"></a><span data-ttu-id="f7b4f-558">戻り値</span><span class="sxs-lookup"><span data-stu-id="f7b4f-558">Return Value</span></span>

<span data-ttu-id="f7b4f-559">状態 \#SUCCESS\_SUCCESS またはエラー コード。これは \#MAPI マクロにあります。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-559">The status \#SUCCESS\_SUCCESS or an error code, which can be found in the \#MAPI macro.</span></span>

### <a name="method-logon"></a><span data-ttu-id="f7b4f-560">メソッド logon</span><span class="sxs-lookup"><span data-stu-id="f7b4f-560">Method logon</span></span>

<span data-ttu-id="f7b4f-561">指定されたプロファイルとパスワードを使用して、メール システムにログオンします。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-561">Logs on to the mail system by using the specified profile and password.</span></span>

    public int logon(str profileName, str password, int flags)

#### <a name="parameters"></a><span data-ttu-id="f7b4f-562">パラメーター</span><span class="sxs-lookup"><span data-stu-id="f7b4f-562">Parameters</span></span>

<span data-ttu-id="f7b4f-563">profileName</span><span class="sxs-lookup"><span data-stu-id="f7b4f-563">profileName</span></span>  
<span data-ttu-id="f7b4f-564">フラグの一覧。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-564">A list of flags.</span></span> <span data-ttu-id="f7b4f-565">有効なフラグは次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-565">The valid flags are as follows:</span></span>

<!-- -->

<span data-ttu-id="f7b4f-566">パスワード</span><span class="sxs-lookup"><span data-stu-id="f7b4f-566">password</span></span>  
<span data-ttu-id="f7b4f-567">フラグの一覧。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-567">A list of flags.</span></span> <span data-ttu-id="f7b4f-568">有効なフラグは次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-568">The valid flags are as follows:</span></span>

<!-- -->

<span data-ttu-id="f7b4f-569">flags</span><span class="sxs-lookup"><span data-stu-id="f7b4f-569">flags</span></span>  
<span data-ttu-id="f7b4f-570">フラグの一覧。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-570">A list of flags.</span></span> <span data-ttu-id="f7b4f-571">有効なフラグは次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-571">The valid flags are as follows:</span></span>

#### <a name="return-value"></a><span data-ttu-id="f7b4f-572">戻り値</span><span class="sxs-lookup"><span data-stu-id="f7b4f-572">Return Value</span></span>

<span data-ttu-id="f7b4f-573">ログオンに成功した場合は、状態 \#SUCCESS\_SUCCESS です。そうでない場合は、エラー コードを返します。これは、\#MAPI マクロにあります。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-573">The status \#SUCCESS\_SUCCESS if the logon succeeded; otherwise, an error code, which can be found in the \#MAPI macro.</span></span>

#### <a name="remarks"></a><span data-ttu-id="f7b4f-574">備考</span><span class="sxs-lookup"><span data-stu-id="f7b4f-574">Remarks</span></span>

<span data-ttu-id="f7b4f-575">ログオンするための簡単で一般的な方法は、既定のプロファイルを使用してログオンする \#MAPI\_USE\_DEFAULT フラグを指定することです。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-575">An easy and common way to log on is to specify the \#MAPI\_USE\_DEFAULT flag, which logs on by using the default profile.</span></span>

### <a name="method-readmail"></a><span data-ttu-id="f7b4f-576">メソッド readMail</span><span class="sxs-lookup"><span data-stu-id="f7b4f-576">Method readMail</span></span>

<span data-ttu-id="f7b4f-577">メッセージ ストアからメッセージを取得します。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-577">Retrieves a message from the message store.</span></span>

    public MapiMessage readMail(str messageID, [int flags])

#### <a name="parameters"></a><span data-ttu-id="f7b4f-578">パラメーター</span><span class="sxs-lookup"><span data-stu-id="f7b4f-578">Parameters</span></span>

<span data-ttu-id="f7b4f-579">messageID</span><span class="sxs-lookup"><span data-stu-id="f7b4f-579">messageID</span></span>  
<span data-ttu-id="f7b4f-580">フラグの一覧 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-580">A list of flags; optional.</span></span> <span data-ttu-id="f7b4f-581">有効なフラグは次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-581">The valid flags are as follows:</span></span>

<!-- -->

<span data-ttu-id="f7b4f-582">flags</span><span class="sxs-lookup"><span data-stu-id="f7b4f-582">flags</span></span>  
<span data-ttu-id="f7b4f-583">フラグの一覧 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-583">A list of flags; optional.</span></span> <span data-ttu-id="f7b4f-584">有効なフラグは次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-584">The valid flags are as follows:</span></span>

#### <a name="return-value"></a><span data-ttu-id="f7b4f-585">戻り値</span><span class="sxs-lookup"><span data-stu-id="f7b4f-585">Return Value</span></span>

<span data-ttu-id="f7b4f-586">取得された MapiMessage オブジェクト、または nullNothingnullptrunita null 参照 (Visual Basic では Nothing)。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-586">The MapiMessage object that is retrieved or nullNothingnullptrunita null reference (Nothing in Visual Basic).</span></span>

### <a name="method-resolvename"></a><span data-ttu-id="f7b4f-587">メソッド resolveName</span><span class="sxs-lookup"><span data-stu-id="f7b4f-587">Method resolveName</span></span>

<span data-ttu-id="f7b4f-588">ユーザーが入力したメッセージ受信者の名前を一意のアドレス一覧エントリに変換します。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-588">Transforms the message recipient's name, as entered by a user, to an unambiguous address list entry.</span></span>

    public MapiRecipDesc resolveName(str mame, int flags)

#### <a name="parameters"></a><span data-ttu-id="f7b4f-589">パラメーター</span><span class="sxs-lookup"><span data-stu-id="f7b4f-589">Parameters</span></span>

<span data-ttu-id="f7b4f-590">mame</span><span class="sxs-lookup"><span data-stu-id="f7b4f-590">mame</span></span>  
<span data-ttu-id="f7b4f-591">フラグの一覧。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-591">A list of flags.</span></span> <span data-ttu-id="f7b4f-592">有効なフラグは次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-592">The valid flags are as follows:</span></span>

<!-- -->

<span data-ttu-id="f7b4f-593">flags</span><span class="sxs-lookup"><span data-stu-id="f7b4f-593">flags</span></span>  
<span data-ttu-id="f7b4f-594">フラグの一覧。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-594">A list of flags.</span></span> <span data-ttu-id="f7b4f-595">有効なフラグは次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-595">The valid flags are as follows:</span></span>

#### <a name="return-value"></a><span data-ttu-id="f7b4f-596">戻り値</span><span class="sxs-lookup"><span data-stu-id="f7b4f-596">Return Value</span></span>

<span data-ttu-id="f7b4f-597">明確なアドレス一覧エントリを持つ MapiRecipDesc クラス オブジェクト。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-597">A MapiRecipDesc class object that has an unambiguous address list entry.</span></span>

### <a name="method-savemail"></a><span data-ttu-id="f7b4f-598">メソッド saveMail</span><span class="sxs-lookup"><span data-stu-id="f7b4f-598">Method saveMail</span></span>

<span data-ttu-id="f7b4f-599">メッセージ ストアにメッセージを保存します。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-599">Saves a message to the message store.</span></span>

    public int saveMail(MapiMessage message, int flags, str messageId)

#### <a name="parameters"></a><span data-ttu-id="f7b4f-600">パラメーター</span><span class="sxs-lookup"><span data-stu-id="f7b4f-600">Parameters</span></span>

<span data-ttu-id="f7b4f-601">メッセージ</span><span class="sxs-lookup"><span data-stu-id="f7b4f-601">message</span></span>  
<span data-ttu-id="f7b4f-602">取得するメッセージの一意の ID。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-602">The unique ID of the message to retrieve.</span></span>

<!-- -->

<span data-ttu-id="f7b4f-603">flags</span><span class="sxs-lookup"><span data-stu-id="f7b4f-603">flags</span></span>  
<span data-ttu-id="f7b4f-604">取得するメッセージの一意の ID。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-604">The unique ID of the message to retrieve.</span></span>

<!-- -->

<span data-ttu-id="f7b4f-605">messageId</span><span class="sxs-lookup"><span data-stu-id="f7b4f-605">messageId</span></span>  
<span data-ttu-id="f7b4f-606">取得するメッセージの一意の ID。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-606">The unique ID of the message to retrieve.</span></span>

#### <a name="return-value"></a><span data-ttu-id="f7b4f-607">戻り値</span><span class="sxs-lookup"><span data-stu-id="f7b4f-607">Return Value</span></span>

<span data-ttu-id="f7b4f-608">状態 \#SUCCESS\_SUCCESS または \#MAPI マクロのエラー コード。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-608">The status \#SUCCESS\_SUCCESS or an error code from the \#MAPI macro.</span></span>

### <a name="method-sendmail"></a><span data-ttu-id="f7b4f-609">メソッド sendMail</span><span class="sxs-lookup"><span data-stu-id="f7b4f-609">Method sendMail</span></span>

<span data-ttu-id="f7b4f-610">特定の受信者にメッセージを送信します。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-610">Sends a message to the specified recipients.</span></span>

    public int sendMail(MapiMessage message, [int flags])

#### <a name="parameters"></a><span data-ttu-id="f7b4f-611">パラメーター</span><span class="sxs-lookup"><span data-stu-id="f7b4f-611">Parameters</span></span>

<span data-ttu-id="f7b4f-612">メッセージ</span><span class="sxs-lookup"><span data-stu-id="f7b4f-612">message</span></span>  
<span data-ttu-id="f7b4f-613">フラグの一覧 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-613">A list of flags; optional.</span></span> <span data-ttu-id="f7b4f-614">有効なフラグは次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-614">The valid flags are as follows:</span></span>

<!-- -->

<span data-ttu-id="f7b4f-615">flags</span><span class="sxs-lookup"><span data-stu-id="f7b4f-615">flags</span></span>  
<span data-ttu-id="f7b4f-616">フラグの一覧 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-616">A list of flags; optional.</span></span> <span data-ttu-id="f7b4f-617">有効なフラグは次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-617">The valid flags are as follows:</span></span>

#### <a name="return-value"></a><span data-ttu-id="f7b4f-618">戻り値</span><span class="sxs-lookup"><span data-stu-id="f7b4f-618">Return Value</span></span>

<span data-ttu-id="f7b4f-619">状態 \#SUCCESS\_SUCCESS または \#MAPI マクロのエラー コード。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-619">The status \#SUCCESS\_SUCCESS or an error code from the \#MAPI macro.</span></span>

### <a name="method-status"></a><span data-ttu-id="f7b4f-620">メソッド status</span><span class="sxs-lookup"><span data-stu-id="f7b4f-620">Method status</span></span>

<span data-ttu-id="f7b4f-621">最後の Mapi 操作のステータスを取得します。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-621">Retrieves the status of the last Mapi operation.</span></span>

    public int status()

#### <a name="return-value"></a><span data-ttu-id="f7b4f-622">戻り値</span><span class="sxs-lookup"><span data-stu-id="f7b4f-622">Return Value</span></span>

<span data-ttu-id="f7b4f-623">最後の Mapi 操作のステータス コード。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-623">The status code of the last Mapi operation.</span></span>

#### <a name="remarks"></a><span data-ttu-id="f7b4f-624">備考</span><span class="sxs-lookup"><span data-stu-id="f7b4f-624">Remarks</span></span>

<span data-ttu-id="f7b4f-625">ステータス コードは \#MAPI マクロにあります。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-625">The status codes can be found in the \#MAPI macro.</span></span>

### <a name="method-new"></a><span data-ttu-id="f7b4f-626">メソッド new</span><span class="sxs-lookup"><span data-stu-id="f7b4f-626">Method new</span></span>

<span data-ttu-id="f7b4f-627">Mapi クラスのインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-627">Initializes an instance of the Mapi class.</span></span>

    public void new()

### <a name="method-finalize"></a><span data-ttu-id="f7b4f-628">メソッド finalize</span><span class="sxs-lookup"><span data-stu-id="f7b4f-628">Method finalize</span></span>

    public void finalize()

## <a name="class-mapiex"></a><span data-ttu-id="f7b4f-629">クラス MapiEx</span><span class="sxs-lookup"><span data-stu-id="f7b4f-629">Class MapiEx</span></span>
    class MapiEx extends Object

### <a name="remarks"></a><span data-ttu-id="f7b4f-630">備考</span><span class="sxs-lookup"><span data-stu-id="f7b4f-630">Remarks</span></span>

### <a name="examples"></a><span data-ttu-id="f7b4f-631">例</span><span class="sxs-lookup"><span data-stu-id="f7b4f-631">Examples</span></span>

### <a name="methods"></a><span data-ttu-id="f7b4f-632">メソッド</span><span class="sxs-lookup"><span data-stu-id="f7b4f-632">Methods</span></span>

| <span data-ttu-id="f7b4f-633">方法</span><span class="sxs-lookup"><span data-stu-id="f7b4f-633">Method</span></span>                                                          | <span data-ttu-id="f7b4f-634">説明</span><span class="sxs-lookup"><span data-stu-id="f7b4f-634">Description</span></span>                                     |
|-----------------------------------------------------------------|-------------------------------------------------|
| <span data-ttu-id="f7b4f-635">public MapiExAppointment getAppointmentFromEntryId(str entryID)</span><span class="sxs-lookup"><span data-stu-id="f7b4f-635">public MapiExAppointment getAppointmentFromEntryId(str entryID)</span></span> |                                                 |
| <span data-ttu-id="f7b4f-636">public MapiExContact getContactFromEntryId(str entryID)</span><span class="sxs-lookup"><span data-stu-id="f7b4f-636">public MapiExContact getContactFromEntryId(str entryID)</span></span>         |                                                 |
| <span data-ttu-id="f7b4f-637">public int getCurrentUser()</span><span class="sxs-lookup"><span data-stu-id="f7b4f-637">public int getCurrentUser()</span></span>                                     |                                                 |
| <span data-ttu-id="f7b4f-638">public str getCurrentUserEmail()</span><span class="sxs-lookup"><span data-stu-id="f7b4f-638">public str getCurrentUserEmail()</span></span>                                |                                                 |
| <span data-ttu-id="f7b4f-639">public str getCurrentUserEntryId()</span><span class="sxs-lookup"><span data-stu-id="f7b4f-639">public str getCurrentUserEntryId()</span></span>                              |                                                 |
| <span data-ttu-id="f7b4f-640">public str getCurrentUserName()</span><span class="sxs-lookup"><span data-stu-id="f7b4f-640">public str getCurrentUserName()</span></span>                                 |                                                 |
| <span data-ttu-id="f7b4f-641">public MapiExMail getMailFromEntryId(str entryID)</span><span class="sxs-lookup"><span data-stu-id="f7b4f-641">public MapiExMail getMailFromEntryId(str entryID)</span></span>               |                                                 |
| <span data-ttu-id="f7b4f-642">public MapiExTask getTaskFromEntryId(str entryID)</span><span class="sxs-lookup"><span data-stu-id="f7b4f-642">public MapiExTask getTaskFromEntryId(str entryID)</span></span>               |                                                 |
| <span data-ttu-id="f7b4f-643">public int logon(str profileName, str password, int flags)</span><span class="sxs-lookup"><span data-stu-id="f7b4f-643">public int logon(str profileName, str password, int flags)</span></span>      |                                                 |
| <span data-ttu-id="f7b4f-644">public boolean mapiInitialised()</span><span class="sxs-lookup"><span data-stu-id="f7b4f-644">public boolean mapiInitialised()</span></span>                                |                                                 |
| <span data-ttu-id="f7b4f-645">public boolean openMessageStore(str str)</span><span class="sxs-lookup"><span data-stu-id="f7b4f-645">public boolean openMessageStore(str str)</span></span>                        |                                                 |
| <span data-ttu-id="f7b4f-646">public void finalize()</span><span class="sxs-lookup"><span data-stu-id="f7b4f-646">public void finalize()</span></span>                                          |                                                 |
| <span data-ttu-id="f7b4f-647">public void new()</span><span class="sxs-lookup"><span data-stu-id="f7b4f-647">public void new()</span></span>                                               | <span data-ttu-id="f7b4f-648">MapiEx クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-648">Initializes a new instance of the MapiEx class.</span></span> |
| <span data-ttu-id="f7b4f-649">public void logout()</span><span class="sxs-lookup"><span data-stu-id="f7b4f-649">public void logout()</span></span>                                            |                                                 |

### <a name="method-getappointmentfromentryid"></a><span data-ttu-id="f7b4f-650">メソッド getAppointmentFromEntryId</span><span class="sxs-lookup"><span data-stu-id="f7b4f-650">Method getAppointmentFromEntryId</span></span>

    public MapiExAppointment getAppointmentFromEntryId(str entryID)

#### <a name="parameters"></a><span data-ttu-id="f7b4f-651">パラメーター</span><span class="sxs-lookup"><span data-stu-id="f7b4f-651">Parameters</span></span>

<span data-ttu-id="f7b4f-652">entryID</span><span class="sxs-lookup"><span data-stu-id="f7b4f-652">entryID</span></span>  

#### <a name="return-value"></a><span data-ttu-id="f7b4f-653">戻り値</span><span class="sxs-lookup"><span data-stu-id="f7b4f-653">Return Value</span></span>

### <a name="method-getcontactfromentryid"></a><span data-ttu-id="f7b4f-654">メソッド getContactFromEntryId</span><span class="sxs-lookup"><span data-stu-id="f7b4f-654">Method getContactFromEntryId</span></span>

    public MapiExContact getContactFromEntryId(str entryID)

#### <a name="parameters"></a><span data-ttu-id="f7b4f-655">パラメーター</span><span class="sxs-lookup"><span data-stu-id="f7b4f-655">Parameters</span></span>

<span data-ttu-id="f7b4f-656">entryID</span><span class="sxs-lookup"><span data-stu-id="f7b4f-656">entryID</span></span>  

#### <a name="return-value"></a><span data-ttu-id="f7b4f-657">戻り値</span><span class="sxs-lookup"><span data-stu-id="f7b4f-657">Return Value</span></span>

### <a name="method-getcurrentuser"></a><span data-ttu-id="f7b4f-658">メソッド getCurrentUser</span><span class="sxs-lookup"><span data-stu-id="f7b4f-658">Method getCurrentUser</span></span>

    public int getCurrentUser()

#### <a name="return-value"></a><span data-ttu-id="f7b4f-659">戻り値</span><span class="sxs-lookup"><span data-stu-id="f7b4f-659">Return Value</span></span>

### <a name="method-getcurrentuseremail"></a><span data-ttu-id="f7b4f-660">メソッド getCurrentUserEmail</span><span class="sxs-lookup"><span data-stu-id="f7b4f-660">Method getCurrentUserEmail</span></span>

    public str getCurrentUserEmail()

#### <a name="return-value"></a><span data-ttu-id="f7b4f-661">戻り値</span><span class="sxs-lookup"><span data-stu-id="f7b4f-661">Return Value</span></span>

### <a name="method-getcurrentuserentryid"></a><span data-ttu-id="f7b4f-662">メソッド getCurrentUserEntryId</span><span class="sxs-lookup"><span data-stu-id="f7b4f-662">Method getCurrentUserEntryId</span></span>

    public str getCurrentUserEntryId()

#### <a name="return-value"></a><span data-ttu-id="f7b4f-663">戻り値</span><span class="sxs-lookup"><span data-stu-id="f7b4f-663">Return Value</span></span>

### <a name="method-getcurrentusername"></a><span data-ttu-id="f7b4f-664">メソッド getCurrentUserName</span><span class="sxs-lookup"><span data-stu-id="f7b4f-664">Method getCurrentUserName</span></span>

    public str getCurrentUserName()

#### <a name="return-value"></a><span data-ttu-id="f7b4f-665">戻り値</span><span class="sxs-lookup"><span data-stu-id="f7b4f-665">Return Value</span></span>

### <a name="method-getmailfromentryid"></a><span data-ttu-id="f7b4f-666">メソッド getMailFromEntryId</span><span class="sxs-lookup"><span data-stu-id="f7b4f-666">Method getMailFromEntryId</span></span>

    public MapiExMail getMailFromEntryId(str entryID)

#### <a name="parameters"></a><span data-ttu-id="f7b4f-667">パラメーター</span><span class="sxs-lookup"><span data-stu-id="f7b4f-667">Parameters</span></span>

<span data-ttu-id="f7b4f-668">entryID</span><span class="sxs-lookup"><span data-stu-id="f7b4f-668">entryID</span></span>  

#### <a name="return-value"></a><span data-ttu-id="f7b4f-669">戻り値</span><span class="sxs-lookup"><span data-stu-id="f7b4f-669">Return Value</span></span>

### <a name="method-gettaskfromentryid"></a><span data-ttu-id="f7b4f-670">メソッド getTaskFromEntryId</span><span class="sxs-lookup"><span data-stu-id="f7b4f-670">Method getTaskFromEntryId</span></span>

    public MapiExTask getTaskFromEntryId(str entryID)

#### <a name="parameters"></a><span data-ttu-id="f7b4f-671">パラメーター</span><span class="sxs-lookup"><span data-stu-id="f7b4f-671">Parameters</span></span>

<span data-ttu-id="f7b4f-672">entryID</span><span class="sxs-lookup"><span data-stu-id="f7b4f-672">entryID</span></span>  

#### <a name="return-value"></a><span data-ttu-id="f7b4f-673">戻り値</span><span class="sxs-lookup"><span data-stu-id="f7b4f-673">Return Value</span></span>

### <a name="method-logon"></a><span data-ttu-id="f7b4f-674">メソッド logon</span><span class="sxs-lookup"><span data-stu-id="f7b4f-674">Method logon</span></span>

    public int logon(str profileName, str password, int flags)

#### <a name="parameters"></a><span data-ttu-id="f7b4f-675">パラメーター</span><span class="sxs-lookup"><span data-stu-id="f7b4f-675">Parameters</span></span>

<span data-ttu-id="f7b4f-676">profileName</span><span class="sxs-lookup"><span data-stu-id="f7b4f-676">profileName</span></span>  

<!-- -->

<span data-ttu-id="f7b4f-677">パスワード</span><span class="sxs-lookup"><span data-stu-id="f7b4f-677">password</span></span>  

<!-- -->

<span data-ttu-id="f7b4f-678">flags</span><span class="sxs-lookup"><span data-stu-id="f7b4f-678">flags</span></span>  

#### <a name="return-value"></a><span data-ttu-id="f7b4f-679">戻り値</span><span class="sxs-lookup"><span data-stu-id="f7b4f-679">Return Value</span></span>

### <a name="method-mapiinitialised"></a><span data-ttu-id="f7b4f-680">メソッド mapiInitialised</span><span class="sxs-lookup"><span data-stu-id="f7b4f-680">Method mapiInitialised</span></span>

    public boolean mapiInitialised()

#### <a name="return-value"></a><span data-ttu-id="f7b4f-681">戻り値</span><span class="sxs-lookup"><span data-stu-id="f7b4f-681">Return Value</span></span>

### <a name="method-openmessagestore"></a><span data-ttu-id="f7b4f-682">メソッド openMessageStore</span><span class="sxs-lookup"><span data-stu-id="f7b4f-682">Method openMessageStore</span></span>

    public boolean openMessageStore(str str)

#### <a name="parameters"></a><span data-ttu-id="f7b4f-683">パラメーター</span><span class="sxs-lookup"><span data-stu-id="f7b4f-683">Parameters</span></span>

<span data-ttu-id="f7b4f-684">str</span><span class="sxs-lookup"><span data-stu-id="f7b4f-684">str</span></span>  

#### <a name="return-value"></a><span data-ttu-id="f7b4f-685">戻り値</span><span class="sxs-lookup"><span data-stu-id="f7b4f-685">Return Value</span></span>

### <a name="method-finalize"></a><span data-ttu-id="f7b4f-686">メソッド finalize</span><span class="sxs-lookup"><span data-stu-id="f7b4f-686">Method finalize</span></span>

    public void finalize()

### <a name="method-new"></a><span data-ttu-id="f7b4f-687">メソッド new</span><span class="sxs-lookup"><span data-stu-id="f7b4f-687">Method new</span></span>

<span data-ttu-id="f7b4f-688">MapiEx クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-688">Initializes a new instance of the MapiEx class.</span></span>

    public void new()

### <a name="method-logout"></a><span data-ttu-id="f7b4f-689">メソッド logout</span><span class="sxs-lookup"><span data-stu-id="f7b4f-689">Method logout</span></span>

    public void logout()

## <a name="class-mapiexappointment"></a><span data-ttu-id="f7b4f-690">クラス MapiExAppointment</span><span class="sxs-lookup"><span data-stu-id="f7b4f-690">Class MapiExAppointment</span></span>
    class MapiExAppointment extends MapiExMessage

### <a name="remarks"></a><span data-ttu-id="f7b4f-691">備考</span><span class="sxs-lookup"><span data-stu-id="f7b4f-691">Remarks</span></span>

### <a name="examples"></a><span data-ttu-id="f7b4f-692">例</span><span class="sxs-lookup"><span data-stu-id="f7b4f-692">Examples</span></span>

### <a name="methods"></a><span data-ttu-id="f7b4f-693">メソッド</span><span class="sxs-lookup"><span data-stu-id="f7b4f-693">Methods</span></span>

| <span data-ttu-id="f7b4f-694">方法</span><span class="sxs-lookup"><span data-stu-id="f7b4f-694">Method</span></span>                                                 | <span data-ttu-id="f7b4f-695">説明</span><span class="sxs-lookup"><span data-stu-id="f7b4f-695">Description</span></span>                                                |
|--------------------------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="f7b4f-696">public str addRecipient(str email, str name, int type)</span><span class="sxs-lookup"><span data-stu-id="f7b4f-696">public str addRecipient(str email, str name, int type)</span></span> |                                                            |
| <span data-ttu-id="f7b4f-697">public str entryId()</span><span class="sxs-lookup"><span data-stu-id="f7b4f-697">public str entryId()</span></span>                                   |                                                            |
| <span data-ttu-id="f7b4f-698">public str getGlobalObjectId()</span><span class="sxs-lookup"><span data-stu-id="f7b4f-698">public str getGlobalObjectId()</span></span>                         |                                                            |
| <span data-ttu-id="f7b4f-699">public boolean getRecipient(int index)</span><span class="sxs-lookup"><span data-stu-id="f7b4f-699">public boolean getRecipient(int index)</span></span>                 |                                                            |
| <span data-ttu-id="f7b4f-700">public int getRecipientCount()</span><span class="sxs-lookup"><span data-stu-id="f7b4f-700">public int getRecipientCount()</span></span>                         |                                                            |
| <span data-ttu-id="f7b4f-701">public str getRecipientDisplayName()</span><span class="sxs-lookup"><span data-stu-id="f7b4f-701">public str getRecipientDisplayName()</span></span>                   |                                                            |
| <span data-ttu-id="f7b4f-702">public str getRecipientEmailAddress()</span><span class="sxs-lookup"><span data-stu-id="f7b4f-702">public str getRecipientEmailAddress()</span></span>                  |                                                            |
| <span data-ttu-id="f7b4f-703">public str getRecipientEntryId()</span><span class="sxs-lookup"><span data-stu-id="f7b4f-703">public str getRecipientEntryId()</span></span>                       |                                                            |
| <span data-ttu-id="f7b4f-704">public boolean getRecipients()</span><span class="sxs-lookup"><span data-stu-id="f7b4f-704">public boolean getRecipients()</span></span>                         |                                                            |
| <span data-ttu-id="f7b4f-705">public str getRecipientSMTPAddress()</span><span class="sxs-lookup"><span data-stu-id="f7b4f-705">public str getRecipientSMTPAddress()</span></span>                   |                                                            |
| <span data-ttu-id="f7b4f-706">public int getRecipientType()</span><span class="sxs-lookup"><span data-stu-id="f7b4f-706">public int getRecipientType()</span></span>                          |                                                            |
| <span data-ttu-id="f7b4f-707">public str getSenderEmail()</span><span class="sxs-lookup"><span data-stu-id="f7b4f-707">public str getSenderEmail()</span></span>                            |                                                            |
| <span data-ttu-id="f7b4f-708">public str getSenderName()</span><span class="sxs-lookup"><span data-stu-id="f7b4f-708">public str getSenderName()</span></span>                             |                                                            |
| <span data-ttu-id="f7b4f-709">public str removeRecipient(str email, int type)</span><span class="sxs-lookup"><span data-stu-id="f7b4f-709">public str removeRecipient(str email, int type)</span></span>        |                                                            |
| <span data-ttu-id="f7b4f-710">public boolean save()</span><span class="sxs-lookup"><span data-stu-id="f7b4f-710">public boolean save()</span></span>                                  |                                                            |
| <span data-ttu-id="f7b4f-711">public boolean setBody(str body)</span><span class="sxs-lookup"><span data-stu-id="f7b4f-711">public boolean setBody(str body)</span></span>                       |                                                            |
| <span data-ttu-id="f7b4f-712">public void new()</span><span class="sxs-lookup"><span data-stu-id="f7b4f-712">public void new()</span></span>                                      | <span data-ttu-id="f7b4f-713">MapiExAppointment クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-713">Initializes a new instance of the MapiExAppointment class.</span></span> |
| <span data-ttu-id="f7b4f-714">public void close()</span><span class="sxs-lookup"><span data-stu-id="f7b4f-714">public void close()</span></span>                                    |                                                            |
| <span data-ttu-id="f7b4f-715">public void finalize()</span><span class="sxs-lookup"><span data-stu-id="f7b4f-715">public void finalize()</span></span>                                 |                                                            |

### <a name="method-addrecipient"></a><span data-ttu-id="f7b4f-716">メソッド addRecipient</span><span class="sxs-lookup"><span data-stu-id="f7b4f-716">Method addRecipient</span></span>

    public str addRecipient(str email, str name, int type)

#### <a name="parameters"></a><span data-ttu-id="f7b4f-717">パラメーター</span><span class="sxs-lookup"><span data-stu-id="f7b4f-717">Parameters</span></span>

<span data-ttu-id="f7b4f-718">電子メール</span><span class="sxs-lookup"><span data-stu-id="f7b4f-718">email</span></span>  

<!-- -->

<span data-ttu-id="f7b4f-719">名前</span><span class="sxs-lookup"><span data-stu-id="f7b4f-719">name</span></span>  

<!-- -->

<span data-ttu-id="f7b4f-720">タイプ</span><span class="sxs-lookup"><span data-stu-id="f7b4f-720">type</span></span>  

#### <a name="return-value"></a><span data-ttu-id="f7b4f-721">戻り値</span><span class="sxs-lookup"><span data-stu-id="f7b4f-721">Return Value</span></span>

### <a name="method-entryid"></a><span data-ttu-id="f7b4f-722">メソッド entryId</span><span class="sxs-lookup"><span data-stu-id="f7b4f-722">Method entryId</span></span>

    public str entryId()

#### <a name="return-value"></a><span data-ttu-id="f7b4f-723">戻り値</span><span class="sxs-lookup"><span data-stu-id="f7b4f-723">Return Value</span></span>

### <a name="method-getglobalobjectid"></a><span data-ttu-id="f7b4f-724">メソッド getGlobalObjectId</span><span class="sxs-lookup"><span data-stu-id="f7b4f-724">Method getGlobalObjectId</span></span>

    public str getGlobalObjectId()

#### <a name="return-value"></a><span data-ttu-id="f7b4f-725">戻り値</span><span class="sxs-lookup"><span data-stu-id="f7b4f-725">Return Value</span></span>

### <a name="method-getrecipient"></a><span data-ttu-id="f7b4f-726">メソッド getRecipient</span><span class="sxs-lookup"><span data-stu-id="f7b4f-726">Method getRecipient</span></span>

    public boolean getRecipient(int index)

#### <a name="parameters"></a><span data-ttu-id="f7b4f-727">パラメーター</span><span class="sxs-lookup"><span data-stu-id="f7b4f-727">Parameters</span></span>

<span data-ttu-id="f7b4f-728">指数</span><span class="sxs-lookup"><span data-stu-id="f7b4f-728">index</span></span>  

#### <a name="return-value"></a><span data-ttu-id="f7b4f-729">戻り値</span><span class="sxs-lookup"><span data-stu-id="f7b4f-729">Return Value</span></span>

### <a name="method-getrecipientcount"></a><span data-ttu-id="f7b4f-730">メソッド getRecipientCount</span><span class="sxs-lookup"><span data-stu-id="f7b4f-730">Method getRecipientCount</span></span>

    public int getRecipientCount()

#### <a name="return-value"></a><span data-ttu-id="f7b4f-731">戻り値</span><span class="sxs-lookup"><span data-stu-id="f7b4f-731">Return Value</span></span>

### <a name="method-getrecipientdisplayname"></a><span data-ttu-id="f7b4f-732">メソッド getRecipientDisplayName</span><span class="sxs-lookup"><span data-stu-id="f7b4f-732">Method getRecipientDisplayName</span></span>

    public str getRecipientDisplayName()

#### <a name="return-value"></a><span data-ttu-id="f7b4f-733">戻り値</span><span class="sxs-lookup"><span data-stu-id="f7b4f-733">Return Value</span></span>

### <a name="method-getrecipientemailaddress"></a><span data-ttu-id="f7b4f-734">メソッド getRecipientEmailAddress</span><span class="sxs-lookup"><span data-stu-id="f7b4f-734">Method getRecipientEmailAddress</span></span>

    public str getRecipientEmailAddress()

#### <a name="return-value"></a><span data-ttu-id="f7b4f-735">戻り値</span><span class="sxs-lookup"><span data-stu-id="f7b4f-735">Return Value</span></span>

### <a name="method-getrecipiententryid"></a><span data-ttu-id="f7b4f-736">メソッド getRecipientEntryId</span><span class="sxs-lookup"><span data-stu-id="f7b4f-736">Method getRecipientEntryId</span></span>

    public str getRecipientEntryId()

#### <a name="return-value"></a><span data-ttu-id="f7b4f-737">戻り値</span><span class="sxs-lookup"><span data-stu-id="f7b4f-737">Return Value</span></span>

### <a name="method-getrecipients"></a><span data-ttu-id="f7b4f-738">メソッド getRecipients</span><span class="sxs-lookup"><span data-stu-id="f7b4f-738">Method getRecipients</span></span>

    public boolean getRecipients()

#### <a name="return-value"></a><span data-ttu-id="f7b4f-739">戻り値</span><span class="sxs-lookup"><span data-stu-id="f7b4f-739">Return Value</span></span>

### <a name="method-getrecipientsmtpaddress"></a><span data-ttu-id="f7b4f-740">メソッド getRecipientSMTPAddress</span><span class="sxs-lookup"><span data-stu-id="f7b4f-740">Method getRecipientSMTPAddress</span></span>

    public str getRecipientSMTPAddress()

#### <a name="return-value"></a><span data-ttu-id="f7b4f-741">戻り値</span><span class="sxs-lookup"><span data-stu-id="f7b4f-741">Return Value</span></span>

### <a name="method-getrecipienttype"></a><span data-ttu-id="f7b4f-742">メソッド getRecipientType</span><span class="sxs-lookup"><span data-stu-id="f7b4f-742">Method getRecipientType</span></span>

    public int getRecipientType()

#### <a name="return-value"></a><span data-ttu-id="f7b4f-743">戻り値</span><span class="sxs-lookup"><span data-stu-id="f7b4f-743">Return Value</span></span>

### <a name="method-getsenderemail"></a><span data-ttu-id="f7b4f-744">メソッド getSenderEmail</span><span class="sxs-lookup"><span data-stu-id="f7b4f-744">Method getSenderEmail</span></span>

    public str getSenderEmail()

#### <a name="return-value"></a><span data-ttu-id="f7b4f-745">戻り値</span><span class="sxs-lookup"><span data-stu-id="f7b4f-745">Return Value</span></span>

### <a name="method-getsendername"></a><span data-ttu-id="f7b4f-746">メソッド getSenderName</span><span class="sxs-lookup"><span data-stu-id="f7b4f-746">Method getSenderName</span></span>

    public str getSenderName()

#### <a name="return-value"></a><span data-ttu-id="f7b4f-747">戻り値</span><span class="sxs-lookup"><span data-stu-id="f7b4f-747">Return Value</span></span>

### <a name="method-removerecipient"></a><span data-ttu-id="f7b4f-748">メソッド removeRecipient</span><span class="sxs-lookup"><span data-stu-id="f7b4f-748">Method removeRecipient</span></span>

    public str removeRecipient(str email, int type)

#### <a name="parameters"></a><span data-ttu-id="f7b4f-749">パラメーター</span><span class="sxs-lookup"><span data-stu-id="f7b4f-749">Parameters</span></span>

<span data-ttu-id="f7b4f-750">電子メール</span><span class="sxs-lookup"><span data-stu-id="f7b4f-750">email</span></span>  

<!-- -->

<span data-ttu-id="f7b4f-751">タイプ</span><span class="sxs-lookup"><span data-stu-id="f7b4f-751">type</span></span>  

#### <a name="return-value"></a><span data-ttu-id="f7b4f-752">戻り値</span><span class="sxs-lookup"><span data-stu-id="f7b4f-752">Return Value</span></span>

### <a name="method-save"></a><span data-ttu-id="f7b4f-753">メソッド save</span><span class="sxs-lookup"><span data-stu-id="f7b4f-753">Method save</span></span>

    public boolean save()

#### <a name="return-value"></a><span data-ttu-id="f7b4f-754">戻り値</span><span class="sxs-lookup"><span data-stu-id="f7b4f-754">Return Value</span></span>

### <a name="method-setbody"></a><span data-ttu-id="f7b4f-755">メソッド setBody</span><span class="sxs-lookup"><span data-stu-id="f7b4f-755">Method setBody</span></span>

    public boolean setBody(str body)

#### <a name="parameters"></a><span data-ttu-id="f7b4f-756">パラメーター</span><span class="sxs-lookup"><span data-stu-id="f7b4f-756">Parameters</span></span>

<span data-ttu-id="f7b4f-757">body</span><span class="sxs-lookup"><span data-stu-id="f7b4f-757">body</span></span>  

#### <a name="return-value"></a><span data-ttu-id="f7b4f-758">戻り値</span><span class="sxs-lookup"><span data-stu-id="f7b4f-758">Return Value</span></span>

### <a name="method-new"></a><span data-ttu-id="f7b4f-759">メソッド new</span><span class="sxs-lookup"><span data-stu-id="f7b4f-759">Method new</span></span>

<span data-ttu-id="f7b4f-760">MapiExAppointment クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-760">Initializes a new instance of the MapiExAppointment class.</span></span>

    public void new()

### <a name="method-close"></a><span data-ttu-id="f7b4f-761">メソッド close</span><span class="sxs-lookup"><span data-stu-id="f7b4f-761">Method close</span></span>

    public void close()

### <a name="method-finalize"></a><span data-ttu-id="f7b4f-762">メソッド finalize</span><span class="sxs-lookup"><span data-stu-id="f7b4f-762">Method finalize</span></span>

    public void finalize()

## <a name="class-mapiexcontact"></a><span data-ttu-id="f7b4f-763">クラス MapiExContact</span><span class="sxs-lookup"><span data-stu-id="f7b4f-763">Class MapiExContact</span></span>
    class MapiExContact extends MapiExMessage

### <a name="remarks"></a><span data-ttu-id="f7b4f-764">備考</span><span class="sxs-lookup"><span data-stu-id="f7b4f-764">Remarks</span></span>

### <a name="examples"></a><span data-ttu-id="f7b4f-765">例</span><span class="sxs-lookup"><span data-stu-id="f7b4f-765">Examples</span></span>

### <a name="methods"></a><span data-ttu-id="f7b4f-766">メソッド</span><span class="sxs-lookup"><span data-stu-id="f7b4f-766">Methods</span></span>

| <span data-ttu-id="f7b4f-767">方法</span><span class="sxs-lookup"><span data-stu-id="f7b4f-767">Method</span></span>                            | <span data-ttu-id="f7b4f-768">説明</span><span class="sxs-lookup"><span data-stu-id="f7b4f-768">Description</span></span>                                            |
|-----------------------------------|--------------------------------------------------------|
| <span data-ttu-id="f7b4f-769">public str entryId()</span><span class="sxs-lookup"><span data-stu-id="f7b4f-769">public str entryId()</span></span>              |                                                        |
| <span data-ttu-id="f7b4f-770">public str getBody()</span><span class="sxs-lookup"><span data-stu-id="f7b4f-770">public str getBody()</span></span>              |                                                        |
| <span data-ttu-id="f7b4f-771">public str getEmail1()</span><span class="sxs-lookup"><span data-stu-id="f7b4f-771">public str getEmail1()</span></span>            |                                                        |
| <span data-ttu-id="f7b4f-772">public str getEmail1DisplayName()</span><span class="sxs-lookup"><span data-stu-id="f7b4f-772">public str getEmail1DisplayName()</span></span> |                                                        |
| <span data-ttu-id="f7b4f-773">public str getEmail1Type()</span><span class="sxs-lookup"><span data-stu-id="f7b4f-773">public str getEmail1Type()</span></span>        |                                                        |
| <span data-ttu-id="f7b4f-774">public str getEmail2()</span><span class="sxs-lookup"><span data-stu-id="f7b4f-774">public str getEmail2()</span></span>            |                                                        |
| <span data-ttu-id="f7b4f-775">public str getEmail2DisplayName()</span><span class="sxs-lookup"><span data-stu-id="f7b4f-775">public str getEmail2DisplayName()</span></span> |                                                        |
| <span data-ttu-id="f7b4f-776">public str getEmail2Type()</span><span class="sxs-lookup"><span data-stu-id="f7b4f-776">public str getEmail2Type()</span></span>        |                                                        |
| <span data-ttu-id="f7b4f-777">public str getEmail3()</span><span class="sxs-lookup"><span data-stu-id="f7b4f-777">public str getEmail3()</span></span>            |                                                        |
| <span data-ttu-id="f7b4f-778">public str getEmail3DisplayName()</span><span class="sxs-lookup"><span data-stu-id="f7b4f-778">public str getEmail3DisplayName()</span></span> |                                                        |
| <span data-ttu-id="f7b4f-779">public str getEmail3Type()</span><span class="sxs-lookup"><span data-stu-id="f7b4f-779">public str getEmail3Type()</span></span>        |                                                        |
| <span data-ttu-id="f7b4f-780">public str getIMAddress()</span><span class="sxs-lookup"><span data-stu-id="f7b4f-780">public str getIMAddress()</span></span>         |                                                        |
| <span data-ttu-id="f7b4f-781">public boolean save()</span><span class="sxs-lookup"><span data-stu-id="f7b4f-781">public boolean save()</span></span>             |                                                        |
| <span data-ttu-id="f7b4f-782">public boolean setBody(str body)</span><span class="sxs-lookup"><span data-stu-id="f7b4f-782">public boolean setBody(str body)</span></span>  |                                                        |
| <span data-ttu-id="f7b4f-783">public void close()</span><span class="sxs-lookup"><span data-stu-id="f7b4f-783">public void close()</span></span>               |                                                        |
| <span data-ttu-id="f7b4f-784">public void finalize()</span><span class="sxs-lookup"><span data-stu-id="f7b4f-784">public void finalize()</span></span>            |                                                        |
| <span data-ttu-id="f7b4f-785">public void new()</span><span class="sxs-lookup"><span data-stu-id="f7b4f-785">public void new()</span></span>                 | <span data-ttu-id="f7b4f-786">MapiExContact クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-786">Initializes a new instance of the MapiExContact class.</span></span> |

### <a name="method-entryid"></a><span data-ttu-id="f7b4f-787">メソッド entryId</span><span class="sxs-lookup"><span data-stu-id="f7b4f-787">Method entryId</span></span>

    public str entryId()

#### <a name="return-value"></a><span data-ttu-id="f7b4f-788">戻り値</span><span class="sxs-lookup"><span data-stu-id="f7b4f-788">Return Value</span></span>

### <a name="method-getbody"></a><span data-ttu-id="f7b4f-789">メソッド getBody</span><span class="sxs-lookup"><span data-stu-id="f7b4f-789">Method getBody</span></span>

    public str getBody()

#### <a name="return-value"></a><span data-ttu-id="f7b4f-790">戻り値</span><span class="sxs-lookup"><span data-stu-id="f7b4f-790">Return Value</span></span>

### <a name="method-getemail1"></a><span data-ttu-id="f7b4f-791">メソッド getEmail1</span><span class="sxs-lookup"><span data-stu-id="f7b4f-791">Method getEmail1</span></span>

    public str getEmail1()

#### <a name="return-value"></a><span data-ttu-id="f7b4f-792">戻り値</span><span class="sxs-lookup"><span data-stu-id="f7b4f-792">Return Value</span></span>

### <a name="method-getemail1displayname"></a><span data-ttu-id="f7b4f-793">メソッド getEmail1DisplayName</span><span class="sxs-lookup"><span data-stu-id="f7b4f-793">Method getEmail1DisplayName</span></span>

    public str getEmail1DisplayName()

#### <a name="return-value"></a><span data-ttu-id="f7b4f-794">戻り値</span><span class="sxs-lookup"><span data-stu-id="f7b4f-794">Return Value</span></span>

### <a name="method-getemail1type"></a><span data-ttu-id="f7b4f-795">メソッド getEmail1Type</span><span class="sxs-lookup"><span data-stu-id="f7b4f-795">Method getEmail1Type</span></span>

    public str getEmail1Type()

#### <a name="return-value"></a><span data-ttu-id="f7b4f-796">戻り値</span><span class="sxs-lookup"><span data-stu-id="f7b4f-796">Return Value</span></span>

### <a name="method-getemail2"></a><span data-ttu-id="f7b4f-797">メソッド getEmail2</span><span class="sxs-lookup"><span data-stu-id="f7b4f-797">Method getEmail2</span></span>

    public str getEmail2()

#### <a name="return-value"></a><span data-ttu-id="f7b4f-798">戻り値</span><span class="sxs-lookup"><span data-stu-id="f7b4f-798">Return Value</span></span>

### <a name="method-getemail2displayname"></a><span data-ttu-id="f7b4f-799">メソッド getEmail2DisplayName</span><span class="sxs-lookup"><span data-stu-id="f7b4f-799">Method getEmail2DisplayName</span></span>

    public str getEmail2DisplayName()

#### <a name="return-value"></a><span data-ttu-id="f7b4f-800">戻り値</span><span class="sxs-lookup"><span data-stu-id="f7b4f-800">Return Value</span></span>

### <a name="method-getemail2type"></a><span data-ttu-id="f7b4f-801">メソッド getEmail2Type</span><span class="sxs-lookup"><span data-stu-id="f7b4f-801">Method getEmail2Type</span></span>

    public str getEmail2Type()

#### <a name="return-value"></a><span data-ttu-id="f7b4f-802">戻り値</span><span class="sxs-lookup"><span data-stu-id="f7b4f-802">Return Value</span></span>

### <a name="method-getemail3"></a><span data-ttu-id="f7b4f-803">メソッド getEmail3</span><span class="sxs-lookup"><span data-stu-id="f7b4f-803">Method getEmail3</span></span>

    public str getEmail3()

#### <a name="return-value"></a><span data-ttu-id="f7b4f-804">戻り値</span><span class="sxs-lookup"><span data-stu-id="f7b4f-804">Return Value</span></span>

### <a name="method-getemail3displayname"></a><span data-ttu-id="f7b4f-805">メソッド getEmail3DisplayName</span><span class="sxs-lookup"><span data-stu-id="f7b4f-805">Method getEmail3DisplayName</span></span>

    public str getEmail3DisplayName()

#### <a name="return-value"></a><span data-ttu-id="f7b4f-806">戻り値</span><span class="sxs-lookup"><span data-stu-id="f7b4f-806">Return Value</span></span>

### <a name="method-getemail3type"></a><span data-ttu-id="f7b4f-807">メソッド getEmail3Type</span><span class="sxs-lookup"><span data-stu-id="f7b4f-807">Method getEmail3Type</span></span>

    public str getEmail3Type()

#### <a name="return-value"></a><span data-ttu-id="f7b4f-808">戻り値</span><span class="sxs-lookup"><span data-stu-id="f7b4f-808">Return Value</span></span>

### <a name="method-getimaddress"></a><span data-ttu-id="f7b4f-809">メソッド getIMAddress</span><span class="sxs-lookup"><span data-stu-id="f7b4f-809">Method getIMAddress</span></span>

    public str getIMAddress()

#### <a name="return-value"></a><span data-ttu-id="f7b4f-810">戻り値</span><span class="sxs-lookup"><span data-stu-id="f7b4f-810">Return Value</span></span>

### <a name="method-save"></a><span data-ttu-id="f7b4f-811">メソッド save</span><span class="sxs-lookup"><span data-stu-id="f7b4f-811">Method save</span></span>

    public boolean save()

#### <a name="return-value"></a><span data-ttu-id="f7b4f-812">戻り値</span><span class="sxs-lookup"><span data-stu-id="f7b4f-812">Return Value</span></span>

### <a name="method-setbody"></a><span data-ttu-id="f7b4f-813">メソッド setBody</span><span class="sxs-lookup"><span data-stu-id="f7b4f-813">Method setBody</span></span>

    public boolean setBody(str body)

#### <a name="parameters"></a><span data-ttu-id="f7b4f-814">パラメーター</span><span class="sxs-lookup"><span data-stu-id="f7b4f-814">Parameters</span></span>

<span data-ttu-id="f7b4f-815">body</span><span class="sxs-lookup"><span data-stu-id="f7b4f-815">body</span></span>  

#### <a name="return-value"></a><span data-ttu-id="f7b4f-816">戻り値</span><span class="sxs-lookup"><span data-stu-id="f7b4f-816">Return Value</span></span>

### <a name="method-close"></a><span data-ttu-id="f7b4f-817">メソッド close</span><span class="sxs-lookup"><span data-stu-id="f7b4f-817">Method close</span></span>

    public void close()

### <a name="method-finalize"></a><span data-ttu-id="f7b4f-818">メソッド finalize</span><span class="sxs-lookup"><span data-stu-id="f7b4f-818">Method finalize</span></span>

    public void finalize()

### <a name="method-new"></a><span data-ttu-id="f7b4f-819">メソッド new</span><span class="sxs-lookup"><span data-stu-id="f7b4f-819">Method new</span></span>

<span data-ttu-id="f7b4f-820">MapiExContact クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-820">Initializes a new instance of the MapiExContact class.</span></span>

    public void new()

## <a name="class-mapiexmail"></a><span data-ttu-id="f7b4f-821">クラス MapiExMail</span><span class="sxs-lookup"><span data-stu-id="f7b4f-821">Class MapiExMail</span></span>
    class MapiExMail extends MapiExMessage

### <a name="remarks"></a><span data-ttu-id="f7b4f-822">備考</span><span class="sxs-lookup"><span data-stu-id="f7b4f-822">Remarks</span></span>

### <a name="examples"></a><span data-ttu-id="f7b4f-823">例</span><span class="sxs-lookup"><span data-stu-id="f7b4f-823">Examples</span></span>

### <a name="methods"></a><span data-ttu-id="f7b4f-824">メソッド</span><span class="sxs-lookup"><span data-stu-id="f7b4f-824">Methods</span></span>

| <span data-ttu-id="f7b4f-825">方法</span><span class="sxs-lookup"><span data-stu-id="f7b4f-825">Method</span></span>                                                 | <span data-ttu-id="f7b4f-826">説明</span><span class="sxs-lookup"><span data-stu-id="f7b4f-826">Description</span></span>                                         |
|--------------------------------------------------------|-----------------------------------------------------|
| <span data-ttu-id="f7b4f-827">public str addRecipient(str email, str name, int type)</span><span class="sxs-lookup"><span data-stu-id="f7b4f-827">public str addRecipient(str email, str name, int type)</span></span> |                                                     |
| <span data-ttu-id="f7b4f-828">public str entryId()</span><span class="sxs-lookup"><span data-stu-id="f7b4f-828">public str entryId()</span></span>                                   |                                                     |
| <span data-ttu-id="f7b4f-829">public boolean getRecipient(int index)</span><span class="sxs-lookup"><span data-stu-id="f7b4f-829">public boolean getRecipient(int index)</span></span>                 |                                                     |
| <span data-ttu-id="f7b4f-830">public int getRecipientCount()</span><span class="sxs-lookup"><span data-stu-id="f7b4f-830">public int getRecipientCount()</span></span>                         |                                                     |
| <span data-ttu-id="f7b4f-831">public str getRecipientDisplayName()</span><span class="sxs-lookup"><span data-stu-id="f7b4f-831">public str getRecipientDisplayName()</span></span>                   |                                                     |
| <span data-ttu-id="f7b4f-832">public str getRecipientEmailAddress()</span><span class="sxs-lookup"><span data-stu-id="f7b4f-832">public str getRecipientEmailAddress()</span></span>                  |                                                     |
| <span data-ttu-id="f7b4f-833">public str getRecipientEntryId()</span><span class="sxs-lookup"><span data-stu-id="f7b4f-833">public str getRecipientEntryId()</span></span>                       |                                                     |
| <span data-ttu-id="f7b4f-834">public boolean getRecipients()</span><span class="sxs-lookup"><span data-stu-id="f7b4f-834">public boolean getRecipients()</span></span>                         |                                                     |
| <span data-ttu-id="f7b4f-835">public str getRecipientSMTPAddress()</span><span class="sxs-lookup"><span data-stu-id="f7b4f-835">public str getRecipientSMTPAddress()</span></span>                   |                                                     |
| <span data-ttu-id="f7b4f-836">public int getRecipientType()</span><span class="sxs-lookup"><span data-stu-id="f7b4f-836">public int getRecipientType()</span></span>                          |                                                     |
| <span data-ttu-id="f7b4f-837">public str getSenderEmail()</span><span class="sxs-lookup"><span data-stu-id="f7b4f-837">public str getSenderEmail()</span></span>                            |                                                     |
| <span data-ttu-id="f7b4f-838">public str getSenderName()</span><span class="sxs-lookup"><span data-stu-id="f7b4f-838">public str getSenderName()</span></span>                             |                                                     |
| <span data-ttu-id="f7b4f-839">public str removeRecipient(str email, int type)</span><span class="sxs-lookup"><span data-stu-id="f7b4f-839">public str removeRecipient(str email, int type)</span></span>        |                                                     |
| <span data-ttu-id="f7b4f-840">public boolean save()</span><span class="sxs-lookup"><span data-stu-id="f7b4f-840">public boolean save()</span></span>                                  |                                                     |
| <span data-ttu-id="f7b4f-841">public boolean saveMsgToFile(str fileName)</span><span class="sxs-lookup"><span data-stu-id="f7b4f-841">public boolean saveMsgToFile(str fileName)</span></span>             |                                                     |
| <span data-ttu-id="f7b4f-842">public boolean send()</span><span class="sxs-lookup"><span data-stu-id="f7b4f-842">public boolean send()</span></span>                                  |                                                     |
| <span data-ttu-id="f7b4f-843">public boolean setBody(str body)</span><span class="sxs-lookup"><span data-stu-id="f7b4f-843">public boolean setBody(str body)</span></span>                       |                                                     |
| <span data-ttu-id="f7b4f-844">public void finalize()</span><span class="sxs-lookup"><span data-stu-id="f7b4f-844">public void finalize()</span></span>                                 |                                                     |
| <span data-ttu-id="f7b4f-845">public void close()</span><span class="sxs-lookup"><span data-stu-id="f7b4f-845">public void close()</span></span>                                    |                                                     |
| <span data-ttu-id="f7b4f-846">public void new()</span><span class="sxs-lookup"><span data-stu-id="f7b4f-846">public void new()</span></span>                                      | <span data-ttu-id="f7b4f-847">MapiExMail クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-847">Initializes a new instance of the MapiExMail class.</span></span> |

### <a name="method-addrecipient"></a><span data-ttu-id="f7b4f-848">メソッド addRecipient</span><span class="sxs-lookup"><span data-stu-id="f7b4f-848">Method addRecipient</span></span>

    public str addRecipient(str email, str name, int type)

#### <a name="parameters"></a><span data-ttu-id="f7b4f-849">パラメーター</span><span class="sxs-lookup"><span data-stu-id="f7b4f-849">Parameters</span></span>

<span data-ttu-id="f7b4f-850">電子メール</span><span class="sxs-lookup"><span data-stu-id="f7b4f-850">email</span></span>  

<!-- -->

<span data-ttu-id="f7b4f-851">名前</span><span class="sxs-lookup"><span data-stu-id="f7b4f-851">name</span></span>  

<!-- -->

<span data-ttu-id="f7b4f-852">タイプ</span><span class="sxs-lookup"><span data-stu-id="f7b4f-852">type</span></span>  

#### <a name="return-value"></a><span data-ttu-id="f7b4f-853">戻り値</span><span class="sxs-lookup"><span data-stu-id="f7b4f-853">Return Value</span></span>

### <a name="method-entryid"></a><span data-ttu-id="f7b4f-854">メソッド entryId</span><span class="sxs-lookup"><span data-stu-id="f7b4f-854">Method entryId</span></span>

    public str entryId()

#### <a name="return-value"></a><span data-ttu-id="f7b4f-855">戻り値</span><span class="sxs-lookup"><span data-stu-id="f7b4f-855">Return Value</span></span>

### <a name="method-getrecipient"></a><span data-ttu-id="f7b4f-856">メソッド getRecipient</span><span class="sxs-lookup"><span data-stu-id="f7b4f-856">Method getRecipient</span></span>

    public boolean getRecipient(int index)

#### <a name="parameters"></a><span data-ttu-id="f7b4f-857">パラメーター</span><span class="sxs-lookup"><span data-stu-id="f7b4f-857">Parameters</span></span>

<span data-ttu-id="f7b4f-858">指数</span><span class="sxs-lookup"><span data-stu-id="f7b4f-858">index</span></span>  

#### <a name="return-value"></a><span data-ttu-id="f7b4f-859">戻り値</span><span class="sxs-lookup"><span data-stu-id="f7b4f-859">Return Value</span></span>

### <a name="method-getrecipientcount"></a><span data-ttu-id="f7b4f-860">メソッド getRecipientCount</span><span class="sxs-lookup"><span data-stu-id="f7b4f-860">Method getRecipientCount</span></span>

    public int getRecipientCount()

#### <a name="return-value"></a><span data-ttu-id="f7b4f-861">戻り値</span><span class="sxs-lookup"><span data-stu-id="f7b4f-861">Return Value</span></span>

### <a name="method-getrecipientdisplayname"></a><span data-ttu-id="f7b4f-862">メソッド getRecipientDisplayName</span><span class="sxs-lookup"><span data-stu-id="f7b4f-862">Method getRecipientDisplayName</span></span>

    public str getRecipientDisplayName()

#### <a name="return-value"></a><span data-ttu-id="f7b4f-863">戻り値</span><span class="sxs-lookup"><span data-stu-id="f7b4f-863">Return Value</span></span>

### <a name="method-getrecipientemailaddress"></a><span data-ttu-id="f7b4f-864">メソッド getRecipientEmailAddress</span><span class="sxs-lookup"><span data-stu-id="f7b4f-864">Method getRecipientEmailAddress</span></span>

    public str getRecipientEmailAddress()

#### <a name="return-value"></a><span data-ttu-id="f7b4f-865">戻り値</span><span class="sxs-lookup"><span data-stu-id="f7b4f-865">Return Value</span></span>

### <a name="method-getrecipiententryid"></a><span data-ttu-id="f7b4f-866">メソッド getRecipientEntryId</span><span class="sxs-lookup"><span data-stu-id="f7b4f-866">Method getRecipientEntryId</span></span>

    public str getRecipientEntryId()

#### <a name="return-value"></a><span data-ttu-id="f7b4f-867">戻り値</span><span class="sxs-lookup"><span data-stu-id="f7b4f-867">Return Value</span></span>

### <a name="method-getrecipients"></a><span data-ttu-id="f7b4f-868">メソッド getRecipients</span><span class="sxs-lookup"><span data-stu-id="f7b4f-868">Method getRecipients</span></span>

    public boolean getRecipients()

#### <a name="return-value"></a><span data-ttu-id="f7b4f-869">戻り値</span><span class="sxs-lookup"><span data-stu-id="f7b4f-869">Return Value</span></span>

### <a name="method-getrecipientsmtpaddress"></a><span data-ttu-id="f7b4f-870">メソッド getRecipientSMTPAddress</span><span class="sxs-lookup"><span data-stu-id="f7b4f-870">Method getRecipientSMTPAddress</span></span>

    public str getRecipientSMTPAddress()

#### <a name="return-value"></a><span data-ttu-id="f7b4f-871">戻り値</span><span class="sxs-lookup"><span data-stu-id="f7b4f-871">Return Value</span></span>

### <a name="method-getrecipienttype"></a><span data-ttu-id="f7b4f-872">メソッド getRecipientType</span><span class="sxs-lookup"><span data-stu-id="f7b4f-872">Method getRecipientType</span></span>

    public int getRecipientType()

#### <a name="return-value"></a><span data-ttu-id="f7b4f-873">戻り値</span><span class="sxs-lookup"><span data-stu-id="f7b4f-873">Return Value</span></span>

### <a name="method-getsenderemail"></a><span data-ttu-id="f7b4f-874">メソッド getSenderEmail</span><span class="sxs-lookup"><span data-stu-id="f7b4f-874">Method getSenderEmail</span></span>

    public str getSenderEmail()

#### <a name="return-value"></a><span data-ttu-id="f7b4f-875">戻り値</span><span class="sxs-lookup"><span data-stu-id="f7b4f-875">Return Value</span></span>

### <a name="method-getsendername"></a><span data-ttu-id="f7b4f-876">メソッド getSenderName</span><span class="sxs-lookup"><span data-stu-id="f7b4f-876">Method getSenderName</span></span>

    public str getSenderName()

#### <a name="return-value"></a><span data-ttu-id="f7b4f-877">戻り値</span><span class="sxs-lookup"><span data-stu-id="f7b4f-877">Return Value</span></span>

### <a name="method-removerecipient"></a><span data-ttu-id="f7b4f-878">メソッド removeRecipient</span><span class="sxs-lookup"><span data-stu-id="f7b4f-878">Method removeRecipient</span></span>

    public str removeRecipient(str email, int type)

#### <a name="parameters"></a><span data-ttu-id="f7b4f-879">パラメーター</span><span class="sxs-lookup"><span data-stu-id="f7b4f-879">Parameters</span></span>

<span data-ttu-id="f7b4f-880">電子メール</span><span class="sxs-lookup"><span data-stu-id="f7b4f-880">email</span></span>  

<!-- -->

<span data-ttu-id="f7b4f-881">タイプ</span><span class="sxs-lookup"><span data-stu-id="f7b4f-881">type</span></span>  

#### <a name="return-value"></a><span data-ttu-id="f7b4f-882">戻り値</span><span class="sxs-lookup"><span data-stu-id="f7b4f-882">Return Value</span></span>

### <a name="method-save"></a><span data-ttu-id="f7b4f-883">メソッド save</span><span class="sxs-lookup"><span data-stu-id="f7b4f-883">Method save</span></span>

    public boolean save()

#### <a name="return-value"></a><span data-ttu-id="f7b4f-884">戻り値</span><span class="sxs-lookup"><span data-stu-id="f7b4f-884">Return Value</span></span>

### <a name="method-savemsgtofile"></a><span data-ttu-id="f7b4f-885">メソッド saveMsgToFile</span><span class="sxs-lookup"><span data-stu-id="f7b4f-885">Method saveMsgToFile</span></span>

    public boolean saveMsgToFile(str fileName)

#### <a name="parameters"></a><span data-ttu-id="f7b4f-886">パラメーター</span><span class="sxs-lookup"><span data-stu-id="f7b4f-886">Parameters</span></span>

<span data-ttu-id="f7b4f-887">fileName</span><span class="sxs-lookup"><span data-stu-id="f7b4f-887">fileName</span></span>  

#### <a name="return-value"></a><span data-ttu-id="f7b4f-888">戻り値</span><span class="sxs-lookup"><span data-stu-id="f7b4f-888">Return Value</span></span>

### <a name="method-send"></a><span data-ttu-id="f7b4f-889">メソッド send</span><span class="sxs-lookup"><span data-stu-id="f7b4f-889">Method send</span></span>

    public boolean send()

#### <a name="return-value"></a><span data-ttu-id="f7b4f-890">戻り値</span><span class="sxs-lookup"><span data-stu-id="f7b4f-890">Return Value</span></span>

### <a name="method-setbody"></a><span data-ttu-id="f7b4f-891">メソッド setBody</span><span class="sxs-lookup"><span data-stu-id="f7b4f-891">Method setBody</span></span>

    public boolean setBody(str body)

#### <a name="parameters"></a><span data-ttu-id="f7b4f-892">パラメーター</span><span class="sxs-lookup"><span data-stu-id="f7b4f-892">Parameters</span></span>

<span data-ttu-id="f7b4f-893">body</span><span class="sxs-lookup"><span data-stu-id="f7b4f-893">body</span></span>  

#### <a name="return-value"></a><span data-ttu-id="f7b4f-894">戻り値</span><span class="sxs-lookup"><span data-stu-id="f7b4f-894">Return Value</span></span>

### <a name="method-finalize"></a><span data-ttu-id="f7b4f-895">メソッド finalize</span><span class="sxs-lookup"><span data-stu-id="f7b4f-895">Method finalize</span></span>

    public void finalize()

### <a name="method-close"></a><span data-ttu-id="f7b4f-896">メソッド close</span><span class="sxs-lookup"><span data-stu-id="f7b4f-896">Method close</span></span>

    public void close()

### <a name="method-new"></a><span data-ttu-id="f7b4f-897">メソッド new</span><span class="sxs-lookup"><span data-stu-id="f7b4f-897">Method new</span></span>

<span data-ttu-id="f7b4f-898">MapiExMail クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-898">Initializes a new instance of the MapiExMail class.</span></span>

    public void new()

## <a name="class-mapiexmessage"></a><span data-ttu-id="f7b4f-899">クラス MapiExMessage</span><span class="sxs-lookup"><span data-stu-id="f7b4f-899">Class MapiExMessage</span></span>
    class MapiExMessage extends Object

### <a name="remarks"></a><span data-ttu-id="f7b4f-900">備考</span><span class="sxs-lookup"><span data-stu-id="f7b4f-900">Remarks</span></span>

### <a name="examples"></a><span data-ttu-id="f7b4f-901">例</span><span class="sxs-lookup"><span data-stu-id="f7b4f-901">Examples</span></span>

### <a name="methods"></a><span data-ttu-id="f7b4f-902">メソッド</span><span class="sxs-lookup"><span data-stu-id="f7b4f-902">Methods</span></span>

| <span data-ttu-id="f7b4f-903">方法</span><span class="sxs-lookup"><span data-stu-id="f7b4f-903">Method</span></span>                           | <span data-ttu-id="f7b4f-904">説明</span><span class="sxs-lookup"><span data-stu-id="f7b4f-904">Description</span></span>                                            |
|----------------------------------|--------------------------------------------------------|
| <span data-ttu-id="f7b4f-905">public str entryId()</span><span class="sxs-lookup"><span data-stu-id="f7b4f-905">public str entryId()</span></span>             |                                                        |
| <span data-ttu-id="f7b4f-906">public str getBody()</span><span class="sxs-lookup"><span data-stu-id="f7b4f-906">public str getBody()</span></span>             |                                                        |
| <span data-ttu-id="f7b4f-907">public boolean save()</span><span class="sxs-lookup"><span data-stu-id="f7b4f-907">public boolean save()</span></span>            |                                                        |
| <span data-ttu-id="f7b4f-908">public boolean setBody(str body)</span><span class="sxs-lookup"><span data-stu-id="f7b4f-908">public boolean setBody(str body)</span></span> |                                                        |
| <span data-ttu-id="f7b4f-909">public void new()</span><span class="sxs-lookup"><span data-stu-id="f7b4f-909">public void new()</span></span>                | <span data-ttu-id="f7b4f-910">MapiExMessage クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-910">Initializes a new instance of the MapiExMessage class.</span></span> |
| <span data-ttu-id="f7b4f-911">public void finalize()</span><span class="sxs-lookup"><span data-stu-id="f7b4f-911">public void finalize()</span></span>           |                                                        |
| <span data-ttu-id="f7b4f-912">public void close()</span><span class="sxs-lookup"><span data-stu-id="f7b4f-912">public void close()</span></span>              |                                                        |

### <a name="method-entryid"></a><span data-ttu-id="f7b4f-913">メソッド entryId</span><span class="sxs-lookup"><span data-stu-id="f7b4f-913">Method entryId</span></span>

    public str entryId()

#### <a name="return-value"></a><span data-ttu-id="f7b4f-914">戻り値</span><span class="sxs-lookup"><span data-stu-id="f7b4f-914">Return Value</span></span>

### <a name="method-getbody"></a><span data-ttu-id="f7b4f-915">メソッド getBody</span><span class="sxs-lookup"><span data-stu-id="f7b4f-915">Method getBody</span></span>

    public str getBody()

#### <a name="return-value"></a><span data-ttu-id="f7b4f-916">戻り値</span><span class="sxs-lookup"><span data-stu-id="f7b4f-916">Return Value</span></span>

### <a name="method-save"></a><span data-ttu-id="f7b4f-917">メソッド save</span><span class="sxs-lookup"><span data-stu-id="f7b4f-917">Method save</span></span>

    public boolean save()

#### <a name="return-value"></a><span data-ttu-id="f7b4f-918">戻り値</span><span class="sxs-lookup"><span data-stu-id="f7b4f-918">Return Value</span></span>

### <a name="method-setbody"></a><span data-ttu-id="f7b4f-919">メソッド setBody</span><span class="sxs-lookup"><span data-stu-id="f7b4f-919">Method setBody</span></span>

    public boolean setBody(str body)

#### <a name="parameters"></a><span data-ttu-id="f7b4f-920">パラメーター</span><span class="sxs-lookup"><span data-stu-id="f7b4f-920">Parameters</span></span>

<span data-ttu-id="f7b4f-921">body</span><span class="sxs-lookup"><span data-stu-id="f7b4f-921">body</span></span>  

#### <a name="return-value"></a><span data-ttu-id="f7b4f-922">戻り値</span><span class="sxs-lookup"><span data-stu-id="f7b4f-922">Return Value</span></span>

### <a name="method-new"></a><span data-ttu-id="f7b4f-923">メソッド new</span><span class="sxs-lookup"><span data-stu-id="f7b4f-923">Method new</span></span>

<span data-ttu-id="f7b4f-924">MapiExMessage クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-924">Initializes a new instance of the MapiExMessage class.</span></span>

    public void new()

### <a name="method-finalize"></a><span data-ttu-id="f7b4f-925">メソッド finalize</span><span class="sxs-lookup"><span data-stu-id="f7b4f-925">Method finalize</span></span>

    public void finalize()

### <a name="method-close"></a><span data-ttu-id="f7b4f-926">メソッド close</span><span class="sxs-lookup"><span data-stu-id="f7b4f-926">Method close</span></span>

    public void close()

## <a name="class-mapiextask"></a><span data-ttu-id="f7b4f-927">クラス MapiExTask</span><span class="sxs-lookup"><span data-stu-id="f7b4f-927">Class MapiExTask</span></span>
    class MapiExTask extends MapiExMessage

### <a name="remarks"></a><span data-ttu-id="f7b4f-928">備考</span><span class="sxs-lookup"><span data-stu-id="f7b4f-928">Remarks</span></span>

### <a name="examples"></a><span data-ttu-id="f7b4f-929">例</span><span class="sxs-lookup"><span data-stu-id="f7b4f-929">Examples</span></span>

### <a name="methods"></a><span data-ttu-id="f7b4f-930">メソッド</span><span class="sxs-lookup"><span data-stu-id="f7b4f-930">Methods</span></span>

| <span data-ttu-id="f7b4f-931">方法</span><span class="sxs-lookup"><span data-stu-id="f7b4f-931">Method</span></span>                           | <span data-ttu-id="f7b4f-932">説明</span><span class="sxs-lookup"><span data-stu-id="f7b4f-932">Description</span></span>                                         |
|----------------------------------|-----------------------------------------------------|
| <span data-ttu-id="f7b4f-933">public str entryId()</span><span class="sxs-lookup"><span data-stu-id="f7b4f-933">public str entryId()</span></span>             |                                                     |
| <span data-ttu-id="f7b4f-934">public str getBody()</span><span class="sxs-lookup"><span data-stu-id="f7b4f-934">public str getBody()</span></span>             |                                                     |
| <span data-ttu-id="f7b4f-935">public boolean save()</span><span class="sxs-lookup"><span data-stu-id="f7b4f-935">public boolean save()</span></span>            |                                                     |
| <span data-ttu-id="f7b4f-936">public boolean setBody(str body)</span><span class="sxs-lookup"><span data-stu-id="f7b4f-936">public boolean setBody(str body)</span></span> |                                                     |
| <span data-ttu-id="f7b4f-937">public void finalize()</span><span class="sxs-lookup"><span data-stu-id="f7b4f-937">public void finalize()</span></span>           |                                                     |
| <span data-ttu-id="f7b4f-938">public void close()</span><span class="sxs-lookup"><span data-stu-id="f7b4f-938">public void close()</span></span>              |                                                     |
| <span data-ttu-id="f7b4f-939">public void new()</span><span class="sxs-lookup"><span data-stu-id="f7b4f-939">public void new()</span></span>                | <span data-ttu-id="f7b4f-940">MapiExTask クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-940">Initializes a new instance of the MapiExTask class.</span></span> |

### <a name="method-entryid"></a><span data-ttu-id="f7b4f-941">メソッド entryId</span><span class="sxs-lookup"><span data-stu-id="f7b4f-941">Method entryId</span></span>

    public str entryId()

#### <a name="return-value"></a><span data-ttu-id="f7b4f-942">戻り値</span><span class="sxs-lookup"><span data-stu-id="f7b4f-942">Return Value</span></span>

### <a name="method-getbody"></a><span data-ttu-id="f7b4f-943">メソッド getBody</span><span class="sxs-lookup"><span data-stu-id="f7b4f-943">Method getBody</span></span>

    public str getBody()

#### <a name="return-value"></a><span data-ttu-id="f7b4f-944">戻り値</span><span class="sxs-lookup"><span data-stu-id="f7b4f-944">Return Value</span></span>

### <a name="method-save"></a><span data-ttu-id="f7b4f-945">メソッド save</span><span class="sxs-lookup"><span data-stu-id="f7b4f-945">Method save</span></span>

    public boolean save()

#### <a name="return-value"></a><span data-ttu-id="f7b4f-946">戻り値</span><span class="sxs-lookup"><span data-stu-id="f7b4f-946">Return Value</span></span>

### <a name="method-setbody"></a><span data-ttu-id="f7b4f-947">メソッド setBody</span><span class="sxs-lookup"><span data-stu-id="f7b4f-947">Method setBody</span></span>

    public boolean setBody(str body)

#### <a name="parameters"></a><span data-ttu-id="f7b4f-948">パラメーター</span><span class="sxs-lookup"><span data-stu-id="f7b4f-948">Parameters</span></span>

<span data-ttu-id="f7b4f-949">body</span><span class="sxs-lookup"><span data-stu-id="f7b4f-949">body</span></span>  

#### <a name="return-value"></a><span data-ttu-id="f7b4f-950">戻り値</span><span class="sxs-lookup"><span data-stu-id="f7b4f-950">Return Value</span></span>

### <a name="method-finalize"></a><span data-ttu-id="f7b4f-951">メソッド finalize</span><span class="sxs-lookup"><span data-stu-id="f7b4f-951">Method finalize</span></span>

    public void finalize()

### <a name="method-close"></a><span data-ttu-id="f7b4f-952">メソッド close</span><span class="sxs-lookup"><span data-stu-id="f7b4f-952">Method close</span></span>

    public void close()

### <a name="method-new"></a><span data-ttu-id="f7b4f-953">メソッド new</span><span class="sxs-lookup"><span data-stu-id="f7b4f-953">Method new</span></span>

<span data-ttu-id="f7b4f-954">MapiExTask クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-954">Initializes a new instance of the MapiExTask class.</span></span>

    public void new()

## <a name="class-mapifiledesc"></a><span data-ttu-id="f7b4f-955">クラス MapiFileDesc</span><span class="sxs-lookup"><span data-stu-id="f7b4f-955">Class MapiFileDesc</span></span>
    class MapiFileDesc extends Object

<span data-ttu-id="f7b4f-956">MapiFileDesc クラスは、メッセージに関連付けられているファイルを取得および設定します。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-956">The MapiFileDesc class gets and sets the files that are attached to messages.</span></span>

### <a name="remarks"></a><span data-ttu-id="f7b4f-957">備考</span><span class="sxs-lookup"><span data-stu-id="f7b4f-957">Remarks</span></span>

<span data-ttu-id="f7b4f-958">ファイルの説明は、ファイルの 2 つのタイプの情報で構成されています。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-958">The file description consists of two types of information for the file:</span></span>

-   <span data-ttu-id="f7b4f-959">ディスク上のファイルをポイントするパス メソッド</span><span class="sxs-lookup"><span data-stu-id="f7b4f-959">A path method, which points to a file on disk</span></span>
-   <span data-ttu-id="f7b4f-960">fileName メソッドには、ユーザーに表示されるファイル名が含まれます。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-960">A fileName method, which contains the file name as it will be presented to the user.</span></span>

### <a name="examples"></a><span data-ttu-id="f7b4f-961">例</span><span class="sxs-lookup"><span data-stu-id="f7b4f-961">Examples</span></span>

    static void example() 
    { 
        MapiMessage msg = New MapiMessage(); 
        MapiFileDesc attach = new MapiFileDesc(); 
        attach.Path("C:\\files\\myfile.txt"); 
    }

### <a name="methods"></a><span data-ttu-id="f7b4f-962">メソッド</span><span class="sxs-lookup"><span data-stu-id="f7b4f-962">Methods</span></span>

| <span data-ttu-id="f7b4f-963">方法</span><span class="sxs-lookup"><span data-stu-id="f7b4f-963">Method</span></span>                                | <span data-ttu-id="f7b4f-964">説明</span><span class="sxs-lookup"><span data-stu-id="f7b4f-964">Description</span></span>                                           |
|---------------------------------------|-------------------------------------------------------|
| <span data-ttu-id="f7b4f-965">public str fileName(\[str filename\])</span><span class="sxs-lookup"><span data-stu-id="f7b4f-965">public str fileName(\[str filename\])</span></span> |                                                       |
| <span data-ttu-id="f7b4f-966">public str path(\[str thePath\])</span><span class="sxs-lookup"><span data-stu-id="f7b4f-966">public str path(\[str thePath\])</span></span>      |                                                       |
| <span data-ttu-id="f7b4f-967">public void new()</span><span class="sxs-lookup"><span data-stu-id="f7b4f-967">public void new()</span></span>                     | <span data-ttu-id="f7b4f-968">MapiFileDesc クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-968">Initializes a new instance of the MapiFileDesc class.</span></span> |
| <span data-ttu-id="f7b4f-969">public void finalize()</span><span class="sxs-lookup"><span data-stu-id="f7b4f-969">public void finalize()</span></span>                |                                                       |

### <a name="method-filename"></a><span data-ttu-id="f7b4f-970">メソッド fileName</span><span class="sxs-lookup"><span data-stu-id="f7b4f-970">Method fileName</span></span>

    public str fileName([str filename])

#### <a name="parameters"></a><span data-ttu-id="f7b4f-971">パラメーター</span><span class="sxs-lookup"><span data-stu-id="f7b4f-971">Parameters</span></span>

<span data-ttu-id="f7b4f-972">filename</span><span class="sxs-lookup"><span data-stu-id="f7b4f-972">filename</span></span>  

#### <a name="return-value"></a><span data-ttu-id="f7b4f-973">戻り値</span><span class="sxs-lookup"><span data-stu-id="f7b4f-973">Return Value</span></span>

### <a name="method-path"></a><span data-ttu-id="f7b4f-974">メソッド path</span><span class="sxs-lookup"><span data-stu-id="f7b4f-974">Method path</span></span>

    public str path([str thePath])

#### <a name="parameters"></a><span data-ttu-id="f7b4f-975">パラメーター</span><span class="sxs-lookup"><span data-stu-id="f7b4f-975">Parameters</span></span>

<span data-ttu-id="f7b4f-976">thePath</span><span class="sxs-lookup"><span data-stu-id="f7b4f-976">thePath</span></span>  

#### <a name="return-value"></a><span data-ttu-id="f7b4f-977">戻り値</span><span class="sxs-lookup"><span data-stu-id="f7b4f-977">Return Value</span></span>

### <a name="method-new"></a><span data-ttu-id="f7b4f-978">メソッド new</span><span class="sxs-lookup"><span data-stu-id="f7b4f-978">Method new</span></span>

<span data-ttu-id="f7b4f-979">MapiFileDesc クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-979">Initializes a new instance of the MapiFileDesc class.</span></span>

    public void new()

### <a name="method-finalize"></a><span data-ttu-id="f7b4f-980">メソッド finalize</span><span class="sxs-lookup"><span data-stu-id="f7b4f-980">Method finalize</span></span>

    public void finalize()

## <a name="class-mapimessage"></a><span data-ttu-id="f7b4f-981">クラス MapiMessage</span><span class="sxs-lookup"><span data-stu-id="f7b4f-981">Class MapiMessage</span></span>
    class MapiMessage extends Object

<span data-ttu-id="f7b4f-982">MapiMessage クラスには、MAPI システムから送受信されるメッセージが含まれています。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-982">The MapiMessage class contains a message that is sent to or received from the MAPI system.</span></span> <span data-ttu-id="f7b4f-983">メッセージには、件名、テキスト、受信者情報、および添付ファイル情報が含まれます。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-983">The message includes a subject, text, recipient information, and attachment information.</span></span>

### <a name="remarks"></a><span data-ttu-id="f7b4f-984">備考</span><span class="sxs-lookup"><span data-stu-id="f7b4f-984">Remarks</span></span>

<span data-ttu-id="f7b4f-985">メッセージを送受信するとき、メッセージは、MapiMessage対象として MAPI システムとの間を渡されます。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-985">When you send or receive a message, the message is passed to and from the MAPI system as a MapiMessage object.</span></span>

### <a name="examples"></a><span data-ttu-id="f7b4f-986">例</span><span class="sxs-lookup"><span data-stu-id="f7b4f-986">Examples</span></span>

### <a name="methods"></a><span data-ttu-id="f7b4f-987">メソッド</span><span class="sxs-lookup"><span data-stu-id="f7b4f-987">Methods</span></span>

| <span data-ttu-id="f7b4f-988">方法</span><span class="sxs-lookup"><span data-stu-id="f7b4f-988">Method</span></span>                                                        | <span data-ttu-id="f7b4f-989">説明</span><span class="sxs-lookup"><span data-stu-id="f7b4f-989">Description</span></span>                                                                                             |
|---------------------------------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f7b4f-990">public str conversationID(\[str conversationId\])</span><span class="sxs-lookup"><span data-stu-id="f7b4f-990">public str conversationID(\[str conversationId\])</span></span>             | <span data-ttu-id="f7b4f-991">メッセージが所属する会話スレッドを識別する文字列を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-991">Gets or sets the string that identifies the conversation thread to which the message belongs.</span></span>           |
| <span data-ttu-id="f7b4f-992">public str dateReceived(\[Date theDate\])</span><span class="sxs-lookup"><span data-stu-id="f7b4f-992">public str dateReceived(\[Date theDate\])</span></span>                     | <span data-ttu-id="f7b4f-993">メッセージを受信した日付を返します。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-993">Returns the date when the message was received.</span></span>                                                         |
| <span data-ttu-id="f7b4f-994">public int flags(\[int flags\])</span><span class="sxs-lookup"><span data-stu-id="f7b4f-994">public int flags(\[int flags\])</span></span>                               | <span data-ttu-id="f7b4f-995">メッセージ ステータス フラグのビットを設定または取得します。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-995">Set or get a bitmask of the message status flags.</span></span>                                                       |
| <span data-ttu-id="f7b4f-996">public MapiFileDesc getFileNo(int fileNo)</span><span class="sxs-lookup"><span data-stu-id="f7b4f-996">public MapiFileDesc getFileNo(int fileNo)</span></span>                     | <span data-ttu-id="f7b4f-997">メッセージからの添付ファイルを取得します。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-997">Gets a file attachment from a message.</span></span>                                                                  |
| <span data-ttu-id="f7b4f-998">public MapiRecipDesc getRecipNo(int recipentNo)</span><span class="sxs-lookup"><span data-stu-id="f7b4f-998">public MapiRecipDesc getRecipNo(int recipentNo)</span></span>               | <span data-ttu-id="f7b4f-999">MapiRecipDesc オブジェクトにあるメッセージの受信者に関する情報を取得します。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-999">Retrieves information about a message recipient in a MapiRecipDesc object.</span></span>                              |
| <span data-ttu-id="f7b4f-1000">public str messageType(\[str messageType\])</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1000">public str messageType(\[str messageType\])</span></span>                   | <span data-ttu-id="f7b4f-1001">IPM (個人間メッセージ) タイプではないメッセージを示す文字列を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1001">Gets or sets the string that indicates that the message is not of the IPM (interpersonal message) type.</span></span> |
| <span data-ttu-id="f7b4f-1002">public int numFiles(\[int numFiles\])</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1002">public int numFiles(\[int numFiles\])</span></span>                         |                                                                                                         |
| <span data-ttu-id="f7b4f-1003">public int numRecips(\[int numRecips\])</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1003">public int numRecips(\[int numRecips\])</span></span>                       |                                                                                                         |
| <span data-ttu-id="f7b4f-1004">public MapiRecipDesc originator(\[MapiRecipDesc originator\])</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1004">public MapiRecipDesc originator(\[MapiRecipDesc originator\])</span></span> |                                                                                                         |
| <span data-ttu-id="f7b4f-1005">public str subject(\[str subject\])</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1005">public str subject(\[str subject\])</span></span>                           |                                                                                                         |
| <span data-ttu-id="f7b4f-1006">public str text(\[str text\])</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1006">public str text(\[str text\])</span></span>                                 |                                                                                                         |
| <span data-ttu-id="f7b4f-1007">public void new()</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1007">public void new()</span></span>                                             | <span data-ttu-id="f7b4f-1008">MapiMessage クラスのインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1008">Initializes an instance of the MapiMessage class.</span></span>                                                       |
| <span data-ttu-id="f7b4f-1009">public void finalize()</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1009">public void finalize()</span></span>                                        |                                                                                                         |
| <span data-ttu-id="f7b4f-1010">public void setRecipNo(int recipNo, MapiRecipDesc recipient)</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1010">public void setRecipNo(int recipNo, MapiRecipDesc recipient)</span></span>  | <span data-ttu-id="f7b4f-1011">メッセージに受信者を追加します。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1011">Adds a recipient to the message.</span></span>                                                                        |
| <span data-ttu-id="f7b4f-1012">public void setFileNo(int fileNo, MapiFileDesc file)</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1012">public void setFileNo(int fileNo, MapiFileDesc file)</span></span>          | <span data-ttu-id="f7b4f-1013">メッセージの添付ファイルを設定します。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1013">Sets a file attachment for the message.</span></span>                                                                 |

### <a name="method-conversationid"></a><span data-ttu-id="f7b4f-1014">メソッド conversationID</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1014">Method conversationID</span></span>

<span data-ttu-id="f7b4f-1015">メッセージが所属する会話スレッドを識別する文字列を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1015">Gets or sets the string that identifies the conversation thread to which the message belongs.</span></span>

    public str conversationID([str conversationId])

#### <a name="parameters"></a><span data-ttu-id="f7b4f-1016">パラメーター</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1016">Parameters</span></span>

<span data-ttu-id="f7b4f-1017">conversationId</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1017">conversationId</span></span>  
<span data-ttu-id="f7b4f-1018">会話スレッドの ID。省略可能。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1018">The ID of the conversation thread; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="f7b4f-1019">戻り値</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1019">Return Value</span></span>

<span data-ttu-id="f7b4f-1020">メッセージが所属する会話スレッドを識別する文字列。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1020">A string that identifies the conversation thread to which the message belongs.</span></span>

#### <a name="remarks"></a><span data-ttu-id="f7b4f-1021">備考</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1021">Remarks</span></span>

<span data-ttu-id="f7b4f-1022">メッセージング システムの中には、無視してこのメンバーを返さないものがあります。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1022">Some messaging systems might ignore and not return this member.</span></span>

### <a name="method-datereceived"></a><span data-ttu-id="f7b4f-1023">メソッド dateReceived</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1023">Method dateReceived</span></span>

<span data-ttu-id="f7b4f-1024">メッセージを受信した日付を返します。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1024">Returns the date when the message was received.</span></span>

    public str dateReceived([Date theDate])

#### <a name="parameters"></a><span data-ttu-id="f7b4f-1025">パラメーター</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1025">Parameters</span></span>

<span data-ttu-id="f7b4f-1026">theDate</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1026">theDate</span></span>  
<span data-ttu-id="f7b4f-1027">メッセージを受信した日付 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1027">The date when the message was received; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="f7b4f-1028">戻り値</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1028">Return Value</span></span>

<span data-ttu-id="f7b4f-1029">メッセージが受信された日付を示す文字列。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1029">A string that indicates the date when the message was received.</span></span>

#### <a name="remarks"></a><span data-ttu-id="f7b4f-1030">備考</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1030">Remarks</span></span>

<span data-ttu-id="f7b4f-1031">返される文字列の形式は、YYYY/MM/DD HH:MMであり、24時間制を使用します。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1031">The format of the string that is returned is YYYY/MM/DD HH:MM and uses a 24-hour clock.</span></span>

### <a name="method-flags"></a><span data-ttu-id="f7b4f-1032">メソッド flags</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1032">Method flags</span></span>

<span data-ttu-id="f7b4f-1033">メッセージ ステータス フラグのビットを設定または取得します。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1033">Set or get a bitmask of the message status flags.</span></span>

    public int flags([int flags])

#### <a name="parameters"></a><span data-ttu-id="f7b4f-1034">パラメーター</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1034">Parameters</span></span>

<span data-ttu-id="f7b4f-1035">flags</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1035">flags</span></span>  
<span data-ttu-id="f7b4f-1036">メッセージ ステータス フラグ (オプション)。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1036">The message status flags; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="f7b4f-1037">戻り値</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1037">Return Value</span></span>

<span data-ttu-id="f7b4f-1038">メッセージ ステータス フラグのビット。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1038">A bitmask of the message status flags.</span></span>

#### <a name="remarks"></a><span data-ttu-id="f7b4f-1039">備考</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1039">Remarks</span></span>

<span data-ttu-id="f7b4f-1040">次のフラグを設定できます。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1040">The following flags can be set:</span></span>

-   <span data-ttu-id="f7b4f-1041">\#MAPI\_RECEIPT\_REQUESTED – 受領通知のリクエストが要求されました。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1041">\#MAPI\_RECEIPT\_REQUESTED – Receipt notification is requested.</span></span> <span data-ttu-id="f7b4f-1042">クライアント アプリケーションは、メッセージを送信するときにこのビットを設定します。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1042">Client applications set this bit when they send a message.</span></span>
-   <span data-ttu-id="f7b4f-1043">\#MAPI\_SENT – メッセージが送信されました。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1043">\#MAPI\_SENT – The message has been sent.</span></span>
-   <span data-ttu-id="f7b4f-1044">\#MAPI\_UNREAD – メッセージが未読です。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1044">\#MAPI\_UNREAD – The message has not been read.</span></span>

### <a name="method-getfileno"></a><span data-ttu-id="f7b4f-1045">メソッド getFileNo</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1045">Method getFileNo</span></span>

<span data-ttu-id="f7b4f-1046">メッセージからの添付ファイルを取得します。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1046">Gets a file attachment from a message.</span></span>

    public MapiFileDesc getFileNo(int fileNo)

#### <a name="parameters"></a><span data-ttu-id="f7b4f-1047">パラメーター</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1047">Parameters</span></span>

<span data-ttu-id="f7b4f-1048">fileNo</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1048">fileNo</span></span>  
<span data-ttu-id="f7b4f-1049">取得する添付ファイルのインデックス。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1049">The index of the attachment to retrieve.</span></span> <span data-ttu-id="f7b4f-1050">インデックスは 1 から始まり、numFiles メソッドを使用して添付ファイルの総数を取得できます。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1050">The index starts at 1, and the total number of attachments can be retrieved using the numFiles method.</span></span>

#### <a name="return-value"></a><span data-ttu-id="f7b4f-1051">戻り値</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1051">Return Value</span></span>

<span data-ttu-id="f7b4f-1052">添付ファイルに関する情報を含む MapiFileDesc オブジェクトを返します。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1052">Returns a MapiFileDesc object that contains information about the attachment.</span></span>

#### <a name="remarks"></a><span data-ttu-id="f7b4f-1053">備考</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1053">Remarks</span></span>

<span data-ttu-id="f7b4f-1054">添付ファイルは、MapiFileDesc オブジェクトで返されます。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1054">The attached file is returned in a MapiFileDesc object.</span></span>

#### <a name="examples"></a><span data-ttu-id="f7b4f-1055">例</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1055">Examples</span></span>

    { 
        MapiFileDesc attachment; 
        MapiMessage message; 
        // Retrieve message. 
        // ...  
        if (message.NumFiles() >= 1) 
        { 
            attachment = message.GetFileNo(1); 
        } 
    }

### <a name="method-getrecipno"></a><span data-ttu-id="f7b4f-1056">メソッド getRecipNo</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1056">Method getRecipNo</span></span>

<span data-ttu-id="f7b4f-1057">MapiRecipDesc オブジェクトにあるメッセージの受信者に関する情報を取得します。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1057">Retrieves information about a message recipient in a MapiRecipDesc object.</span></span>

    public MapiRecipDesc getRecipNo(int recipentNo)

#### <a name="parameters"></a><span data-ttu-id="f7b4f-1058">パラメーター</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1058">Parameters</span></span>

<span data-ttu-id="f7b4f-1059">recipentNo</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1059">recipentNo</span></span>  
<span data-ttu-id="f7b4f-1060">取得する受信者の番号。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1060">The number of the recipient to retrieve.</span></span> <span data-ttu-id="f7b4f-1061">番号付けは 1 から始まり、numRecips メソッドを使用して受信者の総数を読み込むことができます。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1061">The numbering starts at 1, and the total number of recipients can be read by using the numRecips method.</span></span>

#### <a name="return-value"></a><span data-ttu-id="f7b4f-1062">戻り値</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1062">Return Value</span></span>

<span data-ttu-id="f7b4f-1063">受信者または nullNothingnullptrunita null 参照 (Visual Basic にはなし) を説明する MapiRecipDesc オブジェクト。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1063">A MapiRecipDesc object that describes the recipient or nullNothingnullptrunita null reference (Nothing in Visual Basic).</span></span>

### <a name="method-messagetype"></a><span data-ttu-id="f7b4f-1064">メソッド messageType</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1064">Method messageType</span></span>

<span data-ttu-id="f7b4f-1065">IPM (個人間メッセージ) タイプではないメッセージを示す文字列を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1065">Gets or sets the string that indicates that the message is not of the IPM (interpersonal message) type.</span></span>

    public str messageType([str messageType])

#### <a name="parameters"></a><span data-ttu-id="f7b4f-1066">パラメーター</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1066">Parameters</span></span>

<span data-ttu-id="f7b4f-1067">messageType</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1067">messageType</span></span>  
<span data-ttu-id="f7b4f-1068">メッセージに設定する messageType 値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1068">The messageType value to set for the message; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="f7b4f-1069">戻り値</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1069">Return Value</span></span>

<span data-ttu-id="f7b4f-1070">messagetype 文字列。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1070">A messagetype string.</span></span>

#### <a name="remarks"></a><span data-ttu-id="f7b4f-1071">備考</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1071">Remarks</span></span>

<span data-ttu-id="f7b4f-1072">アプリケーションは、IPM ではないメッセージのメッセージ タイプを選択できます。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1072">Applications can select message types for messages that are not IPMs.</span></span> <span data-ttu-id="f7b4f-1073">IPM だけをサポートするクライアントは、メッセージを読むときに MessageType メンバーを無視し、メッセージを送信するときに空にすることができます。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1073">Clients that support only IPMs can ignore the MessageType member when they read messages and set it to empty when they send messages.</span></span>

### <a name="method-numfiles"></a><span data-ttu-id="f7b4f-1074">メソッド numFiles</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1074">Method numFiles</span></span>

    public int numFiles([int numFiles])

#### <a name="parameters"></a><span data-ttu-id="f7b4f-1075">パラメーター</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1075">Parameters</span></span>

<span data-ttu-id="f7b4f-1076">numFiles</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1076">numFiles</span></span>  

#### <a name="return-value"></a><span data-ttu-id="f7b4f-1077">戻り値</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1077">Return Value</span></span>

### <a name="method-numrecips"></a><span data-ttu-id="f7b4f-1078">メソッド numRecips</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1078">Method numRecips</span></span>

    public int numRecips([int numRecips])

#### <a name="parameters"></a><span data-ttu-id="f7b4f-1079">パラメーター</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1079">Parameters</span></span>

<span data-ttu-id="f7b4f-1080">numRecips</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1080">numRecips</span></span>  

#### <a name="return-value"></a><span data-ttu-id="f7b4f-1081">戻り値</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1081">Return Value</span></span>

### <a name="method-originator"></a><span data-ttu-id="f7b4f-1082">メソッド originator</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1082">Method originator</span></span>

    public MapiRecipDesc originator([MapiRecipDesc originator])

#### <a name="parameters"></a><span data-ttu-id="f7b4f-1083">パラメーター</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1083">Parameters</span></span>

<span data-ttu-id="f7b4f-1084">originator</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1084">originator</span></span>  

#### <a name="return-value"></a><span data-ttu-id="f7b4f-1085">戻り値</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1085">Return Value</span></span>

### <a name="method-subject"></a><span data-ttu-id="f7b4f-1086">メソッド subject</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1086">Method subject</span></span>

    public str subject([str subject])

#### <a name="parameters"></a><span data-ttu-id="f7b4f-1087">パラメーター</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1087">Parameters</span></span>

<span data-ttu-id="f7b4f-1088">subject</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1088">subject</span></span>  

#### <a name="return-value"></a><span data-ttu-id="f7b4f-1089">戻り値</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1089">Return Value</span></span>

### <a name="method-text"></a><span data-ttu-id="f7b4f-1090">メソッド text</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1090">Method text</span></span>

    public str text([str text])

#### <a name="parameters"></a><span data-ttu-id="f7b4f-1091">パラメーター</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1091">Parameters</span></span>

<span data-ttu-id="f7b4f-1092">テキスト</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1092">text</span></span>  

#### <a name="return-value"></a><span data-ttu-id="f7b4f-1093">戻り値</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1093">Return Value</span></span>

### <a name="method-new"></a><span data-ttu-id="f7b4f-1094">メソッド new</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1094">Method new</span></span>

<span data-ttu-id="f7b4f-1095">MapiMessage クラスのインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1095">Initializes an instance of the MapiMessage class.</span></span>

    public void new()

### <a name="method-finalize"></a><span data-ttu-id="f7b4f-1096">メソッド finalize</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1096">Method finalize</span></span>

    public void finalize()

### <a name="method-setrecipno"></a><span data-ttu-id="f7b4f-1097">メソッド setRecipNo</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1097">Method setRecipNo</span></span>

<span data-ttu-id="f7b4f-1098">メッセージに受信者を追加します。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1098">Adds a recipient to the message.</span></span>

    public void setRecipNo(int recipNo, MapiRecipDesc recipient)

#### <a name="parameters"></a><span data-ttu-id="f7b4f-1099">パラメーター</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1099">Parameters</span></span>

<span data-ttu-id="f7b4f-1100">recipNo</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1100">recipNo</span></span>  
<span data-ttu-id="f7b4f-1101">受信者を説明する MapiRecipDesc オブジェクト。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1101">The MapiRecipDesc object that describes the recipient.</span></span>

<!-- -->

<span data-ttu-id="f7b4f-1102">recipient</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1102">recipient</span></span>  
<span data-ttu-id="f7b4f-1103">受信者を説明する MapiRecipDesc オブジェクト。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1103">The MapiRecipDesc object that describes the recipient.</span></span>

#### <a name="remarks"></a><span data-ttu-id="f7b4f-1104">備考</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1104">Remarks</span></span>

<span data-ttu-id="f7b4f-1105">正しい MapiRecipDesc オブジェクトをユーザーが入力した名前から取得する必要がある場合は、resolveName メソッドを使用します。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1105">If you have to get a correct MapiRecipDesc object from a name that a user entered, use the resolveName method.</span></span>

### <a name="method-setfileno"></a><span data-ttu-id="f7b4f-1106">メソッド setFileNo</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1106">Method setFileNo</span></span>

<span data-ttu-id="f7b4f-1107">メッセージの添付ファイルを設定します。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1107">Sets a file attachment for the message.</span></span>

    public void setFileNo(int fileNo, MapiFileDesc file)

#### <a name="parameters"></a><span data-ttu-id="f7b4f-1108">パラメーター</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1108">Parameters</span></span>

<span data-ttu-id="f7b4f-1109">fileNo</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1109">fileNo</span></span>  
<span data-ttu-id="f7b4f-1110">添付ファイルを説明する MapiFileDesc オブジェクト。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1110">The MapiFileDesc object that describes the attachment.</span></span>

<!-- -->

<span data-ttu-id="f7b4f-1111">ファイル</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1111">file</span></span>  
<span data-ttu-id="f7b4f-1112">添付ファイルを説明する MapiFileDesc オブジェクト。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1112">The MapiFileDesc object that describes the attachment.</span></span>

#### <a name="remarks"></a><span data-ttu-id="f7b4f-1113">備考</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1113">Remarks</span></span>

<span data-ttu-id="f7b4f-1114">添付ファイルには、1 から始まる番号が付けられます。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1114">The attachments are numbered from 1.</span></span> <span data-ttu-id="f7b4f-1115">したがって、最初の添付ファイルには番号 1 を付ける必要があります。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1115">Therefore, the first attachment should be numbered 1.</span></span> <span data-ttu-id="f7b4f-1116">numFiles メソッドを呼び出してアタッチメントの数を取得することができます。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1116">You can call the numFiles method to retrieve the number of attachments.</span></span>

#### <a name="examples"></a><span data-ttu-id="f7b4f-1117">例</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1117">Examples</span></span>

    { 
        MapiMessage msg = new MapiMessage(); 
        MapiFileDesc attachment = new MapiFileDesc(); 
        attachment.Path("C:\\files\\info.txt"); 
        msg.SetFileNo(1,attachment); 
    }

## <a name="class-mapirecipdesc"></a><span data-ttu-id="f7b4f-1118">クラス MapiRecipDesc</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1118">Class MapiRecipDesc</span></span>
    class MapiRecipDesc extends Object

### <a name="remarks"></a><span data-ttu-id="f7b4f-1119">備考</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1119">Remarks</span></span>

### <a name="examples"></a><span data-ttu-id="f7b4f-1120">例</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1120">Examples</span></span>

### <a name="methods"></a><span data-ttu-id="f7b4f-1121">メソッド</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1121">Methods</span></span>

| <span data-ttu-id="f7b4f-1122">方法</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1122">Method</span></span>                                    | <span data-ttu-id="f7b4f-1123">説明</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1123">Description</span></span>                                                                                                                                   |
|-------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f7b4f-1124">public str address(\[str Address\])</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1124">public str address(\[str Address\])</span></span>       |                                                                                                                                               |
| <span data-ttu-id="f7b4f-1125">public str name(\[str Name\])</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1125">public str name(\[str Name\])</span></span>             | <span data-ttu-id="f7b4f-1126">フォーム、レポート、テーブル、クエリ、または別の Finance and Operations アプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1126">Gets or sets the name that is used in the code to identify a form, report, table, query, or another Finance and Operations application object.</span></span> |
| <span data-ttu-id="f7b4f-1127">public int recipClass(\[int RecipClass\])</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1127">public int recipClass(\[int RecipClass\])</span></span> |                                                                                                                                               |
| <span data-ttu-id="f7b4f-1128">public void new()</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1128">public void new()</span></span>                         | <span data-ttu-id="f7b4f-1129">MapiRecipDesc クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1129">Initializes a new instance of the MapiRecipDesc class.</span></span>                                                                                        |
| <span data-ttu-id="f7b4f-1130">public void finalize()</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1130">public void finalize()</span></span>                    |                                                                                                                                               |

### <a name="method-address"></a><span data-ttu-id="f7b4f-1131">メソッド address</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1131">Method address</span></span>

    public str address([str Address])

#### <a name="parameters"></a><span data-ttu-id="f7b4f-1132">パラメーター</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1132">Parameters</span></span>

<span data-ttu-id="f7b4f-1133">アドレス</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1133">Address</span></span>  

#### <a name="return-value"></a><span data-ttu-id="f7b4f-1134">戻り値</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1134">Return Value</span></span>

### <a name="method-name"></a><span data-ttu-id="f7b4f-1135">メソッド名</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1135">Method name</span></span>

<span data-ttu-id="f7b4f-1136">フォーム、レポート、テーブル、クエリ、または別の Finance and Operations アプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1136">Gets or sets the name that is used in the code to identify a form, report, table, query, or another Finance and Operations application object.</span></span>

    public str name([str Name])

#### <a name="parameters"></a><span data-ttu-id="f7b4f-1137">パラメーター</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1137">Parameters</span></span>

<span data-ttu-id="f7b4f-1138">氏名</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1138">Name</span></span>  

#### <a name="return-value"></a><span data-ttu-id="f7b4f-1139">戻り値</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1139">Return Value</span></span>

<span data-ttu-id="f7b4f-1140">アプリケーション オブジェクトを識別するためにコードで使用される名前。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1140">The name that is used in the code to identify an application object.</span></span>

#### <a name="remarks"></a><span data-ttu-id="f7b4f-1141">備考</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1141">Remarks</span></span>

<span data-ttu-id="f7b4f-1142">オブジェクトの名前プロパティ値は、コードの競合を避けるために、次の基準を満たしている必要があります。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1142">The name property value of an object must meet the following criteria to avoid code conflicts:</span></span>

-   <span data-ttu-id="f7b4f-1143">文字で始めます。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1143">Begins with a letter.</span></span>
-   <span data-ttu-id="f7b4f-1144">250 文字を超えないでください。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1144">Doesn't exceed 250 characters.</span></span>
-   <span data-ttu-id="f7b4f-1145">数字とアンダースコア文字を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1145">Can include numbers and underscore characters.</span></span>
-   <span data-ttu-id="f7b4f-1146">句読点やスペースを含めることはできません。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1146">Cannot include punctuation or spaces.</span></span>
-   <span data-ttu-id="f7b4f-1147">テーブルは、拡張データ型、基本列挙型、クラスなどの他のパブリック オブジェクトと同じ名前を持つことはできません。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1147">Tables cannot have the same name as other public objects, such as extended data types, base enums, classes, and so on.</span></span>

### <a name="method-recipclass"></a><span data-ttu-id="f7b4f-1148">メソッド recipClass</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1148">Method recipClass</span></span>

    public int recipClass([int RecipClass])

#### <a name="parameters"></a><span data-ttu-id="f7b4f-1149">パラメーター</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1149">Parameters</span></span>

<span data-ttu-id="f7b4f-1150">RecipClass</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1150">RecipClass</span></span>  

#### <a name="return-value"></a><span data-ttu-id="f7b4f-1151">戻り値</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1151">Return Value</span></span>

### <a name="method-new"></a><span data-ttu-id="f7b4f-1152">メソッド new</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1152">Method new</span></span>

<span data-ttu-id="f7b4f-1153">MapiRecipDesc クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1153">Initializes a new instance of the MapiRecipDesc class.</span></span>

    public void new()

### <a name="method-finalize"></a><span data-ttu-id="f7b4f-1154">メソッド finalize</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1154">Method finalize</span></span>

    public void finalize()

## <a name="class-mapiterator"></a><span data-ttu-id="f7b4f-1155">クラス MapIterator</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1155">Class MapIterator</span></span>
    class MapIterator extends Object

<span data-ttu-id="f7b4f-1156">MapIterator クラスは、マップ内の要素を反復処理するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1156">The MapIterator class is used to iterate over the elements in a map.</span></span>

### <a name="remarks"></a><span data-ttu-id="f7b4f-1157">備考</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1157">Remarks</span></span>

<span data-ttu-id="f7b4f-1158">マップ反復子は、マップ内で要素を反復処理するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1158">Map iterators are used to iterate over the elements in a map.</span></span> <span data-ttu-id="f7b4f-1159">これらは、反復処理する対象となるマップにシンプルなポインターとして表示することができます。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1159">They can be viewed as simple pointers into the maps over which they iterate.</span></span> <span data-ttu-id="f7b4f-1160">繰り返しを開始する機能は利用可能であり、より多くの (キー、値) の組み合わせが利用可能であるかどうかを決定し、繰り返しによりポイントされる要素をフェッチします。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1160">Functionality is available to start the iteration, determine whether more (key, value) pairs are available, and fetch the element that is pointed to by the iterator.</span></span> <span data-ttu-id="f7b4f-1161">MapIterator クラスよりも MapEnumerator クラスを使用することをお勧めします。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1161">It is better to use the MapEnumerator class than the MapIterator class.</span></span> <span data-ttu-id="f7b4f-1162">マップ反復子および反復処理するマップは、同じクライアント/サーバー側にある必要があります。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1162">Map iterators and the maps over which they iterate must be on the same client/server side.</span></span> <span data-ttu-id="f7b4f-1163">MapIterator クラスを使用し、コードが Called from としてマークされている場合、マップと反復子が別の層で終了する可能性があり、コードは失敗します。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1163">If you use the MapIterator class and code is marked as Called from, the map and the iterator could end up on different tiers, and the code will fail.</span></span> <span data-ttu-id="f7b4f-1164">MapEnumerator クラスを使用する場合、列挙子はマップと同じ層に自動的に作成されます。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1164">If you use the MapEnumerator class, the enumerator is automatically created on the same tier as the map.</span></span> <span data-ttu-id="f7b4f-1165">また、MapIterator クラスを使用する場合、より多くおよび次のメソッドを明示的に呼び出して、マップに次の項目を移動する必要があります。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1165">Additionally, if you use the MapIterator class, you must explicitly call the more and next methods to move to the next item in a map.</span></span> <span data-ttu-id="f7b4f-1166">MapEnumerator クラスを使用する場合、moveNext メソッドを呼び出すだけです。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1166">If you use the MapEnumerator class, you only have to call the moveNext method.</span></span> <span data-ttu-id="f7b4f-1167">要素が挿入されるシーケンスは、挿入の順序を決定しません。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1167">The sequence in which the elements are inserted does not determine the order in which they occur.</span></span> <span data-ttu-id="f7b4f-1168">順序は、要素の順序によって定義されます。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1168">The order is defined by the ordering of the elements.</span></span> <span data-ttu-id="f7b4f-1169">上位キーを持つ要素の前に、下位キーを持つ要素が表示されます。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1169">Elements that have lower keys appear before elements that have higher keys.</span></span> <span data-ttu-id="f7b4f-1170">型の通常の順序が使用されます。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1170">The usual ordering for the types is used.</span></span> <span data-ttu-id="f7b4f-1171">ただし、キーがオブジェクトである場合、オブジェクトのアドレスを使用して順序が指定されるため、特定の順序を推測することはできません。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1171">However, if the keys are objects, the addresses of the objects are used to supply the ordering, and therefore no specific ordering can be inferred.</span></span> <span data-ttu-id="f7b4f-1172">オブジェクトのアドレスは、本来、一時的です。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1172">The addresses of the objects are transient by nature.</span></span>

### <a name="examples"></a><span data-ttu-id="f7b4f-1173">例</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1173">Examples</span></span>

<span data-ttu-id="f7b4f-1174">次の例では、マップを作成し、3 つの (キー、値) のペアを追加します。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1174">The following example creates a map and adds three (key, value) pairs.</span></span> <span data-ttu-id="f7b4f-1175">マップを通じて反復処理し、各マップ要素に関する情報を印刷します。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1175">It then iterates through the map and prints information about each map element.</span></span>

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

### <a name="methods"></a><span data-ttu-id="f7b4f-1176">メソッド</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1176">Methods</span></span>

| <span data-ttu-id="f7b4f-1177">方法</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1177">Method</span></span>                             | <span data-ttu-id="f7b4f-1178">説明</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1178">Description</span></span>                                                                                    |
|------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f7b4f-1179">public str definitionString()</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1179">public str definitionString()</span></span>      | <span data-ttu-id="f7b4f-1180">"\[int -&gt; str\] 反復子" など、反復子の型のテキスト表現を取得します。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1180">Retrieves a textual representation of the iterator type, such as "\[int -&gt; str\] iterator".</span></span> |
| <span data-ttu-id="f7b4f-1181">public AnyType domainValue()</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1181">public AnyType domainValue()</span></span>       | <span data-ttu-id="f7b4f-1182">反復子により参照される (キー、値) ペアにおけるキーの値を返します。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1182">Returns the value of the key in the (key, value) pair that is referred to by the iterator.</span></span>     |
| <span data-ttu-id="f7b4f-1183">public boolean find(AnyType value)</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1183">public boolean find(AnyType value)</span></span> | <span data-ttu-id="f7b4f-1184">指定したキー値を検索します。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1184">Searches for the specified key value.</span></span>                                                          |
| <span data-ttu-id="f7b4f-1185">public AnyType key()</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1185">public AnyType key()</span></span>               | <span data-ttu-id="f7b4f-1186">反復子により参照される (キー、値) ペアからキーを返します。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1186">Returns the key from the (key, value) pair that is referred to by the iterator.</span></span>                |
| <span data-ttu-id="f7b4f-1187">public boolean more()</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1187">public boolean more()</span></span>              | <span data-ttu-id="f7b4f-1188">反復子が有効な (キー、値 ) ペアを検出するかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1188">Determines whether the iterator finds a valid (key, value) pair.</span></span>                               |
| <span data-ttu-id="f7b4f-1189">public AnyType rangeValue()</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1189">public AnyType rangeValue()</span></span>        | <span data-ttu-id="f7b4f-1190">反復子により参照される (キー、値) ペアにおける値の値を返します。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1190">Returns the value of the value in the (key, value) pair that is referred to by the iterator.</span></span>   |
| <span data-ttu-id="f7b4f-1191">public str toString()</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1191">public str toString()</span></span>              | <span data-ttu-id="f7b4f-1192">反復子のテキスト表現を取得します。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1192">Retrieves a textual representation of the iterator.</span></span>                                            |
| <span data-ttu-id="f7b4f-1193">public AnyType value()</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1193">public AnyType value()</span></span>             | <span data-ttu-id="f7b4f-1194">反復子により参照される (キー、値) ペアから値を返します。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1194">Returns the value from the (key, value) pair that is referred to by the iterator.</span></span>              |
| <span data-ttu-id="f7b4f-1195">public container valuePair()</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1195">public container valuePair()</span></span>       | <span data-ttu-id="f7b4f-1196">キーと値を保持するコンテナーを取得します。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1196">Retrieves a container that holds the key and the value.</span></span>                                        |
| <span data-ttu-id="f7b4f-1197">public void next()</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1197">public void next()</span></span>                 | <span data-ttu-id="f7b4f-1198">次の (キー、値) ペアに反復子を移動します。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1198">Moves the iterator to the next (key, value) pair.</span></span>                                              |
| <span data-ttu-id="f7b4f-1199">public void new(Map map)</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1199">public void new(Map map)</span></span>           | <span data-ttu-id="f7b4f-1200">マップ内の要素をスキャンできるマップの新しい反復子を作成します。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1200">Creates a new iterator for a map that lets you traverse through the elements in the map.</span></span>       |
| <span data-ttu-id="f7b4f-1201">public void begin()</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1201">public void begin()</span></span>                | <span data-ttu-id="f7b4f-1202">反復子をマップの先頭に移動します。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1202">Moves the iterator to the start of the map.</span></span>                                                    |
| <span data-ttu-id="f7b4f-1203">public void end()</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1203">public void end()</span></span>                  | <span data-ttu-id="f7b4f-1204">マップで最後の要素の後に反復子を移動します。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1204">Moves the iterator past the last element in the map.</span></span>                                           |
| <span data-ttu-id="f7b4f-1205">public void delete()</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1205">public void delete()</span></span>               | <span data-ttu-id="f7b4f-1206">反復子によってポイントされている要素をマップから削除します。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1206">Removes from the map the element that is pointed to by the iterator.</span></span>                           |

### <a name="method-definitionstring"></a><span data-ttu-id="f7b4f-1207">メソッド definitionString</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1207">Method definitionString</span></span>

<span data-ttu-id="f7b4f-1208">"\[int -&gt; str\] 反復子" など、反復子の型のテキスト表現を取得します。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1208">Retrieves a textual representation of the iterator type, such as "\[int -&gt; str\] iterator".</span></span>

    public str definitionString()

#### <a name="return-value"></a><span data-ttu-id="f7b4f-1209">戻り値</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1209">Return Value</span></span>

<span data-ttu-id="f7b4f-1210">反復子を説明する文字列。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1210">A string that describes the iterator.</span></span>

### <a name="method-domainvalue"></a><span data-ttu-id="f7b4f-1211">メソッド domainValue</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1211">Method domainValue</span></span>

<span data-ttu-id="f7b4f-1212">反復子により参照される (キー、値) ペアにおけるキーの値を返します。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1212">Returns the value of the key in the (key, value) pair that is referred to by the iterator.</span></span>

    public AnyType domainValue()

#### <a name="return-value"></a><span data-ttu-id="f7b4f-1213">戻り値</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1213">Return Value</span></span>

<span data-ttu-id="f7b4f-1214">反復子によって現在参照されているマップ要素の最初の項目の値。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1214">The value of the first item in the map element that is currently referred to by the iterator.</span></span>

### <a name="method-find"></a><span data-ttu-id="f7b4f-1215">メソッド find</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1215">Method find</span></span>

<span data-ttu-id="f7b4f-1216">指定したキー値を検索します。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1216">Searches for the specified key value.</span></span>

    public boolean find(AnyType value)

#### <a name="parameters"></a><span data-ttu-id="f7b4f-1217">パラメーター</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1217">Parameters</span></span>

<span data-ttu-id="f7b4f-1218">値</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1218">value</span></span>  
<span data-ttu-id="f7b4f-1219">検索する値。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1219">The value to search for.</span></span>

#### <a name="return-value"></a><span data-ttu-id="f7b4f-1220">戻り値</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1220">Return Value</span></span>

<span data-ttu-id="f7b4f-1221">値が見つかった場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1221">true if the value is found; otherwise, false.</span></span>

#### <a name="remarks"></a><span data-ttu-id="f7b4f-1222">備考</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1222">Remarks</span></span>

<span data-ttu-id="f7b4f-1223">True が返された場合、このメソッドは、反復子を要素に配置します。それ以外の場合、MapIterator.more メソッドは false を返します。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1223">If true is returned, the method positions the iterator at the element; otherwise, the MapIterator.more method returns false.</span></span>

### <a name="method-key"></a><span data-ttu-id="f7b4f-1224">メソッド key</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1224">Method key</span></span>

<span data-ttu-id="f7b4f-1225">反復子により参照される (キー、値) ペアからキーを返します。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1225">Returns the key from the (key, value) pair that is referred to by the iterator.</span></span>

    public AnyType key()

#### <a name="return-value"></a><span data-ttu-id="f7b4f-1226">戻り値</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1226">Return Value</span></span>

<span data-ttu-id="f7b4f-1227">マップ反復子によって示されるマップ エントリのキー値。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1227">The key value of the map entry that is denoted by the iterator.</span></span>

#### <a name="remarks"></a><span data-ttu-id="f7b4f-1228">備考</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1228">Remarks</span></span>

<span data-ttu-id="f7b4f-1229">マップ要素のキー値を取得する前に要素が存在するかどうかをテストするには、SetIterator.more メソッドを使用します。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1229">Use the SetIterator.more method to test whether an element exists before you try to retrieve the key value of the map element.</span></span>

#### <a name="examples"></a><span data-ttu-id="f7b4f-1230">例</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1230">Examples</span></span>

<span data-ttu-id="f7b4f-1231">次の例では、マップを反復処理し、マップ内のすべての要素の説明を返します。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1231">The following example iterates through a map and returns a description of all the elements in the map.</span></span>

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

### <a name="method-more"></a><span data-ttu-id="f7b4f-1232">メソッド more</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1232">Method more</span></span>

<span data-ttu-id="f7b4f-1233">反復子が有効な (キー、値 ) ペアを検出するかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1233">Determines whether the iterator finds a valid (key, value) pair.</span></span>

    public boolean more()

#### <a name="return-value"></a><span data-ttu-id="f7b4f-1234">戻り値</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1234">Return Value</span></span>

<span data-ttu-id="f7b4f-1235">より多くの (キー、値) の組み合わせがマップで使用可能な場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1235">true if more (key, value) pairs are available in the map; otherwise, false.</span></span>

#### <a name="remarks"></a><span data-ttu-id="f7b4f-1236">備考</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1236">Remarks</span></span>

<span data-ttu-id="f7b4f-1237">more メソッドが false を返すときに反復子が指す要素にアクセスしようとするとエラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1237">If you try to access an element that is pointed to by an iterator when the more method returns false, you receive an error.</span></span> <span data-ttu-id="f7b4f-1238">より多くのメソッドは、反復子が有効な要素を指しているかどうかだけをテストします。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1238">The more method only tests whether the iterator points to a valid element.</span></span> <span data-ttu-id="f7b4f-1239">マップにより多くの要素があるかどうかはテストされません。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1239">It does not test whether there are more elements in the map.</span></span>

#### <a name="examples"></a><span data-ttu-id="f7b4f-1240">例</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1240">Examples</span></span>

<span data-ttu-id="f7b4f-1241">次の例では、more メソッドを使用してマップ内の要素がまだ存在するかどうかを調べることによって、マップを反復処理します。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1241">The following example iterates through a map by using the more method to check whether there are still elements in the map.</span></span> <span data-ttu-id="f7b4f-1242">マップ内のすべての要素の説明を返します。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1242">It then returns a description of all the elements in the map.</span></span>

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

### <a name="method-rangevalue"></a><span data-ttu-id="f7b4f-1243">メソッド rangeValue</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1243">Method rangeValue</span></span>

<span data-ttu-id="f7b4f-1244">反復子により参照される (キー、値) ペアにおける値の値を返します。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1244">Returns the value of the value in the (key, value) pair that is referred to by the iterator.</span></span>

    public AnyType rangeValue()

#### <a name="return-value"></a><span data-ttu-id="f7b4f-1245">戻り値</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1245">Return Value</span></span>

<span data-ttu-id="f7b4f-1246">反復子によって現在参照されているマップ要素の 2 番目の項目の値。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1246">The value of the second item in the map element that is currently referred to by the iterator.</span></span>

#### <a name="remarks"></a><span data-ttu-id="f7b4f-1247">備考</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1247">Remarks</span></span>

<span data-ttu-id="f7b4f-1248">rangeValue メソッドは MapIterator.value メソッドと同じ機能を持ちますが、domainValue メソッドに対応するメソッドとして使用できます。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1248">The rangeValue method has the same functionality as the MapIterator.value method, but it is available as a counterpart to the domainValue method.</span></span>

### <a name="method-tostring"></a><span data-ttu-id="f7b4f-1249">メソッド toString</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1249">Method toString</span></span>

<span data-ttu-id="f7b4f-1250">反復子のテキスト表現を取得します。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1250">Retrieves a textual representation of the iterator.</span></span>

    public str toString()

#### <a name="return-value"></a><span data-ttu-id="f7b4f-1251">戻り値</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1251">Return Value</span></span>

<span data-ttu-id="f7b4f-1252">反復子を説明する文字列。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1252">The string that describes the iterator.</span></span>

#### <a name="remarks"></a><span data-ttu-id="f7b4f-1253">備考</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1253">Remarks</span></span>

<span data-ttu-id="f7b4f-1254">反復子がセット内の最初の要素をポイントする場合、文字列にはこの表現が次のフォームで含まれます: "(開始)\[ *値*\]"</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1254">If the iterator points to the first element in the set, the string will contain an indication of this, in the form: "(begin)\[ *value*\]".</span></span> <span data-ttu-id="f7b4f-1255">反復子が要素をポイントしている場合 (つまり、MapIterator.more メソッドが false を返す場合)、返される文字列は「(終了)」になります。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1255">If the iterator does not point to an element (that is, if the MapIterator.more method returns false), the string that is returned is "(end)".</span></span> <span data-ttu-id="f7b4f-1256">反復子が値をポイントしている場合、文字列は "\[*値*\]" で、*値*が要素値の文字列表現です。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1256">If the iterator points to a value, the string is "\[ *value*\]", where *value* is a string representation of the element value.</span></span>

#### <a name="examples"></a><span data-ttu-id="f7b4f-1257">例</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1257">Examples</span></span>

<span data-ttu-id="f7b4f-1258">次の例では、整数またはクラス マップを反復処理し、各マップ要素に関する情報を出力します。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1258">The following example iterates through an integer or class map, and prints information about each map element.</span></span> <span data-ttu-id="f7b4f-1259">MapIterator.toString メソッドを使用して各マップ要素でのクラスのテキスト表現を返します。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1259">It uses the MapIterator.toString method to return a textual representation of the class in each map element.</span></span>

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

### <a name="method-value"></a><span data-ttu-id="f7b4f-1260">メソッド value</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1260">Method value</span></span>

<span data-ttu-id="f7b4f-1261">反復子により参照される (キー、値) ペアから値を返します。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1261">Returns the value from the (key, value) pair that is referred to by the iterator.</span></span>

    public AnyType value()

#### <a name="return-value"></a><span data-ttu-id="f7b4f-1262">戻り値</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1262">Return Value</span></span>

<span data-ttu-id="f7b4f-1263">マップ反復子によって示されるマップ要素からの値。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1263">The value from the map element that is denoted by the map iterator.</span></span>

#### <a name="remarks"></a><span data-ttu-id="f7b4f-1264">備考</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1264">Remarks</span></span>

<span data-ttu-id="f7b4f-1265">マップ要素のキー値を取得する前に要素が存在するかどうかをテストするには、MapIterator.more メソッドを使用します。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1265">Use the MapIterator.more method to test whether an element exists before you try to retrieve the key value of the map element.</span></span>

#### <a name="examples"></a><span data-ttu-id="f7b4f-1266">例</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1266">Examples</span></span>

<span data-ttu-id="f7b4f-1267">次の例では、マップを反復処理し、マップ内のすべての要素のリストを返します。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1267">The following example iterates through a map and returns a list of all the elements in the map.</span></span>

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

### <a name="method-valuepair"></a><span data-ttu-id="f7b4f-1268">メソッド valuePair</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1268">Method valuePair</span></span>

<span data-ttu-id="f7b4f-1269">キーと値を保持するコンテナーを取得します。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1269">Retrieves a container that holds the key and the value.</span></span>

    public container valuePair()

#### <a name="return-value"></a><span data-ttu-id="f7b4f-1270">戻り値</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1270">Return Value</span></span>

<span data-ttu-id="f7b4f-1271">キーと値を保持するコンテナーです。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1271">A container that holds the key and the value.</span></span>

#### <a name="remarks"></a><span data-ttu-id="f7b4f-1272">備考</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1272">Remarks</span></span>

<span data-ttu-id="f7b4f-1273">オブジェクトをコンテナーに配置することはできません。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1273">Objects cannot reside in containers.</span></span> <span data-ttu-id="f7b4f-1274">したがって、キーまたは値のいずれかがオブジェクトである場合、例外が発生します。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1274">Therefore, an exception is raised if either the key or the value is an object.</span></span>

### <a name="method-next"></a><span data-ttu-id="f7b4f-1275">メソッド next</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1275">Method next</span></span>

<span data-ttu-id="f7b4f-1276">次の (キー、値) ペアに反復子を移動します。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1276">Moves the iterator to the next (key, value) pair.</span></span>

    public void next()

#### <a name="remarks"></a><span data-ttu-id="f7b4f-1277">備考</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1277">Remarks</span></span>

<span data-ttu-id="f7b4f-1278">MapIterator.more メソッドを使用すると、マップ内にさらに要素があるかどうか判断することができます。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1278">You can use the MapIterator.more method to determine whether there are any more elements in the map.</span></span>

#### <a name="examples"></a><span data-ttu-id="f7b4f-1279">例</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1279">Examples</span></span>

<span data-ttu-id="f7b4f-1280">次の例では、next メソッドを使用してマップを反復処理し、マップ内のすべての要素のリストを返します。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1280">The following example uses the next method to iterate through a map and returns a list of all the elements in the map.</span></span>

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

### <a name="method-new"></a><span data-ttu-id="f7b4f-1281">メソッド new</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1281">Method new</span></span>

<span data-ttu-id="f7b4f-1282">マップ内の要素をスキャンできるマップの新しい反復子を作成します。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1282">Creates a new iterator for a map that lets you traverse through the elements in the map.</span></span>

    public void new(Map map)

#### <a name="parameters"></a><span data-ttu-id="f7b4f-1283">パラメーター</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1283">Parameters</span></span>

<span data-ttu-id="f7b4f-1284">マップ</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1284">map</span></span>  
<span data-ttu-id="f7b4f-1285">反復子を作成するマップ。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1285">The map for which to create an iterator.</span></span>

#### <a name="remarks"></a><span data-ttu-id="f7b4f-1286">備考</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1286">Remarks</span></span>

<span data-ttu-id="f7b4f-1287">反復子は、マップが空でない場合、マップの最初の値に配置されます。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1287">The iterator is positioned at the first value in the map if the map is not empty.</span></span>

#### <a name="examples"></a><span data-ttu-id="f7b4f-1288">例</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1288">Examples</span></span>

<span data-ttu-id="f7b4f-1289">次の例では、(整数、クラス) のペアのマップを作成し、マップを移動する反復子を作成します。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1289">The following example creates a map of (integer, class) pairs and then creates an iterator to traverse the map.</span></span>

    Map iim = new Map(Types::Integer, Types::Class); 
    MapIterator it; 
    it = new MapIterator (iim);

### <a name="method-begin"></a><span data-ttu-id="f7b4f-1290">メソッド begin</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1290">Method begin</span></span>

<span data-ttu-id="f7b4f-1291">反復子をマップの先頭に移動します。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1291">Moves the iterator to the start of the map.</span></span>

    public void begin()

#### <a name="remarks"></a><span data-ttu-id="f7b4f-1292">備考</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1292">Remarks</span></span>

<span data-ttu-id="f7b4f-1293">新しく作成されるマップ反復子は、マップの最初の要素に配置されるため、セットを通じて反復する前に開始メソッドを呼び出す必要はありません。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1293">Newly created map iterators are positioned at the first element in the map, so you do not have to call the begin method before you iterate through the set.</span></span> <span data-ttu-id="f7b4f-1294">ポインターをリセットする場合は、開始メソッドを呼び出す必要があります。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1294">You must call the begin method if you want to reset the pointer.</span></span>

### <a name="method-end"></a><span data-ttu-id="f7b4f-1295">メソッド end</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1295">Method end</span></span>

<span data-ttu-id="f7b4f-1296">マップで最後の要素の後に反復子を移動します。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1296">Moves the iterator past the last element in the map.</span></span>

    public void end()

#### <a name="remarks"></a><span data-ttu-id="f7b4f-1297">備考</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1297">Remarks</span></span>

<span data-ttu-id="f7b4f-1298">このメソッドを実行すると、MapIterator.more メソッドが false に戻ります。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1298">After this method runs, the MapIterator.more method will return false.</span></span>

### <a name="method-delete"></a><span data-ttu-id="f7b4f-1299">メソッド delete</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1299">Method delete</span></span>

<span data-ttu-id="f7b4f-1300">反復子によってポイントされている要素をマップから削除します。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1300">Removes from the map the element that is pointed to by the iterator.</span></span>

    public void delete()

#### <a name="remarks"></a><span data-ttu-id="f7b4f-1301">備考</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1301">Remarks</span></span>

<span data-ttu-id="f7b4f-1302">反復子は、delete メソッドが呼び出された後に次の要素を指します。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1302">The iterator points to the next element after the delete method is invoked.</span></span>

## <a name="class-memberfunction"></a><span data-ttu-id="f7b4f-1303">クラス MemberFunction</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1303">Class MemberFunction</span></span>
    class MemberFunction extends TreeNode

<span data-ttu-id="f7b4f-1304">MemberFunction クラスは、フォーム、レポート、クラスなどの Finance and Operations アプリケーション オブジェクト ツリー (AOT) で指定されたノードに関する情報を提供します。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1304">The MemberFunction class provides information about a specified node in the Finance and Operations Application Object Tree (AOT), such as a form, report, or class.</span></span>

### <a name="remarks"></a><span data-ttu-id="f7b4f-1305">備考</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1305">Remarks</span></span>

<span data-ttu-id="f7b4f-1306">このクラスでは、作成、読み取り、更新、および X++ コードとメタデータを削除できます。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1306">This class lets you create, read, update, and delete X++ code and metadata.</span></span> <span data-ttu-id="f7b4f-1307">この API が呼び出される前に、ユーザーが開発セキュリティ キー (SysDevelopment) にアクセスできることを確認します。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1307">Make sure that the user has access to the development security key (SysDevelopment) before this API is called.</span></span> <span data-ttu-id="f7b4f-1308">::findNode メソッドを使用すると MemberFunction クラスのインスタンスにノードを割り当てることができます。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1308">You can use the ::findNode method to assign a node to an instance of the MemberFunction class.</span></span>

### <a name="examples"></a><span data-ttu-id="f7b4f-1309">例</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1309">Examples</span></span>

<span data-ttu-id="f7b4f-1310">次の例では、TreeNode::findNode メソッドを使用して、AddressSelectForm.callerDataSource メソッドのノードを MemberFunction クラスのインスタンスに割り当てます。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1310">The following example uses the TreeNode::findNode method to assign the node for the AddressSelectForm.callerDataSource method to an instance of the MemberFunction class.</span></span> <span data-ttu-id="f7b4f-1311">MemberFunction.AOTgetSource メソッドは、メソッドのソース コードを返します。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1311">The MemberFunction.AOTgetSource Method method returns the method source code.</span></span>

    void getMemberFunction() 
    { 
        MemberFunction memberFunction; 
        str name; 
        boolean isStatic; 
        str source; 
        try 
        { 
            memberFunction = TreeNode::findNode( 
               '\\Classes\\AddressSelectForm\\callerDataSource'); 
            if(!memberFunction) 
            { 
                throw exception::Error; 
            } 
            source = memberFunction.AOTgetSource(); 
            print source; 
            pause; 
        } 
        catch (exception::Error) 
        { 
            print "The specified node does not exist."; 
            pause; 
            } 
        } 
    }

### <a name="methods"></a><span data-ttu-id="f7b4f-1312">メソッド</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1312">Methods</span></span>

| <span data-ttu-id="f7b4f-1313">方法</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1313">Method</span></span>                                                     | <span data-ttu-id="f7b4f-1314">説明</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1314">Description</span></span>                                                                                                                             |
|------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f7b4f-1315">public str AOTgetSource()</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1315">public str AOTgetSource()</span></span>                                  | <span data-ttu-id="f7b4f-1316">クラスやメソッドなど、AOT 内で指定したノードのソース コードを提供します。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1316">Provides the source code for a specified node in the AOT, such as a class or method.</span></span>                                                    |
| <span data-ttu-id="f7b4f-1317">public boolean canAddEventHandler()</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1317">public boolean canAddEventHandler()</span></span>                        |                                                                                                                                         |
| <span data-ttu-id="f7b4f-1318">public boolean isEvent()</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1318">public boolean isEvent()</span></span>                                   |                                                                                                                                         |
| <span data-ttu-id="f7b4f-1319">public boolean isStatic()</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1319">public boolean isStatic()</span></span>                                  | <span data-ttu-id="f7b4f-1320">メソッドが静的かどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1320">Indicates whether a method is static.</span></span>                                                                                                   |
| <span data-ttu-id="f7b4f-1321">public str name(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1321">public str name(\[str value\])</span></span>                             | <span data-ttu-id="f7b4f-1322">フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1322">Gets or sets the name that is used in code to identify a form, report, table, query, or other Finance and Operations application object.</span></span> |
| <span data-ttu-id="f7b4f-1323">public void AOTedit(\[int Line\], \[int Column\])</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1323">public void AOTedit(\[int Line\], \[int Column\])</span></span>          | <span data-ttu-id="f7b4f-1324">AOT で指定したノードの適切なエディタを開きます。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1324">Opens the appropriate editor for a specified node in the AOT.</span></span>                                                                           |
| <span data-ttu-id="f7b4f-1325">public void new()</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1325">public void new()</span></span>                                          | <span data-ttu-id="f7b4f-1326">MemberFunction クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1326">Initializes a new instance of the MemberFunction class.</span></span>                                                                                 |
| <span data-ttu-id="f7b4f-1327">public void AOTsetSource(str source, \[boolean isStatic\])</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1327">public void AOTsetSource(str source, \[boolean isStatic\])</span></span> | <span data-ttu-id="f7b4f-1328">クラスやメソッドなど、AOT 内で指定したノードのソース コードを設定します。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1328">Sets the source code for a specified node in the AOT, such as a class or method.</span></span>                                                        |

### <a name="method-aotgetsource"></a><span data-ttu-id="f7b4f-1329">メソッド AOTgetSource</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1329">Method AOTgetSource</span></span>

<span data-ttu-id="f7b4f-1330">クラスやメソッドなど、AOT 内で指定したノードのソース コードを提供します。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1330">Provides the source code for a specified node in the AOT, such as a class or method.</span></span>

    public str AOTgetSource()

#### <a name="return-value"></a><span data-ttu-id="f7b4f-1331">戻り値</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1331">Return Value</span></span>

<span data-ttu-id="f7b4f-1332">ソース コードの文字列値、ノードにソース コードが含まれていない場合、nullNothingnullptrunita null 参照 (Visual Basic にはなし)。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1332">A string value for the source code; nullNothingnullptrunita null reference (Nothing in Visual Basic) if the node does not contain source code.</span></span>

### <a name="method-canaddeventhandler"></a><span data-ttu-id="f7b4f-1333">メソッド canAddEventHandler</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1333">Method canAddEventHandler</span></span>

    public boolean canAddEventHandler()

#### <a name="return-value"></a><span data-ttu-id="f7b4f-1334">戻り値</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1334">Return Value</span></span>

### <a name="method-isevent"></a><span data-ttu-id="f7b4f-1335">メソッド isEvent</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1335">Method isEvent</span></span>

    public boolean isEvent()

#### <a name="return-value"></a><span data-ttu-id="f7b4f-1336">戻り値</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1336">Return Value</span></span>

### <a name="method-isstatic"></a><span data-ttu-id="f7b4f-1337">メソッド isStatic</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1337">Method isStatic</span></span>

<span data-ttu-id="f7b4f-1338">メソッドが静的かどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1338">Indicates whether a method is static.</span></span>

    public boolean isStatic()

#### <a name="return-value"></a><span data-ttu-id="f7b4f-1339">戻り値</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1339">Return Value</span></span>

<span data-ttu-id="f7b4f-1340">メソッドが静的である場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1340">true if the method is static; otherwise, false.</span></span>

#### <a name="remarks"></a><span data-ttu-id="f7b4f-1341">備考</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1341">Remarks</span></span>

<span data-ttu-id="f7b4f-1342">このメソッドは、AOT の指定されたノード (フォーム、レポート、クラスなど) に関連付けられます。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1342">This method is associated with a specified node in the AOT, such as a form, report, or class.</span></span> <span data-ttu-id="f7b4f-1343">このメソッドは、主に MemberFunction :: AOTsetSource メソッドと組み合わせて使用されます。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1343">This method is used primarily in conjunction with the MemberFunction::AOTsetSource method.</span></span>

### <a name="method-name"></a><span data-ttu-id="f7b4f-1344">メソッド名</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1344">Method name</span></span>

<span data-ttu-id="f7b4f-1345">フォーム、レポート、テーブル、クエリ、または他のアプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1345">Gets or sets the name that is used in code to identify a form, report, table, query, or other Finance and Operations application object.</span></span>

    public str name([str value])

#### <a name="parameters"></a><span data-ttu-id="f7b4f-1346">パラメーター</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1346">Parameters</span></span>

<span data-ttu-id="f7b4f-1347">値</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1347">value</span></span>  
<span data-ttu-id="f7b4f-1348">ノードを指定する文字列、オプション。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1348">A string that specifies a node; optional.</span></span>

#### <a name="return-value"></a><span data-ttu-id="f7b4f-1349">戻り値</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1349">Return Value</span></span>

<span data-ttu-id="f7b4f-1350">アプリケーション オブジェクトを識別するためにコードで使用される名前。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1350">The name that is used in code to identify an application object.</span></span>

#### <a name="remarks"></a><span data-ttu-id="f7b4f-1351">備考</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1351">Remarks</span></span>

<span data-ttu-id="f7b4f-1352">オブジェクトの名前プロパティ値は、コードの競合を避けるために、次の基準を満たしている必要があります。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1352">The name property value of an object must meet the following criteria to avoid code conflicts:</span></span>

-   <span data-ttu-id="f7b4f-1353">文字で始めます。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1353">It starts with a letter.</span></span>
-   <span data-ttu-id="f7b4f-1354">250 文字を超えていません。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1354">It doesn't exceed 250 characters.</span></span>
-   <span data-ttu-id="f7b4f-1355">数字とアンダースコア (\_) 文字を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1355">It can include numbers and underscore (\_) characters.</span></span>
-   <span data-ttu-id="f7b4f-1356">句読点やスペースを含めることはできません。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1356">It cannot include punctuation or spaces.</span></span>
-   <span data-ttu-id="f7b4f-1357">テーブルは、拡張データ型、基本列挙型、およびクラスなどの他のパブリック オブジェクトと同じ名前を持つことはできません。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1357">Tables cannot have the same name as other public objects, such as extended data types, base enums, and classes.</span></span>

### <a name="method-aotedit"></a><span data-ttu-id="f7b4f-1358">メソッド AOTedit</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1358">Method AOTedit</span></span>

<span data-ttu-id="f7b4f-1359">AOT で指定したノードの適切なエディタを開きます。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1359">Opens the appropriate editor for a specified node in the AOT.</span></span>

    public void AOTedit([int Line], [int Column])

#### <a name="parameters"></a><span data-ttu-id="f7b4f-1360">パラメーター</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1360">Parameters</span></span>

<span data-ttu-id="f7b4f-1361">明細行</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1361">Line</span></span>  
<span data-ttu-id="f7b4f-1362">カーソルの列の位置を指定する整数。オプション。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1362">An integer that specifies the column position for the cursor; optional.</span></span>

<!-- -->

<span data-ttu-id="f7b4f-1363">円柱</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1363">Column</span></span>  
<span data-ttu-id="f7b4f-1364">カーソルの列の位置を指定する整数。オプション。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1364">An integer that specifies the column position for the cursor; optional.</span></span>

### <a name="method-new"></a><span data-ttu-id="f7b4f-1365">メソッド new</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1365">Method new</span></span>

<span data-ttu-id="f7b4f-1366">MemberFunction クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1366">Initializes a new instance of the MemberFunction class.</span></span>

    public void new()

### <a name="method-aotsetsource"></a><span data-ttu-id="f7b4f-1367">メソッド AOTsetSource</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1367">Method AOTsetSource</span></span>

<span data-ttu-id="f7b4f-1368">クラスやメソッドなど、AOT 内で指定したノードのソース コードを設定します。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1368">Sets the source code for a specified node in the AOT, such as a class or method.</span></span>

    public void AOTsetSource(str source, [boolean isStatic])

#### <a name="parameters"></a><span data-ttu-id="f7b4f-1369">パラメーター</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1369">Parameters</span></span>

<span data-ttu-id="f7b4f-1370">ソース</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1370">source</span></span>  
<span data-ttu-id="f7b4f-1371">ブール値: 静的メソッドの場合は true、インスタンス メソッドの場合は false; オプション。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1371">A Boolean value: true for a static method or false for an instance method; optional.</span></span>

<!-- -->

<span data-ttu-id="f7b4f-1372">isStatic</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1372">isStatic</span></span>  
<span data-ttu-id="f7b4f-1373">ブール値: 静的メソッドの場合は true、インスタンス メソッドの場合は false; オプション。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1373">A Boolean value: true for a static method or false for an instance method; optional.</span></span>

## <a name="class-menu"></a><span data-ttu-id="f7b4f-1374">クラス メニュー</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1374">Class Menu</span></span>
    class Menu extends TreeNode

<span data-ttu-id="f7b4f-1375">メニュー システム クラスを使用すると、Finance and OperationsMenu オブジェクトのいずれかをコードから構成および実行できます。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1375">The Menu system class lets you configure and run any of the Finance and OperationsMenu objects from code.</span></span>

### <a name="remarks"></a><span data-ttu-id="f7b4f-1376">備考</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1376">Remarks</span></span>

<span data-ttu-id="f7b4f-1377">TreeNode システム クラスは、Finance and Operations アプリケーション オブジェクト ツリー (AOT) で、メニューへのより一般的なアプローチとして機能します。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1377">The TreeNode system class serves as a more general approach to the menus in the Finance and Operations Application Object Tree (AOT).</span></span> <span data-ttu-id="f7b4f-1378">サブメニューやメニュー項目などのメニュー内容を作成または操作するには、Menu クラスを使用します。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1378">You use the Menu class to create or manipulate the menus contents, such as submenus and menu items.</span></span> <span data-ttu-id="f7b4f-1379">このクラスでは、作成、読み取り、更新、および X++ コードとメタデータを削除できます。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1379">This class lets you create, read, update, and delete X++ code and metadata.</span></span> <span data-ttu-id="f7b4f-1380">この API が呼び出される前に、ユーザーが開発セキュリティ キー (SysDevelopment) にアクセスできることを確認します。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1380">Make sure that the user has access to the development security key (SysDevelopment) before this API is called.</span></span>

### <a name="examples"></a><span data-ttu-id="f7b4f-1381">例</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1381">Examples</span></span>

### <a name="methods"></a><span data-ttu-id="f7b4f-1382">メソッド</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1382">Methods</span></span>

| <span data-ttu-id="f7b4f-1383">方法</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1383">Method</span></span>                                                                   | <span data-ttu-id="f7b4f-1384">説明</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1384">Description</span></span>                                                                                                               |
|--------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f7b4f-1385">public str changedBy(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1385">public str changedBy(\[str value\])</span></span>                                      | <span data-ttu-id="f7b4f-1386">アプリケーション オブジェクトを最後に変更したユーザーの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1386">Gets or sets the name of the user who last changed the application object.</span></span>                                                |
| <span data-ttu-id="f7b4f-1387">public Date changedDate(\[Date value\])</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1387">public Date changedDate(\[Date value\])</span></span>                                  | <span data-ttu-id="f7b4f-1388">アプリケーション オブジェクトが最後に変更された日付を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1388">Gets or sets the date an application object was last changed.</span></span>                                                             |
| <span data-ttu-id="f7b4f-1389">public str changedTime(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1389">public str changedTime(\[str value\])</span></span>                                    | <span data-ttu-id="f7b4f-1390">アプリケーション オブジェクトが最後に変更された時刻を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1390">Gets or sets the time an application object was last changed.</span></span>                                                             |
| <span data-ttu-id="f7b4f-1391">public ConfigurationKeyId configurationKey(\[ConfigurationKeyId value\])</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1391">public ConfigurationKeyId configurationKey(\[ConfigurationKeyId value\])</span></span> | <span data-ttu-id="f7b4f-1392">コントロールに割り当てられるコンフィギュレーション キーを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1392">Gets or sets the configuration key that is assigned to the control.</span></span>                                                       |
| <span data-ttu-id="f7b4f-1393">public str countryRegionCodes(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1393">public str countryRegionCodes(\[str value\])</span></span>                             |                                                                                                                           |
| <span data-ttu-id="f7b4f-1394">public str createdBy(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1394">public str createdBy(\[str value\])</span></span>                                      | <span data-ttu-id="f7b4f-1395">アプリケーション オブジェクトを作成したユーザーの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1395">Gets or sets the name of the user who created the application object.</span></span>                                                     |
| <span data-ttu-id="f7b4f-1396">public Date creationDate(\[Date value\])</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1396">public Date creationDate(\[Date value\])</span></span>                                 | <span data-ttu-id="f7b4f-1397">アプリケーション オブジェクトが作成された日付を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1397">Gets or sets the date an application object was created.</span></span>                                                                  |
| <span data-ttu-id="f7b4f-1398">public str creationTime(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1398">public str creationTime(\[str value\])</span></span>                                   |                                                                                                                           |
| <span data-ttu-id="f7b4f-1399">public str disabledImage(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1399">public str disabledImage(\[str value\])</span></span>                                  | <span data-ttu-id="f7b4f-1400">コントロールの無効な画像を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1400">Gets or sets the disabled image of the button.</span></span>                                                                            |
| <span data-ttu-id="f7b4f-1401">public int disabledImageLocation(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1401">public int disabledImageLocation(\[int value\])</span></span>                          |                                                                                                                           |
| <span data-ttu-id="f7b4f-1402">public int disabledResource(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1402">public int disabledResource(\[int value\])</span></span>                               | <span data-ttu-id="f7b4f-1403">無効なボタン画像として使用する画像リソース ID を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1403">Gets or sets the resource ID of the image to use as the disabled button image.</span></span>                                            |
| <span data-ttu-id="f7b4f-1404">public int imageLocation(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1404">public int imageLocation(\[int value\])</span></span>                                  |                                                                                                                           |
| <span data-ttu-id="f7b4f-1405">public str label(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1405">public str label(\[str value\])</span></span>                                          | <span data-ttu-id="f7b4f-1406">コントロールのラベルを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1406">Gets or sets the label for a control.</span></span>                                                                                     |
| <span data-ttu-id="f7b4f-1407">public str menuFunctionName(\[str name\])</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1407">public str menuFunctionName(\[str name\])</span></span>                                |                                                                                                                           |
| <span data-ttu-id="f7b4f-1408">public str menuItemName(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1408">public str menuItemName(\[str value\])</span></span>                                   |                                                                                                                           |
| <span data-ttu-id="f7b4f-1409">public MenuItemType menuItemType(\[MenuItemType value\])</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1409">public MenuItemType menuItemType(\[MenuItemType value\])</span></span>                 |                                                                                                                           |
| <span data-ttu-id="f7b4f-1410">public str menuName()</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1410">public str menuName()</span></span>                                                    |                                                                                                                           |
| <span data-ttu-id="f7b4f-1411">public str name(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1411">public str name(\[str value\])</span></span>                                           | <span data-ttu-id="f7b4f-1412">フォーム、レポート、テーブル、クエリ、または別の MSDAX アプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1412">Gets or sets the name that is used in code to identify a form, report, table, query, or another MSDAX application object.</span></span> |
| <span data-ttu-id="f7b4f-1413">public int neededAccessLevel(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1413">public int neededAccessLevel(\[int value\])</span></span>                              | <span data-ttu-id="f7b4f-1414">MenuFunction クラスの neededAccessLevel プロパティを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1414">Gets or sets the neededAccessLevel property for the MenuFunction class.</span></span>                                                   |
| <span data-ttu-id="f7b4f-1415">public str normalImage(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1415">public str normalImage(\[str value\])</span></span>                                    |                                                                                                                           |
| <span data-ttu-id="f7b4f-1416">public int normalResource(\[int value\])</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1416">public int normalResource(\[int value\])</span></span>                                 |                                                                                                                           |
| <span data-ttu-id="f7b4f-1417">public Guid origin(\[Guid value\])</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1417">public Guid origin(\[Guid value\])</span></span>                                       |                                                                                                                           |
| <span data-ttu-id="f7b4f-1418">public str parameter(\[str parameter\])</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1418">public str parameter(\[str parameter\])</span></span>                                  |                                                                                                                           |
| <span data-ttu-id="f7b4f-1419">public str parameters(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1419">public str parameters(\[str value\])</span></span>                                     | <span data-ttu-id="f7b4f-1420">MenuFunction クラスで実行されるオブジェクトに渡されるパラメータの一覧を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1420">Gets or sets the list of parameters that are passed to objects that are run by the MenuFunction class.</span></span>                    |
| <span data-ttu-id="f7b4f-1421">public SecurityKeyId securityKey(\[SecurityKeyId value\])</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1421">public SecurityKeyId securityKey(\[SecurityKeyId value\])</span></span>                |                                                                                                                           |
| <span data-ttu-id="f7b4f-1422">public boolean setCompany(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1422">public boolean setCompany(\[boolean value\])</span></span>                             |                                                                                                                           |
| <span data-ttu-id="f7b4f-1423">public str shortCut(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1423">public str shortCut(\[str value\])</span></span>                                       |                                                                                                                           |
| <span data-ttu-id="f7b4f-1424">public boolean showParentModule(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1424">public boolean showParentModule(\[boolean value\])</span></span>                       |                                                                                                                           |
| <span data-ttu-id="f7b4f-1425">public boolean visible(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1425">public boolean visible(\[boolean value\])</span></span>                                |                                                                                                                           |
| <span data-ttu-id="f7b4f-1426">public str webTarget(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1426">public str webTarget(\[str value\])</span></span>                                      |                                                                                                                           |
| <span data-ttu-id="f7b4f-1427">public void save()</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1427">public void save()</span></span>                                                       |                                                                                                                           |
| <span data-ttu-id="f7b4f-1428">public void new(str Name)</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1428">public void new(str Name)</span></span>                                                | <span data-ttu-id="f7b4f-1429">TreeNode クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1429">Initializes a new instance of the TreeNode class.</span></span>                                                                         |
| <span data-ttu-id="f7b4f-1430">public void makeWebMenu(Object outputClass)</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1430">public void makeWebMenu(Object outputClass)</span></span>                              |                                                                                                                           |
| <span data-ttu-id="f7b4f-1431">public void addMenuitem(xMenuFunction menuFunction)</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1431">public void addMenuitem(xMenuFunction menuFunction)</span></span>                      | <span data-ttu-id="f7b4f-1432">メニューにメニュー項目を追加します。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1432">Adds a menu item to the menu.</span></span>                                                                                             |
| <span data-ttu-id="f7b4f-1433">public void setTreeNodeName(str name)</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1433">public void setTreeNodeName(str name)</span></span>                                    |                                                                                                                           |
| <span data-ttu-id="f7b4f-1434">public void addMenuReference(Menu menu)</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1434">public void addMenuReference(Menu menu)</span></span>                                  |                                                                                                                           |
| <span data-ttu-id="f7b4f-1435">public void addSubmenu(str name)</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1435">public void addSubmenu(str name)</span></span>                                         | <span data-ttu-id="f7b4f-1436">メニューにサブメニューを追加します。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1436">Adds a submenu to the menu.</span></span>                                                                                               |
| <span data-ttu-id="f7b4f-1437">public void addSeparator()</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1437">public void addSeparator()</span></span>                                               | <span data-ttu-id="f7b4f-1438">メニューにメニューの区切りを追加します。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1438">Adds a menu separator to the menu.</span></span>                                                                                        |

### <a name="method-changedby"></a><span data-ttu-id="f7b4f-1439">メソッド changedBy</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1439">Method changedBy</span></span>

<span data-ttu-id="f7b4f-1440">アプリケーション オブジェクトを最後に変更したユーザーの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1440">Gets or sets the name of the user who last changed the application object.</span></span>

    public str changedBy([str value])

#### <a name="parameters"></a><span data-ttu-id="f7b4f-1441">パラメーター</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1441">Parameters</span></span>

<span data-ttu-id="f7b4f-1442">値</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1442">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="f7b4f-1443">戻り値</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1443">Return Value</span></span>

<span data-ttu-id="f7b4f-1444">ユーザーの名前。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1444">The name of the user.</span></span>

### <a name="method-changeddate"></a><span data-ttu-id="f7b4f-1445">メソッド changedDate</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1445">Method changedDate</span></span>

<span data-ttu-id="f7b4f-1446">アプリケーション オブジェクトが最後に変更された日付を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1446">Gets or sets the date an application object was last changed.</span></span>

    public Date changedDate([Date value])

#### <a name="parameters"></a><span data-ttu-id="f7b4f-1447">パラメーター</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1447">Parameters</span></span>

<span data-ttu-id="f7b4f-1448">値</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1448">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="f7b4f-1449">戻り値</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1449">Return Value</span></span>

<span data-ttu-id="f7b4f-1450">アプリケーション オブジェクトが最後に変更された日付。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1450">The date an application object was last changed.</span></span>

### <a name="method-changedtime"></a><span data-ttu-id="f7b4f-1451">メソッド changedTime</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1451">Method changedTime</span></span>

<span data-ttu-id="f7b4f-1452">アプリケーション オブジェクトが最後に変更された時刻を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1452">Gets or sets the time an application object was last changed.</span></span>

    public str changedTime([str value])

#### <a name="parameters"></a><span data-ttu-id="f7b4f-1453">パラメーター</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1453">Parameters</span></span>

<span data-ttu-id="f7b4f-1454">値</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1454">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="f7b4f-1455">戻り値</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1455">Return Value</span></span>

<span data-ttu-id="f7b4f-1456">アプリケーション オブジェクトが最後に変更された時間。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1456">The time an application object was last changed.</span></span>

### <a name="method-configurationkey"></a><span data-ttu-id="f7b4f-1457">メソッド configurationKey</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1457">Method configurationKey</span></span>

<span data-ttu-id="f7b4f-1458">コントロールに割り当てられるコンフィギュレーション キーを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1458">Gets or sets the configuration key that is assigned to the control.</span></span>

    public ConfigurationKeyId configurationKey([ConfigurationKeyId value])

#### <a name="parameters"></a><span data-ttu-id="f7b4f-1459">パラメーター</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1459">Parameters</span></span>

<span data-ttu-id="f7b4f-1460">値</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1460">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="f7b4f-1461">戻り値</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1461">Return Value</span></span>

<span data-ttu-id="f7b4f-1462">コントロールに割り当てられるコンフィギュレーションの ID。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1462">The identifier of the configuration key that is assigned to the control.</span></span>

#### <a name="remarks"></a><span data-ttu-id="f7b4f-1463">備考</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1463">Remarks</span></span>

<span data-ttu-id="f7b4f-1464">コンフィギュレーション キーは、このコントロールを表示するかどうかを決定するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1464">The configuration key is used to determine whether this control can be displayed.</span></span> <span data-ttu-id="f7b4f-1465">コンフィギュレーション キーがシステムで無効な場合、コントロールはフォームで表示されません。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1465">If the configuration key is disabled in the system, the control is not displayed in the form.</span></span>

### <a name="method-countryregioncodes"></a><span data-ttu-id="f7b4f-1466">メソッド countryRegionCodes</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1466">Method countryRegionCodes</span></span>

    public str countryRegionCodes([str value])

#### <a name="parameters"></a><span data-ttu-id="f7b4f-1467">パラメーター</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1467">Parameters</span></span>

<span data-ttu-id="f7b4f-1468">値</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1468">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="f7b4f-1469">戻り値</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1469">Return Value</span></span>

### <a name="method-createdby"></a><span data-ttu-id="f7b4f-1470">メソッド createdBy</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1470">Method createdBy</span></span>

<span data-ttu-id="f7b4f-1471">アプリケーション オブジェクトを作成したユーザーの名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1471">Gets or sets the name of the user who created the application object.</span></span>

    public str createdBy([str value])

#### <a name="parameters"></a><span data-ttu-id="f7b4f-1472">パラメーター</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1472">Parameters</span></span>

<span data-ttu-id="f7b4f-1473">値</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1473">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="f7b4f-1474">戻り値</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1474">Return Value</span></span>

<span data-ttu-id="f7b4f-1475">ユーザーの名前。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1475">The name of the user.</span></span>

### <a name="method-creationdate"></a><span data-ttu-id="f7b4f-1476">メソッド creationDate</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1476">Method creationDate</span></span>

<span data-ttu-id="f7b4f-1477">アプリケーション オブジェクトが作成された日付を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1477">Gets or sets the date an application object was created.</span></span>

    public Date creationDate([Date value])

#### <a name="parameters"></a><span data-ttu-id="f7b4f-1478">パラメーター</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1478">Parameters</span></span>

<span data-ttu-id="f7b4f-1479">値</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1479">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="f7b4f-1480">戻り値</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1480">Return Value</span></span>

<span data-ttu-id="f7b4f-1481">アプリケーション オブジェクトが作成された日付。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1481">The date an application object was created.</span></span>

### <a name="method-creationtime"></a><span data-ttu-id="f7b4f-1482">メソッド creationTime</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1482">Method creationTime</span></span>

    public str creationTime([str value])

#### <a name="parameters"></a><span data-ttu-id="f7b4f-1483">パラメーター</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1483">Parameters</span></span>

<span data-ttu-id="f7b4f-1484">値</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1484">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="f7b4f-1485">戻り値</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1485">Return Value</span></span>

### <a name="method-disabledimage"></a><span data-ttu-id="f7b4f-1486">メソッド disabledImage</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1486">Method disabledImage</span></span>

<span data-ttu-id="f7b4f-1487">コントロールの無効な画像を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1487">Gets or sets the disabled image of the button.</span></span>

    public str disabledImage([str value])

#### <a name="parameters"></a><span data-ttu-id="f7b4f-1488">パラメーター</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1488">Parameters</span></span>

<span data-ttu-id="f7b4f-1489">値</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1489">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="f7b4f-1490">戻り値</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1490">Return Value</span></span>

<span data-ttu-id="f7b4f-1491">画像ファイルのフル ネーム。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1491">The full name of an image file.</span></span> <span data-ttu-id="f7b4f-1492">システムは、GDI でサポートされているすべてのイメージ形式をサポートしています。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1492">The system supports all of the GDI-supported image formats.</span></span>

#### <a name="remarks"></a><span data-ttu-id="f7b4f-1493">備考</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1493">Remarks</span></span>

<span data-ttu-id="f7b4f-1494">このプロパティは、disabledResource プロパティに優先します。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1494">This property has precedence over the disabledResource property .</span></span> <span data-ttu-id="f7b4f-1495">これらのプロパティの両方が設定されている場合に使用されます。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1495">It is used if both of these properties are set.</span></span>

### <a name="method-disabledimagelocation"></a><span data-ttu-id="f7b4f-1496">メソッド disabledImageLocation</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1496">Method disabledImageLocation</span></span>

    public int disabledImageLocation([int value])

#### <a name="parameters"></a><span data-ttu-id="f7b4f-1497">パラメーター</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1497">Parameters</span></span>

<span data-ttu-id="f7b4f-1498">値</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1498">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="f7b4f-1499">戻り値</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1499">Return Value</span></span>

### <a name="method-disabledresource"></a><span data-ttu-id="f7b4f-1500">メソッド disabledResource</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1500">Method disabledResource</span></span>

<span data-ttu-id="f7b4f-1501">無効なボタン画像として使用する画像リソース ID を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1501">Gets or sets the resource ID of the image to use as the disabled button image.</span></span>

    public int disabledResource([int value])

#### <a name="parameters"></a><span data-ttu-id="f7b4f-1502">パラメーター</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1502">Parameters</span></span>

<span data-ttu-id="f7b4f-1503">値</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1503">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="f7b4f-1504">戻り値</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1504">Return Value</span></span>

<span data-ttu-id="f7b4f-1505">無効なボタン画像として使用する画像リソース ID。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1505">The resource ID of the image to use as the disabled button image.</span></span> <span data-ttu-id="f7b4f-1506">アイコンとビットマップ イメージの両方がサポートされます。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1506">Both icon and bitmap images are supported.</span></span>

### <a name="method-imagelocation"></a><span data-ttu-id="f7b4f-1507">メソッド imageLocation</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1507">Method imageLocation</span></span>

    public int imageLocation([int value])

#### <a name="parameters"></a><span data-ttu-id="f7b4f-1508">パラメーター</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1508">Parameters</span></span>

<span data-ttu-id="f7b4f-1509">値</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1509">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="f7b4f-1510">戻り値</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1510">Return Value</span></span>

### <a name="method-label"></a><span data-ttu-id="f7b4f-1511">メソッド label</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1511">Method label</span></span>

<span data-ttu-id="f7b4f-1512">コントロールのラベルを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1512">Gets or sets the label for a control.</span></span>

    public str label([str value])

#### <a name="parameters"></a><span data-ttu-id="f7b4f-1513">パラメーター</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1513">Parameters</span></span>

<span data-ttu-id="f7b4f-1514">値</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1514">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="f7b4f-1515">戻り値</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1515">Return Value</span></span>

<span data-ttu-id="f7b4f-1516">ラベル文字列の現在の値。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1516">The current value of the label string.</span></span>

#### <a name="remarks"></a><span data-ttu-id="f7b4f-1517">備考</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1517">Remarks</span></span>

<span data-ttu-id="f7b4f-1518">ラベルは、コントロール内に表示されているテキストまたはそれに隣接するテキストを指定します。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1518">The label determines which text is displayed in the control or adjacent to it.</span></span> <span data-ttu-id="f7b4f-1519">ラベルのプロパティ値は 250 文字を超えることはできません。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1519">The label property value cannot exceed 250 characters.</span></span>

### <a name="method-menufunctionname"></a><span data-ttu-id="f7b4f-1520">メソッド menuFunctionName</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1520">Method menuFunctionName</span></span>

    public str menuFunctionName([str name])

#### <a name="parameters"></a><span data-ttu-id="f7b4f-1521">パラメーター</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1521">Parameters</span></span>

<span data-ttu-id="f7b4f-1522">名前</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1522">name</span></span>  

#### <a name="return-value"></a><span data-ttu-id="f7b4f-1523">戻り値</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1523">Return Value</span></span>

### <a name="method-menuitemname"></a><span data-ttu-id="f7b4f-1524">メソッド menuItemName</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1524">Method menuItemName</span></span>

    public str menuItemName([str value])

#### <a name="parameters"></a><span data-ttu-id="f7b4f-1525">パラメーター</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1525">Parameters</span></span>

<span data-ttu-id="f7b4f-1526">値</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1526">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="f7b4f-1527">戻り値</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1527">Return Value</span></span>

### <a name="method-menuitemtype"></a><span data-ttu-id="f7b4f-1528">メソッド menuItemType</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1528">Method menuItemType</span></span>

    public MenuItemType menuItemType([MenuItemType value])

#### <a name="parameters"></a><span data-ttu-id="f7b4f-1529">パラメーター</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1529">Parameters</span></span>

<span data-ttu-id="f7b4f-1530">値</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1530">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="f7b4f-1531">戻り値</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1531">Return Value</span></span>

### <a name="method-menuname"></a><span data-ttu-id="f7b4f-1532">メソッド menuName</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1532">Method menuName</span></span>

    public str menuName()

#### <a name="return-value"></a><span data-ttu-id="f7b4f-1533">戻り値</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1533">Return Value</span></span>

### <a name="method-name"></a><span data-ttu-id="f7b4f-1534">メソッド名</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1534">Method name</span></span>

<span data-ttu-id="f7b4f-1535">フォーム、レポート、テーブル、クエリ、または別の MSDAX アプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1535">Gets or sets the name that is used in code to identify a form, report, table, query, or another MSDAX application object.</span></span>

    public str name([str value])

#### <a name="parameters"></a><span data-ttu-id="f7b4f-1536">パラメーター</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1536">Parameters</span></span>

<span data-ttu-id="f7b4f-1537">値</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1537">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="f7b4f-1538">戻り値</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1538">Return Value</span></span>

<span data-ttu-id="f7b4f-1539">アプリケーション オブジェクトを識別するためにコードで使用される名前。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1539">The name that is used in code to identify an application object.</span></span>

#### <a name="remarks"></a><span data-ttu-id="f7b4f-1540">備考</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1540">Remarks</span></span>

<span data-ttu-id="f7b4f-1541">オブジェクトの名前プロパティ値は、コードの競合を避けるために、次の基準を満たしている必要があります。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1541">The name property value of an object must meet the following criteria to avoid code conflicts:</span></span>

-   <span data-ttu-id="f7b4f-1542">文字で始めます。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1542">Begins with a letter.</span></span>
-   <span data-ttu-id="f7b4f-1543">250 文字を超えないでください。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1543">Doesn't exceed 250 characters.</span></span>
-   <span data-ttu-id="f7b4f-1544">数字とアンダースコア文字を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1544">Can include numbers and underscore characters.</span></span>
-   <span data-ttu-id="f7b4f-1545">句読点やスペースを含めることはできません。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1545">Cannot include punctuation or spaces.</span></span>
-   <span data-ttu-id="f7b4f-1546">テーブルは、拡張データ型、基本列挙型、クラスなどの他のパブリック オブジェクトと同じ名前を持つことはできません。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1546">Tables cannot have the same name as other public objects, such as extended data types, base enums, classes, and so on.</span></span>

### <a name="method-neededaccesslevel"></a><span data-ttu-id="f7b4f-1547">メソッド neededAccessLevel</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1547">Method neededAccessLevel</span></span>

<span data-ttu-id="f7b4f-1548">MenuFunction クラスの neededAccessLevel プロパティを取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1548">Gets or sets the neededAccessLevel property for the MenuFunction class.</span></span>

    public int neededAccessLevel([int value])

#### <a name="parameters"></a><span data-ttu-id="f7b4f-1549">パラメーター</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1549">Parameters</span></span>

<span data-ttu-id="f7b4f-1550">値</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1550">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="f7b4f-1551">戻り値</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1551">Return Value</span></span>

<span data-ttu-id="f7b4f-1552">neededAccessLevel プロパティの現在の値。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1552">The current value of the neededAccessLevel property.</span></span>

#### <a name="remarks"></a><span data-ttu-id="f7b4f-1553">備考</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1553">Remarks</span></span>

<span data-ttu-id="f7b4f-1554">AccessType システム列挙値の使用可能な値は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1554">The possible values for the AccessType system enumeration value are as follows:</span></span>

-   <span data-ttu-id="f7b4f-1555">AccessType::NoAccess.</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1555">AccessType::NoAccess.</span></span>
-   <span data-ttu-id="f7b4f-1556">AccessType::View.</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1556">AccessType::View.</span></span>
-   <span data-ttu-id="f7b4f-1557">AccessType::Edit.</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1557">AccessType::Edit.</span></span>
-   <span data-ttu-id="f7b4f-1558">AccessType::Add.</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1558">AccessType::Add.</span></span>
-   <span data-ttu-id="f7b4f-1559">AccessType::Delete.</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1559">AccessType::Delete.</span></span>

### <a name="method-normalimage"></a><span data-ttu-id="f7b4f-1560">メソッド normalImage</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1560">Method normalImage</span></span>

    public str normalImage([str value])

#### <a name="parameters"></a><span data-ttu-id="f7b4f-1561">パラメーター</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1561">Parameters</span></span>

<span data-ttu-id="f7b4f-1562">値</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1562">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="f7b4f-1563">戻り値</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1563">Return Value</span></span>

### <a name="method-normalresource"></a><span data-ttu-id="f7b4f-1564">メソッド normalResource</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1564">Method normalResource</span></span>

    public int normalResource([int value])

#### <a name="parameters"></a><span data-ttu-id="f7b4f-1565">パラメーター</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1565">Parameters</span></span>

<span data-ttu-id="f7b4f-1566">値</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1566">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="f7b4f-1567">戻り値</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1567">Return Value</span></span>

### <a name="method-origin"></a><span data-ttu-id="f7b4f-1568">メソッド origin</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1568">Method origin</span></span>

    public Guid origin([Guid value])

#### <a name="parameters"></a><span data-ttu-id="f7b4f-1569">パラメーター</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1569">Parameters</span></span>

<span data-ttu-id="f7b4f-1570">値</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1570">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="f7b4f-1571">戻り値</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1571">Return Value</span></span>

### <a name="method-parameter"></a><span data-ttu-id="f7b4f-1572">メソッド parameter</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1572">Method parameter</span></span>

    public str parameter([str parameter])

#### <a name="parameters"></a><span data-ttu-id="f7b4f-1573">パラメーター</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1573">Parameters</span></span>

<span data-ttu-id="f7b4f-1574">パラメーター</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1574">parameter</span></span>  

#### <a name="return-value"></a><span data-ttu-id="f7b4f-1575">戻り値</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1575">Return Value</span></span>

### <a name="method-parameters"></a><span data-ttu-id="f7b4f-1576">メソッド parameters</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1576">Method parameters</span></span>

<span data-ttu-id="f7b4f-1577">MenuFunction クラスで実行されるオブジェクトに渡されるパラメータの一覧を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1577">Gets or sets the list of parameters that are passed to objects that are run by the MenuFunction class.</span></span>

    public str parameters([str value])

#### <a name="parameters"></a><span data-ttu-id="f7b4f-1578">パラメーター</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1578">Parameters</span></span>

<span data-ttu-id="f7b4f-1579">値</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1579">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="f7b4f-1580">戻り値</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1580">Return Value</span></span>

<span data-ttu-id="f7b4f-1581">オブジェクトに渡されるパラメーターのリスト。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1581">The list of parameters that are passed to the object.</span></span>

#### <a name="remarks"></a><span data-ttu-id="f7b4f-1582">備考</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1582">Remarks</span></span>

<span data-ttu-id="f7b4f-1583">パラメータ文字列形式は、パラメーター 1 = 値 1、パラメーター 2 = 値 2、.... というようになります。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1583">The parameters string format is Parameter1=Value1, Parameter2=Value2, and so on.</span></span> <span data-ttu-id="f7b4f-1584">オブジェクトは、渡された未認識のパラメーターを無視します。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1584">Objects ignore passed, unrecognized parameters.</span></span>

### <a name="method-securitykey"></a><span data-ttu-id="f7b4f-1585">メソッド securityKey</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1585">Method securityKey</span></span>

    public SecurityKeyId securityKey([SecurityKeyId value])

#### <a name="parameters"></a><span data-ttu-id="f7b4f-1586">パラメーター</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1586">Parameters</span></span>

<span data-ttu-id="f7b4f-1587">値</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1587">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="f7b4f-1588">戻り値</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1588">Return Value</span></span>

### <a name="method-setcompany"></a><span data-ttu-id="f7b4f-1589">メソッド setCompany</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1589">Method setCompany</span></span>

    public boolean setCompany([boolean value])

#### <a name="parameters"></a><span data-ttu-id="f7b4f-1590">パラメーター</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1590">Parameters</span></span>

<span data-ttu-id="f7b4f-1591">値</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1591">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="f7b4f-1592">戻り値</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1592">Return Value</span></span>

### <a name="method-shortcut"></a><span data-ttu-id="f7b4f-1593">メソッド shortCut</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1593">Method shortCut</span></span>

    public str shortCut([str value])

#### <a name="parameters"></a><span data-ttu-id="f7b4f-1594">パラメーター</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1594">Parameters</span></span>

<span data-ttu-id="f7b4f-1595">値</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1595">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="f7b4f-1596">戻り値</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1596">Return Value</span></span>

### <a name="method-showparentmodule"></a><span data-ttu-id="f7b4f-1597">メソッド showParentModule</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1597">Method showParentModule</span></span>

    public boolean showParentModule([boolean value])

#### <a name="parameters"></a><span data-ttu-id="f7b4f-1598">パラメーター</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1598">Parameters</span></span>

<span data-ttu-id="f7b4f-1599">値</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1599">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="f7b4f-1600">戻り値</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1600">Return Value</span></span>

### <a name="method-visible"></a><span data-ttu-id="f7b4f-1601">メソッド visible</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1601">Method visible</span></span>

    public boolean visible([boolean value])

#### <a name="parameters"></a><span data-ttu-id="f7b4f-1602">パラメーター</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1602">Parameters</span></span>

<span data-ttu-id="f7b4f-1603">値</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1603">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="f7b4f-1604">戻り値</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1604">Return Value</span></span>

### <a name="method-webtarget"></a><span data-ttu-id="f7b4f-1605">メソッド webTarget</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1605">Method webTarget</span></span>

    public str webTarget([str value])

#### <a name="parameters"></a><span data-ttu-id="f7b4f-1606">パラメーター</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1606">Parameters</span></span>

<span data-ttu-id="f7b4f-1607">値</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1607">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="f7b4f-1608">戻り値</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1608">Return Value</span></span>

### <a name="method-save"></a><span data-ttu-id="f7b4f-1609">メソッド save</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1609">Method save</span></span>

    public void save()

### <a name="method-new"></a><span data-ttu-id="f7b4f-1610">メソッド new</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1610">Method new</span></span>

<span data-ttu-id="f7b4f-1611">TreeNode クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1611">Initializes a new instance of the TreeNode class.</span></span>

    public void new(str Name)

#### <a name="parameters"></a><span data-ttu-id="f7b4f-1612">パラメーター</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1612">Parameters</span></span>

<span data-ttu-id="f7b4f-1613">氏名</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1613">Name</span></span>  

### <a name="method-makewebmenu"></a><span data-ttu-id="f7b4f-1614">メソッド makeWebMenu</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1614">Method makeWebMenu</span></span>

    public void makeWebMenu(Object outputClass)

#### <a name="parameters"></a><span data-ttu-id="f7b4f-1615">パラメーター</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1615">Parameters</span></span>

<span data-ttu-id="f7b4f-1616">outputClass</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1616">outputClass</span></span>  

### <a name="method-addmenuitem"></a><span data-ttu-id="f7b4f-1617">メソッド addMenuitem</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1617">Method addMenuitem</span></span>

<span data-ttu-id="f7b4f-1618">メニューにメニュー項目を追加します。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1618">Adds a menu item to the menu.</span></span>

    public void addMenuitem(xMenuFunction menuFunction)

#### <a name="parameters"></a><span data-ttu-id="f7b4f-1619">パラメーター</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1619">Parameters</span></span>

<span data-ttu-id="f7b4f-1620">menuFunction</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1620">menuFunction</span></span>  
<span data-ttu-id="f7b4f-1621">追加するメニュー項目。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1621">The menu item to add.</span></span>

### <a name="method-settreenodename"></a><span data-ttu-id="f7b4f-1622">メソッド setTreeNodeName</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1622">Method setTreeNodeName</span></span>

    public void setTreeNodeName(str name)

#### <a name="parameters"></a><span data-ttu-id="f7b4f-1623">パラメーター</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1623">Parameters</span></span>

<span data-ttu-id="f7b4f-1624">名前</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1624">name</span></span>  

### <a name="method-addmenureference"></a><span data-ttu-id="f7b4f-1625">メソッド addMenuReference</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1625">Method addMenuReference</span></span>

    public void addMenuReference(Menu menu)

#### <a name="parameters"></a><span data-ttu-id="f7b4f-1626">パラメーター</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1626">Parameters</span></span>

<span data-ttu-id="f7b4f-1627">メニュー</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1627">menu</span></span>  

### <a name="method-addsubmenu"></a><span data-ttu-id="f7b4f-1628">メソッド addSubmenu</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1628">Method addSubmenu</span></span>

<span data-ttu-id="f7b4f-1629">メニューにサブメニューを追加します。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1629">Adds a submenu to the menu.</span></span>

    public void addSubmenu(str name)

#### <a name="parameters"></a><span data-ttu-id="f7b4f-1630">パラメーター</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1630">Parameters</span></span>

<span data-ttu-id="f7b4f-1631">名前</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1631">name</span></span>  
<span data-ttu-id="f7b4f-1632">メニューに追加するサブメニューの名前に評価される文字列式。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1632">A string expression that evaluates to the name of the submenu to add to the menu.</span></span>

### <a name="method-addseparator"></a><span data-ttu-id="f7b4f-1633">メソッド addSeparator</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1633">Method addSeparator</span></span>

<span data-ttu-id="f7b4f-1634">メニューにメニューの区切りを追加します。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1634">Adds a menu separator to the menu.</span></span>

    public void addSeparator()

## <a name="class-menuitem"></a><span data-ttu-id="f7b4f-1635">クラス MenuItem</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1635">Class MenuItem</span></span>
    class MenuItem extends TreeNode

<span data-ttu-id="f7b4f-1636">MenuItem クラスを使用すると、X++ コードとメタデータの作成、読み取り、更新、および削除を行うことができます。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1636">The MenuItem class lets you create, read, update, and delete X++ code and metadata.</span></span>

### <a name="remarks"></a><span data-ttu-id="f7b4f-1637">備考</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1637">Remarks</span></span>

<span data-ttu-id="f7b4f-1638">メニュー項目は、メニュー機能のユーザー インターフェイスを表します。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1638">A menu item represents the user interface of a menu function.</span></span> <span data-ttu-id="f7b4f-1639">メニュー項目は、ユーザーがメニュー項目を選択するときに実行される MenuFunction オブジェクトにリンクされます。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1639">Menu items are linked to a MenuFunction object, which runs when the user selects the menu item.</span></span> <span data-ttu-id="f7b4f-1640">この API が呼び出される前に、ユーザーが開発セキュリティ キー (SysDevelopment) にアクセスできることを確認します。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1640">Make sure that the user has access to the development security key (SysDevelopment) before this API is called.</span></span>

### <a name="examples"></a><span data-ttu-id="f7b4f-1641">例</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1641">Examples</span></span>

### <a name="methods"></a><span data-ttu-id="f7b4f-1642">メソッド</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1642">Methods</span></span>

| <span data-ttu-id="f7b4f-1643">方法</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1643">Method</span></span>                                                     | <span data-ttu-id="f7b4f-1644">説明</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1644">Description</span></span>                                                                                                                                   |
|------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f7b4f-1645">public str allowRootNavigation(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1645">public str allowRootNavigation(\[str value\])</span></span>              |                                                                                                                                               |
| <span data-ttu-id="f7b4f-1646">public boolean isDisplayedInContentArea(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1646">public boolean isDisplayedInContentArea(\[boolean value\])</span></span> |                                                                                                                                               |
| <span data-ttu-id="f7b4f-1647">public str label(\[str name\])</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1647">public str label(\[str name\])</span></span>                             |                                                                                                                                               |
| <span data-ttu-id="f7b4f-1648">public str menuFunctionName(\[str name\])</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1648">public str menuFunctionName(\[str name\])</span></span>                  |                                                                                                                                               |
| <span data-ttu-id="f7b4f-1649">public str menuItemName(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1649">public str menuItemName(\[str value\])</span></span>                     |                                                                                                                                               |
| <span data-ttu-id="f7b4f-1650">public MenuItemType menuItemType(\[MenuItemType value\])</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1650">public MenuItemType menuItemType(\[MenuItemType value\])</span></span>   |                                                                                                                                               |
| <span data-ttu-id="f7b4f-1651">public str name(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1651">public str name(\[str value\])</span></span>                             | <span data-ttu-id="f7b4f-1652">フォーム、レポート、テーブル、クエリ、または別の Finance and Operations アプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1652">Gets or sets the name that is used in the code to identify a form, report, table, query, or another Finance and Operations application object.</span></span> |
| <span data-ttu-id="f7b4f-1653">public str parameter(\[str parameter\])</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1653">public str parameter(\[str parameter\])</span></span>                    |                                                                                                                                               |
| <span data-ttu-id="f7b4f-1654">public str parameters(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1654">public str parameters(\[str value\])</span></span>                       | <span data-ttu-id="f7b4f-1655">MenuFunction クラスで実行されるオブジェクトに渡されるパラメータの一覧を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1655">Gets or sets the list of parameters that are passed to objects that are run by the MenuFunction class.</span></span>                                        |
| <span data-ttu-id="f7b4f-1656">public str shortCut(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1656">public str shortCut(\[str value\])</span></span>                         |                                                                                                                                               |
| <span data-ttu-id="f7b4f-1657">public boolean showParentModule(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1657">public boolean showParentModule(\[boolean value\])</span></span>         |                                                                                                                                               |
| <span data-ttu-id="f7b4f-1658">public boolean visible(\[boolean value\])</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1658">public boolean visible(\[boolean value\])</span></span>                  |                                                                                                                                               |
| <span data-ttu-id="f7b4f-1659">public str webTarget(\[str value\])</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1659">public str webTarget(\[str value\])</span></span>                        |                                                                                                                                               |

### <a name="method-allowrootnavigation"></a><span data-ttu-id="f7b4f-1660">メソッド allowRootNavigation</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1660">Method allowRootNavigation</span></span>

    public str allowRootNavigation([str value])

#### <a name="parameters"></a><span data-ttu-id="f7b4f-1661">パラメーター</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1661">Parameters</span></span>

<span data-ttu-id="f7b4f-1662">値</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1662">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="f7b4f-1663">戻り値</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1663">Return Value</span></span>

### <a name="method-isdisplayedincontentarea"></a><span data-ttu-id="f7b4f-1664">メソッド isDisplayedInContentArea</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1664">Method isDisplayedInContentArea</span></span>

    public boolean isDisplayedInContentArea([boolean value])

#### <a name="parameters"></a><span data-ttu-id="f7b4f-1665">パラメーター</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1665">Parameters</span></span>

<span data-ttu-id="f7b4f-1666">値</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1666">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="f7b4f-1667">戻り値</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1667">Return Value</span></span>

### <a name="method-label"></a><span data-ttu-id="f7b4f-1668">メソッド label</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1668">Method label</span></span>

    public str label([str name])

#### <a name="parameters"></a><span data-ttu-id="f7b4f-1669">パラメーター</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1669">Parameters</span></span>

<span data-ttu-id="f7b4f-1670">名前</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1670">name</span></span>  

#### <a name="return-value"></a><span data-ttu-id="f7b4f-1671">戻り値</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1671">Return Value</span></span>

### <a name="method-menufunctionname"></a><span data-ttu-id="f7b4f-1672">メソッド menuFunctionName</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1672">Method menuFunctionName</span></span>

    public str menuFunctionName([str name])

#### <a name="parameters"></a><span data-ttu-id="f7b4f-1673">パラメーター</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1673">Parameters</span></span>

<span data-ttu-id="f7b4f-1674">名前</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1674">name</span></span>  

#### <a name="return-value"></a><span data-ttu-id="f7b4f-1675">戻り値</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1675">Return Value</span></span>

### <a name="method-menuitemname"></a><span data-ttu-id="f7b4f-1676">メソッド menuItemName</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1676">Method menuItemName</span></span>

    public str menuItemName([str value])

#### <a name="parameters"></a><span data-ttu-id="f7b4f-1677">パラメーター</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1677">Parameters</span></span>

<span data-ttu-id="f7b4f-1678">値</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1678">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="f7b4f-1679">戻り値</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1679">Return Value</span></span>

### <a name="method-menuitemtype"></a><span data-ttu-id="f7b4f-1680">メソッド menuItemType</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1680">Method menuItemType</span></span>

    public MenuItemType menuItemType([MenuItemType value])

#### <a name="parameters"></a><span data-ttu-id="f7b4f-1681">パラメーター</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1681">Parameters</span></span>

<span data-ttu-id="f7b4f-1682">値</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1682">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="f7b4f-1683">戻り値</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1683">Return Value</span></span>

### <a name="method-name"></a><span data-ttu-id="f7b4f-1684">メソッド名</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1684">Method name</span></span>

<span data-ttu-id="f7b4f-1685">フォーム、レポート、テーブル、クエリ、または別の Finance and Operations アプリケーション オブジェクトを識別するためのコードで使用される名前を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1685">Gets or sets the name that is used in the code to identify a form, report, table, query, or another Finance and Operations application object.</span></span>

    public str name([str value])

#### <a name="parameters"></a><span data-ttu-id="f7b4f-1686">パラメーター</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1686">Parameters</span></span>

<span data-ttu-id="f7b4f-1687">値</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1687">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="f7b4f-1688">戻り値</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1688">Return Value</span></span>

<span data-ttu-id="f7b4f-1689">アプリケーション オブジェクトを識別するためにコードで使用される名前。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1689">The name that is used in the code to identify an application object.</span></span>

#### <a name="remarks"></a><span data-ttu-id="f7b4f-1690">備考</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1690">Remarks</span></span>

<span data-ttu-id="f7b4f-1691">オブジェクトの名前プロパティ値は、コードの競合を避けるために、次の基準を満たしている必要があります。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1691">The name property value of an object must meet the following criteria to avoid code conflicts:</span></span>

-   <span data-ttu-id="f7b4f-1692">文字で始めます。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1692">Begins with a letter.</span></span>
-   <span data-ttu-id="f7b4f-1693">250 文字を超えないでください。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1693">Doesn't exceed 250 characters.</span></span>
-   <span data-ttu-id="f7b4f-1694">数字とアンダースコア文字を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1694">Can include numbers and underscore characters.</span></span>
-   <span data-ttu-id="f7b4f-1695">句読点やスペースを含めることはできません。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1695">Cannot include punctuation or spaces.</span></span>
-   <span data-ttu-id="f7b4f-1696">テーブルは、拡張データ型、基本列挙型、クラスなどの他のパブリック オブジェクトと同じ名前を持つことはできません。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1696">Tables cannot have the same name as other public objects, such as extended data types, base enums, classes, and so on.</span></span>

### <a name="method-parameter"></a><span data-ttu-id="f7b4f-1697">メソッド parameter</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1697">Method parameter</span></span>

    public str parameter([str parameter])

#### <a name="parameters"></a><span data-ttu-id="f7b4f-1698">パラメーター</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1698">Parameters</span></span>

<span data-ttu-id="f7b4f-1699">パラメーター</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1699">parameter</span></span>  

#### <a name="return-value"></a><span data-ttu-id="f7b4f-1700">戻り値</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1700">Return Value</span></span>

### <a name="method-parameters"></a><span data-ttu-id="f7b4f-1701">メソッド parameters</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1701">Method parameters</span></span>

<span data-ttu-id="f7b4f-1702">MenuFunction クラスで実行されるオブジェクトに渡されるパラメータの一覧を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1702">Gets or sets the list of parameters that are passed to objects that are run by the MenuFunction class.</span></span>

    public str parameters([str value])

#### <a name="parameters"></a><span data-ttu-id="f7b4f-1703">パラメーター</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1703">Parameters</span></span>

<span data-ttu-id="f7b4f-1704">値</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1704">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="f7b4f-1705">戻り値</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1705">Return Value</span></span>

<span data-ttu-id="f7b4f-1706">オブジェクトに渡されるパラメーターのリスト。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1706">The list of parameters that are passed to the object.</span></span>

#### <a name="remarks"></a><span data-ttu-id="f7b4f-1707">備考</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1707">Remarks</span></span>

<span data-ttu-id="f7b4f-1708">パラメータ文字列形式は、パラメーター 1 = 値 1、パラメーター 2 = 値 2、.... というようになります。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1708">The parameters string format is Parameter1=Value1, Parameter2=Value2, and so on.</span></span> <span data-ttu-id="f7b4f-1709">オブジェクトは、渡された未認識のパラメーターを無視します。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1709">Objects ignore passed, unrecognized parameters.</span></span>

### <a name="method-shortcut"></a><span data-ttu-id="f7b4f-1710">メソッド shortCut</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1710">Method shortCut</span></span>

    public str shortCut([str value])

#### <a name="parameters"></a><span data-ttu-id="f7b4f-1711">パラメーター</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1711">Parameters</span></span>

<span data-ttu-id="f7b4f-1712">値</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1712">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="f7b4f-1713">戻り値</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1713">Return Value</span></span>

### <a name="method-showparentmodule"></a><span data-ttu-id="f7b4f-1714">メソッド showParentModule</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1714">Method showParentModule</span></span>

    public boolean showParentModule([boolean value])

#### <a name="parameters"></a><span data-ttu-id="f7b4f-1715">パラメーター</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1715">Parameters</span></span>

<span data-ttu-id="f7b4f-1716">値</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1716">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="f7b4f-1717">戻り値</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1717">Return Value</span></span>

### <a name="method-visible"></a><span data-ttu-id="f7b4f-1718">メソッド visible</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1718">Method visible</span></span>

    public boolean visible([boolean value])

#### <a name="parameters"></a><span data-ttu-id="f7b4f-1719">パラメーター</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1719">Parameters</span></span>

<span data-ttu-id="f7b4f-1720">値</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1720">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="f7b4f-1721">戻り値</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1721">Return Value</span></span>

### <a name="method-webtarget"></a><span data-ttu-id="f7b4f-1722">メソッド webTarget</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1722">Method webTarget</span></span>

    public str webTarget([str value])

#### <a name="parameters"></a><span data-ttu-id="f7b4f-1723">パラメーター</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1723">Parameters</span></span>

<span data-ttu-id="f7b4f-1724">値</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1724">value</span></span>  

#### <a name="return-value"></a><span data-ttu-id="f7b4f-1725">戻り値</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1725">Return Value</span></span>

## <a name="class-menureference"></a><span data-ttu-id="f7b4f-1726">クラス MenuReference</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1726">Class MenuReference</span></span>
    class MenuReference extends TreeNode

<span data-ttu-id="f7b4f-1727">MenuReference クラスを使用すると、X++ コードとメタデータの作成、読み取り、更新、および削除を行うことができます。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1727">The MenuReference class enables you to create, read, update, and delete X++ code and metadata.</span></span>

### <a name="remarks"></a><span data-ttu-id="f7b4f-1728">備考</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1728">Remarks</span></span>

### <a name="examples"></a><span data-ttu-id="f7b4f-1729">例</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1729">Examples</span></span>

### <a name="methods"></a><span data-ttu-id="f7b4f-1730">メソッド</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1730">Methods</span></span>

| <span data-ttu-id="f7b4f-1731">方法</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1731">Method</span></span>                | <span data-ttu-id="f7b4f-1732">説明</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1732">Description</span></span> |
|-----------------------|-------------|
| <span data-ttu-id="f7b4f-1733">public str menuName()</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1733">public str menuName()</span></span> |             |

### <a name="method-menuname"></a><span data-ttu-id="f7b4f-1734">メソッド menuName</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1734">Method menuName</span></span>

    public str menuName()

#### <a name="return-value"></a><span data-ttu-id="f7b4f-1735">戻り値</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1735">Return Value</span></span>

## <a name="class-messagewin"></a><span data-ttu-id="f7b4f-1736">クラス MessageWin</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1736">Class MessageWin</span></span>
    class MessageWin extends Object

<span data-ttu-id="f7b4f-1737">MessageWin クラスを使用すると、Finance and Operations 開発環境の messageWindow クラスにアクセスできます。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1737">The MessageWin class gives access to the messageWindow class of the Finance and Operations development environment.</span></span>

### <a name="remarks"></a><span data-ttu-id="f7b4f-1738">備考</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1738">Remarks</span></span>

<span data-ttu-id="f7b4f-1739">さらに MessageWin オブジェクトをインスタンス化することができますが、画面上に同一のメッセージ ウィンドウを参照します。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1739">Although you can instantiate more MessageWin objects, they will all refer to the same message window on the screen.</span></span>

### <a name="examples"></a><span data-ttu-id="f7b4f-1740">例</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1740">Examples</span></span>

### <a name="methods"></a><span data-ttu-id="f7b4f-1741">メソッド</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1741">Methods</span></span>

| <span data-ttu-id="f7b4f-1742">方法</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1742">Method</span></span>                        | <span data-ttu-id="f7b4f-1743">説明</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1743">Description</span></span>                                           |
|-------------------------------|-------------------------------------------------------|
| <span data-ttu-id="f7b4f-1744">public void clear()</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1744">public void clear()</span></span>           | <span data-ttu-id="f7b4f-1745">メッセージ ウィンドウをクリアします。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1745">Clears the message window.</span></span>                            |
| <span data-ttu-id="f7b4f-1746">public void activate()</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1746">public void activate()</span></span>        | <span data-ttu-id="f7b4f-1747">メッセージ ウィンドウを現在のアクティブ ウィンドウにします。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1747">Makes the message window the currently active window.</span></span> |
| <span data-ttu-id="f7b4f-1748">public void addLine(str line)</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1748">public void addLine(str line)</span></span> | <span data-ttu-id="f7b4f-1749">行をメッセージ ウィンドウに記述します。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1749">Writes a line to the message window.</span></span>                  |

### <a name="method-clear"></a><span data-ttu-id="f7b4f-1750">メソッド clear</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1750">Method clear</span></span>

<span data-ttu-id="f7b4f-1751">メッセージ ウィンドウをクリアします。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1751">Clears the message window.</span></span>

    public void clear()

### <a name="method-activate"></a><span data-ttu-id="f7b4f-1752">メソッド activate</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1752">Method activate</span></span>

<span data-ttu-id="f7b4f-1753">メッセージ ウィンドウを現在のアクティブ ウィンドウにします。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1753">Makes the message window the currently active window.</span></span>

    public void activate()

#### <a name="remarks"></a><span data-ttu-id="f7b4f-1754">備考</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1754">Remarks</span></span>

<span data-ttu-id="f7b4f-1755">バージョン 2.11 より前に、行が追加されたり内容が消去されるとメッセージ ウィンドウがフォーカスを取得します。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1755">Before version 2.11, the message window would get focus when lines were added or contents were cleared.</span></span> <span data-ttu-id="f7b4f-1756">バージョン 2.11 以降では、開発者は、メッセージ ウィンドウを一番上のウィンドウにするためにこのメソッドを呼び出す必要があります。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1756">Starting in version 2.11, the developer must call this method to make the message window the top window.</span></span>

### <a name="method-addline"></a><span data-ttu-id="f7b4f-1757">メソッド addLine</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1757">Method addLine</span></span>

<span data-ttu-id="f7b4f-1758">行をメッセージ ウィンドウに記述します。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1758">Writes a line to the message window.</span></span>

    public void addLine(str line)

#### <a name="parameters"></a><span data-ttu-id="f7b4f-1759">パラメーター</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1759">Parameters</span></span>

<span data-ttu-id="f7b4f-1760">明細行</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1760">line</span></span>  
<span data-ttu-id="f7b4f-1761">メッセージ ウィンドウへの書き込み明細行を含む文字列。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1761">A string that contains the line to write to the message window.</span></span>

## <a name="class-methodinfo"></a><span data-ttu-id="f7b4f-1762">クラス MethodInfo</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1762">Class MethodInfo</span></span>
    class MethodInfo extends Object

<span data-ttu-id="f7b4f-1763">指定したメソッドについて説明します。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1763">Provides information about a specified method.</span></span>

### <a name="remarks"></a><span data-ttu-id="f7b4f-1764">備考</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1764">Remarks</span></span>

<span data-ttu-id="f7b4f-1765">SysDictTable クラスを使用してテーブル メソッドを MethodInfo に割り当てます。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1765">Assign a table method to MethodInfo by using the SysDictTable class.</span></span> <span data-ttu-id="f7b4f-1766">SysDictClass クラスを使用してクラス メソッドを割り当てます。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1766">Assign a class method by using the SysDictClass class.</span></span> <span data-ttu-id="f7b4f-1767">次のクラスは MethodInfo を拡張しています。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1767">The following classes extend MethodInfo:</span></span>

-   <span data-ttu-id="f7b4f-1768">SysMethodInfo</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1768">SysMethodInfo</span></span>
-   <span data-ttu-id="f7b4f-1769">DictMethod</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1769">DictMethod</span></span>

### <a name="examples"></a><span data-ttu-id="f7b4f-1770">例</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1770">Examples</span></span>

<span data-ttu-id="f7b4f-1771">次の例では、SysDictClass::ObjectMethodObject メソッドを使用して、FormBuildDataSource クラス オブジェクトのメソッドをMethodInfo クラスのインスタンスに割り当てます。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1771">The following example uses the SysDictClass::ObjectMethodObject method to assign a method of a FormBuildDataSource Class object to an instance of the MethodInfo class.</span></span> <span data-ttu-id="f7b4f-1772">整数値はメソッドを指定します。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1772">An integer value specifies the method.</span></span> <span data-ttu-id="f7b4f-1773">MethodInfo.name メソッドは、メソッド名を返します。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1773">The MethodInfo.name Method method returns the method name.</span></span>

    void getMethodInfo() 
    { 
        MethodInfo methodInfo; 
        SysDictClass sysDictClass; 
        str name; 
        try 
        { 
            sysDictClass = new SysDictClass(classnum(FormBuildDataSource)); 
            methodInfo = sysDictClass.objectMethodObject(1); 
            if(!methodInfo) 
            { 
                throw exception::Error; 
            } 
            name = methodInfo.name(); 
            print name; 
            pause; 
         } 
         catch (exception::Error) 
         { 
            print "The specified method does not exist"; 
            pause; 
         } 
    }

### <a name="methods"></a><span data-ttu-id="f7b4f-1774">メソッド</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1774">Methods</span></span>

| <span data-ttu-id="f7b4f-1775">方法</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1775">Method</span></span>                                                      | <span data-ttu-id="f7b4f-1776">説明</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1776">Description</span></span>                                                                                                                                   |
|-------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f7b4f-1777">public AccessSpecifier accessSpecifier()</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1777">public AccessSpecifier accessSpecifier()</span></span>                    | <span data-ttu-id="f7b4f-1778">メソッドがパブリック、保護、またはプライベートかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1778">Specifies whether the method is public, protected, or private.</span></span>                                                                                |
| <span data-ttu-id="f7b4f-1779">public boolean compiledOk()</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1779">public boolean compiledOk()</span></span>                                 | <span data-ttu-id="f7b4f-1780">メソッドがコンパイルされているかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1780">Specifies whether the method has compiled.</span></span>                                                                                                    |
| <span data-ttu-id="f7b4f-1781">public TableId displayTableId()</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1781">public TableId displayTableId()</span></span>                             |                                                                                                                                               |
| <span data-ttu-id="f7b4f-1782">public DisplayFunctionType displayType()</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1782">public DisplayFunctionType displayType()</span></span>                    | <span data-ttu-id="f7b4f-1783">メソッドの表示機能のタイプを指定します。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1783">Specifies the display function type of a method.</span></span>                                                                                              |
| <span data-ttu-id="f7b4f-1784">public Array getAllAttributes()</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1784">public Array getAllAttributes()</span></span>                             | <span data-ttu-id="f7b4f-1785">メソッドの属性の完全なセットを取得します。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1785">Gets the full set of attributes for the method.</span></span>                                                                                               |
| <span data-ttu-id="f7b4f-1786">public Object getAttribute(str attribute)</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1786">public Object getAttribute(str attribute)</span></span>                   | <span data-ttu-id="f7b4f-1787">クラス ヘッダー メタデータから最初に一致する属性を取得し、その属性を表すオブジェクト クラスのインスタンスを作成し、返します。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1787">Gets the first matching attribute from the class header metadata, creates an instance of the Object class that represents it, and returns it.</span></span> |
| <span data-ttu-id="f7b4f-1788">public Array getAttributes(str attribute)</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1788">public Array getAttributes(str attribute)</span></span>                   |                                                                                                                                               |
| <span data-ttu-id="f7b4f-1789">public boolean isAbstract()</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1789">public boolean isAbstract()</span></span>                                 | <span data-ttu-id="f7b4f-1790">メソッドが抽象かどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1790">Indicates whether the method is abstract.</span></span>                                                                                                     |
| <span data-ttu-id="f7b4f-1791">public boolean isStatic()</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1791">public boolean isStatic()</span></span>                                   | <span data-ttu-id="f7b4f-1792">メソッドが静的かどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1792">Specifies whether the method is static.</span></span>                                                                                                       |
| <span data-ttu-id="f7b4f-1793">public str name()</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1793">public str name()</span></span>                                           | <span data-ttu-id="f7b4f-1794">メソッドの名前を指定します。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1794">Specifies the name of a method.</span></span>                                                                                                               |
| <span data-ttu-id="f7b4f-1795">public int noParms()</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1795">public int noParms()</span></span>                                        | <span data-ttu-id="f7b4f-1796">メソッド内のパラメーターの数を指定します。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1796">Specifies the number of parameters in a method.</span></span>                                                                                               |
| <span data-ttu-id="f7b4f-1797">public int noVars()</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1797">public int noVars()</span></span>                                         | <span data-ttu-id="f7b4f-1798">メソッド内の変数の数を指定します。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1798">Specifies the number of variables in a method.</span></span>                                                                                                |
| <span data-ttu-id="f7b4f-1799">public int parentId()</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1799">public int parentId()</span></span>                                       | <span data-ttu-id="f7b4f-1800">テーブル メソッドのテーブル ID またはクラス メソッドのクラス ID を指定します。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1800">Specifies the table ID for a table method or the class ID for a class method.</span></span>                                                                 |
| <span data-ttu-id="f7b4f-1801">public str propertyHelp()</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1801">public str propertyHelp()</span></span>                                   | <span data-ttu-id="f7b4f-1802">メソッドがコントロールに設定または返すヘルプ テキストを指定します。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1802">Specifies the Help text that a method sets or returns for a control.</span></span>                                                                          |
| <span data-ttu-id="f7b4f-1803">public NoYes PropertyMethod()</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1803">public NoYes PropertyMethod()</span></span>                               | <span data-ttu-id="f7b4f-1804">メソッドがプロパティ メソッドかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1804">Specifies whether a method is a property method.</span></span>                                                                                              |
| <span data-ttu-id="f7b4f-1805">public int returnId()</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1805">public int returnId()</span></span>                                       | <span data-ttu-id="f7b4f-1806">値を返すメソッドについて、拡張データ型やクラスなどの特定の戻り値のデータ型の ID を指定します。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1806">Specifies the ID for certain return data types, such as extended data types and classes, for a method that returns a value.</span></span>                   |
| <span data-ttu-id="f7b4f-1807">public Types returnType()</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1807">public Types returnType()</span></span>                                   | <span data-ttu-id="f7b4f-1808">メソッドの戻り値の型を指定します。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1808">Specifies a method return type.</span></span>                                                                                                               |
| <span data-ttu-id="f7b4f-1809">public ClassRunMode runMode()</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1809">public ClassRunMode runMode()</span></span>                               | <span data-ttu-id="f7b4f-1810">メソッドが実行される場所を指定します。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1810">Specifies where a method is executed.</span></span>                                                                                                         |
| <span data-ttu-id="f7b4f-1811">public int varId(int variableNumber)</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1811">public int varId(int variableNumber)</span></span>                        | <span data-ttu-id="f7b4f-1812">変数を含むメソッドについて、拡張データ型や列挙値などの特定の変数のデータ型の ID を指定します。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1812">Specifies the ID for certain variable data types, such as extended data types and enums, for a method that contains variables.</span></span>                |
| <span data-ttu-id="f7b4f-1813">public int varIdOld(int variableNumber)</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1813">public int varIdOld(int variableNumber)</span></span>                     |                                                                                                                                               |
| <span data-ttu-id="f7b4f-1814">public Types varType(int variableNumber)</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1814">public Types varType(int variableNumber)</span></span>                    | <span data-ttu-id="f7b4f-1815">Types 列挙の値を使用して変数のデータ型を指定します。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1815">Specifies a variable data type by using values from the Types enumeration.</span></span>                                                                    |
| <span data-ttu-id="f7b4f-1816">public void new(UtilElementType utilType, int Id, str Name)</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1816">public void new(UtilElementType utilType, int Id, str Name)</span></span> | <span data-ttu-id="f7b4f-1817">MethodInfo クラスの新しいインスタンスを作成します。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1817">Creates a new instance of the MethodInfo class.</span></span>                                                                                               |
| <span data-ttu-id="f7b4f-1818">public void setMethod(MemberFunction method)</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1818">public void setMethod(MemberFunction method)</span></span>                | <span data-ttu-id="f7b4f-1819">インスタンスを使用してアプリケーション オブジェクト ツリー (AOT) 内のノードのアプリケーション オブジェクト タイプを指定します。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1819">Specifies the application object type of a node in the Application Object Tree (AOT) by using an instance of the .</span></span>                            |

### <a name="method-accessspecifier"></a><span data-ttu-id="f7b4f-1820">メソッド accessSpecifier</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1820">Method accessSpecifier</span></span>

<span data-ttu-id="f7b4f-1821">メソッドがパブリック、保護、またはプライベートかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1821">Specifies whether the method is public, protected, or private.</span></span>

    public AccessSpecifier accessSpecifier()

#### <a name="return-value"></a><span data-ttu-id="f7b4f-1822">戻り値</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1822">Return Value</span></span>

<span data-ttu-id="f7b4f-1823">メソッドがパブリック、保護、またはプライベートのいずれかを指定する AccessSpecifier 列挙型値です。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1823">An AccessSpecifier enum value that specifies whether the method is public, protected, or private.</span></span>

### <a name="method-compiledok"></a><span data-ttu-id="f7b4f-1824">メソッド compiledOk</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1824">Method compiledOk</span></span>

<span data-ttu-id="f7b4f-1825">メソッドがコンパイルされているかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1825">Specifies whether the method has compiled.</span></span>

    public boolean compiledOk()

#### <a name="return-value"></a><span data-ttu-id="f7b4f-1826">戻り値</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1826">Return Value</span></span>

<span data-ttu-id="f7b4f-1827">メソッドがコンパイル済みの場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1827">true if the method has compiled; otherwise, false.</span></span>

### <a name="method-displaytableid"></a><span data-ttu-id="f7b4f-1828">メソッド displayTableId</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1828">Method displayTableId</span></span>

    public TableId displayTableId()

#### <a name="return-value"></a><span data-ttu-id="f7b4f-1829">戻り値</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1829">Return Value</span></span>

### <a name="method-displaytype"></a><span data-ttu-id="f7b4f-1830">メソッド displayType</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1830">Method displayType</span></span>

<span data-ttu-id="f7b4f-1831">メソッドの表示機能のタイプを指定します。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1831">Specifies the display function type of a method.</span></span>

    public DisplayFunctionType displayType()

#### <a name="return-value"></a><span data-ttu-id="f7b4f-1832">戻り値</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1832">Return Value</span></span>

<span data-ttu-id="f7b4f-1833">メソッドの表示機能のタイプを示す DisplayFunctionType 列挙値。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1833">A DisplayFunctionType enumeration value that indicates the display function type of a method.</span></span>

#### <a name="remarks"></a><span data-ttu-id="f7b4f-1834">備考</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1834">Remarks</span></span>

<span data-ttu-id="f7b4f-1835">次のテーブルに、displayType メソッドによって返される可能な値を示します。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1835">The following table lists the possible values returned by the displayType method.</span></span>

|           |                                             |
|-----------|---------------------------------------------|
| <span data-ttu-id="f7b4f-1836">取得</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1836">Get</span></span>       | <span data-ttu-id="f7b4f-1837">このメソッドは表示メソッドです。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1837">The method is a display method.</span></span>             |
| <span data-ttu-id="f7b4f-1838">None</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1838">None</span></span>      | <span data-ttu-id="f7b4f-1839">このメソッドは、表示メソッドまたは編集メソッドではありません。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1839">The method is not a display or edit method.</span></span> |
| <span data-ttu-id="f7b4f-1840">RecordGet</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1840">RecordGet</span></span> | <span data-ttu-id="f7b4f-1841">このメソッドは、レコードを取得します。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1841">The method gets a record.</span></span>                   |
| <span data-ttu-id="f7b4f-1842">RecordSet</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1842">RecordSet</span></span> | <span data-ttu-id="f7b4f-1843">このメソッドは、レコードを設定します。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1843">The method sets a record.</span></span>                   |
| <span data-ttu-id="f7b4f-1844">セット</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1844">Set</span></span>       | <span data-ttu-id="f7b4f-1845">このメソッドは、編集メソッドです。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1845">The method is an edit method.</span></span>               |

### <a name="method-getallattributes"></a><span data-ttu-id="f7b4f-1846">メソッド getAllAttributes</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1846">Method getAllAttributes</span></span>

<span data-ttu-id="f7b4f-1847">メソッドの属性の完全なセットを取得します。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1847">Gets the full set of attributes for the method.</span></span>

    public Array getAllAttributes()

#### <a name="return-value"></a><span data-ttu-id="f7b4f-1848">戻り値</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1848">Return Value</span></span>

<span data-ttu-id="f7b4f-1849">メソッドの SysAttribute オブジェクトの配列。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1849">The Array of SysAttribute objects for the method.</span></span>

### <a name="method-getattribute"></a><span data-ttu-id="f7b4f-1850">メソッド getAttribute</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1850">Method getAttribute</span></span>

<span data-ttu-id="f7b4f-1851">クラス ヘッダー メタデータから最初に一致する属性を取得し、その属性を表すオブジェクト クラスのインスタンスを作成し、返します。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1851">Gets the first matching attribute from the class header metadata, creates an instance of the Object class that represents it, and returns it.</span></span>

    public Object getAttribute(str attribute)

#### <a name="parameters"></a><span data-ttu-id="f7b4f-1852">パラメーター</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1852">Parameters</span></span>

<span data-ttu-id="f7b4f-1853">属性</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1853">attribute</span></span>  
<span data-ttu-id="f7b4f-1854">検索の対象である属性。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1854">The attribute for which to search.</span></span>

#### <a name="return-value"></a><span data-ttu-id="f7b4f-1855">戻り値</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1855">Return Value</span></span>

<span data-ttu-id="f7b4f-1856">オブジェクト クラスのインスタンスとしての属性。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1856">The attribute as an instance of the Object class.</span></span>

### <a name="method-getattributes"></a><span data-ttu-id="f7b4f-1857">メソッド getAttributes</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1857">Method getAttributes</span></span>

    public Array getAttributes(str attribute)

#### <a name="parameters"></a><span data-ttu-id="f7b4f-1858">パラメーター</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1858">Parameters</span></span>

<span data-ttu-id="f7b4f-1859">属性</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1859">attribute</span></span>  

#### <a name="return-value"></a><span data-ttu-id="f7b4f-1860">戻り値</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1860">Return Value</span></span>

### <a name="method-isabstract"></a><span data-ttu-id="f7b4f-1861">メソッド isAbstract</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1861">Method isAbstract</span></span>

<span data-ttu-id="f7b4f-1862">メソッドが抽象かどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1862">Indicates whether the method is abstract.</span></span>

    public boolean isAbstract()

#### <a name="return-value"></a><span data-ttu-id="f7b4f-1863">戻り値</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1863">Return Value</span></span>

<span data-ttu-id="f7b4f-1864">メソッドが抽象である場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1864">true if the method is abstract; otherwise, false.</span></span>

#### <a name="remarks"></a><span data-ttu-id="f7b4f-1865">備考</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1865">Remarks</span></span>

<span data-ttu-id="f7b4f-1866">抽象メソッドは宣言されていますが、親クラスで実装されていません。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1866">An abstract method is declared but not implemented in a parent class.</span></span> <span data-ttu-id="f7b4f-1867">詳細については、「メソッド モディファイア」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1867">For more information, see Method Modifiers.</span></span>

### <a name="method-isstatic"></a><span data-ttu-id="f7b4f-1868">メソッド isStatic</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1868">Method isStatic</span></span>

<span data-ttu-id="f7b4f-1869">メソッドが静的かどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1869">Specifies whether the method is static.</span></span>

    public boolean isStatic()

#### <a name="return-value"></a><span data-ttu-id="f7b4f-1870">戻り値</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1870">Return Value</span></span>

<span data-ttu-id="f7b4f-1871">メソッドが静的である場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1871">true if the method is static; otherwise, false.</span></span>

#### <a name="remarks"></a><span data-ttu-id="f7b4f-1872">備考</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1872">Remarks</span></span>

<span data-ttu-id="f7b4f-1873">詳細については、「静的メソッド」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1873">For more information, see Static Methods.</span></span>

### <a name="method-name"></a><span data-ttu-id="f7b4f-1874">メソッド名</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1874">Method name</span></span>

<span data-ttu-id="f7b4f-1875">メソッドの名前を指定します。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1875">Specifies the name of a method.</span></span>

    public str name()

#### <a name="return-value"></a><span data-ttu-id="f7b4f-1876">戻り値</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1876">Return Value</span></span>

<span data-ttu-id="f7b4f-1877">メソッド名を示す文字列。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1877">A string that indicates the method name.</span></span>

### <a name="method-noparms"></a><span data-ttu-id="f7b4f-1878">メソッド noParms</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1878">Method noParms</span></span>

<span data-ttu-id="f7b4f-1879">メソッド内のパラメーターの数を指定します。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1879">Specifies the number of parameters in a method.</span></span>

    public int noParms()

#### <a name="return-value"></a><span data-ttu-id="f7b4f-1880">戻り値</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1880">Return Value</span></span>

<span data-ttu-id="f7b4f-1881">メソッド内のパラメータの数を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1881">An integer value that indicates the number of parameters in a method.</span></span>

### <a name="method-novars"></a><span data-ttu-id="f7b4f-1882">メソッド noVars</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1882">Method noVars</span></span>

<span data-ttu-id="f7b4f-1883">メソッド内の変数の数を指定します。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1883">Specifies the number of variables in a method.</span></span>

    public int noVars()

#### <a name="return-value"></a><span data-ttu-id="f7b4f-1884">戻り値</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1884">Return Value</span></span>

<span data-ttu-id="f7b4f-1885">メソッド内の変数の数を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1885">An integer value that indicates the number of variables in a method.</span></span>

### <a name="method-parentid"></a><span data-ttu-id="f7b4f-1886">メソッド parentId</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1886">Method parentId</span></span>

<span data-ttu-id="f7b4f-1887">テーブル メソッドのテーブル ID またはクラス メソッドのクラス ID を指定します。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1887">Specifies the table ID for a table method or the class ID for a class method.</span></span>

    public int parentId()

#### <a name="return-value"></a><span data-ttu-id="f7b4f-1888">戻り値</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1888">Return Value</span></span>

<span data-ttu-id="f7b4f-1889">テーブル ID またはクラス ID を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1889">An integer value that indicates a table ID or a class ID.</span></span>

### <a name="method-propertyhelp"></a><span data-ttu-id="f7b4f-1890">メソッド propertyHelp</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1890">Method propertyHelp</span></span>

<span data-ttu-id="f7b4f-1891">メソッドがコントロールに設定または返すヘルプ テキストを指定します。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1891">Specifies the Help text that a method sets or returns for a control.</span></span>

    public str propertyHelp()

#### <a name="return-value"></a><span data-ttu-id="f7b4f-1892">戻り値</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1892">Return Value</span></span>

<span data-ttu-id="f7b4f-1893">ヘルプ テキストを含む文字列。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1893">A string that contains the Help text.</span></span>

### <a name="method-propertymethod"></a><span data-ttu-id="f7b4f-1894">メソッド PropertyMethod</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1894">Method PropertyMethod</span></span>

<span data-ttu-id="f7b4f-1895">メソッドがプロパティ メソッドかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1895">Specifies whether a method is a property method.</span></span>

    public NoYes PropertyMethod()

#### <a name="return-value"></a><span data-ttu-id="f7b4f-1896">戻り値</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1896">Return Value</span></span>

<span data-ttu-id="f7b4f-1897">メソッドがプロパティ メソッドの場合は 1、それ以外の場合は、0 です。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1897">1 if the method is a property method; otherwise, 0.</span></span>

#### <a name="remarks"></a><span data-ttu-id="f7b4f-1898">備考</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1898">Remarks</span></span>

<span data-ttu-id="f7b4f-1899">プロパティ メソッドは、プロパティを設定または返します。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1899">A property method sets or returns a property.</span></span>

### <a name="method-returnid"></a><span data-ttu-id="f7b4f-1900">メソッド returnId</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1900">Method returnId</span></span>

<span data-ttu-id="f7b4f-1901">値を返すメソッドについて、拡張データ型やクラスなどの特定の戻り値のデータ型の ID を指定します。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1901">Specifies the ID for certain return data types, such as extended data types and classes, for a method that returns a value.</span></span>

    public int returnId()

#### <a name="return-value"></a><span data-ttu-id="f7b4f-1902">戻り値</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1902">Return Value</span></span>

<span data-ttu-id="f7b4f-1903">戻り値のデータ型の ID を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1903">An integer value that indicates the ID for the return data type.</span></span>

#### <a name="remarks"></a><span data-ttu-id="f7b4f-1904">備考</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1904">Remarks</span></span>

<span data-ttu-id="f7b4f-1905">データ型に ID がない場合またはメソッドが値を返さない場合、戻り値は 0 です。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1905">The return value is 0 if the data type does not have an ID or if a method does not return a value.</span></span>

### <a name="method-returntype"></a><span data-ttu-id="f7b4f-1906">メソッド returnType</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1906">Method returnType</span></span>

<span data-ttu-id="f7b4f-1907">メソッドの戻り値の型を指定します。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1907">Specifies a method return type.</span></span>

    public Types returnType()

#### <a name="return-value"></a><span data-ttu-id="f7b4f-1908">戻り値</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1908">Return Value</span></span>

<span data-ttu-id="f7b4f-1909">メソッドの戻り値を示すタイプ列挙値。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1909">A Types enumeration value that indicates a method return type.</span></span>

#### <a name="remarks"></a><span data-ttu-id="f7b4f-1910">備考</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1910">Remarks</span></span>

<span data-ttu-id="f7b4f-1911">表示される値は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1911">The following list indicates the possible values.</span></span> <span data-ttu-id="f7b4f-1912">:</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1912">:</span></span>

-   <span data-ttu-id="f7b4f-1913">AnyType</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1913">AnyType</span></span>
-   <span data-ttu-id="f7b4f-1914">BLOB</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1914">BLOB</span></span>
-   <span data-ttu-id="f7b4f-1915">クラス</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1915">Class</span></span>
-   <span data-ttu-id="f7b4f-1916">コンテナー</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1916">Container</span></span>
-   <span data-ttu-id="f7b4f-1917">日</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1917">Date</span></span>
-   <span data-ttu-id="f7b4f-1918">日時</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1918">DateTime</span></span>
-   <span data-ttu-id="f7b4f-1919">列挙</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1919">Enum</span></span>
-   <span data-ttu-id="f7b4f-1920">グリッド</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1920">Grid</span></span>
-   <span data-ttu-id="f7b4f-1921">Int64</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1921">Int64</span></span>
-   <span data-ttu-id="f7b4f-1922">整数</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1922">Integer</span></span>
-   <span data-ttu-id="f7b4f-1923">実数</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1923">Real</span></span>
-   <span data-ttu-id="f7b4f-1924">レコード</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1924">Record</span></span>
-   <span data-ttu-id="f7b4f-1925">RString</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1925">RString</span></span>
-   <span data-ttu-id="f7b4f-1926">文字列</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1926">String</span></span>
-   <span data-ttu-id="f7b4f-1927">UserType</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1927">UserType</span></span>
-   <span data-ttu-id="f7b4f-1928">VarString</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1928">VarString</span></span>
-   <span data-ttu-id="f7b4f-1929">無効</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1929">void</span></span>

### <a name="method-runmode"></a><span data-ttu-id="f7b4f-1930">メソッド runMode</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1930">Method runMode</span></span>

<span data-ttu-id="f7b4f-1931">メソッドが実行される場所を指定します。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1931">Specifies where a method is executed.</span></span>

    public ClassRunMode runMode()

#### <a name="return-value"></a><span data-ttu-id="f7b4f-1932">戻り値</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1932">Return Value</span></span>

<span data-ttu-id="f7b4f-1933">メソッドが実行される場所を示す ClassRunMode 列挙値。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1933">A ClassRunMode enumeration value that indicates where a method is executed.</span></span>

#### <a name="remarks"></a><span data-ttu-id="f7b4f-1934">備考</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1934">Remarks</span></span>

<span data-ttu-id="f7b4f-1935">表示される値は次のとおりです。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1935">The following list indicates the possible values.</span></span>

-   <span data-ttu-id="f7b4f-1936">呼び出された</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1936">Called</span></span>
-   <span data-ttu-id="f7b4f-1937">クライアント</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1937">Client</span></span>
-   <span data-ttu-id="f7b4f-1938">ClientorServer</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1938">ClientorServer</span></span>
-   <span data-ttu-id="f7b4f-1939">サーバー</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1939">Server</span></span>

### <a name="method-varid"></a><span data-ttu-id="f7b4f-1940">メソッド varId</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1940">Method varId</span></span>

<span data-ttu-id="f7b4f-1941">変数を含むメソッドについて、拡張データ型や列挙値などの特定の変数のデータ型の ID を指定します。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1941">Specifies the ID for certain variable data types, such as extended data types and enums, for a method that contains variables.</span></span>

    public int varId(int variableNumber)

#### <a name="parameters"></a><span data-ttu-id="f7b4f-1942">パラメーター</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1942">Parameters</span></span>

<span data-ttu-id="f7b4f-1943">variableNumber</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1943">variableNumber</span></span>  
<span data-ttu-id="f7b4f-1944">メソッドに一覧表示されている変数の順序に基づいてメソッド変数を指定する整数値。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1944">An integer value that specifies a method variable based on the order of the variables listed in the method.</span></span>

#### <a name="return-value"></a><span data-ttu-id="f7b4f-1945">戻り値</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1945">Return Value</span></span>

<span data-ttu-id="f7b4f-1946">変数のデータ型 ID を示す整数値。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1946">An integer value that indicates the variable data type ID.</span></span>

#### <a name="remarks"></a><span data-ttu-id="f7b4f-1947">備考</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1947">Remarks</span></span>

<span data-ttu-id="f7b4f-1948">データ型に ID がない場合またはメソッドに変数がない場合、戻り値は 0 です。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1948">The return value is 0 if the data type does not have an ID or if a method does not have variables.</span></span>

### <a name="method-varidold"></a><span data-ttu-id="f7b4f-1949">メソッド varIdOld</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1949">Method varIdOld</span></span>

    public int varIdOld(int variableNumber)

#### <a name="parameters"></a><span data-ttu-id="f7b4f-1950">パラメーター</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1950">Parameters</span></span>

<span data-ttu-id="f7b4f-1951">variableNumber</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1951">variableNumber</span></span>  

#### <a name="return-value"></a><span data-ttu-id="f7b4f-1952">戻り値</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1952">Return Value</span></span>

### <a name="method-vartype"></a><span data-ttu-id="f7b4f-1953">メソッド varType</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1953">Method varType</span></span>

<span data-ttu-id="f7b4f-1954">Types 列挙の値を使用して変数のデータ型を指定します。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1954">Specifies a variable data type by using values from the Types enumeration.</span></span>

    public Types varType(int variableNumber)

#### <a name="parameters"></a><span data-ttu-id="f7b4f-1955">パラメーター</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1955">Parameters</span></span>

<span data-ttu-id="f7b4f-1956">variableNumber</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1956">variableNumber</span></span>  
<span data-ttu-id="f7b4f-1957">メソッドに一覧表示されている変数の順序に基づいてメソッド変数を指定する整数。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1957">An integer that specifies a method variable based on the order of the variables listed in the method.</span></span>

#### <a name="return-value"></a><span data-ttu-id="f7b4f-1958">戻り値</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1958">Return Value</span></span>

<span data-ttu-id="f7b4f-1959">変数のデータ型を示すタイプ列挙値。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1959">A Types enumeration value that indicates the variable data type.</span></span>

#### <a name="remarks"></a><span data-ttu-id="f7b4f-1960">備考</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1960">Remarks</span></span>

<span data-ttu-id="f7b4f-1961">以下は使用可能な値です。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1961">Following are the possible values:</span></span>

-   <span data-ttu-id="f7b4f-1962">AnyType</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1962">AnyType</span></span>
-   <span data-ttu-id="f7b4f-1963">BLOB</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1963">BLOB</span></span>
-   <span data-ttu-id="f7b4f-1964">クラス</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1964">Class</span></span>
-   <span data-ttu-id="f7b4f-1965">コンテナー</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1965">Container</span></span>
-   <span data-ttu-id="f7b4f-1966">日</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1966">Date</span></span>
-   <span data-ttu-id="f7b4f-1967">日時</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1967">DateTime</span></span>
-   <span data-ttu-id="f7b4f-1968">列挙</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1968">Enum</span></span>
-   <span data-ttu-id="f7b4f-1969">グリッド</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1969">Grid</span></span>
-   <span data-ttu-id="f7b4f-1970">Int64</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1970">Int64</span></span>
-   <span data-ttu-id="f7b4f-1971">整数</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1971">Integer</span></span>
-   <span data-ttu-id="f7b4f-1972">実数</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1972">Real</span></span>
-   <span data-ttu-id="f7b4f-1973">レコード</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1973">Record</span></span>
-   <span data-ttu-id="f7b4f-1974">RString</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1974">RString</span></span>
-   <span data-ttu-id="f7b4f-1975">文字列</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1975">String</span></span>
-   <span data-ttu-id="f7b4f-1976">UserType</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1976">UserType</span></span>
-   <span data-ttu-id="f7b4f-1977">VarString</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1977">VarString</span></span>
-   <span data-ttu-id="f7b4f-1978">無効</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1978">void</span></span>

### <a name="method-new"></a><span data-ttu-id="f7b4f-1979">メソッド new</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1979">Method new</span></span>

<span data-ttu-id="f7b4f-1980">MethodInfo クラスの新しいインスタンスを作成します。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1980">Creates a new instance of the MethodInfo class.</span></span>

    public void new(UtilElementType utilType, int Id, str Name)

#### <a name="parameters"></a><span data-ttu-id="f7b4f-1981">パラメーター</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1981">Parameters</span></span>

<span data-ttu-id="f7b4f-1982">utilType</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1982">utilType</span></span>  
<span data-ttu-id="f7b4f-1983">要素の名前を指定する文字列。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1983">A string that specifies the name of the element.</span></span>

<!-- -->

<span data-ttu-id="f7b4f-1984">ID</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1984">Id</span></span>  
<span data-ttu-id="f7b4f-1985">要素の名前を指定する文字列。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1985">A string that specifies the name of the element.</span></span>

<!-- -->

<span data-ttu-id="f7b4f-1986">氏名</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1986">Name</span></span>  
<span data-ttu-id="f7b4f-1987">要素の名前を指定する文字列。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1987">A string that specifies the name of the element.</span></span>

### <a name="method-setmethod"></a><span data-ttu-id="f7b4f-1988">メソッド setMethod</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1988">Method setMethod</span></span>

<span data-ttu-id="f7b4f-1989">アプリケーション オブジェクト ツリー (AOT) 内のノードのアプリケーション オブジェクト タイプを指定します。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1989">Specifies the application object type of a node in the Application Object Tree (AOT).</span></span>

    public void setMethod(MemberFunction method)

#### <a name="parameters"></a><span data-ttu-id="f7b4f-1990">パラメーター</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1990">Parameters</span></span>

<span data-ttu-id="f7b4f-1991">メソッド</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1991">method</span></span>  
<span data-ttu-id="f7b4f-1992">AOT 内のノードを表す MemberFunction クラスのインスタンス。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1992">An instance of the MemberFunction class that represents a node in the AOT.</span></span>

## <a name="class-modifyfieldeventargs"></a><span data-ttu-id="f7b4f-1993">クラス ModifyFieldEventArgs</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1993">Class ModifyFieldEventArgs</span></span>
    class ModifyFieldEventArgs extends DataEventArgs

### <a name="remarks"></a><span data-ttu-id="f7b4f-1994">備考</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1994">Remarks</span></span>

### <a name="examples"></a><span data-ttu-id="f7b4f-1995">例</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1995">Examples</span></span>

### <a name="methods"></a><span data-ttu-id="f7b4f-1996">メソッド</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1996">Methods</span></span>

| <span data-ttu-id="f7b4f-1997">方法</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1997">Method</span></span>                       | <span data-ttu-id="f7b4f-1998">説明</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1998">Description</span></span> |
|------------------------------|-------------|
| <span data-ttu-id="f7b4f-1999">public int parmFieldId()</span><span class="sxs-lookup"><span data-stu-id="f7b4f-1999">public int parmFieldId()</span></span>     |             |
| <span data-ttu-id="f7b4f-2000">public void new(int fieldId)</span><span class="sxs-lookup"><span data-stu-id="f7b4f-2000">public void new(int fieldId)</span></span> |             |

### <a name="method-parmfieldid"></a><span data-ttu-id="f7b4f-2001">メソッド parmFieldId</span><span class="sxs-lookup"><span data-stu-id="f7b4f-2001">Method parmFieldId</span></span>

    public int parmFieldId()

#### <a name="return-value"></a><span data-ttu-id="f7b4f-2002">戻り値</span><span class="sxs-lookup"><span data-stu-id="f7b4f-2002">Return Value</span></span>

### <a name="method-new"></a><span data-ttu-id="f7b4f-2003">メソッド new</span><span class="sxs-lookup"><span data-stu-id="f7b4f-2003">Method new</span></span>

    public void new(int fieldId)

#### <a name="parameters"></a><span data-ttu-id="f7b4f-2004">パラメーター</span><span class="sxs-lookup"><span data-stu-id="f7b4f-2004">Parameters</span></span>

<span data-ttu-id="f7b4f-2005">fieldId</span><span class="sxs-lookup"><span data-stu-id="f7b4f-2005">fieldId</span></span>  

## <a name="class-modifyfieldvalueeventargs"></a><span data-ttu-id="f7b4f-2006">クラス ModifyFieldValueEventArgs</span><span class="sxs-lookup"><span data-stu-id="f7b4f-2006">Class ModifyFieldValueEventArgs</span></span>
    class ModifyFieldValueEventArgs extends DataEventArgs

### <a name="remarks"></a><span data-ttu-id="f7b4f-2007">備考</span><span class="sxs-lookup"><span data-stu-id="f7b4f-2007">Remarks</span></span>

### <a name="examples"></a><span data-ttu-id="f7b4f-2008">例</span><span class="sxs-lookup"><span data-stu-id="f7b4f-2008">Examples</span></span>

### <a name="methods"></a><span data-ttu-id="f7b4f-2009">メソッド</span><span class="sxs-lookup"><span data-stu-id="f7b4f-2009">Methods</span></span>

| <span data-ttu-id="f7b4f-2010">方法</span><span class="sxs-lookup"><span data-stu-id="f7b4f-2010">Method</span></span>                                         | <span data-ttu-id="f7b4f-2011">説明</span><span class="sxs-lookup"><span data-stu-id="f7b4f-2011">Description</span></span> |
|------------------------------------------------|-------------|
| <span data-ttu-id="f7b4f-2012">public str parmFieldName()</span><span class="sxs-lookup"><span data-stu-id="f7b4f-2012">public str parmFieldName()</span></span>                     |             |
| <span data-ttu-id="f7b4f-2013">public int parmArrayIndex()</span><span class="sxs-lookup"><span data-stu-id="f7b4f-2013">public int parmArrayIndex()</span></span>                    |             |
| <span data-ttu-id="f7b4f-2014">public void new(str fieldName, int arrayIndex)</span><span class="sxs-lookup"><span data-stu-id="f7b4f-2014">public void new(str fieldName, int arrayIndex)</span></span> |             |

### <a name="method-parmfieldname"></a><span data-ttu-id="f7b4f-2015">メソッド parmFieldName</span><span class="sxs-lookup"><span data-stu-id="f7b4f-2015">Method parmFieldName</span></span>

    public str parmFieldName()

#### <a name="return-value"></a><span data-ttu-id="f7b4f-2016">戻り値</span><span class="sxs-lookup"><span data-stu-id="f7b4f-2016">Return Value</span></span>

### <a name="method-parmarrayindex"></a><span data-ttu-id="f7b4f-2017">メソッド parmArrayIndex</span><span class="sxs-lookup"><span data-stu-id="f7b4f-2017">Method parmArrayIndex</span></span>

    public int parmArrayIndex()

#### <a name="return-value"></a><span data-ttu-id="f7b4f-2018">戻り値</span><span class="sxs-lookup"><span data-stu-id="f7b4f-2018">Return Value</span></span>

### <a name="method-new"></a><span data-ttu-id="f7b4f-2019">メソッド new</span><span class="sxs-lookup"><span data-stu-id="f7b4f-2019">Method new</span></span>

    public void new(str fieldName, int arrayIndex)

#### <a name="parameters"></a><span data-ttu-id="f7b4f-2020">パラメーター</span><span class="sxs-lookup"><span data-stu-id="f7b4f-2020">Parameters</span></span>

<span data-ttu-id="f7b4f-2021">fieldName</span><span class="sxs-lookup"><span data-stu-id="f7b4f-2021">fieldName</span></span>  

<!-- -->

<span data-ttu-id="f7b4f-2022">arrayIndex</span><span class="sxs-lookup"><span data-stu-id="f7b4f-2022">arrayIndex</span></span>  

## <a name="class-multiselectioncontext"></a><span data-ttu-id="f7b4f-2023">クラス MultiSelectionContext</span><span class="sxs-lookup"><span data-stu-id="f7b4f-2023">Class MultiSelectionContext</span></span>
    class MultiSelectionContext extends Object

### <a name="remarks"></a><span data-ttu-id="f7b4f-2024">備考</span><span class="sxs-lookup"><span data-stu-id="f7b4f-2024">Remarks</span></span>

### <a name="examples"></a><span data-ttu-id="f7b4f-2025">例</span><span class="sxs-lookup"><span data-stu-id="f7b4f-2025">Examples</span></span>

### <a name="methods"></a><span data-ttu-id="f7b4f-2026">メソッド</span><span class="sxs-lookup"><span data-stu-id="f7b4f-2026">Methods</span></span>

| <span data-ttu-id="f7b4f-2027">方法</span><span class="sxs-lookup"><span data-stu-id="f7b4f-2027">Method</span></span>                   | <span data-ttu-id="f7b4f-2028">説明</span><span class="sxs-lookup"><span data-stu-id="f7b4f-2028">Description</span></span>                                                    |
|--------------------------|----------------------------------------------------------------|
| <span data-ttu-id="f7b4f-2029">public Common getFirst()</span><span class="sxs-lookup"><span data-stu-id="f7b4f-2029">public Common getFirst()</span></span> |                                                                |
| <span data-ttu-id="f7b4f-2030">public Common getNext()</span><span class="sxs-lookup"><span data-stu-id="f7b4f-2030">public Common getNext()</span></span>  |                                                                |
| <span data-ttu-id="f7b4f-2031">private void new()</span><span class="sxs-lookup"><span data-stu-id="f7b4f-2031">private void new()</span></span>       | <span data-ttu-id="f7b4f-2032">MultiSelectionContext クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-2032">Initializes a new instance of the MultiSelectionContext class.</span></span> |

### <a name="method-getfirst"></a><span data-ttu-id="f7b4f-2033">メソッド getFirst</span><span class="sxs-lookup"><span data-stu-id="f7b4f-2033">Method getFirst</span></span>

    public Common getFirst()

#### <a name="return-value"></a><span data-ttu-id="f7b4f-2034">戻り値</span><span class="sxs-lookup"><span data-stu-id="f7b4f-2034">Return Value</span></span>

### <a name="method-getnext"></a><span data-ttu-id="f7b4f-2035">メソッド getNext</span><span class="sxs-lookup"><span data-stu-id="f7b4f-2035">Method getNext</span></span>

    public Common getNext()

#### <a name="return-value"></a><span data-ttu-id="f7b4f-2036">戻り値</span><span class="sxs-lookup"><span data-stu-id="f7b4f-2036">Return Value</span></span>

### <a name="method-new"></a><span data-ttu-id="f7b4f-2037">メソッド new</span><span class="sxs-lookup"><span data-stu-id="f7b4f-2037">Method new</span></span>

<span data-ttu-id="f7b4f-2038">MultiSelectionContext クラスの新しいインスタンスを初期化します。</span><span class="sxs-lookup"><span data-stu-id="f7b4f-2038">Initializes a new instance of the MultiSelectionContext class.</span></span>

    private void new()




