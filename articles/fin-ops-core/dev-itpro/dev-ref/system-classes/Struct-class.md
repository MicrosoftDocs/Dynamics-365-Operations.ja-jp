---
title: Struct クラス
description: このトピックでは、Struct クラスについて説明します。
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
ms.openlocfilehash: a0bd9b1be951ca89c4e7321869aea256ec6e2e70
ms.sourcegitcommit: 7b0cec2e898ef8ee33baf72f18cdd9cba0e9399c
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/25/2020
ms.locfileid: "3502795"
---
# <a name="class-struct"></a><span data-ttu-id="eb705-103">クラス構造体</span><span class="sxs-lookup"><span data-stu-id="eb705-103">Class Struct</span></span>

[!include [banner](../../includes/banner.md)]

```xpp
class Struct extends Object
```

<span data-ttu-id="eb705-104">構造体は、特定のエンティティに関する情報をグループ化するために、任意の X++ 型の複数値を保持します。</span><span class="sxs-lookup"><span data-stu-id="eb705-104">A struct holds several values of any X++ type, to group the information about a specific entity.</span></span>

## <a name="remarks"></a><span data-ttu-id="eb705-105">備考</span><span class="sxs-lookup"><span data-stu-id="eb705-105">Remarks</span></span>

<span data-ttu-id="eb705-106">構造体 (略構造) は、すべての X++ 型の複数値を保持できるエンティティです。</span><span class="sxs-lookup"><span data-stu-id="eb705-106">A struct (short for structure) is an entity that can hold several values of any X++ type.</span></span> <span data-ttu-id="eb705-107">構造体は、特定のエンティティに関する情報をグループ化するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="eb705-107">Structs are used to group information about a specific entity.</span></span> <span data-ttu-id="eb705-108">たとえば、顧客の名前、年齢、および住所に関する情報を格納し、それからこの複合情報を 1つの項目として扱う場合があります。</span><span class="sxs-lookup"><span data-stu-id="eb705-108">For example, you might want to store information about a customer's name, age and address and then treat this compound information as one item.</span></span> <span data-ttu-id="eb705-109">構造体内の項目は、データ型と名前で指定されます。</span><span class="sxs-lookup"><span data-stu-id="eb705-109">The items in a struct are specified by a data type and a name.</span></span> <span data-ttu-id="eb705-110">項目は、new メソッドを使用して構造体が作成される場合に追加されるか、add メソッドを使用して構造体が作成された後に作成されます。</span><span class="sxs-lookup"><span data-stu-id="eb705-110">Items are added when the struct is created by using the new method, or they are created after the struct has been created by using the add method.</span></span> <span data-ttu-id="eb705-111">Add メソッドを使用して品目を追加する場合は、同時に品目の値を指定し、この値からデータ型が推測されます。</span><span class="sxs-lookup"><span data-stu-id="eb705-111">If you add an item by using the add method, you specify the value for the item at the same time, and the data type is inferred from this value.</span></span> <span data-ttu-id="eb705-112">構造体のインスタンス化中に品目を追加する場合は、値または valueIndex メソッドを使用して、値を割り当てる必要があります。</span><span class="sxs-lookup"><span data-stu-id="eb705-112">If you add an item during the instantiation of the struct, you need to use the value or the valueIndex method to assign a value to it.</span></span> <span data-ttu-id="eb705-113">構造体内の項目は、文字列型、整数型、実数型、日付型、コンテナー型、レコード型、クラス型など、型システムの列挙型にあるデータ型のいずれでもかまいません。</span><span class="sxs-lookup"><span data-stu-id="eb705-113">The items in a struct can be of any of the data types found in the Types system enum, including: string, integer, real, date, container, record, and class.</span></span> <span data-ttu-id="eb705-114">構造体内の項目は、項目名のアルファベット順に並べられます。</span><span class="sxs-lookup"><span data-stu-id="eb705-114">The items in a struct are arranged in alphabetical order of the item names.</span></span> <span data-ttu-id="eb705-115">構造体のフィールドは、fields、fieldName、および fieldType メソッドを使用してスキャンできます。</span><span class="sxs-lookup"><span data-stu-id="eb705-115">The fields in a struct can be traversed by using the fields, fieldName, and fieldType methods.</span></span> <span data-ttu-id="eb705-116">構造体は、コンテナーに梱包し、後で Struct::create メソッドを使用して復元できます。</span><span class="sxs-lookup"><span data-stu-id="eb705-116">Structs can be packed into containers and later restored by using the Struct::create method.</span></span> <span data-ttu-id="eb705-117">構造体には、X++ コンテナーとのいくつかの類似点があります。</span><span class="sxs-lookup"><span data-stu-id="eb705-117">Structs have some similarities to X++ containers.</span></span> <span data-ttu-id="eb705-118">ただし、コンテナーは値の型であり、X++ 言語に組み込まれています。</span><span class="sxs-lookup"><span data-stu-id="eb705-118">However, a container is a value type and is built into the X++ language.</span></span> <span data-ttu-id="eb705-119">入れ子になったコンテナを作成することができますが、入れ子になった構造体は作成することができません。</span><span class="sxs-lookup"><span data-stu-id="eb705-119">You can create nested containers, but you cannot create nested structs.</span></span> <span data-ttu-id="eb705-120">X++ クラスは、構造とほぼ同じ方法で情報を保管することができます。</span><span class="sxs-lookup"><span data-stu-id="eb705-120">X++ classes can store information in much the same way as structs.</span></span> <span data-ttu-id="eb705-121">クラスはデータを操作する方法を供給することができますが、構造体のための該当する機能は提供されておらず、上書きまたは拡張の概念はありません。</span><span class="sxs-lookup"><span data-stu-id="eb705-121">But although classes can supply methods to manipulate the data, no such facility is provided for structs, and there is no concept of overriding or extension.</span></span> <span data-ttu-id="eb705-122">クラスは AOT でのみ作成できますが、構造体は作成されたコードのコンテキスト内にのみ存在します。</span><span class="sxs-lookup"><span data-stu-id="eb705-122">Classes can only be created in the AOT, but structs exist solely in the context of the code in which they are created.</span></span> <span data-ttu-id="eb705-123">クラス メンバーの変数はクラス専用なので、アクセサー関数はクラスの外部から使用される値のためにコード化されている必要があります。</span><span class="sxs-lookup"><span data-stu-id="eb705-123">Class member variables are private to the class, so accessor functions must be coded for them for the values to be used from outside the class.</span></span> <span data-ttu-id="eb705-124">構造体内の項目は一般にアクセス可能です。</span><span class="sxs-lookup"><span data-stu-id="eb705-124">The items within a struct are publicly accessible.</span></span>

## <a name="examples"></a><span data-ttu-id="eb705-125">例</span><span class="sxs-lookup"><span data-stu-id="eb705-125">Examples</span></span>

<span data-ttu-id="eb705-126">次の例では、2 つの項目を含む構造体を作成し、その項目に値を割り当てます。</span><span class="sxs-lookup"><span data-stu-id="eb705-126">The following example creates a struct with two items and then assigns values to those items.</span></span> <span data-ttu-id="eb705-127">Struct.add メソッドを使用して新しい項目が追加されます。項目のデータ型は割り当てられた値から推測されます。</span><span class="sxs-lookup"><span data-stu-id="eb705-127">A new item is then added by using the Struct.add method; the data type of the item is inferred from the value assigned to it.</span></span> <span data-ttu-id="eb705-128">次に、構造体はコンテナーに梱包され、元の構造体のコピーである新しい構造体を作成するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="eb705-128">The struct is then packed into a container and used to create a new struct, a copy of the original struct.</span></span>

```xpp
{ 
    Struct s = new struct ("int age; str name"); 
    Struct copy; 
    container c; 
    int i; 
    // Add values to the items 
    s.value("age", 25); 
    s.value("name", "Jane Dow"); 
  // Add a new item; data type is inferred from value 
    s.add("Shoesize", 45); 
    // Print the definition of the struct 
    print s.definitionString(); 
    // Prints the type and name of all items in the struct 
    for (i =  1;   i <= s.fields();i++) 
    { 
         print s.fieldType(i), " ", s.fieldName(i); 
    }  
    // Pack the struct into a container and restore it into copy 
    c = s.pack(); 
    copy = Struct::create(c); 
    print copy.definitionString(); 
    pause; 
}
```

## <a name="methods"></a><span data-ttu-id="eb705-129">メソッド</span><span class="sxs-lookup"><span data-stu-id="eb705-129">Methods</span></span>

