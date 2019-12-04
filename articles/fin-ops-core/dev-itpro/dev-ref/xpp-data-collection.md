---
title: X++ コレクション クラス
description: このトピックでは、X++のコレクション クラスについて説明します。
author: RobinARH
manager: AnnBe
ms.date: 06/17/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Developer
ms.reviewer: rhaertle
ms.search.scope: Operations
ms.custom: 150183
ms.assetid: 0ff4e759-851d-4b53-aa67-6f03eee53f02
ms.search.region: Global
ms.author: rhaertle
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e8336d8d05abe2267c24aa6aef89edf25dd7f814
ms.sourcegitcommit: 260a820038c29f712e8f1483cca9315b6dd3df55
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/08/2019
ms.locfileid: "2778691"
---
# <a name="x-collection-classes"></a><span data-ttu-id="a251d-103">X++ コレクション クラス</span><span class="sxs-lookup"><span data-stu-id="a251d-103">X++ collection classes</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a251d-104">このトピックでは、X++のコレクション クラスについて説明します。</span><span class="sxs-lookup"><span data-stu-id="a251d-104">This topic describes collection classes in X++.</span></span> 

<span data-ttu-id="a251d-105">X++ 言語の構文には、配列とコンテナーという 2 種類の複合が用意されています。</span><span class="sxs-lookup"><span data-stu-id="a251d-105">The X++ language syntax provides two composite types: arrays and containers.</span></span> <span data-ttu-id="a251d-106">これらの複合型は、プリミティブ型の値を集約するのに便利です。</span><span class="sxs-lookup"><span data-stu-id="a251d-106">These composite types are useful for aggregating values of primitive types.</span></span> <span data-ttu-id="a251d-107">ただし、配列またはコンテナーのクラス オブジェクトを格納することはできません。</span><span class="sxs-lookup"><span data-stu-id="a251d-107">However, you can't store class objects in arrays or containers.</span></span> 

<span data-ttu-id="a251d-108">*コレクション クラス*はオブジェクトの格納に使用されます。</span><span class="sxs-lookup"><span data-stu-id="a251d-108">*Collection classes* are used to store objects.</span></span> <span data-ttu-id="a251d-109">これらは、配列、リスト、セット、マップ、任意のデータ型を保持できる構造、オブジェクトさえも作成できます。</span><span class="sxs-lookup"><span data-stu-id="a251d-109">They let you create arrays, lists, sets, maps, and structs that can hold any data type, even objects.</span></span> <span data-ttu-id="a251d-110">最大パフォーマンスについては、C++ (システム クラス) で、クラスが実装されます。</span><span class="sxs-lookup"><span data-stu-id="a251d-110">For maximum performance, the classes are implemented in C++ (they are system classes).</span></span> <span data-ttu-id="a251d-111">*ファンデーション クラス*と呼ばれていたコレクション クラス。</span><span class="sxs-lookup"><span data-stu-id="a251d-111">Collection classes were previously known as *foundation classes*.</span></span> <span data-ttu-id="a251d-112">コレクション クラスは、**配列**、**リスト**、**マップ**、**設定**、および**構造体**です。</span><span class="sxs-lookup"><span data-stu-id="a251d-112">The collection classes are **Array**, **List**, **Map**, **Set**, and **Struct**.</span></span>