| <span data-ttu-id="eb705-130">方法</span><span class="sxs-lookup"><span data-stu-id="eb705-130">Method</span></span>                                                        | <span data-ttu-id="eb705-131">説明</span><span class="sxs-lookup"><span data-stu-id="eb705-131">Description</span></span>                                                                                   |
|---------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="eb705-132">public boolean add(str fieldName, AnyType value)</span><span class="sxs-lookup"><span data-stu-id="eb705-132">public boolean add(str fieldName, AnyType value)</span></span>              | <span data-ttu-id="eb705-133">構造体に新しい項目を追加し、指定した値を割り当てます。</span><span class="sxs-lookup"><span data-stu-id="eb705-133">Adds a new item to the struct and assigns the specified value to it.</span></span>                          |
| <span data-ttu-id="eb705-134">public str definitionString()</span><span class="sxs-lookup"><span data-stu-id="eb705-134">public str definitionString()</span></span>                                 | <span data-ttu-id="eb705-135">構造体の要素の名前およびタイプの説明を返します。</span><span class="sxs-lookup"><span data-stu-id="eb705-135">Returns a description of the names and types of the elements in the struct.</span></span>                   |
| <span data-ttu-id="eb705-136">public boolean exists(str fieldName)</span><span class="sxs-lookup"><span data-stu-id="eb705-136">public boolean exists(str fieldName)</span></span>                          | <span data-ttu-id="eb705-137">特定の項目が構造体に存在するかどうかを判定します。</span><span class="sxs-lookup"><span data-stu-id="eb705-137">Determines whether a particular item exists in a struct.</span></span>                                      |
| <span data-ttu-id="eb705-138">public str fieldName(int index)</span><span class="sxs-lookup"><span data-stu-id="eb705-138">public str fieldName(int index)</span></span>                               | <span data-ttu-id="eb705-139">指定された位置にある構造体内の項目の名前を返します。</span><span class="sxs-lookup"><span data-stu-id="eb705-139">Returns the name of the item in the struct at the specified position.</span></span>                         |
| <span data-ttu-id="eb705-140">public int fields()</span><span class="sxs-lookup"><span data-stu-id="eb705-140">public int fields()</span></span>                                           | <span data-ttu-id="eb705-141">構造体内の項目の数を返します。</span><span class="sxs-lookup"><span data-stu-id="eb705-141">Returns the number of items in the struct.</span></span>                                                    |
| <span data-ttu-id="eb705-142">public Types fieldType(int index)</span><span class="sxs-lookup"><span data-stu-id="eb705-142">public Types fieldType(int index)</span></span>                             | <span data-ttu-id="eb705-143">指定された位置にある構造体内の項目のデータ型を返します。</span><span class="sxs-lookup"><span data-stu-id="eb705-143">Returns the data type of the item in the struct at the specified position.</span></span>                    |
| <span data-ttu-id="eb705-144">public int index(str fieldName)</span><span class="sxs-lookup"><span data-stu-id="eb705-144">public int index(str fieldName)</span></span>                               | <span data-ttu-id="eb705-145">名前に基づいて構造体の項目の位置を計算します。</span><span class="sxs-lookup"><span data-stu-id="eb705-145">Calculates the position of an item in the struct based on its name.</span></span>                           |
| <span data-ttu-id="eb705-146">public container pack()</span><span class="sxs-lookup"><span data-stu-id="eb705-146">public container pack()</span></span>                                       | <span data-ttu-id="eb705-147">Struct クラスの現在のインスタンスをシリアル化します。</span><span class="sxs-lookup"><span data-stu-id="eb705-147">Serializes the current instance of the Struct class.</span></span>                                          |
| <span data-ttu-id="eb705-148">public boolean remove(str fieldName)</span><span class="sxs-lookup"><span data-stu-id="eb705-148">public boolean remove(str fieldName)</span></span>                          | <span data-ttu-id="eb705-149">構造体から品目を削除します。</span><span class="sxs-lookup"><span data-stu-id="eb705-149">Removes an item from a struct.</span></span>                                                                |
| <span data-ttu-id="eb705-150">public str toString()</span><span class="sxs-lookup"><span data-stu-id="eb705-150">public str toString()</span></span>                                         | <span data-ttu-id="eb705-151">構造体の内容を説明する文字列を返します。</span><span class="sxs-lookup"><span data-stu-id="eb705-151">Returns a string that describes the contents of the struct.</span></span>                                   |
| <span data-ttu-id="eb705-152">public AnyType value(str fieldName, \[AnyType value\])</span><span class="sxs-lookup"><span data-stu-id="eb705-152">public AnyType value(str fieldName, \[AnyType value\])</span></span>        | <span data-ttu-id="eb705-153">構造体で指定される品目の値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="eb705-153">Gets or sets the value for a specified item in a struct.</span></span>                                      |
| <span data-ttu-id="eb705-154">public str valueImage(int index)</span><span class="sxs-lookup"><span data-stu-id="eb705-154">public str valueImage(int index)</span></span>                              | <span data-ttu-id="eb705-155">構造体内の特定の位置にある品目の値を説明する文字列を返します。</span><span class="sxs-lookup"><span data-stu-id="eb705-155">Returns a string that describes the value of the item at a particular position in the struct.</span></span> |
| <span data-ttu-id="eb705-156">public AnyType valueIndex(int index, \[AnyType value\])</span><span class="sxs-lookup"><span data-stu-id="eb705-156">public AnyType valueIndex(int index, \[AnyType value\])</span></span>       | <span data-ttu-id="eb705-157">構造体で指定される位置での品目の値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="eb705-157">Gets or sets the value of the item at a specified position in a struct.</span></span>                       |
| <span data-ttu-id="eb705-158">public str xml(\[int indent\])</span><span class="sxs-lookup"><span data-stu-id="eb705-158">public str xml(\[int indent\])</span></span>                                | <span data-ttu-id="eb705-159">現在のオブジェクトを表す XML 文字列を返します。</span><span class="sxs-lookup"><span data-stu-id="eb705-159">Returns an XML string that represents the current object.</span></span>                                     |
| <span data-ttu-id="eb705-160">::public static Struct create(container container)</span><span class="sxs-lookup"><span data-stu-id="eb705-160">::public static Struct create(container container)</span></span>            | <span data-ttu-id="eb705-161">以前の Struct.pack の呼び出しで取得されたコンテナーから構造体を作成します。</span><span class="sxs-lookup"><span data-stu-id="eb705-161">Creates a struct from a container that is obtained from a prior call to Struct.pack.</span></span>          |
| <span data-ttu-id="eb705-162">::public static Struct createFromXML(Object xmlnode)</span><span class="sxs-lookup"><span data-stu-id="eb705-162">::public static Struct createFromXML(Object xmlnode)</span></span>          |                                                                                               |
| <span data-ttu-id="eb705-163">::public static boolean equal(Struct struct1, Struct struct2)</span><span class="sxs-lookup"><span data-stu-id="eb705-163">::public static boolean equal(Struct struct1, Struct struct2)</span></span> | <span data-ttu-id="eb705-164">2 つの構造体が等しいかどうかを判断します。</span><span class="sxs-lookup"><span data-stu-id="eb705-164">Determines whether two structs are equal.</span></span>                                                     |
| <span data-ttu-id="eb705-165">::public static Struct merge(Struct struct1, Struct struct2)</span><span class="sxs-lookup"><span data-stu-id="eb705-165">::public static Struct merge(Struct struct1, Struct struct2)</span></span>  | <span data-ttu-id="eb705-166">2 つの構造体を組み合わせ、新しい構造体を作成します。</span><span class="sxs-lookup"><span data-stu-id="eb705-166">Combines two structs to create a new struct.</span></span>                                                  |
| <span data-ttu-id="eb705-167">public void new(VarArg specifier)</span><span class="sxs-lookup"><span data-stu-id="eb705-167">public void new(VarArg specifier)</span></span>                             | <span data-ttu-id="eb705-168">構造体を作成します。</span><span class="sxs-lookup"><span data-stu-id="eb705-168">Creates a struct.</span></span>                                                                             |

## <a name="method-add"></a><span data-ttu-id="eb705-169">メソッド add</span><span class="sxs-lookup"><span data-stu-id="eb705-169">Method add</span></span>

<span data-ttu-id="eb705-170">構造体に新しい項目を追加し、指定した値を割り当てます。</span><span class="sxs-lookup"><span data-stu-id="eb705-170">Adds a new item to the struct and assigns the specified value to it.</span></span>

```xpp
public boolean add(str fieldName, AnyType value)
```

### <a name="parameters---add"></a><span data-ttu-id="eb705-171">パラメーター - add</span><span class="sxs-lookup"><span data-stu-id="eb705-171">Parameters - add</span></span>

<span data-ttu-id="eb705-172">fieldName</span><span class="sxs-lookup"><span data-stu-id="eb705-172">fieldName</span></span>  
<span data-ttu-id="eb705-173">新しい項目に割り当てる値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="eb705-173">The value to assign to the new item.</span></span> <span data-ttu-id="eb705-174">この値は、アイテムのタイプを定義します。</span><span class="sxs-lookup"><span data-stu-id="eb705-174">This value defines the type of the item.</span></span>

<!-- -->

<span data-ttu-id="eb705-175">値</span><span class="sxs-lookup"><span data-stu-id="eb705-175">value</span></span>  
<span data-ttu-id="eb705-176">新しい項目に割り当てる値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="eb705-176">The value to assign to the new item.</span></span> <span data-ttu-id="eb705-177">この値は、アイテムのタイプを定義します。</span><span class="sxs-lookup"><span data-stu-id="eb705-177">This value defines the type of the item.</span></span>

### <a name="return-value---add"></a><span data-ttu-id="eb705-178">戻り値 - add</span><span class="sxs-lookup"><span data-stu-id="eb705-178">Return Value - add</span></span>

<span data-ttu-id="eb705-179">値が構造体に追加された場合は true。値を追加することができなかった場合は (既に構造体に存在していた場合は) false。</span><span class="sxs-lookup"><span data-stu-id="eb705-179">true if the value has been added to the struct; false if the value could not be added (if it already existed in the struct).</span></span>

### <a name="remarks---add"></a><span data-ttu-id="eb705-180">備考 - add</span><span class="sxs-lookup"><span data-stu-id="eb705-180">Remarks - add</span></span>

<span data-ttu-id="eb705-181">値のタイプは値の内容から推測されます。</span><span class="sxs-lookup"><span data-stu-id="eb705-181">The type of the value is inferred from content of the value.</span></span> <span data-ttu-id="eb705-182">構造体内の項目は、項目名に従ってアルファベット順に並べられます。</span><span class="sxs-lookup"><span data-stu-id="eb705-182">The items in a struct are arranged in alphabetical order according to the item names.</span></span> <span data-ttu-id="eb705-183">構造体の項目の値は、Struct.value メソッドまたは Struct.valueIndex メソッドを使用して変更できます。</span><span class="sxs-lookup"><span data-stu-id="eb705-183">The value of an item in a struct can be changed by using the Struct.value or the Struct.valueIndex method.</span></span>

### <a name="examples---add"></a><span data-ttu-id="eb705-184">例 - add</span><span class="sxs-lookup"><span data-stu-id="eb705-184">Examples - add</span></span>

<span data-ttu-id="eb705-185">次の例では、名前および年齢フィールドの 2 つの項目を持つ構造体を作成し、それらの項目に値を割り当てます。</span><span class="sxs-lookup"><span data-stu-id="eb705-185">The following example creates a struct with two items name and age fields and assigns values to those items.</span></span> <span data-ttu-id="eb705-186">その後、add メソッドを使用して、43 という値の shoeSize 変数が追加項目として作成されます。</span><span class="sxs-lookup"><span data-stu-id="eb705-186">The add method is then used to create an additional item the shoeSize variable, with a value of 43.</span></span> <span data-ttu-id="eb705-187">値のタイプによって、新しい項目のタイプ int が決まります。</span><span class="sxs-lookup"><span data-stu-id="eb705-187">The type of the value determines the type of the new item, int.</span></span>

```xpp
{ 
    Struct s = new Struct ("str name; int age"); 
    // Prints number of items (2) 
    print s.fields(); 
    // Values are assigned to the two items 
    s.value("name", "John"); 
    s.value("age", 34); 
    //Another item is added to the struct 
    s.add("shoeSize", 43); 
    // Prints number of item (3) 
    print s.fields(); 
    // Prints a description of the items in the struct 
    print s.definitionString(); 
    pause; 
}
```

## <a name="method-definitionstring"></a><span data-ttu-id="eb705-188">メソッド definitionString</span><span class="sxs-lookup"><span data-stu-id="eb705-188">Method definitionString</span></span>

<span data-ttu-id="eb705-189">構造体の要素の名前およびタイプの説明を返します。</span><span class="sxs-lookup"><span data-stu-id="eb705-189">Returns a description of the names and types of the elements in the struct.</span></span>

```xpp
public str definitionString()
```

### <a name="return-value---definitionstring"></a><span data-ttu-id="eb705-190">戻り値 - definitionString</span><span class="sxs-lookup"><span data-stu-id="eb705-190">Return Value - definitionString</span></span>

<span data-ttu-id="eb705-191">構造体の定義を含む文字列。</span><span class="sxs-lookup"><span data-stu-id="eb705-191">A string that contains a definition of the struct.</span></span>

### <a name="remarks---definitionstring"></a><span data-ttu-id="eb705-192">備考 - definitionString</span><span class="sxs-lookup"><span data-stu-id="eb705-192">Remarks - definitionString</span></span>

<span data-ttu-id="eb705-193">definitionString メソッドを使用すると、構文 newStruct = new struct(oldStruct.definitionString()); を用いて構造体のコピーを作成することができます。</span><span class="sxs-lookup"><span data-stu-id="eb705-193">You can use the definitionString method to create a copy of a struct by using the syntax: newStruct = new struct(oldStruct.definitionString());</span></span>

## <a name="method-exists"></a><span data-ttu-id="eb705-194">メソッド exists</span><span class="sxs-lookup"><span data-stu-id="eb705-194">Method exists</span></span>

<span data-ttu-id="eb705-195">特定の項目が構造体に存在するかどうかを判定します。</span><span class="sxs-lookup"><span data-stu-id="eb705-195">Determines whether a particular item exists in a struct.</span></span>

```xpp
public boolean exists(str fieldName)
```

### <a name="parameters---exists"></a><span data-ttu-id="eb705-196">パラメーター - exists</span><span class="sxs-lookup"><span data-stu-id="eb705-196">Parameters - exists</span></span>

<span data-ttu-id="eb705-197">fieldName</span><span class="sxs-lookup"><span data-stu-id="eb705-197">fieldName</span></span>  
<span data-ttu-id="eb705-198">チェックするアイテムの名前。</span><span class="sxs-lookup"><span data-stu-id="eb705-198">The name of the item to check for.</span></span>

### <a name="return-value---exists"></a><span data-ttu-id="eb705-199">戻り値 - exists</span><span class="sxs-lookup"><span data-stu-id="eb705-199">Return Value - exists</span></span>

<span data-ttu-id="eb705-200">項目が構造体内に存在する場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="eb705-200">true if the item exists in the struct; otherwise, false.</span></span>

### <a name="examples---exists"></a><span data-ttu-id="eb705-201">例 - exists</span><span class="sxs-lookup"><span data-stu-id="eb705-201">Examples - exists</span></span>

<span data-ttu-id="eb705-202">次の例では、特定の項目が構造体に存在するかどうかを検査し、存在しない場合は、項目を追加し、Struct.add メソッドを使用して項目に値を割り当てます。</span><span class="sxs-lookup"><span data-stu-id="eb705-202">The following example tests whether a particular item exists in a struct, and if not, it adds the item and assigns a value to it using the Struct.add method.</span></span>

```xpp
client server static void setProp( 
    Struct     properties, 
    str        name, 
    anytype   value 
    ) 
{ 
    if (! properties.exists(name)) 
    { 
        properties.add(name,nullValue(value)); 
    } 
    properties.value(name,value); 
}
```

## <a name="method-fieldname"></a><span data-ttu-id="eb705-203">メソッド fieldName</span><span class="sxs-lookup"><span data-stu-id="eb705-203">Method fieldName</span></span>

<span data-ttu-id="eb705-204">指定された位置にある構造体内の項目の名前を返します。</span><span class="sxs-lookup"><span data-stu-id="eb705-204">Returns the name of the item in the struct at the specified position.</span></span>

```xpp
public str fieldName(int index)
```

### <a name="parameters---fieldname"></a><span data-ttu-id="eb705-205">パラメーター - fieldName</span><span class="sxs-lookup"><span data-stu-id="eb705-205">Parameters - fieldName</span></span>