- <span data-ttu-id="a251d-113">**配列** - このクラスは、X++ 言語の**配列**タイプに似ていますが、単一タイプ、オブジェクトおよびレコードの値を保持できます。</span><span class="sxs-lookup"><span data-stu-id="a251d-113">**Array** – This class resembles the **array** type in the X++ language, but it can hold values of any single type, even objects and records.</span></span> <span data-ttu-id="a251d-114">オブジェクトは、特定の順序でアクセスされます。</span><span class="sxs-lookup"><span data-stu-id="a251d-114">Objects are accessed in a specific order.</span></span>
- <span data-ttu-id="a251d-115">**リスト** – このクラスには、順にアクセスされる要素が含まれます。</span><span class="sxs-lookup"><span data-stu-id="a251d-115">**List** – This class contains elements that are accessed sequentially.</span></span> <span data-ttu-id="a251d-116">配列とは異なり、**List** クラスは **addStart** メソッドを提供します。</span><span class="sxs-lookup"><span data-stu-id="a251d-116">Unlike an array, the **List** class provides an **addStart** method.</span></span> <span data-ttu-id="a251d-117">**Set** クラスと同様に、**List** クラスは **getEnumerator** メソッドと **getIterator** メソッドを提供します。</span><span class="sxs-lookup"><span data-stu-id="a251d-117">Like the **Set** class, the **List** class provides the **getEnumerator** and **getIterator** methods.</span></span> <span data-ttu-id="a251d-118">反復子を使用して、**リスト** オブジェクトから項目を挿入および削除することができます。</span><span class="sxs-lookup"><span data-stu-id="a251d-118">You can use an iterator to insert and delete items from a **List** object.</span></span>
- <span data-ttu-id="a251d-119">**マップ** – このクラスはキー値を別の値に関連付けます。</span><span class="sxs-lookup"><span data-stu-id="a251d-119">**Map** – This class associates a key value with another value.</span></span>
- <span data-ttu-id="a251d-120">**設定** – このクラスは、1 つのタイプの値を保持します。</span><span class="sxs-lookup"><span data-stu-id="a251d-120">**Set** – This class holds values of any single type.</span></span> <span data-ttu-id="a251d-121">値は、追加された順序で格納されません。</span><span class="sxs-lookup"><span data-stu-id="a251d-121">Values aren't stored in the sequence in which they are added.</span></span> <span data-ttu-id="a251d-122">代わりに、**Set** オブジェクトは **in** メソッドのパフォーマンスを最適化するように値を格納します。</span><span class="sxs-lookup"><span data-stu-id="a251d-122">Instead, the **Set** object stores the value in a manner that optimizes performance for the **in** method.</span></span> <span data-ttu-id="a251d-123">**セット**オブジェクトは、**セット**オブジェクトが既に格納している値を追加しようとする試みをすべて無視します。</span><span class="sxs-lookup"><span data-stu-id="a251d-123">A **Set** object ignores any attempt to add a value that the **Set** object is already storing.</span></span> <span data-ttu-id="a251d-124">**Set** クラスは、**Array** クラスとは異なり、**in** メソッドと **remove** メソッドを提供します。</span><span class="sxs-lookup"><span data-stu-id="a251d-124">Unlike the **Array** class, the **Set** class provides the **in** and **remove** methods.</span></span>
- <span data-ttu-id="a251d-125">**構造体** – このクラスは、1 つ以上のタイプの値を含めることができます。</span><span class="sxs-lookup"><span data-stu-id="a251d-125">**Struct** – This class can contain values of more than one type.</span></span> <span data-ttu-id="a251d-126">これは、特定のエンティティに関する情報をグループ化するために使用されます。</span><span class="sxs-lookup"><span data-stu-id="a251d-126">It's used to group information about a specific entity.</span></span>

<span data-ttu-id="a251d-127">**構造体**を除くすべてのコレクション クラスのコンストラクターは、**型**システム列挙型の要素である型パラメーターをとります。</span><span class="sxs-lookup"><span data-stu-id="a251d-127">The constructor for every collection class except **Struct** takes a type parameter that is an element of the **Types** system enum.</span></span> <span data-ttu-id="a251d-128">コレクション インスタンスは、その型のアイテムのみを格納できます。</span><span class="sxs-lookup"><span data-stu-id="a251d-128">The collection instance can store items of that type only.</span></span> <span data-ttu-id="a251d-129">**Types::AnyType** 列挙要素は、**Set** オブジェクトなどのコレクション オブジェクトを作成するために使用できない特殊なケースです。</span><span class="sxs-lookup"><span data-stu-id="a251d-129">The **Types::AnyType** enum element is a special case that can't be used to construct a collection object, such as a **Set** object.</span></span> <span data-ttu-id="a251d-130">**null** 値は、**Set** オブジェクトに要素として格納できません。</span><span class="sxs-lookup"><span data-stu-id="a251d-130">The **null** value can't be stored as an element in a **Set** object.</span></span> <span data-ttu-id="a251d-131">また、**マップ** オブジェクトで **null** はキーになることはできません。</span><span class="sxs-lookup"><span data-stu-id="a251d-131">Additionally, **null** can't be a key in a **Map** object.</span></span> <span data-ttu-id="a251d-132">反復子または列挙子を使用して、コレクション オブジェクトを介して反復することができます。</span><span class="sxs-lookup"><span data-stu-id="a251d-132">You can iterate through a collection object by using an iterator or enumerator.</span></span> <span data-ttu-id="a251d-133">反復子を取得する方法を示す一般的な例を次に示します。</span><span class="sxs-lookup"><span data-stu-id="a251d-133">Here are typical examples that show how you can obtain an iterator.</span></span>

    new MapIterator(myMap)
    myMap.getEnumerator()