<span data-ttu-id="eb705-206">指数</span><span class="sxs-lookup"><span data-stu-id="eb705-206">index</span></span>  
<span data-ttu-id="eb705-207">項目名を取得する構造体内の位置。</span><span class="sxs-lookup"><span data-stu-id="eb705-207">The position in the struct at which you want to retrieve the item name.</span></span>

### <a name="return-value---fieldname"></a><span data-ttu-id="eb705-208">戻り値 - fieldName</span><span class="sxs-lookup"><span data-stu-id="eb705-208">Return Value - fieldName</span></span>

<span data-ttu-id="eb705-209">インデックスで指定された位置にある項目の名前。</span><span class="sxs-lookup"><span data-stu-id="eb705-209">The name of the item at the position specified by index.</span></span>

### <a name="remarks---fieldname"></a><span data-ttu-id="eb705-210">備考 - fieldName</span><span class="sxs-lookup"><span data-stu-id="eb705-210">Remarks - fieldName</span></span>

<span data-ttu-id="eb705-211">インデックスが見つからない場合は、空の文字列が返されます。</span><span class="sxs-lookup"><span data-stu-id="eb705-211">If index is not found, an empty string is returned.</span></span>

### <a name="examples---fieldname"></a><span data-ttu-id="eb705-212">例 - fieldName</span><span class="sxs-lookup"><span data-stu-id="eb705-212">Examples - fieldName</span></span>

<span data-ttu-id="eb705-213">次の例では、コンテナーから構造体を作成し、Struct.fields メソッドを使用してコンテナーの内容を反復処理します。</span><span class="sxs-lookup"><span data-stu-id="eb705-213">The following example creates a struct from a container and then uses the Struct.fields method to iterate through the contents of the container.</span></span> <span data-ttu-id="eb705-214">fieldName メソッドは、構造体の各項目の名前をテストするために使用され、この名前の値に応じて特定のアクションが実行されます。</span><span class="sxs-lookup"><span data-stu-id="eb705-214">The fieldName method is used to test the name of each item in the struct, and a specific action is run depending on the value of this name.</span></span>

```xpp
boolean unpack(container packed) 
{ 
    Struct      unpackedProperties; 
    container   structCon; 
    Counter     i; 
    [#currentList,structCon] = packed; 
    unpackedProperties = Struct::create(structCon); 
    for (i=1;i<=unpackedProperties.fields();i++) 
    { 
        switch (unpackedProperties.fieldName(i)) 
        { 
            case #closedOk: 
                break; 
            case #PropertyCaption: 
                if (! dialogForm  
                    || dialogForm  
                    && ! dialogForm.form().design().caption()) 
                    this.caption(unpackedProperties.valueIndex(i)); 
                break; 
            case #dialogFormname: 
                // Do nothing 
                break; 
            case #PropertyAlwaysOnTop: 
                this.alwaysOnTop(unpackedProperties.valueIndex(i)); 
                break; 
            case #PropertyWindowType: 
                this.windowType(unpackedProperties.valueIndex(i)); 
                break; 
            case #defaultButton: 
                this.defaultButton(unpackedProperties.valueIndex(i)); 
                break; 
            default: 
                throw error(strfmt( 
                    "@SYS67326",unpackedProperties.fieldName(i), 
                     classId2Name(classidget(this)))); 
        } 
    } 
    return true; 
}
```

## <a name="method-fields"></a><span data-ttu-id="eb705-215">メソッド fields</span><span class="sxs-lookup"><span data-stu-id="eb705-215">Method fields</span></span>

<span data-ttu-id="eb705-216">構造体内の項目の数を返します。</span><span class="sxs-lookup"><span data-stu-id="eb705-216">Returns the number of items in the struct.</span></span>

```xpp
public int fields()
```

### <a name="return-value---fields"></a><span data-ttu-id="eb705-217">戻り値 - fields</span><span class="sxs-lookup"><span data-stu-id="eb705-217">Return Value - fields</span></span>

<span data-ttu-id="eb705-218">構造体内の項目の数。</span><span class="sxs-lookup"><span data-stu-id="eb705-218">The number of items in the struct.</span></span>

### <a name="remarks---fields"></a><span data-ttu-id="eb705-219">備考 - fields</span><span class="sxs-lookup"><span data-stu-id="eb705-219">Remarks - fields</span></span>

<span data-ttu-id="eb705-220">構造体内の項目の位置を見つけるには、Struct.index メソッドを使用します。</span><span class="sxs-lookup"><span data-stu-id="eb705-220">To find the position of an item in a struct, use the Struct.index method.</span></span>

### <a name="examples---fields"></a><span data-ttu-id="eb705-221">例 - fields</span><span class="sxs-lookup"><span data-stu-id="eb705-221">Examples - fields</span></span>

<span data-ttu-id="eb705-222">次の例では、コンテナーから構造体を作成し、フィールド メソッドを使用してコンテナーの内容を反復処理します。</span><span class="sxs-lookup"><span data-stu-id="eb705-222">The following example creates a struct from a container and then uses the fields method to iterate through the contents of the container.</span></span>

```xpp
boolean unpack(container packed) 
{ 
    Struct      unpackedProperties; 
    container   structCon; 
    Counter     i; 
    [#currentList,structCon] = packed; 
    unpackedProperties = Struct::create(structCon); 
    for (i=1;i<=unpackedProperties.fields();i++) 
    { 
        switch (unpackedProperties.fieldName(i)) 
        { 
            case #closedOk: 
                break; 
            case #PropertyCaption: 
                if (! dialogForm  
                    || dialogForm  
                    && ! dialogForm.form().design().caption()) 
                    this.caption(unpackedProperties.valueIndex(i)); 
                break; 
            case #dialogFormname: 
                // Do nothing 
                break; 
            case #PropertyAlwaysOnTop: 
                this.alwaysOnTop(unpackedProperties.valueIndex(i)); 
                break; 
            case #PropertyWindowType: 
                this.windowType(unpackedProperties.valueIndex(i)); 
                break; 
            case #defaultButton: 
                this.defaultButton(unpackedProperties.valueIndex(i)); 
                break; 
            default: 
                throw error(strfmt( 
                    "@SYS67326",unpackedProperties.fieldName(i), 
                     classId2Name(classidget(this)))); 
        } 
    } 
    return true; 
}
```

## <a name="method-fieldtype"></a><span data-ttu-id="eb705-223">メソッド fieldType</span><span class="sxs-lookup"><span data-stu-id="eb705-223">Method fieldType</span></span>

<span data-ttu-id="eb705-224">指定された位置にある構造体内の項目のデータ型を返します。</span><span class="sxs-lookup"><span data-stu-id="eb705-224">Returns the data type of the item in the struct at the specified position.</span></span>

```xpp
public Types fieldType(int index)
```

### <a name="parameters---fieldtype"></a><span data-ttu-id="eb705-225">パラメーター - fieldType</span><span class="sxs-lookup"><span data-stu-id="eb705-225">Parameters - fieldType</span></span>

<span data-ttu-id="eb705-226">指数</span><span class="sxs-lookup"><span data-stu-id="eb705-226">index</span></span>  
<span data-ttu-id="eb705-227">データ型を取得する構造体内の位置。</span><span class="sxs-lookup"><span data-stu-id="eb705-227">The position in the struct that you want to retrieve the data type for.</span></span>

### <a name="return-value---fieldtype"></a><span data-ttu-id="eb705-228">戻り値 - fieldType</span><span class="sxs-lookup"><span data-stu-id="eb705-228">Return Value - fieldType</span></span>

<span data-ttu-id="eb705-229">インデックスで指定された位置にある項目のデータ型。</span><span class="sxs-lookup"><span data-stu-id="eb705-229">The data type of the item at the position specified by index.</span></span>

### <a name="remarks---fieldtype"></a><span data-ttu-id="eb705-230">備考 - fieldType</span><span class="sxs-lookup"><span data-stu-id="eb705-230">Remarks - fieldType</span></span>

<span data-ttu-id="eb705-231">可能な値は、システム列挙で提供されます。</span><span class="sxs-lookup"><span data-stu-id="eb705-231">The possible values are supplied by the system enum.</span></span> <span data-ttu-id="eb705-232">インデックスが見つからない場合は、返す値は Types::void です。</span><span class="sxs-lookup"><span data-stu-id="eb705-232">If index is not found, the return value is Types::void.</span></span> <span data-ttu-id="eb705-233">Struct.index メソッドを使用することにより、構造体内の特定の品目の位置を決定することができます。</span><span class="sxs-lookup"><span data-stu-id="eb705-233">You can determine the position of a particular item in a struct by using the Struct.index method</span></span>

## <a name="method-index"></a><span data-ttu-id="eb705-234">メソッド index</span><span class="sxs-lookup"><span data-stu-id="eb705-234">Method index</span></span>

<span data-ttu-id="eb705-235">名前に基づいて構造体の項目の位置を計算します。</span><span class="sxs-lookup"><span data-stu-id="eb705-235">Calculates the position of an item in the struct based on its name.</span></span>

```xpp
public int index(str fieldName)
```

### <a name="parameters---index"></a><span data-ttu-id="eb705-236">パラメーター - index</span><span class="sxs-lookup"><span data-stu-id="eb705-236">Parameters - index</span></span>

<span data-ttu-id="eb705-237">fieldName</span><span class="sxs-lookup"><span data-stu-id="eb705-237">fieldName</span></span>  
<span data-ttu-id="eb705-238">位置を返す項目の名前。</span><span class="sxs-lookup"><span data-stu-id="eb705-238">The name of the item for which to return the position.</span></span>

### <a name="return-value---index"></a><span data-ttu-id="eb705-239">戻り値 - index</span><span class="sxs-lookup"><span data-stu-id="eb705-239">Return Value - index</span></span>

<span data-ttu-id="eb705-240">項目の位置。</span><span class="sxs-lookup"><span data-stu-id="eb705-240">The position of the item.</span></span>

### <a name="remarks---index"></a><span data-ttu-id="eb705-241">備考 - index</span><span class="sxs-lookup"><span data-stu-id="eb705-241">Remarks - index</span></span>

<span data-ttu-id="eb705-242">構造体内の項目は、項目名に従ってアルファベット順に並べられます。</span><span class="sxs-lookup"><span data-stu-id="eb705-242">The items in a struct are arranged in alphabetical order according to the item names.</span></span> <span data-ttu-id="eb705-243">fieldName という名前の項目がない場合は、0 が返されます。</span><span class="sxs-lookup"><span data-stu-id="eb705-243">If there is no item with the name fieldName, 0 is returned.</span></span>

## <a name="method-pack"></a><span data-ttu-id="eb705-244">メソッド pack</span><span class="sxs-lookup"><span data-stu-id="eb705-244">Method pack</span></span>

<span data-ttu-id="eb705-245">Struct クラスの現在のインスタンスをシリアル化します。</span><span class="sxs-lookup"><span data-stu-id="eb705-245">Serializes the current instance of the Struct class.</span></span>

```xpp
public container pack()
```

### <a name="return-value---pack"></a><span data-ttu-id="eb705-246">戻り値 - pack</span><span class="sxs-lookup"><span data-stu-id="eb705-246">Return Value - pack</span></span>

<span data-ttu-id="eb705-247">Struct クラスの現在のインスタンスを含むコンテナーです。</span><span class="sxs-lookup"><span data-stu-id="eb705-247">A container that contains the current instance of the Struct class.</span></span>

### <a name="remarks---pack"></a><span data-ttu-id="eb705-248">備考 - pack</span><span class="sxs-lookup"><span data-stu-id="eb705-248">Remarks - pack</span></span>

<span data-ttu-id="eb705-249">pack メソッドは、オブジェクトを保持する各フィールドで呼び出され、(サブ) コンテナーを生成します。</span><span class="sxs-lookup"><span data-stu-id="eb705-249">The pack method is called on each field that holds an object, to yield a (sub) container.</span></span> <span data-ttu-id="eb705-250">構造体は、Struct.create メソッドを使用してコンテナーから再作成できます。</span><span class="sxs-lookup"><span data-stu-id="eb705-250">The struct may be recreated from the container by using the Struct.create method.</span></span>

### <a name="examples---pack"></a><span data-ttu-id="eb705-251">例 - pack</span><span class="sxs-lookup"><span data-stu-id="eb705-251">Examples - pack</span></span>

<span data-ttu-id="eb705-252">次の例では、2 つの項目 (名前と年齢) を持つ構造体を作成し、項目に値を追加します。</span><span class="sxs-lookup"><span data-stu-id="eb705-252">The following example creates a struct with two items in it (name and age), and then adds values to the items.</span></span> <span data-ttu-id="eb705-253">構造体はコンテナーに梱包され、このコンテナーが使用されて新しい構造体が作成されます。</span><span class="sxs-lookup"><span data-stu-id="eb705-253">The struct is packed into a container, and this container is then used to create a new struct.</span></span>

```xpp
{  
    container packedStruct;  
    Struct s1, s = new Struct ("str name; int age"); 
    s.value ("name", "Jane Dow");  
    s.value ("age", 34); 
    // Struct is packed into a container 
    packedStruct = s.pack();  
    // A new struct is created from the container 
    s1 = Struct::create(packedStruct); 
    // Both structs have the same contents 
    print s.toString();  
    print s1.toString();  
    pause;  
}
```

## <a name="method-remove"></a><span data-ttu-id="eb705-254">メソッド remove</span><span class="sxs-lookup"><span data-stu-id="eb705-254">Method remove</span></span>

<span data-ttu-id="eb705-255">構造体から品目を削除します。</span><span class="sxs-lookup"><span data-stu-id="eb705-255">Removes an item from a struct.</span></span>

```xpp
public boolean remove(str fieldName)
```

### <a name="parameters---remove"></a><span data-ttu-id="eb705-256">パラメーター - remove</span><span class="sxs-lookup"><span data-stu-id="eb705-256">Parameters - remove</span></span>

<span data-ttu-id="eb705-257">fieldName</span><span class="sxs-lookup"><span data-stu-id="eb705-257">fieldName</span></span>  
<span data-ttu-id="eb705-258">削除する項目の名前。</span><span class="sxs-lookup"><span data-stu-id="eb705-258">The name of the item you want to remove.</span></span>

### <a name="return-value---remove"></a><span data-ttu-id="eb705-259">戻り値 - remove</span><span class="sxs-lookup"><span data-stu-id="eb705-259">Return Value - remove</span></span>

<span data-ttu-id="eb705-260">項目が見つかった (そして削除された) 場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="eb705-260">true if the item was found (and removed); otherwise, false.</span></span>

### <a name="remarks---remove"></a><span data-ttu-id="eb705-261">備考 - remove</span><span class="sxs-lookup"><span data-stu-id="eb705-261">Remarks - remove</span></span>

<span data-ttu-id="eb705-262">fieldName パラメーターに指定する名前は、構造体のインスタンス化で指定されたアイテムの名前または Struct.add メソッドを使用して追加されたアイテムの名前でなければなりません。</span><span class="sxs-lookup"><span data-stu-id="eb705-262">The name you specify for the fieldName parameter must be the name of the item as it was specified in the instantiation of the struct or the name of the item as it was added using the Struct.add method.</span></span> <span data-ttu-id="eb705-263">名前は引用符 (" ") で囲む必要があります。</span><span class="sxs-lookup"><span data-stu-id="eb705-263">The name must be enclosed in quotes (" ").</span></span>

### <a name="examples---remove"></a><span data-ttu-id="eb705-264">例 - remove</span><span class="sxs-lookup"><span data-stu-id="eb705-264">Examples - remove</span></span>

<span data-ttu-id="eb705-265">次の例では、2 つの項目を含む構造体を作成し、これらの項目の説明を出力します。</span><span class="sxs-lookup"><span data-stu-id="eb705-265">The following example creates a struct with two items in it and prints a description of these items.</span></span> <span data-ttu-id="eb705-266">品目のいずれかは、メソッドの削除を使用して削除されます。</span><span class="sxs-lookup"><span data-stu-id="eb705-266">One of the items is then removed by using the remove method.</span></span>

```xpp
{ 
    Struct s = new Struct ("str name; int age"); 
    // Values are assigned to the two items 
    s.value("name", "John"); 
    s.value("age", 34); 
    // Prints a description of the items in the struct 
    print s.definitionString(); 
    pause; 
    // Removes the name field 
    s.remove("name"); 
    // Describes remaining items in the struct 
    print s.definitionString(); 
    pause; 
}
```

## <a name="method-tostring"></a><span data-ttu-id="eb705-267">メソッド toString</span><span class="sxs-lookup"><span data-stu-id="eb705-267">Method toString</span></span>