<span data-ttu-id="a251d-134">**設定**オブジェクトで、任意の要素が追加または反復子が作成された後に削除される場合、反復子インスタンスは読み取りまたはコレクションによるステップで使用されることはなくなります。</span><span class="sxs-lookup"><span data-stu-id="a251d-134">For **Set** objects, if any elements are added or removed after an iterator is created, the iterator instance can no longer be used to read from or step through the collection.</span></span> 

<span data-ttu-id="a251d-135">**マップ**オブジェクトで、**設定**オブジェクトと同じように、任意の要素が削除されると、反復子が有効ではなくなります。</span><span class="sxs-lookup"><span data-stu-id="a251d-135">For **Map** objects, as for **Set** objects, if any elements are removed, the iterator is no longer valid.</span></span> <span data-ttu-id="a251d-136">ただし、キーが新しいか、またはキーが既に存在していてその値のみが**マップ**要素で更新されているかどうかに関係なく、**Map.insert** メソッドへの呼び出し後も、**MapIterator** オブジェクトは有効です。</span><span class="sxs-lookup"><span data-stu-id="a251d-136">However, a **MapIterator** object remains valid even after a call to the **Map.insert** method, regardless of whether the key is new, or whether the key already exists and only the value is being updated in the **Map** element.</span></span> <span data-ttu-id="a251d-137">**Map.insert** を呼び出し、反復子オブジェクトが有効であることに依存するコードは、.NET Framework CIL として実行されると失敗する可能性があります。</span><span class="sxs-lookup"><span data-stu-id="a251d-137">Code that calls **Map.insert** and depends on the iterator object remaining valid might fail if it's run as .NET Framework CIL.</span></span> 

<span data-ttu-id="a251d-138">コレクション クラスを使用するとより複雑なクラスを作成することができます。</span><span class="sxs-lookup"><span data-stu-id="a251d-138">You can use the collection classes to form more complex classes.</span></span> <span data-ttu-id="a251d-139">たとえば、リストの先頭に要素が常に追加されるリストを使用して、スタックを簡単に実装できます。</span><span class="sxs-lookup"><span data-stu-id="a251d-139">For example, you can easily implement a stack by using a list where elements are always added to the beginning of the list.</span></span> <span data-ttu-id="a251d-140">最新の要素がスタックの先頭を占めます。</span><span class="sxs-lookup"><span data-stu-id="a251d-140">The newest element then occupies the top of the stack.</span></span> 

<span data-ttu-id="a251d-141">コレクション クラスを拡張することもできます。</span><span class="sxs-lookup"><span data-stu-id="a251d-141">You can also extend the collection classes.</span></span> <span data-ttu-id="a251d-142">たとえば、**リスト**クラスを拡張して、操作がタイプ セーフである顧客レコードの一覧を作成します。</span><span class="sxs-lookup"><span data-stu-id="a251d-142">For example, you can extend the **List** class to create a list of customer records where the operations are type-safe.</span></span> <span data-ttu-id="a251d-143">この場合、派生したコレクション クラスは顧客レコードのみを受け入れます。</span><span class="sxs-lookup"><span data-stu-id="a251d-143">In this case, the derived collection class will accept only customer records.</span></span>