<span data-ttu-id="eb705-268">構造体の内容を説明する文字列を返します。</span><span class="sxs-lookup"><span data-stu-id="eb705-268">Returns a string that describes the contents of the struct.</span></span>

```xpp
public str toString()
```

### <a name="return-value---tostring"></a><span data-ttu-id="eb705-269">戻り値 - toString</span><span class="sxs-lookup"><span data-stu-id="eb705-269">Return Value - toString</span></span>

<span data-ttu-id="eb705-270">構造体の内容を説明する文字列。</span><span class="sxs-lookup"><span data-stu-id="eb705-270">A string that describes the contents of the struct.</span></span>

## <a name="method-value"></a><span data-ttu-id="eb705-271">メソッド value</span><span class="sxs-lookup"><span data-stu-id="eb705-271">Method value</span></span>

<span data-ttu-id="eb705-272">構造体で指定される品目の値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="eb705-272">Gets or sets the value for a specified item in a struct.</span></span>

```xpp
public AnyType value(str fieldName, [AnyType value])
```

### <a name="parameters---value"></a><span data-ttu-id="eb705-273">パラメーター - value</span><span class="sxs-lookup"><span data-stu-id="eb705-273">Parameters - value</span></span>

<span data-ttu-id="eb705-274">fieldName</span><span class="sxs-lookup"><span data-stu-id="eb705-274">fieldName</span></span>  
<span data-ttu-id="eb705-275">項目に割り当てる値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="eb705-275">The value to assign to the item; optional.</span></span>

<!-- -->

<span data-ttu-id="eb705-276">値</span><span class="sxs-lookup"><span data-stu-id="eb705-276">value</span></span>  
<span data-ttu-id="eb705-277">項目に割り当てる値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="eb705-277">The value to assign to the item; optional.</span></span>

### <a name="return-value---value"></a><span data-ttu-id="eb705-278">戻り値 - value</span><span class="sxs-lookup"><span data-stu-id="eb705-278">Return Value - value</span></span>

<span data-ttu-id="eb705-279">指定項目の値。</span><span class="sxs-lookup"><span data-stu-id="eb705-279">The value of the specified item.</span></span>

### <a name="remarks---value"></a><span data-ttu-id="eb705-280">備考 - value</span><span class="sxs-lookup"><span data-stu-id="eb705-280">Remarks - value</span></span>

<span data-ttu-id="eb705-281">構造体内で指定された名前に項目がない場合は例外が発生します。</span><span class="sxs-lookup"><span data-stu-id="eb705-281">An exception is raised if there is no item with the specified name in the struct.</span></span> <span data-ttu-id="eb705-282">構造体内の項目名は、Struct.fieldName メソッドを使用して取得できます。</span><span class="sxs-lookup"><span data-stu-id="eb705-282">The name of an item in a struct may be retrieved by using the Struct.fieldName method.</span></span> <span data-ttu-id="eb705-283">Struct.add メソッドを使用することにより、新しい品目を構造体に追加すると同時に値を割り当てることができます。</span><span class="sxs-lookup"><span data-stu-id="eb705-283">You can add a new item to a struct and assign a value to it at the same time by using the Struct.add method.</span></span> <span data-ttu-id="eb705-284">構造体内の位置に基づいてアイテムに新しい値を割り当てるには、Struct.valueIndex メソッドを使用します。</span><span class="sxs-lookup"><span data-stu-id="eb705-284">To assign a new value to an item based on its position in the struct, use the Struct.valueIndex method.</span></span>

### <a name="examples---value"></a><span data-ttu-id="eb705-285">例 - value</span><span class="sxs-lookup"><span data-stu-id="eb705-285">Examples - value</span></span>

<span data-ttu-id="eb705-286">次の例では、2 つの項目を含む構造体を作成し、value メソッドを使用してこれらの 2 つの項目に値を割り当てます。</span><span class="sxs-lookup"><span data-stu-id="eb705-286">The following example creates a struct with two items in it and then uses the value method to assign values to those two items.</span></span>

```xpp
{ 
    Struct s = new Struct ("str name; int age"); 
    // Set the values 
    s.value("name", "Jane Dow"); 
    s.value("age", 34); 
    // Print the values 
    print s.value("name"); 
    print s.value("age"); 
    pause; 
}
```

## <a name="method-valueimage"></a><span data-ttu-id="eb705-287">メソッド valueImage</span><span class="sxs-lookup"><span data-stu-id="eb705-287">Method valueImage</span></span>

<span data-ttu-id="eb705-288">構造体内の特定の位置にある品目の値を説明する文字列を返します。</span><span class="sxs-lookup"><span data-stu-id="eb705-288">Returns a string that describes the value of the item at a particular position in the struct.</span></span>

```xpp
public str valueImage(int index)
```

### <a name="parameters---valueimage"></a><span data-ttu-id="eb705-289">パラメーター - valueImage</span><span class="sxs-lookup"><span data-stu-id="eb705-289">Parameters - valueImage</span></span>

<span data-ttu-id="eb705-290">指数</span><span class="sxs-lookup"><span data-stu-id="eb705-290">index</span></span>  
<span data-ttu-id="eb705-291">説明を返す項目の位置。</span><span class="sxs-lookup"><span data-stu-id="eb705-291">The position of the item that you want to return a description for.</span></span>

### <a name="return-value---valueimage"></a><span data-ttu-id="eb705-292">戻り値 - valueImage</span><span class="sxs-lookup"><span data-stu-id="eb705-292">Return Value - valueImage</span></span>

<span data-ttu-id="eb705-293">品目の価値を説明する文字列。</span><span class="sxs-lookup"><span data-stu-id="eb705-293">A string that describes the value of the item.</span></span>

### <a name="remarks---valueimage"></a><span data-ttu-id="eb705-294">備考 - valueImage</span><span class="sxs-lookup"><span data-stu-id="eb705-294">Remarks - valueImage</span></span>

<span data-ttu-id="eb705-295">構造体内の項目は、項目の名前に従ってアルファベット順に表示されます。</span><span class="sxs-lookup"><span data-stu-id="eb705-295">The items in a struct are in alphabetical order according to the names of the items.</span></span> <span data-ttu-id="eb705-296">インデックスで指定された位置に項目がない場合は例外が発生します。</span><span class="sxs-lookup"><span data-stu-id="eb705-296">If there is no item at the position specified by index, an exception is raised.</span></span>

## <a name="method-valueindex"></a><span data-ttu-id="eb705-297">メソッド valueIndex</span><span class="sxs-lookup"><span data-stu-id="eb705-297">Method valueIndex</span></span>

<span data-ttu-id="eb705-298">構造体で指定される位置での品目の値を取得または設定します。</span><span class="sxs-lookup"><span data-stu-id="eb705-298">Gets or sets the value of the item at a specified position in a struct.</span></span>

```xpp
public AnyType valueIndex(int index, [AnyType value])
```

### <a name="parameters---valueindex"></a><span data-ttu-id="eb705-299">パラメーター - valueIndex</span><span class="sxs-lookup"><span data-stu-id="eb705-299">Parameters - valueIndex</span></span>

<span data-ttu-id="eb705-300">指数</span><span class="sxs-lookup"><span data-stu-id="eb705-300">index</span></span>  
<span data-ttu-id="eb705-301">インデックスで指定された位置のアイテムに割り当てる値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="eb705-301">The value to assign to the item at the position specified by index; optional.</span></span>

<!-- -->

<span data-ttu-id="eb705-302">値</span><span class="sxs-lookup"><span data-stu-id="eb705-302">value</span></span>  
<span data-ttu-id="eb705-303">インデックスで指定された位置のアイテムに割り当てる値 (オプション)。</span><span class="sxs-lookup"><span data-stu-id="eb705-303">The value to assign to the item at the position specified by index; optional.</span></span>

### <a name="return-value---valueindex"></a><span data-ttu-id="eb705-304">戻り値 - valueIndex</span><span class="sxs-lookup"><span data-stu-id="eb705-304">Return Value - valueIndex</span></span>

<span data-ttu-id="eb705-305">インデックスで指定された位置にある項目の値。</span><span class="sxs-lookup"><span data-stu-id="eb705-305">The value of the item at the position specified by index.</span></span>

### <a name="remarks---valueindex"></a><span data-ttu-id="eb705-306">備考 - valueIndex</span><span class="sxs-lookup"><span data-stu-id="eb705-306">Remarks - valueIndex</span></span>

<span data-ttu-id="eb705-307">インデックスで指定された位置に項目がない場合は例外が発生します。</span><span class="sxs-lookup"><span data-stu-id="eb705-307">An exception is raised if there is no item at the position specified by index.</span></span> <span data-ttu-id="eb705-308">構造体内の項目の位置は、Struct.index メソッドを使用して取得できます。</span><span class="sxs-lookup"><span data-stu-id="eb705-308">The position of an item in a struct can be retrieved by using the Struct.index method.</span></span>

## <a name="method-xml"></a><span data-ttu-id="eb705-309">メソッド xml</span><span class="sxs-lookup"><span data-stu-id="eb705-309">Method xml</span></span>

<span data-ttu-id="eb705-310">現在のオブジェクトを表す XML 文字列を返します。</span><span class="sxs-lookup"><span data-stu-id="eb705-310">Returns an XML string that represents the current object.</span></span>

```xpp
public str xml([int indent])
```

### <a name="parameters---xml"></a><span data-ttu-id="eb705-311">パラメーター - xml</span><span class="sxs-lookup"><span data-stu-id="eb705-311">Parameters - xml</span></span>

<span data-ttu-id="eb705-312">インデント</span><span class="sxs-lookup"><span data-stu-id="eb705-312">indent</span></span>  
<span data-ttu-id="eb705-313">返された XML 文字列のインデントの量 (省略可能)。</span><span class="sxs-lookup"><span data-stu-id="eb705-313">The amount of indentation of the returned XML string; optional.</span></span>

### <a name="return-value---xml"></a><span data-ttu-id="eb705-314">戻り値 - xml</span><span class="sxs-lookup"><span data-stu-id="eb705-314">Return Value - xml</span></span>

<span data-ttu-id="eb705-315">現在のオブジェクトを表す XML 文字列です。</span><span class="sxs-lookup"><span data-stu-id="eb705-315">An XML string that represents the current object.</span></span>

### <a name="remarks---xml"></a><span data-ttu-id="eb705-316">備考 - xml</span><span class="sxs-lookup"><span data-stu-id="eb705-316">Remarks - xml</span></span>

<span data-ttu-id="eb705-317">このメソッドをオーバーライドして、その型に対して意味のある値を返すことができます。</span><span class="sxs-lookup"><span data-stu-id="eb705-317">This method can be overridden to return values that are meaningful for that type.</span></span>

## <a name="method-create"></a><span data-ttu-id="eb705-318">メソッド create</span><span class="sxs-lookup"><span data-stu-id="eb705-318">Method create</span></span>

<span data-ttu-id="eb705-319">以前の Struct.pack の呼び出しで取得されたコンテナーから構造体を作成します。</span><span class="sxs-lookup"><span data-stu-id="eb705-319">Creates a struct from a container that is obtained from a prior call to Struct.pack.</span></span>

```xpp
public static Struct create(container container)
```

### <a name="parameters---create"></a><span data-ttu-id="eb705-320">パラメーター - create</span><span class="sxs-lookup"><span data-stu-id="eb705-320">Parameters - create</span></span>

<span data-ttu-id="eb705-321">コンテナー</span><span class="sxs-lookup"><span data-stu-id="eb705-321">container</span></span>  
<span data-ttu-id="eb705-322">梱包済みの構造体を含むコンテナーです。</span><span class="sxs-lookup"><span data-stu-id="eb705-322">A container that contains the packed struct.</span></span>

### <a name="return-value---create"></a><span data-ttu-id="eb705-323">戻り値 - create</span><span class="sxs-lookup"><span data-stu-id="eb705-323">Return Value - create</span></span>

<span data-ttu-id="eb705-324">特定のコンテナーに梱包されたものと同じ構造体。</span><span class="sxs-lookup"><span data-stu-id="eb705-324">A struct equal to the one that was packed into the specified container.</span></span>

### <a name="remarks---create"></a><span data-ttu-id="eb705-325">備考 - create</span><span class="sxs-lookup"><span data-stu-id="eb705-325">Remarks - create</span></span>

<span data-ttu-id="eb705-326">構造体にオブジェクトが含まれている場合、これらのオブジェクトにはコンテナーからその内部状態を再設定するために呼び出されるアンパック メソッドが必要です。</span><span class="sxs-lookup"><span data-stu-id="eb705-326">If the struct contains objects, these objects must have an unpack method that is called to re-establish their internal state from the container.</span></span>

### <a name="examples---create"></a><span data-ttu-id="eb705-327">例 - create</span><span class="sxs-lookup"><span data-stu-id="eb705-327">Examples - create</span></span>

<span data-ttu-id="eb705-328">次の例では、2 つの項目 (名前と年齢) を持つ構造体を作成し、項目に値を追加します。</span><span class="sxs-lookup"><span data-stu-id="eb705-328">The following example creates a struct with two items in it (name and age), and then adds values to the items.</span></span> <span data-ttu-id="eb705-329">構造体はコンテナーに梱包され、このコンテナーは開梱されて新しい構造体が作成されます。</span><span class="sxs-lookup"><span data-stu-id="eb705-329">The struct is packed into a container, and this container is then unpacked to create a new struct.</span></span>

```xpp
{  
    container packedStruct;  
    Struct s1, s = new Struct ("str name; int age"); 
    s.value ("name", "Jane Dow");  
    s.value ("age", 34); 
    // Struct is packed into a container 
    packedStruct = s.pack();  
    // A new struct is created from the container 
    s1 = Struct::create(packedStruct); 
    // Both structs have the same contents 
    print s.toString();  
    print s1.toString();  
    pause;  
}
```

## <a name="method-createfromxml"></a><span data-ttu-id="eb705-330">メソッド createFromXML</span><span class="sxs-lookup"><span data-stu-id="eb705-330">Method createFromXML</span></span>

```xpp
public static Struct createFromXML(Object xmlnode)
```

### <a name="parameters---createfromxml"></a><span data-ttu-id="eb705-331">パラメータ - createFromXML</span><span class="sxs-lookup"><span data-stu-id="eb705-331">Parameters - createFromXML</span></span>

<span data-ttu-id="eb705-332">xmlnode</span><span class="sxs-lookup"><span data-stu-id="eb705-332">xmlnode</span></span>  

### <a name="return-value---createfromxml"></a><span data-ttu-id="eb705-333">戻り値 - createFromXML</span><span class="sxs-lookup"><span data-stu-id="eb705-333">Return Value - createFromXML</span></span>

## <a name="method-equal"></a><span data-ttu-id="eb705-334">メソッド equal</span><span class="sxs-lookup"><span data-stu-id="eb705-334">Method equal</span></span>

<span data-ttu-id="eb705-335">2 つの構造体が等しいかどうかを判断します。</span><span class="sxs-lookup"><span data-stu-id="eb705-335">Determines whether two structs are equal.</span></span>

```xpp
public static boolean equal(Struct struct1, Struct struct2)
```

### <a name="parameters---equal"></a><span data-ttu-id="eb705-336">パラメーター - equal</span><span class="sxs-lookup"><span data-stu-id="eb705-336">Parameters - equal</span></span>

<span data-ttu-id="eb705-337">struct1</span><span class="sxs-lookup"><span data-stu-id="eb705-337">struct1</span></span>  
<span data-ttu-id="eb705-338">比較される 2 つの構造体のうちの 2 番目の構造体。</span><span class="sxs-lookup"><span data-stu-id="eb705-338">The second of the two structs to be compared.</span></span>

<!-- -->

<span data-ttu-id="eb705-339">struct2</span><span class="sxs-lookup"><span data-stu-id="eb705-339">struct2</span></span>  
<span data-ttu-id="eb705-340">比較される 2 つの構造体のうちの 2 番目の構造体。</span><span class="sxs-lookup"><span data-stu-id="eb705-340">The second of the two structs to be compared.</span></span>

### <a name="return-value---equal"></a><span data-ttu-id="eb705-341">戻り値 - equal</span><span class="sxs-lookup"><span data-stu-id="eb705-341">Return Value - equal</span></span>

<span data-ttu-id="eb705-342">構造体が等しい場合は true。それ以外の場合は、false。</span><span class="sxs-lookup"><span data-stu-id="eb705-342">true if the structs are equal; otherwise, false.</span></span>

### <a name="remarks---equal"></a><span data-ttu-id="eb705-343">備考 - equal</span><span class="sxs-lookup"><span data-stu-id="eb705-343">Remarks - equal</span></span>

<span data-ttu-id="eb705-344">同じ数のフィールドを持ち、フィールド名が同じで、各フィールドが同じ型で同じ値を持つ場合、2 つの構造体は同等です。</span><span class="sxs-lookup"><span data-stu-id="eb705-344">Two structs are equal if they have the same number of fields, the field names are the same, and each field is the same type and has the same value.</span></span>

## <a name="method-merge"></a><span data-ttu-id="eb705-345">メソッド merge</span><span class="sxs-lookup"><span data-stu-id="eb705-345">Method merge</span></span>

<span data-ttu-id="eb705-346">2 つの構造体を組み合わせ、新しい構造体を作成します。</span><span class="sxs-lookup"><span data-stu-id="eb705-346">Combines two structs to create a new struct.</span></span>

```xpp
public static Struct merge(Struct struct1, Struct struct2)
```

### <a name="parameters---merge"></a><span data-ttu-id="eb705-347">パラメーター - merge</span><span class="sxs-lookup"><span data-stu-id="eb705-347">Parameters - merge</span></span>

<span data-ttu-id="eb705-348">struct1</span><span class="sxs-lookup"><span data-stu-id="eb705-348">struct1</span></span>  
<span data-ttu-id="eb705-349">新しい構造体を作成するために最初の構造体の最後に追加される構造体。</span><span class="sxs-lookup"><span data-stu-id="eb705-349">The struct that will be added to the end of the first struct to create a new struct.</span></span>

<!-- -->

<span data-ttu-id="eb705-350">struct2</span><span class="sxs-lookup"><span data-stu-id="eb705-350">struct2</span></span>  
<span data-ttu-id="eb705-351">新しい構造体を作成するために最初の構造体の最後に追加される構造体。</span><span class="sxs-lookup"><span data-stu-id="eb705-351">The struct that will be added to the end of the first struct to create a new struct.</span></span>

### <a name="return-value---merge"></a><span data-ttu-id="eb705-352">戻り値 - merge</span><span class="sxs-lookup"><span data-stu-id="eb705-352">Return Value - merge</span></span>

<span data-ttu-id="eb705-353">新しい構造体。</span><span class="sxs-lookup"><span data-stu-id="eb705-353">The new struct.</span></span>

### <a name="remarks---merge"></a><span data-ttu-id="eb705-354">備考 - merge</span><span class="sxs-lookup"><span data-stu-id="eb705-354">Remarks - merge</span></span>

<span data-ttu-id="eb705-355">struct2 は struct1 の最後に追加されます。</span><span class="sxs-lookup"><span data-stu-id="eb705-355">struct2 is added to the end of struct1.</span></span> <span data-ttu-id="eb705-356">つまり、新しい構造体の項目の順序は、項目名のアルファベット順に並べられた struct1 のすべての項目と、項目名のアルファベット順に並べられた struct2 のすべての項目です。</span><span class="sxs-lookup"><span data-stu-id="eb705-356">This means that the order of the items in the new struct will be: all the items in struct1, arranged in alphabetical order of the item names, followed by all the items in struct2, arranged in alphabetical order of the item names.</span></span> <span data-ttu-id="eb705-357">両方の構造体に同じ名前を持つ品目が含まれている場合は、最初の構造体からの品目のみが含まれるようになります。</span><span class="sxs-lookup"><span data-stu-id="eb705-357">If both structs contain an item with the same name, only the item from the first struct will be included.</span></span>

### <a name="examples---merge"></a><span data-ttu-id="eb705-358">例 - merge</span><span class="sxs-lookup"><span data-stu-id="eb705-358">Examples - merge</span></span>

<span data-ttu-id="eb705-359">次の例では、person と address という 2 つの構造体を作成し、それらを allInfo という新しい構造体にマージします。</span><span class="sxs-lookup"><span data-stu-id="eb705-359">The following example creates two structs called person and address, and then merges them into a new struct called allInfo.</span></span>

```xpp
{ 
    container packedStruct; 
    Struct person = new Struct ("str name; int age"); 
    Struct address = new Struct ("str street; str city; str country"); 
    Struct allInfo; 
    person.value ("name", "Jane Dow"); 
    person.value ("age", 34); 
    address.value ("street", "Downing street 10"); 
    address.value ("country", "Great Britain"); 
    address.value ("city", " London"); 
    allInfo = Struct::merge(person, address); 
    print allInfo.toString(); 
    pause; 
}
```

## <a name="method-new"></a><span data-ttu-id="eb705-360">メソッド new</span><span class="sxs-lookup"><span data-stu-id="eb705-360">Method new</span></span>

<span data-ttu-id="eb705-361">構造体を作成します。</span><span class="sxs-lookup"><span data-stu-id="eb705-361">Creates a struct.</span></span>

```xpp
public void new(VarArg specifier)
```

### <a name="parameters---new"></a><span data-ttu-id="eb705-362">パラメーター - new</span><span class="sxs-lookup"><span data-stu-id="eb705-362">Parameters - new</span></span>

<span data-ttu-id="eb705-363">指定子</span><span class="sxs-lookup"><span data-stu-id="eb705-363">specifier</span></span>  
<span data-ttu-id="eb705-364">文字列として品目の名前の後には、品目のデータ型を指定した 1 つ以上の組み合わせ。</span><span class="sxs-lookup"><span data-stu-id="eb705-364">One or more pairs that specify the data type of an item followed by the name of the item as a string.</span></span>

### <a name="remarks---new"></a><span data-ttu-id="eb705-365">備考 - new</span><span class="sxs-lookup"><span data-stu-id="eb705-365">Remarks - new</span></span>

<span data-ttu-id="eb705-366">項目のデータ型は、プリミティブ データ型の名前を使用するか、システム列挙を使用して指定できます。</span><span class="sxs-lookup"><span data-stu-id="eb705-366">The data type of the item can be specified using the name of a primitive data type or by using the system enum.</span></span> <span data-ttu-id="eb705-367">構造体内の項目は、文字列型、整数型、実数型、日付型、コンテナー型、レコード型、クラス型など、型システムの列挙型にあるデータ型のいずれでもかまいません。</span><span class="sxs-lookup"><span data-stu-id="eb705-367">The items in a struct can be of any of the data types found in the Types system enum, including: string, integer, real, date, container, record, and class.</span></span> <span data-ttu-id="eb705-368">以下の例に説明されているように、Struct.definitionString メソッドを使用して新しい構造体を作成し、構造体のコピーを作成することができます。</span><span class="sxs-lookup"><span data-stu-id="eb705-368">You can create a copy of a struct by using the Struct.definitionString method to create a new struct, as illustrated in the example below.</span></span> <span data-ttu-id="eb705-369">構造体を作成した後は、Struct.add メソッドを使用して新しい項目を追加し、Struct.value または Struct.valueIndex メソッドを使用して構造体に項目の値を設定することができます。</span><span class="sxs-lookup"><span data-stu-id="eb705-369">After you have created a struct, you can add new items using the Struct.add method and set the value of items in the struct by using the Struct.value or Struct.valueIndex method.</span></span>

### <a name="examples---new"></a><span data-ttu-id="eb705-370">例 - new</span><span class="sxs-lookup"><span data-stu-id="eb705-370">Examples - new</span></span>

<span data-ttu-id="eb705-371">次の例では、同じ定義を持つ 2 つの構造体を作成し、2 つの値と追加の項目および値をその 1 つ (s1) に追加します。</span><span class="sxs-lookup"><span data-stu-id="eb705-371">The following example creates two structs with the same definition and then adds 2 values and an additional item and value to one of them (s1).</span></span> <span data-ttu-id="eb705-372">この構造体をコピーして、Struct.definitionString メソッドを使用することにより新しい構造体を作成します。</span><span class="sxs-lookup"><span data-stu-id="eb705-372">This struct is then copied to create a new struct by using the Struct.definitionString method.</span></span>

```xpp
{ 
    Struct s1, s2, s3; 
    // The two constructors below create the same struct 
    s1 = new Struct(Types::Integer, "age", Types::String, "name"); 
    s2 = new Struct ("int age; str name"); 
    // Print the definitions 
    print s1.definitionString(); 
    print s2.definitionString(); 
    s1.value("age", 25); 
    s1.value("name", "Jane Dow"); 
    // Add a field at runtime 
    s1.add("Shoesize", 45); 
    print s1.definitionString(); 
    print s1.toString(); 
    // Create a container with age, name and shoesize, 
    // using definitionString 
    s3 = new struct(s1.definitionString()); 
    print s3.definitionString(); 
    pause; 
}
```

